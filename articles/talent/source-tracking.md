---
title: Spor kandidatkilder i Attract
description: Dette emne indeholder oplysninger om at spore kilden til kandidatprofiler og ansøgninger.
author: hachandr
manager: AnnBe
ms.date: 03/18/2019
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
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 8860f508eebc377042c4e101eeb08a14a737ba0c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460673"
---
# <a name="track-candidate-sources-in-attract"></a><span data-ttu-id="e3c5e-103">Spor kandidatkilder i Attract</span><span class="sxs-lookup"><span data-stu-id="e3c5e-103">Track candidate sources in Attract</span></span>

[!include [banner](includes/banner.md)]

> [!NOTE] 
> <span data-ttu-id="e3c5e-104">De funktioner, der er angivet under dette emne, er tilgængelige som en del af en gennemgang af en eksempelversion.</span><span class="sxs-lookup"><span data-stu-id="e3c5e-104">Functionality noted in this topic is available as part of a preview review release.</span></span> <span data-ttu-id="e3c5e-105">Indholdet og funktionaliteten kan blive ændret.</span><span class="sxs-lookup"><span data-stu-id="e3c5e-105">The content and the functionality are subject to change.</span></span> <span data-ttu-id="e3c5e-106">For at anvende denne funktion skal du anmode en administrator om at aktivere den ved hjælp af **Administratorindstillinger** i Attract.</span><span class="sxs-lookup"><span data-stu-id="e3c5e-106">To use this feature, ask an administrator to enable it using the **Admin settings** in Attract.</span></span> <span data-ttu-id="e3c5e-107">I en kommende udgivelse stilles kildesporingsrapporter til rådighed.</span><span class="sxs-lookup"><span data-stu-id="e3c5e-107">A future release will provide source tracking reports.</span></span> <span data-ttu-id="e3c5e-108">Du kan finde yderligere oplysninger under [Få adgang til funktioner i prøveversioner af Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span><span class="sxs-lookup"><span data-stu-id="e3c5e-108">For more information, see [Access preview features in Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

<span data-ttu-id="e3c5e-109">Når en kandidat søger et job, sporer Attract automatisk kilden til dennes ansøgninger og giver dig værdifulde oplysninger, der kan hjælpe dig med at målrette din rekrutteringsindsats.</span><span class="sxs-lookup"><span data-stu-id="e3c5e-109">When candidates apply for a job, Attract automatically tracks the source of their applications, providing you with valuable information to help you target your recruiting efforts.</span></span> <span data-ttu-id="e3c5e-110">Rekrutteringsmedarbejdere og ansættelsesansvarlige kan endvidere vælge en ansøgningskilde, når de manuelt tilføjer en kandidat til et job eller en talentpulje.</span><span class="sxs-lookup"><span data-stu-id="e3c5e-110">Recruiters and hiring managers can also select an application source while manually adding a candidate to a job or talent pool.</span></span>

<span data-ttu-id="e3c5e-111">Du kan se ansøgningskilden i detaljerne om ansøgningsaktivitet under fanen **Aktivitet** samt i ansøgningshistorikken, der er tilgængelig under **Profil** i talentpuljer.</span><span class="sxs-lookup"><span data-stu-id="e3c5e-111">You can view the application source in the application activity details under the **Activity** tab, as well as in the application history available under **Profile** in talent pools.</span></span> <span data-ttu-id="e3c5e-112">Du kan finde en kandidats profilkilde i kandidatens detaljer under fanen **Profil** i både ansøgninger og talentpuljer.</span><span class="sxs-lookup"><span data-stu-id="e3c5e-112">You can find a candidate's profile source in the candidate details under the **Profile** tab in both applications and talent pools.</span></span>

> [!NOTE] 
> <span data-ttu-id="e3c5e-113">Du kan finde processkabeloner i [Tilføjelsesprogrammet Omfattende ansættelser](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span><span class="sxs-lookup"><span data-stu-id="e3c5e-113">You can find process templates in the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>

## <a name="pre-configured-sources"></a><span data-ttu-id="e3c5e-114">Forudkonfigurerede kilder</span><span class="sxs-lookup"><span data-stu-id="e3c5e-114">Pre-configured sources</span></span>

<span data-ttu-id="e3c5e-115">Standardkildelisten omfatter fælles ansøgningskilder.</span><span class="sxs-lookup"><span data-stu-id="e3c5e-115">The default source list contains common application sources.</span></span> <span data-ttu-id="e3c5e-116">Visse kildetyper såsom **Jobportal** og **Socialt netværk** har yderligere kildedetaljer.</span><span class="sxs-lookup"><span data-stu-id="e3c5e-116">Some source types, like **Job board** and **Social Network**, have additional source details.</span></span> <span data-ttu-id="e3c5e-117">Eksempelvis omfatter **Socialt netværk** Facebook og Twitter.</span><span class="sxs-lookup"><span data-stu-id="e3c5e-117">For example, **Social Network** includes Facebook and Twitter.</span></span> <span data-ttu-id="e3c5e-118">Kildetypen **Henvisning** gør det muligt for dig at angive en intern medarbejder som reference.</span><span class="sxs-lookup"><span data-stu-id="e3c5e-118">The **Referral** source type allows you to specify an internal employee as the referrer.</span></span> <span data-ttu-id="e3c5e-119">Standardkildelisten omfatter følgende forudkonfigurerede kilder:</span><span class="sxs-lookup"><span data-stu-id="e3c5e-119">The default source list includes the following pre-configured sources:</span></span>

-   <span data-ttu-id="e3c5e-120">Attract's karrierewebsted</span><span class="sxs-lookup"><span data-stu-id="e3c5e-120">Attract career site</span></span>

-   <span data-ttu-id="e3c5e-121">Forvaltning</span><span class="sxs-lookup"><span data-stu-id="e3c5e-121">Agency</span></span>

-   <span data-ttu-id="e3c5e-122">Karrieremesse</span><span class="sxs-lookup"><span data-stu-id="e3c5e-122">Career Fair</span></span>

-   <span data-ttu-id="e3c5e-123">Virksomhedens markedsføring</span><span class="sxs-lookup"><span data-stu-id="e3c5e-123">Company Marketing</span></span>

-   <span data-ttu-id="e3c5e-124">Konferencer og messer</span><span class="sxs-lookup"><span data-stu-id="e3c5e-124">Conferences & Trade shows</span></span>

-   <span data-ttu-id="e3c5e-125">Professionel tilknytning</span><span class="sxs-lookup"><span data-stu-id="e3c5e-125">Professional Association</span></span>

-   <span data-ttu-id="e3c5e-126">Jobportal</span><span class="sxs-lookup"><span data-stu-id="e3c5e-126">Job board</span></span>

    -   <span data-ttu-id="e3c5e-127">Indeed</span><span class="sxs-lookup"><span data-stu-id="e3c5e-127">Indeed</span></span>

    -   <span data-ttu-id="e3c5e-128">Seek</span><span class="sxs-lookup"><span data-stu-id="e3c5e-128">Seek</span></span>

    -   <span data-ttu-id="e3c5e-129">CareerBuilder</span><span class="sxs-lookup"><span data-stu-id="e3c5e-129">CareerBuilder</span></span>

    -   <span data-ttu-id="e3c5e-130">Google Jobs</span><span class="sxs-lookup"><span data-stu-id="e3c5e-130">Google Jobs</span></span>

    -   <span data-ttu-id="e3c5e-131">Xing</span><span class="sxs-lookup"><span data-stu-id="e3c5e-131">Xing</span></span>

    -   <span data-ttu-id="e3c5e-132">Glassdoor</span><span class="sxs-lookup"><span data-stu-id="e3c5e-132">Glassdoor</span></span>

    -   <span data-ttu-id="e3c5e-133">Monster Jobs</span><span class="sxs-lookup"><span data-stu-id="e3c5e-133">Monster Jobs</span></span>

-   <span data-ttu-id="e3c5e-134">Magasiner og publikationer</span><span class="sxs-lookup"><span data-stu-id="e3c5e-134">Magazines & Publications</span></span>

-   <span data-ttu-id="e3c5e-135">Socialt netværk</span><span class="sxs-lookup"><span data-stu-id="e3c5e-135">Social Network</span></span>

    -   <span data-ttu-id="e3c5e-136">Facebook</span><span class="sxs-lookup"><span data-stu-id="e3c5e-136">Facebook</span></span>

    -   <span data-ttu-id="e3c5e-137">Twitter</span><span class="sxs-lookup"><span data-stu-id="e3c5e-137">Twitter</span></span>

-   <span data-ttu-id="e3c5e-138">Universitetsrekruttering</span><span class="sxs-lookup"><span data-stu-id="e3c5e-138">University Recruiting</span></span>

-   <span data-ttu-id="e3c5e-139">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="e3c5e-139">LinkedIn</span></span>

-   <span data-ttu-id="e3c5e-140">Annoncer</span><span class="sxs-lookup"><span data-stu-id="e3c5e-140">Classifieds</span></span>

-   <span data-ttu-id="e3c5e-141">Henvisning</span><span class="sxs-lookup"><span data-stu-id="e3c5e-141">Referral</span></span>

-   <span data-ttu-id="e3c5e-142">Tilføjet af rekrutteringsmedarbejder</span><span class="sxs-lookup"><span data-stu-id="e3c5e-142">Added by Recruiter</span></span>

-   <span data-ttu-id="e3c5e-143">Diverse</span><span class="sxs-lookup"><span data-stu-id="e3c5e-143">Other</span></span>

## <a name="customize-the-source-list"></a><span data-ttu-id="e3c5e-144">Tilpas kildelisten</span><span class="sxs-lookup"><span data-stu-id="e3c5e-144">Customize the source list</span></span> 

<span data-ttu-id="e3c5e-145">Du kan udvide kildelisten til at omfatte yderligere ansøgningskilder.</span><span class="sxs-lookup"><span data-stu-id="e3c5e-145">You can extend the source list to include additional application sources.</span></span> <span data-ttu-id="e3c5e-146">For at tilpasse denne liste skal du følge vejledningen i [Udvidede indstillingssæt i Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/extensibility-attract#extending-option-sets-in-attract).</span><span class="sxs-lookup"><span data-stu-id="e3c5e-146">To customize this list, follow the instructions in [Extending Option Sets in Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/extensibility-attract#extending-option-sets-in-attract).</span></span> <span data-ttu-id="e3c5e-147">Rediger enheden **TalentKilde** for at omfatte yderligere kilder.</span><span class="sxs-lookup"><span data-stu-id="e3c5e-147">Edit the **TalentSource** entity to include additional sources.</span></span> 

<span data-ttu-id="e3c5e-148">For at undgå at brugergrænsefladen (UI) påvirkes negativt, må du ikke redigere eller slette **TalentKategori**-enum-værdierne (undtagen navne) for følgende:</span><span class="sxs-lookup"><span data-stu-id="e3c5e-148">To avoid negatively impacting the user interface (UI), don't edit or delete the **TalentCategory** enum values (not names) for the following:</span></span>

- <span data-ttu-id="e3c5e-149">**Henvisning**</span><span class="sxs-lookup"><span data-stu-id="e3c5e-149">**Referral**</span></span>
- <span data-ttu-id="e3c5e-150">**LinkedIn**</span><span class="sxs-lookup"><span data-stu-id="e3c5e-150">**LinkedIn**</span></span>
- <span data-ttu-id="e3c5e-151">**Diverse**</span><span class="sxs-lookup"><span data-stu-id="e3c5e-151">**Other**</span></span>

<span data-ttu-id="e3c5e-152">Du kan i stedet udvide **TalentKilde**-enum for at tilføje andre kildetyper.</span><span class="sxs-lookup"><span data-stu-id="e3c5e-152">Instead, you can extend the **TalentSource** enum to add other types of sources.</span></span>
