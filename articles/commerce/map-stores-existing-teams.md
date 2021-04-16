---
title: Tilknytte butikker og teams, hvis der er eksisterende teams i Microsoft Teams
description: I dette emne kan du se, hvordan du kan tilknytte butikker og tilsvarende teams i Dynamics 365 Commerce-hovedkontoret, hvis din organisation allerede har oprettet teams i Microsoft Teams inden Commerce-integrationen.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3edd176788b24a5f5246e9b7bcb3c6fbcdca2254
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842634"
---
# <a name="map-stores-and-teams-if-there-are-pre-existing-teams-in-microsoft-teams"></a><span data-ttu-id="ecc15-103">Tilknytte butikker og teams, hvis der er eksisterende teams i Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="ecc15-103">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="ecc15-104">I dette emne kan du se, hvordan du kan tilknytte butikker og tilsvarende teams i Dynamics 365 Commerce-hovedkontoret, hvis din organisation allerede har oprettet teams i Microsoft Teams inden Commerce-integrationen.</span><span class="sxs-lookup"><span data-stu-id="ecc15-104">This topic covers how to map stores and corresponding teams in Dynamics 365 Commerce headquarters if your organization has already created teams in Microsoft Teams before Commerce integration.</span></span>

<span data-ttu-id="ecc15-105">Der kan være oprettet teams i din organisation for nogle af eller alle dine butikker, før Dynamics 365 Commerce og Microsoft Teams integreres.</span><span class="sxs-lookup"><span data-stu-id="ecc15-105">Your organization may have teams created for some or all of your stores before integrating Dynamics 365 Commerce and Microsoft Teams.</span></span> <span data-ttu-id="ecc15-106">Hvis det er tilfældet, skal du oprette opgavesynkronisering mellem Commerce POS og Microsoft Teams, og du skal angive tilknytningen af butikker og det tilsvarende team i Commerce-hovedkontoret.</span><span class="sxs-lookup"><span data-stu-id="ecc15-106">If this is the case, to establish task synchronization between Commerce POS and Microsoft Teams you must provide the mapping of stores and corresponding team in Commerce headquarters.</span></span>

## <a name="map-stores-and-corresponding-teams-in-commerce-headquarters"></a><span data-ttu-id="ecc15-107">Tilknytte butikker og tilsvarende teams i Commerce-hovedkontor</span><span class="sxs-lookup"><span data-stu-id="ecc15-107">Map stores and corresponding teams in Commerce headquarters</span></span> 

<span data-ttu-id="ecc15-108">Følg disse trin for at tilknytte butikker og tilsvarende teams i Commerce-hovedkontor.</span><span class="sxs-lookup"><span data-stu-id="ecc15-108">To map stores and corresponding teams in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="ecc15-109">Gå til **Systemadministration \> Arbejdsområde \> Datastyring**.</span><span class="sxs-lookup"><span data-stu-id="ecc15-109">Go to **System Administration \> Workspace \> Data management**.</span></span>
1. <span data-ttu-id="ecc15-110">Vælg **Eksportér**.</span><span class="sxs-lookup"><span data-stu-id="ecc15-110">Select **Export**.</span></span> 
1. <span data-ttu-id="ecc15-111">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="ecc15-111">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="ecc15-112">Angiv "Eksportér tilknytning af teams" under **Gruppenavn**.</span><span class="sxs-lookup"><span data-stu-id="ecc15-112">Under **Group name**, enter "Export Teams mapping".</span></span>
1. <span data-ttu-id="ecc15-113">Vælg **Tilføj enhed** i oversigtspanelet **Valgte enheder**.</span><span class="sxs-lookup"><span data-stu-id="ecc15-113">On the **Selected entities** FastTab, select **Add entity**.</span></span> <span data-ttu-id="ecc15-114">Dialogboksen **Tilføj enhed** vises.</span><span class="sxs-lookup"><span data-stu-id="ecc15-114">The **Add entity** dialog box appears.</span></span>  
1. <span data-ttu-id="ecc15-115">Vælg **Teams-tilknytning mellem kilde og team** på rullelisten **Enhedsnavn**.</span><span class="sxs-lookup"><span data-stu-id="ecc15-115">In the **Entity name** drop-down list, select **Teams mapping between source and team**.</span></span>
1. <span data-ttu-id="ecc15-116">Vælg **CSV** på rullelisten **Måldataformat**.</span><span class="sxs-lookup"><span data-stu-id="ecc15-116">In the **Target data format** drop-down list, select **CSV**.</span></span>
1. <span data-ttu-id="ecc15-117">Vælg **Tilføj**, og vælg derefter **Luk**.</span><span class="sxs-lookup"><span data-stu-id="ecc15-117">Select **Add**, and then select **Close**.</span></span>
1. <span data-ttu-id="ecc15-118">Vælg **Eksportér nu** øverst til venstre under handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="ecc15-118">On the top left under the Action Pane, select **Export now**.</span></span>
1. <span data-ttu-id="ecc15-119">Vælg **Download fil** under **Status for enhedsbehandling**.</span><span class="sxs-lookup"><span data-stu-id="ecc15-119">Under **Entity processing status**, select **Download file**.</span></span>
1. <span data-ttu-id="ecc15-120">I den eksporterede CSV-fil skal du angive værdier for **SOURCETYPE**, **SOURCEID** og **TEAMID** på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="ecc15-120">In the exported CSV file, enter values for **SOURCETYPE**, **SOURCEID**, and **TEAMID** as follows:</span></span>
    - <span data-ttu-id="ecc15-121">Indtast "RetailStore" for **SOURCETYPE**.</span><span class="sxs-lookup"><span data-stu-id="ecc15-121">For **SOURCETYPE**, enter "RetailStore".</span></span> 
    - <span data-ttu-id="ecc15-122">For **SOURCEID** skal du angive butiksnummeret (f.eks. "000135" for San Francisco-butikken).</span><span class="sxs-lookup"><span data-stu-id="ecc15-122">For **SOURCEID**, enter the store number (for example, "000135" for the San Francisco store).</span></span> <span data-ttu-id="ecc15-123">Du kan finde butiksnumre i **Retail og Commerce \> Kanaler \> Butikker**.</span><span class="sxs-lookup"><span data-stu-id="ecc15-123">You can find store numbers at **Retail and Commerce \> Channels \> Stores**.</span></span>
    - <span data-ttu-id="ecc15-124">For **TEAMID** skal du angive det tilsvarende team-id fra Microsoft Teams (f.eks. "5f8bc92b-6aa8-451e-85d1-3949c01ddc6c").</span><span class="sxs-lookup"><span data-stu-id="ecc15-124">For **TEAMID**, enter the corresponding team ID from Microsoft Teams (for example, "5f8bc92b-6aa8-451e-85d1-3949c01ddc6c").</span></span> <span data-ttu-id="ecc15-125">Du kan finde oplysninger om team-id'er på [admin.teams.microsoft.com](https://admin.teams.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="ecc15-125">You can find team ID information at [admin.teams.microsoft.com](https://admin.teams.microsoft.com).</span></span>
1. <span data-ttu-id="ecc15-126">Gem CSV-filen på din lokale computer.</span><span class="sxs-lookup"><span data-stu-id="ecc15-126">Save the CSV file to your local machine.</span></span>
1. <span data-ttu-id="ecc15-127">Gå til **Systemadministration \> Arbejdsområde \> Datastyring**, og vælg **Import**..</span><span class="sxs-lookup"><span data-stu-id="ecc15-127">Go to **System Administration \> Workspace \> Data management**, and then select **Import**.</span></span>
1. <span data-ttu-id="ecc15-128">Vælg **Tilføj fil** i oversigtspanelet **Valgte enheder**.</span><span class="sxs-lookup"><span data-stu-id="ecc15-128">On the **Selected entities** FastTab, select **Add file**.</span></span> <span data-ttu-id="ecc15-129">Dialogboksen **Tilføj fil** vises.</span><span class="sxs-lookup"><span data-stu-id="ecc15-129">The **Add file** dialog box appears.</span></span>
1. <span data-ttu-id="ecc15-130">Vælg **Teams-tilknytning mellem kilde og team** på rullelisten **Enhedsnavn**.</span><span class="sxs-lookup"><span data-stu-id="ecc15-130">In the **Entity name** drop-down list, select **Teams mapping between source and team**.</span></span>
1. <span data-ttu-id="ecc15-131">Vælg **CSV** på rullelisten **Kildedataformat**.</span><span class="sxs-lookup"><span data-stu-id="ecc15-131">In the **Source data format** drop-down list, select **CSV**.</span></span>
1. <span data-ttu-id="ecc15-132">Vælg **Upload og tilføj**, vælg den CSV-fil, du har gemt tidligere, og vælg derefter **Åbn**.</span><span class="sxs-lookup"><span data-stu-id="ecc15-132">Select **Upload and add**, select the CSV file that you saved previously, and then select **Open**.</span></span>
1. <span data-ttu-id="ecc15-133">Vælg **Luk** i dialogboksen **Tilføj fil**.</span><span class="sxs-lookup"><span data-stu-id="ecc15-133">In the **Add file** dialog box, select **Close**.</span></span>
1. <span data-ttu-id="ecc15-134">Vælg **Gem** i handlingsruden, og vælg derefter **Import**.</span><span class="sxs-lookup"><span data-stu-id="ecc15-134">On the Action Pane, select **Save** , and then select **Import**.</span></span>

<span data-ttu-id="ecc15-135">I følgende eksempelbillede vises gruppen **Eksportér tilknytning af teams** i Commerce med **Tilføj enhed**-elementer og de eksporterede CSV-filhoveder fremhævet.</span><span class="sxs-lookup"><span data-stu-id="ecc15-135">The following example image shows the **Export teams mapping** group in Commerce with **Add entity** elements and the exported CSV file headers highlighted.</span></span>

![Gruppen Eksportér tilknytning af teams i Commerce med Tilføj enhed-elementer og de eksporterede CSV-filhoveder fremhævet](media/d365-commerce-data-mgmt-export-entity.png)

> [!NOTE]
> <span data-ttu-id="ecc15-137">Når du har fuldført de forudgående trin, skal du udføre trinnene i [Synkronisere opgavestyring mellem Microsoft Teams og POS](synchronize-tasks-teams-pos.md) for at synkronisere opgavestyring.</span><span class="sxs-lookup"><span data-stu-id="ecc15-137">After you complete the preceeding steps, follow the steps in [Synchronize task management between Microsoft Teams and POS](synchronize-tasks-teams-pos.md) to synchronize task management.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="ecc15-138">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="ecc15-138">Additional resources</span></span>

[<span data-ttu-id="ecc15-139">Oversigt over Dynamics 365 Commerce- og Microsoft Teams-integration</span><span class="sxs-lookup"><span data-stu-id="ecc15-139">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="ecc15-140">Aktivere Dynamics 365 Commerce- og Microsoft Teams-integration</span><span class="sxs-lookup"><span data-stu-id="ecc15-140">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="ecc15-141">Klargøre Microsoft Teams fra Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="ecc15-141">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="ecc15-142">Synkronisere opgavestyring mellem Microsoft Teams og Dynamics 365 Commerce POS</span><span class="sxs-lookup"><span data-stu-id="ecc15-142">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="ecc15-143">Administrere brugerroller i Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="ecc15-143">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="ecc15-144">Ofte stillede spørgsmål til Dynamics 365 Commerce- og Microsoft Teams-integration</span><span class="sxs-lookup"><span data-stu-id="ecc15-144">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
