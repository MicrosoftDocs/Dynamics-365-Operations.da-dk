---
title: Måleenhedskonvertering pr. produktvariant
description: Dette emne beskriver, hvordan måleenhedskonverteringer kan konfigureres for produktvarianter.
author: johanhoffmann
manager: AnnBe
ms.date: 12/18/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: 36fc98c44625cce03945d76973de67021d53353e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844363"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a><span data-ttu-id="90670-103">Måleenhedskonvertering pr. produktvariant</span><span class="sxs-lookup"><span data-stu-id="90670-103">Unit of measure conversion per product variant</span></span>

[!include [banner](../includes/banner.md)]

[!include [pivate-preview](../includes/pivate-preview-banner.md)]

<span data-ttu-id="90670-104">Dette emne beskriver, hvordan måleenhedskonverteringer kan konfigureres for produktvarianter.</span><span class="sxs-lookup"><span data-stu-id="90670-104">This topic explains how unit of measure conversions can be set up on product variants.</span></span> <span data-ttu-id="90670-105">Emnet indeholder et eksempel på opsætningen.</span><span class="sxs-lookup"><span data-stu-id="90670-105">It includes an example of the setup.</span></span>

<span data-ttu-id="90670-106">Denne funktion gør det muligt for virksomheder at definere forskellige enhedsomregninger mellem varianterne af det samme produkt.</span><span class="sxs-lookup"><span data-stu-id="90670-106">This feature makes it possible for companies to define different unit conversion between the variants of the same product.</span></span> <span data-ttu-id="90670-107">I dette emne bruges følgende eksempel.</span><span class="sxs-lookup"><span data-stu-id="90670-107">The following example is used in this topic.</span></span> <span data-ttu-id="90670-108">Et firma sælger T-shirts i størrelse lille, mellem, stor og ekstra stor.</span><span class="sxs-lookup"><span data-stu-id="90670-108">A company sells T-shirts in sizes Small, Medium, Large, and Extra-Large.</span></span> <span data-ttu-id="90670-109">Disse T-shirts er defineret som et produkt, og de forskellige størrelser er defineret som varianter af produktet.</span><span class="sxs-lookup"><span data-stu-id="90670-109">The T-shirt is defined as a product, and the different sizes are defined as variants of the product.</span></span> <span data-ttu-id="90670-110">T-shirts er pakket i kasser, og der kan være fem T-shirts i en kasse med undtagelse af de ekstra store, hvor der er kun plads til fire T-shirts.</span><span class="sxs-lookup"><span data-stu-id="90670-110">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-Large size where there is only space for four T-shirts.</span></span> <span data-ttu-id="90670-111">Virksomheden ønsker at spore de forskellige varianter af sine T-shirts i enheden **Styk**, men sælger T-shirts i enheden **Kasser**.</span><span class="sxs-lookup"><span data-stu-id="90670-111">The company wants to track the different variants of the T-shirts in the unit **Pieces** but is selling the T-shirts in the unit **Boxes**.</span></span> <span data-ttu-id="90670-112">Konverteringen mellem lagerenheden og salgsenheden er 1 kasse = 5 stk. undtagen varianten ekstra stor, hvor konverteringen er 1 kasse = 4 styk.</span><span class="sxs-lookup"><span data-stu-id="90670-112">The conversion between the inventory unit and the sales unit is 1 Box = 5 Pieces, except for the variant Extra-Large, where the conversion is 1 Box = 4 Pieces.</span></span>

## <a name="setup"></a><span data-ttu-id="90670-113">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="90670-113">Setup</span></span>

<span data-ttu-id="90670-114">Du kan konfigurere parametrene til at bruge funktionen for produkter, der er aktiveret til **Alle processer**, eller kun til produkter, der er aktiveret til **Lagerstedsprocesser** ved hjælp af indstillingen **Aktivér konverteringer af måleenheder** på siden **Parametre for produktoplysninger**.</span><span class="sxs-lookup"><span data-stu-id="90670-114">You can configure the parameters for using the feature for products enabled for **All processes** or only for product enabled for the **Warehouse processes** by using the **Enable unit of measure conversations** option on the **Product information parameters** page.</span></span>

### <a name="set-up-a-product-for-unit-conversion-per-variant"></a><span data-ttu-id="90670-115">Konfigurere et produkt til enhedsomregning pr. variant</span><span class="sxs-lookup"><span data-stu-id="90670-115">Set up a product for unit conversion per variant</span></span>

<span data-ttu-id="90670-116">Produktvarianter kan kun oprettes for produkter af **produktundertypen**: **Produktmaster**.</span><span class="sxs-lookup"><span data-stu-id="90670-116">Product variants can only be created for products of **Product subtype**: **Product master**.</span></span> <span data-ttu-id="90670-117">Du kan finde flere oplysninger i [Oprette en produktmaster](tasks/create-product-master.md).</span><span class="sxs-lookup"><span data-stu-id="90670-117">For more information, see [Create a product master](tasks/create-product-master.md).</span></span>

<span data-ttu-id="90670-118">Funktionen er ikke aktiveret for produkter, der er konfigureret til fastvægtprocesser.</span><span class="sxs-lookup"><span data-stu-id="90670-118">The feature is not enabled for products that are set up for Catch Weight processes.</span></span> 

<span data-ttu-id="90670-119">Under oprettelsen af en produktmaster skal du aktivere måleenhedskonvertering ved hjælp af indstillingen **Aktivér konverteringer af måleenheder** på siden **Produktdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="90670-119">During the creation of a product master enable unit of measure conversion by using the **Enable unit of measure conversions** option on the **Product details** page.</span></span>

<span data-ttu-id="90670-120">Når produktmasteren er oprettet med frigivne produktvarianter, kan du angive enhedsomregninger pr. variant.</span><span class="sxs-lookup"><span data-stu-id="90670-120">When the product master with released products variants is created, unit conversions per variants can be set up.</span></span> <span data-ttu-id="90670-121">Du kan finde menupunktet, hvor du kan åbne siden til enhedsomregning i forbindelse med et produkt eller en produktvariant på følgende sider.</span><span class="sxs-lookup"><span data-stu-id="90670-121">You can find the menu item for opening the unit conversion page in context of a product or a product variant on the following pages.</span></span>

-   <span data-ttu-id="90670-122">Siden **Produktdetaljer**</span><span class="sxs-lookup"><span data-stu-id="90670-122">**Product details** page</span></span>
-   <span data-ttu-id="90670-123">Siden **Oplysninger om frigivne produkter**</span><span class="sxs-lookup"><span data-stu-id="90670-123">**Released products details** page</span></span>
-   <span data-ttu-id="90670-124">Siden **Frigivne produktvarianter**</span><span class="sxs-lookup"><span data-stu-id="90670-124">**Released product variants** page</span></span>

<span data-ttu-id="90670-125">Når du åbner siden **Enhedsomregning** i forbindelse med en produktmaster eller en frigivet produktvariant, kan du vælge, om du vil definere enhedsomregningen for produktet eller for en produktvariant.</span><span class="sxs-lookup"><span data-stu-id="90670-125">When you open the **Unit conversion** page in context of a product master or released product variant, you can select if you want to set up the unit conversion for the product or for a product variant.</span></span> <span data-ttu-id="90670-126">Det gør du ved at vælge enten **Produktvariant** eller **Produkt** i feltet **Opret konvertering for**.</span><span class="sxs-lookup"><span data-stu-id="90670-126">You do that by selecting either **Product variant** or **Product** in the **Create conversion for** field.</span></span>

### <a name="product-variant"></a><span data-ttu-id="90670-127">Produktvariant</span><span class="sxs-lookup"><span data-stu-id="90670-127">Product variant</span></span>

<span data-ttu-id="90670-128">Hvis du vælger **Produktvariant**, kan du vælge, hvilken variant du vil definere enhedsomregning for, i feltet **Produktvariant**.</span><span class="sxs-lookup"><span data-stu-id="90670-128">If you select **Product variant,** then you can select for which variant you want to set up the unit conversion in the **Product variant** field.</span></span>

### <a name="product"></a><span data-ttu-id="90670-129">Produkt</span><span class="sxs-lookup"><span data-stu-id="90670-129">Product</span></span>

<span data-ttu-id="90670-130">Hvis du vælger **Produkt**, kan du konfigurere en enhedsomregning for produktmasteren.</span><span class="sxs-lookup"><span data-stu-id="90670-130">If you select **Product**, then you can set up a unit conversion for the product master.</span></span> <span data-ttu-id="90670-131">Denne enhedsomregning skal gælde for alle produktvarianter uden defineret enhedsomregning.</span><span class="sxs-lookup"><span data-stu-id="90670-131">This unit conversion will apply for all product variants with no defined unit conversion.</span></span>

### <a name="example"></a><span data-ttu-id="90670-132">Eksempel</span><span class="sxs-lookup"><span data-stu-id="90670-132">Example</span></span>

<span data-ttu-id="90670-133">En produktmaster, **T-shirt**, har fire frigivne produktvarianter: lille, mellem, stor og ekstra stor.</span><span class="sxs-lookup"><span data-stu-id="90670-133">A product master, **T-Shirt**, has four released products variants Small, Medium, Large, and X-Large.</span></span> <span data-ttu-id="90670-134">T-shirts er pakket i kasser, og der kan være fem T-shirts i en kasse med undtagelse af de ekstra store, hvor der er kun plads til fire T-shirts.</span><span class="sxs-lookup"><span data-stu-id="90670-134">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-large size where there is only space for four T-shirts.</span></span>

<span data-ttu-id="90670-135">Først skal du åbne siden **Enhedsomregning** fra siden Frigivne produktdetaljer for **T-shirt.**</span><span class="sxs-lookup"><span data-stu-id="90670-135">First, open the **Unit conversion** page from the Release product details page for **T-shirt.**</span></span>

<span data-ttu-id="90670-136">På siden **Enhedsomregning** skal du definere enhedsomregningen for produktvarianten ekstra stor.</span><span class="sxs-lookup"><span data-stu-id="90670-136">On the **Unit conversion** page, set up the unit conversion for the release product variant X-Large.</span></span>

| <span data-ttu-id="90670-137">**Felt**</span><span class="sxs-lookup"><span data-stu-id="90670-137">**Field**</span></span>             | <span data-ttu-id="90670-138">**Indstilling**</span><span class="sxs-lookup"><span data-stu-id="90670-138">**Setting**</span></span>             |
|-----------------------|-------------------------|
| <span data-ttu-id="90670-139">Opret konvertering for</span><span class="sxs-lookup"><span data-stu-id="90670-139">Create conversion for</span></span> | <span data-ttu-id="90670-140">Produktvariant</span><span class="sxs-lookup"><span data-stu-id="90670-140">Product variant</span></span>         |
| <span data-ttu-id="90670-141">Produktvariant</span><span class="sxs-lookup"><span data-stu-id="90670-141">Product variant</span></span>       | <span data-ttu-id="90670-142">T-shirt : : Ekstra stor : :</span><span class="sxs-lookup"><span data-stu-id="90670-142">T-Shirt : : X-Large : :</span></span> |
| <span data-ttu-id="90670-143">Fra enhed</span><span class="sxs-lookup"><span data-stu-id="90670-143">From unit</span></span>             | <span data-ttu-id="90670-144">Kasser</span><span class="sxs-lookup"><span data-stu-id="90670-144">Boxes</span></span>                   |
| <span data-ttu-id="90670-145">Faktor</span><span class="sxs-lookup"><span data-stu-id="90670-145">Factor</span></span>                | <span data-ttu-id="90670-146">4</span><span class="sxs-lookup"><span data-stu-id="90670-146">4</span></span>                       |
| <span data-ttu-id="90670-147">Til enhed</span><span class="sxs-lookup"><span data-stu-id="90670-147">To Unit</span></span>               | <span data-ttu-id="90670-148">Styk</span><span class="sxs-lookup"><span data-stu-id="90670-148">Pieces</span></span>                  |

<span data-ttu-id="90670-149">De frigivne produktvarianter lille, mellem og stor har samme enhedsomregning mellem enhedens Kasser og styk, hvilket betyder, at du kan definere enhedsomregningen for disse produktvarianter på produktmasteren.</span><span class="sxs-lookup"><span data-stu-id="90670-149">The Released product variants Small, Medium, and Large have the same unit conversion between the unit Box and Pieces, which means that you can define the unit conversion for these product variants on the product master.</span></span>

| <span data-ttu-id="90670-150">**Felt**</span><span class="sxs-lookup"><span data-stu-id="90670-150">**Field**</span></span>             | <span data-ttu-id="90670-151">**Indstilling**</span><span class="sxs-lookup"><span data-stu-id="90670-151">**Setting**</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="90670-152">Opret konvertering for</span><span class="sxs-lookup"><span data-stu-id="90670-152">Create conversion for</span></span> | <span data-ttu-id="90670-153">Produkt</span><span class="sxs-lookup"><span data-stu-id="90670-153">Product</span></span>     |
| <span data-ttu-id="90670-154">Produkt</span><span class="sxs-lookup"><span data-stu-id="90670-154">Product</span></span>               | <span data-ttu-id="90670-155">T-shirt</span><span class="sxs-lookup"><span data-stu-id="90670-155">T-Shirt</span></span>     |
| <span data-ttu-id="90670-156">Fra enhed</span><span class="sxs-lookup"><span data-stu-id="90670-156">From unit</span></span>             | <span data-ttu-id="90670-157">Kasser</span><span class="sxs-lookup"><span data-stu-id="90670-157">Boxes</span></span>       |
| <span data-ttu-id="90670-158">Faktor</span><span class="sxs-lookup"><span data-stu-id="90670-158">Factor</span></span>                | <span data-ttu-id="90670-159">5</span><span class="sxs-lookup"><span data-stu-id="90670-159">5</span></span>           |
| <span data-ttu-id="90670-160">Til enhed</span><span class="sxs-lookup"><span data-stu-id="90670-160">To Unit</span></span>               | <span data-ttu-id="90670-161">Styk</span><span class="sxs-lookup"><span data-stu-id="90670-161">Pieces</span></span>      |

### <a name="using-excel-to-update-the-unit-conversions"></a><span data-ttu-id="90670-162">Bruge Excel til at opdatere enhedsomregningerne</span><span class="sxs-lookup"><span data-stu-id="90670-162">Using Excel to update the unit conversions</span></span>

<span data-ttu-id="90670-163">Hvis et produkt har mange produktvarianter med forskellige enhedsomregninger, er det en god ide at eksportere enhedsomregninger fra siden **Enhedsomregning** til et Excel-regneark, opdatere konverteringerne og derefter publicere dem i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="90670-163">If a product has many product variants with different unit conversions, it's a good idea to export the unit conversions from the **Unit conversion** page to an Excel spreadsheet, update the conversions, and then publish them back to Finance and Operations.</span></span>

<span data-ttu-id="90670-164">Muligheden for at eksportere til Excel og publicere ændringerne i Finance and Operations aktiveres fra menupunktet **Åbn i Microsoft Office** i handlingsruden på siden **Enhedsomregning**.</span><span class="sxs-lookup"><span data-stu-id="90670-164">The option to export to Excel and publish the edits back to Finance and Operations is enabled from the **Open in Microsoft office** menu item on the Action Pane on the **Unit conversion** page.</span></span>
