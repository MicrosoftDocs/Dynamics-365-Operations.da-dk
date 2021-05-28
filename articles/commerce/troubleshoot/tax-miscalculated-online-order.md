---
title: Moms på onlineordrer beregnes forkert
description: Dette emne indeholder en vejledning til fejlfinding, der kan hjælpe, når moms på onlineordrer beregnes forkert, eller når momsgruppen på salgslinjen ikke er angivet korrekt.
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
ms.openlocfilehash: f7cef533d76bdddfbad2e8c5f84f81ef62bccc38
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021097"
---
# <a name="taxes-on-online-orders-are-incorrectly-calculated"></a><span data-ttu-id="50e85-103">Moms på onlineordrer beregnes forkert</span><span class="sxs-lookup"><span data-stu-id="50e85-103">Taxes on online orders are incorrectly calculated</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="50e85-104">Dette emne indeholder en vejledning til fejlfinding, der kan hjælpe, når moms på onlineordrer beregnes forkert, eller når momsgruppen på salgslinjen ikke er angivet korrekt.</span><span class="sxs-lookup"><span data-stu-id="50e85-104">This topic provides troubleshooting guidance that can help when taxes on online orders are incorrectly calculated, or when the tax group on the sales line isn't correctly set.</span></span>

## <a name="description"></a><span data-ttu-id="50e85-105">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="50e85-105">Description</span></span>

<span data-ttu-id="50e85-106">Når der afregnes en e-handelsordre, beregnes momsen forkert, eller momsgruppen på salgslinjen angives forkert.</span><span class="sxs-lookup"><span data-stu-id="50e85-106">When an e-commerce order is placed, the taxes are incorrectly calculated, or the tax group on the sales line is incorrectly set.</span></span>

## <a name="resolution"></a><span data-ttu-id="50e85-107">Løsning</span><span class="sxs-lookup"><span data-stu-id="50e85-107">Resolution</span></span>

### <a name="configure-the-sales-tax-for-a-retail-store-in-commerce-headquarters"></a><span data-ttu-id="50e85-108">Konfigurere momsen for en detailbutik i Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="50e85-108">Configure the sales tax for a retail store in Commerce headquarters</span></span>

<span data-ttu-id="50e85-109">Følg disse trin for at konfigurere momsen for en detailbutik i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="50e85-109">To configure the sales tax for a retail store in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="50e85-110">Gå til **Retail og Commerce \> Kanaler \> Alle butikker**.</span><span class="sxs-lookup"><span data-stu-id="50e85-110">Go to **Retail and Commerce \> Channels \> All stores**.</span></span>
1. <span data-ttu-id="50e85-111">Vælg den butik, du vil konfigurere moms for.</span><span class="sxs-lookup"><span data-stu-id="50e85-111">Select the store to configure sales tax for.</span></span>
1. <span data-ttu-id="50e85-112">Konfigurer momsoplysningerne for butikken i sektionen **Moms** i oversigtspanelet **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="50e85-112">On the **General** FastTab, in the **Sales tax** section, configure the sales tax information for the store.</span></span>

> [!NOTE]
> <span data-ttu-id="50e85-113">I forbindelse med produktafhentning fra en butik kommer momsgruppen fra den butik, der er valgt til afhentning.</span><span class="sxs-lookup"><span data-stu-id="50e85-113">For product pickup from a store, the tax group comes from the store that is selected for pickup.</span></span> <span data-ttu-id="50e85-114">Du kan finde flere oplysninger i [Angivelse af andre momsindstillinger for butikker](/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span><span class="sxs-lookup"><span data-stu-id="50e85-114">For more information, see [Set other tax options for stores](/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span></span>

### <a name="configure-the-sales-tax-for-a-customers-address-in-commerce-headquarters"></a><span data-ttu-id="50e85-115">Konfigurere momsen for en kundes adresse i Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="50e85-115">Configure the sales tax for a customer's address in Commerce headquarters</span></span>

<span data-ttu-id="50e85-116">Følg disse trin for at konfigurere momsen for en kundes adresse i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="50e85-116">To configure the sales tax for a customer's address in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="50e85-117">Gå til **Debitorer \> Kunder \> Alle kunder**.</span><span class="sxs-lookup"><span data-stu-id="50e85-117">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="50e85-118">Vælg den kunde, du vil konfigurere moms for.</span><span class="sxs-lookup"><span data-stu-id="50e85-118">Select the customer to configure sales taxes for.</span></span>
1. <span data-ttu-id="50e85-119">Vælg den adresse, du vil konfigurere moms for, i oversigtspanelet **Adresser**, vælg **Flere indstillinger**, og vælg derefter **Avanceret**.</span><span class="sxs-lookup"><span data-stu-id="50e85-119">On the **Addresses** FastTab, select the address to configure sales taxes for, select **More options**, and then select **Advanced**.</span></span>
1. <span data-ttu-id="50e85-120">Vælg **Momsgruppe** på oversigtspanelet **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="50e85-120">On the **General** FastTab, select the **Tax group**.</span></span>
1. <span data-ttu-id="50e85-121">Vælg den relevante værdi i feltet **Moms**.</span><span class="sxs-lookup"><span data-stu-id="50e85-121">In the **Sales tax** field, select the appropriate value.</span></span>

> [!NOTE]
> <span data-ttu-id="50e85-122">For forsendelse, der involverer moms på kundens adresse, bestemmer linjens leveringsadresse momsgruppen.</span><span class="sxs-lookup"><span data-stu-id="50e85-122">For shipping that involves sales tax on the customer's address, the delivery address of the line determines the tax group for the line.</span></span> <span data-ttu-id="50e85-123">Hvis kunden afsendes til en eksisterende adresse, der allerede er konfigureret en momsgruppe, vil den eksisterende momsgruppe blive brugt.</span><span class="sxs-lookup"><span data-stu-id="50e85-123">If the customer is shipping to an existing address that has a tax group that is already configured, the existing tax group will be used.</span></span> <span data-ttu-id="50e85-124">Som standard har adresser ikke en momsgruppe, når de oprettes.</span><span class="sxs-lookup"><span data-stu-id="50e85-124">By default, addresses don't have a tax group when they are created.</span></span>

### <a name="configure-general-sales-tax-groups-in-commerce-headquarters"></a><span data-ttu-id="50e85-125">Konfigurere generelle momsgrupper i Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="50e85-125">Configure general sales tax groups in Commerce headquarters</span></span>

<span data-ttu-id="50e85-126">Følg disse trin for at konfigurere generelle momsgrupper i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="50e85-126">To configure general sales tax groups in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="50e85-127">Gå til **Moms \> Indirekte skatter \> Moms \> Momsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="50e85-127">Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax group**.</span></span>
1. <span data-ttu-id="50e85-128">Vælg den momsgruppe, der skal konfigureres, i venstre navigation.</span><span class="sxs-lookup"><span data-stu-id="50e85-128">In the left navigation, select the tax group to configure.</span></span>
1. <span data-ttu-id="50e85-129">Konfigurer momsen for momsgruppen i oversigtspanelet **Detaildestinationsbaseret moms**.</span><span class="sxs-lookup"><span data-stu-id="50e85-129">On the **Retail destination based tax** FastTab, configure the taxes for the sales tax group.</span></span>

> [!NOTE]
> <span data-ttu-id="50e85-130">For forsendelse, der ikke involverer moms på kundens adresse, bestemmer leveringsadressen på linjen og den destinationsbaserede moms, der er konfigureret for momsgruppen, momsgruppen.</span><span class="sxs-lookup"><span data-stu-id="50e85-130">For shipping that doesn't involve sales tax on the customer's address, the delivery address of the line and the destination-based taxes that are configured for the tax group determine the tax group.</span></span> <span data-ttu-id="50e85-131">Du kan finde flere oplysninger i [Konfigurere moms for onlinebutikker, der er baseret på destinationen](/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span><span class="sxs-lookup"><span data-stu-id="50e85-131">For more information, see [Set up taxes for online stores based on destination](/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="50e85-132">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="50e85-132">Additional resources</span></span>

[<span data-ttu-id="50e85-133">Konfigurere moms for onlineordrer</span><span class="sxs-lookup"><span data-stu-id="50e85-133">Configure sales tax for online orders</span></span>](../sales-tax-config.md)