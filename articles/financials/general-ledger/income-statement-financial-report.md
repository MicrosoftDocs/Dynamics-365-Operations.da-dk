---
title: "Regnskabsrapport over resultatopgørelse"
description: "I denne artikel beskrives standardrapporten til resultatopgørelser. Her beskrives også de komponenter, der er knyttet til denne rapport."
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0017d13b7f7594462dfff4ef896f4139607d4bc5
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="income-statement-financial-report"></a><span data-ttu-id="75549-104">Regnskabsrapport over resultatopgørelse</span><span class="sxs-lookup"><span data-stu-id="75549-104">Income statement financial report</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="75549-105">I denne artikel beskrives standardrapporten til resultatopgørelser.</span><span class="sxs-lookup"><span data-stu-id="75549-105">This article describes the default report for income statements.</span></span> <span data-ttu-id="75549-106">Her beskrives også de komponenter, der er knyttet til denne rapport.</span><span class="sxs-lookup"><span data-stu-id="75549-106">It also describes the building blocks that are associated with this report.</span></span> 

<a name="default-income-statement-report"></a><span data-ttu-id="75549-107">Standardrapport over resultatopgørelse</span><span class="sxs-lookup"><span data-stu-id="75549-107">Default income statement report</span></span>
-------------------------------

| <span data-ttu-id="75549-108">Standardrapport</span><span class="sxs-lookup"><span data-stu-id="75549-108">Default report</span></span>             | <span data-ttu-id="75549-109">Hvad den gør</span><span class="sxs-lookup"><span data-stu-id="75549-109">What it does</span></span>                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75549-110">Resultatopgørelse – standard</span><span class="sxs-lookup"><span data-stu-id="75549-110">Income Statement – Default</span></span> | <span data-ttu-id="75549-111">Viser organisationens rentabilitet for den aktuelle periode og også for år til dato.</span><span class="sxs-lookup"><span data-stu-id="75549-111">Provides a view of the organization’s profitability for the current period and also for the year to date.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="75549-112">Komponenter</span><span class="sxs-lookup"><span data-stu-id="75549-112">Building blocks</span></span>
<span data-ttu-id="75549-113">Regnskabsrapporten over resultatopgørelse bruger følgende komponenter.</span><span class="sxs-lookup"><span data-stu-id="75549-113">The income statement financial report uses the following building blocks.</span></span>

| <span data-ttu-id="75549-114">Standardrapport</span><span class="sxs-lookup"><span data-stu-id="75549-114">Default report</span></span>             | <span data-ttu-id="75549-115">Definition af række</span><span class="sxs-lookup"><span data-stu-id="75549-115">Row definition</span></span>                     | <span data-ttu-id="75549-116">Kolonnedefinition</span><span class="sxs-lookup"><span data-stu-id="75549-116">Column definition</span></span>          |
|----------------------------|------------------------------------|----------------------------|
| <span data-ttu-id="75549-117">Resultatopgørelse – standard</span><span class="sxs-lookup"><span data-stu-id="75549-117">Income Statement - Default</span></span> | <span data-ttu-id="75549-118">Oversigt over resultatopgørelse – standard</span><span class="sxs-lookup"><span data-stu-id="75549-118">Summary Income Statement - Default</span></span> | <span data-ttu-id="75549-119">Periodisk og ÅTD -standard.</span><span class="sxs-lookup"><span data-stu-id="75549-119">Periodic and YTD - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="75549-120">Definition af række</span><span class="sxs-lookup"><span data-stu-id="75549-120">Row definition</span></span>

<span data-ttu-id="75549-121">Rækkedefinitionen, oversigt over resultatopgørelse – standard indeholder et afsnit for hver del af en traditionel resultatopgørelse.</span><span class="sxs-lookup"><span data-stu-id="75549-121">The row definition, Summary Income Statement – Default, contains a section for each part of a traditional income statement.</span></span> <span data-ttu-id="75549-122">Dimensionen Hovedkontokategori bruges til at oprette denne rækkedefinition.</span><span class="sxs-lookup"><span data-stu-id="75549-122">The Main Account Category dimension is used to build this row definition.</span></span> <span data-ttu-id="75549-123">Derfor kan alle oprette rapporten uden at skulle foretage ændringer.</span><span class="sxs-lookup"><span data-stu-id="75549-123">Therefore, anyone can generate the report without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="75549-124">Kolonnedefinition</span><span class="sxs-lookup"><span data-stu-id="75549-124">Column Definition</span></span>

<span data-ttu-id="75549-125">Kolonnedefinitionerne indeholder forskellige typer kolonner, der giver forskellige niveauer af detaljer og økonomiske data.</span><span class="sxs-lookup"><span data-stu-id="75549-125">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="75549-126">**Periodisk og ÅTD – standardkolonnetyper:**</span><span class="sxs-lookup"><span data-stu-id="75549-126">**Periodic and YTD – Default column types:**</span></span>
    -   <span data-ttu-id="75549-127">**DESC** – En beskrivelse af rækkedefinitionen</span><span class="sxs-lookup"><span data-stu-id="75549-127">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="75549-128">**FD** – Økonomiske data for den aktuelle periode</span><span class="sxs-lookup"><span data-stu-id="75549-128">**FD** – Financial data for the current period</span></span>
    -   <span data-ttu-id="75549-129">**FD** – Økonomiske data for år til dato</span><span class="sxs-lookup"><span data-stu-id="75549-129">**FD** – Financial data for the year to date</span></span>

 

<a name="see-also"></a><span data-ttu-id="75549-130">Se også</span><span class="sxs-lookup"><span data-stu-id="75549-130">See also</span></span>
--------

[<span data-ttu-id="75549-131">Økonomirapportering</span><span class="sxs-lookup"><span data-stu-id="75549-131">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="75549-132">Se økonomiske rapporter</span><span class="sxs-lookup"><span data-stu-id="75549-132">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="75549-133">Dynamics Financial Reporting-blog</span><span class="sxs-lookup"><span data-stu-id="75549-133">Dynamics Financial Reporting Blog</span></span>](http://blogs.msdn.com/b/dynamics_financial_reporting/)




