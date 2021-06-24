---
title: Prisjusteringer og rabatter
description: Denne artikel indeholder oplysninger om prisjusteringer og rabatter i Dynamics 365 Commerce.
author: scott-tucker
ms.date: 06/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 44c03ae0a04d648e788a72d8f6dcc3671c5736c7
ms.sourcegitcommit: 7c9d6be464db058511df9cb6ba162d21dc0554e8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/11/2021
ms.locfileid: "6240936"
---
# <a name="price-adjustments-and-discounts"></a><span data-ttu-id="eb71f-103">Prisjusteringer og rabatter</span><span class="sxs-lookup"><span data-stu-id="eb71f-103">Price adjustments and discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="eb71f-104">Denne artikel indeholder oplysninger om prisjusteringer og rabatter i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="eb71f-104">This article provides information about price adjustments and discounts in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="eb71f-105">I Commerce kan du foretage prisjusteringer af produkter, og du kan også konfigurere rabatter, der anvendes på et linjeelement eller en transaktion på POS, i et callcenters salgsordre eller i en onlineordre.</span><span class="sxs-lookup"><span data-stu-id="eb71f-105">In Commerce, you can make price adjustments to products, and can also set up discounts that are applied to a line item or a transaction at the point of sale (POS), in a call center sales order, or in an online order.</span></span> <span data-ttu-id="eb71f-106">Både prisjusteringer og rabatter kan være knyttet til prisgrupper.</span><span class="sxs-lookup"><span data-stu-id="eb71f-106">Both price adjustments and discounts can be linked to price groups.</span></span> <span data-ttu-id="eb71f-107">Du kan angive en enkelt startdato og slutdato eller en tilbagevendende periode, en rabatkode og et par ekstra attributter for både prisjusteringer og rabatter.</span><span class="sxs-lookup"><span data-stu-id="eb71f-107">For both price adjustments and discounts, you can specify a single start date and end date or a reoccurring period, a discount code, and a few additional attributes.</span></span> 

<span data-ttu-id="eb71f-108">Prisjusteringer og rabatter kan anvendes på produkter, varianter eller kategorier.</span><span class="sxs-lookup"><span data-stu-id="eb71f-108">Price adjustments and discounts can be applied to products, variants, or categories.</span></span> <span data-ttu-id="eb71f-109">Hvis mere end én rabat gælder for et produkt, kan en kunde måske modtage enten en af rabatterne eller en kombineret rabat, afhængigt af konfigurationen af rabatten.</span><span class="sxs-lookup"><span data-stu-id="eb71f-109">If more than one discount applies to a product, a customer might receive either one of the discounts or a combined discount, depending on the configuration of the discount.</span></span> <span data-ttu-id="eb71f-110">Commerce anvender automatisk rabatten eller den kombination af rabatter, som giver den bedste pris til kunden.</span><span class="sxs-lookup"><span data-stu-id="eb71f-110">Commerce automatically applies the discount or combination of discounts that gives the best price to the customer.</span></span> <span data-ttu-id="eb71f-111">Når du opretter en prisjustering eller rabat, skal du kontrollere, at prisgrupper er knyttet til de korrekte kanaler, kataloger, tilhørsforhold eller loyalitetsprogrammer, som du ønsker, at rabatten skal gælde for.</span><span class="sxs-lookup"><span data-stu-id="eb71f-111">When you set up a price adjustment or a discount, be sure to confirm that price groups are assigned to the correct channels, catalogs, affiliations, or loyalty programs that you want the discount to apply to.</span></span> <span data-ttu-id="eb71f-112">Derudover er det sådan, at hvis du vil oprette rabat-id'et automatisk, kan du oprette nummerserier på siden **Commerce-parametre**, inden du definerer en ny prisjustering eller rabat.</span><span class="sxs-lookup"><span data-stu-id="eb71f-112">Additionally, if you want to automatically generate the discount ID, set up number sequences on the **Commerce parameters** page before you define a new price adjustment or discount.</span></span>

> [!NOTE]
> <span data-ttu-id="eb71f-113">Du kan slette en prisjustering eller en rabat.</span><span class="sxs-lookup"><span data-stu-id="eb71f-113">You can delete a price adjustment or a discount.</span></span> <span data-ttu-id="eb71f-114">Statistiske oplysninger går imidlertid tabt.</span><span class="sxs-lookup"><span data-stu-id="eb71f-114">However, statistical information will be lost.</span></span>

## <a name="types-of-discounts"></a><span data-ttu-id="eb71f-115">Rabattyper</span><span class="sxs-lookup"><span data-stu-id="eb71f-115">Types of discounts</span></span>

<span data-ttu-id="eb71f-116">Der findes mange typer rabatter:</span><span class="sxs-lookup"><span data-stu-id="eb71f-116">There are many types of discounts:</span></span>

- <span data-ttu-id="eb71f-117">**Enkel rabat** – en enkelt procent eller beløb.</span><span class="sxs-lookup"><span data-stu-id="eb71f-117">**Simple discount** – A single percentage or amount.</span></span>
- <span data-ttu-id="eb71f-118">**Mængderabat** – En rabat, der anvendes, når to eller flere produkter købes.</span><span class="sxs-lookup"><span data-stu-id="eb71f-118">**Quantity discount** – A discount that is applied when two or more products are purchased.</span></span>
- <span data-ttu-id="eb71f-119">**Mix og match-rabat** – En rabat, der anvendes, når der købes en specifik kombination af produkter.</span><span class="sxs-lookup"><span data-stu-id="eb71f-119">**Mix and match discount** – A discount that is applied when a specific combination of products is purchased.</span></span>
- <span data-ttu-id="eb71f-120">**Tærskelrabat** – En rabat, der anvendes, når totalen for transaktionen er mere end et bestemt beløb.</span><span class="sxs-lookup"><span data-stu-id="eb71f-120">**Threshold discount** – A discount that is applied when the transaction total is more than a specified amount.</span></span>
- <span data-ttu-id="eb71f-121">**Betalingsmiddelbaserede rabatter** – En rabat, der anvendes, når totalen for transaktionen overstiger et angivet beløb, og når en bestemt betalingstype (f.eks. kontant, kredit- eller debetkort) bruges til betaling.</span><span class="sxs-lookup"><span data-stu-id="eb71f-121">**Tender-based discount** – A discount that is applied when the transaction total is more than a specified amount and a specific payment type (for example, cash, credit, or debit card) is used for payment.</span></span>
- <span data-ttu-id="eb71f-122">**Forsendelsesrabat** – En rabat, der anvendes, når totalen for transaktionen overstiger et angivet beløb, og når en bestemt leveringsmåde (f.eks. forsendelser over to dage eller samme dag) bruges i ordren.</span><span class="sxs-lookup"><span data-stu-id="eb71f-122">**Shipping discount** – A discount that is applied when the transaction total is more than a specified amount and a specific mode of delivery (for example, two day shipping or overnight shipping) is used on the order.</span></span>

<span data-ttu-id="eb71f-123">Både prisjusteringer og rabatter kan være knyttet til prisgrupper.</span><span class="sxs-lookup"><span data-stu-id="eb71f-123">Both price adjustments and discounts can be associated with price groups.</span></span> <span data-ttu-id="eb71f-124">Prisgrupper kan derefter tilknyttes kanaler, kataloger, tilhørsforhold og loyalitetsprogrammer.</span><span class="sxs-lookup"><span data-stu-id="eb71f-124">Price groups can then be associated with channels, catalogs, affiliations, and loyalty programs.</span></span>

> [!NOTE]
> <span data-ttu-id="eb71f-125">Mix og match-rabatten og tærskelrabatten har egenskaber med henholdsvis navnet "Optæl produkter uden rabat" og "Optæl produkter uden rabat i forhold til tærskel".</span><span class="sxs-lookup"><span data-stu-id="eb71f-125">The mix and match discount and the threshold discount have properties named "Count non-discountable products" and "Count non-discountable products towards threshold", respectively.</span></span> <span data-ttu-id="eb71f-126">Hvis disse egenskaber er aktiveret, kan en vare, der ikke er berettiget til rabat, stadig være med til at kvalificere en transaktion til rabatten, men den ikke-berettigede vare kan ikke få rabatten.</span><span class="sxs-lookup"><span data-stu-id="eb71f-126">If these properties are enabled, an item that is not eligible for any discount can still help qualify a transaction for the discount, but the ineligible item will not get the discount.</span></span> 
> 
> <span data-ttu-id="eb71f-127">Hvis du f.eks. opretter en mix og match-rabat med to linjer, A og B, hvor en kunde skal have 10 % rabat på begge varer, men vare A har konfigurationen "Undgå alle rabatter" markeret, vil det typisk forhindre vare A i at blive medtaget i rabatten.</span><span class="sxs-lookup"><span data-stu-id="eb71f-127">For example, if you create a mix and match discount with two lines, A and B, where a customer should get 10% off on both items, but item A has the configuration "Prevent all discounts" checked, then this would typically stop item A from being included in the discount.</span></span> <span data-ttu-id="eb71f-128">Men hvis egenskaben "Optæl produkter uden rabat" er aktiveret, kan vare A bruges til at kvalificere til mix og match-rabatten, men rabatten på 10 % anvendes kun på vare B. Lignende logik gælder for tærskelrabatten.</span><span class="sxs-lookup"><span data-stu-id="eb71f-128">However, if the "Count non-discountable products" property is enabled, then item A can be used to qualify for the mix and match discount, but the 10% discount will only be applied to item B. Similar logic applies to the threshold discount.</span></span> 
>
> <span data-ttu-id="eb71f-129">Egenskaben "Optæl produkter uden rabat i forhold til tærskel" har dog en ekstra egenskab, når den sammenlignes med egenskaben "Optæl produkter uden rabat" for mix og match-rabatter.</span><span class="sxs-lookup"><span data-stu-id="eb71f-129">However, the property "Count non-discountable products towards threshold" has an additional capability when compared to the "Count non-discountable products" property of the mix and match discounts.</span></span> <span data-ttu-id="eb71f-130">Hvis tærskelrabatten er aktiveret, og hvis der er en vare med en eksisterende rabat, som kan forhindre varen i at få andre rabatter, vil den pris, der er betalt for denne vare, være kvalificeret til at nå tærsklen, men denne vare får ikke den ekstra rabat.</span><span class="sxs-lookup"><span data-stu-id="eb71f-130">If the threshold discount is enabled, and if there is an item that has an existing discount which would prevent the item from any other discounts, then  the price paid for this item would qualify towards meeting the threshold, but this item will not get the additional discount.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
