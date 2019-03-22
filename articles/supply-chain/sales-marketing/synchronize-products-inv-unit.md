---
title: Synkronisere produkter med lagerenhed fra Finance and Operations til Field Service
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere produkter med lagerenhed fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 03/12/2019
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
ms.openlocfilehash: 8e421be79fde6103be6344040b6ae6cda0626c5a
ms.sourcegitcommit: d9ed934a142b88340d268fd2bd3753475a3712b0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/12/2019
ms.locfileid: "836296"
---
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a>Synkronisere produkter med lagerenhed fra Finance and Operations til Field Service

[!include[banner](../includes/banner.md)]

I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere produkter med lagerenhed fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.

[![Synkronisering af forretningsprocesser mellem Finance and Operations og Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)

Den anvendte **Field Service-produkter med lagerenhed (Finance and Operations til Field Service)**-skabelon er baseret på skabelonen **Field Service-produkter (Finance and Operations til Field Service)**. Yderligere oplysninger finder du i [Field Service-produkter (Finance and Operations til Field Service)](field-service-product.md).

I dette emne beskrives kun forskellene mellem de to skabeloner: 
- **Field Service-produkter med lagerenhed (Finance and Operations til Sales)**
- **Field Service-produkter (Finance and Operations til Field Service)** 

## <a name="templates-and-tasks"></a>Skabeloner og opgaver

**Navnet på skabelonen i dataintegration:**

- Field Service-produkter med lagerenhed (Finance and Operations til Sales)

**Navnet på opgaven i dataintegrationsprojektet:**

- Produkter

Skabelonen **Field Service-produkter med lagerenhed (Finance and Operations til Field Service)** indeholder én tilknytning, der ikke findes i skabelonen **Field Service-produkter (Finance and Operations til Field Service)**. Denne tilknytning sikrer, at den lagerenhed, der skal bruges til synkronisering på lagerniveau, er inkluderet.

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a>Skabelontilknytning i dataintegration

Følgende illustration viser skabelontilknytningen i Dataintegration.

### <a name="field-service-products-with-inventory-unit-finance-and-operations-to-field-service-products"></a>Field Service-produkter med lagerenhed (Finance and Operations til Field Service): Produkter

[![Skabelontilknytning i dataintegration](./media/FSProduct1.png)](./media/FSProduct1.png)
