---
title: Synkronisere oplysninger på lagerniveau fra Supply Chain Management til Field Service
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere oplysninger på lagerniveau fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.
author: ChristianRytt
manager: tfehr
ms.date: 05/07/2019
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
ms.openlocfilehash: 1228339c12d26f7b91875d15f0daa8da2869cba0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215901"
---
# <a name="synchronize-inventory-level-information-from-supply-chain-management-to-field-service"></a><span data-ttu-id="c3c97-103">Synkronisere oplysninger på lagerniveau fra Supply Chain Management til Field Service</span><span class="sxs-lookup"><span data-stu-id="c3c97-103">Synchronize inventory level information from Supply Chain Management to Field Service</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c3c97-104">I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere oplysninger på lagerniveau fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="c3c97-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory-level information from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="c3c97-105">[![Synkronisering af forretningsprocesser mellem Supply Chain Management og Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span><span class="sxs-lookup"><span data-stu-id="c3c97-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="c3c97-106">Skabeloner og opgaver</span><span class="sxs-lookup"><span data-stu-id="c3c97-106">Templates and tasks</span></span>
<span data-ttu-id="c3c97-107">Følgende skabelon og underliggende opgaver bruges til at synkronisere niveauer af disponibel lagerbeholdning fra Supply Chain Management til Field Service.</span><span class="sxs-lookup"><span data-stu-id="c3c97-107">The following template and underlying tasks are used to synchronize inventory on-hand levels from Supply Chain Management to Field Service.</span></span>

<span data-ttu-id="c3c97-108">**Skabelon i dataintegration**</span><span class="sxs-lookup"><span data-stu-id="c3c97-108">**Template in Data integration**</span></span>
- <span data-ttu-id="c3c97-109">Produktlager (Supply Chain Management til Field Service)</span><span class="sxs-lookup"><span data-stu-id="c3c97-109">Product Inventory (Supply Chain Management to Field Service)</span></span>
  
<span data-ttu-id="c3c97-110">**Opgave i dataintegrationsprojekt**</span><span class="sxs-lookup"><span data-stu-id="c3c97-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="c3c97-111">Produktlager</span><span class="sxs-lookup"><span data-stu-id="c3c97-111">Product inventory</span></span>

<span data-ttu-id="c3c97-112">Følgende synkroniseringsopgaver kræves, før lagerniveauer kan synkroniseres:</span><span class="sxs-lookup"><span data-stu-id="c3c97-112">The following synchronization tasks are required before synchronization of inventory levels can occur:</span></span>
- <span data-ttu-id="c3c97-113">Lagersteder (Supply Chain Management til Field Service)</span><span class="sxs-lookup"><span data-stu-id="c3c97-113">Warehouses (Supply Chain Management to Field Service)</span></span> 
- <span data-ttu-id="c3c97-114">Field Service-produkter med lagerenhed (Supply Chain Management til Sales)</span><span class="sxs-lookup"><span data-stu-id="c3c97-114">Field Service products with Inventory unit (Supply Chain Management to Sales)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="c3c97-115">Enhedssæt</span><span class="sxs-lookup"><span data-stu-id="c3c97-115">Entity set</span></span>

| <span data-ttu-id="c3c97-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="c3c97-116">Field Service</span></span>                      | <span data-ttu-id="c3c97-117">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="c3c97-117">Supply Chain Management</span></span>                |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="c3c97-118">msdynce_externalproductinventories</span><span class="sxs-lookup"><span data-stu-id="c3c97-118">msdynce_externalproductinventories</span></span> | <span data-ttu-id="c3c97-119">CDS Disponibelt lager efter lagersted</span><span class="sxs-lookup"><span data-stu-id="c3c97-119">CDS inventory on-hand by warehouse</span></span>     |

## <a name="entity-flow"></a><span data-ttu-id="c3c97-120">Enhedsflow</span><span class="sxs-lookup"><span data-stu-id="c3c97-120">Entity flow</span></span>
<span data-ttu-id="c3c97-121">Lagerniveauoplysninger fra Finance and Operations sendes til Field Service for udvalgte produkter.</span><span class="sxs-lookup"><span data-stu-id="c3c97-121">Inventory-level information from Finance and Operation is sent to Field Service for selected products.</span></span> <span data-ttu-id="c3c97-122">Lagerniveauoplysningerne omfatter:</span><span class="sxs-lookup"><span data-stu-id="c3c97-122">The inventory-level information includes:</span></span> 
- <span data-ttu-id="c3c97-123">Disponibelt antal (aktuelt registreret fysisk antal, der findes på lagerstedet)</span><span class="sxs-lookup"><span data-stu-id="c3c97-123">On hand quantity (current recorded physical quantity located in the warehouse)</span></span>
- <span data-ttu-id="c3c97-124">Antal i bestilling (samlet registrerede antal i ordre, f.eks. salgsordrer)</span><span class="sxs-lookup"><span data-stu-id="c3c97-124">On order quantity (total recorded quantity on order, such as sales orders)</span></span>
- <span data-ttu-id="c3c97-125">Bestilt antal (samlet registrerede bestilte antal, f.eks. indkøbsordrer)</span><span class="sxs-lookup"><span data-stu-id="c3c97-125">Ordered quantity (total recorded ordered quantity, such as purchase orders)</span></span>

<span data-ttu-id="c3c97-126">Disse oplysninger hentes pr. frigivet produkt for hvert lagersted og synkroniseres efter ændringssporing, når lagerniveauet ændres.</span><span class="sxs-lookup"><span data-stu-id="c3c97-126">This information is captured per released product for each warehouse and synchronized based on change tracking, when the inventory level changes.</span></span>

<span data-ttu-id="c3c97-127">I Field Service opretter integrationsløsningen lagerkladder for deltaet, så niveauerne i Field Service svarer til niveauerne i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c3c97-127">In Field Service, the integration solution creates inventory journals for the delta, so that the levels in Field Service match the levels in Supply Chain Management.</span></span>

<span data-ttu-id="c3c97-128">Supply Chain Management fungerer som master for lagerniveauer.</span><span class="sxs-lookup"><span data-stu-id="c3c97-128">Supply Chain Management will act as the master for inventory levels.</span></span> <span data-ttu-id="c3c97-129">Det er derfor vigtigt at konfigurere integration for arbejdsordrer, overførsler og reguleringer fra Field Service til Supply Chain Management, hvis disse funktioner bruges i Field Service, sammen med synkronisering af lagerniveauer fra Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c3c97-129">Therefore it is important to set up integration for work orders, transfers, and adjustments from Field Service to Supply Chain Management if this functionality is used in Field Service, together with synchronization of inventory levels from Supply Chain Management.</span></span>

<span data-ttu-id="c3c97-130">De produkter og lagersteder, hvor lagerniveauer administreres fra Supply Chain Management, kan kontrolleres med Avanceret forespørgsel og filtrering (Power Query).</span><span class="sxs-lookup"><span data-stu-id="c3c97-130">The products and warehouses where inventory levels are mastered from Supply Chain Management can be controlled with the Advanced Query and Filtering (Power Query).</span></span>

> [!NOTE]
> <span data-ttu-id="c3c97-131">Det er muligt at oprette flere lagersteder i Field Service (med **Vedligeholdes eksternt = Nej**) og derefter knytte dem til et enkelt lagersted i Supply Chain Management, med funktionen Avanceret forespørgsel og filtrering.</span><span class="sxs-lookup"><span data-stu-id="c3c97-131">It is possible to create multiple warehouses in Field Services (with **Is Externally Maintained = No**) and then map them to a single warehouse in Supply Chain Management, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="c3c97-132">Dette bruges i situationer, hvor Field Service skal mestre det detaljerede lagerniveau og kun sende opdateringer til Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c3c97-132">This is used in situations where you want Field Service to master the detailed inventory level and only send updates to Supply Chain Management.</span></span> <span data-ttu-id="c3c97-133">I dette tilfælde modtager Field Service ikke lagerniveauopdateringer fra Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c3c97-133">In this case, Field Service will not receive inventory-level updates from Supply Chain Management.</span></span> <span data-ttu-id="c3c97-134">Du kan se flere oplysninger i [Synkroniser lagerreguleringer fra Field Service til Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) og [Synkronisere arbejdsordrer i Field Service med salgsordrer, der er knyttet til projektet i Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="c3c97-134">For additional information, see [Synchronize inventory adjustments from Field Service to Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="c3c97-135">CRM-løsning til Field Service</span><span class="sxs-lookup"><span data-stu-id="c3c97-135">Field Service CRM solution</span></span>
<span data-ttu-id="c3c97-136">Enheden **Eksternt produktlager** bruges kun til backend i integrationen.</span><span class="sxs-lookup"><span data-stu-id="c3c97-136">The **External product inventory** entity is only used for back end in to the integration.</span></span> <span data-ttu-id="c3c97-137">Denne enhed modtager lagerniveauværdierne fra Supply Chain Management i integrationen og ændrer derefter disse værdier til manuelle lagerkladder, der derefter ændrer lagerprodukterne på lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="c3c97-137">This entity receives the inventory level values from Supply Chain Management in the integration and then transforms those values to Manual inventory journals, which then changes the Inventory products in the Warehouse.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="c3c97-138">Forudsætninger og tilknytningsopsætning</span><span class="sxs-lookup"><span data-stu-id="c3c97-138">Prerequisites and mapping setup</span></span>

### <a name="data-integration"></a><span data-ttu-id="c3c97-139">Dataintegration</span><span class="sxs-lookup"><span data-stu-id="c3c97-139">Data integration</span></span>
<span data-ttu-id="c3c97-140">For at projektet kan fungere skal du sørge for, at integrationsnøglen er opdateret til msdynce_externalproductinventories.</span><span class="sxs-lookup"><span data-stu-id="c3c97-140">For the project to work, you need to ensure that the Integration key is updated for msdynce_externalproductinventories.</span></span>
1.  <span data-ttu-id="c3c97-141">Gå til **Dataintegration > Forbindelsessæt**.</span><span class="sxs-lookup"><span data-stu-id="c3c97-141">Go to **Data integration > Connection sets**.</span></span>
2.  <span data-ttu-id="c3c97-142">Vælg det anvendte forbindelsessæt.</span><span class="sxs-lookup"><span data-stu-id="c3c97-142">Select the used Connection set.</span></span>
3.  <span data-ttu-id="c3c97-143">Kontroller, at følgende nøgler er føjet til msdynce_externalproductinventories, under fanen **Integrationsnøgle**:</span><span class="sxs-lookup"><span data-stu-id="c3c97-143">On the **Integration key** tab, ensure that the following keys are added to msdynce_externalproductinventories:</span></span>
      - <span data-ttu-id="c3c97-144">msdynce_productnumber (produktnummer)</span><span class="sxs-lookup"><span data-stu-id="c3c97-144">msdynce_productnumber (Product Number)</span></span>
      - <span data-ttu-id="c3c97-145">msdynce_warehouseid (lagersteds-ID)</span><span class="sxs-lookup"><span data-stu-id="c3c97-145">msdynce_warehouseid (Warehouse ID)</span></span>
      
### <a name="data-integration-project"></a><span data-ttu-id="c3c97-146">Dataintegrationsprojekt</span><span class="sxs-lookup"><span data-stu-id="c3c97-146">Data integration project</span></span>
<span data-ttu-id="c3c97-147">Du kan anvende filtre i Avanceret forespørgsel og filtrering, så kun bestemte produkter og lagersteder sender lagerniveauoplysninger fra Supply Chain Management til Field Service.</span><span class="sxs-lookup"><span data-stu-id="c3c97-147">You can apply filters with Advanced Query and Filtering so that only certain products and warehouses send inventory-level information from Supply Chain Management to Field Service.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="c3c97-148">Skabelontilknytning i dataintegration</span><span class="sxs-lookup"><span data-stu-id="c3c97-148">Template mapping in Data integration</span></span>

### <a name="product-inventory-supply-chain-management-to-field-service-product-inventory"></a><span data-ttu-id="c3c97-149">Produktlager (Supply Chain Management til Field Service): Produktlager</span><span class="sxs-lookup"><span data-stu-id="c3c97-149">Product inventory (Supply Chain Management to Field Service): Product inventory</span></span>

<span data-ttu-id="c3c97-150">[![Skabelontilknytning i dataintegration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span><span class="sxs-lookup"><span data-stu-id="c3c97-150">[![Template mapping in Data integration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span></span>
