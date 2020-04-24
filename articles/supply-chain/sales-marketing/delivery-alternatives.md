---
title: Leveringsalternativer
description: Salgordretagerne kan bruge siden Leveringsalternativer til at finde alternative indstillinger for ordreopfyldning.
author: ChristianRytt
manager: tfehr
ms.date: 04/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesLineDeliveryDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 271623
ms.assetid: 527f6084-44fe-41bb-924f-4386e926358a
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: crytt
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 48cc8974cc8a8769b3d05f47f82166164e877ae5
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210082"
---
# <a name="delivery-alternatives"></a><span data-ttu-id="b6dc8-103">Leveringsalternativer</span><span class="sxs-lookup"><span data-stu-id="b6dc8-103">Delivery alternatives</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b6dc8-104">Salgordretagerne kan bruge siden **Leveringsalternativer** til at finde alternative indstillinger for ordreopfyldning.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-104">Sales order takers can use the **Delivery alternatives** page to discover alternative order fulfillment options.</span></span>

<span data-ttu-id="b6dc8-105">Siden **Leveringsalternativer** giver et overblik over alle alternative indstillinger.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-105">The **Delivery alternatives** page layout gives an overview of all alternative options.</span></span> <span data-ttu-id="b6dc8-106">Det giver også ordretagerne mulighed for at se opfyldningsmuligheder andre steder end i det aktuelle firma.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-106">It also lets order takers look beyond the current company for fulfillment opportunities.</span></span> <span data-ttu-id="b6dc8-107">De kan nu få vist både interne salgsmuligheder og salgsmuligheder fra eksterne leverandører.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-107">They can now view both intercompany opportunities and opportunities from external vendors.</span></span> <span data-ttu-id="b6dc8-108">Ved at sortere indstillingerne pr. leveringsdato kan salgsordretagerne få vist en intelligent liste over leveringsalternativer.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-108">By sorting the options by delivery date, sales order takers can view an intelligent list of delivery alternatives.</span></span> <span data-ttu-id="b6dc8-109">Desuden hjælper parametre dem med nemmere at administrere de foreslåede leveringer.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-109">In addition, parameters help them better manage the suggested deliveries.</span></span> <span data-ttu-id="b6dc8-110">Da transporttiden kan påvirke leveringsdatoer, kan salgsordretagerne udforske de forskellige transportsmuligheder, som fragtmænd tilbyder.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-110">Because transport time can affect delivery dates, sales order takers can explore the various transportation choices that carriers offer.</span></span> <span data-ttu-id="b6dc8-111">Der vises detaljerede oplysninger om hvert forslag, og ordretagerne kan derfor træffe velfunderede beslutninger direkte fra siden **Leveringsalternativer**.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-111">Because detailed information is shown for each suggestion, order takers can make informed decisions directly from the **Delivery alternatives** page.</span></span>

## <a name="open-the-delivery-alternatives-page"></a><span data-ttu-id="b6dc8-112">Åbne siden Leveringsalternativer</span><span class="sxs-lookup"><span data-stu-id="b6dc8-112">Open the Delivery alternatives page</span></span>
<span data-ttu-id="b6dc8-113">Du kan åbne siden **Leveringsalternativer** fra salgsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-113">You can open the **Delivery alternatives** page from the sales order line.</span></span>

1.  <span data-ttu-id="b6dc8-114">Klik på **Produkter og forsyning** &gt; **Leveringsalternativer**.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-114">Click **Products and supply** &gt; **Delivery alternatives**.</span></span>
2.  <span data-ttu-id="b6dc8-115">Klik på **Linjedetaljer** &gt; **Levering** &gt; **Leveringsalternativer.**</span><span class="sxs-lookup"><span data-stu-id="b6dc8-115">Click **Line details** &gt; **Delivery** &gt; **Delivery alternatives.**</span></span>

<span data-ttu-id="b6dc8-116">Du kan også åbne siden **Leveringsalternativer** ved at åbne arbejdsområdet **Salgsordrebehandling og -forespørgsel** og derefter klikke på **Ordrer og favoritter** &gt; **Forsinkede ordrelinjer** &gt; **Leveringsalternativer** **Bemærk!** Du kan kun åbne siden **Leveringsalternativer**, hvis begge følgende betingelser er opfyldt:</span><span class="sxs-lookup"><span data-stu-id="b6dc8-116">You can also open the **Delivery alternatives** page by opening the **Sales order processing and inquiry** workspace, and then clicking **Orders and favorites** &gt; **Delayed order lines** &gt; **Delivery alternatives** **Note:** You can open the **Delivery alternatives** page only if both the following conditions are met:</span></span>

-   <span data-ttu-id="b6dc8-117">Alle obligatoriske oplysninger om salgslinjen er udfyldt.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-117">All mandatory sales line information is filled in.</span></span>
-   <span data-ttu-id="b6dc8-118">Feltet **Leveringsdatokontrol** er indstillet til en anden værdi end **Ingen**.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-118">The **Delivery date control** field is set to a value other than **None**.</span></span>

## <a name="delivery-date-control-methods"></a><span data-ttu-id="b6dc8-119">Leveringsdatokontrolmetoder</span><span class="sxs-lookup"><span data-stu-id="b6dc8-119">Delivery date control methods</span></span>
<span data-ttu-id="b6dc8-120">Leveringsdatokontrolmetoden bestemmer, hvordan systemet fastsætter leveringsdatoer, hvordan leveringsalternativer beregnes, og hvilke oplysninger der vises.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-120">The delivery date control method determines how the system establishes delivery dates, how delivery alternatives are calculated, and what information is shown.</span></span> <span data-ttu-id="b6dc8-121">Bemærk, at leveringsdatokontrollen tager kalendere i betragtning.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-121">Note that delivery data control takes calendars into consideration.</span></span> <span data-ttu-id="b6dc8-122">Derfor kan følgende kalendere påvirke den foreslåede modtagelsesdato: lagerstedkalender, transportkalender, kreditorkalender og debitorkalender.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-122">Therefore, the following calendars can affect the suggested receipt date: Warehouse calendar, Transport calendar, Vendor calendar, and Customer calendar.</span></span> <span data-ttu-id="b6dc8-123">I følgende tabel beskrives hver metode for leveringsdatokontrol.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-123">The following table describes each method for delivery date control.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b6dc8-124"><strong>Metode</strong></span><span class="sxs-lookup"><span data-stu-id="b6dc8-124"><strong>Method</strong></span></span></td>
<td><span data-ttu-id="b6dc8-125"><strong>Beskrivelse</strong></span><span class="sxs-lookup"><span data-stu-id="b6dc8-125"><strong>Description</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b6dc8-126"><strong>Ingen</strong></span><span class="sxs-lookup"><span data-stu-id="b6dc8-126"><strong>None</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="b6dc8-127">Leveringsalternativer for salgslinjer understøttes ikke.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-127">Delivery alternatives for sales lines aren&#39;t supported.</span></span> <span data-ttu-id="b6dc8-128">Denne indstilling deaktiverer leveringsdatokontrollen.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-128">This option turns off delivery data control.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b6dc8-129"><strong>Salgsleveringstid</strong></span><span class="sxs-lookup"><span data-stu-id="b6dc8-129"><strong>Sales lead time</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="b6dc8-130">Leveringsalternativer beregnes ud fra den foruddefinerede salgsleveringstid.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-130">Delivery alternatives are calculated based on the predefined sales lead time.</span></span> <span data-ttu-id="b6dc8-131">Transportdage beregnes ud fra leveringsmåden.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-131">The transport days are calculated based on the mode of delivery.</span></span></li>
<li><span data-ttu-id="b6dc8-132">Leveringsalternativer omfatter lagersteder, der har en disponibel lagerbeholdning og forsynings- og behovsordrer.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-132">Delivery alternatives include warehouses that have on-hand inventory, and supply/demand orders.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b6dc8-133"><strong>DTT</strong></span><span class="sxs-lookup"><span data-stu-id="b6dc8-133"><strong>ATP</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="b6dc8-134">Leveringsalternativer beregnes ud fra disponibel til tilsagn-logik (DTT).</span><span class="sxs-lookup"><span data-stu-id="b6dc8-134">Delivery alternatives are calculated based on available to promise (ATP) logic.</span></span> <span data-ttu-id="b6dc8-135">Den aktuelle tilgængelighed og den forventede fremtidige tilgængelighed indgår i betragtningerne.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-135">The current availability and expected future availability are considered.</span></span> <span data-ttu-id="b6dc8-136">Transportdage beregnes ud fra leveringsmåden.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-136">The transport days are calculated based on the mode of delivery.</span></span></li>
<li><span data-ttu-id="b6dc8-137">Leveringsalternativer omfatter lagersteder, der har en disponibel lagerbeholdning og forsynings- og behovsordrer.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-137">Delivery alternatives include warehouses that have on-hand inventory, and supply/demand orders.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b6dc8-138"><strong>DTT + afgangsmargen</strong></span><span class="sxs-lookup"><span data-stu-id="b6dc8-138"><strong>ATP + Issue margin</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="b6dc8-139">Leveringsalternativer beregnes som for DTT-metoden, men afgangsmargenen medtages i beregningen.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-139">Delivery alternatives are calculated as for the ATP method, but the issue margin is included in the calculation.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b6dc8-140"><strong>LE</strong></span><span class="sxs-lookup"><span data-stu-id="b6dc8-140"><strong>CTP</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="b6dc8-141">Leveringsalternativer beregnes ud fra leveringsevne-logik (LE).</span><span class="sxs-lookup"><span data-stu-id="b6dc8-141">Delivery alternatives are calculated based on the capable to promise (CTP) logic.</span></span> <span data-ttu-id="b6dc8-142">MPS-udfoldning bruges til at bestemme tilgængeligheden.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-142">MRP explosion is used to determine availability.</span></span> <span data-ttu-id="b6dc8-143">Bemærk, at LE som minimum forskyder leveringsdatoer til salgsleveringstiden.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-143">Note that, at a minimum, CTP offsets delivery dates to the sales lead time.</span></span> <span data-ttu-id="b6dc8-144">Transportdage beregnes ud fra leveringsmåden.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-144">The transport days are calculated based on the mode of delivery.</span></span></li>
<li><span data-ttu-id="b6dc8-145">Leveringsalternativer omfatter forslag for følgende lagersteder:</span><span class="sxs-lookup"><span data-stu-id="b6dc8-145">Delivery alternatives include suggestions for the following warehouses:</span></span>
<ul>
<li><span data-ttu-id="b6dc8-146">Aktuelt lagersted</span><span class="sxs-lookup"><span data-stu-id="b6dc8-146">Current warehouse</span></span></li>
<li><span data-ttu-id="b6dc8-147">Standardlagersted</span><span class="sxs-lookup"><span data-stu-id="b6dc8-147">Default warehouse</span></span></li>
<li><span data-ttu-id="b6dc8-148">Alle lagersteder, der har tilgængelig disponibel lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="b6dc8-148">All warehouses that have available on-hand inventory</span></span></li>
<li><span data-ttu-id="b6dc8-149">Alle lagersteder, der har forsyningsordrer</span><span class="sxs-lookup"><span data-stu-id="b6dc8-149">All warehouses that have supply orders</span></span></li>
<li><span data-ttu-id="b6dc8-150">Alle lagersteder, der har aktive styklisteversioner</span><span class="sxs-lookup"><span data-stu-id="b6dc8-150">All warehouses that have active bill of materials (BOM) versions</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="view-information-about-delivery-alternatives"></a><span data-ttu-id="b6dc8-151">Få vist oplysninger om leveringsalternativer</span><span class="sxs-lookup"><span data-stu-id="b6dc8-151">View information about delivery alternatives</span></span>
<span data-ttu-id="b6dc8-152">I dette afsnit beskrives de oplysninger om leveringsalternativer, der er tilgængelige under hver fane på siden **Leveringsalternativer**.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-152">This section describes the information about delivery alternatives that is available on each tab of the **Delivery alternatives** page.</span></span>

### <a name="products"></a><span data-ttu-id="b6dc8-153">Produkter</span><span class="sxs-lookup"><span data-stu-id="b6dc8-153">Products</span></span>

<span data-ttu-id="b6dc8-154">Denne fane vises en oversigt over produktet og detaljer om den aktuelle salgslinje.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-154">This tab shows a summary of the product and details of the current sales line.</span></span>

### <a name="delivery-alternatives"></a><span data-ttu-id="b6dc8-155">Leveringsalternativer</span><span class="sxs-lookup"><span data-stu-id="b6dc8-155">Delivery alternatives</span></span>

<span data-ttu-id="b6dc8-156">Denne fane viser en liste over leveringsalternativer, der er sorteret efter kvitteringsdata.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-156">This tab shows a list of delivery alternatives that is sorted by receipt data.</span></span> <span data-ttu-id="b6dc8-157">Over listen kan du vælge, hvilke indstillinger du vil basere forslagene på.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-157">Above the list, you can select which options to base the suggestions on.</span></span> <span data-ttu-id="b6dc8-158">Du kan også vælge den leveringsmåde, der bestemmer transportdagene.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-158">You can also select the mode of delivery, which determines the transport days.</span></span> <span data-ttu-id="b6dc8-159">Følgende valgmuligheder er tilgængelige:</span><span class="sxs-lookup"><span data-stu-id="b6dc8-159">The following options are available:</span></span>

-   <span data-ttu-id="b6dc8-160">**Medtag andre produktvarianter** - Denne indstilling er tilgængelig for produkter, der har produktvarianter.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-160">**Include other product variants** - This option is available for products that have product variants.</span></span> <span data-ttu-id="b6dc8-161">Den omfatter leveringsalternativer til andre varianter af produktet.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-161">It will include delivery alternatives for other variants of the product.</span></span> <span data-ttu-id="b6dc8-162">Denne indstilling er ikke tilgængelig for LE.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-162">This option isn't available for CTP.</span></span>
-   <span data-ttu-id="b6dc8-163">**Inkluder delvis mængde** – Som standard medtages kun forslag, der opfylder det fulde antal på salgslinjen.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-163">**Include partial quantity** - By default, only suggestions that fulfill the full quantity of the sales line are included.</span></span> <span data-ttu-id="b6dc8-164">Vælg denne indstilling for at medtage forslag, der kun delvist opfylder ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-164">Select this option to include suggestions that only partially fulfill the order line.</span></span> <span data-ttu-id="b6dc8-165">Denne indstilling er nyttig, når kunden anmoder om en tidligere leveringsdato og accepterer delvis levering.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-165">This option is useful when the customer requests an earlier delivery date and accepts partial delivery.</span></span>
-   <span data-ttu-id="b6dc8-166">**Medtag senere datoer** – Som standard vises kun forslag, som er bedre (tidligere) end de aktuelle datoer på salgslinjen.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-166">**Include later dates** - By default, only suggestions that are better (earlier) than the current dates on the sales line are shown.</span></span> <span data-ttu-id="b6dc8-167">Vælg denne indstilling for at medtage senere datoer.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-167">Select this option to include later dates.</span></span> <span data-ttu-id="b6dc8-168">Denne indstilling kan være nyttigt i situationer, hvor andre parametre end datoen er prioriteret.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-168">This option can be useful in situations where parameters other than the date have priority.</span></span> <span data-ttu-id="b6dc8-169">For eksempel kan en bestemt leverandør eller et lagersted være foretrukket.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-169">For example, a specific vendor or warehouse might be preferred.</span></span>
-   <span data-ttu-id="b6dc8-170">**Leveringsmåde** – Vælg den foretrukne leveringsmåde for at optimere transporttid og omkostninger.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-170">**Mode of delivery** - Select the preferred mode of delivery to optimize transport time and cost.</span></span> <span data-ttu-id="b6dc8-171">Indvirkningen på de foreslåede leveringsalternativer fremgår med det samme.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-171">You will immediately see the effect on the suggested delivery alternatives.</span></span> <span data-ttu-id="b6dc8-172">Det er derfor nemt at sammenligne alternativerne.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-172">Therefore, it's easy to compare the alternatives.</span></span>
-   <span data-ttu-id="b6dc8-173">**Medtag indkøb** – Når indkøb er markeret, omfatter de foreslåede leveringsalternativer muligheder for at købe fra både eksterne leverandører og andre firmaer i virksomheden (intern).</span><span class="sxs-lookup"><span data-stu-id="b6dc8-173">**Include procurement** - When procurement is selected, the suggested delivery alternatives include options to procure from both external vendors and other companies in the enterprise (intercompany).</span></span> <span data-ttu-id="b6dc8-174">Indstillingen **Medtag indkøb** understøttes for DTT og DTT + afgangsmargen-leveringsdatokontrol.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-174">The **Include procurement** option is supported for ATP and ATP + Issue margin delivery date control.</span></span> <span data-ttu-id="b6dc8-175">Indstillinger for indkøb fra standardindskøbsleverandøren for produktet og alle godkendte kreditorer for produktet er inkluderet.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-175">Procurement options from the default purchase vendor for the product and all approved vendors for the product are included.</span></span>
-   <span data-ttu-id="b6dc8-176">For eksterne leverandører er beregningen baseret på leveringstiden for indkøbet.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-176">For external vendors, the calculation is based on the purchase lead time.</span></span>
-   <span data-ttu-id="b6dc8-177">Internt indgår det i beregningen, hvad der er tilgængeligt fra forsyningsfirmaet, baseret på leveringsdatokontrol i forsyningsfirmaet.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-177">For intercompany, the calculation considers what is available from the sourcing company, based on delivery date control in the sourcing company.</span></span>
-   <span data-ttu-id="b6dc8-178">**Leveringstype** (Relevant for indkøb)</span><span class="sxs-lookup"><span data-stu-id="b6dc8-178">**Delivery type** (Relevant for procurement)</span></span>
    -   <span data-ttu-id="b6dc8-179">**Lager** - Produkterne leveres fra forsyningslagerstedet til lokationen/lagerstedet på salgslinjen.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-179">**Stock** - Products are shipped from the sourcing warehouse to the site/warehouse on the sales line.</span></span> <span data-ttu-id="b6dc8-180">De sendes derefter fra lagerstedet til kunden.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-180">They are then shipped from that warehouse to the customer.</span></span>
    -   <span data-ttu-id="b6dc8-181">**Direkte levering** - Produkterne leveres direkte til kunden fra forsyningslagerstedet.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-181">**Direct delivery** - Products are shipped directly from the sourcing warehouse to the customer.</span></span>

### <a name="availability-information"></a><span data-ttu-id="b6dc8-182">Oplysninger om tilgængelighed</span><span class="sxs-lookup"><span data-stu-id="b6dc8-182">Availability information</span></span>

<span data-ttu-id="b6dc8-183">Oplysningerne under denne fane er relateret til den alternative leveringslinje, der er valgt.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-183">Information on this tab is related to the delivery alternative line that is selected.</span></span> <span data-ttu-id="b6dc8-184">Følgende oplysninger vises, afhængigt af leveringsdatokontrollen for salgslinjen:</span><span class="sxs-lookup"><span data-stu-id="b6dc8-184">The following information is shown, depending on the delivery date control for the sales line:</span></span>

-   <span data-ttu-id="b6dc8-185">**Salgsleveringstid**</span><span class="sxs-lookup"><span data-stu-id="b6dc8-185">**Sales lead time**</span></span>
    -   <span data-ttu-id="b6dc8-186">**Til rådighed i dag** – Få vist den aktuelle disponible lagerbeholdning, fysisk reserveret og disponibelt fysisk lager.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-186">**Available today** - Show the current physical on-hand, physical reserved, and available physical inventory.</span></span>
    -   <span data-ttu-id="b6dc8-187">**Parametre** - Viser lagerenheden og salgsleveringstiden.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-187">**Parameters** - Show the inventory unit and sales lead time.</span></span>

-   <span data-ttu-id="b6dc8-188">**DTT og DTT + afgangsmargen**</span><span class="sxs-lookup"><span data-stu-id="b6dc8-188">**ATP and ATP + Issue margin**</span></span>
    -   <span data-ttu-id="b6dc8-189">**Til rådighed i dag** – Få vist den aktuelle disponible lagerbeholdning, fysisk reserveret og disponibelt fysisk lager.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-189">**Available today** - Show the current physical on-hand, physical reserved, and available physical inventory.</span></span>
    -   <span data-ttu-id="b6dc8-190">**Parametre** - Viser lagerenheden og salgsleveringstiden.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-190">**Parameters** - Show the inventory unit and sales lead time.</span></span>
    -   <span data-ttu-id="b6dc8-191">**Fremtidig tilgængelighed** – Få vist en grafisk repræsentation af den aktuelle og fremtidige tilgængelighed for valgt lokation og lagersted under **Leveringsalternativer**.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-191">**Future availability** - Show a graphical representation of current and future availability for the selected site and warehouse under **Delivery alternatives**.</span></span> <span data-ttu-id="b6dc8-192">Hvis du vil have vist mere detaljerede oplysninger om produktets tilgængelig fremover, kan du klikke på diagramsøjlerne.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-192">You can click the chart columns to see more detailed information about the future availability of the product.</span></span> <span data-ttu-id="b6dc8-193">Skyderen viser en liste over relevante behovs- og forsyningsordrer i en DTT-tidshorisont.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-193">The slider shows a list of relevant demand and supply orders within the ATP time fence.</span></span>

-   <span data-ttu-id="b6dc8-194">**LE**</span><span class="sxs-lookup"><span data-stu-id="b6dc8-194">**CTP**</span></span>
    -   <span data-ttu-id="b6dc8-195">**Til rådighed i dag** – Få vist den aktuelle disponible lagerbeholdning, fysisk reserveret og disponibelt fysisk lager.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-195">**Available today** - Show the current physical on-hand, physical reserved, and available physical inventory.</span></span>
    -   <span data-ttu-id="b6dc8-196">**Parametre** - Viser lagerenheden og salgsleveringstiden.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-196">**Parameters** - Show the inventory unit and sales lead time.</span></span>
    -   <span data-ttu-id="b6dc8-197">**Udfoldning** – Få vist forsyning for den valgte leveringsalternative udfoldet.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-197">**Explosion** - Show a supply explosion of the selected delivery alternative.</span></span> <span data-ttu-id="b6dc8-198">Du kan bruge **Konfiguration** til at ændre felterne og de lagerdimensioner, der vises i udfoldningen.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-198">You can use **Setup** to change the fields and inventory dimensions that are shown in the explosion.</span></span>

### <a name="impact-of-selected-alternative"></a><span data-ttu-id="b6dc8-199">Virkning af valgt alternativ</span><span class="sxs-lookup"><span data-stu-id="b6dc8-199">Impact of selected alternative</span></span>

<span data-ttu-id="b6dc8-200">Denne fane viser resultatet af det valgte leveringsalternativ fremhævet.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-200">This tab highlights the impact of the selected delivery alternative.</span></span> <span data-ttu-id="b6dc8-201">Hvis du klikker på **OK**, opdateres salgslinjen med de fremhævede værdierne i de markerede kolonner.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-201">If you click **OK**, the sales line is updated with the highlighted values in the SELECTED columns.</span></span> <span data-ttu-id="b6dc8-202">Bemærk, at hvis antallet i det valgte leveringsalternativ er mindre end antallet på salgslinjen, oprettes en leveranceplan, og ordrelinjen opdeles i to linjer: én linje for det valgte antal og én linje for det resterende antal.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-202">Note that, if the quantity on the selected delivery alternative is less than quantity on the sales line, a delivery schedule is created, and the order line is split into two lines: one line for the selected quantity and one line for the remaining quantity.</span></span> <span data-ttu-id="b6dc8-203">Du kan også opdatere den kommercielle linje, så den svarer til linjerne for tidsplanen og påvirker prisfastsættelsen.</span><span class="sxs-lookup"><span data-stu-id="b6dc8-203">You can also update the commercial line so that it matches the schedule lines and affects the pricing.</span></span>

<a name="additional-resources"></a><span data-ttu-id="b6dc8-204">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="b6dc8-204">Additional resources</span></span>
--------

[<span data-ttu-id="b6dc8-205">Ordretilsagn</span><span class="sxs-lookup"><span data-stu-id="b6dc8-205">Order promising</span></span>](delivery-dates-available-promise-calculations.md)




