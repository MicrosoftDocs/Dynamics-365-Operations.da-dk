---
title: Konfigurer og kør jobbet for at bogføre opgørelser
description: Denne procedure hjælper med at konfigurere og køre et tilbagevendende batchjob for at bogføre opgørelser for en valgt butik eller butiksgruppe.
author: josaw1
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2b1401d51491205731843abe6e2278f798c5c979
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232731"
---
# <a name="configure-and-run-job-to-post-statements"></a><span data-ttu-id="46dab-103">Konfigurer og kør jobbet for at bogføre opgørelser</span><span class="sxs-lookup"><span data-stu-id="46dab-103">Configure and run job to post statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="46dab-104">Denne procedure hjælper med at konfigurere og køre et tilbagevendende batchjob for at bogføre opgørelser for en valgt butik eller butiksgruppe.</span><span class="sxs-lookup"><span data-stu-id="46dab-104">This procedure walks through configuring and running a recurrent batch job to post statements for a selected store or group of stores.</span></span> <span data-ttu-id="46dab-105">Denne procedure bruger USRT-firmaets demodata.</span><span class="sxs-lookup"><span data-stu-id="46dab-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="46dab-106">Gå til Alle arbejdsområder > ..</span><span class="sxs-lookup"><span data-stu-id="46dab-106">Go to All workspaces > ..</span></span> <span data-ttu-id="46dab-107">> Butiksregnskab.</span><span class="sxs-lookup"><span data-stu-id="46dab-107">> Store financials.</span></span>
2. <span data-ttu-id="46dab-108">Klik på Bogfør opgørelse i batch.</span><span class="sxs-lookup"><span data-stu-id="46dab-108">Click Post statements in batch.</span></span>
    * <span data-ttu-id="46dab-109">Vælg et organisationshierarki, og vælg derefter enten en enkelt butik eller en node i organisationens nodetræ.</span><span class="sxs-lookup"><span data-stu-id="46dab-109">Select an organizational hierarchy and then in the organization nodes tree, select either an individual store or a node.</span></span> <span data-ttu-id="46dab-110">Vælg en node, hvis du vil oprette batchjobbet for en gruppe butikker.</span><span class="sxs-lookup"><span data-stu-id="46dab-110">Select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="46dab-111">Klik på pilen for at føje dit valg.</span><span class="sxs-lookup"><span data-stu-id="46dab-111">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="46dab-112">Klik på fanen Kør i baggrunden. ![Kør i baggrunden](../dev-itpro/media/runbackground.png "Kør i baggrunden")</span><span class="sxs-lookup"><span data-stu-id="46dab-112">Click the Run in the background tab. ![Run in the background](../dev-itpro/media/runbackground.png "Run in the background")</span></span> 
4. <span data-ttu-id="46dab-113">Markér eller fjern markeringen af afkrydsningsfeltet Batchbehandling.</span><span class="sxs-lookup"><span data-stu-id="46dab-113">Check or uncheck the Batch processing checkbox.</span></span>
<span data-ttu-id="46dab-114">![Batchbehandling](../dev-itpro/media/batchprocessing.png "Batchbehandling og gentagelse")</span><span class="sxs-lookup"><span data-stu-id="46dab-114">![Batch Processing](../dev-itpro/media/batchprocessing.png "Batch Processing & Recurrance")</span></span> 
5. <span data-ttu-id="46dab-115">Klik på Gentagelse.</span><span class="sxs-lookup"><span data-stu-id="46dab-115">Click Recurrence.</span></span>
6. <span data-ttu-id="46dab-116">Angiv en dato i feltet Startdato.</span><span class="sxs-lookup"><span data-stu-id="46dab-116">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="46dab-117">Angiv et tidspunkt i feltet Starttidspunkt.</span><span class="sxs-lookup"><span data-stu-id="46dab-117">In the Start time field, enter a time.</span></span>
    * <span data-ttu-id="46dab-118">Vælg, om du vil afslutte gentagelsen efter et bestemt antal kørsler, på en bestemt dato eller aldrig.</span><span class="sxs-lookup"><span data-stu-id="46dab-118">Choose whether you want to end the recurrence after a specific number of runs, at a specific date, or never.</span></span> <span data-ttu-id="46dab-119">Derefter skal du vælge forskellige indstillinger for at definere, hvor ofte jobbet skal køre.</span><span class="sxs-lookup"><span data-stu-id="46dab-119">Then choose the various options to define how frequently you want the job to run.</span></span>  
8. <span data-ttu-id="46dab-120">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="46dab-120">Click OK.</span></span>
9. <span data-ttu-id="46dab-121">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="46dab-121">Click OK.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]