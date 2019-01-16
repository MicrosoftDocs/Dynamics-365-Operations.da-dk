---
title: Synkronisere lagerniveauoplysninger fra Finance and Operations til Field Service
description: Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere lagerniveauoplysninger fra Microsoft Dynamics 365 for Finance and Operations med Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
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
ms.openlocfilehash: 3ccc4d406fa4f9800dcdf8697a91892408783196
ms.contentlocale: da-dk
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a><span data-ttu-id="e9bcf-103">Synkronisere lagerniveauoplysninger fra Finance and Operations til Field Service</span><span class="sxs-lookup"><span data-stu-id="e9bcf-103">Synchronize inventory level information from Finance and Operations to Field Service</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e9bcf-104">Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere lagerniveauoplysninger fra Microsoft Dynamics 365 for Finance and Operations med Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="e9bcf-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory level information from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="e9bcf-105">[![Synkronisering af forretningsprocesser mellem Finance and Operations og Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span><span class="sxs-lookup"><span data-stu-id="e9bcf-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="e9bcf-106">Skabeloner og opgaver</span><span class="sxs-lookup"><span data-stu-id="e9bcf-106">Templates and tasks</span></span>
<span data-ttu-id="e9bcf-107">Følgende skabelon og underliggende opgaver bruges til at køre synkronisering af disponible lagerbeholdningsniveauer fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="e9bcf-107">The following template and underlying tasks are used to run synchronization of inventory on-hand levels from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="e9bcf-108">**Navnet på skabelonen i dataintegration:**</span><span class="sxs-lookup"><span data-stu-id="e9bcf-108">**Name of the template in Data integration:**</span></span>
- <span data-ttu-id="e9bcf-109">Produktlager (Finance and Operations til Field Service)</span><span class="sxs-lookup"><span data-stu-id="e9bcf-109">Product Inventory (Finance and Operations to Field Service)</span></span>
  
<span data-ttu-id="e9bcf-110">**Navne på opgaverne i dataintegrationsprojektet:**</span><span class="sxs-lookup"><span data-stu-id="e9bcf-110">**Names of the tasks in the Data integration project:**</span></span>
- <span data-ttu-id="e9bcf-111">Produktlager</span><span class="sxs-lookup"><span data-stu-id="e9bcf-111">Product inventory</span></span>

<span data-ttu-id="e9bcf-112">Følgende synkroniseringsopgaver kræves, før lagerniveauer kan synkroniseres:</span><span class="sxs-lookup"><span data-stu-id="e9bcf-112">The following synchronization tasks are required before synchronization of inventory levels can occur:</span></span>
- <span data-ttu-id="e9bcf-113">Lagersteder (Finance and Operations til Field Service)</span><span class="sxs-lookup"><span data-stu-id="e9bcf-113">Warehouses (Finance and Operations to Field Service)</span></span> 
- <span data-ttu-id="e9bcf-114">Field Service-produkter med lagerenhed (Finance and Operations til Sales)</span><span class="sxs-lookup"><span data-stu-id="e9bcf-114">Field Service Products with Inventory unit (Finance and Operations to Sales)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="e9bcf-115">Enhedssæt</span><span class="sxs-lookup"><span data-stu-id="e9bcf-115">Entity set</span></span>

| <span data-ttu-id="e9bcf-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="e9bcf-116">Field Service</span></span>                      | <span data-ttu-id="e9bcf-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e9bcf-117">Finance and Operations</span></span>                 |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="e9bcf-118">msdynce_externalproductinventories</span><span class="sxs-lookup"><span data-stu-id="e9bcf-118">msdynce_externalproductinventories</span></span> | <span data-ttu-id="e9bcf-119">CDS Disponibelt lager efter lagersted</span><span class="sxs-lookup"><span data-stu-id="e9bcf-119">CDS inventory on-hand by warehouse</span></span>     |

## <a name="entity-flow"></a><span data-ttu-id="e9bcf-120">Enhedsflow</span><span class="sxs-lookup"><span data-stu-id="e9bcf-120">Entity flow</span></span>
<span data-ttu-id="e9bcf-121">Lagerniveauoplysninger fra Finance and Operations sendes til Field Service for udvalgte produkter.</span><span class="sxs-lookup"><span data-stu-id="e9bcf-121">Inventory level information from Finance and Operation is send to Field Service for selected products.</span></span> <span data-ttu-id="e9bcf-122">Lagerniveauoplysningerne omfatter:</span><span class="sxs-lookup"><span data-stu-id="e9bcf-122">The inventory level information include:</span></span> 
- <span data-ttu-id="e9bcf-123">Disponibelt antal (aktuelt registreret fysisk antal, der findes på lagerstedet)</span><span class="sxs-lookup"><span data-stu-id="e9bcf-123">On hand quantity (current recorded physically quantity located in the warehouse)</span></span>
- <span data-ttu-id="e9bcf-124">Antal i bestilling (samlet registrerede antal i ordre - dvs. salgsordrer)</span><span class="sxs-lookup"><span data-stu-id="e9bcf-124">On order quantity (total recorded quantity on order - i.e. sales orders)</span></span>
- <span data-ttu-id="e9bcf-125">Bestilt antal (samlet registrerede bestilte antal - dvs. indkøbsordrer)</span><span class="sxs-lookup"><span data-stu-id="e9bcf-125">Ordered quantity (total recorded ordered quantity - i.e. purchase orders)</span></span>

<span data-ttu-id="e9bcf-126">Disse oplysninger hentes pr. frigivet produkt for hvert lagersted og synkroniseres efter ændringssporing, når lagerniveauet ændres.</span><span class="sxs-lookup"><span data-stu-id="e9bcf-126">This information is captured per released product for each warehouse and synchronized based on change tracking, when the inventory level changes.</span></span>

<span data-ttu-id="e9bcf-127">I Field Service opretter integrationsløsningen lagerkladder for deltaet for at få niveauerne i Field Service til at svare til niveauerne i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e9bcf-127">In Field Service the integration solution create inventory journals for the delta, to get the levels in Field Service to match the levels in Finance and Operations.</span></span>

<span data-ttu-id="e9bcf-128">Finance and Operations fungerer som master for lagerniveauer.</span><span class="sxs-lookup"><span data-stu-id="e9bcf-128">Finance and Operations will act as the master for inventory levels.</span></span> <span data-ttu-id="e9bcf-129">Så det er vigtigt at konfigurere integration for arbejdsordrer, overførsler og reguleringer fra Field Service til Finance and Operations, hvis disse funktioner bruges i Field Service, sammen med synkronisering af lagerniveauer fra Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e9bcf-129">So it is important to setup integration for workorders, transfers and adjustments from Field Service to Finance and Operations if the this functionality is used in Field Service, together with synchronization of inventory levels from Finance and Operations.</span></span>

<span data-ttu-id="e9bcf-130">De produkter og lagersteder, hvor lagerniveauer administreres fra Finance and Operations, kan kontrolleres med Avanceret forespørgsel og filtrering (Power-forespørgsel).</span><span class="sxs-lookup"><span data-stu-id="e9bcf-130">The products and warehouses where inventory levels are mastered from Finance and Operations can be controlled with the Advanced Query and Filtering (Power Query).</span></span>

<span data-ttu-id="e9bcf-131">Bemærk: Det er muligt at oprette flere lagersteder i Field Service (med Vedligeholdes eksternt = Nej) og derefter knytte dem til et enkelt lagersted i Finance and Operations, med funktionen Avanceret forespørgsel og filtrering.</span><span class="sxs-lookup"><span data-stu-id="e9bcf-131">Note: It is possible to create multiple warehouses in Field Services (with Is Externally Maintained = No) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="e9bcf-132">Dette bruges i situationer, hvor Field Service skal mestre det detaljerede lagerniveau og blot sende opdateringer til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e9bcf-132">This is used in situations where you want Field service to master the detailed inventory level and just send updates to Finance and Operations.</span></span> <span data-ttu-id="e9bcf-133">I dette tilfælde modtager Field Service ikke lagerniveauopdateringer fra Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e9bcf-133">In this case Field service will not receive inventory level updates from Finance and Operations.</span></span> <span data-ttu-id="e9bcf-134">Du kan se flere oplysninger i Synkroniser lagerreguleringer fra Field Service til Finance and Operations og Synkronisere arbejdsordrer i Field Service med salgsordrer, der er knyttet til projektet i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e9bcf-134">See additional information in Synchronize inventory adjustments from Field Service to Finance and Operations and Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="e9bcf-135">CRM-løsning til Field Service</span><span class="sxs-lookup"><span data-stu-id="e9bcf-135">Field Service CRM solution</span></span>
<span data-ttu-id="e9bcf-136">Den eksterne produktlagerenhed er en ny enhed, der kun bruges til backend i integrationen.</span><span class="sxs-lookup"><span data-stu-id="e9bcf-136">The External Product Inventory entity is a new entity that’s only used for backend in the integration.</span></span> <span data-ttu-id="e9bcf-137">Den modtager lagerniveauværdierne fra Finance and Operations i integrationen og ændrer derefter disse værdier til manuelle lagerkladder, der derefter ændrer lagerprodukterne på lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="e9bcf-137">It receives the inventory level values from Finance and Operations in the integration and then transforms those values to Manuel Inventory journals, that then changes the Inventory Products on the Warehouse.</span></span> 

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="e9bcf-138">Forudsætninger og tilknytningsopsætning</span><span class="sxs-lookup"><span data-stu-id="e9bcf-138">Prerequisites and mapping setup</span></span>

### <a name="in-the-data-integration-project"></a><span data-ttu-id="e9bcf-139">I dataintegrationsprojektet</span><span class="sxs-lookup"><span data-stu-id="e9bcf-139">In the Data Integration project</span></span>
<span data-ttu-id="e9bcf-140">Anvend filtre i Avanceret forespørgsel og filtrering til at styre, at kun ønskede produkter og lagersteder sender lagerniveauoplysninger fra Finance and Operations til Field Service.</span><span class="sxs-lookup"><span data-stu-id="e9bcf-140">Apply filters with the Advanced  Query and Filtering to control that only desired products and warehouses send inventory level information from Finance and Operations to Field Service.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="e9bcf-141">Skabelontilknytning i dataintegration</span><span class="sxs-lookup"><span data-stu-id="e9bcf-141">Template mapping in Data integration</span></span>

### <a name="product-inventory-finance-and-operations-to-field-service-product-inventory"></a><span data-ttu-id="e9bcf-142">Produktlager (Finance and Operations til Field Service): Produktlager</span><span class="sxs-lookup"><span data-stu-id="e9bcf-142">Product Inventory (Finance and Operations to Field Service): Product inventory</span></span>

<span data-ttu-id="e9bcf-143">[![Skabelontilknytning i dataintegration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span><span class="sxs-lookup"><span data-stu-id="e9bcf-143">[![Template mapping in Data integration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span></span>

