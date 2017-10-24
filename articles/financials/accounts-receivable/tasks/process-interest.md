--- 
title: Behandle rente
description: "Denne procedure viser, hvordan du kan oprette, udskrive og bogføre rentenotaer."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 543ac29ac1b1cbad52f1c155ac90b04d0c122a1f
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="process-interest"></a><span data-ttu-id="4cc9b-103">Behandle rente</span><span class="sxs-lookup"><span data-stu-id="4cc9b-103">Process interest</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4cc9b-104">Denne procedure viser, hvordan du kan oprette, udskrive og bogføre rentenotaer.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-104">This procedure shows how to create, print, and post interest notes.</span></span> <span data-ttu-id="4cc9b-105">Denne opgave bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-interest-on-the-posting-profile"></a><span data-ttu-id="4cc9b-106">Konfigurer rente i posteringsprofilen</span><span class="sxs-lookup"><span data-stu-id="4cc9b-106">Set up interest on the posting profile</span></span>
1. <span data-ttu-id="4cc9b-107">Gå til Kredit og inkasso > Opsætning > Debitorposteringsprofiler.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-107">Go to Credit and collections > Setup > Customer posting profiles.</span></span>
2. <span data-ttu-id="4cc9b-108">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-108">Click Edit.</span></span>
    * <span data-ttu-id="4cc9b-109">Vælg en rentekode på rullelisten.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-109">Select an interest code from the drop-down list.</span></span> <span data-ttu-id="4cc9b-110">Hvis du ikke vil have beregnet rente for transaktioner med denne posteringsprofil, skal du undlade at udfylde feltet.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-110">If you do not want interest calculated for transactions using this posting profile, leave the field blank.</span></span>  
    * <span data-ttu-id="4cc9b-111">Under fanen Tabelbegrænsninger kan du ændre den måde, som rente behandles på.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-111">The Table restriction tab allows you to change the way that interest is processed.</span></span> <span data-ttu-id="4cc9b-112">Hvis dette felt er indstillet til Ja, beregnes der rente for denne posteringsprofil.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-112">If this field is set to Yes, then interest will be calculated for this posting profile.</span></span>  

## <a name="calculate-interest"></a><span data-ttu-id="4cc9b-113">Beregn renter</span><span class="sxs-lookup"><span data-stu-id="4cc9b-113">Calculate interest</span></span>
1. <span data-ttu-id="4cc9b-114">Gå til Kredit og inkasso > Rente > Opret rentenotaer.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-114">Go to Credit and collections > Interest > Create interest notes.</span></span>
    * <span data-ttu-id="4cc9b-115">Du skal vælge de transaktionstyper, du vil beregne rente for.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-115">You must select the transaction types for which you will calculate interest.</span></span> <span data-ttu-id="4cc9b-116">Alle åbne transaktioner for disse typer medtages i beregningen.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-116">All of the open transactions for these types will be included in the calculation.</span></span>  
    * <span data-ttu-id="4cc9b-117">Hvis du vælger Rente, skal du beregne renten af renten.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-117">If you select Interest, you will calculate interest on interest.</span></span> <span data-ttu-id="4cc9b-118">Du bør kontrollere lovgivning vedrørende beregning af renters rente, før du inkluderer disse transaktioner.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-118">You may want to check the laws governing the calculation of interest on interest before including these transactions.</span></span>  
    * <span data-ttu-id="4cc9b-119">Rente beregnes fra denne dato til "Til dato".</span><span class="sxs-lookup"><span data-stu-id="4cc9b-119">Interest will be calculated from this date to the "To date".</span></span> <span data-ttu-id="4cc9b-120">Hvis du ikke angiver en "Fra dato", annulleres alle ikke-bogførte rentenotaer, og rente genberegnes fra transaktionsdatoen.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-120">If you do not specific a "From date", then all unposted interest notes will be canceled and interest will be recalculated from the transaction date.</span></span>  
2. <span data-ttu-id="4cc9b-121">Angiv datoen for rentenotaen.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-121">Enter the date of the interest note.</span></span>
    * <span data-ttu-id="4cc9b-122">Der findes tre posteringsprofilindstillinger: Konto – Brug den posteringsprofil, der er tildelt kundekontoen for hver rentenota.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-122">There are three posting profile options:   Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   <span data-ttu-id="4cc9b-123">Vælg – Brug den posteringsprofil, som du vælger i feltet Posteringsprofil.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-123">Select – Use the posting profile that you select in the Posting profile field.</span></span>   <span data-ttu-id="4cc9b-124">Transaktion – Brug den individuelle posteringsprofil fra transaktioner, som der beregnes rente på for hver rentenota.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-124">Transaction – Use the individual posting profile from transactions on which interest is calculated for each interest note.</span></span> <span data-ttu-id="4cc9b-125">For transaktioner, som ikke har en tildelt posteringsprofil, anvendes den posteringsprofil, der er angivet i området Finans og moms i formen Debitorparametre.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-125">Transactions that do not have an assigned posting profile will use the posting profile that is specified in the Ledger and sales tax area of the Accounts receivable parameters form.</span></span>  
    * <span data-ttu-id="4cc9b-126">Vælg en posteringsprofil her, hvis du har ændret "Anvend posteringsprofil fra" til Vælg.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-126">Select a posting profile here if you changed "Use posting profile from" to "Select".</span></span>  
3. <span data-ttu-id="4cc9b-127">Udvis eller skjul sektionen Poster, der skal indgå.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-127">Expand or collapse the Records to include section.</span></span>
4. <span data-ttu-id="4cc9b-128">Klik på Filtrér.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-128">Click Filter.</span></span>
5. <span data-ttu-id="4cc9b-129">Angiv i feltet kriterier et kunde-ID.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-129">In the Criteria field, enter a Customer ID.</span></span> <span data-ttu-id="4cc9b-130">Indtast for eksempel "US-001".</span><span class="sxs-lookup"><span data-stu-id="4cc9b-130">For example, enter 'US-001'..</span></span>
6. <span data-ttu-id="4cc9b-131">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-131">Click OK.</span></span>
7. <span data-ttu-id="4cc9b-132">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-132">Click OK.</span></span>

## <a name="print-interest-notes"></a><span data-ttu-id="4cc9b-133">Udskrivning af rentenotaer</span><span class="sxs-lookup"><span data-stu-id="4cc9b-133">Print interest notes</span></span>
1. <span data-ttu-id="4cc9b-134">Gå til Kredit og inkasso > Rente > Gennemse og behandl rentenotaer.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-134">Go to Credit and collections > Interest > Review and process interest notes.</span></span>
2. <span data-ttu-id="4cc9b-135">Vælg "Oprettet" i feltet Status.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-135">In the Status field, select 'Created'.</span></span>
3. <span data-ttu-id="4cc9b-136">Vælg "Ikke udskrevet" i feltet Udskrevet.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-136">In the Printed field, select 'Not printed'.</span></span>
4. <span data-ttu-id="4cc9b-137">Klik på Udskriv.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-137">Click Print.</span></span>
5. <span data-ttu-id="4cc9b-138">Udvis eller skjul sektionen Poster, der skal indgå.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-138">Expand or collapse the Records to include section.</span></span>
6. <span data-ttu-id="4cc9b-139">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-139">Click OK.</span></span>
7. <span data-ttu-id="4cc9b-140">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-140">Close the page.</span></span>

## <a name="post-the-interest-note"></a><span data-ttu-id="4cc9b-141">Bogfør rentenotaen</span><span class="sxs-lookup"><span data-stu-id="4cc9b-141">Post the interest note</span></span>
1. <span data-ttu-id="4cc9b-142">Vælg en rentenota, der er klar til at blive bogført (status er Oprettet).</span><span class="sxs-lookup"><span data-stu-id="4cc9b-142">Select an interest note that is ready to post (status is created).</span></span>
2. <span data-ttu-id="4cc9b-143">Klik på Bogfør.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-143">Click Post.</span></span>
3. <span data-ttu-id="4cc9b-144">Angiv bogføringsdatoen for rentenotaen.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-144">Enter the posting date for the interest note.</span></span>
    * <span data-ttu-id="4cc9b-145">Vælg Ja for at oprette en transaktion i finansmodulet for hver enkelt rentenota.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-145">Select Yes to create a general ledger transaction for each interest note.</span></span>     <span data-ttu-id="4cc9b-146">Hvis du ikke vælger Ja, samles renten fra alle rentenotaer til debitoren, og den bogføres til finansmodulet i én transaktion.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-146">If you do not select Yes, the interest on all interest notes to the customer is accumulated and posted to the general ledger in one transaction.</span></span>  
4. <span data-ttu-id="4cc9b-147">Udvis eller skjul sektionen Poster, der skal indgå.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-147">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="4cc9b-148">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-148">Click OK.</span></span>
6. <span data-ttu-id="4cc9b-149">Vælg "Bogført" i feltet Status.</span><span class="sxs-lookup"><span data-stu-id="4cc9b-149">In the Status field, select 'Posted'.</span></span>


