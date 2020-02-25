---
title: Føje en kanal til et organisationshierarki
description: Dette emne beskriver, hvordan du føjer en kanal til et organisationshierarki i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 701c90e8e28b4419422cddde698e9c9862a588a2
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002467"
---
# <a name="add-a-channel-to-an-organizational-hierarchy"></a><span data-ttu-id="f013c-103">Føje en kanal til et organisationshierarki</span><span class="sxs-lookup"><span data-stu-id="f013c-103">Add a channel to an organizational hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="f013c-104">Dette emne beskriver, hvordan du føjer en kanal til et organisationshierarki i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f013c-104">This topic describes how to add a channel to an organizational hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f013c-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="f013c-105">Overview</span></span>

<span data-ttu-id="f013c-106">Kanaler skal knyttes til et eller flere organisationshierarkier.</span><span class="sxs-lookup"><span data-stu-id="f013c-106">Channels need to be associated with one or more organizational hierarchies.</span></span> <span data-ttu-id="f013c-107">Før du opretter kanaler, skal du bekræfte, at organisationshierarkierne er konfigureret.</span><span class="sxs-lookup"><span data-stu-id="f013c-107">Before creating channels, you need to confirm that your organizational hierarchies have been set up.</span></span>  

<span data-ttu-id="f013c-108">Du kan finde flere oplysninger om oprettelse af organisationshierarkier i [Organisationshierarkier](channels-org-hierarchies.md).</span><span class="sxs-lookup"><span data-stu-id="f013c-108">See [Organizational hierarchies](channels-org-hierarchies.md) for more details on how to create organizational hierarchies.</span></span>

## <a name="select-a-hierarchy"></a><span data-ttu-id="f013c-109">Vælg et hierarki</span><span class="sxs-lookup"><span data-stu-id="f013c-109">Select a hierarchy</span></span>

<span data-ttu-id="f013c-110">Følg disse trin for at vælge et hierarki.</span><span class="sxs-lookup"><span data-stu-id="f013c-110">To select a hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="f013c-111">Gå til **Moduler \> Retail og Commerce \> Konfiguration af kanal \> Organisationshierarkier** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="f013c-111">In the navigation pane, go to **Modules \> Retail and commerce \> Channel Setup \> Organization hierarchies**.</span></span>
1. <span data-ttu-id="f013c-112">Vælg det organisationshierarki, du vil føje kanalen til, på listen.</span><span class="sxs-lookup"><span data-stu-id="f013c-112">From the list, select the organization hierarchy that you'll be adding the channel to.</span></span>
1. <span data-ttu-id="f013c-113">Vælg **Vis** i handlingsruden for at få vist hierarkioplysninger.</span><span class="sxs-lookup"><span data-stu-id="f013c-113">On the action pane, select **View** to view hierarchy details.</span></span>

<span data-ttu-id="f013c-114">Følgende billede viser detaljer om organisationshierarkiet for det valgte hierarki.</span><span class="sxs-lookup"><span data-stu-id="f013c-114">The following image shows organizational hierarchy details for the selected hierarchy.</span></span>

![Detaljer om organisationshierarkiet for det valgte hierarki](media/channel-add-to-org-hierarchy-1.png)

## <a name="add-a-channel-to-a-hierachy-node"></a><span data-ttu-id="f013c-116">Føje en kanal til en hierarkinode</span><span class="sxs-lookup"><span data-stu-id="f013c-116">Add a channel to a hierachy node</span></span>

<span data-ttu-id="f013c-117">Følg disse trin for at føje en kanal til en hierarkinode.</span><span class="sxs-lookup"><span data-stu-id="f013c-117">To add a channel to a hierachy node, follow these steps.</span></span>

1. <span data-ttu-id="f013c-118">Vælg **Rediger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="f013c-118">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="f013c-119">Vælg den hierarkinode, som kanalen skal føjes til, og vælg derefter **Detailkanal** på rullelisten **Indsæt**.</span><span class="sxs-lookup"><span data-stu-id="f013c-119">Select the hierachy node you want the channel added to, then from the **Insert** drop-down list, select **Retail Channel**.</span></span> 
1. <span data-ttu-id="f013c-120">Vælg den kanal, der skal tilføjes, og vælg derefter knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="f013c-120">Select the channel to add, then select the **OK** button.</span></span>
1. <span data-ttu-id="f013c-121">Gå til handlingsruden, og vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="f013c-121">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="f013c-122">Vælg **Udgiv** i handlingsruden, og angiv en **Ikrafttrædelsesdato** i fortiden, så denne handling træder i kraft med det samme.</span><span class="sxs-lookup"><span data-stu-id="f013c-122">On the action pane, select **Publish** and provide an **Effective date** in the past to have this action go into effect immediately.</span></span>

<span data-ttu-id="f013c-123">Følgende billede viser, hvordan du vælger en kanal, som skal føjes til en hierarkinode.</span><span class="sxs-lookup"><span data-stu-id="f013c-123">The following image shows how to select a channel to add to a hierarchy node.</span></span>

![Vælge en kanal, som skal føjes til en hierarkinode](media/channel-add-to-org-hierarchy-2.png)

<span data-ttu-id="f013c-125">Følgende billede viser et hierarki med forskellige kanaler tilføjet.</span><span class="sxs-lookup"><span data-stu-id="f013c-125">The following image shows a hierarchy with various channels added.</span></span>

![Et hierarki med forskellige kanaler tilføjet](media/channel-add-to-org-hierarchy-3.png)

## <a name="additional-resources"></a><span data-ttu-id="f013c-127">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="f013c-127">Additional resources</span></span>

[<span data-ttu-id="f013c-128">Oversigt over kanaler</span><span class="sxs-lookup"><span data-stu-id="f013c-128">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="f013c-129">Forudsætninger for konfiguration af kanal</span><span class="sxs-lookup"><span data-stu-id="f013c-129">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="f013c-130">Oversigt over organisationer og organisationshierarkier</span><span class="sxs-lookup"><span data-stu-id="f013c-130">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="f013c-131">Planlægge dit organisationshierarki</span><span class="sxs-lookup"><span data-stu-id="f013c-131">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="f013c-132">Organisationshierarkier</span><span class="sxs-lookup"><span data-stu-id="f013c-132">Organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="f013c-133">Konfigurer en detailkanal</span><span class="sxs-lookup"><span data-stu-id="f013c-133">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="f013c-134">Konfigurere en onlinekanal</span><span class="sxs-lookup"><span data-stu-id="f013c-134">Set up an online channel</span></span>](channel-setup-online.md)
