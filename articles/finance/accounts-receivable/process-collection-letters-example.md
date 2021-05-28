---
title: Behandle eksempel på rykkere
description: I dette emne gennemgås et eksempel, der viser processen til oprettelse, udskrivning og bogføring af rykkere.
author: JodiChristiansen
ms.date: 02/03/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: fb2651644efd2cadfccb91e48c34dfddc8383e1f
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021410"
---
# <a name="process-collection-letters-example"></a><span data-ttu-id="142ac-103">Behandle eksempel på rykkere</span><span class="sxs-lookup"><span data-stu-id="142ac-103">Process collection letters example</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="142ac-104">I dette emne gennemgås et eksempel, der viser processen til oprettelse, udskrivning og bogføring af rykkere.</span><span class="sxs-lookup"><span data-stu-id="142ac-104">This topic goes through an example that shows the process of creating, printing, and posting collection letters.</span></span> <span data-ttu-id="142ac-105">Eksemplet er baseret på **Ignorer betalinger og kreditnotaer ved beregning af indstillingen for rykkerkode** i Kredit og rykkere.</span><span class="sxs-lookup"><span data-stu-id="142ac-105">The example is based on the **Ignore payments and credit memos when calculating collection letter code** option in Credit and collections.</span></span> <span data-ttu-id="142ac-106">Det bruger data i USMF-demofirmaet og en ny kunde, US-045.</span><span class="sxs-lookup"><span data-stu-id="142ac-106">It uses data in the USMF demo company and a new customer, US-045.</span></span>

<span data-ttu-id="142ac-107">Når du vil starte, skal du gå til **Debitor \> Kunder \> Alle kunder**, vælge **Ny**, og derefter angive de nødvendige oplysninger for at oprette kunde US-045.</span><span class="sxs-lookup"><span data-stu-id="142ac-107">To begin, go to **Accounts receivable \> Customers \> All customers**, select **New**, and then enter the required information to create customer US-045.</span></span>

<span data-ttu-id="142ac-108">Når du er færdig, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="142ac-108">When you've finished, follow these steps.</span></span>

1. <span data-ttu-id="142ac-109">Gå til **Kredit og rykkere \> Rykker \> Konfigurer rykkerforløb**, og konfigurer rykkersekvensen, som vist i følgende tabel, som er tildelt debitorens posteringsprofil.</span><span class="sxs-lookup"><span data-stu-id="142ac-109">Go to **Credit and collections \> Collection letter \> Setup collection letter sequence**, and set up the collection letter sequence as shown in the following table that is assigned to the customer posting profile.</span></span>

|     <span data-ttu-id="142ac-110">Rykkerkode</span><span class="sxs-lookup"><span data-stu-id="142ac-110">Collection   letter code</span></span>      |     <span data-ttu-id="142ac-111">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="142ac-111">Description</span></span>                           |     <span data-ttu-id="142ac-112">Valuta</span><span class="sxs-lookup"><span data-stu-id="142ac-112">Currency</span></span>      |     <span data-ttu-id="142ac-113">Hovedkonto</span><span class="sxs-lookup"><span data-stu-id="142ac-113">Main   account</span></span>        |     <span data-ttu-id="142ac-114">Gebyr i valuta</span><span class="sxs-lookup"><span data-stu-id="142ac-114">Fee   in currency</span></span>     |     <span data-ttu-id="142ac-115">Minimum for over</span><span class="sxs-lookup"><span data-stu-id="142ac-115">Minimum   over</span></span>        |     <span data-ttu-id="142ac-116">Antal dage</span><span class="sxs-lookup"><span data-stu-id="142ac-116">Days   Block</span></span>      |
|---------------------------------  |---------------------------------------    |-----------------  |-----------------------    |-------------------------- |-----------------------    |---------------------  |
|     <span data-ttu-id="142ac-117">Rykker 1</span><span class="sxs-lookup"><span data-stu-id="142ac-117">Collection   letter 1</span></span>         |     <span data-ttu-id="142ac-118">Anden besked med gebyr</span><span class="sxs-lookup"><span data-stu-id="142ac-118">Second   notification with fee</span></span>        |     <span data-ttu-id="142ac-119">USD</span><span class="sxs-lookup"><span data-stu-id="142ac-119">USD</span></span>           |                           |     <span data-ttu-id="142ac-120">0,00</span><span class="sxs-lookup"><span data-stu-id="142ac-120">0.00</span></span>                  |     <span data-ttu-id="142ac-121">0,00</span><span class="sxs-lookup"><span data-stu-id="142ac-121">0.00</span></span>                  |     <span data-ttu-id="142ac-122">2</span><span class="sxs-lookup"><span data-stu-id="142ac-122">2</span></span>                 |
|     <span data-ttu-id="142ac-123">Rykker 2</span><span class="sxs-lookup"><span data-stu-id="142ac-123">Collection   letter 2</span></span>         |     <span data-ttu-id="142ac-124">Anden besked med gebyr</span><span class="sxs-lookup"><span data-stu-id="142ac-124">Second   notification with fee</span></span>        |     <span data-ttu-id="142ac-125">USC</span><span class="sxs-lookup"><span data-stu-id="142ac-125">USC</span></span>           |     <span data-ttu-id="142ac-126">403150</span><span class="sxs-lookup"><span data-stu-id="142ac-126">403150</span></span>                |     <span data-ttu-id="142ac-127">20.00</span><span class="sxs-lookup"><span data-stu-id="142ac-127">20.00</span></span>                 |     <span data-ttu-id="142ac-128">10.00</span><span class="sxs-lookup"><span data-stu-id="142ac-128">10.00</span></span>                 |     <span data-ttu-id="142ac-129">3</span><span class="sxs-lookup"><span data-stu-id="142ac-129">3</span></span>                 |
|     <span data-ttu-id="142ac-130">Incasso</span><span class="sxs-lookup"><span data-stu-id="142ac-130">Collection</span></span>                    |     <span data-ttu-id="142ac-131">Sidste besked med gebyr</span><span class="sxs-lookup"><span data-stu-id="142ac-131">Final   notification with fee</span></span>         |     <span data-ttu-id="142ac-132">USD</span><span class="sxs-lookup"><span data-stu-id="142ac-132">USD</span></span>           |     <span data-ttu-id="142ac-133">403150</span><span class="sxs-lookup"><span data-stu-id="142ac-133">403150</span></span>                |     <span data-ttu-id="142ac-134">50.00</span><span class="sxs-lookup"><span data-stu-id="142ac-134">50.00</span></span>                 |     <span data-ttu-id="142ac-135">100.00</span><span class="sxs-lookup"><span data-stu-id="142ac-135">100.00</span></span>                |     <span data-ttu-id="142ac-136">15</span><span class="sxs-lookup"><span data-stu-id="142ac-136">15</span></span>                |

<span data-ttu-id="142ac-137">I følgende illustration vises de oplysninger, der vises i tabellen, som de vises på siden **Rykkere**.</span><span class="sxs-lookup"><span data-stu-id="142ac-137">The following illustration shows the information that's in the table as it would appear on the **Collection letters** page.</span></span> 

<span data-ttu-id="142ac-138">[![Konfigurere et rykkerforløb](./media/Ignore-payments-creditmemos-1.PNG)](./media/Ignore-payments-creditmemos-1.PNG)</span><span class="sxs-lookup"><span data-stu-id="142ac-138">[![Setting up a collection letter sequence](./media/Ignore-payments-creditmemos-1.PNG)](./media/Ignore-payments-creditmemos-1.PNG)</span></span>

 <span data-ttu-id="142ac-139">Du skal nu angive de to parametre, der skal bruges til dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="142ac-139">You must now set the two parameters that are required for this example.</span></span>

2. <span data-ttu-id="142ac-140">Gå til **Kredit og rykkere \> Opsætning \> Debitorparametre**, og følg disse trin.</span><span class="sxs-lookup"><span data-stu-id="142ac-140">Go to **Credit and collections \> Setup \> Accounts receivable parameters**, and follow these steps:</span></span>

    1. <span data-ttu-id="142ac-141">På fanen **Rykkere** skal du indstille **Ignorer betalinger og kreditnotaer ved beregning af indstillingen for rykkerkode** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="142ac-141">On the **Collections** tab, set the **Ignore payments and credit memos when calculating collection letter code** option to **Yes**.</span></span>
    2. <span data-ttu-id="142ac-142">Kontroller, at feltet **Opret rykker** pr. felt er angivet til **Debitor**.</span><span class="sxs-lookup"><span data-stu-id="142ac-142">Make sure that the **Create collection letter per** field is set to **Customer**.</span></span>

    <span data-ttu-id="142ac-143">[![Angive debitorparametre for kreditrykkere](./media/Ignore-payments-creditmemos-2.PNG)](./media/Ignore-payments-creditmemos-2.PNG)</span><span class="sxs-lookup"><span data-stu-id="142ac-143">[![Setting Accounts receivable parameters for Credit collections](./media/Ignore-payments-creditmemos-2.PNG)](./media/Ignore-payments-creditmemos-2.PNG)</span></span>

3. <span data-ttu-id="142ac-144">Gå til **Debitor \> Fakturaer \> Alle fritekstfakturaer**, vælg **Ny**, og følg derefter disse trin:</span><span class="sxs-lookup"><span data-stu-id="142ac-144">Go to **Accounts receivable \> Invoices \> All free text invoices**, select **New**, and then follow these steps:</span></span>

    1. <span data-ttu-id="142ac-145">Vælg **US-045** i feltet **Debitorkonto**.</span><span class="sxs-lookup"><span data-stu-id="142ac-145">In the **Customer account** field select **US-045**.</span></span>
    2. <span data-ttu-id="142ac-146">I feltet **Fakturadato** angives **1/15/2021**.</span><span class="sxs-lookup"><span data-stu-id="142ac-146">In the **Invoice date** field, enter **1/15/2021**.</span></span>
    3. <span data-ttu-id="142ac-147">I feltet **Forfaldsdato** angives **1/16/2021**.</span><span class="sxs-lookup"><span data-stu-id="142ac-147">In the **Due date** field, enter **1/16/2021**.</span></span>
    4. <span data-ttu-id="142ac-148">På oversigtspanelet **Fakturalinjer** i feltet **Hovedkonto** skal du skrive **401100**.</span><span class="sxs-lookup"><span data-stu-id="142ac-148">On the **Invoice lines** FastTab, in the **Main account** field, enter **401100**.</span></span>
    5. <span data-ttu-id="142ac-149">Indtast **500.00** i feltet **Enhedspris**.</span><span class="sxs-lookup"><span data-stu-id="142ac-149">In the **Unit price** field, enter **500.00**.</span></span>
    6. <span data-ttu-id="142ac-150">Vælg **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="142ac-150">Select **Post**.</span></span>

    <span data-ttu-id="142ac-151">Du skal nu indtaste to kreditnotaer for kunden.</span><span class="sxs-lookup"><span data-stu-id="142ac-151">You must now enter two credit notes for the customer.</span></span>

4. <span data-ttu-id="142ac-152">Vælg **Ny**, og følg derefter følgende fremgangsmåde:</span><span class="sxs-lookup"><span data-stu-id="142ac-152">Select **New**, and then follow these steps:</span></span>

    1. <span data-ttu-id="142ac-153">Vælg **US-045** i feltet **Debitorkonto**.</span><span class="sxs-lookup"><span data-stu-id="142ac-153">In the **Customer account** field, select **US-045**.</span></span>
    2. <span data-ttu-id="142ac-154">I feltet **Fakturadato** angives **1/15/2021**.</span><span class="sxs-lookup"><span data-stu-id="142ac-154">In the **Invoice date** field, enter **1/15/2021**.</span></span>
    3. <span data-ttu-id="142ac-155">I feltet **Forfaldsdato** angives **1/16/2021**.</span><span class="sxs-lookup"><span data-stu-id="142ac-155">In the **Due date** field, enter **1/16/2021**.</span></span>
    4. <span data-ttu-id="142ac-156">På oversigtspanelet **Fakturalinjer** i feltet **Hovedkonto** skal du skrive **401100**.</span><span class="sxs-lookup"><span data-stu-id="142ac-156">On the **Invoice lines** FastTab, in the **Main account** field, enter **401100**.</span></span>
    5. <span data-ttu-id="142ac-157">I feltet **Enhedspris** skal du indtaste **-100.00**.</span><span class="sxs-lookup"><span data-stu-id="142ac-157">In the **Unit price** field, enter **-100.00**.</span></span>
    6. <span data-ttu-id="142ac-158">Vælg **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="142ac-158">Select **Post**.</span></span>

5. <span data-ttu-id="142ac-159">Gentag trin 4, men skriv **-200,00** i feltet **Enhedspris**.</span><span class="sxs-lookup"><span data-stu-id="142ac-159">Repeat step 4, but enter **-200.00** in the **Unit price** field.</span></span>
6. <span data-ttu-id="142ac-160">Gå til **Debitor \> Debitorer \> Alle debitorer**, og vælg debitor **US-045**.</span><span class="sxs-lookup"><span data-stu-id="142ac-160">Go to **Accounts receivable \> Customers \> All customers**, and select customer **US-045**.</span></span> <span data-ttu-id="142ac-161">Vælg derefter i handlingsruden **Transaktioner \> Transaktioner** for at gennemse de debitorposteringer, du har bogført tidligere.</span><span class="sxs-lookup"><span data-stu-id="142ac-161">Then, on the Action Pane, select **Transactions \> Transactions** to review the customer transactions that you posted earlier.</span></span>

    <span data-ttu-id="142ac-162">[![Gennemgå de bogførte debitorposteringer](./media/Ignore-payments-creditmemos-3.PNG)](./media/Ignore-payments-creditmemos-3.PNG)</span><span class="sxs-lookup"><span data-stu-id="142ac-162">[![Reviewing the posted customer transactions](./media/Ignore-payments-creditmemos-3.PNG)](./media/Ignore-payments-creditmemos-3.PNG)</span></span>

    <span data-ttu-id="142ac-163">Du skal nu oprette rykkere til debitor US-045.</span><span class="sxs-lookup"><span data-stu-id="142ac-163">You must now create collection letters for customer US-045.</span></span>

7. <span data-ttu-id="142ac-164">Gå til **Kredit og rykkere \> Rykker \> Opret rykkere**, og følg disse trin.</span><span class="sxs-lookup"><span data-stu-id="142ac-164">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="142ac-165">Angiv indstillingerne for **faktura** og **Kreditnota** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="142ac-165">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="142ac-166">Som standard skal feltet **Rykker** angives til **Rykker pr. debitor**.</span><span class="sxs-lookup"><span data-stu-id="142ac-166">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="142ac-167">I feltet **Fakturadato** angives **1/19/2021**.</span><span class="sxs-lookup"><span data-stu-id="142ac-167">In the **Collection letter date** field, enter **1/19/2021**.</span></span>
    3. <span data-ttu-id="142ac-168">I oversigtsfeltet **Poster, der skal indgå** skal du vælge **Filter** og derefter i feltet **Kundekonto** skal du tilføje **US-045**.</span><span class="sxs-lookup"><span data-stu-id="142ac-168">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="142ac-169">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="142ac-169">Select **OK**.</span></span>
    5. <span data-ttu-id="142ac-170">Vælg **OK** for at oprette rykkere.</span><span class="sxs-lookup"><span data-stu-id="142ac-170">Select **OK** to create collection letters.</span></span>

8. <span data-ttu-id="142ac-171">Gå til **Kredit og rykkere \> Rykker \> Gennemse og behandle rykkere**, og følg disse trin.</span><span class="sxs-lookup"><span data-stu-id="142ac-171">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="142ac-172">Bemærk, at rykkerkoden både på hoved- og posteringslinjerne er **Rykker 1**, da denne rykker er den første rykker i sekvensen.</span><span class="sxs-lookup"><span data-stu-id="142ac-172">Notice that the collection letter code on both the header and the transaction lines is **Collection letter 1**, because this collection letter is the first collection letter in the sequence.</span></span> <span data-ttu-id="142ac-173">(Hvis du vil have vist posteringslinjerne, kan du være nødt til at vælge oversigtspanelet **Posteringer**.)</span><span class="sxs-lookup"><span data-stu-id="142ac-173">(To view the transaction lines, you might have to select the **Transactions** FastTab.)</span></span>

   <span data-ttu-id="142ac-174">[![Kontrollere, at den samme rykkerkode vises i hovedet og linjerne](./media/Ignore-payments-creditmemos-4.PNG)](./media/Ignore-payments-creditmemos-4.PNG)</span><span class="sxs-lookup"><span data-stu-id="142ac-174">[![Verifying that the same collection letter code appears on the header and the lines](./media/Ignore-payments-creditmemos-4.PNG)](./media/Ignore-payments-creditmemos-4.PNG)</span></span>

    2. <span data-ttu-id="142ac-175">Vælg **Bogfør** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="142ac-175">On the Action Pane, select **Post**.</span></span>
    3. <span data-ttu-id="142ac-176">I feltet **Bogføringsdato** angives **1/19/2021**.</span><span class="sxs-lookup"><span data-stu-id="142ac-176">In the **Posting date** field, enter **1/19/2021**.</span></span>

    <span data-ttu-id="142ac-177">Du skal nu oprette rykkere igen til debitor US-045.</span><span class="sxs-lookup"><span data-stu-id="142ac-177">You must now create collection letters again for customer US-045.</span></span>

9. <span data-ttu-id="142ac-178">Gå til **Kredit og rykkere \> Rykker \> Opret rykkere**, og følg disse trin.</span><span class="sxs-lookup"><span data-stu-id="142ac-178">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="142ac-179">Angiv indstillingerne for **faktura** og **Kreditnota** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="142ac-179">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="142ac-180">Som standard skal feltet **Rykker** angives til **Rykker pr. debitor**.</span><span class="sxs-lookup"><span data-stu-id="142ac-180">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="142ac-181">I feltet **Fakturadato** angives **1/23/2021**.</span><span class="sxs-lookup"><span data-stu-id="142ac-181">In the **Collection letter date** field, enter **1/23/2021**.</span></span>
    3. <span data-ttu-id="142ac-182">I oversigtsfeltet **Poster, der skal indgå** skal du vælge **Filter** og derefter i feltet **Kundekonto** skal du tilføje **US-045**.</span><span class="sxs-lookup"><span data-stu-id="142ac-182">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="142ac-183">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="142ac-183">Select **OK**.</span></span>
    5. <span data-ttu-id="142ac-184">Vælg **OK** for at oprette rykkere.</span><span class="sxs-lookup"><span data-stu-id="142ac-184">Select **OK** to create collection letters.</span></span>

10. <span data-ttu-id="142ac-185">Gå til **Kredit og rykkere \> Rykker \> Gennemse og behandle rykkere**, og følg disse trin.</span><span class="sxs-lookup"><span data-stu-id="142ac-185">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="142ac-186">Bemærk, at rykkerkoden i hovedet er **Rykker 1**.</span><span class="sxs-lookup"><span data-stu-id="142ac-186">Notice that the collection letter code on the header is **Collection letter 1**.</span></span> <span data-ttu-id="142ac-187">Koden på posteringslinjerne er **Rykker 2**.</span><span class="sxs-lookup"><span data-stu-id="142ac-187">However, the code on the transaction lines is **Collection letter 2**.</span></span>

   <span data-ttu-id="142ac-188">[![Kontrollere, at forskellige rykkerkoder vises i hovedet og linjerne](./media/Ignore-payments-creditmemos-5.PNG)](./media/Ignore-payments-creditmemos-5.PNG)</span><span class="sxs-lookup"><span data-stu-id="142ac-188">[![Verifies that different collection letter codes appear on the header and the lines](./media/Ignore-payments-creditmemos-5.PNG)](./media/Ignore-payments-creditmemos-5.PNG)</span></span>

  <span data-ttu-id="142ac-189">Koden er anderledes, fordi **Ignorer betalinger og kreditnotaer ved beregning af indstillingen for rykkerkode** er angivet til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="142ac-189">The codes differ because the **Ignore payments and credit memos when calculating collection letter code** option is to **Yes**.</span></span>

  2. <span data-ttu-id="142ac-190">Bogfør ikke rykkeren.</span><span class="sxs-lookup"><span data-stu-id="142ac-190">Don't post this collection letter.</span></span>

11. <span data-ttu-id="142ac-191">Gå til **Kredit og rykkere \> Opsætning \> Parametre for debitorer**, og på fanen **Rykkere** skal du angive indstillingen **Ignorer betalinger og kreditnotaer ved beregning af indstillingen for rykkerkode** til **Nej**.</span><span class="sxs-lookup"><span data-stu-id="142ac-191">Go to **Credit and collections \> Setup \> Accounts receivable parameters**, and then, on the **Collections** tab, set the **Ignore payments and credit memos when calculating collection letter code** option to **No**.</span></span>

    <span data-ttu-id="142ac-192">[![Konfigurere Ignorer betalinger og kreditnotaer ved beregning af indstillingen for rykkerkode](./media/Ignore-payments-creditmemos-6.PNG)](./media/Ignore-payments-creditmemos-6.PNG)</span><span class="sxs-lookup"><span data-stu-id="142ac-192">[![Setting the Ignore payments and credit memos when calculating collection letter code option to No](./media/Ignore-payments-creditmemos-6.PNG)](./media/Ignore-payments-creditmemos-6.PNG)</span></span>

    <span data-ttu-id="142ac-193">Du skal nu oprette rykkere igen til debitor US-045.</span><span class="sxs-lookup"><span data-stu-id="142ac-193">You must now create collection letters again for customer US-045.</span></span>

12. <span data-ttu-id="142ac-194">Gå til **Kredit og rykkere \> Rykker \> Opret rykkere**, og følg disse trin.</span><span class="sxs-lookup"><span data-stu-id="142ac-194">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="142ac-195">Angiv indstillingerne for **faktura** og **Kreditnota** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="142ac-195">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="142ac-196">Som standard skal feltet **Rykker** angives til **Rykker pr. debitor**.</span><span class="sxs-lookup"><span data-stu-id="142ac-196">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="142ac-197">I feltet **Fakturadato** angives **1/23/2021**.</span><span class="sxs-lookup"><span data-stu-id="142ac-197">In the **Collection letter date** field, enter **1/23/2021**.</span></span>
    3. <span data-ttu-id="142ac-198">I oversigtsfeltet **Poster, der skal indgå** skal du vælge **Filter** og derefter i feltet **Kundekonto** skal du tilføje **US-045**.</span><span class="sxs-lookup"><span data-stu-id="142ac-198">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="142ac-199">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="142ac-199">Select **OK**.</span></span>
    5. <span data-ttu-id="142ac-200">Vælg **OK** for at oprette rykkere.</span><span class="sxs-lookup"><span data-stu-id="142ac-200">Select **OK** to create collection letters.</span></span>

13. <span data-ttu-id="142ac-201">Gå til **Kredit og rykkere \> Rykker \> Gennemse og behandle rykkere**, og bemærk at rykkerkoden på både hovedet og i transaktionslinjerne er **Rykker 2**.</span><span class="sxs-lookup"><span data-stu-id="142ac-201">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and notice that the collection letter code on both the header and the transaction lines is **Collection letter 2**.</span></span>

    <span data-ttu-id="142ac-202">[![Vise igen, at den samme rykkerkode vises i hovedet og linjerne](./media/Ignore-payments-creditmemos-7.PNG)](./media/Ignore-payments-creditmemos-7.PNG)</span><span class="sxs-lookup"><span data-stu-id="142ac-202">[![Showing again that the same collection letter code appears on the header and the lines](./media/Ignore-payments-creditmemos-7.PNG)](./media/Ignore-payments-creditmemos-7.PNG)</span></span>

    <span data-ttu-id="142ac-203">Den samme kode vises begge steder, fordi **Ignorer betalinger og kreditnotaer ved beregning af indstillingen for rykkerkode** nu er angivet til **Nej**.</span><span class="sxs-lookup"><span data-stu-id="142ac-203">The same code appears in both places because the **Ignore payments and credit memos when calculating collection letter code** option is now set to **No**.</span></span>
