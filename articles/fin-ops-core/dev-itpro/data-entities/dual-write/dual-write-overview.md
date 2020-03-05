---
title: Integration næsten i realtid med Common Data Service
description: Dette emne indeholder en oversigt over integrationen mellem Finance and Operations og Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
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
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 1c09b0c0bb695e7695acb7a8821ffb99ae1f6f06
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019702"
---
# <a name="near-real-time-data-integration-with-common-data-service"></a><span data-ttu-id="9dca1-103">Integration næsten i realtid med Common Data Service</span><span class="sxs-lookup"><span data-stu-id="9dca1-103">Near-real-time data integration with Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="9dca1-104">I den nuværende digitale verden bruger professionelle økosystemer Microsoft Dynamics 365-programmer som en helhed.</span><span class="sxs-lookup"><span data-stu-id="9dca1-104">In the current digital world, business ecosystems use Microsoft Dynamics 365 applications as a whole.</span></span> <span data-ttu-id="9dca1-105">Da data fra personer, kunder, drift og Tingenes internet flyder ind i én kilde, er der mulighed for digitale feedbackløkker.</span><span class="sxs-lookup"><span data-stu-id="9dca1-105">Because data from people, customers, operations, and Internet of Things (IoT) devices flows into one source, there is an opportunity for digital feedback loops.</span></span> <span data-ttu-id="9dca1-106">For at opnå denne oplevelse er integration mellem Finance and Operations-apps og Dynamics 365-programmer afgørende.</span><span class="sxs-lookup"><span data-stu-id="9dca1-106">To achieve this experience, integration between Finance and Operations apps and other Dynamics 365 applications is essential.</span></span> <span data-ttu-id="9dca1-107">Nogle programmer er bygget oven på Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="9dca1-107">Some applications are built on top of Common Data Service.</span></span> <span data-ttu-id="9dca1-108">Integration mellem Finance and Operations-appsdata og Common Data Service giver andre programmer muligheder for at kommunikere sammenhængende og flydende med Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9dca1-108">Integration between Finance and Operations apps data with Common Data Service lets other applications communicate coherently and fluently with Finance and Operations.</span></span>

<span data-ttu-id="9dca1-109">Finance and Operations-apps og Common Data Service leverer datasynkronisering tæt på realtid mellem Finance and Operations-apps og andre Dynamics 365-programmer via en dobbeltskrivningsstruktur.</span><span class="sxs-lookup"><span data-stu-id="9dca1-109">Finance and Operations apps and Common Data Service provide near-real-time data synchronization between Finance and Operations apps and other Dynamics 365 applications via a dual-write framework.</span></span> <span data-ttu-id="9dca1-110">Dækningen er bred og spænder over 28 overfladeområder i programmet.</span><span class="sxs-lookup"><span data-stu-id="9dca1-110">The coverage is broad and spans 28 surface areas of the application.</span></span> <span data-ttu-id="9dca1-111">Målet er at skabe én "One Dynamics 365"-brugeroplevelse gennem problemfri datastrømme, der forbinder forretningsprocesser på tværs af applikationer.</span><span class="sxs-lookup"><span data-stu-id="9dca1-111">The goal is to provide a "One Dynamics 365" user experience through seamless data flows that connect business processes across applications.</span></span>

![Diagram over arkitekturoversigt](media/dual-write-overview.jpg)

<span data-ttu-id="9dca1-113">Følgende værdiforslag er tilgængelige:</span><span class="sxs-lookup"><span data-stu-id="9dca1-113">The following value propositions are available:</span></span>

+ [<span data-ttu-id="9dca1-114">Organisationshierarki i Common Data Service</span><span class="sxs-lookup"><span data-stu-id="9dca1-114">Organization hierarchy in Common Data Service</span></span>](organization-mapping.md)
+ [<span data-ttu-id="9dca1-115">Firmakoncept i Common Data Service</span><span class="sxs-lookup"><span data-stu-id="9dca1-115">Company concept in Common Data Service</span></span>](company-data.md)
+ [<span data-ttu-id="9dca1-116">Integreret debitormaster</span><span class="sxs-lookup"><span data-stu-id="9dca1-116">Integrated customer master</span></span>](customer-mapping.md)
+ [<span data-ttu-id="9dca1-117">Integreret finans</span><span class="sxs-lookup"><span data-stu-id="9dca1-117">Integrated ledger</span></span>](ledger-mapping.md)
+ [<span data-ttu-id="9dca1-118">Samlet produktoplevelse</span><span class="sxs-lookup"><span data-stu-id="9dca1-118">Unified product experience</span></span>](product-mapping.md)
+ [<span data-ttu-id="9dca1-119">Integreret kreditormaster</span><span class="sxs-lookup"><span data-stu-id="9dca1-119">Integrated vendor master</span></span>](vendor-mapping.md)
+ [<span data-ttu-id="9dca1-120">Integrerede lokationer og lagersteder</span><span class="sxs-lookup"><span data-stu-id="9dca1-120">Integrated sites and warehouses</span></span>](sites-warehouses-mapping.md)
+ [<span data-ttu-id="9dca1-121">Integreret momsmaster</span><span class="sxs-lookup"><span data-stu-id="9dca1-121">Integrated tax master</span></span>](tax-mapping.md)

## <a name="system-requirements"></a><span data-ttu-id="9dca1-122">Systemkrav</span><span class="sxs-lookup"><span data-stu-id="9dca1-122">System requirements</span></span>

<span data-ttu-id="9dca1-123">Synkrone, tovejs datastrømme næsten i realtid kræver følgende versioner:</span><span class="sxs-lookup"><span data-stu-id="9dca1-123">Synchronous, bidirectional, near-real-time data flows require the following versions:</span></span>

+ <span data-ttu-id="9dca1-124">Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (juli 2019) med Platform update 28 eller nyere</span><span class="sxs-lookup"><span data-stu-id="9dca1-124">Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019) with Platform update 28, or later</span></span>
+ <span data-ttu-id="9dca1-125">Microsoft Dynamics 365 for Customer Engagement, Platform version 9.1 (4.2) eller nyere</span><span class="sxs-lookup"><span data-stu-id="9dca1-125">Microsoft Dynamics 365 for Customer Engagement, Platform version 9.1 (4.2) or later</span></span>

## <a name="setup-instructions"></a><span data-ttu-id="9dca1-126">Installationsvejledning</span><span class="sxs-lookup"><span data-stu-id="9dca1-126">Setup instructions</span></span>

<span data-ttu-id="9dca1-127">Benyt følgende fremgangsmåde for at konfigurere mellem Finance and Operations-apps og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="9dca1-127">Follow these steps to set up integration between Finance and Operations apps and Common Data Service.</span></span>
    
1. <span data-ttu-id="9dca1-128">For opsætningen af dobbeltskrivningssystemet skal du se [trinvis vejledning](https://aka.ms/dualwrite-docs) til annoncering af prøveversion af dobbeltskrivning.</span><span class="sxs-lookup"><span data-stu-id="9dca1-128">For the setup of the dual-write system, see the [step-by-step guide](https://aka.ms/dualwrite-docs) on Announcing Dual Write Preview.</span></span>
2. <span data-ttu-id="9dca1-129">Download og Installer løsningen fra gruppen [Fin Ops og CDS-/CE-integration via dobbeltskrivning](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer.</span><span class="sxs-lookup"><span data-stu-id="9dca1-129">Download and install the solution from the [Fin Ops and CDS/CE Integration via Dual-Write](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer group.</span></span> <span data-ttu-id="9dca1-130">Pakken indeholder fem løsninger:</span><span class="sxs-lookup"><span data-stu-id="9dca1-130">The package contains five solutions:</span></span>

    + <span data-ttu-id="9dca1-131">Dynamics365Company</span><span class="sxs-lookup"><span data-stu-id="9dca1-131">Dynamics365Company</span></span>
    + <span data-ttu-id="9dca1-132">CurrencyExchangeRates</span><span class="sxs-lookup"><span data-stu-id="9dca1-132">CurrencyExchangeRates</span></span>
    + <span data-ttu-id="9dca1-133">Dynamics365FinanceAndOperationsCommon</span><span class="sxs-lookup"><span data-stu-id="9dca1-133">Dynamics365FinanceAndOperationsCommon</span></span>
    + <span data-ttu-id="9dca1-134">Dynamics365FinanceCommon</span><span class="sxs-lookup"><span data-stu-id="9dca1-134">Dynamics365FinanceCommon</span></span>
    + <span data-ttu-id="9dca1-135">Dynamics365SupplyChainCommon</span><span class="sxs-lookup"><span data-stu-id="9dca1-135">Dynamics365SupplyChainCommon</span></span>

3. <span data-ttu-id="9dca1-136">Følg udførelsesrækkefølgen for [synkronisering af indledende referencedata](initial-sync.md).</span><span class="sxs-lookup"><span data-stu-id="9dca1-136">Follow the execution order for [synchronizing initial reference data](initial-sync.md).</span></span>
4. <span data-ttu-id="9dca1-137">Hvis du støder på problemer med dobbeltskrivningssynkronisering, skal du se [Fejlfindingsvejledning til dataintegration](dual-write-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="9dca1-137">If you encounter dual-write synchronization issues, see the [Troubleshooting guide for data integration](dual-write-troubleshooting.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9dca1-138">Du kan ikke køre dobbeltskrivning og [Kundeemne til kontanter](../../../../supply-chain/sales-marketing/prospect-to-cash.md) side om side.</span><span class="sxs-lookup"><span data-stu-id="9dca1-138">You can’t run dual-write and [Prospect to cash](../../../../supply-chain/sales-marketing/prospect-to-cash.md) side-by-side.</span></span> <span data-ttu-id="9dca1-139">Hvis du kører løsningen Kundeemne til kontanter, skal du afinstallere den.</span><span class="sxs-lookup"><span data-stu-id="9dca1-139">If you're running the Prospect to cash solution, you must uninstall it.</span></span> <span data-ttu-id="9dca1-140">Du skal også deaktivere de skabeloner til dobbeltskrivning af debitorer og kreditorer, der er en del af løsningen Kundeemne til kontanter.</span><span class="sxs-lookup"><span data-stu-id="9dca1-140">You must also disable the customer and vendor dual-write templates that are part of the Prospect to cash solution.</span></span>