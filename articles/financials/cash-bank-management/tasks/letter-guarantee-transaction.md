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
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4dc6ee178121fae05d538f5103919442d91e65eb
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566104"
---
# <a name="letter-of-guarantee-transaction"></a><span data-ttu-id="ba0fd-103">Garantipostering</span><span class="sxs-lookup"><span data-stu-id="ba0fd-103">Letter of guarantee transaction</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ba0fd-104">Denne procedure gennemgår garantiprocessen.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-104">This procedure walks through the Letter of guarantee process.</span></span>



<span data-ttu-id="ba0fd-105">Følgende opgaver skal være fuldført, før du fuldfører denne procedure:</span><span class="sxs-lookup"><span data-stu-id="ba0fd-105">The following tasks must be complete before completing this procedure:</span></span>

- <span data-ttu-id="ba0fd-106">Konfigurere bankfaciliteter og posteringsprofiler for en garanti.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-106">Set up bank facilities and posting profiles for a letter of guarantee.</span></span>

- <span data-ttu-id="ba0fd-107">Opret en bankfacilitetsaftale for en garanti.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-107">Create a bank facility agreement for a letter of guarantee.</span></span>



<span data-ttu-id="ba0fd-108">Denne procedure bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-108">This procedure uses the USMF demo company.</span></span>


## <a name="create-sales-order-with-letter-of-guarantee"></a><span data-ttu-id="ba0fd-109">Oprette salgsordre med Garanti</span><span class="sxs-lookup"><span data-stu-id="ba0fd-109">Create Sales Order with Letter of Guarantee</span></span>
1. <span data-ttu-id="ba0fd-110">Gå til Debitor > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-110">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="ba0fd-111">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-111">Click New.</span></span>
3. <span data-ttu-id="ba0fd-112">Indtast eller vælg en værdi i feltet Kundekonto.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-112">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="ba0fd-113">Udvid afsnittet Generelt.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-113">Expand the General section.</span></span>
5. <span data-ttu-id="ba0fd-114">Indtast eller vælg en værdi i feltet Lokation.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="ba0fd-115">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-115">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="ba0fd-116">Indtast eller vælg en værdi i feltet Lagersted.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-116">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="ba0fd-117">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="ba0fd-118">Vælg Garanti i feltet Bankdokumenttype.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-118">In the Bank document type field, select 'Letter of guarantee'.</span></span>
10. <span data-ttu-id="ba0fd-119">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-119">Click OK.</span></span>
11. <span data-ttu-id="ba0fd-120">Indtast eller vælg en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-120">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="ba0fd-121">Angiv et tal i feltet Enhedspris.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-121">In the Unit price field, enter a number.</span></span>
13. <span data-ttu-id="ba0fd-122">Vis eller skjul sektionen Linjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-122">Expand the Line details section.</span></span>
14. <span data-ttu-id="ba0fd-123">Klik på fanen Levering.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-123">Click the Delivery tab.</span></span>
    * <span data-ttu-id="ba0fd-124">Bemærk! Vælg leveringsdatokontrol = Ingen</span><span class="sxs-lookup"><span data-stu-id="ba0fd-124">Note: Select Delivery date control = None</span></span>  
15. <span data-ttu-id="ba0fd-125">Angiv en dato i feltet Ønsket afsendelsesdato.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-125">In the Requested ship date field, enter a date.</span></span>
16. <span data-ttu-id="ba0fd-126">Angiv en dato i feltet Bekræftet afsendelsesdato.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-126">In the Confirmed ship date field, enter a date.</span></span>

## <a name="process-letter-of-guaranteerequest"></a><span data-ttu-id="ba0fd-127">Behandle garanti_Anmodning</span><span class="sxs-lookup"><span data-stu-id="ba0fd-127">Process letter of guarantee_Request</span></span>
1. <span data-ttu-id="ba0fd-128">Klik på Administrer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-128">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="ba0fd-129">Klik på Garanti.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-129">Click Letter of guarantee.</span></span>
3. <span data-ttu-id="ba0fd-130">I handlingsruden skal du klikke på Garanti.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-130">On the Action Pane, click Letter of guarantee.</span></span>
4. <span data-ttu-id="ba0fd-131">Klik på Anmodning for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-131">Click Request to open the drop dialog.</span></span>
5. <span data-ttu-id="ba0fd-132">Indtast eller vælg en værdi i feltet Type.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-132">In the Type field, enter or select a value.</span></span>
6. <span data-ttu-id="ba0fd-133">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-133">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="ba0fd-134">Angiv et tal i feltet Værdi.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-134">In the Value field, enter a number.</span></span>
8. <span data-ttu-id="ba0fd-135">Angiv dato og klokkeslæt i feltet Udløbsdato.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-135">In the Expiration date field, enter a date and time.</span></span>
9. <span data-ttu-id="ba0fd-136">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-136">Click OK.</span></span>
10. <span data-ttu-id="ba0fd-137">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-137">Close the page.</span></span>

## <a name="process-letter-of-guaranteesubmit-to-bank"></a><span data-ttu-id="ba0fd-138">Behandle anmodning om garanti_Send til bank</span><span class="sxs-lookup"><span data-stu-id="ba0fd-138">Process letter of guarantee_Submit to bank</span></span>
1. <span data-ttu-id="ba0fd-139">Gå til Kontant- og bankstyring > Garantier > Garantier.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-139">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
2. <span data-ttu-id="ba0fd-140">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-140">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="ba0fd-141">Klik på Send til bank for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-141">Click Submit to bank to open the drop dialog.</span></span>
4. <span data-ttu-id="ba0fd-142">Indtast eller vælg en værdi i feltet Bankkonto.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-142">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="ba0fd-143">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-143">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="ba0fd-144">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-144">Click OK.</span></span>

## <a name="process-letter-of-guaranteereceive-from-bank"></a><span data-ttu-id="ba0fd-145">Behandle garanti_Modtag fra bank</span><span class="sxs-lookup"><span data-stu-id="ba0fd-145">Process letter of guarantee_Receive from bank</span></span>
1. <span data-ttu-id="ba0fd-146">Klik på Modtag fra bank for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-146">Click Receive from bank to open the drop dialog.</span></span>
2. <span data-ttu-id="ba0fd-147">Skriv en værdi i feltet Banknummer.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-147">In the Bank number field, type a value.</span></span>
    * <span data-ttu-id="ba0fd-148">Kontrollér værdierne i de beregnede avance- og udgiftsfelter.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-148">Verify the values in the calculated Margin and Expense fields.</span></span>  
3. <span data-ttu-id="ba0fd-149">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-149">Click OK.</span></span>
4. <span data-ttu-id="ba0fd-150">Udvid afsnittet Handlinger.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-150">Expand the Actions section.</span></span>
    * <span data-ttu-id="ba0fd-151">Kontroller posten "Modtag fra bank".</span><span class="sxs-lookup"><span data-stu-id="ba0fd-151">Verify the 'Receive from bank' record.</span></span>  
5. <span data-ttu-id="ba0fd-152">Klik for at følge linket i feltet Kladdebatchnummer.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-152">Click to follow the link in the Journal batch number field.</span></span>
6. <span data-ttu-id="ba0fd-153">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-153">Click Lines.</span></span>
    * <span data-ttu-id="ba0fd-154">Kontrollér bogføringen af kladdeposteringer.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-154">Verify the posting of journal entries.</span></span>  
7. <span data-ttu-id="ba0fd-155">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-155">Close the page.</span></span>

## <a name="process-letter-of-guaranteegive-to-beneficiary"></a><span data-ttu-id="ba0fd-156">Behandle garanti_Giv til modtager</span><span class="sxs-lookup"><span data-stu-id="ba0fd-156">Process letter of guarantee_Give to beneficiary</span></span>
1. <span data-ttu-id="ba0fd-157">Gå til Debitor > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-157">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="ba0fd-158">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-158">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="ba0fd-159">Klik på Administrer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-159">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="ba0fd-160">Klik på Garanti.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-160">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="ba0fd-161">I handlingsruden skal du klikke på Garanti.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-161">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="ba0fd-162">Klik på Giv til modtager for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-162">Click Give to beneficiary to open the drop dialog.</span></span>
7. <span data-ttu-id="ba0fd-163">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-163">Click OK.</span></span>
8. <span data-ttu-id="ba0fd-164">Gå til Kontant- og bankstyring > Garantier > Garantier.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-164">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="ba0fd-165">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-165">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="ba0fd-166">Klik på Giv til modtager for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-166">Click Give to beneficiary to open the drop dialog.</span></span>
11. <span data-ttu-id="ba0fd-167">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-167">Click OK.</span></span>
12. <span data-ttu-id="ba0fd-168">Udvid afsnittet Handlinger.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-168">Expand the Actions section.</span></span>
    * <span data-ttu-id="ba0fd-169">Valider 'Giv til beneficiant'-posten.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-169">Validate the 'Give to beneficiary' record.</span></span>  

## <a name="process-letter-of-guaranteeincrease-value"></a><span data-ttu-id="ba0fd-170">Behandle garanti_Opskriv værdi</span><span class="sxs-lookup"><span data-stu-id="ba0fd-170">Process letter of guarantee_Increase value</span></span>
1. <span data-ttu-id="ba0fd-171">Gå til Debitor > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-171">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="ba0fd-172">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-172">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="ba0fd-173">Klik på Administrer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-173">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="ba0fd-174">Klik på Garanti.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-174">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="ba0fd-175">I handlingsruden skal du klikke på Garanti.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-175">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="ba0fd-176">Klik på Opskriv værdi for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-176">Click Increase value to open the drop dialog.</span></span>
7. <span data-ttu-id="ba0fd-177">Indtast et tal i feltet Værdi, der skal tilføjes.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-177">In the Value to add field, enter a number.</span></span>
8. <span data-ttu-id="ba0fd-178">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-178">Click OK.</span></span>
9. <span data-ttu-id="ba0fd-179">Gå til Kontant- og bankstyring > Garantier > Garantier.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-179">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
10. <span data-ttu-id="ba0fd-180">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-180">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="ba0fd-181">Klik på Opskriv værdi for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-181">Click Increase value to open the drop dialog.</span></span>
12. <span data-ttu-id="ba0fd-182">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-182">Click OK.</span></span>
13. <span data-ttu-id="ba0fd-183">Udvid afsnittet Handlinger.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-183">Expand the Actions section.</span></span>
    * <span data-ttu-id="ba0fd-184">Kontroller posten 'Opskriv værdi'.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-184">Verify the 'Increase value' record.</span></span>  
14. <span data-ttu-id="ba0fd-185">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-185">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="ba0fd-186">Klik for at følge linket i feltet Kladdebatchnummer.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-186">Click to follow the link in the Journal batch number field.</span></span>
16. <span data-ttu-id="ba0fd-187">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-187">Click Lines.</span></span>
    * <span data-ttu-id="ba0fd-188">Kontrollér de bogførte kladdeposteringer.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-188">Verify the posted journal entries.</span></span>  

## <a name="process-letter-of-guaranteeliquidate"></a><span data-ttu-id="ba0fd-189">Behandle garanti_Udfør afvikling</span><span class="sxs-lookup"><span data-stu-id="ba0fd-189">Process letter of guarantee_Liquidate</span></span>
1. <span data-ttu-id="ba0fd-190">Gå til Debitor > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-190">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="ba0fd-191">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-191">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="ba0fd-192">Klik på Administrer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-192">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="ba0fd-193">Klik på Garanti.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-193">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="ba0fd-194">I handlingsruden skal du klikke på Garanti.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-194">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="ba0fd-195">Klik på Udfør afvikling for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-195">Click Liquidate to open the drop dialog.</span></span>
7. <span data-ttu-id="ba0fd-196">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-196">Click OK.</span></span>
8. <span data-ttu-id="ba0fd-197">Gå til Kontant- og bankstyring > Garantier > Garantier.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-197">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="ba0fd-198">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-198">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="ba0fd-199">Klik på Udfør afvikling for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-199">Click Liquidate to open the drop dialog.</span></span>
11. <span data-ttu-id="ba0fd-200">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-200">Click OK.</span></span>
12. <span data-ttu-id="ba0fd-201">Udvid afsnittet Handlinger.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-201">Expand the Actions section.</span></span>
    * <span data-ttu-id="ba0fd-202">Kontroller posten 'Udfør afvikling'.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-202">Verify the 'Liquidate' record.</span></span>  
13. <span data-ttu-id="ba0fd-203">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-203">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="ba0fd-204">Klik for at følge linket i feltet Kladdebatchnummer.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-204">Click to follow the link in the Journal batch number field.</span></span>
15. <span data-ttu-id="ba0fd-205">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-205">Click Lines.</span></span>
    * <span data-ttu-id="ba0fd-206">Kontrollér de bogførte kladdeposteringer.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-206">Verify the posted journal entries.</span></span>  
16. <span data-ttu-id="ba0fd-207">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-207">Close the page.</span></span>

