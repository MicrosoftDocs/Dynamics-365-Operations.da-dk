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
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a><span data-ttu-id="9a3e2-103">Synkronisere produkter med lagerenhed fra Finance and Operations til Field Service</span><span class="sxs-lookup"><span data-stu-id="9a3e2-103">Synchronize products with inventory unit from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="9a3e2-104">I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere produkter med lagerenhed fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="9a3e2-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="9a3e2-105">[![Synkronisering af forretningsprocesser mellem Finance and Operations og Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="9a3e2-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="9a3e2-106">Den anvendte **Field Service-produkter med lagerenhed (Finance and Operations til Field Service)**-skabelon er baseret på skabelonen **Field Service-produkter (Finance and Operations til Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="9a3e2-106">The used **Field Service Products with Inventory unit (Finance and Operations to Field Service)** template is based on the **Field Service Products (Finance and Operations to Field Service)** template.</span></span> <span data-ttu-id="9a3e2-107">Yderligere oplysninger finder du i [Field Service-produkter (Finance and Operations til Field Service)](field-service-product.md).</span><span class="sxs-lookup"><span data-stu-id="9a3e2-107">For more information, see [Field Service Products (Finance and Operations to Field Service)](field-service-product.md).</span></span>

<span data-ttu-id="9a3e2-108">I dette emne beskrives kun forskellene mellem de to skabeloner:</span><span class="sxs-lookup"><span data-stu-id="9a3e2-108">This topic only describes the differences between the two templates:</span></span> 
- <span data-ttu-id="9a3e2-109">**Field Service-produkter med lagerenhed (Finance and Operations til Sales)**</span><span class="sxs-lookup"><span data-stu-id="9a3e2-109">**Field Service Products with Inventory unit (Finance and Operations to Sales)**</span></span>
- <span data-ttu-id="9a3e2-110">**Field Service-produkter (Finance and Operations til Field Service)**</span><span class="sxs-lookup"><span data-stu-id="9a3e2-110">**Field Service Products (Finance and Operations to Field Service)**</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="9a3e2-111">Skabeloner og opgaver</span><span class="sxs-lookup"><span data-stu-id="9a3e2-111">Templates and tasks</span></span>

<span data-ttu-id="9a3e2-112">**Navnet på skabelonen i dataintegration:**</span><span class="sxs-lookup"><span data-stu-id="9a3e2-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="9a3e2-113">Field Service-produkter med lagerenhed (Finance and Operations til Sales)</span><span class="sxs-lookup"><span data-stu-id="9a3e2-113">Field Service Products with Inventory unit (Finance and Operations to Sales)</span></span>

<span data-ttu-id="9a3e2-114">**Navnet på opgaven i dataintegrationsprojektet:**</span><span class="sxs-lookup"><span data-stu-id="9a3e2-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="9a3e2-115">Produkter</span><span class="sxs-lookup"><span data-stu-id="9a3e2-115">Products</span></span>

<span data-ttu-id="9a3e2-116">Skabelonen **Field Service-produkter med lagerenhed (Finance and Operations til Field Service)** indeholder én tilknytning, der ikke findes i skabelonen **Field Service-produkter (Finance and Operations til Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="9a3e2-116">The **Field Service Products with Inventory unit (Finance and Operations to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Finance and Operations to Field Service)** template.</span></span> <span data-ttu-id="9a3e2-117">Denne tilknytning sikrer, at den lagerenhed, der skal bruges til synkronisering på lagerniveau, er inkluderet.</span><span class="sxs-lookup"><span data-stu-id="9a3e2-117">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="9a3e2-118">Skabelontilknytning i dataintegration</span><span class="sxs-lookup"><span data-stu-id="9a3e2-118">Template mapping in Data integration</span></span>

<span data-ttu-id="9a3e2-119">Følgende illustration viser skabelontilknytningen i Dataintegration.</span><span class="sxs-lookup"><span data-stu-id="9a3e2-119">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-finance-and-operations-to-field-service-products"></a><span data-ttu-id="9a3e2-120">Field Service-produkter med lagerenhed (Finance and Operations til Field Service): Produkter</span><span class="sxs-lookup"><span data-stu-id="9a3e2-120">Field Service Products with Inventory unit (Finance and Operations to Field Service): Products</span></span>

<span data-ttu-id="9a3e2-121">[![Skabelontilknytning i dataintegration](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="9a3e2-121">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>
