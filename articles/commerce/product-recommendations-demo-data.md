---
title: Oprette anbefalinger med demonstrationsdata
description: Dette emne er en vejledning til, hvordan du kan udnytte produktanbefalinger til omni-kanal i niveau-1 enkelt boks-miljøer med forudindstillede demodata, der kan tilpasses.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: cca6913375eec2565852676f3c1da5a67f71e14f
ms.sourcegitcommit: 8905d7a7a010e451c5435086480f66650ec54926
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2020
ms.locfileid: "3664900"
---
# <a name="create-recommendations-with-demo-data"></a><span data-ttu-id="57f22-103">Oprette anbefalinger med demonstrationsdata</span><span class="sxs-lookup"><span data-stu-id="57f22-103">Create recommendations with demo data</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="57f22-104">Dette emne er en vejledning til, hvordan du kan udnytte produktanbefalinger til omni-kanal i niveau-1 enkelt boks-miljøer med forudindstillede demodata, der kan tilpasses.</span><span class="sxs-lookup"><span data-stu-id="57f22-104">This topic provides guidance on how to leverage omni-channel product recommendations in Tier-1 single box environments using pre-populated, customizable demo data.</span></span>

<span data-ttu-id="57f22-105">Omni-kanalproduktanbefalinger giver et sæt redaktionelt leverede eller programmeringsmæssigt fremstillede lister over produkter.</span><span class="sxs-lookup"><span data-stu-id="57f22-105">Omni-channel product recommendations provide a set of editorially curated or programmatically generated list of products.</span></span> <span data-ttu-id="57f22-106">Disse lister kan bruges i flere forskellige scenarier, afhængigt af virksomhedens behov.</span><span class="sxs-lookup"><span data-stu-id="57f22-106">These lists can be used in several scenarios, depending on the business need.</span></span> <span data-ttu-id="57f22-107">Yderligere oplysninger om lister over produktanbefalinger finder du under [Oversigt over produktanbefalinger](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="57f22-107">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

<span data-ttu-id="57f22-108">For niveau 2 og højere Dynamics 365-miljøer beregnes produktanbefalinger automatisk ud fra kundedata.</span><span class="sxs-lookup"><span data-stu-id="57f22-108">For Tier-2 and higher Dynamics 365 environments, product recommendations are automatically computed based on customer data.</span></span> <span data-ttu-id="57f22-109">Hvis du bruger demodata til produktanbefalinger, deaktiveres ingen af de anbefalinger for produktløsninger, der allerede er klargjort i miljøet, og eventuelle omkostninger, der er forbundet med brugen af dem.</span><span class="sxs-lookup"><span data-stu-id="57f22-109">Using product recommendations demo data does not disable any product recommendations solution already provisioned in the environment and any costs associated with its usage.</span></span>

<span data-ttu-id="57f22-110">Produktanbefalinger for niveau 1-miljøer er udelukkende baseret på de statiske demodata, der er gemt i en .csv-fil.</span><span class="sxs-lookup"><span data-stu-id="57f22-110">For Tier-1 environments, product recommendations are based only off the static demo data stored in a .csv file.</span></span>

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a><span data-ttu-id="57f22-111">Aktivere demodata til produktanbefalinger i et miljø</span><span class="sxs-lookup"><span data-stu-id="57f22-111">Enabling product recommendations demo data in an environment</span></span>
<span data-ttu-id="57f22-112">Du skal udrulle Dynamics 365 Commerce-prøveversionens demoudvidelse i det respektive miljø for at aktivere demodata til produktanbefalinger.</span><span class="sxs-lookup"><span data-stu-id="57f22-112">To enable product recommendations demo date, you need to deploy the Dynamics 365 Commerce Preview Demo Extension to the respective environment.</span></span> <span data-ttu-id="57f22-113">Hvis du gør det automatisk, aktiveres demodata til produktanbefalinger.</span><span class="sxs-lookup"><span data-stu-id="57f22-113">Doing so automatically enables product recommendations demo data.</span></span>

## <a name="default-demo-data"></a><span data-ttu-id="57f22-114">Standarddemodata</span><span class="sxs-lookup"><span data-stu-id="57f22-114">Default demo data</span></span>
<span data-ttu-id="57f22-115">Hvert OneBox-typemiljø indeholder et forudindlæst sæt demodata til produktanbefalinger, der er gemt i den kommaseparerede 'reco_demo_data.csv'-fil, som er placeret på Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="57f22-115">Each OneBox type environment comes with a preloaded set of product recommendations demo data stored in the coma separated 'reco_demo_data.csv' file, located on the Commerce Scale Unit.</span></span>

<span data-ttu-id="57f22-116">Disse data er struktureret langs følgende kolonner.</span><span class="sxs-lookup"><span data-stu-id="57f22-116">The data is structured along the following columns.</span></span>

| <span data-ttu-id="57f22-117">Kolonnenavn</span><span class="sxs-lookup"><span data-stu-id="57f22-117">Column name</span></span>         | <span data-ttu-id="57f22-118">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="57f22-118">Mandatory</span></span>          | <span data-ttu-id="57f22-119">Beskrivende tekst</span><span class="sxs-lookup"><span data-stu-id="57f22-119">Description</span></span>                                                                                                                                 | <span data-ttu-id="57f22-120">Mulige værdier</span><span class="sxs-lookup"><span data-stu-id="57f22-120">Possible values</span></span>                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="57f22-121">RecoList</span><span class="sxs-lookup"><span data-stu-id="57f22-121">RecoList</span></span>            | :heavy_check_mark: | <span data-ttu-id="57f22-123">Den specifikke listetype for produktanbefalinger, som demodatapunktet skal generere.</span><span class="sxs-lookup"><span data-stu-id="57f22-123">The specific product recommendation list type that the demo data point is to generate.</span></span>                                                    | <ul><li><span data-ttu-id="57f22-124">RecoBestSelling</span><span class="sxs-lookup"><span data-stu-id="57f22-124">RecoBestSelling</span></span></li><li><span data-ttu-id="57f22-125">RecoNew</span><span class="sxs-lookup"><span data-stu-id="57f22-125">RecoNew</span></span></li><li><span data-ttu-id="57f22-126">RecoTrending</span><span class="sxs-lookup"><span data-stu-id="57f22-126">RecoTrending</span></span></li><li><span data-ttu-id="57f22-127">RecoCart</span><span class="sxs-lookup"><span data-stu-id="57f22-127">RecoCart</span></span></li><li><span data-ttu-id="57f22-128">RecoPeopleAlsoBuy</span><span class="sxs-lookup"><span data-stu-id="57f22-128">RecoPeopleAlsoBuy</span></span></li></ul> |
| <span data-ttu-id="57f22-129">OperatingUnitNumber</span><span class="sxs-lookup"><span data-stu-id="57f22-129">OperatingUnitNumber</span></span> | :heavy_check_mark: | <span data-ttu-id="57f22-131">Det specifikke driftsenhedsnummer, hvor produktanbefalinger forventes at blive synlige.</span><span class="sxs-lookup"><span data-stu-id="57f22-131">The specific operating unit number where product recommendations are expected to be   surfaced.</span></span>                                        |                                                                              |
| <span data-ttu-id="57f22-132">Kategori</span><span class="sxs-lookup"><span data-stu-id="57f22-132">Category</span></span>            |                    |    <span data-ttu-id="57f22-133">Den kategori, som den specifikke liste skal returneres for.</span><span class="sxs-lookup"><span data-stu-id="57f22-133">The category the specific list should be returned for.</span></span> <span data-ttu-id="57f22-134">Hvis der ikke er angivet en kategori, gælder listen kun for det øverste navigationshierarki.</span><span class="sxs-lookup"><span data-stu-id="57f22-134">If no category is specified, the list is for top of navigation hierarchy only.</span></span>    |                                                                              |
| <span data-ttu-id="57f22-135">SeedItemId</span><span class="sxs-lookup"><span data-stu-id="57f22-135">SeedItemId</span></span>          |                    |    <span data-ttu-id="57f22-136">Til lister, der kræver oprindelsesdata (RecoPeopleAlsoBuy og RecoCart), skal produktet indeholde supplerende produkter til disse lister.</span><span class="sxs-lookup"><span data-stu-id="57f22-136">For lists that require seed (RecoPeopleAlsoBuy and RecoCart), the product those lists should show additional products for.</span></span>            |                                                                              |
| <span data-ttu-id="57f22-137">CustomerId</span><span class="sxs-lookup"><span data-stu-id="57f22-137">CustomerId</span></span>          |                    |    <span data-ttu-id="57f22-138">For lister, der kræver et kunde-id (RecoPicks).</span><span class="sxs-lookup"><span data-stu-id="57f22-138">For lists that require a customer identifier (RecoPicks).</span></span>  <span data-ttu-id="57f22-139">Standardværdien "0" gælder for alle kunder.</span><span class="sxs-lookup"><span data-stu-id="57f22-139">The default value '0' applies to all customers.</span></span>          |                                                                              |
| <span data-ttu-id="57f22-140">ItemIds</span><span class="sxs-lookup"><span data-stu-id="57f22-140">ItemIds</span></span>             | :heavy_check_mark: | <span data-ttu-id="57f22-142">Et eller flere produkter, der skal returneres som resultat, skal adskilles med ';'.</span><span class="sxs-lookup"><span data-stu-id="57f22-142">One or more products to be returned as the result, separated by ';'.</span></span>                                                                  |                                                                              |

## <a name="customize-demo-data"></a><span data-ttu-id="57f22-143">Tilpasse demodata</span><span class="sxs-lookup"><span data-stu-id="57f22-143">Customize demo data</span></span>
<span data-ttu-id="57f22-144">Du kan redigere standarddemodataene med eventuelle produkt- og kategorioplysninger, der er konfigureret i hovedkontoret.</span><span class="sxs-lookup"><span data-stu-id="57f22-144">You can edit the default demo data with any product and category information configured in HQ.</span></span> <span data-ttu-id="57f22-145">Efter du opdaterer .csv-filen, afspejler de produktanbefalinger, der returneres til kunderne, straks ændringerne.</span><span class="sxs-lookup"><span data-stu-id="57f22-145">After you update the .csv, the product recommendations that are returned to customers will immediately reflect the changes.</span></span>

<span data-ttu-id="57f22-146">Udvidelsen indeholder en datafil med navnet 'RecoMockDataset.csv', som giver dig mulighed for at styre det datasæt, der bruges til at styrke de anbefalede resultater.</span><span class="sxs-lookup"><span data-stu-id="57f22-146">The extension contains a datafile called 'RecoMockDataset.csv', which allows you to control the dataset used to power the mock recommendations results.</span></span> <span data-ttu-id="57f22-147">Filnavnet kan styres via udvidelseskonfiguration ved hjælp af indstillingen **ext.Recommendations.DemoFilePath**.</span><span class="sxs-lookup"><span data-stu-id="57f22-147">The file name can be controlled through extension configuration using the **ext.Recommendations.DemoFilePath** setting.</span></span> <span data-ttu-id="57f22-148">Det giver dig mulighed for at have flere tilgængelige datasæt, der kan skiftes mellem nemt og hurtigt under konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="57f22-148">This enables you to have multiple datasets available that can be switched between easily through configuration.</span></span>


```xml
<settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
</settings>
```

## <a name="additional-resources"></a><span data-ttu-id="57f22-149">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="57f22-149">Additional resources</span></span>

[<span data-ttu-id="57f22-150">Oversigt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="57f22-150">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="57f22-151">Aktivér Azure Data Lake Storage i et Dynamics 365 Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="57f22-151">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="57f22-152">Aktivér produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="57f22-152">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="57f22-153">Aktivere tilpassede anbefalinger</span><span class="sxs-lookup"><span data-stu-id="57f22-153">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="57f22-154">Fravælge tilpassede anbefalinger</span><span class="sxs-lookup"><span data-stu-id="57f22-154">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="57f22-155">Aktivere anbefalinger af "Køb tilsvarende"</span><span class="sxs-lookup"><span data-stu-id="57f22-155">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="57f22-156">Tilføje produktanbefalinger på POS</span><span class="sxs-lookup"><span data-stu-id="57f22-156">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="57f22-157">Føje anbefalinger til transaktionsskærmen</span><span class="sxs-lookup"><span data-stu-id="57f22-157">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="57f22-158">Justere resultater for AI-ML-anbefalinger</span><span class="sxs-lookup"><span data-stu-id="57f22-158">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="57f22-159">Oprette overvågede anbefalinger manuelt</span><span class="sxs-lookup"><span data-stu-id="57f22-159">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="57f22-160">Ofte stillede spørgsmål om produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="57f22-160">Product recommendations FAQ</span></span>](faq-recommendations.md)
