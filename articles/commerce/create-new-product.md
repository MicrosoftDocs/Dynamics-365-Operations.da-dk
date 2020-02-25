---
title: Oprette et nyt produkt
description: Dette emne beskriver, hvordan du opretter et nyt produkt i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 356bf91b2a946e7c0f5d5af9e2fe0b64342b856e
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001958"
---
# <a name="create-a-new-product"></a><span data-ttu-id="b6410-103">Oprette et nyt produkt</span><span class="sxs-lookup"><span data-stu-id="b6410-103">Create a new product</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="b6410-104">Dette emne beskriver, hvordan du opretter et nyt produkt i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b6410-104">This topic describes how to create a new product in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b6410-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="b6410-105">Overview</span></span>

<span data-ttu-id="b6410-106">Et produkt defineres primært af produktnummer, navn og beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="b6410-106">A product is primarily defined by a product number, name, and description.</span></span> <span data-ttu-id="b6410-107">Andre data er dog også nødvendige for at beskrive en vare eller tjenesteydelse:</span><span class="sxs-lookup"><span data-stu-id="b6410-107">However, other data is also required in order to describe a product or service:</span></span>

## <a name="create-a-new-product"></a><span data-ttu-id="b6410-108">Oprette et nyt produkt</span><span class="sxs-lookup"><span data-stu-id="b6410-108">Create a new product</span></span>

1. <span data-ttu-id="b6410-109">Gå til **Moduler \> Retail og Commerce \> Produkter og kategorier \> Produkter efter kategori** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="b6410-109">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Products by category**.</span></span>
1. <span data-ttu-id="b6410-110">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="b6410-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="b6410-111">På rullelisten **Produkttype** skal du vælge enten **Vare** eller **Tjeneste**.</span><span class="sxs-lookup"><span data-stu-id="b6410-111">In the **Product type** drop-down list, select either **Item** or **Service**.</span></span>
1. <span data-ttu-id="b6410-112">På rullelisten **Produktundertype** skal du vælge enten **Produkt** (hvis produktet ikke skal have varianter) eller **Produktmaster** (hvis produktet skal have varianter).</span><span class="sxs-lookup"><span data-stu-id="b6410-112">In the **Product subtype** drop-down list, select either **Product** (if the product will have no variants) or **Product master** (if the product will have variants).</span></span>
1. <span data-ttu-id="b6410-113">Angiv et produktnummer i feltet **Produktnummer**, hvis det ikke allerede er udfyldt på forhånd.</span><span class="sxs-lookup"><span data-stu-id="b6410-113">In the **Product number** box, enter a product number if one is not already prepopulated.</span></span>
1. <span data-ttu-id="b6410-114">Indtast et produktnavn i feltet **Produktnavn**.</span><span class="sxs-lookup"><span data-stu-id="b6410-114">In the **Product name** box, enter a product name.</span></span>
1. <span data-ttu-id="b6410-115">Angiv et søgenavn i feltet **Søgenavn**.</span><span class="sxs-lookup"><span data-stu-id="b6410-115">In the **Search name** box, enter a search name.</span></span>
1. <span data-ttu-id="b6410-116">Vælg en relevant kategori på rullelisten **Detailkategori**.</span><span class="sxs-lookup"><span data-stu-id="b6410-116">In the **Retail category** drop-down list, select an appropriate category.</span></span>
1. <span data-ttu-id="b6410-117">Hvis produktet er en pakke, skal du vælge **Ja** for **Produktpakke**.</span><span class="sxs-lookup"><span data-stu-id="b6410-117">If the product is a kit, select **Yes** for **Product kit**.</span></span>
1. <span data-ttu-id="b6410-118">Hvis produktundertypen er produktmaster, skal du angive **Produktdimensionsgruppe** for at medtage de understøttede varianter.</span><span class="sxs-lookup"><span data-stu-id="b6410-118">If the product subtype is product master, set the **Product dimension group** to include the supported variants.</span></span> <span data-ttu-id="b6410-119">Indstillingerne omfatter **Farve**, **Størrelse**, **Typografi** og **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="b6410-119">Options include **Color**, **Size**, **Style**, and **Configuration**.</span></span> <span data-ttu-id="b6410-120">Det kan være nødvendigt at oprette flere produktdimensionsgrupper efter behov.</span><span class="sxs-lookup"><span data-stu-id="b6410-120">You may need to create additional product dimension groups if needed.</span></span>
1. <span data-ttu-id="b6410-121">Vælg en relevant indstilling på rullelisten **Konfigurationsteknologi**.</span><span class="sxs-lookup"><span data-stu-id="b6410-121">In the **Configuration technology** drop-down list, select an appropriate option.</span></span>
1. <span data-ttu-id="b6410-122">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="b6410-122">Select **OK**.</span></span>

<span data-ttu-id="b6410-123">Følgende billede viser et eksempel på tilføjelse af produkt.</span><span class="sxs-lookup"><span data-stu-id="b6410-123">The following image shows an example product being added.</span></span>

![Oprette et produkt](media/create-new-product.png)

<span data-ttu-id="b6410-125">Når et produkt er tilføjet, kan der angives yderligere data for det, f.eks. **Produktbeskrivelse**, **Variantgrupper**, **Dimensionsgrupper**, **Produktattributter** og **Relaterede produkter**.</span><span class="sxs-lookup"><span data-stu-id="b6410-125">Once a product is added, additional data can be set for it, such as **Product description**, **Variant groups**, **Dimension groups**, **Product attributes**, and **Related products**.</span></span>

<span data-ttu-id="b6410-126">Følgende billede viser flere oplysninger om et produkt.</span><span class="sxs-lookup"><span data-stu-id="b6410-126">The following image shows a product's additional details.</span></span>

![Produktdetaljer](media/create-new-product-2.png)

### <a name="create-product-variants"></a><span data-ttu-id="b6410-128">Opret produktvarianter</span><span class="sxs-lookup"><span data-stu-id="b6410-128">Create product variants</span></span>

<span data-ttu-id="b6410-129">Hvis produktundertypen er **Produktmaster**, skal der oprettes specifikke varianter.</span><span class="sxs-lookup"><span data-stu-id="b6410-129">If the product subtype is **Product master**, specific variants will need to be created.</span></span> 

<span data-ttu-id="b6410-130">Følg disse trin for at oprette produktvarianter.</span><span class="sxs-lookup"><span data-stu-id="b6410-130">To create product variants, follow these steps.</span></span>

1. <span data-ttu-id="b6410-131">Vælg **Produktvarianter** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="b6410-131">On the action pane, select **Product variants**.</span></span>
1. <span data-ttu-id="b6410-132">Hvis der er valgt variantgrupper i handlingsruden, skal du vælge \**Forslag til varianter*.</span><span class="sxs-lookup"><span data-stu-id="b6410-132">If variant groups have been selected on the action pane, select \**Variant suggestions*.</span></span>
1. <span data-ttu-id="b6410-133">Vælg de varianter, du vil understøtte for produktet.</span><span class="sxs-lookup"><span data-stu-id="b6410-133">Select the variants you would like to support for the product.</span></span>
1. <span data-ttu-id="b6410-134">Vælg **Opret**.</span><span class="sxs-lookup"><span data-stu-id="b6410-134">Select **Create**.</span></span>

## <a name="release-a-product"></a><span data-ttu-id="b6410-135">Frigive et produkt</span><span class="sxs-lookup"><span data-stu-id="b6410-135">Release a product</span></span>

<span data-ttu-id="b6410-136">Hvis du vil sælge et produkt, skal det først frigives til en juridisk enhed.</span><span class="sxs-lookup"><span data-stu-id="b6410-136">To sell a product it must first be released to a legal entity.</span></span>

1. <span data-ttu-id="b6410-137">Vælg **Frigiv produkter** på produktsiden.</span><span class="sxs-lookup"><span data-stu-id="b6410-137">From the product page, select **Release products**.</span></span>

    ![Frigive produkt](media/create-new-product-3.png)

1. <span data-ttu-id="b6410-139">Vælg det produkt, der skal frigives, og vælg derefter **Næste**.</span><span class="sxs-lookup"><span data-stu-id="b6410-139">Select the product to release, and then select **Next**.</span></span>

    ![Vælge produkt til frigivelse](media/create-new-product-4.png)

1. <span data-ttu-id="b6410-141">Vælg den række produktvarianter, der skal frigives, og vælg derefter **Næste**.</span><span class="sxs-lookup"><span data-stu-id="b6410-141">Select the set of product variants to release, and then select **Next**.</span></span>

    ![Vælge varianter til frigivelse](media/create-new-product-5.png)

1. <span data-ttu-id="b6410-143">Vælg den juridiske enhed, og vælg derefter **Næste**.</span><span class="sxs-lookup"><span data-stu-id="b6410-143">Select the legal entity, and then select **Next**.</span></span>

    ![Vælg juridisk enhed](media/create-new-product-6.png)

1. <span data-ttu-id="b6410-145">Vælg **Udfør**.</span><span class="sxs-lookup"><span data-stu-id="b6410-145">Select **Finish**.</span></span>

    ![Udføre produktfrigivelse](media/create-new-product-7.png)

## <a name="configure-a-released-product"></a><span data-ttu-id="b6410-147">Konfigurere et frigivet produkt</span><span class="sxs-lookup"><span data-stu-id="b6410-147">Configure a released product</span></span>

<span data-ttu-id="b6410-148">Når et produkt er frigivet, kræver det en yderligere konfiguration, der omfatter tilføjelse af en pris til produktet.</span><span class="sxs-lookup"><span data-stu-id="b6410-148">Once a product is released, it will then require further configuration that includes adding a price to the product.</span></span>

1. <span data-ttu-id="b6410-149">Gå til **Moduler \> Retail og Commerce \> Produkter og kategorier \> Frigivne produkter efter kategori** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="b6410-149">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Released products by category**.</span></span>
1. <span data-ttu-id="b6410-150">Vælg produktkategorinoden for det produkt, der blev frigivet, og vælg derefter produktet på produktlisten.</span><span class="sxs-lookup"><span data-stu-id="b6410-150">Select the product category node for the product that was released, and then select the product from the product list.</span></span>
1. <span data-ttu-id="b6410-151">Vælg **Rediger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="b6410-151">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="b6410-152">I sektionen **Køb** skal du konfigurere de påkrævede egenskaber, herunder **Enhed**, **Pris** og **Antal**.</span><span class="sxs-lookup"><span data-stu-id="b6410-152">In the **Purchase** section, configure any required properties including **Unit**, **Price**,  and **Quantity**.</span></span>
1. <span data-ttu-id="b6410-153">Vælg **Valider** i handlingsruden for at sikre, at der ikke rapporteres fejl for manglende felter.</span><span class="sxs-lookup"><span data-stu-id="b6410-153">On the action pane, select **Validate** to ensure that no errors are reported for missing fields.</span></span>
1. <span data-ttu-id="b6410-154">Gå til handlingsruden, og vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="b6410-154">On the action pane, select **Save**.</span></span>

<span data-ttu-id="b6410-155">Følgende billede viser et eksempel på konfiguration af et frigivet produkt.</span><span class="sxs-lookup"><span data-stu-id="b6410-155">The following image shows an example configuration for a released product.</span></span>

![Konfigurere frigivet produkt](media/create-new-product-8.png)

## <a name="additional-resources"></a><span data-ttu-id="b6410-157">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="b6410-157">Additional resources</span></span>

[<span data-ttu-id="b6410-158">Oprette juridiske enheder</span><span class="sxs-lookup"><span data-stu-id="b6410-158">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="b6410-159">Oprette en variantgruppe</span><span class="sxs-lookup"><span data-stu-id="b6410-159">Create a variant group</span></span>](create-variant-group.md) 
