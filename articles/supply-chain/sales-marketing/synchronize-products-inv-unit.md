---
title: Synkronisere produkter med lagerenhed fra Finance and Operations til Field Service
description: Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere produkter med lagerenhed fra Microsoft Dynamics 365 for Finance and Operations med Microsoft Dynamics 365 for Field Service.
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
ms.openlocfilehash: 5d3767c1a499f3d888d8fc2ce06c2837442e39f0
ms.contentlocale: da-dk
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a>Synkronisere produkter med lagerenhed fra Finance and Operations til Field Service

[!include[banner](../includes/banner.md)]

Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere produkter med lagerenhed fra Microsoft Dynamics 365 for Finance and Operations med Microsoft Dynamics 365 for Field Service.

[![Synkronisering af forretningsprocesser mellem Finance and Operations og Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)

Den anvendte skabelon **Field Service-produkter (Finance and Operations til Field Service)** er baseret på skabelonen **Produkter (Finance and Operations til Sales) – Direkte** fra Kundeemne til kontanter. Yderligere oplysninger finder du i [Produkter (Finance and Operations til Sales) – Direkte](products-template-mapping-direct.md).

Dette emne omhandler kun forskellene mellem skabelonerne **Field Service-produkter (Finance and Operations til Field Service)** og **Produkter (Finance and Operations til Field Service)**.

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

