---
title: Spore genererede rapportresultater og sammenligne dem med basisværdier
description: Dette emne forklarer, hvordan du kan sammenligne resultaterne af genererede ER-rapporter (Electronic reporting) med grundlagsrapportværdier.
author: NickSelin
ms.date: 06/17/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: e4245f5951cc4891b378f2343a1563ced33bc937
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2021
ms.locfileid: "6345834"
---
# <a name="trace-generated-report-results-and-compare-them-with-baseline-values"></a>Spore genererede rapportresultater og sammenligne dem med basisværdier

[!include[banner](../includes/banner.md)]

Du kan spore resultaterne af ER-formater (Electronic reporting), der kan genere udgående elektroniske dokumenter. Når sporingsgenereringen er slået til (ved hjælp af ER-brugerparamenteren  **Kør i fejlfindingstilstand**), genereres en ny sporingspost i udførelseslogfilen i ER-formatet, hver gang der køres en ER-rapport. Følgende oplysninger gemmes i de enkelte spor, der genereres:

- Alle advarsler, der er oprettet af valideringsregler
- Alle fejl, der er oprettet af valideringsregler
- Alle genererede filer, der er gemt som vedhæftede filer, af sporingsposten

Du kan gemme individuelle basisprogramfiler til ethvert ER-format. Filer betragtes som basisfiler, når de beskriver de forventede resultater af rapporter, der køres. Hvis en grundlagsfil er tilgængelig for et ER-format, der køres, mens sporingsgenerering er slået til , lagrer sporingen ud over de detaljer, der blev nævnt tidligere, resultatet af sammenligningen af det genererede elektroniske dokument med grundlagsfilen. Med et enkelt klik kan du også få det genererede elektroniske dokument og dets basisfil i en enkelt zip-fil. Du kan derefter foretage detaljeret sammenligning ved at bruge et eksternt værktøjs om f.eks. WinDiff.

Du kan evaluere sporingen for at analysere, om de elektroniske dokumenter, der genereres, medtager det forventede indhold. Du kan foretage denne evaluering i et UAT-testmiljø til brugeraccept, når kodebasen er blevet ændret (f.eks. når du har overflyttet til en ny forekomst af programmet, installeret hotfix-pakker eller implementeret ændringer af koden). På denne måde kan du sikre dig, at vurderingen ikke påvirker udførelsen af ER-rapporter, der er i brug. For mange ER-rapporter kan evalueringen foretages i uovervåget tilstand.

Du kan få mere at vide om denne funktion ved at afspile opgaveguiderne **ER Generere rapporter og sammenligne resultater (del 1)** og **ER Generere rapporter og sammenligne resultater (del 2)**, der er en del af forretningsprocessen **7.5.4.3 Test it-ydelser og -løsninger (10679)** og kan downloades fra [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684). Disse opgaveguider gennemgår, hvordan ER-strukturen konfigureres til at bruge basisfiler for at evaluere genererede elektroniske dokumenter.

## <a name="example-trace-generated-report-results-and-compare-them-with-baseline-values"></a>Eksempel: Spor genererede rapportresultater, og sammenlign dem med basisværdier

Denne procedure forklarer, hvordan du konfigurerer ER-strukturen til at indsamle oplysninger om ER-formatudførelser og derefter evaluerer resultaterne af disse udførelser. Som del af denne evaluering sammenlignes genererede dokumenter med deres grundlagsfiler. I dette eksempel opretter du de krævede ER-konfigurationer for Litware, Inc., eksempelvirksomheden. Denne procedure er beregnet til brugere, der har fået tildelt rollen som systemadministrator eller elektronisk rapporteringsudvikler. Disse trin kan udføres ved hjælp af et hvilket som helst datasæt.

For at fuldføre trinnene i dette eksempel skal du først fuldføre trinnene i [Opret konfigurationsudbydere, og markér dem som aktive](tasks/er-configuration-provider-mark-it-active-2016-11.md).

1. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. Gå til sektionen **Konfigurationsudbydere** på siden **Lokaliseringskonfigurationer**, og bekræft, at konfigurationsudbyderen for eksempelfirmaet Litware, Inc. er angivet, og at den er markeret som **Aktiv**. Hvis du ikke ser denne konfigurationsudbyder, skal du følge trinnene i [Opret konfigurationsudbydere, og markér dem som aktive](tasks/er-configuration-provider-mark-it-active-2016-11.md).

### <a name="configure-document-management-parameters"></a>Konfigurere parametre til dokumentstyring

1. Gå til **Organisationsadministration** \> **Dokumentstyring** \> **Dokumenttyper**, og opret en ny dokumenttype til lagring af grundlagsfiler.
2. Skriv **Vedhæft fil** i feltet **Class**.
3. Skriv **Filer** i feltet **Group**.

![Siden Dokumenttyper.](media/GER-BaselineSample-SetupDocumentType.PNG "Skærmbillede af siden Dokumenttyper")

> [!NOTE]
> En ny dokumenttype, der har det samme navn, skal være konfigureret for hvert datasæt, hvor du planlægger at bruge ER-grundlagsfunktionen.

### <a name="configure-er-parameters-to-start-to-use-the-baseline-feature"></a>Konfigurer ER-parametre for at begynde at bruge grundlagsfunktionen

1. Gå til arbejdsområdet **Elektronisk rapportering**, og vælg **Parametre til elektronisk rapportering** i sektionen **Relaterede links**.

    ![Arbejdsområde til elektronisk rapportering.](media/GER-BaselineSample-ERWorkspace.PNG "Skærmbillede af arbejdsområdet Elektroniske rapportering")

2. Gå til fanen **Vedhæftede filer**, og angiv eller vælg den dokumenttype, du lige har oprettet, i feltet **Grundlag**.

    ![Vedhæftelsesfane på siden Elektroniske rapporteringsparametre.](media/GER-BaselineSample-ERParameters.PNG "Skærmbillede af Elektroniske rapporteringsparametre")

3. Vælg **Gem**, og luk derefter siden **Parametre til elektronisk rapportering**.

### <a name="add-a-new-er-model-configuration"></a>Tilføj en ny ER-modelkonfiguration

1. Gå til arbejdsområdet **Elektronisk rapporteringreporting**, og vælg feltet **Reporting configurations** i sektionen **Konfigurationer**.
2. Vælg **Opret konfiguration** i handlingsruden.
3. I feltet **Navn** i rulledialogboksen skal du angive **Model til at lære ER-grundlag**.
4. Vælg **Opret konfiguration** for at bekræfte oprettelse af en ny ER-datamodelpost.

![Dialogboks til rulleliste Opret konfiguration.](media/GER-BaselineSample-ModelAdd.PNG "Skærmbillede af dialogboksen til rullelisten Opret konfiguration")

### <a name="design-a-data-model"></a>Design en datamodel

1. Gå til siden **Konfigurationer**, og vælg **Designer** i handlingsruden.
2. Vælg **Ny**.
3. Gå til rulledialogboksen, og angiv **Rod** i feltet **Navn**.
4. Vælg **Tilføj**.
5. Vælg **Rodreference**.
6. Vælg **OK**, og vælg derefter **Gem**.
7. Luk siden **Modeldesigner**.
8. Vælg **Skift status**.
9. Vælg **Fuldfør**, og vælg derefter **OK**.

![Siden Konfigurationer.](media/GER-BaselineSample-ModelComplete.PNG "Skærmbillede af siden Konfigurationer")

### <a name="add-a-new-er-format-configuration"></a>Tilføje en ny ER-formatkonfiguration

1. Gå til siden **Konfigurationer**, og vælg **Opret konfiguration** i handlingsruden.
2. Gå til rulledialogboksen, og vælg **Format baseret på datamodellen Model til at læse ER-grundlag** i feltgruppen **Ny**.
3. Gå til feltet **Navn**, og angiv **Format til at lære ER-grundlag**.
4. Vælg **Opret konfiguration** for at bekræfte oprettelsen af en ny ER-formatpost.

![Dialogboks til rulleliste Opret konfiguration.](media/GER-BaselineSample-FormatAdd.PNG "Skærmbillede af dialogboksen til rullelisten Opret konfiguration")

### <a name="design-a-format"></a>Design et format

I dette eksempel vil du oprette et enkelt ER-format for at generere XML-dokumenter.

1. Gå til siden **Konfigurationer**, og vælg **Designer** i handlingsruden.
2. Vælg **Tilføj rod**.
2. Følg disse trin i rulledialogboksen:

    1. Vælg **Fælles\\Filer** i træet.
    2. I feltet **Navn** skal du skrive **Output**.
    3. Vælg **OK**.

3. Vælg **Tilføj**.
4. Følg disse trin i rulledialogboksen:

    1. Vælg **XML\\Element** i træet.
    2. Angiv **Dokument** i feltet **Navn**.
    3. Vælg **OK**.

5. Vælg **Output\\Dokument** i træet.
6. Vælg **Tilføj**.
7. Følg disse trin i rulledialogboksen:

    1. Vælg **XML\\Attribut** i træet.
    2. Angiv **Id** i feltet **Navn**.
    3. Vælg **OK**.

    ![Siden Formatdesigner.](media/GER-BaselineSample-FormatLayoutDesign.PNG "Skærmbillede af siden Formatdesigner")

8. Vælg **Slet** på fanen **Tilknytning**.
9. Vælg **Tilføj rod**.
10. Gå til rulledialogboksen, og vælg **Generelt\\Brugerinputparameter** i træet, og følg derefter disse trin:

    1. Angiv **Id** i feltet **Navn**.
    2. Angiv **Angiv id** i feltet **Etiket**.
    3. Vælg **OK**.

11. Vælg **Output\\Dokument\\Id** i træet.
12. Vælg **Bind**, og vælg derefter **Gem**.

![Siden Formatdesigner.](media/GER-BaselineSample-FormatMappingDesign.PNG "Skærmbillede af siden Formatdesigner")

Baseret på den designede struktur genererer det konfigurerede format en XML-fil. Denne XML indeholder det **rod**-element, der har **Id**-attributten, der er indstillet til den værdi, som brugeren angiver i ER-kørselsdialogboksen.

### <a name="generate-a-new-baseline-file-for-a-designed-er-format"></a>Opret en ny grundlagsfil for et designet ER-format

1. Gå til siden **Konfigurationer**, og vælg **Kør** i oversigtspanelet **Versioner**.
2. Gå til feltet **Angiv id**, og angiv **1**.
3. Vælg **OK**.

    ![Dialogboksen Parametre til elektronisk rapportering.](media/GER-BaselineSample-FormatRunToMakeBaselineFile1.PNG "Skærmbillede af dialogboksen Elektroniske rapporteringsparametre")

4. Gem en lokal kopi af filen **out.Admin.xml**, der er genereret, så du kan bruge den senere som grundlag for dette ER-format.

    ![Besked om den genererede fil på siden Konfigurationer.](media/GER-BaselineSample-FormatRunToMakeBaselineFile2.PNG "Skærmbillede af beskeden om den genererede fil på siden Konfigurationer")

### <a name="configure-er-parameters-to-use-the-baseline-feature"></a>Konfigur ER-parametre til at bruge grundlagsfunktionen

1. Gå til siden **Konfigurationer**, gå til handlingsruden, og vælg **Brugerparametre** på fanen **Konfigurationer**.
2. Angv indstillingen **Kør i fejlfindingstilstand** til **Ja**.
3. Vælg **OK**.

![Dialogboksen Brugerparametre.](media/GER-BaselineSample-ERUserParameters.PNG "Skærmbillede af dialogboksen Brugerparametre")

### <a name="add-a-new-baseline-for-designed-er-format"></a>Tilføj et nyt grundlag for designet ER-format

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. Gå til handlingsruden, og vælg **Grundlag**.

    ![Knap til Basislinjer på siden Konfigurationer.](media/GER-BaselineSample-OpenBaselinePage.PNG "Skærmbillede af knappen Basislinjer på siden Konfigurationer")

3. Gå til handlingsruden, og vælg **Ny**.
4. Vælg det ER-format **Format til at lære ER-grundlag**, du designede tidligere.
5. Vælg **Gem**.

![Siden for Basislinjer for elektronisk rapporteringsformat.](media/GER-BaselineSample-AddBaseline.PNG "Skærmbillede af siden Format for basislinjer i elektronisk rapportering")

Grundlaget føjes til til formatet **Format til at lære ER-grundlag**.

### <a name="configure-a-baseline-rule-for-the-added-baseline"></a>Konfigurer en grundlagsregel for det tilføjede grundlag

1. Gå til siden **Grundlag for elektronisk rapporteringsformat**, gå til handlingsruden, og vælg knappen **Vedhæftede filer** (papirklipsymbolet).
2. Gå til handlingsruden, og vælg **Ny** \> **Filer**. I ER-parametrene skal **Filer**-dokumenttypen være blevet valgt tidligere som den dokumenttype, der skal bruges til at lagre grundlagsfiler.
3. Vælg **Gennemse**, og vælg filen **out.Admin.xml**, der blev genereret, da du kørte det konfigurerede ER-format tidligere.

    ![Side med vedhæftelser.](media/GER-BaselineSample-UploadBaselineFile.PNG "Skærmbillede af siden Vedhæftelser")

4. Luk siden **Vedhæftede filer**.
5. Gå til oversigtspanelet **Basiværdier**, og vælg **Ny**.
6. Angiv **Grundlag1** i feltet **Navn**.
7. Angiv **Output** i feltet **Filkomponentnavn**. Denne værdi angiver, at det konfigurerede grundlag sammenlignes med en fil, der er genereret ved hjælp af formatelementet **Output**.
8. Gå til feltet **Filnavnsmaske**, og angiv **\*.xml**.

    > [!NOTE]
    > Du kan definere filnavnmasken. Når filnavnmasken er defineret, bruges grundlagsposten kun til at evaluere det genererede output, når navnet på outputfilen, der genereres, opfylder betingelserne for den maske.

9. Hvis det konfigurerede grundlag kun skal bruges når ER-formatet **Format til at lære ER-grundlag** køres af bruger, der er logget ind for specifikke firmaer, skal du vælge disse firmaer i feltet **Firmaer**.
10. I feltet **Grundlag** skal du angive eller vælge den vedhæftede fil **out.Admin**.
11. Vælg **Gem**.

![Siden for Basislinjer for elektronisk rapporteringsformat.](media/GER-BaselineSample-SetupBaselineLine.PNG "Skærmbillede af siden Format for basislinjer i elektronisk rapportering")

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a>Kør det designede ER-format, og gennemse logfilen for at analysere resultaterne

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. Gå til træet, udvid **Model til at lære ER-grundlag**, og vælg derefter **Model til at lære ER-grundlag\\Format til at lære ER-grundlag**.
3. Gå til oversigtspanelet **Versioner**, og vælg **Kør**.
4. Gå til feltet **Angiv id**, og angiv **1**.
5. Vælg **OK**.
6. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Fejlfindingslogs for konfigurationer**.

    ![Siden Kørselslog for elektronisk rapportering.](media/GER-BaselineSample-ReviewBaselineComparison1.PNG "Skærmbillede af siden Kørselslog for elektronisk rapportering")

    > [!NOTE]
    > Udførelseslogfilen indeholder oplysninger om resultaterne af sammenligningen af den genererede fil med det konfigurerede grundlag. I dette eksempel angiver logfilen, at den genererede fil og grundlaget er ens.

7. Vælg **Slet alt**.

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a>Kør det designede ER-format, og gennemse logfilen for at analysere resultaterne

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. Gå til træet, udvid **Model til at lære ER-grundlag**, og vælg derefter **Model til at lære ER-grundlag\\Format til at lære ER-grundlag**.
3. Gå til oversigtspanelet **Versioner**, og vælg **Kør**.
4. Gå til feltet **Angiv id**, og angiv **2**.
5. Vælg **OK**.
6. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Fejlfindingslogs for konfigurationer**.

    ![Siden Kørselslog for elektronisk rapportering.](media/GER-BaselineSample-ReviewBaselineComparison2.PNG "Skærmbillede af siden Kørselslog for elektronisk rapportering")

    > [!NOTE]
    > Udførelseslogfilen indeholder oplysninger om resultaterne af sammenligningen af den genererede fil med det konfigurerede grundlag. I dette eksempel angiver logfilen, at den genererede fil og grundlaget er forskellige.

7. Vælg **Sammenlign**.

> [!NOTE]
> Den genererede fil og grundlagsfilen fås som en zip-fil. Du kan bruge eksterne sammenligningsværktøjer såsom WinDiff til at sammenligne filerne og gennemgå forskellene.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Konfigurer den Elektroniske rapporteringsstruktur (ER)](electronic-reporting-er-configure-parameters.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]