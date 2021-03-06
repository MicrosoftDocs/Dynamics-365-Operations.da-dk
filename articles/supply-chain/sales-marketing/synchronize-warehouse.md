---
title: Synkronisere lagersteder fra Supply Chain Management til Field Service
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere lagersteder fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.
author: ChristianRytt
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: f302f780fa8ba3d387a71770024a1bf7ad42c4ef
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910251"
---
# <a name="synchronize-warehouses-from-supply-chain-management-to-field-service"></a>Synkronisere lagersteder fra Supply Chain Management til Field Service

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere lagersteder fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.

[![Synkronisering af forretningsprocesser mellem Supply Chain Management og Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)

## <a name="templates-and-tasks"></a>Skabeloner og opgaver
Følgende skabelon og underliggende opgaver bruges til at synkronisere lagersteder fra Supply Chain Management til Field Service.

**Skabelon i dataintegration**
- Lagersteder (Supply Chain Management til Field Service)

**Opgave i dataintegrationsprojekt**
- Lagersted

## <a name="table-set"></a>Tabelsæt
| Field Service    | Supply Chain Management                 |
|------------------|----------------------------------------|
| msdyn_warehouses | Lagersteder                             |

## <a name="table-flow"></a>Tabelflow
Lagersteder, der oprettes og vedligeholdes i Supply Chain Management, kan synkroniseres til Field Service via et Microsoft Dataverse-dataintegrationsprojekt. De lagersteder, du vil synkronisere til Field Service, kan styres med Avanceret forespørgsel og filtrering i projektet. Lagersteder, der synkroniseres fra Supply Chain Management, oprettes i Field Service med kolonnen **Vedligeholdes eksternt** indstillet til **Ja**, og posten skrivebeskyttes.

## <a name="field-service-crm-solution"></a>CRM-løsning til Field Service
For at understøtte integrationen mellem Field Service og Supply Chain Management kræves der yderligere funktionalitet fra CRM-løsningen i Field Service. I løsningen er kolonnen **Vedligeholdes eksternt** blevet føjet til tabellen **Lagersted (msdyn_warehouses)**. Denne kolonne bruges til at identificere, om lagerstedet håndteres fra Supply Chain Management, eller om det kun findes i Field Service. Indstillingerne for denne kolonne omfatter:
- **Ja** – Lagerstedet stammer fra Supply Chain Management, og det kan ikke redigeres i Sales.
- **Nej** – Lagerstedet er angivet direkte i Field Service og vedligeholdes her.

Kolonnen **Vedligeholdes eksternt** hjælper med at styre synkroniseringen af lagerniveauer, reguleringer, overførsler og brug i arbejdsordrer. Kun lagersteder, hvor **Vedligeholdes eksternt** er indstillet til **Ja**, kan bruges til at synkronisere direkte til det samme lagersted i andet system. 

> [!NOTE]
> Det er muligt at oprette flere lagersteder i Field Service (med **Vedligeholdes eksternt** = Nej) og derefter knytte dem til et enkelt lagersted med funktionen Avanceret forespørgsel og filtrering. Dette bruges i situationer, hvor Field Service skal mestre det detaljerede lagerniveau og kun sende opdateringer til Supply Chain Management. I dette tilfælde modtager Field Service ikke lagerniveauopdateringer fra Supply Chain Management. Du kan få flere oplysninger i [Synkroniser lagerreguleringer fra Field Service til Finance and Operations](/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) og i [Synkronisere arbejdsordrer i Field Service med salgsordrer, der er knyttet til projektet i Finance and Operations](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

## <a name="prerequisites-and-mapping-setup"></a>Forudsætninger og tilknytningsopsætning
### <a name="data-integration-project"></a>Dataintegrationsprojekt
Inden du synkroniserer lagerstederne, skal du sørge for at opdatere Avanceret forespørgsel og filtrering i projektet, så kun de lagersteder, du vil overføre fra Supply Chain Management til Field Service, medtages. Bemærk, at du skal bruge lagerstedet i Field Service og anvende det på arbejdsordrer, reguleringer og overførsler.  

Gør følgende for at sørge for, at der findes en **Integrationsnøgle** for **msdyn_warehouses**:
1. Gå til Dataintegration.
2. Vælg fanen **Forbindelsessæt**.
3. Vælg det forbindelsessæt, der bruges til synkronisering af arbejdsordre.
4. Vælg fanen **Integrationsnøgle**.
5. Find msdyn_warehouses, og kontroller, at nøglen **msdyn_name (navn)** er tilføjet. Hvis den ikke vises, skal du tilføje den ved at klikke på **Tilføj nøgle** og derefter klikke på **Gem** øverst på siden.

## <a name="template-mapping-in-data-integration"></a>Skabelontilknytning i dataintegration

Følgende illustration viser skabelontilknytningen i Dataintegration.

### <a name="warehouses-supply-chain-management-to-field-service-warehouse"></a>Lagersteder (Supply Chain Management til Field Service): Lagersted

[![Skabelontilknytning i dataintegration](./media/Warehouse1.png)](./media/Warehouse1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]