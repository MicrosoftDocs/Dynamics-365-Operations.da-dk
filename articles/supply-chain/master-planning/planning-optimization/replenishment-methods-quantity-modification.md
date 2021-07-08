---
title: Genopfyldningsmetoder og ændring af antal
description: Dette emne indeholder oplysninger om genopfyldningmetoder i Planlægningsoptimering. Det forklares også, hvordan antallet på flere ordrer på et produkt påvirker resultatet.
author: crytt
ms.date: 6/1/2021
ms.topic: article
ms.search.form: ReqGroup, ReqItemTable, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d5e0e671e624de2646a47647ef08d3567599b884
ms.sourcegitcommit: 4cbd83e21a78459e4711a2dedba0f5a7acc3c841
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/15/2021
ms.locfileid: "6261690"
---
# <a name="replenishment-methods-and-quantity-modification"></a><span data-ttu-id="08de5-104">Genopfyldningsmetoder og ændring af antal</span><span class="sxs-lookup"><span data-stu-id="08de5-104">Replenishment methods and quantity modification</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="08de5-105">Dette emne indeholder oplysninger om genopfyldningmetoder i Planlægningsoptimering.</span><span class="sxs-lookup"><span data-stu-id="08de5-105">This topic provides information about replenishment methods in Planning Optimization.</span></span> <span data-ttu-id="08de5-106">Det forklares også, hvordan antallet på flere ordrer på et produkt påvirker resultatet.</span><span class="sxs-lookup"><span data-stu-id="08de5-106">It also explains how the multiple order quantity for a product affects the result.</span></span>

<span data-ttu-id="08de5-107">Genopfyldningsmetoder kaldes også disponeringsmetoder og metoder til angivelse af partistørrelse.</span><span class="sxs-lookup"><span data-stu-id="08de5-107">Replenishment methods are also known as coverage methods and lot-sizing methods.</span></span>

## <a name="coverage-codes"></a><span data-ttu-id="08de5-108">Disponeringskoder</span><span class="sxs-lookup"><span data-stu-id="08de5-108">Coverage codes</span></span>

<span data-ttu-id="08de5-109">Planlægningsoptimering kan konfigureres til at bruge forskellige genopfyldningsmetoder.</span><span class="sxs-lookup"><span data-stu-id="08de5-109">Planning Optimization can be configured to use different replenishment methods.</span></span> <span data-ttu-id="08de5-110">Genopfyldningsmetoderne er de teknikker, som systemet bruger til at beregne behov for et produkt.</span><span class="sxs-lookup"><span data-stu-id="08de5-110">The replenishment methods are the techniques that the system uses to calculate requirements for a product.</span></span> <span data-ttu-id="08de5-111">Genopfyldningsmetoder defineres ud fra disponeringskoder, du kan angive for enten disponeringsgruppen eller produktet.</span><span class="sxs-lookup"><span data-stu-id="08de5-111">Replenishment methods are defined by coverage codes that you can set up on either the coverage group or the product.</span></span>

<span data-ttu-id="08de5-112">Følgende disponeringskoder kan bruges i Planlægningsoptimering:</span><span class="sxs-lookup"><span data-stu-id="08de5-112">The following coverage codes can be used in Planning Optimization:</span></span>

- <span data-ttu-id="08de5-113">**Periode** – Genopfyldningsmetoden kombinerer alle behov for en periode til én ordre for produktet.</span><span class="sxs-lookup"><span data-stu-id="08de5-113">**Period** – The replenishment method combines all the demand for a period into one order for the product.</span></span> <span data-ttu-id="08de5-114">Ordren planlægges for den første dag i perioden, og dens antal vil opfylde nettobehovet i den oprettede periode.</span><span class="sxs-lookup"><span data-stu-id="08de5-114">The order will be planned for the first day of the period, and its quantity will fulfill the net requirements during the established period.</span></span> <span data-ttu-id="08de5-115">Perioden starter med det første behov for produktet og dækker den definerede varighed i tiden.</span><span class="sxs-lookup"><span data-stu-id="08de5-115">The period starts with the first demand of the product and covers the defined length of time.</span></span> <span data-ttu-id="08de5-116">Den næste periode vil starte med de næste behov for produktet.</span><span class="sxs-lookup"><span data-stu-id="08de5-116">The next period will start with the next requirements of the product.</span></span> <span data-ttu-id="08de5-117">Disponeringskoden for *periode* bruges ofte til ikke-forudsigelige lagertræk, sæsonafhængige produkter eller produkter med høje omkostninger.</span><span class="sxs-lookup"><span data-stu-id="08de5-117">The *Period* coverage code is often used for non-predictable inventory draw, season-influenced products, or high-cost products.</span></span> <span data-ttu-id="08de5-118">Følgende illustration viser et eksempel.</span><span class="sxs-lookup"><span data-stu-id="08de5-118">The following illustration shows an example.</span></span>

    <span data-ttu-id="08de5-119">![Eksempel på brug af periodedisponeringskode](./media/coverage-code-period.png "Eksempel på brug af periodedisponeringskode")</span><span class="sxs-lookup"><span data-stu-id="08de5-119">![Example of Period coverage code use](./media/coverage-code-period.png "Example of Period coverage code use")</span></span>

- <span data-ttu-id="08de5-120">**Behov** – I genopfyldningsmetoden til opretter systemet en planlagt indkøbs-, overførsels- eller produktionsordre pr. behov for produktet.</span><span class="sxs-lookup"><span data-stu-id="08de5-120">**Requirement** – In the replenishment method, the system creates a planned purchase, transfer, or production order per requirement for the product.</span></span> <span data-ttu-id="08de5-121">Denne metode bruges til dyre produkter, hvor efterspørgslen er periodisk.</span><span class="sxs-lookup"><span data-stu-id="08de5-121">This method is used for expensive products that have intermittent demand.</span></span> <span data-ttu-id="08de5-122">Disponeringskoden for *behov* bruges ofte til konfigurerbare produkter eller scenarier for fremstilling efter ordre.</span><span class="sxs-lookup"><span data-stu-id="08de5-122">The *Requirement* coverage code is often used for configurable products or make-to-order scenarios.</span></span> <span data-ttu-id="08de5-123">Følgende illustration viser et eksempel.</span><span class="sxs-lookup"><span data-stu-id="08de5-123">The following illustration shows an example.</span></span>

    <span data-ttu-id="08de5-124">![Eksempel på brug af behovsdisponeringskode](./media/coverage-code-requirement.png "Eksempel på brug af behovsdisponeringskode")</span><span class="sxs-lookup"><span data-stu-id="08de5-124">![Example of Requirement coverage code use](./media/coverage-code-requirement.png "Example of Requirement coverage code use")</span></span>

- <span data-ttu-id="08de5-125">**Min./Maks.**</span><span class="sxs-lookup"><span data-stu-id="08de5-125">**Min./Max.**</span></span> <span data-ttu-id="08de5-126">– Genopfyldningsmetoden er baseret på lagerniveauet.</span><span class="sxs-lookup"><span data-stu-id="08de5-126">– The replenishment method is based on the inventory level.</span></span> <span data-ttu-id="08de5-127">Den definerer genopfyldning af lageret op til et bestemt niveau, når den forventede beholdning er under en bestemt grænseværdi.</span><span class="sxs-lookup"><span data-stu-id="08de5-127">It defines the replenishment of inventory up to a specific level when the predicted on-hand level is below a specific threshold.</span></span> <span data-ttu-id="08de5-128">Genopfyldningsantallet vil være forskellen mellem maksimumniveauet og det forventede disponible lagerniveau.</span><span class="sxs-lookup"><span data-stu-id="08de5-128">The replenishment quantity will be the difference between the maximum level and the predicted on-hand level.</span></span> <span data-ttu-id="08de5-129">Disponeringskoden for *Min./Maks.*</span><span class="sxs-lookup"><span data-stu-id="08de5-129">The *Min./Max.*</span></span> <span data-ttu-id="08de5-130">bruges ofte til forudsigelige lagertræk, mest solgte produkter eller billigste produkter.</span><span class="sxs-lookup"><span data-stu-id="08de5-130">coverage code is often used for predictable inventory draw, high runners, or less expensive products.</span></span> <span data-ttu-id="08de5-131">Følgende illustration viser et eksempel.</span><span class="sxs-lookup"><span data-stu-id="08de5-131">The following illustration shows an example.</span></span>

    <span data-ttu-id="08de5-132">![Eksempel på brug af disponeringskode for Min./Maks.](./media/coverage-code-min-max.png "Eksempel på brug af disponeringskode for Min./Maks.")</span><span class="sxs-lookup"><span data-stu-id="08de5-132">![Example of Min./Max. coverage code use](./media/coverage-code-min-max.png "Example of Min./Max. coverage code use")</span></span>

- <span data-ttu-id="08de5-133">**Manuel** – I genopfyldningsmetoden foreslår systemet ikke køb, overflytning eller produktionsordrer for produktet.</span><span class="sxs-lookup"><span data-stu-id="08de5-133">**Manual** – In the replenishment method, the system doesn't suggest purchase, transfer, or production orders for the product.</span></span> <span data-ttu-id="08de5-134">I stedet er planlægningsmedarbejderen for produktet ansvarlig for oprettelse af de nødvendige ordrer til genopfyldning af produktet.</span><span class="sxs-lookup"><span data-stu-id="08de5-134">Instead, the planner for the product is responsible for creating the required orders for the replenishment of the product.</span></span> <span data-ttu-id="08de5-135">Den *manuelle* disponeringskode bruges ofte til produkter, der ikke ønskes systemgenererede ordreforslag for.</span><span class="sxs-lookup"><span data-stu-id="08de5-135">The *Manual* coverage code is often used for products that system-generated planned orders aren't wanted for.</span></span>

## <a name="impact-of-the-order-quantity-from-default-order-settings"></a><span data-ttu-id="08de5-136">Effekten af ordreantallet fra standardordreindstillinger</span><span class="sxs-lookup"><span data-stu-id="08de5-136">Impact of the order quantity from default order settings</span></span>

<span data-ttu-id="08de5-137">På siden **Standardordreindstilling** for et frigivet produkt kan du angive hver af følgende indstillinger for antal i oversigtspanelerne **Indkøbsordre**, **Lager** og **Salgsordre**.</span><span class="sxs-lookup"><span data-stu-id="08de5-137">On the **Default order setting** page for a released product, you can specify each of following quantity settings on the **Purchase order**, **Inventory**, and **Sales order** FastTabs.</span></span> <span data-ttu-id="08de5-138">(Oversigtspanelet **Lager** bruges til både flytteordrer og produktionsordrer).</span><span class="sxs-lookup"><span data-stu-id="08de5-138">(The **Inventory** FastTab is used for both transfer orders and production orders.)</span></span>

- <span data-ttu-id="08de5-139">**Flere** – Ordreforslag er et multiplum af dette antal.</span><span class="sxs-lookup"><span data-stu-id="08de5-139">**Multiple** – Planned orders will be a multiple of this quantity.</span></span>

    <span data-ttu-id="08de5-140">Hvis feltet **Flere** for eksempel er angivet til *5*, kan en ordre være for et antal på 5, 10, 15, 20 osv.</span><span class="sxs-lookup"><span data-stu-id="08de5-140">For example, if the **Multiple** field is set to *5*, an order can be for a quantity of 5, 10, 15, 20, and so on.</span></span>

- <span data-ttu-id="08de5-141">**Min. ordreantal** – Ordreforslag bliver ikke mindre end den angivne værdi.</span><span class="sxs-lookup"><span data-stu-id="08de5-141">**Min. order quantity** – Planned orders won't be less than the specified value.</span></span>

    <span data-ttu-id="08de5-142">Hvis feltet **Min. ordreantal** for eksempel er angivet til *10*, oprettes der et ordreforslag på 10, også selvom der kun kræves fire for at opfylde behovet.</span><span class="sxs-lookup"><span data-stu-id="08de5-142">For example, if the **Min. order quantity** field is set to *10*, a planned order for a quantity of 10 will be created, even if only four are required to fulfill the demand.</span></span>

- <span data-ttu-id="08de5-143">**Maks. ordreantal** – Ordreforslag bliver ikke større end den angivne værdi.</span><span class="sxs-lookup"><span data-stu-id="08de5-143">**Max. order quantity** – Planned orders won't exceed the specified value.</span></span> <span data-ttu-id="08de5-144">Hvis efterspørgslen er større end værdien **Maks. ordreantal**, oprettes der flere ordreforslag til at dække dette.</span><span class="sxs-lookup"><span data-stu-id="08de5-144">If the demand is more than the **Max. order quantity** value, multiple planned orders will be created to cover it.</span></span>

    <span data-ttu-id="08de5-145">Hvis feltet **Maks. ordreantal** for eksempel angivet til *100*, og behovet er 450, oprettes der fire ordreforslag for et antal på 100, og der oprettes et ordreforslag på 50.</span><span class="sxs-lookup"><span data-stu-id="08de5-145">For example, if the **Max. order quantity** field is set to *100*, and the demand is 450, four planned orders for a quantity of 100 and one planned order for a quantity of 50 will be created.</span></span>

## <a name="examples-of-replenishment-that-use-the-minmax-coverage-code"></a><span data-ttu-id="08de5-146">Eksempler på genopfyldning, hvor disponeringskoden Min./Maks.</span><span class="sxs-lookup"><span data-stu-id="08de5-146">Examples of replenishment that use the Min./Max.</span></span> <span data-ttu-id="08de5-147">bruges</span><span class="sxs-lookup"><span data-stu-id="08de5-147">coverage code</span></span>

<span data-ttu-id="08de5-148">Hvis du ikke angiver en værdi i feltet **Flere** for et produkt på siden **Standardordreindstilling**, og hvis du bruger genopfyldningsmetoden *Min./Maks.*,</span><span class="sxs-lookup"><span data-stu-id="08de5-148">If you don't specify a value in the **Multiple** field for a product on the **Default order setting** page, and if you're using the *Min./Max.*</span></span> <span data-ttu-id="08de5-149">foretager Planlægningsoptimering genopfyldning af lageret op til et bestemt niveau, når den forventede beholdning er under en bestemt grænseværdi.</span><span class="sxs-lookup"><span data-stu-id="08de5-149">replenishment method, Planning Optimization will replenish the inventory up to a specific level when the predicted on-hand level is below a specific threshold.</span></span>

<span data-ttu-id="08de5-150">Hvis du definerer en multiplummængde for et produkt, vil genopfyldningsmetoden *Min./Maks.*</span><span class="sxs-lookup"><span data-stu-id="08de5-150">If you define a multiple quantity for a product, the *Min./Max.*</span></span> <span data-ttu-id="08de5-151">ændrer funktionaliteten og tage værdien af **Flere** med i beregningen.</span><span class="sxs-lookup"><span data-stu-id="08de5-151">replenishment method changes its behavior and considers the **Multiple** value.</span></span>

<span data-ttu-id="08de5-152">Med andre ord genopfylder Planlægningsoptimering stadig lageret op til det definerede maksimumniveau, når den forventede beholdning er mindre end det definerede minimumniveau.</span><span class="sxs-lookup"><span data-stu-id="08de5-152">In other words, Planning Optimization will still replenish the inventory up to the defined maximum level when the predicted on-hand level is less than the defined minimum level.</span></span> <span data-ttu-id="08de5-153">Genopfyldningsantallet skal dog være et multiplum af værdien for **Flere**.</span><span class="sxs-lookup"><span data-stu-id="08de5-153">However, the replenishment quantity must be a multiple of the **Multiple** value.</span></span>

<span data-ttu-id="08de5-154">Hvis genopfyldningsantallet (forskellen mellem det maksimale niveau og det forventede beholdningsniveau) ikke er et multiplum af den definerede multiplummængde, bruger Planlægningsoptimering den første mulige værdi, der sammen med den forventede beholdning vil være under det maksimale niveau.</span><span class="sxs-lookup"><span data-stu-id="08de5-154">If the replenishment quantity (the difference between the maximum level and the predicted on-hand level) isn't a multiple of the defined multiple quantity, Planning Optimization uses the first possible value that, together with predicted on-hand level, will be below the maximum level.</span></span> <span data-ttu-id="08de5-155">Hvis summen er mindre end minimumniveauet, bruger Planlægningsoptimering den første værdi, der sammen med den forventede beholdning vil være over maksimumniveauet.</span><span class="sxs-lookup"><span data-stu-id="08de5-155">If the sum is less than the minimum level, Planning Optimization uses the first value that, together with predicted on-hand, will be above the maximum level.</span></span>

<span data-ttu-id="08de5-156">Følgende undersektioner indeholder nogle eksempler, der viser, hvordan multiplummængden for ordrer på et produkt påvirker resultatet af genopfyldningsmetoden *Min./Maks.*</span><span class="sxs-lookup"><span data-stu-id="08de5-156">The following subsections provide some examples that show how the multiple order quantity for a product affects the result of the *Min./Max.*</span></span> <span data-ttu-id="08de5-157">.</span><span class="sxs-lookup"><span data-stu-id="08de5-157">replenishment method.</span></span>

### <a name="example-1"></a><span data-ttu-id="08de5-158">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="08de5-158">Example 1</span></span>

<span data-ttu-id="08de5-159">Et produkt har følgende konfiguration:</span><span class="sxs-lookup"><span data-stu-id="08de5-159">A product has the following configuration:</span></span>

- <span data-ttu-id="08de5-160">**Disponeringskode:** *Min./Maks.*</span><span class="sxs-lookup"><span data-stu-id="08de5-160">**Coverage code:** *Min./Max.*</span></span>
- <span data-ttu-id="08de5-161">**Minimum:** *15*</span><span class="sxs-lookup"><span data-stu-id="08de5-161">**Minimum:** *15*</span></span>
- <span data-ttu-id="08de5-162">**Maksimum:** *22*</span><span class="sxs-lookup"><span data-stu-id="08de5-162">**Maximum:** *22*</span></span>
- <span data-ttu-id="08de5-163">**Multiplum:** *0*</span><span class="sxs-lookup"><span data-stu-id="08de5-163">**Multiple:** *0*</span></span>

<span data-ttu-id="08de5-164">Der er 10 styk af produktet i lagerbeholdningen, og der er ingen anden efterspørgsel eller forsyning.</span><span class="sxs-lookup"><span data-stu-id="08de5-164">There are 10 pieces of on-hand inventory for the product, and there is no other demand or supply.</span></span>

<span data-ttu-id="08de5-165">Når varedisponering kører, oprettes der et ordreforslag på 12 styk for at genopfylde lageret med det maksimale antal.</span><span class="sxs-lookup"><span data-stu-id="08de5-165">When master planning runs, a planned order for 12 pieces is created to replenish inventory to the maximum quantity.</span></span>

### <a name="example-2"></a><span data-ttu-id="08de5-166">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="08de5-166">Example 2</span></span>

<span data-ttu-id="08de5-167">Et produkt har følgende konfiguration:</span><span class="sxs-lookup"><span data-stu-id="08de5-167">A product has the following configuration:</span></span>

- <span data-ttu-id="08de5-168">**Disponeringskode:** *Min./Maks.*</span><span class="sxs-lookup"><span data-stu-id="08de5-168">**Coverage code:** *Min./Max.*</span></span>
- <span data-ttu-id="08de5-169">**Minimum:** *15*</span><span class="sxs-lookup"><span data-stu-id="08de5-169">**Minimum:** *15*</span></span>
- <span data-ttu-id="08de5-170">**Maksimum:** *22*</span><span class="sxs-lookup"><span data-stu-id="08de5-170">**Maximum:** *22*</span></span>
- <span data-ttu-id="08de5-171">**Multiplum:** *5*</span><span class="sxs-lookup"><span data-stu-id="08de5-171">**Multiple:** *5*</span></span>

<span data-ttu-id="08de5-172">Der er 10 styk af produktet i lagerbeholdningen, og der er ingen anden efterspørgsel eller forsyning.</span><span class="sxs-lookup"><span data-stu-id="08de5-172">There are 10 pieces of on-hand inventory for the product, and there is no other demand or supply.</span></span>

<span data-ttu-id="08de5-173">Når varedisponering kører, oprettes der et ordreforslag på 10 styk (fordi 15 styk af genopfyldning plus 10 styk af den disponible lagerbeholdning vil overstige det maksimale antal).</span><span class="sxs-lookup"><span data-stu-id="08de5-173">When master planning runs, a planned order for 10 pieces is created (because 15 pieces of replenishment plus 10 pieces of on-hand inventory will exceed the maximum quantity).</span></span>

### <a name="example-3"></a><span data-ttu-id="08de5-174">Eksempel 3</span><span class="sxs-lookup"><span data-stu-id="08de5-174">Example 3</span></span>

<span data-ttu-id="08de5-175">Et produkt har følgende konfiguration:</span><span class="sxs-lookup"><span data-stu-id="08de5-175">A product has the following configuration:</span></span>

- <span data-ttu-id="08de5-176">**Disponeringskode:** *Min./Maks.*</span><span class="sxs-lookup"><span data-stu-id="08de5-176">**Coverage code:** *Min./Max.*</span></span>
- <span data-ttu-id="08de5-177">**Minimum:** *21*</span><span class="sxs-lookup"><span data-stu-id="08de5-177">**Minimum:** *21*</span></span>
- <span data-ttu-id="08de5-178">**Maksimum:** *24*</span><span class="sxs-lookup"><span data-stu-id="08de5-178">**Maximum:** *24*</span></span>
- <span data-ttu-id="08de5-179">**Multiplum:** *5*</span><span class="sxs-lookup"><span data-stu-id="08de5-179">**Multiple:** *5*</span></span>

<span data-ttu-id="08de5-180">Der er 10 styk af produktet i lagerbeholdningen, og der er ingen anden efterspørgsel eller forsyning.</span><span class="sxs-lookup"><span data-stu-id="08de5-180">There are 10 pieces of on-hand inventory for the product, and there is no other demand or supply.</span></span>

<span data-ttu-id="08de5-181">Når varedisponering kører, oprettes ordreforslaget på 15 styk (fordi 10 styk af genopfyldning plus 10 styk af den disponible lagerbeholdning vil være mindre end det minimale antal).</span><span class="sxs-lookup"><span data-stu-id="08de5-181">When master planning runs, the planned order for 15 pieces is created (because 10 pieces of replenishment plus 10 pieces of on-hand inventory will be less than the minimum quantity).</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
