---
title: Omkostningsobjekter
description: Denne artikel indeholder oplysninger om omkostningsobjekter og forklarer, hvordan omkostninger og antal akkumuleres. Et omkostningsobjekt er en enhed, hvor omkostninger og antal akkumuleres. En omkostningsobjektenhed kan være et produkt eller produktvarianter som f.eks. varianter af typografier og farver.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c6829f24b8efa29b39f5ed742d8ca99e09bcef01
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910347"
---
# <a name="cost-objects"></a><span data-ttu-id="464ce-105">Omkostningsobjekter</span><span class="sxs-lookup"><span data-stu-id="464ce-105">Cost objects</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="464ce-106">Denne artikel indeholder oplysninger om omkostningsobjekter og forklarer, hvordan omkostninger og antal akkumuleres.</span><span class="sxs-lookup"><span data-stu-id="464ce-106">This article provides information about costs objects, and explains how costs and quantities are accumulated.</span></span> <span data-ttu-id="464ce-107">Et omkostningsobjekt er en enhed, hvor omkostninger og antal akkumuleres.</span><span class="sxs-lookup"><span data-stu-id="464ce-107">A cost object is an entity that costs and quantities are accumulated for.</span></span> <span data-ttu-id="464ce-108">En omkostningsobjektenhed kan være et produkt eller produktvarianter som f.eks. varianter af typografier og farver.</span><span class="sxs-lookup"><span data-stu-id="464ce-108">A cost object entity can be either a product or product variants, such as variants for style and color.</span></span>  

## <a name="cost-objects"></a><span data-ttu-id="464ce-109">Omkostningsobjekter</span><span class="sxs-lookup"><span data-stu-id="464ce-109">Cost objects</span></span>

<span data-ttu-id="464ce-110">Siden **Omkostningsobjekter** viser alle omkostningsobjekter, der er registreret på et produkt.</span><span class="sxs-lookup"><span data-stu-id="464ce-110">The **Cost objects** page lists all cost objects that are registered on a product.</span></span> <span data-ttu-id="464ce-111">Omkostningsobjekter er defineret af data fra følgende kilder:</span><span class="sxs-lookup"><span data-stu-id="464ce-111">The cost objects are defined by data from the following sources:</span></span>

-   <span data-ttu-id="464ce-112">Produkt</span><span class="sxs-lookup"><span data-stu-id="464ce-112">Product</span></span>
-   <span data-ttu-id="464ce-113">Produktdimensionsgruppe</span><span class="sxs-lookup"><span data-stu-id="464ce-113">Product dimension group</span></span>
-   <span data-ttu-id="464ce-114">Lagringsdimensionsgruppe</span><span class="sxs-lookup"><span data-stu-id="464ce-114">Storage dimension group</span></span>
-   <span data-ttu-id="464ce-115">Sporingsdimensionsgruppe</span><span class="sxs-lookup"><span data-stu-id="464ce-115">Tracking dimension group</span></span>

<span data-ttu-id="464ce-116">**Bemærk!** Et omkostningsobjekt repræsenterer kun et omkostningselement af typen **Direkte material**.</span><span class="sxs-lookup"><span data-stu-id="464ce-116">**Note:** A cost object represents a cost element of the **Direct material** type only.</span></span> <span data-ttu-id="464ce-117">Et omkostningsobjekt og et lagerobjekt er forskellige på den måde, at et omkostningsobjekt er defineret af de lagerdimensioner, der er valgt til økonomisk lager.</span><span class="sxs-lookup"><span data-stu-id="464ce-117">A cost object and an inventory object differ in the way that a cost object is defined by the inventory dimensions that are selected for financial inventory.</span></span> <span data-ttu-id="464ce-118">I dette eksempel har en vare følgende konfiguration:</span><span class="sxs-lookup"><span data-stu-id="464ce-118">For example, an item has the following configuration:</span></span>

-   <span data-ttu-id="464ce-119">**Websted:** Fysisk lager = Ja, økonomisk lager = Ja</span><span class="sxs-lookup"><span data-stu-id="464ce-119">**Site:** Physical inventory = Yes, Financial inventory = Yes</span></span>
-   <span data-ttu-id="464ce-120">**Websted:** Fysisk lager = Ja, økonomisk lager = Nej</span><span class="sxs-lookup"><span data-stu-id="464ce-120">**Warehouse:** Physical inventory = Yes, Financial inventory = No</span></span>
-   <span data-ttu-id="464ce-121">**Batch nr.:** Fysisk lager = Ja, økonomisk lager = Nej</span><span class="sxs-lookup"><span data-stu-id="464ce-121">**Batch No.:** Physical inventory = Yes, Financial inventory = No</span></span>

<span data-ttu-id="464ce-122">Tabellen nedenfor viser, hvad der er et omkostningsobjekt, og hvad er et lagerobjekt.</span><span class="sxs-lookup"><span data-stu-id="464ce-122">The following table shows what is a cost object and what is an inventory object.</span></span>

| <span data-ttu-id="464ce-123">Objekttype</span><span class="sxs-lookup"><span data-stu-id="464ce-123">Object type</span></span>      | <span data-ttu-id="464ce-124">Varenummer</span><span class="sxs-lookup"><span data-stu-id="464ce-124">Item number</span></span> | <span data-ttu-id="464ce-125">Lokation</span><span class="sxs-lookup"><span data-stu-id="464ce-125">Site</span></span> | <span data-ttu-id="464ce-126">Lagersted</span><span class="sxs-lookup"><span data-stu-id="464ce-126">Warehouse</span></span> | <span data-ttu-id="464ce-127">Batch nr.</span><span class="sxs-lookup"><span data-stu-id="464ce-127">Batch No.</span></span> |
|------------------|-------------|------|-----------|-----------|
| <span data-ttu-id="464ce-128">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="464ce-128">Cost object</span></span>      | <span data-ttu-id="464ce-129">x</span><span class="sxs-lookup"><span data-stu-id="464ce-129">x</span></span>           | <span data-ttu-id="464ce-130">x</span><span class="sxs-lookup"><span data-stu-id="464ce-130">x</span></span>    |           |           |
| <span data-ttu-id="464ce-131">Lagerobjekt</span><span class="sxs-lookup"><span data-stu-id="464ce-131">Inventory object</span></span> | <span data-ttu-id="464ce-132">x</span><span class="sxs-lookup"><span data-stu-id="464ce-132">x</span></span>           | <span data-ttu-id="464ce-133">x</span><span class="sxs-lookup"><span data-stu-id="464ce-133">x</span></span>    |  <span data-ttu-id="464ce-134">x</span><span class="sxs-lookup"><span data-stu-id="464ce-134">x</span></span>        | <span data-ttu-id="464ce-135">x</span><span class="sxs-lookup"><span data-stu-id="464ce-135">x</span></span>         |

## <a name="accumulation-of-costs-and-quantities"></a><span data-ttu-id="464ce-136">Akkumulering af omkostninger og antal</span><span class="sxs-lookup"><span data-stu-id="464ce-136">Accumulation of costs and quantities</span></span>
-   <span data-ttu-id="464ce-137">Værdien i felterne **Værdi** er en sum af følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="464ce-137">The value in the **Value** fieldis a sum of the following values:</span></span>
    -   <span data-ttu-id="464ce-138">Fysisk kostbeløb</span><span class="sxs-lookup"><span data-stu-id="464ce-138">Physical cost amount</span></span>
    -   <span data-ttu-id="464ce-139">Økonomisk kostbeløb</span><span class="sxs-lookup"><span data-stu-id="464ce-139">Financial cost amount</span></span>
    -   <span data-ttu-id="464ce-140">Reguleringer</span><span class="sxs-lookup"><span data-stu-id="464ce-140">Adjustments</span></span>
-   <span data-ttu-id="464ce-141">Værdien i feltet **Antal** er en sum af følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="464ce-141">The value in the **Quantity** field is a sum of the following values:</span></span>
    -   <span data-ttu-id="464ce-142">Modtaget</span><span class="sxs-lookup"><span data-stu-id="464ce-142">Received</span></span>
    -   <span data-ttu-id="464ce-143">Trukket</span><span class="sxs-lookup"><span data-stu-id="464ce-143">Deducted</span></span>
    -   <span data-ttu-id="464ce-144">Bogført antal</span><span class="sxs-lookup"><span data-stu-id="464ce-144">Posted quantity</span></span>
-   <span data-ttu-id="464ce-145">Feltet **Gennemsnitlig enhedskostpris** er et beregnet felt.</span><span class="sxs-lookup"><span data-stu-id="464ce-145">The **Average unit cost** field is a calculated field.</span></span> <span data-ttu-id="464ce-146">Værdien beregnes ved at dividere værdien **Værdi** med værdien **Antal**.</span><span class="sxs-lookup"><span data-stu-id="464ce-146">The value is calculated by dividing the **Value** value by the **Quantity** value.</span></span>

<span data-ttu-id="464ce-147">**Bemærk!** Parameteren **Medtag fysisk værdi** har ingen effekt på de foregående beregninger.</span><span class="sxs-lookup"><span data-stu-id="464ce-147">**Note:** The \*\*Include physical value \*\*parameter has no effect on the preceding calculations.</span></span>

<a name="additional-resources"></a><span data-ttu-id="464ce-148">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="464ce-148">Additional resources</span></span>
--------

[<span data-ttu-id="464ce-149">Produktdimensionsgruppe</span><span class="sxs-lookup"><span data-stu-id="464ce-149">Product dimension group</span></span>](/dynamicsax-2012/appuser-itpro/about-product-dimensions)

[<span data-ttu-id="464ce-150">Lagringsdimensionsgruppe</span><span class="sxs-lookup"><span data-stu-id="464ce-150">Storage dimension group</span></span>](/dynamicsax-2012//storage-dimension-groups-form)

[<span data-ttu-id="464ce-151">Sporingsdimensionsgruppe</span><span class="sxs-lookup"><span data-stu-id="464ce-151">Tracking dimension group</span></span>](/dynamicsax-2012//tracking-dimension-groups-form)

[<span data-ttu-id="464ce-152">Nyheder eller ændringer</span><span class="sxs-lookup"><span data-stu-id="464ce-152">What's new or changed</span></span>](../../fin-ops-core/fin-ops/get-started/whats-new-changed.md)

[<span data-ttu-id="464ce-153">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="464ce-153">Cost entries</span></span>](cost-entries.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]