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
ms.openlocfilehash: ecda571a356c6968196d09cc19923105cf4544ab
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770133"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="a299a-103">Aktivér produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="a299a-103">Enable product recommendations</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="a299a-104">I dette emne beskrives, hvordan du kan lave produktanbefalinger, der er baseret på kunstig intelligens-maskinel læring (AI-ML), som er tilgængelig for Microsoft Dynamics 365 Commerce-kunder.</span><span class="sxs-lookup"><span data-stu-id="a299a-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="a299a-105">Yderligere oplysninger om lister over produktanbefalinger finder du under [Oversigt over produktanbefalinger](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="a299a-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="a299a-106">Forhåndscheck af anbefalinger</span><span class="sxs-lookup"><span data-stu-id="a299a-106">Recommendations pre-check</span></span>
<span data-ttu-id="a299a-107">Før du aktiverer anbefalinger, skal du vide, at produktanbefalingerne kun understøttes for Finance and Operations-kunder med 10.0.6, og som har overført deres lager for at bruge BDL.</span><span class="sxs-lookup"><span data-stu-id="a299a-107">Before enabling, please note that product recommendations are only supported for F&O customers supporting build 10.0.6 and have migrated their storage to using BDL.</span></span> 

<span data-ttu-id="a299a-108">Derudover skal du kontrollere, at RetailSale-målinger er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="a299a-108">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="a299a-109">Du kan få mere at vide om denne opsætningsproces [her.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span><span class="sxs-lookup"><span data-stu-id="a299a-109">To Learn more about this set up process, go [here.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span></span>


## <a name="turn-on-recommendations"></a><span data-ttu-id="a299a-110">Aktivere anbefalinger</span><span class="sxs-lookup"><span data-stu-id="a299a-110">Turn on recommendations</span></span>

<span data-ttu-id="a299a-111">Benyt følgende fremgangsmåde for at aktivere produktanbefalinger.</span><span class="sxs-lookup"><span data-stu-id="a299a-111">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="a299a-112">Gå til **Detail** &gt; **Produktanbefalinger** &gt; **Anbefalingsparametre**.</span><span class="sxs-lookup"><span data-stu-id="a299a-112">Go to **Retail** &gt; **Product recommendations** &gt; **Recommendation parameters**.</span></span>
1. <span data-ttu-id="a299a-113">Vælg **Anbefalingslister** på listen over delte detailparametre.</span><span class="sxs-lookup"><span data-stu-id="a299a-113">In the list of retail shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="a299a-114">Vælg **Ja** i indstillingen **Aktivér anbefalinger**.</span><span class="sxs-lookup"><span data-stu-id="a299a-114">Set the **Enable recommendations** option to **Yes**.</span></span>

![Aktivere produktanbefalinger](./media/enableproductrecommendations.png)

> [!NOTE]
> <span data-ttu-id="a299a-116">Denne procedure starter processen til oprettelse af produktanbefalingslister.</span><span class="sxs-lookup"><span data-stu-id="a299a-116">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="a299a-117">Der kan være op til flere timer, før listerne er tilgængelige og kan ses på POS eller i Dynamics 365 for Commerce.</span><span class="sxs-lookup"><span data-stu-id="a299a-117">Up to several hours might be required before the lists are available and can be seen at the point of sale (POS) or in Dynamics 365 for Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="a299a-118">Konfigurere parametre for anbefalingslister</span><span class="sxs-lookup"><span data-stu-id="a299a-118">Configure recommendation list parameters</span></span>
<span data-ttu-id="a299a-119">Den AI-ML-baserede produktanbefalingsliste angiver som standard foreslåede værdier.</span><span class="sxs-lookup"><span data-stu-id="a299a-119">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="a299a-120">Du kan ændre de foreslåede standardværdier, så de passer til dit firmas flow.</span><span class="sxs-lookup"><span data-stu-id="a299a-120">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="a299a-121">Hvis du vil vide mere om, hvordan du ændrer standardparametrene, skal du gå til [Administrere resultater for AI-ML-baserede produktanbefalinger](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="a299a-121">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="a299a-122">Vise anbefalinger på POS-enheder</span><span class="sxs-lookup"><span data-stu-id="a299a-122">Show recommendations on POS devices</span></span>
<span data-ttu-id="a299a-123">Når anbefalingerne er aktiveret i bagkontoret, skal anbefalingspanelet føjes til kontrolpanelet kontrolelementets POS-skærm via layoutværktøjet.</span><span class="sxs-lookup"><span data-stu-id="a299a-123">After enabling recommendations in the back office, the recommendations pannel must be added to the control POS screen via the layout tool.</span></span> <span data-ttu-id="a299a-124">Du kan få mere at vide om denne proces [her.](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)</span><span class="sxs-lookup"><span data-stu-id="a299a-124">To learn about this process, go [here.](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)</span></span>


## <a name="additional-resources"></a><span data-ttu-id="a299a-125">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="a299a-125">Additional resources</span></span>

[<span data-ttu-id="a299a-126">Oversigt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="a299a-126">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="a299a-127">Tilføje lister med produktanbefalinger på sider</span><span class="sxs-lookup"><span data-stu-id="a299a-127">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="a299a-128">Føje anbefalingspanel til POS-enheder</span><span class="sxs-lookup"><span data-stu-id="a299a-128">Add recommendations panel to POS devices</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)


