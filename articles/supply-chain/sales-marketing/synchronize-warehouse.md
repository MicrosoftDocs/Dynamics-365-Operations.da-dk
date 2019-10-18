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
ms.openlocfilehash: 94fb6720152cbf6aec58d2b8d9d02fc5343c05e2
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251172"
---
# <a name="synchronize-warehouses-from-supply-chain-management-to-field-service"></a><span data-ttu-id="9c03c-103">Synkronisere lagersteder fra Supply Chain Management til Field Service</span><span class="sxs-lookup"><span data-stu-id="9c03c-103">Synchronize warehouses from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="9c03c-104">I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere lagersteder fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="9c03c-104">This topic discusses the templates and underlying tasks that are used to synchronize warehouses from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="9c03c-105">[![Synkronisering af forretningsprocesser mellem Supply Chain Management og Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span><span class="sxs-lookup"><span data-stu-id="9c03c-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="9c03c-106">Skabeloner og opgaver</span><span class="sxs-lookup"><span data-stu-id="9c03c-106">Templates and tasks</span></span>
<span data-ttu-id="9c03c-107">Følgende skabelon og underliggende opgaver bruges til at synkronisere lagersteder fra Supply Chain Management til Field Service.</span><span class="sxs-lookup"><span data-stu-id="9c03c-107">The following template and underlying tasks are used to run synchronization of warehouses from Supply Chain Management to Field Service.</span></span>

<span data-ttu-id="9c03c-108">**Skabelon i dataintegration**</span><span class="sxs-lookup"><span data-stu-id="9c03c-108">**Template in Data integration**</span></span>
- <span data-ttu-id="9c03c-109">Lagersteder (Supply Chain Management til Field Service)</span><span class="sxs-lookup"><span data-stu-id="9c03c-109">Warehouses (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="9c03c-110">**Opgave i dataintegrationsprojekt**</span><span class="sxs-lookup"><span data-stu-id="9c03c-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="9c03c-111">Lagersted</span><span class="sxs-lookup"><span data-stu-id="9c03c-111">Warehouse</span></span>

## <a name="entity-set"></a><span data-ttu-id="9c03c-112">Enhedssæt</span><span class="sxs-lookup"><span data-stu-id="9c03c-112">Entity set</span></span>
| <span data-ttu-id="9c03c-113">Field Service</span><span class="sxs-lookup"><span data-stu-id="9c03c-113">Field Service</span></span>    | <span data-ttu-id="9c03c-114">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="9c03c-114">Supply Chain Management</span></span>                 |
|------------------|----------------------------------------|
| <span data-ttu-id="9c03c-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="9c03c-115">msdyn_warehouses</span></span> | <span data-ttu-id="9c03c-116">Lagersteder</span><span class="sxs-lookup"><span data-stu-id="9c03c-116">Warehouses</span></span>                             |

## <a name="entity-flow"></a><span data-ttu-id="9c03c-117">Enhedsflow</span><span class="sxs-lookup"><span data-stu-id="9c03c-117">Entity flow</span></span>
<span data-ttu-id="9c03c-118">Lagersteder, der oprettes og vedligeholdes i Supply Chain Management, kan synkroniseres til Field Service via et Common Data Service-dataintegrationsprojekt (CDS).</span><span class="sxs-lookup"><span data-stu-id="9c03c-118">Warehouses that are created and maintained in Supply Chain Management can be synchronized to Field Service via a Common Data Service (CDS) Data integration project.</span></span> <span data-ttu-id="9c03c-119">De lagersteder, du vil synkronisere til Field Service, kan styres med Avanceret forespørgsel og filtrering i projektet.</span><span class="sxs-lookup"><span data-stu-id="9c03c-119">The warehouses that you want to synchronize to Field Service can be controlled with the Advanced query and filtering on the project.</span></span> <span data-ttu-id="9c03c-120">Lagersteder, der synkroniseres fra Supply Chain Management, oprettes i Field Service med feltet **Vedligeholdes eksternt** indstillet til **Ja**, og posten skrivebeskyttes.</span><span class="sxs-lookup"><span data-stu-id="9c03c-120">Warehouses that synchronize from Supply Chain Management are created in Field Service with the **Is maintained externally** field set to **Yes** and the record is read only.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="9c03c-121">CRM-løsning til Field Service</span><span class="sxs-lookup"><span data-stu-id="9c03c-121">Field Service CRM solution</span></span>
<span data-ttu-id="9c03c-122">For at understøtte integrationen mellem Field Service og Finance and Operations, kræves yderligere funktioner fra CRM-løsningen i Field Service.</span><span class="sxs-lookup"><span data-stu-id="9c03c-122">To support the integration between Field Service and Finance and Operations, additional functionality from the Field Service CRM solution is required.</span></span> <span data-ttu-id="9c03c-123">I løsningen er feltet **Vedligeholdes eksternt** blevet føjet til enheden **Lagersted (msdyn_warehouses)**.</span><span class="sxs-lookup"><span data-stu-id="9c03c-123">In the solution, the **Is Maintained Externally** field has been added to the **Warehouse (msdyn_warehouses)** entity.</span></span> <span data-ttu-id="9c03c-124">Dette felt bruges til at identificere, om lagerstedet håndteres fra Supply Chain Management, eller om det kun findes i Field Service.</span><span class="sxs-lookup"><span data-stu-id="9c03c-124">This field helps to identify if the warehouse is handled from Supply Chain Management or if it only exists in Field Service.</span></span> <span data-ttu-id="9c03c-125">Indstillingerne for dette felt omfatter:</span><span class="sxs-lookup"><span data-stu-id="9c03c-125">The settings for this field include:</span></span>
- <span data-ttu-id="9c03c-126">**Ja** – Lagerstedet stammer fra Supply Chain Management, og det kan ikke redigeres i Sales.</span><span class="sxs-lookup"><span data-stu-id="9c03c-126">**Yes** – The warehouse originated from Supply Chain Management and won't be editable in Sales.</span></span>
- <span data-ttu-id="9c03c-127">**Nej** – Lagerstedet er angivet direkte i Field Service og vedligeholdes her.</span><span class="sxs-lookup"><span data-stu-id="9c03c-127">**No** – The warehouse was entered directly in Field Service and is maintained here.</span></span>

<span data-ttu-id="9c03c-128">Feltet **Vedligeholdes eksternt** hjælper med at styre synkroniseringen af lagerniveauer, reguleringer, overførsler og brug i arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="9c03c-128">The **Is Externally Maintained** field helps control the synchronization of inventory levels, adjustments, transfers, and usage on work orders.</span></span> <span data-ttu-id="9c03c-129">Kun lagersteder, hvor **Vedligeholdes eksternt** er indstillet til **Ja**, kan bruges til at synkronisere direkte til det samme lagersted i andet system.</span><span class="sxs-lookup"><span data-stu-id="9c03c-129">Only warehouses with **Is Externally Maintained** set to **Yes** can be used to synchronize directly to the same warehouse in the other system.</span></span> 

> [!NOTE]
> <span data-ttu-id="9c03c-130">Det er muligt at oprette flere lagersteder i Field Service (med **Vedligeholdes eksternt** = Nej) og derefter knytte dem til et enkelt lagersted i Finance and Operations, med funktionen Avanceret forespørgsel og filtrering.</span><span class="sxs-lookup"><span data-stu-id="9c03c-130">It is possible to create multiple warehouses in Field Service (with **Is Externally Maintained** = No) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="9c03c-131">Dette bruges i situationer, hvor Field Service skal mestre det detaljerede lagerniveau og blot sende opdateringer til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9c03c-131">This is used in situations where you want Field Service to master the detailed inventory level and just send updates to Finance and Operations.</span></span> <span data-ttu-id="9c03c-132">I dette tilfælde modtager Field Service ikke lagerniveauopdateringer fra Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9c03c-132">In this case, Field Service will not receive inventory-level updates from Finance and Operations.</span></span> <span data-ttu-id="9c03c-133">Du kan se flere oplysninger i [Synkroniser lagerreguleringer fra Field Service til Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) og [Synkronisere arbejdsordrer i Field Service med salgsordrer, der er knyttet til projektet i Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="9c03c-133">For additional information, see [Synchronize inventory adjustments from Field Service to Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="9c03c-134">Forudsætninger og tilknytningsopsætning</span><span class="sxs-lookup"><span data-stu-id="9c03c-134">Prerequisites and mapping setup</span></span>
### <a name="data-integration-project"></a><span data-ttu-id="9c03c-135">Dataintegrationsprojekt</span><span class="sxs-lookup"><span data-stu-id="9c03c-135">Data Integration project</span></span>
<span data-ttu-id="9c03c-136">Inden du synkroniserer lagerstederne, skal du sørge for at opdatere Avanceret forespørgsel og filtrering i projektet, så kun de lagersteder, du vil overføre fra Supply Chain Management til Field Service, medtages.</span><span class="sxs-lookup"><span data-stu-id="9c03c-136">Before synchronizing the warehouses, make sure to update the Advanced query and filtering on the project to only include the warehouses that you want to bring from Supply Chain Management to Field Service.</span></span> <span data-ttu-id="9c03c-137">Bemærk, at du skal bruge lagerstedet i Field Service og anvende det på arbejdsordrer, reguleringer og overførsler.</span><span class="sxs-lookup"><span data-stu-id="9c03c-137">Note that you will need the warehouse in Field Service to apply it on work orders, adjustments, and transfers.</span></span>  

<span data-ttu-id="9c03c-138">Gør følgende for at sørge for, at der findes en **Integrationsnøgle** for **msdyn_warehouses**:</span><span class="sxs-lookup"><span data-stu-id="9c03c-138">To ensure that the **Integration key** exists for **msdyn_warehouses**:</span></span>
1. <span data-ttu-id="9c03c-139">Gå til Dataintegration.</span><span class="sxs-lookup"><span data-stu-id="9c03c-139">Go to Data Integration.</span></span>
2. <span data-ttu-id="9c03c-140">Vælg fanen **Forbindelsessæt**.</span><span class="sxs-lookup"><span data-stu-id="9c03c-140">Select the **Connection Set** tab.</span></span>
3. <span data-ttu-id="9c03c-141">Vælg det forbindelsessæt, der bruges til synkronisering af arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="9c03c-141">Select the connection set used for work order synchronization.</span></span>
4. <span data-ttu-id="9c03c-142">Vælg fanen **Integrationsnøgle**.</span><span class="sxs-lookup"><span data-stu-id="9c03c-142">Select the **Integration key** tab.</span></span>
5. <span data-ttu-id="9c03c-143">Find msdyn_warehouses, og kontroller, at nøglen **msdyn_name (navn)** er tilføjet.</span><span class="sxs-lookup"><span data-stu-id="9c03c-143">Find msdyn_warehouses and confirm that the key **msdyn_name (name)** is added.</span></span> <span data-ttu-id="9c03c-144">Hvis den ikke vises, skal du tilføje den ved at klikke på **Tilføj nøgle** og derefter klikke på **Gem** øverst på siden.</span><span class="sxs-lookup"><span data-stu-id="9c03c-144">If it is not shown, add it by clicking **Add key** and then click **Save** at the top of the page.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="9c03c-145">Skabelontilknytning i dataintegration</span><span class="sxs-lookup"><span data-stu-id="9c03c-145">Template mapping in Data integration</span></span>

<span data-ttu-id="9c03c-146">Følgende illustration viser skabelontilknytningen i Dataintegration.</span><span class="sxs-lookup"><span data-stu-id="9c03c-146">The following illustration shows the template mapping in Data integration.</span></span>

### <a name="warehouses-supply-chain-management-to-field-service-warehouse"></a><span data-ttu-id="9c03c-147">Lagersteder (Supply Chain Management til Field Service): Lagersted</span><span class="sxs-lookup"><span data-stu-id="9c03c-147">Warehouses (Supply Chain Management to Field Service): Warehouse</span></span>

<span data-ttu-id="9c03c-148">[![Skabelontilknytning i dataintegration](./media/Warehouse1.png)](./media/Warehouse1.png)</span><span class="sxs-lookup"><span data-stu-id="9c03c-148">[![Template mapping in Data integration](./media/Warehouse1.png)](./media/Warehouse1.png)</span></span>
