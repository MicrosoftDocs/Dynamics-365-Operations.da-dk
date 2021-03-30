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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 4212797d2959c4f8b0d60e6b45de76ffc3ee0dc2
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5216740"
---
# <a name="add-a-channel-to-an-organizational-hierarchy"></a><span data-ttu-id="ecde6-103">Føje en kanal til et organisationshierarki</span><span class="sxs-lookup"><span data-stu-id="ecde6-103">Add a channel to an organizational hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="ecde6-104">Dette emne beskriver, hvordan du føjer en kanal til et organisationshierarki i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ecde6-104">This topic describes how to add a channel to an organizational hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ecde6-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="ecde6-105">Overview</span></span>

<span data-ttu-id="ecde6-106">Kanaler skal knyttes til et eller flere organisationshierarkier.</span><span class="sxs-lookup"><span data-stu-id="ecde6-106">Channels need to be associated with one or more organizational hierarchies.</span></span> <span data-ttu-id="ecde6-107">Før du opretter kanaler, skal du bekræfte, at organisationshierarkierne er konfigureret.</span><span class="sxs-lookup"><span data-stu-id="ecde6-107">Before creating channels, you need to confirm that your organizational hierarchies have been set up.</span></span>  

<span data-ttu-id="ecde6-108">Du kan finde flere oplysninger om oprettelse af organisationshierarkier i [Organisationshierarkier](channels-org-hierarchies.md).</span><span class="sxs-lookup"><span data-stu-id="ecde6-108">See [Organizational hierarchies](channels-org-hierarchies.md) for more details on how to create organizational hierarchies.</span></span>

## <a name="select-a-hierarchy"></a><span data-ttu-id="ecde6-109">Vælg et hierarki</span><span class="sxs-lookup"><span data-stu-id="ecde6-109">Select a hierarchy</span></span>

<span data-ttu-id="ecde6-110">Følg disse trin for at vælge et hierarki.</span><span class="sxs-lookup"><span data-stu-id="ecde6-110">To select a hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="ecde6-111">Gå til **Moduler \> Retail og Commerce \> Konfiguration af kanal \> Organisationshierarkier** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="ecde6-111">In the navigation pane, go to **Modules \> Retail and commerce \> Channel Setup \> Organization hierarchies**.</span></span>
1. <span data-ttu-id="ecde6-112">Vælg det organisationshierarki, du vil føje kanalen til, på listen.</span><span class="sxs-lookup"><span data-stu-id="ecde6-112">From the list, select the organization hierarchy that you'll be adding the channel to.</span></span>
1. <span data-ttu-id="ecde6-113">Vælg **Vis** i handlingsruden for at få vist hierarkioplysninger.</span><span class="sxs-lookup"><span data-stu-id="ecde6-113">On the action pane, select **View** to view hierarchy details.</span></span>

<span data-ttu-id="ecde6-114">Følgende billede viser detaljer om organisationshierarkiet for det valgte hierarki.</span><span class="sxs-lookup"><span data-stu-id="ecde6-114">The following image shows organizational hierarchy details for the selected hierarchy.</span></span>

![Detaljer om organisationshierarkiet for det valgte hierarki](media/channel-add-to-org-hierarchy-1.png)

## <a name="add-a-channel-to-a-hierachy-node"></a><span data-ttu-id="ecde6-116">Føje en kanal til en hierarkinode</span><span class="sxs-lookup"><span data-stu-id="ecde6-116">Add a channel to a hierachy node</span></span>

<span data-ttu-id="ecde6-117">Følg disse trin for at føje en kanal til en hierarkinode.</span><span class="sxs-lookup"><span data-stu-id="ecde6-117">To add a channel to a hierachy node, follow these steps.</span></span>

1. <span data-ttu-id="ecde6-118">Vælg **Rediger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="ecde6-118">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="ecde6-119">Vælg den hierarkinode, som kanalen skal føjes til, og vælg derefter **Detailkanal** på rullelisten **Indsæt**.</span><span class="sxs-lookup"><span data-stu-id="ecde6-119">Select the hierachy node you want the channel added to, then from the **Insert** drop-down list, select **Retail Channel**.</span></span> 
1. <span data-ttu-id="ecde6-120">Vælg den kanal, der skal tilføjes, og vælg derefter knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="ecde6-120">Select the channel to add, then select the **OK** button.</span></span>
1. <span data-ttu-id="ecde6-121">Gå til handlingsruden, og vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="ecde6-121">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="ecde6-122">Vælg **Udgiv** i handlingsruden, og angiv en **Ikrafttrædelsesdato** i fortiden, så denne handling træder i kraft med det samme.</span><span class="sxs-lookup"><span data-stu-id="ecde6-122">On the action pane, select **Publish** and provide an **Effective date** in the past to have this action go into effect immediately.</span></span>

<span data-ttu-id="ecde6-123">Følgende billede viser, hvordan du vælger en kanal, som skal føjes til en hierarkinode.</span><span class="sxs-lookup"><span data-stu-id="ecde6-123">The following image shows how to select a channel to add to a hierarchy node.</span></span>

![Vælge en kanal, som skal føjes til en hierarkinode](media/channel-add-to-org-hierarchy-2.png)

<span data-ttu-id="ecde6-125">Følgende billede viser et hierarki med forskellige kanaler tilføjet.</span><span class="sxs-lookup"><span data-stu-id="ecde6-125">The following image shows a hierarchy with various channels added.</span></span>

![Et hierarki med forskellige kanaler tilføjet](media/channel-add-to-org-hierarchy-3.png)

## <a name="additional-resources"></a><span data-ttu-id="ecde6-127">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="ecde6-127">Additional resources</span></span>

[<span data-ttu-id="ecde6-128">Oversigt over kanaler</span><span class="sxs-lookup"><span data-stu-id="ecde6-128">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="ecde6-129">Forudsætninger for konfiguration af kanal</span><span class="sxs-lookup"><span data-stu-id="ecde6-129">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="ecde6-130">Oversigt over organisationer og organisationshierarkier</span><span class="sxs-lookup"><span data-stu-id="ecde6-130">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="ecde6-131">Planlægge dit organisationshierarki</span><span class="sxs-lookup"><span data-stu-id="ecde6-131">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="ecde6-132">Organisationshierarkier</span><span class="sxs-lookup"><span data-stu-id="ecde6-132">Organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="ecde6-133">Konfigurer en detailkanal</span><span class="sxs-lookup"><span data-stu-id="ecde6-133">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="ecde6-134">Konfigurere en onlinekanal</span><span class="sxs-lookup"><span data-stu-id="ecde6-134">Set up an online channel</span></span>](channel-setup-online.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]