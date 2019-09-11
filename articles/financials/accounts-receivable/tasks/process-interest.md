---
title: Behandle rente
description: Denne procedure viser, hvordan du kan oprette, udskrive og bogføre rentenotaer.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, SysQueryForm, CustInterestNote, SrsReportViewerForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7170a7a14237058064ed3091e9437cae312e6bd5
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916270"
---
# <a name="process-interest"></a><span data-ttu-id="ecdf8-103">Behandle rente</span><span class="sxs-lookup"><span data-stu-id="ecdf8-103">Process interest</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ecdf8-104">Denne procedure viser, hvordan du kan oprette, udskrive og bogføre rentenotaer.</span><span class="sxs-lookup"><span data-stu-id="ecdf8-104">This procedure shows how to create, print, and post interest notes.</span></span> <span data-ttu-id="ecdf8-105">Denne opgave bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="ecdf8-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-interest-on-the-posting-profile"></a><span data-ttu-id="ecdf8-106">Konfigurer rente i posteringsprofilen</span><span class="sxs-lookup"><span data-stu-id="ecdf8-106">Set up interest on the posting profile</span></span>
1. <span data-ttu-id="ecdf8-107">Gå i **Navigationsrude** til **Moduler > Kredit > Opsætning > Debitorposteringsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="ecdf8-107">In the **Navigation pane**, go to **Modules > Credit and collections > Setup > Customer posting profiles**.</span></span>
2. <span data-ttu-id="ecdf8-108">Klik på **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="ecdf8-108">Click **Edit**.</span></span>
3. <span data-ttu-id="ecdf8-109">Vælg en rentekode på rullelisten i feltet **Rentekode** i **oversigtspanelet Opsætning**.</span><span class="sxs-lookup"><span data-stu-id="ecdf8-109">In the **Setup fastTab**, in the **Interest code** field, select an interest code from the drop-down list.</span></span> <span data-ttu-id="ecdf8-110">Hvis du ikke vil have beregnet rente for transaktioner med denne posteringsprofil, skal du undlade at udfylde feltet.</span><span class="sxs-lookup"><span data-stu-id="ecdf8-110">If you do not want interest calculated for transactions using this posting profile, leave the field blank.</span></span> <span data-ttu-id="ecdf8-111">Under fanen **Tabelbegrænsninger** kan du ændre den måde, som renter behandles på.</span><span class="sxs-lookup"><span data-stu-id="ecdf8-111">The **Table restriction** fastTab allows you to change the way that interest is processed.</span></span> <span data-ttu-id="ecdf8-112">Hvis dette felt er indstillet til Ja, beregnes der rente for denne posteringsprofil.</span><span class="sxs-lookup"><span data-stu-id="ecdf8-112">If this field is set to Yes, then interest will be calculated for this posting profile.</span></span>  

## <a name="calculate-interest"></a><span data-ttu-id="ecdf8-113">Beregn renter</span><span class="sxs-lookup"><span data-stu-id="ecdf8-113">Calculate interest</span></span>
1. <span data-ttu-id="ecdf8-114">Gå i **Navigationsrude** til **Moduler > Kredit > Rente > Opret rentenotaer**.</span><span class="sxs-lookup"><span data-stu-id="ecdf8-114">In the **Navigation pane**, go to **Modules > Credit and collections > Interest > Create interest notes**.</span></span>
2. <span data-ttu-id="ecdf8-115">Du skal vælge de transaktionstyper, du vil beregne rente for.</span><span class="sxs-lookup"><span data-stu-id="ecdf8-115">You must select the transaction types for which you will calculate interest.</span></span> <span data-ttu-id="ecdf8-116">Alle åbne transaktioner for disse typer medtages i beregningen.</span><span class="sxs-lookup"><span data-stu-id="ecdf8-116">All of the open transactions for these types will be included in the calculation.</span></span>  
3. <span data-ttu-id="ecdf8-117">Hvis du vælger "Ja" i **Rente**, skal du beregne renters rente.</span><span class="sxs-lookup"><span data-stu-id="ecdf8-117">If you set **Interest** to 'Yes', you will calculate interest on interest.</span></span> <span data-ttu-id="ecdf8-118">Du bør kontrollere lovgivning vedrørende beregning af renters rente, før du inkluderer disse transaktioner.</span><span class="sxs-lookup"><span data-stu-id="ecdf8-118">You may want to check the laws governing the calculation of interest on interest before including these transactions.</span></span>  
4. <span data-ttu-id="ecdf8-119">Indtast en dato, som denne aftale skal beregnes fra, i feltet **Fra dato**.</span><span class="sxs-lookup"><span data-stu-id="ecdf8-119">In the **From date** field, enter a date from which the interest will be calculated.</span></span> <span data-ttu-id="ecdf8-120">Hvis du ikke angiver en **Fra dato**, annulleres alle ikke-bogførte rentenotaer, og rente genberegnes fra transaktionsdatoen.</span><span class="sxs-lookup"><span data-stu-id="ecdf8-120">If you do not specific a **From date**, then all unposted interest notes will be canceled and interest will be recalculated from the transaction date.</span></span>
5. <span data-ttu-id="ecdf8-121">Indtast en dato, som denne aftale skal beregnes til, i feltet **Til dato**.</span><span class="sxs-lookup"><span data-stu-id="ecdf8-121">In the **To date** field, enter a date to which the interest would be calculated.</span></span>
6. <span data-ttu-id="ecdf8-122">Vælg en indstilling i feltet **Anvend posteringsprofil fra**.</span><span class="sxs-lookup"><span data-stu-id="ecdf8-122">In the **Use posting profile from** field, select an option.</span></span> <span data-ttu-id="ecdf8-123">Der er tre indstillinger for posteringsprofiler:</span><span class="sxs-lookup"><span data-stu-id="ecdf8-123">There are three posting profile options:</span></span>
    - <span data-ttu-id="ecdf8-124">Konto – Brug den posteringsprofil, der er tildelt debitorens konto for hver rentenota.</span><span class="sxs-lookup"><span data-stu-id="ecdf8-124">Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span> 
    - <span data-ttu-id="ecdf8-125">Vælg – Brug den posteringsprofil, som du vælger i feltet Posteringsprofil.</span><span class="sxs-lookup"><span data-stu-id="ecdf8-125">Select – Use the posting profile that you select in the Posting profile field.</span></span>
    - <span data-ttu-id="ecdf8-126">Transaktion – Brug den individuelle posteringsprofil fra transaktioner, som der beregnes rente på for hver rentenota.</span><span class="sxs-lookup"><span data-stu-id="ecdf8-126">Transaction – Use the individual posting profile from transactions on which interest is calculated for each interest note.</span></span> <span data-ttu-id="ecdf8-127">For transaktioner, som ikke har en tildelt posteringsprofil, anvendes den posteringsprofil, der er angivet i området Finans og moms i formen Debitorparametre.</span><span class="sxs-lookup"><span data-stu-id="ecdf8-127">Transactions that do not have an assigned posting profile will use the posting profile that is specified in the Ledger and sales tax area of the Accounts receivable parameters form.</span></span>  
7. <span data-ttu-id="ecdf8-128">Udvid oversigtspanelet **Poster, der skal indgå**.</span><span class="sxs-lookup"><span data-stu-id="ecdf8-128">Expand the **Records to include** fastTab.</span></span>
8. <span data-ttu-id="ecdf8-129">Klik på **Filtrér**.</span><span class="sxs-lookup"><span data-stu-id="ecdf8-129">Click **Filter**.</span></span>
9. <span data-ttu-id="ecdf8-130">Angiv et debitor-id i feltet **Kriterier**.</span><span class="sxs-lookup"><span data-stu-id="ecdf8-130">In the **Criteria** field, enter a Customer ID.</span></span> <span data-ttu-id="ecdf8-131">Indtast for eksempel "US-001".</span><span class="sxs-lookup"><span data-stu-id="ecdf8-131">For example, enter 'US-001'.</span></span>
6. <span data-ttu-id="ecdf8-132">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="ecdf8-132">Click **OK**.</span></span>
7. <span data-ttu-id="ecdf8-133">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="ecdf8-133">Click **OK**.</span></span>

## <a name="print-interest-notes"></a><span data-ttu-id="ecdf8-134">Udskrivning af rentenotaer</span><span class="sxs-lookup"><span data-stu-id="ecdf8-134">Print interest notes</span></span>
1. <span data-ttu-id="ecdf8-135">Gå i **Navigationsrude** til **Moduler > Kredit > Rente > Gennemse og behandl rentenotaer**.</span><span class="sxs-lookup"><span data-stu-id="ecdf8-135">In the **Navigation pane**, go to **Modules > Credit and collections > Interest > Review and process interest notes**.</span></span>
2. <span data-ttu-id="ecdf8-136">Vælg "Oprettet" i feltet **Status**.</span><span class="sxs-lookup"><span data-stu-id="ecdf8-136">In the **Status** field, select 'Created'.</span></span>
3. <span data-ttu-id="ecdf8-137">Vælg "Ikke udskrevet" i feltet **Udskrevet**.</span><span class="sxs-lookup"><span data-stu-id="ecdf8-137">In the **Printed** field, select 'Not printed'.</span></span>
4. <span data-ttu-id="ecdf8-138">Klik på **Udskriv**.</span><span class="sxs-lookup"><span data-stu-id="ecdf8-138">Click **Print**.</span></span>
5. <span data-ttu-id="ecdf8-139">Udvid oversigtspanelet **Poster, der skal indgå**.</span><span class="sxs-lookup"><span data-stu-id="ecdf8-139">Expand the **Records to include** fastTab.</span></span>
6. <span data-ttu-id="ecdf8-140">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="ecdf8-140">Click **OK**.</span></span>
7. <span data-ttu-id="ecdf8-141">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ecdf8-141">Close the page.</span></span>

## <a name="post-the-interest-note"></a><span data-ttu-id="ecdf8-142">Bogfør rentenotaen</span><span class="sxs-lookup"><span data-stu-id="ecdf8-142">Post the interest note</span></span>
1. <span data-ttu-id="ecdf8-143">Vælg en rentenota, der er klar til at blive bogført (status er Oprettet).</span><span class="sxs-lookup"><span data-stu-id="ecdf8-143">Select an interest note that is ready to post (status is created).</span></span>
2. <span data-ttu-id="ecdf8-144">Klik på **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="ecdf8-144">Click **Post**.</span></span>
3. <span data-ttu-id="ecdf8-145">Angiv bogføringsdatoen for rentenotaen.</span><span class="sxs-lookup"><span data-stu-id="ecdf8-145">Enter the posting date for the interest note.</span></span> <span data-ttu-id="ecdf8-146">Vælg Ja for at oprette en transaktion i finansmodulet for hver enkelt rentenota.</span><span class="sxs-lookup"><span data-stu-id="ecdf8-146">Select Yes to create a general ledger transaction for each interest note.</span></span> <span data-ttu-id="ecdf8-147">Hvis du ikke vælger Ja, samles renten fra alle rentenotaer til debitoren, og den bogføres til finansmodulet i én transaktion.</span><span class="sxs-lookup"><span data-stu-id="ecdf8-147">If you do not select Yes, the interest on all interest notes to the customer is accumulated and posted to the general ledger in one transaction.</span></span>  
4. <span data-ttu-id="ecdf8-148">Udvid oversigtspanelet **Poster, der skal indgå**.</span><span class="sxs-lookup"><span data-stu-id="ecdf8-148">Expand the **Records to include** fastTab.</span></span>
5. <span data-ttu-id="ecdf8-149">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="ecdf8-149">Click **OK**.</span></span>
6. <span data-ttu-id="ecdf8-150">Vælg "Bogført" i feltet **Status**.</span><span class="sxs-lookup"><span data-stu-id="ecdf8-150">In the **Status** field, select 'Posted'.</span></span>

