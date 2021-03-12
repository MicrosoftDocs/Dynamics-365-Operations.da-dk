---
title: Øjeblikkelig genopfyldning
description: Dette emne beskriver, hvordan du kan bruge øjeblikkelig genopfyldning til genopfyldning af lageret, når en lokationsvejledning ikke kan fordele lageret.
author: Mirzaab
manager: tfehr
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocDirTable, WHSReplenishmentTemplates
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 6e2919c003d1dc67b988345260b2747364752222
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5004771"
---
# <a name="immediate-replenishment"></a><span data-ttu-id="a7e31-103">Øjeblikkelig genopfyldning</span><span class="sxs-lookup"><span data-stu-id="a7e31-103">Immediate replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a7e31-104">Øjeblikkelig genopfyldning gør det muligt at genopfylde lageret, så snart en lokationsvejledning ikke kan fordele lageret.</span><span class="sxs-lookup"><span data-stu-id="a7e31-104">Immediate replenishment lets you replenish inventory immediately after a location directive line fails to allocate inventory.</span></span> <span data-ttu-id="a7e31-105">Genopfyldningen er baseret på en enkelt linje i opsætningen af lokationsvejledningen.</span><span class="sxs-lookup"><span data-stu-id="a7e31-105">The replenishment is based on a single line in the setup of the location directive.</span></span> <span data-ttu-id="a7e31-106">Hvis lageret ikke er disponibelt i den måleenhed, der er angivet af den pågældende linje, udføres der straks genopfyldning med den pågældende måleenhed.</span><span class="sxs-lookup"><span data-stu-id="a7e31-106">If inventory isn't on hand in the unit of measure that is specified by that line, replenishment of that unit of measure occurs immediately.</span></span>

<span data-ttu-id="a7e31-107">Øjeblikkelig genopfyldning er et alternativ til den metode, hvor fordelingen af lager er baseret på flere linjer i lokationsvejledningen, og efterspørgslen opsummeres i slutningen af tildelingen og genopfyldes i den måleenhed, der er angivet i den sidste linje i lokationsvejledningen.</span><span class="sxs-lookup"><span data-stu-id="a7e31-107">Immediate replenishment provides an alternative to the method where the allocation of inventory is based on more lines in the location directive, and where the demand is summed at the end of the allocation and replenished in the unit of measure that is specified by the last line in the location directive.</span></span>

<span data-ttu-id="a7e31-108">Fordelene ved at bruge øjeblikkelig opfyldning er, at genopfyldningen kan begrænses af bestemte enheder, og antallet kan sendes til bestemte lokationer.</span><span class="sxs-lookup"><span data-stu-id="a7e31-108">The benefits of using immediate replenishment are that replenishment can be limited by specific units and the quantity can be directed to specific locations.</span></span>

## <a name="business-scenario"></a><span data-ttu-id="a7e31-109">Forretningsscenarie</span><span class="sxs-lookup"><span data-stu-id="a7e31-109">Business scenario</span></span>

<span data-ttu-id="a7e31-110">Du har f.eks., et lagersted med separate plukområder for "kassen" og "hver" måleenhed.</span><span class="sxs-lookup"><span data-stu-id="a7e31-110">For example, you have a warehouse that has separate picking areas for the "box" and "each" units of measure.</span></span> <span data-ttu-id="a7e31-111">Du vil optimere plukprocessen ved at plukke så mange kasser som muligt og derefter plukke eventuelle restantal, der er mindre end en kasse fra området "hver".</span><span class="sxs-lookup"><span data-stu-id="a7e31-111">You want to optimize the picking process by picking as many boxes as possible and then picking any remaining quantity that is less than a box from the "each" area.</span></span>

<span data-ttu-id="a7e31-112">I så fald kan du bruge øjeblikkelig genopfyldning.</span><span class="sxs-lookup"><span data-stu-id="a7e31-112">In this case, you can use immediate replenishment.</span></span> <span data-ttu-id="a7e31-113">I lokationsvejledningen kan du konfigurere øjeblikkelig genopfyldning for kasser, så genopfyldning efter behov bruges, så snart der er mangel på kasser til plukning af behovsantallet.</span><span class="sxs-lookup"><span data-stu-id="a7e31-113">In the location directive, you can set up immediate replenishment for boxes so that demand replenishment is used as soon as there is a shortage of boxes that can be picked for the demand quantity.</span></span> <span data-ttu-id="a7e31-114">På denne måde kan du optimere plukprocessen, så plukningen omfatter så mange kasser som muligt.</span><span class="sxs-lookup"><span data-stu-id="a7e31-114">In this way, you optimize the picking process so that picking includes as many boxes as possible.</span></span> <span data-ttu-id="a7e31-115">Øjeblikkelig genopfyldning genererer genopfyldning af kasserne, og behovet overføres ikke, så antallet plukkes i måleenheden for "hver".</span><span class="sxs-lookup"><span data-stu-id="a7e31-115">Immediate replenishment will generate replenishment of the boxes, and the demand won't be passed on so that the quantities are picked in the "each" unit of measure.</span></span> <span data-ttu-id="a7e31-116">Med andre ord vil kun de antal, der skal plukkes i måleenheden for "hver" (dvs. antal, der er mindre end en boks), blive plukket fra området "hver".</span><span class="sxs-lookup"><span data-stu-id="a7e31-116">In other words, only the quantities that are supposed to be picked in the "each" unit of measure (that is, quantities that are less than a box) will be picked from the "each" area.</span></span> <span data-ttu-id="a7e31-117">Hvis der opstår mangel i området "kasse", kan du plukke så mange kasser som muligt ud af det samlede behov.</span><span class="sxs-lookup"><span data-stu-id="a7e31-117">If a shortage occurs in the "box" area, you can pick as many boxes as possible out of the total demand.</span></span> <span data-ttu-id="a7e31-118">De resterende antal plukkes derefter fra området "hver".</span><span class="sxs-lookup"><span data-stu-id="a7e31-118">The remaining quantities will then be picked from the "each" area.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="a7e31-119">Hvor det er relevant</span><span class="sxs-lookup"><span data-stu-id="a7e31-119">Where it applies</span></span>

<span data-ttu-id="a7e31-120">Øjeblikkelig genopfyldning anvendes under bølgeudførelse, hvis allokeringen mislykkes for en lokationsvejledningslinje, hvor der er angivet en genopfyldningsskabelon.</span><span class="sxs-lookup"><span data-stu-id="a7e31-120">Immediate replenishment is used during wave execution if allocation fails for a location directive line that a replenishment template is set for.</span></span>

## <a name="set-up-immediate-replenishment"></a><span data-ttu-id="a7e31-121">Konfigurere øjeblikkelig genopfyldning</span><span class="sxs-lookup"><span data-stu-id="a7e31-121">Set up immediate replenishment</span></span>

- <span data-ttu-id="a7e31-122">Gå til **Lokationsstyring** \> **Opsætning** \> **Lokationsvejledning**, og klik derefter på fanen **Linjer** på listen **Skabelon for øjeblikkelig genopfyldning**, og vælg en genopfyldningsskabelon for bølgebehov.</span><span class="sxs-lookup"><span data-stu-id="a7e31-122">Go to **Warehouse management** \> **Setup** \> **Location directives**, and then, on the **Lines** tab, in the **Immediate replenishment template** list, select a replenishment template for wave demand.</span></span>

<span data-ttu-id="a7e31-123">Genopfyldningsskabelonen anvendes, hvis lokationsvejledningslinjen ikke kan tildele en dedikeret måleenhed.</span><span class="sxs-lookup"><span data-stu-id="a7e31-123">The replenishment template is applied if the location directive line fails to allocate a dedicated unit of measure.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="a7e31-124">Fejlfinding</span><span class="sxs-lookup"><span data-stu-id="a7e31-124">Troubleshooting</span></span>

<span data-ttu-id="a7e31-125">Hvis øjeblikkelig genopfyldning er valgt for en lokationsvejledningslinje, men intet genopfyldningsarbejde genereres, når du kan bruger skabeloner for genopfyldning efter behov for den pågældende lokationsvejledningslinje, skal to hovedårsager undersøges:</span><span class="sxs-lookup"><span data-stu-id="a7e31-125">If immediate replenishment is selected for a location directive line, but no replenishment work is generated when you use demand replenishment templates for that location directive line, two main causes must be investigated:</span></span>

- <span data-ttu-id="a7e31-126">Kontroller, at den skabelon for genopfyldning efter behov, der anvendes, er konfigureret til at bruge de rette lokationsskabeloner og arbejdsskabeloner af typen **Genopfyldning**.</span><span class="sxs-lookup"><span data-stu-id="a7e31-126">Make sure that the demand replenishment template that is applied is set up to use the correct location templates and work templates of the **Replenishment** type.</span></span>
- <span data-ttu-id="a7e31-127">Sørg for, at der er tilstrækkelig disponibel lagerbeholdning på de lokationer, hvor skabelonen for genopfyldning efter behov søger efter den disponible lagerbeholdning med henblik på genopfyldning.</span><span class="sxs-lookup"><span data-stu-id="a7e31-127">Make sure that there is enough on-hand inventory at the locations where the demand replenishment template searches for on-hand inventory for replenishment.</span></span>
