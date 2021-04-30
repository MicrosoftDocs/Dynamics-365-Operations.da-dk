---
title: Synkronisere arbejdsordrer med projekt fra Field Service til Supply Chain Management
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere arbejdsordrer med et projektnummer fra Dynamics 365 Field Service til Dynamics 365 Supply Chain Management.
author: ChristianRytt
ms.date: 03/12/2019
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
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 0956e7aa51973014ee474d97829d3d15dfdea3b3
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909937"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-supply-chain-management"></a><span data-ttu-id="c737a-103">Synkronisere arbejdsordrer med projekt fra Field Service til Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="c737a-103">Synchronize work orders with project from Field Service to Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c737a-104">I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere arbejdsordrer med et projektnummer fra Dynamics 365 Field Service til Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c737a-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Dynamics 365 Field Service to Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="c737a-105">[![Synkronisering af forretningsprocesser mellem Supply Chain Management og Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="c737a-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="c737a-106">Den anvendte skabelon **Arbejdsordrer med projekt (Field Service til Supply Chain Management)** er baseret på skabelonen **Arbejdsordrer (Field Service til Supply Chain Management)**.</span><span class="sxs-lookup"><span data-stu-id="c737a-106">The used **Work Orders with Project (Field Service to Supply Chain Management)** template is based on the **Work Orders (Field Service to Supply Chain Management)** template.</span></span> <span data-ttu-id="c737a-107">Du kan finde flere oplysninger i [Synkronisere arbejdsordrer i Field Service med salgsordrer i Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="c737a-107">For more information, see [Synchronize work orders in Field Service to sales orders in Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

<span data-ttu-id="c737a-108">I dette emne beskrives kun forskellene mellem de to skabeloner:</span><span class="sxs-lookup"><span data-stu-id="c737a-108">This topic only describes the differences between the two templates:</span></span>
- <span data-ttu-id="c737a-109">**Arbejdsordrer med projekt (Field Service til Supply Chain Management)**</span><span class="sxs-lookup"><span data-stu-id="c737a-109">**Work Orders with Project (Field Service to Supply Chain Management)**</span></span>
- <span data-ttu-id="c737a-110">**Arbejdsordrer (Field Service til Supply Chain Management)**</span><span class="sxs-lookup"><span data-stu-id="c737a-110">**Work Orders (Field Service to Supply Chain Management)**</span></span>

<span data-ttu-id="c737a-111">Den væsentligste forskel er, at denne skabelon indeholder tilknytning af det projektnummer, der er tildelt arbejdsordren i Field Service. Det sikrer, at salgsordren, der er oprettet i Supply Chain Management, omfatter projektnummeret, og at fakturering kan udføres i det relaterede projekt.</span><span class="sxs-lookup"><span data-stu-id="c737a-111">The main difference is that this template includes mapping of the project number assigned to the Work order in Field Service, ensuring that the Sales order created in Supply Chain Management include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="c737a-112">Derudover bruger skabelonen Avanceret forespørgsel og filtrering.</span><span class="sxs-lookup"><span data-stu-id="c737a-112">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="c737a-113">Skabeloner og opgaver</span><span class="sxs-lookup"><span data-stu-id="c737a-113">Templates and tasks</span></span>

<span data-ttu-id="c737a-114">**Navnet på skabelonen i dataintegration:**</span><span class="sxs-lookup"><span data-stu-id="c737a-114">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="c737a-115">Arbejdsordrer med projekt (Field Service til Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="c737a-115">Work Orders with Project (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="c737a-116">**Navnet på opgaven i dataintegrationsprojektet:**</span><span class="sxs-lookup"><span data-stu-id="c737a-116">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="c737a-117">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="c737a-117">WorkOrderHeader</span></span>
- <span data-ttu-id="c737a-118">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="c737a-118">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="c737a-119">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="c737a-119">WorkOrderProduct</span></span>
- <span data-ttu-id="c737a-120">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="c737a-120">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="c737a-121">CRM-løsning til Field Service</span><span class="sxs-lookup"><span data-stu-id="c737a-121">Field Service CRM solution</span></span>
<span data-ttu-id="c737a-122">Feltet **Eksternt projekt** er føjet til enheden Arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="c737a-122">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="c737a-123">Dette er et opslagsfelt, så hvis du mærker arbejdsordren til et projekt, bliver salgsordren forbundet med et projekt i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c737a-123">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Supply Chain Management.</span></span> <span data-ttu-id="c737a-124">Når **Systemstatus** skifter fra Åben - i gang (690,970,000) til en højere status, låses feltet **Eksternt projekt**, og du kan ikke tilføje, fjerne eller ændre værdien.</span><span class="sxs-lookup"><span data-stu-id="c737a-124">When the **System Status** changes from Open – In Progress(690,970,000) to a higher status, the **External Project** field will be locked and you can't add, remove, or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="c737a-125">Skabelontilknytning i dataintegration</span><span class="sxs-lookup"><span data-stu-id="c737a-125">Template mapping in Data integration</span></span>

<span data-ttu-id="c737a-126">Følgende illustration viser skabelontilknytningen i Dataintegration.</span><span class="sxs-lookup"><span data-stu-id="c737a-126">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheader"></a><span data-ttu-id="c737a-127">Arbejdsordrer med projekt (Field Service til Supply Chain Management): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="c737a-127">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderHeader</span></span>

<span data-ttu-id="c737a-128">[![Skabelontilknytning i dataintegration](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="c737a-128">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheaderproject"></a><span data-ttu-id="c737a-129">Arbejdsordrer med projekt (Field Service til Supply Chain Management): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="c737a-129">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderHeaderProject</span></span>

<span data-ttu-id="c737a-130">[![Skabelontilknytning i dataintegration](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="c737a-130">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderproduct"></a><span data-ttu-id="c737a-131">Arbejdsordrer med projekt (Field Service til Supply Chain Management): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="c737a-131">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderProduct</span></span>

<span data-ttu-id="c737a-132">[![Skabelontilknytning i dataintegration](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="c737a-132">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderservice"></a><span data-ttu-id="c737a-133">Arbejdsordrer med projekt (Field Service til Supply Chain Management): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="c737a-133">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderService</span></span>

<span data-ttu-id="c737a-134">[![Skabelontilknytning i dataintegration](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="c737a-134">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]