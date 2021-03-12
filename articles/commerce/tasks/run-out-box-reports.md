---
title: Oprette og køre out of box-rapporter
description: Brug denne opgaveguide til at køre standardrapporter i Headquarters fra forskellige arbejdsområder og forespørgsler og salgsrapporter, der er placeret i Commerce.
author: ashishmsft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailCategoryAndProductWorkspace, RetailOrgHierarchyTreeLookup, SrsReportViewerForm
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e11bca1e6850f401f52c2ccbea1089a4e71591c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003697"
---
# <a name="generate-and-run-out-of-box-reports"></a>Oprette og køre out of box-rapporter

[!include [banner](../includes/banner.md)]

Brug denne opgaveguide til at køre standardrapporter i Headquarters fra forskellige arbejdsområder og forespørgsler og salgsrapporter, der er placeret i Commerce.

Det demodatafirma, der bruges til at oprette denne post, er USRT. Denne registrering er beregnet til rollen systemadministrator.

## <a name="launch-reports-from-workspaces"></a>Start rapporter fra arbejdsområder
1. Gå til Retail og Commerce > Produkter og kategorier > Kategori og produktstyring.
2. Klik på pilen for at udvide eller skjule sektionen Rapporter.
3. Klik på Rapport over topprodukter.
4. Indtast en dato i feltet Fra dato.
5. Indtast en dato i feltet Til dato.
6. Klik på rullelisten i feltet Kanal for at åbne opslaget.
7. Vælg "Contoso Retail\Contoso Retail USA\Central\Houston" i træet.
    * Dette viser standardorganisationshierarkiet for Commerce-rapportering.   Gå til Virksomhedsadministration > Organisationer > Formål med organisationshierarkier, og vælg Commerce-rapportering, og kontrollér under Tildelte hierarkier det hierarkinavn, som standardkolonnen er markeret for. Som en del af demodata (bruges til denne opgaveregistrering) vil du se, at Butikker efter område er standardorganisationshierarkiet for formål med rapportering.     
8. Klik på OK.
9. Vælg en indstilling i feltet Vis.
10. Vælg en indstilling i feltet Efter.
11. Klik på OK.

## <a name="launch-reports-from-the-inquiries-and-sales-reports"></a>Starte rapporter fra forespørgslerne og salgsrapporterne
1. Gå til Retail og Commerce > Forespørgsler og rapporter > Salgsrapporter > Salgsrapport for kategori.
2. Indtast en dato i feltet Fra dato.
3. Indtast en dato i feltet Til dato.
4. Klik på rullelisten i feltet Kanal for at åbne opslaget.
5. Vælg "Contoso Retail\Contoso Retail USA\West\Seattle" i træet.
    * Dette viser standardorganisationshierarkiet for Commerce-rapportering. Gå til Virksomhedsadministration > Organisationer > Formål med organisationshierarkier, og vælg Commerce-rapportering, og kontrollér under Tildelte hierarkier det hierarkinavn, som standardkolonnen er markeret for. Som en del af demodata (bruges til denne opgaveregistrering) vil du se, at Butikker efter område er standardorganisationshierarkiet for formål med rapportering.     
6. Klik på OK.
7. Klik på OK.

## <a name="export-an-hq-reports"></a>Eksporter en HQ-rapport
1. Gå til Retail og Commerce > Forespørgsler og rapporter > Salgsrapporter > Salgsrapport for organisation.
2. Indtast en dato i feltet Fra dato.
3. Indtast en dato i feltet Til dato.
4. Klik på OK.
5. Klik på Eksporter.
6. Klik på PDF.

