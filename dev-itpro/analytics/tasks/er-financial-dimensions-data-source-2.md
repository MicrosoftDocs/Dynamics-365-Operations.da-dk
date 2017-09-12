--- 
title: "Tilknytte modeller til at bruge økonomiske dimensioner som en datakilde til elektronisk rapportering (ER)"
description: "Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at bruge økonomiske dimensioner so datakilde for ER-rapporter."
author: NickSelin
manager: AnnBe
ms.date: 10/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 58a0ce881e5cb8d459256244a144cf51dc357299
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---
# <a name="map-models--to-use-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a><span data-ttu-id="2401c-103">Tilknytte modeller til at bruge økonomiske dimensioner som en datakilde til elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="2401c-103">Map models  to use financial dimensions as a data source for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2401c-104">Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at bruge økonomiske dimensioner so datakilde for ER-rapporter.</span><span class="sxs-lookup"><span data-stu-id="2401c-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="2401c-105">Disse trin kan udføres i en hvilken som helst virksomhed.</span><span class="sxs-lookup"><span data-stu-id="2401c-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="2401c-106">For at fuldføre disse trin skal du først udføre trinnene i proceduren den "ER-brug af økonomiske dimensioner som datakilde (del 1: Design datamodel)".</span><span class="sxs-lookup"><span data-stu-id="2401c-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 1: Design data model” procedure.</span></span>


## <a name="add-required-data-sources-to-model-mapping"></a><span data-ttu-id="2401c-107">Føj nødvendige datakilder til modeltilknytning</span><span class="sxs-lookup"><span data-stu-id="2401c-107">Add required data sources to model mapping</span></span>
1. <span data-ttu-id="2401c-108">Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="2401c-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="2401c-109">Vælg 'Eksempelmodel til økonomiske dimensioner' i træet.</span><span class="sxs-lookup"><span data-stu-id="2401c-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="2401c-110">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="2401c-110">Click Designer.</span></span>
4. <span data-ttu-id="2401c-111">Klik på Tilknyt model til datakilde.</span><span class="sxs-lookup"><span data-stu-id="2401c-111">Click Map model to datasource.</span></span>
5. <span data-ttu-id="2401c-112">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="2401c-112">Click New.</span></span>
6. <span data-ttu-id="2401c-113">Vælg Post i feltet Definition.</span><span class="sxs-lookup"><span data-stu-id="2401c-113">In the Definition field, select Entry.</span></span>
7. <span data-ttu-id="2401c-114">Skriv 'Datatilknytning for dimensioner' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="2401c-114">In the Name field, type 'Dimensions data mapping'.</span></span>
8. <span data-ttu-id="2401c-115">Skriv 'Datatilknytning for dimensioner' i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="2401c-115">In the Description field, type 'Dimensions data mapping'.</span></span>
9. <span data-ttu-id="2401c-116">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="2401c-116">Click Save.</span></span>
10. <span data-ttu-id="2401c-117">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="2401c-117">Click Designer.</span></span>
11. <span data-ttu-id="2401c-118">Vælg 'Dynamics 365 for Operations\Tabel' i træet.</span><span class="sxs-lookup"><span data-stu-id="2401c-118">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
12. <span data-ttu-id="2401c-119">Klik på Tilføj rod.</span><span class="sxs-lookup"><span data-stu-id="2401c-119">Click Add root.</span></span>
13. <span data-ttu-id="2401c-120">Skriv "Firma" feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="2401c-120">In the Name field, type 'Company'.</span></span>
14. <span data-ttu-id="2401c-121">Skriv "CompanyInfo" i feltet Tabel.</span><span class="sxs-lookup"><span data-stu-id="2401c-121">In the Table field, type 'CompanyInfo'.</span></span>
15. <span data-ttu-id="2401c-122">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="2401c-122">Click OK.</span></span>
16. <span data-ttu-id="2401c-123">Vælg 'Funktioner\Oplysninger om økonomiske dimensioner'.</span><span class="sxs-lookup"><span data-stu-id="2401c-123">In the tree, select 'Functions\Financial dimensions details'.</span></span>
17. <span data-ttu-id="2401c-124">Klik på Tilføj rod.</span><span class="sxs-lookup"><span data-stu-id="2401c-124">Click Add root.</span></span>
    * <span data-ttu-id="2401c-125">Denne datakilde angiver, hvordan omfanget af økonomiske dimensioner defineres for en rapport, der bruger denne model som datakilde.</span><span class="sxs-lookup"><span data-stu-id="2401c-125">This data source specifies how the scope of financial dimensions will be defined for any report that will use this model as a data source.</span></span>  
18. <span data-ttu-id="2401c-126">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="2401c-126">In the Name field, type a value.</span></span>
19. <span data-ttu-id="2401c-127">Vælg Ja i feltet Spørg efter dimensioner.</span><span class="sxs-lookup"><span data-stu-id="2401c-127">Select Yes in the Ask for dimensions field.</span></span>
    * <span data-ttu-id="2401c-128">Vælg Ja for at tillade brugeren at vælge dimensioner på kørselstidspunktet i formen Brugerdialogboks.</span><span class="sxs-lookup"><span data-stu-id="2401c-128">Select Yes to allow the user to select dimensions at run-time on the User dialog form.</span></span> <span data-ttu-id="2401c-129">Hvis indstillingen er angivet til Nej, bruges alle økonomiske dimensioner for den aktuelle forekomst som standard.</span><span class="sxs-lookup"><span data-stu-id="2401c-129">If set to No, all financial dimensions of the current instance will be used by default.</span></span>  
20. <span data-ttu-id="2401c-130">Vælg 'Juridisk enhed' i feltet Valg af økonomiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="2401c-130">In the Financial dimensions selection field, select 'Legal entity'.</span></span>
    * <span data-ttu-id="2401c-131">Vælg Alle for at tillade brugeren at vælge de ønskede dimensioner for den aktuelle forekomst i opslagsfeltet.</span><span class="sxs-lookup"><span data-stu-id="2401c-131">Select All to allow the user to select desire dimensions for the current  instance in the Lookup field.</span></span>  <span data-ttu-id="2401c-132">Vælg Juridisk enhed for at tillade brugeren at vælge dimensioner for firmaet i opslagsfeltet.</span><span class="sxs-lookup"><span data-stu-id="2401c-132">Select Legal entity to allow the user to select dimensions for the company in the Lookup field.</span></span>  <span data-ttu-id="2401c-133">Vælg Dimension for at tillade brugeren at vælge dimensioner ved hjælp af et enkelt dimensionssæt.</span><span class="sxs-lookup"><span data-stu-id="2401c-133">Select Dimension to allow the user to select dimensions using a single dimension set.</span></span>  
21. <span data-ttu-id="2401c-134">Vælg Ja i feltet Spørg efter hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="2401c-134">Select Yes in the Ask for main account field.</span></span>
    * <span data-ttu-id="2401c-135">Angiv 'Spørg efter hovedkonto' til Ja for at tillade brugere at vælge hovedkontoen som en del af listen over dimensioner.</span><span class="sxs-lookup"><span data-stu-id="2401c-135">Set ‘Ask for main account’ to Yes to allow users to select the main account as part of the list of dimensions.</span></span>   <span data-ttu-id="2401c-136">Hvis indstillingen er angivet til Nej, inkluderes den primære konto ikke på listen over dimensioner, og indstillingen 'Er hovedkonto obligatorisk' er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="2401c-136">If set to No, the main account will not be included to the list of dimensions and the ‘Is main account mandatory’ option is enabled.</span></span> <span data-ttu-id="2401c-137">Hvis "Er hovedkonto obligatorisk" er angivet til Ja, skal du inkludere hovedkontoen på listen over dimensioner, uanset brugerens valg.</span><span class="sxs-lookup"><span data-stu-id="2401c-137">If “Is main account mandatory’ is set to Yes, include the main account in the list of dimensions regardless of the user’s selection.</span></span>  
22. <span data-ttu-id="2401c-138">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="2401c-138">Click OK.</span></span>
23. <span data-ttu-id="2401c-139">Vælg 'Dynamics 365 for Operations\Tabelposter' i træet.</span><span class="sxs-lookup"><span data-stu-id="2401c-139">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
24. <span data-ttu-id="2401c-140">Klik på Tilføj rod.</span><span class="sxs-lookup"><span data-stu-id="2401c-140">Click Add root.</span></span>
25. <span data-ttu-id="2401c-141">Skriv "LedgerJournal" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="2401c-141">In the Name field, type 'LedgerJournal'.</span></span>
26. <span data-ttu-id="2401c-142">Vælg Ja i feltet Spørg efter forespørgsel.</span><span class="sxs-lookup"><span data-stu-id="2401c-142">Select Yes in the Ask for query field.</span></span>
27. <span data-ttu-id="2401c-143">Skriv "LedgerJournalTable" i feltet Tabel.</span><span class="sxs-lookup"><span data-stu-id="2401c-143">In the Table field, type 'LedgerJournalTable'.</span></span>
28. <span data-ttu-id="2401c-144">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="2401c-144">Click OK.</span></span>

## <a name="map-data-model-elements-to-added-data-sources"></a><span data-ttu-id="2401c-145">Tilknyt datamodelelementer til tilføjede datakilder</span><span class="sxs-lookup"><span data-stu-id="2401c-145">Map data model elements to added data sources</span></span>
1. <span data-ttu-id="2401c-146">Udvid 'Kladde' i træet.</span><span class="sxs-lookup"><span data-stu-id="2401c-146">In the tree, expand 'Journal'.</span></span>
2. <span data-ttu-id="2401c-147">Udvid 'Kladde\Transaktion' i træet.</span><span class="sxs-lookup"><span data-stu-id="2401c-147">In the tree, expand 'Journal\Transaction'.</span></span>
3. <span data-ttu-id="2401c-148">Udvid 'Kladde\Transaktion\Dimensionsdata' i træet.</span><span class="sxs-lookup"><span data-stu-id="2401c-148">In the tree, expand 'Journal\Transaction\Dimensions data'.</span></span>
4. <span data-ttu-id="2401c-149">Udvid eller skjul 'Dimensionsindstilling' i træet.</span><span class="sxs-lookup"><span data-stu-id="2401c-149">In the tree, expand 'Dimensions setting'.</span></span>
5. <span data-ttu-id="2401c-150">Udvid eller skjul 'LedgerJournal' i træet.</span><span class="sxs-lookup"><span data-stu-id="2401c-150">In the tree, expand 'LedgerJournal'.</span></span>
6. <span data-ttu-id="2401c-151">Udvid 'LedgerJournal\<Relations' i træet.</span><span class="sxs-lookup"><span data-stu-id="2401c-151">In the tree, expand 'LedgerJournal\<Relations'.</span></span>
7. <span data-ttu-id="2401c-152">Udvid 'LedgerJournal\<Relations\LedgerJournalTrans' i træet.</span><span class="sxs-lookup"><span data-stu-id="2401c-152">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
8. <span data-ttu-id="2401c-153">Vælg 'LedgerJournal\<Relations\LedgerJournalTrans\Voucher' i træet.</span><span class="sxs-lookup"><span data-stu-id="2401c-153">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Voucher'.</span></span>
9. <span data-ttu-id="2401c-154">Vælg 'Journal\Transaction\Voucher' i træet.</span><span class="sxs-lookup"><span data-stu-id="2401c-154">In the tree, select 'Journal\Transaction\Voucher'.</span></span>
10. <span data-ttu-id="2401c-155">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="2401c-155">Click Bind.</span></span>
11. <span data-ttu-id="2401c-156">Vælg 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)' i træet.</span><span class="sxs-lookup"><span data-stu-id="2401c-156">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
    * <span data-ttu-id="2401c-157">Bemærk, at for en hvilken som helst henvisning til økonomiske dimensioner, der f.eks. er angivet til LedgerDimension, er et tilsvarende datakildeelement tilgængeligt (LedgerDimension.Dimension).</span><span class="sxs-lookup"><span data-stu-id="2401c-157">Note that for any reference to financial dimensions that is set to, for instance, LedgerDimension, a corresponding data source item is available (LedgerDimension.Dimension).</span></span> <span data-ttu-id="2401c-158">Dette datakildeelement indeholder de økonomiske dimensioner for de dimensioner, der er angivet som postens liste.</span><span class="sxs-lookup"><span data-stu-id="2401c-158">This data source item offers the financial dimensions of that dimensions set as the record’s list.</span></span>  
12. <span data-ttu-id="2401c-159">Udvid 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)' i træet.</span><span class="sxs-lookup"><span data-stu-id="2401c-159">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
13. <span data-ttu-id="2401c-160">Udvid 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hovedkonto og dimensioner' i træet.</span><span class="sxs-lookup"><span data-stu-id="2401c-160">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
14. <span data-ttu-id="2401c-161">Udvid 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hovedkonto og dimensioner\Værdi' i træet.</span><span class="sxs-lookup"><span data-stu-id="2401c-161">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value'.</span></span>
15. <span data-ttu-id="2401c-162">Udvid 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hovedkonto og dimensioner\Definition' i træet.</span><span class="sxs-lookup"><span data-stu-id="2401c-162">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition'.</span></span>
16. <span data-ttu-id="2401c-163">Vælg 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hovedkonto og dimensioner\Definition\Navn' i træet.</span><span class="sxs-lookup"><span data-stu-id="2401c-163">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name'.</span></span>
17. <span data-ttu-id="2401c-164">Vælg 'Kladde\Transaktion\Dimensionsdata\Navn' i træet.</span><span class="sxs-lookup"><span data-stu-id="2401c-164">In the tree, select 'Journal\Transaction\Dimensions data\Name'.</span></span>
18. <span data-ttu-id="2401c-165">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="2401c-165">Click Bind.</span></span>
19. <span data-ttu-id="2401c-166">Vælg 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hovedkonto og dimensioner\Værdi\Beskrivelse' i træet.</span><span class="sxs-lookup"><span data-stu-id="2401c-166">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description'.</span></span>
20. <span data-ttu-id="2401c-167">Vælg 'Kladde\Transaktion\Dimensionsdata\Beskrivelse' i træet.</span><span class="sxs-lookup"><span data-stu-id="2401c-167">In the tree, select 'Journal\Transaction\Dimensions data\Description'.</span></span>
21. <span data-ttu-id="2401c-168">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="2401c-168">Click Bind.</span></span>
22. <span data-ttu-id="2401c-169">Vælg 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hovedkonto og dimensioner\Værdi\Kode' i træet.</span><span class="sxs-lookup"><span data-stu-id="2401c-169">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code'.</span></span>
23. <span data-ttu-id="2401c-170">Vælg 'Kladde\Transaktion\Dimensionsdata\Kode' i træet.</span><span class="sxs-lookup"><span data-stu-id="2401c-170">In the tree, select 'Journal\Transaction\Dimensions data\Code'.</span></span>
24. <span data-ttu-id="2401c-171">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="2401c-171">Click Bind.</span></span>
25. <span data-ttu-id="2401c-172">Vælg 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hovedkonto og dimensioner' i træet.</span><span class="sxs-lookup"><span data-stu-id="2401c-172">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
26. <span data-ttu-id="2401c-173">Vælg 'Kladde\Transaktion\Dimensionsdata' i træet.</span><span class="sxs-lookup"><span data-stu-id="2401c-173">In the tree, select 'Journal\Transaction\Dimensions data'.</span></span>
27. <span data-ttu-id="2401c-174">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="2401c-174">Click Bind.</span></span>
28. <span data-ttu-id="2401c-175">Vælg 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)' i træet.</span><span class="sxs-lookup"><span data-stu-id="2401c-175">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)'.</span></span>
29. <span data-ttu-id="2401c-176">Vælg 'Journal\Transaction\Debit' i træet.</span><span class="sxs-lookup"><span data-stu-id="2401c-176">In the tree, select 'Journal\Transaction\Debit'.</span></span>
30. <span data-ttu-id="2401c-177">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="2401c-177">Click Bind.</span></span>
31. <span data-ttu-id="2401c-178">Vælg 'LedgerJournal\\<Relations\LedgerJournalTrans\Date(TransDate)' i træet.</span><span class="sxs-lookup"><span data-stu-id="2401c-178">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)'.</span></span>
32. <span data-ttu-id="2401c-179">Vælg 'Journal\Transaction\Date' i træet.</span><span class="sxs-lookup"><span data-stu-id="2401c-179">In the tree, select 'Journal\Transaction\Date'.</span></span>
33. <span data-ttu-id="2401c-180">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="2401c-180">Click Bind.</span></span>
34. <span data-ttu-id="2401c-181">Vælg 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)' i træet.</span><span class="sxs-lookup"><span data-stu-id="2401c-181">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)'.</span></span>
35. <span data-ttu-id="2401c-182">Vælg 'Journal\Transaction\Currency' i træet.</span><span class="sxs-lookup"><span data-stu-id="2401c-182">In the tree, select 'Journal\Transaction\Currency'.</span></span>
36. <span data-ttu-id="2401c-183">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="2401c-183">Click Bind.</span></span>
37. <span data-ttu-id="2401c-184">Vælg 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)' i træet.</span><span class="sxs-lookup"><span data-stu-id="2401c-184">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)'.</span></span>
38. <span data-ttu-id="2401c-185">Vælg 'Journal\Transaction\Credit' i træet.</span><span class="sxs-lookup"><span data-stu-id="2401c-185">In the tree, select 'Journal\Transaction\Credit'.</span></span>
39. <span data-ttu-id="2401c-186">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="2401c-186">Click Bind.</span></span>
40. <span data-ttu-id="2401c-187">Vælg 'LedgerJournal\<Relations\LedgerJournalTrans' i træet.</span><span class="sxs-lookup"><span data-stu-id="2401c-187">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
41. <span data-ttu-id="2401c-188">Vælg 'Journal\Transaction' i træet.</span><span class="sxs-lookup"><span data-stu-id="2401c-188">In the tree, select 'Journal\Transaction'.</span></span>
42. <span data-ttu-id="2401c-189">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="2401c-189">Click Bind.</span></span>
43. <span data-ttu-id="2401c-190">Vælg "LedgerJournal\Journalbatchnummer(JournalNum)" i træet.</span><span class="sxs-lookup"><span data-stu-id="2401c-190">In the tree, select 'LedgerJournal\Journal batch number(JournalNum)'.</span></span>
44. <span data-ttu-id="2401c-191">Vælg 'Journal\Batch' i træet.</span><span class="sxs-lookup"><span data-stu-id="2401c-191">In the tree, select 'Journal\Batch'.</span></span>
45. <span data-ttu-id="2401c-192">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="2401c-192">Click Bind.</span></span>
46. <span data-ttu-id="2401c-193">Vælg 'LedgerJournal' i træet.</span><span class="sxs-lookup"><span data-stu-id="2401c-193">In the tree, select 'LedgerJournal'.</span></span>
47. <span data-ttu-id="2401c-194">Vælg 'Journal' i træet.</span><span class="sxs-lookup"><span data-stu-id="2401c-194">In the tree, select 'Journal'.</span></span>
48. <span data-ttu-id="2401c-195">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="2401c-195">Click Bind.</span></span>
49. <span data-ttu-id="2401c-196">Udvid 'Dimensions' i træet.</span><span class="sxs-lookup"><span data-stu-id="2401c-196">In the tree, expand 'Dimensions'.</span></span>
50. <span data-ttu-id="2401c-197">Udvid 'Dimensions\Hovedkonto og dimensioner' i træet.</span><span class="sxs-lookup"><span data-stu-id="2401c-197">In the tree, expand 'Dimensions\Main account and dimensions'.</span></span>
51. <span data-ttu-id="2401c-198">Udvid 'Dimensions\Hovedkonto og dimensioner\Definition' i træet.</span><span class="sxs-lookup"><span data-stu-id="2401c-198">In the tree, expand 'Dimensions\Main account and dimensions\Definition'.</span></span>
52. <span data-ttu-id="2401c-199">Vælg 'Dimensions\Hovedkonto og dimensioner\Definition\Navn' i træet.</span><span class="sxs-lookup"><span data-stu-id="2401c-199">In the tree, select 'Dimensions\Main account and dimensions\Definition\Name'.</span></span>
53. <span data-ttu-id="2401c-200">Vælg 'Dimensionsindstilling\Kode' i træet.</span><span class="sxs-lookup"><span data-stu-id="2401c-200">In the tree, select 'Dimensions setting\Code'.</span></span>
54. <span data-ttu-id="2401c-201">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="2401c-201">Click Bind.</span></span>
55. <span data-ttu-id="2401c-202">Vælg 'Dimensions\Hovedkonto og dimensioner\Definition\Navn på rapportkolonne' i træet.</span><span class="sxs-lookup"><span data-stu-id="2401c-202">In the tree, select 'Dimensions\Main account and dimensions\Definition\Report column name'.</span></span>
56. <span data-ttu-id="2401c-203">Vælg 'Dimensionsindstilling\Navn' i træet.</span><span class="sxs-lookup"><span data-stu-id="2401c-203">In the tree, select 'Dimensions setting\Name'.</span></span>
57. <span data-ttu-id="2401c-204">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="2401c-204">Click Bind.</span></span>
58. <span data-ttu-id="2401c-205">Vælg 'Dimensions\Hovedkonto og dimensioner' i træet.</span><span class="sxs-lookup"><span data-stu-id="2401c-205">In the tree, select 'Dimensions\Main account and dimensions'.</span></span>
59. <span data-ttu-id="2401c-206">Vælg 'Dimensionsindstilling' i træet.</span><span class="sxs-lookup"><span data-stu-id="2401c-206">In the tree, select 'Dimensions setting'.</span></span>
60. <span data-ttu-id="2401c-207">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="2401c-207">Click Bind.</span></span>
61. <span data-ttu-id="2401c-208">Vælg "Firma" i træet.</span><span class="sxs-lookup"><span data-stu-id="2401c-208">In the tree, select 'Company'.</span></span>
62. <span data-ttu-id="2401c-209">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="2401c-209">Click Edit.</span></span>
63. <span data-ttu-id="2401c-210">I feltet expressionAsStringText skal du skrive 'Company.'find()'.'name()''.</span><span class="sxs-lookup"><span data-stu-id="2401c-210">In the expressionAsStringText field, enter 'Company.'find()'.'name()''.</span></span>
    * <span data-ttu-id="2401c-211">Company.'find()'.'name()'</span><span class="sxs-lookup"><span data-stu-id="2401c-211">Company.'find()'.'name()'</span></span>  
64. <span data-ttu-id="2401c-212">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="2401c-212">Click Save.</span></span>
65. <span data-ttu-id="2401c-213">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="2401c-213">Close the page.</span></span>
66. <span data-ttu-id="2401c-214">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="2401c-214">Click Save.</span></span>
67. <span data-ttu-id="2401c-215">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="2401c-215">Close the page.</span></span>

## <a name="complete-this-draft-models-version"></a><span data-ttu-id="2401c-216">Fuldfør denne version af kladdemodellen</span><span class="sxs-lookup"><span data-stu-id="2401c-216">Complete this draft model’s version</span></span>
1. <span data-ttu-id="2401c-217">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="2401c-217">Close the page.</span></span>
2. <span data-ttu-id="2401c-218">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="2401c-218">Close the page.</span></span>
3. <span data-ttu-id="2401c-219">Klik på Skift status.</span><span class="sxs-lookup"><span data-stu-id="2401c-219">Click Change status.</span></span>
4. <span data-ttu-id="2401c-220">Klik på Fuldført.</span><span class="sxs-lookup"><span data-stu-id="2401c-220">Click Complete.</span></span>
5. <span data-ttu-id="2401c-221">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="2401c-221">Click OK.</span></span>


