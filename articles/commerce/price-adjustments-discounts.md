---
title: Prisjusteringer og rabatter
description: Denne artikel indeholder oplysninger om prisjusteringer og rabatter i Dynamics 365 Commerce.
author: scott-tucker
manager: AnnBe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 0c2adaa5cd935d5b593bfbb3215d3466fcafab7b
ms.sourcegitcommit: 1d74636bf9db5fb33e998322899504b709b4f89f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/19/2020
ms.locfileid: "4584309"
---
# <a name="price-adjustments-and-discounts"></a><span data-ttu-id="7568d-103">Prisjusteringer og rabatter</span><span class="sxs-lookup"><span data-stu-id="7568d-103">Price adjustments and discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7568d-104">Denne artikel indeholder oplysninger om prisjusteringer og rabatter i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7568d-104">This article provides information about price adjustments and discounts in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="7568d-105">I Commerce kan du foretage prisjusteringer af produkter, og du kan også konfigurere rabatter, der anvendes på et linjeelement eller en transaktion på POS, i et callcenters salgsordre eller i en onlineordre.</span><span class="sxs-lookup"><span data-stu-id="7568d-105">In Commerce, you can make price adjustments to products, and can also set up discounts that are applied to a line item or a transaction at the point of sale (POS), in a call center sales order, or in an online order.</span></span> <span data-ttu-id="7568d-106">Både prisjusteringer og rabatter kan være knyttet til prisgrupper.</span><span class="sxs-lookup"><span data-stu-id="7568d-106">Both price adjustments and discounts can be linked to price groups.</span></span> <span data-ttu-id="7568d-107">Du kan angive en enkelt startdato og slutdato eller en tilbagevendende periode, en rabatkode og et par ekstra attributter for både prisjusteringer og rabatter.</span><span class="sxs-lookup"><span data-stu-id="7568d-107">For both price adjustments and discounts, you can specify a single start date and end date or a reoccurring period, a discount code, and a few additional attributes.</span></span> 

<span data-ttu-id="7568d-108">Prisjusteringer og rabatter kan anvendes på produkter, varianter eller kategorier.</span><span class="sxs-lookup"><span data-stu-id="7568d-108">Price adjustments and discounts can be applied to products, variants, or categories.</span></span> <span data-ttu-id="7568d-109">Hvis mere end én rabat gælder for et produkt, kan en kunde måske modtage enten en af rabatterne eller en kombineret rabat, afhængigt af konfigurationen af rabatten.</span><span class="sxs-lookup"><span data-stu-id="7568d-109">If more than one discount applies to a product, a customer might receive either one of the discounts or a combined discount, depending on the configuration of the discount.</span></span> <span data-ttu-id="7568d-110">Commerce anvender automatisk rabatten eller den kombination af rabatter, som giver den bedste pris til kunden.</span><span class="sxs-lookup"><span data-stu-id="7568d-110">Commerce automatically applies the discount or combination of discounts that gives the best price to the customer.</span></span> <span data-ttu-id="7568d-111">Når du opretter en prisjustering eller rabat, skal du kontrollere, at prisgrupper er knyttet til de korrekte kanaler, kataloger, tilhørsforhold eller loyalitetsprogrammer, som du ønsker, at rabatten skal gælde for.</span><span class="sxs-lookup"><span data-stu-id="7568d-111">When you set up a price adjustment or a discount, be sure to confirm that price groups are assigned to the correct channels, catalogs, affiliations, or loyalty programs that you want the discount to apply to.</span></span> <span data-ttu-id="7568d-112">Derudover er det sådan, at hvis du vil oprette rabat-id'et automatisk, kan du oprette nummerserier på siden **Commerce-parametre**, inden du definerer en ny prisjustering eller rabat.</span><span class="sxs-lookup"><span data-stu-id="7568d-112">Additionally, if you want to automatically generate the discount ID, set up number sequences on the **Commerce parameters** page before you define a new price adjustment or discount.</span></span>

> [!NOTE]
> <span data-ttu-id="7568d-113">Du kan slette en prisjustering eller en rabat.</span><span class="sxs-lookup"><span data-stu-id="7568d-113">You can delete a price adjustment or a discount.</span></span> <span data-ttu-id="7568d-114">Statistiske oplysninger går imidlertid tabt.</span><span class="sxs-lookup"><span data-stu-id="7568d-114">However, statistical information will be lost.</span></span>

## <a name="types-of-discounts"></a><span data-ttu-id="7568d-115">Rabattyper</span><span class="sxs-lookup"><span data-stu-id="7568d-115">Types of discounts</span></span>

<span data-ttu-id="7568d-116">Der findes mange typer rabatter:</span><span class="sxs-lookup"><span data-stu-id="7568d-116">There are many types of discounts:</span></span>

- <span data-ttu-id="7568d-117">**Enkel rabat** – en enkelt procent eller beløb.</span><span class="sxs-lookup"><span data-stu-id="7568d-117">**Simple discount** – A single percentage or amount.</span></span>
- <span data-ttu-id="7568d-118">**Mængderabat** – En rabat, der anvendes, når to eller flere produkter købes.</span><span class="sxs-lookup"><span data-stu-id="7568d-118">**Quantity discount** – A discount that is applied when two or more products are purchased.</span></span>
- <span data-ttu-id="7568d-119">**Mix og match-rabat** – En rabat, der anvendes, når der købes en specifik kombination af produkter.</span><span class="sxs-lookup"><span data-stu-id="7568d-119">**Mix and match discount** – A discount that is applied when a specific combination of products is purchased.</span></span>
- <span data-ttu-id="7568d-120">**Tærskelrabat** – En rabat, der anvendes, når totalen for transaktionen er mere end et bestemt beløb.</span><span class="sxs-lookup"><span data-stu-id="7568d-120">**Threshold discount** – A discount that is applied when the transaction total is more than a specified amount.</span></span>
- <span data-ttu-id="7568d-121">**Betalingsmiddelbaserede rabatter** – En rabat, der anvendes, når totalen for transaktionen overstiger et angivet beløb, og når en bestemt betalingstype (f.eks. kontant, kredit- eller debetkort) bruges til betaling.</span><span class="sxs-lookup"><span data-stu-id="7568d-121">**Tender-based discount** – A discount that is applied when the transaction total is more than a specified amount and a specific payment type (for example, cash, credit, or debit card) is used for payment.</span></span>
- <span data-ttu-id="7568d-122">**Forsendelsesrabat** – En rabat, der anvendes, når totalen for transaktionen overstiger et angivet beløb, og når en bestemt leveringsmåde (f.eks. forsendelser over to dage eller samme dag) bruges i ordren.</span><span class="sxs-lookup"><span data-stu-id="7568d-122">**Shipping discount** – A discount that is applied when the transaction total is more than a specified amount and a specific mode of delivery (for example, two day shipping or overnight shipping) is used on the order.</span></span>

<span data-ttu-id="7568d-123">Både prisjusteringer og rabatter kan være knyttet til prisgrupper.</span><span class="sxs-lookup"><span data-stu-id="7568d-123">Both price adjustments and discounts can be associated with price groups.</span></span> <span data-ttu-id="7568d-124">Prisgrupper kan derefter tilknyttes kanaler, kataloger, tilhørsforhold og loyalitetsprogrammer.</span><span class="sxs-lookup"><span data-stu-id="7568d-124">Price groups can then be associated with channels, catalogs, affiliations, and loyalty programs.</span></span>
