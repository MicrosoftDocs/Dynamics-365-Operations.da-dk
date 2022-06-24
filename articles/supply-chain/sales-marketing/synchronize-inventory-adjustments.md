---
title: Synkronisere lageroverførsler og reguleringer fra Field Service til Supply Chain Management
description: Denne artikel beskriver de skabeloner og underliggende opgaver, der bruges til at synkronisere lagerreguleringer og overførsler fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.
author: Henrikan
ms.date: 04/30/2019
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
ms.author: henrikan
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: e59e50a4f54bac749b3d860404a3ecd444d99a89
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854088"
---
# <a name="synchronize-inventory-transfers-and-adjustments-from-field-service-to-supply-chain-management"></a>Synkronisere lageroverførsler og reguleringer fra Field Service til Supply Chain Management

[!include[banner](../includes/banner.md)]



Denne artikel beskriver de skabeloner og underliggende opgaver, der bruges til at synkronisere lagerreguleringer og overførsler fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.

[![Synkronisering af forretningsprocesser mellem Supply Chain Management og Field Service.](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)

## <a name="templates-and-tasks"></a>Skabeloner og opgaver
Følgende skabelon og underliggende opgaver bruges til at synkronisere lagerreguleringer og overføre fra Field Service til Supply Chain Management.

**Skabeloner i dataintegration**
- Lagerregulering (Field Service til Supply Chain Management)
- Lageroverførsler (Field Service til Supply Chain Management)

**Opgaver i dataintegrationsprojekterne**
- Lagerreguleringer
- Lageroverførsler

## <a name="table-set"></a>Tabelsæt
| Field Service                     | Supply Chain Management                          |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts | Overskrifter og linjer til Dataverse-lagerreguleringskladde |
| msdyn_inventoryadjustmentproducts | Overskrifter og linjer til Dataverse-lageroverførselskladde   |

## <a name="table-flow"></a>Tabelflow
Lagerreguleringer og -overførsler, der er foretaget i Field Service, synkroniseres til Supply Chain Management, når **Bogføringsstatus** ændres fra **Oprettet** til **Bogført**. Når dette sker, låses reguleringen eller flytteordren og bliver skrivebeskyttet. Det betyder, at reguleringer og overførsler kan bogføres i Supply Chain Management, men ikke kan ændres. Du kan konfigurere et batchjob til automatisk at bogføre reguleringerne og overføre lagerkladder, der er genereret under integrationen, i Supply Chain Management. Følgende forudsætninger indeholder oplysninger om, hvordan du aktiverer batchjobbet.

## <a name="field-service-crm-solution"></a>CRM-løsning til Field Service 
Kolonnen **Lagerenhed** er blevet føjet til tabellen **Produkt**. Denne kolonne er nødvendig, fordi salgs- og lagerenheden ikke altid er identisk i Supply Chain Management, og lagerenheden skal bruges i lagerstedet i Supply Chain Management.
Når du angiver produktet i et lagerreguleringsprodukt for både lagerreguleringer og lageroverførsler, hentes enheden fra lagerproduktværdien. Hvis der findes en værdi, låses kolonnen **Enhed** i lagerreguleringsproduktet.

Kolonnen **Bogføringsstatus** er føjet til både tabellen **Lagerregulering** og tabellen **Lageroverførsel**. Denne kolonne bruges som et filter for, hvornår der sendes en regulering eller overførsel til Supply Chain Management. Standardværdien for denne kolonne er Oprettet (1), men den ikke sendes til Supply Chain Management. Når du opdaterer værdien til Bogført (2), sendes den til Supply Chain Management, men derefter kan du ikke længere ændre reguleringen eller overførslen eller tilføje nye linjer.

Kolonnen **Nummerserie** er blevet føjet til tabellen **Lagerreguleringsprodukt**. Kolonnen sikrer, at integrationen har et entydigt nummer, så integrationen kan oprette og opdatere reguleringen. Når du opretter dit første lagerreguleringsprodukt, oprettes en ny post i tabellen **P2C Autonummerering** for at vedligeholde den nummerserie og det præfiks, der bruges.

## <a name="prerequisites-and-mapping-setup"></a>Forudsætninger og tilknytningsopsætning

### <a name="supply-chain-management"></a>Supply Chain Management
De integrationslagerkladder, der genereres af integrationen, kan automatisk bogføres ved hjælp af et batchjob. Dette aktiveres fra **Lagerstyring > Periodiske opgaver > Dataverse-integration > Bogfør integrationen af lagerkladder**.

## <a name="template-mapping-in-data-integration"></a>Skabelontilknytning i dataintegration

Følgende illustration viser skabelontilknytningen i Dataintegration.

### <a name="inventory-adjustment-field-service-to-supply-chain-management-inventory-adjustment"></a>Lagerregulering (Field Service til Supply Chain Management): Lagerregulering

[![Skabelontilknytning i Dataintegration, Lagerregulering (Field Service til Supply Chain Management): Lagerregulering.](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-supply-chain-management-inventory-transfer"></a>Lageroverførsel (Field Service til Supply Chain Management): Lageroverførsel

[![Skabelontilknytning i Dataintegration, Lagerflytning (Field Service til Supply Chain Management): Lagerflytning.](./media/FSTrans1.png)](./media/FSTrans1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]