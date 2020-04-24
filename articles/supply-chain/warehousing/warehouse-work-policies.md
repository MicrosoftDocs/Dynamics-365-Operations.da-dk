---
title: Oversigt over politikker for lagerstedsarbejde
description: Lagerstedets arbejdspolitikker kontrollerer, om lagerstedsarbejde er oprettet af lagerprocesser i produktion, ud fra arbejdsordretype, lagerlokation og produkt.
author: johanhoffmann
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPolicy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 196561
ms.assetid: cbf48ec6-1836-48d5-ad66-a9b534af1786
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 3fe22a92b445abbf6d1dcc67ead878db3f80d532
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204556"
---
# <a name="warehouse-work-policies-overview"></a><span data-ttu-id="0d5b8-103">Oversigt over politikker for lagerstedsarbejde</span><span class="sxs-lookup"><span data-stu-id="0d5b8-103">Warehouse work policies overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0d5b8-104">Lagerstedets arbejdspolitikker kontrollerer, om lagerstedsarbejde er oprettet af lagerprocesser i produktion, ud fra arbejdsordretype, lagerlokation og produkt.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-104">Warehouse work policies control whether warehouse work is created by warehouse processes in manufacturing, based on work order type, inventory location, and product.</span></span>

<span data-ttu-id="0d5b8-105">Denne arbejdspolitik kontrollerer, om lagerstedets arbejde er oprettet for lagerprocesser i produktion.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-105">This work policy controls whether warehouse work is created for warehouse processes in manufacturing.</span></span> <span data-ttu-id="0d5b8-106">Du kan angive arbejdspolitikken ved hjælp af en kombination af **arbejdsordretyper**, en **lagerlokation** og et **produkt**.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-106">You can set up the work policy by using a combination of **work order types**, an **inventory location**, and a **product**.</span></span> <span data-ttu-id="0d5b8-107">Produkt L0101 rapporteres f.eks. som afsluttet til outputlokalitet 001.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-107">For example, product L0101 is reported as finished to output location 001.</span></span> <span data-ttu-id="0d5b8-108">Den færdige vare forbruges senere i en anden produktionsordre på outputlokalitet 001.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-108">The finished good is later consumed in another production order at output location 001.</span></span> <span data-ttu-id="0d5b8-109">I dette tilfælde kan du oprette en arbejdspolitik for at forhindre, at der oprettes arbejde for færdige varer, når du rapporterer produkt L0101 færdig til outputlokalitet 001.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-109">In this case, you can set up a work policy to prevent the work for finished goods put-away from being created when you report product L0101 as finished to output location 001.</span></span> <span data-ttu-id="0d5b8-110">Arbejdspolitikken er en enkelt enhed, der kan beskrives med følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="0d5b8-110">The work policy is an individual entity that can be described through the following information:</span></span>

-   <span data-ttu-id="0d5b8-111">**Navn på arbejdspolitik** (den entydige identifikator for arbejdspolitikken)</span><span class="sxs-lookup"><span data-stu-id="0d5b8-111">**Work policy name** (the unique identifier of the work policy)</span></span>
-   <span data-ttu-id="0d5b8-112">**Arbejdsordretyper** og **Metode til oprettelse af arbejde**</span><span class="sxs-lookup"><span data-stu-id="0d5b8-112">**Work order types** and **Work creation method**</span></span>
-   <span data-ttu-id="0d5b8-113">**Lagerlokationer**</span><span class="sxs-lookup"><span data-stu-id="0d5b8-113">**Inventory locations**</span></span>
-   <span data-ttu-id="0d5b8-114">**Produkter**</span><span class="sxs-lookup"><span data-stu-id="0d5b8-114">**Products**</span></span>

## <a name="work-order-types"></a><span data-ttu-id="0d5b8-115">Arbejdsordretyper</span><span class="sxs-lookup"><span data-stu-id="0d5b8-115">Work order types</span></span>
<span data-ttu-id="0d5b8-116">Du kan vælge mellem følgende arbejdsordretyper:</span><span class="sxs-lookup"><span data-stu-id="0d5b8-116">You can select the following work order types:</span></span>

-   <span data-ttu-id="0d5b8-117">Færdige varer, læg på lager</span><span class="sxs-lookup"><span data-stu-id="0d5b8-117">Finished goods put away</span></span>
-   <span data-ttu-id="0d5b8-118">Samprodukt og biprodukt, læg på lager</span><span class="sxs-lookup"><span data-stu-id="0d5b8-118">Co-product and by-product put away</span></span>
-   <span data-ttu-id="0d5b8-119">Råvarepluk</span><span class="sxs-lookup"><span data-stu-id="0d5b8-119">Raw material picking</span></span>

<span data-ttu-id="0d5b8-120">Feltet **Metode til oprettelse af arbejde** har værdien **Aldrig**.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-120">The **Work creation method** field has the value **Never**.</span></span> <span data-ttu-id="0d5b8-121">Denne værdi angiver, at arbejdspolitikken forhindrer lagerstedsarbejde i at blive oprettet for den valgte arbejdsordretype.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-121">This value indicates that the work policy will prevent warehouse work from being created for the selected work order type.</span></span>

## <a name="inventory-locations"></a><span data-ttu-id="0d5b8-122">Lagerlokationer</span><span class="sxs-lookup"><span data-stu-id="0d5b8-122">Inventory locations</span></span>
<span data-ttu-id="0d5b8-123">Du kan vælge en lokation, der vedrører arbejdspolitikken.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-123">You can select a location that the work policy applies to.</span></span> <span data-ttu-id="0d5b8-124">Hvis ingen lokation er knyttet til en arbejdspolitik, gælder den ikke for alle processer.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-124">If no location is associated with a work policy, the work policy doesn’t apply to any processes.</span></span> <span data-ttu-id="0d5b8-125">På siden **Lokationer** kan du også vælge eller annullere valget af arbejdspolitikken for en bestemt lokation.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-125">On the **Locations** page, you can also select or cancel the selection of the work policy for a specific location.</span></span>

## <a name="products"></a><span data-ttu-id="0d5b8-126">Produkter</span><span class="sxs-lookup"><span data-stu-id="0d5b8-126">Products</span></span>
<span data-ttu-id="0d5b8-127">Du kan vælge et produkt, der vedrører arbejdspolitikken.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-127">You can select a product that the work policy applies to.</span></span> <span data-ttu-id="0d5b8-128">Du kan anvende arbejdspolitikken på alle produkter eller udvalgte produkter.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-128">You can apply the work policy to either all products or selected products.</span></span>

## <a name="example"></a><span data-ttu-id="0d5b8-129">Eksempel</span><span class="sxs-lookup"><span data-stu-id="0d5b8-129">Example</span></span>
<span data-ttu-id="0d5b8-130">I følgende eksempel er der to produktionsordrer, PRD-001 og PRD-00*2*.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-130">In the following example, there are two production orders, PRD-001 and PRD-00*2*.</span></span> <span data-ttu-id="0d5b8-131">Produktionsordre PRD-001 er en handling, der hedder **Assembly**, hvor produktet SC1 færdigmeldes på lokation O1.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-131">Production order PRD-001 has an operation that is named **Assembly**, where product SC1 is being reported as finished to location O1.</span></span> <span data-ttu-id="0d5b8-132">Produktionsordre PRD-002 er en handling, der hedder **Painting** og forbruger produkt SC1 fra lokation O1.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-132">Production order PRD-002 has an operation that is named **Painting** and consumes product SC1 from location O1.</span></span> <span data-ttu-id="0d5b8-133">Produktionsordren PRD-002 forbruger også råvare RM1 fra lokation O1.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-133">Production order PRD-002 also consumes raw material RM1 from location O1.</span></span> <span data-ttu-id="0d5b8-134">RM1 gemmes i lagerlokation BULK-001 og vil blive plukket til lokation O1 af lagerstedets arbejde til råvareplukning.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-134">RM1 is stored in warehouse location BULK-001 and will be picked to location O1 by warehouse work for raw material picking.</span></span> <span data-ttu-id="0d5b8-135">Plukkearbejdet genereres, når produktionen PRD-002 frigives.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-135">The picking work is generated when production PRD-002 is released.</span></span> 

<span data-ttu-id="0d5b8-136">[![Politikker for lagerstedsarbejde](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span><span class="sxs-lookup"><span data-stu-id="0d5b8-136">[![Warehouse work policies](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span></span> 

<span data-ttu-id="0d5b8-137">Når du skal konfigurere lagerstedets arbejdspolitik for dette scenario, skal du overveje følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="0d5b8-137">When you plan to configure a warehouse work policy for this scenario, you should consider the following information:</span></span>

-   <span data-ttu-id="0d5b8-138">Lagerstedets arbejde for færdigvarer, der lægges på lager, er ikke påkrævet, når du færdigmelder produkt SC1 fra produktionsordre PRD-001 til lokation O1.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-138">Warehouse work for finished goods put-away isn’t required when you report product SC1 as finished from production order PRD-001 to location O1.</span></span> <span data-ttu-id="0d5b8-139">Dette skyldes, at **Painting**-operation for produktionsordre PRD-002 forbruger SC1 på samme lokation.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-139">This is because the **Painting** operation for production order PRD-002 consumes SC1 at the same location.</span></span>
-   <span data-ttu-id="0d5b8-140">Lagerstedsarbejde til plukning af råvarer kræves for at flytte råvare RM1 fra lagerlokation BULK-001 til lokation O1.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-140">Warehouse work for raw material picking is required in order to move raw material RM1 from warehouse location BULK-001 to location O1.</span></span>

<span data-ttu-id="0d5b8-141">Her er et eksempel på den politik for arbejde, du har angivet, ud fra disse overvejelser.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-141">Here is an example of the work policy that you can set up, based on these considerations.</span></span>


|                                       |                                       |
|---------------------------------------|---------------------------------------|
| <span data-ttu-id="0d5b8-142"><strong>Navn på arbejdspolitik</strong></span><span class="sxs-lookup"><span data-stu-id="0d5b8-142"><strong>Work policy name</strong></span></span><br> | <span data-ttu-id="0d5b8-143"><strong>Arbejdsordretyper</strong></span><span class="sxs-lookup"><span data-stu-id="0d5b8-143"><strong>Work order types</strong></span></span><br> |
|         <span data-ttu-id="0d5b8-144">Læg ikke på lager 01     \`</span><span class="sxs-lookup"><span data-stu-id="0d5b8-144">No put away 01     \`</span></span>          |     <span data-ttu-id="0d5b8-145">- Færdige varer, læg på lager</span><span class="sxs-lookup"><span data-stu-id="0d5b8-145">- Finished good put away</span></span><br>      |
|                                       |    <span data-ttu-id="0d5b8-146"><strong>Lokationer</strong></span><span class="sxs-lookup"><span data-stu-id="0d5b8-146"><strong>Locations</strong></span></span><br>     |
|                                       |                 <span data-ttu-id="0d5b8-147">- O1</span><span class="sxs-lookup"><span data-stu-id="0d5b8-147">- O1</span></span>                  |
|                                       |    <span data-ttu-id="0d5b8-148"><strong>Produkter</strong></span><span class="sxs-lookup"><span data-stu-id="0d5b8-148"><strong>Products</strong></span></span> <br>     |
|                                       |                 <span data-ttu-id="0d5b8-149">- SC1</span><span class="sxs-lookup"><span data-stu-id="0d5b8-149">- SC1</span></span>                 |

<span data-ttu-id="0d5b8-150">Følgende procedurer indeholder trinvise instruktioner om, hvordan du konfigurerer arbejdspolitikken for lagersted i dette scenario.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-150">The following procedures provide step-by-step instructions about how to set up the warehouse work policy for this scenario.</span></span> <span data-ttu-id="0d5b8-151">En eksempelopsætning, der viser, hvordan du færdigmelder en produktionsordre til en lokation, der ikke er id-kontrolleret, beskrives også.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-151">A sample setup showing how to report a production order as finished to a location that isn’t license plate–controlled is also described.</span></span>

## <a name="set-up-a-warehouse-work-policy"></a><span data-ttu-id="0d5b8-152">Konfigurere en arbejdspolitik for lagersted</span><span class="sxs-lookup"><span data-stu-id="0d5b8-152">Set up a warehouse work policy</span></span>
<span data-ttu-id="0d5b8-153">Lagerstedsprocesser omfatter ikke altid lagerstedsarbejde.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-153">Warehouse processes don’t always include warehouse work.</span></span> <span data-ttu-id="0d5b8-154">Ved at definere en arbejdspolitik kan du forhindre oprettelse af arbejde med pluk af råmaterialer og placering af færdigvarer på lager for en række produkter på bestemte lokationer.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-154">By defining a work policy, you can prevent the creation of work for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span> <span data-ttu-id="0d5b8-155">Demodatafirmaet USMF bruges til at oprette denne procedure.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-155">The USMF demo data company was used to create this procedure.</span></span> 

<span data-ttu-id="0d5b8-156">TRIN (21)</span><span class="sxs-lookup"><span data-stu-id="0d5b8-156">STEPS (21)</span></span>

|     |                                                                            |
|-----|----------------------------------------------------------------------------|
| <span data-ttu-id="0d5b8-157">1</span><span class="sxs-lookup"><span data-stu-id="0d5b8-157">1.</span></span>  | <span data-ttu-id="0d5b8-158">Gå til Lagerstyring &gt; Konfiguration &gt; Arbejde &gt; Arbejdspolitikker.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-158">Go to Warehouse management &gt; Setup &gt; Work &gt; Work policies.</span></span>        |
| <span data-ttu-id="0d5b8-159">2</span><span class="sxs-lookup"><span data-stu-id="0d5b8-159">2.</span></span>  | <span data-ttu-id="0d5b8-160">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-160">Click New.</span></span>                                                                 |
| <span data-ttu-id="0d5b8-161">3</span><span class="sxs-lookup"><span data-stu-id="0d5b8-161">3.</span></span>  | <span data-ttu-id="0d5b8-162">Skriv 'Ikke læg-på-lager-arbejde' i navnefeltet Arbejdspolitik.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-162">In the Work policy name field, type 'No put-away work'.</span></span>                    |
| <span data-ttu-id="0d5b8-163">4</span><span class="sxs-lookup"><span data-stu-id="0d5b8-163">4.</span></span>  | <span data-ttu-id="0d5b8-164">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-164">Click Save.</span></span>                                                                |
| <span data-ttu-id="0d5b8-165">5</span><span class="sxs-lookup"><span data-stu-id="0d5b8-165">5.</span></span>  | <span data-ttu-id="0d5b8-166">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-166">Click Add.</span></span>                                                                 |
| <span data-ttu-id="0d5b8-167">6</span><span class="sxs-lookup"><span data-stu-id="0d5b8-167">6.</span></span>  | <span data-ttu-id="0d5b8-168">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-168">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="0d5b8-169">7</span><span class="sxs-lookup"><span data-stu-id="0d5b8-169">7.</span></span>  | <span data-ttu-id="0d5b8-170">Vælg 'Færdige varer lægges på lager' i feltet Arbejdsordretype.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-170">In the Work order type field, select 'Finished goods put away'.</span></span>            |
| <span data-ttu-id="0d5b8-171">8</span><span class="sxs-lookup"><span data-stu-id="0d5b8-171">8.</span></span>  | <span data-ttu-id="0d5b8-172">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-172">Click Add.</span></span>                                                                 |
| <span data-ttu-id="0d5b8-173">9</span><span class="sxs-lookup"><span data-stu-id="0d5b8-173">9.</span></span>  | <span data-ttu-id="0d5b8-174">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-174">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="0d5b8-175">10.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-175">10.</span></span> | <span data-ttu-id="0d5b8-176">Vælg 'Samprodukter eller biprodukter, der er lagt på lager' i feltet Arbejdsordretype.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-176">In the Work order type field, select 'Co-product and by-product put away'.</span></span> |
| <span data-ttu-id="0d5b8-177">11.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-177">11.</span></span> | <span data-ttu-id="0d5b8-178">Udvid sektionen Lagerlokationer.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-178">Expand the Inventory locations section.</span></span>                                    |
| <span data-ttu-id="0d5b8-179">12.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-179">12.</span></span> | <span data-ttu-id="0d5b8-180">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-180">Click Add.</span></span>                                                                 |
| <span data-ttu-id="0d5b8-181">13</span><span class="sxs-lookup"><span data-stu-id="0d5b8-181">13.</span></span> | <span data-ttu-id="0d5b8-182">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-182">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="0d5b8-183">14.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-183">14.</span></span> | <span data-ttu-id="0d5b8-184">Indtast '51' på lagerstedslisten.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-184">In the Warehouse list, enter '51'.</span></span>                                         |
| <span data-ttu-id="0d5b8-185">15.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-185">15.</span></span> | <span data-ttu-id="0d5b8-186">Indtast eller vælg '001' i feltet Lokation.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-186">In the Location field, enter or select '001'.</span></span>                              |
| <span data-ttu-id="0d5b8-187">16.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-187">16.</span></span> | <span data-ttu-id="0d5b8-188">Udvid afsnittet Produkter.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-188">Expand the Products section.</span></span>                                               |
| <span data-ttu-id="0d5b8-189">17.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-189">17.</span></span> | <span data-ttu-id="0d5b8-190">Vælg 'Valgt' i feltet Produktvalg.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-190">In the Product selection field, select 'Selected'.</span></span>                         |
| <span data-ttu-id="0d5b8-191">18.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-191">18.</span></span> | <span data-ttu-id="0d5b8-192">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-192">Click Add.</span></span>                                                                 |
| <span data-ttu-id="0d5b8-193">19.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-193">19.</span></span> | <span data-ttu-id="0d5b8-194">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-194">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="0d5b8-195">20.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-195">20.</span></span> | <span data-ttu-id="0d5b8-196">Indtast eller vælg 'L0101' i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-196">In the Item number field, enter or select 'L0101'.</span></span>                         |
| <span data-ttu-id="0d5b8-197">21.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-197">21.</span></span> | <span data-ttu-id="0d5b8-198">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-198">Click Save.</span></span>                                                                |

## <a name="report-a-production-order-as-finished-to-a-location-that-isnt-license-platecontrolled"></a><span data-ttu-id="0d5b8-199">Færdigmelde en produktionsordre til en lokation, der ikke er id-kontrolleret</span><span class="sxs-lookup"><span data-stu-id="0d5b8-199">Report a production order as finished to a location that isn’t license plate–controlled</span></span>
<span data-ttu-id="0d5b8-200">Denne procedure viser et eksempel på færdigmelding til en lokation, der ikke er id-kontrolleret.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-200">This procedure shows an example of reporting as finished to a location that isn't license plate–controlled.</span></span> <span data-ttu-id="0d5b8-201">En relevant arbejdspolitik er en forudsætning for denne opgave.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-201">An applicable work policy is the prerequisite for this task.</span></span> <span data-ttu-id="0d5b8-202">Foregående procedure viser konfigurationen af arbejdspolitikken.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-202">The previous procedure shows the setup of the work policy.</span></span> 

<span data-ttu-id="0d5b8-203">TRIN (25)</span><span class="sxs-lookup"><span data-stu-id="0d5b8-203">STEPS (25)</span></span>

<table>
<tbody>
<tr>
<td colspan="3"><span data-ttu-id="0d5b8-204"><strong>Underopgave: Konfigurere en outputlokation.</strong></span><span class="sxs-lookup"><span data-stu-id="0d5b8-204"><strong>Sub-task: Set up an output location.</strong></span></span></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td><span data-ttu-id="0d5b8-205">Gå til Virksomhedsadministration &gt; Ressourcer &gt; Ressourcegrupper.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-205">Go to Organization administration &gt; Resources &gt; Resource groups.</span></span></td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td><span data-ttu-id="0d5b8-206">Vælg ressourcegruppen '5102' på listen.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-206">In the list, select resource group &#39;5102&#39;.</span></span></td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td><span data-ttu-id="0d5b8-207">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-207">Click Edit.</span></span></td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td><span data-ttu-id="0d5b8-208">Indtast '51' i feltet Lagersted for udlagring.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-208">In the Output warehouse field, enter &#39;51&#39;.</span></span></td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td><span data-ttu-id="0d5b8-209">Indtast '001' i feltet Udlagringslokation.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-209">In the Output location field, enter &#39;001&#39;.</span></span></td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td><span data-ttu-id="0d5b8-210">Lokationen 001 er ikke en id-kontrolleret lokation.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-210">Location 001 isn&#39;t a license plate–controlled location.</span></span> <span data-ttu-id="0d5b8-211">Du kan kun konfigurere en outputplacering uden id-kontrol, hvis der findes en gyldig arbejdspolitik for lokationen.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-211">You can set up a non–license plate output location only if an applicable work policy exists for the location.</span></span></td>
</tr>
<tr>
<td colspan="3"><span data-ttu-id="0d5b8-212"><strong>Underopgave: Oprette en produktionsordre og rapportere den som færdig.</strong></span><span class="sxs-lookup"><span data-stu-id="0d5b8-212"><strong>Sub-task: Create a production order and report it as finished.</strong></span></span></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td><span data-ttu-id="0d5b8-213">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-213">Close the page.</span></span></td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td><span data-ttu-id="0d5b8-214">Gå til Produktionsstyring &gt; Produktionsordrer &gt; Alle produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-214">Go to Production control &gt; Production orders &gt; All production orders.</span></span></td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td><span data-ttu-id="0d5b8-215">Klik på Ny produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-215">Click New production order.</span></span></td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td><span data-ttu-id="0d5b8-216">Indtast 'L0101' i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-216">In the Item number field, enter &#39;L0101&#39;.</span></span></td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td><span data-ttu-id="0d5b8-217">Klik på Opret.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-217">Click Create.</span></span></td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td><span data-ttu-id="0d5b8-218">Klik på Produktionsordre i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-218">On the Action Pane, click Production order.</span></span></td>
</tr>
<tr>
<td></td>
<td>7.</td>
<td><span data-ttu-id="0d5b8-219">Klik på Forkalkulation.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-219">Click Estimate.</span></span></td>
</tr>
<tr>
<td></td>
<td>8.</td>
<td><span data-ttu-id="0d5b8-220">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-220">Click OK.</span></span></td>
</tr>
<tr>
<td></td>
<td>9.</td>
<td><span data-ttu-id="0d5b8-221">Klik på Start.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-221">Click Start.</span></span></td>
</tr>
<tr>
<td></td>
<td>10.</td>
<td><span data-ttu-id="0d5b8-222">Klik på fanen Generelt.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-222">Click the General tab.</span></span></td>
</tr>
<tr>
<td></td>
<td>11.</td>
<td><span data-ttu-id="0d5b8-223">Vælg 'Aldrig' i feltet Automatisk styklisteforbrug.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-223">In the Automatic BOM consumption field, select &#39;Never&#39;.</span></span></td>
</tr>
<tr>
<td></td>
<td>12.</td>
<td><span data-ttu-id="0d5b8-224">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-224">Click OK.</span></span></td>
</tr>
<tr>
<td></td>
<td>13.</td>
<td><span data-ttu-id="0d5b8-225">Klik på Færdigmelding.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-225">Click Report as finished.</span></span></td>
</tr>
<tr>
<td></td>
<td>14.</td>
<td><span data-ttu-id="0d5b8-226">Klik på fanen Generelt.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-226">Click the General tab.</span></span></td>
</tr>
<tr>
<td></td>
<td>15.</td>
<td><span data-ttu-id="0d5b8-227">Vælg Ja i feltet Accepter fejl.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-227">Select Yes in the Accept error field.</span></span></td>
</tr>
<tr>
<td></td>
<td>16.</td>
<td><span data-ttu-id="0d5b8-228">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-228">Click OK.</span></span></td>
</tr>
<tr>
<td></td>
<td>17.</td>
<td><span data-ttu-id="0d5b8-229">Klik på Lagersted i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-229">On the Action Pane, click Warehouse.</span></span></td>
</tr>
<tr>
<td></td>
<td>18.</td>
<td><span data-ttu-id="0d5b8-230">Klik på Arbejdsdetaljer.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-230">Click Work details.</span></span></td>
</tr>
<tr>
<td></td>
<td>19.</td>
<td><span data-ttu-id="0d5b8-231">Når produktionsordren er færdigmeldt, oprettes der intet arbejde for læg-på-lager.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-231">When the production order was reported as finished, no work was generated for put-away.</span></span> <span data-ttu-id="0d5b8-232">Dette skyldes, at der er defineret en arbejdspolitik, som forhindrer, at der genereres arbejde, når produktet L0101 rapporteres som færdigt på lokation 001.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-232">This occurs because a work policy is defined that prevents work from being generated when product L0101 is reported as finished to location 001.</span></span></td>
</tr>
</tbody>
</table>



