---
title: Rekruttere jobkandidater
description: Dette emne viser, hvordan du rekrutterer til kandidater i Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 12/03/2020
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
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9259cfa78d65f36da653c807a66e291b3cb01c63
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802521"
---
# <a name="recruit-job-candidates"></a><span data-ttu-id="ff5db-103">Rekruttere jobkandidater</span><span class="sxs-lookup"><span data-stu-id="ff5db-103">Recruit job candidates</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="ff5db-104">Dynamics 365 Human Resources hjælper dig med at administrere rekrutteringsanmodninger.</span><span class="sxs-lookup"><span data-stu-id="ff5db-104">Dynamics 365 Human Resources helps you to manage recruiting requests.</span></span> <span data-ttu-id="ff5db-105">Det hjælper dig også med en problemfri overgang fra kandidat til medarbejder.</span><span class="sxs-lookup"><span data-stu-id="ff5db-105">It also helps you seamlessly transition job candidates to employees.</span></span> <span data-ttu-id="ff5db-106">Hvis organisationen bruger et separat rekrutteringsprogram, kan rekrutteringsprocessen omfatte følgende trin:</span><span class="sxs-lookup"><span data-stu-id="ff5db-106">If your organization uses a separate recruiting application, your recruiting process might include the following steps:</span></span>

- <span data-ttu-id="ff5db-107">Angiv din rekrutteringsanmodning i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ff5db-107">Enter your recruiting request in Human Resources.</span></span>
- <span data-ttu-id="ff5db-108">Modtag henvisninger til kandidater i Human Resources fra rekrutteringsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="ff5db-108">Receive candidate referrals in Human Resources from the recruiting application.</span></span>
- <span data-ttu-id="ff5db-109">Gennemfør godkendelsesprocessen for kandidaten i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ff5db-109">Complete the candidate approval process in Human Resources.</span></span>

<span data-ttu-id="ff5db-110">Hvis du ikke bruger et separat rekrutteringsprogram, kan du også manuelt administrere kandidater i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ff5db-110">If you aren't using a separate recruiting application, you can also manually manage candidates in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="ff5db-111">Hvis du er administrator eller udvikler og vil integrere Human Resources med et rekrutteringsprogram fra tredjepart, skal du se [Konfigurer Dataverse-integration](hr-admin-integration-common-data-service.md) og [Konfigurer Dataverse virtuelle tabeller](hr-admin-integration-common-data-service-virtual-entities.md)</span><span class="sxs-lookup"><span data-stu-id="ff5db-111">If you're an admin or developer and want to integrate Human Resources with a third-party recruiting application, see [Configure Dataverse integration](hr-admin-integration-common-data-service.md) and [Configure Dataverse virtual tables](hr-admin-integration-common-data-service-virtual-entities.md)</span></span>
>
> <span data-ttu-id="ff5db-112">Du kan også finde apps til rekrutteringsintegration på [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).</span><span class="sxs-lookup"><span data-stu-id="ff5db-112">You can also find recruiting integration apps on [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).</span></span>
>
> <span data-ttu-id="ff5db-113">Hvis du vil afprøve vores prøveversionsfunktion til integration med LinkedIn Talent Hub, skal du se [Integrere med LinkedIn Talent Hub](hr-admin-integration-linkedin.md).</span><span class="sxs-lookup"><span data-stu-id="ff5db-113">To try out our preview feature for integrating with LinkedIn Talent Hub, see [Integrate with LinkedIn Talent Hub](hr-admin-integration-linkedin.md).</span></span>

## <a name="enable-recruiting-requests"></a><span data-ttu-id="ff5db-114">Aktiver rekrutteringsanmodninger</span><span class="sxs-lookup"><span data-stu-id="ff5db-114">Enable recruiting requests</span></span>

<span data-ttu-id="ff5db-115">Hvis du vil sende rekrutteringsanmodninger i Human Resources, skal du først aktivere funktionaliteten i **Delte Human Resources-parametre**.</span><span class="sxs-lookup"><span data-stu-id="ff5db-115">If you want to submit recruiting requests in Human Resources, you must first enable the functionality in **Human resources shared parameters**.</span></span>

1. <span data-ttu-id="ff5db-116">Vælg **Links** i arbejdsområdet **Personalestyring**.</span><span class="sxs-lookup"><span data-stu-id="ff5db-116">In the **Personnel management** workspace, select **Links**.</span></span>

2. <span data-ttu-id="ff5db-117">Vælg **Delte parametre for personale** under **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="ff5db-117">Under **Setup**, select **Human resources shared parameters**.</span></span>

3. <span data-ttu-id="ff5db-118">Under fanen **Rekruttering**, under **Rekruttering** skal du indstille **Aktiver rekrutteringsanmodninger** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="ff5db-118">On the **Recruitment** tab, under **RECRUITING**, set **Enable recruiting requests** to **Yes**.</span></span>

## <a name="add-a-recruiting-request-location"></a><span data-ttu-id="ff5db-119">Tilføje en lokation for en rekrutteringsanmodning</span><span class="sxs-lookup"><span data-stu-id="ff5db-119">Add a recruiting request location</span></span>

<span data-ttu-id="ff5db-120">Hvis organisationen har flere lokationer, kan du tilføje dem, så anmodere kan vælge den lokation, hvor den nye rekrutterede skal arbejde.</span><span class="sxs-lookup"><span data-stu-id="ff5db-120">If your organization has multiple locations, you can add them so requestors can select a location where the new recruit will be working.</span></span> <span data-ttu-id="ff5db-121">Lokationen medtages i jobopslaget.</span><span class="sxs-lookup"><span data-stu-id="ff5db-121">The location will be included in the job posting.</span></span>

1. <span data-ttu-id="ff5db-122">Angiv en **lokation for en rekrutteringsanmodning** i søgepanelet.</span><span class="sxs-lookup"><span data-stu-id="ff5db-122">In the search bar, enter **recruiting request location**.</span></span>

2. <span data-ttu-id="ff5db-123">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="ff5db-123">Select **New**.</span></span>

3. <span data-ttu-id="ff5db-124">Angiv navnet på lokationen i feltet **Lokation for rekrutteringsanmodning**.</span><span class="sxs-lookup"><span data-stu-id="ff5db-124">In the **Recruiting request location** field, enter the location name.</span></span>

   ![Tilføje en lokation for en rekrutteringsanmodning](./media/hr-recruit-0a-add-location.png)

4. <span data-ttu-id="ff5db-126">Indtast en beskrivelse af lokationen i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="ff5db-126">In the **Description**, enter a description for the location.</span></span>

5. <span data-ttu-id="ff5db-127">Vælg **Tilføj** under **Lokation**.</span><span class="sxs-lookup"><span data-stu-id="ff5db-127">Under **Location**, select **Add**.</span></span> <span data-ttu-id="ff5db-128">Hvis vinduet **Ny adresse** vises, skal du angive adressen på lokationen.</span><span class="sxs-lookup"><span data-stu-id="ff5db-128">If the **New address** popout appears, enter the address for the location.</span></span>

   ![Indtast adresse](./media/hr-recruit-0b-address.png)

6. <span data-ttu-id="ff5db-130">Angiv oplysningerne om kontaktpersonen på lokationen under **Kontaktoplysninger**.</span><span class="sxs-lookup"><span data-stu-id="ff5db-130">Under **Contact information**, enter the information for the location's contact.</span></span>

7. <span data-ttu-id="ff5db-131">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="ff5db-131">Select **Save**.</span></span>

## <a name="add-a-recruiting-request"></a><span data-ttu-id="ff5db-132">Tilføje en rekrutteringsanmodning</span><span class="sxs-lookup"><span data-stu-id="ff5db-132">Add a recruiting request</span></span>

<span data-ttu-id="ff5db-133">Ledere kan sende rekrutteringsanmodninger i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ff5db-133">Managers can submit recruiting requests in Human Resources.</span></span> <span data-ttu-id="ff5db-134">Hvis du bruger et separat rekrutteringsprogram, vil disse trin sende en rekrutteringsanmodning og starte rekrutteringsprocessen i programmet.</span><span class="sxs-lookup"><span data-stu-id="ff5db-134">If you use a separate recruiting application, completing these steps will send a recruiting request and start the recruiting process in that application.</span></span> <span data-ttu-id="ff5db-135">Ellers skal du udføre denne procedure for at starte arbejdsprocessen for din egen interne rekrutteringsproces.</span><span class="sxs-lookup"><span data-stu-id="ff5db-135">Otherwise, complete this procedure to begin the workflow for your own internal recruiting process.</span></span>

1. <span data-ttu-id="ff5db-136">Vælg **Medarbejderselvbetjening**.</span><span class="sxs-lookup"><span data-stu-id="ff5db-136">Select **Employee self service**.</span></span>

2. <span data-ttu-id="ff5db-137">Vælg fanen **Mit team**.</span><span class="sxs-lookup"><span data-stu-id="ff5db-137">Select the **My team** tab.</span></span>

3. <span data-ttu-id="ff5db-138">Vælg **Anmodning om rekruttering**.</span><span class="sxs-lookup"><span data-stu-id="ff5db-138">Select  **Request to recruit**.</span></span>

   ![Start en rekrutteringsanmodning](./media/hr-recruit-1-request-to-recruit.png)

4. <span data-ttu-id="ff5db-140">Udfyld felterne **Beskrivelse**, **Job** og **Anslået startdato**.</span><span class="sxs-lookup"><span data-stu-id="ff5db-140">Complete the **Description**, **Job**, and **Estimated start date** fields.</span></span>

   ![Fuldfør rekrutteringsanmodningen](./media/hr-recruit-2-request-to-recruit.png)

5. <span data-ttu-id="ff5db-142">Vælg **Fortsæt**.</span><span class="sxs-lookup"><span data-stu-id="ff5db-142">Select **Continue**.</span></span> <span data-ttu-id="ff5db-143">Rekrutteringsanmodningen for stillingen vises.</span><span class="sxs-lookup"><span data-stu-id="ff5db-143">The recruiting request for your position appears.</span></span>

6. <span data-ttu-id="ff5db-144">Vælg en rekrutteringsmedarbejder på rullelisten **Rekrutteringsmedarbejder** under **Generelt**, og vælg derefter en lokation på rullelisten **Lokation for rekrutteringsanmodning**.</span><span class="sxs-lookup"><span data-stu-id="ff5db-144">Under **General**, select a recruiter from the **Recruiter** dropdown, and then select a location from the **Recruiting request location** dropdown.</span></span>

7. <span data-ttu-id="ff5db-145">Rediger oplysninger efter behov under **Job**, og vælg derefter **Opret detaljer fra job**.</span><span class="sxs-lookup"><span data-stu-id="ff5db-145">Under **Job**, change any information as needed, and then select **Create details from job**.</span></span>

   ![Opret detaljer fra job](./media/hr-recruit-3-create-details-from-job.png)

   <span data-ttu-id="ff5db-147">Resten af rekrutteringsanmodningen vil blive udfyldt med standardoplysninger for det job, du har angivet.</span><span class="sxs-lookup"><span data-stu-id="ff5db-147">The rest of the recruiting request will populate with the default information for the job you entered.</span></span>

8. <span data-ttu-id="ff5db-148">Angiv en beskrivelse af en ekstern stilling under **Ekstern beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="ff5db-148">Under **External description**, enter an external-facing job description.</span></span>

9. <span data-ttu-id="ff5db-149">Under **Stillinger** skal du vælge **Tilføj** og derefter vælge en stilling for denne rekrutteringsanmodning.</span><span class="sxs-lookup"><span data-stu-id="ff5db-149">Under **Positions**, select **Add**, and then select a position for this recruiting request.</span></span>

   ![Tilføj en stilling](./media/hr-recruit-4-select-position.png)

10. <span data-ttu-id="ff5db-151">Vælg **Tilføj** under **Færdigheder**, og vælg derefter en færdighed.</span><span class="sxs-lookup"><span data-stu-id="ff5db-151">Under **Skills**, select **Add**, and then select a skill.</span></span>

11. <span data-ttu-id="ff5db-152">Vælg **Tilføj** under **Uddannelseskrav**, og vælg derefter værdier på rullelisten **Uddannelse** og **Uddannelsesniveau**.</span><span class="sxs-lookup"><span data-stu-id="ff5db-152">Under **Educational requirements**, select **Add**, and then select values from the **Education** and **Level of education** dropdowns.</span></span>

   ![Tilføj krav til uddannelse](./media/hr-recruit-5-select-educational-requirements.png)

12. <span data-ttu-id="ff5db-154">Tilføj evt. kommentarer under **Kommentar**.</span><span class="sxs-lookup"><span data-stu-id="ff5db-154">Under **Comment**, add comments as necessary.</span></span>

13. <span data-ttu-id="ff5db-155">Vælg et niveau på rullelisten **Niveau** under **Kompensation**, og juster derefter **Laveste tærskel**, **Referencepunkt** og **Højeste tærskel** efter behov.</span><span class="sxs-lookup"><span data-stu-id="ff5db-155">Under **Compensation**, select a level from the **Level** dropdown, and then adjust **Low threshold**, **Control point**, and **High threshold** as necessary.</span></span>

14. <span data-ttu-id="ff5db-156">Når din rekrutteringsanmodning er fuldført, og du er klar til at starte rekrutteringsprocessen, skal du vælge **Aktivér** på menulinjen.</span><span class="sxs-lookup"><span data-stu-id="ff5db-156">When your recruiting request is complete and you're ready to start the recruiting process, select **Activate** in the menu bar.</span></span>

   ![Aktiver rekrutteringsanmodning](./media/hr-recruit-6-activate-recruit-request.png)

15. <span data-ttu-id="ff5db-158">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="ff5db-158">Select **Save**.</span></span>

## <a name="view-and-edit-your-recruiting-requests"></a><span data-ttu-id="ff5db-159">Se og rediger dine rekrutteringsanmodninger</span><span class="sxs-lookup"><span data-stu-id="ff5db-159">View and edit your recruiting requests</span></span>

<span data-ttu-id="ff5db-160">Hvis du er leder og ønsker at se dine egne anmodninger:</span><span class="sxs-lookup"><span data-stu-id="ff5db-160">If you're a manager and want to view your own requests:</span></span>

1. <span data-ttu-id="ff5db-161">Vælg **Medarbejderselvbetjening**.</span><span class="sxs-lookup"><span data-stu-id="ff5db-161">Select **Employee self service**.</span></span>

2. <span data-ttu-id="ff5db-162">Vælg fanen **Mit team**.</span><span class="sxs-lookup"><span data-stu-id="ff5db-162">Select the **My team** tab.</span></span>

3. <span data-ttu-id="ff5db-163">Under **Mine teamoplysninger** skal du vælge fanen **Rekrutteringsanmodninger**.</span><span class="sxs-lookup"><span data-stu-id="ff5db-163">Under **My team information**, select the **Recruiting requests** tab.</span></span>

   ![Vælg fanen rekrutteringsanmodninger](./media/hr-recruit-7-recruiting-requests.png)

4. <span data-ttu-id="ff5db-165">Hvis du vil have vist eller redigere en rekrutteringsanmodning, skal du vælge den i gitteret.</span><span class="sxs-lookup"><span data-stu-id="ff5db-165">To view or edit a recruiting request, select it in the grid.</span></span>

<span data-ttu-id="ff5db-166">Hvis du er personalemedarbejder og vil have vist alle rekrutteringsanmodninger:</span><span class="sxs-lookup"><span data-stu-id="ff5db-166">If you're an HR pro and want to view all recruiting requests:</span></span>

1. <span data-ttu-id="ff5db-167">Vælg **Personalestyring**.</span><span class="sxs-lookup"><span data-stu-id="ff5db-167">Select **Personnel management**.</span></span>

2. <span data-ttu-id="ff5db-168">Vælg **Rekrutteringsanmodninger**.</span><span class="sxs-lookup"><span data-stu-id="ff5db-168">Select **Recruiting requests**.</span></span>

   ![Få vist rekrutteringsanmodninger i Personalestyring](./media/hr-recruit-8-recruiting-requests-personnel-management.png)

3. <span data-ttu-id="ff5db-170">Hvis du vil have vist eller redigere en rekrutteringsanmodning, skal du vælge den i gitteret.</span><span class="sxs-lookup"><span data-stu-id="ff5db-170">To view or edit a recruiting request, select it in the grid.</span></span>

## <a name="add-or-edit-a-candidate-profile"></a><span data-ttu-id="ff5db-171">Tilføje eller redigere en kandidatprofil</span><span class="sxs-lookup"><span data-stu-id="ff5db-171">Add or edit a candidate profile</span></span>

<span data-ttu-id="ff5db-172">Hvis organisationen er integreret med et andet program for at administrere rekrutteringsanmodninger, videresendes rekrutteringsanmodninger til dette program.</span><span class="sxs-lookup"><span data-stu-id="ff5db-172">If your organization has integrated with another application to manage recruiting requests, recruiting requests are forwarded to that application.</span></span> <span data-ttu-id="ff5db-173">Rekrutteringsprogrammet sender derefter kandidatoplysninger tilbage til Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ff5db-173">The recruiting application then sends candidate information back to Human Resources.</span></span> <span data-ttu-id="ff5db-174">Ellers kan du følge dine egne interne rekrutteringsprocesser og angive kandidatoplysninger manuelt.</span><span class="sxs-lookup"><span data-stu-id="ff5db-174">Otherwise, you can follow your own internal recruiting processes and enter candidate information manually.</span></span>

1. <span data-ttu-id="ff5db-175">Vælg **Personalestyring**.</span><span class="sxs-lookup"><span data-stu-id="ff5db-175">Select **Personnel management**.</span></span>

2. <span data-ttu-id="ff5db-176">Vælg **Links**.</span><span class="sxs-lookup"><span data-stu-id="ff5db-176">Select **Links**.</span></span>

3. <span data-ttu-id="ff5db-177">Vælg **Kandidater** under **Rekruttering**.</span><span class="sxs-lookup"><span data-stu-id="ff5db-177">Under **Recruiting**, select **Candidates**.</span></span>

   ![Få vist kandidater](./media/hr-recruit-9-candidates.png)

4. <span data-ttu-id="ff5db-179">Vælg **Ny** for at tilføje en kandidat.</span><span class="sxs-lookup"><span data-stu-id="ff5db-179">To add a candidate, select **New**.</span></span> <span data-ttu-id="ff5db-180">Hvis du vil redigere en eksisterende kandidat, skal du vælge kandidat på listen og derefter vælge **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="ff5db-180">To edit an existing candidate, select the candidate from the list and then select **Edit**.</span></span> <span data-ttu-id="ff5db-181">Kandidatprofilen vises.</span><span class="sxs-lookup"><span data-stu-id="ff5db-181">The candidate profile appears.</span></span>

5. <span data-ttu-id="ff5db-182">Angiv eller rediger kandidatoplysningerne efter behov under **Kandidatoversigt**.</span><span class="sxs-lookup"><span data-stu-id="ff5db-182">Under **Candidate summary**, enter or edit the candidate information as necessary.</span></span>

6. <span data-ttu-id="ff5db-183">Under **Rekrutteringsanmodning** skal du vælge en rekrutteringsanmodning, som kandidaten skal knyttes til.</span><span class="sxs-lookup"><span data-stu-id="ff5db-183">Under **Recruiting request**, select a recruiting request to link the candidate to.</span></span> <span data-ttu-id="ff5db-184">Udfyld derefter felterne **Anslået startdato**, **Ansættelseschef**, **Stilling** og **Beskrivelse** efter behov.</span><span class="sxs-lookup"><span data-stu-id="ff5db-184">Then complete the **Estimated start date**, **Hiring manager**, **Position**, and **Description fields** as appropriate.</span></span>

   ![Tilknyt til rekrutteringsanmodning](./media/hr-recruit-10-link-to-recruiting-request.png)

7. <span data-ttu-id="ff5db-186">Udfyld alle oplysningerne i følgende områder, som du vil medtage i kandidatens post:</span><span class="sxs-lookup"><span data-stu-id="ff5db-186">Complete all the information in the following areas that you want to include in the candidate's record:</span></span>
   - <span data-ttu-id="ff5db-187">**Bemærkninger**</span><span class="sxs-lookup"><span data-stu-id="ff5db-187">**Comments**</span></span>
   - <span data-ttu-id="ff5db-188">**Erhvervserfaring**</span><span class="sxs-lookup"><span data-stu-id="ff5db-188">**Professional experience**</span></span>
   - <span data-ttu-id="ff5db-189">**Kontaktpersonoplysninger**</span><span class="sxs-lookup"><span data-stu-id="ff5db-189">**Contact information**</span></span>
   - <span data-ttu-id="ff5db-190">**Uddannelser**</span><span class="sxs-lookup"><span data-stu-id="ff5db-190">**Education**</span></span>
   - <span data-ttu-id="ff5db-191">**Færdigheder**</span><span class="sxs-lookup"><span data-stu-id="ff5db-191">**Skills**</span></span>
   - <span data-ttu-id="ff5db-192">**Certifikater**</span><span class="sxs-lookup"><span data-stu-id="ff5db-192">**Certificates**</span></span>
   - <span data-ttu-id="ff5db-193">**Screeninger**</span><span class="sxs-lookup"><span data-stu-id="ff5db-193">**Screenings**</span></span>

8. <span data-ttu-id="ff5db-194">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="ff5db-194">Select **Save**.</span></span>

## <a name="hire-a-candidate"></a><span data-ttu-id="ff5db-195">Ansætte en kandidat</span><span class="sxs-lookup"><span data-stu-id="ff5db-195">Hire a candidate</span></span>

<span data-ttu-id="ff5db-196">Når du er klar til at ansætte en kandidat, skal du følge denne procedure for at lade kandidaten overgå til medarbejder.</span><span class="sxs-lookup"><span data-stu-id="ff5db-196">When you're ready to hire a candidate, follow this procedure to transition the candidate to an employee.</span></span>

1. <span data-ttu-id="ff5db-197">Vælg **Ansæt** i kandidatformularen.</span><span class="sxs-lookup"><span data-stu-id="ff5db-197">On the candidate form, select **Hire**.</span></span>

   ![Ansætte en kandidat](./media/hr-recruit-11-hire.png)

2. <span data-ttu-id="ff5db-199">Udfyld alle felter i formularen **Ansæt ny arbejder** under **Detaljer**.</span><span class="sxs-lookup"><span data-stu-id="ff5db-199">On the **Hire new worker** form, under **Details**, complete all the fields.</span></span>

   ![Angive oplysninger om ny ansættelse](./media/hr-recruit-12-hire-new-worker.png)

3. <span data-ttu-id="ff5db-201">Bekræft og rediger oplysninger efter behov under **Detaljer for stilling**.</span><span class="sxs-lookup"><span data-stu-id="ff5db-201">Under **Position details**, verify and change information as necessary.</span></span>

4. <span data-ttu-id="ff5db-202">Vælg de relevante onboarding-tjeklister for denne medarbejder under **Kontrollister for onboarding**.</span><span class="sxs-lookup"><span data-stu-id="ff5db-202">Under **Onboarding checklists**, select the relevant onboarding checklists for this employee.</span></span>

5. <span data-ttu-id="ff5db-203">Vælg **Fortsæt** for at oprette medarbejderposten.</span><span class="sxs-lookup"><span data-stu-id="ff5db-203">Select **Continue** to create the employee record.</span></span>

   >[!NOTE]
   ><span data-ttu-id="ff5db-204">Afhængigt af organisationens arbejdsgange kan kandidatposten gennemgå yderligere godkendelsestrin, før den bliver en medarbejderpost.</span><span class="sxs-lookup"><span data-stu-id="ff5db-204">Depending on your organization's workflows, the candidate record may go through additional approval steps before becoming an employee record.</span></span>

## <a name="decide-not-to-hire-a-candidate"></a><span data-ttu-id="ff5db-205">Beslutte ikke at ansætte en kandidat</span><span class="sxs-lookup"><span data-stu-id="ff5db-205">Decide not to hire a candidate</span></span>

<span data-ttu-id="ff5db-206">Hvis du beslutter dig for ikke at ansætte en kandidat, skal du følge denne procedure for at fjerne vedkommende fra vurderingsprocessen.</span><span class="sxs-lookup"><span data-stu-id="ff5db-206">If you decide not to hire a candidate, follow this procedure to remove them from the vetting process.</span></span> 

1. <span data-ttu-id="ff5db-207">Vælg **Ansæt ikke** i kandidatformularen.</span><span class="sxs-lookup"><span data-stu-id="ff5db-207">On the candidate form, select **Do not hire**.</span></span>

   ![Ansæt ikke kandidat](./media/hr-recruit-13-do-not-hire.png)

2. <span data-ttu-id="ff5db-209">Vælg en **Årsagskode**, og medtag eventuelle kommentarer.</span><span class="sxs-lookup"><span data-stu-id="ff5db-209">Select a **Reason code** and include any comments.</span></span>

3. <span data-ttu-id="ff5db-210">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="ff5db-210">Select **OK**.</span></span>

## <a name="dismiss-a-candidate"></a><span data-ttu-id="ff5db-211">Afvise en kandidat</span><span class="sxs-lookup"><span data-stu-id="ff5db-211">Dismiss a candidate</span></span>

<span data-ttu-id="ff5db-212">Hvis det er nødvendigt, kan du afvise en kandidat efter at have ansat vedkommende.</span><span class="sxs-lookup"><span data-stu-id="ff5db-212">If needed, you can dismiss a candidate after hiring them.</span></span> <span data-ttu-id="ff5db-213">En kandidat kan f.eks. afvise dit tilbud eller ikke møde op den første dag.</span><span class="sxs-lookup"><span data-stu-id="ff5db-213">For example, a candidate might reject your offer or not show up on their first day.</span></span>

- <span data-ttu-id="ff5db-214">Vælg **Afvis kandidat** i kandidatformularen.</span><span class="sxs-lookup"><span data-stu-id="ff5db-214">On the candidate form, select **Dismiss candidate**.</span></span>

  ![Afvis kandidat](./media/hr-recruit-14-dismiss-candidate.png)

## <a name="see-also"></a><span data-ttu-id="ff5db-216">Se også</span><span class="sxs-lookup"><span data-stu-id="ff5db-216">See also</span></span>

[<span data-ttu-id="ff5db-217">Konfigurere virtuelle Dataverse-tabeller</span><span class="sxs-lookup"><span data-stu-id="ff5db-217">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="ff5db-218">Organisere dine medarbejdere</span><span class="sxs-lookup"><span data-stu-id="ff5db-218">Organize your workforce</span></span>](hr-personnel-departments-jobs-positions.md)<br>
[<span data-ttu-id="ff5db-219">Konfigurere komponenterne i et job</span><span class="sxs-lookup"><span data-stu-id="ff5db-219">Set up the components of a job</span></span>](hr-personnel-jobs.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
