--- 
title: " Konfigurere og køre et job for at bogføre opgørelser"
description: "Denne procedure hjælper med at konfigurere og køre et tilbagevendende batchjob for at bogføre opgørelser for en valgt butik eller butiksgruppe."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0e2dae54cc9ccfc0a85046c5478e539585c3744d
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="configure-and-run-a-job-to-post-statements"></a><span data-ttu-id="9f70b-103"> Konfigurere og køre et job for at bogføre opgørelser</span><span class="sxs-lookup"><span data-stu-id="9f70b-103">Configure and run a job to post statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="9f70b-104">Denne procedure hjælper med at konfigurere og køre et tilbagevendende batchjob for at bogføre opgørelser for en valgt butik eller butiksgruppe.</span><span class="sxs-lookup"><span data-stu-id="9f70b-104">This procedure walks through configuring and running a recurrent batch job to post statements for a selected store or group of stores.</span></span> <span data-ttu-id="9f70b-105">Denne procedure bruger USRT-firmaets demodata.</span><span class="sxs-lookup"><span data-stu-id="9f70b-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="9f70b-106">Gå til Alle arbejdsområder > ..</span><span class="sxs-lookup"><span data-stu-id="9f70b-106">Go to All workspaces > ..</span></span> <span data-ttu-id="9f70b-107">> Detailbutiksregnskab.</span><span class="sxs-lookup"><span data-stu-id="9f70b-107">> Retail store financials.</span></span>
2. <span data-ttu-id="9f70b-108">Klik på Bogfør opgørelser.</span><span class="sxs-lookup"><span data-stu-id="9f70b-108">Click Post statements.</span></span>
    * <span data-ttu-id="9f70b-109">Vælg et organisationshierarki, og vælg derefter enten en enkelt butik eller en node i organisationens nodetræ.</span><span class="sxs-lookup"><span data-stu-id="9f70b-109">Select an organizational hierarchy and then in the organization nodes tree, select either an individual store or a node.</span></span> <span data-ttu-id="9f70b-110">Vælg en node, hvis du vil oprette batchjobbet for en gruppe butikker.</span><span class="sxs-lookup"><span data-stu-id="9f70b-110">Select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="9f70b-111">Klik på pilen for at føje dit valg.</span><span class="sxs-lookup"><span data-stu-id="9f70b-111">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="9f70b-112">Klik på fanen Kør i baggrunden.</span><span class="sxs-lookup"><span data-stu-id="9f70b-112">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="9f70b-113">Markér eller fjern markeringen af afkrydsningsfeltet Batchbehandling.</span><span class="sxs-lookup"><span data-stu-id="9f70b-113">Check or uncheck the Batch processing checkbox.</span></span>
5. <span data-ttu-id="9f70b-114">Klik på Gentagelse.</span><span class="sxs-lookup"><span data-stu-id="9f70b-114">Click Recurrence.</span></span>
6. <span data-ttu-id="9f70b-115">Angiv en dato i feltet Startdato.</span><span class="sxs-lookup"><span data-stu-id="9f70b-115">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="9f70b-116">Angiv et tidspunkt i feltet Starttidspunkt.</span><span class="sxs-lookup"><span data-stu-id="9f70b-116">In the Start time field, enter a time.</span></span>
    * <span data-ttu-id="9f70b-117">Vælg, om du vil afslutte gentagelsen efter et bestemt antal kørsler, på en bestemt dato eller aldrig.</span><span class="sxs-lookup"><span data-stu-id="9f70b-117">Choose whether you want to end the recurrence after a specific number of runs, at a specific date, or never.</span></span> <span data-ttu-id="9f70b-118">Derefter skal du vælge forskellige indstillinger for at definere, hvor ofte jobbet skal køre.</span><span class="sxs-lookup"><span data-stu-id="9f70b-118">Then choose the various options to define how frequently you want the job to run.</span></span>  
8. <span data-ttu-id="9f70b-119">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="9f70b-119">Click OK.</span></span>
9. <span data-ttu-id="9f70b-120">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="9f70b-120">Click OK.</span></span>


