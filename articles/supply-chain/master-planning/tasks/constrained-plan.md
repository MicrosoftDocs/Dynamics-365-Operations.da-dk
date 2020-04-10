---
title: Generere en begrænset plan
description: Dette emne forklarer, hvordan du opretter en plan, der tager højde for både materiale- og kapacitetsbegrænsninger.
author: ShylaThompson
manager: AnnBe
ms.date: 08/02/2019
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
ms.openlocfilehash: 126122d7be36cf1585f372adbae3ced8d6b15134
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150349"
---
# <a name="generate-a-constrained-plan"></a><span data-ttu-id="184ba-103">Generere en begrænset plan</span><span class="sxs-lookup"><span data-stu-id="184ba-103">Generate a constrained plan</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="184ba-104">Dette emne forklarer, hvordan du opretter en plan, der tager højde for både materiale- og kapacitetsbegrænsninger.</span><span class="sxs-lookup"><span data-stu-id="184ba-104">This topic explains how to create a plan that takes into account both material and capacity constraints.</span></span> <span data-ttu-id="184ba-105">Planen sikrer, at produktion ikke starter, før materialer er tilgængelige, og ressourcer overbookes ikke.</span><span class="sxs-lookup"><span data-stu-id="184ba-105">The plan ensures that manufacturing doesn't start before materials are available and resources are not overbooked.</span></span> 

<span data-ttu-id="184ba-106">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="184ba-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="184ba-107">Denne procedure er beregnet til produktionsplanlæggeren.</span><span class="sxs-lookup"><span data-stu-id="184ba-107">This procedure is intended for the production planner.</span></span>


## <a name="set-up-a-constrained-plan"></a><span data-ttu-id="184ba-108">Konfigurer en begrænset plan</span><span class="sxs-lookup"><span data-stu-id="184ba-108">Set up a constrained plan</span></span>
1. <span data-ttu-id="184ba-109">Vælg arbejdsområdet til **Varedisponering** på startsiden.</span><span class="sxs-lookup"><span data-stu-id="184ba-109">In the home page, select the **Master planning** workspace.</span></span>
2. <span data-ttu-id="184ba-110">Vælg **Behovsplaner** på listen over links længst til højre i arbejdsområdet.</span><span class="sxs-lookup"><span data-stu-id="184ba-110">Select **Master plans** in the list of links on the far right side of the workspace.</span></span>
3. <span data-ttu-id="184ba-111">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="184ba-111">In the list, find and select the desired record.</span></span> <span data-ttu-id="184ba-112">Eksempel: **StaticPlan**</span><span class="sxs-lookup"><span data-stu-id="184ba-112">Example: **StaticPlan**</span></span>  
4. <span data-ttu-id="184ba-113">Vælg **Ja** i feltet **Kapacitetsbegrænsning**.</span><span class="sxs-lookup"><span data-stu-id="184ba-113">Select **Yes** in the **Finite capacity** field.</span></span>
5. <span data-ttu-id="184ba-114">Angiv `30` i feltet **Tidshorisont for kapacitetsbegrænsning**.</span><span class="sxs-lookup"><span data-stu-id="184ba-114">In the **Finite capacity time fence** field, enter `30`.</span></span>
6. <span data-ttu-id="184ba-115">Udvid sektionen **Tidshorisonter i dage**.</span><span class="sxs-lookup"><span data-stu-id="184ba-115">Expand the **Time fences in days** section.</span></span>
7. <span data-ttu-id="184ba-116">Vælg **Ja** i feltet **Kapacitet**.</span><span class="sxs-lookup"><span data-stu-id="184ba-116">Select **Yes** in the **Capacity** field.</span></span>
8. <span data-ttu-id="184ba-117">Angiv et tal i feltet **Tidshorisont for kapacitetsplanlægning (dage)**.</span><span class="sxs-lookup"><span data-stu-id="184ba-117">In the **Capacity scheduling time fence (days)** field, enter a number.</span></span> <span data-ttu-id="184ba-118">Eksempel: `60`</span><span class="sxs-lookup"><span data-stu-id="184ba-118">Example: `60`</span></span>  
9. <span data-ttu-id="184ba-119">Vælg **Ja** i feltet **Beregnede forsinkelser**.</span><span class="sxs-lookup"><span data-stu-id="184ba-119">Select **Yes** in the **Calculated delays** field.</span></span>
10. <span data-ttu-id="184ba-120">Angiv et tal i feltet **Tidshorisont for beregning af forsinkelser (dage)**.</span><span class="sxs-lookup"><span data-stu-id="184ba-120">In the **Calculate delays time fence (days)** field, enter a number.</span></span> <span data-ttu-id="184ba-121">Eksempel: `60`</span><span class="sxs-lookup"><span data-stu-id="184ba-121">Example: `60`</span></span> 
11. <span data-ttu-id="184ba-122">Udvid sektionen **Beregnede forsinkelser**.</span><span class="sxs-lookup"><span data-stu-id="184ba-122">Expand the **Calculated delays** section.</span></span>
12. <span data-ttu-id="184ba-123">Vælg **Ja** i feltet **Tilføj den beregnede forsinkelse til behovsdatoen**.</span><span class="sxs-lookup"><span data-stu-id="184ba-123">Select **Yes** in all **Add the calculated delay to the requirement date** fields.</span></span>
13. <span data-ttu-id="184ba-124">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="184ba-124">Close the page.</span></span>

## <a name="create-a-constrained-plan"></a><span data-ttu-id="184ba-125">Opret en begrænset plan</span><span class="sxs-lookup"><span data-stu-id="184ba-125">Create a constrained plan</span></span>
1. <span data-ttu-id="184ba-126">Vælg **Kør**.</span><span class="sxs-lookup"><span data-stu-id="184ba-126">Select **Run**.</span></span>
2. <span data-ttu-id="184ba-127">Angiv eller vælg den plan, du har defineret betingelser for, i feltet **Behovsplan**.</span><span class="sxs-lookup"><span data-stu-id="184ba-127">In the **Master plan** field, enter or select the plan for which you have set up constraints.</span></span>  
3. <span data-ttu-id="184ba-128">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="184ba-128">Select **OK**.</span></span>
4. <span data-ttu-id="184ba-129">Vælg **Ordreforslag**.</span><span class="sxs-lookup"><span data-stu-id="184ba-129">Select **Planned orders**.</span></span>

