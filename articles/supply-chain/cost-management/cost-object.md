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
ms.openlocfilehash: 275855f2fb4d32df91449d7ebb9ad9ba2bd3f36b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "338423"
---
# <a name="cost-objects"></a><span data-ttu-id="cf237-105">Omkostningsobjekter</span><span class="sxs-lookup"><span data-stu-id="cf237-105">Cost objects</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cf237-106">Denne artikel indeholder oplysninger om omkostningsobjekter og forklarer, hvordan omkostninger og antal akkumuleres.</span><span class="sxs-lookup"><span data-stu-id="cf237-106">This article provides information about costs objects, and explains how costs and quantities are accumulated.</span></span> <span data-ttu-id="cf237-107">Et omkostningsobjekt er en enhed, hvor omkostninger og antal akkumuleres.</span><span class="sxs-lookup"><span data-stu-id="cf237-107">A cost object is an entity that costs and quantities are accumulated for.</span></span> <span data-ttu-id="cf237-108">En omkostningsobjektenhed kan være et produkt eller produktvarianter som f.eks. varianter af typografier og farver.</span><span class="sxs-lookup"><span data-stu-id="cf237-108">A cost object entity can be either a product or product variants, such as variants for style and color.</span></span>  

## <a name="cost-objects"></a><span data-ttu-id="cf237-109">Omkostningsobjekter</span><span class="sxs-lookup"><span data-stu-id="cf237-109">Cost objects</span></span>

<span data-ttu-id="cf237-110">Siden **Omkostningsobjekter** viser alle omkostningsobjekter, der er registreret på et produkt.</span><span class="sxs-lookup"><span data-stu-id="cf237-110">The **Cost objects** page lists all cost objects that are registered on a product.</span></span> <span data-ttu-id="cf237-111">Omkostningsobjekter er defineret af data fra følgende kilder:</span><span class="sxs-lookup"><span data-stu-id="cf237-111">The cost objects are defined by data from the following sources:</span></span>

-   <span data-ttu-id="cf237-112">Produkt</span><span class="sxs-lookup"><span data-stu-id="cf237-112">Product</span></span>
-   <span data-ttu-id="cf237-113">Produktdimensionsgruppe</span><span class="sxs-lookup"><span data-stu-id="cf237-113">Product dimension group</span></span>
-   <span data-ttu-id="cf237-114">Lagringsdimensionsgruppe</span><span class="sxs-lookup"><span data-stu-id="cf237-114">Storage dimension group</span></span>
-   <span data-ttu-id="cf237-115">Sporingsdimensionsgruppe</span><span class="sxs-lookup"><span data-stu-id="cf237-115">Tracking dimension group</span></span>

<span data-ttu-id="cf237-116">**Bemærk!** Et omkostningsobjekt repræsenterer kun et omkostningselement af typen **Direkte material**.</span><span class="sxs-lookup"><span data-stu-id="cf237-116">**Note:** A cost object represents a cost element of the **Direct material** type only.</span></span> <span data-ttu-id="cf237-117">Et omkostningsobjekt og et lagerobjekt er forskellige på den måde, at et omkostningsobjekt er defineret af de lagerdimensioner, der er valgt til økonomisk lager.</span><span class="sxs-lookup"><span data-stu-id="cf237-117">A cost object and an inventory object differ in the way that a cost object is defined by the inventory dimensions that are selected for financial inventory.</span></span> <span data-ttu-id="cf237-118">I dette eksempel har en vare følgende konfiguration:</span><span class="sxs-lookup"><span data-stu-id="cf237-118">For example, an item has the following configuration:</span></span>

-   <span data-ttu-id="cf237-119">**Websted:** Fysisk lager = Ja, økonomisk lager = Ja</span><span class="sxs-lookup"><span data-stu-id="cf237-119">**Site:** Physical inventory = Yes, Financial inventory = Yes</span></span>
-   <span data-ttu-id="cf237-120">**Websted:** Fysisk lager = Ja, økonomisk lager = Nej</span><span class="sxs-lookup"><span data-stu-id="cf237-120">**Warehouse:** Physical inventory = Yes, Financial inventory = No</span></span>
-   <span data-ttu-id="cf237-121">**Batch nr.:** Fysisk lager = Ja, økonomisk lager = Nej</span><span class="sxs-lookup"><span data-stu-id="cf237-121">**Batch No.:** Physical inventory = Yes, Financial inventory = No</span></span>

<span data-ttu-id="cf237-122">Tabellen nedenfor viser, hvad der er et omkostningsobjekt, og hvad er et lagerobjekt.</span><span class="sxs-lookup"><span data-stu-id="cf237-122">The following table shows what is a cost object and what is an inventory object.</span></span>

| <span data-ttu-id="cf237-123">Objekttype</span><span class="sxs-lookup"><span data-stu-id="cf237-123">Object type</span></span>      | <span data-ttu-id="cf237-124">Varenummer</span><span class="sxs-lookup"><span data-stu-id="cf237-124">Item number</span></span> | <span data-ttu-id="cf237-125">Lokation</span><span class="sxs-lookup"><span data-stu-id="cf237-125">Site</span></span> | <span data-ttu-id="cf237-126">Lagersted</span><span class="sxs-lookup"><span data-stu-id="cf237-126">Warehouse</span></span> | <span data-ttu-id="cf237-127">Batch nr.</span><span class="sxs-lookup"><span data-stu-id="cf237-127">Batch No.</span></span> |
|------------------|-------------|------|-----------|-----------|
| <span data-ttu-id="cf237-128">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="cf237-128">Cost object</span></span>      | <span data-ttu-id="cf237-129">x</span><span class="sxs-lookup"><span data-stu-id="cf237-129">x</span></span>           | <span data-ttu-id="cf237-130">x</span><span class="sxs-lookup"><span data-stu-id="cf237-130">x</span></span>    |           |           |
| <span data-ttu-id="cf237-131">Lagerobjekt</span><span class="sxs-lookup"><span data-stu-id="cf237-131">Inventory object</span></span> | <span data-ttu-id="cf237-132">x</span><span class="sxs-lookup"><span data-stu-id="cf237-132">x</span></span>           | <span data-ttu-id="cf237-133">x</span><span class="sxs-lookup"><span data-stu-id="cf237-133">x</span></span>    |  <span data-ttu-id="cf237-134">x</span><span class="sxs-lookup"><span data-stu-id="cf237-134">x</span></span>        | <span data-ttu-id="cf237-135">x</span><span class="sxs-lookup"><span data-stu-id="cf237-135">x</span></span>         |

## <a name="accumulation-of-costs-and-quantities"></a><span data-ttu-id="cf237-136">Akkumulering af omkostninger og antal</span><span class="sxs-lookup"><span data-stu-id="cf237-136">Accumulation of costs and quantities</span></span>
-   <span data-ttu-id="cf237-137">Værdien i felterne **Værdi** er en sum af følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="cf237-137">The value in the **Value** fieldis a sum of the following values:</span></span>
    -   <span data-ttu-id="cf237-138">Fysisk kostbeløb</span><span class="sxs-lookup"><span data-stu-id="cf237-138">Physical cost amount</span></span>
    -   <span data-ttu-id="cf237-139">Økonomisk kostbeløb</span><span class="sxs-lookup"><span data-stu-id="cf237-139">Financial cost amount</span></span>
    -   <span data-ttu-id="cf237-140">Reguleringer</span><span class="sxs-lookup"><span data-stu-id="cf237-140">Adjustments</span></span>
-   <span data-ttu-id="cf237-141">Værdien i feltet **Antal** er en sum af følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="cf237-141">The value in the **Quantity** field is a sum of the following values:</span></span>
    -   <span data-ttu-id="cf237-142">Modtaget</span><span class="sxs-lookup"><span data-stu-id="cf237-142">Received</span></span>
    -   <span data-ttu-id="cf237-143">Trukket</span><span class="sxs-lookup"><span data-stu-id="cf237-143">Deducted</span></span>
    -   <span data-ttu-id="cf237-144">Bogført antal</span><span class="sxs-lookup"><span data-stu-id="cf237-144">Posted quantity</span></span>
-   <span data-ttu-id="cf237-145">Feltet **Gennemsnitlig enhedskostpris** er et beregnet felt.</span><span class="sxs-lookup"><span data-stu-id="cf237-145">The **Average unit cost** field is a calculated field.</span></span> <span data-ttu-id="cf237-146">Værdien beregnes ved at dividere værdien **Værdi** med værdien **Antal**.</span><span class="sxs-lookup"><span data-stu-id="cf237-146">The value is calculated by dividing the **Value** value by the **Quantity** value.</span></span>

<span data-ttu-id="cf237-147">**Bemærk!** Parameteren **Medtag fysisk værdi** har ingen effekt på de foregående beregninger.</span><span class="sxs-lookup"><span data-stu-id="cf237-147">**Note:** The \*\*Include physical value \*\*parameter has no effect on the preceding calculations.</span></span>

<a name="additional-resources"></a><span data-ttu-id="cf237-148">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="cf237-148">Additional resources</span></span>
--------

[<span data-ttu-id="cf237-149">Produktdimensionsgruppe</span><span class="sxs-lookup"><span data-stu-id="cf237-149">Product dimension group</span></span>](https://technet.microsoft.com/en-us/library/aa499382.aspx)

[<span data-ttu-id="cf237-150">Lagringsdimensionsgruppe</span><span class="sxs-lookup"><span data-stu-id="cf237-150">Storage dimension group</span></span>](https://technet.microsoft.com/en-us/library/hh209317.aspx)

[<span data-ttu-id="cf237-151">Sporingsdimensionsgruppe</span><span class="sxs-lookup"><span data-stu-id="cf237-151">Tracking dimension group</span></span>](https://technet.microsoft.com/en-us/library/hh209465.aspx)

[<span data-ttu-id="cf237-152">Nyheder eller ændringer</span><span class="sxs-lookup"><span data-stu-id="cf237-152">What's new or changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)

[<span data-ttu-id="cf237-153">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="cf237-153">Cost entries</span></span>](cost-entries.md)



