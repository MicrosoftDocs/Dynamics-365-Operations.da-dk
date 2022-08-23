---
title: Importere data fra manuelt valgte filer i batchtilstand
description: Denne artikel forklarer, hvordan du importerer data fra manuelt valgte filer i batchtilstand.
author: kfend
ms.date: 01/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2022-01-01
ms.dyn365.ops.version: Release 10.0.25
ms.custom: 220314
ms.assetid: ''
ms.search.form: ERSolutionTable, ERImportFormatSourceTable, ERWorkspace
ms.openlocfilehash: 21a2ab5f0eb07dda92baf9cc04ee36caeff8b4ec
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288222"
---
# <a name="import-data-from-manually-selected-files-in-batch-mode"></a>Importere data fra manuelt valgte filer i batchtilstand

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

Hvis du vil bruge strukturen til [elektronisk rapportering (ER)](general-electronic-reporting.md) til at importere data fra manuelt valgte indgående filer i batchtilstand, skal du konfigurere et ER-[format](er-overview-components.md#format-component), der understøtter importen. Kør derefter en [modeltilknytning](er-overview-components.md#model-mapping-component) af typen **Til destination**, der bruger det pågældende format som datakilde. Du importerer data ved at navigere til den fil, du vil importere, og vælge den manuelt. 

Den nye ER-funktionalitet, der understøtter import af data i batchtilstand, gør det muligt at konfigurere denne proces uovervåget. Du kan bruge ER-konfigurationer til at udføre dataimport ved at planlægge et nyt batchjob fra ER-brugergrænsefladen.

Denne artikel forklarer, hvordan du importerer data fra en manuelt valgt fil i batchtilstand. I eksemplerne bruges kreditorposteringer som forretningsdata. Disse eksempeltrin kan fuldføres i firmaet **USMF**. Der kræves ingen kodning.

## <a name="prerequisites"></a>Forudsætninger

Før du kan følge eksemplerne i denne artikel, skal du have følgende adgang:

- En af følgende roller:

    - Udvikler til elektronisk rapportering
    - Funktionel konsulent i elektronisk rapportering
    - Systemadministrator

- ER-format og -modelkonfigurationer til 1099-betalinger

### <a name="create-the-required-er-configurations"></a>Oprette de nødvendige ER-konfigurationer

Hvis du vil oprette de nødvendige ER-konfigurationer og have andre forudsætninger, skal du følge et af disse trin:

- Afspil opgaveguiderne **ER Import af data fra en Microsoft Excel-fil**, der er en del af forretningsprocessen **7.5.4.3 Anskaffe/udarbejde IT-tjeneste/løsningskomponenter (10677)**. Disse opgaveguider gennemgår processen med at designe og bruge ER-konfigurationer til at importere kreditorposteringer interaktivt fra Microsoft Excel-filer. Du kan finde flere oplysninger i [Analysere indgående dokumenter i Excel-format](parse-incoming-documents-excel.md).
- Fuldfør eksemplerne i [Konfigurere dataimport fra SharePoint](er-configure-data-import-sharepoint.md). Disse eksempler gennemgår processen med at designe og bruge ER-konfigurationer til at importere kreditorposteringer interaktivt fra Excel-filer, der er gemt i en SharePoint-mappe.

### <a name="download-the-required-er-configurations"></a>Download de nødvendige ER-konfigurationer

1. Download følgende ER-konfigurationer, og gem dem lokalt.

    | Indholdsbeskrivelse | Filer |
    |---------------------|------|
    | **1099-betalingsmodel** Konfiguration af ER-datamodel | [1099model.xml](https://download.microsoft.com/download/b/d/9/bd9e8373-d558-4ab8-aa9b-31981adc97ea/1099model.xml) |
    | ER-formatkonfiguration **til import af kreditorposteringer (Excel)** | [1099format-import-from-excel.xml](https://download.microsoft.com/download/b/3/8/b38faf0a-fbaf-4e9e-84c2-dedae7464880/1099format-import-from-excel.xml) |

2. Brug ER-indstillingen [Indlæs fra XML-fil](er-defer-sequence-element.md#import-the-sample-er-configurations) til at importere de hentede ER-konfigurationer til din forekomst af Dynamics 365 Finance i følgende rækkefølge:

    1. ER-datamodelkonfiguration
    2. Konfiguration af ER-format

### <a name="download-the-required-excel-files"></a>Downloade de nødvendige Excel-filer

- Download følgende eksempeldatasæt, og gem det lokalt.

    | Indholdsbeskrivelse | Filer |
    |---------------------|------|
    | Indgående **1099import-data.xlsx**-fil, der indeholder eksempeldata til import | [1099import-data.xlsx](https://download.microsoft.com/download/f/f/4/ff4dbce9-8364-4391-adee-877945ff01f7/1099import-data.xlsx) |

### <a name="review-the-prerequisites"></a>Gennemgå forudsætningerne

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. På siden **Konfigurationer** kan du gennemgå den forberedte ER-løsning til dataimport i batchtilstand.
3. Gennemgå formatkonfigurationen **Til import af kreditorposteringer (Excel)**.

    - Formatkomponenten for denne konfiguration er beregnet til at fortolke en indgående Excel-fil.
    - Modeltilknytningskomponenten for denne konfiguration bruges til at udfylde basisdatamodellen ved hjælp af data fra den fortolkede Excel-fil.

    ![Konfiguration af ER-format til import af data i batchtilstand fra ER-brugergrænsefladen.](./media/er-configure-data-import-batch-configurations-1.png)

4. Gennemgå konfigurationen af datamodellen **1099-betalingsmodel**.

    - Modelkomponenten for denne konfiguration repræsenterer datamodelstrukturen, der bruges til at overføre data mellem kørende ER-komponenter.
    - Modeltilknytningskomponenten i denne konfiguration bruges til at trække data fra den udførte formatkomponent og derefter opdatere programtabeller.

    ![Konfiguration af ER-datamodel til import af data i batchtilstand fra ER-brugergrænsefladen.](./media/er-configure-data-import-batch-configurations-2.png)

5. Åbn filen **1099import-data.xlsx** i Excel.

    ![Eksempel på en Excel-fil med data til import i batchtilstand.](./media/er-configure-data-import-batch-excel-content.png)

## <a name="enable-batch-data-import-for-er-from-the-ui"></a>Aktivere batchdataimport for ER fra brugergrænsefladen

1. Gå til **Systemadministration** \> **Arbejdsområder** \> **Funktionsstyring**.
2. Vælg funktionen **Kør ER-import af manuelt uploadede dokumenter i batch** i arbejdsområdet **Funktionsstyring**, og vælg derefter **Aktivér nu**.

## <a name="import-data-from-manually-selected-excel-files"></a>Importere data fra manuelt valgte Excel-filer

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. På siden **Konfigurationer** skal du i datamodelkonfigurationen vælge **1099-betalingsmodel**.
3. Vælg linket **Til manuel import af 1099-transaktioner** i oversigtspanelet **Konfigurationskomponenter**.
4. På siden **Model til datakildetilknytning** er modeltilknytningen **Til manuel import af 1099-transaktioner** valgt på forhånd. Vælg **Kør**.
5. Vælg **Gennemse** i oversigtspanelet **Parametre**. Find og vælg filen **1099import-data.xlsx**, og vælg derefter **OK**.
6. Gå til feltet **Angiv bilags-id**, og angiv **V-00001**.
7. Angiv **Batchbehandling** til **Ja** i oversigtspanelet **Kør i baggrunden**.

    Bemærk, at feltet **Opgavebeskrivelse** er angivet til **Kørsel af modeltilknytning 'Til manuel import af 1099-transaktioner', konfiguration '1099-betalingsmodel'**. Denne værdi angiver, at udførelsen af den valgte modeltilknytning planlægges som et nyt batchjob.

    ![Angiv detaljer for dataimporten i batchtilstand i dialogboksen Parametre for elektronisk rapport.](./media/er-configure-data-import-batch-execution-parameters.png)

8. Vælg **OK**. En meddelelse giver dig besked om, at et nyt batchjob er planlagt.

    ![Meddelelse om et nyt planlagt batchjob på siden Tilknytning af model til datakilde.](./media/er-configure-data-import-batch-scheduled-job-info.png)

## <a name="review-the-data-import-results-on-the-batch-job-page"></a>Gennemse resultaterne af dataimporten på siden Batchjob

1. Gå til **Almindeligt** \> **Forespørgsler** \> **Batchjob** \> **Mine batchjob**.
2. Filtrer listen over batchjob på siden **Batchjob** for at finde det planlagte batch, og vælg det derefter.
3. Vælg linket **Job-id** for at gennemse joboplysninger.
4. I oversigtspanelet **Batchopgaver** skal du vælge **Log på**.

    ![Knappen Log på siden Batchjob.](./media/er-configure-data-import-batch-scheduled-job-record.png)

5. Gennemse kørselsdetaljerne.

    ![Udførelseslog for det planlagte batchjob på batchjobsiden.](./media/er-configure-data-import-batch-scheduled-job-log.png)

## <a name="change-the-data-import-parameters"></a>Ændre parametre for dataimport

Når batchen er planlagt, og mens den endnu ikke er kørt, kan du ændre parametrene for den planlagte dataimport.

1. Gå til **Almindeligt** \> **Forespørgsler** \> **Batchjob** \> **Mine batchjob**.
2. Filtrer listen over batchjob på siden **Batchjob** for at finde det planlagte batch, og vælg det derefter.
3. Vælg **Skift status**.
4. I dialogboksen **Vælg ny status** skal du vælge **Tilbagehold** og derefter vælge **OK**.
5. Vælg linket **Job-id** for at gå til joboplysningerne.
6. I oversigtspanelet **Batchopgaver** skal du vælge **Parametre**.
7. Følg disse trin i dialogboksen **Elektroniske rapporteringsparametre**:

    1. Vælg **Gennemse** for at vælge den alternative fil til dataimport.
    2. Vælg **Angiv bilags-id** for at ændre bilagsnummeret for import af kreditorposteringer.

        ![Ændring af parametrene for dataimporten for det planlagte batchjob i dialogboksen Parametre til elektronisk rapportering.](./media/er-configure-data-import-batch-scheduled-job-parameters.png)

    3. Vælg **OK**.

8. Kontrollér, at batchen stadig er valgt, og vælg derefter **Skift status** igen.
9. I dialogboksen **Vælg ny status** skal du vælge **Venter** og derefter vælge **OK**.

## <a name="review-the-data-import-results-on-the-er-source-page"></a>Gennemse resultaterne af dataimporten på siden ER-kilde

1. Gå til **Virksomhedsadministration** \> **Elektronisk rapportering** \> **Kilde til elektronisk rapportering**.
2. Vælg den **Til import af kreditorposteringer (Excel)**, der blev oprettet automatisk under dataimporten.

    ![Post for konfigurationen Til import af kreditorposteringer (Excel) på siden Elektronisk rapporteringskilde.](./media/er-configure-data-import-batch-files-source-1.png)

3. Vælg **Filtilstande for kilderne**.
4. Gennemse importoplysningerne i oversigtspanelerne **Filer** og **Kildefiler til importformatet**.
5. Vælg posten i oversigtspanelet **Filer**. Bemærk, at den importerede fil er knyttet til denne post.

    ![Importeret fil, der er tilknyttet posten, på siden Filtilstande for kilderne.](./media/er-configure-data-import-batch-files-source-2.png)

6. Vælg **Vedhæftede filer** for at gennemse den importerede fil.

    ![Importeret fil på dokumentvisningssiden.](./media/er-configure-data-import-batch-files-source-3.png)

    > [!TIP]
    > Til at beholde disse vedhæftede filer bruger ER-strukturen en dokumenttype, der er [angivet](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) for det aktuelle firma i feltet **Andre** i ER-parametrene.

## <a name="review-the-data-import-results-on-the-vendor-settlement-for-1099s-page"></a>Gennemse resultaterne af dataimporten på kreditorudligningen for 1099s-siden

1. Gå til **Kreditor** \> **Periodiske opgaver** \> **1099-skat** \> **Kreditorudligning for 1099**.
2. I feltet **Fra dato** skal du indtaste **31-12-2017** (31. december 2017).
3. Vælg **Manuelle 1099-transaktioner**.

    ![Importerede kreditorposteringer på siden Moms 1099-transaktioner.](./media/er-configure-data-import-batch-imported-data.png)

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over elektronisk rapportering](general-electronic-reporting.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
