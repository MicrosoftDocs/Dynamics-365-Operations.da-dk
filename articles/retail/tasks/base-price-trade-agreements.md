---
title: " Basispris- og samhandelsaftaler"
description: Denne procedure gennemgår oprettelse af kanalspecifikke salgsprissamhandelsaftaler.
author: josaw1
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PriceDiscGroup, RetailStoreTable, RetailChannelPriceGroup, EcoResProductDetailsExtended, PriceDiscAdmTable, PriceDiscAdm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8138b6144cc6ba09834f2bfb61cc7334767307d6
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916547"
---
# <a name="base-price-and-trade-agreements"></a><span data-ttu-id="aadd5-103"> Basispris- og samhandelsaftaler</span><span class="sxs-lookup"><span data-stu-id="aadd5-103">Base price and trade agreements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="aadd5-104">Denne procedure gennemgår oprettelse af kanalspecifikke salgsprissamhandelsaftaler.</span><span class="sxs-lookup"><span data-stu-id="aadd5-104">This procedure walks through creating channel-specific sales price trade agreements.</span></span> <span data-ttu-id="aadd5-105">Proceduren bruger USRT-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="aadd5-105">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="aadd5-106">Gå i **navigationsruden** til **Moduler > Detail og handel > Styring af prissætning og rabatter > Prisgrupper > Alle prisgrupper**.</span><span class="sxs-lookup"><span data-stu-id="aadd5-106">In the **Navigation pane**, go to **Modules > Retail and commerce > Pricing and discounts management > Price groups > All price groups**.</span></span> <span data-ttu-id="aadd5-107">Prisgrupper er den måde samhandelsaftaler er tildelt til bestemte kanaler.</span><span class="sxs-lookup"><span data-stu-id="aadd5-107">Price groups are how trade agreements are assigned to specific channels.</span></span> <span data-ttu-id="aadd5-108">Hvis du bruger prisgrupper til at tildele samhandelsaftaler til en kanal, er det muligt at have kanalspecifikke priser.</span><span class="sxs-lookup"><span data-stu-id="aadd5-108">Using price groups to assign trade agreements to a channel enables channel-specific pricing.</span></span>  
2. <span data-ttu-id="aadd5-109">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="aadd5-109">Click **New**.</span></span>
3. <span data-ttu-id="aadd5-110">Indtast en værdi i feltet **Prisgrupper**.</span><span class="sxs-lookup"><span data-stu-id="aadd5-110">In the **Price groups** field, type a value.</span></span>
4. <span data-ttu-id="aadd5-111">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="aadd5-111">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="aadd5-112">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="aadd5-112">Click **Save**.</span></span>
6. <span data-ttu-id="aadd5-113">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="aadd5-113">Close the page.</span></span>
7. <span data-ttu-id="aadd5-114">På **navigationssiden** skal du gå til **Moduler > Detail og handel > Kanaler > Detailbutikker > Alle detailbutikker**.</span><span class="sxs-lookup"><span data-stu-id="aadd5-114">In the **Navigation pane**, go to **Modules > Retail and commerce > Channels > Retail stores > All retail stores**.</span></span>
8. <span data-ttu-id="aadd5-115">Vælg "New York" på listen</span><span class="sxs-lookup"><span data-stu-id="aadd5-115">In the list, select 'New York'</span></span>
9. <span data-ttu-id="aadd5-116">Klik på **Butik** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="aadd5-116">On the Action Pane, click **Store**.</span></span>
10. <span data-ttu-id="aadd5-117">Klik på **Prisgrupper**.</span><span class="sxs-lookup"><span data-stu-id="aadd5-117">Click **Price groups**.</span></span>
11. <span data-ttu-id="aadd5-118">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="aadd5-118">Click **New**.</span></span>
12. <span data-ttu-id="aadd5-119">Klik på rullelisten i feltet **Prisgrupper** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="aadd5-119">In the **Price groups** field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="aadd5-120">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="aadd5-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="aadd5-121">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="aadd5-121">Click **Save**.</span></span>
15. <span data-ttu-id="aadd5-122">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="aadd5-122">Close the page.</span></span>
16. <span data-ttu-id="aadd5-123">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="aadd5-123">Close the page.</span></span>
17. <span data-ttu-id="aadd5-124">Gå i **navigationsruden** til **Moduler > Detail og handel > Produkter og kategorier > Frigivne produkter efter kategori**.</span><span class="sxs-lookup"><span data-stu-id="aadd5-124">In the **Navigation pane**, go to **Modules > Retail and commerce > Products and categories > Released products by category**.</span></span>
18. <span data-ttu-id="aadd5-125">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="aadd5-125">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="aadd5-126">Klik på **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="aadd5-126">Click **Edit**.</span></span>
20. <span data-ttu-id="aadd5-127">Udvid oversigtspanelet **Sælg**.</span><span class="sxs-lookup"><span data-stu-id="aadd5-127">Expand the **Sell** fastTab.</span></span>
21. <span data-ttu-id="aadd5-128">Angiv et tal i feltet **Pris**.</span><span class="sxs-lookup"><span data-stu-id="aadd5-128">In the **Price** field, enter a number.</span></span> <span data-ttu-id="aadd5-129">Denne pris bruges, hvis der findes nogen relevante samhandelsaftaler.</span><span class="sxs-lookup"><span data-stu-id="aadd5-129">This price is used if no applicable trade agreements are found.</span></span>  
22. <span data-ttu-id="aadd5-130">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="aadd5-130">Click **Save**.</span></span>
23. <span data-ttu-id="aadd5-131">Klik på **Sælg** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="aadd5-131">On the **Action Pane**, click **Sell**.</span></span>
24. <span data-ttu-id="aadd5-132">Klik på **Opret handelsaftaler**.</span><span class="sxs-lookup"><span data-stu-id="aadd5-132">Click **Create trade agreements**.</span></span>
25. <span data-ttu-id="aadd5-133">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="aadd5-133">Click **New**.</span></span>
26. <span data-ttu-id="aadd5-134">Klik på rullelisten i feltet **Navn** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="aadd5-134">In the **Name** field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="aadd5-135">Vælg "Detail" på listen.</span><span class="sxs-lookup"><span data-stu-id="aadd5-135">In the list, select 'Retail'.</span></span> <span data-ttu-id="aadd5-136">I demodataene har kladdenavnet "Detail" standardrelationen "Pris (salg)".</span><span class="sxs-lookup"><span data-stu-id="aadd5-136">In the demo data, the 'Retail' journal name has the default relation of 'Price (sales)'.</span></span> <span data-ttu-id="aadd5-137">Det betyder, at alle nye linjer, der oprettes, som standard vil være salgsprissamhandelsaftaler.</span><span class="sxs-lookup"><span data-stu-id="aadd5-137">That means all new lines created will default to sales price trade agreements.</span></span>  
28. <span data-ttu-id="aadd5-138">Klik på **Linjer** i **Handlingsrude**.</span><span class="sxs-lookup"><span data-stu-id="aadd5-138">On the **Action pane**, click **Lines**.</span></span>
29. <span data-ttu-id="aadd5-139">Vælg 'Gruppe' i feltet **Kontokode**.</span><span class="sxs-lookup"><span data-stu-id="aadd5-139">In the **Account code** field, select 'Group'.</span></span>
30. <span data-ttu-id="aadd5-140">Klik på rullelisten i feltet **Kontovalg** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="aadd5-140">In the **Account selection** field, click the drop-down button to open the lookup.</span></span>
31. <span data-ttu-id="aadd5-141">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="aadd5-141">In the list, find and select the desired record.</span></span> <span data-ttu-id="aadd5-142">Dette fuldfører linket fra Kanal til Prisgruppe til Samhandelsaftale.</span><span class="sxs-lookup"><span data-stu-id="aadd5-142">This will complete the link from Channel to Price group to Trade agreement.</span></span>  
32. <span data-ttu-id="aadd5-143">Indtast en værdi i feltet **Varerelation**.</span><span class="sxs-lookup"><span data-stu-id="aadd5-143">In the **Item relation** field, type a value.</span></span>
33. <span data-ttu-id="aadd5-144">Indtast et tal i feltet **Beløb i valuta**.</span><span class="sxs-lookup"><span data-stu-id="aadd5-144">In the **Amount in currency** field, enter a number.</span></span>
34. <span data-ttu-id="aadd5-145">Markér evt. afkrydsningsfeltet **Find næste** i oversigtspanelet **Detaljer**.</span><span class="sxs-lookup"><span data-stu-id="aadd5-145">In the **Details** fastTab, check or uncheck the **Find next** checkbox.</span></span> <span data-ttu-id="aadd5-146">Når **Find næste** er angivet til 'Ja', fortsætter prisprogrammet med at søge efter relevante samhandelsaftaler med en lavere salgspris.</span><span class="sxs-lookup"><span data-stu-id="aadd5-146">When **Find next** is set to 'Yes', the pricing engine will continue to search for applicable trade agreements with a lower sale price.</span></span> <span data-ttu-id="aadd5-147">Når **Find næste** er indstillet til 'Nej', stopper prisprogrammet søgningen og bruger samhandelsaftalen.</span><span class="sxs-lookup"><span data-stu-id="aadd5-147">When **Find next** is set to 'No', the price engine stops searching and uses the trade agreement.</span></span>  
35. <span data-ttu-id="aadd5-148">Klik på **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="aadd5-148">Click **Post**.</span></span>
36. <span data-ttu-id="aadd5-149">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="aadd5-149">Click **OK**.</span></span>
37. <span data-ttu-id="aadd5-150">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="aadd5-150">Close the page.</span></span>
38. <span data-ttu-id="aadd5-151">Klik på Sælg i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="aadd5-151">On the **Action Pane**, click Sell.</span></span>
39. <span data-ttu-id="aadd5-152">Klik på **Salgspris**.</span><span class="sxs-lookup"><span data-stu-id="aadd5-152">Click **Sales price**.</span></span>

