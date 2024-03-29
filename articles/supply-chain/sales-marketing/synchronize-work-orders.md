---
title: Synkronisere arbejdsordrer med projekt fra Field Service til Supply Chain Management
description: Denne artikel beskriver de skabeloner og underliggende opgaver, der bruges til at synkronisere arbejdsordrer med et projektnummer fra Dynamics 365 Field Service til Dynamics 365 Supply Chain Management.
author: Henrikan
ms.date: 03/12/2019
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
ms.openlocfilehash: a43a7f7e900205bdb23fb9a35ca1518369683a42
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860487"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-supply-chain-management"></a>Synkronisere arbejdsordrer med projekt fra Field Service til Supply Chain Management

[!include[banner](../includes/banner.md)]

Denne artikel beskriver de skabeloner og underliggende opgaver, der bruges til at synkronisere arbejdsordrer med et projektnummer fra Dynamics 365 Field Service til Dynamics 365 Supply Chain Management.

[![Synkronisering af forretningsprocesser mellem Supply Chain Management og Field Service.](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)

Den anvendte skabelon **Arbejdsordrer med projekt (Field Service til Supply Chain Management)** er baseret på skabelonen **Arbejdsordrer (Field Service til Supply Chain Management)**. Du kan finde flere oplysninger i [Synkronisere arbejdsordrer i Field Service med salgsordrer i Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

Denne artikel beskriver kun forskellene mellem de to skabeloner:
- **Arbejdsordrer med projekt (Field Service til Supply Chain Management)**
- **Arbejdsordrer (Field Service til Supply Chain Management)**

Den væsentligste forskel er, at denne skabelon indeholder tilknytning af det projektnummer, der er tildelt arbejdsordren i Field Service. Det sikrer, at salgsordren, der er oprettet i Supply Chain Management, omfatter projektnummeret, og at fakturering kan udføres i det relaterede projekt. Derudover bruger skabelonen Avanceret forespørgsel og filtrering.

## <a name="templates-and-tasks"></a>Skabeloner og opgaver

**Navnet på skabelonen i dataintegration:**

- Arbejdsordrer med projekt (Field Service til Supply Chain Management)

**Navnet på opgaven i dataintegrationsprojektet:**

- WorkOrderHeader
- WorkOrderHeaderProject
- WorkOrderProduct
- WorkOrderService

## <a name="field-service-crm-solution"></a>CRM-løsning til Field Service
Feltet **Eksternt projekt** er føjet til enheden Arbejdsordre. Dette er et opslagsfelt, så hvis du mærker arbejdsordren til et projekt, bliver salgsordren forbundet med et projekt i Supply Chain Management. Når **Systemstatus** skifter fra Åben - i gang (690,970,000) til en højere status, låses feltet **Eksternt projekt**, og du kan ikke tilføje, fjerne eller ændre værdien.

## <a name="template-mapping-in-data-integration"></a>Skabelontilknytning i dataintegration

Følgende illustration viser skabelontilknytningen i Dataintegration.

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheader"></a>Arbejdsordrer med projekt (Field Service til Supply Chain Management): WorkOrderHeader

[![Skabelontilknytning i dataintegration for arbejdsordrer med projekt (Field Service til Supply Chain Management): WorkOrderHeader.](./media/FSWOP1.png)](./media/FSWOP1.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheaderproject"></a>Arbejdsordrer med projekt (Field Service til Supply Chain Management): WorkOrderHeaderProject

[![Skabelontilknytning i dataintegration for arbejdsordrer med projekt (Field Service til Supply Chain Management): WorkOrderHeaderProject.](./media/FSWOP2.png)](./media/FSWOP2.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderproduct"></a>Arbejdsordrer med projekt (Field Service til Supply Chain Management): WorkOrderProduct

[![Skabelontilknytning i dataintegration for arbejdsordrer med projekt (Field Service til Supply Chain Management): WorkOrderProduct.](./media/FSWOP3.png)](./media/FSWOP3.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderservice"></a>Arbejdsordrer med projekt (Field Service til Supply Chain Management): WorkOrderService

[![Skabelontilknytning i dataintegration for arbejdsordrer med projekt (Field Service til Supply Chain Management): WorkOrderService.](./media/FSWOP4.png)](./media/FSWOP4.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]