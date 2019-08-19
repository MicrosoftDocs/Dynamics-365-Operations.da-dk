---
title: Overvåge kørsel af en varedisponering
description: Produktionsplanlæggeren ønsker at se, om en varedisponeringskørsel er i gang.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b923b215528ecceaed9b5057ddb736ec959f1d65
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845107"
---
# <a name="monitor-a-master-planning-run"></a><span data-ttu-id="4a7f4-103">Overvåge kørsel af en varedisponering</span><span class="sxs-lookup"><span data-stu-id="4a7f4-103">Monitor a master planning run</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4a7f4-104">Produktionsplanlæggeren ønsker at se, om en varedisponeringskørsel er i gang.</span><span class="sxs-lookup"><span data-stu-id="4a7f4-104">The production planner wants to see if a master planning run is in progress.</span></span> <span data-ttu-id="4a7f4-105">Brug USMF-demodatafirmaet til at fuldføre denne procedure.</span><span class="sxs-lookup"><span data-stu-id="4a7f4-105">Use the demo data company USMF to complete this procedure.</span></span>


## <a name="run-master-planning"></a><span data-ttu-id="4a7f4-106">Køre varedisponering</span><span class="sxs-lookup"><span data-stu-id="4a7f4-106">Run master planning</span></span>
1. <span data-ttu-id="4a7f4-107">Klik på Varedisponering.</span><span class="sxs-lookup"><span data-stu-id="4a7f4-107">Click Master planning.</span></span>
    * <span data-ttu-id="4a7f4-108">Det findes på standarddashboardet.</span><span class="sxs-lookup"><span data-stu-id="4a7f4-108">You'll find this on the default dashboard.</span></span>  
2. <span data-ttu-id="4a7f4-109">Indtast eller vælg en værdi i feltet Plan.</span><span class="sxs-lookup"><span data-stu-id="4a7f4-109">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="4a7f4-110">Eksempel: StaticPlan</span><span class="sxs-lookup"><span data-stu-id="4a7f4-110">Example: StaticPlan</span></span>  
3. <span data-ttu-id="4a7f4-111">Klik på Kør.</span><span class="sxs-lookup"><span data-stu-id="4a7f4-111">Click Run.</span></span>
4. <span data-ttu-id="4a7f4-112">Vælg Ja i feltet Spor behandlingstidspunkt.</span><span class="sxs-lookup"><span data-stu-id="4a7f4-112">Select Yes in the Track processing time field.</span></span>
    * <span data-ttu-id="4a7f4-113">Hvis feltet allerede er markeret, skal du springe over dette trin.</span><span class="sxs-lookup"><span data-stu-id="4a7f4-113">If the field is already selected, skip this step.</span></span>  
5. <span data-ttu-id="4a7f4-114">Indtast et antal i feltet Antal tråde.</span><span class="sxs-lookup"><span data-stu-id="4a7f4-114">In the Number of threads field, enter a number.</span></span>
6. <span data-ttu-id="4a7f4-115">Udvid posterne for at inkludere sektion.</span><span class="sxs-lookup"><span data-stu-id="4a7f4-115">Expand the Records to include section.</span></span>
7. <span data-ttu-id="4a7f4-116">Klik på Filtrér.</span><span class="sxs-lookup"><span data-stu-id="4a7f4-116">Click Filter.</span></span>
8. <span data-ttu-id="4a7f4-117">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="4a7f4-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="4a7f4-118">Marker rækken, hvor feltet = Varenummer.</span><span class="sxs-lookup"><span data-stu-id="4a7f4-118">Mark the row where Field = Item number.</span></span>  
9. <span data-ttu-id="4a7f4-119">Indtast eller vælg en værdi i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="4a7f4-119">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="4a7f4-120">Eksempel: T0001</span><span class="sxs-lookup"><span data-stu-id="4a7f4-120">Example: T0001</span></span>  
10. <span data-ttu-id="4a7f4-121">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="4a7f4-121">Click OK.</span></span>
11. <span data-ttu-id="4a7f4-122">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="4a7f4-122">Click OK.</span></span>

## <a name="monitor-the-master-planning-run"></a><span data-ttu-id="4a7f4-123">Overvåge kørslen af varedisponering</span><span class="sxs-lookup"><span data-stu-id="4a7f4-123">Monitor the master planning run</span></span>
1. <span data-ttu-id="4a7f4-124">Klik på Historik.</span><span class="sxs-lookup"><span data-stu-id="4a7f4-124">Click History.</span></span>
2. <span data-ttu-id="4a7f4-125">Klik på Forespørgsler.</span><span class="sxs-lookup"><span data-stu-id="4a7f4-125">Click Inquiries.</span></span>
3. <span data-ttu-id="4a7f4-126">Klik på Procesopgavens varighed.</span><span class="sxs-lookup"><span data-stu-id="4a7f4-126">Click Process task duration.</span></span>
4. <span data-ttu-id="4a7f4-127">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="4a7f4-127">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4a7f4-128">For hver vare kan du få et overblik over, hvor lang tid det tog at fuldføre hvert trin i planlægningen.</span><span class="sxs-lookup"><span data-stu-id="4a7f4-128">For each item you can get an overview of how long it took to complete each planning step.</span></span>  

