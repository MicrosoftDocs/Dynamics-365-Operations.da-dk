---
title: Måleenhedskonvertering pr. produktvariant
description: Dette emne beskriver, hvordan måleenhedskonverteringer kan konfigureres for produktvarianter.
author: johanhoffmann
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: UnitOfMeasureConversion
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: c8181f0bda9b781a6c2b0feb0aba1beb51bfea65
ms.sourcegitcommit: af36eb17b36092a3101bbfc96486b25036676558
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/06/2020
ms.locfileid: "2935093"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a><span data-ttu-id="9cd55-103">Måleenhedskonvertering pr. produktvariant</span><span class="sxs-lookup"><span data-stu-id="9cd55-103">Unit of measure conversion per product variant</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9cd55-104">Dette emne beskriver, hvordan måleenhedskonverteringer kan konfigureres for produktvarianter.</span><span class="sxs-lookup"><span data-stu-id="9cd55-104">This topic explains how unit of measure conversions can be set up on product variants.</span></span> <span data-ttu-id="9cd55-105">Emnet indeholder et eksempel på opsætningen.</span><span class="sxs-lookup"><span data-stu-id="9cd55-105">It includes an example of the setup.</span></span>

<span data-ttu-id="9cd55-106">Denne funktion gør det muligt for virksomheder at definere forskellige enhedsomregninger mellem varianterne af det samme produkt.</span><span class="sxs-lookup"><span data-stu-id="9cd55-106">This feature makes it possible for companies to define different unit conversion between the variants of the same product.</span></span> <span data-ttu-id="9cd55-107">I dette emne bruges følgende eksempel.</span><span class="sxs-lookup"><span data-stu-id="9cd55-107">The following example is used in this topic.</span></span> <span data-ttu-id="9cd55-108">Et firma sælger T-shirts i størrelse lille, mellem, stor og ekstra stor.</span><span class="sxs-lookup"><span data-stu-id="9cd55-108">A company sells T-shirts in sizes Small, Medium, Large, and Extra-Large.</span></span> <span data-ttu-id="9cd55-109">Disse T-shirts er defineret som et produkt, og de forskellige størrelser er defineret som varianter af produktet.</span><span class="sxs-lookup"><span data-stu-id="9cd55-109">The T-shirt is defined as a product, and the different sizes are defined as variants of the product.</span></span> <span data-ttu-id="9cd55-110">T-shirts er pakket i kasser, og der kan være fem T-shirts i en kasse med undtagelse af de ekstra store, hvor der er kun plads til fire T-shirts.</span><span class="sxs-lookup"><span data-stu-id="9cd55-110">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-Large size where there is only space for four T-shirts.</span></span> <span data-ttu-id="9cd55-111">Virksomheden ønsker at spore de forskellige varianter af sine T-shirts i enheden **Styk**, men sælger T-shirts i enheden **Kasser**.</span><span class="sxs-lookup"><span data-stu-id="9cd55-111">The company wants to track the different variants of the T-shirts in the unit **Pieces** but is selling the T-shirts in the unit **Boxes**.</span></span> <span data-ttu-id="9cd55-112">Konverteringen mellem lagerenheden og salgsenheden er 1 kasse = 5 stk. undtagen varianten ekstra stor, hvor konverteringen er 1 kasse = 4 styk.</span><span class="sxs-lookup"><span data-stu-id="9cd55-112">The conversion between the inventory unit and the sales unit is 1 Box = 5 Pieces, except for the variant Extra-Large, where the conversion is 1 Box = 4 Pieces.</span></span>

### <a name="set-up-a-product-for-unit-conversion-per-variant"></a><span data-ttu-id="9cd55-113">Konfigurere et produkt til enhedsomregning pr. variant</span><span class="sxs-lookup"><span data-stu-id="9cd55-113">Set up a product for unit conversion per variant</span></span>

<span data-ttu-id="9cd55-114">Produktvarianter kan kun oprettes for produkter af **produktundertypen**: **Produktmaster**.</span><span class="sxs-lookup"><span data-stu-id="9cd55-114">Product variants can only be created for products of **Product subtype**: **Product master**.</span></span> <span data-ttu-id="9cd55-115">Du kan finde flere oplysninger i [Oprette en produktmaster](tasks/create-product-master.md).</span><span class="sxs-lookup"><span data-stu-id="9cd55-115">For more information, see [Create a product master](tasks/create-product-master.md).</span></span>

<span data-ttu-id="9cd55-116">Funktionen er ikke aktiveret for produkter, der er konfigureret til fastvægtprocesser.</span><span class="sxs-lookup"><span data-stu-id="9cd55-116">The feature is not enabled for products that are set up for Catch Weight processes.</span></span> 

<span data-ttu-id="9cd55-117">Når produktmasteren er oprettet med frigivne produktvarianter, kan du angive enhedsomregninger pr. variant.</span><span class="sxs-lookup"><span data-stu-id="9cd55-117">When the product master with released products variants is created, unit conversions per variants can be set up.</span></span> <span data-ttu-id="9cd55-118">Du kan finde menupunktet, hvor du kan åbne siden til enhedsomregning i forbindelse med et produkt eller en produktvariant på følgende sider.</span><span class="sxs-lookup"><span data-stu-id="9cd55-118">You can find the menu item for opening the unit conversion page in context of a product or a product variant on the following pages.</span></span>

-   <span data-ttu-id="9cd55-119">Siden **Produktdetaljer**</span><span class="sxs-lookup"><span data-stu-id="9cd55-119">**Product details** page</span></span>
-   <span data-ttu-id="9cd55-120">Siden **Oplysninger om frigivne produkter**</span><span class="sxs-lookup"><span data-stu-id="9cd55-120">**Released products details** page</span></span>
-   <span data-ttu-id="9cd55-121">Siden **Frigivne produktvarianter**</span><span class="sxs-lookup"><span data-stu-id="9cd55-121">**Released product variants** page</span></span>

<span data-ttu-id="9cd55-122">Når du åbner siden **Enhedsomregning** i forbindelse med en produktmaster eller en frigivet produktvariant, kan du vælge, om du vil definere enhedsomregningen for produktet eller for en produktvariant.</span><span class="sxs-lookup"><span data-stu-id="9cd55-122">When you open the **Unit conversion** page in context of a product master or released product variant, you can select if you want to set up the unit conversion for the product or for a product variant.</span></span> <span data-ttu-id="9cd55-123">Det gør du ved at vælge enten **Produktvariant** eller **Produkt** i feltet **Opret konvertering for**.</span><span class="sxs-lookup"><span data-stu-id="9cd55-123">You do that by selecting either **Product variant** or **Product** in the **Create conversion for** field.</span></span>

### <a name="product-variant"></a><span data-ttu-id="9cd55-124">Produktvariant</span><span class="sxs-lookup"><span data-stu-id="9cd55-124">Product variant</span></span>

<span data-ttu-id="9cd55-125">Hvis du vælger **Produktvariant**, kan du vælge, hvilken variant du vil definere enhedsomregning for, i feltet **Produktvariant**.</span><span class="sxs-lookup"><span data-stu-id="9cd55-125">If you select **Product variant,** then you can select for which variant you want to set up the unit conversion in the **Product variant** field.</span></span>

### <a name="product"></a><span data-ttu-id="9cd55-126">Produkt</span><span class="sxs-lookup"><span data-stu-id="9cd55-126">Product</span></span>

<span data-ttu-id="9cd55-127">Hvis du vælger **Produkt**, kan du konfigurere en enhedsomregning for produktmasteren.</span><span class="sxs-lookup"><span data-stu-id="9cd55-127">If you select **Product**, then you can set up a unit conversion for the product master.</span></span> <span data-ttu-id="9cd55-128">Denne enhedsomregning skal gælde for alle produktvarianter uden defineret enhedsomregning.</span><span class="sxs-lookup"><span data-stu-id="9cd55-128">This unit conversion will apply for all product variants with no defined unit conversion.</span></span>

### <a name="example"></a><span data-ttu-id="9cd55-129">Eksempel</span><span class="sxs-lookup"><span data-stu-id="9cd55-129">Example</span></span>

<span data-ttu-id="9cd55-130">En produktmaster, **T-shirt**, har fire frigivne produktvarianter: lille, mellem, stor og ekstra stor.</span><span class="sxs-lookup"><span data-stu-id="9cd55-130">A product master, **T-Shirt**, has four released products variants Small, Medium, Large, and X-Large.</span></span> <span data-ttu-id="9cd55-131">T-shirts er pakket i kasser, og der kan være fem T-shirts i en kasse med undtagelse af de ekstra store, hvor der er kun plads til fire T-shirts.</span><span class="sxs-lookup"><span data-stu-id="9cd55-131">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-large size where there is only space for four T-shirts.</span></span>

<span data-ttu-id="9cd55-132">Først skal du åbne siden **Enhedsomregning** fra siden Frigivne produktdetaljer for **T-shirt.**</span><span class="sxs-lookup"><span data-stu-id="9cd55-132">First, open the **Unit conversion** page from the Release product details page for **T-shirt.**</span></span>

<span data-ttu-id="9cd55-133">På siden **Enhedsomregning** skal du definere enhedsomregningen for produktvarianten ekstra stor.</span><span class="sxs-lookup"><span data-stu-id="9cd55-133">On the **Unit conversion** page, set up the unit conversion for the release product variant X-Large.</span></span>

| <span data-ttu-id="9cd55-134">**Felt**</span><span class="sxs-lookup"><span data-stu-id="9cd55-134">**Field**</span></span>             | <span data-ttu-id="9cd55-135">**Indstilling**</span><span class="sxs-lookup"><span data-stu-id="9cd55-135">**Setting**</span></span>             |
|-----------------------|-------------------------|
| <span data-ttu-id="9cd55-136">Opret konvertering for</span><span class="sxs-lookup"><span data-stu-id="9cd55-136">Create conversion for</span></span> | <span data-ttu-id="9cd55-137">Produktvariant</span><span class="sxs-lookup"><span data-stu-id="9cd55-137">Product variant</span></span>         |
| <span data-ttu-id="9cd55-138">Produktvariant</span><span class="sxs-lookup"><span data-stu-id="9cd55-138">Product variant</span></span>       | <span data-ttu-id="9cd55-139">T-shirt : : Ekstra stor : :</span><span class="sxs-lookup"><span data-stu-id="9cd55-139">T-Shirt : : X-Large : :</span></span> |
| <span data-ttu-id="9cd55-140">Fra enhed</span><span class="sxs-lookup"><span data-stu-id="9cd55-140">From unit</span></span>             | <span data-ttu-id="9cd55-141">Kasser</span><span class="sxs-lookup"><span data-stu-id="9cd55-141">Boxes</span></span>                   |
| <span data-ttu-id="9cd55-142">Faktor</span><span class="sxs-lookup"><span data-stu-id="9cd55-142">Factor</span></span>                | <span data-ttu-id="9cd55-143">4</span><span class="sxs-lookup"><span data-stu-id="9cd55-143">4</span></span>                       |
| <span data-ttu-id="9cd55-144">Til enhed</span><span class="sxs-lookup"><span data-stu-id="9cd55-144">To Unit</span></span>               | <span data-ttu-id="9cd55-145">Styk</span><span class="sxs-lookup"><span data-stu-id="9cd55-145">Pieces</span></span>                  |

<span data-ttu-id="9cd55-146">De frigivne produktvarianter lille, mellem og stor har samme enhedsomregning mellem enhedens Kasser og styk, hvilket betyder, at du kan definere enhedsomregningen for disse produktvarianter på produktmasteren.</span><span class="sxs-lookup"><span data-stu-id="9cd55-146">The Released product variants Small, Medium, and Large have the same unit conversion between the unit Box and Pieces, which means that you can define the unit conversion for these product variants on the product master.</span></span>

| <span data-ttu-id="9cd55-147">**Felt**</span><span class="sxs-lookup"><span data-stu-id="9cd55-147">**Field**</span></span>             | <span data-ttu-id="9cd55-148">**Indstilling**</span><span class="sxs-lookup"><span data-stu-id="9cd55-148">**Setting**</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="9cd55-149">Opret konvertering for</span><span class="sxs-lookup"><span data-stu-id="9cd55-149">Create conversion for</span></span> | <span data-ttu-id="9cd55-150">Produkt</span><span class="sxs-lookup"><span data-stu-id="9cd55-150">Product</span></span>     |
| <span data-ttu-id="9cd55-151">Produkt</span><span class="sxs-lookup"><span data-stu-id="9cd55-151">Product</span></span>               | <span data-ttu-id="9cd55-152">T-shirt</span><span class="sxs-lookup"><span data-stu-id="9cd55-152">T-Shirt</span></span>     |
| <span data-ttu-id="9cd55-153">Fra enhed</span><span class="sxs-lookup"><span data-stu-id="9cd55-153">From unit</span></span>             | <span data-ttu-id="9cd55-154">Kasser</span><span class="sxs-lookup"><span data-stu-id="9cd55-154">Boxes</span></span>       |
| <span data-ttu-id="9cd55-155">Faktor</span><span class="sxs-lookup"><span data-stu-id="9cd55-155">Factor</span></span>                | <span data-ttu-id="9cd55-156">5</span><span class="sxs-lookup"><span data-stu-id="9cd55-156">5</span></span>           |
| <span data-ttu-id="9cd55-157">Til enhed</span><span class="sxs-lookup"><span data-stu-id="9cd55-157">To Unit</span></span>               | <span data-ttu-id="9cd55-158">Styk</span><span class="sxs-lookup"><span data-stu-id="9cd55-158">Pieces</span></span>      |

### <a name="using-excel-to-update-the-unit-conversions"></a><span data-ttu-id="9cd55-159">Bruge Excel til at opdatere enhedsomregningerne</span><span class="sxs-lookup"><span data-stu-id="9cd55-159">Using Excel to update the unit conversions</span></span>

<span data-ttu-id="9cd55-160">Hvis et produkt har mange produktvarianter med forskellige enhedsomregninger, er det en god ide at eksportere enhedsomregninger fra siden **Enhedsomregning** til et Excel-regneark, opdatere konverteringerne og derefter publicere dem tilbage til Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9cd55-160">If a product has many product variants with different unit conversions, it's a good idea to export the unit conversions from the **Unit conversion** page to an Excel spreadsheet, update the conversions, and then publish them back to Supply Chain Mangement.</span></span>

<span data-ttu-id="9cd55-161">Muligheden for at eksportere til Excel og publicere ændringerne tilbage til Supply Chain Management aktiveres fra menupunktet **Åbn i Microsoft Office** i handlingsruden på siden **Enhedsomregning**.</span><span class="sxs-lookup"><span data-stu-id="9cd55-161">The option to export to Excel and publish the edits back to Supply Chain Mangement is enabled from the **Open in Microsoft office** menu item on the Action Pane on the **Unit conversion** page.</span></span>
