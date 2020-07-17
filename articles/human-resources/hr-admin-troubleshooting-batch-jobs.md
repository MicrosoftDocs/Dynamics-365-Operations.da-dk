---
title: Optimere performance ved at planlægge batchjobs efter arbejdstid
description: Dette emne forklarer, hvordan du kan løse problemer med ydeevnen med Microsoft Dynamics 365 Human Resources ved at lægge batchjob, der kører i lang tid, efter arbejdstid.
author: andreabichsel
manager: AnnBe
ms.date: 06/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: f67b4b4c20345297f186c792fe2766c686e2ddbf
ms.sourcegitcommit: bdfc84aa7f607511981c0b2f20f03fabcb773510
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/23/2020
ms.locfileid: "3500499"
---
# <a name="optimize-performance-by-scheduling-batch-jobs-after-hours"></a><span data-ttu-id="5eca5-103">Optimere performance ved at planlægge batchjobs efter arbejdstid</span><span class="sxs-lookup"><span data-stu-id="5eca5-103">Optimize performance by scheduling batch jobs after hours</span></span>

## <a name="issue"></a><span data-ttu-id="5eca5-104">Udsted</span><span class="sxs-lookup"><span data-stu-id="5eca5-104">Issue</span></span>

<span data-ttu-id="5eca5-105">Microsoft Dynamics 365 Human Resources kan opleve problemer med ydeevnen, hvis batchjob, der kører i lang tid, køres i almindelig åbningstid.</span><span class="sxs-lookup"><span data-stu-id="5eca5-105">Microsoft Dynamics 365 Human Resources can experience performance issues if long-running batch jobs run during typical business hours.</span></span>

## <a name="resolution"></a><span data-ttu-id="5eca5-106">Løsning</span><span class="sxs-lookup"><span data-stu-id="5eca5-106">Resolution</span></span>

<span data-ttu-id="5eca5-107">Planlæg følgende batchjob til at blive kørt uden for arbejdstid.</span><span class="sxs-lookup"><span data-stu-id="5eca5-107">Schedule the following batch jobs during off hours.</span></span> <span data-ttu-id="5eca5-108">Det anbefales også, at du gennemgår hyppigheden af batchjob, der køres ofte.</span><span class="sxs-lookup"><span data-stu-id="5eca5-108">We also recommend reviewing the frequency of batch jobs that run frequently.</span></span> <span data-ttu-id="5eca5-109">Hvis det er muligt, skal du reducere gentagelsen af batchjobbet.</span><span class="sxs-lookup"><span data-stu-id="5eca5-109">If possible, reduce the recurrence of the batch job.</span></span> <span data-ttu-id="5eca5-110">I mange tilfælde er standardhyppigheden tilstrækkelig.</span><span class="sxs-lookup"><span data-stu-id="5eca5-110">In many cases, the default frequency is sufficient.</span></span>

<span data-ttu-id="5eca5-111">Følgende batchjob skal køre om natten eller efter arbejdstid.</span><span class="sxs-lookup"><span data-stu-id="5eca5-111">The following batch jobs should run at night or after hours.</span></span> <span data-ttu-id="5eca5-112">Sørg for at kontrollere tidszonen for disse tilbagevendende batchjob.</span><span class="sxs-lookup"><span data-stu-id="5eca5-112">Be sure to check the time zone for these recurring batch jobs.</span></span> <span data-ttu-id="5eca5-113">Nogle batchjob bruger muligvis Pacific Standard Time (PST).</span><span class="sxs-lookup"><span data-stu-id="5eca5-113">Some batch jobs might use Pacific Standard Time (PST).</span></span>

| <span data-ttu-id="5eca5-114">Batchjob</span><span class="sxs-lookup"><span data-stu-id="5eca5-114">Batch job</span></span> | <span data-ttu-id="5eca5-115">Standardforekomst</span><span class="sxs-lookup"><span data-stu-id="5eca5-115">Default occurrence</span></span> |
| --- | --- |
| <span data-ttu-id="5eca5-116">Oprydning i batchjobhistorik</span><span class="sxs-lookup"><span data-stu-id="5eca5-116">Batch job history cleanup</span></span> | <span data-ttu-id="5eca5-117">1 gang om måneden</span><span class="sxs-lookup"><span data-stu-id="5eca5-117">1 time per month</span></span> |
| <span data-ttu-id="5eca5-118">Oprydning i midlertidig placering for eksport</span><span class="sxs-lookup"><span data-stu-id="5eca5-118">Export staging cleanup</span></span> | <span data-ttu-id="5eca5-119">1 gang om dagen</span><span class="sxs-lookup"><span data-stu-id="5eca5-119">1 time per day</span></span> |
| <span data-ttu-id="5eca5-120">Manglende anmodning om synkronisering af Common Data Service-integration</span><span class="sxs-lookup"><span data-stu-id="5eca5-120">Common Data Service integration missed request sync</span></span> | <span data-ttu-id="5eca5-121">1 gang om dagen</span><span class="sxs-lookup"><span data-stu-id="5eca5-121">1 time per day</span></span> |
| <span data-ttu-id="5eca5-122">Systemjob til databasekomprimering, der skal køre regelmæssigt uden for arbejdstid</span><span class="sxs-lookup"><span data-stu-id="5eca5-122">Database compression system job that needs to run regularly during off hours</span></span> | <span data-ttu-id="5eca5-123">1 gang om dagen</span><span class="sxs-lookup"><span data-stu-id="5eca5-123">1 time per day</span></span> |
| <span data-ttu-id="5eca5-124">Systemjob til genopbygning af indeks, der skal køre regelmæssigt uden for arbejdstid</span><span class="sxs-lookup"><span data-stu-id="5eca5-124">Database index rebuild system job that needs to run regularly during off hours</span></span> | <span data-ttu-id="5eca5-125">1 gang om dagen</span><span class="sxs-lookup"><span data-stu-id="5eca5-125">1 time per day</span></span> |

1. <span data-ttu-id="5eca5-126">I Personale skal du vælge **Systemadministration**.</span><span class="sxs-lookup"><span data-stu-id="5eca5-126">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="5eca5-127">I panelet **Søg** skal du søge efter en af de ovennævnte kørsler.</span><span class="sxs-lookup"><span data-stu-id="5eca5-127">In the **Search** bar, search for one of the above batch jobs.</span></span>

3. <span data-ttu-id="5eca5-128">Vælg **Kør i baggrunden**, og vælg derefter **Gentagelse**.</span><span class="sxs-lookup"><span data-stu-id="5eca5-128">Select **Run in the background**, and then select **Recurrence**.</span></span>

   ![Angiv gentagelse](media/talent-batch-history-cleanup-recurrence.png)

4. <span data-ttu-id="5eca5-130">Under **Definer gentagelse** skal du angive **Startdato** og **Starttidspunkt**, der skal være uden for arbejdstiden eller i weekenden.</span><span class="sxs-lookup"><span data-stu-id="5eca5-130">Under **Define recurrence**, set the **Start date** and **Start time** to occur during off hours or the weekend.</span></span> <span data-ttu-id="5eca5-131">Vælg **Ingen slutdato**.</span><span class="sxs-lookup"><span data-stu-id="5eca5-131">Select **No end date**.</span></span> 

   ![Definer startdato og -tidspunkt for gentagelse](media/talent-batch-history-cleanup-define-recurrence.png)

5. <span data-ttu-id="5eca5-133">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="5eca5-133">Select **OK**.</span></span>

6. <span data-ttu-id="5eca5-134">Rediger andre parametre under **Kør i baggrunden** efter behov, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="5eca5-134">If needed, change any other parameters under **Run in the background**, and then select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5eca5-135">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="5eca5-135">Additional resources</span></span>

[<span data-ttu-id="5eca5-136">Optimere ydeevnen med automatiske oprydningsopgaver</span><span class="sxs-lookup"><span data-stu-id="5eca5-136">Optimize performance with auto cleanup tasks</span></span>](hr-admin-troubleshooting-batch-history.md)
