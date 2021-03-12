---
title: Eksportér remburs
description: Denne procedure fører dig gennem processen med at eksportrembursen.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, DefaultDashboard, SalesTableListPage, SalesCreateOrder, SalesTable, BankLCExport, SalesEditLines,  LedgerJournalTable, LedgerJournalTransCustPaym, CustOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5b46ba174d658d27f5349762f3314ea8110490d2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976385"
---
# <a name="export-letter-of-credit"></a><span data-ttu-id="b95c8-103">Eksportér remburs</span><span class="sxs-lookup"><span data-stu-id="b95c8-103">Export letter of credit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b95c8-104">Denne procedure fører dig gennem processen med at eksportrembursen.</span><span class="sxs-lookup"><span data-stu-id="b95c8-104">This procedure walks through the process of the Export letter of credit.</span></span>

<span data-ttu-id="b95c8-105">En remburs er en aftale, der udfærdiges af en bank, hvor banken accepterer at sikre betaling på vegne af køberen, hvis vilkårene i aftalen mellem køberen og sælgeren overholdes.</span><span class="sxs-lookup"><span data-stu-id="b95c8-105">A letter of credit is an agreement that is issued by a bank, in which the bank agrees to ensure payment on behalf of the buyer, if the terms of the agreement between the buyer and seller are met.</span></span>



<span data-ttu-id="b95c8-106">Kør proceduren "Konfigurere bankfaciliteter og posteringsprofiler" og "Remburs_Oprette en bankfacilitetsaftale" inden denne procedure.</span><span class="sxs-lookup"><span data-stu-id="b95c8-106">Run the 'Set up bank facilities and posting profiles' procedure and the 'Letter of Credit_Create a bank facility agreement' procedure prior to this procedure.</span></span> <span data-ttu-id="b95c8-107">USMF-demovirksomheden skal være valgt for at køre denne procedure.</span><span class="sxs-lookup"><span data-stu-id="b95c8-107">The USMF demo company must be selected in order to run this procedure successfully.</span></span>




## <a name="create-sales-order-for-export-letter-of-credit"></a><span data-ttu-id="b95c8-108">Oprette salgsordre for remburs</span><span class="sxs-lookup"><span data-stu-id="b95c8-108">Create Sales Order for Export letter of credit</span></span>
1. <span data-ttu-id="b95c8-109">Gå til Debitor > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="b95c8-109">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="b95c8-110">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="b95c8-110">Click New.</span></span>
3. <span data-ttu-id="b95c8-111">Klik på rullelisten i feltet Kundekonto for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="b95c8-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="b95c8-112">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="b95c8-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="b95c8-113">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="b95c8-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="b95c8-114">Udvis eller skjul sektionen Generelt.</span><span class="sxs-lookup"><span data-stu-id="b95c8-114">Expand or collapse the General section.</span></span>
7. <span data-ttu-id="b95c8-115">Klik på rullelisten i feltet Sted for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="b95c8-115">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="b95c8-116">Vælg den lokation, hvor varen, som skal udleveres, opbevares.</span><span class="sxs-lookup"><span data-stu-id="b95c8-116">Select the Site where the item to be issued is stocked.</span></span>  
8. <span data-ttu-id="b95c8-117">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="b95c8-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="b95c8-118">Klik på rullelisten i feltet Lagersted for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="b95c8-118">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="b95c8-119">Vælg det lagersted, hvor varen, som skal udleveres, opbevares.</span><span class="sxs-lookup"><span data-stu-id="b95c8-119">Select the Warehouse where item to be issued is stocked.</span></span>  
10. <span data-ttu-id="b95c8-120">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="b95c8-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b95c8-121">Bemærk! Vælg "Remburs" som værdi i feltet "Bankdokumenttype".</span><span class="sxs-lookup"><span data-stu-id="b95c8-121">Note: The Bank document type field should be selected with the value 'Letter of credit'.</span></span>  
11. <span data-ttu-id="b95c8-122">Vælg Remburs i feltet Bankdokumenttype.</span><span class="sxs-lookup"><span data-stu-id="b95c8-122">In the Bank document type field, select 'Letter of credit'.</span></span>
12. <span data-ttu-id="b95c8-123">Udvid eller skjul sektionen Levering.</span><span class="sxs-lookup"><span data-stu-id="b95c8-123">Expand or collapse the Delivery section.</span></span>
    * <span data-ttu-id="b95c8-124">Vælg leveringsdatokontrol = Ingen.</span><span class="sxs-lookup"><span data-stu-id="b95c8-124">Select Delivery date control = None.</span></span>  
13. <span data-ttu-id="b95c8-125">Angiv en dato i feltet Ønsket modtagelsesdato.</span><span class="sxs-lookup"><span data-stu-id="b95c8-125">In the Requested receipt date field, enter a date.</span></span>
14. <span data-ttu-id="b95c8-126">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="b95c8-126">Click OK.</span></span>
15. <span data-ttu-id="b95c8-127">Klik på rullelisten i feltet Varenummer for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="b95c8-127">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="b95c8-128">Vælg den ønskede vare, som skal være udleveres/sælges.</span><span class="sxs-lookup"><span data-stu-id="b95c8-128">Select the required item to be Issued/Sold.</span></span>  
16. <span data-ttu-id="b95c8-129">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="b95c8-129">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="b95c8-130">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="b95c8-130">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="b95c8-131">Angiv et nummer i feltet Enhedspris.</span><span class="sxs-lookup"><span data-stu-id="b95c8-131">In the Unit price field, enter a number.</span></span>
19. <span data-ttu-id="b95c8-132">Udvis eller skjul sektionen Linedetaljer.</span><span class="sxs-lookup"><span data-stu-id="b95c8-132">Expand or collapse the Line details section.</span></span>
20. <span data-ttu-id="b95c8-133">Klik på fanen Levering.</span><span class="sxs-lookup"><span data-stu-id="b95c8-133">Click the Delivery tab.</span></span>
21. <span data-ttu-id="b95c8-134">Angiv en dato i feltet Ønsket afsendelsesdato.</span><span class="sxs-lookup"><span data-stu-id="b95c8-134">In the Requested ship date field, enter a date.</span></span>
22. <span data-ttu-id="b95c8-135">Angiv en dato i feltet Bekræftet afsendelsesdato.</span><span class="sxs-lookup"><span data-stu-id="b95c8-135">In the Confirmed ship date field, enter a date.</span></span>
23. <span data-ttu-id="b95c8-136">Klik på Administrer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="b95c8-136">On the Action Pane, click Manage.</span></span>
24. <span data-ttu-id="b95c8-137">Klik på Remburs.</span><span class="sxs-lookup"><span data-stu-id="b95c8-137">Click Letter of credit.</span></span>
25. <span data-ttu-id="b95c8-138">Skriv en værdi i feltet Bankdokumentnummer.</span><span class="sxs-lookup"><span data-stu-id="b95c8-138">In the Bank document number field, type a value.</span></span>
26. <span data-ttu-id="b95c8-139">Angiv dato og klokkeslæt i feltet Udløbsdato.</span><span class="sxs-lookup"><span data-stu-id="b95c8-139">In the Expiration date field, enter a date and time.</span></span>
27. <span data-ttu-id="b95c8-140">Udvid eller skjul sektionen Bankoplysninger.</span><span class="sxs-lookup"><span data-stu-id="b95c8-140">Expand or collapse the Bank details section.</span></span>
28. <span data-ttu-id="b95c8-141">Klik på rullelisten i feltet Udstedende bank for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="b95c8-141">In the Issuing bank field, click the drop-down button to open the lookup.</span></span>
29. <span data-ttu-id="b95c8-142">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="b95c8-142">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="b95c8-143">Klik på rullelisten i feltet Adviserende bank for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="b95c8-143">In the Advising bank field, click the drop-down button to open the lookup.</span></span>
31. <span data-ttu-id="b95c8-144">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="b95c8-144">In the list, find and select the desired record.</span></span>
32. <span data-ttu-id="b95c8-145">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="b95c8-145">In the list, click the link in the selected row.</span></span>
33. <span data-ttu-id="b95c8-146">Klik på Hent salgsordreforsendelser.</span><span class="sxs-lookup"><span data-stu-id="b95c8-146">Click Fetch sales order shipments.</span></span>
34. <span data-ttu-id="b95c8-147">Klik på Udsted bankdokument.</span><span class="sxs-lookup"><span data-stu-id="b95c8-147">Click Issue bank document.</span></span>
35. <span data-ttu-id="b95c8-148">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="b95c8-148">Close the page.</span></span>

## <a name="post-packing-slip"></a><span data-ttu-id="b95c8-149">Bogføre følgeseddel</span><span class="sxs-lookup"><span data-stu-id="b95c8-149">Post Packing slip</span></span>
1. <span data-ttu-id="b95c8-150">Klik på fanen Pluk og pak i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="b95c8-150">On the Action Pane, click Pick and pack.</span></span>
2. <span data-ttu-id="b95c8-151">Klik på Bogfør følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="b95c8-151">Click Post packing slip.</span></span>
3. <span data-ttu-id="b95c8-152">Udvid eller skjul sektionen Parametre.</span><span class="sxs-lookup"><span data-stu-id="b95c8-152">Expand or collapse the Parameters section.</span></span>
4. <span data-ttu-id="b95c8-153">Vælg "Alle" i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="b95c8-153">In the Quantity field, select 'All'.</span></span>
5. <span data-ttu-id="b95c8-154">Udvid eller skjul sektionen Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="b95c8-154">Expand or collapse the Setup section.</span></span>
6. <span data-ttu-id="b95c8-155">Angiv en dato i feltet Følgeseddeldato.</span><span class="sxs-lookup"><span data-stu-id="b95c8-155">In the Packing slip date field, enter a date.</span></span>
7. <span data-ttu-id="b95c8-156">Vælg Forsendelsesnummer.</span><span class="sxs-lookup"><span data-stu-id="b95c8-156">Select the Shipment number.</span></span>
8. <span data-ttu-id="b95c8-157">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="b95c8-157">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="b95c8-158">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="b95c8-158">Click OK.</span></span>
10. <span data-ttu-id="b95c8-159">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="b95c8-159">Click OK.</span></span>

## <a name="post-sales-invoice"></a><span data-ttu-id="b95c8-160">Bogføre salgsfaktura</span><span class="sxs-lookup"><span data-stu-id="b95c8-160">Post sales invoice</span></span>
1. <span data-ttu-id="b95c8-161">Klik på Faktura i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="b95c8-161">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="b95c8-162">Klik på Faktura.</span><span class="sxs-lookup"><span data-stu-id="b95c8-162">Click Invoice.</span></span>
3. <span data-ttu-id="b95c8-163">Udvid eller skjul sektionen Oversigt.</span><span class="sxs-lookup"><span data-stu-id="b95c8-163">Expand or collapse the Overview section.</span></span>
4. <span data-ttu-id="b95c8-164">Vælg Forsendelsesnummer.</span><span class="sxs-lookup"><span data-stu-id="b95c8-164">Select the Shipment number.</span></span>
5. <span data-ttu-id="b95c8-165">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="b95c8-165">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="b95c8-166">Udvid eller skjul sektionen Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="b95c8-166">Expand or collapse the Setup section.</span></span>
7. <span data-ttu-id="b95c8-167">Indtast en dato i feltet Fakturadato.</span><span class="sxs-lookup"><span data-stu-id="b95c8-167">In the Invoice date field, enter a date.</span></span>
8. <span data-ttu-id="b95c8-168">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="b95c8-168">Click OK.</span></span>
9. <span data-ttu-id="b95c8-169">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="b95c8-169">Click OK.</span></span>

## <a name="shipment-document-submitted-status"></a><span data-ttu-id="b95c8-170">Afsendelsesstatus for forsendelsesdokument</span><span class="sxs-lookup"><span data-stu-id="b95c8-170">Shipment document submitted status</span></span>
1. <span data-ttu-id="b95c8-171">Klik på Administrer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="b95c8-171">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="b95c8-172">Klik på Remburs.</span><span class="sxs-lookup"><span data-stu-id="b95c8-172">Click Letter of credit.</span></span>
3. <span data-ttu-id="b95c8-173">Udvid eller skjul sektionen Linjer.</span><span class="sxs-lookup"><span data-stu-id="b95c8-173">Expand or collapse the Lines section.</span></span>
    * <span data-ttu-id="b95c8-174">Bemærk! Feltet "Dokument sendt" skal indstilles til Ja.</span><span class="sxs-lookup"><span data-stu-id="b95c8-174">Note: The 'Document submitted' field should be set to 'Yes'.</span></span>  

## <a name="verify-export-letter-of-credit"></a><span data-ttu-id="b95c8-175">Kontrollere remburs</span><span class="sxs-lookup"><span data-stu-id="b95c8-175">Verify Export letter of credit</span></span>
1. <span data-ttu-id="b95c8-176">Gå til Likviditets- og bankstyring > Remburser > Eksportremburs og importinkasso.</span><span class="sxs-lookup"><span data-stu-id="b95c8-176">Go to Cash and bank management > Letters of credit > Export letter of credit and import collection.</span></span>
2. <span data-ttu-id="b95c8-177">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="b95c8-177">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="b95c8-178">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="b95c8-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b95c8-179">Kontroller, at forsendelsesstatus for eksportrembursen er Faktureret.</span><span class="sxs-lookup"><span data-stu-id="b95c8-179">Verify that the Export letter of credit has a Shipment status of 'Invoiced'.</span></span>  

## <a name="customer-payment"></a><span data-ttu-id="b95c8-180">Debitorbetaling</span><span class="sxs-lookup"><span data-stu-id="b95c8-180">Customer payment</span></span>
1. <span data-ttu-id="b95c8-181">Gå til Kreditor > Betalinger > Betalingskladde.</span><span class="sxs-lookup"><span data-stu-id="b95c8-181">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="b95c8-182">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="b95c8-182">Click New.</span></span>
3. <span data-ttu-id="b95c8-183">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="b95c8-183">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="b95c8-184">Klik på rullelisten i feltet Navn for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="b95c8-184">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="b95c8-185">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="b95c8-185">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="b95c8-186">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="b95c8-186">Click Lines.</span></span>
7. <span data-ttu-id="b95c8-187">Indtast en dato i feltet Dato.</span><span class="sxs-lookup"><span data-stu-id="b95c8-187">In the Date field, enter a date.</span></span>
8. <span data-ttu-id="b95c8-188">I feltet Konto skal du specificere de ønskede værdier.</span><span class="sxs-lookup"><span data-stu-id="b95c8-188">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="b95c8-189">Klik på Udligning.</span><span class="sxs-lookup"><span data-stu-id="b95c8-189">Click Settlement.</span></span>
10. <span data-ttu-id="b95c8-190">Markér afkrydsningsfeltet på overskriften til Totaler.</span><span class="sxs-lookup"><span data-stu-id="b95c8-190">Select the check box on the header of Totals.</span></span>
    * <span data-ttu-id="b95c8-191">Bemærk! Indstil feltet Vis til Remburs.</span><span class="sxs-lookup"><span data-stu-id="b95c8-191">Note: Set the Show field to 'Letter of credit'.</span></span>  
11. <span data-ttu-id="b95c8-192">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="b95c8-192">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="b95c8-193">Markér eller fjern markeringen i afkrydsningsfeltet Markér.</span><span class="sxs-lookup"><span data-stu-id="b95c8-193">Select or clear the Mark check box.</span></span>
13. <span data-ttu-id="b95c8-194">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="b95c8-194">Click OK.</span></span>
14. <span data-ttu-id="b95c8-195">Klik på fanen Betaling.</span><span class="sxs-lookup"><span data-stu-id="b95c8-195">Click the Payment tab.</span></span>
    * <span data-ttu-id="b95c8-196">Kontroller oplysninger om bankdokumentnummer og forsendelsesnummer</span><span class="sxs-lookup"><span data-stu-id="b95c8-196">Verify Bank document number and Shipment number details</span></span>  
15. <span data-ttu-id="b95c8-197">Klik på Bogfør.</span><span class="sxs-lookup"><span data-stu-id="b95c8-197">Click Post.</span></span>

## <a name="verify-export-letter-of-credit-after-payment"></a><span data-ttu-id="b95c8-198">Kontrollere eksportrembursen efter betaling</span><span class="sxs-lookup"><span data-stu-id="b95c8-198">Verify Export letter of credit after payment</span></span>
1. <span data-ttu-id="b95c8-199">Gå til Likviditets- og bankstyring > Remburser > Eksportremburs og importinkasso.</span><span class="sxs-lookup"><span data-stu-id="b95c8-199">Go to Cash and bank management > Letters of credit > Export letter of credit and import collection.</span></span>
2. <span data-ttu-id="b95c8-200">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="b95c8-200">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="b95c8-201">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="b95c8-201">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b95c8-202">Kontroller Forsendelsesstatus = Betaling modtaget og saldobeløb = 0,00.</span><span class="sxs-lookup"><span data-stu-id="b95c8-202">Verify Shipment status = Payment received and balance amount = 0.00.</span></span>  

