---
title: Balance - økonomiske rapporter
description: I denne artikel beskrives standardrapporterne til balancer. Her beskrives også de komponenter, der er knyttet til disse rapporter.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinanicalReports
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 12274
ms.assetid: 52f78229-f531-4d16-b337-e2628994acb6
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9dcac902118c643b9a9d783c12f02fa5c90827b
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839563"
---
# <a name="balance-sheet-financial-reports"></a><span data-ttu-id="dd91f-104">Balance - økonomiske rapporter</span><span class="sxs-lookup"><span data-stu-id="dd91f-104">Balance sheet financial reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dd91f-105">I denne artikel beskrives standardrapporterne til balancer.</span><span class="sxs-lookup"><span data-stu-id="dd91f-105">This article describes the default reports for balance sheets.</span></span> <span data-ttu-id="dd91f-106">Her beskrives også de komponenter, der er knyttet til disse rapporter.</span><span class="sxs-lookup"><span data-stu-id="dd91f-106">It also describes the building blocks that are associated with these reports.</span></span> 

<a name="default-balance-sheet-reports"></a><span data-ttu-id="dd91f-107">Standardbalancerapporter</span><span class="sxs-lookup"><span data-stu-id="dd91f-107">Default balance sheet reports</span></span>
-----------------------------

<span data-ttu-id="dd91f-108">Der er to standardbalancerapporter.</span><span class="sxs-lookup"><span data-stu-id="dd91f-108">There are two default balance sheet reports.</span></span> <span data-ttu-id="dd91f-109">I den ene rapport er afsnittene stablet.</span><span class="sxs-lookup"><span data-stu-id="dd91f-109">On one report, the sections are stacked.</span></span> <span data-ttu-id="dd91f-110">I den anden er de placeret side om side.</span><span class="sxs-lookup"><span data-stu-id="dd91f-110">On the other report, the sections are side by side.</span></span>

| <span data-ttu-id="dd91f-111">Standardrapport</span><span class="sxs-lookup"><span data-stu-id="dd91f-111">Default report</span></span>                       | <span data-ttu-id="dd91f-112">Hvad den gør</span><span class="sxs-lookup"><span data-stu-id="dd91f-112">What it does</span></span>                                                                                                                           |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd91f-113">Balance – standard</span><span class="sxs-lookup"><span data-stu-id="dd91f-113">Balance Sheet – Default</span></span>              | <span data-ttu-id="dd91f-114">Giver en oversigt over organisationens økonomiske situation for året.</span><span class="sxs-lookup"><span data-stu-id="dd91f-114">Provides a view of the organization's financial position for the year.</span></span>                                                                 |
| <span data-ttu-id="dd91f-115">Parallel balance – standard</span><span class="sxs-lookup"><span data-stu-id="dd91f-115">Side by Side Balance Sheet – Default</span></span> | <span data-ttu-id="dd91f-116">Giver en oversigt over organisationens økonomiske situation for året.</span><span class="sxs-lookup"><span data-stu-id="dd91f-116">Provides a view of the organization's financial position for the year.</span></span> <span data-ttu-id="dd91f-117">Aktiver og passiver og egenkapital ved siden af hinanden.</span><span class="sxs-lookup"><span data-stu-id="dd91f-117">Assets and liability and shareholder’s equity are side by side.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="dd91f-118">Komponenter</span><span class="sxs-lookup"><span data-stu-id="dd91f-118">Building blocks</span></span>
<span data-ttu-id="dd91f-119">Balanceregnskabsrapporter bruger følgende komponenter.</span><span class="sxs-lookup"><span data-stu-id="dd91f-119">The balance sheet financial reports use the following building blocks.</span></span>

| <span data-ttu-id="dd91f-120">Standardrapport</span><span class="sxs-lookup"><span data-stu-id="dd91f-120">Default report</span></span>                       | <span data-ttu-id="dd91f-121">Definition af række</span><span class="sxs-lookup"><span data-stu-id="dd91f-121">Row definition</span></span>                       | <span data-ttu-id="dd91f-122">Kolonnedefinition</span><span class="sxs-lookup"><span data-stu-id="dd91f-122">Column definition</span></span>             |
|--------------------------------------|--------------------------------------|-------------------------------|
| <span data-ttu-id="dd91f-123">Balance – standard</span><span class="sxs-lookup"><span data-stu-id="dd91f-123">Balance Sheet - Default</span></span>              | <span data-ttu-id="dd91f-124">Balance – standard</span><span class="sxs-lookup"><span data-stu-id="dd91f-124">Balance Sheet - Default</span></span>              | <span data-ttu-id="dd91f-125">ÅTD og afvigelse - standard</span><span class="sxs-lookup"><span data-stu-id="dd91f-125">YTD and Variance - Default</span></span>    |
| <span data-ttu-id="dd91f-126">Parallel balance – standard</span><span class="sxs-lookup"><span data-stu-id="dd91f-126">Side by Side Balance Sheet – Default</span></span> | <span data-ttu-id="dd91f-127">Parallel balance – standard</span><span class="sxs-lookup"><span data-stu-id="dd91f-127">Side by Side Balance Sheet – Default</span></span> | <span data-ttu-id="dd91f-128">År til dato-kolonne - standard</span><span class="sxs-lookup"><span data-stu-id="dd91f-128">Year to Date Column - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="dd91f-129">Definition af række</span><span class="sxs-lookup"><span data-stu-id="dd91f-129">Row definition</span></span>

<span data-ttu-id="dd91f-130">Rækkedefinitioner for begge balancerapporter indeholder sektioner for hver del af en traditionel balance.</span><span class="sxs-lookup"><span data-stu-id="dd91f-130">The row definitions for both balance sheet reports contain sections for each part of a traditional balance sheet.</span></span> <span data-ttu-id="dd91f-131">Side om side-rapporten indeholder et kolonneskift, så passiver og egenkapital vises ved siden af aktiver.</span><span class="sxs-lookup"><span data-stu-id="dd91f-131">The side-by-side report includes a column break, so that liability and the owner’s equity appear next to assets.</span></span> <span data-ttu-id="dd91f-132">Dimensionen Hovedkontokategori bruges til at oprette begge rækkedefinitioner.</span><span class="sxs-lookup"><span data-stu-id="dd91f-132">The Main Account Category dimension is used to build both row definitions.</span></span> <span data-ttu-id="dd91f-133">Derfor kan alle oprette rapporterne uden at skulle foretage ændringer.</span><span class="sxs-lookup"><span data-stu-id="dd91f-133">Therefore, anyone can generate the reports without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="dd91f-134">Kolonnedefinition</span><span class="sxs-lookup"><span data-stu-id="dd91f-134">Column definition</span></span>

<span data-ttu-id="dd91f-135">Kolonnedefinitionerne indeholder forskellige typer kolonner, der giver forskellige niveauer af detaljer og økonomiske data.</span><span class="sxs-lookup"><span data-stu-id="dd91f-135">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="dd91f-136">**ÅTD og afvigelse – standardkolonnetyper:**</span><span class="sxs-lookup"><span data-stu-id="dd91f-136">**YTD and Variance – Default column types:**</span></span>
    -   <span data-ttu-id="dd91f-137">**DESC** – En beskrivelse af rækkedefinitionen</span><span class="sxs-lookup"><span data-stu-id="dd91f-137">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="dd91f-138">**FD** – År til dato-økonomiske data for indeværende år</span><span class="sxs-lookup"><span data-stu-id="dd91f-138">**FD** – Year-to-date financial data for the current year</span></span>
    -   <span data-ttu-id="dd91f-139">**FD** – År til dato-økonomiske data for sidste år</span><span class="sxs-lookup"><span data-stu-id="dd91f-139">**FD** – Year-to-date financial data for the last year</span></span>
    -   <span data-ttu-id="dd91f-140">**BEREGN** – Afvigelsen ved at fratrække sidste år fra indeværende år</span><span class="sxs-lookup"><span data-stu-id="dd91f-140">**CALC** – The variance from subtracting last year from this year</span></span>

<!-- -->

-   <span data-ttu-id="dd91f-141">**År til dato-kolonne - standard:**</span><span class="sxs-lookup"><span data-stu-id="dd91f-141">**Year to Date Column – Default:**</span></span>
    -   <span data-ttu-id="dd91f-142">**DESC** – En beskrivelse af rækkedefinitionen</span><span class="sxs-lookup"><span data-stu-id="dd91f-142">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="dd91f-143">**FD** – År til dato-økonomiske data for indeværende år</span><span class="sxs-lookup"><span data-stu-id="dd91f-143">**FD** – Year-to-date financial data for the current year</span></span>



<a name="additional-resources"></a><span data-ttu-id="dd91f-144">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="dd91f-144">Additional resources</span></span>
--------

[<span data-ttu-id="dd91f-145">Økonomirapportering</span><span class="sxs-lookup"><span data-stu-id="dd91f-145">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="dd91f-146">Se økonomiske rapporter</span><span class="sxs-lookup"><span data-stu-id="dd91f-146">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="dd91f-147">Dynamics Financial Reporting-blog</span><span class="sxs-lookup"><span data-stu-id="dd91f-147">Dynamics Financial Reporting Blog</span></span>](https://blogs.msdn.com/b/dynamics_financial_reporting/)



