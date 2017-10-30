---
title: Kompensationsplaner
description: "Ledere for kompensation og frynsegoder kan bruge kompensationsstyring til at vedligeholde og behandle faste og variable lønstrukturer for organisationens medarbejdere."
author: kherr75
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmCompensationLevel, HRCCompGrid, HRMCompFixedAction, HRMCompFixedBudget, HRMCompFixedPlanTable
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: kherr75
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: e57db8f4b692aa9c27916625897e268f63031782
ms.openlocfilehash: 321c6448770828f7a4eb46951193bcdf6370c7b1
ms.contentlocale: da-dk
ms.lasthandoff: 10/30/2017

---

# <a name="compensation-plans"></a><span data-ttu-id="7d207-103">Kompensationsplaner</span><span class="sxs-lookup"><span data-stu-id="7d207-103">Compensation plans</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="7d207-104">Ledere for kompensation og frynsegoder kan bruge kompensationsstyring til at vedligeholde og behandle faste og variable lønstrukturer for organisationens medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="7d207-104">Compensation and Benefits Managers can use Compensation management to maintain and process fixed and variable compensation plans for the organization's employees.</span></span>

### <a name="introduction"></a><span data-ttu-id="7d207-105">Introduktion</span><span class="sxs-lookup"><span data-stu-id="7d207-105">Introduction</span></span>

<span data-ttu-id="7d207-106">Kompensationsstyring bruges til at styre fordelingen af grundløn og bonusser.</span><span class="sxs-lookup"><span data-stu-id="7d207-106">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="7d207-107">En medarbejders faste grundløn og kvalifikationstillæg styres gennem faste lønstrukturer.</span><span class="sxs-lookup"><span data-stu-id="7d207-107">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="7d207-108">Betalingen af incitamentsløn som f.eks. bonusudbetalinger, præstationsbonusser, aktieoptioner og tildelte aktier samt engangsbonusser styres ved hjælp af variable lønstrukturer.</span><span class="sxs-lookup"><span data-stu-id="7d207-108">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span> 

<span data-ttu-id="7d207-109">Medarbejdere kan knyttes til en eller flere strukturer af begge typer.</span><span class="sxs-lookup"><span data-stu-id="7d207-109">Employees can be enrolled in one or more plans of both types.</span></span> <span data-ttu-id="7d207-110">En medarbejder skal opfylde følgende krav for at være berettiget til registrering i en lønstruktur:</span><span class="sxs-lookup"><span data-stu-id="7d207-110">An employee must meet the following requirements in order to be eligible for enrollment in a compensation plan:</span></span>
-   <span data-ttu-id="7d207-111">Medarbejderen skal have en aktiv stillingstildeling.</span><span class="sxs-lookup"><span data-stu-id="7d207-111">The employee must have an active position assignment.</span></span>
-   <span data-ttu-id="7d207-112">Medarbejderen skal opfylde de kriterier, der er defineret af berettigelsesreglerne for en lønstruktur.</span><span class="sxs-lookup"><span data-stu-id="7d207-112">The employee must meet the criteria that are defined by eligibility rules for a compensation plan.</span></span>

## <a name="compensation-setup"></a><span data-ttu-id="7d207-113">Lønkonfiguration</span><span class="sxs-lookup"><span data-stu-id="7d207-113">Compensation setup</span></span>
<span data-ttu-id="7d207-114">Følgende tabel viser de komponenter i lønprocessen, der kan være integreret i konfigurationen af virksomhedens lønstrukturer.</span><span class="sxs-lookup"><span data-stu-id="7d207-114">The following table lists components of the compensation process that can be integral in setting up your company's compensation plans.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="7d207-115">Komponent</span><span class="sxs-lookup"><span data-stu-id="7d207-115">Component</span></span></th>
<th><span data-ttu-id="7d207-116">Flere oplysninger...</span><span class="sxs-lookup"><span data-stu-id="7d207-116">More information…</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7d207-117">Fast løn-handlinger</span><span class="sxs-lookup"><span data-stu-id="7d207-117">Fixed compensation actions</span></span></td>
<td><span data-ttu-id="7d207-118">Fast løn-handlinger opfylder to formål:</span><span class="sxs-lookup"><span data-stu-id="7d207-118">Fixed compensation actions accomplish two purposes:</span></span>
<ul>
<li><span data-ttu-id="7d207-119">Handlinger kan angive den type oplysninger, der skal registreres, når en medarbejders kompensation ændres.</span><span class="sxs-lookup"><span data-stu-id="7d207-119">Actions can specify the kind of information that must be recorded when an employee’s compensation changes.</span></span> <span data-ttu-id="7d207-120">For eksempel kan du kræve, at årsagen til en ændring, f.eks en kampagne eller en sænkning, registreres.</span><span class="sxs-lookup"><span data-stu-id="7d207-120">For example, you can require that the reason a change, such as a promotion or a demotion be recorded.</span></span></li>
<li><span data-ttu-id="7d207-121">Handlinger kan sikre, at der anvendes en beregning, når faste lønstrukturer behandles.</span><span class="sxs-lookup"><span data-stu-id="7d207-121">Actions can ensure that a calculation is applied when fixed compensation plans are processed.</span></span>  <span data-ttu-id="7d207-122">Handlinger af typen Egenkapital sammenligner for eksempel medarbejderlønnen med minimumreferencepunktet for niveauet af medarbejderens og sikrer, at medarbejderen bliver betalt mindst minimum.</span><span class="sxs-lookup"><span data-stu-id="7d207-122">For example, actions of type Equity will compare the employees pay to the minimum reference point for the level on the employee's and ensure the employee is getting paid at least the minimum.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d207-123">Niveauer</span><span class="sxs-lookup"><span data-stu-id="7d207-123">Levels</span></span></td>
<td><span data-ttu-id="7d207-124">Niveauer er tilknyttet job og eventuelle stillinger, der er relateret til en jobreference.</span><span class="sxs-lookup"><span data-stu-id="7d207-124">Levels are associated with jobs and any positions that are related to a job reference.</span></span> <span data-ttu-id="7d207-125">Du kan oprette separate niveauer for de tre typer lønstrukturer: klasse, omfang eller trin.</span><span class="sxs-lookup"><span data-stu-id="7d207-125">You can create discrete levels for the three types of compensation plans: Grade, Band, and Step.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7d207-126">Rammeudnyttelsesmatrix</span><span class="sxs-lookup"><span data-stu-id="7d207-126">Range utilization matrix</span></span></td>
<td><span data-ttu-id="7d207-127">En rammeudnyttelsesmatrix hjælper dig med at overføre medarbejdere til deres jobkontrolpunkt.</span><span class="sxs-lookup"><span data-stu-id="7d207-127">A range utilization matrix helps you transition employees to the control point for their jobs.</span></span> <span data-ttu-id="7d207-128">Du kan også bruge rammeudnyttelse til at styre ligelønnen i virksomheden hensyn til den enkelte medarbejders præstation eller virksomhedens overordnede præstation.</span><span class="sxs-lookup"><span data-stu-id="7d207-128">You can also use range utilization to control pay rate equity in the company without regard to an individual employee's performance or the overall performance of the company.</span></span> <span data-ttu-id="7d207-129">For eksempel får medarbejdere, der få laverer løn i deres lønramme, en større procentvis stigninger end medarbejdere, der får en højere løn i lønrammen.</span><span class="sxs-lookup"><span data-stu-id="7d207-129">For example, employees who are paid lower in their range get higher percentage increases than employees who are paid higher in the range.</span></span> <span data-ttu-id="7d207-130">På denne måde kan du systematisk forskyde forskelle.</span><span class="sxs-lookup"><span data-stu-id="7d207-130">In this manner, you can systematically offset equity differences.</span></span> <span data-ttu-id="7d207-131">Rammeudnyttelsen beregnes på følgende måde: (Fast lønsats - Rammeminimum) ÷ (Rammemaksimum - Rammeminimum).</span><span class="sxs-lookup"><span data-stu-id="7d207-131">The range utilization is calculated as follows: (Fixed Pay Rate - Range Minimum) ÷ (Range Maximum - Range Minimum).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d207-132">Opsætninger af referencepunkter</span><span class="sxs-lookup"><span data-stu-id="7d207-132">Reference point setups</span></span></td>
<td><span data-ttu-id="7d207-133">Opsætning af et referencepunkt omfatter et sæt referencepunkter, der repræsenterer intervaller i en matrix.</span><span class="sxs-lookup"><span data-stu-id="7d207-133">A reference point setup includes a set of reference points that represent ranges in a matrix.</span></span> <span data-ttu-id="7d207-134">Hver ramme kan tilknyttes en lønsats.</span><span class="sxs-lookup"><span data-stu-id="7d207-134">Each range can be associated with a pay rate.</span></span> <span data-ttu-id="7d207-135">Lønklassestrukturer har eksempelvis ofte referencepunkter for minimum, midtpunkt og maksimum.</span><span class="sxs-lookup"><span data-stu-id="7d207-135">For example, grade plans will often have reference points of Minimum, Midpoint, and Maximum.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7d207-136">Kompensationsmatrix</span><span class="sxs-lookup"><span data-stu-id="7d207-136">Compensation matrix</span></span></td>
<td><span data-ttu-id="7d207-137">En kompensationsmatrix er det sæt referencepunkter og niveauer, du kan bruge til at oprette en lønstruktur.</span><span class="sxs-lookup"><span data-stu-id="7d207-137">A compensation matrix is the set of reference points and levels that you use to create a compensation structure.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d207-138">Kompensationsstruktur</span><span class="sxs-lookup"><span data-stu-id="7d207-138">Compensation structure</span></span></td>
<td><span data-ttu-id="7d207-139">En lønstruktur er en kompensationsmatrix med rammer, som har lønsatser, der er tilknyttet referencepunkterne for hvert niveau.</span><span class="sxs-lookup"><span data-stu-id="7d207-139">A compensation structure is a compensation matrix that has pay rates associated with the reference points for each level.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7d207-140">Berettigelsesregel</span><span class="sxs-lookup"><span data-stu-id="7d207-140">Eligibility rules</span></span></td>
<td><span data-ttu-id="7d207-141">Berettigelsesregler bruges til at identificere medarbejdere i bestemte job, jobfunktioner, jobtyper, afdelinger, fagforeninger eller kompensationsområder, der er omfattet af specifikke lønstrukturer.</span><span class="sxs-lookup"><span data-stu-id="7d207-141">Eligibility rules are used to identify employees in specific jobs, job functions, job types, departments, labor unions, or compensation regions that are covered by specific compensation plans.</span></span> <span data-ttu-id="7d207-142">Du skal oprette berettigelsesregler for både variable og faste lønstrukturer for at tilmelde medarbejdere til planen.</span><span class="sxs-lookup"><span data-stu-id="7d207-142">You must create eligibility rules for both variable and fixed compensation plans in order to enroll employees in the plan.</span></span> <span data-ttu-id="7d207-143">Når du har angivet berettigelsesreglerne for en lønstruktur, kan du definere niveauer, der skal gælde for de jobs, der er dækket af strukturen.</span><span class="sxs-lookup"><span data-stu-id="7d207-143">After eligibility rules are specified for a compensation plan, you can define the levels that should apply to the jobs that are covered by the plan.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d207-144">Lønfrekvenser</span><span class="sxs-lookup"><span data-stu-id="7d207-144">Pay frequencies</span></span></td>
<td><span data-ttu-id="7d207-145">Lønfrekvenser bruges til at definere den periode, godtgørelsen er angivet for.</span><span class="sxs-lookup"><span data-stu-id="7d207-145">Pay frequencies are used to define the time period for which the compensation is specified.</span></span>  <span data-ttu-id="7d207-146">For eksempel hjælper lønfrekvensen dig med at forstå, om kompensationsbeløbet er angivet som en årslån eller en timeløn.</span><span class="sxs-lookup"><span data-stu-id="7d207-146">For example, the pay frequency helps you understand if the compensation amount is specified as an annual salary versus an hourly pay rate.</span></span> <span data-ttu-id="7d207-147">Lønfrekvenser bruges også til at konfigurere omregningsfaktorer til konvertering af kompensationsbeløb fra pr. måned, uge, 14 dage og time til en årlig lønfrekvens.</span><span class="sxs-lookup"><span data-stu-id="7d207-147">Pay frequencies are also used to set up conversion factors to convert compensation amounts from monthly, weekly, biweekly and hourly pay frequencies to an annual pay frequency.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7d207-148">Kompensationsområder</span><span class="sxs-lookup"><span data-stu-id="7d207-148">Compensation regions</span></span></td>
<td><span data-ttu-id="7d207-149">Kompensationsområder bruges til at angive medarbejderkompensation baseret på arbejdsstedets placering.</span><span class="sxs-lookup"><span data-stu-id="7d207-149">Compensation regions are used to specify employee compensation based on the location of the workplace.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d207-150">Referencepunkt</span><span class="sxs-lookup"><span data-stu-id="7d207-150">Control point</span></span></td>
<td><span data-ttu-id="7d207-151">Referencepunktet definerer, hvad du mener er den ideelle lønsats for alle medarbejdere på et kompensationsniveau.</span><span class="sxs-lookup"><span data-stu-id="7d207-151">The control point defines what you consider to be the ideal pay rate for all employees at a compensation level.</span></span> <span data-ttu-id="7d207-152">For planstrukturer for trin er referencepunkterne typisk rammens midtpunkt.</span><span class="sxs-lookup"><span data-stu-id="7d207-152">For grade plan structures, control points are typically the midpoint of the ranges.</span></span> <span data-ttu-id="7d207-153">Tværgående strukturer bruger sjældent kontrolpunkter.</span><span class="sxs-lookup"><span data-stu-id="7d207-153">Band structures rarely use control points.</span></span> <span data-ttu-id="7d207-154">Du kan angive kontrolpunktet til en fast lønstruktur i formularen Faste lønstrukturer.</span><span class="sxs-lookup"><span data-stu-id="7d207-154">You can specify the control point for a fixed compensation plan in the Fixed compensation plans form.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7d207-155">Jobfunktioner</span><span class="sxs-lookup"><span data-stu-id="7d207-155">Job functions</span></span></td>
<td><span data-ttu-id="7d207-156">Jobfunktioner, der bruges til at klassificere og filtrere kompensationsstrukturer til specifikke job.</span><span class="sxs-lookup"><span data-stu-id="7d207-156">Job functions are used to classify and filter compensation plans to specific jobs.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d207-157">Jobtyper</span><span class="sxs-lookup"><span data-stu-id="7d207-157">Job types</span></span></td>
<td><span data-ttu-id="7d207-158">Jobtyper, der bruges til at klassificere og filtrere kompensationsstrukturer til specifikke job.</span><span class="sxs-lookup"><span data-stu-id="7d207-158">Job types are used to classify and filter compensation plans to specific jobs.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7d207-159">Variable kompensationstyper</span><span class="sxs-lookup"><span data-stu-id="7d207-159">Variable compensation types</span></span></td>
<td><span data-ttu-id="7d207-160">Variabel løn-typer, f.eks. kontantbonusser og aktiebonusser, konfigureres i variable lønstrukturer.</span><span class="sxs-lookup"><span data-stu-id="7d207-160">Variable compensation types, such as stock awards or cash award bonuses, are set up in variable compensation plans.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d207-161">Kompensationsgitre</span><span class="sxs-lookup"><span data-stu-id="7d207-161">Compensation grids</span></span></td>
<td><span data-ttu-id="7d207-162">Kompensationsgitre indeholder kompensationsstrukturen.</span><span class="sxs-lookup"><span data-stu-id="7d207-162">Compensation grids contain the compensation structure.</span></span>  <span data-ttu-id="7d207-163">Kompensationsgitre kan bruges af en eller flere kompensationsplaner.</span><span class="sxs-lookup"><span data-stu-id="7d207-163">Compensation grids can be used by one or more compensation plans.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7d207-164">Performance-planer</span><span class="sxs-lookup"><span data-stu-id="7d207-164">Performance plans</span></span></td>
<td><span data-ttu-id="7d207-165">Performance-planer bruges til at knytte performance til en fordelingsmatrix, så du kan bruge planen i en strategi for præstationsløn.</span><span class="sxs-lookup"><span data-stu-id="7d207-165">Performance plans are used to associate performance with an allocation matrix, so that you can use the plan in a pay-for-performance strategy.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d207-166">Performance-rangeringer</span><span class="sxs-lookup"><span data-stu-id="7d207-166">Performance ratings</span></span></td>
<td><span data-ttu-id="7d207-167">Performance-rangeringer bruges i performanceplaner til at bestemme beløbet for en meritbonus eller en performancebonus.</span><span class="sxs-lookup"><span data-stu-id="7d207-167">Performance ratings are used in performance plans to determine the amount of a merit award or performance award.</span></span></td>
</tr>
</tbody>
</table>

## <a name="process-events"></a><span data-ttu-id="7d207-168">Proceshændelser</span><span class="sxs-lookup"><span data-stu-id="7d207-168">Process events</span></span>
<span data-ttu-id="7d207-169">En proceshændelse beregner lønoplysninger for en bestemt periode for alle medarbejdere, der er tilmeldt en eller flere strukturer for fast eller variabel løn.</span><span class="sxs-lookup"><span data-stu-id="7d207-169">A process event calculates compensation information for a specific period for all employees who are enrolled in one or more fixed or variable compensation plans.</span></span> <span data-ttu-id="7d207-170">Du kan køre en proceshændelse gentagne gange for at teste eller opdatere beregnede lønresultater.</span><span class="sxs-lookup"><span data-stu-id="7d207-170">You can run a process event repeatedly to test or update calculated compensation results.</span></span>

<a name="compensation-events"></a><span data-ttu-id="7d207-171">Kompensationshændelser</span><span class="sxs-lookup"><span data-stu-id="7d207-171">Compensation events</span></span>
-------------------

<span data-ttu-id="7d207-172">Hver gang en proceshændelse afvikles, oprettes der en kompensationshændelse.</span><span class="sxs-lookup"><span data-stu-id="7d207-172">Each time a process event is run, a compensation event is created.</span></span>  <span data-ttu-id="7d207-173">Kompensationshændelser indeholder resultaterne af kompensationsprocessen for hver medarbejder, der er inkluderet i denne proceshændelse.</span><span class="sxs-lookup"><span data-stu-id="7d207-173">Compensation events contain the results of the compensation process for each employee included in that process event.</span></span>  <span data-ttu-id="7d207-174">Når disse beregninger er korrekte, kan du indlæse kompensationshændelsen for at opdatere lønposterne for de medarbejdere, der er berørt af proceshændelsen.</span><span class="sxs-lookup"><span data-stu-id="7d207-174">When the calculations are correct, you can load the compensation event to update the compensation records for the employees who are affected by the process event.</span></span>

## <a name="recommendations"></a><span data-ttu-id="7d207-175">Anbefalinger</span><span class="sxs-lookup"><span data-stu-id="7d207-175">Recommendations</span></span>
<span data-ttu-id="7d207-176">Når du har kørt en proceshændelse, kan du anbefale justeringer i en medarbejders meritforøgelse eller bonusbeløb baseret på de beregnede retningslinjer for proceshændelsen.</span><span class="sxs-lookup"><span data-stu-id="7d207-176">After you run a process event, you can recommend adjustments to an employee’s merit increase or award amount, based on the calculated guidelines of the process event.</span></span> <span data-ttu-id="7d207-177">For at angive anbefalinger for medarbejdere skal du aktivere anbefalinger, når du opretter lønstrukturer, eller når du konfigurerer proceshændelsen.</span><span class="sxs-lookup"><span data-stu-id="7d207-177">To make recommendations for employees, you must enable recommendations when you set up compensation plans or when you set up the process event.</span></span>




