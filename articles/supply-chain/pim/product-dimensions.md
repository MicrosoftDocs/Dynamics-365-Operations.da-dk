---
title: Produktdimensioner
description: "Der er fire produktdimensioner – farve, konfiguration, størrelse og type. Du kan kombinere produktdimensioner i dimensionsgrupper og tildele dimensionsgrupper til produktmastere. Kombinationerne af produktdimensioner bestemmer, hvordan produktvarianter defineres."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDimension, EcoResProductDimensionGroup, EcoResProductMasterDimension, RetailEcoResColor, RetailEcoResSize, RetailEcoResStyle
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e9b1400de76858ca458d6742fba63c967ac6ad74
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---

# <a name="product-dimensions"></a><span data-ttu-id="e5fcb-105">Produktdimensioner</span><span class="sxs-lookup"><span data-stu-id="e5fcb-105">Product dimensions</span></span>

[!include [banner](../includes/banner.md)]

[!include [Retail name](../includes/retail-name.md)]

<span data-ttu-id="e5fcb-106">Der er fire produktdimensioner – farve, konfiguration, størrelse og type.</span><span class="sxs-lookup"><span data-stu-id="e5fcb-106">There are four product dimensions -  Color, Configuration, Size and Style.</span></span> <span data-ttu-id="e5fcb-107">Du kan kombinere produktdimensioner i dimensionsgrupper og tildele dimensionsgrupper til produktmastere.</span><span class="sxs-lookup"><span data-stu-id="e5fcb-107">You combine product dimensions in dimension groups and assign dimension groups to product masters.</span></span> <span data-ttu-id="e5fcb-108">Kombinationerne af produktdimensioner bestemmer, hvordan produktvarianter defineres.</span><span class="sxs-lookup"><span data-stu-id="e5fcb-108">The combinations of product dimensions determine how product variants are defined.</span></span>

<span data-ttu-id="e5fcb-109">Produktdimensioner er egenskaber, der identificerer en produktvariant.</span><span class="sxs-lookup"><span data-stu-id="e5fcb-109">Product dimensions are characteristics that serve to identify a product variant.</span></span> <span data-ttu-id="e5fcb-110">Du kan bruge kombinationer af produktdimensioner til at definere produktvarianter.</span><span class="sxs-lookup"><span data-stu-id="e5fcb-110">You can use combinations of product dimensions to define product variants.</span></span> <span data-ttu-id="e5fcb-111">Du skal definere mindst én produktdimension for en produktmaster for at oprette en produktvariant.</span><span class="sxs-lookup"><span data-stu-id="e5fcb-111">You must define at least one product dimension for a product master in order to create a product variant.</span></span>
<span data-ttu-id="e5fcb-112">Produktvarianter</span><span class="sxs-lookup"><span data-stu-id="e5fcb-112">Product variants</span></span>
----------------

<span data-ttu-id="e5fcb-113">Produktvarianter kaldes også varer.</span><span class="sxs-lookup"><span data-stu-id="e5fcb-113">Product variants are also referred to as items.</span></span> <span data-ttu-id="e5fcb-114">En vare er et fysisk produkt, som ikke er det samme som en tjeneste.</span><span class="sxs-lookup"><span data-stu-id="e5fcb-114">An item is a tangible product, which is not the same as a service.</span></span> <span data-ttu-id="e5fcb-115">Det er også muligt at definere en produktmaster af typen Tjeneste.</span><span class="sxs-lookup"><span data-stu-id="e5fcb-115">It is also possible to define a product master with the Service type.</span></span> <span data-ttu-id="e5fcb-116">Ved hjælp af typen af service kan du angive produktvarianter, der omfatter tjenester.</span><span class="sxs-lookup"><span data-stu-id="e5fcb-116">By using the Service type, you can specify product variants that include services.</span></span> <span data-ttu-id="e5fcb-117">For eksempel kan du angive en produktmaster for konsulentbistand og produktvarianter for arbejde, der udføres af erfarne konsulenter og yngre konsulenter.</span><span class="sxs-lookup"><span data-stu-id="e5fcb-117">For example, you can specify a product master for Consultancy work and product variants for work that is performed by senior consultants and junior consultants.</span></span>

## <a name="product-dimensions"></a><span data-ttu-id="e5fcb-118">Produktdimensioner</span><span class="sxs-lookup"><span data-stu-id="e5fcb-118">Product dimensions</span></span>
<span data-ttu-id="e5fcb-119">Følgende produktdimensioner er tilgængelige: konfiguration, farve, størrelse og type.</span><span class="sxs-lookup"><span data-stu-id="e5fcb-119">The following product dimensions are available: Configuration, Color, Size, and Style.</span></span> <span data-ttu-id="e5fcb-120">En produktvariant kan genereres på basis af produktdimensionsværdierne.</span><span class="sxs-lookup"><span data-stu-id="e5fcb-120">A product variant can be generated based on the product dimension values.</span></span>

<span data-ttu-id="e5fcb-121">Produktets dimensionsværdier, f.eks størrelse, farve og typografi, kan oprettes på siderne **Størrelse**, **Farve** og **Type**, som kan åbnes fra følgende placeringer: **Administration af produktoplysninger** &gt; **Konfiguration** &gt; **Dimensions- og variantgrupper** &gt; **Størrelser/Farver/Typer**.</span><span class="sxs-lookup"><span data-stu-id="e5fcb-121">Product dimensions values such as Size, Color and Style can be created on the **Size**, **Color** and **Style** pages, which can be accessed from the following locations: **Product information management** &gt; **Setup** &gt; **Dimension and variant Groups** &gt; **Sizes/Colors/Styles**.</span></span> <span data-ttu-id="e5fcb-122">Produktets dimensionsværdier for dimensionen Konfiguration oprettes typisk ved hjælp af enten Variantstyring eller Dimensionsbaseret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="e5fcb-122">Product dimension values for the Configuration dimension are typically created using either the Product configurator or the Dimension-based configurator.</span></span> <span data-ttu-id="e5fcb-123">Produktdimensioner kan også oprettes og vedligeholdes på siden **Produktdimensioner**, der kan åbnes fra følgende steder:</span><span class="sxs-lookup"><span data-stu-id="e5fcb-123">Product dimensions can also be created and maintained on the **Product dimensions** page, which can be accessed from the following locations:</span></span>
-   <span data-ttu-id="e5fcb-124">Klik på **Administration af produktoplysninger** &gt; **Produkter** &gt; **Produktmastere**.</span><span class="sxs-lookup"><span data-stu-id="e5fcb-124">Click **Product information management** &gt; **Products** &gt; **Product masters**.</span></span> <span data-ttu-id="e5fcb-125">Klik på **Produktdimensioner** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="e5fcb-125">On the **Action Pane**, click **Product dimensions**.</span></span>
-   <span data-ttu-id="e5fcb-126">Klik på **Administration af produktoplysninger** &gt; **Produkter** &gt; **Alle produkter og produktmastere**.</span><span class="sxs-lookup"><span data-stu-id="e5fcb-126">Click **Product information management** &gt; **Products** &gt; **All products and product masters**.</span></span> <span data-ttu-id="e5fcb-127">Vælg en produktmaster.</span><span class="sxs-lookup"><span data-stu-id="e5fcb-127">Select a product master.</span></span> <span data-ttu-id="e5fcb-128">Klik på **Produktdimensioner** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="e5fcb-128">On the **Action Pane**, click **Product dimensions**.</span></span>
-   <span data-ttu-id="e5fcb-129">Klik på **Administration af produktoplysninger** &gt; **Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="e5fcb-129">Click **Product information management** &gt; **Released products**.</span></span> <span data-ttu-id="e5fcb-130">Vælg en produktmaster.</span><span class="sxs-lookup"><span data-stu-id="e5fcb-130">Select a product master.</span></span> <span data-ttu-id="e5fcb-131">Klik på **Produkt** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="e5fcb-131">On the **Action Pane**, click **Product**.</span></span> <span data-ttu-id="e5fcb-132">Klik på **Produktdimensioner** i gruppen **Produktmaster**.</span><span class="sxs-lookup"><span data-stu-id="e5fcb-132">In the **Product master** group, click **Product dimensions**.</span></span>

<span data-ttu-id="e5fcb-133">Antallet af varianter, der kan oprettes for en vare, er begrænset af antallet af mulige kombinationer af produktdimensioner.</span><span class="sxs-lookup"><span data-stu-id="e5fcb-133">The number of variants that you can create for an item is limited by the number of possible product dimension combinations.</span></span>

| <span data-ttu-id="e5fcb-134">**Tip!**</span><span class="sxs-lookup"><span data-stu-id="e5fcb-134">**Tip**</span></span>                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5fcb-135">Når du bruger et produkt på for eksempel en ordrelinje, skal du vælge produktdimensioner for at identificere den produktvariant, som du vil arbejde med.</span><span class="sxs-lookup"><span data-stu-id="e5fcb-135">When you use a product on, for example, an order line, you select the product dimensions to identify the product variant that you want to work with.</span></span> |

## <a name="example"></a><span data-ttu-id="e5fcb-136">Eksempel</span><span class="sxs-lookup"><span data-stu-id="e5fcb-136">Example</span></span>
<span data-ttu-id="e5fcb-137">Et firma sælger denimbukser.</span><span class="sxs-lookup"><span data-stu-id="e5fcb-137">A company sells denim jeans.</span></span> <span data-ttu-id="e5fcb-138">Til varen cowboybukser bruges produktdimensionerne farve og størrelse.</span><span class="sxs-lookup"><span data-stu-id="e5fcb-138">The item, Jeans, uses the Color and Size product dimensions.</span></span> <span data-ttu-id="e5fcb-139">Cowboybukserne sælges i tre forskellige farver og seks forskellige størrelser.</span><span class="sxs-lookup"><span data-stu-id="e5fcb-139">The jeans are sold in three different colors and six different sizes.</span></span> <span data-ttu-id="e5fcb-140">Farver: blå, sort, brun Størrelser: XS, S, M, L, XL, XXL ikke alle størrelser er tilgængelige i alle tre farver.</span><span class="sxs-lookup"><span data-stu-id="e5fcb-140">Colors: Blue, Black, Brown Sizes: XS, S, M, L, XL, XXL Not all sizes are available in all the three colors.</span></span> <span data-ttu-id="e5fcb-141">Hvis alle kombinationer var tilgængelige, ville det skabe 18 forskellige typer af cowboybukser.</span><span class="sxs-lookup"><span data-stu-id="e5fcb-141">If all combinations were available, it would create 18 different types of jeans.</span></span> <span data-ttu-id="e5fcb-142">I dette eksempel produceres kun følgende ni kombinationer af produktvarianter.</span><span class="sxs-lookup"><span data-stu-id="e5fcb-142">In this example, only the following nine product variant combinations are produced.</span></span>

| <span data-ttu-id="e5fcb-143">Farve</span><span class="sxs-lookup"><span data-stu-id="e5fcb-143">Color</span></span> | <span data-ttu-id="e5fcb-144">Størrelse</span><span class="sxs-lookup"><span data-stu-id="e5fcb-144">Size</span></span> |
|-------|------|
| <span data-ttu-id="e5fcb-145">Blå</span><span class="sxs-lookup"><span data-stu-id="e5fcb-145">Blue</span></span>  | <span data-ttu-id="e5fcb-146">XS</span><span class="sxs-lookup"><span data-stu-id="e5fcb-146">XS</span></span>   |
| <span data-ttu-id="e5fcb-147">Blå</span><span class="sxs-lookup"><span data-stu-id="e5fcb-147">Blue</span></span>  | <span data-ttu-id="e5fcb-148">L</span><span class="sxs-lookup"><span data-stu-id="e5fcb-148">S</span></span>    |
| <span data-ttu-id="e5fcb-149">Blå</span><span class="sxs-lookup"><span data-stu-id="e5fcb-149">Blue</span></span>  | <span data-ttu-id="e5fcb-150">M</span><span class="sxs-lookup"><span data-stu-id="e5fcb-150">M</span></span>    |
| <span data-ttu-id="e5fcb-151">Sort</span><span class="sxs-lookup"><span data-stu-id="e5fcb-151">Black</span></span> | <span data-ttu-id="e5fcb-152">M</span><span class="sxs-lookup"><span data-stu-id="e5fcb-152">M</span></span>    |
| <span data-ttu-id="e5fcb-153">Sort</span><span class="sxs-lookup"><span data-stu-id="e5fcb-153">Black</span></span> | <span data-ttu-id="e5fcb-154">L</span><span class="sxs-lookup"><span data-stu-id="e5fcb-154">L</span></span>    |
| <span data-ttu-id="e5fcb-155">Sort</span><span class="sxs-lookup"><span data-stu-id="e5fcb-155">Black</span></span> | <span data-ttu-id="e5fcb-156">XL</span><span class="sxs-lookup"><span data-stu-id="e5fcb-156">XL</span></span>   |
| <span data-ttu-id="e5fcb-157">Brun</span><span class="sxs-lookup"><span data-stu-id="e5fcb-157">Brown</span></span> | <span data-ttu-id="e5fcb-158">L</span><span class="sxs-lookup"><span data-stu-id="e5fcb-158">L</span></span>    |
| <span data-ttu-id="e5fcb-159">Brun</span><span class="sxs-lookup"><span data-stu-id="e5fcb-159">Brown</span></span> | <span data-ttu-id="e5fcb-160">XL</span><span class="sxs-lookup"><span data-stu-id="e5fcb-160">XL</span></span>   |
| <span data-ttu-id="e5fcb-161">Brun</span><span class="sxs-lookup"><span data-stu-id="e5fcb-161">Brown</span></span> | <span data-ttu-id="e5fcb-162">XXL</span><span class="sxs-lookup"><span data-stu-id="e5fcb-162">XXL</span></span>  |






