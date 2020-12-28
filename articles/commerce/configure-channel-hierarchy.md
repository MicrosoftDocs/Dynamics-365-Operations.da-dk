---
title: Konfigurere en kanal for at bruge et navigationshierarki for en kanal
description: Dette emne beskriver, hvordan du konfigurerer en kanal for at bruge et navigationshierarki for en kanal i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 7b5041d35d310125c314ab2cb77d3cc40cdb7113
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410984"
---
# <a name="configure-a-channel-to-use-a-channel-navigation-hierarchy"></a><span data-ttu-id="9e930-103">Konfigurere en kanal for at bruge et navigationshierarki for en kanal</span><span class="sxs-lookup"><span data-stu-id="9e930-103">Configure a channel to use a channel navigation hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="9e930-104">Dette emne beskriver, hvordan du konfigurerer en kanal for at bruge et navigationshierarki for en kanal i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9e930-104">This topic describes how to configure a channel to use a channel navigation hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9e930-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="9e930-105">Overview</span></span>

<span data-ttu-id="9e930-106">Navigationshierarkier for en kanal organiserer produkter i kategorier, så produkterne kan gennemses på et e-handelswebsted eller ved POS.</span><span class="sxs-lookup"><span data-stu-id="9e930-106">Channel navigation hierarchies organize products into categories so that the products can be browsed on an e-Commerce site or at points of sale (POS).</span></span> <span data-ttu-id="9e930-107">Detail- og onlinekanaler skal konfigureres med navigationshierarkier for en kanal.</span><span class="sxs-lookup"><span data-stu-id="9e930-107">Retail and online channels must be configured with channel navigation hierarchies.</span></span>

## <a name="configure-the-channel"></a><span data-ttu-id="9e930-108">Konfigurere kanalen</span><span class="sxs-lookup"><span data-stu-id="9e930-108">Configure the channel</span></span>

<span data-ttu-id="9e930-109">Du kan konfigurere en kanal for at bruge et navigationshierarki for en kanal ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="9e930-109">To configure a channel to use a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="9e930-110">Gå til **Moduler \> Retail og Commerce \> Konfiguration af kanal \> Kanalkategorier og produktattributter** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="9e930-110">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Channel categories and product attributes**.</span></span>
1. <span data-ttu-id="9e930-111">Vælg den kanal, der skal konfigureres.</span><span class="sxs-lookup"><span data-stu-id="9e930-111">Select the channel to configure.</span></span>
1. <span data-ttu-id="9e930-112">I handlingsruden skal du vælge **Angiv attributmetadata**.</span><span class="sxs-lookup"><span data-stu-id="9e930-112">On the action pane, select **Set attribute metadata**.</span></span>
1. <span data-ttu-id="9e930-113">På rullelisten **Kategorihierarki** skal du vælge det relevante kanalnavigationshierarki.</span><span class="sxs-lookup"><span data-stu-id="9e930-113">In the **Category hierarchy** drop-down list, select the appropriate channel navigation hierarchy.</span></span>
1. <span data-ttu-id="9e930-114">Gå til handlingsruden, og vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="9e930-114">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="9e930-115">Under **Attributgruppe** skal du tilføje alle attributgrupper, der skal være globale attributter for alle noder.</span><span class="sxs-lookup"><span data-stu-id="9e930-115">Under **Attribute group**, add any attribute groups that will be global attributes for all nodes.</span></span>

<span data-ttu-id="9e930-116">Følgende billede viser, hvordan du konfigurerer en kanal for at bruge et navigationshierarki for en kanal.</span><span class="sxs-lookup"><span data-stu-id="9e930-116">The following image shows how to configure a channel to use a channel navigation hierarchy.</span></span>

![Eksempel på kanalkonfiguration](media/configure-channel-hierarchy-1.png)

## <a name="set-attribute-metadata"></a><span data-ttu-id="9e930-118">Angiv attributmetadata</span><span class="sxs-lookup"><span data-stu-id="9e930-118">Set attribute metadata</span></span>

<span data-ttu-id="9e930-119">Angivelse af attributmetadataene giver mulighed for konfiguration af attributter på de enkelte noder.</span><span class="sxs-lookup"><span data-stu-id="9e930-119">Setting the attribute metadata will allow configuration of attributes on each node.</span></span>

<span data-ttu-id="9e930-120">Du kan angive attributmetadataene ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="9e930-120">To set attribute metadata, follow these steps.</span></span>

1. <span data-ttu-id="9e930-121">I handlingsruden skal du vælge **Angiv attributmetadata**.</span><span class="sxs-lookup"><span data-stu-id="9e930-121">On the action pane, select **Set attribute metadata**.</span></span>
1. <span data-ttu-id="9e930-122">Vælg **Kanalproduktattributter** for hver node.</span><span class="sxs-lookup"><span data-stu-id="9e930-122">For each node select **Channel product attributes**.</span></span>
1. <span data-ttu-id="9e930-123">Angiv **Vis attribut på kanal** til **Ja** og **Kan redigeres** til **Ja**, hvis du vil aktivere afgrænsere på denne kanal.</span><span class="sxs-lookup"><span data-stu-id="9e930-123">Set **Show attribute on channel** to **Yes** and **Can be refined** to **Yes**, to enable refiners on that channel.</span></span>
1. <span data-ttu-id="9e930-124">Når du har konfigureret hver enkelt node efter behov, skal du vælge knappen **Gem** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="9e930-124">After configuring each node as desired, on the **Action pane**, select the **Save** button to save.</span></span>
1. <span data-ttu-id="9e930-125">Vælg **X** i øverste højre hjørne for at forlade dette skærmbillede og vende tilbage til siden **Kanalkategorier og produktattributter**.</span><span class="sxs-lookup"><span data-stu-id="9e930-125">Select the **X** in the top right corner to exit this screen back to the **Channel categories and product attributes** page.</span></span>

<span data-ttu-id="9e930-126">Følgende billede viser et sæt af kanalproduktattributter, der er konfigureret på en kanalkategorinode.</span><span class="sxs-lookup"><span data-stu-id="9e930-126">The following image shows an example set of channel product attributes configured on a channel category node.</span></span>

![Kanalattributter på en kanalkategorinode](media/configure-channel-hierarchy-2.png)

## <a name="publish-changes"></a><span data-ttu-id="9e930-128">Publicere ændringer</span><span class="sxs-lookup"><span data-stu-id="9e930-128">Publish changes</span></span>

<span data-ttu-id="9e930-129">Du skal publicere ændringerne, for at ændringerne træder i kraft.</span><span class="sxs-lookup"><span data-stu-id="9e930-129">For changes to take effect, you will need to publish the changes.</span></span>

<span data-ttu-id="9e930-130">Følg disse trin for at publicere ændringer.</span><span class="sxs-lookup"><span data-stu-id="9e930-130">To publish changes, follow these steps.</span></span>

1. <span data-ttu-id="9e930-131">Vælg **Publicer kanalopdateringer** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="9e930-131">On the action pane, select **Publish channel updates**.</span></span>
1. <span data-ttu-id="9e930-132">Vælg **OK** i ruden **Publicer kanalopdateringer**.</span><span class="sxs-lookup"><span data-stu-id="9e930-132">In the **Publish channel updates** pane, select **OK**.</span></span>

<span data-ttu-id="9e930-133">Følgende billede viser, hvordan du kan publicere kanalopdateringer.</span><span class="sxs-lookup"><span data-stu-id="9e930-133">The following image shows how to publish channel updates.</span></span>

![Publicer kanalopdateringer](media/configure-channel-hierarchy-3.png)

## <a name="additional-resources"></a><span data-ttu-id="9e930-135">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="9e930-135">Additional resources</span></span>

[<span data-ttu-id="9e930-136">Oprette et navigationshierarki for kanal</span><span class="sxs-lookup"><span data-stu-id="9e930-136">Create a channel navigation hierarchy</span></span>](create-channel-hierarchy.md)


