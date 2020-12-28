---
title: Lokalisere fejl i priser, rabatter og aftaler
description: Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med priser, rabatter og aftaler.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: b4349eeba285492202b5df8481b277a06708a4c8
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4425052"
---
# <a name="troubleshoot-prices-discounts-agreements-and-rebates"></a><span data-ttu-id="d0213-103">Lokalisere fejl i priser, rabatter og aftaler</span><span class="sxs-lookup"><span data-stu-id="d0213-103">Troubleshoot prices, discounts, agreements, and rebates</span></span>

<span data-ttu-id="d0213-104">Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med priser, rabatter og aftaler.</span><span class="sxs-lookup"><span data-stu-id="d0213-104">This topic describes how to fix issues that you might encounter while you work with prices, discounts, agreements, and rebates.</span></span>

## <a name="i-cant-link-a-purchase-agreement-to-a-purchase-order-line-after-the-purchase-order-is-created"></a><span data-ttu-id="d0213-105">Jeg kan ikke knytte en købsaftale til en indkøbsordrelinje, når indkøbsordren er oprettet.</span><span class="sxs-lookup"><span data-stu-id="d0213-105">I can't link a purchase agreement to a purchase order line after the purchase order is created.</span></span>

<span data-ttu-id="d0213-106">En købsaftale skal knyttes til en indkøbsordre, når indkøbsordren oprettes.</span><span class="sxs-lookup"><span data-stu-id="d0213-106">A purchase agreement must be associated with a purchase order when the purchase order is created.</span></span> <span data-ttu-id="d0213-107">Ellers kan indkøbsordrelinjer ikke knyttes til købsaftalelinjer.</span><span class="sxs-lookup"><span data-stu-id="d0213-107">Otherwise, purchase order lines can't be associated with purchase agreement lines.</span></span>

## <a name="what-check-triggers-the-update-prices-and-discounts-entered-manually-or-external-document-message"></a><span data-ttu-id="d0213-108">Hvilken kontrol aktiverer meddelelsen "Opdater priser og rabatter, der er angivet manuelt eller med et eksternt dokument"?</span><span class="sxs-lookup"><span data-stu-id="d0213-108">What check triggers the "Update prices and discounts entered manually or external document" message?</span></span>

<span data-ttu-id="d0213-109">Når du ændrer afsendelsesdatoen, kan du få vist en meddelelse, der angiver "Opdater priser og rabatter, der er angivet manuelt eller med et eksternt dokument".</span><span class="sxs-lookup"><span data-stu-id="d0213-109">When you change the shipping date, you might receive a message that states, "Update prices and discounts entered manually or external document."</span></span> <span data-ttu-id="d0213-110">Du modtager denne meddelelse, for hvis afsendelsesdatoen ændres, kan en anden samhandels- eller salgsaftale udløses og forårsage en prisændring.</span><span class="sxs-lookup"><span data-stu-id="d0213-110">You receive this message because, if the shipping date is changed, a different trade or sales agreement might be triggered and cause a price change.</span></span> <span data-ttu-id="d0213-111">En ændring af afsendelsesdatoen kan også påvirke lagertidsplaner og andre relaterede oplysninger.</span><span class="sxs-lookup"><span data-stu-id="d0213-111">A change to the shipping date can also affect warehouse schedules and other related information.</span></span>

<span data-ttu-id="d0213-112">Meddelelsen udløses, hver gang en af datoerne eller andre parametre ændres.</span><span class="sxs-lookup"><span data-stu-id="d0213-112">The message is triggered whenever any of the dates or some other parameters are changed.</span></span> <span data-ttu-id="d0213-113">Formålet med meddelelsen er at sikre, at du er opmærksom på prisændringer, der kan forekomme på grund af disse ændringer.</span><span class="sxs-lookup"><span data-stu-id="d0213-113">The purpose of the message is to make sure that you're aware of price changes that can occur because of those changes.</span></span>

<span data-ttu-id="d0213-114">Meddelelsen er anmodningen om evaluering af samhandelsaftalen.</span><span class="sxs-lookup"><span data-stu-id="d0213-114">The message is the trade agreement evaluation (TAE) prompt.</span></span> <span data-ttu-id="d0213-115">En fuldstændig beskrivelse finder du i [Politikker til evaluering af samhandelsaftale](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper).</span><span class="sxs-lookup"><span data-stu-id="d0213-115">For a full description, see [Trade agreement evaluation policies](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper).</span></span>

## <a name="a-purchase-order-receipt-doesnt-include-all-charges"></a><span data-ttu-id="d0213-116">En købsordrekvittering omfatter ikke alle gebyrer.</span><span class="sxs-lookup"><span data-stu-id="d0213-116">A purchase order receipt doesn't include all charges.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="d0213-117">Genskabe problemet</span><span class="sxs-lookup"><span data-stu-id="d0213-117">Reproduce the issue</span></span>

<span data-ttu-id="d0213-118">Følgende procedurer viser en måde at genskabe problemet på.</span><span class="sxs-lookup"><span data-stu-id="d0213-118">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="d0213-119">På siden **Indkøbs- og forsyningsparametre** skal du under fanen **Levering** kontrollere, at indstillingen **Generér gebyrer på produktkvittering** er angivet til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="d0213-119">On the **Procurement and sourcing parameters** page, on the **Delivery** tab, make sure that the **Generate charges on product receipt** option is set to *Yes*.</span></span>
1. <span data-ttu-id="d0213-120">Opret en indkøbsordre, der inkluderer gebyrer.</span><span class="sxs-lookup"><span data-stu-id="d0213-120">Create a purchase order that includes charges.</span></span>
1. <span data-ttu-id="d0213-121">Bekræft indkøbsordren.</span><span class="sxs-lookup"><span data-stu-id="d0213-121">Confirm the purchase order.</span></span>
1. <span data-ttu-id="d0213-122">Modtag indkøbsordren.</span><span class="sxs-lookup"><span data-stu-id="d0213-122">Receive the purchase order.</span></span>
1. <span data-ttu-id="d0213-123">Kig på den kvitteringstotalen, og sammenlign den med den forventede total.</span><span class="sxs-lookup"><span data-stu-id="d0213-123">Look at the receipt total, and compare it to the expected total.</span></span>
1. <span data-ttu-id="d0213-124">Bemærk, at ikke alle gebyrer er medtaget i købsordrekvitteringen.</span><span class="sxs-lookup"><span data-stu-id="d0213-124">Notice that not all the charges are included on the purchase order receipt.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="d0213-125">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="d0213-125">Issue resolution</span></span>

<span data-ttu-id="d0213-126">Løsningen afhænger af den måde, som de forskellige gebyrer er konfigureret på.</span><span class="sxs-lookup"><span data-stu-id="d0213-126">The resolution depends on the way that the miscellaneous charges have been set up.</span></span> <span data-ttu-id="d0213-127">Du kan finde oplysninger om, hvordan du konfigurerer gebyrer, så de opfylder dine behov, i følgende blogindlæg: [Bogføre diverse gebyrer på tidspunktet for produktmodtagelse](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span><span class="sxs-lookup"><span data-stu-id="d0213-127">For information about how to set up miscellaneous charges to meet your requirements, see the following blog post: [Post misc. charges at time of product receipt](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span></span>

## <a name="trade-agreement-prices-and-discounts-arent-applied-on-sales-or-purchase-order-lines-that-are-imported-through-data-management"></a><span data-ttu-id="d0213-128">Priser og rabatter i samhandelsaftaler anvendes ikke på salgs- eller indkøbsordrelinjer, der er importeret via Dataadministration.</span><span class="sxs-lookup"><span data-stu-id="d0213-128">Trade agreement prices and discounts aren't applied on sales or purchase order lines that are imported through data management.</span></span>

### <a name="issue-description"></a><span data-ttu-id="d0213-129">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="d0213-129">Issue description</span></span>

<span data-ttu-id="d0213-130">Samhandelsaftaler, der anvendes på salgs- eller indkøbsordrelinjer, gælder ikke på linjer, der er importeret via Dataadministration.</span><span class="sxs-lookup"><span data-stu-id="d0213-130">Trade agreements that are applicable to sales or purchase order lines aren't applied on lines that are imported through data management.</span></span> <span data-ttu-id="d0213-131">De samme samhandelsaftaler anvendes dog på salgs- eller indkøbsordrelinjer, der er oprettet manuelt.</span><span class="sxs-lookup"><span data-stu-id="d0213-131">However, the same trade agreements are applied on sales or purchase order lines that are manually created.</span></span>

### <a name="reason-for-the-issue"></a><span data-ttu-id="d0213-132">Årsag til problemet</span><span class="sxs-lookup"><span data-stu-id="d0213-132">Reason for the issue</span></span>

<span data-ttu-id="d0213-133">Hvis indkøbsordrelinjer, der importeres via Dataadministration, allerede indeholder prisoplysninger, evalueres samhandelsaftalen ikke igen for disse linjer.</span><span class="sxs-lookup"><span data-stu-id="d0213-133">If purchase order lines that are imported via data management already include price information, the trade agreement won't be reevaluated for those lines.</span></span> <span data-ttu-id="d0213-134">Hvis f.eks. **Linjerabatprocent** eller nogen af pris- og rabatværdierne er angivet for en linje, vil samhandelsaftaler ikke blive slået op for denne linje.</span><span class="sxs-lookup"><span data-stu-id="d0213-134">For example, if **Line discount percentage** or any of the price and discount values is set for a line, then trade agreements will not be looked up for that line.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="d0213-135">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="d0213-135">Issue workaround</span></span>

<span data-ttu-id="d0213-136">Denne funktionsmåde forventes og er ens for både salgsordrer og indkøbsordrer.</span><span class="sxs-lookup"><span data-stu-id="d0213-136">This behavior is expected, and is similar for both sales orders and purchase orders.</span></span>

<span data-ttu-id="d0213-137">Du kan løse problemet ved at importere indkøbsordrelinjerne uden at angive prisoplysninger.</span><span class="sxs-lookup"><span data-stu-id="d0213-137">As a workaround, import the purchase order lines without setting any price information.</span></span> <span data-ttu-id="d0213-138">Samhandelsaftalerne vil derefter blive anvendt, og indkøbsordrelinjerne opdateres på baggrund af de definerede samhandelsaftaler.</span><span class="sxs-lookup"><span data-stu-id="d0213-138">The trade agreements will then be applied, and the purchase order lines will be updated based on the defined trade agreements.</span></span>

## <a name="a-vendor-rebate-isnt-cumulated-based-on-invoices"></a><span data-ttu-id="d0213-139">En leverandørrabat bliver ikke akkumuleret på basis af fakturaer.</span><span class="sxs-lookup"><span data-stu-id="d0213-139">A vendor rebate isn't cumulated based on invoices.</span></span>

### <a name="issue-description"></a><span data-ttu-id="d0213-140">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="d0213-140">Issue description</span></span>

<span data-ttu-id="d0213-141">Hvis fakturaer, der er bogført, har forskellige forfaldsdatoer, afspejles disse fakturaer ikke i de leverandørrabatter, der genereres af dem.</span><span class="sxs-lookup"><span data-stu-id="d0213-141">If invoices that are posted have different due dates, those invoices aren't reflected in vendor rebates that are generated from them.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="d0213-142">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="d0213-142">Issue resolution</span></span>

<span data-ttu-id="d0213-143">Forfaldsdatoen tages som standard ikke i betragtning, når leverandørrabatten beregnes.</span><span class="sxs-lookup"><span data-stu-id="d0213-143">By design, the due date isn't considered when the vendor rebate is calculated.</span></span> <span data-ttu-id="d0213-144">Overvej at tilpasse systemet, så forfaldsdatoen og relationen til fakturaen er mere synlig i forhold til den faktiske leverandørrabat.</span><span class="sxs-lookup"><span data-stu-id="d0213-144">Consider customizing the system so that the due date and the relation to the invoice are more apparent with respect to the actual vendor rebate.</span></span>

## <a name="unit-prices-on-purchase-orders-arent-calculated-based-on-the-unit-conversion"></a><span data-ttu-id="d0213-145">Enhedspriser på indkøbsordrer beregnes ikke ud fra enhedsomregningen.</span><span class="sxs-lookup"><span data-stu-id="d0213-145">Unit prices on purchase orders aren't calculated based on the unit conversion.</span></span>

### <a name="issue-description"></a><span data-ttu-id="d0213-146">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="d0213-146">Issue description</span></span>

<span data-ttu-id="d0213-147">Når en enhed ændres i en indkøbsordre, genberegnes priserne for samhandelsaftaler ikke ifølge definitionerne for enhedsomregning.</span><span class="sxs-lookup"><span data-stu-id="d0213-147">When a unit is changed on a purchase order, trade agreement prices aren't recalculated according to unit conversion definitions.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="d0213-148">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="d0213-148">Issue resolution</span></span>

<span data-ttu-id="d0213-149">Priser hentes altid fra samhandelsaftaler (eller andre prisindstillinger i systemet, f.eks. salgsaftaler eller varepriser), og de angives for en enhed.</span><span class="sxs-lookup"><span data-stu-id="d0213-149">Prices are always obtained from trade agreements (or other price settings in the system, such as sales agreements or item prices), and they are set for a unit.</span></span>

<span data-ttu-id="d0213-150">Hvis enheden ændres på en ordrelinje, søger systemet efter en pris for den nye enhed og anvender denne pris.</span><span class="sxs-lookup"><span data-stu-id="d0213-150">If the unit is changed on an order line, the system looks for a price for the new unit and applies that price.</span></span> <span data-ttu-id="d0213-151">Hvis der ikke findes en pris for enheden, vil systemet ikke anvende en pris.</span><span class="sxs-lookup"><span data-stu-id="d0213-151">If no price is found for the unit, the system doesn't apply a price.</span></span> <span data-ttu-id="d0213-152">Enhedsomregningen kan ikke bruges til at genberegne prisen til en anden enhed.</span><span class="sxs-lookup"><span data-stu-id="d0213-152">The unit conversion can't be used to recalculate the price into another unit.</span></span> <span data-ttu-id="d0213-153">Teoretisk er prisen for en kasse på ti måske ikke lig med ti gange prisen på en enkelt kasse.</span><span class="sxs-lookup"><span data-stu-id="d0213-153">Theoretically, the price for one box of ten might not equal ten times the price of one box.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="d0213-154">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="d0213-154">Issue workaround</span></span>

<span data-ttu-id="d0213-155">En måde at løse dette problem på er at sikre, at der bruges samhandelsaftaler for de enheder, du forventer skal bruges på ordrelinjerne for varen.</span><span class="sxs-lookup"><span data-stu-id="d0213-155">One way to work around this issue is to make sure that there are trade agreements for the units that you expect will be used on order lines for the item.</span></span>

## <a name="currency-conversion-issues-occur-with-trade-agreements"></a><span data-ttu-id="d0213-156">Valutaomregningsproblemer opstår med samhandelsaftaler.</span><span class="sxs-lookup"><span data-stu-id="d0213-156">Currency conversion issues occur with trade agreements.</span></span>

<span data-ttu-id="d0213-157">Priserne i samhandelsaftaler genberegnes ikke i henhold til valutaen, når valutaen afviger på en indkøbsordre.</span><span class="sxs-lookup"><span data-stu-id="d0213-157">Trade agreement prices aren't recalculated according to the currency when the currency differs on a purchase order.</span></span>

<span data-ttu-id="d0213-158">Med funktionen *Generisk valuta* kan du kun definere priser og rabatter i én valuta.</span><span class="sxs-lookup"><span data-stu-id="d0213-158">The *Generic currency* feature lets you define prices and discounts in only one currency.</span></span> <span data-ttu-id="d0213-159">Du kan derefter omregne til andre valutaer efter behov.</span><span class="sxs-lookup"><span data-stu-id="d0213-159">You can then convert to other currencies as you require.</span></span> <span data-ttu-id="d0213-160">Når omregningen er udført, kan funktionen desuden automatisk anvende intelligent afrunding.</span><span class="sxs-lookup"><span data-stu-id="d0213-160">Furthermore, after the conversion is done, the feature can automatically apply smart rounding.</span></span>

## <a name="when-i-open-the-purchase-agreement-page-in-a-line-view-mode-i-cant-personalize-the-page-by-adding-the-price-unit-field-in-the-overview-of-the-line"></a><span data-ttu-id="d0213-161">Når jeg åbner siden Købsaftale i en linjevisningstilstand, kan jeg ikke tilpasse siden ved at føje feltet Prisenhed til oversigten på linjen.</span><span class="sxs-lookup"><span data-stu-id="d0213-161">When I open the Purchase agreement page in a line view mode, I can't personalize the page by adding the Price unit field in the overview of the line.</span></span>

<span data-ttu-id="d0213-162">Visse delte felter i aftalestrukturen kan ikke medtages i personlige indstillinger.</span><span class="sxs-lookup"><span data-stu-id="d0213-162">Some shared fields in the agreement framework can't be included in personalizations.</span></span> <span data-ttu-id="d0213-163">Denne begrænsning forekommer på grund af den implementerede datamodel.</span><span class="sxs-lookup"><span data-stu-id="d0213-163">This limitation occurs because of the data model that is implemented.</span></span> <span data-ttu-id="d0213-164">Du kan derfor ikke tilpasse feltet **Prisenhed**.</span><span class="sxs-lookup"><span data-stu-id="d0213-164">Therefore, you can't personalize the **Price unit** field.</span></span>

## <a name="the-maximum-limit-from-a-purchase-agreement-isnt-effective-on-a-purchase-requisition"></a><span data-ttu-id="d0213-165">Den maksimale grænse for en købsaftale er ikke gældende på en indkøbsrekvisition.</span><span class="sxs-lookup"><span data-stu-id="d0213-165">The maximum limit from a purchase agreement isn't effective on a purchase requisition.</span></span>

### <a name="issue-description"></a><span data-ttu-id="d0213-166">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="d0213-166">Issue description</span></span>

<span data-ttu-id="d0213-167">Når en indkøbsrekvisition er knyttet til en købsaftale, er maksimumgrænsen fra købsaftalen ikke gældende i indkøbsrekvisitionen.</span><span class="sxs-lookup"><span data-stu-id="d0213-167">When a purchase requisition is linked to a purchase agreement, the maximum limit from the purchase agreement isn't effective on the purchase requisition.</span></span> <span data-ttu-id="d0213-168">Standardprisoplysningerne angives korrekt, men mere end maksimumgrænsen fra købsaftalen kan bestilles i indkøbsrekvisitionen.</span><span class="sxs-lookup"><span data-stu-id="d0213-168">The default price information is correctly entered, but more than the maximum limit from the purchase agreement can be ordered in the purchase requisition.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="d0213-169">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="d0213-169">Issue resolution</span></span>

<span data-ttu-id="d0213-170">Denne funktionsmåde forventes.</span><span class="sxs-lookup"><span data-stu-id="d0213-170">This behavior is expected.</span></span> <span data-ttu-id="d0213-171">Da rekvisitioner ikke altid er godkendt, bør et antal eller beløb ikke reserveres på købsaftalen.</span><span class="sxs-lookup"><span data-stu-id="d0213-171">Because requisitions aren't always approved, a quantity or amount should not be reserved on the purchase agreement.</span></span> <span data-ttu-id="d0213-172">Derfor når du ikke maksimumgrænsen fra købsaftalen.</span><span class="sxs-lookup"><span data-stu-id="d0213-172">Therefore, you won't meet the maximum limit from the purchase agreement.</span></span>

## <a name="trade-agreements-can-be-created-from-rejected-rfqs-therefore-the-system-doesnt-prevent-trade-agreement-journals-from-being-created-if-the-rfq-line-hasnt-been-accepted"></a><span data-ttu-id="d0213-173">Der kan oprettes samhandelsaftaler ud fra afviste tilbudsanmodninger.</span><span class="sxs-lookup"><span data-stu-id="d0213-173">Trade agreements can be created from rejected RFQs.</span></span> <span data-ttu-id="d0213-174">Systemet forhindrer derfor ikke, at samhandelskladderne oprettes, hvis linjen i tilbudsanmodningen ikke er blevet accepteret.</span><span class="sxs-lookup"><span data-stu-id="d0213-174">Therefore, the system doesn't prevent trade agreement journals from being created if the RFQ line hasn't been accepted.</span></span>

<span data-ttu-id="d0213-175">Du kan oprette samhandelsaftaler som svar på en tilbudsanmodning, uanset om den er blevet accepteret eller afvist.</span><span class="sxs-lookup"><span data-stu-id="d0213-175">You can create trade agreements for any replies for a request for quotation (RFQ), regardless of whether they were accepted or rejected.</span></span> <span data-ttu-id="d0213-176">Du kan finde flere oplysninger under [Oversigt over tilbudsanmodninger](request-quotations.md).</span><span class="sxs-lookup"><span data-stu-id="d0213-176">For more information, see [Requests for quotation (RFQs) overview](request-quotations.md).</span></span>

