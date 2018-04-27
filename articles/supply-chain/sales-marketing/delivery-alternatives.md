---
title: Leveringsalternativer
description: Salgordretagerne kan bruge siden Leveringsalternativer til at finde alternative indstillinger for ordreopfyldning.
author: ChristianRytt
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesLineDeliveryDetails
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 271623
ms.assetid: 527f6084-44fe-41bb-924f-4386e926358a
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: crytt
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 58c083b2fa76e90d10ec8a197a4743a9e315db46
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---

# <a name="delivery-alternatives"></a><span data-ttu-id="11584-103">Leveringsalternativer</span><span class="sxs-lookup"><span data-stu-id="11584-103">Delivery alternatives</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="11584-104">Salgordretagerne kan bruge siden Leveringsalternativer til at finde alternative indstillinger for ordreopfyldning.</span><span class="sxs-lookup"><span data-stu-id="11584-104">Sales order takers can use the Delivery alternatives page to discover alternative order fulfillment options.</span></span>

<span data-ttu-id="11584-105">I Microsoft Dynamics 365 for Operations version 1611 (november 2016) kan salgsordretagere bruge siden **Leveringsalternativer** til at finde alternative indstillinger for ordreopfyldning.</span><span class="sxs-lookup"><span data-stu-id="11584-105">In Microsoft Dynamics 365 for Operations version 1611 (November 2016), sales order takers can use the **Delivery alternatives** page to discover alternative order fulfillment options.</span></span> <span data-ttu-id="11584-106">Det nye sidelayout giver et bedre overblik over alle alternative indstillinger.</span><span class="sxs-lookup"><span data-stu-id="11584-106">The redesigned page layout gives a better overview of all alternative options.</span></span> <span data-ttu-id="11584-107">Det giver også ordretagerne mulighed for at se opfyldningsmuligheder andre steder end i det aktuelle firma.</span><span class="sxs-lookup"><span data-stu-id="11584-107">It also lets order takers look beyond the current company for fulfillment opportunities.</span></span> <span data-ttu-id="11584-108">De kan nu få vist både interne salgsmuligheder og salgsmuligheder fra eksterne leverandører.</span><span class="sxs-lookup"><span data-stu-id="11584-108">They can now view both intercompany opportunities and opportunities from external vendors.</span></span> <span data-ttu-id="11584-109">Ved at sortere indstillingerne pr. leveringsdato kan salgsordretagerne få vist en intelligent liste over leveringsalternativer.</span><span class="sxs-lookup"><span data-stu-id="11584-109">By sorting the options by delivery date, sales order takers can view an intelligent list of delivery alternatives.</span></span> <span data-ttu-id="11584-110">Desuden hjælper parametre dem med nemmere at administrere de foreslåede leveringer.</span><span class="sxs-lookup"><span data-stu-id="11584-110">In addition, parameters help them better manage the suggested deliveries.</span></span> <span data-ttu-id="11584-111">Da transporttiden kan påvirke leveringsdatoer, kan salgsordretagerne udforske de forskellige transportsmuligheder, som fragtmænd tilbyder.</span><span class="sxs-lookup"><span data-stu-id="11584-111">Because transport time can affect delivery dates, sales order takers can explore the various transportation choices that carriers offer.</span></span> <span data-ttu-id="11584-112">Der vises detaljerede oplysninger om hvert forslag, og ordretagerne kan derfor træffe velfunderede beslutninger direkte fra siden **Leveringsalternativer**.</span><span class="sxs-lookup"><span data-stu-id="11584-112">Because detailed information is shown for each suggestion, order takers can make informed decisions directly from the **Delivery alternatives** page.</span></span>

## <a name="open-the-delivery-alternatives-page"></a><span data-ttu-id="11584-113">Åbne siden Leveringsalternativer</span><span class="sxs-lookup"><span data-stu-id="11584-113">Open the Delivery alternatives page</span></span>
<span data-ttu-id="11584-114">Du kan åbne siden **Leverings** **alternativer** fra salgsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="11584-114">You can open the **Delivery** **alternatives** page from the sales order line.</span></span>

1.  <span data-ttu-id="11584-115">Klik på **Produkter og forsyning** &gt; **Leveringsalternativer**.</span><span class="sxs-lookup"><span data-stu-id="11584-115">Click **Products and supply** &gt; **Delivery alternatives**.</span></span>
2.  <span data-ttu-id="11584-116">Klik på **Linjedetaljer** &gt; **Levering** &gt; **Leveringsalternativer.**</span><span class="sxs-lookup"><span data-stu-id="11584-116">Click **Line details** &gt; **Delivery** &gt; **Delivery alternatives.**</span></span>

<span data-ttu-id="11584-117">Du kan også åbne siden **Leveringsalternativer** ved at åbne arbejdsområdet **Salgsordrebehandling og -forespørgsel** og derefter klikke på **Ordrer og favoritter** &gt; **Forsinkede ordrelinjer** &gt; **Leveringsalternativer** **Bemærk!** Du kan kun åbne siden **Leveringsalternativer**, hvis begge følgende betingelser er opfyldt:</span><span class="sxs-lookup"><span data-stu-id="11584-117">You can also open the **Delivery alternatives** page by opening the **Sales order processing and inquiry** workspace, and then clicking **Orders and favorites** &gt; **Delayed order lines** &gt; **Delivery alternatives** **Note:** You can open the **Delivery alternatives** page only if both the following conditions are met:</span></span>

-   <span data-ttu-id="11584-118">Alle obligatoriske oplysninger om salgslinjen er udfyldt.</span><span class="sxs-lookup"><span data-stu-id="11584-118">All mandatory sales line information is filled in.</span></span>
-   <span data-ttu-id="11584-119">Feltet **Leveringsdatokontrol** er indstillet til en anden værdi end **Ingen**.</span><span class="sxs-lookup"><span data-stu-id="11584-119">The **Delivery date control** field is set to a value other than **None**.</span></span>

## <a name="delivery-date-control-methods"></a><span data-ttu-id="11584-120">Leveringsdatokontrolmetoder</span><span class="sxs-lookup"><span data-stu-id="11584-120">Delivery date control methods</span></span>
<span data-ttu-id="11584-121">Leveringsdatokontrolmetoden bestemmer, hvordan systemet fastsætter leveringsdatoer, hvordan leveringsalternativer beregnes, og hvilke oplysninger der vises.</span><span class="sxs-lookup"><span data-stu-id="11584-121">The delivery date control method determines how the system establishes delivery dates, how delivery alternatives are calculated, and what information is shown.</span></span> <span data-ttu-id="11584-122">Bemærk, at leveringsdatokontrollen tager kalendere i betragtning.</span><span class="sxs-lookup"><span data-stu-id="11584-122">Note that delivery data control takes calendars into consideration.</span></span> <span data-ttu-id="11584-123">Derfor kan følgende kalendere påvirke den foreslåede modtagelsesdato: lagerstedkalender, transportkalender, kreditorkalender og debitorkalender.</span><span class="sxs-lookup"><span data-stu-id="11584-123">Therefore, the following calendars can affect the suggested receipt date: Warehouse calendar, Transport calendar, Vendor calendar, and Customer calendar.</span></span> <span data-ttu-id="11584-124">I følgende tabel beskrives hver metode for leveringsdatokontrol.</span><span class="sxs-lookup"><span data-stu-id="11584-124">The following table describes each method for delivery date control.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="11584-125"><strong>Metode</strong></span><span class="sxs-lookup"><span data-stu-id="11584-125"><strong>Method</strong></span></span></td>
<td><span data-ttu-id="11584-126"><strong>Beskrivelse</strong></span><span class="sxs-lookup"><span data-stu-id="11584-126"><strong>Description</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11584-127"><strong>Ingen</strong></span><span class="sxs-lookup"><span data-stu-id="11584-127"><strong>None</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="11584-128">Leveringsalternativer for salgslinjer understøttes ikke.</span><span class="sxs-lookup"><span data-stu-id="11584-128">Delivery alternatives for sales lines aren&#39;t supported.</span></span> <span data-ttu-id="11584-129">Denne indstilling deaktiverer leveringsdatokontrollen.</span><span class="sxs-lookup"><span data-stu-id="11584-129">This option turns off delivery data control.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11584-130"><strong>Salgsleveringstid</strong></span><span class="sxs-lookup"><span data-stu-id="11584-130"><strong>Sales lead time</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="11584-131">Leveringsalternativer beregnes ud fra den foruddefinerede salgsleveringstid.</span><span class="sxs-lookup"><span data-stu-id="11584-131">Delivery alternatives are calculated based on the predefined sales lead time.</span></span> <span data-ttu-id="11584-132">Transportdage beregnes ud fra leveringsmåden.</span><span class="sxs-lookup"><span data-stu-id="11584-132">The transport days are calculated based on the mode of delivery.</span></span></li>
<li><span data-ttu-id="11584-133">Leveringsalternativer omfatter lagersteder, der har en disponibel lagerbeholdning og forsynings- og behovsordrer.</span><span class="sxs-lookup"><span data-stu-id="11584-133">Delivery alternatives include warehouses that have on-hand inventory, and supply/demand orders.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11584-134"><strong>DTT</strong></span><span class="sxs-lookup"><span data-stu-id="11584-134"><strong>ATP</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="11584-135">Leveringsalternativer beregnes ud fra disponibel til tilsagn-logik (DTT).</span><span class="sxs-lookup"><span data-stu-id="11584-135">Delivery alternatives are calculated based on available to promise (ATP) logic.</span></span> <span data-ttu-id="11584-136">Den aktuelle tilgængelighed og den forventede fremtidige tilgængelighed indgår i betragtningerne.</span><span class="sxs-lookup"><span data-stu-id="11584-136">The current availability and expected future availability are considered.</span></span> <span data-ttu-id="11584-137">Transportdage beregnes ud fra leveringsmåden.</span><span class="sxs-lookup"><span data-stu-id="11584-137">The transport days are calculated based on the mode of delivery.</span></span></li>
<li><span data-ttu-id="11584-138">Leveringsalternativer omfatter lagersteder, der har en disponibel lagerbeholdning og forsynings- og behovsordrer.</span><span class="sxs-lookup"><span data-stu-id="11584-138">Delivery alternatives include warehouses that have on-hand inventory, and supply/demand orders.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11584-139"><strong>DTT + afgangsmargen</strong></span><span class="sxs-lookup"><span data-stu-id="11584-139"><strong>ATP + Issue margin</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="11584-140">Leveringsalternativer beregnes som for DTT-metoden, men afgangsmargenen medtages i beregningen.</span><span class="sxs-lookup"><span data-stu-id="11584-140">Delivery alternatives are calculated as for the ATP method, but the issue margin is included in the calculation.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11584-141"><strong>LE</strong></span><span class="sxs-lookup"><span data-stu-id="11584-141"><strong>CTP</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="11584-142">Leveringsalternativer beregnes ud fra leveringsevne-logik (LE).</span><span class="sxs-lookup"><span data-stu-id="11584-142">Delivery alternatives are calculated based on the capable to promise (CTP) logic.</span></span> <span data-ttu-id="11584-143">MPS-udfoldning bruges til at bestemme tilgængeligheden.</span><span class="sxs-lookup"><span data-stu-id="11584-143">MRP explosion is used to determine availability.</span></span> <span data-ttu-id="11584-144">Bemærk, at LE som minimum forskyder leveringsdatoer til salgsleveringstiden.</span><span class="sxs-lookup"><span data-stu-id="11584-144">Note that, at a minimum, CTP offsets delivery dates to the sales lead time.</span></span> <span data-ttu-id="11584-145">Transportdage beregnes ud fra leveringsmåden.</span><span class="sxs-lookup"><span data-stu-id="11584-145">The transport days are calculated based on the mode of delivery.</span></span></li>
<li><span data-ttu-id="11584-146">Leveringsalternativer omfatter forslag for følgende lagersteder:</span><span class="sxs-lookup"><span data-stu-id="11584-146">Delivery alternatives include suggestions for the following warehouses:</span></span>
<ul>
<li><span data-ttu-id="11584-147">Aktuelt lagersted</span><span class="sxs-lookup"><span data-stu-id="11584-147">Current warehouse</span></span></li>
<li><span data-ttu-id="11584-148">Standardlagersted</span><span class="sxs-lookup"><span data-stu-id="11584-148">Default warehouse</span></span></li>
<li><span data-ttu-id="11584-149">Alle lagersteder, der har tilgængelig disponibel lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="11584-149">All warehouses that have available on-hand inventory</span></span></li>
<li><span data-ttu-id="11584-150">Alle lagersteder, der har forsyningsordrer</span><span class="sxs-lookup"><span data-stu-id="11584-150">All warehouses that have supply orders</span></span></li>
<li><span data-ttu-id="11584-151">Alle lagersteder, der har aktive styklisteversioner</span><span class="sxs-lookup"><span data-stu-id="11584-151">All warehouses that have active bill of materials (BOM) versions</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="view-information-about-delivery-alternatives"></a><span data-ttu-id="11584-152">Få vist oplysninger om leveringsalternativer</span><span class="sxs-lookup"><span data-stu-id="11584-152">View information about delivery alternatives</span></span>
<span data-ttu-id="11584-153">I dette afsnit beskrives de oplysninger om leveringsalternativer, der er tilgængelige under hver fane på siden **Leveringsalternativer**.</span><span class="sxs-lookup"><span data-stu-id="11584-153">This section describes the information about delivery alternatives that is available on each tab of the **Delivery alternatives** page.</span></span>

### <a name="products"></a><span data-ttu-id="11584-154">Produkter</span><span class="sxs-lookup"><span data-stu-id="11584-154">Products</span></span>

<span data-ttu-id="11584-155">Denne fane vises en oversigt over produktet og detaljer om den aktuelle salgslinje.</span><span class="sxs-lookup"><span data-stu-id="11584-155">This tab shows a summary of the product and details of the current sales line.</span></span>

### <a name="delivery-alternatives"></a><span data-ttu-id="11584-156">Leveringsalternativer</span><span class="sxs-lookup"><span data-stu-id="11584-156">Delivery alternatives</span></span>

<span data-ttu-id="11584-157">Denne fane viser en liste over leveringsalternativer, der er sorteret efter kvitteringsdata.</span><span class="sxs-lookup"><span data-stu-id="11584-157">This tab shows a list of delivery alternatives that is sorted by receipt data.</span></span> <span data-ttu-id="11584-158">Over listen kan du vælge, hvilke indstillinger du vil basere forslagene på.</span><span class="sxs-lookup"><span data-stu-id="11584-158">Above the list, you can select which options to base the suggestions on.</span></span> <span data-ttu-id="11584-159">Du kan også vælge den leveringsmåde, der bestemmer transportdagene.</span><span class="sxs-lookup"><span data-stu-id="11584-159">You can also select the mode of delivery, which determines the transport days.</span></span> <span data-ttu-id="11584-160">Følgende valgmuligheder er tilgængelige:</span><span class="sxs-lookup"><span data-stu-id="11584-160">The following options are available:</span></span>

-   <span data-ttu-id="11584-161">**Medtag andre produktvarianter** - Denne indstilling er tilgængelig for produkter, der har produktvarianter.</span><span class="sxs-lookup"><span data-stu-id="11584-161">**Include other product variants** - This option is available for products that have product variants.</span></span> <span data-ttu-id="11584-162">Den omfatter leveringsalternativer til andre varianter af produktet.</span><span class="sxs-lookup"><span data-stu-id="11584-162">It will include delivery alternatives for other variants of the product.</span></span> <span data-ttu-id="11584-163">Denne indstilling er ikke tilgængelig for LE.</span><span class="sxs-lookup"><span data-stu-id="11584-163">This option isn't available for CTP.</span></span>
-   <span data-ttu-id="11584-164">**Inkluder delvis mængde** – Som standard medtages kun forslag, der opfylder det fulde antal på salgslinjen.</span><span class="sxs-lookup"><span data-stu-id="11584-164">**Include partial quantity** - By default, only suggestions that fulfill the full quantity of the sales line are included.</span></span> <span data-ttu-id="11584-165">Vælg denne indstilling for at medtage forslag, der kun delvist opfylder ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="11584-165">Select this option to include suggestions that only partially fulfill the order line.</span></span> <span data-ttu-id="11584-166">Denne indstilling er nyttig, når kunden anmoder om en tidligere leveringsdato og accepterer delvis levering.</span><span class="sxs-lookup"><span data-stu-id="11584-166">This option is useful when the customer requests an earlier delivery date and accepts partial delivery.</span></span>
-   <span data-ttu-id="11584-167">**Medtag senere datoer** – Som standard vises kun forslag, som er bedre (tidligere) end de aktuelle datoer på salgslinjen.</span><span class="sxs-lookup"><span data-stu-id="11584-167">**Include later dates** - By default, only suggestions that are better (earlier) than the current dates on the sales line are shown.</span></span> <span data-ttu-id="11584-168">Vælg denne indstilling for at medtage senere datoer.</span><span class="sxs-lookup"><span data-stu-id="11584-168">Select this option to include later dates.</span></span> <span data-ttu-id="11584-169">Denne indstilling kan være nyttigt i situationer, hvor andre parametre end datoen er prioriteret.</span><span class="sxs-lookup"><span data-stu-id="11584-169">This option can be useful in situations where parameters other than the date have priority.</span></span> <span data-ttu-id="11584-170">For eksempel kan en bestemt leverandør eller et lagersted være foretrukket.</span><span class="sxs-lookup"><span data-stu-id="11584-170">For example, a specific vendor or warehouse might be preferred.</span></span>
-   <span data-ttu-id="11584-171">**Leveringsmåde** – Vælg den foretrukne leveringsmåde for at optimere transporttid og omkostninger.</span><span class="sxs-lookup"><span data-stu-id="11584-171">**Mode of delivery** - Select the preferred mode of delivery to optimize transport time and cost.</span></span> <span data-ttu-id="11584-172">Indvirkningen på de foreslåede leveringsalternativer fremgår med det samme.</span><span class="sxs-lookup"><span data-stu-id="11584-172">You will immediately see the effect on the suggested delivery alternatives.</span></span> <span data-ttu-id="11584-173">Det er derfor nemt at sammenligne alternativerne.</span><span class="sxs-lookup"><span data-stu-id="11584-173">Therefore, it's easy to compare the alternatives.</span></span>
-   <span data-ttu-id="11584-174">**Medtag indkøb** – Når indkøb er markeret, omfatter de foreslåede leveringsalternativer muligheder for at købe fra både eksterne leverandører og andre firmaer i virksomheden (intern).</span><span class="sxs-lookup"><span data-stu-id="11584-174">**Include procurement** - When procurement is selected, the suggested delivery alternatives include options to procure from both external vendors and other companies in the enterprise (intercompany).</span></span> <span data-ttu-id="11584-175">Indstillingen **Medtag indkøb** understøttes for DTT og DTT + afgangsmargen-leveringsdatokontrol.</span><span class="sxs-lookup"><span data-stu-id="11584-175">The **Include procurement** option is supported for ATP and ATP + Issue margin delivery date control.</span></span> <span data-ttu-id="11584-176">Indstillinger for indkøb fra standardindskøbsleverandøren for produktet og alle godkendte kreditorer for produktet er inkluderet.</span><span class="sxs-lookup"><span data-stu-id="11584-176">Procurement options from the default purchase vendor for the product and all approved vendors for the product are included.</span></span>
-   <span data-ttu-id="11584-177">For eksterne leverandører er beregningen baseret på leveringstiden for indkøbet.</span><span class="sxs-lookup"><span data-stu-id="11584-177">For external vendors, the calculation is based on the purchase lead time.</span></span>
-   <span data-ttu-id="11584-178">Internt indgår det i beregningen, hvad der er tilgængeligt fra forsyningsfirmaet, baseret på leveringsdatokontrol i forsyningsfirmaet.</span><span class="sxs-lookup"><span data-stu-id="11584-178">For intercompany, the calculation considers what is available from the sourcing company, based on delivery date control in the sourcing company.</span></span>
-   <span data-ttu-id="11584-179">**Leveringstype** (Relevant for indkøb)</span><span class="sxs-lookup"><span data-stu-id="11584-179">**Delivery type** (Relevant for procurement)</span></span>
    -   <span data-ttu-id="11584-180">**Lager** - Produkterne leveres fra forsyningslagerstedet til lokationen/lagerstedet på salgslinjen.</span><span class="sxs-lookup"><span data-stu-id="11584-180">**Stock** - Products are shipped from the sourcing warehouse to the site/warehouse on the sales line.</span></span> <span data-ttu-id="11584-181">De sendes derefter fra lagerstedet til kunden.</span><span class="sxs-lookup"><span data-stu-id="11584-181">They are then shipped from that warehouse to the customer.</span></span>
    -   <span data-ttu-id="11584-182">**Direkte levering** - Produkterne leveres direkte til kunden fra forsyningslagerstedet.</span><span class="sxs-lookup"><span data-stu-id="11584-182">**Direct delivery** - Products are shipped directly from the sourcing warehouse to the customer.</span></span>

### <a name="availability-information"></a><span data-ttu-id="11584-183">Oplysninger om tilgængelighed</span><span class="sxs-lookup"><span data-stu-id="11584-183">Availability information</span></span>

<span data-ttu-id="11584-184">Oplysningerne under denne fane er relateret til den alternative leveringslinje, der er valgt.</span><span class="sxs-lookup"><span data-stu-id="11584-184">Information on this tab is related to the delivery alternative line that is selected.</span></span> <span data-ttu-id="11584-185">Følgende oplysninger vises, afhængigt af leveringsdatokontrollen for salgslinjen:</span><span class="sxs-lookup"><span data-stu-id="11584-185">The following information is shown, depending on the delivery date control for the sales line:</span></span>

-   <span data-ttu-id="11584-186">**Salgsleveringstid**</span><span class="sxs-lookup"><span data-stu-id="11584-186">**Sales lead time**</span></span>
    -   <span data-ttu-id="11584-187">**Til rådighed i dag** – Få vist den aktuelle disponible lagerbeholdning, fysisk reserveret og disponibelt fysisk lager.</span><span class="sxs-lookup"><span data-stu-id="11584-187">**Available today** - Show the current physical on-hand, physical reserved, and available physical inventory.</span></span>
    -   <span data-ttu-id="11584-188">**Parametre** - Viser lagerenheden og salgsleveringstiden.</span><span class="sxs-lookup"><span data-stu-id="11584-188">**Parameters** - Show the inventory unit and sales lead time.</span></span>

-   <span data-ttu-id="11584-189">**DTT og DTT + afgangsmargen**</span><span class="sxs-lookup"><span data-stu-id="11584-189">**ATP and ATP + Issue margin**</span></span>
    -   <span data-ttu-id="11584-190">**Til rådighed i dag** – Få vist den aktuelle disponible lagerbeholdning, fysisk reserveret og disponibelt fysisk lager.</span><span class="sxs-lookup"><span data-stu-id="11584-190">**Available today** - Show the current physical on-hand, physical reserved, and available physical inventory.</span></span>
    -   <span data-ttu-id="11584-191">**Parametre** - Viser lagerenheden og salgsleveringstiden.</span><span class="sxs-lookup"><span data-stu-id="11584-191">**Parameters** - Show the inventory unit and sales lead time.</span></span>
    -   <span data-ttu-id="11584-192">**Fremtidig tilgængelighed** – Få vist en grafisk repræsentation af den aktuelle og fremtidige tilgængelighed for valgt lokation og lagersted under **Leveringsalternativer**.</span><span class="sxs-lookup"><span data-stu-id="11584-192">**Future availability** - Show a graphical representation of current and future availability for the selected site and warehouse under **Delivery alternatives**.</span></span> <span data-ttu-id="11584-193">Hvis du vil have vist mere detaljerede oplysninger om produktets tilgængelig fremover, kan du klikke på diagramsøjlerne.</span><span class="sxs-lookup"><span data-stu-id="11584-193">You can click the chart columns to see more detailed information about the future availability of the product.</span></span> <span data-ttu-id="11584-194">Skyderen viser en liste over relevante behovs- og forsyningsordrer i en DTT-tidshorisont.</span><span class="sxs-lookup"><span data-stu-id="11584-194">The slider shows a list of relevant demand and supply orders within the ATP time fence.</span></span>

-   <span data-ttu-id="11584-195">**LE**</span><span class="sxs-lookup"><span data-stu-id="11584-195">**CTP**</span></span>
    -   <span data-ttu-id="11584-196">**Til rådighed i dag** – Få vist den aktuelle disponible lagerbeholdning, fysisk reserveret og disponibelt fysisk lager.</span><span class="sxs-lookup"><span data-stu-id="11584-196">**Available today** - Show the current physical on-hand, physical reserved, and available physical inventory.</span></span>
    -   <span data-ttu-id="11584-197">**Parametre** - Viser lagerenheden og salgsleveringstiden.</span><span class="sxs-lookup"><span data-stu-id="11584-197">**Parameters** - Show the inventory unit and sales lead time.</span></span>
    -   <span data-ttu-id="11584-198">**Udfoldning** – Få vist forsyning for den valgte leveringsalternative udfoldet.</span><span class="sxs-lookup"><span data-stu-id="11584-198">**Explosion** - Show a supply explosion of the selected delivery alternative.</span></span> <span data-ttu-id="11584-199">Du kan bruge **Konfiguration** til at ændre felterne og de lagerdimensioner, der vises i udfoldningen.</span><span class="sxs-lookup"><span data-stu-id="11584-199">You can use **Setup** to change the fields and inventory dimensions that are shown in the explosion.</span></span>

### <a name="impact-of-selected-alternative"></a><span data-ttu-id="11584-200">Virkning af valgt alternativ</span><span class="sxs-lookup"><span data-stu-id="11584-200">Impact of selected alternative</span></span>

<span data-ttu-id="11584-201">Denne fane viser resultatet af det valgte leveringsalternativ fremhævet.</span><span class="sxs-lookup"><span data-stu-id="11584-201">This tab highlights the impact of the selected delivery alternative.</span></span> <span data-ttu-id="11584-202">Hvis du klikker på **OK**, opdateres salgslinjen med de fremhævede værdierne i de markerede kolonner.</span><span class="sxs-lookup"><span data-stu-id="11584-202">If you click **OK**, the sales line is updated with the highlighted values in the SELECTED columns.</span></span> <span data-ttu-id="11584-203">Bemærk, at hvis antallet i det valgte leveringsalternativ er mindre end antallet på salgslinjen, oprettes en leveranceplan, og ordrelinjen opdeles i to linjer: én linje for det valgte antal og én linje for det resterende antal.</span><span class="sxs-lookup"><span data-stu-id="11584-203">Note that, if the quantity on the selected delivery alternative is less than quantity on the sales line, a delivery schedule is created, and the order line is split into two lines: one line for the selected quantity and one line for the remaining quantity.</span></span> <span data-ttu-id="11584-204">Du kan også opdatere den kommercielle linje, så den svarer til linjerne for tidsplanen og påvirker prisfastsættelsen.</span><span class="sxs-lookup"><span data-stu-id="11584-204">You can also update the commercial line so that it matches the schedule lines and affects the pricing.</span></span>

<a name="see-also"></a><span data-ttu-id="11584-205">Se også</span><span class="sxs-lookup"><span data-stu-id="11584-205">See also</span></span>
--------

[<span data-ttu-id="11584-206">Ordretilsagn</span><span class="sxs-lookup"><span data-stu-id="11584-206">Order promising</span></span>](delivery-dates-available-promise-calculations.md)





