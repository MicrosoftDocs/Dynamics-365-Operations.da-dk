---
title: Generere en begrænset plan
description: Denne procedure viser, hvordan du opretter en plan, der tager højde for både materiale- og kapacitetsbegrænsninger.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 72cddd58b7068e08cddf24df83da8da2f7af7168
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845281"
---
# <a name="generate-a-constrained-plan"></a><span data-ttu-id="5f03d-103">Generere en begrænset plan</span><span class="sxs-lookup"><span data-stu-id="5f03d-103">Generate a constrained plan</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5f03d-104">Denne procedure viser, hvordan du opretter en plan, der tager højde for både materiale- og kapacitetsbegrænsninger.</span><span class="sxs-lookup"><span data-stu-id="5f03d-104">This procedure shows how to create a plan that takes into account both material and capacity constraints.</span></span> <span data-ttu-id="5f03d-105">Planen sikrer, at produktion ikke starter, før materialer er tilgængelige, og ressourcer overbookes ikke.</span><span class="sxs-lookup"><span data-stu-id="5f03d-105">The plan ensures that manufacturing doesn't start before materials are available and resources are not overbooked.</span></span> 

<span data-ttu-id="5f03d-106">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="5f03d-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="5f03d-107">Denne procedure er beregnet til produktionsplanlæggeren.</span><span class="sxs-lookup"><span data-stu-id="5f03d-107">This procedure is intended for the production planner.</span></span>


## <a name="set-up-a-constrained-plan"></a><span data-ttu-id="5f03d-108">Konfigurer en begrænset plan</span><span class="sxs-lookup"><span data-stu-id="5f03d-108">Set up a constrained plan</span></span>
1. <span data-ttu-id="5f03d-109">Klik på Varedisponering.</span><span class="sxs-lookup"><span data-stu-id="5f03d-109">Click Master planning.</span></span>
2. <span data-ttu-id="5f03d-110">Klik på Behovsplaner.</span><span class="sxs-lookup"><span data-stu-id="5f03d-110">Click Master plans.</span></span>
3. <span data-ttu-id="5f03d-111">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="5f03d-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5f03d-112">Eksempel: StaticPlan</span><span class="sxs-lookup"><span data-stu-id="5f03d-112">Example: StaticPlan</span></span>  
4. <span data-ttu-id="5f03d-113">Vælg Ja i feltet Kapacitetsbegrænsning.</span><span class="sxs-lookup"><span data-stu-id="5f03d-113">Select Yes in the Finite capacity field.</span></span>
5. <span data-ttu-id="5f03d-114">Angiv "30" i feltet Tidshorisont for kapacitetsbegrænsning.</span><span class="sxs-lookup"><span data-stu-id="5f03d-114">In the Finite capacity time fence field, enter '30'.</span></span>
6. <span data-ttu-id="5f03d-115">Udvid sektionen Tidshorisonter i dage.</span><span class="sxs-lookup"><span data-stu-id="5f03d-115">Expand the Time fences in days section.</span></span>
7. <span data-ttu-id="5f03d-116">Vælg Ja i feltet Kapacitet.</span><span class="sxs-lookup"><span data-stu-id="5f03d-116">Select Yes in the Capacity field.</span></span>
8. <span data-ttu-id="5f03d-117">Angiv et tal i feltet Tidshorisont for kapacitetsplanlægning (dage).</span><span class="sxs-lookup"><span data-stu-id="5f03d-117">In the Capacity scheduling time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="5f03d-118">Eksempel: 60</span><span class="sxs-lookup"><span data-stu-id="5f03d-118">Example: 60</span></span>  
9. <span data-ttu-id="5f03d-119">Vælg Ja i feltet Beregnede forsinkelser.</span><span class="sxs-lookup"><span data-stu-id="5f03d-119">Select Yes in the Calculated delays field.</span></span>
10. <span data-ttu-id="5f03d-120">Angiv et tal i feltet Tidshorisont for beregning af forsinkelser (dage).</span><span class="sxs-lookup"><span data-stu-id="5f03d-120">In the Calculate delays time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="5f03d-121">Eksempel: 60</span><span class="sxs-lookup"><span data-stu-id="5f03d-121">Example: 60</span></span>  
11. <span data-ttu-id="5f03d-122">Udvid sektionen Beregnede forsinkelser.</span><span class="sxs-lookup"><span data-stu-id="5f03d-122">Expand the Calculated delays section.</span></span>
12. <span data-ttu-id="5f03d-123">Vælg Ja i feltet Tilføj den beregnede forsinkelse til behovsdatoen.</span><span class="sxs-lookup"><span data-stu-id="5f03d-123">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
13. <span data-ttu-id="5f03d-124">Vælg Ja i feltet Tilføj den beregnede forsinkelse til behovsdatoen.</span><span class="sxs-lookup"><span data-stu-id="5f03d-124">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
14. <span data-ttu-id="5f03d-125">Vælg Ja i feltet Tilføj den beregnede forsinkelse til behovsdatoen.</span><span class="sxs-lookup"><span data-stu-id="5f03d-125">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
15. <span data-ttu-id="5f03d-126">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="5f03d-126">Close the page.</span></span>

## <a name="create-a-constrained-plan"></a><span data-ttu-id="5f03d-127">Opret en begrænset plan</span><span class="sxs-lookup"><span data-stu-id="5f03d-127">Create a constrained plan</span></span>
1. <span data-ttu-id="5f03d-128">Klik på Kør.</span><span class="sxs-lookup"><span data-stu-id="5f03d-128">Click Run.</span></span>
2. <span data-ttu-id="5f03d-129">Indtast eller vælg en værdi i feltet Behovsplan.</span><span class="sxs-lookup"><span data-stu-id="5f03d-129">In the Master plan field, enter or select a value.</span></span>
    * <span data-ttu-id="5f03d-130">Vælg den plan, som du har konfigureret begrænsninger for.</span><span class="sxs-lookup"><span data-stu-id="5f03d-130">Select the plan for which you have set up constraints.</span></span>  
3. <span data-ttu-id="5f03d-131">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="5f03d-131">Click OK.</span></span>
    * <span data-ttu-id="5f03d-132">Det kan tage et stykke tid.</span><span class="sxs-lookup"><span data-stu-id="5f03d-132">This may take a while.</span></span>  
4. <span data-ttu-id="5f03d-133">Klik på Ordreforslag.</span><span class="sxs-lookup"><span data-stu-id="5f03d-133">Click Planned orders.</span></span>

