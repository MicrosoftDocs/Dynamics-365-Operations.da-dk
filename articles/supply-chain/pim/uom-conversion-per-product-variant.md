---
title: Måleenhedskonvertering pr. produktvariant
description: Dette emne beskriver, hvordan du konfigurerer måleenhedskonverteringer for produktvarianter. Emnet indeholder et eksempel på opsætningen.
author: johanhoffmann
manager: tfehr
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: UnitOfMeasureConversion
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: ddb6c614ede98e46e46ff284a1a16669bbaaaf66
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5258041"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a><span data-ttu-id="178be-104">Måleenhedskonvertering pr. produktvariant</span><span class="sxs-lookup"><span data-stu-id="178be-104">Unit of measure conversion per product variant</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="178be-105">Dette emne beskriver, hvordan du konfigurerer måleenhedskonverteringer for forskellige produktvarianter.</span><span class="sxs-lookup"><span data-stu-id="178be-105">This topic explains how to set up unit of measure conversions for various product variants.</span></span>

<span data-ttu-id="178be-106">I stedet for at oprette flere individuelle produkter, der skal vedligeholdelse, kan du bruge produktvarianter til at oprette variationer af et enkelt produkt.</span><span class="sxs-lookup"><span data-stu-id="178be-106">Instead of creating multiple individual products that must be maintained, you can use product variants to create variations of a single product.</span></span> <span data-ttu-id="178be-107">En produktvariant kan f.eks. være en t-shirt af en given størrelse og farve.</span><span class="sxs-lookup"><span data-stu-id="178be-107">For example, a product variant might be a T-shirt of a given size and color.</span></span>

<span data-ttu-id="178be-108">Tidligere kunne enhedsomregninger kun konfigureres på produktmasteren.</span><span class="sxs-lookup"><span data-stu-id="178be-108">Previously, unit conversions could be set up only on the product master.</span></span> <span data-ttu-id="178be-109">Derfor har alle produktvarianter de samme regler for enhedsomregning.</span><span class="sxs-lookup"><span data-stu-id="178be-109">Therefore, all product variants had the same unit conversion rules.</span></span> <span data-ttu-id="178be-110">Men når funktionen *Enhedsomregninger for produktvarianter*, er slået til, hvis t-shirts sælges i kasser, og antallet af t-shirts, der kan pakkes i en kasse, afhænger af størrelsen på T-shirts, kan du nu konfigurere enhedsomregninger mellem de forskellige t-shirt-størrelser og de kasser der bruges til pakning.</span><span class="sxs-lookup"><span data-stu-id="178be-110">However, when the *Unit of measure conversions for product variants* feature is turned on, if your T-shirts are sold in boxes, and the number of T-shirts that can be packed in a box depends on the size of the T-shirts, you can now set up unit conversions between the different shirt sizes and the boxes that are used for packaging.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="178be-111">Aktivere funktionen i systemet</span><span class="sxs-lookup"><span data-stu-id="178be-111">Turn on the feature in your system</span></span>

<span data-ttu-id="178be-112">Hvis du ikke allerede kan se denne funktion i dit system, skal du gå til [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og aktivere funktionen *Enhedsomregninger for produktvarianter*.</span><span class="sxs-lookup"><span data-stu-id="178be-112">If you don't already see this feature in your system, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Unit of measure conversions for product variants* feature.</span></span>

## <a name="set-up-a-product-for-unit-conversion-per-variant"></a><span data-ttu-id="178be-113">Konfigurere et produkt til enhedsomregning pr. variant</span><span class="sxs-lookup"><span data-stu-id="178be-113">Set up a product for unit conversion per variant</span></span>

<span data-ttu-id="178be-114">Produktvarianter kan kun bruges til produkter, der er produktmastere.</span><span class="sxs-lookup"><span data-stu-id="178be-114">Product variants can be created only for products that are product masters.</span></span> <span data-ttu-id="178be-115">Du kan finde flere oplysninger i [Oprette en produktmaster](tasks/create-product-master.md).</span><span class="sxs-lookup"><span data-stu-id="178be-115">For more information, see [Create a product master](tasks/create-product-master.md).</span></span> <span data-ttu-id="178be-116">Funktionen *Enhedsomregninger for produktvarianter* er ikke tilgængelig for produkter, der er konfigureret til fastvægtsprocesser.</span><span class="sxs-lookup"><span data-stu-id="178be-116">The *Unit of measure conversions for product variants* feature isn't available for products that are set up for catch-weight processes.</span></span>

<span data-ttu-id="178be-117">Udfør følgende trin for at konfigurere en produktmaster til at understøtte enhedsomregning pr. variant:</span><span class="sxs-lookup"><span data-stu-id="178be-117">To configure a product master to support unit conversion per variant, follow these steps.</span></span>

1. <span data-ttu-id="178be-118">Gå til **Administration af produktoplysninger \> Produkter \> Produktmastere**.</span><span class="sxs-lookup"><span data-stu-id="178be-118">Go to **Product information management \> Products \> Product masters**.</span></span>
1. <span data-ttu-id="178be-119">Opret eller åbn en produktmaster for at gå til siden **Produktdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="178be-119">Create or open a product master to go to its **Product details** page.</span></span>
1. <span data-ttu-id="178be-120">Angiv indstillingen **Aktivér enhedsomregning** til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="178be-120">Set the **Enable unit of measure conversions** option to *Yes*.</span></span>
1. <span data-ttu-id="178be-121">Gå til handlingsruden, og vælg **Enhedsomregninger** i gruppen **Opsætning** under fanen **Produkt**.</span><span class="sxs-lookup"><span data-stu-id="178be-121">On the Action Pane, on the **Product** tab, in the **Set up** group, select **Unit conversions**.</span></span>
1. <span data-ttu-id="178be-122">Siden **Enhedsomregninger** åbnes.</span><span class="sxs-lookup"><span data-stu-id="178be-122">The **Unit conversions** page opens.</span></span> <span data-ttu-id="178be-123">Vælg én af følgende faner:</span><span class="sxs-lookup"><span data-stu-id="178be-123">Select one of the following tabs:</span></span>

    - <span data-ttu-id="178be-124">**Omregninger i klasser** – vælg denne fane for at konvertere mellem enheder, der tilhører samme enhedsklasse.</span><span class="sxs-lookup"><span data-stu-id="178be-124">**Intra-class conversions** – Select this tab to convert between units that belong to the same unit class.</span></span>
    - <span data-ttu-id="178be-125">**Omregninger mellem klasser** – vælg denne fane for at konvertere mellem enheder, der tilhører forskellige enhedsklasse.</span><span class="sxs-lookup"><span data-stu-id="178be-125">**Inter-class conversions** – Select this tab to convert between units that belong to different unit classes.</span></span>

1. <span data-ttu-id="178be-126">Vælg **Ny** for at tilføje en ny enhedsomregning.</span><span class="sxs-lookup"><span data-stu-id="178be-126">Select **New** to add a new unit conversion.</span></span>
1. <span data-ttu-id="178be-127">Indstil feltet **Opret omregning for** til en af følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="178be-127">Set the **Create conversion for** field to one of the following values:</span></span>

    - <span data-ttu-id="178be-128">**Produkt** – hvis du vælger denne værdi, kan du konfigurere en enhedsomregning for produktmasteren.</span><span class="sxs-lookup"><span data-stu-id="178be-128">**Product** – If you select this value, you can set up a unit conversion for the product master.</span></span> <span data-ttu-id="178be-129">Denne enhedsomregning vil blive brugt som reserve for alle produktvarianter, der ikke er defineret en enhedsomregning for.</span><span class="sxs-lookup"><span data-stu-id="178be-129">That unit conversion will be used as a fallback for all product variants that no unit conversion is defined for.</span></span>
    - <span data-ttu-id="178be-130">**Produktvariant** – hvis du vælger denne værdi, kan du konfigurere en enhedsomregning for en specifik produktvariant.</span><span class="sxs-lookup"><span data-stu-id="178be-130">**Product variant** – If you select this value, you can set up a unit conversion for a specific product variant.</span></span> <span data-ttu-id="178be-131">Brug feltet **Produktvariant** til at vælge varianten.</span><span class="sxs-lookup"><span data-stu-id="178be-131">Use the **Product variant** field to select the variant.</span></span>

    <span data-ttu-id="178be-132">![Tilføje en ny enhedsomregning](media/uom-new-conversion.png "Tilføje en ny enhedsomregning")</span><span class="sxs-lookup"><span data-stu-id="178be-132">![Adding a new unit conversion](media/uom-new-conversion.png "Adding a new unit conversion")</span></span>

1. <span data-ttu-id="178be-133">Brug de andre felter, der er angivet, til at konfigurere din enhedsomregning.</span><span class="sxs-lookup"><span data-stu-id="178be-133">Use the other fields that are provided to set up your unit conversion.</span></span>
1. <span data-ttu-id="178be-134">Vælg **OK** for at gemme den nye enhedsomregning.</span><span class="sxs-lookup"><span data-stu-id="178be-134">Select **OK** to save the new unit conversion.</span></span>

> [!TIP]
> <span data-ttu-id="178be-135">Du kan åbne siden **Enhedsomregninger** for et produkt eller en produktvariant fra en af følgende sider:</span><span class="sxs-lookup"><span data-stu-id="178be-135">You can open the **Unit conversions** page for a product or a product variant from any of the following pages:</span></span>
> 
> - <span data-ttu-id="178be-136">Produktdetaljer</span><span class="sxs-lookup"><span data-stu-id="178be-136">Product details</span></span>
> - <span data-ttu-id="178be-137">Frigivne produktdetaljer</span><span class="sxs-lookup"><span data-stu-id="178be-137">Released products details</span></span>
> - <span data-ttu-id="178be-138">Frigivne produktvarianter</span><span class="sxs-lookup"><span data-stu-id="178be-138">Released product variants</span></span>

## <a name="example-scenario"></a><span data-ttu-id="178be-139">Eksempelscenario</span><span class="sxs-lookup"><span data-stu-id="178be-139">Example scenario</span></span>

<span data-ttu-id="178be-140">I dette scenarie sælger et firma t-shirts i størrelserne lille, mellem, stor og ekstra stor.</span><span class="sxs-lookup"><span data-stu-id="178be-140">In this scenario, a company sells T-shirts in sizes small, medium, large, and extra-large.</span></span> <span data-ttu-id="178be-141">Disse t-shirts er defineret som et produkt, og de forskellige størrelser er defineret som varianter af det pågældende produkt.</span><span class="sxs-lookup"><span data-stu-id="178be-141">The T-shirt is defined as a product, and the different sizes are defined as variants of that product.</span></span> <span data-ttu-id="178be-142">T-shirtene er pakket i kasser.</span><span class="sxs-lookup"><span data-stu-id="178be-142">The shirts are packed in boxes.</span></span> <span data-ttu-id="178be-143">I størrelser lille, mellem og stor kan der være fem t-shirts i hver kasse.</span><span class="sxs-lookup"><span data-stu-id="178be-143">For sizes small, medium, and large, there can be five shirts in each box.</span></span> <span data-ttu-id="178be-144">Men i størrelsen ekstra stor er der kun plads til fire t-shirts i hver kasse.</span><span class="sxs-lookup"><span data-stu-id="178be-144">However, for size extra-large, there is space for only four shirts in each box.</span></span>

<span data-ttu-id="178be-145">Virksomheden ønsker at spore de forskellige varianter i enheden *Styk*, men sælger dem i enheden *Kasser*.</span><span class="sxs-lookup"><span data-stu-id="178be-145">The company wants to track the different variants in the *Pieces* unit, but it's selling them in the *Boxes* unit.</span></span> <span data-ttu-id="178be-146">I størrelserne lille, mellem og stor er omregningen mellem lagerenheden og salgsenheden 1 kasse = 5 stk.</span><span class="sxs-lookup"><span data-stu-id="178be-146">For sizes small, medium, and large, the conversion between the inventory unit and the sales unit is 1 Box = 5 Pieces.</span></span> <span data-ttu-id="178be-147">I størrelsen ekstra stor er omregningen 1 kasse = 4 styk.</span><span class="sxs-lookup"><span data-stu-id="178be-147">For size extra-large, the conversion is 1 Box = 4 Pieces.</span></span>

1. <span data-ttu-id="178be-148">På siden **Frigivne produktdetaljer** for produktet **T-shirt** skal du åbne siden **Enhedsomregninger**.</span><span class="sxs-lookup"><span data-stu-id="178be-148">From the **Released product details** page for the **T-Shirt** product, open the **Unit conversions** page.</span></span>
1. <span data-ttu-id="178be-149">På siden **Enhedsomregning** skal du konfigurere følgende enhedsomregning for den frigivning produktvariant **Ekstra stor**.</span><span class="sxs-lookup"><span data-stu-id="178be-149">On the **Unit conversions** page, set up the following unit conversion for the **X-Large** released product variant.</span></span>

    | <span data-ttu-id="178be-150">Felt</span><span class="sxs-lookup"><span data-stu-id="178be-150">Field</span></span>                 | <span data-ttu-id="178be-151">Indstilling</span><span class="sxs-lookup"><span data-stu-id="178be-151">Setting</span></span>                 |
    |-----------------------|-------------------------|
    | <span data-ttu-id="178be-152">Opret konvertering for</span><span class="sxs-lookup"><span data-stu-id="178be-152">Create conversion for</span></span> | <span data-ttu-id="178be-153">Produktvariant</span><span class="sxs-lookup"><span data-stu-id="178be-153">Product variant</span></span>         |
    | <span data-ttu-id="178be-154">Produktvariant</span><span class="sxs-lookup"><span data-stu-id="178be-154">Product variant</span></span>       | <span data-ttu-id="178be-155">T-shirt : : Ekstra stor : :</span><span class="sxs-lookup"><span data-stu-id="178be-155">T-Shirt : : X-Large : :</span></span> |
    | <span data-ttu-id="178be-156">Fra enhed</span><span class="sxs-lookup"><span data-stu-id="178be-156">From unit</span></span>             | <span data-ttu-id="178be-157">Kasser</span><span class="sxs-lookup"><span data-stu-id="178be-157">Boxes</span></span>                   |
    | <span data-ttu-id="178be-158">Faktor</span><span class="sxs-lookup"><span data-stu-id="178be-158">Factor</span></span>                | <span data-ttu-id="178be-159">4</span><span class="sxs-lookup"><span data-stu-id="178be-159">4</span></span>                       |
    | <span data-ttu-id="178be-160">Til enhed</span><span class="sxs-lookup"><span data-stu-id="178be-160">To Unit</span></span>               | <span data-ttu-id="178be-161">Styk</span><span class="sxs-lookup"><span data-stu-id="178be-161">Pieces</span></span>                  |

1. <span data-ttu-id="178be-162">Da produktvarianterne **Lille**, **Mellem** og **Stor** alle har samme enhedsomregning mellem *Kasse*- og *Styk*-enheder, kan du definere følgende enhedsomregning for dem på produktmasteren.</span><span class="sxs-lookup"><span data-stu-id="178be-162">Because the **Small**, **Medium**, and **Large** product variants all have the same unit conversion between the *Box* and *Pieces* units, you can define the following unit conversion for them on the product master.</span></span>

    | <span data-ttu-id="178be-163">Felt</span><span class="sxs-lookup"><span data-stu-id="178be-163">Field</span></span>                 | <span data-ttu-id="178be-164">Indstilling</span><span class="sxs-lookup"><span data-stu-id="178be-164">Setting</span></span> |
    |-----------------------|---------|
    | <span data-ttu-id="178be-165">Opret konvertering for</span><span class="sxs-lookup"><span data-stu-id="178be-165">Create conversion for</span></span> | <span data-ttu-id="178be-166">Produkt</span><span class="sxs-lookup"><span data-stu-id="178be-166">Product</span></span> |
    | <span data-ttu-id="178be-167">Produkt</span><span class="sxs-lookup"><span data-stu-id="178be-167">Product</span></span>               | <span data-ttu-id="178be-168">T-shirt</span><span class="sxs-lookup"><span data-stu-id="178be-168">T-Shirt</span></span> |
    | <span data-ttu-id="178be-169">Fra enhed</span><span class="sxs-lookup"><span data-stu-id="178be-169">From unit</span></span>             | <span data-ttu-id="178be-170">Kasser</span><span class="sxs-lookup"><span data-stu-id="178be-170">Boxes</span></span>   |
    | <span data-ttu-id="178be-171">Faktor</span><span class="sxs-lookup"><span data-stu-id="178be-171">Factor</span></span>                | <span data-ttu-id="178be-172">5</span><span class="sxs-lookup"><span data-stu-id="178be-172">5</span></span>       |
    | <span data-ttu-id="178be-173">Til enhed</span><span class="sxs-lookup"><span data-stu-id="178be-173">To Unit</span></span>               | <span data-ttu-id="178be-174">Styk</span><span class="sxs-lookup"><span data-stu-id="178be-174">Pieces</span></span>  |

## <a name="using-excel-to-update-the-unit-conversions"></a><span data-ttu-id="178be-175">Bruge Excel til at opdatere enhedsomregningerne</span><span class="sxs-lookup"><span data-stu-id="178be-175">Using Excel to update the unit conversions</span></span>

<span data-ttu-id="178be-176">Hvis et produkt har mange produktvarianter, der har forskellige enhedsomregninger, er det en god ide at eksportere enhedsomregninger til en Microsoft Excel-projektmappe, opdatere dem og derefter udgive dem igen i Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="178be-176">If a product has many product variants that have different unit conversions, it's a good idea to export the unit conversions to a Microsoft Excel workbook, update them, and then publish them back to Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="178be-177">Hvis du vil eksportere enhedsomregninger til Excel, skal du på siden **Enhedsomregninger** vælge **Åbn i Microsoft Office** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="178be-177">To export unit conversions to Excel, on the **Unit conversions** page, on the Action Pane, select **Open in Microsoft Office**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="178be-178">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="178be-178">Additional resources</span></span>

[<span data-ttu-id="178be-179">Administrere måleenhed</span><span class="sxs-lookup"><span data-stu-id="178be-179">Manage unit of measure</span></span>](tasks/manage-unit-measure.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]