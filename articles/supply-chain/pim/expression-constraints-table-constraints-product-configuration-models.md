---
title: "Udtryksbegrænsninger og tabelbegrænsninger i produktkonfigurationsmodeller"
description: "I dette emne beskrives brugen af udtryksbegrænsninger og tabelbegrænsninger. Begrænsninger styrer de attributværdier, som du kan vælge, når du konfigurerer produkter til en salgsordre, et salgstilbud, en indkøbsordre eller en produktionsordre. Du kan bruge udtryksbegrænsninger eller tabelbegrænsninger, afhængigt af hvordan du foretrækker at udforme begrænsninger."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCGlobalTableConstraintEdit, PCProductConfigurationModelDetails, PCTableConstraintAttachAttributeTree, PCTableConstraintDefinition
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 53111
ms.assetid: 5c12b1f2-eb89-4648-a755-de412f2eadd6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 6dd2aa1ebc713287120106a9d1ec7dc15c24def9
ms.openlocfilehash: 66d5ec61c1d69ebc8a8fc10d0b9b2a4b174729ee
ms.contentlocale: da-dk
ms.lasthandoff: 09/14/2017

---

# <a name="expression-constraints-and-table-constraints-in-product-configuration-models"></a><span data-ttu-id="2af74-105">Udtryksbegrænsninger og tabelbegrænsninger i produktkonfigurationsmodeller</span><span class="sxs-lookup"><span data-stu-id="2af74-105">Expression constraints and table constraints in product configuration models</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="2af74-106">I dette emne beskrives brugen af udtryksbegrænsninger og tabelbegrænsninger.</span><span class="sxs-lookup"><span data-stu-id="2af74-106">This topic describes the use of expression constraints and table constraints.</span></span> <span data-ttu-id="2af74-107">Begrænsninger styrer de attributværdier, som du kan vælge, når du konfigurerer produkter til en salgsordre, et salgstilbud, en indkøbsordre eller en produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="2af74-107">Constraints control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="2af74-108">Du kan bruge udtryksbegrænsninger eller tabelbegrænsninger, afhængigt af hvordan du foretrækker at udforme begrænsninger.</span><span class="sxs-lookup"><span data-stu-id="2af74-108">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> 

<span data-ttu-id="2af74-109">Begrænsninger bruges til at styre de attributværdier, som du kan vælge, når du konfigurerer produkter til en salgsordre, et salgstilbud, en indkøbsordre eller en produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="2af74-109">Constraints are used to control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="2af74-110">Du kan bruge udtryksbegrænsninger eller tabelbegrænsninger, afhængigt af hvordan du foretrækker at udforme begrænsninger.</span><span class="sxs-lookup"><span data-stu-id="2af74-110">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span>

## <a name="what-are-expression-constraints"></a><span data-ttu-id="2af74-111">Hvad er udtryksbegrænsninger?</span><span class="sxs-lookup"><span data-stu-id="2af74-111">What are expression constraints?</span></span>
<span data-ttu-id="2af74-112">Udtryksbegrænsninger er kendetegnet ved et udtryk, der bruger de aritmetiske og booleske operatorer og funktioner.</span><span class="sxs-lookup"><span data-stu-id="2af74-112">Expression constraints are characterized by an expression that uses arithmetic and Boolean operators and functions.</span></span> <span data-ttu-id="2af74-113">En udtryksbegrænsning skrives til en bestemt komponent i en produktkonfigurationsmodel.</span><span class="sxs-lookup"><span data-stu-id="2af74-113">An expression constraint is written for a specific component in a product configuration model.</span></span> <span data-ttu-id="2af74-114">Den kan ikke genbruges af eller deles med en anden komponent.</span><span class="sxs-lookup"><span data-stu-id="2af74-114">It can't be reused by or shared with another component.</span></span> <span data-ttu-id="2af74-115">Udtryksbegrænsninger for en komponent kan dog henvise til attributter for komponentens underkomponenter.</span><span class="sxs-lookup"><span data-stu-id="2af74-115">However, the expression constraints for a component can reference attributes of the component's subcomponents.</span></span>

## <a name="what-are-table-constraints"></a><span data-ttu-id="2af74-116">Hvad er tabelbegrænsninger?</span><span class="sxs-lookup"><span data-stu-id="2af74-116">What are table constraints?</span></span>
<span data-ttu-id="2af74-117">Tabelbegrænsninger viser kombinationerne af de værdi, der er tilladt for attributter, når du konfigurerer et produkt.</span><span class="sxs-lookup"><span data-stu-id="2af74-117">Table constraints list the combinations of values that are allowed for attributes when you configure a product.</span></span> <span data-ttu-id="2af74-118">Definitioner på tabelbegrænsninger kan anvendes generisk.</span><span class="sxs-lookup"><span data-stu-id="2af74-118">Table constraint definitions can be used generically.</span></span> <span data-ttu-id="2af74-119">Når du opretter en tabelbegrænsning for en komponent i en produktkonfigurationsmodel, skal du vælge en definition på en tabelbegrænsning.</span><span class="sxs-lookup"><span data-stu-id="2af74-119">When you create a table constraint for a component in a product configuration model, you select a table constraint definition.</span></span> <span data-ttu-id="2af74-120">Hvis du vil oprette kombinationer, der er tilladt, skal du føje attributter af bestemte typer til komponenterne.</span><span class="sxs-lookup"><span data-stu-id="2af74-120">To create the combinations that are allowed, you add attributes of specific types to the components.</span></span> <span data-ttu-id="2af74-121">Hver attributtype har en bestemt værdi.</span><span class="sxs-lookup"><span data-stu-id="2af74-121">Each attribute type has a specific value.</span></span>

### <a name="example-of-a-table-constraint"></a><span data-ttu-id="2af74-122">Eksempel på tabelbegrænsning</span><span class="sxs-lookup"><span data-stu-id="2af74-122">Example of a table constraint</span></span>

<span data-ttu-id="2af74-123">Dette eksempel viser, hvordan du kan begrænse konfigurationen af en højttaler til bestemte kabinetfinishes og fronter.</span><span class="sxs-lookup"><span data-stu-id="2af74-123">This example shows how you can limit the configuration of a speaker to specific cabinet finishes and fronts.</span></span> <span data-ttu-id="2af74-124">I den første tabel vises de kabinetfinishes og fronter, der normalt er tilgængelige til konfiguration.</span><span class="sxs-lookup"><span data-stu-id="2af74-124">The first table shows the cabinet finishes and fronts that are generally available for configuration.</span></span> <span data-ttu-id="2af74-125">Værdierne er defineret for attributtyperne **Kabinetfinish** og **Frontgitter**.</span><span class="sxs-lookup"><span data-stu-id="2af74-125">The values are defined for the **Cabinet finish** and **Front grill** attribute types.</span></span>

| <span data-ttu-id="2af74-126">Attributtype</span><span class="sxs-lookup"><span data-stu-id="2af74-126">Attribute type</span></span> | <span data-ttu-id="2af74-127">Værdier</span><span class="sxs-lookup"><span data-stu-id="2af74-127">Values</span></span>                      |
|----------------|-----------------------------|
| <span data-ttu-id="2af74-128">Kabinetfinish</span><span class="sxs-lookup"><span data-stu-id="2af74-128">Cabinet finish</span></span> | <span data-ttu-id="2af74-129">Sort, egetræ, rosentræ, hvid</span><span class="sxs-lookup"><span data-stu-id="2af74-129">Black, Oak, Rosewood, White</span></span> |
| <span data-ttu-id="2af74-130">Frontgitter</span><span class="sxs-lookup"><span data-stu-id="2af74-130">Front grill</span></span>    | <span data-ttu-id="2af74-131">Sort, metal, hvid</span><span class="sxs-lookup"><span data-stu-id="2af74-131">Black, Metal, White</span></span>         |

<span data-ttu-id="2af74-132">I næste tabel vises de kombinationer, der er defineret af tabel begrænsningen **Farve og finish**.</span><span class="sxs-lookup"><span data-stu-id="2af74-132">The next table shows the combinations that are defined by the **Color and finish** table constraint.</span></span> <span data-ttu-id="2af74-133">Ved hjælp af denne tabelbegrænsning kan du konfigurere en højttaler, der har en finish i egetræ og et sort gitter, en finish i rosentræ og et hvidt gitter og så videre.</span><span class="sxs-lookup"><span data-stu-id="2af74-133">By using this table constraint, you can configure a speaker that has an oak finish and a black grill, a Rosewood finish and a white grill, and so on.</span></span>

| <span data-ttu-id="2af74-134">Afslut</span><span class="sxs-lookup"><span data-stu-id="2af74-134">Finish</span></span>         | <span data-ttu-id="2af74-135">Gitter</span><span class="sxs-lookup"><span data-stu-id="2af74-135">Grill</span></span>                       |
|----------------|-----------------------------|
| <span data-ttu-id="2af74-136">Egetræ</span><span class="sxs-lookup"><span data-stu-id="2af74-136">Oak</span></span>            | <span data-ttu-id="2af74-137">Sort</span><span class="sxs-lookup"><span data-stu-id="2af74-137">Black</span></span>                       |
| <span data-ttu-id="2af74-138">Rosentræ</span><span class="sxs-lookup"><span data-stu-id="2af74-138">Rosewood</span></span>       | <span data-ttu-id="2af74-139">Hvid</span><span class="sxs-lookup"><span data-stu-id="2af74-139">White</span></span>                       |
| <span data-ttu-id="2af74-140">Hvid</span><span class="sxs-lookup"><span data-stu-id="2af74-140">White</span></span>          | <span data-ttu-id="2af74-141">Sort</span><span class="sxs-lookup"><span data-stu-id="2af74-141">Black</span></span>                       |
| <span data-ttu-id="2af74-142">Hvid</span><span class="sxs-lookup"><span data-stu-id="2af74-142">White</span></span>          | <span data-ttu-id="2af74-143">Hvid</span><span class="sxs-lookup"><span data-stu-id="2af74-143">White</span></span>                       |
| <span data-ttu-id="2af74-144">Sort</span><span class="sxs-lookup"><span data-stu-id="2af74-144">Black</span></span>          | <span data-ttu-id="2af74-145">Sort</span><span class="sxs-lookup"><span data-stu-id="2af74-145">Black</span></span>                       |
| <span data-ttu-id="2af74-146">Sort</span><span class="sxs-lookup"><span data-stu-id="2af74-146">Black</span></span>          | <span data-ttu-id="2af74-147">Metal</span><span class="sxs-lookup"><span data-stu-id="2af74-147">Metal</span></span>                       | 

<span data-ttu-id="2af74-148">Du kan oprette systemdefinerede og brugerdefinerede tabelbegrænsninger.</span><span class="sxs-lookup"><span data-stu-id="2af74-148">You can create system-defined and user-defined table constraints.</span></span> <span data-ttu-id="2af74-149">Du kan finde flere oplysninger under [Systemdefinerede og brugerdefinerede tabelbegrænsninger](system-defined-user-defined-table-constraints.md).</span><span class="sxs-lookup"><span data-stu-id="2af74-149">For more information, see [System-defined and user-defined table constraints](system-defined-user-defined-table-constraints.md).</span></span>

## <a name="what-syntax-should-be-used-to-write-constraints"></a><span data-ttu-id="2af74-150">Hvilken syntaks skal der bruges til at skrive begrænsninger?</span><span class="sxs-lookup"><span data-stu-id="2af74-150">What syntax should be used to write constraints?</span></span>
<span data-ttu-id="2af74-151">Du skal bruge OML-syntaksen, når du skriver begrænsninger.</span><span class="sxs-lookup"><span data-stu-id="2af74-151">You must use Optimization Modeling Language (OML) syntax when you write constraints.</span></span> <span data-ttu-id="2af74-152">Systemet bruger Microsoft Solver Foundation-begrænsningsløseren til at løse begrænsningerne.</span><span class="sxs-lookup"><span data-stu-id="2af74-152">The system uses Microsoft Solver Foundation constraint solver to solve the constraints.</span></span>

## <a name="should-i-use-table-constraints-or-expression-constraints"></a><span data-ttu-id="2af74-153">Skal jeg bruge tabelbegrænsninger eller udtryksbegrænsninger?</span><span class="sxs-lookup"><span data-stu-id="2af74-153">Should I use table constraints or expression constraints?</span></span>
<span data-ttu-id="2af74-154">Du kan enten bruge udtryksbegrænsninger eller tabelbegrænsninger, afhængigt af hvordan du foretrækker at konfigurere begrænsninger.</span><span class="sxs-lookup"><span data-stu-id="2af74-154">You can use either expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> <span data-ttu-id="2af74-155">Du udformer en tabelbegrænsning som en matrix, hvorimod en udtryksbegrænsning er en enkelt sætning.</span><span class="sxs-lookup"><span data-stu-id="2af74-155">You build a table constraint as a matrix, whereas an expression constraint is an individual statement.</span></span> <span data-ttu-id="2af74-156">Når du konfigurerer et produkt, betyder det ikke noget, hvilken slags begrænsning der bruges.</span><span class="sxs-lookup"><span data-stu-id="2af74-156">When you configure a product, it doesn't matter what kind of constraint is used.</span></span> <span data-ttu-id="2af74-157">I følgende eksempel kan du se, hvordan de to metoder adskiller sig fra hinanden.</span><span class="sxs-lookup"><span data-stu-id="2af74-157">The following example shows how the two methods differ.</span></span>  

<span data-ttu-id="2af74-158">Når du konfigurerer et produkt ved hjælp af følgende begrænsnings, er disse kombinationer tilladt:</span><span class="sxs-lookup"><span data-stu-id="2af74-158">When you configure a product by using the following constraint setups, these combinations are allowed:</span></span>

-   <span data-ttu-id="2af74-159">Et produkt i farven sort og i størrelsen 30 eller 50</span><span class="sxs-lookup"><span data-stu-id="2af74-159">A product in the color Black, and in size 30 or 50</span></span>
-   <span data-ttu-id="2af74-160">Et produkt i farven rød og i størrelsen 20</span><span class="sxs-lookup"><span data-stu-id="2af74-160">A product in the color Red and in size 20</span></span>

### <a name="table-constraint-setup"></a><span data-ttu-id="2af74-161">Konfiguration af tabelbegrænsning</span><span class="sxs-lookup"><span data-stu-id="2af74-161">Table constraint setup</span></span>

| <span data-ttu-id="2af74-162">Farve</span><span class="sxs-lookup"><span data-stu-id="2af74-162">Color</span></span> | <span data-ttu-id="2af74-163">Størrelse</span><span class="sxs-lookup"><span data-stu-id="2af74-163">Size</span></span> |
|-------|------|
| <span data-ttu-id="2af74-164">Sort</span><span class="sxs-lookup"><span data-stu-id="2af74-164">Black</span></span> | <span data-ttu-id="2af74-165">30</span><span class="sxs-lookup"><span data-stu-id="2af74-165">30</span></span>   |
| <span data-ttu-id="2af74-166">Sort</span><span class="sxs-lookup"><span data-stu-id="2af74-166">Black</span></span> | <span data-ttu-id="2af74-167">50</span><span class="sxs-lookup"><span data-stu-id="2af74-167">50</span></span>   |
| <span data-ttu-id="2af74-168">Rød</span><span class="sxs-lookup"><span data-stu-id="2af74-168">Red</span></span>   | <span data-ttu-id="2af74-169">20</span><span class="sxs-lookup"><span data-stu-id="2af74-169">20</span></span>   |

### <a name="expression-constraint-setup"></a><span data-ttu-id="2af74-170">Konfiguration af udtryksbegrænsning</span><span class="sxs-lookup"><span data-stu-id="2af74-170">Expression constraint setup</span></span>

<span data-ttu-id="2af74-171">(Color == "Sort" & (size == "30" | size == "50")) | (color == "Rød" & size = "20")</span><span class="sxs-lookup"><span data-stu-id="2af74-171">(Color == "Black" & (size == "30" | size == "50")) | (color == "Red" & size = "20")</span></span>

## <a name="should-i-use-operators-or-infix-notation-when-i-write-expression-constraints"></a><span data-ttu-id="2af74-172">Skal jeg bruge operatorer eller infix-anmærkning, når jeg skriver udtryksbegrænsninger?</span><span class="sxs-lookup"><span data-stu-id="2af74-172">Should I use operators or infix notation when I write expression constraints?</span></span>
<span data-ttu-id="2af74-173">Du kan skrive en udtryksbegrænsning enten ved hjælp af de tilgængelige præfiksoperatorer eller ved hjælp af infix-anmærkningen.</span><span class="sxs-lookup"><span data-stu-id="2af74-173">You can write an expression constraint by using either the available prefix operators or infix notation.</span></span> <span data-ttu-id="2af74-174">Du kan ikke bruge infix-anmærkningen for operatorerne **Min**, **Max** og **Abs**.</span><span class="sxs-lookup"><span data-stu-id="2af74-174">For the **Min**, **Max**, and **Abs** operators, you can't use infix notation.</span></span> <span data-ttu-id="2af74-175">Disse operatorer er inkluderet som standardoperatorer i de fleste programmeringssprog.</span><span class="sxs-lookup"><span data-stu-id="2af74-175">These operators are included as standard operators in most programming languages.</span></span>

## <a name="what-operators-and-infix-notation-can-i-use-when-i-write-expression-constraints"></a><span data-ttu-id="2af74-176">Hvilke operatorer og hvilken infix-anmærkning kan jeg bruge, når jeg skriver udtryksbegrænsninger?</span><span class="sxs-lookup"><span data-stu-id="2af74-176">What operators and infix notation can I use when I write expression constraints?</span></span>
<span data-ttu-id="2af74-177">I følgende tabeller vises de operatorer og den infix-anmærkning, som du kan bruge, når du skriver en udtryksbegrænsning for en komponent i en produktkonfigurationsmodel.</span><span class="sxs-lookup"><span data-stu-id="2af74-177">The following tables list the operators and infix notation that you can use when you write an expression constraint for a component in a product configuration model.</span></span> <span data-ttu-id="2af74-178">I eksemplerne i den første tabel kan du se, hvordan du skriver et udtryk ved hjælp af infix-anmærkningen eller operatorer.</span><span class="sxs-lookup"><span data-stu-id="2af74-178">The examples in the first table show how to write an expression by using either infix notation or operators.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2af74-179">Operatør</span><span class="sxs-lookup"><span data-stu-id="2af74-179">Operator</span></span></th>
<th><span data-ttu-id="2af74-180">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="2af74-180">Description</span></span></th>
<th><span data-ttu-id="2af74-181">Syntaks</span><span class="sxs-lookup"><span data-stu-id="2af74-181">Syntax</span></span></th>
<th><span data-ttu-id="2af74-182">Eksempler</span><span class="sxs-lookup"><span data-stu-id="2af74-182">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2af74-183">Indebærer</span><span class="sxs-lookup"><span data-stu-id="2af74-183">Implies</span></span></td>
<td><span data-ttu-id="2af74-184">Dette er tilfældet, hvis den første betingelse er falsk, den anden betingelse er sand, eller begge dele.</span><span class="sxs-lookup"><span data-stu-id="2af74-184">This is true if the first condition is false, the second condition is true, or both.</span></span></td>
<td><span data-ttu-id="2af74-185">Implies[a, b], infix: a -: b</span><span class="sxs-lookup"><span data-stu-id="2af74-185">Implies[a, b], infix: a -: b</span></span></td>
<td><ul>
<li><span data-ttu-id="2af74-186"><strong>Operator:</strong> Implies[x != 0, y &gt;= 0]</span><span class="sxs-lookup"><span data-stu-id="2af74-186"><strong>Operator:</strong> Implies[x != 0, y &gt;= 0]</span></span></li>
<li><span data-ttu-id="2af74-187"><strong>Infix-anmærkning:</strong> x != 0 -: y &gt;= 0</span><span class="sxs-lookup"><span data-stu-id="2af74-187"><strong>Infix notation:</strong> x != 0 -: y &gt;= 0</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2af74-188">Og</span><span class="sxs-lookup"><span data-stu-id="2af74-188">And</span></span></td>
<td><span data-ttu-id="2af74-189">Dette gælder kun, hvis alle betingelser er opfyldt.</span><span class="sxs-lookup"><span data-stu-id="2af74-189">This is true only if all conditions are true.</span></span> <span data-ttu-id="2af74-190">Hvis antallet af betingelser er 0 (nul), returneres <strong>True</strong>.</span><span class="sxs-lookup"><span data-stu-id="2af74-190">If the number of conditions is 0 (zero), it produces <strong>True</strong>.</span></span></td>
<td><span data-ttu-id="2af74-191">And[args], infix: a &amp; b &amp; ... &amp; z</span><span class="sxs-lookup"><span data-stu-id="2af74-191">And[args], infix: a &amp; b &amp; ... &amp; z</span></span></td>
<td><ul>
<li><span data-ttu-id="2af74-192"><strong>Operator:</strong> And[x == 2, y &lt;= 2]</span><span class="sxs-lookup"><span data-stu-id="2af74-192"><strong>Operator:</strong> And[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="2af74-193"><strong>Infix-anmærkning:</strong> x == 2 &amp; y &lt;= 2</span><span class="sxs-lookup"><span data-stu-id="2af74-193"><strong>Infix notation:</strong> x == 2 &amp; y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2af74-194">Eller</span><span class="sxs-lookup"><span data-stu-id="2af74-194">Or</span></span></td>
<td><span data-ttu-id="2af74-195">Dette er tilfældet, hvis en betingelse er sand.</span><span class="sxs-lookup"><span data-stu-id="2af74-195">This is true if any condition is true.</span></span> <span data-ttu-id="2af74-196">Hvis antallet af betingelser er 0 (nul), returneres <strong>False</strong>.</span><span class="sxs-lookup"><span data-stu-id="2af74-196">If the number of conditions is 0 (zero), it produces <strong>False</strong>.</span></span></td>
<td><span data-ttu-id="2af74-197">Or[args], infix: a | b | ... | z</span><span class="sxs-lookup"><span data-stu-id="2af74-197">Or[args], infix: a | b | ... | z</span></span></td>
<td><ul>
<li><span data-ttu-id="2af74-198"><strong>Operator:</strong> Or[x == 2, y &lt;= 2]</span><span class="sxs-lookup"><span data-stu-id="2af74-198"><strong>Operator:</strong> Or[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="2af74-199"><strong>Infix-anmærkning:</strong> x == 2 | y &lt;= 2</span><span class="sxs-lookup"><span data-stu-id="2af74-199"><strong>Infix notation:</strong> x == 2 | y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2af74-200">Plus</span><span class="sxs-lookup"><span data-stu-id="2af74-200">Plus</span></span></td>
<td><span data-ttu-id="2af74-201">Dette opsummerer dens betingelser.</span><span class="sxs-lookup"><span data-stu-id="2af74-201">This sums its conditions.</span></span> <span data-ttu-id="2af74-202">Hvis antallet af betingelser er 0 (nul), returneres <strong>0</strong>.</span><span class="sxs-lookup"><span data-stu-id="2af74-202">If the number of conditions is 0 (zero), it produces <strong>0</strong>.</span></span></td>
<td><span data-ttu-id="2af74-203">Plus[args], infix: a + b + ... + z</span><span class="sxs-lookup"><span data-stu-id="2af74-203">Plus[args], infix: a + b + ... + z</span></span></td>
<td><ul>
<li><span data-ttu-id="2af74-204"><strong>Operator:</strong> Plus[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="2af74-204"><strong>Operator:</strong> Plus[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="2af74-205"><strong>Infix-anmærkning:</strong> x + y + 2 == z</span><span class="sxs-lookup"><span data-stu-id="2af74-205"><strong>Infix notation:</strong> x + y + 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2af74-206">Minus</span><span class="sxs-lookup"><span data-stu-id="2af74-206">Minus</span></span></td>
<td><span data-ttu-id="2af74-207">Derved negeres argumentet.</span><span class="sxs-lookup"><span data-stu-id="2af74-207">This negates its argument.</span></span> <span data-ttu-id="2af74-208">Det skal have præcis én betingelse.</span><span class="sxs-lookup"><span data-stu-id="2af74-208">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="2af74-209">Minus[expr], infix: -expr</span><span class="sxs-lookup"><span data-stu-id="2af74-209">Minus[expr], infix: -expr</span></span></td>
<td><ul>
<li><span data-ttu-id="2af74-210"><strong>Operator:</strong> Minus[x] == y</span><span class="sxs-lookup"><span data-stu-id="2af74-210"><strong>Operator:</strong> Minus[x] == y</span></span></li>
<li><span data-ttu-id="2af74-211"><strong>Infix-anmærkning:</strong> -x == y</span><span class="sxs-lookup"><span data-stu-id="2af74-211"><strong>Infix notation:</strong> -x == y</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2af74-212">Abs</span><span class="sxs-lookup"><span data-stu-id="2af74-212">Abs</span></span></td>
<td><span data-ttu-id="2af74-213">Dette tager den absolutte værdi af dets tilstand.</span><span class="sxs-lookup"><span data-stu-id="2af74-213">This takes the absolute value of its condition.</span></span> <span data-ttu-id="2af74-214">Det skal have præcis én betingelse.</span><span class="sxs-lookup"><span data-stu-id="2af74-214">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="2af74-215">Abs[expr]</span><span class="sxs-lookup"><span data-stu-id="2af74-215">Abs[expr]</span></span></td>
<td><span data-ttu-id="2af74-216"><strong>Operator:</strong> Abs[x]</span><span class="sxs-lookup"><span data-stu-id="2af74-216"><strong>Operator:</strong> Abs[x]</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2af74-217">Tider</span><span class="sxs-lookup"><span data-stu-id="2af74-217">Times</span></span></td>
<td><span data-ttu-id="2af74-218">Herefter tages produktet af dens betingelser.</span><span class="sxs-lookup"><span data-stu-id="2af74-218">This takes the product of its conditions.</span></span> <span data-ttu-id="2af74-219">Hvis antallet af betingelser er 0 (nul), returneres <strong>1</strong>.</span><span class="sxs-lookup"><span data-stu-id="2af74-219">If the number of conditions is 0 (zero), it produces <strong>1</strong>.</span></span></td>
<td><span data-ttu-id="2af74-220">Times[args], infix: a * b * ... * z</span><span class="sxs-lookup"><span data-stu-id="2af74-220">Times[args], infix: a * b * ... * z</span></span></td>
<td><ul>
<li><span data-ttu-id="2af74-221"><strong>Operator:</strong> Times[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="2af74-221"><strong>Operator:</strong> Times[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="2af74-222"><strong>Infix-anmærkning:</strong> x * y * 2 == z</span><span class="sxs-lookup"><span data-stu-id="2af74-222"><strong>Infix notation:</strong> x * y * 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2af74-223">Strøm</span><span class="sxs-lookup"><span data-stu-id="2af74-223">Power</span></span></td>
<td><span data-ttu-id="2af74-224">Det tager en eksponentiel.</span><span class="sxs-lookup"><span data-stu-id="2af74-224">This takes an exponential.</span></span> <span data-ttu-id="2af74-225">Det gælder eksponentiering fra højre mod venstre.</span><span class="sxs-lookup"><span data-stu-id="2af74-225">It applies exponentiation from right to left.</span></span> <span data-ttu-id="2af74-226">(Det er med andre ord en højre-association). Derfor svarer <strong>Power[a, b, c]</strong> til <strong>Power[a, Power[b, c]]</strong>.</span><span class="sxs-lookup"><span data-stu-id="2af74-226">(In other words, it's right-associative.) Therefore, <strong>Power[a, b, c]</strong> is equivalent to <strong>Power[a, Power[b, c]]</strong>.</span></span> <span data-ttu-id="2af74-227"><strong>Power</strong> kan kun bruges, hvis eksponenten er en positiv konstant.</span><span class="sxs-lookup"><span data-stu-id="2af74-227"><strong>Power</strong> can be used only if the exponent is a positive constant.</span></span></td>
<td><span data-ttu-id="2af74-228">Power[args], infix: a ^ b ^ ... ^ z</span><span class="sxs-lookup"><span data-stu-id="2af74-228">Power[args], infix: a ^ b ^ ... ^ z</span></span></td>
<td><ul>
<li><span data-ttu-id="2af74-229"><strong>Operator:</strong> Power[x, 2] == y</span><span class="sxs-lookup"><span data-stu-id="2af74-229"><strong>Operator:</strong> Power[x, 2] == y</span></span></li>
<li><span data-ttu-id="2af74-230"><strong>Infix-anmærkning:</strong> x ^ 2 == y</span><span class="sxs-lookup"><span data-stu-id="2af74-230"><strong>Infix notation:</strong> x ^ 2 == y</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2af74-231">Maks.</span><span class="sxs-lookup"><span data-stu-id="2af74-231">Max</span></span></td>
<td><span data-ttu-id="2af74-232">Dette giver den største tilstand.</span><span class="sxs-lookup"><span data-stu-id="2af74-232">This produces the largest condition.</span></span> <span data-ttu-id="2af74-233">Hvis antallet af betingelser er 0 (nul), returneres <strong>Infinity</strong>.</span><span class="sxs-lookup"><span data-stu-id="2af74-233">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="2af74-234">Max[args]</span><span class="sxs-lookup"><span data-stu-id="2af74-234">Max[args]</span></span></td>
<td><span data-ttu-id="2af74-235"><strong>Operator:</strong> Max[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="2af74-235"><strong>Operator:</strong> Max[x, y, 2] == z</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2af74-236">Min.</span><span class="sxs-lookup"><span data-stu-id="2af74-236">Min</span></span></td>
<td><span data-ttu-id="2af74-237">Dette giver den mindste tilstand.</span><span class="sxs-lookup"><span data-stu-id="2af74-237">This produces the smallest condition.</span></span> <span data-ttu-id="2af74-238">Hvis antallet af betingelser er 0 (nul), returneres <strong>Infinity</strong>.</span><span class="sxs-lookup"><span data-stu-id="2af74-238">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="2af74-239">Min[args]</span><span class="sxs-lookup"><span data-stu-id="2af74-239">Min[args]</span></span></td>
<td><span data-ttu-id="2af74-240"><strong>Operator:</strong> Min[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="2af74-240"><strong>Operator:</strong> Min[x, y, 2] == z</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2af74-241">Negeret</span><span class="sxs-lookup"><span data-stu-id="2af74-241">Not</span></span></td>
<td><span data-ttu-id="2af74-242">Dette giver den logiske inverse af tilstanden.</span><span class="sxs-lookup"><span data-stu-id="2af74-242">This produces the logical inverse of its condition.</span></span> <span data-ttu-id="2af74-243">Det skal have præcis én betingelse.</span><span class="sxs-lookup"><span data-stu-id="2af74-243">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="2af74-244">Not[expr], infix: !expr</span><span class="sxs-lookup"><span data-stu-id="2af74-244">Not[expr], infix: !expr</span></span></td>
<td><ul>
<li><span data-ttu-id="2af74-245"><strong>Operator:</strong> Not[x] &amp; Not[y == 3]</span><span class="sxs-lookup"><span data-stu-id="2af74-245"><strong>Operator:</strong> Not[x] &amp; Not[y == 3]</span></span></li>
<li><span data-ttu-id="2af74-246"><strong>Infix-anmærkning:</strong> !x!(y == 3)</span><span class="sxs-lookup"><span data-stu-id="2af74-246"><strong>Infix notation:</strong> !x!(y == 3)</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2af74-247">Eksemplerne i næste tabel viser, hvordan du skriver en infix-anmærkning.</span><span class="sxs-lookup"><span data-stu-id="2af74-247">The examples in the next table show how to write infix notation.</span></span>

| <span data-ttu-id="2af74-248">Notationen infix</span><span class="sxs-lookup"><span data-stu-id="2af74-248">Infix notation</span></span>    | <span data-ttu-id="2af74-249">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="2af74-249">Description</span></span>                                                                                   |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2af74-250">x + y + z</span><span class="sxs-lookup"><span data-stu-id="2af74-250">x + y + z</span></span>         | <span data-ttu-id="2af74-251">Tilføjelse</span><span class="sxs-lookup"><span data-stu-id="2af74-251">Addition</span></span>                                                                                      |
| <span data-ttu-id="2af74-252">x \* y \* z</span><span class="sxs-lookup"><span data-stu-id="2af74-252">x \* y \* z</span></span>       | <span data-ttu-id="2af74-253">Multiplikation</span><span class="sxs-lookup"><span data-stu-id="2af74-253">Multiplication</span></span>                                                                                |
| <span data-ttu-id="2af74-254">x - y</span><span class="sxs-lookup"><span data-stu-id="2af74-254">x - y</span></span>             | <span data-ttu-id="2af74-255">Binær subtraktion oversættes på samme måde som binær addition, hvor der er et negativt sekund.</span><span class="sxs-lookup"><span data-stu-id="2af74-255">Binary subtraction is translated the same as binary addition where there is a negated second.</span></span> |
| <span data-ttu-id="2af74-256">x ^ y ^ z</span><span class="sxs-lookup"><span data-stu-id="2af74-256">x ^ y ^ z</span></span>         | <span data-ttu-id="2af74-257">Eksponentiering, der har en højre-association</span><span class="sxs-lookup"><span data-stu-id="2af74-257">Exponentiation that has right associativity</span></span>                                                   |
| <span data-ttu-id="2af74-258">!x</span><span class="sxs-lookup"><span data-stu-id="2af74-258">!x</span></span>                | <span data-ttu-id="2af74-259">Boolesk ikke</span><span class="sxs-lookup"><span data-stu-id="2af74-259">Boolean not</span></span>                                                                                   |
| <span data-ttu-id="2af74-260">x -: y</span><span class="sxs-lookup"><span data-stu-id="2af74-260">x -: y</span></span>            | <span data-ttu-id="2af74-261">Boolesk virkning</span><span class="sxs-lookup"><span data-stu-id="2af74-261">Boolean implication</span></span>                                                                           |
| <span data-ttu-id="2af74-262">x</span><span class="sxs-lookup"><span data-stu-id="2af74-262">x</span></span> | <span data-ttu-id="2af74-263">y</span><span class="sxs-lookup"><span data-stu-id="2af74-263">y</span></span> | <span data-ttu-id="2af74-264">z</span><span class="sxs-lookup"><span data-stu-id="2af74-264">z</span></span>         | <span data-ttu-id="2af74-265">Boolsk eller</span><span class="sxs-lookup"><span data-stu-id="2af74-265">Boolean or</span></span>                                                                                    |
| <span data-ttu-id="2af74-266">x & y & z</span><span class="sxs-lookup"><span data-stu-id="2af74-266">x & y & z</span></span>         | <span data-ttu-id="2af74-267">Boolesk og</span><span class="sxs-lookup"><span data-stu-id="2af74-267">Boolean and</span></span>                                                                                   |
| <span data-ttu-id="2af74-268">x == y == z</span><span class="sxs-lookup"><span data-stu-id="2af74-268">x == y == z</span></span>       | <span data-ttu-id="2af74-269">Lig med</span><span class="sxs-lookup"><span data-stu-id="2af74-269">Equality</span></span>                                                                                      |
| <span data-ttu-id="2af74-270">x != y != z</span><span class="sxs-lookup"><span data-stu-id="2af74-270">x != y != z</span></span>       | <span data-ttu-id="2af74-271">Bestemt</span><span class="sxs-lookup"><span data-stu-id="2af74-271">Distinct</span></span>                                                                                      |
| <span data-ttu-id="2af74-272">x &lt; y &lt; z</span><span class="sxs-lookup"><span data-stu-id="2af74-272">x &lt; y &lt; z</span></span>   | <span data-ttu-id="2af74-273">Mindre end</span><span class="sxs-lookup"><span data-stu-id="2af74-273">Less than</span></span>                                                                                     |
| <span data-ttu-id="2af74-274">x &gt; y &gt; z</span><span class="sxs-lookup"><span data-stu-id="2af74-274">x &gt; y &gt; z</span></span>   | <span data-ttu-id="2af74-275">Større end</span><span class="sxs-lookup"><span data-stu-id="2af74-275">Greater than</span></span>                                                                                  |
| <span data-ttu-id="2af74-276">x &lt;= y &lt;= z</span><span class="sxs-lookup"><span data-stu-id="2af74-276">x &lt;= y &lt;= z</span></span> | <span data-ttu-id="2af74-277">Mindre end eller lig med</span><span class="sxs-lookup"><span data-stu-id="2af74-277">Less than or equal to</span></span>                                                                         |
| <span data-ttu-id="2af74-278">x &gt;= y &gt;= z</span><span class="sxs-lookup"><span data-stu-id="2af74-278">x &gt;= y &gt;= z</span></span> | <span data-ttu-id="2af74-279">Større end eller lig med</span><span class="sxs-lookup"><span data-stu-id="2af74-279">Greater than or equal to</span></span>                                                                      |
| <span data-ttu-id="2af74-280">(x)</span><span class="sxs-lookup"><span data-stu-id="2af74-280">(x)</span></span>               | <span data-ttu-id="2af74-281">Parentes tilsidesætter standardprioritering.</span><span class="sxs-lookup"><span data-stu-id="2af74-281">Parentheses override default precedence.</span></span>                                                      |

## <a name="why-arent-my-expression-constraints-validated-correctly"></a><span data-ttu-id="2af74-282">Hvorfor valideres mine udtryksbegrænsninger ikke korrekt?</span><span class="sxs-lookup"><span data-stu-id="2af74-282">Why aren't my expression constraints validated correctly?</span></span>
<span data-ttu-id="2af74-283">Du kan ikke bruge et reserveret nøgleord som problemløsernavn til attributter, komponenter og underkomponenter i en produktkonfigurationsmodel.</span><span class="sxs-lookup"><span data-stu-id="2af74-283">You can't use reserved keywords as solver names for attributes, components, or subcomponents in a product configuration model.</span></span> <span data-ttu-id="2af74-284">Her er en liste over de reserverede nøgleord, som du kan bruge:</span><span class="sxs-lookup"><span data-stu-id="2af74-284">Here is a list of the reserved keywords that you can't use:</span></span>

-   <span data-ttu-id="2af74-285">Loft</span><span class="sxs-lookup"><span data-stu-id="2af74-285">Ceiling</span></span>
-   <span data-ttu-id="2af74-286">Element</span><span class="sxs-lookup"><span data-stu-id="2af74-286">Element</span></span>
-   <span data-ttu-id="2af74-287">Lig med</span><span class="sxs-lookup"><span data-stu-id="2af74-287">Equal</span></span>
-   <span data-ttu-id="2af74-288">Etage</span><span class="sxs-lookup"><span data-stu-id="2af74-288">Floor</span></span>
-   <span data-ttu-id="2af74-289">Hvis</span><span class="sxs-lookup"><span data-stu-id="2af74-289">If</span></span>
-   <span data-ttu-id="2af74-290">Mindre end</span><span class="sxs-lookup"><span data-stu-id="2af74-290">Less</span></span>
-   <span data-ttu-id="2af74-291">Større end</span><span class="sxs-lookup"><span data-stu-id="2af74-291">Greater</span></span>
-   <span data-ttu-id="2af74-292">Indebærer</span><span class="sxs-lookup"><span data-stu-id="2af74-292">Implies</span></span>
-   <span data-ttu-id="2af74-293">Logfil</span><span class="sxs-lookup"><span data-stu-id="2af74-293">Log</span></span>
-   <span data-ttu-id="2af74-294">Maks</span><span class="sxs-lookup"><span data-stu-id="2af74-294">Max</span></span>
-   <span data-ttu-id="2af74-295">Min.</span><span class="sxs-lookup"><span data-stu-id="2af74-295">Min</span></span>
-   <span data-ttu-id="2af74-296">Minus</span><span class="sxs-lookup"><span data-stu-id="2af74-296">Minus</span></span>
-   <span data-ttu-id="2af74-297">Plus</span><span class="sxs-lookup"><span data-stu-id="2af74-297">Plus</span></span>
-   <span data-ttu-id="2af74-298">Strøm</span><span class="sxs-lookup"><span data-stu-id="2af74-298">Power</span></span>
-   <span data-ttu-id="2af74-299">Tider</span><span class="sxs-lookup"><span data-stu-id="2af74-299">Times</span></span>
-   <span data-ttu-id="2af74-300">Slot</span><span class="sxs-lookup"><span data-stu-id="2af74-300">Slot</span></span>
-   <span data-ttu-id="2af74-301">Model</span><span class="sxs-lookup"><span data-stu-id="2af74-301">Model</span></span>
-   <span data-ttu-id="2af74-302">Beslutning</span><span class="sxs-lookup"><span data-stu-id="2af74-302">Decision</span></span>
-   <span data-ttu-id="2af74-303">Mål</span><span class="sxs-lookup"><span data-stu-id="2af74-303">Goal</span></span>


<a name="see-also"></a><span data-ttu-id="2af74-304">Se også</span><span class="sxs-lookup"><span data-stu-id="2af74-304">See also</span></span>
--------

<span data-ttu-id="2af74-305">[Oprette en udtryksbegrænsning (opgave guide)(/dynamics365/unified-operations/supply-chain/pim/tasks/add-expression-constraint-product-configuration-model)</span><span class="sxs-lookup"><span data-stu-id="2af74-305">[Create an expression constraint (Task guide)(/dynamics365/unified-operations/supply-chain/pim/tasks/add-expression-constraint-product-configuration-model)</span></span>

[<span data-ttu-id="2af74-306">Føje en beregning til en produktkonfigurationsmodel (Opgaveguide)</span><span class="sxs-lookup"><span data-stu-id="2af74-306">Add a calculation to a product configuration model (Task guide)</span></span>](/dynamics365/unified-operations/supply-chain/pim/tasks/add-calculation-product-configuration-model)




