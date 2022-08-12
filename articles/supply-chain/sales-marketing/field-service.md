---
title: Oversigt over integration med Microsoft Dynamics 365 Field Service
description: Denne artikel indeholder en oversigt over integrationen med Microsoft Dynamics 365 Field Service.
author: Henrikan
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: henrikan
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 12a9c57e2587150914c6087c041d63af9783c1f3
ms.sourcegitcommit: 12b3dbee905f8b2eb2e6c383c822a0fc9fccf063
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/01/2022
ms.locfileid: "9103691"
---
# <a name="integration-with-microsoft-dynamics-365-field-service-overview"></a>Oversigt over integration med Microsoft Dynamics 365 Field Service

[!include[banner](../includes/banner.md)]



Supply Chain Management gør det muligt at synkronisere forretningsprocesser mellem Dynamics 365 Supply Chain Management og Dynamics 365 Field Service. Integrationsmulighederne konfigureres ved hjælp af dataintegratorskabeloner, der kan udvides, og Microsoft Dataverse med henblik på at muliggøre synkronisering af forretningsprocesser.
Standardskabeloner kan anvendes til at oprette brugerdefinerede integrationsprojekter, hvor flere standard- og brugerdefinerede kolonner og tabeller kan tilknyttes for at justere integrationen og opfylde forretningsbehov. 

Field Service-integrationen bygger på den eksisterende kundeemne til kontant-funktionalitet.

![Synkronisering af forretningsprocesser mellem Supply Chain Management og Field Service.](./media/field-service-integration.png)

Den første fase af integrationen mellem Field Service og Supply Chain Management fokuserer på at gøre det muligt at fakturere arbejdsordrer og aftaler fra Field Service i Supply Chain Management. Den understøttede arbejdsgang begynder i Field Service, hvor oplysninger fra arbejdsordrer synkroniseres til Supply Chain Management som salgsordrer. I Supply Chain Management faktureres salgsordrerne, så fakturadokumenterne kan genereres. Endvidere synkroniseres aftalefakturaer i Field Service til Supply Chain Management. Microsoft Dynamics 365-dataintegratoren synkroniserer data ved hjælp af projekter, der kan tilpasses. Standardskabeloner kan anvendes til at oprette brugerdefinerede integrationsprojekter, hvor flere standardkolonner og brugerdefinerede kolonner, foruden tabeller, kan tilknyttes for at justere integrationen og opfylde bestemte krav.

Den første fase i integrationen mellem Field Service og Supply Chain Management muliggør synkronisering af følgende elementer:

- [Synkronisere produkter i Supply Chain Management med produkter i Field Service](field-service-product.md)
- [Synkroniser arbejdsordrer i Field Service til salgsordrer i Supply Chain Management](field-service-work-order.md)
- [Synkroniser aftalefakturaer i Field Service til fritekstfakturaer i Supply Chain Management](field-service-invoice.md)

Hvis du vil se et eksempel på, hvordan du synkroniserer en arbejdsordre mellem Field Service og Supply Chain Management, kan du se den korte YouTube-video [Sådan synkroniserer du en arbejdsordre med Microsoft Dynamics 365-integration](https://www.youtube.com/watch?v=46ylO7raZAo).

## <a name="integration-with-field-service-including-inventory-and-project-information"></a>Integration med Field Service, herunder lager- og projektoplysninger

Den ekstra funktionalitet i denne anden fase fokuserer på at give serviceteknikere indsigt i lageroplysninger fra Supply Chain Management, så de kan opdatere lagerbeholdninger og foretage materialeoverførsler. Derudover har firmaer, der installerer og yder service til solgte varer, fordelen af bedre styring og synlighed i hele salgs- og serviceprocessen med integration fra projekter.

### <a name="functionality-includes-integration-of"></a>Funktionerne omfatter integration af:
- Oplysninger om lagersted
- Oplysninger om disponibel lagerbeholdning
- Lageroverførsler
- Lagerreguleringer
- Supply Chain Management-projekter, der er forbundet med Dynamics 365 Field Service-arbejdsordrer
- Dynamics 365 Field Service-arbejdsordrer med tilknytning til Supply Chain Management-projekter anvender dette projektnummer på salgsordren, så der kan faktureres fra projektet. 

![Synkronisering af forretningsprocesser mellem Supply Chain Management og Field Service, herunder lager- og projektoplysninger.](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-supply-chain-management-enables-synchronization-with-the-following-templates"></a>Den anden fase i integrationen mellem Field Service og Supply Chain Management muliggør synkronisering med følgende skabeloner:
- Lagersteder (Supply Chain Management til Field Service) - Lagersteder fra Supply Chain Management til Field Service [Avanceret forespørgsel] 
- Produktlager (Supply Chain Management til Field Service) - Lagerniveauoplysninger fra Supply Chain Management til Field Service [Avanceret forespørgsel] 
- Lagerregulering (Field Service til Supply Chain Management) - Lagerreguleringer fra Field Service til Supply Chain Management [Avanceret forespørgsel] 
- Lageroverførsler (Field Service til Supply Chain Management) - Lageroverførsler fra Field Service til Supply Chain Management [Avanceret forespørgsel] 
- Projekter (Supply Chain Management til Field Service) - Projektliste fra Supply Chain Management til Field Service 
- Arbejdsordrer med projekt (Field Service til Supply Chain Management) - Arbejdsordrer i Field Service til salgsordrer i Supply Chain Management med understøttelse af projekt [Avanceret forespørgsel] 
- Field Service-produkter med lagerenhed (Supply Chain Management til Sales) - 'Salgbare frigivne produkter' i Supply Chain Management til 'Salgsprodukter' for Field Service, herunder lagerenhed. 

## <a name="system-requirements"></a>Systemkrav

### <a name="system-requirements-for-supply-chain-management"></a>Systemkrav til Supply Chain Management
Integration i Field Service understøtter følgende versioner:

- Dynamics 365 Finance and Operations version 8.1.2 (december 2018) blev frigivet i december 2018, og programmet har buildnummeret 8.1.195 med platformsopdatering 22 (7.0.5095). 

### <a name="system-requirements-for-field-service"></a>Systemkravene til Field Service
Hvis du vil bruge integrationsløsningen i Field Service, skal du installere følgende komponenter:

- Field Service (version 8.2.0.286) eller en nyere version i Dynamics 365 9.1.x - udgivet november 2018
- Løsningen Kundeemne til kontanter (P2C) til Dynamics 365, version 1.15.0.1 eller en nyere version. Løsningen kan hentes fra [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
- 'Field Service-integration, projekt og lager'-løsning til Dynamics 365, version 2.0.0.0 eller en nyere version. Løsningen kan hentes fra [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
