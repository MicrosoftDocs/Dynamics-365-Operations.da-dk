---
title: Synkronisere produkter i Supply Chain Management med produkter i Field Service
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere produkter fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.
author: ChristianRytt
ms.date: 04/09/2018
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
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: f765a6f0cbdc99604e0b0191e1cb6a200546769b
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2021
ms.locfileid: "6359575"
---
# <a name="synchronize-products-in-supply-chain-management-to-products-in-field-service"></a>Synkronisere produkter i Supply Chain Management med produkter i Field Service

[!include[banner](../includes/banner.md)]

I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere produkter fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.

Den anvendte skabelon **Field Service-produkter (Supply Chain Management til Field Service)** er baseret på skabelonen **Produkter (Supply Chain Management til Sales) – Direkte** fra Kundeemne til kontanter. Yderligere oplysninger finder du i [Produkter (Supply Chain Management til Sales) – Direkte](/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).

Dette emne omhandler kun forskellene mellem skabelonerne **Field Service-produkter (Supply Chain Management til Field Service)** og **Produkter (Supply Chain Management til Sales) – Direkte**.

## <a name="templates-and-tasks"></a>Skabeloner og opgaver

**Navnet på skabelonen i Dataintegration**

- Field Service-produkter (Supply Chain Management til Field Service).

**Navnet på opgaven i dataintegrationsprojektet**

- Produkter – Produkter

Den anvendte skabelon **Field Service-produkter (Supply Chain Management til Field Service)** indeholder én tilknytning, der ikke findes i skabelonen **Produkter (Supply Chain Management til Sales) – Direkte**. Denne tilknytning sikrer, at det krævede Field Service-specifikke felt **Serviceprodukttype** er angivet korrekt.

```plaintext
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

Følgende værditilknytning anvendes.

```plaintext
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

[![Skabelontilknytning i dataintegration.](./media/FSProduct.png)](./media/FSProduct.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]