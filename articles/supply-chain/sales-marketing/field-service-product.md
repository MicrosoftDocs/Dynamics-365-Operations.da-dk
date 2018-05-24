---
title: Synkronisere produkter fra Finance and Operations med produkter i Field Service
description: Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere produkter fra Microsoft Dynamics 365 for Finance and Operations med Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 04/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: ace66c037953f4b1b2e8b93a315faefdb090b1eb
ms.openlocfilehash: bf5de13fee6db1b467c1cf4d5cc65b46c67b29fe
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---

# <a name="synchronize-products-in-finance-and-operations-to-products-in-field-service"></a>Synkronisere produkter fra Finance and Operations med produkter i Field Service

[!include[banner](../includes/banner.md)]

Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere produkter fra Microsoft Dynamics 365 for Finance and Operations med Microsoft Dynamics 365 for Field Service.

Den anvendte skabelon **Field Service-produkter (Fin og Ops til Field Service)** er baseret på skabelonen **Produkter (Fin and Ops til Sales) – Direkte** fra Kundeemne til kontanter. Yderligere oplysninger finder du i [Produkter (Fin and Ops til Sales) – Direkte](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).

Dette emne omhandler kun forskellene mellem skabelonerne **Field Service-produkter (Fin and Ops til Field Service)** og **Produkter (Fin and Ops til Sales) – Direkte**.

## <a name="templates-and-tasks"></a>Skabeloner og opgaver

**Navnet på skabelonen i dataintegration:**

- Field Service-produkter (Fin and Ops til Field Service)

**Navnet på opgaven i dataintegrationsprojektet:**

- Produkter – Produkter

Skabelonen **Field Service-produkter (Fin and Ops til Field Service)** omfatter en tilknytning, der ikke er inkluderet i skabelonen **Produkter (Fin and Ops til Sales) – Direkte** fra Kundeemne til kontanter. Denne tilknytning sikrer, at det krævede Field Service-specifikke felt **Serviceprodukttype** er angivet korrekt.

```
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

Følgende værditilknytning anvendes.

```
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

I Finance and Operations beregnes værdien **Field Service-produkttype** på dataenheden **Salgbare frigivne produkter** på følgende måde:

- **Lager:** Produkttype = Produkt- og varemodelgruppe, Lagerført produkt = Sand
- **Ikke-lager:** Produkttype = Produkt- og varemodelgruppe, Lagerført produkt = Falsk
- **Service:** Produkttype = Service

## <a name="template-mapping-in-data-integration"></a>Skabelontilknytning i dataintegration

Følgende illustration viser skabelontilknytningen i Dataintegration.

### <a name="field-service-products-fin-and-ops-to-field-service-products---products"></a>Field Service-produkter (Fin and Ops til Field Service): Produkter - Produkter

[![Skabelontilknytning i dataintegration](./media/FSProduct.png)](./media/FSProduct.png)

