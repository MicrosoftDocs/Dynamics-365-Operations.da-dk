---
title: Udfoldning af styklisteversion
description: I denne artikel beskrives en varedisponeringssituation, der involverer udfoldning af en styklisteversion.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 482c036294f525be5db1dc6efefe76a9ba5b3ce5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424865"
---
# <a name="explosion-of-a-bom-version"></a><span data-ttu-id="b66fa-103">Udfoldning af styklisteversion</span><span class="sxs-lookup"><span data-stu-id="b66fa-103">Explosion of a BOM version</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b66fa-104">I denne artikel beskrives en varedisponeringssituation, der involverer udfoldning af en styklisteversion.</span><span class="sxs-lookup"><span data-stu-id="b66fa-104">This article explains a master planning scenario that involves explosion of a bill of materials (BOM) version.</span></span>

<span data-ttu-id="b66fa-105">En efterspørgselsudfoldning af en styklisteversion opretter en efterspørgsel efter de enkelte varer på styklistelinjen på en bestemt lokation og muligvis på et bestemt lagersted.</span><span class="sxs-lookup"><span data-stu-id="b66fa-105">A demand explosion of a bill of materials (BOM) version creates a demand for each BOM line item at a specific site and, possibly, at a specific warehouse.</span></span> <span data-ttu-id="b66fa-106">På en lokationsspecifik stykliste kan der defineres et bestemt lagersted defineret for de enkelte styklistelinjer.</span><span class="sxs-lookup"><span data-stu-id="b66fa-106">In a site-specific BOM, a specific warehouse can be defined for each BOM line.</span></span> <span data-ttu-id="b66fa-107">Og for de enkelte styklistelinjer bestemmer varens dimensionsindstillinger, om lagerstedet er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="b66fa-107">Additionally, for each BOM line, the item's dimension settings determine whether the warehouse is required.</span></span> <span data-ttu-id="b66fa-108">Den resulterende efterspørgsel for de enkelte styklistelinjer bliver derefter startpunktet for en ekstra efterspørgselsudfoldning.</span><span class="sxs-lookup"><span data-stu-id="b66fa-108">The resulting demand for each BOM line item then becomes the starting point for additional demand explosion.</span></span> <span data-ttu-id="b66fa-109">Dette behovsplanlægningsscenario omfatter følgende forhold:</span><span class="sxs-lookup"><span data-stu-id="b66fa-109">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="b66fa-110">Lokationsdimensionen er obligatorisk og skal angives ved posteringen.</span><span class="sxs-lookup"><span data-stu-id="b66fa-110">The site dimension is mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="b66fa-111">Lokationsdimensionen er konsistent.</span><span class="sxs-lookup"><span data-stu-id="b66fa-111">The site dimension is consistent.</span></span> <span data-ttu-id="b66fa-112">Lokationen for efterspørgsel på lavere niveau er derfor den samme som lokationen for posteringen af den indledende efterspørgsel.</span><span class="sxs-lookup"><span data-stu-id="b66fa-112">Therefore, the site for lower-level demand is the same as the site on the initial demand transaction.</span></span>

<span data-ttu-id="b66fa-113">I følgende grafik vises, hvordan efterspørgselsudfoldningen for behovsplanlægning forløber.</span><span class="sxs-lookup"><span data-stu-id="b66fa-113">The following illustration shows how the process for master planning demand explosion.</span></span> ![Efterspørgselsudfoldning med styklisteversion](./media/multisitedemandexplosionscenariousingbomversion.gif)

<a name="additional-resources"></a><span data-ttu-id="b66fa-115">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="b66fa-115">Additional resources</span></span>
--------

[<span data-ttu-id="b66fa-116">Bestemme styklisteversionen</span><span class="sxs-lookup"><span data-stu-id="b66fa-116">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)

[<span data-ttu-id="b66fa-117">Oversigt over varedisponering og funktionen til flere lokationer</span><span class="sxs-lookup"><span data-stu-id="b66fa-117">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)



