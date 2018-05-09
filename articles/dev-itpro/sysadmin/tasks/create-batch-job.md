--- 
title: Oprette et batchjob
description: Et batchjob er en gruppe opgaver, der sendes til en AOS-forekomst (applikationsobjektserver) til automatisk behandling.
author: maertenm
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 55b153e6044f61f16e19ae0b264e3f23538e004a
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-batch-job"></a><span data-ttu-id="278dc-103">Oprette et batchjob</span><span class="sxs-lookup"><span data-stu-id="278dc-103">Create a batch job</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="278dc-104">Et batchjob er en gruppe opgaver, der sendes til en AOS-forekomst (applikationsobjektserver) til automatisk behandling.</span><span class="sxs-lookup"><span data-stu-id="278dc-104">A batch job is a group of tasks that are submitted to an Application Object Server (AOS) instance for automatic processing.</span></span> <span data-ttu-id="278dc-105">Batchjob køres ved hjælp af sikkerhedslegitimationsoplysningerne for den bruger, der har oprettet jobbet.</span><span class="sxs-lookup"><span data-stu-id="278dc-105">Batch jobs are run by using the security credentials of the user who created the job.</span></span> <span data-ttu-id="278dc-106">Du kan bruge følgende procedure for at oprette et batchjob.</span><span class="sxs-lookup"><span data-stu-id="278dc-106">Use the following procedure to create a batch job.</span></span> <span data-ttu-id="278dc-107">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="278dc-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-the-batch-job"></a><span data-ttu-id="278dc-108">Opret batchjobbet</span><span class="sxs-lookup"><span data-stu-id="278dc-108">Create the batch job</span></span>
1. <span data-ttu-id="278dc-109">Gå til Systemadministration > Forespørgsler > Batchjob.</span><span class="sxs-lookup"><span data-stu-id="278dc-109">Go to System administration > Inquiries > Batch jobs.</span></span>
2. <span data-ttu-id="278dc-110">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="278dc-110">Click New.</span></span>
3. <span data-ttu-id="278dc-111">Indtast en værdi i feltet Stillingsbeskrivelse.</span><span class="sxs-lookup"><span data-stu-id="278dc-111">In the Job description field, type a value.</span></span>
4. <span data-ttu-id="278dc-112">Angiv en dato og et klokkeslæt i feltet Planlagt startdato/-klokkeslæt.</span><span class="sxs-lookup"><span data-stu-id="278dc-112">In the Scheduled start date/time field, enter a date and time.</span></span>
5. <span data-ttu-id="278dc-113">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="278dc-113">Click Save.</span></span>

## <a name="create-a-recurrence"></a><span data-ttu-id="278dc-114">Opret en gentagelse</span><span class="sxs-lookup"><span data-stu-id="278dc-114">Create a recurrence</span></span>
1. <span data-ttu-id="278dc-115">Klik på Batchjob i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="278dc-115">On the Action Pane, click Batch job.</span></span>
2. <span data-ttu-id="278dc-116">Klik på Gentagelse.</span><span class="sxs-lookup"><span data-stu-id="278dc-116">Click Recurrence.</span></span>
    * <span data-ttu-id="278dc-117">Brug disse indstillinger til at angive et interval og mønster for gentagelsen.</span><span class="sxs-lookup"><span data-stu-id="278dc-117">Use these options to enter a range and pattern for the recurrence.</span></span>  
3. <span data-ttu-id="278dc-118">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="278dc-118">Click OK.</span></span>

## <a name="add-alerts"></a><span data-ttu-id="278dc-119">Tilføj beskeder</span><span class="sxs-lookup"><span data-stu-id="278dc-119">Add alerts</span></span>
1. <span data-ttu-id="278dc-120">Klik på Batchjob i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="278dc-120">On the Action Pane, click Batch job.</span></span>
2. <span data-ttu-id="278dc-121">Klik på Beskeder.</span><span class="sxs-lookup"><span data-stu-id="278dc-121">Click Alerts.</span></span>
    * <span data-ttu-id="278dc-122">Angiv, om der skal sendes meddelelser om påmindelser til dig, når batchjobbet afsluttes, støder på en fejl eller annulleres.</span><span class="sxs-lookup"><span data-stu-id="278dc-122">Indicate if you want alert messages sent when the batch job ends, has an error, or is canceled.</span></span> <span data-ttu-id="278dc-123">Angiv derefter, om der skal vises påmindelser som pop op-meddelelser.</span><span class="sxs-lookup"><span data-stu-id="278dc-123">Then specify if you want the alerts to be displayed as pop-up messages.</span></span>   
3. <span data-ttu-id="278dc-124">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="278dc-124">Click OK.</span></span>


