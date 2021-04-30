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
ms.openlocfilehash: 45a989604d829db715756b6cd206a5675a18acf2
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909985"
---
# <a name="synchronize-products-in-supply-chain-management-to-products-in-field-service"></a><span data-ttu-id="1f0a0-103">Synkronisere produkter i Supply Chain Management med produkter i Field Service</span><span class="sxs-lookup"><span data-stu-id="1f0a0-103">Synchronize products in Supply Chain Management to products in Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="1f0a0-104">I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere produkter fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-104">This topic discusses the templates and underlying task that are used to synchronize products from Dynamics 365 Supply Chain Management to Dynamics 365  Field Service.</span></span>

<span data-ttu-id="1f0a0-105">Den anvendte skabelon **Field Service-produkter (Supply Chain Management til Field Service)** er baseret på skabelonen **Produkter (Supply Chain Management til Sales) – Direkte** fra Kundeemne til kontanter.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-105">The used **Field Service Products (Supply Chain Management to Field Service)** template is based on the **Products (Supply Chain Management to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="1f0a0-106">Yderligere oplysninger finder du i [Produkter (Supply Chain Management til Sales) – Direkte](/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="1f0a0-106">For more information, see [Products (Supply Chain Management to Sales) – Direct](/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="1f0a0-107">Dette emne omhandler kun forskellene mellem skabelonerne **Field Service-produkter (Supply Chain Management til Field Service)** og **Produkter (Supply Chain Management til Sales) – Direkte**.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-107">This topic only describes the differences between the **Field Service Products (Supply Chain Management to Field Service)** and **Products (Supply Chain Management to Sales) – Direct** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="1f0a0-108">Skabeloner og opgaver</span><span class="sxs-lookup"><span data-stu-id="1f0a0-108">Templates and tasks</span></span>

<span data-ttu-id="1f0a0-109">**Navnet på skabelonen i Dataintegration**</span><span class="sxs-lookup"><span data-stu-id="1f0a0-109">**Name of the template in Data integration**</span></span>

- <span data-ttu-id="1f0a0-110">Field Service-produkter (Supply Chain Management til Field Service).</span><span class="sxs-lookup"><span data-stu-id="1f0a0-110">Field Service Products (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="1f0a0-111">**Navnet på opgaven i dataintegrationsprojektet**</span><span class="sxs-lookup"><span data-stu-id="1f0a0-111">**Name of the task in the Data integration project**</span></span>

- <span data-ttu-id="1f0a0-112">Produkter – Produkter</span><span class="sxs-lookup"><span data-stu-id="1f0a0-112">Products - Products</span></span>

<span data-ttu-id="1f0a0-113">Den anvendte skabelon **Field Service-produkter (Supply Chain Management til Field Service)** indeholder én tilknytning, der ikke findes i skabelonen **Produkter (Supply Chain Management til Sales) – Direkte**.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-113">The **Field Service Products (Supply Chain Management to Field Service)** template includes one mapping that isn't included in the **Products (Supply Chain Management to Sales) – Direct** template.</span></span> <span data-ttu-id="1f0a0-114">Denne tilknytning sikrer, at det krævede Field Service-specifikke felt **Serviceprodukttype** er angivet korrekt.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-114">This mapping ensures that the required Field Service-specific field **Service Product Type** is set correctly.</span></span>

```plaintext
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

<span data-ttu-id="1f0a0-115">Følgende værditilknytning anvendes.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-115">The following value mapping is used.</span></span>

```plaintext
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

<span data-ttu-id="1f0a0-116">I Supply Chain Management beregnes værdien **Field Service-produkttype** på dataenheden **Salgbare frigivne produkter** på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="1f0a0-116">In Supply Chain Management, the **Field Service product type** value on the **Sellable released products** data entity is calculated as follows:</span></span>

- <span data-ttu-id="1f0a0-117">**Lager:** Produkttype = Produkt- og varemodelgruppe, Lagerført produkt = Sand</span><span class="sxs-lookup"><span data-stu-id="1f0a0-117">**Inventory:** Product type = Product and Item model group, Stocked product = True</span></span>
- <span data-ttu-id="1f0a0-118">**Ikke-lager:** Produkttype = Produkt- og varemodelgruppe, Lagerført produkt = Falsk</span><span class="sxs-lookup"><span data-stu-id="1f0a0-118">**NonInventory:** Product type = Product and Item model group, Stocked product = False</span></span>
- <span data-ttu-id="1f0a0-119">**Service:** Produkttype = Service</span><span class="sxs-lookup"><span data-stu-id="1f0a0-119">**Service:** Product type = Service</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="1f0a0-120">Skabelontilknytning i dataintegration</span><span class="sxs-lookup"><span data-stu-id="1f0a0-120">Template mapping in Data integration</span></span>

<span data-ttu-id="1f0a0-121">Følgende illustration viser skabelontilknytningen i Dataintegration.</span><span class="sxs-lookup"><span data-stu-id="1f0a0-121">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-supply-chain-management-to-field-service-products---products"></a><span data-ttu-id="1f0a0-122">Field Service-produkter (Supply Chain Management til Field Service): Produkter - Produkter</span><span class="sxs-lookup"><span data-stu-id="1f0a0-122">Field Service Products (Supply Chain Management to Field Service): Products - Products</span></span>

<span data-ttu-id="1f0a0-123">[![Skabelontilknytning i dataintegration](./media/FSProduct.png)](./media/FSProduct.png)</span><span class="sxs-lookup"><span data-stu-id="1f0a0-123">[![Template mapping in Data integration](./media/FSProduct.png)](./media/FSProduct.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]