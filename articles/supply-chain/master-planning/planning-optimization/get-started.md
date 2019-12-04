---
title: Introduktion til Planlægningsoptimering
description: I dette emne beskrives, hvordan du kommer i gang med at bruge funktionen Planlægningsoptimering.
author: ChristianRytt
manager: AnnBe
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 37c2acb2397b2a0ad69272c0645bd200a8d7910d
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773923"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="cf50c-103">Introduktion til Planlægningsoptimering</span><span class="sxs-lookup"><span data-stu-id="cf50c-103">Get started with Planning Optimization</span></span>

<span data-ttu-id="cf50c-104">Funktionen Planlægningsoptimering understøtter i øjeblikket ikke alle de funktioner, der er tilgængelige i det planlægningsprogram, der er indbygget i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="cf50c-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="cf50c-105">Det er derfor vigtigt, at du evaluerer, om det funktionssæt, der aktuelt er tilgængeligt i Planlægningsoptimering, opfylder dine behov.</span><span class="sxs-lookup"><span data-stu-id="cf50c-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="cf50c-106">Funktionen Planlægningsoptimering er som standard ikke slået til i Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="cf50c-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="cf50c-107">Derfor har du mulighed for at foretage evalueringen, før den aktiveres.</span><span class="sxs-lookup"><span data-stu-id="cf50c-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="cf50c-108">Til sidst erstatter Planlægningsoptimering det eksisterende indbyggede planlægningsprogram Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="cf50c-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="cf50c-109">Før du slår Planlægningsoptimering til, anbefales det på det kraftigste, at du evaluerer resultaterne af analysen af om Planlægningsoptimering passer.</span><span class="sxs-lookup"><span data-stu-id="cf50c-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="cf50c-110">Du kan finde flere oplysninger under [Analyse af om Planlægningsoptimering passer](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="cf50c-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="licensing"></a><span data-ttu-id="cf50c-111">Licenser</span><span class="sxs-lookup"><span data-stu-id="cf50c-111">Licensing</span></span>

<span data-ttu-id="cf50c-112">Hvis du kan køre varedisponering ved hjælp af din aktuelle licens, behøver du ikke købe en ekstra licens for at begynde at bruge Planlægningsoptimering.</span><span class="sxs-lookup"><span data-stu-id="cf50c-112">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="cf50c-113">Installer tilføjelsesprogrammet</span><span class="sxs-lookup"><span data-stu-id="cf50c-113">Install the add-in</span></span>

<span data-ttu-id="cf50c-114">Hvis du vil bruge Planlægningsoptimering, skal du installere tilføjelsesprogrammet Planlægningsoptimering til Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="cf50c-114">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="cf50c-115">Du kan få adgang til tilføjelsesprogrammet fra dit LCS projekt og slå Planlægningsoptimeringsfunktionen til fra brugergrænsefladen til Supply Chain Management (UI).</span><span class="sxs-lookup"><span data-stu-id="cf50c-115">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

1. <span data-ttu-id="cf50c-116">Log på LCS, og åbn det ønskede miljø.</span><span class="sxs-lookup"><span data-stu-id="cf50c-116">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="cf50c-117">Gå til **Alle detaljer**.</span><span class="sxs-lookup"><span data-stu-id="cf50c-117">Go to **Full details**.</span></span>
1. <span data-ttu-id="cf50c-118">Vælg **Vedligehold**, eller rul ned til oversigtspanelet **Tilføjelsesprogrammer for miljø**.</span><span class="sxs-lookup"><span data-stu-id="cf50c-118">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="cf50c-119">Vælg **Installer et nyt tilføjelsesprogram**.</span><span class="sxs-lookup"><span data-stu-id="cf50c-119">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="cf50c-120">Vælg **Planlægningsoptimering**.</span><span class="sxs-lookup"><span data-stu-id="cf50c-120">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="cf50c-121">Følg installationsvejledningen, og accepter vilkårene og betingelserne.</span><span class="sxs-lookup"><span data-stu-id="cf50c-121">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="cf50c-122">Vælg **Installer**.</span><span class="sxs-lookup"><span data-stu-id="cf50c-122">Select **Install**.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="cf50c-123">Integration af Planlægningsoptimering</span><span class="sxs-lookup"><span data-stu-id="cf50c-123">Planning Optimization integration</span></span>

<span data-ttu-id="cf50c-124">Hvis du vil konfigurere, om tilføjelsesprogrammet til Planlægningsoptimering skal bruges til varedisponering, skal du gå til **Varedisponering** \> **Opsætning** \> **Integration af Planlægningsoptimering** \> **Integrationsparametre**.</span><span class="sxs-lookup"><span data-stu-id="cf50c-124">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization integration** \> **Integration parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="cf50c-125">Forbindelsesstatus</span><span class="sxs-lookup"><span data-stu-id="cf50c-125">Connection status</span></span>

<span data-ttu-id="cf50c-126">Forbindelsesstatussen angiver den aktuelle status for forbindelsen mellem Supply Chain Management og tjenesten Planlægningsoptimering.</span><span class="sxs-lookup"><span data-stu-id="cf50c-126">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="cf50c-127">I følgende tabel vises de mulige værdier.</span><span class="sxs-lookup"><span data-stu-id="cf50c-127">The following table shows the possible values.</span></span>

| <span data-ttu-id="cf50c-128">Forbindelsesstatus</span><span class="sxs-lookup"><span data-stu-id="cf50c-128">Connection status</span></span> | <span data-ttu-id="cf50c-129">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="cf50c-129">Description</span></span> | <span data-ttu-id="cf50c-130">Kan Planlægningsoptimering anvendes?</span><span class="sxs-lookup"><span data-stu-id="cf50c-130">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="cf50c-131">Tilsluttet</span><span class="sxs-lookup"><span data-stu-id="cf50c-131">Connected</span></span> | <span data-ttu-id="cf50c-132">Der er oprettet en forbindelse mellem Planlægningsoptimeringstjenesten og Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="cf50c-132">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="cf50c-133">Ja</span><span class="sxs-lookup"><span data-stu-id="cf50c-133">Yes</span></span> |
| <span data-ttu-id="cf50c-134">Forbindelse aktiveres</span><span class="sxs-lookup"><span data-stu-id="cf50c-134">Enabling connection</span></span> | <span data-ttu-id="cf50c-135">En anmodning om at aktivere forbindelsen til Planlægningsoptimeringstjenesten er i øjeblikket i gang.</span><span class="sxs-lookup"><span data-stu-id="cf50c-135">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="cf50c-136">Nr.</span><span class="sxs-lookup"><span data-stu-id="cf50c-136">No</span></span> |
| <span data-ttu-id="cf50c-137">Forbindelse afbrudt</span><span class="sxs-lookup"><span data-stu-id="cf50c-137">Disconnected</span></span> | <span data-ttu-id="cf50c-138">Der er ingen forbindelse til Planlægningsoptimeringstjenesten.</span><span class="sxs-lookup"><span data-stu-id="cf50c-138">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="cf50c-139">Forbindelsen kan slås til fra LCS, som beskrevet tidligere i dette emne.</span><span class="sxs-lookup"><span data-stu-id="cf50c-139">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="cf50c-140">Nr.</span><span class="sxs-lookup"><span data-stu-id="cf50c-140">No</span></span> |
| <span data-ttu-id="cf50c-141">Forbindelse deaktiveres</span><span class="sxs-lookup"><span data-stu-id="cf50c-141">Disabling connection</span></span> | <span data-ttu-id="cf50c-142">En anmodning om at deaktivere forbindelsen til Planlægningsoptimeringstjenesten er i øjeblikket i gang.</span><span class="sxs-lookup"><span data-stu-id="cf50c-142">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="cf50c-143">Nr.</span><span class="sxs-lookup"><span data-stu-id="cf50c-143">No</span></span> |
| <span data-ttu-id="cf50c-144">Henter status</span><span class="sxs-lookup"><span data-stu-id="cf50c-144">Getting status</span></span> | <span data-ttu-id="cf50c-145">Systemet venter på statusoplysninger fra Planlægningsoptimeringstjenesten.</span><span class="sxs-lookup"><span data-stu-id="cf50c-145">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="cf50c-146">Nr.</span><span class="sxs-lookup"><span data-stu-id="cf50c-146">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="cf50c-147">Indstillingen Brug Planlægningsoptimering</span><span class="sxs-lookup"><span data-stu-id="cf50c-147">The Use Planning Optimization option</span></span>

<span data-ttu-id="cf50c-148">Indstillingen af indstillingen **Brug Planlægningsoptimering** bestemmer, hvilket planlægningsprogram der bruges til varedisponering:</span><span class="sxs-lookup"><span data-stu-id="cf50c-148">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="cf50c-149">**Ja** – Planlægningsoptimering bruges til varedisponering.</span><span class="sxs-lookup"><span data-stu-id="cf50c-149">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="cf50c-150">**Nej** – Det indbyggede planlægningsprogram for Supply Chain Management bruges til varedisponering.</span><span class="sxs-lookup"><span data-stu-id="cf50c-150">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="cf50c-151">Hvis de eksisterende planlægningsbatchjob, der blev oprettet til det indbyggede planlægningsprogram for Supply Chain Management, udløses mens indstillingen **Brug Planlægningsoptimering** er angivet til **Ja**, vil disse job ikke blive udført.</span><span class="sxs-lookup"><span data-stu-id="cf50c-151">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="cf50c-152">Integration med opsætningen</span><span class="sxs-lookup"><span data-stu-id="cf50c-152">Integration with the setup</span></span>

<span data-ttu-id="cf50c-153">Hvis forhåndsvisningen af Planlægningsoptimering er aktiveret, foretages varedisponering ved hjælp af tilføjelsesprogrammet for Planlægningsoptimering.</span><span class="sxs-lookup"><span data-stu-id="cf50c-153">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="cf50c-154">I dette tilfælde påvirkes resultaterne af og funktionerne for varedisponering.</span><span class="sxs-lookup"><span data-stu-id="cf50c-154">In this case, master planning results and features are affected.</span></span>

## <a name="related-resources"></a><span data-ttu-id="cf50c-155">Tilknyttede ressourcer</span><span class="sxs-lookup"><span data-stu-id="cf50c-155">Related resources</span></span>

[<span data-ttu-id="cf50c-156">Vilkår og betingelser for forhåndsvisning</span><span class="sxs-lookup"><span data-stu-id="cf50c-156">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="cf50c-157">Oversigt over Planlægningsoptimering</span><span class="sxs-lookup"><span data-stu-id="cf50c-157">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="cf50c-158">Analyse af om Planlægningsoptimering passer til</span><span class="sxs-lookup"><span data-stu-id="cf50c-158">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="cf50c-159">Få vist planhistorik og planlægningslogs</span><span class="sxs-lookup"><span data-stu-id="cf50c-159">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="cf50c-160">Anvend filtre på en plan</span><span class="sxs-lookup"><span data-stu-id="cf50c-160">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="cf50c-161">Annullere et planlægningsjob</span><span class="sxs-lookup"><span data-stu-id="cf50c-161">Cancel a planning job</span></span>](cancel-planning-job.md)
