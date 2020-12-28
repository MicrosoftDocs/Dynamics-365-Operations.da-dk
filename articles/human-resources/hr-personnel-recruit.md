---
title: Rekruttere jobkandidater
description: Dette emne viser, hvordan du rekrutterer til kandidater i Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 12/03/2020
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
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9a35abcb8a2f6aa8031c8d84a44c2a8ad93883ac
ms.sourcegitcommit: 0354ca7e566fbd2eb0aabdd40000d4ac5c44ea78
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/04/2020
ms.locfileid: "4669159"
---
# <a name="recruit-job-candidates"></a><span data-ttu-id="e834d-103">Rekruttere jobkandidater</span><span class="sxs-lookup"><span data-stu-id="e834d-103">Recruit job candidates</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="e834d-104">Dynamics 365 Human Resources hjælper dig med at administrere rekrutteringsanmodninger.</span><span class="sxs-lookup"><span data-stu-id="e834d-104">Dynamics 365 Human Resources helps you to manage recruiting requests.</span></span> <span data-ttu-id="e834d-105">Det hjælper dig også med en problemfri overgang fra kandidat til medarbejder.</span><span class="sxs-lookup"><span data-stu-id="e834d-105">It also helps you seamlessly transition job candidates to employees.</span></span> <span data-ttu-id="e834d-106">Hvis organisationen bruger et separat rekrutteringsprogram, kan rekrutteringsprocessen omfatte følgende trin:</span><span class="sxs-lookup"><span data-stu-id="e834d-106">If your organization uses a separate recruiting application, your recruiting process might include the following steps:</span></span>

- <span data-ttu-id="e834d-107">Angiv din rekrutteringsanmodning i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e834d-107">Enter your recruiting request in Human Resources.</span></span>
- <span data-ttu-id="e834d-108">Modtag henvisninger til kandidater i Human Resources fra rekrutteringsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="e834d-108">Receive candidate referrals in Human Resources from the recruiting application.</span></span>
- <span data-ttu-id="e834d-109">Gennemfør godkendelsesprocessen for kandidaten i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e834d-109">Complete the candidate approval process in Human Resources.</span></span>

<span data-ttu-id="e834d-110">Hvis du ikke bruger et separat rekrutteringsprogram, kan du også manuelt administrere kandidater i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e834d-110">If you aren't using a separate recruiting application, you can also manually manage candidates in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="e834d-111">Hvis du er administrator eller udvikler og vil integrere Human Resources med et rekrutteringsprogram fra tredjepart, skal du se [Konfigurer Common Data Service-integration](hr-admin-integration-common-data-service.md) og [Konfigurer Common Data Service virtuelle enheder](hr-admin-integration-common-data-service-virtual-entities.md)</span><span class="sxs-lookup"><span data-stu-id="e834d-111">If you're an admin or developer and want to integrate Human Resources with a third-party recruiting application, see [Configure Common Data Service integration](hr-admin-integration-common-data-service.md) and [Configure Common Data Service virtual entities](hr-admin-integration-common-data-service-virtual-entities.md)</span></span>
>
> <span data-ttu-id="e834d-112">Du kan også finde apps til rekrutteringsintegration på [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).</span><span class="sxs-lookup"><span data-stu-id="e834d-112">You can also find recruiting integration apps on [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).</span></span>
>
> <span data-ttu-id="e834d-113">Hvis du vil afprøve vores prøveversionsfunktion til integration med LinkedIn Talent Hub, skal du se [Integrere med LinkedIn Talent Hub](hr-admin-integration-linkedin.md).</span><span class="sxs-lookup"><span data-stu-id="e834d-113">To try out our preview feature for integrating with LinkedIn Talent Hub, see [Integrate with LinkedIn Talent Hub](hr-admin-integration-linkedin.md).</span></span>

## <a name="enable-recruiting-requests"></a><span data-ttu-id="e834d-114">Aktiver rekrutteringsanmodninger</span><span class="sxs-lookup"><span data-stu-id="e834d-114">Enable recruiting requests</span></span>

<span data-ttu-id="e834d-115">Hvis du vil sende rekrutteringsanmodninger i Human Resources, skal du først aktivere funktionaliteten i **Personaleparametre**.</span><span class="sxs-lookup"><span data-stu-id="e834d-115">If you want to submit recruiting requests in Human Resources, you must first enable the functionality in **Human resources parameters**.</span></span>

1. <span data-ttu-id="e834d-116">Vælg **Links** i arbejdsområdet **Personalestyring**.</span><span class="sxs-lookup"><span data-stu-id="e834d-116">In the **Personnel management** workspace, select **Links**.</span></span>

2. <span data-ttu-id="e834d-117">Vælg **Personaleparametre** under **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="e834d-117">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="e834d-118">Under **Rekruttering** under fanen **Generelt** skal du indstille **Aktiver rekrutteringsanmodninger** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="e834d-118">On the **General** tab, under **RECRUITING**, set **Enable recruiting requests** to **Yes**.</span></span>

   ![Aktiver rekrutteringsanmodninger](./media/hr-recruit-0-enable-requests.png)

## <a name="add-a-recruiting-request-location"></a><span data-ttu-id="e834d-120">Tilføje en lokation for en rekrutteringsanmodning</span><span class="sxs-lookup"><span data-stu-id="e834d-120">Add a recruiting request location</span></span>

<span data-ttu-id="e834d-121">Hvis organisationen har flere lokationer, kan du tilføje dem, så anmodere kan vælge den lokation, hvor den nye rekrutterede skal arbejde.</span><span class="sxs-lookup"><span data-stu-id="e834d-121">If your organization has multiple locations, you can add them so requestors can select a location where the new recruit will be working.</span></span> <span data-ttu-id="e834d-122">Lokationen medtages i jobopslaget.</span><span class="sxs-lookup"><span data-stu-id="e834d-122">The location will be included in the job posting.</span></span>

1. <span data-ttu-id="e834d-123">Angiv en **lokation for en rekrutteringsanmodning** i søgepanelet.</span><span class="sxs-lookup"><span data-stu-id="e834d-123">In the search bar, enter **recruiting request location**.</span></span>

2. <span data-ttu-id="e834d-124">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="e834d-124">Select **New**.</span></span>

3. <span data-ttu-id="e834d-125">Angiv navnet på lokationen i feltet **Lokation for rekrutteringsanmodning**.</span><span class="sxs-lookup"><span data-stu-id="e834d-125">In the **Recruiting request location** field, enter the location name.</span></span>

   ![Tilføje en lokation for en rekrutteringsanmodning](./media/hr-recruit-0a-add-location.png)

4. <span data-ttu-id="e834d-127">Indtast en beskrivelse af lokationen i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="e834d-127">In the **Description**, enter a description for the location.</span></span>

5. <span data-ttu-id="e834d-128">Vælg **Tilføj** under **Lokation**.</span><span class="sxs-lookup"><span data-stu-id="e834d-128">Under **Location**, select **Add**.</span></span> <span data-ttu-id="e834d-129">Hvis vinduet **Ny adresse** vises, skal du angive adressen på lokationen.</span><span class="sxs-lookup"><span data-stu-id="e834d-129">If the **New address** popout appears, enter the address for the location.</span></span>

   ![Indtast adresse](./media/hr-recruit-0b-address.png)

6. <span data-ttu-id="e834d-131">Angiv oplysningerne om kontaktpersonen på lokationen under **Kontaktoplysninger**.</span><span class="sxs-lookup"><span data-stu-id="e834d-131">Under **Contact information**, enter the information for the location's contact.</span></span>

7. <span data-ttu-id="e834d-132">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="e834d-132">Select **Save**.</span></span>

## <a name="add-a-recruiting-request"></a><span data-ttu-id="e834d-133">Tilføje en rekrutteringsanmodning</span><span class="sxs-lookup"><span data-stu-id="e834d-133">Add a recruiting request</span></span>

<span data-ttu-id="e834d-134">Ledere kan sende rekrutteringsanmodninger i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e834d-134">Managers can submit recruiting requests in Human Resources.</span></span> <span data-ttu-id="e834d-135">Hvis du bruger et separat rekrutteringsprogram, vil disse trin sende en rekrutteringsanmodning og starte rekrutteringsprocessen i programmet.</span><span class="sxs-lookup"><span data-stu-id="e834d-135">If you use a separate recruiting application, completing these steps will send a recruiting request and start the recruiting process in that application.</span></span> <span data-ttu-id="e834d-136">Ellers skal du udføre denne procedure for at starte arbejdsprocessen for din egen interne rekrutteringsproces.</span><span class="sxs-lookup"><span data-stu-id="e834d-136">Otherwise, complete this procedure to begin the workflow for your own internal recruiting process.</span></span>

1. <span data-ttu-id="e834d-137">Vælg **Medarbejderselvbetjening**.</span><span class="sxs-lookup"><span data-stu-id="e834d-137">Select **Employee self service**.</span></span>

2. <span data-ttu-id="e834d-138">Vælg fanen **Mit team**.</span><span class="sxs-lookup"><span data-stu-id="e834d-138">Select the **My team** tab.</span></span>

3. <span data-ttu-id="e834d-139">Vælg **Anmodning om rekruttering**.</span><span class="sxs-lookup"><span data-stu-id="e834d-139">Select  **Request to recruit**.</span></span>

   ![Start en rekrutteringsanmodning](./media/hr-recruit-1-request-to-recruit.png)

4. <span data-ttu-id="e834d-141">Udfyld felterne **Beskrivelse**, **Job** og **Anslået startdato**.</span><span class="sxs-lookup"><span data-stu-id="e834d-141">Complete the **Description**, **Job**, and **Estimated start date** fields.</span></span>

   ![Fuldfør rekrutteringsanmodningen](./media/hr-recruit-2-request-to-recruit.png)

5. <span data-ttu-id="e834d-143">Vælg **Fortsæt**.</span><span class="sxs-lookup"><span data-stu-id="e834d-143">Select **Continue**.</span></span> <span data-ttu-id="e834d-144">Rekrutteringsanmodningen for stillingen vises.</span><span class="sxs-lookup"><span data-stu-id="e834d-144">The recruiting request for your position appears.</span></span>

6. <span data-ttu-id="e834d-145">Vælg en rekrutteringsmedarbejder på rullelisten **Rekrutteringsmedarbejder** under **Generelt**, og vælg derefter en lokation på rullelisten **Lokation for rekrutteringsanmodning**.</span><span class="sxs-lookup"><span data-stu-id="e834d-145">Under **General**, select a recruiter from the **Recruiter** dropdown, and then select a location from the **Recruiting request location** dropdown.</span></span>

7. <span data-ttu-id="e834d-146">Rediger oplysninger efter behov under **Job**, og vælg derefter **Opret detaljer fra job**.</span><span class="sxs-lookup"><span data-stu-id="e834d-146">Under **Job**, change any information as needed, and then select **Create details from job**.</span></span>

   ![Opret detaljer fra job](./media/hr-recruit-3-create-details-from-job.png)

   <span data-ttu-id="e834d-148">Resten af rekrutteringsanmodningen vil blive udfyldt med standardoplysninger for det job, du har angivet.</span><span class="sxs-lookup"><span data-stu-id="e834d-148">The rest of the recruiting request will populate with the default information for the job you entered.</span></span>

8. <span data-ttu-id="e834d-149">Angiv en beskrivelse af en ekstern stilling under **Ekstern beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="e834d-149">Under **External description**, enter an external-facing job description.</span></span>

9. <span data-ttu-id="e834d-150">Under **Stillinger** skal du vælge **Tilføj** og derefter vælge en stilling for denne rekrutteringsanmodning.</span><span class="sxs-lookup"><span data-stu-id="e834d-150">Under **Positions**, select **Add**, and then select a position for this recruiting request.</span></span>

   ![Tilføj en stilling](./media/hr-recruit-4-select-position.png)

10. <span data-ttu-id="e834d-152">Vælg **Tilføj** under **Færdigheder**, og vælg derefter en færdighed.</span><span class="sxs-lookup"><span data-stu-id="e834d-152">Under **Skills**, select **Add**, and then select a skill.</span></span>

11. <span data-ttu-id="e834d-153">Vælg **Tilføj** under **Uddannelseskrav**, og vælg derefter værdier på rullelisten **Uddannelse** og **Uddannelsesniveau**.</span><span class="sxs-lookup"><span data-stu-id="e834d-153">Under **Educational requirements**, select **Add**, and then select values from the **Education** and **Level of education** dropdowns.</span></span>

   ![Tilføj krav til uddannelse](./media/hr-recruit-5-select-educational-requirements.png)

12. <span data-ttu-id="e834d-155">Tilføj evt. kommentarer under **Kommentar**.</span><span class="sxs-lookup"><span data-stu-id="e834d-155">Under **Comment**, add comments as necessary.</span></span>

13. <span data-ttu-id="e834d-156">Vælg et niveau på rullelisten **Niveau** under **Kompensation**, og juster derefter **Laveste tærskel**, **Referencepunkt** og **Højeste tærskel** efter behov.</span><span class="sxs-lookup"><span data-stu-id="e834d-156">Under **Compensation**, select a level from the **Level** dropdown, and then adjust **Low threshold**, **Control point**, and **High threshold** as necessary.</span></span>

14. <span data-ttu-id="e834d-157">Når din rekrutteringsanmodning er fuldført, og du er klar til at starte rekrutteringsprocessen, skal du vælge **Aktivér** på menulinjen.</span><span class="sxs-lookup"><span data-stu-id="e834d-157">When your recruiting request is complete and you're ready to start the recruiting process, select **Activate** in the menu bar.</span></span>

   ![Aktiver rekrutteringsanmodning](./media/hr-recruit-6-activate-recruit-request.png)

15. <span data-ttu-id="e834d-159">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="e834d-159">Select **Save**.</span></span>

## <a name="view-and-edit-your-recruiting-requests"></a><span data-ttu-id="e834d-160">Se og rediger dine rekrutteringsanmodninger</span><span class="sxs-lookup"><span data-stu-id="e834d-160">View and edit your recruiting requests</span></span>

<span data-ttu-id="e834d-161">Hvis du er leder og ønsker at se dine egne anmodninger:</span><span class="sxs-lookup"><span data-stu-id="e834d-161">If you're a manager and want to view your own requests:</span></span>

1. <span data-ttu-id="e834d-162">Vælg **Medarbejderselvbetjening**.</span><span class="sxs-lookup"><span data-stu-id="e834d-162">Select **Employee self service**.</span></span>

2. <span data-ttu-id="e834d-163">Vælg fanen **Mit team**.</span><span class="sxs-lookup"><span data-stu-id="e834d-163">Select the **My team** tab.</span></span>

3. <span data-ttu-id="e834d-164">Under **Mine teamoplysninger** skal du vælge fanen **Rekrutteringsanmodninger**.</span><span class="sxs-lookup"><span data-stu-id="e834d-164">Under **My team information**, select the **Recruiting requests** tab.</span></span>

   ![Vælg fanen rekrutteringsanmodninger](./media/hr-recruit-7-recruiting-requests.png)

4. <span data-ttu-id="e834d-166">Hvis du vil have vist eller redigere en rekrutteringsanmodning, skal du vælge den i gitteret.</span><span class="sxs-lookup"><span data-stu-id="e834d-166">To view or edit a recruiting request, select it in the grid.</span></span>

<span data-ttu-id="e834d-167">Hvis du er personalemedarbejder og vil have vist alle rekrutteringsanmodninger:</span><span class="sxs-lookup"><span data-stu-id="e834d-167">If you're an HR pro and want to view all recruiting requests:</span></span>

1. <span data-ttu-id="e834d-168">Vælg **Personalestyring**.</span><span class="sxs-lookup"><span data-stu-id="e834d-168">Select **Personnel management**.</span></span>

2. <span data-ttu-id="e834d-169">Vælg **Rekrutteringsanmodninger**.</span><span class="sxs-lookup"><span data-stu-id="e834d-169">Select **Recruiting requests**.</span></span>

   ![Få vist rekrutteringsanmodninger i Personalestyring](./media/hr-recruit-8-recruiting-requests-personnel-management.png)

3. <span data-ttu-id="e834d-171">Hvis du vil have vist eller redigere en rekrutteringsanmodning, skal du vælge den i gitteret.</span><span class="sxs-lookup"><span data-stu-id="e834d-171">To view or edit a recruiting request, select it in the grid.</span></span>

## <a name="add-or-edit-a-candidate-profile"></a><span data-ttu-id="e834d-172">Tilføje eller redigere en kandidatprofil</span><span class="sxs-lookup"><span data-stu-id="e834d-172">Add or edit a candidate profile</span></span>

<span data-ttu-id="e834d-173">Hvis organisationen er integreret med et andet program for at administrere rekrutteringsanmodninger, videresendes rekrutteringsanmodninger til dette program.</span><span class="sxs-lookup"><span data-stu-id="e834d-173">If your organization has integrated with another application to manage recruiting requests, recruiting requests are forwarded to that application.</span></span> <span data-ttu-id="e834d-174">Rekrutteringsprogrammet sender derefter kandidatoplysninger tilbage til Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e834d-174">The recruiting application then sends candidate information back to Human Resources.</span></span> <span data-ttu-id="e834d-175">Ellers kan du følge dine egne interne rekrutteringsprocesser og angive kandidatoplysninger manuelt.</span><span class="sxs-lookup"><span data-stu-id="e834d-175">Otherwise, you can follow your own internal recruiting processes and enter candidate information manually.</span></span>

1. <span data-ttu-id="e834d-176">Vælg **Personalestyring**.</span><span class="sxs-lookup"><span data-stu-id="e834d-176">Select **Personnel management**.</span></span>

2. <span data-ttu-id="e834d-177">Vælg **Links**.</span><span class="sxs-lookup"><span data-stu-id="e834d-177">Select **Links**.</span></span>

3. <span data-ttu-id="e834d-178">Vælg **Kandidater** under **Rekruttering**.</span><span class="sxs-lookup"><span data-stu-id="e834d-178">Under **Recruiting**, select **Candidates**.</span></span>

   ![Få vist kandidater](./media/hr-recruit-9-candidates.png)

4. <span data-ttu-id="e834d-180">Vælg **Ny** for at tilføje en kandidat.</span><span class="sxs-lookup"><span data-stu-id="e834d-180">To add a candidate, select **New**.</span></span> <span data-ttu-id="e834d-181">Hvis du vil redigere en eksisterende kandidat, skal du vælge kandidat på listen og derefter vælge **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="e834d-181">To edit an existing candidate, select the candidate from the list and then select **Edit**.</span></span> <span data-ttu-id="e834d-182">Kandidatprofilen vises.</span><span class="sxs-lookup"><span data-stu-id="e834d-182">The candidate profile appears.</span></span>

5. <span data-ttu-id="e834d-183">Angiv eller rediger kandidatoplysningerne efter behov under **Kandidatoversigt**.</span><span class="sxs-lookup"><span data-stu-id="e834d-183">Under **Candidate summary**, enter or edit the candidate information as necessary.</span></span>

6. <span data-ttu-id="e834d-184">Under **Rekrutteringsanmodning** skal du vælge en rekrutteringsanmodning, som kandidaten skal knyttes til.</span><span class="sxs-lookup"><span data-stu-id="e834d-184">Under **Recruiting request**, select a recruiting request to link the candidate to.</span></span> <span data-ttu-id="e834d-185">Udfyld derefter felterne **Anslået startdato**, **Ansættelseschef**, **Stilling** og **Beskrivelse** efter behov.</span><span class="sxs-lookup"><span data-stu-id="e834d-185">Then complete the **Estimated start date**, **Hiring manager**, **Position**, and **Description fields** as appropriate.</span></span>

   ![Tilknyt til rekrutteringsanmodning](./media/hr-recruit-10-link-to-recruiting-request.png)

7. <span data-ttu-id="e834d-187">Udfyld alle oplysningerne i følgende områder, som du vil medtage i kandidatens post:</span><span class="sxs-lookup"><span data-stu-id="e834d-187">Complete all the information in the following areas that you want to include in the candidate's record:</span></span>
   - <span data-ttu-id="e834d-188">**Bemærkninger**</span><span class="sxs-lookup"><span data-stu-id="e834d-188">**Comments**</span></span>
   - <span data-ttu-id="e834d-189">**Erhvervserfaring**</span><span class="sxs-lookup"><span data-stu-id="e834d-189">**Professional experience**</span></span>
   - <span data-ttu-id="e834d-190">**Kontaktpersonoplysninger**</span><span class="sxs-lookup"><span data-stu-id="e834d-190">**Contact information**</span></span>
   - <span data-ttu-id="e834d-191">**Uddannelser**</span><span class="sxs-lookup"><span data-stu-id="e834d-191">**Education**</span></span>
   - <span data-ttu-id="e834d-192">**Færdigheder**</span><span class="sxs-lookup"><span data-stu-id="e834d-192">**Skills**</span></span>
   - <span data-ttu-id="e834d-193">**Certifikater**</span><span class="sxs-lookup"><span data-stu-id="e834d-193">**Certificates**</span></span>
   - <span data-ttu-id="e834d-194">**Screeninger**</span><span class="sxs-lookup"><span data-stu-id="e834d-194">**Screenings**</span></span>

8. <span data-ttu-id="e834d-195">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="e834d-195">Select **Save**.</span></span>

## <a name="hire-a-candidate"></a><span data-ttu-id="e834d-196">Ansætte en kandidat</span><span class="sxs-lookup"><span data-stu-id="e834d-196">Hire a candidate</span></span>

<span data-ttu-id="e834d-197">Når du er klar til at ansætte en kandidat, skal du følge denne procedure for at lade kandidaten overgå til medarbejder.</span><span class="sxs-lookup"><span data-stu-id="e834d-197">When you're ready to hire a candidate, follow this procedure to transition the candidate to an employee.</span></span>

1. <span data-ttu-id="e834d-198">Vælg **Ansæt** i kandidatformularen.</span><span class="sxs-lookup"><span data-stu-id="e834d-198">On the candidate form, select **Hire**.</span></span>

   ![Ansætte en kandidat](./media/hr-recruit-11-hire.png)

2. <span data-ttu-id="e834d-200">Udfyld alle felter i formularen **Ansæt ny arbejder** under **Detaljer**.</span><span class="sxs-lookup"><span data-stu-id="e834d-200">On the **Hire new worker** form, under **Details**, complete all the fields.</span></span>

   ![Angive oplysninger om ny ansættelse](./media/hr-recruit-12-hire-new-worker.png)

3. <span data-ttu-id="e834d-202">Bekræft og rediger oplysninger efter behov under **Detaljer for stilling**.</span><span class="sxs-lookup"><span data-stu-id="e834d-202">Under **Position details**, verify and change information as necessary.</span></span>

4. <span data-ttu-id="e834d-203">Vælg de relevante onboarding-tjeklister for denne medarbejder under **Kontrollister for onboarding**.</span><span class="sxs-lookup"><span data-stu-id="e834d-203">Under **Onboarding checklists**, select the relevant onboarding checklists for this employee.</span></span>

5. <span data-ttu-id="e834d-204">Vælg **Fortsæt** for at oprette medarbejderposten.</span><span class="sxs-lookup"><span data-stu-id="e834d-204">Select **Continue** to create the employee record.</span></span>

   >[!NOTE]
   ><span data-ttu-id="e834d-205">Afhængigt af organisationens arbejdsgange kan kandidatposten gennemgå yderligere godkendelsestrin, før den bliver en medarbejderpost.</span><span class="sxs-lookup"><span data-stu-id="e834d-205">Depending on your organization's workflows, the candidate record may go through additional approval steps before becoming an employee record.</span></span>

## <a name="decide-not-to-hire-a-candidate"></a><span data-ttu-id="e834d-206">Beslutte ikke at ansætte en kandidat</span><span class="sxs-lookup"><span data-stu-id="e834d-206">Decide not to hire a candidate</span></span>

<span data-ttu-id="e834d-207">Hvis du beslutter dig for ikke at ansætte en kandidat, skal du følge denne procedure for at fjerne vedkommende fra vurderingsprocessen.</span><span class="sxs-lookup"><span data-stu-id="e834d-207">If you decide not to hire a candidate, follow this procedure to remove them from the vetting process.</span></span> 

1. <span data-ttu-id="e834d-208">Vælg **Ansæt ikke** i kandidatformularen.</span><span class="sxs-lookup"><span data-stu-id="e834d-208">On the candidate form, select **Do not hire**.</span></span>

   ![Ansæt ikke kandidat](./media/hr-recruit-13-do-not-hire.png)

2. <span data-ttu-id="e834d-210">Vælg en **Årsagskode**, og medtag eventuelle kommentarer.</span><span class="sxs-lookup"><span data-stu-id="e834d-210">Select a **Reason code** and include any comments.</span></span>

3. <span data-ttu-id="e834d-211">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="e834d-211">Select **OK**.</span></span>

## <a name="dismiss-a-candidate"></a><span data-ttu-id="e834d-212">Afvise en kandidat</span><span class="sxs-lookup"><span data-stu-id="e834d-212">Dismiss a candidate</span></span>

<span data-ttu-id="e834d-213">Hvis det er nødvendigt, kan du afvise en kandidat efter at have ansat vedkommende.</span><span class="sxs-lookup"><span data-stu-id="e834d-213">If needed, you can dismiss a candidate after hiring them.</span></span> <span data-ttu-id="e834d-214">En kandidat kan f.eks. afvise dit tilbud eller ikke møde op den første dag.</span><span class="sxs-lookup"><span data-stu-id="e834d-214">For example, a candidate might reject your offer or not show up on their first day.</span></span>

- <span data-ttu-id="e834d-215">Vælg **Afvis kandidat** i kandidatformularen.</span><span class="sxs-lookup"><span data-stu-id="e834d-215">On the candidate form, select **Dismiss candidate**.</span></span>

  ![Afvis kandidat](./media/hr-recruit-14-dismiss-candidate.png)

## <a name="see-also"></a><span data-ttu-id="e834d-217">Se også</span><span class="sxs-lookup"><span data-stu-id="e834d-217">See also</span></span>

[<span data-ttu-id="e834d-218">Konfigurere Common Data Service virtuelle enheder</span><span class="sxs-lookup"><span data-stu-id="e834d-218">Configure Common Data Service virtual entities</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="e834d-219">Organisere dine medarbejdere</span><span class="sxs-lookup"><span data-stu-id="e834d-219">Organize your workforce</span></span>](hr-personnel-departments-jobs-positions.md)<br>
[<span data-ttu-id="e834d-220">Konfigurere komponenterne i et job</span><span class="sxs-lookup"><span data-stu-id="e834d-220">Set up the components of a job</span></span>](hr-personnel-jobs.md)