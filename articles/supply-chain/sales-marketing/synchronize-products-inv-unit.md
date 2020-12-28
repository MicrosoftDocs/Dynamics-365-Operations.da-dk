---
title: Synkronisere produkter med lagerenhed fra Supply Chain Management til Field Service
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere produkter med lagerenhed fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.
author: ChristianRytt
manager: tfehr
ms.date: 03/13/2019
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
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 911c5cc79ae359bbb77d31f366ccfeabf282a33e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424772"
---
# <a name="synchronize-products-with-inventory-unit-from-supply-chain-management-to-field-service"></a><span data-ttu-id="8d69a-103">Synkronisere produkter med lagerenhed fra Supply Chain Management til Field Service</span><span class="sxs-lookup"><span data-stu-id="8d69a-103">Synchronize products with inventory unit from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="8d69a-104">I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere produkter med lagerenhed fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="8d69a-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="8d69a-105">[![Synkronisering af forretningsprocesser mellem Supply Chain Management og Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="8d69a-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="8d69a-106">Den anvendte skabelon **Field Service-produkter med lagerenhed (Supply Chain Management til Field Service)** er baseret på skabelonen **Field Service-produkter (Supply Chain Management til Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="8d69a-106">The used **Field Service Products with Inventory unit (Supply Chain Management to Field Service)** template is based on the **Field Service Products (Supply Chain Management to Field Service)** template.</span></span> <span data-ttu-id="8d69a-107">Du kan finde flere oplysninger i [Synkroniser produkter i Supply Chain Management med produkter i Field Service](field-service-product.md).</span><span class="sxs-lookup"><span data-stu-id="8d69a-107">For more information, see [Synchronize products in Supply Chain Management to products in Field Service](field-service-product.md).</span></span>

<span data-ttu-id="8d69a-108">I dette emne beskrives kun forskellene mellem de to skabeloner:</span><span class="sxs-lookup"><span data-stu-id="8d69a-108">This topic only describes the differences between the two templates:</span></span> 
- <span data-ttu-id="8d69a-109">**Field Service-produkter med lagerenhed (Supply Chain Management til Sales)**</span><span class="sxs-lookup"><span data-stu-id="8d69a-109">**Field Service Products with Inventory unit (Supply Chain Management to Sales)**</span></span>
- <span data-ttu-id="8d69a-110">**Field Service-produkter (Supply Chain Management til Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="8d69a-110">**Field Service Products (Supply Chain Management to Field Service)**</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="8d69a-111">Skabeloner og opgaver</span><span class="sxs-lookup"><span data-stu-id="8d69a-111">Templates and tasks</span></span>

<span data-ttu-id="8d69a-112">**Navnet på skabelonen i dataintegration:**</span><span class="sxs-lookup"><span data-stu-id="8d69a-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="8d69a-113">Field Service-produkter med lagerenhed (Supply Chain Management til Sales)</span><span class="sxs-lookup"><span data-stu-id="8d69a-113">Field Service Products with Inventory unit (Supply Chain Management to Sales)</span></span>

<span data-ttu-id="8d69a-114">**Navnet på opgaven i dataintegrationsprojektet:**</span><span class="sxs-lookup"><span data-stu-id="8d69a-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="8d69a-115">Produkter</span><span class="sxs-lookup"><span data-stu-id="8d69a-115">Products</span></span>

<span data-ttu-id="8d69a-116">Skabelonen **Field Service-produkter med lagerenhed (Supply Chain Management til Field Service)** indeholder én tilknytning, der ikke er medtaget i skabelonen **Field Service-produkter (Supply Chain Management til Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="8d69a-116">The **Field Service Products with Inventory unit (Supply Chain Management to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Supply Chain Management to Field Service)** template.</span></span> <span data-ttu-id="8d69a-117">Denne tilknytning sikrer, at den lagerenhed, der skal bruges til synkronisering på lagerniveau, er inkluderet.</span><span class="sxs-lookup"><span data-stu-id="8d69a-117">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```plaintext
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="8d69a-118">Skabelontilknytning i dataintegration</span><span class="sxs-lookup"><span data-stu-id="8d69a-118">Template mapping in Data integration</span></span>

<span data-ttu-id="8d69a-119">Følgende illustration viser skabelontilknytningen i Dataintegration.</span><span class="sxs-lookup"><span data-stu-id="8d69a-119">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-supply-chain-management-to-field-service-products"></a><span data-ttu-id="8d69a-120">Field Service-produkter med lagerenhed (Supply Chain Management til Field Service): Produkter</span><span class="sxs-lookup"><span data-stu-id="8d69a-120">Field Service Products with Inventory unit (Supply Chain Management to Field Service): Products</span></span>

<span data-ttu-id="8d69a-121">[![Skabelontilknytning i dataintegration](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="8d69a-121">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>
