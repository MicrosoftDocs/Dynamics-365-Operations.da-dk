---
title: Importér kreditorkataloger
description: Dette emne beskriver processen for import af data fra kreditorkataloget.
author: GalynaFedorova
ms.date: 03/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationRequests, CatVendorCatalogDetails, CatVendorCatalogReleaseApprovedProducts, CatVendorCMRDetails, CatVendorCatalogProductPerCompanyStatus, CatVendorMaintenanceEventLog, CatVendorCatalogReviewTool, CatVendorCatalogFileUpload, CatVendorCatalogMaintenanceRequest, CatVendorCatalogFileInLegalEntity, CatVendorCatalogSchema, CatVendorCatalogFilePreviewPane, CatVendorCatalogImportParameter
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gfedorova
ms.search.validFrom: 2018-04-20
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: decf8b487f939ecb7b0ecf8be377fdd85e3947cf
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/03/2022
ms.locfileid: "8676853"
---
# <a name="import-vendor-catalogs"></a>Importér kreditorkataloger

[!include[banner](../includes/banner.md)]

## <a name="vendor-catalogs-import"></a>Import af kreditorkataloger

I Dynamics 365 Supply Chain Management kan indkøbsmedarbejderne oprette og vedligeholde kataloger, som virksomhedens medarbejdere derefter kan bruge, når de bestiller varer og tjenesteydelser til intern brug. Hvis du vil oprette et indkøbskatalog, kan du tilføje de varer og tjenester, som du vil gøre tilgængelige for medarbejderne, enten ved at importere produktkataloget eller ved manuelt at tilføje data fra produktkataloget til produktmasteren. 

Du kan overføre katalogdata, som er indsendt af en kreditor, fra klienten for Microsoft Dynamics 365.

De produktdata, som en kreditor sender til dig i form af en CMR-fil (Catalog Maintenance Request – anmodning om katalogvedligeholdelse), skal være i filformatet XML. CMR-filen skal indeholde alle oplysninger om de produkter, som kreditoren leverer til dit firma.

## <a name="import-vendor-catalog-data"></a>Importere oplysninger fra et kreditorkatalog

Hvis du vil importere oplysninger fra et kreditorkatalog, skal du fuldføre følgende opgaver:

1. Opret et projekt i det arbejdsområde for Datastyring, hvor du har defineret dine regler for tilknytning af data. Vælg **Datastyring** og derefter **Opsætning af roller for dataprojekter**.

2. Opret et indkøbskategorihierarki, og knyt dine leverandører til bestemte indkøbskategorier. Hvis du bruger varekoder, skal du føje varekoder til indkøbskategorierne. Du kan finde flere oplysninger om opsætning af et hierarki af indkøbskategorier under [Konfigurere et indkøbskategorihierarki](../procurement/tasks/set-up-procurement-category-hierarchy.md).

3. Konfigurer kreditoren til katalogimport. Vælg en kreditor, og vælg derefter **Indkøb** > **Opsætning** > **Konfigurer kreditor til katalogimport**.

4. Konfigurer arbejdsgangen til katalogimport. Opret en skabelon for CMR-filen, og del den med kreditoren.

5. Vælg **Indkøb og forsyning** \> **Generelt** \> **Kataloger** \> **Kreditorkataloger** for at oprette et kreditorkatalog. De CMR-filer, som du modtager fra leverandøren, grupperes i dette katalog. 

6. Overfør CMR-filen.

7. Gennemgå, godkend eller afvis produkterne i kreditorkataloget. Produkterne knyttes automatisk til indkøbskategorierne. 

Godkendte produkter føjes til produktmasteren og frigives til de valgte juridiske enheder. Kun godkendte produkter kan føjes til indkøbskataloget.

## <a name="generate-a-catalog-import-file-template"></a>Generere en filskabelon til katalogimport

Filskabelonen til katalogimport er en XSD-fil, som du kan bruge til at oprette en CMR-fil til kreditorens produkter. Du kan bruge CMR-filen til at oprette et nyt katalog, erstatte et eksisterende katalog eller redigere et eksisterende katalog.

1. Vælg **Indkøb og forsyning** \> **Kataloger** \> **Kreditorkataloger**, og dobbeltklik på det katalog, du vil arbejde med.

2. Hent den aktuelle katalogimportskabelon (XSD-fil). På siden **Opdater katalog** i **Handlingsrude** på fanen **Kataloger** i gruppen **Relaterede oplysninger** skal du klikke på **Generér skabelon til katalog** og vælge **Indkøbskategori**.

    - Med indstillingen **Indkøbskategori** kan du generere en katalogskabelon, der omfatter de indkøbskategorier, som kreditoren har tilladelse til at levere produkter fra.

3. Vælg **Gem som** i dialogboksen, vælg den placering, hvor du vil gemme katalogfilskabelonen, og gem filen.

Yderligere oplysninger og eksempler finder du i dette blogindlæg: [Kreditorkataloger i Dynamics AX](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]