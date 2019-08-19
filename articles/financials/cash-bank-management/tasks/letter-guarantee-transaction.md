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
ms.openlocfilehash: ff105bdefff2ea93c853d590c77391653f50a4dc
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841987"
---
# <a name="letter-of-guarantee-transaction"></a><span data-ttu-id="f3669-103">Garantipostering</span><span class="sxs-lookup"><span data-stu-id="f3669-103">Letter of guarantee transaction</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f3669-104">Denne procedure gennemgår garantiprocessen.</span><span class="sxs-lookup"><span data-stu-id="f3669-104">This procedure walks through the Letter of guarantee process.</span></span>



<span data-ttu-id="f3669-105">Følgende opgaver skal være fuldført, før du fuldfører denne procedure:</span><span class="sxs-lookup"><span data-stu-id="f3669-105">The following tasks must be complete before completing this procedure:</span></span>

- <span data-ttu-id="f3669-106">Konfigurere bankfaciliteter og posteringsprofiler for en garanti.</span><span class="sxs-lookup"><span data-stu-id="f3669-106">Set up bank facilities and posting profiles for a letter of guarantee.</span></span>

- <span data-ttu-id="f3669-107">Opret en bankfacilitetsaftale for en garanti.</span><span class="sxs-lookup"><span data-stu-id="f3669-107">Create a bank facility agreement for a letter of guarantee.</span></span>



<span data-ttu-id="f3669-108">Denne procedure bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="f3669-108">This procedure uses the USMF demo company.</span></span>


## <a name="create-sales-order-with-letter-of-guarantee"></a><span data-ttu-id="f3669-109">Oprette salgsordre med Garanti</span><span class="sxs-lookup"><span data-stu-id="f3669-109">Create Sales Order with Letter of Guarantee</span></span>
1. <span data-ttu-id="f3669-110">Gå til Debitor > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="f3669-110">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="f3669-111">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="f3669-111">Click New.</span></span>
3. <span data-ttu-id="f3669-112">Indtast eller vælg en værdi i feltet Kundekonto.</span><span class="sxs-lookup"><span data-stu-id="f3669-112">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="f3669-113">Udvid afsnittet Generelt.</span><span class="sxs-lookup"><span data-stu-id="f3669-113">Expand the General section.</span></span>
5. <span data-ttu-id="f3669-114">Indtast eller vælg en værdi i feltet Lokation.</span><span class="sxs-lookup"><span data-stu-id="f3669-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="f3669-115">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="f3669-115">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="f3669-116">Indtast eller vælg en værdi i feltet Lagersted.</span><span class="sxs-lookup"><span data-stu-id="f3669-116">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="f3669-117">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="f3669-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="f3669-118">Vælg Garanti i feltet Bankdokumenttype.</span><span class="sxs-lookup"><span data-stu-id="f3669-118">In the Bank document type field, select 'Letter of guarantee'.</span></span>
10. <span data-ttu-id="f3669-119">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="f3669-119">Click OK.</span></span>
11. <span data-ttu-id="f3669-120">Indtast eller vælg en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="f3669-120">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="f3669-121">Angiv et tal i feltet Enhedspris.</span><span class="sxs-lookup"><span data-stu-id="f3669-121">In the Unit price field, enter a number.</span></span>
13. <span data-ttu-id="f3669-122">Vis eller skjul sektionen Linjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="f3669-122">Expand the Line details section.</span></span>
14. <span data-ttu-id="f3669-123">Klik på fanen Levering.</span><span class="sxs-lookup"><span data-stu-id="f3669-123">Click the Delivery tab.</span></span>
    * <span data-ttu-id="f3669-124">Bemærk! Vælg leveringsdatokontrol = Ingen</span><span class="sxs-lookup"><span data-stu-id="f3669-124">Note: Select Delivery date control = None</span></span>  
15. <span data-ttu-id="f3669-125">Angiv en dato i feltet Ønsket afsendelsesdato.</span><span class="sxs-lookup"><span data-stu-id="f3669-125">In the Requested ship date field, enter a date.</span></span>
16. <span data-ttu-id="f3669-126">Angiv en dato i feltet Bekræftet afsendelsesdato.</span><span class="sxs-lookup"><span data-stu-id="f3669-126">In the Confirmed ship date field, enter a date.</span></span>

## <a name="process-letter-of-guarantee_request"></a><span data-ttu-id="f3669-127">Behandle garanti_Anmodning</span><span class="sxs-lookup"><span data-stu-id="f3669-127">Process letter of guarantee_Request</span></span>
1. <span data-ttu-id="f3669-128">Klik på Administrer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="f3669-128">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="f3669-129">Klik på Garanti.</span><span class="sxs-lookup"><span data-stu-id="f3669-129">Click Letter of guarantee.</span></span>
3. <span data-ttu-id="f3669-130">I handlingsruden skal du klikke på Garanti.</span><span class="sxs-lookup"><span data-stu-id="f3669-130">On the Action Pane, click Letter of guarantee.</span></span>
4. <span data-ttu-id="f3669-131">Klik på Anmodning for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="f3669-131">Click Request to open the drop dialog.</span></span>
5. <span data-ttu-id="f3669-132">Indtast eller vælg en værdi i feltet Type.</span><span class="sxs-lookup"><span data-stu-id="f3669-132">In the Type field, enter or select a value.</span></span>
6. <span data-ttu-id="f3669-133">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="f3669-133">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="f3669-134">Angiv et tal i feltet Værdi.</span><span class="sxs-lookup"><span data-stu-id="f3669-134">In the Value field, enter a number.</span></span>
8. <span data-ttu-id="f3669-135">Angiv dato og klokkeslæt i feltet Udløbsdato.</span><span class="sxs-lookup"><span data-stu-id="f3669-135">In the Expiration date field, enter a date and time.</span></span>
9. <span data-ttu-id="f3669-136">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="f3669-136">Click OK.</span></span>
10. <span data-ttu-id="f3669-137">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="f3669-137">Close the page.</span></span>

## <a name="process-letter-of-guarantee_submit-to-bank"></a><span data-ttu-id="f3669-138">Behandle anmodning om garanti_Send til bank</span><span class="sxs-lookup"><span data-stu-id="f3669-138">Process letter of guarantee_Submit to bank</span></span>
1. <span data-ttu-id="f3669-139">Gå til Kontant- og bankstyring > Garantier > Garantier.</span><span class="sxs-lookup"><span data-stu-id="f3669-139">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
2. <span data-ttu-id="f3669-140">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="f3669-140">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="f3669-141">Klik på Send til bank for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="f3669-141">Click Submit to bank to open the drop dialog.</span></span>
4. <span data-ttu-id="f3669-142">Indtast eller vælg en værdi i feltet Bankkonto.</span><span class="sxs-lookup"><span data-stu-id="f3669-142">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="f3669-143">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="f3669-143">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="f3669-144">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="f3669-144">Click OK.</span></span>

## <a name="process-letter-of-guarantee_receive-from-bank"></a><span data-ttu-id="f3669-145">Behandle garanti_Modtag fra bank</span><span class="sxs-lookup"><span data-stu-id="f3669-145">Process letter of guarantee_Receive from bank</span></span>
1. <span data-ttu-id="f3669-146">Klik på Modtag fra bank for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="f3669-146">Click Receive from bank to open the drop dialog.</span></span>
2. <span data-ttu-id="f3669-147">Skriv en værdi i feltet Banknummer.</span><span class="sxs-lookup"><span data-stu-id="f3669-147">In the Bank number field, type a value.</span></span>
    * <span data-ttu-id="f3669-148">Kontrollér værdierne i de beregnede avance- og udgiftsfelter.</span><span class="sxs-lookup"><span data-stu-id="f3669-148">Verify the values in the calculated Margin and Expense fields.</span></span>  
3. <span data-ttu-id="f3669-149">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="f3669-149">Click OK.</span></span>
4. <span data-ttu-id="f3669-150">Udvid afsnittet Handlinger.</span><span class="sxs-lookup"><span data-stu-id="f3669-150">Expand the Actions section.</span></span>
    * <span data-ttu-id="f3669-151">Kontroller posten "Modtag fra bank".</span><span class="sxs-lookup"><span data-stu-id="f3669-151">Verify the 'Receive from bank' record.</span></span>  
5. <span data-ttu-id="f3669-152">Klik for at følge linket i feltet Kladdebatchnummer.</span><span class="sxs-lookup"><span data-stu-id="f3669-152">Click to follow the link in the Journal batch number field.</span></span>
6. <span data-ttu-id="f3669-153">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="f3669-153">Click Lines.</span></span>
    * <span data-ttu-id="f3669-154">Kontrollér bogføringen af kladdeposteringer.</span><span class="sxs-lookup"><span data-stu-id="f3669-154">Verify the posting of journal entries.</span></span>  
7. <span data-ttu-id="f3669-155">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="f3669-155">Close the page.</span></span>

## <a name="process-letter-of-guarantee_give-to-beneficiary"></a><span data-ttu-id="f3669-156">Behandle garanti_Giv til modtager</span><span class="sxs-lookup"><span data-stu-id="f3669-156">Process letter of guarantee_Give to beneficiary</span></span>
1. <span data-ttu-id="f3669-157">Gå til Debitor > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="f3669-157">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="f3669-158">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="f3669-158">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="f3669-159">Klik på Administrer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="f3669-159">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="f3669-160">Klik på Garanti.</span><span class="sxs-lookup"><span data-stu-id="f3669-160">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="f3669-161">I handlingsruden skal du klikke på Garanti.</span><span class="sxs-lookup"><span data-stu-id="f3669-161">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="f3669-162">Klik på Giv til modtager for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="f3669-162">Click Give to beneficiary to open the drop dialog.</span></span>
7. <span data-ttu-id="f3669-163">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="f3669-163">Click OK.</span></span>
8. <span data-ttu-id="f3669-164">Gå til Kontant- og bankstyring > Garantier > Garantier.</span><span class="sxs-lookup"><span data-stu-id="f3669-164">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="f3669-165">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="f3669-165">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="f3669-166">Klik på Giv til modtager for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="f3669-166">Click Give to beneficiary to open the drop dialog.</span></span>
11. <span data-ttu-id="f3669-167">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="f3669-167">Click OK.</span></span>
12. <span data-ttu-id="f3669-168">Udvid afsnittet Handlinger.</span><span class="sxs-lookup"><span data-stu-id="f3669-168">Expand the Actions section.</span></span>
    * <span data-ttu-id="f3669-169">Valider 'Giv til beneficiant'-posten.</span><span class="sxs-lookup"><span data-stu-id="f3669-169">Validate the 'Give to beneficiary' record.</span></span>  

## <a name="process-letter-of-guarantee_increase-value"></a><span data-ttu-id="f3669-170">Behandle garanti_Opskriv værdi</span><span class="sxs-lookup"><span data-stu-id="f3669-170">Process letter of guarantee_Increase value</span></span>
1. <span data-ttu-id="f3669-171">Gå til Debitor > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="f3669-171">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="f3669-172">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="f3669-172">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="f3669-173">Klik på Administrer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="f3669-173">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="f3669-174">Klik på Garanti.</span><span class="sxs-lookup"><span data-stu-id="f3669-174">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="f3669-175">I handlingsruden skal du klikke på Garanti.</span><span class="sxs-lookup"><span data-stu-id="f3669-175">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="f3669-176">Klik på Opskriv værdi for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="f3669-176">Click Increase value to open the drop dialog.</span></span>
7. <span data-ttu-id="f3669-177">Indtast et tal i feltet Værdi, der skal tilføjes.</span><span class="sxs-lookup"><span data-stu-id="f3669-177">In the Value to add field, enter a number.</span></span>
8. <span data-ttu-id="f3669-178">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="f3669-178">Click OK.</span></span>
9. <span data-ttu-id="f3669-179">Gå til Kontant- og bankstyring > Garantier > Garantier.</span><span class="sxs-lookup"><span data-stu-id="f3669-179">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
10. <span data-ttu-id="f3669-180">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="f3669-180">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="f3669-181">Klik på Opskriv værdi for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="f3669-181">Click Increase value to open the drop dialog.</span></span>
12. <span data-ttu-id="f3669-182">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="f3669-182">Click OK.</span></span>
13. <span data-ttu-id="f3669-183">Udvid afsnittet Handlinger.</span><span class="sxs-lookup"><span data-stu-id="f3669-183">Expand the Actions section.</span></span>
    * <span data-ttu-id="f3669-184">Kontroller posten 'Opskriv værdi'.</span><span class="sxs-lookup"><span data-stu-id="f3669-184">Verify the 'Increase value' record.</span></span>  
14. <span data-ttu-id="f3669-185">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="f3669-185">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="f3669-186">Klik for at følge linket i feltet Kladdebatchnummer.</span><span class="sxs-lookup"><span data-stu-id="f3669-186">Click to follow the link in the Journal batch number field.</span></span>
16. <span data-ttu-id="f3669-187">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="f3669-187">Click Lines.</span></span>
    * <span data-ttu-id="f3669-188">Kontrollér de bogførte kladdeposteringer.</span><span class="sxs-lookup"><span data-stu-id="f3669-188">Verify the posted journal entries.</span></span>  

## <a name="process-letter-of-guarantee_liquidate"></a><span data-ttu-id="f3669-189">Behandle garanti_Udfør afvikling</span><span class="sxs-lookup"><span data-stu-id="f3669-189">Process letter of guarantee_Liquidate</span></span>
1. <span data-ttu-id="f3669-190">Gå til Debitor > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="f3669-190">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="f3669-191">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="f3669-191">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="f3669-192">Klik på Administrer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="f3669-192">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="f3669-193">Klik på Garanti.</span><span class="sxs-lookup"><span data-stu-id="f3669-193">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="f3669-194">I handlingsruden skal du klikke på Garanti.</span><span class="sxs-lookup"><span data-stu-id="f3669-194">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="f3669-195">Klik på Udfør afvikling for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="f3669-195">Click Liquidate to open the drop dialog.</span></span>
7. <span data-ttu-id="f3669-196">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="f3669-196">Click OK.</span></span>
8. <span data-ttu-id="f3669-197">Gå til Kontant- og bankstyring > Garantier > Garantier.</span><span class="sxs-lookup"><span data-stu-id="f3669-197">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="f3669-198">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="f3669-198">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="f3669-199">Klik på Udfør afvikling for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="f3669-199">Click Liquidate to open the drop dialog.</span></span>
11. <span data-ttu-id="f3669-200">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="f3669-200">Click OK.</span></span>
12. <span data-ttu-id="f3669-201">Udvid afsnittet Handlinger.</span><span class="sxs-lookup"><span data-stu-id="f3669-201">Expand the Actions section.</span></span>
    * <span data-ttu-id="f3669-202">Kontroller posten 'Udfør afvikling'.</span><span class="sxs-lookup"><span data-stu-id="f3669-202">Verify the 'Liquidate' record.</span></span>  
13. <span data-ttu-id="f3669-203">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="f3669-203">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="f3669-204">Klik for at følge linket i feltet Kladdebatchnummer.</span><span class="sxs-lookup"><span data-stu-id="f3669-204">Click to follow the link in the Journal batch number field.</span></span>
15. <span data-ttu-id="f3669-205">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="f3669-205">Click Lines.</span></span>
    * <span data-ttu-id="f3669-206">Kontrollér de bogførte kladdeposteringer.</span><span class="sxs-lookup"><span data-stu-id="f3669-206">Verify the posted journal entries.</span></span>  
16. <span data-ttu-id="f3669-207">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="f3669-207">Close the page.</span></span>

