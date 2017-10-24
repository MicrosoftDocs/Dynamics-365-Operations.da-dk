---
title: Power BI-indhold til Faktisk vs. budget
description: "I dette emne beskrives Power BI-indhold til Faktisk vs. budget. Det beskrives, hvordan du får adgang til rapporter, der er inkluderet i indholdet, og indeholder oplysninger om den datamodel og de enheder, der blev brugt til at oprette indholdet."
author: ryansandness
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application user, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: afa8e07505283531c97663f35b208d82d69d2b42
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="actual-vs-budget-power-bi-content"></a><span data-ttu-id="d1e39-104">Power BI-indhold til Faktisk vs. budget</span><span class="sxs-lookup"><span data-stu-id="d1e39-104">Actual vs budget Power BI content</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d1e39-105">I dette emne beskrives Microsoft Power BI-indhold til **Faktisk vs. budget**.</span><span class="sxs-lookup"><span data-stu-id="d1e39-105">This topic describes the **Actual vs budget** Microsoft Power BI content.</span></span> <span data-ttu-id="d1e39-106">Det beskrives, hvordan du får adgang til Power BI-rapporter, og der er oplysninger om den datamodel og de enheder, der blev brugt til at oprette indholdspakken.</span><span class="sxs-lookup"><span data-stu-id="d1e39-106">It explains how to access the Power BI reports, and provides information about the data model and entities that were used to build the content.</span></span> 

# <a name="overview"></a><span data-ttu-id="d1e39-107">Overblik</span><span class="sxs-lookup"><span data-stu-id="d1e39-107">Overview</span></span>

<span data-ttu-id="d1e39-108">Power BI-indholdet til **Faktisk vs. budget** er beregnet til personer, der er ansvarlige for at overvåge performance for faktisk vs. budget i deres organisation.</span><span class="sxs-lookup"><span data-stu-id="d1e39-108">The **Actual vs budget** Power BI content was created for individuals who are responsible for monitoring actual versus budget performance in their organization.</span></span> <span data-ttu-id="d1e39-109">Power BI-indholdet til **Faktisk vs. budget** skaber synlighed i dine budgetafvigelser.</span><span class="sxs-lookup"><span data-stu-id="d1e39-109">The **Actual vs budget** Power BI content provides visibility into your budget variances.</span></span> <span data-ttu-id="d1e39-110">Du kan analysere budgettet for det indeværende år efter kontokategori, budgetkode, hovedkonto, beskrivelser af hovedkonto eller regnskabsperiode for at få en bedre forståelse af årsagen til eventuelle afvigelser.</span><span class="sxs-lookup"><span data-stu-id="d1e39-110">You can analyze budget for the current year by account category, budget code, main account, main account descriptions, or fiscal period to get a better understanding of the cause of any variances.</span></span> 

# <a name="accessing-the-power-bi-content"></a><span data-ttu-id="d1e39-111">Adgang til Power BI-indhold</span><span class="sxs-lookup"><span data-stu-id="d1e39-111">Accessing the Power BI content</span></span>
<span data-ttu-id="d1e39-112">Hvis du bruger Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (juli 2017), vises rapporter fra Power BI-indholdet til **Faktisk vs. budget** i arbejdsområderne **Finansbudgetter og budgetter** og **Regnskabsdirektør**.</span><span class="sxs-lookup"><span data-stu-id="d1e39-112">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017), reports from the **Actual vs budget** Power BI content are shown in the **Ledger budget and forecasts** and **CFO** workspaces.</span></span>

# <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="d1e39-113">Rapporter, der er inkluderet i Power BI-indholdet</span><span class="sxs-lookup"><span data-stu-id="d1e39-113">Reports that are included in the Power BI content</span></span>
<span data-ttu-id="d1e39-114">Følgende tabel indeholder oplysninger om de nøgletal, der findes på de enkelte rapportsider i Power BI-indholdet til **Faktisk vs. budget**.</span><span class="sxs-lookup"><span data-stu-id="d1e39-114">The following table provides details about the metrics that are found on each report page in the **Actual vs budget** Power BI content.</span></span>

| <span data-ttu-id="d1e39-115">Rapport</span><span class="sxs-lookup"><span data-stu-id="d1e39-115">Report</span></span>                      | <span data-ttu-id="d1e39-116">Metrik</span><span class="sxs-lookup"><span data-stu-id="d1e39-116">Metrics</span></span> |
|-----------------------------|---------|
| <span data-ttu-id="d1e39-117">Udgifter - Faktisk vs. budget</span><span class="sxs-lookup"><span data-stu-id="d1e39-117">Expenses - Actual vs budget</span></span> | <ul><li><span data-ttu-id="d1e39-118">Samlede udgifter i år</span><span class="sxs-lookup"><span data-stu-id="d1e39-118">Total expenses this year</span></span></li><li><span data-ttu-id="d1e39-119">Budgetterede samlede udgifter i år</span><span class="sxs-lookup"><span data-stu-id="d1e39-119">Budget total expenses this year</span></span></li></ul> |
| <span data-ttu-id="d1e39-120">Indtægt - Faktisk vs. budget</span><span class="sxs-lookup"><span data-stu-id="d1e39-120">Revenue - Actual vs budget</span></span>  | <ul><li><span data-ttu-id="d1e39-121">Samlet omsætning i år</span><span class="sxs-lookup"><span data-stu-id="d1e39-121">Total revenue this year</span></span></li><li><span data-ttu-id="d1e39-122">Samlet budgetteret omsætning i år</span><span class="sxs-lookup"><span data-stu-id="d1e39-122">Budget total revenue this year</span></span></li><ul> |
| <span data-ttu-id="d1e39-123">Udgift</span><span class="sxs-lookup"><span data-stu-id="d1e39-123">Expense</span></span>                     | <ul><li><span data-ttu-id="d1e39-124">Samlede udgifter i år</span><span class="sxs-lookup"><span data-stu-id="d1e39-124">Total expenses this year</span></span></li><li><span data-ttu-id="d1e39-125">Mål for udgifter baseret på budget</span><span class="sxs-lookup"><span data-stu-id="d1e39-125">Goal for expenses based on budget</span></span> </li><ul> |
| <span data-ttu-id="d1e39-126">Indtægter</span><span class="sxs-lookup"><span data-stu-id="d1e39-126">Revenue</span></span>                     | <ul><li><span data-ttu-id="d1e39-127">Samlet omsætning i år</span><span class="sxs-lookup"><span data-stu-id="d1e39-127">Total revenue this year</span></span></li><li><span data-ttu-id="d1e39-128">Mål for indtægter baseret på budget</span><span class="sxs-lookup"><span data-stu-id="d1e39-128">Goal for revenue based on budget</span></span> </li><ul> |
| <span data-ttu-id="d1e39-129">Nettoresultat</span><span class="sxs-lookup"><span data-stu-id="d1e39-129">Net income</span></span>                  | <ul><li><span data-ttu-id="d1e39-130">Nettoresultat i år</span><span class="sxs-lookup"><span data-stu-id="d1e39-130">Net income this year</span></span></li><li><span data-ttu-id="d1e39-131">Mål for nettoindkomst baseret på budget</span><span class="sxs-lookup"><span data-stu-id="d1e39-131">Goal for net income based on budget</span></span> </li><ul> |

## <a name="extending-the-power-bi-content"></a><span data-ttu-id="d1e39-132">Udvidelse af Power BI-indhold</span><span class="sxs-lookup"><span data-stu-id="d1e39-132">Extending the Power BI content</span></span>
<span data-ttu-id="d1e39-133">Når du bruger de indholdspakker, der er tilgængelige i Microsoft Dynamics Lifecycle Services (LCS), kan du levere fremragende analyser til personer, der ikke logger på Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="d1e39-133">By using the content packs that are available in Microsoft Dynamics Lifecycle Services (LCS), you can provide great analytics to people who don't sign in to Microsoft Dynamics 365.</span></span> <span data-ttu-id="d1e39-134">Du kan redigere disse indholdspakker, så de omfatter andre rapporter eller grafik, og derefter udgive indholdspakkerne på din Power BI.com-lejer med henblik på analyse.</span><span class="sxs-lookup"><span data-stu-id="d1e39-134">You can modify these content packs so that they include other reports or visuals, and then publish the content packs to your Power BI.com tenant for analysis.</span></span> 

<span data-ttu-id="d1e39-135">Du kan finde Power BI-indholdet til **Faktisk vs. budget** i biblioteket med delte aktiver i LCS.</span><span class="sxs-lookup"><span data-stu-id="d1e39-135">You can find the **Actual vs budget** Power BI content in the Shared assets library in LCS.</span></span> <span data-ttu-id="d1e39-136">Du kan finde flere oplysninger om, hvordan du downloader indhold og implementerer det i din organisation, under [Power BI-indhold i LCS fra Microsoft og dine partnere](power-bi-content-microsoft-partners.md).</span><span class="sxs-lookup"><span data-stu-id="d1e39-136">For more information about how to download the content and implement it in your organization, see [Power BI content in LCS from Microsoft and your partners](power-bi-content-microsoft-partners.md).</span></span> <span data-ttu-id="d1e39-137">Hvis du vil se en demo, der viser, hvordan du implementerer Power BI-indholdet, kan du se dette Office Mix [Power BI-indhold fra Microsoft og dine partnere i Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w).</span><span class="sxs-lookup"><span data-stu-id="d1e39-137">To watch a demo that shows how to implement the Power BI content, see the [Power BI content from Microsoft and your partners in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix.</span></span>

# <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="d1e39-138">Forståelse af datamodellen og enheder</span><span class="sxs-lookup"><span data-stu-id="d1e39-138">Understanding the data model and entities</span></span>

| <span data-ttu-id="d1e39-139">Enhed</span><span class="sxs-lookup"><span data-stu-id="d1e39-139">Entity</span></span>                    | <span data-ttu-id="d1e39-140">Indhold</span><span class="sxs-lookup"><span data-stu-id="d1e39-140">Contents</span></span> |
|---------------------------|----------|
| <span data-ttu-id="d1e39-141">Finansaktiviteter</span><span class="sxs-lookup"><span data-stu-id="d1e39-141">General Ledger Activities</span></span> | <span data-ttu-id="d1e39-142">Transaktionsbeløb for Finans</span><span class="sxs-lookup"><span data-stu-id="d1e39-142">Transaction amounts for the general ledger</span></span> |
| <span data-ttu-id="d1e39-143">Budgetaktiviteter</span><span class="sxs-lookup"><span data-stu-id="d1e39-143">Budget Activities</span></span>         | <span data-ttu-id="d1e39-144">Transaktionsbeløb for budgetregisteret</span><span class="sxs-lookup"><span data-stu-id="d1e39-144">Transaction amounts for the budget register</span></span> |
| <span data-ttu-id="d1e39-145">Hovedkonti</span><span class="sxs-lookup"><span data-stu-id="d1e39-145">Main Accounts</span></span>             | <span data-ttu-id="d1e39-146">Hovedkonti til at filtrere rapporter efter</span><span class="sxs-lookup"><span data-stu-id="d1e39-146">Main accounts to filter reports by</span></span> |
| <span data-ttu-id="d1e39-147">Regnskabskalendere</span><span class="sxs-lookup"><span data-stu-id="d1e39-147">Fiscal Calendars</span></span>          | <span data-ttu-id="d1e39-148">Regnskabskalendere til at filtrere rapporter efter</span><span class="sxs-lookup"><span data-stu-id="d1e39-148">Fiscal calendars to filter reports by</span></span> |
| <span data-ttu-id="d1e39-149">Finans</span><span class="sxs-lookup"><span data-stu-id="d1e39-149">Ledgers</span></span>                   | <span data-ttu-id="d1e39-150">Finanskonti, der kan bruges til at filtrere rapporten til det aktuelle finansmodul</span><span class="sxs-lookup"><span data-stu-id="d1e39-150">Ledgers that can be used to filter the report to the current ledger</span></span> |
| <span data-ttu-id="d1e39-151">Budgetkoder</span><span class="sxs-lookup"><span data-stu-id="d1e39-151">Budget Codes</span></span>              | <span data-ttu-id="d1e39-152">Budgetkoder, som rapporter kan filtreres efter</span><span class="sxs-lookup"><span data-stu-id="d1e39-152">Budget codes to filter reports by</span></span> |
| <span data-ttu-id="d1e39-153">Juridiske enheder</span><span class="sxs-lookup"><span data-stu-id="d1e39-153">Legal Entities</span></span>            | <span data-ttu-id="d1e39-154">Juridiske enheder, der kan bruges til at filtrere rapporten til den aktuelle juridisk enhed</span><span class="sxs-lookup"><span data-stu-id="d1e39-154">Legal entities that can be used to filter the report to the current legal entity</span></span> |

