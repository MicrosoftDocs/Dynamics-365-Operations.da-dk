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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 05abad6898c2b97cf66abdff21b30407dacd6488
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141781"
---
# <a name="letter-of-guarantee-transaction"></a><span data-ttu-id="4e1fe-103">Garantipostering</span><span class="sxs-lookup"><span data-stu-id="4e1fe-103">Letter of guarantee transaction</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4e1fe-104">Denne procedure gennemgår garantiprocessen.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-104">This procedure walks through the Letter of guarantee process.</span></span>



<span data-ttu-id="4e1fe-105">Følgende opgaver skal være fuldført, før du fuldfører denne procedure:</span><span class="sxs-lookup"><span data-stu-id="4e1fe-105">The following tasks must be complete before completing this procedure:</span></span>

- <span data-ttu-id="4e1fe-106">Konfigurere bankfaciliteter og posteringsprofiler for en garanti.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-106">Set up bank facilities and posting profiles for a letter of guarantee.</span></span>

- <span data-ttu-id="4e1fe-107">Opret en bankfacilitetsaftale for en garanti.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-107">Create a bank facility agreement for a letter of guarantee.</span></span>



<span data-ttu-id="4e1fe-108">Denne procedure bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-108">This procedure uses the USMF demo company.</span></span>


## <a name="create-sales-order-with-letter-of-guarantee"></a><span data-ttu-id="4e1fe-109">Oprette salgsordre med Garanti</span><span class="sxs-lookup"><span data-stu-id="4e1fe-109">Create Sales Order with Letter of Guarantee</span></span>
1. <span data-ttu-id="4e1fe-110">Gå til Debitor > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-110">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="4e1fe-111">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-111">Click New.</span></span>
3. <span data-ttu-id="4e1fe-112">Indtast eller vælg en værdi i feltet Kundekonto.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-112">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="4e1fe-113">Udvid afsnittet Generelt.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-113">Expand the General section.</span></span>
5. <span data-ttu-id="4e1fe-114">Indtast eller vælg en værdi i feltet Lokation.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="4e1fe-115">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-115">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="4e1fe-116">Indtast eller vælg en værdi i feltet Lagersted.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-116">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="4e1fe-117">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="4e1fe-118">Vælg Garanti i feltet Bankdokumenttype.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-118">In the Bank document type field, select 'Letter of guarantee'.</span></span>
10. <span data-ttu-id="4e1fe-119">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-119">Click OK.</span></span>
11. <span data-ttu-id="4e1fe-120">Indtast eller vælg en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-120">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="4e1fe-121">Angiv et tal i feltet Enhedspris.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-121">In the Unit price field, enter a number.</span></span>
13. <span data-ttu-id="4e1fe-122">Vis eller skjul sektionen Linjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-122">Expand the Line details section.</span></span>
14. <span data-ttu-id="4e1fe-123">Klik på fanen Levering.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-123">Click the Delivery tab.</span></span>
    * <span data-ttu-id="4e1fe-124">Bemærk! Vælg leveringsdatokontrol = Ingen</span><span class="sxs-lookup"><span data-stu-id="4e1fe-124">Note: Select Delivery date control = None</span></span>  
15. <span data-ttu-id="4e1fe-125">Angiv en dato i feltet Ønsket afsendelsesdato.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-125">In the Requested ship date field, enter a date.</span></span>
16. <span data-ttu-id="4e1fe-126">Angiv en dato i feltet Bekræftet afsendelsesdato.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-126">In the Confirmed ship date field, enter a date.</span></span>

## <a name="process-letter-of-guarantee_request"></a><span data-ttu-id="4e1fe-127">Behandle garanti_Anmodning</span><span class="sxs-lookup"><span data-stu-id="4e1fe-127">Process letter of guarantee_Request</span></span>
1. <span data-ttu-id="4e1fe-128">Klik på Administrer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-128">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="4e1fe-129">Klik på Garanti.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-129">Click Letter of guarantee.</span></span>
3. <span data-ttu-id="4e1fe-130">I handlingsruden skal du klikke på Garanti.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-130">On the Action Pane, click Letter of guarantee.</span></span>
4. <span data-ttu-id="4e1fe-131">Klik på Anmodning for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-131">Click Request to open the drop dialog.</span></span>
5. <span data-ttu-id="4e1fe-132">Indtast eller vælg en værdi i feltet Type.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-132">In the Type field, enter or select a value.</span></span>
6. <span data-ttu-id="4e1fe-133">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-133">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="4e1fe-134">Angiv et tal i feltet Værdi.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-134">In the Value field, enter a number.</span></span>
8. <span data-ttu-id="4e1fe-135">Angiv dato og klokkeslæt i feltet Udløbsdato.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-135">In the Expiration date field, enter a date and time.</span></span>
9. <span data-ttu-id="4e1fe-136">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-136">Click OK.</span></span>
10. <span data-ttu-id="4e1fe-137">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-137">Close the page.</span></span>

## <a name="process-letter-of-guarantee_submit-to-bank"></a><span data-ttu-id="4e1fe-138">Behandle anmodning om garanti_Send til bank</span><span class="sxs-lookup"><span data-stu-id="4e1fe-138">Process letter of guarantee_Submit to bank</span></span>
1. <span data-ttu-id="4e1fe-139">Gå til Kontant- og bankstyring > Garantier > Garantier.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-139">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
2. <span data-ttu-id="4e1fe-140">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-140">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="4e1fe-141">Klik på Send til bank for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-141">Click Submit to bank to open the drop dialog.</span></span>
4. <span data-ttu-id="4e1fe-142">Indtast eller vælg en værdi i feltet Bankkonto.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-142">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="4e1fe-143">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-143">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="4e1fe-144">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-144">Click OK.</span></span>

## <a name="process-letter-of-guarantee_receive-from-bank"></a><span data-ttu-id="4e1fe-145">Behandle garanti_Modtag fra bank</span><span class="sxs-lookup"><span data-stu-id="4e1fe-145">Process letter of guarantee_Receive from bank</span></span>
1. <span data-ttu-id="4e1fe-146">Klik på Modtag fra bank for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-146">Click Receive from bank to open the drop dialog.</span></span>
2. <span data-ttu-id="4e1fe-147">Skriv en værdi i feltet Banknummer.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-147">In the Bank number field, type a value.</span></span>
    * <span data-ttu-id="4e1fe-148">Kontrollér værdierne i de beregnede avance- og udgiftsfelter.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-148">Verify the values in the calculated Margin and Expense fields.</span></span>  
3. <span data-ttu-id="4e1fe-149">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-149">Click OK.</span></span>
4. <span data-ttu-id="4e1fe-150">Udvid afsnittet Handlinger.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-150">Expand the Actions section.</span></span>
    * <span data-ttu-id="4e1fe-151">Kontroller posten "Modtag fra bank".</span><span class="sxs-lookup"><span data-stu-id="4e1fe-151">Verify the 'Receive from bank' record.</span></span>  
5. <span data-ttu-id="4e1fe-152">Klik for at følge linket i feltet Kladdebatchnummer.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-152">Click to follow the link in the Journal batch number field.</span></span>
6. <span data-ttu-id="4e1fe-153">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-153">Click Lines.</span></span>
    * <span data-ttu-id="4e1fe-154">Kontrollér bogføringen af kladdeposteringer.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-154">Verify the posting of journal entries.</span></span>  
7. <span data-ttu-id="4e1fe-155">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-155">Close the page.</span></span>

## <a name="process-letter-of-guarantee_give-to-beneficiary"></a><span data-ttu-id="4e1fe-156">Behandle garanti_Giv til modtager</span><span class="sxs-lookup"><span data-stu-id="4e1fe-156">Process letter of guarantee_Give to beneficiary</span></span>
1. <span data-ttu-id="4e1fe-157">Gå til Debitor > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-157">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="4e1fe-158">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-158">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="4e1fe-159">Klik på Administrer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-159">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="4e1fe-160">Klik på Garanti.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-160">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="4e1fe-161">I handlingsruden skal du klikke på Garanti.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-161">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="4e1fe-162">Klik på Giv til modtager for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-162">Click Give to beneficiary to open the drop dialog.</span></span>
7. <span data-ttu-id="4e1fe-163">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-163">Click OK.</span></span>
8. <span data-ttu-id="4e1fe-164">Gå til Kontant- og bankstyring > Garantier > Garantier.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-164">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="4e1fe-165">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-165">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="4e1fe-166">Klik på Giv til modtager for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-166">Click Give to beneficiary to open the drop dialog.</span></span>
11. <span data-ttu-id="4e1fe-167">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-167">Click OK.</span></span>
12. <span data-ttu-id="4e1fe-168">Udvid afsnittet Handlinger.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-168">Expand the Actions section.</span></span>
    * <span data-ttu-id="4e1fe-169">Valider 'Giv til beneficiant'-posten.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-169">Validate the 'Give to beneficiary' record.</span></span>  

## <a name="process-letter-of-guarantee_increase-value"></a><span data-ttu-id="4e1fe-170">Behandle garanti_Opskriv værdi</span><span class="sxs-lookup"><span data-stu-id="4e1fe-170">Process letter of guarantee_Increase value</span></span>
1. <span data-ttu-id="4e1fe-171">Gå til Debitor > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-171">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="4e1fe-172">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-172">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="4e1fe-173">Klik på Administrer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-173">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="4e1fe-174">Klik på Garanti.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-174">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="4e1fe-175">I handlingsruden skal du klikke på Garanti.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-175">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="4e1fe-176">Klik på Opskriv værdi for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-176">Click Increase value to open the drop dialog.</span></span>
7. <span data-ttu-id="4e1fe-177">Indtast et tal i feltet Værdi, der skal tilføjes.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-177">In the Value to add field, enter a number.</span></span>
8. <span data-ttu-id="4e1fe-178">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-178">Click OK.</span></span>
9. <span data-ttu-id="4e1fe-179">Gå til Kontant- og bankstyring > Garantier > Garantier.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-179">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
10. <span data-ttu-id="4e1fe-180">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-180">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="4e1fe-181">Klik på Opskriv værdi for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-181">Click Increase value to open the drop dialog.</span></span>
12. <span data-ttu-id="4e1fe-182">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-182">Click OK.</span></span>
13. <span data-ttu-id="4e1fe-183">Udvid afsnittet Handlinger.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-183">Expand the Actions section.</span></span>
    * <span data-ttu-id="4e1fe-184">Kontroller posten 'Opskriv værdi'.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-184">Verify the 'Increase value' record.</span></span>  
14. <span data-ttu-id="4e1fe-185">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-185">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="4e1fe-186">Klik for at følge linket i feltet Kladdebatchnummer.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-186">Click to follow the link in the Journal batch number field.</span></span>
16. <span data-ttu-id="4e1fe-187">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-187">Click Lines.</span></span>
    * <span data-ttu-id="4e1fe-188">Kontrollér de bogførte kladdeposteringer.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-188">Verify the posted journal entries.</span></span>  

## <a name="process-letter-of-guarantee_liquidate"></a><span data-ttu-id="4e1fe-189">Behandle garanti_Udfør afvikling</span><span class="sxs-lookup"><span data-stu-id="4e1fe-189">Process letter of guarantee_Liquidate</span></span>
1. <span data-ttu-id="4e1fe-190">Gå til Debitor > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-190">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="4e1fe-191">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-191">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="4e1fe-192">Klik på Administrer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-192">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="4e1fe-193">Klik på Garanti.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-193">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="4e1fe-194">I handlingsruden skal du klikke på Garanti.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-194">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="4e1fe-195">Klik på Udfør afvikling for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-195">Click Liquidate to open the drop dialog.</span></span>
7. <span data-ttu-id="4e1fe-196">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-196">Click OK.</span></span>
8. <span data-ttu-id="4e1fe-197">Gå til Kontant- og bankstyring > Garantier > Garantier.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-197">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="4e1fe-198">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-198">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="4e1fe-199">Klik på Udfør afvikling for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-199">Click Liquidate to open the drop dialog.</span></span>
11. <span data-ttu-id="4e1fe-200">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-200">Click OK.</span></span>
12. <span data-ttu-id="4e1fe-201">Udvid afsnittet Handlinger.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-201">Expand the Actions section.</span></span>
    * <span data-ttu-id="4e1fe-202">Kontroller posten 'Udfør afvikling'.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-202">Verify the 'Liquidate' record.</span></span>  
13. <span data-ttu-id="4e1fe-203">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-203">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="4e1fe-204">Klik for at følge linket i feltet Kladdebatchnummer.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-204">Click to follow the link in the Journal batch number field.</span></span>
15. <span data-ttu-id="4e1fe-205">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-205">Click Lines.</span></span>
    * <span data-ttu-id="4e1fe-206">Kontrollér de bogførte kladdeposteringer.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-206">Verify the posted journal entries.</span></span>  
16. <span data-ttu-id="4e1fe-207">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="4e1fe-207">Close the page.</span></span>

