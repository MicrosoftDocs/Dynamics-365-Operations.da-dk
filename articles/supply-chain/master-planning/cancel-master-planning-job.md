---
title: Annuller et varedisponeringsjob
description: I dette emne beskrives det, hvordan du kan annullere et aktivt planlægningsjob, der bruger den indbyggede planlægningsfunktion.
author: ChristianRytt
manager: tfehr
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace, ReqProcessList
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-12-16
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3d5dad766f4c01e993dd77dd762595b29208c6cb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5264740"
---
# <a name="cancel-a-master-planning-job"></a><span data-ttu-id="599b8-103">Annuller et varedisponeringsjob</span><span class="sxs-lookup"><span data-stu-id="599b8-103">Cancel a master planning job</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="599b8-104">I Microsoft Dynamics 365 Supply Chain Management er der flere muligheder for at annullere et varedisponeringsjob.</span><span class="sxs-lookup"><span data-stu-id="599b8-104">In Microsoft Dynamics 365 Supply Chain Management, there are multiple options for canceling a master planning job.</span></span> <span data-ttu-id="599b8-105">Du kan for eksempel annullere et varedisponeringsjob, hvis det er startet ved en fejltagelse eller kører længere tid end forventet, og du vil afslutte det.</span><span class="sxs-lookup"><span data-stu-id="599b8-105">For example, you may want to cancel a master planning job if it was started by mistake or is running longer than expected and you want to end it.</span></span> <span data-ttu-id="599b8-106">Den bedste måde at annullere et varedisponeringsjob på er ved hjælp af siden **Uafsluttede planlægningsprocesser**.</span><span class="sxs-lookup"><span data-stu-id="599b8-106">The best way to cancel a planning job is from  the **Unfinished planning processes** page.</span></span> <span data-ttu-id="599b8-107">Alternative indstillinger fra siderne **Batchjobs** og **Forbedrede batchjobs** bør kun bruges, hvis annullering af varedisponeringsjobbet fra siden **Uafsluttede planlægningsprocesser** ikke blev fuldført inden for få minutter.</span><span class="sxs-lookup"><span data-stu-id="599b8-107">Alternative options from the **Batch jobs** and **Batch jobs enhanced** pages should only be used if canceling the master planning job from the **Unfinished planning processes** page did not complete within a few minutes.</span></span>

## <a name="preferred-cancel-option"></a><span data-ttu-id="599b8-108">Foretrukket annulleringsindstilling</span><span class="sxs-lookup"><span data-stu-id="599b8-108">Preferred cancel option</span></span>
### <a name="cancel-master-planning-job-from-unfinished-planning-processes-page"></a><span data-ttu-id="599b8-109">Annuller varedisponeringsjob fra siden **Uafsluttede planlægningsprocesser**</span><span class="sxs-lookup"><span data-stu-id="599b8-109">Cancel master planning job from **Unfinished planning processes** page</span></span>
1. <span data-ttu-id="599b8-110">Gå til **Varedisponering > Forespørgsler og rapporter > Varedisponering > Uafsluttede planlægningsprocesser**.</span><span class="sxs-lookup"><span data-stu-id="599b8-110">Go to **Master planning > Inquiries and reports > Master planning > Unfinished planning processes**.</span></span>
2. <span data-ttu-id="599b8-111">Vælg linjen med den planlægningsproces, du vil annullere.</span><span class="sxs-lookup"><span data-stu-id="599b8-111">Select the line with the planning process that you want to cancel.</span></span>
3. <span data-ttu-id="599b8-112">Klik på **Annuller**.</span><span class="sxs-lookup"><span data-stu-id="599b8-112">Click **Cancel**.</span></span>

## <a name="additional-cancel-options"></a><span data-ttu-id="599b8-113">Flere annulleringsindstillinger</span><span class="sxs-lookup"><span data-stu-id="599b8-113">Additional cancel options</span></span>
<span data-ttu-id="599b8-114">Disse bør kun anvendes hvis annulleringen af varedisponeringsjobbet fra siden **Uafsluttede planlægningsprocesser** ikke blev fuldført inden for få minutter.</span><span class="sxs-lookup"><span data-stu-id="599b8-114">These should only be used if canceling the master planning job from the **Unfinished planning processes** page did not complete within a few minutes.</span></span>

### <a name="delete-master-planning-job-from-the-batch-jobs-page"></a><span data-ttu-id="599b8-115">Slet varedisponeringsjobbet fra siden **Batchjobs**</span><span class="sxs-lookup"><span data-stu-id="599b8-115">Delete master planning job from the **Batch jobs** page</span></span>
1. <span data-ttu-id="599b8-116">Gå til **Systemadministration > Forespørgsler > Batchjob**.</span><span class="sxs-lookup"><span data-stu-id="599b8-116">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="599b8-117">Vælg linjen med det planlægningsjob, du vil slette.</span><span class="sxs-lookup"><span data-stu-id="599b8-117">Select the line with the planning job that you want to delete.</span></span>
3. <span data-ttu-id="599b8-118">Klik på **Slet**.</span><span class="sxs-lookup"><span data-stu-id="599b8-118">Click **Delete**.</span></span>

### <a name="abort-master-planning-job-task-from-the-batch-jobs-enhanced-page"></a><span data-ttu-id="599b8-119">Afbryd opgaven varedisponeringsjob fra siden **Forbedrede batchjobs**</span><span class="sxs-lookup"><span data-stu-id="599b8-119">Abort master planning job task from the **Batch jobs enhanced** page</span></span>
1. <span data-ttu-id="599b8-120">Gå til **Systemadministration > Forespørgsler > Batchjob**.</span><span class="sxs-lookup"><span data-stu-id="599b8-120">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="599b8-121">Hvis job-ID'et ikke fremgår af listen, skal du klikke på **Skift til udvidet formular**, ellers skal du fortsætte med næste trin.</span><span class="sxs-lookup"><span data-stu-id="599b8-121">If the job ID is not shown in the list, click **Switch to enhanced form**, otherwise proceed with the next step.</span></span>
3. <span data-ttu-id="599b8-122">Åbn batchjobbet.</span><span class="sxs-lookup"><span data-stu-id="599b8-122">Open the batch job.</span></span> <span data-ttu-id="599b8-123">Klik på **Opgave-ID'et** for batchjobbet med de opgaver, du vil afslutte.</span><span class="sxs-lookup"><span data-stu-id="599b8-123">Click the **Job ID** for the batch job with tasks that you want to end.</span></span>
4. <span data-ttu-id="599b8-124">Vælg hvilke opgaver, der skal afsluttes, i **Batchopgaver**.</span><span class="sxs-lookup"><span data-stu-id="599b8-124">In **Batch tasks**, select the tasks to end.</span></span>
5. <span data-ttu-id="599b8-125">Klik på **Skift status**, vælg **Annuller**, og klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="599b8-125">Click **Change status**, choose **Canceling** and click **OK**.</span></span>
6. <span data-ttu-id="599b8-126">I oversigtspanelet **Batchopgaver** skal du klikke på **Afbryd**.</span><span class="sxs-lookup"><span data-stu-id="599b8-126">On the **Batch tasks** FastTab, click **Abort**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]