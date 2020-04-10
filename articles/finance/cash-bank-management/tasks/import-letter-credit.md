---
title: Importér remburs
description: Denne procedure fører dig gennem processen med at importere en remburs.
author: kweekley
manager: AnnBe
ms.date: 02/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, BankLCImport,  PurchEditLines, VendEditInvoice, SrsReportViewerForm, LedgerJournalTable, LedgerJournalTransVendPaym, VendOpenTrans, SysQueryForm, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9f9c73ec1347e72f8cd4ae8eec580bb8fe3df8ed
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141758"
---
# <a name="import-letter-of-credit"></a><span data-ttu-id="d9105-103">Importér remburs</span><span class="sxs-lookup"><span data-stu-id="d9105-103">Import letter of credit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d9105-104">Denne procedure fører dig gennem processen med at importere en remburs.</span><span class="sxs-lookup"><span data-stu-id="d9105-104">This procedure walks through the process of importing a letter of credit.</span></span> <span data-ttu-id="d9105-105">Følgende skal være konfigureret, før du udfører denne procedure: bankfaciliteter, posteringsprofiler, en bankfacilitetsaftale og oplysninger om kreditorbank.</span><span class="sxs-lookup"><span data-stu-id="d9105-105">The following must be set up before completing this procedure: bank facilities, posting profiles, a bank facility agreement and vendor bank details.</span></span>

<span data-ttu-id="d9105-106">Denne procedure bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="d9105-106">This procedure uses the USMF demo company.</span></span>


## <a name="create-a-purchase-order-with-letter-of-credit"></a><span data-ttu-id="d9105-107">Oprette en indkøbsordre med remburs</span><span class="sxs-lookup"><span data-stu-id="d9105-107">Create a Purchase order with Letter of credit</span></span>
1. <span data-ttu-id="d9105-108">Gå til Kreditor > Indkøbsordrer > Alle indkøbsordrer.</span><span class="sxs-lookup"><span data-stu-id="d9105-108">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="d9105-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="d9105-109">Click New.</span></span>
3. <span data-ttu-id="d9105-110">Indtast eller vælg en værdi i feltet Kreditorkonto.</span><span class="sxs-lookup"><span data-stu-id="d9105-110">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="d9105-111">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="d9105-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="d9105-112">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d9105-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="d9105-113">Udvid afsnittet Generelt.</span><span class="sxs-lookup"><span data-stu-id="d9105-113">Expand the General section.</span></span>
7. <span data-ttu-id="d9105-114">Indtast eller vælg en værdi i feltet Lokation.</span><span class="sxs-lookup"><span data-stu-id="d9105-114">In the Site field, enter or select a value.</span></span>
8. <span data-ttu-id="d9105-115">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d9105-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="d9105-116">Indtast eller vælg en værdi i feltet Lagersted.</span><span class="sxs-lookup"><span data-stu-id="d9105-116">In the Warehouse field, enter or select a value.</span></span>
10. <span data-ttu-id="d9105-117">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d9105-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="d9105-118">Angiv en dato i datofeltet Regnskab.</span><span class="sxs-lookup"><span data-stu-id="d9105-118">In the Accounting date field, enter a date.</span></span>
12. <span data-ttu-id="d9105-119">Angiv en dato i feltet Leveringsdato.</span><span class="sxs-lookup"><span data-stu-id="d9105-119">In the Delivery date field, enter a date.</span></span>
    * <span data-ttu-id="d9105-120">Bemærk! Vælg "Remburs" som værdi i feltet "Bankdokumenttype".</span><span class="sxs-lookup"><span data-stu-id="d9105-120">Note: The 'Bank document type' field should be selected with the value  'Letter of credit'.</span></span>  
13. <span data-ttu-id="d9105-121">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d9105-121">Click OK.</span></span>
14. <span data-ttu-id="d9105-122">Indtast eller vælg en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="d9105-122">In the Item number field, enter or select a value.</span></span>
15. <span data-ttu-id="d9105-123">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="d9105-123">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="d9105-124">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d9105-124">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="d9105-125">Vis eller skjul sektionen Linjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="d9105-125">Expand the Line details section.</span></span>
18. <span data-ttu-id="d9105-126">Klik på fanen Levering.</span><span class="sxs-lookup"><span data-stu-id="d9105-126">Click the Delivery tab.</span></span>
19. <span data-ttu-id="d9105-127">Angiv en dato i feltet Leveringsdato.</span><span class="sxs-lookup"><span data-stu-id="d9105-127">In the Delivery date field, enter a date.</span></span>
20. <span data-ttu-id="d9105-128">Angiv en dato i feltet Bekræftet leveringsdato.</span><span class="sxs-lookup"><span data-stu-id="d9105-128">In the Confirmed delivery date field, enter a date.</span></span>
21. <span data-ttu-id="d9105-129">Angiv et tal i feltet Enhedspris.</span><span class="sxs-lookup"><span data-stu-id="d9105-129">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="d9105-130">Definer oplysninger om rembursen.</span><span class="sxs-lookup"><span data-stu-id="d9105-130">Define the Letter of credit details.</span></span>  
22. <span data-ttu-id="d9105-131">Klik på Administrer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="d9105-131">On the Action Pane, click Manage.</span></span>
23. <span data-ttu-id="d9105-132">Klik på Remburs/importinkasso.</span><span class="sxs-lookup"><span data-stu-id="d9105-132">Click Letter of credit / import collection.</span></span>
24. <span data-ttu-id="d9105-133">Angiv en dato og et klokkeslæt i feltet Ansøgningsdato.</span><span class="sxs-lookup"><span data-stu-id="d9105-133">In the Application date field, enter a date and time.</span></span>
    * <span data-ttu-id="d9105-134">Kontroller, at feltet "Bankkonto" har den aktive standardbankkonto, der er baseret på ansøgningsdatoen.</span><span class="sxs-lookup"><span data-stu-id="d9105-134">Verify that the 'Bank account' field has the default active Bank account, which is based on the application date.</span></span>  
25. <span data-ttu-id="d9105-135">Skriv en værdi i feltet Bankdokumentnummer.</span><span class="sxs-lookup"><span data-stu-id="d9105-135">In the Bank document number field, type a value.</span></span>
26. <span data-ttu-id="d9105-136">Angiv en dato og et klokkeslæt i feltet Modtagelsesdato.</span><span class="sxs-lookup"><span data-stu-id="d9105-136">In the Date of receipt field, enter a date and time.</span></span>
27. <span data-ttu-id="d9105-137">Udvid sektionen Bankdokument.</span><span class="sxs-lookup"><span data-stu-id="d9105-137">Expand the Bank document section.</span></span>
28. <span data-ttu-id="d9105-138">Angiv dato og klokkeslæt i feltet Udløbsdato.</span><span class="sxs-lookup"><span data-stu-id="d9105-138">In the Expiration date field, enter a date and time.</span></span>
29. <span data-ttu-id="d9105-139">Udvid sektionen Bankoplysninger.</span><span class="sxs-lookup"><span data-stu-id="d9105-139">Expand the Bank details section.</span></span>
30. <span data-ttu-id="d9105-140">Indtast eller vælg en værdi i feltet Adviserende bank.</span><span class="sxs-lookup"><span data-stu-id="d9105-140">In the Advising bank field, enter or select a value.</span></span>
31. <span data-ttu-id="d9105-141">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d9105-141">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="d9105-142">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="d9105-142">Click Save.</span></span>
33. <span data-ttu-id="d9105-143">Klik på Hent indkøbsordreforsendelser.</span><span class="sxs-lookup"><span data-stu-id="d9105-143">Click Fetch purchase order shipments.</span></span>
34. <span data-ttu-id="d9105-144">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d9105-144">Close the page.</span></span>
35. <span data-ttu-id="d9105-145">Klik på Køb i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="d9105-145">On the Action Pane, click Purchase.</span></span>
36. <span data-ttu-id="d9105-146">Klik på Bekræft.</span><span class="sxs-lookup"><span data-stu-id="d9105-146">Click Confirm.</span></span>
37. <span data-ttu-id="d9105-147">Klik på Administrer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="d9105-147">On the Action Pane, click Manage.</span></span>
38. <span data-ttu-id="d9105-148">Klik på Remburs/importinkasso.</span><span class="sxs-lookup"><span data-stu-id="d9105-148">Click Letter of credit / import collection.</span></span>
39. <span data-ttu-id="d9105-149">Klik på Proces.</span><span class="sxs-lookup"><span data-stu-id="d9105-149">Click Process.</span></span>
40. <span data-ttu-id="d9105-150">Klik på Bekræft.</span><span class="sxs-lookup"><span data-stu-id="d9105-150">Click Confirm.</span></span>
    * <span data-ttu-id="d9105-151">Kontroller, at facilitetssaldoen reducerer beløbet på indkøbsordren.</span><span class="sxs-lookup"><span data-stu-id="d9105-151">Verify that the Facility balance reduces the purchase order amount.</span></span>  <span data-ttu-id="d9105-152">I dette eksempel er Købsbeløb = 500,00 Facilitetsgrænse = 10000,00, og derfor er Facilitetssaldo = 9500,00.</span><span class="sxs-lookup"><span data-stu-id="d9105-152">In this example, Purchase amount = 500.00,  Facility limit = 10000.00,  therefore, Facility balance = 9500.00.</span></span>  
41. <span data-ttu-id="d9105-153">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d9105-153">Close the page.</span></span>
42. <span data-ttu-id="d9105-154">Angiv et tal i feltet Enhedspris.</span><span class="sxs-lookup"><span data-stu-id="d9105-154">In the Unit price field, enter a number.</span></span>
43. <span data-ttu-id="d9105-155">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="d9105-155">Click Save.</span></span>
44. <span data-ttu-id="d9105-156">Klik på Køb i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="d9105-156">On the Action Pane, click Purchase.</span></span>
45. <span data-ttu-id="d9105-157">Klik på Bekræft.</span><span class="sxs-lookup"><span data-stu-id="d9105-157">Click Confirm.</span></span>
    * <span data-ttu-id="d9105-158">Rediger rembursen på grund af ændring i enhedsprisen.</span><span class="sxs-lookup"><span data-stu-id="d9105-158">Amend the Letter of credit, due to the change in Unit price.</span></span>  
46. <span data-ttu-id="d9105-159">Klik på Administrer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="d9105-159">On the Action Pane, click Manage.</span></span>
47. <span data-ttu-id="d9105-160">Klik på Remburs/importinkasso.</span><span class="sxs-lookup"><span data-stu-id="d9105-160">Click Letter of credit / import collection.</span></span>
    * <span data-ttu-id="d9105-161">Rediger rembursen på grund af ændring i Købsenhedspris.</span><span class="sxs-lookup"><span data-stu-id="d9105-161">Amend the letter of credit, due to the change in Purchase unit price.</span></span>  
48. <span data-ttu-id="d9105-162">Klik på Proces.</span><span class="sxs-lookup"><span data-stu-id="d9105-162">Click Process.</span></span>
49. <span data-ttu-id="d9105-163">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="d9105-163">Click Amend.</span></span>
50. <span data-ttu-id="d9105-164">Klik på Fjern.</span><span class="sxs-lookup"><span data-stu-id="d9105-164">Click Remove.</span></span>
51. <span data-ttu-id="d9105-165">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="d9105-165">Click Yes.</span></span>
52. <span data-ttu-id="d9105-166">Klik på Hent indkøbsordreforsendelser.</span><span class="sxs-lookup"><span data-stu-id="d9105-166">Click Fetch purchase order shipments.</span></span>
53. <span data-ttu-id="d9105-167">Klik på Proces.</span><span class="sxs-lookup"><span data-stu-id="d9105-167">Click Process.</span></span>
54. <span data-ttu-id="d9105-168">Klik på Bekræft.</span><span class="sxs-lookup"><span data-stu-id="d9105-168">Click Confirm.</span></span>
    * <span data-ttu-id="d9105-169">Kontroller, at facilitetssaldoen reducerer beløbet på indkøbsordren.</span><span class="sxs-lookup"><span data-stu-id="d9105-169">Verify that the Facility balance reduces the purchase order amount.</span></span>  <span data-ttu-id="d9105-170">I dette eksempel er redigeret Købsbeløb = 600,00 Facilitetsgrænse = 10000,00, og derfor er Facilitetssaldo = 9400,00.</span><span class="sxs-lookup"><span data-stu-id="d9105-170">In this example, edited Purchase amount = 600.00,  Facility limit = 10000.00,  therefore, Facility balance = 9400.00.</span></span>  
55. <span data-ttu-id="d9105-171">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d9105-171">Close the page.</span></span>

## <a name="post-packing-slip"></a><span data-ttu-id="d9105-172">Bogføre følgeseddel</span><span class="sxs-lookup"><span data-stu-id="d9105-172">Post Packing slip</span></span>
1. <span data-ttu-id="d9105-173">Klik på Modtag i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="d9105-173">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="d9105-174">Klik på Produktkvittering.</span><span class="sxs-lookup"><span data-stu-id="d9105-174">Click Product receipt.</span></span>
3. <span data-ttu-id="d9105-175">Skriv en værdi i feltet PurchParmTable_Num.</span><span class="sxs-lookup"><span data-stu-id="d9105-175">In the PurchParmTable_Num field, type a value.</span></span>
    * <span data-ttu-id="d9105-176">Vælg det forsendelsesnummer, der blev oprettet med reference til rembursen.</span><span class="sxs-lookup"><span data-stu-id="d9105-176">Select the Shipment number created with reference to the Letter of credit.</span></span>  
4. <span data-ttu-id="d9105-177">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d9105-177">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="d9105-178">Angiv en dato i feltet Produktkvittering.</span><span class="sxs-lookup"><span data-stu-id="d9105-178">In the Product receipt date field, enter a date.</span></span>
6. <span data-ttu-id="d9105-179">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d9105-179">Click OK.</span></span>
7. <span data-ttu-id="d9105-180">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d9105-180">Close the page.</span></span>
8. <span data-ttu-id="d9105-181">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d9105-181">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status"></a><span data-ttu-id="d9105-182">Bekræfte status for importremburs</span><span class="sxs-lookup"><span data-stu-id="d9105-182">Verify Import letter of credit status</span></span>
1. <span data-ttu-id="d9105-183">Gå til Likviditets- og bankstyring > Remburser > Importremburs og importinkasso.</span><span class="sxs-lookup"><span data-stu-id="d9105-183">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="d9105-184">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="d9105-184">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="d9105-185">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d9105-185">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="d9105-186">Bekræft status for importrembursen.</span><span class="sxs-lookup"><span data-stu-id="d9105-186">Verify the Import letter of credit status.</span></span>     
4. <span data-ttu-id="d9105-187">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d9105-187">Close the page.</span></span>
5. <span data-ttu-id="d9105-188">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d9105-188">Close the page.</span></span>

## <a name="post-purchase-invoice"></a><span data-ttu-id="d9105-189">Bogføre købsfaktura</span><span class="sxs-lookup"><span data-stu-id="d9105-189">Post purchase invoice</span></span>
1. <span data-ttu-id="d9105-190">Gå til Kreditor > Indkøbsordrer > Alle indkøbsordrer.</span><span class="sxs-lookup"><span data-stu-id="d9105-190">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
    * <span data-ttu-id="d9105-191">Vælg den indkøbsordre, der blev oprettet med remburs.</span><span class="sxs-lookup"><span data-stu-id="d9105-191">Select the purchase order that was created with letter of credit.</span></span>  
2. <span data-ttu-id="d9105-192">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="d9105-192">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="d9105-193">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d9105-193">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="d9105-194">Klik på Faktura i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="d9105-194">On the Action Pane, click Invoice.</span></span>
5. <span data-ttu-id="d9105-195">Klik på Faktura.</span><span class="sxs-lookup"><span data-stu-id="d9105-195">Click Invoice.</span></span>
6. <span data-ttu-id="d9105-196">Skriv en værdi i feltet Nummer.</span><span class="sxs-lookup"><span data-stu-id="d9105-196">In the Number field, type a value.</span></span>
7. <span data-ttu-id="d9105-197">Indtast eller vælg en værdi i feltet Forsendelsesnummer.</span><span class="sxs-lookup"><span data-stu-id="d9105-197">In the Shipment number field, enter or select a value.</span></span>
8. <span data-ttu-id="d9105-198">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d9105-198">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="d9105-199">Indtast en dato i feltet Fakturadato.</span><span class="sxs-lookup"><span data-stu-id="d9105-199">In the Invoice date field, enter a date.</span></span>
10. <span data-ttu-id="d9105-200">Klik på Opdater status for sammenholdelse.</span><span class="sxs-lookup"><span data-stu-id="d9105-200">Click Update match status.</span></span>
11. <span data-ttu-id="d9105-201">Klik på Bogfør.</span><span class="sxs-lookup"><span data-stu-id="d9105-201">Click Post.</span></span>
12. <span data-ttu-id="d9105-202">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d9105-202">Close the page.</span></span>
13. <span data-ttu-id="d9105-203">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d9105-203">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status"></a><span data-ttu-id="d9105-204">Bekræfte status for importremburs</span><span class="sxs-lookup"><span data-stu-id="d9105-204">Verify Import letter of credit status</span></span>
1. <span data-ttu-id="d9105-205">Gå til Likviditets- og bankstyring > Remburser > Importremburs og importinkasso.</span><span class="sxs-lookup"><span data-stu-id="d9105-205">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="d9105-206">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="d9105-206">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="d9105-207">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d9105-207">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="d9105-208">Bekræft importrembursen2.</span><span class="sxs-lookup"><span data-stu-id="d9105-208">Verify the Import letter of credit2.</span></span>  
    * <span data-ttu-id="d9105-209">Valider: Forsendelsesstatus = Oplysninger om bankfacilitet for faktura</span><span class="sxs-lookup"><span data-stu-id="d9105-209">Validate :  Shipment status = Invoiced  Bank facility details</span></span>  
4. <span data-ttu-id="d9105-210">Klik på Vis.</span><span class="sxs-lookup"><span data-stu-id="d9105-210">Click View.</span></span>
5. <span data-ttu-id="d9105-211">Klik på Udskriv ansøgning.</span><span class="sxs-lookup"><span data-stu-id="d9105-211">Click Print application.</span></span>
6. <span data-ttu-id="d9105-212">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d9105-212">Click OK.</span></span>
    * <span data-ttu-id="d9105-213">Kontroller, at rembursansøgningen bliver udskrevet.</span><span class="sxs-lookup"><span data-stu-id="d9105-213">Verify that the Letter of credit application gets printed.</span></span>  
7. <span data-ttu-id="d9105-214">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d9105-214">Close the page.</span></span>
8. <span data-ttu-id="d9105-215">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d9105-215">Close the page.</span></span>
9. <span data-ttu-id="d9105-216">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d9105-216">Close the page.</span></span>

## <a name="post-vendor-payment-journal-for-the-created-purchase-invoice-with-letter-of-credit"></a><span data-ttu-id="d9105-217">Bogføre kreditorbetalingskladde for indkøbsordre, der er oprettet med remburs</span><span class="sxs-lookup"><span data-stu-id="d9105-217">Post Vendor payment journal for the created purchase invoice with letter of credit</span></span>
1. <span data-ttu-id="d9105-218">Gå til Kreditor > Betalinger > Betalingskladde.</span><span class="sxs-lookup"><span data-stu-id="d9105-218">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="d9105-219">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="d9105-219">Click New.</span></span>
3. <span data-ttu-id="d9105-220">Indtast eller vælg en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="d9105-220">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="d9105-221">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d9105-221">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="d9105-222">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="d9105-222">Click Lines.</span></span>
6. <span data-ttu-id="d9105-223">Indtast en dato i feltet Dato.</span><span class="sxs-lookup"><span data-stu-id="d9105-223">In the Date field, enter a date.</span></span>
7. <span data-ttu-id="d9105-224">I feltet Konto skal du specificere de ønskede værdier.</span><span class="sxs-lookup"><span data-stu-id="d9105-224">In the Account field, specify the desired values.</span></span>
8. <span data-ttu-id="d9105-225">Klik på Udlign transaktioner.</span><span class="sxs-lookup"><span data-stu-id="d9105-225">Click Settle transactions.</span></span>
9. <span data-ttu-id="d9105-226">Udvid afsnittet Totaler.</span><span class="sxs-lookup"><span data-stu-id="d9105-226">Expand the Totals section.</span></span>
10. <span data-ttu-id="d9105-227">Vælg en indstilling i feltet Vis.</span><span class="sxs-lookup"><span data-stu-id="d9105-227">In the Show field, select an option.</span></span>
    * <span data-ttu-id="d9105-228">Kontroller, at felterne Bankdokumentnummer og Forsendelsesnummer er blevet opdateret.</span><span class="sxs-lookup"><span data-stu-id="d9105-228">Verify that the Bank document number and Shipment number fields have been updated.</span></span>  
11. <span data-ttu-id="d9105-229">Marker afkrydsningsfeltet Marker.</span><span class="sxs-lookup"><span data-stu-id="d9105-229">Select the Mark check box.</span></span>
12. <span data-ttu-id="d9105-230">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d9105-230">Click OK.</span></span>
13. <span data-ttu-id="d9105-231">Klik på fanen Betaling.</span><span class="sxs-lookup"><span data-stu-id="d9105-231">Click the Payment tab.</span></span>
    * <span data-ttu-id="d9105-232">Kontroller, at felterne Bankdokumentnummer og Forsendelsesnummer er blevet opdateret.</span><span class="sxs-lookup"><span data-stu-id="d9105-232">Verify that the Bank document number and Shipment number fields have been updated.</span></span>  
14. <span data-ttu-id="d9105-233">Klik på Bogfør.</span><span class="sxs-lookup"><span data-stu-id="d9105-233">Click Post.</span></span>
15. <span data-ttu-id="d9105-234">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d9105-234">Close the page.</span></span>
16. <span data-ttu-id="d9105-235">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d9105-235">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status-after-invoice-paid"></a><span data-ttu-id="d9105-236">Bekræfte status for importremburs, når fakturaen er betalt</span><span class="sxs-lookup"><span data-stu-id="d9105-236">Verify Import letter of credit status after Invoice paid</span></span>
1. <span data-ttu-id="d9105-237">Gå til Likviditets- og bankstyring > Remburser > Importremburs og importinkasso.</span><span class="sxs-lookup"><span data-stu-id="d9105-237">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="d9105-238">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="d9105-238">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="d9105-239">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d9105-239">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="d9105-240">Bekræft status for importrembursen.</span><span class="sxs-lookup"><span data-stu-id="d9105-240">Verify the Import letter of credit status.</span></span>   
4. <span data-ttu-id="d9105-241">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d9105-241">Close the page.</span></span>

## <a name="verify-the-bank-facility-limit-and-utilization-report"></a><span data-ttu-id="d9105-242">Kontrollere rapport om bankfacilitetsgrænse og udnyttelse</span><span class="sxs-lookup"><span data-stu-id="d9105-242">Verify the Bank facility limit and utilization report</span></span>
1. <span data-ttu-id="d9105-243">Gå til Likviditets- og bankstyring > Forespørgsler og rapporter > Remburser eller garanti > Bankfaciliteter og udnyttelse, rapport.</span><span class="sxs-lookup"><span data-stu-id="d9105-243">Go to Cash and bank management > Inquiries and reports > Letters of credit or guarantee > Bank facilities and utilization report.</span></span>
2. <span data-ttu-id="d9105-244">Udvid posterne for at inkludere sektion.</span><span class="sxs-lookup"><span data-stu-id="d9105-244">Expand the Records to include section.</span></span>
3. <span data-ttu-id="d9105-245">Klik på Filtrér.</span><span class="sxs-lookup"><span data-stu-id="d9105-245">Click Filter.</span></span>
    * <span data-ttu-id="d9105-246">Definer feltet Kriterier med den ønskede bankkonto.</span><span class="sxs-lookup"><span data-stu-id="d9105-246">Define the Criteria field with the required bank account.</span></span>  
4. <span data-ttu-id="d9105-247">Indtast eller vælg en værdi i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="d9105-247">In the Criteria field, enter or select a value.</span></span>
5. <span data-ttu-id="d9105-248">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d9105-248">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="d9105-249">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d9105-249">Click OK.</span></span>
7. <span data-ttu-id="d9105-250">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d9105-250">Click OK.</span></span>
    * <span data-ttu-id="d9105-251">Kontroller den rapport, som viser posteringerne.</span><span class="sxs-lookup"><span data-stu-id="d9105-251">Verify the report which lists the transactions.</span></span>  
    * <span data-ttu-id="d9105-252">Kontrol af rapporten viser posteringerne med bankdokumentnummer, facilitetsgrænse, udnyttet beløb og facilitetssaldobeløb.</span><span class="sxs-lookup"><span data-stu-id="d9105-252">Verify the report lists the transactions with Bank document number, Facility limit, utilized amount and the facility balance amount.</span></span>  
8. <span data-ttu-id="d9105-253">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d9105-253">Close the page.</span></span>

