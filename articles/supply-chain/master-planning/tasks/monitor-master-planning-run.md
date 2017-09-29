--- 
title: "Overvåge kørsel af en varedisponering"
description: "Produktionsplanlæggeren ønsker at se, om en varedisponeringskørsel er i gang."
author: YuyuScheller
manager: AnnBe
ms.date: 06/10/2016
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
ms.openlocfilehash: 1e08d9fd3388561563e6fb982416186a652b4ce2
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---
# <a name="monitor-a-master-planning-run"></a><span data-ttu-id="0910e-103">Overvåge kørsel af en varedisponering</span><span class="sxs-lookup"><span data-stu-id="0910e-103">Monitor a master planning run</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0910e-104">Produktionsplanlæggeren ønsker at se, om en varedisponeringskørsel er i gang.</span><span class="sxs-lookup"><span data-stu-id="0910e-104">The production planner wants to see if a master planning run is in progress.</span></span> <span data-ttu-id="0910e-105">Brug USMF-demodatafirmaet til at fuldføre denne procedure.</span><span class="sxs-lookup"><span data-stu-id="0910e-105">Use the demo data company USMF to complete this procedure.</span></span>


## <a name="run-master-planning"></a><span data-ttu-id="0910e-106">Køre varedisponering</span><span class="sxs-lookup"><span data-stu-id="0910e-106">Run master planning</span></span>
1. <span data-ttu-id="0910e-107">Klik på Varedisponering.</span><span class="sxs-lookup"><span data-stu-id="0910e-107">Click Master planning.</span></span>
    * <span data-ttu-id="0910e-108">Det findes på standarddashboardet.</span><span class="sxs-lookup"><span data-stu-id="0910e-108">You'll find this on the default dashboard.</span></span>  
2. <span data-ttu-id="0910e-109">Indtast eller vælg en værdi i feltet Plan.</span><span class="sxs-lookup"><span data-stu-id="0910e-109">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="0910e-110">Eksempel: StaticPlan</span><span class="sxs-lookup"><span data-stu-id="0910e-110">Example: StaticPlan</span></span>  
3. <span data-ttu-id="0910e-111">Klik på Kør.</span><span class="sxs-lookup"><span data-stu-id="0910e-111">Click Run.</span></span>
4. <span data-ttu-id="0910e-112">Vælg Ja i feltet Spor behandlingstidspunkt.</span><span class="sxs-lookup"><span data-stu-id="0910e-112">Select Yes in the Track processing time field.</span></span>
    * <span data-ttu-id="0910e-113">Hvis feltet allerede er markeret, skal du springe over dette trin.</span><span class="sxs-lookup"><span data-stu-id="0910e-113">If the field is already selected, skip this step.</span></span>  
5. <span data-ttu-id="0910e-114">Indtast et antal i feltet Antal tråde.</span><span class="sxs-lookup"><span data-stu-id="0910e-114">In the Number of threads field, enter a number.</span></span>
6. <span data-ttu-id="0910e-115">Udvid posterne for at inkludere sektion.</span><span class="sxs-lookup"><span data-stu-id="0910e-115">Expand the Records to include section.</span></span>
7. <span data-ttu-id="0910e-116">Klik på Filtrér.</span><span class="sxs-lookup"><span data-stu-id="0910e-116">Click Filter.</span></span>
8. <span data-ttu-id="0910e-117">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="0910e-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="0910e-118">Marker rækken, hvor feltet = Varenummer.</span><span class="sxs-lookup"><span data-stu-id="0910e-118">Mark the row where Field = Item number.</span></span>  
9. <span data-ttu-id="0910e-119">Indtast eller vælg en værdi i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="0910e-119">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="0910e-120">Eksempel: T0001</span><span class="sxs-lookup"><span data-stu-id="0910e-120">Example: T0001</span></span>  
10. <span data-ttu-id="0910e-121">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0910e-121">Click OK.</span></span>
11. <span data-ttu-id="0910e-122">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0910e-122">Click OK.</span></span>

## <a name="monitor-the-master-planning-run"></a><span data-ttu-id="0910e-123">Overvåge kørslen af varedisponering</span><span class="sxs-lookup"><span data-stu-id="0910e-123">Monitor the master planning run</span></span>
1. <span data-ttu-id="0910e-124">Klik på Historik.</span><span class="sxs-lookup"><span data-stu-id="0910e-124">Click History.</span></span>
2. <span data-ttu-id="0910e-125">Klik på Forespørgsler.</span><span class="sxs-lookup"><span data-stu-id="0910e-125">Click Inquiries.</span></span>
3. <span data-ttu-id="0910e-126">Klik på Procesopgavens varighed.</span><span class="sxs-lookup"><span data-stu-id="0910e-126">Click Process task duration.</span></span>
4. <span data-ttu-id="0910e-127">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="0910e-127">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0910e-128">For hver vare kan du få et overblik over, hvor lang tid det tog at fuldføre hvert trin i planlægningen.</span><span class="sxs-lookup"><span data-stu-id="0910e-128">For each item you can get an overview of how long it took to complete each planning step.</span></span>  


