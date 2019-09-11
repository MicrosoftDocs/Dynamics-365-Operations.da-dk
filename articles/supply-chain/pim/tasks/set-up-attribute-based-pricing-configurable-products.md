---
title: Konfigurere attributbaseret prissætning for konfigurerbare produkter
description: I dette emne beskrives, hvordan du opretter attributbaserede priser.
author: ShylaThompson
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 534e9c9332c107afebd814cf2090ecbdf0ec6459
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914693"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a><span data-ttu-id="3904f-103">Konfigurere attributbaseret prissætning for konfigurerbare produkter</span><span class="sxs-lookup"><span data-stu-id="3904f-103">Set up attribute-based pricing for configurable products</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3904f-104">I dette emne beskrives, hvordan du opretter attributbaserede priser.</span><span class="sxs-lookup"><span data-stu-id="3904f-104">This topic explains how to set up attribute-based pricing.</span></span> <span data-ttu-id="3904f-105">Som en forudsætning skal du have en produktkonfigurationsmodel, der har en eller flere komponenter og attributter.</span><span class="sxs-lookup"><span data-stu-id="3904f-105">As a prerequisite, you must have a product configuration model that has one or more components and attributes.</span></span> <span data-ttu-id="3904f-106">I dette eksempel bruges Højttaler af topkvalitet-modellen i demodatafirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="3904f-106">This example uses the High End Speaker product model in the USMF demo data company.</span></span> <span data-ttu-id="3904f-107">Normalt bruger en produktchef denne procedure.</span><span class="sxs-lookup"><span data-stu-id="3904f-107">Typically, a product manager uses this procedure.</span></span>


## <a name="create-a-new-price-model"></a><span data-ttu-id="3904f-108">Opret en ny prismodel</span><span class="sxs-lookup"><span data-stu-id="3904f-108">Create a new price model</span></span>
1. <span data-ttu-id="3904f-109">Vælg **Definition af produktvariantmodel** på startsiden.</span><span class="sxs-lookup"><span data-stu-id="3904f-109">Select **Product variant model definition** on the home page.</span></span>
2. <span data-ttu-id="3904f-110">Vælg **Produktkonfigurationsmodeller** i sektionen **Links**.</span><span class="sxs-lookup"><span data-stu-id="3904f-110">Select **Product configuration models** in the **links** section.</span></span>
3. <span data-ttu-id="3904f-111">På listen skal du vælge linjen **Højttaler af topkvalitet**, men vælg ikke linket for navnet.</span><span class="sxs-lookup"><span data-stu-id="3904f-111">In the list, select the **High End Speaker** line, but don’t select the link for the name.</span></span>
4. <span data-ttu-id="3904f-112">Vælg **Model** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="3904f-112">On the Action Pane, select **Model**.</span></span>
5. <span data-ttu-id="3904f-113">Vælg **Prismodeller**.</span><span class="sxs-lookup"><span data-stu-id="3904f-113">Select **Price models**.</span></span>
6. <span data-ttu-id="3904f-114">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="3904f-114">Select **New**.</span></span>
7. <span data-ttu-id="3904f-115">Angiv en værdi i feltet **Navn på prismodel**.</span><span class="sxs-lookup"><span data-stu-id="3904f-115">In the **Price model name** field, type a value.</span></span> <span data-ttu-id="3904f-116">Brug et navn, der gør det nemt at identificere modellen.</span><span class="sxs-lookup"><span data-stu-id="3904f-116">Use a name that makes the model easy to identify.</span></span>  
8. <span data-ttu-id="3904f-117">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="3904f-117">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="3904f-118">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="3904f-118">Select **Save**.</span></span>

## <a name="add-price-elements"></a><span data-ttu-id="3904f-119">Tilføj priselementer</span><span class="sxs-lookup"><span data-stu-id="3904f-119">Add price elements</span></span>
1. <span data-ttu-id="3904f-120">Vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="3904f-120">Select **Edit**.</span></span> <span data-ttu-id="3904f-121">Hver komponent i en produktmodel kan have et basispriselement og et vilkårligt antal prisudtryksregler.</span><span class="sxs-lookup"><span data-stu-id="3904f-121">Each component in a product model can have a base price element and any number of price expression rules.</span></span> <span data-ttu-id="3904f-122">Du kan også tilføje priser i forskellige valutaer.</span><span class="sxs-lookup"><span data-stu-id="3904f-122">You can also add prices in different currencies.</span></span>  
2. <span data-ttu-id="3904f-123">Indtast en værdi i feltet **Basisprisudtryk**.</span><span class="sxs-lookup"><span data-stu-id="3904f-123">In the **Base price expression** field, type a value.</span></span> <span data-ttu-id="3904f-124">Skriv for eksempel 100.</span><span class="sxs-lookup"><span data-stu-id="3904f-124">For example, type 100.</span></span> <span data-ttu-id="3904f-125">En basisprisudtryk kan være en numerisk værdi, eller det kan bestå af en matematisk beregning, der omfatter en eller flere attributter.</span><span class="sxs-lookup"><span data-stu-id="3904f-125">A base price expression can be a numerical value, or it can consist of an arithmetic calculation that involves one or more attributes.</span></span>  
3. <span data-ttu-id="3904f-126">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="3904f-126">Select **Add**.</span></span>
4. <span data-ttu-id="3904f-127">Skriv `Rosewood` i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="3904f-127">In the **Name** field, type `Rosewood`.</span></span> <span data-ttu-id="3904f-128">Navnet på prisudtrykket hjælper med at identificere, hvad priselementet repræsenterer.</span><span class="sxs-lookup"><span data-stu-id="3904f-128">The price expression name helps identify what the price element represents.</span></span> <span data-ttu-id="3904f-129">I dette eksempel opretter vi priselementet for indstillingen Kabinetfinish til Rosewood-højttaler.</span><span class="sxs-lookup"><span data-stu-id="3904f-129">In this example, we are creating a price element for the Rosewood speaker cabinet finish option.</span></span>  
5. <span data-ttu-id="3904f-130">Vælg **Rediger betingelse**.</span><span class="sxs-lookup"><span data-stu-id="3904f-130">Select **Edit condition**.</span></span> <span data-ttu-id="3904f-131">En prisbetingelse hjælper med at sikre, at prisudtrykselementet kun er inkluderet i salgsprisen, hvis der findes en bestemt kombination af attributter.</span><span class="sxs-lookup"><span data-stu-id="3904f-131">A price condition helps guarantee that a price expression element is included in the sales price only if a specific combination of attributes is present.</span></span>  
6. <span data-ttu-id="3904f-132">Angiv `CabinetFinish=="Rosewood"` i feltet **ConstraintBody**.</span><span class="sxs-lookup"><span data-stu-id="3904f-132">In the **ConstraintBody** field, enter `CabinetFinish=="Rosewood"`.</span></span>
7. <span data-ttu-id="3904f-133">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="3904f-133">Select **OK**.</span></span>
8. <span data-ttu-id="3904f-134">Skriv en værdi i feltet **Udtryk**.</span><span class="sxs-lookup"><span data-stu-id="3904f-134">In the **Expression** field, type a value.</span></span> <span data-ttu-id="3904f-135">Skriv f.eks. `50`.</span><span class="sxs-lookup"><span data-stu-id="3904f-135">For example, type `50`.</span></span> 
9. <span data-ttu-id="3904f-136">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="3904f-136">Close the page.</span></span>

