---
title: Tilføje en foregående aktivitet til en produktionsflowversion
description: Alle aktiviteter skal angives i rækkefølge i en produktionsflowversion.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a9b761e61bf6a810da9258870e9a994da4ced125
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981425"
---
# <a name="add-a-predecessor-to-a-production-flow-activity"></a><span data-ttu-id="95d77-103">Tilføje en foregående aktivitet til en produktionsflowversion</span><span class="sxs-lookup"><span data-stu-id="95d77-103">Add a predecessor to a production flow activity</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="95d77-104">Alle aktiviteter skal angives i rækkefølge i en produktionsflowversion.</span><span class="sxs-lookup"><span data-stu-id="95d77-104">In a production flow version, all activities must be sequenced.</span></span> <span data-ttu-id="95d77-105">En aktivitet kan have en eller flere foregående eller efterfølgende opgaver.</span><span class="sxs-lookup"><span data-stu-id="95d77-105">An activity can have one or multiple predecessors or successors.</span></span> 

<span data-ttu-id="95d77-106">Denne fremgangsmåde viser, hvordan du knytter en foregående opgave til en aktivitet.</span><span class="sxs-lookup"><span data-stu-id="95d77-106">This procedure shows how to associate a predecessor to an activity.</span></span> 

<span data-ttu-id="95d77-107">Hvis du vil udføre denne opgave, skal du bruge et produktionsflow, der har kladdeversionen med mindst to aktiviteter, som kan forbindes.</span><span class="sxs-lookup"><span data-stu-id="95d77-107">To perform this task, you need a production flow that has the Draft version with at least two activities that can be connected.</span></span> 

<span data-ttu-id="95d77-108">Du kan få mere at vide ved at læse hvidbogen "Production flows and activities in lean manufacturing".</span><span class="sxs-lookup"><span data-stu-id="95d77-108">To learn more, read the white paper "Production flows and activities in lean manufacturing."</span></span>


## <a name="find-the-production-flow-and-version"></a><span data-ttu-id="95d77-109">Find produktionsflow og -version</span><span class="sxs-lookup"><span data-stu-id="95d77-109">Find the production flow and version</span></span>
1. <span data-ttu-id="95d77-110">Gå til Produktionsstyring > Opsætning > Lean produktionsflow > Produktionsflow.</span><span class="sxs-lookup"><span data-stu-id="95d77-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="95d77-111">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="95d77-111">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="95d77-112">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="95d77-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="95d77-113">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="95d77-113">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="95d77-114">Klik på Aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="95d77-114">Click Activities.</span></span>

## <a name="select-an-activity-and-add-a-predecessor"></a><span data-ttu-id="95d77-115">Vælg en aktivitet, og tilføj en foregående opgave</span><span class="sxs-lookup"><span data-stu-id="95d77-115">Select an activity and add a predecessor</span></span>
1. <span data-ttu-id="95d77-116">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="95d77-116">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="95d77-117">Klik på Tilføj foregående aktivitet.</span><span class="sxs-lookup"><span data-stu-id="95d77-117">Click Add predecessor.</span></span>
3. <span data-ttu-id="95d77-118">Indtast eller vælg en værdi i feltet Aktivitet.</span><span class="sxs-lookup"><span data-stu-id="95d77-118">In the Activity field, enter or select a value.</span></span>
4. <span data-ttu-id="95d77-119">Angiv et tal i feltet Procestidsforhold.</span><span class="sxs-lookup"><span data-stu-id="95d77-119">In the Cycle time ratio field, enter a number.</span></span>
    * <span data-ttu-id="95d77-120">Standardprocestidsforholdet for en aktivitetsrelation er 1.</span><span class="sxs-lookup"><span data-stu-id="95d77-120">The default cycle time ratio of an activity relation is 1.</span></span> <span data-ttu-id="95d77-121">Dette forudsætter, at begge aktiviteter kører i samme tempo eller takttid.</span><span class="sxs-lookup"><span data-stu-id="95d77-121">This assumes that both activities run at the same pace or takt time.</span></span> <span data-ttu-id="95d77-122">Hvis den foregående opgave kører i et højere tempo (lavere takttid), skal forholdet være mindre end 1, hvis den foregående opgave kører i et langsommere tempo (højere takttid) og procestidsforholdet er større end 1.</span><span class="sxs-lookup"><span data-stu-id="95d77-122">If the predecessor runs at a higher pace (lower takt time), the ratio should be lower than 1, if the predecessor runs at a slower pace (higher takt time) the cycle time ratio is greater than 1.</span></span>  
5. <span data-ttu-id="95d77-123">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="95d77-123">Click OK.</span></span>

