---
title: Behandle rykkere
description: Denne procedure viser, hvordan du kan oprette, udskrive og bogføre rykkere.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 12/04/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 8a3f74d2891c050294e089eae14ba2386449d7c9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "358847"
---
# <a name="process-collection-letters"></a><span data-ttu-id="71fed-103">Behandle rykkere</span><span class="sxs-lookup"><span data-stu-id="71fed-103">Process collection letters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="71fed-104">Denne procedure viser, hvordan du kan oprette, udskrive og bogføre rykkere.</span><span class="sxs-lookup"><span data-stu-id="71fed-104">This procedure shows how to create, print, and post collection letters.</span></span> <span data-ttu-id="71fed-105">Denne opgave bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="71fed-105">This task uses the USMF demo company.</span></span>

## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a><span data-ttu-id="71fed-106">Konfigurere et rykkerforløb i en posteringsprofil</span><span class="sxs-lookup"><span data-stu-id="71fed-106">Set up a collection letter sequence on the posting profile</span></span>
1. <span data-ttu-id="71fed-107">Gå til **Kredit og inkasso > Opsætning > Debitorposteringsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="71fed-107">Go to **Credit and collections > Setup > Customer posting profiles**.</span></span>
2. <span data-ttu-id="71fed-108">Klik på **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="71fed-108">Click **Edit**.</span></span>
3. <span data-ttu-id="71fed-109">Vælg et rykkerforløb på rullelisten.</span><span class="sxs-lookup"><span data-stu-id="71fed-109">Select a collection letter sequence from the drop-down list.</span></span> <span data-ttu-id="71fed-110">Hvis du ikke vil oprette rykkere for transaktioner med denne posteringsprofil, skal du lade feltet være tomt.</span><span class="sxs-lookup"><span data-stu-id="71fed-110">If you do not want to generate collection letters for transactions using this posting profile, leave the field blank.</span></span>  
4. <span data-ttu-id="71fed-111">Udvid fanen Tabelbegrænsninger for at ændre den måde, som rykkere behandles på.</span><span class="sxs-lookup"><span data-stu-id="71fed-111">Expand the table restriction tab to change the way that collection letters are processed.</span></span> <span data-ttu-id="71fed-112">Hvis dette felt er indstillet til **Ja**, oprettes rykkerne for denne posteringsprofil.</span><span class="sxs-lookup"><span data-stu-id="71fed-112">If this field is set to **Yes**, then collection letters will be created for this posting profile.</span></span>  

## <a name="create-collection-letters"></a><span data-ttu-id="71fed-113">Opret rykkere</span><span class="sxs-lookup"><span data-stu-id="71fed-113">Create collection letters</span></span>
1. <span data-ttu-id="71fed-114">Gå til **Kredit og inkasso > Rykker > Opret rykkere**.</span><span class="sxs-lookup"><span data-stu-id="71fed-114">Go to **Credit and collections > Collection letter > Create collection letters**.</span></span>
2. <span data-ttu-id="71fed-115">Vælg de transaktionstyper, du vil rykke for.</span><span class="sxs-lookup"><span data-stu-id="71fed-115">Select the transaction types for which you will collect letters.</span></span> <span data-ttu-id="71fed-116">Alle åbne transaktioner for disse typer medtages i beregningen.</span><span class="sxs-lookup"><span data-stu-id="71fed-116">All of the open transactions for these types will be included in the calculation.</span></span>  
2. <span data-ttu-id="71fed-117">Vælg en indstilling i feltet **Rykker**.</span><span class="sxs-lookup"><span data-stu-id="71fed-117">In the **Collection letter** field, select an option.</span></span>
3. <span data-ttu-id="71fed-118">Angiv datoen for rykkeren.</span><span class="sxs-lookup"><span data-stu-id="71fed-118">Enter the date of the collection letter.</span></span>
4. <span data-ttu-id="71fed-119">Vælg en posteringsprofil, hvis du har ændret **Anvend posteringsprofil fra** til **Vælg**.</span><span class="sxs-lookup"><span data-stu-id="71fed-119">Select a posting profile if you changed **Use posting profile from** to **Select**.</span></span> <span data-ttu-id="71fed-120">Der er to indstillinger for posteringsprofiler:</span><span class="sxs-lookup"><span data-stu-id="71fed-120">There are two posting profile options:</span></span>   
   - <span data-ttu-id="71fed-121">**Konto** – Brug den posteringsprofil, der er tildelt debitorens konto for hver rentenota.</span><span class="sxs-lookup"><span data-stu-id="71fed-121">**Account** – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   
   - <span data-ttu-id="71fed-122">**Vælg** – Brug den posteringsprofil, som du vælger i feltet **Posteringsprofil**.</span><span class="sxs-lookup"><span data-stu-id="71fed-122">**Select** – Use the posting profile that you select in the **Posting profile** field.</span></span>  
5. <span data-ttu-id="71fed-123">Udvid sektionen **Poster, der skal indgå**.</span><span class="sxs-lookup"><span data-stu-id="71fed-123">Expand the **Records to include** section.</span></span>
6. <span data-ttu-id="71fed-124">Klik på **Filtrér**.</span><span class="sxs-lookup"><span data-stu-id="71fed-124">Click **Filter**.</span></span>
7. <span data-ttu-id="71fed-125">Angiv et debitor-id i feltet **Kriterier**.</span><span class="sxs-lookup"><span data-stu-id="71fed-125">In the **Criteria** field, enter a Customer ID.</span></span> <span data-ttu-id="71fed-126">Indtast for eksempel "US-001".</span><span class="sxs-lookup"><span data-stu-id="71fed-126">For example, enter 'US-001'.</span></span>
8. <span data-ttu-id="71fed-127">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="71fed-127">Click **OK**.</span></span>
9. <span data-ttu-id="71fed-128">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="71fed-128">Click **OK**.</span></span>

## <a name="print-collection-letters"></a><span data-ttu-id="71fed-129">Udskrive rykkere</span><span class="sxs-lookup"><span data-stu-id="71fed-129">Print collection letters</span></span>
1. <span data-ttu-id="71fed-130">Gå til **Kredit og inkasso > Rykker > Gennemse og behandl alle rykkere**.</span><span class="sxs-lookup"><span data-stu-id="71fed-130">Go to **Credit and collections > Collection letter > Review and process collection letters**.</span></span>
2. <span data-ttu-id="71fed-131">Vælg **Oprettet** i feltet **Status**.</span><span class="sxs-lookup"><span data-stu-id="71fed-131">In the **Status** field, select **Created**.</span></span>
3. <span data-ttu-id="71fed-132">Vælg **Ikke udskrevet** i feltet **Udskrevet**.</span><span class="sxs-lookup"><span data-stu-id="71fed-132">In the **Printed** field, select **Not printed**.</span></span>
4. <span data-ttu-id="71fed-133">Klik på **Udskriv**.</span><span class="sxs-lookup"><span data-stu-id="71fed-133">Click **Print**.</span></span>
5. <span data-ttu-id="71fed-134">Klik på **Rykkernota**.</span><span class="sxs-lookup"><span data-stu-id="71fed-134">Click **Collection letter note**.</span></span>
6. <span data-ttu-id="71fed-135">Udvid sektionen **Poster, der skal indgå**.</span><span class="sxs-lookup"><span data-stu-id="71fed-135">Expand the **Records to include** section.</span></span>
7. <span data-ttu-id="71fed-136">Angiv skæringsdatoen for bogføringer.</span><span class="sxs-lookup"><span data-stu-id="71fed-136">Enter the cutoff date for postings.</span></span>
8. <span data-ttu-id="71fed-137">Klik på **OK** for at udskrive rykkeren.</span><span class="sxs-lookup"><span data-stu-id="71fed-137">Click **OK** to print the collection letter.</span></span>
9. <span data-ttu-id="71fed-138">Bogfør rykkeren.</span><span class="sxs-lookup"><span data-stu-id="71fed-138">Post the collection letter.</span></span>
   1. <span data-ttu-id="71fed-139">Klik på **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="71fed-139">Click **Post**.</span></span>
   2. <span data-ttu-id="71fed-140">Angiv rykkerens bogføringsdato.</span><span class="sxs-lookup"><span data-stu-id="71fed-140">Enter the posting date for the collection letter.</span></span>
   3. <span data-ttu-id="71fed-141">Udvid sektionen **Poster, der skal indgå**.</span><span class="sxs-lookup"><span data-stu-id="71fed-141">Expand the **Records to include** section.</span></span>
   4. <span data-ttu-id="71fed-142">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="71fed-142">Click **OK**.</span></span>
   5. <span data-ttu-id="71fed-143">Vælg **Bogført** i feltet **Status**.</span><span class="sxs-lookup"><span data-stu-id="71fed-143">In the **Status** field, select **Posted**.</span></span>
   6. <span data-ttu-id="71fed-144">Vælg en indstilling i feltet **Udskrevet**.</span><span class="sxs-lookup"><span data-stu-id="71fed-144">In the **Printed** field, select an option.</span></span>

## <a name="control-collection-letters-at-the-customer-level"></a><span data-ttu-id="71fed-145">Styre rykkere på debitorniveau</span><span class="sxs-lookup"><span data-stu-id="71fed-145">Control collection letters at the customer level</span></span>
<span data-ttu-id="71fed-146">Du kan også konfigurere rykkere på debitorniveau, så rykkerkoden for hver postering spores, mens rykkerbehandlingen baseres på niveauet for den enkelte rykker, der er gemt for debitoren.</span><span class="sxs-lookup"><span data-stu-id="71fed-146">You can also set up collection letters at the customer level so that the collection letter code for each transaction is tracked, but the collection letter processing will be based on a single collection letter level that is stored for the customer.</span></span> <span data-ttu-id="71fed-147">Enkeltrykkeren indeholder alle posteringer, der er forfaldne for debitoren.</span><span class="sxs-lookup"><span data-stu-id="71fed-147">The single collection letter will contain all transactions that are overdue for the customer.</span></span> <span data-ttu-id="71fed-148">Da respitdagene nu spores på debitorniveau, bliver den næste rykker ikke sendt, før antallet af respitdage er overskredet for den næste rykker i rækkefølgen, selvom posteringer er forfaldne, efter at den sidste rykker blev sendt.</span><span class="sxs-lookup"><span data-stu-id="71fed-148">Because the grace days are now tracked on the customer level, the next collection letter will not be sent until the number of grace days has passed for the next collection letter in the sequence, even though transactions become overdue after the last collection letter was sent.</span></span> <span data-ttu-id="71fed-149">Denne indstilling reducerer det antal rykkere, du skal sende pr. debitor.</span><span class="sxs-lookup"><span data-stu-id="71fed-149">This option reduces the number of collection letters you will send per customer.</span></span> 

### <a name="set-up-the-customer-to-control-collection-letters-at-the-customer-level"></a><span data-ttu-id="71fed-150">Konfigurere debitor for at styre rykkere på debitorniveau</span><span class="sxs-lookup"><span data-stu-id="71fed-150">Set up the customer to control collection letters at the customer level</span></span>
1.  <span data-ttu-id="71fed-151">Gå til **Kredit > Opsætning > Debitorparametre**, og klik på fanen **Rykkere**.</span><span class="sxs-lookup"><span data-stu-id="71fed-151">Go to **Credit and collections > Setup > Accounts receivable parameters** and click the **Collections** tab.</span></span> 
2.  <span data-ttu-id="71fed-152">Rediger værdien i **Opret rykker pr.** til **Debitor**.</span><span class="sxs-lookup"><span data-stu-id="71fed-152">Change the value of **Create collection letter per** to **Customer**.</span></span> 
3.  <span data-ttu-id="71fed-153">Gå til **Kredit og inkasso > Rykker > Gennemse og behandl alle rykkere**.</span><span class="sxs-lookup"><span data-stu-id="71fed-153">Go to **Credit and collections > Collection letter > Review and process collection letters**.</span></span> <span data-ttu-id="71fed-154">Der genereres kun én rykker for en debitors samlede forfaldne posteringer.</span><span class="sxs-lookup"><span data-stu-id="71fed-154">Only one collection letter will be generated for a customer with all the overdue transactions.</span></span>

## <a name="ignore-payments-and-credit-memos-when-calculating-the-collection-letter-code"></a><span data-ttu-id="71fed-155">Ignorere betalinger og kreditnotaer ved beregning af rykkerkoden</span><span class="sxs-lookup"><span data-stu-id="71fed-155">Ignore payments and credit memos when calculating the collection letter code</span></span>
<span data-ttu-id="71fed-156">Hvis du medtager betalinger og kreditnotaer i de posteringer, der skal medtages i rykkerne, har du muligvis betalinger eller kreditnotaer, der udløser en rykker.</span><span class="sxs-lookup"><span data-stu-id="71fed-156">If you include payments and credit memos in the transactions that will be included in the collection letters, you may have payments or credit memos that will trigger a collection letter.</span></span> <span data-ttu-id="71fed-157">Du kan styre, hvordan betalinger og kreditnotaer styrer rykkerkoden ved at ændre værdien af parameteren **Ignorere betalinger og kreditnotaer ved beregning af rykkerkoden**.</span><span class="sxs-lookup"><span data-stu-id="71fed-157">You can control how payments and credit memos control the collection letter code by changing the value of the **Ignore payments and credit memos when calculating the collection letter code** parameter.</span></span> 

<span data-ttu-id="71fed-158">Gør følgende for at ignorere betalinger og kreditnotaer ved beregning af rykkerkoden.</span><span class="sxs-lookup"><span data-stu-id="71fed-158">To ignore payments and credit memos when calculating the collection letter code, do the following.</span></span>
1. <span data-ttu-id="71fed-159">Gå til **Kredit > Opsætning > Debitorparametre**, og klik på fanen **Rykkere**.</span><span class="sxs-lookup"><span data-stu-id="71fed-159">Go to **Credit and collections > Setup > Accounts receivable parameters** and click the **Collections** tab.</span></span> 
2. <span data-ttu-id="71fed-160">Vælg **Ja** for **Ignorere betalinger og kreditnotaer ved beregning af rykkerkoden**.</span><span class="sxs-lookup"><span data-stu-id="71fed-160">Change the value of **Ignore payments and credit memos when calculating the collection letter code** to **Yes**.</span></span>
