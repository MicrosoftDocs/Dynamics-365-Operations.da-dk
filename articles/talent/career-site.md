---
title: Funktioner for karrierewebsteder i Attract
description: Denne artikel indeholder en oversigt over funktioner for kandidater på karrierewebstedet i Attract.
author: josaw1
manager: AnnBe
ms.date: 02/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-02-12
ms.dyn365.ops.version: AX 7.1.0, Talent April 2018 update
ms.openlocfilehash: 087ab4034a1e601e7f3514c77d56ef54b0c5c52d
ms.sourcegitcommit: 1ee613a88edddab036d145f27f19d071a4b8ad24
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/13/2019
ms.locfileid: "389954"
---
# <a name="career-site-functionality-in-attract"></a><span data-ttu-id="08b94-103">Funktioner for karrierewebsteder i Attract</span><span class="sxs-lookup"><span data-stu-id="08b94-103">Career site functionality in Attract</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="08b94-104">Denne artikel indeholder en oversigt over funktioner for kandidater på karrierewebstedet i Microsoft Dynamics 365 for Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="08b94-104">This topic provides an overview of the candidate-facing career site functionality in Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="08b94-105">I artiklen beskrives også, hvordan du konfigurerer denne funktion.</span><span class="sxs-lookup"><span data-stu-id="08b94-105">It also explains how to set up this functionality.</span></span>

<span data-ttu-id="08b94-106">Attract indeholder ét karrierewebsted for hvert miljø i en lejer.</span><span class="sxs-lookup"><span data-stu-id="08b94-106">Attract provides one career site for each environment in a tenant.</span></span> <span data-ttu-id="08b94-107">F.eks. hvis en organisation har et miljø til udvikling og et testmiljø, klargøres ét karrierewebsted til udviklingsmiljøet og et andet til testmiljøet.</span><span class="sxs-lookup"><span data-stu-id="08b94-107">For example, if an organization has a development environment and a test environment, one career site is provisioned for the development environment, and another career site is provisioned for the test environment.</span></span> <span data-ttu-id="08b94-108">Hvert karrierewebsted er fuldstændigt isoleret og har sit eget system til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="08b94-108">Each career site is completely isolated and has its own authentication mechanism.</span></span> <span data-ttu-id="08b94-109">Job- og kandidatprofiler deles ikke mellem karrierewebstederne.</span><span class="sxs-lookup"><span data-stu-id="08b94-109">Jobs and candidate profiles aren't shared between career sites.</span></span>

<span data-ttu-id="08b94-110">Som standard er karrierewebstedet offentligt.</span><span class="sxs-lookup"><span data-stu-id="08b94-110">By default, the career site is public.</span></span> <span data-ttu-id="08b94-111">Derfor kan kandidater få vist alle job, der er markeret som eksterne, uden at skulle logge på.</span><span class="sxs-lookup"><span data-stu-id="08b94-111">Therefore, candidates can view all jobs that are marked as external without having to sign in.</span></span> <span data-ttu-id="08b94-112">Alle andre handlinger kræver dog, at kandidaterne er logget på.</span><span class="sxs-lookup"><span data-stu-id="08b94-112">However, all other actions require that candidates sign in.</span></span>

## <a name="career-site-management"></a><span data-ttu-id="08b94-113">Administration af karrierewebsted</span><span class="sxs-lookup"><span data-stu-id="08b94-113">Career site management</span></span>

<span data-ttu-id="08b94-114">For at angive værdierne for følgende elementer skal brugeren logge på Attract som administrator, vælge **Administration** i menuen **Indstillinger** (tandhjulsymbolet) og derefter vælge fanen **Firmaoplysninger**.</span><span class="sxs-lookup"><span data-stu-id="08b94-114">To set the values for the following items, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu (the gear symbol), and then select the **Company information** tab.</span></span>

-   <span data-ttu-id="08b94-115">**Organisationsnavn** - Organisationens navn vises på navigationslinjen øverst i karrierewebstedet.</span><span class="sxs-lookup"><span data-stu-id="08b94-115">**Organization name** - The organization name appears on the navigation bar at the top of the career site.</span></span> <span data-ttu-id="08b94-116">Hvis kandidaterne vælger organisationsnavnet, kommer de til en side over alle ledige job.</span><span class="sxs-lookup"><span data-stu-id="08b94-116">By selecting the organization name, candidates go to a page that lists all open jobs.</span></span>

-   <span data-ttu-id="08b94-117">**Organisationslogo** - Et billede af organisationens logo vises øverst til venstre på karrierewebstedet.</span><span class="sxs-lookup"><span data-stu-id="08b94-117">**Organization logo** - An image of the organization's logo appears in the upper left of the career site.</span></span> <span data-ttu-id="08b94-118">Hvis kandidaterne vælger logobilledet, kommer de til en side over alle ledige job.</span><span class="sxs-lookup"><span data-stu-id="08b94-118">By selecting the logo image, candidates go to a page that lists all open jobs.</span></span>

    >   [!NOTE] 
    >   <span data-ttu-id="08b94-119">Logobilledet, der vises på karrierewebstedet, har en fast højde på 20 pixel (px).</span><span class="sxs-lookup"><span data-stu-id="08b94-119">The logo image that appears on the career site has a fixed height of 20 pixels (px).</span></span> <span data-ttu-id="08b94-120">Det billede, du føjer til Administration, skaleres, så det passer i størrelsen.</span><span class="sxs-lookup"><span data-stu-id="08b94-120">The image that you add in the Admin center is scaled to fit.</span></span> <span data-ttu-id="08b94-121">Afhængigt af billedet kan bredden evt. blive ændret.</span><span class="sxs-lookup"><span data-stu-id="08b94-121">Therefore, depending on the image, the width might change.</span></span>
 
<span data-ttu-id="08b94-122">For at angive værdierne for følgende elementer skal brugeren logge på Attract som administrator, vælge **Administration** i menuen **Indstillinger** og derefter vælge fanen **Administration af karrierewebsted**.</span><span class="sxs-lookup"><span data-stu-id="08b94-122">To set the values for the following items, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu, and then select the **Career site management** tab.</span></span>

-   <span data-ttu-id="08b94-123">**Optimering af søgemaskine** – Når denne indstilling er aktiveret, kan der søges i alle offentlige job, der opslås på Attract-karrierewebstedet, ved hjælp af søgemaskiner som Bing og Google.</span><span class="sxs-lookup"><span data-stu-id="08b94-123">**Search Engine Optimization** - When enabled, all public jobs posted to Attract career site will be searchable using search engines like Bing and Google.</span></span>

    >   [!NOTE] 
    >   <span data-ttu-id="08b94-124">Der kan være en forsinkelse fra denne indstilling aktiveres, til søgeresultater vises, afhængigt af hvilken søgemaskine du bruger.</span><span class="sxs-lookup"><span data-stu-id="08b94-124">There might be a delay between turning this setting on and search results appearing, depending on the search engine that you are using.</span></span>
         
## <a name="career-site-urls"></a><span data-ttu-id="08b94-125">URL-adresser til karrierewebsteder</span><span class="sxs-lookup"><span data-stu-id="08b94-125">Career site URLs</span></span>

<span data-ttu-id="08b94-126">Følgende liste indeholder de almindeligt anvendte karrierewebsteders URL-adresser, og hvordan du får adgang til dem.</span><span class="sxs-lookup"><span data-stu-id="08b94-126">The following list contains the commonly used career site URLs and how to access them.</span></span>

-   <span data-ttu-id="08b94-127">**URL-adresse til startside for karrierewebsted** - Hvis du vil have vist URL-adressen til startsiden for karrierewebstedet, skal du logge på Attract som administrator, vælge **Administration** i menuen **Indstillinger** og derefter vælge fanen **Administration af karrierewebsted**.</span><span class="sxs-lookup"><span data-stu-id="08b94-127">**Career site home page URL** - To view the career site home page URL, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu, and then select the **Career site management** tab.</span></span>

-   <span data-ttu-id="08b94-128">**URL-adresse til ansøgning om individuelt jobopslag** - Når du [slå et eksternt job op](Creating-jobs-Attract.md#postings) for første gang, kan du kopiere linket **Ansøg** fra programmet Attract.</span><span class="sxs-lookup"><span data-stu-id="08b94-128">**Individual job post apply URL** - When you [post an external job](Creating-jobs-Attract.md#postings) for the first time, you can copy the **Apply** link from the Attract application.</span></span> <span data-ttu-id="08b94-129">URL-adressen til dette link har følgende format: [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>/apply](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e/apply)</span><span class="sxs-lookup"><span data-stu-id="08b94-129">The URL for this link will be in the following format: [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>/apply](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e/apply)</span></span>

-   <span data-ttu-id="08b94-130">**URL-adresse til individuelt jobopslag** - URL-adressen til jobopslaget er en understreng af URL-adressen til ansøgningen.</span><span class="sxs-lookup"><span data-stu-id="08b94-130">**Individual job post URL** - The URL of the job post is a substring of the Apply URL.</span></span> <span data-ttu-id="08b94-131">Den består af alt op til og med jobnummeret.</span><span class="sxs-lookup"><span data-stu-id="08b94-131">It consists of everything up through the job number.</span></span> <span data-ttu-id="08b94-132">Derfor, for den foregående URL-adresse til ansøgning, er URL-adressen til jobopslaget [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e)</span><span class="sxs-lookup"><span data-stu-id="08b94-132">Therefore, for the preceding Apply URL, the job post URL is [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e)</span></span>

## <a name="authentication-options"></a><span data-ttu-id="08b94-133">Godkendelsesindstillinger</span><span class="sxs-lookup"><span data-stu-id="08b94-133">Authentication options</span></span>

<span data-ttu-id="08b94-134">Kandidaterne har følgende logonmuligheder for et Attract-karrierewebsted:</span><span class="sxs-lookup"><span data-stu-id="08b94-134">Candidates have the following sign-in options for an Attract career site:</span></span>

-   <span data-ttu-id="08b94-135">Personlig konto:</span><span class="sxs-lookup"><span data-stu-id="08b94-135">Personal account:</span></span>

    -   <span data-ttu-id="08b94-136">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="08b94-136">LinkedIn</span></span>

    -   <span data-ttu-id="08b94-137">Microsoft</span><span class="sxs-lookup"><span data-stu-id="08b94-137">Microsoft</span></span>

    -   <span data-ttu-id="08b94-138">Google</span><span class="sxs-lookup"><span data-stu-id="08b94-138">Google</span></span>

    -   <span data-ttu-id="08b94-139">Facebook</span><span class="sxs-lookup"><span data-stu-id="08b94-139">Facebook</span></span>

-   <span data-ttu-id="08b94-140">Arbejds- eller skolekonto:</span><span class="sxs-lookup"><span data-stu-id="08b94-140">Work or school account:</span></span>

    -   <span data-ttu-id="08b94-141">Microsoft Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="08b94-141">Microsoft Azure Active Directory (Azure AD)</span></span>

<span data-ttu-id="08b94-142">Azure AD-logon er kun beregnet til interne kandidater.</span><span class="sxs-lookup"><span data-stu-id="08b94-142">Azure AD sign-in is intended only for internal candidates.</span></span> <span data-ttu-id="08b94-143">Derfor fungerer det kun for interne kandidater, der bruger deres firmas Azure AD-legitimationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="08b94-143">Therefore, it works only for internal candidates who use their company Azure AD credentials.</span></span> <span data-ttu-id="08b94-144">F.eks. ønsker en kandidat, der aktuelt er medarbejder hos Contoso, Ltd, at ansøge om et job i en ikke-relateret virksomhed, Alpine Ski House.</span><span class="sxs-lookup"><span data-stu-id="08b94-144">For example, a candidate who is currently an employee of Contoso Ltd wants to apply for a job in an unrelated company, Alpine Ski House.</span></span> <span data-ttu-id="08b94-145">I dette tilfælde kan medarbejderen ikke logge på, hvis han eller hun forsøger at bruge sine Azure AD-legitimationsoplysninger fra Contoso Ltd.</span><span class="sxs-lookup"><span data-stu-id="08b94-145">In this case, the sign-in will be unsuccessful if the employee tries to use Azure AD credentials from Contoso Ltd.</span></span>

## <a name="create-and-maintain-a-profile"></a><span data-ttu-id="08b94-146">Oprette og vedligeholde en profil</span><span class="sxs-lookup"><span data-stu-id="08b94-146">Create and maintain a profile</span></span>

<span data-ttu-id="08b94-147">Når kandidater har logget på karrierewebstedet, kan de vælge **Min profil** på navigationslinjen øverst på siden for at oprette og vedligeholde deres profil.</span><span class="sxs-lookup"><span data-stu-id="08b94-147">After candidates sign in to the career site, they can select **My profile** on the navigation bar at the top of the page to create and maintain their profile.</span></span>
<span data-ttu-id="08b94-148">Profilen indeholder personlige oplysninger, oplysninger om arbejdserfaring og uddannelse, dokumenter, links og oplysninger om færdigheder.</span><span class="sxs-lookup"><span data-stu-id="08b94-148">The profile includes personal information, information about work experience, education details, documents, links, and information about skill sets.</span></span> <span data-ttu-id="08b94-149">Når en profil er oprettet, kan den bruges til at ansøge om job, som kandidaten er interesseret i.</span><span class="sxs-lookup"><span data-stu-id="08b94-149">After a profile is created, it can be used to apply for jobs that the candidate is interested in.</span></span> <span data-ttu-id="08b94-150">Profiler hjælper også Attract med at anbefale de rigtige job til kandidater.</span><span class="sxs-lookup"><span data-stu-id="08b94-150">Profiles also help Attract recommend the right jobs to candidates.</span></span>

>   [!NOTE]
>   <span data-ttu-id="08b94-151">Hvis en kandidat bruger et e-mail-id til at logge på ved hjælp af en af godkendelsesudbyder, der er angivet ovenfor, anvendes standardkontaktens e-mail-id, der er knyttet til profilen.</span><span class="sxs-lookup"><span data-stu-id="08b94-151">If a candidate uses an email ID to sign in using one of the authentication providers listed above, that email ID will default to the contact email ID associated with the profile.</span></span> <span data-ttu-id="08b94-152">Id'et kan dog ændres når som helst og er helt uafhængigt af det første id.</span><span class="sxs-lookup"><span data-stu-id="08b94-152">However, the latter can be changed at any time and is completely independent of the former.</span></span> <span data-ttu-id="08b94-153">Attract bruger altid det kontakt-e-mail-id'et, der skal knyttes til din profil, til al e-mailkommunikation.</span><span class="sxs-lookup"><span data-stu-id="08b94-153">Attract will always use the contact email ID to associate with your profile for all email communications.</span></span>

## <a name="find-the-right-job"></a><span data-ttu-id="08b94-154">Finde det rette job</span><span class="sxs-lookup"><span data-stu-id="08b94-154">Find the right job</span></span>

<span data-ttu-id="08b94-155">På joblistesiden kan kandidaterne søge efter et bestemt job ved at indtaste søgeord.</span><span class="sxs-lookup"><span data-stu-id="08b94-155">On the job list page, candidates can search for a specific job by entering search terms.</span></span> <span data-ttu-id="08b94-156">Søgefunktionen leder efter søgeord i stillingsbetegnelser og jobbeskrivelser og viser de relevante job som resultat.</span><span class="sxs-lookup"><span data-stu-id="08b94-156">The search functionality looks for the search terms in job titles and job descriptions, and shows relevant jobs as results.</span></span> <span data-ttu-id="08b94-157">Kandidaterne kan filtrere resultaterne når som helst baseret på jobstedet eller jobfunktionen.</span><span class="sxs-lookup"><span data-stu-id="08b94-157">Candidates can filter the results at any time, based on the job location or job function.</span></span>

<span data-ttu-id="08b94-158">Kandidaterne kan også se en række anbefalede job på karrierewebstedet.</span><span class="sxs-lookup"><span data-stu-id="08b94-158">Candidates can also view a set of recommended jobs on the career site.</span></span> <span data-ttu-id="08b94-159">Hvilke job der anbefales til en kandidat, afhænger af kandidatens tidligere ansøgninger, profil og CV'er.</span><span class="sxs-lookup"><span data-stu-id="08b94-159">The jobs that are recommended to a candidate are based on the candidate's past applications, profile, and resumes.</span></span>

>   [!NOTE] 
>   <span data-ttu-id="08b94-160">Jobanbefalinger vises kun, hvis der er opslået mindst 10 job på karrierewebstedet, og hvis kandidaten har fuldført en profil.</span><span class="sxs-lookup"><span data-stu-id="08b94-160">Job recommendations are shown only if at least 10 jobs are posted on the career site, and if the candidate has completed a profile.</span></span>

## <a name="apply-for-jobs"></a><span data-ttu-id="08b94-161">Ansøge om job</span><span class="sxs-lookup"><span data-stu-id="08b94-161">Apply for jobs</span></span>

<span data-ttu-id="08b94-162">Når kandidaterne har fundet det rigtige job, kan de ansøge ved hjælp af knappen **Ansøg** på siden med **Jobdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="08b94-162">After candidates find the right job, they can apply by using the **Apply** button on the **Job details** page.</span></span> <span data-ttu-id="08b94-163">På dette tidspunkt kan ansøgerne enten oprette en ny profil eller gennemse oplysningerne i deres eksisterende profil.</span><span class="sxs-lookup"><span data-stu-id="08b94-163">At this point, candidates can either create a new profile or review the information in their existing profile.</span></span>
<span data-ttu-id="08b94-164">De kan også overføre et CV efter behov og derefter sende jobansøgningen.</span><span class="sxs-lookup"><span data-stu-id="08b94-164">Candidates can also upload a resume, as required, and then submit the job application.</span></span>

## <a name="check-application-status"></a><span data-ttu-id="08b94-165">Kontrollere ansøgningsstatus</span><span class="sxs-lookup"><span data-stu-id="08b94-165">Check application status</span></span>

<span data-ttu-id="08b94-166">Når kandidaterne har ansøgt om et eller flere job, kan de vælge **Ansøgninger** på navigationslinjen øverst på siden for at få vist deres åbne og lukkede ansøgninger.</span><span class="sxs-lookup"><span data-stu-id="08b94-166">After candidates apply for one or more jobs, they can select **Applications** on the navigation bar at the top of the page to view their open and closed applications.</span></span> <span data-ttu-id="08b94-167">Når kandidaterne åbner en af deres ansøgninger, kan de se det aktuelle stadie og evt. ventende handlinger, som de skal udføre.</span><span class="sxs-lookup"><span data-stu-id="08b94-167">When candidates open one of their applications, they see the current stage and any pending action items that they must complete.</span></span> <span data-ttu-id="08b94-168">Hvis en kandidat f.eks. skal angive potentielle datoer for en personlig samtale, vises de tilgængelige indstillinger på siden.</span><span class="sxs-lookup"><span data-stu-id="08b94-168">For example, if a candidate must provide potential dates for an in-person interview, the page shows the available options.</span></span>

## <a name="internal-jobs"></a><span data-ttu-id="08b94-169">Interne job</span><span class="sxs-lookup"><span data-stu-id="08b94-169">Internal jobs</span></span>

<span data-ttu-id="08b94-170">Job, der er markeret som interne og opslået på Attract-karrierewebstedet, vises i øjeblikket ikke på karrierewebstedet.</span><span class="sxs-lookup"><span data-stu-id="08b94-170">Currently, jobs that are marked as internal and posted to the Attract career site don't appear on the career site.</span></span> <span data-ttu-id="08b94-171">De er kun tilgængelige via en direkte **Ansøg** URL-adresse, der kan kopieres fra programmet Attract.</span><span class="sxs-lookup"><span data-stu-id="08b94-171">They are only accessible using the direct **Apply** URL that can be copied from the Attract application.</span></span>
