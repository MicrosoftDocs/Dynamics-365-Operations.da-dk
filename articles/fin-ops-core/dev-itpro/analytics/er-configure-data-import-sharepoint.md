---
title: Konfigurere dataimport fra SharePoint
description: I dette emne beskrives, hvordan du importerer data fra Microsoft SharePoint.
author: NickSelin
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 1f7754a3e69238ab1760b3f7eb8f5e2c792b451b
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680896"
---
# <a name="configure-data-import-from-sharepoint"></a>Konfigurere dataimport fra SharePoint

[!include[banner](../includes/banner.md)]

Hvis du vil importere data fra en indgående fil ved hjælp af strukturen til elektronisk rapportering (ER), skal du konfigurere et ER-format, der understøtter importen og derefter køre en modeltilknytning af typen **Til destination**, der bruger dette format som datakilde. Du importerer data ved at navigere til den fil, du vil importere. Den indgående fil kan vælges manuelt af brugeren. Denne proces kan konfigureres som automatiseret med den nye ER-funktionalitet, der understøtter import af data fra Microsoft SharePoint. Du kan bruge ER-konfigurationer til at udføre dataimport fra filer, der er gemt i Microsoft SharePoint-mapper. I dette emne beskrives, hvordan du udfører importen fra SharePoint. I eksemplerne bruges kreditorposteringer som forretningsdata.

## <a name="prerequisites"></a>Forudsætninger
Før du kan følge eksemplerne i dette emne, skal du have følgende adgang:

- Få adgang til en af følgende roller:

    - Udvikler til elektronisk rapportering
    - Funktionel konsulent i elektronisk rapportering
    - Systemadministrator

- Adgang til den forekomst af Microsoft SharePoint Server, der er konfigureret til brug sammen med programmet.
- ER-format og -modelkonfigurationer til 1099-betalinger.

### <a name="create-required-er-configurations"></a>Oprette de nødvendige ER-konfigurationer
Afspil opgaveguiderne **ER Import af data fra en Microsoft Excel-fil**, der er en del af forretningsprocessen **7.5.4.3 Anskaffe/udarbejde IT-tjeneste/løsningskomponenter (10677)**. Disse opgaveguider gennemgår processen med at designe og bruge ER-konfigurationer til at importere kreditorposteringer interaktivt fra Microsoft Excel-filer. Du kan finde flere oplysninger i [Analysere indgående dokumenter i Excel-format](parse-incoming-documents-excel.md). Når du har fuldført opgavevejledningerne, har du følgende konfiguration.

#### <a name="er-configurations"></a>ER-konfigurationer

- ER-modelkonfigurationen **1099-betalingsmodel**
- ER-formatkonfigurationen **Format til import af kreditorposteringer fra Excel**

![ER-konfigurationer til import af data fra SharePoint](./media/GERImportFromSharePoint-01-Configurations.PNG)

#### <a name="sample-of-the-incoming-file-for-data-import"></a>Eksempel på den indgående fil til import af data

- Excel-filen **1099import-data.xlsx** med kreditorposteringer, der skal importeres.

![Excel-eksempelfil til import fra SharePoint](./media/GERImportFromSharePoint-02-Excel.PNG)
    
> [!NOTE]
> Formatet til import af kreditorposteringer er valgt som standardmodeltilknytningen. Hvis du derfor kører en modeltilknytning af **1099-betalingsmodellen**, og modeltilknytningen er af typen **Til destination**, kører modeltilknytningen dette format ved import af data fra eksterne filer. Derefter bruges disse data til at opdatere programtabeller.

## <a name="configure-access-to-sharepoint-for-file-storage"></a>Konfigurere adgang til SharePoint for at gemme filer
Du kan gemme elektroniske rapportfiler på en SharePoint-placering ved at konfigurere adgang til den SharePoint Server-forekomst, der skal bruges af den aktuelle virksomhed. I dette eksempel er firmaet USMF. Du kan finde flere oplysninger i [Konfigurere SharePoint-lager](../../fin-ops/organization-administration/configure-document-management.md#configure-sharepoint-storage).

1. Udfør trinnene i [Konfigurere SharePoint-lager](../../fin-ops/organization-administration/configure-document-management.md#configure-sharepoint-storage).
2. Åbn det konfigurerede SharePoint-websted.
3. Opret følgende mapper, hvor indgående elektroniske rapporteringsfiler kan gemmes:

     - Filimportkilde (hoved) (eksempel vises på skærmbilledet nedenfor)
     - Filimportkilde (alternativ)

    ![Filimportkilde (hoved)](./media/GERImportFromSharePoint-04-SharePointFolder1.png)

4. (Valgfrit) Opret følgende mapper, hvor filerne kan gemmes efter import. 

    - Filarkivmappe – Denne mappe bruges til filer, der er importeret.
    - Mappe til filer med advarsler - Denne mappe er til filer, der er importeret med en advarsel.
    - Mappe til fejlslagne filer – Denne mappe bruges til filer, der ikke blev importeret.

4. Gå til **Virksomhedsadministration > Dokumentstyring > Dokumenttyper**.
5. Opret følgende dokumenttyper, der skal bruges til at få adgang til de SharePoint-mapper, du har oprettet. Yderligere oplysninger finder du i [Konfigurere dokumenttyper](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types).

|Dokumenttype       | Multi              | Placering      | SharePoint-mappe      |
|--------------------|--------------------|---------------|------------------------|
|SP-hoved             |Fil                |SharePoint     |Filimportkilde (hoved)|
|SP-alternativ             |Fil                |SharePoint     |Filimportkilde (alternativ)|
|SP-arkiv             |Fil                |SharePoint     |Filarkivmappe|
|SP-advarsel             |Fil                |SharePoint     |Mappe til filer med advarsler|
|SP-fejl             |Fil                |SharePoint     |Mappe til fejlslagne filer|

![SharePoint-indstilling – ny dokumenttype](./media/GERImportFromSharePoint-06-SharePointDocumentTypesSetup.png)

## <a name="configure-er-sources-for-the-er-format"></a>Konfigurere ER-kilder for ER-formatet
1. Klik på **Virksomhedsadministration** \> **Elektronisk rapportering** \> **Kilde til elektronisk rapportering**.
2. På siden **Kilde til elektronisk rapportering** skal du konfigurere kildefilerne til import af data ved hjælp af det konfigurerede ER-format.
3. Definer en filnavnsmaske, så kun filer med filtypenavnet .xlsx importeres. Filnavnsmasken er valgfri og bruges kun, når den er defineret. Du kan kun definere én maske for hvert ER-format.
4. Skift **Sortér filer før import** til **Sortér ikke**, hvis der er mange filer til import, og importrækkefølgen ikke er vigtig
5. Vælg alle de SharePoint-mapper, du oprettede tidligere.

    [![Indstilling for ER-filkilde](./media/GERImportFromSharePoint-07-FormatSourceSetup.PNG)](./media/GERImportFromSharePoint-07-FormatSourceSetup.PNG)

> [!NOTE]
> - ER *kilde* defineres individuelt for hvert firma i programmet. Derimod deles ER *konfigurationer* på tværs af firmaer.
> - Når du sletter en ER-kildeindstilling for et ER-format, slettes også alle tilknyttede filtilstande (se nedenfor) efter bekræftelse.

## <a name="review-the-files-states-for-the-er-format"></a>Gennemse filtilstande for ER-formatet
1. På siden **Kilde til elektronisk rapportering** skal du vælge **Filtilstande for kilderne** for at gennemse indholdet af de konfigurerede filkilder for det aktuelle ER-format.
2. I sektionen **Filer** skal du gennemse listen over filer. Denne liste viser følgende:

    - Kildefiler, der er relevante, baseret på filnavnsmasken (hvis der er defineret en maske), og som er klar til dataimport. For disse filer er sektionen **Kildelogfiler for importformatet** tom.
    - Tidligere importerede filer. For hver af disse filer i sektionen **Kildelogfiler for importformatet** kan du gennemse oversigten over import af filen.

Du kan også åbne siden **Filtilstande for kilderne** ved at vælge **Virksomhedsadministration** \> **Elektronisk rapportering** \> **Filtilstande for kilderne**. I så fald indeholder siden oplysninger om filkilder for alle ER-formater, som filkilder er konfigureret for i det firma, du aktuelt er logget på.

## <a name="import-data-from-excel-files-that-are-in-a-sharepoint-folder"></a>Importere data fra Excel-filer, der findes i en SharePoint-mappe
1. I SharePoint skal du overføre Microsoft Excel-filen **1099import-data.xlsx**, der indeholder kreditorposter, til den **Filimportkilde (hoved)** SharePoint-mappe, du oprettede tidligere.

    [![SharePoint-indhold – Microsoft Excel-fil til import](./media/GERImportFromSharePoint-08-UploadFile.png)](./media/GERImportFromSharePoint-08-UploadFile.png)

2. På siden **Filtilstande for kilderne** skal du vælge **Opdater** for at opdatere siden. Den Excel-fil, der blev overført til SharePoint, blev vist på denne side med status **Klar**. Følgende statusser understøttes i øjeblikket:

    - **Klar** – Tildeles automatisk til hver ny fil i en SharePoint-mappe. Denne status betyder, at filen er klar til import.
    - **Importerer** – Tildeles automatisk af en ER-rapport, når filen låses af importen for at forhindre, at den bruges af andre processer (hvis mange af dem kører samtidigt).
    - **Importeret** – Tildeles automatisk af en ER-rapport, når filimporten er fuldført. Denne status betyder, at den importerede fil er blevet slettet fra den konfigurerede filkilde (SharePoint-mappe).
    - **Mislykkedes** – Tildeles automatisk af en ER-rapport, når filimporten blev fuldført med fejl eller undtagelser.
    - **På hold** – Tildeles manuelt af brugeren på denne side. Denne status betyder, at filen ikke importeres på nuværende tidspunkt. Denne status kan bruges til at udskyde importen af visse filer.

    [![Opdateret ER-filtilstandsside for de valgte kilder](./media/GERImportFromSharePoint-09-FileStatesForm.png)](./media/GERImportFromSharePoint-09-FileStatesForm.png)

## <a name="import-data-from-sharepoint-files"></a>Importere data fra SharePoint-filer
1. Åbn ER-konfigurationstræet, vælg **1099-betalingsmodel**, og udvid listen over ER-modelkomponenter.
2. Vælg navnet på modeltilknytningen for at åbne listen over modeltilknytninger for den valgte ER-modelkonfiguration.

    [![Siden Konfiguration](./media/GERImportFromSharePoint-10-SelectModelMapping.PNG)](./media/GERImportFromSharePoint-10-SelectModelMapping.PNG)

3. Vælg **Kør** for at køre den valgte modeltilknytning. Da du har konfigureret filkilder for ER-formatet, kan du ændre indstillingen **Filkilde**, hvis der er brug for det. Hvis du lader denne indstilling være uændret, importeres .xslx-filerne fra de konfigurerede kilder (SharePoint-mapperne i dette eksempel).

    I dette eksempel skal du kun importere én fil. Hvis der er flere filer, vælges de til import i samme rækkefølge, som de blev tilføjet i SharePoint-mappen. Hver kørsel af et ER-format importerer en enkelt valgt fil.

    [![Importere fra SharePoint og køre ER-modeltilknytning](./media/GERImportFromSharePoint-11-RunModelMapping.PNG)](./media/GERImportFromSharePoint-11-RunModelMapping.PNG)

4. Modeltilknytningen kan køre [automatisk](#limitations) i batchtilstand. I så fald importeres en enkelt fil fra de konfigurerede filkilder, hver gang en batch kører dette ER-format.

    Når en fil er importeret fra SharePoint-mappen, slettes den fra den pågældende mappe og flyttes til mappen med importerede filer eller til mappen til importerede filer med advarsler. Ellers flyttes den til mappen for fejlslagne filer eller forbliver i denne mappe, hvis mappen med fejlslagne filer ikke er konfigureret. 

5. Angiv bilags-id'et, f.eks. **V-00001**, og vælg derefter **OK**.

    [![Køre ER-modeltilknytning](./media/GERImportFromSharePoint-12-ModelMappingRunFinished.PNG)](./media/GERImportFromSharePoint-12-ModelMappingRunFinished.PNG)

6. På siden **Filtilstande for kilderne** skal du vælge **Opdater** for at opdatere siden.

    [![ER-filtilstande for den valgte kildeside](./media/GERImportFromSharePoint-13-FileStatesForm.PNG)](./media/GERImportFromSharePoint-13-FileStatesForm.PNG)

7. I sektionen **Filer** skal du gennemse listen over filer. Sektionen **Kildelogfiler for importformatet** indeholder en oversigt over Excel-filimporten. Da denne fil blev importeret korrekt, er den markeret som **Slettet** i SharePoint-mappen.
8. Gennemse SharePoint-mappen **Filimportkilde (hoved)**. Excel-filer, der blev importeret, er blevet slettet fra denne mappe.
9. Vælg **Kreditor** \> **Periodiske opgaver** \> **1099-skat** \> **Kreditorudligning for 1099**.
10. I felterne **Fra dato** og **Til dato** skal du angive relevante værdier. Vælg derefter **Manuelle 1099-transaktioner**.

    De kreditorposteringer, der blev importeret fra Excel-filerne i SharePoint for bilag **V-00001**, vises på siden.

    [![Side for 1099-kreditorposteringer](./media/GERImportFromSharePoint-14-ImportedTransactions.PNG)](./media/GERImportFromSharePoint-14-ImportedTransactions.PNG)

## <a name="prepare-an-excel-file-for-import"></a>Forberede en Excel-fil til import
1. Åbn den Excel-fil, du tidligere brugte. I række 3, kolonne 1 skal du tilføje en kreditorkode, der ikke findes i programmet. Føj yderligere falske kreditoroplysninger til rækken.

    [![Microsoft Excel-eksempelfil til import fra SharePoint](./media/GERImportFromSharePoint-15-Excel.PNG)](./media/GERImportFromSharePoint-15-Excel.PNG)

2. Overfør den opdaterede Excel-fil, der indeholder kreditorposteringer til SharePoint-mappen **Filimportkilde (hoved)**.
3. Åbn ER-konfigurationstræet, vælg **1099-betalingsmodel**, og udvid listen over ER-modelkomponenter.
4. Vælg navnet på modeltilknytningen for at opdatere modeltilknytningen, så den forkerte kreditorkode betragtes som en fejl under dataimporten.
5. Vælg **Designer**.
6. Under fanen **Valideringer** skal du ændre efter-valideringshandlingen for den valideringsregel, der blev konfigureret, for at vurdere, om den kreditorkonto, der importeres, findes i programmet. Opdater værdien i feltet **Efter-valideringshandling** for at **Stop udførelse**, gemme ændringerne og lukke siden.

    [![Side for ER-modeltilknytningsdesigner](./media/GERImportFromSharePoint-16-UpdateModelMapping.PNG)](./media/GERImportFromSharePoint-16-UpdateModelMapping.PNG)

7. Gem ændringerne, og luk ER-modeltilknytningsdesigneren.
8. Vælg **Kør** for at køre den ændrede ER-modeltilknytning.
9. Angiv bilags-id'et, f.eks. **V-00002**, og vælg derefter **OK**.

    Infologgen indeholder en besked om, at der er en fil i SharePoint-mappen, der indeholder en forkert kreditorkonto, som ikke kan importeres.

    [![Fuldført kørsel af ER-modeltilknytning](./media/GERImportFromSharePoint-17-ModelMappingRunFinished.PNG)](./media/GERImportFromSharePoint-17-ModelMappingRunFinished.PNG)

10. På siden **Filtilstande for kilderne** skal du vælge **Opdater** og derefter i sektionen **Filer** gennemgå listen over filer.

    [![ER-filtilstandsside for de valgte kilder](./media/GERImportFromSharePoint-18-FileStatesForm.PNG)](./media/GERImportFromSharePoint-18-FileStatesForm.PNG)

   Sektionen **Kildelogfiler for importformatet** angiver, at importen mislykkedes, og at filen er i SharePoint-mappen til fejlslagne filer (afkrydsningsfeltet **Er slettet** er ikke markeret). Hvis du reparerer denne fil på SharePoint ved at tilføje den korrekte kreditorkode og derefter flytter den til SharePoint-mappen Filimportkilde (hoved), kan du importere filen igen.

11. Vælg **Kreditor** \> **Periodiske opgaver** \> **1099-skat** \> **Kreditorudligning for 1099**, angiv de relevante værdier i **Fra dato** og **Til dato**-felterne, og vælg derefter **Manuelle 1099-transaktioner**.

    Kun posteringer for bilag V-00001 er tilgængelige. Ingen posteringer for bilag V-00002 er tilgængelige, selvom fejlen for den sidste importerede transaktion blev fundet i Excel-filen.

## <a name=""></a><a name="limitations">Begrænsninger</a>

ER-strukturen giver ikke mulighed for at starte et nyt batchjob, der udfører en modeltilknytning i automatisk tilstand for dataimport. Hvis du vil gøre det, skal du udvikle ny logik, så den konfigurerede ER-modeltilknytning kan kaldes fra brugergrænsefladen i programmet for at importere data fra indgående filer. Dette kræver derfor udviklingsarbejde. 

Du kan få mere om det relevante-API i afsnittet [Kode til kørsel af en formattilknytning til dataimport](er-apis-app73.md#code-to-run-a-format-mapping-for-data-import) i emnet [Ændringer af API til ER-struktur til Application Update 7.3](er-apis-app73.md).

Gennemse koden i `BankImport_RU`-klassen for `Application Suite`-modellen for at se, hvordan din brugerdefinerede logik kan implementeres. Denne klasse udvider `RunBaseBatch`-klassen. Du skal især gennemse `runER()`-metoden, hvor `ERIModelMappingDestinationRun`-objektet oprettes som kørselsfunktion for en ER-modeltilknytning.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over elektronisk rapportering](general-electronic-reporting.md)

[Ændringer af API til ER-struktur for Application Update 7.3](er-apis-app73.md)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]