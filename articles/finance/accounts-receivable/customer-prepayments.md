---
title: Forudbetalinger fra debitorer
description: Dette emne indeholder en forklaring på, hvordan du kan konfigurere og behandle forudbetalinger fra kunder (også kaldet kundeindbetalinger).
author: roschlom
ms.date: 04/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, LedgerJournalTransCustPaym, CustParameters
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: ''
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3314803b994aed40e5b04d8546a45bd305d48b6
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019414"
---
# <a name="customer-prepayments"></a><span data-ttu-id="09522-103">Forudbetalinger fra debitorer</span><span class="sxs-lookup"><span data-stu-id="09522-103">Customer prepayments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="09522-104">Forudbetalinger fra debitorer bruges, når du modtager en betaling fra en debitor, uden at der er en faktura, som betalingen kan udlignes mod.</span><span class="sxs-lookup"><span data-stu-id="09522-104">Customer prepayments are used when you receive a payment from a customer, but there is no invoice that the payment can be settled against.</span></span> <span data-ttu-id="09522-105">Disse typer betalinger kaldes også debitorindbetalinger.</span><span class="sxs-lookup"><span data-stu-id="09522-105">These types of payments are also referred to as customer deposits.</span></span>

<span data-ttu-id="09522-106">Processen til opsætning og arbejde med forudbetalinger fra kunder består af følgende grundlæggende trin.</span><span class="sxs-lookup"><span data-stu-id="09522-106">The process of setting up and working with customer prepayments consists of the following basic steps.</span></span>

1. <span data-ttu-id="09522-107">Opret en debitorposteringsprofil til forudbetalinger.</span><span class="sxs-lookup"><span data-stu-id="09522-107">Create a customer posting profile for prepayments.</span></span>
2. <span data-ttu-id="09522-108">Angiv parameteren **Posteringsprofil med kladdebilag for forudbetaling**.</span><span class="sxs-lookup"><span data-stu-id="09522-108">Set the **Posting profile with prepayment journal voucher** parameter.</span></span>
3. <span data-ttu-id="09522-109">Opret en debitorbetalingskladde, og marker afkrydsningsfeltet **Kladdebilag for forudbetaling** på hver linje.</span><span class="sxs-lookup"><span data-stu-id="09522-109">Create a customer payment journal, and select the **Prepayment journal voucher** check box on each line.</span></span>
4. <span data-ttu-id="09522-110">Bogfør debitorbetalingskladde.</span><span class="sxs-lookup"><span data-stu-id="09522-110">Post the customer payment journal.</span></span>
5. <span data-ttu-id="09522-111">Når en faktura er genereret, skal du udligne forudbetalingen på den ved hjælp af siden **Udlign åbne posteringer**.</span><span class="sxs-lookup"><span data-stu-id="09522-111">After an invoice is generated, settle the prepayment with it by using the **Settle open transactions** page.</span></span>

## <a name="create-a-customer-posting-profile-for-prepayments"></a><span data-ttu-id="09522-112">Oprette en debitorposteringsprofil til forudbetalinger</span><span class="sxs-lookup"><span data-stu-id="09522-112">Create a customer posting profile for prepayments</span></span>

<span data-ttu-id="09522-113">Når du accepterer forudbetalinger eller indbetalinger fra kunderne, inden varer eller tjenester leveres, eller før der findes en faktura i systemet, vil du typisk registrere kontanterne som et passiv i stedet for et aktiv i din kontoplan.</span><span class="sxs-lookup"><span data-stu-id="09522-113">Typically, when you accept prepayments or deposits from your customers before goods or services are delivered, or before an invoice exists in your system, you will want to record the cash as a liability instead of an asset in your chart of accounts.</span></span> <span data-ttu-id="09522-114">Kravene til registrering af disse beløb i finansmodulet kan dog være forskellige, afhængigt af dit land eller område.</span><span class="sxs-lookup"><span data-stu-id="09522-114">However, the requirements for recording these amounts in your general ledger might differ, depending on your country or region.</span></span> <span data-ttu-id="09522-115">Derfor skal du sørge for at kontakte en revisor vedrørende eventuelle lokale regler, der er gældende.</span><span class="sxs-lookup"><span data-stu-id="09522-115">Therefore, be sure to consult your accountants about any local regulations that apply.</span></span>

<span data-ttu-id="09522-116">Generelt er processen til oprettelse af en posteringsprofil, der kan bruges til forudbetalinger, den samme som processen til oprettelse af andre posteringsprofiler.</span><span class="sxs-lookup"><span data-stu-id="09522-116">In general, the process for creating a posting profile that can be used for prepayments is the same as the process for creating other posting profiles.</span></span> <span data-ttu-id="09522-117">Den primære forskel er den hovedkonto, du vælger i feltet **Samlekonto**.</span><span class="sxs-lookup"><span data-stu-id="09522-117">The primary difference is the main account that you select in the **Summary account** field.</span></span> <span data-ttu-id="09522-118">Du kan finde flere oplysninger i [Debitorposteringsprofiler](customer-posting-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="09522-118">For more information, see [Customer posting profiles](customer-posting-profiles.md).</span></span>

## <a name="define-parameters-for-customer-prepayments"></a><span data-ttu-id="09522-119">Definere parametre for debitorforudbetalinger</span><span class="sxs-lookup"><span data-stu-id="09522-119">Define parameters for customer prepayments</span></span>

<span data-ttu-id="09522-120">Der er to hovedparametre for debitorer, som du skal overveje, når du konfigurerer systemet til debitorforudbetalinger.</span><span class="sxs-lookup"><span data-stu-id="09522-120">There are two main Accounts receivable parameters that you must consider when you configure the system for customer prepayments.</span></span> <span data-ttu-id="09522-121">Følg disse trin for at konfigurere parametrene.</span><span class="sxs-lookup"><span data-stu-id="09522-121">Follow these steps to configure the parameters.</span></span>

1. <span data-ttu-id="09522-122">Gå til **Debitor \> Opsætning \> Debitorparametre**.</span><span class="sxs-lookup"><span data-stu-id="09522-122">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="09522-123">Valgfrit: Vælg **Ja** i **Moms for kladdebilag for forudbetalinger** i oversigtspanelet **Betaling** under fanen **Finans og moms**.</span><span class="sxs-lookup"><span data-stu-id="09522-123">Optional: On the **Ledger and sales tax** tab, on the **Payment** FastTab, set the **Sales tax on prepayment journal voucher** option to **Yes**.</span></span>
3. <span data-ttu-id="09522-124">Vælg den debitorposteringsprofil, der skal bruges til bogføring af forudbetalinger, i feltet **Posteringsprofil med kladdebilag for forudbetaling**.</span><span class="sxs-lookup"><span data-stu-id="09522-124">In the **Posting profile with prepayment journal voucher** field, select the customer posting profile to use when customer prepayments are posted.</span></span>
4. <span data-ttu-id="09522-125">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="09522-125">Close the page.</span></span>

## <a name="create-customer-prepayment-vouchers"></a><span data-ttu-id="09522-126">Oprette forudbetalingsbilag for debitorer</span><span class="sxs-lookup"><span data-stu-id="09522-126">Create customer prepayment vouchers</span></span>

<span data-ttu-id="09522-127">Når du opretter debitorbetalingskladden, skal du for hver forudbetaling vælge **Ja** i indstillingen **Kladdebilag for forudbetaling** på siden **Debitorbetalingskladde**.</span><span class="sxs-lookup"><span data-stu-id="09522-127">When you create the customer payment journal, for every prepayment, you must set the **Prepayment journal voucher** option to **Yes** on the **Customer payment journal** page.</span></span> <span data-ttu-id="09522-128">Følg disse trin for at oprette en debitorforudbetaling.</span><span class="sxs-lookup"><span data-stu-id="09522-128">Follow these steps to create a customer prepayment.</span></span>

1. <span data-ttu-id="09522-129">Gå til **Debitor \> Betalinger \> Debitorbetalingskladde**.</span><span class="sxs-lookup"><span data-stu-id="09522-129">Go to **Accounts receivable \> Payments \> Customer payment journal**.</span></span>
2. <span data-ttu-id="09522-130">Vælg **Ny** for at oprette en kladde.</span><span class="sxs-lookup"><span data-stu-id="09522-130">Select **New** to create a journal.</span></span>
3. <span data-ttu-id="09522-131">I feltet **Navn** skal du vælge det kladdenavn, der skal bruges.</span><span class="sxs-lookup"><span data-stu-id="09522-131">In the **Name** field, select the journal name to use.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="09522-132">Hvis du valgte **Ja** i indstillingen **Moms for kladdebilag for forudbetalinger** i den foregående procedure, skal du vælge et kladdenavn, hvor parameteren **Beløb er inklusive moms** er valgt.</span><span class="sxs-lookup"><span data-stu-id="09522-132">If you set the **Sales tax on prepayment journal voucher** option to **Yes** in the previous procedure, you must select a journal name where the **Amount includes sales tax** parameter is selected.</span></span> 

4. <span data-ttu-id="09522-133">Valgfrit: Angiv en detaljeret beskrivelse i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="09522-133">Optional: In the **Description** field, enter a detailed description.</span></span>
5. <span data-ttu-id="09522-134">Vælg **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="09522-134">Select **Lines**.</span></span>
6. <span data-ttu-id="09522-135">Hvis der ikke findes en tom linje, skal du vælge **Ny** for at oprette en linje.</span><span class="sxs-lookup"><span data-stu-id="09522-135">If a blank line doesn't exist, select **New** to create a line.</span></span>
7. <span data-ttu-id="09522-136">Angiv den dato, hvor forudbetalingen skal bogføres, i feltet **Dato**.</span><span class="sxs-lookup"><span data-stu-id="09522-136">In the **Date** field, enter the date when the prepayment should be posted.</span></span>
8. <span data-ttu-id="09522-137">Vælg kunden for forudbetalingen i feltet **Konto**.</span><span class="sxs-lookup"><span data-stu-id="09522-137">In the **Account** field, select the customer for the prepayment.</span></span>
9. <span data-ttu-id="09522-138">Valgfrit: Angiv en detaljeret beskrivelse af transaktionen i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="09522-138">Optional: In the **Description** field, enter a detailed description of the transaction.</span></span>
10. <span data-ttu-id="09522-139">Angiv forudbetalingsbeløbet i feltet **Kredit**.</span><span class="sxs-lookup"><span data-stu-id="09522-139">In the **Credit** field, enter the amount of the prepayment.</span></span>
11. <span data-ttu-id="09522-140">Vælg den konto, som betalingen skal modregnes mod, i feltet **Modkonto**.</span><span class="sxs-lookup"><span data-stu-id="09522-140">In the **Offset account** field, select the account to offset the payment to.</span></span> <span data-ttu-id="09522-141">Vælg f.eks. den bank- eller hovedkonto, betalingen skal bogføres på.</span><span class="sxs-lookup"><span data-stu-id="09522-141">For example, select the bank or main account to post the payment to.</span></span>
12. <span data-ttu-id="09522-142">Vælg kundens betalingsmåde i feltet **Betalingsmåde**.</span><span class="sxs-lookup"><span data-stu-id="09522-142">In the **Method of payment** field, select the customer's method of payment.</span></span>
13. <span data-ttu-id="09522-143">Vælg **Ja** i indstillingen **Kladdebilag for forudbetaling** under fanen **Betaling**.</span><span class="sxs-lookup"><span data-stu-id="09522-143">On the **Payment** tab, set the **Prepayment journal voucher** option to **Yes**.</span></span>
14. <span data-ttu-id="09522-144">Gentag trin 7 til 13 for hver ekstra forudbetaling, der skal bogføres.</span><span class="sxs-lookup"><span data-stu-id="09522-144">Repeat steps 7 through 13 for each additional prepayment that must be posted.</span></span>
15. <span data-ttu-id="09522-145">Vælg **Bogfør** for at afslutte kladden.</span><span class="sxs-lookup"><span data-stu-id="09522-145">Select **Post** to finalize the journal.</span></span>

## <a name="settle-prepayments-with-invoices"></a><span data-ttu-id="09522-146">Udligne forudbetalinger med fakturaer</span><span class="sxs-lookup"><span data-stu-id="09522-146">Settle prepayments with invoices</span></span>

<span data-ttu-id="09522-147">Du kan bruge arbejdsområdet **Debitorbetalinger** til nemt at finde og udligne betalinger, der ikke er fuldt udlignet.</span><span class="sxs-lookup"><span data-stu-id="09522-147">You can use the **Customer payments** workspace to easily find and settle payments that haven't been fully settled.</span></span>

1. <span data-ttu-id="09522-148">Vælg feltet **Debitorbetalinger** på dashboardet **Start**.</span><span class="sxs-lookup"><span data-stu-id="09522-148">On the **Home** dashboard, select the **Customer payments** tile.</span></span>
2. <span data-ttu-id="09522-149">Søg efter og vælg den betaling, der skal udlignes, under fanen **Betalinger, der ikke er udlignet** i sektionen **Debitorposter**.</span><span class="sxs-lookup"><span data-stu-id="09522-149">In the **Customer transactions** section, on the **Payments not settled** tab, search for and select the payment to settle.</span></span>
3. <span data-ttu-id="09522-150">Vælg **Udlign posteringer**.</span><span class="sxs-lookup"><span data-stu-id="09522-150">Select **Settle transactions**.</span></span>
4. <span data-ttu-id="09522-151">Marker afkrydsningsfeltet **Marker** for fakturaen og den betaling, der skal udlignes.</span><span class="sxs-lookup"><span data-stu-id="09522-151">Select the **Mark** check box for the invoice and the payment that will be settled.</span></span>
5. <span data-ttu-id="09522-152">Vælg **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="09522-152">Select **Post**.</span></span>

<span data-ttu-id="09522-153">Du kan finde flere oplysninger om, hvordan du udligner åbne posteringer, i [Udligningsoversigt](/cash-bank-management/settlement-overview.md).</span><span class="sxs-lookup"><span data-stu-id="09522-153">For more information about how to settle open transactions, see [Settlement overview](/cash-bank-management/settlement-overview.md).</span></span>
