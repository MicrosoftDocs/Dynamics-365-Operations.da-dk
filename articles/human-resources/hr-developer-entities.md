---
title: Dataverse-tabeller
description: Microsoft Dynamics 365 Human Resources bruger Dataverse til at aktivere udvidelses- og integrationsscenarier.
author: andreabichsel
manager: tfehr
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2f075a8e96af55b1363d2d51db377c5b25c38775
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111966"
---
# <a name="dataverse-tables"></a><span data-ttu-id="38793-103">Dataverse-tabeller</span><span class="sxs-lookup"><span data-stu-id="38793-103">Dataverse tables</span></span>

<span data-ttu-id="38793-104">Microsoft Dynamics 365 Human Resources bruger Dataverse til at aktivere udvidelses- og integrationsscenarier.</span><span class="sxs-lookup"><span data-stu-id="38793-104">Microsoft Dynamics 365 Human Resources uses Dataverse to enable extensibility and integration scenarios.</span></span>

> [!NOTE]
> <span data-ttu-id="38793-105">Enheder under Human Resources svarer til Dataverse-tabeller.</span><span class="sxs-lookup"><span data-stu-id="38793-105">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="38793-106">Yderligere oplysninger om Dataverse (tidligere Common Data Service) og terminologiopdateringer finder du i [Hvad er Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="38793-106">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="38793-107">Følgende Dataverse-tabeller er tilgængelige baseret på Human Resources-enheder.</span><span class="sxs-lookup"><span data-stu-id="38793-107">The following Dataverse tables are available based on Human Resources entities.</span></span>

## <a name="benefit-tables"></a><span data-ttu-id="38793-108">Frynsegodetabeller</span><span class="sxs-lookup"><span data-stu-id="38793-108">Benefit tables</span></span>

| <span data-ttu-id="38793-109">Navn</span><span class="sxs-lookup"><span data-stu-id="38793-109">Name</span></span> | <span data-ttu-id="38793-110">Tabellen</span><span class="sxs-lookup"><span data-stu-id="38793-110">Table</span></span> |
| --- | --- |
| <span data-ttu-id="38793-111">Frekvens for personalegodeberegning</span><span class="sxs-lookup"><span data-stu-id="38793-111">Benefit Calculation Frequency</span></span> | <span data-ttu-id="38793-112">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="38793-112">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="38793-113">Frynsegoders Beregningsfrekvens, betalingsperiode</span><span class="sxs-lookup"><span data-stu-id="38793-113">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="38793-114">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="38793-114">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="38793-115">Frynsegodeberegningssats</span><span class="sxs-lookup"><span data-stu-id="38793-115">Benefit Calculation Rate</span></span> | <span data-ttu-id="38793-116">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="38793-116">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="38793-117">Oplysninger om frynsegodeberegningssats</span><span class="sxs-lookup"><span data-stu-id="38793-117">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="38793-118">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="38793-118">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="38793-119">Frynsegodeindstilling</span><span class="sxs-lookup"><span data-stu-id="38793-119">Benefit Option</span></span> | <span data-ttu-id="38793-120">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="38793-120">cdm_benefitoption</span></span> |
| <span data-ttu-id="38793-121">Frynsegodeplan</span><span class="sxs-lookup"><span data-stu-id="38793-121">Benefit Plan</span></span> | <span data-ttu-id="38793-122">cdm_benefitplan (ikke aktiveret til understøttelse af brugerdefinerede felter)</span><span class="sxs-lookup"><span data-stu-id="38793-122">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="38793-123">Human Resourcesgodetype</span><span class="sxs-lookup"><span data-stu-id="38793-123">Benefit Type</span></span> | <span data-ttu-id="38793-124">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="38793-124">cdm_benefittype</span></span> |

## <a name="business-process-tasks-tables"></a><span data-ttu-id="38793-125">Tabeller for forretningsprocesopgaver</span><span class="sxs-lookup"><span data-stu-id="38793-125">Business process tasks tables</span></span>

| <span data-ttu-id="38793-126">Navn</span><span class="sxs-lookup"><span data-stu-id="38793-126">Name</span></span> | <span data-ttu-id="38793-127">Tabellen</span><span class="sxs-lookup"><span data-stu-id="38793-127">Table</span></span> |
| --- | --- |
| <span data-ttu-id="38793-128">Forretningsproceskalender</span><span class="sxs-lookup"><span data-stu-id="38793-128">Business Process Calendar</span></span> | <span data-ttu-id="38793-129">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="38793-129">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="38793-130">Tildeling af forretningsprocesgruppe</span><span class="sxs-lookup"><span data-stu-id="38793-130">Business Process Group Assignment</span></span> | <span data-ttu-id="38793-131">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="38793-131">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="38793-132">Opgavegruppe for forretningsprocesbibliotek</span><span class="sxs-lookup"><span data-stu-id="38793-132">Business Process Library Task Group</span></span> | <span data-ttu-id="38793-133">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="38793-133">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="38793-134">Forretningsprocesstadie</span><span class="sxs-lookup"><span data-stu-id="38793-134">Business Process Stage</span></span> | <span data-ttu-id="38793-135">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="38793-135">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="38793-136">Kontrollisteskabelonhoved</span><span class="sxs-lookup"><span data-stu-id="38793-136">Checklist Template Header</span></span> | <span data-ttu-id="38793-137">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="38793-137">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="38793-138">Tjeklisteskabelonopgave</span><span class="sxs-lookup"><span data-stu-id="38793-138">Checklist Template Task</span></span> | <span data-ttu-id="38793-139">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="38793-139">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-tables"></a><span data-ttu-id="38793-140">Kompensationstabeller</span><span class="sxs-lookup"><span data-stu-id="38793-140">Compensation tables</span></span>

| <span data-ttu-id="38793-141">Navn</span><span class="sxs-lookup"><span data-stu-id="38793-141">Name</span></span> | <span data-ttu-id="38793-142">Tabellen</span><span class="sxs-lookup"><span data-stu-id="38793-142">Table</span></span> |
| --- | --- |
| <span data-ttu-id="38793-143">Fast lønstruktur</span><span class="sxs-lookup"><span data-stu-id="38793-143">Compensation Fixed Plan</span></span> | <span data-ttu-id="38793-144">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="38793-144">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="38793-145">Kompensationsgitter</span><span class="sxs-lookup"><span data-stu-id="38793-145">Compensation Grid</span></span> | <span data-ttu-id="38793-146">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="38793-146">cdm_compensationgrid</span></span> |
| <span data-ttu-id="38793-147">Kompensationsniveau</span><span class="sxs-lookup"><span data-stu-id="38793-147">Compensation Level</span></span> | <span data-ttu-id="38793-148">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="38793-148">cdm_compensationlevel</span></span> |
| <span data-ttu-id="38793-149">Kompensation - lønfrekvens</span><span class="sxs-lookup"><span data-stu-id="38793-149">Compensation Pay Frequency</span></span> | <span data-ttu-id="38793-150">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="38793-150">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="38793-151">Opsætning af kompensationsreferencepunkt</span><span class="sxs-lookup"><span data-stu-id="38793-151">Compensation Reference Point Setup</span></span> | <span data-ttu-id="38793-152">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="38793-152">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="38793-153">Opsætningslinje for kompensationsreferencepunkt</span><span class="sxs-lookup"><span data-stu-id="38793-153">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="38793-154">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="38793-154">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="38793-155">Kompensationsområde</span><span class="sxs-lookup"><span data-stu-id="38793-155">Compensation Region</span></span> | <span data-ttu-id="38793-156">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="38793-156">cdm_compensationregion</span></span> |
| <span data-ttu-id="38793-157">Kompensationsstruktur</span><span class="sxs-lookup"><span data-stu-id="38793-157">Compensation Structure</span></span> | <span data-ttu-id="38793-158">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="38793-158">cdm_compensationstructure</span></span> |
| <span data-ttu-id="38793-159">Variabel kompensationsplan</span><span class="sxs-lookup"><span data-stu-id="38793-159">Compensation Variable Plan</span></span> | <span data-ttu-id="38793-160">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="38793-160">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="38793-161">Niveau i variabel kompensationsplan</span><span class="sxs-lookup"><span data-stu-id="38793-161">Compensation Variable Plan Level</span></span> | <span data-ttu-id="38793-162">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="38793-162">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="38793-163">Type af variabel kompensationsplan</span><span class="sxs-lookup"><span data-stu-id="38793-163">Compensation Variable Plan Type</span></span> | <span data-ttu-id="38793-164">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="38793-164">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="38793-165">Hændelse for fast løn</span><span class="sxs-lookup"><span data-stu-id="38793-165">Fixed Compensation Event</span></span> | <span data-ttu-id="38793-166">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="38793-166">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="38793-167">Fordelingsregel</span><span class="sxs-lookup"><span data-stu-id="38793-167">Vesting Rule</span></span> | <span data-ttu-id="38793-168">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="38793-168">cdm_vestingrule</span></span> |
| <span data-ttu-id="38793-169">Arbejders faste løn</span><span class="sxs-lookup"><span data-stu-id="38793-169">Worker Fixed Compensation</span></span> | <span data-ttu-id="38793-170">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="38793-170">cdm_workerfixedcompensation</span></span> |

## <a name="organization-tables"></a><span data-ttu-id="38793-171">Organisationstabeller</span><span class="sxs-lookup"><span data-stu-id="38793-171">Organization tables</span></span>

| <span data-ttu-id="38793-172">Navn</span><span class="sxs-lookup"><span data-stu-id="38793-172">Name</span></span> | <span data-ttu-id="38793-173">Tabellen</span><span class="sxs-lookup"><span data-stu-id="38793-173">Table</span></span> |
| --- | --- |
| <span data-ttu-id="38793-174">Afdeling</span><span class="sxs-lookup"><span data-stu-id="38793-174">Department</span></span> | <span data-ttu-id="38793-175">cdm_department</span><span class="sxs-lookup"><span data-stu-id="38793-175">cdm_department</span></span> |
| <span data-ttu-id="38793-176">Ansættelse</span><span class="sxs-lookup"><span data-stu-id="38793-176">Employment</span></span> | <span data-ttu-id="38793-177">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="38793-177">cdm_employment</span></span> |
| <span data-ttu-id="38793-178">Firma</span><span class="sxs-lookup"><span data-stu-id="38793-178">Company</span></span> | <span data-ttu-id="38793-179">cdm_company</span><span class="sxs-lookup"><span data-stu-id="38793-179">cdm_company</span></span> |
| <span data-ttu-id="38793-180">Stilling</span><span class="sxs-lookup"><span data-stu-id="38793-180">Job</span></span> | <span data-ttu-id="38793-181">cdm_job</span><span class="sxs-lookup"><span data-stu-id="38793-181">cdm_job</span></span> |
| <span data-ttu-id="38793-182">Jobfunktion</span><span class="sxs-lookup"><span data-stu-id="38793-182">Job Function</span></span> | <span data-ttu-id="38793-183">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="38793-183">cdm_jobfunction</span></span> |
| <span data-ttu-id="38793-184">Stilling</span><span class="sxs-lookup"><span data-stu-id="38793-184">Job Position</span></span> | <span data-ttu-id="38793-185">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="38793-185">cdm_jobposition</span></span> |
| <span data-ttu-id="38793-186">Stillingstype</span><span class="sxs-lookup"><span data-stu-id="38793-186">Position Type</span></span> | <span data-ttu-id="38793-187">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="38793-187">cdm_positiontype</span></span> |
| <span data-ttu-id="38793-188">Arbejdertildeling til stilling</span><span class="sxs-lookup"><span data-stu-id="38793-188">Position Worker Assignment</span></span> | <span data-ttu-id="38793-189">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="38793-189">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="38793-190">Stillingsdimension</span><span class="sxs-lookup"><span data-stu-id="38793-190">Job Position Dimension</span></span> | <span data-ttu-id="38793-191">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="38793-191">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="38793-192">Jobtype</span><span class="sxs-lookup"><span data-stu-id="38793-192">Job Type</span></span> | <span data-ttu-id="38793-193">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="38793-193">cdm_jobtype</span></span> |
| <span data-ttu-id="38793-194">Sprog</span><span class="sxs-lookup"><span data-stu-id="38793-194">Language</span></span> | <span data-ttu-id="38793-195">cdm_language</span><span class="sxs-lookup"><span data-stu-id="38793-195">cdm_language</span></span> |
| <span data-ttu-id="38793-196">Stilling</span><span class="sxs-lookup"><span data-stu-id="38793-196">Title</span></span> | <span data-ttu-id="38793-197">cdm_title</span><span class="sxs-lookup"><span data-stu-id="38793-197">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="38793-198">Økonomiske dimensioner for **Stillingstype**, **Arbejdertildeling til stilling** og **Ansættelse** giver integration i én retning til Dataverse.</span><span class="sxs-lookup"><span data-stu-id="38793-198">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Dataverse.</span></span> <span data-ttu-id="38793-199">Opdateringer af økonomiske dimensioner kan i øjeblikket ikke synkroniseres fra Dataverse til HR.</span><span class="sxs-lookup"><span data-stu-id="38793-199">Financial dimensions updates currently can't synchronize from Dataverse to Human Resources.</span></span> 

## <a name="leave-and-absence-tables"></a><span data-ttu-id="38793-200">Orlov og fravær-tabeller</span><span class="sxs-lookup"><span data-stu-id="38793-200">Leave and absence tables</span></span>

| <span data-ttu-id="38793-201">Navn</span><span class="sxs-lookup"><span data-stu-id="38793-201">Name</span></span> | <span data-ttu-id="38793-202">Tabellen</span><span class="sxs-lookup"><span data-stu-id="38793-202">Table</span></span> |
| --- | --- |
| <span data-ttu-id="38793-203">Orlovsbanktransaktion</span><span class="sxs-lookup"><span data-stu-id="38793-203">Leave Bank Transaction</span></span> | <span data-ttu-id="38793-204">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="38793-204">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="38793-205">Orlovstilmelding</span><span class="sxs-lookup"><span data-stu-id="38793-205">Leave Enrollment</span></span> | <span data-ttu-id="38793-206">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="38793-206">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="38793-207">Orlovsplan</span><span class="sxs-lookup"><span data-stu-id="38793-207">Leave Plan</span></span> | <span data-ttu-id="38793-208">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="38793-208">cdm_leaveplan</span></span> |
| <span data-ttu-id="38793-209">Orlovsanmodning</span><span class="sxs-lookup"><span data-stu-id="38793-209">Leave Request</span></span> | <span data-ttu-id="38793-210">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="38793-210">cdm_leaverequest</span></span> |
| <span data-ttu-id="38793-211">Detaljer om orlovsanmodning</span><span class="sxs-lookup"><span data-stu-id="38793-211">Leave Request Detail</span></span> | <span data-ttu-id="38793-212">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="38793-212">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="38793-213">Orlovstype</span><span class="sxs-lookup"><span data-stu-id="38793-213">Leave Type</span></span> | <span data-ttu-id="38793-214">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="38793-214">cdm_leavetype</span></span> |
| <span data-ttu-id="38793-215">Orlovstypens årsagskode</span><span class="sxs-lookup"><span data-stu-id="38793-215">Leave Type Reason Code</span></span> | <span data-ttu-id="38793-216">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="38793-216">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-tables"></a><span data-ttu-id="38793-217">Løntabeller</span><span class="sxs-lookup"><span data-stu-id="38793-217">Payroll tables</span></span>

| <span data-ttu-id="38793-218">Navn</span><span class="sxs-lookup"><span data-stu-id="38793-218">Name</span></span> | <span data-ttu-id="38793-219">Tabellen</span><span class="sxs-lookup"><span data-stu-id="38793-219">Table</span></span> |
| --- | --- |
| <span data-ttu-id="38793-220">Betalingscyklus</span><span class="sxs-lookup"><span data-stu-id="38793-220">Pay Cycle</span></span> | <span data-ttu-id="38793-221">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="38793-221">cdm_paycycle</span></span> |
| <span data-ttu-id="38793-222">Lønperiode</span><span class="sxs-lookup"><span data-stu-id="38793-222">Pay Period</span></span> | <span data-ttu-id="38793-223">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="38793-223">cdm_payperiod</span></span> |
| <span data-ttu-id="38793-224">Lønkode</span><span class="sxs-lookup"><span data-stu-id="38793-224">Payroll Earning Code</span></span> | <span data-ttu-id="38793-225">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="38793-225">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="38793-226">Bankkontoudbetalinger</span><span class="sxs-lookup"><span data-stu-id="38793-226">Bank Account Disbursement</span></span> | <span data-ttu-id="38793-227">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="38793-227">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="38793-228">Skatteområde</span><span class="sxs-lookup"><span data-stu-id="38793-228">Tax Region</span></span> | <span data-ttu-id="38793-229">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="38793-229">cdm_taxregion</span></span> |

## <a name="worker-tables"></a><span data-ttu-id="38793-230">Arbejdertabeller</span><span class="sxs-lookup"><span data-stu-id="38793-230">Worker tables</span></span>

| <span data-ttu-id="38793-231">Navn</span><span class="sxs-lookup"><span data-stu-id="38793-231">Name</span></span> | <span data-ttu-id="38793-232">Tabellen</span><span class="sxs-lookup"><span data-stu-id="38793-232">Table</span></span> |
| --- | --- |
| <span data-ttu-id="38793-233">Arbejdstråd</span><span class="sxs-lookup"><span data-stu-id="38793-233">Worker</span></span> | <span data-ttu-id="38793-234">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="38793-234">cdm_worker</span></span> |
| <span data-ttu-id="38793-235">Arbejderadresse</span><span class="sxs-lookup"><span data-stu-id="38793-235">Worker Address</span></span> | <span data-ttu-id="38793-236">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="38793-236">cdm_workeraddress</span></span> |
| <span data-ttu-id="38793-237">Arbejders personlige oplysninger</span><span class="sxs-lookup"><span data-stu-id="38793-237">Worker Personal Detail</span></span> | <span data-ttu-id="38793-238">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="38793-238">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="38793-239">Personidentifikationsnummeret for arbejder</span><span class="sxs-lookup"><span data-stu-id="38793-239">Worker Person Identification Number</span></span> | <span data-ttu-id="38793-240">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="38793-240">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="38793-241">Personidentifikationstype for arbejder</span><span class="sxs-lookup"><span data-stu-id="38793-241">Worker Person Identification Type</span></span> | <span data-ttu-id="38793-242">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="38793-242">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="38793-243">Arbejdskalender</span><span class="sxs-lookup"><span data-stu-id="38793-243">Work Calendar</span></span> | <span data-ttu-id="38793-244">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="38793-244">cdm_workcalendar</span></span> |
| <span data-ttu-id="38793-245">Arbejdskalenderdag</span><span class="sxs-lookup"><span data-stu-id="38793-245">Work Calendar Day</span></span> | <span data-ttu-id="38793-246">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="38793-246">cdm_workcalendarday</span></span> |
| <span data-ttu-id="38793-247">Arbejdskalenderfridag</span><span class="sxs-lookup"><span data-stu-id="38793-247">Work Calendar Holiday</span></span> |<span data-ttu-id="38793-248">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="38793-248">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="38793-249">Ferielinje i arbejdskalender</span><span class="sxs-lookup"><span data-stu-id="38793-249">Work Calendar Holiday Line</span></span> | <span data-ttu-id="38793-250">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="38793-250">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="38793-251">Tidsinterval i arbejdskalender</span><span class="sxs-lookup"><span data-stu-id="38793-251">Work Calendar Time Interval</span></span> | <span data-ttu-id="38793-252">cdm_workcalendartimeinterval (ikke aktiveret til understøttelse af brugerdefinerede felter)</span><span class="sxs-lookup"><span data-stu-id="38793-252">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="38793-253">Arbejderbankkonto</span><span class="sxs-lookup"><span data-stu-id="38793-253">Worker Bank Account</span></span> | <span data-ttu-id="38793-254">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="38793-254">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-tables"></a><span data-ttu-id="38793-255">Opsætningstabeller for arbejdere</span><span class="sxs-lookup"><span data-stu-id="38793-255">Worker setup tables</span></span>

| <span data-ttu-id="38793-256">Navn</span><span class="sxs-lookup"><span data-stu-id="38793-256">Name</span></span> | <span data-ttu-id="38793-257">Tabellen</span><span class="sxs-lookup"><span data-stu-id="38793-257">Table</span></span> |
| --- | --- |
| <span data-ttu-id="38793-258">Veteranstatus</span><span class="sxs-lookup"><span data-stu-id="38793-258">Veteran Status</span></span> | <span data-ttu-id="38793-259">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="38793-259">cdm_veteranstatus</span></span> |
| <span data-ttu-id="38793-260">Etnisk oprindelse</span><span class="sxs-lookup"><span data-stu-id="38793-260">Ethnic Origin</span></span> | <span data-ttu-id="38793-261">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="38793-261">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="38793-262">Årsagskode</span><span class="sxs-lookup"><span data-stu-id="38793-262">Reason Code</span></span> | <span data-ttu-id="38793-263">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="38793-263">cdm_reasoncode</span></span> |
| <span data-ttu-id="38793-264">Udstedende organ for personidentifikation</span><span class="sxs-lookup"><span data-stu-id="38793-264">Person Identification Issuing Agency</span></span> | <span data-ttu-id="38793-265">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="38793-265">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-tables"></a><span data-ttu-id="38793-266">Kompetencetabeller</span><span class="sxs-lookup"><span data-stu-id="38793-266">Competency tables</span></span>

| <span data-ttu-id="38793-267">Navn</span><span class="sxs-lookup"><span data-stu-id="38793-267">Name</span></span> | <span data-ttu-id="38793-268">Tabellen</span><span class="sxs-lookup"><span data-stu-id="38793-268">Table</span></span> |
| --- | --- |
| <span data-ttu-id="38793-269">Kompetencetype</span><span class="sxs-lookup"><span data-stu-id="38793-269">Skill Type</span></span> | <span data-ttu-id="38793-270">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="38793-270">cdm_skilltype</span></span> |

## <a name="table-relationship-models"></a><span data-ttu-id="38793-271">Tabelrelationsmodeller</span><span class="sxs-lookup"><span data-stu-id="38793-271">Table relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="38793-272">Arbejdstråd</span><span class="sxs-lookup"><span data-stu-id="38793-272">Worker</span></span>

![Arbejdstråd](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="38793-274">Stilling og job</span><span class="sxs-lookup"><span data-stu-id="38793-274">Job and Job Position</span></span>

![Stilling og job](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="38793-276">Frynsegoder</span><span class="sxs-lookup"><span data-stu-id="38793-276">Benefits</span></span>

![Frynsegoder](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="38793-278">Kompensation</span><span class="sxs-lookup"><span data-stu-id="38793-278">Compensation</span></span>

![Kompensation](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="38793-280">Orlov</span><span class="sxs-lookup"><span data-stu-id="38793-280">Leave</span></span>

![Orlov](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="38793-282">Arbejdskalender</span><span class="sxs-lookup"><span data-stu-id="38793-282">Work Calendar</span></span>

![Arbejdskalender](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="38793-284">Se også</span><span class="sxs-lookup"><span data-stu-id="38793-284">See also</span></span>

[<span data-ttu-id="38793-285">Vælg en dataintegrationsteknologi</span><span class="sxs-lookup"><span data-stu-id="38793-285">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)<br>
[<span data-ttu-id="38793-286">Konfigurere Dataverse-integration</span><span class="sxs-lookup"><span data-stu-id="38793-286">Configure Dataverse integration</span></span>](hr-admin-integration-common-data-service.md)<br>
[<span data-ttu-id="38793-287">Konfigurere virtuelle Dataverse-tabeller</span><span class="sxs-lookup"><span data-stu-id="38793-287">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="38793-288">Ofte stillede spørgsmål om Virtuelle tabeller i Human Resources</span><span class="sxs-lookup"><span data-stu-id="38793-288">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="38793-289">Hvad er Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="38793-289">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="38793-290">Terminologiopdateringer</span><span class="sxs-lookup"><span data-stu-id="38793-290">Terminology updates</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates)
