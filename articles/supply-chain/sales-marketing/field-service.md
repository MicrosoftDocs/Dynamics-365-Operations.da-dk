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
ms.sourcegitcommit: a57e23691a6b4d48c6b8dd6d1f61fc9730365b39
ms.openlocfilehash: 0c1268d2fddcf7b28ecfc3197f21e9d30a5a5855
ms.contentlocale: da-dk
ms.lasthandoff: 05/31/2018

---


# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a>Integration med Microsoft Dynamics 365 for Field Service

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations muliggør synkronisering af forretningsprocesser mellem Finance and Operations og Microsoft Dynamics 365 for Field Service. Integrationsmulighederne konfigureres ved hjælp af dataintegratorskabeloner, der kan udvides, og den fælles dataservice (CDS) med henblik på at muliggøre synkronisering af forretningsprocesser.

[![Synkronisering af forretningsprocesser mellem Finance and Operations og Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)

Den første fase af integrationen mellem Field Service og Finance and Operations fokuserer på at gøre det muligt at fakturere arbejdsordrer og aftaler fra Field Service i Finance and Operations. Den understøttede arbejdsgang begynder i Field Service, hvor oplysninger fra arbejdsordrer synkroniseres til Finance and Operations som salgsordrer. I Finance and Operations faktureres salgsordrer for at generere fakturadokumenter. Derudiver synkroniseres aftalefakturaer i Field Service til Finance and Operations. Microsoft Dynamics 365-dataintegratoren synkroniserer data ved hjælp af projekter, der kan tilpasses. Standardskabeloner kan anvendes til at oprette brugerdefinerede integrationsprojekter, hvor flere standardfelter og brugerdefinerede felter, foruden enheder, kan tilknyttes for at justere integrationen og opfylde bestemte krav.

Den første fase i integrationen mellem Field Service og Finance and Operations muliggør synkronisering af følgende elementer:

- [Produkter i Finance and Operations til produkter i Field Service, som omfatter produkttypeoplysninger](field-service-product.md)
- [Arbejdsordrer i Field Service til salgsordrer i Finance and Operations](field-service-work-order.md)
- [Fakturaer i Field Service til fritekstfakturaer i Finance and Operations](field-service-invoice.md)

Hvis du vil se et eksempel på, hvordan du synkroniserer en arbejdsordre mellem Field Service og Finance and Operations, skal du se korte YouTube-video [Synkronisere en arbejdsordre mellem Dynamics 365 for Field Service og Finance and Operations](https://www.youtube.com/watch?v=hAB4TDVMjxU).

[![](https://img.youtube.com/vi/hAB4TDVMjxU/0.jpg)](https://www.youtube.com/watch?v=hAB4TDVMjxU)

## <a name="system-requirements-for-finance-and-operations"></a>Systemkrav til Finance and Operations
Integration i Field Service understøtter følgende versioner:

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a>Dynamics 365 for Finance and Operations version 8.0 (april 2018) eller nyere

- Dynamics 365 for Finance and Operations version 8.0 (april 2018) blev frigivet i april 2018, og programmet har buildnummeret 8.0.30.8020 med platformsopdatering 15 (7.0.4841.35234). 

## <a name="system-requirements-for-field-service"></a>Systemkravene til Field Service
Hvis du vil bruge integrationsløsningen i Field Service, skal du installere følgende komponenter:

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a>Microsoft Dynamics 365 for Field Service 9.0 eller nyere

- Dynamics 365 for Field Service version 1612 (9.0.1.733) (DB 9.0.1.733) online eller en nyere version.
- Løsningen Kundeemne til kontanter (P2C) til Dynamics 365, version 1.15.0.1 eller en nyere version. Løsningen kan hentes fra [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
- Integrationsløsningen i Field Service til Dynamics 365, version 1.0.0.0 eller en nyere version. Løsningen kan hentes fra [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.p2cfieldserviceintegration).

