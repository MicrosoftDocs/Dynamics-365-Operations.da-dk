---
title: Synkronisere oplysninger på lagerniveau fra Supply Chain Management til Field Service
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere oplysninger på lagerniveau fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.
author: ChristianRytt
manager: tfehr
ms.date: 05/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 1228339c12d26f7b91875d15f0daa8da2869cba0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215901"
---
# <a name="synchronize-inventory-level-information-from-supply-chain-management-to-field-service"></a>Synkronisere oplysninger på lagerniveau fra Supply Chain Management til Field Service 

[!include[banner](../includes/banner.md)]

I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere oplysninger på lagerniveau fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.

[![Synkronisering af forretningsprocesser mellem Supply Chain Management og Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)

## <a name="templates-and-tasks"></a>Skabeloner og opgaver
Følgende skabelon og underliggende opgaver bruges til at synkronisere niveauer af disponibel lagerbeholdning fra Supply Chain Management til Field Service.

**Skabelon i dataintegration**
- Produktlager (Supply Chain Management til Field Service)
  
**Opgave i dataintegrationsprojekt**
- Produktlager

Følgende synkroniseringsopgaver kræves, før lagerniveauer kan synkroniseres:
- Lagersteder (Supply Chain Management til Field Service) 
- Field Service-produkter med lagerenhed (Supply Chain Management til Sales) 

## <a name="entity-set"></a>Enhedssæt

| Field Service                      | Supply Chain Management                |
|------------------------------------|----------------------------------------|
| msdynce_externalproductinventories | CDS Disponibelt lager efter lagersted     |

## <a name="entity-flow"></a>Enhedsflow
Lagerniveauoplysninger fra Finance and Operations sendes til Field Service for udvalgte produkter. Lagerniveauoplysningerne omfatter: 
- Disponibelt antal (aktuelt registreret fysisk antal, der findes på lagerstedet)
- Antal i bestilling (samlet registrerede antal i ordre, f.eks. salgsordrer)
- Bestilt antal (samlet registrerede bestilte antal, f.eks. indkøbsordrer)

Disse oplysninger hentes pr. frigivet produkt for hvert lagersted og synkroniseres efter ændringssporing, når lagerniveauet ændres.

I Field Service opretter integrationsløsningen lagerkladder for deltaet, så niveauerne i Field Service svarer til niveauerne i Supply Chain Management.

Supply Chain Management fungerer som master for lagerniveauer. Det er derfor vigtigt at konfigurere integration for arbejdsordrer, overførsler og reguleringer fra Field Service til Supply Chain Management, hvis disse funktioner bruges i Field Service, sammen med synkronisering af lagerniveauer fra Supply Chain Management.

De produkter og lagersteder, hvor lagerniveauer administreres fra Supply Chain Management, kan kontrolleres med Avanceret forespørgsel og filtrering (Power Query).

> [!NOTE]
> Det er muligt at oprette flere lagersteder i Field Service (med **Vedligeholdes eksternt = Nej**) og derefter knytte dem til et enkelt lagersted i Supply Chain Management, med funktionen Avanceret forespørgsel og filtrering. Dette bruges i situationer, hvor Field Service skal mestre det detaljerede lagerniveau og kun sende opdateringer til Supply Chain Management. I dette tilfælde modtager Field Service ikke lagerniveauopdateringer fra Supply Chain Management. Du kan se flere oplysninger i [Synkroniser lagerreguleringer fra Field Service til Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) og [Synkronisere arbejdsordrer i Field Service med salgsordrer, der er knyttet til projektet i Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

## <a name="field-service-crm-solution"></a>CRM-løsning til Field Service
Enheden **Eksternt produktlager** bruges kun til backend i integrationen. Denne enhed modtager lagerniveauværdierne fra Supply Chain Management i integrationen og ændrer derefter disse værdier til manuelle lagerkladder, der derefter ændrer lagerprodukterne på lagerstedet.

## <a name="prerequisites-and-mapping-setup"></a>Forudsætninger og tilknytningsopsætning

### <a name="data-integration"></a>Dataintegration
For at projektet kan fungere skal du sørge for, at integrationsnøglen er opdateret til msdynce_externalproductinventories.
1.  Gå til **Dataintegration > Forbindelsessæt**.
2.  Vælg det anvendte forbindelsessæt.
3.  Kontroller, at følgende nøgler er føjet til msdynce_externalproductinventories, under fanen **Integrationsnøgle**:
      - msdynce_productnumber (produktnummer)
      - msdynce_warehouseid (lagersteds-ID)
      
### <a name="data-integration-project"></a>Dataintegrationsprojekt
Du kan anvende filtre i Avanceret forespørgsel og filtrering, så kun bestemte produkter og lagersteder sender lagerniveauoplysninger fra Supply Chain Management til Field Service.

## <a name="template-mapping-in-data-integration"></a>Skabelontilknytning i dataintegration

### <a name="product-inventory-supply-chain-management-to-field-service-product-inventory"></a>Produktlager (Supply Chain Management til Field Service): Produktlager

[![Skabelontilknytning i dataintegration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)
