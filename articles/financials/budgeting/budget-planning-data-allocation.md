---
title: "Fordeling af budgetplanlægningsdata"
description: "I denne artikel beskrives de forskellige fordelingsmetoder, der er tilgængelige i Microsoft Dynamics 365 for Finance and Operations, og hvordan de kan bruges."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15191
ms.assetid: 89a918e8-59a4-4711-a2e9-b41989ddd0f1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 6436a412f6b10040e1c7254a4912c839e610dede
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---

# <a name="budget-planning-data-allocation"></a><span data-ttu-id="d524e-103">Datafordeling til budgetplanlægning</span><span class="sxs-lookup"><span data-stu-id="d524e-103">Budget planning data allocation</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="d524e-104">I denne artikel beskrives de forskellige fordelingsmetoder, der er tilgængelige i Microsoft Dynamics 365 for Finance and Operations, og hvordan de kan bruges.</span><span class="sxs-lookup"><span data-stu-id="d524e-104">This article describes the various allocation methods that are available in Microsoft Dynamics 365 for Finance and Operations and how they can be used.</span></span>  

<span data-ttu-id="d524e-105">Du kan distribuere data i en budgetplan på en række forskellige måder at give et præcist billede af de forventede beløb.</span><span class="sxs-lookup"><span data-stu-id="d524e-105">You can distribute the data in a budget plan in a number of ways to accurately portray the projected amounts.</span></span>

## <a name="allocation-methods"></a><span data-ttu-id="d524e-106">Fordelingsmetoder</span><span class="sxs-lookup"><span data-stu-id="d524e-106">Allocation methods</span></span>
<span data-ttu-id="d524e-107">Tre fordelingsmetoder (Fordel hen over perioder, Fordel på dimensioner og Brug finansfordelingsregler) kan oprette budgetplanlinjer, der er baseret på linjer i den samme budgetplan.</span><span class="sxs-lookup"><span data-stu-id="d524e-107">Three allocation methods (Allocate across periods, Allocate to dimensions, and Use ledger allocation rules) can create budget plan lines that are based on lines in the same budget plan.</span></span> <span data-ttu-id="d524e-108">Tre andre metoder (Aggregat, Fordel og Kopier fra budgetplanen) kan oprette budgetplanlinjer i andre budgetplaner.</span><span class="sxs-lookup"><span data-stu-id="d524e-108">Three other methods (Aggregate, Distribute, and Copy from budget plan) can create budget plan lines in other budget plans.</span></span> <span data-ttu-id="d524e-109">Du kan angive destinationsscenariet for alle seks fordelingsmetoder.</span><span class="sxs-lookup"><span data-stu-id="d524e-109">For all six allocation methods, you specify the destination scenario.</span></span> <span data-ttu-id="d524e-110">Destinationsscenariet kan enten være det samme som kildescenariet eller forskelligt fra kildescenariet.</span><span class="sxs-lookup"><span data-stu-id="d524e-110">The destination scenario can be either the same as the source scenario or different from the source scenario.</span></span> <span data-ttu-id="d524e-111">Desuden kan du angive, om nye linjer er føjet til budgetplanen eller erstatter de aktuelle linjer i budgetplanen.</span><span class="sxs-lookup"><span data-stu-id="d524e-111">Additionally, you can specify whether new lines are appended to the budget plan or replace the current lines in the budget plan.</span></span>

<span data-ttu-id="d524e-112">[![AllocateAcrossPeriods](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)
**Fordel hen over perioder** – en periodefordelingskategori bruges til at fordele budgetplanlinjerne fra Kildebudgetplanscenariet på tværs af perioder i destinationsscenariet.</span><span class="sxs-lookup"><span data-stu-id="d524e-112">[![AllocateAcrossPeriods](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)
**Allocate across periods** – A period allocation category is used to allocate the budget plan lines from the source budget plan scenario across periods in the destination scenario.</span></span> <span data-ttu-id="d524e-113">Beløbet i kildedokumentet er tildelt flere linjer i destinationsscenariet, baseret på den procentdel og dato, der er defineret i periodefordelingskategorien.</span><span class="sxs-lookup"><span data-stu-id="d524e-113">The source amount is assigned to multiple lines in the destination scenario, based on the percentage and date that are defined in the period allocation category.</span></span>         

<span data-ttu-id="d524e-114">[![AllocateToDimensions](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**Fordel på dimensioner** – Budgetplanlinjerne fordeles fra kildebudgetplanlægningsscenariet til en eller flere linjer i destinationsscenariet, baseret på procentsatserne og de økonomiske dimensioner, der er defineret i den valgte budgetfordelingsbetingelse.</span><span class="sxs-lookup"><span data-stu-id="d524e-114">[![AllocateToDimensions](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**Allocate to dimensions** – The budget plan lines are allocated from the source budget planning scenario to one or more lines in the destination scenario, based on the percentages and financial dimensions that are defined in a selected budget allocation term.</span></span>           

<span data-ttu-id="d524e-115">![AggregateChart](./media/aggregatechart-300x230.png)
**Aggreger** – Budgetplanlinjerne aggregeres fra kildebudgetplanscenariet i de tilknyttede (underordnede) budgetplaner til destinationsscenariet i den overordnede budgetplan.</span><span class="sxs-lookup"><span data-stu-id="d524e-115">![AggregateChart](./media/aggregatechart-300x230.png)
**Aggregate** – The budget plan lines are aggregated from the source budget plan scenario in the associated (child) budget plans to the destination scenario in the parent budget plan.</span></span> <span data-ttu-id="d524e-116">Denne metode gør det muligt at konsolidere budgetbeløb, der er oprettet på et lavere niveau i organisationen, på et højere niveau.</span><span class="sxs-lookup"><span data-stu-id="d524e-116">This method enables budget amounts that are prepared at a lower level in the organization to be consolidated at a higher level.</span></span>          

<span data-ttu-id="d524e-117">[![DistributeChart](./media/distributechart-300x230.png)](./media/distributechart.png)
**Fordel** – Budgetplanlinjerne fordeles fra kilden budgetplanlægningsscenariet i den overordnede budgetplan til destinationsscenariet i de tilknyttede (underordnede) budgetplaner, baseret på de økonomiske dimensioner for organisationsenheder i de tilknyttede planer.</span><span class="sxs-lookup"><span data-stu-id="d524e-117">[![DistributeChart](./media/distributechart-300x230.png)](./media/distributechart.png)
**Distribute** – The budget plan lines are distributed from the source budget planning scenario in the parent budget plan to the destination scenario in the associated (child) budget plans, based on the financial dimensions of the organization units of the associated plans.</span></span> <span data-ttu-id="d524e-118">Denne metode gør det muligt at sprede budgetbeløb, der er oprettet på et højere niveau i organisationen, ud for en mere lokaliseret gennemgang.</span><span class="sxs-lookup"><span data-stu-id="d524e-118">This method enables budget amounts that are prepared at a higher level in the organization to be spread out for more localized review.</span></span>           

<span data-ttu-id="d524e-119">[![LedgerAllocationRules](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**Brug finansfordelingsregler** – Budgetplanlinjerne fordeles fra kildebudgetplanlægningscenariet til destinationscenariet på basis af den valgte finansfordelingsregel.</span><span class="sxs-lookup"><span data-stu-id="d524e-119">[![LedgerAllocationRules](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**Use ledger allocation rules** – The budget plan lines are distributed from the source budget planning scenario to the destination scenario, based on the ledger allocation rule that is selected.</span></span> 

<span data-ttu-id="d524e-120">[![CopyFromBudgetPlan](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**Kopier fra budgetplanen** – Som i fordelingsmetoden oprettes budgetplanlinjer i destinationen på basis af linjerne i en relateret budgetplan.</span><span class="sxs-lookup"><span data-stu-id="d524e-120">[![CopyFromBudgetPlan](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**Copy from budget plan** – As in the Distribute allocation method, budget plan lines are created in the destination, based on lines in a related budget plan.</span></span> <span data-ttu-id="d524e-121">Men for denne metode behøver kildebudgetplanen ikke være overordnet men kan være på et højere niveau i hierarkiet for budgetplanen.</span><span class="sxs-lookup"><span data-stu-id="d524e-121">However, for this method, the source budget plan doesn't have to be the parent but can be at any higher level in the budget plan hierarchy.</span></span> <span data-ttu-id="d524e-122">Denne fordelingsmetode er nyttig, hvis konsoliderede beløb oprindeligt er budgetteret på et meget højere niveau og skal overføres til et lavere niveau i organisationen for detaljeret gennemgang og regulering, før de kan modtage godkendelse på øverste niveau.</span><span class="sxs-lookup"><span data-stu-id="d524e-122">This allocation method is useful if consolidated amounts are originally budgeted at a much higher level, and must be transferred to a lower level of the organization for detailed review and adjustment before they can receive upper-level approval.</span></span>          

## <a name="using-allocation-methods-in-a-budget-plan"></a><span data-ttu-id="d524e-123">Ved hjælp af fordelingsmetoder i en budgetplan</span><span class="sxs-lookup"><span data-stu-id="d524e-123">Using allocation methods in a budget plan</span></span>
<span data-ttu-id="d524e-124">Hvis du vil udføre fordelinger, skal du vælge de linjer, der skal tildeles, og derefter klikke på **Fordel budget**.</span><span class="sxs-lookup"><span data-stu-id="d524e-124">To perform allocations on the budget plan page, select the lines to allocate, and then click **Allocate budget**.</span></span>

<span data-ttu-id="d524e-125">[![AllocateBudgetButton](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png)</span><span class="sxs-lookup"><span data-stu-id="d524e-125">[![AllocateBudgetButton](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png)</span></span> 

<span data-ttu-id="d524e-126">Vælg derefter en fordelingsmetode.</span><span class="sxs-lookup"><span data-stu-id="d524e-126">Next, select an allocation method.</span></span> <span data-ttu-id="d524e-127">De resterende felter angives derefter baseret på den metode, du har valgt.</span><span class="sxs-lookup"><span data-stu-id="d524e-127">The remaining fields are then set, based on the method that you selected.</span></span> <span data-ttu-id="d524e-128">Disse felter indeholder kilden og destinationen for budgetplansdataene og en indstilling, der gør det muligt at multiplicere kilden med en bestemt faktor, når destinationsbeløbene er oprettet, for at forenkle masseregulering.</span><span class="sxs-lookup"><span data-stu-id="d524e-128">These fields include the source and destination of the budget plan data, and an option that lets you multiply the source by a specified factor when the destination amounts are created, to simplify bulk adjustment.</span></span> <span data-ttu-id="d524e-129">Du kan også angive indstillingen **Vedhæft til plan**.</span><span class="sxs-lookup"><span data-stu-id="d524e-129">You can also set the **Append to plan** option.</span></span> <span data-ttu-id="d524e-130">Vælg **Nej** for at erstatte de eksisterende budgetplanlinjer, eller Vælg **Ja** for at bevare de eksisterende budgetplanlinjer og tilføje nye linjer for de fordelte beløb.</span><span class="sxs-lookup"><span data-stu-id="d524e-130">Select **No** to replace the existing budget plan lines, or select **Yes** to retain the existing budget plan lines and add new lines for the allocated amounts.</span></span>

## <a name="automating-allocations-during-a-workflow"></a><span data-ttu-id="d524e-131">Automatisering af tildelinger under en arbejdsproces</span><span class="sxs-lookup"><span data-stu-id="d524e-131">Automating allocations during a workflow</span></span>
<span data-ttu-id="d524e-132">En effektiv funktion gør det muligt at foretage tildelinger automatisk som et led i en arbejdsgang i budgetplanlægningen.</span><span class="sxs-lookup"><span data-stu-id="d524e-132">One powerful feature enables allocations to be performed automatically as part of a budget planning workflow.</span></span> <span data-ttu-id="d524e-133">I løbet af arbejdsgangen for en budgetplan kan automatiserede opgaver starte en tildeling på et bestemt stadie i budgetplanlægningen.</span><span class="sxs-lookup"><span data-stu-id="d524e-133">As a budget plan moves through its workflow, automated tasks can invoke an allocation at a specified budget planning stage.</span></span> 

<span data-ttu-id="d524e-134">Hvis du vil konfigurere automatisk tildeling, skal du først oprette en fordelingstidsplan på siden **Konfiguration af budgetplanlægning**.</span><span class="sxs-lookup"><span data-stu-id="d524e-134">To set up automated allocation, you must first create an allocation schedule on the **Budget planning configuration** page.</span></span> <span data-ttu-id="d524e-135">Fordelingstidsplanen definerer den fordelingsmetode, der skal bruges, når den automatiske tildeling køres, og værdierne af de forskellige fordelingsindstillinger (se beskrivelse i afsnittet ovenfor).</span><span class="sxs-lookup"><span data-stu-id="d524e-135">The allocation schedule defines the allocation method that will be used when the automated allocation is run, and the values of the various allocation options (see the previous section for descriptions).</span></span> 

<span data-ttu-id="d524e-136">Derefter skal du oprette en trinvis fordeling på siden **Konfiguration af budgetplanlægning**.</span><span class="sxs-lookup"><span data-stu-id="d524e-136">Next, you create a stage allocation on the **Budget planning configuration** page.</span></span> <span data-ttu-id="d524e-137">Den trinvise fordeling tildeler en fordelingstidsplan til arbejdsgangen for budgetplanlægningen og budgetplanlægningstrinnet.</span><span class="sxs-lookup"><span data-stu-id="d524e-137">The stage allocation assigns an allocation schedule to the budget planning workflow and stage.</span></span> 

<span data-ttu-id="d524e-138">Til sidst skal du tilføje en automatiseret opgave til fordeling på det ønskede arbejdsprocesstadium i budgetplanlægningen.</span><span class="sxs-lookup"><span data-stu-id="d524e-138">Finally, add an automated task for budget planning stage allocation at the desired workflow stage.</span></span> <span data-ttu-id="d524e-139">I følgende eksempel er der indsat to fase budgetplanlægningsfordelinger (vises med rødt) i arbejdsprocessen.</span><span class="sxs-lookup"><span data-stu-id="d524e-139">In the following example, two budget planning stage allocations (outlined in red) have been inserted into the workflow.</span></span>

<span data-ttu-id="d524e-140">[![BudgetPlanningStageAllocations](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)</span><span class="sxs-lookup"><span data-stu-id="d524e-140">[![BudgetPlanningStageAllocations](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)</span></span>




