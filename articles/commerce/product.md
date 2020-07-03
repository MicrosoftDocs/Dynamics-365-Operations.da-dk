---
title: Tilføje produktanbefalinger på POS
description: Dette emne beskriver brugen af produktanbefalinger på en POS-enhed.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: fabf08e8dde1b9b6d27af3e42d3aaff904b467b0
ms.sourcegitcommit: ac47e8679fb104515f7dcca509294264bd05d2b1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/15/2020
ms.locfileid: "3454527"
---
# <a name="add-product-recommendations-on-pos"></a><span data-ttu-id="8ae53-103">Tilføje produktanbefalinger på POS</span><span class="sxs-lookup"><span data-stu-id="8ae53-103">Add product recommendations on POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8ae53-104">I sin kerne er produktanbefalinger et tværgående forretningsprogram, der dækker alle Commerce-områder for at skabe avancerede, spændende og skræddersyede oplevelser med produktregistrering.</span><span class="sxs-lookup"><span data-stu-id="8ae53-104">At its core, product recommendations are a transformative business application that span across all commerce spaces to create rich, engaging, and tailored product discovery experiences.</span></span> <span data-ttu-id="8ae53-105">Hvis du vil implementere denne funktion på POS, skal du følge trinnene under [Sådan tilføjer du anbefalinger på dine POS-enheder.](add-recommendations-control-pos-screen.md)</span><span class="sxs-lookup"><span data-stu-id="8ae53-105">To implement this feature on POS, follow the steps on [how to add recommendations to your POS devices.](add-recommendations-control-pos-screen.md)</span></span> 

<span data-ttu-id="8ae53-106">Yderligere oplysninger om funktioner for produktanbefalinger finder du under [Oversigt over produktanbefalinger.](../commerce/product-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="8ae53-106">For more information about product recommendations features, read the [product recommendations overview.](../commerce/product-recommendations.md)</span></span> 

## <a name="scenarios"></a><span data-ttu-id="8ae53-107">Scenarier</span><span class="sxs-lookup"><span data-stu-id="8ae53-107">Scenarios</span></span>

<span data-ttu-id="8ae53-108">Produktanbefalinger er aktiveret for følgende POS-scenarier.</span><span class="sxs-lookup"><span data-stu-id="8ae53-108">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="8ae53-109">De er tilgængelige i Cloud POS eller Modern POS (MPOS).</span><span class="sxs-lookup"><span data-stu-id="8ae53-109">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1. <span data-ttu-id="8ae53-110">På siden **Produktdetaljer**:</span><span class="sxs-lookup"><span data-stu-id="8ae53-110">On the **Product details** page:</span></span>

    - <span data-ttu-id="8ae53-111">Hvis en medarbejder går ind på siden **Produktdetaljer**, når vedkommende ser på tidligere transaktioner på tværs af forskellige kanaler, foreslår anbefalingstjenesten flere varer, det er sandsynligt at købe sammen.</span><span class="sxs-lookup"><span data-stu-id="8ae53-111">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendations service suggests additional items that are likely to be purchased together.</span></span>

    <span data-ttu-id="8ae53-112">[![Anbefalinger på siden Produktdetaljer](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="8ae53-112">[![Recommendations on the Product details page](./media/proddetails.png)](./media/proddetails.png)</span></span>

2. <span data-ttu-id="8ae53-113">På siden **Transaktion**:</span><span class="sxs-lookup"><span data-stu-id="8ae53-113">On the **Transaction** page:</span></span>

    - <span data-ttu-id="8ae53-114">Anbefalingsprogrammet foreslår varer baseret på hele listen med varer i kurven, der ofte købes sammen.</span><span class="sxs-lookup"><span data-stu-id="8ae53-114">The recommendation engine suggests items based on the entire list of items in the basket that are frequently bought together.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8ae53-115">For at få vist anbefalinger på siden **Transaktion** skal forhandleren opdatere skærmlayoutet i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8ae53-115">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 Commerce.</span></span> <span data-ttu-id="8ae53-116">Kontrolelementet **Anbefalinger** skal slippes på siden **Transaktion**.</span><span class="sxs-lookup"><span data-stu-id="8ae53-116">The **Recommendations** control must be dropped onto the **Transaction** page.</span></span>

    <span data-ttu-id="8ae53-117">[![Anbefalinger på siden Transaktion](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="8ae53-117">[![Recommendations on the Transaction page](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

## <a name="configure-commerce-to-enable-pos-recommendations"></a><span data-ttu-id="8ae53-118">Konfigurere Commerce til aktivering af POS-anbefalinger</span><span class="sxs-lookup"><span data-stu-id="8ae53-118">Configure Commerce to enable POS recommendations</span></span>

<span data-ttu-id="8ae53-119">Benyt følgende fremgangsmåde for at konfigurere produktanbefalinger:</span><span class="sxs-lookup"><span data-stu-id="8ae53-119">To set up product recommendations, follow these steps:</span></span>

1. <span data-ttu-id="8ae53-120">Kontrollér, at din tjeneste er blevet opdateret til **10.0.6-buildet.**</span><span class="sxs-lookup"><span data-stu-id="8ae53-120">Ensure your service has been updated to the **10.0.6 build.**</span></span>
2. <span data-ttu-id="8ae53-121">Følg instruktionerne i, hvordan du kan [aktivere produktanbefalinger](../commerce/enable-product-recommendations.md) for din virksomhed.</span><span class="sxs-lookup"><span data-stu-id="8ae53-121">Follow the instructions on how to [enable product recommendations](../commerce/enable-product-recommendations.md) for your business.</span></span>
3. <span data-ttu-id="8ae53-122">Valgfrit: For at få vist anbefalinger på skærmbilledet Transaktion, skal du gå til **Skærmlayout**, vælge dit skærmlayout, starte **skærmlayoutdesigneren** og derefter slippe kontrolelementet med **anbefalinger**, hvor der er behov for det.</span><span class="sxs-lookup"><span data-stu-id="8ae53-122">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**, and then drop the **recommendations** control where needed.</span></span>
4. <span data-ttu-id="8ae53-123">Gå til **Commerce-parametre**, vælg **Maskinel indlæring**, og vælg **Ja** under **Aktivér POS-anbefalinger**.</span><span class="sxs-lookup"><span data-stu-id="8ae53-123">Go to **Commerce parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5. <span data-ttu-id="8ae53-124">For at se anbefalinger på et POS skal du kører det globale konfigurationsjob **1110**.</span><span class="sxs-lookup"><span data-stu-id="8ae53-124">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="8ae53-125">For at afspejle ændringer i POS-skærmlayoutdesigneren skal du køre kanalkonfigurationsjobbet **1070**.</span><span class="sxs-lookup"><span data-stu-id="8ae53-125">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a><span data-ttu-id="8ae53-126">Foretage fejlfinding af problemer, hvor produktanbefalingerne allerede er aktiveret</span><span class="sxs-lookup"><span data-stu-id="8ae53-126">Troubleshoot issues where you have Product recommendations already enabled</span></span>

- <span data-ttu-id="8ae53-127">Gå til **Commerce-parametre** \> **Anbefalingslister** \> **Deaktiver produktanbefalinger**, og kør **Globalt konfigurationsjob \[9999\]**.</span><span class="sxs-lookup"><span data-stu-id="8ae53-127">Navigate to **Commerce Parameters** \> **Recommendation lists** \> **Disable product recommendations** and run **Global configuration job \[9999\]**.</span></span> 
- <span data-ttu-id="8ae53-128">Hvis du har føjet **Kontrolelement til anbefalinger** til din transaktionsskærm ved hjælp af **Designer for skærmlayout**, skal du også fjerne det.</span><span class="sxs-lookup"><span data-stu-id="8ae53-128">If you added the **Recommendations control** to your transaction screen using the **Screen layout designer**, please remove that as well.</span></span>
- <span data-ttu-id="8ae53-129">Hvis du har flere spørgsmål, kan du se [Ofte stillede spørgsmål om produktanbefalinger](../commerce/faq-recommendations.md) for at få yderligere oplysninger.</span><span class="sxs-lookup"><span data-stu-id="8ae53-129">If you have additional questions, check out the [Product recommendations FAQ](../commerce/faq-recommendations.md) for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8ae53-130">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="8ae53-130">Additional resources</span></span>

[<span data-ttu-id="8ae53-131">Oversigt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="8ae53-131">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="8ae53-132">Aktivér Azure Data Lake Storage i et Dynamics 365 Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="8ae53-132">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="8ae53-133">Aktivér produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="8ae53-133">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="8ae53-134">Aktivere tilpassede anbefalinger</span><span class="sxs-lookup"><span data-stu-id="8ae53-134">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="8ae53-135">Fravælge tilpassede anbefalinger</span><span class="sxs-lookup"><span data-stu-id="8ae53-135">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="8ae53-136">Føje anbefalinger til transaktionsskærmen</span><span class="sxs-lookup"><span data-stu-id="8ae53-136">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="8ae53-137">Justere resultater for AI-ML-anbefalinger</span><span class="sxs-lookup"><span data-stu-id="8ae53-137">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="8ae53-138">Oprette overvågede anbefalinger manuelt</span><span class="sxs-lookup"><span data-stu-id="8ae53-138">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="8ae53-139">Oprette anbefalinger med demonstrationsdata</span><span class="sxs-lookup"><span data-stu-id="8ae53-139">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="8ae53-140">Ofte stillede spørgsmål om produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="8ae53-140">Product recommendations FAQ</span></span>](faq-recommendations.md)
