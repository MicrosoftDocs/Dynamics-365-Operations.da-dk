---
title: Opdatere standardomkostninger i et produktionsmiljø
description: Denne artikel indeholder vejledning i at opdatere standardomkostninger i et produktionsmiljø.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79663
ms.assetid: 3a7c3d13-8dbc-442d-a281-ac0ebe99ec83
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7bc203176967fbe6c20f4f687fe36fdcf3157b20
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983819"
---
# <a name="update-standard-costs-in-a-manufacturing-environment"></a><span data-ttu-id="c54cd-103">Opdatere standardomkostninger i et produktionsmiljø</span><span class="sxs-lookup"><span data-stu-id="c54cd-103">Update standard costs in a manufacturing environment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c54cd-104">Denne artikel indeholder vejledning i at opdatere standardomkostninger i et produktionsmiljø.</span><span class="sxs-lookup"><span data-stu-id="c54cd-104">This article provides guidance about how to update standard costs in a manufacturing environment.</span></span> 

<span data-ttu-id="c54cd-105">Opdateringer kan afspejle nye varer, omkostningskategorier eller formler til beregning af indirekte omkostninger.</span><span class="sxs-lookup"><span data-stu-id="c54cd-105">Updates can reflect new items, cost categories, or indirect cost calculation formulas.</span></span> <span data-ttu-id="c54cd-106">De kan også afspejle korrektioner og ændrede omkostninger.</span><span class="sxs-lookup"><span data-stu-id="c54cd-106">They can also reflect corrections and cost changes.</span></span> <span data-ttu-id="c54cd-107">Typen af opdatering påvirker, hvilke trin der skal udføres for at opdatere standardomkostninger som vist i følgende tilfælde:</span><span class="sxs-lookup"><span data-stu-id="c54cd-107">The type of update affects the steps that you must complete to update standard costs, as illustrated in the following cases:</span></span>

-   <span data-ttu-id="c54cd-108">Angiv de forventede ændringer af standardomkostninger for købte varer, og ret derefter status for varens omkostningsposter til **Aktiv** på den relevante dato.</span><span class="sxs-lookup"><span data-stu-id="c54cd-108">Enter expected standard cost changes for purchased items, and then change the status of the item cost records to **Active** on the appropriate date.</span></span> <span data-ttu-id="c54cd-109">Du skal dog ikke efterkalkulere omkostningerne for producerede varer, der bruger de købte varer.</span><span class="sxs-lookup"><span data-stu-id="c54cd-109">However, don't recalculate the costs of manufactured items that use the purchased items.</span></span>
-   <span data-ttu-id="c54cd-110">Angiv standardomkostninger for en ny købt vare, men du skal ikke efterkalkulere omkostningerne for producerede varer med en styklisteversion, der indeholder nye købte varer som en komponent.</span><span class="sxs-lookup"><span data-stu-id="c54cd-110">Enter standard costs for a new purchased item, but don't recalculate the costs of manufactured items that have a bill of materials (BOM) version that contains the new purchased item as a component.</span></span>
-   <span data-ttu-id="c54cd-111">Korriger eller rediger omkostningerne for en købt vare, eller rediger den omkostningsgruppe, der er tildelt en købt vare, og beregn derefter omkostningen for alle producerede varer med en styklisteversion, der indeholder den købte vare som en komponent.</span><span class="sxs-lookup"><span data-stu-id="c54cd-111">Correct or change the cost of a purchased item, or change the cost group that is assigned to a purchased item, and calculate the cost for all manufactured items that have a BOM version that contains the purchased item as a component.</span></span>
-   <span data-ttu-id="c54cd-112">Rediger omkostningerne for en omkostningsart, og beregn omkostningerne for alle producerede varer med en ruteversion, der indeholder ruteoperationer, som bruger omkostningsarten.</span><span class="sxs-lookup"><span data-stu-id="c54cd-112">Change the cost for a cost category, and calculate the cost for all manufactured items that have a route version that contains routing operations that use the cost category.</span></span>
-   <span data-ttu-id="c54cd-113">Ret de omkostningskategorier, der er knyttet til ruteoperationer, eller den omkostningsgruppe, der er tildelt omkostningskategorierne.</span><span class="sxs-lookup"><span data-stu-id="c54cd-113">Change the cost categories that are assigned to routing operations or the cost group that is assigned to cost categories.</span></span> <span data-ttu-id="c54cd-114">Beregn derefter omkostningerne for alle producerede varer med en ruteversion, der indeholder ruteoperationer, som bruger omkostningsarten.</span><span class="sxs-lookup"><span data-stu-id="c54cd-114">Then calculate the cost for all manufactured items that have a route version that contains routing operations that use the cost category.</span></span>
-   <span data-ttu-id="c54cd-115">Rediger en beregningsformel for indirekte omkostninger, og beregn omkostningerne for alle producerede varer, der påvirkes af ændringen.</span><span class="sxs-lookup"><span data-stu-id="c54cd-115">Change an indirect cost calculation formula, and calculate the cost for all manufactured items that are affected by the change.</span></span>
-   <span data-ttu-id="c54cd-116">Rediger eller tilføj en produktionslokation for en produceret vare, og beregn varens produktionsomkostninger for lokationen.</span><span class="sxs-lookup"><span data-stu-id="c54cd-116">Change or add a manufacturing site for a manufactured item, and calculate the item's manufactured cost for the site.</span></span>
-   <span data-ttu-id="c54cd-117">Beregn eller genberegn omkostningerne for en produceret vare, og genberegn omkostningerne for alle producerede varer med en styklisteversion, der indeholder den producerede vare som en komponent.</span><span class="sxs-lookup"><span data-stu-id="c54cd-117">Calculate, or recalculate, the cost for a manufactured item, and recalculate the cost for all manufactured items that have a BOM version that contains the manufactured item as a component.</span></span>
-   <span data-ttu-id="c54cd-118">Beregn omkostninger for en ny produceret vare baseret på den definerede, godkendte og aktive stykliste samt ruteoplysninger.</span><span class="sxs-lookup"><span data-stu-id="c54cd-118">Calculate costs for a new manufactured item, based on its defined, approved, and active BOM and route information.</span></span>

<span data-ttu-id="c54cd-119">De kræver alle nøje overvejelser om, hvordan standardomkostningerne skal opdateres.</span><span class="sxs-lookup"><span data-stu-id="c54cd-119">Each case requires careful consideration about how to update standard costs.</span></span>



