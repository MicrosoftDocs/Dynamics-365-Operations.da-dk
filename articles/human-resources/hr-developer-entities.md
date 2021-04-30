---
title: Dataverse-tabeller
description: Microsoft Dynamics 365 Human Resources bruger Dataverse til at aktivere udvidelses- og integrationsscenarier.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 8ddb74a2f0b6265c5be3c13a009211455ea862da
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893394"
---
# <a name="dataverse-tables"></a><span data-ttu-id="aa278-103">Dataverse-tabeller</span><span class="sxs-lookup"><span data-stu-id="aa278-103">Dataverse tables</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="aa278-104">Microsoft Dynamics 365 Human Resources bruger Dataverse til at aktivere udvidelses- og integrationsscenarier.</span><span class="sxs-lookup"><span data-stu-id="aa278-104">Microsoft Dynamics 365 Human Resources uses Dataverse to enable extensibility and integration scenarios.</span></span>

> [!NOTE]
> <span data-ttu-id="aa278-105">Enheder under Human Resources svarer til Dataverse-tabeller.</span><span class="sxs-lookup"><span data-stu-id="aa278-105">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="aa278-106">Yderligere oplysninger om Dataverse (tidligere Common Data Service) og terminologiopdateringer finder du i [Hvad er Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="aa278-106">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="aa278-107">Følgende Dataverse-tabeller er tilgængelige baseret på Human Resources-enheder.</span><span class="sxs-lookup"><span data-stu-id="aa278-107">The following Dataverse tables are available based on Human Resources entities.</span></span>

## <a name="benefit-tables"></a><span data-ttu-id="aa278-108">Frynsegodetabeller</span><span class="sxs-lookup"><span data-stu-id="aa278-108">Benefit tables</span></span>

| <span data-ttu-id="aa278-109">Navn</span><span class="sxs-lookup"><span data-stu-id="aa278-109">Name</span></span> | <span data-ttu-id="aa278-110">Tabellen</span><span class="sxs-lookup"><span data-stu-id="aa278-110">Table</span></span> |
| --- | --- |
| <span data-ttu-id="aa278-111">Frekvens for personalegodeberegning</span><span class="sxs-lookup"><span data-stu-id="aa278-111">Benefit Calculation Frequency</span></span> | <span data-ttu-id="aa278-112">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="aa278-112">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="aa278-113">Frynsegoders Beregningsfrekvens, betalingsperiode</span><span class="sxs-lookup"><span data-stu-id="aa278-113">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="aa278-114">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="aa278-114">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="aa278-115">Frynsegodeberegningssats</span><span class="sxs-lookup"><span data-stu-id="aa278-115">Benefit Calculation Rate</span></span> | <span data-ttu-id="aa278-116">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="aa278-116">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="aa278-117">Oplysninger om frynsegodeberegningssats</span><span class="sxs-lookup"><span data-stu-id="aa278-117">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="aa278-118">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="aa278-118">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="aa278-119">Frynsegodeindstilling</span><span class="sxs-lookup"><span data-stu-id="aa278-119">Benefit Option</span></span> | <span data-ttu-id="aa278-120">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="aa278-120">cdm_benefitoption</span></span> |
| <span data-ttu-id="aa278-121">Frynsegodeplan</span><span class="sxs-lookup"><span data-stu-id="aa278-121">Benefit Plan</span></span> | <span data-ttu-id="aa278-122">cdm_benefitplan (ikke aktiveret til understøttelse af brugerdefinerede felter)</span><span class="sxs-lookup"><span data-stu-id="aa278-122">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="aa278-123">Human Resourcesgodetype</span><span class="sxs-lookup"><span data-stu-id="aa278-123">Benefit Type</span></span> | <span data-ttu-id="aa278-124">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="aa278-124">cdm_benefittype</span></span> |

## <a name="business-process-tasks-tables"></a><span data-ttu-id="aa278-125">Tabeller for forretningsprocesopgaver</span><span class="sxs-lookup"><span data-stu-id="aa278-125">Business process tasks tables</span></span>

| <span data-ttu-id="aa278-126">Navn</span><span class="sxs-lookup"><span data-stu-id="aa278-126">Name</span></span> | <span data-ttu-id="aa278-127">Tabellen</span><span class="sxs-lookup"><span data-stu-id="aa278-127">Table</span></span> |
| --- | --- |
| <span data-ttu-id="aa278-128">Forretningsproceskalender</span><span class="sxs-lookup"><span data-stu-id="aa278-128">Business Process Calendar</span></span> | <span data-ttu-id="aa278-129">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="aa278-129">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="aa278-130">Tildeling af forretningsprocesgruppe</span><span class="sxs-lookup"><span data-stu-id="aa278-130">Business Process Group Assignment</span></span> | <span data-ttu-id="aa278-131">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="aa278-131">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="aa278-132">Opgavegruppe for forretningsprocesbibliotek</span><span class="sxs-lookup"><span data-stu-id="aa278-132">Business Process Library Task Group</span></span> | <span data-ttu-id="aa278-133">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="aa278-133">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="aa278-134">Forretningsprocesstadie</span><span class="sxs-lookup"><span data-stu-id="aa278-134">Business Process Stage</span></span> | <span data-ttu-id="aa278-135">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="aa278-135">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="aa278-136">Kontrollisteskabelonhoved</span><span class="sxs-lookup"><span data-stu-id="aa278-136">Checklist Template Header</span></span> | <span data-ttu-id="aa278-137">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="aa278-137">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="aa278-138">Tjeklisteskabelonopgave</span><span class="sxs-lookup"><span data-stu-id="aa278-138">Checklist Template Task</span></span> | <span data-ttu-id="aa278-139">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="aa278-139">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-tables"></a><span data-ttu-id="aa278-140">Kompensationstabeller</span><span class="sxs-lookup"><span data-stu-id="aa278-140">Compensation tables</span></span>

| <span data-ttu-id="aa278-141">Navn</span><span class="sxs-lookup"><span data-stu-id="aa278-141">Name</span></span> | <span data-ttu-id="aa278-142">Tabellen</span><span class="sxs-lookup"><span data-stu-id="aa278-142">Table</span></span> |
| --- | --- |
| <span data-ttu-id="aa278-143">Fast lønstruktur</span><span class="sxs-lookup"><span data-stu-id="aa278-143">Compensation Fixed Plan</span></span> | <span data-ttu-id="aa278-144">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="aa278-144">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="aa278-145">Kompensationsgitter</span><span class="sxs-lookup"><span data-stu-id="aa278-145">Compensation Grid</span></span> | <span data-ttu-id="aa278-146">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="aa278-146">cdm_compensationgrid</span></span> |
| <span data-ttu-id="aa278-147">Kompensationsniveau</span><span class="sxs-lookup"><span data-stu-id="aa278-147">Compensation Level</span></span> | <span data-ttu-id="aa278-148">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="aa278-148">cdm_compensationlevel</span></span> |
| <span data-ttu-id="aa278-149">Kompensation - lønfrekvens</span><span class="sxs-lookup"><span data-stu-id="aa278-149">Compensation Pay Frequency</span></span> | <span data-ttu-id="aa278-150">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="aa278-150">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="aa278-151">Opsætning af kompensationsreferencepunkt</span><span class="sxs-lookup"><span data-stu-id="aa278-151">Compensation Reference Point Setup</span></span> | <span data-ttu-id="aa278-152">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="aa278-152">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="aa278-153">Opsætningslinje for kompensationsreferencepunkt</span><span class="sxs-lookup"><span data-stu-id="aa278-153">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="aa278-154">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="aa278-154">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="aa278-155">Kompensationsområde</span><span class="sxs-lookup"><span data-stu-id="aa278-155">Compensation Region</span></span> | <span data-ttu-id="aa278-156">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="aa278-156">cdm_compensationregion</span></span> |
| <span data-ttu-id="aa278-157">Kompensationsstruktur</span><span class="sxs-lookup"><span data-stu-id="aa278-157">Compensation Structure</span></span> | <span data-ttu-id="aa278-158">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="aa278-158">cdm_compensationstructure</span></span> |
| <span data-ttu-id="aa278-159">Variabel kompensationsplan</span><span class="sxs-lookup"><span data-stu-id="aa278-159">Compensation Variable Plan</span></span> | <span data-ttu-id="aa278-160">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="aa278-160">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="aa278-161">Niveau i variabel kompensationsplan</span><span class="sxs-lookup"><span data-stu-id="aa278-161">Compensation Variable Plan Level</span></span> | <span data-ttu-id="aa278-162">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="aa278-162">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="aa278-163">Type af variabel kompensationsplan</span><span class="sxs-lookup"><span data-stu-id="aa278-163">Compensation Variable Plan Type</span></span> | <span data-ttu-id="aa278-164">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="aa278-164">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="aa278-165">Hændelse for fast løn</span><span class="sxs-lookup"><span data-stu-id="aa278-165">Fixed Compensation Event</span></span> | <span data-ttu-id="aa278-166">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="aa278-166">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="aa278-167">Fordelingsregel</span><span class="sxs-lookup"><span data-stu-id="aa278-167">Vesting Rule</span></span> | <span data-ttu-id="aa278-168">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="aa278-168">cdm_vestingrule</span></span> |
| <span data-ttu-id="aa278-169">Arbejders faste løn</span><span class="sxs-lookup"><span data-stu-id="aa278-169">Worker Fixed Compensation</span></span> | <span data-ttu-id="aa278-170">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="aa278-170">cdm_workerfixedcompensation</span></span> |

## <a name="organization-tables"></a><span data-ttu-id="aa278-171">Organisationstabeller</span><span class="sxs-lookup"><span data-stu-id="aa278-171">Organization tables</span></span>

| <span data-ttu-id="aa278-172">Navn</span><span class="sxs-lookup"><span data-stu-id="aa278-172">Name</span></span> | <span data-ttu-id="aa278-173">Tabellen</span><span class="sxs-lookup"><span data-stu-id="aa278-173">Table</span></span> |
| --- | --- |
| <span data-ttu-id="aa278-174">Afdeling</span><span class="sxs-lookup"><span data-stu-id="aa278-174">Department</span></span> | <span data-ttu-id="aa278-175">cdm_department</span><span class="sxs-lookup"><span data-stu-id="aa278-175">cdm_department</span></span> |
| <span data-ttu-id="aa278-176">Ansættelse</span><span class="sxs-lookup"><span data-stu-id="aa278-176">Employment</span></span> | <span data-ttu-id="aa278-177">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="aa278-177">cdm_employment</span></span> |
| <span data-ttu-id="aa278-178">Firma</span><span class="sxs-lookup"><span data-stu-id="aa278-178">Company</span></span> | <span data-ttu-id="aa278-179">cdm_company</span><span class="sxs-lookup"><span data-stu-id="aa278-179">cdm_company</span></span> |
| <span data-ttu-id="aa278-180">Stilling</span><span class="sxs-lookup"><span data-stu-id="aa278-180">Job</span></span> | <span data-ttu-id="aa278-181">cdm_job</span><span class="sxs-lookup"><span data-stu-id="aa278-181">cdm_job</span></span> |
| <span data-ttu-id="aa278-182">Jobfunktion</span><span class="sxs-lookup"><span data-stu-id="aa278-182">Job Function</span></span> | <span data-ttu-id="aa278-183">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="aa278-183">cdm_jobfunction</span></span> |
| <span data-ttu-id="aa278-184">Stilling</span><span class="sxs-lookup"><span data-stu-id="aa278-184">Job Position</span></span> | <span data-ttu-id="aa278-185">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="aa278-185">cdm_jobposition</span></span> |
| <span data-ttu-id="aa278-186">Stillingstype</span><span class="sxs-lookup"><span data-stu-id="aa278-186">Position Type</span></span> | <span data-ttu-id="aa278-187">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="aa278-187">cdm_positiontype</span></span> |
| <span data-ttu-id="aa278-188">Arbejdertildeling til stilling</span><span class="sxs-lookup"><span data-stu-id="aa278-188">Position Worker Assignment</span></span> | <span data-ttu-id="aa278-189">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="aa278-189">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="aa278-190">Stillingsdimension</span><span class="sxs-lookup"><span data-stu-id="aa278-190">Job Position Dimension</span></span> | <span data-ttu-id="aa278-191">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="aa278-191">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="aa278-192">Jobtype</span><span class="sxs-lookup"><span data-stu-id="aa278-192">Job Type</span></span> | <span data-ttu-id="aa278-193">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="aa278-193">cdm_jobtype</span></span> |
| <span data-ttu-id="aa278-194">Sprog</span><span class="sxs-lookup"><span data-stu-id="aa278-194">Language</span></span> | <span data-ttu-id="aa278-195">cdm_language</span><span class="sxs-lookup"><span data-stu-id="aa278-195">cdm_language</span></span> |
| <span data-ttu-id="aa278-196">Stilling</span><span class="sxs-lookup"><span data-stu-id="aa278-196">Title</span></span> | <span data-ttu-id="aa278-197">cdm_title</span><span class="sxs-lookup"><span data-stu-id="aa278-197">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="aa278-198">Økonomiske dimensioner for **Stillingstype**, **Arbejdertildeling til stilling** og **Ansættelse** giver integration i én retning til Dataverse.</span><span class="sxs-lookup"><span data-stu-id="aa278-198">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Dataverse.</span></span> <span data-ttu-id="aa278-199">Opdateringer af økonomiske dimensioner kan i øjeblikket ikke synkroniseres fra Dataverse til HR.</span><span class="sxs-lookup"><span data-stu-id="aa278-199">Financial dimensions updates currently can't synchronize from Dataverse to Human Resources.</span></span> 

## <a name="leave-and-absence-tables"></a><span data-ttu-id="aa278-200">Orlov og fravær-tabeller</span><span class="sxs-lookup"><span data-stu-id="aa278-200">Leave and absence tables</span></span>

| <span data-ttu-id="aa278-201">Navn</span><span class="sxs-lookup"><span data-stu-id="aa278-201">Name</span></span> | <span data-ttu-id="aa278-202">Tabellen</span><span class="sxs-lookup"><span data-stu-id="aa278-202">Table</span></span> |
| --- | --- |
| <span data-ttu-id="aa278-203">Orlovsbanktransaktion</span><span class="sxs-lookup"><span data-stu-id="aa278-203">Leave Bank Transaction</span></span> | <span data-ttu-id="aa278-204">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="aa278-204">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="aa278-205">Orlovstilmelding</span><span class="sxs-lookup"><span data-stu-id="aa278-205">Leave Enrollment</span></span> | <span data-ttu-id="aa278-206">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="aa278-206">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="aa278-207">Orlovsplan</span><span class="sxs-lookup"><span data-stu-id="aa278-207">Leave Plan</span></span> | <span data-ttu-id="aa278-208">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="aa278-208">cdm_leaveplan</span></span> |
| <span data-ttu-id="aa278-209">Orlovsanmodning</span><span class="sxs-lookup"><span data-stu-id="aa278-209">Leave Request</span></span> | <span data-ttu-id="aa278-210">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="aa278-210">cdm_leaverequest</span></span> |
| <span data-ttu-id="aa278-211">Detaljer om orlovsanmodning</span><span class="sxs-lookup"><span data-stu-id="aa278-211">Leave Request Detail</span></span> | <span data-ttu-id="aa278-212">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="aa278-212">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="aa278-213">Orlovstype</span><span class="sxs-lookup"><span data-stu-id="aa278-213">Leave Type</span></span> | <span data-ttu-id="aa278-214">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="aa278-214">cdm_leavetype</span></span> |
| <span data-ttu-id="aa278-215">Orlovstypens årsagskode</span><span class="sxs-lookup"><span data-stu-id="aa278-215">Leave Type Reason Code</span></span> | <span data-ttu-id="aa278-216">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="aa278-216">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-tables"></a><span data-ttu-id="aa278-217">Løntabeller</span><span class="sxs-lookup"><span data-stu-id="aa278-217">Payroll tables</span></span>

| <span data-ttu-id="aa278-218">Navn</span><span class="sxs-lookup"><span data-stu-id="aa278-218">Name</span></span> | <span data-ttu-id="aa278-219">Tabellen</span><span class="sxs-lookup"><span data-stu-id="aa278-219">Table</span></span> |
| --- | --- |
| <span data-ttu-id="aa278-220">Betalingscyklus</span><span class="sxs-lookup"><span data-stu-id="aa278-220">Pay Cycle</span></span> | <span data-ttu-id="aa278-221">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="aa278-221">cdm_paycycle</span></span> |
| <span data-ttu-id="aa278-222">Lønperiode</span><span class="sxs-lookup"><span data-stu-id="aa278-222">Pay Period</span></span> | <span data-ttu-id="aa278-223">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="aa278-223">cdm_payperiod</span></span> |
| <span data-ttu-id="aa278-224">Lønkode</span><span class="sxs-lookup"><span data-stu-id="aa278-224">Payroll Earning Code</span></span> | <span data-ttu-id="aa278-225">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="aa278-225">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="aa278-226">Bankkontoudbetalinger</span><span class="sxs-lookup"><span data-stu-id="aa278-226">Bank Account Disbursement</span></span> | <span data-ttu-id="aa278-227">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="aa278-227">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="aa278-228">Skatteområde</span><span class="sxs-lookup"><span data-stu-id="aa278-228">Tax Region</span></span> | <span data-ttu-id="aa278-229">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="aa278-229">cdm_taxregion</span></span> |

## <a name="worker-tables"></a><span data-ttu-id="aa278-230">Arbejdertabeller</span><span class="sxs-lookup"><span data-stu-id="aa278-230">Worker tables</span></span>

| <span data-ttu-id="aa278-231">Navn</span><span class="sxs-lookup"><span data-stu-id="aa278-231">Name</span></span> | <span data-ttu-id="aa278-232">Tabellen</span><span class="sxs-lookup"><span data-stu-id="aa278-232">Table</span></span> |
| --- | --- |
| <span data-ttu-id="aa278-233">Arbejdstråd</span><span class="sxs-lookup"><span data-stu-id="aa278-233">Worker</span></span> | <span data-ttu-id="aa278-234">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="aa278-234">cdm_worker</span></span> |
| <span data-ttu-id="aa278-235">Arbejderadresse</span><span class="sxs-lookup"><span data-stu-id="aa278-235">Worker Address</span></span> | <span data-ttu-id="aa278-236">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="aa278-236">cdm_workeraddress</span></span> |
| <span data-ttu-id="aa278-237">Arbejders personlige oplysninger</span><span class="sxs-lookup"><span data-stu-id="aa278-237">Worker Personal Detail</span></span> | <span data-ttu-id="aa278-238">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="aa278-238">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="aa278-239">Personidentifikationsnummeret for arbejder</span><span class="sxs-lookup"><span data-stu-id="aa278-239">Worker Person Identification Number</span></span> | <span data-ttu-id="aa278-240">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="aa278-240">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="aa278-241">Personidentifikationstype for arbejder</span><span class="sxs-lookup"><span data-stu-id="aa278-241">Worker Person Identification Type</span></span> | <span data-ttu-id="aa278-242">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="aa278-242">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="aa278-243">Arbejdskalender</span><span class="sxs-lookup"><span data-stu-id="aa278-243">Work Calendar</span></span> | <span data-ttu-id="aa278-244">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="aa278-244">cdm_workcalendar</span></span> |
| <span data-ttu-id="aa278-245">Arbejdskalenderdag</span><span class="sxs-lookup"><span data-stu-id="aa278-245">Work Calendar Day</span></span> | <span data-ttu-id="aa278-246">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="aa278-246">cdm_workcalendarday</span></span> |
| <span data-ttu-id="aa278-247">Arbejdskalenderfridag</span><span class="sxs-lookup"><span data-stu-id="aa278-247">Work Calendar Holiday</span></span> |<span data-ttu-id="aa278-248">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="aa278-248">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="aa278-249">Ferielinje i arbejdskalender</span><span class="sxs-lookup"><span data-stu-id="aa278-249">Work Calendar Holiday Line</span></span> | <span data-ttu-id="aa278-250">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="aa278-250">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="aa278-251">Tidsinterval i arbejdskalender</span><span class="sxs-lookup"><span data-stu-id="aa278-251">Work Calendar Time Interval</span></span> | <span data-ttu-id="aa278-252">cdm_workcalendartimeinterval (ikke aktiveret til understøttelse af brugerdefinerede felter)</span><span class="sxs-lookup"><span data-stu-id="aa278-252">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="aa278-253">Arbejderbankkonto</span><span class="sxs-lookup"><span data-stu-id="aa278-253">Worker Bank Account</span></span> | <span data-ttu-id="aa278-254">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="aa278-254">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-tables"></a><span data-ttu-id="aa278-255">Opsætningstabeller for arbejdere</span><span class="sxs-lookup"><span data-stu-id="aa278-255">Worker setup tables</span></span>

| <span data-ttu-id="aa278-256">Navn</span><span class="sxs-lookup"><span data-stu-id="aa278-256">Name</span></span> | <span data-ttu-id="aa278-257">Tabellen</span><span class="sxs-lookup"><span data-stu-id="aa278-257">Table</span></span> |
| --- | --- |
| <span data-ttu-id="aa278-258">Veteranstatus</span><span class="sxs-lookup"><span data-stu-id="aa278-258">Veteran Status</span></span> | <span data-ttu-id="aa278-259">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="aa278-259">cdm_veteranstatus</span></span> |
| <span data-ttu-id="aa278-260">Etnisk oprindelse</span><span class="sxs-lookup"><span data-stu-id="aa278-260">Ethnic Origin</span></span> | <span data-ttu-id="aa278-261">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="aa278-261">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="aa278-262">Årsagskode</span><span class="sxs-lookup"><span data-stu-id="aa278-262">Reason Code</span></span> | <span data-ttu-id="aa278-263">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="aa278-263">cdm_reasoncode</span></span> |
| <span data-ttu-id="aa278-264">Udstedende organ for personidentifikation</span><span class="sxs-lookup"><span data-stu-id="aa278-264">Person Identification Issuing Agency</span></span> | <span data-ttu-id="aa278-265">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="aa278-265">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-tables"></a><span data-ttu-id="aa278-266">Kompetencetabeller</span><span class="sxs-lookup"><span data-stu-id="aa278-266">Competency tables</span></span>

| <span data-ttu-id="aa278-267">Navn</span><span class="sxs-lookup"><span data-stu-id="aa278-267">Name</span></span> | <span data-ttu-id="aa278-268">Tabellen</span><span class="sxs-lookup"><span data-stu-id="aa278-268">Table</span></span> |
| --- | --- |
| <span data-ttu-id="aa278-269">Kompetencetype</span><span class="sxs-lookup"><span data-stu-id="aa278-269">Skill Type</span></span> | <span data-ttu-id="aa278-270">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="aa278-270">cdm_skilltype</span></span> |

## <a name="table-relationship-models"></a><span data-ttu-id="aa278-271">Tabelrelationsmodeller</span><span class="sxs-lookup"><span data-stu-id="aa278-271">Table relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="aa278-272">Arbejdstråd</span><span class="sxs-lookup"><span data-stu-id="aa278-272">Worker</span></span>

![Arbejdstråd](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="aa278-274">Stilling og job</span><span class="sxs-lookup"><span data-stu-id="aa278-274">Job and Job Position</span></span>

![Stilling og job](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="aa278-276">Frynsegoder</span><span class="sxs-lookup"><span data-stu-id="aa278-276">Benefits</span></span>

![Frynsegoder](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="aa278-278">Kompensation</span><span class="sxs-lookup"><span data-stu-id="aa278-278">Compensation</span></span>

![Kompensation](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="aa278-280">Orlov</span><span class="sxs-lookup"><span data-stu-id="aa278-280">Leave</span></span>

![Orlov](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="aa278-282">Arbejdskalender</span><span class="sxs-lookup"><span data-stu-id="aa278-282">Work Calendar</span></span>

![Arbejdskalender](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="aa278-284">Se også</span><span class="sxs-lookup"><span data-stu-id="aa278-284">See also</span></span>

[<span data-ttu-id="aa278-285">Vælg en dataintegrationsteknologi</span><span class="sxs-lookup"><span data-stu-id="aa278-285">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)<br>
[<span data-ttu-id="aa278-286">Konfigurere Dataverse-integration</span><span class="sxs-lookup"><span data-stu-id="aa278-286">Configure Dataverse integration</span></span>](hr-admin-integration-common-data-service.md)<br>
[<span data-ttu-id="aa278-287">Konfigurere virtuelle Dataverse-tabeller</span><span class="sxs-lookup"><span data-stu-id="aa278-287">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="aa278-288">Ofte stillede spørgsmål om Virtuelle tabeller i Human Resources</span><span class="sxs-lookup"><span data-stu-id="aa278-288">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="aa278-289">Hvad er Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="aa278-289">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="aa278-290">Terminologiopdateringer</span><span class="sxs-lookup"><span data-stu-id="aa278-290">Terminology updates</span></span>](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]