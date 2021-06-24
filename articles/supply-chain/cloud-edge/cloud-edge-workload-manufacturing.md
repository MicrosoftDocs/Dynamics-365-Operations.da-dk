---
title: Produktionsarbejdsbyrder for sky- og kantskalaenheder
description: Dette emne beskriver, hvordan produktionsarbejdsbyrder virker sammen med sky- og kantskalaenheder.
author: cabeln
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: cabeln
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 9cd7dd8b9241171bdfdb3cc1379211a2fe99bbe1
ms.sourcegitcommit: 8d50c905a0c9d4347519549b587bdebab8ffc628
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2021
ms.locfileid: "6183990"
---
# <a name="manufacturing-execution-workloads-for-cloud-and-edge-scale-units"></a><span data-ttu-id="00c96-103">Arbejdsbelastninger i forbindelse med produktionsudførelse for sky- og edge-skaleringsenheder</span><span class="sxs-lookup"><span data-stu-id="00c96-103">Manufacturing execution workloads for cloud and edge scale units</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> <span data-ttu-id="00c96-104">Arbejdsbyrden for produktionsudførelse er tilgængelig i forhåndsversion på nuværende tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="00c96-104">The manufacturing execution workload is available in preview at this point in time.</span></span>
> <span data-ttu-id="00c96-105">Nogle forretningsfunktioner understøttes ikke fuldt ud i den offentlige prøveversion, når der anvendes skalaenheder for arbejdsbyrder.</span><span class="sxs-lookup"><span data-stu-id="00c96-105">Some business functionality isn't fully supported in the public preview when workload scale units are used.</span></span>

<span data-ttu-id="00c96-106">I produktionsudførelse giver skalaenheder følgende egenskaber:</span><span class="sxs-lookup"><span data-stu-id="00c96-106">In manufacturing execution, scale units deliver the following capabilities:</span></span>

- <span data-ttu-id="00c96-107">Maskinoperatører og tilsynsførende kan få adgang til den operationelle produktionsplan.</span><span class="sxs-lookup"><span data-stu-id="00c96-107">Machine operators and shop floor supervisors can access the operational production plan.</span></span>
- <span data-ttu-id="00c96-108">Maskinoperatører kan holde planen opdateret ved at køre diskrete og procesproduktionsjob.</span><span class="sxs-lookup"><span data-stu-id="00c96-108">Machine operators can keep the plan up to date by running discrete and process manufacturing jobs.</span></span>
- <span data-ttu-id="00c96-109">Den tilsynsførende kan justere driftsplanen.</span><span class="sxs-lookup"><span data-stu-id="00c96-109">The shop floor supervisor can adjust the operational plan.</span></span>
- <span data-ttu-id="00c96-110">Arbejderne kan få adgang til fremmøde og indstemplings- og udstemplingstid på kanten for at sikre en korrekt beregning af arbejderes løn.</span><span class="sxs-lookup"><span data-stu-id="00c96-110">Workers can access time and attendance for clock-in and clock-out on the edge, to ensure correct worker pay calculation.</span></span>

<span data-ttu-id="00c96-111">Dette emne beskriver, hvordan produktionsarbejdsbyrder virker sammen med sky- og kantskalaenheder.</span><span class="sxs-lookup"><span data-stu-id="00c96-111">This topic describes how manufacturing execution workloads work with cloud and edge scale units.</span></span>

## <a name="the-manufacturing-lifecycle"></a><span data-ttu-id="00c96-112">Livscyklussen for produktion</span><span class="sxs-lookup"><span data-stu-id="00c96-112">The manufacturing lifecycle</span></span>

<span data-ttu-id="00c96-113">Når følgende illustration vises, er produktions livscyklussen opdelt i tre faser: *Planlæg*, *Udfør* og *Færdiggør*.</span><span class="sxs-lookup"><span data-stu-id="00c96-113">As the following illustration shows, the manufacturing lifecycle is divided into three phases: *Plan*, *Execute*, and *Finalize*.</span></span>

<span data-ttu-id="00c96-114">[![Produktionsudførelsesfaser, når der bruges et enkelt miljø](media/mes-phases.png "Produktionsudførelsesfaser, når der bruges et enkelt miljø")](media/mes-phases-large.png)</span><span class="sxs-lookup"><span data-stu-id="00c96-114">[![Manufacturing execution phases when a single environment is used](media/mes-phases.png "Manufacturing execution phases when a single environment is used")](media/mes-phases-large.png)</span></span>

<span data-ttu-id="00c96-115">Fasen _Planlæg_ omfatter produktdefinition, planlægning, oprettelse og planlægning af ordrer og frigivelse.</span><span class="sxs-lookup"><span data-stu-id="00c96-115">The _Plan_ phase includes product definition, planning, order creation and scheduling, and release.</span></span> <span data-ttu-id="00c96-116">Frigivelsestrinnet angiver overgangen fra fasen _Planlæg_ til fasen _Udfør_.</span><span class="sxs-lookup"><span data-stu-id="00c96-116">The release step indicates the transition from the _Plan_ phase to the _Execute_ phase.</span></span> <span data-ttu-id="00c96-117">Når en produktionsordre frigives, vil produktionsordrejobbene være synlige i produktionen og være klar til udførelse.</span><span class="sxs-lookup"><span data-stu-id="00c96-117">When a production order is released, the production order jobs will be visible on the production floor and ready for execution.</span></span>

<span data-ttu-id="00c96-118">Når et produktionsjob er markeret som fuldført, flyttes det fra fasen _Udfør_ til fasen _Færdiggør_.</span><span class="sxs-lookup"><span data-stu-id="00c96-118">When a production job is marked as completed, it moves from the _Execute_ phase to the _Finalize_ phase.</span></span> <span data-ttu-id="00c96-119">I fasen _Færdiggør_ går registreringerne fra fasen *Udfør* via en godkendelsesarbejdsproces, hvor de beregnes, godkendes og overføres.</span><span class="sxs-lookup"><span data-stu-id="00c96-119">In the _Finalize_ phase, the registrations from the *Execute* phase go through an approval workflow, where they are calculated, approved, and transferred.</span></span> <span data-ttu-id="00c96-120">På dette tidspunkt er produktionsordren fuldført.</span><span class="sxs-lookup"><span data-stu-id="00c96-120">At that point, the production order is completed.</span></span> <span data-ttu-id="00c96-121">Derfor genereres udgangspunktet for arbejderens løn.</span><span class="sxs-lookup"><span data-stu-id="00c96-121">Therefore, the basis for the workers' pay is generated.</span></span>

## <a name="splitting-the-execute-phase-into-a-separate-workload"></a><span data-ttu-id="00c96-122">Opdeling af udførelsesfasen i en separat arbejdsbyrde</span><span class="sxs-lookup"><span data-stu-id="00c96-122">Splitting the Execute phase into a separate workload</span></span>

<span data-ttu-id="00c96-123">Som følgende illustration viser er fasen _Udfør_ opdelt som en separat belastning, når der bruges skalaenheder.</span><span class="sxs-lookup"><span data-stu-id="00c96-123">As the following illustration shows, when scale units are used, the _Execute_ phase is split out as a separate workload.</span></span>

<span data-ttu-id="00c96-124">[![Produktionsudførelsesfaser ved brug af skalaenheder](media/mes-phases-workloads.png "Produktionsudførelsesfaser ved brug af skalaenheder")](media/mes-phases-workloads-large.png)</span><span class="sxs-lookup"><span data-stu-id="00c96-124">[![Manufacturing execution phases when scale units are used](media/mes-phases-workloads.png "Manufacturing execution phases when scale units are used")](media/mes-phases-workloads-large.png)</span></span>

<span data-ttu-id="00c96-125">Modellen går nu fra en installation med én forekomst til en model, der er baseret på hubben og skalaenhederne.</span><span class="sxs-lookup"><span data-stu-id="00c96-125">The model now goes from a single-instance installation to a model that is based on the hub and scale units.</span></span> <span data-ttu-id="00c96-126">Faserne _Planlæg_ og _Færdiggør_ kører som baggrundshandlinger på hubben, og arbejdsbyrden for produktionsudførelse kører på skalaenhederne.</span><span class="sxs-lookup"><span data-stu-id="00c96-126">The _Plan_ and _Finalize_ phases run as back-office operations on the hub, and the manufacturing execution workload runs on the scale units.</span></span> <span data-ttu-id="00c96-127">Data overføres asynkront mellem hubben og skalaenhederne.</span><span class="sxs-lookup"><span data-stu-id="00c96-127">Data is transferred asynchronously between the hub and scale units.</span></span>

<span data-ttu-id="00c96-128">Når en produktionsordre frigives på hubben, overføres alle de data, der er nødvendige for at behandle produktionsjob, til skalaenheden.</span><span class="sxs-lookup"><span data-stu-id="00c96-128">When a production order is released on the hub, all data that is required to process production jobs is transferred to the scale unit.</span></span> <span data-ttu-id="00c96-129">Disse data omfatter produktionsordrer, produktionsruter, styklister og produkter.</span><span class="sxs-lookup"><span data-stu-id="00c96-129">This data includes production orders, production routes, bills of materials, and products.</span></span> <span data-ttu-id="00c96-130">Data, der ikke er relateret til en produktionsordre (f.eks. indirekte aktiviteter, fraværskoder og produktionsparametre), overføres også fra hubben til skalaenheden.</span><span class="sxs-lookup"><span data-stu-id="00c96-130">Data that isn't related to a production order (such as indirect activities, absence codes, and production parameters) is also transferred from the hub to the scale unit.</span></span> <span data-ttu-id="00c96-131">Som regel kan data, der kommer fra hubben og overføres til skalaenheden, kun oprettes eller opdateres på hubben.</span><span class="sxs-lookup"><span data-stu-id="00c96-131">As a rule, data that originates from the hub and that is transferred to the scale unit can be created or updated only on the hub.</span></span> <span data-ttu-id="00c96-132">En ny fraværskode eller indirekte aktivitet kan f.eks. ikke oprettes på skalaenheden, og de kan kun bruges til registrering.</span><span class="sxs-lookup"><span data-stu-id="00c96-132">For example, a new absence code or indirect activity can't be created on the scale unit&mdash;they can be used only for registration.</span></span> <span data-ttu-id="00c96-133">De registreringer, der foretages på skalaenheden under udførelsen, overføres derefter til hubben, hvor tids og fremmødegodkendelse, lager og økonomiske opdateringer behandles.</span><span class="sxs-lookup"><span data-stu-id="00c96-133">The registrations that are made on the scale unit during execution are then transferred to the hub, where time and attendance approval, inventory, and financial updates are processed.</span></span>

## <a name="manufacturing-execution-tasks-that-can-be-run-on-workloads"></a><span data-ttu-id="00c96-134">Produktionsudførelsesopgaver, der kan køres på arbejdsbyrder</span><span class="sxs-lookup"><span data-stu-id="00c96-134">Manufacturing execution tasks that can be run on workloads</span></span>

<span data-ttu-id="00c96-135">Følgende opgaver for produktionsudførelse kan i øjeblikket køres på arbejdsbyrder, når der bruges skalaenheder:</span><span class="sxs-lookup"><span data-stu-id="00c96-135">The following manufacturing execution tasks can currently be run on workloads when scale units are used:</span></span>

- <span data-ttu-id="00c96-136">Indstempling, login, udstempling og fravær</span><span class="sxs-lookup"><span data-stu-id="00c96-136">Clock-in, log-in, clock-out, and absence</span></span>
- <span data-ttu-id="00c96-137">Start job</span><span class="sxs-lookup"><span data-stu-id="00c96-137">Start job</span></span>
- <span data-ttu-id="00c96-138">Bundte job</span><span class="sxs-lookup"><span data-stu-id="00c96-138">Bundle jobs</span></span>
- <span data-ttu-id="00c96-139">Rapport i gang</span><span class="sxs-lookup"><span data-stu-id="00c96-139">Report progress</span></span>
- <span data-ttu-id="00c96-140">Rapportér spild</span><span class="sxs-lookup"><span data-stu-id="00c96-140">Report scrap</span></span>
- <span data-ttu-id="00c96-141">Indirekte aktivitet</span><span class="sxs-lookup"><span data-stu-id="00c96-141">Indirect activity</span></span>
- <span data-ttu-id="00c96-142">Pause</span><span class="sxs-lookup"><span data-stu-id="00c96-142">Break</span></span>
- <span data-ttu-id="00c96-143">Færdigmeld og læg på lager (kræver, at du også kører arbejdsbyrden for lagerstedsudførelse på skalaenheden. Se også [Færdigmelde og lægge på lager på en skalaenhed](#RAF))</span><span class="sxs-lookup"><span data-stu-id="00c96-143">Report as finished and putaway (requires that you also run the warehouse execution workload on your scale unit, see also [Report as finished and putaway on a scale unit](#RAF))</span></span>

## <a name="working-with-manufacturing-execution-workloads-on-the-hub"></a><span data-ttu-id="00c96-144">Arbejde med arbejdsbelastninger i produktionsudførelse på hubben</span><span class="sxs-lookup"><span data-stu-id="00c96-144">Working with manufacturing execution workloads on the hub</span></span>

<span data-ttu-id="00c96-145">De processer, der kræves for at køre arbejdsbelastninger for produktionsudførelse, kører som regel automatisk for at holde hubben og alle skalaenheder synkrone efter behov.</span><span class="sxs-lookup"><span data-stu-id="00c96-145">Usually, the processes that are required to run manufacturing execution workloads run automatically to keep the hub and all the scale units in sync, as needed.</span></span> <span data-ttu-id="00c96-146">Men hvis du har problemer, kan du manuelt udløse behandlingen af rå registreringer, der modtages fra arbejdsbyrder, og/eller kontrollere registreringsbehandlingsloggen.</span><span class="sxs-lookup"><span data-stu-id="00c96-146">However, if you're having trouble, you can manually trigger the processing of raw registrations that are received from workloads and/or check the registration processing log.</span></span>

### <a name="manually-process-raw-registrations"></a><span data-ttu-id="00c96-147">Behandle rå registreringer manuelt</span><span class="sxs-lookup"><span data-stu-id="00c96-147">Manually process raw registrations</span></span>

<span data-ttu-id="00c96-148">Et batchjob i Supply Chain Management kører automatisk for at behandle alle registreringer, der er modtaget fra arbejdsbyrderne.</span><span class="sxs-lookup"><span data-stu-id="00c96-148">A batch job in Supply Chain Management runs automatically to process all the registrations that have been received from the workloads.</span></span> <span data-ttu-id="00c96-149">Dette job opretter de nødvendige produktionskladder og logbogsposter, når en registrering behandles for en fuldført opgave på arbejdsbyrden.</span><span class="sxs-lookup"><span data-stu-id="00c96-149">This job creates the required production journals and logbook entries when a registration is processed for a completed job on the workload.</span></span>

<span data-ttu-id="00c96-150">Selvom jobbet normalt køres automatisk, kan du køre det manuelt på et hvilket som helst tidspunkt ved at logge på hubben og gå til **Produktionsstyring \> Periodiske opgaver \> BackOffice-styring af arbejdsbyrder \> Behandle rå registreringer**.</span><span class="sxs-lookup"><span data-stu-id="00c96-150">Although the job usually runs automatically, you can run it manually at any time by signing in to the hub and going to **Production control \> Periodic tasks \> Backoffice workload management \> Process raw registrations**.</span></span>

### <a name="check-the-raw-registration-processing-log"></a><span data-ttu-id="00c96-151">Kontrollere behandlingsloggen for rå registrering</span><span class="sxs-lookup"><span data-stu-id="00c96-151">Check the raw registration processing log</span></span>

<span data-ttu-id="00c96-152">Hvis du vil gennemgå registreringsbehandlingsloggen, skal du logge på hubben og gå til **Produktionsstyring \> Periodiske opgaver \> BackOffice-styring af arbejdsbyrder \> Behandlingslog for rå registrering**.</span><span class="sxs-lookup"><span data-stu-id="00c96-152">To review the registration processing log, sign in to the hub, and go to **Production control \> Periodic tasks \> Backoffice workload management \> Raw registration processing log**.</span></span> <span data-ttu-id="00c96-153">På siden **Behandlingslog for rå registrering** vises en liste over behandlede rå registreringer og status for hver registrering.</span><span class="sxs-lookup"><span data-stu-id="00c96-153">The **Raw registration processing log** page shows a list of processed raw registrations and the status of each registration.</span></span>

<span data-ttu-id="00c96-154">![Siden Behandlingslog for rå registrering](media/mes-processing-log.png "Siden Behandlingslog for rå registrering")</span><span class="sxs-lookup"><span data-stu-id="00c96-154">![Raw registration processing log page](media/mes-processing-log.png "Raw registration processing log page")</span></span>

<span data-ttu-id="00c96-155">Du kan arbejde på enhver registrering på listen ved at markere den og derefter vælge en af følgende knapper i handlingsruden:</span><span class="sxs-lookup"><span data-stu-id="00c96-155">You can work on any registration in the list by selecting it and then selecting one of the following buttons on the Action Pane:</span></span>

- <span data-ttu-id="00c96-156">**Proces** – Behandler den valgte registrering manuelt.</span><span class="sxs-lookup"><span data-stu-id="00c96-156">**Process** – Manually process the selected registration.</span></span> <span data-ttu-id="00c96-157">Denne handling kan være nyttig, hvis jobbet _Behandle rå registreringer_ ikke er kørt, eller hvis det mislykkedes.</span><span class="sxs-lookup"><span data-stu-id="00c96-157">This action can be useful if the _Process raw registrations_ job hasn't run, or if it failed.</span></span>
- <span data-ttu-id="00c96-158">**Annuller** – Annuller den valgte registrering.</span><span class="sxs-lookup"><span data-stu-id="00c96-158">**Cancel** – Cancel the selected registration.</span></span>

## <a name="working-with-manufacturing-execution-workloads-on-a-scale-unit"></a><span data-ttu-id="00c96-159">Arbejde med arbejdsbelastninger i produktionsudførelse på en skalaenhed</span><span class="sxs-lookup"><span data-stu-id="00c96-159">Working with manufacturing execution workloads on a scale unit</span></span>

<span data-ttu-id="00c96-160">De processer, der kræves for at køre arbejdsbelastninger for produktionsudførelse, kører som regel automatisk for at holde hubben og alle skalaenheder synkrone efter behov.</span><span class="sxs-lookup"><span data-stu-id="00c96-160">Usually, the processes that are required to run manufacturing execution workloads run automatically to keep the hub and all the scale units in sync, as needed.</span></span> <span data-ttu-id="00c96-161">Men hvis du har problemer, kan du kontrollere historikken for de ordrer, der er behandlet på en skalaenhed, eller manuelt køre jobbet _Meddelelsesprocessor for produktionshub til skalaenhed_.</span><span class="sxs-lookup"><span data-stu-id="00c96-161">However, if you're having trouble, you can check the history of orders that have been processed on a scale unit or manually run the _Manufacturing hub to scale unit message processor_ job.</span></span>

### <a name="view-the-history-of-manufacturing-jobs-that-have-been-processed-on-a-scale-unit"></a><span data-ttu-id="00c96-162">Se historikken for de produktionsjob, der er behandlet på en skalaenhed</span><span class="sxs-lookup"><span data-stu-id="00c96-162">View the history of manufacturing jobs that have been processed on a scale unit</span></span>

<span data-ttu-id="00c96-163">Hvis du vil gennemgå historikken for de produktionsjob, der er behandlet på en skalaenhed, skal du logge på skalaenhedens maskine og gå til **Produktionsstyring \> Periodiske opgaver \> BackOffice-styring af arbejdsbyrder \> Behandlingshistorik for produktionsjob**.</span><span class="sxs-lookup"><span data-stu-id="00c96-163">To review the history of manufacturing jobs that have been processed on a scale unit, sign in to the scale unit machine, and go to **Production control \> Periodic tasks \> Backoffice workload management \> Manufacturing jobs processing history**.</span></span> <span data-ttu-id="00c96-164">Siden **Behandlingshistorik for produktionsjob** viser behandlingshistorikken for produktionsordrerne på skalaenheden.</span><span class="sxs-lookup"><span data-stu-id="00c96-164">The **Manufacturing jobs processing history** page shows the processing history of the production orders on the scale unit.</span></span> <span data-ttu-id="00c96-165">Du kan arbejde på enhver produktionsordre på listen ved at markere den og derefter vælge en af følgende knapper i handlingsruden:</span><span class="sxs-lookup"><span data-stu-id="00c96-165">You can work on any production order in the list by selecting it and then selecting one of the following buttons on the Action Pane:</span></span>

- <span data-ttu-id="00c96-166">**Proces** – Behandler den valgte produktionsordre manuelt.</span><span class="sxs-lookup"><span data-stu-id="00c96-166">**Process** – Manually process the selected production order.</span></span>
- <span data-ttu-id="00c96-167">**Annuller** – Annullerer den valgte produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="00c96-167">**Cancel** – Cancel the selected production order.</span></span>

### <a name="manufacturing-hub-to-scale-unit-message-processor-job"></a><span data-ttu-id="00c96-168">Jobbet Meddelelsesprocessor for produktionshub til skalaenhed</span><span class="sxs-lookup"><span data-stu-id="00c96-168">Manufacturing hub to scale unit message processor job</span></span>

<span data-ttu-id="00c96-169">Jobbet _Meddelelsesprocessor for produktionshub til skalaenhed_ behandler data fra hubben til skalaenheden.</span><span class="sxs-lookup"><span data-stu-id="00c96-169">The _Manufacturing hub to scale unit message processor_ job processes data from the hub to the scale unit.</span></span> <span data-ttu-id="00c96-170">Dette job startes automatisk, når arbejdsbyrden for produktionsudførelse udrulles.</span><span class="sxs-lookup"><span data-stu-id="00c96-170">This job is automatically started when the manufacturing execution workload is deployed.</span></span> <span data-ttu-id="00c96-171">Du kan dog køre den manuelt på et hvilket som helst tidspunkt ved at gå til **Produktionsstyring \> Periodiske opgaver \> BackOffice-styring af arbejdsbyrder \> Meddelelsesprocessor for produktionshub til skalaenhed**.</span><span class="sxs-lookup"><span data-stu-id="00c96-171">However, you can run it manually at any time by going to **Production control \> Periodic tasks \> Backoffice workload management \> Manufacturing hub to scale unit message processor**.</span></span>

<a name="RAF"></a>

## <a name="report-as-finished-and-putaway-on-a-scale-unit"></a><span data-ttu-id="00c96-172">Færdigmelde og lægge på lager på en skalaenhed</span><span class="sxs-lookup"><span data-stu-id="00c96-172">Report as finished and putaway on a scale unit</span></span>

<!-- KFM: 
This section describes how to enable the abilities to report as finished and then putaway finished items when you are using to a scale unit.

### Enable and use report as finished and putaway on a scale unit -->

<span data-ttu-id="00c96-173">I den aktuelle version understøttes færdigmeldings- og lagringsoperationer (for færdigvarer, samprodukter og biprodukter) af [arbejdsbyrden for lagerstedsudførelse](cloud-edge-workload-warehousing.md) (ikke arbejdsbyrden for produktionsudførelse).</span><span class="sxs-lookup"><span data-stu-id="00c96-173">In the current release, report as finished and putaway operations (for finished products, co-products, and by-products) are supported by the [warehouse execution workload](cloud-edge-workload-warehousing.md) (not the manufacturing execution workload).</span></span> <span data-ttu-id="00c96-174">Hvis du vil bruge denne funktion, når den er knyttet til en skalaenhed, skal du derfor gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="00c96-174">Therefore, to use this functionality when connected to a scale unit, you must do the following:</span></span>

- <span data-ttu-id="00c96-175">Installer både arbejdsbyrden for udførelse af lagersteder og arbejdsbyrden for produktionsudførelse på din skalaenhed.</span><span class="sxs-lookup"><span data-stu-id="00c96-175">Install both the warehouse execution workload and the manufacturing execution workload on your scale unit.</span></span>
- <span data-ttu-id="00c96-176">Du kan bruge mobilappen Warehouse Management til at færdigmelde og behandle læg på lager-arbejdet.</span><span class="sxs-lookup"><span data-stu-id="00c96-176">Use the Warehouse Management mobile app to report as finished and process the putaway work.</span></span> <span data-ttu-id="00c96-177">Grænsefladen til produktionsudførelse understøtter i øjeblikket ikke disse processer.</span><span class="sxs-lookup"><span data-stu-id="00c96-177">The production floor execution interface does not currently support these processes.</span></span>

<!-- KFM: API details needed

### Customize report as finished and putaway functionality

 -->

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
