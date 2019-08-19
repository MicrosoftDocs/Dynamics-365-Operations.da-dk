---
title: Fastlægge betingelser for debitorbetaling
description: Denne procedure definerer opsætning af en kasserabat og forfaldsdato.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PaymDay, PaymTerm, CashDisc
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cddccbeb60e3eb9e498affcaa547fddb145a2bb2
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846409"
---
# <a name="establish-customer-payment-terms"></a><span data-ttu-id="e8916-103">Fastlægge betingelser for debitorbetaling</span><span class="sxs-lookup"><span data-stu-id="e8916-103">Establish customer payment terms</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e8916-104">Denne procedure definerer opsætning af en kasserabat og forfaldsdato.</span><span class="sxs-lookup"><span data-stu-id="e8916-104">This procedure defines a cash discount and due date setup.</span></span> <span data-ttu-id="e8916-105">Denne opgaveguide anvender demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="e8916-105">This task guide uses the USMF demo company.</span></span>

1. <span data-ttu-id="e8916-106">Gå til Debitor > Betalingsopsætning > Betalingsdage.</span><span class="sxs-lookup"><span data-stu-id="e8916-106">Go to Accounts receivable > Payments setup > Payment days.</span></span>
    * <span data-ttu-id="e8916-107">Opsætningen af betalingsbetingelserne er delt for Debitor og Kreditor.</span><span class="sxs-lookup"><span data-stu-id="e8916-107">The setup for the Terms of payment is shared for Accounts receivable and Accounts payable.</span></span> <span data-ttu-id="e8916-108">Hvis du definerer den i modulet, bliver den også tilgængelig i det andet modul.</span><span class="sxs-lookup"><span data-stu-id="e8916-108">If you define it in module, it will be available in the other module also.</span></span> <span data-ttu-id="e8916-109">Til denne opgaveguide angiver jeg alle betalingsbetingelserne under Debitor.</span><span class="sxs-lookup"><span data-stu-id="e8916-109">For this task guide, I set up all the terms of payment under Accounts receivable.</span></span>  
2. <span data-ttu-id="e8916-110">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="e8916-110">Click New.</span></span>
    * <span data-ttu-id="e8916-111">Opret en betalingsdag, hvis betalingsbetingelserne kræver en bestemt dag i ugen (mandag, tirsdag osv.) eller en bestemt dato i måneden (5., 10 osv).</span><span class="sxs-lookup"><span data-stu-id="e8916-111">Create a payment day if your terms of payment require a specific day of the week (Monday, Tuesday, etc) or a specific date of the month (5th, 10th, etc).</span></span>  
3. <span data-ttu-id="e8916-112">Angiv et id for betalingsdagen i feltet Betalingsdag.</span><span class="sxs-lookup"><span data-stu-id="e8916-112">In the Payment day field, enter an ID for the Payment day in the payment day field.</span></span>
4. <span data-ttu-id="e8916-113">Angiv en beskrivelse af betalingsdagen i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="e8916-113">In the Description field, enter a description of the payment day.</span></span>
5. <span data-ttu-id="e8916-114">Vælg enten Uge eller Måned i feltet Uge/Måned.</span><span class="sxs-lookup"><span data-stu-id="e8916-114">In the Week/Month field, select either Week or Month.</span></span>
    * <span data-ttu-id="e8916-115">Hvis du vil angive en dag i ugen, såsom mandag, skal du vælge Uge.</span><span class="sxs-lookup"><span data-stu-id="e8916-115">If you want to enter a day of the week, such as Monday, select Week.</span></span> <span data-ttu-id="e8916-116">Hvis du vil angive en dato i måneden, såsom den 10., skal du vælge Måned.</span><span class="sxs-lookup"><span data-stu-id="e8916-116">If you want to enter a date in the month, such as the 10th, select Month.</span></span> <span data-ttu-id="e8916-117">Væld Måned i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="e8916-117">Select Month for this example.</span></span>  
6. <span data-ttu-id="e8916-118">Angiv en dato i feltet Dag i måned.</span><span class="sxs-lookup"><span data-stu-id="e8916-118">In the Day of month field, enter a date.</span></span>
    * <span data-ttu-id="e8916-119">Datoen skal angives som et tal, f.eks "10" og ikke "10.".</span><span class="sxs-lookup"><span data-stu-id="e8916-119">The date should be entered as a number, such as '10', and not as '10th'.</span></span>  
7. <span data-ttu-id="e8916-120">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="e8916-120">Click Save.</span></span>
8. <span data-ttu-id="e8916-121">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e8916-121">Close the page.</span></span>
9. <span data-ttu-id="e8916-122">Gå til Debitor > Betalingsopsætning > Betalingsbetingelse.</span><span class="sxs-lookup"><span data-stu-id="e8916-122">Go to Accounts receivable > Payments setup > Terms of payment.</span></span>
10. <span data-ttu-id="e8916-123">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="e8916-123">Click New.</span></span>
    * <span data-ttu-id="e8916-124">Betalingsbetingelser bruges til at definere, hvordan forfaldsdatoer beregnes.</span><span class="sxs-lookup"><span data-stu-id="e8916-124">Terms of payment is used to define how the due dates will be calculated.</span></span> <span data-ttu-id="e8916-125">Opsætningen af datoen for kasserabatten er defineret på en separat side.</span><span class="sxs-lookup"><span data-stu-id="e8916-125">The cash discount date setup is defined in a separate page.</span></span>  
11. <span data-ttu-id="e8916-126">Angiv et id i feltet Betalingsbetingelser.</span><span class="sxs-lookup"><span data-stu-id="e8916-126">In the Terms of payment field, enter an ID in the Terms of payment field.</span></span>
12. <span data-ttu-id="e8916-127">Indtast en beskrivelse i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="e8916-127">In the Description field, enter a description.</span></span>
13. <span data-ttu-id="e8916-128">Vælg en betalingsmetode, f.eks. Efterkrav, Aktuel måned osv.</span><span class="sxs-lookup"><span data-stu-id="e8916-128">Select a Payment method such as COD, Net, Current month, etc.</span></span>
    * <span data-ttu-id="e8916-129">Betalingsmåden bruges til at definere starten for, hvordan forfaldsdatoen beregnes.</span><span class="sxs-lookup"><span data-stu-id="e8916-129">The Payment method is used to define the start of how the due will be calculated.</span></span>  <span data-ttu-id="e8916-130">Net bruges for eksempel, hvis forfaldsdatoen altid er et angivet antal måneder eller dage efter fakturadatoen.</span><span class="sxs-lookup"><span data-stu-id="e8916-130">For example, Net is used if the due date is always a set number of months or days after the invoice date.</span></span> <span data-ttu-id="e8916-131">Efterkrav kan bruges i tilfælde, hvor betalingen skal falde ved fakturering, så der ikke beregnes en forfaldsdato.</span><span class="sxs-lookup"><span data-stu-id="e8916-131">COD can be used to when payment is required upon invoice, so a due date wouldn't be calculated.</span></span> <span data-ttu-id="e8916-132">Vælg Indeværende måned for denne opgaveguide.</span><span class="sxs-lookup"><span data-stu-id="e8916-132">Select Current month for this task guide.</span></span>  
14. <span data-ttu-id="e8916-133">Vælg en betalingsdag, hvis en bestemt dag i ugen eller dato medtages i beregningen.</span><span class="sxs-lookup"><span data-stu-id="e8916-133">Select a Payment day if a specific day of the  week or date are included in the calculation.</span></span>
    * <span data-ttu-id="e8916-134">Du kan angive et antal i måneder eller dage, afhængigt af dine betalingsbetingelser.</span><span class="sxs-lookup"><span data-stu-id="e8916-134">Depending on your terms of payment, you may enter a quantity in Months or Days.</span></span> <span data-ttu-id="e8916-135">Eller du kan bruge betalingsplanen eller betalingsdagen, som skal "tilføjes" til slutningen af betalingsmåden.</span><span class="sxs-lookup"><span data-stu-id="e8916-135">Or you can use the Payment schedule or Payment day to 'add' to the end of the Payment method.</span></span> <span data-ttu-id="e8916-136">Hvis forfaldsdatoen altid vil være den 10. i næste måned, skal du vælge den 10. som betalingsdag.</span><span class="sxs-lookup"><span data-stu-id="e8916-136">If the due date will always be the 10th of the next month, select a Payment day of the 10th.</span></span>  
15. <span data-ttu-id="e8916-137">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="e8916-137">Click Save.</span></span>
16. <span data-ttu-id="e8916-138">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e8916-138">Close the page.</span></span>
17. <span data-ttu-id="e8916-139">Gå til Debitor > Betalingsopsætning > Kasserabatter.</span><span class="sxs-lookup"><span data-stu-id="e8916-139">Go to Accounts receivable > Payments setup > Cash discounts.</span></span>
18. <span data-ttu-id="e8916-140">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="e8916-140">Click New.</span></span>
    * <span data-ttu-id="e8916-141">Denne side bruges til at definere, hvordan kasserabatdatoen beregnes.</span><span class="sxs-lookup"><span data-stu-id="e8916-141">This page is used to define how the cash discount date will be calculated.</span></span>  
19. <span data-ttu-id="e8916-142">Angiv et id i feltet Kasserabat.</span><span class="sxs-lookup"><span data-stu-id="e8916-142">In the Cash discount field, enter an ID in the Cash discount field.</span></span>
20. <span data-ttu-id="e8916-143">Indtast en beskrivelse i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="e8916-143">In the Description field, enter a description.</span></span>
21. <span data-ttu-id="e8916-144">Hvis der findes en lagdelt kasserabat, kan du vælge Næste rabatkode, der er relevant efter denne nye kasserabat.</span><span class="sxs-lookup"><span data-stu-id="e8916-144">If a tiered cash discount is available, select the Next discount code that is relevant after this new cash discount.</span></span>
22. <span data-ttu-id="e8916-145">Angiv antal dage, der bruges til at beregne kasserabatdatoen.</span><span class="sxs-lookup"><span data-stu-id="e8916-145">Enter the number of days used to calculate the cash dicount date.</span></span>
    * <span data-ttu-id="e8916-146">Hvis der vælges nettoprincip, føjes antallet af dage til fakturadatoen for at beregne kasserabatdatoen.</span><span class="sxs-lookup"><span data-stu-id="e8916-146">If Net principle is selected, the number of days will be added to the invoice date to calculate the cash discount date.</span></span>  
23. <span data-ttu-id="e8916-147">Angiv procentdelen af kasserabatten.</span><span class="sxs-lookup"><span data-stu-id="e8916-147">Enter the percentage of the cash discount.</span></span>
24. <span data-ttu-id="e8916-148">Angiv den hovedkonto, som kasserabatten bogfører til for debitorfakturaer.</span><span class="sxs-lookup"><span data-stu-id="e8916-148">Enter the main account to which the cash discount will post for customer invoices.</span></span>
25. <span data-ttu-id="e8916-149">Vælg en indstilling i feltet Rabatmodkonti.</span><span class="sxs-lookup"><span data-stu-id="e8916-149">In the Discount offset accounts field, select an option.</span></span>
    * <span data-ttu-id="e8916-150">Hvis du vælger "Konti på fakturalinjer", bogføres kasserabatten til samme aktiv/udgiftshovedkonto på linjerne i kreditorfakturaen.</span><span class="sxs-lookup"><span data-stu-id="e8916-150">If you select 'Accounts on the invoice lines', the cash discount will post to the same asset/expense main account on the lines of the vendor invoice.</span></span> <span data-ttu-id="e8916-151">Kasserabatten"Brug hovedkonto til kreditorfakturaer", bogføres kasserabatten til den hovedkonto, du definerer i "Hovedkonto for kreditorfakturaer".</span><span class="sxs-lookup"><span data-stu-id="e8916-151">If you select 'Use main account for vendor invoices', the cash discount will post to the main account you define in the 'Main account for vendor invoices'.</span></span> <span data-ttu-id="e8916-152">I dette eksempel skal du vælge "Brug hovedkonto til kreditorfakturaer".</span><span class="sxs-lookup"><span data-stu-id="e8916-152">For this example, select 'Use main account for vendor invoices.'</span></span>  
26. <span data-ttu-id="e8916-153">Angiv den hovedkonto, som kasserabatten bogfører til for kreditorfakturaer.</span><span class="sxs-lookup"><span data-stu-id="e8916-153">Enter the main account to which the cash discount will post for vendor invoices.</span></span>
27. <span data-ttu-id="e8916-154">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="e8916-154">Click Save.</span></span>

