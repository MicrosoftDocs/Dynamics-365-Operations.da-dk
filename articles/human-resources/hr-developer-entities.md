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
ms.openlocfilehash: 988fa0b6d39a49b973626a8a0abe83c546f42297
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/17/2020
ms.locfileid: "4530000"
---
# <a name="common-data-service-entities"></a><span data-ttu-id="1cb1c-103">Common Data Service-enheder</span><span class="sxs-lookup"><span data-stu-id="1cb1c-103">Common Data Service entities</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="1cb1c-104">Microsoft Dynamics 365 Human Resources bruger Common Data Service til at aktivere udvidelses- og integrationsscenarier.</span><span class="sxs-lookup"><span data-stu-id="1cb1c-104">Microsoft Dynamics 365 Human Resources uses Common Data Service to enable extensibility and integration scenarios.</span></span>

<span data-ttu-id="1cb1c-105">Du kan finde flere oplysninger om Common Data Service i [Hvad er Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span><span class="sxs-lookup"><span data-stu-id="1cb1c-105">For more information about Common Data Service, see [What is Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span></span>

<span data-ttu-id="1cb1c-106">Følgende HR-ressourcer er tilgængelige i Common Data Service .</span><span class="sxs-lookup"><span data-stu-id="1cb1c-106">The following Human Resources entities are available in Common Data Service.</span></span>

## <a name="benefit-entities"></a><span data-ttu-id="1cb1c-107">Frynsegodeenheder</span><span class="sxs-lookup"><span data-stu-id="1cb1c-107">Benefit entities</span></span>

| <span data-ttu-id="1cb1c-108">Navn</span><span class="sxs-lookup"><span data-stu-id="1cb1c-108">Name</span></span> | <span data-ttu-id="1cb1c-109">Enhed</span><span class="sxs-lookup"><span data-stu-id="1cb1c-109">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="1cb1c-110">Frekvens for frynsegodeberegning</span><span class="sxs-lookup"><span data-stu-id="1cb1c-110">Benefit Calculation Frequency</span></span> | <span data-ttu-id="1cb1c-111">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="1cb1c-111">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="1cb1c-112">Frynsegoders Beregningsfrekvens, betalingsperiode</span><span class="sxs-lookup"><span data-stu-id="1cb1c-112">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="1cb1c-113">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="1cb1c-113">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="1cb1c-114">Frynsegodeberegningssats</span><span class="sxs-lookup"><span data-stu-id="1cb1c-114">Benefit Calculation Rate</span></span> | <span data-ttu-id="1cb1c-115">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="1cb1c-115">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="1cb1c-116">Oplysninger om frynsegodeberegningssats</span><span class="sxs-lookup"><span data-stu-id="1cb1c-116">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="1cb1c-117">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="1cb1c-117">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="1cb1c-118">Frynsegodeindstilling</span><span class="sxs-lookup"><span data-stu-id="1cb1c-118">Benefit Option</span></span> | <span data-ttu-id="1cb1c-119">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="1cb1c-119">cdm_benefitoption</span></span> |
| <span data-ttu-id="1cb1c-120">Frynsegodeplan</span><span class="sxs-lookup"><span data-stu-id="1cb1c-120">Benefit Plan</span></span> | <span data-ttu-id="1cb1c-121">cdm_benefitplan (ikke aktiveret til understøttelse af brugerdefinerede felter)</span><span class="sxs-lookup"><span data-stu-id="1cb1c-121">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="1cb1c-122">Frynsegodetype</span><span class="sxs-lookup"><span data-stu-id="1cb1c-122">Benefit Type</span></span> | <span data-ttu-id="1cb1c-123">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="1cb1c-123">cdm_benefittype</span></span> |

## <a name="business-process-tasks-entities"></a><span data-ttu-id="1cb1c-124">Enheder for forretningsprocesopgaver</span><span class="sxs-lookup"><span data-stu-id="1cb1c-124">Business process tasks entities</span></span>

| <span data-ttu-id="1cb1c-125">Navn</span><span class="sxs-lookup"><span data-stu-id="1cb1c-125">Name</span></span> | <span data-ttu-id="1cb1c-126">Enhed</span><span class="sxs-lookup"><span data-stu-id="1cb1c-126">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="1cb1c-127">Forretningsproceskalender</span><span class="sxs-lookup"><span data-stu-id="1cb1c-127">Business Process Calendar</span></span> | <span data-ttu-id="1cb1c-128">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="1cb1c-128">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="1cb1c-129">Tildeling af forretningsprocesgruppe</span><span class="sxs-lookup"><span data-stu-id="1cb1c-129">Business Process Group Assignment</span></span> | <span data-ttu-id="1cb1c-130">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="1cb1c-130">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="1cb1c-131">Opgavegruppe for forretningsprocesbibliotek</span><span class="sxs-lookup"><span data-stu-id="1cb1c-131">Business Process Library Task Group</span></span> | <span data-ttu-id="1cb1c-132">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="1cb1c-132">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="1cb1c-133">Forretningsprocesstadie</span><span class="sxs-lookup"><span data-stu-id="1cb1c-133">Business Process Stage</span></span> | <span data-ttu-id="1cb1c-134">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="1cb1c-134">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="1cb1c-135">Kontrollisteskabelonhoved</span><span class="sxs-lookup"><span data-stu-id="1cb1c-135">Checklist Template Header</span></span> | <span data-ttu-id="1cb1c-136">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="1cb1c-136">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="1cb1c-137">Kontrollisteskabelonopgave</span><span class="sxs-lookup"><span data-stu-id="1cb1c-137">Checklist Template Task</span></span> | <span data-ttu-id="1cb1c-138">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="1cb1c-138">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-entities"></a><span data-ttu-id="1cb1c-139">Kompensationsenheder</span><span class="sxs-lookup"><span data-stu-id="1cb1c-139">Compensation entities</span></span>

| <span data-ttu-id="1cb1c-140">Navn</span><span class="sxs-lookup"><span data-stu-id="1cb1c-140">Name</span></span> | <span data-ttu-id="1cb1c-141">Enhed</span><span class="sxs-lookup"><span data-stu-id="1cb1c-141">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="1cb1c-142">Kompensation - fast struktur</span><span class="sxs-lookup"><span data-stu-id="1cb1c-142">Compensation Fixed Plan</span></span> | <span data-ttu-id="1cb1c-143">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="1cb1c-143">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="1cb1c-144">Kompensationsgitter</span><span class="sxs-lookup"><span data-stu-id="1cb1c-144">Compensation Grid</span></span> | <span data-ttu-id="1cb1c-145">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="1cb1c-145">cdm_compensationgrid</span></span> |
| <span data-ttu-id="1cb1c-146">Kompensationsniveau</span><span class="sxs-lookup"><span data-stu-id="1cb1c-146">Compensation Level</span></span> | <span data-ttu-id="1cb1c-147">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="1cb1c-147">cdm_compensationlevel</span></span> |
| <span data-ttu-id="1cb1c-148">Kompensation - lønfrekvens</span><span class="sxs-lookup"><span data-stu-id="1cb1c-148">Compensation Pay Frequency</span></span> | <span data-ttu-id="1cb1c-149">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="1cb1c-149">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="1cb1c-150">Opsætning af kompensationsreferencepunkt</span><span class="sxs-lookup"><span data-stu-id="1cb1c-150">Compensation Reference Point Setup</span></span> | <span data-ttu-id="1cb1c-151">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="1cb1c-151">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="1cb1c-152">Opsætningslinje for kompensationsreferencepunkt</span><span class="sxs-lookup"><span data-stu-id="1cb1c-152">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="1cb1c-153">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="1cb1c-153">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="1cb1c-154">Kompensationsområde</span><span class="sxs-lookup"><span data-stu-id="1cb1c-154">Compensation Region</span></span> | <span data-ttu-id="1cb1c-155">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="1cb1c-155">cdm_compensationregion</span></span> |
| <span data-ttu-id="1cb1c-156">Kompensationsstruktur</span><span class="sxs-lookup"><span data-stu-id="1cb1c-156">Compensation Structure</span></span> | <span data-ttu-id="1cb1c-157">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="1cb1c-157">cdm_compensationstructure</span></span> |
| <span data-ttu-id="1cb1c-158">Variabel kompensationsplan</span><span class="sxs-lookup"><span data-stu-id="1cb1c-158">Compensation Variable Plan</span></span> | <span data-ttu-id="1cb1c-159">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="1cb1c-159">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="1cb1c-160">Niveau i variabel kompensationsplan</span><span class="sxs-lookup"><span data-stu-id="1cb1c-160">Compensation Variable Plan Level</span></span> | <span data-ttu-id="1cb1c-161">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="1cb1c-161">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="1cb1c-162">Type af variabel kompensationsplan</span><span class="sxs-lookup"><span data-stu-id="1cb1c-162">Compensation Variable Plan Type</span></span> | <span data-ttu-id="1cb1c-163">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="1cb1c-163">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="1cb1c-164">Hændelse for fast løn</span><span class="sxs-lookup"><span data-stu-id="1cb1c-164">Fixed Compensation Event</span></span> | <span data-ttu-id="1cb1c-165">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="1cb1c-165">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="1cb1c-166">Fordelingsregel</span><span class="sxs-lookup"><span data-stu-id="1cb1c-166">Vesting Rule</span></span> | <span data-ttu-id="1cb1c-167">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="1cb1c-167">cdm_vestingrule</span></span> |
| <span data-ttu-id="1cb1c-168">Arbejders faste løn</span><span class="sxs-lookup"><span data-stu-id="1cb1c-168">Worker Fixed Compensation</span></span> | <span data-ttu-id="1cb1c-169">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="1cb1c-169">cdm_workerfixedcompensation</span></span> |

## <a name="organization-entities"></a><span data-ttu-id="1cb1c-170">Organisationsenheder</span><span class="sxs-lookup"><span data-stu-id="1cb1c-170">Organization entities</span></span>

| <span data-ttu-id="1cb1c-171">Navn</span><span class="sxs-lookup"><span data-stu-id="1cb1c-171">Name</span></span> | <span data-ttu-id="1cb1c-172">Enhed</span><span class="sxs-lookup"><span data-stu-id="1cb1c-172">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="1cb1c-173">Afdeling</span><span class="sxs-lookup"><span data-stu-id="1cb1c-173">Department</span></span> | <span data-ttu-id="1cb1c-174">cdm_department</span><span class="sxs-lookup"><span data-stu-id="1cb1c-174">cdm_department</span></span> |
| <span data-ttu-id="1cb1c-175">Ansættelse</span><span class="sxs-lookup"><span data-stu-id="1cb1c-175">Employment</span></span> | <span data-ttu-id="1cb1c-176">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="1cb1c-176">cdm_employment</span></span> |
| <span data-ttu-id="1cb1c-177">Regnskab</span><span class="sxs-lookup"><span data-stu-id="1cb1c-177">Company</span></span> | <span data-ttu-id="1cb1c-178">cdm_company</span><span class="sxs-lookup"><span data-stu-id="1cb1c-178">cdm_company</span></span> |
| <span data-ttu-id="1cb1c-179">Stilling</span><span class="sxs-lookup"><span data-stu-id="1cb1c-179">Job</span></span> | <span data-ttu-id="1cb1c-180">cdm_job</span><span class="sxs-lookup"><span data-stu-id="1cb1c-180">cdm_job</span></span> |
| <span data-ttu-id="1cb1c-181">Jobfunktion</span><span class="sxs-lookup"><span data-stu-id="1cb1c-181">Job Function</span></span> | <span data-ttu-id="1cb1c-182">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="1cb1c-182">cdm_jobfunction</span></span> |
| <span data-ttu-id="1cb1c-183">Stilling</span><span class="sxs-lookup"><span data-stu-id="1cb1c-183">Job Position</span></span> | <span data-ttu-id="1cb1c-184">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="1cb1c-184">cdm_jobposition</span></span> |
| <span data-ttu-id="1cb1c-185">Stillingstype</span><span class="sxs-lookup"><span data-stu-id="1cb1c-185">Position Type</span></span> | <span data-ttu-id="1cb1c-186">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="1cb1c-186">cdm_positiontype</span></span> |
| <span data-ttu-id="1cb1c-187">Arbejdertildeling til stilling</span><span class="sxs-lookup"><span data-stu-id="1cb1c-187">Position Worker Assignment</span></span> | <span data-ttu-id="1cb1c-188">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="1cb1c-188">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="1cb1c-189">Stillingsdimension</span><span class="sxs-lookup"><span data-stu-id="1cb1c-189">Job Position Dimension</span></span> | <span data-ttu-id="1cb1c-190">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="1cb1c-190">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="1cb1c-191">Jobtype</span><span class="sxs-lookup"><span data-stu-id="1cb1c-191">Job Type</span></span> | <span data-ttu-id="1cb1c-192">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="1cb1c-192">cdm_jobtype</span></span> |
| <span data-ttu-id="1cb1c-193">Sprog</span><span class="sxs-lookup"><span data-stu-id="1cb1c-193">Language</span></span> | <span data-ttu-id="1cb1c-194">cdm_language</span><span class="sxs-lookup"><span data-stu-id="1cb1c-194">cdm_language</span></span> |
| <span data-ttu-id="1cb1c-195">Stilling</span><span class="sxs-lookup"><span data-stu-id="1cb1c-195">Title</span></span> | <span data-ttu-id="1cb1c-196">cdm_title</span><span class="sxs-lookup"><span data-stu-id="1cb1c-196">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="1cb1c-197">Økonomiske dimensioner for **Stillingstype**, **Arbejdertildeling til stilling** og **Ansættelse** giver integration i én retning til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="1cb1c-197">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Common Data Service.</span></span> <span data-ttu-id="1cb1c-198">Opdateringer af økonomiske dimensioner kan i øjeblikket ikke synkroniseres fra Common Data Service til HR.</span><span class="sxs-lookup"><span data-stu-id="1cb1c-198">Financial dimensions updates currently can't synchronize from Common Data Service to Human Resources.</span></span> 

## <a name="leave-and-absence-entities"></a><span data-ttu-id="1cb1c-199">Orlovs- og fraværsenheder</span><span class="sxs-lookup"><span data-stu-id="1cb1c-199">Leave and absence entities</span></span>

| <span data-ttu-id="1cb1c-200">Navn</span><span class="sxs-lookup"><span data-stu-id="1cb1c-200">Name</span></span> | <span data-ttu-id="1cb1c-201">Enhed</span><span class="sxs-lookup"><span data-stu-id="1cb1c-201">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="1cb1c-202">Orlovsbanktransaktion</span><span class="sxs-lookup"><span data-stu-id="1cb1c-202">Leave Bank Transaction</span></span> | <span data-ttu-id="1cb1c-203">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="1cb1c-203">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="1cb1c-204">Orlovstilmelding</span><span class="sxs-lookup"><span data-stu-id="1cb1c-204">Leave Enrollment</span></span> | <span data-ttu-id="1cb1c-205">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="1cb1c-205">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="1cb1c-206">Orlovsplan</span><span class="sxs-lookup"><span data-stu-id="1cb1c-206">Leave Plan</span></span> | <span data-ttu-id="1cb1c-207">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="1cb1c-207">cdm_leaveplan</span></span> |
| <span data-ttu-id="1cb1c-208">Orlovsanmodning</span><span class="sxs-lookup"><span data-stu-id="1cb1c-208">Leave Request</span></span> | <span data-ttu-id="1cb1c-209">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="1cb1c-209">cdm_leaverequest</span></span> |
| <span data-ttu-id="1cb1c-210">Detaljer om orlovsanmodning</span><span class="sxs-lookup"><span data-stu-id="1cb1c-210">Leave Request Detail</span></span> | <span data-ttu-id="1cb1c-211">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="1cb1c-211">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="1cb1c-212">Orlovstype</span><span class="sxs-lookup"><span data-stu-id="1cb1c-212">Leave Type</span></span> | <span data-ttu-id="1cb1c-213">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="1cb1c-213">cdm_leavetype</span></span> |
| <span data-ttu-id="1cb1c-214">Orlovstypens årsagskode</span><span class="sxs-lookup"><span data-stu-id="1cb1c-214">Leave Type Reason Code</span></span> | <span data-ttu-id="1cb1c-215">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="1cb1c-215">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-entities"></a><span data-ttu-id="1cb1c-216">Lønenheder</span><span class="sxs-lookup"><span data-stu-id="1cb1c-216">Payroll entities</span></span>

| <span data-ttu-id="1cb1c-217">Navn</span><span class="sxs-lookup"><span data-stu-id="1cb1c-217">Name</span></span> | <span data-ttu-id="1cb1c-218">Enhed</span><span class="sxs-lookup"><span data-stu-id="1cb1c-218">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="1cb1c-219">Betalingscyklus</span><span class="sxs-lookup"><span data-stu-id="1cb1c-219">Pay Cycle</span></span> | <span data-ttu-id="1cb1c-220">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="1cb1c-220">cdm_paycycle</span></span> |
| <span data-ttu-id="1cb1c-221">Lønperiode</span><span class="sxs-lookup"><span data-stu-id="1cb1c-221">Pay Period</span></span> | <span data-ttu-id="1cb1c-222">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="1cb1c-222">cdm_payperiod</span></span> |
| <span data-ttu-id="1cb1c-223">Lønkode</span><span class="sxs-lookup"><span data-stu-id="1cb1c-223">Payroll Earning Code</span></span> | <span data-ttu-id="1cb1c-224">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="1cb1c-224">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="1cb1c-225">Bankkontoudbetalinger</span><span class="sxs-lookup"><span data-stu-id="1cb1c-225">Bank Account Disbursement</span></span> | <span data-ttu-id="1cb1c-226">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="1cb1c-226">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="1cb1c-227">Skatteområde</span><span class="sxs-lookup"><span data-stu-id="1cb1c-227">Tax Region</span></span> | <span data-ttu-id="1cb1c-228">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="1cb1c-228">cdm_taxregion</span></span> |

## <a name="worker-entities"></a><span data-ttu-id="1cb1c-229">Enheder for arbejder</span><span class="sxs-lookup"><span data-stu-id="1cb1c-229">Worker entities</span></span>

| <span data-ttu-id="1cb1c-230">Navn</span><span class="sxs-lookup"><span data-stu-id="1cb1c-230">Name</span></span> | <span data-ttu-id="1cb1c-231">Enhed</span><span class="sxs-lookup"><span data-stu-id="1cb1c-231">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="1cb1c-232">Arbejdstråd</span><span class="sxs-lookup"><span data-stu-id="1cb1c-232">Worker</span></span> | <span data-ttu-id="1cb1c-233">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="1cb1c-233">cdm_worker</span></span> |
| <span data-ttu-id="1cb1c-234">Arbejders adresse</span><span class="sxs-lookup"><span data-stu-id="1cb1c-234">Worker Address</span></span> | <span data-ttu-id="1cb1c-235">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="1cb1c-235">cdm_workeraddress</span></span> |
| <span data-ttu-id="1cb1c-236">Arbejders personlige oplysninger</span><span class="sxs-lookup"><span data-stu-id="1cb1c-236">Worker Personal Detail</span></span> | <span data-ttu-id="1cb1c-237">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="1cb1c-237">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="1cb1c-238">Personidentifikationsnummeret for arbejder</span><span class="sxs-lookup"><span data-stu-id="1cb1c-238">Worker Person Identification Number</span></span> | <span data-ttu-id="1cb1c-239">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="1cb1c-239">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="1cb1c-240">Personidentifikationstype for arbejder</span><span class="sxs-lookup"><span data-stu-id="1cb1c-240">Worker Person Identification Type</span></span> | <span data-ttu-id="1cb1c-241">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="1cb1c-241">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="1cb1c-242">Arbejdskalender</span><span class="sxs-lookup"><span data-stu-id="1cb1c-242">Work Calendar</span></span> | <span data-ttu-id="1cb1c-243">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="1cb1c-243">cdm_workcalendar</span></span> |
| <span data-ttu-id="1cb1c-244">Arbejdskalenderdag</span><span class="sxs-lookup"><span data-stu-id="1cb1c-244">Work Calendar Day</span></span> | <span data-ttu-id="1cb1c-245">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="1cb1c-245">cdm_workcalendarday</span></span> |
| <span data-ttu-id="1cb1c-246">Arbejdskalenderfridag</span><span class="sxs-lookup"><span data-stu-id="1cb1c-246">Work Calendar Holiday</span></span> |<span data-ttu-id="1cb1c-247">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="1cb1c-247">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="1cb1c-248">Ferielinje i arbejdskalender</span><span class="sxs-lookup"><span data-stu-id="1cb1c-248">Work Calendar Holiday Line</span></span> | <span data-ttu-id="1cb1c-249">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="1cb1c-249">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="1cb1c-250">Tidsinterval i arbejdskalender</span><span class="sxs-lookup"><span data-stu-id="1cb1c-250">Work Calendar Time Interval</span></span> | <span data-ttu-id="1cb1c-251">cdm_workcalendartimeinterval (ikke aktiveret til understøttelse af brugerdefinerede felter)</span><span class="sxs-lookup"><span data-stu-id="1cb1c-251">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="1cb1c-252">Arbejders bankkonto</span><span class="sxs-lookup"><span data-stu-id="1cb1c-252">Worker Bank Account</span></span> | <span data-ttu-id="1cb1c-253">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="1cb1c-253">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-entities"></a><span data-ttu-id="1cb1c-254">Enheder til opsætning af arbejder</span><span class="sxs-lookup"><span data-stu-id="1cb1c-254">Worker setup entities</span></span>

| <span data-ttu-id="1cb1c-255">Navn</span><span class="sxs-lookup"><span data-stu-id="1cb1c-255">Name</span></span> | <span data-ttu-id="1cb1c-256">Enhed</span><span class="sxs-lookup"><span data-stu-id="1cb1c-256">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="1cb1c-257">Veteranstatus</span><span class="sxs-lookup"><span data-stu-id="1cb1c-257">Veteran Status</span></span> | <span data-ttu-id="1cb1c-258">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="1cb1c-258">cdm_veteranstatus</span></span> |
| <span data-ttu-id="1cb1c-259">Etnisk oprindelse</span><span class="sxs-lookup"><span data-stu-id="1cb1c-259">Ethnic Origin</span></span> | <span data-ttu-id="1cb1c-260">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="1cb1c-260">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="1cb1c-261">Årsagskode</span><span class="sxs-lookup"><span data-stu-id="1cb1c-261">Reason Code</span></span> | <span data-ttu-id="1cb1c-262">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="1cb1c-262">cdm_reasoncode</span></span> |
| <span data-ttu-id="1cb1c-263">Udstedende organ for personidentifikation</span><span class="sxs-lookup"><span data-stu-id="1cb1c-263">Person Identification Issuing Agency</span></span> | <span data-ttu-id="1cb1c-264">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="1cb1c-264">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-entities"></a><span data-ttu-id="1cb1c-265">Kompetenceenheder</span><span class="sxs-lookup"><span data-stu-id="1cb1c-265">Competency entities</span></span>

| <span data-ttu-id="1cb1c-266">Navn</span><span class="sxs-lookup"><span data-stu-id="1cb1c-266">Name</span></span> | <span data-ttu-id="1cb1c-267">Enhed</span><span class="sxs-lookup"><span data-stu-id="1cb1c-267">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="1cb1c-268">Færdighedstype</span><span class="sxs-lookup"><span data-stu-id="1cb1c-268">Skill Type</span></span> | <span data-ttu-id="1cb1c-269">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="1cb1c-269">cdm_skilltype</span></span> |

## <a name="entity-relationship-models"></a><span data-ttu-id="1cb1c-270">Enhedsrelationsmodeller</span><span class="sxs-lookup"><span data-stu-id="1cb1c-270">Entity relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="1cb1c-271">Arbejdstråd</span><span class="sxs-lookup"><span data-stu-id="1cb1c-271">Worker</span></span>

![Arbejdstråd](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="1cb1c-273">Stilling og job</span><span class="sxs-lookup"><span data-stu-id="1cb1c-273">Job and Job Position</span></span>

![Stilling og job](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="1cb1c-275">Frynsegoder</span><span class="sxs-lookup"><span data-stu-id="1cb1c-275">Benefits</span></span>

![Frynsegoder](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="1cb1c-277">Kompensation</span><span class="sxs-lookup"><span data-stu-id="1cb1c-277">Compensation</span></span>

![Kompensation](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="1cb1c-279">Orlov</span><span class="sxs-lookup"><span data-stu-id="1cb1c-279">Leave</span></span>

![Orlov](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="1cb1c-281">Arbejdskalender</span><span class="sxs-lookup"><span data-stu-id="1cb1c-281">Work Calendar</span></span>

![Arbejdskalender](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="1cb1c-283">Se også</span><span class="sxs-lookup"><span data-stu-id="1cb1c-283">See also</span></span>

[<span data-ttu-id="1cb1c-284">Vælg en dataintegrationsteknologi</span><span class="sxs-lookup"><span data-stu-id="1cb1c-284">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)</br>
[<span data-ttu-id="1cb1c-285">Konfigurere Common Data Service-integration</span><span class="sxs-lookup"><span data-stu-id="1cb1c-285">Configure Common Data Service integration</span></span>](hr-admin-integration-common-data-service.md)
