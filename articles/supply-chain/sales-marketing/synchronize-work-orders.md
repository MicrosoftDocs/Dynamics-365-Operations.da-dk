---
title: Synkronisere arbejdsordrer med et projektnummer fra Field Service til Finance and Operations
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere arbejdsordrer med et projektnummer fra Microsoft Dynamics 365 for Field Service til Microsoft Dynamics 365 for Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 03/12/2019
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
ms.openlocfilehash: 77358513ffdf791ab10d6efe1b84f598ffb5ec26
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843403"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a>Synkronisere arbejdsordrer med et projektnummer fra Field Service til Finance and Operations

[!include[banner](../includes/banner.md)]

I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere arbejdsordrer med et projektnummer fra Microsoft Dynamics 365 for Field Service til Microsoft Dynamics 365 for Finance and Operations.

[![Synkronisering af forretningsprocesser mellem Finance and Operations og Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)

Den anvendte skabelon **Arbejdsordrer med projekt (Field Service til Finance and Operations)** er baseret på skabelonen **Arbejdsordrer (Field Service til Finance and Operations)**. Du kan finde flere oplysninger i [Synkronisere arbejdsordrer i Field Service med salgsordrer i Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

I dette emne beskrives kun forskellene mellem de to skabeloner:
- **Arbejdsordrer med projekt (Field Service til Finance and Operations)**
- **Arbejdsordrer (Field Service til Finance and Operations)**

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

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheader"></a>Arbejdsordrer med projekt (Field Service til Finance and Operations): WorkOrderHeader

[![Skabelontilknytning i dataintegration](./media/FSWOP1.png)](./media/FSWOP1.png)

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheaderproject"></a>Arbejdsordrer med projekt (Field Service til Finance and Operations): WorkOrderHeaderProject

[![Skabelontilknytning i dataintegration](./media/FSWOP2.png)](./media/FSWOP2.png)

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderproduct"></a>Arbejdsordrer med projekt (Field Service til Finance and Operations): WorkOrderProduct

[![Skabelontilknytning i dataintegration](./media/FSWOP3.png)](./media/FSWOP3.png)

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderservice"></a>Arbejdsordrer med projekt (Field Service til Finance and Operations): WorkOrderService

[![Skabelontilknytning i dataintegration](./media/FSWOP4.png)](./media/FSWOP4.png)
