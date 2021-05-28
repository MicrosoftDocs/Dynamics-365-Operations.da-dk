---
title: Retail-butik vises ikke på listen over butikker, der kan vælges
description: Dette emne indeholder vejledning i fejlfinding, der kan hjælpe, når en detailbutik ikke vises på listen over butikker, hvor der kan afhentes varer.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: ad7ddf8a17640471a2344c45eef76f682d29ef2b
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020811"
---
# <a name="retail-store-doesnt-appear-in-the-list-of-stores-to-pick-up-from"></a><span data-ttu-id="1dd34-103">Retail-butik vises ikke på listen over butikker, der kan vælges</span><span class="sxs-lookup"><span data-stu-id="1dd34-103">Retail store doesn't appear in the list of stores to pick up from</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1dd34-104">Dette emne indeholder vejledning i fejlfinding, der kan hjælpe, når en detailbutik ikke vises på listen over butikker, hvor der kan afhentes varer.</span><span class="sxs-lookup"><span data-stu-id="1dd34-104">This topic provides troubleshooting guidance that can help when a retail store doesn't appear in the list of stores where items can be picked up.</span></span>

## <a name="description"></a><span data-ttu-id="1dd34-105">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="1dd34-105">Description</span></span>

<span data-ttu-id="1dd34-106">En detailbutik vises ikke på listen over butikker, hvor varerne kan afhentes.</span><span class="sxs-lookup"><span data-stu-id="1dd34-106">A retail store doesn't appear in the list of stores where items can be picked up.</span></span>

## <a name="resolution"></a><span data-ttu-id="1dd34-107">Løsning</span><span class="sxs-lookup"><span data-stu-id="1dd34-107">Resolution</span></span>

### <a name="configure-the-longitude-and-latitude-for-the-store-address-in-commerce-headquarters"></a><span data-ttu-id="1dd34-108">Konfigurere længde- og breddegrad for butiksadressen i Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="1dd34-108">Configure the longitude and latitude for the store address in Commerce headquarters</span></span>

<span data-ttu-id="1dd34-109">Følg disse trin for at fonfigurere længde- og breddegrad for butiksadressen i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="1dd34-109">To configure the longitude and latitude for the store address in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="1dd34-110">Gå til **Retail og Commerce \> Kanaler \> Butikker \> Alle butikker**.</span><span class="sxs-lookup"><span data-stu-id="1dd34-110">Go to **Retail and Commerce \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="1dd34-111">Find den butik, du vil have vist blandt afhentningsindstillingerne på e-handelswebstedet.</span><span class="sxs-lookup"><span data-stu-id="1dd34-111">Find the store that you want to appear among the pickup options on the e-commerce site.</span></span> <span data-ttu-id="1dd34-112">Noter værdien for **driftsenhedsnummer**.</span><span class="sxs-lookup"><span data-stu-id="1dd34-112">Make a note of its **Operating unit number** value.</span></span>
1. <span data-ttu-id="1dd34-113">Gå til **Organisationsadministration \> Organisationer \> Driftsenheder**.</span><span class="sxs-lookup"><span data-stu-id="1dd34-113">Go to **Organization administration \> Organizations \> Operating units**.</span></span>
1. <span data-ttu-id="1dd34-114">Søg efter det driftsenhedsnummer, du har angivet tidligere, og vælg derefter driftsenheden i søgeresultaterne.</span><span class="sxs-lookup"><span data-stu-id="1dd34-114">Search for the operating unit number that you noted earlier, and then select the operating unit in the search results.</span></span>
1. <span data-ttu-id="1dd34-115">Vælg **Flere indstillinger** i oversigtspanelet **Adresser**, og vælg derefter **Avanceret**.</span><span class="sxs-lookup"><span data-stu-id="1dd34-115">On the **Addresses** FastTab, select **More options**, and then select **Advanced**.</span></span>
1. <span data-ttu-id="1dd34-116">Kontroller, at felterne **Længdegrad** og **Breddegrad** i oversigtspanelet **Generelt** er indstillet korrekt.</span><span class="sxs-lookup"><span data-stu-id="1dd34-116">On the **General** FastTab, make sure that the **Longitude** and **Latitude** fields are correctly set.</span></span> <span data-ttu-id="1dd34-117">Som en del af dette trin skal du sikre dig, at værdierne er angivet korrekt som positive eller negative tal.</span><span class="sxs-lookup"><span data-stu-id="1dd34-117">As part of this step, make sure that the values are correctly specified as positive or negative numbers.</span></span>

### <a name="configure-fulfillment-groups-in-commerce-headquarters"></a><span data-ttu-id="1dd34-118">Konfigurere opfyldningsgrupper i Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="1dd34-118">Configure fulfillment groups in Commerce headquarters</span></span>

<span data-ttu-id="1dd34-119">Følg disse trin for at konfigurere opfyldningsgrupper i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="1dd34-119">To configure fulfillment groups in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="1dd34-120">Gå til **Retail og Commerce \> Kanaler \> Onlinebutikker**.</span><span class="sxs-lookup"><span data-stu-id="1dd34-120">Go to **Retail and Commerce \> Channels \> Online stores**.</span></span>
1. <span data-ttu-id="1dd34-121">Vælg den onlinebutik, der skal konfigureres.</span><span class="sxs-lookup"><span data-stu-id="1dd34-121">Select the online store to configure.</span></span>
1. <span data-ttu-id="1dd34-122">Vælg fanen Handling skal du vælge **Opsætning** og derefter **Gruppetildeling for opfyldelse**.</span><span class="sxs-lookup"><span data-stu-id="1dd34-122">On the Action Pane, select **Set up**, and then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="1dd34-123">På siden **Tildeling af opfyldningsgruppe** skal du vælge opfyldningsgruppen for onlinebutikken.</span><span class="sxs-lookup"><span data-stu-id="1dd34-123">On the **Fulfillment group assignment** page, select the fulfillment group for the online store.</span></span>
1. <span data-ttu-id="1dd34-124">Under **Opsætning** skal du sikre dig, at detailbutikken er konfigureret korrekt til opfyldningsgruppen.</span><span class="sxs-lookup"><span data-stu-id="1dd34-124">Under **Setup**, make sure that the retail store is correctly configured for the fulfillment group.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1dd34-125">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="1dd34-125">Additional resources</span></span> 

[<span data-ttu-id="1dd34-126">Oprette en driftsenhed</span><span class="sxs-lookup"><span data-stu-id="1dd34-126">Create an operating unit</span></span>](../../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md)

[<span data-ttu-id="1dd34-127">Konfigurere en onlinekanal</span><span class="sxs-lookup"><span data-stu-id="1dd34-127">Set up an online channel</span></span>](../channel-setup-online.md)