---
title: Administrere måleenheder
description: Dette emne beskriver, hvordan du definerer en måleenhed, angiver oversættelser for enheden og dens beskrivelse og definerer omregningsregler for relaterede enheder.
author: sorenva
ms.date: 04/09/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup, UnitOfMeasureCalculator, UnitOfMeasureWizard, UnitOfMeasureLookupTest
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d36839cd8e3398225d3421bf0f268068599ca49f
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921335"
---
# <a name="manage-units-of-measure"></a><span data-ttu-id="97a5f-103">Administrere måleenheder</span><span class="sxs-lookup"><span data-stu-id="97a5f-103">Manage units of measure</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="97a5f-104">Dette emne beskriver, hvordan du definerer en måleenhed, angiver oversættelser for enheden og dens beskrivelse og definerer omregningsregler for relaterede enheder.</span><span class="sxs-lookup"><span data-stu-id="97a5f-104">This topic describes how to define a unit of measure, provide translations for the unit and its description, and define conversion rules for related units.</span></span>

## <a name="open-the-units-page"></a><span data-ttu-id="97a5f-105">Åbne siden Enheder</span><span class="sxs-lookup"><span data-stu-id="97a5f-105">Open the Units page</span></span>

<span data-ttu-id="97a5f-106">Hvis du vil oprette og arbejde med de måleenheder, der er tilgængelige i systemet, skal du gå til **Organisationsadministration \> Opsætning \> Enheder \> enheder**.</span><span class="sxs-lookup"><span data-stu-id="97a5f-106">To create and work with the units of measure that are available in your system, go to **Organization administration \> Setup \> Units \> Units**.</span></span>

<span data-ttu-id="97a5f-107">I de resterende afsnit i dette emne beskriver, hvad du kan gøre på siden **Enheder**.</span><span class="sxs-lookup"><span data-stu-id="97a5f-107">The remaining sections of this topic describe what you can do on the **Units** page.</span></span>

## <a name="create-standard-units-and-conversions"></a><span data-ttu-id="97a5f-108">Oprette standardenheder og -omregninger</span><span class="sxs-lookup"><span data-stu-id="97a5f-108">Create standard units and conversions</span></span>

<span data-ttu-id="97a5f-109">Hvis systemet ikke allerede indeholder de mest almindelige måleenheder for det metriske system og/eller det amerikanske målesystem (USCS), kan guiden Enhedsopsætning hjælpe dig med hurtigt at komme i gang med grundlæggende enhedsdefinitioner og -omregninger.</span><span class="sxs-lookup"><span data-stu-id="97a5f-109">If your system doesn't already include the most commonly used units of measure for the metric system and/or the US customary system (USCS), the unit setup wizard can help you quickly get started with basic unit definitions and conversions.</span></span> <span data-ttu-id="97a5f-110">Hvis du vil fuldføre guiden, skal du vælge **Guide til oprettelse af enhed** i handlingsruden og derefter følge instruktionerne på skærmen.</span><span class="sxs-lookup"><span data-stu-id="97a5f-110">To complete the wizard, select **Unit creation wizard** on the Action Pane, and then follow the on-screen instructions.</span></span>

## <a name="create-or-edit-a-unit-of-measure"></a><span data-ttu-id="97a5f-111">Oprette eller redigere en måleenhed</span><span class="sxs-lookup"><span data-stu-id="97a5f-111">Create or edit a unit of measure</span></span>

<span data-ttu-id="97a5f-112">Benyt følgende fremgangsmåde for at oprette eller redigere en måleenhed.</span><span class="sxs-lookup"><span data-stu-id="97a5f-112">To create or edit a unit of measure, follow these steps.</span></span>

1. <span data-ttu-id="97a5f-113">Udfør ét af følgende trin:</span><span class="sxs-lookup"><span data-stu-id="97a5f-113">Follow one of these steps:</span></span>

    - <span data-ttu-id="97a5f-114">Hvis du vil redigere en eksisterende enhed, skal du vælge den i listeruden.</span><span class="sxs-lookup"><span data-stu-id="97a5f-114">To edit an existing unit, select it in the list pane.</span></span>
    - <span data-ttu-id="97a5f-115">Vælg **Ny** i handlingsruden for at oprette en ny enhed.</span><span class="sxs-lookup"><span data-stu-id="97a5f-115">To create a new unit, select **New** on the Action Pane.</span></span>

1. <span data-ttu-id="97a5f-116">Angiv følgende felter i postens hoved:</span><span class="sxs-lookup"><span data-stu-id="97a5f-116">On the header of the record, set the following fields:</span></span>

    - <span data-ttu-id="97a5f-117">**Enhed** – Angiv det id eller symbol, der skal bruges til at referere til enheden på systemsproget.</span><span class="sxs-lookup"><span data-stu-id="97a5f-117">**Unit** – Enter the ID or symbol to use to refer to the unit in the system language.</span></span> <span data-ttu-id="97a5f-118">Dette id eller symbol er normalt en almindelig forkortelse for enheden, f.eks. *stk.* for hver eller *cm* for centimeter.</span><span class="sxs-lookup"><span data-stu-id="97a5f-118">This ID or symbol is usually a common abbreviation for the unit, such as *ea* for each or *cm* for centimeter.</span></span>
    - <span data-ttu-id="97a5f-119">**Beskrivelse** – Indtast et beskrivende navn for enheden i systemsproget.</span><span class="sxs-lookup"><span data-stu-id="97a5f-119">**Description** – Enter a descriptive name for the unit in the system language.</span></span> <span data-ttu-id="97a5f-120">Dette navn er normalt det fulde navn på enheden som f.eks. *Hver* eller *Centimeter*.</span><span class="sxs-lookup"><span data-stu-id="97a5f-120">This name is usually the full name of the unit, such as *Each* or *Centimeter*.</span></span>

1. <span data-ttu-id="97a5f-121">I oversigtspanelet **Generelt** skal du indstille følgende felter:</span><span class="sxs-lookup"><span data-stu-id="97a5f-121">On the **General** FastTab, set the following fields:</span></span><!-- KFM: confirm this:    - **Fixed unit assignment** and **Fixed unit** – These fields have an effect only if you're using the Microsoft Retail Essentials product. If the current unit can be mapped to one of the fixed units that are used by Retail Essentials, set the **Fixed unit assignment** option to *Yes*. Then select the fixed unit in the **Fixed unit** field. -->

    - <span data-ttu-id="97a5f-122">**Enhedsklasse** – Vælg den egenskab, som enheden måler (f.eks. længde, område, masse eller antal).</span><span class="sxs-lookup"><span data-stu-id="97a5f-122">**Unit class** – Select the property that the unit measures (such as length, area, mass, or quantity).</span></span>
    - <span data-ttu-id="97a5f-123">**Enhedssystem** – Vælg det målingssystem, som enheden tilhører (*Metriske enheder* eller *Amerikanske måleenheder*).</span><span class="sxs-lookup"><span data-stu-id="97a5f-123">**System of units** – Select the measurement system that the unit belongs to (*Metric units* or *United States customary units*).</span></span>
    - <span data-ttu-id="97a5f-124">**Basisenhed** – Angiv denne indstilling til *Ja*, hvis du vil bruge den aktuelle enhed som basisenhed for enhedsklassen.</span><span class="sxs-lookup"><span data-stu-id="97a5f-124">**Base unit** – Set this option to *Yes* to use the current unit as the base unit for its unit class.</span></span> <span data-ttu-id="97a5f-125">I så fald skal du kun angive omregningsfaktoren mellem basisenheden og hver ekstra enhed i enhedsklassen.</span><span class="sxs-lookup"><span data-stu-id="97a5f-125">In this case, you only have to specify the conversion factor between the base unit and each additional unit in the unit class.</span></span> <span data-ttu-id="97a5f-126">Derefter kan systemet omregne alle enheder i enhedsklassen.</span><span class="sxs-lookup"><span data-stu-id="97a5f-126">The system can then convert between all units in that unit class.</span></span> <span data-ttu-id="97a5f-127">Derfor er det lettere at konfigurere omregninger.</span><span class="sxs-lookup"><span data-stu-id="97a5f-127">Therefore, it's easier to set up conversions.</span></span>

        <span data-ttu-id="97a5f-128">Hvis gallon f.eks. er basisenheden for enhedsklassen *Volumen*, skal du kun konfigurere omregningsfaktorer fra quart til gallon og fra pint til gallon.</span><span class="sxs-lookup"><span data-stu-id="97a5f-128">For example, if gallon is the base unit for the *Volume* unit class, you only have to set up conversion factors from quart to gallon and from pint to gallon.</span></span> <span data-ttu-id="97a5f-129">Systemet kan derefter også omregne quart til pint.</span><span class="sxs-lookup"><span data-stu-id="97a5f-129">The system can then also convert from quart to pint.</span></span>

        <span data-ttu-id="97a5f-130">Du kan kun have én basisenhed pr. enhedsklasse.</span><span class="sxs-lookup"><span data-stu-id="97a5f-130">You can have only one base unit per unit class.</span></span>

    - <span data-ttu-id="97a5f-131">**Systemenhed** – Angiv denne indstilling til *Ja*, hvis du vil bruge den aktuelle enhed som antaget enhed for alle uspecificerede målinger i enhedsklassen.</span><span class="sxs-lookup"><span data-stu-id="97a5f-131">**System unit** – Set this option to *Yes* to use the current unit as the assumed unit for all unspecified measurements in its unit class.</span></span> <span data-ttu-id="97a5f-132">Hvis et felt, der bruges til at angive et antal, f.eks. ikke tillader, at der angives en enhed (eller hvis brugeren ikke vælger en enhed), bruger systemet den enhed, der er angivet som systemenhed for enhedsklassen *Antal*.</span><span class="sxs-lookup"><span data-stu-id="97a5f-132">For example, if a field that is used to enter a quantity doesn't allow a unit to be specified (of if the user doesn't select a unit), the system uses the unit that is set as the system unit for the *Quantity* unit class.</span></span> <span data-ttu-id="97a5f-133">Du kan kun have én systemenhed pr. enhedsklasse.</span><span class="sxs-lookup"><span data-stu-id="97a5f-133">You can have only one system unit per unit class.</span></span>
    - <span data-ttu-id="97a5f-134">**Decimalpræcision** – Angiv det antal decimaler, som værdier, der er angivet for den aktuelle enhed eller omregnet til den, skal afrundes til.</span><span class="sxs-lookup"><span data-stu-id="97a5f-134">**Decimal precision** – Specify the number of decimal places that values that are specified for the current unit or converted to it should be rounded to.</span></span>

1. <span data-ttu-id="97a5f-135">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="97a5f-135">On the Action Pane, select **Save**.</span></span>

## <a name="define-unit-translations"></a><span data-ttu-id="97a5f-136">Definer enhedsoversættelser</span><span class="sxs-lookup"><span data-stu-id="97a5f-136">Define unit translations</span></span>

<span data-ttu-id="97a5f-137">Hvis du vil definere oversættelser for id'et eller symbolet og beskrivelsen af en måleenhed, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="97a5f-137">To define translations for the ID or symbol and the description for a unit of measure, follow these steps.</span></span>

1. <span data-ttu-id="97a5f-138">Opret eller vælg den enhed, der skal oprettes oversættelser for.</span><span class="sxs-lookup"><span data-stu-id="97a5f-138">Create or select the unit to create translations for.</span></span>
1. <span data-ttu-id="97a5f-139">Vælg **Enhedstekster** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="97a5f-139">On the Action Pane, select **Unit texts**.</span></span>

    <span data-ttu-id="97a5f-140">Siden **Enhedstekster** vises.</span><span class="sxs-lookup"><span data-stu-id="97a5f-140">The **Unit texts** page appears.</span></span> <span data-ttu-id="97a5f-141">Du kan bruge denne side til at definere oversættelser for id'et eller symbolet for den valgte enhed.</span><span class="sxs-lookup"><span data-stu-id="97a5f-141">You use this page to define translations for the ID or symbol for the selected unit.</span></span> <span data-ttu-id="97a5f-142">Disse oversættelser kan derefter bruges på eksterne dokumenter på kundespecifikke eller leverandørspecifikke sprog.</span><span class="sxs-lookup"><span data-stu-id="97a5f-142">Those translations can then be used on external documents in customer-specific or vendor-specific languages.</span></span>

1. <span data-ttu-id="97a5f-143">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="97a5f-143">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="97a5f-144">I feltet **Sprog** skal du vælge det sprog, som du vil oversætte enhedens id eller symbol til.</span><span class="sxs-lookup"><span data-stu-id="97a5f-144">In the **Language** field, select the language to translate the unit ID or symbol to.</span></span>
1. <span data-ttu-id="97a5f-145">Angiv oversættelsen af enheds-id'et eller symbolet på det valgte sprog i feltet **Tekst**.</span><span class="sxs-lookup"><span data-stu-id="97a5f-145">In the **Text** field, enter the translation of the unit ID or symbol in the selected language.</span></span>
1. <span data-ttu-id="97a5f-146">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="97a5f-146">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="97a5f-147">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="97a5f-147">Close the page.</span></span>
1. <span data-ttu-id="97a5f-148">Vælg **Oversatte enhedsbeskrivelser** i **Handlingsrude**.</span><span class="sxs-lookup"><span data-stu-id="97a5f-148">On the **Action Pane**, select **Translated unit descriptions**.</span></span>

    <span data-ttu-id="97a5f-149">Siden **Oversatte enhedsbeskrivelser** vises.</span><span class="sxs-lookup"><span data-stu-id="97a5f-149">The **Translated unit descriptions** page appears.</span></span> <span data-ttu-id="97a5f-150">Du kan bruge denne side til at definere sprogspecifikke beskrivelser af den valgte enhed.</span><span class="sxs-lookup"><span data-stu-id="97a5f-150">You use this page to define language-specific descriptions for the selected unit.</span></span>

1. <span data-ttu-id="97a5f-151">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="97a5f-151">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="97a5f-152">I feltet **Sprog** skal du vælge det sprog, som du vil oversætte enhedsbeskrivelsen til.</span><span class="sxs-lookup"><span data-stu-id="97a5f-152">In the **Language** field, select the language to translate the unit description to.</span></span>
1. <span data-ttu-id="97a5f-153">Angiv oversættelsen af enhedsbeskrivelsen på det valgte sprog i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="97a5f-153">In the **Description** field, enter the translation of the unit description in the selected language.</span></span>
1. <span data-ttu-id="97a5f-154">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="97a5f-154">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="97a5f-155">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="97a5f-155">Close the page.</span></span>

## <a name="define-unit-conversion-rules"></a><span data-ttu-id="97a5f-156">Definer omregningsregler for enhed</span><span class="sxs-lookup"><span data-stu-id="97a5f-156">Define unit conversion rules</span></span>

<span data-ttu-id="97a5f-157">Hvis du vil definere regler for omregninger mellem måleenheder, skal du benytte følgende fremgangsmåde.</span><span class="sxs-lookup"><span data-stu-id="97a5f-157">To define rules for conversions between units of measure, follow these steps.</span></span>

1. <span data-ttu-id="97a5f-158">Opret eller vælg den enhed, du vil definere omregningsregler for.</span><span class="sxs-lookup"><span data-stu-id="97a5f-158">Create or select the unit to define conversion rules for.</span></span>
1. <span data-ttu-id="97a5f-159">Vælg **Enhedsomregninger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="97a5f-159">On the Action Pane, select **Unit conversions**.</span></span>

    <span data-ttu-id="97a5f-160">Siden **Enhedsomregninger** åbnes.</span><span class="sxs-lookup"><span data-stu-id="97a5f-160">The **Unit conversions** page appears.</span></span> <span data-ttu-id="97a5f-161">Du kan bruge denne side til at definere regler for omregning af den valgte enhed til og fra andre enheder i enhedsklassen.</span><span class="sxs-lookup"><span data-stu-id="97a5f-161">You use this page to define rules for converting the selected unit to and from other units in the unit class.</span></span>

1. <span data-ttu-id="97a5f-162">Vælg en af følgende faner, afhængigt af den type omregning, som du vil konfigurere:</span><span class="sxs-lookup"><span data-stu-id="97a5f-162">Select one of the following tabs, depending on the type of conversion that you want to set up:</span></span>

    - <span data-ttu-id="97a5f-163">**Standardomregninger** – Konfigurer standardomregningsregler for alle produkter.</span><span class="sxs-lookup"><span data-stu-id="97a5f-163">**Standard conversions** – Set up standard conversion rules for all products.</span></span>
    - <span data-ttu-id="97a5f-164">**Omregninger i klasser** – Konfigurer produktspecifikke omregningsregler for enheder i samme enhedsklasse.</span><span class="sxs-lookup"><span data-stu-id="97a5f-164">**Intra-class conversions** – Set up product-specific conversion rules for units in the same unit class.</span></span>
    - <span data-ttu-id="97a5f-165">**Omregninger mellem klasser** – Konfigurer produktspecifikke omregningsregler for enheder på tværs af enhedsklasser.</span><span class="sxs-lookup"><span data-stu-id="97a5f-165">**Inter-class conversions** – Set up product-specific conversion rules for units across unit classes.</span></span>

1. <span data-ttu-id="97a5f-166">Udfør ét af følgende trin:</span><span class="sxs-lookup"><span data-stu-id="97a5f-166">Follow one of these steps:</span></span>

    - <span data-ttu-id="97a5f-167">Vælg **Ny** på værktøjslinjen for at oprette en ny omregning.</span><span class="sxs-lookup"><span data-stu-id="97a5f-167">To create a new conversion, select **New** on the toolbar.</span></span>
    - <span data-ttu-id="97a5f-168">Hvis du vil redigere en eksisterende omregning, skal du markere omregningen i gitteret og derefter vælge **Rediger** på værktøjslinjen.</span><span class="sxs-lookup"><span data-stu-id="97a5f-168">To edit an existing conversion, select the conversion in the grid, and then select **Edit** on the toolbar.</span></span>

1. <span data-ttu-id="97a5f-169">Angiv følgende felter i den viste dialogboks med rullepanel:</span><span class="sxs-lookup"><span data-stu-id="97a5f-169">In the drop-down dialog box that appears, set the following fields:</span></span>

    - <span data-ttu-id="97a5f-170">**Produkt** – Vælg det specifikke produkt, som omregningen gælder for.</span><span class="sxs-lookup"><span data-stu-id="97a5f-170">**Product** – Select the specific product that the conversion applies to.</span></span> <span data-ttu-id="97a5f-171">Dette felt er kun tilgængeligt ved omregninger i og mellem klasser.</span><span class="sxs-lookup"><span data-stu-id="97a5f-171">This field is available only for intra-class and inter-class conversions.</span></span>
    - <span data-ttu-id="97a5f-172">**Formellayout** – Lad dette felt være angivet til *Simpel* for at angive en simpel omregning, der har en enkelt faktor.</span><span class="sxs-lookup"><span data-stu-id="97a5f-172">**Formula layout** – Leave this field set to *Simple* to specify a simple conversion that has a single factor.</span></span> <span data-ttu-id="97a5f-173">Angiv den til *Avanceret* for at konfigurere en mere kompleks ligning.</span><span class="sxs-lookup"><span data-stu-id="97a5f-173">Set it to *Advanced* to set up a more complex equation.</span></span> <span data-ttu-id="97a5f-174">Formatet for avancerede ligninger varierer, afhængigt af enhedsklassen.</span><span class="sxs-lookup"><span data-stu-id="97a5f-174">The format for advanced equations varies, depending on the unit class.</span></span>
    - <span data-ttu-id="97a5f-175">**Fra enhed** – Dette felt viser den valgte enhed.</span><span class="sxs-lookup"><span data-stu-id="97a5f-175">**From unit** – This field shows the selected unit.</span></span> <span data-ttu-id="97a5f-176">Normalt skal du ikke ændre værdien.</span><span class="sxs-lookup"><span data-stu-id="97a5f-176">Usually, you should not change the value.</span></span> <span data-ttu-id="97a5f-177">(Hvis du ændrer værdien, skal du åbne Siden **Enhedsomregninger** for den valgte enhed for at få vist den nye omregning, når du har gemt den.)</span><span class="sxs-lookup"><span data-stu-id="97a5f-177">(If you do change the value, you must open the **Unit conversions** page for the selected unit to view your new conversion after you save it.)</span></span>
    - <span data-ttu-id="97a5f-178">**Til enhed** – Vælg den enhed, der skal omregnes til.</span><span class="sxs-lookup"><span data-stu-id="97a5f-178">**To unit** – Select the unit to convert to.</span></span>
    - <span data-ttu-id="97a5f-179">**Afrunding** – Vælg, hvordan brøkdele skal afrundes baseret på værdien for **Decimalpræcision** for den valgte enhed (*Til nærmeste*, *Op* eller *Ned*).</span><span class="sxs-lookup"><span data-stu-id="97a5f-179">**Rounding** – Select how fractions should be rounded, based on the **Decimal precision** value of the selected unit (*To nearest*, *Up*, or *Down*).</span></span>
    - <span data-ttu-id="97a5f-180">**Omregningsformel** – Brug de resterende felter øverst i dialogboksen med rullelisten til at angive formlen for omregning mellem de to enheder.</span><span class="sxs-lookup"><span data-stu-id="97a5f-180">**Conversion formula** – Use the remaining fields at the top of the drop-down dialog box to specify the formula for converting between the two units.</span></span> <span data-ttu-id="97a5f-181">De tilgængelige felter varierer, afhængigt af enhedsklassen og det formellayout, du har valgt.</span><span class="sxs-lookup"><span data-stu-id="97a5f-181">The available fields vary, depending on the unit class and formula layout that you've selected.</span></span>

1. <span data-ttu-id="97a5f-182">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="97a5f-182">Select **OK**.</span></span>
1. <span data-ttu-id="97a5f-183">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="97a5f-183">Close the page.</span></span>

> [!TIP]
> <span data-ttu-id="97a5f-184">Du kan også konfigurere enhedsomregninger pr. produktvariant.</span><span class="sxs-lookup"><span data-stu-id="97a5f-184">You can also set up unit conversions per product variant.</span></span> <span data-ttu-id="97a5f-185">Du kan finde flere oplysninger i [Måleenhedsomregning pr. produktvariant](../uom-conversion-per-product-variant.md).</span><span class="sxs-lookup"><span data-stu-id="97a5f-185">For more information, see [Unit of measure conversion per product variant](../uom-conversion-per-product-variant.md).</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
