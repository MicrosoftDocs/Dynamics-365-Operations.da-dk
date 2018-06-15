---
title: Integration med Microsoft Dynamics 365 for Field Service
description: Dette emne indeholder en oversigt over integrationen med Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 04/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 03a932652cdd93b2a5917d0fca72809d1648b678
ms.openlocfilehash: b1acf0b64914a3199fcf44f8377e32b26f0af99e
ms.contentlocale: da-dk
ms.lasthandoff: 04/25/2018

---


# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a><span data-ttu-id="e8585-103">Integration med Microsoft Dynamics 365 for Field Service</span><span class="sxs-lookup"><span data-stu-id="e8585-103">Integration with Microsoft Dynamics 365 for Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e8585-104">Microsoft Dynamics 365 for Finance and Operations muliggør synkronisering af forretningsprocesser mellem Finance and Operations og Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="e8585-104">Microsoft Dynamics 365 for Finance and Operations enables synchronization of business processes between Finance and Operations and Microsoft Dynamics 365 for Field Service.</span></span> <span data-ttu-id="e8585-105">Integrationsmulighederne konfigureres ved hjælp af dataintegratorskabeloner, der kan udvides, og den fælles dataservice (CDS) med henblik på at muliggøre synkronisering af forretningsprocesser.</span><span class="sxs-lookup"><span data-stu-id="e8585-105">The integration scenarios are configured by using extensible Data integrator templates and the Common Data Service (CDS) to enable the synchronization of business processes.</span></span>

<span data-ttu-id="e8585-106">[![Synkronisering af forretningsprocesser mellem Finance and Operations og Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="e8585-106">[![Synchronization of business processes between Finance and Operations and Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)</span></span>

<span data-ttu-id="e8585-107">Den første fase af integrationen mellem Field Service og Finance and Operations fokuserer på at gøre det muligt at fakturere arbejdsordrer og aftaler fra Field Service i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e8585-107">The first phase  of the integration between Field Service and Finance and Operations is focused on enabling work orders and agreements in Field Service to be invoiced in Finance and Operations.</span></span> <span data-ttu-id="e8585-108">Den understøttede arbejdsgang begynder i Field Service, hvor oplysninger fra arbejdsordrer synkroniseres til Finance and Operations som salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="e8585-108">The supported flow starts in Field Service, where information from work orders is synchronized to Finance and Operations as sales orders.</span></span> <span data-ttu-id="e8585-109">I Finance and Operations faktureres salgsordrer for at generere fakturadokumenter.</span><span class="sxs-lookup"><span data-stu-id="e8585-109">In Finance and Operations, the sales orders are invoiced to generate invoice documents.</span></span> <span data-ttu-id="e8585-110">Derudiver synkroniseres aftalefakturaer i Field Service til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e8585-110">In addition, the information from Field Service agreement invoices is synchronized to Finance and Operations.</span></span> <span data-ttu-id="e8585-111">Microsoft Dynamics 365-dataintegratoren synkroniserer data ved hjælp af projekter, der kan tilpasses.</span><span class="sxs-lookup"><span data-stu-id="e8585-111">The Microsoft Dynamics 365 Data integrator synchronizes data by using customizable projects.</span></span> <span data-ttu-id="e8585-112">Standardskabeloner kan anvendes til at oprette brugerdefinerede integrationsprojekter, hvor flere standardfelter og brugerdefinerede felter, foruden enheder, kan tilknyttes for at justere integrationen og opfylde bestemte krav.</span><span class="sxs-lookup"><span data-stu-id="e8585-112">Standard templates can be used to create custom integration projects where additional standard and custom fields, and also entities, can be mapped to adjust the integration and meet specific requirements.</span></span>

<span data-ttu-id="e8585-113">Den første fase i integrationen mellem Field Service og Finance and Operations muliggør synkronisering af følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="e8585-113">The first phase of the integration between Field Service and Finance and Operations enables synchronization of the following items:</span></span>

- [<span data-ttu-id="e8585-114">Produkter i Finance and Operations til produkter i Field Service, som omfatter produkttypeoplysninger</span><span class="sxs-lookup"><span data-stu-id="e8585-114">Products in Finance and Operations to products in Field Service that include Product Type information</span></span>](field-service-product.md)
- [<span data-ttu-id="e8585-115">Arbejdsordrer i Field Service til salgsordrer i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e8585-115">Work orders in Field Service to sales orders in Finance and Operations</span></span>](field-service-work-order.md)
- [<span data-ttu-id="e8585-116">Fakturaer i Field Service til fritekstfakturaer i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e8585-116">Invoices in Field Service to free text invoices in Finance and Operations</span></span>](field-service-invoice.md)

<span data-ttu-id="e8585-117">Du kan se et eksempel på, hvordan du kan synkronisere en arbejdsordre mellem Field Service og Finance and Operations, i denne korte YouTube-video:</span><span class="sxs-lookup"><span data-stu-id="e8585-117">To see an example of how you can synchronize a work order between Field Service and Finance and Operations, watch the short YouTube video:</span></span>

> [!Video https://www.youtube.com/embed/hAB4TDVMjxU]

[<span data-ttu-id="e8585-118">Synkronisere en arbejdsordre mellem Field Service og Finance and Operations (YouTube-video)</span><span class="sxs-lookup"><span data-stu-id="e8585-118">Synchronize a work order between Field Service and Finance and Operations (YouTube video)</span></span>](https://youtu.be/hAB4TDVMjxU)

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="e8585-119">Systemkrav til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e8585-119">System requirements for Finance and Operations</span></span>
<span data-ttu-id="e8585-120">Integration i Field Service understøtter følgende versioner:</span><span class="sxs-lookup"><span data-stu-id="e8585-120">Field Service integration supports the following versions:</span></span>

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a><span data-ttu-id="e8585-121">Dynamics 365 for Finance and Operations version 8.0 (april 2018) eller nyere</span><span class="sxs-lookup"><span data-stu-id="e8585-121">Dynamics 365 for Finance and Operations version 8.0 (April 2018) or later</span></span>

- <span data-ttu-id="e8585-122">Dynamics 365 for Finance and Operations version 8.0 (april 2018) blev frigivet i april 2018, og programmet har buildnummeret 8.0.30.8020 med platformsopdatering 15 (7.0.4841.35234).</span><span class="sxs-lookup"><span data-stu-id="e8585-122">Dynamics 365 for Finance and Operations version 8.0 (April 2018) was released in April 2018 and has an application build number 8.0.30.8020 with Platform Update 15 (7.0.4841.35234).</span></span> 

## <a name="system-requirements-for-field-service"></a><span data-ttu-id="e8585-123">Systemkravene til Field Service</span><span class="sxs-lookup"><span data-stu-id="e8585-123">System requirements for Field Service</span></span>
<span data-ttu-id="e8585-124">Hvis du vil bruge integrationsløsningen i Field Service, skal du installere følgende komponenter:</span><span class="sxs-lookup"><span data-stu-id="e8585-124">To use the Field Service integration solution, you must install the following components:</span></span>

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a><span data-ttu-id="e8585-125">Microsoft Dynamics 365 for Field Service 9.0 eller nyere</span><span class="sxs-lookup"><span data-stu-id="e8585-125">Microsoft Dynamics 365 for Field Service 9.0 or later</span></span>

- <span data-ttu-id="e8585-126">Dynamics 365 for Field Service version 1612 (9.0.1.733) (DB 9.0.1.733) online eller en nyere version.</span><span class="sxs-lookup"><span data-stu-id="e8585-126">Dynamics 365 for Field Service version 1612 (9.0.1.733) (DB 9.0.1.733) online or a later version.</span></span>
- <span data-ttu-id="e8585-127">Løsningen Kundeemne til kontanter (P2C) til Dynamics 365, version 1.15.0.1 eller en nyere version.</span><span class="sxs-lookup"><span data-stu-id="e8585-127">Prospect to Cash (P2C) solution for Dynamics 365, version 1.15.0.1 or a later version.</span></span> <span data-ttu-id="e8585-128">Løsningen kan hentes fra [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span><span class="sxs-lookup"><span data-stu-id="e8585-128">The solution is available for download from [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>
- <span data-ttu-id="e8585-129">Integrationsløsningen i Field Service til Dynamics 365, version 1.0.0.0 eller en nyere version.</span><span class="sxs-lookup"><span data-stu-id="e8585-129">Field Service integration solution for Dynamics 365, version 1.0.0.0 or a later version.</span></span> <span data-ttu-id="e8585-130">Løsningen kan hentes fra [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.p2cfieldserviceintegration).</span><span class="sxs-lookup"><span data-stu-id="e8585-130">The solution is available for download from [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.p2cfieldserviceintegration).</span></span>
