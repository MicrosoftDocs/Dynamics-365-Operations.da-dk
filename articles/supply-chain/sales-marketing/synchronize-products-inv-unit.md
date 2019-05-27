---
title: Synkronisere produkter med lagerenhed fra Finance and Operations til Field Service
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere produkter med lagerenhed fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
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
ms.openlocfilehash: 080672b9a6acd9fd6137580b5b7e14d12cfccf19
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/07/2019
ms.locfileid: "1535853"
---
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a><span data-ttu-id="0fa51-103">Synkronisere produkter med lagerenhed fra Finance and Operations til Field Service</span><span class="sxs-lookup"><span data-stu-id="0fa51-103">Synchronize products with inventory unit from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0fa51-104">I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere produkter med lagerenhed fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="0fa51-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="0fa51-105">[![Synkronisering af forretningsprocesser mellem Finance and Operations og Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="0fa51-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="0fa51-106">Den anvendte skabelon **Field Service-produkter med lagerenhed (Fin and Ops til Field Service)** er baseret på skabelonen **Field Service-produkter (Fin and Ops til Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="0fa51-106">The used **Field Service Products with Inventory unit (Fin and Ops to Field Service)** template is based on the **Field Service Products (Fin and Ops to Field Service)** template.</span></span> <span data-ttu-id="0fa51-107">Yderligere oplysninger finder du i [Field Service-produkter (Finance and Operations til Field Service)](field-service-product.md).</span><span class="sxs-lookup"><span data-stu-id="0fa51-107">For more information, see [Field Service Products (Finance and Operations to Field Service)](field-service-product.md).</span></span>

<span data-ttu-id="0fa51-108">I dette emne beskrives kun forskellene mellem de to skabeloner:</span><span class="sxs-lookup"><span data-stu-id="0fa51-108">This topic only describes the differences between the two templates:</span></span> 
- <span data-ttu-id="0fa51-109">**Field Service-produkter med lagerenhed (Fin and Ops til salg)**</span><span class="sxs-lookup"><span data-stu-id="0fa51-109">**Field Service Products with Inventory unit (Fin and Ops to Sales)**</span></span>
- <span data-ttu-id="0fa51-110">**Field Service-produkter (Fin and Ops til Field Service)**</span><span class="sxs-lookup"><span data-stu-id="0fa51-110">**Field Service Products (Fin and Ops to Field Service)**</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="0fa51-111">Skabeloner og opgaver</span><span class="sxs-lookup"><span data-stu-id="0fa51-111">Templates and tasks</span></span>

<span data-ttu-id="0fa51-112">**Navnet på skabelonen i dataintegration:**</span><span class="sxs-lookup"><span data-stu-id="0fa51-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="0fa51-113">Field Service-produkter med lagerenhed (Fin and Ops til salg)</span><span class="sxs-lookup"><span data-stu-id="0fa51-113">Field Service Products with Inventory unit (Fin and Ops to Sales)</span></span>

<span data-ttu-id="0fa51-114">**Navnet på opgaven i dataintegrationsprojektet:**</span><span class="sxs-lookup"><span data-stu-id="0fa51-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="0fa51-115">Produkter</span><span class="sxs-lookup"><span data-stu-id="0fa51-115">Products</span></span>

<span data-ttu-id="0fa51-116">Skabelonen **Field Service-produkter med lagerenhed (Fin and Ops til Field Service)** indeholder et felt, der ikke er omfattet af skabelonen **Field Service-produkter (Fin and Ops til Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="0fa51-116">The **Field Service Products with Inventory unit (Fin and Ops to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Fin and Ops to Field Service)** template.</span></span> <span data-ttu-id="0fa51-117">Denne tilknytning sikrer, at den lagerenhed, der skal bruges til synkronisering på lagerniveau, er inkluderet.</span><span class="sxs-lookup"><span data-stu-id="0fa51-117">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="0fa51-118">Skabelontilknytning i dataintegration</span><span class="sxs-lookup"><span data-stu-id="0fa51-118">Template mapping in Data integration</span></span>

<span data-ttu-id="0fa51-119">Følgende illustration viser skabelontilknytningen i Dataintegration.</span><span class="sxs-lookup"><span data-stu-id="0fa51-119">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-fin-and-ops-to-field-service-products"></a><span data-ttu-id="0fa51-120">Field Service-produkter med lagerenhed (Fin and Ops til Field Service): produkter</span><span class="sxs-lookup"><span data-stu-id="0fa51-120">Field Service Products with Inventory unit (Fin and Ops to Field Service): Products</span></span>

<span data-ttu-id="0fa51-121">[![Skabelontilknytning i dataintegration](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="0fa51-121">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>
