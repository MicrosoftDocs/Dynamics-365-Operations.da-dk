---
title: Slå jobs op på eksterne karrierewebsteder via Attract
description: Dette emne beskriver, hvordan du anvender Dynamics 365 for Talent - Attract til at slå jobs op på eksterne rekrutteringswebsteder
author: pganapmsft
manager: AnnBe
ms.date: 03/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-03-19
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: eca599ad189edae29ef2de496196b08799a5e745
ms.sourcegitcommit: 1653d1e28d02f8a9a4bea8df562ac98d7a350ed1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/15/2019
ms.locfileid: "993662"
---
# <a name="post-jobs-to-external-career-sites-from-attract"></a><span data-ttu-id="8163a-103">Slå jobs op på eksterne karrierewebsteder via Attract</span><span class="sxs-lookup"><span data-stu-id="8163a-103">Post jobs to external career sites from Attract</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8163a-104">Du vil gerne have, at dine ledige stillinger ses af så mange kvalificerede kandidater som muligt.</span><span class="sxs-lookup"><span data-stu-id="8163a-104">You want to get your open positions in front of as many qualified candidates as possible.</span></span> <span data-ttu-id="8163a-105">Rekrutteringswebsteder såsom Broadbean kan hjælpe dig med at nå dette mål.</span><span class="sxs-lookup"><span data-stu-id="8163a-105">Recruiting sites such as Broadbean help you accomplish this goal.</span></span> <span data-ttu-id="8163a-106">Microsoft Dynamics 365 Talent: Attract giver dig nu mulighed for at slå jobs op på Broadbean, og Microsoft stiller konstant nye tilbud til rådighed på dette område.</span><span class="sxs-lookup"><span data-stu-id="8163a-106">Microsoft Dynamics 365 Talent: Attract now lets you post jobs to Broadbean, and Microsoft is constantly providing new offerings in this area.</span></span>

## <a name="post-jobs-to-broadbean"></a><span data-ttu-id="8163a-107">Slå jobs op på Broadbean</span><span class="sxs-lookup"><span data-stu-id="8163a-107">Post jobs to Broadbean</span></span>

<span data-ttu-id="8163a-108">Du skal konfigurere integrationen af Broadbean, før du kan slå jobs op på Broadbean.</span><span class="sxs-lookup"><span data-stu-id="8163a-108">Before you can post jobs to Broadbean, you must configure the Broadbean integration.</span></span>

> [!NOTE]
> - <span data-ttu-id="8163a-109">For at slå jobs op på eksterne websteder skal du have [Tilføjelsesprogrammet Omfattende ansættelser](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span><span class="sxs-lookup"><span data-stu-id="8163a-109">To post jobs to external sites, you must have the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>
> - <span data-ttu-id="8163a-110">Denne funktion findes på nuværende tidspunkt i prøveversionen.</span><span class="sxs-lookup"><span data-stu-id="8163a-110">This feature is currently in preview.</span></span> <span data-ttu-id="8163a-111">Hvis du ønsker at prøve det, skal du [slå det til i administratorindstillingerne i Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span><span class="sxs-lookup"><span data-stu-id="8163a-111">If you want to try it, you must [turn it on in the Attract admin settings](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

### <a name="configure-broadbean-integration"></a><span data-ttu-id="8163a-112">Konfigurer integrationen af Broadbean</span><span class="sxs-lookup"><span data-stu-id="8163a-112">Configure Broadbean integration</span></span>

1. <span data-ttu-id="8163a-113">Log på Attract som administrator.</span><span class="sxs-lookup"><span data-stu-id="8163a-113">Sign in to Attract as an admin.</span></span>
2. <span data-ttu-id="8163a-114">Vælg knappen **Indstillinger** (tandhjulssymbolet) i øverste højre hjørne af siden, og vælg dernæst **Administration**.</span><span class="sxs-lookup"><span data-stu-id="8163a-114">Select the **Settings** button (the gear symbol) in the upper-right corner of the page, and then select **Admin center**.</span></span>
3. <span data-ttu-id="8163a-115">På fanen **Indstillinger for jobportal** i afsnittet **Aktiver integration af Broadbean** skal du slå integrationen til.</span><span class="sxs-lookup"><span data-stu-id="8163a-115">On the **Job board settings** tab, in the **Enable Broadbean integration** section, turn on the integration.</span></span>
4. <span data-ttu-id="8163a-116">Kontakt Broadbean, og indtast dine oplysninger under **Brugernavn, Klient-id, Krypteringstoken**.</span><span class="sxs-lookup"><span data-stu-id="8163a-116">Contact Broadbean, and enter your information in **Username, Client ID, Encryption Token**.</span></span>

> [!WARNING]
> <span data-ttu-id="8163a-117">Dine legitimationsoplysninger til Broadbean er følsomme og fortrolige.</span><span class="sxs-lookup"><span data-stu-id="8163a-117">Your Broadbean credentials are sensitive and confidential.</span></span> <span data-ttu-id="8163a-118">Opbevar og del dem derfor ansvarligt.</span><span class="sxs-lookup"><span data-stu-id="8163a-118">Therefore, store and share them responsibly.</span></span> <span data-ttu-id="8163a-119">Alle med en administratorrolle i Attract kan se disse legitimationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="8163a-119">Anyone who has an Administrator role in Attract can view these credentials.</span></span>

> [!NOTE]
> <span data-ttu-id="8163a-120">Microsoft og Attract er ikke involveret i dannelsen og vedligeholdelsen af disse værdier.</span><span class="sxs-lookup"><span data-stu-id="8163a-120">Microsoft and Attract aren't involved in creating and maintaining these values.</span></span> <span data-ttu-id="8163a-121">Det er dit ansvar at ajourføre dem i Attract og arbejde sammen med Broadbean om at løse alle problemer vedrørende dine legitimationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="8163a-121">It's your responsibility to keep them up to date in Attract and to work with Broadbean to resolve any issues that involve your credentials.</span></span>

### <a name="post-a-job-to-broadbean"></a><span data-ttu-id="8163a-122">Slå et job op på Broadbean</span><span class="sxs-lookup"><span data-stu-id="8163a-122">Post a job to Broadbean</span></span>

<span data-ttu-id="8163a-123">Når du har slået Broadbean til, kan rekrutteringsmedarbejdere og administratorer slå et job op på webstedet.</span><span class="sxs-lookup"><span data-stu-id="8163a-123">After Broadbean has been turned on, recruiters and admins can post a job to it.</span></span> <span data-ttu-id="8163a-124">Du skal have an URL-adresse til jobrelaterede ansøgninger.</span><span class="sxs-lookup"><span data-stu-id="8163a-124">You must have an apply URL for the job.</span></span>

1. <span data-ttu-id="8163a-125">I Attract skal du åbne det job, du ønsker at slå op på Broadbean.</span><span class="sxs-lookup"><span data-stu-id="8163a-125">In Attract, open the job that you want to post to Broadbean.</span></span>
2. <span data-ttu-id="8163a-126">I afsnittet **Opslag** skal du vælge den knap for **Slå op nu**, der svarer til Broadbean.</span><span class="sxs-lookup"><span data-stu-id="8163a-126">In the **Postings** section, select the **Post Now** button that corresponds to Broadbean.</span></span>
3. <span data-ttu-id="8163a-127">Følg vejledningen i Broadbean-vinduet.</span><span class="sxs-lookup"><span data-stu-id="8163a-127">Follow the instructions in the Broadbean window.</span></span>

<span data-ttu-id="8163a-128">Attract videregiver følgende oplysninger til Broadbean:</span><span class="sxs-lookup"><span data-stu-id="8163a-128">Attract passes the following information to Broadbean:</span></span>

- <span data-ttu-id="8163a-129">Anmodnings-id</span><span class="sxs-lookup"><span data-stu-id="8163a-129">Request ID</span></span>
- <span data-ttu-id="8163a-130">Stillingsbetegnelse</span><span class="sxs-lookup"><span data-stu-id="8163a-130">Job title</span></span>
- <span data-ttu-id="8163a-131">Jobbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="8163a-131">Job description</span></span>
- <span data-ttu-id="8163a-132">Jobsted</span><span class="sxs-lookup"><span data-stu-id="8163a-132">Job location</span></span>
- <span data-ttu-id="8163a-133">URL-adressen til ansøgningen</span><span class="sxs-lookup"><span data-stu-id="8163a-133">Apply URL</span></span>
- <span data-ttu-id="8163a-134">Oplysninger om rekrutteringsansvarlig</span><span class="sxs-lookup"><span data-stu-id="8163a-134">Recruiter information</span></span>

<span data-ttu-id="8163a-135">Efter Broadbean har fuldført opslaget, fremgår det af afsnittet **Opslag** under jobbet i Attract, at Broadbean-statussen er angivet til **Opslået**.</span><span class="sxs-lookup"><span data-stu-id="8163a-135">After Broadbean successfully completes the posting, the **Postings** section of the job in Attract shows the Broadbean status as **Posted**.</span></span>

> [!NOTE]
> - <span data-ttu-id="8163a-136">Broadbean kræver feltet **Industri**.</span><span class="sxs-lookup"><span data-stu-id="8163a-136">Broadbean requires the **Industry** field.</span></span> <span data-ttu-id="8163a-137">Dette felt er på nuværende tidspunkt angivet til **IT** som standard.</span><span class="sxs-lookup"><span data-stu-id="8163a-137">Currently, this field is set to **IT** by default.</span></span> <span data-ttu-id="8163a-138">Du kan dog ændre værdien til den rette industri i vinduet for jobopslag på Broadbean.</span><span class="sxs-lookup"><span data-stu-id="8163a-138">However, you can change the value to the correct industry in the window for Broadbean job posting.</span></span>
> - <span data-ttu-id="8163a-139">Det tager lidt tid, før Broadbean har slået dit job op på alle de valgte jobportaler.</span><span class="sxs-lookup"><span data-stu-id="8163a-139">It takes some time for Broadbean to finish posting your job to all the job boards that you selected.</span></span> <span data-ttu-id="8163a-140">Der kan derfor være en mindre forsinkelse, før Attract viser en statusopdatering for jobbet.</span><span class="sxs-lookup"><span data-stu-id="8163a-140">Therefore, there might be a slight delay before Attract provides a status update for the job.</span></span>

### <a name="view-a-broadbean-job-posting"></a><span data-ttu-id="8163a-141">Se et jobopslag på Broadbean</span><span class="sxs-lookup"><span data-stu-id="8163a-141">View a Broadbean job posting</span></span>

<span data-ttu-id="8163a-142">Når du har slået et job op på Broadbean, kan du se det i Attract.</span><span class="sxs-lookup"><span data-stu-id="8163a-142">After you post a job to Broadbean, you can view it from Attract.</span></span>

1. <span data-ttu-id="8163a-143">I Attract skal du åbne det job, du ønsker at se på Broadbean.</span><span class="sxs-lookup"><span data-stu-id="8163a-143">In Attract, open the job that you want to view on Broadbean.</span></span>
2. <span data-ttu-id="8163a-144">I afsnittet **Opslag** skal du vælge den ellipseformede knap (**...**), der svarer til Broadbean, og dernæst vælge **Se**.</span><span class="sxs-lookup"><span data-stu-id="8163a-144">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **View**.</span></span>

<span data-ttu-id="8163a-145">Jobopslaget på Broadbean vises i et nyt vindue.</span><span class="sxs-lookup"><span data-stu-id="8163a-145">The Broadbean job posting appears in a new window.</span></span>

### <a name="update-a-broadbean-job-posting"></a><span data-ttu-id="8163a-146">Opdater et jobopslag på Broadbean</span><span class="sxs-lookup"><span data-stu-id="8163a-146">Update a Broadbean job posting</span></span>

<span data-ttu-id="8163a-147">Du kan opdatere et jobopslag på Broadbean på to måder:</span><span class="sxs-lookup"><span data-stu-id="8163a-147">You can update a Broadbean job posting in two ways.</span></span>

1. <span data-ttu-id="8163a-148">I Attract skal du åbne det job, du ønsker at opdatere.</span><span class="sxs-lookup"><span data-stu-id="8163a-148">In Attract, open the job that you want to update.</span></span>
2. <span data-ttu-id="8163a-149">I afsnittet **Opslag** skal du vælge den knap for **Opdater opslag**, der svarer til Broadbean.</span><span class="sxs-lookup"><span data-stu-id="8163a-149">In the **Postings** section, select the **Update Post** button that corresponds to Broadbean.</span></span>
3. <span data-ttu-id="8163a-150">Rediger opslaget i Broadbean-vinduet.</span><span class="sxs-lookup"><span data-stu-id="8163a-150">Edit the posting in the Broadbean window.</span></span>

<span data-ttu-id="8163a-151">eller</span><span class="sxs-lookup"><span data-stu-id="8163a-151">–or–</span></span>

1. <span data-ttu-id="8163a-152">I Attract skal du åbne det job, du ønsker at se på Broadbean.</span><span class="sxs-lookup"><span data-stu-id="8163a-152">In Attract, open the job that you want to view on Broadbean.</span></span>
2. <span data-ttu-id="8163a-153">I afsnittet **Opslag** skal du vælge den ellipseformede knap (**...**), der svarer til Broadbean, og dernæst vælge **Se**.</span><span class="sxs-lookup"><span data-stu-id="8163a-153">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **View**.</span></span>
3. <span data-ttu-id="8163a-154">I Broadbean-vinduet skal du redigere jobdetaljerne og dernæst slå jobbet op på ny.</span><span class="sxs-lookup"><span data-stu-id="8163a-154">In the Broadbean window, edit the job details, and then repost the job.</span></span> <span data-ttu-id="8163a-155">Jobdetaljerne i Attract ændres ikke.</span><span class="sxs-lookup"><span data-stu-id="8163a-155">The job details in Attract aren't changed.</span></span>

### <a name="remove-a-broadbean-job-posting"></a><span data-ttu-id="8163a-156">Fjern et jobopslag fra Broadbean</span><span class="sxs-lookup"><span data-stu-id="8163a-156">Remove a Broadbean job posting</span></span>

<span data-ttu-id="8163a-157">Du kan fjerne et jobopslag fra Broadbean efter behov.</span><span class="sxs-lookup"><span data-stu-id="8163a-157">You can remove a job posting from Broadbean as you require.</span></span>

1. <span data-ttu-id="8163a-158">I Attract skal du åbne det job, du ønsker at fjerne.</span><span class="sxs-lookup"><span data-stu-id="8163a-158">In Attract, open the job that you want to remove.</span></span>
2. <span data-ttu-id="8163a-159">I afsnittet **Opslag** skal du vælge den ellipseformede knap (**...**), der svarer til Broadbean, og dernæst vælge **Fjern opslag**.</span><span class="sxs-lookup"><span data-stu-id="8163a-159">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **Remove Post**.</span></span>

<span data-ttu-id="8163a-160">Når Broadbean har fjernet jobbet, får Broadbean-elementet i Attract en **Slå op nu**-knap.</span><span class="sxs-lookup"><span data-stu-id="8163a-160">After Broadbean removes the job, the Broadbean item in Attract has a **Post Now** button.</span></span> <span data-ttu-id="8163a-161">Fremkomsten af denne knap indikerer, at jobbet er blevet fjernet og kan slås op på ny.</span><span class="sxs-lookup"><span data-stu-id="8163a-161">The presence of this button indicates that the job has been removed and can be posted again.</span></span>

### <a name="troubleshoot-the-broadbean-integration"></a><span data-ttu-id="8163a-162">Fejlfinding i Broadbean-integrationen</span><span class="sxs-lookup"><span data-stu-id="8163a-162">Troubleshoot the Broadbean integration</span></span>

<span data-ttu-id="8163a-163">Hvis du har problemer med at slå et job op på Broadbean, kan du prøve disse trin:</span><span class="sxs-lookup"><span data-stu-id="8163a-163">If you're having trouble posting a job to Broadbean, try these steps.</span></span>

1. <span data-ttu-id="8163a-164">Kontroller, at de legitimationsoplysninger til Broadbean, du indtastede i Attract, er gyldige og korrekte.</span><span class="sxs-lookup"><span data-stu-id="8163a-164">Verify that the Broadbean credentials that you entered in Attract are valid and correct.</span></span>
2. <span data-ttu-id="8163a-165">Hvis de legitimationsoplysninger til Broadbean, du indtastede i Attract, er gyldige og korrekte, skal du kontakte [Broadbean-support](https://www.broadbean.com/resources/support/).</span><span class="sxs-lookup"><span data-stu-id="8163a-165">If the credentials are valid and correct, contact [Broadbean support](https://www.broadbean.com/resources/support/).</span></span>
3. <span data-ttu-id="8163a-166">Hvis problemet fortsætter, skal du kontakte [Microsoft-support](./talent-support.md).</span><span class="sxs-lookup"><span data-stu-id="8163a-166">If the issue persists, contact [Microsoft support](./talent-support.md).</span></span>
