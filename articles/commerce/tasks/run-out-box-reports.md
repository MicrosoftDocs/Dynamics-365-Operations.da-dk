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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d148fa36a116860af8c44043d90759b8a2d76fb
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140755"
---
# <a name="generate-and-run-out-of-box-reports"></a><span data-ttu-id="93de2-103">Oprette og køre out of box-rapporter</span><span class="sxs-lookup"><span data-stu-id="93de2-103">Generate and run out of box reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="93de2-104">Brug denne opgaveguide til at køre standardrapporter i Headquarters fra forskellige arbejdsområder og forespørgsler og salgsrapporter, der er placeret i Commerce.</span><span class="sxs-lookup"><span data-stu-id="93de2-104">Use this task guide to run out of box reports in Headquarters from different workspaces and Inquiries & Sales reports located in Commerce.</span></span>

<span data-ttu-id="93de2-105">Det demodatafirma, der bruges til at oprette denne post, er USRT.</span><span class="sxs-lookup"><span data-stu-id="93de2-105">The demo data company used to create this recording is USRT.</span></span> <span data-ttu-id="93de2-106">Denne registrering er beregnet til rollen systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="93de2-106">This recording is intended for the System administrator role.</span></span>

## <a name="launch-reports-from-workspaces"></a><span data-ttu-id="93de2-107">Start rapporter fra arbejdsområder</span><span class="sxs-lookup"><span data-stu-id="93de2-107">Launch reports from workspaces</span></span>
1. <span data-ttu-id="93de2-108">Gå til Retail og Commerce > Produkter og kategorier > Kategori og produktstyring.</span><span class="sxs-lookup"><span data-stu-id="93de2-108">Go to Retail and Commerce > Products and categories > Category and product management.</span></span>
2. <span data-ttu-id="93de2-109">Klik på pilen for at udvide eller skjule sektionen Rapporter.</span><span class="sxs-lookup"><span data-stu-id="93de2-109">Click the arrow to expand or collapse the Reports section.</span></span>
3. <span data-ttu-id="93de2-110">Klik på Rapport over topprodukter.</span><span class="sxs-lookup"><span data-stu-id="93de2-110">Click Top products report.</span></span>
4. <span data-ttu-id="93de2-111">Indtast en dato i feltet Fra dato.</span><span class="sxs-lookup"><span data-stu-id="93de2-111">In the From date field, enter a date.</span></span>
5. <span data-ttu-id="93de2-112">Indtast en dato i feltet Til dato.</span><span class="sxs-lookup"><span data-stu-id="93de2-112">In the To date field, enter a date.</span></span>
6. <span data-ttu-id="93de2-113">Klik på rullelisten i feltet Kanal for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="93de2-113">In the Channel field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="93de2-114">Vælg "Contoso Retail\Contoso Retail USA\Central\Houston" i træet.</span><span class="sxs-lookup"><span data-stu-id="93de2-114">In the tree, select 'Contoso Retail\Contoso Retail USA\Central\Houston'.</span></span>
    * <span data-ttu-id="93de2-115">Dette viser standardorganisationshierarkiet for Commerce-rapportering.</span><span class="sxs-lookup"><span data-stu-id="93de2-115">This shows the default organization hierarchy for Commerce reporting purpose.</span></span>   <span data-ttu-id="93de2-116">Gå til Virksomhedsadministration > Organisationer > Formål med organisationshierarkier, og vælg Commerce-rapportering, og kontrollér under Tildelte hierarkier det hierarkinavn, som standardkolonnen er markeret for.</span><span class="sxs-lookup"><span data-stu-id="93de2-116">Go to Organization administration > Organizations > Organization hierarchy purposes and choose Commerce reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span> <span data-ttu-id="93de2-117">Som en del af demodata (bruges til denne opgaveregistrering) vil du se, at Butikker efter område er standardorganisationshierarkiet for formål med rapportering.</span><span class="sxs-lookup"><span data-stu-id="93de2-117">As part of demo data (used for this task recording) you would notice, Stores by Region, is the default organization hierarchy for the reporting purpose.</span></span>     
8. <span data-ttu-id="93de2-118">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="93de2-118">Click OK.</span></span>
9. <span data-ttu-id="93de2-119">Vælg en indstilling i feltet Vis.</span><span class="sxs-lookup"><span data-stu-id="93de2-119">In the View field, select an option.</span></span>
10. <span data-ttu-id="93de2-120">Vælg en indstilling i feltet Efter.</span><span class="sxs-lookup"><span data-stu-id="93de2-120">In the By field, select an option.</span></span>
11. <span data-ttu-id="93de2-121">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="93de2-121">Click OK.</span></span>

## <a name="launch-reports-from-the-inquiries-and-sales-reports"></a><span data-ttu-id="93de2-122">Starte rapporter fra forespørgslerne og salgsrapporterne</span><span class="sxs-lookup"><span data-stu-id="93de2-122">Launch reports from the inquiries and sales reports</span></span>
1. <span data-ttu-id="93de2-123">Gå til Retail og Commerce > Forespørgsler og rapporter > Salgsrapporter > Salgsrapport for kategori.</span><span class="sxs-lookup"><span data-stu-id="93de2-123">Go to Retail and Commerce > Inquiries and reports > Sales reports > Category sales report.</span></span>
2. <span data-ttu-id="93de2-124">Indtast en dato i feltet Fra dato.</span><span class="sxs-lookup"><span data-stu-id="93de2-124">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="93de2-125">Indtast en dato i feltet Til dato.</span><span class="sxs-lookup"><span data-stu-id="93de2-125">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="93de2-126">Klik på rullelisten i feltet Kanal for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="93de2-126">In the Channel field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="93de2-127">Vælg "Contoso Retail\Contoso Retail USA\West\Seattle" i træet.</span><span class="sxs-lookup"><span data-stu-id="93de2-127">In the tree, select 'Contoso Retail\Contoso Retail USA\West\Seattle'.</span></span>
    * <span data-ttu-id="93de2-128">Dette viser standardorganisationshierarkiet for Commerce-rapportering.</span><span class="sxs-lookup"><span data-stu-id="93de2-128">This shows the default organization hierarchy for Commerce reporting purpose.</span></span> <span data-ttu-id="93de2-129">Gå til Virksomhedsadministration > Organisationer > Formål med organisationshierarkier, og vælg Commerce-rapportering, og kontrollér under Tildelte hierarkier det hierarkinavn, som standardkolonnen er markeret for.</span><span class="sxs-lookup"><span data-stu-id="93de2-129">Go to Organization administration > Organizations > Organization hierarchy purposes and choose Commerce reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span> <span data-ttu-id="93de2-130">Som en del af demodata (bruges til denne opgaveregistrering) vil du se, at Butikker efter område er standardorganisationshierarkiet for formål med rapportering.</span><span class="sxs-lookup"><span data-stu-id="93de2-130">As part of demo data (used for this task recording) you would notice, Stores by Region, is the default organization hierarchy for the reporting purpose.</span></span>     
6. <span data-ttu-id="93de2-131">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="93de2-131">Click OK.</span></span>
7. <span data-ttu-id="93de2-132">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="93de2-132">Click OK.</span></span>

## <a name="export-an-hq-reports"></a><span data-ttu-id="93de2-133">Eksporter en HQ-rapport</span><span class="sxs-lookup"><span data-stu-id="93de2-133">Export an HQ reports</span></span>
1. <span data-ttu-id="93de2-134">Gå til Retail og Commerce > Forespørgsler og rapporter > Salgsrapporter > Salgsrapport for organisation.</span><span class="sxs-lookup"><span data-stu-id="93de2-134">Go to Retail and Commerce > Inquiries and reports > Sales reports > Organization sales report.</span></span>
2. <span data-ttu-id="93de2-135">Indtast en dato i feltet Fra dato.</span><span class="sxs-lookup"><span data-stu-id="93de2-135">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="93de2-136">Indtast en dato i feltet Til dato.</span><span class="sxs-lookup"><span data-stu-id="93de2-136">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="93de2-137">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="93de2-137">Click OK.</span></span>
5. <span data-ttu-id="93de2-138">Klik på Eksporter.</span><span class="sxs-lookup"><span data-stu-id="93de2-138">Click Export.</span></span>
6. <span data-ttu-id="93de2-139">Klik på PDF.</span><span class="sxs-lookup"><span data-stu-id="93de2-139">Click PDF.</span></span>

