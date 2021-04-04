---
title: Hændelser for lagerapp
description: I dette emne beskrives den hændelsesbehandling i lagerstedsappen, der bruges til at behandle hændelsesmeddelelser i lagerstedsapps som en del af et batchjob.
author: perlynne
manager: tfehr
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileDeviceQueueEvent
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 0bafcbd5306860cb80d6e813aabf83853a9011c1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248637"
---
# <a name="warehouse-app-event-processing"></a><span data-ttu-id="42da8-103">Hændelsesbehandling i lagerstedsapp</span><span class="sxs-lookup"><span data-stu-id="42da8-103">Warehouse app event processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="42da8-104">Batchjob, der kører i Supply Chain Management, kan bruge data fra en kø til behandling af hændelser, der er udstedt af lagerstedsappen, til at reagere efter behov på de signalerede hændelser.</span><span class="sxs-lookup"><span data-stu-id="42da8-104">Batch jobs running in Supply Chain Management can use data from a queue for processing events issued by the warehouse app to react as needed to the signaled events.</span></span> <span data-ttu-id="42da8-105">Denne funktion føjer relevante hændelser til køen som svar på bestemte typer handlinger, der udføres af arbejdere, der bruger appen.</span><span class="sxs-lookup"><span data-stu-id="42da8-105">This feature add relevant events to the queue in response to certain types of actions taken by workers using the app.</span></span> <span data-ttu-id="42da8-106">Hvis du f.eks. bruger funktionen **Opret og behandl overførselsordrer fra lagerstedsappen**, oprettes og opdateres overflytningsordrehovedet og -linjerne automatisk i back-end, når systemet kører batchjobbet **Hændelsesbehandling i lagerstedsapp**.</span><span class="sxs-lookup"><span data-stu-id="42da8-106">An example is when using the **Create and process transfer orders from the warehouse app** feature, the transfer order header and lines get created and updated in the back end when the system is running the **Process warehouse app events** batch job.</span></span>

## <a name="enable-the-process-warehouse-app-events-feature"></a><span data-ttu-id="42da8-107">Aktivere funktionen Hændelsesbehandling i lagerstedsapp</span><span class="sxs-lookup"><span data-stu-id="42da8-107">Enable the Process warehouse app events feature</span></span>

<span data-ttu-id="42da8-108">Før du kan bruge denne funktion, skal den aktiveres i dit system.</span><span class="sxs-lookup"><span data-stu-id="42da8-108">Before you can use this feature, it must be enabled on your system.</span></span> <span data-ttu-id="42da8-109">Administratorer kan bruge siden [funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionsstatus og aktivere den, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="42da8-109">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) page to check the feature status and enable it if needed.</span></span> <span data-ttu-id="42da8-110">Funktionen Hændelsesbehandling i lagerstedsapp vises som:</span><span class="sxs-lookup"><span data-stu-id="42da8-110">The Process warehouse app events feature is listed as:</span></span>

- <span data-ttu-id="42da8-111">**Modul** – Lokationsstyring</span><span class="sxs-lookup"><span data-stu-id="42da8-111">**Module** - Warehouse management</span></span>
- <span data-ttu-id="42da8-112">**Funktionsnavn** - Hændelsesbehandling i lagerstedsapp</span><span class="sxs-lookup"><span data-stu-id="42da8-112">**Feature name** - Process warehouse app events</span></span>

## <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a><span data-ttu-id="42da8-113">Konfigurere et batchjob, der skal behandle hændelser i lagerstedsapp</span><span class="sxs-lookup"><span data-stu-id="42da8-113">Set up a batch job to process warehouse app events</span></span>

### <a name="process-warehouse-app-events"></a><span data-ttu-id="42da8-114">Proces for hændelser for lagerapp</span><span class="sxs-lookup"><span data-stu-id="42da8-114">Process warehouse app events</span></span>

<span data-ttu-id="42da8-115">Konfigurere et planlagt batchjob, der skal behandle hændelser i lagerstedsapp for oprettelse af overførselsordrer og linjeopdateringer.</span><span class="sxs-lookup"><span data-stu-id="42da8-115">Set up a scheduled batch job to process the warehouse app events for the transfer order creation and line updates.</span></span>

1. <span data-ttu-id="42da8-116">Gå til **Lokationsstyring \> Periodiske opgaver \> Hændelsesbehandling i lagerstedsapp**.</span><span class="sxs-lookup"><span data-stu-id="42da8-116">Go to **Warehouse management \> Periodic tasks \> Process warehouse app events**.</span></span>
1. <span data-ttu-id="42da8-117">Dialogboksen Hændelsesbehandling i lagerstedsapp vises.</span><span class="sxs-lookup"><span data-stu-id="42da8-117">The Process warehouse app events dialog box opens.</span></span> <span data-ttu-id="42da8-118">Angiv **Batchbehandling** til **Ja** i oversigtspanelet **Kør i baggrunden**.</span><span class="sxs-lookup"><span data-stu-id="42da8-118">Expand the **Run in background** FastTab and set **Batch processing** to **Yes**.</span></span>
1. <span data-ttu-id="42da8-119">Vælg **Gentagelse** i oversigtspanelet **Kør i baggrunden**.</span><span class="sxs-lookup"><span data-stu-id="42da8-119">On the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="42da8-120">Dialogboksen **Definer gentagelse** åbnes.</span><span class="sxs-lookup"><span data-stu-id="42da8-120">The **Define recurrence** dialog box opens.</span></span> <span data-ttu-id="42da8-121">Angiv kørselsplanen efter behov for din virksomhed.</span><span class="sxs-lookup"><span data-stu-id="42da8-121">Set the run schedule as needed for your business.</span></span>
1. <span data-ttu-id="42da8-122">Klik på **OK** for at vende tilbage til dialogboksen **Hændelsesbehandling i lagerstedsapp**.</span><span class="sxs-lookup"><span data-stu-id="42da8-122">Select **OK** to return to the **Process warehouse app events** dialog box.</span></span>
1. <span data-ttu-id="42da8-123">Vælg **OK** i dialogboksen **Hændelsesbehandling i lagerstedsapp** for at føje batchjobbet til batchkøen.</span><span class="sxs-lookup"><span data-stu-id="42da8-123">Select **OK** in the **Process warehouse app events** dialog box to add the batch job to the batch queue.</span></span>

## <a name="query-warehouse-app-events"></a><span data-ttu-id="42da8-124">Forespørge på hændelser i lagerstedsapp</span><span class="sxs-lookup"><span data-stu-id="42da8-124">Query warehouse app events</span></span>

<span data-ttu-id="42da8-125">Du kan få vist hændelseskøen og de hændelsesmeddelelser, der er genereret af lagerstedsappen, ved at gå til **Lokationsstyring \> Forespørgsler og rapporter \> Mobilenhedslogge \> Hændelser i lagerstedsapp**.</span><span class="sxs-lookup"><span data-stu-id="42da8-125">You can view the event queue and events messages generated by the warehouse app by going to **Warehouse management \> Inquiries and reports \> Mobile device logs \> Warehouse app events**.</span></span>

## <a name="the-standard-event-queue-process"></a><span data-ttu-id="42da8-126">Standardprocessen for hændelseskøer</span><span class="sxs-lookup"><span data-stu-id="42da8-126">The standard event queue process</span></span>

<span data-ttu-id="42da8-127">Køen for hændelser i lagerstedsapps vil typisk blive brugt sammen med følgende beskrevet flow:</span><span class="sxs-lookup"><span data-stu-id="42da8-127">The warehouse apps events queue will typically be used with the following described flow:</span></span>

1. <span data-ttu-id="42da8-128">Der bliver føjet en hændelse til køen med en hændelsesmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="42da8-128">An event gets added to the queue  with an event message.</span></span> <span data-ttu-id="42da8-129">Den nye meddelelse har til at begynde med hændelsestilstanden **Ventende**, hvilket betyder, at batchjobbet **Hændelsesbehandling i lagerstedsapp** ikke vil hente og behandle denne meddelelse.</span><span class="sxs-lookup"><span data-stu-id="42da8-129">The new message initially has an Event state of **Waiting**, which means that the **Process warehouse app events** batch job will not pick up and process this message.</span></span>
1. <span data-ttu-id="42da8-130">Så snart meddelelsestilstanden er opdateret til **Sat i kø**, henter batchjobbet **Hændelsesbehandling i lagerstedsapp** hændelsen og behandler den.</span><span class="sxs-lookup"><span data-stu-id="42da8-130">As soon as the message state is updated to **Queued**, the **Process warehouse app** events batch job will pick up and process the event.</span></span>
1. <span data-ttu-id="42da8-131">Batchjobbet opdaterer hændelsestilstandene til enten **Fuldført** eller **Mislykket**, afhængigt af om den anmodede proces var mulig.</span><span class="sxs-lookup"><span data-stu-id="42da8-131">The batch job updates the event states to either **Completed** or **Failed**, depending on whether the requested process was possible.</span></span>
1. <span data-ttu-id="42da8-132">Når alle relaterede hændelsesmeddelelser er **Fuldført**, slettes hændelsen fra køen.</span><span class="sxs-lookup"><span data-stu-id="42da8-132">When all the related event messages are **Completed**, the event is deleted from the queue.</span></span>

 <span data-ttu-id="42da8-133">Du kan få vist et detaljeret eksempel under [Oprette en flytteordre fra en lagerstedsapp-proces](create-transfer-order-from-warehouse-app.md).</span><span class="sxs-lookup"><span data-stu-id="42da8-133">For a detailed example, see [Create transfer order from warehouse app process](create-transfer-order-from-warehouse-app.md).</span></span>

## <a name="handle-event-errors"></a><span data-ttu-id="42da8-134">Håndtere hændelsesfejl</span><span class="sxs-lookup"><span data-stu-id="42da8-134">Handle event errors</span></span>

<span data-ttu-id="42da8-135">Som en del af behandlingen af lagerstedshændelsen vil den anmodede meddelelsesaktivitet muligvis ikke modtage processer fra batchjobbet.</span><span class="sxs-lookup"><span data-stu-id="42da8-135">As part of the warehouse event processing, the requested message activity may not receive processes from the batch job.</span></span> <span data-ttu-id="42da8-136">Hvis dette er tilfældet, ændres hændelsesmeddelelsen til **Mislykket**.</span><span class="sxs-lookup"><span data-stu-id="42da8-136">In this case, the event message will change to **Failed**.</span></span> <span data-ttu-id="42da8-137">Du kan bruge oplysningerne i **Batchlogfilen** til at se hvorfor og foretage de nødvendige handlinger for at løse eventuelle problemer.</span><span class="sxs-lookup"><span data-stu-id="42da8-137">You can use the **Batch log** information to learn why and take needed action to correct any problems.</span></span>

<span data-ttu-id="42da8-138">Du kan få vist et detaljeret eksempel under [Oprette en flytteordre fra lagerstedsapp](create-transfer-order-from-warehouse-app.md).</span><span class="sxs-lookup"><span data-stu-id="42da8-138">For a detailed example, see [Create transfer order from warehouse app](create-transfer-order-from-warehouse-app.md).</span></span>

<span data-ttu-id="42da8-139">Sådan nulstiller du en mislykket hændelsesmeddelelse i lagerstedsappen:</span><span class="sxs-lookup"><span data-stu-id="42da8-139">To reset a failed warehouse app event message:</span></span>

1. <span data-ttu-id="42da8-140">Gå til **Lokationsstyring \> Forespørgsler og rapporter \> Mobilenhedslogge \> Hændelser i lagerstedsapp**.</span><span class="sxs-lookup"><span data-stu-id="42da8-140">Go to **Warehouse management \> Inquiries and reports \> Mobile device logs \> Warehouse app events**.</span></span>
1. <span data-ttu-id="42da8-141">Find og vælg en relevant hændelse, der vises som **Mislykket** i kolonnen **Hændelsestilstand** i oversigtspanelet **Hændelsesmeddelelser i lagerstedsapp**.</span><span class="sxs-lookup"><span data-stu-id="42da8-141">On the **Warehouse app event messages** FastTab, find and select a relevant event that is showing **Failed** in the **Event state** column.</span></span>
1. <span data-ttu-id="42da8-142">Vælg **Nulstil** fra værktøjslinjen **Hændelsesmeddelelser i lagerstedsapp**.</span><span class="sxs-lookup"><span data-stu-id="42da8-142">Select **Reset** from the **Warehouse app event messages** toolbar.</span></span>
1. <span data-ttu-id="42da8-143">Fortsæt med at arbejde, indtil alle relevante meddelelser er nulstillet.</span><span class="sxs-lookup"><span data-stu-id="42da8-143">Continue working until all relevant messages are reset.</span></span>

<span data-ttu-id="42da8-144">Du kan også fjerne en **Mislykket** hændelsesmeddelelse ved hjælp af indstillingen **Slet** på værktøjslinjen **Hændelsesmeddelelser i lagerstedsapp**.</span><span class="sxs-lookup"><span data-stu-id="42da8-144">You can also remove a **Failed** event message by using the **Delete** option on the **Warehouse app event messages** toolbar.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]