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
# <a name="purchase-accrual-that-has-a-zero-amount-is-posted-for-a-zero-value-product-receipt"></a>Indkøbsperiodisering med et beløb på nul bogføres for en produktkvittering med nulværdi

KB-nummer: 4612588

## <a name="symptoms"></a>Symptomer

Når en produktkvittering med nulværdi bogføres, opretter systemet en postering til købsperiodisering, hvor beløbet er 0 (nul).

## <a name="resolution"></a>Løsning

Som standard er `IsTransferredIndetail`-feltet altid indstillet til *Oversigt* i forbindelse med finansposteringer af typen *Indkøb, periodisering* i posteringer for reskontroen. Systemet opretter derfor en relateret bilagspost, selvom beløbet er 0 (nul).

Hvis du vil springe denne bogføringstype over, når beløbet er 0 (nul), skal du forlænge `subledgerJournalizer.markDoNotTransferEntries`-metoden, så den omfatter `ledgerPostingType = PurchPckSlpPurchaseOffsetAccount`, som vist i følgende eksempel.

```xpp
update_recordset existingSubledgerJournalAccountEntry
setting
    IsTransferredInDetail = TransferPolicy::DoNotTransfer
where existingSubledgerJournalAccountEntry.SubledgerJournalEntry == _subledgerJournalEntryRecId
    && (existingSubledgerJournalAccountEntry.AccountingCurrencyAmount == 0 && existingSubledgerJournalAccountEntry.ReportingCurrencyAmount == 0)
    && existingSubledgerJournalAccountEntry.PostingType == LedgerPostingType::PurchPckSlpPurchaseOffsetAccount;
```
