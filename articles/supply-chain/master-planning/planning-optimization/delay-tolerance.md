---
title: Forsinkelsestolerance (negative dage)
description: Dette emne indeholder oplysninger om beregning af forsinkelsestolerance, og hvordan det påvirker oprettelsen af ordreforslag i planlægningsoptimering.
author: crytt
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 748e047e89747f2eabccc04a40c79bcb1e6f3dea
ms.sourcegitcommit: f21659f1c23bc2cd65bbe7fb7210910d5a8e1cb9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/24/2021
ms.locfileid: "6306457"
---
# <a name="delay-tolerance-negative-days"></a><span data-ttu-id="0b763-103">Forsinkelsestolerance (negative dage)</span><span class="sxs-lookup"><span data-stu-id="0b763-103">Delay tolerance (negative days)</span></span>

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="0b763-104">Funktionen til forsinkelsestolerance giver planlægningsoptimering mulighed for at overveje den værdi for **Negative dage**, der er angivet for disponeringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="0b763-104">The delay tolerance functionality enables Planning Optimization to consider the **Negative days** value that is set for coverage groups.</span></span> <span data-ttu-id="0b763-105">Den bruges til at forlænge den forsinkelsestoleranceperiode, der anvendes under behovsplanlægning.</span><span class="sxs-lookup"><span data-stu-id="0b763-105">It's used to extend the delay tolerance period that is applied during master planning.</span></span> <span data-ttu-id="0b763-106">På denne måde kan du undgå at oprette nye forsyningsordrer, hvis eksisterende forsyninger kan dække behovet med kort forsinkelse.</span><span class="sxs-lookup"><span data-stu-id="0b763-106">In this way, you can avoid creating new supply orders if existing supply will be able to cover the demand after a short delay.</span></span> <span data-ttu-id="0b763-107">Formålet med funktionen er at bestemme, om det giver mening at oprette en ny forsyningsordre for en given efterspørgsel.</span><span class="sxs-lookup"><span data-stu-id="0b763-107">The purpose of the functionality is to determine whether it makes sense to create a new supply order for a given demand.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="0b763-108">Aktivere funktionen i systemet</span><span class="sxs-lookup"><span data-stu-id="0b763-108">Turn on the feature in your system</span></span>

<span data-ttu-id="0b763-109">Du kan gøre funktionen til forsinkelsestolerance tilgængelig i systemet ved at gå til [Funktionsstyring](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og aktivere funktionen *Negative dage for Planlægningsoptimering*.</span><span class="sxs-lookup"><span data-stu-id="0b763-109">To make the delay tolerance functionality available in your system, go to [Feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Negative days for Planning Optimization* feature.</span></span>

## <a name="delay-tolerance-in-planning-optimization"></a><span data-ttu-id="0b763-110">Forsinkelsestolerance i planlægningsoptimering</span><span class="sxs-lookup"><span data-stu-id="0b763-110">Delay tolerance in Planning Optimization</span></span>

<span data-ttu-id="0b763-111">Forsinkelsestolerance er det antal dage efter leveringstiden, du er villig til at vente, før du bestiller ny genopfyldning, når der allerede er planlagt en eksisterende forsyning.</span><span class="sxs-lookup"><span data-stu-id="0b763-111">Delay tolerance represents the number of days beyond the lead time that you're willing to wait before you order new replenishment when existing supply is already planned.</span></span> <span data-ttu-id="0b763-112">Forsinkelsestolerance defineres ved hjælp af kalenderdage og ikke arbejdsdage.</span><span class="sxs-lookup"><span data-stu-id="0b763-112">Delay tolerance is defined by using calendar days, not business days.</span></span>

<span data-ttu-id="0b763-113">Når systemet beregner forsinkelsestolerancen, tages indstillingen af **Negative dage** med i beregningen på tidspunktet for behovsplanlægning.</span><span class="sxs-lookup"><span data-stu-id="0b763-113">At the time of master planning, when the system calculates the delay tolerance, it considers the **Negative days** setting.</span></span> <span data-ttu-id="0b763-114">Du kan enten angive værdien for **Negative dage** på siden **Disponeringsgrupper** eller på siden **Varedisponering**.</span><span class="sxs-lookup"><span data-stu-id="0b763-114">You can set the **Negative days** value on either the **Coverage groups** page or the **Item coverage** page.</span></span>

<span data-ttu-id="0b763-115">Systemet knytter beregningen af forsinkelsestolerancen til den *tidligste genopfyldningsdato*, hvilket er lig med dags dato plus gennemløbstiden.</span><span class="sxs-lookup"><span data-stu-id="0b763-115">The system links the delay tolerance calculation to the *earliest replenishment date*, which equals today's date plus the lead time.</span></span> <span data-ttu-id="0b763-116">Forsinkelsestolerancen beregnes ved at bruge følgende formel, hvor *max()* finder den største af to værdier:</span><span class="sxs-lookup"><span data-stu-id="0b763-116">The delay tolerance is calculated by using following formula, where *max()* finds the larger of two values:</span></span>

<span data-ttu-id="0b763-117">*max(Tidligste genopfyldningsdato, Forfaldsdato for efterspørgsel)* – *Forfaldsdato for efterspørgsel* + *Negative dage*</span><span class="sxs-lookup"><span data-stu-id="0b763-117">*max(Earliest replenishment date, Demand due date)* – *Demand due date* + *Negative days*</span></span>

<span data-ttu-id="0b763-118">Denne formel sikrer, at varedisponering ikke opretter nye leveringsordrer, når den eksisterende forsyning er tilstrækkelig under produktets gennemløbstid.</span><span class="sxs-lookup"><span data-stu-id="0b763-118">This formula ensures that master planning doesn't create new supply orders when enough supply exists during the product lead time.</span></span>

> [!NOTE]
> <span data-ttu-id="0b763-119">Beregningen af forsinkelsestolerance i Planlægningsoptimering bruger altid beregningen af dynamiske negative dage fra en indbygget behovsplanlægning.</span><span class="sxs-lookup"><span data-stu-id="0b763-119">The delay tolerance calculation in Planning Optimization always uses the dynamic negative days calculation from built-in master planning.</span></span> <span data-ttu-id="0b763-120">Indstillingen **Brug dynamiske negative dage** på siden **Parametre for behovsplanlægning** har ingen indflydelse på denne funktionsmåde.</span><span class="sxs-lookup"><span data-stu-id="0b763-120">The **Use dynamic negative days** setting on the **Master planning parameters** page has no effect on this behavior.</span></span>

<span data-ttu-id="0b763-121">Hvis den eksisterende forsyning medfører en forsinkelse i efterspørgsel, der er mindre end eller lig med den beregnede forsinkelsestolerance, udligner Planlægningsoptimering den eksisterende forsyning med efterspørgslen.</span><span class="sxs-lookup"><span data-stu-id="0b763-121">If the existing supply implies a demand delay that is less than or equal to the calculated delay tolerance, Planning Optimization pegs existing supply with the demand.</span></span> <span data-ttu-id="0b763-122">I nogle tilfælde er det bedre at udskyde behovet end at ende med for stor forsyning.</span><span class="sxs-lookup"><span data-stu-id="0b763-122">In some cases, it's better to delay the demand than to end up with oversupply.</span></span>

<span data-ttu-id="0b763-123">Følgende undersektioner indeholder eksempler på, hvordan forsinkelsestolerance påvirker oprettelsen af ordreforslag i Planlægningsoptimering.</span><span class="sxs-lookup"><span data-stu-id="0b763-123">The following subsections provide examples that show how delay tolerance affects the creation of planned orders in Planning Optimization.</span></span>

### <a name="example-1"></a><span data-ttu-id="0b763-124">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="0b763-124">Example 1</span></span>

<span data-ttu-id="0b763-125">Et produkt har følgende konfiguration:</span><span class="sxs-lookup"><span data-stu-id="0b763-125">A product has the following configuration:</span></span>

- <span data-ttu-id="0b763-126">**Leveringstid:** *10*</span><span class="sxs-lookup"><span data-stu-id="0b763-126">**Lead time:** *10*</span></span>
- <span data-ttu-id="0b763-127">**Negative dage:** *2*</span><span class="sxs-lookup"><span data-stu-id="0b763-127">**Negative days:** *2*</span></span>

<span data-ttu-id="0b763-128">Der findes følgende udbud og efterspørgsel for produktet:</span><span class="sxs-lookup"><span data-stu-id="0b763-128">The following supply and demand exist for the product:</span></span>

- <span data-ttu-id="0b763-129">**Efterspørgsel for i dag**: En salgsordre på et antal på 10</span><span class="sxs-lookup"><span data-stu-id="0b763-129">**Demand for today:** A sales order for a quantity of 10</span></span>
- <span data-ttu-id="0b763-130">**Forsyning om 12 dage:** En indkøbsordre på et antal på 10</span><span class="sxs-lookup"><span data-stu-id="0b763-130">**Supply in 12 days:** A purchase order for a quantity of 10</span></span>

<span data-ttu-id="0b763-131">Eksisterende forsyning kan dække behovet inden for 12 dage, og denne periode er lig med forsinkelsestolerancen.</span><span class="sxs-lookup"><span data-stu-id="0b763-131">Existing supply can cover the demand within 12 days, and that period equals the delay tolerance.</span></span> <span data-ttu-id="0b763-132">Når behovsplanlægningen køres, oprettes der derfor ikke ordreforslag.</span><span class="sxs-lookup"><span data-stu-id="0b763-132">Therefore, when master planning runs, no planned orders are created.</span></span>

### <a name="example-2"></a><span data-ttu-id="0b763-133">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="0b763-133">Example 2</span></span>

<span data-ttu-id="0b763-134">Et produkt har følgende konfiguration:</span><span class="sxs-lookup"><span data-stu-id="0b763-134">A product has the following configuration:</span></span>

- <span data-ttu-id="0b763-135">**Leveringstid:** *10*</span><span class="sxs-lookup"><span data-stu-id="0b763-135">**Lead time:** *10*</span></span>
- <span data-ttu-id="0b763-136">**Negative dage:** *0*</span><span class="sxs-lookup"><span data-stu-id="0b763-136">**Negative days:** *0*</span></span>

<span data-ttu-id="0b763-137">Der findes følgende udbud og efterspørgsel for produktet:</span><span class="sxs-lookup"><span data-stu-id="0b763-137">The following supply and demand exist for the product:</span></span>

- <span data-ttu-id="0b763-138">**Efterspørgsel for i dag**: En salgsordre på et antal på 10</span><span class="sxs-lookup"><span data-stu-id="0b763-138">**Demand for today:** A sales order for a quantity of 10</span></span>
- <span data-ttu-id="0b763-139">**Forsyning om 12 dage:** En indkøbsordre på et antal på 10</span><span class="sxs-lookup"><span data-stu-id="0b763-139">**Supply in 12 days:** A purchase order for a quantity of 10</span></span>

<span data-ttu-id="0b763-140">Eksisterende forsyning kan først dække behovet efter 12 dage.</span><span class="sxs-lookup"><span data-stu-id="0b763-140">Existing supply can cover the demand only after 12 days.</span></span> <span data-ttu-id="0b763-141">Men forsinkelsestolerancen er 10 dage.</span><span class="sxs-lookup"><span data-stu-id="0b763-141">However, the delay tolerance is 10 days.</span></span> <span data-ttu-id="0b763-142">Når varedisponering køres, oprettes der derfor et ordreforslag på 10.</span><span class="sxs-lookup"><span data-stu-id="0b763-142">Therefore, when master planning runs, a planned order for a quantity of 10 is created.</span></span>

### <a name="example-3"></a><span data-ttu-id="0b763-143">Eksempel 3</span><span class="sxs-lookup"><span data-stu-id="0b763-143">Example 3</span></span>

<span data-ttu-id="0b763-144">Et produkt har følgende konfiguration:</span><span class="sxs-lookup"><span data-stu-id="0b763-144">A product has the following configuration:</span></span>

- <span data-ttu-id="0b763-145">**Leveringstid:** *10*</span><span class="sxs-lookup"><span data-stu-id="0b763-145">**Lead time:** *10*</span></span>
- <span data-ttu-id="0b763-146">**Negative dage:** *2*</span><span class="sxs-lookup"><span data-stu-id="0b763-146">**Negative days:** *2*</span></span>

<span data-ttu-id="0b763-147">Der findes følgende udbud og efterspørgsel for produktet:</span><span class="sxs-lookup"><span data-stu-id="0b763-147">The following supply and demand exist for the product:</span></span>

- <span data-ttu-id="0b763-148">**Efterspørgsel om 11 dage**: En salgsordre på et antal på 10</span><span class="sxs-lookup"><span data-stu-id="0b763-148">**Demand in 11 days:** A sales order for a quantity of 10</span></span>
- <span data-ttu-id="0b763-149">**Forsyning om 14 dage:** En indkøbsordre på et antal på 10</span><span class="sxs-lookup"><span data-stu-id="0b763-149">**Supply in 14 days:** A purchase order for a quantity of 10</span></span>

<span data-ttu-id="0b763-150">Eksisterende forsyning kan først dække behovet efter tre dage.</span><span class="sxs-lookup"><span data-stu-id="0b763-150">Existing supply can cover the demand only after three days.</span></span> <span data-ttu-id="0b763-151">Men forsinkelsestolerancen er to dage.</span><span class="sxs-lookup"><span data-stu-id="0b763-151">However, the delay tolerance is two days.</span></span> <span data-ttu-id="0b763-152">I dette tilfælde omfatter forsinkelsestolerancen kun de to negative dage.</span><span class="sxs-lookup"><span data-stu-id="0b763-152">(In this case, the delay tolerance includes only the two negative days.</span></span> <span data-ttu-id="0b763-153">Efterspørgselsdatoen medtages ikke, fordi den ligger efter produktets leveringstid. Når varedisponering køres, oprettes der derfor et ordreforslag på 10.</span><span class="sxs-lookup"><span data-stu-id="0b763-153">The demand date isn't included because it's after the product lead time.) Therefore, when master planning runs, a planned order for a quantity of 10 is created.</span></span>
