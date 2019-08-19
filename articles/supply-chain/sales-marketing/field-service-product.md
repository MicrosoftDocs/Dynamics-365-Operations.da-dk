---
title: Synkronisere produkter fra Finance and Operations med produkter i Field Service
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere produkter fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 04/09/2018
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 06d7ff272ecb79abded3c3d3ade1f6bc0ef1f095
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742349"
---
# <a name="synchronize-products-in-finance-and-operations-to-products-in-field-service"></a><span data-ttu-id="25549-103">Synkronisere produkter fra Finance and Operations med produkter i Field Service</span><span class="sxs-lookup"><span data-stu-id="25549-103">Synchronize products in Finance and Operations to products in Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="25549-104">I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere produkter fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="25549-104">This topic discusses the templates and underlying task that are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="25549-105">Den anvendte skabelon **Field Service-produkter (Fin og Ops til Field Service)** er baseret på skabelonen **Produkter (Fin and Ops til Sales) – Direkte** fra Kundeemne til kontanter.</span><span class="sxs-lookup"><span data-stu-id="25549-105">The used **Field Service Products (Fin and Ops to Field Service)** template is based on the **Products (Fin and Ops to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="25549-106">Yderligere oplysninger finder du i [Produkter (Fin and Ops til Sales) – Direkte](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="25549-106">For more information, see [Products (Fin and Ops to Sales) – Direct](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="25549-107">Dette emne omhandler kun forskellene mellem skabelonerne **Field Service-produkter (Fin and Ops til Field Service)** og **Produkter (Fin and Ops til Sales) – Direkte**.</span><span class="sxs-lookup"><span data-stu-id="25549-107">This topic only describes the differences between the **Field Service Products (Fin and Ops to Field Service)** and **Products (Fin and Ops to Sales) – Direct** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="25549-108">Skabeloner og opgaver</span><span class="sxs-lookup"><span data-stu-id="25549-108">Templates and tasks</span></span>

<span data-ttu-id="25549-109">**Navnet på skabelonen i dataintegration:**</span><span class="sxs-lookup"><span data-stu-id="25549-109">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="25549-110">Field Service-produkter (Fin and Ops til Field Service)</span><span class="sxs-lookup"><span data-stu-id="25549-110">Field Service Products (Fin and Ops to Field Service)</span></span>

<span data-ttu-id="25549-111">**Navnet på opgaven i dataintegrationsprojektet:**</span><span class="sxs-lookup"><span data-stu-id="25549-111">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="25549-112">Produkter – Produkter</span><span class="sxs-lookup"><span data-stu-id="25549-112">Products - Products</span></span>

<span data-ttu-id="25549-113">Skabelonen **Field Service-produkter (Fin and Ops til Field Service)** omfatter en tilknytning, der ikke er inkluderet i skabelonen **Produkter (Fin and Ops til Sales) – Direkte** fra Kundeemne til kontanter.</span><span class="sxs-lookup"><span data-stu-id="25549-113">The **Field Service Products (Fin and Ops to Field Service)** template includes one mapping that isn't included in the **Products (Fin and Ops to Sales) – Direct** template.</span></span> <span data-ttu-id="25549-114">Denne tilknytning sikrer, at det krævede Field Service-specifikke felt **Serviceprodukttype** er angivet korrekt.</span><span class="sxs-lookup"><span data-stu-id="25549-114">This mapping ensures that the required Field Service-specific field **Service Product Type** is set correctly.</span></span>

```
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

<span data-ttu-id="25549-115">Følgende værditilknytning anvendes.</span><span class="sxs-lookup"><span data-stu-id="25549-115">The following value mapping is used.</span></span>

```
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

<span data-ttu-id="25549-116">I Finance and Operations beregnes værdien **Field Service-produkttype** på dataenheden **Salgbare frigivne produkter** på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="25549-116">In Finance and Operations, the **Field Service product type** value on the **Sellable released products** data entity is calculated as follows:</span></span>

- <span data-ttu-id="25549-117">**Lager:** Produkttype = Produkt- og varemodelgruppe, Lagerført produkt = Sand</span><span class="sxs-lookup"><span data-stu-id="25549-117">**Inventory:** Product type = Product and Item model group, Stocked product = True</span></span>
- <span data-ttu-id="25549-118">**Ikke-lager:** Produkttype = Produkt- og varemodelgruppe, Lagerført produkt = Falsk</span><span class="sxs-lookup"><span data-stu-id="25549-118">**NonInventory:** Product type = Product and Item model group, Stocked product = False</span></span>
- <span data-ttu-id="25549-119">**Service:** Produkttype = Service</span><span class="sxs-lookup"><span data-stu-id="25549-119">**Service:** Product type = Service</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="25549-120">Skabelontilknytning i dataintegration</span><span class="sxs-lookup"><span data-stu-id="25549-120">Template mapping in Data integration</span></span>

<span data-ttu-id="25549-121">Følgende illustration viser skabelontilknytningen i Dataintegration.</span><span class="sxs-lookup"><span data-stu-id="25549-121">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-fin-and-ops-to-field-service-products---products"></a><span data-ttu-id="25549-122">Field Service-produkter (Fin and Ops til Field Service): Produkter - Produkter</span><span class="sxs-lookup"><span data-stu-id="25549-122">Field Service Products (Fin and Ops to Field Service): Products - Products</span></span>

<span data-ttu-id="25549-123">[![Skabelontilknytning i dataintegration](./media/FSProduct.png)](./media/FSProduct.png)</span><span class="sxs-lookup"><span data-stu-id="25549-123">[![Template mapping in Data integration](./media/FSProduct.png)](./media/FSProduct.png)</span></span>
