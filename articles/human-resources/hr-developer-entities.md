---
title: Common Data Service-enheder
description: Microsoft Dynamics 365 Human Resources bruger Common Data Service til at aktivere udvidelses- og integrationsscenarier.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: 6879a45dd1fcc1ba718747aaaf0d7936c2eac49f
ms.sourcegitcommit: 3cad15f8ecc257d3a45c1bc1fada7c094ff4bcec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/26/2020
ms.locfileid: "3087340"
---
# <a name="common-data-service-entities"></a><span data-ttu-id="ef16b-103">Common Data Service-enheder</span><span class="sxs-lookup"><span data-stu-id="ef16b-103">Common Data Service entities</span></span>

<span data-ttu-id="ef16b-104">Microsoft Dynamics 365 Human Resources bruger Common Data Service til at aktivere udvidelses- og integrationsscenarier.</span><span class="sxs-lookup"><span data-stu-id="ef16b-104">Microsoft Dynamics 365 Human Resources uses Common Data Service to enable extensibility and integration scenarios.</span></span>

<span data-ttu-id="ef16b-105">Du kan finde flere oplysninger om Common Data Service i [Hvad er Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span><span class="sxs-lookup"><span data-stu-id="ef16b-105">For more information about Common Data Service, see [What is Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span></span>

<span data-ttu-id="ef16b-106">Følgende HR-ressourcer er tilgængelige i Common Data Service .</span><span class="sxs-lookup"><span data-stu-id="ef16b-106">The following Human Resources entities are available in Common Data Service.</span></span>

## <a name="benefit-entities"></a><span data-ttu-id="ef16b-107">Frynsegodeenheder</span><span class="sxs-lookup"><span data-stu-id="ef16b-107">Benefit entities</span></span>

| <span data-ttu-id="ef16b-108">Navn</span><span class="sxs-lookup"><span data-stu-id="ef16b-108">Name</span></span> | <span data-ttu-id="ef16b-109">Enhed</span><span class="sxs-lookup"><span data-stu-id="ef16b-109">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="ef16b-110">Frekvens for frynsegodeberegning</span><span class="sxs-lookup"><span data-stu-id="ef16b-110">Benefit Calculation Frequency</span></span> | <span data-ttu-id="ef16b-111">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="ef16b-111">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="ef16b-112">Frynsegoders Beregningsfrekvens, betalingsperiode</span><span class="sxs-lookup"><span data-stu-id="ef16b-112">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="ef16b-113">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="ef16b-113">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="ef16b-114">Frynsegodeberegningssats</span><span class="sxs-lookup"><span data-stu-id="ef16b-114">Benefit Calculation Rate</span></span> | <span data-ttu-id="ef16b-115">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="ef16b-115">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="ef16b-116">Oplysninger om frynsegodeberegningssats</span><span class="sxs-lookup"><span data-stu-id="ef16b-116">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="ef16b-117">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="ef16b-117">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="ef16b-118">Frynsegodeindstilling</span><span class="sxs-lookup"><span data-stu-id="ef16b-118">Benefit Option</span></span> | <span data-ttu-id="ef16b-119">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="ef16b-119">cdm_benefitoption</span></span> |
| <span data-ttu-id="ef16b-120">Frynsegodeplan</span><span class="sxs-lookup"><span data-stu-id="ef16b-120">Benefit Plan</span></span> | <span data-ttu-id="ef16b-121">cdm_benefitplan (ikke aktiveret til understøttelse af brugerdefinerede felter)</span><span class="sxs-lookup"><span data-stu-id="ef16b-121">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="ef16b-122">Frynsegodetype</span><span class="sxs-lookup"><span data-stu-id="ef16b-122">Benefit Type</span></span> | <span data-ttu-id="ef16b-123">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="ef16b-123">cdm_benefittype</span></span> |

## <a name="business-process-tasks-entities"></a><span data-ttu-id="ef16b-124">Enheder for forretningsprocesopgaver</span><span class="sxs-lookup"><span data-stu-id="ef16b-124">Business process tasks entities</span></span>

| <span data-ttu-id="ef16b-125">Navn</span><span class="sxs-lookup"><span data-stu-id="ef16b-125">Name</span></span> | <span data-ttu-id="ef16b-126">Enhed</span><span class="sxs-lookup"><span data-stu-id="ef16b-126">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="ef16b-127">Forretningsproceskalender</span><span class="sxs-lookup"><span data-stu-id="ef16b-127">Business Process Calendar</span></span> | <span data-ttu-id="ef16b-128">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="ef16b-128">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="ef16b-129">Tildeling af forretningsprocesgruppe</span><span class="sxs-lookup"><span data-stu-id="ef16b-129">Business Process Group Assignment</span></span> | <span data-ttu-id="ef16b-130">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="ef16b-130">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="ef16b-131">Opgavegruppe for forretningsprocesbibliotek</span><span class="sxs-lookup"><span data-stu-id="ef16b-131">Business Process Library Task Group</span></span> | <span data-ttu-id="ef16b-132">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="ef16b-132">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="ef16b-133">Forretningsprocesstadie</span><span class="sxs-lookup"><span data-stu-id="ef16b-133">Business Process Stage</span></span> | <span data-ttu-id="ef16b-134">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="ef16b-134">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="ef16b-135">Kontrollisteskabelonhoved</span><span class="sxs-lookup"><span data-stu-id="ef16b-135">Checklist Template Header</span></span> | <span data-ttu-id="ef16b-136">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="ef16b-136">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="ef16b-137">Kontrollisteskabelonopgave</span><span class="sxs-lookup"><span data-stu-id="ef16b-137">Checklist Template Task</span></span> | <span data-ttu-id="ef16b-138">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="ef16b-138">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-entities"></a><span data-ttu-id="ef16b-139">Kompensationsenheder</span><span class="sxs-lookup"><span data-stu-id="ef16b-139">Compensation entities</span></span>

| <span data-ttu-id="ef16b-140">Navn</span><span class="sxs-lookup"><span data-stu-id="ef16b-140">Name</span></span> | <span data-ttu-id="ef16b-141">Enhed</span><span class="sxs-lookup"><span data-stu-id="ef16b-141">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="ef16b-142">Kompensation - fast struktur</span><span class="sxs-lookup"><span data-stu-id="ef16b-142">Compensation Fixed Plan</span></span> | <span data-ttu-id="ef16b-143">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="ef16b-143">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="ef16b-144">Kompensationsgitter</span><span class="sxs-lookup"><span data-stu-id="ef16b-144">Compensation Grid</span></span> | <span data-ttu-id="ef16b-145">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="ef16b-145">cdm_compensationgrid</span></span> |
| <span data-ttu-id="ef16b-146">Kompensationsniveau</span><span class="sxs-lookup"><span data-stu-id="ef16b-146">Compensation Level</span></span> | <span data-ttu-id="ef16b-147">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="ef16b-147">cdm_compensationlevel</span></span> |
| <span data-ttu-id="ef16b-148">Kompensation - lønfrekvens</span><span class="sxs-lookup"><span data-stu-id="ef16b-148">Compensation Pay Frequency</span></span> | <span data-ttu-id="ef16b-149">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="ef16b-149">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="ef16b-150">Opsætning af kompensationsreferencepunkt</span><span class="sxs-lookup"><span data-stu-id="ef16b-150">Compensation Reference Point Setup</span></span> | <span data-ttu-id="ef16b-151">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="ef16b-151">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="ef16b-152">Opsætningslinje for kompensationsreferencepunkt</span><span class="sxs-lookup"><span data-stu-id="ef16b-152">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="ef16b-153">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="ef16b-153">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="ef16b-154">Kompensationsområde</span><span class="sxs-lookup"><span data-stu-id="ef16b-154">Compensation Region</span></span> | <span data-ttu-id="ef16b-155">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="ef16b-155">cdm_compensationregion</span></span> |
| <span data-ttu-id="ef16b-156">Kompensationsstruktur</span><span class="sxs-lookup"><span data-stu-id="ef16b-156">Compensation Structure</span></span> | <span data-ttu-id="ef16b-157">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="ef16b-157">cdm_compensationstructure</span></span> |
| <span data-ttu-id="ef16b-158">Variabel kompensationsplan</span><span class="sxs-lookup"><span data-stu-id="ef16b-158">Compensation Variable Plan</span></span> | <span data-ttu-id="ef16b-159">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="ef16b-159">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="ef16b-160">Niveau i variabel kompensationsplan</span><span class="sxs-lookup"><span data-stu-id="ef16b-160">Compensation Variable Plan Level</span></span> | <span data-ttu-id="ef16b-161">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="ef16b-161">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="ef16b-162">Type af variabel kompensationsplan</span><span class="sxs-lookup"><span data-stu-id="ef16b-162">Compensation Variable Plan Type</span></span> | <span data-ttu-id="ef16b-163">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="ef16b-163">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="ef16b-164">Hændelse for fast løn</span><span class="sxs-lookup"><span data-stu-id="ef16b-164">Fixed Compensation Event</span></span> | <span data-ttu-id="ef16b-165">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="ef16b-165">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="ef16b-166">Fordelingsregel</span><span class="sxs-lookup"><span data-stu-id="ef16b-166">Vesting Rule</span></span> | <span data-ttu-id="ef16b-167">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="ef16b-167">cdm_vestingrule</span></span> |
| <span data-ttu-id="ef16b-168">Arbejders faste løn</span><span class="sxs-lookup"><span data-stu-id="ef16b-168">Worker Fixed Compensation</span></span> | <span data-ttu-id="ef16b-169">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="ef16b-169">cdm_workerfixedcompensation</span></span> |

## <a name="organization-entities"></a><span data-ttu-id="ef16b-170">Organisationsenheder</span><span class="sxs-lookup"><span data-stu-id="ef16b-170">Organization entities</span></span>

| <span data-ttu-id="ef16b-171">Navn</span><span class="sxs-lookup"><span data-stu-id="ef16b-171">Name</span></span> | <span data-ttu-id="ef16b-172">Enhed</span><span class="sxs-lookup"><span data-stu-id="ef16b-172">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="ef16b-173">Afdeling</span><span class="sxs-lookup"><span data-stu-id="ef16b-173">Department</span></span> | <span data-ttu-id="ef16b-174">cdm_department</span><span class="sxs-lookup"><span data-stu-id="ef16b-174">cdm_department</span></span> |
| <span data-ttu-id="ef16b-175">Ansættelse</span><span class="sxs-lookup"><span data-stu-id="ef16b-175">Employment</span></span> | <span data-ttu-id="ef16b-176">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="ef16b-176">cdm_employment</span></span> |
| <span data-ttu-id="ef16b-177">Regnskab</span><span class="sxs-lookup"><span data-stu-id="ef16b-177">Company</span></span> | <span data-ttu-id="ef16b-178">cdm_company</span><span class="sxs-lookup"><span data-stu-id="ef16b-178">cdm_company</span></span> |
| <span data-ttu-id="ef16b-179">Stilling</span><span class="sxs-lookup"><span data-stu-id="ef16b-179">Job</span></span> | <span data-ttu-id="ef16b-180">cdm_job</span><span class="sxs-lookup"><span data-stu-id="ef16b-180">cdm_job</span></span> |
| <span data-ttu-id="ef16b-181">Jobfunktion</span><span class="sxs-lookup"><span data-stu-id="ef16b-181">Job Function</span></span> | <span data-ttu-id="ef16b-182">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="ef16b-182">cdm_jobfunction</span></span> |
| <span data-ttu-id="ef16b-183">Stilling</span><span class="sxs-lookup"><span data-stu-id="ef16b-183">Job Position</span></span> | <span data-ttu-id="ef16b-184">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="ef16b-184">cdm_jobposition</span></span> |
| <span data-ttu-id="ef16b-185">Stillingstype</span><span class="sxs-lookup"><span data-stu-id="ef16b-185">Position Type</span></span> | <span data-ttu-id="ef16b-186">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="ef16b-186">cdm_positiontype</span></span> |
| <span data-ttu-id="ef16b-187">Arbejdertildeling til stilling</span><span class="sxs-lookup"><span data-stu-id="ef16b-187">Position Worker Assignment</span></span> | <span data-ttu-id="ef16b-188">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="ef16b-188">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="ef16b-189">Jobtype</span><span class="sxs-lookup"><span data-stu-id="ef16b-189">Job Type</span></span> | <span data-ttu-id="ef16b-190">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="ef16b-190">cdm_jobtype</span></span> |
| <span data-ttu-id="ef16b-191">Sprog</span><span class="sxs-lookup"><span data-stu-id="ef16b-191">Language</span></span> | <span data-ttu-id="ef16b-192">cdm_language</span><span class="sxs-lookup"><span data-stu-id="ef16b-192">cdm_language</span></span> |

## <a name="leave-and-absence-entities"></a><span data-ttu-id="ef16b-193">Orlovs- og fraværsenheder</span><span class="sxs-lookup"><span data-stu-id="ef16b-193">Leave and absence entities</span></span>

| <span data-ttu-id="ef16b-194">Navn</span><span class="sxs-lookup"><span data-stu-id="ef16b-194">Name</span></span> | <span data-ttu-id="ef16b-195">Enhed</span><span class="sxs-lookup"><span data-stu-id="ef16b-195">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="ef16b-196">Orlovsbanktransaktion</span><span class="sxs-lookup"><span data-stu-id="ef16b-196">Leave Bank Transaction</span></span> | <span data-ttu-id="ef16b-197">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="ef16b-197">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="ef16b-198">Orlovstilmelding</span><span class="sxs-lookup"><span data-stu-id="ef16b-198">Leave Enrollment</span></span> | <span data-ttu-id="ef16b-199">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="ef16b-199">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="ef16b-200">Orlovsplan</span><span class="sxs-lookup"><span data-stu-id="ef16b-200">Leave Plan</span></span> | <span data-ttu-id="ef16b-201">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="ef16b-201">cdm_leaveplan</span></span> |
| <span data-ttu-id="ef16b-202">Orlovsanmodning</span><span class="sxs-lookup"><span data-stu-id="ef16b-202">Leave Request</span></span> | <span data-ttu-id="ef16b-203">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="ef16b-203">cdm_leaverequest</span></span> |
| <span data-ttu-id="ef16b-204">Detaljer om orlovsanmodning</span><span class="sxs-lookup"><span data-stu-id="ef16b-204">Leave Request Detail</span></span> | <span data-ttu-id="ef16b-205">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="ef16b-205">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="ef16b-206">Orlovstype</span><span class="sxs-lookup"><span data-stu-id="ef16b-206">Leave Type</span></span> | <span data-ttu-id="ef16b-207">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="ef16b-207">cdm_leavetype</span></span> |
| <span data-ttu-id="ef16b-208">Orlovstypens årsagskode</span><span class="sxs-lookup"><span data-stu-id="ef16b-208">Leave Type Reason Code</span></span> | <span data-ttu-id="ef16b-209">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="ef16b-209">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-entities"></a><span data-ttu-id="ef16b-210">Lønenheder</span><span class="sxs-lookup"><span data-stu-id="ef16b-210">Payroll entities</span></span>

| <span data-ttu-id="ef16b-211">Navn</span><span class="sxs-lookup"><span data-stu-id="ef16b-211">Name</span></span> | <span data-ttu-id="ef16b-212">Enhed</span><span class="sxs-lookup"><span data-stu-id="ef16b-212">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="ef16b-213">Betalingscyklus</span><span class="sxs-lookup"><span data-stu-id="ef16b-213">Pay Cycle</span></span> | <span data-ttu-id="ef16b-214">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="ef16b-214">cdm_paycycle</span></span> |
| <span data-ttu-id="ef16b-215">Lønperiode</span><span class="sxs-lookup"><span data-stu-id="ef16b-215">Pay Period</span></span> | <span data-ttu-id="ef16b-216">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="ef16b-216">cdm_payperiod</span></span> |
| <span data-ttu-id="ef16b-217">Lønkode</span><span class="sxs-lookup"><span data-stu-id="ef16b-217">Payroll Earning Code</span></span> | <span data-ttu-id="ef16b-218">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="ef16b-218">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="ef16b-219">Bankkontoudbetalinger</span><span class="sxs-lookup"><span data-stu-id="ef16b-219">Bank Account Disbursement</span></span> | <span data-ttu-id="ef16b-220">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="ef16b-220">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="ef16b-221">Skatteområde</span><span class="sxs-lookup"><span data-stu-id="ef16b-221">Tax Region</span></span> | <span data-ttu-id="ef16b-222">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="ef16b-222">cdm_taxregion</span></span> |

## <a name="worker-entities"></a><span data-ttu-id="ef16b-223">Enheder for arbejder</span><span class="sxs-lookup"><span data-stu-id="ef16b-223">Worker entities</span></span>

| <span data-ttu-id="ef16b-224">Navn</span><span class="sxs-lookup"><span data-stu-id="ef16b-224">Name</span></span> | <span data-ttu-id="ef16b-225">Enhed</span><span class="sxs-lookup"><span data-stu-id="ef16b-225">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="ef16b-226">Arbejdstråd</span><span class="sxs-lookup"><span data-stu-id="ef16b-226">Worker</span></span> | <span data-ttu-id="ef16b-227">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="ef16b-227">cdm_worker</span></span> |
| <span data-ttu-id="ef16b-228">Arbejders adresse</span><span class="sxs-lookup"><span data-stu-id="ef16b-228">Worker Address</span></span> | <span data-ttu-id="ef16b-229">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="ef16b-229">cdm_workeraddress</span></span> |
| <span data-ttu-id="ef16b-230">Arbejders personlige oplysninger</span><span class="sxs-lookup"><span data-stu-id="ef16b-230">Worker Personal Detail</span></span> | <span data-ttu-id="ef16b-231">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="ef16b-231">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="ef16b-232">Personidentifikationsnummeret for arbejder</span><span class="sxs-lookup"><span data-stu-id="ef16b-232">Worker Person Identification Number</span></span> | <span data-ttu-id="ef16b-233">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="ef16b-233">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="ef16b-234">Personidentifikationstype for arbejder</span><span class="sxs-lookup"><span data-stu-id="ef16b-234">Worker Person Identification Type</span></span> | <span data-ttu-id="ef16b-235">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="ef16b-235">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="ef16b-236">Arbejdskalender</span><span class="sxs-lookup"><span data-stu-id="ef16b-236">Work Calendar</span></span> | <span data-ttu-id="ef16b-237">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="ef16b-237">cdm_workcalendar</span></span> |
| <span data-ttu-id="ef16b-238">Arbejdskalenderdag</span><span class="sxs-lookup"><span data-stu-id="ef16b-238">Work Calendar Day</span></span> | <span data-ttu-id="ef16b-239">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="ef16b-239">cdm_workcalendarday</span></span> |
| <span data-ttu-id="ef16b-240">Arbejdskalenderfridag</span><span class="sxs-lookup"><span data-stu-id="ef16b-240">Work Calendar Holiday</span></span> |<span data-ttu-id="ef16b-241">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="ef16b-241">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="ef16b-242">Ferielinje i arbejdskalender</span><span class="sxs-lookup"><span data-stu-id="ef16b-242">Work Calendar Holiday Line</span></span> | <span data-ttu-id="ef16b-243">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="ef16b-243">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="ef16b-244">Tidsinterval i arbejdskalender</span><span class="sxs-lookup"><span data-stu-id="ef16b-244">Work Calendar Time Interval</span></span> | <span data-ttu-id="ef16b-245">cdm_workcalendartimeinterval (ikke aktiveret til understøttelse af brugerdefinerede felter)</span><span class="sxs-lookup"><span data-stu-id="ef16b-245">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="ef16b-246">Arbejders bankkonto</span><span class="sxs-lookup"><span data-stu-id="ef16b-246">Worker Bank Account</span></span> | <span data-ttu-id="ef16b-247">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="ef16b-247">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-entities"></a><span data-ttu-id="ef16b-248">Enheder til opsætning af arbejder</span><span class="sxs-lookup"><span data-stu-id="ef16b-248">Worker setup entities</span></span>

| <span data-ttu-id="ef16b-249">Navn</span><span class="sxs-lookup"><span data-stu-id="ef16b-249">Name</span></span> | <span data-ttu-id="ef16b-250">Enhed</span><span class="sxs-lookup"><span data-stu-id="ef16b-250">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="ef16b-251">Veteranstatus</span><span class="sxs-lookup"><span data-stu-id="ef16b-251">Veteran Status</span></span> | <span data-ttu-id="ef16b-252">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="ef16b-252">cdm_veteranstatus</span></span> |
| <span data-ttu-id="ef16b-253">Etnisk oprindelse</span><span class="sxs-lookup"><span data-stu-id="ef16b-253">Ethnic Origin</span></span> | <span data-ttu-id="ef16b-254">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="ef16b-254">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="ef16b-255">Årsagskode</span><span class="sxs-lookup"><span data-stu-id="ef16b-255">Reason Code</span></span> | <span data-ttu-id="ef16b-256">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="ef16b-256">cdm_reasoncode</span></span> |
| <span data-ttu-id="ef16b-257">Udstedende organ for personidentifikation</span><span class="sxs-lookup"><span data-stu-id="ef16b-257">Person Identification Issuing Agency</span></span> | <span data-ttu-id="ef16b-258">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="ef16b-258">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-entities"></a><span data-ttu-id="ef16b-259">Kompetenceenheder</span><span class="sxs-lookup"><span data-stu-id="ef16b-259">Competency entities</span></span>

| <span data-ttu-id="ef16b-260">Navn</span><span class="sxs-lookup"><span data-stu-id="ef16b-260">Name</span></span> | <span data-ttu-id="ef16b-261">Enhed</span><span class="sxs-lookup"><span data-stu-id="ef16b-261">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="ef16b-262">Færdighedstype</span><span class="sxs-lookup"><span data-stu-id="ef16b-262">Skill Type</span></span> | <span data-ttu-id="ef16b-263">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="ef16b-263">cdm_skilltype</span></span> |

## <a name="entity-relationship-models"></a><span data-ttu-id="ef16b-264">Enhedsrelationsmodeller</span><span class="sxs-lookup"><span data-stu-id="ef16b-264">Entity relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="ef16b-265">Arbejdstråd</span><span class="sxs-lookup"><span data-stu-id="ef16b-265">Worker</span></span>

![Arbejdstråd](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="ef16b-267">Stilling og job</span><span class="sxs-lookup"><span data-stu-id="ef16b-267">Job and Job Position</span></span>

![Stilling og job](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="ef16b-269">Frynsegoder</span><span class="sxs-lookup"><span data-stu-id="ef16b-269">Benefits</span></span>

![Frynsegoder](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="ef16b-271">Kompensation</span><span class="sxs-lookup"><span data-stu-id="ef16b-271">Compensation</span></span>

![Kompensation](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="ef16b-273">Orlov</span><span class="sxs-lookup"><span data-stu-id="ef16b-273">Leave</span></span>

![Orlov](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="ef16b-275">Arbejdskalender</span><span class="sxs-lookup"><span data-stu-id="ef16b-275">Work Calendar</span></span>

![Arbejdskalender](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="ef16b-277">Se også</span><span class="sxs-lookup"><span data-stu-id="ef16b-277">See also</span></span>

[<span data-ttu-id="ef16b-278">Vælg en dataintegrationsteknologi</span><span class="sxs-lookup"><span data-stu-id="ef16b-278">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)</br>
[<span data-ttu-id="ef16b-279">Konfigurere Common Data Service-integration</span><span class="sxs-lookup"><span data-stu-id="ef16b-279">Configure Common Data Service integration</span></span>](hr-admin-integration-common-data-service.md)