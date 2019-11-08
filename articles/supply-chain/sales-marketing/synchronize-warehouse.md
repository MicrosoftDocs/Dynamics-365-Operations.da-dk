---
title: Synkronisere lagersteder fra Supply Chain Management til Field Service
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere lagersteder fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
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
ms.openlocfilehash: b55a0b9e54eabdcdbd3f858cf3725b8fe833f65d
ms.sourcegitcommit: 0099fb24f5f40ff442020b488ef4171836c35c48
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/23/2019
ms.locfileid: "2653388"
---
# <a name="synchronize-warehouses-from-supply-chain-management-to-field-service"></a><span data-ttu-id="b3b28-103">Synkronisere lagersteder fra Supply Chain Management til Field Service</span><span class="sxs-lookup"><span data-stu-id="b3b28-103">Synchronize warehouses from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b3b28-104">I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere lagersteder fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="b3b28-104">This topic discusses the templates and underlying tasks that are used to synchronize warehouses from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="b3b28-105">[![Synkronisering af forretningsprocesser mellem Supply Chain Management og Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span><span class="sxs-lookup"><span data-stu-id="b3b28-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="b3b28-106">Skabeloner og opgaver</span><span class="sxs-lookup"><span data-stu-id="b3b28-106">Templates and tasks</span></span>
<span data-ttu-id="b3b28-107">Følgende skabelon og underliggende opgaver bruges til at synkronisere lagersteder fra Supply Chain Management til Field Service.</span><span class="sxs-lookup"><span data-stu-id="b3b28-107">The following template and underlying tasks are used to run synchronization of warehouses from Supply Chain Management to Field Service.</span></span>

<span data-ttu-id="b3b28-108">**Skabelon i dataintegration**</span><span class="sxs-lookup"><span data-stu-id="b3b28-108">**Template in Data integration**</span></span>
- <span data-ttu-id="b3b28-109">Lagersteder (Supply Chain Management til Field Service)</span><span class="sxs-lookup"><span data-stu-id="b3b28-109">Warehouses (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="b3b28-110">**Opgave i dataintegrationsprojekt**</span><span class="sxs-lookup"><span data-stu-id="b3b28-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="b3b28-111">Lagersted</span><span class="sxs-lookup"><span data-stu-id="b3b28-111">Warehouse</span></span>

## <a name="entity-set"></a><span data-ttu-id="b3b28-112">Enhedssæt</span><span class="sxs-lookup"><span data-stu-id="b3b28-112">Entity set</span></span>
| <span data-ttu-id="b3b28-113">Field Service</span><span class="sxs-lookup"><span data-stu-id="b3b28-113">Field Service</span></span>    | <span data-ttu-id="b3b28-114">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="b3b28-114">Supply Chain Management</span></span>                 |
|------------------|----------------------------------------|
| <span data-ttu-id="b3b28-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="b3b28-115">msdyn_warehouses</span></span> | <span data-ttu-id="b3b28-116">Lagersteder</span><span class="sxs-lookup"><span data-stu-id="b3b28-116">Warehouses</span></span>                             |

## <a name="entity-flow"></a><span data-ttu-id="b3b28-117">Enhedsflow</span><span class="sxs-lookup"><span data-stu-id="b3b28-117">Entity flow</span></span>
<span data-ttu-id="b3b28-118">Lagersteder, der oprettes og vedligeholdes i Supply Chain Management, kan synkroniseres til Field Service via et Common Data Service-dataintegrationsprojekt (CDS).</span><span class="sxs-lookup"><span data-stu-id="b3b28-118">Warehouses that are created and maintained in Supply Chain Management can be synchronized to Field Service via a Common Data Service (CDS) Data integration project.</span></span> <span data-ttu-id="b3b28-119">De lagersteder, du vil synkronisere til Field Service, kan styres med Avanceret forespørgsel og filtrering i projektet.</span><span class="sxs-lookup"><span data-stu-id="b3b28-119">The warehouses that you want to synchronize to Field Service can be controlled with the Advanced query and filtering on the project.</span></span> <span data-ttu-id="b3b28-120">Lagersteder, der synkroniseres fra Supply Chain Management, oprettes i Field Service med feltet **Vedligeholdes eksternt** indstillet til **Ja**, og posten skrivebeskyttes.</span><span class="sxs-lookup"><span data-stu-id="b3b28-120">Warehouses that synchronize from Supply Chain Management are created in Field Service with the **Is maintained externally** field set to **Yes** and the record is read only.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="b3b28-121">CRM-løsning til Field Service</span><span class="sxs-lookup"><span data-stu-id="b3b28-121">Field Service CRM solution</span></span>
<span data-ttu-id="b3b28-122">For at understøtte integrationen mellem Field Service og Supply Chain Management kræves der yderligere funktionalitet fra CRM-løsningen i Field Service.</span><span class="sxs-lookup"><span data-stu-id="b3b28-122">To support the integration between Field Service and Supply Chain Management, additional functionality from the Field Service CRM solution is required.</span></span> <span data-ttu-id="b3b28-123">I løsningen er feltet **Vedligeholdes eksternt** blevet føjet til enheden **Lagersted (msdyn_warehouses)**.</span><span class="sxs-lookup"><span data-stu-id="b3b28-123">In the solution, the **Is Maintained Externally** field has been added to the **Warehouse (msdyn_warehouses)** entity.</span></span> <span data-ttu-id="b3b28-124">Dette felt bruges til at identificere, om lagerstedet håndteres fra Supply Chain Management, eller om det kun findes i Field Service.</span><span class="sxs-lookup"><span data-stu-id="b3b28-124">This field helps to identify if the warehouse is handled from Supply Chain Management or if it only exists in Field Service.</span></span> <span data-ttu-id="b3b28-125">Indstillingerne for dette felt omfatter:</span><span class="sxs-lookup"><span data-stu-id="b3b28-125">The settings for this field include:</span></span>
- <span data-ttu-id="b3b28-126">**Ja** – Lagerstedet stammer fra Supply Chain Management, og det kan ikke redigeres i Sales.</span><span class="sxs-lookup"><span data-stu-id="b3b28-126">**Yes** – The warehouse originated from Supply Chain Management and won't be editable in Sales.</span></span>
- <span data-ttu-id="b3b28-127">**Nej** – Lagerstedet er angivet direkte i Field Service og vedligeholdes her.</span><span class="sxs-lookup"><span data-stu-id="b3b28-127">**No** – The warehouse was entered directly in Field Service and is maintained here.</span></span>

<span data-ttu-id="b3b28-128">Feltet **Vedligeholdes eksternt** hjælper med at styre synkroniseringen af lagerniveauer, reguleringer, overførsler og brug i arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="b3b28-128">The **Is Externally Maintained** field helps control the synchronization of inventory levels, adjustments, transfers, and usage on work orders.</span></span> <span data-ttu-id="b3b28-129">Kun lagersteder, hvor **Vedligeholdes eksternt** er indstillet til **Ja**, kan bruges til at synkronisere direkte til det samme lagersted i andet system.</span><span class="sxs-lookup"><span data-stu-id="b3b28-129">Only warehouses with **Is Externally Maintained** set to **Yes** can be used to synchronize directly to the same warehouse in the other system.</span></span> 

> [!NOTE]
> <span data-ttu-id="b3b28-130">Det er muligt at oprette flere lagersteder i Field Service (med **Vedligeholdes eksternt** = Nej) og derefter knytte dem til et enkelt lagersted med funktionen Avanceret forespørgsel og filtrering.</span><span class="sxs-lookup"><span data-stu-id="b3b28-130">It is possible to create multiple warehouses in Field Service (with **Is Externally Maintained** = No) and then map them to a single warehouse, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="b3b28-131">Dette bruges i situationer, hvor Field Service skal mestre det detaljerede lagerniveau og kun sende opdateringer til Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b3b28-131">This is used in situations where you want Field Service to master the detailed inventory level and just send updates to Supply Chain Management.</span></span> <span data-ttu-id="b3b28-132">I dette tilfælde modtager Field Service ikke lagerniveauopdateringer fra Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b3b28-132">In this case, Field Service will not receive inventory-level updates from Supply Chain Management.</span></span> <span data-ttu-id="b3b28-133">Du kan se flere oplysninger i [Synkroniser lagerreguleringer fra Field Service til Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) og [Synkronisere arbejdsordrer i Field Service med salgsordrer, der er knyttet til projektet i Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="b3b28-133">For additional information, see [Synchronize inventory adjustments from Field Service to Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="b3b28-134">Forudsætninger og tilknytningsopsætning</span><span class="sxs-lookup"><span data-stu-id="b3b28-134">Prerequisites and mapping setup</span></span>
### <a name="data-integration-project"></a><span data-ttu-id="b3b28-135">Dataintegrationsprojekt</span><span class="sxs-lookup"><span data-stu-id="b3b28-135">Data Integration project</span></span>
<span data-ttu-id="b3b28-136">Inden du synkroniserer lagerstederne, skal du sørge for at opdatere Avanceret forespørgsel og filtrering i projektet, så kun de lagersteder, du vil overføre fra Supply Chain Management til Field Service, medtages.</span><span class="sxs-lookup"><span data-stu-id="b3b28-136">Before synchronizing the warehouses, make sure to update the Advanced query and filtering on the project to only include the warehouses that you want to bring from Supply Chain Management to Field Service.</span></span> <span data-ttu-id="b3b28-137">Bemærk, at du skal bruge lagerstedet i Field Service og anvende det på arbejdsordrer, reguleringer og overførsler.</span><span class="sxs-lookup"><span data-stu-id="b3b28-137">Note that you will need the warehouse in Field Service to apply it on work orders, adjustments, and transfers.</span></span>  

<span data-ttu-id="b3b28-138">Gør følgende for at sørge for, at der findes en **Integrationsnøgle** for **msdyn_warehouses**:</span><span class="sxs-lookup"><span data-stu-id="b3b28-138">To ensure that the **Integration key** exists for **msdyn_warehouses**:</span></span>
1. <span data-ttu-id="b3b28-139">Gå til Dataintegration.</span><span class="sxs-lookup"><span data-stu-id="b3b28-139">Go to Data Integration.</span></span>
2. <span data-ttu-id="b3b28-140">Vælg fanen **Forbindelsessæt**.</span><span class="sxs-lookup"><span data-stu-id="b3b28-140">Select the **Connection Set** tab.</span></span>
3. <span data-ttu-id="b3b28-141">Vælg det forbindelsessæt, der bruges til synkronisering af arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="b3b28-141">Select the connection set used for work order synchronization.</span></span>
4. <span data-ttu-id="b3b28-142">Vælg fanen **Integrationsnøgle**.</span><span class="sxs-lookup"><span data-stu-id="b3b28-142">Select the **Integration key** tab.</span></span>
5. <span data-ttu-id="b3b28-143">Find msdyn_warehouses, og kontroller, at nøglen **msdyn_name (navn)** er tilføjet.</span><span class="sxs-lookup"><span data-stu-id="b3b28-143">Find msdyn_warehouses and confirm that the key **msdyn_name (name)** is added.</span></span> <span data-ttu-id="b3b28-144">Hvis den ikke vises, skal du tilføje den ved at klikke på **Tilføj nøgle** og derefter klikke på **Gem** øverst på siden.</span><span class="sxs-lookup"><span data-stu-id="b3b28-144">If it is not shown, add it by clicking **Add key** and then click **Save** at the top of the page.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="b3b28-145">Skabelontilknytning i dataintegration</span><span class="sxs-lookup"><span data-stu-id="b3b28-145">Template mapping in Data integration</span></span>

<span data-ttu-id="b3b28-146">Følgende illustration viser skabelontilknytningen i Dataintegration.</span><span class="sxs-lookup"><span data-stu-id="b3b28-146">The following illustration shows the template mapping in Data integration.</span></span>

### <a name="warehouses-supply-chain-management-to-field-service-warehouse"></a><span data-ttu-id="b3b28-147">Lagersteder (Supply Chain Management til Field Service): Lagersted</span><span class="sxs-lookup"><span data-stu-id="b3b28-147">Warehouses (Supply Chain Management to Field Service): Warehouse</span></span>

<span data-ttu-id="b3b28-148">[![Skabelontilknytning i dataintegration](./media/Warehouse1.png)](./media/Warehouse1.png)</span><span class="sxs-lookup"><span data-stu-id="b3b28-148">[![Template mapping in Data integration](./media/Warehouse1.png)](./media/Warehouse1.png)</span></span>
