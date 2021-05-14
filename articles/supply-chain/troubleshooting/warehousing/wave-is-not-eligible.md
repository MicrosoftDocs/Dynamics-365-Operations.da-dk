---
title: Bølge er ikke berettiget til oprydning
description: Bølge er ikke berettiget til oprydning
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWaveTable_WHSWaveProcessingDataCleanup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3e5142cf40a6c0d308e8e952bbe17e85b498826d
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924321"
---
# <a name="wave-isnt-eligible-for-cleanup"></a><span data-ttu-id="f85c4-103">Bølge er ikke berettiget til oprydning</span><span class="sxs-lookup"><span data-stu-id="f85c4-103">Wave isn't eligible for cleanup</span></span>

<span data-ttu-id="f85c4-104">Fejlkode: WaveNotEligibleForCleanup</span><span class="sxs-lookup"><span data-stu-id="f85c4-104">Error code: WaveNotEligibleForCleanup</span></span>

## <a name="symptoms"></a><span data-ttu-id="f85c4-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="f85c4-105">Symptoms</span></span>

<span data-ttu-id="f85c4-106">Systemet viser følgende fejlmeddelelse:</span><span class="sxs-lookup"><span data-stu-id="f85c4-106">The system shows the following error message:</span></span>

> <span data-ttu-id="f85c4-107">Bølge %1 er ikke berettiget til oprydning.</span><span class="sxs-lookup"><span data-stu-id="f85c4-107">Wave %1 is not eligible for cleanup.</span></span>

<span data-ttu-id="f85c4-108">Du kan ikke rydde op i bølgedataene.</span><span class="sxs-lookup"><span data-stu-id="f85c4-108">The wave data can't be cleaned up.</span></span>  

## <a name="cause"></a><span data-ttu-id="f85c4-109">Årsag</span><span class="sxs-lookup"><span data-stu-id="f85c4-109">Cause</span></span>

<span data-ttu-id="f85c4-110">Bølgen behandles i øjeblikket som angivet med en af følgende forhold:</span><span class="sxs-lookup"><span data-stu-id="f85c4-110">The wave is currently being processed, as indicated by one of the following conditions:</span></span>

- <span data-ttu-id="f85c4-111">Feltet **Bølgestatus** er angivet til *Udfører*.</span><span class="sxs-lookup"><span data-stu-id="f85c4-111">The **Wave status** field is set to *Executing*.</span></span>
- <span data-ttu-id="f85c4-112">Når du vælger **Batchjob** i gruppen **Bølge** under fanen **Bølge** i handlingsruden, er feltet **Status** ikke angivet til *Afsluttet*, *Fejl* eller *Annulleret*.</span><span class="sxs-lookup"><span data-stu-id="f85c4-112">When you select **Batch job** in the **Wave** group on the **Wave** tab of the Action Pane, the **Status** field isn't set to *Ended*, *Error*, or *Canceled*.</span></span> <span data-ttu-id="f85c4-113">Derfor kører der aktuelt et batchjob.</span><span class="sxs-lookup"><span data-stu-id="f85c4-113">Therefore, a batch job is currently running.</span></span>

## <a name="resolution"></a><span data-ttu-id="f85c4-114">Løsning</span><span class="sxs-lookup"><span data-stu-id="f85c4-114">Resolution</span></span>

<span data-ttu-id="f85c4-115">Vælg **Batchjob** i gruppen **Bølge** under fanen **Bølge** i handlingsruden, og benyt derefter en af følgende fremgangsmåder:</span><span class="sxs-lookup"><span data-stu-id="f85c4-115">On the Action Pane, on the **Wave** tab, in the **Wave** group, select **Batch job**, and then follow one of these steps:</span></span>

- <span data-ttu-id="f85c4-116">Hvis feltet **Status** er angivet til *Udfører*: Vælg **Vis opgaver** i gruppen **Batchjob** under fanen **Batchjob** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="f85c4-116">If the **Status** field is set to *Executing*: On the Action Pane, on the **Batch job** tab, in the **Batch job** group, select **View tasks**.</span></span> <span data-ttu-id="f85c4-117">Du kan følge status ved at opdatere siden **Batchopgaver**.</span><span class="sxs-lookup"><span data-stu-id="f85c4-117">You can follow the progress by refreshing the **Batch tasks** page.</span></span>
- <span data-ttu-id="f85c4-118">Hvis feltet **Status** ikke er angivet til *Udfører*: Vælg **Skift status** i gruppen **Funktioner** under fanen **Batchjob** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="f85c4-118">If the **Status** field isn't set to *Executing*: On the Action Pane, on the **Batch job** tab, in the **Functions** group, select **Change status**.</span></span> <span data-ttu-id="f85c4-119">Vælg **Venter** i feltet *Vælg ny status*.</span><span class="sxs-lookup"><span data-stu-id="f85c4-119">In the **Select new status** field, select *Waiting*.</span></span> <span data-ttu-id="f85c4-120">Vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="f85c4-120">Then select **OK**.</span></span>
