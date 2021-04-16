---
title: Bølgefordeling
description: Dette emne indeholder en beskrivelse af, hvordan du kan konfigurere trinnet til bølgefordeling, herunder hvordan du kan aktivere parallel behandling af den.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: feee33a7d4ea3f0d9c4d671210293a28aac14f61
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823161"
---
# <a name="wave-allocation"></a><span data-ttu-id="c10ce-103">Bølgefordeling</span><span class="sxs-lookup"><span data-stu-id="c10ce-103">Wave allocation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c10ce-104">Bølgebehandling kan være tidskrævende, og den meste af behandlingstiden bruges på fordelingstrinnet og i trin til oprettelse af arbejde.</span><span class="sxs-lookup"><span data-stu-id="c10ce-104">Wave processing can be time consuming, and most of the processing time is spent in the allocation step and in the work creation step.</span></span>

<span data-ttu-id="c10ce-105">Nu er det muligt at køre hvert af disse trin parallelt, hvilket kan forbedre ydeevnen af bølgebehandling og give mulighed for større gennemløb af bølger på samme lagersted.</span><span class="sxs-lookup"><span data-stu-id="c10ce-105">It is now possible to run each of these steps in parallel, which can improve the performance of the wave processing, and allow for a larger throughput of waves in the same warehouse.</span></span> <span data-ttu-id="c10ce-106">Dette emne forklarer, hvordan du kan konfigurere metode til tildeling af bølger, så den kører parallelt.</span><span class="sxs-lookup"><span data-stu-id="c10ce-106">This topic explains how to set up the wave allocation method to run in parallel.</span></span> <span data-ttu-id="c10ce-107">Du kan finde flere oplysninger om, hvordan du konfigurerer arbejdsoprettelse til at køre parallelt, under [Planlægge oprettelse af arbejde under bølgen](configure-wave-schedule-work-creation.md).</span><span class="sxs-lookup"><span data-stu-id="c10ce-107">For more information about how to set up work creation to run in parallel, see [Schedule work creation during wave](configure-wave-schedule-work-creation.md).</span></span>

<span data-ttu-id="c10ce-108">Tidligere var det kun muligt at tildele én bølge ad gangen på et lagersted.</span><span class="sxs-lookup"><span data-stu-id="c10ce-108">Previously it was only possible to allocate one wave at a warehouse at a time.</span></span> <span data-ttu-id="c10ce-109">Denne begrænsning er blevet fjernet og erstattet af en ny begrænsning, der kun låser den vare og de dimensioner, der ligger over lokationen i reservationshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="c10ce-109">This constraint has been removed and replaced by a new constraint that only locks the item and dimensions that are above location in the reservation hierarchy.</span></span> <span data-ttu-id="c10ce-110">Dimensioner over lokationen omfatter altid produktdimensioner.</span><span class="sxs-lookup"><span data-stu-id="c10ce-110">Dimensions above the location always include product dimensions.</span></span> <span data-ttu-id="c10ce-111">Hvis en vare f.eks. er konfigureret med *Farve*, kan varianterne *Rød*, *Blå* og *Gul* hver behandles parallelt.</span><span class="sxs-lookup"><span data-stu-id="c10ce-111">For example, if an item is configured using *Color*, then variants for *Red*, *Blue*, and *Yellow* could each be processed in parallel.</span></span>

<span data-ttu-id="c10ce-112">Dette betyder, at hvis den samme vare med samme dimensioner over lokationen tildeles af én bølge, vil andre bølger blive nødt til at vente med at få en lås på samme vare og dimensioner.</span><span class="sxs-lookup"><span data-stu-id="c10ce-112">This means that if the same item with the same dimensions above the location is being allocated by one wave, other waves will have to wait to acquire a lock on the same item and dimensions.</span></span> <span data-ttu-id="c10ce-113">Hvis låsen ikke kan anskaffes i rette tid, opstår der en fejl, og behandling af bølgen mislykkes.</span><span class="sxs-lookup"><span data-stu-id="c10ce-113">If the lock can't be acquired in a timely manner, an error will occur and the wave processing will fail.</span></span>

<span data-ttu-id="c10ce-114">Hvis du vil bruge parallel behandling, skal der køres en bølge i batch.</span><span class="sxs-lookup"><span data-stu-id="c10ce-114">In order to utilize parallel processing, the wave must run in batch.</span></span>

## <a name="performance-improvements"></a><span data-ttu-id="c10ce-115">Forbedringer af ydeevne</span><span class="sxs-lookup"><span data-stu-id="c10ce-115">Performance improvements</span></span>

<span data-ttu-id="c10ce-116">Ydeevnefordelene ved parallel behandling falder i to kategorier:</span><span class="sxs-lookup"><span data-stu-id="c10ce-116">Performance benefits of parallel processing fall in two categories:</span></span>

- <span data-ttu-id="c10ce-117">**Forbedret gennemløb** – Gennemløbet af bølger forbedres typisk, selvom parallel behandling ikke er konfigureret, især for scenarier, hvor der ikke er overlapning af varer i bølgen.</span><span class="sxs-lookup"><span data-stu-id="c10ce-117">**Improved throughput** - The throughput of waves will typically improve even if parallel processing isn't configured, especially for scenarios where there is no overlap of items within the waves.</span></span>
- <span data-ttu-id="c10ce-118">**Forbedring af fordelingen af en enkelt bølge** – Test af kundedata har vist en næsten 50 % ydeevneforbedring efter skift til parallel fordeling.</span><span class="sxs-lookup"><span data-stu-id="c10ce-118">**Improvement of the allocation for a single wave** - Testing on customer data has shown a near 50% performance improvement after switching to parallel allocation.</span></span> <span data-ttu-id="c10ce-119">Den parallelle behandling udføres for de varer og dimensioner, der ligger over lokationen, og derfor afhænger forbedringerne af, hvor mange forskellige varer en bølge indeholder, den tilgængelige infrastruktur og varigheden af fordelingen i forhold til varigheden af oprettelsen af arbejdet.</span><span class="sxs-lookup"><span data-stu-id="c10ce-119">The parallel processing is done per items and dimensions above the location, so the improvements depend on how many different items a wave contains, the infrastructure available, and the duration of the allocation versus the duration of the work creation.</span></span>

## <a name="configure-parallel-allocation"></a><span data-ttu-id="c10ce-120">Konfigurere parallel fordeling</span><span class="sxs-lookup"><span data-stu-id="c10ce-120">Configure parallel allocation</span></span>

### <a name="warehouse-management-parameters"></a><span data-ttu-id="c10ce-121">Parametre til lokationsstyring</span><span class="sxs-lookup"><span data-stu-id="c10ce-121">Warehouse management parameters</span></span>

<span data-ttu-id="c10ce-122">Hvis du vil bruge parallel fordelingsbehandling, skal du gå til **Lokationsstyring > Opsætning > Parametre for lokationsstyring**, åbne fanen **Bølgebehandling** og angive følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="c10ce-122">To use parallel allocation processing, go to **Warehouse management > Setup > Warehouse management parameters**, open the **Wave processing** tab, and make the following settings:</span></span>

- <span data-ttu-id="c10ce-123">**Batchgruppe til behandling af bølger** – Vælg den batchgruppe, som den første behandling af bølgerne skal bruge.</span><span class="sxs-lookup"><span data-stu-id="c10ce-123">**Wave processing batch group** - Select the batch group that the initial processing of the waves should use.</span></span> <span data-ttu-id="c10ce-124">Den efterfølgende behandling af fordelingen kan ske ved hjælp af forskellige batchgrupper.</span><span class="sxs-lookup"><span data-stu-id="c10ce-124">The subsequent processing of allocation can be done using different batch groups.</span></span>
- <span data-ttu-id="c10ce-125">**Udfør behandling af bølger i batch** – Angiv dette til *Ja*, så der bruges parallel behandling.</span><span class="sxs-lookup"><span data-stu-id="c10ce-125">**Process waves in batch** - Set this to *Yes* to use parallel processing.</span></span>
- <span data-ttu-id="c10ce-126">**Vent på lås (ms)** – Angiv tid i millisekunder, som et fordelingstrin venter på en systemressource, der er låst af et andet fordelingstrin.</span><span class="sxs-lookup"><span data-stu-id="c10ce-126">**Wait for lock (ms)** - Enter the time, in milliseconds, that an allocation step will wait for a system resource that is locked by another allocation step.</span></span> <span data-ttu-id="c10ce-127">Når denne tid overskrides, behandles bølgen ikke, og der vises en fejlmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="c10ce-127">When this time is exceeded, the wave is not processed and an error message is displayed.</span></span> <span data-ttu-id="c10ce-128">Det anbefales, at du tillader mindst et par sekunder, før fordelingen af én logisk enhed slutter.</span><span class="sxs-lookup"><span data-stu-id="c10ce-128">We recommend that you allow at least a few seconds to allow for allocation of one logical unit to finish.</span></span>

<span data-ttu-id="c10ce-129">Du kan finde oplysninger om disse og andre indstillinger for behandling af bølger på siden **Parametre for lokationsstyring** under [Lagerstedsparametre til bølgebehandling](wave-warehouse-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c10ce-129">For information about these and other wave processing options on the **Warehouse management parameters** page, see [Warehouse parameters for wave processing](wave-warehouse-parameters.md).</span></span>

## <a name="wave-process-methods"></a><span data-ttu-id="c10ce-130">Metoder til bølgeproces</span><span class="sxs-lookup"><span data-stu-id="c10ce-130">Wave process methods</span></span>

<span data-ttu-id="c10ce-131">Sådan konfigurerer du parallel behandling:</span><span class="sxs-lookup"><span data-stu-id="c10ce-131">To set up parallel processing:</span></span>

1. <span data-ttu-id="c10ce-132">Gå til **Lokationsstyring > Konfiguration > Bølger > Bølgeprocesmetoder**.</span><span class="sxs-lookup"><span data-stu-id="c10ce-132">Go to **Warehouse Management > Setup > Waves > Wave process methods**.</span></span>
1. <span data-ttu-id="c10ce-133">Vælg metoden `allocateWave` i gitteret.</span><span class="sxs-lookup"><span data-stu-id="c10ce-133">Select the `allocateWave` method in the grid.</span></span>
1. <span data-ttu-id="c10ce-134">Vælg **Opgavekonfiguration** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="c10ce-134">On the Action Pane, select **Task configuration**.</span></span>
1. <span data-ttu-id="c10ce-135">Siden **Konfiguration af opgave til bølgebogføringsmetode** åbnes.</span><span class="sxs-lookup"><span data-stu-id="c10ce-135">The **Wave post method task configuration** page opens.</span></span> <span data-ttu-id="c10ce-136">Dette gitter viser de enkelte lagersteder, hvor du har konfigureret `allocateWave`-metoden.</span><span class="sxs-lookup"><span data-stu-id="c10ce-136">This grid lists each warehouse where you have configured the `allocateWave` method.</span></span> <span data-ttu-id="c10ce-137">Parallel behandling bruges kun til lagerstederne på listen.</span><span class="sxs-lookup"><span data-stu-id="c10ce-137">Parallel processing will only be used for warehouses that are listed.</span></span> <span data-ttu-id="c10ce-138">Brug knapperne i handlingsruden til at tilføje eller fjerne lagersteder fra gitteret efter behov.</span><span class="sxs-lookup"><span data-stu-id="c10ce-138">Use the Action Pane buttons to add or remove warehouses from the grid as needed.</span></span> 
1. <span data-ttu-id="c10ce-139">For hvert lagersted skal du foretage følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="c10ce-139">For each warehouse, make the following settings:</span></span>
    - <span data-ttu-id="c10ce-140">**Maksimalt antal batchopgaver** – Angiv det antal batchopgaver, der skal bruges til fordelingen for det valgte lagersted.</span><span class="sxs-lookup"><span data-stu-id="c10ce-140">**Maximum number of batch tasks** - Specify the number of batch tasks that should be used for the allocation for the selected warehouse.</span></span> <span data-ttu-id="c10ce-141">Det optimale antal batchopgaver afhænger af den tilgængelige infrastruktur, og hvilke andre batchjob der behandles på serveren.</span><span class="sxs-lookup"><span data-stu-id="c10ce-141">The optimal number of batch tasks depends on the infrastructure available and what other batch jobs are being processed on the server.</span></span> <span data-ttu-id="c10ce-142">Test udført på et firekernemiljø, der var dedikeret til behandling af bølger, har vist, at brug af otte opgaver giver gode resultater.</span><span class="sxs-lookup"><span data-stu-id="c10ce-142">Tests done on a four core environment that was dedicated to wave processing showed that using eight tasks produced good results.</span></span>
    - <span data-ttu-id="c10ce-143">**Batchgruppe til bølgebehandling** – Bestemte batchgrupper kan bruges til forskellige lagersteder for at tillade, at fordelingsbehandlingen skaleres ud pr. lagersted.</span><span class="sxs-lookup"><span data-stu-id="c10ce-143">**Wave processing batch group** - Specific batch groups can be used for different warehouses to allow the allocation processing to scale out per warehouse.</span></span>

## <a name="enable-or-disable-parallelization-across-all-legal-entities"></a><span data-ttu-id="c10ce-144">Aktivere eller deaktivere parallelisering på tværs af alle juridiske enheder</span><span class="sxs-lookup"><span data-stu-id="c10ce-144">Enable or disable parallelization across all legal entities</span></span>

<span data-ttu-id="c10ce-145">Det anbefales, at du angiver metoden `allocateWave` til at køre parallelt på tværs af alle juridiske enheder, da det er med til at forbedre ydeevnen af bølgebehandling.</span><span class="sxs-lookup"><span data-stu-id="c10ce-145">We recommend that you set the `allocateWave` method to run in parallel across all legal entities because this helps to improve the performance of the wave processing.</span></span> <span data-ttu-id="c10ce-146">Fra og med Supply Chain Management version 10.0.17 aktiveres funktionen *Bølgeparallelisering af Tilde bølge-metode* som standard for alle nye og opdaterede installationer, og den kan ikke deaktiveres igen.</span><span class="sxs-lookup"><span data-stu-id="c10ce-146">Starting in Supply Chain Management version 10.0.17, the *Wave parallelization for Allocate Wave method* feature is enabled by default for all new and updated installations, and can't be turned off again.</span></span> <span data-ttu-id="c10ce-147">Når du har aktiveret denne funktion, sker følgende:</span><span class="sxs-lookup"><span data-stu-id="c10ce-147">After enabling this feature, the following occurs:</span></span>

- <span data-ttu-id="c10ce-148">Metoden `allocateWave` opdateres, så den indeholder en indstilling for opgavekonfiguration, som giver dig mulighed for at bruge siden **Bølgeprocesmetoder** til at definere antallet af opgaver, der skal køres samtidigt, hvilket svarer til antallet af parallelle processer.</span><span class="sxs-lookup"><span data-stu-id="c10ce-148">The `allocateWave` method is updated to include a task configuration setting that lets you use the **Wave process methods** page to define the number of tasks that will run simultaneously, equivalent to the number of parallel processes.</span></span> <span data-ttu-id="c10ce-149">Som følge heraf reduceres den tid, der bruges på trinnet Tildel bølge (som typisk er 30 % til 60 % af den samlede behandlingstid) med en faktor, der stort set svarer til antallet af opgaver.</span><span class="sxs-lookup"><span data-stu-id="c10ce-149">As a result, the time used on the allocate-wave step (which is typically 30% to 60% of the total processing time) is reduced by a factor roughly equivalent to the number of tasks.</span></span> <span data-ttu-id="c10ce-150">Det er også muligt at vælge, hvilket batch der skal tildeles for at behandle disse opgaver.</span><span class="sxs-lookup"><span data-stu-id="c10ce-150">It's also possible to select which batch will be assigned to process these tasks.</span></span> <span data-ttu-id="c10ce-151">Det er vigtigt at bemærke, at alle de juridiske enheder konfigureres til at behandle bølger i batch.</span><span class="sxs-lookup"><span data-stu-id="c10ce-151">It's important to note that all of your legal entities will be configured to process waves in batch.</span></span> <span data-ttu-id="c10ce-152">For de lagersteder, der allerede er konfigureret til at behandle bølger i batch, og for de lagersteder, der allerede er konfigureret til at bruge metoden `allocateWave` parallelt, bevares den eksisterende konfiguration.</span><span class="sxs-lookup"><span data-stu-id="c10ce-152">For the warehouses that are already configured to process waves in batch, and for the warehouses that are already configured to use the `allocateWave` method in parallel, the existing configuration will be kept.</span></span>
- <span data-ttu-id="c10ce-153">Som standard er alle de nye juridiske enheder konfigureret til at behandle bølger i batch.</span><span class="sxs-lookup"><span data-stu-id="c10ce-153">By default, all the new legal entities are configured to process waves in batch.</span></span> <span data-ttu-id="c10ce-154">Alle nye lagersteder, hvor indstillingen **Lokationsstyringsprocesser** er aktiveret, vil have metoden `allocateWave` konfigureret til at køre parallelt som standard.</span><span class="sxs-lookup"><span data-stu-id="c10ce-154">All new warehouses with the **Warehouse management processes** option enabled will have the `allocateWave` method configured to run in parallel by default.</span></span>
- <span data-ttu-id="c10ce-155">På siden **Parametre for lokationsstyring** angives **Udfør behandling af bølger i batch** til *Ja* og **Vent på lås (ms)** er angivet til standarden 15 sekunder.</span><span class="sxs-lookup"><span data-stu-id="c10ce-155">On the **Warehouse management parameters** page, **Process saves in batch** is set to *Yes* and  **Wait for lock (ms)** set to a default 15 seconds.</span></span> <span data-ttu-id="c10ce-156">Det betyder, at alle bølger udføres i batch.</span><span class="sxs-lookup"><span data-stu-id="c10ce-156">This means that all waves will be executed in batch.</span></span> <span data-ttu-id="c10ce-157">Når en bølge kører, får den en lås på varen og dimensionerne over lokationen under fordelingstrinnet.</span><span class="sxs-lookup"><span data-stu-id="c10ce-157">When a wave is running, it acquires a lock on the item and dimensions above location during the allocation step.</span></span> <span data-ttu-id="c10ce-158">Når en anden bølgebehandlingsopgave forsøger at få den samme lås for den samme post, blokeres den, indtil den aktuelle proces er færdig.</span><span class="sxs-lookup"><span data-stu-id="c10ce-158">When another wave processing task tries to acquire the same lock for the identical record, it is blocked until the current process is finished.</span></span> <span data-ttu-id="c10ce-159">Indstillingerne **Vent på lås (ms)** fastsætter den maksimale tid, systemet vil vente, før låsen frigives.</span><span class="sxs-lookup"><span data-stu-id="c10ce-159">The **Wait for lock (ms)** settings establishes the maximum time the system will wait before the lock is released.</span></span>

<span data-ttu-id="c10ce-160">Parallel fordelingsbehandling kræver, at der køres bølgebehandling i batch.</span><span class="sxs-lookup"><span data-stu-id="c10ce-160">Parallel allocation processing requires wave processing to run in batch.</span></span> <span data-ttu-id="c10ce-161">Du vil derfor reducere den ydeevne, du bruger til behandling af bølger, hvis du deaktiverer indstillingen **Udfør behandling af bølger i batch**, specielt hvis behandling af bølger bruger en parallel proces som defineret af opgavekonfigurationen for de relevante bølgemetoder.</span><span class="sxs-lookup"><span data-stu-id="c10ce-161">Therefore, you will reduce your wave processing performance if you turn off the **Process saves in batch** setting, especially if wave processing is using a parallel process as defined by the task configuration for the relevant wave methods.</span></span>

<span data-ttu-id="c10ce-162">Hvis det er nødvendigt, kan du fortryde hver af de indstillinger, der er foretaget som standard, når funktionen *Bølgeparallelisering af Tilde bølge-metode* automatisk aktiveres for din forekomst.</span><span class="sxs-lookup"><span data-stu-id="c10ce-162">If necessary, you can undo each of the settings made by default when the *Wave parallelization for Allocate Wave method* feature is automatically enabled for your instance.</span></span> <span data-ttu-id="c10ce-163">Sådan gør du dette:</span><span class="sxs-lookup"><span data-stu-id="c10ce-163">To do this:</span></span>

- <span data-ttu-id="c10ce-164">Gå til **Lokationsstyring \> Konfiguration \> Parametre til lokationsstyring**.</span><span class="sxs-lookup"><span data-stu-id="c10ce-164">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span> <span data-ttu-id="c10ce-165">Anvend dine foretrukne værdier for **Udfør behandling af bølger i batch** og **Vent på lås (ms)** under fanen **Bølgebehandling**.</span><span class="sxs-lookup"><span data-stu-id="c10ce-165">On the **Wave processing** tab, apply your preferred values for **Process waves in batch** and **Wait for lock (ms)**.</span></span>
- <span data-ttu-id="c10ce-166">Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgeprocesmetoder**.</span><span class="sxs-lookup"><span data-stu-id="c10ce-166">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span> <span data-ttu-id="c10ce-167">Vælg metoden `allocateWave`.</span><span class="sxs-lookup"><span data-stu-id="c10ce-167">Select the `allocateWave` method.</span></span> <span data-ttu-id="c10ce-168">Vælg **Opgavekonfiguration** i handlingsruden for at åbne en side med en oversigt over hvert lagersted, hvor metoden er indstillet til at køre parallelt.</span><span class="sxs-lookup"><span data-stu-id="c10ce-168">On the Action Pane, select **Task configuration** to open a page that lists each warehouse where the method is set to run in parallel.</span></span> <span data-ttu-id="c10ce-169">Rediger eller slet antallet af batchopgaver og den tildelte bølgegruppe for hvert af de viste lagersteder efter behov.</span><span class="sxs-lookup"><span data-stu-id="c10ce-169">Modify or delete the number of batch tasks and the assigned wave group for each listed warehouse as needed.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="c10ce-170">Fejlfinding</span><span class="sxs-lookup"><span data-stu-id="c10ce-170">Troubleshooting</span></span>

### <a name="troubleshoot-using-the-infolog"></a><span data-ttu-id="c10ce-171">Foretage fejlfinding af infologgen</span><span class="sxs-lookup"><span data-stu-id="c10ce-171">Troubleshoot using the Infolog</span></span>

<span data-ttu-id="c10ce-172">Da batchstrukturen bruges, registreres fejl, der opstår under behandling af bølger, som en del af infologgen til batchjobbene.</span><span class="sxs-lookup"><span data-stu-id="c10ce-172">Because the batch framework is used, errors that occur during wave processing will be captured as part of the batch jobs Infologs.</span></span> <span data-ttu-id="c10ce-173">Sådan aflæser du de batchjob, der er relateret til en bølge:</span><span class="sxs-lookup"><span data-stu-id="c10ce-173">To read the batch jobs related to a wave:</span></span>

1. <span data-ttu-id="c10ce-174">Gå til **Lokationsstyring \> Udgående bølger \> Forsendelsesbølger \> Alle bølger**.</span><span class="sxs-lookup"><span data-stu-id="c10ce-174">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="c10ce-175">Vælg den bølge, der skal inspiceres.</span><span class="sxs-lookup"><span data-stu-id="c10ce-175">Select the wave you want to inspect.</span></span>
1. <span data-ttu-id="c10ce-176">Åbn fanen **Bølge** i handlingsruden, og vælg **Batchjob** i gruppen **Bølge**.</span><span class="sxs-lookup"><span data-stu-id="c10ce-176">On the Action Pane, open the **Wave** tab and, from the **Wave** group, select **Batch jobs**.</span></span>

<span data-ttu-id="c10ce-177">Bølgebehandling er selvkorrigerende, så alle fejl, der registreres under behandlingen, skulle blive rapporteret i infologgen.</span><span class="sxs-lookup"><span data-stu-id="c10ce-177">Wave processing is self-correcting, so any error detected during processing should be reported using the Infolog.</span></span>

<span data-ttu-id="c10ce-178">En typisk fejl, der er relateret til parallel behandling, kan være, at to bølger forsøger at tildele den samme vare samtidig, og at den ene ikke fuldføres, så den anden bølge ikke kan få en lås inden for den angivne tid.</span><span class="sxs-lookup"><span data-stu-id="c10ce-178">A typical error related to parallel processing could be that two waves try to allocate the same item at the same time and one does not complete so that the other wave is unable to acquire a lock within the specified time.</span></span> <span data-ttu-id="c10ce-179">Hvis denne situation opstår, indeholder batchjobloggen oplysninger om, at låsen for varen ikke kunne anskaffes. I så fald skal den bølge, der mislykkedes, behandles igen.</span><span class="sxs-lookup"><span data-stu-id="c10ce-179">If this situation occurs, the batch jobs log will contain information stating that the lock for the item could not be acquired, in which case the wave that failed must be processed again.</span></span>

<span data-ttu-id="c10ce-180">Da behandlingen sker parallelt, skal data vedligeholdes i forskellige tabeller for at spore behandlingstilstanden.</span><span class="sxs-lookup"><span data-stu-id="c10ce-180">Because the processing is happening in parallel, data must be maintained in different tables to track the state of the processing.</span></span> <span data-ttu-id="c10ce-181">Det betyder, at logfilerne for batchjobbene kan indeholde fejl, f.eks. fejl med om identiske nøgler.</span><span class="sxs-lookup"><span data-stu-id="c10ce-181">This means that the logs for the batch jobs might contain errors such as duplicate key errors.</span></span>

<span data-ttu-id="c10ce-182">Fejlene fra batchopgaverne er også en del af batchjobloggen.</span><span class="sxs-lookup"><span data-stu-id="c10ce-182">The errors from the batch tasks are also part of the batch jobs log.</span></span> <span data-ttu-id="c10ce-183">De vigtigste oplysninger vises typisk i bunden.</span><span class="sxs-lookup"><span data-stu-id="c10ce-183">The most important information is typically at the bottom.</span></span>

<span data-ttu-id="c10ce-184">I sjældne tilfælde, hvis SQL-forbindelsen f.eks. afbrydes, kan bølgebehandlingen afsluttes i en uoverensstemmende tilstand, hvor batchjobbet ser ud til at køre, men behandlingen stoppes.</span><span class="sxs-lookup"><span data-stu-id="c10ce-184">In rare cases, for example if the SQL connection ended, it is possible for the wave processing to end in an inconsistent state where the batch job appears to be running but the processing is stopped.</span></span> <span data-ttu-id="c10ce-185">Bølgen kan ikke håndtere fejl som denne, så der udføres et forsøg på at rydde op i mislykkede bølger, når næste bølge køres.</span><span class="sxs-lookup"><span data-stu-id="c10ce-185">The wave can't handle errors like this, so an attempt to clean up failed waves is done when the next wave runs.</span></span> <span data-ttu-id="c10ce-186">Hvis den aktuelle bølge har uoverensstemmende tilstand, kan du også udføre følgende trin:</span><span class="sxs-lookup"><span data-stu-id="c10ce-186">Alternatively, if the current wave is in an inconsistent state, perform the following steps:</span></span>

1. <span data-ttu-id="c10ce-187">Gå til **Lokationsstyring \> Udgående bølger \> Forsendelsesbølger \> Alle bølger**.</span><span class="sxs-lookup"><span data-stu-id="c10ce-187">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="c10ce-188">Vælg den bølge, der skal ryddes op i.</span><span class="sxs-lookup"><span data-stu-id="c10ce-188">Select the wave you need to clean up.</span></span>
1. <span data-ttu-id="c10ce-189">Åbn fanen **Bølge** i handlingsruden, og vælg **Oprydning af bølgedata** i gruppen **Bølge**.</span><span class="sxs-lookup"><span data-stu-id="c10ce-189">On the Action Pane, open the **Wave** tab and, in the **Wave** group, select **Cleanup wave data**.</span></span>

### <a name="troubleshoot-using-the-wave-progress-log"></a><span data-ttu-id="c10ce-190">Foretage fejlfinding ved hjælp af log over bølgestatus</span><span class="sxs-lookup"><span data-stu-id="c10ce-190">Troubleshoot using the wave progress log</span></span>

<span data-ttu-id="c10ce-191">Hvis indstillingen **Opret log over bølgestatus** er aktiveret på siden **Parametre for lokationsstyring**, oprettes der en logpost, hver gang fordelingen for en vare og dens dimensioner starter og slutter.</span><span class="sxs-lookup"><span data-stu-id="c10ce-191">If the **Create wave progress log** option is enabled on the **Warehouse management parameters** page, then a log record is created every time allocation for an item and its dimensions begins and ends.</span></span> <span data-ttu-id="c10ce-192">Du skal kun aktivere denne log, når du har brug for den, f.eks. under den indledende test eller ved fejlfinding.</span><span class="sxs-lookup"><span data-stu-id="c10ce-192">You should only enable this log when you need it, for example, during initial testing or for troubleshooting.</span></span> <span data-ttu-id="c10ce-193">Når denne indstilling er aktiveret, kan du få vist loggen ved at følge nedenstående trin:</span><span class="sxs-lookup"><span data-stu-id="c10ce-193">When this option is enabled, you can view the log by taking the following steps:</span></span>

1. <span data-ttu-id="c10ce-194">Gå til **Lokationsstyring \> Udgående bølger \> Forsendelsesbølger \> Alle bølger**.</span><span class="sxs-lookup"><span data-stu-id="c10ce-194">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="c10ce-195">Vælg den bølge, der skal inspiceres.</span><span class="sxs-lookup"><span data-stu-id="c10ce-195">Select the wave you want to inspect.</span></span>
1. <span data-ttu-id="c10ce-196">I handlingsruden under fanen **Bølge** i gruppen **Bølge** skal du vælge **Status**.</span><span class="sxs-lookup"><span data-stu-id="c10ce-196">On the Action Pane, open the **Wave** tab and, in the **Wave** group, select **Progress**.</span></span>