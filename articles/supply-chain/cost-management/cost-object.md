---
title: Omkostningsobjekter
description: "Denne artikel indeholder oplysninger om omkostningsobjekter og forklarer, hvordan omkostninger og antal akkumuleres. Et omkostningsobjekt er en enhed, hvor omkostninger og antal akkumuleres. En omkostningsobjektenhed kan være et produkt eller produktvarianter som f.eks. varianter af typografier og farver."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a61761a5c9d98befd67682e1790af5377b7a55e1
ms.openlocfilehash: 13efb284c24c20cf4115ce2dd50be31dd3e5543e
ms.contentlocale: da-dk
ms.lasthandoff: 10/13/2017

---

# <a name="cost-objects"></a><span data-ttu-id="e4a58-105">Omkostningsobjekter</span><span class="sxs-lookup"><span data-stu-id="e4a58-105">Cost objects</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="e4a58-106">Denne artikel indeholder oplysninger om omkostningsobjekter og forklarer, hvordan omkostninger og antal akkumuleres.</span><span class="sxs-lookup"><span data-stu-id="e4a58-106">This article provides information about costs objects, and explains how costs and quantities are accumulated.</span></span> <span data-ttu-id="e4a58-107">Et omkostningsobjekt er en enhed, hvor omkostninger og antal akkumuleres.</span><span class="sxs-lookup"><span data-stu-id="e4a58-107">A cost object is an entity that costs and quantities are accumulated for.</span></span> <span data-ttu-id="e4a58-108">En omkostningsobjektenhed kan være et produkt eller produktvarianter som f.eks. varianter af typografier og farver.</span><span class="sxs-lookup"><span data-stu-id="e4a58-108">A cost object entity can be either a product or product variants, such as variants for style and color.</span></span>  

## <a name="cost-objects"></a><span data-ttu-id="e4a58-109">Omkostningsobjekter</span><span class="sxs-lookup"><span data-stu-id="e4a58-109">Cost objects</span></span>

<span data-ttu-id="e4a58-110">Siden **Omkostningsobjekter** viser alle omkostningsobjekter, der er registreret på et produkt.</span><span class="sxs-lookup"><span data-stu-id="e4a58-110">The **Cost objects** page lists all cost objects that are registered on a product.</span></span> <span data-ttu-id="e4a58-111">Omkostningsobjekter er defineret af data fra følgende kilder:</span><span class="sxs-lookup"><span data-stu-id="e4a58-111">The cost objects are defined by data from the following sources:</span></span>

-   <span data-ttu-id="e4a58-112">Produkt</span><span class="sxs-lookup"><span data-stu-id="e4a58-112">Product</span></span>
-   <span data-ttu-id="e4a58-113">Produktdimensionsgruppe</span><span class="sxs-lookup"><span data-stu-id="e4a58-113">Product dimension group</span></span>
-   <span data-ttu-id="e4a58-114">Lagringsdimensionsgruppe</span><span class="sxs-lookup"><span data-stu-id="e4a58-114">Storage dimension group</span></span>
-   <span data-ttu-id="e4a58-115">Sporingsdimensionsgruppe</span><span class="sxs-lookup"><span data-stu-id="e4a58-115">Tracking dimension group</span></span>

<span data-ttu-id="e4a58-116">**Bemærk!** Et omkostningsobjekt repræsenterer kun et omkostningselement af typen **Direkte material**.</span><span class="sxs-lookup"><span data-stu-id="e4a58-116">**Note:** A cost object represents a cost element of the **Direct material** type only.</span></span> <span data-ttu-id="e4a58-117">Et omkostningsobjekt og et lagerobjekt er forskellige på den måde, at et omkostningsobjekt er defineret af de lagerdimensioner, der er valgt til økonomisk lager.</span><span class="sxs-lookup"><span data-stu-id="e4a58-117">A cost object and an inventory object differ in the way that a cost object is defined by the inventory dimensions that are selected for financial inventory.</span></span> <span data-ttu-id="e4a58-118">I dette eksempel har en vare følgende konfiguration:</span><span class="sxs-lookup"><span data-stu-id="e4a58-118">For example, an item has the following configuration:</span></span>

-   <span data-ttu-id="e4a58-119">**Websted:** Fysisk lager = Ja, økonomisk lager = Ja</span><span class="sxs-lookup"><span data-stu-id="e4a58-119">**Site:** Physical inventory = Yes, Financial inventory = Yes</span></span>
-   <span data-ttu-id="e4a58-120">**Websted:** Fysisk lager = Ja, økonomisk lager = Nej</span><span class="sxs-lookup"><span data-stu-id="e4a58-120">**Warehouse:** Physical inventory = Yes, Financial inventory = No</span></span>
-   <span data-ttu-id="e4a58-121">**Batch nr.:** Fysisk lager = Ja, økonomisk lager = Nej</span><span class="sxs-lookup"><span data-stu-id="e4a58-121">**Batch No.:** Physical inventory = Yes, Financial inventory = No</span></span>

<span data-ttu-id="e4a58-122">Tabellen nedenfor viser, hvad der er et omkostningsobjekt, og hvad er et lagerobjekt.</span><span class="sxs-lookup"><span data-stu-id="e4a58-122">The following table shows what is a cost object and what is an inventory object.</span></span>

| <span data-ttu-id="e4a58-123">Objekttype</span><span class="sxs-lookup"><span data-stu-id="e4a58-123">Object type</span></span>      | <span data-ttu-id="e4a58-124">Varenummer</span><span class="sxs-lookup"><span data-stu-id="e4a58-124">Item number</span></span> | <span data-ttu-id="e4a58-125">Lokation</span><span class="sxs-lookup"><span data-stu-id="e4a58-125">Site</span></span> | <span data-ttu-id="e4a58-126">Lagersted</span><span class="sxs-lookup"><span data-stu-id="e4a58-126">Warehouse</span></span> | <span data-ttu-id="e4a58-127">Batch nr.</span><span class="sxs-lookup"><span data-stu-id="e4a58-127">Batch No.</span></span> |
|------------------|-------------|------|-----------|-----------|
| <span data-ttu-id="e4a58-128">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="e4a58-128">Cost object</span></span>      | <span data-ttu-id="e4a58-129">x</span><span class="sxs-lookup"><span data-stu-id="e4a58-129">x</span></span>           | <span data-ttu-id="e4a58-130">x</span><span class="sxs-lookup"><span data-stu-id="e4a58-130">x</span></span>    |           |           |
| <span data-ttu-id="e4a58-131">Lagerobjekt</span><span class="sxs-lookup"><span data-stu-id="e4a58-131">Inventory object</span></span> | <span data-ttu-id="e4a58-132">x</span><span class="sxs-lookup"><span data-stu-id="e4a58-132">x</span></span>           | <span data-ttu-id="e4a58-133">x</span><span class="sxs-lookup"><span data-stu-id="e4a58-133">x</span></span>    |  <span data-ttu-id="e4a58-134">x</span><span class="sxs-lookup"><span data-stu-id="e4a58-134">x</span></span>        | <span data-ttu-id="e4a58-135">x</span><span class="sxs-lookup"><span data-stu-id="e4a58-135">x</span></span>         |

## <a name="accumulation-of-costs-and-quantities"></a><span data-ttu-id="e4a58-136">Akkumulering af omkostninger og antal</span><span class="sxs-lookup"><span data-stu-id="e4a58-136">Accumulation of costs and quantities</span></span>
-   <span data-ttu-id="e4a58-137">Værdien i felterne **Værdi** er en sum af følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="e4a58-137">The value in the **Value** fieldis a sum of the following values:</span></span>
    -   <span data-ttu-id="e4a58-138">Fysisk kostbeløb</span><span class="sxs-lookup"><span data-stu-id="e4a58-138">Physical cost amount</span></span>
    -   <span data-ttu-id="e4a58-139">Økonomisk kostbeløb</span><span class="sxs-lookup"><span data-stu-id="e4a58-139">Financial cost amount</span></span>
    -   <span data-ttu-id="e4a58-140">Reguleringer</span><span class="sxs-lookup"><span data-stu-id="e4a58-140">Adjustments</span></span>
-   <span data-ttu-id="e4a58-141">Værdien i feltet **Antal** er en sum af følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="e4a58-141">The value in the **Quantity** field is a sum of the following values:</span></span>
    -   <span data-ttu-id="e4a58-142">Modtaget</span><span class="sxs-lookup"><span data-stu-id="e4a58-142">Received</span></span>
    -   <span data-ttu-id="e4a58-143">Trukket</span><span class="sxs-lookup"><span data-stu-id="e4a58-143">Deducted</span></span>
    -   <span data-ttu-id="e4a58-144">Bogført antal</span><span class="sxs-lookup"><span data-stu-id="e4a58-144">Posted quantity</span></span>
-   <span data-ttu-id="e4a58-145">Feltet **Gennemsnitlig enhedskostpris** er et beregnet felt.</span><span class="sxs-lookup"><span data-stu-id="e4a58-145">The **Average unit cost** field is a calculated field.</span></span> <span data-ttu-id="e4a58-146">Værdien beregnes ved at dividere værdien **Værdi** med værdien **Antal**.</span><span class="sxs-lookup"><span data-stu-id="e4a58-146">The value is calculated by dividing the **Value** value by the **Quantity** value.</span></span>

<span data-ttu-id="e4a58-147">**Bemærk!** Parameteren **Medtag fysisk værdi** har ingen effekt på de foregående beregninger.</span><span class="sxs-lookup"><span data-stu-id="e4a58-147">**Note:** The **Include physical value **parameter has no effect on the preceding calculations.</span></span>

<a name="see-also"></a><span data-ttu-id="e4a58-148">Se også</span><span class="sxs-lookup"><span data-stu-id="e4a58-148">See also</span></span>
--------

[<span data-ttu-id="e4a58-149">Produktdimensionsgruppe</span><span class="sxs-lookup"><span data-stu-id="e4a58-149">Product dimension group</span></span>](https://technet.microsoft.com/en-us/library/aa499382.aspx)

[<span data-ttu-id="e4a58-150">Lagringsdimensionsgruppe</span><span class="sxs-lookup"><span data-stu-id="e4a58-150">Storage dimension group</span></span>](https://technet.microsoft.com/en-us/library/hh209317.aspx)

[<span data-ttu-id="e4a58-151">Sporingsdimensionsgruppe</span><span class="sxs-lookup"><span data-stu-id="e4a58-151">Tracking dimension group</span></span>](https://technet.microsoft.com/en-us/library/hh209465.aspx)

[<span data-ttu-id="e4a58-152">Nyheder eller ændringer</span><span class="sxs-lookup"><span data-stu-id="e4a58-152">What's new or changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)

[<span data-ttu-id="e4a58-153">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="e4a58-153">Cost entries</span></span>](cost-entries.md)




