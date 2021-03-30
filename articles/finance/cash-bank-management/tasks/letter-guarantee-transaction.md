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
ms.openlocfilehash: 566849cfcedd29f4bb92d08a17b67e16b1cbc372
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225363"
---
# <a name="letter-of-guarantee-transaction"></a><span data-ttu-id="44516-103">Garantipostering</span><span class="sxs-lookup"><span data-stu-id="44516-103">Letter of guarantee transaction</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="44516-104">Denne procedure gennemgår garantiprocessen.</span><span class="sxs-lookup"><span data-stu-id="44516-104">This procedure walks through the Letter of guarantee process.</span></span>



<span data-ttu-id="44516-105">Følgende opgaver skal være fuldført, før du fuldfører denne procedure:</span><span class="sxs-lookup"><span data-stu-id="44516-105">The following tasks must be complete before completing this procedure:</span></span>

- <span data-ttu-id="44516-106">Konfigurere bankfaciliteter og posteringsprofiler for en garanti.</span><span class="sxs-lookup"><span data-stu-id="44516-106">Set up bank facilities and posting profiles for a letter of guarantee.</span></span>

- <span data-ttu-id="44516-107">Opret en bankfacilitetsaftale for en garanti.</span><span class="sxs-lookup"><span data-stu-id="44516-107">Create a bank facility agreement for a letter of guarantee.</span></span>



<span data-ttu-id="44516-108">Denne procedure bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="44516-108">This procedure uses the USMF demo company.</span></span>


## <a name="create-sales-order-with-letter-of-guarantee"></a><span data-ttu-id="44516-109">Oprette salgsordre med Garanti</span><span class="sxs-lookup"><span data-stu-id="44516-109">Create Sales Order with Letter of Guarantee</span></span>
1. <span data-ttu-id="44516-110">Gå til Debitor > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="44516-110">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="44516-111">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="44516-111">Click New.</span></span>
3. <span data-ttu-id="44516-112">Indtast eller vælg en værdi i feltet Kundekonto.</span><span class="sxs-lookup"><span data-stu-id="44516-112">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="44516-113">Udvid afsnittet Generelt.</span><span class="sxs-lookup"><span data-stu-id="44516-113">Expand the General section.</span></span>
5. <span data-ttu-id="44516-114">Indtast eller vælg en værdi i feltet Lokation.</span><span class="sxs-lookup"><span data-stu-id="44516-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="44516-115">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="44516-115">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="44516-116">Indtast eller vælg en værdi i feltet Lagersted.</span><span class="sxs-lookup"><span data-stu-id="44516-116">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="44516-117">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="44516-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="44516-118">Vælg Garanti i feltet Bankdokumenttype.</span><span class="sxs-lookup"><span data-stu-id="44516-118">In the Bank document type field, select 'Letter of guarantee'.</span></span>
10. <span data-ttu-id="44516-119">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="44516-119">Click OK.</span></span>
11. <span data-ttu-id="44516-120">Indtast eller vælg en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="44516-120">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="44516-121">Angiv et tal i feltet Enhedspris.</span><span class="sxs-lookup"><span data-stu-id="44516-121">In the Unit price field, enter a number.</span></span>
13. <span data-ttu-id="44516-122">Vis eller skjul sektionen Linjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="44516-122">Expand the Line details section.</span></span>
14. <span data-ttu-id="44516-123">Klik på fanen Levering.</span><span class="sxs-lookup"><span data-stu-id="44516-123">Click the Delivery tab.</span></span>
    * <span data-ttu-id="44516-124">Bemærk! Vælg leveringsdatokontrol = Ingen</span><span class="sxs-lookup"><span data-stu-id="44516-124">Note: Select Delivery date control = None</span></span>  
15. <span data-ttu-id="44516-125">Angiv en dato i feltet Ønsket afsendelsesdato.</span><span class="sxs-lookup"><span data-stu-id="44516-125">In the Requested ship date field, enter a date.</span></span>
16. <span data-ttu-id="44516-126">Angiv en dato i feltet Bekræftet afsendelsesdato.</span><span class="sxs-lookup"><span data-stu-id="44516-126">In the Confirmed ship date field, enter a date.</span></span>

## <a name="process-letter-of-guarantee_request"></a><span data-ttu-id="44516-127">Behandle garanti_Anmodning</span><span class="sxs-lookup"><span data-stu-id="44516-127">Process letter of guarantee_Request</span></span>
1. <span data-ttu-id="44516-128">Klik på Administrer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="44516-128">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="44516-129">Klik på Garanti.</span><span class="sxs-lookup"><span data-stu-id="44516-129">Click Letter of guarantee.</span></span>
3. <span data-ttu-id="44516-130">I handlingsruden skal du klikke på Garanti.</span><span class="sxs-lookup"><span data-stu-id="44516-130">On the Action Pane, click Letter of guarantee.</span></span>
4. <span data-ttu-id="44516-131">Klik på Anmodning for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="44516-131">Click Request to open the drop dialog.</span></span>
5. <span data-ttu-id="44516-132">Indtast eller vælg en værdi i feltet Type.</span><span class="sxs-lookup"><span data-stu-id="44516-132">In the Type field, enter or select a value.</span></span>
6. <span data-ttu-id="44516-133">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="44516-133">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="44516-134">Angiv et tal i feltet Værdi.</span><span class="sxs-lookup"><span data-stu-id="44516-134">In the Value field, enter a number.</span></span>
8. <span data-ttu-id="44516-135">Angiv dato og klokkeslæt i feltet Udløbsdato.</span><span class="sxs-lookup"><span data-stu-id="44516-135">In the Expiration date field, enter a date and time.</span></span>
9. <span data-ttu-id="44516-136">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="44516-136">Click OK.</span></span>
10. <span data-ttu-id="44516-137">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="44516-137">Close the page.</span></span>

## <a name="process-letter-of-guarantee_submit-to-bank"></a><span data-ttu-id="44516-138">Behandle anmodning om garanti_Send til bank</span><span class="sxs-lookup"><span data-stu-id="44516-138">Process letter of guarantee_Submit to bank</span></span>
1. <span data-ttu-id="44516-139">Gå til Kontant- og bankstyring > Garantier > Garantier.</span><span class="sxs-lookup"><span data-stu-id="44516-139">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
2. <span data-ttu-id="44516-140">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="44516-140">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="44516-141">Klik på Send til bank for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="44516-141">Click Submit to bank to open the drop dialog.</span></span>
4. <span data-ttu-id="44516-142">Indtast eller vælg en værdi i feltet Bankkonto.</span><span class="sxs-lookup"><span data-stu-id="44516-142">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="44516-143">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="44516-143">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="44516-144">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="44516-144">Click OK.</span></span>

## <a name="process-letter-of-guarantee_receive-from-bank"></a><span data-ttu-id="44516-145">Behandle garanti_Modtag fra bank</span><span class="sxs-lookup"><span data-stu-id="44516-145">Process letter of guarantee_Receive from bank</span></span>
1. <span data-ttu-id="44516-146">Klik på Modtag fra bank for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="44516-146">Click Receive from bank to open the drop dialog.</span></span>
2. <span data-ttu-id="44516-147">Skriv en værdi i feltet Banknummer.</span><span class="sxs-lookup"><span data-stu-id="44516-147">In the Bank number field, type a value.</span></span>
    * <span data-ttu-id="44516-148">Kontrollér værdierne i de beregnede avance- og udgiftsfelter.</span><span class="sxs-lookup"><span data-stu-id="44516-148">Verify the values in the calculated Margin and Expense fields.</span></span>  
3. <span data-ttu-id="44516-149">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="44516-149">Click OK.</span></span>
4. <span data-ttu-id="44516-150">Udvid afsnittet Handlinger.</span><span class="sxs-lookup"><span data-stu-id="44516-150">Expand the Actions section.</span></span>
    * <span data-ttu-id="44516-151">Kontroller posten "Modtag fra bank".</span><span class="sxs-lookup"><span data-stu-id="44516-151">Verify the 'Receive from bank' record.</span></span>  
5. <span data-ttu-id="44516-152">Klik for at følge linket i feltet Kladdebatchnummer.</span><span class="sxs-lookup"><span data-stu-id="44516-152">Click to follow the link in the Journal batch number field.</span></span>
6. <span data-ttu-id="44516-153">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="44516-153">Click Lines.</span></span>
    * <span data-ttu-id="44516-154">Kontrollér bogføringen af kladdeposteringer.</span><span class="sxs-lookup"><span data-stu-id="44516-154">Verify the posting of journal entries.</span></span>  
7. <span data-ttu-id="44516-155">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="44516-155">Close the page.</span></span>

## <a name="process-letter-of-guarantee_give-to-beneficiary"></a><span data-ttu-id="44516-156">Behandle garanti_Giv til modtager</span><span class="sxs-lookup"><span data-stu-id="44516-156">Process letter of guarantee_Give to beneficiary</span></span>
1. <span data-ttu-id="44516-157">Gå til Debitor > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="44516-157">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="44516-158">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="44516-158">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="44516-159">Klik på Administrer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="44516-159">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="44516-160">Klik på Garanti.</span><span class="sxs-lookup"><span data-stu-id="44516-160">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="44516-161">I handlingsruden skal du klikke på Garanti.</span><span class="sxs-lookup"><span data-stu-id="44516-161">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="44516-162">Klik på Giv til modtager for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="44516-162">Click Give to beneficiary to open the drop dialog.</span></span>
7. <span data-ttu-id="44516-163">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="44516-163">Click OK.</span></span>
8. <span data-ttu-id="44516-164">Gå til Kontant- og bankstyring > Garantier > Garantier.</span><span class="sxs-lookup"><span data-stu-id="44516-164">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="44516-165">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="44516-165">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="44516-166">Klik på Giv til modtager for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="44516-166">Click Give to beneficiary to open the drop dialog.</span></span>
11. <span data-ttu-id="44516-167">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="44516-167">Click OK.</span></span>
12. <span data-ttu-id="44516-168">Udvid afsnittet Handlinger.</span><span class="sxs-lookup"><span data-stu-id="44516-168">Expand the Actions section.</span></span>
    * <span data-ttu-id="44516-169">Valider 'Giv til beneficiant'-posten.</span><span class="sxs-lookup"><span data-stu-id="44516-169">Validate the 'Give to beneficiary' record.</span></span>  

## <a name="process-letter-of-guarantee_increase-value"></a><span data-ttu-id="44516-170">Behandle garanti_Opskriv værdi</span><span class="sxs-lookup"><span data-stu-id="44516-170">Process letter of guarantee_Increase value</span></span>
1. <span data-ttu-id="44516-171">Gå til Debitor > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="44516-171">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="44516-172">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="44516-172">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="44516-173">Klik på Administrer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="44516-173">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="44516-174">Klik på Garanti.</span><span class="sxs-lookup"><span data-stu-id="44516-174">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="44516-175">I handlingsruden skal du klikke på Garanti.</span><span class="sxs-lookup"><span data-stu-id="44516-175">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="44516-176">Klik på Opskriv værdi for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="44516-176">Click Increase value to open the drop dialog.</span></span>
7. <span data-ttu-id="44516-177">Indtast et tal i feltet Værdi, der skal tilføjes.</span><span class="sxs-lookup"><span data-stu-id="44516-177">In the Value to add field, enter a number.</span></span>
8. <span data-ttu-id="44516-178">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="44516-178">Click OK.</span></span>
9. <span data-ttu-id="44516-179">Gå til Kontant- og bankstyring > Garantier > Garantier.</span><span class="sxs-lookup"><span data-stu-id="44516-179">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
10. <span data-ttu-id="44516-180">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="44516-180">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="44516-181">Klik på Opskriv værdi for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="44516-181">Click Increase value to open the drop dialog.</span></span>
12. <span data-ttu-id="44516-182">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="44516-182">Click OK.</span></span>
13. <span data-ttu-id="44516-183">Udvid afsnittet Handlinger.</span><span class="sxs-lookup"><span data-stu-id="44516-183">Expand the Actions section.</span></span>
    * <span data-ttu-id="44516-184">Kontroller posten 'Opskriv værdi'.</span><span class="sxs-lookup"><span data-stu-id="44516-184">Verify the 'Increase value' record.</span></span>  
14. <span data-ttu-id="44516-185">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="44516-185">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="44516-186">Klik for at følge linket i feltet Kladdebatchnummer.</span><span class="sxs-lookup"><span data-stu-id="44516-186">Click to follow the link in the Journal batch number field.</span></span>
16. <span data-ttu-id="44516-187">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="44516-187">Click Lines.</span></span>
    * <span data-ttu-id="44516-188">Kontrollér de bogførte kladdeposteringer.</span><span class="sxs-lookup"><span data-stu-id="44516-188">Verify the posted journal entries.</span></span>  

## <a name="process-letter-of-guarantee_liquidate"></a><span data-ttu-id="44516-189">Behandle garanti_Udfør afvikling</span><span class="sxs-lookup"><span data-stu-id="44516-189">Process letter of guarantee_Liquidate</span></span>
1. <span data-ttu-id="44516-190">Gå til Debitor > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="44516-190">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="44516-191">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="44516-191">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="44516-192">Klik på Administrer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="44516-192">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="44516-193">Klik på Garanti.</span><span class="sxs-lookup"><span data-stu-id="44516-193">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="44516-194">I handlingsruden skal du klikke på Garanti.</span><span class="sxs-lookup"><span data-stu-id="44516-194">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="44516-195">Klik på Udfør afvikling for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="44516-195">Click Liquidate to open the drop dialog.</span></span>
7. <span data-ttu-id="44516-196">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="44516-196">Click OK.</span></span>
8. <span data-ttu-id="44516-197">Gå til Kontant- og bankstyring > Garantier > Garantier.</span><span class="sxs-lookup"><span data-stu-id="44516-197">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="44516-198">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="44516-198">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="44516-199">Klik på Udfør afvikling for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="44516-199">Click Liquidate to open the drop dialog.</span></span>
11. <span data-ttu-id="44516-200">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="44516-200">Click OK.</span></span>
12. <span data-ttu-id="44516-201">Udvid afsnittet Handlinger.</span><span class="sxs-lookup"><span data-stu-id="44516-201">Expand the Actions section.</span></span>
    * <span data-ttu-id="44516-202">Kontroller posten 'Udfør afvikling'.</span><span class="sxs-lookup"><span data-stu-id="44516-202">Verify the 'Liquidate' record.</span></span>  
13. <span data-ttu-id="44516-203">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="44516-203">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="44516-204">Klik for at følge linket i feltet Kladdebatchnummer.</span><span class="sxs-lookup"><span data-stu-id="44516-204">Click to follow the link in the Journal batch number field.</span></span>
15. <span data-ttu-id="44516-205">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="44516-205">Click Lines.</span></span>
    * <span data-ttu-id="44516-206">Kontrollér de bogførte kladdeposteringer.</span><span class="sxs-lookup"><span data-stu-id="44516-206">Verify the posted journal entries.</span></span>  
16. <span data-ttu-id="44516-207">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="44516-207">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]