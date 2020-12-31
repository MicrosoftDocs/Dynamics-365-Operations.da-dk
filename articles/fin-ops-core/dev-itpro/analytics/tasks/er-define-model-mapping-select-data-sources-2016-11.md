---
title: Definere ER-modeltilknytninger og vælge datakilder til dem
description: Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler til elektronisk rapportering kan vælge datakilder til en datamodel for elektronisk rapportering.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7d57c191761b8e2367ff8806c1cd98d6d83559e3
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682111"
---
# <a name="define-er-model-mappings-and-select-data-sources-for-them"></a><span data-ttu-id="0fc21-103">Definere ER-modeltilknytninger og vælge datakilder til dem</span><span class="sxs-lookup"><span data-stu-id="0fc21-103">Define ER model mappings and select data sources for them</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0fc21-104">Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler til elektronisk rapportering kan vælge datakilder til en datamodel for elektronisk rapportering (ER).</span><span class="sxs-lookup"><span data-stu-id="0fc21-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can select data sources for an Electronic reporting (ER) data model.</span></span> <span data-ttu-id="0fc21-105">Datakilderne skal være bundet til enkelte komponenter i den valgte datamodel i designfasen og udfylde forretningsoplysninger til denne datamodel på kørselstidspunktet.</span><span class="sxs-lookup"><span data-stu-id="0fc21-105">The data sources will be bound to individual components of the selected data model at design time and populate business data to that data model at run-time.</span></span> <span data-ttu-id="0fc21-106">I dette eksempel skal du vælge datakilder til en eksisterende datamodel, der er oprettet for eksempelfirmaet Litware, Inc. For at fuldføre denne fremgangsmåde, skal du først fuldføre trinnene i proceduren "Oprette en ny datamodel".</span><span class="sxs-lookup"><span data-stu-id="0fc21-106">In this example, you will select data sources for an existing data model that has been created for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the "Create a new data model" procedure.</span></span>


## <a name="open-the-electronic-reporting-configurations-tree"></a><span data-ttu-id="0fc21-107">Åbn træet til elektroniske rapporteringskonfigurationer</span><span class="sxs-lookup"><span data-stu-id="0fc21-107">Open the Electronic Reporting configurations tree</span></span>
1. <span data-ttu-id="0fc21-108">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="0fc21-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="0fc21-109">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="0fc21-109">Click Reporting configurations.</span></span>

## <a name="insert-a-new-model-mapping"></a><span data-ttu-id="0fc21-110">Indsæt en ny modeltilknytning</span><span class="sxs-lookup"><span data-stu-id="0fc21-110">Insert a new model mapping</span></span>
1. <span data-ttu-id="0fc21-111">Vælg "Betalinger (forenklet mode)" i træet.</span><span class="sxs-lookup"><span data-stu-id="0fc21-111">In the tree, select 'Payments (simplified model)'.</span></span>
2. <span data-ttu-id="0fc21-112">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="0fc21-112">Click Designer.</span></span>
3. <span data-ttu-id="0fc21-113">Klik på Tilknyt model til datakilde.</span><span class="sxs-lookup"><span data-stu-id="0fc21-113">Click Map model to datasource.</span></span>
4. <span data-ttu-id="0fc21-114">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="0fc21-114">Click New.</span></span>
    * <span data-ttu-id="0fc21-115">Derved oprettes en ny post, der knytter datamodellen til datakilder.</span><span class="sxs-lookup"><span data-stu-id="0fc21-115">This will create a new record that will map the data model to data sources.</span></span> <span data-ttu-id="0fc21-116">I dette eksempel skal du knytte datamodellen til datakilder for den ønskede betalingstype: overførsel.</span><span class="sxs-lookup"><span data-stu-id="0fc21-116">In this example, you will map the data model to data sources for the desired payment type: credit transfer.</span></span>     <span data-ttu-id="0fc21-117">Det er muligt at udforme mere end én tilknytning til en bestemt datamodel.</span><span class="sxs-lookup"><span data-stu-id="0fc21-117">It is possible to design more than one mapping for a particular data model.</span></span> <span data-ttu-id="0fc21-118">For eksempel kan du oprette en tilknytning til de forskellige typer betalinger, såsom direkte debitering eller krediteringsoverførsler.</span><span class="sxs-lookup"><span data-stu-id="0fc21-118">For example, you could create a mapping for the different types of payments, such as for direct debit or for credit transfers.</span></span> <span data-ttu-id="0fc21-119">I dette eksempel skal du oprette en tilknytning til overførsler.</span><span class="sxs-lookup"><span data-stu-id="0fc21-119">In this example, you will create a mapping for credit transfers.</span></span>  
5. <span data-ttu-id="0fc21-120">Skriv CT-tilknytning" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0fc21-120">In the Name field, type 'CT mapping'.</span></span>
    * <span data-ttu-id="0fc21-121">CT-tilknytning</span><span class="sxs-lookup"><span data-stu-id="0fc21-121">CT mapping</span></span>  
6. <span data-ttu-id="0fc21-122">Skriv "Betalingsmodel tilknytning CT" i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="0fc21-122">In the Description field, type 'Payment model mapping CT'.</span></span>
    * <span data-ttu-id="0fc21-123">Betalingsmodel tilknytning CT</span><span class="sxs-lookup"><span data-stu-id="0fc21-123">Payment model mapping CT</span></span>  
7. <span data-ttu-id="0fc21-124">Skriv "CustomerCreditTransferInitiation" i feltet Definition.</span><span class="sxs-lookup"><span data-stu-id="0fc21-124">In the Definition field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="0fc21-125">Vælg CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="0fc21-125">CustomerCreditTransferInitiation</span></span>  
8. <span data-ttu-id="0fc21-126">ResolveChanges definitionen.</span><span class="sxs-lookup"><span data-stu-id="0fc21-126">ResolveChanges the Definition.</span></span>
9. <span data-ttu-id="0fc21-127">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="0fc21-127">Click Save.</span></span>

## <a name="define-required-data-sources-for-the-current-model-mapping"></a><span data-ttu-id="0fc21-128">Definer påkrævede datakilder for den aktuelle modeltilknytning</span><span class="sxs-lookup"><span data-stu-id="0fc21-128">Define required data sources for the current model mapping</span></span>
1. <span data-ttu-id="0fc21-129">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="0fc21-129">Click Designer.</span></span>
2. <span data-ttu-id="0fc21-130">Vælg 'Dynamics 365 for Operations\Tabelposter' i træet.</span><span class="sxs-lookup"><span data-stu-id="0fc21-130">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
3. <span data-ttu-id="0fc21-131">Klik på Tilføj rod.</span><span class="sxs-lookup"><span data-stu-id="0fc21-131">Click Add root.</span></span>
    * <span data-ttu-id="0fc21-132">Angiv denne datakilde for at få adgang til betalingstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="0fc21-132">Enter this data source to access payment transactions.</span></span>  
4. <span data-ttu-id="0fc21-133">Skriv "Transaktioner" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0fc21-133">In the Name field, type 'Transactions'.</span></span>
    * <span data-ttu-id="0fc21-134">Poster</span><span class="sxs-lookup"><span data-stu-id="0fc21-134">Transactions</span></span>  
5. <span data-ttu-id="0fc21-135">Angiv "Transaktioner" i feltet Etiket.</span><span class="sxs-lookup"><span data-stu-id="0fc21-135">In the Label field, enter 'Transactions'.</span></span>
    * <span data-ttu-id="0fc21-136">Poster</span><span class="sxs-lookup"><span data-stu-id="0fc21-136">Transactions</span></span>  
6. <span data-ttu-id="0fc21-137">Angiv "Finansjournallinjer" i feltet Hjælp.</span><span class="sxs-lookup"><span data-stu-id="0fc21-137">In the Help field, enter 'Ledger journal lines'.</span></span>
    * <span data-ttu-id="0fc21-138">Finansjournallinjer</span><span class="sxs-lookup"><span data-stu-id="0fc21-138">Ledger journal lines</span></span>  
7. <span data-ttu-id="0fc21-139">Vælg Ja i feltet Spørg efter forespørgsel.</span><span class="sxs-lookup"><span data-stu-id="0fc21-139">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="0fc21-140">Vælg Ja.</span><span class="sxs-lookup"><span data-stu-id="0fc21-140">Select Yes.</span></span>  
8. <span data-ttu-id="0fc21-141">Skriv "LedgerJournalTrans" i feltet Tabel.</span><span class="sxs-lookup"><span data-stu-id="0fc21-141">In the Table field, type 'LedgerJournalTrans'.</span></span>
    * <span data-ttu-id="0fc21-142">LedgerJournalTrans</span><span class="sxs-lookup"><span data-stu-id="0fc21-142">LedgerJournalTrans</span></span>  
9. <span data-ttu-id="0fc21-143">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0fc21-143">Click OK.</span></span>
    * <span data-ttu-id="0fc21-144">Vælg LedgerJournalTrans-tabellen som en datakilde for den aktuelle datamodel.</span><span class="sxs-lookup"><span data-stu-id="0fc21-144">Select the LedgerJournalTrans table as a data source for the current data model.</span></span>  
10. <span data-ttu-id="0fc21-145">Vælg "Funktioner\Beregnet felt" i træet.</span><span class="sxs-lookup"><span data-stu-id="0fc21-145">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="0fc21-146">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="0fc21-146">Click Add.</span></span>
    * <span data-ttu-id="0fc21-147">Klik på Tilføj for at tilføje et nyt beregnet felt.</span><span class="sxs-lookup"><span data-stu-id="0fc21-147">Click Add to add a new calculated field.</span></span>  
12. <span data-ttu-id="0fc21-148">Skriv "$EndToEndID" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0fc21-148">In the Name field, type '$EndToEndID'.</span></span>
    * <span data-ttu-id="0fc21-149">$EndToEndID</span><span class="sxs-lookup"><span data-stu-id="0fc21-149">$EndToEndID</span></span>  
13. <span data-ttu-id="0fc21-150">Klik på Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="0fc21-150">Click Edit formula.</span></span>
14. <span data-ttu-id="0fc21-151">Vælg '"Streng\SAMMENKÆD" i træet.</span><span class="sxs-lookup"><span data-stu-id="0fc21-151">In the tree, select 'String\CONCATENATE'.</span></span>
15. <span data-ttu-id="0fc21-152">Klik på Tilføj funktion.</span><span class="sxs-lookup"><span data-stu-id="0fc21-152">Click Add function.</span></span>
16. <span data-ttu-id="0fc21-153">Udvid "Transaktioner" i træet.</span><span class="sxs-lookup"><span data-stu-id="0fc21-153">In the tree, expand 'Transactions'.</span></span>
17. <span data-ttu-id="0fc21-154">Vælg "Transaktioner\Bilag" i træet.</span><span class="sxs-lookup"><span data-stu-id="0fc21-154">In the tree, select 'Transactions\Voucher'.</span></span>
18. <span data-ttu-id="0fc21-155">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="0fc21-155">Click Add data source.</span></span>
19. <span data-ttu-id="0fc21-156">Skriv "CONCATENATE(Transaktioner.Bilag, "-", " i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="0fc21-156">In the Formula field, enter 'CONCATENATE(Transactions.Voucher, "-", '.</span></span>
    * <span data-ttu-id="0fc21-157">Skriv [ , "-", ] i slutningen af formlen.</span><span class="sxs-lookup"><span data-stu-id="0fc21-157">Type [ , "-", ] at the end of the formula.</span></span>  
20. <span data-ttu-id="0fc21-158">Vælg "Streng\TEKST" i træet.</span><span class="sxs-lookup"><span data-stu-id="0fc21-158">In the tree, select 'String\TEXT'.</span></span>
21. <span data-ttu-id="0fc21-159">Klik på Tilføj funktion.</span><span class="sxs-lookup"><span data-stu-id="0fc21-159">Click Add function.</span></span>
22. <span data-ttu-id="0fc21-160">Vælg "Transaktioner\Post-ID(RecId)' i træet.</span><span class="sxs-lookup"><span data-stu-id="0fc21-160">In the tree, select 'Transactions\Record-ID(RecId)'.</span></span>
23. <span data-ttu-id="0fc21-161">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="0fc21-161">Click Add data source.</span></span>
24. <span data-ttu-id="0fc21-162">Skriv "CONCATENATE(Transaktioner.Bilag, "-", TEXT(Transaktioner.RecId))" i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="0fc21-162">In the Formula field, enter 'CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))'.</span></span>
    * <span data-ttu-id="0fc21-163">Skriv [))] i slutningen af formlen.</span><span class="sxs-lookup"><span data-stu-id="0fc21-163">Type [))] at the end of the formula.</span></span>  
25. <span data-ttu-id="0fc21-164">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="0fc21-164">Click Save.</span></span>
    * <span data-ttu-id="0fc21-165">Sørg for, at ingen fejl er fundet for den formel, der er oprettet.</span><span class="sxs-lookup"><span data-stu-id="0fc21-165">Make sure that no errors have been discovered for the created formula.</span></span> <span data-ttu-id="0fc21-166">Se fanen FEJL under formelkontrolelementet.</span><span class="sxs-lookup"><span data-stu-id="0fc21-166">See the ERRORS tab below the formula editor control.</span></span>  
26. <span data-ttu-id="0fc21-167">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0fc21-167">Close the page.</span></span>
27. <span data-ttu-id="0fc21-168">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0fc21-168">Click OK.</span></span>
    * <span data-ttu-id="0fc21-169">Føj det beregnede felt til denne datakilde.</span><span class="sxs-lookup"><span data-stu-id="0fc21-169">Add the calculated field to this data source.</span></span>  
28. <span data-ttu-id="0fc21-170">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="0fc21-170">Click Add.</span></span>
    * <span data-ttu-id="0fc21-171">Klik på Tilføj for at tilføje et nyt beregnet felt.</span><span class="sxs-lookup"><span data-stu-id="0fc21-171">Click Add to add a new calculated field.</span></span>  
29. <span data-ttu-id="0fc21-172">Skriv "$Amount" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0fc21-172">In the Name field, type '$Amount'.</span></span>
    * <span data-ttu-id="0fc21-173">$Amount</span><span class="sxs-lookup"><span data-stu-id="0fc21-173">$Amount</span></span>  
30. <span data-ttu-id="0fc21-174">Klik på Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="0fc21-174">Click Edit formula.</span></span>
31. <span data-ttu-id="0fc21-175">Udvid "Transaktioner" i træet.</span><span class="sxs-lookup"><span data-stu-id="0fc21-175">In the tree, expand 'Transactions'.</span></span>
32. <span data-ttu-id="0fc21-176">Vælg "Transaktioner\Debit(AmountCurDebit)" i træet.</span><span class="sxs-lookup"><span data-stu-id="0fc21-176">In the tree, select 'Transactions\Debit(AmountCurDebit)'.</span></span>
33. <span data-ttu-id="0fc21-177">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="0fc21-177">Click Add data source.</span></span>
34. <span data-ttu-id="0fc21-178">Skriv "Transaktioner.AmountCurDebit - " i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="0fc21-178">In the Formula field, enter 'Transactions.AmountCurDebit - '.</span></span>
    * <span data-ttu-id="0fc21-179">Skriv [ - ] i slutningen af formlen.</span><span class="sxs-lookup"><span data-stu-id="0fc21-179">Type [ - ] at the end of the formula.</span></span>  
35. <span data-ttu-id="0fc21-180">Vælg "Transaktioner\Credit(AmountCurCredit)" i træet.</span><span class="sxs-lookup"><span data-stu-id="0fc21-180">In the tree, select 'Transactions\Credit(AmountCurCredit)'.</span></span>
36. <span data-ttu-id="0fc21-181">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="0fc21-181">Click Add data source.</span></span>
37. <span data-ttu-id="0fc21-182">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="0fc21-182">Click Save.</span></span>
38. <span data-ttu-id="0fc21-183">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0fc21-183">Close the page.</span></span>
39. <span data-ttu-id="0fc21-184">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0fc21-184">Click OK.</span></span>
    * <span data-ttu-id="0fc21-185">Dette føjer det $Amount-beregnede felt til den valgte datakilde for den aktuelle datamodel.</span><span class="sxs-lookup"><span data-stu-id="0fc21-185">This will add the $Amount calculated field to the selected data source for the current data model.</span></span>  
40. <span data-ttu-id="0fc21-186">Vælg "Transaktioner\$Amount" i træet.</span><span class="sxs-lookup"><span data-stu-id="0fc21-186">In the tree, select 'Transactions\$Amount'.</span></span>
41. <span data-ttu-id="0fc21-187">Udvid "Transaktioner" i træet.</span><span class="sxs-lookup"><span data-stu-id="0fc21-187">In the tree, expand 'Transactions'.</span></span>
42. <span data-ttu-id="0fc21-188">Udvid eller skjul "Transaktioner\$Amount" i træet.</span><span class="sxs-lookup"><span data-stu-id="0fc21-188">In the tree, expand or collapse 'Transactions\$Amount'.</span></span>
43. <span data-ttu-id="0fc21-189">Udvid eller skjul "Transaktioner" i træet.</span><span class="sxs-lookup"><span data-stu-id="0fc21-189">In the tree, expand or collapse 'Transactions'.</span></span>
44. <span data-ttu-id="0fc21-190">Vælg 'Dynamics 365 for Operations\Tabelposter' i træet.</span><span class="sxs-lookup"><span data-stu-id="0fc21-190">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
45. <span data-ttu-id="0fc21-191">Klik på Tilføj rod.</span><span class="sxs-lookup"><span data-stu-id="0fc21-191">Click Add root.</span></span>
    * <span data-ttu-id="0fc21-192">Angiv denne datakilde for at få adgang til oplysninger om firmaets bankkonto.</span><span class="sxs-lookup"><span data-stu-id="0fc21-192">Enter this data source to access the company's bank account details.</span></span>  
46. <span data-ttu-id="0fc21-193">Skriv "BankAccount" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0fc21-193">In the Name field, type 'BankAccount'.</span></span>
    * <span data-ttu-id="0fc21-194">BankAccount</span><span class="sxs-lookup"><span data-stu-id="0fc21-194">BankAccount</span></span>  
47. <span data-ttu-id="0fc21-195">Angiv "Bankkonto" i feltet Etiket.</span><span class="sxs-lookup"><span data-stu-id="0fc21-195">In the Label field, enter 'Bank Account'.</span></span>
    * <span data-ttu-id="0fc21-196">Bankkonto</span><span class="sxs-lookup"><span data-stu-id="0fc21-196">Bank Account</span></span>  
48. <span data-ttu-id="0fc21-197">Angiv "Bankkonto" i feltet Hjælp.</span><span class="sxs-lookup"><span data-stu-id="0fc21-197">In the Help field, enter 'Bank Account'.</span></span>
    * <span data-ttu-id="0fc21-198">Bankkonto</span><span class="sxs-lookup"><span data-stu-id="0fc21-198">Bank Account</span></span>  
49. <span data-ttu-id="0fc21-199">Vælg Ja i feltet Spørg efter forespørgsel.</span><span class="sxs-lookup"><span data-stu-id="0fc21-199">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="0fc21-200">Vælg Ja.</span><span class="sxs-lookup"><span data-stu-id="0fc21-200">Select Yes.</span></span>  
50. <span data-ttu-id="0fc21-201">Skriv "BankAccountTable" i feltet Tabel.</span><span class="sxs-lookup"><span data-stu-id="0fc21-201">In the Table field, type 'BankAccountTable'.</span></span>
    * <span data-ttu-id="0fc21-202">BankAccountTable</span><span class="sxs-lookup"><span data-stu-id="0fc21-202">BankAccountTable</span></span>  
51. <span data-ttu-id="0fc21-203">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0fc21-203">Click OK.</span></span>
    * <span data-ttu-id="0fc21-204">Vælg BankAccountTable-tabellen som en datakilde for den aktuelle datamodel.</span><span class="sxs-lookup"><span data-stu-id="0fc21-204">Select the BankAccountTable table as a data source for the current data model.</span></span>  
52. <span data-ttu-id="0fc21-205">Klik på Tilføj rod.</span><span class="sxs-lookup"><span data-stu-id="0fc21-205">Click Add root.</span></span>
    * <span data-ttu-id="0fc21-206">Angiv denne datakilde for at få adgang til oplysninger om firmaets forudsætninger.</span><span class="sxs-lookup"><span data-stu-id="0fc21-206">Enter this data source to access the company's requisites.</span></span>  
53. <span data-ttu-id="0fc21-207">Skriv "Firma" feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0fc21-207">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="0fc21-208">Regnskab</span><span class="sxs-lookup"><span data-stu-id="0fc21-208">Company</span></span>  
54. <span data-ttu-id="0fc21-209">Skriv en værdi i feltet Etiket.</span><span class="sxs-lookup"><span data-stu-id="0fc21-209">In the Label field, type a value.</span></span>
    * <span data-ttu-id="0fc21-210">Firmaoplysninger</span><span class="sxs-lookup"><span data-stu-id="0fc21-210">Company information</span></span>  
55. <span data-ttu-id="0fc21-211">Skriv "Firmaoplysninger" i feltet Hjælp.</span><span class="sxs-lookup"><span data-stu-id="0fc21-211">In the Help field, enter 'Company information'.</span></span>
    * <span data-ttu-id="0fc21-212">Firmaoplysninger</span><span class="sxs-lookup"><span data-stu-id="0fc21-212">Company information</span></span>  
56. <span data-ttu-id="0fc21-213">Vælg Ja i feltet Spørg efter forespørgsel.</span><span class="sxs-lookup"><span data-stu-id="0fc21-213">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="0fc21-214">Vælg Ja.</span><span class="sxs-lookup"><span data-stu-id="0fc21-214">Select Yes.</span></span>  
57. <span data-ttu-id="0fc21-215">Skriv "CompanyInfo" i feltet Tabel.</span><span class="sxs-lookup"><span data-stu-id="0fc21-215">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="0fc21-216">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="0fc21-216">CompanyInfo</span></span>  
58. <span data-ttu-id="0fc21-217">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0fc21-217">Click OK.</span></span>
    * <span data-ttu-id="0fc21-218">Vælg CompanyInfo-tabellen som en datakilde for den aktuelle datamodel.</span><span class="sxs-lookup"><span data-stu-id="0fc21-218">Select the CompanyInfo table as a data source for the current data model.</span></span>  
59. <span data-ttu-id="0fc21-219">Vælg "Funktioner\Beregnet felt" i træet.</span><span class="sxs-lookup"><span data-stu-id="0fc21-219">In the tree, select 'Functions\Calculated field'.</span></span>
60. <span data-ttu-id="0fc21-220">Klik på Tilføj rod.</span><span class="sxs-lookup"><span data-stu-id="0fc21-220">Click Add root.</span></span>
    * <span data-ttu-id="0fc21-221">Indsæt et beregnet felt som en ny datakilde.</span><span class="sxs-lookup"><span data-stu-id="0fc21-221">Insert a calculated field as a new data source.</span></span>  
61. <span data-ttu-id="0fc21-222">Skriv "ProcessingDateTime" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0fc21-222">In the Name field, type 'ProcessingDateTime'.</span></span>
    * <span data-ttu-id="0fc21-223">ProcessingDateTime</span><span class="sxs-lookup"><span data-stu-id="0fc21-223">ProcessingDateTime</span></span>  
62. <span data-ttu-id="0fc21-224">Skriv "Afviklingsdato og -klokkeslæt" i feltet Etiket.</span><span class="sxs-lookup"><span data-stu-id="0fc21-224">In the Label field, enter 'Processing date & time'.</span></span>
    * <span data-ttu-id="0fc21-225">Behandlingsdato og -klokkeslæt</span><span class="sxs-lookup"><span data-stu-id="0fc21-225">Processing date & time</span></span>  
63. <span data-ttu-id="0fc21-226">Klik på Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="0fc21-226">Click Edit formula.</span></span>
64. <span data-ttu-id="0fc21-227">Vælg "Dato/klokkeslæt\SESSIONNOW".</span><span class="sxs-lookup"><span data-stu-id="0fc21-227">In the tree, select 'Date/time\SESSIONNOW'.</span></span>
65. <span data-ttu-id="0fc21-228">Klik på Tilføj funktion.</span><span class="sxs-lookup"><span data-stu-id="0fc21-228">Click Add function.</span></span>
66. <span data-ttu-id="0fc21-229">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="0fc21-229">Click Save.</span></span>
67. <span data-ttu-id="0fc21-230">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0fc21-230">Close the page.</span></span>
68. <span data-ttu-id="0fc21-231">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0fc21-231">Click OK.</span></span>
    * <span data-ttu-id="0fc21-232">Føj det ProcessingDateTime-beregnede som en datakilde til den aktuelle datamodel.</span><span class="sxs-lookup"><span data-stu-id="0fc21-232">Add the ProcessingDateTime calculated field as a data source for the current data model.</span></span>  
69. <span data-ttu-id="0fc21-233">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="0fc21-233">Click Save.</span></span>
70. <span data-ttu-id="0fc21-234">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0fc21-234">Close the page.</span></span>
71. <span data-ttu-id="0fc21-235">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0fc21-235">Close the page.</span></span>
72. <span data-ttu-id="0fc21-236">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0fc21-236">Close the page.</span></span>

