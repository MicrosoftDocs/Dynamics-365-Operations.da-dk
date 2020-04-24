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
# <a name="synchronize-products-in-supply-chain-management-to-products-in-field-service"></a><span data-ttu-id="99dd8-103">Synkronisere produkter i Supply Chain Management med produkter i Field Service</span><span class="sxs-lookup"><span data-stu-id="99dd8-103">Synchronize products in Supply Chain Management to products in Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="99dd8-104">I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere produkter fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="99dd8-104">This topic discusses the templates and underlying task that are used to synchronize products from Dynamics 365 Supply Chain Management to Dynamics 365  Field Service.</span></span>

<span data-ttu-id="99dd8-105">Den anvendte skabelon **Field Service-produkter (Supply Chain Management til Field Service)** er baseret på skabelonen **Produkter (Supply Chain Management til Sales) – Direkte** fra Kundeemne til kontanter.</span><span class="sxs-lookup"><span data-stu-id="99dd8-105">The used **Field Service Products (Supply Chain Management to Field Service)** template is based on the **Products (Supply Chain Management to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="99dd8-106">Yderligere oplysninger finder du i [Produkter (Supply Chain Management til Sales) – Direkte](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="99dd8-106">For more information, see [Products (Supply Chain Management to Sales) – Direct](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="99dd8-107">Dette emne omhandler kun forskellene mellem skabelonerne **Field Service-produkter (Supply Chain Management til Field Service)** og **Produkter (Supply Chain Management til Sales) – Direkte**.</span><span class="sxs-lookup"><span data-stu-id="99dd8-107">This topic only describes the differences between the **Field Service Products (Supply Chain Management to Field Service)** and **Products (Supply Chain Management to Sales) – Direct** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="99dd8-108">Skabeloner og opgaver</span><span class="sxs-lookup"><span data-stu-id="99dd8-108">Templates and tasks</span></span>

<span data-ttu-id="99dd8-109">**Navnet på skabelonen i Dataintegration**</span><span class="sxs-lookup"><span data-stu-id="99dd8-109">**Name of the template in Data integration**</span></span>

- <span data-ttu-id="99dd8-110">Field Service-produkter (Supply Chain Management til Field Service).</span><span class="sxs-lookup"><span data-stu-id="99dd8-110">Field Service Products (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="99dd8-111">**Navnet på opgaven i dataintegrationsprojektet**</span><span class="sxs-lookup"><span data-stu-id="99dd8-111">**Name of the task in the Data integration project**</span></span>

- <span data-ttu-id="99dd8-112">Produkter – Produkter</span><span class="sxs-lookup"><span data-stu-id="99dd8-112">Products - Products</span></span>

<span data-ttu-id="99dd8-113">Den anvendte skabelon **Field Service-produkter (Supply Chain Management til Field Service)** indeholder én tilknytning, der ikke findes i skabelonen **Produkter (Supply Chain Management til Sales) – Direkte**.</span><span class="sxs-lookup"><span data-stu-id="99dd8-113">The **Field Service Products (Supply Chain Management to Field Service)** template includes one mapping that isn't included in the **Products (Supply Chain Management to Sales) – Direct** template.</span></span> <span data-ttu-id="99dd8-114">Denne tilknytning sikrer, at det krævede Field Service-specifikke felt **Serviceprodukttype** er angivet korrekt.</span><span class="sxs-lookup"><span data-stu-id="99dd8-114">This mapping ensures that the required Field Service-specific field **Service Product Type** is set correctly.</span></span>

```Text
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

<span data-ttu-id="99dd8-115">Følgende værditilknytning anvendes.</span><span class="sxs-lookup"><span data-stu-id="99dd8-115">The following value mapping is used.</span></span>

```Text
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

<span data-ttu-id="99dd8-116">I Supply Chain Management beregnes værdien **Field Service-produkttype** på dataenheden **Salgbare frigivne produkter** på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="99dd8-116">In Supply Chain Management, the **Field Service product type** value on the **Sellable released products** data entity is calculated as follows:</span></span>

- <span data-ttu-id="99dd8-117">**Lager:** Produkttype = Produkt- og varemodelgruppe, Lagerført produkt = Sand</span><span class="sxs-lookup"><span data-stu-id="99dd8-117">**Inventory:** Product type = Product and Item model group, Stocked product = True</span></span>
- <span data-ttu-id="99dd8-118">**Ikke-lager:** Produkttype = Produkt- og varemodelgruppe, Lagerført produkt = Falsk</span><span class="sxs-lookup"><span data-stu-id="99dd8-118">**NonInventory:** Product type = Product and Item model group, Stocked product = False</span></span>
- <span data-ttu-id="99dd8-119">**Service:** Produkttype = Service</span><span class="sxs-lookup"><span data-stu-id="99dd8-119">**Service:** Product type = Service</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="99dd8-120">Skabelontilknytning i dataintegration</span><span class="sxs-lookup"><span data-stu-id="99dd8-120">Template mapping in Data integration</span></span>

<span data-ttu-id="99dd8-121">Følgende illustration viser skabelontilknytningen i Dataintegration.</span><span class="sxs-lookup"><span data-stu-id="99dd8-121">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-supply-chain-management-to-field-service-products---products"></a><span data-ttu-id="99dd8-122">Field Service-produkter (Supply Chain Management til Field Service): Produkter - Produkter</span><span class="sxs-lookup"><span data-stu-id="99dd8-122">Field Service Products (Supply Chain Management to Field Service): Products - Products</span></span>

<span data-ttu-id="99dd8-123">[![Skabelontilknytning i dataintegration](./media/FSProduct.png)](./media/FSProduct.png)</span><span class="sxs-lookup"><span data-stu-id="99dd8-123">[![Template mapping in Data integration](./media/FSProduct.png)](./media/FSProduct.png)</span></span>
