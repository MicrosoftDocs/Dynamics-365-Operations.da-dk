---
title: Annullere et planlægningsjob
description: I dette emne beskrives det, hvordan du kan annullere et aktivt planlægningsjob, der bruger funktionen Planlægningsoptimering.
author: ChristianRytt
manager: AnnBe
ms.date: 02/18/2020
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
ms.openlocfilehash: 18c5c7b8030fc6adbc548dab750e4f454aebc867
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076337"
---
# <a name="cancel-a-planning-job"></a><span data-ttu-id="a759e-103">Annullere et planlægningsjob</span><span class="sxs-lookup"><span data-stu-id="a759e-103">Cancel a planning job</span></span>

[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="a759e-104">I Microsoft Dynamics 365 Supply Chain Management kan du annullere et aktivt planlægningsjob, der bruger funktionen Planlægningsoptimering.</span><span class="sxs-lookup"><span data-stu-id="a759e-104">In Microsoft Dynamics 365 Supply Chain Management, you can cancel an active planning job that uses the Planning optimization functionality.</span></span> <span data-ttu-id="a759e-105">Når du vælger **Annuller** i dialogboksen, når et planlægningsoptimeringsjob udløses direkte fra brugergrænsefladen (ikke i baggrunden), annullerer dette ikke planlægningsoptimeringsjobbet.</span><span class="sxs-lookup"><span data-stu-id="a759e-105">When you select **Cancel** in the dialog box when a Planning optimization job is triggered directly from the user interface (not in the background), this will not cancel the Planning optimization job.</span></span> <span data-ttu-id="a759e-106">Selvom du får vist en advarsel såsom "Handlingen er annulleret", skal du stadig bruge følgende trin for at annullere et planlægningsjob med planlægningsoptimering.</span><span class="sxs-lookup"><span data-stu-id="a759e-106">Even if you receive a warning such as “Operation canceled”, you will still need to use the following steps to cancel a planning job with Planning optimization.</span></span>


<span data-ttu-id="a759e-107">Benyt følgende fremgangsmåde for at annullere et aktivt planlægningsjob.</span><span class="sxs-lookup"><span data-stu-id="a759e-107">To cancel an active planning job, follow these steps.</span></span> 

> [!NOTE]
> <span data-ttu-id="a759e-108">Kun aktive jobs kan annulleres.</span><span class="sxs-lookup"><span data-stu-id="a759e-108">Only active jobs can be canceled.</span></span>

1. <span data-ttu-id="a759e-109">Gå til **Varedisponering \> Opsætning \> Planer**.</span><span class="sxs-lookup"><span data-stu-id="a759e-109">Go to **Master planning \> Setup \> Plans**.</span></span>
2. <span data-ttu-id="a759e-110">Vælg den relevante plan for den planlagte kørsel.</span><span class="sxs-lookup"><span data-stu-id="a759e-110">Select an appropriate plan for the planning run.</span></span>
3. <span data-ttu-id="a759e-111">Vælg **Historik**.</span><span class="sxs-lookup"><span data-stu-id="a759e-111">Select **History**.</span></span>
4. <span data-ttu-id="a759e-112">Vælg det planlægningsjob, du vil annullere.</span><span class="sxs-lookup"><span data-stu-id="a759e-112">Select the planning job to cancel.</span></span>
5. <span data-ttu-id="a759e-113">Vælg **Annuller**.</span><span class="sxs-lookup"><span data-stu-id="a759e-113">Select **Cancel**.</span></span>

<span data-ttu-id="a759e-114">Jobstatussen angives til **Annulleres** indtil planlægningsoptimeringstjenesten bekræfter, at jobbet er blevet annulleret.</span><span class="sxs-lookup"><span data-stu-id="a759e-114">The job status will be **Canceling** until the Planning Optimization service confirms that the job has been canceled.</span></span> <span data-ttu-id="a759e-115">Statussen ændres derefter til **Annulleret**.</span><span class="sxs-lookup"><span data-stu-id="a759e-115">The status will then be changed to **Canceled**.</span></span>

> [!NOTE]
> <span data-ttu-id="a759e-116">Hvis du vil have vist statusændringerne, skal du opdatere siden ved at klikke på knappen **Opdater**.</span><span class="sxs-lookup"><span data-stu-id="a759e-116">To see status changes, you must refresh the page by selecting the **Refresh** button.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a759e-117">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="a759e-117">Additional resources</span></span>

[<span data-ttu-id="a759e-118">Oversigt over planlægningsoptimering</span><span class="sxs-lookup"><span data-stu-id="a759e-118">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="a759e-119">Kom i gang med planlægningsoptimering</span><span class="sxs-lookup"><span data-stu-id="a759e-119">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="a759e-120">Analyse af om Planlægningsoptimering passer til</span><span class="sxs-lookup"><span data-stu-id="a759e-120">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="a759e-121">Få vist planhistorik og planlægningslogs</span><span class="sxs-lookup"><span data-stu-id="a759e-121">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="a759e-122">Anvend filtre på en plan</span><span class="sxs-lookup"><span data-stu-id="a759e-122">Apply filters to a plan</span></span>](plan-filters.md)
