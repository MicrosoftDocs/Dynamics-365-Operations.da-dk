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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7c2e158d8cbad1f5d4f377f6a8eb43487b34ffdc
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "367495"
---
# <a name="monitor-a-master-planning-run"></a><span data-ttu-id="7ca7f-103">Overvåge kørsel af en varedisponering</span><span class="sxs-lookup"><span data-stu-id="7ca7f-103">Monitor a master planning run</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7ca7f-104">Produktionsplanlæggeren ønsker at se, om en varedisponeringskørsel er i gang.</span><span class="sxs-lookup"><span data-stu-id="7ca7f-104">The production planner wants to see if a master planning run is in progress.</span></span> <span data-ttu-id="7ca7f-105">Brug USMF-demodatafirmaet til at fuldføre denne procedure.</span><span class="sxs-lookup"><span data-stu-id="7ca7f-105">Use the demo data company USMF to complete this procedure.</span></span>


## <a name="run-master-planning"></a><span data-ttu-id="7ca7f-106">Køre varedisponering</span><span class="sxs-lookup"><span data-stu-id="7ca7f-106">Run master planning</span></span>
1. <span data-ttu-id="7ca7f-107">Klik på Varedisponering.</span><span class="sxs-lookup"><span data-stu-id="7ca7f-107">Click Master planning.</span></span>
    * <span data-ttu-id="7ca7f-108">Det findes på standarddashboardet.</span><span class="sxs-lookup"><span data-stu-id="7ca7f-108">You'll find this on the default dashboard.</span></span>  
2. <span data-ttu-id="7ca7f-109">Indtast eller vælg en værdi i feltet Plan.</span><span class="sxs-lookup"><span data-stu-id="7ca7f-109">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="7ca7f-110">Eksempel: StaticPlan</span><span class="sxs-lookup"><span data-stu-id="7ca7f-110">Example: StaticPlan</span></span>  
3. <span data-ttu-id="7ca7f-111">Klik på Kør.</span><span class="sxs-lookup"><span data-stu-id="7ca7f-111">Click Run.</span></span>
4. <span data-ttu-id="7ca7f-112">Vælg Ja i feltet Spor behandlingstidspunkt.</span><span class="sxs-lookup"><span data-stu-id="7ca7f-112">Select Yes in the Track processing time field.</span></span>
    * <span data-ttu-id="7ca7f-113">Hvis feltet allerede er markeret, skal du springe over dette trin.</span><span class="sxs-lookup"><span data-stu-id="7ca7f-113">If the field is already selected, skip this step.</span></span>  
5. <span data-ttu-id="7ca7f-114">Indtast et antal i feltet Antal tråde.</span><span class="sxs-lookup"><span data-stu-id="7ca7f-114">In the Number of threads field, enter a number.</span></span>
6. <span data-ttu-id="7ca7f-115">Udvid posterne for at inkludere sektion.</span><span class="sxs-lookup"><span data-stu-id="7ca7f-115">Expand the Records to include section.</span></span>
7. <span data-ttu-id="7ca7f-116">Klik på Filtrér.</span><span class="sxs-lookup"><span data-stu-id="7ca7f-116">Click Filter.</span></span>
8. <span data-ttu-id="7ca7f-117">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="7ca7f-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="7ca7f-118">Marker rækken, hvor feltet = Varenummer.</span><span class="sxs-lookup"><span data-stu-id="7ca7f-118">Mark the row where Field = Item number.</span></span>  
9. <span data-ttu-id="7ca7f-119">Indtast eller vælg en værdi i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="7ca7f-119">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="7ca7f-120">Eksempel: T0001</span><span class="sxs-lookup"><span data-stu-id="7ca7f-120">Example: T0001</span></span>  
10. <span data-ttu-id="7ca7f-121">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="7ca7f-121">Click OK.</span></span>
11. <span data-ttu-id="7ca7f-122">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="7ca7f-122">Click OK.</span></span>

## <a name="monitor-the-master-planning-run"></a><span data-ttu-id="7ca7f-123">Overvåge kørslen af varedisponering</span><span class="sxs-lookup"><span data-stu-id="7ca7f-123">Monitor the master planning run</span></span>
1. <span data-ttu-id="7ca7f-124">Klik på Historik.</span><span class="sxs-lookup"><span data-stu-id="7ca7f-124">Click History.</span></span>
2. <span data-ttu-id="7ca7f-125">Klik på Forespørgsler.</span><span class="sxs-lookup"><span data-stu-id="7ca7f-125">Click Inquiries.</span></span>
3. <span data-ttu-id="7ca7f-126">Klik på Procesopgavens varighed.</span><span class="sxs-lookup"><span data-stu-id="7ca7f-126">Click Process task duration.</span></span>
4. <span data-ttu-id="7ca7f-127">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="7ca7f-127">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="7ca7f-128">For hver vare kan du få et overblik over, hvor lang tid det tog at fuldføre hvert trin i planlægningen.</span><span class="sxs-lookup"><span data-stu-id="7ca7f-128">For each item you can get an overview of how long it took to complete each planning step.</span></span>  

