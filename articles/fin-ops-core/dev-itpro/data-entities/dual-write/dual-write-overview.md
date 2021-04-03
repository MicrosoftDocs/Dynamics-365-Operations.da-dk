---
title: Oversigt over dobbeltskrivning
description: Dette emne indeholder en oversigt over dobbeltskrivning, der giver næsten realtidsinteraktion mellem kundeengagementapps og Finance and Operations-apps.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 6cc02b483a2975dd3be28032ea7e90b540945492
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561272"
---
# <a name="dual-write-overview"></a><span data-ttu-id="e6b0a-103">Oversigt over dobbeltskrivning</span><span class="sxs-lookup"><span data-stu-id="e6b0a-103">Dual-write overview</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="what-is-dual-write"></a><span data-ttu-id="e6b0a-104">Hvad er dobbeltskrivning?</span><span class="sxs-lookup"><span data-stu-id="e6b0a-104">What is dual-write?</span></span>

<span data-ttu-id="e6b0a-105">Dobbeltskrivning er en brugsklar infrastruktur, der giver næsten realtidsinteraktion mellem kundeengagementapps og Finance and Operations-apps.</span><span class="sxs-lookup"><span data-stu-id="e6b0a-105">Dual-write is an out-of-box infrastructure that provides near-real-time interaction between customer engagement apps and Finance and Operations apps.</span></span> <span data-ttu-id="e6b0a-106">Når data om kunder, produkter, personer og handlinger går ud over programgrænserne, styrkes alle afdelinger i en organisation.</span><span class="sxs-lookup"><span data-stu-id="e6b0a-106">When data about customers, products, people, and operations flows beyond application boundaries, all departments in an organization are empowered.</span></span>

<span data-ttu-id="e6b0a-107">Dobbeltskrivning giver en tæt kombineret, tovejsintegration mellem Finance and Operations-apps og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="e6b0a-107">Dual-write provides tightly coupled, bidirectional integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="e6b0a-108">Alle dataændringer i Finance and Operations-apps forårsager ændringer i Dataverse, og alle dataændringer i Dataverse medfører ændringer i Finance and Operations-apps.</span><span class="sxs-lookup"><span data-stu-id="e6b0a-108">Any data change in Finance and Operations apps causes writes to Dataverse, and any data change in Dataverse causes writes to Finance and Operations apps.</span></span> <span data-ttu-id="e6b0a-109">Dette automatiserede dataflow giver en integreret brugeroplevelse på tværs af apps.</span><span class="sxs-lookup"><span data-stu-id="e6b0a-109">This automated data flow provides an integrated user experience across the apps.</span></span>

![Datarelation mellem apps](media/dual-write-overview.jpg)

<span data-ttu-id="e6b0a-111">Dobbeltskrivning har to aspekter: et *infrastruktur*-aspekt og et *program*-aspekt.</span><span class="sxs-lookup"><span data-stu-id="e6b0a-111">Dual-write has two aspects: an *infrastructure* aspect and an *application* aspect.</span></span>

### <a name="infrastructure"></a><span data-ttu-id="e6b0a-112">Infrastruktur</span><span class="sxs-lookup"><span data-stu-id="e6b0a-112">Infrastructure</span></span>

<span data-ttu-id="e6b0a-113">Dobbeltskrivningsinfrastrukturen kan udvides og er pålidelig og indeholder følgende nøglefunktioner:</span><span class="sxs-lookup"><span data-stu-id="e6b0a-113">The dual-write infrastructure is extensible and reliable, and includes the following key features:</span></span>

+ <span data-ttu-id="e6b0a-114">Synkrone og tovejsdatastrømme mellem programmer</span><span class="sxs-lookup"><span data-stu-id="e6b0a-114">Synchronous and bidirectional data flow between applications</span></span>
+ <span data-ttu-id="e6b0a-115">Synkronisering sammen med kørsels-, pause- og catch-up-tilstande til at understøtte systemet i onlinetilstand samt offline/asynkron-tilstand.</span><span class="sxs-lookup"><span data-stu-id="e6b0a-115">Synchronization, together with play, pause, and catchup modes to support the system during online and offline/asynchronous modes.</span></span>
+ <span data-ttu-id="e6b0a-116">Mulighed for at synkronisere indledende data mellem programmerne</span><span class="sxs-lookup"><span data-stu-id="e6b0a-116">Ability to sync initial data between the applications</span></span>
+ <span data-ttu-id="e6b0a-117">Kombineret visning af aktivitet og fejllogfiler for dataadministratorer</span><span class="sxs-lookup"><span data-stu-id="e6b0a-117">Combined view of activity and error logs for data admins</span></span>
+ <span data-ttu-id="e6b0a-118">Mulighed for at konfigurere brugerdefinerede påmindelser og tærskler og til at abonnere på beskeder</span><span class="sxs-lookup"><span data-stu-id="e6b0a-118">Ability to configure custom alerts and thresholds, and to subscribe to notifications</span></span>
+ <span data-ttu-id="e6b0a-119">Intuitiv brugergrænseflade (UI) til filtrering og transformationer</span><span class="sxs-lookup"><span data-stu-id="e6b0a-119">Intuitive user interface (UI) for filtering and transformations</span></span>
+ <span data-ttu-id="e6b0a-120">Mulighed for at angive og se tabelafhængigheder og relationer</span><span class="sxs-lookup"><span data-stu-id="e6b0a-120">Ability to set and view table dependencies and relationships</span></span>
+ <span data-ttu-id="e6b0a-121">Udvidelse til både standard- og brugerdefinerede tabeller og tilknytninger</span><span class="sxs-lookup"><span data-stu-id="e6b0a-121">Extensibility for both standard and custom tables and maps</span></span>
+ <span data-ttu-id="e6b0a-122">Pålidelig administration af programlevetiden</span><span class="sxs-lookup"><span data-stu-id="e6b0a-122">Reliable application lifecycle management</span></span>
+ <span data-ttu-id="e6b0a-123">Brugsklar opsætningsoplevelse for nye kunder</span><span class="sxs-lookup"><span data-stu-id="e6b0a-123">Out-of-box setup experience for new customers</span></span>

### <a name="application"></a><span data-ttu-id="e6b0a-124">Applikation</span><span class="sxs-lookup"><span data-stu-id="e6b0a-124">Application</span></span>

<span data-ttu-id="e6b0a-125">Dobbeltskrivning opretter en tilknytning mellem koncepter i Finance and Operations-apps og koncepter i kundeengagementapps.</span><span class="sxs-lookup"><span data-stu-id="e6b0a-125">Dual-write creates a mapping between concepts in Finance and Operations apps and concepts in customer engagement apps.</span></span> <span data-ttu-id="e6b0a-126">Denne integration understøtter følgende scenarier:</span><span class="sxs-lookup"><span data-stu-id="e6b0a-126">This integration supports the following scenarios:</span></span>

+ <span data-ttu-id="e6b0a-127">Integreret kundemaster</span><span class="sxs-lookup"><span data-stu-id="e6b0a-127">Integrated customer master</span></span>
+ <span data-ttu-id="e6b0a-128">Adgang til kundefordelskundekort og belønningspoint</span><span class="sxs-lookup"><span data-stu-id="e6b0a-128">Access to customer loyalty cards and reward points</span></span>
+ <span data-ttu-id="e6b0a-129">Samlet produktmasteroplevelse</span><span class="sxs-lookup"><span data-stu-id="e6b0a-129">Unified product mastering experience</span></span>
+ <span data-ttu-id="e6b0a-130">Bevidsthed om organisationens hierarki</span><span class="sxs-lookup"><span data-stu-id="e6b0a-130">Awareness of organization hierarchy</span></span>
+ <span data-ttu-id="e6b0a-131">Integreret kreditormaster</span><span class="sxs-lookup"><span data-stu-id="e6b0a-131">Integrated vendor master</span></span>
+ <span data-ttu-id="e6b0a-132">Adgang til finansierings- og momsreferencedata</span><span class="sxs-lookup"><span data-stu-id="e6b0a-132">Access to finance and tax reference data</span></span>
+ <span data-ttu-id="e6b0a-133">Prisprogramoplevelse efter behov</span><span class="sxs-lookup"><span data-stu-id="e6b0a-133">On-demand price engine experience</span></span>
+ <span data-ttu-id="e6b0a-134">Integreret kundeemne-til-køb-oplevelse</span><span class="sxs-lookup"><span data-stu-id="e6b0a-134">Integrated prospect-to-cash experience</span></span>
+ <span data-ttu-id="e6b0a-135">Mulighed for at betjene både interne aktiver og kundeaktiver via feltagenter</span><span class="sxs-lookup"><span data-stu-id="e6b0a-135">Ability to serve both in-house assets and customer assets through field agents</span></span>
+ <span data-ttu-id="e6b0a-136">Integreret oplevelse fra indkøb til betaling</span><span class="sxs-lookup"><span data-stu-id="e6b0a-136">Integrated procure-to-pay experience</span></span>
+ <span data-ttu-id="e6b0a-137">Integrerede aktiviteter og notater til kundedata og -dokumenter</span><span class="sxs-lookup"><span data-stu-id="e6b0a-137">Integrated activities and notes for customer data and documents</span></span>
+ <span data-ttu-id="e6b0a-138">Mulighed for at slå disponibel lagertilgængelighed op og få detaljer herom</span><span class="sxs-lookup"><span data-stu-id="e6b0a-138">Ability to look up on-hand inventory availability and details</span></span>
+ <span data-ttu-id="e6b0a-139">Oplevelsen projekt til kontant</span><span class="sxs-lookup"><span data-stu-id="e6b0a-139">Project-to-cash experience</span></span>
+ <span data-ttu-id="e6b0a-140">Mulighed for at håndtere flere adresser og roller via partskonceptet</span><span class="sxs-lookup"><span data-stu-id="e6b0a-140">Ability to handle multiple addresses and roles through the party concept</span></span>
+ <span data-ttu-id="e6b0a-141">Enkel kildestyring til brugere</span><span class="sxs-lookup"><span data-stu-id="e6b0a-141">Single source management for users</span></span>
+ <span data-ttu-id="e6b0a-142">Integrerede kanaler til detailhandel og marketing</span><span class="sxs-lookup"><span data-stu-id="e6b0a-142">Integrated channels for retailing and marketing</span></span>
+ <span data-ttu-id="e6b0a-143">Synlighed i kampagner og rabatter</span><span class="sxs-lookup"><span data-stu-id="e6b0a-143">Visibility into promotions and discounts</span></span>
+ <span data-ttu-id="e6b0a-144">Funktioner for anmodning om tjenester</span><span class="sxs-lookup"><span data-stu-id="e6b0a-144">Request-for-service functions</span></span>
+ <span data-ttu-id="e6b0a-145">Integrerede tjenestehandlinger</span><span class="sxs-lookup"><span data-stu-id="e6b0a-145">Streamlined service operations</span></span>

## <a name="top-reasons-to-use-dual-write"></a><span data-ttu-id="e6b0a-146">De vigtigste grunde til at bruge dobbeltskrivning</span><span class="sxs-lookup"><span data-stu-id="e6b0a-146">Top reasons to use dual-write</span></span>

<span data-ttu-id="e6b0a-147">Dobbeltskrivning giver dataintegration på tværs af Microsoft Dynamics 365-programmer.</span><span class="sxs-lookup"><span data-stu-id="e6b0a-147">Dual-write provides data integration across Microsoft Dynamics 365 applications.</span></span> <span data-ttu-id="e6b0a-148">Denne solide rammer forbinder miljøer og giver forskellige virksomhedsprogrammer mulighed for at arbejde sammen.</span><span class="sxs-lookup"><span data-stu-id="e6b0a-148">This robust framework links environments and enables different business applications to work together.</span></span> <span data-ttu-id="e6b0a-149">Her er de vigtigste grunde til, at du skal bruge dobbeltskrivning:</span><span class="sxs-lookup"><span data-stu-id="e6b0a-149">Here are the top reasons why you should use dual-write:</span></span>

+ <span data-ttu-id="e6b0a-150">Dobbeltskrivning giver tæt kombineret, nær-realtidsintegration tovejsintegration mellem Finance and Operations-apps og modelbaserede apps i Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="e6b0a-150">Dual-write provides tightly coupled, near-real-time, and bidirectional integration between Finance and Operations apps and model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="e6b0a-151">Denne integration gør Microsoft Dynamics 365 til en fælles løsning for alle dine virksomhedsløsninger.</span><span class="sxs-lookup"><span data-stu-id="e6b0a-151">This integration makes Microsoft Dynamics 365 the one-stop shop for all your business solutions.</span></span> <span data-ttu-id="e6b0a-152">Kunder, der bruger Dynamics 365 Finance og Dynamics 365 Supply Chain Management, men som bruger løsninger fra andre leverandører end Microsoft til kunderelationsstyring (CRM), hælder mod Dynamics 365 for så vidt angår understøttelse af dobbeltskrivning.</span><span class="sxs-lookup"><span data-stu-id="e6b0a-152">Customers who use Dynamics 365 Finance and Dynamics 365 Supply Chain Management, but who use non-Microsoft solutions for customer relationship management (CRM), are moving toward Dynamics 365 for its dual-write support.</span></span>
+ <span data-ttu-id="e6b0a-153">Data fra kunder, produkter, handlinger, projekter og Tingenes internet flyder automatisk over til Dataverse via dobbeltskrivning.</span><span class="sxs-lookup"><span data-stu-id="e6b0a-153">Data from customers, products, operations, projects, and the Internet of Things (IoT) automatically flows to Dataverse through dual-write.</span></span> <span data-ttu-id="e6b0a-154">Denne forbindelse er nyttig for virksomheder, der er interesserede i Power Platform-udvidelser.</span><span class="sxs-lookup"><span data-stu-id="e6b0a-154">This connection is useful for businesses that are interested in Power Platform expansions.</span></span>
+ <span data-ttu-id="e6b0a-155">Infrastrukturen med dobbeltskrivninger følger princippet om ingen kode/lav kode.</span><span class="sxs-lookup"><span data-stu-id="e6b0a-155">The dual-write infrastructure follows the no-code/low-code principle.</span></span> <span data-ttu-id="e6b0a-156">Der kræves en minimal teknisk indsats for at udvide standard tabel-til-tabel-tilknytningerne og for at medtage brugerdefinerede kort.</span><span class="sxs-lookup"><span data-stu-id="e6b0a-156">Minimal engineering effort is required to extend the standard table-to-table maps and to include custom maps.</span></span>
+ <span data-ttu-id="e6b0a-157">Dobbeltskrivning understøtter både onlinetilstand og offlinetilstand.</span><span class="sxs-lookup"><span data-stu-id="e6b0a-157">Dual-write supports both online mode and offline mode.</span></span> <span data-ttu-id="e6b0a-158">Microsoft er det eneste firma, der tilbyder support til online- og offline-tilstand.</span><span class="sxs-lookup"><span data-stu-id="e6b0a-158">Microsoft is the only company that offers support for online and offline modes.</span></span>

## <a name="what-does-dual-write-mean-for-developers-and-architects-of-customer-engagement-apps"></a><a id="developer-architect"></a><span data-ttu-id="e6b0a-159">Hvad betyder dobbeltskrivning for udviklere og arkitekter af kundeengagementapps?</span><span class="sxs-lookup"><span data-stu-id="e6b0a-159">What does dual-write mean for developers and architects of customer engagement apps?</span></span>

<span data-ttu-id="e6b0a-160">Dobbeltskrivning automatiserer datastrømmen mellem Finance and Operations-apps og kundeengagementapps.</span><span class="sxs-lookup"><span data-stu-id="e6b0a-160">Dual-write automates the data flow between Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="e6b0a-161">Dobbeltskrivning består af to AppSource-løsninger, der er installeret på Dataverse.</span><span class="sxs-lookup"><span data-stu-id="e6b0a-161">Dual-write consists of two AppSource solutions that are installed on Dataverse.</span></span> <span data-ttu-id="e6b0a-162">Løsningerne udvider tabelskemaet, plug-ins og arbejdsprocesser på Dataverse, så de kan skaleres til ERP-størrelse.</span><span class="sxs-lookup"><span data-stu-id="e6b0a-162">The solutions expand the table schema, plugins, and workflows on Dataverse so that they can scale to ERP size.</span></span> <span data-ttu-id="e6b0a-163">For at opnå en vellykket implementering skal udviklere og arkitekter af kundeengagementapps forstå disse ændringer og samarbejde med deres kolleger på Finance and Operations-apps.</span><span class="sxs-lookup"><span data-stu-id="e6b0a-163">For a successful implementation, developers and architects of customer engagement apps must understand these changes and collaborate with their counterparts on Finance and Operations apps.</span></span>

<span data-ttu-id="e6b0a-164">For at skabe paritet med Finance and Operations-programmer foretager dobbeltskrivning vigtige ændringer i Dataverse-skemaet.</span><span class="sxs-lookup"><span data-stu-id="e6b0a-164">To create parity with Finance and Operations applications, dual-write makes some crucial changes in the Dataverse schema.</span></span> <span data-ttu-id="e6b0a-165">Hvis du forstår planen, kan du slippe for at ændre noget design og udvikling fremover.</span><span class="sxs-lookup"><span data-stu-id="e6b0a-165">If you understand the plan, you can avoid some design and development rework in the future.</span></span>

+ <span data-ttu-id="e6b0a-166">Når AppSource-pakken til dobbeltskrivning er installeret, vil Dataverse have nye begreber som f.eks. firma og part.</span><span class="sxs-lookup"><span data-stu-id="e6b0a-166">When the dual-write AppSource package is installed, Dataverse will have new concepts such as company and party.</span></span> <span data-ttu-id="e6b0a-167">Disse koncepter hjælper programmer, der bygger på Dataverse, herunder Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service og Dynamics 365 Field Service, med problemfri interaktion med Finance and Operations-apps.</span><span class="sxs-lookup"><span data-stu-id="e6b0a-167">These concepts help applications built on Dataverse, including Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service, and Dynamics 365 Field Service, to interact seamlessly with Finance and Operations apps.</span></span>

+ <span data-ttu-id="e6b0a-168">Aktiviteter og noter samles og udvides til at understøtte både C1s (brugere af systemet) og C2s (systemkunder).</span><span class="sxs-lookup"><span data-stu-id="e6b0a-168">Activities and notes are unified and expanded to support both C1s (users of the system) and C2s (customers of the system).</span></span>

+ <span data-ttu-id="e6b0a-169">Hvis du vil undgå tab af data i forbindelse med valutaoverførsel mellem Finance and Operations-apps og Dataverse, kan du udvide antallet af decimaler i valutadatatypen for kundeengagementapps.</span><span class="sxs-lookup"><span data-stu-id="e6b0a-169">To prevent data loss during currency transmission between Finance and Operations apps and the Dataverse, you'll be able to extend the number of decimal places in the currency data type of customers engagement apps.</span></span> <span data-ttu-id="e6b0a-170">Med denne funktion oversættes eksisterende rækker automatisk til den nye udvidede tilstand på metadatalaget.</span><span class="sxs-lookup"><span data-stu-id="e6b0a-170">The feature autotranslates existing rows to the new extended state at the metadata layer.</span></span> <span data-ttu-id="e6b0a-171">I løbet af denne proces oversættes valutaværdien til decimaldata og ikke til pengedata, og valutaværdien understøtter 10 decimalpladser.</span><span class="sxs-lookup"><span data-stu-id="e6b0a-171">During this process, the currency value is translated to decimal data rather than money data, and the currency value supports 10 decimal places.</span></span> <span data-ttu-id="e6b0a-172">Denne funktion er et tilvalg, og organisationer, der ikke har brug for mere end 4 decimaler, behøver ikke at tilmelde sig.</span><span class="sxs-lookup"><span data-stu-id="e6b0a-172">This feature is opt-in, and organizations that don't need more than 4 decimal places of precision do not need to opt in.</span></span> <span data-ttu-id="e6b0a-173">Du kan finde flere oplysninger under [Migrering af valutadatatype til dobbeltskrivning](currrency-decimal-places.md).</span><span class="sxs-lookup"><span data-stu-id="e6b0a-173">For more information, see [Currency data-type migration for dual-write](currrency-decimal-places.md).</span></span>

+ <span data-ttu-id="e6b0a-174">[Gyldighedsdato](../../dev-tools/date-effectivity.md) vil blive føjet til Dataverse.</span><span class="sxs-lookup"><span data-stu-id="e6b0a-174">[Date effectivity](../../dev-tools/date-effectivity.md) will be added to Dataverse.</span></span> <span data-ttu-id="e6b0a-175">Den understøtter tidligere, nuværende og fremtidige data på samme tabel.</span><span class="sxs-lookup"><span data-stu-id="e6b0a-175">It will support past, present, and future data on the same table.</span></span>

+ <span data-ttu-id="e6b0a-176">Produktets [enhedsomregninger](../../../../supply-chain/pim/tasks/manage-unit-measure.md) understøttes for produkter, tilbud, ordrer og fakturaer.</span><span class="sxs-lookup"><span data-stu-id="e6b0a-176">Product [unit conversions](../../../../supply-chain/pim/tasks/manage-unit-measure.md) are supported for products, quotes, orders, and invoices.</span></span>

<span data-ttu-id="e6b0a-177">Yderligere oplysninger om kommende ændringer finder du i [Nyheder eller ændringer i dobbeltskrivning](whats-new-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="e6b0a-177">For more information about upcoming changes, see [What's new or changed in dual-write](whats-new-dual-write.md).</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]