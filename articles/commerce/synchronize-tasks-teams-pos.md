---
title: Synkronisere opgavestyring mellem Microsoft Teams og Dynamics 365 Commerce POS
description: Dette emne beskriver, hvordan opgavestyring synkroniseres mellem Microsoft Teams og Dynamics 365 Commerce POS.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 74d53a850113c83979fba6baa4ff3c3e5d9ca02d
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020621"
---
# <a name="synchronize-task-management-between-microsoft-teams-and-dynamics-365-commerce-pos"></a><span data-ttu-id="93b7e-103">Synkronisere opgavestyring mellem Microsoft Teams og Dynamics 365 Commerce POS</span><span class="sxs-lookup"><span data-stu-id="93b7e-103">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="93b7e-104">Dette emne beskriver, hvordan opgavestyring synkroniseres mellem Microsoft Teams og Dynamics 365 Commerce POS.</span><span class="sxs-lookup"><span data-stu-id="93b7e-104">This topic describes how to synchronize task management between Microsoft Teams and Dynamics 365 Commerce point of sale (POS).</span></span>

<span data-ttu-id="93b7e-105">Et af de væsentligste formål med Teams-integration er at aktivere synkronisering af opgavestyring mellem POS-programmet og Teams.</span><span class="sxs-lookup"><span data-stu-id="93b7e-105">One of the main purposes of Teams integration is to enable the synchronization of task management between the POS application and Teams.</span></span> <span data-ttu-id="93b7e-106">På den måde kan butiksansatte enten bruge POS-programmet eller Teams til at administrere opgaver og behøver ikke skifte program.</span><span class="sxs-lookup"><span data-stu-id="93b7e-106">In this way, store employees can use either the POS application or Teams to manage tasks, and don't have to switch applications.</span></span>

<span data-ttu-id="93b7e-107">Da Planner bruges som lager for opgaver i Teams, skal der være et link mellem Teams og Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="93b7e-107">Because Planner is used as a repository for tasks in Teams, there must be a link between Teams and Dynamics 365 Commerce.</span></span> <span data-ttu-id="93b7e-108">Dette link oprettes ved hjælp af et bestemt plan-id for et bestemt butiksteam.</span><span class="sxs-lookup"><span data-stu-id="93b7e-108">This link is established by using a specific plan ID for a given store team.</span></span>

<span data-ttu-id="93b7e-109">Følgende procedurer viser, hvordan du kan konfigurere synkronisering af opgavestyring mellem POS- og Teams-applikationerne.</span><span class="sxs-lookup"><span data-stu-id="93b7e-109">The following procedures show how to set up task management synchronization between the POS and Teams applications.</span></span>

## <a name="publish-a-test-task-list-in-teams"></a><span data-ttu-id="93b7e-110">Publicere en testopgaveliste i Teams</span><span class="sxs-lookup"><span data-stu-id="93b7e-110">Publish a test task list in Teams</span></span>

<span data-ttu-id="93b7e-111">I følgende procedure antages det, at butiksteamene bruger integration af Microsoft Teams-opgavestyring med Commerce for første gang.</span><span class="sxs-lookup"><span data-stu-id="93b7e-111">The following procedure assumes that your store teams are using Microsoft Teams task management integration with Commerce for the first time.</span></span>

<span data-ttu-id="93b7e-112">Hvis du vil publicere en testopgaveliste i Teams, skal du udføre disse trin.</span><span class="sxs-lookup"><span data-stu-id="93b7e-112">To publish a test task list in Teams, follow these steps.</span></span>

1. <span data-ttu-id="93b7e-113">Log på Teams som kommunikationschef.</span><span class="sxs-lookup"><span data-stu-id="93b7e-113">Sign in to Teams as a communications manager.</span></span> <span data-ttu-id="93b7e-114">Kommunikationschefer er typisk brugere, der har rollen **Regionschef** i Commerce.</span><span class="sxs-lookup"><span data-stu-id="93b7e-114">Typically, communications managers are users who have the **Regional manager** role in Commerce.</span></span>
1. <span data-ttu-id="93b7e-115">Vælg **Opgaver efter planlægning** i den venstre navigationsrude.</span><span class="sxs-lookup"><span data-stu-id="93b7e-115">In the left navigation pane, select **Tasks by Planner**.</span></span>
1. <span data-ttu-id="93b7e-116">Under fanen **Publicerede lister** skal du vælge **Ny liste** nederst til venstre og navngive den nye liste **Testopgaveliste**.</span><span class="sxs-lookup"><span data-stu-id="93b7e-116">On the **Published lists** tab, select **New list** in the lower left, and name the new list **Test task list**.</span></span>
1. <span data-ttu-id="93b7e-117">Vælg **Opret**.</span><span class="sxs-lookup"><span data-stu-id="93b7e-117">Select **Create**.</span></span> <span data-ttu-id="93b7e-118">Den nye liste vises under **Kladder**.</span><span class="sxs-lookup"><span data-stu-id="93b7e-118">The new list appears under **Drafts**.</span></span>
1. <span data-ttu-id="93b7e-119">Giv den første opgave titlen **Test af Teams-integration** under **Opgavetitel**.</span><span class="sxs-lookup"><span data-stu-id="93b7e-119">Under **Task title**, give the first task the title **Testing Teams integration**.</span></span> <span data-ttu-id="93b7e-120">Vælg derefter **Angiv**.</span><span class="sxs-lookup"><span data-stu-id="93b7e-120">Then select **Enter**.</span></span>
1. <span data-ttu-id="93b7e-121">Vælg opgavelisten på listen **Kladder**.</span><span class="sxs-lookup"><span data-stu-id="93b7e-121">In the **Drafts** list, select the task list.</span></span> <span data-ttu-id="93b7e-122">Vælg derefter **Publicer** i øverste højre hjørne.</span><span class="sxs-lookup"><span data-stu-id="93b7e-122">Then select **Publish** in the upper-right corner.</span></span>
1. <span data-ttu-id="93b7e-123">Vælg de teams, der skal modtage testopgavelisten, i dialogboksen **Vælg, hvem der skal publiceres til**.</span><span class="sxs-lookup"><span data-stu-id="93b7e-123">In the **Select who to publish to** dialog box, select the teams that should receive the test task list.</span></span>
1. <span data-ttu-id="93b7e-124">Vælg **Næste** for at gennemse publikationsplanen.</span><span class="sxs-lookup"><span data-stu-id="93b7e-124">Select **Next** to review your publication plan.</span></span> <span data-ttu-id="93b7e-125">Hvis du skal foretage ændringer, skal du vælge **Tilbage**.</span><span class="sxs-lookup"><span data-stu-id="93b7e-125">If you must make changes, select **Back**.</span></span> 
1. <span data-ttu-id="93b7e-126">Vælg **Bekræft, at du vil fortsætte**, og vælg derefter **Publicer**.</span><span class="sxs-lookup"><span data-stu-id="93b7e-126">Select **Confirm to proceed**, and then select **Publish**.</span></span>
1. <span data-ttu-id="93b7e-127">Når publiceringen er fuldført, angiver en meddelelse øverst under fanen **Publicerede lister**, om opgavelisten er blevet leveret.</span><span class="sxs-lookup"><span data-stu-id="93b7e-127">After publishing is completed, a message at the top of the **Published lists** tab indicates whether your task list was successfully delivered.</span></span>

<span data-ttu-id="93b7e-128">Du kan finde flere oplysninger i [Publicere opgavelister for at oprette og spore arbejde i organisationen](https://support.microsoft.com/office/publish-task-lists-to-create-and-track-work-in-your-organization-095409b3-f5af-40aa-9f9e-339b54e705df).</span><span class="sxs-lookup"><span data-stu-id="93b7e-128">For more information, see [Publish task lists to create and track work in your organization](https://support.microsoft.com/office/publish-task-lists-to-create-and-track-work-in-your-organization-095409b3-f5af-40aa-9f9e-339b54e705df).</span></span>

## <a name="link-pos-and-teams-for-task-management"></a><span data-ttu-id="93b7e-129">Forbinde POS og Teams til opgavestyring</span><span class="sxs-lookup"><span data-stu-id="93b7e-129">Link POS and Teams for task management</span></span>

<span data-ttu-id="93b7e-130">Benyt følgende fremgangsmåde for at sammenkæde POS- og Microsoft Teams-programmer til opgavestyring i Commerce-hovedkontoret.</span><span class="sxs-lookup"><span data-stu-id="93b7e-130">To link the POS and Microsoft Teams applications for task management in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="93b7e-131">Gå til **Retail og Commerce \> Opgavestyring \> Opgaveintegration med Microsoft Teams**.</span><span class="sxs-lookup"><span data-stu-id="93b7e-131">Go to **Retail and Commerce \> Task management \> Tasks integration with Microsoft Teams**.</span></span>
1. <span data-ttu-id="93b7e-132">Vælg **Rediger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="93b7e-132">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="93b7e-133">Indstil **Aktivér integration af opgavestyring** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="93b7e-133">Set the **Enable Task Management Integration** option to **Yes**.</span></span>
1. <span data-ttu-id="93b7e-134">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="93b7e-134">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="93b7e-135">Vælg **Konfigurer opgavestyring** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="93b7e-135">On the Action Pane, select **Setup task management**.</span></span> <span data-ttu-id="93b7e-136">Du skal modtage en besked om, at der oprettes et batchjob med navnet **Teams-klargøring**.</span><span class="sxs-lookup"><span data-stu-id="93b7e-136">You should receive a notification that indicates that a batch job that is named **Teams provision** is being created.</span></span>
1. <span data-ttu-id="93b7e-137">Gå til **Systemadministration \> Forespørgsler \> Batchjob**, og find det seneste job, der indeholder beskrivelsen **Teams-klargøring**.</span><span class="sxs-lookup"><span data-stu-id="93b7e-137">Go to **System administration \> Inquiries \> Batch jobs**, and find the most recent job that has the description **Teams provision**.</span></span> <span data-ttu-id="93b7e-138">Vent, indtil jobbet er kørt færdig.</span><span class="sxs-lookup"><span data-stu-id="93b7e-138">Wait until this job has finished running.</span></span>
1. <span data-ttu-id="93b7e-139">Kør **CDX-job 1070** for at publicere plan-id'et og butiksreferencerne til Retail Server.</span><span class="sxs-lookup"><span data-stu-id="93b7e-139">Run the **CDX job 1070** to publish the plan ID and store references to Retail Server.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="93b7e-140">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="93b7e-140">Additional resources</span></span>

[<span data-ttu-id="93b7e-141">Oversigt over Dynamics 365 Commerce- og Microsoft Teams-integration</span><span class="sxs-lookup"><span data-stu-id="93b7e-141">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="93b7e-142">Aktivere Dynamics 365 Commerce- og Microsoft Teams-integration</span><span class="sxs-lookup"><span data-stu-id="93b7e-142">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="93b7e-143">Klargøre Microsoft Teams fra Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="93b7e-143">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="93b7e-144">Administrere brugerroller i Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="93b7e-144">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="93b7e-145">Tilknytte butikker og teams, hvis der er eksisterende teams i Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="93b7e-145">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="93b7e-146">Ofte stillede spørgsmål til Dynamics 365 Commerce- og Microsoft Teams-integration</span><span class="sxs-lookup"><span data-stu-id="93b7e-146">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
