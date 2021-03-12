---
title: Generere en begrænset plan
description: Dette emne forklarer, hvordan du opretter en plan, der tager højde for både materiale- og kapacitetsbegrænsninger.
author: ShylaThompson
manager: tfehr
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d4af946a8dd4e5311bcb90386c88d5e7f205c4eb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999850"
---
# <a name="generate-a-constrained-plan"></a><span data-ttu-id="7908a-103">Generere en begrænset plan</span><span class="sxs-lookup"><span data-stu-id="7908a-103">Generate a constrained plan</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7908a-104">Dette emne forklarer, hvordan du opretter en plan, der tager højde for både materiale- og kapacitetsbegrænsninger.</span><span class="sxs-lookup"><span data-stu-id="7908a-104">This topic explains how to create a plan that takes into account both material and capacity constraints.</span></span> <span data-ttu-id="7908a-105">Planen sikrer, at produktion ikke starter, før materialer er tilgængelige, og ressourcer overbookes ikke.</span><span class="sxs-lookup"><span data-stu-id="7908a-105">The plan ensures that manufacturing doesn't start before materials are available and resources are not overbooked.</span></span> 

<span data-ttu-id="7908a-106">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="7908a-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="7908a-107">Denne procedure er beregnet til produktionsplanlæggeren.</span><span class="sxs-lookup"><span data-stu-id="7908a-107">This procedure is intended for the production planner.</span></span>


## <a name="set-up-a-constrained-plan"></a><span data-ttu-id="7908a-108">Konfigurer en begrænset plan</span><span class="sxs-lookup"><span data-stu-id="7908a-108">Set up a constrained plan</span></span>
1. <span data-ttu-id="7908a-109">Vælg arbejdsområdet til **Varedisponering** på startsiden.</span><span class="sxs-lookup"><span data-stu-id="7908a-109">In the home page, select the **Master planning** workspace.</span></span>
2. <span data-ttu-id="7908a-110">Vælg **Behovsplaner** på listen over links længst til højre i arbejdsområdet.</span><span class="sxs-lookup"><span data-stu-id="7908a-110">Select **Master plans** in the list of links on the far right side of the workspace.</span></span>
3. <span data-ttu-id="7908a-111">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="7908a-111">In the list, find and select the desired record.</span></span> <span data-ttu-id="7908a-112">Eksempel: **StaticPlan**</span><span class="sxs-lookup"><span data-stu-id="7908a-112">Example: **StaticPlan**</span></span>  
4. <span data-ttu-id="7908a-113">Vælg **Ja** i feltet **Kapacitetsbegrænsning**.</span><span class="sxs-lookup"><span data-stu-id="7908a-113">Select **Yes** in the **Finite capacity** field.</span></span>
5. <span data-ttu-id="7908a-114">Angiv `30` i feltet **Tidshorisont for kapacitetsbegrænsning**.</span><span class="sxs-lookup"><span data-stu-id="7908a-114">In the **Finite capacity time fence** field, enter `30`.</span></span>
6. <span data-ttu-id="7908a-115">Udvid sektionen **Tidshorisonter i dage**.</span><span class="sxs-lookup"><span data-stu-id="7908a-115">Expand the **Time fences in days** section.</span></span>
7. <span data-ttu-id="7908a-116">Vælg **Ja** i feltet **Kapacitet**.</span><span class="sxs-lookup"><span data-stu-id="7908a-116">Select **Yes** in the **Capacity** field.</span></span>
8. <span data-ttu-id="7908a-117">Angiv et tal i feltet **Tidshorisont for kapacitetsplanlægning (dage)**.</span><span class="sxs-lookup"><span data-stu-id="7908a-117">In the **Capacity scheduling time fence (days)** field, enter a number.</span></span> <span data-ttu-id="7908a-118">Eksempel: `60`</span><span class="sxs-lookup"><span data-stu-id="7908a-118">Example: `60`</span></span>  
9. <span data-ttu-id="7908a-119">Vælg **Ja** i feltet **Beregnede forsinkelser**.</span><span class="sxs-lookup"><span data-stu-id="7908a-119">Select **Yes** in the **Calculated delays** field.</span></span>
10. <span data-ttu-id="7908a-120">Angiv et tal i feltet **Tidshorisont for beregning af forsinkelser (dage)**.</span><span class="sxs-lookup"><span data-stu-id="7908a-120">In the **Calculate delays time fence (days)** field, enter a number.</span></span> <span data-ttu-id="7908a-121">Eksempel: `60`</span><span class="sxs-lookup"><span data-stu-id="7908a-121">Example: `60`</span></span> 
11. <span data-ttu-id="7908a-122">Udvid sektionen **Beregnede forsinkelser**.</span><span class="sxs-lookup"><span data-stu-id="7908a-122">Expand the **Calculated delays** section.</span></span>
12. <span data-ttu-id="7908a-123">Vælg **Ja** i feltet **Tilføj den beregnede forsinkelse til behovsdatoen**.</span><span class="sxs-lookup"><span data-stu-id="7908a-123">Select **Yes** in all **Add the calculated delay to the requirement date** fields.</span></span>
13. <span data-ttu-id="7908a-124">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="7908a-124">Close the page.</span></span>

## <a name="create-a-constrained-plan"></a><span data-ttu-id="7908a-125">Opret en begrænset plan</span><span class="sxs-lookup"><span data-stu-id="7908a-125">Create a constrained plan</span></span>
1. <span data-ttu-id="7908a-126">Vælg **Kør**.</span><span class="sxs-lookup"><span data-stu-id="7908a-126">Select **Run**.</span></span>
2. <span data-ttu-id="7908a-127">Angiv eller vælg den plan, du har defineret betingelser for, i feltet **Behovsplan**.</span><span class="sxs-lookup"><span data-stu-id="7908a-127">In the **Master plan** field, enter or select the plan for which you have set up constraints.</span></span>  
3. <span data-ttu-id="7908a-128">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="7908a-128">Select **OK**.</span></span>
4. <span data-ttu-id="7908a-129">Vælg **Ordreforslag**.</span><span class="sxs-lookup"><span data-stu-id="7908a-129">Select **Planned orders**.</span></span>

