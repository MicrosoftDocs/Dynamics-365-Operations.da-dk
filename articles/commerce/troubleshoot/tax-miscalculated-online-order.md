---
title: Moms på onlineordrer beregnes forkert
description: Dette emne indeholder en vejledning til fejlfinding, der kan hjælpe, når moms på onlineordrer beregnes forkert, eller når momsgruppen på salgslinjen ikke er angivet korrekt.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: 421df7545e285950ef8a3c4b753c8c6dc5f26422
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585245"
---
# <a name="taxes-on-online-orders-are-incorrectly-calculated"></a><span data-ttu-id="1d39c-103">Moms på onlineordrer beregnes forkert</span><span class="sxs-lookup"><span data-stu-id="1d39c-103">Taxes on online orders are incorrectly calculated</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1d39c-104">Dette emne indeholder en vejledning til fejlfinding, der kan hjælpe, når moms på onlineordrer beregnes forkert, eller når momsgruppen på salgslinjen ikke er angivet korrekt.</span><span class="sxs-lookup"><span data-stu-id="1d39c-104">This topic provides troubleshooting guidance that can help when taxes on online orders are incorrectly calculated, or when the tax group on the sales line isn't correctly set.</span></span>

## <a name="description"></a><span data-ttu-id="1d39c-105">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="1d39c-105">Description</span></span>

<span data-ttu-id="1d39c-106">Når der afregnes en e-handelsordre, beregnes momsen forkert, eller momsgruppen på salgslinjen angives forkert.</span><span class="sxs-lookup"><span data-stu-id="1d39c-106">When an e-commerce order is placed, the taxes are incorrectly calculated, or the tax group on the sales line is incorrectly set.</span></span>

## <a name="resolution"></a><span data-ttu-id="1d39c-107">Løsning</span><span class="sxs-lookup"><span data-stu-id="1d39c-107">Resolution</span></span>

### <a name="configure-the-sales-tax-for-a-retail-store-in-commerce-headquarters"></a><span data-ttu-id="1d39c-108">Konfigurere momsen for en detailbutik i Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="1d39c-108">Configure the sales tax for a retail store in Commerce headquarters</span></span>

<span data-ttu-id="1d39c-109">Følg disse trin for at konfigurere momsen for en detailbutik i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="1d39c-109">To configure the sales tax for a retail store in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="1d39c-110">Gå til **Retail og Commerce \> Kanaler \> Alle butikker**.</span><span class="sxs-lookup"><span data-stu-id="1d39c-110">Go to **Retail and Commerce \> Channels \> All stores**.</span></span>
1. <span data-ttu-id="1d39c-111">Vælg den butik, du vil konfigurere moms for.</span><span class="sxs-lookup"><span data-stu-id="1d39c-111">Select the store to configure sales tax for.</span></span>
1. <span data-ttu-id="1d39c-112">Konfigurer momsoplysningerne for butikken i sektionen **Moms** i oversigtspanelet **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="1d39c-112">On the **General** FastTab, in the **Sales tax** section, configure the sales tax information for the store.</span></span>

> [!NOTE]
> <span data-ttu-id="1d39c-113">I forbindelse med produktafhentning fra en butik kommer momsgruppen fra den butik, der er valgt til afhentning.</span><span class="sxs-lookup"><span data-stu-id="1d39c-113">For product pickup from a store, the tax group comes from the store that is selected for pickup.</span></span> <span data-ttu-id="1d39c-114">Du kan finde flere oplysninger i [Angivelse af andre momsindstillinger for butikker](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span><span class="sxs-lookup"><span data-stu-id="1d39c-114">For more information, see [Set other tax options for stores](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span></span>

### <a name="configure-the-sales-tax-for-a-customers-address-in-commerce-headquarters"></a><span data-ttu-id="1d39c-115">Konfigurere momsen for en kundes adresse i Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="1d39c-115">Configure the sales tax for a customer's address in Commerce headquarters</span></span>

<span data-ttu-id="1d39c-116">Følg disse trin for at konfigurere momsen for en kundes adresse i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="1d39c-116">To configure the sales tax for a customer's address in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="1d39c-117">Gå til **Debitorer \> Kunder \> Alle kunder**.</span><span class="sxs-lookup"><span data-stu-id="1d39c-117">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="1d39c-118">Vælg den kunde, du vil konfigurere moms for.</span><span class="sxs-lookup"><span data-stu-id="1d39c-118">Select the customer to configure sales taxes for.</span></span>
1. <span data-ttu-id="1d39c-119">Vælg den adresse, du vil konfigurere moms for, i oversigtspanelet **Adresser**, vælg **Flere indstillinger**, og vælg derefter **Avanceret**.</span><span class="sxs-lookup"><span data-stu-id="1d39c-119">On the **Addresses** FastTab, select the address to configure sales taxes for, select **More options**, and then select **Advanced**.</span></span>
1. <span data-ttu-id="1d39c-120">Vælg **Momsgruppe** på oversigtspanelet **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="1d39c-120">On the **General** FastTab, select the **Tax group**.</span></span>
1. <span data-ttu-id="1d39c-121">Vælg den relevante værdi i feltet **Moms**.</span><span class="sxs-lookup"><span data-stu-id="1d39c-121">In the **Sales tax** field, select the appropriate value.</span></span>

> [!NOTE]
> <span data-ttu-id="1d39c-122">For forsendelse, der involverer moms på kundens adresse, bestemmer linjens leveringsadresse momsgruppen.</span><span class="sxs-lookup"><span data-stu-id="1d39c-122">For shipping that involves sales tax on the customer's address, the delivery address of the line determines the tax group for the line.</span></span> <span data-ttu-id="1d39c-123">Hvis kunden afsendes til en eksisterende adresse, der allerede er konfigureret en momsgruppe, vil den eksisterende momsgruppe blive brugt.</span><span class="sxs-lookup"><span data-stu-id="1d39c-123">If the customer is shipping to an existing address that has a tax group that is already configured, the existing tax group will be used.</span></span> <span data-ttu-id="1d39c-124">Som standard har adresser ikke en momsgruppe, når de oprettes.</span><span class="sxs-lookup"><span data-stu-id="1d39c-124">By default, addresses don't have a tax group when they are created.</span></span>

### <a name="configure-general-sales-tax-groups-in-commerce-headquarters"></a><span data-ttu-id="1d39c-125">Konfigurere generelle momsgrupper i Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="1d39c-125">Configure general sales tax groups in Commerce headquarters</span></span>

<span data-ttu-id="1d39c-126">Følg disse trin for at konfigurere generelle momsgrupper i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="1d39c-126">To configure general sales tax groups in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="1d39c-127">Gå til **Moms \> Indirekte skatter \> Moms \> Momsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="1d39c-127">Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax group**.</span></span>
1. <span data-ttu-id="1d39c-128">Vælg den momsgruppe, der skal konfigureres, i venstre navigation.</span><span class="sxs-lookup"><span data-stu-id="1d39c-128">In the left navigation, select the tax group to configure.</span></span>
1. <span data-ttu-id="1d39c-129">Konfigurer momsen for momsgruppen i oversigtspanelet **Detaildestinationsbaseret moms**.</span><span class="sxs-lookup"><span data-stu-id="1d39c-129">On the **Retail destination based tax** FastTab, configure the taxes for the sales tax group.</span></span>

> [!NOTE]
> <span data-ttu-id="1d39c-130">For forsendelse, der ikke involverer moms på kundens adresse, bestemmer leveringsadressen på linjen og den destinationsbaserede moms, der er konfigureret for momsgruppen, momsgruppen.</span><span class="sxs-lookup"><span data-stu-id="1d39c-130">For shipping that doesn't involve sales tax on the customer's address, the delivery address of the line and the destination-based taxes that are configured for the tax group determine the tax group.</span></span> <span data-ttu-id="1d39c-131">Du kan finde flere oplysninger i [Konfigurere moms for onlinebutikker, der er baseret på destinationen](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span><span class="sxs-lookup"><span data-stu-id="1d39c-131">For more information, see [Set up taxes for online stores based on destination](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1d39c-132">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="1d39c-132">Additional resources</span></span>

[<span data-ttu-id="1d39c-133">Konfigurere moms for onlineordrer</span><span class="sxs-lookup"><span data-stu-id="1d39c-133">Configure sales tax for online orders</span></span>](../sales-tax-config.md)
