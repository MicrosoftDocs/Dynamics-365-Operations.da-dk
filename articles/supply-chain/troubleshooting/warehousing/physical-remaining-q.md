---
title: Fysisk restantal i enheden må ikke være nul
description: Når du opretter en følgeseddel, har de data, der leveres til den, et lagerantal, der ikke er nul, men et salgsantal på nul.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningListPage_WHSSalesPackingSlipPost, WHSLoadTable_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: bfd381160bcfd1e6e5489e16cc22178b8a5142ee
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/14/2021
ms.locfileid: "6248772"
---
# <a name="physical-remaining-quantity-in-the-unit-must-not-be-zero"></a><span data-ttu-id="1328e-103">Fysisk restantal i enheden må ikke være nul</span><span class="sxs-lookup"><span data-stu-id="1328e-103">Physical remaining quantity in the unit must not be zero</span></span>

<span data-ttu-id="1328e-104">Fejlkode: SYS19591</span><span class="sxs-lookup"><span data-stu-id="1328e-104">Error code: SYS19591</span></span>

## <a name="symptoms"></a><span data-ttu-id="1328e-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="1328e-105">Symptoms</span></span>

<span data-ttu-id="1328e-106">Når du opretter en følgeseddel, har de data, der leveres til den, et lagerantal, der ikke er nul, men et salgsantal på nul.</span><span class="sxs-lookup"><span data-stu-id="1328e-106">When you generate a packing slip, the data that is supplied to it has a non-zero inventory quantity but a zero sales quantity.</span></span>

<span data-ttu-id="1328e-107">Når du forsøger at oprette følgesedlen, vises følgende fejlmeddelelse:</span><span class="sxs-lookup"><span data-stu-id="1328e-107">When you try to generate the packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="1328e-108">Fysisk rest i enheden %1 skal være forskellig fra nul.</span><span class="sxs-lookup"><span data-stu-id="1328e-108">Physical remaining quantity in the unit %1 must be other than zero.</span></span>

<span data-ttu-id="1328e-109">Du kan derfor ikke oprette følgesedlen for lasten.</span><span class="sxs-lookup"><span data-stu-id="1328e-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="1328e-110">Årsag</span><span class="sxs-lookup"><span data-stu-id="1328e-110">Cause</span></span>

<span data-ttu-id="1328e-111">Systemet evaluerer det fysiske restantal i lagerenheden og det fysisk restantal i forsendelsesenheden.</span><span class="sxs-lookup"><span data-stu-id="1328e-111">The system evaluates the physical remaining quantity in the inventory unit and the physical remaining quantity in the shipping unit.</span></span> <span data-ttu-id="1328e-112">Hvis det fysiske restantal i forsendelsesenheden er 0 (nul), men det fysiske restantal i lagerenheden ikke er 0, kan du ikke oprette følgesedlen.</span><span class="sxs-lookup"><span data-stu-id="1328e-112">If the system finds that the physical remaining quantity in the shipping unit is 0 (zero), but the physical remaining quantity in the inventory unit isn't 0, you can't generate the packing slip.</span></span> <span data-ttu-id="1328e-113">Dette problem kan for eksempel forekomme, hvis salgsenheden og lagerenheden for varen er forskellig, og omregningen mellem enheder ikke er nøjagtig.</span><span class="sxs-lookup"><span data-stu-id="1328e-113">For example, this issue might occur if the sales unit and inventory unit for the item differ, and the conversion between units isn't accurate.</span></span>

## <a name="resolution"></a><span data-ttu-id="1328e-114">Løsning</span><span class="sxs-lookup"><span data-stu-id="1328e-114">Resolution</span></span>

<span data-ttu-id="1328e-115">Lasten eller forsendelsen er i øjeblikket i en tilstand, hvor der ikke kan oprettes en følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="1328e-115">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="1328e-116">Du kan håndtere dette problem ved at udføre en eller flere af følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="1328e-116">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="1328e-117">Gennemse dine lastlinjer, og kontrollér, at alt det relaterede arbejde er fuldført på den endelige forsendelseslokation, og at mængderne stemmer overens.</span><span class="sxs-lookup"><span data-stu-id="1328e-117">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="1328e-118">Gennemse lastlinjerne, og foretag justeringer for at sikre, at antallet kan konverteres rent uden afrundingsproblemer.</span><span class="sxs-lookup"><span data-stu-id="1328e-118">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without rounding issues.</span></span>
- <span data-ttu-id="1328e-119">Gennemse lastlinjerne, og foretag justeringer for at sikre, at enheden og antallet er tilpasset enhedens decimalpræcision.</span><span class="sxs-lookup"><span data-stu-id="1328e-119">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>
- <span data-ttu-id="1328e-120">Kontrollér, at måleenheden for lageret er mindre end måleenheden for salg.</span><span class="sxs-lookup"><span data-stu-id="1328e-120">Make sure that the inventory unit of measure is smaller than the sales unit of measure.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="1328e-121">Gennemse dine lastlinjer, og kontrollér, at alt det relaterede arbejde er fuldført på den endelige forsendelseslokation, og at mængderne stemmer overens</span><span class="sxs-lookup"><span data-stu-id="1328e-121">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="1328e-122">Brug følgende procedure til at gennemse dine lastlinjer og kontrollere, at alt det relaterede arbejde er fuldført på den endelige forsendelseslokation, og at mængderne stemmer overens.</span><span class="sxs-lookup"><span data-stu-id="1328e-122">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="1328e-123">Gå til **Lokationsstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="1328e-123">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="1328e-124">Vælg den last, som forsendelsen ikke kan bekræftes for.</span><span class="sxs-lookup"><span data-stu-id="1328e-124">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="1328e-125">Vælg linjen for lasten i oversigtspanelet **Lastlinjer**.</span><span class="sxs-lookup"><span data-stu-id="1328e-125">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="1328e-126">Notér værdien for feltet **Antal oprettet under arbejde**.</span><span class="sxs-lookup"><span data-stu-id="1328e-126">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="1328e-127">under fanen **Laster** i gruppen **Relaterede oplysninger** i handlingsruden skal du vælge **Arbejde**.</span><span class="sxs-lookup"><span data-stu-id="1328e-127">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="1328e-128">Kontrollér, at arbejdet er udført på den endelige forsendelseslokation, og at det plukkede arbejdsantal svarer til det oprettede arbejdsantal på lastlinjen.</span><span class="sxs-lookup"><span data-stu-id="1328e-128">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="1328e-129">Gentag denne procedure for alle lastlinjer for at sikre, at alle kriterier er opfyldt.</span><span class="sxs-lookup"><span data-stu-id="1328e-129">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-rounding-issues"></a><span data-ttu-id="1328e-130">Gennemse lastlinjerne, og foretag justeringer for at sikre, at antallet kan konverteres rent uden afrundingsproblemer</span><span class="sxs-lookup"><span data-stu-id="1328e-130">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without rounding issues</span></span>

<span data-ttu-id="1328e-131">Brug følgende procedure til at gennemse lastlinjerne og foretage justeringer for at sikre, at antallet kan konverteres rent uden afrundingsproblemer.</span><span class="sxs-lookup"><span data-stu-id="1328e-131">Use the following procedure to review your load lines and make adjustments to ensure that the quantity can be cleanly converted without rounding issues.</span></span>

1. <span data-ttu-id="1328e-132">Gå til **Lokationsstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="1328e-132">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="1328e-133">Vælg den last, som følgesedlen ikke kan genereres for.</span><span class="sxs-lookup"><span data-stu-id="1328e-133">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="1328e-134">Vælg  **Tilbagefør forsendelsesbekræftelse** i gruppen  **Tilbagefør** under fanen  **Levér og modtag** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="1328e-134">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="1328e-135">Vælg lastlinjen for den vare, der overstiger overleveringen, under fanen  **Lastlinjer**.</span><span class="sxs-lookup"><span data-stu-id="1328e-135">On the **Load lines** tab, select the load line for the item that exceeds the over-delivery.</span></span>
1. <span data-ttu-id="1328e-136">Vælg **Reducer plukket antal** for at justere det plukkede antal.</span><span class="sxs-lookup"><span data-stu-id="1328e-136">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="1328e-137">Vælg **Ordre** under fanen  **Linjedetaljer**.</span><span class="sxs-lookup"><span data-stu-id="1328e-137">On the  **Line details** tab, select **Order**.</span></span>
1. <span data-ttu-id="1328e-138">Angiv feltet **Antal** til det plukkede antal (dvs. værdien for feltet **Antal oprettet under arbejde**), så du kan fortsætte med at generere følgesedlen.</span><span class="sxs-lookup"><span data-stu-id="1328e-138">Set the **Quantity** field to the picked quantity (that is, the value of the **Work created quantity** field), so that packing slip generation can proceed.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-unit-and-quantity-are-aligned-with-the-decimal-precision-of-the-unit"></a><span data-ttu-id="1328e-139">Gennemse lastlinjerne, og foretag justeringer for at sikre, at enheden og antallet er tilpasset enhedens decimalpræcision</span><span class="sxs-lookup"><span data-stu-id="1328e-139">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit</span></span>

<span data-ttu-id="1328e-140">Brug følgende procedure til at gennemse lastlinjerne og foretage justeringer for at sikre, at enheden og antallet er tilpasset enhedens decimalpræcision.</span><span class="sxs-lookup"><span data-stu-id="1328e-140">Use the following procedure to review your load lines and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>

1. <span data-ttu-id="1328e-141">Gå til **Lokationsstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="1328e-141">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="1328e-142">Vælg den last, som følgesedlen ikke kan genereres for.</span><span class="sxs-lookup"><span data-stu-id="1328e-142">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="1328e-143">Vælg lastlinjen for den vare, der forårsager et problem, i oversigtspanelet **Lastlinjer**.</span><span class="sxs-lookup"><span data-stu-id="1328e-143">On the **Load lines** FastTab, select the load line for the item that causes an issue.</span></span> <span data-ttu-id="1328e-144">Notér værdien for felterne **Antal** og **Enhed**.</span><span class="sxs-lookup"><span data-stu-id="1328e-144">Make a note of the value of the **Quantity** and **Unit** fields.</span></span>
1. <span data-ttu-id="1328e-145">Gå til **Virksomhedsadministration \> Enheder \> Enheder**.</span><span class="sxs-lookup"><span data-stu-id="1328e-145">Go to **Organization administration \> Units \> Units**.</span></span>
1. <span data-ttu-id="1328e-146">Vælg den enhed, som følgesedlen ikke kan genereres for.</span><span class="sxs-lookup"><span data-stu-id="1328e-146">Select the unit that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="1328e-147">Juster værdien i feltet **Decimalpræcision** efter behov.</span><span class="sxs-lookup"><span data-stu-id="1328e-147">Adjust the value of the **Decimal precision** field as required.</span></span>

### <a name="make-sure-that-the-inventory-unit-of-measure-is-smaller-than-the-sales-unit-of-measure"></a><span data-ttu-id="1328e-148">Kontrollér, at måleenheden for lageret er mindre end måleenheden for salg</span><span class="sxs-lookup"><span data-stu-id="1328e-148">Make sure that the inventory unit of measure is smaller than the sales unit of measure</span></span>

<span data-ttu-id="1328e-149">Kontrollér, at måleenheden for lageret er mindre end måleenheden for salg.</span><span class="sxs-lookup"><span data-stu-id="1328e-149">Make sure that the inventory unit of measure is smaller than the sales unit of measure.</span></span> <span data-ttu-id="1328e-150">Overvej at omkonfigurere måleenheden for varen efter behov.</span><span class="sxs-lookup"><span data-stu-id="1328e-150">Consider reconfiguring the unit of measure for the item as required.</span></span>
