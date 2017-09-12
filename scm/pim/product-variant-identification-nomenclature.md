---
title: Nomenklatur for produktvariantnumre og -navne
description: "Dette emne beskriver, hvordan du kan konfigurere en nomenklatur for produktnumre til erstatning for det faste [produktmasternummer - konfiguration - størrelse - farve - type] format. Den nye nomenklatur har et målrettet format, der omfatter produktmasternummer, aktive produktdimensioner og tekstafgrænsningstegn efter eget valg. Du kan også oprette en nomenklatur for produktnavne. Endelig kan du også oprette en nomenklatur til at identificere konfigurationer, der er oprettet af den begrænsningsbaserede produktkonfigurator. Disse nomenklaturer kan indeholde attributter efter eget valg."
author: roxanadiaconu
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 220104
ms.assetid: 3fe69fb7-5c32-423c-98a8-2f53186cda68
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: d1a9ced00d8dc09e59512056392a250a76ba5b97
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---

# <a name="nomenclature-of-product-variant-numbers-and-names"></a><span data-ttu-id="ebe92-107">Nomenklatur for produktvariantnumre og -navne</span><span class="sxs-lookup"><span data-stu-id="ebe92-107">Nomenclature of product variant numbers and names</span></span>

<span data-ttu-id="ebe92-108">Dette emne beskriver, hvordan du kan konfigurere en nomenklatur for produktnumre til erstatning for det faste [produktmasternummer - konfiguration - størrelse - farve - type] format.</span><span class="sxs-lookup"><span data-stu-id="ebe92-108">This topic describes how you can set up a product number nomenclature to replace the fixed [Product master number - Configuration - Size - Color - Style] format.</span></span> <span data-ttu-id="ebe92-109">Den nye nomenklatur har et målrettet format, der omfatter produktmasternummer, aktive produktdimensioner og tekstafgrænsningstegn efter eget valg.</span><span class="sxs-lookup"><span data-stu-id="ebe92-109">The new nomenclature has a targeted format that includes the product master number, active product dimensions, and text delimiters of your choice.</span></span> <span data-ttu-id="ebe92-110">Du kan også oprette en nomenklatur for produktnavne.</span><span class="sxs-lookup"><span data-stu-id="ebe92-110">You can also create a nomenclature for product names.</span></span> <span data-ttu-id="ebe92-111">Endelig kan du også oprette en nomenklatur til at identificere konfigurationer, der er oprettet af den begrænsningsbaserede produktkonfigurator.</span><span class="sxs-lookup"><span data-stu-id="ebe92-111">Finally, you can build a nomenclature to identify configurations that are created by the constraint-based product configurator.</span></span> <span data-ttu-id="ebe92-112">Disse nomenklaturer kan indeholde attributter efter eget valg.</span><span class="sxs-lookup"><span data-stu-id="ebe92-112">These nomenclatures can contain attributes of your choice.</span></span>

<span data-ttu-id="ebe92-113">De nye nomenklaturer for produktvariantnumre og produktvariantnavne giver dig mulighed for at medtage segmenter i id'erne for produktvarianter.</span><span class="sxs-lookup"><span data-stu-id="ebe92-113">The new nomenclatures for product variant numbers and product variant names let you include segments in the identifiers for product variants.</span></span> <span data-ttu-id="ebe92-114">Disse segmenter kan indeholde produktmasternummer og -navn, produktdimensions-id'er og -navne, nummerserier, tekstkonstanter og attributter.</span><span class="sxs-lookup"><span data-stu-id="ebe92-114">These segments can include the product master number and name, product dimension IDs and names, number sequences, text constants, and attributes.</span></span> <span data-ttu-id="ebe92-115">Med denne funktion kan du hurtigt finde en bestemt produktvariant, når du opretter en salgsordre eller en indkøbsordre.</span><span class="sxs-lookup"><span data-stu-id="ebe92-115">This functionality lets you quickly find a specific product variant when you create a sales order or a purchase order.</span></span> <span data-ttu-id="ebe92-116">Du opretter nomenklaturer til både produktvariantnumre og produktvariantnavne ved hjælp af siden **Produktnomenklatur**.</span><span class="sxs-lookup"><span data-stu-id="ebe92-116">You create nomenclatures for both product variant numbers and product variant names by using the **Product nomenclature** page.</span></span> <span data-ttu-id="ebe92-117">Klik på **Administration af produktoplysninger** &gt; **Konfiguration** for at åbne denne side.</span><span class="sxs-lookup"><span data-stu-id="ebe92-117">To open this page, click **Product information management** &gt; **Setup**.</span></span>

## <a name="nomenclature-of-predefined-product-variants"></a><span data-ttu-id="ebe92-118">Nomenklatur for foruddefinerede produktvarianter</span><span class="sxs-lookup"><span data-stu-id="ebe92-118">Nomenclature of predefined product variants</span></span>
<span data-ttu-id="ebe92-119">Der oprettes produktvarianter for produktmastere efter en af de tre konfigurationsteknologier:</span><span class="sxs-lookup"><span data-stu-id="ebe92-119">Product variants are generated for product masters according to one of three configuration technologies:</span></span>

-   <span data-ttu-id="ebe92-120">Foruddefinerede varianter</span><span class="sxs-lookup"><span data-stu-id="ebe92-120">Predefined variants</span></span>
-   <span data-ttu-id="ebe92-121">Begrænsningsbaseret</span><span class="sxs-lookup"><span data-stu-id="ebe92-121">Constraint-based</span></span>
-   <span data-ttu-id="ebe92-122">Dimensionsbaseret</span><span class="sxs-lookup"><span data-stu-id="ebe92-122">Dimension-based</span></span>

<span data-ttu-id="ebe92-123">Hver produktvariant har et nummer og et navn, og nomenklaturerne for produktvariantidentifikation giver dig mulighed for at vælge de segmenter, der skal medtages i hvert produktvariantnummer eller -navn.</span><span class="sxs-lookup"><span data-stu-id="ebe92-123">Each product variant has a number and a name, and the product variant identification nomenclatures let you select the segments that will be included in each product variant number or name.</span></span> <span data-ttu-id="ebe92-124">Du kan vælge følgende segmenter på siden **Produktnomenklatur**:</span><span class="sxs-lookup"><span data-stu-id="ebe92-124">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="ebe92-125">Produktmasternummer</span><span class="sxs-lookup"><span data-stu-id="ebe92-125">Product master number</span></span>
-   <span data-ttu-id="ebe92-126">Produktmasternavn</span><span class="sxs-lookup"><span data-stu-id="ebe92-126">Product master name</span></span>
-   <span data-ttu-id="ebe92-127">Nummerserieværdi</span><span class="sxs-lookup"><span data-stu-id="ebe92-127">Number sequence value</span></span>
-   <span data-ttu-id="ebe92-128">Tekstkonstant</span><span class="sxs-lookup"><span data-stu-id="ebe92-128">Text constant</span></span>
-   <span data-ttu-id="ebe92-129">Produktdimensioner</span><span class="sxs-lookup"><span data-stu-id="ebe92-129">Product dimensions</span></span>
    -   <span data-ttu-id="ebe92-130">Konfigurations-id eller -navn</span><span class="sxs-lookup"><span data-stu-id="ebe92-130">Configuration ID or name</span></span>
    -   <span data-ttu-id="ebe92-131">Farve-id eller -navn</span><span class="sxs-lookup"><span data-stu-id="ebe92-131">Color ID or name</span></span>
    -   <span data-ttu-id="ebe92-132">Størrelses-id eller -navn</span><span class="sxs-lookup"><span data-stu-id="ebe92-132">Size ID or name</span></span>
    -   <span data-ttu-id="ebe92-133">Type-id eller -navn</span><span class="sxs-lookup"><span data-stu-id="ebe92-133">Style ID or name</span></span>

<span data-ttu-id="ebe92-134">Når du har defineret en nomenklatur for produktvariantidentifikationsnummer, kan du knytte den til en produktdimensionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="ebe92-134">After you define a product variant identification number nomenclature, you can associate it with a product dimension group.</span></span> <span data-ttu-id="ebe92-135">Alle de produktmastere, der refererer til denne produktdimensionsgruppe, vil derfor blive tildelt produktvariantnumre efter nomenklaturen.</span><span class="sxs-lookup"><span data-stu-id="ebe92-135">All product masters that reference this product dimension group will then be assigned product variant numbers according to the nomenclature.</span></span> <span data-ttu-id="ebe92-136">Men nomenklaturer for produktvariantnavn kan dog ikke knyttes til produktdimensionsgrupper.</span><span class="sxs-lookup"><span data-stu-id="ebe92-136">However, product variant name nomenclatures can't be associated with product dimension groups.</span></span> <span data-ttu-id="ebe92-137">Du kan også tildele en nomenklatur for produktvariantidentifikation direkte til en produktmaster.</span><span class="sxs-lookup"><span data-stu-id="ebe92-137">You can also assign a product variant identification nomenclature directly to a product master.</span></span> <span data-ttu-id="ebe92-138">I dette tilfælde tildeles de produktvarianter, der hører til produktmasteren, produktvariantnumre og -navne i overensstemmelse med nomenklaturerne.</span><span class="sxs-lookup"><span data-stu-id="ebe92-138">In this case, the product variants that belong to the product master will be assigned product variant numbers and names according to the nomenclatures.</span></span>

### <a name="example"></a><span data-ttu-id="ebe92-139">Eksempel</span><span class="sxs-lookup"><span data-stu-id="ebe92-139">Example</span></span>

<span data-ttu-id="ebe92-140">En T-shirt (TS1234), der produceres i tre størrelser (S, M, L), fire farver (rød, grøn, blå, gul) og to typer (Polo, V).</span><span class="sxs-lookup"><span data-stu-id="ebe92-140">A T-shirt (TS1234) is produced in three sizes (S, M, L), four colors (Red, Green, Blue, Yellow), and two styles (Polo, V).</span></span> <span data-ttu-id="ebe92-141">Derfor er der 24 mulige produktvarianter (= 3 × 4 × 2).</span><span class="sxs-lookup"><span data-stu-id="ebe92-141">Therefore, 24 product variants are possible (= 3 × 4 × 2).</span></span> <span data-ttu-id="ebe92-142">Du opretter en nomenklatur for produktvariantnumre, der har følgende segmenter:</span><span class="sxs-lookup"><span data-stu-id="ebe92-142">You create a product variant number nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="ebe92-143">Produktmasternummer</span><span class="sxs-lookup"><span data-stu-id="ebe92-143">Product master number</span></span>
2.  <span data-ttu-id="ebe92-144">Tekstkonstant: "-"</span><span class="sxs-lookup"><span data-stu-id="ebe92-144">Text constant: "-"</span></span>
3.  <span data-ttu-id="ebe92-145">Farve</span><span class="sxs-lookup"><span data-stu-id="ebe92-145">Color</span></span>
4.  <span data-ttu-id="ebe92-146">Tekstkonstant: "-"</span><span class="sxs-lookup"><span data-stu-id="ebe92-146">Text constant: "-"</span></span>
5.  <span data-ttu-id="ebe92-147">Størrelse</span><span class="sxs-lookup"><span data-stu-id="ebe92-147">Size</span></span>
6.  <span data-ttu-id="ebe92-148">Tekstkonstant: "-"</span><span class="sxs-lookup"><span data-stu-id="ebe92-148">Text constant: "-"</span></span>
7.  <span data-ttu-id="ebe92-149">Type</span><span class="sxs-lookup"><span data-stu-id="ebe92-149">Style</span></span>

<span data-ttu-id="ebe92-150">I dette tilfælde vil produktvariantnummeret for en rød, small, polo T-shirt være TS1234-Rød-Small-Polo.</span><span class="sxs-lookup"><span data-stu-id="ebe92-150">In this case, the product variant number for a red, small, polo T-shirt will be TS1234-Red-Small-Polo.</span></span>

## <a name="nomenclature-of-constraintbased-configurations"></a><span data-ttu-id="ebe92-151">Nomenklatur for begrænsningsbaserede konfigurationer</span><span class="sxs-lookup"><span data-stu-id="ebe92-151">Nomenclature of constraintbased configurations</span></span>
<span data-ttu-id="ebe92-152">Til begrænsningsbaserede konfigurationer kan du oprette en dedikeret nomenklatur til konfigurationsproduktdimensionen.</span><span class="sxs-lookup"><span data-stu-id="ebe92-152">For constraint-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="ebe92-153">Du kan vælge følgende segmenter på siden **Produktnomenklatur**:</span><span class="sxs-lookup"><span data-stu-id="ebe92-153">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="ebe92-154">Nummerserieværdi</span><span class="sxs-lookup"><span data-stu-id="ebe92-154">Number sequence value</span></span>
-   <span data-ttu-id="ebe92-155">Tekstkonstant</span><span class="sxs-lookup"><span data-stu-id="ebe92-155">Text constant</span></span>
-   <span data-ttu-id="ebe92-156">Attributværdi</span><span class="sxs-lookup"><span data-stu-id="ebe92-156">Attribute value</span></span>

<span data-ttu-id="ebe92-157">Hver komponent i en produktkonfigurationsmodel kan have sin egen konfigurationsnomenklatur.</span><span class="sxs-lookup"><span data-stu-id="ebe92-157">Each component in a product configuration model can have its own configuration nomenclature.</span></span> <span data-ttu-id="ebe92-158">Kun de attributter, der tilhører komponenten, kan anvendes.</span><span class="sxs-lookup"><span data-stu-id="ebe92-158">Only attributes that belong to the component can be used.</span></span> <span data-ttu-id="ebe92-159">Attributter fra underkomponenter eller brugerkrav kan ikke anvendes.</span><span class="sxs-lookup"><span data-stu-id="ebe92-159">Attributes from subcomponents or user requirements can't be used.</span></span>

### <a name="example"></a><span data-ttu-id="ebe92-160">Eksempel</span><span class="sxs-lookup"><span data-stu-id="ebe92-160">Example</span></span>

<span data-ttu-id="ebe92-161">En produktkonfigurationsmodel har en rodkomponent, der har to attributter:</span><span class="sxs-lookup"><span data-stu-id="ebe92-161">A product configuration model has a root component that has two attributes:</span></span>

-   <span data-ttu-id="ebe92-162">Materiale (plast, træ, stål)</span><span class="sxs-lookup"><span data-stu-id="ebe92-162">Material (Plastic, Wood, Steel)</span></span>
-   <span data-ttu-id="ebe92-163">Længde (10... 100)</span><span class="sxs-lookup"><span data-stu-id="ebe92-163">Length (10...100)</span></span>

<span data-ttu-id="ebe92-164">Du opretter en konfigurationsnomenklatur, der har følgende segmenter:</span><span class="sxs-lookup"><span data-stu-id="ebe92-164">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="ebe92-165">Attributværdi: Materiale</span><span class="sxs-lookup"><span data-stu-id="ebe92-165">Attribute value: Material</span></span>
2.  <span data-ttu-id="ebe92-166">Tekstkonstant: "AAA"</span><span class="sxs-lookup"><span data-stu-id="ebe92-166">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="ebe92-167">Attributværdi: Længde</span><span class="sxs-lookup"><span data-stu-id="ebe92-167">Attribute value: Length</span></span>

<span data-ttu-id="ebe92-168">I dette tilfælde vil konfigurations-id'et for træmateriale, der har en længde på 78, være WoodAAA78.</span><span class="sxs-lookup"><span data-stu-id="ebe92-168">In this case, the configuration ID for wood material that has a length of 78 will be WoodAAA78.</span></span>

## <a name="nomenclature-of-dimensionbased-configurations"></a><span data-ttu-id="ebe92-169">Nomenklatur for dimensionsbaserede konfigurationer</span><span class="sxs-lookup"><span data-stu-id="ebe92-169">Nomenclature of dimensionbased configurations</span></span>
<span data-ttu-id="ebe92-170">Til dimensionsbaserede konfigurationer kan du oprette en dedikeret nomenklatur til konfigurationsproduktdimensionen.</span><span class="sxs-lookup"><span data-stu-id="ebe92-170">For dimension-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="ebe92-171">Du kan vælge følgende segmenter på siden **Produktnomenklatur**:</span><span class="sxs-lookup"><span data-stu-id="ebe92-171">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="ebe92-172">Nummerserieværdi</span><span class="sxs-lookup"><span data-stu-id="ebe92-172">Number sequence value</span></span>
-   <span data-ttu-id="ebe92-173">Tekstkonstant</span><span class="sxs-lookup"><span data-stu-id="ebe92-173">Text constant</span></span>
-   <span data-ttu-id="ebe92-174">Vare i konfigurationsgruppe</span><span class="sxs-lookup"><span data-stu-id="ebe92-174">Configuration group item</span></span>

<span data-ttu-id="ebe92-175">Du kan definere en konfigurationsnomenklatur for en stykliste.</span><span class="sxs-lookup"><span data-stu-id="ebe92-175">You can define a configuration nomenclature for a bill of materials (BOM).</span></span>

### <a name="example"></a><span data-ttu-id="ebe92-176">Eksempel</span><span class="sxs-lookup"><span data-stu-id="ebe92-176">Example</span></span>

<span data-ttu-id="ebe92-177">En stykliste indeholder fire styklistelinjer, der er opdelt i to konfigurationsgrupper:</span><span class="sxs-lookup"><span data-stu-id="ebe92-177">A BOM has four BOM lines that are divided into two configuration groups:</span></span>

-   <span data-ttu-id="ebe92-178">Styklistelinje: M0007, Standardkabinet</span><span class="sxs-lookup"><span data-stu-id="ebe92-178">BOM line: M0007, Standard cabinet</span></span>
    -   <span data-ttu-id="ebe92-179">Variantgruppe: Kabinet</span><span class="sxs-lookup"><span data-stu-id="ebe92-179">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="ebe92-180">Styklistelinje: M0008, Kabinet af topkvalitet</span><span class="sxs-lookup"><span data-stu-id="ebe92-180">BOM line: M0008, High end cabinet</span></span>
    -   <span data-ttu-id="ebe92-181">Variantgruppe: Kabinet</span><span class="sxs-lookup"><span data-stu-id="ebe92-181">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="ebe92-182">Styklistelinje: M0021, Forgitter af stof</span><span class="sxs-lookup"><span data-stu-id="ebe92-182">BOM line: M0021, Front grill cloth</span></span>
    -   <span data-ttu-id="ebe92-183">Variantgruppe: Forgitter</span><span class="sxs-lookup"><span data-stu-id="ebe92-183">Configuration group: Front grill</span></span>
-   <span data-ttu-id="ebe92-184">Styklistelinje: M0022, Forgitter af metal</span><span class="sxs-lookup"><span data-stu-id="ebe92-184">BOM line: M0022, Front grill metal</span></span>
    -   <span data-ttu-id="ebe92-185">Variantgruppe: Forgitter</span><span class="sxs-lookup"><span data-stu-id="ebe92-185">Configuration group: Front grill</span></span>

<span data-ttu-id="ebe92-186">Du opretter en konfigurationsnomenklatur, der har følgende segmenter:</span><span class="sxs-lookup"><span data-stu-id="ebe92-186">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="ebe92-187">Variantgruppe: Kabinet</span><span class="sxs-lookup"><span data-stu-id="ebe92-187">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="ebe92-188">Tekstkonstant: "&"</span><span class="sxs-lookup"><span data-stu-id="ebe92-188">Text constant: "&"</span></span>
3.  <span data-ttu-id="ebe92-189">Variantgruppe: Forgitter</span><span class="sxs-lookup"><span data-stu-id="ebe92-189">Configuration group: Front grill</span></span>

<span data-ttu-id="ebe92-190">I dette tilfælde vil konfigurations-id'et for et standardkabinet, der har frontgitter af stof, være M0007&M0021.</span><span class="sxs-lookup"><span data-stu-id="ebe92-190">In this case, the configuration ID for a standard cabinet that has a cloth front grill will be M0007&M0021.</span></span>

## <a name="nomenclature-for-a-combination-of-product-variants-and-configurations"></a><span data-ttu-id="ebe92-191">Nomenklaturen for en kombination af produktvarianter og -konfigurationer</span><span class="sxs-lookup"><span data-stu-id="ebe92-191">Nomenclature for a combination of product variants and configurations</span></span>
<span data-ttu-id="ebe92-192">Når du bruger enten begrænsningsbaseret eller dimensionsbaseret konfigurationsteknologi til at konfigurere produktvarianter for en produktmaster, kan produktvariantnumrene for produktvarianterne omfatte nomenklaturen fra konfigurationsdimensionen.</span><span class="sxs-lookup"><span data-stu-id="ebe92-192">When you use either the constraint-based configuration technology or the dimension-based configuration technology to configure product variants for a product master, the product variant numbers of the product variants can include the nomenclature from the configuration dimension.</span></span> <span data-ttu-id="ebe92-193">Hvis du vil konfigurere varianter, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="ebe92-193">Follow these steps to configure variants.</span></span>

1.  <span data-ttu-id="ebe92-194">Definer en nomenklatur for produktvariantnummer, som indeholder konfigurationsdimensionen på siden **Produktnomenklatur**.</span><span class="sxs-lookup"><span data-stu-id="ebe92-194">On the **Product nomenclature** page, define a product variant number nomenclature that includes the configuration dimension.</span></span>
2.  <span data-ttu-id="ebe92-195">Tildel nomenklaturen til en produktdimensionsgruppe, der har konfigurationsdimensionen.</span><span class="sxs-lookup"><span data-stu-id="ebe92-195">Assign the nomenclature to a product dimension group that has the configuration dimension.</span></span>
3.  <span data-ttu-id="ebe92-196">Definer en konfigurationsnomenklatur for komponenter eller styklister, der skal bruges til at konfigurere produktvarianterne.</span><span class="sxs-lookup"><span data-stu-id="ebe92-196">Define a configuration nomenclature for the components or BOMs that will be used to configure the product variants.</span></span>

<span data-ttu-id="ebe92-197">Du kan også oprette en nomenklaturer for produktvariantnavne.</span><span class="sxs-lookup"><span data-stu-id="ebe92-197">You can also create nomenclatures for the product variant names.</span></span> <span data-ttu-id="ebe92-198">Produktvariantnavnene kan konfigureres til at indeholde konfigurations-id'et eller -navnet.</span><span class="sxs-lookup"><span data-stu-id="ebe92-198">The product variant names can be configured to include the configuration ID or name.</span></span>

### <a name="example-for-constraint-based-configurations"></a><span data-ttu-id="ebe92-199">Eksempel på begrænsningsbaserede konfigurationer</span><span class="sxs-lookup"><span data-stu-id="ebe92-199">Example for constraint-based configurations</span></span>

<span data-ttu-id="ebe92-200">I dette eksempel bruger du bruge en nomenklatur for produktvariantnummer, der består af følgende segmenter:</span><span class="sxs-lookup"><span data-stu-id="ebe92-200">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="ebe92-201">Produktmasternummer</span><span class="sxs-lookup"><span data-stu-id="ebe92-201">Product master number</span></span>
2.  <span data-ttu-id="ebe92-202">Tekstkonstant "\_"</span><span class="sxs-lookup"><span data-stu-id="ebe92-202">Text constant "\_"</span></span>
3.  <span data-ttu-id="ebe92-203">Variantkonfiguration</span><span class="sxs-lookup"><span data-stu-id="ebe92-203">Configuration</span></span>

<span data-ttu-id="ebe92-204">Konfigurationsnomenklaturen består af følgende segmenter:</span><span class="sxs-lookup"><span data-stu-id="ebe92-204">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="ebe92-205">Attributværdi: Materiale</span><span class="sxs-lookup"><span data-stu-id="ebe92-205">Attribute value: Material</span></span>
2.  <span data-ttu-id="ebe92-206">Tekstkonstant: "AAA"</span><span class="sxs-lookup"><span data-stu-id="ebe92-206">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="ebe92-207">Attributværdi: Længde</span><span class="sxs-lookup"><span data-stu-id="ebe92-207">Attribute value: Length</span></span>

<span data-ttu-id="ebe92-208">Du kan angive følgende værdier for segmenter:</span><span class="sxs-lookup"><span data-stu-id="ebe92-208">You enter the following values for segments:</span></span>

-   <span data-ttu-id="ebe92-209">Produktmasternummer = **M0099**</span><span class="sxs-lookup"><span data-stu-id="ebe92-209">Product master number = **M0099**</span></span>
-   <span data-ttu-id="ebe92-210">Materiale = **Plast**</span><span class="sxs-lookup"><span data-stu-id="ebe92-210">Material = **Plastic**</span></span>
-   <span data-ttu-id="ebe92-211">Længde = **12**</span><span class="sxs-lookup"><span data-stu-id="ebe92-211">Length = **12**</span></span>

<span data-ttu-id="ebe92-212">I dette tilfælde er produktvariantnummeret M0099\_PlastAAA12.</span><span class="sxs-lookup"><span data-stu-id="ebe92-212">In this case, the product variant number will be M0099\_PlasticAAA12.</span></span>

### <a name="example-for-dimension-based-configurations"></a><span data-ttu-id="ebe92-213">Eksempel på dimensionsbaserede konfigurationer</span><span class="sxs-lookup"><span data-stu-id="ebe92-213">Example for dimension-based configurations</span></span>

<span data-ttu-id="ebe92-214">I dette eksempel bruger du bruge en nomenklatur for produktvariantnummer, der består af følgende segmenter:</span><span class="sxs-lookup"><span data-stu-id="ebe92-214">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="ebe92-215">Produktmasternummer</span><span class="sxs-lookup"><span data-stu-id="ebe92-215">Product master number</span></span>
2.  <span data-ttu-id="ebe92-216">Tekstkonstant "//"</span><span class="sxs-lookup"><span data-stu-id="ebe92-216">Text constant "//"</span></span>
3.  <span data-ttu-id="ebe92-217">Variantkonfiguration</span><span class="sxs-lookup"><span data-stu-id="ebe92-217">Configuration</span></span>

<span data-ttu-id="ebe92-218">Konfigurationsnomenklaturen består af følgende segmenter:</span><span class="sxs-lookup"><span data-stu-id="ebe92-218">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="ebe92-219">Variantgruppe: Kabinet</span><span class="sxs-lookup"><span data-stu-id="ebe92-219">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="ebe92-220">Tekstkonstant: "&"</span><span class="sxs-lookup"><span data-stu-id="ebe92-220">Text constant: "&"</span></span>
3.  <span data-ttu-id="ebe92-221">Variantgruppe: Forgitter</span><span class="sxs-lookup"><span data-stu-id="ebe92-221">Configuration group: Front grill</span></span>

<span data-ttu-id="ebe92-222">Du kan angive følgende værdier for segmenter:</span><span class="sxs-lookup"><span data-stu-id="ebe92-222">You enter the following values for segments:</span></span>

-   <span data-ttu-id="ebe92-223">Produktmasternummer = **D0123**</span><span class="sxs-lookup"><span data-stu-id="ebe92-223">Product master number = **D0123**</span></span>
-   <span data-ttu-id="ebe92-224">Kabinet = **M0008**</span><span class="sxs-lookup"><span data-stu-id="ebe92-224">Cabinet = **M0008**</span></span>
-   <span data-ttu-id="ebe92-225">Frontgitter = **M0022**</span><span class="sxs-lookup"><span data-stu-id="ebe92-225">Front grill = **M0022**</span></span>

<span data-ttu-id="ebe92-226">I dette tilfælde er produktvariantnummeret D0123//M0008&M0022.</span><span class="sxs-lookup"><span data-stu-id="ebe92-226">In this case, the product variant number will be D0123//M0008&M0022.</span></span>

## <a name="numbering-conflicts"></a><span data-ttu-id="ebe92-227">Nummerkonflikter</span><span class="sxs-lookup"><span data-stu-id="ebe92-227">Numbering conflicts</span></span>
<span data-ttu-id="ebe92-228">I nogle tilfælde resulterer en nomenklatur for produktvariantnummer, som du konfigurerer, muligvis ikke i entydige produktvariantnumre.</span><span class="sxs-lookup"><span data-stu-id="ebe92-228">In some cases, a product variant number nomenclature that you set up might not produce unique product variant numbers.</span></span> <span data-ttu-id="ebe92-229">F.eks. er produktvariantnumrene ikke entydige, hvis én aktiv produktdimension ikke er inkluderet i nomenklaturen for en produktmaster, der bruger foruddefineret variantkonfigurationsteknologi.</span><span class="sxs-lookup"><span data-stu-id="ebe92-229">For example, the product variant numbers won't be unique if one active product dimension isn't included in the nomenclature for a product master that uses the predefined variant configuration technology.</span></span> <span data-ttu-id="ebe92-230">Hvordan du håndterer konflikter varierer, afhængigt af konfigurationsteknologien.</span><span class="sxs-lookup"><span data-stu-id="ebe92-230">The way that you handle conflicts varies, depending on the configuration technology.</span></span>

### <a name="predefined-variants"></a><span data-ttu-id="ebe92-231">Foruddefinerede varianter</span><span class="sxs-lookup"><span data-stu-id="ebe92-231">Predefined variants</span></span>

<span data-ttu-id="ebe92-232">Der opstår en fejl, hvis du forsøger manuelt eller automatisk at generere produktvarianter, hvor en eller flere produktvarianter ender med at have det samme produktvariantnummer.</span><span class="sxs-lookup"><span data-stu-id="ebe92-232">An error occurs if you try to manually create or automatically generate product variants, and more than one product variant ends up with the same product variant number.</span></span> <span data-ttu-id="ebe92-233">Hvis du vil undgå denne situation, skal du bruge alle aktive produktdimensioner i produktdimensionsgruppen.</span><span class="sxs-lookup"><span data-stu-id="ebe92-233">To avoid this scenario, you should use all active product dimensions in the product dimension group.</span></span> <span data-ttu-id="ebe92-234">Du kan også inkludere en nummerserie for at sikre, at produktvariantnumrene er entydige.</span><span class="sxs-lookup"><span data-stu-id="ebe92-234">Alternatively, include a number sequence to help guarantee that the product variant numbers are unique.</span></span>

### <a name="constraint-based-configurations"></a><span data-ttu-id="ebe92-235">Begrænsningsbaserede konfigurationer</span><span class="sxs-lookup"><span data-stu-id="ebe92-235">Constraint-based configurations</span></span>

<span data-ttu-id="ebe92-236">Afhængigt af nomenklaturen vil systemet muligvis forsøge at tildele en konfiguration et ikke-entydigt produktvariantnummer.</span><span class="sxs-lookup"><span data-stu-id="ebe92-236">Depending on the nomenclature, the system might try to assign a non-unique product variant number to a configuration.</span></span> <span data-ttu-id="ebe92-237">I dette tilfælde bruger systemet i stedet for nummerserien for konfigurationsdimensionen som produktvariantnummer, og du får vist advarsel.</span><span class="sxs-lookup"><span data-stu-id="ebe92-237">In this case, the system uses the number sequence for the configuration dimension as the product variant number instead, and you receive a warning.</span></span> <span data-ttu-id="ebe92-238">Hvis du vil undgå dette scenarie, skal du medtage tilstrækkelig mange attributter i nomenklaturen til at sikre entydige produktvariantnumre.</span><span class="sxs-lookup"><span data-stu-id="ebe92-238">To avoid this scenario, you should include enough attributes in the nomenclature to help guarantee unique product variant numbers.</span></span> <span data-ttu-id="ebe92-239">Du skal også kontrollere, at indstillingen **Genbrug** er slået til for komponenten.</span><span class="sxs-lookup"><span data-stu-id="ebe92-239">You should also make sure that the **Reuse** option is turned on for the component.</span></span>

### <a name="dimension-based-configurations"></a><span data-ttu-id="ebe92-240">Dimensionsbaserede konfigurationer</span><span class="sxs-lookup"><span data-stu-id="ebe92-240">Dimension-based configurations</span></span>

<span data-ttu-id="ebe92-241">Under ét trin af konfigurationsprocessen, foreslår systemet en konfigurationsværdi i overensstemmelse med nomenklaturen.</span><span class="sxs-lookup"><span data-stu-id="ebe92-241">During one step of the configuration process, the system suggests a configuration value according to the nomenclature.</span></span> <span data-ttu-id="ebe92-242">I dette trin kan du manuelt ændre konfigurationsværdien.</span><span class="sxs-lookup"><span data-stu-id="ebe92-242">In this step, you can manually change the configuration value.</span></span> <span data-ttu-id="ebe92-243">Når du gemmer konfigurationen, undersøges det, om konfigurationsværdien er entydig.</span><span class="sxs-lookup"><span data-stu-id="ebe92-243">When you save the configuration, the system verifies that the configuration value is unique.</span></span> <span data-ttu-id="ebe92-244">Hvis den indtastede værdi ikke er entydig, får du vist en fejlmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="ebe92-244">If the value that you entered isn't unique, you receive an error message.</span></span> <span data-ttu-id="ebe92-245">Du skal angive en unik konfigurationsværdi for at kunne gemme konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="ebe92-245">To save the configuration, you must enter a unique configuration value.</span></span>

<a name="see-also"></a><span data-ttu-id="ebe92-246">Se også</span><span class="sxs-lookup"><span data-stu-id="ebe92-246">See also</span></span>
--------

[<span data-ttu-id="ebe92-247">Opret en nomenklatur for produktnumre for foruddefinerede produktvarianter</span><span class="sxs-lookup"><span data-stu-id="ebe92-247">Create a product number nomenclature for predefined product variants</span></span>](/dynamics365/unified-operations/supply-chain/pim/tasks/create-product-number-nomenclature-predefined-variants-2016-11)

[<span data-ttu-id="ebe92-248">Opret en nomenklatur for produktnumre for konfigurerede produktvarianter</span><span class="sxs-lookup"><span data-stu-id="ebe92-248">Create a product number nomenclature for configured product variants</span></span>](/dynamics365/unified-operations/supply-chain/pim/tasks/create-product-number-nomenclature-product-variants_2016_11)


