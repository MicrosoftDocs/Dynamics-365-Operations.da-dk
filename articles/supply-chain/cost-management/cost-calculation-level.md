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
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 1cfbbb6aadbd24a0352776285f6c60ff10f59549
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251020"
---
# <a name="cost-calculation-level"></a><span data-ttu-id="345ba-104">Omkostningsberegningsniveau</span><span class="sxs-lookup"><span data-stu-id="345ba-104">Cost calculation level</span></span>

<span data-ttu-id="345ba-105">Styklisteniveauet, der er navngivet **Omkostningsberegningsniveau** udelukker produktionsordrer og batchordrer fra beregningerne.</span><span class="sxs-lookup"><span data-stu-id="345ba-105">The bill of materials (BOM) level that is named **Cost calculation level** excludes production orders and batch orders from its calculations.</span></span> <span data-ttu-id="345ba-106">Systemet bruger dette niveau, når det kører omkostningsberegninger i efterkalkulationsversioner.</span><span class="sxs-lookup"><span data-stu-id="345ba-106">The system uses this level when it runs cost calculations in costing versions.</span></span> <span data-ttu-id="345ba-107">I processer som genberegning og lagerlukning bruger systemet styklisteniveauet **Efterkalkulationsniveauet** i stedet.</span><span class="sxs-lookup"><span data-stu-id="345ba-107">In processes such as recalculation and inventory close, the system uses the **Costing level** BOM level instead.</span></span>

<span data-ttu-id="345ba-108">I følgende simple scenarie vises forskellene mellem styklisteniveauet **Omkostningsberegningsniveau** og styklisteniveauet **Efterkalkulationsniveau**.</span><span class="sxs-lookup"><span data-stu-id="345ba-108">The following simple scenario shows the differences between the **Cost calculation level** BOM level and the **Costing level** BOM level.</span></span>

<span data-ttu-id="345ba-109">Du har tre produkter: A, B og C. Produkt C er komponent i produkt B, og produkt B er komponent i produkt A.</span><span class="sxs-lookup"><span data-stu-id="345ba-109">You have three products: A, B, and C. Product C is the component of product B, and product B is the component of product A.</span></span>

- <span data-ttu-id="345ba-110">**Efterkalkulationsniveau** tildeler følgende styklisteniveauer:</span><span class="sxs-lookup"><span data-stu-id="345ba-110">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="345ba-111">**Produkt A:** 0</span><span class="sxs-lookup"><span data-stu-id="345ba-111">**Product A:** 0</span></span>
    - <span data-ttu-id="345ba-112">**Produkt B:** 1</span><span class="sxs-lookup"><span data-stu-id="345ba-112">**Product B:** 1</span></span>
    - <span data-ttu-id="345ba-113">**Produkt C:** 2</span><span class="sxs-lookup"><span data-stu-id="345ba-113">**Product C:** 2</span></span>

- <span data-ttu-id="345ba-114">**Omkostningsberegningsniveau** tildeler følgende styklisteniveauer:</span><span class="sxs-lookup"><span data-stu-id="345ba-114">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="345ba-115">**Produkt A:** 0</span><span class="sxs-lookup"><span data-stu-id="345ba-115">**Product A:** 0</span></span>
    - <span data-ttu-id="345ba-116">**Produkt B:** 1</span><span class="sxs-lookup"><span data-stu-id="345ba-116">**Product B:** 1</span></span>
    - <span data-ttu-id="345ba-117">**Produkt C:** 2</span><span class="sxs-lookup"><span data-stu-id="345ba-117">**Product C:** 2</span></span>

<span data-ttu-id="345ba-118">Derefter oprettes der en produktionsordre til produkt C, og produkt A føjes til produktionsordrens stykliste.</span><span class="sxs-lookup"><span data-stu-id="345ba-118">A production order for product C is then created, and product A is added to the production order BOM.</span></span> <span data-ttu-id="345ba-119">Når ordren er forkalkuleret, opdateres styklisteniveauerne på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="345ba-119">After the order is estimated, BOM levels are updated in the following way:</span></span>

- <span data-ttu-id="345ba-120">**Efterkalkulationsniveau** tildeler følgende styklisteniveauer:</span><span class="sxs-lookup"><span data-stu-id="345ba-120">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="345ba-121">**Produkt B:** 1</span><span class="sxs-lookup"><span data-stu-id="345ba-121">**Product B:** 1</span></span>
    - <span data-ttu-id="345ba-122">**Produkt C:** 2</span><span class="sxs-lookup"><span data-stu-id="345ba-122">**Product C:** 2</span></span>
    - <span data-ttu-id="345ba-123">**Produkt A:** 3</span><span class="sxs-lookup"><span data-stu-id="345ba-123">**Product A:** 3</span></span>

- <span data-ttu-id="345ba-124">**Omkostningsberegningsniveau** tildeler følgende styklisteniveauer:</span><span class="sxs-lookup"><span data-stu-id="345ba-124">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="345ba-125">**Produkt A:** 0</span><span class="sxs-lookup"><span data-stu-id="345ba-125">**Product A:** 0</span></span>
    - <span data-ttu-id="345ba-126">**Produkt B:** 1</span><span class="sxs-lookup"><span data-stu-id="345ba-126">**Product B:** 1</span></span>
    - <span data-ttu-id="345ba-127">**Produkt C:** 2</span><span class="sxs-lookup"><span data-stu-id="345ba-127">**Product C:** 2</span></span>

<span data-ttu-id="345ba-128">Denne funktionsmåde sikrer, at ændringer i produktionsordrestyklister ikke påvirker de efterfølgende omkostningsberegninger.</span><span class="sxs-lookup"><span data-stu-id="345ba-128">This behavior ensures that changes to production order BOMs don't affect subsequent cost calculations.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]