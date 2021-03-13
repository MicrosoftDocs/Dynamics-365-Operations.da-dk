---
title: Power BI-indhold til Faktisk vs. budget
description: I dette emne beskrives Power BI-indhold til Faktisk vs. budget. Det forklarer, hvordan du får adgang til rapporterne, og giver oplysninger om datamodellen.
author: panolte
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetTrackingWorkspace
audience: Application user, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 908b96af5b3d67f265953648edd6aa7ec31556a4
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093842"
---
# <a name="actual-vs-budget-power-bi-content"></a><span data-ttu-id="4d20f-104">Power BI-indhold til Faktisk vs. budget</span><span class="sxs-lookup"><span data-stu-id="4d20f-104">Actual vs budget Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4d20f-105">I dette emne beskrives Power BI-indhold til **Faktisk vs. budget**.</span><span class="sxs-lookup"><span data-stu-id="4d20f-105">This topic describes the **Actual vs budget** Microsoft Power BI content.</span></span> <span data-ttu-id="4d20f-106">Det beskrives, hvordan du får adgang til Power BI-rapporter, og der er oplysninger om den datamodel og de enheder, der blev brugt til at oprette indholdspakken.</span><span class="sxs-lookup"><span data-stu-id="4d20f-106">It explains how to access the Power BI reports, and provides information about the data model and entities that were used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="4d20f-107">Overblik</span><span class="sxs-lookup"><span data-stu-id="4d20f-107">Overview</span></span>

<span data-ttu-id="4d20f-108">Power BI-indholdet til **Faktisk vs. budget** er beregnet til personer, der er ansvarlige for at overvåge performance for faktisk vs. budget i deres organisation.</span><span class="sxs-lookup"><span data-stu-id="4d20f-108">The **Actual vs budget** Power BI content was created for individuals who are responsible for monitoring actual versus budget performance in their organization.</span></span> <span data-ttu-id="4d20f-109">Power BI-indholdet til **Faktisk vs. budget** skaber synlighed i dine budgetafvigelser.</span><span class="sxs-lookup"><span data-stu-id="4d20f-109">The **Actual vs budget** Power BI content provides visibility into your budget variances.</span></span> <span data-ttu-id="4d20f-110">Du kan analysere budgettet for det indeværende år efter kontokategori, budgetkode, hovedkonto, beskrivelser af hovedkonto eller regnskabsperiode for at få en bedre forståelse af årsagen til eventuelle afvigelser.</span><span class="sxs-lookup"><span data-stu-id="4d20f-110">You can analyze budget for the current year by account category, budget code, main account, main account descriptions, or fiscal period to get a better understanding of the cause of any variances.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="4d20f-111">Adgang til Power BI-indholdet</span><span class="sxs-lookup"><span data-stu-id="4d20f-111">Accessing the Power BI content</span></span>
<span data-ttu-id="4d20f-112">Rapporter fra Power BI-indholdet **Faktisk vs. budget** vises i arbejdsområderne **Finansbudgetter og budgetter** og **Regnskabsdirektør**.</span><span class="sxs-lookup"><span data-stu-id="4d20f-112">Reports from the **Actual vs budget** Power BI content are shown in the **Ledger budget and forecasts** and **CFO** workspaces.</span></span>

## <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="4d20f-113">Rapporter, der er inkluderet i Power BI-indholdet</span><span class="sxs-lookup"><span data-stu-id="4d20f-113">Reports that are included in the Power BI content</span></span>
<span data-ttu-id="4d20f-114">Følgende tabel indeholder oplysninger om de nøgletal, der findes på de enkelte rapportsider i Power BI-indholdet til **Faktisk vs. budget**.</span><span class="sxs-lookup"><span data-stu-id="4d20f-114">The following table provides details about the metrics that are found on each report page in the **Actual vs budget** Power BI content.</span></span>

| <span data-ttu-id="4d20f-115">Rapport</span><span class="sxs-lookup"><span data-stu-id="4d20f-115">Report</span></span>                      | <span data-ttu-id="4d20f-116">Metrik</span><span class="sxs-lookup"><span data-stu-id="4d20f-116">Metrics</span></span>                                                                             |
|-----------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4d20f-117">Udgifter - Faktisk vs. budget</span><span class="sxs-lookup"><span data-stu-id="4d20f-117">Expenses - Actual vs budget</span></span> | <ul><li><span data-ttu-id="4d20f-118">Samlede udgifter i år</span><span class="sxs-lookup"><span data-stu-id="4d20f-118">Total expenses this year</span></span></li><li><span data-ttu-id="4d20f-119">Budgetterede samlede udgifter i år</span><span class="sxs-lookup"><span data-stu-id="4d20f-119">Budget total expenses this year</span></span></li></ul>  |
| <span data-ttu-id="4d20f-120">Indtægt - Faktisk vs. budget</span><span class="sxs-lookup"><span data-stu-id="4d20f-120">Revenue - Actual vs budget</span></span>  | <ul><li><span data-ttu-id="4d20f-121">Samlet omsætning i år</span><span class="sxs-lookup"><span data-stu-id="4d20f-121">Total revenue this year</span></span></li><li><span data-ttu-id="4d20f-122">Samlet budgetteret omsætning i år</span><span class="sxs-lookup"><span data-stu-id="4d20f-122">Budget total revenue this year</span></span></li><ul>     |
| <span data-ttu-id="4d20f-123">Udgift</span><span class="sxs-lookup"><span data-stu-id="4d20f-123">Expense</span></span>                     | <ul><li><span data-ttu-id="4d20f-124">Samlede udgifter i år</span><span class="sxs-lookup"><span data-stu-id="4d20f-124">Total expenses this year</span></span></li><li><span data-ttu-id="4d20f-125">Mål for udgifter baseret på budget</span><span class="sxs-lookup"><span data-stu-id="4d20f-125">Goal for expenses based on budget</span></span></li><ul> |
| <span data-ttu-id="4d20f-126">Indtægter</span><span class="sxs-lookup"><span data-stu-id="4d20f-126">Revenue</span></span>                     | <ul><li><span data-ttu-id="4d20f-127">Samlet omsætning i år</span><span class="sxs-lookup"><span data-stu-id="4d20f-127">Total revenue this year</span></span></li><li><span data-ttu-id="4d20f-128">Mål for indtægter baseret på budget</span><span class="sxs-lookup"><span data-stu-id="4d20f-128">Goal for revenue based on budget</span></span></li><ul>   |
| <span data-ttu-id="4d20f-129">Nettoresultat</span><span class="sxs-lookup"><span data-stu-id="4d20f-129">Net income</span></span>                  | <ul><li><span data-ttu-id="4d20f-130">Nettoresultat i år</span><span class="sxs-lookup"><span data-stu-id="4d20f-130">Net income this year</span></span></li><li><span data-ttu-id="4d20f-131">Mål for nettoindkomst baseret på budget</span><span class="sxs-lookup"><span data-stu-id="4d20f-131">Goal for net income based on budget</span></span></li><ul>   |

## <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="4d20f-132">Forståelse af datamodellen og enheder</span><span class="sxs-lookup"><span data-stu-id="4d20f-132">Understanding the data model and entities</span></span>

| <span data-ttu-id="4d20f-133">Enhed</span><span class="sxs-lookup"><span data-stu-id="4d20f-133">Entity</span></span>                    | <span data-ttu-id="4d20f-134">Indhold</span><span class="sxs-lookup"><span data-stu-id="4d20f-134">Contents</span></span>                                                                         |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4d20f-135">Finansaktiviteter</span><span class="sxs-lookup"><span data-stu-id="4d20f-135">General Ledger Activities</span></span> | <span data-ttu-id="4d20f-136">Transaktionsbeløb for Finans</span><span class="sxs-lookup"><span data-stu-id="4d20f-136">Transaction amounts for the general ledger</span></span>                                       |
| <span data-ttu-id="4d20f-137">Budgetaktiviteter</span><span class="sxs-lookup"><span data-stu-id="4d20f-137">Budget Activities</span></span>         | <span data-ttu-id="4d20f-138">Transaktionsbeløb for budgetregisteret</span><span class="sxs-lookup"><span data-stu-id="4d20f-138">Transaction amounts for the budget register</span></span>                                      |
| <span data-ttu-id="4d20f-139">Hovedkonti</span><span class="sxs-lookup"><span data-stu-id="4d20f-139">Main Accounts</span></span>             | <span data-ttu-id="4d20f-140">Hovedkonti til at filtrere rapporter efter</span><span class="sxs-lookup"><span data-stu-id="4d20f-140">Main accounts to filter reports by</span></span>                                               |
| <span data-ttu-id="4d20f-141">Regnskabskalendere</span><span class="sxs-lookup"><span data-stu-id="4d20f-141">Fiscal Calendars</span></span>          | <span data-ttu-id="4d20f-142">Regnskabskalendere til at filtrere rapporter efter</span><span class="sxs-lookup"><span data-stu-id="4d20f-142">Fiscal calendars to filter reports by</span></span>                                            |
| <span data-ttu-id="4d20f-143">Finans</span><span class="sxs-lookup"><span data-stu-id="4d20f-143">Ledgers</span></span>                   | <span data-ttu-id="4d20f-144">Finanskonti, der kan bruges til at filtrere rapporten til det aktuelle finansmodul</span><span class="sxs-lookup"><span data-stu-id="4d20f-144">Ledgers that can be used to filter the report to the current ledger</span></span>              |
| <span data-ttu-id="4d20f-145">Budgetkoder</span><span class="sxs-lookup"><span data-stu-id="4d20f-145">Budget Codes</span></span>              | <span data-ttu-id="4d20f-146">Budgetkoder, som rapporter kan filtreres efter</span><span class="sxs-lookup"><span data-stu-id="4d20f-146">Budget codes to filter reports by</span></span>                                                |
| <span data-ttu-id="4d20f-147">Juridiske enheder</span><span class="sxs-lookup"><span data-stu-id="4d20f-147">Legal Entities</span></span>            | <span data-ttu-id="4d20f-148">Juridiske enheder, der kan bruges til at filtrere rapporten til den aktuelle juridisk enhed</span><span class="sxs-lookup"><span data-stu-id="4d20f-148">Legal entities that can be used to filter the report to the current legal entity</span></span> |
