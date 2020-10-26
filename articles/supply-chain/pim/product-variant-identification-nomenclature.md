---
title: Nomenklatur for produktvariantnumre og -navne
description: Dette emne beskriver, hvordan du kan konfigurere en nomenklatur for produktnumre til erstatning for det faste [produktmasternummer - konfiguration - størrelse - farve - type] format.
author: roxanadiaconu
manager: tfehr
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 220104
ms.assetid: 3fe69fb7-5c32-423c-98a8-2f53186cda68
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 90c01e4281246d890ef888c56ca137f83e83741c
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2020
ms.locfileid: "3980477"
---
# <a name="nomenclature-of-product-variant-numbers-and-names"></a><span data-ttu-id="5ec35-103">Nomenklatur for produktvariantnumre og -navne</span><span class="sxs-lookup"><span data-stu-id="5ec35-103">Nomenclature of product variant numbers and names</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5ec35-104">Dette emne beskriver, hvordan du kan konfigurere en nomenklatur for produktnumre til erstatning for det faste [produktmasternummer - konfiguration - størrelse - farve - type] format.</span><span class="sxs-lookup"><span data-stu-id="5ec35-104">This topic describes how you can set up a product number nomenclature to replace the fixed [Product master number - Configuration - Size - Color - Style] format.</span></span> <span data-ttu-id="5ec35-105">Den nye nomenklatur har et målrettet format, der omfatter produktmasternummer, aktive produktdimensioner og tekstafgrænsningstegn efter eget valg.</span><span class="sxs-lookup"><span data-stu-id="5ec35-105">The new nomenclature has a targeted format that includes the product master number, active product dimensions, and text delimiters of your choice.</span></span> <span data-ttu-id="5ec35-106">Du kan også oprette en nomenklatur for produktnavne.</span><span class="sxs-lookup"><span data-stu-id="5ec35-106">You can also create a nomenclature for product names.</span></span> <span data-ttu-id="5ec35-107">Endelig kan du også oprette en nomenklatur til at identificere konfigurationer, der er oprettet af den begrænsningsbaserede produktkonfigurator.</span><span class="sxs-lookup"><span data-stu-id="5ec35-107">Finally, you can build a nomenclature to identify configurations that are created by the constraint-based product configurator.</span></span> <span data-ttu-id="5ec35-108">Disse nomenklaturer kan indeholde attributter efter eget valg.</span><span class="sxs-lookup"><span data-stu-id="5ec35-108">These nomenclatures can contain attributes of your choice.</span></span>

<span data-ttu-id="5ec35-109">De nye nomenklaturer for produktvariantnumre og produktvariantnavne giver dig mulighed for at medtage segmenter i id'erne for produktvarianter.</span><span class="sxs-lookup"><span data-stu-id="5ec35-109">The new nomenclatures for product variant numbers and product variant names let you include segments in the identifiers for product variants.</span></span> <span data-ttu-id="5ec35-110">Disse segmenter kan indeholde produktmasternummer og -navn, produktdimensions-id'er og -navne, nummerserier, tekstkonstanter og attributter.</span><span class="sxs-lookup"><span data-stu-id="5ec35-110">These segments can include the product master number and name, product dimension IDs and names, number sequences, text constants, and attributes.</span></span> <span data-ttu-id="5ec35-111">Med denne funktion kan du hurtigt finde en bestemt produktvariant, når du opretter en salgsordre eller en indkøbsordre.</span><span class="sxs-lookup"><span data-stu-id="5ec35-111">This functionality lets you quickly find a specific product variant when you create a sales order or a purchase order.</span></span> <span data-ttu-id="5ec35-112">Du opretter nomenklaturer til både produktvariantnumre og produktvariantnavne ved hjælp af siden **Produktnomenklatur**.</span><span class="sxs-lookup"><span data-stu-id="5ec35-112">You create nomenclatures for both product variant numbers and product variant names by using the **Product nomenclature** page.</span></span> <span data-ttu-id="5ec35-113">Klik på **Administration af produktoplysninger** &gt; **Konfiguration** for at åbne denne side.</span><span class="sxs-lookup"><span data-stu-id="5ec35-113">To open this page, click **Product information management** &gt; **Setup**.</span></span>

## <a name="nomenclature-of-predefined-product-variants"></a><span data-ttu-id="5ec35-114">Nomenklatur for foruddefinerede produktvarianter</span><span class="sxs-lookup"><span data-stu-id="5ec35-114">Nomenclature of predefined product variants</span></span>
<span data-ttu-id="5ec35-115">Der oprettes produktvarianter for produktmastere efter en af de tre konfigurationsteknologier:</span><span class="sxs-lookup"><span data-stu-id="5ec35-115">Product variants are generated for product masters according to one of three configuration technologies:</span></span>

-   <span data-ttu-id="5ec35-116">Foruddefinerede varianter</span><span class="sxs-lookup"><span data-stu-id="5ec35-116">Predefined variants</span></span>
-   <span data-ttu-id="5ec35-117">Begrænsningsbaseret</span><span class="sxs-lookup"><span data-stu-id="5ec35-117">Constraint-based</span></span>
-   <span data-ttu-id="5ec35-118">Dimensionsbaseret</span><span class="sxs-lookup"><span data-stu-id="5ec35-118">Dimension-based</span></span>

<span data-ttu-id="5ec35-119">Hver produktvariant har et nummer og et navn, og nomenklaturerne for produktvariantidentifikation giver dig mulighed for at vælge de segmenter, der skal medtages i hvert produktvariantnummer eller -navn.</span><span class="sxs-lookup"><span data-stu-id="5ec35-119">Each product variant has a number and a name, and the product variant identification nomenclatures let you select the segments that will be included in each product variant number or name.</span></span> <span data-ttu-id="5ec35-120">Du kan vælge følgende segmenter på siden **Produktnomenklatur**:</span><span class="sxs-lookup"><span data-stu-id="5ec35-120">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="5ec35-121">Produktmasternummer</span><span class="sxs-lookup"><span data-stu-id="5ec35-121">Product master number</span></span>
-   <span data-ttu-id="5ec35-122">Produktmasternavn</span><span class="sxs-lookup"><span data-stu-id="5ec35-122">Product master name</span></span>
-   <span data-ttu-id="5ec35-123">Nummerserieværdi</span><span class="sxs-lookup"><span data-stu-id="5ec35-123">Number sequence value</span></span>
-   <span data-ttu-id="5ec35-124">Tekstkonstant</span><span class="sxs-lookup"><span data-stu-id="5ec35-124">Text constant</span></span>
-   <span data-ttu-id="5ec35-125">Produktdimensioner</span><span class="sxs-lookup"><span data-stu-id="5ec35-125">Product dimensions</span></span>
    -   <span data-ttu-id="5ec35-126">Konfigurations-id eller -navn</span><span class="sxs-lookup"><span data-stu-id="5ec35-126">Configuration ID or name</span></span>
    -   <span data-ttu-id="5ec35-127">Farve-id eller -navn</span><span class="sxs-lookup"><span data-stu-id="5ec35-127">Color ID or name</span></span>
    -   <span data-ttu-id="5ec35-128">Størrelses-id eller -navn</span><span class="sxs-lookup"><span data-stu-id="5ec35-128">Size ID or name</span></span>
    -   <span data-ttu-id="5ec35-129">Type-id eller -navn</span><span class="sxs-lookup"><span data-stu-id="5ec35-129">Style ID or name</span></span>

<span data-ttu-id="5ec35-130">Når du har defineret en nomenklatur for produktvariantidentifikationsnummer, kan du knytte den til en produktdimensionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="5ec35-130">After you define a product variant identification number nomenclature, you can associate it with a product dimension group.</span></span> <span data-ttu-id="5ec35-131">Alle de produktmastere, der refererer til denne produktdimensionsgruppe, vil derfor blive tildelt produktvariantnumre efter nomenklaturen.</span><span class="sxs-lookup"><span data-stu-id="5ec35-131">All product masters that reference this product dimension group will then be assigned product variant numbers according to the nomenclature.</span></span> <span data-ttu-id="5ec35-132">Men nomenklaturer for produktvariantnavn kan dog ikke knyttes til produktdimensionsgrupper.</span><span class="sxs-lookup"><span data-stu-id="5ec35-132">However, product variant name nomenclatures can't be associated with product dimension groups.</span></span> <span data-ttu-id="5ec35-133">Du kan også tildele en nomenklatur for produktvariantidentifikation direkte til en produktmaster.</span><span class="sxs-lookup"><span data-stu-id="5ec35-133">You can also assign a product variant identification nomenclature directly to a product master.</span></span> <span data-ttu-id="5ec35-134">I dette tilfælde tildeles de produktvarianter, der hører til produktmasteren, produktvariantnumre og -navne i overensstemmelse med nomenklaturerne.</span><span class="sxs-lookup"><span data-stu-id="5ec35-134">In this case, the product variants that belong to the product master will be assigned product variant numbers and names according to the nomenclatures.</span></span>

### <a name="example"></a><span data-ttu-id="5ec35-135">Eksempel</span><span class="sxs-lookup"><span data-stu-id="5ec35-135">Example</span></span>

<span data-ttu-id="5ec35-136">En T-shirt (TS1234), der produceres i tre størrelser (S, M, L), fire farver (rød, grøn, blå, gul) og to typer (Polo, V).</span><span class="sxs-lookup"><span data-stu-id="5ec35-136">A T-shirt (TS1234) is produced in three sizes (S, M, L), four colors (Red, Green, Blue, Yellow), and two styles (Polo, V).</span></span> <span data-ttu-id="5ec35-137">Derfor er der 24 mulige produktvarianter (= 3 × 4 × 2).</span><span class="sxs-lookup"><span data-stu-id="5ec35-137">Therefore, 24 product variants are possible (= 3 × 4 × 2).</span></span> <span data-ttu-id="5ec35-138">Du opretter en nomenklatur for produktvariantnumre, der har følgende segmenter:</span><span class="sxs-lookup"><span data-stu-id="5ec35-138">You create a product variant number nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="5ec35-139">Produktmasternummer</span><span class="sxs-lookup"><span data-stu-id="5ec35-139">Product master number</span></span>
2.  <span data-ttu-id="5ec35-140">Tekstkonstant: "-"</span><span class="sxs-lookup"><span data-stu-id="5ec35-140">Text constant: "-"</span></span>
3.  <span data-ttu-id="5ec35-141">Farve</span><span class="sxs-lookup"><span data-stu-id="5ec35-141">Color</span></span>
4.  <span data-ttu-id="5ec35-142">Tekstkonstant: "-"</span><span class="sxs-lookup"><span data-stu-id="5ec35-142">Text constant: "-"</span></span>
5.  <span data-ttu-id="5ec35-143">Størrelse</span><span class="sxs-lookup"><span data-stu-id="5ec35-143">Size</span></span>
6.  <span data-ttu-id="5ec35-144">Tekstkonstant: "-"</span><span class="sxs-lookup"><span data-stu-id="5ec35-144">Text constant: "-"</span></span>
7.  <span data-ttu-id="5ec35-145">Type</span><span class="sxs-lookup"><span data-stu-id="5ec35-145">Style</span></span>

<span data-ttu-id="5ec35-146">I dette tilfælde vil produktvariantnummeret for en rød, small, polo T-shirt være TS1234-Rød-Small-Polo.</span><span class="sxs-lookup"><span data-stu-id="5ec35-146">In this case, the product variant number for a red, small, polo T-shirt will be TS1234-Red-Small-Polo.</span></span>

## <a name="nomenclature-of-constraint-based-configurations"></a><span data-ttu-id="5ec35-147">Nomenklatur for begrænsningsbaserede konfigurationer</span><span class="sxs-lookup"><span data-stu-id="5ec35-147">Nomenclature of constraint-based configurations</span></span>
<span data-ttu-id="5ec35-148">Til begrænsningsbaserede konfigurationer kan du oprette en dedikeret nomenklatur til konfigurationsproduktdimensionen.</span><span class="sxs-lookup"><span data-stu-id="5ec35-148">For constraint-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="5ec35-149">Du kan vælge følgende segmenter på siden **Produktnomenklatur**:</span><span class="sxs-lookup"><span data-stu-id="5ec35-149">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="5ec35-150">Nummerserieværdi</span><span class="sxs-lookup"><span data-stu-id="5ec35-150">Number sequence value</span></span>
-   <span data-ttu-id="5ec35-151">Tekstkonstant</span><span class="sxs-lookup"><span data-stu-id="5ec35-151">Text constant</span></span>
-   <span data-ttu-id="5ec35-152">Attributværdi</span><span class="sxs-lookup"><span data-stu-id="5ec35-152">Attribute value</span></span>

<span data-ttu-id="5ec35-153">Hver komponent i en produktkonfigurationsmodel kan have sin egen konfigurationsnomenklatur.</span><span class="sxs-lookup"><span data-stu-id="5ec35-153">Each component in a product configuration model can have its own configuration nomenclature.</span></span> <span data-ttu-id="5ec35-154">Kun de attributter, der tilhører komponenten, kan anvendes.</span><span class="sxs-lookup"><span data-stu-id="5ec35-154">Only attributes that belong to the component can be used.</span></span> <span data-ttu-id="5ec35-155">Attributter fra underkomponenter eller brugerkrav kan ikke anvendes.</span><span class="sxs-lookup"><span data-stu-id="5ec35-155">Attributes from subcomponents or user requirements can't be used.</span></span>

### <a name="example"></a><span data-ttu-id="5ec35-156">Eksempel</span><span class="sxs-lookup"><span data-stu-id="5ec35-156">Example</span></span>

<span data-ttu-id="5ec35-157">En produktkonfigurationsmodel har en rodkomponent, der har to attributter:</span><span class="sxs-lookup"><span data-stu-id="5ec35-157">A product configuration model has a root component that has two attributes:</span></span>

-   <span data-ttu-id="5ec35-158">Materiale (plast, træ, stål)</span><span class="sxs-lookup"><span data-stu-id="5ec35-158">Material (Plastic, Wood, Steel)</span></span>
-   <span data-ttu-id="5ec35-159">Længde (10... 100)</span><span class="sxs-lookup"><span data-stu-id="5ec35-159">Length (10...100)</span></span>

<span data-ttu-id="5ec35-160">Du opretter en konfigurationsnomenklatur, der har følgende segmenter:</span><span class="sxs-lookup"><span data-stu-id="5ec35-160">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="5ec35-161">Attributværdi: Materiale</span><span class="sxs-lookup"><span data-stu-id="5ec35-161">Attribute value: Material</span></span>
2.  <span data-ttu-id="5ec35-162">Tekstkonstant: "AAA"</span><span class="sxs-lookup"><span data-stu-id="5ec35-162">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="5ec35-163">Attributværdi: Længde</span><span class="sxs-lookup"><span data-stu-id="5ec35-163">Attribute value: Length</span></span>

<span data-ttu-id="5ec35-164">I dette tilfælde vil konfigurations-id'et for træmateriale, der har en længde på 78, være WoodAAA78.</span><span class="sxs-lookup"><span data-stu-id="5ec35-164">In this case, the configuration ID for wood material that has a length of 78 will be WoodAAA78.</span></span>

## <a name="nomenclature-of-dimension-based-configurations"></a><span data-ttu-id="5ec35-165">Nomenklatur for dimensionsbaserede konfigurationer</span><span class="sxs-lookup"><span data-stu-id="5ec35-165">Nomenclature of dimension-based configurations</span></span>
<span data-ttu-id="5ec35-166">Til dimensionsbaserede konfigurationer kan du oprette en dedikeret nomenklatur til konfigurationsproduktdimensionen.</span><span class="sxs-lookup"><span data-stu-id="5ec35-166">For dimension-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="5ec35-167">Du kan vælge følgende segmenter på siden **Produktnomenklatur**:</span><span class="sxs-lookup"><span data-stu-id="5ec35-167">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="5ec35-168">Nummerserieværdi</span><span class="sxs-lookup"><span data-stu-id="5ec35-168">Number sequence value</span></span>
-   <span data-ttu-id="5ec35-169">Tekstkonstant</span><span class="sxs-lookup"><span data-stu-id="5ec35-169">Text constant</span></span>
-   <span data-ttu-id="5ec35-170">Vare i konfigurationsgruppe</span><span class="sxs-lookup"><span data-stu-id="5ec35-170">Configuration group item</span></span>

<span data-ttu-id="5ec35-171">Du kan definere en konfigurationsnomenklatur for en stykliste.</span><span class="sxs-lookup"><span data-stu-id="5ec35-171">You can define a configuration nomenclature for a bill of materials (BOM).</span></span>

### <a name="example"></a><span data-ttu-id="5ec35-172">Eksempel</span><span class="sxs-lookup"><span data-stu-id="5ec35-172">Example</span></span>

<span data-ttu-id="5ec35-173">En stykliste indeholder fire styklistelinjer, der er opdelt i to konfigurationsgrupper:</span><span class="sxs-lookup"><span data-stu-id="5ec35-173">A BOM has four BOM lines that are divided into two configuration groups:</span></span>

-   <span data-ttu-id="5ec35-174">Styklistelinje: M0007, Standardkabinet</span><span class="sxs-lookup"><span data-stu-id="5ec35-174">BOM line: M0007, Standard cabinet</span></span>
    -   <span data-ttu-id="5ec35-175">Variantgruppe: Kabinet</span><span class="sxs-lookup"><span data-stu-id="5ec35-175">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="5ec35-176">Styklistelinje: M0008, Kabinet af topkvalitet</span><span class="sxs-lookup"><span data-stu-id="5ec35-176">BOM line: M0008, High end cabinet</span></span>
    -   <span data-ttu-id="5ec35-177">Variantgruppe: Kabinet</span><span class="sxs-lookup"><span data-stu-id="5ec35-177">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="5ec35-178">Styklistelinje: M0021, Forgitter af stof</span><span class="sxs-lookup"><span data-stu-id="5ec35-178">BOM line: M0021, Front grill cloth</span></span>
    -   <span data-ttu-id="5ec35-179">Variantgruppe: Forgitter</span><span class="sxs-lookup"><span data-stu-id="5ec35-179">Configuration group: Front grill</span></span>
-   <span data-ttu-id="5ec35-180">Styklistelinje: M0022, Forgitter af metal</span><span class="sxs-lookup"><span data-stu-id="5ec35-180">BOM line: M0022, Front grill metal</span></span>
    -   <span data-ttu-id="5ec35-181">Variantgruppe: Forgitter</span><span class="sxs-lookup"><span data-stu-id="5ec35-181">Configuration group: Front grill</span></span>

<span data-ttu-id="5ec35-182">Du opretter en konfigurationsnomenklatur, der har følgende segmenter:</span><span class="sxs-lookup"><span data-stu-id="5ec35-182">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="5ec35-183">Variantgruppe: Kabinet</span><span class="sxs-lookup"><span data-stu-id="5ec35-183">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="5ec35-184">Tekstkonstant: "&"</span><span class="sxs-lookup"><span data-stu-id="5ec35-184">Text constant: "&"</span></span>
3.  <span data-ttu-id="5ec35-185">Variantgruppe: Forgitter</span><span class="sxs-lookup"><span data-stu-id="5ec35-185">Configuration group: Front grill</span></span>

<span data-ttu-id="5ec35-186">I dette tilfælde vil konfigurations-id'et for et standardkabinet, der har frontgitter af stof, være M0007&M0021.</span><span class="sxs-lookup"><span data-stu-id="5ec35-186">In this case, the configuration ID for a standard cabinet that has a cloth front grill will be M0007&M0021.</span></span>

## <a name="nomenclature-for-a-combination-of-product-variants-and-configurations"></a><span data-ttu-id="5ec35-187">Nomenklaturen for en kombination af produktvarianter og -konfigurationer</span><span class="sxs-lookup"><span data-stu-id="5ec35-187">Nomenclature for a combination of product variants and configurations</span></span>
<span data-ttu-id="5ec35-188">Når du bruger enten begrænsningsbaseret eller dimensionsbaseret konfigurationsteknologi til at konfigurere produktvarianter for en produktmaster, kan produktvariantnumrene for produktvarianterne omfatte nomenklaturen fra konfigurationsdimensionen.</span><span class="sxs-lookup"><span data-stu-id="5ec35-188">When you use either the constraint-based configuration technology or the dimension-based configuration technology to configure product variants for a product master, the product variant numbers of the product variants can include the nomenclature from the configuration dimension.</span></span> <span data-ttu-id="5ec35-189">Hvis du vil konfigurere varianter, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="5ec35-189">Follow these steps to configure variants.</span></span>

1.  <span data-ttu-id="5ec35-190">Definer en nomenklatur for produktvariantnummer, som indeholder konfigurationsdimensionen på siden **Produktnomenklatur**.</span><span class="sxs-lookup"><span data-stu-id="5ec35-190">On the **Product nomenclature** page, define a product variant number nomenclature that includes the configuration dimension.</span></span>
2.  <span data-ttu-id="5ec35-191">Tildel nomenklaturen til en produktdimensionsgruppe, der har konfigurationsdimensionen.</span><span class="sxs-lookup"><span data-stu-id="5ec35-191">Assign the nomenclature to a product dimension group that has the configuration dimension.</span></span>
3.  <span data-ttu-id="5ec35-192">Definer en konfigurationsnomenklatur for komponenter eller styklister, der skal bruges til at konfigurere produktvarianterne.</span><span class="sxs-lookup"><span data-stu-id="5ec35-192">Define a configuration nomenclature for the components or BOMs that will be used to configure the product variants.</span></span>

<span data-ttu-id="5ec35-193">Du kan også oprette en nomenklaturer for produktvariantnavne.</span><span class="sxs-lookup"><span data-stu-id="5ec35-193">You can also create nomenclatures for the product variant names.</span></span> <span data-ttu-id="5ec35-194">Produktvariantnavnene kan konfigureres til at indeholde konfigurations-id'et eller -navnet.</span><span class="sxs-lookup"><span data-stu-id="5ec35-194">The product variant names can be configured to include the configuration ID or name.</span></span>

### <a name="example-for-constraint-based-configurations"></a><span data-ttu-id="5ec35-195">Eksempel på begrænsningsbaserede konfigurationer</span><span class="sxs-lookup"><span data-stu-id="5ec35-195">Example for constraint-based configurations</span></span>

<span data-ttu-id="5ec35-196">I dette eksempel bruger du bruge en nomenklatur for produktvariantnummer, der består af følgende segmenter:</span><span class="sxs-lookup"><span data-stu-id="5ec35-196">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="5ec35-197">Produktmasternummer</span><span class="sxs-lookup"><span data-stu-id="5ec35-197">Product master number</span></span>
2.  <span data-ttu-id="5ec35-198">Tekstkonstant "\_"</span><span class="sxs-lookup"><span data-stu-id="5ec35-198">Text constant "\_"</span></span>
3.  <span data-ttu-id="5ec35-199">Variantkonfiguration</span><span class="sxs-lookup"><span data-stu-id="5ec35-199">Configuration</span></span>

<span data-ttu-id="5ec35-200">Konfigurationsnomenklaturen består af følgende segmenter:</span><span class="sxs-lookup"><span data-stu-id="5ec35-200">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="5ec35-201">Attributværdi: Materiale</span><span class="sxs-lookup"><span data-stu-id="5ec35-201">Attribute value: Material</span></span>
2.  <span data-ttu-id="5ec35-202">Tekstkonstant: "AAA"</span><span class="sxs-lookup"><span data-stu-id="5ec35-202">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="5ec35-203">Attributværdi: Længde</span><span class="sxs-lookup"><span data-stu-id="5ec35-203">Attribute value: Length</span></span>

<span data-ttu-id="5ec35-204">Du kan angive følgende værdier for segmenter:</span><span class="sxs-lookup"><span data-stu-id="5ec35-204">You enter the following values for segments:</span></span>

-   <span data-ttu-id="5ec35-205">Produktmasternummer = **M0099**</span><span class="sxs-lookup"><span data-stu-id="5ec35-205">Product master number = **M0099**</span></span>
-   <span data-ttu-id="5ec35-206">Materiale = **Plast**</span><span class="sxs-lookup"><span data-stu-id="5ec35-206">Material = **Plastic**</span></span>
-   <span data-ttu-id="5ec35-207">Længde = **12**</span><span class="sxs-lookup"><span data-stu-id="5ec35-207">Length = **12**</span></span>

<span data-ttu-id="5ec35-208">I dette tilfælde er produktvariantnummeret M0099\_PlastAAA12.</span><span class="sxs-lookup"><span data-stu-id="5ec35-208">In this case, the product variant number will be M0099\_PlasticAAA12.</span></span>

### <a name="example-for-dimension-based-configurations"></a><span data-ttu-id="5ec35-209">Eksempel på dimensionsbaserede konfigurationer</span><span class="sxs-lookup"><span data-stu-id="5ec35-209">Example for dimension-based configurations</span></span>

<span data-ttu-id="5ec35-210">I dette eksempel bruger du bruge en nomenklatur for produktvariantnummer, der består af følgende segmenter:</span><span class="sxs-lookup"><span data-stu-id="5ec35-210">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="5ec35-211">Produktmasternummer</span><span class="sxs-lookup"><span data-stu-id="5ec35-211">Product master number</span></span>
2.  <span data-ttu-id="5ec35-212">Tekstkonstant "//"</span><span class="sxs-lookup"><span data-stu-id="5ec35-212">Text constant "//"</span></span>
3.  <span data-ttu-id="5ec35-213">Variantkonfiguration</span><span class="sxs-lookup"><span data-stu-id="5ec35-213">Configuration</span></span>

<span data-ttu-id="5ec35-214">Konfigurationsnomenklaturen består af følgende segmenter:</span><span class="sxs-lookup"><span data-stu-id="5ec35-214">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="5ec35-215">Variantgruppe: Kabinet</span><span class="sxs-lookup"><span data-stu-id="5ec35-215">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="5ec35-216">Tekstkonstant: "&"</span><span class="sxs-lookup"><span data-stu-id="5ec35-216">Text constant: "&"</span></span>
3.  <span data-ttu-id="5ec35-217">Variantgruppe: Forgitter</span><span class="sxs-lookup"><span data-stu-id="5ec35-217">Configuration group: Front grill</span></span>

<span data-ttu-id="5ec35-218">Du kan angive følgende værdier for segmenter:</span><span class="sxs-lookup"><span data-stu-id="5ec35-218">You enter the following values for segments:</span></span>

-   <span data-ttu-id="5ec35-219">Produktmasternummer = **D0123**</span><span class="sxs-lookup"><span data-stu-id="5ec35-219">Product master number = **D0123**</span></span>
-   <span data-ttu-id="5ec35-220">Kabinet = **M0008**</span><span class="sxs-lookup"><span data-stu-id="5ec35-220">Cabinet = **M0008**</span></span>
-   <span data-ttu-id="5ec35-221">Frontgitter = **M0022**</span><span class="sxs-lookup"><span data-stu-id="5ec35-221">Front grill = **M0022**</span></span>

<span data-ttu-id="5ec35-222">I dette tilfælde er produktvariantnummeret D0123//M0008&M0022.</span><span class="sxs-lookup"><span data-stu-id="5ec35-222">In this case, the product variant number will be D0123//M0008&M0022.</span></span>

## <a name="numbering-conflicts"></a><span data-ttu-id="5ec35-223">Nummerkonflikter</span><span class="sxs-lookup"><span data-stu-id="5ec35-223">Numbering conflicts</span></span>
<span data-ttu-id="5ec35-224">I nogle tilfælde resulterer en nomenklatur for produktvariantnummer, som du konfigurerer, muligvis ikke i entydige produktvariantnumre.</span><span class="sxs-lookup"><span data-stu-id="5ec35-224">In some cases, a product variant number nomenclature that you set up might not produce unique product variant numbers.</span></span> <span data-ttu-id="5ec35-225">F.eks. er produktvariantnumrene ikke entydige, hvis én aktiv produktdimension ikke er inkluderet i nomenklaturen for en produktmaster, der bruger foruddefineret variantkonfigurationsteknologi.</span><span class="sxs-lookup"><span data-stu-id="5ec35-225">For example, the product variant numbers won't be unique if one active product dimension isn't included in the nomenclature for a product master that uses the predefined variant configuration technology.</span></span> <span data-ttu-id="5ec35-226">Hvordan du håndterer konflikter varierer, afhængigt af konfigurationsteknologien.</span><span class="sxs-lookup"><span data-stu-id="5ec35-226">The way that you handle conflicts varies, depending on the configuration technology.</span></span>

### <a name="predefined-variants"></a><span data-ttu-id="5ec35-227">Foruddefinerede varianter</span><span class="sxs-lookup"><span data-stu-id="5ec35-227">Predefined variants</span></span>

<span data-ttu-id="5ec35-228">Der opstår en fejl, hvis du forsøger manuelt eller automatisk at generere produktvarianter, hvor en eller flere produktvarianter ender med at have det samme produktvariantnummer.</span><span class="sxs-lookup"><span data-stu-id="5ec35-228">An error occurs if you try to manually create or automatically generate product variants, and more than one product variant ends up with the same product variant number.</span></span> <span data-ttu-id="5ec35-229">Hvis du vil undgå denne situation, skal du bruge alle aktive produktdimensioner i produktdimensionsgruppen.</span><span class="sxs-lookup"><span data-stu-id="5ec35-229">To avoid this scenario, you should use all active product dimensions in the product dimension group.</span></span> <span data-ttu-id="5ec35-230">Du kan også inkludere en nummerserie for at sikre, at produktvariantnumrene er entydige.</span><span class="sxs-lookup"><span data-stu-id="5ec35-230">Alternatively, include a number sequence to help guarantee that the product variant numbers are unique.</span></span>

### <a name="constraint-based-configurations"></a><span data-ttu-id="5ec35-231">Begrænsningsbaserede konfigurationer</span><span class="sxs-lookup"><span data-stu-id="5ec35-231">Constraint-based configurations</span></span>

<span data-ttu-id="5ec35-232">Afhængigt af nomenklaturen vil systemet muligvis forsøge at tildele en konfiguration et ikke-entydigt produktvariantnummer.</span><span class="sxs-lookup"><span data-stu-id="5ec35-232">Depending on the nomenclature, the system might try to assign a non-unique product variant number to a configuration.</span></span> <span data-ttu-id="5ec35-233">I dette tilfælde bruger systemet i stedet for nummerserien for konfigurationsdimensionen som produktvariantnummer, og du får vist advarsel.</span><span class="sxs-lookup"><span data-stu-id="5ec35-233">In this case, the system uses the number sequence for the configuration dimension as the product variant number instead, and you receive a warning.</span></span> <span data-ttu-id="5ec35-234">Hvis du vil undgå dette scenarie, skal du medtage tilstrækkelig mange attributter i nomenklaturen til at sikre entydige produktvariantnumre.</span><span class="sxs-lookup"><span data-stu-id="5ec35-234">To avoid this scenario, you should include enough attributes in the nomenclature to help guarantee unique product variant numbers.</span></span> <span data-ttu-id="5ec35-235">Du skal også kontrollere, at indstillingen **Genbrug** er slået til for komponenten.</span><span class="sxs-lookup"><span data-stu-id="5ec35-235">You should also make sure that the **Reuse** option is turned on for the component.</span></span>

### <a name="dimension-based-configurations"></a><span data-ttu-id="5ec35-236">Dimensionsbaserede konfigurationer</span><span class="sxs-lookup"><span data-stu-id="5ec35-236">Dimension-based configurations</span></span>

<span data-ttu-id="5ec35-237">Under ét trin af konfigurationsprocessen, foreslår systemet en konfigurationsværdi i overensstemmelse med nomenklaturen.</span><span class="sxs-lookup"><span data-stu-id="5ec35-237">During one step of the configuration process, the system suggests a configuration value according to the nomenclature.</span></span> <span data-ttu-id="5ec35-238">I dette trin kan du manuelt ændre konfigurationsværdien.</span><span class="sxs-lookup"><span data-stu-id="5ec35-238">In this step, you can manually change the configuration value.</span></span> <span data-ttu-id="5ec35-239">Når du gemmer konfigurationen, undersøges det, om konfigurationsværdien er entydig.</span><span class="sxs-lookup"><span data-stu-id="5ec35-239">When you save the configuration, the system verifies that the configuration value is unique.</span></span> <span data-ttu-id="5ec35-240">Hvis den indtastede værdi ikke er entydig, får du vist en fejlmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="5ec35-240">If the value that you entered isn't unique, you receive an error message.</span></span> <span data-ttu-id="5ec35-241">Du skal angive en unik konfigurationsværdi for at kunne gemme konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="5ec35-241">To save the configuration, you must enter a unique configuration value.</span></span>

<a name="additional-resources"></a><span data-ttu-id="5ec35-242">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="5ec35-242">Additional resources</span></span>
--------

[<span data-ttu-id="5ec35-243">Oprette et produktnummernomenklatur for foruddefinerede produktvarianter</span><span class="sxs-lookup"><span data-stu-id="5ec35-243">Create a product number nomenclature for predefined product variants</span></span>](tasks/create-product-number-nomenclature-predefined-variants-2016-11.md)

[<span data-ttu-id="5ec35-244">Opret en nomenklatur for produktnumre for konfigurerede produktvarianter</span><span class="sxs-lookup"><span data-stu-id="5ec35-244">Create a product number nomenclature for configured product variants</span></span>](tasks/create-product-number-nomenclature-product-variants_2016_11.md)

