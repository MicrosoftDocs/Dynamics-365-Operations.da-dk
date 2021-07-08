---
title: Decimalafrunding af det fysiske opdateringsantal er ikke korrekt
description: Når du genererer en følgeseddel, indeholder den udgående last et antal, der ikke svarer til den decimalpræcision, der er defineret i enheden.
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
ms.openlocfilehash: 1e63440834f516879aa8ad711bd789e62b0ee993
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/14/2021
ms.locfileid: "6248773"
---
# <a name="decimal-rounding-of-the-physical-updating-quantity-is-incorrect"></a><span data-ttu-id="14668-103">Decimalafrunding af det fysiske opdateringsantal er ikke korrekt</span><span class="sxs-lookup"><span data-stu-id="14668-103">Decimal rounding of the physical updating quantity is incorrect</span></span>

<span data-ttu-id="14668-104">Fejlkode: SYS19589</span><span class="sxs-lookup"><span data-stu-id="14668-104">Error code: SYS19589</span></span>

## <a name="symptoms"></a><span data-ttu-id="14668-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="14668-105">Symptoms</span></span>

<span data-ttu-id="14668-106">Når du genererer en følgeseddel, indeholder den udgående last et antal, der ikke svarer til den decimalpræcision, der er defineret i enheden.</span><span class="sxs-lookup"><span data-stu-id="14668-106">When you generate a packing slip, the outbound load contains a quantity that doesn't match the decimal precision that is defined in the unit.</span></span>

<span data-ttu-id="14668-107">Når du forsøger at oprette en følgeseddel, vises følgende fejlmeddelelse:</span><span class="sxs-lookup"><span data-stu-id="14668-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="14668-108">Fysisk opdateringsantal i enheden %1 er ikke korrekt decimalafrundet.</span><span class="sxs-lookup"><span data-stu-id="14668-108">Decimal rounding of the physical updating quantity in the unit %1 is incorrect.</span></span>

<span data-ttu-id="14668-109">Du kan derfor ikke oprette følgesedlen for lasten.</span><span class="sxs-lookup"><span data-stu-id="14668-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="14668-110">Årsag</span><span class="sxs-lookup"><span data-stu-id="14668-110">Cause</span></span>

<span data-ttu-id="14668-111">Systemet evaluerer, om decimalafrunding af afsendelsesantallet svarer til den decimalpræcision, der er defineret for forsendelsesenheden.</span><span class="sxs-lookup"><span data-stu-id="14668-111">The system evaluates whether the decimal rounding of the shipping quantity corresponds to the decimal precision that is defined for the shipping unit.</span></span> <span data-ttu-id="14668-112">Når systemet afrunder afsendelsesantallet til det angivne antal decimaler, kan du ikke generere følgesedlen, hvis det afrundede afsendelsesantal ikke svarer til det faktiske afsendelsesantal.</span><span class="sxs-lookup"><span data-stu-id="14668-112">When the system rounds the shipping quantity to the specified number of decimal places, if it finds that the rounded shipping quantity doesn't match the actual shipping quantity, you can't generate the packing slip.</span></span> <span data-ttu-id="14668-113">Dette problem kan f.eks. forekomme, hvis salgsantallet er 1,75 kg, men decimalpræcisionen er angivet til *1*.</span><span class="sxs-lookup"><span data-stu-id="14668-113">For example, this issue might occur if the sales quantity is 1.75 kilograms (kg), but the decimal precision is set to *1*.</span></span>

## <a name="resolution"></a><span data-ttu-id="14668-114">Løsning</span><span class="sxs-lookup"><span data-stu-id="14668-114">Resolution</span></span>

<span data-ttu-id="14668-115">Lasten eller forsendelsen er i øjeblikket i en tilstand, hvor der ikke kan oprettes en følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="14668-115">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="14668-116">Du kan håndtere dette problem ved at udføre en eller flere af følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="14668-116">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="14668-117">Gennemse lastlinjerne, og foretag justeringer for at sikre, at antallet kan konverteres rent uden decimaltal og andre afrundingsproblemer.</span><span class="sxs-lookup"><span data-stu-id="14668-117">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without decimal numbers and any other rounding issues.</span></span>
- <span data-ttu-id="14668-118">Gennemse lastlinjerne, og foretag justeringer for at sikre, at enheden og antallet er tilpasset enhedens decimalpræcision.</span><span class="sxs-lookup"><span data-stu-id="14668-118">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-decimal-numbers-and-any-other-rounding-issues"></a><span data-ttu-id="14668-119">Gennemse lastlinjerne, og foretag justeringer for at sikre, at antallet kan konverteres rent uden decimaltal og andre afrundingsproblemer</span><span class="sxs-lookup"><span data-stu-id="14668-119">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without decimal numbers and any other rounding issues</span></span>

<span data-ttu-id="14668-120">Brug følgende procedure til at gennemse lastlinjerne og foretage justeringer for at sikre, at antallet kan konverteres rent uden decimaltal og andre afrundingsproblemer.</span><span class="sxs-lookup"><span data-stu-id="14668-120">Use the following procedure to review your load lines and make adjustments to ensure that the quantity can be cleanly converted without decimal numbers and any other rounding issues.</span></span>

1. <span data-ttu-id="14668-121">Gå til **Lokationsstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="14668-121">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="14668-122">Vælg den last, som følgesedlen ikke kan genereres for.</span><span class="sxs-lookup"><span data-stu-id="14668-122">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="14668-123">Vælg  **Tilbagefør forsendelsesbekræftelse** i gruppen  **Tilbagefør** under fanen  **Levér og modtag** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="14668-123">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="14668-124">Vælg lastlinjen for den vare, der forårsager et problem, under fanen  **Lastlinjer**.</span><span class="sxs-lookup"><span data-stu-id="14668-124">On the **Load lines** tab, select the load line for the item that causes an issue.</span></span>
1. <span data-ttu-id="14668-125">Vælg **Reducer plukket antal** for at justere det plukkede antal.</span><span class="sxs-lookup"><span data-stu-id="14668-125">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="14668-126">Vælg **Ordre** under fanen  **Linjedetaljer**.</span><span class="sxs-lookup"><span data-stu-id="14668-126">On the  **Line details** tab, select **Order**.</span></span>
1. <span data-ttu-id="14668-127">Angiv feltet **Antal** til det plukkede antal (dvs. værdien for feltet **Antal oprettet under arbejde**), så du kan fortsætte med at generere følgesedlen.</span><span class="sxs-lookup"><span data-stu-id="14668-127">Set the **Quantity** field to the picked quantity (that is, the value of the **Work created quantity** field), so that packing slip generation can proceed.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-unit-and-quantity-are-aligned-with-the-decimal-precision-of-the-unit"></a><span data-ttu-id="14668-128">Gennemse lastlinjerne, og foretag justeringer for at sikre, at enheden og antallet er tilpasset enhedens decimalpræcision</span><span class="sxs-lookup"><span data-stu-id="14668-128">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit</span></span>

<span data-ttu-id="14668-129">Brug følgende procedure til at gennemse lastlinjerne og foretage justeringer for at sikre, at enheden og antallet er tilpasset enhedens decimalpræcision.</span><span class="sxs-lookup"><span data-stu-id="14668-129">Use the following procedure to review your load lines and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>

1. <span data-ttu-id="14668-130">Gå til **Lokationsstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="14668-130">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="14668-131">Vælg den last, som følgesedlen ikke kan genereres for.</span><span class="sxs-lookup"><span data-stu-id="14668-131">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="14668-132">Vælg lastlinjen for den vare, der forårsager et problem, i oversigtspanelet **Lastlinjer**.</span><span class="sxs-lookup"><span data-stu-id="14668-132">On the **Load lines** FastTab, select the load line for the item that causes an issue.</span></span> <span data-ttu-id="14668-133">Notér værdien for felterne **Antal** og **Enhed**.</span><span class="sxs-lookup"><span data-stu-id="14668-133">Make a note of the value of the **Quantity** and **Unit** fields.</span></span>
1. <span data-ttu-id="14668-134">Gå til **Virksomhedsadministration \> Enheder \> Enheder**.</span><span class="sxs-lookup"><span data-stu-id="14668-134">Go to **Organization administration \> Units \> Units**.</span></span>
1. <span data-ttu-id="14668-135">Vælg den enhed, som følgesedlen ikke kan genereres for.</span><span class="sxs-lookup"><span data-stu-id="14668-135">Select the unit that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="14668-136">Juster værdien i feltet **Decimalpræcision** efter behov.</span><span class="sxs-lookup"><span data-stu-id="14668-136">Adjust the value of the **Decimal precision** field as required.</span></span>
