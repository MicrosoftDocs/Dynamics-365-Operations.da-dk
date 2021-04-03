---
title: Få adgang til programmetadata ved hjælp af ER-konfiguration
description: Dette emne forklarer, hvordan en Regulatory Configuration Service-bruger kan designe en ny elektronisk rapporteringsmodel ved hjælp af metadata.
author: NickSelin
manager: AnnBe
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 91c50047781fdc21c9157ceb634822c6cfb5a075
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559645"
---
# <a name="access-application-metadata-by-using-er-configuration"></a>Få adgang til programmetadata ved hjælp af ER-konfiguration

[!include [banner](../../includes/banner.md)]

Følgende trin beskriver, hvordan en RCS-bruger (Regulatory Configuration Service) i rollen Systemadministrator eller Udvikler til elektronisk rapportering kan designe en ny ER-modeltilknytning ved hjælp af metadataene i applikationen. Der opnås adgang til programmetadata ved hjælp af en ER-metadatakonfiguration, der indeholder et eksempel sæt af metadata for adgang til udenrigshandelstransaktioner. Du skal først fuldføre RCS-trinnene i procedureemnet [Oprette konfigurationsudbydere og markere dem som aktive](er-configuration-provider-mark-it-active-2016-11.md). Udfør derefter trinnene i emnet [Klargør de programmetadata, der skal bruges i RCS](prepare-application-metadata-rcs.md).

## <a name="prerequisites"></a>Forudsætninger
1. Gå til **Alle arbejdsområder** > **Elektronisk rapportering**. 
2. Sørg for, at konfigurationsudbyderen for eksempelfirmaet Litware Inc. er tilgængelig og markeret som **Aktiv**. Hvis du ikke kan se denne konfigurationsudbyder, skal du fuldføre trinnene i proceduren [Opret konfigurationsudbydere, og markér dem som aktive](er-configuration-provider-mark-it-active-2016-11.md). 

## <a name="import-metadata-configuration"></a>Importere konfiguration af metadata 
1. Klik på **Konfiguration af metadata**. 
2. Importer den ER-metadatakonfiguration, der indeholder metadata, der er konfigureret til at generere elektroniske dokumenter for udenrigshandel. Denne ER-konfiguration af metadata er blevet eksporteret som en XML-fil, mens trinnene i proceduren for [Klargøring af de programmetadata, der skal bruges i RCS](prepare-application-metadata-rcs.md) blev fuldført. 
3. Klik på **Udveksling**. 
4. Klik på **Indlæs fra XML-fil**. 
5. Klik på **Gennemse**, og vælg filen 'Udenrigshandelmetadata.xml'. 
6. Klik på **OK**. 
7. Luk siden. 

## <a name="create-data-model-configuration"></a>Oprette datamodelkonfiguration
1. Klik på **Rapporteringskonfigurationer**. 
2. Klik på **Opret konfiguration** for at åbne dialogboksen. 
3. Skriv 'Udenrigshandelmodel' i feltet **Navn**. 
4. Klik på **Opret konfiguration**. 
5. Klik på **Designer**. 
6. Klik på **Ny** for at åbne dialogboksen Fjern. 
7. Skriv "Rod" i feltet **Navn**. 
8. Klik på **Tilføj**. 
9. Klik på **Ny** for at åbne dialogboksen Fjern. 
10.    Skriv 'Transaktion' i feltet **Navn**. 
11.    Vælg **Liste over poster** i feltet **Varetype**. 
12.    Klik på **Tilføj**. 
13.    Klik på **Ny** for at åbne dialogboksen Fjern. 
14.    Skriv 'Varekode' i feltet **Navn**. 
15.    Vælg **Streng** i feltet **Varetype**. 
16.    Klik på **Tilføj**. 
17.    Klik på **Ny** for at åbne dialogboksen Fjern. 
18.    Skriv 'Faktureret beløb' i feltet **Navn**. 
19.    Vælg **Kommatal** i feltet **Varetype**. 
20.    Klik på **Tilføj**. 
21.    Klik på **Ny** for at åbne dialogboksen Fjern. 
22.    Skriv 'Dato' i feltet **Navn**. 
23.    Vælg **Dato** i feltet **Varetype**. 
24.    Klik på **Tilføj**. 
25.    Klik på **Rodreference**. 
26.    Klik på **OK**. 
27.    Klik på **Gem**. 
28.    Luk siden. 
29.    Klik på **Skift status**. 
30.    Klik på **Fuldfør**. 
31.    Klik på **OK**. 

## <a name="create-model-mapping-configuration"></a>Oprette konfiguration af modeltilknytning 
1. Klik på **Opret konfiguration** for at åbne dialogboksen. 
2. Angiv 'Modeltilknytning baseret på datamodellen Udenrigshandelmodel' i feltet **Ny**. 
3. Skriv 'Tilknytning af udenrigshandel' i feltet **Navn**. 
4. Klik på **Opret konfiguration**. 
5. Udvid sektionen **Forudsætninger**. 
6. Klik på **Rediger**. 
7. Klik på **Ny**. 
8. Markér den valgte række på listen. 
9. Vælg **Konfiguration** i feltet **Type af forudsætningskomponent**. 
10.    Vælg konfiguration **Udenrigshandelmetadata**. 
11.    Klik på **Gem**. 
12.    Vi har tilføjet referencen til version 1 af konfigurationen af 'Udenrigshandelmetadata'. Der tilbydes programmetadata fra denne konfiguration, mens denne modeltilknytning bliver udformet. 
13.    Luk siden. 
14.    Klik på **Designer**. 
15.    Klik på **Designer**. 
16.    Vælg **Dynamics 365 for Operations\Tabelposter** i træet. 
17.    Klik på **Tilføj rod**. 
18.    Skriv 'Intrastat' i feltet **Navn**. 
19.    Vælg **Intrastat** -tabelposter. 
20.    Klik på **OK**. 

> [!NOTE]
> De eneste to tabeller blev tilbudt, da der kun blev føjet to tabeller til det sæt metadata, der bruges i øjeblikket. 

21.    Klik på **Bind**. 
22.    Udvid **Intrastat** i træet. 
23.    Vælg **Intrastat\AmountMST** i træet. 
24.    Udvid **Transaktion = Intrastat** i træet. 
25.    Vælg **Transaktion = Intrastat\Faktureret beløb** i træet. 
26.    Klik på **Bind**. 
27.    Vælg **Intrastat\TransDate** i træet. 
28.    Vælg **Transaktion = Intrastat\Dato** i træet. 
29.    Klik på **Bind**. 
30.    Udvid **Intrastat\>Relationer** i træet. 
31.    Udvid **Intrastat\>Relationer\IntrastatCommodity** i træet. 
32.    Vælg **Intrastat\>Relationer\IntrastatCommodity\Kode** i træet. 
33.    Vælg **Transaktion = Intrastat\Varekode** i træet. 
34.    Klik på **Bind**. 
35.    Klik på **Valider**. 

> [!NOTE]
> Vi har bundet elementer i datamodellen til elementer i de datakilder, der er beskrevet, ved hjælp af oplysninger om programmetadata fra den ER-metadatakonfiguration, der henvises til. 
36.    Klik på **Gem**. 
37.    Luk siden. 
38.    Luk siden. 
39.    Når det er nødvendigt, kan du udvide det eksisterende sæt metadata og derefter eksportere den nye fuldførte version af ER-metadatakonfiguration. Du kan derefter importere den til RCS og opdatere forudsætningerne for den konfigurerede konfiguration af modeltilknytning, der henviser til en ny version af importeret metadatakonfiguration. 

> [!NOTE]
> Denne måde at hente oplysninger om programmetadata er den eneste, der er tilgængelig for lokalt installerede programmer (når der bruges lokale virksomhedsdata (LBD) eller en lokal installationsmodel).
        


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]