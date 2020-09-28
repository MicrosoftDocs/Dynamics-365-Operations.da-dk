---
title: Konfigurere projektressourcer
description: Dette emne giver oplysninger om opsætning eller anmodning om projektressourcer.
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
ms.openlocfilehash: c882e23794e3937f85b3e73774b36deaf28ac3ed
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760508"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="30918-103">Konfigurere projektressourcer</span><span class="sxs-lookup"><span data-stu-id="30918-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="30918-104">Du skal oprette en kalender og knytte den til en medarbejder eller en arbejder.</span><span class="sxs-lookup"><span data-stu-id="30918-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="30918-105">Kalenderen bruges til at planlægge projektet og arbejdstiden for de ressourcer, der er reserveret til projektet.</span><span class="sxs-lookup"><span data-stu-id="30918-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="30918-106">Projektledere kan udføre ressourceudjævning som en del af ressourceoptimering, når de konfigurerer kalenderen.</span><span class="sxs-lookup"><span data-stu-id="30918-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="30918-107">Baseret på kalendertidsplanen kan der sættes begrænsninger på ressourcer.</span><span class="sxs-lookup"><span data-stu-id="30918-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="30918-108">Du kan oprette en kalender på siden **Kalendere**.</span><span class="sxs-lookup"><span data-stu-id="30918-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="30918-109">Når du konfigurerer en arbejder som en projektressource, kan du vælge mellem arbejdere, der arbejder i det firma, du konfigurerer ressourcer til.</span><span class="sxs-lookup"><span data-stu-id="30918-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="30918-110">Du kan også vælge arbejdere fra andre firmaer i organisationen.</span><span class="sxs-lookup"><span data-stu-id="30918-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="30918-111">Disse arbejdere kaldes interne ressourcer.</span><span class="sxs-lookup"><span data-stu-id="30918-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="30918-112">Nedenstående fremgangsmåder forklarer, hvordan du konfigurerer en arbejder som en projektressource i virksomheden, og hvordan du opretter en intern projektressource.</span><span class="sxs-lookup"><span data-stu-id="30918-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="30918-113">Konfigurere en arbejder som en projektressource</span><span class="sxs-lookup"><span data-stu-id="30918-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="30918-114">På siden **Arbejdere** på listen **Arbejdere** skal du vælge den arbejder, som du vil tilføje som en projektressource, og åbne arbejderposten.</span><span class="sxs-lookup"><span data-stu-id="30918-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="30918-115">I handlingsruden skal du vælge **Projekt** &gt; **Konfiguration** &gt; **Opsætning af projekt**.</span><span class="sxs-lookup"><span data-stu-id="30918-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="30918-116">Vælg en kalender, og luk derefter siden.</span><span class="sxs-lookup"><span data-stu-id="30918-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="30918-117">Du kan også angive standardprojekter for en ressource som en slags foreløbig tildeling.</span><span class="sxs-lookup"><span data-stu-id="30918-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="30918-118">Foreløbige tildelinger kan bruges, når ressourcestyringen eller projektlederen i forvejen ved, hvilke projekter ressourcen skal arbejde på.</span><span class="sxs-lookup"><span data-stu-id="30918-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="30918-119">Foreløbige tildelinger kan også være baseret på anmodning fra en projektsponsor eller kunde.</span><span class="sxs-lookup"><span data-stu-id="30918-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="30918-120">Når du vil tildele et projekt foreløbigt, skal du vælge det relevante projekt på siden **Tildel projekter** under fanen **Projekter** på listen **Resterende projekter**.</span><span class="sxs-lookup"><span data-stu-id="30918-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="30918-121">Opret en intern ressource</span><span class="sxs-lookup"><span data-stu-id="30918-121">Set up an intercompany resource</span></span>

<span data-ttu-id="30918-122">Når du opretter en arbejder som en intern ressource, skal du fuldføre opsætningen både i firmaet, der udlåner, og i firmaet, der låner.</span><span class="sxs-lookup"><span data-stu-id="30918-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="30918-123">I firmaet, der udlåner</span><span class="sxs-lookup"><span data-stu-id="30918-123">In the lending company</span></span>

1. <span data-ttu-id="30918-124">I Finance skal du kontrollere, at firmaet, der låner, er markeret, og derefter skal du fuldføre proceduren i det forrige afsnit, "Konfigurere en arbejder som en projektressource".</span><span class="sxs-lookup"><span data-stu-id="30918-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="30918-125">På siden **Mellemregning** skal du vælge **Ny**.</span><span class="sxs-lookup"><span data-stu-id="30918-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="30918-126">I feltet **Id for juridisk enhed** skal du vælge firmaet, der udlåner.</span><span class="sxs-lookup"><span data-stu-id="30918-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="30918-127">Udfyld de resterende felter efter behov, og vælg derefter **Gem**.</span><span class="sxs-lookup"><span data-stu-id="30918-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="30918-128">På siden **Intern afregningspris** skal du vælge **Ny**.</span><span class="sxs-lookup"><span data-stu-id="30918-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="30918-129">I feltet **Udlånt til (juridisk enhed)** skal du vælge det relevante firma.</span><span class="sxs-lookup"><span data-stu-id="30918-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="30918-130">Hvis du kun vil låne firmaet, der låner, den ressource, du oprettede i starten af dette afsnit i feltet **Ressource** skal du vælge navnet på den ressource, du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="30918-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="30918-131">Hvis du vil gøre alle ressourcer i firmaet tilgængelige for firmaet, der låner, skal du lade feltet **Ressource** stå tomt.</span><span class="sxs-lookup"><span data-stu-id="30918-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="30918-132">På siden **Parametre for projektstyring og regnskab** under fanen **Intern** skal du angive indstillingen **Aktivér intern ressourceplanlægning og timesedler** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="30918-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="30918-133">I firmaet, der låner</span><span class="sxs-lookup"><span data-stu-id="30918-133">In the borrowing company</span></span>

- <span data-ttu-id="30918-134">På siden **Liste over ressourcer** skal du i søgefiltret angive navnet på den ressource, du oprettede for firmaet, der udlåner, for at kontrollere, at navnet er inkluderet på ressourcelisten for firmaet, der låner.</span><span class="sxs-lookup"><span data-stu-id="30918-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="30918-135">Anmode om projektressourcer</span><span class="sxs-lookup"><span data-stu-id="30918-135">Request project resources</span></span>
<span data-ttu-id="30918-136">Planlægningsfunktionen projektressource giver kun ressourcechefer mulighed for at distribuere bemandingsressourcer på opgaver eller projekter.</span><span class="sxs-lookup"><span data-stu-id="30918-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="30918-137">Udfør følgende opgaver for at aktivere denne funktion, eller kontrollér, at de er blevet fuldført:</span><span class="sxs-lookup"><span data-stu-id="30918-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="30918-138">Konfigurer nummerserier.</span><span class="sxs-lookup"><span data-stu-id="30918-138">Set up number sequences.</span></span>
- <span data-ttu-id="30918-139">Konfigurer arbejdsgange i Projektstyring og regnskab.</span><span class="sxs-lookup"><span data-stu-id="30918-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="30918-140">Aktivér arbejdsgange for ressourceanmodning</span><span class="sxs-lookup"><span data-stu-id="30918-140">Enable resource request workflows.</span></span>

<span data-ttu-id="30918-141">Når de foregående opgaver er fuldført, kan du udføre følgende opgaver efter behov:</span><span class="sxs-lookup"><span data-stu-id="30918-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="30918-142">Opret en ressourceanmodning fra en midlertidigt reserveret bemandingsressource.</span><span class="sxs-lookup"><span data-stu-id="30918-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="30918-143">Overvåg ressourceanmodninger.</span><span class="sxs-lookup"><span data-stu-id="30918-143">Monitor resource requests.</span></span>
- <span data-ttu-id="30918-144">Opfyld ressourceanmodninger.</span><span class="sxs-lookup"><span data-stu-id="30918-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="30918-145">Anmod om en bemandingsressource fra et WBS.</span><span class="sxs-lookup"><span data-stu-id="30918-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="30918-146">Reservér ressourcer til et projekt uden at have en anmodning om en bemandingsressource.</span><span class="sxs-lookup"><span data-stu-id="30918-146">Book resources to a project without having a request for a staffed resource.</span></span>
