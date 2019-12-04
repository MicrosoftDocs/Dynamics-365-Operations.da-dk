---
title: Føje et kontrolelement med anbefalinger til posteringsskærmen på POS-enheder
description: I dette emne beskrives, hvordan du tilføjer et kontrolelement med anbefalinger til transaktionsskærmbilledet på en POS-enhed (point of sale) ved hjælp af skærmlayoutdesigneren i Microsoft Dynamics 365 for Retail.
author: bebeale
manager: AnnBe
ms.date: 10/01/19
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: e6f0b75c8d81a5ac6ec90020375aec39120d4406
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811210"
---
# <a name="add-a-recommendations-control-to-the-transaction-screen-on-pos-devices"></a><span data-ttu-id="2c8ae-103">Føje et kontrolelement med anbefalinger til posteringsskærmen på POS-enheder</span><span class="sxs-lookup"><span data-stu-id="2c8ae-103">Add a recommendations control to the transaction screen on POS devices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="2c8ae-104">I dette emne beskrives, hvordan du føjer et kontrolelement med anbefalinger til transaktionsskærmbilledet på en POS-enhed (point of sale) ved hjælp af skærmlayoutdesigneren i Microsoft Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="2c8ae-104">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 Retail.</span></span> <span data-ttu-id="2c8ae-105">Hvis du ønsker yderligere oplysninger om produktanbefalinger, kan du læse [produktanbefalingerne i POS-dokumentation](product.md).</span><span class="sxs-lookup"><span data-stu-id="2c8ae-105">For more information about product recommendations, read the  [product recommendations on POS documentation](product.md).</span></span>


<span data-ttu-id="2c8ae-106">Du kan få vist produktanbefalinger på POS-enheden, når du bruger Microsoft Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="2c8ae-106">You can display product recommendations on your POS device when you use Microsoft Dynamics 365 Retail.</span></span> <span data-ttu-id="2c8ae-107">For at få vist produktanbefalinger skal du føje et kontrolelement til transaktionsskærmen ved hjælp af skærmlayoutdesigneren.</span><span class="sxs-lookup"><span data-stu-id="2c8ae-107">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span> 

## <a name="open-layout-designer"></a><span data-ttu-id="2c8ae-108">Åbn layoutdesigner</span><span class="sxs-lookup"><span data-stu-id="2c8ae-108">Open Layout designer</span></span>

1. <span data-ttu-id="2c8ae-109">Gå til **Retail** &gt; **Konfiguration af kanal** &gt; **POS-opsætning** &gt; **POS** &gt; **Skærmlayout**.</span><span class="sxs-lookup"><span data-stu-id="2c8ae-109">Go to **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2. <span data-ttu-id="2c8ae-110">Brug Quick Filter til at finde det skærmbillede, du vil føje kontrolelementet til.</span><span class="sxs-lookup"><span data-stu-id="2c8ae-110">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="2c8ae-111">Filtrer for eksempel på feltet **Skærmlayout-id** ved hjælp af værdien **F2CP16:9M**.</span><span class="sxs-lookup"><span data-stu-id="2c8ae-111">For example, filter on the **Screen layout ID** field using a value of **F2CP16:9M**.</span></span>
3. <span data-ttu-id="2c8ae-112">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="2c8ae-112">In the list, find and select the desired record.</span></span> <span data-ttu-id="2c8ae-113">Vælg for eksempel **Navn: F2CP16:9M skærmlayout-ID: F2CP16:9M**.</span><span class="sxs-lookup"><span data-stu-id="2c8ae-113">For example, select **Name: F2CP16:9M Screen Layout ID: F2CP16:9M**.</span></span>
4. <span data-ttu-id="2c8ae-114">Klik på **Layoutdesigner**.</span><span class="sxs-lookup"><span data-stu-id="2c8ae-114">Click **Layout designer**.</span></span>
5. <span data-ttu-id="2c8ae-115">Følg vejledningen for at starte layoutdesigneren.</span><span class="sxs-lookup"><span data-stu-id="2c8ae-115">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="2c8ae-116">Når du bliver bedt om legitimationsoplysninger, skal du angive de legitimationsoplysninger, der var i brug, da layoutdesigneren blev startet fra siden **Skærmlayout**.</span><span class="sxs-lookup"><span data-stu-id="2c8ae-116">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6. <span data-ttu-id="2c8ae-117">Når du logger på, vises en side, der ligner den nedenfor.</span><span class="sxs-lookup"><span data-stu-id="2c8ae-117">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="2c8ae-118">Layoutet er forskelligt, afhængigt af de tilpasninger, der er foretaget for din butik.</span><span class="sxs-lookup"><span data-stu-id="2c8ae-118">The layout will be different depending on the customizations that were made for your store.</span></span>


    <span data-ttu-id="2c8ae-119">[![Layoutdesigner](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span><span class="sxs-lookup"><span data-stu-id="2c8ae-119">[![Layout designer](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span></span>

## <a name="choose-a-display-option"></a><span data-ttu-id="2c8ae-120">Vælg en visningsindstilling</span><span class="sxs-lookup"><span data-stu-id="2c8ae-120">Choose a display option</span></span>

<span data-ttu-id="2c8ae-121">Der findes to konfigurationsindstillinger.</span><span class="sxs-lookup"><span data-stu-id="2c8ae-121">There are two configurations options available.</span></span> <span data-ttu-id="2c8ae-122">Vælg den indstilling, der passer bedst til din butik, og følg derefter vejledningen for at afslutte opsætningen af kontrolelementet.</span><span class="sxs-lookup"><span data-stu-id="2c8ae-122">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="2c8ae-123">Der er følgende to indstillinger:</span><span class="sxs-lookup"><span data-stu-id="2c8ae-123">The two options are:</span></span>

- <span data-ttu-id="2c8ae-124">Anbefalingerne er altid synlige.</span><span class="sxs-lookup"><span data-stu-id="2c8ae-124">Recommendations are always visible.</span></span>
- <span data-ttu-id="2c8ae-125">Fanen **Anbefalinger** vises i gitteret i højre side af skærmen.</span><span class="sxs-lookup"><span data-stu-id="2c8ae-125">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

### <a name="make-recommendations-always-visible"></a><span data-ttu-id="2c8ae-126">Gøre anbefalinger synlige permanent</span><span class="sxs-lookup"><span data-stu-id="2c8ae-126">Make recommendations always visible</span></span>


1. <span data-ttu-id="2c8ae-127">Reducer højden af området med detaljer for transaktionslinjer, så det har samme højde som kundepanelet til venstre.</span><span class="sxs-lookup"><span data-stu-id="2c8ae-127">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.</span></span>


    <span data-ttu-id="2c8ae-128">[![Højden på området med transaktionslinjedetaljer er reduceret](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="2c8ae-128">[![Height of the transaction lines details area reduced](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>

2. <span data-ttu-id="2c8ae-129">I menuen til venstre skal du trække og slippe kontrolelementet med anbefalinger til mellem området med transaktionslinjedetaljer og knapmatricen nederst i midten af transaktionsskærmbilledet.</span><span class="sxs-lookup"><span data-stu-id="2c8ae-129">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="2c8ae-130">Rediger størrelsen på kontrolelementet, så det passer i det pågældende område.</span><span class="sxs-lookup"><span data-stu-id="2c8ae-130">Resize the control so it fits in that space.</span></span>

    <span data-ttu-id="2c8ae-131">[![Kontrolelement til anbefalinger er føjet til layoutet](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="2c8ae-131">[![Recommendations control added to the layout](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>


3. <span data-ttu-id="2c8ae-132">Klik på **X** for at lukke og afslutte layoutdesigneren.</span><span class="sxs-lookup"><span data-stu-id="2c8ae-132">Click the **X** to save and exit Layout designer.</span></span>
4. <span data-ttu-id="2c8ae-133">I Dynamics 365 for Retail skal du gå til **Detail** &gt; **Detail-it** &gt; **Distributionsplaner**.</span><span class="sxs-lookup"><span data-stu-id="2c8ae-133">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
5. <span data-ttu-id="2c8ae-134">Vælg **1090, kasseapparater** på listen.</span><span class="sxs-lookup"><span data-stu-id="2c8ae-134">In the list, select **1090 Registers**.</span></span>
6. <span data-ttu-id="2c8ae-135">Klik på **Kør nu**.</span><span class="sxs-lookup"><span data-stu-id="2c8ae-135">Click **Run now**.</span></span>


### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="2c8ae-136">Tilføj fanen Anbefalinger i gitteret nederst i højre side af skærmen</span><span class="sxs-lookup"><span data-stu-id="2c8ae-136">Add a Recommendations tab to the button grid on the right side of the screen</span></span>

1. <span data-ttu-id="2c8ae-137">Højreklik på det tomme område under den sidste fane i knapmatricen i højre side af siden.</span><span class="sxs-lookup"><span data-stu-id="2c8ae-137">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>

2. <span data-ttu-id="2c8ae-138">Klik på **Tilpas**.</span><span class="sxs-lookup"><span data-stu-id="2c8ae-138">Click **Customize**.</span></span>

    <span data-ttu-id="2c8ae-139">[![Dialogboksen Tilpasning - fanekontrolelement](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="2c8ae-139">[![Customization - Tab control dialog box](./media/pic-5.png)](./media/pic-5.png)</span></span>

3. <span data-ttu-id="2c8ae-140">Klik på fanen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="2c8ae-140">Click **New tab**.</span></span>
4. <span data-ttu-id="2c8ae-141">Find den nye fane, du lige har tilføjet.</span><span class="sxs-lookup"><span data-stu-id="2c8ae-141">Find the new tab that you just added.</span></span> <span data-ttu-id="2c8ae-142">Du skal muligvis rulle ned.</span><span class="sxs-lookup"><span data-stu-id="2c8ae-142">You may need to scroll down.</span></span>
5. <span data-ttu-id="2c8ae-143">I rullemenuen **Indhold** skal du vælge **Anbefalede produkter**.</span><span class="sxs-lookup"><span data-stu-id="2c8ae-143">In the **Contents** drop-down, select **Recommended products**.</span></span>

    <span data-ttu-id="2c8ae-144">[![Vælge Anbefalede produkter i feltet Indhold](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="2c8ae-144">[![Selecting Recommended products in the Contents field](./media/pic-6.png)](./media/pic-6.png)</span></span>

6. <span data-ttu-id="2c8ae-145">I feltet **Etiket** skal du angive et navn til fanen Anbefalinger. Skriv f.eks. 'Anbefalede produkter'.</span><span class="sxs-lookup"><span data-stu-id="2c8ae-145">In the **Label** field, type a name for the recommendations tab. For example, type 'Recommended products'.</span></span>
7. <span data-ttu-id="2c8ae-146">Vælg det billede, der skal vises på fanen, i feltet **Billede**.</span><span class="sxs-lookup"><span data-stu-id="2c8ae-146">In the **Image** field, select the image to appear on the tab.</span></span>
8. <span data-ttu-id="2c8ae-147">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="2c8ae-147">Click **OK**.</span></span> <span data-ttu-id="2c8ae-148">Den nye fane vises i knapmatricen.</span><span class="sxs-lookup"><span data-stu-id="2c8ae-148">The new tab appears in the button grid.</span></span>
9. <span data-ttu-id="2c8ae-149">Klik på **X** for at lukke og afslutte layoutdesigneren.</span><span class="sxs-lookup"><span data-stu-id="2c8ae-149">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="2c8ae-150">I Dynamics 365 for Retail skal du gå til **Detail** &gt; **Detail-it** &gt; **Distributionsplaner**.</span><span class="sxs-lookup"><span data-stu-id="2c8ae-150">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="2c8ae-151">Vælg **1090, kasseapparater** på listen.</span><span class="sxs-lookup"><span data-stu-id="2c8ae-151">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="2c8ae-152">Klik på **Kør nu**.</span><span class="sxs-lookup"><span data-stu-id="2c8ae-152">Click **Run now**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2c8ae-153">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="2c8ae-153">Additional resources</span></span>

[<span data-ttu-id="2c8ae-154">Produktanbefalinger på POS</span><span class="sxs-lookup"><span data-stu-id="2c8ae-154">Product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="2c8ae-155">Oversigt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="2c8ae-155">Product recommendations overview</span></span>](../commerce/product-recommendations.md)
