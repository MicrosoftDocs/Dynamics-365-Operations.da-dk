---
title: Bruge arbejdsområdet til aktivstyring på mobilenhed
description: Dette emne indeholder oplysninger om arbejdsområdet Styring af aktiver på mobilenheder.
author: josaw1
manager: tfehr
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.dyn365.ops.version: 10.0.5
ms.search.validFrom: 2019-08-31
ms.openlocfilehash: afda807714f14efb1cbab4ecfdd273aac52f4558
ms.sourcegitcommit: 995c678b4715be267f1f97148902a6b3dde3bcab
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/20/2021
ms.locfileid: "5033146"
---
# <a name="use-the-asset-management-mobile-workspace"></a><span data-ttu-id="d7833-103">Bruge arbejdsområdet til aktivstyring på mobilenhed</span><span class="sxs-lookup"><span data-stu-id="d7833-103">Use the Asset management mobile workspace</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d7833-104">Dette emne indeholder oplysninger om arbejdsområdet **Styring af aktiver** på mobilenheder.</span><span class="sxs-lookup"><span data-stu-id="d7833-104">This topic provides information about the **Asset management** mobile workspace.</span></span> <span data-ttu-id="d7833-105">I dette arbejdsområde kan brugerne se og oprette vedligeholdelsesanmodninger og arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="d7833-105">This workspace lets users view and create maintenance requests and work orders.</span></span> <span data-ttu-id="d7833-106">Brugere kan også få vist de tildelte job i arbejdsordrejob i en kalender- eller listevisning.</span><span class="sxs-lookup"><span data-stu-id="d7833-106">Users can also view the assigned work order jobs in a calendar or list view.</span></span> <span data-ttu-id="d7833-107">Aktiver og arbejdssteder kan også ses og søges efter.</span><span class="sxs-lookup"><span data-stu-id="d7833-107">Assets and functional locations can also be viewed and searched for.</span></span>

## <a name="overview"></a><span data-ttu-id="d7833-108">Overblik</span><span class="sxs-lookup"><span data-stu-id="d7833-108">Overview</span></span>

<span data-ttu-id="d7833-109">Styring af aktiver er et avanceret modul til administration af aktiver og arbejdsordrejob i Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d7833-109">Asset Management is an advanced module for managing assets and work order jobs in Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="d7833-110">Med arbejdsområdet **Styring af aktiver** på mobilenheder kan brugerne hurtigt få vist arbejdsordrejob på en mobilenhed efter eget valg.</span><span class="sxs-lookup"><span data-stu-id="d7833-110">The **Asset management** mobile workspace lets users quickly view assigned work order jobs on the mobile device of their choice.</span></span> <span data-ttu-id="d7833-111">Brugerne kan også oprette og administrere vedligeholdelsesanmodninger, opdatere livscyklustilstand og se detaljer om aktiver og arbejdssted ved hjælp af deres mobilenhed.</span><span class="sxs-lookup"><span data-stu-id="d7833-111">Users can also create and manage maintenance requests, update lifecycle state, and view asset and functional location details by using their mobile device.</span></span>

<span data-ttu-id="d7833-112">Med arbejdsområdet **Styring af aktiver** på mobilenheder kan brugerne udføre disse opgaver:</span><span class="sxs-lookup"><span data-stu-id="d7833-112">Specifically, the **Asset management** mobile workspace lets users perform these tasks:</span></span>

- <span data-ttu-id="d7833-113">Oprette, få vist og redigere vedligeholdelsesanmodninger, tage et billede eller vedhæfte et eksisterende billede til vedligeholdelsesanmodningen, ændre livscyklustilstanden for vedligeholdelsesanmodningen.</span><span class="sxs-lookup"><span data-stu-id="d7833-113">Create, view, and edit maintenance requests, take a photo or attach an existing image to the maintenance request, change the maintenance request lifecycle state.</span></span> 
- <span data-ttu-id="d7833-114">Oprette, få vist og redigere arbejdsordrer, tage et billede eller vedhæfte et eksisterende billede til arbejdsordren, ændre livscyklustilstanden for arbejdsordren, få vist arbejdsordrejob.</span><span class="sxs-lookup"><span data-stu-id="d7833-114">Create, view, and edit work orders, take a photo or attach an existing image to the work order, change the work order lifecycle state, view work order jobs.</span></span>
- <span data-ttu-id="d7833-115">Få vist tildelte arbejdsordrejob i en kalendervisning.</span><span class="sxs-lookup"><span data-stu-id="d7833-115">View assigned work order jobs in a calendar view.</span></span>
- <span data-ttu-id="d7833-116">Oprette, få vist og redigere arbejdsordrejob, opdatere aktivtællere, få vist vedligeholdelsestjekliste, få vist og redigere notater til arbejdsordrer, få vist de nødvendige værktøjer til arbejdsordrejobbet.</span><span class="sxs-lookup"><span data-stu-id="d7833-116">Create, view, and edit work order job, update asset counters, view maintenance checklist, view and edit work order job notes, view the tools required for the work order job.</span></span>
- <span data-ttu-id="d7833-117">Få vist eller søge efter et bestemt aktiv eller et arbejdssted.</span><span class="sxs-lookup"><span data-stu-id="d7833-117">View or search for a specific asset or functional location.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d7833-118">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="d7833-118">Prerequisites</span></span>

<span data-ttu-id="d7833-119">Før du kan bruge arbejdsområdet **Aktivstyring** til mobilenheder, skal din administrator konfigurere de nødvendige bruger- og arbejderkonti og publicere arbejdsområdet.</span><span class="sxs-lookup"><span data-stu-id="d7833-119">Before you can use the **Asset management** mobile workspace, your admin must set up the required user and worker accounts, and publish the workspace.</span></span> <span data-ttu-id="d7833-120">Du kan finde flere oplysninger [Konfigurere arbejdsområdet til aktivstyring på mobilenhed](set-up-asset-management-mobile.md).</span><span class="sxs-lookup"><span data-stu-id="d7833-120">For more information, see [Set up the Asset management mobile workspace](set-up-asset-management-mobile.md).</span></span>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="d7833-121">Downloade og installere mobilappen</span><span class="sxs-lookup"><span data-stu-id="d7833-121">Download and install the mobile app</span></span>

<span data-ttu-id="d7833-122">Download og installer Dynamics 365 for Unified Operations-mobilappen:</span><span class="sxs-lookup"><span data-stu-id="d7833-122">Download and install the Dynamics 365 for Unified Operations mobile app:</span></span>

- [<span data-ttu-id="d7833-123">Til Android-telefoner</span><span class="sxs-lookup"><span data-stu-id="d7833-123">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
- [<span data-ttu-id="d7833-124">Til iPhones</span><span class="sxs-lookup"><span data-stu-id="d7833-124">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="d7833-125">Log på mobilappen</span><span class="sxs-lookup"><span data-stu-id="d7833-125">Sign in to the mobile app</span></span>

1. <span data-ttu-id="d7833-126">Start appen på din mobilenhed.</span><span class="sxs-lookup"><span data-stu-id="d7833-126">Start the app on your mobile device.</span></span>

1. <span data-ttu-id="d7833-127">Angiv URL-adressen til din Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="d7833-127">Enter your Dynamics 365 URL.</span></span>

1. <span data-ttu-id="d7833-128">Første gang du logger på, bliver du bedt om at angive brugernavn og adgangskode.</span><span class="sxs-lookup"><span data-stu-id="d7833-128">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="d7833-129">Angiv dine legitimationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="d7833-129">Enter your credentials.</span></span>

1. <span data-ttu-id="d7833-130">Når du har logget på, vises de arbejdsområder, der er tilgængelige for din virksomhed.</span><span class="sxs-lookup"><span data-stu-id="d7833-130">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="d7833-131">Bemærk, at hvis systemadministratoren publicerer et nyt arbejdsområde senere, skal du opdatere listen over arbejdsområder til mobilenheder.</span><span class="sxs-lookup"><span data-stu-id="d7833-131">Note that if your system administrator publishes a new workspace later, you'll have to refresh the list of mobile workspaces.</span></span>

    <span data-ttu-id="d7833-132">![Vælg et arbejdsområde](media/am-mobile-01.png "Vælg et arbejdsområde")</span><span class="sxs-lookup"><span data-stu-id="d7833-132">![Select a workspace](media/am-mobile-01.png "Select a workspace")</span></span>

## <a name="view-assigned-work-order-jobs-in-calendar-view"></a><span data-ttu-id="d7833-133">Få vist tildelte arbejdsordrejob i en kalendervisning</span><span class="sxs-lookup"><span data-stu-id="d7833-133">View assigned work order jobs in calendar view</span></span>

1. <span data-ttu-id="d7833-134">På din mobilenhed skal du åbne arbejdsområdet **Styring af aktiver**.</span><span class="sxs-lookup"><span data-stu-id="d7833-134">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="d7833-135">Vælg **Min kalender over arbejdsordrejob**.</span><span class="sxs-lookup"><span data-stu-id="d7833-135">Select **My work order jobs calendar**.</span></span>

1. <span data-ttu-id="d7833-136">Vælg den dato, som du vil have vist arbejdsordrejob for.</span><span class="sxs-lookup"><span data-stu-id="d7833-136">Select the date you want to view work order jobs for.</span></span> <span data-ttu-id="d7833-137">På listen kan du se aktiv-id'et og arbejdssteds-id'et for hvert arbejdsordrejob.</span><span class="sxs-lookup"><span data-stu-id="d7833-137">In the list, you'll see the asset ID and functional location ID for each work order job.</span></span>

1. <span data-ttu-id="d7833-138">Vælg et arbejdsordrejob på listen for at se joboplysninger: oplysninger om aktiv og arbejdssted samt andre navigationslinks for at få vist **vedhæftede filer**, **kontrollister**, **værktøjer**, **aktivtællere**, **notater**, **kladder**.</span><span class="sxs-lookup"><span data-stu-id="d7833-138">Select a work order job in the list to see job details: Asset and functional location details as well as other navigation links to view **Attachments**, **Checklists**, **Tools**, **Asset counters**, **Notes**, **Journals**.</span></span>

    <span data-ttu-id="d7833-139">![Få vist tildelte arbejdsordrejob i en kalendervisning](media/am-mobile-02.png "Få vist tildelte arbejdsordrejob i en kalendervisning")</span><span class="sxs-lookup"><span data-stu-id="d7833-139">![View assigned work order jobs in calendar view](media/am-mobile-02.png "View assigned work order jobs in calendar view")</span></span>

## <a name="create-a-work-order-job"></a><span data-ttu-id="d7833-140">Opret et arbejdsordrejob</span><span class="sxs-lookup"><span data-stu-id="d7833-140">Create a work order job</span></span>

1. <span data-ttu-id="d7833-141">På din mobilenhed skal du åbne arbejdsområdet **Styring af aktiver**.</span><span class="sxs-lookup"><span data-stu-id="d7833-141">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="d7833-142">Vælg **Alle vedligeholdelsesarbejdsordrer**.</span><span class="sxs-lookup"><span data-stu-id="d7833-142">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="d7833-143">Vælg den arbejdsordre, du vil oprette et nyt arbejdsordrejob for.</span><span class="sxs-lookup"><span data-stu-id="d7833-143">Select the work order you want to create a new work order job for.</span></span>

1. <span data-ttu-id="d7833-144">Vælg knappen **Tilføj linje**.</span><span class="sxs-lookup"><span data-stu-id="d7833-144">Select the **Add line** button.</span></span>

1. <span data-ttu-id="d7833-145">Vælg det **aktiv**, du vil oprette et nyt arbejdsordrejob for.</span><span class="sxs-lookup"><span data-stu-id="d7833-145">Select the **Asset** you want to create a work order job for.</span></span>

1. <span data-ttu-id="d7833-146">Vælg **Vedligeholdelsesjobtype**, **Vedligeholdelsesjobtypevariant** og **Fag**.</span><span class="sxs-lookup"><span data-stu-id="d7833-146">Select **Maintenance job type**, **Maintenance job type variant** and **Trade**.</span></span>

1. <span data-ttu-id="d7833-147">Vælg **Udført**.</span><span class="sxs-lookup"><span data-stu-id="d7833-147">Select **Done**.</span></span>

    <span data-ttu-id="d7833-148">![Skærmbilledet Tilføj linje](media/am-mobile-03.png "Skærmbilledet Tilføj linje")</span><span class="sxs-lookup"><span data-stu-id="d7833-148">![The Add line screen](media/am-mobile-03.png "The Add line screen")</span></span>


## <a name="add-attachment-to-a-work-order-job"></a><span data-ttu-id="d7833-149">Føj en vedhæftet fil til et arbejdsordrejob</span><span class="sxs-lookup"><span data-stu-id="d7833-149">Add attachment to a work order job</span></span>

1. <span data-ttu-id="d7833-150">På din mobilenhed skal du åbne arbejdsområdet **Styring af aktiver**.</span><span class="sxs-lookup"><span data-stu-id="d7833-150">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="d7833-151">Vælg **Alle vedligeholdelsesarbejdsordrer**.</span><span class="sxs-lookup"><span data-stu-id="d7833-151">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="d7833-152">Vælg arbejdsordren > arbejdsordrejobbet, du vil føje en vedhæftet fil til.</span><span class="sxs-lookup"><span data-stu-id="d7833-152">Select the work order > work order job you want to add an attachment to.</span></span>
    - <span data-ttu-id="d7833-153">Alternativt kan du også vælge **Min kalender over arbejdsordrejob** eller **Min liste over arbejdsordrejob** på startsiden for at navigere til siden **Oplysninger om arbejdsordrejob**.</span><span class="sxs-lookup"><span data-stu-id="d7833-153">Alternatively, you can also select **My work order jobs calendar** or **My work order jobs list** on the home page to navigate to the **Work order job details** page.</span></span>

1. <span data-ttu-id="d7833-154">Vælg **Vedhæftede filer** på siden **Oplysninger om arbejdsordrejob**.</span><span class="sxs-lookup"><span data-stu-id="d7833-154">Select **Attachments** on the **Work order job details** page.</span></span>

1. <span data-ttu-id="d7833-155">Du vil se eksisterende vedhæftede filer i arbejdsordrejobbet.</span><span class="sxs-lookup"><span data-stu-id="d7833-155">You'll see existing attachments on the work order job.</span></span> <span data-ttu-id="d7833-156">Vælg **Tilføj vedhæftet fil**.</span><span class="sxs-lookup"><span data-stu-id="d7833-156">Select **Add attachment**.</span></span>

1. <span data-ttu-id="d7833-157">Angiv **Navn** og **Notater** for den vedhæftede fil.</span><span class="sxs-lookup"><span data-stu-id="d7833-157">Enter **Name** and **Notes** for the attachment.</span></span>

1. <span data-ttu-id="d7833-158">Vælg **Vælg billede** for at vælge et billede i mobilgalleriet eller **Tag foto** for at tage et billede.</span><span class="sxs-lookup"><span data-stu-id="d7833-158">Select **Choose image** to select a photo from the mobile gallery, or **Take photo** to take a photo.</span></span>

1. <span data-ttu-id="d7833-159">Vælg **Udført**.</span><span class="sxs-lookup"><span data-stu-id="d7833-159">Select **Done**.</span></span>

    <span data-ttu-id="d7833-160">![Se og tilføje tilknytninger til et arbejdsordrejob](media/am-mobile-04.png "Se og tilføje tilknytninger til et arbejdsordrejob")</span><span class="sxs-lookup"><span data-stu-id="d7833-160">![View and add attachments for a work order job](media/am-mobile-04.png "View and add attachments for a work order job")</span></span>

## <a name="view-maintenance-checklist-on-a-work-order-job"></a><span data-ttu-id="d7833-161">Få vist vedligeholdelsestjeklisten for et arbejdsordrejob</span><span class="sxs-lookup"><span data-stu-id="d7833-161">View maintenance checklist on a work order job</span></span>

1. <span data-ttu-id="d7833-162">På din mobilenhed skal du åbne arbejdsområdet **Styring af aktiver**.</span><span class="sxs-lookup"><span data-stu-id="d7833-162">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="d7833-163">Vælg **Alle vedligeholdelsesarbejdsordrer**.</span><span class="sxs-lookup"><span data-stu-id="d7833-163">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="d7833-164">Vælg den arbejdsordre > arbejdsordrejob, du vil se tjeklister for.</span><span class="sxs-lookup"><span data-stu-id="d7833-164">Select the work order > work order job you want to view checklists for.</span></span>
    - <span data-ttu-id="d7833-165">Alternativt kan du også vælge **Min kalender over arbejdsordrejob** eller **Min liste over arbejdsordrejob** på startsiden for at navigere til siden **Oplysninger om arbejdsordrejob**.</span><span class="sxs-lookup"><span data-stu-id="d7833-165">Alternatively, you can also select **My work order jobs calendar** or **My work order jobs list** on the home page to navigate to the **work order job details** page.</span></span>

1. <span data-ttu-id="d7833-166">Vælg **Kontrollister** på siden **Oplysninger om arbejdsordrejob**.</span><span class="sxs-lookup"><span data-stu-id="d7833-166">Select **Checklists** on the **Work order job details** page.</span></span>

1. <span data-ttu-id="d7833-167">Der vises en liste over tjeklistelinjer, der er relateret til arbejdsordrejobbet.</span><span class="sxs-lookup"><span data-stu-id="d7833-167">You'll see a list of checklist lines related to the work order job.</span></span> <span data-ttu-id="d7833-168">Vælg en tjeklistelinje for at få vist **Instruktioner** og tilføje **notater**.</span><span class="sxs-lookup"><span data-stu-id="d7833-168">Select a checklist line to view **Instructions** and add **Notes**.</span></span>

1. <span data-ttu-id="d7833-169">Vælg knappen Tilbage (**<**) for at vende tilbage til den forrige side.</span><span class="sxs-lookup"><span data-stu-id="d7833-169">Select the back button (**<**) to return to the previous page.</span></span>

    <span data-ttu-id="d7833-170">![Vedligeholdelsestjekliste og linjedetaljer](media/am-mobile-05.png "Vedligeholdelsestjekliste og linjedetaljer")</span><span class="sxs-lookup"><span data-stu-id="d7833-170">![Maintenance checklist and line details](media/am-mobile-05.png "Maintenance checklist and line details")</span></span>

## <a name="view-and-update-asset-counters-on-a-work-order-job"></a><span data-ttu-id="d7833-171">Få vist og opdatere aktivtællere på et arbejdsordrejob</span><span class="sxs-lookup"><span data-stu-id="d7833-171">View and update asset counters on a work order job</span></span>

1. <span data-ttu-id="d7833-172">På din mobilenhed skal du åbne arbejdsområdet **Styring af aktiver**.</span><span class="sxs-lookup"><span data-stu-id="d7833-172">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="d7833-173">Vælg **Alle vedligeholdelsesarbejdsordrer**.</span><span class="sxs-lookup"><span data-stu-id="d7833-173">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="d7833-174">Vælg den arbejdsordre > arbejdsordrejob, du vil se aktivtællere for.</span><span class="sxs-lookup"><span data-stu-id="d7833-174">Select the work order > work order job you want to view asset counters for.</span></span>
    - <span data-ttu-id="d7833-175">Alternativt kan du også vælge **Min kalender over arbejdsordrejob** eller **Min liste over arbejdsordrejob** på startsiden for at navigere til siden **Oplysninger om arbejdsordrejob**.</span><span class="sxs-lookup"><span data-stu-id="d7833-175">Alternatively, you can also select **My work order jobs calendar** or **My work order jobs list** on the home page to navigate to the **work order job details** page.</span></span>

1. <span data-ttu-id="d7833-176">Vælg **Aktivtællere** på siden **Oplysninger om arbejdsordrejob**.</span><span class="sxs-lookup"><span data-stu-id="d7833-176">Select **Asset counters** on the **Work order job details** page.</span></span>

1. <span data-ttu-id="d7833-177">Der vises en liste over aktivtællere, der er relateret til arbejdsordrejobbet.</span><span class="sxs-lookup"><span data-stu-id="d7833-177">You see a list of asset counters related to the work order job.</span></span> <span data-ttu-id="d7833-178">Vælg blyantikonet på en aktivtællerlinje for at opdatere tællerværdien.</span><span class="sxs-lookup"><span data-stu-id="d7833-178">Select the pencil icon on an asset counter line to update the counter value.</span></span>

1. <span data-ttu-id="d7833-179">Angiv en ny tællerværdi, og vælg **Udført**.</span><span class="sxs-lookup"><span data-stu-id="d7833-179">Enter a new counter value, and select **Done**.</span></span>

    <span data-ttu-id="d7833-180">![Se og opdatere aktivtællere](media/am-mobile-06.png "Se og opdatere aktivtællere")</span><span class="sxs-lookup"><span data-stu-id="d7833-180">![View and update asset counters](media/am-mobile-06.png "View and update asset counters")</span></span>

## <a name="register-consumption-on-a-work-order-job"></a><span data-ttu-id="d7833-181">Registrer forbrug på et arbejdsordrejob</span><span class="sxs-lookup"><span data-stu-id="d7833-181">Register consumption on a work order job</span></span>

1. <span data-ttu-id="d7833-182">På din mobilenhed skal du åbne arbejdsområdet **Styring af aktiver**.</span><span class="sxs-lookup"><span data-stu-id="d7833-182">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="d7833-183">Vælg **Alle vedligeholdelsesarbejdsordrer**.</span><span class="sxs-lookup"><span data-stu-id="d7833-183">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="d7833-184">Vælg arbejdsordre > arbejdsordrejob, du vil tilføje forbrugsregistreringer for.</span><span class="sxs-lookup"><span data-stu-id="d7833-184">Select the work order > work order job you want to add consumption registrations for.</span></span>
    - <span data-ttu-id="d7833-185">Alternativt kan du også vælge **Min kalender over arbejdsordrejob** eller **Min liste over arbejdsordrejob** på startsiden for at navigere til siden **Oplysninger om arbejdsordrejob**.</span><span class="sxs-lookup"><span data-stu-id="d7833-185">Alternatively, you can also select **My work order jobs calendar** or **My work order jobs list** on the home page to navigate to the **work order job details** page.</span></span>

1. <span data-ttu-id="d7833-186">Vælg **Kladder** på siden **Oplysninger om arbejdsordrejob**.</span><span class="sxs-lookup"><span data-stu-id="d7833-186">Select **Journals** on the **Work order job details** page.</span></span>

1. <span data-ttu-id="d7833-187">Vælg **Tilføj timer** for at oprette arbejdstidsregistreringer.</span><span class="sxs-lookup"><span data-stu-id="d7833-187">Select **Add hours** to create work hour registrations.</span></span>
    1. <span data-ttu-id="d7833-188">Vælg **Kategori** fra opslaget.</span><span class="sxs-lookup"><span data-stu-id="d7833-188">Select the **Category** from the lookup.</span></span>
    1. <span data-ttu-id="d7833-189">Angiv det antal arbejdstimer, der er brugt på arbejdsordrejobbet, i feltet **Timer**.</span><span class="sxs-lookup"><span data-stu-id="d7833-189">In the **Hours** field, enter the number of work hours spent on the work order job.</span></span>
    1. <span data-ttu-id="d7833-190">Vælg den relevante **Linjeegenskab**.</span><span class="sxs-lookup"><span data-stu-id="d7833-190">Select the appropriate **Line property**.</span></span>
    1. <span data-ttu-id="d7833-191">Vælg **Udført**.</span><span class="sxs-lookup"><span data-stu-id="d7833-191">Select **Done**.</span></span>

1. <span data-ttu-id="d7833-192">Vælg **Tilføj varer** for at oprette vareregistreringer.</span><span class="sxs-lookup"><span data-stu-id="d7833-192">Select **Add items** to create item registrations.</span></span>
    1. <span data-ttu-id="d7833-193">Vælg **Varenummer** fra opslaget.</span><span class="sxs-lookup"><span data-stu-id="d7833-193">Select the **Item number** from the lookup.</span></span>
    1. <span data-ttu-id="d7833-194">Vælg **Sted** fra opslaget.</span><span class="sxs-lookup"><span data-stu-id="d7833-194">Select the **Site** from the lookup.</span></span>
    1. <span data-ttu-id="d7833-195">Angiv forbrugte varer under **Antal**.</span><span class="sxs-lookup"><span data-stu-id="d7833-195">Enter the **Quantity** of items consumed.</span></span>
    1. <span data-ttu-id="d7833-196">Vælg **Udført**.</span><span class="sxs-lookup"><span data-stu-id="d7833-196">Select **Done**.</span></span>

1. <span data-ttu-id="d7833-197">Vælg **Tilføj udgift** for at oprette udgiftsregistreringer.</span><span class="sxs-lookup"><span data-stu-id="d7833-197">Select **Add expense** to create expense registrations.</span></span>
    1. <span data-ttu-id="d7833-198">Vælg **Kategori** fra opslaget.</span><span class="sxs-lookup"><span data-stu-id="d7833-198">Select the **Category** from the lookup.</span></span>
    1. <span data-ttu-id="d7833-199">Angiv antallet for udgiftsregistreringen.</span><span class="sxs-lookup"><span data-stu-id="d7833-199">Enter the quantity for the expense registration.</span></span>
    1. <span data-ttu-id="d7833-200">Vælg **Salgsvaluta** fra opslaget.</span><span class="sxs-lookup"><span data-stu-id="d7833-200">Select the **Sales currency** from the lookup.</span></span>
    1. <span data-ttu-id="d7833-201">Angiv **Kostpris** for udgiftsregistreringen.</span><span class="sxs-lookup"><span data-stu-id="d7833-201">Enter the **Cost price** for the expense registration.</span></span>
    1. <span data-ttu-id="d7833-202">Vælg **Udført**.</span><span class="sxs-lookup"><span data-stu-id="d7833-202">Select **Done**.</span></span>

    <span data-ttu-id="d7833-203">![Opdatere en arbejdsordrekladde](media/am-mobile-07.png "Opdatere en arbejdsordrekladde")</span><span class="sxs-lookup"><span data-stu-id="d7833-203">![Update a work order journal](media/am-mobile-07.png "Update a work order journal")</span></span>

## <a name="update-lifecycle-state-on-a-work-order"></a><span data-ttu-id="d7833-204">Opdater livscyklustilstand på en arbejdsordre</span><span class="sxs-lookup"><span data-stu-id="d7833-204">Update lifecycle state on a work order</span></span>

1. <span data-ttu-id="d7833-205">På din mobilenhed skal du åbne arbejdsområdet **Styring af aktiver**.</span><span class="sxs-lookup"><span data-stu-id="d7833-205">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="d7833-206">Vælg **Alle vedligeholdelsesarbejdsordrer**.</span><span class="sxs-lookup"><span data-stu-id="d7833-206">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="d7833-207">Vælg den arbejdsordre, du vil opdatere livscyklustilstand for.</span><span class="sxs-lookup"><span data-stu-id="d7833-207">Select the work order you want to update lifecycle state for.</span></span>

1. <span data-ttu-id="d7833-208">Vælg knappen **Opdater tilstand** nederst på skærmen.</span><span class="sxs-lookup"><span data-stu-id="d7833-208">Select the **Update state** button at the bottom of the screen.</span></span>

1. <span data-ttu-id="d7833-209">Vælg en ny livscyklustilstand på listen.</span><span class="sxs-lookup"><span data-stu-id="d7833-209">Select a new lifecycle state from the list.</span></span>

1. <span data-ttu-id="d7833-210">Vælg **Udført**.</span><span class="sxs-lookup"><span data-stu-id="d7833-210">Select **Done**.</span></span>

    <span data-ttu-id="d7833-211">![Opdater livscyklustilstand på en arbejdsordre](media/am-mobile-08.png "Opdater livscyklustilstand på en arbejdsordre")</span><span class="sxs-lookup"><span data-stu-id="d7833-211">![Update lifecycle state on a work order](media/am-mobile-08.png "Update lifecycle state on a work order")</span></span>

## <a name="create-a-maintenance-request"></a><span data-ttu-id="d7833-212">Oprette en vedligeholdelsesanmodning</span><span class="sxs-lookup"><span data-stu-id="d7833-212">Create a maintenance request</span></span>

1. <span data-ttu-id="d7833-213">På din mobilenhed skal du åbne arbejdsområdet **Styring af aktiver**.</span><span class="sxs-lookup"><span data-stu-id="d7833-213">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="d7833-214">Vælg **Alle vedligeholdelsesanmodninger**.</span><span class="sxs-lookup"><span data-stu-id="d7833-214">Select **All maintenance requests**.</span></span>

1. <span data-ttu-id="d7833-215">Vælg **Handlinger** nederst på skærmen, og vælg **Opret vedligeholdelsesanmodning**.</span><span class="sxs-lookup"><span data-stu-id="d7833-215">Select **Actions** at the bottom of the screen, and select **Create maintenance request**.</span></span>

1. <span data-ttu-id="d7833-216">Hvis nummerserien er aktiveret for vedligeholdelsesanmodninger i **Styring af aktiver** er feltet **Vedligeholdelsesanmodning** skjult, fordi det udfyldes automatisk. Hvis feltet **Vedligeholdelsesanmodning** er synligt, skal du angive et id for vedligeholdelsesanmodningen.</span><span class="sxs-lookup"><span data-stu-id="d7833-216">If number sequence is enabled for maintenance requests in **Asset management**, the **Maintenance request** field is hidden because it is automatically filled out. If the **Maintenance request** field is visible, enter a maintenance request ID.</span></span>

1. <span data-ttu-id="d7833-217">Vælg en **Vedligeholdelsesanmodningstype**.</span><span class="sxs-lookup"><span data-stu-id="d7833-217">Select a **Maintenance request type**.</span></span>

1. <span data-ttu-id="d7833-218">Angiv en **Beskrivelse** af vedligeholdelsesanmodningen.</span><span class="sxs-lookup"><span data-stu-id="d7833-218">Enter a **Description** for the maintenance request.</span></span>

1. <span data-ttu-id="d7833-219">Vælg det **Aktiv**, som du vil oprette anmodningen for.</span><span class="sxs-lookup"><span data-stu-id="d7833-219">Select the **Asset** you want to create the request for.</span></span>

1. <span data-ttu-id="d7833-220">Vælg **Serviceniveau** for vedligeholdelsesanmodningen.</span><span class="sxs-lookup"><span data-stu-id="d7833-220">Select the **Service level** for the maintenance request.</span></span>

1. <span data-ttu-id="d7833-221">Vælg **Udført**.</span><span class="sxs-lookup"><span data-stu-id="d7833-221">Select **Done**.</span></span>

    <span data-ttu-id="d7833-222">![Oprette en vedligeholdelsesanmodning](media/am-mobile-09.png "Oprette en vedligeholdelsesanmodning")</span><span class="sxs-lookup"><span data-stu-id="d7833-222">![Create a maintenance request](media/am-mobile-09.png "Create a maintenance request")</span></span>

## <a name="add-attachment-to-a-maintenance-request"></a><span data-ttu-id="d7833-223">Føj en vedhæftet fil til en vedligeholdelsesanmodning</span><span class="sxs-lookup"><span data-stu-id="d7833-223">Add attachment to a maintenance request</span></span>

1. <span data-ttu-id="d7833-224">På din mobilenhed skal du åbne arbejdsområdet **Styring af aktiver**.</span><span class="sxs-lookup"><span data-stu-id="d7833-224">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="d7833-225">Vælg **Alle vedligeholdelsesanmodninger**.</span><span class="sxs-lookup"><span data-stu-id="d7833-225">Select **All maintenance requests**.</span></span>

1. <span data-ttu-id="d7833-226">Vælg den vedligeholdelsesanmodning, du vil føje en vedhæftet fil til.</span><span class="sxs-lookup"><span data-stu-id="d7833-226">Select the maintenance request you want to add an attachment to.</span></span>

1. <span data-ttu-id="d7833-227">Vælg **Vedhæftede filer** nederst på skærmen.</span><span class="sxs-lookup"><span data-stu-id="d7833-227">Select **Attachments** at the bottom of the screen.</span></span>

1. <span data-ttu-id="d7833-228">Vælg **Tilføj vedhæftede filer**.</span><span class="sxs-lookup"><span data-stu-id="d7833-228">Select **Add attachments**.</span></span>

1. <span data-ttu-id="d7833-229">Angiv **Navn** og **Notater** for den vedhæftede fil.</span><span class="sxs-lookup"><span data-stu-id="d7833-229">Enter **Name** and **Notes** for the attachment.</span></span>

1. <span data-ttu-id="d7833-230">Vælg **Vælg billede** for at vælge et billede i mobilgalleriet eller **Tag foto** for at tage et billede.</span><span class="sxs-lookup"><span data-stu-id="d7833-230">Select **Choose image** to select a photo from the mobile gallery or **Take photo** to take a photo.</span></span>

1. <span data-ttu-id="d7833-231">Vælg **Udført**.</span><span class="sxs-lookup"><span data-stu-id="d7833-231">Select **Done**.</span></span>

    <span data-ttu-id="d7833-232">![Føj en vedhæftet fil til en vedligeholdelsesanmodning](media/am-mobile-10.png "Føj en vedhæftet fil til en vedligeholdelsesanmodning")</span><span class="sxs-lookup"><span data-stu-id="d7833-232">![Add an attachment to a maintenance request](media/am-mobile-10.png "Add an attachment to a maintenance request")</span></span>
