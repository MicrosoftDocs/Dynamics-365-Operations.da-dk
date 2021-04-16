---
title: Beregninger af produktkonfigurationsmodel
description: Dette emne beskriver, hvordan du opretter beregninger for attributter i en produktkonfigurationsmodel
author: t-benebo
ms.date: 03/18/2021
ms.topic: article
ms.search.form: PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-03-18
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: eaf6264f060d33575740ad38e7a65158baba296b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829612"
---
# <a name="product-configuration-model-calculations"></a><span data-ttu-id="1118b-103">Beregninger af produktkonfigurationsmodel</span><span class="sxs-lookup"><span data-stu-id="1118b-103">Product configuration model calculations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1118b-104">Dette emne beskriver, hvordan du opretter beregninger for attributter i en produktkonfigurationsmodel.</span><span class="sxs-lookup"><span data-stu-id="1118b-104">This topic describes how to create calculations for attributes in a product configuration model.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1118b-105">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="1118b-105">Prerequisites</span></span>

<span data-ttu-id="1118b-106">Beregninger bruges i en produktkonfigurationsmodel til at beregne konfigurationsværdier for et produkt.</span><span class="sxs-lookup"><span data-stu-id="1118b-106">Calculations are used in a product configuration model to calculate the configuration values for a product.</span></span> <span data-ttu-id="1118b-107">Før du kan gå i gang med at konfigurere beregninger, skal den relaterede produktkonfigurationsmodel eksistere.</span><span class="sxs-lookup"><span data-stu-id="1118b-107">Before you can start to set up calculations, the related product configuration model must exist.</span></span> <span data-ttu-id="1118b-108">Du kan finde en oversigt over opsætningsprocessen for konfigurationsmodeller og de relaterede opgaver under [Konfigurere en produktkonfigurationsmodel](set-up-maintain-product-configuration-model.md).</span><span class="sxs-lookup"><span data-stu-id="1118b-108">For an overview of the setup process for configuration models and the related tasks, see [Set up a product configuration model](set-up-maintain-product-configuration-model.md).</span></span>

## <a name="create-a-calculation"></a><span data-ttu-id="1118b-109">Oprette en beregning</span><span class="sxs-lookup"><span data-stu-id="1118b-109">Create a calculation</span></span>

<span data-ttu-id="1118b-110">En beregning består af et udtryk og en målattribut.</span><span class="sxs-lookup"><span data-stu-id="1118b-110">A calculation consists of an expression and a target attribute.</span></span> <span data-ttu-id="1118b-111">Du kan få flere oplysninger under [Ofte stillede spørgsmål om beregninger for produktkonfigurationsmodeller](calculate-product-configuration-models.md).</span><span class="sxs-lookup"><span data-stu-id="1118b-111">For more information, see [Calculations for product configuration models FAQ](calculate-product-configuration-models.md).</span></span>

<span data-ttu-id="1118b-112">Hvis du vil oprette en beregning for en eksisterende produktmodel, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="1118b-112">To create a calculation for an existing product model, follow these steps.</span></span>

1. <span data-ttu-id="1118b-113">Gå til **Administration af produktoplysninger \> Fælles \> Produktkonfigurationsmodeller**.</span><span class="sxs-lookup"><span data-stu-id="1118b-113">Go to **Product information management \> Common \> Product configuration models**.</span></span>
1. <span data-ttu-id="1118b-114">Åbn en produktkonfigurationsmodel, og vælg derefter **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="1118b-114">Open a product configuration model, and then select **Edit**.</span></span>
1. <span data-ttu-id="1118b-115">I oversigtspanelet **Beregninger** skal du vælge **Tilføj** for at tilføje en beregning, og indstil derefter følgende felter:</span><span class="sxs-lookup"><span data-stu-id="1118b-115">On the **Calculations** FastTab, select **Add** to add a calculation, and then set the following fields:</span></span>

    - <span data-ttu-id="1118b-116">**Navn** – Angiv et navn til beregningen.</span><span class="sxs-lookup"><span data-stu-id="1118b-116">**Name** – Enter a name for the calculation.</span></span>
    - <span data-ttu-id="1118b-117">**Beskrivelse** – Indtast en beskrivelse af beregningen.</span><span class="sxs-lookup"><span data-stu-id="1118b-117">**Description** – Enter a description of the calculation.</span></span>
    - <span data-ttu-id="1118b-118">**Målattribut** – Vælg den attribut, du foretager beregningen for.</span><span class="sxs-lookup"><span data-stu-id="1118b-118">**Target attribute** – Select the attribute that you're making the calculation for.</span></span>

1. <span data-ttu-id="1118b-119">Vælg **Rediger udtryk**.</span><span class="sxs-lookup"><span data-stu-id="1118b-119">Select **Edit expression**.</span></span>
1. <span data-ttu-id="1118b-120">I dialogboksen **Angiv en beregning** skal du føje de påkrævede attributter, operatorer og værdier til udtrykket.</span><span class="sxs-lookup"><span data-stu-id="1118b-120">In the **Enter a calculation** dialog box, add the required attributes, operators, and values to the expression.</span></span> <span data-ttu-id="1118b-121">Få flere oplysninger om arbejdet med disse elementer under [Udtryksbegrænsninger og tabelbegrænsninger i modeller for produktkonfiguration](expression-constraints-table-constraints-product-configuration-models.md).</span><span class="sxs-lookup"><span data-stu-id="1118b-121">For more information about how to work with these elements, see [Expression constraints and table constraints in product configuration models](expression-constraints-table-constraints-product-configuration-models.md).</span></span>
1. <span data-ttu-id="1118b-122">Når udtrykket er klar, skal du vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="1118b-122">When your expression is ready, select **OK**.</span></span>

## <a name="calculation-examples"></a><span data-ttu-id="1118b-123">Eksempler på beregninger</span><span class="sxs-lookup"><span data-stu-id="1118b-123">Calculation examples</span></span>

<span data-ttu-id="1118b-124">Dette afsnit indeholder et par eksempler, der viser, hvordan beregninger fungerer.</span><span class="sxs-lookup"><span data-stu-id="1118b-124">This section provides a few examples that show how calculations work.</span></span>

### <a name="example-1"></a><span data-ttu-id="1118b-125">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="1118b-125">Example 1</span></span>

<span data-ttu-id="1118b-126">Målattributten er boolesk, og beregningen bruger følgende betingede udtryk:</span><span class="sxs-lookup"><span data-stu-id="1118b-126">The target attribute is Boolean, and the calculation uses the following conditional expression:</span></span>

`If[(decimalAttribute1 / decimalAttribute2) < 1, True, False]`

<span data-ttu-id="1118b-127">Udtrykket returnerer værdien *Sand* til målattributten, hvis `decimalAttribute2` er større end eller lig med `decimalAttribute1`.</span><span class="sxs-lookup"><span data-stu-id="1118b-127">This expression returns a value of *True* to the target attribute if `decimalAttribute2` is greater than or equal to `decimalAttribute1`.</span></span> <span data-ttu-id="1118b-128">Ellers returneres værdien *Falsk*.</span><span class="sxs-lookup"><span data-stu-id="1118b-128">Otherwise, it returns a value of *False*.</span></span>

### <a name="example-2"></a><span data-ttu-id="1118b-129">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="1118b-129">Example 2</span></span>

<span data-ttu-id="1118b-130">I dette eksempel bruges tekstattributten `textFixedList` som målattribut.</span><span class="sxs-lookup"><span data-stu-id="1118b-130">This example uses the text attribute `textFixedList` as the target attribute.</span></span> <span data-ttu-id="1118b-131">Denne attribut indeholder følgende faste liste.</span><span class="sxs-lookup"><span data-stu-id="1118b-131">This attribute contains the following fixed list.</span></span>

| <span data-ttu-id="1118b-132">Værdi</span><span class="sxs-lookup"><span data-stu-id="1118b-132">Value</span></span> | <span data-ttu-id="1118b-133">Værdi for problemløser</span><span class="sxs-lookup"><span data-stu-id="1118b-133">Solver value</span></span> |
|---|---|
| <span data-ttu-id="1118b-134">A</span><span class="sxs-lookup"><span data-stu-id="1118b-134">A</span></span> | <span data-ttu-id="1118b-135">1a</span><span class="sxs-lookup"><span data-stu-id="1118b-135">1a</span></span> |
| <span data-ttu-id="1118b-136">B</span><span class="sxs-lookup"><span data-stu-id="1118b-136">B</span></span> | <span data-ttu-id="1118b-137">2b</span><span class="sxs-lookup"><span data-stu-id="1118b-137">2b</span></span> |
| <span data-ttu-id="1118b-138">C</span><span class="sxs-lookup"><span data-stu-id="1118b-138">C</span></span> | <span data-ttu-id="1118b-139">2c</span><span class="sxs-lookup"><span data-stu-id="1118b-139">2c</span></span> |

<span data-ttu-id="1118b-140">Følgende skærmbillede viser, hvordan indstillingerne for denne attribut kan se ud i systemet.</span><span class="sxs-lookup"><span data-stu-id="1118b-140">The following screenshot shows how the settings for this attribute might look in your system.</span></span>

<span data-ttu-id="1118b-141">![Indstillinger af attributtype, f.eks. 2](media/model-calculations-example2.png "Indstillinger af attributtype, f.eks. 2")</span><span class="sxs-lookup"><span data-stu-id="1118b-141">![Attribute type settings for example 2](media/model-calculations-example2.png "Attribute type settings for example 2")</span></span>

<span data-ttu-id="1118b-142">Attributten bruges i følgende betingede sætning:</span><span class="sxs-lookup"><span data-stu-id="1118b-142">The attribute is used in the following conditional statement:</span></span>

`If[integerAttribute < 150, 0, 2]`

<span data-ttu-id="1118b-143">Hvis `integerAttribute` er mindre end 150, returnerer denne sætning tekstværdien af den første post på den faste liste, *A*. Ellers returnerer den tekstværdien for den tredje post på den faste liste, *C*.</span><span class="sxs-lookup"><span data-stu-id="1118b-143">If `integerAttribute` is less than 150, this statement returns the text value of the first record in the fixed list, *A*. Otherwise, it returns the text value of the third record in the fixed list, *C*.</span></span>

> [!NOTE]
> <span data-ttu-id="1118b-144">Den faste liste svarer til en nulbaseret fasttekst, og dens værdier åbnes med den relevante heltalsværdi.</span><span class="sxs-lookup"><span data-stu-id="1118b-144">The fixed list is equivalent to a zero-based enumeration (enum), and its values are accessed by the appropriate integer value.</span></span> <span data-ttu-id="1118b-145">Den første faste listeværdi (*A*) sammenholdes derfor med *0*, den anden værdi (*B*) sammenholdes med *1*, og den tredje værdi (*C*) sammenholdes med *2*.</span><span class="sxs-lookup"><span data-stu-id="1118b-145">Therefore, the first fixed list value (*A*) is matched to *0*, the second value (*B*) is matched to *1*, and the third value (*C*) is matched to *2*.</span></span>

### <a name="example-3"></a><span data-ttu-id="1118b-146">Eksempel 3</span><span class="sxs-lookup"><span data-stu-id="1118b-146">Example 3</span></span>

<span data-ttu-id="1118b-147">I dette eksempel bruges målattributten `textFixedList` fra det forrige eksempel.</span><span class="sxs-lookup"><span data-stu-id="1118b-147">This example uses the `textFixedList` target attribute from the previous example.</span></span> <span data-ttu-id="1118b-148">Der bruges også en anden tekstattribut, `textAttribute`, der indeholder følgende faste liste.</span><span class="sxs-lookup"><span data-stu-id="1118b-148">It also uses another text attribute, `textAttribute`, that contains the following fixed list.</span></span>

| <span data-ttu-id="1118b-149">Værdi</span><span class="sxs-lookup"><span data-stu-id="1118b-149">Value</span></span> | <span data-ttu-id="1118b-150">Værdi for problemløser</span><span class="sxs-lookup"><span data-stu-id="1118b-150">Solver value</span></span> |
|---|---|
| <span data-ttu-id="1118b-151">AA</span><span class="sxs-lookup"><span data-stu-id="1118b-151">AA</span></span> | <span data-ttu-id="1118b-152">1aa</span><span class="sxs-lookup"><span data-stu-id="1118b-152">1aa</span></span> |
| <span data-ttu-id="1118b-153">BB</span><span class="sxs-lookup"><span data-stu-id="1118b-153">BB</span></span> | <span data-ttu-id="1118b-154">2bb</span><span class="sxs-lookup"><span data-stu-id="1118b-154">2bb</span></span> |

<span data-ttu-id="1118b-155">Følgende skærmbillede viser, hvordan indstillingerne for denne attribut kan se ud i systemet.</span><span class="sxs-lookup"><span data-stu-id="1118b-155">The following screenshot shows how the settings for this attribute might look in your system.</span></span>

<span data-ttu-id="1118b-156">![Indstillinger af attributtype, f.eks. 3](media/model-calculations-example3.png "Indstillinger af attributtype, f.eks. 3")</span><span class="sxs-lookup"><span data-stu-id="1118b-156">![Attribute type settings for example 3](media/model-calculations-example3.png "Attribute type settings for example 3")</span></span>

<span data-ttu-id="1118b-157">Værdien af `textFixedList`-attributten beregnes ved hjælp af følgende betingede sætning:</span><span class="sxs-lookup"><span data-stu-id="1118b-157">The value for the `textFixedList` attribute is calculated by using the following conditional statement:</span></span>

`If[textAttribute == "1aa", 0, 2]`

<span data-ttu-id="1118b-158">Hvis `textAttribute` har en problemløserværdi, der er lig med *1aa*, returnerer dette udtryk tekstværdien af den første post på den faste liste `textFixedList`, *A*. Ellers returnerer den tekstværdien for den tredje post på den faste liste `textFixedList`, *C*.</span><span class="sxs-lookup"><span data-stu-id="1118b-158">If the `textAttribute` value has a solver value that equals *1aa*, this expression returns the text value of the first record in the `textFixedList` fixed list, *A*. Otherwise, it returns the text value of the third record in the `textFixedList` fixed list, *C*.</span></span>

> [!NOTE]
> - <span data-ttu-id="1118b-159">Den betingede sætning skal bruge problemløserværdien for attributten.</span><span class="sxs-lookup"><span data-stu-id="1118b-159">The conditional statement must use the solver value of the attribute.</span></span>
> - <span data-ttu-id="1118b-160">Det er kun tekstattributter fra fastlisten, der kan bruges i beregninger.</span><span class="sxs-lookup"><span data-stu-id="1118b-160">Only fixed-list text attributes can be used in calculations.</span></span>

## <a name="see-also"></a><span data-ttu-id="1118b-161">Se også</span><span class="sxs-lookup"><span data-stu-id="1118b-161">See also</span></span>

- [<span data-ttu-id="1118b-162">Ofte stillede spørgsmål om beregninger for produktkonfigurationsmodeller</span><span class="sxs-lookup"><span data-stu-id="1118b-162">Calculations for product configuration models FAQ</span></span>](calculate-product-configuration-models.md)
- [<span data-ttu-id="1118b-163">Tilføje en udtryksbegrænsing til en produktkonfigurationsmodel</span><span class="sxs-lookup"><span data-stu-id="1118b-163">Add an expression constraint to a product configuration model</span></span>](tasks/add-expression-constraint-product-configuration-model.md)
- [<span data-ttu-id="1118b-164">Oversigt over produktkonfigurationsmodeller</span><span class="sxs-lookup"><span data-stu-id="1118b-164">Product configuration models overview</span></span>](product-configuration-models.md)
