---
title: Integration næsten i realtid med Common Data Service
description: Dette emne indeholder en oversigt over integrationen mellem Finance and Operations-apps og Common Data Service.
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
ms.openlocfilehash: d70bce4e47c05a7974c1b974fdca17682e5370aa
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550851"
---
# <a name="near-real-time-data-integration-with-common-data-service"></a><span data-ttu-id="f2c13-103">Integration næsten i realtid med Common Data Service</span><span class="sxs-lookup"><span data-stu-id="f2c13-103">Near-real-time data integration with Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="f2c13-104">I den nuværende digitale verden bruger professionelle økosystemer Microsoft Dynamics 365-programmer som en helhed.</span><span class="sxs-lookup"><span data-stu-id="f2c13-104">In the current digital world, business ecosystems use Microsoft Dynamics 365 applications as a whole.</span></span> <span data-ttu-id="f2c13-105">Da data fra personer, kunder, drift og Tingenes internet flyder ind i én kilde, er der mulighed for digitale feedbackløkker.</span><span class="sxs-lookup"><span data-stu-id="f2c13-105">Because data from people, customers, operations, and Internet of Things (IoT) devices flows into one source, there is an opportunity for digital feedback loops.</span></span> <span data-ttu-id="f2c13-106">For at opnå denne oplevelse er integration mellem Finance and Operations-apps og Dynamics 365-programmer afgørende.</span><span class="sxs-lookup"><span data-stu-id="f2c13-106">To achieve this experience, integration between Finance and Operations apps and other Dynamics 365 applications is essential.</span></span> <span data-ttu-id="f2c13-107">Nogle programmer er bygget oven på Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="f2c13-107">Some applications are built on top of Common Data Service.</span></span> <span data-ttu-id="f2c13-108">Integration mellem Finance and Operations-appdata og Common Data Service giver andre programmer mulighed for at kommunikere sammenhængende og flydende med Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f2c13-108">Integration between Finance and Operations apps data with Common Data Service lets other applications communicate coherently and fluently with Finance and Operations.</span></span>

<span data-ttu-id="f2c13-109">Finance and Operations-apps og Common Data Service leverer datasynkronisering tæt på realtid mellem Finance and Operations-apps og andre Dynamics 365-programmer via en dobbeltskrivningsstruktur.</span><span class="sxs-lookup"><span data-stu-id="f2c13-109">Finance and Operations apps and Common Data Service provide near-real-time data synchronization between Finance and Operations apps and other Dynamics 365 applications via a dual-write framework.</span></span> <span data-ttu-id="f2c13-110">Dækningen er bred og spænder over 28 overfladeområder i programmet.</span><span class="sxs-lookup"><span data-stu-id="f2c13-110">The coverage is broad and spans 28 surface areas of the application.</span></span> <span data-ttu-id="f2c13-111">Målet er at skabe én "One Dynamics 365"-brugeroplevelse gennem problemfri datastrømme, der forbinder forretningsprocesser på tværs af applikationer.</span><span class="sxs-lookup"><span data-stu-id="f2c13-111">The goal is to provide a "One Dynamics 365" user experience through seamless data flows that connect business processes across applications.</span></span>

![Diagram over arkitekturoversigt](media/dual-write-overview.jpg)

<span data-ttu-id="f2c13-113">Følgende værdiforslag er tilgængelige for kunderne:</span><span class="sxs-lookup"><span data-stu-id="f2c13-113">The following value propositions are available for customers:</span></span>

+ [<span data-ttu-id="f2c13-114">Organisationshierarki i Common Data Service</span><span class="sxs-lookup"><span data-stu-id="f2c13-114">Organization hierarchy in Common Data Service</span></span>](dual-write-organization.md)
+ [<span data-ttu-id="f2c13-115">Firmakoncept i Common Data Service</span><span class="sxs-lookup"><span data-stu-id="f2c13-115">Company concept in Common Data Service</span></span>](dual-write-company.md)
+ [<span data-ttu-id="f2c13-116">Integreret debitormaster</span><span class="sxs-lookup"><span data-stu-id="f2c13-116">Integrated customer master</span></span>](dual-write-customer.md)
+ [<span data-ttu-id="f2c13-117">Integreret kreditormaster</span><span class="sxs-lookup"><span data-stu-id="f2c13-117">Integrated vendor master</span></span>](dual-write-vendor.md)
+ <span data-ttu-id="f2c13-118">Samlet produktmaster</span><span class="sxs-lookup"><span data-stu-id="f2c13-118">Unified product master</span></span>

## <a name="system-requirements"></a><span data-ttu-id="f2c13-119">Systemkrav</span><span class="sxs-lookup"><span data-stu-id="f2c13-119">System requirements</span></span>

<span data-ttu-id="f2c13-120">Synkrone, tovejs datastrømme næsten i realtid kræver følgende versioner:</span><span class="sxs-lookup"><span data-stu-id="f2c13-120">Synchronous, bidirectional, near-real-time data flows require the following versions:</span></span>

+ <span data-ttu-id="f2c13-121">Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (juli 2019) med Platform update 28 eller nyere</span><span class="sxs-lookup"><span data-stu-id="f2c13-121">Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019) with Platform update 28, or later</span></span>
+ <span data-ttu-id="f2c13-122">Microsoft Dynamics 365 for Customer Engagement, Platform version 9.1 (4.2) eller nyere</span><span class="sxs-lookup"><span data-stu-id="f2c13-122">Microsoft Dynamics 365 for Customer Engagement, Platform version 9.1 (4.2) or later</span></span>

## <a name="setup-instructions"></a><span data-ttu-id="f2c13-123">Installationsvejledning</span><span class="sxs-lookup"><span data-stu-id="f2c13-123">Setup instructions</span></span>

<span data-ttu-id="f2c13-124">Følg disse trin for at konfigurere integrationen mellem Finance and Operations-apps og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="f2c13-124">Follow these steps to set up integration between Finance and Operations apps and Common Data Service.</span></span>
    
1. <span data-ttu-id="f2c13-125">For opsætningen af dobbeltskrivningssystemet skal du se [trinvis vejledning](https://aka.ms/dualwrite-docs) til annoncering af prøveversion af dobbeltskrivning.</span><span class="sxs-lookup"><span data-stu-id="f2c13-125">For the setup of the dual-write system, see the [step-by-step guide](https://aka.ms/dualwrite-docs) on Announcing Dual Write Preview.</span></span>
2. <span data-ttu-id="f2c13-126">Download og installer løsningen fra [Finance and Operations, Common Data Service og Customer Engagement-integration](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer-gruppen.</span><span class="sxs-lookup"><span data-stu-id="f2c13-126">Download and install the solution from the [Finance and Operations, Common Data Service, and Customer Engagement Integration](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer group.</span></span> <span data-ttu-id="f2c13-127">Pakken indeholder fem løsninger:</span><span class="sxs-lookup"><span data-stu-id="f2c13-127">The package contains five solutions:</span></span>

    + <span data-ttu-id="f2c13-128">Dynamics365Company</span><span class="sxs-lookup"><span data-stu-id="f2c13-128">Dynamics365Company</span></span>
    + <span data-ttu-id="f2c13-129">CurrencyExchangeRates</span><span class="sxs-lookup"><span data-stu-id="f2c13-129">CurrencyExchangeRates</span></span>
    + <span data-ttu-id="f2c13-130">Dynamics365FinanceAndOperationsCommon</span><span class="sxs-lookup"><span data-stu-id="f2c13-130">Dynamics365FinanceAndOperationsCommon</span></span>
    + <span data-ttu-id="f2c13-131">Dynamics365FinanceCommon</span><span class="sxs-lookup"><span data-stu-id="f2c13-131">Dynamics365FinanceCommon</span></span>
    + <span data-ttu-id="f2c13-132">Dynamics365SupplyChainCommon</span><span class="sxs-lookup"><span data-stu-id="f2c13-132">Dynamics365SupplyChainCommon</span></span>

3. <span data-ttu-id="f2c13-133">Følg udførelsesrækkefølgen for [synkronisering af indledende referencedata](dual-write-initial.md).</span><span class="sxs-lookup"><span data-stu-id="f2c13-133">Follow the execution order for [synchronizing initial reference data](dual-write-initial.md).</span></span>
4. <span data-ttu-id="f2c13-134">Hvis du støder på problemer med dobbeltskrivningssynkronisering, skal du se [Fejlfindingsvejledning til dataintegration](dual-write-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="f2c13-134">If you encounter dual-write synchronization issues, see the [Troubleshooting guide for data integration](dual-write-troubleshooting.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f2c13-135">Du kan ikke køre dobbeltskrivning og [Kundeemne til kontanter](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) side om side.</span><span class="sxs-lookup"><span data-stu-id="f2c13-135">You can’t run dual-write and [Prospect to cash](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) side-by-side.</span></span> <span data-ttu-id="f2c13-136">Hvis du kører løsningen Kundeemne til kontanter, skal du afinstallere den.</span><span class="sxs-lookup"><span data-stu-id="f2c13-136">If you're running the Prospect to cash solution, you must uninstall it.</span></span> <span data-ttu-id="f2c13-137">Du skal også deaktivere de skabeloner til dobbeltskrivning af debitorer og kreditorer, der er en del af løsningen Kundeemne til kontanter.</span><span class="sxs-lookup"><span data-stu-id="f2c13-137">You must also disable the customer and vendor dual-write templates that are part of the Prospect to cash solution.</span></span>
