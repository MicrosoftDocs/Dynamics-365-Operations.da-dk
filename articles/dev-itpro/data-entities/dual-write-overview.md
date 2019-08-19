---
title: Integration næsten i realtid mellem Finance and Operations og Common Data Service
description: Dette emne indeholder en oversigt over integrationen mellem Microsoft Dynamics 365 for Finance and Operations og Common Data Service.
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
ms.openlocfilehash: aa614c8e6a79a3f7a4f8f2f99f1f1bd1a67ac921
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797222"
---
# <a name="near-real-time-data-integration-between-finance-and-operations-and-common-data-service"></a><span data-ttu-id="fa1fe-103">Integration næsten i realtid mellem Finance and Operations og Common Data Service</span><span class="sxs-lookup"><span data-stu-id="fa1fe-103">Near-real-time data integration between Finance and Operations and Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="fa1fe-104">I den nuværende digitale verden bruger professionelle økosystemer Microsoft Dynamics 365-pakken som helhed.</span><span class="sxs-lookup"><span data-stu-id="fa1fe-104">In the current digital world, business ecosystems use the Microsoft Dynamics 365 suite as a whole.</span></span> <span data-ttu-id="fa1fe-105">Da data fra personer, kunder, drift og Tingenes internet flyder ind i én kilde, er der mulighed for digitale feedbackløkker.</span><span class="sxs-lookup"><span data-stu-id="fa1fe-105">Because data from people, customers, operations, and Internet of Things (IoT) devices flows into one source, there is an opportunity for digital feedback loops.</span></span> <span data-ttu-id="fa1fe-106">For at opnå denne oplevelse er integration mellem Dynamics 365 for Finance and Operations og Dynamics 365 for Customer Engagement-programmer afgørende.</span><span class="sxs-lookup"><span data-stu-id="fa1fe-106">To achieve this experience, integration between Dynamics 365 for Finance and Operations and Dynamics 365 for Customer Engagement applications is essential.</span></span> <span data-ttu-id="fa1fe-107">Customer Engagement-programmer er bygget oven på Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="fa1fe-107">Customer Engagement applications are built on top of Common Data Service.</span></span> <span data-ttu-id="fa1fe-108">Integration mellem Finance and Operations-data og Common Data Service giver Customer Engagement-programmer mulighed for at kommunikere sammenhængende og flydende med Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="fa1fe-108">Integration between Finance and Operations data with Common Data Service lets Customer Engagement applications communicate coherently and fluently with Finance and Operations.</span></span>

<span data-ttu-id="fa1fe-109">Finance and Operations og Common Data Service leverer datasynkronisering tæt på realtid mellem Finance and Operations og Customer Engagement-programmer via en dobbeltskrivningsstruktur.</span><span class="sxs-lookup"><span data-stu-id="fa1fe-109">Finance and Operations and Common Data Service provide near-real-time data synchronization between Finance and Operations and Customer Engagement applications via a dual-write framework.</span></span> <span data-ttu-id="fa1fe-110">Dækningen er bred og spænder over 28 overfladeområder i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="fa1fe-110">The coverage is broad and spans 28 surface areas of Finance and Operations.</span></span> <span data-ttu-id="fa1fe-111">Målet er at skabe én "One Dynamics 365"-brugeroplevelse gennem problemfri datastrømme, der forbinder forretningsprocesser på tværs af applikationer.</span><span class="sxs-lookup"><span data-stu-id="fa1fe-111">The goal is to provide a "One Dynamics 365" user experience through seamless data flows that connect business processes across applications.</span></span>

![Diagram over arkitekturoversigt](media/dual-write-overview.jpg)

<span data-ttu-id="fa1fe-113">Følgende værdiforslag er tilgængelige for kunderne:</span><span class="sxs-lookup"><span data-stu-id="fa1fe-113">The following value propositions are available for customers:</span></span>

+ [<span data-ttu-id="fa1fe-114">Organisationshierarki i Common Data Service</span><span class="sxs-lookup"><span data-stu-id="fa1fe-114">Organization hierarchy in Common Data Service</span></span>](dual-write-organization.md)
+ [<span data-ttu-id="fa1fe-115">Firmakoncept i Common Data Service</span><span class="sxs-lookup"><span data-stu-id="fa1fe-115">Company concept in Common Data Service</span></span>](dual-write-company.md)
+ [<span data-ttu-id="fa1fe-116">Integreret debitormaster</span><span class="sxs-lookup"><span data-stu-id="fa1fe-116">Integrated customer master</span></span>](dual-write-customer.md)
+ [<span data-ttu-id="fa1fe-117">Integreret kreditormaster</span><span class="sxs-lookup"><span data-stu-id="fa1fe-117">Integrated vendor master</span></span>](dual-write-vendor.md)
+ <span data-ttu-id="fa1fe-118">Samlet produktmaster</span><span class="sxs-lookup"><span data-stu-id="fa1fe-118">Unified product master</span></span>

## <a name="system-requirements"></a><span data-ttu-id="fa1fe-119">Systemkrav</span><span class="sxs-lookup"><span data-stu-id="fa1fe-119">System requirements</span></span>

<span data-ttu-id="fa1fe-120">Synkrone, tovejs datastrømme næsten i realtid kræver følgende versioner:</span><span class="sxs-lookup"><span data-stu-id="fa1fe-120">Synchronous, bidirectional, near-real-time data flows require the following versions:</span></span>

+ <span data-ttu-id="fa1fe-121">Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (juli 2019) med Platform update 28 eller nyere</span><span class="sxs-lookup"><span data-stu-id="fa1fe-121">Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019) with Platform update 28, or later</span></span>
+ <span data-ttu-id="fa1fe-122">Microsoft Dynamics 365 for Customer Engagement, Platform version 9.1 (4.2) eller nyere</span><span class="sxs-lookup"><span data-stu-id="fa1fe-122">Microsoft Dynamics 365 for Customer Engagement, Platform version 9.1 (4.2) or later</span></span>

## <a name="setup-instructions"></a><span data-ttu-id="fa1fe-123">Installationsvejledning</span><span class="sxs-lookup"><span data-stu-id="fa1fe-123">Setup instructions</span></span>

<span data-ttu-id="fa1fe-124">Følg disse trin for at konfigurere integrationen mellem Finance and Operations og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="fa1fe-124">Follow these steps to set up integration between Finance and Operations and Common Data Service.</span></span>
    
1. <span data-ttu-id="fa1fe-125">For opsætningen af dobbeltskrivningssystemet skal du se [trinvis vejledning](https://aka.ms/dualwrite-docs) til annoncering af prøveversion af dobbeltskrivning.</span><span class="sxs-lookup"><span data-stu-id="fa1fe-125">For the setup of the dual-write system, see the [step-by-step guide](https://aka.ms/dualwrite-docs) on Announcing Dual Write Preview.</span></span>
2. <span data-ttu-id="fa1fe-126">Download og installer løsningen fra [Finance and Operations, Common Data Service og Customer Engagement-integration](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer-gruppen.</span><span class="sxs-lookup"><span data-stu-id="fa1fe-126">Download and install the solution from the [Finance and Operations, Common Data Service, and Customer Engagement Integration](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer group.</span></span> <span data-ttu-id="fa1fe-127">Pakken indeholder fem løsninger:</span><span class="sxs-lookup"><span data-stu-id="fa1fe-127">The package contains five solutions:</span></span>

    + <span data-ttu-id="fa1fe-128">Dynamics365Company</span><span class="sxs-lookup"><span data-stu-id="fa1fe-128">Dynamics365Company</span></span>
    + <span data-ttu-id="fa1fe-129">CurrencyExchangeRates</span><span class="sxs-lookup"><span data-stu-id="fa1fe-129">CurrencyExchangeRates</span></span>
    + <span data-ttu-id="fa1fe-130">Dynamics365FinanceAndOperationsCommon</span><span class="sxs-lookup"><span data-stu-id="fa1fe-130">Dynamics365FinanceAndOperationsCommon</span></span>
    + <span data-ttu-id="fa1fe-131">Dynamics365FinanceCommon</span><span class="sxs-lookup"><span data-stu-id="fa1fe-131">Dynamics365FinanceCommon</span></span>
    + <span data-ttu-id="fa1fe-132">Dynamics365SupplyChainCommon</span><span class="sxs-lookup"><span data-stu-id="fa1fe-132">Dynamics365SupplyChainCommon</span></span>

3. <span data-ttu-id="fa1fe-133">Følg udførelsesrækkefølgen for [synkronisering af indledende referencedata](dual-write-initial.md).</span><span class="sxs-lookup"><span data-stu-id="fa1fe-133">Follow the execution order for [synchronizing initial reference data](dual-write-initial.md).</span></span>
4. <span data-ttu-id="fa1fe-134">Hvis du støder på problemer med dobbeltskrivningssynkronisering, skal du se [Fejlfindingsvejledning til dataintegration](dual-write-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="fa1fe-134">If you encounter dual-write synchronization issues, see the [Troubleshooting guide for data integration](dual-write-troubleshooting.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fa1fe-135">Du kan ikke køre dobbeltskrivning og [Kundeemne til kontanter](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) side om side.</span><span class="sxs-lookup"><span data-stu-id="fa1fe-135">You can’t run dual-write and [Prospect to cash](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) side-by-side.</span></span> <span data-ttu-id="fa1fe-136">Hvis du kører løsningen Kundeemne til kontanter, skal du afinstallere den.</span><span class="sxs-lookup"><span data-stu-id="fa1fe-136">If you're running the Prospect to cash solution, you must uninstall it.</span></span> <span data-ttu-id="fa1fe-137">Du skal også deaktivere de skabeloner til dobbeltskrivning af debitorer og kreditorer, der er en del af løsningen Kundeemne til kontanter.</span><span class="sxs-lookup"><span data-stu-id="fa1fe-137">You must also disable the customer and vendor dual-write templates that are part of the Prospect to cash solution.</span></span>
