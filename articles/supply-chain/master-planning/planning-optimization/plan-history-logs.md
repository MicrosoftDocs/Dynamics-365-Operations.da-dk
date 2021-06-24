---
title: Få vist planhistorik og planlægningslogs
description: Dette emne beskriver, hvordan du kan få vist historikken for planlægningsjobs, der udløses af funktionen Planlægningsoptimering.
author: ChristianRytt
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MPSPlanRegenerationJobList, MPSPlanRegenerationJobLogs
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: d7bba084b03f8698c8bf31d171d5e4e486ed06ad
ms.sourcegitcommit: a7649b361ec54b49c0e9ee1c1c63a8815f320225
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187241"
---
# <a name="view-plan-history-and-planning-logs"></a><span data-ttu-id="0be36-103">Få vist planhistorik og planlægningslogs</span><span class="sxs-lookup"><span data-stu-id="0be36-103">View plan history and planning logs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0be36-104">Dette emne beskriver, hvordan du kan få vist historikken for planlægningsjobs, der udløses af funktionen Planlægningsoptimering i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0be36-104">This topic explains how to view the history of planning jobs that are triggered by the Planning Optimization functionality in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="0be36-105">Hvis du vil have vist historikken for en plan, skal du åbne planen ved at gå til **Varedisponering** \> **Opsætning** \> **Planer** \> **Behovsplaner** og vælge **Historik**.</span><span class="sxs-lookup"><span data-stu-id="0be36-105">To view the history for a plan, open the plan by going to **Master planning** \> **Setup** \> **Plans** \> **Master plans** and selecting **History**.</span></span> <span data-ttu-id="0be36-106">Historikken viser alle job for den valgte plan.</span><span class="sxs-lookup"><span data-stu-id="0be36-106">The history lists all the jobs for the selected plan.</span></span> <span data-ttu-id="0be36-107">Listen omfatter afsluttede og aktive job.</span><span class="sxs-lookup"><span data-stu-id="0be36-107">The list includes completed and active jobs.</span></span>

<span data-ttu-id="0be36-108">Historikken for job til varedisponering i Planlægningsoptimering beholder kun 60 poster pr. behovsplan.</span><span class="sxs-lookup"><span data-stu-id="0be36-108">The history of jobs for Planning Optimization master planning runs keeps only up to 60 records per master plan.</span></span> <span data-ttu-id="0be36-109">Når du kører en ny beregning af varedisponering, slettes den tidligste historikpost for planen.</span><span class="sxs-lookup"><span data-stu-id="0be36-109">Whenever you run a new master planning calculation, that plan's earliest history record is deleted.</span></span>

<span data-ttu-id="0be36-110">Ud over at se starttidspunkt og status for job, kan du få vist loggen for et bestemt job.</span><span class="sxs-lookup"><span data-stu-id="0be36-110">In addition to seeing the start time and status of jobs, you can view the log for a specific job.</span></span> <span data-ttu-id="0be36-111">Loggen indeholder yderligere oplysninger og advarsler.</span><span class="sxs-lookup"><span data-stu-id="0be36-111">The log includes additional information and warnings.</span></span> <span data-ttu-id="0be36-112">Ikke alle job har en log.</span><span class="sxs-lookup"><span data-stu-id="0be36-112">Not all jobs have a log.</span></span> <span data-ttu-id="0be36-113">Hvis du vil have vist loggen for et job, skla du vælge **Log**.</span><span class="sxs-lookup"><span data-stu-id="0be36-113">To view the log for a job, select **Log**.</span></span> <span data-ttu-id="0be36-114">Logposter gemmes kun i 30 dage efter den dato, hvor jobbet er afsluttet, og derefter slettes de automatisk.</span><span class="sxs-lookup"><span data-stu-id="0be36-114">Log entries are only stored for 30 days after the date the job finished, after that they are automatically deleted.</span></span>

## <a name="related-resources"></a><span data-ttu-id="0be36-115">Tilknyttede ressourcer</span><span class="sxs-lookup"><span data-stu-id="0be36-115">Related resources</span></span>

- [<span data-ttu-id="0be36-116">Oversigt over planlægningsoptimering</span><span class="sxs-lookup"><span data-stu-id="0be36-116">Planning Optimization overview</span></span>](planning-optimization-overview.md)
- [<span data-ttu-id="0be36-117">Start her med planlægningsoptimering</span><span class="sxs-lookup"><span data-stu-id="0be36-117">Get started with Planning Optimization</span></span>](get-started.md)
- [<span data-ttu-id="0be36-118">Analyse af om Planlægningsoptimering passer til</span><span class="sxs-lookup"><span data-stu-id="0be36-118">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)
- [<span data-ttu-id="0be36-119">Anvend filtre på en plan</span><span class="sxs-lookup"><span data-stu-id="0be36-119">Apply filters to a plan</span></span>](plan-filters.md)
- [<span data-ttu-id="0be36-120">Annullere et planlægningsjob</span><span class="sxs-lookup"><span data-stu-id="0be36-120">Cancel a planning job</span></span>](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]