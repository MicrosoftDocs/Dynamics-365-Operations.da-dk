---
title: Oprette en ny bemyndigelse til direkte debitering til en debitor
description: Denne opgaveguide viser, hvordan du kan oprette en bemyndigelse til direkte debitering og bruge den til en faktura.
author: ShivamPandey-msft
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, BankAccountTable, CustPaymMode, CustDirectDebitMandate, BankAccountTableLookUp, SrsReportViewerForm,  LogisticsAddressCityLookup, CustFreeInvoice, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e3bbf3703941255dfd82b8fb501ba8a9d1f3a2ec
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835070"
---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a><span data-ttu-id="d4a1b-103">Oprette en ny bemyndigelse til direkte debitering til en debitor</span><span class="sxs-lookup"><span data-stu-id="d4a1b-103">Create a direct debit mandate for a customer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d4a1b-104">Denne opgaveguide viser, hvordan du kan oprette en bemyndigelse til direkte debitering og bruge den til en faktura.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-104">This task guide demonstrates how to create a direct debit mandate and use it on an invoice.</span></span>


## <a name="create-a-bank-account"></a><span data-ttu-id="d4a1b-105">Opret en bankkonto</span><span class="sxs-lookup"><span data-stu-id="d4a1b-105">Create a bank account</span></span>
1. <span data-ttu-id="d4a1b-106">I **navigationsruden** skal du gå til **Moduler > Debitor > Debitorer > Alle kunder**.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-106">In the **Navigation pane**, go to **Modules > Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="d4a1b-107">Vælg en post på listen.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-107">In the list, select a record.</span></span> <span data-ttu-id="d4a1b-108">Vælg f.eks. US-001</span><span class="sxs-lookup"><span data-stu-id="d4a1b-108">For example, select US-001</span></span>
3. <span data-ttu-id="d4a1b-109">Klik på **Debitor** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-109">On the Action Pane, click **Customer**.</span></span>
4. <span data-ttu-id="d4a1b-110">Klik på **Bankkonti**.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-110">Click **Bank accounts**.</span></span>
5. <span data-ttu-id="d4a1b-111">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-111">Click **New**.</span></span>
6. <span data-ttu-id="d4a1b-112">Skriv en værdi i feltet **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-112">In the **Bank account** field, type a value.</span></span>
7. <span data-ttu-id="d4a1b-113">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-113">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="d4a1b-114">Skriv en værdi i feltet **IBAN**.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-114">In the **IBAN** field, type a value.</span></span>
9. <span data-ttu-id="d4a1b-115">Skriv en værdi i feltet **Valuta**.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-115">In the **Currency** field, type a value.</span></span>
10. <span data-ttu-id="d4a1b-116">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-116">Click **Save**.</span></span>
11. <span data-ttu-id="d4a1b-117">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-117">Close the page.</span></span>
12. <span data-ttu-id="d4a1b-118">Gå i **navigationsruden** til **Moduler > Kontant- og bankstyring > Bankkonti > Bankkonti**.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-118">In the **Navigation pane**, go to **Modules > Cash and bank management > Bank accounts > Bank accounts**.</span></span>
13. <span data-ttu-id="d4a1b-119">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-119">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="d4a1b-120">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-120">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="d4a1b-121">Klik på **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-121">Click **Edit**.</span></span>
16. <span data-ttu-id="d4a1b-122">Udvid oversigtspanelet **Yderligere identifikation**.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-122">Expand the **Additional identification** fastTab.</span></span>
17. <span data-ttu-id="d4a1b-123">Skriv en værdi i feltet **Direct Debit-id**.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-123">In the **Direct debit ID** field, type a value.</span></span>
18. <span data-ttu-id="d4a1b-124">Skriv en værdi i feltet **IBAN**.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-124">In the **IBAN** field, type a value.</span></span>
19. <span data-ttu-id="d4a1b-125">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-125">Close the page.</span></span>
20. <span data-ttu-id="d4a1b-126">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-126">Close the page.</span></span>

## <a name="define-the-electronic-payment-method"></a><span data-ttu-id="d4a1b-127">Definer den elektroniske betalingsmåde</span><span class="sxs-lookup"><span data-stu-id="d4a1b-127">Define the electronic payment method</span></span>
1. <span data-ttu-id="d4a1b-128">I **navigationsruden** skal du gå til **Moduler > Debitor > Betalingsopsætning > Betalingsmåder**.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-128">In the **Navigation pane**, go to **Modules > Accounts receivable > Payments setup > Methods of payment**.</span></span>
2. <span data-ttu-id="d4a1b-129">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-129">Click **New**.</span></span>
3. <span data-ttu-id="d4a1b-130">Indtast en værdi i feltet **Betalingsmåde**.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-130">In the **Method of payment** field, type a value.</span></span>
4. <span data-ttu-id="d4a1b-131">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-131">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="d4a1b-132">Vælg 'Elektronisk betaling' i feltet **Betalingstype**.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-132">In the **Payment type** field, enter 'Electronic payment'.</span></span> <span data-ttu-id="d4a1b-133">Betalingstypen for en betalingsmåde med bemyndigelse til direkte debitering skal være elektronisk betaling.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-133">The payment type for a direct debit mandate method of payment must be Electronic payment.</span></span>
6. <span data-ttu-id="d4a1b-134">Vælg Ja i feltet **Kræv bemyndigelse**.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-134">Select Yes in the **Require mandate** field.</span></span>
7. <span data-ttu-id="d4a1b-135">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-135">Close the page.</span></span>

## <a name="add-a-direct-debit-mandate-to-a-customer"></a><span data-ttu-id="d4a1b-136">Føj en bemyndigelse til direkte debitering til en debitor.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-136">Add a direct debit mandate to a customer.</span></span>
1. <span data-ttu-id="d4a1b-137">I **navigationsruden** skal du gå til **Moduler > Debitor > Debitorer > Alle kunder**.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-137">In the **Navigation pane**, go to **Modules > Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="d4a1b-138">Vælg en post på listen.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-138">In the list, select a record.</span></span> <span data-ttu-id="d4a1b-139">Vælg f.eks. US-001</span><span class="sxs-lookup"><span data-stu-id="d4a1b-139">For example, select US-001</span></span>
3. <span data-ttu-id="d4a1b-140">Klik på **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-140">Click **Edit**.</span></span>
4. <span data-ttu-id="d4a1b-141">Udvid oversigtspanelet **Betalingsstandarder**.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-141">Expand the **Payment defaults** fastTab.</span></span>
5. <span data-ttu-id="d4a1b-142">Indtast eller vælg en værdi i feltet **Betalingsmåde**.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-142">In the **Method of payment** field, enter or select a value.</span></span>
6. <span data-ttu-id="d4a1b-143">Udvid oversigtspanelet **Betalingsstandarder**.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-143">Expand the **Payment defaults** fastTab.</span></span>
7. <span data-ttu-id="d4a1b-144">Udvid oversigtspanelet **Bemyndigelser til Direct Debit**.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-144">Expand the **Direct debit mandates** fastTab.</span></span>
8. <span data-ttu-id="d4a1b-145">Klik på **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-145">Click **Add**.</span></span>
9. <span data-ttu-id="d4a1b-146">Indtast eller vælg en værdi i feltet **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-146">In the **Bank account** field, enter or select a value.</span></span>
10. <span data-ttu-id="d4a1b-147">Indtast eller vælg en værdi i feltet **Kreditors bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-147">In the **Creditor bank account** field, enter or select a value.</span></span>
11. <span data-ttu-id="d4a1b-148">Angiv antallet af betalinger, du forventer at behandle for denne bemyndigelse, i feltet **Betalingshyppighed**.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-148">In the **Payment frequency** field, enter the number of payments that you expect to process for this mandate.</span></span>
12. <span data-ttu-id="d4a1b-149">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-149">Click **OK**.</span></span>
13. <span data-ttu-id="d4a1b-150">Klik på **Udskriv**.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-150">Click **Print**.</span></span>
14. <span data-ttu-id="d4a1b-151">Klik på **Bemyndigelsesrapport**.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-151">Click **Mandate report**.</span></span>
15. <span data-ttu-id="d4a1b-152">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-152">Close the page.</span></span>
16. <span data-ttu-id="d4a1b-153">Klik på **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-153">Click **Edit**.</span></span>
17. <span data-ttu-id="d4a1b-154">Angiv en dato i feltet **Dato for signatur**.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-154">In the **Signature date** field, enter a date.</span></span>
18. <span data-ttu-id="d4a1b-155">Klik på **Ja**.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-155">Click **Yes**.</span></span>
19. <span data-ttu-id="d4a1b-156">Angiv den lokalitet, hvor bemyndigelsen blev signeret.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-156">Enter the location where the mandate was signed.</span></span>
20. <span data-ttu-id="d4a1b-157">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-157">Click **OK**.</span></span>
21. <span data-ttu-id="d4a1b-158">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-158">Close the page.</span></span>

## <a name="create-a-free-text-invoice-with-mandate"></a><span data-ttu-id="d4a1b-159">Opret en fritekstfaktura med bemyndigelse</span><span class="sxs-lookup"><span data-stu-id="d4a1b-159">Create a free text invoice with mandate</span></span>
1. <span data-ttu-id="d4a1b-160">I **navigationsruden** skal du gå til **Moduler > Debitor > Fakturaer > Alle fritekstfakturaer**.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-160">In the **Navigation pane**, go to **Modules > Accounts receivable > Invoices > All free text invoices**.</span></span>
2. <span data-ttu-id="d4a1b-161">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-161">Click **New**.</span></span>
3. <span data-ttu-id="d4a1b-162">Vælg den debitor, du har føjet mandatet til.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-162">Select the customer that you added the mandate to.</span></span>
4. <span data-ttu-id="d4a1b-163">Indtast eller vælg en værdi i feltet **Id for bemyndigelse til Direct Debit**.</span><span class="sxs-lookup"><span data-stu-id="d4a1b-163">In the **Direct debit mandate ID** field, enter or select a value.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]