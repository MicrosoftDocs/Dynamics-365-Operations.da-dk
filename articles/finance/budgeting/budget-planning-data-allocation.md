---
title: Datafordeling til budgetplanlægning
description: I dette emne beskrives de forskellige fordelingsmetoder, der er tilgængelige i Microsoft Dynamics 365 Finance, og hvordan de kan bruges.
author: ShylaThompson
ms.date: 03/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: roschlom
ms.custom: 15191
ms.assetid: 89a918e8-59a4-4711-a2e9-b41989ddd0f1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bef79df8d9806771f87a6f77a0c9094887050646
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822197"
---
# <a name="budget-planning-data-allocation"></a><span data-ttu-id="7e6bb-103">Datafordeling til budgetplanlægning</span><span class="sxs-lookup"><span data-stu-id="7e6bb-103">Budget planning data allocation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7e6bb-104">I dette emne beskrives de forskellige fordelingsmetoder, der er tilgængelige i Microsoft Dynamics 365 Finance, og hvordan de kan bruges.</span><span class="sxs-lookup"><span data-stu-id="7e6bb-104">This topic describes the allocation methods that are available in Microsoft Dynamics 365 Finance and how they can be used.</span></span>  

<span data-ttu-id="7e6bb-105">Du kan distribuere data i en budgetplan på en række forskellige måder at give et præcist billede af de forventede beløb.</span><span class="sxs-lookup"><span data-stu-id="7e6bb-105">You can distribute the data in a budget plan in a number of ways to accurately portray the projected amounts.</span></span>

## <a name="allocation-methods"></a><span data-ttu-id="7e6bb-106">Fordelingsmetoder</span><span class="sxs-lookup"><span data-stu-id="7e6bb-106">Allocation methods</span></span>
<span data-ttu-id="7e6bb-107">Tre fordelingsmetoder (Fordel hen over perioder, Fordel på dimensioner og Brug finansfordelingsregler) kan oprette budgetplanlinjer, der er baseret på linjer i den samme budgetplan.</span><span class="sxs-lookup"><span data-stu-id="7e6bb-107">Three allocation methods (Allocate across periods, Allocate to dimensions, and Use ledger allocation rules) can create budget plan lines that are based on lines in the same budget plan.</span></span> <span data-ttu-id="7e6bb-108">Tre andre metoder (Aggregat, Fordel og Kopier fra budgetplanen) kan oprette budgetplanlinjer i andre budgetplaner.</span><span class="sxs-lookup"><span data-stu-id="7e6bb-108">Three other methods (Aggregate, Distribute, and Copy from budget plan) can create budget plan lines in other budget plans.</span></span> <span data-ttu-id="7e6bb-109">Du kan angive destinationsscenariet for alle seks fordelingsmetoder.</span><span class="sxs-lookup"><span data-stu-id="7e6bb-109">For all six allocation methods, you specify the destination scenario.</span></span> <span data-ttu-id="7e6bb-110">Destinationsscenariet kan enten være det samme som kildescenariet eller forskelligt fra kildescenariet.</span><span class="sxs-lookup"><span data-stu-id="7e6bb-110">The destination scenario can be either the same as the source scenario or different from the source scenario.</span></span> <span data-ttu-id="7e6bb-111">Desuden kan du angive, om nye linjer er føjet til budgetplanen eller erstatter de aktuelle linjer i budgetplanen.</span><span class="sxs-lookup"><span data-stu-id="7e6bb-111">Additionally, you can specify whether new lines are appended to the budget plan or replace the current lines in the budget plan.</span></span>

> [!NOTE] 
> <span data-ttu-id="7e6bb-112">Et entydigt scenarie skal bruges til sammenlægning, der adskiller sig fra det scenarie, som blev brugt til distribution, eller andre ændringer, som tidligere er udført i den overordnede plan.</span><span class="sxs-lookup"><span data-stu-id="7e6bb-112">A unique scenario should be used for aggregation that is different from the scenario that was used for distribution or other modifications that were previously performed  in the parent plan.</span></span>  

<span data-ttu-id="7e6bb-113">[![Fordel på tværs af metode for periodefordeling](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)
**Fordel på tværs af perioder** – En periodefordelingskategori bruges til at fordele budgetplanlinjerne fra Kildebudgetplanscenariet på tværs af perioder i destinationsscenariet.</span><span class="sxs-lookup"><span data-stu-id="7e6bb-113">[![Allocate across Periods allocation method](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)
**Allocate across periods** – A period allocation category is used to allocate the budget plan lines from the source budget plan scenario across periods in the destination scenario.</span></span> <span data-ttu-id="7e6bb-114">Beløbet i kildedokumentet er tildelt flere linjer i destinationsscenariet, baseret på den procentdel og dato, der er defineret i periodefordelingskategorien.</span><span class="sxs-lookup"><span data-stu-id="7e6bb-114">The source amount is assigned to multiple lines in the destination scenario, based on the percentage and date that are defined in the period allocation category.</span></span>         

<span data-ttu-id="7e6bb-115">[![Fordel til metode for dimensionsfordeling](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**Fordel på dimensioner** – Budgetplanlinjerne fordeles fra kildebudgetplanlægningsscenariet til en eller flere linjer i destinationsscenariet, baseret på procentsatserne og de økonomiske dimensioner, der er defineret i den valgte budgetfordelingsbetingelse.</span><span class="sxs-lookup"><span data-stu-id="7e6bb-115">[![Allocate to Dimensions allocation method](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**Allocate to dimensions** – The budget plan lines are allocated from the source budget planning scenario to one or more lines in the destination scenario, based on the percentages and financial dimensions that are defined in a selected budget allocation term.</span></span>           

<span data-ttu-id="7e6bb-116">![Aggreger diagram](./media/aggregatechart-300x230.png)
**Aggreger** – Budgetplanlinjerne aggregeres fra kildebudgetplanscenariet i de tilknyttede (underordnede) budgetplaner til destinationsscenariet i den overordnede budgetplan.</span><span class="sxs-lookup"><span data-stu-id="7e6bb-116">![Aggregate chart](./media/aggregatechart-300x230.png)
**Aggregate** – The budget plan lines are aggregated from the source budget plan scenario in the associated (child) budget plans to the destination scenario in the parent budget plan.</span></span> <span data-ttu-id="7e6bb-117">Denne metode gør det muligt at konsolidere budgetbeløb, der er oprettet på et lavere niveau i organisationen, på et højere niveau.</span><span class="sxs-lookup"><span data-stu-id="7e6bb-117">This method enables budget amounts that are prepared at a lower level in the organization to be consolidated at a higher level.</span></span>          

<span data-ttu-id="7e6bb-118">[![Fordel diagram](./media/distributechart-300x230.png)](./media/distributechart.png)
**Fordel** – Budgetplanlinjerne fordeles fra kilden budgetplanlægningsscenariet i den overordnede budgetplan til destinationsscenariet i de tilknyttede (underordnede) budgetplaner, baseret på de økonomiske dimensioner for organisationsenheder i de tilknyttede planer.</span><span class="sxs-lookup"><span data-stu-id="7e6bb-118">[![Distribute chart](./media/distributechart-300x230.png)](./media/distributechart.png)
**Distribute** – The budget plan lines are distributed from the source budget planning scenario in the parent budget plan to the destination scenario in the associated (child) budget plans, based on the financial dimensions of the organization units of the associated plans.</span></span> <span data-ttu-id="7e6bb-119">Denne metode gør det muligt at sprede budgetbeløb, der er oprettet på et højere niveau i organisationen, ud for en mere lokaliseret gennemgang.</span><span class="sxs-lookup"><span data-stu-id="7e6bb-119">This method enables budget amounts that are prepared at a higher level in the organization to be spread out for more localized review.</span></span>           

<span data-ttu-id="7e6bb-120">[![Regler for finansfordeling](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**Brug finansfordelingsregler** – Budgetplanlinjerne fordeles fra kildebudgetplanlægningscenariet til destinationscenariet på basis af den valgte finansfordelingsregel.</span><span class="sxs-lookup"><span data-stu-id="7e6bb-120">[![Ledger allocation rules](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**Use ledger allocation rules** – The budget plan lines are distributed from the source budget planning scenario to the destination scenario, based on the ledger allocation rule that is selected.</span></span> 

<span data-ttu-id="7e6bb-121">[![Kopier fra budgetplan](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**Kopier fra budgetplanen** – Som i fordelingsmetoden oprettes budgetplanlinjer i destinationen på basis af linjerne i en relateret budgetplan.</span><span class="sxs-lookup"><span data-stu-id="7e6bb-121">[![Copy from budget plan](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**Copy from budget plan** – As in the Distribute allocation method, budget plan lines are created in the destination, based on lines in a related budget plan.</span></span> <span data-ttu-id="7e6bb-122">Men for denne metode behøver kildebudgetplanen ikke være overordnet men kan være på et højere niveau i hierarkiet for budgetplanen.</span><span class="sxs-lookup"><span data-stu-id="7e6bb-122">However, for this method, the source budget plan doesn't have to be the parent but can be at any higher level in the budget plan hierarchy.</span></span> <span data-ttu-id="7e6bb-123">Denne fordelingsmetode er nyttig, hvis konsoliderede beløb oprindeligt er budgetteret på et meget højere niveau og skal overføres til et lavere niveau i organisationen for detaljeret gennemgang og regulering, før de kan modtage godkendelse på øverste niveau.</span><span class="sxs-lookup"><span data-stu-id="7e6bb-123">This allocation method is useful if consolidated amounts are originally budgeted at a much higher level, and must be transferred to a lower level of the organization for detailed review and adjustment before they can receive upper-level approval.</span></span>          

## <a name="using-allocation-methods-in-a-budget-plan"></a><span data-ttu-id="7e6bb-124">Ved hjælp af fordelingsmetoder i en budgetplan</span><span class="sxs-lookup"><span data-stu-id="7e6bb-124">Using allocation methods in a budget plan</span></span>
<span data-ttu-id="7e6bb-125">Hvis du vil udføre fordelinger, skal du vælge de linjer, der skal tildeles, og derefter klikke på **Fordel budget**.</span><span class="sxs-lookup"><span data-stu-id="7e6bb-125">To perform allocations on the budget plan page, select the lines to allocate, and then click **Allocate budget**.</span></span>

<span data-ttu-id="7e6bb-126">[![Knappen Fordel budget](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png)</span><span class="sxs-lookup"><span data-stu-id="7e6bb-126">[![Allocate budget button](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png)</span></span> 

<span data-ttu-id="7e6bb-127">Vælg derefter en fordelingsmetode.</span><span class="sxs-lookup"><span data-stu-id="7e6bb-127">Next, select an allocation method.</span></span> <span data-ttu-id="7e6bb-128">De resterende felter angives derefter baseret på den metode, du har valgt.</span><span class="sxs-lookup"><span data-stu-id="7e6bb-128">The remaining fields are then set, based on the method that you selected.</span></span> <span data-ttu-id="7e6bb-129">Disse felter indeholder kilden og destinationen for budgetplansdataene og en indstilling, der gør det muligt at multiplicere kilden med en bestemt faktor, når destinationsbeløbene er oprettet, for at forenkle masseregulering.</span><span class="sxs-lookup"><span data-stu-id="7e6bb-129">These fields include the source and destination of the budget plan data, and an option that lets you multiply the source by a specified factor when the destination amounts are created, to simplify bulk adjustment.</span></span> <span data-ttu-id="7e6bb-130">Du kan også angive indstillingen **Vedhæft til plan**.</span><span class="sxs-lookup"><span data-stu-id="7e6bb-130">You can also set the **Append to plan** option.</span></span> <span data-ttu-id="7e6bb-131">Vælg **Nej** for at erstatte de eksisterende budgetplanlinjer, eller Vælg **Ja** for at bevare de eksisterende budgetplanlinjer og tilføje nye linjer for de fordelte beløb.</span><span class="sxs-lookup"><span data-stu-id="7e6bb-131">Select **No** to replace the existing budget plan lines, or select **Yes** to retain the existing budget plan lines and add new lines for the allocated amounts.</span></span>

## <a name="automating-allocations-during-a-workflow"></a><span data-ttu-id="7e6bb-132">Automatisering af tildelinger under en arbejdsproces</span><span class="sxs-lookup"><span data-stu-id="7e6bb-132">Automating allocations during a workflow</span></span>
<span data-ttu-id="7e6bb-133">En effektiv funktion gør det muligt at foretage tildelinger automatisk som et led i en arbejdsgang i budgetplanlægningen.</span><span class="sxs-lookup"><span data-stu-id="7e6bb-133">One powerful feature enables allocations to be performed automatically as part of a budget planning workflow.</span></span> <span data-ttu-id="7e6bb-134">I løbet af arbejdsgangen for en budgetplan kan automatiserede opgaver starte en tildeling på et bestemt stadie i budgetplanlægningen.</span><span class="sxs-lookup"><span data-stu-id="7e6bb-134">As a budget plan moves through its workflow, automated tasks can invoke an allocation at a specified budget planning stage.</span></span> 

<span data-ttu-id="7e6bb-135">Hvis du vil konfigurere automatisk tildeling, skal du først oprette en fordelingstidsplan på siden **Konfiguration af budgetplanlægning**.</span><span class="sxs-lookup"><span data-stu-id="7e6bb-135">To set up automated allocation, you must first create an allocation schedule on the **Budget planning configuration** page.</span></span> <span data-ttu-id="7e6bb-136">Fordelingstidsplanen definerer den fordelingsmetode, der skal bruges, når den automatiske tildeling køres, og værdierne af de forskellige fordelingsindstillinger (se beskrivelse i afsnittet ovenfor).</span><span class="sxs-lookup"><span data-stu-id="7e6bb-136">The allocation schedule defines the allocation method that will be used when the automated allocation is run, and the values of the various allocation options (see the previous section for descriptions).</span></span> 

<span data-ttu-id="7e6bb-137">Derefter skal du oprette en trinvis fordeling på siden **Konfiguration af budgetplanlægning**.</span><span class="sxs-lookup"><span data-stu-id="7e6bb-137">Next, you create a stage allocation on the **Budget planning configuration** page.</span></span> <span data-ttu-id="7e6bb-138">Den trinvise fordeling tildeler en fordelingstidsplan til arbejdsgangen for budgetplanlægningen og budgetplanlægningstrinnet.</span><span class="sxs-lookup"><span data-stu-id="7e6bb-138">The stage allocation assigns an allocation schedule to the budget planning workflow and stage.</span></span> 

<span data-ttu-id="7e6bb-139">Til sidst skal du tilføje en automatiseret opgave til fordeling på det ønskede arbejdsprocesstadium i budgetplanlægningen.</span><span class="sxs-lookup"><span data-stu-id="7e6bb-139">Finally, add an automated task for budget planning stage allocation at the desired workflow stage.</span></span> <span data-ttu-id="7e6bb-140">I følgende eksempel er der indsat to fase budgetplanlægningsfordelinger (vises med rødt) i arbejdsprocessen.</span><span class="sxs-lookup"><span data-stu-id="7e6bb-140">In the following example, two budget planning stage allocations (outlined in red) have been inserted into the workflow.</span></span>

<span data-ttu-id="7e6bb-141">[![Trinfordelinger for budgetplanlægning](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)</span><span class="sxs-lookup"><span data-stu-id="7e6bb-141">[![Budget planning stage allocations](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]