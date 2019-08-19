---
title: Synkronisere arbejdsordrer med et projektnummer fra Field Service til Finance and Operations
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere arbejdsordrer med et projektnummer fra Microsoft Dynamics 365 for Field Service til Microsoft Dynamics 365 for Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 03/12/2019
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
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 77358513ffdf791ab10d6efe1b84f598ffb5ec26
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843403"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a><span data-ttu-id="5fe20-103">Synkronisere arbejdsordrer med et projektnummer fra Field Service til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5fe20-103">Synchronize work orders with project from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="5fe20-104">I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere arbejdsordrer med et projektnummer fra Microsoft Dynamics 365 for Field Service til Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5fe20-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="5fe20-105">[![Synkronisering af forretningsprocesser mellem Finance and Operations og Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="5fe20-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="5fe20-106">Den anvendte skabelon **Arbejdsordrer med projekt (Field Service til Finance and Operations)** er baseret på skabelonen **Arbejdsordrer (Field Service til Finance and Operations)**.</span><span class="sxs-lookup"><span data-stu-id="5fe20-106">The used **Work Orders with Project (Field Service to Fin and Ops)** template is based on the **Work Orders (Field Service to Fin and Ops)** template.</span></span> <span data-ttu-id="5fe20-107">Du kan finde flere oplysninger i [Synkronisere arbejdsordrer i Field Service med salgsordrer i Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="5fe20-107">For more information, see [Synchronize work orders in Field Service to sales orders in Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

<span data-ttu-id="5fe20-108">I dette emne beskrives kun forskellene mellem de to skabeloner:</span><span class="sxs-lookup"><span data-stu-id="5fe20-108">This topic only describes the differences between the two templates:</span></span>
- <span data-ttu-id="5fe20-109">**Arbejdsordrer med projekt (Field Service til Finance and Operations)**</span><span class="sxs-lookup"><span data-stu-id="5fe20-109">**Work Orders with Project (Field Service to Fin and Ops)**</span></span>
- <span data-ttu-id="5fe20-110">**Arbejdsordrer (Field Service til Finance and Operations)**</span><span class="sxs-lookup"><span data-stu-id="5fe20-110">**Work Orders (Field Service to Fin and Ops)**</span></span>

<span data-ttu-id="5fe20-111">Den væsentligste forskel er, at denne skabelon indeholder tilknytning af det projektnummer, der er tildelt til arbejdsordren i Field Service. Det sikrer, at salgsordren, der er oprettet i Finance and Operations, omfatter projektnummeret, og at fakturering kan udføres i det relaterede projekt.</span><span class="sxs-lookup"><span data-stu-id="5fe20-111">The main difference is that this template includes mapping of the project number asigned to the Work order in Field Service, ensuring that the Sales order created in Finance and Operations include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="5fe20-112">Derudover bruger skabelonen Avanceret forespørgsel og filtrering.</span><span class="sxs-lookup"><span data-stu-id="5fe20-112">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="5fe20-113">Skabeloner og opgaver</span><span class="sxs-lookup"><span data-stu-id="5fe20-113">Templates and tasks</span></span>

<span data-ttu-id="5fe20-114">**Navnet på skabelonen i dataintegration:**</span><span class="sxs-lookup"><span data-stu-id="5fe20-114">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="5fe20-115">Arbejdsordrer med projekt (Field Service til Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="5fe20-115">Work Orders with Project (Field Service to Fin and Ops)</span></span>

<span data-ttu-id="5fe20-116">**Navnet på opgaven i dataintegrationsprojektet:**</span><span class="sxs-lookup"><span data-stu-id="5fe20-116">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="5fe20-117">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="5fe20-117">WorkOrderHeader</span></span>
- <span data-ttu-id="5fe20-118">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="5fe20-118">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="5fe20-119">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="5fe20-119">WorkOrderProduct</span></span>
- <span data-ttu-id="5fe20-120">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="5fe20-120">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="5fe20-121">CRM-løsning til Field Service</span><span class="sxs-lookup"><span data-stu-id="5fe20-121">Field Service CRM solution</span></span>
<span data-ttu-id="5fe20-122">Feltet **Eksternt projekt** er føjet til enheden Arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="5fe20-122">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="5fe20-123">Dette er et find og køb-felt, som mærker arbejdsordren til et projekt. Salgsordren bliver derefter forbundet med et projekt i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5fe20-123">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Finance and Operations.</span></span> <span data-ttu-id="5fe20-124">Når **Systemstatus** skifter fra Åben - i gang (690,970,000) til en højere status, låses feltet **Eksternt projekt**, og du kan ikke tilføje, fjerne eller ændre værdien.</span><span class="sxs-lookup"><span data-stu-id="5fe20-124">Ones the **System Status** changes from Open – In Progress(690,970,000) to a higher status the **External Project** field will be locked and you can't add, remove or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="5fe20-125">Skabelontilknytning i dataintegration</span><span class="sxs-lookup"><span data-stu-id="5fe20-125">Template mapping in Data integration</span></span>

<span data-ttu-id="5fe20-126">Følgende illustration viser skabelontilknytningen i Dataintegration.</span><span class="sxs-lookup"><span data-stu-id="5fe20-126">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheader"></a><span data-ttu-id="5fe20-127">Arbejdsordrer med projekt (Field Service til Finance and Operations): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="5fe20-127">Work Orders with Project (Field Service to Fin and Ops): WorkOrderHeader</span></span>

<span data-ttu-id="5fe20-128">[![Skabelontilknytning i dataintegration](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="5fe20-128">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheaderproject"></a><span data-ttu-id="5fe20-129">Arbejdsordrer med projekt (Field Service til Finance and Operations): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="5fe20-129">Work Orders with Project (Field Service to Fin and Ops): WorkOrderHeaderProject</span></span>

<span data-ttu-id="5fe20-130">[![Skabelontilknytning i dataintegration](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="5fe20-130">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderproduct"></a><span data-ttu-id="5fe20-131">Arbejdsordrer med projekt (Field Service til Finance and Operations): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="5fe20-131">Work Orders with Project (Field Service to Fin and Ops): WorkOrderProduct</span></span>

<span data-ttu-id="5fe20-132">[![Skabelontilknytning i dataintegration](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="5fe20-132">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderservice"></a><span data-ttu-id="5fe20-133">Arbejdsordrer med projekt (Field Service til Finance and Operations): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="5fe20-133">Work Orders with Project (Field Service to Fin and Ops): WorkOrderService</span></span>

<span data-ttu-id="5fe20-134">[![Skabelontilknytning i dataintegration](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="5fe20-134">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>
