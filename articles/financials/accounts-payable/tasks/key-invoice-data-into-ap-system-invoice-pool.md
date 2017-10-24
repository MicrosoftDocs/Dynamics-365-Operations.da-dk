--- 
title: "Indtaste fakturadata i kreditorsystemet ved hjælp af en fakturapulje"
description: Denne opgaveguide viser, hvordan du kan bruge indgangsbogen til at oprette fakturaer.
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 96040b1c1ba130f773ba0defbf7bf1dcebedfc13
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a><span data-ttu-id="1d50d-103">Indtaste fakturadata i kreditorsystemet ved hjælp af en fakturapulje</span><span class="sxs-lookup"><span data-stu-id="1d50d-103">Key invoice data into the AP system using invoice pool</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1d50d-104">Denne opgaveguide viser, hvordan du kan bruge indgangsbogen til at oprette fakturaer.</span><span class="sxs-lookup"><span data-stu-id="1d50d-104">This task guide will show you how to use the invoice register to create invoices.</span></span>  <span data-ttu-id="1d50d-105">Brug derefter fakturapuljen til at afstemme fakturaen med en indkøbsordre, og færdiggør udgiften på siden med kreditorfakturaer.</span><span class="sxs-lookup"><span data-stu-id="1d50d-105">Then use the invoice pool to match the invoice to a purchase order and finalize the expense in the vendor invoice page.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="1d50d-106">Oprette en indkøbsordre</span><span class="sxs-lookup"><span data-stu-id="1d50d-106">Create a purchase order</span></span>
1. <span data-ttu-id="1d50d-107">Gå til Kreditor > Indkøbsordrer > Indkøbsordrer.</span><span class="sxs-lookup"><span data-stu-id="1d50d-107">Go to Accounts payable > Purchase orders > Purchase orders.</span></span>
2. <span data-ttu-id="1d50d-108">Klik på Ny for at oprette en indkøbsordre.</span><span class="sxs-lookup"><span data-stu-id="1d50d-108">Click New to create a purchase order.</span></span>
3. <span data-ttu-id="1d50d-109">Klik på rullelisten i feltet Kreditorkonto for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="1d50d-109">In the Vendor account field, click the drop down button to open the lookup.</span></span>
4. <span data-ttu-id="1d50d-110">Vælg kreditoren på listen.</span><span class="sxs-lookup"><span data-stu-id="1d50d-110">Select the vendor from the list.</span></span> <span data-ttu-id="1d50d-111">For eksempel kreditor 1001.</span><span class="sxs-lookup"><span data-stu-id="1d50d-111">For example, vendor 1001.</span></span>
5. <span data-ttu-id="1d50d-112">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="1d50d-112">Click OK.</span></span>
6. <span data-ttu-id="1d50d-113">Klik på rullelisten i feltet Varenummer for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="1d50d-113">In the Item number field, click the drop down button to open the lookup.</span></span>
7. <span data-ttu-id="1d50d-114">Markér varenummeret for tjenester på listen.</span><span class="sxs-lookup"><span data-stu-id="1d50d-114">Find the services item number in the list.</span></span> <span data-ttu-id="1d50d-115">Vælg for eksempel S0001.</span><span class="sxs-lookup"><span data-stu-id="1d50d-115">For example, select S0001.</span></span>
8. <span data-ttu-id="1d50d-116">Klik på varenummeret, og vælg det.</span><span class="sxs-lookup"><span data-stu-id="1d50d-116">Click on the item number and select it.</span></span>
    * <span data-ttu-id="1d50d-117">Nettobeløbet er 75,00.</span><span class="sxs-lookup"><span data-stu-id="1d50d-117">The net amount is 75.00.</span></span>  <span data-ttu-id="1d50d-118">Det er det beløb, som vi forventer på fakturaen.</span><span class="sxs-lookup"><span data-stu-id="1d50d-118">That is the amount that we will expect on the invoice.</span></span>  
9. <span data-ttu-id="1d50d-119">Klik på Køb i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="1d50d-119">On the action pane, click Purchase.</span></span>
10. <span data-ttu-id="1d50d-120">Klik på Bekræft.</span><span class="sxs-lookup"><span data-stu-id="1d50d-120">Click Confirm.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="1d50d-121">Oprette og bogføre fakturaen</span><span class="sxs-lookup"><span data-stu-id="1d50d-121">Create and post and invoice</span></span>
1. <span data-ttu-id="1d50d-122">Gå til Kreditor > Fakturaer > Indgangsbog.</span><span class="sxs-lookup"><span data-stu-id="1d50d-122">Go to Accounts payable > Invoices > Invoice register.</span></span>
2. <span data-ttu-id="1d50d-123">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="1d50d-123">Click New.</span></span>
3. <span data-ttu-id="1d50d-124">Åbn opslaget for at vælge navnet på den indgangsbog, du vil bruge.</span><span class="sxs-lookup"><span data-stu-id="1d50d-124">Open the lookup to select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="1d50d-125">Vælg navnet på den indgangsbog, du vil bruge.</span><span class="sxs-lookup"><span data-stu-id="1d50d-125">Select the name of the invoice register that you want to use.</span></span>
5. <span data-ttu-id="1d50d-126">Klik på Linjer for at åbne bogen og angive udgiftslinjer.</span><span class="sxs-lookup"><span data-stu-id="1d50d-126">Click on Lines to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="1d50d-127">Vælg en kreditor i opslaget.</span><span class="sxs-lookup"><span data-stu-id="1d50d-127">In the lookup, select a vendor.</span></span> <span data-ttu-id="1d50d-128">Klik for eksempel på kreditor 1001.</span><span class="sxs-lookup"><span data-stu-id="1d50d-128">For example, click on vendor 1001.</span></span>
7. <span data-ttu-id="1d50d-129">Angiv fakturanummeret i feltet Faktura.</span><span class="sxs-lookup"><span data-stu-id="1d50d-129">In the Invoice field, enter the invoice number.</span></span>
8. <span data-ttu-id="1d50d-130">Indtast en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="1d50d-130">In the Description field, type a value.</span></span>
9. <span data-ttu-id="1d50d-131">Angiv et tal i feltet Kredit.</span><span class="sxs-lookup"><span data-stu-id="1d50d-131">In the Credit field, enter a number.</span></span>
10. <span data-ttu-id="1d50d-132">Klik på rullelisten i feltet Indkøbsordre for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="1d50d-132">In the Purchase order field, click the drop down button to open the lookup.</span></span>
11. <span data-ttu-id="1d50d-133">Vælg den indkøbsordre, du oprettede tidligere.</span><span class="sxs-lookup"><span data-stu-id="1d50d-133">Select the purchase order that you created earlier.</span></span>
12. <span data-ttu-id="1d50d-134">Klik på rullelisten i feltet Godkendt af for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="1d50d-134">In the Approved by field, click the drop down button to open the lookup.</span></span>
13. <span data-ttu-id="1d50d-135">Fremhæv en godkender, og klik på Vælg for at vælge den pågældende godkender.</span><span class="sxs-lookup"><span data-stu-id="1d50d-135">Highlight an approver and click Select to select that approver.</span></span>
14. <span data-ttu-id="1d50d-136">Klik på Bogfør.</span><span class="sxs-lookup"><span data-stu-id="1d50d-136">Click Post.</span></span>
15. <span data-ttu-id="1d50d-137">Luk formularen.</span><span class="sxs-lookup"><span data-stu-id="1d50d-137">Close the form.</span></span>
16. <span data-ttu-id="1d50d-138">Luk formularen.</span><span class="sxs-lookup"><span data-stu-id="1d50d-138">Close the form.</span></span>

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a><span data-ttu-id="1d50d-139">Åbne en faktura fra puljen og tilpasse den til en indkøbsordre for at fuldføre fakturaprocessen</span><span class="sxs-lookup"><span data-stu-id="1d50d-139">Open an invoice from the pool and match it to a purchase order to complete the invoice process</span></span>
1. <span data-ttu-id="1d50d-140">Gå til Kreditor > Fakturaer > Fakturapulje.</span><span class="sxs-lookup"><span data-stu-id="1d50d-140">Go to Accounts payable > Invoices > Invoice pool.</span></span>
2. <span data-ttu-id="1d50d-141">Klik på Indkøbsordre for at oprette en kreditorfaktura ud fra fakturaen i puljen.</span><span class="sxs-lookup"><span data-stu-id="1d50d-141">Click Purchase order to create a vendor invoice from the invoice in the pool.</span></span>
3. <span data-ttu-id="1d50d-142">Vælg den faktura, du vil gennemse.</span><span class="sxs-lookup"><span data-stu-id="1d50d-142">Select the invoice that you want to review.</span></span>
4. <span data-ttu-id="1d50d-143">Klik på Opdater status for sammenholdelse for at fuldføre sammenholdelsen.</span><span class="sxs-lookup"><span data-stu-id="1d50d-143">Click Update match status to complete the matching.</span></span>
5. <span data-ttu-id="1d50d-144">Klik på Indstillinger i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="1d50d-144">On the action pane, click Options.</span></span>
6. <span data-ttu-id="1d50d-145">Klik på Skift visning.</span><span class="sxs-lookup"><span data-stu-id="1d50d-145">Click Change view.</span></span>
7. <span data-ttu-id="1d50d-146">Klik på Gittervisning.</span><span class="sxs-lookup"><span data-stu-id="1d50d-146">Click Grid view.</span></span>
8. <span data-ttu-id="1d50d-147">Klik på Bogfør.</span><span class="sxs-lookup"><span data-stu-id="1d50d-147">Click Post.</span></span>
9. <span data-ttu-id="1d50d-148">Luk formularen.</span><span class="sxs-lookup"><span data-stu-id="1d50d-148">Close the form.</span></span>
10. <span data-ttu-id="1d50d-149">Gå til Kreditor > Kreditorer > Kreditorer.</span><span class="sxs-lookup"><span data-stu-id="1d50d-149">Go to Accounts payable > Vendors > Vendors.</span></span>
11. <span data-ttu-id="1d50d-150">Vælg den kreditor, der stod i indkøbsordren.</span><span class="sxs-lookup"><span data-stu-id="1d50d-150">Select the vendor that was on the purchase order.</span></span> <span data-ttu-id="1d50d-151">Vælg for eksempel kreditor 1001.</span><span class="sxs-lookup"><span data-stu-id="1d50d-151">For example, select vendor 1001.</span></span>
12. <span data-ttu-id="1d50d-152">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="1d50d-152">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="1d50d-153">Klik på Kreditor i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="1d50d-153">On the action pane, click Vendor.</span></span>
14. <span data-ttu-id="1d50d-154">Klik på Transaktioner.</span><span class="sxs-lookup"><span data-stu-id="1d50d-154">Click Transactions.</span></span>
15. <span data-ttu-id="1d50d-155">Vælg den faktura, du oprettede.</span><span class="sxs-lookup"><span data-stu-id="1d50d-155">Select the invoice that you created.</span></span>
    * <span data-ttu-id="1d50d-156">Periodiseringen af indgangsbogen blev tilbageført og bogført på den relevante udgiftskonto.</span><span class="sxs-lookup"><span data-stu-id="1d50d-156">The invoice register accrual was reversed and posted to the appropriate expense account.</span></span>  


