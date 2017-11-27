---
title: Systemkrav til skyinstallationer
description: Dette emne viser systemkravene til den aktuelle version af Microsoft Dynamics 365 for Finance and Operations, Enterprise edition til skyinstallationer.
author: sericks007
manager: AnnBe
ms.date: 08/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 83637b4b2ccc01950e68569b3b8bee1a7cd69855
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="system-requirements-for-cloud-deployments"></a><span data-ttu-id="3d41e-103">Systemkrav til skyinstallationer</span><span class="sxs-lookup"><span data-stu-id="3d41e-103">System requirements for cloud deployments</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="3d41e-104">Dette emne viser systemkravene til den aktuelle version af Microsoft Dynamics 365 for Finance and Operations, Enterprise edition til skyinstallationer.</span><span class="sxs-lookup"><span data-stu-id="3d41e-104">This topic lists the system requirements for the current version of Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, for cloud deployments.</span></span> <span data-ttu-id="3d41e-105">Før du installerer Finance and Operations, skal du evt. kontrollere, at det system, du bruger, opfylder eller overstiger minimumkrav til netværk, hardware og software.</span><span class="sxs-lookup"><span data-stu-id="3d41e-105">Before you install Finance and Operations, when this step is appropriate, verify that the system that you're working with meets or exceeds the minimum network, hardware, and software requirements.</span></span>

## <a name="supported-web-browsers"></a><span data-ttu-id="3d41e-106">Understøttede webbrowsere</span><span class="sxs-lookup"><span data-stu-id="3d41e-106">Supported web browsers</span></span>
<span data-ttu-id="3d41e-107">Webprogrammet kan køre i en af følgende webbrowsere, der kører på de angivne operativsystemer:</span><span class="sxs-lookup"><span data-stu-id="3d41e-107">The web application can run in any of the following web browsers that run on the specified operating systems:</span></span>

-   <span data-ttu-id="3d41e-108">Microsoft Edge (nyeste offentligt tilgængelige version) på Windows-10</span><span class="sxs-lookup"><span data-stu-id="3d41e-108">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
-   <span data-ttu-id="3d41e-109">Internet Explorer 11 på Windows 10, Windows 8.1 eller Windows 7</span><span class="sxs-lookup"><span data-stu-id="3d41e-109">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
-   <span data-ttu-id="3d41e-110">Google Chrome (nyeste offentligt tilgængelige version) på Windows 10, Windows 8.1, Windows 8, Windows 7 eller Google Nexus 10-tablet</span><span class="sxs-lookup"><span data-stu-id="3d41e-110">Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet</span></span>
-   <span data-ttu-id="3d41e-111">Apple Safari (nyeste offentligt tilgængelige version) på Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) 10.12 (Sierra) eller Apple iPad</span><span class="sxs-lookup"><span data-stu-id="3d41e-111">Apple Safari (latest publicly available version) on Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) or 10.12 (Sierra), or Apple iPad</span></span>

<span data-ttu-id="3d41e-112">Gå til producentens websted for at finde den nyeste version af hver webbrowser.</span><span class="sxs-lookup"><span data-stu-id="3d41e-112">To find the latest release for each web browser, go to the software manufacturer’s website.</span></span> 

> [!NOTE]
> -   <span data-ttu-id="3d41e-113">Du skal installere en foreløbig version af Chrome-udvidelsen, for at Arbejdsrutineoptager kan tage skærmbilleder og medtage dem i de Microsoft Word-dokumenter, der genereres.</span><span class="sxs-lookup"><span data-stu-id="3d41e-113">You must install a pre-release Chrome extension to enable Task Recorder to capture screenshots and include them in Microsoft Word documents that are generated.</span></span> <!---For instructions about how to install the extension, see [Screenshot Extension setup](../../dev-itpro/user-interface/task-recorder).-->
> -   <span data-ttu-id="3d41e-114">Arbejdsgangseditoren startes som et ClickOnce-program.</span><span class="sxs-lookup"><span data-stu-id="3d41e-114">The Workflow Editor is started as a ClickOnce application.</span></span> <span data-ttu-id="3d41e-115">Kun Microsoft Edge og Internet Explorer (på en understøttet version af Microsoft Windows) understøtter ClickOnce-programmer.</span><span class="sxs-lookup"><span data-stu-id="3d41e-115">Only Microsoft Edge and Internet Explorer (on a supported version of Microsoft Windows) support ClickOnce applications.</span></span> <span data-ttu-id="3d41e-116">ClickOnce-programmet til arbejdsgangseditoren kræver et kompatibelt 64-bit-operativsystem.</span><span class="sxs-lookup"><span data-stu-id="3d41e-116">The Workflow Editor ClickOnce application requires a 64-bit-compatible operating system.</span></span>
> -   <span data-ttu-id="3d41e-117">Report Designer til finansiel rapportering startes som et ClickOnce-program.</span><span class="sxs-lookup"><span data-stu-id="3d41e-117">The Report Designer for Financial reporting is started as a ClickOnce application.</span></span> <span data-ttu-id="3d41e-118">Det kræver et kompatibelt 64-bit-operativsystem.</span><span class="sxs-lookup"><span data-stu-id="3d41e-118">It requires a 64-bit-compatible operating system.</span></span> <span data-ttu-id="3d41e-119">Hvis du bruger Chrome, skal du installere en ClickOnce-udvidelse for at kunne hente Report Designer-klienten.</span><span class="sxs-lookup"><span data-stu-id="3d41e-119">If you’re using Chrome, you must install a ClickOnce extension to download the Report Designer client.</span></span> <span data-ttu-id="3d41e-120">Hvis du bruger Chrome i Incognito-tilstand, skal du kontrollere, at ClickOnce-udvidelsen også er aktiveret til Incognito-tilstand.</span><span class="sxs-lookup"><span data-stu-id="3d41e-120">If you use Chrome in Incognito mode, make sure that the ClickOnce extension is also enabled for Incognito mode.</span></span>
> -   <span data-ttu-id="3d41e-121">Hvis du vil se PDF-filer, anbefaler vi, at du bruger browsere som f.eks. Microsoft Edge (seneste offentligt tilgængelige version) i Windows 10 eller Google Chrome (seneste offentligt tilgængelige version) i Windows 10, Windows 8.1, Windows 8, Windows 7 eller Google Nexus 10-tabletten.</span><span class="sxs-lookup"><span data-stu-id="3d41e-121">To preview PDF files, we recommend that you use browsers such as Microsoft Edge (latest publicly available version) on Windows 10, or Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet.</span></span>

### <a name="supported-web-browsers-for-retail-cloud-pos"></a><span data-ttu-id="3d41e-122">Understøttede webbrowsere for Retail Cloud POS</span><span class="sxs-lookup"><span data-stu-id="3d41e-122">Supported web browsers for Retail Cloud POS</span></span>

<span data-ttu-id="3d41e-123">Retail Cloud POS kan køre i en af følgende webbrowsere, der kører på de angivne operativsystemer:</span><span class="sxs-lookup"><span data-stu-id="3d41e-123">Retail Cloud POS can run in any of the following web browsers that run on the specified operating systems:</span></span>

-   <span data-ttu-id="3d41e-124">Microsoft Edge (nyeste offentligt tilgængelige version) på Windows-10</span><span class="sxs-lookup"><span data-stu-id="3d41e-124">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
-   <span data-ttu-id="3d41e-125">Internet Explorer 11 på Windows 10, Windows 8.1 eller Windows 7</span><span class="sxs-lookup"><span data-stu-id="3d41e-125">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
-   <span data-ttu-id="3d41e-126">Chrome (seneste offentligt tilgængelige version) på Windows 10, Windows 8.1 eller Windows 7</span><span class="sxs-lookup"><span data-stu-id="3d41e-126">Chrome (latest publicly available version) on Windows 10, Windows 8.1, or Windows 7</span></span>

## <a name="network-requirements"></a><span data-ttu-id="3d41e-127">Netværkskrav</span><span class="sxs-lookup"><span data-stu-id="3d41e-127">Network requirements</span></span>
-   <span data-ttu-id="3d41e-128">Finance and Operations er designet til netværk, der har en ventetid på 250-300 millisekunder (ms) eller mindre.</span><span class="sxs-lookup"><span data-stu-id="3d41e-128">Finance and Operations is designed for networks that have a latency of 250–300 milliseconds (ms) or less.</span></span> <span data-ttu-id="3d41e-129">Denne ventetid fra en browserklient til Microsoft Azure-datacenteret, der er vært for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3d41e-129">This latency is the latency from a browser client to the Microsoft Azure datacenter that hosts Finance and Operations.</span></span> <span data-ttu-id="3d41e-130">Vi anbefaler, at du tester netværksventetiden på <http://www.azurespeed.com>.</span><span class="sxs-lookup"><span data-stu-id="3d41e-130">We recommend that you test network latency at <http://www.azurespeed.com>.</span></span>
-   <span data-ttu-id="3d41e-131">Kravene til båndbredde for Finance and Operations afhænger af scenariet.</span><span class="sxs-lookup"><span data-stu-id="3d41e-131">Bandwidth requirements for Finance and Operations depend on your scenario.</span></span> <span data-ttu-id="3d41e-132">De fleste typiske scenarier kræver en båndbredde på mere end 50 kilobyte pr. sekund (KBps).</span><span class="sxs-lookup"><span data-stu-id="3d41e-132">Most typical scenarios require a bandwidth of more than 50 kilobytes per second (KBps).</span></span> <span data-ttu-id="3d41e-133">Men vi anbefaler mere båndbredde til scenarier, der har store datakrav, f.eks. arbejdsområder eller omfattende tilpasning.</span><span class="sxs-lookup"><span data-stu-id="3d41e-133">However, we recommend more bandwidth for scenarios that have high payload requirements, such as scenarios that involve workspaces or extensive customization.</span></span>

<span data-ttu-id="3d41e-134">Generelt er Finance and Operations optimeret til internettet.</span><span class="sxs-lookup"><span data-stu-id="3d41e-134">In general, Finance and Operations is optimized for the internet.</span></span> <span data-ttu-id="3d41e-135">Antallet af rundture fra en browserklient til Azure-datacenteret er meget lille, og alle data komprimeres.</span><span class="sxs-lookup"><span data-stu-id="3d41e-135">The number of round trips from a browser client to the Azure datacenter is very small, and the whole payload is compressed.</span></span> 

> [!WARNING]
> <span data-ttu-id="3d41e-136">Du må ikke beregne kravene til båndbredde fra en klientlokalitet ved at multiplicere antallet af brugere med minimumkravene til båndbredde.</span><span class="sxs-lookup"><span data-stu-id="3d41e-136">Don't calculate bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="3d41e-137">Den samtidig brug af en given lokalitet er meget vanskeligt at beregne.</span><span class="sxs-lookup"><span data-stu-id="3d41e-137">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="3d41e-138">Kunder, der er bekymret over kravene til båndbredde, kan bruge en prøveversion af Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3d41e-138">Customers who are concerned about bandwidth requirements should use a preview version of Finance and Operations.</span></span>

## <a name="net-framework-requirements"></a><span data-ttu-id="3d41e-139">.NET Framework-krav</span><span class="sxs-lookup"><span data-stu-id="3d41e-139">.NET Framework requirements</span></span>
<span data-ttu-id="3d41e-140">Finance and Operations kræver Microsoft .NET Framework version 4.6.2 til alle ClickOnce-programmer, f.eks. ruteplanlægningsagenten for dokumenter.</span><span class="sxs-lookup"><span data-stu-id="3d41e-140">Finance and Operations requires the Microsoft .NET Framework version 4.6.2 for all ClickOnce applications, such as the document routing agent.</span></span> <span data-ttu-id="3d41e-141">Se installationsvejledning i [Installation af. NET Framework-](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="3d41e-141">For installation instructions, see [Installing the .NET Framework](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="3d41e-142">Understøttede Microsoft Office-programmer</span><span class="sxs-lookup"><span data-stu-id="3d41e-142">Supported Microsoft Office applications</span></span>
<span data-ttu-id="3d41e-143">Følgende Microsoft Office-programmer understøttes i installationerne af Finance and Operations i skyen og det lokale miljø:</span><span class="sxs-lookup"><span data-stu-id="3d41e-143">The following Microsoft Office applications are supported in cloud and on-premises deployments of Finance and Operations:</span></span>

-   <span data-ttu-id="3d41e-144">Hvis du vil køre tilføjelsesprogrammer til Microsoft Excel og Word, skal du have Microsoft Office 2016 til Windows eller Mac installeret.</span><span class="sxs-lookup"><span data-stu-id="3d41e-144">To run the Microsoft Excel and Word add-ins, you must have Microsoft Office 2016 for Windows or Mac installed.</span></span> <span data-ttu-id="3d41e-145">Du kan finde yderligere oplysninger om versionskrav i [Fejlfinding af Office-integration](../../dev-itpro/office-integration/office-integration-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="3d41e-145">For more information about version requirements, see [Office integration troubleshooting](../../dev-itpro/office-integration/office-integration-troubleshooting.md).</span></span>
-   <span data-ttu-id="3d41e-146">Hvis du vil have vist dokumenter, der er genereret med funktionerne Eksport til Excel eller Eksport til Word, skal have Microsoft Office 2007 eller nyere installeret.</span><span class="sxs-lookup"><span data-stu-id="3d41e-146">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="retail-modern-pos-requirements"></a><span data-ttu-id="3d41e-147">Retail Modern POS-krav</span><span class="sxs-lookup"><span data-stu-id="3d41e-147">Retail Modern POS requirements</span></span>

> [!NOTE]
> <span data-ttu-id="3d41e-148">Hvis Retail Modern POS vil bruge en offlinedatabase, skal computeren opfylde alle systemkrav til Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3d41e-148">If Retail Modern POS will use an offline database, the computer must meet all system requirements for Microsoft SQL Server.</span></span> <span data-ttu-id="3d41e-149">En Retail Modern POS-database fungerer på Microsoft SQL Server 2012 med Service Pack 3 eller nyere, Microsoft SQL Server 2014 med Service Pack 2 eller nyere og Microsoft SQL Server 2016.</span><span class="sxs-lookup"><span data-stu-id="3d41e-149">A Retail Modern POS offline database will work on Microsoft SQL Server 2012 with Service Pack 3 or later, Microsoft SQL Server 2014 with Service Pack 2 or later, and Microsoft SQL Server 2016.</span></span> <span data-ttu-id="3d41e-150">Det anbefales, at du altid bruger den nyeste version, der er tilgængelig, og at du installerer alle de nyeste service packs.</span><span class="sxs-lookup"><span data-stu-id="3d41e-150">We recommend that you always use the latest version that is available, and that you install all the latest service packs.</span></span>

### <a name="supported-operating-systems"></a><span data-ttu-id="3d41e-151">Understøttede operativsystemer</span><span class="sxs-lookup"><span data-stu-id="3d41e-151">Supported operating systems</span></span>

-   <span data-ttu-id="3d41e-152">Retail Modern POS er et 32-bit-program, men det kan køre på både x86- og x64-arkitekturer.</span><span class="sxs-lookup"><span data-stu-id="3d41e-152">Retail Modern POS is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="3d41e-153">Retail Modern POS understøttes kun på udgaverne Windows 10 Pro, Enterprise og Enterprise Long Term Servicing Branch (LTSB).</span><span class="sxs-lookup"><span data-stu-id="3d41e-153">Retail Modern POS is supported only on Windows 10 Pro, Enterprise, and Enterprise Long Term Servicing Branch (LTSB) editions.</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="3d41e-154">Minimumssystemkrav</span><span class="sxs-lookup"><span data-stu-id="3d41e-154">Minimum system requirements</span></span>

-   <span data-ttu-id="3d41e-155">Den mindste understøttede opløsning er 1280 × 1024.</span><span class="sxs-lookup"><span data-stu-id="3d41e-155">The minimum supported resolution is 1,280 × 1,024.</span></span>
-   <span data-ttu-id="3d41e-156">Den computer, der kører Retail Modern POS, skal opfylde følgende krav:</span><span class="sxs-lookup"><span data-stu-id="3d41e-156">The computer that Retail Modern POS runs on must meet these requirements:</span></span>

    -   <span data-ttu-id="3d41e-157">Den skal som minimum have en dual core-processor, der ikke kører mindre end 2 gigahertz (GHz).</span><span class="sxs-lookup"><span data-stu-id="3d41e-157">It must have, at a minimum, a dual-core processor that runs at no less than 2 gigahertz (GHz).</span></span>
    -   <span data-ttu-id="3d41e-158">Den skal minimum have 3 GB (gigabyte) RAM (random-access memory).</span><span class="sxs-lookup"><span data-stu-id="3d41e-158">It must have, at a minimum, 3 gigabytes (GB) of random-access memory (RAM).</span></span>
    -   <span data-ttu-id="3d41e-159">Den skal have adgang til internettet.</span><span class="sxs-lookup"><span data-stu-id="3d41e-159">It must have internet access.</span></span>

## <a name="retail-hardware-station-requirements"></a><span data-ttu-id="3d41e-160">Krav til Retail hardware station</span><span class="sxs-lookup"><span data-stu-id="3d41e-160">Retail hardware station requirements</span></span>
### <a name="supported-operating-systems"></a><span data-ttu-id="3d41e-161">Understøttede operativsystemer</span><span class="sxs-lookup"><span data-stu-id="3d41e-161">Supported operating systems</span></span>

-   <span data-ttu-id="3d41e-162">Retail hardware station er et 32-bit-program, men det kan køre på både x86- og x64-arkitekturer.</span><span class="sxs-lookup"><span data-stu-id="3d41e-162">Retail hardware station is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="3d41e-163">Retail hardware station understøttes på følgende operativsystemer:</span><span class="sxs-lookup"><span data-stu-id="3d41e-163">Retail hardware station is supported on the following operating systems:</span></span>

    -   <span data-ttu-id="3d41e-164">Windows 7 Professional-, Enterprise- og Ultimate-udgaverne</span><span class="sxs-lookup"><span data-stu-id="3d41e-164">Windows 7 Professional, Enterprise, and Ultimate editions</span></span> 
    
        > [!NOTE]
        > <span data-ttu-id="3d41e-165">Windows 7 understøttes kun, hvis Internet Explorer 11 installeres manuelt på systemet.</span><span class="sxs-lookup"><span data-stu-id="3d41e-165">Windows 7 is supported only if Internet Explorer 11 is manually installed on the system.</span></span>

    -   <span data-ttu-id="3d41e-166">Windows 8.1 Update 1 Professional-, Enterprise- og Embedded-udgaverne</span><span class="sxs-lookup"><span data-stu-id="3d41e-166">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions</span></span>
    -   <span data-ttu-id="3d41e-167">Windows 10 Pro-, Enterprise- og Enterprise LTSB-udgaverne</span><span class="sxs-lookup"><span data-stu-id="3d41e-167">Windows 10 Pro, Enterprise, and Enterprise LTSB editions</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="3d41e-168">Minimumssystemkrav</span><span class="sxs-lookup"><span data-stu-id="3d41e-168">Minimum system requirements</span></span>

<span data-ttu-id="3d41e-169">Computeren skal opfylde alle systemkrav til installation og brug af følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="3d41e-169">The computer must meet all system requirements for installing and using the following items:</span></span>

-   <span data-ttu-id="3d41e-170">IIS (Internet Information Services)</span><span class="sxs-lookup"><span data-stu-id="3d41e-170">Internet Information Services (IIS)</span></span>
-   <span data-ttu-id="3d41e-171">Tredjepartshardware</span><span class="sxs-lookup"><span data-stu-id="3d41e-171">Third-party hardware</span></span>

## <a name="retail-store-scale-unit-requirements"></a><span data-ttu-id="3d41e-172">Krav til vægtenhed til detailbutikker</span><span class="sxs-lookup"><span data-stu-id="3d41e-172">Retail Store Scale Unit requirements</span></span>
### <a name="supported-operating-systems"></a><span data-ttu-id="3d41e-173">Understøttede operativsystemer</span><span class="sxs-lookup"><span data-stu-id="3d41e-173">Supported operating systems</span></span>

-   <span data-ttu-id="3d41e-174">Vægtenhed til detailbutikker er et 32-bit-program, men det kan køre på både x86- og x64-arkitekturer.</span><span class="sxs-lookup"><span data-stu-id="3d41e-174">Retail Store Scale Unit is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="3d41e-175">Vægtenhed til detailbutikker understøttes på følgende operativsystemer:</span><span class="sxs-lookup"><span data-stu-id="3d41e-175">Retail Store Scale Unit is supported on the following operating systems:</span></span>

    -   <span data-ttu-id="3d41e-176">Windows 7 Professional-, Enterprise- og Ultimate-udgaverne</span><span class="sxs-lookup"><span data-stu-id="3d41e-176">Windows 7 Professional, Enterprise, and Ultimate editions</span></span>
    -   <span data-ttu-id="3d41e-177">Windows 8.1 Update 1 Professional-, Enterprise- og Embedded-udgaverne</span><span class="sxs-lookup"><span data-stu-id="3d41e-177">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions</span></span>
    -   <span data-ttu-id="3d41e-178">Windows 10 Pro-, Enterprise- og Enterprise LTSB-udgaverne</span><span class="sxs-lookup"><span data-stu-id="3d41e-178">Windows 10 Pro, Enterprise, and Enterprise LTSB editions</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="3d41e-179">Minimumssystemkrav</span><span class="sxs-lookup"><span data-stu-id="3d41e-179">Minimum system requirements</span></span>

-   <span data-ttu-id="3d41e-180">4 GB RAM</span><span class="sxs-lookup"><span data-stu-id="3d41e-180">4 GB of RAM</span></span>
-   <span data-ttu-id="3d41e-181">1,6 GHz spidsbelastnings CPU-hastighed pr. processorkerne (to kerner er minimum).</span><span class="sxs-lookup"><span data-stu-id="3d41e-181">1.6 GHz peak CPU speed per core (Two cores are the minimum.)</span></span>
-   <span data-ttu-id="3d41e-182">Mindst 10 GB ledig plads (kanaldatabasen kan kræve en stor mængde plads.)</span><span class="sxs-lookup"><span data-stu-id="3d41e-182">At least 10 GB of free space (The channel database can require a large amount of space.)</span></span>

### <a name="recommended-system-requirements"></a><span data-ttu-id="3d41e-183">Anbefalede systemkrav</span><span class="sxs-lookup"><span data-stu-id="3d41e-183">Recommended system requirements</span></span>

-   <span data-ttu-id="3d41e-184">6 GB RAM</span><span class="sxs-lookup"><span data-stu-id="3d41e-184">6 GB of RAM</span></span>
-   <span data-ttu-id="3d41e-185">2,4 GHz i7 (eller tilsvarende) top CPU-hastighed pr. processorkerne (fire kerner anbefales.)</span><span class="sxs-lookup"><span data-stu-id="3d41e-185">2.4 GHz i7 (or equivalent) peak CPU speed per core (Four cores are recommended.)</span></span>
-   <span data-ttu-id="3d41e-186">Mindst 10 GB ledig plads (kanaldatabasen kan kræve en stor mængde plads.)</span><span class="sxs-lookup"><span data-stu-id="3d41e-186">At least 10 GB of free space (The channel database can require a large amount of space.)</span></span>

## <a name="connector-requirements"></a><span data-ttu-id="3d41e-187">Krav til Connector</span><span class="sxs-lookup"><span data-stu-id="3d41e-187">Connector requirements</span></span>
### <a name="supported-operating-systems"></a><span data-ttu-id="3d41e-188">Understøttede operativsystemer</span><span class="sxs-lookup"><span data-stu-id="3d41e-188">Supported operating systems</span></span>

-   <span data-ttu-id="3d41e-189">Connector til Microsoft Dynamics AX har to separate installationsprogrammer, et til Async Server Connector-tjenesten og et til Real-time service for Dynamics AX 2012 R3.</span><span class="sxs-lookup"><span data-stu-id="3d41e-189">The Connector for Microsoft Dynamics AX has two separate installers, one for Async Server Connector service and one for Real-time service for Dynamics AX 2012 R3.</span></span>
-   <span data-ttu-id="3d41e-190">Begge komponenter er et 32-bit-program, men de kan køre på både x86- og x64-arkitekturer.</span><span class="sxs-lookup"><span data-stu-id="3d41e-190">Both components are 32-bit applications, but they will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="3d41e-191">Begge komponenter understøttes på følgende operativsystemer:</span><span class="sxs-lookup"><span data-stu-id="3d41e-191">Both components are supported on the following operating systems:</span></span>

    -   <span data-ttu-id="3d41e-192">Windows 7 Professional-, Enterprise- og Ultimate-udgaverne</span><span class="sxs-lookup"><span data-stu-id="3d41e-192">Windows 7 Professional, Enterprise, and Ultimate editions</span></span>
    -   <span data-ttu-id="3d41e-193">Windows 8.1 Update 1 Professional-, Enterprise- og Embedded-udgaverne</span><span class="sxs-lookup"><span data-stu-id="3d41e-193">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions</span></span>
    -   <span data-ttu-id="3d41e-194">Windows 10 Pro-, Enterprise- og Enterprise LTSB-udgaverne</span><span class="sxs-lookup"><span data-stu-id="3d41e-194">Windows 10 Pro, Enterprise, and Enterprise LTSB editions</span></span>
    -   <span data-ttu-id="3d41e-195">Microsoft Windows Server 2012 R2 og Microsoft Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3d41e-195">Microsoft Windows Server 2012 R2 and Microsoft Windows Server 2016</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="3d41e-196">Minimumssystemkrav</span><span class="sxs-lookup"><span data-stu-id="3d41e-196">Minimum system requirements</span></span>
-   <span data-ttu-id="3d41e-197">2 GB RAM (4 GB RAM anbefales).</span><span class="sxs-lookup"><span data-stu-id="3d41e-197">2 GB of RAM (4 GB of RAM are recommended.)</span></span>
-   <span data-ttu-id="3d41e-198">1,6 GHz spidsbelastnings CPU-hastighed pr. processorkerne (to kerner er minimum).</span><span class="sxs-lookup"><span data-stu-id="3d41e-198">1.6 GHz peak CPU speed per core (Two cores are the minimum.)</span></span>
-   <span data-ttu-id="3d41e-199">Mindst 10 GB ledig plads (kanaldatabasen kan kræve en stor mængde plads.)</span><span class="sxs-lookup"><span data-stu-id="3d41e-199">At least 10 GB of free space (The channel database can require a large amount of space.)</span></span>

## <a name="requirements-for-development-on-local-vms"></a><span data-ttu-id="3d41e-200">Krav til udvikling på lokale virtuelle maskiner</span><span class="sxs-lookup"><span data-stu-id="3d41e-200">Requirements for development on local VMs</span></span>
<span data-ttu-id="3d41e-201">Du kan finde oplysninger om kravene til udvikling på lokale virtuelle maskiner (VM'er), [VM, der kører i det lokale miljø](../../dev-itpro/dev-tools/access-instances.md).</span><span class="sxs-lookup"><span data-stu-id="3d41e-201">For information about the requirements for development on local virtual machines (VMs), see [VM running on-premises](../../dev-itpro/dev-tools/access-instances.md).</span></span>


## <a name="see-also"></a><span data-ttu-id="3d41e-202">Se også</span><span class="sxs-lookup"><span data-stu-id="3d41e-202">See also</span></span>

[<span data-ttu-id="3d41e-203">Få en evalueringskopi af Dynamics 365 for Finance and Operations, Enterprise edition</span><span class="sxs-lookup"><span data-stu-id="3d41e-203">Get an evaluation copy of Dynamics 365 for Finance and Operations, Enterprise edition</span></span>](../../dev-itpro/dev-tools/get-evaluation-copy.md)

