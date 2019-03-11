---
title: Synkronisere lageroverførsler og reguleringer fra Field Service til Finance and Operations
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere lagerreguleringer og overførsler fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.
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
ms.openlocfilehash: aa54945cea5821da163e1f6ea1747ac29b31a3ce
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "308362"
---
# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a>Synkronisere lagerreguleringer fra Field Service til Finance and Operations

[!include[banner](../includes/banner.md)]

I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere lagerreguleringer og overførsler fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.

[![Synkronisering af forretningsprocesser mellem Finance and Operations og Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)

## <a name="templates-and-tasks"></a>Skabeloner og opgaver
Følgende skabelon og underliggende opgaver bruges til at synkronisere lagerreguleringer og overførsler fra Microsoft Dynamics 365 for Field Service til Microsoft Dynamics 365 for Finance and Operations.

**Skabeloner i dataintegration**
- Lagerregulering (Field Service til Finance and Operations)
- Lageroverførsler (Field Service til Finance and Operations)

**Opgaver i dataintegrationsprojekterne**
- Lagerreguleringer
- Lageroverførsler

## <a name="entity-set"></a>Enhedssæt
| Field Service                     | Finance and Operations                             |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts |   CDS Overskrifter og linjer til lagerreguleringskladde |
| msdyn_inventoryadjustmentproducts | CDS Overskrifter og linjer til lageroverførselskladde   |

## <a name="entity-flow"></a>Enhedsflow
Lagerreguleringer og overførsler, der er foretaget i Field Service, synkroniseres til Finance and Operations, når **Bogføringsstatus** ændres fra **Oprettet** til **Bogført**. Når dette sker, låses reguleringen eller flytteordren og bliver skrivebeskyttet. Det betyder, at reguleringer og overførsler kan bogføres i Finance and Operations, men ikke kan ændres. Du kan konfigurere et batchjob til automatisk at bogføre reguleringerne og overføre lagerkladder, der er genereret under integrationen, i Finance and Operations. Følgende forudsætninger indeholder oplysninger om, hvordan du aktiverer batchjobbet.

## <a name="field-service-crm-solution"></a>CRM-løsning til Field Service 
Feltet **Lagerenhed** er blevet føjet til **Produkt**-enheden. Dette felt er nødvendigt, fordi salgs- og lagerenheden ikke altid er identisk i Finance and Operations, og lagerenheden skal bruges i lagerstedet i Finance and Operations.
Når du angiver produktet i et lagerreguleringsprodukt for både lagerreguleringer og lageroverførsler, hentes enheden fra lagerproduktværdien. Hvis der findes en værdi, låses feltet **Enhed** i lagerreguleringsproduktet.

Feltet **Bogføringsstatus** er føjet til både **Lagerregulering**-enheden og **Lageroverførsel**-enheden. Dette felt bruges som et filter for, hvornår der sendes en regulering eller overførsel til Finance and Operations. Standardværdien for dette felt er Oprettet (1), men den ikke sendes til Finance and Operations. Når du opdaterer værdien til Bogført (2), sendes den til Finance and Operations, men derefter kan du ikke længere ændre reguleringen eller overførslen eller tilføje nye linjer.

Feltet **Nummerserie** er blevet føjet til enheden **Lagerreguleringsprodukt**. Feltet sikrer, at integrationen har et entydigt nummer, så integrationen kan oprette og opdatere reguleringen. Når du opretter dit første lagerreguleringsprodukt, oprettes en ny post i enheden **P2C Autonummerering** for at vedligeholde den nummerserie og det præfiks, der bruges.

## <a name="prerequisites-and-mapping-setup"></a>Forudsætninger og tilknytningsopsætning

### <a name="finance-and-operations"></a>Finance and Operations
De integrationslagerkladder, der genereres af integrationen, kan automatisk bogføres ved hjælp af et batchjob. Dette aktiveres fra **Lagerstyring > Periodiske opgaver > CDS-integration > Bogfør integrationen af lagerkladder**.

## <a name="template-mapping-in-data-integration"></a>Skabelontilknytning i dataintegration

Følgende illustration viser skabelontilknytningen i Dataintegration.

### <a name="inventory-adjustment-field-service-to-finance-and-operations-inventory-adjustment"></a>Lagerregulering (Field Service til Finance and Operations): Lagerregulering

[![Skabelontilknytning i dataintegration](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-finance-and-operations-inventory-transfer"></a>Lageroverførsel (Field Service til Finance and Operations): Lageroverførsel

[![Skabelontilknytning i dataintegration](./media/FSTrans1.png)](./media/FSTrans1.png)
