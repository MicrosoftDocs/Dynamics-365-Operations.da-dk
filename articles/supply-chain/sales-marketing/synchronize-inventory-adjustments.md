---
title: Synkronisere lageroverførsler og reguleringer fra Field Service til Supply Chain Management
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere lagerreguleringer og overførsler fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 04/30/2019
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
ms.openlocfilehash: d76adf10b9df48f5a7a5196e0469bb7cb1dbb34f
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/03/2019
ms.locfileid: "2552227"
---
# <a name="synchronize-inventory-transfers-and-adjustments-from-field-service-to-supply-chain-management"></a><span data-ttu-id="ed5d8-103">Synkronisere lageroverførsler og reguleringer fra Field Service til Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="ed5d8-103">Synchronize inventory transfers and adjustments from Field Service to Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ed5d8-104">I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere lagerreguleringer og overførsler fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="ed5d8-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory adjustments and transfers from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="ed5d8-105">[![Synkronisering af forretningsprocesser mellem Supply Chain Management og Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span><span class="sxs-lookup"><span data-stu-id="ed5d8-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="ed5d8-106">Skabeloner og opgaver</span><span class="sxs-lookup"><span data-stu-id="ed5d8-106">Templates and tasks</span></span>
<span data-ttu-id="ed5d8-107">Følgende skabelon og underliggende opgaver bruges til at synkronisere lagerreguleringer og overføre fra Field Service til Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ed5d8-107">The following template and underlying tasks are used to synchronize inventory adjustments and transfers from Field Service to Supply Chain Management.</span></span>

<span data-ttu-id="ed5d8-108">**Skabeloner i dataintegration**</span><span class="sxs-lookup"><span data-stu-id="ed5d8-108">**Templates in Data integration**</span></span>
- <span data-ttu-id="ed5d8-109">Lagerregulering (Field Service til Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="ed5d8-109">Inventory Adjustment (Field Service to Supply Chain Management)</span></span>
- <span data-ttu-id="ed5d8-110">Lageroverførsler (Field Service til Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="ed5d8-110">Inventory Transfers (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="ed5d8-111">**Opgaver i dataintegrationsprojekterne**</span><span class="sxs-lookup"><span data-stu-id="ed5d8-111">**Tasks in the Data integration projects**</span></span>
- <span data-ttu-id="ed5d8-112">Lagerreguleringer</span><span class="sxs-lookup"><span data-stu-id="ed5d8-112">Inventory Adjustments</span></span>
- <span data-ttu-id="ed5d8-113">Lageroverførsler</span><span class="sxs-lookup"><span data-stu-id="ed5d8-113">Inventory Transfers</span></span>

## <a name="entity-set"></a><span data-ttu-id="ed5d8-114">Enhedssæt</span><span class="sxs-lookup"><span data-stu-id="ed5d8-114">Entity set</span></span>
| <span data-ttu-id="ed5d8-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="ed5d8-115">Field Service</span></span>                     | <span data-ttu-id="ed5d8-116">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="ed5d8-116">Supply Chain Management</span></span>                          |
|-----------------------------------|----------------------------------------------------|
| <span data-ttu-id="ed5d8-117">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="ed5d8-117">msdyn_inventoryadjustmentproducts</span></span> |   <span data-ttu-id="ed5d8-118">CDS Overskrifter og linjer til lagerreguleringskladde</span><span class="sxs-lookup"><span data-stu-id="ed5d8-118">CDS Inventory adjustment journal headers and lines</span></span> |
| <span data-ttu-id="ed5d8-119">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="ed5d8-119">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="ed5d8-120">CDS Overskrifter og linjer til lageroverførselskladde</span><span class="sxs-lookup"><span data-stu-id="ed5d8-120">CDS inventory transfer journal headers and lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="ed5d8-121">Enhedsflow</span><span class="sxs-lookup"><span data-stu-id="ed5d8-121">Entity flow</span></span>
<span data-ttu-id="ed5d8-122">Lagerreguleringer og -overførsler, der er foretaget i Field Service, synkroniseres til Supply Chain Management, når **Bogføringsstatus** ændres fra **Oprettet** til **Bogført**.</span><span class="sxs-lookup"><span data-stu-id="ed5d8-122">Inventory adjustments and transfers made in Field Service will synchronize to Supply Chain Management after the **Post status** changes from **Created** to **Posted**.</span></span> <span data-ttu-id="ed5d8-123">Når dette sker, låses reguleringen eller flytteordren og bliver skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="ed5d8-123">When this occurs, the adjustment or the transfer order will be locked and become read only.</span></span> <span data-ttu-id="ed5d8-124">Det betyder, at reguleringer og overførsler kan bogføres i Supply Chain Management, men ikke kan ændres.</span><span class="sxs-lookup"><span data-stu-id="ed5d8-124">This means that adjustments and transfers can be posted in Supply Chain Management, but cannot be modified.</span></span> <span data-ttu-id="ed5d8-125">Du kan konfigurere et batchjob til automatisk at bogføre reguleringerne og overføre lagerkladder, der er genereret under integrationen, i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ed5d8-125">In Supply Chain Management, you can set up a batch job to automatically post the adjustments and transfer inventory journals that have been generated during the integration.</span></span> <span data-ttu-id="ed5d8-126">Følgende forudsætninger indeholder oplysninger om, hvordan du aktiverer batchjobbet.</span><span class="sxs-lookup"><span data-stu-id="ed5d8-126">See the following prerequisites for details on how to enable the batch job.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="ed5d8-127">CRM-løsning til Field Service</span><span class="sxs-lookup"><span data-stu-id="ed5d8-127">Field Service CRM solution</span></span> 
<span data-ttu-id="ed5d8-128">Feltet **Lagerenhed** er blevet føjet til **Produkt**-enheden.</span><span class="sxs-lookup"><span data-stu-id="ed5d8-128">The **Inventory unit** field has been added to the **Product** entity.</span></span> <span data-ttu-id="ed5d8-129">Dette felt er nødvendigt, fordi salgs- og lagerenheden ikke altid er identisk i Supply Chain Management, og lagerenheden skal bruges i lagerstedet i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ed5d8-129">This field is needed because the Sales and Inventory unit is not always the same in Supply Chain Management, and the Inventory Unit is needed for the Warehouse Inventory in Supply Chain Management.</span></span>
<span data-ttu-id="ed5d8-130">Når du angiver produktet i et lagerreguleringsprodukt for både lagerreguleringer og lageroverførsler, hentes enheden fra lagerproduktværdien.</span><span class="sxs-lookup"><span data-stu-id="ed5d8-130">When you set the product on an Inventory adjustment product for both Inventory adjustments and Inventory transfers, the unit will be fetched from the inventory product value.</span></span> <span data-ttu-id="ed5d8-131">Hvis der findes en værdi, låses feltet **Enhed** i lagerreguleringsproduktet.</span><span class="sxs-lookup"><span data-stu-id="ed5d8-131">If a value is found, the **Unit** field will be locked on the Inventory adjustment product.</span></span>

<span data-ttu-id="ed5d8-132">Feltet **Bogføringsstatus** er føjet til både **Lagerregulering**-enheden og **Lageroverførsel**-enheden.</span><span class="sxs-lookup"><span data-stu-id="ed5d8-132">The **Post status** field has been added to both the **Inventory adjustment** entity and the **Inventory transfer** entity.</span></span> <span data-ttu-id="ed5d8-133">Dette felt bruges som et filter for, hvornår der sendes en regulering eller overførsel til Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ed5d8-133">This field is used as a filter when an adjustment or transfer is sent to Supply Chain Management.</span></span> <span data-ttu-id="ed5d8-134">Standardværdien for dette felt er Oprettet (1), men den ikke sendes til Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ed5d8-134">The default for this field is Created (1), however it is not sent to Supply Chain Management.</span></span> <span data-ttu-id="ed5d8-135">Når du opdaterer værdien til Bogført (2), sendes den til Supply Chain Management, men derefter kan du ikke længere ændre reguleringen eller overførslen eller tilføje nye linjer.</span><span class="sxs-lookup"><span data-stu-id="ed5d8-135">When you update the value to Posted (2), it is sent to Supply Chain Management, but after that you will no longer be able to change the adjustment or transfer or add new lines.</span></span>

<span data-ttu-id="ed5d8-136">Feltet **Nummerserie** er blevet føjet til enheden **Lagerreguleringsprodukt**.</span><span class="sxs-lookup"><span data-stu-id="ed5d8-136">The **Number sequence** field has been added to the **Inventory adjustment product** entity.</span></span> <span data-ttu-id="ed5d8-137">Feltet sikrer, at integrationen har et entydigt nummer, så integrationen kan oprette og opdatere reguleringen.</span><span class="sxs-lookup"><span data-stu-id="ed5d8-137">This field ensures that the integration has a unique number, so the integration can create and update the adjustment.</span></span> <span data-ttu-id="ed5d8-138">Når du opretter dit første lagerreguleringsprodukt, oprettes en ny post i enheden **P2C Autonummerering** for at vedligeholde den nummerserie og det præfiks, der bruges.</span><span class="sxs-lookup"><span data-stu-id="ed5d8-138">When you create your first inventory adjustment product, it will create a new record in the **P2C AutoNumber** entity to maintain the number series and the prefix that is used.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="ed5d8-139">Forudsætninger og tilknytningsopsætning</span><span class="sxs-lookup"><span data-stu-id="ed5d8-139">Prerequisites and mapping setup</span></span>

### <a name="supply-chain-management"></a><span data-ttu-id="ed5d8-140">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="ed5d8-140">Supply Chain Management</span></span>
<span data-ttu-id="ed5d8-141">De integrationslagerkladder, der genereres af integrationen, kan automatisk bogføres ved hjælp af et batchjob.</span><span class="sxs-lookup"><span data-stu-id="ed5d8-141">The integration inventory journals generated by the integration can automatically be posted using a batch job.</span></span> <span data-ttu-id="ed5d8-142">Dette aktiveres fra **Lagerstyring > Periodiske opgaver > CDS-integration > Bogfør integrationen af lagerkladder**.</span><span class="sxs-lookup"><span data-stu-id="ed5d8-142">This is enabled from **Inventory management > Periodic tasks > CDS integration > Post integration inventory journals**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="ed5d8-143">Skabelontilknytning i dataintegration</span><span class="sxs-lookup"><span data-stu-id="ed5d8-143">Template mapping in Data integration</span></span>

<span data-ttu-id="ed5d8-144">Følgende illustration viser skabelontilknytningen i Dataintegration.</span><span class="sxs-lookup"><span data-stu-id="ed5d8-144">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="inventory-adjustment-field-service-to-supply-chain-management-inventory-adjustment"></a><span data-ttu-id="ed5d8-145">Lagerregulering (Field Service til Supply Chain Management): Lagerregulering</span><span class="sxs-lookup"><span data-stu-id="ed5d8-145">Inventory adjustment (Field Service to Supply Chain Management): Inventory adjustment</span></span>

<span data-ttu-id="ed5d8-146">[![Skabelontilknytning i dataintegration](./media/FSAdj1.png)](./media/FSAdj1.png)</span><span class="sxs-lookup"><span data-stu-id="ed5d8-146">[![Template mapping in Data integration](./media/FSAdj1.png)](./media/FSAdj1.png)</span></span>


### <a name="inventory-transfer-field-service-to-supply-chain-management-inventory-transfer"></a><span data-ttu-id="ed5d8-147">Lageroverførsel (Field Service til Supply Chain Management): Lageroverførsel</span><span class="sxs-lookup"><span data-stu-id="ed5d8-147">Inventory transfer (Field Service to Supply Chain Management): Inventory transfer</span></span>

<span data-ttu-id="ed5d8-148">[![Skabelontilknytning i dataintegration](./media/FSTrans1.png)](./media/FSTrans1.png)</span><span class="sxs-lookup"><span data-stu-id="ed5d8-148">[![Template mapping in Data integration](./media/FSTrans1.png)](./media/FSTrans1.png)</span></span>
