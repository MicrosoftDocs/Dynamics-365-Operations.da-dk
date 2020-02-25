---
title: Aktivér produktanbefalinger
description: I dette emne beskrives, hvordan du kan lave produktanbefalinger, der er baseret på kunstig intelligens-maskinel læring (AI-ML), som er tilgængelig for Microsoft Dynamics 365 Commerce-kunder.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
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
ms.openlocfilehash: 2d3f1bc2526eeacb4bd6338a0679eadd95a75989
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024950"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="fe974-103">Aktivér produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="fe974-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fe974-104">I dette emne beskrives, hvordan du kan lave produktanbefalinger, der er baseret på kunstig intelligens-maskinel læring (AI-ML), som er tilgængelig for Microsoft Dynamics 365 Commerce-kunder.</span><span class="sxs-lookup"><span data-stu-id="fe974-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="fe974-105">Yderligere oplysninger om lister over produktanbefalinger finder du under [Oversigt over produktanbefalinger](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="fe974-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="fe974-106">Forhåndscheck af anbefalinger</span><span class="sxs-lookup"><span data-stu-id="fe974-106">Recommendations pre-check</span></span>

<span data-ttu-id="fe974-107">Før du aktiverer anbefalinger, skal du vide, at produktanbefalingerne kun understøttes for Commerce-kunder, som har overført deres lager for at bruge Azure Data Lake Storage (ADLS).</span><span class="sxs-lookup"><span data-stu-id="fe974-107">Before enabling, please note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage (ADLS).</span></span> 

<span data-ttu-id="fe974-108">Du kan se trinnene til at aktivere i [Sådan aktiveres ADLS i et Dynamics 365-miljø](enable-ADLS-environment.md).</span><span class="sxs-lookup"><span data-stu-id="fe974-108">For steps on enabling ADLS, see [How to enable ADLS in a Dynamics 365 environment](enable-ADLS-environment.md).</span></span>

<span data-ttu-id="fe974-109">Derudover skal du kontrollere, at RetailSale-målinger er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="fe974-109">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="fe974-110">Du kan få mere at vide om denne opsætningsproces [her.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span><span class="sxs-lookup"><span data-stu-id="fe974-110">To learn more about this set up process, go [here.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span></span>


## <a name="turn-on-recommendations"></a><span data-ttu-id="fe974-111">Aktivere anbefalinger</span><span class="sxs-lookup"><span data-stu-id="fe974-111">Turn on recommendations</span></span>

<span data-ttu-id="fe974-112">Benyt følgende fremgangsmåde for at aktivere produktanbefalinger.</span><span class="sxs-lookup"><span data-stu-id="fe974-112">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="fe974-113">Gå til **Retail og Commerce &gt; Produktanbefalinger &gt; Anbefalingsparametre**.</span><span class="sxs-lookup"><span data-stu-id="fe974-113">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation parameters**.</span></span>
1. <span data-ttu-id="fe974-114">Vælg **Anbefalingslister** på listen over delte parametre.</span><span class="sxs-lookup"><span data-stu-id="fe974-114">In the list of shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="fe974-115">Vælg **Ja** i indstillingen **Aktivér anbefalinger**.</span><span class="sxs-lookup"><span data-stu-id="fe974-115">Set the **Enable recommendations** option to **Yes**.</span></span>

![Aktivere produktanbefalinger](./media/enableproductrecommendations.png)

> [!NOTE]
> <span data-ttu-id="fe974-117">Denne procedure starter processen til oprettelse af produktanbefalingslister.</span><span class="sxs-lookup"><span data-stu-id="fe974-117">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="fe974-118">Der kan være op til flere timer, før listerne er tilgængelige og kan ses på POS eller i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fe974-118">Up to several hours might be required before the lists are available and can be seen at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="fe974-119">Konfigurere parametre for anbefalingslister</span><span class="sxs-lookup"><span data-stu-id="fe974-119">Configure recommendation list parameters</span></span>

<span data-ttu-id="fe974-120">Den AI-ML-baserede produktanbefalingsliste angiver som standard foreslåede værdier.</span><span class="sxs-lookup"><span data-stu-id="fe974-120">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="fe974-121">Du kan ændre de foreslåede standardværdier, så de passer til dit firmas flow.</span><span class="sxs-lookup"><span data-stu-id="fe974-121">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="fe974-122">Hvis du vil vide mere om, hvordan du ændrer standardparametrene, skal du gå til [Administrere resultater for AI-ML-baserede produktanbefalinger](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="fe974-122">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="fe974-123">Vise anbefalinger på POS-enheder</span><span class="sxs-lookup"><span data-stu-id="fe974-123">Show recommendations on POS devices</span></span>

<span data-ttu-id="fe974-124">Når anbefalingerne er aktiveret i Commerce-administrationen, skal anbefalingspanelet føjes til kontrolelementets POS-skærm ved hjælp af layoutværktøjet.</span><span class="sxs-lookup"><span data-stu-id="fe974-124">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="fe974-125">Du kan få mere at vide om denne proces i [Føje et kontrolelement med anbefalinger til posteringsskærmen på POS-enheder](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="fe974-125">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="fe974-126">Aktivere personlige anbefalinger</span><span class="sxs-lookup"><span data-stu-id="fe974-126">Enable personalized recommendations</span></span>

<span data-ttu-id="fe974-127">Yderligere oplysninger om, hvordan du modtager tilpassede anbefalinger, finder du i [Aktivere personlige anbefalinger](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="fe974-127">To learn more about how to receive personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fe974-128">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="fe974-128">Additional resources</span></span>

[<span data-ttu-id="fe974-129">Oversigt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="fe974-129">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="fe974-130">Aktivere personlige anbefalinger</span><span class="sxs-lookup"><span data-stu-id="fe974-130">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="fe974-131">Tilføje lister med produktanbefalinger på sider</span><span class="sxs-lookup"><span data-stu-id="fe974-131">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="fe974-132">Føje anbefalingspanel til POS-enheder</span><span class="sxs-lookup"><span data-stu-id="fe974-132">Add recommendations panel to POS devices</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="fe974-133">Oversigt over modulet Produktsamling</span><span class="sxs-lookup"><span data-stu-id="fe974-133">Product collection module overview</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="fe974-134">Aktivere ADLS i Dynamics 365-miljøet</span><span class="sxs-lookup"><span data-stu-id="fe974-134">Enable ADLS in Dynamics 365 environment</span></span>](enable-ADLS-environment.md)

