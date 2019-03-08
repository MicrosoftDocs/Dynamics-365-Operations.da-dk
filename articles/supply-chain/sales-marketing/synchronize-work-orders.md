---
title: Synkronisere arbejdsordrer med et projektnummer fra Field Service til Finance and Operations
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere arbejdsordrer med et projektnummer fra Microsoft Dynamics 365 for Field Service til Microsoft Dynamics 365 for Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
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
ms.openlocfilehash: 6b61411a5a235e2d0aad8bb25ae4a3bfcf1248d1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "329844"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a><span data-ttu-id="5a01f-103">Synkronisere arbejdsordrer med et projektnummer fra Field Service til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5a01f-103">Synchronize work orders with project from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="5a01f-104">I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere arbejdsordrer med et projektnummer fra Microsoft Dynamics 365 for Field Service til Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5a01f-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="5a01f-105">[![Synkronisering af forretningsprocesser mellem Finance and Operations og Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="5a01f-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="5a01f-106">Den anvendte skabelon **Field Service-produkter (Finance and Operations til Field Service)** er baseret på skabelonen **Produkter (Finance and Operations til Sales) – Direkte** fra Kundeemne til kontanter.</span><span class="sxs-lookup"><span data-stu-id="5a01f-106">The used **Field Service Products (Finance and Operations to Field Service)** template is based on the **Products (Finance and Operations to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="5a01f-107">Yderligere oplysninger finder du i [Produkter (Finance and Operations til Sales) – Direkte](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="5a01f-107">For more information, see [Products (Finance and Operations to Sales) – Direct](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="5a01f-108">Dette emne omhandler kun forskellene mellem skabelonerne **Field Service-produkter (Finance and Operations til Field Service)** og **Produkter (Finance and Operations til Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="5a01f-108">This topic only describes the differences between the **Field Service Products (Finance and Operations to Field Service)** and **Field Service Products (Finance and Operations to Field Service)** templates.</span></span>

<span data-ttu-id="5a01f-109">Den væsentligste forskel er, at denne skabelon indeholder tilknytning af det projektnummer, der er tildelt til arbejdsordren i Field Service. Det sikrer, at salgsordren, der er oprettet i Finance and Operations, omfatter projektnummeret, og at fakturering kan udføres i det relaterede projekt.</span><span class="sxs-lookup"><span data-stu-id="5a01f-109">The main difference is that this template includes mapping of the project number asigned to the Work order in Field Service, ensuring that the Sales order created in Finance and Operations include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="5a01f-110">Derudover bruger skabelonen Avanceret forespørgsel og filtrering.</span><span class="sxs-lookup"><span data-stu-id="5a01f-110">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="5a01f-111">Skabeloner og opgaver</span><span class="sxs-lookup"><span data-stu-id="5a01f-111">Templates and tasks</span></span>

<span data-ttu-id="5a01f-112">**Navnet på skabelonen i dataintegration:**</span><span class="sxs-lookup"><span data-stu-id="5a01f-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="5a01f-113">Arbejdsordrer med projekt (Field Service til Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="5a01f-113">Work Orders with Project (Field Service to Finance and Operations)</span></span>

<span data-ttu-id="5a01f-114">**Navnet på opgaven i dataintegrationsprojektet:**</span><span class="sxs-lookup"><span data-stu-id="5a01f-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="5a01f-115">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="5a01f-115">WorkOrderHeader</span></span>
- <span data-ttu-id="5a01f-116">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="5a01f-116">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="5a01f-117">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="5a01f-117">WorkOrderProduct</span></span>
- <span data-ttu-id="5a01f-118">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="5a01f-118">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="5a01f-119">CRM-løsning til Field Service</span><span class="sxs-lookup"><span data-stu-id="5a01f-119">Field Service CRM solution</span></span>
<span data-ttu-id="5a01f-120">Feltet **Eksternt projekt** er føjet til enheden Arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="5a01f-120">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="5a01f-121">Dette er et find og køb-felt, som mærker arbejdsordren til et projekt. Salgsordren bliver derefter forbundet med et projekt i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5a01f-121">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Finance and Operations.</span></span> <span data-ttu-id="5a01f-122">Når **Systemstatus** skifter fra Åben - i gang (690,970,000) til en højere status, låses feltet **Eksternt projekt**, og du kan ikke tilføje, fjerne eller ændre værdien.</span><span class="sxs-lookup"><span data-stu-id="5a01f-122">Ones the **System Status** changes from Open – In Progress(690,970,000) to a higher status the **External Project** field will be locked and you can't add, remove or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="5a01f-123">Skabelontilknytning i dataintegration</span><span class="sxs-lookup"><span data-stu-id="5a01f-123">Template mapping in Data integration</span></span>

<span data-ttu-id="5a01f-124">Følgende illustration viser skabelontilknytningen i Dataintegration.</span><span class="sxs-lookup"><span data-stu-id="5a01f-124">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheader"></a><span data-ttu-id="5a01f-125">Arbejdsordrer med projekt (Field Service til Finance and Operations): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="5a01f-125">Work Orders with Project (Field Service to Finance and Operations): WorkOrderHeader</span></span>

<span data-ttu-id="5a01f-126">[![Skabelontilknytning i dataintegration](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="5a01f-126">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheaderproject"></a><span data-ttu-id="5a01f-127">Arbejdsordrer med projekt (Field Service til Finance and Operations): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="5a01f-127">Work Orders with Project (Field Service to Finance and Operations): WorkOrderHeaderProject</span></span>

<span data-ttu-id="5a01f-128">[![Skabelontilknytning i dataintegration](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="5a01f-128">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderproduct"></a><span data-ttu-id="5a01f-129">Arbejdsordrer med projekt (Field Service til Finance and Operations): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="5a01f-129">Work Orders with Project (Field Service to Finance and Operations): WorkOrderProduct</span></span>

<span data-ttu-id="5a01f-130">[![Skabelontilknytning i dataintegration](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="5a01f-130">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderservice"></a><span data-ttu-id="5a01f-131">Arbejdsordrer med projekt (Field Service til Finance and Operations): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="5a01f-131">Work Orders with Project (Field Service to Finance and Operations): WorkOrderService</span></span>

<span data-ttu-id="5a01f-132">[![Skabelontilknytning i dataintegration](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="5a01f-132">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>
