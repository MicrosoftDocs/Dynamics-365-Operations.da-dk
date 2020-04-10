---
title: Aktivere ADLS i et Dynamics 365 Commerce-miljø
description: Dette emne forklarer, hvordan du aktiverer og tester Azure Data Lake Storage (ADLS) for et Dynamics 365 Commerce-miljø, som er en forudsætning for, at du kan aktivere produktanbefalinger.
author: bebeale
manager: AnnBe
ms.date: 03/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3c037f5603af5af84917084eefa1edd508891c0d
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154430"
---
# <a name="enable-adls-in-a-dynamics-365-commerce-environment"></a><span data-ttu-id="e6205-103">Aktivere ADLS i et Dynamics 365 Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="e6205-103">Enable ADLS in a Dynamics 365 Commerce environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e6205-104">Dette emne forklarer, hvordan du aktiverer og tester Azure Data Lake Storage (ADLS) for et Dynamics 365 Commerce-miljø, som er en forudsætning for, at du kan aktivere produktanbefalinger.</span><span class="sxs-lookup"><span data-stu-id="e6205-104">This topic explains how to enable and test Azure Data Lake Storage (ADLS) for a Dynamics 365 Commerce environment, which is a prerequisite for enabling product recommendations.</span></span>

## <a name="overview"></a><span data-ttu-id="e6205-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="e6205-105">Overview</span></span>

<span data-ttu-id="e6205-106">I Dynamics 365 Commerce-løsningen spores alle produkt- og transaktionsoplysninger i miljøets enhedslager.</span><span class="sxs-lookup"><span data-stu-id="e6205-106">In the Dynamics 365 Commerce solution, all product and transaction information is tracked in the environment's Entity store.</span></span> <span data-ttu-id="e6205-107">For at gøre disse data tilgængelige for andre Dynamics 365-tjenester, f.eks. dataanalyse, business intelligence og personlige anbefalinger, er det nødvendigt at knytte miljøet til en kundeejet Azure Data Lake Storage Gen 2-løsning (ADLS).</span><span class="sxs-lookup"><span data-stu-id="e6205-107">To make this data accessible to other Dynamics 365 services, such as data analytics, business intelligence, and personalized recommendations, it is necessary to connect the environment to a customer-owned Azure Data Lake Storage Gen 2 (ADLS) solution.</span></span>

<span data-ttu-id="e6205-108">Da ADLS er konfigureret i et miljø, spejles alle nødvendige data fra enhedslageret, mens de stadig er beskyttet og under kundens kontrol.</span><span class="sxs-lookup"><span data-stu-id="e6205-108">As ADLS is configured in an environment, all necessary data is mirrored from the Entity store while still being protected and under customer's control.</span></span>

<span data-ttu-id="e6205-109">Hvis produktanbefalinger eller personlige anbefalinger også er aktiveret i miljøet, vil stakken med produktanbefalinger blive tildelt adgang til den dedikerede mappe i ADLS for at hente kundens data og beregne anbefalinger baseret på den.</span><span class="sxs-lookup"><span data-stu-id="e6205-109">If product recommendations or personalized recommendations are also enabled in the environment, then the product recommendations stack will be granted access to the dedicated folder in ADLS to retrieve the customer’s data and compute recommendations based on it.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e6205-110">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="e6205-110">Prerequisites</span></span>

<span data-ttu-id="e6205-111">Kunderne skal have ADLS konfigureret i et Azure-abonnement, som de ejer.</span><span class="sxs-lookup"><span data-stu-id="e6205-111">Customers need to have ADLS configured in an Azure subscription that they own.</span></span> <span data-ttu-id="e6205-112">Dette emne dækker ikke købet af et Azure-abonnement eller opsætningen af en ADLS-aktiveret lagerkonto.</span><span class="sxs-lookup"><span data-stu-id="e6205-112">This topic does not cover the purchase of an Azure subscription or the setup of an ADLS-enabled storage account.</span></span>

<span data-ttu-id="e6205-113">Du kan finde flere oplysninger om ADLS i [ADLS officiel dokumentation](https://azure.microsoft.com/pricing/details/storage/data-lake).</span><span class="sxs-lookup"><span data-stu-id="e6205-113">For more information about ADLS, see [ADLS official documentation](https://azure.microsoft.com/pricing/details/storage/data-lake).</span></span>
  
## <a name="configuration-steps"></a><span data-ttu-id="e6205-114">Konfigurationstrin</span><span class="sxs-lookup"><span data-stu-id="e6205-114">Configuration steps</span></span>

<span data-ttu-id="e6205-115">I dette afsnit beskrives de konfigurationstrin, der er nødvendige for at aktivere ADLS i et miljø.</span><span class="sxs-lookup"><span data-stu-id="e6205-115">This section covers the configuration steps necessary for enabling ADLS in an environment.</span></span>

### <a name="enable-adls-in-the-environment"></a><span data-ttu-id="e6205-116">Aktivere ADLS i miljøet</span><span class="sxs-lookup"><span data-stu-id="e6205-116">Enable ADLS in the environment</span></span>

1. <span data-ttu-id="e6205-117">Log på miljøets administrationsportal.</span><span class="sxs-lookup"><span data-stu-id="e6205-117">Log in to the environment's back office portal.</span></span>
1. <span data-ttu-id="e6205-118">Søg efter **Systemparametre**, og gå til fanen **Dataforbindelser**.</span><span class="sxs-lookup"><span data-stu-id="e6205-118">Search for **System Parameters** and navigate to the **Data connections** tab.</span></span> 
1. <span data-ttu-id="e6205-119">Angiv **Aktivér Data Lake-integration** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="e6205-119">Set **Enable Data Lake integration** to **Yes**.</span></span>
1. <span data-ttu-id="e6205-120">Angiv **Foretag sivende opdatering af Data Lake** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="e6205-120">Set **Trickle update Data Lake** to **Yes**.</span></span>
1. <span data-ttu-id="e6205-121">Angiv derefter følgende nødvendige oplysninger:</span><span class="sxs-lookup"><span data-stu-id="e6205-121">Next, enter the following required information:</span></span>
    1. <span data-ttu-id="e6205-122">**Program-id** // **Programhemmelighed** // **DNS-navn** – skal bruges til at oprette forbindelse til KeyVault, hvor ADLS-hemmeligheden opbevares.</span><span class="sxs-lookup"><span data-stu-id="e6205-122">**Application ID** // **Application Secret** // **DNS Name** - Needed to connect to KeyVault where the ADLS secret is stored.</span></span>
    1. <span data-ttu-id="e6205-123">**Hemmeligt navn** – det hemmelige navn, der er gemt i KeyVault og bruges til at godkende med ADLS.</span><span class="sxs-lookup"><span data-stu-id="e6205-123">**Secret name** - The secret name stored in KeyVault and used to authenticate with ADLS.</span></span>
1. <span data-ttu-id="e6205-124">Gem ændringerne i øverste venstre hjørne af siden.</span><span class="sxs-lookup"><span data-stu-id="e6205-124">Save your changes in the top left corner of the page.</span></span>

<span data-ttu-id="e6205-125">Følgende billede viser et eksempel på en ADLS-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="e6205-125">The following image shows an example ADLS configuration.</span></span>

![Eksempel på ADLS-konfiguration](./media/exampleADLSConfig1.png)

### <a name="test-the-adls-connection"></a><span data-ttu-id="e6205-127">Test ADLS-forbindelsen</span><span class="sxs-lookup"><span data-stu-id="e6205-127">Test the ADLS connection</span></span>

1. <span data-ttu-id="e6205-128">Test forbindelsen til KeyVault ved hjælp af linket **Test Azure Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="e6205-128">Test the connection to KeyVault using the **Test Azure Key Vault** link.</span></span>
1. <span data-ttu-id="e6205-129">Test forbindelsen til ADLS ved hjælp af linket **Test Azure Storage**.</span><span class="sxs-lookup"><span data-stu-id="e6205-129">Test the connection to ADLS using the **Test Azure Storage** link.</span></span>

> [!NOTE]
> <span data-ttu-id="e6205-130">Hvis testene ikke lykkes, skal du dobbelttjekke, at alle KeyVault-oplysningerne, der er tilføjet ovenfor, er korrekte, og derefter prøve igen.</span><span class="sxs-lookup"><span data-stu-id="e6205-130">If the tests fail, double-check that all of the KeyVault information added above is correct, then try again.</span></span>

<span data-ttu-id="e6205-131">Når test af forbindelsen er gennemført korrekt, skal du aktivere automatisk opdatering af enhedslageret.</span><span class="sxs-lookup"><span data-stu-id="e6205-131">Once the connection tests are successful, you must enable automatic refresh for Entity store.</span></span>

<span data-ttu-id="e6205-132">Følg disse trin for at aktivere automatisk opdatering af enhedslager.</span><span class="sxs-lookup"><span data-stu-id="e6205-132">To enable automatic refresh for Entity store, follow these steps.</span></span>

1. <span data-ttu-id="e6205-133">Søg efter **Enhedslager**.</span><span class="sxs-lookup"><span data-stu-id="e6205-133">Search for **Entity Store**.</span></span>
1. <span data-ttu-id="e6205-134">Gå til posten **RetailSales** på listen til venstre, og vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="e6205-134">In the list on the left, navigate to the **RetailSales** entry, and select **Edit**.</span></span>
1. <span data-ttu-id="e6205-135">Sørg for, at **Automatisk opdatering er aktiveret** er angivet til **Ja**, vælg **Opdater**, og vælg derefter **Gem**.</span><span class="sxs-lookup"><span data-stu-id="e6205-135">Ensure that **Automatic Refresh Enabled** is set to **Yes**, select **Refresh**, and then select **Save**.</span></span>

<span data-ttu-id="e6205-136">Følgende billede viser et eksempel på enhedslager med automatisk opdatering aktiveret.</span><span class="sxs-lookup"><span data-stu-id="e6205-136">The following image shows an example of Entity store with automatic refresh enabled.</span></span>

![Eksempel på enhedslager med automatisk opdatering aktiveret](./media/exampleADLSConfig2.png)

<span data-ttu-id="e6205-138">ADLS er nu konfigureret for miljøet.</span><span class="sxs-lookup"><span data-stu-id="e6205-138">ADLS is now configured for the environment.</span></span> 

<span data-ttu-id="e6205-139">Hvis det ikke allerede er fuldført, skal du følge trinnene for [aktivering af produktanbefalinger og tilpasning](enable-product-recommendations.md) for miljøet.</span><span class="sxs-lookup"><span data-stu-id="e6205-139">If not completed already, follow the steps for [enabling product recommendations and personalization](enable-product-recommendations.md) for the environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e6205-140">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="e6205-140">Additional resources</span></span>

[<span data-ttu-id="e6205-141">Oversigt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="e6205-141">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="e6205-142">Aktivér produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="e6205-142">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="e6205-143">Aktivere tilpassede anbefalinger</span><span class="sxs-lookup"><span data-stu-id="e6205-143">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="e6205-144">Fravælge tilpassede anbefalinger</span><span class="sxs-lookup"><span data-stu-id="e6205-144">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="e6205-145">Tilføje produktanbefalinger på POS</span><span class="sxs-lookup"><span data-stu-id="e6205-145">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="e6205-146">Føje anbefalinger til transaktionsskærmen</span><span class="sxs-lookup"><span data-stu-id="e6205-146">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="e6205-147">Justere resultater for AI-ML-anbefalinger</span><span class="sxs-lookup"><span data-stu-id="e6205-147">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="e6205-148">Oprette overvågede anbefalinger manuelt</span><span class="sxs-lookup"><span data-stu-id="e6205-148">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="e6205-149">Oprette anbefalinger med demonstrationsdata</span><span class="sxs-lookup"><span data-stu-id="e6205-149">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="e6205-150">Ofte stillede spørgsmål om produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="e6205-150">Product recommendations FAQ</span></span>](faq-recommendations.md)


