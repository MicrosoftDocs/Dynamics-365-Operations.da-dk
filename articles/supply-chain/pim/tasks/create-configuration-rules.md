--- 
title: Oprette konfigurationsregler
description: Denne procedure opretter variantregler, der kan bruges til dimensionsbaseret konfiguration for at gennemtvinge eller forhindre bestemte kombinationer af styklistelinjer.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMTable, BOMConfigRule, ConfigItemIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: a315ddecd2e10f508b86ac8ea18a36df71616963
ms.contentlocale: da-dk
ms.lasthandoff: 09/14/2018

---
# <a name="create-configuration-rules"></a><span data-ttu-id="ea670-103">Oprette konfigurationsregler</span><span class="sxs-lookup"><span data-stu-id="ea670-103">Create configuration rules</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ea670-104">Denne procedure opretter variantregler, der kan bruges til dimensionsbaseret konfiguration for at gennemtvinge eller forhindre bestemte kombinationer af styklistelinjer.</span><span class="sxs-lookup"><span data-stu-id="ea670-104">This procedure creates configuration rules that can be used for dimension-based configuration to enforce or prevent certain combinations of BOM lines.</span></span> <span data-ttu-id="ea670-105">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="ea670-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="ea670-106">Dette er den syvende procedure ud af otte, som forklarer, hvordan du kan opbygge kombinationer til dimensionsbaseret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="ea670-106">This is the seventh procedure out of eight that explains how to build combinations for dimension-based configuration.</span></span>

1. <span data-ttu-id="ea670-107">Gå til Administration af produktoplysninger > Styklister og formler > Styklister.</span><span class="sxs-lookup"><span data-stu-id="ea670-107">Go to Product information management > Bills of materials and formulas > Bills of materials.</span></span>
2. <span data-ttu-id="ea670-108">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="ea670-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ea670-109">Find og vælg stykliste for dimensionsbaseret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="ea670-109">Find and select the BOM for the dimension-based configuration.</span></span>  
3. <span data-ttu-id="ea670-110">Klik på Indstillinger i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="ea670-110">On the Action Pane, click Options.</span></span>
4. <span data-ttu-id="ea670-111">Klik på Skift visning.</span><span class="sxs-lookup"><span data-stu-id="ea670-111">Click Change view.</span></span>
5. <span data-ttu-id="ea670-112">Klik på Overskriftsvisning.</span><span class="sxs-lookup"><span data-stu-id="ea670-112">Click Header view.</span></span>
    * <span data-ttu-id="ea670-113">Åbn Overskriftsvisning for at åbne oversigtspanelet Variantrute.</span><span class="sxs-lookup"><span data-stu-id="ea670-113">Open the header view to access the Configuration route FastTab.</span></span>  
6. <span data-ttu-id="ea670-114">Vis eller skjul sektionen Variansrute.</span><span class="sxs-lookup"><span data-stu-id="ea670-114">Expand or collapse the Configuration route section.</span></span>
    * <span data-ttu-id="ea670-115">Oversigtspanelet Variantrute skal være i udvidet tilstand.</span><span class="sxs-lookup"><span data-stu-id="ea670-115">The Configuration route FastTab must be in the expanded mode.</span></span>  
7. <span data-ttu-id="ea670-116">Klik på Konfigurationsregler.</span><span class="sxs-lookup"><span data-stu-id="ea670-116">Click Configuration rules.</span></span>
8. <span data-ttu-id="ea670-117">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="ea670-117">Click New.</span></span>
9. <span data-ttu-id="ea670-118">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ea670-118">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="ea670-119">Klik på rullelisten i feltet Varenummer for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="ea670-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="ea670-120">Varerne i den aktuelle variantgruppe vises.</span><span class="sxs-lookup"><span data-stu-id="ea670-120">The items in the current configuration group are displayed.</span></span> <span data-ttu-id="ea670-121">Vælg den, der repræsenterer betingelsen i reglen.</span><span class="sxs-lookup"><span data-stu-id="ea670-121">Select the one that represents the condition in the rule.</span></span>  
11. <span data-ttu-id="ea670-122">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ea670-122">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="ea670-123">Vælg en indstilling i feltet Metode.</span><span class="sxs-lookup"><span data-stu-id="ea670-123">In the Method field, select an option.</span></span>
    * <span data-ttu-id="ea670-124">Det er muligt at gennemtvinge enten en markering eller et fravalg af en vare fra en anden variantgruppe.</span><span class="sxs-lookup"><span data-stu-id="ea670-124">It is possible to enforce either a selection or a deselection of an item from another configuration group.</span></span>  
13. <span data-ttu-id="ea670-125">Klik på rullelisten i feltet Afledt gruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="ea670-125">In the Derived group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="ea670-126">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="ea670-126">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="ea670-127">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ea670-127">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ea670-128">Vælg den ønskede variantgruppe.</span><span class="sxs-lookup"><span data-stu-id="ea670-128">Select the desired configuration group.</span></span>  
16. <span data-ttu-id="ea670-129">Klik på rullelisten i feltet Afledt varenummer for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="ea670-129">In the Derived item number field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="ea670-130">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ea670-130">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ea670-131">Vælg det varenummer, der skal vælges eller fravælges afhængigt af den valgte metode.</span><span class="sxs-lookup"><span data-stu-id="ea670-131">Select the item number that will be either selected or deselected depending on the chosen method.</span></span>  
18. <span data-ttu-id="ea670-132">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ea670-132">Close the page.</span></span>


