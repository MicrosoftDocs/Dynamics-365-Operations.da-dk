--- 
title: Vigtigste fakturadata i kreditorsystem, der bruger kreditorfaktura
description: "Denne opgaveguide hjælper dig med at oprette en kreditorfaktura fra en indkøbsordre og få vist resultaterne af sammenholdelse af indkøbsordre, tilgang og faktura (trevejs-sammenholdelse)."
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines, VendEditInvoice, InventItemIdLookupSimple, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: e1d2e31a5de7cefd20996c18bf4771296a587997
ms.contentlocale: da-dk
ms.lasthandoff: 09/14/2018

---
# <a name="key-invoice-data-in-ap-system-using-vendor-invoice"></a><span data-ttu-id="e82f6-103">Vigtigste fakturadata i kreditorsystem, der bruger kreditorfaktura</span><span class="sxs-lookup"><span data-stu-id="e82f6-103">Key invoice data in AP system using vendor invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e82f6-104">Denne opgaveguide hjælper dig med at oprette en kreditorfaktura fra en indkøbsordre og få vist resultaterne af sammenholdelse af indkøbsordre, tilgang og faktura (trevejs-sammenholdelse).</span><span class="sxs-lookup"><span data-stu-id="e82f6-104">This task guide will help you create a vendor invoice from a purchase order and view the results of matching the purchase order, receipt, and invoice (3 way matching).</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="e82f6-105">Oprette en indkøbsordre</span><span class="sxs-lookup"><span data-stu-id="e82f6-105">Create a purchase order</span></span>
1. <span data-ttu-id="e82f6-106">Gå til Kreditor > Indkøbsordrer > Alle indkøbsordrer.</span><span class="sxs-lookup"><span data-stu-id="e82f6-106">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="e82f6-107">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="e82f6-107">Click New.</span></span>
3. <span data-ttu-id="e82f6-108">Klik på rullelisten i feltet Kreditorkonto for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="e82f6-108">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="e82f6-109">Find en kreditor, du vil vælge.</span><span class="sxs-lookup"><span data-stu-id="e82f6-109">Find a vendor to select.</span></span> <span data-ttu-id="e82f6-110">Rul for eksempel ned til US-104.</span><span class="sxs-lookup"><span data-stu-id="e82f6-110">For example, scroll down to US-104.</span></span>
5. <span data-ttu-id="e82f6-111">Vælg kreditor US-104.</span><span class="sxs-lookup"><span data-stu-id="e82f6-111">Select vendor US-104.</span></span>
6. <span data-ttu-id="e82f6-112">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="e82f6-112">Click OK.</span></span>
7. <span data-ttu-id="e82f6-113">Klik på rullelisten i feltet Varenummer for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="e82f6-113">In the Item number field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="e82f6-114">Vælg en lagervare.</span><span class="sxs-lookup"><span data-stu-id="e82f6-114">Select an inventory item.</span></span> <span data-ttu-id="e82f6-115">Du kan for eksempel vælge varenummer 1000.</span><span class="sxs-lookup"><span data-stu-id="e82f6-115">For example, select item number 1000.</span></span>
9. <span data-ttu-id="e82f6-116">Udvis eller skjul sektionen Linedetaljer.</span><span class="sxs-lookup"><span data-stu-id="e82f6-116">Expand or collapse the Line details section.</span></span>
10. <span data-ttu-id="e82f6-117">Klik på fanen Opsætning.</span><span class="sxs-lookup"><span data-stu-id="e82f6-117">Click the Setup tab.</span></span>
    * <span data-ttu-id="e82f6-118">Du kan tilsidesætte sammenholdelsespolitikken for at undlade at bruge sammenholdelse, tovejs-sammenholdelse eller trevejs-sammenholdelse .</span><span class="sxs-lookup"><span data-stu-id="e82f6-118">You can override the matching policy to use no matching, 2-way matching, or 3-way matching.</span></span>  
11. <span data-ttu-id="e82f6-119">Udvis eller skjul sektionen Linedetaljer.</span><span class="sxs-lookup"><span data-stu-id="e82f6-119">Expand or collapse the Line details section.</span></span>
12. <span data-ttu-id="e82f6-120">Klik på Køb i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="e82f6-120">On the Action Pane, click Purchase.</span></span>
13. <span data-ttu-id="e82f6-121">Klik på Bekræft.</span><span class="sxs-lookup"><span data-stu-id="e82f6-121">Click Confirm.</span></span>

## <a name="receive-the-products"></a><span data-ttu-id="e82f6-122">Modtage produkterne</span><span class="sxs-lookup"><span data-stu-id="e82f6-122">Receive the products</span></span>
1. <span data-ttu-id="e82f6-123">Klik på Modtag i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="e82f6-123">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="e82f6-124">Klik på Produktkvittering.</span><span class="sxs-lookup"><span data-stu-id="e82f6-124">Click Product receipt.</span></span>
3. <span data-ttu-id="e82f6-125">Angiv nummeret på produktkvitteringen i feltet Produktkvittering.</span><span class="sxs-lookup"><span data-stu-id="e82f6-125">In the Product receipt field, enter the product receipt number.</span></span> <span data-ttu-id="e82f6-126">Angiv for eksempel PR123.</span><span class="sxs-lookup"><span data-stu-id="e82f6-126">For example, enter PR123.</span></span>
4. <span data-ttu-id="e82f6-127">Klik på OK for at bogføre produktkvitteringen.</span><span class="sxs-lookup"><span data-stu-id="e82f6-127">Click OK to post the product receipt.</span></span>
5. <span data-ttu-id="e82f6-128">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e82f6-128">Close the page.</span></span>

## <a name="create-a-vendor-invoice"></a><span data-ttu-id="e82f6-129">Oprette en kreditorfaktura</span><span class="sxs-lookup"><span data-stu-id="e82f6-129">Create a vendor invoice</span></span>
1. <span data-ttu-id="e82f6-130">Gå til Debitor > Indkøbsordrer > Indkøbsordrer, der er modtaget, men ikke faktureret.</span><span class="sxs-lookup"><span data-stu-id="e82f6-130">Go to Accounts payable > Purchase orders > Purchase orders received but not invoiced.</span></span>
2. <span data-ttu-id="e82f6-131">Vælg den indkøbsordrelinje, du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="e82f6-131">Select the purchase order that you created.</span></span>
3. <span data-ttu-id="e82f6-132">Klik på Faktura i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="e82f6-132">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="e82f6-133">Klik på Faktura.</span><span class="sxs-lookup"><span data-stu-id="e82f6-133">Click Invoice.</span></span>
5. <span data-ttu-id="e82f6-134">Angiv fakturanummeret i feltet Nummer.</span><span class="sxs-lookup"><span data-stu-id="e82f6-134">In the Number field, enter the invoice number.</span></span>
6. <span data-ttu-id="e82f6-135">Skriv en værdi i feltet Fakturabeskrivelse.</span><span class="sxs-lookup"><span data-stu-id="e82f6-135">In the Invoice description field, type a value.</span></span>
7. <span data-ttu-id="e82f6-136">Indtast en dato i feltet Fakturadato.</span><span class="sxs-lookup"><span data-stu-id="e82f6-136">In the Invoice date field, enter a date.</span></span>
8. <span data-ttu-id="e82f6-137">Angiv 1200 i feltet Enhedspris.</span><span class="sxs-lookup"><span data-stu-id="e82f6-137">In the Unit price field, enter 1200.</span></span>
9. <span data-ttu-id="e82f6-138">Klik på Tilføj linje.</span><span class="sxs-lookup"><span data-stu-id="e82f6-138">Click Add line.</span></span>
10. <span data-ttu-id="e82f6-139">Klik på rullelisten i feltet Varenummer for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="e82f6-139">In the Item number field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="e82f6-140">Find installationens gebyrvarenummer på listen.</span><span class="sxs-lookup"><span data-stu-id="e82f6-140">In the list, find the installation charge item number.</span></span> <span data-ttu-id="e82f6-141">For eksempel S0001</span><span class="sxs-lookup"><span data-stu-id="e82f6-141">For example, S0001</span></span>
12. <span data-ttu-id="e82f6-142">Vælg installationens gebyrvarenummer.</span><span class="sxs-lookup"><span data-stu-id="e82f6-142">Select the installation charge item number.</span></span>
    * <span data-ttu-id="e82f6-143">Bemærk, at sammenholdelse ikke er blevet udført, siden du foretog ændringerne.</span><span class="sxs-lookup"><span data-stu-id="e82f6-143">Note that matching has not been performed since you made the changes.</span></span>  
13. <span data-ttu-id="e82f6-144">Klik på Opdater status for sammenholdelse.</span><span class="sxs-lookup"><span data-stu-id="e82f6-144">Click Update match status.</span></span>
14. <span data-ttu-id="e82f6-145">Klik på Gennemse i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="e82f6-145">On the Action Pane, click Review.</span></span>
15. <span data-ttu-id="e82f6-146">Klik på Detaljer om sammenholdelse.</span><span class="sxs-lookup"><span data-stu-id="e82f6-146">Click Matching details.</span></span>
    * <span data-ttu-id="e82f6-147">Den nye linje med tjenester behøver ikke at blive sammenholdt, så status forbliver "Ikke udført".</span><span class="sxs-lookup"><span data-stu-id="e82f6-147">The new line with services does not need to be matched so the status stays "Not performed".</span></span>  
16. <span data-ttu-id="e82f6-148">Vælg produktkvitteringen for den lagervare, du har modtaget.</span><span class="sxs-lookup"><span data-stu-id="e82f6-148">Select the product receipt for the inventory item that you received.</span></span>
    * <span data-ttu-id="e82f6-149">Linjen med produktkvitteringen blev sammenholdt, men der er en uoverensstemmelse i antallet eller prisen, så den mislykkes.</span><span class="sxs-lookup"><span data-stu-id="e82f6-149">The line with the product receipt was matched but there is a mismatch of quantity or price so it fails.</span></span>  
17. <span data-ttu-id="e82f6-150">Angiv et tal i feltet Enhedspris.</span><span class="sxs-lookup"><span data-stu-id="e82f6-150">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="e82f6-151">Nu, da enhedsprisen passer, opdateres status til Fuldført.</span><span class="sxs-lookup"><span data-stu-id="e82f6-151">Now that the unit price matches, the status is updated to Passed.</span></span> <span data-ttu-id="e82f6-152">Hvis politikken tillader uoverensstemmelser, eller hvis sammenholdelse kun er en advarsel, kan du stadig bogføre fakturaen.</span><span class="sxs-lookup"><span data-stu-id="e82f6-152">If your policy allows discrepancies or if matching is only a warning, you can still post the invoice.</span></span>  
18. <span data-ttu-id="e82f6-153">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e82f6-153">Close the page.</span></span>
19. <span data-ttu-id="e82f6-154">Klik på Bogfør.</span><span class="sxs-lookup"><span data-stu-id="e82f6-154">Click Post.</span></span>
20. <span data-ttu-id="e82f6-155">Luk formularen.</span><span class="sxs-lookup"><span data-stu-id="e82f6-155">Close the form.</span></span>
    * <span data-ttu-id="e82f6-156">Bemærk, at indkøbsordren ikke længere er angivet som modtaget, men ikke faktureret.</span><span class="sxs-lookup"><span data-stu-id="e82f6-156">Note that the purchase order is no longer listed as received but not invoiced.</span></span>  


