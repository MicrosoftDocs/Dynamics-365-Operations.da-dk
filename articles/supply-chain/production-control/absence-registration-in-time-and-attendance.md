---
title: Fraværsregistrering i Tid og fremmøde
description: I dette emne forklares, hvordan du håndterer fraværsregistreringer i Tid og fremmøde.
author: johanhoffmann
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JMGParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a076ade51ad295886bef747302c4874ef09d3fa7
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203267"
---
# <a name="absence-registration-in-time-and-attendance"></a><span data-ttu-id="6e7a7-103">Fraværsregistrering i Tid og fremmøde</span><span class="sxs-lookup"><span data-stu-id="6e7a7-103">Absence registration in Time and attendance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6e7a7-104">I dette emne beskrives begreberne for fravær, og det forklares, hvordan du håndterer fravær i Tid og fremmøde.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-104">This topic describes the concepts for absence and explains how to handle absence in Time and attendance.</span></span>

## <a name="absence-that-is-based-on-regular-work-hours"></a><span data-ttu-id="6e7a7-105">Fravær, der er baseret på almindelig arbejdstid</span><span class="sxs-lookup"><span data-stu-id="6e7a7-105">Absence that is based on regular work hours</span></span>

<span data-ttu-id="6e7a7-106">Arbejdere betragtes som fraværende i alle timer, hvor de ikke arbejder i deres almindelig arbejdstid.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-106">Workers are considered absent for any hours that they don't work during their regular work hours.</span></span> <span data-ttu-id="6e7a7-107">Almindelig arbejdstid er defineret i en arbejders profil for normaltid.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-107">Regular work hours are defined in a worker's standard time profile.</span></span>

<span data-ttu-id="6e7a7-108">En arbejder har f.eks. arbejde på en dagprofil, der har mødetid 7.00 og sluttid 15.00.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-108">For example, a worker is working on a day profile that has clock-in at 7:00 AM and clock-out at 3:00 PM.</span></span> <span data-ttu-id="6e7a7-109">Hvis arbejderen møder 9.00, betragtes han fraværende fra 7.00 til 9.00 på den pågældende dag.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-109">If the worker clocks in at 9:00 AM, he is considered absent from 7:00 AM to 9:00 AM on that day.</span></span>

<span data-ttu-id="6e7a7-110">I så fald bliver arbejderne bedt om at angive en årsag til deres fravær.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-110">In this case, workers are prompted to enter a reason for their absence.</span></span> <span data-ttu-id="6e7a7-111">De kan angive en årsag ved at vælge en fraværskode.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-111">They can specify a reason by selecting an absence code.</span></span>

## <a name="absence-codes"></a><span data-ttu-id="6e7a7-112">Fraværskoder</span><span class="sxs-lookup"><span data-stu-id="6e7a7-112">Absence codes</span></span>

<span data-ttu-id="6e7a7-113">Fraværskoder definerer de forskellige typer fravær.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-113">Absence codes define the various types of absence.</span></span> <span data-ttu-id="6e7a7-114">Fraværskoder defineres af firmaet.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-114">Absence codes are defined by the company.</span></span>

<span data-ttu-id="6e7a7-115">Forskellige regler kan anvendes til fraværskoder.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-115">Various rules can be applied to absence codes.</span></span> <span data-ttu-id="6e7a7-116">F.eks. kan en fraværskode konfigureres til at trække eller give løn.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-116">For example, an absence code can be configured to deduct or grant pay.</span></span>

<span data-ttu-id="6e7a7-117">En virksomhed definerer f.eks. fraværskoden **For sent**, som arbejdere bruger, hvis de kommer sent og ikke har en god grund.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-117">For example, a company defines a **Late** absence code that workers use if they come in late and don't have a good reason.</span></span> <span data-ttu-id="6e7a7-118">Virksomheden definerer også fraværskoden **Internt kursus**, som arbejdere bruger for tid, som de bruger på at deltage i interne kurser.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-118">The company also defines an **Internal course** absence code that workers use for time that they spend attending internal courses.</span></span> <span data-ttu-id="6e7a7-119">Disse fraværskoder kan konfigureres, så **For sent** trækker fra arbejderens løn, men **Internt kursus** ikke trækker fra en arbejders løn.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-119">These absence codes can be set up so that **Late** deducts from a worker's pay but **Internal course** doesn't deduct from a worker's pay.</span></span>

<span data-ttu-id="6e7a7-120">Du kan konfigurere automatiske fraværkskoder.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-120">You can set up automatic absence codes.</span></span> <span data-ttu-id="6e7a7-121">Disse fraværskoder kan bruges til at beregne en arbejders tid, når der ikke er registreret noget fravær.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-121">These absence codes can be used to calculate a worker's time when no absence is registered.</span></span> <span data-ttu-id="6e7a7-122">Arbejderens arbejdstidsprofil bestemmer, om fraværskoden for normaltid eller flekstid bruges.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-122">The worker's time profile determines whether the absence code for standard time or flex time is used.</span></span>

### <a name="set-up-standard-time-and-flex-time"></a><span data-ttu-id="6e7a7-123">Opsætning af normaltid og flekstid</span><span class="sxs-lookup"><span data-stu-id="6e7a7-123">Set up standard time and flex time</span></span>

- <span data-ttu-id="6e7a7-124">Konfigurer parametrene for standardtid og flekstid ved hjælp af indstillingerne **Automatisk indsættelse af fravær** og **Automatisk indsættelse af fleks -** på siden **Parametre for tid og fremmøde**.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-124">Configure the parameters for standard time and flex time by using the **Auto insert absence** and **Auto insert Flex-** options on the **Time and attendance parameters** page.</span></span>

## <a name="absence-groups"></a><span data-ttu-id="6e7a7-125">Fraværsgrupper</span><span class="sxs-lookup"><span data-stu-id="6e7a7-125">Absence groups</span></span>

<span data-ttu-id="6e7a7-126">Fraværskoder er grupperet i fraværsgrupper.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-126">Absence codes are grouped into absence groups.</span></span> <span data-ttu-id="6e7a7-127">Du kan bruge fraværsgrupper til at gruppere fraværskoder, der har fælles karakteristika.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-127">You use absence groups to group absence codes that have common characteristics.</span></span> <span data-ttu-id="6e7a7-128">Eksemplerne omfatter fraværskoderne for et gyldigt fravær eller fravær på grund af en lægeaftale, deltagelse i jury eller barns sygdom.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-128">Examples include absence codes for a legal absence, or absence because of a doctor's appointment, jury duty, or a sick child.</span></span>

## <a name="planned-absence"></a><span data-ttu-id="6e7a7-129">Planlagt fravær</span><span class="sxs-lookup"><span data-stu-id="6e7a7-129">Planned absence</span></span>

<span data-ttu-id="6e7a7-130">Hvis du ved, at en arbejder vil være fraværende i en periode, f.eks. en kommende ferie, kan du bruge planlagt fravær.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-130">If you know that a worker will be absent for a period, such as an upcoming vacation, you can use planned absence.</span></span> <span data-ttu-id="6e7a7-131">Du kan oprette planlagt fravær ved at konfigurere fraværskoden, så den tager højde for det planlagte fravær.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-131">You set up planned absence by configuring the absence code so that it considers the planned absence.</span></span> <span data-ttu-id="6e7a7-132">Når du opretter et planlagt fravær, bliver du ikke bedt om en fraværskode i fraværsperioden, når tidsregistreringer for brugeren beregnes.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-132">When you set up a planned absence, you aren't prompted for an absence code during the absence period when user time registrations are calculated.</span></span> <span data-ttu-id="6e7a7-133">Planlagt fravær kan defineres for en enkelt arbejder, eller du kan definere et batchjob til masseopdatering af planlagt fravær for arbejdere.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-133">Planned absence can be defined for a single worker, or you can define a batch job to bulk update the planned absence for workers.</span></span>

### <a name="set-up-planned-absence"></a><span data-ttu-id="6e7a7-134">Konfigurer planlagt fravær</span><span class="sxs-lookup"><span data-stu-id="6e7a7-134">Set up planned absence</span></span>

1. <span data-ttu-id="6e7a7-135">Vælg **Personale** &gt; **Arbejdere** &gt; **Medarbejdere**, og vælg en medarbejder.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-135">Select **Human resources** &gt; **Workers** &gt; **Employees**, and select an employee.</span></span>
2. <span data-ttu-id="6e7a7-136">Vælg **Tid** &gt; **Tidstildelinger** &gt; **Fraværsregistrering i tid**, og konfigurer det planlagte fravær.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-136">Select **Time** &gt; **Time assignments** &gt; **Time Absence registration**, and set up the planned absence.</span></span>

## <a name="interrupted-planned-absence"></a><span data-ttu-id="6e7a7-137">Afbrudt planlagt fravær</span><span class="sxs-lookup"><span data-stu-id="6e7a7-137">Interrupted planned absence</span></span>

<span data-ttu-id="6e7a7-138">Hvis du anvender indstillingen **Afbryd**, når du opretter et planlagt fravær, afbrydes det planlagte fravær, hvis arbejderen logger på, under den planlagte fraværsperiode.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-138">If you apply the **Interrupt** option when you set up a planned absence, the planned absence will be interrupted if the worker signs in during the planned absence period.</span></span> <span data-ttu-id="6e7a7-139">Det planlagte fravær markeres som **Afbrudt** og har ingen indflydelse på fremtidige beregninger.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-139">The planned absence will be marked as **Interrupted** and won't have any effect on future calculations.</span></span>

### <a name="set-up-a-planned-absence-for-interruption"></a><span data-ttu-id="6e7a7-140">Konfigurere et planlagt fravær til afbrydelse</span><span class="sxs-lookup"><span data-stu-id="6e7a7-140">Set up a planned absence for interruption</span></span>

1. <span data-ttu-id="6e7a7-141">Åbn siden **Fraværsregistrering i tid**, som beskrevet i proceduren til opsætning af planlagt fravær.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-141">Open the **Time Absence registration** page as described in the procedure for setting up planned absence.</span></span>
2. <span data-ttu-id="6e7a7-142">Vælg **Afbryd**.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-142">Select **Interrupt**.</span></span>

<span data-ttu-id="6e7a7-143">Indstillingen **Afbryd** gælder, når tiden registreres via produktionsterminalen eller produktionsenheden.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-143">The **Interrupt** option applies when time is registered through the shop floor terminal or the shop floor device.</span></span> <span data-ttu-id="6e7a7-144">Indstillingen gælder ikke, hvis registreringerne er angivet på beregnings- og godkendelsessiderne, eller på siden **Elektronisk timeseddel**.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-144">The option doesn't apply if the registrations are entered on the calculation and approval pages, or on the **Electronic timecard** page.</span></span>

## <a name="examples-of-the-use-of-absence-in-a-flex-profile"></a><span data-ttu-id="6e7a7-145">Eksempler på brugen af fravær i en fleksprofil</span><span class="sxs-lookup"><span data-stu-id="6e7a7-145">Examples of the use of absence in a flex profile</span></span>

<span data-ttu-id="6e7a7-146">De følgende tre eksempler viser, hvordan fravær beregnes i en profil, der har fleksperioder.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-146">The following three examples show how absence is calculated in a profile that has flex periods.</span></span>

<span data-ttu-id="6e7a7-147">Eksemplerne bruger følgende profil.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-147">The examples use the following profile.</span></span>

| <span data-ttu-id="6e7a7-148">Komme</span><span class="sxs-lookup"><span data-stu-id="6e7a7-148">Clock-in</span></span> | <span data-ttu-id="6e7a7-149">Normaltid</span><span class="sxs-lookup"><span data-stu-id="6e7a7-149">Standard time</span></span>    | <span data-ttu-id="6e7a7-150">Pause</span><span class="sxs-lookup"><span data-stu-id="6e7a7-150">Break</span></span>             | <span data-ttu-id="6e7a7-151">Normaltid</span><span class="sxs-lookup"><span data-stu-id="6e7a7-151">Standard time</span></span> | <span data-ttu-id="6e7a7-152">Fleks-</span><span class="sxs-lookup"><span data-stu-id="6e7a7-152">Flex-</span></span>        | <span data-ttu-id="6e7a7-153">Gå</span><span class="sxs-lookup"><span data-stu-id="6e7a7-153">Clock-out</span></span> | <span data-ttu-id="6e7a7-154">Fleks+</span><span class="sxs-lookup"><span data-stu-id="6e7a7-154">Flex+</span></span>        |
|----------|------------------|-------------------|---------------|--------------|-----------|--------------|
| <span data-ttu-id="6e7a7-155">8.00</span><span class="sxs-lookup"><span data-stu-id="6e7a7-155">8 AM</span></span>     | <span data-ttu-id="6e7a7-156">9.00 til 11.30</span><span class="sxs-lookup"><span data-stu-id="6e7a7-156">9 AM to 11:30 AM</span></span> | <span data-ttu-id="6e7a7-157">11.30 til 12.00</span><span class="sxs-lookup"><span data-stu-id="6e7a7-157">11:30 AM to 12 PM</span></span> | <span data-ttu-id="6e7a7-158">12.00 til 15.00</span><span class="sxs-lookup"><span data-stu-id="6e7a7-158">12 PM to 3 PM</span></span> | <span data-ttu-id="6e7a7-159">15.00 til 16.00</span><span class="sxs-lookup"><span data-stu-id="6e7a7-159">3 PM to 4 PM</span></span> | <span data-ttu-id="6e7a7-160">16.00</span><span class="sxs-lookup"><span data-stu-id="6e7a7-160">4 PM</span></span>      | <span data-ttu-id="6e7a7-161">16.00 til 18.00</span><span class="sxs-lookup"><span data-stu-id="6e7a7-161">4 PM to 6 PM</span></span> |

### <a name="example-1-signing-out-during-a-flex--period"></a><span data-ttu-id="6e7a7-162">Eksempel 1: Logger af i en fleksperiode</span><span class="sxs-lookup"><span data-stu-id="6e7a7-162">Example 1: Signing out during a Flex- period</span></span>

<span data-ttu-id="6e7a7-163">Arbejderen stempler ind kl. 8.00 og stempler ud på kl. 15.30.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-163">The worker clocks in at 8:00 AM and clocks out at 3:30 PM.</span></span> <span data-ttu-id="6e7a7-164">Fordi arbejderen i dette tilfælde stempler ud i en fleksperiode, beregnes der intet fravær, og der trækkes en halv time fra arbejderens flekssaldo.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-164">In this case, because the worker clocks out during a Flex- period, no absence is calculated, and half an hour is deducted from the worker's flex balance.</span></span>

### <a name="example-2-signing-out-in-during-standard-time-period"></a><span data-ttu-id="6e7a7-165">Eksempel 2: Logger af inden for perioden for normaltid</span><span class="sxs-lookup"><span data-stu-id="6e7a7-165">Example 2: Signing out in during Standard time period</span></span>

<span data-ttu-id="6e7a7-166">Arbejderen stempler ind kl. 8.00 og stempler ud på kl. 14.30.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-166">The worker clocks in at 8:00 AM and clocks out at 2:30 PM.</span></span> <span data-ttu-id="6e7a7-167">Fordi arbejderen i dette tilfælde stempler ud inden for perioden for normaltid, beregnes fravær fra 14.30 til 16.00, og der registreres en fraværsperiode på 1,5 timer.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-167">In this case, because the worker clocks out during the Standard time period, absence is calculated from 2:30 PM to 4 PM, and an absence period of 1.5 hours is registered.</span></span> <span data-ttu-id="6e7a7-168">Der kræves en fraværskode for den pågældende periode.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-168">An absence code for that period is required.</span></span>

### <a name="example-3-signing-out-during-a-flex-period"></a><span data-ttu-id="6e7a7-169">Eksempel 3: Logger af under en fleks+-periode</span><span class="sxs-lookup"><span data-stu-id="6e7a7-169">Example 3: Signing out during a Flex+ period</span></span>

<span data-ttu-id="6e7a7-170">Arbejderen stempler ind kl. 8.00 og stempler ud kl. 16.30.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-170">The worker clocks in at 8:00 AM and clocks out at 4:30 PM.</span></span> <span data-ttu-id="6e7a7-171">Fordi arbejderen i dette tilfælde stempler ud i en fleks+-periode, beregnes der intet fravær, og der lægges en halv time til arbejderens flekssaldo.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-171">In this case, because the worker clocks out during a Flex+ period, no absence is calculated, and half an hour is added to the worker's flex balance.</span></span>

## <a name="absence-in-the-calculation-and-approval-process"></a><span data-ttu-id="6e7a7-172">Fravær i processen til beregning og godkendelse</span><span class="sxs-lookup"><span data-stu-id="6e7a7-172">Absence in the calculation and approval process</span></span>

<span data-ttu-id="6e7a7-173">Tidsregistreringer for arbejderen skal beregnes og godkendes, før de kan overføres til et lønsystem som lønposter.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-173">Worker time registrations must be calculated and approved before they can be transferred to a payroll system as pay items.</span></span>

<span data-ttu-id="6e7a7-174">En godkender kan ændre en arbejders tidsregistreringer.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-174">An approver can change a worker's time registrations.</span></span> <span data-ttu-id="6e7a7-175">Godkenderen kan desuden ændre ethvert fravær, som arbejderen har registreret.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-175">The approver can even change any absence that the worker has registered.</span></span> <span data-ttu-id="6e7a7-176">Hvis godkenderen manuelt angiver en tidsperiode, der har en fraværskode, tilsidesættes fraværskoden for den pågældende periode ikke af standardfraværskoden fra parametrene i Tid og fremmøde.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-176">If the approver manually enters a time period that has an absence code, the absence code for that period isn't overridden by the default absence code from the Time and attendance parameters.</span></span>

<span data-ttu-id="6e7a7-177">En arbejder stempler f.eks. ind 10.00 og vælger en fraværskode, der angiver, at hun er forsinket.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-177">For example, a worker clocks in at 10 AM and selects an absence code that indicates that she is late.</span></span> <span data-ttu-id="6e7a7-178">Senere fortæller arbejderen sin arbejdsleder, at hun havde en lægeaftale fra 8.00 til 10.00.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-178">Later, the worker informs her supervisor that she had a doctor's appointment from 8 AM to 10 AM.</span></span> <span data-ttu-id="6e7a7-179">En lægeaftale bør ikke føre til et fradrag i arbejderens løn.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-179">A doctor's appointment should not cause a deduction in the worker's pay.</span></span> <span data-ttu-id="6e7a7-180">I dette tilfælde kan arbejdslederen derfor justere to timers fravær fra 8.00 til 10.00 ved manuelt at angive en fraværskode, der angiver sygdom i to timer.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-180">Therefore, in this case, the supervisor can adjust the two hours of absence from 8 AM to 10 AM by manually entering an absence code that indicates illness for those two hours.</span></span>

### <a name="calculate-and-approve-absence"></a><span data-ttu-id="6e7a7-181">Beregne og godkende fravær</span><span class="sxs-lookup"><span data-stu-id="6e7a7-181">Calculate and approve absence</span></span>

- <span data-ttu-id="6e7a7-182">Vælg **Tid og fremmøde** &gt; **Gennemse og godkend** &gt; **Godkend eller beregn**.</span><span class="sxs-lookup"><span data-stu-id="6e7a7-182">Select **Time attendance** &gt; **Review and approve** &gt; **Approve or Calculate**.</span></span>
