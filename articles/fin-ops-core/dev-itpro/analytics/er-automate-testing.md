---
title: Automatisere test med elektronisk rapportering
description: I dette emne forklares det, hvordan du kan bruge grundlagsfunktionen for elektronisk rapporteringsstruktur (ER) til at automatisere test af nogle funktioner.
author: NickSelin
manager: AnnBe
ms.date: 07/02/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERFormatBaselineTable, ERFormatMappingRunLogTable, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 503d4ca562df5c60ee7c475ac146dffbe0edc0c9
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569039"
---
# <a name="automate-testing-with-electronic-reporting"></a>Automatisere test med elektronisk rapportering

[!include[banner](../includes/banner.md)]

I dette emne forklares det, hvordan du kan bruge den elektroniske rapporteringsstruktur (ER) til at automatisere test af nogle funktioner. I eksemplet i dette emne kan du se, hvordan du kan automatisere testen af kreditorbetalingsbehandling.

Programmet bruger ER-strukturen til at generere betalingsfiler og tilsvarende dokumenter under behandling af leverandørbetalinger. ER-strukturen består af en datamodel, modeltilknytninger og formatkomponenter, der understøtter betalingsbehandling af forskellige betalingstyper og generering af dokumenter i forskellige formater. Disse komponenter kan downloades fra Microsoft Dynamics Lifecycle Services (LCS) og importeres til forekomsten.

Du kan også tilpasse de enkelte Microsoft-komponenter og bruge dem som basis for din egen tilpassede komponent. Ved at oprette en tilpasset version kan du foretage ændringer, der understøtter bestemte krav. Du kan f.eks. justere ER-datamodellen og ER-modeltilknytningen til at få adgang til kundespecifikke programdata, eller du kan ændre et ER-format for at ændre layoutet af et genereret dokument.

Du kan bruge tilpassede ER-formater til at behandle betalingsfiler, der genererer leverandørbetalinger, og som også skal behandle kontrolrapporter. Versionering understøttes i ER-komponenter. Microsoft kan derfor levere opdaterede versioner af ER-løsninger til behandling af kreditorbetalinger, og du kan automatisk flette den opdaterede version med den tilpassede komponent ved at rebasere den. Du skal dog teste den rebaserede version for at sikre, at den fungerer efter hensigten.

ER-datamodeller og ER-modeltilknytninger er fælles for mange ER-formater, der bruges til at behandle betalinger af forskellige typer og til at oprette land/område-specifikke betalingsdokumenter. Derfor er det meget ønskeligt at automatisere test af brugeraccept og integration, så det automatisk udføres i flere virksomheder, men som tager hensyn til land/område-konteksten for hvert af de pågældende destinationsfirmaer, bruger forskellige datasæt osv.

Du kan finde flere oplysninger om, hvordan du opretter en tilpasset version af et format, der er baseret på det format, du har modtaget fra en konfigurationsudbyder, i [Opgradere dit ER-format ved at bruge en ny basisversion af formatet](./tasks/er-upgrade-format.md).

## <a name="key-concepts"></a>Nøglebegreber

Funktionelle superbrugere kan oprette test af brugeraccept og-integration uden at skulle skrive kildekode.

- Brug den grundlæggende ER-funktion til at sammenligne genererede dokumenter med masterkopier. Du kan finde flere oplysninger under [Spore genererede rapportresultater og sammenligne dem med basisværdier](er-trace-reports-compare-baseline.md).
- Brug Arbejdsrutineoptager til at registrere testsager og inkludere basisvurdering. Du kan finde flere oplysninger under [Arbejdsrutineoptagerressourcer](../user-interface/task-recorder.md).
- Gruppér testsager for nødvendige testsituationer. Du kan finde flere oplysninger under [Opret og automatiser test af brugeraccept](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md).

    - Brug Forretningsmodeldesigner (BPM) i LCS til at oprette biblioteker til test af brugeraccept.
    - Brug BPM-testbiblioteker til at oprette en testplan og testpakker i Microsoft Azure DevOps Services (Azure DevOps).

Funktionelle superbrugere kan køre test af brugeraccept og -integration.

- Brug Regression Suite Automation Tool (RSAT) til at køre testsager af den ønskede testpakke.
- Rapportér resultaterne af testen til Azure DevOps, og brug denne tjeneste til at undersøge disse resultater.

## <a name="prerequisites"></a>Forudsætninger

Før du kan fuldføre opgaverne i dette emne, skal du fuldføre følgende forudsætninger:

- Implementer en topologi, der understøtter testautomatisering. Du skal have adgang til forekomsten af denne topologi for rollen **Systemadministrator**. Denne topologi skal indeholde de demodata, der vil blive brugt i dette eksempel. Du kan finde flere oplysninger under [Installer og anvend et miljø, som understøtter fortløbende build og automatisering af test](../perf-test/continuous-build-test-automation.md).
- Hvis du vil køre test af brugergodkendelse og -integration automatisk, skal du installere RSAT i den topologi, du bruger, og konfigurere den på en passende måde. Du kan finde oplysninger om, hvordan du installerer og konfigurerer RSAT og konfigurerer den til at virke sammen Finance and Operations-apps og Azure DevOps, i [Regression Suite Automation Tool](https://www.microsoft.com/download/details.aspx?id=57357). Vær opmærksom på forudsætningerne for at bruge værktøjet. I følgende illustration vises et eksempel på RSAT-indstillingerne. Det blå rektangel omgiver de parametre, der er angivet for adgang til Azure DevOps. Det grønne rektangel omgiver de parametre, der angiver adgangen til forekomsten.

    ![RSAT-indstillinger](media/GER-Configure.png "Skærmbillede af dialogboksen RSAT-indstillinger")

- Hvis du vil organisere testsager i pakker for at hjælpe med at sikre den korrekte kørselssekvens, så du kan indsamle logfiler med testkørsler til yderligere rapportering og undersøgelse, skal du have adgang til Azure DevOps fra den installerede topologi.
- Hvis du vil fuldføre eksemplet i dette emne, anbefales du at downloade [ER-brug for RSAT-test](https://go.microsoft.com/fwlink/?linkid=874684). Denne zip-fil indeholder følgende opgaveguider:

    | Indhold                                           | Filens navn og placering |
    |---------------------------------------------------|------------------------|
    | Eksempel på opgaveregistrering for at forberede data til test | Forberede\\Registrering.xml |
    | Eksempel på opgaveregistrering for at behandle kreditorbetaling   | Behandle\\Registrering.xml |

## <a name="prepare-the-accounts-payable-module-to-process-vendor-payments"></a>Forberede modulet Kreditor til behandling af kreditorbetalinger

1. Log på din forekomst.
2. Download følgende ER-konfigurationer fra LCS. Der er instruktioner under [Importere ER-konfiguration fra Lifecycle Services](./tasks/er-import-configuration-lifecycle-services.md).

    - **Betalingsmodel** ER-modelkonfigurationen
    - **Betalingsmodel-tilknytning 1611** Konfiguration af ER-modeltilknytning
    - **BACS (UK)** ER-formatkonfiguration

    ![Konfigurationer for elektronisk rapportering](media/GER-Configurations.png "Skærmbillede af siden Konfigurationer i elektronisk rapportering")

3. Vælg det **GBSI**-demodatafirma, som har en land/område-kontekst i Storbritannien.
4. Konfigurer kreditorparametre:

    1. Gå til **Kreditor \> Opsætning af betaling \> Betalingsmåder**.
    2. Vælg betalingsmetoden **Elektronisk**.
    3. Konfigurer den valgte betalingsmåde, så den bruger ER-formatet **BACS (UK)**, som du har downloadet tidligere til behandling af kreditorbetalinger:

        1. Brug oversigtspanelet **Filformater** til at angive indstillingen **Generisk elektronisk eksportformat** til **Ja**.
        2. Vælg **BACS (UK)** i feltet **Eksportér formatkonfiguration**.

    ![Side med betalingsmetoder](media/GER-APParameters.png "Skærmbillede af siden Betalingsmetoder")

    > [!NOTE]
    > Hvis du har den afledte version af dette ER-format, der er oprettet for at understøtte tilpasninger, kan du vælge denne konfiguration i **Elektronisk** betalingsmåde.

5. Opret et eksempel på en kreditorbetaling:

    1. Gå til **Kreditor \> Betalinger \> Betalingskladde**.
    2. Kontrollér, at du ikke har bogført betalingskladden.

        ![Side med betalingskladde](media/GER-APJournal.png "Skærmbillede af siden Betalingskladde")

    3. Vælg **Linjer**, og angiv en linje med følgende oplysninger.

        | Felt               | Eksempelværdi   |
        |---------------------|-----------------|
        | Navn på kreditor         | GB\_SI\_000001  |
        | Debet               | 1,000.00        |
        | Valuta            | GBP             |
        | Modkontotype | Bank            |
        | Modkonto      | GBSI OPER       |
        | Betalingsmåde   | Elektronisk      |

    ![Side med leverandørbetalinger](media/GER-APJournalLines.png "Skærmbillede af siden Leverandørbetalinger")

## <a name="prepare-the-er-framework-to-test-vendor-payment-processing"></a>Forberede ER-strukturen til at teste behandling af kreditorbetaling

### <a name="configure-er-parameters"></a>Konfigurere ER-parametre

1. Gå til **Virksomhedsadministration \> Elektronisk rapportering \> Parametre til elektronisk rapportering**.
2. Under fanen **Vedhæftede filer** i feltet **Grundlag** skal du vælge **Fil** som den dokumenttype, som dokumentstyringsstrukturen (DM) bruger til at holde på dokumenter, der er relateret til basisfunktionen, som vedhæftede DM-filer.

    ![Siden Parametre til elektronisk rapportering](media/GER-ERParameters.png "Skærmbillede af siden Elektroniske rapporteringsparametre")

### <a name="generate-baseline-copies-of-vendor-paymentrelated-documents"></a>Generere basiskopier af kreditorbetaling – relaterede dokumenter

1. Gå til **Kreditor \> Betalinger \> Betalingskladde**.
2. Vælg **Linjer**.
3. Vælg **Opret betalinger**.
4. Vælg betalingsmetoden **Elektronisk**.
5. Vælg bankkontoen **GBSI OPER**
6. Angiv indstillingen **Udskriv kontrolrapport** til **Ja**.
7. Download det genererede output som en zip-fil.
8. Åbn den downloadede fil.
9. Udtræk følgende filer fra den downloadede fil:

    - **Fil**: betalingsfil i tekstformat
    - **ERVendOutPaymControlReport**: kontrolrapportfil i xlsx-format

    ![Udpakkede filer](media/GER-APJournalProcessed.png "Skærmbillede af udtrukket filnavne i Windows Stifinder")

### <a name="turn-on-the-er-baseline-feature"></a>Slå funktionen for ER-grundlag til

1. Gå til **Virksomhedsadministration \> Elektronisk rapportering \> Konfigurationer**.
2. I handlingsruden skal du på fanen **Konfigurationer** vælge **Brugerparametre**.
3. Angv indstillingen **Kør i fejlfindingstilstand** til **Ja**.

Når du aktiverer parameteren **Kør i fejlfindingstilstand**, tvinger du ER-strukturen til at udføre følgende handlinger efter udførelse af ethvert ER-format, der genererer udgående dokumenter:

1. Bestem, om der er konfigureret et grundlag for nogen af komponenterne i det afviklede ER-format.
2. Bestem, om hvert konfigurerede grundlag gælder under de aktuelle betingelser (firmakoden for det firma, der er logget på, og filnavnet og filtypenavnet for det genererede output osv.).
3. Udfør følgende handlinger for hvert relevante grundlag:

    1. Sammenlign det output, der genereres under kørslen af ER-formatet, med det tilsvarende grundlag.
    2. Gem resultaterne af sammenligningen i fejlfindingsloggen for ER-konfigurationer.

### <a name="configure-er-baselines-for-vendor-payment-processing"></a>Konfigurere ER-grundlag til behandling af kreditorbetalinger

1. Gå til **Virksomhedsadministration \> Elektronisk rapportering \> Konfigurationer**.
2. Vælg **Grundlag**.
3. Vælg **Ny**.
4. Vælg formatet **BACS (UK)** i feltet **Reference**.
5. Vælg **Vedhæftede filer**.
6. Tilføj et nyt grundlag for kreditorbetalingsfilen:

    1. Vælg **Ny**.
    2. Vælg den **Fil**-DM-dokumenttype i feltet **Type**, du har konfigureret i ER-parametrene til lagring af grundlæggende artefakter.
    3. Naviger for at vælge den lokalt gemte **Fil**-betalingsfil i tekstformat.
    4. I feltet **Beskrivelse** skal du angive **TXT-betalingsfil**.

7. Tilføj et nyt grundlag for kontrolrapporten til kreditorbetalingen:

    1. Vælg **Ny**.
    2. Vælg den **Fil**-DM-dokumenttype i feltet **Type**, du har konfigureret i ER-parametrene til lagring af grundlæggende artefakter.
    3. Naviger for at vælge den lokalt gemte **ERVendOutPaymControlReport**-kontrolrapportfil i xlsx-format.
    4. I feltet **Beskrivelse** skal du angive **XLSX-betalingskontrolrapport**.

    ![Basislinjer for leverandørbetalingsfiler og kontrolrapport](media/GER-BaselineAttachments.png "Skærmbillede af siden Konfigurationer med rapporten Betalingskontrol XLSX valgt")

8. Luk siden.
9. Vælg **Nyt** i oversigtspanelet **Grundlag** for at konfigurere et grundlag for betalingsfilen:

    1. Navngiv linjen **Indstilling af grundlag for betalingsfil**.
    2. Vælg **Fil** i feltet **Filkomponentnavn** for at anvende dette grundlag på det ER-formatoutput, der genererer betalingsfilen i tekstformatet BACS (UK).
    3. I feltet **Firmaer** skal du vælge **GBSI** for at anvende dette grundlag, når **BACS (UK)** ER-formatet køres i GBSI-firmaet.
    4. Brug feltet **Filnavnsmaske** til at angive **\*.TXT** for kun at anvende dette grundlag på output i **fil**-formatkomponenten, der har filtypenavnet **.txt**.
    5. Vælg **TXT-betalingsfil** i feltet **Grundlag**, så dette grundlag bruges til sammenligning med det genererede output.

10. Vælg **Ny** for at konfigurere et grundlag for kontrolrapporten:

    1. Navngiv linjen **Indstilling af grundlag for kontrolrapport**.
    2. Vælg **ERVendOutPaymControlReport** i feltet **Filkomponentnavn** for at anvende dette grundlag på det ER-formatoutput, der genererer kontrolrapporten.
    3. I feltet **Firmaer** skal du vælge **GBSI** for at anvende dette grundlag, når **BACS (UK)** ER-formatet køres i GBSI-firmaet.
    4. Brug feltet **Filnavnsmaske** til at angive **\*.XLSX** for kun at anvende dette grundlag på output i **ERVendOutPaymControlReport**-formatkomponenten, der har filtypenavnet **.xslx**.
    5. Vælg **XLSX-betalingskontrolrapport** i feltet **Grundlag**, så dette grundlag bruges til sammenligning med det genererede output.

    ![Basislinjers oversigtspanel på siden Konfigurationer](media/GER-BaselineRules.png "Skærmbillede af oversigtspanelet Basislinjer på Konfigurationsside")

## <a name="record-tests-to-validate-vendor-payment-processing"></a>Registrere test for at validere behandling af kreditorbetaling

Som funktionel superbruger kan du registrere dine egne trin for at teste behandling af leverandørbetaling. Det anbefales, at du afspiller (og redigerer, efter behov) opgaveregistreringen **Forberede\\Registrering.xml**, som du har downloadet tidligere. Denne registrering bruges til at indstille alle testdata til den korrekte tilstand. Dette trin er nødvendigt, fordi testen kan udføres mange gange, og alle test skal bruge data, der findes i samme tilstand.

### <a name="reset-user-settings"></a>Nulstille brugerindstillinger

1. Åbn standarddashboardet.
2. Vælg knappen **Indstillinger** (tandhjulsymbolet).
3. Vælg **Brugerindstillinger**.
4. Vælg **Brugsdata**.
5. Vælg **Nulstil**.
6. Vælg **Ja** for at bekræfte, at du vil nulstille brugsdata.
7. Luk siden.

### <a name="record-the-steps-to-prepare-data-for-testing"></a>Registrere de trin, der skal forberede data til test

1. Vælg knappen **Indstillinger** (tandhjulsymbolet).
2. Vælg **Arbejdsrutineoptager**.
3. Vælg **Afspil registrering**.
4. Vælg **Åbn fra denne pc**.
5. Vælg **Gennemse**, og vælg den lokalt gemte fil **Forberede\\Registrering.xml**.
6. Vælg **Start**.
7. Bliv ved med at vælge **Afspil næste ventende trin**, indtil alle trin i registreringen er blevet afspillet.

Denne opgaveregistrering udfører følgende handlinger:

1. Angiv status for den behandlede betalingslinje til **Ingen**.

    ![Opgaveregistrering trin 3 til 4](media/GER-Recording1Review1.png "Skærmbillede af opgaveregistrering trin 3 til 4")

2. Aktivér ER-brugerparameteren **Kør i fejlfindingstilstand**.

    ![Opgaveregistrering trin 9 til 10](media/GER-Recording1Review2.png "Skærmbillede af opgaveregistrering trin 9 til 10")

3. Ryd op i den ER-fejlfindingslog, som indeholder resultaterne af sammenligningen af oprettede filer med grundlag.

    ![Opgaveregistrering trin 13 til 15](media/GER-Recording1Review3.png "Skærmbillede af opgaveregistrering trin 13 til 15")

### <a name="record-the-steps-to-test-vendor-payment-processing"></a>Registrere trin for at teste behandling af kreditorbetaling

Det anbefales, at du afspiller (og redigerer, efter behov) opgaveregistreringen **Behandle\\Registrering.xml**, som du har downloadet tidligere. Denne registrering bruges til at behandle kreditorbetalinger og validere resultaterne af sammenligningen af genererede dokumenter med de tilsvarende grundlag.

1. Vælg knappen **Indstillinger** (tandhjulsymbolet).
2. Vælg **Arbejdsrutineoptager**.
3. Vælg **Afspil registrering**.
4. Vælg **Åbn fra denne pc**.
5. Vælg **Gennemse**, og vælg den lokalt gemte fil **Behandle\\Registrering.xml**.
6. Vælg **Start**.
7. Bliv ved med at vælge **Afspil næste ventende trin**, indtil alle trin i registreringen er blevet afspillet.

Denne opgaveregistrering udfører følgende handlinger:

1. Start behandling af kreditorbetaling.
2. Vælg de korrekte kørselsparametre, og aktivér generering af en kontrolrapport.

    ![Opgaveregistrering trin 3 til 8](media/GER-Recording2Review1.png "Skærmbillede af opgaveregistrering trin 3 til 8")

3. Åbn ER-fejlfindingsloggen for at registrere resultaterne af sammenligningen af genereret output med grundlag.

    I ER-fejlfindingsloggen vises resultaterne af sammenligningen i **Genereret**-tekstfeltet. Felterne **Formatkomponent** og **Formatsti, der medførte en post i logfil** refererer til den filkomponent, for hvilken det genererede output er sammenlignet med grundlaget.

    ![Posteringer på siden Kørselslogge for elektronisk rapportering](media/GER-ERDebugLog.png "Skærmbillede af posteringer på siden Kørselslogge for elektronisk rapportering")

4. Sammenligningen af det aktuelle output med grundlaget registreres ved at bruge indstillingen **Valider** for Arbejdsrutineoptager og vælge **Aktuel værdi**.

    ![Bruge indstillingen Valider til at sammenligne med den aktuelle værdi](media/GER-TRRecordValidation.png "Skærmbillede af anvendelse af indstillingen Valider til at sammenligne med den aktuelle værdi")

    I følgende illustration vises det, hvordan de registrerede valideringstrin ser ud i opgaveregistreringen.

    ![Opgaveregistrering trin 13 og 15](media/GER-Recording2Review2.png "Skærmbillede af opgaveregistrering trin 13 og 15")

## <a name="add-the-recorded-tests-to-azure-devops"></a>Tilføje de registrerede test i Azure DevOps

1. Åbn Azure DevOps-miljøet.
2. Vælg det projekt, du har defineret i RSAT-parametrene, da du [konfigurerede værktøjet](#prerequisites).
3. Vælg den testplan, du har defineret i RSAT-parametrene, da du [konfigurerede værktøjet](#prerequisites).
4. Opret en ny testsag til den valgte testplan:

    1. Navngiv testsagen **Forberede data til testbehandling af kreditors elektroniske betaling**.
    2. Vedhæft filen **Registrering.xml** fra den **Forberede**-mappe, du har downloadet tidligere.

5. Opret en ny testsag til den valgte testplan:

    1. Navngiv testsagen **Test behandling af kreditorbetalinger ved hjælp af ER-format BACS (UK)**.
    2. Vedhæft filen **Registrering.xml** fra den **Behandle**-mappe, du har downloadet tidligere.

    ![Nye testsager for den valgte testplan](media/GER-RSAT-DevOps-Tests-Passed.png "Skærmbillede af de nye testsager for den valgte testplan")

> [!NOTE]
> Vær opmærksom på den korrekte udførelsesrækkefølge af de test, der er tilføjet.

## <a name="prepare-rsat-to-run-the-recorded-tests"></a>Forberede RSAT til at køre de registrerede test

### <a name="load-the-tests-from-azure-devops-to-rsat"></a>Indlæs testene fra Azure DevOps til RSAT

1. Åbn det lokale RSAT-program i den aktuelle topologi.
2. Vælg **Indlæs** for at indlæse de test, der aktuelt findes i Azure DevOps, i RSAT.

    ![Test indlæst i RSAT](media/GER-RSAT-RSAT-Tests-Loaded.png "Skærmbillede af de test, der er indlæst i RSAT")

### <a name="create-automation-and-parameters-files"></a>Oprette automatisering og parameterfiler

1. Vælg de test, du har indlæst fra Azure DevOps, i RSAT.
2. Vælg **Ny** for at oprette RSAT-automatiserings- og parameterfiler.

    ![RSAT-automatisering og parameterfiler oprettede i RSAT](media/GER-RSAT-RSAT-Tests-Initiated.png "Skærmbillede af RSAT-automatisering og parameterfiler oprettede i RSAT")

### <a name="modify-the-parameters-files"></a>Redigere parameterfilerne

1. Vælg testsagen **Forberede data til testbehandling af kreditors elektroniske betaling** i RSAT.
2. Vælg **Rediger**.
3. I den Microsoft Excel-projektmappe, der åbnes, skal du i regnearket **Generelt** ændre firmakoden til **GBSI**, da dette firma skal bruges til testkørslen.
4. Vælg testsagen **Test behandling af kreditorbetalinger ved hjælp af ER-format BACS (UK)** i RSAT.
5. Vælg **Rediger**.
6. I den Excel-projektmappe, der åbnes, skal du i regnearket **Generelt** ændre firmakoden til **GBSI**.
7. I regnearket **ERFormatMappingRunLogTable** skal du bemærke, at cellerne A:3 og C:3 indeholder teksten fra felterne i ER-fejlfindingslogtabellen, der bruges til at validere resultaterne af sammenligningen af outputtet med grundlaget. Disse tekster bruges til at evaluere poster i ER-fejlfindingsloggen, som oprettes under testkørslen.

    ![Regneark med ERFormatMappingRunLogTable](media/GER-RSAT-RSAT-ExcelParameters.png "Skærmbillede af ERFormatMappingRunLogTable-regnearket")

## <a name="run-the-tests-and-analyze-the-results"></a>Køre testene, og analysere resultaterne

### <a name="run-the-tests-in-rsat"></a>Køre testene i RSAT

1. Vælg de indlæste test i RSAT.
2. Vælg **Kør**.

Bemærk, at testsager automatisk køres i programmet ved hjælp af en webbrowser.

### <a name="analyze-the-results-of-test-execution"></a>Analysere resultaterne af testkørsel

Resultaterne af testkørslen gemmes i RSAT. Bemærk, at begge test blev bestået.

![Test, der bestod i RSAT](media/GER-RSAT-RSAT-Tests-Passed.png "Skærmbillede af test, der er bestået i RSAT")

Bemærk, at resultaterne af testkørslen også sendes til Azure DevOps, så du kan foretage yderligere analyser.

![Resultater af udførelse af test i Azure DevOps](media/GER-RSAT-DevOps-Tests-Added.png "Skærmbillede af resultaterne af testudførelsen i Azure DevOps")

### <a name="simulate-a-situation-where-tests-fail"></a>Simulere en situation, hvor test mislykkes

Denne testpakke skal mislykkes, når mindst et af de genererede output ikke matcher det tilsvarende grundlag. For at opnå denne situation kan du bruge den afledte version af formatet **BACS (UK)**, der genererer en betalingsfil, der har et andet indhold end det tilsvarende grundlag. Hvis du vil simulere denne situation, kan du bruge samme **BACS (UK)**-format, men ændre betalingsbeløbet på den behandlede betalingslinje.

1. Åbn programmet og gå til **Kreditorer \> Betalinger \> Betalingskladde**.
2. Vælg **Linjer**.
3. Vælg betalingslinjen, og vælg derefter **Betalingsstatus \> Ingen**.
4. I feltet **Debet** skal du ændre værdien fra **1.000,00** til **2.000,00**.
5. Vælg **Gem** for at gemme ændringerne.

### <a name="run-the-tests-in-rsat"></a>Køre testene i RSAT

1. Vælg de indlæste test i RSAT.
2. Vælg **Kør**.

Bemærk, at testsager automatisk køres i programmet ved hjælp af en webbrowser.

### <a name="analyze-the-results-of-test-execution"></a>Analysere resultaterne af testkørsel

Resultaterne af testkørslen gemmes i RSAT. Bemærk, at den anden test mislykkedes under den anden kørsel.

![Mislykkede testresultater i RSAT](media/GER-RSAT-RSAT-Tests-Failed.png "Skærmbillede af resultaterne af den mislykkede testudførelsen RSAT")

Bemærk, at resultaterne af testkørslen også sendes til Azure DevOps, så du kan foretage yderligere analyser.

![Mislykkede testresultater i Azure DevOps](media/GER-RSAT-DevOps-Tests-Failed.png "Skærmbillede af resultaterne af den mislykkede testudførelse i Azure DevOps")

Du kan få adgang til status for hver test. Du kan også få adgang til kørselsloggen, så du kan analysere årsagerne til eventuelle fejl. I følgende illustration viser kørselslogfilen, at fejlen opstod på grund af forskellen i indhold mellem den genererede betalingsfil og dens grundlag.

![Udførelseslogfil for analysefejl i Azure DevOps](media/GER-RSAT-DevOps-Tests-Failed-Log.png "Skærmbillede af kørselsloggen for analyse af fejl i Azure DevOps")

Som du har set, kan ER-formatets funktionsmåde evalueres automatisk ved hjælp af RSAT som testplatform og ved hjælp af Arbejdsrutineoptager-baserede testsager, der bruger ER-grundlagsfunktionen.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Ressourcer til arbejdsrutineoptager](../user-interface/task-recorder.md)
- [Regression Suite Automation Tool](https://www.microsoft.com/download/details.aspx?id=57357)
- [Oprette og automatisere test af brugeraccept](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md)
- [Installer og anvend et miljø, der understøtter fortløbende build og automatisering af test](../perf-test/continuous-build-test-automation.md)
- [Spore genererede rapportresultater og sammenligne dem med basisværdier](er-trace-reports-compare-baseline.md)
- [ER Opgradere dit format ved at bruge en ny basisversion af formatet](tasks/er-upgrade-format.md)
- [Importere ER-konfiguration fra Lifecycle Services](tasks/er-import-configuration-lifecycle-services.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]