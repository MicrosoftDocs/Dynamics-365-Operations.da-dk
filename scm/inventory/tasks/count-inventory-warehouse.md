---
title: "Optælle lager på et lagersted"
description: "Denne procedure fører dig gennem processen med at oprette og bogføre en lageroptællingskladde for at optælle en bestemt vare på en lokalitet på lageret."
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: fa72cb0d651f5e60797fa41f6e2b2cf1891730b5
ms.contentlocale: da-dk
ms.lasthandoff: 09/12/2017

---
# <a name="count-inventory-in-a-warehouse"></a><span data-ttu-id="3708e-103">Optælle lager på et lagersted</span><span class="sxs-lookup"><span data-stu-id="3708e-103">Count inventory in a warehouse</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3708e-104">Denne procedure fører dig gennem processen med at oprette og bogføre en lageroptællingskladde for at optælle en bestemt vare på en lokalitet på lageret.</span><span class="sxs-lookup"><span data-stu-id="3708e-104">This procedure walks you through the process of creating and posting an inventory counting journal in order to count a specific item at a location in the warehouse.</span></span> <span data-ttu-id="3708e-105">Proceduren gælder for "grundlæggende lagerfunktioner", der er tilgængelige i modulet Lager, ikke for den lagerfunktion, der er tilgængelig i modulet Lagerstedsstyring.</span><span class="sxs-lookup"><span data-stu-id="3708e-105">The procedure applies to “basic warehousing” functionality, available in the Inventory management module, not to the warehousing functionality that’s available in the Warehouse management module.</span></span> <span data-ttu-id="3708e-106">Du kan gennemgå denne procedure i demodatafirmaet USMF eller bruge dine egne data.</span><span class="sxs-lookup"><span data-stu-id="3708e-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="3708e-107">Hvis du bruger dine egne data, skal du kontrollere, at produkter og lokaliteter er konfigureret, og at du har oprettet et lagerkladdenavn for optællingskladder.</span><span class="sxs-lookup"><span data-stu-id="3708e-107">If you’re using your own data, make sure that you have products and locations set up, and that you’ve created an inventory journal name for counting journals.</span></span> <span data-ttu-id="3708e-108">Optælling af lager udføres normalt af en lagermedarbejder.</span><span class="sxs-lookup"><span data-stu-id="3708e-108">Inventory counting is normally carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-counting-journal"></a><span data-ttu-id="3708e-109">Opret en lageroptællingskladde</span><span class="sxs-lookup"><span data-stu-id="3708e-109">Create an inventory counting journal</span></span>
1. <span data-ttu-id="3708e-110">Gå til Lagerstyring > Kladdeposteringer > Vareoptælling > Optælling.</span><span class="sxs-lookup"><span data-stu-id="3708e-110">Go to Inventory management > Journal entries > Item counting > Counting.</span></span>
2. <span data-ttu-id="3708e-111">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="3708e-111">Click New.</span></span>
3. <span data-ttu-id="3708e-112">Klik på rullelisten i feltet Navn for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="3708e-112">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="3708e-113">På listen skal du klikke på det lageroptællingskladdenavn, du vil bruge</span><span class="sxs-lookup"><span data-stu-id="3708e-113">In the list, click on the inventory counting journal name you want to use</span></span>
    * <span data-ttu-id="3708e-114">Nogle andre felter udfyldes baseret på opsætningen af det lageroptællingskladdenavn, du vælger.</span><span class="sxs-lookup"><span data-stu-id="3708e-114">Some other fields will be populated based on the setup of the inventory counting journal name that you select.</span></span>  
5. <span data-ttu-id="3708e-115">Klik på rullelisten i feltet Arbejder for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="3708e-115">In the Worker field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="3708e-116">Vælg den arbejder, du vil bruge, på listen.</span><span class="sxs-lookup"><span data-stu-id="3708e-116">In the list, select the worker you want to use.</span></span>
7. <span data-ttu-id="3708e-117">Klik på Vælg.</span><span class="sxs-lookup"><span data-stu-id="3708e-117">Click Select.</span></span>
8. <span data-ttu-id="3708e-118">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="3708e-118">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="3708e-119">Oprette journallinjer</span><span class="sxs-lookup"><span data-stu-id="3708e-119">Create journal lines</span></span>
1. <span data-ttu-id="3708e-120">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="3708e-120">Click New.</span></span>
2. <span data-ttu-id="3708e-121">Klik på rullelisten i feltet Varenummer for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="3708e-121">In the Item number field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="3708e-122">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="3708e-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3708e-123">Hvis du bruger demodatafirmaet USMF, kan du vælge 'A0001'.</span><span class="sxs-lookup"><span data-stu-id="3708e-123">If you are using demo data company USMF, select 'A0001'.</span></span>  
4. <span data-ttu-id="3708e-124">Klik på rullelisten i feltet Sted for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="3708e-124">In the Site field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="3708e-125">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="3708e-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3708e-126">Hvis du bruger demodatafirmaet USMF, skal du vælge stedet '2'.</span><span class="sxs-lookup"><span data-stu-id="3708e-126">If you are using demo data company USMF, select site '2'.</span></span>  
6. <span data-ttu-id="3708e-127">Klik på rullelisten i feltet Lagersted for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="3708e-127">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="3708e-128">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="3708e-128">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3708e-129">Hvis du bruger demodatafirmaet USMF, skal du vælge lagerstedet '24'.</span><span class="sxs-lookup"><span data-stu-id="3708e-129">If you are using demo data company USMF, select warehouse '24'.</span></span>  
8. <span data-ttu-id="3708e-130">Klik på rullelisten i feltet Lokation for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="3708e-130">In the Location field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="3708e-131">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="3708e-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3708e-132">Hvis du bruger demodatafirmaet USMF, skal du vælge lokaliteten 'BULK-001'.</span><span class="sxs-lookup"><span data-stu-id="3708e-132">If you are using demo data company USMF, select location 'BULK-001'</span></span>  
10. <span data-ttu-id="3708e-133">Angiv et tal i feltet Optalt.</span><span class="sxs-lookup"><span data-stu-id="3708e-133">In the Counted field, enter a number.</span></span>
    * <span data-ttu-id="3708e-134">Hvis du angiver et optalte antal, der adskiller sig fra det tal, der vises i feltet Beholdning, opdateres feltet Antal for at vise forskellen.</span><span class="sxs-lookup"><span data-stu-id="3708e-134">If you enter a counted number that’s different to the number shown in the On-hand field, the Quantity field is updated to show the discrepancy.</span></span>  
11. <span data-ttu-id="3708e-135">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="3708e-135">Click Save.</span></span>

## <a name="post-the-inventory-counting-journal"></a><span data-ttu-id="3708e-136">Bogfør lageroptællingskladden</span><span class="sxs-lookup"><span data-stu-id="3708e-136">Post the inventory counting journal</span></span>
1. <span data-ttu-id="3708e-137">Klik på Bogfør.</span><span class="sxs-lookup"><span data-stu-id="3708e-137">Click Post.</span></span>
    * <span data-ttu-id="3708e-138">Når du bogfører en lageroptællingskladde, og det optalte beløb er forskelligt fra det beløb, der rapporteres i feltet Beholdning, bogføres en lagertilgang eller lagerafgang, lagerniveauet og -værdien ændres, og der genereres finansposteringer.</span><span class="sxs-lookup"><span data-stu-id="3708e-138">When you post an inventory counting journal, if the counted amount differs from amount that’s reported in the On-hand field an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>  
2. <span data-ttu-id="3708e-139">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="3708e-139">Click OK.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="3708e-140">Få vist lagertransaktioner</span><span class="sxs-lookup"><span data-stu-id="3708e-140">View inventory transactions</span></span>
1. <span data-ttu-id="3708e-141">Klik på lager.</span><span class="sxs-lookup"><span data-stu-id="3708e-141">Click Inventory.</span></span>
2. <span data-ttu-id="3708e-142">Klik på Transaktioner.</span><span class="sxs-lookup"><span data-stu-id="3708e-142">Click Transactions.</span></span>
    * <span data-ttu-id="3708e-143">Her kan du se alle relaterede posteringer, der oprettes, når du bogfører din lageroptællingskladde.</span><span class="sxs-lookup"><span data-stu-id="3708e-143">Here you can see any related transactions that will be created when you post your inventory counting journal.</span></span>   

