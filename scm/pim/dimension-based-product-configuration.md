---
title: Dimensionsbaseret produktkonfiguration
description: "Dimensionsbaseret produktkonfiguration repræsenterer en enkel løsning til at oprette mange produktvarianter fra en enkelt produktmaster og tilhørende stykliste."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConfigRule, BOMTable, ConfigChooseFromRoute, ConfigGroup, ConfigHierarchy, EcoResDimensionBasedConfiguration
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19821
ms.assetid: 4db9890b-306b-4be7-ba98-3be2094d561f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 89f01401f1d937a72ae7e59b784cf034b48aaf1f
ms.contentlocale: da-dk
ms.lasthandoff: 07/18/2017

---

# <a name="dimension-based-product-configuration"></a><span data-ttu-id="0e140-103">Dimensionsbaseret produktkonfiguration</span><span class="sxs-lookup"><span data-stu-id="0e140-103">Dimension-based product configuration</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="0e140-104">Dimensionsbaseret produktkonfiguration repræsenterer en enkel løsning til at oprette mange produktvarianter fra en enkelt produktmaster og tilhørende stykliste.</span><span class="sxs-lookup"><span data-stu-id="0e140-104">Dimension-based product configuration represents a simple solution for creating many product variants from a single product master and its bill of materials.</span></span>

<span data-ttu-id="0e140-105">Dimensionsbaseret produktkonfiguration er en af de tre indbyggede teknologier til produktkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="0e140-105">Dimension-based product configuration is one of the three built-in product configuration technologies.</span></span> <span data-ttu-id="0e140-106">De to andre teknologier er foruddefinerede varianter og begrænsningsbaseret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="0e140-106">The two other technologies are predefined variants and constraint-based configuration.</span></span> <span data-ttu-id="0e140-107">Alle tre teknologier bruger en produktmaster som udgangspunkt og tillader brugeren at oprette mange produktvarianter for en produktmaster.</span><span class="sxs-lookup"><span data-stu-id="0e140-107">All three technologies use a product master as the starting point and allow the user to create many product variants for one product master.</span></span>

## <a name="key-concepts"></a><span data-ttu-id="0e140-108">Nøglebegreber</span><span class="sxs-lookup"><span data-stu-id="0e140-108">Key concepts</span></span>
<span data-ttu-id="0e140-109">Dimensionsbaseret produktkonfiguration er baseret på følgende nøglebegreber:</span><span class="sxs-lookup"><span data-stu-id="0e140-109">Dimension-based product configuration is based on the following key concepts:</span></span>

-   <span data-ttu-id="0e140-110">Produktmastere</span><span class="sxs-lookup"><span data-stu-id="0e140-110">Product masters</span></span>
-   <span data-ttu-id="0e140-111">Konfiguration af produktdimension</span><span class="sxs-lookup"><span data-stu-id="0e140-111">Configuration product dimension</span></span>
-   <span data-ttu-id="0e140-112">Variantgrupper</span><span class="sxs-lookup"><span data-stu-id="0e140-112">Configuration groups</span></span>
-   <span data-ttu-id="0e140-113">Stykliste</span><span class="sxs-lookup"><span data-stu-id="0e140-113">Bill of materials (BOM)</span></span>
-   <span data-ttu-id="0e140-114">Konfigurationsrute</span><span class="sxs-lookup"><span data-stu-id="0e140-114">Configuration route</span></span>
-   <span data-ttu-id="0e140-115">Variantregler</span><span class="sxs-lookup"><span data-stu-id="0e140-115">Configuration rules</span></span>

### <a name="product-masters"></a><span data-ttu-id="0e140-116">Produktmastere</span><span class="sxs-lookup"><span data-stu-id="0e140-116">Product masters</span></span>

<span data-ttu-id="0e140-117">En produktmaster er udgangspunktet for enhver proces til produktkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="0e140-117">A product master is the starting point for any product configuration process.</span></span> <span data-ttu-id="0e140-118">Til den dimensionsbaserede produktkonfiguration skal du bruge en produktmaster med denne bestemte konfigurationsteknologi og en produktdimensionsgruppe, der omfatter konfigurationens produktdimension.</span><span class="sxs-lookup"><span data-stu-id="0e140-118">For the dimension-based product configuration, you need a product master with this particular configuration technology and a product dimension group that includes the configuration product dimension.</span></span>

### <a name="configuration-product-dimension"></a><span data-ttu-id="0e140-119">Konfiguration af produktdimension</span><span class="sxs-lookup"><span data-stu-id="0e140-119">Configuration product dimension</span></span>

<span data-ttu-id="0e140-120">Konfigurationens produktdimension bruges til at identificere produktvarianter for en produktmaster med den dimensionsbaserede konfigurationsteknologi.</span><span class="sxs-lookup"><span data-stu-id="0e140-120">The configuration product dimension is used to identify the product variants for a product master with the dimension-based configuration technology.</span></span> <span data-ttu-id="0e140-121">Konfigurationens dimensionsværdi er angivet af brugeren og skal hjælpe med at identificere de enkelte produktvarianter.</span><span class="sxs-lookup"><span data-stu-id="0e140-121">The configuration dimension value is entered by the user and should help to identify the individual product variants.</span></span>

### <a name="configuration-groups"></a><span data-ttu-id="0e140-122">Variantgrupper</span><span class="sxs-lookup"><span data-stu-id="0e140-122">Configuration groups</span></span>

<span data-ttu-id="0e140-123">Variantgrupper er defineret i et centralt lager og kan bruges til alle dimensionsbaserede produktkonfigurationsmodeller.</span><span class="sxs-lookup"><span data-stu-id="0e140-123">Configuration groups are defined in a central repository and can be used for all dimension-based product configuration models.</span></span> <span data-ttu-id="0e140-124">Variantgrupper er knyttet til de enkelte styklistelinjer og holder en gruppe af linjer sammen, der gensidigt udelukker hinanden.</span><span class="sxs-lookup"><span data-stu-id="0e140-124">Configuration groups are associated to the individual BOM lines and hold together a group of lines that are mutually exclusive.</span></span> <span data-ttu-id="0e140-125">Det betyder, at kun én linje i en gruppe kan vælges til en enkelt produktvariant.</span><span class="sxs-lookup"><span data-stu-id="0e140-125">This means that only one line in a group can be selected for a single product variant.</span></span>

### <a name="bill-of-materials-bom"></a><span data-ttu-id="0e140-126">Stykliste</span><span class="sxs-lookup"><span data-stu-id="0e140-126">Bill of materials (BOM)</span></span>

<span data-ttu-id="0e140-127">Styklisten repræsenterer byggesten for en dimensionsbaseret produktkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="0e140-127">The BOM represent the building blocks for a dimension-based product configuration.</span></span> <span data-ttu-id="0e140-128">Den skal indeholde alle de forskellige produkter, der kan bruges i en produktvariant.</span><span class="sxs-lookup"><span data-stu-id="0e140-128">It must include all the different products that can be used in any product variant.</span></span> <span data-ttu-id="0e140-129">Hver linje i styklisten kan henvise til en variantgruppe.</span><span class="sxs-lookup"><span data-stu-id="0e140-129">Each line in the BOM can reference a configuration group.</span></span> <span data-ttu-id="0e140-130">Hvis en linje ikke refererer til en variantgruppe, medtages den i alle produktvarianter.</span><span class="sxs-lookup"><span data-stu-id="0e140-130">If a line doesn’t reference a configuration group, it will be included in all product variants.</span></span>

### <a name="configuration-route"></a><span data-ttu-id="0e140-131">Konfigurationsrute</span><span class="sxs-lookup"><span data-stu-id="0e140-131">Configuration route</span></span>

<span data-ttu-id="0e140-132">Variantruten bestemmer rækkefølgen af variantgrupper, da de vil blive vist for brugeren under processen til produktkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="0e140-132">The configuration route determines the sequence of the configuration groups, as they will be displayed to the user during the product configuration process.</span></span>

### <a name="configuration-rules"></a><span data-ttu-id="0e140-133">Variantregler</span><span class="sxs-lookup"><span data-stu-id="0e140-133">Configuration rules</span></span>

<span data-ttu-id="0e140-134">Variantregler repræsenterer en mekanisme til at sikre, at et produkt, der er medtaget i en variantgruppe på en stykliste, gennemtvinger enten en medtagelse eller en udelukkelse af et produkt i en anden variantgruppe på samme stykliste.</span><span class="sxs-lookup"><span data-stu-id="0e140-134">The configuration rules represent a mechanism for ensuring that a product included in one configuration group in a BOM enforces either an inclusion or an exclusion of a product in a different configuration group in the same BOM.</span></span>

## <a name="product-modeling-process"></a><span data-ttu-id="0e140-135">Proces til produktmodel</span><span class="sxs-lookup"><span data-stu-id="0e140-135">Product modeling process</span></span>
<span data-ttu-id="0e140-136">Den naturlige sekvens til opbygning af en produktmodel for et dimensionsbaseret produkt, starter med at definere de relevante variantgrupper.</span><span class="sxs-lookup"><span data-stu-id="0e140-136">The natural sequence for building a product model for a dimension-based product starts with defining the relevant configuration groups.</span></span> <span data-ttu-id="0e140-137">Det er vigtigt at sikre, at alle produkter, der skal bruges i styklisten, er blevet frigivet til den virksomhed, som produktmodellen er bygget til.</span><span class="sxs-lookup"><span data-stu-id="0e140-137">It is important to ensure that all products which will be used in the BOM have been relased to the company that the product model is built for.</span></span> <span data-ttu-id="0e140-138">Med disse byggeklodser på plads kan brugeren oprette styklisten og tildele variantgrupper til alle relevante styklistelinjer.</span><span class="sxs-lookup"><span data-stu-id="0e140-138">With these building blocks in place, the user can create the BOM and assign configuration groups to all relevant BOM lines.</span></span> <span data-ttu-id="0e140-139">Når styklisten er fuldført, kan du definere en variantrute for rækkefølgen af variantgrupper i den rigtige rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="0e140-139">When the BOM is complete, a configuration route can be defined for ordering the configuration groups in the proper sequence.</span></span> <span data-ttu-id="0e140-140">\[caption id="attachment\_282671" align="alignnone" width="1187"\][![Proces til dimensionsbaseret produktmodel](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) Proces til dimensionsbaseret produktmodel\[/caption\] Hvis der er visse produkter fra forskellige variantgrupper, der enten skal eller ikke skal bruges sammen, kan du oprette variantregler, der gennemtvinger disse produktrelationer..</span><span class="sxs-lookup"><span data-stu-id="0e140-140">\[caption id="attachment\_282671" align="alignnone" width="1187"\][![Dimension-based product modeling process](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) Dimension-based product modeling process\[/caption\] If there are certain products from different configuration groups that either must or must not be used together, you can create configuration rules that will enforce these product relationships.</span></span> <span data-ttu-id="0e140-141">Når styklisten er blevet knyttet sammen med en dimensionsbaseret produktmaster via en styklisteversion, og begge er blevet godkendt og er aktiveret, kan du oprette produktkonfigurationer og angiv et navn for hver konfiguration.</span><span class="sxs-lookup"><span data-stu-id="0e140-141">After the BOM has been tied together with a dimension-based product master through a BOM version and both have been approved and activated, you can create product configurations and enter a name for each configuration.</span></span> <span data-ttu-id="0e140-142">Konfigurationerne kan defineres, før der genereres posteringer, eller det kan gøres, når der opstår behov for en bestemt konfiguration.</span><span class="sxs-lookup"><span data-stu-id="0e140-142">The configurations can be defined before any transactions are generated or it can be done when the need for a certain configuration occurs.</span></span>

### <a name="suggested-use"></a><span data-ttu-id="0e140-143">Foreslået anvendelse</span><span class="sxs-lookup"><span data-stu-id="0e140-143">Suggested use</span></span>

<span data-ttu-id="0e140-144">Den dimensionsbaserede konfigurationsteknologi er bedst anvendt til produkter med begrænset variation, og kombinationen af størrelse på standardproduktdimension, farve, typografi og konfiguration egner sig ikke til at identificere en bestemt produktvariant.</span><span class="sxs-lookup"><span data-stu-id="0e140-144">The dimension-based configuration technology is best used for products with limited variability and the combination of the standard product dimensions size, color, style, and configuration is unsuitable for identifying a specific product variant.</span></span> <span data-ttu-id="0e140-145">Et eksempel kunne være cykler med stelhøjde, hjulstørrelse, bremsetyper og forskellige gear.</span><span class="sxs-lookup"><span data-stu-id="0e140-145">An example could be bicycle with frame height, wheel size, brake types, and different gears.</span></span>




