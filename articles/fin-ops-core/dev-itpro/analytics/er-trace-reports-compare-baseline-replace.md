---
title: Forbedringer i sporing af resultaterne fra genererede ER-rapporter og sammenligning af dem med basisværdier
description: Dette emne indeholder oplysninger om, hvordan funktionen for ER-grundlag er blevet forbedret Microsoft Dynamics 365 for Finance and Operations i version 10.0.3 (juni 2019).
author: NickSelin
manager: AnnBe
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: a260be0f8659106907b26bf69bee3b33b09d0c24
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2181329"
---
# <a name="improvements-in-tracing-the-results-of-generated-er-reports-and-comparing-them-with-baseline-values"></a>Forbedringer i sporing af resultaterne fra genererede ER-rapporter og sammenligning af dem med basisværdier

[!include[banner](../includes/banner.md)]

Dette emne beskriver det første sæt forbedringer, der er foretaget i grundlagsfunktionen i ER-strukturen (Electronic reporting). Disse forbedringer er tilgængelige i Microsoft Dynamics 365 for Finance and Operations version 10.0.3 (juni 2019) og nyere.

## <a name="automate-the-setting-of-baseline-rules"></a>Automatiser indstillingen af regler for grundlag

Emnet [Spore genererede rapportresultater og sammenligne dem med basisværdier](er-trace-reports-compare-baseline.md) forklarer, hvordan du kan konfigurere ER-strukturen til at indsamle oplysninger om udførelser af ER-formater og evaluering af resultaterne af disse udførelser. Eksemplet i dette emne beskriver de trin, der skal udføres.

Her er nogle af trinnene:

- Kør et ER-format for at oprette en udgående fil, og gem filen lokalt.
- Tilføj den lokalt gemte fil som en vedhæftet fil til det grundlag, der blev føjet til et ER-format.
- Konfigurer grundlagsreglen for det tilføjede grundlag. Denne konfiguration omfatter følgende trin:

    - Angiv et ER-formatelement, der bruges til at generere en udgående fil.
    - Vælg den vedhæftede fil, der refererer til den genererede udgående fil.

> [!NOTE]
> Disse trin skal udføres manuelt, selvom de nye ER-funktioner gør det muligt at automatisere dem. Hvis du vil vide mere om denne funktion, skal du udføre følgende eksempel.

## <a name="example-automate-the-setting-of-baseline-rules"></a>Eksempel: Automatiser indstillingen af regler for grundlag

Hvis du vil udføre trinnene i dette eksempel, skal du først fuldføre trinenne i eksemplet [Spore genererede rapportresultater og sammenligne dem med basisværdier](er-trace-reports-compare-baseline.md) til og med afsnittet "Tilføj et nyt grundlag for designet ER-format".

### <a name="review-added-baseline"></a>Gennemse tilføjet grundlag

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. Vælg **Grundlag**.

    > [!NOTE]
    > Knappen **Grundlag** i handlingsruden er kun tilgængelig, når brugerparameteren  **Kør i fejlfindingstilstand** er aktiveret for det aktuelle firma.

Grundlaget er blevet tilføjet for det valgte **Format til at lære ER-grundlag**, men grundlagsreglerne er endnu ikke blevet tilføjet for dette grundlag.

![Siden Grundlag for elektronisk rapporteringsformat](media/GER-BaselineSample-AddBaseline2.PNG "Skærmbillede af siden Grundlag for elektronisk rapporteringsformat")

### <a name="make-a-new-baseline-rule"></a>Opret en ny grundlagsregel

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. Udvid **Model til at lære ER-grundlag** i træet.
3. Vælg **Model til at lære ER-brundlag\\Format til at lære ER-grundlag** i træet.
4. Gå til oversigtspanelet **Versioner**, og vælg **Kør**.
5. Gå til feltet **Angiv id**, og angiv **1**.
6. Angiv indstillingen **Opret grundlagsfiler** til **Ja**.
7. Vælg **OK**.

    ![Dialogboksen Parametre for elektronisk rapportering](media/GER-BaselineSample-FormatRunToMakeBaselineFile3.PNG "Skærmbillede af dialogboksen Parametre for elektronisk rapportering")

8. Vælg **Grundlag**.

    ![Siden Grundlag for elektronisk rapporteringsformat](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "Skærmbillede af siden Grundlag for elektronisk rapporteringsformat")

    Den genererede udgående fil er automatisk blevet knyttet til grundlaget i det udførte ER-format. Grundlagsreglen er automatisk blevet føjet til dette grundlag og indeholder også referencen til den vedhæftede fil.

9. Angiv **Grundlag1** i feltet **Navn**.
10. Gå til feltet **Filnavnsmaske**, og angiv **.xml**.
11. Vælg **Gem**.

### <a name="run-the-format"></a>Køre formatet

Du er nu klar til at fuldføre de resterende trin i emnet [Spore genererede rapportresultater og sammenligne dem med basisværdier](er-trace-reports-compare-baseline.md) med start fra afsnittet "Kør det designede ER-format, og gennemse logfilen for at analysere resultaterne".

> [!NOTE]
> Når du sletter den automatisk tilføjede grundlagsregel på oversigtspanelet **Grundlag**, slettes den refererede vedhæftede fil ikke automatisk.

## <a name="configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a>Konfigurer grundlinjen, så den hele tiden ignorerer ændringer i dele af ER-outputtet

Når et ER-format er designet til at indeholde oplysninger, der ændres, når formatet køres, skal formatet være obligatorisk, før du kan bruge funktionen til grundlag til at sammenligne de genererede resultater med basisværdier. Oplysningerne kan f. eks. være behandlingsdatoen og -tidspunktet eller det entydige id for et genereret dokument i forskellige formater (globally unique identifier \[GUID\] osv). De nye ER-funktioner giver dig mulighed for at konfigurere grundlagsreglen, så den ignorerer de elementer i et ER-format, der kan ændres, når formatet køres, med det formål at sammenligne basisværdier med resultaterne af formatets udførelse. Hvis du vil vide mere om denne funktion, skal du udføre følgende eksempel.

## <a name="example-configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a>Eksempel: Konfigurer grundlaget, så det hele tiden ignorerer ændringer i dele af ER-outputtet

Hvis du vil udføre trinnene i dette eksempel, skal du først fuldføre trinnene i eksemplet [Spore genererede rapportresultater og sammenligne dem med basisværdier](er-trace-reports-compare-baseline.md).

### <a name="modify-a-configured-er-format"></a>Rediger et konfigureret ER-format

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. Udvid **Model til at lære ER-grundlag** i træet.
3. Vælg **Model til at lære ER-brundlag\\Format til at lære ER-grundlag** i træet.
4. Vælg **Designer**.
5. Vælg **Output\\Dokument** i træet.
6. Vælg **Tilføj**.
7. Vælg **XML\\Attribut** i træet i rulledialogboksen.
8. Angiv **ProcessingDateTime** i feltet **Navn**.
9. Vælg **OK**.
10. Gå til fanen **Tilknytning**, og vælg **Output\\Dokument\\ProcessingDateTime** i træet.
11. Vælg **Rediger formel**.
12. Gå til feltet **Formel**, og angiv følgende udtryk: **DATETIMEFORMAT(NOW(), "O")**
13. Vælg **Gem**, og vælg derefter **Test**.
14. Vælg **Test** igen for at teste det konfigurerede udtryk igen.

    ![Siden Formeldesigner](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "Skærmbillede af siden Formeldesigner")

    > [!NOTE]
    > Under **Testresultat** kan du se, at det konfigurerede udtryk returnerer en anden værdi for dato/klokkeslæt, hver gang det kaldes.

15. Luk siden **Formeldesigner**, og vælg derefter **Gem**.

    ![Siden Formatdesigner](media/GER-BaselineSample-FormatMappingDesign2.PNG "Skærmbillede af siden Formatdesigner")

16. Luk siden **Formatdesigner**.

### <a name="remove-an-existing-baseline-rule"></a>Fjerne en eksisterende grundlagsregel

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. Vælg **Grundlag**.
3. På listen over grundlag skal du vælge det grundlag, der er konfigureret til formatet **Format til at lære ER-grundlag**.
4. I oversigtspanelet **Grundlag** skal du vælge **Slet** for at fjerne den grundlagsregel, du konfigurerede tidligere.

![Siden Grundlag for elektronisk rapporteringsformat](media/GER-BaselineSample-AddBaseline3.PNG "Skærmbillede af siden Grundlag for elektronisk rapporteringsformat")

### <a name="define-replacements-for-bindings-of-designed-er-format"></a>Definer erstatninger for bindinger, der er designet ER-format

1. Gå til siden **Konfigurationer**, og vælg **Vælg komponenter** i oversigtspanelet **Erstatninger**.
2. I træet til formatkomponenter skal du udvide **Output**, udvide **Output\\Dokument** og derefter markere afkrydsningsfeltet for **Output\\Dokument\\ProcessingDateTime**.

    ![Dialogboksen Vælg komponenter](media/GER-BaselineSample-SelectComponentForBindingReplacement.PNG "Skærmbillede af dialogboksen Vælg Komponenter")

3. Vælg **OK**.

![Siden Grundlag for elektronisk rapporteringsformat](media/GER-BaselineSample-AddBaseline4.PNG "Skærmbillede af siden Grundlag for elektronisk rapporteringsformat")

Den valgte ER-formatkomponent er føjet til listen over komponenter i oversigtspanelet **Erstatninger**. Når basis-ER-formatet køres i fejlfindingstilstand, vil formatets binding for hver komponent blive erstattet af den binding, der vises i kolonnen **Binding**. Hvis du vil ændre standardbindingen for en komponent, der vises i oversigtspanelet **Erstatninger**, skal du vælge **Rediger**.

### <a name="make-a-new-baseline-rule"></a>Opret en ny grundlagsregel

Følg trinnene i afsnittet "Eksempel: Automatiser indstillingen af regler for grundlag" tidligere i dette emne. En besked advarer dig om, at den udgående fil er blevet oprettet ved hjælp af grundlagsindstillinger, og at der er foretaget en tvungen erstatning af formatbindingerne.

![Besked på siden Konfigurationer](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "Skærmbillede af besked på siden Konfigurationer")

### <a name="suppress-warnings-about-the-replacement-of-format-bindings"></a>Undertryk advarsler om erstatning af formatbindinger

Hvis du angiver specifikke ER-parametre, kan du undertrykke beskeder, der advarer om erstatning af formatbindinger. Denne undertrykkelse kan være nyttig, når formatbindinger erstattes i en automatisk tilstand ved hjælp af Regression Suite Automation Tool. I dette tilfælde kan advarslen betragtes som en fejl i den test, der kører.

1. Gå til siden **Konfigurationer**, gå til handlingsruden, og vælg **Brugerparametre** på fanen **Konfigurationer**.
2. Angiv indstillingen **Undertryk grundlagsadvarsler** til **Ja**, og vælg derefter **OK**.

![Dialogboksen Brugerparametre](media/GER-BaselineSample-ERUserParameters1.png "Skærmbillede af dialogboksen Brugerparametre")

### <a name="review-the-generated-baseline-file"></a>Gennemse den genererede grundlagsfil.

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. Vælg **Grundlag**.
3. Vælg **Vedhæftede filer**.

    ![Siden Vedhæftede filer](media/GER-BaselineSample-AttachedBaselineFile.PNG "Skærmbillede af siden Vedhæftede filer")

    > [!NOTE]
    > Den genererede fil indeholder behandlingsdato- og klokkeslættetsteksten (**"#"**) fra den binding, der blev konfigureret i den tilføjede grundlagsregel, ikke fra formatets binding.

4. Luk siden **Vedhæftede filer**.

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a>Kør det designede ER-format, og gennemse logfilen for at analysere resultaterne

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. Udvid **Model til at lære ER-grundlag** i træet.
3. Vælg **Model til at lære ER-brundlag\\Format til at lære ER-grundlag** i træet.
4. Gå til oversigtspanelet **Versioner**, og vælg **Kør**.
5. Gå til feltet **Angiv id**, og skriv **1**.
6. Vælg **OK**.
7. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Fejlfindingslogs for konfigurationer**.

Udførelseslogfilen indeholder oplysninger om resultaterne af sammenligningen af den genererede fil med det konfigurerede grundlag. Logfilen angiver, at den genererede fil og grundlaet er ens, selvom det udførte format indeholder bindingen til at angive en konstant ændring af dato- og klokkeslætsværdien i den udgående fil.

> [!NOTE]
> Selvom den udgående fil er genereret ved hjælp af de grundlagsindstillinger, der gennemtvinger erstatningen af formatets bindinger, modtager du ingen advarsler om erstatningen.

## <a name="exchange-baseline-settings-between-environments"></a>Udskift indstillinger for grundlag mellem miljøer

### <a name="export-baseline-settings"></a>Eksport indstillinger for grundlag

Med de nye ER-funktioner kan du eksportere indstillinger for grundlag for det valgte ER-format fra det aktuelle miljø og gemme dem som XML-filer. 

Hvis du vil eksportere indstillinger for grundlag, skal du på siden **Grundlag for elektronisk rapporteringsformat** vælge **Eksporter**.

### <a name="import-baseline-settings"></a>Importer oprindelige indstillinger

Eksporterede indstillinger for grundlag kan importeres til et andet miljø. Miljøet skal først importeres som et ER-format. Du kan derefter importere grundlagsindstillingerne.

Hvis du vil importere grundlagsindstillinger fra en XML-fil, der er gemt lokalt, skal du på siden **Grundlag for elektronisk rapporteringsformat** vælge **Importer** og derefter **Gennemse** for at vælge XML-filen.

![Dialogboksen Import indstillinger for grundlag](media/GER-BaselineSample-ImportBaseline1.PNG "Skærmbillede af dialogboksen Import indstillinger for grundlag")

Hvis du vil importere grundlagsindstillinger fra en XML-fil, der er gemt på Microsoft SharePoint Server, baseret på de aktuelle indstillinger for dokumentstyring og den valgte dokumenttype, skal du vælge **Importer fra kilde** på siden **Grundlag for elektronisk rapporteringsformat**. Vælg derefter dokumenttypen, og XML-filen. Den krævede dokumenttype for at få adgang til SharePoint-mappen skal være konfigureret i forvejen.

![Dialogboksen Importer fra kilde](media/GER-BaselineSample-ImportBaseline2.PNG "Skærmbillede af dialogboksen Importer fra kilde")

> [!NOTE]
> Du kan bruge Arbejdsrutineoptager til at registrere de trin, der skal bruges til at vælge den ønskede dokument type og filnavnet i dialogboksen **Importer fra kilde**. På denne måde kan du beholde de nødvendige indstillinger for grundlag på SharePoint Server og derefter importere dem automatisk ved at afspille en opgaveregistrering, når du kører automatiske test ved hjælp af Regression Suite Automation Tool.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Spore genererede rapportresultater og sammenligne dem med basisværdier](er-trace-reports-compare-baseline.md)
- [Arbejdsrutineoptager](../user-interface/task-recorder.md)
