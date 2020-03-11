---
title: Udarbejde en kompensationsstruktur
description: Denne artikel fører dig gennem processen med at oprette en kompensationsplan og melde medarbejdere til planen via berettigelsesregler.
author: andreabichsel
manager: AnnBe
ms.date: 02/10/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: DefaultDashboard, HcmCompensationWorkspace, HcmCompFixedPlansPart, HRMCompFixedPlanTable, HRMCompCreateGridDialog, HRCCompGridView, HRMCompEligibility,  HRCCompGrid
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 124d0f7f83feebabf622f00732c25bfa0f6eccdd
ms.sourcegitcommit: de715b7fda2f1548f2f443b9e0f6d09f5b881d61
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/10/2020
ms.locfileid: "3034257"
---
# <a name="develop-a-compensation-structure"></a><span data-ttu-id="23fc8-103">Udarbejde en kompensationsstruktur</span><span class="sxs-lookup"><span data-stu-id="23fc8-103">Develop a compensation structure</span></span>

<span data-ttu-id="23fc8-104">Denne artikel fører dig gennem processen med at oprette en kompensationsplan og melde medarbejdere til planen via berettigelsesregler.</span><span class="sxs-lookup"><span data-stu-id="23fc8-104">This article walks you through creating a fixed compensation plan and enrolling employees in the plan through eligibility rules.</span></span> <span data-ttu-id="23fc8-105">Denne artikel bruger USMF-demodata og gælder for styring af kompensation og frynsegoder.</span><span class="sxs-lookup"><span data-stu-id="23fc8-105">This article uses the USMF demo data and applies to Compensation and Benefits Managers.</span></span>

## <a name="create-a-fixed-compensation-plan"></a><span data-ttu-id="23fc8-106">Oprette en fast løn-struktur</span><span class="sxs-lookup"><span data-stu-id="23fc8-106">Create a fixed compensation plan</span></span>

1. <span data-ttu-id="23fc8-107">Vælg **Kompensationsstyring**.</span><span class="sxs-lookup"><span data-stu-id="23fc8-107">Select **Compensation management**.</span></span>

2. <span data-ttu-id="23fc8-108">Vælg **Faste lønstrukturer**.</span><span class="sxs-lookup"><span data-stu-id="23fc8-108">Select **Fixed compensation plans**.</span></span>

3. <span data-ttu-id="23fc8-109">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="23fc8-109">Select **New**.</span></span>

4. <span data-ttu-id="23fc8-110">Angiv en værdi i feltet **Plan**.</span><span class="sxs-lookup"><span data-stu-id="23fc8-110">In the **Plan** field, enter a value.</span></span>

5. <span data-ttu-id="23fc8-111">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="23fc8-111">In the **Description** field, enter a value.</span></span>

6. <span data-ttu-id="23fc8-112">Angiv en dato i feltet **Ikrafttrædelsesdato**.</span><span class="sxs-lookup"><span data-stu-id="23fc8-112">In the **Effective date** field, enter a date.</span></span>

7. <span data-ttu-id="23fc8-113">I feltet **Type** skal du vælge, om den faste lønstruktur er en plan af typen **Omfang**, **Klasse** eller **Trin**.</span><span class="sxs-lookup"><span data-stu-id="23fc8-113">In the **Type** field, select whether the fixed compensation plan is a **Band**, **Grade**, or **Step** plan.</span></span>

8. <span data-ttu-id="23fc8-114">Afkrydsningsfeltet **Anbefaling tilladt** fungerer som standardværdi for alle handlinger, der er føjet til denne plan i en proceshændelse.</span><span class="sxs-lookup"><span data-stu-id="23fc8-114">The **Recommendation allowed** checkbox acts as a default value for any actions added to this plan in a Process event.</span></span> <span data-ttu-id="23fc8-115">Ved at tillade anbefalinger kan du tilsidesætte det beregnede aftalebeløb ved behandling af kompensation.</span><span class="sxs-lookup"><span data-stu-id="23fc8-115">Allowing recommendations enables you to override the calculated guideline amount when processing compensation.</span></span>

9. <span data-ttu-id="23fc8-116">I feltet **Tolerance uden for afgrænsningerne** kan du angive, hvordan du vil håndtere kompensationsbeløb, der falder uden for den angivne lønstrukturramme på det givne niveau.</span><span class="sxs-lookup"><span data-stu-id="23fc8-116">The **Out of range tolerance** field allows you to specify how you want to handle compensation amounts that fall outside of the specified compensation structure range for the given level.</span></span> <span data-ttu-id="23fc8-117">Hvis du angiver feltet **Tolerance uden for afgrænsningerne** til **Ingen**, kan du bruge et hvilket som helst kompensationsbeløb.</span><span class="sxs-lookup"><span data-stu-id="23fc8-117">Setting the **Out of range tolerance** field to **None** allows you to use any compensation amount.</span></span> <span data-ttu-id="23fc8-118">**Tolerancen Blød** advarer brugerne, hvis kompensationsbeløbet er mindre end minimum- eller større end maksimumbeløbet for referencepunktet for det pågældende niveau.</span><span class="sxs-lookup"><span data-stu-id="23fc8-118">**Soft tolerance** warns users if the compensation amount is less than the minimum or greater than the maximum reference point amounts for that level.</span></span> <span data-ttu-id="23fc8-119">Brugerne kan ignorere advarslen og fortsætte.</span><span class="sxs-lookup"><span data-stu-id="23fc8-119">Users can ignore the warning and continue.</span></span> <span data-ttu-id="23fc8-120">**Tolerancen Hård** genererer en fejl, hvis en medarbejders løn er angivet uden for minimale og maksimale referencepunkter for niveauet og justerer automatisk medarbejderens løn, så den ligger inden for rammen.</span><span class="sxs-lookup"><span data-stu-id="23fc8-120">**Hard tolerance** generates an error if an employee's compensation is outside the minimum and maximum reference points for the level and will automatically adjust the employee's compensation to fall within the range.</span></span>

10. <span data-ttu-id="23fc8-121">I feltet **Ansættelsesregel** beregnes en medarbejders kompensation under en proceshændelse.</span><span class="sxs-lookup"><span data-stu-id="23fc8-121">The **Hire rule** field calculates an employee's compensation during a process event.</span></span> <span data-ttu-id="23fc8-122">En **Ansættelsesregel** af **Procent** beregner en forholdsmæssig stigning for den tid, arbejderen har været ansat i cyklussen.</span><span class="sxs-lookup"><span data-stu-id="23fc8-122">A **Hire rule** of **Percent** calculates an increase that's prorated for the length of the time the worker has been employed in the cycle.</span></span>

11. <span data-ttu-id="23fc8-123">Skriv en værdi i feltet **Valuta**.</span><span class="sxs-lookup"><span data-stu-id="23fc8-123">In the **Currency** field, type a value.</span></span>

12. <span data-ttu-id="23fc8-124">Indtast eller vælg en værdi i feltet **Konvertering af lønsats**.</span><span class="sxs-lookup"><span data-stu-id="23fc8-124">In the **Pay rate conversion** field, enter or select a value.</span></span>

13. <span data-ttu-id="23fc8-125">Udvid sektionen **Rammeudnyttelsesmatrix**.</span><span class="sxs-lookup"><span data-stu-id="23fc8-125">Expand the **Range utilization matrix** section.</span></span> <span data-ttu-id="23fc8-126">Du kan eventuelt tilføje poster for rammeudnyttelse for at få medarbejdere til deres middelpunkt hurtigere og gøre det langsommere for dem at nå maksimum for deres ramme.</span><span class="sxs-lookup"><span data-stu-id="23fc8-126">Optionally, add range utilization records to get employees to their midpoint faster and slow them from reaching the maximum of their range.</span></span>

14. <span data-ttu-id="23fc8-127">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="23fc8-127">Select **Save**.</span></span> <span data-ttu-id="23fc8-128">Det aktiverer knappen **Konfigurer kompensation** og fortsætter med at definere kompensationsstrukturen for planen.</span><span class="sxs-lookup"><span data-stu-id="23fc8-128">This enables the **Set up compensation** button and continue defining your compensation structure for the plan.</span></span>

15. <span data-ttu-id="23fc8-129">Vælg **Konfigurer kompensation**.</span><span class="sxs-lookup"><span data-stu-id="23fc8-129">Select **Set up compensation**.</span></span> <span data-ttu-id="23fc8-130">Du kan oprette en kompensationsstruktur ved hjælp af en af disse tre metoder:</span><span class="sxs-lookup"><span data-stu-id="23fc8-130">You can create a compensation structure by using one of these three methods:</span></span>

    - <span data-ttu-id="23fc8-131">Opret en helt ny struktur ved at vælge et sæt referencepunkter og tilføje niveauer for at oprette din egen struktur.</span><span class="sxs-lookup"><span data-stu-id="23fc8-131">Create a completely new structure by selecting a set of reference points and adding the levels to create your own structure.</span></span>
    - <span data-ttu-id="23fc8-132">Kopiér kompensationsstruktur fra en eksisterende plan som udgangspunkt, og tilpas den til den nye plan.</span><span class="sxs-lookup"><span data-stu-id="23fc8-132">Copy a compensation structure from an existing plan as a starting point and modify it for the new plan.</span></span>
    - <span data-ttu-id="23fc8-133">Vælg et eksisterende kompensationsgitter.</span><span class="sxs-lookup"><span data-stu-id="23fc8-133">Select an existing compensation grid.</span></span> <span data-ttu-id="23fc8-134">Hvis en anden plan allerede bruger kompensationsgitteret, afspejler den anden plan også eventuelle ændringer, du laver i gitteret.</span><span class="sxs-lookup"><span data-stu-id="23fc8-134">If another plan already uses the compensation grid, the other plan also reflects any changes you make to the grid.</span></span>

16. <span data-ttu-id="23fc8-135">Vælg **Opret nyt matrix fra eksisterende kompensationsmatrix**.</span><span class="sxs-lookup"><span data-stu-id="23fc8-135">Select **Create new from existing compensation matrix**.</span></span>

17. <span data-ttu-id="23fc8-136">Indtast eller vælg en værdi i feltet **Kopier fra gitter**.</span><span class="sxs-lookup"><span data-stu-id="23fc8-136">In the **Copy from grid** field, enter or select a value.</span></span> <span data-ttu-id="23fc8-137">Du kan eventuelt ændre navnet på det nye kompensationsgitter, du opretter, ved at kopiere det valgte gitter.</span><span class="sxs-lookup"><span data-stu-id="23fc8-137">Optionally, you can change the name of the new compensation grid that you create by copying the selected grid.</span></span>

18. <span data-ttu-id="23fc8-138">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="23fc8-138">Select **OK**.</span></span>

19. <span data-ttu-id="23fc8-139">Vælg **Masseændring**.</span><span class="sxs-lookup"><span data-stu-id="23fc8-139">Select **Mass change**.</span></span> <span data-ttu-id="23fc8-140">**Masseændring** gør det muligt at bevare kompensationsbeløb for matrixen ved at anvende en stigning i procent eller fladt beløb på ét eller flere niveauer og/eller referencepunkter.</span><span class="sxs-lookup"><span data-stu-id="23fc8-140">**Mass change** allows you to maintain the compensation matrix amounts by applying a percent or flat amount increase to one or more levels or reference points.</span></span>

20. <span data-ttu-id="23fc8-141">Indtast et tal i feltet **Justeringsbeløb**.</span><span class="sxs-lookup"><span data-stu-id="23fc8-141">In the **Adjustment amount** field, enter a number.</span></span>

21. <span data-ttu-id="23fc8-142">Markér eller fjern markeringen af alle rækker på listen.</span><span class="sxs-lookup"><span data-stu-id="23fc8-142">In the list, mark or unmark all rows.</span></span>

22. <span data-ttu-id="23fc8-143">Klik på **Anvend på gitter**.</span><span class="sxs-lookup"><span data-stu-id="23fc8-143">Click **Apply to grid**.</span></span>

23. <span data-ttu-id="23fc8-144">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="23fc8-144">Close the page.</span></span> <span data-ttu-id="23fc8-145">Når du har oprettet kompensationsstrukturen, kan du vælge, hvilke referencepunkter der skal bruges som kontrolpunkt for den faste lønstruktur.</span><span class="sxs-lookup"><span data-stu-id="23fc8-145">After you create the compensation structure, you can select which of the reference points to use as the control point for the fixed compensation plan.</span></span> <span data-ttu-id="23fc8-146">Kontrolpunktet bruges til at beregne kompensationsforholdet for en medarbejder.</span><span class="sxs-lookup"><span data-stu-id="23fc8-146">The control point is used to calculate an employee's Compa Ratio.</span></span>

24. <span data-ttu-id="23fc8-147">Indtast eller vælg en værdi i feltet **Kontrolpunkt**.</span><span class="sxs-lookup"><span data-stu-id="23fc8-147">In the **Control point** field, enter or select a value.</span></span>

25. <span data-ttu-id="23fc8-148">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="23fc8-148">Close the page.</span></span>

## <a name="create-an-eligibility-rule-for-the-fixed-compensation-plan"></a><span data-ttu-id="23fc8-149">Opret en berettigelsesregel for den faste lønstruktur</span><span class="sxs-lookup"><span data-stu-id="23fc8-149">Create an eligibility rule for the fixed compensation plan</span></span>

<span data-ttu-id="23fc8-150">Du kan ikke tildele en fast lønstruktur til en medarbejder, før du definerer berettigelsesregler for strukturen.</span><span class="sxs-lookup"><span data-stu-id="23fc8-150">You can't assign a fixed compensation plan to an employee until you define eligibility rules for the plan.</span></span>  

1. <span data-ttu-id="23fc8-151">Vis **Berettigelsesregler**.</span><span class="sxs-lookup"><span data-stu-id="23fc8-151">Select **Eligibility rules**.</span></span>

2. <span data-ttu-id="23fc8-152">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="23fc8-152">Select **New**.</span></span>

3. <span data-ttu-id="23fc8-153">Indtast en værdi i feltet **Berettigelse**.</span><span class="sxs-lookup"><span data-stu-id="23fc8-153">In the **Eligibility** field, enter a value.</span></span>

4. <span data-ttu-id="23fc8-154">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="23fc8-154">In the **Description** field, enter a value.</span></span>

5. <span data-ttu-id="23fc8-155">Angiv en dato i feltet **Ikrafttrædelsesdato**.</span><span class="sxs-lookup"><span data-stu-id="23fc8-155">In the **Effective date** field, enter a date.</span></span> <span data-ttu-id="23fc8-156">Faste og variable lønstrukturer bruger berettigelsesregler.</span><span class="sxs-lookup"><span data-stu-id="23fc8-156">Both fixed and variable compensation plans use eligibility rules.</span></span> <span data-ttu-id="23fc8-157">Vælg plantypen i feltet **Type**.</span><span class="sxs-lookup"><span data-stu-id="23fc8-157">In the **Type** field, select the type of plan.</span></span>

6. <span data-ttu-id="23fc8-158">I feltet **Plan** indtastes eller vælges en værdi.</span><span class="sxs-lookup"><span data-stu-id="23fc8-158">In the **Plan** field, enter or select a value.</span></span> <span data-ttu-id="23fc8-159">Vælg de kriterier, en medarbejder skal opfylde for at være berettiget til lønstrukturen.</span><span class="sxs-lookup"><span data-stu-id="23fc8-159">Select the criteria an employee must meet in order to be eligible for the compensation plan.</span></span> <span data-ttu-id="23fc8-160">Kriterier kan omfatte:</span><span class="sxs-lookup"><span data-stu-id="23fc8-160">Criteria can include:</span></span>

    - <span data-ttu-id="23fc8-161">**Afdeling**</span><span class="sxs-lookup"><span data-stu-id="23fc8-161">**Department**</span></span>
    - <span data-ttu-id="23fc8-162">**Fagforening**</span><span class="sxs-lookup"><span data-stu-id="23fc8-162">**Labor union**</span></span>
    - <span data-ttu-id="23fc8-163">**Sted** (**Kompensationsregion**)</span><span class="sxs-lookup"><span data-stu-id="23fc8-163">**Location** (**Compensation region**)</span></span>
    - <span data-ttu-id="23fc8-164">**Stilling**</span><span class="sxs-lookup"><span data-stu-id="23fc8-164">**Job**</span></span>
    - <span data-ttu-id="23fc8-165">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="23fc8-165">**Function**</span></span>
    - <span data-ttu-id="23fc8-166">**Jobtype**</span><span class="sxs-lookup"><span data-stu-id="23fc8-166">**Job type**</span></span>
    - <span data-ttu-id="23fc8-167">**Kompensationsniveau**</span><span class="sxs-lookup"><span data-stu-id="23fc8-167">**Compensation level**</span></span>
    
    <span data-ttu-id="23fc8-168">Medarbejderen skal opfylde alle angivne kriterier for at være berettiget til lønstrukturen.</span><span class="sxs-lookup"><span data-stu-id="23fc8-168">The employee must meet all specified criteria to be eligible for the compensation plan.</span></span> <span data-ttu-id="23fc8-169">Hvis du ikke angiver nogen kriterier, er alle medarbejdere berettiget til lønstrukturen.</span><span class="sxs-lookup"><span data-stu-id="23fc8-169">If you don't specify any criteria, all employees are eligible for the compensation plan.</span></span> <span data-ttu-id="23fc8-170">Hvis en medarbejder ikke opfylder de kriterier, der er angivet i berettigelsesreglen, eller er der ikke angivet en berettigelsesregel for en lønstruktur, vises lønstrukturen ikke i opslaget, når du opretter en post for fast løn for en medarbejder.</span><span class="sxs-lookup"><span data-stu-id="23fc8-170">If an employee doesn't meet the criteria specified in the eligibility rule, or an eligibility rule has not been specified for a compensation plan, the compensation plan won't appear in the lookup when you create a fixed compensation record for an employee.</span></span>

7. <span data-ttu-id="23fc8-171">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="23fc8-171">Close the page.</span></span>

8. <span data-ttu-id="23fc8-172">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="23fc8-172">Close the page.</span></span>

