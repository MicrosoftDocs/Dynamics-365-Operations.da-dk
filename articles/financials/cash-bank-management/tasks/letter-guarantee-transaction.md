--- 
title: Garantipostering
description: "Denne procedure gennemgår garantiprocessen."
author: kweekley
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: Reasons, SalesTableListPage, SalesCreateOrder, SalesTable, BankLGRequestForm, BankLGRequestFormRequest, BankLGGuarantee, BankLGFormSubmitToBank, BankDocumentAgreementLineLookup, BankLGFormReceiveFromBank, LedgerJournalTable, LedgerJournalTransDaily, BankLGRequestFormGiveToBeneficiary, BankLGFormGiveToBeneficiary, BankLGRequestFormIncreaseValue, BankLGFormIncreaseValue, BankLGRequestFormLiquidate, BankLGFormLiquidate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 3b15133106d751c28029862217427e47085044f4
ms.contentlocale: da-dk
ms.lasthandoff: 09/11/2018

---
# <a name="letter-of-guarantee-transaction"></a><span data-ttu-id="09175-103">Garantipostering</span><span class="sxs-lookup"><span data-stu-id="09175-103">Letter of guarantee transaction</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="09175-104">Denne procedure gennemgår garantiprocessen.</span><span class="sxs-lookup"><span data-stu-id="09175-104">This procedure walks through the Letter of guarantee process.</span></span>



<span data-ttu-id="09175-105">Følgende opgaver skal være fuldført, før du fuldfører denne procedure:</span><span class="sxs-lookup"><span data-stu-id="09175-105">The following tasks must be complete before completing this procedure:</span></span>

- <span data-ttu-id="09175-106">Konfigurere bankfaciliteter og posteringsprofiler for en garanti.</span><span class="sxs-lookup"><span data-stu-id="09175-106">Set up bank facilities and posting profiles for a letter of guarantee.</span></span>

- <span data-ttu-id="09175-107">Opret en bankfacilitetsaftale for en garanti.</span><span class="sxs-lookup"><span data-stu-id="09175-107">Create a bank facility agreement for a letter of guarantee.</span></span>



<span data-ttu-id="09175-108">Denne procedure bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="09175-108">This procedure uses the USMF demo company.</span></span>


## <a name="create-sales-order-with-letter-of-guarantee"></a><span data-ttu-id="09175-109">Oprette salgsordre med Garanti</span><span class="sxs-lookup"><span data-stu-id="09175-109">Create Sales Order with Letter of Guarantee</span></span>
1. <span data-ttu-id="09175-110">Gå til Debitor > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="09175-110">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="09175-111">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="09175-111">Click New.</span></span>
3. <span data-ttu-id="09175-112">Indtast eller vælg en værdi i feltet Kundekonto.</span><span class="sxs-lookup"><span data-stu-id="09175-112">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="09175-113">Udvid afsnittet Generelt.</span><span class="sxs-lookup"><span data-stu-id="09175-113">Expand the General section.</span></span>
5. <span data-ttu-id="09175-114">Indtast eller vælg en værdi i feltet Lokation.</span><span class="sxs-lookup"><span data-stu-id="09175-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="09175-115">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="09175-115">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="09175-116">Indtast eller vælg en værdi i feltet Lagersted.</span><span class="sxs-lookup"><span data-stu-id="09175-116">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="09175-117">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="09175-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="09175-118">Vælg Garanti i feltet Bankdokumenttype.</span><span class="sxs-lookup"><span data-stu-id="09175-118">In the Bank document type field, select 'Letter of guarantee'.</span></span>
10. <span data-ttu-id="09175-119">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="09175-119">Click OK.</span></span>
11. <span data-ttu-id="09175-120">Indtast eller vælg en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="09175-120">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="09175-121">Angiv et tal i feltet Enhedspris.</span><span class="sxs-lookup"><span data-stu-id="09175-121">In the Unit price field, enter a number.</span></span>
13. <span data-ttu-id="09175-122">Vis eller skjul sektionen Linjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="09175-122">Expand the Line details section.</span></span>
14. <span data-ttu-id="09175-123">Klik på fanen Levering.</span><span class="sxs-lookup"><span data-stu-id="09175-123">Click the Delivery tab.</span></span>
    * <span data-ttu-id="09175-124">Bemærk! Vælg leveringsdatokontrol = Ingen</span><span class="sxs-lookup"><span data-stu-id="09175-124">Note: Select Delivery date control = None</span></span>  
15. <span data-ttu-id="09175-125">Angiv en dato i feltet Ønsket afsendelsesdato.</span><span class="sxs-lookup"><span data-stu-id="09175-125">In the Requested ship date field, enter a date.</span></span>
16. <span data-ttu-id="09175-126">Angiv en dato i feltet Bekræftet afsendelsesdato.</span><span class="sxs-lookup"><span data-stu-id="09175-126">In the Confirmed ship date field, enter a date.</span></span>

## <a name="process-letter-of-guaranteerequest"></a><span data-ttu-id="09175-127">Behandle garanti_Anmodning</span><span class="sxs-lookup"><span data-stu-id="09175-127">Process letter of guarantee_Request</span></span>
1. <span data-ttu-id="09175-128">Klik på Administrer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="09175-128">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="09175-129">Klik på Garanti.</span><span class="sxs-lookup"><span data-stu-id="09175-129">Click Letter of guarantee.</span></span>
3. <span data-ttu-id="09175-130">I handlingsruden skal du klikke på Garanti.</span><span class="sxs-lookup"><span data-stu-id="09175-130">On the Action Pane, click Letter of guarantee.</span></span>
4. <span data-ttu-id="09175-131">Klik på Anmodning for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="09175-131">Click Request to open the drop dialog.</span></span>
5. <span data-ttu-id="09175-132">Indtast eller vælg en værdi i feltet Type.</span><span class="sxs-lookup"><span data-stu-id="09175-132">In the Type field, enter or select a value.</span></span>
6. <span data-ttu-id="09175-133">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="09175-133">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="09175-134">Angiv et tal i feltet Værdi.</span><span class="sxs-lookup"><span data-stu-id="09175-134">In the Value field, enter a number.</span></span>
8. <span data-ttu-id="09175-135">Angiv dato og klokkeslæt i feltet Udløbsdato.</span><span class="sxs-lookup"><span data-stu-id="09175-135">In the Expiration date field, enter a date and time.</span></span>
9. <span data-ttu-id="09175-136">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="09175-136">Click OK.</span></span>
10. <span data-ttu-id="09175-137">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="09175-137">Close the page.</span></span>

## <a name="process-letter-of-guaranteesubmit-to-bank"></a><span data-ttu-id="09175-138">Behandle anmodning om garanti_Send til bank</span><span class="sxs-lookup"><span data-stu-id="09175-138">Process letter of guarantee_Submit to bank</span></span>
1. <span data-ttu-id="09175-139">Gå til Kontant- og bankstyring > Garantier > Garantier.</span><span class="sxs-lookup"><span data-stu-id="09175-139">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
2. <span data-ttu-id="09175-140">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="09175-140">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="09175-141">Klik på Send til bank for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="09175-141">Click Submit to bank to open the drop dialog.</span></span>
4. <span data-ttu-id="09175-142">Indtast eller vælg en værdi i feltet Bankkonto.</span><span class="sxs-lookup"><span data-stu-id="09175-142">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="09175-143">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="09175-143">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="09175-144">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="09175-144">Click OK.</span></span>

## <a name="process-letter-of-guaranteereceive-from-bank"></a><span data-ttu-id="09175-145">Behandle garanti_Modtag fra bank</span><span class="sxs-lookup"><span data-stu-id="09175-145">Process letter of guarantee_Receive from bank</span></span>
1. <span data-ttu-id="09175-146">Klik på Modtag fra bank for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="09175-146">Click Receive from bank to open the drop dialog.</span></span>
2. <span data-ttu-id="09175-147">Skriv en værdi i feltet Banknummer.</span><span class="sxs-lookup"><span data-stu-id="09175-147">In the Bank number field, type a value.</span></span>
    * <span data-ttu-id="09175-148">Kontrollér værdierne i de beregnede avance- og udgiftsfelter.</span><span class="sxs-lookup"><span data-stu-id="09175-148">Verify the values in the calculated Margin and Expense fields.</span></span>  
3. <span data-ttu-id="09175-149">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="09175-149">Click OK.</span></span>
4. <span data-ttu-id="09175-150">Udvid afsnittet Handlinger.</span><span class="sxs-lookup"><span data-stu-id="09175-150">Expand the Actions section.</span></span>
    * <span data-ttu-id="09175-151">Kontroller posten "Modtag fra bank".</span><span class="sxs-lookup"><span data-stu-id="09175-151">Verify the 'Receive from bank' record.</span></span>  
5. <span data-ttu-id="09175-152">Klik for at følge linket i feltet Kladdebatchnummer.</span><span class="sxs-lookup"><span data-stu-id="09175-152">Click to follow the link in the Journal batch number field.</span></span>
6. <span data-ttu-id="09175-153">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="09175-153">Click Lines.</span></span>
    * <span data-ttu-id="09175-154">Kontrollér bogføringen af kladdeposteringer.</span><span class="sxs-lookup"><span data-stu-id="09175-154">Verify the posting of journal entries.</span></span>  
7. <span data-ttu-id="09175-155">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="09175-155">Close the page.</span></span>

## <a name="process-letter-of-guaranteegive-to-beneficiary"></a><span data-ttu-id="09175-156">Behandle garanti_Giv til modtager</span><span class="sxs-lookup"><span data-stu-id="09175-156">Process letter of guarantee_Give to beneficiary</span></span>
1. <span data-ttu-id="09175-157">Gå til Debitor > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="09175-157">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="09175-158">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="09175-158">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="09175-159">Klik på Administrer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="09175-159">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="09175-160">Klik på Garanti.</span><span class="sxs-lookup"><span data-stu-id="09175-160">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="09175-161">I handlingsruden skal du klikke på Garanti.</span><span class="sxs-lookup"><span data-stu-id="09175-161">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="09175-162">Klik på Giv til modtager for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="09175-162">Click Give to beneficiary to open the drop dialog.</span></span>
7. <span data-ttu-id="09175-163">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="09175-163">Click OK.</span></span>
8. <span data-ttu-id="09175-164">Gå til Kontant- og bankstyring > Garantier > Garantier.</span><span class="sxs-lookup"><span data-stu-id="09175-164">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="09175-165">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="09175-165">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="09175-166">Klik på Giv til modtager for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="09175-166">Click Give to beneficiary to open the drop dialog.</span></span>
11. <span data-ttu-id="09175-167">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="09175-167">Click OK.</span></span>
12. <span data-ttu-id="09175-168">Udvid afsnittet Handlinger.</span><span class="sxs-lookup"><span data-stu-id="09175-168">Expand the Actions section.</span></span>
    * <span data-ttu-id="09175-169">Valider 'Giv til beneficiant'-posten.</span><span class="sxs-lookup"><span data-stu-id="09175-169">Validate the 'Give to beneficiary' record.</span></span>  

## <a name="process-letter-of-guaranteeincrease-value"></a><span data-ttu-id="09175-170">Behandle garanti_Opskriv værdi</span><span class="sxs-lookup"><span data-stu-id="09175-170">Process letter of guarantee_Increase value</span></span>
1. <span data-ttu-id="09175-171">Gå til Debitor > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="09175-171">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="09175-172">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="09175-172">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="09175-173">Klik på Administrer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="09175-173">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="09175-174">Klik på Garanti.</span><span class="sxs-lookup"><span data-stu-id="09175-174">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="09175-175">I handlingsruden skal du klikke på Garanti.</span><span class="sxs-lookup"><span data-stu-id="09175-175">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="09175-176">Klik på Opskriv værdi for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="09175-176">Click Increase value to open the drop dialog.</span></span>
7. <span data-ttu-id="09175-177">Indtast et tal i feltet Værdi, der skal tilføjes.</span><span class="sxs-lookup"><span data-stu-id="09175-177">In the Value to add field, enter a number.</span></span>
8. <span data-ttu-id="09175-178">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="09175-178">Click OK.</span></span>
9. <span data-ttu-id="09175-179">Gå til Kontant- og bankstyring > Garantier > Garantier.</span><span class="sxs-lookup"><span data-stu-id="09175-179">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
10. <span data-ttu-id="09175-180">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="09175-180">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="09175-181">Klik på Opskriv værdi for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="09175-181">Click Increase value to open the drop dialog.</span></span>
12. <span data-ttu-id="09175-182">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="09175-182">Click OK.</span></span>
13. <span data-ttu-id="09175-183">Udvid afsnittet Handlinger.</span><span class="sxs-lookup"><span data-stu-id="09175-183">Expand the Actions section.</span></span>
    * <span data-ttu-id="09175-184">Kontroller posten 'Opskriv værdi'.</span><span class="sxs-lookup"><span data-stu-id="09175-184">Verify the 'Increase value' record.</span></span>  
14. <span data-ttu-id="09175-185">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="09175-185">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="09175-186">Klik for at følge linket i feltet Kladdebatchnummer.</span><span class="sxs-lookup"><span data-stu-id="09175-186">Click to follow the link in the Journal batch number field.</span></span>
16. <span data-ttu-id="09175-187">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="09175-187">Click Lines.</span></span>
    * <span data-ttu-id="09175-188">Kontrollér de bogførte kladdeposteringer.</span><span class="sxs-lookup"><span data-stu-id="09175-188">Verify the posted journal entries.</span></span>  

## <a name="process-letter-of-guaranteeliquidate"></a><span data-ttu-id="09175-189">Behandle garanti_Udfør afvikling</span><span class="sxs-lookup"><span data-stu-id="09175-189">Process letter of guarantee_Liquidate</span></span>
1. <span data-ttu-id="09175-190">Gå til Debitor > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="09175-190">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="09175-191">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="09175-191">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="09175-192">Klik på Administrer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="09175-192">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="09175-193">Klik på Garanti.</span><span class="sxs-lookup"><span data-stu-id="09175-193">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="09175-194">I handlingsruden skal du klikke på Garanti.</span><span class="sxs-lookup"><span data-stu-id="09175-194">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="09175-195">Klik på Udfør afvikling for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="09175-195">Click Liquidate to open the drop dialog.</span></span>
7. <span data-ttu-id="09175-196">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="09175-196">Click OK.</span></span>
8. <span data-ttu-id="09175-197">Gå til Kontant- og bankstyring > Garantier > Garantier.</span><span class="sxs-lookup"><span data-stu-id="09175-197">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="09175-198">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="09175-198">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="09175-199">Klik på Udfør afvikling for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="09175-199">Click Liquidate to open the drop dialog.</span></span>
11. <span data-ttu-id="09175-200">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="09175-200">Click OK.</span></span>
12. <span data-ttu-id="09175-201">Udvid afsnittet Handlinger.</span><span class="sxs-lookup"><span data-stu-id="09175-201">Expand the Actions section.</span></span>
    * <span data-ttu-id="09175-202">Kontroller posten 'Udfør afvikling'.</span><span class="sxs-lookup"><span data-stu-id="09175-202">Verify the 'Liquidate' record.</span></span>  
13. <span data-ttu-id="09175-203">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="09175-203">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="09175-204">Klik for at følge linket i feltet Kladdebatchnummer.</span><span class="sxs-lookup"><span data-stu-id="09175-204">Click to follow the link in the Journal batch number field.</span></span>
15. <span data-ttu-id="09175-205">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="09175-205">Click Lines.</span></span>
    * <span data-ttu-id="09175-206">Kontrollér de bogførte kladdeposteringer.</span><span class="sxs-lookup"><span data-stu-id="09175-206">Verify the posted journal entries.</span></span>  
16. <span data-ttu-id="09175-207">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="09175-207">Close the page.</span></span>


