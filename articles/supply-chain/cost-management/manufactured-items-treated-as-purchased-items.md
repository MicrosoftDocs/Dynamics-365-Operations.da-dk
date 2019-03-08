---
title: Konfigurere produkter, som kan være produceret eller indkøbt
description: 'Produkterne kan købes på forskellige måder: De kan produceres (fremstilles) eller fremskaffes (købes). Denne artikel beskriver nogle typiske punkter, du skal overveje, når du konfigurerer produkter til understøttelse af multiforsyning.'
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 21841
ms.assetid: acc608b7-2cad-4fba-afee-9b7cc93761ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a910b5782c8f15cfdd4cf93ea883bc28a5ce8e1a
ms.sourcegitcommit: 2ebea3cbddfa0a5ef0e0fd13d3693da6152bc288
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/30/2019
ms.locfileid: "338446"
---
# <a name="set-up-products-that-can-be-produced-or-procured"></a><span data-ttu-id="c0a77-104">Konfigurere produkter, som kan være produceret eller indkøbt</span><span class="sxs-lookup"><span data-stu-id="c0a77-104">Set up products that can be produced or procured</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c0a77-105">Produkterne kan købes på forskellige måder: De kan produceres (fremstilles) eller fremskaffes (købes).</span><span class="sxs-lookup"><span data-stu-id="c0a77-105">Products can be sourced in various ways -  they can be produced (manufactured) or procured (purchased).</span></span> <span data-ttu-id="c0a77-106">Denne artikel beskriver nogle typiske punkter, du skal overveje, når du konfigurerer produkter til understøttelse af multiforsyning.</span><span class="sxs-lookup"><span data-stu-id="c0a77-106">This article describes some typical points to consider when you configure products to support multi-sourcing.</span></span> 

<span data-ttu-id="c0a77-107">Multiforsyning bruges typisk til en købt vare, der fremstilles fra tid til anden, eller når en vare, der var først og fremmest var en produceret vare, ændres, så den nu primært er en købt vare.</span><span class="sxs-lookup"><span data-stu-id="c0a77-107">Multi-sourcing is typically used for a purchased item that is occasionally manufactured, or when an item that was primarily a manufactured item is changed so that it's now primarily a purchased item.</span></span> <span data-ttu-id="c0a77-108">Varen angives først som en produceret vare, så der kan defineres stykliste- og ruteoplysninger, og for at understøtte produktionsordrer for varen.</span><span class="sxs-lookup"><span data-stu-id="c0a77-108">The item is first designated as a manufactured item, so that bill of materials (BOM) and route information can be defined, and to support production orders for the item.</span></span> <span data-ttu-id="c0a77-109">Produktionstypen skal angives til **Stykliste** (eller til **Formel** eller **Samprodukt** i forbindelse med produktionsprocessen).</span><span class="sxs-lookup"><span data-stu-id="c0a77-109">The production type should be set to **BOM** (or, for process manufacturing, **Formula** or **Co-Product**).</span></span>

<span data-ttu-id="c0a77-110">Når du bruger standardomkostning, kan vareomkostningsposten beregnes for den producerede vare.</span><span class="sxs-lookup"><span data-stu-id="c0a77-110">When you use standard cost, the item cost record can be calculated for the manufactured item.</span></span> <span data-ttu-id="c0a77-111">Men vareomkostningsposten kan måske ikke beregnes for den standardomkostning, du vil bruge ved indkøb.</span><span class="sxs-lookup"><span data-stu-id="c0a77-111">However, the item cost record might not match the standard cost that you want for purchasing purposes.</span></span> <span data-ttu-id="c0a77-112">I dette tilfælde skal standardomkostningen angives og aktiveres manuelt for vareomkostningsposten.</span><span class="sxs-lookup"><span data-stu-id="c0a77-112">In this case, the standard cost must be manually entered and activated for the item cost record.</span></span> <span data-ttu-id="c0a77-113">I forbindelse med omkostningsberegning kan du overveje at bruge en særlig stykliste og rute, der repræsenterer forsyningsblandingen af produktet i løbet af regnskabsperioden, for at minimere afvigelserne over tid.</span><span class="sxs-lookup"><span data-stu-id="c0a77-113">For the cost calculation, consider using a special BOM and route that represent the supply mix of the product over the course of a fiscal period, to minimize the variances over time.</span></span> <span data-ttu-id="c0a77-114">Derudover kan en produceret vare på ét sted overføres til et andet sted.</span><span class="sxs-lookup"><span data-stu-id="c0a77-114">Additionally, a manufactured item at one site can be transferred to another site.</span></span> <span data-ttu-id="c0a77-115">Varens kostpris skal derfor angives manuelt og aktiveres for det sted, som varen overføres til.</span><span class="sxs-lookup"><span data-stu-id="c0a77-115">Therefore, the item's cost must be manually entered and activated for the site that the item is transferred to.</span></span> <span data-ttu-id="c0a77-116">Når du bruger den producerede varen som en komponent i varer på højere niveau, skal komponentens omkostninger behandles som en købt vare.</span><span class="sxs-lookup"><span data-stu-id="c0a77-116">When you use the manufactured item as a component in higher-level products, the component's costs should be treated as a purchased item.</span></span> <span data-ttu-id="c0a77-117">Disse retningslinjer gælder, uanset om komponentens omkostninger er beregnet eller angivet manuelt.</span><span class="sxs-lookup"><span data-stu-id="c0a77-117">This guideline applies, regardless of whether the component’s costs were calculated or manually entered.</span></span> <span data-ttu-id="c0a77-118">Vareomkostningen i styklisteberegningen skal med andre ord behandles som en indkøbt komponent i stedet for at bruge varens stykliste og ruteoplysninger til at beregne omkostninger.</span><span class="sxs-lookup"><span data-stu-id="c0a77-118">In other words, a BOM calculation should treat the item's costs as a purchased component instead of using the item's BOM and route information to calculate costs.</span></span> 

<span data-ttu-id="c0a77-119">Du kan forhindre beregningen i at finde sted ved at angive flaget **Stop udfoldning**, der er indlejret i den styklistekalkulationsgruppe, som er tilknyttet varen.</span><span class="sxs-lookup"><span data-stu-id="c0a77-119">To prevent the calculation from occurring, select the **Stop explosion** flag that is embedded in the BOM calculation group that is assigned to the item.</span></span> <span data-ttu-id="c0a77-120">Du kan forhindre, at der udfoldes behov gennem varen ved behovsplanlægningsberegninger, ved at angive udfoldningshorisonten til 0 (nul) dage i varedisponeringen eller i disponeringsgruppen.</span><span class="sxs-lookup"><span data-stu-id="c0a77-120">To prevent master scheduling calculations from exploding requirements through the item, set the explosion fence to 0 (zero) days in item coverage or in the coverage group.</span></span> <span data-ttu-id="c0a77-121">I behovsplanlægningsberegningen behandles varen derefter som en købt vare, og der udføres ikke yderligere beregninger for varens stykliste- og ruteoplysninger.</span><span class="sxs-lookup"><span data-stu-id="c0a77-121">The master scheduling calculation will then treat the item as a purchased item and won't perform more calculations for the item's BOM and route information.</span></span>





