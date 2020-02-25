---
title: Introduktion til Planlægningsoptimering
description: I dette emne beskrives, hvordan du kommer i gang med at bruge funktionen Planlægningsoptimering.
author: ChristianRytt
manager: AnnBe
ms.date: 01/17/2020
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
ms.openlocfilehash: 3e0371c6addc0412dc2fc105891b012941e92a06
ms.sourcegitcommit: e5a3c85a322a9216b8f176536d664fef40ae0bec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/17/2020
ms.locfileid: "2971458"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="721f2-103">Introduktion til Planlægningsoptimering</span><span class="sxs-lookup"><span data-stu-id="721f2-103">Get started with Planning Optimization</span></span>

<span data-ttu-id="721f2-104">Funktionen Planlægningsoptimering understøtter i øjeblikket ikke alle de funktioner, der er tilgængelige i det planlægningsprogram, der er indbygget i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="721f2-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="721f2-105">Det er derfor vigtigt, at du evaluerer, om det funktionssæt, der aktuelt er tilgængeligt i Planlægningsoptimering, opfylder dine behov.</span><span class="sxs-lookup"><span data-stu-id="721f2-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="721f2-106">Funktionen Planlægningsoptimering er som standard ikke slået til i Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="721f2-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="721f2-107">Derfor har du mulighed for at foretage evalueringen, før den aktiveres.</span><span class="sxs-lookup"><span data-stu-id="721f2-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="721f2-108">Til sidst erstatter Planlægningsoptimering det eksisterende indbyggede planlægningsprogram Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="721f2-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="721f2-109">Før du slår Planlægningsoptimering til, anbefales det på det kraftigste, at du evaluerer resultaterne af analysen af om Planlægningsoptimering passer.</span><span class="sxs-lookup"><span data-stu-id="721f2-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="721f2-110">Du kan finde flere oplysninger under [Analyse af om Planlægningsoptimering passer](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="721f2-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="licensing"></a><span data-ttu-id="721f2-111">Licenser</span><span class="sxs-lookup"><span data-stu-id="721f2-111">Licensing</span></span>

<span data-ttu-id="721f2-112">Hvis du kan køre varedisponering ved hjælp af din aktuelle licens, behøver du ikke købe en ekstra licens for at begynde at bruge Planlægningsoptimering.</span><span class="sxs-lookup"><span data-stu-id="721f2-112">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="721f2-113">Installer tilføjelsesprogrammet</span><span class="sxs-lookup"><span data-stu-id="721f2-113">Install the add-in</span></span>

<span data-ttu-id="721f2-114">Hvis du vil bruge Planlægningsoptimering, skal du installere tilføjelsesprogrammet Planlægningsoptimering til Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="721f2-114">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="721f2-115">Du kan få adgang til tilføjelsesprogrammet fra dit LCS projekt og slå Planlægningsoptimeringsfunktionen til fra brugergrænsefladen til Supply Chain Management (UI).</span><span class="sxs-lookup"><span data-stu-id="721f2-115">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

1. <span data-ttu-id="721f2-116">Log på LCS, og åbn det ønskede miljø.</span><span class="sxs-lookup"><span data-stu-id="721f2-116">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="721f2-117">Gå til **Alle detaljer**.</span><span class="sxs-lookup"><span data-stu-id="721f2-117">Go to **Full details**.</span></span>
1. <span data-ttu-id="721f2-118">Rul ned til oversigtspanelet **Tilføjelsesprogrammer for miljø**.</span><span class="sxs-lookup"><span data-stu-id="721f2-118">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="721f2-119">Vælg **Installer et nyt tilføjelsesprogram**.</span><span class="sxs-lookup"><span data-stu-id="721f2-119">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="721f2-120">Vælg **Planlægningsoptimering**.</span><span class="sxs-lookup"><span data-stu-id="721f2-120">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="721f2-121">Følg installationsvejledningen, og accepter vilkårene og betingelserne.</span><span class="sxs-lookup"><span data-stu-id="721f2-121">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="721f2-122">Vælg **Installer**.</span><span class="sxs-lookup"><span data-stu-id="721f2-122">Select **Install**.</span></span>
1. <span data-ttu-id="721f2-123">I oversigtspanelet **Tilføjelsesprogrammer for miljø** kan du se, at Planlægningsoptimering er ved at blive installeret.</span><span class="sxs-lookup"><span data-stu-id="721f2-123">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="721f2-124">Efter nogle minutter bør **Installerer** blive ændret til **Installeret** (du skal muligvis opdatere siden).</span><span class="sxs-lookup"><span data-stu-id="721f2-124">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="721f2-125">Når den er installeret, er du klar til at aktivere Planlægningsoptimering i Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="721f2-125">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="721f2-126">Integration af Planlægningsoptimering</span><span class="sxs-lookup"><span data-stu-id="721f2-126">Planning Optimization integration</span></span>

<span data-ttu-id="721f2-127">Hvis du vil konfigurere, om tilføjelsesprogrammet til Planlægningsoptimering skal bruges til varedisponering, skal du gå til **Varedisponering** \> **Opsætning** \> **Parametre for Planlægningsoptimering**.</span><span class="sxs-lookup"><span data-stu-id="721f2-127">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="721f2-128">Forbindelsesstatus</span><span class="sxs-lookup"><span data-stu-id="721f2-128">Connection status</span></span>

<span data-ttu-id="721f2-129">Forbindelsesstatussen angiver den aktuelle status for forbindelsen mellem Supply Chain Management og tjenesten Planlægningsoptimering.</span><span class="sxs-lookup"><span data-stu-id="721f2-129">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="721f2-130">I følgende tabel vises de mulige værdier.</span><span class="sxs-lookup"><span data-stu-id="721f2-130">The following table shows the possible values.</span></span>

| <span data-ttu-id="721f2-131">Forbindelsesstatus</span><span class="sxs-lookup"><span data-stu-id="721f2-131">Connection status</span></span> | <span data-ttu-id="721f2-132">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="721f2-132">Description</span></span> | <span data-ttu-id="721f2-133">Kan Planlægningsoptimering anvendes?</span><span class="sxs-lookup"><span data-stu-id="721f2-133">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="721f2-134">Tilsluttet</span><span class="sxs-lookup"><span data-stu-id="721f2-134">Connected</span></span> | <span data-ttu-id="721f2-135">Der er oprettet en forbindelse mellem Planlægningsoptimeringstjenesten og Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="721f2-135">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="721f2-136">Ja</span><span class="sxs-lookup"><span data-stu-id="721f2-136">Yes</span></span> |
| <span data-ttu-id="721f2-137">Forbindelse aktiveres</span><span class="sxs-lookup"><span data-stu-id="721f2-137">Enabling connection</span></span> | <span data-ttu-id="721f2-138">En anmodning om at aktivere forbindelsen til Planlægningsoptimeringstjenesten er i øjeblikket i gang.</span><span class="sxs-lookup"><span data-stu-id="721f2-138">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="721f2-139">Nr.</span><span class="sxs-lookup"><span data-stu-id="721f2-139">No</span></span> |
| <span data-ttu-id="721f2-140">Forbindelse afbrudt</span><span class="sxs-lookup"><span data-stu-id="721f2-140">Disconnected</span></span> | <span data-ttu-id="721f2-141">Der er ingen forbindelse til Planlægningsoptimeringstjenesten.</span><span class="sxs-lookup"><span data-stu-id="721f2-141">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="721f2-142">Forbindelsen kan slås til fra LCS, som beskrevet tidligere i dette emne.</span><span class="sxs-lookup"><span data-stu-id="721f2-142">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="721f2-143">Nr.</span><span class="sxs-lookup"><span data-stu-id="721f2-143">No</span></span> |
| <span data-ttu-id="721f2-144">Forbindelse deaktiveres</span><span class="sxs-lookup"><span data-stu-id="721f2-144">Disabling connection</span></span> | <span data-ttu-id="721f2-145">En anmodning om at deaktivere forbindelsen til Planlægningsoptimeringstjenesten er i øjeblikket i gang.</span><span class="sxs-lookup"><span data-stu-id="721f2-145">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="721f2-146">Nr.</span><span class="sxs-lookup"><span data-stu-id="721f2-146">No</span></span> |
| <span data-ttu-id="721f2-147">Henter status</span><span class="sxs-lookup"><span data-stu-id="721f2-147">Getting status</span></span> | <span data-ttu-id="721f2-148">Systemet venter på statusoplysninger fra Planlægningsoptimeringstjenesten.</span><span class="sxs-lookup"><span data-stu-id="721f2-148">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="721f2-149">Nr.</span><span class="sxs-lookup"><span data-stu-id="721f2-149">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="721f2-150">Indstillingen Brug Planlægningsoptimering</span><span class="sxs-lookup"><span data-stu-id="721f2-150">The Use Planning Optimization option</span></span>

<span data-ttu-id="721f2-151">Indstillingen af indstillingen **Brug Planlægningsoptimering** bestemmer, hvilket planlægningsprogram der bruges til varedisponering:</span><span class="sxs-lookup"><span data-stu-id="721f2-151">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="721f2-152">**Ja** – Planlægningsoptimering bruges til varedisponering.</span><span class="sxs-lookup"><span data-stu-id="721f2-152">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="721f2-153">**Nej** – Det indbyggede planlægningsprogram for Supply Chain Management bruges til varedisponering.</span><span class="sxs-lookup"><span data-stu-id="721f2-153">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="721f2-154">Hvis de eksisterende planlægningsbatchjob, der blev oprettet til det indbyggede planlægningsprogram for Supply Chain Management, udløses mens indstillingen **Brug Planlægningsoptimering** er angivet til **Ja**, vil disse job ikke blive udført.</span><span class="sxs-lookup"><span data-stu-id="721f2-154">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="721f2-155">Integration med opsætningen</span><span class="sxs-lookup"><span data-stu-id="721f2-155">Integration with the setup</span></span>

<span data-ttu-id="721f2-156">Hvis forhåndsvisningen af Planlægningsoptimering er aktiveret, foretages varedisponering ved hjælp af tilføjelsesprogrammet for Planlægningsoptimering.</span><span class="sxs-lookup"><span data-stu-id="721f2-156">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="721f2-157">I dette tilfælde påvirkes resultaterne af og funktionerne for varedisponering.</span><span class="sxs-lookup"><span data-stu-id="721f2-157">In this case, master planning results and features are affected.</span></span>

## <a name="related-resources"></a><span data-ttu-id="721f2-158">Tilknyttede ressourcer</span><span class="sxs-lookup"><span data-stu-id="721f2-158">Related resources</span></span>

[<span data-ttu-id="721f2-159">Vilkår og betingelser for forhåndsvisning</span><span class="sxs-lookup"><span data-stu-id="721f2-159">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="721f2-160">Oversigt over Planlægningsoptimering</span><span class="sxs-lookup"><span data-stu-id="721f2-160">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="721f2-161">Analyse af om Planlægningsoptimering passer til</span><span class="sxs-lookup"><span data-stu-id="721f2-161">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="721f2-162">Få vist planhistorik og planlægningslogs</span><span class="sxs-lookup"><span data-stu-id="721f2-162">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="721f2-163">Anvend filtre på en plan</span><span class="sxs-lookup"><span data-stu-id="721f2-163">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="721f2-164">Annullere et planlægningsjob</span><span class="sxs-lookup"><span data-stu-id="721f2-164">Cancel a planning job</span></span>](cancel-planning-job.md)
