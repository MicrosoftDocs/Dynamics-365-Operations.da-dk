---
title: " Basispris- og samhandelsaftaler"
description: Denne procedure gennemgår oprettelse af kanalspecifikke salgsprissamhandelsaftaler.
author: josaw1
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PriceDiscGroup, RetailStoreTable, RetailChannelPriceGroup, EcoResProductDetailsExtended, PriceDiscAdmTable, PriceDiscAdm
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: df4d0042e51524c1d50568e969b59923a7ba4a65
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5789798"
---
# <a name="base-price-and-trade-agreements"></a><span data-ttu-id="a098f-103"> Basispris- og samhandelsaftaler</span><span class="sxs-lookup"><span data-stu-id="a098f-103">Base price and trade agreements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a098f-104">Denne procedure gennemgår oprettelse af kanalspecifikke salgsprissamhandelsaftaler.</span><span class="sxs-lookup"><span data-stu-id="a098f-104">This procedure walks through creating channel-specific sales price trade agreements.</span></span> <span data-ttu-id="a098f-105">Proceduren bruger USRT-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="a098f-105">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="a098f-106">Gå til **Moduler > Retail og Commerce > Styring af prissætning og rabatter > Prisgrupper > Alle prisgrupper** i **Navigationsrude**.</span><span class="sxs-lookup"><span data-stu-id="a098f-106">In the **Navigation pane**, go to **Modules > Retail and Commerce > Pricing and discounts management > Price groups > All price groups**.</span></span> <span data-ttu-id="a098f-107">Prisgrupper er den måde samhandelsaftaler er tildelt til bestemte kanaler.</span><span class="sxs-lookup"><span data-stu-id="a098f-107">Price groups are how trade agreements are assigned to specific channels.</span></span> <span data-ttu-id="a098f-108">Hvis du bruger prisgrupper til at tildele samhandelsaftaler til en kanal, er det muligt at have kanalspecifikke priser.</span><span class="sxs-lookup"><span data-stu-id="a098f-108">Using price groups to assign trade agreements to a channel enables channel-specific pricing.</span></span>  
2. <span data-ttu-id="a098f-109">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a098f-109">Click **New**.</span></span>
3. <span data-ttu-id="a098f-110">Indtast en værdi i feltet **Prisgrupper**.</span><span class="sxs-lookup"><span data-stu-id="a098f-110">In the **Price groups** field, type a value.</span></span>
4. <span data-ttu-id="a098f-111">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="a098f-111">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="a098f-112">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="a098f-112">Click **Save**.</span></span>
6. <span data-ttu-id="a098f-113">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a098f-113">Close the page.</span></span>
7. <span data-ttu-id="a098f-114">Gå til **Moduler > Retail og Commerce > Kanaler > Butikker > Alle butikker** i **Navigationsrude**.</span><span class="sxs-lookup"><span data-stu-id="a098f-114">In the **Navigation pane**, go to **Modules > Retail and Commerce > Channels > Stores > All stores**.</span></span>
8. <span data-ttu-id="a098f-115">Vælg "New York" på listen</span><span class="sxs-lookup"><span data-stu-id="a098f-115">In the list, select 'New York'</span></span>
9. <span data-ttu-id="a098f-116">Klik på **Butik** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="a098f-116">On the Action Pane, click **Store**.</span></span>
10. <span data-ttu-id="a098f-117">Klik på **Prisgrupper**.</span><span class="sxs-lookup"><span data-stu-id="a098f-117">Click **Price groups**.</span></span>
11. <span data-ttu-id="a098f-118">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a098f-118">Click **New**.</span></span>
12. <span data-ttu-id="a098f-119">Klik på rullelisten i feltet **Prisgrupper** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="a098f-119">In the **Price groups** field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="a098f-120">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="a098f-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="a098f-121">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="a098f-121">Click **Save**.</span></span>
15. <span data-ttu-id="a098f-122">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a098f-122">Close the page.</span></span>
16. <span data-ttu-id="a098f-123">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a098f-123">Close the page.</span></span>
17. <span data-ttu-id="a098f-124">Gå til **Moduler > Retail og Commerce > Produkter og kategorier > Frigivne produkter efter kategori** i **Navigationsrude**.</span><span class="sxs-lookup"><span data-stu-id="a098f-124">In the **Navigation pane**, go to **Modules > Retail and Commerce > Products and categories > Released products by category**.</span></span>
18. <span data-ttu-id="a098f-125">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="a098f-125">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="a098f-126">Klik på **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="a098f-126">Click **Edit**.</span></span>
20. <span data-ttu-id="a098f-127">Udvid oversigtspanelet **Sælg**.</span><span class="sxs-lookup"><span data-stu-id="a098f-127">Expand the **Sell** fastTab.</span></span>
21. <span data-ttu-id="a098f-128">Angiv et tal i feltet **Pris**.</span><span class="sxs-lookup"><span data-stu-id="a098f-128">In the **Price** field, enter a number.</span></span> <span data-ttu-id="a098f-129">Denne pris bruges, hvis der findes nogen relevante samhandelsaftaler.</span><span class="sxs-lookup"><span data-stu-id="a098f-129">This price is used if no applicable trade agreements are found.</span></span>  
22. <span data-ttu-id="a098f-130">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="a098f-130">Click **Save**.</span></span>
23. <span data-ttu-id="a098f-131">Klik på **Sælg** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="a098f-131">On the **Action Pane**, click **Sell**.</span></span>
24. <span data-ttu-id="a098f-132">Klik på **Opret handelsaftaler**.</span><span class="sxs-lookup"><span data-stu-id="a098f-132">Click **Create trade agreements**.</span></span>
25. <span data-ttu-id="a098f-133">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a098f-133">Click **New**.</span></span>
26. <span data-ttu-id="a098f-134">Klik på rullelisten i feltet **Navn** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="a098f-134">In the **Name** field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="a098f-135">Markér **Commerce** på listen.</span><span class="sxs-lookup"><span data-stu-id="a098f-135">In the list, select **Commerce**.</span></span> <span data-ttu-id="a098f-136">I demodataene har kladdenavnet **Commerce** standardrelationen **Pris (salg)**.</span><span class="sxs-lookup"><span data-stu-id="a098f-136">In the demo data, the **Commerce** journal name has the default relation of **Price (sales)**.</span></span> <span data-ttu-id="a098f-137">Det betyder, at alle nye linjer, der oprettes, som standard vil være salgsprissamhandelsaftaler.</span><span class="sxs-lookup"><span data-stu-id="a098f-137">That means all new lines created will default to sales price trade agreements.</span></span>  
28. <span data-ttu-id="a098f-138">Klik på **Linjer** i **Handlingsrude**.</span><span class="sxs-lookup"><span data-stu-id="a098f-138">On the **Action pane**, click **Lines**.</span></span>
29. <span data-ttu-id="a098f-139">Vælg 'Gruppe' i feltet **Type af partkode**.</span><span class="sxs-lookup"><span data-stu-id="a098f-139">In the **Party code type** field, select 'Group'.</span></span>
30. <span data-ttu-id="a098f-140">Klik på rullelisten i feltet **Kontovalg** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="a098f-140">In the **Account selection** field, click the drop-down button to open the lookup.</span></span>
31. <span data-ttu-id="a098f-141">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="a098f-141">In the list, find and select the desired record.</span></span> <span data-ttu-id="a098f-142">Dette fuldfører linket fra Kanal til Prisgruppe til Samhandelsaftale.</span><span class="sxs-lookup"><span data-stu-id="a098f-142">This will complete the link from Channel to Price group to Trade agreement.</span></span>  
32. <span data-ttu-id="a098f-143">Indtast en værdi i feltet **Varerelation**.</span><span class="sxs-lookup"><span data-stu-id="a098f-143">In the **Item relation** field, type a value.</span></span>
33. <span data-ttu-id="a098f-144">Indtast et tal i feltet **Beløb i valuta**.</span><span class="sxs-lookup"><span data-stu-id="a098f-144">In the **Amount in currency** field, enter a number.</span></span>
34. <span data-ttu-id="a098f-145">Markér evt. afkrydsningsfeltet **Find næste** i oversigtspanelet **Detaljer**.</span><span class="sxs-lookup"><span data-stu-id="a098f-145">In the **Details** fastTab, check or uncheck the **Find next** checkbox.</span></span> <span data-ttu-id="a098f-146">Når **Find næste** er angivet til 'Ja', fortsætter prisprogrammet med at søge efter relevante samhandelsaftaler med en lavere salgspris.</span><span class="sxs-lookup"><span data-stu-id="a098f-146">When **Find next** is set to 'Yes', the pricing engine will continue to search for applicable trade agreements with a lower sale price.</span></span> <span data-ttu-id="a098f-147">Når **Find næste** er indstillet til 'Nej', stopper prisprogrammet søgningen og bruger samhandelsaftalen.</span><span class="sxs-lookup"><span data-stu-id="a098f-147">When **Find next** is set to 'No', the price engine stops searching and uses the trade agreement.</span></span>  
35. <span data-ttu-id="a098f-148">Klik på **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="a098f-148">Click **Post**.</span></span>
36. <span data-ttu-id="a098f-149">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="a098f-149">Click **OK**.</span></span>
37. <span data-ttu-id="a098f-150">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a098f-150">Close the page.</span></span>
38. <span data-ttu-id="a098f-151">Klik på Sælg i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="a098f-151">On the **Action Pane**, click Sell.</span></span>
39. <span data-ttu-id="a098f-152">Klik på **Salgspris**.</span><span class="sxs-lookup"><span data-stu-id="a098f-152">Click **Sales price**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]