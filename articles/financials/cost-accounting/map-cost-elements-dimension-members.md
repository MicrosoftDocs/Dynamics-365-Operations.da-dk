---
title: "Knytte dimensionsmedlemmer for omkostningselement til et fælles sæt dimensionsmedlemmer"
description: "Ved tilknytning af forskellige dimensionsmedlemmer for omkostningselement til et fælles sæt dimensionsmedlemmer for omkostningselement kan du flette data i et fælles format til analyseformål."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimension, CAMDimensionMember
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 223234
ms.assetid: 4c66a231-aed2-48b5-9727-b3eb4fe6e6aa
ms.search.region: global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 57602f03706e54475aee3ca1817a9f170a2b9f2d
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---

# <a name="map-cost-element-dimension-members-to-a-common-set-of-dimension-members"></a><span data-ttu-id="e5192-103">Knytte dimensionsmedlemmer for omkostningselement til et fælles sæt dimensionsmedlemmer</span><span class="sxs-lookup"><span data-stu-id="e5192-103">Map cost element dimension members to a common set of dimension members</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e5192-104">Ved tilknytning af forskellige dimensionsmedlemmer for omkostningselement til et fælles sæt dimensionsmedlemmer for omkostningselement kan du flette data i et fælles format til analyseformål.</span><span class="sxs-lookup"><span data-stu-id="e5192-104">By mapping different cost element dimension members to a common set of cost element dimension members, you merge data into a common format for analysis purposes.</span></span>

<span data-ttu-id="e5192-105">Hvis du er en global virksomhed og overholder lovpligtige regnskabsmæssige krav, kan du bruge flere kontoplaner.</span><span class="sxs-lookup"><span data-stu-id="e5192-105">If you're a global company and comply with statutory accounting requirements, you might use multiple charts of accounts.</span></span> <span data-ttu-id="e5192-106">Når du importerer dimensionsmedlemmer for omkostningselementer fra forskellige kontoplaner, kan det ende med en blanding af konti.</span><span class="sxs-lookup"><span data-stu-id="e5192-106">When you import cost element dimension members from different charts of accounts, you can end up with a mix of accounts.</span></span> <span data-ttu-id="e5192-107">Men disse konti kan faktisk have samme karakter, og du kan måske analysere og allokere omkostninger til dem ved hjælp af et fælles format.</span><span class="sxs-lookup"><span data-stu-id="e5192-107">However, these accounts might actually have the same nature, and you might want to analyze and allocate costs for them by using a common format.</span></span>

## <a name="map-cost-element-dimension-members-to-a-common-format"></a><span data-ttu-id="e5192-108">Knytte dimensionsmedlemmer for omkostningselementer til et fælles format</span><span class="sxs-lookup"><span data-stu-id="e5192-108">Map cost element dimension members to a common format</span></span>
<span data-ttu-id="e5192-109">Følgende eksempel viser, hvordan du, som omkostningscontroller, kan oprette en ny dimension til omkostningselement i omkostningsregnskab, der knytter omkostningselementers dimensionsmedlemmer fra den amerikanske kontoplanstruktur og den franske kontoplanstruktur til et fælles sæt dimensionsmedlemmer for omkostningselement.</span><span class="sxs-lookup"><span data-stu-id="e5192-109">The following example shows how you, as a cost controller, can create a new cost element dimension in Cost accounting that maps cost element dimension members from the US chart of accounts structure and the French chart of accounts structure to a common set of cost element dimension members.</span></span> <span data-ttu-id="e5192-110">Du kan derefter bruge det fælles sæt dimensionsmedlemmer for omkostningselement til at analysere omkostningsdata fra de to juridiske enheder i omkostningsregnskabet for Finans.</span><span class="sxs-lookup"><span data-stu-id="e5192-110">You can then use the common set of cost element dimension members to analyze cost data from the two legal entities in a cost accounting ledger.</span></span>

| <span data-ttu-id="e5192-111">Kilde: amerikansk kontoplan</span><span class="sxs-lookup"><span data-stu-id="e5192-111">Source: US chart of accounts</span></span>                                          | <span data-ttu-id="e5192-112">Kilde: fransk kontoplan</span><span class="sxs-lookup"><span data-stu-id="e5192-112">Source: French chart of accounts</span></span>                                          | <span data-ttu-id="e5192-113">Nyt sæt fælles dimensionsmedlemmer for omkostningselement</span><span class="sxs-lookup"><span data-stu-id="e5192-113">New common set of cost element dimension members</span></span>                        |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="e5192-114">Importerede dimensionsmedlemmer for omkostningselement fra amerikanske kontoplaner</span><span class="sxs-lookup"><span data-stu-id="e5192-114">Imported cost element dimension members from the US chart of accounts</span></span> | <span data-ttu-id="e5192-115">Importerede dimensionsmedlemmer for omkostningselement fra franske kontoplaner</span><span class="sxs-lookup"><span data-stu-id="e5192-115">Imported cost element dimension members from the French chart of accounts</span></span> | <span data-ttu-id="e5192-116">Tilknytning af amerikanske og franske dimensionsmedlemmer for omkostningselement til et fælles sæt</span><span class="sxs-lookup"><span data-stu-id="e5192-116">Mapping of US and French cost element dimension members to a common set</span></span> |
| <span data-ttu-id="e5192-117">5001: salg</span><span class="sxs-lookup"><span data-stu-id="e5192-117">5001: Sales</span></span>                                                           | <span data-ttu-id="e5192-118">5001: salg og marketing</span><span class="sxs-lookup"><span data-stu-id="e5192-118">5001: Sales and advertising</span></span>                                               | <span data-ttu-id="e5192-119">5000: salg og marketing</span><span class="sxs-lookup"><span data-stu-id="e5192-119">5000: Sales and advertising</span></span>                                             |
| <span data-ttu-id="e5192-120">5030: annoncer</span><span class="sxs-lookup"><span data-stu-id="e5192-120">5030: Advertising</span></span>                                                     | <span data-ttu-id="e5192-121">6390: lagerkøb\*</span><span class="sxs-lookup"><span data-stu-id="e5192-121">6390: Stock purchase\*</span></span>                                                    | <span data-ttu-id="e5192-122">7000: rengøringsudgifter</span><span class="sxs-lookup"><span data-stu-id="e5192-122">7000: Cleaning expenses</span></span>                                                 |
| <span data-ttu-id="e5192-123">7001: rengøringsudgifter</span><span class="sxs-lookup"><span data-stu-id="e5192-123">7001: Cleaning expenses</span></span>                                               | <span data-ttu-id="e5192-124">7001: rejseudgifter</span><span class="sxs-lookup"><span data-stu-id="e5192-124">7001: Travel expense</span></span>                                                      | <span data-ttu-id="e5192-125">7001: rejseudgifter</span><span class="sxs-lookup"><span data-stu-id="e5192-125">7001: Travel expenses</span></span>                                                   |

<span data-ttu-id="e5192-126">\* Det franske dimensionsmedlem for omkostningselement er ikke tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="e5192-126">\*The Stock purchase French cost element dimension member isn't mapped.</span></span>

## <a name="currency-conversion"></a><span data-ttu-id="e5192-127">Valutaomregning</span><span class="sxs-lookup"><span data-stu-id="e5192-127">Currency conversion</span></span>
<span data-ttu-id="e5192-128">De forskellige kontoplaner, som du bruger, kan konfigureres til at bruge forskellige valutaer.</span><span class="sxs-lookup"><span data-stu-id="e5192-128">The various charts of accounts that you use might be set up to use different currencies.</span></span> <span data-ttu-id="e5192-129">I dette tilfælde skal du angive en valutaomregning, så omkostningsdata der behandles ved hjælp af den rigtige valuta, som er defineret i omkostningsregnskabet for Finans, hvor dimensionsmedlemmer for omkostningselement anvendes.</span><span class="sxs-lookup"><span data-stu-id="e5192-129">In this case, be sure to specify a currency conversion, so that cost data is processed by using the correct currency, as defined in the cost accounting ledger where the cost element dimension members are used.</span></span> <span data-ttu-id="e5192-130">I ovenstående eksempel bruges amerikanske dollar (USD) i omkostningsregnskabet for Finans, så du skal oprette en valutaomregning fra USD til euro (EUR) for at behandle transaktioner for det tilknyttede omkostningselement dimensionsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="e5192-130">In the preceding example, if US dollars (USD) are used in the cost accounting ledger, you must create a currency conversion from USD to euros (EUR) to process transactions for the mapped cost element dimension members.</span></span>

## <a name="update-mappings-at-any-time"></a><span data-ttu-id="e5192-131">Opdatere tilknytninger efter behov</span><span class="sxs-lookup"><span data-stu-id="e5192-131">Update mappings at any time</span></span>
<span data-ttu-id="e5192-132">Du kan opdatere tilknytningsdefinitionerne af en dimension med omkostningselement når som helst.</span><span class="sxs-lookup"><span data-stu-id="e5192-132">You can update the mapping definitions for a cost element dimension at any time.</span></span> <span data-ttu-id="e5192-133">Da tilknytningerne ikke er datorelaterede, anvendes ændringer, næste gang du behandler omkostningsposteringer eller kører omkostningsberegninger.</span><span class="sxs-lookup"><span data-stu-id="e5192-133">Because mappings aren't date-effective, changes are applied the next time that you process cost transactions or run cost calculations.</span></span>




