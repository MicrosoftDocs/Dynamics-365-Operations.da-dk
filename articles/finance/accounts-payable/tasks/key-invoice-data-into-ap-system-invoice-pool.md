---
title: Indtaste fakturadata i kreditorsystemet ved hjælp af en fakturapulje
description: Dette emne beskriver, hvordan du kan bruge indgangsbogen til at oprette fakturaer.
author: abruer
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e53de7091fd818bdc7085c404794e16dc84dd156
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979282"
---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a><span data-ttu-id="f8997-103">Indtaste fakturadata i kreditorsystemet ved hjælp af en fakturapulje</span><span class="sxs-lookup"><span data-stu-id="f8997-103">Key invoice data into the AP system using invoice pool</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f8997-104">Dette emne beskriver, hvordan du kan bruge indgangsbogen til at oprette fakturaer.</span><span class="sxs-lookup"><span data-stu-id="f8997-104">This topic describes how to use the invoice register to create invoices.</span></span> <span data-ttu-id="f8997-105">Brug derefter fakturapuljen til at afstemme fakturaen med en indkøbsordre, og færdiggør udgiften på siden med kreditorfakturaer.</span><span class="sxs-lookup"><span data-stu-id="f8997-105">Then use the invoice pool to match the invoice to a purchase order and finalize the expense in the vendor invoice page.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="f8997-106">Oprette en indkøbsordre</span><span class="sxs-lookup"><span data-stu-id="f8997-106">Create a purchase order</span></span>
1. <span data-ttu-id="f8997-107">I navigationsruden skal du gå til **Moduler > Kreditor > Indkøbsordrer > Indkøbsordrer**.</span><span class="sxs-lookup"><span data-stu-id="f8997-107">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > Purchase orders**.</span></span>
2. <span data-ttu-id="f8997-108">Vælg **Ny** for at oprette en ny indkøbsordre.</span><span class="sxs-lookup"><span data-stu-id="f8997-108">Select **New** to create a purchase order.</span></span>
3. <span data-ttu-id="f8997-109">I feltet **Kreditorkonto** skal du vælge en kreditor på rullelisten.</span><span class="sxs-lookup"><span data-stu-id="f8997-109">In the **Vendor account** field, select a vendor for the drop-down list.</span></span> <span data-ttu-id="f8997-110">Vælg for eksempel kreditor **1001**.</span><span class="sxs-lookup"><span data-stu-id="f8997-110">For example, select vendor **1001**.</span></span>
4. <span data-ttu-id="f8997-111">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="f8997-111">Select **OK**.</span></span>
5. <span data-ttu-id="f8997-112">Vælg servicevarenummeret på rullelisten i feltet **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="f8997-112">In the **Item number** field, select the services item number in the drop-down list.</span></span> <span data-ttu-id="f8997-113">Vælg for eksempel **S0001**.</span><span class="sxs-lookup"><span data-stu-id="f8997-113">For example, select **S0001**.</span></span> <span data-ttu-id="f8997-114">Nettobeløbet er 75,00.</span><span class="sxs-lookup"><span data-stu-id="f8997-114">The net amount is 75.00.</span></span>  <span data-ttu-id="f8997-115">Det er det beløb, som vi forventer på fakturaen.</span><span class="sxs-lookup"><span data-stu-id="f8997-115">That is the amount that we will expect on the invoice.</span></span>  
6. <span data-ttu-id="f8997-116">Vælg **Køb** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="f8997-116">On the action pane, select **Purchase**.</span></span>
7. <span data-ttu-id="f8997-117">Vælg **Bekræft**.</span><span class="sxs-lookup"><span data-stu-id="f8997-117">Select **Confirm**.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="f8997-118">Oprette og bogføre fakturaen</span><span class="sxs-lookup"><span data-stu-id="f8997-118">Create and post and invoice</span></span>
1. <span data-ttu-id="f8997-119">Gå i navigationsruden til **Moduler > Kreditorer > Fakturaer > Indgangsbog**.</span><span class="sxs-lookup"><span data-stu-id="f8997-119">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice register**.</span></span>
2. <span data-ttu-id="f8997-120">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="f8997-120">Select **New**.</span></span>
3. <span data-ttu-id="f8997-121">Åbn opslaget for at vælge navnet på den indgangsbog, du vil bruge.</span><span class="sxs-lookup"><span data-stu-id="f8997-121">Open the lookup to select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="f8997-122">Vælg navnet på den indgangsbog, du vil bruge.</span><span class="sxs-lookup"><span data-stu-id="f8997-122">Select the name of the invoice register that you want to use.</span></span>
5. <span data-ttu-id="f8997-123">Vælg **Linjer** for at åbne bogen og angive udgiftslinjer.</span><span class="sxs-lookup"><span data-stu-id="f8997-123">Select **Lines** to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="f8997-124">Vælg en kreditor i opslaget.</span><span class="sxs-lookup"><span data-stu-id="f8997-124">In the lookup, select a vendor.</span></span> <span data-ttu-id="f8997-125">Vælg for eksempel kreditor **1001**.</span><span class="sxs-lookup"><span data-stu-id="f8997-125">For example, select vendor **1001**.</span></span>
7. <span data-ttu-id="f8997-126">Angiv fakturanummeret i feltet **Faktura**.</span><span class="sxs-lookup"><span data-stu-id="f8997-126">In the **Invoice** field, enter the invoice number.</span></span>
8. <span data-ttu-id="f8997-127">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="f8997-127">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="f8997-128">Angiv et tal i feltet **Kredit**.</span><span class="sxs-lookup"><span data-stu-id="f8997-128">In the **Credit** field, enter a number.</span></span>
10. <span data-ttu-id="f8997-129">Åbn rullelisten i feltet **Indkøbsordre** for at vælge den indkøbsordre, du oprettede tidligere.</span><span class="sxs-lookup"><span data-stu-id="f8997-129">In the **Purchase order** field, open the drop-down list to select the purchase order that you created earlier.</span></span>
11. <span data-ttu-id="f8997-130">Fremhæv en godkender på rullelisten i feltet **Godkendt af**, og klik på **Vælg** for at vælge den pågældende godkender.</span><span class="sxs-lookup"><span data-stu-id="f8997-130">In the **Approved by** field, highlight an approver in the drop-down list and click **Select** to select that approver.</span></span>
12. <span data-ttu-id="f8997-131">Vælg **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="f8997-131">Select **Post**.</span></span>

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a><span data-ttu-id="f8997-132">Åbne en faktura fra puljen og tilpasse den til en indkøbsordre for at fuldføre fakturaprocessen</span><span class="sxs-lookup"><span data-stu-id="f8997-132">Open an invoice from the pool and match it to a purchase order to complete the invoice process</span></span>
1. <span data-ttu-id="f8997-133">Gå i navigationsruden til **Moduler > Kreditorer > Fakturaer > Fakturapulje**.</span><span class="sxs-lookup"><span data-stu-id="f8997-133">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice pool**.</span></span>
2. <span data-ttu-id="f8997-134">Vælg **Indkøbsordre** for at oprette en kreditorfaktura ud fra fakturaen i puljen.</span><span class="sxs-lookup"><span data-stu-id="f8997-134">Select **Purchase order** to create a vendor invoice from the invoice in the pool.</span></span>
3. <span data-ttu-id="f8997-135">Vælg den faktura, du vil gennemse.</span><span class="sxs-lookup"><span data-stu-id="f8997-135">Select the invoice that you want to review.</span></span>
4. <span data-ttu-id="f8997-136">Vælg **Opdater status for sammenholdelse** for at fuldføre sammenholdelsen.</span><span class="sxs-lookup"><span data-stu-id="f8997-136">Select **Update match status** to complete the matching.</span></span>
5. <span data-ttu-id="f8997-137">Vælg **Indstillinger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="f8997-137">On the action pane, select **Options**.</span></span>
6. <span data-ttu-id="f8997-138">Vælg **Skift visning**.</span><span class="sxs-lookup"><span data-stu-id="f8997-138">Select **Change view**.</span></span>
7. <span data-ttu-id="f8997-139">Vælg **Gittervisning**.</span><span class="sxs-lookup"><span data-stu-id="f8997-139">Select **Grid view**.</span></span>
8. <span data-ttu-id="f8997-140">Vælg **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="f8997-140">Select **Post**.</span></span>
9. <span data-ttu-id="f8997-141">Luk formularen.</span><span class="sxs-lookup"><span data-stu-id="f8997-141">Close the form.</span></span>
10. <span data-ttu-id="f8997-142">Gå i navigationsruden til **Moduler > Kreditor > Kreditorer > Kreditorer**.</span><span class="sxs-lookup"><span data-stu-id="f8997-142">In the navigation pane, go to **Modules > Accounts payable > Vendors > Vendors**.</span></span>
11. <span data-ttu-id="f8997-143">Vælg den kreditor, der stod i indkøbsordren.</span><span class="sxs-lookup"><span data-stu-id="f8997-143">Select the vendor that was on the purchase order.</span></span> <span data-ttu-id="f8997-144">Vælg for eksempel kreditor **1001**.</span><span class="sxs-lookup"><span data-stu-id="f8997-144">For example, select vendor **1001**.</span></span>
12. <span data-ttu-id="f8997-145">Vælg **Kreditor** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="f8997-145">On the action pane, select **Vendor**.</span></span>
13. <span data-ttu-id="f8997-146">Vælg **Transaktioner**.</span><span class="sxs-lookup"><span data-stu-id="f8997-146">Select **Transactions**.</span></span>
14. <span data-ttu-id="f8997-147">Vælg den faktura, du oprettede.</span><span class="sxs-lookup"><span data-stu-id="f8997-147">Select the invoice that you created.</span></span> <span data-ttu-id="f8997-148">Periodiseringen af indgangsbogen blev tilbageført og bogført på den relevante udgiftskonto.</span><span class="sxs-lookup"><span data-stu-id="f8997-148">The invoice register accrual was reversed and posted to the appropriate expense account.</span></span>  

