---
title: Synkronisere arbejdsordrer fra Finance and Operations til Field Service
description: Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere arbejdsordrer med et projektnummer fra Microsoft Dynamics 365 for Field Service med Microsoft Dynamics 365 for Finance and Operations.
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
ms.openlocfilehash: f5bd6b8c554688d0d1b2bfd93a34a60a95412bf3
ms.contentlocale: da-dk
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a>Synkronisere arbejdsordrer med et projektnummer fra Field Service til Finance and Operations

[!include[banner](../includes/banner.md)]

Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere arbejdsordrer med et projektnummer fra Microsoft Dynamics 365 for Field Service med Microsoft Dynamics 365 for Finance and Operations.

[![Synkronisering af forretningsprocesser mellem Finance and Operations og Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)

Den anvendte skabelon **Field Service-produkter (Finance and Operations til Field Service)** er baseret på skabelonen **Produkter (Finance and Operations til Sales) – Direkte** fra Kundeemne til kontanter. Yderligere oplysninger finder du i [Produkter (Finance and Operations til Sales) – Direkte](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).

Dette emne omhandler kun forskellene mellem skabelonerne **Field Service-produkter (Finance and Operations til Field Service)** og **Produkter (Finance and Operations til Field Service)**.

Den væsentligste forskel er, at denne skabelon indeholder tilknytning af det projektnummer, der er tildelt til arbejdsordren i Field Service. Det sikrer, at salgsordren, der er oprettet i Finance and Operations, omfatter projektnummeret, og at fakturering kan udføres i det relaterede projekt. Derudover bruger skabelonen Avanceret forespørgsel og filtrering.

## <a name="templates-and-tasks"></a>Skabeloner og opgaver

**Navnet på skabelonen i dataintegration:**

- Arbejdsordrer med projekt (Field Service til Finance and Operations)

**Navnet på opgaven i dataintegrationsprojektet:**

- WorkOrderHeader
- WorkOrderHeaderProject
- WorkOrderProduct
- WorkOrderService

## <a name="field-service-crm-solution"></a>CRM-løsning til Field Service
Feltet **Eksternt projekt** er føjet til enheden Arbejdsordre. Dette er et find og køb-felt, som mærker arbejdsordren til et projekt. Salgsordren bliver derefter forbundet med et projekt i Finance and Operations. Når **Systemstatus** skifter fra Åben - i gang (690,970,000) til en højere status, låses feltet **Eksternt projekt**, og du kan ikke tilføje, fjerne eller ændre værdien.

## <a name="template-mapping-in-data-integration"></a>Skabelontilknytning i dataintegration

Følgende illustration viser skabelontilknytningen i Dataintegration.

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheader"></a>Arbejdsordrer med projekt (Field Service til Finance and Operations): WorkOrderHeader

[![Skabelontilknytning i dataintegration](./media/FSWOP1.png)](./media/FSWOP1.png)

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheaderproject"></a>Arbejdsordrer med projekt (Field Service til Finance and Operations): WorkOrderHeaderProject

[![Skabelontilknytning i dataintegration](./media/FSWOP2.png)](./media/FSWOP2.png)

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderproduct"></a>Arbejdsordrer med projekt (Field Service til Finance and Operations): WorkOrderProduct

[![Skabelontilknytning i dataintegration](./media/FSWOP3.png)](./media/FSWOP3.png)

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderservice"></a>Arbejdsordrer med projekt (Field Service til Finance and Operations): WorkOrderService

[![Skabelontilknytning i dataintegration](./media/FSWOP4.png)](./media/FSWOP4.png)

