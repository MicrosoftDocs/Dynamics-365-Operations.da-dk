---
title: Synkronisere lageroverførsler og reguleringer fra Field Service til Finance and Operations
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere lagerreguleringer og overførsler fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.
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
ms.openlocfilehash: 75181661c41d238cdc06ffbb6969a2efd7d88d46
ms.sourcegitcommit: a6d385db6636ef2b7fb6b24d37a2160c8d5a3c0f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/14/2019
ms.locfileid: "842409"
---
# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a><span data-ttu-id="43841-103">Synkronisere lagerreguleringer fra Field Service til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="43841-103">Synchronize inventory adjustments from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="43841-104">I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere lagerreguleringer og overførsler fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="43841-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory adjustments and transfers from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="43841-105">[![Synkronisering af forretningsprocesser mellem Finance and Operations og Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span><span class="sxs-lookup"><span data-stu-id="43841-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="43841-106">Skabeloner og opgaver</span><span class="sxs-lookup"><span data-stu-id="43841-106">Templates and tasks</span></span>
<span data-ttu-id="43841-107">Følgende skabelon og underliggende opgaver bruges til at synkronisere lagerreguleringer og overførsler fra Microsoft Dynamics 365 for Field Service til Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="43841-107">The following template and underlying tasks are used to synchronize inventory adjustments and transfers from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="43841-108">**Skabeloner i dataintegration**</span><span class="sxs-lookup"><span data-stu-id="43841-108">**Templates in Data integration**</span></span>
- <span data-ttu-id="43841-109">Lagerregulering (Field Service til Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="43841-109">Inventory Adjustment (Field Service to Fin and Ops)</span></span>
- <span data-ttu-id="43841-110">Lageroverførelser (Field Service til Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="43841-110">Inventory Transfers (Field Service to Fin and Ops)</span></span>

<span data-ttu-id="43841-111">**Opgaver i dataintegrationsprojekterne**</span><span class="sxs-lookup"><span data-stu-id="43841-111">**Tasks in the Data integration projects**</span></span>
- <span data-ttu-id="43841-112">Lagerreguleringer</span><span class="sxs-lookup"><span data-stu-id="43841-112">Inventory Adjustments</span></span>
- <span data-ttu-id="43841-113">Lageroverførsler</span><span class="sxs-lookup"><span data-stu-id="43841-113">Inventory Transfers</span></span>

## <a name="entity-set"></a><span data-ttu-id="43841-114">Enhedssæt</span><span class="sxs-lookup"><span data-stu-id="43841-114">Entity set</span></span>
| <span data-ttu-id="43841-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="43841-115">Field Service</span></span>                     | <span data-ttu-id="43841-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="43841-116">Finance and Operations</span></span>                             |
|-----------------------------------|----------------------------------------------------|
| <span data-ttu-id="43841-117">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="43841-117">msdyn_inventoryadjustmentproducts</span></span> |   <span data-ttu-id="43841-118">CDS Overskrifter og linjer til lagerreguleringskladde</span><span class="sxs-lookup"><span data-stu-id="43841-118">CDS Inventory adjustment journal headers and lines</span></span> |
| <span data-ttu-id="43841-119">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="43841-119">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="43841-120">CDS Overskrifter og linjer til lageroverførselskladde</span><span class="sxs-lookup"><span data-stu-id="43841-120">CDS inventory transfer journal headers and lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="43841-121">Enhedsflow</span><span class="sxs-lookup"><span data-stu-id="43841-121">Entity flow</span></span>
<span data-ttu-id="43841-122">Lagerreguleringer og overførsler, der er foretaget i Field Service, synkroniseres til Finance and Operations, når **Bogføringsstatus** ændres fra **Oprettet** til **Bogført**.</span><span class="sxs-lookup"><span data-stu-id="43841-122">Inventory adjustments and transfers made in Field Service will synchronize to Finance and Operations after the **Post status** changes from **Created** to **Posted**.</span></span> <span data-ttu-id="43841-123">Når dette sker, låses reguleringen eller flytteordren og bliver skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="43841-123">When this occurs, the adjustment or the transfer order will be locked and become read only.</span></span> <span data-ttu-id="43841-124">Det betyder, at reguleringer og overførsler kan bogføres i Finance and Operations, men ikke kan ændres.</span><span class="sxs-lookup"><span data-stu-id="43841-124">This means that adjustments and transfers can be posted in Finance and Operations, but cannot be modified.</span></span> <span data-ttu-id="43841-125">Du kan konfigurere et batchjob til automatisk at bogføre reguleringerne og overføre lagerkladder, der er genereret under integrationen, i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="43841-125">In Finance and Operations, you can set up a batch job to automatically post the adjustments and transfer inventory journals that have been generated during the integration.</span></span> <span data-ttu-id="43841-126">Følgende forudsætninger indeholder oplysninger om, hvordan du aktiverer batchjobbet.</span><span class="sxs-lookup"><span data-stu-id="43841-126">See the following prerequisites for details on how to enable the batch job.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="43841-127">CRM-løsning til Field Service</span><span class="sxs-lookup"><span data-stu-id="43841-127">Field Service CRM solution</span></span> 
<span data-ttu-id="43841-128">Feltet **Lagerenhed** er blevet føjet til **Produkt**-enheden.</span><span class="sxs-lookup"><span data-stu-id="43841-128">The **Inventory unit** field has been added to the **Product** entity.</span></span> <span data-ttu-id="43841-129">Dette felt er nødvendigt, fordi salgs- og lagerenheden ikke altid er identisk i Finance and Operations, og lagerenheden skal bruges i lagerstedet i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="43841-129">This field is needed because the Sales and Inventory unit is not always the same in Finance and Operations, and the Inventory Unit is needed for the Warehouse Inventory in Finance and Operations.</span></span>
<span data-ttu-id="43841-130">Når du angiver produktet i et lagerreguleringsprodukt for både lagerreguleringer og lageroverførsler, hentes enheden fra lagerproduktværdien.</span><span class="sxs-lookup"><span data-stu-id="43841-130">When you set the product on an Inventory adjustment product for both Inventory adjustments and Inventory transfers, the unit will be fetched from the inventory product value.</span></span> <span data-ttu-id="43841-131">Hvis der findes en værdi, låses feltet **Enhed** i lagerreguleringsproduktet.</span><span class="sxs-lookup"><span data-stu-id="43841-131">If a value is found, the **Unit** field will be locked on the Inventory adjustment product.</span></span>

<span data-ttu-id="43841-132">Feltet **Bogføringsstatus** er føjet til både **Lagerregulering**-enheden og **Lageroverførsel**-enheden.</span><span class="sxs-lookup"><span data-stu-id="43841-132">The **Post status** field has been added to both the **Inventory adjustment** entity and the **Inventory transfer** entity.</span></span> <span data-ttu-id="43841-133">Dette felt bruges som et filter for, hvornår der sendes en regulering eller overførsel til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="43841-133">This field is used as a filter when an adjustment or transfer is sent to Finance and Operations.</span></span> <span data-ttu-id="43841-134">Standardværdien for dette felt er Oprettet (1), men den ikke sendes til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="43841-134">The default for this field is Created (1), however it is not sent to Finance and Operations.</span></span> <span data-ttu-id="43841-135">Når du opdaterer værdien til Bogført (2), sendes den til Finance and Operations, men derefter kan du ikke længere ændre reguleringen eller overførslen eller tilføje nye linjer.</span><span class="sxs-lookup"><span data-stu-id="43841-135">When you update the value to Posted (2), it is sent to Finance and Operations, but after that you will no longer be able to change the adjustment or transfer or add new lines.</span></span>

<span data-ttu-id="43841-136">Feltet **Nummerserie** er blevet føjet til enheden **Lagerreguleringsprodukt**.</span><span class="sxs-lookup"><span data-stu-id="43841-136">The **Number sequence** field has been added to the **Inventory adjustment product** entity.</span></span> <span data-ttu-id="43841-137">Feltet sikrer, at integrationen har et entydigt nummer, så integrationen kan oprette og opdatere reguleringen.</span><span class="sxs-lookup"><span data-stu-id="43841-137">This field ensures that the integration has a unique number, so the integration can create and update the adjustment.</span></span> <span data-ttu-id="43841-138">Når du opretter dit første lagerreguleringsprodukt, oprettes en ny post i enheden **P2C Autonummerering** for at vedligeholde den nummerserie og det præfiks, der bruges.</span><span class="sxs-lookup"><span data-stu-id="43841-138">When you create your first inventory adjustment product, it will create a new record in the **P2C AutoNumber** entity to maintain the number series and the prefix that is used.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="43841-139">Forudsætninger og tilknytningsopsætning</span><span class="sxs-lookup"><span data-stu-id="43841-139">Prerequisites and mapping setup</span></span>

### <a name="finance-and-operations"></a><span data-ttu-id="43841-140">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="43841-140">Finance and Operations</span></span>
<span data-ttu-id="43841-141">De integrationslagerkladder, der genereres af integrationen, kan automatisk bogføres ved hjælp af et batchjob.</span><span class="sxs-lookup"><span data-stu-id="43841-141">The integration inventory journals generated by the integration can automatically be posted using a batch job.</span></span> <span data-ttu-id="43841-142">Dette aktiveres fra **Lagerstyring > Periodiske opgaver > CDS-integration > Bogfør integrationen af lagerkladder**.</span><span class="sxs-lookup"><span data-stu-id="43841-142">This is enabled from **Inventory management > Periodic tasks > CDS integration > Post integration inventory journals**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="43841-143">Skabelontilknytning i dataintegration</span><span class="sxs-lookup"><span data-stu-id="43841-143">Template mapping in Data integration</span></span>

<span data-ttu-id="43841-144">Følgende illustration viser skabelontilknytningen i Dataintegration.</span><span class="sxs-lookup"><span data-stu-id="43841-144">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="inventory-adjustment-field-service-to-fin-and-ops-inventory-adjustment"></a><span data-ttu-id="43841-145">Lagerregulering (Field Service til Fin and Ops): lagerregulering</span><span class="sxs-lookup"><span data-stu-id="43841-145">Inventory adjustment (Field Service to Fin and Ops): Inventory adjustment</span></span>

<span data-ttu-id="43841-146">[![Skabelontilknytning i dataintegration](./media/FSAdj1.png)](./media/FSAdj1.png)</span><span class="sxs-lookup"><span data-stu-id="43841-146">[![Template mapping in Data integration](./media/FSAdj1.png)](./media/FSAdj1.png)</span></span>


### <a name="inventory-transfer-field-service-to-fin-and-ops-inventory-transfer"></a><span data-ttu-id="43841-147">Lageroverførelse (Field Service til Fin and Ops): lageroverførelse</span><span class="sxs-lookup"><span data-stu-id="43841-147">Inventory transfer (Field Service to Fin and Ops): Inventory transfer</span></span>

<span data-ttu-id="43841-148">[![Skabelontilknytning i dataintegration](./media/FSTrans1.png)](./media/FSTrans1.png)</span><span class="sxs-lookup"><span data-stu-id="43841-148">[![Template mapping in Data integration](./media/FSTrans1.png)](./media/FSTrans1.png)</span></span>
