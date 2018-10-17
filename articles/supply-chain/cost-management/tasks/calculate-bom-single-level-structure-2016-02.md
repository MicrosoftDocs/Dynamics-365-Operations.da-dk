--- 
title: "Beregne en stykliste ved hjælp af en enkelt struktur (februar 2016)"
description: "Denne procedure viser, hvordan omkostningerne for et færdigt produkt beregnes ved hjælp af udfoldning på enkeltniveau, der er baseret på efterkalkulationsarket."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: f74f8e4efc4474693f0a5b543c1300c3b64ecda0
ms.contentlocale: da-dk
ms.lasthandoff: 09/14/2018

---
# <a name="calculate-a-bom-by-using-a-single-level-structure-february-2016"></a><span data-ttu-id="f7025-103">Beregne en stykliste ved hjælp af en enkelt struktur (februar 2016)</span><span class="sxs-lookup"><span data-stu-id="f7025-103">Calculate a BOM by using a single level structure (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f7025-104">Denne procedure viser, hvordan omkostningerne for et færdigt produkt beregnes ved hjælp af udfoldning på enkeltniveau, der er baseret på efterkalkulationsarket.</span><span class="sxs-lookup"><span data-stu-id="f7025-104">This procedure shows how to calculate the cost of a finished product by using single level explosion that is based in the Costing sheet.</span></span> <span data-ttu-id="f7025-105">Det er den sjette opgave i styklisteberegningsserien.</span><span class="sxs-lookup"><span data-stu-id="f7025-105">This is the sixth task in the BOM calculation series.</span></span> <span data-ttu-id="f7025-106">Det demodatafirma, der bruges til at oprette denne opgave, er USMF.</span><span class="sxs-lookup"><span data-stu-id="f7025-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="f7025-107">Gå til Frigivne produkter.</span><span class="sxs-lookup"><span data-stu-id="f7025-107">Go to Released products.</span></span>
2. <span data-ttu-id="f7025-108">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="f7025-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f7025-109">Vælg produktet BOM_1.</span><span class="sxs-lookup"><span data-stu-id="f7025-109">Select product BOM_1.</span></span>  
3. <span data-ttu-id="f7025-110">Klik på Administrer omkostninger i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="f7025-110">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="f7025-111">Klik på Varepris.</span><span class="sxs-lookup"><span data-stu-id="f7025-111">Click Item price.</span></span>
5. <span data-ttu-id="f7025-112">Klik på Beregn varens kostpris.</span><span class="sxs-lookup"><span data-stu-id="f7025-112">Click Calculate item cost.</span></span>
    * <span data-ttu-id="f7025-113">Du skal måske klikke på ellipseknappen (...) for at se denne indstilling i den øverste menu.</span><span class="sxs-lookup"><span data-stu-id="f7025-113">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  
6. <span data-ttu-id="f7025-114">Klik på rullelisten i feltet Efterkalkulationsversion for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="f7025-114">In the Costing version field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f7025-115">I dette eksempel skal du vælge 10.</span><span class="sxs-lookup"><span data-stu-id="f7025-115">For this demo, select 10.</span></span> <span data-ttu-id="f7025-116">Dette er den samme efterkalkulationsversion, som bruges til at føje kostprisen til komponenterne.</span><span class="sxs-lookup"><span data-stu-id="f7025-116">This is the same costing version used for adding the cost price to the components.</span></span>  
7. <span data-ttu-id="f7025-117">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="f7025-117">Click OK.</span></span>
8. <span data-ttu-id="f7025-118">Klik på Vis beregningsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="f7025-118">Click View calculation details.</span></span>
    * <span data-ttu-id="f7025-119">Du skal måske klikke på ellipseknappen (...) for at se denne indstilling i den øverste menu.</span><span class="sxs-lookup"><span data-stu-id="f7025-119">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>    <span data-ttu-id="f7025-120">Her er kompositionen af omkostningerne: • 10 er afledt af ITEM_A, 10 fra ITEM_B, 10 fra BOM_2.</span><span class="sxs-lookup"><span data-stu-id="f7025-120">Here's the composition of the cost:  •    10 is derived from ITEM_A, 10 from ITEM_B, 10 from BOM_2.</span></span> <span data-ttu-id="f7025-121">Der er i dette tilfælde ingen oplysninger om BOM_2, fordi den blev angivet som en standardomkostning på 10, men ikke blev angivet gennem beregning.</span><span class="sxs-lookup"><span data-stu-id="f7025-121">In this case there are no details for BOM_2 because it was entered as a standard cost of 10 but not done through calculation.</span></span>  <span data-ttu-id="f7025-122">• 7 afledes fra opstillingstiden, der er en konstant omkostning, og yderligere 7 afledes fra procestidshandlingen (proces).</span><span class="sxs-lookup"><span data-stu-id="f7025-122">•  7 is derived from the setup time, which is a constant cost, and additional 7 is derived from the run-time operation (Process).</span></span>  <span data-ttu-id="f7025-123">• Der findes også andre beløb, der svarer til indirekte omkostninger.</span><span class="sxs-lookup"><span data-stu-id="f7025-123">•   There are also other amounts that correspond to indirect costs.</span></span>  
9. @SysTaskRecorder:_RequestClose


