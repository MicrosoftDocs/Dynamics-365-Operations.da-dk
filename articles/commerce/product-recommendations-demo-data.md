---
title: Få produktanbefalinger ved hjælp af demo-data
description: Dette dokument er en vejledning til, hvordan du kan udnytte produktanbefalinger til omni-kanal i niveau-1 enkelt boks-miljøer med forudindstillede demodata, der kan tilpasses.
author: bebeale
manager: AnnBe
ms.date: 10/01/19
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
ms.openlocfilehash: af8a30e69d9ed143e045950efdcece207f6da14c
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697928"
---
# <a name="get-product-recommendations-using-demo-data"></a><span data-ttu-id="4d566-103">Få produktanbefalinger ved hjælp af demo-data</span><span class="sxs-lookup"><span data-stu-id="4d566-103">Get product recommendations using demo data</span></span>
<span data-ttu-id="4d566-104">Dette dokument er en vejledning til, hvordan du kan udnytte produktanbefalinger til omni-kanal i niveau-1 enkelt boks-miljøer med forudindstillede demodata, der kan tilpasses.</span><span class="sxs-lookup"><span data-stu-id="4d566-104">This document provides guidance on how to leverage omni-channel product recommendations in Tier-1 single box environments using pre-populated, customizable demo data.</span></span>

<span data-ttu-id="4d566-105">Omni-kanalproduktanbefalinger giver et sæt redaktionelt leverede eller programmeringsmæssigt fremstillede lister over produkter.</span><span class="sxs-lookup"><span data-stu-id="4d566-105">Omni-channel product recommendations provide a set of editorially curated or programmatically generated list of products.</span></span> <span data-ttu-id="4d566-106">Disse lister kan bruges i flere forskellige scenarier, afhængigt af virksomhedens behov.</span><span class="sxs-lookup"><span data-stu-id="4d566-106">These lists can be used in several scenarios, depending on the business need.</span></span> <span data-ttu-id="4d566-107">Yderligere oplysninger om lister over produktanbefalinger finder du under [Oversigt over produktanbefalinger](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="4d566-107">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

<span data-ttu-id="4d566-108">For niveau 2 og højere Dynamics 365-miljøer beregnes produktanbefalinger automatisk ud fra kundedata.</span><span class="sxs-lookup"><span data-stu-id="4d566-108">For Tier-2 and higher Dynamics 365 environments, product recommendations are automatically computed based on customer data.</span></span> <span data-ttu-id="4d566-109">Hvis du bruger demodata til produktanbefalinger, deaktiveres ingen af de anbefalinger for produktløsninger, der allerede er klargjort i miljøet, og eventuelle omkostninger, der er forbundet med brugen af dem.</span><span class="sxs-lookup"><span data-stu-id="4d566-109">Using product recommendations demo data does not disable any product recommendations solution already provisioned in the environment and any costs associated with its usage.</span></span>

<span data-ttu-id="4d566-110">Produktanbefalinger for niveau 1-miljøer er udelukkende baseret på de statiske demodata, der er gemt i en .csv-fil.</span><span class="sxs-lookup"><span data-stu-id="4d566-110">For Tier-1 environments, product recommendations are based only off the static demo data stored in a .csv file.</span></span>

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a><span data-ttu-id="4d566-111">Aktivere demodata til produktanbefalinger i et miljø</span><span class="sxs-lookup"><span data-stu-id="4d566-111">Enabling product recommendations demo data in an environment</span></span>
<span data-ttu-id="4d566-112">Du skal udrulle Dynamics 365 Commerce-prøveversionens demoudvidelse i det respektive miljø for at aktivere demodata til produktanbefalinger.</span><span class="sxs-lookup"><span data-stu-id="4d566-112">To enable product recommensations demo date, you need to deploy the Dynamics 365 Commerce Preview Demo Extension to the respective environment.</span></span> <span data-ttu-id="4d566-113">Hvis du gør det automatisk, aktiveres demodata til produktanbefalinger.</span><span class="sxs-lookup"><span data-stu-id="4d566-113">Doing so automatically enables product recommendations demo data.</span></span>

## <a name="default-demo-data"></a><span data-ttu-id="4d566-114">Standarddemodata</span><span class="sxs-lookup"><span data-stu-id="4d566-114">Default demo data</span></span>
<span data-ttu-id="4d566-115">Hvert Onebox-typemiljø indeholder et forudindlæst sæt demodata til produktanbefalinger, der er gemt i den kommaseparerede fil 'reco_demo_data.csv', som er placeret på Retail Server.</span><span class="sxs-lookup"><span data-stu-id="4d566-115">Each Onebox type environment comes with a preloaded set of product recommendations demo data stored in the coma separated ‘reco_demo_data.csv’ file, located on the Retail Server.</span></span>

<span data-ttu-id="4d566-116">Disse data er struktureret langs følgende kolonner.</span><span class="sxs-lookup"><span data-stu-id="4d566-116">The data is structured along the following columns.</span></span>

| <span data-ttu-id="4d566-117">Kolonnenavn</span><span class="sxs-lookup"><span data-stu-id="4d566-117">Column name</span></span>         | <span data-ttu-id="4d566-118">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="4d566-118">Mandatory</span></span>          | <span data-ttu-id="4d566-119">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="4d566-119">Description</span></span>                                                                                                                                 | <span data-ttu-id="4d566-120">Mulige værdier</span><span class="sxs-lookup"><span data-stu-id="4d566-120">Possible Values</span></span>                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="4d566-121">RecoList</span><span class="sxs-lookup"><span data-stu-id="4d566-121">RecoList</span></span>            | :heavy_check_mark: | <span data-ttu-id="4d566-123">Den specifikke listetype for produktanbefalinger, som demodatapunktet skal generere.</span><span class="sxs-lookup"><span data-stu-id="4d566-123">The specific product recommendation list type that the demo data point is to generate.</span></span>                                                    | <ul><li><span data-ttu-id="4d566-124">RecoBestSelling</span><span class="sxs-lookup"><span data-stu-id="4d566-124">RecoBestSelling</span></span></li><li><span data-ttu-id="4d566-125">RecoNew</span><span class="sxs-lookup"><span data-stu-id="4d566-125">RecoNew</span></span></li><li><span data-ttu-id="4d566-126">RecoTrending</span><span class="sxs-lookup"><span data-stu-id="4d566-126">RecoTrending</span></span></li><li><span data-ttu-id="4d566-127">RecoCart</span><span class="sxs-lookup"><span data-stu-id="4d566-127">RecoCart</span></span></li><li><span data-ttu-id="4d566-128">RecoPeopleAlsoBuy</span><span class="sxs-lookup"><span data-stu-id="4d566-128">RecoPeopleAlsoBuy</span></span></li></ul> |
| <span data-ttu-id="4d566-129">OperatingUnitNumber</span><span class="sxs-lookup"><span data-stu-id="4d566-129">OperatingUnitNumber</span></span> | :heavy_check_mark: | <span data-ttu-id="4d566-131">Det specifikke driftsenhedsnummer, hvor produktanbefalinger forventes at blive synlige.</span><span class="sxs-lookup"><span data-stu-id="4d566-131">The specific operating unit number where product recommendations are expected to be   surfaced.</span></span>                                        |                                                                              |
| <span data-ttu-id="4d566-132">Kategori</span><span class="sxs-lookup"><span data-stu-id="4d566-132">Category</span></span>            |                    |    <span data-ttu-id="4d566-133">Den kategori, som den specifikke liste skal returneres for.</span><span class="sxs-lookup"><span data-stu-id="4d566-133">The category the specific list should be returned for.</span></span> <span data-ttu-id="4d566-134">Hvis der ikke er angivet en kategori, gælder listen kun for det øverste navigationshierarki.</span><span class="sxs-lookup"><span data-stu-id="4d566-134">If no category is specified, the list is for top of navigation hierarchy only.</span></span>    |                                                                              |
| <span data-ttu-id="4d566-135">SeedItemId</span><span class="sxs-lookup"><span data-stu-id="4d566-135">SeedItemId</span></span>          |                    |    <span data-ttu-id="4d566-136">Til lister, der kræver oprindelsesdata (RecoPeopleAlsoBuy og RecoCart), skal produktet indeholde supplerende produkter til disse lister.</span><span class="sxs-lookup"><span data-stu-id="4d566-136">For lists that require seed (RecoPeopleAlsoBuy and RecoCart), the product those lists should show additional products for.</span></span>            |                                                                              |
| <span data-ttu-id="4d566-137">ItemIds</span><span class="sxs-lookup"><span data-stu-id="4d566-137">ItemIds</span></span>             | :heavy_check_mark: | <span data-ttu-id="4d566-139">Et eller flere produkter, der skal returneres som resultat, adskilt af ';'.</span><span class="sxs-lookup"><span data-stu-id="4d566-139">One or more products to be returned as the result, separated by ‘;’.</span></span>                                                                  |                                                                              |

## <a name="customize-demo-data"></a><span data-ttu-id="4d566-140">Tilpasse demodata</span><span class="sxs-lookup"><span data-stu-id="4d566-140">Customize demo data</span></span>
<span data-ttu-id="4d566-141">Du kan redigere standarddemodataene med eventuelle produkt- og kategorioplysninger, der er konfigureret i hovedkontoret.</span><span class="sxs-lookup"><span data-stu-id="4d566-141">You can edit the default demo data with any product and category information configured in HQ.</span></span> <span data-ttu-id="4d566-142">Når du opdaterer .csv-filen, afspejler de produktanbefalinger, der returneres til kunderne, straks ændringerne.</span><span class="sxs-lookup"><span data-stu-id="4d566-142">Once you update the .csv, the product recommendations that are returned to customers will immediately reflect the changes.</span></span>

<span data-ttu-id="4d566-143">Udvidelsen indeholder en datafil med navnet 'RecoMockDataset.csv', som giver dig mulighed for at styre det datasæt, der bruges til at styrke de anbefalede resultater.</span><span class="sxs-lookup"><span data-stu-id="4d566-143">The extension contains a datafile called 'RecoMockDataset.csv' which allows you to control the dataset used to power the mock recommendations results.</span></span> <span data-ttu-id="4d566-144">Filnavnet kan styres via udvidelseskonfiguration ved hjælp af indstillingen **ext.Recommendations.DemoFilePath**.</span><span class="sxs-lookup"><span data-stu-id="4d566-144">The file name can be controlled through extension configuration using the **ext.Recommendations.DemoFilePath** setting.</span></span> <span data-ttu-id="4d566-145">Det giver dig mulighed for at have flere tilgængelige datasæt, der kan skiftes mellem nemt og hurtigt under konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="4d566-145">This enables you to have multiple datasets available that can be switched between easily through configuration.</span></span>


```
  <settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
  </settings>
```

## <a name="additional-resources"></a><span data-ttu-id="4d566-146">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="4d566-146">Additional Resources</span></span>

[<span data-ttu-id="4d566-147">Oversigt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="4d566-147">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="4d566-148">Miljøplanlægning</span><span class="sxs-lookup"><span data-stu-id="4d566-148">Environment planning</span></span>](../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)
