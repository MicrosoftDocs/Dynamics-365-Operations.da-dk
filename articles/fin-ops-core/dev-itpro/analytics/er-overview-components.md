---
title: Komponenter i elektronisk rapportering
description: Denne artikel indeholder en beskrivelse af ER-komponenterne (Elektronisk rapportering).
author: kfend
ms.date: 09/28/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58941
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.form: ERWorkspace
ms.openlocfilehash: 4851374ca4943a84d35f063e0ee65b537ec3b6cd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285025"
---
# <a name="electronic-reporting-components"></a>Komponenter i elektronisk rapportering

[!include [banner](../includes/banner.md)]

Elektronisk rapportering (ER) understøtter følgende komponenttyper:

- Datamodel
- Modeltilknytning
- Formater
- Metadata

## <a name="data-model-component"></a>Datamodelkomponent

En datamodelkomponent er en abstrakt repræsentation af en datastruktur. Den beskriver et bestemt forretningsdomæneområde tilstrækkeligt detaljeret til at opfylde kravene til rapportering for det pågældende domæne. En data modelkomponent består af følgende dele:

- **Datamodel** - Et sæt af domænespecifikke forretningsenheder samt en hierarkisk struktureret definition af relationerne mellem enhederne.
- **Modeltilknytning** - Valgte programdatakilder med enkelte elementer i en datamodel, der under kørsel angiver dataflow og regler for angivelse af forretningsdata til en datamodelkomponent.

Forretningsenheden til en datamodel er repræsenteret som en beholder eller post. Egenskaber for forretningsenheden er repræsenteret som dataelementer eller felter. Hvert dataelement har et entydigt navn, etiket, beskrivelse og værdi. Værdien af hvert dataelement kan være udformet, så den kan genkendes som en streng, heltal, reelt tal, dato, fasttekst eller boolesk værdi. Desuden kan dataelementet være en anden post eller postliste.

En enkelt modelkomponent kan indeholde flere hierarkier af domænespecifikke forretningsobjekter. Den kan også indeholde modeltilknytninger, der understøtter et rapportspecifikt dataflow på kørselstidspunktet. Hierarkierne afpasses efter en enkelt post, der er valgt som en rod for modeltilknytningen. Datamodellen for betalingsdomæneområdet kan f.eks. understøtte følgende tilknytninger:


- Virksomhed \> Kreditor \> Betalingstransaktioner for AP-domænet
- Debitor \> Virksomhed \> Betalingstransaktioner for AR-domænet

Forretningsenheder som f.eks firma- og betalingsposteringer angives én gang. Forskellige tilknytninger kan genbruge dem efter behov.

## <a name="model-mapping-component"></a>Komponent til modeltilknytning

Modeltilknytning til programdatakilder med enkelte elementer i en datamodel, der under kørsel angiver dataflow og regler for angivelse af forretningsdata til en datamodelkomponent.

En modeltilknytning, der understøtter udgående elektroniske dokumenter, har følgende muligheder:

- Den kan bruge forskellige datatyper som datakilder til en datamodel. Disse datatyper omfatter tabeller, dataenheder, metoder og fasttekster.
- Den understøtter brugerinputparametre, der kan defineres som datakilder for en datamodel, når data skal angives på kørselstidspunktet.
- Den understøtter datatransformationen til de grupper, der kræves. Du kan også filtrere, sortere og summere data og tilføje logisk beregnede felter, der er designet via formler, der ligner Microsoft Excel-formler. Du kan finde flere oplysninger under [Formeldesigner i elektronisk rapportering (ER)](general-electronic-reporting-formula-designer.md).

En modeltilknytning, der understøtter indgående elektroniske dokumenter, har følgende muligheder:

- Det kan bruge forskellige opdaterbare dataelementer som mål. Disse dataelementer omfatter tabeller, dataenheder og visninger. Dataene kan opdateres ved hjælp af indgående dataene fra de elektroniske dokumenter. Der kan bruges flere destinationer i en enkelt modeltilknytning.
- Den understøtter brugerinputparametre, der kan defineres som datakilder for en datamodel, når data skal angives på kørselstidspunktet.

En datamodelkomponent er udviklet til hvert forretningsdomæne, der bruges som en samlet datakilde til rapportering. Den samlede datakilde afrapporterer fra den fysiske implementering af datakilder. Komponenten repræsenterer domænespecifikke forretningsbegreber og -funktioner i en formular, der gør et rapporteringsformats oprindelige design og yderligere vedligeholdelse mere effektivt.

## <a name="format-component"></a>Formatkomponent

### <a name="format-components-for-outgoing-electronic-documents"></a>Formatkomponenter for udgående elektroniske dokumenter

En formatkomponent er skemaet for rapporteringsoutput, der skal oprettes på kørselstidspunktet. Et skema består af følgende elementer:

- Et format, der definerer strukturen og indholdet af det udgående elektroniske dokument, der oprettes på kørselstidspunktet.
- Datakilder som et sæt brugerinputparametre og en domænespecifik datamodel, der bruger en valgt modeltilknytning.
- En formattilknytning som et sæt bindinger af formatdatakilder, der har enkelte elementer af et format, der angiver dataflow og regler for formatoutputgenerering på kørselstidspunktet.
- En formatvalidering som et sæt konfigurerbare regler, der styrer oprettelsen af rapporten på kørselstidspunktet afhængigt af kørselskonteksten. Eksempelvis kan der være en regel, der standser outputgenerering af en kreditors betalinger og medfører en undtagelse, når bestemte attributter for den valgte kreditor mangler, f.eks. bankkontonummeret.

En formatkomponent understøtter følgende funktioner:

- Oprettelse af rapporteringsoutput som separate filer i forskellige formater, f.eks. tekst, XML, Microsoft Word-dokument eller regneark
- Separat oprettelse af flere filer og indkapsling af disse filer i zip-filer

En formatkomponent gør det muligt at vedhæfte bestemte filer, der kan bruges i rapporteringsoutputtet:

- Excel-projektmapper, der indeholder et regneark, der kan bruges som skabelon for output i regnearksformat OPENXML:
- Word-filer, der indeholder et dokument, der kan bruges som skabelon for output i Microsoft Word-dokumentformatet
- Andre filer kan indgå i formatets output som foruddefinerede filer.

I følgende illustration vises, hvordan dataene flyder for disse formater.

[![Dataflow for udgående formatkomponenter](./media/ER-overview-02.png)](./media/ER-overview-02.png)

For at køre en enkelt ER-formatkonfiguration og generere et udgående elektronisk dokument skal du identificere tilknytningen af formatkonfigurationen.

#### <a name="format-components-for-incoming-electronic-documents"></a>Formatkomponenter for indgående elektroniske dokumenter
En formatkomponent er skemaet for det indgående dokument, der importeres på kørselstidspunktet. Et skema består af følgende elementer:

- Et format, der definerer strukturen og indholdet af det indgående elektroniske dokument, som indeholder data, der importeres på kørselstidspunktet. En formatkomponent bruges til at fortolke et indgående dokument i forskellige formater, f.eks. tekst og XML.
- En formattilknytning, som binder individuelle formateringselementer til elementer i en domænespecifik datamodel. På kørselstidspunktet angiver elementerne i datamodellen dataflowet og reglerne for import af data fra et indgående dokument og gemmer derefter dataene i en datamodel.
- En formatvalidering som et sæt konfigurerbare regler, der styrer import af data på kørselstidspunktet afhængigt af kørselskonteksten. Eksempelvis kan der være en regel, der standser import af data fra et bankkontoudtog, der har en kreditors betalinger og medfører en undtagelse, når en bestemt kreditors attributter mangler, f.eks. kreditor-id-koden.

I følgende illustration vises, hvordan dataene flyder for disse formater.

[![Dataflow for indgående formatkomponenter](./media/ER-overview-03.png)](./media/ER-overview-03.png)

Hvis du vil køre en enkelt ER-formatkonfigurationen for at importere data fra et indgående elektronisk dokument, skal du identificere den ønskede tilknytning af en formatkonfiguration samt integrationspunktet for en modeltilknytning. Du kan bruge den samme modeltilknytning og de samme destinationer sammen med forskellige formater for forskellige typer indgående dokumenter.


## <a name="component-versioning"></a>Komponentversioner

Versionering understøttes for ER-komponenter. Der findes følgende arbejdsgang til håndtering af ændringer i ER-komponenter:

1. Den oprindelige version, der blev oprettet, er markeret som en **Kladde**-version. Denne version kan redigeres og er tilgængelig for testkørsler.
2. **Kladde** versionen kan konverteres til en **Fuldført** version. Denne version kan bruges i lokale rapporteringsprocesser.
3. Versionen **Fuldført** kan konverteres til en **Delt** version. Denne version udgives på Microsoft Dynamics Lifecycle Services (LCS) og kan bruges i globale rapportingsprocesser.
4. Versionen **Delt** kan konverteres til en **Annulleret** version. Denne version kan slettes.

Versioner, der har status som enten **Fuldført** eller **Delt** er tilgængelige for anden dataudveksling. Følgende handlinger kan udføres på en komponent, der har disse statusser:

- Komponenten kan serialiseres i XML-format og eksporteres som en fil i XML-format.
- Komponenten kan reserialiseres fra en XML-fil og importeres til programmet som en ny version af en ER-komponent.

Du kan finde flere oplysninger under [Importere en ny datamodelkonfiguration](er-quick-start1-new-solution.md#ImportDataModel) og [Eksportere den fuldførte version af et afledt format](er-calculated-field-type.md#export-completed-version-of-a-derived-format).

### <a name="draft-versions-at-runtime"></a>Kladdeversioner under kørsel

I dine personlige brugerparametre til ER-strukturen kan du aktivere den indstilling, der giver dig mulighed for at angive, om kladdeversionen af en ER-konfiguration skal bruges under kørslen. Du kan finde oplysninger om, hvordan du gør indstillingen **Kør kladde** tilgængelig for dine ER-konfigurationer, under [Markere et brugerdefineret format som kørbart](er-quick-start2-customize-report.md#MarkFormatRunnable).

> [!NOTE]
> ER-brugerparametre er brugerspecifikke og firmaspecifikke.

### <a name="draft-format-versions-at-runtime"></a>Kladdeformatversioner under kørsel

Når du kører en ER-løsning, ignoreres som standard kladdeversionerne af dens formatkomponenter. I stedet er det kun den relevante version, der har en anden status end **Kladde**, der bruges. Af og til vil du måske tvinge ER til at bruge kladdeversionen af ER-formatkonfigurationen under kørslen. Når du f.eks. har introduceret nødvendige ændringer i kladdeversionen, kan du bruge denne kladdeversion til at udføre testkørslen. På denne måde kan du validere gyldigheden af ændringerne. [Angiv](er-quick-start2-customize-report.md#MarkFormatRunnable) indstillingen **Kør kladde** for den relevante ER-konfiguration til **Ja** for at begynde at bruge kladdeversionen af formatet.

### <a name="draft-model-mapping-versions-at-runtime"></a>Kladdeversioner af modeltilknytning under kørsel

Når du kører en ER-løsning, bruges som standard kladdeversionerne af dens modeltilknytningskomponenter. Af og til vil du måske tvinge ER til at ignorere kladdeversionen af ER-modeltilknytningen under kørslen. I **version 10.0.29 og senere** kan du aktivere funktionen **Tag altid indstillingen "Kør kladde" i betragtning for ER-modeltilknytninger** for at styre den modeltilknytningsversion, der bruges under kørslen. Når denne funktion er aktiveret, forekommer følgende funktionsmåde:

- Når indstillingen **Kør kladde** er angivet til **Nej** for en konfiguration af modeltilknytning, bruges den højeste version, der ikke er kladde, af denne konfiguration under kørslen. En undtagelse opstår, hvis konfigurationen ikke er tilgængelig i den aktuelle Finance-forekomst.
- Når indstillingen **Kør kladde** er angivet til **Ja** for en konfiguration af modeltilknytning, bruges kladdeversionen af denne konfiguration under kørslen.

## <a name="component-date-effectivity"></a>Komponentens datogyldighed

ER-formatkomponentversioner har en ikrafttrædelsesdato. Du kan indstille datoen "Gyldig fra" for en ER-formatkomponent for at angive startdatoen, hvor komponenten træder i kraft for rapporteringsprocesser. Programsessionsdatoen bruges til at definere, om en komponent er gyldig til udførelse. Hvis mere end én version er gyldig for en bestemt dato, bruges den nyeste version til rapporteringsprocesser.

## <a name="component-access"></a>Komponentadgang

Adgangen til ER-format- og modeltilknytningskomponenter ved kørsel afhænger af indstillingen for ISO-lande-/områdekoden (International Organization for Standardization). Hvis denne indstilling er tom for en valgt version af en format- eller modeltilknytningskonfiguration, kan en format- eller modeltilknytningskomponent åbnes fra ethvert firma på kørselstidspunktet. Hvis denne indstilling indeholder ISO-land/område-koder, er en format- eller modeltilknytningskomponent kun tilgængelig fra firmaer, der har en primær adresse, som er defineret for en af en formatkomponents ISO-land/område-koder.

Forskellige versioner af en format- eller modeltilknytningskomponent kan have forskellige indstillinger for ISO-land/område-koder.

Du kan få flere oplysninger i [Konfigurere landekontekstafhængige ER-modeltilknytninger](er-country-dependent-model-mapping.md).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

