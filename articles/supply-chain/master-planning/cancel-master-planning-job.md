---
title: Annuller et varedisponeringsjob
description: I dette emne beskrives det, hvordan du kan annullere et aktivt planlægningsjob, der bruger den indbyggede planlægningsfunktion.
author: ChristianRytt
manager: tfehr
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-12-16
ms.dyn365.ops.version: ''
ms.openlocfilehash: 08dd612d9fb01ba2db6d4fcc7db9507a41a4b29f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203911"
---
# <a name="cancel-a-master-planning-job"></a><span data-ttu-id="91488-103">Annuller et varedisponeringsjob</span><span class="sxs-lookup"><span data-stu-id="91488-103">Cancel a master planning job</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="91488-104">I Microsoft Dynamics 365 Supply Chain Management er der flere muligheder for at annullere et varedisponeringsjob.</span><span class="sxs-lookup"><span data-stu-id="91488-104">In Microsoft Dynamics 365 Supply Chain Management, there are multiple options for canceling a master planning job.</span></span> <span data-ttu-id="91488-105">Du kan for eksempel annullere et varedisponeringsjob, hvis det er startet ved en fejltagelse eller kører længere tid end forventet, og du vil afslutte det.</span><span class="sxs-lookup"><span data-stu-id="91488-105">For example, you may want to cancel a master planning job if it was started by mistake or is running longer than expected and you want to end it.</span></span> <span data-ttu-id="91488-106">Den bedste måde at annullere et varedisponeringsjob på er ved hjælp af siden **Uafsluttede planlægningsprocesser**.</span><span class="sxs-lookup"><span data-stu-id="91488-106">The best way to cancel a planning job is from  the **Unfinished planning processes** page.</span></span> <span data-ttu-id="91488-107">Alternative indstillinger fra siderne **Batchjobs** og **Forbedrede batchjobs** bør kun bruges, hvis annullering af varedisponeringsjobbet fra siden **Uafsluttede planlægningsprocesser** ikke blev fuldført inden for få minutter.</span><span class="sxs-lookup"><span data-stu-id="91488-107">Alternative options from the **Batch jobs** and **Batch jobs enhanced** pages should only be used if canceling the master planning job from the **Unfinished planning processes** page did not complete within a few minutes.</span></span>

## <a name="preferred-cancel-option"></a><span data-ttu-id="91488-108">Foretrukket annulleringsindstilling</span><span class="sxs-lookup"><span data-stu-id="91488-108">Preferred cancel option</span></span>
### <a name="cancel-master-planning-job-from-unfinished-planning-processes-page"></a><span data-ttu-id="91488-109">Annuller varedisponeringsjob fra siden **Uafsluttede planlægningsprocesser**</span><span class="sxs-lookup"><span data-stu-id="91488-109">Cancel master planning job from **Unfinished planning processes** page</span></span>
1. <span data-ttu-id="91488-110">Gå til **Varedisponering > Forespørgsler og rapporter > Varedisponering > Uafsluttede planlægningsprocesser**.</span><span class="sxs-lookup"><span data-stu-id="91488-110">Go to **Master planning > Inquiries and reports > Master planning > Unfinished planning processes**.</span></span>
2. <span data-ttu-id="91488-111">Vælg linjen med den planlægningsproces, du vil annullere.</span><span class="sxs-lookup"><span data-stu-id="91488-111">Select the line with the planning process that you want to cancel.</span></span>
3. <span data-ttu-id="91488-112">Klik på **Annuller**.</span><span class="sxs-lookup"><span data-stu-id="91488-112">Click **Cancel**.</span></span>

## <a name="additional-cancel-options"></a><span data-ttu-id="91488-113">Flere annulleringsindstillinger</span><span class="sxs-lookup"><span data-stu-id="91488-113">Additional cancel options</span></span>
<span data-ttu-id="91488-114">Disse bør kun anvendes hvis annulleringen af varedisponeringsjobbet fra siden **Uafsluttede planlægningsprocesser** ikke blev fuldført inden for få minutter.</span><span class="sxs-lookup"><span data-stu-id="91488-114">These should only be used if canceling the master planning job from the **Unfinished planning processes** page did not complete within a few minutes.</span></span>

### <a name="delete-master-planning-job-from-the-batch-jobs-page"></a><span data-ttu-id="91488-115">Slet varedisponeringsjobbet fra siden **Batchjobs**</span><span class="sxs-lookup"><span data-stu-id="91488-115">Delete master planning job from the **Batch jobs** page</span></span>
1. <span data-ttu-id="91488-116">Gå til **Systemadministration > Forespørgsler > Batchjob**.</span><span class="sxs-lookup"><span data-stu-id="91488-116">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="91488-117">Vælg linjen med det planlægningsjob, du vil slette.</span><span class="sxs-lookup"><span data-stu-id="91488-117">Select the line with the planning job that you want to delete.</span></span>
3. <span data-ttu-id="91488-118">Klik på **Slet**.</span><span class="sxs-lookup"><span data-stu-id="91488-118">Click **Delete**.</span></span>

### <a name="abort-master-planning-job-task-from-the-batch-jobs-enhanced-page"></a><span data-ttu-id="91488-119">Afbryd opgaven varedisponeringsjob fra siden **Forbedrede batchjobs**</span><span class="sxs-lookup"><span data-stu-id="91488-119">Abort master planning job task from the **Batch jobs enhanced** page</span></span>
1. <span data-ttu-id="91488-120">Gå til **Systemadministration > Forespørgsler > Batchjob**.</span><span class="sxs-lookup"><span data-stu-id="91488-120">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="91488-121">Hvis job-ID'et ikke fremgår af listen, skal du klikke på **Skift til udvidet formular**, ellers skal du fortsætte med næste trin.</span><span class="sxs-lookup"><span data-stu-id="91488-121">If the job ID is not shown in the list, click **Switch to enhanced form**, otherwise proceed with the next step.</span></span>
3. <span data-ttu-id="91488-122">Åbn batchjobbet.</span><span class="sxs-lookup"><span data-stu-id="91488-122">Open the batch job.</span></span> <span data-ttu-id="91488-123">Klik på **Opgave-ID'et** for batchjobbet med de opgaver, du vil afslutte.</span><span class="sxs-lookup"><span data-stu-id="91488-123">Click the **Job ID** for the batch job with tasks that you want to end.</span></span>
4. <span data-ttu-id="91488-124">Vælg hvilke opgaver, der skal afsluttes, i **Batchopgaver**.</span><span class="sxs-lookup"><span data-stu-id="91488-124">In **Batch tasks**, select the tasks to end.</span></span>
5. <span data-ttu-id="91488-125">I oversigtspanelet **Batchopgaver** skal du klikke på **Afbryd**.</span><span class="sxs-lookup"><span data-stu-id="91488-125">On the **Batch tasks** FastTab, click **Abort**.</span></span>
