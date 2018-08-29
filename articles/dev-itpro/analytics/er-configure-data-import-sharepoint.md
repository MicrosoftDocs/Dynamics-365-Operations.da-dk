---
title: Konfigurere import af data fra SharePoint
description: I dette emne beskrives, hvordan du importerer data fra Microsoft SharePoint.
author: NickSelin
manager: AnnBe
ms.date: 05/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: 2fc887668171175d436b9eb281a35c1c9d089591
ms.openlocfilehash: 4285db9c71208bce45d64933e692a25ef3f46b26
ms.contentlocale: da-dk
ms.lasthandoff: 08/08/2018

---
# <a name="configure-data-import-from-sharepoint"></a>Konfigurere import af data fra SharePoint

[!include[banner](../includes/banner.md)]

Hvis du vil importere data fra en indgående fil ved hjælp af strukturen til elektronisk rapportering (ER), skal du konfigurere et ER-format, der understøtter importen og derefter køre en modeltilknytning af typen **Til destination**, der bruger dette format som datakilde. Du importerer data ved at navigere til den fil, du vil importere. Den indgående fil kan vælges manuelt af brugeren. Denne proces kan konfigureres som automatiseret med den nye ER-funktionalitet, der understøtter import af data fra Microsoft SharePoint. Du kan bruge ER-konfigurationer til at udføre dataimport fra filer, der er gemt i Microsoft SharePoint-mapper. I dette emne beskrives, hvordan du udfører importen fra SharePoint til Microsoft Dynamics 365 for Finance and Operations. I eksemplerne bruges kreditorposteringer som forretningsdata.

## <a name="prerequisites"></a>Forudsætninger
Før du kan følge eksemplerne i dette emne, skal du have følgende adgang:

- Adgang til Finance and Operations for en af følgende roller:

    - Udvikler til elektronisk rapportering
    - Funktionel konsulent i elektronisk rapportering
    - Systemadministrator

- Adgang til den forekomst af Microsoft SharePoint Server, der er konfigureret til brug sammen med Finance and Operations
- ER-format og -modelkonfigurationer til 1099-betalinger

### <a name="create-required-er-configurations"></a>Oprette de nødvendige ER-konfigurationer
Afspil opgaveguiderne **ER Import af data fra en Microsoft Excel-fil**, der er en del af forretningsprocessen **7.5.4.3 Anskaffe/udarbejde IT-tjeneste/løsningskomponenter (10677)**. Disse opgaveguider gennemgår processen med at designe og bruge ER-konfigurationer til at importere kreditorposteringer interaktivt fra eksterne Microsoft Excel-filer. Du kan finde flere oplysninger i [Analysere indgående dokumenter i Microsoft Excel](parse-incoming-documents-excel.md). Til slut har du:

- ER-konfigurationer:

    - ER-modelkonfigurationen **1099-betalingsmodel**
    - ER-formatkonfigurationen **Format til import af kreditorposteringer fra Excel**

[![ER-konfigurationer til import af data fra SharePoint](./media/GERImportFromSharePoint-01-Configurations.PNG)](./media/GERImportFromSharePoint-01-Configurations.PNG)

- Eksempel på den indgående fil til import af data:

    - Excel-filen **1099import-data.xlsx** med kreditorposteringer, der skal importeres til Finance and Operations

[![Microsoft Excel-eksempelfil til import fra SharePoint](./media/GERImportFromSharePoint-02-Excel.PNG)](./media/GERImportFromSharePoint-02-Excel.PNG)

> [!NOTE]
> Formatet til import af kreditorposteringer er valgt som standardmodeltilknytningen. Hvis du derfor kører en modeltilknytning af **1099-betalingsmodellen**, og modeltilknytningen er af typen **Til destination**, kører modeltilknytningen dette format ved import af data fra eksterne filer. Derefter bruges disse data til at opdatere programtabeller.

## <a name="configure-document-management-parameters"></a>Konfigurere dokumentstyringsparametre
1. På siden **Dokumentstyringsparametre** skal du konfigurere adgang til den forekomst af SharePoint-server, der skal bruges af den virksomhed, som du aktuelt er logget på. I dette eksempel er firmaet USMF.
2. Test forbindelsen til forekomsten af SharePoint Server for at sikre, at du har adgangstilladelse.

[![Indstilling for dokumentstyring – SharePoint Server](./media/GERImportFromSharePoint-03-SharePointSetup.png)](./media/GERImportFromSharePoint-03-SharePointSetup.png)

3. Åbn det konfigurerede SharePoint-websted, og opret følgende mapper, hvor indgående filer kan gemmes:

    - Filimportkilde (hoved)
    - Filimportkilde (alternativ)

[![Indstilling for dokumentstyring – SharePoint Server](./media/GERImportFromSharePoint-04-SharePointFolder1.png)](./media/GERImportFromSharePoint-04-SharePointFolder1.png)

[![Indstilling for dokumentstyring – SharePoint Server](./media/GERImportFromSharePoint-05-SharePointFolder2.png)](./media/GERImportFromSharePoint-05-SharePointFolder2.png)

4. I Finance and Operations skal du på siden **Dokumenttyper** oprette følgende dokumenttyper, der skal bruges til at få adgang til de SharePoint-mapper, du netop har oprettet:

    - SP-hoved
    - SP-alternativ

5. For oprettede dokumenttyper skal du i feltet **Gruppe** angive **Fil** og i feltet **Placering** skal du angive **SharePoint**. Indtast derefter adressen på SharePoint-mappen:

    - For **SP-hoved**-dokumenttypen: Filimportkilde (hoved)
    - For **SP-alternativ**-dokumenttypen: Filimportkilde (alternativ)

[![SharePoint-indstilling – ny dokumenttype](./media/GERImportFromSharePoint-06-SharePointDocumentTypesSetup.png)](./media/GERImportFromSharePoint-06-SharePointDocumentTypesSetup.png)

## <a name="configure-er-sources-for-the-er-format"></a>Konfigurere ER-kilder for ER-formatet
1. Klik på **Virksomhedsadministration** > **Elektronisk rapportering** > **Kilde til elektronisk rapportering**.
2. På siden **Kilde til elektronisk rapportering** skal du konfigurere kildefilerne til import af data ved hjælp af det konfigurerede ER-format.
3. Definer en filnavnsmaske, så kun filer med filtypenavnet .xlsx importeres. Filnavnsmasken er valgfri og bruges kun, når den er defineret. Du kan kun definere én maske for hvert ER-format.
4. Vælg begge de SharePoint-mapper, du oprettede tidligere.

[![Indstilling for ER-filkilde](./media/GERImportFromSharePoint-07-FormatSourceSetup.PNG)](./media/GERImportFromSharePoint-07-FormatSourceSetup.PNG)

> [!NOTE]
>ER *kilde* defineres individuelt for hvert firma i programmet. Derimod deles ER *konfigurationer* på tværs af firmaer.

> [!NOTE]
> Når du sletter en ER-kildeindstilling for et ER-format, slettes også alle tilknyttede filtilstande (se nedenfor).

## <a name="review-the-files-states-for-the-er-format"></a>Gennemse filtilstande for ER-formatet
1. På siden **Kilde til elektronisk rapportering** skal du vælge **Filtilstande for kilderne** for at gennemse indholdet af de konfigurerede filkilder for det aktuelle ER-format.
2. I sektionen **Filer** skal du gennemse listen over filer. Denne liste viser følgende:

    - Kildefiler, der er relevante, baseret på filnavnsmasken (hvis der er defineret en maske), og som er klar til dataimport. For disse filer er sektionen **Kildelogfiler for importformatet** tom.
    - Tidligere importerede filer. For hver af disse filer i sektionen ***Kildelogfiler for importformatet** kan du gennemse oversigten over import af filen.

Du kan også åbne siden **Filtilstande for kilderne** ved at vælge **Virksomhedsadministration** \> **Elektronisk rapportering** \> **Filtilstande for kilderne**. I så fald indeholder siden oplysninger om filkilder for alle ER-formater, som filkilder er konfigureret for i det firma, du aktuelt er logget på.

## <a name="import-data-from-excel-files-that-are-in-a-sharepoint-folder"></a>Importere data fra Excel-filer, der findes i en SharePoint-mappe
1. I SharePoint skal du overføre Microsoft Excel-filen **1099import-data.xlsx**, der indeholder kreditorposter, til den **Filimportkilde (hoved)** SharePoint-mappe, du oprettede tidligere.

[![SharePoint content – Microsoft Excel-eksempelfil til import](./media/GERImportFromSharePoint-08-UploadFile.png)](./media/GERImportFromSharePoint-08-UploadFile.png)

2. I Finance and Operations skal du på siden **Filtilstande for kilderne** vælge **Opdater** for at opdatere siden. Bemærk, at den Excel-fil, der blev overført til SharePoint, blev vist i denne formular med status **Klar**. Følgende statusser understøttes i øjeblikket:

    - **Klar** - Tildeles automatisk til hver ny fil i en SharePoint-mappe. Denne status betyder, at filen er klar til import.
    - **Importerer** - Tildeles automatisk af en ER-rapport, når filen låses af importen for at forhindre, at den bruges af andre processer (hvis mange af dem kører samtidigt).
    - **Importeret** - Tildeles automatisk af en ER-rapport, når filimporten er fuldført. Denne status betyder, at den importerede fil er blevet slettet fra den konfigurerede filkilde (SharePoint-mappe).
    - **Mislykkedes** - Tildeles automatisk af en ER-rapport, når filimporten blev fuldført med fejl eller undtagelser.
    - **På hold** - Tildeles manuelt af brugeren i denne formular. Denne status betyder, at filen ikke importeres på nuværende tidspunkt. Denne status kan bruges til at udskyde importen af visse filer.

[![ER-filtilstandsside for de valgte kilder](./media/GERImportFromSharePoint-09-FileStatesForm.png)](./media/GERImportFromSharePoint-09-FileStatesForm.png)

## <a name="import-data-from-sharepoint-files"></a>Importere data fra SharePoint-filer
1. Åbn ER-konfigurationstræet, vælg **1099-betalingsmodel**, og udvid listen over ER-modelkomponenter.
2. Vælg navnet på modeltilknytningen for at åbne listen over modeltilknytninger for den valgte ER-modelkonfiguration.

[![ER-filtilstandsside for de valgte kilder](./media/GERImportFromSharePoint-10-SelectModelMapping.PNG)](./media/GERImportFromSharePoint-10-SelectModelMapping.PNG)

3. Vælg **Kør** for at køre den valgte modeltilknytning. Da du har konfigureret filkilder for ER-formatet, kan du ændre indstillingen **Filkilde** efter behov. Hvis du lader denne indstilling være uændret, importeres .xslx-filerne fra de konfigurerede kilder (SharePoint-mapperne i dette eksempel).

    I dette eksempel skal du kun importere én fil. Hvis der er flere filer, vælges de til import i samme rækkefølge, som de blev tilføjet i SharePoint-mappen. Hver kørsel af et ER-format importerer en enkelt valgt fil.

[![Køre ER-modeltilknytning](./media/GERImportFromSharePoint-11-RunModelMapping.PNG)](./media/GERImportFromSharePoint-11-RunModelMapping.PNG)

4. Modeltilknytningen kan køre automatisk i batchtilstand. I så fald importeres en enkelt fil fra de konfigurerede filkilder, hver gang en batch kører dette ER-format. Du kan bruge følgende kode til at implementere denne batchkørsel.

    ```
    ERObjectsFactory::createMappingDestinationRunByImportFormatMappingId().run()
    ```

    Når en fil er importeret fra SharePoint-mappen, slettes den fra den pågældende mappe.

5. Angiv bilags-id'et, f.eks. **V-00001**, og vælg derefter **OK**.

[![Køre ER-modeltilknytning](./media/GERImportFromSharePoint-12-ModelMappingRunFinished.PNG)](./media/GERImportFromSharePoint-12-ModelMappingRunFinished.PNG)

6. På siden **Filtilstande for kilderne** skal du vælge **Opdater** for at opdatere siden.

[![ER-filtilstandsside for de valgte kilder](./media/GERImportFromSharePoint-13-FileStatesForm.PNG)](./media/GERImportFromSharePoint-13-FileStatesForm.PNG)

7. I sektionen **Filer** skal du gennemse listen over filer. Sektionen **Kildelogfiler for importformatet** indeholder en oversigt over Excel-filimporten. Da denne fil blev importeret korrekt, er den markeret som **Slettet** i SharePoint-mappen.
8. Gennemse SharePoint-mappen **Filimportkilde (hoved)**. Excel-filer, der blev importeret, er blevet slettet fra denne mappe.
9. Vælg i Finance and Operations **Kreditor** \> **Periodiske opgaver** \> **1099-skat** \> **Kreditorudligning for 1099**.
10. I felterne **Fra dato** og **Til dato** skal du angive relevante værdier. Vælg derefter **Manuelle 1099-transaktioner**.

    De kreditorposteringer, der blev importeret fra Excel-filerne i SharePoint for bilag **V-00001**, vises på siden.

[![Side for 1099-kreditorposteringer](./media/GERImportFromSharePoint-14-ImportedTransactions.PNG)](./media/GERImportFromSharePoint-14-ImportedTransactions.PNG)

## <a name="prepare-an-excel-file-for-import"></a>Forberede en Excel-fil til import
1. Åbn den Excel-fil, du tidligere brugte. I række 3, kolonne 1 skal du tilføje en kreditorkode, der ikke findes i programmet. Føj yderligere falske kreditoroplysninger til rækken.

[![Microsoft Excel-eksempelfil til import fra SharePoint](./media/GERImportFromSharePoint-15-Excel.PNG)](./media/GERImportFromSharePoint-15-Excel.PNG)

2. Overfør den opdaterede Excel-fil, der indeholder kreditorposteringer til SharePoint-mappen **Filimportkilde (hoved)**.
3. I Finance and Operations skal du åbne ER-konfigurationstræet, vælge **1099-betalingsmodel** og udvide listen over ER-modelkomponenter.
4. Vælg navnet på modeltilknytningen for at opdatere modeltilknytningen, så den forkerte kreditorkode betragtes som en fejl under dataimporten.
5. Vælg **Designer**.
6. Under fanen **Valideringer** skal du ændre efter-valideringshandlingen for den valideringsregel, der blev konfigureret, for at vurdere, om den kreditorkonto, der importeres, findes i programmet. Opdater værdien i feltet **Efter-valideringshandling** for at **Stop udførelse**, gemme ændringerne og lukke siden.

[![Side for ER-modeltilknytningsdesigner](./media/GERImportFromSharePoint-16-UpdateModelMapping.PNG)](./media/GERImportFromSharePoint-16-UpdateModelMapping.PNG)

7. Gem ændringerne, og luk ER-modeltilknytningsdesigneren.
8. Vælg **Kør** for at køre den ændrede ER-modeltilknytning.
9. Angiv bilags-id'et, f.eks. **V-00002**, og vælg derefter **OK**.

    Bemærk, infologgen indeholder en besked med oplysninger om, at der i en fil i en SharePoint-mappe findes en forkert kreditorkonto, som ikke kan importeres.

[![Køre ER-modeltilknytning](./media/GERImportFromSharePoint-17-ModelMappingRunFinished.PNG)](./media/GERImportFromSharePoint-17-ModelMappingRunFinished.PNG)

10. På siden **Filtilstande for kilderne** skal du vælge **Opdater** og derefter i sektionen **Filer** gennemgå listen over filer.

[![ER-filtilstandsside for de valgte kilder](./media/GERImportFromSharePoint-18-FileStatesForm.PNG)](./media/GERImportFromSharePoint-18-FileStatesForm.PNG)

Sektionen **Kildelogfiler for importformatet** angiver, at importen mislykkedes, og at filen stadig er i SharePoint-mappen (afkrydsningsfeltet **Er slettet** er ikke markeret). Hvis du reparerer denne fil i SharePoint ved at tilføje den korrekte kreditorkode og derefter ændrer status for filen fra **Mislykkedes** til **Klar** i sektionen **Kildelogfiler for importformatet**, kan du importere filen igen.

11. Gennemse SharePoint-mappen **Filimportkilde (hoved)**. Bemærk, at den Excel-fil, der ikke blev importeret, stadig findes i denne mappe.
12. I Finance and Operations skal du vælge **Kreditor** \> **Periodiske opgaver** \> **1099-skat** \> **Kreditorudligning for 1099'er**, angive de relevante værdier i **Fra dato** og **Til dato**-felterne og derefter vælge **Manuelle 1099-transaktioner**.

    Kun posteringer for bilag V-00001 er tilgængelige. Ingen posteringer for bilag V-00002 er tilgængelige, selvom fejlen for den sidste importerede transaktion blev fundet i Excel-filen.

