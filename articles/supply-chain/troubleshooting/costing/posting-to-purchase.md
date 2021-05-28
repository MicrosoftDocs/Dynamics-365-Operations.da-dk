---
title: Indkøbsperiodisering med et beløb på nul bogføres for en produktkvittering med nulværdi
description: Når en produktkvittering med nulværdi bogføres, opretter systemet en postering til købsperiodisering, hvor beløbet er 0 (nul).
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: LedgerTransVoucher
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: f8d9d857590dc788d16b01edf77600d8fd8c8444
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026387"
---
# <a name="purchase-accrual-that-has-a-zero-amount-is-posted-for-a-zero-value-product-receipt"></a><span data-ttu-id="b6d96-103">Indkøbsperiodisering med et beløb på nul bogføres for en produktkvittering med nulværdi</span><span class="sxs-lookup"><span data-stu-id="b6d96-103">Purchase accrual that has a zero amount is posted for a zero-value product receipt</span></span>

<span data-ttu-id="b6d96-104">KB-nummer: 4612588</span><span class="sxs-lookup"><span data-stu-id="b6d96-104">KB number: 4612588</span></span>

## <a name="symptoms"></a><span data-ttu-id="b6d96-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="b6d96-105">Symptoms</span></span>

<span data-ttu-id="b6d96-106">Når en produktkvittering med nulværdi bogføres, opretter systemet en postering til købsperiodisering, hvor beløbet er 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="b6d96-106">When a product receipt that has zero value is posted, the system creates a posting to purchase accrual where the amount is 0 (zero).</span></span>

## <a name="resolution"></a><span data-ttu-id="b6d96-107">Løsning</span><span class="sxs-lookup"><span data-stu-id="b6d96-107">Resolution</span></span>

<span data-ttu-id="b6d96-108">Som standard er `IsTransferredIndetail`-feltet altid indstillet til *Oversigt* i forbindelse med finansposteringer af typen *Indkøb, periodisering* i posteringer for reskontroen.</span><span class="sxs-lookup"><span data-stu-id="b6d96-108">By default, for ledger postings of the *Purchase, accrual* type, the `IsTransferredIndetail` field is always set to *Summary* in subledger transactions.</span></span> <span data-ttu-id="b6d96-109">Systemet opretter derfor en relateret bilagspost, selvom beløbet er 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="b6d96-109">Therefore, the system creates a related voucher entry even if the amount is 0 (zero).</span></span>

<span data-ttu-id="b6d96-110">Hvis du vil springe denne bogføringstype over, når beløbet er 0 (nul), skal du forlænge `subledgerJournalizer.markDoNotTransferEntries`-metoden, så den omfatter `ledgerPostingType = PurchPckSlpPurchaseOffsetAccount`, som vist i følgende eksempel.</span><span class="sxs-lookup"><span data-stu-id="b6d96-110">To skip this posting type when the amount is 0 (zero), extend the `subledgerJournalizer.markDoNotTransferEntries` method so that it includes `ledgerPostingType = PurchPckSlpPurchaseOffsetAccount`, as shown in the following example.</span></span>

```xpp
update_recordset existingSubledgerJournalAccountEntry
setting
    IsTransferredInDetail = TransferPolicy::DoNotTransfer
where existingSubledgerJournalAccountEntry.SubledgerJournalEntry == _subledgerJournalEntryRecId
    && (existingSubledgerJournalAccountEntry.AccountingCurrencyAmount == 0 && existingSubledgerJournalAccountEntry.ReportingCurrencyAmount == 0)
    && existingSubledgerJournalAccountEntry.PostingType == LedgerPostingType::PurchPckSlpPurchaseOffsetAccount;
```
