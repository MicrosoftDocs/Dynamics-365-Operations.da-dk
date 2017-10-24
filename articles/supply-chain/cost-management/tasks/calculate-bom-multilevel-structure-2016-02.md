--- 
title: "Beregne en stykliste ved hjælp af en struktur i flere niveauer (kun februar 2016)"
description: "Denne procedure viser, hvordan omkostningerne for et færdigt produkt beregnes ved hjælp af udfoldning på flere niveauer, der er baseret på efterkalkulationsarket."
author: YuyuScheller
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 16c2cacaf70df5455c3ed49b8dcb5756e89f8cb8
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="calculate-a-bom-by-using-a-multilevel-structure-february-2016-only"></a><span data-ttu-id="ae020-103">Beregne en stykliste ved hjælp af en struktur i flere niveauer (kun februar 2016)</span><span class="sxs-lookup"><span data-stu-id="ae020-103">Calculate a BOM by using a multilevel structure (February 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ae020-104">Denne procedure viser, hvordan omkostningerne for et færdigt produkt beregnes ved hjælp af udfoldning på flere niveauer, der er baseret på efterkalkulationsarket.</span><span class="sxs-lookup"><span data-stu-id="ae020-104">This procedure shows how to calculate the cost of a finished product by using multilevel explosion that is based in the Costing sheet.</span></span> <span data-ttu-id="ae020-105">Det er den syvende opgave i styklisteberegningsserien.</span><span class="sxs-lookup"><span data-stu-id="ae020-105">It is the seventh task in the BOM calculation series.</span></span> <span data-ttu-id="ae020-106">Det demodatafirma, der bruges til at oprette denne opgave, er USMF.</span><span class="sxs-lookup"><span data-stu-id="ae020-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="ae020-107">Gå til Administration af produktoplysninger > Produkter > Frigivne produkter.</span><span class="sxs-lookup"><span data-stu-id="ae020-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="ae020-108">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="ae020-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ae020-109">Vælg produktet BOM_1.</span><span class="sxs-lookup"><span data-stu-id="ae020-109">Select product BOM_1.</span></span>  
3. <span data-ttu-id="ae020-110">Klik på Administrer omkostninger i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="ae020-110">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="ae020-111">Klik på Varepris.</span><span class="sxs-lookup"><span data-stu-id="ae020-111">Click Item price.</span></span>
5. <span data-ttu-id="ae020-112">Klik på Beregn varens kostpris.</span><span class="sxs-lookup"><span data-stu-id="ae020-112">Click Calculate item cost.</span></span>
    * <span data-ttu-id="ae020-113">Du skal måske klikke på ellipseknappen (...) for at se denne indstilling i den øverste menu.</span><span class="sxs-lookup"><span data-stu-id="ae020-113">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  
6. <span data-ttu-id="ae020-114">Indtast eller vælg en værdi i feltet Efterkalkulationsversion.</span><span class="sxs-lookup"><span data-stu-id="ae020-114">In the Costing version field, enter or select a value.</span></span>
    * <span data-ttu-id="ae020-115">Vælg Efterkalkulationsversion 20, fordi omkostningstypen er Planlagt, og udfoldningstilstanden er Flere niveauer.</span><span class="sxs-lookup"><span data-stu-id="ae020-115">Select Costing version 20, because it's Planned cost type and Explosion mode is Multilevel.</span></span>   <span data-ttu-id="ae020-116">Udfoldningstilstanden Flere niveauer er for planlagte omkostninger og simuleringer.</span><span class="sxs-lookup"><span data-stu-id="ae020-116">The Multilevel explosion mode is for planned costs and simulations.</span></span> <span data-ttu-id="ae020-117">Den bruges ikke til standardomkostninger.</span><span class="sxs-lookup"><span data-stu-id="ae020-117">It is not used for standard cost.</span></span>  
7. <span data-ttu-id="ae020-118">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="ae020-118">Click OK.</span></span>
8. <span data-ttu-id="ae020-119">Klik på Vis beregningsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="ae020-119">Click View calculation details.</span></span>
    * <span data-ttu-id="ae020-120">Du skal måske klikke på ellipseknappen (...) for at se denne indstilling i den øverste menu.</span><span class="sxs-lookup"><span data-stu-id="ae020-120">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  <span data-ttu-id="ae020-121">Bemærk i dette tilfælde, hvordan BOM_2 er blevet beregnet under hensyntagen til råvare, proces samt faste omkostninger med en total på 29,40 i stedet for standardkostprisen på 10, der blev aktiveret i den indledende opgaveguide i denne serie.</span><span class="sxs-lookup"><span data-stu-id="ae020-121">In this case, notice how BOM_2 has been calculated taking into account the raw material, process, and overhead with a total of 29,40 instead of the standard cost of 10 that was activated in the initial task guide in this series.</span></span>  
9. <span data-ttu-id="ae020-122">Klik på arkfanen Efterkalkulation.</span><span class="sxs-lookup"><span data-stu-id="ae020-122">Click the Costing sheet tab.</span></span>
    * <span data-ttu-id="ae020-123">Hvis du flytter til fanen Efterkalkulation, er totalerne pr. omkostningsgruppe forskellige sammenlignet med den beregning, der er udført i forrige opgaveguide.</span><span class="sxs-lookup"><span data-stu-id="ae020-123">Moving to the Costing sheet tab, the totals per cost group are different compared to the calculation done in previous task guide.</span></span>  
10. <span data-ttu-id="ae020-124">Vælg "Flere" i feltet Niveau.</span><span class="sxs-lookup"><span data-stu-id="ae020-124">In the Level field, select 'Multi'.</span></span>
    * <span data-ttu-id="ae020-125">Når du vælger Flere, klassificeres omkostningerne efter sammensætningen af BOM_2, hvor 10 er afledt af omkostningsgruppen M1 (ITEM_C), og 15,60 er afledt af dens produktion, hvor omkostningsgruppen er L2.</span><span class="sxs-lookup"><span data-stu-id="ae020-125">When selecting Multi, the costs are classified according to the composition of BOM_2, where 10 is derived from the M1 cost group (ITEM_C), and 15,60 is derived from its manufacturing where the cost group is L2.</span></span> <span data-ttu-id="ae020-126">Indirekte omkostninger varierer også.</span><span class="sxs-lookup"><span data-stu-id="ae020-126">Indirect costs also vary.</span></span>  
11. <span data-ttu-id="ae020-127">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ae020-127">Close the page.</span></span>
12. <span data-ttu-id="ae020-128">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ae020-128">Close the page.</span></span>


