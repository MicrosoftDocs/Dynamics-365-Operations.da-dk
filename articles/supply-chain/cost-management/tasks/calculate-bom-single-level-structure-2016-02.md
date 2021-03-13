---
title: Beregne en stykliste ved hjælp af en enkelt struktur (februar 2016)
description: Denne procedure viser, hvordan omkostningerne for et færdigt produkt beregnes ved hjælp af udfoldning på enkeltniveau, der er baseret på efterkalkulationsarket.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 36f908e02c996c0d0a636fd9295b84fcc16b6b63
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011766"
---
# <a name="calculate-a-bom-by-using-a-single-level-structure-february-2016"></a><span data-ttu-id="0a3ca-103">Beregne en stykliste ved hjælp af en enkelt struktur (februar 2016)</span><span class="sxs-lookup"><span data-stu-id="0a3ca-103">Calculate a BOM by using a single level structure (February 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0a3ca-104">Denne procedure viser, hvordan omkostningerne for et færdigt produkt beregnes ved hjælp af udfoldning på enkeltniveau, der er baseret på efterkalkulationsarket.</span><span class="sxs-lookup"><span data-stu-id="0a3ca-104">This procedure shows how to calculate the cost of a finished product by using single level explosion that is based in the Costing sheet.</span></span> <span data-ttu-id="0a3ca-105">Det er den sjette opgave i styklisteberegningsserien.</span><span class="sxs-lookup"><span data-stu-id="0a3ca-105">This is the sixth task in the BOM calculation series.</span></span> <span data-ttu-id="0a3ca-106">Det demodatafirma, der bruges til at oprette denne opgave, er USMF.</span><span class="sxs-lookup"><span data-stu-id="0a3ca-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="0a3ca-107">Gå til Frigivne produkter.</span><span class="sxs-lookup"><span data-stu-id="0a3ca-107">Go to Released products.</span></span>
2. <span data-ttu-id="0a3ca-108">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="0a3ca-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0a3ca-109">Vælg produktet BOM_1.</span><span class="sxs-lookup"><span data-stu-id="0a3ca-109">Select product BOM_1.</span></span>  
3. <span data-ttu-id="0a3ca-110">Klik på Administrer omkostninger i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="0a3ca-110">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="0a3ca-111">Klik på Varepris.</span><span class="sxs-lookup"><span data-stu-id="0a3ca-111">Click Item price.</span></span>
5. <span data-ttu-id="0a3ca-112">Klik på Beregn varens kostpris.</span><span class="sxs-lookup"><span data-stu-id="0a3ca-112">Click Calculate item cost.</span></span>
    * <span data-ttu-id="0a3ca-113">Du skal måske klikke på ellipseknappen (...) for at se denne indstilling i den øverste menu.</span><span class="sxs-lookup"><span data-stu-id="0a3ca-113">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  
6. <span data-ttu-id="0a3ca-114">Klik på rullelisten i feltet Efterkalkulationsversion for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="0a3ca-114">In the Costing version field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="0a3ca-115">I dette eksempel skal du vælge 10.</span><span class="sxs-lookup"><span data-stu-id="0a3ca-115">For this demo, select 10.</span></span> <span data-ttu-id="0a3ca-116">Dette er den samme efterkalkulationsversion, som bruges til at føje kostprisen til komponenterne.</span><span class="sxs-lookup"><span data-stu-id="0a3ca-116">This is the same costing version used for adding the cost price to the components.</span></span>  
7. <span data-ttu-id="0a3ca-117">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0a3ca-117">Click OK.</span></span>
8. <span data-ttu-id="0a3ca-118">Klik på Vis beregningsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="0a3ca-118">Click View calculation details.</span></span>
    * <span data-ttu-id="0a3ca-119">Du skal måske klikke på ellipseknappen (...) for at se denne indstilling i den øverste menu.</span><span class="sxs-lookup"><span data-stu-id="0a3ca-119">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>    <span data-ttu-id="0a3ca-120">Her er kompositionen af omkostningerne: \*    10 er afledt af ITEM_A, 10 fra ITEM_B, 10 fra BOM_2.</span><span class="sxs-lookup"><span data-stu-id="0a3ca-120">Here's the composition of the cost:  \*    10 is derived from ITEM_A, 10 from ITEM_B, 10 from BOM_2.</span></span> <span data-ttu-id="0a3ca-121">Der er i dette tilfælde ingen oplysninger om BOM_2, fordi den blev angivet som en standardomkostning på 10, men ikke blev angivet gennem beregning.</span><span class="sxs-lookup"><span data-stu-id="0a3ca-121">In this case there are no details for BOM_2 because it was entered as a standard cost of 10 but not done through calculation.</span></span>  <span data-ttu-id="0a3ca-122">\*    7 afledes fra opstillingstiden, der er en konstant omkostning, og yderligere 7 afledes fra procestidshandlingen (proces).</span><span class="sxs-lookup"><span data-stu-id="0a3ca-122">\*    7 is derived from the setup time, which is a constant cost, and additional 7 is derived from the run-time operation (Process).</span></span>  <span data-ttu-id="0a3ca-123">\*    Der findes også andre beløb, der svarer til indirekte omkostninger.</span><span class="sxs-lookup"><span data-stu-id="0a3ca-123">\*    There are also other amounts that correspond to indirect costs.</span></span>  
9. <span data-ttu-id="0a3ca-124">@SysTaskRecorder:_RequestClose</span><span class="sxs-lookup"><span data-stu-id="0a3ca-124">@SysTaskRecorder:_RequestClose</span></span>

