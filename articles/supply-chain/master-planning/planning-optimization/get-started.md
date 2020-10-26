---
title: Introduktion til Planlægningsoptimering
description: I dette emne beskrives, hvordan du kommer i gang med at bruge funktionen Planlægningsoptimering.
author: ChristianRytt
manager: tfehr
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
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
ms.openlocfilehash: 49025d0aa0f6a627b816a43dd4260449942b400c
ms.sourcegitcommit: ae04c7cb48f7ecafe71bbe77a0f97715e6290991
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/09/2020
ms.locfileid: "3973470"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="72d66-103">Kom i gang med planlægningsoptimering</span><span class="sxs-lookup"><span data-stu-id="72d66-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="72d66-104">Som [tidligere annonceret](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios) er planlægningsoptimering planlagt til at erstatte det eksisterende indbyggede varedisponeringsprogram.</span><span class="sxs-lookup"><span data-stu-id="72d66-104">As [previously announced](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios), Planning Optimization is scheduled to replace the existing built-in master planning engine.</span></span>

<span data-ttu-id="72d66-105">Hvis du i øjeblikket bruger det indbyggede varedisponeringsprogram, skal du starte med at planlægge din migrering til planlægningsoptimering nu.</span><span class="sxs-lookup"><span data-stu-id="72d66-105">If you currently use the built-in master planning engine, you should start planning your migration to Planning Optimization now.</span></span> <span data-ttu-id="72d66-106">Det er vigtigt at starte migreringsprocessen med det samme, fordi dine handlinger kan blive påvirket, når udfasning gennemtvinges.</span><span class="sxs-lookup"><span data-stu-id="72d66-106">It is important to start the migration process right away because your operations may be impacted when deprecation is enforced.</span></span> <span data-ttu-id="72d66-107">For at undgå problemer i sidste øjeblik, når udfasning gennemtvinges, anbefaler vi kraftigt, at du fuldfører migreringen før 1. december 2020.</span><span class="sxs-lookup"><span data-stu-id="72d66-107">To avoid last-minutes issues when deprecation is enforced, we strongly encourage you to complete the migration before December 1, 2020.</span></span> 

<span data-ttu-id="72d66-108">Funktionen Planlægningsoptimering understøtter i øjeblikket ikke alle de funktioner, der er tilgængelige i det planlægningsprogram, der er indbygget i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="72d66-108">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Supply Chain Management.</span></span> <span data-ttu-id="72d66-109">Det er derfor vigtigt, at du evaluerer, om det funktionssæt, der aktuelt er tilgængeligt i Planlægningsoptimering, opfylder dine behov.</span><span class="sxs-lookup"><span data-stu-id="72d66-109">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="72d66-110">Planlægningsoptimeringsfunktionen er i øjeblikket ikke aktiveret som standard i Dynamics Lifecycle Services (LCS), så du har mulighed for at foretage din evaluering, før funktionen er slået til.</span><span class="sxs-lookup"><span data-stu-id="72d66-110">The Planning Optimization functionality isn't currently turned on by default in Dynamics Lifecycle Services (LCS), so you have the opportunity to do your evaluation before the feature is turned on.</span></span>

> [!NOTE]
> <span data-ttu-id="72d66-111">Du skal anmode om en undtagelse fra migrering til planlægningsoptimering, hvis din varedisponeringsproces ikke omfatter produktion (varedisponeringsgenererede produktionsordreforslag), og du har brug for det indbyggede varedisponeringsprogram ud over version 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="72d66-111">You need to request an exception from migration to Planning Optimization if your master planning process does not include production (master planning generated planned production orders) and you require the built-in master planning engine beyond version 10.0.15.</span></span> <span data-ttu-id="72d66-112">Startende med version 10.0.16 vises der en fejl i miljøer, når der køres indbygget varedisponering uden generering af produktionsordreforslag.</span><span class="sxs-lookup"><span data-stu-id="72d66-112">Starting in version 10.0.16, an error will be shown in environments when running built-in master planning without generation of planned production orders.</span></span> <span data-ttu-id="72d66-113">Planlægningsoptimering skal bruges til alle nye installationer, der ikke genererer produktionsordreforslag under varedisponering.</span><span class="sxs-lookup"><span data-stu-id="72d66-113">Planning Optimization should be used for all new deployments that do not generate planned production orders during master planning.</span></span> <span data-ttu-id="72d66-114">Ejere af eksisterende miljøer, der kører det indbyggede varedisponeringsprogram uden generering af produktionsordreforslag, modtager en mail med detaljer om undtagelsesprocessen.</span><span class="sxs-lookup"><span data-stu-id="72d66-114">Owners of existing environments running the built-in master planning engine without generation of Planned production orders, will receive a mail with details about the exception process.</span></span> <span data-ttu-id="72d66-115">Det anbefales, at du arbejder med en partner for at evaluere og planlægge migreringen til planlægningsoptimering.</span><span class="sxs-lookup"><span data-stu-id="72d66-115">We recommend that you work with a partner to evaluate and plan the migration to Planning Optimization.</span></span>

<span data-ttu-id="72d66-116">Før du slår Planlægningsoptimering til, anbefales det på det kraftigste, at du evaluerer resultaterne af analysen af om Planlægningsoptimering passer.</span><span class="sxs-lookup"><span data-stu-id="72d66-116">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="72d66-117">Du kan finde flere oplysninger under [Analyse af om Planlægningsoptimering passer](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="72d66-117">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="availability"></a><span data-ttu-id="72d66-118">Tilgængelighed</span><span class="sxs-lookup"><span data-stu-id="72d66-118">Availability</span></span>
<span data-ttu-id="72d66-119">Planlægningsoptimering er i øjeblikket tilgængelig i følgende Azure-områder: USA, Canada, Europa, Storbritannien og Australien.</span><span class="sxs-lookup"><span data-stu-id="72d66-119">Planning Optimization is currently available in the following Azure geographies: United States, Canada, Europe, United Kingdom, and Australia.</span></span> <span data-ttu-id="72d66-120">Hvis du forsøger at installere tilføjelsesprogrammet fra et andet geografisk område, vil LCS vise en meddelelse om, at dette geografiske område ikke understøttes.</span><span class="sxs-lookup"><span data-stu-id="72d66-120">If you try to install the add-in from another geographic region, then LCS will show a message that this geographic is not supported.</span></span>

<span data-ttu-id="72d66-121">Bemærk, at planlægningsoptimering ikke understøtter lokale installationer af Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="72d66-121">Note that Planning Optimization does not support on-premises deployments of Dynamics 365 Supply Chain Management.</span></span>

### <a name="licensing"></a><span data-ttu-id="72d66-122">Licensering</span><span class="sxs-lookup"><span data-stu-id="72d66-122">Licensing</span></span>

<span data-ttu-id="72d66-123">Hvis du kan køre varedisponering ved hjælp af din aktuelle licens, behøver du ikke købe en ekstra licens for at begynde at bruge Planlægningsoptimering.</span><span class="sxs-lookup"><span data-stu-id="72d66-123">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="72d66-124">Installer tilføjelsesprogrammet</span><span class="sxs-lookup"><span data-stu-id="72d66-124">Install the add-in</span></span>

<span data-ttu-id="72d66-125">Hvis du vil bruge Planlægningsoptimering, skal du installere tilføjelsesprogrammet Planlægningsoptimering til Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="72d66-125">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="72d66-126">Du kan få adgang til tilføjelsesprogrammet fra dit LCS projekt og slå Planlægningsoptimeringsfunktionen til fra brugergrænsefladen til Supply Chain Management (UI).</span><span class="sxs-lookup"><span data-stu-id="72d66-126">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

> [!NOTE]
> <span data-ttu-id="72d66-127">Behovet for planlægningsoptimering er et LCS-aktiveret miljø med høj tilgængelighed på niveau 2 eller højere (ikke et Onebox-miljø) i Dynamics 365 Supply Chain Management, version 10.0.7 eller nyere.</span><span class="sxs-lookup"><span data-stu-id="72d66-127">The requirement for Planning Optimization is an LCS enabled high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="72d66-128">Hvis du forsøger at installere tilføjelsesprogrammet i et OneBox-miljø, fuldføres installationen ikke, og du skal annullere installationen.</span><span class="sxs-lookup"><span data-stu-id="72d66-128">If you try to install the add-in on a OneBox environment, the installation will not complete and you will need to cancel the installation.</span></span>

1. <span data-ttu-id="72d66-129">Log på LCS, og åbn det ønskede miljø.</span><span class="sxs-lookup"><span data-stu-id="72d66-129">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="72d66-130">Gå til **Alle detaljer**.</span><span class="sxs-lookup"><span data-stu-id="72d66-130">Go to **Full details**.</span></span>
1. <span data-ttu-id="72d66-131">Rul ned til oversigtspanelet **Tilføjelsesprogrammer for miljø**.</span><span class="sxs-lookup"><span data-stu-id="72d66-131">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="72d66-132">Vælg **Installer et nyt tilføjelsesprogram**.</span><span class="sxs-lookup"><span data-stu-id="72d66-132">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="72d66-133">Vælg **Planlægningsoptimering**.</span><span class="sxs-lookup"><span data-stu-id="72d66-133">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="72d66-134">Følg installationsvejledningen, og accepter vilkårene og betingelserne.</span><span class="sxs-lookup"><span data-stu-id="72d66-134">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="72d66-135">Vælg **Installer**.</span><span class="sxs-lookup"><span data-stu-id="72d66-135">Select **Install**.</span></span>
1. <span data-ttu-id="72d66-136">I oversigtspanelet **Tilføjelsesprogrammer for miljø** kan du se, at Planlægningsoptimering er ved at blive installeret.</span><span class="sxs-lookup"><span data-stu-id="72d66-136">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="72d66-137">Efter nogle minutter bør **Installerer** blive ændret til **Installeret** (du skal muligvis opdatere siden).</span><span class="sxs-lookup"><span data-stu-id="72d66-137">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="72d66-138">Når den er installeret, er du klar til at aktivere Planlægningsoptimering i Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="72d66-138">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="72d66-139">Integration af Planlægningsoptimering</span><span class="sxs-lookup"><span data-stu-id="72d66-139">Planning Optimization integration</span></span>

<span data-ttu-id="72d66-140">Hvis du vil konfigurere, om tilføjelsesprogrammet til Planlægningsoptimering skal bruges til varedisponering, skal du gå til **Varedisponering** \> **Opsætning** \> **Parametre for Planlægningsoptimering**.</span><span class="sxs-lookup"><span data-stu-id="72d66-140">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="72d66-141">Forbindelsesstatus</span><span class="sxs-lookup"><span data-stu-id="72d66-141">Connection status</span></span>

<span data-ttu-id="72d66-142">Forbindelsesstatussen angiver den aktuelle status for forbindelsen mellem Supply Chain Management og tjenesten Planlægningsoptimering.</span><span class="sxs-lookup"><span data-stu-id="72d66-142">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="72d66-143">I følgende tabel vises de mulige værdier.</span><span class="sxs-lookup"><span data-stu-id="72d66-143">The following table shows the possible values.</span></span>

| <span data-ttu-id="72d66-144">Forbindelsesstatus</span><span class="sxs-lookup"><span data-stu-id="72d66-144">Connection status</span></span> | <span data-ttu-id="72d66-145">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="72d66-145">Description</span></span> | <span data-ttu-id="72d66-146">Kan Planlægningsoptimering anvendes?</span><span class="sxs-lookup"><span data-stu-id="72d66-146">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="72d66-147">Tilsluttet</span><span class="sxs-lookup"><span data-stu-id="72d66-147">Connected</span></span> | <span data-ttu-id="72d66-148">Der er oprettet en forbindelse mellem Planlægningsoptimeringstjenesten og Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="72d66-148">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="72d66-149">Ja</span><span class="sxs-lookup"><span data-stu-id="72d66-149">Yes</span></span> |
| <span data-ttu-id="72d66-150">Forbindelse aktiveres</span><span class="sxs-lookup"><span data-stu-id="72d66-150">Enabling connection</span></span> | <span data-ttu-id="72d66-151">En anmodning om at aktivere forbindelsen til Planlægningsoptimeringstjenesten er i øjeblikket i gang.</span><span class="sxs-lookup"><span data-stu-id="72d66-151">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="72d66-152">Nr.</span><span class="sxs-lookup"><span data-stu-id="72d66-152">No</span></span> |
| <span data-ttu-id="72d66-153">Forbindelse afbrudt</span><span class="sxs-lookup"><span data-stu-id="72d66-153">Disconnected</span></span> | <span data-ttu-id="72d66-154">Der er ingen forbindelse til Planlægningsoptimeringstjenesten.</span><span class="sxs-lookup"><span data-stu-id="72d66-154">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="72d66-155">Forbindelsen kan slås til fra LCS, som beskrevet tidligere i dette emne.</span><span class="sxs-lookup"><span data-stu-id="72d66-155">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="72d66-156">Nr.</span><span class="sxs-lookup"><span data-stu-id="72d66-156">No</span></span> |
| <span data-ttu-id="72d66-157">Forbindelse deaktiveres</span><span class="sxs-lookup"><span data-stu-id="72d66-157">Disabling connection</span></span> | <span data-ttu-id="72d66-158">En anmodning om at deaktivere forbindelsen til Planlægningsoptimeringstjenesten er i øjeblikket i gang.</span><span class="sxs-lookup"><span data-stu-id="72d66-158">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="72d66-159">Nr.</span><span class="sxs-lookup"><span data-stu-id="72d66-159">No</span></span> |
| <span data-ttu-id="72d66-160">Henter status</span><span class="sxs-lookup"><span data-stu-id="72d66-160">Getting status</span></span> | <span data-ttu-id="72d66-161">Systemet venter på statusoplysninger fra Planlægningsoptimeringstjenesten.</span><span class="sxs-lookup"><span data-stu-id="72d66-161">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="72d66-162">Nr.</span><span class="sxs-lookup"><span data-stu-id="72d66-162">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="72d66-163">Indstillingen Brug Planlægningsoptimering</span><span class="sxs-lookup"><span data-stu-id="72d66-163">The Use Planning Optimization option</span></span>

<span data-ttu-id="72d66-164">Indstillingen af indstillingen **Brug Planlægningsoptimering** bestemmer, hvilket planlægningsprogram der bruges til varedisponering:</span><span class="sxs-lookup"><span data-stu-id="72d66-164">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="72d66-165">**Ja** – Planlægningsoptimering bruges til varedisponering.</span><span class="sxs-lookup"><span data-stu-id="72d66-165">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="72d66-166">**Nej** – Det indbyggede planlægningsprogram for Supply Chain Management bruges til varedisponering.</span><span class="sxs-lookup"><span data-stu-id="72d66-166">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="72d66-167">Hvis de eksisterende planlægningsbatchjob, der blev oprettet til det indbyggede planlægningsprogram for Supply Chain Management, udløses mens indstillingen **Brug Planlægningsoptimering** er angivet til **Ja**, vil disse job ikke blive udført.</span><span class="sxs-lookup"><span data-stu-id="72d66-167">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="72d66-168">Integration med opsætningen</span><span class="sxs-lookup"><span data-stu-id="72d66-168">Integration with the setup</span></span>

<span data-ttu-id="72d66-169">Hvis forhåndsvisningen af Planlægningsoptimering er aktiveret, foretages varedisponering ved hjælp af tilføjelsesprogrammet for Planlægningsoptimering.</span><span class="sxs-lookup"><span data-stu-id="72d66-169">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="72d66-170">I dette tilfælde påvirkes resultaterne af og funktionerne for varedisponering.</span><span class="sxs-lookup"><span data-stu-id="72d66-170">In this case, master planning results and features are affected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="72d66-171">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="72d66-171">Additional resources</span></span>

[<span data-ttu-id="72d66-172">Vilkår og betingelser for forhåndsvisning</span><span class="sxs-lookup"><span data-stu-id="72d66-172">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="72d66-173">Oversigt over planlægningsoptimering</span><span class="sxs-lookup"><span data-stu-id="72d66-173">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="72d66-174">Analyse af om Planlægningsoptimering passer til</span><span class="sxs-lookup"><span data-stu-id="72d66-174">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="72d66-175">Få vist planhistorik og planlægningslogs</span><span class="sxs-lookup"><span data-stu-id="72d66-175">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="72d66-176">Anvend filtre på en plan</span><span class="sxs-lookup"><span data-stu-id="72d66-176">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="72d66-177">Annullere et planlægningsjob</span><span class="sxs-lookup"><span data-stu-id="72d66-177">Cancel a planning job</span></span>](cancel-planning-job.md)
