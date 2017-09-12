--- 
title: "Generere en begrænset plan"
description: "Denne procedure viser, hvordan du opretter en plan, der tager højde for både materiale- og kapacitetsbegrænsninger."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 9deb615d05b90865ea6a050599bf91879b5688d0
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---
# <a name="generate-a-constrained-plan"></a><span data-ttu-id="601b7-103">Generere en begrænset plan</span><span class="sxs-lookup"><span data-stu-id="601b7-103">Generate a constrained plan</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="601b7-104">Denne procedure viser, hvordan du opretter en plan, der tager højde for både materiale- og kapacitetsbegrænsninger.</span><span class="sxs-lookup"><span data-stu-id="601b7-104">This procedure shows how to create a plan that takes into account both material and capacity constraints.</span></span> <span data-ttu-id="601b7-105">Planen sikrer, at produktion ikke starter, før materialer er tilgængelige, og ressourcer overbookes ikke.</span><span class="sxs-lookup"><span data-stu-id="601b7-105">The plan ensures that manufacturing doesn't start before materials are available and resources are not overbooked.</span></span> 

<span data-ttu-id="601b7-106">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="601b7-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="601b7-107">Denne procedure er beregnet til produktionsplanlæggeren.</span><span class="sxs-lookup"><span data-stu-id="601b7-107">This procedure is intended for the production planner.</span></span>


## <a name="set-up-a-constrained-plan"></a><span data-ttu-id="601b7-108">Konfigurer en begrænset plan</span><span class="sxs-lookup"><span data-stu-id="601b7-108">Set up a constrained plan</span></span>
1. <span data-ttu-id="601b7-109">Klik på Varedisponering.</span><span class="sxs-lookup"><span data-stu-id="601b7-109">Click Master planning.</span></span>
2. <span data-ttu-id="601b7-110">Klik på Behovsplaner.</span><span class="sxs-lookup"><span data-stu-id="601b7-110">Click Master plans.</span></span>
3. <span data-ttu-id="601b7-111">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="601b7-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="601b7-112">Eksempel: StaticPlan</span><span class="sxs-lookup"><span data-stu-id="601b7-112">Example: StaticPlan</span></span>  
4. <span data-ttu-id="601b7-113">Vælg Ja i feltet Kapacitetsbegrænsning.</span><span class="sxs-lookup"><span data-stu-id="601b7-113">Select Yes in the Finite capacity field.</span></span>
5. <span data-ttu-id="601b7-114">Angiv "30" i feltet Tidshorisont for kapacitetsbegrænsning.</span><span class="sxs-lookup"><span data-stu-id="601b7-114">In the Finite capacity time fence field, enter '30'.</span></span>
6. <span data-ttu-id="601b7-115">Udvid sektionen Tidshorisonter i dage.</span><span class="sxs-lookup"><span data-stu-id="601b7-115">Expand the Time fences in days section.</span></span>
7. <span data-ttu-id="601b7-116">Vælg Ja i feltet Kapacitet.</span><span class="sxs-lookup"><span data-stu-id="601b7-116">Select Yes in the Capacity field.</span></span>
8. <span data-ttu-id="601b7-117">Angiv et tal i feltet Tidshorisont for kapacitetsplanlægning (dage).</span><span class="sxs-lookup"><span data-stu-id="601b7-117">In the Capacity scheduling time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="601b7-118">Eksempel: 60</span><span class="sxs-lookup"><span data-stu-id="601b7-118">Example: 60</span></span>  
9. <span data-ttu-id="601b7-119">Vælg Ja i feltet Beregnede forsinkelser.</span><span class="sxs-lookup"><span data-stu-id="601b7-119">Select Yes in the Calculated delays field.</span></span>
10. <span data-ttu-id="601b7-120">Angiv et tal i feltet Tidshorisont for beregning af forsinkelser (dage).</span><span class="sxs-lookup"><span data-stu-id="601b7-120">In the Calculate delays time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="601b7-121">Eksempel: 60</span><span class="sxs-lookup"><span data-stu-id="601b7-121">Example: 60</span></span>  
11. <span data-ttu-id="601b7-122">Udvid sektionen Beregnede forsinkelser.</span><span class="sxs-lookup"><span data-stu-id="601b7-122">Expand the Calculated delays section.</span></span>
12. <span data-ttu-id="601b7-123">Vælg Ja i feltet Tilføj den beregnede forsinkelse til behovsdatoen.</span><span class="sxs-lookup"><span data-stu-id="601b7-123">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
13. <span data-ttu-id="601b7-124">Vælg Ja i feltet Tilføj den beregnede forsinkelse til behovsdatoen.</span><span class="sxs-lookup"><span data-stu-id="601b7-124">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
14. <span data-ttu-id="601b7-125">Vælg Ja i feltet Tilføj den beregnede forsinkelse til behovsdatoen.</span><span class="sxs-lookup"><span data-stu-id="601b7-125">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
15. <span data-ttu-id="601b7-126">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="601b7-126">Close the page.</span></span>

## <a name="create-a-constrained-plan"></a><span data-ttu-id="601b7-127">Opret en begrænset plan</span><span class="sxs-lookup"><span data-stu-id="601b7-127">Create a constrained plan</span></span>
1. <span data-ttu-id="601b7-128">Klik på Kør.</span><span class="sxs-lookup"><span data-stu-id="601b7-128">Click Run.</span></span>
2. <span data-ttu-id="601b7-129">Indtast eller vælg en værdi i feltet Behovsplan.</span><span class="sxs-lookup"><span data-stu-id="601b7-129">In the Master plan field, enter or select a value.</span></span>
    * <span data-ttu-id="601b7-130">Vælg den plan, som du har konfigureret begrænsninger for.</span><span class="sxs-lookup"><span data-stu-id="601b7-130">Select the plan for which you have set up constraints.</span></span>  
3. <span data-ttu-id="601b7-131">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="601b7-131">Click OK.</span></span>
    * <span data-ttu-id="601b7-132">Det kan tage et stykke tid.</span><span class="sxs-lookup"><span data-stu-id="601b7-132">This may take a while.</span></span>  
4. <span data-ttu-id="601b7-133">Klik på Ordreforslag.</span><span class="sxs-lookup"><span data-stu-id="601b7-133">Click Planned orders.</span></span>


