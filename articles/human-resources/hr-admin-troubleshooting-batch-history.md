---
title: Optimere ydeevnen med automatiske oprydningsopgaver
description: Denne artikel forklarer, hvordan du kan løse problemer med ydeevnen af Microsoft Dynamics 365 Human Resources ved at rydde historikken for batchjob.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 6a9e94e282aa8f101b42c1378ef21c6c1fe0477e
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053485"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a><span data-ttu-id="39164-103">Optimere ydeevnen med automatiske oprydningsopgaver</span><span class="sxs-lookup"><span data-stu-id="39164-103">Optimize performance with auto cleanup tasks</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="39164-104">**Udsted**</span><span class="sxs-lookup"><span data-stu-id="39164-104">**Issue**</span></span>

<span data-ttu-id="39164-105">Microsoft Dynamics 365 Human Resources kan give problemer med ydeevnen, hvis historikken for batchjob bliver for stor.</span><span class="sxs-lookup"><span data-stu-id="39164-105">Microsoft Dynamics 365 Human Resources can experience performance issues if the batch job history grows too large.</span></span>

<span data-ttu-id="39164-106">**Årsag**</span><span class="sxs-lookup"><span data-stu-id="39164-106">**Cause**</span></span>

<span data-ttu-id="39164-107">Batchjob, der kører ofte, kan føre til en ikke-bæredygtig forøgelse af historikken for batchjob.</span><span class="sxs-lookup"><span data-stu-id="39164-107">Batch jobs that run frequently can lead to unsustainable growth of the batch job history.</span></span> <span data-ttu-id="39164-108">Dette kan forårsage problemer med ydeevnen.</span><span class="sxs-lookup"><span data-stu-id="39164-108">This can cause performance issues.</span></span> 

<span data-ttu-id="39164-109">**Løsning**</span><span class="sxs-lookup"><span data-stu-id="39164-109">**Resolution**</span></span>

<span data-ttu-id="39164-110">Planlæg en automatisk opgave for at rydde op i historikken for batchjob.</span><span class="sxs-lookup"><span data-stu-id="39164-110">Schedule an automatic task to clean up your batch job history.</span></span> <span data-ttu-id="39164-111">Vi anbefaler, at du konfigurerer opgaven til at køre ugentligt, men du kan blive nødt til at køre oprydningen mere eller mindre hyppigt, afhængigt af miljøet.</span><span class="sxs-lookup"><span data-stu-id="39164-111">We recommend setting up the task to run weekly, but you might need to run the cleanup more or less frequently, depending on your environment.</span></span> <span data-ttu-id="39164-112">Følgende procedure indeholder vores anbefalede indstillinger, men du kan ændre dem efter behov.</span><span class="sxs-lookup"><span data-stu-id="39164-112">The following procedure contains our recommended settings, but you can change these according to your needs.</span></span>

1. <span data-ttu-id="39164-113">I Human Resources skal du vælge **Systemadministration**.</span><span class="sxs-lookup"><span data-stu-id="39164-113">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="39164-114">På linjen **Søg** skal du indtaste **Oprydning i batchjobhistorik**.</span><span class="sxs-lookup"><span data-stu-id="39164-114">In the **Search** bar, enter **Batch job history clean-up**.</span></span>

   ![Søg efter oprydning af historik for batchjob](media/talent-batch-history-cleanup-search-bar.png)

3. <span data-ttu-id="39164-116">I **Historikgrænse (dage)** skal du skrive **30**.</span><span class="sxs-lookup"><span data-stu-id="39164-116">In **History limit (days)**, enter **30**.</span></span>

   ![Angiv historikgrænse til 30](media/talent-batch-history-cleanup-history-limit.png)

4. <span data-ttu-id="39164-118">Vælg **Kør i baggrunden**, og vælg derefter **Gentagelse**.</span><span class="sxs-lookup"><span data-stu-id="39164-118">Select **Run in the background** and then select **Recurrence**.</span></span>

   ![Angiv gentagelse](media/talent-batch-history-cleanup-recurrence.png)

5. <span data-ttu-id="39164-120">Under **Definer gentagelse** skal du angive **Startdato** og **Starttidspunkt**, der skal være uden for arbejdstiden eller i weekenden, og vælg derefter **Ingen slutdato**.</span><span class="sxs-lookup"><span data-stu-id="39164-120">Under **Define recurrence**, set the **Start date** and **Start time** to occur during off-hours or the weekend, and then select **NO END DATE**.</span></span> 

   ![Definer startdato og -tidspunkt for gentagelse](media/talent-batch-history-cleanup-define-recurrence.png)

6. <span data-ttu-id="39164-122">Vælg **Dage** under **Gentagelsesmønster**, og angiv **Gentag efter angivet interval** til **7**.</span><span class="sxs-lookup"><span data-stu-id="39164-122">Under **RECURRENCE PATTERN**, select **Days** and set **REPEAT AFTER SPECIFIED INTERVAL** to **7**.</span></span>

   ![Indstil oprydning til ugentlig gentagelse](media/talent-batch-history-cleanup-recurrence-pattern.png)

7. <span data-ttu-id="39164-124">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="39164-124">Select **OK**.</span></span>

8. <span data-ttu-id="39164-125">Rediger andre parametre under **Kør i baggrunden** efter behov, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="39164-125">Change any other parameters under **Run in the background** as necessary, and then select **OK**.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]