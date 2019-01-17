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
ms.sourcegitcommit: 95031534c43dc0578e258bc3e5376c429d72b0ab
ms.openlocfilehash: 673ab2a101cee1a3dbbb1249f582d959cecc7f7f
ms.contentlocale: da-dk
ms.lasthandoff: 12/23/2018

---

# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a>Integration med Microsoft Dynamics 365 for Field Service

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations muliggør synkronisering af forretningsprocesser mellem Finance and Operations og Microsoft Dynamics 365 for Field Service. Integrationsmulighederne konfigureres ved hjælp af dataintegratorskabeloner, der kan udvides, og den fælles dataservice (CDS) med henblik på at muliggøre synkronisering af forretningsprocesser.
Standardskabeloner kan anvendes til at oprette brugerdefinerede integrationsprojekter, hvor flere standardfelter og brugerdefinerede felter, foruden enheder, kan tilknyttes for at justere integrationen og opfylde forretningsbehov. 

Field Service-integrationen bygger på den eksisterende kundeemne til kontant-funktionalitet.

![Synkronisering af forretningsprocesser mellem Finance and Operations og Field Service](./media/field-service-integration.png)

Den første fase af integrationen mellem Field Service og Finance and Operations fokuserer på at gøre det muligt at fakturere arbejdsordrer og aftaler fra Field Service i Finance and Operations. Den understøttede arbejdsgang begynder i Field Service, hvor oplysninger fra arbejdsordrer synkroniseres til Finance and Operations som salgsordrer. I Finance and Operations faktureres salgsordrer for at generere fakturadokumenter. Derudiver synkroniseres aftalefakturaer i Field Service til Finance and Operations. Microsoft Dynamics 365-dataintegratoren synkroniserer data ved hjælp af projekter, der kan tilpasses. Standardskabeloner kan anvendes til at oprette brugerdefinerede integrationsprojekter, hvor flere standardfelter og brugerdefinerede felter, foruden enheder, kan tilknyttes for at justere integrationen og opfylde bestemte krav.

Den første fase i integrationen mellem Field Service og Finance and Operations muliggør synkronisering af følgende elementer:

- [Produkter i Finance and Operations til produkter i Field Service, som omfatter produkttypeoplysninger](field-service-product.md)
- [Arbejdsordrer i Field Service til salgsordrer i Finance and Operations](field-service-work-order.md)
- [Fakturaer i Field Service til fritekstfakturaer i Finance and Operations](field-service-invoice.md)

Hvis du vil se et eksempel på, hvordan du synkroniserer en arbejdsordre mellem Field Service og Finance and Operations, skal du se korte YouTube-video [Sådan synkroniserer du en arbejdsordre med Microsoft Dynamics 365-integration](https://www.youtube.com/watch?v=46ylO7raZAo).

## <a name="system-requirements-for-finance-and-operations"></a>Systemkrav til Finance and Operations
Integration i Field Service understøtter følgende versioner:

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a>Dynamics 365 for Finance and Operations version 8.0 (april 2018) eller nyere

- Dynamics 365 for Finance and Operations version 8.0 (april 2018) blev frigivet i april 2018, og programmet har buildnummeret 8.0.30.8020 med platformsopdatering 15 (7.0.4841.35234). 

## <a name="system-requirements-for-field-service"></a>Systemkravene til Field Service
Hvis du vil bruge integrationsløsningen i Field Service, skal du installere følgende komponenter:

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a>Microsoft Dynamics 365 for Field Service 9.0 eller nyere

- Dynamics 365 for Field Service version 1612 (9.0.1.733) (DB 9.0.1.733) online eller en nyere version.
- Løsningen Kundeemne til kontanter (P2C) til Dynamics 365, version 1.15.0.1 eller en nyere version. Løsningen kan hentes fra [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
- Integrationsløsningen i Field Service til Dynamics 365, version 1.0.0.0 eller en nyere version. Løsningen kan hentes fra [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegration).

# <a name="integration-with-microsoft-dynamics-365-for-field-service-including-inventory-and-project-information"></a>Integration med Microsoft Dynamics 365 for Field Service, inklusive lager- og projektoplysninger

Den ekstra funktionalitet i denne anden fase fokuserer på at give serviceteknikere indsigt i lageroplysninger fra Finance and Operations, så de kan opdatere lagerbeholdninger og foretage materialeoverførsler. Derudover har firmaer, der installerer og yder service til solgte varer, fordelen af bedre styring og synlighed i hele salgs- og serviceprocessen med integration fra projekter.

### <a name="functionality-includes-integration-of"></a>Funktionerne omfatter integration af:
- Oplysninger om lagersted
- Oplysninger om disponibel lagerbeholdning
- Lageroverførsler
- Lagerreguleringer
- Dynamics 365 for Finance and Operations-projekter, der er forbundet med Dynamics 365 for Field Service-serviceordrer
- Dynamics 365 for Field Service-arbejdsordrer med link til Dynamics 365 for Finance and Operations-projekter anvender dette projektnummer på Dynamics 365 for Finance and Operations-salgsordren, så der kan faktureres fra projektet. 

![Synkronisering af forretningsprocesser mellem Finance and Operations og Field Service](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-finance-and-operations-enables-synchronization-with-the-following-templates"></a>Den anden fase i integrationen mellem Field Service og Finance and Operations muliggør synkronisering med følgende skabeloner:
- Lagersteder (Finance and Operations til Field Service) - Lagersteder fra Finance and Operations til Field Service [Avanceret forespørgsel] 
- Produktlager (Finance and Operations til Field Service) - Lagerniveauoplysninger fra Finance and Operations til Field Service [Avanceret forespørgsel] 
- Lagerregulering (Field Service til Finance and Operations) - Lagerreguleringer fra Field Service til Finance and Operations [Avanceret forespørgsel] 
- Lageroverførsler (Field Service til Finance and Operations) - Lageroverførsler fra Field Service til Finance and Operations [Avanceret forespørgsel] 
- Projekter (Finance and Operations til Field Service) - Projektliste fra Finance and Operations til Field Service 
- Arbejdsordrer med projekt (Field Service til Finance and Operations) - Arbejdsordrer i Field Service til salgsordrer i Finance and Operations, med understøttelse af projekt [Avanceret forespørgsel] 
- Field Service-produkter med lagerenhed (Finance and Operations til Sales) - 'Salgbare frigivne produkter' i Finance and Operations til 'salgsprodukter' til Field Service, herunder lagerenhed. 

## <a name="system-requirements-for-finance-and-operations"></a>Systemkrav til Finance and Operations
Integration i Field Service understøtter følgende versioner:

- Dynamics 365 for Finance and Operations version 8.1.2 (december 2019) blev frigivet i december 2019, og programmet har buildnummeret 8.1.195 med platformsopdatering 22 (7.0.5095). 

## <a name="system-requirements-for-field-service"></a>Systemkravene til Field Service
Hvis du vil bruge integrationsløsningen i Field Service, skal du installere følgende komponenter:

- Field Service for Dynamics 365 (version 8.2.0.286) eller en nyere version i Dynamics 365 9.1.x - udgivet november 2018
- Løsningen Kundeemne til kontanter (P2C) til Dynamics 365, version 1.15.0.1 eller en nyere version. Løsningen kan hentes fra [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
- 'Field Service-integration, projekt og lager'-løsning til Dynamics 365, version 2.0.0.0 eller en nyere version. Løsningen kan hentes fra [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2).

