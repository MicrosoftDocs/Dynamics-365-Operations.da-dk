--- 
title: "Konfigurere attributbaseret prissætning for konfigurerbare produkter"
description: Denne procedure viser, hvordan du opretter attributbaserede priser.
author: YuyuScheller
manager: AnnBe
ms.date: 10/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 6dd2aa1ebc713287120106a9d1ec7dc15c24def9
ms.openlocfilehash: 88402bef6fd5dad38a74795cd31a4046085d6db7
ms.contentlocale: da-dk
ms.lasthandoff: 09/14/2017

---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a><span data-ttu-id="265c6-103">Konfigurere attributbaseret prissætning for konfigurerbare produkter</span><span class="sxs-lookup"><span data-stu-id="265c6-103">Set up attribute-based pricing for configurable products</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="265c6-104">Denne procedure viser, hvordan du opretter attributbaserede priser.</span><span class="sxs-lookup"><span data-stu-id="265c6-104">This procedure shows how to set up attribute-based pricing.</span></span> <span data-ttu-id="265c6-105">Som en forudsætning skal du have en produktkonfigurationsmodel, der har en eller flere komponenter og attributter.</span><span class="sxs-lookup"><span data-stu-id="265c6-105">As a prerequisite, you must have a product configuration model that has one or more components and attributes.</span></span> <span data-ttu-id="265c6-106">I dette eksempel bruges Højttaler af topkvalitet-modellen i demodatafirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="265c6-106">This example uses the High End Speaker product model in the USMF demo data company.</span></span> <span data-ttu-id="265c6-107">Normalt bruger en produktchef denne procedure.</span><span class="sxs-lookup"><span data-stu-id="265c6-107">Typically, a product manager uses this procedure.</span></span>


## <a name="create-a-new-price-model"></a><span data-ttu-id="265c6-108">Opret en ny prismodel</span><span class="sxs-lookup"><span data-stu-id="265c6-108">Create a new price model</span></span>
1. <span data-ttu-id="265c6-109">Klik på Definition af produktvariantmodel.</span><span class="sxs-lookup"><span data-stu-id="265c6-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="265c6-110">Klik på Produktkonfigurationsmodeller.</span><span class="sxs-lookup"><span data-stu-id="265c6-110">Click Product configuration models.</span></span>
3. <span data-ttu-id="265c6-111">På listen skal du vælge linjen Højttaler af topkvalitet, men ikke klikke på linket for navnet.</span><span class="sxs-lookup"><span data-stu-id="265c6-111">In the list, select the High End Speaker line, but don’t click the link for the name.</span></span>
4. <span data-ttu-id="265c6-112">Klik på Model i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="265c6-112">On the Action Pane, click Model.</span></span>
5. <span data-ttu-id="265c6-113">Klik på Prismodeller.</span><span class="sxs-lookup"><span data-stu-id="265c6-113">Click Price models.</span></span>
6. <span data-ttu-id="265c6-114">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="265c6-114">Click New.</span></span>
7. <span data-ttu-id="265c6-115">Angiv en værdi i feltet Prismodel.</span><span class="sxs-lookup"><span data-stu-id="265c6-115">In the Price model name field, type a value.</span></span>
    * <span data-ttu-id="265c6-116">Brug et navn, der gør det nemt at identificere modellen.</span><span class="sxs-lookup"><span data-stu-id="265c6-116">Use a name that makes the model easy to identify.</span></span>  
8. <span data-ttu-id="265c6-117">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="265c6-117">In the Description field, type a value.</span></span>
9. <span data-ttu-id="265c6-118">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="265c6-118">Click Save.</span></span>

## <a name="add-price-elements"></a><span data-ttu-id="265c6-119">Tilføj priselementer</span><span class="sxs-lookup"><span data-stu-id="265c6-119">Add price elements</span></span>
1. <span data-ttu-id="265c6-120">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="265c6-120">Click Edit.</span></span>
    * <span data-ttu-id="265c6-121">Hver komponent i en produktmodel kan have et basispriselement og et vilkårligt antal prisudtryksregler.</span><span class="sxs-lookup"><span data-stu-id="265c6-121">Each component in a product model can have a base price element and any number of price expression rules.</span></span> <span data-ttu-id="265c6-122">Du kan også tilføje priser i forskellige valutaer.</span><span class="sxs-lookup"><span data-stu-id="265c6-122">You can also add prices in different currencies.</span></span>  
2. <span data-ttu-id="265c6-123">Indtast en værdi i feltet Basisprisudtryk.</span><span class="sxs-lookup"><span data-stu-id="265c6-123">In the Base price expression field, type a value.</span></span>
    * <span data-ttu-id="265c6-124">Skriv for eksempel 100.</span><span class="sxs-lookup"><span data-stu-id="265c6-124">For example, type 100.</span></span>   <span data-ttu-id="265c6-125">En basisprisudtryk kan være en numerisk værdi, eller det kan bestå af en matematisk beregning, der omfatter en eller flere attributter.</span><span class="sxs-lookup"><span data-stu-id="265c6-125">A base price expression can be a numerical value, or it can consist of an arithmetic calculation that involves one or more attributes.</span></span>  
3. <span data-ttu-id="265c6-126">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="265c6-126">Click Add.</span></span>
4. <span data-ttu-id="265c6-127">Skriv 'Rosewood' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="265c6-127">In the Name field, type ‘Rosewood’.</span></span>
    * <span data-ttu-id="265c6-128">Navnet på prisudtrykket hjælper med at identificere, hvad priselementet repræsenterer.</span><span class="sxs-lookup"><span data-stu-id="265c6-128">The price expression name helps identify what the price element represents.</span></span> <span data-ttu-id="265c6-129">I dette eksempel opretter vi priselementet for indstillingen Kabinetfinish til Rosewood-højttaler.</span><span class="sxs-lookup"><span data-stu-id="265c6-129">In this example, we are creating a price element for the Rosewood speaker cabinet finish option.</span></span>  
5. <span data-ttu-id="265c6-130">Klik på Rediger betingelse.</span><span class="sxs-lookup"><span data-stu-id="265c6-130">Click Edit condition.</span></span>
    * <span data-ttu-id="265c6-131">En prisbetingelse hjælper med at sikre, at prisudtrykselementet kun er inkluderet i salgsprisen, hvis der findes en bestemt kombination af attributter.</span><span class="sxs-lookup"><span data-stu-id="265c6-131">A price condition helps guarantee that a price expression element is included in the sales price only if a specific combination of attributes is present.</span></span>  
6. <span data-ttu-id="265c6-132">I feltet ConstraintBody skal du angive 'CabinetFinish=="Rosewood"'.</span><span class="sxs-lookup"><span data-stu-id="265c6-132">In the ConstraintBody field, enter 'CabinetFinish=="Rosewood"'.</span></span>
7. <span data-ttu-id="265c6-133">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="265c6-133">Click OK.</span></span>
8. <span data-ttu-id="265c6-134">Skriv en værdi i feltet Udtryk.</span><span class="sxs-lookup"><span data-stu-id="265c6-134">In the Expression field, type a value.</span></span>
    * <span data-ttu-id="265c6-135">Skriv for eksempel 50.</span><span class="sxs-lookup"><span data-stu-id="265c6-135">For example, type 50.</span></span>  
9. <span data-ttu-id="265c6-136">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="265c6-136">Close the page.</span></span>
10. <span data-ttu-id="265c6-137">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="265c6-137">Close the page.</span></span>


