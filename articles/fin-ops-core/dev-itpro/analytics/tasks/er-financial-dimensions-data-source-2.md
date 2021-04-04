---
title: 'ER Bruge økonomiske dimensioner som en datakilde (del 2: Modeltilknytning)'
description: Dette emne beskriver, hvordan du konfigurerer en ER-model (elektronisk rapportering) til at bruge økonomiske dimensioner som datakilde til ER-rapporter. (Del 2)
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 59f65962ef8f6ae79190b6595a313831eca53830
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570162"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-2---model-mapping"></a><span data-ttu-id="3e0cf-104">ER Bruge økonomiske dimensioner som en datakilde (del 2: Modeltilknytning)</span><span class="sxs-lookup"><span data-stu-id="3e0cf-104">ER Use financial dimensions as a data source (Part 2 - Model mapping)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3e0cf-105">Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at bruge økonomiske dimensioner so datakilde for ER-rapporter.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="3e0cf-106">Disse trin kan udføres i en hvilken som helst virksomhed.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="3e0cf-107">For at fuldføre disse trin skal du først udføre trinnene i proceduren den "ER-brug af økonomiske dimensioner som datakilde (del 1: Design datamodel)".</span><span class="sxs-lookup"><span data-stu-id="3e0cf-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 1: Design data model" procedure.</span></span>


## <a name="add-required-data-sources-to-model-mapping"></a><span data-ttu-id="3e0cf-108">Føj nødvendige datakilder til modeltilknytning</span><span class="sxs-lookup"><span data-stu-id="3e0cf-108">Add required data sources to model mapping</span></span>
1. <span data-ttu-id="3e0cf-109">Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="3e0cf-110">Vælg 'Eksempelmodel til økonomiske dimensioner' i træet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-110">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="3e0cf-111">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-111">Click Designer.</span></span>
4. <span data-ttu-id="3e0cf-112">Klik på Tilknyt model til datakilde.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-112">Click Map model to datasource.</span></span>
5. <span data-ttu-id="3e0cf-113">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-113">Click New.</span></span>
6. <span data-ttu-id="3e0cf-114">Vælg Post i feltet Definition.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-114">In the Definition field, select Entry.</span></span>
7. <span data-ttu-id="3e0cf-115">Skriv 'Datatilknytning for dimensioner' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-115">In the Name field, type 'Dimensions data mapping'.</span></span>
8. <span data-ttu-id="3e0cf-116">Skriv 'Datatilknytning for dimensioner' i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-116">In the Description field, type 'Dimensions data mapping'.</span></span>
9. <span data-ttu-id="3e0cf-117">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-117">Click Save.</span></span>
10. <span data-ttu-id="3e0cf-118">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-118">Click Designer.</span></span>
11. <span data-ttu-id="3e0cf-119">Vælg 'Dynamics 365 for Operations\Tabel' i træet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-119">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
12. <span data-ttu-id="3e0cf-120">Klik på Tilføj rod.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-120">Click Add root.</span></span>
13. <span data-ttu-id="3e0cf-121">Skriv "Firma" feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-121">In the Name field, type 'Company'.</span></span>
14. <span data-ttu-id="3e0cf-122">Skriv "CompanyInfo" i feltet Tabel.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-122">In the Table field, type 'CompanyInfo'.</span></span>
15. <span data-ttu-id="3e0cf-123">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-123">Click OK.</span></span>
16. <span data-ttu-id="3e0cf-124">Vælg 'Funktioner\Oplysninger om økonomiske dimensioner'.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-124">In the tree, select 'Functions\Financial dimensions details'.</span></span>
17. <span data-ttu-id="3e0cf-125">Klik på Tilføj rod.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-125">Click Add root.</span></span>
    * <span data-ttu-id="3e0cf-126">Denne datakilde angiver, hvordan omfanget af økonomiske dimensioner defineres for en rapport, der bruger denne model som datakilde.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-126">This data source specifies how the scope of financial dimensions will be defined for any report that will use this model as a data source.</span></span>  
18. <span data-ttu-id="3e0cf-127">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-127">In the Name field, type a value.</span></span>
19. <span data-ttu-id="3e0cf-128">Vælg Ja i feltet Spørg efter dimensioner.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-128">Select Yes in the Ask for dimensions field.</span></span>
    * <span data-ttu-id="3e0cf-129">Vælg Ja for at tillade brugeren at vælge dimensioner på kørselstidspunktet i formen Brugerdialogboks.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-129">Select Yes to allow the user to select dimensions at run-time on the User dialog form.</span></span> <span data-ttu-id="3e0cf-130">Hvis indstillingen er angivet til Nej, bruges alle økonomiske dimensioner for den aktuelle forekomst som standard.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-130">If set to No, all financial dimensions of the current instance will be used by default.</span></span>  
20. <span data-ttu-id="3e0cf-131">Vælg 'Juridisk enhed' i feltet Valg af økonomiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-131">In the Financial dimensions selection field, select 'Legal entity'.</span></span>
    * <span data-ttu-id="3e0cf-132">Vælg Alle for at tillade brugeren at vælge de ønskede dimensioner for den aktuelle forekomst i opslagsfeltet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-132">Select All to allow the user to select desire dimensions for the current  instance in the Lookup field.</span></span>  <span data-ttu-id="3e0cf-133">Vælg Juridisk enhed for at tillade brugeren at vælge dimensioner for firmaet i opslagsfeltet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-133">Select Legal entity to allow the user to select dimensions for the company in the Lookup field.</span></span>  <span data-ttu-id="3e0cf-134">Vælg Dimension for at tillade brugeren at vælge dimensioner ved hjælp af et enkelt dimensionssæt.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-134">Select Dimension to allow the user to select dimensions using a single dimension set.</span></span>  
21. <span data-ttu-id="3e0cf-135">Vælg Ja i feltet Spørg efter hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-135">Select Yes in the Ask for main account field.</span></span>
    * <span data-ttu-id="3e0cf-136">Angiv 'Spørg efter hovedkonto' til Ja for at tillade brugere at vælge hovedkontoen som en del af listen over dimensioner.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-136">Set 'Ask for main account' to Yes to allow users to select the main account as part of the list of dimensions.</span></span>   <span data-ttu-id="3e0cf-137">Hvis indstillingen er angivet til Nej, inkluderes den primære konto ikke på listen over dimensioner, og indstillingen 'Er hovedkonto obligatorisk' er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-137">If set to No, the main account will not be included to the list of dimensions and the 'Is main account mandatory' option is enabled.</span></span> <span data-ttu-id="3e0cf-138">Hvis "Er hovedkonto obligatorisk" er angivet til Ja, skal du inkludere hovedkontoen på listen over dimensioner, uanset brugerens valg.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-138">If "Is main account mandatory' is set to Yes, include the main account in the list of dimensions regardless of the user's selection.</span></span>  
22. <span data-ttu-id="3e0cf-139">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-139">Click OK.</span></span>
<span data-ttu-id="3e0cf-140">![Side for ER-modeltilknytningsdesigner](../media/er-financial-dimensions-guides-model-mapping1.png)</span><span class="sxs-lookup"><span data-stu-id="3e0cf-140">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping1.png)</span></span>
23. <span data-ttu-id="3e0cf-141">Vælg 'Dynamics 365 for Operations\Tabelposter' i træet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-141">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
24. <span data-ttu-id="3e0cf-142">Klik på Tilføj rod.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-142">Click Add root.</span></span>
25. <span data-ttu-id="3e0cf-143">Skriv "LedgerJournal" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-143">In the Name field, type 'LedgerJournal'.</span></span>
26. <span data-ttu-id="3e0cf-144">Vælg Ja i feltet Spørg efter forespørgsel.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-144">Select Yes in the Ask for query field.</span></span>
27. <span data-ttu-id="3e0cf-145">Skriv "LedgerJournalTable" i feltet Tabel.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-145">In the Table field, type 'LedgerJournalTable'.</span></span>
28. <span data-ttu-id="3e0cf-146">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-146">Click OK.</span></span>
<span data-ttu-id="3e0cf-147">![Side for ER-modeltilknytningsdesigner](../media/er-financial-dimensions-guides-model-mapping2.png)</span><span class="sxs-lookup"><span data-stu-id="3e0cf-147">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping2.png)</span></span>

## <a name="map-data-model-elements-to-added-data-sources"></a><span data-ttu-id="3e0cf-148">Tilknyt datamodelelementer til tilføjede datakilder</span><span class="sxs-lookup"><span data-stu-id="3e0cf-148">Map data model elements to added data sources</span></span>
1. <span data-ttu-id="3e0cf-149">Udvid 'Kladde' i træet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-149">In the tree, expand 'Journal'.</span></span>
2. <span data-ttu-id="3e0cf-150">Udvid 'Kladde\Transaktion' i træet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-150">In the tree, expand 'Journal\Transaction'.</span></span>
3. <span data-ttu-id="3e0cf-151">Udvid 'Kladde\Transaktion\Dimensionsdata' i træet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-151">In the tree, expand 'Journal\Transaction\Dimensions data'.</span></span>
4. <span data-ttu-id="3e0cf-152">Udvid eller skjul 'Dimensionsindstilling' i træet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-152">In the tree, expand 'Dimensions setting'.</span></span>
5. <span data-ttu-id="3e0cf-153">Udvid eller skjul 'LedgerJournal' i træet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-153">In the tree, expand 'LedgerJournal'.</span></span>
6. <span data-ttu-id="3e0cf-154">Udvid 'LedgerJournal\<Relations' i træet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-154">In the tree, expand 'LedgerJournal\<Relations'.</span></span>
7. <span data-ttu-id="3e0cf-155">Udvid 'LedgerJournal\<Relations\LedgerJournalTrans' i træet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-155">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
8. <span data-ttu-id="3e0cf-156">Vælg 'LedgerJournal\<Relations\LedgerJournalTrans\Voucher' i træet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-156">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Voucher'.</span></span>
9. <span data-ttu-id="3e0cf-157">Vælg 'Journal\Transaction\Voucher' i træet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-157">In the tree, select 'Journal\Transaction\Voucher'.</span></span>
10. <span data-ttu-id="3e0cf-158">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-158">Click Bind.</span></span>
11. <span data-ttu-id="3e0cf-159">Vælg 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)' i træet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-159">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
    * <span data-ttu-id="3e0cf-160">Bemærk, at for en hvilken som helst henvisning til økonomiske dimensioner, der f.eks. er angivet til LedgerDimension, er et tilsvarende datakildeelement tilgængeligt (LedgerDimension.Dimension).</span><span class="sxs-lookup"><span data-stu-id="3e0cf-160">Note that for any reference to financial dimensions that is set to, for instance, LedgerDimension, a corresponding data source item is available (LedgerDimension.Dimension).</span></span> <span data-ttu-id="3e0cf-161">Dette datakildeelement indeholder de økonomiske dimensioner for de dimensioner, der er angivet som postens liste.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-161">This data source item offers the financial dimensions of that dimensions set as the record's list.</span></span>  
12. <span data-ttu-id="3e0cf-162">Udvid 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)' i træet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-162">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
13. <span data-ttu-id="3e0cf-163">Udvid 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hovedkonto og dimensioner' i træet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-163">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
14. <span data-ttu-id="3e0cf-164">Udvid 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hovedkonto og dimensioner\Værdi' i træet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-164">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value'.</span></span>
15. <span data-ttu-id="3e0cf-165">Udvid 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hovedkonto og dimensioner\Definition' i træet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-165">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition'.</span></span>
16. <span data-ttu-id="3e0cf-166">Vælg 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hovedkonto og dimensioner\Definition\Navn' i træet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-166">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name'.</span></span>
17. <span data-ttu-id="3e0cf-167">Vælg 'Kladde\Transaktion\Dimensionsdata\Navn' i træet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-167">In the tree, select 'Journal\Transaction\Dimensions data\Name'.</span></span>
18. <span data-ttu-id="3e0cf-168">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-168">Click Bind.</span></span>
19. <span data-ttu-id="3e0cf-169">Vælg 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hovedkonto og dimensioner\Værdi\Beskrivelse' i træet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-169">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description'.</span></span>
20. <span data-ttu-id="3e0cf-170">Vælg 'Kladde\Transaktion\Dimensionsdata\Beskrivelse' i træet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-170">In the tree, select 'Journal\Transaction\Dimensions data\Description'.</span></span>
21. <span data-ttu-id="3e0cf-171">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-171">Click Bind.</span></span>
22. <span data-ttu-id="3e0cf-172">Vælg 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hovedkonto og dimensioner\Værdi\Kode' i træet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-172">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code'.</span></span>
23. <span data-ttu-id="3e0cf-173">Vælg 'Kladde\Transaktion\Dimensionsdata\Kode' i træet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-173">In the tree, select 'Journal\Transaction\Dimensions data\Code'.</span></span>
24. <span data-ttu-id="3e0cf-174">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-174">Click Bind.</span></span>
25. <span data-ttu-id="3e0cf-175">Vælg 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Hovedkonto og dimensioner' i træet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-175">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
26. <span data-ttu-id="3e0cf-176">Vælg 'Kladde\Transaktion\Dimensionsdata' i træet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-176">In the tree, select 'Journal\Transaction\Dimensions data'.</span></span>
27. <span data-ttu-id="3e0cf-177">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-177">Click Bind.</span></span>
<span data-ttu-id="3e0cf-178">![Side for ER-modeltilknytningsdesigner](../media/er-financial-dimensions-guides-model-mapping3.png)</span><span class="sxs-lookup"><span data-stu-id="3e0cf-178">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping3.png)</span></span>
28. <span data-ttu-id="3e0cf-179">Vælg 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)' i træet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-179">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)'.</span></span>
29. <span data-ttu-id="3e0cf-180">Vælg 'Journal\Transaction\Debit' i træet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-180">In the tree, select 'Journal\Transaction\Debit'.</span></span>
30. <span data-ttu-id="3e0cf-181">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-181">Click Bind.</span></span>
31. <span data-ttu-id="3e0cf-182">Vælg 'LedgerJournal\\<Relations\LedgerJournalTrans\Date(TransDate)' i træet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-182">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)'.</span></span>
32. <span data-ttu-id="3e0cf-183">Vælg 'Journal\Transaction\Date' i træet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-183">In the tree, select 'Journal\Transaction\Date'.</span></span>
33. <span data-ttu-id="3e0cf-184">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-184">Click Bind.</span></span>
34. <span data-ttu-id="3e0cf-185">Vælg 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)' i træet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-185">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)'.</span></span>
35. <span data-ttu-id="3e0cf-186">Vælg 'Journal\Transaction\Currency' i træet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-186">In the tree, select 'Journal\Transaction\Currency'.</span></span>
36. <span data-ttu-id="3e0cf-187">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-187">Click Bind.</span></span>
37. <span data-ttu-id="3e0cf-188">Vælg 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)' i træet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-188">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)'.</span></span>
38. <span data-ttu-id="3e0cf-189">Vælg 'Journal\Transaction\Credit' i træet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-189">In the tree, select 'Journal\Transaction\Credit'.</span></span>
39. <span data-ttu-id="3e0cf-190">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-190">Click Bind.</span></span>
40. <span data-ttu-id="3e0cf-191">Vælg 'LedgerJournal\<Relations\LedgerJournalTrans' i træet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-191">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
41. <span data-ttu-id="3e0cf-192">Vælg 'Journal\Transaction' i træet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-192">In the tree, select 'Journal\Transaction'.</span></span>
42. <span data-ttu-id="3e0cf-193">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-193">Click Bind.</span></span>
43. <span data-ttu-id="3e0cf-194">Vælg "LedgerJournal\Journalbatchnummer(JournalNum)" i træet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-194">In the tree, select 'LedgerJournal\Journal batch number(JournalNum)'.</span></span>
44. <span data-ttu-id="3e0cf-195">Vælg 'Journal\Batch' i træet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-195">In the tree, select 'Journal\Batch'.</span></span>
45. <span data-ttu-id="3e0cf-196">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-196">Click Bind.</span></span>
46. <span data-ttu-id="3e0cf-197">Vælg 'LedgerJournal' i træet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-197">In the tree, select 'LedgerJournal'.</span></span>
47. <span data-ttu-id="3e0cf-198">Vælg 'Journal' i træet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-198">In the tree, select 'Journal'.</span></span>
48. <span data-ttu-id="3e0cf-199">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-199">Click Bind.</span></span>
49. <span data-ttu-id="3e0cf-200">Udvid 'Dimensions' i træet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-200">In the tree, expand 'Dimensions'.</span></span>
50. <span data-ttu-id="3e0cf-201">Udvid 'Dimensions\Hovedkonto og dimensioner' i træet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-201">In the tree, expand 'Dimensions\Main account and dimensions'.</span></span>
51. <span data-ttu-id="3e0cf-202">Udvid 'Dimensions\Hovedkonto og dimensioner\Definition' i træet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-202">In the tree, expand 'Dimensions\Main account and dimensions\Definition'.</span></span>
52. <span data-ttu-id="3e0cf-203">Vælg 'Dimensions\Hovedkonto og dimensioner\Definition\Navn' i træet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-203">In the tree, select 'Dimensions\Main account and dimensions\Definition\Name'.</span></span>
53. <span data-ttu-id="3e0cf-204">Vælg 'Dimensionsindstilling\Kode' i træet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-204">In the tree, select 'Dimensions setting\Code'.</span></span>
54. <span data-ttu-id="3e0cf-205">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-205">Click Bind.</span></span>
55. <span data-ttu-id="3e0cf-206">Vælg 'Dimensions\Hovedkonto og dimensioner\Definition\Navn på rapportkolonne' i træet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-206">In the tree, select 'Dimensions\Main account and dimensions\Definition\Report column name'.</span></span>
56. <span data-ttu-id="3e0cf-207">Vælg 'Dimensionsindstilling\Navn' i træet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-207">In the tree, select 'Dimensions setting\Name'.</span></span>
57. <span data-ttu-id="3e0cf-208">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-208">Click Bind.</span></span>
58. <span data-ttu-id="3e0cf-209">Vælg 'Dimensions\Hovedkonto og dimensioner' i træet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-209">In the tree, select 'Dimensions\Main account and dimensions'.</span></span>
59. <span data-ttu-id="3e0cf-210">Vælg 'Dimensionsindstilling' i træet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-210">In the tree, select 'Dimensions setting'.</span></span>
60. <span data-ttu-id="3e0cf-211">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-211">Click Bind.</span></span>
61. <span data-ttu-id="3e0cf-212">Vælg "Firma" i træet.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-212">In the tree, select 'Company'.</span></span>
62. <span data-ttu-id="3e0cf-213">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-213">Click Edit.</span></span>
63. <span data-ttu-id="3e0cf-214">I feltet expressionAsStringText skal du skrive 'Company.'find()'.'name()''.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-214">In the expressionAsStringText field, enter 'Company.'find()'.'name()''.</span></span>
    * <span data-ttu-id="3e0cf-215">Company.'find()'.'name()'</span><span class="sxs-lookup"><span data-stu-id="3e0cf-215">Company.'find()'.'name()'</span></span>  
64. <span data-ttu-id="3e0cf-216">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-216">Click Save.</span></span>
<span data-ttu-id="3e0cf-217">![Side for ER-modeltilknytningsdesigner](../media/er-financial-dimensions-guides-model-mapping4.png)</span><span class="sxs-lookup"><span data-stu-id="3e0cf-217">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping4.png)</span></span>
65. <span data-ttu-id="3e0cf-218">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-218">Close the page.</span></span>
66. <span data-ttu-id="3e0cf-219">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-219">Click Save.</span></span>
67. <span data-ttu-id="3e0cf-220">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-220">Close the page.</span></span>

## <a name="complete-this-draft-models-version"></a><span data-ttu-id="3e0cf-221">Fuldfør denne version af kladdemodellen</span><span class="sxs-lookup"><span data-stu-id="3e0cf-221">Complete this draft model's version</span></span>
1. <span data-ttu-id="3e0cf-222">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-222">Close the page.</span></span>
2. <span data-ttu-id="3e0cf-223">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-223">Close the page.</span></span>
3. <span data-ttu-id="3e0cf-224">Klik på Skift status.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-224">Click Change status.</span></span>
4. <span data-ttu-id="3e0cf-225">Klik på Fuldført.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-225">Click Complete.</span></span>
5. <span data-ttu-id="3e0cf-226">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="3e0cf-226">Click OK.</span></span>
<span data-ttu-id="3e0cf-227">![Side for ER-modeltilknytningsdesigner](../media/er-financial-dimensions-guides-model-mapping5.png)</span><span class="sxs-lookup"><span data-stu-id="3e0cf-227">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping5.png)</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]