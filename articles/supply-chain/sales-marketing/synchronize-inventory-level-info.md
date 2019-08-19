---
title: Synkronisere lagerniveauoplysninger fra Finance and Operations til Field Service
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere oplysninger på lagerniveau fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 05/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 6b56eb545f87c31ef30d6a897f48539068583486
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843427"
---
# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a>Synkronisere lagerniveauoplysninger fra Finance and Operations til Field Service 

[!include[banner](../includes/banner.md)]

I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere oplysninger på lagerniveau fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.

[![Synkronisering af forretningsprocesser mellem Finance and Operations og Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)

## <a name="templates-and-tasks"></a>Skabeloner og opgaver
Følgende skabelon og underliggende opgaver bruges til at synkronisere disponible lagerbeholdningsniveauer fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.

**Skabelon i dataintegration**
- Produktlager (Fin and Ops til Field Service)
  
**Opgave i dataintegrationsprojekt**
- Produktlager

Følgende synkroniseringsopgaver kræves, før lagerniveauer kan synkroniseres:
- Lagersteder (Fin and Ops til Field Service) 
- Field Service-produkter med lagerenhed (Fin and Ops til salg) 

## <a name="entity-set"></a>Enhedssæt

| Field Service                      | Finance and Operations                 |
|------------------------------------|----------------------------------------|
| msdynce_externalproductinventories | CDS Disponibelt lager efter lagersted     |

## <a name="entity-flow"></a>Enhedsflow
Lagerniveauoplysninger fra Finance and Operations sendes til Field Service for udvalgte produkter. Lagerniveauoplysningerne omfatter: 
- Disponibelt antal (aktuelt registreret fysisk antal, der findes på lagerstedet)
- Antal i bestilling (samlet registrerede antal i ordre, f.eks. salgsordrer)
- Bestilt antal (samlet registrerede bestilte antal, f.eks. indkøbsordrer)

Disse oplysninger hentes pr. frigivet produkt for hvert lagersted og synkroniseres efter ændringssporing, når lagerniveauet ændres.

I Field Service opretter integrationsløsningen lagerkladder for deltaet, så niveauerne i Field Service svarer til niveauerne i Finance and Operations.

Finance and Operations fungerer som master for lagerniveauer. Det er derfor vigtigt at konfigurere integration for arbejdsordrer, overførsler og reguleringer fra Field Service til Finance and Operations, hvis disse funktioner bruges i Field Service, sammen med synkronisering af lagerniveauer fra Finance and Operations.

De produkter og lagersteder, hvor lagerniveauer administreres fra Finance and Operations, kan kontrolleres med Avanceret forespørgsel og filtrering (Power-forespørgsel).

> [!NOTE]
> Det er muligt at oprette flere lagersteder i Field Service (med **Vedligeholdes eksternt = Nej**) og derefter knytte dem til et enkelt lagersted i Finance and Operations, med funktionen Avanceret forespørgsel og filtrering. Dette bruges i situationer, hvor Field Service skal mestre det detaljerede lagerniveau og kun sende opdateringer til Finance and Operations. I dette tilfælde modtager Field Service ikke lagerniveauopdateringer fra Finance and Operations. Du kan se flere oplysninger i [Synkroniser lagerreguleringer fra Field Service til Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) og [Synkronisere arbejdsordrer i Field Service med salgsordrer, der er knyttet til projektet i Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

## <a name="field-service-crm-solution"></a>CRM-løsning til Field Service
Enheden **Eksternt produktlager** bruges kun til backend i integrationen. Denne enhed modtager lagerniveauværdierne fra Finance and Operations i integrationen og ændrer derefter disse værdier til manuelle lagerkladder, der derefter ændrer lagerprodukterne på lagerstedet.

## <a name="prerequisites-and-mapping-setup"></a>Forudsætninger og tilknytningsopsætning

### <a name="data-integration"></a>Dataintegration
For at projektet kan fungere skal du sørge for, at integrationsnøglen er opdateret til msdynce_externalproductinventories.
1.  Gå til **Dataintegration > Forbindelsessæt**.
2.  Vælg det anvendte forbindelsessæt.
3.  Kontroller, at følgende nøgler er føjet til msdynce_externalproductinventories, under fanen **Integrationsnøgle**:
      - msdynce_productnumber (produktnummer)
      - msdynce_warehouseid (lagersteds-ID)
      
### <a name="data-integration-project"></a>Dataintegrationsprojekt
Du kan anvende filtre i Avanceret forespørgsel og filtrering, så kun bestemte produkter og lagersteder sender lagerniveauoplysninger fra Finance and Operations til Field Service.

## <a name="template-mapping-in-data-integration"></a>Skabelontilknytning i dataintegration

### <a name="product-inventory-fin-and-ops-to-field-service-product-inventory"></a>Produktlager (Fin and Ops til Field Service): produktlager

[![Skabelontilknytning i dataintegration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)
