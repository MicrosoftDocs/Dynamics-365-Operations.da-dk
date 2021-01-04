---
title: Regnskabsrapport over resultatopgørelse
description: I denne artikel beskrives standardrapporten til resultatopgørelser. Her beskrives også de komponenter, der er knyttet til denne rapport.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 429283865c66ca5f03608e4a02c3aba5bb5ea7e3
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645571"
---
# <a name="income-statement-financial-report"></a><span data-ttu-id="ee588-104">Regnskabsrapport over resultatopgørelse</span><span class="sxs-lookup"><span data-stu-id="ee588-104">Income statement financial report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ee588-105">I denne artikel beskrives standardrapporten til resultatopgørelser.</span><span class="sxs-lookup"><span data-stu-id="ee588-105">This article describes the default report for income statements.</span></span> <span data-ttu-id="ee588-106">Her beskrives også de komponenter, der er knyttet til denne rapport.</span><span class="sxs-lookup"><span data-stu-id="ee588-106">It also describes the building blocks that are associated with this report.</span></span> 

<a name="default-income-statement-report"></a><span data-ttu-id="ee588-107">Standardrapport over resultatopgørelse</span><span class="sxs-lookup"><span data-stu-id="ee588-107">Default income statement report</span></span>
-------------------------------

| <span data-ttu-id="ee588-108">Standardrapport</span><span class="sxs-lookup"><span data-stu-id="ee588-108">Default report</span></span>             | <span data-ttu-id="ee588-109">Hvad den gør</span><span class="sxs-lookup"><span data-stu-id="ee588-109">What it does</span></span>                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee588-110">Resultatopgørelse – standard</span><span class="sxs-lookup"><span data-stu-id="ee588-110">Income Statement – Default</span></span> | <span data-ttu-id="ee588-111">Viser organisationens rentabilitet for den aktuelle periode og også for år til dato.</span><span class="sxs-lookup"><span data-stu-id="ee588-111">Provides a view of the organization’s profitability for the current period and also for the year to date.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="ee588-112">Komponenter</span><span class="sxs-lookup"><span data-stu-id="ee588-112">Building blocks</span></span>
<span data-ttu-id="ee588-113">Regnskabsrapporten over resultatopgørelse bruger følgende komponenter.</span><span class="sxs-lookup"><span data-stu-id="ee588-113">The income statement financial report uses the following building blocks.</span></span>

| <span data-ttu-id="ee588-114">Standardrapport</span><span class="sxs-lookup"><span data-stu-id="ee588-114">Default report</span></span>             | <span data-ttu-id="ee588-115">Definition af række</span><span class="sxs-lookup"><span data-stu-id="ee588-115">Row definition</span></span>                     | <span data-ttu-id="ee588-116">Kolonnedefinition</span><span class="sxs-lookup"><span data-stu-id="ee588-116">Column definition</span></span>          |
|----------------------------|------------------------------------|----------------------------|
| <span data-ttu-id="ee588-117">Resultatopgørelse – standard</span><span class="sxs-lookup"><span data-stu-id="ee588-117">Income Statement - Default</span></span> | <span data-ttu-id="ee588-118">Oversigt over resultatopgørelse – standard</span><span class="sxs-lookup"><span data-stu-id="ee588-118">Summary Income Statement - Default</span></span> | <span data-ttu-id="ee588-119">Periodisk og ÅTD -standard.</span><span class="sxs-lookup"><span data-stu-id="ee588-119">Periodic and YTD - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="ee588-120">Definition af række</span><span class="sxs-lookup"><span data-stu-id="ee588-120">Row definition</span></span>

<span data-ttu-id="ee588-121">Rækkedefinitionen, oversigt over resultatopgørelse – standard indeholder et afsnit for hver del af en traditionel resultatopgørelse.</span><span class="sxs-lookup"><span data-stu-id="ee588-121">The row definition, Summary Income Statement – Default, contains a section for each part of a traditional income statement.</span></span> <span data-ttu-id="ee588-122">Dimensionen Hovedkontokategori bruges til at oprette denne rækkedefinition.</span><span class="sxs-lookup"><span data-stu-id="ee588-122">The Main Account Category dimension is used to build this row definition.</span></span> <span data-ttu-id="ee588-123">Derfor kan alle oprette rapporten uden at skulle foretage ændringer.</span><span class="sxs-lookup"><span data-stu-id="ee588-123">Therefore, anyone can generate the report without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="ee588-124">Kolonnedefinition</span><span class="sxs-lookup"><span data-stu-id="ee588-124">Column Definition</span></span>

<span data-ttu-id="ee588-125">Kolonnedefinitionerne indeholder forskellige typer kolonner, der giver forskellige niveauer af detaljer og økonomiske data.</span><span class="sxs-lookup"><span data-stu-id="ee588-125">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="ee588-126">**Periodisk og ÅTD – standardkolonnetyper:**</span><span class="sxs-lookup"><span data-stu-id="ee588-126">**Periodic and YTD – Default column types:**</span></span>
    -   <span data-ttu-id="ee588-127">**DESC** – En beskrivelse af rækkedefinitionen</span><span class="sxs-lookup"><span data-stu-id="ee588-127">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="ee588-128">**FD** – Økonomiske data for den aktuelle periode</span><span class="sxs-lookup"><span data-stu-id="ee588-128">**FD** – Financial data for the current period</span></span>
    -   <span data-ttu-id="ee588-129">**FD** – Økonomiske data for år til dato</span><span class="sxs-lookup"><span data-stu-id="ee588-129">**FD** – Financial data for the year to date</span></span>



<a name="additional-resources"></a><span data-ttu-id="ee588-130">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="ee588-130">Additional resources</span></span>
--------

[<span data-ttu-id="ee588-131">Oversigt over økonomirapportering</span><span class="sxs-lookup"><span data-stu-id="ee588-131">Financial reporting overview</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="ee588-132">Vise økonomirapporter</span><span class="sxs-lookup"><span data-stu-id="ee588-132">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="ee588-133">Dynamics Financial Reporting-blog</span><span class="sxs-lookup"><span data-stu-id="ee588-133">Dynamics Financial Reporting Blog</span></span>](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog)



