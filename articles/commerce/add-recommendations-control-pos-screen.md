---
title: Føje anbefalinger til transaktionsskærmen
description: I dette emne beskrives, hvordan du føjer et kontrolelement med anbefalinger til transaktionsskærmbilledet på en POS-enhed (point of sale) ved hjælp af skærmlayoutdesigneren i Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 2e1ef6506833b35e61351600553a3bc29c20d5b2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980226"
---
# <a name="add-recommendations-to-the-transaction-screen"></a><span data-ttu-id="f7c84-103">Føje anbefalinger til transaktionsskærmen</span><span class="sxs-lookup"><span data-stu-id="f7c84-103">Add recommendations to the transaction screen</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="f7c84-104">I dette emne beskrives, hvordan du føjer et kontrolelement med anbefalinger til transaktionsskærmbilledet på en POS-enhed (point of sale) ved hjælp af skærmlayoutdesigneren i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f7c84-104">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="f7c84-105">Hvis du ønsker yderligere oplysninger om produktanbefalinger, kan du læse [produktanbefalingerne i POS-dokumentation](product.md).</span><span class="sxs-lookup"><span data-stu-id="f7c84-105">For more information about product recommendations, read the  [product recommendations on POS documentation](product.md).</span></span>


<span data-ttu-id="f7c84-106">Du kan få vist produktanbefalinger på POS-enheden, når du bruger Commerce.</span><span class="sxs-lookup"><span data-stu-id="f7c84-106">You can display product recommendations on your POS device when you use Commerce.</span></span> <span data-ttu-id="f7c84-107">For at få vist produktanbefalinger skal du føje et kontrolelement til transaktionsskærmen ved hjælp af skærmlayoutdesigneren.</span><span class="sxs-lookup"><span data-stu-id="f7c84-107">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span> 

## <a name="open-layout-designer"></a><span data-ttu-id="f7c84-108">Åbn layoutdesigner</span><span class="sxs-lookup"><span data-stu-id="f7c84-108">Open Layout designer</span></span>

1. <span data-ttu-id="f7c84-109">Gå til **Retail og Commerce** &gt; **Konfiguration af kanal** &gt; **POS-opsætning** &gt; **POS** &gt; **Skærmlayout**.</span><span class="sxs-lookup"><span data-stu-id="f7c84-109">Go to **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2. <span data-ttu-id="f7c84-110">Brug Quick Filter til at finde det skærmbillede, du vil føje kontrolelementet til.</span><span class="sxs-lookup"><span data-stu-id="f7c84-110">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="f7c84-111">Filtrer for eksempel på feltet **Skærmlayout-id** ved hjælp af værdien **F2CP16:9M**.</span><span class="sxs-lookup"><span data-stu-id="f7c84-111">For example, filter on the **Screen layout ID** field using a value of **F2CP16:9M**.</span></span>
3. <span data-ttu-id="f7c84-112">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="f7c84-112">In the list, find and select the desired record.</span></span> <span data-ttu-id="f7c84-113">Vælg for eksempel **Navn: F2CP16:9M skærmlayout-ID: F2CP16:9M**.</span><span class="sxs-lookup"><span data-stu-id="f7c84-113">For example, select **Name: F2CP16:9M Screen Layout ID: F2CP16:9M**.</span></span>
4. <span data-ttu-id="f7c84-114">Klik på **Layoutdesigner**.</span><span class="sxs-lookup"><span data-stu-id="f7c84-114">Click **Layout designer**.</span></span>
5. <span data-ttu-id="f7c84-115">Følg vejledningen for at starte layoutdesigneren.</span><span class="sxs-lookup"><span data-stu-id="f7c84-115">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="f7c84-116">Når du bliver bedt om legitimationsoplysninger, skal du angive de legitimationsoplysninger, der var i brug, da layoutdesigneren blev startet fra siden **Skærmlayout**.</span><span class="sxs-lookup"><span data-stu-id="f7c84-116">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6. <span data-ttu-id="f7c84-117">Når du logger på, vises en side, der ligner den nedenfor.</span><span class="sxs-lookup"><span data-stu-id="f7c84-117">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="f7c84-118">Layoutet er forskelligt, afhængigt af de tilpasninger, der er foretaget for din butik.</span><span class="sxs-lookup"><span data-stu-id="f7c84-118">The layout will be different depending on the customizations that were made for your store.</span></span>


    <span data-ttu-id="f7c84-119">[![Layoutdesigner](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span><span class="sxs-lookup"><span data-stu-id="f7c84-119">[![Layout designer](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span></span>

## <a name="choose-a-display-option"></a><span data-ttu-id="f7c84-120">Vælg en visningsindstilling</span><span class="sxs-lookup"><span data-stu-id="f7c84-120">Choose a display option</span></span>

<span data-ttu-id="f7c84-121">Der findes to konfigurationsindstillinger.</span><span class="sxs-lookup"><span data-stu-id="f7c84-121">There are two configurations options available.</span></span> <span data-ttu-id="f7c84-122">Vælg den indstilling, der passer bedst til din butik, og følg derefter vejledningen for at afslutte opsætningen af kontrolelementet.</span><span class="sxs-lookup"><span data-stu-id="f7c84-122">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="f7c84-123">Der er følgende to indstillinger:</span><span class="sxs-lookup"><span data-stu-id="f7c84-123">The two options are:</span></span>

- <span data-ttu-id="f7c84-124">Anbefalingerne er altid synlige.</span><span class="sxs-lookup"><span data-stu-id="f7c84-124">Recommendations are always visible.</span></span>
- <span data-ttu-id="f7c84-125">Fanen **Anbefalinger** vises i gitteret i højre side af skærmen.</span><span class="sxs-lookup"><span data-stu-id="f7c84-125">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

### <a name="make-recommendations-always-visible"></a><span data-ttu-id="f7c84-126">Gøre anbefalinger synlige permanent</span><span class="sxs-lookup"><span data-stu-id="f7c84-126">Make recommendations always visible</span></span>


1. <span data-ttu-id="f7c84-127">Reducer højden af området med detaljer for transaktionslinjer, så det har samme højde som kundepanelet til venstre.</span><span class="sxs-lookup"><span data-stu-id="f7c84-127">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.</span></span>


    <span data-ttu-id="f7c84-128">[![Højden på området med transaktionslinjedetaljer er reduceret](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="f7c84-128">[![Height of the transaction lines details area reduced](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>

2. <span data-ttu-id="f7c84-129">I menuen til venstre skal du trække og slippe kontrolelementet med anbefalinger til mellem området med transaktionslinjedetaljer og knapmatricen nederst i midten af transaktionsskærmbilledet.</span><span class="sxs-lookup"><span data-stu-id="f7c84-129">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="f7c84-130">Rediger størrelsen på kontrolelementet, så det passer i det pågældende område.</span><span class="sxs-lookup"><span data-stu-id="f7c84-130">Resize the control so it fits in that space.</span></span>

    <span data-ttu-id="f7c84-131">[![Kontrolelement til anbefalinger er føjet til layoutet](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="f7c84-131">[![Recommendations control added to the layout](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>


3. <span data-ttu-id="f7c84-132">Klik på **X** for at lukke og afslutte layoutdesigneren.</span><span class="sxs-lookup"><span data-stu-id="f7c84-132">Click the **X** to save and exit Layout designer.</span></span>
4. <span data-ttu-id="f7c84-133">I Commerce gå til **Retail og Commerce** &gt; **Retail og Commerce IT** &gt; **Distributionsplaner**.</span><span class="sxs-lookup"><span data-stu-id="f7c84-133">In Commerce, go to **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Distribution schedules**.</span></span>
5. <span data-ttu-id="f7c84-134">Vælg **1090, kasseapparater** på listen.</span><span class="sxs-lookup"><span data-stu-id="f7c84-134">In the list, select **1090 Registers**.</span></span>
6. <span data-ttu-id="f7c84-135">Klik på **Kør nu**.</span><span class="sxs-lookup"><span data-stu-id="f7c84-135">Click **Run now**.</span></span>


### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="f7c84-136">Tilføj fanen Anbefalinger i gitteret nederst i højre side af skærmen</span><span class="sxs-lookup"><span data-stu-id="f7c84-136">Add a Recommendations tab to the button grid on the right side of the screen</span></span>

1. <span data-ttu-id="f7c84-137">Højreklik på det tomme område under den sidste fane i knapmatricen i højre side af siden.</span><span class="sxs-lookup"><span data-stu-id="f7c84-137">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>

2. <span data-ttu-id="f7c84-138">Klik på **Tilpas**.</span><span class="sxs-lookup"><span data-stu-id="f7c84-138">Click **Customize**.</span></span>

    <span data-ttu-id="f7c84-139">[![Dialogboksen Tilpasning - fanekontrolelement](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="f7c84-139">[![Customization - Tab control dialog box](./media/pic-5.png)](./media/pic-5.png)</span></span>

3. <span data-ttu-id="f7c84-140">Klik på fanen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="f7c84-140">Click **New tab**.</span></span>
4. <span data-ttu-id="f7c84-141">Find den nye fane, du lige har tilføjet.</span><span class="sxs-lookup"><span data-stu-id="f7c84-141">Find the new tab that you just added.</span></span> <span data-ttu-id="f7c84-142">Du skal muligvis rulle ned.</span><span class="sxs-lookup"><span data-stu-id="f7c84-142">You may need to scroll down.</span></span>
5. <span data-ttu-id="f7c84-143">I rullemenuen **Indhold** skal du vælge **Anbefalede produkter**.</span><span class="sxs-lookup"><span data-stu-id="f7c84-143">In the **Contents** drop-down, select **Recommended products**.</span></span>

    <span data-ttu-id="f7c84-144">[![Vælge Anbefalede produkter i feltet Indhold](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="f7c84-144">[![Selecting Recommended products in the Contents field](./media/pic-6.png)](./media/pic-6.png)</span></span>

6. <span data-ttu-id="f7c84-145">I feltet **Etiket** skal du angive et navn til fanen Anbefalinger. Skriv f.eks. 'Anbefalede produkter'.</span><span class="sxs-lookup"><span data-stu-id="f7c84-145">In the **Label** field, type a name for the recommendations tab. For example, type 'Recommended products'.</span></span>
7. <span data-ttu-id="f7c84-146">Vælg det billede, der skal vises på fanen, i feltet **Billede**.</span><span class="sxs-lookup"><span data-stu-id="f7c84-146">In the **Image** field, select the image to appear on the tab.</span></span>
8. <span data-ttu-id="f7c84-147">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="f7c84-147">Click **OK**.</span></span> <span data-ttu-id="f7c84-148">Den nye fane vises i knapmatricen.</span><span class="sxs-lookup"><span data-stu-id="f7c84-148">The new tab appears in the button grid.</span></span>
9. <span data-ttu-id="f7c84-149">Klik på **X** for at lukke og afslutte layoutdesigneren.</span><span class="sxs-lookup"><span data-stu-id="f7c84-149">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="f7c84-150">I Commerce gå til **Retail og Commerce** &gt; **Retail og Commerce IT** &gt; **Distributionsplaner**.</span><span class="sxs-lookup"><span data-stu-id="f7c84-150">In Commerce, go to **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="f7c84-151">Vælg **1090, kasseapparater** på listen.</span><span class="sxs-lookup"><span data-stu-id="f7c84-151">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="f7c84-152">Klik på **Kør nu**.</span><span class="sxs-lookup"><span data-stu-id="f7c84-152">Click **Run now**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f7c84-153">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="f7c84-153">Additional resources</span></span>

[<span data-ttu-id="f7c84-154">Oversigt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="f7c84-154">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="f7c84-155">Aktivér Azure Data Lake Storage i et Dynamics 365 Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="f7c84-155">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="f7c84-156">Aktivér produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="f7c84-156">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="f7c84-157">Aktivere tilpassede anbefalinger</span><span class="sxs-lookup"><span data-stu-id="f7c84-157">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="f7c84-158">Fravælge tilpassede anbefalinger</span><span class="sxs-lookup"><span data-stu-id="f7c84-158">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="f7c84-159">Aktivere anbefalinger af "Køb tilsvarende"</span><span class="sxs-lookup"><span data-stu-id="f7c84-159">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="f7c84-160">Tilføje produktanbefalinger på POS</span><span class="sxs-lookup"><span data-stu-id="f7c84-160">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="f7c84-161">Justere resultater for AI-ML-anbefalinger</span><span class="sxs-lookup"><span data-stu-id="f7c84-161">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="f7c84-162">Oprette overvågede anbefalinger manuelt</span><span class="sxs-lookup"><span data-stu-id="f7c84-162">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="f7c84-163">Oprette anbefalinger med demonstrationsdata</span><span class="sxs-lookup"><span data-stu-id="f7c84-163">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="f7c84-164">Ofte stillede spørgsmål om produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="f7c84-164">Product recommendations FAQ</span></span>](faq-recommendations.md)
