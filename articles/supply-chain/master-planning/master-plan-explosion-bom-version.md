---
title: Udfoldning af styklisteversion
description: I denne artikel beskrives en varedisponeringssituation, der involverer udfoldning af en styklisteversion.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f8c633e09103c45aff5614270a94a3bfe4fc5e20
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="explosion-of-a-bom-version"></a><span data-ttu-id="6ce8b-103">Udfoldning af styklisteversion</span><span class="sxs-lookup"><span data-stu-id="6ce8b-103">Explosion of a BOM version</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="6ce8b-104">I denne artikel beskrives en varedisponeringssituation, der involverer udfoldning af en styklisteversion.</span><span class="sxs-lookup"><span data-stu-id="6ce8b-104">This article explains a master planning scenario that involves explosion of a bill of materials (BOM) version.</span></span>

<span data-ttu-id="6ce8b-105">En efterspørgselsudfoldning af en styklisteversion opretter en efterspørgsel efter de enkelte varer på styklistelinjen på en bestemt lokation og muligvis på et bestemt lagersted.</span><span class="sxs-lookup"><span data-stu-id="6ce8b-105">A demand explosion of a bill of materials (BOM) version creates a demand for each BOM line item at a specific site and, possibly, at a specific warehouse.</span></span> <span data-ttu-id="6ce8b-106">På en lokationsspecifik stykliste kan der defineres et bestemt lagersted defineret for de enkelte styklistelinjer.</span><span class="sxs-lookup"><span data-stu-id="6ce8b-106">In a site-specific BOM, a specific warehouse can be defined for each BOM line.</span></span> <span data-ttu-id="6ce8b-107">Og for de enkelte styklistelinjer bestemmer varens dimensionsindstillinger, om lagerstedet er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="6ce8b-107">Additionally, for each BOM line, the item's dimension settings determine whether the warehouse is required.</span></span> <span data-ttu-id="6ce8b-108">Den resulterende efterspørgsel for de enkelte styklistelinjer bliver derefter startpunktet for en ekstra efterspørgselsudfoldning.</span><span class="sxs-lookup"><span data-stu-id="6ce8b-108">The resulting demand for each BOM line item then becomes the starting point for additional demand explosion.</span></span> <span data-ttu-id="6ce8b-109">Dette behovsplanlægningsscenario omfatter følgende forhold:</span><span class="sxs-lookup"><span data-stu-id="6ce8b-109">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="6ce8b-110">Lokationsdimensionen er obligatorisk og skal angives ved posteringen.</span><span class="sxs-lookup"><span data-stu-id="6ce8b-110">The site dimension is mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="6ce8b-111">Lokationsdimensionen er konsistent.</span><span class="sxs-lookup"><span data-stu-id="6ce8b-111">The site dimension is consistent.</span></span> <span data-ttu-id="6ce8b-112">Lokationen for efterspørgsel på lavere niveau er derfor den samme som lokationen for posteringen af den indledende efterspørgsel.</span><span class="sxs-lookup"><span data-stu-id="6ce8b-112">Therefore, the site for lower-level demand is the same as the site on the initial demand transaction.</span></span>

<span data-ttu-id="6ce8b-113">I følgende grafik vises, hvordan efterspørgselsudfoldningen for behovsplanlægning forløber.</span><span class="sxs-lookup"><span data-stu-id="6ce8b-113">The following illustration shows how the process for master planning demand explosion.</span></span> ![Efterspørgselsudfoldning med styklisteversion](./media/multisitedemandexplosionscenariousingbomversion.gif)

<a name="see-also"></a><span data-ttu-id="6ce8b-115">Se også</span><span class="sxs-lookup"><span data-stu-id="6ce8b-115">See also</span></span>
--------

[<span data-ttu-id="6ce8b-116">Varedisponering – Sådan bestemmes styklisteversionen</span><span class="sxs-lookup"><span data-stu-id="6ce8b-116">Master planning - how the BOM version is determined</span></span>](master-plan-bom-version-determined.md)

[<span data-ttu-id="6ce8b-117">Varedisponering og funktionen til flere lokationer</span><span class="sxs-lookup"><span data-stu-id="6ce8b-117">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)




