---
title: Overføre projektbudgetter ved regnskabsårets afslutning
description: Denne artikel indeholder oplysninger om, hvordan du kan overføre resterende budgetbeløb til fremtidige år og oprette budgetregisteroplysninger.
author: RadhikaRS
manager: AnnBe
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 41e985825a24de2d6510938cf3d61715c35f9939
ms.sourcegitcommit: 2ea5ff784500d5be9203e9a1560eabd4fea46f4e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172324"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a><span data-ttu-id="c275c-103">Overføre projektbudgetter ved regnskabsårets afslutning</span><span class="sxs-lookup"><span data-stu-id="c275c-103">Transfer project budgets at fiscal year end</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c275c-104">Når du arbejder på et projekt, der strækker sig over flere år, kan du have resterende budgetbeløb ved regnskabsårets afslutning.</span><span class="sxs-lookup"><span data-stu-id="c275c-104">When working on a multi-year project, you might have remaining budget at the end of the fiscal year.</span></span> <span data-ttu-id="c275c-105">Du kan overføre de resterende budgetbeløb til et fremtidigt år og oprette budgetregisteroplysninger for beløbene i de tilknyttede finanskonti.</span><span class="sxs-lookup"><span data-stu-id="c275c-105">You can transfer the remaining budget amounts to a future year, and create budget register details for the amounts in the associated general ledger accounts.</span></span> <span data-ttu-id="c275c-106">Før du overfører restbeløbene, skal du gennemgå og analysere de resterende budgetbeløb.</span><span class="sxs-lookup"><span data-stu-id="c275c-106">Before you carry forward the remaining amounts, review and analyze the remaining budget amounts.</span></span>

## <a name="review-and-analyze-remaining-budget-amounts"></a><span data-ttu-id="c275c-107">Gennemgå og analysere resterende budgetbeløb</span><span class="sxs-lookup"><span data-stu-id="c275c-107">Review and analyze remaining budget amounts</span></span>

<span data-ttu-id="c275c-108">Udfør nedenstående trin for at gennemse budgetbeløbene ved årsafslutningen for projekter, men uden at overføre beløbene.</span><span class="sxs-lookup"><span data-stu-id="c275c-108">Complete the following steps to review the year-end budget amounts for projects, but not carry the amounts forward.</span></span>

1. <span data-ttu-id="c275c-109">Gå til **Projektstyring og regnskab** > **Periodisk** > **Budgetter** > **Overførte budgetter**.</span><span class="sxs-lookup"><span data-stu-id="c275c-109">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="c275c-110">Kontroller, at **Overfør resterende projektbudgetbeløb** ikke er aktiveret under fanen **Indstillinger for årsafslutning** på siden **Proces for projektbudgetoverførsel**.</span><span class="sxs-lookup"><span data-stu-id="c275c-110">On the **Project budget carry-forward process** page, on the **Year-end options** tab, verify that **Carry forward remaining project budget amounts** is not enabled.</span></span>
3. <span data-ttu-id="c275c-111">Vælg det regnskabsår, du vil have vist det resterende budgetbeløb for, i feltet **Projektbudgetår** under fanen **Parametre**.</span><span class="sxs-lookup"><span data-stu-id="c275c-111">On the **Parameters** tab, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
4. <span data-ttu-id="c275c-112">Vælg det regnskabsår, du vil have vist de resterende budgetbeløb for, i feltet **Nyt regnskabsår**.</span><span class="sxs-lookup"><span data-stu-id="c275c-112">In the **Opening fiscal year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
5. <span data-ttu-id="c275c-113">Vælg **Resterende budget** i feltet **Fra budgetmodel**.</span><span class="sxs-lookup"><span data-stu-id="c275c-113">In the **From forecast model** field, select **Remaining budget**.</span></span> 
6. <span data-ttu-id="c275c-114">Hvis du vil inkludere projekter, der opfylder dine valgte kriterier, uden at der er et resterende budget, skal du vælge **Vis nul resterende**.</span><span class="sxs-lookup"><span data-stu-id="c275c-114">To include projects that meet your selected criteria and have no remaining budget, select **Show zero remaining**.</span></span>  
7. <span data-ttu-id="c275c-115">Under fanen **Vælg budgetter** skal du vælge **Hent alle budgetter** for at indlæse alle budgetter, der opfylder dine valgte kriterier, og derefter vælge **Behandl**.</span><span class="sxs-lookup"><span data-stu-id="c275c-115">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match your selected criteria, and then select **Process**.</span></span> 
8. <span data-ttu-id="c275c-116">Hvis du opretter en databaseforespørgsel, der indlæser en bestemt gruppe budgetter i ruden, skal du vælge **Hent valgte budgetter**.</span><span class="sxs-lookup"><span data-stu-id="c275c-116">To design a database query that loads a specific set of budgets into the pane, select **Retrieve selected budgets**.</span></span>

<span data-ttu-id="c275c-117">Yderligere oplysninger om en bestemt linje i ruden finder du ved at markere linjen og derefter vælge **Vis budgetoplysninger** eller **Vis konti**.</span><span class="sxs-lookup"><span data-stu-id="c275c-117">For more information about a specific line in the pane, select the line, and then select **View budget details** or **View accounts**.</span></span>

## <a name="carry-forward-remaining-budget-amounts"></a><span data-ttu-id="c275c-118">Overføre resterende budgetbeløb</span><span class="sxs-lookup"><span data-stu-id="c275c-118">Carry forward remaining budget amounts</span></span> 

<span data-ttu-id="c275c-119">Når du behandler de resterende budgetbeløb, kan du oprette posteringer i finansbogholderiet for de beløb, du overfører.</span><span class="sxs-lookup"><span data-stu-id="c275c-119">When you process remaining budget amounts, you can create transactions in the general ledger for the amounts that you are carrying forward.</span></span> <span data-ttu-id="c275c-120">Hvis du vil oprette finansposteringer, skal du udføre trinnene i afsnittet [Overføre budgetbeløb og oprette finansposteringer](#carry-forward).</span><span class="sxs-lookup"><span data-stu-id="c275c-120">To create general ledger transactions, complete the steps in the section, [Carry forward budget amounts and create general ledger transactions](#carry-forward).</span></span> 

> [!NOTE]
> <span data-ttu-id="c275c-121">De budgetbeløb, der overføres, overføres til den budgetmodel, der er valgt som overført budgetmodel på siden **Budgetmodeller**.</span><span class="sxs-lookup"><span data-stu-id="c275c-121">Budget amounts that are carried forward are transferred to the forecast model that is selected in the **Forecast models** page as the carry-forward forecast model.</span></span>  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a><span data-ttu-id="c275c-122">Overføre budgetbeløb og oprette finansposteringer</span><span class="sxs-lookup"><span data-stu-id="c275c-122">Carry forward budget amounts and create general ledger transactions</span></span>

1.  <span data-ttu-id="c275c-123">Vælg **Projektstyring og regnskab** > **Periodisk** > **Budgetter** > **Overførte budgetter**.</span><span class="sxs-lookup"><span data-stu-id="c275c-123">Select **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="c275c-124">På siden **Proces for projektbudgetoverførsel** skal du vælge **Årsafslutning** og derefter aktivere **Overfør resterende projektbudgetbeløb** og **Opret budgetregisterposter i Finans**.</span><span class="sxs-lookup"><span data-stu-id="c275c-124">On the **Project budget carry-forward process** page, select **Year-end**, and then enable **Carry forward remaining project budget amounts** and **Create budget register entries in general ledger**.</span></span> 
3. <span data-ttu-id="c275c-125">Vælg følgende i feltgruppen **Projektparametre** under fanen **Parametre**:</span><span class="sxs-lookup"><span data-stu-id="c275c-125">On the **Parameters** tab, in the **Project parameters** field group, select the following:</span></span>

   - <span data-ttu-id="c275c-126">**Projektbudgetår**: Vælg starten af det regnskabsår, du vil have vist de resterende budgetbeløb for.</span><span class="sxs-lookup"><span data-stu-id="c275c-126">**Project budget year**: Select the beginning of the fiscal year for which you want to view the remaining budget amounts.</span></span> 
   - <span data-ttu-id="c275c-127">**Drift**: Opret driftsposter i Finans.</span><span class="sxs-lookup"><span data-stu-id="c275c-127">**Profit and loss**: Create profit and loss transactions in the general ledger.</span></span> 
   -  <span data-ttu-id="c275c-128">**IGVF**: Opret IGVF-transaktioner (igangværende arbejde) i Finans.</span><span class="sxs-lookup"><span data-stu-id="c275c-128">**WIP**: Create Work in Progress (WIP) transactions in the general ledger.</span></span>
   -  <span data-ttu-id="c275c-129">**Løn**: Opret lønfordelingsposteringer i Finans.</span><span class="sxs-lookup"><span data-stu-id="c275c-129">**Payroll**: Create payroll allocation transactions in the general ledger.</span></span> 

5. <span data-ttu-id="c275c-130">Angiv følgende oplysninger i feltgruppen **Finans**:</span><span class="sxs-lookup"><span data-stu-id="c275c-130">In the **General ledger** field group, provide the following information:</span></span> 

   - <span data-ttu-id="c275c-131">Vælg det regnskabsår, du vil overføre de resterende budgetbeløb i projekterne til, i feltet **Nyt regnskabsår**.</span><span class="sxs-lookup"><span data-stu-id="c275c-131">In the **Opening fiscal year** field, select the fiscal year that you want to transfer remaining budget amounts to for the projects.</span></span> <span data-ttu-id="c275c-132">Standardværdien er ét år efter værdien i feltet **Projektbudgetår**.</span><span class="sxs-lookup"><span data-stu-id="c275c-132">The default value is one year after the value in the **Project budget year** field.</span></span>
   -  <span data-ttu-id="c275c-133">Vælg den periode, du vil oprette budgetregisteroplysningerne i finansbogholderiet for, i feltet **Overførselsperiode**.</span><span class="sxs-lookup"><span data-stu-id="c275c-133">In the **Carry-forward period** field, select the period that you want to create the budget register details for in the general ledger.</span></span> <span data-ttu-id="c275c-134">Dette er typisk den første periode i det nye regnskabsår.</span><span class="sxs-lookup"><span data-stu-id="c275c-134">This is typically the first period in the opening fiscal year.</span></span>

6. <span data-ttu-id="c275c-135">Angiv følgende oplysninger i feltgruppen **Kopiér til/fra**:</span><span class="sxs-lookup"><span data-stu-id="c275c-135">In the **Copy from/to** field group, provide the following information:</span></span>

   - <span data-ttu-id="c275c-136">Vælg i feltet **Fra budgetmodel** den projektbudgetmodel, der er knyttet til de resterende budgetbeløb, som du vil overføre for projekterne.</span><span class="sxs-lookup"><span data-stu-id="c275c-136">In the **From forecast model** field, select the project budget forecast model associated with the remaining budget amounts you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="c275c-137">Vælg i feltet **Til finansbudgetmodel** den finansbudgetmodel, der er knyttet til de budgetbeløb, som du vil overføre til finansbogholderiet.</span><span class="sxs-lookup"><span data-stu-id="c275c-137">In the **To ledger budget model** field, select the ledger budget model associated with the budget amounts you want to transfer to the general ledger.</span></span> 
   -  <span data-ttu-id="c275c-138">Vælg **Overfør salgsvaluta**, hvis du vil bruge projektets salgsvaluta til de finansposteringer, der oprettes, når du overfører budgetbeløbene i projekterne.</span><span class="sxs-lookup"><span data-stu-id="c275c-138">Select **Transfer sales currency** to use the project's sales currency for the general ledger transactions that are created when you transfer the budget amounts for the projects.</span></span> <span data-ttu-id="c275c-139">Når indstillingen ikke er markeret, bruger posteringerne regnskabsvalutaen.</span><span class="sxs-lookup"><span data-stu-id="c275c-139">When the option is not selected, the transactions use the accounting currency.</span></span> 
   -  <span data-ttu-id="c275c-140">Vælg **Vis nul resterende** for at inkludere projekter, der ikke indeholder resterende budgetbeløb, men lever op til de øvrige kriterier, som du vælger i de projekter, der vises i den nederste rude.</span><span class="sxs-lookup"><span data-stu-id="c275c-140">Select **Show zero remaining** to include projects that have no remaining budget amounts, but meet the other criteria that you select in the projects displayed in the bottom pane.</span></span>

7. <span data-ttu-id="c275c-141">Under fanen **Vælg budgetter** skal du vælge **Hent alle budgetter** for at indlæse alle budgetter, der opfylder de kriterier, du har valgt.</span><span class="sxs-lookup"><span data-stu-id="c275c-141">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match the criteria you selected.</span></span> <span data-ttu-id="c275c-142">Hvis du foretrækker at oprette en databaseforespørgsel, der indlæser en bestemt gruppe projektbudgetter i ruden, skal du vælge **Hent valgte budgetter**.</span><span class="sxs-lookup"><span data-stu-id="c275c-142">If you prefer to design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>
8. <span data-ttu-id="c275c-143">For hvert projekt, du vil behandle, skal du vælge indstillingen i starten af projektlinjen.</span><span class="sxs-lookup"><span data-stu-id="c275c-143">For each project that you want to process, select the option at the beginning of the line for the project.</span></span>

    > [!TIP]
    > <span data-ttu-id="c275c-144">Hvis du vil vælge alle eller de fleste af projekterne, skal du markere afkrydsningsfeltet øverst til venstre.</span><span class="sxs-lookup"><span data-stu-id="c275c-144">To select all or most of the projects, select the check mark in the top upper-left corner.</span></span> <span data-ttu-id="c275c-145">Hvis du vil udelade behandlingen af et projekt, skal du fjerne markeringen for dette projekt.</span><span class="sxs-lookup"><span data-stu-id="c275c-145">To exclude processing any project, clear the check mark for that project.</span></span>

9. <span data-ttu-id="c275c-146">Hvis du vil overføre de resterende budgetbeløb for de valgte projekter til det valgte regnskabsår og oprette budgetregisteroplysninger i finansbogholderiet, skal du vælge **Behandl**.</span><span class="sxs-lookup"><span data-stu-id="c275c-146">To transfer the remaining budget amounts for the selected projects to the selected fiscal year and create budget register details in the general ledger, select **Process**.</span></span>

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a><span data-ttu-id="c275c-147">Overføre budgetbeløb uden at oprette finansposteringer</span><span class="sxs-lookup"><span data-stu-id="c275c-147">Carry forward budget amounts without creating general ledger transactions</span></span>

1. <span data-ttu-id="c275c-148">Gå til **Projektstyring og regnskab** > **Periodisk** > **Budgetter** > **Overførte budgetter**.</span><span class="sxs-lookup"><span data-stu-id="c275c-148">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span>
2. <span data-ttu-id="c275c-149">Vælg **Overfør resterende projektbudgetbeløb** ikke er aktiveret i feltet **Indstillinger for årsafslutning** på siden **Proces for projektbudgetoverførsel**.</span><span class="sxs-lookup"><span data-stu-id="c275c-149">On the **Project budget carry-forward process** page, in the **Year-end options** field, select **Carry forward remaining project budget amounts**.</span></span>
3. <span data-ttu-id="c275c-150">Vælg det regnskabsår, du vil have vist de resterende budgetbeløb for, i feltet **Projektbudgetår** i gruppen **Parametre**.</span><span class="sxs-lookup"><span data-stu-id="c275c-150">In the **Parameters** group, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amounts.</span></span>
4. <span data-ttu-id="c275c-151">Angiv følgende oplysninger i gruppen **Kopiér til/fra**:</span><span class="sxs-lookup"><span data-stu-id="c275c-151">In the **Copy from/to** group, provide the following information:</span></span>

   - <span data-ttu-id="c275c-152">Vælg i feltet **Fra budgetmodel** den projektbudgetmodel, der er knyttet til de resterende budgetbeløb, som du vil overføre for projekterne.</span><span class="sxs-lookup"><span data-stu-id="c275c-152">In the **From forecast model** field, select the project budget forecast model that is associated with the remaining budget amounts that you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="c275c-153">Vælg **Vis nul resterende**, hvis du vil inkludere projekter, der opfylder dine valgte kriterier, uden at der er et resterende budget.</span><span class="sxs-lookup"><span data-stu-id="c275c-153">Select **Show zero remaining** to include projects that have no remaining budget amounts, but that meet the other criteria you selected.</span></span>
   - <span data-ttu-id="c275c-154">I gruppen **Vælg budgetter** skal du vælge **Hent alle budgetter** for at indlæse alle budgetter, der opfylder de kriterier, du har valgt.</span><span class="sxs-lookup"><span data-stu-id="c275c-154">In the **Select Budgets** group, select **Retrieve all budgets** to load all budgets that match the criteria that you selected.</span></span> <span data-ttu-id="c275c-155">Hvis du opretter en databaseforespørgsel, der indlæser en bestemt gruppe projektbudgetter i ruden, skal du vælge **Hent valgte budgetter**.</span><span class="sxs-lookup"><span data-stu-id="c275c-155">To design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>

5. <span data-ttu-id="c275c-156">For hvert projekt, du vil behandle, skal du vælge indstillingen i starten af projektlinjen.</span><span class="sxs-lookup"><span data-stu-id="c275c-156">For each project that you want to process, select the option at the beginning of the line for the project.</span></span> 
6. <span data-ttu-id="c275c-157">Vælg **Behandl** for at overføre de resterende budgetbeløb i de valgte projekter til det valgte regnskabsår.</span><span class="sxs-lookup"><span data-stu-id="c275c-157">Select **Process** to transfer the remaining budget amounts for the selected projects to the selected fiscal year.</span></span>

