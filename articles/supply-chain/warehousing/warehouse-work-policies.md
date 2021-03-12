---
title: Arbejdspolitikker
description: I dette emne forklares, hvordan du konfigurerer arbejdspolitikker.
author: perlynne
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPolicy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 530abffb4c80a2d2f0e58e0c5a34294f7cba0b1a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4998447"
---
# <a name="work-policies"></a><span data-ttu-id="ec942-103">Arbejdspolitikker</span><span class="sxs-lookup"><span data-stu-id="ec942-103">Work policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ec942-104">I dette emne forklares, hvordan du kan konfigurere systemet og lagerstedsappen, så de understøtter arbejdspolitikker.</span><span class="sxs-lookup"><span data-stu-id="ec942-104">This topic explains how to set up the system and the warehouse app so that they support work policies.</span></span> <span data-ttu-id="ec942-105">Du kan bruge denne funktion til hurtigt at registrere lagerbeholdningen uden at oprette læg på lager-arbejde, når du modtager indkøbs- eller flytteordrer, eller når du fuldfører produktionsprocesser.</span><span class="sxs-lookup"><span data-stu-id="ec942-105">You can use this functionality to quickly register inventory without creating putaway work when you receive purchase or transfer orders, or when you complete manufacturing processes.</span></span> <span data-ttu-id="ec942-106">Dette emne indeholder generelle oplysninger.</span><span class="sxs-lookup"><span data-stu-id="ec942-106">This topic provides general information.</span></span> <span data-ttu-id="ec942-107">Du kan finde detaljerede oplysninger, der er relateret til id-modtagelse, under [Modtagelse af id via lagerstedsappen](warehousing-mobile-device-app-license-plate-receiving.md).</span><span class="sxs-lookup"><span data-stu-id="ec942-107">For detailed information that is related to license plate receiving, see [License plate receiving via the warehouse app](warehousing-mobile-device-app-license-plate-receiving.md).</span></span>

<span data-ttu-id="ec942-108">En arbejdspolitik styrer, om der oprettes lagerstedsarbejde, når en produceret vare færdigmeldes, eller når varer modtages ved hjælp af lagerstedsappen.</span><span class="sxs-lookup"><span data-stu-id="ec942-108">A work policy controls whether warehouse work is created when a manufactured item is reported as finished, or when goods are received by using the warehouse app.</span></span> <span data-ttu-id="ec942-109">Du konfigurerer hver arbejdspolitik ved at definere de betingelser, der gælder: arbejdsordretyper og processer, lagerlokation og (valgfrit) produkter.</span><span class="sxs-lookup"><span data-stu-id="ec942-109">You set up each work policy by defining the conditions where it applies: the work order types and processes, the inventory location, and (optionally) the products.</span></span> <span data-ttu-id="ec942-110">En indkøbsordre på produkt *A0001* skal f.eks. modtages på lokation *RECV* på lagersted *24*.</span><span class="sxs-lookup"><span data-stu-id="ec942-110">For example, a purchase order for product *A0001* must be received in location *RECV* in warehouse *24*.</span></span> <span data-ttu-id="ec942-111">Senere forbruges produktet i en anden proces på lokation *RECV*.</span><span class="sxs-lookup"><span data-stu-id="ec942-111">Later, the product is consumed in another process at location *RECV*.</span></span> <span data-ttu-id="ec942-112">I dette tilfælde kan du konfigurere en arbejdspolitik for at forhindre, at læg på lager-arbejde oprettes, når en arbejder rapporterer, at produkt *A0001* er modtaget på lokation *RECV*.</span><span class="sxs-lookup"><span data-stu-id="ec942-112">In this case, you can set up a work policy to prevent putaway work from being created when a worker reports product *A0001* as received in location *RECV*.</span></span>

> [!NOTE]
> - <span data-ttu-id="ec942-113">Hvis en arbejdspolitik skal være aktiv, skal du definere mindst én lokation for den i oversigtspanelet **Lagerlokationer** på siden **Arbejdspolitikker**.</span><span class="sxs-lookup"><span data-stu-id="ec942-113">For a work policy to be active, you must define at least one location for it on the **Inventory locations** FastTab of the **Work policies** page.</span></span> 
> - <span data-ttu-id="ec942-114">Du kan ikke angive den samme placering for flere arbejdspolitikker.</span><span class="sxs-lookup"><span data-stu-id="ec942-114">You can't specify the same location for multiple work policies.</span></span>
> - <span data-ttu-id="ec942-115">Indstillingen **Udskriv label** til mobilenhedens menupunkter udskriver ikke en id-label, medmindre arbejde er oprettet.</span><span class="sxs-lookup"><span data-stu-id="ec942-115">The **Print label** option for mobile device menu items won't print a license plate label unless work was created.</span></span>

## <a name="activate-the-features-in-your-system"></a><span data-ttu-id="ec942-116">Aktivere funktionerne i systemet</span><span class="sxs-lookup"><span data-stu-id="ec942-116">Activate the features in your system</span></span>

<span data-ttu-id="ec942-117">Hvis du vil gøre alle funktioner, der beskrives i dette emne, tilgængelige i systemet, skal du aktivere følgende to funktioner i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):</span><span class="sxs-lookup"><span data-stu-id="ec942-117">To make all the functionality that is described in this topic available in your system, turn on the following two features in [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):</span></span>

- <span data-ttu-id="ec942-118">Forbedringer af modtagelse af id</span><span class="sxs-lookup"><span data-stu-id="ec942-118">License plate receiving enhancements</span></span>
- <span data-ttu-id="ec942-119">Forbedringer af arbejdspolitikker for indgående arbejde</span><span class="sxs-lookup"><span data-stu-id="ec942-119">Work policy enhancements for inbound work</span></span>

## <a name="the-work-policies-page"></a><span data-ttu-id="ec942-120">Siden arbejdspolitikker</span><span class="sxs-lookup"><span data-stu-id="ec942-120">The Work policies page</span></span>

<span data-ttu-id="ec942-121">Hvis du vil konfigurere arbejdspolitikker, skal du gå til **Lokationsstyring \> Konfiguration \> Arbejde \> Arbejdspolitikker**.</span><span class="sxs-lookup"><span data-stu-id="ec942-121">To set up work policies, go to **Warehouse management \> Setup \> Work \> Work policies**.</span></span> <span data-ttu-id="ec942-122">Derefter skal du i hvert oversigtspanel angive felterne som beskrevet i følgende underafsnit.</span><span class="sxs-lookup"><span data-stu-id="ec942-122">Then, on each FastTab, set the fields as described in the following subsections.</span></span>

### <a name="the-work-order-types-fasttab"></a><span data-ttu-id="ec942-123">Oversigtspanelet Arbejdsordretyper</span><span class="sxs-lookup"><span data-stu-id="ec942-123">The Work order types FastTab</span></span>

<span data-ttu-id="ec942-124">I oversigtspanelet **Arbejdsordretyper** skal du tilføje alle arbejdsordretyper og de relaterede arbejdsprocesser, som arbejdspolitikken gælder for.</span><span class="sxs-lookup"><span data-stu-id="ec942-124">On the **Work order types** FastTab, add all the work order types, and the related work processes, that the work policy applies to.</span></span> <span data-ttu-id="ec942-125">Følgende arbejdsordretyper og relaterede arbejdsprocesser understøttes for arbejdspolitikker.</span><span class="sxs-lookup"><span data-stu-id="ec942-125">The following work order types and related work processes are supported for work policies.</span></span>

| <span data-ttu-id="ec942-126">Arbejdsordretype</span><span class="sxs-lookup"><span data-stu-id="ec942-126">Work order type</span></span> | <span data-ttu-id="ec942-127">Arbejdsproces</span><span class="sxs-lookup"><span data-stu-id="ec942-127">Work process</span></span> |
|---|---|
| <span data-ttu-id="ec942-128">Råvarepluk</span><span class="sxs-lookup"><span data-stu-id="ec942-128">Raw material picking</span></span>| <span data-ttu-id="ec942-129">Alle relaterede processer</span><span class="sxs-lookup"><span data-stu-id="ec942-129">All related processes</span></span> |
| <span data-ttu-id="ec942-130">Samprodukt og biprodukt, læg på lager</span><span class="sxs-lookup"><span data-stu-id="ec942-130">Co-product and by-product put away</span></span> | <span data-ttu-id="ec942-131">Alle relaterede processer</span><span class="sxs-lookup"><span data-stu-id="ec942-131">All related processes</span></span> |
| <span data-ttu-id="ec942-132">Færdige varer, læg på lager</span><span class="sxs-lookup"><span data-stu-id="ec942-132">Finished goods putaway</span></span> | <span data-ttu-id="ec942-133">Alle relaterede processer</span><span class="sxs-lookup"><span data-stu-id="ec942-133">All related processes</span></span> |
| <span data-ttu-id="ec942-134">Tilgang for overførsel</span><span class="sxs-lookup"><span data-stu-id="ec942-134">Transfer receipt</span></span> | <span data-ttu-id="ec942-135">Modtagelse af id (og læg på lager)</span><span class="sxs-lookup"><span data-stu-id="ec942-135">License plate receiving (and putaway)</span></span> |
| <span data-ttu-id="ec942-136">Indkøbsordrer</span><span class="sxs-lookup"><span data-stu-id="ec942-136">Purchase orders</span></span> | <ul><li><span data-ttu-id="ec942-137">Modtagelse af id (og læg på lager)</span><span class="sxs-lookup"><span data-stu-id="ec942-137">License plate receiving (and putaway)</span></span></li><li><span data-ttu-id="ec942-138">Modtagelse af varelast (og læg på lager)</span><span class="sxs-lookup"><span data-stu-id="ec942-138">Load item receiving (and putaway)</span></span></li><li><span data-ttu-id="ec942-139">Indkøbsordrelinje til modtagelse (og læg på lager)</span><span class="sxs-lookup"><span data-stu-id="ec942-139">Purchase order line receiving (and putaway)</span></span></li><li><span data-ttu-id="ec942-140">Indkøbsordrevare til modtagelse (og læg på lager)</span><span class="sxs-lookup"><span data-stu-id="ec942-140">Purchase order item receiving (and putaway)</span></span></li></ul> |

<span data-ttu-id="ec942-141">Hvis du vil oprette en arbejdspolitik, så den gælder for flere arbejdsprocesser med samme arbejdsordretype, skal du føje en separat linje for hver arbejdsproces til gitteret.</span><span class="sxs-lookup"><span data-stu-id="ec942-141">To set up a work policy so that it applies to several work processes of the same work order type, add a separate line for each work process to the grid.</span></span>

<span data-ttu-id="ec942-142">For hver linje i gitteret skal du angive feltet **Metode til oprettelse af arbejde** til en af følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="ec942-142">For each line in the grid, set the **Work creation method** field to one of the following values:</span></span>

- <span data-ttu-id="ec942-143">**Aldrig** – Arbejdspolitikken forhindrer lagerstedsarbejde i at blive oprettet for den valgte arbejdsordretype og relaterede arbejdsproces.</span><span class="sxs-lookup"><span data-stu-id="ec942-143">**Never** – The work policy will prevent warehouse work from being created for the selected work order type and related work process.</span></span>
- <span data-ttu-id="ec942-144">**Cross-docking** – Arbejdspolitikken opretter cross-docking-arbejde ved hjælp af den politik, du vælger i feltet **Navn på politik for cross-docking**.</span><span class="sxs-lookup"><span data-stu-id="ec942-144">**Cross docking** – The work policy will create cross-docking work by using the policy that you select in the **Cross docking policy name** field.</span></span>

### <a name="the-inventory-locations-fasttab"></a><span data-ttu-id="ec942-145">Oversigtspanelet Lagerlokationer</span><span class="sxs-lookup"><span data-stu-id="ec942-145">The Inventory locations FastTab</span></span>

<span data-ttu-id="ec942-146">Tilføj alle de lokationer, hvor denne arbejdspolitik skal anvendes, i oversigtspanelet **Lagerlokationer**.</span><span class="sxs-lookup"><span data-stu-id="ec942-146">On the **Inventory locations** FastTab, add all the locations where this work policy should be applied.</span></span> <span data-ttu-id="ec942-147">Hvis ingen lokation er knyttet til en arbejdspolitik, gælder arbejdspolitikken ikke for nogen proces.</span><span class="sxs-lookup"><span data-stu-id="ec942-147">If no location is associated with a work policy, the work policy won't be applied to any process.</span></span>

<span data-ttu-id="ec942-148">Du kan ikke angive den samme placering for flere arbejdspolitikker.</span><span class="sxs-lookup"><span data-stu-id="ec942-148">You can't specify the same location for multiple work policies.</span></span>

<span data-ttu-id="ec942-149">Det er muligt at bruge en lagerlokation, der er tildelt en lokationsprofil, når **Brug nummerpladesporing** er slået fra.</span><span class="sxs-lookup"><span data-stu-id="ec942-149">You can use a warehouse location that is assigned to a location profile where the **Use license plate tracking** option is turned off.</span></span> <span data-ttu-id="ec942-150">I dette tilfælde vil arbejderne direkte registrere den disponible lagerbeholdning.</span><span class="sxs-lookup"><span data-stu-id="ec942-150">In this case, workers will directly register the on-hand inventory.</span></span>

### <a name="the-products-fasttab"></a><span data-ttu-id="ec942-151">Oversigtspanelet Produkter</span><span class="sxs-lookup"><span data-stu-id="ec942-151">The Products FastTab</span></span>

<span data-ttu-id="ec942-152">Under fanen **Produkter** skal du angive feltet **Produktvalg** for at styre, hvilke produkter politikken skal gælde for:</span><span class="sxs-lookup"><span data-stu-id="ec942-152">On the **Products** tab, set the **Product selection** field to control which products the policy should apply to:</span></span>

- <span data-ttu-id="ec942-153">**Alle** – Politikken skal gælde for alle produkter.</span><span class="sxs-lookup"><span data-stu-id="ec942-153">**All** – The policy should apply to all products.</span></span>
- <span data-ttu-id="ec942-154">**Valgte** – Politikken skal kun gælde for produkter, der er angivet i gitteret.</span><span class="sxs-lookup"><span data-stu-id="ec942-154">**Selected** – The policy should apply only to products that are listed in the grid.</span></span> <span data-ttu-id="ec942-155">Brug værktøjslinjen i oversigtspanelet **Produkter** til at føje produkter til gitteret eller fjerne dem fra gitteret.</span><span class="sxs-lookup"><span data-stu-id="ec942-155">Use the toolbar on the **Products** FastTab to add products to the grid or remove them from the grid.</span></span>

## <a name="default-and-custom-to-locations"></a><span data-ttu-id="ec942-156">Standard- og brugerdefinerede "til"-lokationer</span><span class="sxs-lookup"><span data-stu-id="ec942-156">Default and custom "to" locations</span></span>

> [!NOTE]
> <span data-ttu-id="ec942-157">Hvis du vil gøre den funktionalitet, der er beskrevet i dette afsnit, tilgængelig i systemet, skal du aktivere *Forbedringer af modtagelse af id* og *Forbedringer af arbejdspolitikken, for indgående arbejde* i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ec942-157">To make the functionality that is described in this section available in your system, you must turn on the *License plate receiving enhancements* and *Work policy enhancements for inbound work* features in [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

<span data-ttu-id="ec942-158">Tidligere understøttede systemet kun modtagelse på den standardplacering, der er defineret for hvert lagersted.</span><span class="sxs-lookup"><span data-stu-id="ec942-158">Previously, the system supported receiving only at the default location that is defined for each warehouse.</span></span> <span data-ttu-id="ec942-159">Men menupunkterne i mobilenheder, der bruger følgende processer til oprettelse af arbejdsopgaver, indeholder nu indstillingen **Brug standarddata**.</span><span class="sxs-lookup"><span data-stu-id="ec942-159">However, mobile device menu items that use the following work creation processes now provide the **Use default data** option.</span></span> <span data-ttu-id="ec942-160">Med denne indstilling kan du tildele en brugerdefineret "til"-lokation til et eller flere menupunkter.</span><span class="sxs-lookup"><span data-stu-id="ec942-160">This option lets you assign a custom "to" location to one or more menu items.</span></span> <span data-ttu-id="ec942-161">(Denne indstilling var allerede tilgængelig for andre typer menupunkter).</span><span class="sxs-lookup"><span data-stu-id="ec942-161">(This option was already available for some other types of menu items.)</span></span>

- <span data-ttu-id="ec942-162">Modtagelse af id (og læg på lager)</span><span class="sxs-lookup"><span data-stu-id="ec942-162">License plate receiving (and putaway)</span></span>
- <span data-ttu-id="ec942-163">Modtagelse af varelast (og læg på lager)</span><span class="sxs-lookup"><span data-stu-id="ec942-163">Load item receiving (and putaway)</span></span>
- <span data-ttu-id="ec942-164">Indkøbsordrelinje til modtagelse (og læg på lager)</span><span class="sxs-lookup"><span data-stu-id="ec942-164">Purchase order line receiving (and putaway)</span></span>
- <span data-ttu-id="ec942-165">Indkøbsordrevare til modtagelse (og læg på lager)</span><span class="sxs-lookup"><span data-stu-id="ec942-165">Purchase order item receiving (and putaway)</span></span>

<span data-ttu-id="ec942-166">Indstillingen **Til lokation** for et menupunkt tilsidesætter standardplaceringen for modtagelse på lagerstedet for alle ordrer, der behandles ved hjælp af dette menupunkt.</span><span class="sxs-lookup"><span data-stu-id="ec942-166">The **To location** setting for a menu item overrides the default receiving location for the warehouse, for all orders that are processed by using that menu item.</span></span>

<span data-ttu-id="ec942-167">Hvis du vil konfigurere et menupunkt for mobilenheden til at understøtte modtagelse på en brugerdefineret lokation, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="ec942-167">To set up a mobile device menu item to support receiving at a custom location, follow these steps.</span></span>

1. <span data-ttu-id="ec942-168">Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Menupunkter i mobilenhed**.</span><span class="sxs-lookup"><span data-stu-id="ec942-168">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="ec942-169">Vælg eller opret et menupunkt, der bruger en af de processer til oprettelse af arbejde, der er angivet tidligere i dette afsnit.</span><span class="sxs-lookup"><span data-stu-id="ec942-169">Select or create a menu item that uses one of the work creation processes that are listed earlier in this section.</span></span>
1. <span data-ttu-id="ec942-170">I oversigtspanelet **Generelt** skal du angive indstillingen **Brug standarddata** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="ec942-170">On the **General** FastTab, set the **Use default data** option to **Yes**.</span></span>
1. <span data-ttu-id="ec942-171">Vælg **Standarddata** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="ec942-171">On the Action Pane, select **Default data**.</span></span>
1. <span data-ttu-id="ec942-172">På siden **Standarddata** kan du angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="ec942-172">On the **Default data** page, set the following values:</span></span>

    - <span data-ttu-id="ec942-173">**Feltet Standarddata:** Indstil dette felt til *Til lokation*.</span><span class="sxs-lookup"><span data-stu-id="ec942-173">**Default data field:** Set this field to *To location*.</span></span>
    - <span data-ttu-id="ec942-174">**Lagersted:** Vælg det destinationslagersted, der skal bruges til dette menupunkt.</span><span class="sxs-lookup"><span data-stu-id="ec942-174">**Warehouse:** Select the destination warehouse to use with this menu item.</span></span>
    - <span data-ttu-id="ec942-175">**Lokation:** Dette felt viser alle de lokations-id'er, der er tilgængelige for det valgte lagersted.</span><span class="sxs-lookup"><span data-stu-id="ec942-175">**Location:** This field lists all the location IDs that are available for the selected warehouse.</span></span> <span data-ttu-id="ec942-176">Indstillingen i dette felt har dog ikke nogen virkning.</span><span class="sxs-lookup"><span data-stu-id="ec942-176">However, the setting of this field doesn't actually have any effect.</span></span> <span data-ttu-id="ec942-177">Du kan derfor lade feltet være tomt.</span><span class="sxs-lookup"><span data-stu-id="ec942-177">Therefore, you can leave it blank.</span></span> <span data-ttu-id="ec942-178">Du kan dog bruge listen til at bekræfte det id, du skal angive i feltet **Hardcodet værdi**.</span><span class="sxs-lookup"><span data-stu-id="ec942-178">Nevertheless, you can use the list to confirm the ID that you must enter in the **Hardcoded value** field.</span></span>
    - <span data-ttu-id="ec942-179">**Hardcodet værdi:** Angiv lokalitets-id'et for den modtagende lokation, der gælder for dette menupunkt.</span><span class="sxs-lookup"><span data-stu-id="ec942-179">**Hardcoded value:** Enter the location ID for the receiving location that applies to this menu item.</span></span>

> [!TIP]
> <span data-ttu-id="ec942-180">Der kan kun anvendes en arbejdspolitik, hvis alle de modtagende lokationer er angivet i den relevante opsætning af arbejdspolitik.</span><span class="sxs-lookup"><span data-stu-id="ec942-180">A work policy can be applied only if all the receiving locations are listed in the relevant work policy setup.</span></span> <span data-ttu-id="ec942-181">Dette krav gælder, uanset om du bruger standardlokationen for modtagelse på lagersted eller en brugerdefineret "til"-lokation.</span><span class="sxs-lookup"><span data-stu-id="ec942-181">This requirement applies regardless of whether you're using the default warehouse receiving location or a custom "to" location.</span></span>

## <a name="example-scenario-warehouse-receiving"></a><span data-ttu-id="ec942-182">Eksempelscenario: modtagelse på lagerstedet</span><span class="sxs-lookup"><span data-stu-id="ec942-182">Example scenario: Warehouse receiving</span></span>

<span data-ttu-id="ec942-183">Alle produkter, der modtages af processen *Indkøbsordrevare til modtagelse (og læg på lager)*, skal være registreret i lokation *FL-001*, og de skal være tilgængelige på lagersted *24*.</span><span class="sxs-lookup"><span data-stu-id="ec942-183">All products that are received by the *Purchase order item receiving (and putaway)* process must be registered in location *FL-001*, and they must be available in warehouse *24*.</span></span> <span data-ttu-id="ec942-184">Der skal dog ikke oprettes arbejde.</span><span class="sxs-lookup"><span data-stu-id="ec942-184">However, work should not be created.</span></span> <span data-ttu-id="ec942-185">Produkter, der modtages af enhver anden proces (dvs. ved hjælp af andre menupunkter i mobilenheder), skal registreres på standardlagerstedets modtagelseslokation (*RECV*), og der skal oprettes arbejde som normalt.</span><span class="sxs-lookup"><span data-stu-id="ec942-185">Products that are received by any other process (that is, by using other mobile device menu items) should be registered at the default warehouse receiving location (*RECV*), and work should be created as usual.</span></span> <span data-ttu-id="ec942-186">(Dette scenarie viser ikke den standardopsætning af modtagelse).</span><span class="sxs-lookup"><span data-stu-id="ec942-186">(This scenario doesn't show the default receiving setup.)</span></span>

<span data-ttu-id="ec942-187">Dette scenario kræver følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="ec942-187">This scenario requires the following elements:</span></span>

- <span data-ttu-id="ec942-188">En arbejdspolitik til processen *Indkøbsordrevare til modtagelse (og læg på lager)* i lokation *FL-001* for alle produkter</span><span class="sxs-lookup"><span data-stu-id="ec942-188">A work policy for the *Purchase order item receiving (and putaway)* process in location *FL-001*, for all products</span></span>
- <span data-ttu-id="ec942-189">Et menupunkt i mobilenheden, der indeholder standarddata, og som angiver feltet **Til lokation** til *FL-001*</span><span class="sxs-lookup"><span data-stu-id="ec942-189">A mobile device menu item that has default data, and that sets the **To location** field to *FL-001*</span></span>

### <a name="prerequisites"></a><span data-ttu-id="ec942-190">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="ec942-190">Prerequisites</span></span>

<span data-ttu-id="ec942-191">Hvis du vil gøre den funktionalitet, der er beskrevet i dette scenarie, tilgængelig i systemet, skal du aktivere *Forbedringer af modtagelse af id* og *Forbedringer af arbejdspolitikken, for indgående arbejde* i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ec942-191">To make the functionality that is described in this scenario available in your system, you must turn on the *License plate receiving enhancements* and *Work policy enhancements for inbound work* features in [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

<span data-ttu-id="ec942-192">Dette scenarie bruger standarddemodata.</span><span class="sxs-lookup"><span data-stu-id="ec942-192">This scenario uses the standard demo data.</span></span> <span data-ttu-id="ec942-193">Hvis du vil gennemgå scenariet ved hjælp af de værdier, der vises her, skal du arbejde på et system, hvor demodata er installeret.</span><span class="sxs-lookup"><span data-stu-id="ec942-193">Therefore, if you want to work through it by using the values that are provided here, you must work on a system where demo data is installed.</span></span> <span data-ttu-id="ec942-194">Derudover skal du vælge den juridiske enhed **USMF**.</span><span class="sxs-lookup"><span data-stu-id="ec942-194">Additionally, you must select the **USMF** legal entity.</span></span>

### <a name="set-up-a-work-policy"></a><span data-ttu-id="ec942-195">Konfigurere en arbejdspolitik</span><span class="sxs-lookup"><span data-stu-id="ec942-195">Set up a work policy</span></span>

1. <span data-ttu-id="ec942-196">Gå til **Lokationsstyring \> Konfiguration \> Arbejde \> Arbejdspolitikker**.</span><span class="sxs-lookup"><span data-stu-id="ec942-196">Go to **Warehouse management \> Setup \> Work \> Work policies**.</span></span>
1. <span data-ttu-id="ec942-197">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="ec942-197">Select **New**.</span></span>
1. <span data-ttu-id="ec942-198">I feltet **Navn på arbejdspolitik** skal du angive *Intet læg på lager-arbejde for indkøbsvare*.</span><span class="sxs-lookup"><span data-stu-id="ec942-198">In the **Work policy name** field, enter *No purchase item putaway work*.</span></span>
1. <span data-ttu-id="ec942-199">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="ec942-199">Select **Save**.</span></span>
1. <span data-ttu-id="ec942-200">Vælg **Tilføj** i oversigtspanelet **Arbejdsordretyper** for at føje en række til gitteret, og angiv derefter følgende værdier for den nye række:</span><span class="sxs-lookup"><span data-stu-id="ec942-200">On the **Work order types** FastTab, select **Add** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="ec942-201">**Arbejdsordretype:** *Indkøbsordrer*</span><span class="sxs-lookup"><span data-stu-id="ec942-201">**Work order type:** *Purchase orders*</span></span>
    - <span data-ttu-id="ec942-202">**Arbejdsproces:** *Indkøbsordrevare til modtagelse (og læg på lager)*</span><span class="sxs-lookup"><span data-stu-id="ec942-202">**Work process:** *Purchase order item receiving (and putaway)*</span></span>
    - <span data-ttu-id="ec942-203">**Metode til oprettelse af arbejde:** *Aldrig*</span><span class="sxs-lookup"><span data-stu-id="ec942-203">**Work creation method:** *Never*</span></span>
    - <span data-ttu-id="ec942-204">**Navn på politik for cross-docking:** Lad feltet være tomt.</span><span class="sxs-lookup"><span data-stu-id="ec942-204">**Cross docking policy name:** Leave this field blank.</span></span>

1. <span data-ttu-id="ec942-205">Vælg **Tilføj** i oversigtspanelet **Lagerlokationer** for at føje en række til gitteret, og angiv derefter følgende værdier for den nye række:</span><span class="sxs-lookup"><span data-stu-id="ec942-205">On the **Inventory locations** FastTab, select **Add** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="ec942-206">**Lagersted:** *24*</span><span class="sxs-lookup"><span data-stu-id="ec942-206">**Warehouse:** *24*</span></span>
    - <span data-ttu-id="ec942-207">**Lokation:** *FL-001*</span><span class="sxs-lookup"><span data-stu-id="ec942-207">**Location:** *FL-001*</span></span>

1. <span data-ttu-id="ec942-208">I oversigtspanelet **Produkter** skal du angive feltet **Produktvalg** til *Alle*.</span><span class="sxs-lookup"><span data-stu-id="ec942-208">On the **Products** FastTab, set the **Product selection** field to *All*.</span></span>
1. <span data-ttu-id="ec942-209">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="ec942-209">Select **Save**.</span></span>

### <a name="set-up-a-mobile-device-menu-item-to-change-the-receiving-location"></a><span data-ttu-id="ec942-210">Konfigurere et menupunkt for mobilenheden til ændring af modtagelseslokationen</span><span class="sxs-lookup"><span data-stu-id="ec942-210">Set up a mobile device menu item to change the receiving location</span></span>

1. <span data-ttu-id="ec942-211">Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Menupunkter i mobilenhed**.</span><span class="sxs-lookup"><span data-stu-id="ec942-211">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="ec942-212">I venstre rude skal du vælge det eksisterende menupunkt **Købsmodtagelse**.</span><span class="sxs-lookup"><span data-stu-id="ec942-212">In the left pane, select the existing **Purchase receive** menu item.</span></span>
1. <span data-ttu-id="ec942-213">I oversigtspanelet **Generelt** skal du angive indstillingen **Brug standarddata** til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="ec942-213">On the **General** FastTab, set the **Use default data** option to *Yes*.</span></span>
1. <span data-ttu-id="ec942-214">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="ec942-214">Select **Save**.</span></span>
1. <span data-ttu-id="ec942-215">Vælg **Standarddata** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="ec942-215">On the Action Pane, select **Default data**.</span></span>
1. <span data-ttu-id="ec942-216">Vælg **Ny** i handlingsruden på siden **Standarddata** for at føje en række til gitteret, og angiv derefter følgende værdier for den nye række:</span><span class="sxs-lookup"><span data-stu-id="ec942-216">On the **Default data** page, on the Action Pane, select **New** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="ec942-217">**Standarddatafelt:** *Til lokation*</span><span class="sxs-lookup"><span data-stu-id="ec942-217">**Default data field:** *To location*</span></span>
    - <span data-ttu-id="ec942-218">**Lagersted:** *24*</span><span class="sxs-lookup"><span data-stu-id="ec942-218">**Warehouse:** *24*</span></span>
    - <span data-ttu-id="ec942-219">**Lokation:** Lad feltet være tomt.</span><span class="sxs-lookup"><span data-stu-id="ec942-219">**Location:** Leave this field blank.</span></span>
    - <span data-ttu-id="ec942-220">**Hardcodet værdi:** *FL-001*</span><span class="sxs-lookup"><span data-stu-id="ec942-220">**Hardcoded value:** *FL-001*</span></span>

1. <span data-ttu-id="ec942-221">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="ec942-221">Select **Save**.</span></span>

### <a name="receive-a-purchase-order-without-creating-work"></a><span data-ttu-id="ec942-222">Modtage en indkøbsordre uden at oprette arbejde</span><span class="sxs-lookup"><span data-stu-id="ec942-222">Receive a purchase order without creating work</span></span>

<span data-ttu-id="ec942-223">I eksemplet i dette afsnit vises, hvordan du modtager en indkøbsordrevare, men uden at oprette arbejde, på en lokation, der er forskellig fra standardlokationen for modtagelse på lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="ec942-223">The example in this section shows how to receive a purchase order item, but without creating work, at a location that differs from the default receiving location that is set up for the warehouse.</span></span> <span data-ttu-id="ec942-224">I dette eksempel bruges den arbejdspolitik og det mobilenhedselement, du har oprettet tidligere i dette scenario.</span><span class="sxs-lookup"><span data-stu-id="ec942-224">This example uses the work policy and mobile device item that you created earlier in this scenario.</span></span>

#### <a name="create-a-purchase-order"></a><span data-ttu-id="ec942-225">Oprette en indkøbsordre</span><span class="sxs-lookup"><span data-stu-id="ec942-225">Create a purchase order</span></span>

1. <span data-ttu-id="ec942-226">Gå til **Indkøb og forsyning \> Indkøbsordrer \> Alle indkøbsordrer**.</span><span class="sxs-lookup"><span data-stu-id="ec942-226">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="ec942-227">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="ec942-227">Select **New**.</span></span>
1. <span data-ttu-id="ec942-228">Angiv følgende værdier i dialogboksen **Opret indkøbsordre**:</span><span class="sxs-lookup"><span data-stu-id="ec942-228">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="ec942-229">**Kreditorkonto:** *US-101*</span><span class="sxs-lookup"><span data-stu-id="ec942-229">**Vendor account:** *US-101*</span></span>
    - <span data-ttu-id="ec942-230">**Lokation:** *2*</span><span class="sxs-lookup"><span data-stu-id="ec942-230">**Site:** *2*</span></span>
    - <span data-ttu-id="ec942-231">**Lagersted:** *24*</span><span class="sxs-lookup"><span data-stu-id="ec942-231">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="ec942-232">Vælg **OK** for at åbne den nye indkøbsordre og lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="ec942-232">Select **OK** to close the dialog box and open the new purchase order.</span></span>
1. <span data-ttu-id="ec942-233">I oversigtspanelet **Indkøbsordrelinjer** skal du angive følgende værdier for den tomme række:</span><span class="sxs-lookup"><span data-stu-id="ec942-233">On the **Purchase order lines** FastTab, set the following values for the empty row:</span></span>

    - <span data-ttu-id="ec942-234">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="ec942-234">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="ec942-235">**Antal:** *1*</span><span class="sxs-lookup"><span data-stu-id="ec942-235">**Quantity:** *1*</span></span>

1. <span data-ttu-id="ec942-236">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="ec942-236">Select **Save**.</span></span>
1. <span data-ttu-id="ec942-237">Notér dig købsordrenummeret.</span><span class="sxs-lookup"><span data-stu-id="ec942-237">Make a note of the purchase order number.</span></span>

#### <a name="receive-a-purchase-order"></a><span data-ttu-id="ec942-238">Modtage en indkøbsordre</span><span class="sxs-lookup"><span data-stu-id="ec942-238">Receive a purchase order</span></span>

1. <span data-ttu-id="ec942-239">På mobilenheden skal du logge på lagersted *24* ved hjælp *24* som bruger-id og *1* som adgangskode.</span><span class="sxs-lookup"><span data-stu-id="ec942-239">On the mobile device, sign in to warehouse *24* by using *24* as the user ID and *1* as the password.</span></span>
1. <span data-ttu-id="ec942-240">Vælg **Indgående**.</span><span class="sxs-lookup"><span data-stu-id="ec942-240">Select **Inbound**.</span></span>
1. <span data-ttu-id="ec942-241">Vælg **Købsmodtagelse**.</span><span class="sxs-lookup"><span data-stu-id="ec942-241">Select **Purchase receive**.</span></span> <span data-ttu-id="ec942-242">Feltet **Lokation** skal indstilles til *FL-001*.</span><span class="sxs-lookup"><span data-stu-id="ec942-242">The **Location** field should be set to *FL-001*.</span></span>
1. <span data-ttu-id="ec942-243">Angiv indkøbsordrenummeret for den indkøbsordre, du oprettede i den foregående procedure.</span><span class="sxs-lookup"><span data-stu-id="ec942-243">Enter the purchase order number for the purchase order that you created in the previous procedure.</span></span>
1. <span data-ttu-id="ec942-244">Indtast **A0001** i feltet *Varenummer*.</span><span class="sxs-lookup"><span data-stu-id="ec942-244">In the **Item number** field, enter *A0001*.</span></span>
1. <span data-ttu-id="ec942-245">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="ec942-245">Select **OK**.</span></span>
1. <span data-ttu-id="ec942-246">Angiv **1** i feltet *Antal*.</span><span class="sxs-lookup"><span data-stu-id="ec942-246">In the **Quantity** field, enter *1*.</span></span>
1. <span data-ttu-id="ec942-247">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="ec942-247">Select **OK**.</span></span>

<span data-ttu-id="ec942-248">Indkøbsordren er nu modtaget, men der er ikke knyttet noget arbejde til den.</span><span class="sxs-lookup"><span data-stu-id="ec942-248">The purchase order is now received, but no work is associated with it.</span></span> <span data-ttu-id="ec942-249">Den disponible lagerbeholdning er opdateret, og et antal på *1* af vare *A0001* er nu tilgængeligt på lokationen *FL-001*.</span><span class="sxs-lookup"><span data-stu-id="ec942-249">The on-hand inventory has been updated, and a quantity of *1* of item *A0001* is now available at location *FL-001*.</span></span>

## <a name="example-scenario-manufacturing"></a><span data-ttu-id="ec942-250">Eksempelscenario: produktion</span><span class="sxs-lookup"><span data-stu-id="ec942-250">Example scenario: Manufacturing</span></span>

<span data-ttu-id="ec942-251">I følgende eksempel er der to produktionsordrer, *PRD-001* og *PRD-002*.</span><span class="sxs-lookup"><span data-stu-id="ec942-251">In the following example, there are two production orders, *PRD-001* and *PRD-002*.</span></span> <span data-ttu-id="ec942-252">Produktionsordre *PRD-001* er en handling, der hedder *Samling*, hvor produktet *SC1* færdigmeldes på lokation *001*.</span><span class="sxs-lookup"><span data-stu-id="ec942-252">Production order *PRD-001* has an operation that is named *Assembly*, where product *SC1* is being reported as finished to location *001*.</span></span> <span data-ttu-id="ec942-253">Produktionsordre *PRD-002* er en handling, der hedder *Maling* og forbruger produkt *SC1* fra lokation *001*.</span><span class="sxs-lookup"><span data-stu-id="ec942-253">Production order *PRD-002* has an operation that is named *Painting* and consumes product *SC1* from location *001*.</span></span> <span data-ttu-id="ec942-254">Produktionsordren *PRD-002* forbruger også råvare *RM1* fra lokation *001*.</span><span class="sxs-lookup"><span data-stu-id="ec942-254">Production order *PRD-002* also consumes raw material *RM1* from location *001*.</span></span> <span data-ttu-id="ec942-255">Råvare *RM1* opbevares på lagerlokation *BULK-001* og vil blive plukket til lokation *001* af lagerstedets arbejde til råvareplukning.</span><span class="sxs-lookup"><span data-stu-id="ec942-255">Raw material *RM1* is stored in warehouse location *BULK-001* and will be picked to location *001* by warehouse work for raw material picking.</span></span> <span data-ttu-id="ec942-256">Plukkearbejdet genereres, når produktionen *PRD-002* frigives.</span><span class="sxs-lookup"><span data-stu-id="ec942-256">The picking work is generated when production *PRD-002* is released.</span></span>

<span data-ttu-id="ec942-257">[![Politikker for lagerstedsarbejde](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span><span class="sxs-lookup"><span data-stu-id="ec942-257">[![Warehouse work policies](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span></span>

<span data-ttu-id="ec942-258">Når du skal konfigurere lagerstedets arbejdspolitik for dette scenario, skal du overveje følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="ec942-258">When you're planning to configure a warehouse work policy for this scenario, you should consider the following points:</span></span>

- <span data-ttu-id="ec942-259">Lagerstedets arbejde for færdigvarer, der skal lægges på lager, er ikke påkrævet, når du færdigmelder produkt *SC1* fra produktionsordre *PRD-001* til lokation *001*.</span><span class="sxs-lookup"><span data-stu-id="ec942-259">Warehouse work for putaway of finished goods isn't required when you report product *SC1* as finished from production order *PRD-001* to location *001*.</span></span> <span data-ttu-id="ec942-260">Dette skyldes, at *Maling*-handlingen for produktionsordre *PRD-002* forbruger produkt *SC1* på samme lokation.</span><span class="sxs-lookup"><span data-stu-id="ec942-260">The reason is that the *Painting* operation for production order *PRD-002* consumes product *SC1* at the same location.</span></span>
- <span data-ttu-id="ec942-261">Lagerstedsarbejde til plukning af råvarer kræves for at flytte råvare *RM1* fra lagerlokation *BULK-001* til lokation *001*.</span><span class="sxs-lookup"><span data-stu-id="ec942-261">Warehouse work for raw material picking is required to move raw material *RM1* from warehouse location *BULK-001* to location *001*.</span></span>

<span data-ttu-id="ec942-262">Her er et eksempel på en politik for arbejde, du har angivet, ud fra disse overvejelser:</span><span class="sxs-lookup"><span data-stu-id="ec942-262">Here is an example of a work policy that you can set up, based on these considerations:</span></span>

- <span data-ttu-id="ec942-263">**Navn på arbejdspolitik:** *Intet læg på lager-arbejde*</span><span class="sxs-lookup"><span data-stu-id="ec942-263">**Work policy name:** *No putaway work*</span></span>
- <span data-ttu-id="ec942-264">**Arbejdsordretyper:** *Færdige varer, læg på lager*, og *Samprodukt og biprodukt, læg på lager*</span><span class="sxs-lookup"><span data-stu-id="ec942-264">**Work order types:** *Finished goods put away* and *Co-product and by-product put away*</span></span>
- <span data-ttu-id="ec942-265">**Lagerlokationer:** Lagersted *51* og lokation *001*</span><span class="sxs-lookup"><span data-stu-id="ec942-265">**Inventory locations:** Warehouse *51* and location *001*</span></span>
- <span data-ttu-id="ec942-266">**Produkter:** *SC1*</span><span class="sxs-lookup"><span data-stu-id="ec942-266">**Products:** *SC1*</span></span>

<span data-ttu-id="ec942-267">Følgende eksempelscenario indeholder trinvise instruktioner i, hvordan du konfigurerer arbejdspolitikken for lagersted i dette scenario.</span><span class="sxs-lookup"><span data-stu-id="ec942-267">The following example scenario provides step-by-step instructions for setting up the warehouse work policy for this scenario.</span></span>

## <a name="example-scenario-report-as-finished-to-a-location-that-isnt-license-platecontrolled"></a><span data-ttu-id="ec942-268">Eksempelscenario: Færdigmelde til en lokation, der ikke er id-kontrolleret</span><span class="sxs-lookup"><span data-stu-id="ec942-268">Example scenario: Report as finished to a location that isn't license plate–controlled</span></span>

<span data-ttu-id="ec942-269">Dette scenarie viser et eksempel på, hvor en produktionsordre færdigmeldes til en lokation, der ikke er id-kontrolleret.</span><span class="sxs-lookup"><span data-stu-id="ec942-269">This scenario shows an example where a production order is reported as finished to a location that isn't license plate–controlled.</span></span>

<span data-ttu-id="ec942-270">Dette scenarie bruger standarddemodata.</span><span class="sxs-lookup"><span data-stu-id="ec942-270">This scenario uses the standard demo data.</span></span> <span data-ttu-id="ec942-271">Hvis du vil gennemgå scenariet ved hjælp af de værdier, der vises her, skal du arbejde på et system, hvor demodata er installeret.</span><span class="sxs-lookup"><span data-stu-id="ec942-271">Therefore, if you want to work through it by using the values that are provided here, you must work on a system where demo data is installed.</span></span> <span data-ttu-id="ec942-272">Derudover skal du vælge den juridiske enhed **USMF**.</span><span class="sxs-lookup"><span data-stu-id="ec942-272">Additionally, you must select the **USMF** legal entity.</span></span>

### <a name="set-up-a-warehouse-work-policy"></a><span data-ttu-id="ec942-273">Konfigurere en arbejdspolitik for lagersted</span><span class="sxs-lookup"><span data-stu-id="ec942-273">Set up a warehouse work policy</span></span>

<span data-ttu-id="ec942-274">Lagerstedsprocesser omfatter ikke altid lagerstedsarbejde.</span><span class="sxs-lookup"><span data-stu-id="ec942-274">Warehouse processes don't always include warehouse work.</span></span> <span data-ttu-id="ec942-275">Ved at definere en arbejdspolitik kan du forhindre oprettelse af arbejde med pluk af råmaterialer og læg færdigvarer på lager for en række produkter på bestemte lokationer.</span><span class="sxs-lookup"><span data-stu-id="ec942-275">By defining a work policy, you can prevent the creation of work for raw material picking and putaway of finished goods for a set of products at specific locations.</span></span>

1. <span data-ttu-id="ec942-276">Gå til **Lokationsstyring \> Konfiguration \> Arbejde \> Arbejdspolitikker**.</span><span class="sxs-lookup"><span data-stu-id="ec942-276">Go to **Warehouse management \> Setup \> Work \> Work policies**.</span></span>
1. <span data-ttu-id="ec942-277">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="ec942-277">Select **New**.</span></span>
1. <span data-ttu-id="ec942-278">I feltet **Navn på arbejdspolitik** skal du angive *Intet læg på lager-arbejde*.</span><span class="sxs-lookup"><span data-stu-id="ec942-278">In the **Work policy name** field, enter *No putaway work*.</span></span>
1. <span data-ttu-id="ec942-279">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="ec942-279">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="ec942-280">Vælg **Tilføj** i oversigtspanelet **Arbejdsordretyper** for at føje en række til gitteret, og angiv derefter følgende værdier for den nye række:</span><span class="sxs-lookup"><span data-stu-id="ec942-280">On the **Work order types** FastTab, select **Add** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="ec942-281">**Arbejdsordretype:** *Færdige varer, læg på lager*</span><span class="sxs-lookup"><span data-stu-id="ec942-281">**Work order type:** *Finished goods put away*</span></span>
    - <span data-ttu-id="ec942-282">**Arbejdsproces:** *Alle relaterede arbejdsprocesser*</span><span class="sxs-lookup"><span data-stu-id="ec942-282">**Work process:** *All related work processes*</span></span>
    - <span data-ttu-id="ec942-283">**Metode til oprettelse af arbejde:** *Aldrig*</span><span class="sxs-lookup"><span data-stu-id="ec942-283">**Work creation method:** *Never*</span></span>
    - <span data-ttu-id="ec942-284">**Navn på politik for cross-docking:** Lad feltet være tomt.</span><span class="sxs-lookup"><span data-stu-id="ec942-284">**Cross docking policy name:** Leave this field blank.</span></span>

1. <span data-ttu-id="ec942-285">Vælg **Tilføj** for at tilføje endnu en række i gitteret, og angiv derefter følgende værdier for den nye række:</span><span class="sxs-lookup"><span data-stu-id="ec942-285">Select **Add** again to add a second row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="ec942-286">**Arbejdsordretype:** *Samprodukt og biprodukt, læg på lager*</span><span class="sxs-lookup"><span data-stu-id="ec942-286">**Work order type:** *Co-product and by-product put away*</span></span>
    - <span data-ttu-id="ec942-287">**Arbejdsproces:** *Alle relaterede arbejdsprocesser*</span><span class="sxs-lookup"><span data-stu-id="ec942-287">**Work process:** *All related work processes*</span></span>
    - <span data-ttu-id="ec942-288">**Metode til oprettelse af arbejde:** *Aldrig*</span><span class="sxs-lookup"><span data-stu-id="ec942-288">**Work creation method:** *Never*</span></span>
    - <span data-ttu-id="ec942-289">**Navn på politik for cross-docking:** Lad feltet være tomt.</span><span class="sxs-lookup"><span data-stu-id="ec942-289">**Cross docking policy name:** Leave this field blank.</span></span>

1. <span data-ttu-id="ec942-290">Vælg **Tilføj** i oversigtspanelet **Lagerlokationer** for at føje en række til gitteret, og angiv derefter følgende værdier for den nye række:</span><span class="sxs-lookup"><span data-stu-id="ec942-290">On the **Inventory locations** FastTab, select **Add** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="ec942-291">**Lagersted:** *51*</span><span class="sxs-lookup"><span data-stu-id="ec942-291">**Warehouse:** *51*</span></span>
    - <span data-ttu-id="ec942-292">**Lokation:** *001*</span><span class="sxs-lookup"><span data-stu-id="ec942-292">**Location:** *001*</span></span>

1. <span data-ttu-id="ec942-293">I oversigtspanelet **Produkter** skal du angive feltet **Produktvalg** til *Valgte*.</span><span class="sxs-lookup"><span data-stu-id="ec942-293">On the **Products** FastTab, set the **Product selection** field to *Selected*.</span></span>
1. <span data-ttu-id="ec942-294">I oversigtspanelet **Produkter** skal du vælge **Tilføj** for at føje en række til gitteret.</span><span class="sxs-lookup"><span data-stu-id="ec942-294">On the **Products** FastTab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="ec942-295">Angiv feltet **Varenummer** til *L0101* i den nye række.</span><span class="sxs-lookup"><span data-stu-id="ec942-295">In the new row, set the **Item number** field to *L0101*.</span></span>
1. <span data-ttu-id="ec942-296">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="ec942-296">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-an-output-location"></a><span data-ttu-id="ec942-297">Konfigurere en outputlokation</span><span class="sxs-lookup"><span data-stu-id="ec942-297">Set up an output location</span></span>

1. <span data-ttu-id="ec942-298">Gå til **Virksomhedsadministration \> Ressourcer \> Ressourcegrupper**.</span><span class="sxs-lookup"><span data-stu-id="ec942-298">Go to **Organization administration \> Resources \> Resource groups**.</span></span>
1. <span data-ttu-id="ec942-299">Vælg ressourcegruppen **5102** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="ec942-299">In the left pane, select resource group **5102**.</span></span>
1. <span data-ttu-id="ec942-300">I oversigtspanelet **Generelt** kan du angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="ec942-300">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="ec942-301">**Lagersted for udlagring:** *51*</span><span class="sxs-lookup"><span data-stu-id="ec942-301">**Output warehouse:** *51*</span></span>
    - <span data-ttu-id="ec942-302">**Udlagringslokation:** *001*</span><span class="sxs-lookup"><span data-stu-id="ec942-302">**Output location:** *001*</span></span>

1. <span data-ttu-id="ec942-303">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="ec942-303">On the Action Pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="ec942-304">Lokationen *001* er ikke en id-kontrolleret lokation.</span><span class="sxs-lookup"><span data-stu-id="ec942-304">Location *001* isn't a license plate–controlled location.</span></span> <span data-ttu-id="ec942-305">Du kan kun konfigurere en udlagringslokation uden id-kontrol, hvis der findes en gyldig arbejdspolitik for lokationen.</span><span class="sxs-lookup"><span data-stu-id="ec942-305">You can set up an output location that isn't license plate–controlled only if an applicable work policy exists for the location.</span></span>

### <a name="create-a-production-order-and-report-it-as-finished"></a><span data-ttu-id="ec942-306">Oprette en produktionsordre og rapportere den som færdig</span><span class="sxs-lookup"><span data-stu-id="ec942-306">Create a production order and report it as finished</span></span>

1. <span data-ttu-id="ec942-307">Gå til **Produktionsstyring \> Produktionsordrer \> Alle produktionsordrer**.</span><span class="sxs-lookup"><span data-stu-id="ec942-307">Go to **Production control \> Production orders \> All production orders**.</span></span>
1. <span data-ttu-id="ec942-308">Vælg **Ny produktionsordre** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="ec942-308">On the Action Pane, select **New production order**.</span></span>
1. <span data-ttu-id="ec942-309">Angiv feltet **Varenummer** til **L0101** i dialogboksen *Opret produktionsordre*.</span><span class="sxs-lookup"><span data-stu-id="ec942-309">In the **Create production order** dialog box, set the **Item number** field to *L0101*.</span></span>
1. <span data-ttu-id="ec942-310">Vælg **Opret** for at oprette ordren og lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="ec942-310">Select **Create** to create the order and close the dialog box.</span></span>

    <span data-ttu-id="ec942-311">En ny produktionsordre føjes til gitteret på siden **Alle produktionsordrer**.</span><span class="sxs-lookup"><span data-stu-id="ec942-311">A new production order is added to the grid on the **All production orders** page.</span></span>

    <span data-ttu-id="ec942-312">Lad den nye produktionsordre forblive valgt.</span><span class="sxs-lookup"><span data-stu-id="ec942-312">Keep the new production order selected.</span></span>

1. <span data-ttu-id="ec942-313">I handlingsruden under fanen **Produktionsordre** skal du i gruppen **Proces** vælge **Estimer**.</span><span class="sxs-lookup"><span data-stu-id="ec942-313">On the Action Pane, on the **Production order** tab, in the **Process** group, select **Estimate**.</span></span>
1. <span data-ttu-id="ec942-314">Læs estimatet i dialogboksen **Estimat**, og vælg derefter **OK** for at lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="ec942-314">In the **Estimate** dialog box, read the estimate, and then select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="ec942-315">I handlingsruden under fanen **Produktionsordre** skal du i gruppen **Proces** vælge **Start**.</span><span class="sxs-lookup"><span data-stu-id="ec942-315">On the Action Pane, on the **Production order** tab, in the **Process** group, select **Start**.</span></span>
1. <span data-ttu-id="ec942-316">I dialogboksen **Start** skal du under fanen **Generelt** angive feltet **Automatisk styklisteforbrug** til *Aldrig*.</span><span class="sxs-lookup"><span data-stu-id="ec942-316">In the **Start** dialog box, on the **General** tab, set the **Automatic BOM consumption** field to *Never*.</span></span>
1. <span data-ttu-id="ec942-317">Vælg **OK** for at gemme indstillingen og lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="ec942-317">Select **OK** to save your setting and close the dialog box.</span></span>
1. <span data-ttu-id="ec942-318">I handlingsruden under fanen **Produktionsordre** skal du i gruppen **Proces** vælge **Færdigmeld**.</span><span class="sxs-lookup"><span data-stu-id="ec942-318">On the Action Pane, on the **Production order** tab, in the **Process** group, select **Report as finished**.</span></span>
1. <span data-ttu-id="ec942-319">I dialogboksen **Færdigmeld** under fanen **Generelt** skal du angive indstillingen **Accepter fejl** til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="ec942-319">In the **Report as finished** dialog box, on the **General** tab, set the **Accept error** option to *Yes*.</span></span>
1. <span data-ttu-id="ec942-320">Vælg **OK** for at gemme indstillingen og lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="ec942-320">Select **OK** to save your setting and close the dialog box.</span></span>
1. <span data-ttu-id="ec942-321">Vælg **Arbejdsdetaljer** i gruppen **Generelt** under fanen **Lagersted** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="ec942-321">On the Action Pane, on the **Warehouse** tab, in the **General** group, select **Work details**.</span></span>

<span data-ttu-id="ec942-322">Når produktionsordren er færdigmeldt, oprettes der intet arbejde for læg på lager.</span><span class="sxs-lookup"><span data-stu-id="ec942-322">When the production order is reported as finished, no work is generated for putaway.</span></span> <span data-ttu-id="ec942-323">Dette skyldes, at der er defineret en arbejdspolitik, som forhindrer, at der genereres arbejde, når produktet *L0101* færdigmeldes på lokation *001*.</span><span class="sxs-lookup"><span data-stu-id="ec942-323">This behavior occurs because a work policy is defined that prevents work from being generated when product *L0101* is reported as finished to location *001*.</span></span>

## <a name="more-information"></a><span data-ttu-id="ec942-324">Flere oplysninger</span><span class="sxs-lookup"><span data-stu-id="ec942-324">More information</span></span>

<span data-ttu-id="ec942-325">Du kan få flere oplysninger om menupunkter på mobilenheder, i [Konfigurere mobilenheder til lagerstedsarbejde](configure-mobile-devices-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="ec942-325">For more information about mobile device menu items, see [Set up mobile devices for warehouse work](configure-mobile-devices-warehouse.md).</span></span>

<span data-ttu-id="ec942-326">Du kan finde flere oplysninger om id-modtagelse og arbejdspolitikker under [Modtagelse af id via lagerstedsappen](warehousing-mobile-device-app-license-plate-receiving.md).</span><span class="sxs-lookup"><span data-stu-id="ec942-326">For more information about license plate receiving and work policies, see [License plate receiving via the warehouse app](warehousing-mobile-device-app-license-plate-receiving.md).</span></span>

<span data-ttu-id="ec942-327">Du finder flere oplysninger om indgående laststyring i [Lagerstedshåndtering af indgående laster til indkøbsordrer](inbound-load-handling.md).</span><span class="sxs-lookup"><span data-stu-id="ec942-327">For more information about inbound load management, see [Warehouse handling of inbound loads for purchase orders](inbound-load-handling.md).</span></span>
