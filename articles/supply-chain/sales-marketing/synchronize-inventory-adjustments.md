---
title: Synkronisere lageroverførsler og reguleringer fra Field Service til Supply Chain Management
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere lagerreguleringer og overførsler fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.
author: ChristianRytt
manager: tfehr
ms.date: 04/30/2019
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
ms.openlocfilehash: ff64f28af570b792f73b51aa9caf06dd2445b2ca
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204418"
---
# <a name="synchronize-inventory-transfers-and-adjustments-from-field-service-to-supply-chain-management"></a>Synkronisere lageroverførsler og reguleringer fra Field Service til Supply Chain Management

[!include[banner](../includes/banner.md)]

I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere lagerreguleringer og overførsler fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.

[![Synkronisering af forretningsprocesser mellem Supply Chain Management og Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)

## <a name="templates-and-tasks"></a>Skabeloner og opgaver
Følgende skabelon og underliggende opgaver bruges til at synkronisere lagerreguleringer og overføre fra Field Service til Supply Chain Management.

**Skabeloner i dataintegration**
- Lagerregulering (Field Service til Supply Chain Management)
- Lageroverførsler (Field Service til Supply Chain Management)

**Opgaver i dataintegrationsprojekterne**
- Lagerreguleringer
- Lageroverførsler

## <a name="entity-set"></a>Enhedssæt
| Field Service                     | Supply Chain Management                          |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts |   CDS Overskrifter og linjer til lagerreguleringskladde |
| msdyn_inventoryadjustmentproducts | CDS Overskrifter og linjer til lageroverførselskladde   |

## <a name="entity-flow"></a>Enhedsflow
Lagerreguleringer og -overførsler, der er foretaget i Field Service, synkroniseres til Supply Chain Management, når **Bogføringsstatus** ændres fra **Oprettet** til **Bogført**. Når dette sker, låses reguleringen eller flytteordren og bliver skrivebeskyttet. Det betyder, at reguleringer og overførsler kan bogføres i Supply Chain Management, men ikke kan ændres. Du kan konfigurere et batchjob til automatisk at bogføre reguleringerne og overføre lagerkladder, der er genereret under integrationen, i Supply Chain Management. Følgende forudsætninger indeholder oplysninger om, hvordan du aktiverer batchjobbet.

## <a name="field-service-crm-solution"></a>CRM-løsning til Field Service 
Feltet **Lagerenhed** er blevet føjet til **Produkt**-enheden. Dette felt er nødvendigt, fordi salgs- og lagerenheden ikke altid er identisk i Supply Chain Management, og lagerenheden skal bruges i lagerstedet i Supply Chain Management.
Når du angiver produktet i et lagerreguleringsprodukt for både lagerreguleringer og lageroverførsler, hentes enheden fra lagerproduktværdien. Hvis der findes en værdi, låses feltet **Enhed** i lagerreguleringsproduktet.

Feltet **Bogføringsstatus** er føjet til både **Lagerregulering**-enheden og **Lageroverførsel**-enheden. Dette felt bruges som et filter for, hvornår der sendes en regulering eller overførsel til Supply Chain Management. Standardværdien for dette felt er Oprettet (1), men den ikke sendes til Supply Chain Management. Når du opdaterer værdien til Bogført (2), sendes den til Supply Chain Management, men derefter kan du ikke længere ændre reguleringen eller overførslen eller tilføje nye linjer.

Feltet **Nummerserie** er blevet føjet til enheden **Lagerreguleringsprodukt**. Feltet sikrer, at integrationen har et entydigt nummer, så integrationen kan oprette og opdatere reguleringen. Når du opretter dit første lagerreguleringsprodukt, oprettes en ny post i enheden **P2C Autonummerering** for at vedligeholde den nummerserie og det præfiks, der bruges.

## <a name="prerequisites-and-mapping-setup"></a>Forudsætninger og tilknytningsopsætning

### <a name="supply-chain-management"></a>Supply Chain Management
De integrationslagerkladder, der genereres af integrationen, kan automatisk bogføres ved hjælp af et batchjob. Dette aktiveres fra **Lagerstyring > Periodiske opgaver > CDS-integration > Bogfør integrationen af lagerkladder**.

## <a name="template-mapping-in-data-integration"></a>Skabelontilknytning i dataintegration

Følgende illustration viser skabelontilknytningen i Dataintegration.

### <a name="inventory-adjustment-field-service-to-supply-chain-management-inventory-adjustment"></a>Lagerregulering (Field Service til Supply Chain Management): Lagerregulering

[![Skabelontilknytning i dataintegration](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-supply-chain-management-inventory-transfer"></a>Lageroverførsel (Field Service til Supply Chain Management): Lageroverførsel

[![Skabelontilknytning i dataintegration](./media/FSTrans1.png)](./media/FSTrans1.png)
