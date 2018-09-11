--- 
title: "Tilføje en foregående aktivitet til en produktionsflowversion"
description: "Alle aktiviteter skal angives i rækkefølge i en produktionsflowversion."
author: cvocph
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 176dbf03dd4769c94da69910a4a1b1ac83b54df3
ms.contentlocale: da-dk
ms.lasthandoff: 09/11/2018

---
# <a name="add-a-predecessor-to-a-production-flow-activity"></a><span data-ttu-id="47007-103">Tilføje en foregående aktivitet til en produktionsflowversion</span><span class="sxs-lookup"><span data-stu-id="47007-103">Add a predecessor to a production flow activity</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="47007-104">Alle aktiviteter skal angives i rækkefølge i en produktionsflowversion.</span><span class="sxs-lookup"><span data-stu-id="47007-104">In a production flow version, all activities must be sequenced.</span></span> <span data-ttu-id="47007-105">En aktivitet kan have en eller flere foregående eller efterfølgende opgaver.</span><span class="sxs-lookup"><span data-stu-id="47007-105">An activity can have one or multiple predecessors or successors.</span></span> 

<span data-ttu-id="47007-106">Denne fremgangsmåde viser, hvordan du knytter en foregående opgave til en aktivitet.</span><span class="sxs-lookup"><span data-stu-id="47007-106">This procedure shows how to associate a predecessor to an activity.</span></span> 

<span data-ttu-id="47007-107">Hvis du vil udføre denne opgave, skal du bruge et produktionsflow, der har kladdeversionen med mindst to aktiviteter, som kan forbindes.</span><span class="sxs-lookup"><span data-stu-id="47007-107">To perform this task, you need a production flow that has the Draft version with at least two activities that can be connected.</span></span> 

<span data-ttu-id="47007-108">Du kan få mere at vide ved at læse hvidbogen "Production flows and activities in lean manufacturing".</span><span class="sxs-lookup"><span data-stu-id="47007-108">To learn more, read the white paper "Production flows and activities in lean manufacturing."</span></span>


## <a name="find-the-production-flow-and-version"></a><span data-ttu-id="47007-109">Find produktionsflow og -version</span><span class="sxs-lookup"><span data-stu-id="47007-109">Find the production flow and version</span></span>
1. <span data-ttu-id="47007-110">Gå til Produktionsstyring > Opsætning > Lean produktionsflow > Produktionsflow.</span><span class="sxs-lookup"><span data-stu-id="47007-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="47007-111">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="47007-111">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="47007-112">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="47007-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="47007-113">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="47007-113">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="47007-114">Klik på Aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="47007-114">Click Activities.</span></span>

## <a name="select-an-activity-and-add-a-predecessor"></a><span data-ttu-id="47007-115">Vælg en aktivitet, og tilføj en foregående opgave</span><span class="sxs-lookup"><span data-stu-id="47007-115">Select an activity and add a predecessor</span></span>
1. <span data-ttu-id="47007-116">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="47007-116">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="47007-117">Klik på Tilføj foregående aktivitet.</span><span class="sxs-lookup"><span data-stu-id="47007-117">Click Add predecessor.</span></span>
3. <span data-ttu-id="47007-118">Indtast eller vælg en værdi i feltet Aktivitet.</span><span class="sxs-lookup"><span data-stu-id="47007-118">In the Activity field, enter or select a value.</span></span>
4. <span data-ttu-id="47007-119">Angiv et tal i feltet Procestidsforhold.</span><span class="sxs-lookup"><span data-stu-id="47007-119">In the Cycle time ratio field, enter a number.</span></span>
    * <span data-ttu-id="47007-120">Standardprocestidsforholdet for en aktivitetsrelation er 1.</span><span class="sxs-lookup"><span data-stu-id="47007-120">The default cycle time ratio of an activity relation is 1.</span></span> <span data-ttu-id="47007-121">Dette forudsætter, at begge aktiviteter kører i samme tempo eller takttid.</span><span class="sxs-lookup"><span data-stu-id="47007-121">This assumes that both activities run at the same pace or takt time.</span></span> <span data-ttu-id="47007-122">Hvis den foregående opgave kører i et højere tempo (lavere takttid), skal forholdet være mindre end 1, hvis den foregående opgave kører i et langsommere tempo (højere takttid) og procestidsforholdet er større end 1.</span><span class="sxs-lookup"><span data-stu-id="47007-122">If the predecessor runs at a higher pace (lower takt time), the ratio should be lower than 1, if the predecessor runs at a slower pace (higher takt time) the cycle time ratio is greater than 1.</span></span>  
5. <span data-ttu-id="47007-123">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="47007-123">Click OK.</span></span>


