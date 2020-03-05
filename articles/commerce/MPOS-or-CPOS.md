---
title: Vælge mellem Modern POS (MPOS) og Cloud POS
description: I dette emne beskrives de grundlæggende forskelle mellem Modern POS og Cloud POS. Emnet beskriver også forskellige faktorer, som detailhandlere, der implementerer Dynamics 365 Commerce, bør overveje, så de bedre kan foretage det rette valg ud fra deres behov.
author: jblucher
manager: AnnBe
ms.date: 10/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2017-10-12
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 1fffc7141c041873f39f716aaf1a775984ef499c
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021945"
---
# <a name="choose-between-modern-pos-mpos-and-cloud-pos"></a><span data-ttu-id="932fe-104">Vælge mellem Modern POS (MPOS) og Cloud POS</span><span class="sxs-lookup"><span data-stu-id="932fe-104">Choose between Modern POS (MPOS) and Cloud POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="932fe-105">Emnet giver implementeringskonsulenter yderligere baggrund, tip og vejledning til de faktorer, som de skal overveje, når de installerer Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="932fe-105">This topic gives implementers additional background, tips, and guidance for factors that they should consider when they deploy Dynamics 365 Commerce.</span></span> <span data-ttu-id="932fe-106">Ved at gennemse og følge denne vejledning som en del af installationsprocessen kan implementeringskonsulenter undgå problemer, der kan påvirke brugertilfredsheden eller ydeevnen.</span><span class="sxs-lookup"><span data-stu-id="932fe-106">By reviewing and following this guidance as part of the deployment process, implementers can avoid issues that might affect user satisfaction or performance.</span></span>

## <a name="insights"></a><span data-ttu-id="932fe-107">Indsigt</span><span class="sxs-lookup"><span data-stu-id="932fe-107">Insights</span></span>

<span data-ttu-id="932fe-108">Commerce indeholder en lang række installations- og topologiindstillinger.</span><span class="sxs-lookup"><span data-stu-id="932fe-108">Commerce provides a wide range of deployment and topology options.</span></span> <span data-ttu-id="932fe-109">Detailhandlere kan derfor vælge de komponenter og den konfiguration, der bedst opfylder deres forretnings- og teknologikrav.</span><span class="sxs-lookup"><span data-stu-id="932fe-109">Therefore, retailers can choose the components and configuration that best meet their business and technology requirements.</span></span> <span data-ttu-id="932fe-110">Et aspekt af implementering, der kræver nøje overvejelser, er valget af en platform og formfaktor til POS-komponenten.</span><span class="sxs-lookup"><span data-stu-id="932fe-110">One aspect of implementation that requires careful consideration is the choice of a platform and form factor for the point of sale (POS) component.</span></span>

### <a name="pos-platform-and-form-factor-considerations"></a><span data-ttu-id="932fe-111">Overvejelser i forbindelse med POS-platform og formfaktor</span><span class="sxs-lookup"><span data-stu-id="932fe-111">POS platform and form factor considerations</span></span>

<span data-ttu-id="932fe-112">Commerce understøtter følgende POS-indstillinger:</span><span class="sxs-lookup"><span data-stu-id="932fe-112">Commerce supports the following POS options:</span></span>

- <span data-ttu-id="932fe-113">Modern POS (MPOS) til Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="932fe-113">Modern POS (MPOS) for Microsoft Windows</span></span>
- <span data-ttu-id="932fe-114">MPOS til Microsoft Windows Phone</span><span class="sxs-lookup"><span data-stu-id="932fe-114">MPOS for Microsoft Windows Phone</span></span>
- <span data-ttu-id="932fe-115">MPOS til Apple iPad eller Google Android-tablet</span><span class="sxs-lookup"><span data-stu-id="932fe-115">MPOS for Apple iPad or Google Android tablet</span></span>
- <span data-ttu-id="932fe-116">Cloud POS (CPOS), som understøtter Microsoft Edge-, Internet Explorer- og Google Chrome-browsere</span><span class="sxs-lookup"><span data-stu-id="932fe-116">Cloud POS (CPOS), which supports the Microsoft Edge, Internet Explorer, and Google Chrome browsers</span></span>

<span data-ttu-id="932fe-117">I alle tilfælde deler POS (MPOS og CPOS) samme kerneprogramkode.</span><span class="sxs-lookup"><span data-stu-id="932fe-117">In all cases, the POS (MPOS and CPOS) shares the same core application code.</span></span> <span data-ttu-id="932fe-118">Dette er vigtigt af følgende årsager:</span><span class="sxs-lookup"><span data-stu-id="932fe-118">This point is important for the following reasons:</span></span>

- <span data-ttu-id="932fe-119">Brugergrænsefladen (UI) er ensartet på tværs af platformen eller formfaktoren.</span><span class="sxs-lookup"><span data-stu-id="932fe-119">The user interface (UI) is consistent, regardless of the platform or form factor.</span></span>
- <span data-ttu-id="932fe-120">De fleste af de funktionelle egenskaber er de samme, uanset platform eller formfaktor.</span><span class="sxs-lookup"><span data-stu-id="932fe-120">Most of the functional capabilities are the same, regardless of the platform or form factor.</span></span> <span data-ttu-id="932fe-121">Der er dog nogle vigtige forskelle.</span><span class="sxs-lookup"><span data-stu-id="932fe-121">However, there are some important differences.</span></span> <span data-ttu-id="932fe-122">Disse forskelle er anført i dette emne.</span><span class="sxs-lookup"><span data-stu-id="932fe-122">These differences are noted in this topic.</span></span>
- <span data-ttu-id="932fe-123">I en bestemt butik kan POS-variationerne kombineres og kan køre samtidigt.</span><span class="sxs-lookup"><span data-stu-id="932fe-123">In a given store, the POS variations can be combined and can run concurrently.</span></span> <span data-ttu-id="932fe-124">For eksempel kan en forhandler til sine overordnede kasseapparater bruge MPOS på computere, der kører Windows.</span><span class="sxs-lookup"><span data-stu-id="932fe-124">For example, for its main registers, a retailer can use MPOS on computers that run Windows.</span></span> <span data-ttu-id="932fe-125">Forhandleren kan imidlertid supplere disse kasseapparater med browserbaserede terminaler eller mobilenheder.</span><span class="sxs-lookup"><span data-stu-id="932fe-125">However, the retailer can supplement those registers with browser-based terminals or mobile devices.</span></span>
- <span data-ttu-id="932fe-126">Tilpasninger og udvidelser kan nemt bruges på tværs af platforme og formfaktorer.</span><span class="sxs-lookup"><span data-stu-id="932fe-126">Customizations and extensions can easily be used across platforms and form factors.</span></span> <span data-ttu-id="932fe-127">Da kerneprogramkoden er delt, kan de fleste tilpasninger implementeres én gang i stedet for flere gange.</span><span class="sxs-lookup"><span data-stu-id="932fe-127">Because the core application code is shared, most customizations can be implemented one time instead of multiple times.</span></span>

### <a name="mpos-vs-cpos"></a><span data-ttu-id="932fe-128">MPOS vs. CPOS</span><span class="sxs-lookup"><span data-stu-id="932fe-128">MPOS vs. CPOS</span></span>

<span data-ttu-id="932fe-129">Selvom MPOS og CPOS stort set er ens, er der nogle vigtige forskelle, som du skal kende.</span><span class="sxs-lookup"><span data-stu-id="932fe-129">Although MPOS and CPOS are largely the same, there are some important differences that you must understand.</span></span>

#### <a name="mpos"></a><span data-ttu-id="932fe-130">MPOS</span><span class="sxs-lookup"><span data-stu-id="932fe-130">MPOS</span></span>

<span data-ttu-id="932fe-131">MPOS på en Windows-, iOS- eller Android-enhed er et program, der pakkes, installeres og serviceres på enheden.</span><span class="sxs-lookup"><span data-stu-id="932fe-131">MPOS on a Windows, iOS, or Android device is an application that is packaged, installed, and serviced on that device.</span></span>

- <span data-ttu-id="932fe-132">**Windows** – MPOS for Windows-programmet indeholder al programkode og det integrerede Commerce Runtime (CRT).</span><span class="sxs-lookup"><span data-stu-id="932fe-132">**Windows** – The MPOS for Windows application contains all the application code and the embedded commerce runtime (CRT).</span></span> 
- <span data-ttu-id="932fe-133">**iOS/Android** – På disse platforme fungerer programmet som vært for CPOS-programkoden.</span><span class="sxs-lookup"><span data-stu-id="932fe-133">**iOS/Android** – On these platforms, the application acts as a host for the CPOS application code.</span></span> <span data-ttu-id="932fe-134">Med andre ord kommer programkoden fra CPOS-serveren på Microsoft Azure eller Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="932fe-134">In other words, the application code comes from the CPOS server on Microsoft Azure or the Commerce Scale Unit.</span></span> <span data-ttu-id="932fe-135">Du kan finde flere oplysninger under [Oversigt over Retail Store Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/retail-store-system-begin).</span><span class="sxs-lookup"><span data-stu-id="932fe-135">For more information, see [Retail Store Scale Unit overview](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/retail-store-system-begin).</span></span>

#### <a name="cpos"></a><span data-ttu-id="932fe-136">CPOS</span><span class="sxs-lookup"><span data-stu-id="932fe-136">CPOS</span></span>

<span data-ttu-id="932fe-137">Da CPOS kører i en browser, bliver programmet ikke installeret på enheden.</span><span class="sxs-lookup"><span data-stu-id="932fe-137">Because CPOS runs in a browser, the application isn't installed on the device.</span></span> <span data-ttu-id="932fe-138">I stedet får browseren adgang til programkoden fra CPOS-serveren.</span><span class="sxs-lookup"><span data-stu-id="932fe-138">Instead, the browser accesses the application code from the CPOS server.</span></span> <span data-ttu-id="932fe-139">Derfor kan CPOS ikke få direkte adgang til POS-hardware eller arbejde i offlinetilstand.</span><span class="sxs-lookup"><span data-stu-id="932fe-139">Therefore, CPOS can't directly access POS hardware or work in an offline state.</span></span>

### <a name="store-deployment-considerations"></a><span data-ttu-id="932fe-140">Overvejelser om installation i butik</span><span class="sxs-lookup"><span data-stu-id="932fe-140">Store deployment considerations</span></span>

<span data-ttu-id="932fe-141">Ud over en platform og formfaktor skal detailhandlere også vælge en implementeringsindstilling i butikken.</span><span class="sxs-lookup"><span data-stu-id="932fe-141">In addition to a platform and form factor, retailers must also choose a deployment option at the store.</span></span> <span data-ttu-id="932fe-142">I følgende tabel vises de konfigurationer, der er tilgængelige for hver POS-indstilling.</span><span class="sxs-lookup"><span data-stu-id="932fe-142">The following table shows the configurations that are available for each POS option.</span></span>

| <span data-ttu-id="932fe-143">POS-program</span><span class="sxs-lookup"><span data-stu-id="932fe-143">POS application</span></span>         | <span data-ttu-id="932fe-144">Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="932fe-144">Commerce Scale Unit</span></span> | <span data-ttu-id="932fe-145">Tilgængelig offline</span><span class="sxs-lookup"><span data-stu-id="932fe-145">Available offline</span></span> |
|-------------------------|---------------|-------------------|
| <span data-ttu-id="932fe-146">MPOS for Windows</span><span class="sxs-lookup"><span data-stu-id="932fe-146">MPOS for Windows</span></span>        | <span data-ttu-id="932fe-147">Cloud eller RSSU</span><span class="sxs-lookup"><span data-stu-id="932fe-147">Cloud or RSSU</span></span> | <span data-ttu-id="932fe-148">Ja</span><span class="sxs-lookup"><span data-stu-id="932fe-148">Yes</span></span>               |
| <span data-ttu-id="932fe-149">MPOS for iOS eller Android</span><span class="sxs-lookup"><span data-stu-id="932fe-149">MPOS for iOS or Android</span></span> | <span data-ttu-id="932fe-150">Cloud eller RSSU</span><span class="sxs-lookup"><span data-stu-id="932fe-150">Cloud or RSSU</span></span> | <span data-ttu-id="932fe-151">Nr.</span><span class="sxs-lookup"><span data-stu-id="932fe-151">No</span></span>                |
| <span data-ttu-id="932fe-152">Cloud POS</span><span class="sxs-lookup"><span data-stu-id="932fe-152">Cloud POS</span></span>               | <span data-ttu-id="932fe-153">Cloud eller RSSU</span><span class="sxs-lookup"><span data-stu-id="932fe-153">Cloud or RSSU</span></span> | <span data-ttu-id="932fe-154">Nr.</span><span class="sxs-lookup"><span data-stu-id="932fe-154">No</span></span>                |

#### <a name="commerce-scale-unit"></a><span data-ttu-id="932fe-155">Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="932fe-155">Commerce Scale Unit</span></span>

<span data-ttu-id="932fe-156">Commerce Scale Unit er en komponent, der er vært for CRT.</span><span class="sxs-lookup"><span data-stu-id="932fe-156">The Commerce Scale Unit is a component that hosts the CRT.</span></span> <span data-ttu-id="932fe-157">CRT indeholder al forretningslogik, som POS bruger, og giver adgang til kanaldatabasen.</span><span class="sxs-lookup"><span data-stu-id="932fe-157">The CRT contains all the business logic that the POS uses, and it provides access to the channel database.</span></span> <span data-ttu-id="932fe-158">Mens de er online, kan alle POS-klienter i butikken bruge Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="932fe-158">While they are online, all POS clients in the store use the Commerce Scale Unit.</span></span> <span data-ttu-id="932fe-159">Commerce Scale Unit kan implementeres enten i skyen eller i butikken.</span><span class="sxs-lookup"><span data-stu-id="932fe-159">The Commerce Scale Unit can be deployed either in the cloud or in the store.</span></span>

#### <a name="offline-mode"></a><span data-ttu-id="932fe-160">Offlinetilstand</span><span class="sxs-lookup"><span data-stu-id="932fe-160">Offline mode</span></span>

<span data-ttu-id="932fe-161">MPOS til Windows understøtter offlinetilstand.</span><span class="sxs-lookup"><span data-stu-id="932fe-161">MPOS for Windows supports offline mode.</span></span> <span data-ttu-id="932fe-162">I offlinetilstand kan POS fortsætte med at behandle salg, selvom forbindelsen til Commerce Scale Unit bliver afbrudt.</span><span class="sxs-lookup"><span data-stu-id="932fe-162">In offline mode, the POS can continue to process sales even if it's disconnected from the Commerce Scale Unit.</span></span> <span data-ttu-id="932fe-163">Det kan derefter synkroniseres med kanaldatabasen, når forbindelsen er genoprettet.</span><span class="sxs-lookup"><span data-stu-id="932fe-163">It can then be synchronized with the channel database when connectivity is restored.</span></span> <span data-ttu-id="932fe-164">MPOS bruger sin egen integrerede forekomst af CRT og bruger midlertidigt sin egen lokale datakilde (offline SQL Server-database).</span><span class="sxs-lookup"><span data-stu-id="932fe-164">MPOS uses its own embedded instance of the CRT and temporarily uses its own local data source (offline SQL Server database).</span></span> <span data-ttu-id="932fe-165">Du kan finde flere oplysninger om offlinefunktionalitet under [POS-offlinefunktionalitet](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-offline-functionality).</span><span class="sxs-lookup"><span data-stu-id="932fe-165">For more information about offline functionality, see [POS offline functionality](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-offline-functionality).</span></span>

### <a name="pos-peripheralhardware-considerations"></a><span data-ttu-id="932fe-166">Overvejelser i forbindelse med eksterne POS-enheder/POS-hardware</span><span class="sxs-lookup"><span data-stu-id="932fe-166">POS peripheral/hardware considerations</span></span>

<span data-ttu-id="932fe-167">Detailhandlere skal også overveje, hvordan POS kan få adgang til enheder og eksterne enheder som printere, pengeskuffer og betalingsterminaler.</span><span class="sxs-lookup"><span data-stu-id="932fe-167">Retailers must also consider how the POS will access devices and peripherals such as printers, cash drawers, and payment terminals.</span></span> <span data-ttu-id="932fe-168">Kun MPOS for Windows understøtter direkte kommunikation med disse enheder.</span><span class="sxs-lookup"><span data-stu-id="932fe-168">Only MPOS for Windows supports direct communication with these devices.</span></span> <span data-ttu-id="932fe-169">MPOS for Windows Phone, iOS eller Android og Cloud POS kræver en hardwarestation for at få adgang til disse enheder.</span><span class="sxs-lookup"><span data-stu-id="932fe-169">MPOS for Windows Phone, iOS, or Android, and Cloud POS require a hardware station in order to access these devices.</span></span> <span data-ttu-id="932fe-170">Hardwarestationer kan dedikeres til et POS-kasseapparat eller deles af kasseapparaterne i butikken.</span><span class="sxs-lookup"><span data-stu-id="932fe-170">Hardware stations can be dedicated to a POS register or shared among the registers in a store.</span></span> <span data-ttu-id="932fe-171">Du kan finde flere oplysninger om hardwarestationener i [Konfigurere og installere hardwarestation til detail](https://docs.microsoft.com/dynamics365/unified-operations/retail/retail-hardware-station-configuration-installation).</span><span class="sxs-lookup"><span data-stu-id="932fe-171">For more information about hardware stations, see [Configure and install Retail hardware station](https://docs.microsoft.com/dynamics365/unified-operations/retail/retail-hardware-station-configuration-installation).</span></span>

## <a name="implementation-considerations"></a><span data-ttu-id="932fe-172">Overvejelser i forbindelse med implementering</span><span class="sxs-lookup"><span data-stu-id="932fe-172">Implementation considerations</span></span>

<span data-ttu-id="932fe-173">Når du planlægger POS-implementeringen i dine butikker, skal du overveje følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="932fe-173">Consider the following information as you plan your POS implementation in your stores:</span></span>

- <span data-ttu-id="932fe-174">**Funktionskrav** – Kerneforretningsaktiviteter og -egenskaber er de samme, uanset platform, formfaktor eller topologien til installationen.</span><span class="sxs-lookup"><span data-stu-id="932fe-174">**Functional requirements** – The core business processes and capabilities are the same, regardless of the platform, form factor, or deployment topology.</span></span> <span data-ttu-id="932fe-175">De fleste forhandlere behøver derfor ikke at overveje funktionskrav, når de planlægger deres implementering.</span><span class="sxs-lookup"><span data-stu-id="932fe-175">Therefore, most retailers don't have to consider functional requirements when they plan their implementation.</span></span>
- <span data-ttu-id="932fe-176">**Forbindelse** – Tilgængelighed på netværket (Wide Area Network \[WAN\] og Local Area Network \[LAN\]) er en vigtig faktor, der kræver nøje overvejelser.</span><span class="sxs-lookup"><span data-stu-id="932fe-176">**Connectivity** – Network availability (wide area network \[WAN\] and local area network \[LAN\]) is a major factor that requires careful consideration.</span></span> <span data-ttu-id="932fe-177">Eventuelle fordele, som en ikke-pladskrævende, skybaseret løsning giver dig med hensyn til omkostninger og enkelhed, går tabt, hvis systemet ikke er tilgængeligt for forretningskritiske processer.</span><span class="sxs-lookup"><span data-stu-id="932fe-177">Any benefits that a zero-footprint, cloud-hosted solution brings in terms of cost and simplicity are lost if the system isn't available for business-critical processes.</span></span>

    <span data-ttu-id="932fe-178">Medmindre forbindelsen for en given enhed er meget pålidelig og fleksibel, eller medmindre en bestemt mængde nedetid er acceptabel for detailhandleren, anbefaler vi en af følgende muligheder:</span><span class="sxs-lookup"><span data-stu-id="932fe-178">Unless the connectivity for a given device is very dependable and resilient, or unless a certain amount of downtime is acceptable to the retailer, we recommend one of the following options:</span></span>

    - <span data-ttu-id="932fe-179">Brug MPOS i Windows, og aktivér offlinetilstand.</span><span class="sxs-lookup"><span data-stu-id="932fe-179">Use MPOS in Windows, and enable offline mode.</span></span>
    - <span data-ttu-id="932fe-180">Installer en Commerce Scale Unit i det lokale miljø.</span><span class="sxs-lookup"><span data-stu-id="932fe-180">Deploy an on-premises Commerce Scale Unit.</span></span>

    <span data-ttu-id="932fe-181">Disse to indstillinger udelukker ikke gensidigt hinanden.</span><span class="sxs-lookup"><span data-stu-id="932fe-181">These two options aren't mutually exclusive.</span></span> <span data-ttu-id="932fe-182">Den mest pålidelige topologi detailhandlere kan implementere en lokal RSSU for at mindske afhængigheden af forbindelse til internettet eller Azure tilgængelighed og de kan også installere POS-kasseapparater, hvor offline-tilstand er aktiveret, hvis der er et problem med den lokale server eller et netværk.</span><span class="sxs-lookup"><span data-stu-id="932fe-182">For the most reliable topology, retailers can deploy a local RSSU to reduce the dependency on internet connectivity or Azure availability, and they can also deploy POS registers where offline mode is enabled if there is an issue with the local server or network.</span></span>

- <span data-ttu-id="932fe-183">**Hardwareenheder/eksterne enheder/** – Et vigtigt aspekt ved et Retail POS-system er dets evne til at bruge eksterne POS-enheder som printere, pengeskuffer og betalingsterminaler.</span><span class="sxs-lookup"><span data-stu-id="932fe-183">**Hardware devices/peripherals** – One important aspect of a Retail POS system is its ability to use POS peripherals such as printers, cash drawers, and payment terminals.</span></span> <span data-ttu-id="932fe-184">Selvom alle de tilgængelige POS-muligheder kan bruge eksterne enheder, er det kun MPOS for Windows der understøtter dem direkte.</span><span class="sxs-lookup"><span data-stu-id="932fe-184">Although all the available POS options can use peripheral devices, only MPOS for Windows supports them directly.</span></span> <span data-ttu-id="932fe-185">Alle andre programmer kræver en eller flere hardwarestationer.</span><span class="sxs-lookup"><span data-stu-id="932fe-185">For all other applications, one or more hardware stations are required.</span></span> <span data-ttu-id="932fe-186">Selvom denne metode giver fleksibilitet, skal yderligere komponenter installeres, konfigureres og serviceres.</span><span class="sxs-lookup"><span data-stu-id="932fe-186">Although this approach adds flexibility, additional components must be deployed, configured, and serviced.</span></span>
- <span data-ttu-id="932fe-187">**Systemkrav** – Systemkravene til POS-programmet varierer.</span><span class="sxs-lookup"><span data-stu-id="932fe-187">**System requirements** – The system requirements for the POS application vary.</span></span> <span data-ttu-id="932fe-188">Sørg for at se de seneste oplysninger, før du foretager dit valg.</span><span class="sxs-lookup"><span data-stu-id="932fe-188">Be sure to check the latest information before you make your choice.</span></span> <span data-ttu-id="932fe-189">For eksempel kører CPOS i en browser og understøtter derfor flere operativsystemer.</span><span class="sxs-lookup"><span data-stu-id="932fe-189">For example, because CPOS runs in a browser, it supports a wider range of operating systems.</span></span> <span data-ttu-id="932fe-190">Du kan finde flere oplysninger om systemkrav i [Systemkrav til skyinstallationer](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/system-requirements).</span><span class="sxs-lookup"><span data-stu-id="932fe-190">For more information about system requirements, see [System requirements for cloud deployments](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/system-requirements).</span></span>
- <span data-ttu-id="932fe-191">**Installation og vedligeholdelse** – Kompleksiteten i installations- og vedligeholdelseskrav kan variere, afhængigt af program- og installationsvalg.</span><span class="sxs-lookup"><span data-stu-id="932fe-191">**Deployment and servicing** – The complexity of the deployment and servicing requirements can vary, depending on the application and deployment choices.</span></span> <span data-ttu-id="932fe-192">En skybaseret CPOS-installation kræver f.eks. ikke, at du installerer og opdaterer på hver enhed.</span><span class="sxs-lookup"><span data-stu-id="932fe-192">For example, for a cloud-hosted CPOS deployment, you don't have to install and update on every device.</span></span> <span data-ttu-id="932fe-193">Denne metode reducerer derfor kompleksitet og omkostninger meget.</span><span class="sxs-lookup"><span data-stu-id="932fe-193">Therefore, this approach greatly reduces complexity and cost.</span></span> <span data-ttu-id="932fe-194">Men hvis du installerer MPOS på hvert kasseapparat og aktiverer offlinetilstand og også installerer delte hardwarestationer, øger du antallet af slutpunkter, der skal administreres, meget.</span><span class="sxs-lookup"><span data-stu-id="932fe-194">However, if you deploy MPOS on every register and enable offline mode, and you also deploy shared hardware stations, you greatly increase the number of endpoints that must be managed.</span></span>