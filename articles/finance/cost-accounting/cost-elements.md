---
title: Dimensioner for omkostningselement
description: Som et af de centrale elementer i omkostningsregnskabet bruges omkostningselementdimensioner til at kategorisere og spore, hvor omkostningerne flyder til.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 223204
ms.assetid: 1eda0e62-760b-4737-9dfd-3c3c38d80c1a
ms.search.region: global
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 037d4971fe0a5a9d08f0ed20d2482b8feb9aa4f2
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176985"
---
# <a name="cost-element-dimensions"></a><span data-ttu-id="8f129-103">Dimensioner for omkostningselement</span><span class="sxs-lookup"><span data-stu-id="8f129-103">Cost element dimensions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8f129-104">Som et af de centrale elementer i omkostningsregnskabet bruges omkostningselementdimensioner til at kategorisere og spore, hvor omkostningerne flyder til.</span><span class="sxs-lookup"><span data-stu-id="8f129-104">As one of the core pillars in Cost accounting, cost element dimensions are used to categorize and track where costs flow to.</span></span> 

<span data-ttu-id="8f129-105">Et omkostningselement svarer til et omkostningsrelevant element i kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="8f129-105">A cost element corresponds to a cost-relevant item in the chart of accounts.</span></span> <span data-ttu-id="8f129-106">Grundlæggende kan det være en hvilken som helst type af element på det laveste niveau i en virksomhed, hvor omkostningerne kan flyde til.</span><span class="sxs-lookup"><span data-stu-id="8f129-106">Basically, it can be any type of element at the lowest level in a business where costs can flow to.</span></span> <span data-ttu-id="8f129-107">Omkostningselementer som et koncept går fra finanskonti til alle omkostningsrelevante ressourcer.</span><span class="sxs-lookup"><span data-stu-id="8f129-107">Cost elements as a concept range from ledger accounts to all cost-relevant resources.</span></span> <span data-ttu-id="8f129-108">I øjeblikket understøtter omkostningsregnskab finanskonti.</span><span class="sxs-lookup"><span data-stu-id="8f129-108">Currently, Cost accounting supports ledger accounts.</span></span>

## <a name="two-types-of-cost-elements"></a><span data-ttu-id="8f129-109">To typer omkostningselementer</span><span class="sxs-lookup"><span data-stu-id="8f129-109">Two types of cost elements</span></span>
<span data-ttu-id="8f129-110">Der findes to typer omkostningselementer: primære omkostningselementer og sekundære omkostningselementer.</span><span class="sxs-lookup"><span data-stu-id="8f129-110">There are two types of cost elements: primary cost elements and secondary cost elements.</span></span> <span data-ttu-id="8f129-111">Følgende tabel beskriver forskellene mellem de to typer.</span><span class="sxs-lookup"><span data-stu-id="8f129-111">The following table describes the difference between the two types.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8f129-112"><strong>Primære omkostningselementer</strong></span><span class="sxs-lookup"><span data-stu-id="8f129-112"><strong>Primary cost elements</strong></span></span></td>
<td><span data-ttu-id="8f129-113"><strong>Sekundære omkostningselementer</strong></span><span class="sxs-lookup"><span data-stu-id="8f129-113"><strong>Secondary cost elements</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8f129-114">De primære omkostningselementer repræsenterer strømmen af omkostninger fra finansregnskab til omkostningsregnskab.</span><span class="sxs-lookup"><span data-stu-id="8f129-114">The primary cost elements represent the flow of costs from financial accounting to cost accounting.</span></span> <span data-ttu-id="8f129-115">Strukturen af omkostningselementet svarer til driftskontostrukturen i Finans, hvor et omkostningselement kan svare til en hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="8f129-115">The cost element structure corresponds to the profit and loss account structure in the general ledger, where a cost element can correspond to a main account.</span></span> <span data-ttu-id="8f129-116">Ikke alle hovedkonti kan nødvendigvis være repræsenteret som omkostningselementer, afhængigt af virksomhedens behov.</span><span class="sxs-lookup"><span data-stu-id="8f129-116">Not all main accounts may necessarily be represented as cost elements depending on the business needs.</span></span> <span data-ttu-id="8f129-117">Eksempler på primære omkostningselementer omfatter:</span><span class="sxs-lookup"><span data-stu-id="8f129-117">Examples of primary cost elements include:</span></span>
<ul>
<li><span data-ttu-id="8f129-118">Vareforbrug</span><span class="sxs-lookup"><span data-stu-id="8f129-118">Costs of goods sold (COGs)</span></span></li>
<li><span data-ttu-id="8f129-119">Indirekte materialeomkostninger</span><span class="sxs-lookup"><span data-stu-id="8f129-119">Indirect material costs</span></span></li>
<li><span data-ttu-id="8f129-120">Personaleomkostninger</span><span class="sxs-lookup"><span data-stu-id="8f129-120">Personnel costs</span></span></li>
<li><span data-ttu-id="8f129-121">Energiomkostninger</span><span class="sxs-lookup"><span data-stu-id="8f129-121">Energy costs</span></span></li>
</ul></td>
<td><span data-ttu-id="8f129-122">De sekundære omkostningselementer repræsenterer internt flow af omkostninger, da disse omkostninger kun oprettes og bruges i forbindelse med omkostningsregnskab.</span><span class="sxs-lookup"><span data-stu-id="8f129-122">The secondary cost elements represent the flow of costs internally because these costs are created and used only in Cost accounting.</span></span> <span data-ttu-id="8f129-123">De bruges til at sikre, at kilden til omkostningerne kan spores.</span><span class="sxs-lookup"><span data-stu-id="8f129-123">They are used to secure that the source of costs can be traced.</span></span> <span data-ttu-id="8f129-124">Disse omkostningselementer bruges i omkostningsfordelinger og beregninger af faste omkostninger.</span><span class="sxs-lookup"><span data-stu-id="8f129-124">These cost elements are used in cost allocations and overhead calculations.</span></span> <span data-ttu-id="8f129-125">Eksempler på sekundære omkostningselementer omfatter:</span><span class="sxs-lookup"><span data-stu-id="8f129-125">Examples of secondary cost elements include:</span></span>
<ul>
<li><span data-ttu-id="8f129-126">Produktionsomkostninger</span><span class="sxs-lookup"><span data-stu-id="8f129-126">Production costs</span></span></li>
<li><span data-ttu-id="8f129-127">Indirekte produktions, materiale- og marketingomkostninger</span><span class="sxs-lookup"><span data-stu-id="8f129-127">Production, material, and marketing overheads</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="cost-element-dimensions-and-cost-element-dimension-members"></a><span data-ttu-id="8f129-128">Omkostningselementdimensioner og omkostningselementers dimensionsmedlemmer</span><span class="sxs-lookup"><span data-stu-id="8f129-128">Cost element dimensions and cost element dimension members</span></span>
<span data-ttu-id="8f129-129">Omkostningselementer omtales som *omkostningselementdimensioner*.</span><span class="sxs-lookup"><span data-stu-id="8f129-129">Cost elements are referred to as *cost element dimensions* .</span></span> <span data-ttu-id="8f129-130">De enkelte dimensionsværdier kaldes *omkostningselementers dimensionsmedlemmer*.</span><span class="sxs-lookup"><span data-stu-id="8f129-130">The individual dimension values are called *cost element dimension members*.</span></span> <span data-ttu-id="8f129-131">For eksempel kan du have en dansk struktur for kontoplanen, der er grundlaget for lovpligtig rapportering.</span><span class="sxs-lookup"><span data-stu-id="8f129-131">For example, you have a US chart of accounts structure (COA) that is the base for your statutory reporting.</span></span> <span data-ttu-id="8f129-132">Kontoplanen anvendes som omkostningselementdimension.</span><span class="sxs-lookup"><span data-stu-id="8f129-132">This COA is used as the cost element dimension.</span></span> <span data-ttu-id="8f129-133">De konti, som er primære omkostningselementer, repræsenteres som omkostningselementets dimensionsmedlemmer i omkostningsregnskabet.</span><span class="sxs-lookup"><span data-stu-id="8f129-133">The accounts, which are primary cost elements, are represented as the cost element dimension members in Cost accounting.</span></span> <span data-ttu-id="8f129-134">Følgende skærmbillede vises et eksempel på hovedkonti som omkostningselementdimension med dets faktiske hovedkonti som dimensionsmedlemmer af omkostningselementet.</span><span class="sxs-lookup"><span data-stu-id="8f129-134">The following screenshot shows an example of Main Accounts as the cost element dimension with its actual main accounts as the cost element dimension members.</span></span> 

<span data-ttu-id="8f129-135">[![cost-element-dimensions](./media/cost-element-dimensions.png)](./media/cost-element-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="8f129-135">[![cost-element-dimensions](./media/cost-element-dimensions.png)](./media/cost-element-dimensions.png)</span></span>

## <a name="import-cost-element-dimension-members-through-data-connectors"></a><span data-ttu-id="8f129-136">Importere omkostningselementers dimensionsmedlemmer gennem dataforbindelser</span><span class="sxs-lookup"><span data-stu-id="8f129-136">Import cost element dimension members through data connectors</span></span>
<span data-ttu-id="8f129-137">For at forenkle opsætningen af omkostningselementets dimensionsmedlemmer i omkostningsregnskabet kan du bruge dataforbindelser, der enten er færdigbyggede eller tilpassede til at hente de primære omkostningselementer fra et eller flere kildesystemer.</span><span class="sxs-lookup"><span data-stu-id="8f129-137">To ease the setup of cost element dimension members in Cost accounting, you can use data connectors that are either pre-built or your custom build to retrieve the primary cost elements from one or more source systems.</span></span>

## <a name="implementation-considerations"></a><span data-ttu-id="8f129-138">Overvejelser i forbindelse med implementering</span><span class="sxs-lookup"><span data-stu-id="8f129-138">Implementation considerations</span></span>
<span data-ttu-id="8f129-139">Da omkostningselementer repræsenterer det laveste niveau af oplysninger om omkostninger, skal du sikre dig, at alle de omkostningselementer, der kræves i den ledelsesmæssige rapportering, er medtaget, når du implementerer omkostningselementernes struktur.</span><span class="sxs-lookup"><span data-stu-id="8f129-139">As cost elements represent the lowest level of cost details, you should make sure that all the cost elements required to make the managerial reporting are included when you implement the cost elements structure.</span></span> <span data-ttu-id="8f129-140">Det kan være en udfordring at finde et passende antal omkostningselementer til omkostningsstyring.</span><span class="sxs-lookup"><span data-stu-id="8f129-140">It can be a challenge to find an appropriate number of cost elements for cost control.</span></span> <span data-ttu-id="8f129-141">Tusindvis af omkostningselementer kan gøre det svært at styre hvert omkostningselement.</span><span class="sxs-lookup"><span data-stu-id="8f129-141">Having thousands of cost elements can make it difficult to control each cost element.</span></span> <span data-ttu-id="8f129-142">Som et alternativ kan du gruppere omkostningselementer og administrere omkostningsstyring på et samlet niveau.</span><span class="sxs-lookup"><span data-stu-id="8f129-142">As an alternative, you can group cost elements and manage cost control at an aggregated level.</span></span>



