---
title: Rekruttering med LinkedIn Recruiter
description: Dette emne indeholder oplysninger om brug af maskinel indlæring til at få anbefalinger om job og jobkandidater.
author: andreabichsel
manager: AnnBe
ms.date: 12/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 4ac7a302e5bf589beb2b560b0ff5818e90c67139
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/19/2019
ms.locfileid: "859568"
---
# <a name="sourcing-with-linkedin-recruiter"></a><span data-ttu-id="882cb-103">Rekruttering med LinkedIn Recruiter</span><span class="sxs-lookup"><span data-stu-id="882cb-103">Sourcing with LinkedIn Recruiter</span></span>
[!include[banner](../includes/banner.md)]

<span data-ttu-id="882cb-104">LinkedIn er verdens største talentdatabase og ofte det primære system, som rekrutteringsmedarbejdere bruger til at finde og kommunikere med kandidater og til kandidatkilde til de stillinger, som rekrutteringsmedarbejdere ønsker at besætte.</span><span class="sxs-lookup"><span data-stu-id="882cb-104">LinkedIn is the world’s largest talent database and often the primary system that recruiters use to find, communicate with, and source candidates for the jobs that recruiters are looking to fill.</span></span> <span data-ttu-id="882cb-105">Integrationen af LinkedIn Recruiter med Dynamics 365 for Talent: Attract gør det nemmere for brugerne at ansætte nye medarbejdere og sørge for, at dataene mellem de to systemer er synkroniserede.</span><span class="sxs-lookup"><span data-stu-id="882cb-105">LinkedIn Recruiter integration with Dynamics 365 for Talent: Attract makes it easier for users to hire, and to keep the data in sync between the two systems.</span></span>

> [!NOTE]
> <span data-ttu-id="882cb-106">Du skal bruge tilføjelsesprogrammet Omfattende ansættelser og LinkedIn Recruiter-pladser for at kunne anvende LinkedIn Recruiter-integration med Attract.</span><span class="sxs-lookup"><span data-stu-id="882cb-106">You need the Comprehensive hiring add-on and LinkedIn Recruiter seats to be able to use LinkedIn Recruiter integration with Attract.</span></span>

## <a name="set-up-linkedin-recruiter-with-attract"></a><span data-ttu-id="882cb-107">Konfigurer LinkedIn Recruiter med Attract</span><span class="sxs-lookup"><span data-stu-id="882cb-107">Set up LinkedIn Recruiter with Attract</span></span> 

<span data-ttu-id="882cb-108">Før du kan bruge egenskaberne i LinkedIn Recruiter, skal du konfigurere adgangen på kontrakts- eller virksomhedsniveau i din Attract-forekomst.</span><span class="sxs-lookup"><span data-stu-id="882cb-108">Before you can use the LinkedIn Recruiter capabilities, you must configure contract-level or company-level access with your Attract instance.</span></span> <span data-ttu-id="882cb-109">For at gennemføre konfigurationsprocessen skal du arbejde sammen med den bruger, der er administrator på din LinkedIn Recruiter-kontrakt.</span><span class="sxs-lookup"><span data-stu-id="882cb-109">To complete the configuration process, you must work with the user who is an Admin on your LinkedIn Recruiter contract.</span></span> <span data-ttu-id="882cb-110">Fuldfør følgende fremgangsmåde for at konfigurere LinkedIn Recruiter med Attract.</span><span class="sxs-lookup"><span data-stu-id="882cb-110">Complete the following steps to configure LinkedIn Recruiter with Attract.</span></span>

1.  <span data-ttu-id="882cb-111">Log på Attract som administrator, og gå til **Administratorindstillinger**.</span><span class="sxs-lookup"><span data-stu-id="882cb-111">Sign in to Attract as an Admin and go to **Admin Settings**.</span></span>

2.  <span data-ttu-id="882cb-112">Klik i venstre rude på fanen **Integration af LinkedIn**.</span><span class="sxs-lookup"><span data-stu-id="882cb-112">On the left pane, click the **LinkedIn Integration** tab.</span></span>

<span data-ttu-id="882cb-113">[![Attract-administratorvisning for at starte integrationen af LinkedIn Recruiter](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)</span><span class="sxs-lookup"><span data-stu-id="882cb-113">[![Attract Admin view to start LinkedIn Recruiter integration](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)</span></span>

3.  <span data-ttu-id="882cb-114">Klik på **Opret forbindelse** for at starte opsætningen og blive hjulpet gennem LinkedIn-logonprocessen.</span><span class="sxs-lookup"><span data-stu-id="882cb-114">Click **Connect** to start the setup and be guided through the LinkedIn sign-in process.</span></span>

4.  <span data-ttu-id="882cb-115">Hvis du har poster på flere LinkedIn-kontrakter, skal du vælge den kontrakt, som du vil forbinde med Attract-systemet.</span><span class="sxs-lookup"><span data-stu-id="882cb-115">If you have seats on multiple LinkedIn contracts, select the contract that you would like to connect to the Attract system.</span></span> <span data-ttu-id="882cb-116">Hvis du har en post i kun én LinkedIn-kontrakt, er dette trin ikke nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="882cb-116">If you have a seat on only one LinkedIn contract, this step will not be needed.</span></span>

5.  <span data-ttu-id="882cb-117">LinkedIn-widgetten indlæses nu i dine administratorindstillinger med listen over integrationer vist.</span><span class="sxs-lookup"><span data-stu-id="882cb-117">The LinkedIn widget will now load in your Admin settings with the list of integrations shown.</span></span> <span data-ttu-id="882cb-118">Under **Recruiter System Connect** skal du klikke på **Request** (Anmod om).</span><span class="sxs-lookup"><span data-stu-id="882cb-118">Under **Recruiter System connect**, click **Request**.</span></span>

<span data-ttu-id="882cb-119">[![Attract-administratorvisning for at anmode om integration af LinkedIn Recruiter](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)</span><span class="sxs-lookup"><span data-stu-id="882cb-119">[![Attract Admin view to Request LinkedIn Recruiter integration](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)</span></span>

6.  <span data-ttu-id="882cb-120">Når Attract har anmodet om integration, vises meddelelsen som **Partner ready** (Partnerklar), og integrationen kan aktiveres fra **Recruiter Admin settings** (Recruiter-administratorindstillinger).</span><span class="sxs-lookup"><span data-stu-id="882cb-120">After the integration is requested from Attract, it will show as **Partner ready** and is ready to be turned on from **Recruiter Admin settings**.</span></span> <span data-ttu-id="882cb-121">Hvis du kan se **Notify partner** (Informer partner) på denne side, skal du vente et øjeblik, klikke på **Notify partner** (Informer partner) og derefter opdatere siden.</span><span class="sxs-lookup"><span data-stu-id="882cb-121">If you see **Notify partner** on this page, wait a few seconds, click **Notify partner**, and then refresh the page.</span></span> <span data-ttu-id="882cb-122">Der bør nu stå **Partner ready** (Partnerklar).</span><span class="sxs-lookup"><span data-stu-id="882cb-122">It should now show as **Partner ready**.</span></span>

<span data-ttu-id="882cb-123">[![Attract-administratorvisning til angivelse af Attract-siden af anmodninger, der er fuldført](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)</span><span class="sxs-lookup"><span data-stu-id="882cb-123">[![Attract Admin view to indicate Attract side of requests have been completed](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)</span></span>

<span data-ttu-id="882cb-124">For at fuldføre det næste trin skal du have administratorrettigheder til din LinkedIn Recruiter-kontrakt.</span><span class="sxs-lookup"><span data-stu-id="882cb-124">To complete the next step, you need to have an Admin privilege on your LinkedIn Recruiter Contract.</span></span>

7.  <span data-ttu-id="882cb-125">Log på LinkedIn ved hjælp af administratorkontoen, og gå til LinkedIn Recruiter øverst til højre.</span><span class="sxs-lookup"><span data-stu-id="882cb-125">Sign in to LinkedIn using the Admin account and go to LinkedIn Recruiter on the top right.</span></span> 

8. <span data-ttu-id="882cb-126">I menuen **More** (Flere) øverst på skærmen skal du klikke på **Admin Settings** (Administratorindstillinger) og derefter klikke på fanen **ATS**.</span><span class="sxs-lookup"><span data-stu-id="882cb-126">On the **More** menu at the top of the screen, click **Admin Settings**, and then click the **ATS** Tab.</span></span>

<span data-ttu-id="882cb-127">Attract-systemet vises med et par indstillinger, der kan aktiveres.</span><span class="sxs-lookup"><span data-stu-id="882cb-127">The Attract system will be listed with a couple of options that can be turned on.</span></span>

9. <span data-ttu-id="882cb-128">Hvis du kun vil aktivere eksport med 1 klik for **In-ATS indicator** og **In-ATS Profile Widget**, skal du vælge **Company-level access** (Adgang på firmaniveau).</span><span class="sxs-lookup"><span data-stu-id="882cb-128">If you want to enable only 1-Click export for the **In-ATS indicator** and the **In-ATS Profile Widget**, select **Company-level access**.</span></span> <span data-ttu-id="882cb-129">Hvis du vil aktivere alle adgangsfunktioner på firmaniveau plus adgang til InMail-historik, Notes-oversigt og InMail-stubprofil, skal du vælge **Contract-level access** (Adgang på kontraktniveau).</span><span class="sxs-lookup"><span data-stu-id="882cb-129">If you want to enable all of Company-level access features plus InMail history, Notes history, and the InMail stub profile access, select **Contract-level access**.</span></span>

10. <span data-ttu-id="882cb-130">Slå det ønskede adgangsniveau til fra dine **Admin-ATS**-indstillinger i LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="882cb-130">Turn on the desired access level from your LinkedIn Recruiter **Admin-ATS** settings.</span></span>

<span data-ttu-id="882cb-131">[![Slå integration af Attract til fra administratorvisning i LinkedIn Recruiter](./media/EnableRSC.png)](./media/EnableRSC.png)</span><span class="sxs-lookup"><span data-stu-id="882cb-131">[![Turn on Attract integration from LinkedIn Recruiter Admin view](./media/EnableRSC.png)](./media/EnableRSC.png)</span></span>

12. <span data-ttu-id="882cb-132">Gå tilbage til Attract-administratorindstillingerne, og vælg fanen **LinkedIn Integration**. Du kan nu se LinkedIn-widgetindlæsningen, som viser **Enabled** (Aktiveret) og det valgte adgangsniveau aktiveret.</span><span class="sxs-lookup"><span data-stu-id="882cb-132">Go back to Attract Admin Settings as an AttractAdmin and select the **LinkedIn integration** tab. You should now see the LinkedIn widget load showing **Enabled** with the selected access level turned on.</span></span>

<span data-ttu-id="882cb-133">[![LinkedIn Recruiter-integration er fuldført](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)</span><span class="sxs-lookup"><span data-stu-id="882cb-133">[![LinkedIn Recruiter integration complete](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)</span></span>

## <a name="using-linkedin-recruiter-capabilities"></a><span data-ttu-id="882cb-134">Anvendelse af egenskaberne i LinkedIn Recruiter</span><span class="sxs-lookup"><span data-stu-id="882cb-134">Using LinkedIn Recruiter capabilities</span></span>

<span data-ttu-id="882cb-135">Når egenskaberne i LinkedIn Recruiter er aktiveret af Attract-administratoren, er de tilgængelige for de ansættelsesansvarlige og rekrutteringsmedarbejderne.</span><span class="sxs-lookup"><span data-stu-id="882cb-135">After LinkedIn Recruiter capabilities has been enabled by the Attract Admin it is available for hiring managers and recruiters to access.</span></span> <span data-ttu-id="882cb-136">Du kan bruge disse funktioner ved at oprette forbindelse til din LinkedIn-konto under **Brugerindstillinger**.</span><span class="sxs-lookup"><span data-stu-id="882cb-136">To use these capabilities, connect your LinkedIn account under **User Settings**.</span></span> <span data-ttu-id="882cb-137">Flere funktioner bliver tilgængelige, når der er forbindelse til både administrator- og brugerindstillinger.</span><span class="sxs-lookup"><span data-stu-id="882cb-137">Several capabilities will be available after both the Admin and User settings have been connected.</span></span>

### <a name="in-ats-profile-widget"></a><span data-ttu-id="882cb-138">In-ATS-profilwidget</span><span class="sxs-lookup"><span data-stu-id="882cb-138">In-ATS profile widget</span></span>

<span data-ttu-id="882cb-139">Du kan få vist kandidatens LinkedIn-profil i Attract.</span><span class="sxs-lookup"><span data-stu-id="882cb-139">You can view the candidate’s LinkedIn profile in Attract.</span></span> <span data-ttu-id="882cb-140">LinkedIn-widgetten viser kandidatprofilen, når ATS-oplysningerne svarer til brugernes LinkedIn-oplysninger.</span><span class="sxs-lookup"><span data-stu-id="882cb-140">The LinkedIn widget will display the candidate profile when the ATS information matches the LinkedIn information of its users.</span></span>

<span data-ttu-id="882cb-141">Hvis du vil se en profil, skal du gå til kandidatprofilen, enten fra et job eller en talentpulje.</span><span class="sxs-lookup"><span data-stu-id="882cb-141">To view a profile, go the candidate profile either from a job or talent pool.</span></span> <span data-ttu-id="882cb-142">I kandidatprofilen skal du vælge fanen **LinkedIn**, så profilwidgetten indlæses.</span><span class="sxs-lookup"><span data-stu-id="882cb-142">In the candidate profile, select the **LinkedIn** tab and the profile widget will load.</span></span> <span data-ttu-id="882cb-143">Du kan også gemme kandidaten i dine LinkedIn Recruiter-projekter fra denne side.</span><span class="sxs-lookup"><span data-stu-id="882cb-143">You can also save the candidate to your LinkedIn Recruiter projects from this page.</span></span>
1. <span data-ttu-id="882cb-144">Hvis LinkedIn har fundet dette match ud fra e-mail og LinkedIn-medlemmets id (nøjagtigt match), vises kandidatens profil.</span><span class="sxs-lookup"><span data-stu-id="882cb-144">If LinkedIn found the match based on email and LinkedIn member ID (exact match), the candidate's profile will be shown.</span></span> <span data-ttu-id="882cb-145">Brugeren har stadig mulighed for at sammenkæde/fjerne sammenkædningen af profilen.</span><span class="sxs-lookup"><span data-stu-id="882cb-145">The user still has an option to link/unlink the profile.</span></span>

2. <span data-ttu-id="882cb-146">Hvis LinkedIn ikke kan finde kandidaten baseret på vedkommendes e-mail- eller medlems-id, vises en liste over mulige kandidater baseret på kandidatens navn, og brugeren kan vælge en af dem og sammenkæde profilen.</span><span class="sxs-lookup"><span data-stu-id="882cb-146">If LinkedIn cannot find the candidate based on their email or member ID, it will show a list of possible candidate matches based on candidate name and the user can choose one of them and link the profile.</span></span>  

3. <span data-ttu-id="882cb-147">Hvis LinkedIn ikke kan finde nogen kandidater baseret på navnet, returneres, at der ikke blev fundet et match.</span><span class="sxs-lookup"><span data-stu-id="882cb-147">If LinkedIn cannot find any candidate based on the name, it will return that no match was found.</span></span>

### <a name="1-click-export"></a><span data-ttu-id="882cb-148">Eksport med 1 klik</span><span class="sxs-lookup"><span data-stu-id="882cb-148">1-click export</span></span> 

<span data-ttu-id="882cb-149">Mens kandidatforsyningen pågår i LinkedIn, kan du eksportere kandidaten med 1 klik til de job, du har åbnet.</span><span class="sxs-lookup"><span data-stu-id="882cb-149">While sourcing candidates in LinkedIn, you can 1-click export the candidate to the jobs that you currently have open.</span></span> <span data-ttu-id="882cb-150">Udfør følgende trin for at anvende eksport med 1 klik.</span><span class="sxs-lookup"><span data-stu-id="882cb-150">Complete the following steps for a 1-click export.</span></span> <span data-ttu-id="882cb-151">Før du fuldfører disse trin, skal du kontrollere, at du er tildelt rollen som ansættelsesansvarlig eller rekrutteringsmedarbejder for jobbet, og at jobbet har stadiet **Jobkandidat**.</span><span class="sxs-lookup"><span data-stu-id="882cb-151">Before you complete these steps, verify that you are a assigned the role of Hiring manager or Recruiter for the job and that the job has a **Prospect** stage.</span></span>

1.  <span data-ttu-id="882cb-152">Opret jobbet, tildel de relevante roller, og aktivér jobbet.</span><span class="sxs-lookup"><span data-stu-id="882cb-152">Create the job, assign the appropriate roles, and activate the job.</span></span>

2.  <span data-ttu-id="882cb-153">Gå til LinkedIn Recruiter, når jobbet er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="882cb-153">When the job is activated, navigate to LinkedIn Recruiter.</span></span>

3.  <span data-ttu-id="882cb-154">Find den kandidat, du søger efter, og gå til vedkommendes profil.</span><span class="sxs-lookup"><span data-stu-id="882cb-154">Find the candidate that you are looking for and go to their profile.</span></span>

4.  <span data-ttu-id="882cb-155">Ved hjælp af søgefeltet i kontaktkortet skal du finde jobbet ved hjælp af titlen eller det job-id, der blev aktiveret i Attract.</span><span class="sxs-lookup"><span data-stu-id="882cb-155">Using the job search box in the contact card, find the job using the title or the Job ID that was activated in Attract.</span></span> <span data-ttu-id="882cb-156">Hvis du ikke finder jobbet, skal du klikke på **Change ATS** (Skift ATS) for at finde den korrekte forekomst af Attract.</span><span class="sxs-lookup"><span data-stu-id="882cb-156">If you don’t find the job, click **Change ATS** to find the correct Attract instance.</span></span>

5. <span data-ttu-id="882cb-157">Når jobbet er valgt, skal du klikke på **Eksport**.</span><span class="sxs-lookup"><span data-stu-id="882cb-157">After the job is selected, click **Export**.</span></span> <span data-ttu-id="882cb-158">Kandidaten hentes nu af Attract.</span><span class="sxs-lookup"><span data-stu-id="882cb-158">The candidate is now fetched by Attract.</span></span>

6.  <span data-ttu-id="882cb-159">Gå til Attract, og åbn det pågældende job.</span><span class="sxs-lookup"><span data-stu-id="882cb-159">Go to Attract and open the respective job.</span></span> <span data-ttu-id="882cb-160">Du kan finde den kandidat, som du lige har eksporteret i stadiet **Jobkandidat** for jobbet.</span><span class="sxs-lookup"><span data-stu-id="882cb-160">You will find the candidate that you just exported in the **Prospect** stage of the job.</span></span>

### <a name="in-ats-indicator"></a><span data-ttu-id="882cb-161">In-ATS indicator</span><span class="sxs-lookup"><span data-stu-id="882cb-161">In-ATS indicator</span></span> 

<span data-ttu-id="882cb-162">Når du bruger LinkedIn Recruiter, kan du følge med i, om en kandidat har søgt andre jobs i organisationen, se, hvor de befinder sig i jobansøgningernes forskellige faser, samt gennemse tilbagemeldinger og kommentarer fra Attract i LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="882cb-162">Using LinkedIn recruiter, you can track whether a candidate has applied to other jobs in your organization, look at where they are in different stages of job applications, and view the feedback and comments from Attract in LinkedIn Recruiter.</span></span>

1.  <span data-ttu-id="882cb-163">Åbn LinkedIn Recruiter, og find den kandidatprofil, du leder efter.</span><span class="sxs-lookup"><span data-stu-id="882cb-163">Open LinkedIn Recruiter and locate the candidate profile that you are looking for.</span></span>

2.  <span data-ttu-id="882cb-164">Rul ned for at få vist sektionen **In-ATS** i kandidatens profil.</span><span class="sxs-lookup"><span data-stu-id="882cb-164">Scroll down to view the **In-ATS** section on the candidate’s profile.</span></span>

3.  <span data-ttu-id="882cb-165">Du kan bruge denne widget til at få vist alle de oplysninger om kandidaten, der findes i Attract, fra LinkedIn Recruiter-visningen.</span><span class="sxs-lookup"><span data-stu-id="882cb-165">You can use this widget to view all of the information about the candidate that’s present in Attract from within the LinkedIn Recruiter view.</span></span>

4.  <span data-ttu-id="882cb-166">Vælg fanen **Jobs & Statuses** for at få vist job, som de er en del af, den seneste status, og hvordan de har rykket i forhold til hvert job.</span><span class="sxs-lookup"><span data-stu-id="882cb-166">Select the **Jobs & Statuses** tab to see jobs they are part of, the latest status, and how they have been moving against each job.</span></span>

5.  <span data-ttu-id="882cb-167">Vælg fanen **Interview Feedback** for at se feedback, som interviewerne har sendt i Attract.</span><span class="sxs-lookup"><span data-stu-id="882cb-167">Select the **Interview Feedback** tab to see feedback that the interviewers have submitted in Attract.</span></span>

6.  <span data-ttu-id="882cb-168">Vælg fanen **Notes** for at få vist noter, der er hentet for denne ansøger i Attract.</span><span class="sxs-lookup"><span data-stu-id="882cb-168">Select the **Notes** tab to see notes that have been captured for this applicant in Attract.</span></span>

> [!NOTE]
> <span data-ttu-id="882cb-169">Kandidat- og ansøgningsdata synkroniseres ikke med LinkedIn Recruiter, hvis kandidaten ikke har passeret kandidatemnestadiet.</span><span class="sxs-lookup"><span data-stu-id="882cb-169">Candidate and application data will not be synced to LinkedIn Recruiter if the candidate hasn't moved past the prospect stage.</span></span>

### <a name="inmail-history"></a><span data-ttu-id="882cb-170">InMail-historik</span><span class="sxs-lookup"><span data-stu-id="882cb-170">InMail history</span></span>

<span data-ttu-id="882cb-171">LinkedIn InMail-historikken er tilgængelig i LinkedIn Recruiter med adgang på kontraktniveau.</span><span class="sxs-lookup"><span data-stu-id="882cb-171">The LinkedIn InMail history is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="882cb-172">Når den er aktiveret, kan du få vist hele InMail-historikken for kandidaten.</span><span class="sxs-lookup"><span data-stu-id="882cb-172">When it is enabled, you can view your entire InMail history with the candidate.</span></span> <span data-ttu-id="882cb-173">Du kan også se, hvem fra din organisation der har udvekslet InMail med kandidaten, men du ikke kan få vist meddelelserne mellem dem.</span><span class="sxs-lookup"><span data-stu-id="882cb-173">You can also see who else from your organization has exchanged InMail with the candidate, however you can't view the messages between them.</span></span>

<span data-ttu-id="882cb-174">Hvis du vil se InMail-historik, skal du gå til en kandidats profil, gå til fanen **LinkedIn** og rulle til bunden af siden for at få vist historikken.</span><span class="sxs-lookup"><span data-stu-id="882cb-174">To view InMail history, go to a candidate’s profile, go to the **LinkedIn** tab and scroll to the bottom of the page to view the history.</span></span> <span data-ttu-id="882cb-175">Du kan få vist historik for InMail, hvis du har haft en diskussion med kandidaten.</span><span class="sxs-lookup"><span data-stu-id="882cb-175">You can view InMail history if you have had a discussion with the candidate.</span></span> <span data-ttu-id="882cb-176">Meddelelserne fra InMail synkroniseres med Attract med få timers mellemrum.</span><span class="sxs-lookup"><span data-stu-id="882cb-176">The messages from InMail will sync with Attract every couple of hours.</span></span>

### <a name="notes-history"></a><span data-ttu-id="882cb-177">Oversigt over noter</span><span class="sxs-lookup"><span data-stu-id="882cb-177">Notes history</span></span> 

<span data-ttu-id="882cb-178">LinkedIn-noterne er tilgængelige i LinkedIn Recruiter med adgang på kontraktniveau.</span><span class="sxs-lookup"><span data-stu-id="882cb-178">The LinkedIn notes history is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="882cb-179">Når den er aktiveret, kan du få vist de noter, der er hentet om kandidaten fra forskellige rekrutteringsmedarbejdere fra din organisation.</span><span class="sxs-lookup"><span data-stu-id="882cb-179">When it is enabled, you can view the notes that have been captured about the candidate by different recruiters from your organization.</span></span>

<span data-ttu-id="882cb-180">Hvis du vil se Notes-historikken, skal du gå til en kandidats profil, gå til fanen **LinkedIn** og rulle til bunden af siden for at få vist historikken.</span><span class="sxs-lookup"><span data-stu-id="882cb-180">To view Notes history, go to a candidate’s profile, go to the **LinkedIn** tab and scroll to the bottom of the page to view the history.</span></span> <span data-ttu-id="882cb-181">Du kan se alle noterne om kandidaten i LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="882cb-181">You can view all the notes about the candidate from LinkedIn Recruiter.</span></span>

### <a name="inmail-stub-profile"></a><span data-ttu-id="882cb-182">InMail-stubprofil</span><span class="sxs-lookup"><span data-stu-id="882cb-182">InMail stub profile</span></span>

<span data-ttu-id="882cb-183">InMail-stubprofilen er tilgængelig i LinkedIn Recruiter med adgang på kontraktniveau.</span><span class="sxs-lookup"><span data-stu-id="882cb-183">The InMail stub profile is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="882cb-184">Hvis kandidaterne accepterer at dele deres LinkedIn-profiler med enhver bruger i din organisation, kan du spore kandidaterne i Attract, og der bliver oprettet en ny kandidatpost for hver kandidat.</span><span class="sxs-lookup"><span data-stu-id="882cb-184">If candidates agree to share their LinkedIn profiles with any user in your organization, you can track the candidates in Attract and a new candidate record will be created for each candidate.</span></span> <span data-ttu-id="882cb-185">Du kan få vist kandidatens e-mailadresse, hvis kandidaten allerede findes i systemet med en e-mailadresse eller har valgt at dele sin adresse med rekrutteringsmedarbejderen.</span><span class="sxs-lookup"><span data-stu-id="882cb-185">You can view candidate's email address if the candidate already exists in the system with an email address or has chosen to share their address with the recruiter.</span></span>

<span data-ttu-id="882cb-186">For at få vist listen over kandidater skal du gå til **Talentpuljer** for at få vist en systemoprettet LinkedIn-talentpulje.</span><span class="sxs-lookup"><span data-stu-id="882cb-186">To view the list of candidates, go to **Talent pools** to see a system-created LinkedIn talent pool.</span></span> <span data-ttu-id="882cb-187">Denne talentpulje indeholder listen over kandidater og deres stubprofiler som modtaget fra LinkedIn med kandidatens fornavn og efternavn.</span><span class="sxs-lookup"><span data-stu-id="882cb-187">This talent pool contains the list candidates and their stub profiles as received from LinkedIn, showing the candidate's first name and last name.</span></span> <span data-ttu-id="882cb-188">Kandidatens e-mail-id vises, hvis kandidaten har valgt at dele sin e-mailadresse.</span><span class="sxs-lookup"><span data-stu-id="882cb-188">The candidate’s email ID will be displayed if the candidate had chosen to share their email address.</span></span>
