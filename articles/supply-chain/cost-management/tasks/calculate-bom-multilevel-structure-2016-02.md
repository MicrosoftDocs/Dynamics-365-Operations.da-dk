---
title: Beregne en stykliste ved hjælp af en struktur for flere niveauer (februar 2016)
description: Denne procedure viser, hvordan omkostningerne for et færdigt produkt beregnes ved hjælp af udfoldning på flere niveauer, der er baseret på efterkalkulationsarket.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog, BOMCalcTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fcc1248d64145c10f1c67bfac49c053e99dc1598
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1557657"
---
# <a name="calculate-a-bom-by-using-a-multilevel-structure-february-2016"></a><span data-ttu-id="eac82-103">Beregne en stykliste ved hjælp af en struktur for flere niveauer (februar 2016)</span><span class="sxs-lookup"><span data-stu-id="eac82-103">Calculate a BOM by using a multilevel structure (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="eac82-104">Denne procedure viser, hvordan omkostningerne for et færdigt produkt beregnes ved hjælp af udfoldning på flere niveauer, der er baseret på efterkalkulationsarket.</span><span class="sxs-lookup"><span data-stu-id="eac82-104">This procedure shows how to calculate the cost of a finished product by using multilevel explosion that is based in the Costing sheet.</span></span> <span data-ttu-id="eac82-105">Det er den syvende opgave i styklisteberegningsserien.</span><span class="sxs-lookup"><span data-stu-id="eac82-105">It is the seventh task in the BOM calculation series.</span></span> <span data-ttu-id="eac82-106">Det demodatafirma, der bruges til at oprette denne opgave, er USMF.</span><span class="sxs-lookup"><span data-stu-id="eac82-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="eac82-107">Gå til Administration af produktoplysninger > Produkter > Frigivne produkter.</span><span class="sxs-lookup"><span data-stu-id="eac82-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="eac82-108">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="eac82-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="eac82-109">Vælg produktet BOM_1.</span><span class="sxs-lookup"><span data-stu-id="eac82-109">Select product BOM_1.</span></span>  
3. <span data-ttu-id="eac82-110">Klik på Administrer omkostninger i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="eac82-110">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="eac82-111">Klik på Varepris.</span><span class="sxs-lookup"><span data-stu-id="eac82-111">Click Item price.</span></span>
5. <span data-ttu-id="eac82-112">Klik på Beregn varens kostpris.</span><span class="sxs-lookup"><span data-stu-id="eac82-112">Click Calculate item cost.</span></span>
    * <span data-ttu-id="eac82-113">Du skal måske klikke på ellipseknappen (...) for at se denne indstilling i den øverste menu.</span><span class="sxs-lookup"><span data-stu-id="eac82-113">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  
6. <span data-ttu-id="eac82-114">Indtast eller vælg en værdi i feltet Efterkalkulationsversion.</span><span class="sxs-lookup"><span data-stu-id="eac82-114">In the Costing version field, enter or select a value.</span></span>
    * <span data-ttu-id="eac82-115">Vælg Efterkalkulationsversion 20, fordi omkostningstypen er Planlagt, og udfoldningstilstanden er Flere niveauer.</span><span class="sxs-lookup"><span data-stu-id="eac82-115">Select Costing version 20, because it's Planned cost type and Explosion mode is Multilevel.</span></span>   <span data-ttu-id="eac82-116">Udfoldningstilstanden Flere niveauer er for planlagte omkostninger og simuleringer.</span><span class="sxs-lookup"><span data-stu-id="eac82-116">The Multilevel explosion mode is for planned costs and simulations.</span></span> <span data-ttu-id="eac82-117">Den bruges ikke til standardomkostninger.</span><span class="sxs-lookup"><span data-stu-id="eac82-117">It is not used for standard cost.</span></span>  
7. <span data-ttu-id="eac82-118">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="eac82-118">Click OK.</span></span>
8. <span data-ttu-id="eac82-119">Klik på Vis beregningsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="eac82-119">Click View calculation details.</span></span>
    * <span data-ttu-id="eac82-120">Du skal måske klikke på ellipseknappen (...) for at se denne indstilling i den øverste menu.</span><span class="sxs-lookup"><span data-stu-id="eac82-120">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  <span data-ttu-id="eac82-121">Bemærk i dette tilfælde, hvordan BOM_2 er blevet beregnet under hensyntagen til råvare, proces samt faste omkostninger med en total på 29,40 i stedet for standardkostprisen på 10, der blev aktiveret i den indledende opgaveguide i denne serie.</span><span class="sxs-lookup"><span data-stu-id="eac82-121">In this case, notice how BOM_2 has been calculated taking into account the raw material, process, and overhead with a total of 29,40 instead of the standard cost of 10 that was activated in the initial task guide in this series.</span></span>  
9. <span data-ttu-id="eac82-122">Klik på arkfanen Efterkalkulation.</span><span class="sxs-lookup"><span data-stu-id="eac82-122">Click the Costing sheet tab.</span></span>
    * <span data-ttu-id="eac82-123">Hvis du flytter til fanen Efterkalkulation, er totalerne pr. omkostningsgruppe forskellige sammenlignet med den beregning, der er udført i forrige opgaveguide.</span><span class="sxs-lookup"><span data-stu-id="eac82-123">Moving to the Costing sheet tab, the totals per cost group are different compared to the calculation done in previous task guide.</span></span>  
10. <span data-ttu-id="eac82-124">Vælg "Flere" i feltet Niveau.</span><span class="sxs-lookup"><span data-stu-id="eac82-124">In the Level field, select 'Multi'.</span></span>
    * <span data-ttu-id="eac82-125">Når du vælger Flere, klassificeres omkostningerne efter sammensætningen af BOM_2, hvor 10 er afledt af omkostningsgruppen M1 (ITEM_C), og 15,60 er afledt af dens produktion, hvor omkostningsgruppen er L2.</span><span class="sxs-lookup"><span data-stu-id="eac82-125">When selecting Multi, the costs are classified according to the composition of BOM_2, where 10 is derived from the M1 cost group (ITEM_C), and 15,60 is derived from its manufacturing where the cost group is L2.</span></span> <span data-ttu-id="eac82-126">Indirekte omkostninger varierer også.</span><span class="sxs-lookup"><span data-stu-id="eac82-126">Indirect costs also vary.</span></span>  
11. <span data-ttu-id="eac82-127">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="eac82-127">Close the page.</span></span>
12. <span data-ttu-id="eac82-128">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="eac82-128">Close the page.</span></span>

