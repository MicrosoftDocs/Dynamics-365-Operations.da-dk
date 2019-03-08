---
title: Føje et kontrolelement med anbefalinger til posteringsskærmen på POS-enheder
description: I dette emne beskrives, hvordan du tilføjer et kontrolelement med anbefalinger til transaktionsskærmbilledet på en POS-enhed (point of sale) ved hjælp af skærmlayoutdesigneren i Microsoft Dynamics 365 for Retail.
author: ashishmsft
manager: AnnBe
ms.date: 02/05/2018
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
ms.openlocfilehash: 213b47422a5e31c2cfc2d173b8c7d9efdecc7568
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "320437"
---
# <a name="add-a-recommendations-control-to-the-transaction-screen-on-pos-devices"></a><span data-ttu-id="3cbef-103">Føje et kontrolelement med anbefalinger til posteringsskærmen på POS-enheder</span><span class="sxs-lookup"><span data-stu-id="3cbef-103">Add a recommendations control to the transaction screen on POS devices</span></span>

[!include [banner](includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="3cbef-104">Vi vil fjerne den aktuelle version af produktanbefalingstjenesten, fordi vi ændrer denne funktion og giver den en bedre algoritme og nyere detailrelaterede funktioner.</span><span class="sxs-lookup"><span data-stu-id="3cbef-104">We are removing the current version of the product recommendation service as we redesign this feature with a better algorithm and newer retail-oriented capabilities.</span></span> <span data-ttu-id="3cbef-105">Du kan finde flere oplysninger i [Fjernede eller forældede funktioner](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features).</span><span class="sxs-lookup"><span data-stu-id="3cbef-105">For more information see [Removed or deprecated features](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features).</span></span>

<span data-ttu-id="3cbef-106">I dette emne beskrives, hvordan du tilføjer et kontrolelement med anbefalinger til transaktionsskærmbilledet på en POS-enhed (point of sale) ved hjælp af skærmlayoutdesigneren i Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="3cbef-106">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="3cbef-107">Du kan få vist produktanbefalinger på POS-enheden, når du bruger Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="3cbef-107">You can display product recommendations on your POS device when you use Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="3cbef-108">*Anbefalinger* er varer, som kunden muligvis er interesseret i baseret på deres købshistorik, varer i deres ønskeseddel og varer, som andre kunder har købt online og i fysiske butikker.</span><span class="sxs-lookup"><span data-stu-id="3cbef-108">*Recommendations* are items that your customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="3cbef-109">For at få vist produktanbefalinger skal du føje et kontrolelement til transaktionsskærmen ved hjælp af skærmlayoutdesigneren.</span><span class="sxs-lookup"><span data-stu-id="3cbef-109">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span>

## <a name="open-layout-designer"></a><span data-ttu-id="3cbef-110">Åbn layoutdesigner</span><span class="sxs-lookup"><span data-stu-id="3cbef-110">Open Layout designer</span></span>

1. <span data-ttu-id="3cbef-111">Gå til **Retail** &gt; **Konfiguration af kanal** &gt; **POS-opsætning** &gt; **POS** &gt; **Skærmlayout**.</span><span class="sxs-lookup"><span data-stu-id="3cbef-111">Go to **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2. <span data-ttu-id="3cbef-112">Brug Quick Filter til at finde det skærmbillede, du vil føje kontrolelementet til.</span><span class="sxs-lookup"><span data-stu-id="3cbef-112">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="3cbef-113">Filtrer for eksempel på feltet **Skærmlayout-id** ved hjælp af værdien 'F2CP16:9M'.</span><span class="sxs-lookup"><span data-stu-id="3cbef-113">For example, filter on the **Screen layout ID** field using a value of 'F2CP16:9M'.</span></span>
3. <span data-ttu-id="3cbef-114">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="3cbef-114">In the list, find and select the desired record.</span></span> <span data-ttu-id="3cbef-115">Vælg for eksempel 'Navn: F2CP16:9M skærmlayout-ID: F2CP16:9M'.</span><span class="sxs-lookup"><span data-stu-id="3cbef-115">For example, select 'Name: F2CP16:9M Screen Layout ID: F2CP16:9M'.</span></span>
4. <span data-ttu-id="3cbef-116">Klik på **Layoutdesigner**.</span><span class="sxs-lookup"><span data-stu-id="3cbef-116">Click **Layout designer**.</span></span>
5. <span data-ttu-id="3cbef-117">Følg vejledningen for at starte layoutdesigneren.</span><span class="sxs-lookup"><span data-stu-id="3cbef-117">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="3cbef-118">Når du bliver bedt om legitimationsoplysninger, skal du angive de legitimationsoplysninger, der var i brug, da layoutdesigneren blev startet fra **Skærmlayout** siden.</span><span class="sxs-lookup"><span data-stu-id="3cbef-118">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6. <span data-ttu-id="3cbef-119">Når du logger på, vises en side, der ligner den nedenfor.</span><span class="sxs-lookup"><span data-stu-id="3cbef-119">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="3cbef-120">Layoutet er forskelligt, afhængigt af de tilpasninger, der er foretaget for din butik.</span><span class="sxs-lookup"><span data-stu-id="3cbef-120">The layout will be different depending on the customizations that were made for your store.</span></span>

    <span data-ttu-id="3cbef-121">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span><span class="sxs-lookup"><span data-stu-id="3cbef-121">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span></span>

## <a name="choose-a-display-option"></a><span data-ttu-id="3cbef-122">Vælg en visningsindstilling</span><span class="sxs-lookup"><span data-stu-id="3cbef-122">Choose a display option</span></span>

<span data-ttu-id="3cbef-123">Der findes to konfigurationsindstillinger.</span><span class="sxs-lookup"><span data-stu-id="3cbef-123">There are two configurations options available.</span></span> <span data-ttu-id="3cbef-124">Vælg den indstilling, der passer bedst til din butik, og følg derefter vejledningen for at afslutte opsætningen af kontrolelementet.</span><span class="sxs-lookup"><span data-stu-id="3cbef-124">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="3cbef-125">Der er følgende to indstillinger:</span><span class="sxs-lookup"><span data-stu-id="3cbef-125">The two options are:</span></span>

- <span data-ttu-id="3cbef-126">Anbefalingerne er altid synlige.</span><span class="sxs-lookup"><span data-stu-id="3cbef-126">Recommendations are always visible.</span></span>
- <span data-ttu-id="3cbef-127">Fanen **Anbefalinger** vises i gitteret i højre side af skærmen.</span><span class="sxs-lookup"><span data-stu-id="3cbef-127">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

### <a name="make-recommendations-always-visible"></a><span data-ttu-id="3cbef-128">Gøre anbefalinger synlige permanent</span><span class="sxs-lookup"><span data-stu-id="3cbef-128">Make recommendations always visible</span></span>

1. <span data-ttu-id="3cbef-129">Reducer højden af området med detaljer for transaktionslinjer, så det har samme højde som kundepanelet til venstre.</span><span class="sxs-lookup"><span data-stu-id="3cbef-129">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.</span></span>

    <span data-ttu-id="3cbef-130">[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="3cbef-130">[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>

2. <span data-ttu-id="3cbef-131">I menuen til venstre skal du trække og slippe kontrolelementet med anbefalinger til mellem området med transaktionslinjedetaljer og knapmatricen nederst i midten af transaktionsskærmbilledet.</span><span class="sxs-lookup"><span data-stu-id="3cbef-131">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="3cbef-132">Rediger størrelsen på kontrolelementet, så det passer i det pågældende område.</span><span class="sxs-lookup"><span data-stu-id="3cbef-132">Resize the control so it fits in that space.</span></span>

    <span data-ttu-id="3cbef-133">[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="3cbef-133">[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>

3. <span data-ttu-id="3cbef-134">Klik på **X** for at lukke og afslutte layoutdesigneren.</span><span class="sxs-lookup"><span data-stu-id="3cbef-134">Click the **X** to save and exit Layout designer.</span></span>
4. <span data-ttu-id="3cbef-135">I Dynamics 365 for Retail skal du gå til **Detail** &gt; **Detail-it** &gt; **Distributionsplaner**.</span><span class="sxs-lookup"><span data-stu-id="3cbef-135">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
5. <span data-ttu-id="3cbef-136">Vælg  **1090, kasseapparater** på listen.</span><span class="sxs-lookup"><span data-stu-id="3cbef-136">In the list, select **1090 Registers**.</span></span>
6. <span data-ttu-id="3cbef-137">Klik på **Kør nu**.</span><span class="sxs-lookup"><span data-stu-id="3cbef-137">Click **Run now**.</span></span>

### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="3cbef-138">Tilføj fanen Anbefalinger i gitteret nederst i højre side af skærmen</span><span class="sxs-lookup"><span data-stu-id="3cbef-138">Add a Recommendations tab to the button grid on the right side of the screen</span></span>

1. <span data-ttu-id="3cbef-139">Højreklik på det tomme område under den sidste fane i knapmatricen i højre side af siden.</span><span class="sxs-lookup"><span data-stu-id="3cbef-139">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>
2. <span data-ttu-id="3cbef-140">Klik på **Tilpas**.</span><span class="sxs-lookup"><span data-stu-id="3cbef-140">Click **Customize**.</span></span>

    <span data-ttu-id="3cbef-141">[![PIC-5](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="3cbef-141">[![pic-5](./media/pic-5.png)](./media/pic-5.png)</span></span>

3. <span data-ttu-id="3cbef-142">Klik på fanen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="3cbef-142">Click **New tab**.</span></span>
4. <span data-ttu-id="3cbef-143">Find den nye fane, du lige har tilføjet.</span><span class="sxs-lookup"><span data-stu-id="3cbef-143">Find the new tab that you just added.</span></span> <span data-ttu-id="3cbef-144">Du skal muligvis rulle ned.</span><span class="sxs-lookup"><span data-stu-id="3cbef-144">You may need to scroll down.</span></span>
5. <span data-ttu-id="3cbef-145">I rullemenuen **Indhold** skal du vælge **Anbefalede produkter**.</span><span class="sxs-lookup"><span data-stu-id="3cbef-145">In the **Contents** drop-down, select **Recommended products**.</span></span>

    <span data-ttu-id="3cbef-146">[![PIC-6](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="3cbef-146">[![pic-6](./media/pic-6.png)](./media/pic-6.png)</span></span>

6. <span data-ttu-id="3cbef-147">I feltet **Etiket** skal du angive et navn til fanen Anbefalinger. Skriv f.eks. 'Anbefalede produkter'.</span><span class="sxs-lookup"><span data-stu-id="3cbef-147">In the **Label** field, type a name for the recommendations tab. For example, type 'Recommended products'.</span></span>
7. <span data-ttu-id="3cbef-148">Vælg det billede, der skal vises på fanen, i feltet **Billede**.</span><span class="sxs-lookup"><span data-stu-id="3cbef-148">In the **Image** field, select the image to appear on the tab.</span></span>
8. <span data-ttu-id="3cbef-149">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="3cbef-149">Click **OK**.</span></span> <span data-ttu-id="3cbef-150">Den nye fane vises i knapmatricen.</span><span class="sxs-lookup"><span data-stu-id="3cbef-150">The new tab appears in the button grid.</span></span>
9. <span data-ttu-id="3cbef-151">Klik på **X** for at lukke og afslutte layoutdesigneren.</span><span class="sxs-lookup"><span data-stu-id="3cbef-151">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="3cbef-152">I Dynamics 365 for Retail skal du gå til **Detail** &gt; **Detail-it** &gt; **Distributionsplaner**.</span><span class="sxs-lookup"><span data-stu-id="3cbef-152">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="3cbef-153">Vælg **1090 kasseapparater** på listen.</span><span class="sxs-lookup"><span data-stu-id="3cbef-153">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="3cbef-154">Klik på **Kør nu**.</span><span class="sxs-lookup"><span data-stu-id="3cbef-154">Click **Run now**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3cbef-155">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="3cbef-155">Additional resources</span></span>

[<span data-ttu-id="3cbef-156">Oversigt over tilpassede produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="3cbef-156">Personalized product recommendations overview</span></span>](personalized-product-recommendations.md)
