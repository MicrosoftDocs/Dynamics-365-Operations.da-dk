---
title: Produktionsarbejdsbyrder for sky- og kantskalaenheder
description: Dette emne beskriver, hvordan produktionsarbejdsbyrder virker sammen med sky- og kantskalaenheder.
author: cabeln
manager: ''
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 6bef28d16236a7862550f3ab87f73baf8dab97b0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251068"
---
# <a name="manufacturing-execution-workloads-for-cloud-and-edge-scale-units"></a><span data-ttu-id="c0e00-103">Produktionsarbejdsbyrder for sky- og kantskalaenheder</span><span class="sxs-lookup"><span data-stu-id="c0e00-103">Manufacturing execution workloads for cloud and edge scale units</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> <span data-ttu-id="c0e00-104">Nogle forretningsfunktioner understøttes ikke fuldt ud i den offentlige prøveversion, når der anvendes skalaenheder for arbejdsbyrder.</span><span class="sxs-lookup"><span data-stu-id="c0e00-104">Some business functionality isn't fully supported in the public preview when workload scale units are used.</span></span>

<span data-ttu-id="c0e00-105">I produktionsudførelse giver sky- og kantskalaenheder følgende funktioner, også selvom der ikke er forbindelse mellem kantenheder og hubben:</span><span class="sxs-lookup"><span data-stu-id="c0e00-105">In manufacturing execution, cloud and edge scale units deliver the following capabilities, even when edge units aren't connected to the hub:</span></span>

- <span data-ttu-id="c0e00-106">Maskinoperatører og tilsynsførende kan få adgang til den operationelle produktionsplan.</span><span class="sxs-lookup"><span data-stu-id="c0e00-106">Machine operators and shop floor supervisors can access the operational production plan.</span></span>
- <span data-ttu-id="c0e00-107">Maskinoperatører kan holde planen opdateret ved at køre diskrete og procesproduktionsjob.</span><span class="sxs-lookup"><span data-stu-id="c0e00-107">Machine operators can keep the plan up to date by running discrete and process manufacturing jobs.</span></span>
- <span data-ttu-id="c0e00-108">Den tilsynsførende kan justere driftsplanen.</span><span class="sxs-lookup"><span data-stu-id="c0e00-108">The shop floor supervisor can adjust the operational plan.</span></span>
- <span data-ttu-id="c0e00-109">Arbejderne kan få adgang til fremmøde og indstemplings- og udstemplingstid på kanten for at sikre en korrekt beregning af arbejderes løn.</span><span class="sxs-lookup"><span data-stu-id="c0e00-109">Workers can access time and attendance for clock-in and clock-out on the edge, to ensure correct worker pay calculation.</span></span>

<span data-ttu-id="c0e00-110">Dette emne beskriver, hvordan produktionsarbejdsbyrder virker sammen med sky- og kantskalaenheder.</span><span class="sxs-lookup"><span data-stu-id="c0e00-110">This topic describes how manufacturing execution workloads work with cloud and edge scale units.</span></span>

## <a name="the-manufacturing-lifecycle"></a><span data-ttu-id="c0e00-111">Livscyklussen for produktion</span><span class="sxs-lookup"><span data-stu-id="c0e00-111">The manufacturing lifecycle</span></span>

<span data-ttu-id="c0e00-112">Når følgende illustration vises, er produktions livscyklussen opdelt i tre faser: *Planlæg*, *Udfør* og *Færdiggør*.</span><span class="sxs-lookup"><span data-stu-id="c0e00-112">As the following illustration shows, the manufacturing lifecycle is divided into three phases: *Plan*, *Execute*, and *Finalize*.</span></span>

<span data-ttu-id="c0e00-113">[![Produktionsudførelsesfaser, når der bruges et enkelt miljø](media/mes-phases.png "Produktionsudførelsesfaser, når der bruges et enkelt miljø")](media/mes-phases-large.png)</span><span class="sxs-lookup"><span data-stu-id="c0e00-113">[![Manufacturing execution phases when a single environment is used](media/mes-phases.png "Manufacturing execution phases when a single environment is used")](media/mes-phases-large.png)</span></span>

<span data-ttu-id="c0e00-114">Fasen _Planlæg_ omfatter produktdefinition, planlægning, oprettelse og planlægning af ordrer og frigivelse.</span><span class="sxs-lookup"><span data-stu-id="c0e00-114">The _Plan_ phase includes product definition, planning, order creation and scheduling, and release.</span></span> <span data-ttu-id="c0e00-115">Frigivelsestrinnet angiver overgangen fra fasen _Planlæg_ til fasen _Udfør_.</span><span class="sxs-lookup"><span data-stu-id="c0e00-115">The release step indicates the transition from the _Plan_ phase to the _Execute_ phase.</span></span> <span data-ttu-id="c0e00-116">Når en produktionsordre frigives, vil produktionsordrejobbene være synlige i produktionen og være klar til udførelse.</span><span class="sxs-lookup"><span data-stu-id="c0e00-116">When a production order is released, the production order jobs will be visible on the production floor and ready for execution.</span></span>

<span data-ttu-id="c0e00-117">Når et produktionsjob er markeret som fuldført, flyttes det fra fasen _Udfør_ til fasen _Færdiggør_.</span><span class="sxs-lookup"><span data-stu-id="c0e00-117">When a production job is marked as completed, it moves from the _Execute_ phase to the _Finalize_ phase.</span></span> <span data-ttu-id="c0e00-118">I fasen _Færdiggør_ går registreringerne fra fasen *Udfør* via en godkendelsesarbejdsproces, hvor de beregnes, godkendes og overføres.</span><span class="sxs-lookup"><span data-stu-id="c0e00-118">In the _Finalize_ phase, the registrations from the *Execute* phase go through an approval workflow, where they are calculated, approved, and transferred.</span></span> <span data-ttu-id="c0e00-119">På dette tidspunkt er produktionsordren fuldført.</span><span class="sxs-lookup"><span data-stu-id="c0e00-119">At that point, the production order is completed.</span></span> <span data-ttu-id="c0e00-120">Derfor genereres udgangspunktet for arbejderens løn.</span><span class="sxs-lookup"><span data-stu-id="c0e00-120">Therefore, the basis for the workers' pay is generated.</span></span>

## <a name="splitting-the-execute-phase-into-a-separate-workload"></a><span data-ttu-id="c0e00-121">Opdeling af udførelsesfasen i en separat arbejdsbyrde</span><span class="sxs-lookup"><span data-stu-id="c0e00-121">Splitting the Execute phase into a separate workload</span></span>

<span data-ttu-id="c0e00-122">Som følgende illustration viser er fasen _Udfør_ opdelt som en separat belastning, når der bruges skalaenheder.</span><span class="sxs-lookup"><span data-stu-id="c0e00-122">As the following illustration shows, when scale units are used, the _Execute_ phase is split out as a separate workload.</span></span>

<span data-ttu-id="c0e00-123">[![Produktionsudførelsesfaser ved brug af skalaenheder](media/mes-phases-workloads.png "Produktionsudførelsesfaser ved brug af skalaenheder")](media/mes-phases-workloads-large.png)</span><span class="sxs-lookup"><span data-stu-id="c0e00-123">[![Manufacturing execution phases when scale units are used](media/mes-phases-workloads.png "Manufacturing execution phases when scale units are used")](media/mes-phases-workloads-large.png)</span></span>

<span data-ttu-id="c0e00-124">Modellen går nu fra en installation med én forekomst til en model, der er baseret på hubben og skalaenhederne.</span><span class="sxs-lookup"><span data-stu-id="c0e00-124">The model now goes from a single-instance installation to a model that is based on the hub and scale units.</span></span> <span data-ttu-id="c0e00-125">Faserne _Planlæg_ og _Færdiggør_ kører som baggrundshandlinger på hubben, og arbejdsbyrden for produktionsudførelse kører på skalaenhederne.</span><span class="sxs-lookup"><span data-stu-id="c0e00-125">The _Plan_ and _Finalize_ phases run as back-office operations on the hub, and the manufacturing execution workload runs on the scale units.</span></span> <span data-ttu-id="c0e00-126">Data overføres asynkront mellem hubben og skalaenhederne.</span><span class="sxs-lookup"><span data-stu-id="c0e00-126">Data is transferred asynchronously between the hub and scale units.</span></span>

<span data-ttu-id="c0e00-127">Når en produktionsordre frigives på hubben, overføres alle de data, der er nødvendige for at behandle produktionsjob, til skalaenheden.</span><span class="sxs-lookup"><span data-stu-id="c0e00-127">When a production order is released on the hub, all data that is required to process production jobs is transferred to the scale unit.</span></span> <span data-ttu-id="c0e00-128">Disse data omfatter produktionsordrer, produktionsruter, styklister og produkter.</span><span class="sxs-lookup"><span data-stu-id="c0e00-128">This data includes production orders, production routes, bills of materials, and products.</span></span> <span data-ttu-id="c0e00-129">Data, der ikke er relateret til en produktionsordre (f.eks. indirekte aktiviteter, fraværskoder og produktionsparametre), overføres også fra hubben til skalaenheden.</span><span class="sxs-lookup"><span data-stu-id="c0e00-129">Data that isn't related to a production order (such as indirect activities, absence codes, and production parameters) is also transferred from the hub to the scale unit.</span></span> <span data-ttu-id="c0e00-130">Som regel kan data, der kommer fra hubben og overføres til skalaenheden, kun oprettes eller opdateres på hubben.</span><span class="sxs-lookup"><span data-stu-id="c0e00-130">As a rule, data that originates from the hub and that is transferred to the scale unit can be created or updated only on the hub.</span></span> <span data-ttu-id="c0e00-131">En ny fraværskode eller indirekte aktivitet kan f.eks. ikke oprettes på skalaenheden, og de kan kun bruges til registrering.</span><span class="sxs-lookup"><span data-stu-id="c0e00-131">For example, a new absence code or indirect activity can't be created on the scale unit&mdash;they can be used only for registration.</span></span> <span data-ttu-id="c0e00-132">De registreringer, der foretages på skalaenheden under udførelsen, overføres derefter til hubben, hvor tids og fremmødegodkendelse, lager og økonomiske opdateringer behandles.</span><span class="sxs-lookup"><span data-stu-id="c0e00-132">The registrations that are made on the scale unit during execution are then transferred to the hub, where time and attendance approval, inventory, and financial updates are processed.</span></span>

## <a name="manufacturing-execution-tasks-that-can-be-run-on-workloads"></a><span data-ttu-id="c0e00-133">Produktionsudførelsesopgaver, der kan køres på arbejdsbyrder</span><span class="sxs-lookup"><span data-stu-id="c0e00-133">Manufacturing execution tasks that can be run on workloads</span></span>

<span data-ttu-id="c0e00-134">Følgende opgaver for produktionsudførelse kan i øjeblikket køres på arbejdsbyrder, når der bruges skalaenheder:</span><span class="sxs-lookup"><span data-stu-id="c0e00-134">The following manufacturing execution tasks can currently be run on workloads when scale units are used:</span></span>

- <span data-ttu-id="c0e00-135">Indstempling, login, udstempling og fravær</span><span class="sxs-lookup"><span data-stu-id="c0e00-135">Clock-in, log-in, clock-out, and absence</span></span>
- <span data-ttu-id="c0e00-136">Start job</span><span class="sxs-lookup"><span data-stu-id="c0e00-136">Start job</span></span>
- <span data-ttu-id="c0e00-137">Bundte job</span><span class="sxs-lookup"><span data-stu-id="c0e00-137">Bundle jobs</span></span>
- <span data-ttu-id="c0e00-138">Rapport i gang</span><span class="sxs-lookup"><span data-stu-id="c0e00-138">Report progress</span></span>
- <span data-ttu-id="c0e00-139">Rapportér spild</span><span class="sxs-lookup"><span data-stu-id="c0e00-139">Report scrap</span></span>
- <span data-ttu-id="c0e00-140">Indirekte aktivitet</span><span class="sxs-lookup"><span data-stu-id="c0e00-140">Indirect activity</span></span>
- <span data-ttu-id="c0e00-141">Pause</span><span class="sxs-lookup"><span data-stu-id="c0e00-141">Break</span></span>

## <a name="working-with-manufacturing-execution-workloads-on-the-hub"></a><span data-ttu-id="c0e00-142">Arbejde med arbejdsbelastninger i produktionsudførelse på hubben</span><span class="sxs-lookup"><span data-stu-id="c0e00-142">Working with manufacturing execution workloads on the hub</span></span>

<span data-ttu-id="c0e00-143">De processer, der kræves for at køre arbejdsbelastninger for produktionsudførelse, kører som regel automatisk for at holde hubben og alle skalaenheder synkrone efter behov.</span><span class="sxs-lookup"><span data-stu-id="c0e00-143">Usually, the processes that are required to run manufacturing execution workloads run automatically to keep the hub and all the scale units in sync, as needed.</span></span> <span data-ttu-id="c0e00-144">Men hvis du har problemer, kan du manuelt udløse behandlingen af rå registreringer, der modtages fra arbejdsbyrder, og/eller kontrollere registreringsbehandlingsloggen.</span><span class="sxs-lookup"><span data-stu-id="c0e00-144">However, if you're having trouble, you can manually trigger the processing of raw registrations that are received from workloads and/or check the registration processing log.</span></span>

### <a name="manually-process-raw-registrations"></a><span data-ttu-id="c0e00-145">Behandle rå registreringer manuelt</span><span class="sxs-lookup"><span data-stu-id="c0e00-145">Manually process raw registrations</span></span>

<span data-ttu-id="c0e00-146">Et batchjob i Supply Chain Management kører automatisk for at behandle alle registreringer, der er modtaget fra arbejdsbyrderne.</span><span class="sxs-lookup"><span data-stu-id="c0e00-146">A batch job in Supply Chain Management runs automatically to process all the registrations that have been received from the workloads.</span></span> <span data-ttu-id="c0e00-147">Dette job opretter de nødvendige produktionskladder og logbogsposter, når en registrering behandles for en fuldført opgave på arbejdsbyrden.</span><span class="sxs-lookup"><span data-stu-id="c0e00-147">This job creates the required production journals and logbook entries when a registration is processed for a completed job on the workload.</span></span>

<span data-ttu-id="c0e00-148">Selvom jobbet normalt køres automatisk, kan du køre det manuelt på et hvilket som helst tidspunkt ved at logge på hubben og gå til **Produktionsstyring \> Periodiske opgaver \> BackOffice-styring af arbejdsbyrder \> Behandle rå registreringer**.</span><span class="sxs-lookup"><span data-stu-id="c0e00-148">Although the job usually runs automatically, you can run it manually at any time by signing in to the hub and going to **Production control \> Periodic tasks \> Backoffice workload management \> Process raw registrations**.</span></span>

### <a name="check-the-raw-registration-processing-log"></a><span data-ttu-id="c0e00-149">Kontrollere behandlingsloggen for rå registrering</span><span class="sxs-lookup"><span data-stu-id="c0e00-149">Check the raw registration processing log</span></span>

<span data-ttu-id="c0e00-150">Hvis du vil gennemgå registreringsbehandlingsloggen, skal du logge på hubben og gå til **Produktionsstyring \> Periodiske opgaver \> BackOffice-styring af arbejdsbyrder \> Behandlingslog for rå registrering**.</span><span class="sxs-lookup"><span data-stu-id="c0e00-150">To review the registration processing log, sign in to the hub, and go to **Production control \> Periodic tasks \> Backoffice workload management \> Raw registration processing log**.</span></span> <span data-ttu-id="c0e00-151">På siden **Behandlingslog for rå registrering** vises en liste over behandlede rå registreringer og status for hver registrering.</span><span class="sxs-lookup"><span data-stu-id="c0e00-151">The **Raw registration processing log** page shows a list of processed raw registrations and the status of each registration.</span></span>

<span data-ttu-id="c0e00-152">![Siden Behandlingslog for rå registrering](media/mes-processing-log.png "Siden Behandlingslog for rå registrering")</span><span class="sxs-lookup"><span data-stu-id="c0e00-152">![Raw registration processing log page](media/mes-processing-log.png "Raw registration processing log page")</span></span>

<span data-ttu-id="c0e00-153">Du kan arbejde på enhver registrering på listen ved at markere den og derefter vælge en af følgende knapper i handlingsruden:</span><span class="sxs-lookup"><span data-stu-id="c0e00-153">You can work on any registration in the list by selecting it and then selecting one of the following buttons on the Action Pane:</span></span>

- <span data-ttu-id="c0e00-154">**Proces** – Behandler den valgte registrering manuelt.</span><span class="sxs-lookup"><span data-stu-id="c0e00-154">**Process** – Manually process the selected registration.</span></span> <span data-ttu-id="c0e00-155">Denne handling kan være nyttig, hvis jobbet _Behandle rå registreringer_ ikke er kørt, eller hvis det mislykkedes.</span><span class="sxs-lookup"><span data-stu-id="c0e00-155">This action can be useful if the _Process raw registrations_ job hasn't run, or if it failed.</span></span>
- <span data-ttu-id="c0e00-156">**Annuller** – Annuller den valgte registrering.</span><span class="sxs-lookup"><span data-stu-id="c0e00-156">**Cancel** – Cancel the selected registration.</span></span>

## <a name="working-with-manufacturing-execution-workloads-on-a-scale-unit"></a><span data-ttu-id="c0e00-157">Arbejde med arbejdsbelastninger i produktionsudførelse på en skalaenhed</span><span class="sxs-lookup"><span data-stu-id="c0e00-157">Working with manufacturing execution workloads on a scale unit</span></span>

<span data-ttu-id="c0e00-158">De processer, der kræves for at køre arbejdsbelastninger for produktionsudførelse, kører som regel automatisk for at holde hubben og alle skalaenheder synkrone efter behov.</span><span class="sxs-lookup"><span data-stu-id="c0e00-158">Usually, the processes that are required to run manufacturing execution workloads run automatically to keep the hub and all the scale units in sync, as needed.</span></span> <span data-ttu-id="c0e00-159">Men hvis du har problemer, kan du kontrollere historikken for de ordrer, der er behandlet på en skalaenhed, eller manuelt køre jobbet _Meddelelsesprocessor for produktionshub til skalaenhed_.</span><span class="sxs-lookup"><span data-stu-id="c0e00-159">However, if you're having trouble, you can check the history of orders that have been processed on a scale unit or manually run the _Manufacturing hub to scale unit message processor_ job.</span></span>

### <a name="view-the-history-of-manufacturing-jobs-that-have-been-processed-on-a-scale-unit"></a><span data-ttu-id="c0e00-160">Se historikken for de produktionsjob, der er behandlet på en skalaenhed</span><span class="sxs-lookup"><span data-stu-id="c0e00-160">View the history of manufacturing jobs that have been processed on a scale unit</span></span>

<span data-ttu-id="c0e00-161">Hvis du vil gennemgå historikken for de produktionsjob, der er behandlet på en skalaenhed, skal du logge på skalaenhedens maskine og gå til **Produktionsstyring \> Periodiske opgaver \> BackOffice-styring af arbejdsbyrder \> Behandlingshistorik for produktionsjob**.</span><span class="sxs-lookup"><span data-stu-id="c0e00-161">To review the history of manufacturing jobs that have been processed on a scale unit, sign in to the scale unit machine, and go to **Production control \> Periodic tasks \> Backoffice workload management \> Manufacturing jobs processing history**.</span></span> <span data-ttu-id="c0e00-162">Siden **Behandlingshistorik for produktionsjob** viser behandlingshistorikken for produktionsordrerne på skalaenheden.</span><span class="sxs-lookup"><span data-stu-id="c0e00-162">The **Manufacturing jobs processing history** page shows the processing history of the production orders on the scale unit.</span></span> <span data-ttu-id="c0e00-163">Du kan arbejde på enhver produktionsordre på listen ved at markere den og derefter vælge en af følgende knapper i handlingsruden:</span><span class="sxs-lookup"><span data-stu-id="c0e00-163">You can work on any production order in the list by selecting it and then selecting one of the following buttons on the Action Pane:</span></span>

- <span data-ttu-id="c0e00-164">**Proces** – Behandler den valgte produktionsordre manuelt.</span><span class="sxs-lookup"><span data-stu-id="c0e00-164">**Process** – Manually process the selected production order.</span></span>
- <span data-ttu-id="c0e00-165">**Annuller** – Annullerer den valgte produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="c0e00-165">**Cancel** – Cancel the selected production order.</span></span>

### <a name="manufacturing-hub-to-scale-unit-message-processor-job"></a><span data-ttu-id="c0e00-166">Jobbet Meddelelsesprocessor for produktionshub til skalaenhed</span><span class="sxs-lookup"><span data-stu-id="c0e00-166">Manufacturing hub to scale unit message processor job</span></span>

<span data-ttu-id="c0e00-167">Jobbet _Meddelelsesprocessor for produktionshub til skalaenhed_ behandler data fra hubben til skalaenheden.</span><span class="sxs-lookup"><span data-stu-id="c0e00-167">The _Manufacturing hub to scale unit message processor_ job processes data from the hub to the scale unit.</span></span> <span data-ttu-id="c0e00-168">Dette job startes automatisk, når arbejdsbyrden for produktionsudførelse udrulles.</span><span class="sxs-lookup"><span data-stu-id="c0e00-168">This job is automatically started when the manufacturing execution workload is deployed.</span></span> <span data-ttu-id="c0e00-169">Du kan dog køre den manuelt på et hvilket som helst tidspunkt ved at gå til **Produktionsstyring \> Periodiske opgaver \> BackOffice-styring af arbejdsbyrder \> Meddelelsesprocessor for produktionshub til skalaenhed**.</span><span class="sxs-lookup"><span data-stu-id="c0e00-169">However, you can run it manually at any time by going to **Production control \> Periodic tasks \> Backoffice workload management \> Manufacturing hub to scale unit message processor**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]