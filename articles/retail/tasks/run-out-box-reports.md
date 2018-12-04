--- 
title: "Oprette og køre out of box-rapporter"
description: "Brug denne opgaveguide til at køre out of box-rapporter i Headquarters fra forskellige arbejdsområder og forespørgsler og salgsrapporter, der er placeret under Detail og handel."
author: ashishmsft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailCategoryAndProductWorkspace, RetailOrgHierarchyTreeLookup, SrsReportViewerForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: b42f86fc243312d18654b1a048f9dffb29afd187
ms.contentlocale: da-dk
ms.lasthandoff: 09/14/2018

---
# <a name="generate-and-run-out-of-box-reports"></a>Oprette og køre out of box-rapporter

[!include[task guide banner](../includes/task-guide-banner.md)]

Brug denne opgaveguide til at køre out of box-rapporter i Headquarters fra forskellige arbejdsområder og forespørgsler og salgsrapporter, der er placeret under Detail og handel.



Det demodatafirma, der bruges til at oprette denne post, er USRT. Denne registrering er beregnet til rollen systemadministrator.


## <a name="launch-reports-from-workspaces"></a>Start rapporter fra arbejdsområder
1. Gå til Detail og handel > Produkter og kategorier > Kategori og produktstyring.
2. Klik på pilen for at udvide eller skjule sektionen Rapporter.
3. Klik på Rapport over topprodukter.
4. Indtast en dato i feltet Fra dato.
5. Indtast en dato i feltet Til dato.
6. Klik på rullelisten i feltet Kanal for at åbne opslaget.
7. Vælg "Contoso Retail\Contoso Retail USA\Central\Houston" i træet.
    * Dette viser standardhierarkiet for detailorganisationen med henblik på detailrapportering.   Gå til Virksomhedsadministration > Organisationer > Formål med organisationshierarkier, og vælg Detailrapportering, og kontrollér under Tildelte hierarkier det hierarkinavn, som standardkolonnen er markeret for.      Som en del af demodata (bruges til denne opgaveregistrering) vil du se, at Detailbutikker efter område er standardorganisationshierarkiet for formål med detailrapportering.     
8. Klik på OK.
9. Vælg en indstilling i feltet Vis.
10. Vælg en indstilling i feltet Efter.
11. Klik på OK.

## <a name="launch-reports-from-the-inquiries-and-sales-reports-located-under-retail--commerce-app-link"></a>Start rapporter fra forespørgsler og salg placeret under Detail og handel; link til Commerce-app.
1. Gå til Detail og handel > Forespørgsler og rapporter > Salgsrapporter > Salgsrapport for kategori.
2. Indtast en dato i feltet Fra dato.
3. Indtast en dato i feltet Til dato.
4. Klik på rullelisten i feltet Kanal for at åbne opslaget.
5. Vælg "Contoso Retail\Contoso Retail USA\West\Seattle" i træet.
    * Dette viser standardhierarkiet for detailorganisationen med henblik på detailrapportering.   Gå til Virksomhedsadministration > Organisationer > Formål med organisationshierarkier, og vælg Detailrapportering, og kontrollér under Tildelte hierarkier det hierarkinavn, som standardkolonnen er markeret for.      Som en del af demodata (bruges til denne opgaveregistrering) vil du se, at Detailbutikker efter område er standardorganisationshierarkiet for formål med detailrapportering.     
6. Klik på OK.
7. Klik på OK.

## <a name="export-an-hq-reports"></a>Eksporter en HQ-rapport
1. Gå til Detail og handel > Forespørgsler og rapporter > Salgsrapporter > Salgsrapport for organisation.
2. Indtast en dato i feltet Fra dato.
3. Indtast en dato i feltet Til dato.
4. Klik på OK.
5. Klik på Eksporter.
6. Klik på PDF.


