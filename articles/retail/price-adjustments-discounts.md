---
title: Prisjusteringer og rabatter
description: Denne artikel indeholder oplysninger om prisjusteringer og rabatter i Microsoft Dynamics 365 for Retail.
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c96f7afdb095fd45b5dd88c7760a24226518f61c
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---

# <a name="price-adjustments-and-discounts"></a><span data-ttu-id="5641e-103">Prisjusteringer og rabatter</span><span class="sxs-lookup"><span data-stu-id="5641e-103">Price adjustments and discounts</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="5641e-104">Denne artikel indeholder oplysninger om prisjusteringer og rabatter i Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="5641e-104">This article provides information about price adjustments and discounts in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="5641e-105">I Dynamics 365 for Retail kan du foretage prisreguleringer i forhold til produkter, og du kan også konfigurere rabatter, der gælder for en varelinje eller en transaktion på salgsstedet (POS), i salgsordren for et callcenter eller i en onlineordre.</span><span class="sxs-lookup"><span data-stu-id="5641e-105">In Dynamics 365 for Retail, you can make price adjustments to products, and can also set up discounts that are applied to a line item or a transaction at the point of sale (POS), in a call center sales order, or in an online order.</span></span> <span data-ttu-id="5641e-106">Både prisjusteringer og rabatter kan være knyttet til prisgrupper.</span><span class="sxs-lookup"><span data-stu-id="5641e-106">Both price adjustments and discounts can be linked to price groups.</span></span> <span data-ttu-id="5641e-107">Du kan angive en enkelt startdato og slutdato eller en tilbagevendende periode, en rabatkode og et par ekstra attributter for både prisjusteringer og rabatter.</span><span class="sxs-lookup"><span data-stu-id="5641e-107">For both price adjustments and discounts, you can specify a single start date and end date or a reoccurring period, a discount code, and a few additional attributes.</span></span> <span data-ttu-id="5641e-108">Prisjusteringer og rabatter kan anvendes på produkter, varianter eller kategorier.</span><span class="sxs-lookup"><span data-stu-id="5641e-108">Price adjustments and discounts can be applied to products, variants, or categories.</span></span> <span data-ttu-id="5641e-109">Hvis mere end én rabat gælder for et produkt, kan en kunde måske modtage enten en af rabatterne eller en kombineret rabat, afhængigt af konfigurationen af rabatten.</span><span class="sxs-lookup"><span data-stu-id="5641e-109">If more than one discount applies to a product, a customer might receive either one of the discounts or a combined discount, depending on the configuration of the discount.</span></span> <span data-ttu-id="5641e-110">Dynamics 365 for Retail anvender automatisk rabatten eller den kombination af rabatter, som giver den bedste pris til kunden.</span><span class="sxs-lookup"><span data-stu-id="5641e-110">Dynamics 365 for Retail automatically applies the discount or combination of discounts that gives the best price to the customer.</span></span> <span data-ttu-id="5641e-111">Når du opretter en prisjustering eller rabat, skal du kontrollere, at prisgrupper er knyttet til de korrekte kanaler, kataloger, tilhørsforhold eller loyalitetsprogrammer, som du ønsker, at rabatten skal gælde for.</span><span class="sxs-lookup"><span data-stu-id="5641e-111">When you set up a price adjustment or a discount, be sure to confirm that price groups are assigned to the correct channels, catalogs, affiliations, or loyalty programs that you want the discount to apply to.</span></span> <span data-ttu-id="5641e-112">Derudover er det sådan, at hvis du vil oprette rabat-id'et automatisk, kan du oprette nummerserier på siden **Detailparametre**, inden du definerer en ny prisjustering eller rabat.</span><span class="sxs-lookup"><span data-stu-id="5641e-112">Additionally, if you want to automatically generate the discount ID, set up number sequences on the **Retail parameters** page before you define a new price adjustment or discount.</span></span> <span data-ttu-id="5641e-113">**Bemærk!** Du kan slette en prisjustering eller en rabat.</span><span class="sxs-lookup"><span data-stu-id="5641e-113">**Note:** You can delete a price adjustment or a discount.</span></span> <span data-ttu-id="5641e-114">Statistiske oplysninger går imidlertid tabt.</span><span class="sxs-lookup"><span data-stu-id="5641e-114">However, statistical information will be lost.</span></span>

### <a name="types-of-discounts"></a><span data-ttu-id="5641e-115">Rabattyper</span><span class="sxs-lookup"><span data-stu-id="5641e-115">Types of discounts</span></span>

<span data-ttu-id="5641e-116">Der findes fire typer detailrabatter:</span><span class="sxs-lookup"><span data-stu-id="5641e-116">There are four types of retail discounts:</span></span>

-   <span data-ttu-id="5641e-117">**Enkel rabat** – en enkelt procent eller beløb.</span><span class="sxs-lookup"><span data-stu-id="5641e-117">**Simple discount** – A single percentage or amount.</span></span>
-   <span data-ttu-id="5641e-118">**Mængderabat** – En rabat, der anvendes, når to eller flere produkter købes.</span><span class="sxs-lookup"><span data-stu-id="5641e-118">**Quantity discount** – A discount that is applied when two or more products are purchased.</span></span>
-   <span data-ttu-id="5641e-119">**Mix og match-rabat** – En rabat, der anvendes, når der købes en specifik kombination af produkter.</span><span class="sxs-lookup"><span data-stu-id="5641e-119">**Mix and match discount** – A discount that is applied when a specific combination of products is purchased.</span></span>
-   <span data-ttu-id="5641e-120">**Tærskelrabat** – En rabat, der anvendes, når totalen for transaktionen er mere end et bestemt beløb.</span><span class="sxs-lookup"><span data-stu-id="5641e-120">**Threshold discount** – A discount that is applied when the transaction total is more than a specified amount.</span></span>

<span data-ttu-id="5641e-121">Både prisjusteringer og rabatter kan være knyttet til prisgrupper.</span><span class="sxs-lookup"><span data-stu-id="5641e-121">Both price adjustments and discounts can be associated with price groups.</span></span> <span data-ttu-id="5641e-122">Prisgrupper kan derefter tilknyttes kanaler, kataloger, tilhørsforhold og loyalitetsprogrammer.</span><span class="sxs-lookup"><span data-stu-id="5641e-122">Price groups can then be associated with channels, catalogs, affiliations, and loyalty programs.</span></span>




