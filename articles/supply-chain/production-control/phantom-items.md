---
title: Fantomvarer
description: Dette emne beskriver, i detaljer, hvordan fantomlinjetypen kan bruges til linjerne i en stykliste og en formel i Dynamics 365 Supply Chain Management.
author: ShylaThompson
manager: tfehr
ms.date: 06/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.search.region: Global
ms.author: kamaybac
ms.search.validfrom: ''
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: b14bebadd7088c9bbcfb6b1c5df1fe1a3c98694d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424812"
---
# <a name="phantom-items"></a><span data-ttu-id="d19d8-103">Fantomvarer</span><span class="sxs-lookup"><span data-stu-id="d19d8-103">Phantom items</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d19d8-104">Dette emne beskriver, i detaljer, hvordan fantomlinjetypen kan bruges til linjerne i en stykliste og en formel.</span><span class="sxs-lookup"><span data-stu-id="d19d8-104">This topic describes, in detail, how the Phantom line type can be used for the lines of a bill of materials (BOM) and a formula.</span></span> <span data-ttu-id="d19d8-105">I følgende illustration er (a) styklisten for produktet H og delene F og G, og (b) er rutearket for produkt H og del F.</span><span class="sxs-lookup"><span data-stu-id="d19d8-105">In the following illustration, (a) is the BOM for product H and parts F and G, and (b) is the route sheet for products H and part F.</span></span>

![Produkt H og del F](media/product-H-part-F.png)


<span data-ttu-id="d19d8-107">Følgende illustration vises et eksempel på en styklistestruktur i to niveauer.</span><span class="sxs-lookup"><span data-stu-id="d19d8-107">This illustration shows an example of a BOM structure in two levels.</span></span> <span data-ttu-id="d19d8-108">Færdigvaren H repræsenterer et produkt til en maskinmontage.</span><span class="sxs-lookup"><span data-stu-id="d19d8-108">Finished product H represents a product for a machine assembly.</span></span> <span data-ttu-id="d19d8-109">Maskinmontagen består af to dele, en elektrisk enhed (F), der har to materialer (A og B), og en gruppe af emballage (G), som også har to materialer (C og D).</span><span class="sxs-lookup"><span data-stu-id="d19d8-109">The machine assembly consists of two parts, an electrical unit (F) that has two materials (A and B) and a group of packaging materials (G) that also has two materials (C and D).</span></span> <span data-ttu-id="d19d8-110">Et andet materiale (E) bruges under den generelle montage af maskinen.</span><span class="sxs-lookup"><span data-stu-id="d19d8-110">Another material (E) is used during the general assembly of the machine.</span></span>

![Produkt H og del F](media/product-H-part-B.png)

<span data-ttu-id="d19d8-112">Foregående illustration repræsenterer styklisten Engineering for produkt H. Denne struktur giver et godt overblik over delene og komponenterne til den overordnede maskinmontage.</span><span class="sxs-lookup"><span data-stu-id="d19d8-112">The preceding illustration represents the Engineering BOM for product H. This structure provides a good overview of the parts and components of the overall machine assembly.</span></span> <span data-ttu-id="d19d8-113">Men selvom produktudviklere måske foretrækker at få vist styklisten på denne måde, viser denne struktur måske ikke korrekt den måde, som maskinen opbygges på på fabrikken.</span><span class="sxs-lookup"><span data-stu-id="d19d8-113">However, although product designers might prefer to see the BOM represented in this way, this structure might not correctly represent the way that the machine is built on the shop floor.</span></span> 

<span data-ttu-id="d19d8-114">Styklisten Engineering i foregående illustration angiver f.eks., at den elektriske enhed F monteres som en separat del på en separat arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="d19d8-114">For example, the Engineering BOM in the preceding illustration indicates that electrical unit F is assembled as a separate part on a separate work order.</span></span> <span data-ttu-id="d19d8-115">Men i produktionen kan det virke mere optimalt at montere den elektriske enhed som en del af den overordnede maskinmontage, og ikke som en separat arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="d19d8-115">However, on the shop floor, it might be judged more optimal to assemble the electrical unit as part of the overall machine assembly, not as a separate work order.</span></span>

<span data-ttu-id="d19d8-116">Styklisten Engineering angiver også, at del G er en separat del.</span><span class="sxs-lookup"><span data-stu-id="d19d8-116">This Engineering BOM also indicates that part G is a separate part.</span></span> <span data-ttu-id="d19d8-117">Men i denne struktur er del G ikke en fysisk del, men en samling af emballagematerialer.</span><span class="sxs-lookup"><span data-stu-id="d19d8-117">However, in this structure, part G doesn’t represent a physical part but a collection of packaging materials.</span></span> 

<span data-ttu-id="d19d8-118">Derfor, selvom styklisten Engineering er meget værdifuld til designet af et produkt og vedligeholdelsen af designet, er det måske ikke den mest logiske måde at understøtte produktionsprocessen på for produktet.</span><span class="sxs-lookup"><span data-stu-id="d19d8-118">Therefore, although an Engineering BOM provides great value for the design of a product and maintenance of that design, it might not be the most logical way to support the manufacturing execution process of the product.</span></span> <span data-ttu-id="d19d8-119">Derimod repræsenterer styklisten Manufacturing den bedste måde at opbygge et produkt på.</span><span class="sxs-lookup"><span data-stu-id="d19d8-119">By contrast, a Manufacturing BOM represents the best way to build a product.</span></span>

<span data-ttu-id="d19d8-120">I følgende illustration vises, hvordan den foregående stykliste Engineering er overgået til styklisten Manufacturing.</span><span class="sxs-lookup"><span data-stu-id="d19d8-120">The following illustration shows how the preceding Engineering BOM is transitioned into a Manufacturing BOM.</span></span> <span data-ttu-id="d19d8-121">I denne illustration er (a) styklisten for produktet H, og b er rutearket for produkt H.</span><span class="sxs-lookup"><span data-stu-id="d19d8-121">In this illustration, (a) is the BOM for product H, and b is the route sheet for product H.</span></span>

<span data-ttu-id="d19d8-122">I denne struktur kan du se, at delene F og G ikke findes, og de materialer, som delene består af, er hævet til næste niveau i styklisten.</span><span class="sxs-lookup"><span data-stu-id="d19d8-122">In this structure, you can see that there is no notion of parts F and G, and the materials that these parts consist of have been elevated to the next BOM level.</span></span> 

<span data-ttu-id="d19d8-123">I modsætning til Engineering-styklisten, som havde to driftsark, har styklisten Manufacturing kun ét driftsark.</span><span class="sxs-lookup"><span data-stu-id="d19d8-123">Unlike the Engineering BOM, which had two operations sheets, the Manufacturing BOM has only one operations sheet.</span></span> <span data-ttu-id="d19d8-124">Emballagedriften, der var knyttet til del G, er også blevet forhøjet og er nu en del af driftsarket for produkt H. Montagen af den elektriske enhed er den første driftsoperation.</span><span class="sxs-lookup"><span data-stu-id="d19d8-124">The packaging operation that was linked to part G has also been elevated and is now part of the operations sheet for product H. The assembly of the electrical unit is the first operation.</span></span> <span data-ttu-id="d19d8-125">Denne ordre er en god idé, da denne enhed bruges i den næste operation, som er maskinmontagen.</span><span class="sxs-lookup"><span data-stu-id="d19d8-125">This order makes good sense, because this unit is used in the next operation, which is the machine assembly.</span></span> <span data-ttu-id="d19d8-126">Den sidste operation er emballagen, der forbruger to emballagematerialer (C og D).</span><span class="sxs-lookup"><span data-stu-id="d19d8-126">The last operation is the packaging operation, which consumes two packing materials (C and D).</span></span>

<span data-ttu-id="d19d8-127">Overgangen mellem Engineering-styklisten og Produktions-styklisten aktiveres via fantomstyklistens linjetype.</span><span class="sxs-lookup"><span data-stu-id="d19d8-127">The transition between the Engineering BOM and the Manufacturing BOM is enabled through the Phantom BOM line type.</span></span> <span data-ttu-id="d19d8-128">Som betegnelsen "fantom" antyder, er delene F og G forsvundet i overgangen mellem de to typer af styklister.</span><span class="sxs-lookup"><span data-stu-id="d19d8-128">As the term “phantom” indicates, parts F and G have disappeared during the transition between the two BOM types.</span></span> <span data-ttu-id="d19d8-129">I dette eksempel anvendes fantomlinjetypen på styklistelinjerne for delene F og G i Engineering-styklisten.</span><span class="sxs-lookup"><span data-stu-id="d19d8-129">In this example, the Phantom line type is applied to the BOM lines for parts F and G in the Engineering BOM.</span></span> <span data-ttu-id="d19d8-130">Når der oprettes en produktionsordre eller batchordre, kopieres styklisten Engineering til produktions- eller batchordren.</span><span class="sxs-lookup"><span data-stu-id="d19d8-130">When a production or batch order is created, the Engineering BOM is copied to the production or batch order.</span></span> <span data-ttu-id="d19d8-131">Når ordren forkalkuleres, sker overgangen fra styklisten Engineering til styklisten Manufacturing, som vist i de foregående illustrationer.</span><span class="sxs-lookup"><span data-stu-id="d19d8-131">Then, when the order is estimated, the transition from the Engineering BOM to the Manufacturing BOM occurs, as shown in the preceding illustrations.</span></span> <span data-ttu-id="d19d8-132">Fra driftsarket i den anden illustration indtastes emballagematerialerne C og D for operationen.</span><span class="sxs-lookup"><span data-stu-id="d19d8-132">From the operations sheet in the second illustration, packaging materials C and D are input for the operation.</span></span> 

## <a name="multilevel-phantom-bom-structures"></a><span data-ttu-id="d19d8-133">Flere strukturniveauer af fantomstykliste</span><span class="sxs-lookup"><span data-stu-id="d19d8-133">Multilevel phantom BOM structures</span></span>
<span data-ttu-id="d19d8-134">Fantomlinjetypen kan bruges i flere niveauer styklisteniveauer, som vist i følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="d19d8-134">The Phantom line type can be used in multilevel BOM structures, as shown in the following illustration.</span></span> <span data-ttu-id="d19d8-135">I denne illustration er (a) styklisten for produkt G, og (b) er rutearket for del E og F og produkt G.</span><span class="sxs-lookup"><span data-stu-id="d19d8-135">In this illustration, (a) is the BOM for product G, and (b) is the route sheet for parts E and F and product G.</span></span> 

![Produkt G og del F med ruteark](media/product-G-route-sheet-G.png)


<span data-ttu-id="d19d8-137">I følgende illustration vises styklisten Manufacturing og rutearket, hvis styklistelinjerne for del E og F er konfigureret, så linjetypen er Fantom.</span><span class="sxs-lookup"><span data-stu-id="d19d8-137">The following illustration shows the resulting Manufacturing BOM and route sheet if the BOM lines for parts E and F are configured so that the line type is Phantom.</span></span> <span data-ttu-id="d19d8-138">I denne illustration er (a) styklisten for produkt G, og (b) er rutearket for produkt G.</span><span class="sxs-lookup"><span data-stu-id="d19d8-138">In this illustration, (a) is the BOM for product G, and (b) is the route sheet for product G.</span></span>

![Produkt G](media/product-G.png)


## <a name="phantom-and-route-network"></a><span data-ttu-id="d19d8-140">Fantom- og rutenetværk</span><span class="sxs-lookup"><span data-stu-id="d19d8-140">Phantom and route network</span></span>
<span data-ttu-id="d19d8-141">Fantomstyklister kan også bruges til en stykliste, der har et rutenetværk.</span><span class="sxs-lookup"><span data-stu-id="d19d8-141">Phantom BOMs can also be used for a BOM that has a route network.</span></span> <span data-ttu-id="d19d8-142">I et rutenetværk køres en eller flere driftsoperationer parallelt.</span><span class="sxs-lookup"><span data-stu-id="d19d8-142">In a route network, one or more operations run in parallel.</span></span> <span data-ttu-id="d19d8-143">I følgende illustration vises et eksempel på et rutenetværk, der bruges i en stykliste med flere niveauer.</span><span class="sxs-lookup"><span data-stu-id="d19d8-143">The following illustration shows an example of a route network that is used in a multilevel BOM.</span></span> <span data-ttu-id="d19d8-144">I denne illustration er (a) styklisten for produkt G og del F, og (b) er rutearket for produkt G og del F, som har et rutenetværk.</span><span class="sxs-lookup"><span data-stu-id="d19d8-144">In this illustration, (a) is the BOM for product G and part F, and (b) is the route sheet for product G and part F, which has a route network.</span></span>

![Produkt G og del F](media/product-G-part-F.png)


<span data-ttu-id="d19d8-146">I følgende illustration er (a) styklisten for produkt G og del F, og (b) er rutearket for produkt G og del F.</span><span class="sxs-lookup"><span data-stu-id="d19d8-146">In the following illustration, (a) is the BOM for product G and part F, and (b) is the route sheet for product G and part F.</span></span>

![Produkt G og del F med ruteark](media/product-G-part-F-with-route-sheet.png)
