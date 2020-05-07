---
title: Oprette avancerede kontrakter til fakturering baseret på status
description: Dette emne forklarer, hvordan du opretter projektkontrakter, så du kan generere fakturaer for debitorer baseret på en procentdel af det udførte arbejde.
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
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
ms.openlocfilehash: 90cae104d0abad909606ef6a0e0c45ed95e74de2
ms.sourcegitcommit: dfef2faf881b2db1bd0f016df36e2b838105312b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/22/2020
ms.locfileid: "3282817"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a><span data-ttu-id="2b753-103">Oprette avancerede kontrakter til fakturering baseret på status</span><span class="sxs-lookup"><span data-stu-id="2b753-103">Create advanced contracts for billing based on progress</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="2b753-104">Dette emne forklarer, hvordan du opretter projektkontrakter, så du kan oprette fakturaer for debitorer baseret på en procentdel af det udførte arbejde.</span><span class="sxs-lookup"><span data-stu-id="2b753-104">This topic explains how to create project contracts so that you can create invoices for customers, based on a percentage of completed work.</span></span> <span data-ttu-id="2b753-105">Fakturabeløb beregnes automatisk for de budgetkategorier, som du opretter for det arbejde, du konfigurerer for et projekt.</span><span class="sxs-lookup"><span data-stu-id="2b753-105">Invoice amounts are automatically calculated for the budget categories of work that you set up for a project.</span></span> <span data-ttu-id="2b753-106">Tidspunktet for fakturaen angives, når du forhandler projektkontrakten med kunden.</span><span class="sxs-lookup"><span data-stu-id="2b753-106">The invoice timing is set when you negotiate the project contract with the customer.</span></span>

<span data-ttu-id="2b753-107">Benyt fremgangsmåderne i dette emne til at oprette en kontrakt, et tilhørende projekt og de regler for fakturering, der skal bruges til beregning af fakturabeløbene for de budgetkategorier, som du opretter for arbejde på projektet.</span><span class="sxs-lookup"><span data-stu-id="2b753-107">Use the procedures in this topic to set up a contract, an associated project, and the billing rules that calculate invoice amounts for the budget categories of work that you set up for the project.</span></span>

<span data-ttu-id="2b753-108">Når du har oprettet kontrakten og projektet, kan du angive projektdetaljerne.</span><span class="sxs-lookup"><span data-stu-id="2b753-108">After you've created the contract and the project, you can set up the details of the project.</span></span> <span data-ttu-id="2b753-109">Du kan for eksempel definere aktiviteter og tildele projektet arbejdere.</span><span class="sxs-lookup"><span data-stu-id="2b753-109">For example, you can define activities and assign workers to the project.</span></span>

## <a name="example"></a><span data-ttu-id="2b753-110">Eksempel</span><span class="sxs-lookup"><span data-stu-id="2b753-110">Example</span></span>

<span data-ttu-id="2b753-111">Din organisation udvikler software.</span><span class="sxs-lookup"><span data-stu-id="2b753-111">Your organization is a software development firm.</span></span> <span data-ttu-id="2b753-112">Du aftaler at udvikle en pakkeløsning med et system til lønningsregnskab for en kunde for i alt 20.000 kr.</span><span class="sxs-lookup"><span data-stu-id="2b753-112">You agree to develop a payroll accounting package for a customer for a total fee of 20,000 US dollars (USD).</span></span> <span data-ttu-id="2b753-113">Din organisation accepterer at fakturere kunden, efterhånden som du fuldfører de angivne procentdele af arbejdet på projektet.</span><span class="sxs-lookup"><span data-stu-id="2b753-113">Your organization agrees to invoice the customer as you complete specific percentages of the project.</span></span> <span data-ttu-id="2b753-114">Du konfigurerer følgende projektkategorier for arbejdet, så du kan bruge dem i faktureringsprocessen:</span><span class="sxs-lookup"><span data-stu-id="2b753-114">You set up the following project categories for the work, so that you can use them in the billing process:</span></span>

- <span data-ttu-id="2b753-115">Rådgivning</span><span class="sxs-lookup"><span data-stu-id="2b753-115">Consulting</span></span>
- <span data-ttu-id="2b753-116">Design</span><span class="sxs-lookup"><span data-stu-id="2b753-116">Design</span></span>
- <span data-ttu-id="2b753-117">Installation</span><span class="sxs-lookup"><span data-stu-id="2b753-117">Installation</span></span>

<span data-ttu-id="2b753-118">Du opretter også regler for fakturering, så fakturabeløbene beregnes automatisk for den procentdel af arbejdet, der er fuldført inden for hver kategori.</span><span class="sxs-lookup"><span data-stu-id="2b753-118">You also set up billing rules that automatically calculate the invoice amounts for the percentage of project work that is completed in each category.</span></span>

<span data-ttu-id="2b753-119">Budgetadministratoren opretter et budget for projektkategorierne.</span><span class="sxs-lookup"><span data-stu-id="2b753-119">The budget manager creates a budget for the project categories.</span></span> <span data-ttu-id="2b753-120">Beløbet for udført arbejde beregnes automatisk som en procentdel af det faktiske arbejde sammenlignet med de budgetterede beløb.</span><span class="sxs-lookup"><span data-stu-id="2b753-120">The amount of completed work is automatically calculated as a percentage of actual work in comparison to the budgeted amounts.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2b753-121">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="2b753-121">Prerequisites</span></span>

<span data-ttu-id="2b753-122">Før du opretter et projekt, der bruger faktureringsregler, skal du konfigurere nummerserierne for faktureringsregler og en gebyrkladde, der bruges til at bogføre statusfaktureringer.</span><span class="sxs-lookup"><span data-stu-id="2b753-122">Before you create a project that uses billing rules, you must set up the number sequences for billing rules and a fee journal that is used to post progress billings.</span></span>

1. <span data-ttu-id="2b753-123">Gå til **Projektstyring og regnskab** \> **Opsætning** \> **Parametre for projektstyring og regnskab**.</span><span class="sxs-lookup"><span data-stu-id="2b753-123">Go to **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>
2. <span data-ttu-id="2b753-124">På siden **Parametre for projektstyring og regnskab** skal du under fanen **Nummerserier** du angive den nummerserie, du vil bruge, når der oprettes faktureringsregler.</span><span class="sxs-lookup"><span data-stu-id="2b753-124">On the **Project management and accounting parameters** page, on the **Number sequences** tab, set up the number sequence that you want to use when billing rules are created.</span></span>
3. <span data-ttu-id="2b753-125">Gå til **Projektstyring og regnskab** \> **Kladder** \> **Gebyr**.</span><span class="sxs-lookup"><span data-stu-id="2b753-125">Go to **Project management and accounting** \> **Journals** \> **Fee**.</span></span>
4. <span data-ttu-id="2b753-126">Vælg **Ny** på siden **Gebyrkladde**, og angiv kladdenavnet.</span><span class="sxs-lookup"><span data-stu-id="2b753-126">On the **Fee journal** page, select **New**, and enter the journal name.</span></span>

## <a name="create-a-contract-for-progress-billings"></a><span data-ttu-id="2b753-127">Oprette en kontrakt for statusfaktureringer</span><span class="sxs-lookup"><span data-stu-id="2b753-127">Create a contract for progress billings</span></span>

<span data-ttu-id="2b753-128">Brug denne fremgangsmåde til at oprette en projektkontrakt til et fastprisprojekt.</span><span class="sxs-lookup"><span data-stu-id="2b753-128">Use this procedure to create a project contract for a fixed-price project.</span></span> <span data-ttu-id="2b753-129">Du opretter en projektfaktura, når det arbejde, der er udført på projektet, når en bestemt procentdel.</span><span class="sxs-lookup"><span data-stu-id="2b753-129">You create a project invoice when the work that is completed on the project reaches a specified percentage.</span></span>

1. <span data-ttu-id="2b753-130">Gå til **Projektstyring og regnskab** \> **Projekter** \> **Projektkontrakter**.</span><span class="sxs-lookup"><span data-stu-id="2b753-130">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="2b753-131">På siden **Projektkontrakter** skal du vælge **Ny**.</span><span class="sxs-lookup"><span data-stu-id="2b753-131">On the **Project contracts** page, select **New**.</span></span>
3. <span data-ttu-id="2b753-132">Angiv følgende felter i dialogboksen **Ny projektkontrakt**:</span><span class="sxs-lookup"><span data-stu-id="2b753-132">In the **New project contract** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="2b753-133">**Navn**</span><span class="sxs-lookup"><span data-stu-id="2b753-133">**Name**</span></span>
    - <span data-ttu-id="2b753-134">**Finansieringstype**</span><span class="sxs-lookup"><span data-stu-id="2b753-134">**Funding type**</span></span>
    - <span data-ttu-id="2b753-135">**Finansieringskilde**</span><span class="sxs-lookup"><span data-stu-id="2b753-135">**Funding source**</span></span>
    - <span data-ttu-id="2b753-136">**Salgsvaluta** – Det er den valuta, der som standard skal bruges til debitorfakturaer, som er knyttet til projektkontrakten.</span><span class="sxs-lookup"><span data-stu-id="2b753-136">**Sales currency** – By default, this currency is used for customer invoices that are associated with the project contract.</span></span> <span data-ttu-id="2b753-137">Du kan dog ændre salgsvalutaen på en bestemt debitorfaktura.</span><span class="sxs-lookup"><span data-stu-id="2b753-137">However, you can change the sales currency on a specific customer invoice.</span></span>

4. <span data-ttu-id="2b753-138">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="2b753-138">Select **OK**.</span></span> <span data-ttu-id="2b753-139">Oplysningerne kopieres til hovedet på siden **Projektkontrakter**.</span><span class="sxs-lookup"><span data-stu-id="2b753-139">The information is copied to the header of the **Project contracts** page.</span></span>
5. <span data-ttu-id="2b753-140">Udfyld resten af de nødvendige oplysninger om projektet på siden **Projektkontrakter**.</span><span class="sxs-lookup"><span data-stu-id="2b753-140">On the **Project contracts** page, fill in the rest of the required information for the project.</span></span>

## <a name="create-a-project-for-progress-billings"></a><span data-ttu-id="2b753-141">Oprette et projekt for statusfaktureringer</span><span class="sxs-lookup"><span data-stu-id="2b753-141">Create a project for progress billings</span></span>

<span data-ttu-id="2b753-142">Brug følgende procedure til at oprette et projekt og eventuelle underprojekter, der er tilknyttet en projektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="2b753-142">Follow these steps to create a project and any subprojects that are associated with a project contract.</span></span>

1. <span data-ttu-id="2b753-143">Gå til **Projektstyring og regnskab** \> **Projekter** \> **Alle projekter**.</span><span class="sxs-lookup"><span data-stu-id="2b753-143">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="2b753-144">På siden **Alle projekter** skal du vælge **Ny**.</span><span class="sxs-lookup"><span data-stu-id="2b753-144">On the **All projects** page, select **New**.</span></span>
3. <span data-ttu-id="2b753-145">Vælg **Tid og materiale** i feltet **Projekttype** i dialogboksen **Nyt projekt**.</span><span class="sxs-lookup"><span data-stu-id="2b753-145">In the **New project** dialog box, in the **Project type** field, select **Time and material**.</span></span>
4. <span data-ttu-id="2b753-146">Vælg en projektgruppe.</span><span class="sxs-lookup"><span data-stu-id="2b753-146">Select a project group.</span></span> <span data-ttu-id="2b753-147">En projektgruppe definerer posteringsoplysninger for de projekter, der er tildelt gruppen.</span><span class="sxs-lookup"><span data-stu-id="2b753-147">A project group defines the posting information for the projects that are assigned to the group.</span></span>
5. <span data-ttu-id="2b753-148">Vælg **Opret projekt**.</span><span class="sxs-lookup"><span data-stu-id="2b753-148">Select **Create project**.</span></span>
6. <span data-ttu-id="2b753-149">Når du har oprettet projektet, skal du angive projektstadiet til **Igangværende**.</span><span class="sxs-lookup"><span data-stu-id="2b753-149">After the project is created, set the project stage to **In process**.</span></span>

## <a name="create-a-budget-for-a-project"></a><span data-ttu-id="2b753-150">Oprette et budget til et projekt</span><span class="sxs-lookup"><span data-stu-id="2b753-150">Create a budget for a project</span></span>

<span data-ttu-id="2b753-151">Budgetkategorierne bruges til automatisk beregning af fakturabeløb for den procentdel af arbejdet, der er fuldført i hver kategori.</span><span class="sxs-lookup"><span data-stu-id="2b753-151">Budget categories are used to automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="2b753-152">Udfør følgende trin for at oprette budgetkategorier for de forkalkulerede omkostninger.</span><span class="sxs-lookup"><span data-stu-id="2b753-152">Follow these steps to create budget categories for the estimated costs.</span></span>

1. <span data-ttu-id="2b753-153">Gå til **Projektstyring og regnskab** \> **Projekter** \> **Alle projekter**.</span><span class="sxs-lookup"><span data-stu-id="2b753-153">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="2b753-154">Vælg og åbn det ønskede projekt på siden **Alle projekter**.</span><span class="sxs-lookup"><span data-stu-id="2b753-154">On the **All projects** page, select and open the project that you want.</span></span>
3. <span data-ttu-id="2b753-155">Vælg **Projektbudget** i gruppen **Budget** under fanen **Plan** i handlingsruden på siden **Projekter**.</span><span class="sxs-lookup"><span data-stu-id="2b753-155">On the **Projects** page, on the Action Pane, on the **Plan** tab, in the **Budget** group, select **Project budget**.</span></span>
4. <span data-ttu-id="2b753-156">Angiv en forkalkuleret omkostning for hver kategori i projektet på siden **Projektbudget**.</span><span class="sxs-lookup"><span data-stu-id="2b753-156">On the **Project budget** page, enter an estimated cost for each category in the project.</span></span>

## <a name="create-billing-rules-for-progress-billings"></a><span data-ttu-id="2b753-157">Oprette faktureringsregler for statusfaktureringer</span><span class="sxs-lookup"><span data-stu-id="2b753-157">Create billing rules for progress billings</span></span>

1. <span data-ttu-id="2b753-158">Gå til **Projektstyring og regnskab** \> **Projekter** \> **Projektkontrakter**.</span><span class="sxs-lookup"><span data-stu-id="2b753-158">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="2b753-159">Vælg og åbn en projektkontrakt på siden **Projektkontrakter**.</span><span class="sxs-lookup"><span data-stu-id="2b753-159">On the **Project contracts** page, select and open a project contract.</span></span>
3. <span data-ttu-id="2b753-160">Vælg **Tilføj** i oversigtspanelet **Faktureringsregler** på siden Projektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="2b753-160">On the project contract page, on the **Billing rules** FastTab, select **Add**.</span></span>
4. <span data-ttu-id="2b753-161">Vælg **Status** i feltet **Linjetype** på siden **Faktureringsregel**.</span><span class="sxs-lookup"><span data-stu-id="2b753-161">On the **Billing rule** page, in the **Line type** field, select **Progress**.</span></span>
5. <span data-ttu-id="2b753-162">Angiv kontraktens samlede beløb i feltet **Kontraktværdi** i oversigtspanelet **Faktureringsregellinjer - detaljer**.</span><span class="sxs-lookup"><span data-stu-id="2b753-162">On the **Billing rule line details** FastTab, in the **Contract value** field, enter the total value of the contract.</span></span>
6. <span data-ttu-id="2b753-163">Vælg den kategori, som gebyrtransaktionen skal bogføres i, i feltet **Kategori**.</span><span class="sxs-lookup"><span data-stu-id="2b753-163">In the **Category** field, select the category to post the fee transaction to.</span></span>
7. <span data-ttu-id="2b753-164">Vælg det projekt, der bruger denne faktureringsregel, i feltet **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="2b753-164">In the **Project** field, select the project that uses this billing rule.</span></span>
8. <span data-ttu-id="2b753-165">Valgfrit: Tildel faktureringsreglen flere projekter.</span><span class="sxs-lookup"><span data-stu-id="2b753-165">Optional: Assign the billing rule to additional projects.</span></span> <span data-ttu-id="2b753-166">Vælg et projekt i sektionen **Tilgængelige projekter** i oversigtspanelet **Projekt**, og vælg derefter den højre pileknap for at føje projektet til sektionen **Valgte projekter**.</span><span class="sxs-lookup"><span data-stu-id="2b753-166">On the **Project** FastTab, in the **Available projects** section, select a project, and then select the right arrow button to add the project to the **Selected projects** section.</span></span>
9. <span data-ttu-id="2b753-167">Valgfrit: Beregn det procentvise beløb, som kunden holder tilbage fra betalinger på en faktura.</span><span class="sxs-lookup"><span data-stu-id="2b753-167">Optional: Calculate the percentage amount that the customer withholds from payments on an invoice.</span></span> <span data-ttu-id="2b753-168">Vælg finansieringskilden i oversigtspanelet **Betingelser for tilbageholdelse af betaling**, og angiv derefter tilbageholdelsesprocenten i feltet **Tilbageholdelsesprocent**.</span><span class="sxs-lookup"><span data-stu-id="2b753-168">On the **Payment retention terms** FastTab, select the funding source, and then, in the **Retention percentage** field, enter the retention percentage.</span></span>
10. <span data-ttu-id="2b753-169">Gentag disse trin, hvis du vil oprette flere faktureringsregler for projektkontrakten.</span><span class="sxs-lookup"><span data-stu-id="2b753-169">Repeat these steps to create additional billing rules for the project contract.</span></span>
