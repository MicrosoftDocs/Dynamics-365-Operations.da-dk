--- 
title: "Regulere lagerbeholdninger på lagerstedet (grundlæggende lagerstyring)"
description: "Denne fremgangsmåde fører dig gennem processen med at oprette og bogføre en lagerreguleringsjournal for at justere lagerbeholdningerne af varer på lageret."
author: MarkusFogelberg
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalLossProfit, InventJournalCreate, InventLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 75ff53872fd81d5b25964c1ba65127f9feaf2b45
ms.contentlocale: da-dk
ms.lasthandoff: 09/11/2018

---
# <a name="adjust-stock-levels-in-the-warehouse-basic-warehousing"></a><span data-ttu-id="9f4b8-103">Regulere lagerbeholdninger på lagerstedet (grundlæggende lagerstyring)</span><span class="sxs-lookup"><span data-stu-id="9f4b8-103">Adjust stock levels in the warehouse (basic warehousing)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9f4b8-104">Denne fremgangsmåde fører dig gennem processen med at oprette og bogføre en lagerreguleringsjournal for at justere lagerbeholdningerne af varer på lageret.</span><span class="sxs-lookup"><span data-stu-id="9f4b8-104">This procedure walks you through the process of creating and posting an inventory adjustment journal in order to adjust stock levels of products in the warehouse.</span></span> <span data-ttu-id="9f4b8-105">Du skal have oprettet et lagerjournalnavn for lagerreguleringer, før du begynder på dette.</span><span class="sxs-lookup"><span data-stu-id="9f4b8-105">You need to have an inventory journal name set up for inventory adjustments before you start this.</span></span> <span data-ttu-id="9f4b8-106">Du kan gennemgå denne procedure i demodatafirmaet USMF eller bruge dine egne data.</span><span class="sxs-lookup"><span data-stu-id="9f4b8-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="9f4b8-107">Disse opgaver udføres normalt af en lagermedarbejder.</span><span class="sxs-lookup"><span data-stu-id="9f4b8-107">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-adjustment-journal"></a><span data-ttu-id="9f4b8-108">Oprette en lagerreguleringsjournal</span><span class="sxs-lookup"><span data-stu-id="9f4b8-108">Create an inventory adjustment journal</span></span>
1. <span data-ttu-id="9f4b8-109">Gå til Lagerstyring > Kladdeposteringer > Elementer > Lagerregulering.</span><span class="sxs-lookup"><span data-stu-id="9f4b8-109">Go to Inventory management > Journal entries > Items > Inventory adjustment.</span></span>
2. <span data-ttu-id="9f4b8-110">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="9f4b8-110">Click New.</span></span>
3. <span data-ttu-id="9f4b8-111">Klik på rullelisten i feltet Navn for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="9f4b8-111">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="9f4b8-112">På listen skal du klikke på det lagerreguleringsjournalnavn, du vil bruge.</span><span class="sxs-lookup"><span data-stu-id="9f4b8-112">In the list, click on the inventory adjustment journal name you want to use.</span></span>
    * <span data-ttu-id="9f4b8-113">Nogle andre felter udfyldes baseret på opsætningen af det lagerreguleringsjournalnavn, du vælger.</span><span class="sxs-lookup"><span data-stu-id="9f4b8-113">Some other fields will be populated based on the setup of the inventory adjustment journal name you select.</span></span>  
5. <span data-ttu-id="9f4b8-114">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="9f4b8-114">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="9f4b8-115">Oprette journallinjer</span><span class="sxs-lookup"><span data-stu-id="9f4b8-115">Create journal lines</span></span>
1. <span data-ttu-id="9f4b8-116">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="9f4b8-116">Click New.</span></span>
2. <span data-ttu-id="9f4b8-117">Marker feltet Varenummer på listen.</span><span class="sxs-lookup"><span data-stu-id="9f4b8-117">In the list, mark the item number field.</span></span>
3. <span data-ttu-id="9f4b8-118">Vælg en vare i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="9f4b8-118">In the Item number field, Select an item.</span></span> <span data-ttu-id="9f4b8-119">Hvis du bruger demodatafirmaet USMF, kan du skrive 'D0001'.</span><span class="sxs-lookup"><span data-stu-id="9f4b8-119">If you are using demo data company USMF, type 'D0001'.</span></span>
4. <span data-ttu-id="9f4b8-120">Klik på rullelisten i feltet Sted for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="9f4b8-120">In the Site field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="9f4b8-121">Vælg et sted på listen.</span><span class="sxs-lookup"><span data-stu-id="9f4b8-121">In the list, select a site.</span></span>
6. <span data-ttu-id="9f4b8-122">Klik på rullelisten i feltet Lagersted for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="9f4b8-122">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="9f4b8-123">Vælg et lagersted på listen.</span><span class="sxs-lookup"><span data-stu-id="9f4b8-123">In the list, select a warehouse.</span></span>
    * <span data-ttu-id="9f4b8-124">Hvis du har valgt et element med Lokalitet som en obligatorisk dimension, skal du angive lokaliteten her.</span><span class="sxs-lookup"><span data-stu-id="9f4b8-124">If you have selected an item with Location as a mandatory dimension, you would have to specify the location here.</span></span>  
8. <span data-ttu-id="9f4b8-125">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="9f4b8-125">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="9f4b8-126">Feltet Kostpris angiver kostprisen pr. enhed for lagertilgange.</span><span class="sxs-lookup"><span data-stu-id="9f4b8-126">The cost price field specifies the cost per unit for inventory receipts.</span></span> <span data-ttu-id="9f4b8-127">Hvis omkostningen ikke er defineret for varenummeret, eller hvis du vil ændre den manuelt, skal du gøre det her.</span><span class="sxs-lookup"><span data-stu-id="9f4b8-127">If the cost is not specified for the item number or if you wanted to change it manually, you would do this here.</span></span>  

## <a name="validate-and-post-the-inventory-adjustment-journal"></a><span data-ttu-id="9f4b8-128">Kontrollere og bogføre lagerreguleringsjournalen.</span><span class="sxs-lookup"><span data-stu-id="9f4b8-128">Validate and post the inventory adjustment journal</span></span>
1. <span data-ttu-id="9f4b8-129">Klik på Valider.</span><span class="sxs-lookup"><span data-stu-id="9f4b8-129">Click Validate.</span></span>
2. <span data-ttu-id="9f4b8-130">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="9f4b8-130">Click OK.</span></span>
3. <span data-ttu-id="9f4b8-131">Klik på Bogfør.</span><span class="sxs-lookup"><span data-stu-id="9f4b8-131">Click Post.</span></span>
    * <span data-ttu-id="9f4b8-132">Når du bogfører denne kladdetype, bogføres en lagertilgang eller -afgang, lagerniveauet og -værdien ændres, og der genereres finansposteringer.</span><span class="sxs-lookup"><span data-stu-id="9f4b8-132">When you post this kind of journal, an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>  
4. <span data-ttu-id="9f4b8-133">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="9f4b8-133">Click OK.</span></span>
5. <span data-ttu-id="9f4b8-134">Luk formularen.</span><span class="sxs-lookup"><span data-stu-id="9f4b8-134">Close the form.</span></span>
6. <span data-ttu-id="9f4b8-135">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="9f4b8-135">Close the page.</span></span>


