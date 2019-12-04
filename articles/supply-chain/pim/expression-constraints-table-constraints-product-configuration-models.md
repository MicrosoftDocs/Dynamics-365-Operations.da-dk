---
title: Udtryksbegrænsninger og tabelbegrænsninger i produktkonfigurationsmodeller
description: I dette emne beskrives brugen af udtryksbegrænsninger og tabelbegrænsninger. Begrænsninger styrer de attributværdier, som du kan vælge, når du konfigurerer produkter til en salgsordre, et salgstilbud, en indkøbsordre eller en produktionsordre. Du kan bruge udtryksbegrænsninger eller tabelbegrænsninger, afhængigt af hvordan du foretrækker at udforme begrænsninger.
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCGlobalTableConstraintEdit, PCProductConfigurationModelDetails, PCTableConstraintAttachAttributeTree, PCTableConstraintDefinition
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 53111
ms.assetid: 5c12b1f2-eb89-4648-a755-de412f2eadd6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 91eb5f166633f5be0ad68c039d3e538e4060ea0b
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/18/2019
ms.locfileid: "2815059"
---
# <a name="expression-constraints-and-table-constraints-in-product-configuration-models"></a><span data-ttu-id="0f247-105">Udtryksbegrænsninger og tabelbegrænsninger i produktkonfigurationsmodeller</span><span class="sxs-lookup"><span data-stu-id="0f247-105">Expression constraints and table constraints in product configuration models</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0f247-106">I dette emne beskrives brugen af udtryksbegrænsninger og tabelbegrænsninger.</span><span class="sxs-lookup"><span data-stu-id="0f247-106">This topic describes the use of expression constraints and table constraints.</span></span> <span data-ttu-id="0f247-107">Begrænsninger styrer de attributværdier, som du kan vælge, når du konfigurerer produkter til en salgsordre, et salgstilbud, en indkøbsordre eller en produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="0f247-107">Constraints control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="0f247-108">Du kan bruge udtryksbegrænsninger eller tabelbegrænsninger, afhængigt af hvordan du foretrækker at udforme begrænsninger.</span><span class="sxs-lookup"><span data-stu-id="0f247-108">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> 

<span data-ttu-id="0f247-109">Begrænsninger bruges til at styre de attributværdier, som du kan vælge, når du konfigurerer produkter til en salgsordre, et salgstilbud, en indkøbsordre eller en produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="0f247-109">Constraints are used to control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="0f247-110">Du kan bruge udtryksbegrænsninger eller tabelbegrænsninger, afhængigt af hvordan du foretrækker at udforme begrænsninger.</span><span class="sxs-lookup"><span data-stu-id="0f247-110">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span>

## <a name="what-are-expression-constraints"></a><span data-ttu-id="0f247-111">Hvad er udtryksbegrænsninger?</span><span class="sxs-lookup"><span data-stu-id="0f247-111">What are expression constraints?</span></span>
<span data-ttu-id="0f247-112">Udtryksbegrænsninger er kendetegnet ved et udtryk, der bruger de aritmetiske og booleske operatorer og funktioner.</span><span class="sxs-lookup"><span data-stu-id="0f247-112">Expression constraints are characterized by an expression that uses arithmetic and Boolean operators and functions.</span></span> <span data-ttu-id="0f247-113">En udtryksbegrænsning skrives til en bestemt komponent i en produktkonfigurationsmodel.</span><span class="sxs-lookup"><span data-stu-id="0f247-113">An expression constraint is written for a specific component in a product configuration model.</span></span> <span data-ttu-id="0f247-114">Den kan ikke genbruges af eller deles med en anden komponent.</span><span class="sxs-lookup"><span data-stu-id="0f247-114">It can't be reused by or shared with another component.</span></span> <span data-ttu-id="0f247-115">Udtryksbegrænsninger for en komponent kan dog henvise til attributter for komponentens underkomponenter.</span><span class="sxs-lookup"><span data-stu-id="0f247-115">However, the expression constraints for a component can reference attributes of the component's subcomponents.</span></span>

## <a name="what-are-table-constraints"></a><span data-ttu-id="0f247-116">Hvad er tabelbegrænsninger?</span><span class="sxs-lookup"><span data-stu-id="0f247-116">What are table constraints?</span></span>
<span data-ttu-id="0f247-117">Tabelbegrænsninger viser kombinationerne af de værdi, der er tilladt for attributter, når du konfigurerer et produkt.</span><span class="sxs-lookup"><span data-stu-id="0f247-117">Table constraints list the combinations of values that are allowed for attributes when you configure a product.</span></span> <span data-ttu-id="0f247-118">Definitioner på tabelbegrænsninger kan anvendes generisk.</span><span class="sxs-lookup"><span data-stu-id="0f247-118">Table constraint definitions can be used generically.</span></span> <span data-ttu-id="0f247-119">Når du opretter en tabelbegrænsning for en komponent i en produktkonfigurationsmodel, skal du vælge en definition på en tabelbegrænsning.</span><span class="sxs-lookup"><span data-stu-id="0f247-119">When you create a table constraint for a component in a product configuration model, you select a table constraint definition.</span></span> <span data-ttu-id="0f247-120">Hvis du vil oprette kombinationer, der er tilladt, skal du føje attributter af bestemte typer til komponenterne.</span><span class="sxs-lookup"><span data-stu-id="0f247-120">To create the combinations that are allowed, you add attributes of specific types to the components.</span></span> <span data-ttu-id="0f247-121">Hver attributtype har en bestemt værdi.</span><span class="sxs-lookup"><span data-stu-id="0f247-121">Each attribute type has a specific value.</span></span>

### <a name="example-of-a-table-constraint"></a><span data-ttu-id="0f247-122">Eksempel på tabelbegrænsning</span><span class="sxs-lookup"><span data-stu-id="0f247-122">Example of a table constraint</span></span>

<span data-ttu-id="0f247-123">Dette eksempel viser, hvordan du kan begrænse konfigurationen af en højttaler til bestemte kabinetfinishes og fronter.</span><span class="sxs-lookup"><span data-stu-id="0f247-123">This example shows how you can limit the configuration of a speaker to specific cabinet finishes and fronts.</span></span> <span data-ttu-id="0f247-124">I den første tabel vises de kabinetfinishes og fronter, der normalt er tilgængelige til konfiguration.</span><span class="sxs-lookup"><span data-stu-id="0f247-124">The first table shows the cabinet finishes and fronts that are generally available for configuration.</span></span> <span data-ttu-id="0f247-125">Værdierne er defineret for attributtyperne **Kabinetfinish** og **Frontgitter**.</span><span class="sxs-lookup"><span data-stu-id="0f247-125">The values are defined for the **Cabinet finish** and **Front grill** attribute types.</span></span>

| <span data-ttu-id="0f247-126">Attributtype</span><span class="sxs-lookup"><span data-stu-id="0f247-126">Attribute type</span></span> | <span data-ttu-id="0f247-127">Værdier</span><span class="sxs-lookup"><span data-stu-id="0f247-127">Values</span></span>                      |
|----------------|-----------------------------|
| <span data-ttu-id="0f247-128">Kabinetfinish</span><span class="sxs-lookup"><span data-stu-id="0f247-128">Cabinet finish</span></span> | <span data-ttu-id="0f247-129">Sort, egetræ, rosentræ, hvid</span><span class="sxs-lookup"><span data-stu-id="0f247-129">Black, Oak, Rosewood, White</span></span> |
| <span data-ttu-id="0f247-130">Frontgitter</span><span class="sxs-lookup"><span data-stu-id="0f247-130">Front grill</span></span>    | <span data-ttu-id="0f247-131">Sort, metal, hvid</span><span class="sxs-lookup"><span data-stu-id="0f247-131">Black, Metal, White</span></span>         |

<span data-ttu-id="0f247-132">I næste tabel vises de kombinationer, der er defineret af tabel begrænsningen **Farve og finish**.</span><span class="sxs-lookup"><span data-stu-id="0f247-132">The next table shows the combinations that are defined by the **Color and finish** table constraint.</span></span> <span data-ttu-id="0f247-133">Ved hjælp af denne tabelbegrænsning kan du konfigurere en højttaler, der har en finish i egetræ og et sort gitter, en finish i rosentræ og et hvidt gitter og så videre.</span><span class="sxs-lookup"><span data-stu-id="0f247-133">By using this table constraint, you can configure a speaker that has an oak finish and a black grill, a Rosewood finish and a white grill, and so on.</span></span>

| <span data-ttu-id="0f247-134">Afslut</span><span class="sxs-lookup"><span data-stu-id="0f247-134">Finish</span></span>         | <span data-ttu-id="0f247-135">Gitter</span><span class="sxs-lookup"><span data-stu-id="0f247-135">Grill</span></span>                       |
|----------------|-----------------------------|
| <span data-ttu-id="0f247-136">Egetræ</span><span class="sxs-lookup"><span data-stu-id="0f247-136">Oak</span></span>            | <span data-ttu-id="0f247-137">Sort</span><span class="sxs-lookup"><span data-stu-id="0f247-137">Black</span></span>                       |
| <span data-ttu-id="0f247-138">Rosentræ</span><span class="sxs-lookup"><span data-stu-id="0f247-138">Rosewood</span></span>       | <span data-ttu-id="0f247-139">Hvid</span><span class="sxs-lookup"><span data-stu-id="0f247-139">White</span></span>                       |
| <span data-ttu-id="0f247-140">Hvid</span><span class="sxs-lookup"><span data-stu-id="0f247-140">White</span></span>          | <span data-ttu-id="0f247-141">Sort</span><span class="sxs-lookup"><span data-stu-id="0f247-141">Black</span></span>                       |
| <span data-ttu-id="0f247-142">Hvid</span><span class="sxs-lookup"><span data-stu-id="0f247-142">White</span></span>          | <span data-ttu-id="0f247-143">Hvid</span><span class="sxs-lookup"><span data-stu-id="0f247-143">White</span></span>                       |
| <span data-ttu-id="0f247-144">Sort</span><span class="sxs-lookup"><span data-stu-id="0f247-144">Black</span></span>          | <span data-ttu-id="0f247-145">Sort</span><span class="sxs-lookup"><span data-stu-id="0f247-145">Black</span></span>                       |
| <span data-ttu-id="0f247-146">Sort</span><span class="sxs-lookup"><span data-stu-id="0f247-146">Black</span></span>          | <span data-ttu-id="0f247-147">Metal</span><span class="sxs-lookup"><span data-stu-id="0f247-147">Metal</span></span>                       | 

<span data-ttu-id="0f247-148">Du kan oprette systemdefinerede og brugerdefinerede tabelbegrænsninger.</span><span class="sxs-lookup"><span data-stu-id="0f247-148">You can create system-defined and user-defined table constraints.</span></span> <span data-ttu-id="0f247-149">Du kan finde flere oplysninger under [Systemdefinerede og brugerdefinerede tabelbegrænsninger](system-defined-user-defined-table-constraints.md).</span><span class="sxs-lookup"><span data-stu-id="0f247-149">For more information, see [System-defined and user-defined table constraints](system-defined-user-defined-table-constraints.md).</span></span>

## <a name="what-syntax-should-be-used-to-write-constraints"></a><span data-ttu-id="0f247-150">Hvilken syntaks skal der bruges til at skrive begrænsninger?</span><span class="sxs-lookup"><span data-stu-id="0f247-150">What syntax should be used to write constraints?</span></span>
<span data-ttu-id="0f247-151">Du skal bruge OML-syntaksen, når du skriver begrænsninger.</span><span class="sxs-lookup"><span data-stu-id="0f247-151">You must use Optimization Modeling Language (OML) syntax when you write constraints.</span></span> <span data-ttu-id="0f247-152">Systemet bruger Microsoft Solver Foundation-begrænsningsløseren til at løse begrænsningerne.</span><span class="sxs-lookup"><span data-stu-id="0f247-152">The system uses Microsoft Solver Foundation constraint solver to solve the constraints.</span></span>

## <a name="should-i-use-table-constraints-or-expression-constraints"></a><span data-ttu-id="0f247-153">Skal jeg bruge tabelbegrænsninger eller udtryksbegrænsninger?</span><span class="sxs-lookup"><span data-stu-id="0f247-153">Should I use table constraints or expression constraints?</span></span>
<span data-ttu-id="0f247-154">Du kan enten bruge udtryksbegrænsninger eller tabelbegrænsninger, afhængigt af hvordan du foretrækker at konfigurere begrænsninger.</span><span class="sxs-lookup"><span data-stu-id="0f247-154">You can use either expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> <span data-ttu-id="0f247-155">Du udformer en tabelbegrænsning som en matrix, hvorimod en udtryksbegrænsning er en enkelt sætning.</span><span class="sxs-lookup"><span data-stu-id="0f247-155">You build a table constraint as a matrix, whereas an expression constraint is an individual statement.</span></span> <span data-ttu-id="0f247-156">Når du konfigurerer et produkt, betyder det ikke noget, hvilken slags begrænsning der bruges.</span><span class="sxs-lookup"><span data-stu-id="0f247-156">When you configure a product, it doesn't matter what kind of constraint is used.</span></span> <span data-ttu-id="0f247-157">I følgende eksempel kan du se, hvordan de to metoder adskiller sig fra hinanden.</span><span class="sxs-lookup"><span data-stu-id="0f247-157">The following example shows how the two methods differ.</span></span>  

<span data-ttu-id="0f247-158">Når du konfigurerer et produkt ved hjælp af følgende begrænsnings, er disse kombinationer tilladt:</span><span class="sxs-lookup"><span data-stu-id="0f247-158">When you configure a product by using the following constraint setups, these combinations are allowed:</span></span>

-   <span data-ttu-id="0f247-159">Et produkt i farven sort og i størrelsen 30 eller 50</span><span class="sxs-lookup"><span data-stu-id="0f247-159">A product in the color Black, and in size 30 or 50</span></span>
-   <span data-ttu-id="0f247-160">Et produkt i farven rød og i størrelsen 20</span><span class="sxs-lookup"><span data-stu-id="0f247-160">A product in the color Red and in size 20</span></span>

### <a name="table-constraint-setup"></a><span data-ttu-id="0f247-161">Konfiguration af tabelbegrænsning</span><span class="sxs-lookup"><span data-stu-id="0f247-161">Table constraint setup</span></span>

| <span data-ttu-id="0f247-162">Farve</span><span class="sxs-lookup"><span data-stu-id="0f247-162">Color</span></span> | <span data-ttu-id="0f247-163">Størrelse</span><span class="sxs-lookup"><span data-stu-id="0f247-163">Size</span></span> |
|-------|------|
| <span data-ttu-id="0f247-164">Sort</span><span class="sxs-lookup"><span data-stu-id="0f247-164">Black</span></span> | <span data-ttu-id="0f247-165">30</span><span class="sxs-lookup"><span data-stu-id="0f247-165">30</span></span>   |
| <span data-ttu-id="0f247-166">Sort</span><span class="sxs-lookup"><span data-stu-id="0f247-166">Black</span></span> | <span data-ttu-id="0f247-167">50</span><span class="sxs-lookup"><span data-stu-id="0f247-167">50</span></span>   |
| <span data-ttu-id="0f247-168">Rød</span><span class="sxs-lookup"><span data-stu-id="0f247-168">Red</span></span>   | <span data-ttu-id="0f247-169">20</span><span class="sxs-lookup"><span data-stu-id="0f247-169">20</span></span>   |

### <a name="expression-constraint-setup"></a><span data-ttu-id="0f247-170">Konfiguration af udtryksbegrænsning</span><span class="sxs-lookup"><span data-stu-id="0f247-170">Expression constraint setup</span></span>

<span data-ttu-id="0f247-171">(Color == "Sort" & (size == "30" | size == "50")) | (color == "Rød" & size = "20")</span><span class="sxs-lookup"><span data-stu-id="0f247-171">(Color == "Black" & (size == "30" | size == "50")) | (color == "Red" & size = "20")</span></span>

## <a name="should-i-use-operators-or-infix-notation-when-i-write-expression-constraints"></a><span data-ttu-id="0f247-172">Skal jeg bruge operatorer eller infix-anmærkning, når jeg skriver udtryksbegrænsninger?</span><span class="sxs-lookup"><span data-stu-id="0f247-172">Should I use operators or infix notation when I write expression constraints?</span></span>
<span data-ttu-id="0f247-173">Du kan skrive en udtryksbegrænsning enten ved hjælp af de tilgængelige præfiksoperatorer eller ved hjælp af infix-anmærkningen.</span><span class="sxs-lookup"><span data-stu-id="0f247-173">You can write an expression constraint by using either the available prefix operators or infix notation.</span></span> <span data-ttu-id="0f247-174">Du kan ikke bruge infix-anmærkningen for operatorerne **Min**, **Max** og **Abs**.</span><span class="sxs-lookup"><span data-stu-id="0f247-174">For the **Min**, **Max**, and **Abs** operators, you can't use infix notation.</span></span> <span data-ttu-id="0f247-175">Disse operatorer er inkluderet som standardoperatorer i de fleste programmeringssprog.</span><span class="sxs-lookup"><span data-stu-id="0f247-175">These operators are included as standard operators in most programming languages.</span></span>

## <a name="what-operators-and-infix-notation-can-i-use-when-i-write-expression-constraints"></a><span data-ttu-id="0f247-176">Hvilke operatorer og hvilken infix-anmærkning kan jeg bruge, når jeg skriver udtryksbegrænsninger?</span><span class="sxs-lookup"><span data-stu-id="0f247-176">What operators and infix notation can I use when I write expression constraints?</span></span>
<span data-ttu-id="0f247-177">I følgende tabeller vises de operatorer og den infix-anmærkning, som du kan bruge, når du skriver en udtryksbegrænsning for en komponent i en produktkonfigurationsmodel.</span><span class="sxs-lookup"><span data-stu-id="0f247-177">The following tables list the operators and infix notation that you can use when you write an expression constraint for a component in a product configuration model.</span></span> <span data-ttu-id="0f247-178">I eksemplerne i den første tabel kan du se, hvordan du skriver et udtryk ved hjælp af infix-anmærkningen eller operatorer.</span><span class="sxs-lookup"><span data-stu-id="0f247-178">The examples in the first table show how to write an expression by using either infix notation or operators.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0f247-179">Operatør</span><span class="sxs-lookup"><span data-stu-id="0f247-179">Operator</span></span></th>
<th><span data-ttu-id="0f247-180">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="0f247-180">Description</span></span></th>
<th><span data-ttu-id="0f247-181">Syntaks</span><span class="sxs-lookup"><span data-stu-id="0f247-181">Syntax</span></span></th>
<th><span data-ttu-id="0f247-182">Eksempler</span><span class="sxs-lookup"><span data-stu-id="0f247-182">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0f247-183">Indebærer</span><span class="sxs-lookup"><span data-stu-id="0f247-183">Implies</span></span></td>
<td><span data-ttu-id="0f247-184">Dette er tilfældet, hvis den første betingelse er falsk, den anden betingelse er sand, eller begge dele.</span><span class="sxs-lookup"><span data-stu-id="0f247-184">This is true if the first condition is false, the second condition is true, or both.</span></span></td>
<td><span data-ttu-id="0f247-185">Implies[a, b], infix: a -: b</span><span class="sxs-lookup"><span data-stu-id="0f247-185">Implies[a, b], infix: a -: b</span></span></td>
<td><ul>
<li><span data-ttu-id="0f247-186"><strong>Operator:</strong> Implies[x != 0, y &gt;= 0]</span><span class="sxs-lookup"><span data-stu-id="0f247-186"><strong>Operator:</strong> Implies[x != 0, y &gt;= 0]</span></span></li>
<li><span data-ttu-id="0f247-187"><strong>Infix-anmærkning:</strong> x != 0 -: y &gt;= 0</span><span class="sxs-lookup"><span data-stu-id="0f247-187"><strong>Infix notation:</strong> x != 0 -: y &gt;= 0</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0f247-188">Og</span><span class="sxs-lookup"><span data-stu-id="0f247-188">And</span></span></td>
<td><span data-ttu-id="0f247-189">Dette gælder kun, hvis alle betingelser er opfyldt.</span><span class="sxs-lookup"><span data-stu-id="0f247-189">This is true only if all conditions are true.</span></span> <span data-ttu-id="0f247-190">Hvis antallet af betingelser er 0 (nul), returneres <strong>True</strong>.</span><span class="sxs-lookup"><span data-stu-id="0f247-190">If the number of conditions is 0 (zero), it produces <strong>True</strong>.</span></span></td>
<td><span data-ttu-id="0f247-191">And[args], infix: a &amp; b &amp; ... &amp; z</span><span class="sxs-lookup"><span data-stu-id="0f247-191">And[args], infix: a &amp; b &amp; ... &amp; z</span></span></td>
<td><ul>
<li><span data-ttu-id="0f247-192"><strong>Operator:</strong> And[x == 2, y &lt;= 2]</span><span class="sxs-lookup"><span data-stu-id="0f247-192"><strong>Operator:</strong> And[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="0f247-193"><strong>Infix-anmærkning:</strong> x == 2 &amp; y &lt;= 2</span><span class="sxs-lookup"><span data-stu-id="0f247-193"><strong>Infix notation:</strong> x == 2 &amp; y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0f247-194">Eller</span><span class="sxs-lookup"><span data-stu-id="0f247-194">Or</span></span></td>
<td><span data-ttu-id="0f247-195">Dette er tilfældet, hvis en betingelse er sand.</span><span class="sxs-lookup"><span data-stu-id="0f247-195">This is true if any condition is true.</span></span> <span data-ttu-id="0f247-196">Hvis antallet af betingelser er 0 (nul), returneres <strong>False</strong>.</span><span class="sxs-lookup"><span data-stu-id="0f247-196">If the number of conditions is 0 (zero), it produces <strong>False</strong>.</span></span></td>
<td><span data-ttu-id="0f247-197">Or[args], infix: a | b | ... | z</span><span class="sxs-lookup"><span data-stu-id="0f247-197">Or[args], infix: a | b | ... | z</span></span></td>
<td><ul>
<li><span data-ttu-id="0f247-198"><strong>Operator:</strong> Or[x == 2, y &lt;= 2]</span><span class="sxs-lookup"><span data-stu-id="0f247-198"><strong>Operator:</strong> Or[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="0f247-199"><strong>Infix-anmærkning:</strong> x == 2 | y &lt;= 2</span><span class="sxs-lookup"><span data-stu-id="0f247-199"><strong>Infix notation:</strong> x == 2 | y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0f247-200">Plus</span><span class="sxs-lookup"><span data-stu-id="0f247-200">Plus</span></span></td>
<td><span data-ttu-id="0f247-201">Dette opsummerer dens betingelser.</span><span class="sxs-lookup"><span data-stu-id="0f247-201">This sums its conditions.</span></span> <span data-ttu-id="0f247-202">Hvis antallet af betingelser er 0 (nul), returneres <strong>0</strong>.</span><span class="sxs-lookup"><span data-stu-id="0f247-202">If the number of conditions is 0 (zero), it produces <strong>0</strong>.</span></span></td>
<td><span data-ttu-id="0f247-203">Plus[args], infix: a + b + ... + z</span><span class="sxs-lookup"><span data-stu-id="0f247-203">Plus[args], infix: a + b + ... + z</span></span></td>
<td><ul>
<li><span data-ttu-id="0f247-204"><strong>Operator:</strong> Plus[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="0f247-204"><strong>Operator:</strong> Plus[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="0f247-205"><strong>Infix-anmærkning:</strong> x + y + 2 == z</span><span class="sxs-lookup"><span data-stu-id="0f247-205"><strong>Infix notation:</strong> x + y + 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0f247-206">Minus</span><span class="sxs-lookup"><span data-stu-id="0f247-206">Minus</span></span></td>
<td><span data-ttu-id="0f247-207">Derved negeres argumentet.</span><span class="sxs-lookup"><span data-stu-id="0f247-207">This negates its argument.</span></span> <span data-ttu-id="0f247-208">Det skal have præcis én betingelse.</span><span class="sxs-lookup"><span data-stu-id="0f247-208">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="0f247-209">Minus[expr], infix: -expr</span><span class="sxs-lookup"><span data-stu-id="0f247-209">Minus[expr], infix: -expr</span></span></td>
<td><ul>
<li><span data-ttu-id="0f247-210"><strong>Operator:</strong> Minus[x] == y</span><span class="sxs-lookup"><span data-stu-id="0f247-210"><strong>Operator:</strong> Minus[x] == y</span></span></li>
<li><span data-ttu-id="0f247-211"><strong>Infix-anmærkning:</strong> -x == y</span><span class="sxs-lookup"><span data-stu-id="0f247-211"><strong>Infix notation:</strong> -x == y</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0f247-212">Abs</span><span class="sxs-lookup"><span data-stu-id="0f247-212">Abs</span></span></td>
<td><span data-ttu-id="0f247-213">Dette tager den absolutte værdi af dets tilstand.</span><span class="sxs-lookup"><span data-stu-id="0f247-213">This takes the absolute value of its condition.</span></span> <span data-ttu-id="0f247-214">Det skal have præcis én betingelse.</span><span class="sxs-lookup"><span data-stu-id="0f247-214">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="0f247-215">Abs[expr]</span><span class="sxs-lookup"><span data-stu-id="0f247-215">Abs[expr]</span></span></td>
<td><span data-ttu-id="0f247-216"><strong>Operator:</strong> Abs[x]</span><span class="sxs-lookup"><span data-stu-id="0f247-216"><strong>Operator:</strong> Abs[x]</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0f247-217">Tider</span><span class="sxs-lookup"><span data-stu-id="0f247-217">Times</span></span></td>
<td><span data-ttu-id="0f247-218">Herefter tages produktet af dens betingelser.</span><span class="sxs-lookup"><span data-stu-id="0f247-218">This takes the product of its conditions.</span></span> <span data-ttu-id="0f247-219">Hvis antallet af betingelser er 0 (nul), returneres <strong>1</strong>.</span><span class="sxs-lookup"><span data-stu-id="0f247-219">If the number of conditions is 0 (zero), it produces <strong>1</strong>.</span></span></td>
<td><span data-ttu-id="0f247-220">Times[args], infix: a \* b \* ... \* z</span><span class="sxs-lookup"><span data-stu-id="0f247-220">Times[args], infix: a \* b \* ... \* z</span></span></td>
<td><ul>
<li><span data-ttu-id="0f247-221"><strong>Operator:</strong> Times[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="0f247-221"><strong>Operator:</strong> Times[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="0f247-222"><strong>Infix-anmærkning:</strong> x \* y \* 2 == z</span><span class="sxs-lookup"><span data-stu-id="0f247-222"><strong>Infix notation:</strong> x \* y \* 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0f247-223">Strøm</span><span class="sxs-lookup"><span data-stu-id="0f247-223">Power</span></span></td>
<td><span data-ttu-id="0f247-224">Det tager en eksponentiel.</span><span class="sxs-lookup"><span data-stu-id="0f247-224">This takes an exponential.</span></span> <span data-ttu-id="0f247-225">Det gælder eksponentiering fra højre mod venstre.</span><span class="sxs-lookup"><span data-stu-id="0f247-225">It applies exponentiation from right to left.</span></span> <span data-ttu-id="0f247-226">(Det er med andre ord en højre-association). Derfor svarer <strong>Power[a, b, c]</strong> til <strong>Power[a, Power[b, c]]</strong>.</span><span class="sxs-lookup"><span data-stu-id="0f247-226">(In other words, it&#39;s right-associative.) Therefore, <strong>Power[a, b, c]</strong> is equivalent to <strong>Power[a, Power[b, c]]</strong>.</span></span> <span data-ttu-id="0f247-227"><strong>Power</strong> kan kun bruges, hvis eksponenten er en positiv konstant.</span><span class="sxs-lookup"><span data-stu-id="0f247-227"><strong>Power</strong> can be used only if the exponent is a positive constant.</span></span></td>
<td><span data-ttu-id="0f247-228">Power[args], infix: a ^ b ^ ... ^ z</span><span class="sxs-lookup"><span data-stu-id="0f247-228">Power[args], infix: a ^ b ^ ... ^ z</span></span></td>
<td><ul>
<li><span data-ttu-id="0f247-229"><strong>Operator:</strong> Power[x, 2] == y</span><span class="sxs-lookup"><span data-stu-id="0f247-229"><strong>Operator:</strong> Power[x, 2] == y</span></span></li>
<li><span data-ttu-id="0f247-230"><strong>Infix-anmærkning:</strong> x ^ 2 == y</span><span class="sxs-lookup"><span data-stu-id="0f247-230"><strong>Infix notation:</strong> x ^ 2 == y</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0f247-231">Maks.</span><span class="sxs-lookup"><span data-stu-id="0f247-231">Max</span></span></td>
<td><span data-ttu-id="0f247-232">Dette giver den største tilstand.</span><span class="sxs-lookup"><span data-stu-id="0f247-232">This produces the largest condition.</span></span> <span data-ttu-id="0f247-233">Hvis antallet af betingelser er 0 (nul), returneres <strong>Infinity</strong>.</span><span class="sxs-lookup"><span data-stu-id="0f247-233">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="0f247-234">Max[args]</span><span class="sxs-lookup"><span data-stu-id="0f247-234">Max[args]</span></span></td>
<td><span data-ttu-id="0f247-235"><strong>Operator:</strong> Max[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="0f247-235"><strong>Operator:</strong> Max[x, y, 2] == z</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0f247-236">Min.</span><span class="sxs-lookup"><span data-stu-id="0f247-236">Min</span></span></td>
<td><span data-ttu-id="0f247-237">Dette giver den mindste tilstand.</span><span class="sxs-lookup"><span data-stu-id="0f247-237">This produces the smallest condition.</span></span> <span data-ttu-id="0f247-238">Hvis antallet af betingelser er 0 (nul), returneres <strong>Infinity</strong>.</span><span class="sxs-lookup"><span data-stu-id="0f247-238">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="0f247-239">Min[args]</span><span class="sxs-lookup"><span data-stu-id="0f247-239">Min[args]</span></span></td>
<td><span data-ttu-id="0f247-240"><strong>Operator:</strong> Min[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="0f247-240"><strong>Operator:</strong> Min[x, y, 2] == z</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0f247-241">Negeret</span><span class="sxs-lookup"><span data-stu-id="0f247-241">Not</span></span></td>
<td><span data-ttu-id="0f247-242">Dette giver den logiske inverse af tilstanden.</span><span class="sxs-lookup"><span data-stu-id="0f247-242">This produces the logical inverse of its condition.</span></span> <span data-ttu-id="0f247-243">Det skal have præcis én betingelse.</span><span class="sxs-lookup"><span data-stu-id="0f247-243">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="0f247-244">Not[expr], infix: !expr</span><span class="sxs-lookup"><span data-stu-id="0f247-244">Not[expr], infix: !expr</span></span></td>
<td><ul>
<li><span data-ttu-id="0f247-245"><strong>Operator:</strong> Not[x] &amp; Not[y == 3]</span><span class="sxs-lookup"><span data-stu-id="0f247-245"><strong>Operator:</strong> Not[x] &amp; Not[y == 3]</span></span></li>
<li><span data-ttu-id="0f247-246"><strong>Infix-anmærkning:</strong> !x!(y == 3)</span><span class="sxs-lookup"><span data-stu-id="0f247-246"><strong>Infix notation:</strong> !x!(y == 3)</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0f247-247">Eksemplerne i næste tabel viser, hvordan du skriver en infix-anmærkning.</span><span class="sxs-lookup"><span data-stu-id="0f247-247">The examples in the next table show how to write infix notation.</span></span>


|  <span data-ttu-id="0f247-248">Notationen infix</span><span class="sxs-lookup"><span data-stu-id="0f247-248">Infix notation</span></span>   |                                          <span data-ttu-id="0f247-249">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="0f247-249">Description</span></span>                                          |
|-------------------|-----------------------------------------------------------------------------------------------|
|     <span data-ttu-id="0f247-250">x + y + z</span><span class="sxs-lookup"><span data-stu-id="0f247-250">x + y + z</span></span>     |                                           <span data-ttu-id="0f247-251">Tilføjelse</span><span class="sxs-lookup"><span data-stu-id="0f247-251">Addition</span></span>                                            |
|    <span data-ttu-id="0f247-252">x \* y \* z</span><span class="sxs-lookup"><span data-stu-id="0f247-252">x \* y \* z</span></span>    |                                        <span data-ttu-id="0f247-253">Multiplikation</span><span class="sxs-lookup"><span data-stu-id="0f247-253">Multiplication</span></span>                                         |
|       <span data-ttu-id="0f247-254">x - y</span><span class="sxs-lookup"><span data-stu-id="0f247-254">x - y</span></span>       | <span data-ttu-id="0f247-255">Binær subtraktion oversættes på samme måde som binær addition, hvor der er et negativt sekund.</span><span class="sxs-lookup"><span data-stu-id="0f247-255">Binary subtraction is translated the same as binary addition where there is a negated second.</span></span> |
|     <span data-ttu-id="0f247-256">x ^ y ^ z</span><span class="sxs-lookup"><span data-stu-id="0f247-256">x ^ y ^ z</span></span>     |                          <span data-ttu-id="0f247-257">Eksponentiering, der har en højre-association</span><span class="sxs-lookup"><span data-stu-id="0f247-257">Exponentiation that has right associativity</span></span>                          |
|        <span data-ttu-id="0f247-258">!x</span><span class="sxs-lookup"><span data-stu-id="0f247-258">!x</span></span>         |                                          <span data-ttu-id="0f247-259">Boolesk ikke</span><span class="sxs-lookup"><span data-stu-id="0f247-259">Boolean not</span></span>                                          |
|      <span data-ttu-id="0f247-260">x -: y</span><span class="sxs-lookup"><span data-stu-id="0f247-260">x -: y</span></span>       |                                      <span data-ttu-id="0f247-261">Boolesk virkning</span><span class="sxs-lookup"><span data-stu-id="0f247-261">Boolean implication</span></span>                                      |
|         <span data-ttu-id="0f247-262">x</span><span class="sxs-lookup"><span data-stu-id="0f247-262">x</span></span>         |                                               <span data-ttu-id="0f247-263">y</span><span class="sxs-lookup"><span data-stu-id="0f247-263">y</span></span>                                               |
|     <span data-ttu-id="0f247-264">x & y & z</span><span class="sxs-lookup"><span data-stu-id="0f247-264">x & y & z</span></span>     |                                          <span data-ttu-id="0f247-265">Boolesk og</span><span class="sxs-lookup"><span data-stu-id="0f247-265">Boolean and</span></span>                                          |
|    <span data-ttu-id="0f247-266">x == y == z</span><span class="sxs-lookup"><span data-stu-id="0f247-266">x == y == z</span></span>    |                                           <span data-ttu-id="0f247-267">Lig med</span><span class="sxs-lookup"><span data-stu-id="0f247-267">Equality</span></span>                                            |
|    <span data-ttu-id="0f247-268">x != y != z</span><span class="sxs-lookup"><span data-stu-id="0f247-268">x != y != z</span></span>    |                                           <span data-ttu-id="0f247-269">Bestemt</span><span class="sxs-lookup"><span data-stu-id="0f247-269">Distinct</span></span>                                            |
|  <span data-ttu-id="0f247-270">x &lt; y &lt; z</span><span class="sxs-lookup"><span data-stu-id="0f247-270">x &lt; y &lt; z</span></span>  |                                           <span data-ttu-id="0f247-271">Mindre end</span><span class="sxs-lookup"><span data-stu-id="0f247-271">Less than</span></span>                                           |
|  <span data-ttu-id="0f247-272">x &gt; y &gt; z</span><span class="sxs-lookup"><span data-stu-id="0f247-272">x &gt; y &gt; z</span></span>  |                                         <span data-ttu-id="0f247-273">Større end</span><span class="sxs-lookup"><span data-stu-id="0f247-273">Greater than</span></span>                                          |
| <span data-ttu-id="0f247-274">x &lt;= y &lt;= z</span><span class="sxs-lookup"><span data-stu-id="0f247-274">x &lt;= y &lt;= z</span></span> |                                     <span data-ttu-id="0f247-275">Mindre end eller lig med</span><span class="sxs-lookup"><span data-stu-id="0f247-275">Less than or equal to</span></span>                                     |
| <span data-ttu-id="0f247-276">x &gt;= y &gt;= z</span><span class="sxs-lookup"><span data-stu-id="0f247-276">x &gt;= y &gt;= z</span></span> |                                   <span data-ttu-id="0f247-277">Større end eller lig med</span><span class="sxs-lookup"><span data-stu-id="0f247-277">Greater than or equal to</span></span>                                    |
|        <span data-ttu-id="0f247-278">(x)</span><span class="sxs-lookup"><span data-stu-id="0f247-278">(x)</span></span>        |                           <span data-ttu-id="0f247-279">Parentes tilsidesætter standardprioritering.</span><span class="sxs-lookup"><span data-stu-id="0f247-279">Parentheses override default precedence.</span></span>                            |

## <a name="why-arent-my-expression-constraints-validated-correctly"></a><span data-ttu-id="0f247-280">Hvorfor valideres mine udtryksbegrænsninger ikke korrekt?</span><span class="sxs-lookup"><span data-stu-id="0f247-280">Why aren't my expression constraints validated correctly?</span></span>
<span data-ttu-id="0f247-281">Du kan ikke bruge et reserveret nøgleord som problemløsernavn til attributter, komponenter og underkomponenter i en produktkonfigurationsmodel.</span><span class="sxs-lookup"><span data-stu-id="0f247-281">You can't use reserved keywords as solver names for attributes, components, or subcomponents in a product configuration model.</span></span><span data-ttu-id="0f247-282">Her er en liste over de reserverede nøgleord, som du kan bruge:</span><span class="sxs-lookup"><span data-stu-id="0f247-282"> Here is a list of the reserved keywords that you can't use:</span></span>

-   <span data-ttu-id="0f247-283">Loft</span><span class="sxs-lookup"><span data-stu-id="0f247-283">Ceiling</span></span>
-   <span data-ttu-id="0f247-284">Element</span><span class="sxs-lookup"><span data-stu-id="0f247-284">Element</span></span>
-   <span data-ttu-id="0f247-285">Lig med</span><span class="sxs-lookup"><span data-stu-id="0f247-285">Equal</span></span>
-   <span data-ttu-id="0f247-286">Etage</span><span class="sxs-lookup"><span data-stu-id="0f247-286">Floor</span></span>
-   <span data-ttu-id="0f247-287">Hvis</span><span class="sxs-lookup"><span data-stu-id="0f247-287">If</span></span>
-   <span data-ttu-id="0f247-288">Mindre end</span><span class="sxs-lookup"><span data-stu-id="0f247-288">Less</span></span>
-   <span data-ttu-id="0f247-289">Større end</span><span class="sxs-lookup"><span data-stu-id="0f247-289">Greater</span></span>
-   <span data-ttu-id="0f247-290">Indebærer</span><span class="sxs-lookup"><span data-stu-id="0f247-290">Implies</span></span>
-   <span data-ttu-id="0f247-291">Log</span><span class="sxs-lookup"><span data-stu-id="0f247-291">Log</span></span>
-   <span data-ttu-id="0f247-292">Maks</span><span class="sxs-lookup"><span data-stu-id="0f247-292">Max</span></span>
-   <span data-ttu-id="0f247-293">Min.</span><span class="sxs-lookup"><span data-stu-id="0f247-293">Min</span></span>
-   <span data-ttu-id="0f247-294">Minus</span><span class="sxs-lookup"><span data-stu-id="0f247-294">Minus</span></span>
-   <span data-ttu-id="0f247-295">Plus</span><span class="sxs-lookup"><span data-stu-id="0f247-295">Plus</span></span>
-   <span data-ttu-id="0f247-296">Strøm</span><span class="sxs-lookup"><span data-stu-id="0f247-296">Power</span></span>
-   <span data-ttu-id="0f247-297">Tider</span><span class="sxs-lookup"><span data-stu-id="0f247-297">Times</span></span>
-   <span data-ttu-id="0f247-298">Slot</span><span class="sxs-lookup"><span data-stu-id="0f247-298">Slot</span></span>
-   <span data-ttu-id="0f247-299">Model</span><span class="sxs-lookup"><span data-stu-id="0f247-299">Model</span></span>
-   <span data-ttu-id="0f247-300">Beslutning</span><span class="sxs-lookup"><span data-stu-id="0f247-300">Decision</span></span>
-   <span data-ttu-id="0f247-301">Mål</span><span class="sxs-lookup"><span data-stu-id="0f247-301">Goal</span></span>


<a name="additional-resources"></a><span data-ttu-id="0f247-302">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="0f247-302">Additional resources</span></span>
--------

[<span data-ttu-id="0f247-303">Oprette en udtryksbegrænsning</span><span class="sxs-lookup"><span data-stu-id="0f247-303">Create an expression constraint</span></span>](tasks/add-expression-constraint-product-configuration-model.md)

[<span data-ttu-id="0f247-304">Tilføje en beregning til en produktkonfigurationsmodel</span><span class="sxs-lookup"><span data-stu-id="0f247-304">Add a calculation to a product configuration model</span></span>](tasks/add-calculation-product-configuration-model.md)



