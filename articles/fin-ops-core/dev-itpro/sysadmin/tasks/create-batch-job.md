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
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4903724adc9deaa40b6cd04c215273dd4b0522d4
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982520"
---
# <a name="create-a-batch-job"></a><span data-ttu-id="6dd13-103">Oprette et batchjob</span><span class="sxs-lookup"><span data-stu-id="6dd13-103">Create a batch job</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6dd13-104">Et batchjob er en gruppe opgaver, der sendes til en AOS-forekomst (applikationsobjektserver) til automatisk behandling.</span><span class="sxs-lookup"><span data-stu-id="6dd13-104">A batch job is a group of tasks that are submitted to an Application Object Server (AOS) instance for automatic processing.</span></span> <span data-ttu-id="6dd13-105">Batchjob køres ved hjælp af sikkerhedslegitimationsoplysningerne for den bruger, der har oprettet jobbet.</span><span class="sxs-lookup"><span data-stu-id="6dd13-105">Batch jobs are run by using the security credentials of the user who created the job.</span></span> <span data-ttu-id="6dd13-106">Du kan bruge følgende procedure for at oprette et batchjob.</span><span class="sxs-lookup"><span data-stu-id="6dd13-106">Use the following procedure to create a batch job.</span></span> <span data-ttu-id="6dd13-107">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="6dd13-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-the-batch-job"></a><span data-ttu-id="6dd13-108">Opret batchjobbet</span><span class="sxs-lookup"><span data-stu-id="6dd13-108">Create the batch job</span></span>
1. <span data-ttu-id="6dd13-109">Gå til **Navigationsrude > Moduler > Systemadministration > Forespørgsler > Batchjob**.</span><span class="sxs-lookup"><span data-stu-id="6dd13-109">Go to **Navigation pane > Modules > System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="6dd13-110">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="6dd13-110">Click **New**.</span></span>
3. <span data-ttu-id="6dd13-111">Indtast en værdi i feltet **Stillingsbeskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="6dd13-111">In the **Job description** field, type a value.</span></span>
4. <span data-ttu-id="6dd13-112">Angiv en dato og et klokkeslæt i feltet **Planlagt startdato/-klokkeslæt**.</span><span class="sxs-lookup"><span data-stu-id="6dd13-112">In the **Scheduled start date/time** field, enter a date and time.</span></span>
5. <span data-ttu-id="6dd13-113">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="6dd13-113">Click **Save**.</span></span>

## <a name="create-a-recurrence"></a><span data-ttu-id="6dd13-114">Opret en gentagelse</span><span class="sxs-lookup"><span data-stu-id="6dd13-114">Create a recurrence</span></span>
1. <span data-ttu-id="6dd13-115">Klik på **Batchjob** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="6dd13-115">On the Action Pane, click **Batch job**.</span></span>
2. <span data-ttu-id="6dd13-116">Klik på **Gentagelse**.</span><span class="sxs-lookup"><span data-stu-id="6dd13-116">Click **Recurrence**.</span></span> <span data-ttu-id="6dd13-117">Brug disse indstillinger til at angive et interval og mønster for gentagelsen.</span><span class="sxs-lookup"><span data-stu-id="6dd13-117">Use these options to enter a range and pattern for the recurrence.</span></span>  
3. <span data-ttu-id="6dd13-118">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="6dd13-118">Click **OK**.</span></span>

## <a name="add-alerts"></a><span data-ttu-id="6dd13-119">Tilføj beskeder</span><span class="sxs-lookup"><span data-stu-id="6dd13-119">Add alerts</span></span>
1. <span data-ttu-id="6dd13-120">Klik på **Batchjob** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="6dd13-120">On the Action Pane, click **Batch job**.</span></span>
2. <span data-ttu-id="6dd13-121">Klik på **Beskeder**.</span><span class="sxs-lookup"><span data-stu-id="6dd13-121">Click **Alerts**.</span></span> <span data-ttu-id="6dd13-122">Angiv, om der skal sendes meddelelser om påmindelser til dig, når batchjobbet afsluttes, støder på en fejl eller annulleres.</span><span class="sxs-lookup"><span data-stu-id="6dd13-122">Indicate if you want alert messages sent when the batch job ends, has an error, or is canceled.</span></span> <span data-ttu-id="6dd13-123">Angiv derefter, om der skal vises påmindelser som pop op-meddelelser.</span><span class="sxs-lookup"><span data-stu-id="6dd13-123">Then specify if you want the alerts to be displayed as pop-up messages.</span></span>   
3. <span data-ttu-id="6dd13-124">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="6dd13-124">Click **OK**.</span></span>

## <a name="adjust-batch-job-status"></a><span data-ttu-id="6dd13-125">Justere status for batchjob</span><span class="sxs-lookup"><span data-stu-id="6dd13-125">Adjust batch job status</span></span>
1. <span data-ttu-id="6dd13-126">Gå til **Systemadministration > Forespørgsler > Batchjob**.</span><span class="sxs-lookup"><span data-stu-id="6dd13-126">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="6dd13-127">Vælg det relevante batchjob.</span><span class="sxs-lookup"><span data-stu-id="6dd13-127">Select the appropriate batch job.</span></span>
3. <span data-ttu-id="6dd13-128">Klik på **Batchjob > Funktioner > Skift status** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="6dd13-128">On the Action Pane, click **Batch job > Functions > Change status**.</span></span>
4. <span data-ttu-id="6dd13-129">Vælg den relevante status:</span><span class="sxs-lookup"><span data-stu-id="6dd13-129">Select the appropriate status:</span></span>
    - <span data-ttu-id="6dd13-130">**Tilbagehold**: Angiv batchjobbet som **tilbageholdt**, så det tilbageholdes fra batchjobbets planlægger.</span><span class="sxs-lookup"><span data-stu-id="6dd13-130">**Withhold**: Set the batch job as **withhold** so it is withheld from the batch job scheduler.</span></span> <span data-ttu-id="6dd13-131">Svarer til *stop*.</span><span class="sxs-lookup"><span data-stu-id="6dd13-131">Equivalent to *stop*.</span></span>
    - <span data-ttu-id="6dd13-132">**Venter**: Angiv batchjobbet til **venter**, så det venter på at blive afhentet af batchjobbets planlægger.</span><span class="sxs-lookup"><span data-stu-id="6dd13-132">**Waiting**: Set the batch job as **waiting** so it is waiting to be picked up by the batch job scheduler.</span></span> <span data-ttu-id="6dd13-133">Svarer til *start*.</span><span class="sxs-lookup"><span data-stu-id="6dd13-133">Equivalent to *go*.</span></span>
5. <span data-ttu-id="6dd13-134">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="6dd13-134">Click **OK**.</span></span>
