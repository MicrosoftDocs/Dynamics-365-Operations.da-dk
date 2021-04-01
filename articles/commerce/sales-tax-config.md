---
title: Konfigurere moms for onlineordrer
description: Dette emne giver en oversigt over valg af momsgrupper for forskellige onlineordretyper i Dynamics 365 Commerce.
author: gvrmohanreddy
manager: AnnBe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: gmohanv
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 36dd3e8a3d47f02eed5b9c8bb79d773d98069376
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254835"
---
# <a name="configure-sales-tax-for-online-orders"></a><span data-ttu-id="2897a-103">Konfigurere moms for onlineordrer</span><span class="sxs-lookup"><span data-stu-id="2897a-103">Configure sales tax for online orders</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2897a-104">Dette emne giver en oversigt over valg af momsgrupper for forskellige onlineordretyper.</span><span class="sxs-lookup"><span data-stu-id="2897a-104">This topic provides an overview of sales tax group selection for different online order types.</span></span> 

<span data-ttu-id="2897a-105">Din e-handelskanal vil måske understøtte valgmuligheder som levering eller afhentning af onlineordrer.</span><span class="sxs-lookup"><span data-stu-id="2897a-105">Your e-commerce channel may want to support options like delivery or pickup for online orders.</span></span> <span data-ttu-id="2897a-106">Om moms kan anvendes afhænger af den indstilling, som dine onlinebrugere vælger.</span><span class="sxs-lookup"><span data-stu-id="2897a-106">The sales tax applicability is based on the option selected by your online users.</span></span> <span data-ttu-id="2897a-107">Når en kunde på et websted vælger at købe en vare online og får den leveret til en adresse, bestemmes momsen på basis af kundens indstilling for momsgruppen for leveringsadressen.</span><span class="sxs-lookup"><span data-stu-id="2897a-107">When a site customer chooses to buy an item online and gets it shipped to an address, the sales tax is determined based on the customer's shipping address tax group setting.</span></span> <span data-ttu-id="2897a-108">Når en kunde vælger at afhente en købt vare i en butik, bestemmes momsen ud fra indstillingen for afhentningsbutikkens momsgruppe.</span><span class="sxs-lookup"><span data-stu-id="2897a-108">When a customer opts to pick up a purchased item at a store, the sales tax is determined based on the pickup store's tax group setting.</span></span> 

## <a name="orders-shipped-to-a-customer-address"></a><span data-ttu-id="2897a-109">Ordrer, der sendes til en kundeadresse</span><span class="sxs-lookup"><span data-stu-id="2897a-109">Orders shipped to a customer address</span></span> 

<span data-ttu-id="2897a-110">Generelt defineres moms på onlineordrer, der sendes til kundeadresser, af destinationen.</span><span class="sxs-lookup"><span data-stu-id="2897a-110">In general, taxes for online orders that ship to customer addresses are defined by the destination.</span></span> <span data-ttu-id="2897a-111">Hver momsgruppe har en konfiguration for moms, der er baseret på en detaildestination, hvor forretningen kan definere destinationsoplysninger, som f.eks. land/område, stat, region og by i en hierarkisk struktur.</span><span class="sxs-lookup"><span data-stu-id="2897a-111">Every sales tax group has a retail destination-based tax configuration in which your business can define destination details such as county/region, state, county, and city in a hierarchical form.</span></span> <span data-ttu-id="2897a-112">Når en onlineordre afgives, bruger Commerce-momsprogrammet leveringsadressen for alle linjevarer i ordren og finder momsgrupper med tilsvarende destinationsbaserede momskriterier.</span><span class="sxs-lookup"><span data-stu-id="2897a-112">When an online order is placed, the Commerce tax engine uses the delivery address of every line item in the order, and finds sales tax groups with matching destination-based tax criteria.</span></span> <span data-ttu-id="2897a-113">F.eks. kan momsprogrammet for en onlineordre med leveringsadresse for en linjevare i San Francisco, Californien, finde momsgruppen og momskoden for Californien og derefter beregne skatten for hvert linjeelement tilsvarende.</span><span class="sxs-lookup"><span data-stu-id="2897a-113">For example, for an online order with a line item delivery address to San Francisco, California, the tax engine will find the sales tax group and sales tax code for California and then calculate tax for each line item accordingly.</span></span>  

## <a name="customer-based-tax-groups"></a><span data-ttu-id="2897a-114">Kundebaserede momsgrupper</span><span class="sxs-lookup"><span data-stu-id="2897a-114">Customer-based tax groups</span></span>

<span data-ttu-id="2897a-115">I Commerce Headquarters er der to steder, hvor kundemomsgrupper kan konfigureres:</span><span class="sxs-lookup"><span data-stu-id="2897a-115">In Commerce headquarters, there are two places where customer tax groups are configured:</span></span>

- <span data-ttu-id="2897a-116">**Kundens profil**</span><span class="sxs-lookup"><span data-stu-id="2897a-116">**Customer's profile**</span></span>
- <span data-ttu-id="2897a-117">**Kundens leveringsadresse**</span><span class="sxs-lookup"><span data-stu-id="2897a-117">**Customer's shipping address**</span></span>

### <a name="if-a-customers-profile-has-a-tax-group-configured"></a><span data-ttu-id="2897a-118">Hvis en kundes profil har en konfigureret momsgruppe</span><span class="sxs-lookup"><span data-stu-id="2897a-118">If a customer's profile has a tax group configured</span></span>

<span data-ttu-id="2897a-119">En kundeprofilpost i Headquarters kan have en konfigureret momsgruppe, men til onlineordrer bruges den momsgruppe, der er konfigureret i en kundeprofil, ikke af momsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="2897a-119">A customer's profile record in headquarters may have a sales tax group configured, however for online orders the sales tax group configured in a customer's profile will not be used by the tax engine.</span></span> 

### <a name="if-a-customers-shipping-address-has-a-tax-group-configured"></a><span data-ttu-id="2897a-120">Hvis en kundes leveringsadresse har en konfigureret momsgruppe</span><span class="sxs-lookup"><span data-stu-id="2897a-120">If a customer's shipping address has a tax group configured</span></span>

<span data-ttu-id="2897a-121">Hvis der er konfigureret en momsgruppe for en kundes leveringsadressepost, og der leveres en onlineordre (eller linjevare) til kundens leveringsadresse, vil den momsgruppe, der er konfigureret i kundens adressepost, blive brugt af momsprogrammet til momsberegninger.</span><span class="sxs-lookup"><span data-stu-id="2897a-121">If a customer's shipping address record has a tax group configured and an online order (or line item) is shipped to the customer's shipping address, the tax group configured in the customer's address record will be used by the tax engine for tax calculations.</span></span>

#### <a name="configure-a-tax-group-for-a-customers-shipping-address-record"></a><span data-ttu-id="2897a-122">Konfigurere en momsgruppe for en kundes leveringsadressepost</span><span class="sxs-lookup"><span data-stu-id="2897a-122">Configure a tax group for a customer's shipping address record</span></span>

<span data-ttu-id="2897a-123">Hvis du vil konfigurere en momsgruppe for en kundes leveringsadressepost i Commerce Headquarters, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="2897a-123">To configure a tax group for a customer's shipping address record in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="2897a-124">Gå til **Alle debitorer**, og vælg derefter den ønskede debitor.</span><span class="sxs-lookup"><span data-stu-id="2897a-124">Go to **All customers**, and then select the desired customer.</span></span> 
1. <span data-ttu-id="2897a-125">I oversigtspanelet **Adresser** skal du vælge den ønskede adresse og derefter vælge **Flere indstillinger \> Avanceret**.</span><span class="sxs-lookup"><span data-stu-id="2897a-125">On the **Addresses** FastTab, select the desired address, and then select **More options \> Advanced**.</span></span> 
1. <span data-ttu-id="2897a-126">Angiv momsværdien efter behov under fanen **Generelt** på siden **Administrer adresser**.</span><span class="sxs-lookup"><span data-stu-id="2897a-126">Under the **General** tab on the **Manage addresses** page, set the sales tax value as needed.</span></span>

> [!NOTE]
> <span data-ttu-id="2897a-127">Momsgruppen defineres ved hjælp af leveringsadressen for ordrelinjen, og den destinationsbaserede moms konfigureres i selve momsgruppen.</span><span class="sxs-lookup"><span data-stu-id="2897a-127">The tax group is defined using the delivery address of the order line and the destination-based taxes are configured at the tax group itself.</span></span> <span data-ttu-id="2897a-128">Du kan finde flere oplysninger i [Konfigurere moms for onlinebutikker, der er baseret på destinationen](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span><span class="sxs-lookup"><span data-stu-id="2897a-128">For more information, see [Set up taxes for online stores based on destination](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span></span>

## <a name="order-pickup-in-store"></a><span data-ttu-id="2897a-129">Ordreafhentning i butik</span><span class="sxs-lookup"><span data-stu-id="2897a-129">Order pickup in store</span></span>

<span data-ttu-id="2897a-130">For ordrelinjer, hvor der er angivet afhentning i butik eller ved fortovskant, anvendes momsgruppen fra den valgte afhentningsbutik.</span><span class="sxs-lookup"><span data-stu-id="2897a-130">For order lines with pickup in store or curbside pickup specified, the tax group from the selected pickup store will be applied.</span></span> <span data-ttu-id="2897a-131">Du kan finde flere oplysninger om, hvordan du konfigurerer momsgruppen for en bestemt butik, i [Angive andre momsindstillinger for butikker](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span><span class="sxs-lookup"><span data-stu-id="2897a-131">For details about how to configure the tax group for a given store, see [Set other tax options for stores](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span></span>

> [!NOTE]
> <span data-ttu-id="2897a-132">Når en ordrelinje afhentes i en butik, vil en kundes indstillinger for adressemoms (hvis de er angivet) blive ignoreret af momsprogrammet, og afhentningsbutikkens momskonfiguration vil blive anvendt.</span><span class="sxs-lookup"><span data-stu-id="2897a-132">When an order line is picked up at a store, a customer's address tax settings (if set up) will be ignored by the tax engine and the pickup store's tax configuration will be applied.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="2897a-133">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="2897a-133">Additional resources</span></span>

[<span data-ttu-id="2897a-134">Momsoversigt</span><span class="sxs-lookup"><span data-stu-id="2897a-134">Sales tax overview</span></span>](https://docs.microsoft.com/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="2897a-135">Momsberegningsmetoder i feltet Grundlag</span><span class="sxs-lookup"><span data-stu-id="2897a-135">Sales tax calculation methods in the Origin field</span></span>](https://docs.microsoft.com/dynamics365/finance/general-ledger/sales-tax-calculation-methods-origin-field?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="2897a-136">Tildeling og tilsidesættelser af moms</span><span class="sxs-lookup"><span data-stu-id="2897a-136">Sales tax assignment and overrides</span></span>](https://docs.microsoft.com/dynamics365/supply-chain/procurement/tasks/sales-tax-assignment-overrides?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="2897a-137">Indstillinger for beregning af hele beløbet og intervaller for momskoder</span><span class="sxs-lookup"><span data-stu-id="2897a-137">Whole amount and Interval calculation options for sales tax codes</span></span>](https://docs.microsoft.com/dynamics365/finance/general-ledger/whole-amount-interval-options-sales-tax-codes?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="2897a-138">Beregning af momsfritagelse</span><span class="sxs-lookup"><span data-stu-id="2897a-138">Calculation of tax exemption</span></span>](tax-exempt-price-inclusive.md) 



[!INCLUDE[footer-include](../includes/footer-banner.md)]