---
title: Systemkrav for Talent
description: I dette emne beskrives kravene til Dynamics 365 Talent.
author: andreabichsel
manager: AnnBe
ms.date: 10/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 509827d5736887f56e7754a0760af7dea76277f7
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2020
ms.locfileid: "3006049"
---
# <a name="talent-system-requirements"></a><span data-ttu-id="db606-103">Systemkrav for Talent</span><span class="sxs-lookup"><span data-stu-id="db606-103">Talent system requirements</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="db606-104">Dette emne indeholder beskrivelser af kravene til Microsoft Dynamics 365 Talent, herunder Attract og Onboard.</span><span class="sxs-lookup"><span data-stu-id="db606-104">This topic describes requirements for Microsoft Dynamics 365 Talent, including Attract and Onboard.</span></span> <span data-ttu-id="db606-105">Den beskriver også de lande og områder, hvor Talent er tilgængelig, samt oplysninger om sprog og lokalisering for Talent-data.</span><span class="sxs-lookup"><span data-stu-id="db606-105">It also outlines the countries and regions where Talent is available, plus information about languages and localization for Talent data.</span></span> <span data-ttu-id="db606-106">I tilføjelser indeholder dette emne opdateringspolitikken for Talent.</span><span class="sxs-lookup"><span data-stu-id="db606-106">In additions, this topic provides the update policy for Talent.</span></span>

## <a name="supported-web-browsers"></a><span data-ttu-id="db606-107">Understøttede webbrowsere</span><span class="sxs-lookup"><span data-stu-id="db606-107">Supported web browsers</span></span>

<span data-ttu-id="db606-108">Microsoft Dynamics 365 Talent kan køre i en af følgende webbrowsere, der kører på de angivne operativsystemer:</span><span class="sxs-lookup"><span data-stu-id="db606-108">Microsoft Dynamics 365 Talent can run in any of the following web browsers that run on the specified operating systems:</span></span> 

*   <span data-ttu-id="db606-109">Microsoft Edge (nyeste offentligt tilgængelige version) på Windows 10</span><span class="sxs-lookup"><span data-stu-id="db606-109">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
*   <span data-ttu-id="db606-110">Internet Explorer 11 på Windows 10, Windows 8.1 eller Windows 7</span><span class="sxs-lookup"><span data-stu-id="db606-110">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
*   <span data-ttu-id="db606-111">Google Chrome (nyeste offentligt tilgængelige version)</span><span class="sxs-lookup"><span data-stu-id="db606-111">Google Chrome (latest publicly available version)</span></span>
*   <span data-ttu-id="db606-112">Apple Safari (nyeste offentligt tilgængelige version)</span><span class="sxs-lookup"><span data-stu-id="db606-112">Apple Safari (latest publicly available version)</span></span>

<span data-ttu-id="db606-113">Gå til producentens websted for at finde den nyeste version af hver webbrowser.</span><span class="sxs-lookup"><span data-stu-id="db606-113">To find the latest release for each web browser, go to the software manufacturer’s website.</span></span> 

> [!NOTE]
> * <span data-ttu-id="db606-114">Hvis du vil hente billeder, der er genereret ud fra Arbejdsrutineoptager og inkludere dem i Microsoft Word-dokumenter, skal du have en Chrome-udvidelse installeret.</span><span class="sxs-lookup"><span data-stu-id="db606-114">To capture images that are generated from Task Recorder and include them in Microsoft Word documents, you must have a Chrome extension installed.</span></span> 
> * <span data-ttu-id="db606-115">Arbejdsgangseditoren startes som et ClickOnce-program.</span><span class="sxs-lookup"><span data-stu-id="db606-115">The Workflow Editor is started as a ClickOnce application.</span></span> <span data-ttu-id="db606-116">Kun Microsoft Edge og Internet Explorer (på en understøttet version af Microsoft Windows) understøtter ClickOnce-programmer.</span><span class="sxs-lookup"><span data-stu-id="db606-116">Only Microsoft Edge and Internet Explorer (on a supported version of Microsoft Windows) support ClickOnce applications.</span></span> <span data-ttu-id="db606-117">ClickOnce-programmet til arbejdsgangseditoren kræver et kompatibelt 64-bit-operativsystem.</span><span class="sxs-lookup"><span data-stu-id="db606-117">The Workflow Editor ClickOnce application requires a 64-bit compatible operating system.</span></span>
> * <span data-ttu-id="db606-118">Hvis du vil se PDF-filer, anbefaler vi, at du bruger moderne browsere, som Microsoft Edge (seneste offentligt tilgængelige version) i Windows 10 eller Google Chrome (seneste offentligt tilgængelige version) i Windows 10, Windows 8.1, Windows 8, Windows 7 eller Google Nexus 10-tabletten.</span><span class="sxs-lookup"><span data-stu-id="db606-118">To preview PDF files, we recommend that you use modern browsers like Microsoft Edge (latest publicly available version) on Windows 10, or Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet.</span></span>
>   <span data-ttu-id="db606-119">Netværkskrav</span><span class="sxs-lookup"><span data-stu-id="db606-119">Network requirements</span></span>
> * <span data-ttu-id="db606-120">Dynamics 365 Talent er designet til netværk med ventetid på 250-300 millisekunder (ms) eller mindre.</span><span class="sxs-lookup"><span data-stu-id="db606-120">Dynamics 365 Talent is designed for networks with latency of 250-300 milliseconds (ms) or less.</span></span> <span data-ttu-id="db606-121">Dette er ventetiden fra en browserklient til Microsoft Azure-datacenteret, der er vært for Talent.</span><span class="sxs-lookup"><span data-stu-id="db606-121">This is the latency from a browser client to the Microsoft Azure data center that hosts Talent.</span></span> <span data-ttu-id="db606-122">Vi anbefaler, at du tester netværksventetiden på [www.azurespeed.com](https://www.azurespeed.com "Test af ventetid i Azure").</span><span class="sxs-lookup"><span data-stu-id="db606-122">We recommend that you test network latency at [www.azurespeed.com](https://www.azurespeed.com "Azure Latency Test").</span></span>
> * <span data-ttu-id="db606-123">Kravene til båndbredde for Talent afhænger af dit scenarie.</span><span class="sxs-lookup"><span data-stu-id="db606-123">Bandwidth requirements for Talent depend on your scenario.</span></span> <span data-ttu-id="db606-124">De fleste typiske scenarier kræver en båndbredde på mere end 50 kilobyte pr. sekund (KBps).</span><span class="sxs-lookup"><span data-stu-id="db606-124">Most typical scenarios require a bandwidth of more than 50 kilobytes per second (KBps).</span></span>
> 
> [!WARNING]
> <span data-ttu-id="db606-125">Du må ikke beregne kravene til båndbredde fra en klientlokalitet ved at multiplicere antallet af brugere med minimumkravene til båndbredde.</span><span class="sxs-lookup"><span data-stu-id="db606-125">Don't compute bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="db606-126">Den samtidig brug af en given lokalitet er meget vanskeligt at beregne.</span><span class="sxs-lookup"><span data-stu-id="db606-126">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="db606-127">Til kunder, der er bekymret over kravene til båndbredde, kan du bruge en prøveversion af Talent.</span><span class="sxs-lookup"><span data-stu-id="db606-127">For customers who are concerned about bandwidth requirements, use a trial version of Talent.</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="db606-128">Understøttede Microsoft Office-applikationer</span><span class="sxs-lookup"><span data-stu-id="db606-128">Supported Microsoft Office applications</span></span>

* <span data-ttu-id="db606-129">Hvis du vil køre tilføjelsesprogrammer til Microsoft Excel og Word, skal du have Microsoft Office 2016 til Windows eller Mac installeret.</span><span class="sxs-lookup"><span data-stu-id="db606-129">To run the Microsoft Excel and Word add-ins, you must have Microsoft Office 2016 for Windows or Mac installed.</span></span> <span data-ttu-id="db606-130">Du kan finde yderligere oplysninger om versionskrav i [Fejlfinding af Office-integration](../dev-itpro/office-integration/office-integration-troubleshooting.md "Fejlfinding af Office-integration").</span><span class="sxs-lookup"><span data-stu-id="db606-130">For more details about version requirements, see [Office integration troubleshooting](../dev-itpro/office-integration/office-integration-troubleshooting.md "Office integration troubleshooting").</span></span>
* <span data-ttu-id="db606-131">Hvis du vil have vist dokumenter, der er genereret med funktionerne Eksport til Excel eller Eksport til Word, skal have Microsoft Office 2007 eller nyere installeret.</span><span class="sxs-lookup"><span data-stu-id="db606-131">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="regional-availability-languages-and-localization"></a><span data-ttu-id="db606-132">Regional tilgængelighed, sprog og lokalisering</span><span class="sxs-lookup"><span data-stu-id="db606-132">Regional availability, languages, and localization</span></span>

<span data-ttu-id="db606-133">Du kan hente en PDF-fil over de lande, regioner og sprog, som Talent understøtter i [International tilgængelighed af Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/get-started/availability).</span><span class="sxs-lookup"><span data-stu-id="db606-133">You can download a PDF file of the countries, regions, and languages Talent supports at [International availability of Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/get-started/availability).</span></span> 

> [!NOTE]
> <span data-ttu-id="db606-134">Mens brugergrænsefladen er lokaliseret til andre sprog, gemmes alle brugerdata på det sprog, de blev indtastet på.</span><span class="sxs-lookup"><span data-stu-id="db606-134">While the user interface is localized into other languages, all user data is stored in the language in which it was entered.</span></span> <span data-ttu-id="db606-135">Du kan oprette mails og skabeloner på andre sprog, men data som f.eks. planlægningsoplysninger, er kun tilgængelige på engelsk på nuværende tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="db606-135">You can create emails and templates in other languages, but data such as scheduling information is only available in English at this time.</span></span>

<span data-ttu-id="db606-136">Hvis du er udvikler, der er interesseret i at oprette lande- eller områdespecifikke tilpasninger, eller i at oprette en løsning for et land eller en region, der ikke understøttes af Microsoft, skal du se [Globalisering](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).</span><span class="sxs-lookup"><span data-stu-id="db606-136">If you're a developer interested in creating country- or region-specific customizations, or in creating a solution for a country or region not currently supported by Microsoft, see [Globalization](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).</span></span>

