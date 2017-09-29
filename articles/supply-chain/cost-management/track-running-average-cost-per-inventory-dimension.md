---
title: "Spore løbende gennemsnitskostpris pr. lagerdimension"
description: "Der er tildelt en lagerdimensionsgruppe til de enkelte lagervarer. Den løbende gennemsnitskostpris for en vare beregnes derfor på baggrund af de valgte lagerdimensioner, der spores økonomisk."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventOnhandItem
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 75053
ms.assetid: 68cc00f4-0f7a-4a7d-be90-8f2e0d0563d3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: a88ec380810a9a2d7048d5a8773ebb5960e4cf86
ms.contentlocale: da-dk
ms.lasthandoff: 07/18/2017

---

# <a name="tracking-running-average-cost-per-inventory-dimension"></a><span data-ttu-id="c3d5e-104">Spore løbende gennemsnitskostpris pr. lagerdimension</span><span class="sxs-lookup"><span data-stu-id="c3d5e-104">Tracking running average cost per inventory dimension</span></span>

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


<span data-ttu-id="c3d5e-105">Der er tildelt en lagerdimensionsgruppe til de enkelte lagervarer.</span><span class="sxs-lookup"><span data-stu-id="c3d5e-105">An inventory dimension group is attached to every inventory item.</span></span> <span data-ttu-id="c3d5e-106">Den løbende gennemsnitskostpris for en vare beregnes derfor på baggrund af de valgte lagerdimensioner, der spores økonomisk.</span><span class="sxs-lookup"><span data-stu-id="c3d5e-106">Therefore, the running average cost price of an item is calculated based on the selected inventory dimensions that are being tracked financially.</span></span>

<span data-ttu-id="c3d5e-107">Der findes tre typer lagerdimensioner: produkt, lager og sporing.</span><span class="sxs-lookup"><span data-stu-id="c3d5e-107">There are three types of inventory dimensions: product, storage, and tracking.</span></span> <span data-ttu-id="c3d5e-108">Produktdimensioner omfatter konfiguration, størrelse og farve.</span><span class="sxs-lookup"><span data-stu-id="c3d5e-108">Product dimensions include configuration, size, and color.</span></span> <span data-ttu-id="c3d5e-109">Produktdimensioner spores altid økonomisk.</span><span class="sxs-lookup"><span data-stu-id="c3d5e-109">Product dimensions are always tracked financially.</span></span> <span data-ttu-id="c3d5e-110">Lager- og sporingsdimensioner omfatter lokation, lagersted, lokalitet, lagerstatus, nummerplade, batchnummer og serienummer.</span><span class="sxs-lookup"><span data-stu-id="c3d5e-110">Storage and tracking dimensions include site, warehouse, location, inventory status, license plate, batch number, and serial number.</span></span> <span data-ttu-id="c3d5e-111">Du kan vælge, hvilke lager- og sporingsdimensioner der skal spores økonomisk.</span><span class="sxs-lookup"><span data-stu-id="c3d5e-111">You can decide which storage and tracking dimensions are tracked financially.</span></span> 

<span data-ttu-id="c3d5e-112">**Eksempel 1**</span><span class="sxs-lookup"><span data-stu-id="c3d5e-112">**Example 1**</span></span> 

<span data-ttu-id="c3d5e-113">Hvis den lagerdimensionsgruppe, der er knyttet til varen, spores økonomisk af lagerstedet, beregnes den løbende gennemsnitskostpris pr. lagersted.</span><span class="sxs-lookup"><span data-stu-id="c3d5e-113">If the storage dimension group that is attached to the item is financially tracked by warehouse, the running average cost price is calculated per warehouse.</span></span> <span data-ttu-id="c3d5e-114">Følgende indkøbsordrer er faktureret:</span><span class="sxs-lookup"><span data-stu-id="c3d5e-114">The following purchase orders have been invoiced:</span></span>

-   <span data-ttu-id="c3d5e-115">En indkøbsordre på et antal på 2 til en kostpris af kr. 10,00 er faktureret for lagerstedet GL.</span><span class="sxs-lookup"><span data-stu-id="c3d5e-115">A purchase order for a quantity of 2 at a cost price of USD 10.00 has been invoiced for warehouse GW.</span></span>
-   <span data-ttu-id="c3d5e-116">En indkøbsordre på et antal på 3 til en kostpris af kr. 12,00 er faktureret for lagerstedet GL.</span><span class="sxs-lookup"><span data-stu-id="c3d5e-116">A purchase order for a quantity of 3 at a cost price of USD 12.00 has been invoiced for warehouse GW.</span></span>
-   <span data-ttu-id="c3d5e-117">En indkøbsordre på et antal på 5 til en kostpris af kr. 15,00 er faktureret for lagerstedet HL.</span><span class="sxs-lookup"><span data-stu-id="c3d5e-117">A purchase order for a quantity of 5 at a cost price of USD 15.00 has been invoiced for warehouse MW.</span></span>

<span data-ttu-id="c3d5e-118">Den løbende gennemsnitskostpris for lagerstedet GL er kr. 11,20, og den løbende gennemsnitskostpris for lagerstedet HL er kr. 15,00.</span><span class="sxs-lookup"><span data-stu-id="c3d5e-118">The running average cost price for warehouse GW is USD 11.20, and the running average cost price for warehouse MW is USD 15.00.</span></span> <span data-ttu-id="c3d5e-119">En salgsordrefaktura bogføres for lagerstedet GL.</span><span class="sxs-lookup"><span data-stu-id="c3d5e-119">A sales order invoice is posted for warehouse GW.</span></span> <span data-ttu-id="c3d5e-120">Værdien af lageret og kostprisen for solgte varer (før der køres lagerlukning og uden afmærkning) er kr. 11,20.</span><span class="sxs-lookup"><span data-stu-id="c3d5e-120">The value of the inventory and the cost of goods sold (before inventory close is run and without marking) is USD 11.20.</span></span> <span data-ttu-id="c3d5e-121">En anden salgsordre bogføres for lagerstedet GL.</span><span class="sxs-lookup"><span data-stu-id="c3d5e-121">Another sales order is posted for warehouse MW.</span></span> <span data-ttu-id="c3d5e-122">Værdien af lageret og kostprisen for solgte varer (før der køres lagerlukning og uden afmærkning) er kr. 15,00.</span><span class="sxs-lookup"><span data-stu-id="c3d5e-122">The value of the inventory and the cost of goods sold (before inventory close is run and without marking) is USD 15.00.</span></span> 

<span data-ttu-id="c3d5e-123">**Eksempel 2** Hvis den lagringsdimensionsgruppe, der er knyttet til varen, spores økonomisk af lagerstedet, og sporingsdimensionsgruppen spores økonomisk af batchnummeret, beregnes den løbende gennemsnitskostpris for de enkelte batches.</span><span class="sxs-lookup"><span data-stu-id="c3d5e-123">**Example 2** If the storage dimension group that is attached to the item is financially tracked by warehouse, and the tracking dimension group is financially tracked by batch number, the running average cost price is calculated for each batch.</span></span> 

<span data-ttu-id="c3d5e-124">**Bemærk!** Det anbefales, at du altid ser kostprisen for alle økonomiske dimensioner, der spores.</span><span class="sxs-lookup"><span data-stu-id="c3d5e-124">**Note:** We recommend that you always view the cost price for all financial dimensions that are being tracked.</span></span> <span data-ttu-id="c3d5e-125">Følgende indkøbsordrer er faktureret:</span><span class="sxs-lookup"><span data-stu-id="c3d5e-125">The following purchase orders have been invoiced:</span></span>

-   <span data-ttu-id="c3d5e-126">En indkøbsordre på et antal på 2 til en kostpris af kr. 10,00 er faktureret for lagerstedet GL og batch AAA.</span><span class="sxs-lookup"><span data-stu-id="c3d5e-126">A purchase order for a quantity of 2 at a cost price of USD 10.00 has been invoiced for warehouse GW and batch AAA.</span></span>
-   <span data-ttu-id="c3d5e-127">En indkøbsordre på et antal på 3 til en kostpris af kr. 12,00 er faktureret for lagerstedet GL og batch AAA.</span><span class="sxs-lookup"><span data-stu-id="c3d5e-127">A purchase order for a quantity of 3 at a cost price of USD 12.00 has been invoiced for warehouse GW and batch AAA.</span></span>
-   <span data-ttu-id="c3d5e-128">En indkøbsordre på et antal på 2 til en kostpris af kr. 15,00 er faktureret for lagerstedet GL og batch BBB.</span><span class="sxs-lookup"><span data-stu-id="c3d5e-128">A purchase order for a quantity of 2 at a cost price of USD 15.00 has been invoiced for warehouse GW and batch BBB.</span></span>

<span data-ttu-id="c3d5e-129">Den løbende gennemsnitskostpris for lagerstedet GL og batch AAA er kr. 11,20, og den løbende gennemsnitskostpris for lagerstedet HL og batch BBB er kr. 15,00.</span><span class="sxs-lookup"><span data-stu-id="c3d5e-129">The running average cost price for warehouse GW and batch AAA is USD 11.20, and the running average cost price for warehouse GW and batch BBB is USD 15.00.</span></span>




