---
title: "Synkronisere lageroverførsler og reguleringer fra Field Service til Finance and Operations"
description: "Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere lageroverførsler og reguleringer fra Microsoft Dynamics 365 for Finance and Operations med Microsoft Dynamics 365 for Field Service."
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
ms.openlocfilehash: 79a1cfac3fa94223cc9af73e758ce95fd47065c9
ms.contentlocale: da-dk
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a><span data-ttu-id="2330f-103">Synkronisere lagerreguleringer fra Field Service til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2330f-103">Synchronize inventory adjustments from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="2330f-104">Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere lageroverførsler og reguleringer fra Microsoft Dynamics 365 for Finance and Operations med Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="2330f-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory adjustments and transfers from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="2330f-105">[![Synkronisering af forretningsprocesser mellem Finance and Operations og Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span><span class="sxs-lookup"><span data-stu-id="2330f-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="2330f-106">Skabeloner og opgaver</span><span class="sxs-lookup"><span data-stu-id="2330f-106">Templates and tasks</span></span>
<span data-ttu-id="2330f-107">Følgende skabelon og underliggende opgaver bruges til at køre synkronisering af lageroverførsler og reguleringer fra Microsoft Dynamics 365 for Field Service til Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2330f-107">The following template and underlying tasks are used to run synchronization of inventory adjustments and transfers from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="2330f-108">**Navnet på skabelonerne i dataintegration:**</span><span class="sxs-lookup"><span data-stu-id="2330f-108">**Name of the templates in Data integration:**</span></span>
- <span data-ttu-id="2330f-109">Lagerregulering (Field Service til Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="2330f-109">Inventory Adjustment (Field Service to Finance and Operations)</span></span>
- <span data-ttu-id="2330f-110">Lageroverførsler (Field Service til Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="2330f-110">Inventory Transfers (Field Service to Finance and Operations)</span></span>

<span data-ttu-id="2330f-111">**Navne på opgaverne i dataintegrationsprojekterne:**</span><span class="sxs-lookup"><span data-stu-id="2330f-111">**Names of the tasks in the Data integration projects:**</span></span>
- <span data-ttu-id="2330f-112">Lagerreguleringer</span><span class="sxs-lookup"><span data-stu-id="2330f-112">Inventory Adjustments</span></span>
- <span data-ttu-id="2330f-113">Lageroverførsler</span><span class="sxs-lookup"><span data-stu-id="2330f-113">Inventory Transfers</span></span>

## <a name="entity-set"></a><span data-ttu-id="2330f-114">Enhedssæt</span><span class="sxs-lookup"><span data-stu-id="2330f-114">Entity set</span></span>
| <span data-ttu-id="2330f-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="2330f-115">Field Service</span></span>                     | <span data-ttu-id="2330f-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2330f-116">Finance and Operations</span></span>                             |
|-----------------------------------|----------------------------------------------------|
| <span data-ttu-id="2330f-117">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="2330f-117">msdyn_inventoryadjustmentproducts</span></span> |   <span data-ttu-id="2330f-118">CDS Overskrifter og linjer til lagerreguleringskladde</span><span class="sxs-lookup"><span data-stu-id="2330f-118">CDS Inventory adjustment journal headers and lines</span></span> |
| <span data-ttu-id="2330f-119">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="2330f-119">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="2330f-120">CDS Overskrifter og linjer til lageroverførselskladde</span><span class="sxs-lookup"><span data-stu-id="2330f-120">CDS inventory transfer journal headers and lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="2330f-121">Enhedsflow</span><span class="sxs-lookup"><span data-stu-id="2330f-121">Entity flow</span></span>
<span data-ttu-id="2330f-122">Lagerreguleringer og overførsler, der er foretaget i Field Service, synkroniseres til Finance and Operations, når **Bogføringsstatus** ændres fra Oprettet til Bogført.</span><span class="sxs-lookup"><span data-stu-id="2330f-122">Inventory adjustments and transfers made in Field Service will synchronize to Finance and Operations, once the **Post status** is changed from Created to Posted.</span></span> <span data-ttu-id="2330f-123">Når dette sker, låses regulerings- eller overførselsordren og bliver skrivebeskyttet, fordi reguleringer og overførsler muligvis bogføres i Finance and Operations og derfor ikke kan ændres.</span><span class="sxs-lookup"><span data-stu-id="2330f-123">When this happen the adjustment or transfer order will be locked and become read-only, as adjustments and transfers might be posted in Finance and Operations and therefor can't be modified.</span></span>
<span data-ttu-id="2330f-124">Du kan konfigurere et batchjob til automatisk at bogføre reguleringerne og overføre lagerkladder, der er genereret med integrationen, i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2330f-124">In Finance and Operations you can setup a batch job to automatically post the adjustments and transfer inventory journals generated with the integration.</span></span> <span data-ttu-id="2330f-125">Se oplysninger om, hvordan du aktiverer kørslen, i forudsætningen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="2330f-125">See prerequisite below for details on how to enable the batch job.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="2330f-126">CRM-løsning til Field Service</span><span class="sxs-lookup"><span data-stu-id="2330f-126">Field Service CRM solution</span></span> 
<span data-ttu-id="2330f-127">Feltet Lagerenhed er blevet føjet til produktenheden.</span><span class="sxs-lookup"><span data-stu-id="2330f-127">The Inventory Unit field has been added to the Product entity.</span></span> <span data-ttu-id="2330f-128">Dette felt er nødvendigt, fordi salgs- og lagerenheden ikke altid er identiske i Operations, og vi skal bruge lagerenheden i Standardlagersted i Operations.</span><span class="sxs-lookup"><span data-stu-id="2330f-128">This field is needed since the Sales and Inventory Unit is not always the same in Operations, and for the Warehouse Inventory in operations we need the Inventory Unit.</span></span>
<span data-ttu-id="2330f-129">Når du angiver produktet i et lagerreguleringsprodukt for både lagerreguleringer og lageroverførsler, hentes enheden fra værdien Produkters værdi for lagerprodukt.</span><span class="sxs-lookup"><span data-stu-id="2330f-129">When you set the Product on an Inventory Adjustment Product for both Inventory Adjustments and Inventory Transfers the Unit will be fetched from the Products Inventory Product value.</span></span> <span data-ttu-id="2330f-130">Hvis der findes en værdi, låses feltet Enhed i lagerreguleringsproduktet</span><span class="sxs-lookup"><span data-stu-id="2330f-130">If a value is found the Unit field will be locked on the Inventory Adjustment Product</span></span>

<span data-ttu-id="2330f-131">Feltet Bogføringsstatus er føjet til både lagerreguleringsenheden og lageroverførselsenheden.</span><span class="sxs-lookup"><span data-stu-id="2330f-131">The Post Status field has been added to both the Inventory Adjustment entity and the Inventory Transfer entity.</span></span> <span data-ttu-id="2330f-132">Dette felt bruges som et filter for, hvornår der sendes en regulering eller overførsel til Operations.</span><span class="sxs-lookup"><span data-stu-id="2330f-132">This field is used as a filter for when a adjustment or transfer is sent to Operations.</span></span> <span data-ttu-id="2330f-133">Feltet er som standard Oprettet (1), og sendes som sådan ikke til Operations.</span><span class="sxs-lookup"><span data-stu-id="2330f-133">The field is defaulted to Created (1) and its then not sent over to Operations.</span></span> <span data-ttu-id="2330f-134">Når du har ændret til Bogført (2), sendes det til Operations, men du kan derefter ikke længere ændre noget i Regulering eller Overførsel eller føje nye linjer til det.</span><span class="sxs-lookup"><span data-stu-id="2330f-134">Ones you change is to Posted (2) It is sent over to operations, but you will then no longer be able to change anything in the Adjustment or Transfer or add any new lines to it.</span></span>
<span data-ttu-id="2330f-135">Feltet Nummerserie er blevet føjet til produktenheden Lagerregulering.</span><span class="sxs-lookup"><span data-stu-id="2330f-135">The Number Sequence field has been added to the Inventory Adjustment Product entity.</span></span> <span data-ttu-id="2330f-136">Dette felt tildeler integrationen et entydigt nummer, så det står klart, hvornår der skal udføres henholdsvis oprettelser og opdateringer.</span><span class="sxs-lookup"><span data-stu-id="2330f-136">This field helps the integration to have a Unique number, so the integration knows when to do creates and when to do updates.</span></span> <span data-ttu-id="2330f-137">Når du opretter dit første lagerreguleringsprodukt, oprettes en ny post i objektet P2C Autonummerering for at vedligeholde den nummerserie og det præfiks, der bruges.</span><span class="sxs-lookup"><span data-stu-id="2330f-137">When you create your first Inventory Adjustment Product it will create a new record in the P2C AutoNumber entity to maintain the number series and the prefix that is used.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="2330f-138">Forudsætninger og tilknytningsopsætning</span><span class="sxs-lookup"><span data-stu-id="2330f-138">Prerequisites and mapping setup</span></span>

### <a name="in-finance-and-operations"></a><span data-ttu-id="2330f-139">I Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2330f-139">In Finance and Operations</span></span>
<span data-ttu-id="2330f-140">De integrationslagerkladder, der genereres af integrationen, kan automatisk bogføres med et batchjob.</span><span class="sxs-lookup"><span data-stu-id="2330f-140">The integration inventory journals generated by the integration can automatically be posted with a batch job.</span></span> <span data-ttu-id="2330f-141">Dette aktiveres fra: Lagerstyring > Periodiske opgaver > CDS-integration > Bogfør integrationen af lagerkladder</span><span class="sxs-lookup"><span data-stu-id="2330f-141">This is enabled from: Inventory management > Periodic tasks > CDS integration > Post integration inventory journals</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="2330f-142">Skabelontilknytning i dataintegration</span><span class="sxs-lookup"><span data-stu-id="2330f-142">Template mapping in Data integration</span></span>

<span data-ttu-id="2330f-143">Følgende illustration viser skabelontilknytningen i Dataintegration.</span><span class="sxs-lookup"><span data-stu-id="2330f-143">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="inventory-adjustment-field-service-to-finance-and-operations-inventory-adjustment"></a><span data-ttu-id="2330f-144">Lagerregulering (Field Service til Finance and Operations): Lagerregulering</span><span class="sxs-lookup"><span data-stu-id="2330f-144">Inventory Adjustment (Field Service to Finance and Operations): Inventory Adjustment</span></span>

<span data-ttu-id="2330f-145">[![Skabelontilknytning i dataintegration](./media/FSAdj1.png)](./media/FSAdj1.png)</span><span class="sxs-lookup"><span data-stu-id="2330f-145">[![Template mapping in Data integration](./media/FSAdj1.png)](./media/FSAdj1.png)</span></span>


### <a name="inventory-transfer-field-service-to-finance-and-operations-inventory-transfer"></a><span data-ttu-id="2330f-146">Lageroverførsel (Field Service til Finance and Operations): Lageroverførsel</span><span class="sxs-lookup"><span data-stu-id="2330f-146">Inventory Transfer (Field Service to Finance and Operations): Inventory Transfer</span></span>

<span data-ttu-id="2330f-147">[![Skabelontilknytning i dataintegration](./media/FSTrans1.png)](./media/FSTrans1.png)</span><span class="sxs-lookup"><span data-stu-id="2330f-147">[![Template mapping in Data integration](./media/FSTrans1.png)](./media/FSTrans1.png)</span></span>

