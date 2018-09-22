---
title: Integration med Microsoft Dynamics 365 for Field Service
description: Dette emne indeholder en oversigt over integrationen med Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 08/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: d20bc3519096f1035d26f89d42aa7e8f0fc368cd
ms.openlocfilehash: cb21667021a32381fd8038e1c9f0182b05622e3d
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2018

---


# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a><span data-ttu-id="5e9d9-103">Integration med Microsoft Dynamics 365 for Field Service</span><span class="sxs-lookup"><span data-stu-id="5e9d9-103">Integration with Microsoft Dynamics 365 for Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="5e9d9-104">Microsoft Dynamics 365 for Finance and Operations muliggør synkronisering af forretningsprocesser mellem Finance and Operations og Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="5e9d9-104">Microsoft Dynamics 365 for Finance and Operations enables synchronization of business processes between Finance and Operations and Microsoft Dynamics 365 for Field Service.</span></span> <span data-ttu-id="5e9d9-105">Integrationsmulighederne konfigureres ved hjælp af dataintegratorskabeloner, der kan udvides, og den fælles dataservice (CDS) med henblik på at muliggøre synkronisering af forretningsprocesser.</span><span class="sxs-lookup"><span data-stu-id="5e9d9-105">The integration scenarios are configured by using extensible Data integrator templates and the Common Data Service (CDS) to enable the synchronization of business processes.</span></span>

<span data-ttu-id="5e9d9-106">[![Synkronisering af forretningsprocesser mellem Finance and Operations og Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="5e9d9-106">[![Synchronization of business processes between Finance and Operations and Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)</span></span>

<span data-ttu-id="5e9d9-107">Den første fase af integrationen mellem Field Service og Finance and Operations fokuserer på at gøre det muligt at fakturere arbejdsordrer og aftaler fra Field Service i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5e9d9-107">The first phase  of the integration between Field Service and Finance and Operations is focused on enabling work orders and agreements in Field Service to be invoiced in Finance and Operations.</span></span> <span data-ttu-id="5e9d9-108">Den understøttede arbejdsgang begynder i Field Service, hvor oplysninger fra arbejdsordrer synkroniseres til Finance and Operations som salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="5e9d9-108">The supported flow starts in Field Service, where information from work orders is synchronized to Finance and Operations as sales orders.</span></span> <span data-ttu-id="5e9d9-109">I Finance and Operations faktureres salgsordrer for at generere fakturadokumenter.</span><span class="sxs-lookup"><span data-stu-id="5e9d9-109">In Finance and Operations, the sales orders are invoiced to generate invoice documents.</span></span> <span data-ttu-id="5e9d9-110">Derudiver synkroniseres aftalefakturaer i Field Service til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5e9d9-110">In addition, the information from Field Service agreement invoices is synchronized to Finance and Operations.</span></span> <span data-ttu-id="5e9d9-111">Microsoft Dynamics 365-dataintegratoren synkroniserer data ved hjælp af projekter, der kan tilpasses.</span><span class="sxs-lookup"><span data-stu-id="5e9d9-111">The Microsoft Dynamics 365 Data integrator synchronizes data by using customizable projects.</span></span> <span data-ttu-id="5e9d9-112">Standardskabeloner kan anvendes til at oprette brugerdefinerede integrationsprojekter, hvor flere standardfelter og brugerdefinerede felter, foruden enheder, kan tilknyttes for at justere integrationen og opfylde bestemte krav.</span><span class="sxs-lookup"><span data-stu-id="5e9d9-112">Standard templates can be used to create custom integration projects where additional standard and custom fields, and also entities, can be mapped to adjust the integration and meet specific requirements.</span></span>

<span data-ttu-id="5e9d9-113">Den første fase i integrationen mellem Field Service og Finance and Operations muliggør synkronisering af følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="5e9d9-113">The first phase of the integration between Field Service and Finance and Operations enables synchronization of the following items:</span></span>

- [<span data-ttu-id="5e9d9-114">Produkter i Finance and Operations til produkter i Field Service, som omfatter produkttypeoplysninger</span><span class="sxs-lookup"><span data-stu-id="5e9d9-114">Products in Finance and Operations to products in Field Service that include Product Type information</span></span>](field-service-product.md)
- [<span data-ttu-id="5e9d9-115">Arbejdsordrer i Field Service til salgsordrer i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5e9d9-115">Work orders in Field Service to sales orders in Finance and Operations</span></span>](field-service-work-order.md)
- [<span data-ttu-id="5e9d9-116">Fakturaer i Field Service til fritekstfakturaer i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5e9d9-116">Invoices in Field Service to free text invoices in Finance and Operations</span></span>](field-service-invoice.md)

<span data-ttu-id="5e9d9-117">Hvis du vil se et eksempel på, hvordan du synkroniserer en arbejdsordre mellem Field Service og Finance and Operations, skal du se korte YouTube-video [Sådan synkroniserer du en arbejdsordre med Microsoft Dynamics 365-integration](https://www.youtube.com/watch?v=46ylO7raZAo).</span><span class="sxs-lookup"><span data-stu-id="5e9d9-117">To see an example of how you can synchronize a work order between Field Service and Finance and Operations, watch the short YouTube video [How to synchronize a work order with Microsoft Dynamics 365 Integration](https://www.youtube.com/watch?v=46ylO7raZAo).</span></span>

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="5e9d9-118">Systemkrav til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5e9d9-118">System requirements for Finance and Operations</span></span>
<span data-ttu-id="5e9d9-119">Integration i Field Service understøtter følgende versioner:</span><span class="sxs-lookup"><span data-stu-id="5e9d9-119">Field Service integration supports the following versions:</span></span>

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a><span data-ttu-id="5e9d9-120">Dynamics 365 for Finance and Operations version 8.0 (april 2018) eller nyere</span><span class="sxs-lookup"><span data-stu-id="5e9d9-120">Dynamics 365 for Finance and Operations version 8.0 (April 2018) or later</span></span>

- <span data-ttu-id="5e9d9-121">Dynamics 365 for Finance and Operations version 8.0 (april 2018) blev frigivet i april 2018, og programmet har buildnummeret 8.0.30.8020 med platformsopdatering 15 (7.0.4841.35234).</span><span class="sxs-lookup"><span data-stu-id="5e9d9-121">Dynamics 365 for Finance and Operations version 8.0 (April 2018) was released in April 2018 and has an application build number 8.0.30.8020 with Platform Update 15 (7.0.4841.35234).</span></span> 

## <a name="system-requirements-for-field-service"></a><span data-ttu-id="5e9d9-122">Systemkravene til Field Service</span><span class="sxs-lookup"><span data-stu-id="5e9d9-122">System requirements for Field Service</span></span>
<span data-ttu-id="5e9d9-123">Hvis du vil bruge integrationsløsningen i Field Service, skal du installere følgende komponenter:</span><span class="sxs-lookup"><span data-stu-id="5e9d9-123">To use the Field Service integration solution, you must install the following components:</span></span>

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a><span data-ttu-id="5e9d9-124">Microsoft Dynamics 365 for Field Service 9.0 eller nyere</span><span class="sxs-lookup"><span data-stu-id="5e9d9-124">Microsoft Dynamics 365 for Field Service 9.0 or later</span></span>

- <span data-ttu-id="5e9d9-125">Dynamics 365 for Field Service version 1612 (9.0.1.733) (DB 9.0.1.733) online eller en nyere version.</span><span class="sxs-lookup"><span data-stu-id="5e9d9-125">Dynamics 365 for Field Service version 1612 (9.0.1.733) (DB 9.0.1.733) online or a later version.</span></span>
- <span data-ttu-id="5e9d9-126">Løsningen Kundeemne til kontanter (P2C) til Dynamics 365, version 1.15.0.1 eller en nyere version.</span><span class="sxs-lookup"><span data-stu-id="5e9d9-126">Prospect to Cash (P2C) solution for Dynamics 365, version 1.15.0.1 or a later version.</span></span> <span data-ttu-id="5e9d9-127">Løsningen kan hentes fra [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span><span class="sxs-lookup"><span data-stu-id="5e9d9-127">The solution is available for download from [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>
- <span data-ttu-id="5e9d9-128">Integrationsløsningen i Field Service til Dynamics 365, version 1.0.0.0 eller en nyere version.</span><span class="sxs-lookup"><span data-stu-id="5e9d9-128">Field Service integration solution for Dynamics 365, version 1.0.0.0 or a later version.</span></span> <span data-ttu-id="5e9d9-129">Løsningen kan hentes fra [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.p2cfieldserviceintegration).</span><span class="sxs-lookup"><span data-stu-id="5e9d9-129">The solution is available for download from [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.p2cfieldserviceintegration).</span></span>

