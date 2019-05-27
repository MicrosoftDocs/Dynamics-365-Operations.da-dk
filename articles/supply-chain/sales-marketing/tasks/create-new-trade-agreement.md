---
title: Oprette en ny samhandelsaftale
description: Denne fremgangsmåde viser, hvordan du kan oprette en samhandelsaftale, hvor du registrerer en ny produktsalgspris, som du har aftalt med en bestemt debitor.
author: omulvad
manager: AnnBe
ms.date: 11/16/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e132cd20437b7929e81fcaa123d70bb57fb320c8
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549261"
---
# <a name="create-a-new-trade-agreement"></a><span data-ttu-id="b6e65-103">Oprette en ny samhandelsaftale</span><span class="sxs-lookup"><span data-stu-id="b6e65-103">Create a new trade agreement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b6e65-104">Denne fremgangsmåde viser, hvordan du kan oprette en samhandelsaftale, hvor du registrerer en ny produktsalgspris, som du har aftalt med en bestemt debitor.</span><span class="sxs-lookup"><span data-stu-id="b6e65-104">This procedure shows you how to create a trade agreement where you register a new product sales price that you've agreed with a specific customer.</span></span> <span data-ttu-id="b6e65-105">Du kan køre denne procedure på dit eget demodatafirma USMF eller på dine egne data.</span><span class="sxs-lookup"><span data-stu-id="b6e65-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="b6e65-106">Hvis du bruger dine egne data, før du starter denne vejledning, skal du sikre, at der findes et navn på en Samhandelskladde, hvor standardrelationen er indstillet til "Pris (salg)".</span><span class="sxs-lookup"><span data-stu-id="b6e65-106">If you’re using your own data, before you start this guide you need to make sure that a Trade agreement journal name exists where the Default relation is set to “Price (sales)”.</span></span>


## <a name="create-and-post-a-new-trade-agreement-journal"></a><span data-ttu-id="b6e65-107">Opret og bogfør en ny samhandelsaftalekladde</span><span class="sxs-lookup"><span data-stu-id="b6e65-107">Create and post a new trade agreement journal</span></span>
1. <span data-ttu-id="b6e65-108">Gå til Salg og marketing > Priser og rabatter > Samhandelskladder.</span><span class="sxs-lookup"><span data-stu-id="b6e65-108">Go to Sales and marketing > Prices and discounts > Trade agreement journals.</span></span>
2. <span data-ttu-id="b6e65-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="b6e65-109">Click New.</span></span>
3. <span data-ttu-id="b6e65-110">Klik på rullelisten i feltet Navn for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="b6e65-110">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="b6e65-111">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="b6e65-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="b6e65-112">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="b6e65-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="b6e65-113">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="b6e65-113">Click Lines.</span></span>
7. <span data-ttu-id="b6e65-114">Vælg "Tabel" i feltet Kontokode.</span><span class="sxs-lookup"><span data-stu-id="b6e65-114">In the Account code field, select 'Table'.</span></span>
    * <span data-ttu-id="b6e65-115">I dette eksempel skal du opdatere prisen for en bestemt debitor, hvilket betyder, at du skal vælge Tabel.</span><span class="sxs-lookup"><span data-stu-id="b6e65-115">In this example, you're updating the price for a specific customer, which means you need to choose Table.</span></span> <span data-ttu-id="b6e65-116">Hvis du har opdateret produktets listepris, skal du markere Alle, så den nye pris gælder alle debitorer.</span><span class="sxs-lookup"><span data-stu-id="b6e65-116">If you were updating the product's list price, you would select All, so that the new price is valid for all customers.</span></span> <span data-ttu-id="b6e65-117">Hvis du differentierer priser mellem forskellige debitorsegmenter, skal du vælge Gruppe.</span><span class="sxs-lookup"><span data-stu-id="b6e65-117">If you were differentiating prices among different customer segments, then you would select Group.</span></span> <span data-ttu-id="b6e65-118">Hvis du vil vælge Gruppe, skal du have indstillet Debitorprisgrupper.</span><span class="sxs-lookup"><span data-stu-id="b6e65-118">To select Group, you must have set up Customer price groups.</span></span>  
8. <span data-ttu-id="b6e65-119">Klik på rullelisten i feltet Kontovalg for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="b6e65-119">In the Account selection field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="b6e65-120">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="b6e65-120">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="b6e65-121">Vælg "Tabel" i feltet Varekode.</span><span class="sxs-lookup"><span data-stu-id="b6e65-121">In the Item code field, select 'Table'.</span></span>
    * <span data-ttu-id="b6e65-122">Når du indtaster en samhandelsaftale af typen "Pris (salg)", skal du kun vælge "Tabel" i feltet Varekode.</span><span class="sxs-lookup"><span data-stu-id="b6e65-122">When you are entering a trade agreement of type 'Price (sales)', you must only select 'Table' in the Item code field.</span></span> <span data-ttu-id="b6e65-123">Det skyldes, at en pris er en absolut værdi og ikke kan være ens for alle produkter eller gruppe af produkter.</span><span class="sxs-lookup"><span data-stu-id="b6e65-123">This is because a price is an absolute value and cannot be same for all products or a group of products.</span></span>  
11. <span data-ttu-id="b6e65-124">Klik på rullelisten i feltet Varerelation for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="b6e65-124">In the Item relation field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="b6e65-125">Vælg det produkt, der inkluderes i dokumentet, på listen.</span><span class="sxs-lookup"><span data-stu-id="b6e65-125">In the list, select the product you want to include in the agreement.</span></span>
    * <span data-ttu-id="b6e65-126">Noter hvilket produkt, du har valgt.</span><span class="sxs-lookup"><span data-stu-id="b6e65-126">Make a note of which product you've selected.</span></span>  
13. <span data-ttu-id="b6e65-127">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="b6e65-127">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="b6e65-128">Indtast en minimummængde i feltet Fra.</span><span class="sxs-lookup"><span data-stu-id="b6e65-128">In the From field, enter a minimum quantity.</span></span>
    * <span data-ttu-id="b6e65-129">Hvis debitoren skal bestille et minimumsantal, før de kan blive kvalificeret til den nye pris, skal du angive antallet her.</span><span class="sxs-lookup"><span data-stu-id="b6e65-129">If the customer has to order a minimum quantity  before they can qualify for the new price, then you need to specify that quantity here.</span></span>  
    * <span data-ttu-id="b6e65-130">Angiv en værdi i feltet Til for at angive det maksimale antal, over hvilken aftalens pris ikke er gyldig.</span><span class="sxs-lookup"><span data-stu-id="b6e65-130">Enter a value in the To field to specify the maximum quantity above which the agreement's price will not be valid.</span></span> <span data-ttu-id="b6e65-131">Hvis du tilbyder priser og rabatter, der er baseret på flere mængdereduktioner, skal du angive hver mængdekategori som et par med min. og maks. mængde i felterne henholdsvis "Fra" og "Til".</span><span class="sxs-lookup"><span data-stu-id="b6e65-131">If you offer prices and discounts based on multiple quantity breaks, then specify each quantity bracket as a pair of minimum and maximum quantity in the 'From' and 'To' fields respectively.</span></span>  
15. <span data-ttu-id="b6e65-132">Indtast en pris i feltet Beløb i valuta.</span><span class="sxs-lookup"><span data-stu-id="b6e65-132">In the Amount in currency field, enter a price.</span></span>
16. <span data-ttu-id="b6e65-133">Indtast en dato, hvorfra denne aftale vil være gyldig, i feltet Fra dato.</span><span class="sxs-lookup"><span data-stu-id="b6e65-133">In the From date field, enter a date from which this agreement will be valid.</span></span>
17. <span data-ttu-id="b6e65-134">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="b6e65-134">Click Save.</span></span>
18. <span data-ttu-id="b6e65-135">Klik på Valider.</span><span class="sxs-lookup"><span data-stu-id="b6e65-135">Click Validate.</span></span>
19. <span data-ttu-id="b6e65-136">Klik på Valider valgte linjer.</span><span class="sxs-lookup"><span data-stu-id="b6e65-136">Click Validate selected lines.</span></span>
20. <span data-ttu-id="b6e65-137">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="b6e65-137">Click OK.</span></span>
21. <span data-ttu-id="b6e65-138">Klik på Bogfør.</span><span class="sxs-lookup"><span data-stu-id="b6e65-138">Click Post.</span></span>
22. <span data-ttu-id="b6e65-139">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="b6e65-139">Click OK.</span></span>

## <a name="view-trade-agreements-for-a-product"></a><span data-ttu-id="b6e65-140">Få vist samhandelsaftaler for et produkt</span><span class="sxs-lookup"><span data-stu-id="b6e65-140">View trade agreements for a product</span></span>
1. <span data-ttu-id="b6e65-141">Gå til Administration af produktoplysninger > Produkter > Frigivne produkter.</span><span class="sxs-lookup"><span data-stu-id="b6e65-141">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="b6e65-142">På listen skal du finde og vælge produktet, hvis pris du netop har opdateret.</span><span class="sxs-lookup"><span data-stu-id="b6e65-142">In the list, find and select the product whose price you have just updated.</span></span>
3. <span data-ttu-id="b6e65-143">Klik på Sælg i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="b6e65-143">On the Action Pane, click Sell.</span></span>
4. <span data-ttu-id="b6e65-144">Klik på Vis samhandelsaftaler.</span><span class="sxs-lookup"><span data-stu-id="b6e65-144">Click View trade agreements.</span></span>
    * <span data-ttu-id="b6e65-145">Gennemse oplysningerne om samhandelsaftalens pris, som du lige har oprettet.</span><span class="sxs-lookup"><span data-stu-id="b6e65-145">Review the details of the price trade agreement you have just created.</span></span>    
5. <span data-ttu-id="b6e65-146">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="b6e65-146">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b6e65-147">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="b6e65-147">Additional resources</span></span>
### <a name="community-blogs"></a><span data-ttu-id="b6e65-148">Fællesskabsblogge</span><span class="sxs-lookup"><span data-stu-id="b6e65-148">Community blogs</span></span>
- [<span data-ttu-id="b6e65-149">Salgspriser i Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b6e65-149">Sales prices in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/11/14/sales-prices-in-dynamics-365-for-finance-and-operations/#sales_price_in_trade_agreements)
