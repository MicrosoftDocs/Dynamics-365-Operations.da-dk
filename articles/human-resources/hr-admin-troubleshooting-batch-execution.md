---
title: Nulstille fastsiddende batchjob
description: Dette emne indeholder en forklaring på, hvordan du kan løse problemer med batchjob, der er fastlåst.
author: andreabichsel
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: 906a391b3c28d15445f6ddf0fc547ebcf842ba19
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881754"
---
# <a name="reset-stuck-batch-jobs"></a><span data-ttu-id="6b8f9-103">Nulstille fastsiddende batchjob</span><span class="sxs-lookup"><span data-stu-id="6b8f9-103">Reset stuck batch jobs</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="issue"></a><span data-ttu-id="6b8f9-104">Udsted</span><span class="sxs-lookup"><span data-stu-id="6b8f9-104">Issue</span></span>

<span data-ttu-id="6b8f9-105">Microsoft Dynamics 365 Human Resources kan opleve problemer med batchjob, der enten sidder fast i tilstanden **Udfører** eller **Annullering**, og som ikke fuldføres.</span><span class="sxs-lookup"><span data-stu-id="6b8f9-105">Microsoft Dynamics 365 Human Resources can experience issues with batch jobs that are stuck in either an **Executing** or **Canceling** state and don't complete.</span></span>

## <a name="resolution"></a><span data-ttu-id="6b8f9-106">Løsning</span><span class="sxs-lookup"><span data-stu-id="6b8f9-106">Resolution</span></span>

<span data-ttu-id="6b8f9-107">Når et batchjob sidder fast i tilstanden **Udfører** eller **Annullerer**, kan du nulstille statussen ved at gennemtvinge annulleringen af jobbet.</span><span class="sxs-lookup"><span data-stu-id="6b8f9-107">When a batch job is stuck in an **Executing** or **Canceling** state, you can reset the status by forcing the cancellation of the job.</span></span> <span data-ttu-id="6b8f9-108">Når du har annulleret det, kan du nulstille batchjobbet ved at indstille det til **Venter**-status.</span><span class="sxs-lookup"><span data-stu-id="6b8f9-108">After you cancel it, you can reset the batch job by setting it to a **Waiting** status.</span></span> <span data-ttu-id="6b8f9-109">Det opsamles derefter igen for udførelse i næste planlagte batchkørsel.</span><span class="sxs-lookup"><span data-stu-id="6b8f9-109">It will then be picked up again for execution in the next scheduled batch run.</span></span>

1. <span data-ttu-id="6b8f9-110">Vælg siden **Links** i arbejdsområdet til **Systemadministration**, og vælg **Batchjob**.</span><span class="sxs-lookup"><span data-stu-id="6b8f9-110">In the **System administration** workspace, select the **Links** page, and select **Batch jobs**.</span></span>

2. <span data-ttu-id="6b8f9-111">Vælg det job, der skal nulstilles, på listesiden **Batchjob**.</span><span class="sxs-lookup"><span data-stu-id="6b8f9-111">On the **Batch job** list page, select the job that needs to be reset.</span></span>

3. <span data-ttu-id="6b8f9-112">Vælg **Gennemtving annullering** på handlingsbåndet, og bekræft handlingen.</span><span class="sxs-lookup"><span data-stu-id="6b8f9-112">On the action ribbon, select **Force cancel**, and confirm the action.</span></span>

   > [!NOTE]
   > <span data-ttu-id="6b8f9-113">Handlingen **Gennemtving annullering** er kun tilgængelig, når det valgte batchjob har status af enten **Udfører** eller **Annullerer**, og der ikke kører nogen batchudførelses- eller annulleringsprocesser for jobbet.</span><span class="sxs-lookup"><span data-stu-id="6b8f9-113">The **Force cancel** action is only available when the selected batch job has a status of either **Executing** or **Canceling**, and no batch execution or cancellation processes are running for the job.</span></span>

4. <span data-ttu-id="6b8f9-114">Vælg **Skift status** på handlingsbåndet.</span><span class="sxs-lookup"><span data-stu-id="6b8f9-114">On the action ribbon, select **Change status**.</span></span>

5. <span data-ttu-id="6b8f9-115">Vælg **Venter** på siden **Vælg ny status**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="6b8f9-115">On the **Select new status** page, select **Waiting**, and then select **OK**.</span></span>

   ![Vælge en ny status for batchjob](./media/hr-admin-reset-batch-job-status.png)

## <a name="see-also"></a><span data-ttu-id="6b8f9-117">Se også</span><span class="sxs-lookup"><span data-stu-id="6b8f9-117">See also</span></span>

[<span data-ttu-id="6b8f9-118">Optimere ydeevnen ved at planlægge batchjob efter arbejdstid</span><span class="sxs-lookup"><span data-stu-id="6b8f9-118">Optimize performance by scheduling batch jobs after hours</span></span>](hr-admin-troubleshooting-batch-jobs.md)<br>
[<span data-ttu-id="6b8f9-119">Optimere ydeevnen med automatiske oprydningsopgaver</span><span class="sxs-lookup"><span data-stu-id="6b8f9-119">Optimize performance with auto cleanup tasks</span></span>](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
