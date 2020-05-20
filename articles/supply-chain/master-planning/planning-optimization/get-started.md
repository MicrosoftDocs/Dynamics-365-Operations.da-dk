---
title: Introduktion til Planlægningsoptimering
description: I dette emne beskrives, hvordan du kommer i gang med at bruge funktionen Planlægningsoptimering.
author: ChristianRytt
manager: tfehr
ms.date: 05/06/2020
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
ms.openlocfilehash: ce1bbb18e9a448e84d001a4195421d2b0e4af5be
ms.sourcegitcommit: c0d37fdd70f3dec4605fdee6f981f84a49be9b9e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/06/2020
ms.locfileid: "3339872"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="85824-103">Introduktion til Planlægningsoptimering</span><span class="sxs-lookup"><span data-stu-id="85824-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="85824-104">Funktionen Planlægningsoptimering understøtter i øjeblikket ikke alle de funktioner, der er tilgængelige i det planlægningsprogram, der er indbygget i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="85824-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="85824-105">Det er derfor vigtigt, at du evaluerer, om det funktionssæt, der aktuelt er tilgængeligt i Planlægningsoptimering, opfylder dine behov.</span><span class="sxs-lookup"><span data-stu-id="85824-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="85824-106">Funktionen Planlægningsoptimering er som standard ikke slået til i Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="85824-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="85824-107">Derfor har du mulighed for at foretage evalueringen, før den aktiveres.</span><span class="sxs-lookup"><span data-stu-id="85824-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="85824-108">Til sidst erstatter Planlægningsoptimering det eksisterende indbyggede planlægningsprogram Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="85824-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="85824-109">Før du slår Planlægningsoptimering til, anbefales det på det kraftigste, at du evaluerer resultaterne af analysen af om Planlægningsoptimering passer.</span><span class="sxs-lookup"><span data-stu-id="85824-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="85824-110">Du kan finde flere oplysninger under [Analyse af om Planlægningsoptimering passer](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="85824-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="availability"></a><span data-ttu-id="85824-111">Tilgængelighed</span><span class="sxs-lookup"><span data-stu-id="85824-111">Availability</span></span>
<span data-ttu-id="85824-112">Planlægningsoptimering er i øjeblikket tilgængelig i følgende Azure-områder: USA, Canada, Europa, Storbritannien og Australien.</span><span class="sxs-lookup"><span data-stu-id="85824-112">Planning Optimization is currently available in the following Azure geographies: United States, Canada, Europe, United Kingdom, and Australia.</span></span> <span data-ttu-id="85824-113">Hvis du forsøger at installere tilføjelsesprogrammet fra et andet geografisk område, vil LCS vise en meddelelse om, at dette geografiske område ikke understøttes.</span><span class="sxs-lookup"><span data-stu-id="85824-113">If you try to install the add-in from another geographic region, then LCS will show a message that this geographic is not supported.</span></span>

<span data-ttu-id="85824-114">Bemærk, at planlægningsoptimering ikke understøtter lokale installationer af Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="85824-114">Note that Planning Optimization does not support on-premises deployments of Dynamics 365 Supply Chain Management.</span></span>

### <a name="licensing"></a><span data-ttu-id="85824-115">Licensering</span><span class="sxs-lookup"><span data-stu-id="85824-115">Licensing</span></span>

<span data-ttu-id="85824-116">Hvis du kan køre varedisponering ved hjælp af din aktuelle licens, behøver du ikke købe en ekstra licens for at begynde at bruge Planlægningsoptimering.</span><span class="sxs-lookup"><span data-stu-id="85824-116">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="85824-117">Installer tilføjelsesprogrammet</span><span class="sxs-lookup"><span data-stu-id="85824-117">Install the add-in</span></span>

<span data-ttu-id="85824-118">Hvis du vil bruge Planlægningsoptimering, skal du installere tilføjelsesprogrammet Planlægningsoptimering til Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="85824-118">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="85824-119">Du kan få adgang til tilføjelsesprogrammet fra dit LCS projekt og slå Planlægningsoptimeringsfunktionen til fra brugergrænsefladen til Supply Chain Management (UI).</span><span class="sxs-lookup"><span data-stu-id="85824-119">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

> [!NOTE]
> <span data-ttu-id="85824-120">Behovet for planlægningsoptimering er et LCS-aktiveret miljø med høj tilgængelighed på niveau 2 eller højere (ikke et Onebox-miljø) i Dynamics 365 Supply Chain Management, version 10.0.7 eller nyere.</span><span class="sxs-lookup"><span data-stu-id="85824-120">The requirement for Planning Optimization is an LCS enabled high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="85824-121">Hvis du forsøger at installere tilføjelsesprogrammet i et OneBox-miljø, fuldføres installationen ikke, og du skal annullere installationen.</span><span class="sxs-lookup"><span data-stu-id="85824-121">If you try to install the add-in on a OneBox environment, the installation will not complete and you will need to cancel the installation.</span></span>

1. <span data-ttu-id="85824-122">Log på LCS, og åbn det ønskede miljø.</span><span class="sxs-lookup"><span data-stu-id="85824-122">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="85824-123">Gå til **Alle detaljer**.</span><span class="sxs-lookup"><span data-stu-id="85824-123">Go to **Full details**.</span></span>
1. <span data-ttu-id="85824-124">Rul ned til oversigtspanelet **Tilføjelsesprogrammer for miljø**.</span><span class="sxs-lookup"><span data-stu-id="85824-124">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="85824-125">Vælg **Installer et nyt tilføjelsesprogram**.</span><span class="sxs-lookup"><span data-stu-id="85824-125">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="85824-126">Vælg **Planlægningsoptimering**.</span><span class="sxs-lookup"><span data-stu-id="85824-126">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="85824-127">Følg installationsvejledningen, og accepter vilkårene og betingelserne.</span><span class="sxs-lookup"><span data-stu-id="85824-127">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="85824-128">Vælg **Installer**.</span><span class="sxs-lookup"><span data-stu-id="85824-128">Select **Install**.</span></span>
1. <span data-ttu-id="85824-129">I oversigtspanelet **Tilføjelsesprogrammer for miljø** kan du se, at Planlægningsoptimering er ved at blive installeret.</span><span class="sxs-lookup"><span data-stu-id="85824-129">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="85824-130">Efter nogle minutter bør **Installerer** blive ændret til **Installeret** (du skal muligvis opdatere siden).</span><span class="sxs-lookup"><span data-stu-id="85824-130">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="85824-131">Når den er installeret, er du klar til at aktivere Planlægningsoptimering i Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="85824-131">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="85824-132">Integration af Planlægningsoptimering</span><span class="sxs-lookup"><span data-stu-id="85824-132">Planning Optimization integration</span></span>

<span data-ttu-id="85824-133">Hvis du vil konfigurere, om tilføjelsesprogrammet til Planlægningsoptimering skal bruges til varedisponering, skal du gå til **Varedisponering** \> **Opsætning** \> **Parametre for Planlægningsoptimering**.</span><span class="sxs-lookup"><span data-stu-id="85824-133">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="85824-134">Forbindelsesstatus</span><span class="sxs-lookup"><span data-stu-id="85824-134">Connection status</span></span>

<span data-ttu-id="85824-135">Forbindelsesstatussen angiver den aktuelle status for forbindelsen mellem Supply Chain Management og tjenesten Planlægningsoptimering.</span><span class="sxs-lookup"><span data-stu-id="85824-135">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="85824-136">I følgende tabel vises de mulige værdier.</span><span class="sxs-lookup"><span data-stu-id="85824-136">The following table shows the possible values.</span></span>

| <span data-ttu-id="85824-137">Forbindelsesstatus</span><span class="sxs-lookup"><span data-stu-id="85824-137">Connection status</span></span> | <span data-ttu-id="85824-138">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="85824-138">Description</span></span> | <span data-ttu-id="85824-139">Kan Planlægningsoptimering anvendes?</span><span class="sxs-lookup"><span data-stu-id="85824-139">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="85824-140">Tilsluttet</span><span class="sxs-lookup"><span data-stu-id="85824-140">Connected</span></span> | <span data-ttu-id="85824-141">Der er oprettet en forbindelse mellem Planlægningsoptimeringstjenesten og Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="85824-141">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="85824-142">Ja</span><span class="sxs-lookup"><span data-stu-id="85824-142">Yes</span></span> |
| <span data-ttu-id="85824-143">Forbindelse aktiveres</span><span class="sxs-lookup"><span data-stu-id="85824-143">Enabling connection</span></span> | <span data-ttu-id="85824-144">En anmodning om at aktivere forbindelsen til Planlægningsoptimeringstjenesten er i øjeblikket i gang.</span><span class="sxs-lookup"><span data-stu-id="85824-144">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="85824-145">Nr.</span><span class="sxs-lookup"><span data-stu-id="85824-145">No</span></span> |
| <span data-ttu-id="85824-146">Forbindelse afbrudt</span><span class="sxs-lookup"><span data-stu-id="85824-146">Disconnected</span></span> | <span data-ttu-id="85824-147">Der er ingen forbindelse til Planlægningsoptimeringstjenesten.</span><span class="sxs-lookup"><span data-stu-id="85824-147">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="85824-148">Forbindelsen kan slås til fra LCS, som beskrevet tidligere i dette emne.</span><span class="sxs-lookup"><span data-stu-id="85824-148">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="85824-149">Nr.</span><span class="sxs-lookup"><span data-stu-id="85824-149">No</span></span> |
| <span data-ttu-id="85824-150">Forbindelse deaktiveres</span><span class="sxs-lookup"><span data-stu-id="85824-150">Disabling connection</span></span> | <span data-ttu-id="85824-151">En anmodning om at deaktivere forbindelsen til Planlægningsoptimeringstjenesten er i øjeblikket i gang.</span><span class="sxs-lookup"><span data-stu-id="85824-151">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="85824-152">Nr.</span><span class="sxs-lookup"><span data-stu-id="85824-152">No</span></span> |
| <span data-ttu-id="85824-153">Henter status</span><span class="sxs-lookup"><span data-stu-id="85824-153">Getting status</span></span> | <span data-ttu-id="85824-154">Systemet venter på statusoplysninger fra Planlægningsoptimeringstjenesten.</span><span class="sxs-lookup"><span data-stu-id="85824-154">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="85824-155">Nr.</span><span class="sxs-lookup"><span data-stu-id="85824-155">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="85824-156">Indstillingen Brug Planlægningsoptimering</span><span class="sxs-lookup"><span data-stu-id="85824-156">The Use Planning Optimization option</span></span>

<span data-ttu-id="85824-157">Indstillingen af indstillingen **Brug Planlægningsoptimering** bestemmer, hvilket planlægningsprogram der bruges til varedisponering:</span><span class="sxs-lookup"><span data-stu-id="85824-157">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="85824-158">**Ja** – Planlægningsoptimering bruges til varedisponering.</span><span class="sxs-lookup"><span data-stu-id="85824-158">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="85824-159">**Nej** – Det indbyggede planlægningsprogram for Supply Chain Management bruges til varedisponering.</span><span class="sxs-lookup"><span data-stu-id="85824-159">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="85824-160">Hvis de eksisterende planlægningsbatchjob, der blev oprettet til det indbyggede planlægningsprogram for Supply Chain Management, udløses mens indstillingen **Brug Planlægningsoptimering** er angivet til **Ja**, vil disse job ikke blive udført.</span><span class="sxs-lookup"><span data-stu-id="85824-160">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="85824-161">Integration med opsætningen</span><span class="sxs-lookup"><span data-stu-id="85824-161">Integration with the setup</span></span>

<span data-ttu-id="85824-162">Hvis forhåndsvisningen af Planlægningsoptimering er aktiveret, foretages varedisponering ved hjælp af tilføjelsesprogrammet for Planlægningsoptimering.</span><span class="sxs-lookup"><span data-stu-id="85824-162">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="85824-163">I dette tilfælde påvirkes resultaterne af og funktionerne for varedisponering.</span><span class="sxs-lookup"><span data-stu-id="85824-163">In this case, master planning results and features are affected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="85824-164">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="85824-164">Additional resources</span></span>

[<span data-ttu-id="85824-165">Vilkår og betingelser for forhåndsvisning</span><span class="sxs-lookup"><span data-stu-id="85824-165">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="85824-166">Oversigt over planlægningsoptimering</span><span class="sxs-lookup"><span data-stu-id="85824-166">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="85824-167">Analyse af om Planlægningsoptimering passer til</span><span class="sxs-lookup"><span data-stu-id="85824-167">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="85824-168">Få vist planhistorik og planlægningslogs</span><span class="sxs-lookup"><span data-stu-id="85824-168">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="85824-169">Anvend filtre på en plan</span><span class="sxs-lookup"><span data-stu-id="85824-169">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="85824-170">Annullere et planlægningsjob</span><span class="sxs-lookup"><span data-stu-id="85824-170">Cancel a planning job</span></span>](cancel-planning-job.md)
