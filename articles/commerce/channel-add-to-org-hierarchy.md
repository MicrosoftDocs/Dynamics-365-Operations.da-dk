---
title: Føje en kanal til et organisationshierarki
description: Dette emne beskriver, hvordan du føjer en kanal til et organisationshierarki i Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: c7ff6d8ee7e526e45975cfa500b5e6d6079054dc
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800681"
---
# <a name="add-a-channel-to-an-organizational-hierarchy"></a><span data-ttu-id="be59f-103">Føje en kanal til et organisationshierarki</span><span class="sxs-lookup"><span data-stu-id="be59f-103">Add a channel to an organizational hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="be59f-104">Dette emne beskriver, hvordan du føjer en kanal til et organisationshierarki i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="be59f-104">This topic describes how to add a channel to an organizational hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="be59f-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="be59f-105">Overview</span></span>

<span data-ttu-id="be59f-106">Kanaler skal knyttes til et eller flere organisationshierarkier.</span><span class="sxs-lookup"><span data-stu-id="be59f-106">Channels need to be associated with one or more organizational hierarchies.</span></span> <span data-ttu-id="be59f-107">Før du opretter kanaler, skal du bekræfte, at organisationshierarkierne er konfigureret.</span><span class="sxs-lookup"><span data-stu-id="be59f-107">Before creating channels, you need to confirm that your organizational hierarchies have been set up.</span></span>  

<span data-ttu-id="be59f-108">Du kan finde flere oplysninger om oprettelse af organisationshierarkier i [Organisationshierarkier](channels-org-hierarchies.md).</span><span class="sxs-lookup"><span data-stu-id="be59f-108">See [Organizational hierarchies](channels-org-hierarchies.md) for more details on how to create organizational hierarchies.</span></span>

## <a name="select-a-hierarchy"></a><span data-ttu-id="be59f-109">Vælg et hierarki</span><span class="sxs-lookup"><span data-stu-id="be59f-109">Select a hierarchy</span></span>

<span data-ttu-id="be59f-110">Følg disse trin for at vælge et hierarki.</span><span class="sxs-lookup"><span data-stu-id="be59f-110">To select a hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="be59f-111">Gå til **Moduler \> Retail og Commerce \> Konfiguration af kanal \> Organisationshierarkier** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="be59f-111">In the navigation pane, go to **Modules \> Retail and commerce \> Channel Setup \> Organization hierarchies**.</span></span>
1. <span data-ttu-id="be59f-112">Vælg det organisationshierarki, du vil føje kanalen til, på listen.</span><span class="sxs-lookup"><span data-stu-id="be59f-112">From the list, select the organization hierarchy that you'll be adding the channel to.</span></span>
1. <span data-ttu-id="be59f-113">Vælg **Vis** i handlingsruden for at få vist hierarkioplysninger.</span><span class="sxs-lookup"><span data-stu-id="be59f-113">On the action pane, select **View** to view hierarchy details.</span></span>

<span data-ttu-id="be59f-114">Følgende billede viser detaljer om organisationshierarkiet for det valgte hierarki.</span><span class="sxs-lookup"><span data-stu-id="be59f-114">The following image shows organizational hierarchy details for the selected hierarchy.</span></span>

![Detaljer om organisationshierarkiet for det valgte hierarki](media/channel-add-to-org-hierarchy-1.png)

## <a name="add-a-channel-to-a-hierachy-node"></a><span data-ttu-id="be59f-116">Føje en kanal til en hierarkinode</span><span class="sxs-lookup"><span data-stu-id="be59f-116">Add a channel to a hierachy node</span></span>

<span data-ttu-id="be59f-117">Følg disse trin for at føje en kanal til en hierarkinode.</span><span class="sxs-lookup"><span data-stu-id="be59f-117">To add a channel to a hierachy node, follow these steps.</span></span>

1. <span data-ttu-id="be59f-118">Vælg **Rediger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="be59f-118">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="be59f-119">Vælg den hierarkinode, som kanalen skal føjes til, og vælg derefter **Detailkanal** på rullelisten **Indsæt**.</span><span class="sxs-lookup"><span data-stu-id="be59f-119">Select the hierachy node you want the channel added to, then from the **Insert** drop-down list, select **Retail Channel**.</span></span> 
1. <span data-ttu-id="be59f-120">Vælg den kanal, der skal tilføjes, og vælg derefter knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="be59f-120">Select the channel to add, then select the **OK** button.</span></span>
1. <span data-ttu-id="be59f-121">Gå til handlingsruden, og vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="be59f-121">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="be59f-122">Vælg **Udgiv** i handlingsruden, og angiv en **Ikrafttrædelsesdato** i fortiden, så denne handling træder i kraft med det samme.</span><span class="sxs-lookup"><span data-stu-id="be59f-122">On the action pane, select **Publish** and provide an **Effective date** in the past to have this action go into effect immediately.</span></span>

<span data-ttu-id="be59f-123">Følgende billede viser, hvordan du vælger en kanal, som skal føjes til en hierarkinode.</span><span class="sxs-lookup"><span data-stu-id="be59f-123">The following image shows how to select a channel to add to a hierarchy node.</span></span>

![Vælge en kanal, som skal føjes til en hierarkinode](media/channel-add-to-org-hierarchy-2.png)

<span data-ttu-id="be59f-125">Følgende billede viser et hierarki med forskellige kanaler tilføjet.</span><span class="sxs-lookup"><span data-stu-id="be59f-125">The following image shows a hierarchy with various channels added.</span></span>

![Et hierarki med forskellige kanaler tilføjet](media/channel-add-to-org-hierarchy-3.png)

## <a name="additional-resources"></a><span data-ttu-id="be59f-127">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="be59f-127">Additional resources</span></span>

[<span data-ttu-id="be59f-128">Oversigt over kanaler</span><span class="sxs-lookup"><span data-stu-id="be59f-128">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="be59f-129">Forudsætninger for konfiguration af kanal</span><span class="sxs-lookup"><span data-stu-id="be59f-129">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="be59f-130">Oversigt over organisationer og organisationshierarkier</span><span class="sxs-lookup"><span data-stu-id="be59f-130">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="be59f-131">Planlægge dit organisationshierarki</span><span class="sxs-lookup"><span data-stu-id="be59f-131">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="be59f-132">Organisationshierarkier</span><span class="sxs-lookup"><span data-stu-id="be59f-132">Organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="be59f-133">Konfigurer en detailkanal</span><span class="sxs-lookup"><span data-stu-id="be59f-133">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="be59f-134">Konfigurere en onlinekanal</span><span class="sxs-lookup"><span data-stu-id="be59f-134">Set up an online channel</span></span>](channel-setup-online.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]