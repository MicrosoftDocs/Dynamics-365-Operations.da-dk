---
title: Introduktion til Planlægningsoptimering
description: I dette emne beskrives, hvordan du kommer i gang med at bruge funktionen Planlægningsoptimering.
author: ChristianRytt
manager: tfehr
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 4f9124e824a0b6d5035b2567cb19c2c494390d55
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213509"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="1b3b9-103">Introduktion til Planlægningsoptimering</span><span class="sxs-lookup"><span data-stu-id="1b3b9-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1b3b9-104">Funktionen Planlægningsoptimering understøtter i øjeblikket ikke alle de funktioner, der er tilgængelige i det planlægningsprogram, der er indbygget i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1b3b9-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="1b3b9-105">Det er derfor vigtigt, at du evaluerer, om det funktionssæt, der aktuelt er tilgængeligt i Planlægningsoptimering, opfylder dine behov.</span><span class="sxs-lookup"><span data-stu-id="1b3b9-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="1b3b9-106">Funktionen Planlægningsoptimering er som standard ikke slået til i Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="1b3b9-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="1b3b9-107">Derfor har du mulighed for at foretage evalueringen, før den aktiveres.</span><span class="sxs-lookup"><span data-stu-id="1b3b9-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="1b3b9-108">Til sidst erstatter Planlægningsoptimering det eksisterende indbyggede planlægningsprogram Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1b3b9-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="1b3b9-109">Før du slår Planlægningsoptimering til, anbefales det på det kraftigste, at du evaluerer resultaterne af analysen af om Planlægningsoptimering passer.</span><span class="sxs-lookup"><span data-stu-id="1b3b9-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="1b3b9-110">Du kan finde flere oplysninger under [Analyse af om Planlægningsoptimering passer](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="1b3b9-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="licensing"></a><span data-ttu-id="1b3b9-111">Licenser</span><span class="sxs-lookup"><span data-stu-id="1b3b9-111">Licensing</span></span>

<span data-ttu-id="1b3b9-112">Hvis du kan køre varedisponering ved hjælp af din aktuelle licens, behøver du ikke købe en ekstra licens for at begynde at bruge Planlægningsoptimering.</span><span class="sxs-lookup"><span data-stu-id="1b3b9-112">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="1b3b9-113">Installer tilføjelsesprogrammet</span><span class="sxs-lookup"><span data-stu-id="1b3b9-113">Install the add-in</span></span>

<span data-ttu-id="1b3b9-114">Hvis du vil bruge Planlægningsoptimering, skal du installere tilføjelsesprogrammet Planlægningsoptimering til Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1b3b9-114">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="1b3b9-115">Du kan få adgang til tilføjelsesprogrammet fra dit LCS projekt og slå Planlægningsoptimeringsfunktionen til fra brugergrænsefladen til Supply Chain Management (UI).</span><span class="sxs-lookup"><span data-stu-id="1b3b9-115">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

> [!NOTE]
> <span data-ttu-id="1b3b9-116">Behovet for planlægningsoptimering er et LCS-aktiveret miljø med høj tilgængelighed (ikke et Onebox-miljø) i Dynamics 365 Supply Chain Management, version 10.0.7 eller nyere.</span><span class="sxs-lookup"><span data-stu-id="1b3b9-116">The requirement for Planning Optimization is an LCS enabled high-availability environment (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span>

1. <span data-ttu-id="1b3b9-117">Log på LCS, og åbn det ønskede miljø.</span><span class="sxs-lookup"><span data-stu-id="1b3b9-117">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="1b3b9-118">Gå til **Alle detaljer**.</span><span class="sxs-lookup"><span data-stu-id="1b3b9-118">Go to **Full details**.</span></span>
1. <span data-ttu-id="1b3b9-119">Rul ned til oversigtspanelet **Tilføjelsesprogrammer for miljø**.</span><span class="sxs-lookup"><span data-stu-id="1b3b9-119">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="1b3b9-120">Vælg **Installer et nyt tilføjelsesprogram**.</span><span class="sxs-lookup"><span data-stu-id="1b3b9-120">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="1b3b9-121">Vælg **Planlægningsoptimering**.</span><span class="sxs-lookup"><span data-stu-id="1b3b9-121">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="1b3b9-122">Følg installationsvejledningen, og accepter vilkårene og betingelserne.</span><span class="sxs-lookup"><span data-stu-id="1b3b9-122">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="1b3b9-123">Vælg **Installer**.</span><span class="sxs-lookup"><span data-stu-id="1b3b9-123">Select **Install**.</span></span>
1. <span data-ttu-id="1b3b9-124">I oversigtspanelet **Tilføjelsesprogrammer for miljø** kan du se, at Planlægningsoptimering er ved at blive installeret.</span><span class="sxs-lookup"><span data-stu-id="1b3b9-124">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="1b3b9-125">Efter nogle minutter bør **Installerer** blive ændret til **Installeret** (du skal muligvis opdatere siden).</span><span class="sxs-lookup"><span data-stu-id="1b3b9-125">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="1b3b9-126">Når den er installeret, er du klar til at aktivere Planlægningsoptimering i Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1b3b9-126">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="1b3b9-127">Integration af Planlægningsoptimering</span><span class="sxs-lookup"><span data-stu-id="1b3b9-127">Planning Optimization integration</span></span>

<span data-ttu-id="1b3b9-128">Hvis du vil konfigurere, om tilføjelsesprogrammet til Planlægningsoptimering skal bruges til varedisponering, skal du gå til **Varedisponering** \> **Opsætning** \> **Parametre for Planlægningsoptimering**.</span><span class="sxs-lookup"><span data-stu-id="1b3b9-128">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="1b3b9-129">Forbindelsesstatus</span><span class="sxs-lookup"><span data-stu-id="1b3b9-129">Connection status</span></span>

<span data-ttu-id="1b3b9-130">Forbindelsesstatussen angiver den aktuelle status for forbindelsen mellem Supply Chain Management og tjenesten Planlægningsoptimering.</span><span class="sxs-lookup"><span data-stu-id="1b3b9-130">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="1b3b9-131">I følgende tabel vises de mulige værdier.</span><span class="sxs-lookup"><span data-stu-id="1b3b9-131">The following table shows the possible values.</span></span>

| <span data-ttu-id="1b3b9-132">Forbindelsesstatus</span><span class="sxs-lookup"><span data-stu-id="1b3b9-132">Connection status</span></span> | <span data-ttu-id="1b3b9-133">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="1b3b9-133">Description</span></span> | <span data-ttu-id="1b3b9-134">Kan Planlægningsoptimering anvendes?</span><span class="sxs-lookup"><span data-stu-id="1b3b9-134">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="1b3b9-135">Tilsluttet</span><span class="sxs-lookup"><span data-stu-id="1b3b9-135">Connected</span></span> | <span data-ttu-id="1b3b9-136">Der er oprettet en forbindelse mellem Planlægningsoptimeringstjenesten og Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1b3b9-136">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="1b3b9-137">Ja</span><span class="sxs-lookup"><span data-stu-id="1b3b9-137">Yes</span></span> |
| <span data-ttu-id="1b3b9-138">Forbindelse aktiveres</span><span class="sxs-lookup"><span data-stu-id="1b3b9-138">Enabling connection</span></span> | <span data-ttu-id="1b3b9-139">En anmodning om at aktivere forbindelsen til Planlægningsoptimeringstjenesten er i øjeblikket i gang.</span><span class="sxs-lookup"><span data-stu-id="1b3b9-139">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="1b3b9-140">Nr.</span><span class="sxs-lookup"><span data-stu-id="1b3b9-140">No</span></span> |
| <span data-ttu-id="1b3b9-141">Forbindelse afbrudt</span><span class="sxs-lookup"><span data-stu-id="1b3b9-141">Disconnected</span></span> | <span data-ttu-id="1b3b9-142">Der er ingen forbindelse til Planlægningsoptimeringstjenesten.</span><span class="sxs-lookup"><span data-stu-id="1b3b9-142">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="1b3b9-143">Forbindelsen kan slås til fra LCS, som beskrevet tidligere i dette emne.</span><span class="sxs-lookup"><span data-stu-id="1b3b9-143">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="1b3b9-144">Nr.</span><span class="sxs-lookup"><span data-stu-id="1b3b9-144">No</span></span> |
| <span data-ttu-id="1b3b9-145">Forbindelse deaktiveres</span><span class="sxs-lookup"><span data-stu-id="1b3b9-145">Disabling connection</span></span> | <span data-ttu-id="1b3b9-146">En anmodning om at deaktivere forbindelsen til Planlægningsoptimeringstjenesten er i øjeblikket i gang.</span><span class="sxs-lookup"><span data-stu-id="1b3b9-146">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="1b3b9-147">Nr.</span><span class="sxs-lookup"><span data-stu-id="1b3b9-147">No</span></span> |
| <span data-ttu-id="1b3b9-148">Henter status</span><span class="sxs-lookup"><span data-stu-id="1b3b9-148">Getting status</span></span> | <span data-ttu-id="1b3b9-149">Systemet venter på statusoplysninger fra Planlægningsoptimeringstjenesten.</span><span class="sxs-lookup"><span data-stu-id="1b3b9-149">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="1b3b9-150">Nr.</span><span class="sxs-lookup"><span data-stu-id="1b3b9-150">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="1b3b9-151">Indstillingen Brug Planlægningsoptimering</span><span class="sxs-lookup"><span data-stu-id="1b3b9-151">The Use Planning Optimization option</span></span>

<span data-ttu-id="1b3b9-152">Indstillingen af indstillingen **Brug Planlægningsoptimering** bestemmer, hvilket planlægningsprogram der bruges til varedisponering:</span><span class="sxs-lookup"><span data-stu-id="1b3b9-152">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="1b3b9-153">**Ja** – Planlægningsoptimering bruges til varedisponering.</span><span class="sxs-lookup"><span data-stu-id="1b3b9-153">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="1b3b9-154">**Nej** – Det indbyggede planlægningsprogram for Supply Chain Management bruges til varedisponering.</span><span class="sxs-lookup"><span data-stu-id="1b3b9-154">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="1b3b9-155">Hvis de eksisterende planlægningsbatchjob, der blev oprettet til det indbyggede planlægningsprogram for Supply Chain Management, udløses mens indstillingen **Brug Planlægningsoptimering** er angivet til **Ja**, vil disse job ikke blive udført.</span><span class="sxs-lookup"><span data-stu-id="1b3b9-155">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="1b3b9-156">Integration med opsætningen</span><span class="sxs-lookup"><span data-stu-id="1b3b9-156">Integration with the setup</span></span>

<span data-ttu-id="1b3b9-157">Hvis forhåndsvisningen af Planlægningsoptimering er aktiveret, foretages varedisponering ved hjælp af tilføjelsesprogrammet for Planlægningsoptimering.</span><span class="sxs-lookup"><span data-stu-id="1b3b9-157">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="1b3b9-158">I dette tilfælde påvirkes resultaterne af og funktionerne for varedisponering.</span><span class="sxs-lookup"><span data-stu-id="1b3b9-158">In this case, master planning results and features are affected.</span></span>

## <a name="related-resources"></a><span data-ttu-id="1b3b9-159">Tilknyttede ressourcer</span><span class="sxs-lookup"><span data-stu-id="1b3b9-159">Related resources</span></span>

[<span data-ttu-id="1b3b9-160">Vilkår og betingelser for forhåndsvisning</span><span class="sxs-lookup"><span data-stu-id="1b3b9-160">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="1b3b9-161">Oversigt over Planlægningsoptimering</span><span class="sxs-lookup"><span data-stu-id="1b3b9-161">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="1b3b9-162">Analyse af om Planlægningsoptimering passer til</span><span class="sxs-lookup"><span data-stu-id="1b3b9-162">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="1b3b9-163">Få vist planhistorik og planlægningslogs</span><span class="sxs-lookup"><span data-stu-id="1b3b9-163">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="1b3b9-164">Anvend filtre på en plan</span><span class="sxs-lookup"><span data-stu-id="1b3b9-164">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="1b3b9-165">Annullere et planlægningsjob</span><span class="sxs-lookup"><span data-stu-id="1b3b9-165">Cancel a planning job</span></span>](cancel-planning-job.md)
