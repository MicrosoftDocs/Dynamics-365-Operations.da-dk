---
title: Nyheder eller ændringer i Dynamics 365 Human Resources (28. maj 2020)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7664afbd0b1fd4e2c9686053fa102d85809c0411
ms.sourcegitcommit: bd9ff0d28718d535356ffbe1cffaaf60310dd430
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/13/2020
ms.locfileid: "3555309"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-28-2020"></a><span data-ttu-id="b9881-103">Nyheder eller ændringer i Dynamics 365 Human Resources (28. maj 2020)</span><span class="sxs-lookup"><span data-stu-id="b9881-103">What's new or changed in Dynamics 365 Human Resources (May 28, 2020)</span></span>

<span data-ttu-id="b9881-104">I dette emne beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b9881-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="b9881-105">Ændringerne gælder for build nummer 8.1.3287.</span><span class="sxs-lookup"><span data-stu-id="b9881-105">Changes apply to build number 8.1.3287.</span></span> <span data-ttu-id="b9881-106">Tallene i parenteser i nogle overskrifter henviser til LCS-supportnumre som reference.</span><span class="sxs-lookup"><span data-stu-id="b9881-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="leaverequest-entity-doesnt-work-when-you-enable-multiple-types-per-leave-plan-447498"></a><span data-ttu-id="b9881-107">LeaveRequest-enheden fungerer ikke, når du aktiverer flere typer pr. orlovsplan (447498)</span><span class="sxs-lookup"><span data-stu-id="b9881-107">LeaveRequest entity doesn't work when you enable multiple types per leave plan (447498)</span></span>

<span data-ttu-id="b9881-108">Med denne ændring er **LeaveEnrollmentV2Entity** nu tilgængelig til at rette den fejl, der opstår, når du aktiverer flere orlovstyper.</span><span class="sxs-lookup"><span data-stu-id="b9881-108">With this change, the **LeaveEnrollmentV2Entity** is now available to correct the error that occurs when you enable multiple leave types.</span></span>

## <a name="batch-contention-reduction-feature-preview-446619"></a><span data-ttu-id="b9881-109">Funktion til reduktion af batchindhold (prøveversion) (446619)</span><span class="sxs-lookup"><span data-stu-id="b9881-109">Batch contention reduction feature (preview) (446619)</span></span>

<span data-ttu-id="b9881-110">Når du aktiverer denne funktion, kan du forvente en reduktion i blokeringen af batchstrukturtabeller, mens du vælger opgaver og afslutter job.</span><span class="sxs-lookup"><span data-stu-id="b9881-110">When you enable this feature, you can expect a reduction in blocking on batch framework tables while selecting tasks and finishing jobs.</span></span>

## <a name="updateconflict-while-saving-worker-prevents-editing-a-record-in-people-427915"></a><span data-ttu-id="b9881-111">UpdateConflict, der sparer arbejderen, forhindrer redigering af en post i People (427915)</span><span class="sxs-lookup"><span data-stu-id="b9881-111">UpdateConflict while saving worker prevents editing a record in People (427915)</span></span>

<span data-ttu-id="b9881-112">Denne ændring retter en fejl ved tilføjelse af en ny arbejder, med opdatering af adresseoplysninger og ændring af foretrukket sprog.</span><span class="sxs-lookup"><span data-stu-id="b9881-112">This change corrects an error when adding a new worker, updating address information, and changing language preference.</span></span> <span data-ttu-id="b9881-113">I dette entydige scenarie blev der vist en fejl, som angiver, at posten ikke kunne opdateres.</span><span class="sxs-lookup"><span data-stu-id="b9881-113">In this unique scenario, an error displayed indicating the record couldn't be updated.</span></span> 

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-to-resubmit-425407"></a><span data-ttu-id="b9881-114">Det var ikke muligt at føje en vedhæftet fil til en godkendt orlovsanmodning, der skulle sendes igen (425407)</span><span class="sxs-lookup"><span data-stu-id="b9881-114">Unable to add an attachment to an approved leave request to resubmit (425407)</span></span>

<span data-ttu-id="b9881-115">Denne ændring tillader nu, at der vedhæftes filer til godkendte orlovsanmodninger.</span><span class="sxs-lookup"><span data-stu-id="b9881-115">This change now allows attachments to approved leave requests.</span></span>

## <a name="user-can-enter-compensation-for-an-employee-in-a-different-legal-entity-form-409529"></a><span data-ttu-id="b9881-116">Brugeren kan angive kompensation for en medarbejder i en anden juridisk enheds formular (409529)</span><span class="sxs-lookup"><span data-stu-id="b9881-116">User can enter compensation for an employee in a different legal entity form (409529)</span></span>

<span data-ttu-id="b9881-117">Denne ændring deaktiverer kompensationsindstillingerne for at forhindre utilsigtet indtastning af kompensationsposter for den forkerte juridiske enhed.</span><span class="sxs-lookup"><span data-stu-id="b9881-117">This change disables compensation options to prevent inadvertent entry of compensation records for the wrong legal entity.</span></span>

## <a name="error-when-you-transfer-an-employee-and-the-worker-position-assignment-date-is-before-the-position-duration-429402"></a><span data-ttu-id="b9881-118">Fejl, når du overfører en medarbejder, og datoen for arbejderens stillingstildeling er før stillingens varighed (429402)</span><span class="sxs-lookup"><span data-stu-id="b9881-118">Error when you transfer an employee and the Worker position assignment date is before the position duration (429402)</span></span>

<span data-ttu-id="b9881-119">Fejlmeddelelser, når en medarbejder overføres i dette scenarie, er blevet opdateret, så de indeholder en bedre beskrivelse af de ændringer, der er nødvendige for at løse problemet.</span><span class="sxs-lookup"><span data-stu-id="b9881-119">Error messages when transferring an employee in this scenario have been updated to better describe the changes needed to correct the problem.</span></span>

## <a name="attachments-capabilities-in-employee-self-service-benefits-enrollment"></a><span data-ttu-id="b9881-120">Egenskaber for vedhæftede filer i tilmelding til frynsegoder i medarbejderselvbetjening</span><span class="sxs-lookup"><span data-stu-id="b9881-120">Attachments capabilities in Employee self service benefits enrollment</span></span>
 
<span data-ttu-id="b9881-121">Nu kan du tilføje vedhæftede filer under tilmeldingsprocessen for frynsegoder for hver enkelt plan, som medarbejderen tilmelder sig.</span><span class="sxs-lookup"><span data-stu-id="b9881-121">Now you can add attachments during the benefits enrollment process for each plan that the employee's enrolling in.</span></span> <span data-ttu-id="b9881-122">Du kan derefter få vist de vedhæftede filer i formularen **Frynsegode, som arbejderen er tilmeldt**.</span><span class="sxs-lookup"><span data-stu-id="b9881-122">You can then view the attachments within the **Worker enrolled benefit** form.</span></span>

## <a name="in-preview"></a><span data-ttu-id="b9881-123">Som eksempel</span><span class="sxs-lookup"><span data-stu-id="b9881-123">In preview</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="b9881-124">Human Resources-app i Teams</span><span class="sxs-lookup"><span data-stu-id="b9881-124">Human Resources application in Teams</span></span>

<span data-ttu-id="b9881-125">Medarbejderne kan få vist og anmode om fri fra arbejde i Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="b9881-125">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="b9881-126">De kan interagere med en bot for at oprette orlovsanmodninger.</span><span class="sxs-lookup"><span data-stu-id="b9881-126">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="b9881-127">Yderligere oplysninger finder du i [Human Resources-appen i Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span><span class="sxs-lookup"><span data-stu-id="b9881-127">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="leave-suspension"></a><span data-ttu-id="b9881-128">Forlad suspension</span><span class="sxs-lookup"><span data-stu-id="b9881-128">Leave suspension</span></span>

<span data-ttu-id="b9881-129">Du kan afbryde orlov og fravær i Human Resources for en medarbejder.</span><span class="sxs-lookup"><span data-stu-id="b9881-129">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="b9881-130">Når du suspendere orlov, stoppes orloven for de valgte orlovstyper.</span><span class="sxs-lookup"><span data-stu-id="b9881-130">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="b9881-131">Hvis suspensionen finder sted, når en periodisering er blevet behandlet, opretter suspensionen en forholdsmæssig justering til medarbejderens orlov.</span><span class="sxs-lookup"><span data-stu-id="b9881-131">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="b9881-132">Du kan finde flere oplysninger i [Suspender orlov](hr-leave-and-absence-suspend-leave.md).</span><span class="sxs-lookup"><span data-stu-id="b9881-132">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a><span data-ttu-id="b9881-133">Opdatere brugeroplevelsen for at angive, at periodiseringen er udsat (429550)</span><span class="sxs-lookup"><span data-stu-id="b9881-133">Update user experience to indicate that accrual is suspended (429550)</span></span>

<span data-ttu-id="b9881-134">Brugeroplevelsen indikerer nu, at periodiseringen er blevet suspenderet for en plan.</span><span class="sxs-lookup"><span data-stu-id="b9881-134">The user experience now indicates that the accrual has been suspended for a plan.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="b9881-135">Kommer snart</span><span class="sxs-lookup"><span data-stu-id="b9881-135">Coming soon</span></span>

## <a name="database-logging-in-preview-in-june"></a><span data-ttu-id="b9881-136">Databaselogning (i prøveversion i juni)</span><span class="sxs-lookup"><span data-stu-id="b9881-136">Database logging (in preview in June)</span></span>

<span data-ttu-id="b9881-137">Du kan bruge funktionen til databaselogning til at bestemme, hvilken tabel og hvilke felter der skal overvåges.</span><span class="sxs-lookup"><span data-stu-id="b9881-137">The database logging feature allows you to determine which table and fields should be monitored.</span></span> <span data-ttu-id="b9881-138">Du kan også bestemme, hvilke hændelser der skal udløse ændringssporing.</span><span class="sxs-lookup"><span data-stu-id="b9881-138">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="b9881-139">Du kan få vist forespørgselsfunktioner for at se disse ændringer over tid.</span><span class="sxs-lookup"><span data-stu-id="b9881-139">Inquiry capabilities are available to see these changes over time.</span></span>

## <a name="buy-and-sell-leave-in-preview-june-1"></a><span data-ttu-id="b9881-140">Købe og sælge orlov (i prøveversion d. 1. juni)</span><span class="sxs-lookup"><span data-stu-id="b9881-140">Buy and sell leave (in preview June 1)</span></span>

<span data-ttu-id="b9881-141">Nogle organisationer giver et frynsegode, der giver medarbejderne mulighed for at købe eller sælge deres orlov.</span><span class="sxs-lookup"><span data-stu-id="b9881-141">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="b9881-142">Denne proces styres ofte manuelt.</span><span class="sxs-lookup"><span data-stu-id="b9881-142">This process is often managed manually.</span></span> <span data-ttu-id="b9881-143">Denne funktion giver en mere automatiseret metode til at administrere politikker og anmodninger for personaleafdelingen, og den hjælper med at eliminere fejl, samtidig med at orlovsprocessen strømlines.</span><span class="sxs-lookup"><span data-stu-id="b9881-143">This feature provides a more automated way to manage policies and requests for the HR department, and it helps eliminate mistakes while streamlining the leave management process.</span></span> <span data-ttu-id="b9881-144">Du kan finde flere oplysninger i:</span><span class="sxs-lookup"><span data-stu-id="b9881-144">For more information, see:</span></span>

- [<span data-ttu-id="b9881-145">Administrere politikker for køb og salg af orlov</span><span class="sxs-lookup"><span data-stu-id="b9881-145">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="b9881-146">Købe og sælge orlov</span><span class="sxs-lookup"><span data-stu-id="b9881-146">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="b9881-147">DMF-enheder (Data Management Framework) til styring af frynsegoder</span><span class="sxs-lookup"><span data-stu-id="b9881-147">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="b9881-148">Enheder til håndtering af frynsegoder frigives.</span><span class="sxs-lookup"><span data-stu-id="b9881-148">Benefits management entities are releasing.</span></span> <span data-ttu-id="b9881-149">Med DMF-enheder kan du importere og eksportere data, så du nemt kan konfigurere frynsegodestyring.</span><span class="sxs-lookup"><span data-stu-id="b9881-149">DMF entities allow importing and exporting data to easily configure benefits management.</span></span> <span data-ttu-id="b9881-150">En skabelon til frynsegodestyring kan også bruges til at flytte data.</span><span class="sxs-lookup"><span data-stu-id="b9881-150">A Benefits management template will also be available to move data.</span></span> <span data-ttu-id="b9881-151">Skabelonen eksporterer og importerer dataene på en sekventiel måde for at respektere dataafhængigheder.</span><span class="sxs-lookup"><span data-stu-id="b9881-151">The template exports and imports the data in a sequential manner to respect data dependencies.</span></span>

## <a name="add-reason-code-to-accrual-suspensions-june-1"></a><span data-ttu-id="b9881-152">Føje årsagskoder til periodiseringssuspensioner (1. juni)</span><span class="sxs-lookup"><span data-stu-id="b9881-152">Add reason code to accrual suspensions (June 1)</span></span>

<span data-ttu-id="b9881-153">Årsagskoder er føjet til periodiseringssuspenderingen.</span><span class="sxs-lookup"><span data-stu-id="b9881-153">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules-june-1"></a><span data-ttu-id="b9881-154">Overføre regler (1. juni)</span><span class="sxs-lookup"><span data-stu-id="b9881-154">Carry forward rules (June 1)</span></span>

<span data-ttu-id="b9881-155">Du kan angive en orlovstype for overførselssaldi, hvor gennemførte reguleringer overføres.</span><span class="sxs-lookup"><span data-stu-id="b9881-155">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="b9881-156">Hvis en medarbejder f.eks. overfører 10 dage, kan du vælge en anden orlovstype for disse 10 dage.</span><span class="sxs-lookup"><span data-stu-id="b9881-156">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="b9881-157">Du kan finde flere oplysninger i [Konfigurere orlovs- og fraværstyper](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="b9881-157">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types-june-1"></a><span data-ttu-id="b9881-158">Suspendere orlovsperiodisering for angivne orlovstyper (1. juni)</span><span class="sxs-lookup"><span data-stu-id="b9881-158">Suspend leave accrual for specified leave types (June 1)</span></span>

<span data-ttu-id="b9881-159">I denne udgave kan HR oprette en regel om periodiseringer for suspendering af orlov for medarbejdere med orlovsanmodninger, der er angivet til ubetalt orlov.</span><span class="sxs-lookup"><span data-stu-id="b9881-159">In this release, HR can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="b9881-160">Ubetalt orlov kan være en type, men behøver ikke at være det.</span><span class="sxs-lookup"><span data-stu-id="b9881-160">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="b9881-161">Du kan suspendere enhver orlov baseret på en anden orlovstype.</span><span class="sxs-lookup"><span data-stu-id="b9881-161">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions-june-1"></a><span data-ttu-id="b9881-162">DMF-enhed er tilgængelig for periodiseringssuspenderinger (1. juni)</span><span class="sxs-lookup"><span data-stu-id="b9881-162">DMF entity available for accrual suspensions (June 1)</span></span>

<span data-ttu-id="b9881-163">En DMF-enhed er nu tilgængelig for periodiseringssuspenderinger.</span><span class="sxs-lookup"><span data-stu-id="b9881-163">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="see-also"></a><span data-ttu-id="b9881-164">Se også</span><span class="sxs-lookup"><span data-stu-id="b9881-164">See also</span></span>

[<span data-ttu-id="b9881-165">Nyheder eller ændringer i Human Resources</span><span class="sxs-lookup"><span data-stu-id="b9881-165">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="b9881-166">Oversigt over Dynamics 365 Human Resources 2019 frigivelsesbølge 2</span><span class="sxs-lookup"><span data-stu-id="b9881-166">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="b9881-167">Opdater proces</span><span class="sxs-lookup"><span data-stu-id="b9881-167">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="b9881-168">Administrere funktioner</span><span class="sxs-lookup"><span data-stu-id="b9881-168">Manage features</span></span>](hr-admin-manage-features.md)