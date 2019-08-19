---
title: Omkostningsobjekter
description: Denne artikel indeholder oplysninger om omkostningsobjekter og forklarer, hvordan omkostninger og antal akkumuleres. Et omkostningsobjekt er en enhed, hvor omkostninger og antal akkumuleres. En omkostningsobjektenhed kan være et produkt eller produktvarianter som f.eks. varianter af typografier og farver.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6501e8d809d12df421ad081662d23a6b5005f39c
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742130"
---
# <a name="cost-objects"></a><span data-ttu-id="c914b-105">Omkostningsobjekter</span><span class="sxs-lookup"><span data-stu-id="c914b-105">Cost objects</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c914b-106">Denne artikel indeholder oplysninger om omkostningsobjekter og forklarer, hvordan omkostninger og antal akkumuleres.</span><span class="sxs-lookup"><span data-stu-id="c914b-106">This article provides information about costs objects, and explains how costs and quantities are accumulated.</span></span> <span data-ttu-id="c914b-107">Et omkostningsobjekt er en enhed, hvor omkostninger og antal akkumuleres.</span><span class="sxs-lookup"><span data-stu-id="c914b-107">A cost object is an entity that costs and quantities are accumulated for.</span></span> <span data-ttu-id="c914b-108">En omkostningsobjektenhed kan være et produkt eller produktvarianter som f.eks. varianter af typografier og farver.</span><span class="sxs-lookup"><span data-stu-id="c914b-108">A cost object entity can be either a product or product variants, such as variants for style and color.</span></span>  

## <a name="cost-objects"></a><span data-ttu-id="c914b-109">Omkostningsobjekter</span><span class="sxs-lookup"><span data-stu-id="c914b-109">Cost objects</span></span>

<span data-ttu-id="c914b-110">Siden **Omkostningsobjekter** viser alle omkostningsobjekter, der er registreret på et produkt.</span><span class="sxs-lookup"><span data-stu-id="c914b-110">The **Cost objects** page lists all cost objects that are registered on a product.</span></span> <span data-ttu-id="c914b-111">Omkostningsobjekter er defineret af data fra følgende kilder:</span><span class="sxs-lookup"><span data-stu-id="c914b-111">The cost objects are defined by data from the following sources:</span></span>

-   <span data-ttu-id="c914b-112">Produkt</span><span class="sxs-lookup"><span data-stu-id="c914b-112">Product</span></span>
-   <span data-ttu-id="c914b-113">Produktdimensionsgruppe</span><span class="sxs-lookup"><span data-stu-id="c914b-113">Product dimension group</span></span>
-   <span data-ttu-id="c914b-114">Lagringsdimensionsgruppe</span><span class="sxs-lookup"><span data-stu-id="c914b-114">Storage dimension group</span></span>
-   <span data-ttu-id="c914b-115">Sporingsdimensionsgruppe</span><span class="sxs-lookup"><span data-stu-id="c914b-115">Tracking dimension group</span></span>

<span data-ttu-id="c914b-116">**Bemærk!** Et omkostningsobjekt repræsenterer kun et omkostningselement af typen **Direkte material**.</span><span class="sxs-lookup"><span data-stu-id="c914b-116">**Note:** A cost object represents a cost element of the **Direct material** type only.</span></span> <span data-ttu-id="c914b-117">Et omkostningsobjekt og et lagerobjekt er forskellige på den måde, at et omkostningsobjekt er defineret af de lagerdimensioner, der er valgt til økonomisk lager.</span><span class="sxs-lookup"><span data-stu-id="c914b-117">A cost object and an inventory object differ in the way that a cost object is defined by the inventory dimensions that are selected for financial inventory.</span></span> <span data-ttu-id="c914b-118">I dette eksempel har en vare følgende konfiguration:</span><span class="sxs-lookup"><span data-stu-id="c914b-118">For example, an item has the following configuration:</span></span>

-   <span data-ttu-id="c914b-119">**Websted:** Fysisk lager = Ja, økonomisk lager = Ja</span><span class="sxs-lookup"><span data-stu-id="c914b-119">**Site:** Physical inventory = Yes, Financial inventory = Yes</span></span>
-   <span data-ttu-id="c914b-120">**Websted:** Fysisk lager = Ja, økonomisk lager = Nej</span><span class="sxs-lookup"><span data-stu-id="c914b-120">**Warehouse:** Physical inventory = Yes, Financial inventory = No</span></span>
-   <span data-ttu-id="c914b-121">**Batch nr.:** Fysisk lager = Ja, økonomisk lager = Nej</span><span class="sxs-lookup"><span data-stu-id="c914b-121">**Batch No.:** Physical inventory = Yes, Financial inventory = No</span></span>

<span data-ttu-id="c914b-122">Tabellen nedenfor viser, hvad der er et omkostningsobjekt, og hvad er et lagerobjekt.</span><span class="sxs-lookup"><span data-stu-id="c914b-122">The following table shows what is a cost object and what is an inventory object.</span></span>

| <span data-ttu-id="c914b-123">Objekttype</span><span class="sxs-lookup"><span data-stu-id="c914b-123">Object type</span></span>      | <span data-ttu-id="c914b-124">Varenummer</span><span class="sxs-lookup"><span data-stu-id="c914b-124">Item number</span></span> | <span data-ttu-id="c914b-125">Lokation</span><span class="sxs-lookup"><span data-stu-id="c914b-125">Site</span></span> | <span data-ttu-id="c914b-126">Lagersted</span><span class="sxs-lookup"><span data-stu-id="c914b-126">Warehouse</span></span> | <span data-ttu-id="c914b-127">Batch nr.</span><span class="sxs-lookup"><span data-stu-id="c914b-127">Batch No.</span></span> |
|------------------|-------------|------|-----------|-----------|
| <span data-ttu-id="c914b-128">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="c914b-128">Cost object</span></span>      | <span data-ttu-id="c914b-129">x</span><span class="sxs-lookup"><span data-stu-id="c914b-129">x</span></span>           | <span data-ttu-id="c914b-130">x</span><span class="sxs-lookup"><span data-stu-id="c914b-130">x</span></span>    |           |           |
| <span data-ttu-id="c914b-131">Lagerobjekt</span><span class="sxs-lookup"><span data-stu-id="c914b-131">Inventory object</span></span> | <span data-ttu-id="c914b-132">x</span><span class="sxs-lookup"><span data-stu-id="c914b-132">x</span></span>           | <span data-ttu-id="c914b-133">x</span><span class="sxs-lookup"><span data-stu-id="c914b-133">x</span></span>    |  <span data-ttu-id="c914b-134">x</span><span class="sxs-lookup"><span data-stu-id="c914b-134">x</span></span>        | <span data-ttu-id="c914b-135">x</span><span class="sxs-lookup"><span data-stu-id="c914b-135">x</span></span>         |

## <a name="accumulation-of-costs-and-quantities"></a><span data-ttu-id="c914b-136">Akkumulering af omkostninger og antal</span><span class="sxs-lookup"><span data-stu-id="c914b-136">Accumulation of costs and quantities</span></span>
-   <span data-ttu-id="c914b-137">Værdien i felterne **Værdi** er en sum af følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="c914b-137">The value in the **Value** fieldis a sum of the following values:</span></span>
    -   <span data-ttu-id="c914b-138">Fysisk kostbeløb</span><span class="sxs-lookup"><span data-stu-id="c914b-138">Physical cost amount</span></span>
    -   <span data-ttu-id="c914b-139">Økonomisk kostbeløb</span><span class="sxs-lookup"><span data-stu-id="c914b-139">Financial cost amount</span></span>
    -   <span data-ttu-id="c914b-140">Reguleringer</span><span class="sxs-lookup"><span data-stu-id="c914b-140">Adjustments</span></span>
-   <span data-ttu-id="c914b-141">Værdien i feltet **Antal** er en sum af følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="c914b-141">The value in the **Quantity** field is a sum of the following values:</span></span>
    -   <span data-ttu-id="c914b-142">Modtaget</span><span class="sxs-lookup"><span data-stu-id="c914b-142">Received</span></span>
    -   <span data-ttu-id="c914b-143">Trukket</span><span class="sxs-lookup"><span data-stu-id="c914b-143">Deducted</span></span>
    -   <span data-ttu-id="c914b-144">Bogført antal</span><span class="sxs-lookup"><span data-stu-id="c914b-144">Posted quantity</span></span>
-   <span data-ttu-id="c914b-145">Feltet **Gennemsnitlig enhedskostpris** er et beregnet felt.</span><span class="sxs-lookup"><span data-stu-id="c914b-145">The **Average unit cost** field is a calculated field.</span></span> <span data-ttu-id="c914b-146">Værdien beregnes ved at dividere værdien **Værdi** med værdien **Antal**.</span><span class="sxs-lookup"><span data-stu-id="c914b-146">The value is calculated by dividing the **Value** value by the **Quantity** value.</span></span>

<span data-ttu-id="c914b-147">**Bemærk!** Parameteren **Medtag fysisk værdi** har ingen effekt på de foregående beregninger.</span><span class="sxs-lookup"><span data-stu-id="c914b-147">**Note:** The \*\*Include physical value \*\*parameter has no effect on the preceding calculations.</span></span>

<a name="additional-resources"></a><span data-ttu-id="c914b-148">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="c914b-148">Additional resources</span></span>
--------

[<span data-ttu-id="c914b-149">Produktdimensionsgruppe</span><span class="sxs-lookup"><span data-stu-id="c914b-149">Product dimension group</span></span>](https://technet.microsoft.com/library/aa499382.aspx)

[<span data-ttu-id="c914b-150">Lagringsdimensionsgruppe</span><span class="sxs-lookup"><span data-stu-id="c914b-150">Storage dimension group</span></span>](https://technet.microsoft.com/library/hh209317.aspx)

[<span data-ttu-id="c914b-151">Sporingsdimensionsgruppe</span><span class="sxs-lookup"><span data-stu-id="c914b-151">Tracking dimension group</span></span>](https://technet.microsoft.com/library/hh209465.aspx)

[<span data-ttu-id="c914b-152">Nyheder eller ændringer</span><span class="sxs-lookup"><span data-stu-id="c914b-152">What's new or changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)

[<span data-ttu-id="c914b-153">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="c914b-153">Cost entries</span></span>](cost-entries.md)



