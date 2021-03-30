---
title: Aktivér produktanbefalinger
description: I dette emne beskrives, hvordan du kan lave produktanbefalinger, der er baseret på kunstig intelligens-maskinel læring (AI-ML), som er tilgængelig for Microsoft Dynamics 365 Commerce-kunder.
author: bebeale
manager: AnnBe
ms.date: 08/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fcb3b542d290e01a3cddc73ae163ed2ef420771b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238780"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="56848-103">Aktivér produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="56848-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="56848-104">I dette emne beskrives, hvordan du kan lave produktanbefalinger, der er baseret på kunstig intelligens-maskinel læring (AI-ML), som er tilgængelig for Microsoft Dynamics 365 Commerce-kunder.</span><span class="sxs-lookup"><span data-stu-id="56848-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="56848-105">Yderligere oplysninger om lister over produktanbefalinger finder du under [Oversigt over produktanbefalinger](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="56848-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="56848-106">Forhåndscheck af anbefalinger</span><span class="sxs-lookup"><span data-stu-id="56848-106">Recommendations pre-check</span></span>

<span data-ttu-id="56848-107">Før du aktiverer, skal du vide, at produktanbefalingerne kun understøttes for Commerce-kunder, som har overført deres lager for at bruge Azure Data Lake Storage.</span><span class="sxs-lookup"><span data-stu-id="56848-107">Before enabling, note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage.</span></span> 

<span data-ttu-id="56848-108">Følgende konfigurationer skal aktiveres i administrationen, før du aktiverer anbefalinger:</span><span class="sxs-lookup"><span data-stu-id="56848-108">The following configurations must be enabled in the back office before enabling recommendations:</span></span>

1. <span data-ttu-id="56848-109">Kontrollér, at Azure Data Lake Storage er købt og godkendt i miljøet.</span><span class="sxs-lookup"><span data-stu-id="56848-109">Ensure that Azure Data Lake Storage has been purchased and successfully verified in the environment.</span></span> <span data-ttu-id="56848-110">Du kan få flere oplysninger i [Kontrollér, at Azure Data Lake Storage er købt og godkendt i miljøet](enable-ADLS-environment.md).</span><span class="sxs-lookup"><span data-stu-id="56848-110">For more information, see [Ensure that Azure Data Lake Storage has been purchased and successfully verified in the environment](enable-ADLS-environment.md).</span></span>
2. <span data-ttu-id="56848-111">Sørg for, at opdatering af enhedslageret er automatiseret.</span><span class="sxs-lookup"><span data-stu-id="56848-111">Ensure that the entity store refresh has been automated.</span></span> <span data-ttu-id="56848-112">Du kan finde flere oplysninger i [Sørg for, at opdatering af enhedslageret er automatiseret](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="56848-112">For more information, see [Ensure that the Entity store refresh has been automated](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span></span>
3. <span data-ttu-id="56848-113">Bekræft, at Azure AD-identitetskonfiguration indeholder en indtastning til anbefalinger.</span><span class="sxs-lookup"><span data-stu-id="56848-113">Confirm that Azure AD Identity configuration contains an entry for Recommendations.</span></span> <span data-ttu-id="56848-114">Du kan få flere oplysninger om, hvordan denne handling udføres, nedenfor.</span><span class="sxs-lookup"><span data-stu-id="56848-114">More information on how to do this action is below.</span></span>

<span data-ttu-id="56848-115">Derudover skal du kontrollere, at RetailSale-målinger er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="56848-115">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="56848-116">Du kan få mere at vide om denne opsætning i [Arbejde med målpunkter](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).</span><span class="sxs-lookup"><span data-stu-id="56848-116">To learn more about this set up process, see [Work with measures](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).</span></span>

## <a name="azure-ad-identity-configuration"></a><span data-ttu-id="56848-117">Azure AD-identitetskonfiguration</span><span class="sxs-lookup"><span data-stu-id="56848-117">Azure AD Identity configuration</span></span>

<span data-ttu-id="56848-118">Dette trin er obligatorisk for alle kunder, der kører en IaaS-konfiguration (Infra-Structure as a Service).</span><span class="sxs-lookup"><span data-stu-id="56848-118">This step is required for all customers running an infra-structure as a service (IaaS) configuration.</span></span> <span data-ttu-id="56848-119">For kunder, der kører på service fabric (SF), skal dette trin være automatisk, og det anbefales, at man kontrollerer, at indstillingen er konfigureret som forventet.</span><span class="sxs-lookup"><span data-stu-id="56848-119">For customers running on service fabric (SF), this step should be automatic and we recommend verifying the setting is configured as expected.</span></span>

### <a name="setup"></a><span data-ttu-id="56848-120">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="56848-120">Setup</span></span>

1. <span data-ttu-id="56848-121">Fra administrationen skal du søge efter siden **Azure Active Directory-programmer**.</span><span class="sxs-lookup"><span data-stu-id="56848-121">From the back office, search for the **Azure Active Directory applications** page.</span></span>
2. <span data-ttu-id="56848-122">Kontrollér, om der findes en post for "RecommendationSystemApplication-1".</span><span class="sxs-lookup"><span data-stu-id="56848-122">Verify if an entry exists for "RecommendationSystemApplication-1".</span></span>

<span data-ttu-id="56848-123">Hvis posten ikke findes, skal du tilføje en ny post med følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="56848-123">If the entry does not exist, add a new entry with the following information:</span></span>

- <span data-ttu-id="56848-124">**Klient-id** – d37b07e8-dd1c-4514-835d-8b918e6f9727</span><span class="sxs-lookup"><span data-stu-id="56848-124">**Client Id** - d37b07e8-dd1c-4514-835d-8b918e6f9727</span></span>
- <span data-ttu-id="56848-125">**Navn** – RecommendationSystemApplication-1</span><span class="sxs-lookup"><span data-stu-id="56848-125">**Name** - RecommendationSystemApplication-1</span></span>
- <span data-ttu-id="56848-126">**Bruger-id** – RetailServiceAccount</span><span class="sxs-lookup"><span data-stu-id="56848-126">**User Id** - RetailServiceAccount</span></span>

<span data-ttu-id="56848-127">Gem og luk siden.</span><span class="sxs-lookup"><span data-stu-id="56848-127">Save and close the page.</span></span> 

## <a name="turn-on-recommendations"></a><span data-ttu-id="56848-128">Aktivere anbefalinger</span><span class="sxs-lookup"><span data-stu-id="56848-128">Turn on recommendations</span></span>

<span data-ttu-id="56848-129">Benyt følgende fremgangsmåde for at aktivere produktanbefalinger.</span><span class="sxs-lookup"><span data-stu-id="56848-129">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="56848-130">Søg efter **Funktionsstyring** i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="56848-130">In Commerce headquarters, search for **Feature Management**.</span></span>
1. <span data-ttu-id="56848-131">Vælg **Alle** for at få vist en liste over tilgængelige funktioner.</span><span class="sxs-lookup"><span data-stu-id="56848-131">Select **All** to see a list of available features.</span></span> 
1. <span data-ttu-id="56848-132">Skriv **Anbefalinger** i søgefeltet.</span><span class="sxs-lookup"><span data-stu-id="56848-132">In the search box, enter **Recommendations**.</span></span>
1. <span data-ttu-id="56848-133">Vælg funktionen **Produktanbefalinger**.</span><span class="sxs-lookup"><span data-stu-id="56848-133">Select the **Product recommendations** feature.</span></span>
1. <span data-ttu-id="56848-134">Vælg **Aktivér nu** i ruden med egenskaber for **Produktanbefalinger**.</span><span class="sxs-lookup"><span data-stu-id="56848-134">In the **Product recommendations** properties pane, select **Enable now**.</span></span>

![Slå anbefalinger til](./media/FeatureManagement_Recommendations.PNG)

> [!NOTE]
> <span data-ttu-id="56848-136">Denne procedure starter processen til oprettelse af produktanbefalingslister.</span><span class="sxs-lookup"><span data-stu-id="56848-136">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="56848-137">Der kan tage op til flere timer, før listerne er tilgængelige og bliver vist på POS eller i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="56848-137">It may take several hours before the lists are available and can be viewed at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="56848-138">Konfigurere parametre for anbefalingslister</span><span class="sxs-lookup"><span data-stu-id="56848-138">Configure recommendation list parameters</span></span>

<span data-ttu-id="56848-139">Den AI-ML-baserede produktanbefalingsliste angiver som standard foreslåede værdier.</span><span class="sxs-lookup"><span data-stu-id="56848-139">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="56848-140">Du kan ændre de foreslåede standardværdier, så de passer til dit firmas flow.</span><span class="sxs-lookup"><span data-stu-id="56848-140">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="56848-141">Hvis du vil vide mere om, hvordan du ændrer standardparametrene, skal du gå til [Administrere resultater for AI-ML-baserede produktanbefalinger](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="56848-141">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="56848-142">Vise anbefalinger på POS-enheder</span><span class="sxs-lookup"><span data-stu-id="56848-142">Show recommendations on POS devices</span></span>

<span data-ttu-id="56848-143">Når anbefalingerne er aktiveret i Commerce-administrationen, skal anbefalingspanelet føjes til kontrolelementets POS-skærm ved hjælp af layoutværktøjet.</span><span class="sxs-lookup"><span data-stu-id="56848-143">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="56848-144">Du kan få mere at vide om denne proces i [Føje et kontrolelement med anbefalinger til posteringsskærmen på POS-enheder](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="56848-144">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="56848-145">Aktivere tilpassede anbefalinger</span><span class="sxs-lookup"><span data-stu-id="56848-145">Enable personalized recommendations</span></span>

<span data-ttu-id="56848-146">I Dynamics 365 Commerce kan detailhandlere gøre personligt tilpassede produktanbefalinger tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="56848-146">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="56848-147">På denne måde kan personlige anbefalinger indarbejdes i den online kundeoplevelse og på salgsstedet (POS).</span><span class="sxs-lookup"><span data-stu-id="56848-147">In this way, personalized recommendations can be incorporated into the online customer experience and at the point of sale.</span></span> <span data-ttu-id="56848-148">Når tilpasningsfunktionen er slået til, kan systemet tilknytte en brugers købs- og produktoplysninger for at generere individuelle produktanbefalinger.</span><span class="sxs-lookup"><span data-stu-id="56848-148">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

<span data-ttu-id="56848-149">Du kan få flere oplysninger om tilpassede anbefalinger i [Aktivere personlige anbefalinger](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="56848-149">To learn more about personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="56848-150">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="56848-150">Additional resources</span></span>

[<span data-ttu-id="56848-151">Oversigt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="56848-151">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="56848-152">Aktivér Azure Data Lake Storage i et Dynamics 365 Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="56848-152">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="56848-153">Aktivere tilpassede anbefalinger</span><span class="sxs-lookup"><span data-stu-id="56848-153">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="56848-154">Aktivere anbefalinger af "Køb tilsvarende"</span><span class="sxs-lookup"><span data-stu-id="56848-154">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="56848-155">Fravælge tilpassede anbefalinger</span><span class="sxs-lookup"><span data-stu-id="56848-155">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="56848-156">Tilføje produktanbefalinger på POS</span><span class="sxs-lookup"><span data-stu-id="56848-156">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="56848-157">Føje anbefalinger til transaktionsskærmen</span><span class="sxs-lookup"><span data-stu-id="56848-157">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="56848-158">Justere resultater for AI-ML-anbefalinger</span><span class="sxs-lookup"><span data-stu-id="56848-158">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="56848-159">Oprette overvågede anbefalinger manuelt</span><span class="sxs-lookup"><span data-stu-id="56848-159">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="56848-160">Oprette anbefalinger med demonstrationsdata</span><span class="sxs-lookup"><span data-stu-id="56848-160">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="56848-161">Ofte stillede spørgsmål om produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="56848-161">Product recommendations FAQ</span></span>](faq-recommendations.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]