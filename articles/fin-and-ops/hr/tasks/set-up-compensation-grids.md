--- 
title: Konfigurere kompensationsgitre
description: "Kompensationsgitre bruges til at definere og vedligeholde lønstrukturerne for fast løn-planer."
author: kherr75
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 258149dbd610dafb8daacaf54c61e69898ca35d6
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-compensation-grids"></a><span data-ttu-id="5dae8-103">Konfigurere kompensationsgitre</span><span class="sxs-lookup"><span data-stu-id="5dae8-103">Set up compensation grids</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5dae8-104">Kompensationsgitre bruges til at definere og vedligeholde lønstrukturerne for fast løn-planer.</span><span class="sxs-lookup"><span data-stu-id="5dae8-104">Compensation grids are used to define and maintain the pay structures for fixed compensation plans.</span></span> <span data-ttu-id="5dae8-105">Kompensationsgitre kan deles mellem flere planer eller kopieres, når du opretter en ny lønstruktur.</span><span class="sxs-lookup"><span data-stu-id="5dae8-105">Compensation grids can be shared between multiple plans or copied when creating a new compensation plan.</span></span>  <span data-ttu-id="5dae8-106">Før du opretter et kompensationsgitteret, skal niveauer og referencepunkter konfigureres.</span><span class="sxs-lookup"><span data-stu-id="5dae8-106">Before creating a compensation grid, Levels and Reference points must be set up.</span></span> <span data-ttu-id="5dae8-107">I dette eksempel oprettes der en ny klassetype for kompensationsgitteret ved hjælp af demodata for niveauerne og referencepunkter.</span><span class="sxs-lookup"><span data-stu-id="5dae8-107">This example will create a new Grade type of compensation grid using demo data for the Levels and Reference points.</span></span> <span data-ttu-id="5dae8-108">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="5dae8-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-information-about-the-compensation-grid"></a><span data-ttu-id="5dae8-109">Konfigurer oplysninger om kompensationsgitteret</span><span class="sxs-lookup"><span data-stu-id="5dae8-109">Set up information about the compensation grid</span></span>
1. <span data-ttu-id="5dae8-110">Gå til Personale > Kompensation > Fast løn > Kompensationsgitre.</span><span class="sxs-lookup"><span data-stu-id="5dae8-110">Go to Human resources > Compensation > Fixed compensation > Compensation grids.</span></span>
2. <span data-ttu-id="5dae8-111">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="5dae8-111">Click New.</span></span>
3. <span data-ttu-id="5dae8-112">Skriv en værdi i feltet Gitter.</span><span class="sxs-lookup"><span data-stu-id="5dae8-112">In the Grid field, type a value.</span></span>
4. <span data-ttu-id="5dae8-113">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="5dae8-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="5dae8-114">Vælg en indstilling i feltet Type.</span><span class="sxs-lookup"><span data-stu-id="5dae8-114">In the Type field, select an option.</span></span>
6. <span data-ttu-id="5dae8-115">Indtast eller vælg en værdi i feltet Opsætning af reference.</span><span class="sxs-lookup"><span data-stu-id="5dae8-115">In the Reference setup field, enter or select a value.</span></span>
7. <span data-ttu-id="5dae8-116">Indtast eller vælg en værdi i feltet Valuta.</span><span class="sxs-lookup"><span data-stu-id="5dae8-116">In the Currency field, enter or select a value.</span></span>
8. <span data-ttu-id="5dae8-117">Skriv en værdi i feltet Valuta.</span><span class="sxs-lookup"><span data-stu-id="5dae8-117">In the Currency field, type a value.</span></span>
9. <span data-ttu-id="5dae8-118">Angiv en dato i feltet Ikrafttrædelsesdato.</span><span class="sxs-lookup"><span data-stu-id="5dae8-118">In the Effective date field, enter a date.</span></span>

## <a name="add-levels-to-the-compensation-structure"></a><span data-ttu-id="5dae8-119">Føje niveauer til kompensationsstrukturen</span><span class="sxs-lookup"><span data-stu-id="5dae8-119">Add levels to the compensation structure</span></span>
1. <span data-ttu-id="5dae8-120">Klik på Kompensationsstruktur.</span><span class="sxs-lookup"><span data-stu-id="5dae8-120">Click Compensation structure.</span></span>
2. <span data-ttu-id="5dae8-121">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="5dae8-121">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="5dae8-122">Indtast eller vælg en værdi i feltet Niveau.</span><span class="sxs-lookup"><span data-stu-id="5dae8-122">In the Level field, enter or select a value.</span></span>
4. <span data-ttu-id="5dae8-123">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="5dae8-123">Click New.</span></span>
5. <span data-ttu-id="5dae8-124">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="5dae8-124">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="5dae8-125">Indtast eller vælg en værdi i feltet Niveau.</span><span class="sxs-lookup"><span data-stu-id="5dae8-125">In the Level field, enter or select a value.</span></span>
7. <span data-ttu-id="5dae8-126">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="5dae8-126">Click New.</span></span>
8. <span data-ttu-id="5dae8-127">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="5dae8-127">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="5dae8-128">Indtast eller vælg en værdi i feltet Niveau.</span><span class="sxs-lookup"><span data-stu-id="5dae8-128">In the Level field, enter or select a value.</span></span>
10. <span data-ttu-id="5dae8-129">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="5dae8-129">Click New.</span></span>
11. <span data-ttu-id="5dae8-130">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="5dae8-130">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="5dae8-131">Indtast eller vælg en værdi i feltet Niveau.</span><span class="sxs-lookup"><span data-stu-id="5dae8-131">In the Level field, enter or select a value.</span></span>
13. <span data-ttu-id="5dae8-132">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="5dae8-132">Click New.</span></span>
14. <span data-ttu-id="5dae8-133">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="5dae8-133">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="5dae8-134">Indtast eller vælg en værdi i feltet Niveau.</span><span class="sxs-lookup"><span data-stu-id="5dae8-134">In the Level field, enter or select a value.</span></span>

## <a name="fill-in-the-compensation-structure-with-values"></a><span data-ttu-id="5dae8-135">Udfyld kompensationsstrukturen med værdier</span><span class="sxs-lookup"><span data-stu-id="5dae8-135">Fill in the compensation structure with values</span></span>
1. <span data-ttu-id="5dae8-136">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="5dae8-136">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="5dae8-137">På dette tidspunkt kan kompensationsværdier manuelt indtastes i hvert felt i tabellen, eller masseændringsfunktionen kan bruges til nemt at udfylde flere felter og udføre grundlæggende beregninger.</span><span class="sxs-lookup"><span data-stu-id="5dae8-137">At this point, compensation values can manually be entered into each field in the table, or the Mass change functionality can be used to easily fill in multiple fields and perform basic calculations.</span></span>  
2. <span data-ttu-id="5dae8-138">Klik på Masseændring.</span><span class="sxs-lookup"><span data-stu-id="5dae8-138">Click Mass change.</span></span>
    * <span data-ttu-id="5dae8-139">For dette gitter vil vi først anvende værdien af midtpunktet på første niveau på alle felter i tabellen.</span><span class="sxs-lookup"><span data-stu-id="5dae8-139">For this grid, we'll first apply the value for the midpoint of the first level's to all the fields in the table.</span></span> <span data-ttu-id="5dae8-140">Dette er grundlaget for kompensationsmatrixen.</span><span class="sxs-lookup"><span data-stu-id="5dae8-140">This will be the basis for the compensation matrix.</span></span>  
3. <span data-ttu-id="5dae8-141">Vælg en indstilling i feltet Reguleringstype.</span><span class="sxs-lookup"><span data-stu-id="5dae8-141">In the Adjustment type field, select an option.</span></span>
4. <span data-ttu-id="5dae8-142">Indtast et tal i feltet Justeringsbeløb.</span><span class="sxs-lookup"><span data-stu-id="5dae8-142">In the Adjustment amount field, enter a number.</span></span>
5. <span data-ttu-id="5dae8-143">Markér eller fjern markeringen af alle rækker på listen.</span><span class="sxs-lookup"><span data-stu-id="5dae8-143">In the list, mark or unmark all rows.</span></span>
6. <span data-ttu-id="5dae8-144">Klik på Anvend på gitter.</span><span class="sxs-lookup"><span data-stu-id="5dae8-144">Click Apply to grid.</span></span>
    * <span data-ttu-id="5dae8-145">Nu bruger vi masseændringsfunktionen til at forøge beløbene i hvert efterfølgende niveau med en bestemt procentdel eller et beløb.</span><span class="sxs-lookup"><span data-stu-id="5dae8-145">Now we'll use the mass change function to increment the amounts in each subsequent level by a certain percentage or amount.</span></span> <span data-ttu-id="5dae8-146">I dette eksempel har hver lønklasse et 12,5% opslag mellem sine midtpunkter.</span><span class="sxs-lookup"><span data-stu-id="5dae8-146">In this example, each grade will have a 12.5% spread between their midpoints.</span></span>  
7. <span data-ttu-id="5dae8-147">Vælg en indstilling i feltet Reguleringstype.</span><span class="sxs-lookup"><span data-stu-id="5dae8-147">In the Adjustment type field, select an option.</span></span>
8. <span data-ttu-id="5dae8-148">Indtast et tal i feltet Justeringsbeløb.</span><span class="sxs-lookup"><span data-stu-id="5dae8-148">In the Adjustment amount field, enter a number.</span></span>
9. <span data-ttu-id="5dae8-149">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="5dae8-149">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="5dae8-150">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="5dae8-150">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="5dae8-151">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="5dae8-151">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="5dae8-152">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="5dae8-152">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="5dae8-153">Klik på Anvend på gitter.</span><span class="sxs-lookup"><span data-stu-id="5dae8-153">Click Apply to grid.</span></span>
14. <span data-ttu-id="5dae8-154">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="5dae8-154">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="5dae8-155">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="5dae8-155">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="5dae8-156">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="5dae8-156">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="5dae8-157">Klik på Anvend på gitter.</span><span class="sxs-lookup"><span data-stu-id="5dae8-157">Click Apply to grid.</span></span>
18. <span data-ttu-id="5dae8-158">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="5dae8-158">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="5dae8-159">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="5dae8-159">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="5dae8-160">Klik på Anvend på gitter.</span><span class="sxs-lookup"><span data-stu-id="5dae8-160">Click Apply to grid.</span></span>
21. <span data-ttu-id="5dae8-161">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="5dae8-161">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="5dae8-162">Klik på Anvend på gitter.</span><span class="sxs-lookup"><span data-stu-id="5dae8-162">Click Apply to grid.</span></span>
    * <span data-ttu-id="5dae8-163">Nu skal vi bruge masseændringsfunktionen til at justere minimum og maksimumreferencepunkter for hvert niveau.</span><span class="sxs-lookup"><span data-stu-id="5dae8-163">Now we'll use the mass change function to adjust the Minimum and Maximum reference points for each level.</span></span> <span data-ttu-id="5dae8-164">I dette eksempel bruger vi et opslag med 50%, så minimumreferencepunktet reguleres -20% og maksimumopslaget bliver reguleret +20%.</span><span class="sxs-lookup"><span data-stu-id="5dae8-164">This example will use a 50% spread so the Minimum reference point will be adjusted -20% and the Maximum will be adjusted +20%.</span></span>  
23. <span data-ttu-id="5dae8-165">Indtast et tal i feltet Justeringsbeløb.</span><span class="sxs-lookup"><span data-stu-id="5dae8-165">In the Adjustment amount field, enter a number.</span></span>
24. <span data-ttu-id="5dae8-166">Indtast eller vælg en værdi i feltet Referencepunkt.</span><span class="sxs-lookup"><span data-stu-id="5dae8-166">In the Reference point field, enter or select a value.</span></span>
25. <span data-ttu-id="5dae8-167">Markér eller fjern markeringen af alle rækker på listen.</span><span class="sxs-lookup"><span data-stu-id="5dae8-167">In the list, mark or unmark all rows.</span></span>
26. <span data-ttu-id="5dae8-168">Klik på Anvend på gitter.</span><span class="sxs-lookup"><span data-stu-id="5dae8-168">Click Apply to grid.</span></span>
27. <span data-ttu-id="5dae8-169">Indtast et tal i feltet Justeringsbeløb.</span><span class="sxs-lookup"><span data-stu-id="5dae8-169">In the Adjustment amount field, enter a number.</span></span>
28. <span data-ttu-id="5dae8-170">Indtast eller vælg en værdi i feltet Referencepunkt.</span><span class="sxs-lookup"><span data-stu-id="5dae8-170">In the Reference point field, enter or select a value.</span></span>
29. <span data-ttu-id="5dae8-171">Markér eller fjern markeringen af alle rækker på listen.</span><span class="sxs-lookup"><span data-stu-id="5dae8-171">In the list, mark or unmark all rows.</span></span>
30. <span data-ttu-id="5dae8-172">Klik på Anvend på gitter.</span><span class="sxs-lookup"><span data-stu-id="5dae8-172">Click Apply to grid.</span></span>


