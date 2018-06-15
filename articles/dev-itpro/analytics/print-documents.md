---
title: Udskrivning i Finance and Operations-programmer
description: "I Microsoft Dynamics 365 for Finance and Operations kan du udskrive dokumenter ved hjælp af enten en lokal printer eller en netværkstilsluttet enhed. Denne artikel indeholder en oversigt over, hvordan dokumenter udskrives."
author: TJVass
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: IT Pro, Application User
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.custom: 69161
ms.assetid: 7815bddd-c4f4-4bc3-a29b-315458065374
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: b1e6893eda35b7e4d863116edf2787685071bbc3
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---

# <a name="printing-in-finance-and-operations-applications"></a><span data-ttu-id="64fc9-104">Udskrivning i Finance and Operations-programmer</span><span class="sxs-lookup"><span data-stu-id="64fc9-104">Printing in Finance and Operations applications</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="64fc9-105">I Microsoft Dynamics 365 for Finance and Operations kan du udskrive dokumenter ved hjælp af enten en lokal printer eller en netværkstilsluttet enhed.</span><span class="sxs-lookup"><span data-stu-id="64fc9-105">In Microsoft Dynamics 365 for Finance and Operations, you can print documents by using either a local printer or a network-connected device.</span></span> <span data-ttu-id="64fc9-106">Denne artikel indeholder en oversigt over, hvordan dokumenter udskrives.</span><span class="sxs-lookup"><span data-stu-id="64fc9-106">This article provides an overview of how documents are printed.</span></span>

<a name="printing-overview"></a><span data-ttu-id="64fc9-107">Oversigt over udskrivning</span><span class="sxs-lookup"><span data-stu-id="64fc9-107">Printing overview</span></span>
-----------------

<span data-ttu-id="64fc9-108">Microsoft Dynamics 365 for Finance and Operations indeholder integrerede tjenester og klientapplikationer, der gør det nemt at oprette, gemme og distribuere dokumenter, der understøtter forretningsaktiviteter.</span><span class="sxs-lookup"><span data-stu-id="64fc9-108">Microsoft Dynamics 365 for Finance and Operations provides integrated services and client applications that make it easy to generate, store, and distribute documents that support business activity.</span></span> <span data-ttu-id="64fc9-109">I Finance and Operations kan du udskrive dokumenter ved hjælp af enten en lokal printer eller en netværkstilsluttet enhed.</span><span class="sxs-lookup"><span data-stu-id="64fc9-109">In Finance and Operations, you can print documents by using either a local printer or a network-connected device.</span></span> <span data-ttu-id="64fc9-110">Derudover kan du eksportere sider og rapporter i Finance and Operations direkte fra klienten som PDF-filer eller Microsoft Office-dokumenter.</span><span class="sxs-lookup"><span data-stu-id="64fc9-110">In addition, you can export Finance and Operations pages and reports directly from the client, as PDF files or Microsoft Office documents.</span></span> <span data-ttu-id="64fc9-111">Endelig tillader den distribuerede arbejdsbyrde, at du udskriver forretningsdokumenter direkte fra en mobilenhed ved hjælp af netværksressourcer.</span><span class="sxs-lookup"><span data-stu-id="64fc9-111">Finally, the distributed workload lets you print business documents directly from a mobile device by using network resources.</span></span> <span data-ttu-id="64fc9-112">Selvom udskrivningsbehov kan variere, skal alle brancher typisk oprette udskrifter af forretningsdokumenter ved hjælp af Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="64fc9-112">Although printing requirements might vary, all industries typically must create hard copies of business documents by using Finance and Operations.</span></span> <span data-ttu-id="64fc9-113">Udskrivning af dokumenter på netværksenheder fra tilknyttede programmer medfører en særlig række af udfordringer.</span><span class="sxs-lookup"><span data-stu-id="64fc9-113">Printing documents on network devices from hosted applications presents a unique set of challenges.</span></span> <span data-ttu-id="64fc9-114">Her er nogle eksempler:</span><span class="sxs-lookup"><span data-stu-id="64fc9-114">Here are some examples:</span></span>

-   <span data-ttu-id="64fc9-115">Printerdrivere er muligvis ikke tilgængelige på brugerens enhed.</span><span class="sxs-lookup"><span data-stu-id="64fc9-115">Print drivers might not be available on the user's device.</span></span>
-   <span data-ttu-id="64fc9-116">Brugerens enhed er muligvis ikke tilsluttet virksomhedens netværk.</span><span class="sxs-lookup"><span data-stu-id="64fc9-116">The user’s device might not be connected to the corporate network.</span></span>

<span data-ttu-id="64fc9-117">Systemadministratorer kan konfigurere installationer ved at bruge en dedikeret vært og følge nogle få nemme trin, så brugerne kan udskrive direkte fra forretningsprogrammer på netværksenheder.</span><span class="sxs-lookup"><span data-stu-id="64fc9-117">By using a dedicated host and following a few easy steps, system administrators can configure deployments so that users can print directly from business applications on network devices.</span></span>

### <a name="printing-scenarios-in-finance-and-operations-applications"></a><span data-ttu-id="64fc9-118">Udskrivningsscenarier i Finance and Operations-programmer</span><span class="sxs-lookup"><span data-stu-id="64fc9-118">Printing scenarios in Finance and Operations applications</span></span>

<span data-ttu-id="64fc9-119">I følgende tabel beskrives de tre primære udskrivningsscenarier i Finance and Operations-programmer.</span><span class="sxs-lookup"><span data-stu-id="64fc9-119">The following table describes the three primary printing scenarios in Finance and Operations applications.</span></span>

| <span data-ttu-id="64fc9-120">Scenario</span><span class="sxs-lookup"><span data-stu-id="64fc9-120">Scenario</span></span>                        | <span data-ttu-id="64fc9-121">Mål</span><span class="sxs-lookup"><span data-stu-id="64fc9-121">Goal</span></span>                                                      | <span data-ttu-id="64fc9-122">Løsning</span><span class="sxs-lookup"><span data-stu-id="64fc9-122">Solution</span></span>                                                                                                            |
|---------------------------------|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64fc9-123">1. Udskrivning af det, du kan se</span><span class="sxs-lookup"><span data-stu-id="64fc9-123">1. Printing what you see</span></span>        | <span data-ttu-id="64fc9-124">Udskriv det, der aktuelt vises i browseren.</span><span class="sxs-lookup"><span data-stu-id="64fc9-124">Print what is currently shown in the browser.</span></span>             | <span data-ttu-id="64fc9-125">Der genereres en "udskriftsvenlig" version af websiden i browseren.</span><span class="sxs-lookup"><span data-stu-id="64fc9-125">A “print-friendly” version of the webpage is generated for the browser.</span></span>                                             |
| <span data-ttu-id="64fc9-126">2. Interaktiv udskrivning</span><span class="sxs-lookup"><span data-stu-id="64fc9-126">2. Interactive printing</span></span>         | <span data-ttu-id="64fc9-127">Udskriv et dokument med høj præcision på en lokalt tilsluttet enhed.</span><span class="sxs-lookup"><span data-stu-id="64fc9-127">Print a precision document on a locally connected device.</span></span> | <span data-ttu-id="64fc9-128">Du kan eksportere en PDF-version af rapporten og åbne den i browseren.</span><span class="sxs-lookup"><span data-stu-id="64fc9-128">You can export a PDF version of the report and download it to the browser.</span></span>                                          |
| <span data-ttu-id="64fc9-129">3. Udskrivning på en netværksenhed</span><span class="sxs-lookup"><span data-stu-id="64fc9-129">3. Printing on a network device</span></span> | <span data-ttu-id="64fc9-130">Send et dokument med høj præcision til en printerenhed for et domæne.</span><span class="sxs-lookup"><span data-stu-id="64fc9-130">Send a precision document to a domain printer device.</span></span>     | <span data-ttu-id="64fc9-131">Et præcisiondokument sendes til et klientprogram, der kører på en server, der er tilknyttet kundens domæne.</span><span class="sxs-lookup"><span data-stu-id="64fc9-131">A precision document is sent to a client application that runs on a server that is hosted in the customer’s domain.</span></span> |

<span data-ttu-id="64fc9-132">Eftersom løsningen varierer afhængigt af scenariet, tilbyder Finance and Opersations-programmer indbyggede tjenester og værktøjer, der hjælper brugerne med at opfylde deres mål:</span><span class="sxs-lookup"><span data-stu-id="64fc9-132">Because the solution varies, depending on the scenario, Finance and Operations applications provide built-in services and tooling to help users accomplish their goals:</span></span>

-   <span data-ttu-id="64fc9-133">**Eksempel 1** understøttes af browserens gengivelse af HTML5-klienten.</span><span class="sxs-lookup"><span data-stu-id="64fc9-133">**Scenario 1** is supported by the browser’s rendering of the HTML5 client.</span></span>
-   <span data-ttu-id="64fc9-134">**Eksempel 2** bruger klientprogrammer og Microsoft Office 365-tjenester.</span><span class="sxs-lookup"><span data-stu-id="64fc9-134">**Scenario 2** uses client applications and Microsoft Office 365 services.</span></span>
-   <span data-ttu-id="64fc9-135">**Eksempel 3** kræver understøttelse fra klientprogrammer og tjenester, der er tilknyttet Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="64fc9-135">**Scenario 3** requires support from client applications and from services that are hosted in Microsoft Azure.</span></span>

<span data-ttu-id="64fc9-136">Ud over den platform, der er installeret under Azure-abonnementet, giver Finance and Opersations-programmer kunderne et integreret, oprindeligt Azure-program, der gør det lettere at bruge domænetilknyttede enheder til at udskrive dokumenter.</span><span class="sxs-lookup"><span data-stu-id="64fc9-136">In addition to the platform that is deployed to the Azure subscription, Finance and Operations applications provide customers with an integrated, first-party Azure application that helps them more easily use domain-hosted devices to print documents.</span></span>

## <a name="service-overview"></a><span data-ttu-id="64fc9-137">Serviceoversigt</span><span class="sxs-lookup"><span data-stu-id="64fc9-137">Service overview</span></span>
<span data-ttu-id="64fc9-138">Mens dokumenter, der fremstilles af de tilknyttede programmer, venter på at blive udskrevet på en netværkstilsluttet enhed, gemmes de i blob-lageret for Azure.</span><span class="sxs-lookup"><span data-stu-id="64fc9-138">While documents that are produced by the hosted applications are waiting to be printed on a network-connected device, they are stored in Azure blob storage.</span></span> <span data-ttu-id="64fc9-139">[Dokumentets ruteplanlægningsagent](install-document-routing-agent.md) bruger Azure-godkendelse til at oprette en sikker kanal for Azure-tjenesterne.</span><span class="sxs-lookup"><span data-stu-id="64fc9-139">The [Document Routing Agent](install-document-routing-agent.md) uses Azure authentication to establish a secure channel to the Azure services.</span></span> <span data-ttu-id="64fc9-140">**Udførelsessekvens**</span><span class="sxs-lookup"><span data-stu-id="64fc9-140">**Execution sequence**</span></span>

1.  <span data-ttu-id="64fc9-141">Rapporten oprettes af Microsoft SQL Server Reporting Services (SSRS) og gemmes i blob-lageret for Azure.</span><span class="sxs-lookup"><span data-stu-id="64fc9-141">The report is generated by Microsoft SQL Server Reporting Services (SSRS) and stored in Azure blob storage.</span></span> <span data-ttu-id="64fc9-142">Tilknyttede printerindstillinger gemmes sammen med dokumentet.</span><span class="sxs-lookup"><span data-stu-id="64fc9-142">Attached printer settings are stored together with the document.</span></span>
2.  <span data-ttu-id="64fc9-143">Dokumentets ruteplanlægningsagent forespørger Azure Service Bus-køen om aktive job.</span><span class="sxs-lookup"><span data-stu-id="64fc9-143">The Document Routing Agent queries the Azure Service Bus queue for active jobs.</span></span>
3.  <span data-ttu-id="64fc9-144">Dokumentet hentes af dokumentruteplanlægningsagent og sættes i kø til netværksprinteren.</span><span class="sxs-lookup"><span data-stu-id="64fc9-144">The document is downloaded by the Document Routing Agent and spooled to the network printer.</span></span>

<span data-ttu-id="64fc9-145">Den klientbaserede løsning lader kunder styre omfanget af deres udskrivningsbehov.</span><span class="sxs-lookup"><span data-stu-id="64fc9-145">The client-based solution lets customers manage the scale of their printing needs.</span></span> <span data-ttu-id="64fc9-146">Kunder med omfattende udskrivningsbehov kan installere flere dokumentruteplanlægningsagenter for at øge antallet af samtidige udskrivningshandlinger.</span><span class="sxs-lookup"><span data-stu-id="64fc9-146">Customers who have heavy-volume printing workloads can install many Document Routing Agents to increase the number of concurrent printing operations.</span></span> <span data-ttu-id="64fc9-147">Du kan også kræve nogle kunder meget få installationer af dokumentruteplanlægningsagent til at håndtere deres forventede behov for udskrivning.</span><span class="sxs-lookup"><span data-stu-id="64fc9-147">Alternatively, some customers require very few installations of the Document Routing Agent to handle their anticipated printing needs.</span></span>

### <a name="service-components-for-network-printing"></a><span data-ttu-id="64fc9-148">Servicekomponenter til netværksudskrivning</span><span class="sxs-lookup"><span data-stu-id="64fc9-148">Service components for network printing</span></span>

<span data-ttu-id="64fc9-149">Følgende diagram viser de grundlæggende komponenter, der kan understøtte netværksudskrivning.</span><span class="sxs-lookup"><span data-stu-id="64fc9-149">The following diagram shows the basic components that help support network printing operations.</span></span> <span data-ttu-id="64fc9-150">[![servicekomponenter-til-netværksudskrivning\_2016](./media/service-components-for-network-printing_2016.png)](./media/service-components-for-network-printing_2016.png) Bemærk, at en enkelt printer kan registreres med flere dokumentruteplanlægningsagenter.</span><span class="sxs-lookup"><span data-stu-id="64fc9-150">[![service-components-for-network-printing\_2016](./media/service-components-for-network-printing_2016.png)](./media/service-components-for-network-printing_2016.png) Note that a single printer can be registered with multiple Document Routing Agents.</span></span> <span data-ttu-id="64fc9-151">For at håndtere printerindstillingerne bruger den hostede tjeneste netværksstien, der entydigt identificerer hver netværksprinter.</span><span class="sxs-lookup"><span data-stu-id="64fc9-151">To resolve the printer preferences, the hosted service uses the network path that uniquely identifies every network printer.</span></span> <span data-ttu-id="64fc9-152">Når der registreres en printer af flere klienter, vises den således som et enkelt punkt på listen over printere, som er tilgængelige i Finance and Opersations-programmer.</span><span class="sxs-lookup"><span data-stu-id="64fc9-152">As a result, even when a printer is registered by multiple clients, it appears as a single selection in the list of printers available in Finance and Operations applications.</span></span>



