---
title: Afhentningsindstillingen vises ikke på sider med oplysninger om indkøbsvogn eller produkt
description: Dette emne indeholder en vejledning i fejlfinding, der kan hjælpe, når indstillingen for afhentning i butikken ikke vises på siden med indkøbsvognen eller produktdetaljer.
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
ms.openlocfilehash: f692d73bf1755422e9bfc8314c1156e043ccf761
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020799"
---
# <a name="pick-this-up-option-doesnt-appear-on-cart-or-product-details-pages"></a><span data-ttu-id="5b32d-103">"Afhentningsindstillingen" vises ikke på sider med oplysninger om indkøbsvogn eller produkt</span><span class="sxs-lookup"><span data-stu-id="5b32d-103">"Pick this up" option doesn't appear on cart or product details pages</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5b32d-104">Dette emne indeholder en vejledning i fejlfinding, der kan hjælpe, når indstillingen for afhentning i butikken ikke vises på siden med indkøbsvognen eller produktdetaljer.</span><span class="sxs-lookup"><span data-stu-id="5b32d-104">This topic provides troubleshooting guidance that can help when the option for in-store pickup doesn't appear on the cart page or product details pages.</span></span>

## <a name="description"></a><span data-ttu-id="5b32d-105">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="5b32d-105">Description</span></span>

<span data-ttu-id="5b32d-106">Knappen **Afhent** vises ikke på sider med oplysninger om indkøbsvogn eller produkt.</span><span class="sxs-lookup"><span data-stu-id="5b32d-106">The **Pick this up** button doesn't appear on the cart page or product details pages.</span></span>

<span data-ttu-id="5b32d-107">I følgende illustration vises et eksempel på en side, der indeholder knappen **Afhent**.</span><span class="sxs-lookup"><span data-stu-id="5b32d-107">The following illustration shows an example of a page that includes the **Pick this up** button.</span></span>

![Knappen Afhent](media/pickup-button-missing.jpg)

## <a name="resolution"></a><span data-ttu-id="5b32d-109">Løsning</span><span class="sxs-lookup"><span data-stu-id="5b32d-109">Resolution</span></span>

### <a name="enable-the-bopis-extension-in-commerce-site-builder"></a><span data-ttu-id="5b32d-110">Aktivere BOPIS-filtypenavnet i Commerce Site Builder</span><span class="sxs-lookup"><span data-stu-id="5b32d-110">Enable the BOPIS extension in Commerce site builder</span></span>

<span data-ttu-id="5b32d-111">Hvis du vil aktivere filtypen "køb online, hent op i butikken" (BOPIS) i Commerce site builder, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="5b32d-111">To enable the "buy online, pick up in store" (BOPIS) extension in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="5b32d-112">Vælge dit websted.</span><span class="sxs-lookup"><span data-stu-id="5b32d-112">Select your site.</span></span>
1. <span data-ttu-id="5b32d-113">Vælg **Webstedsindstillinger**, og vælg derefter **Udvidelse**.</span><span class="sxs-lookup"><span data-stu-id="5b32d-113">Select **Site settings**, and then select **Extensions**.</span></span>
1. <span data-ttu-id="5b32d-114">Kontroller, at indstillingen **Deaktiver BOPIS** er fjernet.</span><span class="sxs-lookup"><span data-stu-id="5b32d-114">Make sure that the **Disable BOPIS** option is cleared.</span></span>

### <a name="configure-modes-of-delivery-in-commerce-headquarters"></a><span data-ttu-id="5b32d-115">Konfigurere leveringsmåder i Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="5b32d-115">Configure modes of delivery in Commerce headquarters</span></span>

<span data-ttu-id="5b32d-116">Følg disse trin for at konfigurere leveringstilstande i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="5b32d-116">To configure modes of delivery in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="5b32d-117">Gå til **Indkøb og forsyning \> Opsætning \> Leveringstilstande**.</span><span class="sxs-lookup"><span data-stu-id="5b32d-117">Go to **Procurement and sourcing \> Setup \> Modes of delivery**.</span></span>
1. <span data-ttu-id="5b32d-118">Kontroller, at der oprettet en **Kundeafhentning**, og at der er knyttet produkter og adresser til den.</span><span class="sxs-lookup"><span data-stu-id="5b32d-118">Make sure that a **Customer pickup** mode of delivery has been created, and that products and addresses are assigned to it.</span></span>
1. <span data-ttu-id="5b32d-119">Gå til **Retail og Commerce \> Headquarters setup \> Parametre**.</span><span class="sxs-lookup"><span data-stu-id="5b32d-119">Go to **Retail and Commerce \> Headquarters setup \> Parameters**.</span></span>
1. <span data-ttu-id="5b32d-120">Vælg **Kundeordrer** i navigationsruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="5b32d-120">In the left navigation, select **Customer orders**.</span></span>
1. <span data-ttu-id="5b32d-121">Sørg for, **Levering gennem afhentning** er konfigureret korrekt.</span><span class="sxs-lookup"><span data-stu-id="5b32d-121">Make sure that **Pickup mode of delivery** is correctly configured.</span></span>

### <a name="configure-customer-orders-payments"></a><span data-ttu-id="5b32d-122">Konfigurere debitorordrebetalinger</span><span class="sxs-lookup"><span data-stu-id="5b32d-122">Configure customer orders payments</span></span>

<span data-ttu-id="5b32d-123">Følg disse trin for at konfigurere kundeordrebetalinger i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="5b32d-123">To configure customer orders payments in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="5b32d-124">Gå til **Retail og Commerce \> Headquarters setup \> Parametre**.</span><span class="sxs-lookup"><span data-stu-id="5b32d-124">Go to **Retail and Commerce \> Headquarters setup \> Parameters**.</span></span>
1. <span data-ttu-id="5b32d-125">Vælg **Kundeordrer** i navigationsruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="5b32d-125">In the left navigation, select **Customer orders**.</span></span>
1. <span data-ttu-id="5b32d-126">Kontroller, at felterne **Betalingsbetingelser** og **Betalingsmetoder** på oversigtspanelet **Betalinger** er angivet korrekt.</span><span class="sxs-lookup"><span data-stu-id="5b32d-126">On the **Payments** FastTab, make sure that the **Terms of payment** and **Method of payment** fields are correctly set.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5b32d-127">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="5b32d-127">Additional resources</span></span>

[<span data-ttu-id="5b32d-128">Konfigurere BOPIS</span><span class="sxs-lookup"><span data-stu-id="5b32d-128">Configure BOPIS</span></span>](../cpe-bopis.md)

[<span data-ttu-id="5b32d-129">Aktivere flere leveringsmåder for afhentning af kundeordrer</span><span class="sxs-lookup"><span data-stu-id="5b32d-129">Enable multiple pickup delivery modes for customer orders</span></span>](../multiple-pickup-modes.md)

[<span data-ttu-id="5b32d-130">Omni-kanalers Commerce-ordrebetalinger</span><span class="sxs-lookup"><span data-stu-id="5b32d-130">Omni-channel Commerce order payments</span></span>](../dev-itpro/commerce-payments.md)

[<span data-ttu-id="5b32d-131">Butiksvælgermodul</span><span class="sxs-lookup"><span data-stu-id="5b32d-131">Store selector module</span></span>](../store-selector.md)
