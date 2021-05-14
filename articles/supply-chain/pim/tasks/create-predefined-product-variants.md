---
title: Oprette foruddefinerede produktvarianter
description: Denne procedure fører dig gennem oprettelsen af produktvarianter for en produktmaster ved hjælp af kombinationer af produktdimensioner.
author: t-benebo
manager: tfehr
ms.date: 04/22/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions, EcoResProductVariantsPendingReleaseFormPart, EcoResProductVariantSuggestionsEnhanced
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: acd2e3f1464dfed09ee24764270b06970b747d7c
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938196"
---
# <a name="predefined-product-variants"></a><span data-ttu-id="e9efd-103">Foruddefinerede produktvarianter</span><span class="sxs-lookup"><span data-stu-id="e9efd-103">Predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="example-scenario-create-predefined-product-variants"></a><span data-ttu-id="e9efd-104">Eksempelscenarie: Oprette foruddefinerede produktvarianter</span><span class="sxs-lookup"><span data-stu-id="e9efd-104">Example scenario: Create predefined product variants</span></span>

<span data-ttu-id="e9efd-105">Dette eksempelscenarie viser, hvordan du opretter produktvarianter for en produktmaster ved hjælp af kombinationer af produktdimensioner.</span><span class="sxs-lookup"><span data-stu-id="e9efd-105">This example scenario shows how to create product variants for a product master using a combinations of product dimensions.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="e9efd-106">Gøre demodata tilgængelige</span><span class="sxs-lookup"><span data-stu-id="e9efd-106">Make demo data available</span></span>

<span data-ttu-id="e9efd-107">Hvis du vil følge dette scenarie ved hjælp af de foreslåede værdier, skal du have installeret demodata, og du skal bruge den juridiske enhed *USMF*.</span><span class="sxs-lookup"><span data-stu-id="e9efd-107">To follow this scenario using the values suggested here, you must have demo data installed, and you must select the *USMF* legal entity.</span></span>

### <a name="step-1-create-a-product-master"></a><span data-ttu-id="e9efd-108">Trin 1: Opret en produktmaster</span><span class="sxs-lookup"><span data-stu-id="e9efd-108">Step 1: Create a product master</span></span>

<span data-ttu-id="e9efd-109">Sådan oprettes en produktmaster:</span><span class="sxs-lookup"><span data-stu-id="e9efd-109">To create a product master:</span></span>

1. <span data-ttu-id="e9efd-110">Gå til **Administration af produktoplysninger > Produkter > Produktmastere**.</span><span class="sxs-lookup"><span data-stu-id="e9efd-110">Go to **Product information management > Products > Product masters**.</span></span>
1. <span data-ttu-id="e9efd-111">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="e9efd-111">Select **New**.</span></span>
1. <span data-ttu-id="e9efd-112">Hvis feltet **Produktnummer** ikke allerede viser et tal, skal du angive en værdi.</span><span class="sxs-lookup"><span data-stu-id="e9efd-112">If the **Product number** field doesn't already show a number, then enter a value.</span></span> <span data-ttu-id="e9efd-113">Dette trin er kun påkrævet, hvis der ikke er oprettet nogen nummerserie for dette felt.</span><span class="sxs-lookup"><span data-stu-id="e9efd-113">This is only required if no number sequence has been set for this field.</span></span>
1. <span data-ttu-id="e9efd-114">Indtast en navn i feltet **Produktnavn**.</span><span class="sxs-lookup"><span data-stu-id="e9efd-114">Enter a name in the **Product name** field.</span></span>
1. <span data-ttu-id="e9efd-115">I feltet **Produktdimensionsgruppe** skal du vælge produktdimensionsgruppen *SizeCol* (Størrelse og Farve).</span><span class="sxs-lookup"><span data-stu-id="e9efd-115">In the **Product dimension group** field, select the product dimension group *SizeCol* (Size and Color).</span></span>
1. <span data-ttu-id="e9efd-116">Vælg **OK** for at oprette og åbne den nye produktmaster.</span><span class="sxs-lookup"><span data-stu-id="e9efd-116">Select **OK** to create and open the new product master.</span></span>

### <a name="step-2-add-product-dimensions"></a><span data-ttu-id="e9efd-117">Trin 2: Tilføj produktdimensioner</span><span class="sxs-lookup"><span data-stu-id="e9efd-117">Step 2: Add product dimensions</span></span>

<span data-ttu-id="e9efd-118">Dette eksempel viser, hvordan du manuelt angiver produktdimensioner.</span><span class="sxs-lookup"><span data-stu-id="e9efd-118">This example shows how to manually enter product dimensions.</span></span> <span data-ttu-id="e9efd-119">Du kan også vælge en størrelses-, farve- eller typografigruppe, der indeholder de produktdimensionsværdier, du vil bruge.</span><span class="sxs-lookup"><span data-stu-id="e9efd-119">You can also choose to select a size, color, or style group that includes the product dimension values you want to use.</span></span>

<span data-ttu-id="e9efd-120">Sådan tilføjes produktdimensioner:</span><span class="sxs-lookup"><span data-stu-id="e9efd-120">To add product dimensions:</span></span>

1. <span data-ttu-id="e9efd-121">Når den nye produktmaster stadig er åben, skal du vælge **Produktdimensioner** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="e9efd-121">With your new product master still open, select **Product dimensions** on the Action Pane.</span></span>
1. <span data-ttu-id="e9efd-122">Åbn fanen **Størrelse**, og vælg **Ny** på værktøjslinjen for at føje en række til gitteret.</span><span class="sxs-lookup"><span data-stu-id="e9efd-122">Open the **Size** tab and select **New** on the toolbar to add a row to the grid.</span></span> <span data-ttu-id="e9efd-123">Angiv følgende indstillinger for den nye række:</span><span class="sxs-lookup"><span data-stu-id="e9efd-123">Make the following settings for the new row:</span></span>
    - <span data-ttu-id="e9efd-124">**Størrelse:** Vælg en størrelsesværdi.</span><span class="sxs-lookup"><span data-stu-id="e9efd-124">**Size:** Select a size value.</span></span>
    - <span data-ttu-id="e9efd-125">**Navn:** Angiv et navn til størrelsen.</span><span class="sxs-lookup"><span data-stu-id="e9efd-125">**Name:** Enter a name for the size.</span></span>
1. <span data-ttu-id="e9efd-126">Vælg **Ny** på værktøjslinjen, og føj endnu en størrelse til gitteret med en ny **Størrelse** og et nyt **Navn**.</span><span class="sxs-lookup"><span data-stu-id="e9efd-126">Select **New** on the toolbar and add a second size to the grid with a new **Size** and **Name**.</span></span>
1. <span data-ttu-id="e9efd-127">Åbn fanen **Farver**, og vælg **Ny** på værktøjslinjen for at føje en række til gitteret.</span><span class="sxs-lookup"><span data-stu-id="e9efd-127">Open the **Colors** tab and select **New** on the toolbar to add a row to the grid.</span></span> <span data-ttu-id="e9efd-128">Angiv følgende indstillinger for den nye række:</span><span class="sxs-lookup"><span data-stu-id="e9efd-128">Make the following settings for the new row:</span></span>
    - <span data-ttu-id="e9efd-129">**Farve:** Vælg en farveværdi.</span><span class="sxs-lookup"><span data-stu-id="e9efd-129">**Color:** Select a color value.</span></span>
    - <span data-ttu-id="e9efd-130">**Navn:** Angiv et navn til farven.</span><span class="sxs-lookup"><span data-stu-id="e9efd-130">**Name:** Enter a name for the color.</span></span>
1. <span data-ttu-id="e9efd-131">Vælg **Ny** på værktøjslinjen, og føj endnu en farve til gitteret med en ny **Farve** og et nyt **Navn**.</span><span class="sxs-lookup"><span data-stu-id="e9efd-131">Select **New** on the toolbar and add a second color to the grid with a new **Color** and **Name**.</span></span>
1. <span data-ttu-id="e9efd-132">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="e9efd-132">Select **Save**.</span></span>
1. <span data-ttu-id="e9efd-133">Luk siden for at vende tilbage til den nye produktmaster.</span><span class="sxs-lookup"><span data-stu-id="e9efd-133">Close the page to return to your new product master.</span></span>

### <a name="step-3-generate-product-variants"></a><span data-ttu-id="e9efd-134">Trin 3: Generer produktvarianter</span><span class="sxs-lookup"><span data-stu-id="e9efd-134">Step 3: Generate product variants</span></span>

> [!NOTE]
> <span data-ttu-id="e9efd-135">I dette afsnit beskrives, hvordan du kan generere produktvarianter, når funktionen *Forbedringer af sider med variantforslag* ikke er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="e9efd-135">This section describes how to generate product variants when the *Variant suggestions page improvements* feature isn't enabled.</span></span> <span data-ttu-id="e9efd-136">Se næste afsnit for at få oplysninger om, hvordan du kan generere produktvarianter, når funktionen er tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="e9efd-136">See the next section for details about how to generate product variants when that feature is available.</span></span>

<span data-ttu-id="e9efd-137">Sådan genereres produktvarianter:</span><span class="sxs-lookup"><span data-stu-id="e9efd-137">To generate product variants:</span></span>

1. <span data-ttu-id="e9efd-138">Når den nye produktmaster stadig er åben, skal du vælge **Produktvarianter** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="e9efd-138">With your new product master still open, select **Product variants** on the Action Pane.</span></span>
1. <span data-ttu-id="e9efd-139">Vælg **Variantforslag** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="e9efd-139">Select **Variant suggestions** on the Action Pane.</span></span>
1. <span data-ttu-id="e9efd-140">Systemet genererer en liste over alle de mulige kombinationer af de størrelser og farver, du har defineret for produktet.</span><span class="sxs-lookup"><span data-stu-id="e9efd-140">The system generates a list with all possible combinations of the sizes and colors you defined for the product.</span></span> <span data-ttu-id="e9efd-141">Vælg **Vælg alle** på værktøjslinjen.</span><span class="sxs-lookup"><span data-stu-id="e9efd-141">Select **Select all** on the toolbar.</span></span>
    - <span data-ttu-id="e9efd-142">I dette eksempel skal du vælge alle mulige varianter.</span><span class="sxs-lookup"><span data-stu-id="e9efd-142">In this example, select all of the possible variants.</span></span> <span data-ttu-id="e9efd-143">Hvis du kun vil bruge et undersæt af de mulige kombinationer af produktdimensioner, skal du kun markere de nødvendige afkrydsningsfelter efter behov.</span><span class="sxs-lookup"><span data-stu-id="e9efd-143">If you only want to use a subset of the possible product dimension combinations, select only the required check boxes as needed.</span></span>  
1. <span data-ttu-id="e9efd-144">Vælg **Opret**.</span><span class="sxs-lookup"><span data-stu-id="e9efd-144">Select **Create**.</span></span>
1. <span data-ttu-id="e9efd-145">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="e9efd-145">Select **Save**.</span></span>

## <a name="improved-variant-suggestions"></a><span data-ttu-id="e9efd-146">Forbedrede variantforslag</span><span class="sxs-lookup"><span data-stu-id="e9efd-146">Improved variant suggestions</span></span>

[!INCLUDE [preview-banner-section](../../../includes/preview-banner-section.md)]

<span data-ttu-id="e9efd-147">Funktionen *Forbedringer af sider med variantforslag* forbedrer siden **Variantforslag** med henblik på at løse problemer med ydeevne og anvendelighed for virksomheder, der har et stort antal kombinationer af produktdimensioner.</span><span class="sxs-lookup"><span data-stu-id="e9efd-147">The *Variant suggestions page improvements* feature improves the **Variant suggestions** page to address performance and usability issues for companies that have a high number of product dimension combinations.</span></span> <span data-ttu-id="e9efd-148">Den forbedrede proces for valg af produktdimensionsværdier, hvor der kan genereres variantforslag, gør det hurtigere og nemmere at identificere og frigive de relevante sæt produktvarianter.</span><span class="sxs-lookup"><span data-stu-id="e9efd-148">The enhanced process for selecting the product dimension values for which to generate variant suggestions makes it faster and easier to identify and release the relevant set of product variants.</span></span>

<span data-ttu-id="e9efd-149">Følgende forbedringer tilføjes af denne funktion:</span><span class="sxs-lookup"><span data-stu-id="e9efd-149">The following improvements are added by this feature:</span></span>

- <span data-ttu-id="e9efd-150">**Udskudt generering af variantforslag:** Siden **Variantforslag** viser ikke længere forslag, når du åbner det første gang.</span><span class="sxs-lookup"><span data-stu-id="e9efd-150">**Deferred generation of variant suggestions:** The **Variant suggestions** page no longer shows suggestions when you first open it.</span></span> <span data-ttu-id="e9efd-151">I stedet skal du udtrykkeligt vælge, hvilke værdier du skal bruge, og derefter vælge knappen **Foreslå** for at generere kombinationerne.</span><span class="sxs-lookup"><span data-stu-id="e9efd-151">Instead, you must explicitly choose which values you will need and then select the **Suggest** button to generate the combinations.</span></span> <span data-ttu-id="e9efd-152">Dette gør processen mere synlig og interaktiv.</span><span class="sxs-lookup"><span data-stu-id="e9efd-152">This makes the process more visible and interactive.</span></span>
- <span data-ttu-id="e9efd-153">**Valg af dimensionsværdier:** Når du har mange dimensionsværdier, er du typisk interesseret i at generere variantforslag, der kun indeholder nogle få af dem (f.eks. når du introducerer et nyt sæt farver eller typografier).</span><span class="sxs-lookup"><span data-stu-id="e9efd-153">**Selection of dimensions values:** When you have many dimension values, you are typically interested in generating variant suggestions that include just a few of them (such as when introducing a new set of colors or styles).</span></span> <span data-ttu-id="e9efd-154">Med det forbedrede design kan du vælge de dimensionsværdier, du vil generere produktvariantforslag for.</span><span class="sxs-lookup"><span data-stu-id="e9efd-154">With the improved design, you can select the dimension values for which you want to generate product variant suggestions.</span></span> <span data-ttu-id="e9efd-155">Dette øger relevansen af de foreslåede varianter markant og forbedrer både systemets ydeevne og brugerens produktivitet.</span><span class="sxs-lookup"><span data-stu-id="e9efd-155">This greatly increases the relevance of the suggested variants and improves both system performance and user productivity.</span></span>

### <a name="turn-on-the-variant-suggestions-page-improvements-feature"></a><span data-ttu-id="e9efd-156">Aktivere funktionen Forbedringer på side med variantforslag</span><span class="sxs-lookup"><span data-stu-id="e9efd-156">Turn on the Variant suggestions page improvements feature</span></span>

<span data-ttu-id="e9efd-157">Før du kan bruge funktionen *Forbedringer af side med variantforslag*, skal den være aktiveret i dit system.</span><span class="sxs-lookup"><span data-stu-id="e9efd-157">Before you can use *Variant suggestions page improvements* feature, it must be turned on in your system.</span></span> <span data-ttu-id="e9efd-158">Administratorer kan bruge indstillingerne i [Funktionsstyring](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til.</span><span class="sxs-lookup"><span data-stu-id="e9efd-158">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="e9efd-159">I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="e9efd-159">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="e9efd-160">**Modul:** *Administration af produktoplysninger*</span><span class="sxs-lookup"><span data-stu-id="e9efd-160">**Module:** *Product information management*</span></span>
- <span data-ttu-id="e9efd-161">**Funktionsnavn:** *Forbedringer af side med variantforslag*</span><span class="sxs-lookup"><span data-stu-id="e9efd-161">**Feature name:** *Variant suggestions page improvements*</span></span>

### <a name="work-with-the-improved-variant-suggestions"></a><span data-ttu-id="e9efd-162">Arbejde med de forbedrede variantforslag</span><span class="sxs-lookup"><span data-stu-id="e9efd-162">Work with the improved variant suggestions</span></span>

<span data-ttu-id="e9efd-163">Sådan genereres forslag til produktvarianter, når funktionen *Forbedringer af side med variantforslag* er aktiveret:</span><span class="sxs-lookup"><span data-stu-id="e9efd-163">To generate product variant suggestions when the *Variant suggestions page improvements* feature is enabled:</span></span>

1. <span data-ttu-id="e9efd-164">Åbn eller opret en produktmaster, og tilføj de nødvendige produktdimensioner som beskrevet i forrige afsnit.</span><span class="sxs-lookup"><span data-stu-id="e9efd-164">Open or create a product master and add the required product dimensions to it, as described in the previous section.</span></span>
1. <span data-ttu-id="e9efd-165">Når produktmasteren er åben, skal du vælge **Produktvarianter** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="e9efd-165">With the product master open, select **Product variants** on the Action Pane.</span></span>
1. <span data-ttu-id="e9efd-166">Vælg **Variantforslag** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="e9efd-166">Select **Variant suggestions** on the Action Pane.</span></span>
1. <span data-ttu-id="e9efd-167">Vælg de værdier, du vil bruge til de enkelte dimensioner.</span><span class="sxs-lookup"><span data-stu-id="e9efd-167">Select the values that you want to use for each of the dimensions.</span></span>
1. <span data-ttu-id="e9efd-168">Vælg **Foreslå** på den øverste værktøjslinje.</span><span class="sxs-lookup"><span data-stu-id="e9efd-168">On the top toolbar, select **Suggest**.</span></span>
1. <span data-ttu-id="e9efd-169">Systemet genererer en liste over alle de mulige kombinationer af de størrelser og farver, du har valgt.</span><span class="sxs-lookup"><span data-stu-id="e9efd-169">The system generates a list with all possible combinations of the sizes and colors you selected.</span></span> <span data-ttu-id="e9efd-170">I oversigtspanelet **Foreslåede varianter** skal du markere afkrydsningsfeltet for hver kombination af produktdimensioner, du vil bruge, eller vælg **Vælg alle** på værktøjslinjen for at vælge dem alle.</span><span class="sxs-lookup"><span data-stu-id="e9efd-170">On the **Suggested variants** FastTab, select the check box for each product dimension combination that you want to use, or select **Select all** on the toolbar to select all of them.</span></span>  
1. <span data-ttu-id="e9efd-171">Vælg **Opret** for at føje varianter til den aktuelle produktmaster.</span><span class="sxs-lookup"><span data-stu-id="e9efd-171">Select **Create** to add the variants to the current product master.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
