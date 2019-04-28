---
title: Synkronisere lagerniveauoplysninger fra Finance and Operations til Field Service
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere oplysninger på lagerniveau fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.
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
ms.openlocfilehash: 6b2bdf1ca6f6ae43cd85c8a1353ee8305052761d
ms.sourcegitcommit: a6d385db6636ef2b7fb6b24d37a2160c8d5a3c0f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/14/2019
ms.locfileid: "842550"
---
# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a><span data-ttu-id="50111-103">Synkronisere lagerniveauoplysninger fra Finance and Operations til Field Service</span><span class="sxs-lookup"><span data-stu-id="50111-103">Synchronize inventory level information from Finance and Operations to Field Service</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="50111-104">I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere oplysninger på lagerniveau fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="50111-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory-level information from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="50111-105">[![Synkronisering af forretningsprocesser mellem Finance and Operations og Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span><span class="sxs-lookup"><span data-stu-id="50111-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="50111-106">Skabeloner og opgaver</span><span class="sxs-lookup"><span data-stu-id="50111-106">Templates and tasks</span></span>
<span data-ttu-id="50111-107">Følgende skabelon og underliggende opgaver bruges til at synkronisere disponible lagerbeholdningsniveauer fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="50111-107">The following template and underlying tasks are used to synchronize inventory on-hand levels from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="50111-108">**Skabelon i dataintegration**</span><span class="sxs-lookup"><span data-stu-id="50111-108">**Template in Data integration**</span></span>
- <span data-ttu-id="50111-109">Produktlager (Fin and Ops til Field Service)</span><span class="sxs-lookup"><span data-stu-id="50111-109">Product Inventory (Fin and Ops to Field Service)</span></span>
  
<span data-ttu-id="50111-110">**Opgave i dataintegrationsprojekt**</span><span class="sxs-lookup"><span data-stu-id="50111-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="50111-111">Produktlager</span><span class="sxs-lookup"><span data-stu-id="50111-111">Product inventory</span></span>

<span data-ttu-id="50111-112">Følgende synkroniseringsopgaver kræves, før lagerniveauer kan synkroniseres:</span><span class="sxs-lookup"><span data-stu-id="50111-112">The following synchronization tasks are required before synchronization of inventory levels can occur:</span></span>
- <span data-ttu-id="50111-113">Lagersteder (Fin and Ops til Field Service)</span><span class="sxs-lookup"><span data-stu-id="50111-113">Warehouses (Fin and Ops to Field Service)</span></span> 
- <span data-ttu-id="50111-114">Field Service-produkter med lagerenhed (Fin and Ops til salg)</span><span class="sxs-lookup"><span data-stu-id="50111-114">Field Service products with Inventory unit (Fin and Ops to Sales)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="50111-115">Enhedssæt</span><span class="sxs-lookup"><span data-stu-id="50111-115">Entity set</span></span>

| <span data-ttu-id="50111-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="50111-116">Field Service</span></span>                      | <span data-ttu-id="50111-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="50111-117">Finance and Operations</span></span>                 |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="50111-118">msdynce_externalproductinventories</span><span class="sxs-lookup"><span data-stu-id="50111-118">msdynce_externalproductinventories</span></span> | <span data-ttu-id="50111-119">CDS Disponibelt lager efter lagersted</span><span class="sxs-lookup"><span data-stu-id="50111-119">CDS inventory on-hand by warehouse</span></span>     |

## <a name="entity-flow"></a><span data-ttu-id="50111-120">Enhedsflow</span><span class="sxs-lookup"><span data-stu-id="50111-120">Entity flow</span></span>
<span data-ttu-id="50111-121">Lagerniveauoplysninger fra Finance and Operations sendes til Field Service for udvalgte produkter.</span><span class="sxs-lookup"><span data-stu-id="50111-121">Inventory-level information from Finance and Operation is sent to Field Service for selected products.</span></span> <span data-ttu-id="50111-122">Lagerniveauoplysningerne omfatter:</span><span class="sxs-lookup"><span data-stu-id="50111-122">The inventory-level information includes:</span></span> 
- <span data-ttu-id="50111-123">Disponibelt antal (aktuelt registreret fysisk antal, der findes på lagerstedet)</span><span class="sxs-lookup"><span data-stu-id="50111-123">On hand quantity (current recorded physical quantity located in the warehouse)</span></span>
- <span data-ttu-id="50111-124">Antal i bestilling (samlet registrerede antal i ordre, f.eks. salgsordrer)</span><span class="sxs-lookup"><span data-stu-id="50111-124">On order quantity (total recorded quantity on order, such as sales orders)</span></span>
- <span data-ttu-id="50111-125">Bestilt antal (samlet registrerede bestilte antal, f.eks. indkøbsordrer)</span><span class="sxs-lookup"><span data-stu-id="50111-125">Ordered quantity (total recorded ordered quantity, such as purchase orders)</span></span>

<span data-ttu-id="50111-126">Disse oplysninger hentes pr. frigivet produkt for hvert lagersted og synkroniseres efter ændringssporing, når lagerniveauet ændres.</span><span class="sxs-lookup"><span data-stu-id="50111-126">This information is captured per released product for each warehouse and synchronized based on change tracking, when the inventory level changes.</span></span>

<span data-ttu-id="50111-127">I Field Service opretter integrationsløsningen lagerkladder for deltaet, så niveauerne i Field Service svarer til niveauerne i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="50111-127">In Field Service, the integration solution creates inventory journals for the delta, so that the levels in Field Service match the levels in Finance and Operations.</span></span>

<span data-ttu-id="50111-128">Finance and Operations fungerer som master for lagerniveauer.</span><span class="sxs-lookup"><span data-stu-id="50111-128">Finance and Operations will act as the master for inventory levels.</span></span> <span data-ttu-id="50111-129">Det er derfor vigtigt at konfigurere integration for arbejdsordrer, overførsler og reguleringer fra Field Service til Finance and Operations, hvis disse funktioner bruges i Field Service, sammen med synkronisering af lagerniveauer fra Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="50111-129">Therefore it is important to set up integration for work orders, transfers, and adjustments from Field Service to Finance and Operations if this functionality is used in Field Service, together with synchronization of inventory levels from Finance and Operations.</span></span>

<span data-ttu-id="50111-130">De produkter og lagersteder, hvor lagerniveauer administreres fra Finance and Operations, kan kontrolleres med Avanceret forespørgsel og filtrering (Power-forespørgsel).</span><span class="sxs-lookup"><span data-stu-id="50111-130">The products and warehouses where inventory levels are mastered from Finance and Operations can be controlled with the Advanced Query and Filtering (Power Query).</span></span>

> [!NOTE]
> <span data-ttu-id="50111-131">Det er muligt at oprette flere lagersteder i Field Service (med **Vedligeholdes eksternt = Nej**) og derefter knytte dem til et enkelt lagersted i Finance and Operations, med funktionen Avanceret forespørgsel og filtrering.</span><span class="sxs-lookup"><span data-stu-id="50111-131">It is possible to create multiple warehouses in Field Services (with **Is Externally Maintained = No**) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="50111-132">Dette bruges i situationer, hvor Field Service skal mestre det detaljerede lagerniveau og kun sende opdateringer til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="50111-132">This is used in situations where you want Field Service to master the detailed inventory level and only send updates to Finance and Operations.</span></span> <span data-ttu-id="50111-133">I dette tilfælde modtager Field Service ikke lagerniveauopdateringer fra Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="50111-133">In this case, Field Service will not receive inventory-level updates from Finance and Operations.</span></span> <span data-ttu-id="50111-134">Du kan se flere oplysninger i [Synkroniser lagerreguleringer fra Field Service til Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) og [Synkronisere arbejdsordrer i Field Service med salgsordrer, der er knyttet til projektet i Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="50111-134">For additional information, see [Synchronize inventory adjustments from Field Service to Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="50111-135">CRM-løsning til Field Service</span><span class="sxs-lookup"><span data-stu-id="50111-135">Field Service CRM solution</span></span>
<span data-ttu-id="50111-136">Enheden **Eksternt produktlager** bruges kun til backend i integrationen.</span><span class="sxs-lookup"><span data-stu-id="50111-136">The **External product inventory** entity is only used for back end in to the integration.</span></span> <span data-ttu-id="50111-137">Denne enhed modtager lagerniveauværdierne fra Finance and Operations i integrationen og ændrer derefter disse værdier til manuelle lagerkladder, der derefter ændrer lagerprodukterne på lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="50111-137">This entity receives the inventory level values from Finance and Operations in the integration and then transforms those values to Manual inventory journals, which then changes the Inventory products in the Warehouse.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="50111-138">Forudsætninger og tilknytningsopsætning</span><span class="sxs-lookup"><span data-stu-id="50111-138">Prerequisites and mapping setup</span></span>

### <a name="data-integration-project"></a><span data-ttu-id="50111-139">Dataintegrationsprojekt</span><span class="sxs-lookup"><span data-stu-id="50111-139">Data integration project</span></span>
<span data-ttu-id="50111-140">Du kan anvende filtre i Avanceret forespørgsel og filtrering, så kun bestemte produkter og lagersteder sender lagerniveauoplysninger fra Finance and Operations til Field Service.</span><span class="sxs-lookup"><span data-stu-id="50111-140">You can apply filters with Advanced Query and Filtering so that only certain products and warehouses send inventory-level information from Finance and Operations to Field Service.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="50111-141">Skabelontilknytning i dataintegration</span><span class="sxs-lookup"><span data-stu-id="50111-141">Template mapping in Data integration</span></span>

### <a name="product-inventory-fin-and-ops-to-field-service-product-inventory"></a><span data-ttu-id="50111-142">Produktlager (Fin and Ops til Field Service): produktlager</span><span class="sxs-lookup"><span data-stu-id="50111-142">Product inventory (Fin and Ops to Field Service): Product inventory</span></span>

<span data-ttu-id="50111-143">[![Skabelontilknytning i dataintegration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span><span class="sxs-lookup"><span data-stu-id="50111-143">[![Template mapping in Data integration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span></span>
