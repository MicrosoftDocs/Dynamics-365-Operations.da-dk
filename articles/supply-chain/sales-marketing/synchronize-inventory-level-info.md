---
title: Synkronisere lagerniveauoplysninger fra Finance and Operations til Field Service
description: Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere lagerniveauoplysninger fra Microsoft Dynamics 365 for Finance and Operations med Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: 3ccc4d406fa4f9800dcdf8697a91892408783196
ms.contentlocale: da-dk
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a>Synkronisere lagerniveauoplysninger fra Finance and Operations til Field Service 

[!include[banner](../includes/banner.md)]

Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere lagerniveauoplysninger fra Microsoft Dynamics 365 for Finance and Operations med Microsoft Dynamics 365 for Field Service.

[![Synkronisering af forretningsprocesser mellem Finance and Operations og Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)

## <a name="templates-and-tasks"></a>Skabeloner og opgaver
Følgende skabelon og underliggende opgaver bruges til at køre synkronisering af disponible lagerbeholdningsniveauer fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.

**Navnet på skabelonen i dataintegration:**
- Produktlager (Finance and Operations til Field Service)
  
**Navne på opgaverne i dataintegrationsprojektet:**
- Produktlager

Følgende synkroniseringsopgaver kræves, før lagerniveauer kan synkroniseres:
- Lagersteder (Finance and Operations til Field Service) 
- Field Service-produkter med lagerenhed (Finance and Operations til Sales) 

## <a name="entity-set"></a>Enhedssæt

| Field Service                      | Finance and Operations                 |
|------------------------------------|----------------------------------------|
| msdynce_externalproductinventories | CDS Disponibelt lager efter lagersted     |

## <a name="entity-flow"></a>Enhedsflow
Lagerniveauoplysninger fra Finance and Operations sendes til Field Service for udvalgte produkter. Lagerniveauoplysningerne omfatter: 
- Disponibelt antal (aktuelt registreret fysisk antal, der findes på lagerstedet)
- Antal i bestilling (samlet registrerede antal i ordre - dvs. salgsordrer)
- Bestilt antal (samlet registrerede bestilte antal - dvs. indkøbsordrer)

Disse oplysninger hentes pr. frigivet produkt for hvert lagersted og synkroniseres efter ændringssporing, når lagerniveauet ændres.

I Field Service opretter integrationsløsningen lagerkladder for deltaet for at få niveauerne i Field Service til at svare til niveauerne i Finance and Operations.

Finance and Operations fungerer som master for lagerniveauer. Så det er vigtigt at konfigurere integration for arbejdsordrer, overførsler og reguleringer fra Field Service til Finance and Operations, hvis disse funktioner bruges i Field Service, sammen med synkronisering af lagerniveauer fra Finance and Operations.

De produkter og lagersteder, hvor lagerniveauer administreres fra Finance and Operations, kan kontrolleres med Avanceret forespørgsel og filtrering (Power-forespørgsel).

Bemærk: Det er muligt at oprette flere lagersteder i Field Service (med Vedligeholdes eksternt = Nej) og derefter knytte dem til et enkelt lagersted i Finance and Operations, med funktionen Avanceret forespørgsel og filtrering. Dette bruges i situationer, hvor Field Service skal mestre det detaljerede lagerniveau og blot sende opdateringer til Finance and Operations. I dette tilfælde modtager Field Service ikke lagerniveauopdateringer fra Finance and Operations. Du kan se flere oplysninger i Synkroniser lagerreguleringer fra Field Service til Finance and Operations og Synkronisere arbejdsordrer i Field Service med salgsordrer, der er knyttet til projektet i Finance and Operations.

## <a name="field-service-crm-solution"></a>CRM-løsning til Field Service
Den eksterne produktlagerenhed er en ny enhed, der kun bruges til backend i integrationen. Den modtager lagerniveauværdierne fra Finance and Operations i integrationen og ændrer derefter disse værdier til manuelle lagerkladder, der derefter ændrer lagerprodukterne på lagerstedet. 

## <a name="prerequisites-and-mapping-setup"></a>Forudsætninger og tilknytningsopsætning

### <a name="in-the-data-integration-project"></a>I dataintegrationsprojektet
Anvend filtre i Avanceret forespørgsel og filtrering til at styre, at kun ønskede produkter og lagersteder sender lagerniveauoplysninger fra Finance and Operations til Field Service.

## <a name="template-mapping-in-data-integration"></a>Skabelontilknytning i dataintegration

### <a name="product-inventory-finance-and-operations-to-field-service-product-inventory"></a>Produktlager (Finance and Operations til Field Service): Produktlager

[![Skabelontilknytning i dataintegration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)

