---
title: Omkostningsberegningsniveau
description: Dette emne beskriver det styklisteniveau, der er navngivet Omkostningsberegningsniveau. Dette styklisteniveau omfatter ikke produktion og batchordrer fra beregningerne.
author: AndersGirke
manager: tfehr
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 52b77e794ee38add556ac01d62c973b38c48a548
ms.sourcegitcommit: a3cd2783ae120ac6681431c010b9b126a9ca7d94
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/29/2020
ms.locfileid: "3410936"
---
# <a name="cost-calculation-level"></a><span data-ttu-id="b0b38-104">Omkostningsberegningsniveau</span><span class="sxs-lookup"><span data-stu-id="b0b38-104">Cost calculation level</span></span>

<span data-ttu-id="b0b38-105">Styklisteniveauet, der er navngivet **Omkostningsberegningsniveau** udelukker produktionsordrer og batchordrer fra beregningerne.</span><span class="sxs-lookup"><span data-stu-id="b0b38-105">The bill of materials (BOM) level that is named **Cost calculation level** excludes production orders and batch orders from its calculations.</span></span> <span data-ttu-id="b0b38-106">Systemet bruger dette niveau, når det kører omkostningsberegninger i efterkalkulationsversioner.</span><span class="sxs-lookup"><span data-stu-id="b0b38-106">The system uses this level when it runs cost calculations in costing versions.</span></span> <span data-ttu-id="b0b38-107">I processer som genberegning og lagerlukning bruger systemet styklisteniveauet **Efterkalkulationsniveauet** i stedet.</span><span class="sxs-lookup"><span data-stu-id="b0b38-107">In processes such as recalculation and inventory close, the system uses the **Costing level** BOM level instead.</span></span>

<span data-ttu-id="b0b38-108">I følgende simple scenarie vises forskellene mellem styklisteniveauet **Omkostningsberegningsniveau** og styklisteniveauet **Efterkalkulationsniveau**.</span><span class="sxs-lookup"><span data-stu-id="b0b38-108">The following simple scenario shows the differences between the **Cost calculation level** BOM level and the **Costing level** BOM level.</span></span>

<span data-ttu-id="b0b38-109">Du har tre produkter: A, B og C. Produkt C er komponent i produkt B, og produkt B er komponent i produkt A.</span><span class="sxs-lookup"><span data-stu-id="b0b38-109">You have three products: A, B, and C. Product C is the component of product B, and product B is the component of product A.</span></span>

- <span data-ttu-id="b0b38-110">**Efterkalkulationsniveau** tildeler følgende styklisteniveauer:</span><span class="sxs-lookup"><span data-stu-id="b0b38-110">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="b0b38-111">**Produkt A:** 0</span><span class="sxs-lookup"><span data-stu-id="b0b38-111">**Product A:** 0</span></span>
    - <span data-ttu-id="b0b38-112">**Produkt B:** 1</span><span class="sxs-lookup"><span data-stu-id="b0b38-112">**Product B:** 1</span></span>
    - <span data-ttu-id="b0b38-113">**Produkt C:** 2</span><span class="sxs-lookup"><span data-stu-id="b0b38-113">**Product C:** 2</span></span>

- <span data-ttu-id="b0b38-114">**Omkostningsberegningsniveau** tildeler følgende styklisteniveauer:</span><span class="sxs-lookup"><span data-stu-id="b0b38-114">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="b0b38-115">**Produkt A:** 0</span><span class="sxs-lookup"><span data-stu-id="b0b38-115">**Product A:** 0</span></span>
    - <span data-ttu-id="b0b38-116">**Produkt B:** 1</span><span class="sxs-lookup"><span data-stu-id="b0b38-116">**Product B:** 1</span></span>
    - <span data-ttu-id="b0b38-117">**Produkt C:** 2</span><span class="sxs-lookup"><span data-stu-id="b0b38-117">**Product C:** 2</span></span>

<span data-ttu-id="b0b38-118">Derefter oprettes der en produktionsordre til produkt C, og produkt A føjes til produktionsordrens stykliste.</span><span class="sxs-lookup"><span data-stu-id="b0b38-118">A production order for product C is then created, and product A is added to the production order BOM.</span></span> <span data-ttu-id="b0b38-119">Når ordren er forkalkuleret, opdateres styklisteniveauerne på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="b0b38-119">After the order is estimated, BOM levels are updated in the following way:</span></span>

- <span data-ttu-id="b0b38-120">**Efterkalkulationsniveau** tildeler følgende styklisteniveauer:</span><span class="sxs-lookup"><span data-stu-id="b0b38-120">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="b0b38-121">**Produkt B:** 1</span><span class="sxs-lookup"><span data-stu-id="b0b38-121">**Product B:** 1</span></span>
    - <span data-ttu-id="b0b38-122">**Produkt C:** 2</span><span class="sxs-lookup"><span data-stu-id="b0b38-122">**Product C:** 2</span></span>
    - <span data-ttu-id="b0b38-123">**Produkt A:** 3</span><span class="sxs-lookup"><span data-stu-id="b0b38-123">**Product A:** 3</span></span>

- <span data-ttu-id="b0b38-124">**Omkostningsberegningsniveau** tildeler følgende styklisteniveauer:</span><span class="sxs-lookup"><span data-stu-id="b0b38-124">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="b0b38-125">**Produkt A:** 0</span><span class="sxs-lookup"><span data-stu-id="b0b38-125">**Product A:** 0</span></span>
    - <span data-ttu-id="b0b38-126">**Produkt B:** 1</span><span class="sxs-lookup"><span data-stu-id="b0b38-126">**Product B:** 1</span></span>
    - <span data-ttu-id="b0b38-127">**Produkt C:** 2</span><span class="sxs-lookup"><span data-stu-id="b0b38-127">**Product C:** 2</span></span>

<span data-ttu-id="b0b38-128">Denne funktionsmåde sikrer, at ændringer i produktionsordrestyklister ikke påvirker de efterfølgende omkostningsberegninger.</span><span class="sxs-lookup"><span data-stu-id="b0b38-128">This behavior ensures that changes to production order BOMs don't affect subsequent cost calculations.</span></span>