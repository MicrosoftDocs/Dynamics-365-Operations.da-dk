---
title: Opret et nyt projekt
description: Dette emne indeholder oplysninger om, hvordan du opretter et nyt projekt.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c8c52b8c1c86ea2f6e03cf439ba5930f1006ab4f
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760503"
---
# <a name="create-a-new-project"></a><span data-ttu-id="a45e3-103">Opret et nyt projekt</span><span class="sxs-lookup"><span data-stu-id="a45e3-103">Create a new project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a45e3-104">Udfør følgende trin for at oprette et nyt projekt.</span><span class="sxs-lookup"><span data-stu-id="a45e3-104">Complete the following steps to create a new project.</span></span>

1. <span data-ttu-id="a45e3-105">På siden **Projektstyring** skal du vælge **Nyt projekt** og angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="a45e3-105">On the **Project management** page, select **New project**, and enter the following values:</span></span>

    - <span data-ttu-id="a45e3-106">**Projekttype:** Tid og materialer</span><span class="sxs-lookup"><span data-stu-id="a45e3-106">**Project type:** Time and material</span></span>
    - <span data-ttu-id="a45e3-107">**Projektnavn:** XYZ-opgradering fase 2</span><span class="sxs-lookup"><span data-stu-id="a45e3-107">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="a45e3-108">**Projektgruppe:** TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="a45e3-108">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="a45e3-109">**Projektkontrakt-id:** 00000002</span><span class="sxs-lookup"><span data-stu-id="a45e3-109">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="a45e3-110">Vælg **Opret projekt**.</span><span class="sxs-lookup"><span data-stu-id="a45e3-110">Select **Create project**.</span></span>

## <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="a45e3-111">Tildel en ressource til et projekt</span><span class="sxs-lookup"><span data-stu-id="a45e3-111">Assign a resource to a project</span></span>

1. <span data-ttu-id="a45e3-112">På siden **Arbejdere** på listen **Arbejdere** skal du vælge posten for den arbejder, som du tidligere har konfigureret kompetencer for, og åbne arbejderposten.</span><span class="sxs-lookup"><span data-stu-id="a45e3-112">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="a45e3-113">Vælg **Tildel projekter** i gruppen **Konfiguration** under fanen **Projekt** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="a45e3-113">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="a45e3-114">På siden **Ressourcevalidering af projekttildelinger** under fanen **Projekter** skal du i feltet **Føj projektet til udvalgte projekter** filtrere på projektet **XYZ-opgradering fase 2**.</span><span class="sxs-lookup"><span data-stu-id="a45e3-114">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="a45e3-115">I ruden **Resterende projekter** skal du vælge et projekt og derefter vælge pileknappen for at føje det til ruden **Valgte projekter**.</span><span class="sxs-lookup"><span data-stu-id="a45e3-115">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="a45e3-116">Du kan også tildele kategorier til en ressource, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="a45e3-116">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="a45e3-117">Kategoritypen er enten **Omkostning** eller **Indtægter**.</span><span class="sxs-lookup"><span data-stu-id="a45e3-117">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="a45e3-118">Kategoritypen bestemmes af din organisation.</span><span class="sxs-lookup"><span data-stu-id="a45e3-118">The category type is determined by your organization.</span></span> <span data-ttu-id="a45e3-119">Hvis en ressource ikke er tildelt nogen kategorier, leder Finance efter standardkategorien på timepriser for omkostninger og indtægter.</span><span class="sxs-lookup"><span data-stu-id="a45e3-119">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

## <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="a45e3-120">Konfigurere projektressource- og rollekarakteristika</span><span class="sxs-lookup"><span data-stu-id="a45e3-120">Set up project resource and role characteristics</span></span>

<span data-ttu-id="a45e3-121">En projektleder kan bruge projektressourcefunktionaliteten til at oprette de roller, der er nødvendige for projektet.</span><span class="sxs-lookup"><span data-stu-id="a45e3-121">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="a45e3-122">Roller kan bruges, hvis bekræftede ressourcer stadig er ukendte, når ressourcer reserveres.</span><span class="sxs-lookup"><span data-stu-id="a45e3-122">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="a45e3-123">Roller kan midlertidigt reserveres som planlagte ressourcer, så du kan fortsætte med projektplanlægningsfaserne.</span><span class="sxs-lookup"><span data-stu-id="a45e3-123">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="a45e3-124">[![Eksempel på en rolle](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="a45e3-124">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="a45e3-125">**Scenarie:** Contoso blev ansat til at udføre et tids- og materialeprojekt, der har et godkendt projektcharter.</span><span class="sxs-lookup"><span data-stu-id="a45e3-125">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="a45e3-126">Juniorprojektlederen er stadig ved at færdiggøre omfanget af projektet.</span><span class="sxs-lookup"><span data-stu-id="a45e3-126">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="a45e3-127">Ressourcestyringen identificerer i øjeblikket bestemte ressourcer, der skal reserveres til arbejde på det nye projekt.</span><span class="sxs-lookup"><span data-stu-id="a45e3-127">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="a45e3-128">På grund af projektets kritiske natur har projektsponsoren anmodet om, at en af rollerne er seniorprojektleder.</span><span class="sxs-lookup"><span data-stu-id="a45e3-128">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="a45e3-129">Ressourcechefen skal anskaffe den nye ressource og definere rollen i systemet i tilfælde af, at juniorprojektlederen kræver ressourceoplysninger under projektplanlægningen.</span><span class="sxs-lookup"><span data-stu-id="a45e3-129">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="a45e3-130">Følgende fremgangsmåde viser, hvordan ressourcechefen kan konfigurere seniorprojektlederrollen og knytte ressourceegenskaber til den.</span><span class="sxs-lookup"><span data-stu-id="a45e3-130">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="a45e3-131">Rollen kan senere bruges til at søge efter tilgængelige ressourcer, der svarer til de krævede ressourcekompetencer.</span><span class="sxs-lookup"><span data-stu-id="a45e3-131">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="a45e3-132">På siden **Konfigurer roller** skal du vælge **Ny** og angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="a45e3-132">On the **Setup roles** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="a45e3-133">**Rolle-id:** Seniorprojektleder</span><span class="sxs-lookup"><span data-stu-id="a45e3-133">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="a45e3-134">**Beskrivelse:** Seniorprojektleder</span><span class="sxs-lookup"><span data-stu-id="a45e3-134">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="a45e3-135">Vælg **Opret**.</span><span class="sxs-lookup"><span data-stu-id="a45e3-135">Select **Create**.</span></span>
3. <span data-ttu-id="a45e3-136">Vælg rollen **Seniorprojektleder**, og vælg derefter **Konfigurer egenskaber**.</span><span class="sxs-lookup"><span data-stu-id="a45e3-136">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="a45e3-137">Vælg **Færdighed** i feltet **Karakteristikatype**.</span><span class="sxs-lookup"><span data-stu-id="a45e3-137">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="a45e3-138">I feltet **Tilgængelige karakteristika** skal du angive den færdighed, du søger efter.</span><span class="sxs-lookup"><span data-stu-id="a45e3-138">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="a45e3-139">I **Karakteristikatype** feltet skal du vælge **Certifikat**.</span><span class="sxs-lookup"><span data-stu-id="a45e3-139">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="a45e3-140">I feltet **Tilgængelige karakteristika** skal du angive den certifikattype, du søger efter.</span><span class="sxs-lookup"><span data-stu-id="a45e3-140">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

## <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="a45e3-141">Tildele en projektressource til et projekt</span><span class="sxs-lookup"><span data-stu-id="a45e3-141">Assign a project resource to a project</span></span>

1. <span data-ttu-id="a45e3-142">På siden **Alle projekter** skal du vælge projektet **XYZ-opgradering fase 2**.</span><span class="sxs-lookup"><span data-stu-id="a45e3-142">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="a45e3-143">Under fanen **Projektteam og planlægning** skal vælge **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="a45e3-143">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="a45e3-144">I feltet **Rolle** skal du vælge **Teammedlem**.</span><span class="sxs-lookup"><span data-stu-id="a45e3-144">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="a45e3-145">Vælg **Reservér fra kalender**.</span><span class="sxs-lookup"><span data-stu-id="a45e3-145">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="a45e3-146">På siden **Ressourcetilgængelighed** skal du vælge **Vis indstillinger**.</span><span class="sxs-lookup"><span data-stu-id="a45e3-146">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="a45e3-147">På siden **Juster visningsindstillinger** skal du angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="a45e3-147">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="a45e3-148">**Viser format for datoområde:** Dag</span><span class="sxs-lookup"><span data-stu-id="a45e3-148">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="a45e3-149">**Vis beskrivelser af tilgængelighed:** Ja</span><span class="sxs-lookup"><span data-stu-id="a45e3-149">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="a45e3-150">**Vis resterende kapacitet:** Ja</span><span class="sxs-lookup"><span data-stu-id="a45e3-150">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="a45e3-151">Vælg en ressource på listen over ressourcer.</span><span class="sxs-lookup"><span data-stu-id="a45e3-151">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="a45e3-152">Vælg **Definitiv reservation** og **Fuld kapacitet**.</span><span class="sxs-lookup"><span data-stu-id="a45e3-152">Select **Hard book** and **Full capacity**.</span></span>

## <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="a45e3-153">Tildele en ressource til en standardrolle</span><span class="sxs-lookup"><span data-stu-id="a45e3-153">Assign a resource to a default role</span></span>

<span data-ttu-id="a45e3-154">Som en hjælp kan projektledere eller ressourcechefer rulle længere ned i de ressourcer, der kan reserveres til et projekt.</span><span class="sxs-lookup"><span data-stu-id="a45e3-154">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="a45e3-155">Du kan knytte en standardrolle til en eksisterende ressource eller en nyligt erhvervet ressource.</span><span class="sxs-lookup"><span data-stu-id="a45e3-155">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="a45e3-156">Da Daniel f.eks. blev ansat, havde han erfaring og kompetence til at udfylde rollen Forretningsanalytiker.</span><span class="sxs-lookup"><span data-stu-id="a45e3-156">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="a45e3-157">Ressourcechefen tildelte denne rolle som Daniels standardrolle.</span><span class="sxs-lookup"><span data-stu-id="a45e3-157">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="a45e3-158">Derfor tilføjede ressourcechefen Daniel til en pulje af forretningsanalytikere, der er tilgængelige til at arbejde på projekter.</span><span class="sxs-lookup"><span data-stu-id="a45e3-158">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="a45e3-159">Under ressourcereservationen kan projektledere filtrere de ressourceroller, der er tilgængelige for arbejde på projekter.</span><span class="sxs-lookup"><span data-stu-id="a45e3-159">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="a45e3-160">De kan bruge disse oplysninger som et kriterium, når de foretager beslutningsanalyse med flere kriterier under ressourceopfyldelsen.</span><span class="sxs-lookup"><span data-stu-id="a45e3-160">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="a45e3-161">De kan også føje andre ressourcekarakteristika til filteret for at søge efter ressourcer, som har særlige kvalifikationer, uddannelse og erfaringer med et givent projekt.</span><span class="sxs-lookup"><span data-stu-id="a45e3-161">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="a45e3-162">**Scenarie:** Et godkendt projekt er startet, og rollen som seniorprojektleder blev reserveret som en planlagt ressource i løbet af projektets planlægningsstadie.</span><span class="sxs-lookup"><span data-stu-id="a45e3-162">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="a45e3-163">Ressourcestyringen har nu fået en ressource, der skal opfylde rollen som seniorprojektleder.</span><span class="sxs-lookup"><span data-stu-id="a45e3-163">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="a45e3-164">Vælg **Daniel Goldschmidt** på siden **Liste over ressourcer**.</span><span class="sxs-lookup"><span data-stu-id="a45e3-164">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="a45e3-165">På siden **Ressourcerolle** skal du vælge **Ny** og angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="a45e3-165">On the **Resource role** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="a45e3-166">**Gyldig fra:** Angiv den aktuelle dato.</span><span class="sxs-lookup"><span data-stu-id="a45e3-166">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="a45e3-167">**Udløb:** Angiv **Aldrig**.</span><span class="sxs-lookup"><span data-stu-id="a45e3-167">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="a45e3-168">**Rolle:** Angiv **Seniorprojektleder**.</span><span class="sxs-lookup"><span data-stu-id="a45e3-168">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="a45e3-169">Vælg **Gem**, og luk derefter siden.</span><span class="sxs-lookup"><span data-stu-id="a45e3-169">Select **Save**, and then close the page.</span></span>
4. <span data-ttu-id="a45e3-170">Under fanen **Kompetencer** skal du tilføje færdigheden **ProjectMgmt** og **PMP**-certifikatet.</span><span class="sxs-lookup"><span data-stu-id="a45e3-170">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>
