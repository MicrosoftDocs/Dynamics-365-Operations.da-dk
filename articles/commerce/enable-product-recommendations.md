---
title: Aktivér produktanbefalinger
description: I dette emne beskrives, hvordan du kan lave produktanbefalinger, der er baseret på kunstig intelligens-maskinel læring (AI-ML), som er tilgængelig for Microsoft Dynamics 365 Commerce-kunder.
author: bebeale
manager: AnnBe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d38d7b0e98d84e23d7a51c5d8ee65df4a3b9e4a7
ms.sourcegitcommit: dbff1c6bb371a443a0cd2a310f5a48d5c21b08ca
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/13/2020
ms.locfileid: "3259788"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="8b08c-103">Aktivér produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="8b08c-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8b08c-104">I dette emne beskrives, hvordan du kan lave produktanbefalinger, der er baseret på kunstig intelligens-maskinel læring (AI-ML), som er tilgængelig for Microsoft Dynamics 365 Commerce-kunder.</span><span class="sxs-lookup"><span data-stu-id="8b08c-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="8b08c-105">Yderligere oplysninger om lister over produktanbefalinger finder du under [Oversigt over produktanbefalinger](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="8b08c-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="8b08c-106">Forhåndscheck af anbefalinger</span><span class="sxs-lookup"><span data-stu-id="8b08c-106">Recommendations pre-check</span></span>

<span data-ttu-id="8b08c-107">Før du aktiverer, skal du vide, at produktanbefalingerne kun understøttes for Commerce-kunder, som har overført deres lager for at bruge Azure Data Lake Storage (ADLS).</span><span class="sxs-lookup"><span data-stu-id="8b08c-107">Before enabling, note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage (ADLS).</span></span> 

<span data-ttu-id="8b08c-108">Følgende konfigurationer skal aktiveres i administrationen, før du aktiverer anbefalinger:</span><span class="sxs-lookup"><span data-stu-id="8b08c-108">The following configurations must be enabled in the back office before enabling recommendations:</span></span>

1. <span data-ttu-id="8b08c-109">Kontrollér, at ADLS er købt og godkendt i miljøet.</span><span class="sxs-lookup"><span data-stu-id="8b08c-109">Ensure that ADLS has been purchased and successfully verified in the environment.</span></span> <span data-ttu-id="8b08c-110">Du kan få flere oplysninger i [Kontrollér, at ADLS er købt og godkendt i miljøet](enable-ADLS-environment.md).</span><span class="sxs-lookup"><span data-stu-id="8b08c-110">For more information, see [Ensure that ADLS has been purchased and successfully verified in the environment](enable-ADLS-environment.md).</span></span>
2. <span data-ttu-id="8b08c-111">Sørg for, at opdatering af enhedslageret er automatiseret.</span><span class="sxs-lookup"><span data-stu-id="8b08c-111">Ensure that the entity store refresh has been automated.</span></span> <span data-ttu-id="8b08c-112">Du kan finde flere oplysninger i [Sørg for, at opdatering af enhedslageret er automatiseret](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="8b08c-112">For more information, see [Ensure that the Entity store refresh has been automated](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span></span>
3. <span data-ttu-id="8b08c-113">Bekræft, at Azure AD-identitetskonfiguration indeholder en indtastning til anbefalinger.</span><span class="sxs-lookup"><span data-stu-id="8b08c-113">Confirm that Azure AD Identity configuration contains an entry for Recommendations.</span></span> <span data-ttu-id="8b08c-114">Du kan få flere oplysninger om, hvordan denne handling udføres, nedenfor.</span><span class="sxs-lookup"><span data-stu-id="8b08c-114">More information on how to do this action is below.</span></span>

<span data-ttu-id="8b08c-115">Derudover skal du kontrollere, at RetailSale-målinger er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="8b08c-115">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="8b08c-116">Du kan få mere at vide om denne opsætning i [Arbejde med målpunkter](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).</span><span class="sxs-lookup"><span data-stu-id="8b08c-116">To learn more about this set up process, see [Work with measures](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).</span></span>

## <a name="azure-ad-identity-configuration"></a><span data-ttu-id="8b08c-117">Azure AD-identitetskonfiguration</span><span class="sxs-lookup"><span data-stu-id="8b08c-117">Azure AD Identity configuration</span></span>

<span data-ttu-id="8b08c-118">Dette trin er obligatorisk for alle kunder, der kører en IaaS-konfiguration (Infra-Structure as a Service).</span><span class="sxs-lookup"><span data-stu-id="8b08c-118">This step is required for all customers running an infra-structure as a service (IaaS) configuration.</span></span> <span data-ttu-id="8b08c-119">For kunder, der kører på service fabric (SF), skal dette trin være automatisk, og det anbefales, at man kontrollerer, at indstillingen er konfigureret som forventet.</span><span class="sxs-lookup"><span data-stu-id="8b08c-119">For customers running on service fabric (SF), this step should be automatic and we recommend verifying the setting is configured as expected.</span></span>

### <a name="setup"></a><span data-ttu-id="8b08c-120">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="8b08c-120">Setup</span></span>

1. <span data-ttu-id="8b08c-121">Fra administrationen skal du søge efter siden **Azure Active Directory-programmer**.</span><span class="sxs-lookup"><span data-stu-id="8b08c-121">From the back office, search for the **Azure Active Directory applications** page.</span></span>
2. <span data-ttu-id="8b08c-122">Kontrollér, om der findes en post for "RecommendationSystemApplication-1".</span><span class="sxs-lookup"><span data-stu-id="8b08c-122">Verify if an entry exists for "RecommendationSystemApplication-1".</span></span>

<span data-ttu-id="8b08c-123">Hvis posten ikke findes, skal du tilføje en ny post med følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="8b08c-123">If the entry does not exist, add a new entry with the following information:</span></span>

- <span data-ttu-id="8b08c-124">**Klient-id** – d37b07e8-dd1c-4514-835d-8b918e6f9727</span><span class="sxs-lookup"><span data-stu-id="8b08c-124">**Client Id** - d37b07e8-dd1c-4514-835d-8b918e6f9727</span></span>
- <span data-ttu-id="8b08c-125">**Navn** – RecommendationSystemApplication-1</span><span class="sxs-lookup"><span data-stu-id="8b08c-125">**Name** - RecommendationSystemApplication-1</span></span>
- <span data-ttu-id="8b08c-126">**Bruger-id** – RetailServiceAccount</span><span class="sxs-lookup"><span data-stu-id="8b08c-126">**User Id** - RetailServiceAccount</span></span>

<span data-ttu-id="8b08c-127">Gem og luk siden.</span><span class="sxs-lookup"><span data-stu-id="8b08c-127">Save and close the page.</span></span> 

## <a name="turn-on-recommendations"></a><span data-ttu-id="8b08c-128">Aktivere anbefalinger</span><span class="sxs-lookup"><span data-stu-id="8b08c-128">Turn on recommendations</span></span>

<span data-ttu-id="8b08c-129">Benyt følgende fremgangsmåde for at aktivere produktanbefalinger.</span><span class="sxs-lookup"><span data-stu-id="8b08c-129">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="8b08c-130">Gå til **Retail og Commerce &gt; Produktanbefalinger &gt; Anbefalingsparametre**.</span><span class="sxs-lookup"><span data-stu-id="8b08c-130">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation parameters**.</span></span>
1. <span data-ttu-id="8b08c-131">Vælg **Anbefalingslister** på listen over delte parametre.</span><span class="sxs-lookup"><span data-stu-id="8b08c-131">In the list of shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="8b08c-132">Vælg **Ja** i indstillingen **Aktivér anbefalinger**.</span><span class="sxs-lookup"><span data-stu-id="8b08c-132">Set the **Enable recommendations** option to **Yes**.</span></span>

![Slå anbefalinger til](./media/enablepersonalization.png)

> [!NOTE]
> <span data-ttu-id="8b08c-134">Denne procedure starter processen til oprettelse af produktanbefalingslister.</span><span class="sxs-lookup"><span data-stu-id="8b08c-134">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="8b08c-135">Der kan tage op til flere timer, før listerne er tilgængelige og bliver vist på POS eller i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8b08c-135">It may take several hours before the lists are available and can be viewed at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="8b08c-136">Konfigurere parametre for anbefalingslister</span><span class="sxs-lookup"><span data-stu-id="8b08c-136">Configure recommendation list parameters</span></span>

<span data-ttu-id="8b08c-137">Den AI-ML-baserede produktanbefalingsliste angiver som standard foreslåede værdier.</span><span class="sxs-lookup"><span data-stu-id="8b08c-137">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="8b08c-138">Du kan ændre de foreslåede standardværdier, så de passer til dit firmas flow.</span><span class="sxs-lookup"><span data-stu-id="8b08c-138">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="8b08c-139">Hvis du vil vide mere om, hvordan du ændrer standardparametrene, skal du gå til [Administrere resultater for AI-ML-baserede produktanbefalinger](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="8b08c-139">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="8b08c-140">Vise anbefalinger på POS-enheder</span><span class="sxs-lookup"><span data-stu-id="8b08c-140">Show recommendations on POS devices</span></span>

<span data-ttu-id="8b08c-141">Når anbefalingerne er aktiveret i Commerce-administrationen, skal anbefalingspanelet føjes til kontrolelementets POS-skærm ved hjælp af layoutværktøjet.</span><span class="sxs-lookup"><span data-stu-id="8b08c-141">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="8b08c-142">Du kan få mere at vide om denne proces i [Føje et kontrolelement med anbefalinger til posteringsskærmen på POS-enheder](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="8b08c-142">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="8b08c-143">Aktivere tilpassede anbefalinger</span><span class="sxs-lookup"><span data-stu-id="8b08c-143">Enable personalized recommendations</span></span>

<span data-ttu-id="8b08c-144">I Dynamics 365 Commerce kan detailhandlere gøre personligt tilpassede produktanbefalinger tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="8b08c-144">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="8b08c-145">På denne måde kan personlige anbefalinger indarbejdes i den online kundeoplevelse og på salgsstedet (POS).</span><span class="sxs-lookup"><span data-stu-id="8b08c-145">In this way, personalized recommendations can be incorporated into the online customer experience and at the point of sale.</span></span> <span data-ttu-id="8b08c-146">Når tilpasningsfunktionen er slået til, kan systemet tilknytte en brugers købs- og produktoplysninger for at generere individuelle produktanbefalinger.</span><span class="sxs-lookup"><span data-stu-id="8b08c-146">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

<span data-ttu-id="8b08c-147">Du kan få flere oplysninger om tilpassede anbefalinger i [Aktivere personlige anbefalinger](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="8b08c-147">To learn more about personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8b08c-148">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="8b08c-148">Additional resources</span></span>

[<span data-ttu-id="8b08c-149">Oversigt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="8b08c-149">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="8b08c-150">Aktivere ADLS i et Dynamics 365 Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="8b08c-150">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="8b08c-151">Aktivere tilpassede anbefalinger</span><span class="sxs-lookup"><span data-stu-id="8b08c-151">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="8b08c-152">Fravælge tilpassede anbefalinger</span><span class="sxs-lookup"><span data-stu-id="8b08c-152">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="8b08c-153">Tilføje produktanbefalinger på POS</span><span class="sxs-lookup"><span data-stu-id="8b08c-153">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="8b08c-154">Føje anbefalinger til transaktionsskærmen</span><span class="sxs-lookup"><span data-stu-id="8b08c-154">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="8b08c-155">Justere resultater for AI-ML-anbefalinger</span><span class="sxs-lookup"><span data-stu-id="8b08c-155">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="8b08c-156">Oprette overvågede anbefalinger manuelt</span><span class="sxs-lookup"><span data-stu-id="8b08c-156">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="8b08c-157">Oprette anbefalinger med demonstrationsdata</span><span class="sxs-lookup"><span data-stu-id="8b08c-157">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="8b08c-158">Ofte stillede spørgsmål om produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="8b08c-158">Product recommendations FAQ</span></span>](faq-recommendations.md)

