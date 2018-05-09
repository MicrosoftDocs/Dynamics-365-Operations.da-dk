---
title: Refundere kunder
description: "I denne artikel beskrives det, hvordan du kan oprette refusionsposteringer for en gruppe af debitorer. Hvis en kunde har en kreditsaldo, kan du refundere kunden beløbet svarende til saldoen."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: c3bee87b1d82dbe3d1c6de78a26633f2e1f5e92f
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---

# <a name="reimburse-customers"></a><span data-ttu-id="9994c-104">Refundere kunder</span><span class="sxs-lookup"><span data-stu-id="9994c-104">Reimburse customers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9994c-105">I denne artikel beskrives det, hvordan du kan oprette refusionsposteringer for en gruppe af debitorer.</span><span class="sxs-lookup"><span data-stu-id="9994c-105">This article explains how to create reimbursement transactions for a group of customers.</span></span> <span data-ttu-id="9994c-106">Hvis en kunde har en kreditsaldo, kan du refundere kunden beløbet svarende til saldoen.</span><span class="sxs-lookup"><span data-stu-id="9994c-106">If a customer has a credit balance, you can reimburse the customer for the amount of the balance.</span></span> 

<span data-ttu-id="9994c-107">Følgende tabel viser de forudsætninger, der skal være på plads, før du starter.</span><span class="sxs-lookup"><span data-stu-id="9994c-107">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="9994c-108">Forudsætning</span><span class="sxs-lookup"><span data-stu-id="9994c-108">Prerequisite</span></span>                                                            | <span data-ttu-id="9994c-109">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="9994c-109">Description</span></span>                                                                                                                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9994c-110">Angiv minimumbeløbet for refusion for den juridiske enhed.</span><span class="sxs-lookup"><span data-stu-id="9994c-110">Specify the minimum reimbursement amount for the legal entity.</span></span>          | <span data-ttu-id="9994c-111">På siden **Debitorparametre** side i området **Generelt** i feltet **Minimumsrefusion** skal du angive det minimumbeløb, som kan refunderes i forbindelse med kunders overbetaling.</span><span class="sxs-lookup"><span data-stu-id="9994c-111">On the **Accounts receivable parameters** page, in the **General** area, in the **Minimum reimbursement** field, enter the minimum amount that can be reimbursed for customer overpayments.</span></span> |
| <span data-ttu-id="9994c-112">Valgfrit: Føj en kreditorkonto til hver kunde, der kan få refunderet beløb.</span><span class="sxs-lookup"><span data-stu-id="9994c-112">Optional: Add a vendor account to each customer that can be reimbursed.</span></span> | <span data-ttu-id="9994c-113">Vælg kundens kreditorkonto på siden **Kunder** på oversigtspanelet **Diverse detaljer** i feltet **Kreditorkonto**.</span><span class="sxs-lookup"><span data-stu-id="9994c-113">On the **Customers** page, on the **Miscellaneous details** FastTab, in the **Vendor account** field, select the vendor account for the customer.</span></span>                                           |

<span data-ttu-id="9994c-114">Når du opretter refusionsposteringer, oprettes der en kreditorfaktura for beløbet svarende til kreditsaldoen.</span><span class="sxs-lookup"><span data-stu-id="9994c-114">When you create reimbursement transactions, a vendor invoice is created for the amount of the credit balance.</span></span> <span data-ttu-id="9994c-115">Refusionsprocessen fjerner kreditsaldoen for debitorkontoen, og der oprettes en forfalden saldo for kreditorkontoen, der er knyttet til kunden.</span><span class="sxs-lookup"><span data-stu-id="9994c-115">The reimbursement process removes the credit balance for the customer account and creates a balance due for the vendor account that corresponds to the customer.</span></span>

1.  <span data-ttu-id="9994c-116">I Debitor skal du køre processen **Refusion**.</span><span class="sxs-lookup"><span data-stu-id="9994c-116">In Accounts receivable, run the **Reimbursement** process.</span></span>
2.  <span data-ttu-id="9994c-117">Udfør ét af følgende trin:</span><span class="sxs-lookup"><span data-stu-id="9994c-117">Follow one of these steps:</span></span>
    -   <span data-ttu-id="9994c-118">Hvis refusionen kun gælder bestemte kundekonti, skal du klikke på **Vælg** og angive kundekontiene i forespørgslen.</span><span class="sxs-lookup"><span data-stu-id="9994c-118">To reimburse specific customer accounts, click **Select**, and specify the customer accounts in the query.</span></span>
    -   <span data-ttu-id="9994c-119">Hvis refusionen gælder alle kundekonti, skal du klikke på **OK**.</span><span class="sxs-lookup"><span data-stu-id="9994c-119">To reimburse all customer accounts, click **OK**.</span></span>

    <span data-ttu-id="9994c-120">Kreditbeløbene overføres til kundernes kreditorkonti og behandles som almindelige betalinger.</span><span class="sxs-lookup"><span data-stu-id="9994c-120">The credit amounts are transferred to the vendor accounts of the customers and are processed as ordinary payments.</span></span> <span data-ttu-id="9994c-121">Hvis en kunde ikke har en kreditorkonto, oprettes der automatisk en engangskreditorkonto for kunden.</span><span class="sxs-lookup"><span data-stu-id="9994c-121">If a customer doesn't have a vendor account, a one-time vendor account is automatically created for the customer.</span></span>
3.  <span data-ttu-id="9994c-122">Til at få vist de refusionsposter, der er oprettet, kan du bruge siden **Refusion**.</span><span class="sxs-lookup"><span data-stu-id="9994c-122">To view the reimbursement transactions that were created, use the **Reimbursement** page.</span></span>
4.  <span data-ttu-id="9994c-123">I Kreditor skal du oprette en betaling for kreditorfakturaer, der er oprettet af refusionsprocessen.</span><span class="sxs-lookup"><span data-stu-id="9994c-123">In Accounts payable, create a payment for the vendor invoices that were created by the reimbursement process.</span></span>





