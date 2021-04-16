---
title: Tilknyt ER-datamodel til markerede datakilder
description: I dette emne beskrives, hvordan du kan knytte en ER-datamodel (elektronisk rapportering) til udvalgte Microsoft Dynamics 365 Finance-datakilder.
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0eb7f48a50e32637003c1488d80899a704709068
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751480"
---
# <a name="er-map-data-model-to-selected-data-sources"></a><span data-ttu-id="d958c-103">Tilknyt ER-datamodel til markerede datakilder</span><span class="sxs-lookup"><span data-stu-id="d958c-103">ER Map data model to selected data sources</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d958c-104">Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler til elektronisk rapportering kan tilknytte en datamodel for elektronisk rapportering (ER) til valgte datakilder.</span><span class="sxs-lookup"><span data-stu-id="d958c-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can map an Electronic reporting (ER) data model to selected data sources.</span></span> <span data-ttu-id="d958c-105">Denne modeltilknytning bruges senere som datakilde i en formatkonfiguration, der skal bruges til at administrere elektroniske betalingsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="d958c-105">This model mapping will later be used as a data source in a format configuration that will be used to manage electronic payment documents.</span></span> <span data-ttu-id="d958c-106">I dette eksempel skal du tilknytte en datamodel for eksempelfirmaet Litware, Inc. til datakilder.</span><span class="sxs-lookup"><span data-stu-id="d958c-106">In this example, you map a data model for sample company, Litware, Inc. to data sources.</span></span> <span data-ttu-id="d958c-107">For at fuldføre disse trin skal du først fuldføre trinnene i proceduren "Vælg datakilder til modeltilknytning".</span><span class="sxs-lookup"><span data-stu-id="d958c-107">To complete these steps, you must first complete the steps in the "Select data sources for model mapping" procedure.</span></span>


## <a name="open-er-configurations-tree"></a><span data-ttu-id="d958c-108">Åbn ER-konfigurationstræ</span><span class="sxs-lookup"><span data-stu-id="d958c-108">Open ER configurations tree</span></span>
1. <span data-ttu-id="d958c-109">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="d958c-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="d958c-110">Klik på Konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="d958c-110">Click Configurations.</span></span>

## <a name="select-created-model-mapping"></a><span data-ttu-id="d958c-111">Vælg oprettet modeltilknytning</span><span class="sxs-lookup"><span data-stu-id="d958c-111">Select created model mapping</span></span>
1. <span data-ttu-id="d958c-112">Vælg "Betalinger (forenklet mode)" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-112">In the tree, select 'Payments (simplified model)'.</span></span>
    * <span data-ttu-id="d958c-113">Kontrollér, at konfigurationen af modellen "Betalinger (forenklet model)" er oprettet på forhånd.</span><span class="sxs-lookup"><span data-stu-id="d958c-113">Make sure that the model configuration "Payments (simplified model)" has been created in advance.</span></span> <span data-ttu-id="d958c-114">Eller stop nu og vend tilbage efter du har fuldført opgaveguiden "Opret en ny konfiguration med det valgte domænes datamodel".</span><span class="sxs-lookup"><span data-stu-id="d958c-114">Otherwise, stop now and return after completion of the task guide 'Create a new configuration with data model of the selected domain'.</span></span>  
2. <span data-ttu-id="d958c-115">Klik på Modeldesigner.</span><span class="sxs-lookup"><span data-stu-id="d958c-115">Click Model designer.</span></span>
3. <span data-ttu-id="d958c-116">Klik på Tilknyt model til datakilde.</span><span class="sxs-lookup"><span data-stu-id="d958c-116">Click Map model to datasource.</span></span>
4. <span data-ttu-id="d958c-117">Vælg posten "CT-tilknytning".</span><span class="sxs-lookup"><span data-stu-id="d958c-117">Select the 'CT mapping' record.</span></span>
    * <span data-ttu-id="d958c-118">CT-tilknytning</span><span class="sxs-lookup"><span data-stu-id="d958c-118">CT mapping</span></span>  

## <a name="bind-created-data-sources-to-data-model-elements"></a><span data-ttu-id="d958c-119">Bind oprettede datakilder til datamodelelementer</span><span class="sxs-lookup"><span data-stu-id="d958c-119">Bind created data sources to data model elements</span></span>
1. <span data-ttu-id="d958c-120">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="d958c-120">Click Designer.</span></span>
2. <span data-ttu-id="d958c-121">Vælg "Afviklingsdato og klokkeslæt(ProcessingDateTime)" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-121">In the tree, select 'Processing date & time(ProcessingDateTime)'.</span></span>
3. <span data-ttu-id="d958c-122">Vælg "Afviklingsdato(ProcessingDateTime)" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-122">In the tree, select 'Processing date(ProcessingDateTime)'.</span></span>
4. <span data-ttu-id="d958c-123">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="d958c-123">Click Bind.</span></span>
5. <span data-ttu-id="d958c-124">Vælg "Identifikation for betalingsmeddelelse(MessageIdentification)" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-124">In the tree, select 'Payment message identification(MessageIdentification)'.</span></span>
6. <span data-ttu-id="d958c-125">Udvid "Transaktioner" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-125">In the tree, expand 'Transactions'.</span></span>
7. <span data-ttu-id="d958c-126">Vælg "Transaktioner\Journalbatchnummer(JournalNum)" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-126">In the tree, select 'Transactions\Journal batch number(JournalNum)'.</span></span>
8. <span data-ttu-id="d958c-127">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="d958c-127">Click Bind.</span></span>
9. <span data-ttu-id="d958c-128">Vælg "Betalinger" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-128">In the tree, select 'Payments'.</span></span>
10. <span data-ttu-id="d958c-129">Vælg "Transaktioner" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-129">In the tree, select 'Transactions'.</span></span>
11. <span data-ttu-id="d958c-130">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="d958c-130">Click Bind.</span></span>
12. <span data-ttu-id="d958c-131">Udvid "Betalinger= Transaktioner" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-131">In the tree, expand 'Payments= Transactions'.</span></span>
13. <span data-ttu-id="d958c-132">Udvid "Betalinger= Transaktioner\Kreditor" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-132">In the tree, expand 'Payments= Transactions\Creditor'.</span></span>
14. <span data-ttu-id="d958c-133">Udvid "Betalinger= Transaktioner\Kreditor\Konto" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-133">In the tree, expand 'Payments= Transactions\Creditor\Account'.</span></span>
15. <span data-ttu-id="d958c-134">Vælg "Betalinger= Transaktioner\Kreditor\Konto\Valutakode(Currency)" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-134">In the tree, select 'Payments= Transactions\Creditor\Account\Currency code(Currency)'.</span></span>
16. <span data-ttu-id="d958c-135">Udvid "Transaktioner\vendBankAccountInTransactionCompany()" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-135">In the tree, expand 'Transactions\vendBankAccountInTransactionCompany()'.</span></span>
17. <span data-ttu-id="d958c-136">Vælg "Transaktioner\vendBankAccountInTransactionCompany()\Currency(CurrencyCode)" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-136">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Currency(CurrencyCode)'.</span></span>
18. <span data-ttu-id="d958c-137">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="d958c-137">Click Bind.</span></span>
19. <span data-ttu-id="d958c-138">Vælg "Betalinger= Transaktioner\Kreditor\Konto\IBAN-kode(IBAN)" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-138">In the tree, select 'Payments= Transactions\Creditor\Account\IBAN code(IBAN)'.</span></span>
20. <span data-ttu-id="d958c-139">Vælg "Transaktioner\vendBankAccountInTransactionCompany()\IBAN(BankIBAN)" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-139">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\IBAN(BankIBAN)'.</span></span>
21. <span data-ttu-id="d958c-140">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="d958c-140">Click Bind.</span></span>
22. <span data-ttu-id="d958c-141">Vælg "Betalinger= Transaktioner\Kreditor\Konto\Nummer" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-141">In the tree, select 'Payments= Transactions\Creditor\Account\Number'.</span></span>
23. <span data-ttu-id="d958c-142">Vælg "Transaktioner\vendBankAccountInTransactionCompany()\Bankkontonummer(AccountNum)" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-142">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Bank account number(AccountNum)'.</span></span>
24. <span data-ttu-id="d958c-143">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="d958c-143">Click Bind.</span></span>
25. <span data-ttu-id="d958c-144">Udvid "Betalinger= Transaktioner\Kreditor\Speditør" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-144">In the tree, expand 'Payments= Transactions\Creditor\Agent'.</span></span>
26. <span data-ttu-id="d958c-145">Vælg "Betalinger= Transaktioner\Kreditor\Konto\Speditør\Navn" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-145">In the tree, select 'Payments= Transactions\Creditor\Agent\Name'.</span></span>
27. <span data-ttu-id="d958c-146">Vælg "Transaktioner\vendBankAccountInTransactionCompany()\Navn" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-146">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Name'.</span></span>
28. <span data-ttu-id="d958c-147">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="d958c-147">Click Bind.</span></span>
29. <span data-ttu-id="d958c-148">Vælg "Betalinger = Transaktioner\Kreditor\Speditør\Registreringsnummer(RoutingNumber)" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-148">In the tree, select 'Payments= Transactions\Creditor\Agent\Routing number(RoutingNumber)'.</span></span>
30. <span data-ttu-id="d958c-149">Vælg "Transaktioner\vendBankAccountInTransactionCompany()\Registreringsnummer(RegistrationNum)" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-149">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Routing number(RegistrationNum)'.</span></span>
31. <span data-ttu-id="d958c-150">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="d958c-150">Click Bind.</span></span>
32. <span data-ttu-id="d958c-151">Vælg "Betalinger= Transaktioner\Kreditor\Speditør\SWIFT-kode(SWIFT)" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-151">In the tree, select 'Payments= Transactions\Creditor\Agent\SWIFT code(SWIFT)'.</span></span>
33. <span data-ttu-id="d958c-152">Vælg "Transaktioner\vendBankAccountInTransactionCompany()\Swift-kode/(SWIFTNo)" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-152">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\SWIFT code(SWIFTNo)'.</span></span>
34. <span data-ttu-id="d958c-153">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="d958c-153">Click Bind.</span></span>
35. <span data-ttu-id="d958c-154">Vælg "Betalinger= Transaktioner\Kreditor\Navn" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-154">In the tree, select 'Payments= Transactions\Creditor\Name'.</span></span>
36. <span data-ttu-id="d958c-155">Udvid "Transaktioner\findVendTable()" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-155">In the tree, expand 'Transactions\findVendTable()'.</span></span>
37. <span data-ttu-id="d958c-156">Vælg "Transaktioner\findVendTable()\ame()" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-156">In the tree, select 'Transactions\findVendTable()\name()'.</span></span>
38. <span data-ttu-id="d958c-157">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="d958c-157">Click Bind.</span></span>
39. <span data-ttu-id="d958c-158">Vælg "Betalinger= Transaktioner\Valutakode(Currency)" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-158">In the tree, select 'Payments= Transactions\Currency code(Currency)'.</span></span>
40. <span data-ttu-id="d958c-159">Udvid "Transaktioner\>Relations" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-159">In the tree, expand 'Transactions\>Relations'.</span></span>
41. <span data-ttu-id="d958c-160">Udvid "Transaktioner\>Relationer\Valutatabel(Currency)" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-160">In the tree, expand 'Transactions\>Relations\Currency table(Currency)'.</span></span>
42. <span data-ttu-id="d958c-161">Vælg "Transaktioner\>Relationer\Valutatabel (Currency)\Valutakode(CurrencyCodeISO)" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-161">In the tree, select 'Transactions\>Relations\Currency table(Currency)\Currency code(CurrencyCodeISO)'.</span></span>
43. <span data-ttu-id="d958c-162">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="d958c-162">Click Bind.</span></span>
44. <span data-ttu-id="d958c-163">Udvid "Betalinger= Transaktioner\Debitor" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-163">In the tree, expand 'Payments= Transactions\Debtor'.</span></span>
45. <span data-ttu-id="d958c-164">Udvid "Betalinger= Transaktioner\Debitor\Konto" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-164">In the tree, expand 'Payments= Transactions\Debtor\Account'.</span></span>
46. <span data-ttu-id="d958c-165">Vælg "Betalinger= Transaktioner\Debitor\Konto\Valutakode(Currency)" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-165">In the tree, select 'Payments= Transactions\Debtor\Account\Currency code(Currency)'.</span></span>
47. <span data-ttu-id="d958c-166">Vælg "Bankkonto(BankAccount)" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-166">In the tree, select 'Bank Account(BankAccount)'.</span></span>
48. <span data-ttu-id="d958c-167">Udvid "Bankkonto(BankAccount)" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-167">In the tree, expand 'Bank Account(BankAccount)'.</span></span>
49. <span data-ttu-id="d958c-168">Vælg "Bankkonto(BankAccount)\Valuta(CurrencyCode)" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-168">In the tree, select 'Bank Account(BankAccount)\Currency(CurrencyCode)'.</span></span>
50. <span data-ttu-id="d958c-169">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="d958c-169">Click Bind.</span></span>
51. <span data-ttu-id="d958c-170">Vælg "Bankkonto(BankAccount)\IBAN" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-170">In the tree, select 'Bank Account(BankAccount)\IBAN'.</span></span>
52. <span data-ttu-id="d958c-171">Vælg "Betalinger= Transaktioner\Debitor\Konto\IBAN-kode(IBAN)" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-171">In the tree, select 'Payments= Transactions\Debtor\Account\IBAN code(IBAN)'.</span></span>
53. <span data-ttu-id="d958c-172">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="d958c-172">Click Bind.</span></span>
54. <span data-ttu-id="d958c-173">Vælg "Betalinger= Transaktioner\Debitor\Konto\Nummer" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-173">In the tree, select 'Payments= Transactions\Debtor\Account\Number'.</span></span>
55. <span data-ttu-id="d958c-174">Vælg "Bankkonto(BankAccount)\Bankkontonummer(AccountNum)" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-174">In the tree, select 'Bank Account(BankAccount)\Bank account number(AccountNum)'.</span></span>
56. <span data-ttu-id="d958c-175">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="d958c-175">Click Bind.</span></span>
57. <span data-ttu-id="d958c-176">Udvid "Betalinger= Transaktioner\Debitor\Speditør" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-176">In the tree, expand 'Payments= Transactions\Debtor\Agent'.</span></span>
58. <span data-ttu-id="d958c-177">Vælg "Betalinger= Transaktioner\Debitor\Speditør\Navn" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-177">In the tree, select 'Payments= Transactions\Debtor\Agent\Name'.</span></span>
59. <span data-ttu-id="d958c-178">Vælg "Bankkonto(BankAccount)\Navn" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-178">In the tree, select 'Bank Account(BankAccount)\Name'.</span></span>
60. <span data-ttu-id="d958c-179">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="d958c-179">Click Bind.</span></span>
61. <span data-ttu-id="d958c-180">Vælg "Betalinger = Transaktioner\Debitor\Speditør\Registreringsnummer(RoutingNumber)" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-180">In the tree, select 'Payments= Transactions\Debtor\Agent\Routing number(RoutingNumber)'.</span></span>
62. <span data-ttu-id="d958c-181">Vælg "Bankkonto(BankAccount)\Registreringsnummer(RegistrationNum)" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-181">In the tree, select 'Bank Account(BankAccount)\Routing number(RegistrationNum)'.</span></span>
63. <span data-ttu-id="d958c-182">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="d958c-182">Click Bind.</span></span>
64. <span data-ttu-id="d958c-183">Vælg "Betalinger= Transaktioner\Debitor\Speditør\SWIFT-kode(SWIFT)" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-183">In the tree, select 'Payments= Transactions\Debtor\Agent\SWIFT code(SWIFT)'.</span></span>
65. <span data-ttu-id="d958c-184">Vælg "Bankkonto(BankAccount)\SWIFT-kode(SWIFTNo)" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-184">In the tree, select 'Bank Account(BankAccount)\SWIFT code(SWIFTNo)'.</span></span>
66. <span data-ttu-id="d958c-185">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="d958c-185">Click Bind.</span></span>
67. <span data-ttu-id="d958c-186">Vælg "Betalinger= Transaktioner\Debitor\Navn" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-186">In the tree, select 'Payments= Transactions\Debtor\Name'.</span></span>
68. <span data-ttu-id="d958c-187">Vælg 'Firmaoplysninger(Company)' i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-187">In the tree, select 'Company information(Company)'.</span></span>
69. <span data-ttu-id="d958c-188">Udvid "Firmaoplysninger(Company)" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-188">In the tree, expand 'Company information(Company)'.</span></span>
70. <span data-ttu-id="d958c-189">Vælg "Firmaoplysninger(Company)\Navn" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-189">In the tree, select 'Company information(Company)\Name'.</span></span>
71. <span data-ttu-id="d958c-190">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="d958c-190">Click Bind.</span></span>
72. <span data-ttu-id="d958c-191">Vælg "Betalinger= Transaktioner\Beskrivelse" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-191">In the tree, select 'Payments= Transactions\Description'.</span></span>
73. <span data-ttu-id="d958c-192">Vælg "Transaktioner\Beskrivelse(Txt)" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-192">In the tree, select 'Transactions\Description(Txt)'.</span></span>
74. <span data-ttu-id="d958c-193">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="d958c-193">Click Bind.</span></span>
75. <span data-ttu-id="d958c-194">Vælg "Betalinger= Transaktioner\Slutpunkt til slutpunkt-identifikationskode(End2EndID)" i træet".</span><span class="sxs-lookup"><span data-stu-id="d958c-194">In the tree, select 'Payments= Transactions\End to end identification code(End2EndID)'.</span></span>
76. <span data-ttu-id="d958c-195">Vælg "Transaktioner\$EndToEndID" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-195">In the tree, select 'Transactions\$EndToEndID'.</span></span>
77. <span data-ttu-id="d958c-196">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="d958c-196">Click Bind.</span></span>
78. <span data-ttu-id="d958c-197">Vælg "Betalinger= Transaktioner\Instrueret beløb(InstructedAmount)" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-197">In the tree, select 'Payments= Transactions\Instructed amount(InstructedAmount)'.</span></span>
79. <span data-ttu-id="d958c-198">Vælg "Transaktioner\$Amount" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-198">In the tree, select 'Transactions\$Amount'.</span></span>
80. <span data-ttu-id="d958c-199">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="d958c-199">Click Bind.</span></span>
81. <span data-ttu-id="d958c-200">Vælg "Betalinger= Transaktioner\Posteringsdato(TransactionDate)" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-200">In the tree, select 'Payments= Transactions\Transaction date(TransactionDate)'.</span></span>
82. <span data-ttu-id="d958c-201">Vælg "Transaktioner\Dato(TransDate)" i træet.</span><span class="sxs-lookup"><span data-stu-id="d958c-201">In the tree, select 'Transactions\Date(TransDate)'.</span></span>
83. <span data-ttu-id="d958c-202">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="d958c-202">Click Bind.</span></span>

## <a name="validate-created-mapping"></a><span data-ttu-id="d958c-203">Valider oprettet tilknytning</span><span class="sxs-lookup"><span data-stu-id="d958c-203">Validate created mapping</span></span>
1. <span data-ttu-id="d958c-204">Klik på Valider.</span><span class="sxs-lookup"><span data-stu-id="d958c-204">Click Validate.</span></span>
    * <span data-ttu-id="d958c-205">Valider den nye tilknytning for at sikre, at alle bindinger er i orden.</span><span class="sxs-lookup"><span data-stu-id="d958c-205">Validate the new mapping to ensure that all bindings are okay.</span></span>  
2. <span data-ttu-id="d958c-206">Klik på pilen for at vise eller skjule sektionen Fejlliste.</span><span class="sxs-lookup"><span data-stu-id="d958c-206">Click the arrow to expand or collapse the Error List section.</span></span>
3. <span data-ttu-id="d958c-207">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="d958c-207">Click Save.</span></span>
4. <span data-ttu-id="d958c-208">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d958c-208">Close the page.</span></span>
5. <span data-ttu-id="d958c-209">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d958c-209">Close the page.</span></span>
6. <span data-ttu-id="d958c-210">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d958c-210">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-model-configuration"></a><span data-ttu-id="d958c-211">Ændr status for den aktuelle version af modelkonfiguration</span><span class="sxs-lookup"><span data-stu-id="d958c-211">Change the status of the current version of model configuration</span></span>
1. <span data-ttu-id="d958c-212">Klik på Skift status.</span><span class="sxs-lookup"><span data-stu-id="d958c-212">Click Change status.</span></span>
    * <span data-ttu-id="d958c-213">Skift status for den designede modelkonfiguration – fra Kladde til Fuldført for at gøre den tilgængelig for oprettelse af betalingsformatdesign.</span><span class="sxs-lookup"><span data-stu-id="d958c-213">Change the status of designed model configuration – from Draft to Completed to make it available for payment format design.</span></span>  
2. <span data-ttu-id="d958c-214">Klik på Fuldført.</span><span class="sxs-lookup"><span data-stu-id="d958c-214">Click Complete.</span></span>
    * <span data-ttu-id="d958c-215">Vælg Fuldfør.</span><span class="sxs-lookup"><span data-stu-id="d958c-215">Select Complete.</span></span>  
3. <span data-ttu-id="d958c-216">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="d958c-216">In the Description field, type a value.</span></span>
    * <span data-ttu-id="d958c-217">For eksempel "version 1".</span><span class="sxs-lookup"><span data-stu-id="d958c-217">For example, 'version 1'.</span></span>  
4. <span data-ttu-id="d958c-218">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d958c-218">Click OK.</span></span>
5. <span data-ttu-id="d958c-219">Vælg den færdige version af den aktuelle konfiguration.</span><span class="sxs-lookup"><span data-stu-id="d958c-219">Select the completed version of the current configuration.</span></span>
    * <span data-ttu-id="d958c-220">Bemærk, at den oprettede konfiguration gemmes som fuldført version 1.</span><span class="sxs-lookup"><span data-stu-id="d958c-220">Note that the created configuration is saved as completed version 1.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]