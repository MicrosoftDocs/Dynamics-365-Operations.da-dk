---
title: "Føje et kontrolelement med anbefalinger til transaktionssiden på en POS-enhed"
description: "I dette emne beskrives, hvordan du tilføjer et kontrolelement med anbefalinger til transaktionsskærmbilledet på en POS-enhed (point of sale) ved hjælp af skærmlayoutdesigneren i Microsoft Dynamics 365 for Retail."
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Operations, Core, UnifiedOperations
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4cdfcbdcafdbbbab21c398ebc8002a45742e33e6
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="add-a-recommendations-control-to-the-transaction-page-on-a-pos-device"></a><span data-ttu-id="f448a-103">Føje et kontrolelement med anbefalinger til transaktionssiden på en POS-enhed</span><span class="sxs-lookup"><span data-stu-id="f448a-103">Add a recommendations control to the transaction page on a POS device</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="f448a-104">I dette emne beskrives, hvordan du tilføjer et kontrolelement med anbefalinger til transaktionsskærmbilledet på en POS-enhed (point of sale) ved hjælp af skærmlayoutdesigneren i Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="f448a-104">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="f448a-105">Du kan få vist produktanbefalinger på POS-enheden, når du bruger Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="f448a-105">You can display product recommendations on your POS device when you use Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="f448a-106">*Anbefalinger* er varer, som kunden muligvis er interesseret i baseret på deres købshistorik, varer i deres ønskeseddel og varer, som andre kunder har købt online og i fysiske butikker.</span><span class="sxs-lookup"><span data-stu-id="f448a-106">*Recommendations* are items that your customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="f448a-107">For at få vist produktanbefalinger skal du føje et kontrolelement til transaktionsskærmen ved hjælp af skærmlayoutdesigneren.</span><span class="sxs-lookup"><span data-stu-id="f448a-107">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span>

## <a name="open-layout-designer"></a><span data-ttu-id="f448a-108">Åbn layoutdesigner</span><span class="sxs-lookup"><span data-stu-id="f448a-108">Open Layout designer</span></span>
1.  <span data-ttu-id="f448a-109">Gå til **Retail** &gt; **Konfiguration af kanal** &gt; **POS-opsætning** &gt; **POS** &gt; **Skærmlayout**.</span><span class="sxs-lookup"><span data-stu-id="f448a-109">Go to **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2.  <span data-ttu-id="f448a-110">Brug Quick Filter til at finde det skærmbillede, du vil føje kontrolelementet til.</span><span class="sxs-lookup"><span data-stu-id="f448a-110">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="f448a-111">Filtrer for eksempel på feltet **Skærmlayout-id** ved hjælp af værdien 'F2CP16:9M'.</span><span class="sxs-lookup"><span data-stu-id="f448a-111">For example, filter on the **Screen layout ID** field using a value of ‘F2CP16:9M’.</span></span>
3.  <span data-ttu-id="f448a-112">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="f448a-112">In the list, find and select the desired record.</span></span> <span data-ttu-id="f448a-113">Vælg for eksempel 'Navn: F2CP16:9M skærmlayout-ID: F2CP16:9M'.</span><span class="sxs-lookup"><span data-stu-id="f448a-113">For example, select ‘Name: F2CP16:9M Screen Layout ID: F2CP16:9M’.</span></span>
4.  <span data-ttu-id="f448a-114">Klik på **Layoutdesigner**.</span><span class="sxs-lookup"><span data-stu-id="f448a-114">Click **Layout designer**.</span></span>
5.  <span data-ttu-id="f448a-115">Følg vejledningen for at starte layoutdesigneren.</span><span class="sxs-lookup"><span data-stu-id="f448a-115">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="f448a-116">Når du bliver bedt om legitimationsoplysninger, skal du angive de legitimationsoplysninger, der var i brug, da layoutdesigneren blev startet fra **Skærmlayout** siden.</span><span class="sxs-lookup"><span data-stu-id="f448a-116">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6.  <span data-ttu-id="f448a-117">Når du logger på, vises en side, der ligner den nedenfor.</span><span class="sxs-lookup"><span data-stu-id="f448a-117">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="f448a-118">Layoutet er forskelligt, afhængigt af de tilpasninger, der er foretaget for din butik.</span><span class="sxs-lookup"><span data-stu-id="f448a-118">The layout will be different depending on the customizations that were made for your store.</span></span>

<span data-ttu-id="f448a-119">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Vælg en visningsindstilling</span><span class="sxs-lookup"><span data-stu-id="f448a-119">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Choose a display option</span></span>
-----------------------

<span data-ttu-id="f448a-120">Der findes to konfigurationsindstillinger.</span><span class="sxs-lookup"><span data-stu-id="f448a-120">There are two configurations options available.</span></span> <span data-ttu-id="f448a-121">Vælg den indstilling, der passer bedst til din butik, og følg derefter vejledningen for at afslutte opsætningen af kontrolelementet.</span><span class="sxs-lookup"><span data-stu-id="f448a-121">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="f448a-122">Der er følgende to indstillinger:</span><span class="sxs-lookup"><span data-stu-id="f448a-122">The two options are:</span></span>
-   <span data-ttu-id="f448a-123">Anbefalingerne er altid synlige.</span><span class="sxs-lookup"><span data-stu-id="f448a-123">Recommendations are always visible.</span></span>
-   <span data-ttu-id="f448a-124">Fanen **Anbefalinger** vises i gitteret på højre side af skærmen.</span><span class="sxs-lookup"><span data-stu-id="f448a-124">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

#### <a name="to-make-recommendations-always-visible"></a><span data-ttu-id="f448a-125">Sådan gøres anbefalinger synlige altid</span><span class="sxs-lookup"><span data-stu-id="f448a-125">To make recommendations always visible</span></span>

1.  <span data-ttu-id="f448a-126">Reducer højden af området med detaljer for transaktionslinjer, så det har samme højde som kundepanelet til venstre.[](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="f448a-126">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.[](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>
2.  <span data-ttu-id="f448a-127">I menuen til venstre skal du trække og slippe kontrolelementet med anbefalinger til mellem området med transaktionslinjedetaljer og knapmatricen nederst i midten af transaktionsskærmbilledet.</span><span class="sxs-lookup"><span data-stu-id="f448a-127">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="f448a-128">Rediger størrelsen på kontrolelementet, så det passer i det pågældende område.[](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="f448a-128">Resize the control so it fits in that space.[](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>
3.  <span data-ttu-id="f448a-129">Klik på **X** for at lukke og afslutte layoutdesigneren.</span><span class="sxs-lookup"><span data-stu-id="f448a-129">Click the **X** to save and exit Layout designer.</span></span>
4.  <span data-ttu-id="f448a-130">I Dynamics 365 for Retail skal du gå til **Retail** &gt; **Retail it** &gt; **Distributionsplaner**.</span><span class="sxs-lookup"><span data-stu-id="f448a-130">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
5.  <span data-ttu-id="f448a-131">Vælg **1090, kasseapparater** på listen.</span><span class="sxs-lookup"><span data-stu-id="f448a-131">In the list, select **1090 Registers**.</span></span>
6.  <span data-ttu-id="f448a-132">Klik på **Kør nu**.</span><span class="sxs-lookup"><span data-stu-id="f448a-132">Click **Run now**.</span></span>

#### <a name="to-add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="f448a-133">Sådan tilføjes fanen Anbefalinger i gitteret nederst i højre side af skærmen</span><span class="sxs-lookup"><span data-stu-id="f448a-133">To add a Recommendations tab to the button grid on the right side of the screen</span></span>

1.  <span data-ttu-id="f448a-134">Højreklik på det tomme område under den sidste fane i knapmatricen i højre side af siden.</span><span class="sxs-lookup"><span data-stu-id="f448a-134">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>
2.  <span data-ttu-id="f448a-135">Klik på **Tilpas**.[![pic-5](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="f448a-135">Click **Customize**.[![pic-5](./media/pic-5.png)](./media/pic-5.png)</span></span>
3.  <span data-ttu-id="f448a-136">Klik på fanen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="f448a-136">Click **New tab**.</span></span>
4.  <span data-ttu-id="f448a-137">Find den nye fane, du lige har tilføjet.</span><span class="sxs-lookup"><span data-stu-id="f448a-137">Find the new tab that you just added.</span></span> <span data-ttu-id="f448a-138">Du skal muligvis rulle ned.</span><span class="sxs-lookup"><span data-stu-id="f448a-138">You may need to scroll down.</span></span>
5.  <span data-ttu-id="f448a-139">I rullemenuen **Indhold** skal du vælge **Anbefalede produkter**.</span><span class="sxs-lookup"><span data-stu-id="f448a-139">In the **Contents** drop-down, select **Recommended products**.</span></span> <span data-ttu-id="f448a-140">[![PIC-6](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="f448a-140">[![pic-6](./media/pic-6.png)](./media/pic-6.png)</span></span>
6.  <span data-ttu-id="f448a-141">I feltet **Etiket** skal du angive et navn til fanen Anbefalinger. Skriv f.eks. 'Anbefalede produkter'.</span><span class="sxs-lookup"><span data-stu-id="f448a-141">In the **Label** field, type a name for the recommendations tab. For example, type ‘Recommended products’.</span></span>
7.  <span data-ttu-id="f448a-142">Vælg det billede, der skal vises på fanen, i feltet **Billede**.</span><span class="sxs-lookup"><span data-stu-id="f448a-142">In the **Image** field, select the image to appear on the tab.</span></span>
8.  <span data-ttu-id="f448a-143">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="f448a-143">Click **OK**.</span></span> <span data-ttu-id="f448a-144">Den nye fane vises i knapmatricen.</span><span class="sxs-lookup"><span data-stu-id="f448a-144">The new tab appears in the button grid.</span></span>
9.  <span data-ttu-id="f448a-145">Klik på **X** for at lukke og afslutte layoutdesigneren.</span><span class="sxs-lookup"><span data-stu-id="f448a-145">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="f448a-146">I Dynamics 365 for Retail skal du gå til **Retail** &gt; **Retail it** &gt; **Distributionsplaner**.</span><span class="sxs-lookup"><span data-stu-id="f448a-146">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="f448a-147">Vælg **1090, kasseapparater** på listen.</span><span class="sxs-lookup"><span data-stu-id="f448a-147">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="f448a-148">Klik på **Kør nu**.</span><span class="sxs-lookup"><span data-stu-id="f448a-148">Click **Run now**.</span></span>


<a name="see-also"></a><span data-ttu-id="f448a-149">Se også</span><span class="sxs-lookup"><span data-stu-id="f448a-149">See also</span></span>
--------

[<span data-ttu-id="f448a-150">Oversigt over personligt tilpassede produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="f448a-150">Personalized product recommendations overview</span></span>](personalized-product-recommendations.md)




