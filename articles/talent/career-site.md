---
title: Karrierewebsted i Attract
description: "Denne artikel indeholder en oversigt over funktioner for kandidater på karrierewebstedet i Microsoft Dynamics 365 for Talent - Attract. I artiklen beskrives også, hvordan du konfigurerer denne funktion."
author: josaw
manager: AnnBe
ms.date: 10/18/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: 452e3e92ea32ab5f1e3720ab81ff2f7ea18b2a06
ms.contentlocale: da-dk
ms.lasthandoff: 10/22/2018

---
# <a name="career-site-functionality-in-attract"></a><span data-ttu-id="145fc-104">Karrierewebsted i Attract</span><span class="sxs-lookup"><span data-stu-id="145fc-104">Career site functionality in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="145fc-105">Denne artikel indeholder en oversigt over funktioner for kandidater på karrierewebstedet i Microsoft Dynamics 365 for Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="145fc-105">This article provides an overview of the candidate-facing career site functionality in Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="145fc-106">I artiklen beskrives også, hvordan du konfigurerer denne funktion.</span><span class="sxs-lookup"><span data-stu-id="145fc-106">It also explains how to set up this functionality.</span></span>

## <a name="overview"></a><span data-ttu-id="145fc-107">Overblik</span><span class="sxs-lookup"><span data-stu-id="145fc-107">Overview</span></span>

<span data-ttu-id="145fc-108">Attract indeholder ét karrierewebsted for de enkelte miljøer i en lejer.</span><span class="sxs-lookup"><span data-stu-id="145fc-108">Attract provides one career site for each environment in a tenant.</span></span> <span data-ttu-id="145fc-109">F.eks. hvis en organisation har et miljø til udvikling og et testmiljø, klargøres ét karrierewebsted til udviklingsmiljøet og et andet til testmiljøet.</span><span class="sxs-lookup"><span data-stu-id="145fc-109">For example, if an organization has a development environment and a test environment, one career site is provisioned for the development environment, and another career site is provisioned for the test environment.</span></span> <span data-ttu-id="145fc-110">Hver karrierewebsted er **fuldstændigt isoleret** og har sit eget system til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="145fc-110">Each career site is **completely isolated** and has its own authentication mechanism.</span></span> <span data-ttu-id="145fc-111">Job- og kandidatprofiler deles ikke mellem karrierewebstederne.</span><span class="sxs-lookup"><span data-stu-id="145fc-111">Jobs and candidate profiles aren't shared between career sites.</span></span>

<span data-ttu-id="145fc-112">Som standard er karrierewebstedet offentlig.</span><span class="sxs-lookup"><span data-stu-id="145fc-112">By default, the career site is public.</span></span> <span data-ttu-id="145fc-113">Derfor kan kandidater få vist alle job, der er markeret som eksterne, uden at skulle logge på.</span><span class="sxs-lookup"><span data-stu-id="145fc-113">Therefore, candidates can view all jobs that are marked as external without having to sign in.</span></span> <span data-ttu-id="145fc-114">Alle andre handlinger kræver dog, at kandidaterne er logget på.</span><span class="sxs-lookup"><span data-stu-id="145fc-114">However, all other actions require that candidates sign in.</span></span>

## <a name="career-site-management"></a><span data-ttu-id="145fc-115">Administration af karrierewebsted</span><span class="sxs-lookup"><span data-stu-id="145fc-115">Career site management</span></span>

<span data-ttu-id="145fc-116">Følgende elementer på karrierewebstedet styres af indstillingerne:</span><span class="sxs-lookup"><span data-stu-id="145fc-116">The following items on the career site are controlled by settings:</span></span>

- <span data-ttu-id="145fc-117">**Organisationsnavn:** Organisationens navn vises på navigationslinjen øverst i karrierewebstedet.</span><span class="sxs-lookup"><span data-stu-id="145fc-117">**Organization name:** The organization name appears on the navigation bar at the top of the career site.</span></span> <span data-ttu-id="145fc-118">Hvis kandidaterne vælger organisationsnavnet, kommer de til en side over alle ledige job.</span><span class="sxs-lookup"><span data-stu-id="145fc-118">By selecting the organization name, candidates go to a page that lists all open jobs.</span></span>
- <span data-ttu-id="145fc-119">**Organisationslogo:** Et billede af organisationens logo vises øverst til venstre på karrierewebstedet.</span><span class="sxs-lookup"><span data-stu-id="145fc-119">**Organization logo:** An image of the organization's logo appears in the upper left of the career site.</span></span> <span data-ttu-id="145fc-120">Hvis kandidaterne vælger logobilledet, kommer de til en side over alle ledige job.</span><span class="sxs-lookup"><span data-stu-id="145fc-120">By selecting the logo image, candidates go to a page that lists all open jobs.</span></span>

<span data-ttu-id="145fc-121">For at angive værdierne for organisationsnavn og -logo skal brugeren logge på Attract som administrator, vælge **Administration** i menuen **Indstillinger** (tandhjulsymbolet) og derefter vælge fanen **Firmaoplysninger**.</span><span class="sxs-lookup"><span data-stu-id="145fc-121">To set the values for the organization name and logo, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu (the gear symbol), and then select the **Company information** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="145fc-122">Logobilledet, der vises på karrierewebstedet, har en fast højde på 20 pixel (px).</span><span class="sxs-lookup"><span data-stu-id="145fc-122">The logo image that appears on the career site has a fixed height of 20 pixels (px).</span></span> <span data-ttu-id="145fc-123">Det billede, du føjer til administration, skaleres, så det passer i størrelsen.</span><span class="sxs-lookup"><span data-stu-id="145fc-123">The image that you add in the Admin center is scaled to fit.</span></span> <span data-ttu-id="145fc-124">Afhængigt af billedet kan bredden evt. blive ændret.</span><span class="sxs-lookup"><span data-stu-id="145fc-124">Therefore, depending on the image, the width might change.</span></span>

## <a name="career-site-url"></a><span data-ttu-id="145fc-125">URL-adresse til karrierewebsted</span><span class="sxs-lookup"><span data-stu-id="145fc-125">Career site URL</span></span>

<span data-ttu-id="145fc-126">Når du [slå et eksternt job op](./Creating-jobs-Attract.md#postings) for første gang, kan du kopiere linket **Ansøg** fra programmet Attract.</span><span class="sxs-lookup"><span data-stu-id="145fc-126">When you [post an external job](./Creating-jobs-Attract.md#postings) for the first time, you can copy the **Apply** link from the Attract application.</span></span> <span data-ttu-id="145fc-127">URL-adressen til dette link har følgende format: `https://jobs.talent.dynamics.com/jobs/<company_name>/<environment_number>/<job_number>/apply`</span><span class="sxs-lookup"><span data-stu-id="145fc-127">The URL for this link will be in the following format: `https://jobs.talent.dynamics.com/jobs/<company_name>/<environment_number>/<job_number>/apply`</span></span>

<span data-ttu-id="145fc-128">URL-adressen på karrierewebstedet er en understreng af **Ansøg** URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="145fc-128">The URL of the career site is a substring of the **Apply** URL.</span></span> <span data-ttu-id="145fc-129">Den består af alt op til og med firmanavnet.</span><span class="sxs-lookup"><span data-stu-id="145fc-129">It consists of everything up through the company name.</span></span> <span data-ttu-id="145fc-130">Derfor, for den foregående **Ansøg** URL-adresse, er karrierewebstedets URL-adresse `https://jobs.talent.dynamics.com/jobs/<company_name>/`.</span><span class="sxs-lookup"><span data-stu-id="145fc-130">Therefore, for the preceding **Apply** URL, the career site URL is `https://jobs.talent.dynamics.com/jobs/<company_name>/`.</span></span>

## <a name="authentication-options"></a><span data-ttu-id="145fc-131">Godkendelsesindstillinger</span><span class="sxs-lookup"><span data-stu-id="145fc-131">Authentication options</span></span>

<span data-ttu-id="145fc-132">Kandidaterne har følgende logonmuligheder på et Attract-karrierewebsted:</span><span class="sxs-lookup"><span data-stu-id="145fc-132">Candidates have the following sign-in options for an Attract career site:</span></span>

- <span data-ttu-id="145fc-133">Personlig konto:</span><span class="sxs-lookup"><span data-stu-id="145fc-133">Personal account:</span></span>

    - <span data-ttu-id="145fc-134">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="145fc-134">LinkedIn</span></span>
    - <span data-ttu-id="145fc-135">Microsoft</span><span class="sxs-lookup"><span data-stu-id="145fc-135">Microsoft</span></span>
    - <span data-ttu-id="145fc-136">Google</span><span class="sxs-lookup"><span data-stu-id="145fc-136">Google</span></span>
    - <span data-ttu-id="145fc-137">Facebook</span><span class="sxs-lookup"><span data-stu-id="145fc-137">Facebook</span></span>

- <span data-ttu-id="145fc-138">Arbejds- eller skolekonto:</span><span class="sxs-lookup"><span data-stu-id="145fc-138">Work or school account:</span></span>

    - <span data-ttu-id="145fc-139">Microsoft Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="145fc-139">Microsoft Azure Active Directory (Azure AD)</span></span>

<span data-ttu-id="145fc-140">Azure AD-logon er kun beregnet til interne kandidater.</span><span class="sxs-lookup"><span data-stu-id="145fc-140">Azure AD sign-in is intended only for internal candidates.</span></span> <span data-ttu-id="145fc-141">Derfor fungerer det kun for interne kandidater, der bruger deres firmas Azure AD-legitimationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="145fc-141">Therefore, it works only for internal candidates who use their company Azure AD credentials.</span></span> <span data-ttu-id="145fc-142">F.eks. ønsker en kandidat, der aktuelt er medarbejder hos Contoso, Ltd, at ansøge om et job i en ikke-relateret virksomhed, Alpine Ski House.</span><span class="sxs-lookup"><span data-stu-id="145fc-142">For example, a candidate who is currently an employee of Contoso Ltd wants to apply for a job in an unrelated company, Alpine Ski House.</span></span> <span data-ttu-id="145fc-143">I dette tilfælde kan medarbejderen ikke logge på, hvis han eller hun forsøger at bruge sine Azure AD-legitimationsoplysninger fra Contoso Ltd.</span><span class="sxs-lookup"><span data-stu-id="145fc-143">In this case, the sign-in will be unsuccessful if the employee tries to use his or her Azure AD credentials from Contoso Ltd.</span></span>

## <a name="create-and-maintain-a-profile"></a><span data-ttu-id="145fc-144">Oprette og vedligeholde en profil</span><span class="sxs-lookup"><span data-stu-id="145fc-144">Create and maintain a profile</span></span>

<span data-ttu-id="145fc-145">Når kandidater har logget på karrierewebstedet, kan de vælge **Min profil** på navigationslinjen øverst på siden for at oprette og vedligeholde deres profil.</span><span class="sxs-lookup"><span data-stu-id="145fc-145">After candidates sign in to the career site, they can select **My profile** on the navigation bar at the top of the page to create and maintain their profile.</span></span> <span data-ttu-id="145fc-146">Profilen indeholder personlige oplysninger, oplysninger om arbejdserfaring og uddannelse, dokumenter, links og oplysninger om færdigheder.</span><span class="sxs-lookup"><span data-stu-id="145fc-146">The profile includes personal information, information about work experience, education details, documents, links, and information about skill sets.</span></span> <span data-ttu-id="145fc-147">Når en profil er oprettet, kan den bruges til at ansøge om job, som kandidaten er interesseret i.</span><span class="sxs-lookup"><span data-stu-id="145fc-147">After a profile is created, it can be used to apply for jobs that the candidate is interested in.</span></span> <span data-ttu-id="145fc-148">Profiler hjælper også Attract med at anbefale de rigtige job til kandidater.</span><span class="sxs-lookup"><span data-stu-id="145fc-148">Profiles also help Attract recommend the right jobs to candidates.</span></span>

## <a name="find-the-right-job"></a><span data-ttu-id="145fc-149">Finde det rette job</span><span class="sxs-lookup"><span data-stu-id="145fc-149">Find the right job</span></span>

<span data-ttu-id="145fc-150">På joblistesiden kan kandidaterne søge efter et bestemt job ved at indtaste søgeord.</span><span class="sxs-lookup"><span data-stu-id="145fc-150">On the job list page, candidates can search for a specific job by entering search terms.</span></span> <span data-ttu-id="145fc-151">Søgefunktionen leder efter søgeord i stillingsbetegnelser og jobbeskrivelser og viser de relevante job som resultat.</span><span class="sxs-lookup"><span data-stu-id="145fc-151">The search functionality looks for the search terms in job titles and job descriptions, and shows relevant jobs as results.</span></span> <span data-ttu-id="145fc-152">Kandidaterne kan filtrere resultaterne når som helst baseret på jobstedet eller jobfunktionen.</span><span class="sxs-lookup"><span data-stu-id="145fc-152">Candidates can filter the results at any time, based on the job location or job function.</span></span>

<span data-ttu-id="145fc-153">Kandidaterne kan også se en række anbefalede job på karrierewebstedet.</span><span class="sxs-lookup"><span data-stu-id="145fc-153">Candidates can also view a set of recommended jobs on the career site.</span></span> <span data-ttu-id="145fc-154">Hvilke job der anbefales til en kandidat, afhænger af kandidatens tidligere ansøgninger, profil og CV'er.</span><span class="sxs-lookup"><span data-stu-id="145fc-154">The jobs that are recommended to a candidate are based on the candidate's past applications, profile, and resumes.</span></span>

> [!NOTE]
> <span data-ttu-id="145fc-155">Jobanbefalinger vises kun, hvis der er opslået mindst 10 job på karrierewebstedet, og hvis kandidaten har fuldført sin profil.</span><span class="sxs-lookup"><span data-stu-id="145fc-155">Job recommendations are shown only if at least 10 jobs are posted on the career site, and if the candidate has completed his or her profile.</span></span>

## <a name="apply-for-jobs"></a><span data-ttu-id="145fc-156">Ansøge om job</span><span class="sxs-lookup"><span data-stu-id="145fc-156">Apply for jobs</span></span>

<span data-ttu-id="145fc-157">Når kandidaterne har fundet det rigtige job, kan de ansøge ved hjælp af knappen **Ansøg** på siden med jobdetaljer.</span><span class="sxs-lookup"><span data-stu-id="145fc-157">After candidates find the right job, they can apply by using the **Apply** button on the job details page.</span></span> <span data-ttu-id="145fc-158">På dette tidspunkt kan ansøgerne enten oprette en helt ny profil eller gennemse oplysningerne i deres eksisterende profil.</span><span class="sxs-lookup"><span data-stu-id="145fc-158">At this point, candidates can either create a brand-new profile or review the information in their existing profile.</span></span> <span data-ttu-id="145fc-159">De kan også overføre et CV efter behov og derefter sende jobansøgningen.</span><span class="sxs-lookup"><span data-stu-id="145fc-159">Candidates can also upload a resume, as required, and then submit the job application.</span></span>

## <a name="check-application-status"></a><span data-ttu-id="145fc-160">Kontrollere ansøgningsstatus</span><span class="sxs-lookup"><span data-stu-id="145fc-160">Check application status</span></span>

<span data-ttu-id="145fc-161">Når kandidaterne har ansøgt om et eller flere job, kan de vælge **Ansøgninger** på navigationslinjen øverst på siden for at få vist deres åbne og lukkede ansøgninger.</span><span class="sxs-lookup"><span data-stu-id="145fc-161">After candidates apply for one or more jobs, they can select **Applications** on the navigation bar at the top of the page to view their open and closed applications.</span></span> <span data-ttu-id="145fc-162">Når kandidaterne åbner en af deres ansøgninger, kan de se det aktuelle stadie og evt. ventende handlinger, som de skal udføre.</span><span class="sxs-lookup"><span data-stu-id="145fc-162">When candidates open one of their applications, they see the current stage and any pending action items that they must complete.</span></span> <span data-ttu-id="145fc-163">Hvis en kandidat f.eks. skal angive potentielle datoer for en personlig samtale, viser siden vedkommendes indstillinger.</span><span class="sxs-lookup"><span data-stu-id="145fc-163">For example, if a candidate must provide potential dates for an in-person interview, the page shows his or her options.</span></span>

## <a name="internal-jobs"></a><span data-ttu-id="145fc-164">Interne job</span><span class="sxs-lookup"><span data-stu-id="145fc-164">Internal jobs</span></span>

<span data-ttu-id="145fc-165">Job, der er markeret som interne og opslået på Attract-karrierewebstedet, vises i øjeblikket ikke på karrierewebstedet.</span><span class="sxs-lookup"><span data-stu-id="145fc-165">Currently, jobs that are marked as internal and posted to the Attract career site don't appear on the career site.</span></span> <span data-ttu-id="145fc-166">De er kun tilgængelige via en direkte **Ansøg** URL-adresse, der kan kopieres fra programmet Attract.</span><span class="sxs-lookup"><span data-stu-id="145fc-166">They are accessible only via the direct **Apply** URL that can be copied from the Attract application.</span></span>

