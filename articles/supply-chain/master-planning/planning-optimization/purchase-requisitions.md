---
title: Indkøbsrekvisitioner
description: Dette emne beskriver, hvordan indkøbsrekvisitioner understøttes i Planlægningsoptimering.
author: ChristianRytt
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqPlanSched, ReqGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 564f87fe78e79107feb103f953ed4769e4734aa1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808034"
---
# <a name="purchase-requisitions"></a><span data-ttu-id="a01f0-103">Indkøbsrekvisitioner</span><span class="sxs-lookup"><span data-stu-id="a01f0-103">Purchase requisitions</span></span>

<span data-ttu-id="a01f0-104">Ved varedisponering kan godkendte indkøbsrekvisitioner genopfyldes.</span><span class="sxs-lookup"><span data-stu-id="a01f0-104">Master planning can replenish approved purchase requisitions.</span></span> <span data-ttu-id="a01f0-105">Derfor behøver brugerne ikke bruge en arbejdsproces til at oprette indkøbsordrer for at dække indkøbsrekvisitioner.</span><span class="sxs-lookup"><span data-stu-id="a01f0-105">Therefore, to cover purchase requisitions, users don't have to use a workflow to create purchase orders.</span></span> <span data-ttu-id="a01f0-106">Indkøbsrekvisitioner kan i stedet dækkes af varedisponeringen.</span><span class="sxs-lookup"><span data-stu-id="a01f0-106">Instead, purchase requisitions can be covered by master planning.</span></span> <span data-ttu-id="a01f0-107">På grund af denne funktion kan en indkøbsrekvisition oprette en indkøbsordre, en flytteordre eller en produktionsordre afhængigt af den **Ordreforslagstype**-værdi, der er angivet for det relaterede produkt.</span><span class="sxs-lookup"><span data-stu-id="a01f0-107">Because of this functionality, a purchase requisition can produce a purchase order, a transfer order, or a production order, depending on the **Planned order type** value that is set for the related product.</span></span>

## <a name="enable-master-plans-to-include-requisitions"></a><span data-ttu-id="a01f0-108">Gøre det muligt for behovsplaner at indeholde rekvisitioner</span><span class="sxs-lookup"><span data-stu-id="a01f0-108">Enable master plans to include requisitions</span></span>

<span data-ttu-id="a01f0-109">Du kan medtage rekvisitioner under beregningen af disponeringen for en behovsplan ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="a01f0-109">To include requisitions during the coverage calculation for a master plan, follow these steps.</span></span>

1. <span data-ttu-id="a01f0-110">Gå til **Varedisponering** \> **Opsætning** \> **Planer** \> **Behovsplaner**.</span><span class="sxs-lookup"><span data-stu-id="a01f0-110">Go to **Master planning** \> **Setup** \> **Plans** \> **Master plans**.</span></span>
1. <span data-ttu-id="a01f0-111">Opret eller vælg en behovsplan.</span><span class="sxs-lookup"><span data-stu-id="a01f0-111">Create or select a master plan.</span></span>
1. <span data-ttu-id="a01f0-112">I oversigtspanelet **Generelt** skal du angive indstillingen **Medtag rekvisitioner** til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="a01f0-112">On the **General** FastTab, set the **Include requisitions** option to *Yes*.</span></span>
1. <span data-ttu-id="a01f0-113">Gentag trin 2 og 3 for hver ekstra behovsplan, hvor du vil medtage rekvisitioner.</span><span class="sxs-lookup"><span data-stu-id="a01f0-113">Repeat steps 2 and 3 for each additional master plan where you want to include requisitions.</span></span>

## <a name="approved-requisitions-time-fence"></a><span data-ttu-id="a01f0-114">Tidshorisont for godkendte rekvisitioner</span><span class="sxs-lookup"><span data-stu-id="a01f0-114">Approved requisitions time fence</span></span>

<span data-ttu-id="a01f0-115">*Tidshorisonten for godkendte rekvisitioner* fastlægger, hvor langt tilbage (i dage) en behovsplan vil medtage efterspørgsler fra godkendte genopfyldningsrekvisitioner.</span><span class="sxs-lookup"><span data-stu-id="a01f0-115">The *approved requisitions time fence* establishes how far back (in days) a master plan will include demand from approved replenishment requisitions.</span></span> <span data-ttu-id="a01f0-116">Du kan angive en tidshorisont for godkendte rekvisitioner på både disponeringsgruppeniveau og behovsplanniveau.</span><span class="sxs-lookup"><span data-stu-id="a01f0-116">You can set an approved requisitions time fence at both the coverage group level and the master plan level.</span></span>

### <a name="set-the-approved-requisitions-time-fence-for-a-coverage-group"></a><span data-ttu-id="a01f0-117">Angive tidshorisonten for godkendte rekvisitioner for en disponeringsgruppe</span><span class="sxs-lookup"><span data-stu-id="a01f0-117">Set the approved requisitions time fence for a coverage group</span></span>

1. <span data-ttu-id="a01f0-118">Gå til **Varedisponering** \> **Opsætning** \> **Dækning** \> **Dækningsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="a01f0-118">Go to **Master planning** \> **Setup** \> **Coverage** \> **Coverage groups**.</span></span>
1. <span data-ttu-id="a01f0-119">Opret eller vælg en disponeringsgruppe.</span><span class="sxs-lookup"><span data-stu-id="a01f0-119">Create or select a coverage group.</span></span>
1. <span data-ttu-id="a01f0-120">På oversigtspanelet **Andet** skal du angive **Tidshorisont (dage) for godkendte rekvisitioner** til det antal dage, der skal medtages i tidshorisonten.</span><span class="sxs-lookup"><span data-stu-id="a01f0-120">On the **Other** FastTab, set the **Approved requisitions time fence (days)** field to the number of days to include in the time fence.</span></span>
1. <span data-ttu-id="a01f0-121">Gentag trin 2 og 3 for hver ekstra disponeringsgruppe, hvor du vil angive en tidshorisont for godkendte rekvisitioner.</span><span class="sxs-lookup"><span data-stu-id="a01f0-121">Repeat steps 2 and 3 for each additional coverage group where you want to set an approved requisitions time fence.</span></span>

### <a name="set-the-approved-requisitions-time-fence-for-individual-master-plans"></a><span data-ttu-id="a01f0-122">Angive tidshorisonten for godkendte rekvisitioner for forskellige behovsplaner</span><span class="sxs-lookup"><span data-stu-id="a01f0-122">Set the approved requisitions time fence for individual master plans</span></span>

<span data-ttu-id="a01f0-123">Når du angiver en tidshorisont for godkendte rekvisitioner for en enkelt behovsplan, tilsidesætter indstillingen tidshorisonten for alle relevante disponeringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="a01f0-123">When you set an approved requisitions time fence for an individual master plan, the setting overrides the time fence setting for any applicable coverage group.</span></span>

1. <span data-ttu-id="a01f0-124">Gå til **Varedisponering** \> **Opsætning** \> **Planer** \> **Behovsplaner**.</span><span class="sxs-lookup"><span data-stu-id="a01f0-124">Go to **Master planning** \> **Setup** \> **Plans** \> **Master plans**.</span></span>
1. <span data-ttu-id="a01f0-125">Opret eller vælg en behovsplan.</span><span class="sxs-lookup"><span data-stu-id="a01f0-125">Create or select a master plan.</span></span>
1. <span data-ttu-id="a01f0-126">På oversigtspanelet **Tidshorisonter i dage** skal du angive **Tidshorisont (dage) for godkendte rekvisitioner** til det antal dage, der skal medtages i tidshorisonten.</span><span class="sxs-lookup"><span data-stu-id="a01f0-126">On the **TIme fences in days** FastTab, set the **Approved requisitions time fence (days)** field to the number of days to include in the time fence.</span></span>
1. <span data-ttu-id="a01f0-127">Gentag trin 2 og 3 for hver ekstra behovsplan, hvor du vil angive en tidshorisont for godkendte rekvisitioner.</span><span class="sxs-lookup"><span data-stu-id="a01f0-127">Repeat steps 2 and 3 for each additional master plan where you want to set an approved requisitions time fence.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a01f0-128">**Kommer snart:** Tidshorisonter for godkendte rekvisitioner understøttes endnu ikke til Planlægningsoptimering.</span><span class="sxs-lookup"><span data-stu-id="a01f0-128">**Coming soon:** Approved requisitions time fences aren't yet supported for Planning Optimization.</span></span> <span data-ttu-id="a01f0-129">Indtil de understøttes, ignoreres alle de værdier, du angiver i feltet **Tidshorisont (dage) for godkendte rekvisitioner**.</span><span class="sxs-lookup"><span data-stu-id="a01f0-129">Until they are supported, all values that you enter in the **Approved requisitions time fence (days)** field will be ignored.</span></span>

## <a name="independent-supply-regardless-of-coverage-code"></a><span data-ttu-id="a01f0-130">Uafhængig forsyning, uanset disponeringskoden</span><span class="sxs-lookup"><span data-stu-id="a01f0-130">Independent supply, regardless of coverage code</span></span>

<span data-ttu-id="a01f0-131">Indkøbsrekvisitioner dækkes altid af uafhængige ordreforslag, uanset disponeringskoden.</span><span class="sxs-lookup"><span data-stu-id="a01f0-131">Purchase requisitions are always covered by independent planned orders, regardless of the coverage code.</span></span> <span data-ttu-id="a01f0-132">Denne funktionalitet sikrer klar sporing og klare arbejdsprocesser mellem indkøbsrekvisitioner og genopfyldningsordrer.</span><span class="sxs-lookup"><span data-stu-id="a01f0-132">This behavior ensures clear traceability and workflows between purchase requisitions and replenishment orders.</span></span>

### <a name="example-1"></a><span data-ttu-id="a01f0-133">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="a01f0-133">Example 1</span></span>

<span data-ttu-id="a01f0-134">Et produkt er konfigureret til at have en **disponeringskodeværdi** på *min./maks.*. Det har følgende statusser for lager og rekvisitioner:</span><span class="sxs-lookup"><span data-stu-id="a01f0-134">A product is set up so that it has a **Coverage code** value of *Min/max*. It has the following inventory and requisition statuses:</span></span>

- <span data-ttu-id="a01f0-135">Mængde disponibel lagerbeholdning = 10.</span><span class="sxs-lookup"><span data-stu-id="a01f0-135">Inventory on-hand quantity = 10.</span></span>
- <span data-ttu-id="a01f0-136">Minimum lagerantal = 15.</span><span class="sxs-lookup"><span data-stu-id="a01f0-136">Minimum inventory quantity = 15.</span></span>
- <span data-ttu-id="a01f0-137">Maks. lagerantal = 20.</span><span class="sxs-lookup"><span data-stu-id="a01f0-137">Maximum inventory quantity = 20.</span></span>
- <span data-ttu-id="a01f0-138">Der findes en indkøbsrekvisition for ét styk.</span><span class="sxs-lookup"><span data-stu-id="a01f0-138">A purchase requisition for one piece exists.</span></span> <span data-ttu-id="a01f0-139">Den har en ønsket dato for dags dato.</span><span class="sxs-lookup"><span data-stu-id="a01f0-139">It has a requested date of today.</span></span>

<span data-ttu-id="a01f0-140">Når varedisponering kører, oprettes der to ordreforslag: et på 10 styk for at genopfylde lageret med det maksimale antal, og et på ét styk for at genopfylde indkøbsrekvisitionen.</span><span class="sxs-lookup"><span data-stu-id="a01f0-140">When master planning runs, two planned orders are created: one for 10 pieces to replenish inventory to the maximum quantity, and one for one piece to replenish the purchase requisition.</span></span>

### <a name="example-2"></a><span data-ttu-id="a01f0-141">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="a01f0-141">Example 2</span></span>

<span data-ttu-id="a01f0-142">Et produkt er konfigureret til at have en **disponeringskodeværdi** på *min./maks.*. Det har følgende statusser for lager og rekvisitioner:</span><span class="sxs-lookup"><span data-stu-id="a01f0-142">A product is set up so that it has a **Coverage code** value of *Min/max*. It has the following inventory and requisition statuses:</span></span>

- <span data-ttu-id="a01f0-143">Mængde disponibel lagerbeholdning = 17.</span><span class="sxs-lookup"><span data-stu-id="a01f0-143">Inventory on-hand quantity = 17.</span></span>
- <span data-ttu-id="a01f0-144">Minimum lagerantal = 15.</span><span class="sxs-lookup"><span data-stu-id="a01f0-144">Minimum inventory quantity = 15.</span></span>
- <span data-ttu-id="a01f0-145">Maks. lagerantal = 20.</span><span class="sxs-lookup"><span data-stu-id="a01f0-145">Maximum inventory quantity = 20.</span></span>
- <span data-ttu-id="a01f0-146">Der findes en indkøbsrekvisition for ét styk.</span><span class="sxs-lookup"><span data-stu-id="a01f0-146">A purchase requisition for one piece exists.</span></span> <span data-ttu-id="a01f0-147">Den har en ønsket dato for dags dato.</span><span class="sxs-lookup"><span data-stu-id="a01f0-147">It has a requested date of today.</span></span>

<span data-ttu-id="a01f0-148">Når varedisponering kører, oprettes der et ordreforslag for ét styk til genopfyldning af indkøbsrekvisitionen.</span><span class="sxs-lookup"><span data-stu-id="a01f0-148">When master planning runs, one planned order for one piece is created to replenish the purchase requisition.</span></span>

### <a name="example-3"></a><span data-ttu-id="a01f0-149">Eksempel 3</span><span class="sxs-lookup"><span data-stu-id="a01f0-149">Example 3</span></span>

<span data-ttu-id="a01f0-150">Et produkt er konfigureret til at have en **disponeringskodeværdi** for *Periode* og en periodelængde på syv dage.</span><span class="sxs-lookup"><span data-stu-id="a01f0-150">A product is set up so that it has a **Coverage code** value of *Period* and a period length of seven days.</span></span> <span data-ttu-id="a01f0-151">Den har følgende statusser for lager, salgsordre og rekvisition:</span><span class="sxs-lookup"><span data-stu-id="a01f0-151">It has the following inventory, sales order, and requisition statuses:</span></span>

- <span data-ttu-id="a01f0-152">Mængde disponibel lagerbeholdning = 0.</span><span class="sxs-lookup"><span data-stu-id="a01f0-152">Inventory on-hand quantity = 0.</span></span>
- <span data-ttu-id="a01f0-153">Der findes en salgsordre på fem styk.</span><span class="sxs-lookup"><span data-stu-id="a01f0-153">A sales order for five pieces exists.</span></span> <span data-ttu-id="a01f0-154">Den har en forventet afsendelsesdato i dag plus én dag.</span><span class="sxs-lookup"><span data-stu-id="a01f0-154">It has an expected ship date of today plus one day.</span></span>
- <span data-ttu-id="a01f0-155">Der findes en indkøbsrekvisition for tre styk.</span><span class="sxs-lookup"><span data-stu-id="a01f0-155">A purchase requisition for three pieces exists.</span></span> <span data-ttu-id="a01f0-156">Den har en ønsket dato for dags dato plus tre dage.</span><span class="sxs-lookup"><span data-stu-id="a01f0-156">It has a requested date of today plus three days.</span></span>

<span data-ttu-id="a01f0-157">Når varedisponering kører, oprettes der to ordreforslag: et på tre styk for at genopfylde indkøbsrekvisitionen og et på fem styk for at genopfylde salgsordrebehovet.</span><span class="sxs-lookup"><span data-stu-id="a01f0-157">When master planning runs, two planned orders are created: one for three pieces to replenish the purchase requisition and one for five pieces to replenish sales order demand.</span></span>

> [!NOTE]
> <span data-ttu-id="a01f0-158">Når et ordreforslag, der er udlignet til en indkøbsrekvisition, er autoriseret, holder planlægningsprogrammet udligningen på indkøbsrekvisitionen.</span><span class="sxs-lookup"><span data-stu-id="a01f0-158">After a planned order that is pegged to a purchase requisition is firmed, the planning engine keeps the pegging to the purchase requisition.</span></span> <span data-ttu-id="a01f0-159">Hvis den autoriserede ordre senere viser sig at mangle et antal, der skal bruges til at opfylde indkøbsrekvisitionen, opretter systemet et nyt ordreforslag for differencen.</span><span class="sxs-lookup"><span data-stu-id="a01f0-159">If the firmed order is later found to be missing some quantity that is required to fulfill the purchase requisition, the system will create a new planned order for the difference.</span></span>

<span data-ttu-id="a01f0-160">Du kan finde flere oplysninger om indkøbsrekvisitioner i [Oversigt over indkøbsrekvisitioner](../../procurement/purchase-requisitions-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a01f0-160">For more information about purchase requisitions, see [Purchase requisition overview](../../procurement/purchase-requisitions-overview.md).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]