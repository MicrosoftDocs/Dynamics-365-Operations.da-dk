---
title: Aktivér produktanbefalinger
description: I dette emne beskrives, hvordan du kan lave produktanbefalinger, der er baseret på kunstig intelligens-maskinel læring (AI-ML), som er tilgængelig for Microsoft Dynamics 365 Commerce-kunder.
author: bebeale
manager: AnnBe
ms.date: 03/12/2020
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
ms.openlocfilehash: 879fccb063ca0b74e0f022a9edf6a15f7d1311ae
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127876"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="1b929-103">Aktivér produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="1b929-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1b929-104">I dette emne beskrives, hvordan du kan lave produktanbefalinger, der er baseret på kunstig intelligens-maskinel læring (AI-ML), som er tilgængelig for Microsoft Dynamics 365 Commerce-kunder.</span><span class="sxs-lookup"><span data-stu-id="1b929-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="1b929-105">Yderligere oplysninger om lister over produktanbefalinger finder du under [Oversigt over produktanbefalinger](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="1b929-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="1b929-106">Forhåndscheck af anbefalinger</span><span class="sxs-lookup"><span data-stu-id="1b929-106">Recommendations pre-check</span></span>

<span data-ttu-id="1b929-107">Før du aktiverer anbefalinger, skal du vide, at produktanbefalingerne kun understøttes for Commerce-kunder, som har overført deres lager for at bruge Azure Data Lake Storage (ADLS).</span><span class="sxs-lookup"><span data-stu-id="1b929-107">Before enabling, please note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage (ADLS).</span></span> 

<span data-ttu-id="1b929-108">Du kan se trinnene til at aktivere i [Sådan aktiveres ADLS i et Dynamics 365-miljø](enable-ADLS-environment.md).</span><span class="sxs-lookup"><span data-stu-id="1b929-108">For steps on enabling ADLS, see [How to enable ADLS in a Dynamics 365 environment](enable-ADLS-environment.md).</span></span>

<span data-ttu-id="1b929-109">Derudover skal du kontrollere, at RetailSale-målinger er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="1b929-109">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="1b929-110">Du kan få mere at vide om denne opsætningsproces [her.](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures)</span><span class="sxs-lookup"><span data-stu-id="1b929-110">To learn more about this set up process, go [here.](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures)</span></span>


## <a name="turn-on-recommendations"></a><span data-ttu-id="1b929-111">Aktivere anbefalinger</span><span class="sxs-lookup"><span data-stu-id="1b929-111">Turn on recommendations</span></span>

<span data-ttu-id="1b929-112">Benyt følgende fremgangsmåde for at aktivere produktanbefalinger.</span><span class="sxs-lookup"><span data-stu-id="1b929-112">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="1b929-113">Gå til **Retail og Commerce &gt; Produktanbefalinger &gt; Anbefalingsparametre**.</span><span class="sxs-lookup"><span data-stu-id="1b929-113">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation parameters**.</span></span>
1. <span data-ttu-id="1b929-114">Vælg **Anbefalingslister** på listen over delte parametre.</span><span class="sxs-lookup"><span data-stu-id="1b929-114">In the list of shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="1b929-115">Vælg **Ja** i indstillingen **Aktivér anbefalinger**.</span><span class="sxs-lookup"><span data-stu-id="1b929-115">Set the **Enable recommendations** option to **Yes**.</span></span>

![Aktivere produktanbefalinger](./media/enableproductrecommendations.png)

> [!NOTE]
> <span data-ttu-id="1b929-117">Denne procedure starter processen til oprettelse af produktanbefalingslister.</span><span class="sxs-lookup"><span data-stu-id="1b929-117">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="1b929-118">Der kan være op til flere timer, før listerne er tilgængelige og kan ses på POS eller i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1b929-118">Up to several hours might be required before the lists are available and can be seen at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="1b929-119">Konfigurere parametre for anbefalingslister</span><span class="sxs-lookup"><span data-stu-id="1b929-119">Configure recommendation list parameters</span></span>

<span data-ttu-id="1b929-120">Den AI-ML-baserede produktanbefalingsliste angiver som standard foreslåede værdier.</span><span class="sxs-lookup"><span data-stu-id="1b929-120">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="1b929-121">Du kan ændre de foreslåede standardværdier, så de passer til dit firmas flow.</span><span class="sxs-lookup"><span data-stu-id="1b929-121">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="1b929-122">Hvis du vil vide mere om, hvordan du ændrer standardparametrene, skal du gå til [Administrere resultater for AI-ML-baserede produktanbefalinger](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="1b929-122">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="1b929-123">Vise anbefalinger på POS-enheder</span><span class="sxs-lookup"><span data-stu-id="1b929-123">Show recommendations on POS devices</span></span>

<span data-ttu-id="1b929-124">Når anbefalingerne er aktiveret i Commerce-administrationen, skal anbefalingspanelet føjes til kontrolelementets POS-skærm ved hjælp af layoutværktøjet.</span><span class="sxs-lookup"><span data-stu-id="1b929-124">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="1b929-125">Du kan få mere at vide om denne proces i [Føje et kontrolelement med anbefalinger til posteringsskærmen på POS-enheder](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="1b929-125">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="1b929-126">Aktivere personlige anbefalinger</span><span class="sxs-lookup"><span data-stu-id="1b929-126">Enable personalized recommendations</span></span>

<span data-ttu-id="1b929-127">Yderligere oplysninger om, hvordan du modtager tilpassede anbefalinger, finder du i [Aktivere personlige anbefalinger](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="1b929-127">To learn more about how to receive personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1b929-128">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="1b929-128">Additional resources</span></span>

[<span data-ttu-id="1b929-129">Oversigt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="1b929-129">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="1b929-130">Aktivere ADLS i et Dynamics 365 Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="1b929-130">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="1b929-131">Aktivere tilpassede anbefalinger</span><span class="sxs-lookup"><span data-stu-id="1b929-131">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="1b929-132">Fravælge tilpassede anbefalinger</span><span class="sxs-lookup"><span data-stu-id="1b929-132">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="1b929-133">Føje lister med anbefalinger til et e-handelswebsted</span><span class="sxs-lookup"><span data-stu-id="1b929-133">Add recommendation lists to an e-Commerce site</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="1b929-134">Tilføje produktanbefalinger på POS</span><span class="sxs-lookup"><span data-stu-id="1b929-134">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="1b929-135">Føje anbefalinger til transaktionsskærmen</span><span class="sxs-lookup"><span data-stu-id="1b929-135">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="1b929-136">Justere resultater for AI-ML-anbefalinger</span><span class="sxs-lookup"><span data-stu-id="1b929-136">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="1b929-137">Oprette overvågede anbefalinger manuelt</span><span class="sxs-lookup"><span data-stu-id="1b929-137">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="1b929-138">Oprette anbefalinger med demonstrationsdata</span><span class="sxs-lookup"><span data-stu-id="1b929-138">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="1b929-139">Ofte stillede spørgsmål om produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="1b929-139">Product recommendations FAQ</span></span>](faq-recommendations.md)

