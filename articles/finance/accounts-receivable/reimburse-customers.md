---
title: Refundere kunder
description: I denne artikel beskrives det, hvordan du kan oprette refusionsposteringer for en gruppe af debitorer. Hvis en kunde har en kreditsaldo, kan du refundere kunden beløbet svarende til saldoen.
author: JodiChristiansen
manager: AnnBe
ms.date: 09/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: roschlom
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ae6a3078743fc9cd43c71bc1d4531c0553ee53bb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5012133"
---
# <a name="reimburse-customers"></a><span data-ttu-id="bd587-104">Refundere kunder</span><span class="sxs-lookup"><span data-stu-id="bd587-104">Reimburse customers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bd587-105">I denne artikel beskrives det, hvordan du kan oprette refusionsposteringer for en gruppe af debitorer.</span><span class="sxs-lookup"><span data-stu-id="bd587-105">This article explains how to create reimbursement transactions for a group of customers.</span></span> <span data-ttu-id="bd587-106">Hvis en kunde har en kreditsaldo, kan du refundere kunden beløbet svarende til saldoen.</span><span class="sxs-lookup"><span data-stu-id="bd587-106">If a customer has a credit balance, you can reimburse the customer for the amount of the balance.</span></span> 

<span data-ttu-id="bd587-107">Følgende tabel viser de forudsætninger, der skal være på plads, før du starter.</span><span class="sxs-lookup"><span data-stu-id="bd587-107">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="bd587-108">Forudsætning</span><span class="sxs-lookup"><span data-stu-id="bd587-108">Prerequisite</span></span>                                                            | <span data-ttu-id="bd587-109">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="bd587-109">Description</span></span> |
|-------------------------------------------------------------------------|-------------|
| <span data-ttu-id="bd587-110">Angiv minimumbeløbet for refusion for den juridiske enhed.</span><span class="sxs-lookup"><span data-stu-id="bd587-110">Specify the minimum reimbursement amount for the legal entity.</span></span>          | <span data-ttu-id="bd587-111">På siden **Debitorparametre** side i området **Generelt** i feltet **Minimumsrefusion** skal du angive det minimumbeløb, som kan refunderes i forbindelse med kunders overbetaling.</span><span class="sxs-lookup"><span data-stu-id="bd587-111">On the **Accounts receivable parameters** page, in the **General** area, in the **Minimum reimbursement** field, enter the minimum amount that can be reimbursed for customer overpayments.</span></span> |
| <span data-ttu-id="bd587-112">Valgfrit: Føj en kreditorkonto til hver kunde, der kan få refunderet beløb.</span><span class="sxs-lookup"><span data-stu-id="bd587-112">Optional: Add a vendor account to each customer that can be reimbursed.</span></span> | <span data-ttu-id="bd587-113">Vælg kundens kreditorkonto på siden **Kunder** på oversigtspanelet **Diverse detaljer** i feltet **Kreditorkonto**.</span><span class="sxs-lookup"><span data-stu-id="bd587-113">On the **Customers** page, on the **Miscellaneous details** FastTab, in the **Vendor account** field, select the vendor account for the customer.</span></span> |

<span data-ttu-id="bd587-114">Når du opretter refusionsposteringer, oprettes der en kreditorfaktura for beløbet svarende til kreditsaldoen.</span><span class="sxs-lookup"><span data-stu-id="bd587-114">When you create reimbursement transactions, a vendor invoice is created for the amount of the credit balance.</span></span> <span data-ttu-id="bd587-115">Refusionsprocessen fjerner kreditsaldoen for debitorkontoen, og der oprettes en forfalden saldo for kreditorkontoen, der er knyttet til kunden.</span><span class="sxs-lookup"><span data-stu-id="bd587-115">The reimbursement process removes the credit balance for the customer account and creates a balance due for the vendor account that corresponds to the customer.</span></span>

1. <span data-ttu-id="bd587-116">I debitor skal du køre **Refusions-** processen (**Debitor \> Periodiske opgaver \> Refusion**).</span><span class="sxs-lookup"><span data-stu-id="bd587-116">In Accounts receivable, run the **Reimbursement** process (**Accounts receivable \> Periodic tasks \> Reimbursement**).</span></span>
2. <span data-ttu-id="bd587-117">Hvis du vil gruppere alle posteringer, uanset finansdimensioner, skal du angive indstillingen **Opsummer debitor** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="bd587-117">To group all transactions, regardless of ledger dimensions, set the **Summarize customer** option to **Yes**.</span></span> <span data-ttu-id="bd587-118">Hvis du kun vil gruppere posteringer med lignende finansdimensioner, skal du angive indstillingen til **Nej**.</span><span class="sxs-lookup"><span data-stu-id="bd587-118">To group only transactions that have similar ledger dimensions, set the option to **No**.</span></span>
3. <span data-ttu-id="bd587-119">Vælg **Medtag debitorer med udestående debetposteringer** for at vælge kunder, der har ikke-udlignede debetbeløb.</span><span class="sxs-lookup"><span data-stu-id="bd587-119">Select **Include customers with outstanding debit transactions** to select customers who have unsettled debit amounts.</span></span>
4. <span data-ttu-id="bd587-120">Hvis du vil refundere bestemte debitorkonti, skal du på oversigtspanelet **Poster, der skal indgå** vælge **Filter** og derefter angive debitorkontiene i forespørgslen.</span><span class="sxs-lookup"><span data-stu-id="bd587-120">To reimburse specific customer accounts, on the **Records to include** FastTab, select **Filter**, and then specify the customer accounts in the query.</span></span>

    <span data-ttu-id="bd587-121">Kreditbeløbene overføres til kundernes kreditorkonti og behandles som almindelige betalinger.</span><span class="sxs-lookup"><span data-stu-id="bd587-121">The credit amounts are transferred to the vendor accounts of the customers and are processed as ordinary payments.</span></span> <span data-ttu-id="bd587-122">Hvis en kunde ikke har en kreditorkonto, oprettes der automatisk en engangskreditorkonto for kunden.</span><span class="sxs-lookup"><span data-stu-id="bd587-122">If a customer doesn't have a vendor account, a one-time vendor account is automatically created for the customer.</span></span>

5. <span data-ttu-id="bd587-123">Hvis du vil have vist de refusionsposteringer, der er oprettet, skal du bruge rapporten **Refusion** (**Debitor \> Forespørgsler og rapporter \> Refusionsrapport**).</span><span class="sxs-lookup"><span data-stu-id="bd587-123">To view the reimbursement transactions that were created, use the **Reimbursement** report (**Accounts Receivable \> Inquiries and reports \> Reimbursement report**).</span></span>
6. <span data-ttu-id="bd587-124">I Kreditor skal du oprette en betaling for kreditorfakturaer, der er oprettet af refusionsprocessen.</span><span class="sxs-lookup"><span data-stu-id="bd587-124">In Accounts payable, create a payment for the vendor invoices that were created by the reimbursement process.</span></span> <span data-ttu-id="bd587-125">Du kan finde flere oplysninger om betaling af kreditorer under [Oversigten Kreditorbetaling](../accounts-payable/Vendor-payments-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="bd587-125">For information about how to pay vendors, see [Vendor payment overview](../accounts-payable/Vendor-payments-workspace.md).</span></span>
