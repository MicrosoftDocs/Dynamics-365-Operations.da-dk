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
ms.sourcegitcommit: 08cfd2cfa24bef0f0c92126f5d1052a12ceba37a
ms.openlocfilehash: 699830ce6cd993f3dd3fd4ff744ce5a8b9645c32
ms.contentlocale: da-dk
ms.lasthandoff: 04/11/2018

---

# <a name="synchronize-products-in-finance-and-operations-to-products-in-field-service"></a><span data-ttu-id="5bf43-103">Synkronisere produkter fra Finance and Operations med produkter i Field Service</span><span class="sxs-lookup"><span data-stu-id="5bf43-103">Synchronize products in Finance and Operations to products in Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="5bf43-104">Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere produkter fra Microsoft Dynamics 365 for Finance and Operations med Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="5bf43-104">This topic discusses the templates and underlying task that are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="5bf43-105">Den anvendte skabelon **Field Service-produkter (Fin og Ops til Field Service)** er baseret på skabelonen **Produkter (Fin and Ops til Sales) – Direkte** fra Kundeemne til kontanter.</span><span class="sxs-lookup"><span data-stu-id="5bf43-105">The used **Field Service Products (Fin and Ops to Field Service)** template is based on the **Products (Fin and Ops to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="5bf43-106">Yderligere oplysninger finder du i [Produkter (Fin and Ops til Sales) – Direkte](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="5bf43-106">For more information, see [Products (Fin and Ops to Sales) – Direct](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="5bf43-107">Dette emne omhandler kun forskellene mellem skabelonerne **Field Service-produkter (Fin and Ops til Field Service)** og **Produkter (Fin and Ops til Sales) – Direkte**.</span><span class="sxs-lookup"><span data-stu-id="5bf43-107">This topic only describes the differences between the **Field Service Products (Fin and Ops to Field Service)** and **Products (Fin and Ops to Sales) – Direct** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="5bf43-108">Skabeloner og opgaver</span><span class="sxs-lookup"><span data-stu-id="5bf43-108">Templates and tasks</span></span>

<span data-ttu-id="5bf43-109">**Navnet på skabelonen i dataintegration:**</span><span class="sxs-lookup"><span data-stu-id="5bf43-109">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="5bf43-110">Field Service-produkter (Fin and Ops til Field Service)</span><span class="sxs-lookup"><span data-stu-id="5bf43-110">Field Service Products (Fin and Ops to Field Service)</span></span>

<span data-ttu-id="5bf43-111">**Navnet på opgaven i dataintegrationsprojektet:**</span><span class="sxs-lookup"><span data-stu-id="5bf43-111">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="5bf43-112">Produkter – Produkter</span><span class="sxs-lookup"><span data-stu-id="5bf43-112">Products - Products</span></span>

<span data-ttu-id="5bf43-113">Skabelonen **Field Service-produkter (Fin and Ops til Field Service)** omfatter en tilknytning, der ikke er inkluderet i skabelonen **Produkter (Fin and Ops til Sales) – Direkte** fra Kundeemne til kontanter.</span><span class="sxs-lookup"><span data-stu-id="5bf43-113">The **Field Service Products (Fin and Ops to Field Service)** template includes one mapping that isn't included in the **Products (Fin and Ops to Sales) – Direct** template.</span></span> <span data-ttu-id="5bf43-114">Denne tilknytning sikrer, at det krævede Field Service-specifikke felt **Serviceprodukttype** er angivet korrekt.</span><span class="sxs-lookup"><span data-stu-id="5bf43-114">This mapping ensures that the required Field Service-specific field **Service Product Type** is set correctly.</span></span>

```
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

<span data-ttu-id="5bf43-115">Følgende værditilknytning anvendes.</span><span class="sxs-lookup"><span data-stu-id="5bf43-115">The following value mapping is used.</span></span>

```
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

<span data-ttu-id="5bf43-116">I Finance and Operations beregnes værdien **Field Service-produkttype** på dataenheden **Salgbare frigivne produkter** på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="5bf43-116">In Finance and Operations, the **Field Service product type** value on the **Sellable released products** data entity is calculated as follows:</span></span>

- <span data-ttu-id="5bf43-117">**Lager:** Produkttype = Produkt- og varemodelgruppe, Lagerført produkt = Sand</span><span class="sxs-lookup"><span data-stu-id="5bf43-117">**Inventory:** Product type = Product and Item model group, Stocked product = True</span></span>
- <span data-ttu-id="5bf43-118">**Ikke-lager:** Produkttype = Produkt- og varemodelgruppe, Lagerført produkt = Falsk</span><span class="sxs-lookup"><span data-stu-id="5bf43-118">**NonInventory:** Product type = Product and Item model group, Stocked product = False</span></span>
- <span data-ttu-id="5bf43-119">**Service:** Produkttype = Service</span><span class="sxs-lookup"><span data-stu-id="5bf43-119">**Service:** Product type = Service</span></span>

