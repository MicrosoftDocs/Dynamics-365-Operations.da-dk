---
title: Foretage fejlfinding af variantstyring
description: Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med variantstyring.
author: SmithaNataraj
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 77d0c21fbb5a8479ca5e7bdb759c1373b6b255a4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841545"
---
# <a name="troubleshoot-the-product-configurator"></a><span data-ttu-id="a9b72-103">Foretage fejlfinding af variantstyring</span><span class="sxs-lookup"><span data-stu-id="a9b72-103">Troubleshoot the product configurator</span></span>

<span data-ttu-id="a9b72-104">Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med variantstyringen.</span><span class="sxs-lookup"><span data-stu-id="a9b72-104">This topic describes how to fix issues that you might encounter while you work with the product configurator.</span></span>

## <a name="item-text-is-overwritten-when-i-configure-a-product-on-a-sales-order-line"></a><span data-ttu-id="a9b72-105">Varetekst overskrives, når jeg konfigurerer et produkt på en salgsordrelinje.</span><span class="sxs-lookup"><span data-stu-id="a9b72-105">Item text is overwritten when I configure a product on a sales order line.</span></span>

### <a name="issue-description"></a><span data-ttu-id="a9b72-106">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="a9b72-106">Issue description</span></span>

<span data-ttu-id="a9b72-107">Dette problem opstår, når du opretter en salgsordrelinje for en vare, der kan konfigureres, og derefter redigere vareteksten.</span><span class="sxs-lookup"><span data-stu-id="a9b72-107">This issue occurs when you create a sales order line for a configurable item and then modify the item text.</span></span> <span data-ttu-id="a9b72-108">Når du konfigurerer varen og derefter vælger **OK**, overskrives teksten med standardteksten.</span><span class="sxs-lookup"><span data-stu-id="a9b72-108">When you configure the item and then select **OK**, the text is overwritten with the standard text.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="a9b72-109">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="a9b72-109">Issue resolution</span></span>

<span data-ttu-id="a9b72-110">Denne funktionsmåde forventes.</span><span class="sxs-lookup"><span data-stu-id="a9b72-110">This behavior is expected.</span></span> <span data-ttu-id="a9b72-111">Tekstfeltet indeholder variantnavnet, som kun er udfyldt, når du har konfigureret linjen.</span><span class="sxs-lookup"><span data-stu-id="a9b72-111">The text field includes the variant name, which is filled in only after you configure the line.</span></span> <span data-ttu-id="a9b72-112">Derfor skal du ændre teksten, efter at du har konfigureret linjen, og ikke før.</span><span class="sxs-lookup"><span data-stu-id="a9b72-112">Therefore, you must change the text after you've configured the line, not before.</span></span>

## <a name="integer-attributes-are-incorrectly-rounded-when-product-configuration-models-are-calculated"></a><span data-ttu-id="a9b72-113">Heltalsattributter afrundes forkert, når produktkonfigurationsmodeller beregnes.</span><span class="sxs-lookup"><span data-stu-id="a9b72-113">Integer attributes are incorrectly rounded when product configuration models are calculated.</span></span>

### <a name="issue-description"></a><span data-ttu-id="a9b72-114">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="a9b72-114">Issue description</span></span>

<span data-ttu-id="a9b72-115">Dette problem kan opstå, når du udfører følgende serie af handlinger:</span><span class="sxs-lookup"><span data-stu-id="a9b72-115">This issue can occur when you perform the following series of actions:</span></span>

1. <span data-ttu-id="a9b72-116">Konfigurer følgende attributter på en produktionskonfigurationsmodel:</span><span class="sxs-lookup"><span data-stu-id="a9b72-116">Set up the following attributes on a production configuration model:</span></span>

    - <span data-ttu-id="a9b72-117">Input (heltal)</span><span class="sxs-lookup"><span data-stu-id="a9b72-117">Input (integer)</span></span>
    - <span data-ttu-id="a9b72-118">Procent (decimal)</span><span class="sxs-lookup"><span data-stu-id="a9b72-118">Percent (decimal)</span></span>
    - <span data-ttu-id="a9b72-119">Resultat (heltal)</span><span class="sxs-lookup"><span data-stu-id="a9b72-119">Result (integer)</span></span>

2. <span data-ttu-id="a9b72-120">Opret en beregning, der har følgende udtryk:</span><span class="sxs-lookup"><span data-stu-id="a9b72-120">Create a calculation that has the following expression:</span></span>

    <span data-ttu-id="a9b72-121">*Resultat* = *Input* × *Procent* ÷ 100</span><span class="sxs-lookup"><span data-stu-id="a9b72-121">*Result* = *Input* × *Percent* ÷ 100</span></span>

<span data-ttu-id="a9b72-122">I dette tilfælde afrundes heltalsresultatet ikke altid korrekt.</span><span class="sxs-lookup"><span data-stu-id="a9b72-122">In this case, the integer result isn't always correctly rounded.</span></span> <span data-ttu-id="a9b72-123">Input er f.eks. 1.000, og procentsatsen er 2,40.</span><span class="sxs-lookup"><span data-stu-id="a9b72-123">For example, the input is 1,000, and the percentage is 2.40.</span></span> <span data-ttu-id="a9b72-124">Derfor forventer du, at heltalsresultatet er 24, fordi 2,40 procent af 1.000 er 24 (eller 24,00 i decimalform).</span><span class="sxs-lookup"><span data-stu-id="a9b72-124">Therefore, you expect the integer result to be 24, because 2.40 percent of 1,000 is 24 (or 24.00 in decimal form).</span></span> <span data-ttu-id="a9b72-125">Resultatet vises i stedet som 23.</span><span class="sxs-lookup"><span data-stu-id="a9b72-125">Instead, the result is shown as 23.</span></span> <span data-ttu-id="a9b72-126">Men når procentsatsen er 2,39, afrundes beregningen til 24 i stedet for 23.</span><span class="sxs-lookup"><span data-stu-id="a9b72-126">However, when the percentage is 2.39, the calculation is rounded to 24 instead of 23.</span></span> <span data-ttu-id="a9b72-127">Når procentsatsen er 2,50, afrundes beregningen til 25 som forventet.</span><span class="sxs-lookup"><span data-stu-id="a9b72-127">When the percentage is 2.50, the calculation is rounded to 25, as expected.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="a9b72-128">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="a9b72-128">Issue resolution</span></span>

<span data-ttu-id="a9b72-129">Dette problem opstår på grund af den måde, som Microsoft Solver Foundation repræsenterer tal internt på ved at bruge brøker.</span><span class="sxs-lookup"><span data-stu-id="a9b72-129">This issue occurs because of the way that Microsoft Solver Foundation internally represents numbers by using fractions.</span></span> <span data-ttu-id="a9b72-130">I eksemplet ovenfor repræsenteres resultatet af beregningen, hvor procentdelen er 2,40, som 27021597764222975 ÷ 1125899906842624 = 23,99999999999999911182158029987476766109466552734375.</span><span class="sxs-lookup"><span data-stu-id="a9b72-130">For the preceding example, the result of the calculation where the percentage is 2.40 is represented as 27021597764222975 ÷ 1125899906842624 = 23.99999999999999911182158029987476766109466552734375.</span></span> <span data-ttu-id="a9b72-131">Når .NET bruger denne værdi som et heltal, returnerer den 23.</span><span class="sxs-lookup"><span data-stu-id="a9b72-131">When .NET casts this value as an integer, it will return 23.</span></span>

<span data-ttu-id="a9b72-132">Denne funktionsmåde ændres ikke, fordi andre scenarier afhænger af den.</span><span class="sxs-lookup"><span data-stu-id="a9b72-132">This behavior won't be changed, because other scenarios depend on it.</span></span> <span data-ttu-id="a9b72-133">I det foregående eksempel kan du løse problemet ved at indføre en ekstra decimalattribut og en beregning.</span><span class="sxs-lookup"><span data-stu-id="a9b72-133">For the preceding example, you can fix the issue by introducing an additional decimal attribute and a calculation.</span></span>

<span data-ttu-id="a9b72-134">Konfigurer f.eks. følgende attributter på en produktionskonfigurationsmodel:</span><span class="sxs-lookup"><span data-stu-id="a9b72-134">For example, you can set up the following attributes on a production configuration model:</span></span>

- <span data-ttu-id="a9b72-135">Input (heltal)</span><span class="sxs-lookup"><span data-stu-id="a9b72-135">Input (integer)</span></span>
- <span data-ttu-id="a9b72-136">Procent (decimal)</span><span class="sxs-lookup"><span data-stu-id="a9b72-136">Percent (decimal)</span></span>
- <span data-ttu-id="a9b72-137">ResultDecimal (decimal)</span><span class="sxs-lookup"><span data-stu-id="a9b72-137">ResultDecimal (decimal)</span></span>
- <span data-ttu-id="a9b72-138">ResultInteger (heltal)</span><span class="sxs-lookup"><span data-stu-id="a9b72-138">ResultInteger (integer)</span></span>

<span data-ttu-id="a9b72-139">Du kan derefter tilføje følgende beregninger:</span><span class="sxs-lookup"><span data-stu-id="a9b72-139">You can then add the following calculations:</span></span>

- <span data-ttu-id="a9b72-140">*ResultDecimal* = *Input* × *Procent* ÷ 100</span><span class="sxs-lookup"><span data-stu-id="a9b72-140">*ResultDecimal* = *Input* × *Percent* ÷ 100</span></span>
- <span data-ttu-id="a9b72-141">*ResultInteger* = *ResultDecimal*</span><span class="sxs-lookup"><span data-stu-id="a9b72-141">*ResultInteger* = *ResultDecimal*</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]