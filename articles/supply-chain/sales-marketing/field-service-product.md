---
title: Synkronisere produkter i Supply Chain Management med produkter i Field Service
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere produkter fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.
author: ChristianRytt
manager: tfehr
ms.date: 04/09/2018
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 1efa4e403f5cf2cdc5fb797f05781f6d42245ed5
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210003"
---
# <a name="synchronize-products-in-supply-chain-management-to-products-in-field-service"></a>Synkronisere produkter i Supply Chain Management med produkter i Field Service

[!include[banner](../includes/banner.md)]

I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere produkter fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.

Den anvendte skabelon **Field Service-produkter (Supply Chain Management til Field Service)** er baseret på skabelonen **Produkter (Supply Chain Management til Sales) – Direkte** fra Kundeemne til kontanter. Yderligere oplysninger finder du i [Produkter (Supply Chain Management til Sales) – Direkte](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).

Dette emne omhandler kun forskellene mellem skabelonerne **Field Service-produkter (Supply Chain Management til Field Service)** og **Produkter (Supply Chain Management til Sales) – Direkte**.

## <a name="templates-and-tasks"></a>Skabeloner og opgaver

**Navnet på skabelonen i Dataintegration**

- Field Service-produkter (Supply Chain Management til Field Service).

**Navnet på opgaven i dataintegrationsprojektet**

- Produkter – Produkter

Den anvendte skabelon **Field Service-produkter (Supply Chain Management til Field Service)** indeholder én tilknytning, der ikke findes i skabelonen **Produkter (Supply Chain Management til Sales) – Direkte**. Denne tilknytning sikrer, at det krævede Field Service-specifikke felt **Serviceprodukttype** er angivet korrekt.

```Text
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

Følgende værditilknytning anvendes.

```Text
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

I Supply Chain Management beregnes værdien **Field Service-produkttype** på dataenheden **Salgbare frigivne produkter** på følgende måde:

- **Lager:** Produkttype = Produkt- og varemodelgruppe, Lagerført produkt = Sand
- **Ikke-lager:** Produkttype = Produkt- og varemodelgruppe, Lagerført produkt = Falsk
- **Service:** Produkttype = Service

## <a name="template-mapping-in-data-integration"></a>Skabelontilknytning i dataintegration

Følgende illustration viser skabelontilknytningen i Dataintegration.

### <a name="field-service-products-supply-chain-management-to-field-service-products---products"></a>Field Service-produkter (Supply Chain Management til Field Service): Produkter - Produkter

[![Skabelontilknytning i dataintegration](./media/FSProduct.png)](./media/FSProduct.png)
