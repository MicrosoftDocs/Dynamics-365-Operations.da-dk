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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0e2265f7788fd2a4a37f6fb96d7562649dbc5b1c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "336031"
---
# <a name="generate-a-constrained-plan"></a><span data-ttu-id="f86c3-103">Generere en begrænset plan</span><span class="sxs-lookup"><span data-stu-id="f86c3-103">Generate a constrained plan</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f86c3-104">Denne procedure viser, hvordan du opretter en plan, der tager højde for både materiale- og kapacitetsbegrænsninger.</span><span class="sxs-lookup"><span data-stu-id="f86c3-104">This procedure shows how to create a plan that takes into account both material and capacity constraints.</span></span> <span data-ttu-id="f86c3-105">Planen sikrer, at produktion ikke starter, før materialer er tilgængelige, og ressourcer overbookes ikke.</span><span class="sxs-lookup"><span data-stu-id="f86c3-105">The plan ensures that manufacturing doesn't start before materials are available and resources are not overbooked.</span></span> 

<span data-ttu-id="f86c3-106">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="f86c3-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="f86c3-107">Denne procedure er beregnet til produktionsplanlæggeren.</span><span class="sxs-lookup"><span data-stu-id="f86c3-107">This procedure is intended for the production planner.</span></span>


## <a name="set-up-a-constrained-plan"></a><span data-ttu-id="f86c3-108">Konfigurer en begrænset plan</span><span class="sxs-lookup"><span data-stu-id="f86c3-108">Set up a constrained plan</span></span>
1. <span data-ttu-id="f86c3-109">Klik på Varedisponering.</span><span class="sxs-lookup"><span data-stu-id="f86c3-109">Click Master planning.</span></span>
2. <span data-ttu-id="f86c3-110">Klik på Behovsplaner.</span><span class="sxs-lookup"><span data-stu-id="f86c3-110">Click Master plans.</span></span>
3. <span data-ttu-id="f86c3-111">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="f86c3-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f86c3-112">Eksempel: StaticPlan</span><span class="sxs-lookup"><span data-stu-id="f86c3-112">Example: StaticPlan</span></span>  
4. <span data-ttu-id="f86c3-113">Vælg Ja i feltet Kapacitetsbegrænsning.</span><span class="sxs-lookup"><span data-stu-id="f86c3-113">Select Yes in the Finite capacity field.</span></span>
5. <span data-ttu-id="f86c3-114">Angiv "30" i feltet Tidshorisont for kapacitetsbegrænsning.</span><span class="sxs-lookup"><span data-stu-id="f86c3-114">In the Finite capacity time fence field, enter '30'.</span></span>
6. <span data-ttu-id="f86c3-115">Udvid sektionen Tidshorisonter i dage.</span><span class="sxs-lookup"><span data-stu-id="f86c3-115">Expand the Time fences in days section.</span></span>
7. <span data-ttu-id="f86c3-116">Vælg Ja i feltet Kapacitet.</span><span class="sxs-lookup"><span data-stu-id="f86c3-116">Select Yes in the Capacity field.</span></span>
8. <span data-ttu-id="f86c3-117">Angiv et tal i feltet Tidshorisont for kapacitetsplanlægning (dage).</span><span class="sxs-lookup"><span data-stu-id="f86c3-117">In the Capacity scheduling time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="f86c3-118">Eksempel: 60</span><span class="sxs-lookup"><span data-stu-id="f86c3-118">Example: 60</span></span>  
9. <span data-ttu-id="f86c3-119">Vælg Ja i feltet Beregnede forsinkelser.</span><span class="sxs-lookup"><span data-stu-id="f86c3-119">Select Yes in the Calculated delays field.</span></span>
10. <span data-ttu-id="f86c3-120">Angiv et tal i feltet Tidshorisont for beregning af forsinkelser (dage).</span><span class="sxs-lookup"><span data-stu-id="f86c3-120">In the Calculate delays time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="f86c3-121">Eksempel: 60</span><span class="sxs-lookup"><span data-stu-id="f86c3-121">Example: 60</span></span>  
11. <span data-ttu-id="f86c3-122">Udvid sektionen Beregnede forsinkelser.</span><span class="sxs-lookup"><span data-stu-id="f86c3-122">Expand the Calculated delays section.</span></span>
12. <span data-ttu-id="f86c3-123">Vælg Ja i feltet Tilføj den beregnede forsinkelse til behovsdatoen.</span><span class="sxs-lookup"><span data-stu-id="f86c3-123">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
13. <span data-ttu-id="f86c3-124">Vælg Ja i feltet Tilføj den beregnede forsinkelse til behovsdatoen.</span><span class="sxs-lookup"><span data-stu-id="f86c3-124">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
14. <span data-ttu-id="f86c3-125">Vælg Ja i feltet Tilføj den beregnede forsinkelse til behovsdatoen.</span><span class="sxs-lookup"><span data-stu-id="f86c3-125">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
15. <span data-ttu-id="f86c3-126">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="f86c3-126">Close the page.</span></span>

## <a name="create-a-constrained-plan"></a><span data-ttu-id="f86c3-127">Opret en begrænset plan</span><span class="sxs-lookup"><span data-stu-id="f86c3-127">Create a constrained plan</span></span>
1. <span data-ttu-id="f86c3-128">Klik på Kør.</span><span class="sxs-lookup"><span data-stu-id="f86c3-128">Click Run.</span></span>
2. <span data-ttu-id="f86c3-129">Indtast eller vælg en værdi i feltet Behovsplan.</span><span class="sxs-lookup"><span data-stu-id="f86c3-129">In the Master plan field, enter or select a value.</span></span>
    * <span data-ttu-id="f86c3-130">Vælg den plan, som du har konfigureret begrænsninger for.</span><span class="sxs-lookup"><span data-stu-id="f86c3-130">Select the plan for which you have set up constraints.</span></span>  
3. <span data-ttu-id="f86c3-131">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="f86c3-131">Click OK.</span></span>
    * <span data-ttu-id="f86c3-132">Det kan tage et stykke tid.</span><span class="sxs-lookup"><span data-stu-id="f86c3-132">This may take a while.</span></span>  
4. <span data-ttu-id="f86c3-133">Klik på Ordreforslag.</span><span class="sxs-lookup"><span data-stu-id="f86c3-133">Click Planned orders.</span></span>

