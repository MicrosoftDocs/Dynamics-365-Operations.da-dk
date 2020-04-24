---
title: Optælle lager på et lagersted
description: Dette emne fører dig gennem processen med at oprette og bogføre en lageroptællingskladde for at optælle en bestemt vare på en lokation på lagerstedet.
author: MarkusFogelberg
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 34013783bab79d80f1dac9a7806042608635e617
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204165"
---
# <a name="count-inventory-in-a-warehouse"></a><span data-ttu-id="c7cdf-103">Optælle lager på et lagersted</span><span class="sxs-lookup"><span data-stu-id="c7cdf-103">Count inventory in a warehouse</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c7cdf-104">Dette emne fører dig gennem processen med at oprette og bogføre en lageroptællingskladde for at optælle en bestemt vare på en lokation på lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="c7cdf-104">This topic describes the process of creating and posting an inventory counting journal in order to count a specific item at a location in the warehouse.</span></span> <span data-ttu-id="c7cdf-105">Proceduren gælder for "grundlæggende lagerfunktioner", der er tilgængelige i modulet Lager, ikke for den lagerfunktion, der er tilgængelig i modulet Lagerstedsstyring.</span><span class="sxs-lookup"><span data-stu-id="c7cdf-105">The procedure applies to "basic warehousing" functionality, available in the Inventory management module, not to the warehousing functionality that's available in the Warehouse management module.</span></span> <span data-ttu-id="c7cdf-106">Du kan gennemgå denne procedure i demodatafirmaet USMF eller bruge dine egne data.</span><span class="sxs-lookup"><span data-stu-id="c7cdf-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="c7cdf-107">Hvis du bruger dine egne data, skal du kontrollere, at produkter og lokaliteter er konfigureret, og at du har oprettet et lagerkladdenavn for optællingskladder.</span><span class="sxs-lookup"><span data-stu-id="c7cdf-107">If you're using your own data, make sure that you have products and locations set up, and that you've created an inventory journal name for counting journals.</span></span> <span data-ttu-id="c7cdf-108">Optælling af lager udføres normalt af en lagermedarbejder.</span><span class="sxs-lookup"><span data-stu-id="c7cdf-108">Inventory counting is normally carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-counting-journal"></a><span data-ttu-id="c7cdf-109">Opret en lageroptællingskladde</span><span class="sxs-lookup"><span data-stu-id="c7cdf-109">Create an inventory counting journal</span></span>
1. <span data-ttu-id="c7cdf-110">Gå til **Navigationsrude > Moduler > Lagerstyring > Kladdeposteringer > Vareoptælling > Optælling**.</span><span class="sxs-lookup"><span data-stu-id="c7cdf-110">Go to **Navigation pane > Modules > Inventory management > Journal entries > Item counting > Counting**.</span></span>
2. <span data-ttu-id="c7cdf-111">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c7cdf-111">Select **New**.</span></span>
3. <span data-ttu-id="c7cdf-112">I feltet **Navn** skal du vælge det lageroptællingskladdenavn, du vil bruge, på rullelisten.</span><span class="sxs-lookup"><span data-stu-id="c7cdf-112">In the **Name** field, select the inventory counting journal name you want to use from the drop-down list.</span></span> <span data-ttu-id="c7cdf-113">Nogle andre felter udfyldes baseret på opsætningen af det lageroptællingskladdenavn, du vælger.</span><span class="sxs-lookup"><span data-stu-id="c7cdf-113">Some other fields will be populated based on the setup of the inventory counting journal name that you select.</span></span>  
4. <span data-ttu-id="c7cdf-114">Vælg rullelisten i feltet **Arbejder** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="c7cdf-114">In the **Worker** field, select the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="c7cdf-115">**Vælg** den arbejder, du vil bruge, på listen.</span><span class="sxs-lookup"><span data-stu-id="c7cdf-115">In the list, **Select** the worker you want to use.</span></span>
6. <span data-ttu-id="c7cdf-116">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="c7cdf-116">Select **OK**.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="c7cdf-117">Opret kladdelinjer</span><span class="sxs-lookup"><span data-stu-id="c7cdf-117">Create journal lines</span></span>
1. <span data-ttu-id="c7cdf-118">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c7cdf-118">Select **New**.</span></span>
2. <span data-ttu-id="c7cdf-119">Vælg den ønskede post på rullelisten i feltet **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="c7cdf-119">In the **Item number** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="c7cdf-120">Hvis du bruger demodatafirmaet USMF, skal du vælge **A0001**.</span><span class="sxs-lookup"><span data-stu-id="c7cdf-120">If you are using demo data company USMF, select **A0001**.</span></span>  
3. <span data-ttu-id="c7cdf-121">Vælg den ønskede post på rullelisten i feltet **Sted**.</span><span class="sxs-lookup"><span data-stu-id="c7cdf-121">In the **Site** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="c7cdf-122">Hvis du bruger demodatafirmaet USMF, skal du vælge stedet **2**.</span><span class="sxs-lookup"><span data-stu-id="c7cdf-122">If you are using demo data company USMF, select site **2**.</span></span>
4. <span data-ttu-id="c7cdf-123">Vælg den ønskede post på rullelisten i feltet **Lagersted**.</span><span class="sxs-lookup"><span data-stu-id="c7cdf-123">In the **Warehouse** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="c7cdf-124">Hvis du bruger demodatafirmaet USMF, skal du vælge lagerstedet **24**.</span><span class="sxs-lookup"><span data-stu-id="c7cdf-124">If you are using demo data company USMF, select warehouse **24**.</span></span>  
5. <span data-ttu-id="c7cdf-125">Vælg den ønskede post på rullelisten i feltet **Lokation**.</span><span class="sxs-lookup"><span data-stu-id="c7cdf-125">In the **Location** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="c7cdf-126">Hvis du bruger demodatafirmaet USMF, skal du vælge lokationen **BULK-001**.</span><span class="sxs-lookup"><span data-stu-id="c7cdf-126">If you are using demo data company USMF, select location **BULK-001**.</span></span>  
6. <span data-ttu-id="c7cdf-127">Angiv et tal i feltet Optalt.</span><span class="sxs-lookup"><span data-stu-id="c7cdf-127">In the Counted field, enter a number.</span></span> <span data-ttu-id="c7cdf-128">Hvis du angiver et optalt antal, der adskiller sig fra det tal, der vises i feltet **Beholdning**, opdateres feltet **Antal** for at vise forskellen.</span><span class="sxs-lookup"><span data-stu-id="c7cdf-128">If you enter a counted number that's different to the number shown in the **On-hand** field, the **Quantity** field is updated to show the discrepancy.</span></span>  
7. <span data-ttu-id="c7cdf-129">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="c7cdf-129">Select **Save**.</span></span>

## <a name="post-the-inventory-counting-journal"></a><span data-ttu-id="c7cdf-130">Bogfør lageroptællingskladden</span><span class="sxs-lookup"><span data-stu-id="c7cdf-130">Post the inventory counting journal</span></span>
1. <span data-ttu-id="c7cdf-131">Vælg **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="c7cdf-131">Select **Post**.</span></span> <span data-ttu-id="c7cdf-132">Når du bogfører en lageroptællingskladde, og det optalte beløb er forskelligt fra det beløb, der rapporteres i feltet **Beholdning**, bogføres en lagertilgang eller lagerafgang, lagerniveauet og -værdien ændres, og der genereres finansposteringer.</span><span class="sxs-lookup"><span data-stu-id="c7cdf-132">When you post an inventory counting journal, if the counted amount differs from amount that's reported in the **On-hand** field an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>
2. <span data-ttu-id="c7cdf-133">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="c7cdf-133">Select **OK**.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="c7cdf-134">Få vist lagertransaktioner</span><span class="sxs-lookup"><span data-stu-id="c7cdf-134">View inventory transactions</span></span>
1. <span data-ttu-id="c7cdf-135">Vælg **Lager**.</span><span class="sxs-lookup"><span data-stu-id="c7cdf-135">Select **Inventory**.</span></span>
2. <span data-ttu-id="c7cdf-136">Vælg **Transaktioner**.</span><span class="sxs-lookup"><span data-stu-id="c7cdf-136">Select **Transactions**.</span></span> <span data-ttu-id="c7cdf-137">Her kan du se alle relaterede posteringer, der oprettes, når du bogfører din lageroptællingskladde.</span><span class="sxs-lookup"><span data-stu-id="c7cdf-137">Here you can see any related transactions that will be created when you post your inventory counting journal.</span></span>   

