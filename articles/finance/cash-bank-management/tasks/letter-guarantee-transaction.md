---
title: Garantipostering
description: Denne procedure gennemgår garantiprocessen.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Reasons, SalesTableListPage, SalesCreateOrder, SalesTable, BankLGRequestForm, BankLGRequestFormRequest, BankLGGuarantee, BankLGFormSubmitToBank, BankDocumentAgreementLineLookup, BankLGFormReceiveFromBank, LedgerJournalTable, LedgerJournalTransDaily, BankLGRequestFormGiveToBeneficiary, BankLGFormGiveToBeneficiary, BankLGRequestFormIncreaseValue, BankLGFormIncreaseValue, BankLGRequestFormLiquidate, BankLGFormLiquidate
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5f13ea1f9acd48cc1e7dce794369e89901bdb582
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976313"
---
# <a name="letter-of-guarantee-transaction"></a><span data-ttu-id="e5a38-103">Garantipostering</span><span class="sxs-lookup"><span data-stu-id="e5a38-103">Letter of guarantee transaction</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e5a38-104">Denne procedure gennemgår garantiprocessen.</span><span class="sxs-lookup"><span data-stu-id="e5a38-104">This procedure walks through the Letter of guarantee process.</span></span>



<span data-ttu-id="e5a38-105">Følgende opgaver skal være fuldført, før du fuldfører denne procedure:</span><span class="sxs-lookup"><span data-stu-id="e5a38-105">The following tasks must be complete before completing this procedure:</span></span>

- <span data-ttu-id="e5a38-106">Konfigurere bankfaciliteter og posteringsprofiler for en garanti.</span><span class="sxs-lookup"><span data-stu-id="e5a38-106">Set up bank facilities and posting profiles for a letter of guarantee.</span></span>

- <span data-ttu-id="e5a38-107">Opret en bankfacilitetsaftale for en garanti.</span><span class="sxs-lookup"><span data-stu-id="e5a38-107">Create a bank facility agreement for a letter of guarantee.</span></span>



<span data-ttu-id="e5a38-108">Denne procedure bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="e5a38-108">This procedure uses the USMF demo company.</span></span>


## <a name="create-sales-order-with-letter-of-guarantee"></a><span data-ttu-id="e5a38-109">Oprette salgsordre med Garanti</span><span class="sxs-lookup"><span data-stu-id="e5a38-109">Create Sales Order with Letter of Guarantee</span></span>
1. <span data-ttu-id="e5a38-110">Gå til Debitor > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="e5a38-110">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="e5a38-111">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="e5a38-111">Click New.</span></span>
3. <span data-ttu-id="e5a38-112">Indtast eller vælg en værdi i feltet Kundekonto.</span><span class="sxs-lookup"><span data-stu-id="e5a38-112">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="e5a38-113">Udvid afsnittet Generelt.</span><span class="sxs-lookup"><span data-stu-id="e5a38-113">Expand the General section.</span></span>
5. <span data-ttu-id="e5a38-114">Indtast eller vælg en værdi i feltet Lokation.</span><span class="sxs-lookup"><span data-stu-id="e5a38-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="e5a38-115">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="e5a38-115">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="e5a38-116">Indtast eller vælg en værdi i feltet Lagersted.</span><span class="sxs-lookup"><span data-stu-id="e5a38-116">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="e5a38-117">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="e5a38-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="e5a38-118">Vælg Garanti i feltet Bankdokumenttype.</span><span class="sxs-lookup"><span data-stu-id="e5a38-118">In the Bank document type field, select 'Letter of guarantee'.</span></span>
10. <span data-ttu-id="e5a38-119">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="e5a38-119">Click OK.</span></span>
11. <span data-ttu-id="e5a38-120">Indtast eller vælg en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="e5a38-120">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="e5a38-121">Angiv et tal i feltet Enhedspris.</span><span class="sxs-lookup"><span data-stu-id="e5a38-121">In the Unit price field, enter a number.</span></span>
13. <span data-ttu-id="e5a38-122">Vis eller skjul sektionen Linjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="e5a38-122">Expand the Line details section.</span></span>
14. <span data-ttu-id="e5a38-123">Klik på fanen Levering.</span><span class="sxs-lookup"><span data-stu-id="e5a38-123">Click the Delivery tab.</span></span>
    * <span data-ttu-id="e5a38-124">Bemærk! Vælg leveringsdatokontrol = Ingen</span><span class="sxs-lookup"><span data-stu-id="e5a38-124">Note: Select Delivery date control = None</span></span>  
15. <span data-ttu-id="e5a38-125">Angiv en dato i feltet Ønsket afsendelsesdato.</span><span class="sxs-lookup"><span data-stu-id="e5a38-125">In the Requested ship date field, enter a date.</span></span>
16. <span data-ttu-id="e5a38-126">Angiv en dato i feltet Bekræftet afsendelsesdato.</span><span class="sxs-lookup"><span data-stu-id="e5a38-126">In the Confirmed ship date field, enter a date.</span></span>

## <a name="process-letter-of-guarantee_request"></a><span data-ttu-id="e5a38-127">Behandle garanti_Anmodning</span><span class="sxs-lookup"><span data-stu-id="e5a38-127">Process letter of guarantee_Request</span></span>
1. <span data-ttu-id="e5a38-128">Klik på Administrer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="e5a38-128">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="e5a38-129">Klik på Garanti.</span><span class="sxs-lookup"><span data-stu-id="e5a38-129">Click Letter of guarantee.</span></span>
3. <span data-ttu-id="e5a38-130">I handlingsruden skal du klikke på Garanti.</span><span class="sxs-lookup"><span data-stu-id="e5a38-130">On the Action Pane, click Letter of guarantee.</span></span>
4. <span data-ttu-id="e5a38-131">Klik på Anmodning for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="e5a38-131">Click Request to open the drop dialog.</span></span>
5. <span data-ttu-id="e5a38-132">Indtast eller vælg en værdi i feltet Type.</span><span class="sxs-lookup"><span data-stu-id="e5a38-132">In the Type field, enter or select a value.</span></span>
6. <span data-ttu-id="e5a38-133">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="e5a38-133">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="e5a38-134">Angiv et tal i feltet Værdi.</span><span class="sxs-lookup"><span data-stu-id="e5a38-134">In the Value field, enter a number.</span></span>
8. <span data-ttu-id="e5a38-135">Angiv dato og klokkeslæt i feltet Udløbsdato.</span><span class="sxs-lookup"><span data-stu-id="e5a38-135">In the Expiration date field, enter a date and time.</span></span>
9. <span data-ttu-id="e5a38-136">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="e5a38-136">Click OK.</span></span>
10. <span data-ttu-id="e5a38-137">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e5a38-137">Close the page.</span></span>

## <a name="process-letter-of-guarantee_submit-to-bank"></a><span data-ttu-id="e5a38-138">Behandle anmodning om garanti_Send til bank</span><span class="sxs-lookup"><span data-stu-id="e5a38-138">Process letter of guarantee_Submit to bank</span></span>
1. <span data-ttu-id="e5a38-139">Gå til Kontant- og bankstyring > Garantier > Garantier.</span><span class="sxs-lookup"><span data-stu-id="e5a38-139">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
2. <span data-ttu-id="e5a38-140">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="e5a38-140">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="e5a38-141">Klik på Send til bank for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="e5a38-141">Click Submit to bank to open the drop dialog.</span></span>
4. <span data-ttu-id="e5a38-142">Indtast eller vælg en værdi i feltet Bankkonto.</span><span class="sxs-lookup"><span data-stu-id="e5a38-142">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="e5a38-143">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="e5a38-143">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="e5a38-144">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="e5a38-144">Click OK.</span></span>

## <a name="process-letter-of-guarantee_receive-from-bank"></a><span data-ttu-id="e5a38-145">Behandle garanti_Modtag fra bank</span><span class="sxs-lookup"><span data-stu-id="e5a38-145">Process letter of guarantee_Receive from bank</span></span>
1. <span data-ttu-id="e5a38-146">Klik på Modtag fra bank for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="e5a38-146">Click Receive from bank to open the drop dialog.</span></span>
2. <span data-ttu-id="e5a38-147">Skriv en værdi i feltet Banknummer.</span><span class="sxs-lookup"><span data-stu-id="e5a38-147">In the Bank number field, type a value.</span></span>
    * <span data-ttu-id="e5a38-148">Kontrollér værdierne i de beregnede avance- og udgiftsfelter.</span><span class="sxs-lookup"><span data-stu-id="e5a38-148">Verify the values in the calculated Margin and Expense fields.</span></span>  
3. <span data-ttu-id="e5a38-149">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="e5a38-149">Click OK.</span></span>
4. <span data-ttu-id="e5a38-150">Udvid afsnittet Handlinger.</span><span class="sxs-lookup"><span data-stu-id="e5a38-150">Expand the Actions section.</span></span>
    * <span data-ttu-id="e5a38-151">Kontroller posten "Modtag fra bank".</span><span class="sxs-lookup"><span data-stu-id="e5a38-151">Verify the 'Receive from bank' record.</span></span>  
5. <span data-ttu-id="e5a38-152">Klik for at følge linket i feltet Kladdebatchnummer.</span><span class="sxs-lookup"><span data-stu-id="e5a38-152">Click to follow the link in the Journal batch number field.</span></span>
6. <span data-ttu-id="e5a38-153">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="e5a38-153">Click Lines.</span></span>
    * <span data-ttu-id="e5a38-154">Kontrollér bogføringen af kladdeposteringer.</span><span class="sxs-lookup"><span data-stu-id="e5a38-154">Verify the posting of journal entries.</span></span>  
7. <span data-ttu-id="e5a38-155">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e5a38-155">Close the page.</span></span>

## <a name="process-letter-of-guarantee_give-to-beneficiary"></a><span data-ttu-id="e5a38-156">Behandle garanti_Giv til modtager</span><span class="sxs-lookup"><span data-stu-id="e5a38-156">Process letter of guarantee_Give to beneficiary</span></span>
1. <span data-ttu-id="e5a38-157">Gå til Debitor > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="e5a38-157">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="e5a38-158">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="e5a38-158">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="e5a38-159">Klik på Administrer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="e5a38-159">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="e5a38-160">Klik på Garanti.</span><span class="sxs-lookup"><span data-stu-id="e5a38-160">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="e5a38-161">I handlingsruden skal du klikke på Garanti.</span><span class="sxs-lookup"><span data-stu-id="e5a38-161">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="e5a38-162">Klik på Giv til modtager for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="e5a38-162">Click Give to beneficiary to open the drop dialog.</span></span>
7. <span data-ttu-id="e5a38-163">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="e5a38-163">Click OK.</span></span>
8. <span data-ttu-id="e5a38-164">Gå til Kontant- og bankstyring > Garantier > Garantier.</span><span class="sxs-lookup"><span data-stu-id="e5a38-164">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="e5a38-165">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="e5a38-165">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="e5a38-166">Klik på Giv til modtager for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="e5a38-166">Click Give to beneficiary to open the drop dialog.</span></span>
11. <span data-ttu-id="e5a38-167">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="e5a38-167">Click OK.</span></span>
12. <span data-ttu-id="e5a38-168">Udvid afsnittet Handlinger.</span><span class="sxs-lookup"><span data-stu-id="e5a38-168">Expand the Actions section.</span></span>
    * <span data-ttu-id="e5a38-169">Valider 'Giv til beneficiant'-posten.</span><span class="sxs-lookup"><span data-stu-id="e5a38-169">Validate the 'Give to beneficiary' record.</span></span>  

## <a name="process-letter-of-guarantee_increase-value"></a><span data-ttu-id="e5a38-170">Behandle garanti_Opskriv værdi</span><span class="sxs-lookup"><span data-stu-id="e5a38-170">Process letter of guarantee_Increase value</span></span>
1. <span data-ttu-id="e5a38-171">Gå til Debitor > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="e5a38-171">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="e5a38-172">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="e5a38-172">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="e5a38-173">Klik på Administrer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="e5a38-173">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="e5a38-174">Klik på Garanti.</span><span class="sxs-lookup"><span data-stu-id="e5a38-174">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="e5a38-175">I handlingsruden skal du klikke på Garanti.</span><span class="sxs-lookup"><span data-stu-id="e5a38-175">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="e5a38-176">Klik på Opskriv værdi for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="e5a38-176">Click Increase value to open the drop dialog.</span></span>
7. <span data-ttu-id="e5a38-177">Indtast et tal i feltet Værdi, der skal tilføjes.</span><span class="sxs-lookup"><span data-stu-id="e5a38-177">In the Value to add field, enter a number.</span></span>
8. <span data-ttu-id="e5a38-178">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="e5a38-178">Click OK.</span></span>
9. <span data-ttu-id="e5a38-179">Gå til Kontant- og bankstyring > Garantier > Garantier.</span><span class="sxs-lookup"><span data-stu-id="e5a38-179">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
10. <span data-ttu-id="e5a38-180">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="e5a38-180">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="e5a38-181">Klik på Opskriv værdi for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="e5a38-181">Click Increase value to open the drop dialog.</span></span>
12. <span data-ttu-id="e5a38-182">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="e5a38-182">Click OK.</span></span>
13. <span data-ttu-id="e5a38-183">Udvid afsnittet Handlinger.</span><span class="sxs-lookup"><span data-stu-id="e5a38-183">Expand the Actions section.</span></span>
    * <span data-ttu-id="e5a38-184">Kontroller posten 'Opskriv værdi'.</span><span class="sxs-lookup"><span data-stu-id="e5a38-184">Verify the 'Increase value' record.</span></span>  
14. <span data-ttu-id="e5a38-185">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="e5a38-185">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="e5a38-186">Klik for at følge linket i feltet Kladdebatchnummer.</span><span class="sxs-lookup"><span data-stu-id="e5a38-186">Click to follow the link in the Journal batch number field.</span></span>
16. <span data-ttu-id="e5a38-187">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="e5a38-187">Click Lines.</span></span>
    * <span data-ttu-id="e5a38-188">Kontrollér de bogførte kladdeposteringer.</span><span class="sxs-lookup"><span data-stu-id="e5a38-188">Verify the posted journal entries.</span></span>  

## <a name="process-letter-of-guarantee_liquidate"></a><span data-ttu-id="e5a38-189">Behandle garanti_Udfør afvikling</span><span class="sxs-lookup"><span data-stu-id="e5a38-189">Process letter of guarantee_Liquidate</span></span>
1. <span data-ttu-id="e5a38-190">Gå til Debitor > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="e5a38-190">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="e5a38-191">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="e5a38-191">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="e5a38-192">Klik på Administrer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="e5a38-192">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="e5a38-193">Klik på Garanti.</span><span class="sxs-lookup"><span data-stu-id="e5a38-193">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="e5a38-194">I handlingsruden skal du klikke på Garanti.</span><span class="sxs-lookup"><span data-stu-id="e5a38-194">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="e5a38-195">Klik på Udfør afvikling for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="e5a38-195">Click Liquidate to open the drop dialog.</span></span>
7. <span data-ttu-id="e5a38-196">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="e5a38-196">Click OK.</span></span>
8. <span data-ttu-id="e5a38-197">Gå til Kontant- og bankstyring > Garantier > Garantier.</span><span class="sxs-lookup"><span data-stu-id="e5a38-197">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="e5a38-198">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="e5a38-198">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="e5a38-199">Klik på Udfør afvikling for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="e5a38-199">Click Liquidate to open the drop dialog.</span></span>
11. <span data-ttu-id="e5a38-200">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="e5a38-200">Click OK.</span></span>
12. <span data-ttu-id="e5a38-201">Udvid afsnittet Handlinger.</span><span class="sxs-lookup"><span data-stu-id="e5a38-201">Expand the Actions section.</span></span>
    * <span data-ttu-id="e5a38-202">Kontroller posten 'Udfør afvikling'.</span><span class="sxs-lookup"><span data-stu-id="e5a38-202">Verify the 'Liquidate' record.</span></span>  
13. <span data-ttu-id="e5a38-203">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="e5a38-203">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="e5a38-204">Klik for at følge linket i feltet Kladdebatchnummer.</span><span class="sxs-lookup"><span data-stu-id="e5a38-204">Click to follow the link in the Journal batch number field.</span></span>
15. <span data-ttu-id="e5a38-205">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="e5a38-205">Click Lines.</span></span>
    * <span data-ttu-id="e5a38-206">Kontrollér de bogførte kladdeposteringer.</span><span class="sxs-lookup"><span data-stu-id="e5a38-206">Verify the posted journal entries.</span></span>  
16. <span data-ttu-id="e5a38-207">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e5a38-207">Close the page.</span></span>

