---
title: "Betalingsspærring af kreditorfakturaer i den offentlige sektor i Frankrig"
description: "De almindelige processer, der vedrører betalingsspærringer af kreditorfakturaer i Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, er suppleret for franske enheder i den offentlige sektor. I dette emne beskrives de funktioner til betalingsspærring af kreditorfakturaer, der bruges af den offentlige sektor i Frankrig."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 27331
ms.search.region: France
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: d561da4f331bd62ad74d81a5d0d6eea98fdde7d4
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="vendor-invoice-payment-holds-in-the-public-sector-in-france"></a><span data-ttu-id="9d443-104">Betalingsspærring af kreditorfakturaer i den offentlige sektor i Frankrig</span><span class="sxs-lookup"><span data-stu-id="9d443-104">Vendor invoice payment holds in the public sector in France</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="9d443-105">De almindelige processer, der vedrører betalingsspærringer af kreditorfakturaer i Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, er suppleret for franske enheder i den offentlige sektor.</span><span class="sxs-lookup"><span data-stu-id="9d443-105">The standard processes related to vendor invoice payment holds in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition are augmented for French entities in the public sector.</span></span> <span data-ttu-id="9d443-106">I dette emne beskrives de funktioner til betalingsspærring af kreditorfakturaer, der bruges af den offentlige sektor i Frankrig.</span><span class="sxs-lookup"><span data-stu-id="9d443-106">This topic describes the vendor invoice payment holds functionality used by the public sector in France.</span></span>

<a name="set-up-rules-for-vendor-invoice-payment-holds"></a><span data-ttu-id="9d443-107">Konfigurere regler for betalingsspærring af kreditorfakturaer</span><span class="sxs-lookup"><span data-stu-id="9d443-107">Set up rules for vendor invoice payment holds</span></span>
---------------------------------------------

<span data-ttu-id="9d443-108">Regler for betalingsspærring af kreditorfakturaer er angivet i oversigtspanelet **På hold** på siden **Betalingsbetingelser**.</span><span class="sxs-lookup"><span data-stu-id="9d443-108">Rules for vendor invoice payment holds are set up on the **Hold** FastTab on the **Terms of payment** page.</span></span> <span data-ttu-id="9d443-109">Hver regel har tre dele:</span><span class="sxs-lookup"><span data-stu-id="9d443-109">Each rule has three parts:</span></span>

-   <span data-ttu-id="9d443-110">En brugerrolle, som f.eks. bogholder, regnskabschef eller controller.</span><span class="sxs-lookup"><span data-stu-id="9d443-110">A user role, such as accountant, accounting manager, or controller.</span></span> <span data-ttu-id="9d443-111">Kun brugere, der er tildelt den angivne rolle, kan spærre eller frigive en betaling i henhold til de angivne betalingsbetingelser.</span><span class="sxs-lookup"><span data-stu-id="9d443-111">Only users who are assigned the specified role can hold or release a payment under the specified terms of payment.</span></span>
-   <span data-ttu-id="9d443-112">Minimum antal dage, der lægges til fakturabetalingens forfaldsdato, når en bruger med den valgte rolle frigiver spærringen.</span><span class="sxs-lookup"><span data-stu-id="9d443-112">The minimum number of days that will be added to the invoice payment due date when a user with the selected role releases the hold.</span></span>
-   <span data-ttu-id="9d443-113">Det maks. antal gange, som bruger med den valgte rolle kan spærre en betaling på hver faktura.</span><span class="sxs-lookup"><span data-stu-id="9d443-113">The maximum number of times that a user with the selected role can hold a payment on each invoice.</span></span> <span data-ttu-id="9d443-114">**Tip**! Hvis du vil tillade ubegrænsede spærringer, skal du angive et højt tal, f.eks. 9999.</span><span class="sxs-lookup"><span data-stu-id="9d443-114">**Tip**: To allow unlimited holds, enter a large number, such as 9999.</span></span>

<span data-ttu-id="9d443-115">For eksempel på Net 30 betalingsbetingelsen kan du oprette to regler, én for bogholdere og én til direktører.</span><span class="sxs-lookup"><span data-stu-id="9d443-115">For example, on the Net 30 term of payment, you might create two rules, one for accountants and one for directors.</span></span> <span data-ttu-id="9d443-116">Reglen for bogholdere føjer mindst 30 dage til fakturabetalingens forfaldsdato, hvor spærringen frigives, og tillader maksimalt 3 spærringer på en faktura.</span><span class="sxs-lookup"><span data-stu-id="9d443-116">The rule for accountants adds a minimum of 30 days to the invoice payment due date when the hold is released, and allows a maximum of 3 holds on an invoice.</span></span> <span data-ttu-id="9d443-117">Reglen for direktører føjer mindst 15 dage til forfaldsdatoen for betaling af fakturaen, med højst 10 spærringer på en faktura.</span><span class="sxs-lookup"><span data-stu-id="9d443-117">The rule for directors adds a minimum of 15 days to the invoice payment due date, with a maximum of 10 holds on an invoice.</span></span>

## <a name="when-can-i-place-and-release-vendor-invoice-payment-holds"></a><span data-ttu-id="9d443-118">Hvornår kan jeg angive og frigive betalingsspærringer for kreditorfakturaer?</span><span class="sxs-lookup"><span data-stu-id="9d443-118">When can I place and release vendor invoice payment holds?</span></span>
<span data-ttu-id="9d443-119">Spærringer kan angives og frigives i følgende situationer:</span><span class="sxs-lookup"><span data-stu-id="9d443-119">Holds can be placed and released in the following circumstances:</span></span>

-   <span data-ttu-id="9d443-120">Betalingsbetingelser skal konfigureres for en kreditorfaktura, eller for alle kreditorfakturaer for en bestemt kreditor, før du kan angive en spærring.</span><span class="sxs-lookup"><span data-stu-id="9d443-120">Payment terms must be set up for a vendor invoice, or for all vendor invoices for a specific vendor, before you can place a hold.</span></span>
-   <span data-ttu-id="9d443-121">For at angive eller frigive en spærring skal du være tildelt en brugerrolle, hvor der er konfigureret regler for betalingsspærringer.</span><span class="sxs-lookup"><span data-stu-id="9d443-121">To place or release a hold, you must be assigned to a user role where rules have been set up for payment holds.</span></span>
-   <span data-ttu-id="9d443-122">Hvis en spærring er aktiv for en kreditor, kan du ikke frigive en spærring for en faktura for den samme kreditor.</span><span class="sxs-lookup"><span data-stu-id="9d443-122">If a hold is active for a vendor, you cannot release a hold for an invoice for that same vendor.</span></span> <span data-ttu-id="9d443-123">Først skal du frigive spærringen for kreditoren.</span><span class="sxs-lookup"><span data-stu-id="9d443-123">You must first release the hold for the vendor.</span></span>
-   <span data-ttu-id="9d443-124">Du kan ikke frigive en spærring, medmindre du er den bruger, der angav spærringen, eller du er tildelt til den samme brugerrolle som den bruger, der angav spærringen.</span><span class="sxs-lookup"><span data-stu-id="9d443-124">You cannot release a hold unless you are the user who placed the hold, or you are assigned to the same user role as the user who placed the hold.</span></span>
-   <span data-ttu-id="9d443-125">Du kan ikke bogføre en kreditorfaktura, hvis den har en betalingsspærring.</span><span class="sxs-lookup"><span data-stu-id="9d443-125">You cannot post a vendor invoice if it has a payment hold.</span></span> <span data-ttu-id="9d443-126">Spærringen skal først frigives.</span><span class="sxs-lookup"><span data-stu-id="9d443-126">The hold must first be released.</span></span>

## <a name="where-do-i-place-and-release-vendor-invoice-payment-holds"></a><span data-ttu-id="9d443-127">Hvor angiver og frigiver jeg betalingsspærringer for kreditorfakturaer?</span><span class="sxs-lookup"><span data-stu-id="9d443-127">Where do I place and release vendor invoice payment holds?</span></span>
### <a name="for-a-vendor"></a><span data-ttu-id="9d443-128">For en kreditor</span><span class="sxs-lookup"><span data-stu-id="9d443-128">For a vendor</span></span>
<span data-ttu-id="9d443-129">Angiv eller frigiv en betalingsspærring for alle fakturaer for den valgte kreditor på siden **kreditorposteringer** eller siden **Udlign posteringer**.</span><span class="sxs-lookup"><span data-stu-id="9d443-129">Place or release a payment hold for all invoices for a selected vendor on the **Vendor transactions** page or the **Settle transactions** page.</span></span> <span data-ttu-id="9d443-130">Hvis du angiver en betalingsspærring for en kreditor, omfatter denne spærring alle eksisterende fakturaer for den pågældende kreditor.</span><span class="sxs-lookup"><span data-stu-id="9d443-130">If you place a payment hold for a vendor, this hold includes all existing invoices for that vendor.</span></span> <span data-ttu-id="9d443-131">Hvis du frigiver en betalingsspærring for en kreditor, frigives denne betalingsspærring kun for de kreditorfakturaer, der ikke har individuelle betalingsspærringer.</span><span class="sxs-lookup"><span data-stu-id="9d443-131">If you release a payment hold for a vendor, this releases the payment hold only for those vendor invoices that do not have individual payment holds.</span></span> <span data-ttu-id="9d443-132">For eksempel angiver du individuelle betalingsspærringer på to forskellige kreditorfakturaer for samme kreditor.</span><span class="sxs-lookup"><span data-stu-id="9d443-132">For example, you place individual payment holds on two different vendor invoices for the same vendor.</span></span> <span data-ttu-id="9d443-133">Senere angiver du en betalingsspærring for den pågældende kreditor.</span><span class="sxs-lookup"><span data-stu-id="9d443-133">You later place a payment hold for that vendor.</span></span> <span data-ttu-id="9d443-134">Hvis du senere frigiver betalingsspærringen for den pågældende kreditor, frigives de individuelle spærringer for de to kreditorfakturaer ikke.</span><span class="sxs-lookup"><span data-stu-id="9d443-134">If you later release the payment hold for that vendor, it will not release the individual holds for the two vendor invoices.</span></span>

### <a name="for-a-vendor-invoice"></a><span data-ttu-id="9d443-135">For en kreditorfaktura</span><span class="sxs-lookup"><span data-stu-id="9d443-135">For a vendor invoice</span></span>

<span data-ttu-id="9d443-136">Angiv eller frigiv en betalingsspærring for en enkelt faktura på siden **Kreditorfaktura** eller siden **Udlign posteringer**.</span><span class="sxs-lookup"><span data-stu-id="9d443-136">Place or release a payment hold for a single invoice on the **Vendor invoice** page or the **Settle transactions** page.</span></span>

### <a name="for-a-posted-vendor-invoice"></a><span data-ttu-id="9d443-137">For en bogført kreditorfaktura</span><span class="sxs-lookup"><span data-stu-id="9d443-137">For a posted vendor invoice</span></span>

<span data-ttu-id="9d443-138">Angiv eller frigiv en betalingsspærring for en bogført kreditorfaktura på siden **Fakturajournal**.</span><span class="sxs-lookup"><span data-stu-id="9d443-138">Place or release a payment hold for a posted vendor invoice on the **Invoice journal** page.</span></span>

### <a name="for-all-vendor-invoices-associated-with-a-purchase-order"></a><span data-ttu-id="9d443-139">For alle kreditorfakturaer, der er tilknyttet en indkøbsordre</span><span class="sxs-lookup"><span data-stu-id="9d443-139">For all vendor invoices associated with a purchase order</span></span>

<span data-ttu-id="9d443-140">Angiv eller frigiv en betalingsspærring for alle kreditorfakturaer, der er tilknyttet en indkøbsordre på siden **Udlign posteringer**.</span><span class="sxs-lookup"><span data-stu-id="9d443-140">Place or release a payment hold for all vendor invoices that are associated with a purchase order on the **Settle transactions** page.</span></span>

## <a name="can-i-settle-an-invoice-that-is-on-hold"></a><span data-ttu-id="9d443-141">Kan jeg udligne en faktura, der er spærret?</span><span class="sxs-lookup"><span data-stu-id="9d443-141">Can I settle an invoice that is on hold?</span></span>
<span data-ttu-id="9d443-142">Hvis du er tildelt til den samme brugerrolle som den bruger, der angav spærringen, kan du fjerne spærringen fra siden **Udlign posteringer** og udligne kreditorfakturaen.</span><span class="sxs-lookup"><span data-stu-id="9d443-142">If you are assigned to the same user role as the user who placed the hold, you can clear the hold from the **Settle transactions** page and settle the vendor invoice.</span></span> <span data-ttu-id="9d443-143">Når du angiver en betalingsspærring, vælges indstillingen **Fakturabetaling på hold** automatisk under fanen **Betaling** på siden **Udlign posteringer**.</span><span class="sxs-lookup"><span data-stu-id="9d443-143">When you place a payment hold, the **Invoice payment hold** option is automatically selected on the **Payment** tab of the **Settle transactions** page.</span></span> <span data-ttu-id="9d443-144">Dette forhindrer, at en kreditorfaktura kan udlignes, før spærringen er frigivet.</span><span class="sxs-lookup"><span data-stu-id="9d443-144">This prevents a vendor invoice from being settled until the hold is released.</span></span>




