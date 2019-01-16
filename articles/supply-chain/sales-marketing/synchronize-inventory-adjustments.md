---
title: "Synkronisere lageroverførsler og reguleringer fra Field Service til Finance and Operations"
description: "Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere lageroverførsler og reguleringer fra Microsoft Dynamics 365 for Finance and Operations med Microsoft Dynamics 365 for Field Service."
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
ms.openlocfilehash: 79a1cfac3fa94223cc9af73e758ce95fd47065c9
ms.contentlocale: da-dk
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a>Synkronisere lagerreguleringer fra Field Service til Finance and Operations

[!include[banner](../includes/banner.md)]

Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere lageroverførsler og reguleringer fra Microsoft Dynamics 365 for Finance and Operations med Microsoft Dynamics 365 for Field Service.

[![Synkronisering af forretningsprocesser mellem Finance and Operations og Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)

## <a name="templates-and-tasks"></a>Skabeloner og opgaver
Følgende skabelon og underliggende opgaver bruges til at køre synkronisering af lageroverførsler og reguleringer fra Microsoft Dynamics 365 for Field Service til Microsoft Dynamics 365 for Finance and Operations.

**Navnet på skabelonerne i dataintegration:**
- Lagerregulering (Field Service til Finance and Operations)
- Lageroverførsler (Field Service til Finance and Operations)

**Navne på opgaverne i dataintegrationsprojekterne:**
- Lagerreguleringer
- Lageroverførsler

## <a name="entity-set"></a>Enhedssæt
| Field Service                     | Finance and Operations                             |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts |   CDS Overskrifter og linjer til lagerreguleringskladde |
| msdyn_inventoryadjustmentproducts | CDS Overskrifter og linjer til lageroverførselskladde   |

## <a name="entity-flow"></a>Enhedsflow
Lagerreguleringer og overførsler, der er foretaget i Field Service, synkroniseres til Finance and Operations, når **Bogføringsstatus** ændres fra Oprettet til Bogført. Når dette sker, låses regulerings- eller overførselsordren og bliver skrivebeskyttet, fordi reguleringer og overførsler muligvis bogføres i Finance and Operations og derfor ikke kan ændres.
Du kan konfigurere et batchjob til automatisk at bogføre reguleringerne og overføre lagerkladder, der er genereret med integrationen, i Finance and Operations. Se oplysninger om, hvordan du aktiverer kørslen, i forudsætningen nedenfor.

## <a name="field-service-crm-solution"></a>CRM-løsning til Field Service 
Feltet Lagerenhed er blevet føjet til produktenheden. Dette felt er nødvendigt, fordi salgs- og lagerenheden ikke altid er identiske i Operations, og vi skal bruge lagerenheden i Standardlagersted i Operations.
Når du angiver produktet i et lagerreguleringsprodukt for både lagerreguleringer og lageroverførsler, hentes enheden fra værdien Produkters værdi for lagerprodukt. Hvis der findes en værdi, låses feltet Enhed i lagerreguleringsproduktet

Feltet Bogføringsstatus er føjet til både lagerreguleringsenheden og lageroverførselsenheden. Dette felt bruges som et filter for, hvornår der sendes en regulering eller overførsel til Operations. Feltet er som standard Oprettet (1), og sendes som sådan ikke til Operations. Når du har ændret til Bogført (2), sendes det til Operations, men du kan derefter ikke længere ændre noget i Regulering eller Overførsel eller føje nye linjer til det.
Feltet Nummerserie er blevet føjet til produktenheden Lagerregulering. Dette felt tildeler integrationen et entydigt nummer, så det står klart, hvornår der skal udføres henholdsvis oprettelser og opdateringer. Når du opretter dit første lagerreguleringsprodukt, oprettes en ny post i objektet P2C Autonummerering for at vedligeholde den nummerserie og det præfiks, der bruges.

## <a name="prerequisites-and-mapping-setup"></a>Forudsætninger og tilknytningsopsætning

### <a name="in-finance-and-operations"></a>I Finance and Operations
De integrationslagerkladder, der genereres af integrationen, kan automatisk bogføres med et batchjob. Dette aktiveres fra: Lagerstyring > Periodiske opgaver > CDS-integration > Bogfør integrationen af lagerkladder

## <a name="template-mapping-in-data-integration"></a>Skabelontilknytning i dataintegration

Følgende illustration viser skabelontilknytningen i Dataintegration.

### <a name="inventory-adjustment-field-service-to-finance-and-operations-inventory-adjustment"></a>Lagerregulering (Field Service til Finance and Operations): Lagerregulering

[![Skabelontilknytning i dataintegration](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-finance-and-operations-inventory-transfer"></a>Lageroverførsel (Field Service til Finance and Operations): Lageroverførsel

[![Skabelontilknytning i dataintegration](./media/FSTrans1.png)](./media/FSTrans1.png)

