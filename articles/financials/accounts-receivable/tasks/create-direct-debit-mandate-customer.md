--- 
title: Oprette en ny bemyndigelse til direkte debitering til en debitor
description: Denne opgaveguide viser, hvordan du kan oprette en bemyndigelse til direkte debitering og bruge den til en faktura.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/23/2016
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: be0db88639586e50f8a883bada64a52fb3e83e14
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a><span data-ttu-id="cb7f6-103">Oprette en ny bemyndigelse til direkte debitering til en debitor</span><span class="sxs-lookup"><span data-stu-id="cb7f6-103">Create a direct debit mandate for a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cb7f6-104">Denne opgaveguide viser, hvordan du kan oprette en bemyndigelse til direkte debitering og bruge den til en faktura.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-104">This task guide demonstrates how to create a direct debit mandate and use it on an invoice.</span></span>


## <a name="create-a-bank-account"></a><span data-ttu-id="cb7f6-105">Opret en bankkonto</span><span class="sxs-lookup"><span data-stu-id="cb7f6-105">Create a bank account</span></span>
1. <span data-ttu-id="cb7f6-106">Gå til Debitor > Kunder > Alle kunder.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-106">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="cb7f6-107">Vælg f.eks. US-001</span><span class="sxs-lookup"><span data-stu-id="cb7f6-107">For example, select US-001</span></span>
3. <span data-ttu-id="cb7f6-108">Klik på Kunde i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-108">On the Action Pane, click Customer.</span></span>
4. <span data-ttu-id="cb7f6-109">Klik på Bankkonti.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-109">Click Bank accounts.</span></span>
5. <span data-ttu-id="cb7f6-110">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-110">Click New.</span></span>
6. <span data-ttu-id="cb7f6-111">Skriv en værdi i feltet Bankkonto.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-111">In the Bank account field, type a value.</span></span>
7. <span data-ttu-id="cb7f6-112">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-112">In the Name field, type a value.</span></span>
8. <span data-ttu-id="cb7f6-113">Skriv en værdi i feltet IBAN.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-113">In the IBAN field, type a value.</span></span>
9. <span data-ttu-id="cb7f6-114">Skriv en værdi i feltet Valuta.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-114">In the Currency field, type a value.</span></span>
10. <span data-ttu-id="cb7f6-115">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-115">Click Save.</span></span>
11. <span data-ttu-id="cb7f6-116">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-116">Close the page.</span></span>
12. <span data-ttu-id="cb7f6-117">Gå til Kontant- og bankstyring > Bankkonti > Bankkonti.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-117">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
13. <span data-ttu-id="cb7f6-118">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-118">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="cb7f6-119">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-119">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="cb7f6-120">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-120">Click Edit.</span></span>
16. <span data-ttu-id="cb7f6-121">Udvid sektionen Yderligere identifikation.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-121">Expand the Additional identification section.</span></span>
17. <span data-ttu-id="cb7f6-122">Skriv en værdi i feltet Direct Debit-id.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-122">In the Direct debit ID field, type a value.</span></span>
18. <span data-ttu-id="cb7f6-123">Skriv en værdi i feltet IBAN.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-123">In the IBAN field, type a value.</span></span>
19. <span data-ttu-id="cb7f6-124">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-124">Close the page.</span></span>
20. <span data-ttu-id="cb7f6-125">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-125">Close the page.</span></span>

## <a name="define-the-electronic-payment-method"></a><span data-ttu-id="cb7f6-126">Definer den elektroniske betalingsmåde</span><span class="sxs-lookup"><span data-stu-id="cb7f6-126">Define the electronic payment method</span></span>
1. <span data-ttu-id="cb7f6-127">Gå til Debitor > Betalingsopsætning > Betalingsmetoder.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-127">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="cb7f6-128">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-128">Click New.</span></span>
3. <span data-ttu-id="cb7f6-129">Indtast en værdi i feltet Betalingsmåde.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-129">In the Method of payment field, type a value.</span></span>
4. <span data-ttu-id="cb7f6-130">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-130">In the Description field, type a value.</span></span>
5. <span data-ttu-id="cb7f6-131">Betalingstypen for en betalingsmåde med bemyndigelse til direkte debitering skal være elektronisk betaling.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-131">The payment type for a direct debit mandate method of payment must be Electronic payment.</span></span>
6. <span data-ttu-id="cb7f6-132">Vælg Ja i feltet Kræv bemyndigelse.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-132">Select Yes in the Require mandate field.</span></span>
7. <span data-ttu-id="cb7f6-133">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-133">Close the page.</span></span>

## <a name="add-a-direct-debit-mandate-to-a-customer"></a><span data-ttu-id="cb7f6-134">Føj en bemyndigelse til direkte debitering til en debitor.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-134">Add a direct debit mandate to a customer.</span></span>
1. <span data-ttu-id="cb7f6-135">Gå til Debitor > Kunder > Alle kunder.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-135">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="cb7f6-136">Vælg f.eks. US-001</span><span class="sxs-lookup"><span data-stu-id="cb7f6-136">For example, select US-001</span></span>
3. <span data-ttu-id="cb7f6-137">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-137">Click Edit.</span></span>
4. <span data-ttu-id="cb7f6-138">Udvid sektionen Betalingsstandarder.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-138">Expand the Payment defaults section.</span></span>
5. <span data-ttu-id="cb7f6-139">Indtast eller vælg en værdi i feltet Betalingsmåde.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-139">In the Method of payment field, enter or select a value.</span></span>
6. <span data-ttu-id="cb7f6-140">Udvid sektionen Betalingsstandarder.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-140">Expand the Payment defaults section.</span></span>
7. <span data-ttu-id="cb7f6-141">Udvid sektionen Bemyndigelser til Direct Debit.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-141">Expand the Direct debit mandates section.</span></span>
8. <span data-ttu-id="cb7f6-142">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-142">Click Add.</span></span>
9. <span data-ttu-id="cb7f6-143">Indtast eller vælg en værdi i feltet Bankkonto.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-143">In the Bank account field, enter or select a value.</span></span>
10. <span data-ttu-id="cb7f6-144">Indtast eller vælg en værdi i feltet Kreditors bankkonto.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-144">In the Creditor bank account field, enter or select a value.</span></span>
11. <span data-ttu-id="cb7f6-145">Angiv antallet af betalinger, du forventer at behandle for denne bemyndigelse.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-145">Enter the number of payments that you expect to process for this mandate.</span></span>
12. <span data-ttu-id="cb7f6-146">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-146">Click OK.</span></span>
13. <span data-ttu-id="cb7f6-147">Klik på Udskriv.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-147">Click Print.</span></span>
14. <span data-ttu-id="cb7f6-148">Klik på Bemyndigelsesrapport.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-148">Click Mandate report.</span></span>
15. <span data-ttu-id="cb7f6-149">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-149">Close the page.</span></span>
16. <span data-ttu-id="cb7f6-150">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-150">Click Edit.</span></span>
17. <span data-ttu-id="cb7f6-151">Angiv en dato i feltet Dato for signatur.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-151">In the Signature date field, enter a date.</span></span>
18. <span data-ttu-id="cb7f6-152">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-152">Click Yes.</span></span>
19. <span data-ttu-id="cb7f6-153">Angiv den lokalitet, hvor bemyndigelsen blev signeret.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-153">Enter the location where the mandate was signed.</span></span>
20. <span data-ttu-id="cb7f6-154">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-154">Click OK.</span></span>
21. <span data-ttu-id="cb7f6-155">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-155">Close the page.</span></span>

## <a name="create-a-free-text-invoice-with-mandate"></a><span data-ttu-id="cb7f6-156">Opret en fritekstfaktura med bemyndigelse</span><span class="sxs-lookup"><span data-stu-id="cb7f6-156">Create a free text invoice with mandate</span></span>
1. <span data-ttu-id="cb7f6-157">Gå til Debitor > Fakturaer > Alle fritekstfakturaer.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-157">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="cb7f6-158">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-158">Click New.</span></span>
3. <span data-ttu-id="cb7f6-159">Vælg den debitor, du har føjet mandatet til.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-159">Select the customer that you added the mandate to.</span></span>
4. <span data-ttu-id="cb7f6-160">Indtast eller vælg en værdi i feltet Id for bemyndigelse til Direct Debit.</span><span class="sxs-lookup"><span data-stu-id="cb7f6-160">In the Direct debit mandate ID field, enter or select a value.</span></span>


