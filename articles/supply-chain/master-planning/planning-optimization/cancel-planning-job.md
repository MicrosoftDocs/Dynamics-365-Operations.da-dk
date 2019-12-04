---
title: Annullere et planlægningsjob
description: I dette emne beskrives det, hvordan du kan annullere et aktivt planlægningsjob, der bruger funktionen Planlægningsoptimering.
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: a2d90f04985fdd66ca83582ee676100fffb26981
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773928"
---
[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

# <a name="cancel-a-planning-job"></a><span data-ttu-id="9aa16-103">Annullere et planlægningsjob</span><span class="sxs-lookup"><span data-stu-id="9aa16-103">Cancel a planning job</span></span>

<span data-ttu-id="9aa16-104">I Microsoft Dynamics 365 Supply Chain Management kan du annullere et aktivt planlægningsjob, der bruger funktionen Planlægningsoptimering.</span><span class="sxs-lookup"><span data-stu-id="9aa16-104">In Microsoft Dynamics 365 Supply Chain Management, you can cancel an active planning job that uses the Planning Optimization functionality.</span></span>

<span data-ttu-id="9aa16-105">Benyt følgende fremgangsmåde for at annullere et aktivt planlægningsjob.</span><span class="sxs-lookup"><span data-stu-id="9aa16-105">To cancel an active planning job, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="9aa16-106">Kun aktive jobs kan annulleres.</span><span class="sxs-lookup"><span data-stu-id="9aa16-106">Only active jobs can be canceled.</span></span>

1. <span data-ttu-id="9aa16-107">Gå til **Varedisponering \> Opsætning \> Planer**.</span><span class="sxs-lookup"><span data-stu-id="9aa16-107">Go to **Master planning \> Setup \> Plans**.</span></span>
2. <span data-ttu-id="9aa16-108">Vælg den relevante plan for den planlagte kørsel.</span><span class="sxs-lookup"><span data-stu-id="9aa16-108">Select an appropriate plan for the planning run.</span></span>
3. <span data-ttu-id="9aa16-109">Vælg **Historik**.</span><span class="sxs-lookup"><span data-stu-id="9aa16-109">Select **History**.</span></span>
4. <span data-ttu-id="9aa16-110">Vælg det planlægningsjob, du vil annullere.</span><span class="sxs-lookup"><span data-stu-id="9aa16-110">Select the planning job to cancel.</span></span>
5. <span data-ttu-id="9aa16-111">Vælg **Annuller**.</span><span class="sxs-lookup"><span data-stu-id="9aa16-111">Select **Cancel**.</span></span>

<span data-ttu-id="9aa16-112">Jobstatussen angives til **Annulleres** indtil planlægningsoptimeringstjenesten bekræfter, at jobbet er blevet annulleret.</span><span class="sxs-lookup"><span data-stu-id="9aa16-112">The job status will be **Canceling** until the Planning Optimization service confirms that the job has been canceled.</span></span> <span data-ttu-id="9aa16-113">Statussen ændres derefter til **Annulleret**.</span><span class="sxs-lookup"><span data-stu-id="9aa16-113">The status will then be changed to **Canceled**.</span></span>

> [!NOTE]
> <span data-ttu-id="9aa16-114">Hvis du vil have vist statusændringerne, skal du opdatere siden ved at klikke på knappen **Opdater**.</span><span class="sxs-lookup"><span data-stu-id="9aa16-114">To see status changes, you must refresh the page by selecting the **Refresh** button.</span></span>

## <a name="related-resources"></a><span data-ttu-id="9aa16-115">Tilknyttede ressourcer</span><span class="sxs-lookup"><span data-stu-id="9aa16-115">Related resources</span></span>

[<span data-ttu-id="9aa16-116">Oversigt over Planlægningsoptimering</span><span class="sxs-lookup"><span data-stu-id="9aa16-116">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="9aa16-117">Introduktion til Planlægningsoptimering</span><span class="sxs-lookup"><span data-stu-id="9aa16-117">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="9aa16-118">Analyse af om Planlægningsoptimering passer til</span><span class="sxs-lookup"><span data-stu-id="9aa16-118">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="9aa16-119">Få vist planhistorik og planlægningslogs</span><span class="sxs-lookup"><span data-stu-id="9aa16-119">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="9aa16-120">Anvend filtre på en plan</span><span class="sxs-lookup"><span data-stu-id="9aa16-120">Apply filters to a plan</span></span>](plan-filters.md)
