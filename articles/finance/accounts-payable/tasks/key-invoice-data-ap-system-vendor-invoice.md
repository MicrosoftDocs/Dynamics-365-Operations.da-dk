---
title: Vigtigste fakturadata i kreditor, der bruger en kreditorfaktura
description: Denne opgaveguide hjælper dig med at oprette en kreditorfaktura fra en indkøbsordre og få vist resultaterne af sammenholdelse af indkøbsordre, tilgang og faktura (trevejs-sammenholdelse).
author: abruer
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines, VendEditInvoice, InventItemIdLookupSimple, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 74065fa3177c8add29e64ce0f77461df036c8fe5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979307"
---
# <a name="key-invoice-data-in-ap-using-a-vendor-invoice"></a><span data-ttu-id="a87f3-103">Vigtigste fakturadata i kreditor, der bruger en kreditorfaktura</span><span class="sxs-lookup"><span data-stu-id="a87f3-103">Key invoice data in AP using a vendor invoice</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a87f3-104">Denne opgaveguide hjælper dig med at oprette en kreditorfaktura fra en indkøbsordre og få vist resultaterne af sammenholdelse af indkøbsordre, tilgang og faktura (trevejs-sammenholdelse).</span><span class="sxs-lookup"><span data-stu-id="a87f3-104">This task guide will help you create a vendor invoice from a purchase order and view the results of matching the purchase order, receipt, and invoice (3 way matching).</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="a87f3-105">Oprette en indkøbsordre</span><span class="sxs-lookup"><span data-stu-id="a87f3-105">Create a purchase order</span></span>
1. <span data-ttu-id="a87f3-106">I navigationsruden skal du gå til **Moduler > Kreditor > Indkøbsordrer > Alle indkøbsordrer**.</span><span class="sxs-lookup"><span data-stu-id="a87f3-106">In the Navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
2. <span data-ttu-id="a87f3-107">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a87f3-107">Click **New**.</span></span>
3. <span data-ttu-id="a87f3-108">I feltet **Kreditorkonto** skal du klikke på rullelisten for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="a87f3-108">In the **Vendor account** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="a87f3-109">Find en kreditor, du vil vælge.</span><span class="sxs-lookup"><span data-stu-id="a87f3-109">Find a vendor to select.</span></span> <span data-ttu-id="a87f3-110">Rul for eksempel ned til US-104.</span><span class="sxs-lookup"><span data-stu-id="a87f3-110">For example, scroll down to US-104.</span></span>
5. <span data-ttu-id="a87f3-111">Vælg kreditor US-104.</span><span class="sxs-lookup"><span data-stu-id="a87f3-111">Select vendor US-104.</span></span>
6. <span data-ttu-id="a87f3-112">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="a87f3-112">Click **OK**.</span></span>
7. <span data-ttu-id="a87f3-113">Klik på rullelisten i feltet **Varenummer** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="a87f3-113">In the **Item number** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="a87f3-114">Vælg en lagervare.</span><span class="sxs-lookup"><span data-stu-id="a87f3-114">Select an inventory item.</span></span> <span data-ttu-id="a87f3-115">Du kan for eksempel vælge varenummer 1000.</span><span class="sxs-lookup"><span data-stu-id="a87f3-115">For example, select item number 1000.</span></span>
9. <span data-ttu-id="a87f3-116">Vis eller skjul oversigtspanelet **Linjedetaljer**.</span><span class="sxs-lookup"><span data-stu-id="a87f3-116">Expand the **Line details** fastTab.</span></span>
10. <span data-ttu-id="a87f3-117">Klik på fanen **Opsætning**. Du kan tilsidesætte sammenholdelsespolitikken for at undlade at bruge sammenholdelse, tovejssammenholdelse eller trevejssammenholdelse.</span><span class="sxs-lookup"><span data-stu-id="a87f3-117">Click the **Setup** tab. You can override the matching policy to use no matching, 2-way matching, or 3-way matching.</span></span>  
11. <span data-ttu-id="a87f3-118">Klik på **Køb** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="a87f3-118">On the Action Pane, click **Purchase**.</span></span>
12. <span data-ttu-id="a87f3-119">Klik på **Bekræft**.</span><span class="sxs-lookup"><span data-stu-id="a87f3-119">Click **Confirm**.</span></span>

## <a name="receive-the-products"></a><span data-ttu-id="a87f3-120">Modtage produkterne</span><span class="sxs-lookup"><span data-stu-id="a87f3-120">Receive the products</span></span>
1. <span data-ttu-id="a87f3-121">Klik på **Modtag** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="a87f3-121">On the Action Pane, click **Receive**.</span></span>
2. <span data-ttu-id="a87f3-122">Klik på **Produktkvittering**.</span><span class="sxs-lookup"><span data-stu-id="a87f3-122">Click **Product receipt**.</span></span>
3. <span data-ttu-id="a87f3-123">Angiv nummeret på produktkvitteringen i feltet **Produktkvittering**.</span><span class="sxs-lookup"><span data-stu-id="a87f3-123">In the **Product receipt** field, enter the product receipt number.</span></span> <span data-ttu-id="a87f3-124">Angiv for eksempel PR123.</span><span class="sxs-lookup"><span data-stu-id="a87f3-124">For example, enter PR123.</span></span>
4. <span data-ttu-id="a87f3-125">Klik på **OK** for at bogføre produktkvitteringen.</span><span class="sxs-lookup"><span data-stu-id="a87f3-125">Click **OK** to post the product receipt.</span></span>
5. <span data-ttu-id="a87f3-126">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a87f3-126">Close the page.</span></span>

## <a name="create-a-vendor-invoice"></a><span data-ttu-id="a87f3-127">Oprette en kreditorfaktura</span><span class="sxs-lookup"><span data-stu-id="a87f3-127">Create a vendor invoice</span></span>
1. <span data-ttu-id="a87f3-128">I navigationsruden skal du gå til **Moduler > Kreditor > Indkøbsordrer > Modtagne indkøbsordrer der ikke er bogført**.</span><span class="sxs-lookup"><span data-stu-id="a87f3-128">In the Navigation pane, go to **Modules > Accounts payable > Purchase orders > Purchase orders received but not invoiced**.</span></span>
2. <span data-ttu-id="a87f3-129">Vælg den indkøbsordrelinje, du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="a87f3-129">Select the purchase order that you created.</span></span>
3. <span data-ttu-id="a87f3-130">Klik på **Faktura** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="a87f3-130">On the Action Pane, click **Invoice**.</span></span>
4. <span data-ttu-id="a87f3-131">Klik på **Faktura**.</span><span class="sxs-lookup"><span data-stu-id="a87f3-131">Click **Invoice**.</span></span>
5. <span data-ttu-id="a87f3-132">Angiv fakturanummeret i feltet **Nummer**.</span><span class="sxs-lookup"><span data-stu-id="a87f3-132">In the **Number** field, enter the invoice number.</span></span>
6. <span data-ttu-id="a87f3-133">Angiv en værdi i feltet **Fakturabeskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="a87f3-133">In the **Invoice description** field, type a value.</span></span>
7. <span data-ttu-id="a87f3-134">Indtast en dato i feltet **Fakturadato**.</span><span class="sxs-lookup"><span data-stu-id="a87f3-134">In the **Invoice date** field, enter a date.</span></span>
8. <span data-ttu-id="a87f3-135">Indtast "1200" i feltet **Enhedspris**.</span><span class="sxs-lookup"><span data-stu-id="a87f3-135">In the **Unit price** field, enter 1200.</span></span>
9. <span data-ttu-id="a87f3-136">Klik på **Tilføj linje**.</span><span class="sxs-lookup"><span data-stu-id="a87f3-136">Click **Add line**.</span></span>
10. <span data-ttu-id="a87f3-137">Klik på rullelisten i feltet **Varenummer** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="a87f3-137">In the **Item number** field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="a87f3-138">Find installationens gebyrvarenummer på listen.</span><span class="sxs-lookup"><span data-stu-id="a87f3-138">In the list, find the installation charge item number.</span></span> <span data-ttu-id="a87f3-139">For eksempel S0001</span><span class="sxs-lookup"><span data-stu-id="a87f3-139">For example, S0001</span></span>
12. <span data-ttu-id="a87f3-140">Vælg installationens gebyrvarenummer.</span><span class="sxs-lookup"><span data-stu-id="a87f3-140">Select the installation charge item number.</span></span> <span data-ttu-id="a87f3-141">Bemærk, at sammenholdelse ikke er blevet udført, siden du foretog ændringerne.</span><span class="sxs-lookup"><span data-stu-id="a87f3-141">Note that matching has not been performed since you made the changes.</span></span>  
13. <span data-ttu-id="a87f3-142">Klik på **Opdater status for match**.</span><span class="sxs-lookup"><span data-stu-id="a87f3-142">Click **Update match status**.</span></span>
14. <span data-ttu-id="a87f3-143">Klik på **Gennemse** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="a87f3-143">On the Action Pane, click **Review**.</span></span>
15. <span data-ttu-id="a87f3-144">Klik på **Detaljer om sammenholdelse**.</span><span class="sxs-lookup"><span data-stu-id="a87f3-144">Click **Matching details**.</span></span> <span data-ttu-id="a87f3-145">Den nye linje med tjenester behøver ikke at blive sammenholdt, så status forbliver "Ikke udført".</span><span class="sxs-lookup"><span data-stu-id="a87f3-145">The new line with services does not need to be matched so the status stays "Not performed".</span></span>  
16. <span data-ttu-id="a87f3-146">Vælg produktkvitteringen for den lagervare, du har modtaget.</span><span class="sxs-lookup"><span data-stu-id="a87f3-146">Select the product receipt for the inventory item that you received.</span></span> <span data-ttu-id="a87f3-147">Linjen med produktkvitteringen blev sammenholdt, men der er en uoverensstemmelse i antallet eller prisen, så den mislykkes.</span><span class="sxs-lookup"><span data-stu-id="a87f3-147">The line with the product receipt was matched but there is a mismatch of quantity or price so it fails.</span></span>  
17. <span data-ttu-id="a87f3-148">Angiv et tal i feltet **Enhedspris**.</span><span class="sxs-lookup"><span data-stu-id="a87f3-148">In the **Unit price** field, enter a number.</span></span> <span data-ttu-id="a87f3-149">Nu, da enhedsprisen passer, opdateres status til Fuldført.</span><span class="sxs-lookup"><span data-stu-id="a87f3-149">Now that the unit price matches, the status is updated to Passed.</span></span> <span data-ttu-id="a87f3-150">Hvis politikken tillader uoverensstemmelser, eller hvis sammenholdelse kun er en advarsel, kan du stadig bogføre fakturaen.</span><span class="sxs-lookup"><span data-stu-id="a87f3-150">If your policy allows discrepancies or if matching is only a warning, you can still post the invoice.</span></span>  
18. <span data-ttu-id="a87f3-151">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a87f3-151">Close the page.</span></span>
19. <span data-ttu-id="a87f3-152">Klik på **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="a87f3-152">Click **Post**.</span></span>
20. <span data-ttu-id="a87f3-153">Luk formularen.</span><span class="sxs-lookup"><span data-stu-id="a87f3-153">Close the form.</span></span> <span data-ttu-id="a87f3-154">Bemærk, at indkøbsordren ikke længere er angivet som modtaget, men ikke faktureret.</span><span class="sxs-lookup"><span data-stu-id="a87f3-154">Note that the purchase order is no longer listed as received but not invoiced.</span></span>  

