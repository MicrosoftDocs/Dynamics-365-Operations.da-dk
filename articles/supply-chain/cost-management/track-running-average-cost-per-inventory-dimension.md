---
title: "Spore løbende gennemsnitskostpris pr. lagerdimension"
description: "Der er tildelt en lagerdimensionsgruppe til de enkelte lagervarer. Den løbende gennemsnitskostpris for en vare beregnes derfor på baggrund af de valgte lagerdimensioner, der spores økonomisk."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventOnhandItem
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, Retail
ms.custom: 75053
ms.assetid: 68cc00f4-0f7a-4a7d-be90-8f2e0d0563d3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: bb2a3a193585944810c5dfac1eb3c019e074008f
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="tracking-running-average-cost-per-inventory-dimension"></a><span data-ttu-id="5333d-104">Spore løbende gennemsnitskostpris pr. lagerdimension</span><span class="sxs-lookup"><span data-stu-id="5333d-104">Tracking running average cost per inventory dimension</span></span>

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


<span data-ttu-id="5333d-105">Der er tildelt en lagerdimensionsgruppe til de enkelte lagervarer.</span><span class="sxs-lookup"><span data-stu-id="5333d-105">An inventory dimension group is attached to every inventory item.</span></span> <span data-ttu-id="5333d-106">Den løbende gennemsnitskostpris for en vare beregnes derfor på baggrund af de valgte lagerdimensioner, der spores økonomisk.</span><span class="sxs-lookup"><span data-stu-id="5333d-106">Therefore, the running average cost price of an item is calculated based on the selected inventory dimensions that are being tracked financially.</span></span>

<span data-ttu-id="5333d-107">Der findes tre typer lagerdimensioner: produkt, lager og sporing.</span><span class="sxs-lookup"><span data-stu-id="5333d-107">There are three types of inventory dimensions: product, storage, and tracking.</span></span> <span data-ttu-id="5333d-108">Produktdimensioner omfatter konfiguration, størrelse og farve.</span><span class="sxs-lookup"><span data-stu-id="5333d-108">Product dimensions include configuration, size, and color.</span></span> <span data-ttu-id="5333d-109">Produktdimensioner spores altid økonomisk.</span><span class="sxs-lookup"><span data-stu-id="5333d-109">Product dimensions are always tracked financially.</span></span> <span data-ttu-id="5333d-110">Lager- og sporingsdimensioner omfatter lokation, lagersted, lokalitet, lagerstatus, nummerplade, batchnummer og serienummer.</span><span class="sxs-lookup"><span data-stu-id="5333d-110">Storage and tracking dimensions include site, warehouse, location, inventory status, license plate, batch number, and serial number.</span></span> <span data-ttu-id="5333d-111">Du kan vælge, hvilke lager- og sporingsdimensioner der skal spores økonomisk.</span><span class="sxs-lookup"><span data-stu-id="5333d-111">You can decide which storage and tracking dimensions are tracked financially.</span></span> 

<span data-ttu-id="5333d-112">**Eksempel 1**</span><span class="sxs-lookup"><span data-stu-id="5333d-112">**Example 1**</span></span> 

<span data-ttu-id="5333d-113">Hvis den lagerdimensionsgruppe, der er knyttet til varen, spores økonomisk af lagerstedet, beregnes den løbende gennemsnitskostpris pr. lagersted.</span><span class="sxs-lookup"><span data-stu-id="5333d-113">If the storage dimension group that is attached to the item is financially tracked by warehouse, the running average cost price is calculated per warehouse.</span></span> <span data-ttu-id="5333d-114">Følgende indkøbsordrer er faktureret:</span><span class="sxs-lookup"><span data-stu-id="5333d-114">The following purchase orders have been invoiced:</span></span>

-   <span data-ttu-id="5333d-115">En indkøbsordre på et antal på 2 til en kostpris af kr. 10,00 er faktureret for lagerstedet GL.</span><span class="sxs-lookup"><span data-stu-id="5333d-115">A purchase order for a quantity of 2 at a cost price of USD 10.00 has been invoiced for warehouse GW.</span></span>
-   <span data-ttu-id="5333d-116">En indkøbsordre på et antal på 3 til en kostpris af kr. 12,00 er faktureret for lagerstedet GL.</span><span class="sxs-lookup"><span data-stu-id="5333d-116">A purchase order for a quantity of 3 at a cost price of USD 12.00 has been invoiced for warehouse GW.</span></span>
-   <span data-ttu-id="5333d-117">En indkøbsordre på et antal på 5 til en kostpris af kr. 15,00 er faktureret for lagerstedet HL.</span><span class="sxs-lookup"><span data-stu-id="5333d-117">A purchase order for a quantity of 5 at a cost price of USD 15.00 has been invoiced for warehouse MW.</span></span>

<span data-ttu-id="5333d-118">Den løbende gennemsnitskostpris for lagerstedet GL er kr. 11,20, og den løbende gennemsnitskostpris for lagerstedet HL er kr. 15,00.</span><span class="sxs-lookup"><span data-stu-id="5333d-118">The running average cost price for warehouse GW is USD 11.20, and the running average cost price for warehouse MW is USD 15.00.</span></span> <span data-ttu-id="5333d-119">En salgsordrefaktura bogføres for lagerstedet GL.</span><span class="sxs-lookup"><span data-stu-id="5333d-119">A sales order invoice is posted for warehouse GW.</span></span> <span data-ttu-id="5333d-120">Værdien af lageret og kostprisen for solgte varer (før der køres lagerlukning og uden afmærkning) er kr. 11,20.</span><span class="sxs-lookup"><span data-stu-id="5333d-120">The value of the inventory and the cost of goods sold (before inventory close is run and without marking) is USD 11.20.</span></span> <span data-ttu-id="5333d-121">En anden salgsordre bogføres for lagerstedet GL.</span><span class="sxs-lookup"><span data-stu-id="5333d-121">Another sales order is posted for warehouse MW.</span></span> <span data-ttu-id="5333d-122">Værdien af lageret og kostprisen for solgte varer (før der køres lagerlukning og uden afmærkning) er kr. 15,00.</span><span class="sxs-lookup"><span data-stu-id="5333d-122">The value of the inventory and the cost of goods sold (before inventory close is run and without marking) is USD 15.00.</span></span> 

<span data-ttu-id="5333d-123">**Eksempel 2** Hvis den lagringsdimensionsgruppe, der er knyttet til varen, spores økonomisk af lagerstedet, og sporingsdimensionsgruppen spores økonomisk af batchnummeret, beregnes den løbende gennemsnitskostpris for de enkelte batches.</span><span class="sxs-lookup"><span data-stu-id="5333d-123">**Example 2** If the storage dimension group that is attached to the item is financially tracked by warehouse, and the tracking dimension group is financially tracked by batch number, the running average cost price is calculated for each batch.</span></span> 

<span data-ttu-id="5333d-124">**Bemærk!** Det anbefales, at du altid ser kostprisen for alle økonomiske dimensioner, der spores.</span><span class="sxs-lookup"><span data-stu-id="5333d-124">**Note:** We recommend that you always view the cost price for all financial dimensions that are being tracked.</span></span> <span data-ttu-id="5333d-125">Følgende indkøbsordrer er faktureret:</span><span class="sxs-lookup"><span data-stu-id="5333d-125">The following purchase orders have been invoiced:</span></span>

-   <span data-ttu-id="5333d-126">En indkøbsordre på et antal på 2 til en kostpris af kr. 10,00 er faktureret for lagerstedet GL og batch AAA.</span><span class="sxs-lookup"><span data-stu-id="5333d-126">A purchase order for a quantity of 2 at a cost price of USD 10.00 has been invoiced for warehouse GW and batch AAA.</span></span>
-   <span data-ttu-id="5333d-127">En indkøbsordre på et antal på 3 til en kostpris af kr. 12,00 er faktureret for lagerstedet GL og batch AAA.</span><span class="sxs-lookup"><span data-stu-id="5333d-127">A purchase order for a quantity of 3 at a cost price of USD 12.00 has been invoiced for warehouse GW and batch AAA.</span></span>
-   <span data-ttu-id="5333d-128">En indkøbsordre på et antal på 2 til en kostpris af kr. 15,00 er faktureret for lagerstedet GL og batch BBB.</span><span class="sxs-lookup"><span data-stu-id="5333d-128">A purchase order for a quantity of 2 at a cost price of USD 15.00 has been invoiced for warehouse GW and batch BBB.</span></span>

<span data-ttu-id="5333d-129">Den løbende gennemsnitskostpris for lagerstedet GL og batch AAA er kr. 11,20, og den løbende gennemsnitskostpris for lagerstedet HL og batch BBB er kr. 15,00.</span><span class="sxs-lookup"><span data-stu-id="5333d-129">The running average cost price for warehouse GW and batch AAA is USD 11.20, and the running average cost price for warehouse GW and batch BBB is USD 15.00.</span></span>




