---
title: Oprette et batchjob
description: Et batchjob er en gruppe opgaver, der sendes til en AOS-forekomst (applikationsobjektserver) til automatisk behandling.
author: maertenm
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d211dcd7cb47df135d395d2a993429746aa35a85
ms.sourcegitcommit: 6ba4006fb6a67ddd4b1e54e3d62b9d1239b5e5a3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/21/2019
ms.locfileid: "1700835"
---
# <a name="create-a-batch-job"></a><span data-ttu-id="c7bec-103">Oprette et batchjob</span><span class="sxs-lookup"><span data-stu-id="c7bec-103">Create a batch job</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c7bec-104">Et batchjob er en gruppe opgaver, der sendes til en AOS-forekomst (applikationsobjektserver) til automatisk behandling.</span><span class="sxs-lookup"><span data-stu-id="c7bec-104">A batch job is a group of tasks that are submitted to an Application Object Server (AOS) instance for automatic processing.</span></span> <span data-ttu-id="c7bec-105">Batchjob køres ved hjælp af sikkerhedslegitimationsoplysningerne for den bruger, der har oprettet jobbet.</span><span class="sxs-lookup"><span data-stu-id="c7bec-105">Batch jobs are run by using the security credentials of the user who created the job.</span></span> <span data-ttu-id="c7bec-106">Du kan bruge følgende procedure for at oprette et batchjob.</span><span class="sxs-lookup"><span data-stu-id="c7bec-106">Use the following procedure to create a batch job.</span></span> <span data-ttu-id="c7bec-107">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="c7bec-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-the-batch-job"></a><span data-ttu-id="c7bec-108">Opret batchjobbet</span><span class="sxs-lookup"><span data-stu-id="c7bec-108">Create the batch job</span></span>
1. <span data-ttu-id="c7bec-109">Gå til **Navigationsrude > Moduler > Systemadministration > Forespørgsler > Batchjob**.</span><span class="sxs-lookup"><span data-stu-id="c7bec-109">Go to **Navigation pane > Modules > System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="c7bec-110">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c7bec-110">Click **New**.</span></span>
3. <span data-ttu-id="c7bec-111">Indtast en værdi i feltet **Stillingsbeskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="c7bec-111">In the **Job description** field, type a value.</span></span>
4. <span data-ttu-id="c7bec-112">Angiv en dato og et klokkeslæt i feltet **Planlagt startdato/-klokkeslæt**.</span><span class="sxs-lookup"><span data-stu-id="c7bec-112">In the **Scheduled start date/time** field, enter a date and time.</span></span>
5. <span data-ttu-id="c7bec-113">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="c7bec-113">Click **Save**.</span></span>

## <a name="create-a-recurrence"></a><span data-ttu-id="c7bec-114">Opret en gentagelse</span><span class="sxs-lookup"><span data-stu-id="c7bec-114">Create a recurrence</span></span>
1. <span data-ttu-id="c7bec-115">Klik på **Batchjob** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="c7bec-115">On the Action Pane, click **Batch job**.</span></span>
2. <span data-ttu-id="c7bec-116">Klik på **Gentagelse**.</span><span class="sxs-lookup"><span data-stu-id="c7bec-116">Click **Recurrence**.</span></span> <span data-ttu-id="c7bec-117">Brug disse indstillinger til at angive et interval og mønster for gentagelsen.</span><span class="sxs-lookup"><span data-stu-id="c7bec-117">Use these options to enter a range and pattern for the recurrence.</span></span>  
3. <span data-ttu-id="c7bec-118">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="c7bec-118">Click **OK**.</span></span>

## <a name="add-alerts"></a><span data-ttu-id="c7bec-119">Tilføj beskeder</span><span class="sxs-lookup"><span data-stu-id="c7bec-119">Add alerts</span></span>
1. <span data-ttu-id="c7bec-120">Klik på **Batchjob** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="c7bec-120">On the Action Pane, click **Batch job**.</span></span>
2. <span data-ttu-id="c7bec-121">Klik på **Beskeder**.</span><span class="sxs-lookup"><span data-stu-id="c7bec-121">Click **Alerts**.</span></span> <span data-ttu-id="c7bec-122">Angiv, om der skal sendes meddelelser om påmindelser til dig, når batchjobbet afsluttes, støder på en fejl eller annulleres.</span><span class="sxs-lookup"><span data-stu-id="c7bec-122">Indicate if you want alert messages sent when the batch job ends, has an error, or is canceled.</span></span> <span data-ttu-id="c7bec-123">Angiv derefter, om der skal vises påmindelser som pop op-meddelelser.</span><span class="sxs-lookup"><span data-stu-id="c7bec-123">Then specify if you want the alerts to be displayed as pop-up messages.</span></span>   
3. <span data-ttu-id="c7bec-124">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="c7bec-124">Click **OK**.</span></span>

## <a name="adjust-batch-job-status"></a><span data-ttu-id="c7bec-125">Justere status for batchjob</span><span class="sxs-lookup"><span data-stu-id="c7bec-125">Adjust batch job status</span></span>
1. <span data-ttu-id="c7bec-126">Gå til **Systemadministration > Forespørgsler > Batchjob**.</span><span class="sxs-lookup"><span data-stu-id="c7bec-126">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="c7bec-127">Vælg det relevante batchjob.</span><span class="sxs-lookup"><span data-stu-id="c7bec-127">Select the appropriate batch job.</span></span>
3. <span data-ttu-id="c7bec-128">Klik på **Batchjob > Funktioner > Skift status** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="c7bec-128">On the Action Pane, click **Batch job > Functions > Change status**.</span></span>
4. <span data-ttu-id="c7bec-129">Vælg den relevante status:</span><span class="sxs-lookup"><span data-stu-id="c7bec-129">Select the appropriate status:</span></span>
    - <span data-ttu-id="c7bec-130">**Tilbagehold**: Angiv batchjobbet som **tilbageholdt**, så det tilbageholdes fra batchjobbets planlægger.</span><span class="sxs-lookup"><span data-stu-id="c7bec-130">**Withhold**: Set the batch job as **withhold** so it is withheld from the batch job scheduler.</span></span> <span data-ttu-id="c7bec-131">Svarer til *stop*.</span><span class="sxs-lookup"><span data-stu-id="c7bec-131">Equivalent to *stop*.</span></span>
    - <span data-ttu-id="c7bec-132">**Venter**: Angiv batchjobbet til **venter**, så det venter på at blive afhentet af batchjobbets planlægger.</span><span class="sxs-lookup"><span data-stu-id="c7bec-132">**Waiting**: Set the batch job as **waiting** so it is waiting to be picked up by the batch job scheduler.</span></span> <span data-ttu-id="c7bec-133">Svarer til *start*.</span><span class="sxs-lookup"><span data-stu-id="c7bec-133">Equivalent to *go*.</span></span>
5. <span data-ttu-id="c7bec-134">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="c7bec-134">Click **OK**.</span></span>
