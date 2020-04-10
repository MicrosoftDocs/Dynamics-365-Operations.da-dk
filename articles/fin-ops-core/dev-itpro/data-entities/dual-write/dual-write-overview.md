---
title: Oversigt over dobbeltskrivning
description: Dette emne giver en oversigt over dobbeltskrivning. Dobbeltskrivning er en infrastruktur, der giver næsten realtidsinteraktion mellem Microsoft Dynamics 365 modelbaserede apps og Finance and Operations-apps.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 64626ebdd7fbad3d47a4b4c6bbc45bf3bc0c8277
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172778"
---
# <a name="dual-write-overview"></a><span data-ttu-id="9aac9-104">Oversigt over dobbeltskrivning</span><span class="sxs-lookup"><span data-stu-id="9aac9-104">Dual-write overview</span></span>

[!include [banner](../../includes/banner.md)]



## <a name="what-is-dual-write"></a><span data-ttu-id="9aac9-105">Hvad er dobbeltskrivning?</span><span class="sxs-lookup"><span data-stu-id="9aac9-105">What is dual-write?</span></span>

<span data-ttu-id="9aac9-106">Dobbeltskrivning er en brugsklar infrastruktur, der giver næsten realtidsinteraktion mellem modelbaserede apps i Microsoft Dynamics 365 og Finance and Operations-apps.</span><span class="sxs-lookup"><span data-stu-id="9aac9-106">Dual-write is an out-of-box infrastructure that provides near-real-time interaction between model-driven apps in Microsoft Dynamics 365 and Finance and Operations apps.</span></span> <span data-ttu-id="9aac9-107">Når data om kunder, produkter, personer og handlinger går ud over programgrænserne, styrkes alle afdelinger i en organisation.</span><span class="sxs-lookup"><span data-stu-id="9aac9-107">When data about customers, products, people, and operations flows beyond application boundaries, all departments in an organization are empowered.</span></span>

<span data-ttu-id="9aac9-108">Dobbeltskrivning giver en tæt kombineret, tovejsintegration mellem Finance and Operations-apps og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="9aac9-108">Dual-write provides tightly coupled, bidirectional integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="9aac9-109">Alle dataændringer i Finance and Operations-apps forårsager ændringer i Common Data Service, og alle dataændringer i Common Data Service medfører ændringer i Finance and Operations-apps.</span><span class="sxs-lookup"><span data-stu-id="9aac9-109">Any data change in Finance and Operations apps causes writes to Common Data Service, and any data change in Common Data Service causes writes to Finance and Operations apps.</span></span> <span data-ttu-id="9aac9-110">Dette automatiserede dataflow giver en integreret brugeroplevelse på tværs af apps.</span><span class="sxs-lookup"><span data-stu-id="9aac9-110">This automated data flow provides an integrated user experience across the apps.</span></span>

![Datarelation mellem apps](media/dual-write-overview.jpg)

<span data-ttu-id="9aac9-112">Dobbeltskrivning har to aspekter: et *infrastruktur*-aspekt og et *program*-aspekt.</span><span class="sxs-lookup"><span data-stu-id="9aac9-112">Dual-write has two aspects: an *infrastructure* aspect and an *application* aspect.</span></span>

### <a name="infrastructure"></a><span data-ttu-id="9aac9-113">Infrastruktur</span><span class="sxs-lookup"><span data-stu-id="9aac9-113">Infrastructure</span></span>

<span data-ttu-id="9aac9-114">Dobbeltskrivningsinfrastrukturen kan udvides og er pålidelig og indeholder følgende nøglefunktioner:</span><span class="sxs-lookup"><span data-stu-id="9aac9-114">The dual-write infrastructure is extensible and reliable, and includes the following key features:</span></span>

+ <span data-ttu-id="9aac9-115">Synkrone og tovejsdatastrømme mellem programmer</span><span class="sxs-lookup"><span data-stu-id="9aac9-115">Synchronous and bidirectional data flow between applications</span></span>
+ <span data-ttu-id="9aac9-116">Synkronisering sammen med kørsels-, pause- og catch-up-tilstande til at understøtte systemet i onlinetilstand samt offline/asynkron-tilstand.</span><span class="sxs-lookup"><span data-stu-id="9aac9-116">Synchronization, together with play, pause, and catchup modes to support the system during online and offline/asynchronous modes.</span></span>
+ <span data-ttu-id="9aac9-117">Mulighed for at synkronisere indledende data mellem programmerne</span><span class="sxs-lookup"><span data-stu-id="9aac9-117">Ability to sync initial data between the applications</span></span>
+ <span data-ttu-id="9aac9-118">Konsolideret visning af aktivitet og fejllogfiler for dataadministratorer</span><span class="sxs-lookup"><span data-stu-id="9aac9-118">Consolidated view of activity and error logs for data admins</span></span>
+ <span data-ttu-id="9aac9-119">Mulighed for at konfigurere brugerdefinerede påmindelser og tærskler og til at abonnere på beskeder</span><span class="sxs-lookup"><span data-stu-id="9aac9-119">Ability to configure custom alerts and thresholds, and to subscribe to notifications</span></span>
+ <span data-ttu-id="9aac9-120">Intuitiv brugergrænseflade (UI) til filtrering og transformationer</span><span class="sxs-lookup"><span data-stu-id="9aac9-120">Intuitive user interface (UI) for filtering and transformations</span></span>
+ <span data-ttu-id="9aac9-121">Mulighed for at angive og få vist enhedsafhængigheder og relationer</span><span class="sxs-lookup"><span data-stu-id="9aac9-121">Ability to set and view entity dependencies and relationships</span></span>
+ <span data-ttu-id="9aac9-122">Udvidelse til både standard- og brugerdefinerede enheder og kort</span><span class="sxs-lookup"><span data-stu-id="9aac9-122">Extensibility for both standard and custom entities and maps</span></span>
+ <span data-ttu-id="9aac9-123">Pålidelig administration af programlevetiden</span><span class="sxs-lookup"><span data-stu-id="9aac9-123">Reliable application lifecycle management</span></span>
+ <span data-ttu-id="9aac9-124">Brugsklar opsætningsoplevelse for nye kunder</span><span class="sxs-lookup"><span data-stu-id="9aac9-124">Out-of-box setup experience for new customers</span></span>

### <a name="application"></a><span data-ttu-id="9aac9-125">Applikation</span><span class="sxs-lookup"><span data-stu-id="9aac9-125">Application</span></span>

<span data-ttu-id="9aac9-126">Dobbeltskrivning opretter en tilknytning mellem koncepter i Finance and Operations-apps og koncepter i modelbaserede apps i Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="9aac9-126">Dual-write creates a mapping between concepts in Finance and Operations apps and concepts in model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="9aac9-127">Denne integration understøtter følgende scenarier:</span><span class="sxs-lookup"><span data-stu-id="9aac9-127">This integration supports the following scenarios:</span></span>

+ <span data-ttu-id="9aac9-128">Integreret kundemaster</span><span class="sxs-lookup"><span data-stu-id="9aac9-128">Integrated customer master</span></span>
+ <span data-ttu-id="9aac9-129">Adgang til kundefordelskundekort og belønningspoint</span><span class="sxs-lookup"><span data-stu-id="9aac9-129">Access to customer loyalty cards and reward points</span></span>
+ <span data-ttu-id="9aac9-130">Samlet produktmasteroplevelse</span><span class="sxs-lookup"><span data-stu-id="9aac9-130">Unified product mastering experience</span></span>
+ <span data-ttu-id="9aac9-131">Bevidsthed om organisationens hierarki</span><span class="sxs-lookup"><span data-stu-id="9aac9-131">Awareness of organization hierarchy</span></span>
+ <span data-ttu-id="9aac9-132">Integreret kreditormaster</span><span class="sxs-lookup"><span data-stu-id="9aac9-132">Integrated vendor master</span></span>
+ <span data-ttu-id="9aac9-133">Adgang til finansierings- og momsreferencedata</span><span class="sxs-lookup"><span data-stu-id="9aac9-133">Access to finance and tax reference data</span></span>
+ <span data-ttu-id="9aac9-134">Prisprogramoplevelse efter behov</span><span class="sxs-lookup"><span data-stu-id="9aac9-134">On-demand price engine experience</span></span>
+ <span data-ttu-id="9aac9-135">Integreret kundeemne-til-køb-oplevelse</span><span class="sxs-lookup"><span data-stu-id="9aac9-135">Integrated prospect-to-cash experience</span></span>
+ <span data-ttu-id="9aac9-136">Mulighed for at betjene både interne aktiver og kundeaktiver via feltagenter</span><span class="sxs-lookup"><span data-stu-id="9aac9-136">Ability to serve both in-house assets and customer assets through field agents</span></span>
+ <span data-ttu-id="9aac9-137">Integreret oplevelse fra indkøb til betaling</span><span class="sxs-lookup"><span data-stu-id="9aac9-137">Integrated procure-to-pay experience</span></span>
+ <span data-ttu-id="9aac9-138">Integrerede aktiviteter og notater til kundedata og -dokumenter</span><span class="sxs-lookup"><span data-stu-id="9aac9-138">Integrated activities and notes for customer data and documents</span></span>
+ <span data-ttu-id="9aac9-139">Mulighed for at slå disponibel lagertilgængelighed op og få detaljer herom</span><span class="sxs-lookup"><span data-stu-id="9aac9-139">Ability to look up on-hand inventory availability and details</span></span>
+ <span data-ttu-id="9aac9-140">Oplevelsen projekt til kontant</span><span class="sxs-lookup"><span data-stu-id="9aac9-140">Project-to-cash experience</span></span>
+ <span data-ttu-id="9aac9-141">Mulighed for at håndtere flere adresser og roller via partskonceptet</span><span class="sxs-lookup"><span data-stu-id="9aac9-141">Ability to handle multiple addresses and roles through the party concept</span></span>
+ <span data-ttu-id="9aac9-142">Enkel kildestyring til brugere</span><span class="sxs-lookup"><span data-stu-id="9aac9-142">Single source management for users</span></span>
+ <span data-ttu-id="9aac9-143">Integrerede kanaler til detailhandel og marketing</span><span class="sxs-lookup"><span data-stu-id="9aac9-143">Integrated channels for retailing and marketing</span></span>
+ <span data-ttu-id="9aac9-144">Synlighed i kampagner og rabatter</span><span class="sxs-lookup"><span data-stu-id="9aac9-144">Visibility into promotions and discounts</span></span>
+ <span data-ttu-id="9aac9-145">Funktioner for anmodning om tjenester</span><span class="sxs-lookup"><span data-stu-id="9aac9-145">Request-for-service functions</span></span>
+ <span data-ttu-id="9aac9-146">Integrerede tjenestehandlinger</span><span class="sxs-lookup"><span data-stu-id="9aac9-146">Streamlined service operations</span></span>

## <a name="top-reasons-to-use-dual-write"></a><span data-ttu-id="9aac9-147">De vigtigste grunde til at bruge dobbeltskrivning</span><span class="sxs-lookup"><span data-stu-id="9aac9-147">Top reasons to use dual-write</span></span>

<span data-ttu-id="9aac9-148">Dobbeltskrivning giver dataintegration på tværs af Microsoft Dynamics 365-programmer.</span><span class="sxs-lookup"><span data-stu-id="9aac9-148">Dual-write provides data integration across Microsoft Dynamics 365 applications.</span></span> <span data-ttu-id="9aac9-149">Denne solide rammer forbinder miljøer og giver forskellige virksomhedsprogrammer mulighed for at arbejde sammen.</span><span class="sxs-lookup"><span data-stu-id="9aac9-149">This robust framework links environments and enables different business applications to work together.</span></span> <span data-ttu-id="9aac9-150">Her er de vigtigste grunde til, at du skal bruge dobbeltskrivning:</span><span class="sxs-lookup"><span data-stu-id="9aac9-150">Here are the top reasons why you should use dual-write:</span></span>

+ <span data-ttu-id="9aac9-151">Dobbeltskrivning giver tæt kombineret, nær-realtidsintegration tovejsintegration mellem Finance and Operations-apps og modelbaserede apps i Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="9aac9-151">Dual-write provides tightly coupled, near-real-time, and bidirectional integration between Finance and Operations apps and model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="9aac9-152">Denne integration gør Microsoft Dynamics 365 til en fælles løsning for alle dine virksomhedsløsninger.</span><span class="sxs-lookup"><span data-stu-id="9aac9-152">This integration makes Microsoft Dynamics 365 the one-stop shop for all your business solutions.</span></span> <span data-ttu-id="9aac9-153">Kunder, der bruger Dynamics 365 Finance og Dynamics 365 Supply Chain Management, men som bruger løsninger fra andre leverandører end Microsoft til kunderelationsstyring (CRM), hælder mod Dynamics 365 for så vidt angår understøttelse af dobbeltskrivning.</span><span class="sxs-lookup"><span data-stu-id="9aac9-153">Customers who use Dynamics 365 Finance and Dynamics 365 Supply Chain Management, but who use non-Microsoft solutions for customer relationship management (CRM), are moving toward Dynamics 365 for its dual-write support.</span></span>
+ <span data-ttu-id="9aac9-154">Data fra kunder, produkter, handlinger, projekter og Tingenes internet flyder automatisk over til Common Data Service via dobbeltskrivning.</span><span class="sxs-lookup"><span data-stu-id="9aac9-154">Data from customers, products, operations, projects, and the Internet of Things (IoT) automatically flows to Common Data Service through dual-write.</span></span> <span data-ttu-id="9aac9-155">Denne forbindelse er meget anvendelig for virksomheder, der er interesserede i Microsoft Power Platform-udvidelser.</span><span class="sxs-lookup"><span data-stu-id="9aac9-155">This connection is very useful for businesses that are interested in Microsoft Power Platform expansions.</span></span>
+ <span data-ttu-id="9aac9-156">Infrastrukturen med dobbeltskrivninger følger princippet om ingen kode/lav kode.</span><span class="sxs-lookup"><span data-stu-id="9aac9-156">The dual-write infrastructure follows the no-code/low-code principle.</span></span> <span data-ttu-id="9aac9-157">Der kræves en minimal teknisk indsats for at udvide standard tabel-til-tabel-tilknytningerne og for at medtage brugerdefinerede kort.</span><span class="sxs-lookup"><span data-stu-id="9aac9-157">Minimal engineering effort is required to extend the standard table-to-table maps and to include custom maps.</span></span>
+ <span data-ttu-id="9aac9-158">Dobbeltskrivning understøtter både onlinetilstand og offlinetilstand.</span><span class="sxs-lookup"><span data-stu-id="9aac9-158">Dual-write supports both online mode and offline mode.</span></span> <span data-ttu-id="9aac9-159">Microsoft er det eneste firma, der tilbyder support til online- og offline-tilstand.</span><span class="sxs-lookup"><span data-stu-id="9aac9-159">Microsoft is the only company that offers support for online and offline modes.</span></span>

## <a name="what-does-dual-write-mean-for-users-and-architects-of-crm-products"></a><span data-ttu-id="9aac9-160">Hvad betyder dobbeltskrivning for brugere og arkitekter af CRM-produkter?</span><span class="sxs-lookup"><span data-stu-id="9aac9-160">What does dual-write mean for users and architects of CRM products?</span></span>

<span data-ttu-id="9aac9-161">Dobbeltskrivning automatiserer datastrømmen mellem Finance and Operations-apps og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="9aac9-161">Dual-write automates the data flow between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="9aac9-162">I fremtidige udgivelser vil koncepterne i modelbaserede apps i Dynamics 365 (f.eks. kunde, kontaktperson, tilbud og ordre) blive skaleret til mellemstore og større mellemstore kunder.</span><span class="sxs-lookup"><span data-stu-id="9aac9-162">In future releases, concepts in model-driven apps in Dynamics 365 (for example, customer, contact, quotation, and order) will be scaled to mid-market and upper-mid-market customers.</span></span>

<span data-ttu-id="9aac9-163">I den første version håndteres det meste af automatiseringen af dobbeltskrivningsløsninger.</span><span class="sxs-lookup"><span data-stu-id="9aac9-163">In the first release, most of the automation is handled by dual-write solutions.</span></span> <span data-ttu-id="9aac9-164">I fremtidige versioner bliver løsningerne en del af Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="9aac9-164">In future releases, those solutions will become part of Common Data Service.</span></span> <span data-ttu-id="9aac9-165">Når du forstår de kommende ændringer af Common Data Service, kan du spare en del på lang sigt.</span><span class="sxs-lookup"><span data-stu-id="9aac9-165">By understanding the upcoming changes to Common Data Service, you can save yourself effort in the long term.</span></span> <span data-ttu-id="9aac9-166">Her er nogle af de vigtigste ændringer:</span><span class="sxs-lookup"><span data-stu-id="9aac9-166">Here are some of the crucial changes:</span></span>

+ <span data-ttu-id="9aac9-167">Common Data Service vil få nye begreber såsom firma og part.</span><span class="sxs-lookup"><span data-stu-id="9aac9-167">Common Data Service will have new concepts, such as company and party.</span></span> <span data-ttu-id="9aac9-168">Disse begreber påvirker alle de apps, der er baseret på Common Data Service, som f.eks. Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service og Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="9aac9-168">These concepts will affect all apps that are built on Common Data Service, such as Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service, and Dynamics 365 Field Service.</span></span>
+ <span data-ttu-id="9aac9-169">Aktiviteter og noter samles og udvides til at understøtte både C1s (brugere af systemet) og C2s (systemkunder).</span><span class="sxs-lookup"><span data-stu-id="9aac9-169">Activities and notes are unified and expanded to support both C1s (users of the system) and C2s (customers of the system).</span></span>
+ <span data-ttu-id="9aac9-170">Her er nogle af de kommende ændringer i Common Data Service:</span><span class="sxs-lookup"><span data-stu-id="9aac9-170">Here are some of the upcoming changes in Common Data Service:</span></span>

    - <span data-ttu-id="9aac9-171">Datatypen decimal vil erstatte datatypen penge.</span><span class="sxs-lookup"><span data-stu-id="9aac9-171">The decimal data type will replace the money data type.</span></span>
    - <span data-ttu-id="9aac9-172">Datoudnyttelse understøtter tidligere, nuværende og fremtidige data på samme sted.</span><span class="sxs-lookup"><span data-stu-id="9aac9-172">Date effectivity will support past, present, and future data in the same place.</span></span>
    - <span data-ttu-id="9aac9-173">Der vil være mere understøttelse af valuta og valutakurser, og API'en (Application Programming Interface) **Valutakurs** vil blive revideret.</span><span class="sxs-lookup"><span data-stu-id="9aac9-173">There will be more support for currency and exchange rates, and the **Exchange Rate** application programming interface (API) will be revised.</span></span>
    - <span data-ttu-id="9aac9-174">Enhedsomregninger understøttes.</span><span class="sxs-lookup"><span data-stu-id="9aac9-174">Unit conversions will be supported.</span></span>

<span data-ttu-id="9aac9-175">Yderligere oplysninger om kommende ændringer finder du i [Data i Common Data Service – fase 1 & 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/finance-operations-crossapp-capabilities/data-common-data-service-phase-1).</span><span class="sxs-lookup"><span data-stu-id="9aac9-175">For more information about upcoming changes, see [Data in Common Data Service – phase 1 & 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/finance-operations-crossapp-capabilities/data-common-data-service-phase-1).</span></span>
