---
title: Nyheder eller ændringer i Dynamics 365 for Talent Core HR (14. december 2018)
description: Dette emne beskriver funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 12/14/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-12-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c2d209cac52665053b664a93bfb6c35e171b0948
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517595"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-december-14-2018"></a><span data-ttu-id="fa6ba-103">Nyheder eller ændringer i Dynamics 365 for Talent Core HR (14. december 2018)</span><span class="sxs-lookup"><span data-stu-id="fa6ba-103">What's new or changed in Dynamics 365 for Talent Core HR (December 14, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fa6ba-104">**Build 8.1.2085**</span><span class="sxs-lookup"><span data-stu-id="fa6ba-104">**Build 8.1.2085**</span></span>

<span data-ttu-id="fa6ba-105">Dette emne beskriver funktioner, der enten er nye eller ændrede i Core HR.</span><span class="sxs-lookup"><span data-stu-id="fa6ba-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="changes"></a><span data-ttu-id="fa6ba-106">Ændringer</span><span class="sxs-lookup"><span data-stu-id="fa6ba-106">Changes</span></span>

### <a name="us---aca-affordable-care-act-support-for-tax-year-2018-1095-b-and-1095-c-forms"></a><span data-ttu-id="fa6ba-107">USA - ACA-understøttelse (Affordable Care Act) med formularerne 1095-B og C-1095 for skatteåret 2018</span><span class="sxs-lookup"><span data-stu-id="fa6ba-107">US - ACA (Affordable Care Act) support for tax year 2018 1095-B and 1095-C forms</span></span>

<span data-ttu-id="fa6ba-108">Hvert år skal ALE (Applicable Large Employers) levere en 1095-C til hver fuldtidsansat.</span><span class="sxs-lookup"><span data-stu-id="fa6ba-108">Each year, Applicable Large Employers (ALEs) must provide each full-time employees with a 1095-C.</span></span> <span data-ttu-id="fa6ba-109">Hvis arbejdsgiveren derudover har sygesikringsordning med egendækning, skal han eller hun levere 1095-C (hvis det er en ALE) og 1095-B (hvis det er en lille arbejdsgiver) til en medarbejder på fuld tid eller på deltid, der er omfattet af et af deres tilbudte sygesikringsprogrammer.</span><span class="sxs-lookup"><span data-stu-id="fa6ba-109">In addition, if the employer provides self-insured coverage they must provide the 1095-C (if they are an ALE) and a 1095-B (if they are a small employer) to any employee, full-time or part-time, covered under one of their offered health plans.</span></span> <span data-ttu-id="fa6ba-110">Denne funktion leverer formularer, der kan udskrives, til både 1095-C- og 1095 B.</span><span class="sxs-lookup"><span data-stu-id="fa6ba-110">This feature provides printable forms for both the 1095-C and 1095-B.</span></span>

### <a name="during-import-submittedbypersonid-field-on-hcmperfjournalentity-is-ignored"></a><span data-ttu-id="fa6ba-111">Feltet SubmittedByPersonId i HcmPerfJournalEntity ignoreres under import</span><span class="sxs-lookup"><span data-stu-id="fa6ba-111">During import SubmittedByPersonId field on HcmPerfJournalEntity is ignored</span></span>

<span data-ttu-id="fa6ba-112">Når kladdeposteringer importeres eller eksporteres, ignoreres feltet **Sendt af**.</span><span class="sxs-lookup"><span data-stu-id="fa6ba-112">When importing/exporting performance journal entries, the **Submitted by** field is ignored.</span></span> <span data-ttu-id="fa6ba-113">Med denne ændring afspejler værdien **importeret/eksporteret** værdien i tabellen under eksport. Under import opdateres systemet med den værdi, der er angivet i importfilen.</span><span class="sxs-lookup"><span data-stu-id="fa6ba-113">With this change, the value **imported/exported** will reflect the value in the table during the export, when importing the system will be updated with the value supplied in the import file.</span></span>

### <a name="analytics-tab-on-leave-and-absence-workspace-displays-openconnectionerror-error-for-non-system-admin-roles"></a><span data-ttu-id="fa6ba-114">Fanen Analyser i 'Orlov og fravær' arbejdsområdet viser "OpenConnectionError"-fejl for ikke-system-administratorroller</span><span class="sxs-lookup"><span data-stu-id="fa6ba-114">Analytics tab on 'Leave and absence' workspace displays "OpenConnectionError" error for non-system Admin roles</span></span>

<span data-ttu-id="fa6ba-115">Med denne opdatering opstår der ikke fejl, når du åbner fanen **Analyser** i **Orlov og fravær**-arbejdsområdet.</span><span class="sxs-lookup"><span data-stu-id="fa6ba-115">With this update, no errors will be issued when opening the **Analytics** tab on the **Leave and Absence** workspace.</span></span>

### <a name="employee-self-service-position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a><span data-ttu-id="fa6ba-116">Medarbejderselvbetjening, Stillingshierarki-detailudledning fra felt kan ikke hente overordnet node</span><span class="sxs-lookup"><span data-stu-id="fa6ba-116">Employee self-service, Position Hierarchy drill-down from tile fails to get parent node</span></span>

<span data-ttu-id="fa6ba-117">Der er foretaget en ændring for at rette fejlen "Den overordnede node kunne ikke hentes", når stillingshierarkiet er blevet tilpasset, så det kan vises i et eksisterende arbejdsområde, og der er valgt en stilling i hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="fa6ba-117">A change has been made to correct the error "Getting the parent node failed" when the position hierarchy has been personalized to appear on an existing workspace and a position is selected in the hierarchy.</span></span>  

### <a name="must-be-system-admin-to-see-the-payroll-tab-in-the-position-page"></a><span data-ttu-id="fa6ba-118">Du skal være systemadministrator for at få vist fanen Løn på siden Stilling.</span><span class="sxs-lookup"><span data-stu-id="fa6ba-118">Must be System Admin to see the Payroll tab in the Position page</span></span>

<span data-ttu-id="fa6ba-119">Der er foretaget en ændring, så de korrekte sikkerhedselementer medtages i den eksisterende rettighed: "Vedligehold oplysninger om lønarbejder og stilling".</span><span class="sxs-lookup"><span data-stu-id="fa6ba-119">A change has been made to include the correct security elements in the existing privilege: "Maintain payroll worker and position detail".</span></span> <span data-ttu-id="fa6ba-120">Med denne ændring får lønadministratoren som standard adgang til Løn-felterne på siden Stilling.</span><span class="sxs-lookup"><span data-stu-id="fa6ba-120">With this change, by default, the Payroll Administrator will have access to the Payroll fields on the Position page.</span></span>

### <a name="error-when-submitting-performance-review-to-manager-and-the-reviewsperfperiod-placeholder-is-used-in-the-submission-instructions"></a><span data-ttu-id="fa6ba-121">Der opstod en fejl under afsendelse af performancegennemgang til chef, og pladsholderen %Reviews.PerfPeriod% bruges i indgivelsesinstruktionerne</span><span class="sxs-lookup"><span data-stu-id="fa6ba-121">Error when submitting performance review to manager and the %Reviews.PerfPeriod% placeholder is used in the Submission instructions</span></span>

<span data-ttu-id="fa6ba-122">Der er foretaget en ændring, der retter fejlen "Null-reference", når du bruger pladsholderen %Reviews.PerfPeriod% i indgivelsesinstruktionerne.</span><span class="sxs-lookup"><span data-stu-id="fa6ba-122">A change has been made that corrects the "Null Reference" error when using the %Reviews.PerfPeriod% placeholder in the Submission instructions.</span></span>

### <a name="workforce-power-bi-report-shows-error-when-worker-seniority-date-is-a-leap-day"></a><span data-ttu-id="fa6ba-123">Power BI-personalerapporten viser fejl, når arbejderens anciennitetsdato er en skuddag</span><span class="sxs-lookup"><span data-stu-id="fa6ba-123">Workforce Power BI report shows error when worker seniority date is a leap day</span></span>

<span data-ttu-id="fa6ba-124">Med denne ændring understøttes skuddage nu i Power BI.</span><span class="sxs-lookup"><span data-stu-id="fa6ba-124">With this change, leap days are now supported in Power BI.</span></span>

### <a name="integration-between-core-hr-and-attract"></a><span data-ttu-id="fa6ba-125">Integration mellem Core HR og Attract</span><span class="sxs-lookup"><span data-stu-id="fa6ba-125">Integration between Core HR and Attract</span></span>

<span data-ttu-id="fa6ba-126">Der er foretaget en ændring, så den integration mellem Core HR og Attract, der er relateret til ansøgere, der skal ansættes, opdateres.</span><span class="sxs-lookup"><span data-stu-id="fa6ba-126">A change has been made to update the integration between Core HR and Attract related to candidates to hire.</span></span> <span data-ttu-id="fa6ba-127">For at gøre de kandidater, der skal ansættes, synlige i arbejdsområdet **Personalestyring** anvendes følgende Common Data Service-enheder:</span><span class="sxs-lookup"><span data-stu-id="fa6ba-127">For candidates to hire to be visible in the **Personnel Management** workspace, the following Common Data Service entities are used:</span></span>

<span data-ttu-id="fa6ba-128">Jobansøgning</span><span class="sxs-lookup"><span data-stu-id="fa6ba-128">Job Application</span></span>
- <span data-ttu-id="fa6ba-129">Statusårsag skal være indstillet til Tilbud accepteret</span><span class="sxs-lookup"><span data-stu-id="fa6ba-129">Status Reason needs to be set to Offer Accepted</span></span>
-   <span data-ttu-id="fa6ba-130">Indeholder en ansøger og jobmuligheder</span><span class="sxs-lookup"><span data-stu-id="fa6ba-130">Provides Candidate and Job Opening</span></span>

<span data-ttu-id="fa6ba-131">Kandidat</span><span class="sxs-lookup"><span data-stu-id="fa6ba-131">Candidate</span></span>
-   <span data-ttu-id="fa6ba-132">Angiver oplysninger om kandidaten</span><span class="sxs-lookup"><span data-stu-id="fa6ba-132">Provides Candidate information</span></span>

<span data-ttu-id="fa6ba-133">Jobmulighed</span><span class="sxs-lookup"><span data-stu-id="fa6ba-133">Job Opening</span></span>
-   <span data-ttu-id="fa6ba-134">Angiver id for jobmulighed og deltagere i jobmulighed</span><span class="sxs-lookup"><span data-stu-id="fa6ba-134">Provides Job Opening ID and Job Opening Participants</span></span>

<span data-ttu-id="fa6ba-135">Deltagere i jobmulighed</span><span class="sxs-lookup"><span data-stu-id="fa6ba-135">Job Opening Participants</span></span>
-   <span data-ttu-id="fa6ba-136">Angiver ansættelseschef</span><span class="sxs-lookup"><span data-stu-id="fa6ba-136">Provides Hiring Manager</span></span>

<span data-ttu-id="fa6ba-137">Når en ansøger føjes til Personalestyring, kan vedkommende nu også afskediges ved hjælp af en ny indstilling, der er tilgængelig på kandidatkortet.</span><span class="sxs-lookup"><span data-stu-id="fa6ba-137">When a candidate is added to Personnel Management, the candidate can now also be dismissed using a new option available on the candidate card.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="fa6ba-138">Kommer snart</span><span class="sxs-lookup"><span data-stu-id="fa6ba-138">Coming soon</span></span>

### <a name="leave-and-absence-future-leave-and-forecasting-leave-balances"></a><span data-ttu-id="fa6ba-139">Orlov og fravær: fremtidig orlov og budgettering af orlovssaldi</span><span class="sxs-lookup"><span data-stu-id="fa6ba-139">Leave and absence: Future leave and forecasting leave balances</span></span>

<span data-ttu-id="fa6ba-140">Med de ændringer, der foretages, så medarbejderne kan budgettere fritid og anmode om fremtidig fritid, uden at det påvirker deres aktuelle fritidssaldi, ændres den måde, som fritidssaldi vises på, også.</span><span class="sxs-lookup"><span data-stu-id="fa6ba-140">With the changes being made to allow for employees to forecast time off and request future time off requests without impacting their current time off balances, the way the time off balances are displayed is also changing.</span></span> 

<span data-ttu-id="fa6ba-141">Den disponible saldo, der aktuelt vises, er mængden af fritid, der er tilgængelig for anmodninger, herunder periodiseringer, til og med i dag og alle godkendte orlovsanmodninger og i al fremtid.</span><span class="sxs-lookup"><span data-stu-id="fa6ba-141">The available balance currently displayed is the amount of time off available for requests including accruals through today and all approved leave requests to the end of time.</span></span> 

<span data-ttu-id="fa6ba-142">Når der gives mulighed for budgettering, ændres den viste saldo til den aktuelle fritidssaldo, herunder periodiseringer til og med i dag og anmodninger til og med dags dato.</span><span class="sxs-lookup"><span data-stu-id="fa6ba-142">When the ability to forecast is released, the balance displayed changes to  be the current balance of time off including accruals through today and requests through today.</span></span> <span data-ttu-id="fa6ba-143">Medarbejdere og ledere kan se disse opdaterede saldi i medarbejdernes og ledernes selvbetjeningsportal på kortet **Fridage** og i vinduet **Saldi for fritid**.</span><span class="sxs-lookup"><span data-stu-id="fa6ba-143">Employees and managers will see these updated balances in employee and manager self-service on the **Time off** card and in the **Time off balances** window.</span></span> <span data-ttu-id="fa6ba-144">Personalechefer kan se disse opdaterede saldi i arbejdsområdet **Personer** og i medarbejderens vindue **Tildelte orlovsplaner**.</span><span class="sxs-lookup"><span data-stu-id="fa6ba-144">HR managers will see these updated balances in the **People** workspace and in the employee’s **Assigned leave plans** window.</span></span>

## <a name="known-issue"></a><span data-ttu-id="fa6ba-145">Kendt problem</span><span class="sxs-lookup"><span data-stu-id="fa6ba-145">Known issue</span></span>

### <a name="mapping-errors-in-the-integration-with-finance-and-operations"></a><span data-ttu-id="fa6ba-146">Tilknytningsfejl i integrationen med Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="fa6ba-146">Mapping errors in the integration with Finance and Operations</span></span>

<span data-ttu-id="fa6ba-147">Følgende problemer er identificeret i den aktuelle skabelon til integration af Talent med Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="fa6ba-147">The following issues have been identified in the current template for integrating Talent with Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="fa6ba-148">En ny skabelon offentliggøres snart og anvendes på alle nye integrationsprojekter, der oprettes.</span><span class="sxs-lookup"><span data-stu-id="fa6ba-148">A new template will be published soon and will be applied to all new integration projects that are created.</span></span> <span data-ttu-id="fa6ba-149">For eksisterende integrationsprojekter kan opgavetilknytningerne opdateres.</span><span class="sxs-lookup"><span data-stu-id="fa6ba-149">For existing integration projects, the task mappings can be updated.</span></span> <span data-ttu-id="fa6ba-150">Du kan finde opdaterede tilknytninger i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="fa6ba-150">Refer to the following table for updated mappings.</span></span> 

>[!NOTE]
> <span data-ttu-id="fa6ba-151">Den overordnede tildelingsopgave Jobstillinger til stillinger kan ikke integrere data.</span><span class="sxs-lookup"><span data-stu-id="fa6ba-151">The Job Positions to Positions Parent Job Assignment task does not integrate data.</span></span> <span data-ttu-id="fa6ba-152">Dette er et problem, der er i øjeblikket undersøges.</span><span class="sxs-lookup"><span data-stu-id="fa6ba-152">This is an issue that is currently being researched.</span></span> <span data-ttu-id="fa6ba-153">Der findes ingen løsning i den aktuelle tilknytning.</span><span class="sxs-lookup"><span data-stu-id="fa6ba-153">There is no workaround in the current mapping.</span></span> 

<span data-ttu-id="fa6ba-154">I opgaven Afdelinger til driftsenhed skal følgende tilknytninger opdateres.</span><span class="sxs-lookup"><span data-stu-id="fa6ba-154">The Departments to Operating unit task needs the following mappings updated.</span></span>

| <span data-ttu-id="fa6ba-155">Eksisterende kildefelt</span><span class="sxs-lookup"><span data-stu-id="fa6ba-155">Existing source field</span></span>          | <span data-ttu-id="fa6ba-156">Nyt kildefelt</span><span class="sxs-lookup"><span data-stu-id="fa6ba-156">New source field</span></span> |
| -------------------------------|------------------|
| <span data-ttu-id="fa6ba-157">cdm_description (beskrivelse)</span><span class="sxs-lookup"><span data-stu-id="fa6ba-157">cdm_description (Description)</span></span>  | <span data-ttu-id="fa6ba-158">cdm_name (navn)</span><span class="sxs-lookup"><span data-stu-id="fa6ba-158">cdm_name (Name)</span></span>  |

<span data-ttu-id="fa6ba-159">En yderligere tilknytning skal også tilføjes.</span><span class="sxs-lookup"><span data-stu-id="fa6ba-159">An additional mapping also needs to be added.</span></span> <span data-ttu-id="fa6ba-160">Vælg det sidste **Ingen**-felt for at tilføje følgende tilknytning.</span><span class="sxs-lookup"><span data-stu-id="fa6ba-160">Select the last **None** field to add the following mapping.</span></span>

| <span data-ttu-id="fa6ba-161">Kildefelt</span><span class="sxs-lookup"><span data-stu-id="fa6ba-161">Source field</span></span>                   | <span data-ttu-id="fa6ba-162">Destinationsfelt</span><span class="sxs-lookup"><span data-stu-id="fa6ba-162">Destination field</span></span>    |
| -------------------------------|----------------------|
| <span data-ttu-id="fa6ba-163">cdm_description (beskrivelse)</span><span class="sxs-lookup"><span data-stu-id="fa6ba-163">cdm_description (Description)</span></span>  | <span data-ttu-id="fa6ba-164">NAMEALIAS (NAMEALIAS)</span><span class="sxs-lookup"><span data-stu-id="fa6ba-164">NAMEALIAS (NAMEALIAS)</span></span>|

<span data-ttu-id="fa6ba-165">De opdaterede tilknytninger skal se ud som på følgende billede.</span><span class="sxs-lookup"><span data-stu-id="fa6ba-165">The updated mappings should look like the following image.</span></span>

![Opgaven Afdelinger til driftsenheder](./media/DepartmentMapping.png)


<span data-ttu-id="fa6ba-167">I opgaven Job til stillingsdetaljer skal følgende tilknytninger opdateres.</span><span class="sxs-lookup"><span data-stu-id="fa6ba-167">The Jobs to Job Detail task needs the following mappings updated.</span></span>

| <span data-ttu-id="fa6ba-168">Eksisterende kildefelt</span><span class="sxs-lookup"><span data-stu-id="fa6ba-168">Existing source field</span></span>          | <span data-ttu-id="fa6ba-169">Nyt kildefelt</span><span class="sxs-lookup"><span data-stu-id="fa6ba-169">New source field</span></span>                   |
| -------------------------------|------------------------------------|
| <span data-ttu-id="fa6ba-170">cdm_name (navn)</span><span class="sxs-lookup"><span data-stu-id="fa6ba-170">cdm_name (Name)</span></span>                | <span data-ttu-id="fa6ba-171">cdm_description (beskrivelse)</span><span class="sxs-lookup"><span data-stu-id="fa6ba-171">cdm_description (Description)</span></span>      |
| <span data-ttu-id="fa6ba-172">cdm_name (beskrivelse)</span><span class="sxs-lookup"><span data-stu-id="fa6ba-172">cdm_name (Description)</span></span>         | <span data-ttu-id="fa6ba-173">cdm_jobdescription (stillingsbeskrivelse)</span><span class="sxs-lookup"><span data-stu-id="fa6ba-173">cdm_jobdescription(Job Description)</span></span>|


<span data-ttu-id="fa6ba-174">De opdaterede tilknytninger skal se ud som på billedet nedenfor.</span><span class="sxs-lookup"><span data-stu-id="fa6ba-174">The updated mappings should look like the image below.</span></span>

![Opgaven Job til stillingsdetaljer](./media/JobMapping.png)

<span data-ttu-id="fa6ba-176">I opgaven Arbejdere til arbejde skal følgende tilknytninger opdateres.</span><span class="sxs-lookup"><span data-stu-id="fa6ba-176">The Workers to Work task needs the following mappings updated.</span></span>

| <span data-ttu-id="fa6ba-177">Eksisterende kildefelt</span><span class="sxs-lookup"><span data-stu-id="fa6ba-177">Existing source field</span></span>                 | <span data-ttu-id="fa6ba-178">Nyt kildefelt</span><span class="sxs-lookup"><span data-stu-id="fa6ba-178">New source field</span></span>                               |
| --------------------------------------|------------------------------------------------|
| <span data-ttu-id="fa6ba-179">cdm_emailaddress1 (e-mailadresse 1)</span><span class="sxs-lookup"><span data-stu-id="fa6ba-179">cdm_emailaddress1 (Email Address 1)</span></span>   | <span data-ttu-id="fa6ba-180">cdm_primaryemailaddress (primær e-mailadresse)</span><span class="sxs-lookup"><span data-stu-id="fa6ba-180">cdm_primaryemailaddress (Primary Email Address</span></span> |
| <span data-ttu-id="fa6ba-181">cdm_telephone1 (telefon 1)</span><span class="sxs-lookup"><span data-stu-id="fa6ba-181">cdm_telephone1 (Telephone 1)</span></span>          | <span data-ttu-id="fa6ba-182">cdm_primarytelephone (primær telefon)</span><span class="sxs-lookup"><span data-stu-id="fa6ba-182">cdm_primarytelephone (Primary Telephone)</span></span>       |

<span data-ttu-id="fa6ba-183">Transformeringen af feltet Køn skal også opdateres.</span><span class="sxs-lookup"><span data-stu-id="fa6ba-183">The Gender field transform also needs to be updated.</span></span> <span data-ttu-id="fa6ba-184">Vælg tilknytningstypen **fn** (funktion) for Køn, og opdater følgende værditilknytninger.</span><span class="sxs-lookup"><span data-stu-id="fa6ba-184">Select the **fn** (function) map type for Gender and update the following value mappings.</span></span>

| <span data-ttu-id="fa6ba-185">Common Data Service-værdi</span><span class="sxs-lookup"><span data-stu-id="fa6ba-185">Common Data Service value</span></span>                   | <span data-ttu-id="fa6ba-186">Finance and Operations-værdi</span><span class="sxs-lookup"><span data-stu-id="fa6ba-186">Finance and Operations value</span></span>                     |
| ----------------------------|--------------------------------------------------|
| <span data-ttu-id="fa6ba-187">75440000</span><span class="sxs-lookup"><span data-stu-id="fa6ba-187">75440000</span></span>                    | <span data-ttu-id="fa6ba-188">Mand</span><span class="sxs-lookup"><span data-stu-id="fa6ba-188">Male</span></span>                                             |
| <span data-ttu-id="fa6ba-189">75440001</span><span class="sxs-lookup"><span data-stu-id="fa6ba-189">75440001</span></span>                    | <span data-ttu-id="fa6ba-190">Kvinde</span><span class="sxs-lookup"><span data-stu-id="fa6ba-190">Female</span></span>                                           |
| <span data-ttu-id="fa6ba-191">75440002</span><span class="sxs-lookup"><span data-stu-id="fa6ba-191">75440002</span></span>                    | <span data-ttu-id="fa6ba-192">Ingen</span><span class="sxs-lookup"><span data-stu-id="fa6ba-192">None</span></span>                                             | 
| <span data-ttu-id="fa6ba-193">75440003</span><span class="sxs-lookup"><span data-stu-id="fa6ba-193">75440003</span></span>                    | <span data-ttu-id="fa6ba-194">Ikke-specifik</span><span class="sxs-lookup"><span data-stu-id="fa6ba-194">NonSpecific</span></span>                                      |

<span data-ttu-id="fa6ba-195">De opdaterede tilknytninger skal se ud som på følgende billeder.</span><span class="sxs-lookup"><span data-stu-id="fa6ba-195">The updated mappings should look like the following images.</span></span>

![Opgaven Arbejdere til arbejde](./media/WorkerMapping.png)

![Transformering af feltet Køn](./media/WorkerTransform.png)
