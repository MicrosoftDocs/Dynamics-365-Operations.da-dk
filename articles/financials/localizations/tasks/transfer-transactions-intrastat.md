---
title: Overføre posteringer til Intrastat
description: Denne procedure viser dig, hvordan du kan konfigurere Intrastat-parametre og overføre transaktioner til Intrastat.
author: Anasyash
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategory, UnitOfMeasureLookup, ProcCategoryAddCommodityCode, EcoResProductDetailsExtended, IntrastatCommodityLookup, IntrastatTransactionCode, IntrastatParameters, DeliveryMode, MarkupTable, SalesTableListPage, SalesCreateOrder, SalesTable, MarkupTrans, SalesEditLines,  Intrastat, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: anasyash
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 13cc9dc2119ad3dc85d580e92edee7bb9ef2075c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "370268"
---
# <a name="transfer-transactions-to-the-intrastat"></a><span data-ttu-id="16b4e-103">Overføre posteringer til Intrastat</span><span class="sxs-lookup"><span data-stu-id="16b4e-103">Transfer transactions to the Intrastat</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="16b4e-104">Denne procedure viser dig, hvordan du kan konfigurere Intrastat-parametre og overføre transaktioner til Intrastat.</span><span class="sxs-lookup"><span data-stu-id="16b4e-104">This procedure walks you through how to set up Intrastat parameters and transfer transactions to Intrastat.</span></span> <span data-ttu-id="16b4e-105">Denne procedure blev oprettet ved hjælp af demodatafirmaet DEMF.</span><span class="sxs-lookup"><span data-stu-id="16b4e-105">This procedure was created using the demo data company DEMF.</span></span>


## <a name="create-new-and-update-existing-commodity-code"></a><span data-ttu-id="16b4e-106">Oprette en ny og opdatere en eksisterende varekode</span><span class="sxs-lookup"><span data-stu-id="16b4e-106">Create new and update existing commodity code</span></span>
1. <span data-ttu-id="16b4e-107">Gå til administration af produktoplysninger > Opsætning af > Kategorier og attributter > Kategorihierarkier.</span><span class="sxs-lookup"><span data-stu-id="16b4e-107">Go to Product information management > Setup > Categories and attributes > Category hierarchies.</span></span>
2. <span data-ttu-id="16b4e-108">Søg på listen eller vælg posten "Intrastat-varekoder."</span><span class="sxs-lookup"><span data-stu-id="16b4e-108">In the list, find or select the record "Intrastat commodity codes."</span></span>
3. <span data-ttu-id="16b4e-109">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="16b4e-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="16b4e-110">Vælg 'en post' i træet.</span><span class="sxs-lookup"><span data-stu-id="16b4e-110">In the tree, select 'a record'.</span></span>
    * <span data-ttu-id="16b4e-111">Vælg for eksempel 'Intrastat\Speaker'.</span><span class="sxs-lookup"><span data-stu-id="16b4e-111">For example, select 'Intrastat\Speaker'.</span></span>  
5. <span data-ttu-id="16b4e-112">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="16b4e-112">Click Edit.</span></span>
6. <span data-ttu-id="16b4e-113">Udvid sektionen Udenrigshandel.</span><span class="sxs-lookup"><span data-stu-id="16b4e-113">Expand the Foreign trade section.</span></span>
7. <span data-ttu-id="16b4e-114">Indtast eller vælg en værdi i feltet Supplerende enheder.</span><span class="sxs-lookup"><span data-stu-id="16b4e-114">In the Additional units field, enter or select a value.</span></span>
    * <span data-ttu-id="16b4e-115">Vælg for eksempel 'styk'.</span><span class="sxs-lookup"><span data-stu-id="16b4e-115">For example, choose 'pcs'.</span></span>  
8. <span data-ttu-id="16b4e-116">Vælg Ja i feltet Vægt ikke gældende.</span><span class="sxs-lookup"><span data-stu-id="16b4e-116">Select Yes in the Weight not applicable field.</span></span>
9. <span data-ttu-id="16b4e-117">Vælg 'Intrastat' i træet.</span><span class="sxs-lookup"><span data-stu-id="16b4e-117">In the tree, select 'Intrastat'.</span></span>
10. <span data-ttu-id="16b4e-118">Klik på Ny kategorinode.</span><span class="sxs-lookup"><span data-stu-id="16b4e-118">Click New category node.</span></span>
11. <span data-ttu-id="16b4e-119">Indtast navnet på varen i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="16b4e-119">In the Name field, enter the name of commodity.</span></span>
    * <span data-ttu-id="16b4e-120">Skriv for eksempel 'Anden varekode'.</span><span class="sxs-lookup"><span data-stu-id="16b4e-120">For example, type 'Other commodity'.</span></span>  
12. <span data-ttu-id="16b4e-121">Indtast varekoden i feltet Kode.</span><span class="sxs-lookup"><span data-stu-id="16b4e-121">In the Code field, enter the commodity code.</span></span>
    * <span data-ttu-id="16b4e-122">Skriv for eksempel '995 00 00'.</span><span class="sxs-lookup"><span data-stu-id="16b4e-122">For example, type '995 00 00'.</span></span>  
13. <span data-ttu-id="16b4e-123">Indtast en værdi i feltet Brugervenligt navn.</span><span class="sxs-lookup"><span data-stu-id="16b4e-123">In the Friendly name field, type a value.</span></span>
    * <span data-ttu-id="16b4e-124">Skriv for eksempel 'Anden'.</span><span class="sxs-lookup"><span data-stu-id="16b4e-124">For example, type 'Other'.</span></span>  
14. <span data-ttu-id="16b4e-125">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="16b4e-125">Click Save.</span></span>
15. <span data-ttu-id="16b4e-126">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="16b4e-126">Close the page.</span></span>

## <a name="assign-commodity-code-to-product-hierarchy-and-released-product"></a><span data-ttu-id="16b4e-127">Tildele varekode til et produkthierarki og et frigivet produkt</span><span class="sxs-lookup"><span data-stu-id="16b4e-127">Assign commodity code to product hierarchy and released product</span></span>
1. <span data-ttu-id="16b4e-128">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="16b4e-128">Use the Quick Filter to find records.</span></span> <span data-ttu-id="16b4e-129">Du kan for eksempel filtrere på feltet Navn med værdien 'salg'.</span><span class="sxs-lookup"><span data-stu-id="16b4e-129">For example, filter on the Name field with a value of 'sales'.</span></span>
2. <span data-ttu-id="16b4e-130">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="16b4e-130">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="16b4e-131">Udvid 'en kategorinode' i træet.</span><span class="sxs-lookup"><span data-stu-id="16b4e-131">In the tree, expand 'a category node'.</span></span>
    * <span data-ttu-id="16b4e-132">Udvid for eksempel 'Sales hierarchy\Home audio'.</span><span class="sxs-lookup"><span data-stu-id="16b4e-132">For example, expand 'Sales hierarchy\Home audio'.</span></span>  
4. <span data-ttu-id="16b4e-133">Vælg 'kategori, som skal tildeles varekoden' i træet.</span><span class="sxs-lookup"><span data-stu-id="16b4e-133">In the tree, select 'the category to assign to the commodity code'.</span></span>
    * <span data-ttu-id="16b4e-134">Vælg for eksempel 'Sales hierarchy\Home audio\Speakers'.</span><span class="sxs-lookup"><span data-stu-id="16b4e-134">For example, select 'Sales hierarchy\Home audio\Speakers.</span></span>  
5. <span data-ttu-id="16b4e-135">Udvid sektionen Varekoder.</span><span class="sxs-lookup"><span data-stu-id="16b4e-135">Expand the Commodity codes section.</span></span>
6. <span data-ttu-id="16b4e-136">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="16b4e-136">Click Add.</span></span>
7. <span data-ttu-id="16b4e-137">Vælg 'Intrastat' i feltet Vælg hierarki.</span><span class="sxs-lookup"><span data-stu-id="16b4e-137">In the Select hierarchy field, select 'Intrastat'.</span></span>
8. <span data-ttu-id="16b4e-138">Find og vælg varekoden på listen.</span><span class="sxs-lookup"><span data-stu-id="16b4e-138">In the list, find and select the commodity code</span></span>
    * <span data-ttu-id="16b4e-139">Vælg for eksempel '920 20 34 Speaker'.</span><span class="sxs-lookup"><span data-stu-id="16b4e-139">For example, select '920 20 34 Speaker'.</span></span>  
9. <span data-ttu-id="16b4e-140">Klik på SelectCodes.</span><span class="sxs-lookup"><span data-stu-id="16b4e-140">Click SelectCodes.</span></span>
10. <span data-ttu-id="16b4e-141">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="16b4e-141">Click OK.</span></span>
11. <span data-ttu-id="16b4e-142">Gå til Administration af produktoplysninger > Produkter > Frigivne produkter.</span><span class="sxs-lookup"><span data-stu-id="16b4e-142">Go to Product information management > Products > Released products.</span></span>
12. <span data-ttu-id="16b4e-143">Vælg det frigivne produkt på listen, som du vil tildele til varekoden.</span><span class="sxs-lookup"><span data-stu-id="16b4e-143">In the list, choose the released product that you will assign to the commodity code.</span></span>
    * <span data-ttu-id="16b4e-144">Vælg for eksempel 'D0001'.</span><span class="sxs-lookup"><span data-stu-id="16b4e-144">For example, choose 'D0001'.</span></span>  
13. <span data-ttu-id="16b4e-145">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="16b4e-145">Click Edit.</span></span>
14. <span data-ttu-id="16b4e-146">Udvid sektionen Udenrigshandel.</span><span class="sxs-lookup"><span data-stu-id="16b4e-146">Expand the Foreign trade section.</span></span>
15. <span data-ttu-id="16b4e-147">Indtast varekoden i feltet Vare.</span><span class="sxs-lookup"><span data-stu-id="16b4e-147">In the Commodity field, enter the commodity code</span></span>
    * <span data-ttu-id="16b4e-148">Vælg for eksempel værdien '920 20 34 Speaker'.</span><span class="sxs-lookup"><span data-stu-id="16b4e-148">For example, select value '920 20 34 Speaker'.</span></span>    
16. <span data-ttu-id="16b4e-149">Indtast et tal i feltet Gebyrprocent.</span><span class="sxs-lookup"><span data-stu-id="16b4e-149">In the Charges percentage field, enter a number.</span></span>
    * <span data-ttu-id="16b4e-150">Indtast for eksempel '3'.</span><span class="sxs-lookup"><span data-stu-id="16b4e-150">For example, enter '3'.</span></span>  
17. <span data-ttu-id="16b4e-151">Indtaste eller vælge et land eller område i feltet Land/område</span><span class="sxs-lookup"><span data-stu-id="16b4e-151">In the Country/region field, enter or select a country or region of origin</span></span>
    * <span data-ttu-id="16b4e-152">Vælg for eksempel 'AUT'.</span><span class="sxs-lookup"><span data-stu-id="16b4e-152">For example, select 'AUT'.</span></span>  
18. <span data-ttu-id="16b4e-153">Udvid sektionen Styr lager.</span><span class="sxs-lookup"><span data-stu-id="16b4e-153">Expand the Manage inventory section.</span></span>
19. <span data-ttu-id="16b4e-154">Indtast en vægt i kg i feltet Nettovægt.</span><span class="sxs-lookup"><span data-stu-id="16b4e-154">In the Net weight field, enter a weight in kg.</span></span>
    * <span data-ttu-id="16b4e-155">Indtast for eksempel '2,5'.</span><span class="sxs-lookup"><span data-stu-id="16b4e-155">For example, enter '2.5'.</span></span>  
20. <span data-ttu-id="16b4e-156">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="16b4e-156">Click Save.</span></span>

## <a name="set-up-intrastat-transaction-codes-and-foreign-trade-parameters"></a><span data-ttu-id="16b4e-157">Oprette Intrastat-transaktionkoder og udenrigshandelsparametre</span><span class="sxs-lookup"><span data-stu-id="16b4e-157">Set up Intrastat transaction codes and foreign trade parameters</span></span>
1. <span data-ttu-id="16b4e-158">Gå til Skat > Konfiguration > Udenrigshandel > Transaktionskoder</span><span class="sxs-lookup"><span data-stu-id="16b4e-158">Go to Tax > Setup > Foreign trade > Transaction codes</span></span>
2. <span data-ttu-id="16b4e-159">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="16b4e-159">Click New.</span></span>
3. <span data-ttu-id="16b4e-160">Indtast en værdi i feltet Transaktionskode.</span><span class="sxs-lookup"><span data-stu-id="16b4e-160">In the Transaction code field, type a value.</span></span>
    * <span data-ttu-id="16b4e-161">Indtast for eksempel '21' for den transaktionkode, der anvendes som returværdi.</span><span class="sxs-lookup"><span data-stu-id="16b4e-161">For example, enter '21' for the transaction code used as return.</span></span>  
4. <span data-ttu-id="16b4e-162">Skriv navnet på transaktionskoden i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="16b4e-162">In the Name field, type the name of transaction code.</span></span>
    * <span data-ttu-id="16b4e-163">Indtast for eksempel 'Retur'.</span><span class="sxs-lookup"><span data-stu-id="16b4e-163">For example, enter 'Return'.</span></span>  
5. <span data-ttu-id="16b4e-164">Vælg en indstilling i feltet Statistisk beløb.</span><span class="sxs-lookup"><span data-stu-id="16b4e-164">In the Statistical amount field, select an option.</span></span>
    * <span data-ttu-id="16b4e-165">Vælg for eksempel 'Tom' for at angive, at den statistiske værdi, der skal rapporteres for transaktioner med transaktionskoden "21", altid vil være nul.</span><span class="sxs-lookup"><span data-stu-id="16b4e-165">For example, select 'Empty' which indicates that the Statistical value to be reported for transactions with Transaction code of "21" will always be zero.</span></span>  
6. <span data-ttu-id="16b4e-166">Gå til Skat > Opsætning > Udenrigshandel > Udenrigshandelsparametre</span><span class="sxs-lookup"><span data-stu-id="16b4e-166">Go to Tax > Setup > Foreign trade > Foreign trade parameters</span></span>
7. <span data-ttu-id="16b4e-167">Indtast eller vælg en værdi i feltet Transaktionskode.</span><span class="sxs-lookup"><span data-stu-id="16b4e-167">In the Transaction code field, enter or select a value.</span></span>
    * <span data-ttu-id="16b4e-168">Vælg for eksempel '11'.</span><span class="sxs-lookup"><span data-stu-id="16b4e-168">For example, select '11'.</span></span>  
8. <span data-ttu-id="16b4e-169">Indtast eller vælg en værdi i feltet Kreditnota.</span><span class="sxs-lookup"><span data-stu-id="16b4e-169">In the Credit note field, enter or select a value.</span></span>
    * <span data-ttu-id="16b4e-170">Denne værdi identificerer også fysisk returnering.</span><span class="sxs-lookup"><span data-stu-id="16b4e-170">This value also identifies the physical return.</span></span> <span data-ttu-id="16b4e-171">Kreditnotaen for den fysiske returnering overføres i Intrastat-kladden med modsat retning.</span><span class="sxs-lookup"><span data-stu-id="16b4e-171">The credit note for the physical return will be transferred in the Intrastat journal with opposite direction.</span></span> <span data-ttu-id="16b4e-172">Returneringen af modtagede varer overføres f.eks. som en forsendelse.</span><span class="sxs-lookup"><span data-stu-id="16b4e-172">For example, the return of arrival is transferred as dispatch.</span></span>   <span data-ttu-id="16b4e-173">Ellers betragtes kreditnotaen som en rettelse, og den overføres med samme retning og modsat fortegn.</span><span class="sxs-lookup"><span data-stu-id="16b4e-173">Otherwise, the credit note is considered a correction and is transferred with the same direction and opposite sign.</span></span> <span data-ttu-id="16b4e-174">Korrektion af varemodtagelse overføres f.eks. som en modtagelse med et negativt beløb og det aktive flag er indstillet til "Korrektion".</span><span class="sxs-lookup"><span data-stu-id="16b4e-174">For example, the correction of arrival is transferred as an arrival with negative amount and the active flag is set to "Correction".</span></span>  
9. <span data-ttu-id="16b4e-175">Udvid sektionen Overførsel.</span><span class="sxs-lookup"><span data-stu-id="16b4e-175">Expand the Transfer section.</span></span>
10. <span data-ttu-id="16b4e-176">Vælg Ja i feltet Varer med varekode.</span><span class="sxs-lookup"><span data-stu-id="16b4e-176">Select Yes in the Items with commodity code field.</span></span>
    * <span data-ttu-id="16b4e-177">Vælg denne indstilling for at overføre transaktionerne med en tildelt varekode.</span><span class="sxs-lookup"><span data-stu-id="16b4e-177">Select this option to transfer only the transactions with a commodity code assigned.</span></span> <span data-ttu-id="16b4e-178">Transaktioner uden en varekode bliver ikke overført til Intrastat.</span><span class="sxs-lookup"><span data-stu-id="16b4e-178">Transactions without a commodity code won't be transferred to Intrastat.</span></span>  
11. <span data-ttu-id="16b4e-179">Vælg en indstilling i feltet Overfør ved opfyldelse af kriterium på.</span><span class="sxs-lookup"><span data-stu-id="16b4e-179">In the Transfer when meeting criterion for field, select an option.</span></span>
    * <span data-ttu-id="16b4e-180">Vælg for eksempel 'En af de valgte'.</span><span class="sxs-lookup"><span data-stu-id="16b4e-180">For example, select 'One of the selected'.</span></span>  
12. <span data-ttu-id="16b4e-181">Udvid sektionen Varekodehierarki.</span><span class="sxs-lookup"><span data-stu-id="16b4e-181">Expand the Commodity code hierarchy section.</span></span>
13. <span data-ttu-id="16b4e-182">Klik på fanen Egenskaber for land/område.</span><span class="sxs-lookup"><span data-stu-id="16b4e-182">Click the Country/region properties tab.</span></span>
14. <span data-ttu-id="16b4e-183">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="16b4e-183">Click New.</span></span>
15. <span data-ttu-id="16b4e-184">Indtast eller vælg en værdi i feltet Land/område.</span><span class="sxs-lookup"><span data-stu-id="16b4e-184">In the Country/region field, enter or select a value.</span></span>
    * <span data-ttu-id="16b4e-185">Vælg for eksempel værdien 'FRA'.</span><span class="sxs-lookup"><span data-stu-id="16b4e-185">For example, select the value 'FRA'.</span></span>  
16. <span data-ttu-id="16b4e-186">I feltet Intrastat-kode skal du angive ISO-koden for landet/området.</span><span class="sxs-lookup"><span data-stu-id="16b4e-186">In the Intrastat code field, enter the ISO code for the country.</span></span>
    * <span data-ttu-id="16b4e-187">Skriv for eksempel 'FR'.</span><span class="sxs-lookup"><span data-stu-id="16b4e-187">For example, type 'FR'.</span></span>  
17. <span data-ttu-id="16b4e-188">Vælg "EU" i feltet Lande-/områdetype.</span><span class="sxs-lookup"><span data-stu-id="16b4e-188">In the Country/region type field, select 'EU'.</span></span>
18. <span data-ttu-id="16b4e-189">Klik på fanen Nummerserier.</span><span class="sxs-lookup"><span data-stu-id="16b4e-189">Click the Number sequences tab.</span></span>

## <a name="set-up-modes-of-delivery-and-rules-for-including-charges-in-intrastat"></a><span data-ttu-id="16b4e-190">Konfigurere leveringsmåder og regler for at medtage gebyrer i Intrastat</span><span class="sxs-lookup"><span data-stu-id="16b4e-190">Set up Modes of delivery and rules for including charges in Intrastat</span></span>
1. <span data-ttu-id="16b4e-191">Gå til Salg og marketing > Konfiguration > Distribution > Leveringsmåder</span><span class="sxs-lookup"><span data-stu-id="16b4e-191">Go to Sales and marketing > Setup > Distribution > Modes of delivery</span></span>
2. <span data-ttu-id="16b4e-192">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="16b4e-192">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="16b4e-193">Vælg for eksempel '20 Air'.</span><span class="sxs-lookup"><span data-stu-id="16b4e-193">For example, select '20 Air'.</span></span>  
3. <span data-ttu-id="16b4e-194">Udvid sektionen Udenrigshandel.</span><span class="sxs-lookup"><span data-stu-id="16b4e-194">Expand the Foreign trade section.</span></span>
4. <span data-ttu-id="16b4e-195">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="16b4e-195">Click Edit.</span></span>
5. <span data-ttu-id="16b4e-196">Indtast eller vælg en værdi i feltet Transport.</span><span class="sxs-lookup"><span data-stu-id="16b4e-196">In the Transport field, enter or select a value.</span></span>
    * <span data-ttu-id="16b4e-197">Vælg for eksempel '02'.</span><span class="sxs-lookup"><span data-stu-id="16b4e-197">For example, select '02'.</span></span>  
6. <span data-ttu-id="16b4e-198">Gå til Debitor > Konfiguration af gebyrer > Gebyrkode.</span><span class="sxs-lookup"><span data-stu-id="16b4e-198">Go to Accounts receivable > Charges setup > Charges code.</span></span>
7. <span data-ttu-id="16b4e-199">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="16b4e-199">Use the Quick Filter to find records.</span></span> <span data-ttu-id="16b4e-200">Filtrer for eksempel efter feltet Gebyrkode med værdien 'fragt'.</span><span class="sxs-lookup"><span data-stu-id="16b4e-200">For example, filter on the Charges code field with a value of 'freight'.</span></span>
8. <span data-ttu-id="16b4e-201">Udvid sektionen Udenrigshandel.</span><span class="sxs-lookup"><span data-stu-id="16b4e-201">Expand the Foreign trade section.</span></span>
9. <span data-ttu-id="16b4e-202">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="16b4e-202">Click Edit.</span></span>
10. <span data-ttu-id="16b4e-203">Vælg Ja i feltet Intrastat-fakturaværdi.</span><span class="sxs-lookup"><span data-stu-id="16b4e-203">Select Yes in the Intrastat invoice value field.</span></span>
    * <span data-ttu-id="16b4e-204">Beløbet vil blive overført til feltet Fakturagebyrer og lægges til det beløb, der er overført i feltet Fakturabeløb.</span><span class="sxs-lookup"><span data-stu-id="16b4e-204">The amount will be transferred to the  Invoice charges field and will be summarized with the amount transferred in the Invoice amount field.</span></span>    <span data-ttu-id="16b4e-205">Vælg Ja i feltet Værdi af Intrastat-statistik, hvis antallet af ændringer skal overføres til feltet Statistiske gebyrbeløb og lægges til Statistisk beløb.</span><span class="sxs-lookup"><span data-stu-id="16b4e-205">Select Yes in the Intrastat statistical value field if the amount of changes need to be transferred to the field Statistical charges and summarized with Statistical amount.</span></span>  

## <a name="sell-products-for-eu-customers"></a><span data-ttu-id="16b4e-206">Sælge produkter til EU-debitorer</span><span class="sxs-lookup"><span data-stu-id="16b4e-206">Sell products for EU customers</span></span>
1. <span data-ttu-id="16b4e-207">Gå til Debitor > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="16b4e-207">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="16b4e-208">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="16b4e-208">Click New.</span></span>
3. <span data-ttu-id="16b4e-209">Vælg en EU-debitor i feltet Debitorkonto.</span><span class="sxs-lookup"><span data-stu-id="16b4e-209">In the Customer account field, select an EU customer</span></span>
    * <span data-ttu-id="16b4e-210">Vælg for eksempel "DE-012 Litware Retail".</span><span class="sxs-lookup"><span data-stu-id="16b4e-210">For example, select "DE-012 Litware Retail".</span></span>  
4. <span data-ttu-id="16b4e-211">Udvid sektionen Levering.</span><span class="sxs-lookup"><span data-stu-id="16b4e-211">Expand the Delivery section.</span></span>
5. <span data-ttu-id="16b4e-212">Indtast eller vælg en værdi i feltet Leveringsmåde.</span><span class="sxs-lookup"><span data-stu-id="16b4e-212">In the Mode of delivery field, enter or select a value.</span></span>
    * <span data-ttu-id="16b4e-213">Vælg for eksempel '20 Air'.</span><span class="sxs-lookup"><span data-stu-id="16b4e-213">For example, select '20 Air'.</span></span>  
6. <span data-ttu-id="16b4e-214">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="16b4e-214">Click OK.</span></span>
7. <span data-ttu-id="16b4e-215">Placer markøren på den første række af salgsordrelinjer.</span><span class="sxs-lookup"><span data-stu-id="16b4e-215">Place the cursor on the first row of sales order lines.</span></span>
8. <span data-ttu-id="16b4e-216">Indtast eller vælg en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="16b4e-216">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="16b4e-217">Vælg for eksempel 'D001'.</span><span class="sxs-lookup"><span data-stu-id="16b4e-217">For example, select 'D001'.</span></span>  
9. <span data-ttu-id="16b4e-218">Vis eller skjul sektionen Linjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="16b4e-218">Expand the Line details section.</span></span>
10. <span data-ttu-id="16b4e-219">Klik på fanen Udenrigshandel.</span><span class="sxs-lookup"><span data-stu-id="16b4e-219">Click the Foreign trade tab.</span></span>
    * <span data-ttu-id="16b4e-220">Transporten udfyldes automatisk fra den valgte leveringsmåde.</span><span class="sxs-lookup"><span data-stu-id="16b4e-220">The transport is filled automatically from the chosen Mode of delivery.</span></span>  
11. <span data-ttu-id="16b4e-221">Indtast eller vælg en værdi i feltet Havn.</span><span class="sxs-lookup"><span data-stu-id="16b4e-221">In the Port field, enter or select a value.</span></span>
12. <span data-ttu-id="16b4e-222">Klik på Finans.</span><span class="sxs-lookup"><span data-stu-id="16b4e-222">Click Financials.</span></span>
    * <span data-ttu-id="16b4e-223">I henhold til indstillingerne skal dette beløb medtages i Intrastat-fakturaværdi.</span><span class="sxs-lookup"><span data-stu-id="16b4e-223">As per the settings, this amount will be included in Intrastat invoice value.</span></span>  
13. <span data-ttu-id="16b4e-224">Klik på Vedligehold gebyrer.</span><span class="sxs-lookup"><span data-stu-id="16b4e-224">Click Maintain charges.</span></span>
14. <span data-ttu-id="16b4e-225">Indtast eller vælg en værdi i feltet Gebyrkode.</span><span class="sxs-lookup"><span data-stu-id="16b4e-225">In the Charges code field, enter or select a value.</span></span>
    * <span data-ttu-id="16b4e-226">Vælg for eksempel 'FREIGHT'.</span><span class="sxs-lookup"><span data-stu-id="16b4e-226">For example, select 'FREIGHT'.</span></span>  
15. <span data-ttu-id="16b4e-227">Marker afkrydsningsfeltet Behold.</span><span class="sxs-lookup"><span data-stu-id="16b4e-227">Select the Keep check box.</span></span>
16. <span data-ttu-id="16b4e-228">Indtast et tal i feltet Gebyrværdi.</span><span class="sxs-lookup"><span data-stu-id="16b4e-228">In the Charges value field, enter a number.</span></span>
    * <span data-ttu-id="16b4e-229">Indtast for eksempel '10'.</span><span class="sxs-lookup"><span data-stu-id="16b4e-229">For example, enter '10'.</span></span>  
17. <span data-ttu-id="16b4e-230">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="16b4e-230">Click Save.</span></span>
18. <span data-ttu-id="16b4e-231">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="16b4e-231">Close the page.</span></span>
19. <span data-ttu-id="16b4e-232">Klik på Faktura i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="16b4e-232">On the Action Pane, click Invoice.</span></span>
20. <span data-ttu-id="16b4e-233">Klik på Faktura.</span><span class="sxs-lookup"><span data-stu-id="16b4e-233">Click Invoice.</span></span>
21. <span data-ttu-id="16b4e-234">Udvid sektionen Parametre.</span><span class="sxs-lookup"><span data-stu-id="16b4e-234">Expand the Parameters section.</span></span>
22. <span data-ttu-id="16b4e-235">Vælg "Alle" i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="16b4e-235">In the Quantity field, select 'All'.</span></span>
23. <span data-ttu-id="16b4e-236">Udvid sektionen Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="16b4e-236">Expand the Setup section.</span></span>
24. <span data-ttu-id="16b4e-237">Indtast en dato i feltet Fakturadato.</span><span class="sxs-lookup"><span data-stu-id="16b4e-237">In the Invoice date field, enter a date.</span></span>
    * <span data-ttu-id="16b4e-238">Indtast for eksempel '2015-01-31'.</span><span class="sxs-lookup"><span data-stu-id="16b4e-238">For example, enter '2015-01-31'.</span></span>  
25. <span data-ttu-id="16b4e-239">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="16b4e-239">Click OK.</span></span>
26. <span data-ttu-id="16b4e-240">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="16b4e-240">Click OK.</span></span>
27. <span data-ttu-id="16b4e-241">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="16b4e-241">Close the page.</span></span>
28. <span data-ttu-id="16b4e-242">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="16b4e-242">Click New.</span></span>
29. <span data-ttu-id="16b4e-243">Vælg en EU-debitor i feltet Debitorkonto.</span><span class="sxs-lookup"><span data-stu-id="16b4e-243">In the Customer account field, select an EU customer.</span></span>
    * <span data-ttu-id="16b4e-244">Vælg for eksempel 'DE-013 Trey Wholesales'.</span><span class="sxs-lookup"><span data-stu-id="16b4e-244">For example, select 'DE-013 Trey Wholesales'</span></span>  
30. <span data-ttu-id="16b4e-245">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="16b4e-245">Click OK.</span></span>
31. <span data-ttu-id="16b4e-246">Indtast eller vælg en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="16b4e-246">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="16b4e-247">Vælg for eksempel 'D0001'.</span><span class="sxs-lookup"><span data-stu-id="16b4e-247">For example, select 'D0001'.</span></span>  
32. <span data-ttu-id="16b4e-248">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="16b4e-248">Click Save.</span></span>
33. <span data-ttu-id="16b4e-249">Klik på Faktura.</span><span class="sxs-lookup"><span data-stu-id="16b4e-249">Click Invoice.</span></span>
34. <span data-ttu-id="16b4e-250">Indtast en dato i feltet Fakturadato.</span><span class="sxs-lookup"><span data-stu-id="16b4e-250">In the Invoice date field, enter a date.</span></span>
    * <span data-ttu-id="16b4e-251">Indtast for eksempel datoen '2015-01-31'.</span><span class="sxs-lookup"><span data-stu-id="16b4e-251">For example, enter the date '2015-01-31'.</span></span>  
35. <span data-ttu-id="16b4e-252">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="16b4e-252">Click OK.</span></span>
36. <span data-ttu-id="16b4e-253">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="16b4e-253">Click OK.</span></span>

## <a name="transfer-transactions-to-the-intrastat"></a><span data-ttu-id="16b4e-254">Overføre posteringer til Intrastat</span><span class="sxs-lookup"><span data-stu-id="16b4e-254">Transfer transactions to the Intrastat</span></span>
1. <span data-ttu-id="16b4e-255">Gå til Skat > Erklæringer > Udenrigshandel > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="16b4e-255">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
2. <span data-ttu-id="16b4e-256">Klik på Overførsel.</span><span class="sxs-lookup"><span data-stu-id="16b4e-256">Click Transfer.</span></span>
3. <span data-ttu-id="16b4e-257">Vælg Ja i feltet Debitorfaktura.</span><span class="sxs-lookup"><span data-stu-id="16b4e-257">Select Yes in the Customer invoice field.</span></span>
4. <span data-ttu-id="16b4e-258">Klik på Filtrér.</span><span class="sxs-lookup"><span data-stu-id="16b4e-258">Click Filter.</span></span>
5. <span data-ttu-id="16b4e-259">Markér rækken Dato på listen.</span><span class="sxs-lookup"><span data-stu-id="16b4e-259">In the list, mark the row with Date</span></span>
6. <span data-ttu-id="16b4e-260">Skriv en værdi i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="16b4e-260">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="16b4e-261">Angiv for eksempel filteret for perioden januar 2015 (den nøjagtige værdi afhænger af dit datoformat): 1/1/2015..31/1/2015</span><span class="sxs-lookup"><span data-stu-id="16b4e-261">For example, enter the filter for the period January 2015 (the exact value depends on your date format): 1/1/2015..1/31/2015</span></span>  
7. <span data-ttu-id="16b4e-262">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="16b4e-262">Click OK.</span></span>
8. <span data-ttu-id="16b4e-263">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="16b4e-263">Click OK.</span></span>
9. <span data-ttu-id="16b4e-264">Find og vælg den overførte post på listen.</span><span class="sxs-lookup"><span data-stu-id="16b4e-264">In the list, find and selected the transferred record.</span></span>
10. <span data-ttu-id="16b4e-265">Klik på fanen Generelt.</span><span class="sxs-lookup"><span data-stu-id="16b4e-265">Click the General tab.</span></span>
    * <span data-ttu-id="16b4e-266">Gennemse overførte data, herunder land/område for destination/afsendelse, oprindelsesland/område, vægt, antal, antal i supplerende enheder, varekode, transaktionskode, fakturabeløb og statistiske beløb.</span><span class="sxs-lookup"><span data-stu-id="16b4e-266">Review transferred data, including country\region of destination/dispatch, country of origin, weight, quantity, quantity in additional units, commodity, transaction code, invoice amounts and statistical amounts.</span></span>   <span data-ttu-id="16b4e-267">Du kan ændre data, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="16b4e-267">You can modify data if necessary.</span></span>  

