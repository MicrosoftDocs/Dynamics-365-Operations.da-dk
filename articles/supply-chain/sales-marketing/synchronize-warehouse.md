---
title: Synkronisere lagersteder fra Finance and Operations til Field Service
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere lagersteder fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 01/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 34cd18a18715d12d4002e6dbeee047467ed2a5ad
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "340309"
---
# <a name="synchronize-warehouses-from-finance-and-operations-to-field-service"></a>Synkronisere lagersteder fra Finance and Operations til Field Service

[!include[banner](../includes/banner.md)]

I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere lagersteder fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.

[![Synkronisering af forretningsprocesser mellem Finance and Operations og Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)

## <a name="templates-and-tasks"></a>Skabeloner og opgaver
Følgende skabelon og underliggende opgaver bruges til at køre synkronisering af lagersteder fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.

**Skabelon i dataintegration**
- Lagersteder (Finance and Operations til Field Service)

**Opgave i dataintegrationsprojekt**
- Lagersted

## <a name="entity-set"></a>Enhedssæt
| Field Service    | Finance and Operations                 |
|------------------|----------------------------------------|
| msdyn_warehouses | Lagersteder                             |

## <a name="entity-flow"></a>Enhedsflow
Lagersteder, der er oprettet og vedligeholdes i Finance and Operations, kan synkroniseres til Field Service via et Common Data Service-dataintegrationsprojekt (CDS). De lagersteder, du vil synkronisere til Field Service, kan styres med Avanceret forespørgsel og filtrering i projektet. Lagersteder, der synkroniseres fra Finance and Operations, oprettes i Field Service med feltet **Vedligeholdes eksternt indstillet** til **Ja**, og posten skrivebeskyttes.

## <a name="field-service-crm-solution"></a>CRM-løsning til Field Service
For at understøtte integrationen mellem Field Service og Finance and Operations, kræves yderligere funktioner fra CRM-løsningen i Field Service. I løsningen er feltet **Vedligeholdes eksternt** blevet føjet til enheden **Lagersted (msdyn_warehouses)**. Dette felt bruges til at identificere, om lagerstedet håndteres fra Finance and Operations, eller om det kun findes i Field Service. Indstillingerne for dette felt omfatter:
- **Ja** – Lagerstedet stammer fra Finance and Operations og kan ikke redigeres i Sales.
- **Nej** – Lagerstedet er angivet direkte i Field Service og vedligeholdes her.

Feltet **Vedligeholdes eksternt** hjælper med at styre synkroniseringen af lagerniveauer, reguleringer, overførsler og brug i arbejdsordrer. Kun lagersteder, hvor **Vedligeholdes eksternt** er indstillet til **Ja**, kan bruges til at synkronisere direkte til det samme lagersted i andet system. 

> [!NOTE]
> Det er muligt at oprette flere lagersteder i Field Service (med **Vedligeholdes eksternt** = Nej) og derefter knytte dem til et enkelt lagersted i Finance and Operations, med funktionen Avanceret forespørgsel og filtrering. Dette bruges i situationer, hvor Field Service skal mestre det detaljerede lagerniveau og blot sende opdateringer til Finance and Operations. I dette tilfælde modtager Field Service ikke lagerniveauopdateringer fra Finance and Operations. Du kan se flere oplysninger i [Synkroniser lagerreguleringer fra Field Service til Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) og [Synkronisere arbejdsordrer i Field Service med salgsordrer, der er knyttet til projektet i Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

## <a name="prerequisites-and-mapping-setup"></a>Forudsætninger og tilknytningsopsætning
### <a name="data-integration-project"></a>Dataintegrationsprojekt
Inden du synkroniserer lagerstederne, skal du sørge for at opdatere Avanceret forespørgsel og filtrering i projektet, så kun de lagersteder, du vil overføre fra Finance and Operations til Field Service, medtages. Bemærk, at du skal bruge lagerstedet i Field Service og anvende det på arbejdsordrer, reguleringer og overførsler.  

Gør følgende for at sørge for, at der findes en **Integrationsnøgle** for **msdyn_warehouses**:
1. Gå til Dataintegration.
2. Vælg fanen **Forbindelsessæt**.
3. Vælg det forbindelsessæt, der bruges til synkronisering af arbejdsordre.
4. Vælg fanen **Integrationsnøgle**.
5. Find msdyn_warehouses, og kontroller, at nøglen **msdyn_name (navn)** er tilføjet. Hvis den ikke vises, skal du tilføje den ved at klikke på **Tilføj nøgle** og derefter klikke på **Gem** øverst på siden.

## <a name="template-mapping-in-data-integration"></a>Skabelontilknytning i dataintegration

Følgende illustration viser skabelontilknytningen i Dataintegration.

### <a name="warehouses-finance-and-operations-to-field-service-warehouse"></a>Lagersteder (Finance and Operations til Field Service): Lagersted

[![Skabelontilknytning i dataintegration](./media/Warehouse1.png)](./media/Warehouse1.png)
