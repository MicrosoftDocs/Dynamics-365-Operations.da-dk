---
title: Fejlfinde batch- og seriereservationshierarkier for lagersteder
description: Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du arbejder med reservationshierarkier, der bruger batch- eller seriedimensioner.
author: perlynne
ms.date: 3/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 3/12/2021
ms.openlocfilehash: 1cd4883cdd95a97f821e0103da910e2c0346a08d
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022540"
---
# <a name="troubleshoot-warehouse-batch-and-serial-reservation-hierarchies"></a><span data-ttu-id="37e2b-103">Fejlfinde batch- og seriereservationshierarkier for lagersteder</span><span class="sxs-lookup"><span data-stu-id="37e2b-103">Troubleshoot warehouse batch and serial reservation hierarchies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="37e2b-104">Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du arbejder med reservationshierarkier, der bruger batch- eller seriedimensioner.</span><span class="sxs-lookup"><span data-stu-id="37e2b-104">This topic describes how to fix common issues that you might encounter while you work with reservation hierarchies that use batch or serial dimensions.</span></span>

<span data-ttu-id="37e2b-105">Du kan finde flere oplysninger under [Fleksibel reservationspolitik for dimension på lagerstedsniveau](flexible-warehouse-level-dimension-reservation.md).</span><span class="sxs-lookup"><span data-stu-id="37e2b-105">For more information, see [Flexible warehouse-level dimension reservation policy](flexible-warehouse-level-dimension-reservation.md).</span></span>

<span data-ttu-id="37e2b-106">Reservationshierarkiet for en vare angiver behovet for lagringsdimensioner, der skal opfyldes, for at der kan knyttes en lokation til en behovsordre.</span><span class="sxs-lookup"><span data-stu-id="37e2b-106">The reservation hierarchy of an item dictates the requirement of storage dimensions that must be fulfilled to assign a location to a demand order.</span></span> <span data-ttu-id="37e2b-107">Disse dimensioner kan beskrives som *dimensioner over lokation* for alle de dimensioner, der skal opfyldes, før lokationen tildeles, og *dimensioner under lokation* for dimensioner, der kan tildeles, når der er tildelt en lokation til behovsordren.</span><span class="sxs-lookup"><span data-stu-id="37e2b-107">These dimensions can be described as *dimensions above location*, for all the dimensions that must be fulfilled before a location is assigned, and *dimensions below location*, for dimensions that can be allocated after a location has been assigned to the demand order.</span></span> <span data-ttu-id="37e2b-108">Disse reservationshierarkier kaldes også *batch over*- og *batch under*-reservationshierarkier eller *serie over*- og *serie under*-reservationshierarkier.</span><span class="sxs-lookup"><span data-stu-id="37e2b-108">These reservation hierarchies are also known as *batch-above* and *batch-below* reservation hierarchies, or *serial-above* and *serial-below* reservation hierarchies.</span></span>

<span data-ttu-id="37e2b-109">Lageret kan kun fordeles, hvis der ikke er huller i dimensionerne over lokationen.</span><span class="sxs-lookup"><span data-stu-id="37e2b-109">Inventory can be successfully allocated only if there are no gaps in the dimensions above location.</span></span> <span data-ttu-id="37e2b-110">I et *batch over*-reservationshierarki kan du f.eks. forvente, at dimensionerne **Lokation**, **Lagersted** og **Batchnummer** angives i behovsordren.</span><span class="sxs-lookup"><span data-stu-id="37e2b-110">For example, in a *batch-above* reservation hierarchy, you expect **Site,** **Warehouse,** and **Batch number** dimensions to be specified on the demand order.</span></span> <span data-ttu-id="37e2b-111">Hvis nogen af disse dimensioner mangler, mislykkes fordelingsprocessen.</span><span class="sxs-lookup"><span data-stu-id="37e2b-111">If any of these dimensions are missing, the allocation process will fail.</span></span> <span data-ttu-id="37e2b-112">Modsat kan der i et *batch under*- eller *serie under*-reservationshierarki angives et batch- eller serienummer på behovsordren, men det kræver fordelingsprocessen ikke.</span><span class="sxs-lookup"><span data-stu-id="37e2b-112">By contrast, in a *batch-below* or *serial-below* reservation hierarchy, a batch or serial number might be specified on the demand order, but the allocation process doesn't require it.</span></span>

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a><span data-ttu-id="37e2b-113">Jeg får vist følgende fejlmeddelelse: "For at blive tildelt en bølge skal lastlinjer angive dimensionerne over lokationen.</span><span class="sxs-lookup"><span data-stu-id="37e2b-113">I receive the following error message: "To be assigned to wave, load lines must specify the dimensions above the location.</span></span> <span data-ttu-id="37e2b-114">Du kan tildele disse dimensioner ved at reservere og genoprette lastlinjen".</span><span class="sxs-lookup"><span data-stu-id="37e2b-114">To assign these dimensions, reserve and recreate the load line."</span></span>

### <a name="issue-description"></a><span data-ttu-id="37e2b-115">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="37e2b-115">Issue description</span></span>

<span data-ttu-id="37e2b-116">Når du bruger en vare, der har et *batch over*-reservationshierarki, vil kommandoen **Frigiv til lagersted** på siden **Panelet Lastplanlægning** ikke fungere, hvis du prøver at frigive en last for en delmængde.</span><span class="sxs-lookup"><span data-stu-id="37e2b-116">When you use an item that has a *batch-above* reservation hierarchy, the **Release to warehouse** command on the **Load planning workbench** page doesn't work if you try to release a load for a partial quantity.</span></span> <span data-ttu-id="37e2b-117">Du får vist denne fejlmeddelelse, og der oprettes ikke noget arbejde for delmængden.</span><span class="sxs-lookup"><span data-stu-id="37e2b-117">You receive this error message, and no work is created for the partial quantity.</span></span>

<span data-ttu-id="37e2b-118">Men, hvis du bruger en vare, der har et *batch under*-reservationshierarki, kan du frigive en last for en delmængde fra siden **Panelet Lastplanlægning**.</span><span class="sxs-lookup"><span data-stu-id="37e2b-118">However, when you use an item that has a *batch-below* reservation hierarchy, you can release a load for a partial quantity from the **Load planning workbench** page.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="37e2b-119">Problemårsag</span><span class="sxs-lookup"><span data-stu-id="37e2b-119">Issue cause</span></span>

<span data-ttu-id="37e2b-120">Når en dimension er over **Lokation**-dimensionen i reservationshierarkiet, skal den angives før frigivelsen til lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="37e2b-120">When a dimension is above the **Location** dimension in the reservation hierarchy, it must be specified before the release to the warehouse.</span></span> <span data-ttu-id="37e2b-121">Delmængder kan ikke frigives, hvis en eller flere dimensioner over **Lokation** ikke er angivet.</span><span class="sxs-lookup"><span data-stu-id="37e2b-121">Partial quantities can't be released if one or more dimensions above **Location** aren't specified.</span></span>

## <a name="the-auto-reservation-prompt-for-a-batch-number-is-triggered-even-though-there-is-available-inventory"></a><span data-ttu-id="37e2b-122">Prompten til automatisk reservation af et batchnummer udløses, selvom der er tilgængelig lagerbeholdning.</span><span class="sxs-lookup"><span data-stu-id="37e2b-122">The auto-reservation prompt for a batch number is triggered even though there is available inventory.</span></span>

### <a name="issue-description"></a><span data-ttu-id="37e2b-123">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="37e2b-123">Issue description</span></span>

<span data-ttu-id="37e2b-124">Når du bruger en vare, der har et *batch over*-reservationshierarki på et lagersted, hvor der ikke er aktiveret lagerstedsprocesser, og automatisk reservation er aktiveret, vises prompten for automatisk reservation af et batchnummer, også selvom der kun er ét tilgængeligt batch til plukning.</span><span class="sxs-lookup"><span data-stu-id="37e2b-124">When you use an item that has a *batch-above* reservation hierarchy in a warehouse that hasn't enabled warehouse processes, and automatic reservation is enabled, the auto-reservation prompt for a batch number is shown even if only one batch is available for picking.</span></span>

<span data-ttu-id="37e2b-125">Men når du bruger den samme vare på et lagersted, hvor lagerprocesser er aktiveret, vises prompten for automatisk reservation ikke.</span><span class="sxs-lookup"><span data-stu-id="37e2b-125">However, when you use the same item in a warehouse where warehouse processes are enabled, the auto-reservation prompt isn't shown.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="37e2b-126">Problemårsag</span><span class="sxs-lookup"><span data-stu-id="37e2b-126">Issue cause</span></span>

<span data-ttu-id="37e2b-127">Hvis et reservationshierarki defineres som *batch over* eller *serie over*, skal den dimension, der refereres til (**Batchnummer** eller **Serienummer**), altid angives ved behovsordrer.</span><span class="sxs-lookup"><span data-stu-id="37e2b-127">If a reservation hierarchy is defined as *batch-above* or *serial-above*, the referenced dimension (**Batch number** or **Serial number**) must always be specified on demand orders.</span></span> <span data-ttu-id="37e2b-128">Lagerstedsprocesserne kan muligvis fuldføre oplysningerne, hvis der er et enkelt batch- eller serienummer tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="37e2b-128">Warehouse processes might be able to complete the information if a single batch or serial number is available.</span></span> <span data-ttu-id="37e2b-129">Men da lagerstedet ikke er aktiveret for lagerstedsprocesser, skal brugeren altid angive alle dimensionerne over **Lokation**.</span><span class="sxs-lookup"><span data-stu-id="37e2b-129">However, because the warehouse isn't enabled for warehouse processes, the user must always specify all the dimensions above **Location**.</span></span>

## <a name="slotting-templates-that-have-the-consider-on-hand-slot-criterion-dont-consider-current-on-hand-inventory-for-batch-enabled-items"></a><span data-ttu-id="37e2b-130">Allokeringsskabeloner med Overvej beholdning som kriterium tager ikke den aktuelle disponible lagerbeholdning i betragtning for batchaktiverede varer.</span><span class="sxs-lookup"><span data-stu-id="37e2b-130">Slotting templates that have the Consider on-hand slot criterion don't consider current on-hand inventory for batch-enabled items.</span></span>

<span data-ttu-id="37e2b-131">Du kan finde flere oplysninger under [Lagerstedsallokering](warehouse-slotting.md).</span><span class="sxs-lookup"><span data-stu-id="37e2b-131">For more information, see [Warehouse slotting](warehouse-slotting.md).</span></span>

### <a name="issue-description"></a><span data-ttu-id="37e2b-132">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="37e2b-132">Issue description</span></span>

<span data-ttu-id="37e2b-133">Allokeringsskabeloner med *Overvej beholdning* som kriterium tager ikke den aktuelle disponible lagerbeholdning i betragtning for *batch over*-varer.</span><span class="sxs-lookup"><span data-stu-id="37e2b-133">Slotting templates that have the *Consider on-hand* slot criterion don't consider current on-hand inventory for *batch-above* items.</span></span> <span data-ttu-id="37e2b-134">De tager kun højde for det, hvis batchnummeret er angivet på salgsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="37e2b-134">They consider it only if the batch number is specified on the sales order line.</span></span>

<span data-ttu-id="37e2b-135">Men når du bruger *batch under*-varer, anses den aktuelle lagerbeholdning for at være forventet.</span><span class="sxs-lookup"><span data-stu-id="37e2b-135">However, when you use *batch-below* items, the current on-hand inventory is considered as expected.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="37e2b-136">Problemårsag</span><span class="sxs-lookup"><span data-stu-id="37e2b-136">Issue cause</span></span>

<span data-ttu-id="37e2b-137">Hovedet til allokeringsskabelonen kan defineres for behovsstrategien *Bestilt*, *Reserveret* eller *Frigivet*.</span><span class="sxs-lookup"><span data-stu-id="37e2b-137">The slotting template header can be defined for the *Ordered,* *Reserved*, or *Released* demand strategy.</span></span> <span data-ttu-id="37e2b-138">I strategien *Bestilt* gælder de samme reservationshierarkikrav, der gælder for reservation eller frigivelse til lagerprocesser.</span><span class="sxs-lookup"><span data-stu-id="37e2b-138">For the *Ordered* demand strategy, the same reservation hierarchy requirements apply that apply to reservation or release to warehouse processes.</span></span> <span data-ttu-id="37e2b-139">Derfor skal der for *batch over*- og *serie under*-reservationshierarkier angives batch- eller serienummer på behovsordren (salg eller flytning).</span><span class="sxs-lookup"><span data-stu-id="37e2b-139">Therefore, for items that have *batch-above* and *serial-below* reservation hierarchies, the batch or serial number must be specified on the demand order (sales or transfer).</span></span> <span data-ttu-id="37e2b-140">Du kan også bruge behovsstrategien *Reserveret* til at vælge batch- eller serienummer, før der genereres behov for lagerstedsallokering.</span><span class="sxs-lookup"><span data-stu-id="37e2b-140">Alternatively, the *Reserved* demand strategy can be used to select the batch or serial number before the warehouse slotting demand is generated.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
