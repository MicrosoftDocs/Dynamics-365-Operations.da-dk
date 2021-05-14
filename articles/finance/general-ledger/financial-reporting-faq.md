---
title: Ofte stillede spørgsmål vedrørende Økonomirapportering
description: Dette emne indeholder en oversigt over spørgsmål vedrørende økonomirapportering, som andre brugere har haft.
author: jiwo
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 023354b0e2973f63411bf81cbeb0344333c49112
ms.sourcegitcommit: d63e7e0593084a61362a6cad3937b1fd956c384f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923019"
---
# <a name="financial-reporting-faq"></a><span data-ttu-id="e9b93-103">Ofte stillede spørgsmål vedrørende Økonomirapportering</span><span class="sxs-lookup"><span data-stu-id="e9b93-103">Financial reporting FAQ</span></span> 

<span data-ttu-id="e9b93-104">Dette emne indeholder svar på ofte stillede spørgsmål om økonomirapportering.</span><span class="sxs-lookup"><span data-stu-id="e9b93-104">This topic provides answers to frequently asked questions about financial reporting.</span></span> 

## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a><span data-ttu-id="e9b93-105">Hvordan begrænser jeg adgangen til en rapport ved hjælp af sikkerhedstræet?</span><span class="sxs-lookup"><span data-stu-id="e9b93-105">How do I restrict access to a report using tree security?</span></span>

<span data-ttu-id="e9b93-106">I følgende eksempel vises, hvordan du kan begrænse adgangen til en rapport ved hjælp af sikkerhedstræet.</span><span class="sxs-lookup"><span data-stu-id="e9b93-106">The following example shows how to restrict access to a report using tree security.</span></span>

<span data-ttu-id="e9b93-107">USMF-demofirmaet har en finansbalancerapport, som ikke alle brugere af økonomirapportering bør have adgang til.</span><span class="sxs-lookup"><span data-stu-id="e9b93-107">The USMF demo company has a Balance sheet report that not all Financial reporting users should have access to.</span></span> <span data-ttu-id="e9b93-108">Til at begrænse adgangen kan du bruge sikkerhedstræet til at begrænse adgangen til en enkelt rapport, så kun bestemte brugere kan få adgang til rapporten.</span><span class="sxs-lookup"><span data-stu-id="e9b93-108">To restrict access, you can use tree security to restrict access to a single report so that only certain users can access the report.</span></span> <span data-ttu-id="e9b93-109">Benyt følgende fremgangsmåde for at begrænse adgangen:</span><span class="sxs-lookup"><span data-stu-id="e9b93-109">Follow these steps to restrict access:</span></span> 

1. <span data-ttu-id="e9b93-110">Log på Financial Reporter Report Designer.</span><span class="sxs-lookup"><span data-stu-id="e9b93-110">Sign in to Financial Reporter Report Designer.</span></span>
2. <span data-ttu-id="e9b93-111">Opret en ny trædefinition.</span><span class="sxs-lookup"><span data-stu-id="e9b93-111">Create a new tree definition.</span></span> <span data-ttu-id="e9b93-112">Gå til **Fil > Ny > Trædefinition**.</span><span class="sxs-lookup"><span data-stu-id="e9b93-112">Go to **File > New > Tree Definition**.</span></span>
3. <span data-ttu-id="e9b93-113">Dobbeltklik på linjen **Oversigt** i kolonnen **Enhedssikkerhed**.</span><span class="sxs-lookup"><span data-stu-id="e9b93-113">Double-click the **Summary** line in the **Unit Security** column.</span></span>
4. <span data-ttu-id="e9b93-114">Vælg **Brugere og Grupper**.</span><span class="sxs-lookup"><span data-stu-id="e9b93-114">Select **Users and Groups**.</span></span>  
5. <span data-ttu-id="e9b93-115">Vælg de brugere eller grupper, som har behov for at have adgang til denne rapport.</span><span class="sxs-lookup"><span data-stu-id="e9b93-115">Select the users or groups that need access to this report.</span></span> 
6. <span data-ttu-id="e9b93-116">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="e9b93-116">Select **Save**.</span></span>
7. <span data-ttu-id="e9b93-117">Tilføj den nye trædefinition i rapportdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="e9b93-117">In the report definition, add your new tree definition.</span></span>
8. <span data-ttu-id="e9b93-118">Vælg **Indstilling** i trædefinitionen.</span><span class="sxs-lookup"><span data-stu-id="e9b93-118">In the tree definition, select **Setting**.</span></span> <span data-ttu-id="e9b93-119">Vælg **Medtag alle enheder** under **Valg af rapporteringsenhed**.</span><span class="sxs-lookup"><span data-stu-id="e9b93-119">Under **Reporting unit selection**, select **Include all units**.</span></span>

## <a name="how-do-i-identify-which-accounts-do-not-match-my-balances"></a><span data-ttu-id="e9b93-120">Hvordan identificerer jeg, hvilke konti der ikke svarer til mine saldi?</span><span class="sxs-lookup"><span data-stu-id="e9b93-120">How do I identify which accounts do not match my balances?</span></span>

<span data-ttu-id="e9b93-121">Når du har en rapport, der ikke har tilsvarende saldi, kan du gøre følgende for at identificere hver af kontiene og afvigelserne.</span><span class="sxs-lookup"><span data-stu-id="e9b93-121">If you have a report that doesn't have matching balances, here are some steps you can take to identify each of the accounts and variances.</span></span> 

<span data-ttu-id="e9b93-122">**Financial Reporter Report Designer**</span><span class="sxs-lookup"><span data-stu-id="e9b93-122">**Financial Reporter Report Designer**</span></span>
1. <span data-ttu-id="e9b93-123">I Financial Reporter Report Designer skal du oprette en ny rækkedefinition.</span><span class="sxs-lookup"><span data-stu-id="e9b93-123">In Financial Reporter Report Designer, create a new row definition.</span></span> 
2. <span data-ttu-id="e9b93-124">Vælg **Rediger > Indsæt rækker fra dimensioner**.</span><span class="sxs-lookup"><span data-stu-id="e9b93-124">Select **Edit > Insert Rows from Dimensions**.</span></span>
3. <span data-ttu-id="e9b93-125">Vælg **MainAccount**.</span><span class="sxs-lookup"><span data-stu-id="e9b93-125">Select **MainAccount**.</span></span>  
4. <span data-ttu-id="e9b93-126">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="e9b93-126">Select **OK**.</span></span>
5. <span data-ttu-id="e9b93-127">Gem rækkedefinitionen.</span><span class="sxs-lookup"><span data-stu-id="e9b93-127">Save the row definition.</span></span>
6. <span data-ttu-id="e9b93-128">Opret en ny kolonnedefinition</span><span class="sxs-lookup"><span data-stu-id="e9b93-128">Create a new column definition</span></span>
7. <span data-ttu-id="e9b93-129">Opret en ny rapportdefinition.</span><span class="sxs-lookup"><span data-stu-id="e9b93-129">Create a new report definition.</span></span>
8. <span data-ttu-id="e9b93-130">Vælg **Indstillinger**, og fjern markering af denne indstilling.</span><span class="sxs-lookup"><span data-stu-id="e9b93-130">Select **Settings** and unmark this option.</span></span>  
9. <span data-ttu-id="e9b93-131">Opret rapporten.</span><span class="sxs-lookup"><span data-stu-id="e9b93-131">Generate the report.</span></span> 
10. <span data-ttu-id="e9b93-132">Eksporter rapporten til Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="e9b93-132">Export the report to Microsoft Excel.</span></span>

<span data-ttu-id="e9b93-133">**Dynamics 365 Finance**</span><span class="sxs-lookup"><span data-stu-id="e9b93-133">**Dynamics 365 Finance**</span></span> 
1. <span data-ttu-id="e9b93-134">I Dynamics 365 Finance skal du gå til **Finans > Forespørgsler og rapporter > Råbalance**.</span><span class="sxs-lookup"><span data-stu-id="e9b93-134">In Dynamics 365 Finance, go to **General Ledger > Inquiries and Reports > Trial Balance**.</span></span>
2. <span data-ttu-id="e9b93-135">Angiv følgende parametre:</span><span class="sxs-lookup"><span data-stu-id="e9b93-135">Set the following parameters:</span></span>
   - <span data-ttu-id="e9b93-136">**Fra dato** – Angiv starten af regnskabsåret.</span><span class="sxs-lookup"><span data-stu-id="e9b93-136">**From Date** - Enter the start of the fiscal year.</span></span>
   - <span data-ttu-id="e9b93-137">**Til dato** – Angiv den dato, rapporten skal genereres for.</span><span class="sxs-lookup"><span data-stu-id="e9b93-137">**To Date** - Enter the date you are generating the report for.</span></span>
   - <span data-ttu-id="e9b93-138">**Økonomisk dimension** – Angiv dette felt til **Hovedkontosæt**.</span><span class="sxs-lookup"><span data-stu-id="e9b93-138">**Financial Dimension** - Set this field to **Main Account set**.</span></span>
 3. <span data-ttu-id="e9b93-139">Vælg **Beregn**.</span><span class="sxs-lookup"><span data-stu-id="e9b93-139">Select **Calculate**.</span></span>
 4. <span data-ttu-id="e9b93-140">Eksporter rapporten til Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="e9b93-140">Export the report to Microsoft Excel.</span></span>

<span data-ttu-id="e9b93-141">Du skal nu kunne kopiere data fra Excel-rapporten i økonomirapport til rapporten Råbalance, så du kan sammenligne kolonnerne med **Ultimosaldo**.</span><span class="sxs-lookup"><span data-stu-id="e9b93-141">You should now be able to copy the data from the Financial Reporter Excel report to the Trial Balance report, so you can compare the **Closing Balance** columns.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]