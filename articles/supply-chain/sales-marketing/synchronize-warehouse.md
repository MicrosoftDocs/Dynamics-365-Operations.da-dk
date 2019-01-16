---
title: Synkronisere lagersteder fra Finance and Operations til Field Service
description: Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere lagersteder fra Microsoft Dynamics 365 for Finance and Operations med Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 10/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: eb8ba6051777e27bd44504a8160118e8096b1435
ms.contentlocale: da-dk
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-warehouses-from-finance-and-operations-to-field-service"></a><span data-ttu-id="9a7c5-103">Synkronisere lagersteder fra Finance and Operations til Field Service</span><span class="sxs-lookup"><span data-stu-id="9a7c5-103">Synchronize warehouses from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="9a7c5-104">Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere lagersteder fra Microsoft Dynamics 365 for Finance and Operations med Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="9a7c5-104">This topic discusses the templates and underlying tasks that are used to synchronize warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="9a7c5-105">[![Synkronisering af forretningsprocesser mellem Finance and Operations og Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span><span class="sxs-lookup"><span data-stu-id="9a7c5-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="9a7c5-106">Skabeloner og opgaver</span><span class="sxs-lookup"><span data-stu-id="9a7c5-106">Templates and tasks</span></span>
<span data-ttu-id="9a7c5-107">Følgende skabelon og underliggende opgaver bruges til at køre synkronisering af lagersteder fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="9a7c5-107">The following template and underlying tasks are used to run synchronization of warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="9a7c5-108">**Navnet på skabelonen i dataintegration:**</span><span class="sxs-lookup"><span data-stu-id="9a7c5-108">**Name of the template in Data integration:**</span></span>
- <span data-ttu-id="9a7c5-109">Lagersteder (Finance and Operations til Field Service)</span><span class="sxs-lookup"><span data-stu-id="9a7c5-109">Warehouses (Finance and Operations to Field Service)</span></span>

<span data-ttu-id="9a7c5-110">**Navne på opgaverne i dataintegrationsprojektet:**</span><span class="sxs-lookup"><span data-stu-id="9a7c5-110">**Names of the tasks in the Data integration project:**</span></span>
- <span data-ttu-id="9a7c5-111">Lagersted</span><span class="sxs-lookup"><span data-stu-id="9a7c5-111">Warehouse</span></span>

## <a name="entity-set"></a><span data-ttu-id="9a7c5-112">Enhedssæt</span><span class="sxs-lookup"><span data-stu-id="9a7c5-112">Entity set</span></span>
| <span data-ttu-id="9a7c5-113">Field Service</span><span class="sxs-lookup"><span data-stu-id="9a7c5-113">Field Service</span></span>    | <span data-ttu-id="9a7c5-114">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9a7c5-114">Finance and Operations</span></span>                 |
|------------------|----------------------------------------|
| <span data-ttu-id="9a7c5-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="9a7c5-115">msdyn_warehouses</span></span> | <span data-ttu-id="9a7c5-116">Lagersteder</span><span class="sxs-lookup"><span data-stu-id="9a7c5-116">Warehouses</span></span>                             |

## <a name="entity-flow"></a><span data-ttu-id="9a7c5-117">Enhedsflow</span><span class="sxs-lookup"><span data-stu-id="9a7c5-117">Entity flow</span></span>
<span data-ttu-id="9a7c5-118">Lagersteder, der er oprettet og vedligeholdes i Finance and Operations, kan synkroniseres til Field Service via et CDS-dataintegrationsprojekt (CDS – Common Data Service).</span><span class="sxs-lookup"><span data-stu-id="9a7c5-118">Warehouses that are created and maintained in Finance and Operations can be synchronized to Field Service via a Common Data Service (CDS) Data integration project.</span></span> <span data-ttu-id="9a7c5-119">De ønskede lagersteder, der skal synkroniseres til Field Service, kan styres med Avanceret forespørgsel og filtrering i projektet.</span><span class="sxs-lookup"><span data-stu-id="9a7c5-119">The desired warehouses that synchronize to Field Service can be controlled with the Advanced query and filtering on the project.</span></span> <span data-ttu-id="9a7c5-120">Lagersteder, der synkroniseres fra Finance and Operations, oprettes i Field Service med feltet Vedligeholdes eksternt indstillet til Ja, og posten skrivebeskyttes.</span><span class="sxs-lookup"><span data-stu-id="9a7c5-120">Warehouses that synchronize from Finance and Operations are created in Field Service with the field Is maintained externally set to Yes and the record is made read only.</span></span>
<span data-ttu-id="9a7c5-121">CRM-løsning til Field Service For at understøtte integrationen mellem Field Service og Finance and Operations kræves yderligere funktioner fra CRM-løsningen til Field Service.</span><span class="sxs-lookup"><span data-stu-id="9a7c5-121">Field Service CRM solution To support the integration between Field Service and Finance and Operations, additional functionality from the Field Service CRM solution is required.</span></span> <span data-ttu-id="9a7c5-122">Løsningen indeholder følgende ændringer.</span><span class="sxs-lookup"><span data-stu-id="9a7c5-122">The solution includes the following changes.</span></span>
<span data-ttu-id="9a7c5-123">Feltet **Vedligeholdes eksternt** er blevet føjet til enheden **Lagersted (msdyn_warehouses)**.</span><span class="sxs-lookup"><span data-stu-id="9a7c5-123">The field **Is Maintained Externally** has been added to the **Warehouse (msdyn_warehouses)** entity.</span></span> <span data-ttu-id="9a7c5-124">Dette felt bruges til at identificere, om lagerstedet håndteres fra Operations, eller om det kun findes i Field Service.</span><span class="sxs-lookup"><span data-stu-id="9a7c5-124">This field helps to identify If the Warehouse is handled from Operations or if It only exists in Field Service.</span></span>
- <span data-ttu-id="9a7c5-125">Ja – Lagerstedet stammer fra Finance and Operations og kan ikke redigeres i Sales.</span><span class="sxs-lookup"><span data-stu-id="9a7c5-125">Yes – The warehouse originated from Finance and Operations and won't be editable in Sales.</span></span>
- <span data-ttu-id="9a7c5-126">Nej – Lagerstedet er angivet direkte i Field Service og vedligeholdes her.</span><span class="sxs-lookup"><span data-stu-id="9a7c5-126">No – The warehouse was entered directly in Field Service and is maintained here.</span></span>

<span data-ttu-id="9a7c5-127">Feltet **Vedligeholdes eksternt** hjælper med at styre synkroniseringen af lagerniveauer, reguleringer, overførsler og brug i arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="9a7c5-127">The **Is Externally Maintained** field helps control the synchronization of inventory levels, adjustments, transfers and usage on work orders.</span></span> <span data-ttu-id="9a7c5-128">Kun lagersteder, hvor **Vedligeholdes eksternt** = Ja, kan bruges til at synkronisere direkte til det samme lagersted i andet system.</span><span class="sxs-lookup"><span data-stu-id="9a7c5-128">Only warehouses with **Is Externally Maintained** = Yes can be used to synchronize directly to the same warehouse in the other system.</span></span> 

<span data-ttu-id="9a7c5-129">Bemærk: Det er muligt at oprette flere lagersteder i Field Service (med **Vedligeholdes eksternt** = Nej) og derefter knytte dem til et enkelt lagersted i Finance and Operations, med funktionen Avanceret forespørgsel og filtrering.</span><span class="sxs-lookup"><span data-stu-id="9a7c5-129">Note: It is possible to create multiple warehouses in Field Services (with **Is Externally Maintained** = No) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="9a7c5-130">Dette bruges i situationer, hvor Field Service skal mestre det detaljerede lagerniveau og blot sende opdateringer til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9a7c5-130">This is used in situations where you want Field service to master the detailed inventory level and just send updates to Finance and Operations.</span></span> <span data-ttu-id="9a7c5-131">I dette tilfælde modtager Field Service ikke lagerniveauopdateringer fra Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9a7c5-131">In this case Field service will not receive inventory level updates from Finance and Operations.</span></span> <span data-ttu-id="9a7c5-132">Du kan se flere oplysninger i Synkroniser lagerreguleringer fra Field Service til Finance and Operations og Synkronisere arbejdsordrer i Field Service med salgsordrer, der er knyttet til projektet i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9a7c5-132">See additional information in Synchronize inventory adjustments from Field Service to Finance and Operations and Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="9a7c5-133">Forudsætninger og tilknytningsopsætning</span><span class="sxs-lookup"><span data-stu-id="9a7c5-133">Prerequisites and mapping setup</span></span>
### <a name="in-the-data-integration-project"></a><span data-ttu-id="9a7c5-134">I dataintegrationsprojektet</span><span class="sxs-lookup"><span data-stu-id="9a7c5-134">In the Data Integration project</span></span>
<span data-ttu-id="9a7c5-135">Inden synkroniseringen af lagerstederne skal du sørge for at opdatere Avanceret forespørgsel og filtrering i projektet, så kun de lagersteder, du vil overføre fra Finance and Operations til Field Service, medtages.</span><span class="sxs-lookup"><span data-stu-id="9a7c5-135">Before synchronization of the warehouses make sure to update the Advanced query and filtering on the project to only include the warehouses that you want to bring from Finance and Operations to Field Service.</span></span> <span data-ttu-id="9a7c5-136">Bemærk, at du skal bruge lagerstedet i Field Service og anvende det på arbejdsordrer, reguleringer og overførsler.</span><span class="sxs-lookup"><span data-stu-id="9a7c5-136">Note that you will need the warehouse in Field Service to apply it on work orders, adjustments and transfers.</span></span>  

<span data-ttu-id="9a7c5-137">Sørg for, at der findes en **Integrationsnøgle** for **msdyn_warehouses**</span><span class="sxs-lookup"><span data-stu-id="9a7c5-137">Ensure the **Integration key** exist for **msdyn_warehouses**</span></span>
1. <span data-ttu-id="9a7c5-138">Gå til Dataintegration</span><span class="sxs-lookup"><span data-stu-id="9a7c5-138">Go to Data Integration</span></span>
2. <span data-ttu-id="9a7c5-139">Vælg fanen **Forbindelsessæt**</span><span class="sxs-lookup"><span data-stu-id="9a7c5-139">Select **Connection Set** tab</span></span>
3. <span data-ttu-id="9a7c5-140">Vælg det forbindelsessæt, der bruges til synkronisering af arbejdsordre</span><span class="sxs-lookup"><span data-stu-id="9a7c5-140">Select the Connection set used for Work order synchronization</span></span>
4. <span data-ttu-id="9a7c5-141">Vælg fanen **Integrationsnøgle**</span><span class="sxs-lookup"><span data-stu-id="9a7c5-141">Select **Integration key** tab</span></span>
5. <span data-ttu-id="9a7c5-142">Find msdyn_warehouses, og kontroller, at nøglen **msdyn_name (navn)** er tilføjet.</span><span class="sxs-lookup"><span data-stu-id="9a7c5-142">Find msdyn_warehouses and check that the key **msdyn_name (name)** is added.</span></span> <span data-ttu-id="9a7c5-143">Hvis den ikke vises, kan du tilføje den ved at klikke på **Tilføj nøgle** og klikke på **Gem** øverst på siden</span><span class="sxs-lookup"><span data-stu-id="9a7c5-143">If it is not shown, add it by click **Add key** and click **Save** in the top of the page</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="9a7c5-144">Skabelontilknytning i dataintegration</span><span class="sxs-lookup"><span data-stu-id="9a7c5-144">Template mapping in Data integration</span></span>

<span data-ttu-id="9a7c5-145">Følgende illustration viser skabelontilknytningen i Dataintegration.</span><span class="sxs-lookup"><span data-stu-id="9a7c5-145">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="warehouses-finance-and-operations-to-field-service-warehouse"></a><span data-ttu-id="9a7c5-146">Lagersteder (Finance and Operations til Field Service): Lagersted</span><span class="sxs-lookup"><span data-stu-id="9a7c5-146">Warehouses (Finance and Operations to Field Service): Warehouse</span></span>

<span data-ttu-id="9a7c5-147">[![Skabelontilknytning i dataintegration](./media/Warehouse1.png)](./media/Warehouse1.png)</span><span class="sxs-lookup"><span data-stu-id="9a7c5-147">[![Template mapping in Data integration](./media/Warehouse1.png)](./media/Warehouse1.png)</span></span>

