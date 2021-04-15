---
title: Periodiser orlovs- og fraværsplaner
description: Du kan periodisere orlov og fravær Dynamics 365 Human Resources for flere medarbejdere eller for en enkelt person.
author: andreabichsel
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 53c089da64f6b5f950a92afb9246454fb9a9686d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800255"
---
# <a name="accrue-leave-and-absence-plans"></a><span data-ttu-id="fd12e-103">Periodiser orlovs- og fraværsplaner</span><span class="sxs-lookup"><span data-stu-id="fd12e-103">Accrue leave and absence plans</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="fd12e-104">Du kan periodisere orlov og fravær Dynamics 365 Human Resources for flere medarbejdere eller for en enkelt person.</span><span class="sxs-lookup"><span data-stu-id="fd12e-104">You can accrue leave and absence in Dynamics 365 Human Resources for multiple employees or for an individual.</span></span>

## <a name="accrue-leave-and-absence-for-multiple-employees"></a><span data-ttu-id="fd12e-105">Periodisere orlov og fravær for flere medarbejdere</span><span class="sxs-lookup"><span data-stu-id="fd12e-105">Accrue leave and absence for multiple employees</span></span>

1. <span data-ttu-id="fd12e-106">På siden **Orlov og fravær** skal du vælge fanen **Links**.</span><span class="sxs-lookup"><span data-stu-id="fd12e-106">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="fd12e-107">Under **Administrer orlov** skal du vælge **Periodiser orlovs- og fraværsplaner**.</span><span class="sxs-lookup"><span data-stu-id="fd12e-107">Under **Manage leave**, select **Accrue leave and absence plans**.</span></span>

3. <span data-ttu-id="fd12e-108">Dialogboksen **Periodisere planer for orlov og fravær** vises.</span><span class="sxs-lookup"><span data-stu-id="fd12e-108">The **Accrue leave and absence plans** dialog box appears.</span></span> <span data-ttu-id="fd12e-109">I **Periodisering pr.** skal du vælge **Dags dato** eller **Brugerdefineret dato** og angive en brugerdefineret dato.</span><span class="sxs-lookup"><span data-stu-id="fd12e-109">In **Accrue as of**, either select **Today's date** or select **Custom date** and enter a custom date.</span></span>

4. <span data-ttu-id="fd12e-110">Hvis du vil køre periodiseringer for alle firmaer, skal du vælge **Alle firmaer**.</span><span class="sxs-lookup"><span data-stu-id="fd12e-110">If you want to run accruals for all companies, select **All companies**.</span></span> <span data-ttu-id="fd12e-111">Hvis du vil behandle periodiseringer for en enkelt orlovsplan, skal du vælge **Nej** for **Alle planer** og derefter vælge en **Orlovsplan**.</span><span class="sxs-lookup"><span data-stu-id="fd12e-111">If you want to process accruals for a single leave plan, select **No** for **All plans**, and then select a **Leave plan**.</span></span> <span data-ttu-id="fd12e-112">Hvis du vælger alle firmaer, kan du ikke vælge en individuel orlovsplan.</span><span class="sxs-lookup"><span data-stu-id="fd12e-112">If you select all companies, you can't select an individual leave plan.</span></span> 

5. <span data-ttu-id="fd12e-113">Hvis du vil køre periodiseringsprocessen i baggrunden, skal du vælge **Kør i baggrunden** og udføre følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="fd12e-113">If you want to run the accrual process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="fd12e-114">Angiv oplysninger om periodiseringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="fd12e-114">Enter information for the accrual process.</span></span>

   2. <span data-ttu-id="fd12e-115">Hvis du vil konfigurere et tilbagevendende job, skal du vælge **Gentagelse**, angive gentagelsesoplysningerne og vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="fd12e-115">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="fd12e-116">Hvis du vil oprette en jobpåmindelse, skal du vælge **Påmindelser**, vælge de påmindelser, du vil modtage, og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="fd12e-116">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="fd12e-117">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="fd12e-117">Select **OK**.</span></span> <span data-ttu-id="fd12e-118">Periodiseringsprocessen køres med de parametre, du angiver.</span><span class="sxs-lookup"><span data-stu-id="fd12e-118">The accrual process will run with the parameters you set.</span></span>

## <a name="accrue-leave-and-absence-for-an-employee"></a><span data-ttu-id="fd12e-119">Periodisere orlov og fravær for en medarbejder</span><span class="sxs-lookup"><span data-stu-id="fd12e-119">Accrue leave and absence for an employee</span></span>

1. <span data-ttu-id="fd12e-120">Vælg **Orlov** i medarbejderens post.</span><span class="sxs-lookup"><span data-stu-id="fd12e-120">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="fd12e-121">Vælg **Periodiser orlovs- og fraværsplaner**.</span><span class="sxs-lookup"><span data-stu-id="fd12e-121">Select **Accrue leave and absence**.</span></span>

3. <span data-ttu-id="fd12e-122">Dialogboksen **Periodisere planer for orlov og fravær** vises.</span><span class="sxs-lookup"><span data-stu-id="fd12e-122">The **Accrue leave and absence plans** dialog box appears.</span></span> <span data-ttu-id="fd12e-123">I **Periodisering pr.** skal du vælge **Dags dato** eller **Brugerdefineret dato** og angive en brugerdefineret dato.</span><span class="sxs-lookup"><span data-stu-id="fd12e-123">In **Accrue as of**, either select **Today's date** or select **Custom date** and enter a custom date.</span></span>

4. <span data-ttu-id="fd12e-124">Hvis du vil køre periodiseringer for alle firmaer, skal du vælge **Alle firmaer**.</span><span class="sxs-lookup"><span data-stu-id="fd12e-124">If you want to run accruals for all companies, select **All companies**.</span></span> <span data-ttu-id="fd12e-125">Hvis du vil behandle periodiseringer for en enkelt orlovsplan, skal du vælge **Nej** for **Alle planer** og derefter vælge en **Orlovsplan**.</span><span class="sxs-lookup"><span data-stu-id="fd12e-125">If you want to process accruals for a single leave plan, select **No** for **All plans**, and then select a **Leave plan**.</span></span> <span data-ttu-id="fd12e-126">Hvis du vælger alle firmaer, kan du ikke vælge en individuel orlovsplan.</span><span class="sxs-lookup"><span data-stu-id="fd12e-126">If you select all companies, you can't select an individual leave plan.</span></span> 

5. <span data-ttu-id="fd12e-127">Hvis du vil køre periodiseringsprocessen i baggrunden, skal du vælge **Kør i baggrunden** og udføre følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="fd12e-127">If you want to run the accrual process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="fd12e-128">Angiv oplysninger om periodiseringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="fd12e-128">Enter information for the accrual process.</span></span>

   2. <span data-ttu-id="fd12e-129">Hvis du vil konfigurere et tilbagevendende job, skal du vælge **Gentagelse**, angive gentagelsesoplysningerne og vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="fd12e-129">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="fd12e-130">Hvis du vil oprette en jobpåmindelse, skal du vælge **Påmindelser**, vælge de påmindelser, du vil modtage, og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="fd12e-130">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="fd12e-131">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="fd12e-131">Select **OK**.</span></span> <span data-ttu-id="fd12e-132">Periodiseringsprocessen køres med de parametre, du angiver.</span><span class="sxs-lookup"><span data-stu-id="fd12e-132">The accrual process will run with the parameters you set.</span></span>

## <a name="delete-leave-and-absence-accruals-for-multiple-employees"></a><span data-ttu-id="fd12e-133">Slette periodiseringer af orlov og fravær for flere medarbejdere</span><span class="sxs-lookup"><span data-stu-id="fd12e-133">Delete leave and absence accruals for multiple employees</span></span>

<span data-ttu-id="fd12e-134">Slet periodiseringsposter for en specifik plan og et bestemt datointerval.</span><span class="sxs-lookup"><span data-stu-id="fd12e-134">Delete accrual records for a specific plan and date range.</span></span> <span data-ttu-id="fd12e-135">Periodiseringsdatoer skal være dateret i dag eller i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="fd12e-135">Accrual dates must be dated today or in the future.</span></span>

1. <span data-ttu-id="fd12e-136">På siden **Orlov og fravær** skal du vælge fanen **Links**.</span><span class="sxs-lookup"><span data-stu-id="fd12e-136">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="fd12e-137">Under **Administrer orlov** skal du vælge **Slet periodiseringer af orlovs- og fraværsplaner**.</span><span class="sxs-lookup"><span data-stu-id="fd12e-137">Under **Manage leave**, select **Delete leave and absence plan accruals**.</span></span>

3. <span data-ttu-id="fd12e-138">Vælg **Orlovsplan** i dialogboksen **Slet periodiseringer af orlovs- og fraværsplaner**.</span><span class="sxs-lookup"><span data-stu-id="fd12e-138">In the **Delete leave and absence plan accruals** dialog box, select the **Leave plan**.</span></span> 

4. <span data-ttu-id="fd12e-139">Vælg **Slet saldoreguleringer**, hvis det er relevant.</span><span class="sxs-lookup"><span data-stu-id="fd12e-139">If applicable, choose **Delete balance adjustments**.</span></span>

5. <span data-ttu-id="fd12e-140">Angiv eller vælg en **Dato for orlovsperiodisering**.</span><span class="sxs-lookup"><span data-stu-id="fd12e-140">Enter or select a **Leave accrual date**.</span></span> <span data-ttu-id="fd12e-141">Denne dato skal være i dag eller i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="fd12e-141">This date has to be either today or in the future.</span></span> 

6. <span data-ttu-id="fd12e-142">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="fd12e-142">Select **OK**.</span></span> <span data-ttu-id="fd12e-143">Periodiseringsprocessen sletter periodiseringer med de parametre, du angiver.</span><span class="sxs-lookup"><span data-stu-id="fd12e-143">The accrual process will delete accruals with the parameters you set.</span></span> 

## <a name="delete-leave-and-absence-accruals-for-a-single-employee"></a><span data-ttu-id="fd12e-144">Slette periodiseringer af orlov og fravær for en enkelt medarbejder</span><span class="sxs-lookup"><span data-stu-id="fd12e-144">Delete leave and absence accruals for a single employee</span></span>

1. <span data-ttu-id="fd12e-145">Vælg **Orlov** i medarbejderens post.</span><span class="sxs-lookup"><span data-stu-id="fd12e-145">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="fd12e-146">Vælg **Slet periodiseringer af orlovs- og fraværsplaner**.</span><span class="sxs-lookup"><span data-stu-id="fd12e-146">Select **Delete leave and absence plan accruals**.</span></span>

3. <span data-ttu-id="fd12e-147">Vælg **Orlovsplan** i dialogboksen **Slet periodiseringer af orlovs- og fraværsplaner**.</span><span class="sxs-lookup"><span data-stu-id="fd12e-147">In the **Delete leave and absence plan accruals** dialog box, select **Leave plan**.</span></span> 

4. <span data-ttu-id="fd12e-148">Vælg **Slet saldoreguleringer**, hvis det er relevant.</span><span class="sxs-lookup"><span data-stu-id="fd12e-148">If applicable, choose **Delete balance adjustments**.</span></span>

5. <span data-ttu-id="fd12e-149">Angiv eller vælg en **Dato for orlovsperiodisering**.</span><span class="sxs-lookup"><span data-stu-id="fd12e-149">Enter or select a **Leave accrual date**.</span></span> <span data-ttu-id="fd12e-150">Denne dato skal være i dag eller i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="fd12e-150">This date must be either today or in the future.</span></span> 

6. <span data-ttu-id="fd12e-151">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="fd12e-151">Select **OK**.</span></span> <span data-ttu-id="fd12e-152">Periodiseringsprocessen sletter periodiseringer med de parametre, du angiver.</span><span class="sxs-lookup"><span data-stu-id="fd12e-152">The accrual process will delete accruals with the parameters you set.</span></span> 

## <a name="review-leave-accrual-and-deletion-processes"></a><span data-ttu-id="fd12e-153">Gennemse processer til orlovsperiodisering og sletning</span><span class="sxs-lookup"><span data-stu-id="fd12e-153">Review leave accrual and deletion processes</span></span>

<span data-ttu-id="fd12e-154">**Revision af orlovsperiodisering** vises, hver gang du kører eller sletter en periodisering for en eller flere medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="fd12e-154">**Leave accrual audit** displays each time you run or delete an accrual for one or all employees.</span></span> <span data-ttu-id="fd12e-155">Datoen og den person, der udførte handlingen, vises også.</span><span class="sxs-lookup"><span data-stu-id="fd12e-155">The date and person who performed the action also displays.</span></span>

1. <span data-ttu-id="fd12e-156">På siden **Orlov og fravær** skal du vælge fanen **Links**.</span><span class="sxs-lookup"><span data-stu-id="fd12e-156">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="fd12e-157">Under **Administrer orlov** skal du vælge **Slet revision af orlovsperiodisering**.</span><span class="sxs-lookup"><span data-stu-id="fd12e-157">Under **Manage leave**, select **Delete leave accrual audit**.</span></span>

## <a name="see-also"></a><span data-ttu-id="fd12e-158">Se også</span><span class="sxs-lookup"><span data-stu-id="fd12e-158">See also</span></span>

[<span data-ttu-id="fd12e-159">Oversigt over orlov og fravær</span><span class="sxs-lookup"><span data-stu-id="fd12e-159">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="fd12e-160">Oprette en plan for orlov og fravær</span><span class="sxs-lookup"><span data-stu-id="fd12e-160">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]