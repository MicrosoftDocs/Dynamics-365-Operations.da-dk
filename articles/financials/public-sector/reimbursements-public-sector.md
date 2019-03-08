---
title: Refusioner i den offentlige sektor
description: I dette emne besvares almindelige spørgsmål i forbindelse med refusioner i den offentlige sektor.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustBillingClassification
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 27311
ms.assetid: 9d61d1d8-1672-4bd0-ae0d-605b09240890
ms.search.region: Global
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b08e821cae0a2ac6c133f63d71c068c3d950a6fa
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "370191"
---
# <a name="reimbursements-in-the-public-sector"></a><span data-ttu-id="8449a-103">Refusioner i den offentlige sektor</span><span class="sxs-lookup"><span data-stu-id="8449a-103">Reimbursements in the public sector</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8449a-104">I dette emne besvares almindelige spørgsmål i forbindelse med refusioner i den offentlige sektor.</span><span class="sxs-lookup"><span data-stu-id="8449a-104">This topic answers common questions related to reimbursements in the public sector.</span></span> 

<a name="what-happens-if-i-create-a-separate-reimbursement-transaction-for-each-billing-classification"></a><span data-ttu-id="8449a-105">Hvad sker der, hvis jeg opretter en separat refusionspostering for hver faktureringsklassifikation?</span><span class="sxs-lookup"><span data-stu-id="8449a-105">What happens if I create a separate reimbursement transaction for each billing classification?</span></span>
----------------------------------------------------------------------------------------------

<span data-ttu-id="8449a-106">Når du opretter en separat refusionspostering for hver faktureringsklassifikation, samles kreditnotaposteringer, der er fordelt til den samme finanskonto, og som har samme faktureringsklassifikation til en enkelt refusionspostering.</span><span class="sxs-lookup"><span data-stu-id="8449a-106">When you create a separate reimbursement transaction for each billing classification, the credit note transactions that are distributed to the same ledger account and that have the same billing classification will be combined into a single reimbursement transaction.</span></span> <span data-ttu-id="8449a-107">Der oprettes separate refusionsposteringer for kreditnotaposteringer, der er fordelt til den samme finanskonto, og som har forskellige faktureringsklassifikationer.</span><span class="sxs-lookup"><span data-stu-id="8449a-107">Credit note transactions that are distributed to the same ledger account and that have different billing classifications will generate separate reimbursement transactions.</span></span> <span data-ttu-id="8449a-108">Lad os f.eks. antage, du behandler refusioner til tre kreditnotaer.</span><span class="sxs-lookup"><span data-stu-id="8449a-108">For example, let’s say that you process reimbursements for three credit notes.</span></span> <span data-ttu-id="8449a-109">Alle tre kreditnotaer er $1000.</span><span class="sxs-lookup"><span data-stu-id="8449a-109">All three credit notes are for $1000.</span></span>

-   <span data-ttu-id="8449a-110">Første kreditnota har faktureringsklassifikation UTL, er fordelt på tre firmaer, med 15 % til konto 1110, 30 % til konto 2210 og 55 % til konto 3210.</span><span class="sxs-lookup"><span data-stu-id="8449a-110">The first credit note has billing classification UTL, is distributed to three accounts, with 15% going to account 1110, 30% to account 2210, and 55% to account 3210.</span></span>
-   <span data-ttu-id="8449a-111">Den anden kreditnota har også faktureringsklassifikation UTL.</span><span class="sxs-lookup"><span data-stu-id="8449a-111">The second credit note also has billing classification UTL.</span></span> <span data-ttu-id="8449a-112">Den er distribueret 100 % til konto 3210.</span><span class="sxs-lookup"><span data-stu-id="8449a-112">It is distributed 100% to account 3210.</span></span>
-   <span data-ttu-id="8449a-113">Den tredje kreditnota med faktureringsklassifikationen GEN er distribueret 100 % til konto 1110.</span><span class="sxs-lookup"><span data-stu-id="8449a-113">The third credit note, with billing classification GEN, is distributed 100% to account 1110.</span></span>

<span data-ttu-id="8449a-114">Hvis du opretter en separat refusionspostering for hver faktureringsklassifikation, vil fire refusionsposteringer blive oprettet, på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="8449a-114">If you create a separate reimbursement transaction for each billing classification, four reimbursement transactions will be created, as follows:</span></span>

-   <span data-ttu-id="8449a-115">$150 til konto 1110</span><span class="sxs-lookup"><span data-stu-id="8449a-115">$150 to account 1110</span></span>
-   <span data-ttu-id="8449a-116">$1000 til konto 1110</span><span class="sxs-lookup"><span data-stu-id="8449a-116">$1000 to account 1110</span></span>
-   <span data-ttu-id="8449a-117">$300 til konto 2210</span><span class="sxs-lookup"><span data-stu-id="8449a-117">$300 to account 2210</span></span>
-   <span data-ttu-id="8449a-118">$1550 til konto 3210</span><span class="sxs-lookup"><span data-stu-id="8449a-118">$1550 to account 3210</span></span>

<span data-ttu-id="8449a-119">De beløb, der går til konto 3210, kombineres, fordi de begge bruger samme faktureringsklassifikation.</span><span class="sxs-lookup"><span data-stu-id="8449a-119">The amounts going to account 3210 are combined, because they both use the same billing classification.</span></span> <span data-ttu-id="8449a-120">De beløb, der går til konto 1110, kombineres ikke, fordi de ikke bruger samme faktureringsklassifikation.</span><span class="sxs-lookup"><span data-stu-id="8449a-120">The amounts going to account 1110 are not combined, because they do not use the same billing classification.</span></span> <span data-ttu-id="8449a-121">Hvis du ikke opretter en separat refusion for hver faktureringsklassifikation, vil posteringerne for konto 1110 blive kombineret, og kun tre refusionsposteringer vil blive oprettet.</span><span class="sxs-lookup"><span data-stu-id="8449a-121">If you do not create a separate reimbursement for each billing classification, the transactions for account 1110 would be combined, and only three reimbursement transactions would be created.</span></span>

## <a name="how-do-billing-classifications-affect-reimbursements-for-overpayments"></a><span data-ttu-id="8449a-122">Hvordan påvirker faktureringsklassifikationer refusioner for overbetalinger?</span><span class="sxs-lookup"><span data-stu-id="8449a-122">How do billing classifications affect reimbursements for overpayments?</span></span>
<span data-ttu-id="8449a-123">Det gør de ikke.</span><span class="sxs-lookup"><span data-stu-id="8449a-123">They don’t.</span></span> <span data-ttu-id="8449a-124">Faktureringsklassifikationer anvendes aldrig til debitorbetalinger, så de bruges ikke ved behandling af refusioner for overbetalinger.</span><span class="sxs-lookup"><span data-stu-id="8449a-124">Billing classifications are never applied to customer payments, so they aren’t used when processing reimbursements for overpayments.</span></span>

## <a name="can-i-process-a-reimbursement-for-a-customer-who-has-outstanding-debit-transactions"></a><span data-ttu-id="8449a-125">Er det muligt at behandle en refusion til en kunde, der har udestående debiteringer?</span><span class="sxs-lookup"><span data-stu-id="8449a-125">Can I process a reimbursement for a customer who has outstanding debit transactions?</span></span>
<span data-ttu-id="8449a-126">Ja.</span><span class="sxs-lookup"><span data-stu-id="8449a-126">Yes.</span></span> <span data-ttu-id="8449a-127">Hvis du vil behandle en refusion for en kunde med udestående debiteringer, skal du bruge filtre på siden refusion til at vælge debitoren og vælge indstillingen for at medtage debitorer med udestående debiteringer.</span><span class="sxs-lookup"><span data-stu-id="8449a-127">If you need to process a reimbursement for a customer with outstanding debit transactions, use the filters on the reimbursement page to select the customer, and select the option to include customers with outstanding debit transactions.</span></span> <span data-ttu-id="8449a-128">Når du gør dette, oprettes refusionsposteringer for det fulde beløb af alle kundens kreditposteringer.</span><span class="sxs-lookup"><span data-stu-id="8449a-128">When you do this, reimbursement transactions are created for the full amount of all of the customer’s credit transactions.</span></span> <span data-ttu-id="8449a-129">De udestående debetbeløb er ikke trukket fra kreditbeløbene.</span><span class="sxs-lookup"><span data-stu-id="8449a-129">The outstanding debit amounts are not deducted from the credit amounts.</span></span>

## <a name="can-i-process-reimbursements-for-customers-who-have-pending-settlements"></a><span data-ttu-id="8449a-130">Kan jeg ikke behandle refusioner for kunder, der har ventende udligninger?</span><span class="sxs-lookup"><span data-stu-id="8449a-130">Can I process reimbursements for customers who have pending settlements?</span></span>
<span data-ttu-id="8449a-131">Nr.</span><span class="sxs-lookup"><span data-stu-id="8449a-131">No.</span></span> <span data-ttu-id="8449a-132">Refusioner behandles ikke for en kunde, der har ventende udligninger, der ikke er blevet bogført til journalen.</span><span class="sxs-lookup"><span data-stu-id="8449a-132">Reimbursements are not processed for any customer who has pending settlements that have not been posted to the journal.</span></span>

## <a name="can-i-reverse-reimbursement-settlements"></a><span data-ttu-id="8449a-133">Kan jeg fortryde refusionsudligninger?</span><span class="sxs-lookup"><span data-stu-id="8449a-133">Can I reverse reimbursement settlements?</span></span>
<span data-ttu-id="8449a-134">Nej, ikke direkte.</span><span class="sxs-lookup"><span data-stu-id="8449a-134">No, not directly.</span></span> <span data-ttu-id="8449a-135">Du kan dog bruge finanskladdeposter til at oprette posteringer, der ville medføre tilbageførsel af finansposterne.</span><span class="sxs-lookup"><span data-stu-id="8449a-135">However, you could use general journal entries to create transactions that would have the effect of reversing the general ledger entries.</span></span>





