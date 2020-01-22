---
title: Demodata til produktanbefalinger for omni-kanal
description: Dette dokument er en vejledning til, hvordan du kan udnytte produktanbefalinger til omni-kanal i trin-1 enkelt boks-miljøer med forudindstillede demodata, der kan tilpasses.
author: bebeale
manager: AnnBe
ms.date: 12/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 31aa5dbd2fa814fd572024a4ae36b9d9b46a2fb0
ms.sourcegitcommit: 398c0652acde12c953de007d06055456d6e0a516
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/02/2019
ms.locfileid: "2872320"
---
# <a name="omni-channel-product-recommendations-demo-data"></a><span data-ttu-id="91d63-103">Demodata til produktanbefalinger for omni-kanal</span><span class="sxs-lookup"><span data-stu-id="91d63-103">Omni-channel product recommendations demo data</span></span>

<span data-ttu-id="91d63-104">Dette dokument er en vejledning til, hvordan du kan udnytte produktanbefalinger til omni-kanal i trin-1 enkelt boks-miljøer med forudindstillede demodata, der kan tilpasses.</span><span class="sxs-lookup"><span data-stu-id="91d63-104">This document aims to provide guidance on how to leverage omni-channel product recommendations in Tier-1 single box environments using pre-populated, customizable demo data.</span></span>

<span data-ttu-id="91d63-105">Omni-kanalproduktanbefalinger giver et sæt redaktionelt leverede eller programmeringsmæssigt fremstillede lister over produkter.</span><span class="sxs-lookup"><span data-stu-id="91d63-105">Omni-channel product recommendations provide a set of editorially curated or programmatically generated ordered list of products.</span></span> <span data-ttu-id="91d63-106">Disse lister kan bruges i flere forskellige scenarier, afhængigt af virksomhedens behov.</span><span class="sxs-lookup"><span data-stu-id="91d63-106">These lists can be used in several scenarios, depending on the business need.</span></span> <span data-ttu-id="91d63-107">Yderligere oplysninger om lister over produktanbefalinger finder du under [Oversigt over produktanbefalinger.](../commerce/product-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="91d63-107">For more information about product recommendation lists, see [Product recommendations overview.](../commerce/product-recommendations.md)</span></span>

<span data-ttu-id="91d63-108">For niveau 2 og højere Dynamics-miljøer beregnes produktanbefalinger automatisk ud fra kundedata.</span><span class="sxs-lookup"><span data-stu-id="91d63-108">For Tier-2 and higher Dynamics Environments product recommendations are automatically computed based on customer data.</span></span>
<span data-ttu-id="91d63-109">Hvis du bruger demodata til produktanbefalinger, deaktiveres ingen af de anbefalinger for produktløsninger, der allerede er klargjort i miljøet, og eventuelle omkostninger, der er forbundet med brugen af dem.</span><span class="sxs-lookup"><span data-stu-id="91d63-109">Using product recommendations demo data does not disable any product recommendations solution already provisioned in the environment and any costs associated with its usage.</span></span>

<span data-ttu-id="91d63-110">Produkt anbefalinger for niveau 1-miljøer er udelukkende baseret på de statiske demodata, der er gemt i en CSV-fil.</span><span class="sxs-lookup"><span data-stu-id="91d63-110">For Tier-1 environments product recommendations are based only off the static demo data stored in a csv file.</span></span>

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a><span data-ttu-id="91d63-111">Aktivere demodata til produktanbefalinger i et miljø</span><span class="sxs-lookup"><span data-stu-id="91d63-111">Enabling product recommendations demo data in an environment</span></span>

<span data-ttu-id="91d63-112">Kunderne skal installere **Dynamics 365 Commerce Preview Demo Extension** i det respektive miljø, der automatisk aktiverer demodata til produktanbefalinger.</span><span class="sxs-lookup"><span data-stu-id="91d63-112">Customers need to deploy the **Dynamics 365 Commerce Preview Demo Extension** to the respective environment, which automatically enables product recommendations demo data.</span></span>

## <a name="default-demo-data"></a><span data-ttu-id="91d63-113">Standarddemodata</span><span class="sxs-lookup"><span data-stu-id="91d63-113">Default demo data</span></span>
<span data-ttu-id="91d63-114">Hvert Onebox-typemiljø indeholder et forudindlæst sæt demodata til produktanbefalinger, der er gemt i den kommaseparerede fil **'reco_demo_data.** , som er placeret i samme mappe som dette dokument på Retail Server.</span><span class="sxs-lookup"><span data-stu-id="91d63-114">Each Onebox type environment comes with a preloaded set of product recommendations demo data stored in the coma separated **‘reco_demo_data.csv’** file, located in the same folder as this document on Retail Server.</span></span>

<span data-ttu-id="91d63-115">Disse data er struktureret langs følgende kolonner</span><span class="sxs-lookup"><span data-stu-id="91d63-115">This data is structured along the following columns</span></span>

| <span data-ttu-id="91d63-116">Kolonnenavn</span><span class="sxs-lookup"><span data-stu-id="91d63-116">Column name</span></span>         | <span data-ttu-id="91d63-117">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="91d63-117">Mandatory</span></span>          | <span data-ttu-id="91d63-118">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="91d63-118">Description</span></span>                                                                                                                                 | <span data-ttu-id="91d63-119">Mulige værdier</span><span class="sxs-lookup"><span data-stu-id="91d63-119">Possible Values</span></span>                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="91d63-120">RecoList</span><span class="sxs-lookup"><span data-stu-id="91d63-120">RecoList</span></span>            | :heavy_check_mark: | <span data-ttu-id="91d63-122">Den specifikke listetype for produktanbefalinger, som demodatapunktet skal generere.</span><span class="sxs-lookup"><span data-stu-id="91d63-122">The specific product   recommendation list type that the demo data point is to generate.</span></span>                                                    | <ul><li><span data-ttu-id="91d63-123">RecoBestSelling</span><span class="sxs-lookup"><span data-stu-id="91d63-123">RecoBestSelling</span></span></li><li><span data-ttu-id="91d63-124">RecoNew</span><span class="sxs-lookup"><span data-stu-id="91d63-124">RecoNew</span></span></li><li><span data-ttu-id="91d63-125">RecoTrending</span><span class="sxs-lookup"><span data-stu-id="91d63-125">RecoTrending</span></span></li><li><span data-ttu-id="91d63-126">RecoCart</span><span class="sxs-lookup"><span data-stu-id="91d63-126">RecoCart</span></span></li><li><span data-ttu-id="91d63-127">RecoPeopleAlsoBuy</span><span class="sxs-lookup"><span data-stu-id="91d63-127">RecoPeopleAlsoBuy</span></span></li></ul> |
| <span data-ttu-id="91d63-128">OperatingUnitNumber</span><span class="sxs-lookup"><span data-stu-id="91d63-128">OperatingUnitNumber</span></span> | :heavy_check_mark: | <span data-ttu-id="91d63-130">Det specifikke driftsenhedsnummer, hvor produktanbefalinger forventes at bliver vist.</span><span class="sxs-lookup"><span data-stu-id="91d63-130">The specific   operating unit number where product recommendations are expected to be   surfaced in.</span></span>                                        |                                                                              |
| <span data-ttu-id="91d63-131">Kategori</span><span class="sxs-lookup"><span data-stu-id="91d63-131">Category</span></span>            |                    |    <span data-ttu-id="91d63-132">Den kategori, som den specifikke liste skal returneres for.</span><span class="sxs-lookup"><span data-stu-id="91d63-132">The category the   specific list should be returned for.</span></span> <span data-ttu-id="91d63-133">Hvis der ikke er angivet en kategori, gælder listen kun for det øverste navigationshierarki.</span><span class="sxs-lookup"><span data-stu-id="91d63-133">If no category is specified, list is   for top of navigation hierarchy only.</span></span>    |                                                                              |
| <span data-ttu-id="91d63-134">SeedItemId</span><span class="sxs-lookup"><span data-stu-id="91d63-134">SeedItemId</span></span>          |                    |    <span data-ttu-id="91d63-135">Til lister, der kræver oprindelsesdata (RecoPeopleAlsoBuy og RecoCart), skal produktet indeholde supplerende produkter til disse lister.</span><span class="sxs-lookup"><span data-stu-id="91d63-135">For lists that   require seed (RecoPeopleAlsoBuy and RecoCart) the product those lists should   show additional products for.</span></span>            |                                                                              |
| <span data-ttu-id="91d63-136">ItemIds</span><span class="sxs-lookup"><span data-stu-id="91d63-136">ItemIds</span></span>             | :heavy_check_mark: | <span data-ttu-id="91d63-138">Et eller flere produkter, der skal returneres som resultat, adskilt af **';'**.</span><span class="sxs-lookup"><span data-stu-id="91d63-138">One or more products   to be returned as the result, separated by **‘;’**.</span></span>                                                                  |                                                                              |


## <a name="customize-demo-data"></a><span data-ttu-id="91d63-139">Tilpasse demodata</span><span class="sxs-lookup"><span data-stu-id="91d63-139">Customize demo data</span></span>
<span data-ttu-id="91d63-140">Kunder kan redigere standarddemodataene med eventuelle produkt- og kategorioplysninger, der er konfigureret i hovedkontoret.</span><span class="sxs-lookup"><span data-stu-id="91d63-140">Customers can edit the default demo data with any product and category information that is configured in HQ.</span></span> <span data-ttu-id="91d63-141">Når CSV-filen er opdateret, afspejler de produktanbefalinger, der returneres til kunderne, straks ændringerne.</span><span class="sxs-lookup"><span data-stu-id="91d63-141">Once the CSV is updated, the Product Recommendations returned to customers will immediately reflect the changes.</span></span>

<span data-ttu-id="91d63-142">Udvidelsen indeholder en datafil med navnet RecoMockDataset.csv, som giver kunden mulighed for at styre det datasæt, der bruges til at styrke de anbefalede resultater.</span><span class="sxs-lookup"><span data-stu-id="91d63-142">The extension contains a datafile called RecoMockDataset.csv which allows the customer to control the dataset used to power the mock recommendations results.</span></span> <span data-ttu-id="91d63-143">Filnavnet kan styres via udvidelseskonfiguration ved hjælp af indstillingen **ext.Recommendations.DemoFilePath**.</span><span class="sxs-lookup"><span data-stu-id="91d63-143">The file name can be controlled through extension configuration using the **ext.Recommendations.DemoFilePath** setting.</span></span> <span data-ttu-id="91d63-144">Det giver kunderne mulighed for at have flere tilgængelige datasæt, der kan skiftes mellem nemt og hurtigt under konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="91d63-144">This enables the customers to have multiple datasets available that can be switched between easily through configuration.</span></span>

```
  <settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
  </settings>
```

## <a name="additional-resources"></a><span data-ttu-id="91d63-145">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="91d63-145">Additional resources</span></span>

[<span data-ttu-id="91d63-146">Oversigt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="91d63-146">Product recommendations overview</span></span>](../commerce/product-recommendations.md)

[<span data-ttu-id="91d63-147">Miljøplanlægning</span><span class="sxs-lookup"><span data-stu-id="91d63-147">Environment planning</span></span>](../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)
