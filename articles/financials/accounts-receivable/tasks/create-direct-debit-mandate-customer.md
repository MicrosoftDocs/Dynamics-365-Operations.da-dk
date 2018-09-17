--- 
title: Oprette en ny bemyndigelse til direkte debitering til en debitor
description: Denne opgaveguide viser, hvordan du kan oprette en bemyndigelse til direkte debitering og bruge den til en faktura.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustTable, CustBankAccounts, BankAccountTable, CustPaymMode, CustDirectDebitMandate, BankAccountTableLookUp, SrsReportViewerForm,  LogisticsAddressCityLookup, CustFreeInvoice, CustTableLookup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d01c7c19925a3c7064ab3f845b92b610b162066c
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a>Oprette en ny bemyndigelse til direkte debitering til en debitor

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne opgaveguide viser, hvordan du kan oprette en bemyndigelse til direkte debitering og bruge den til en faktura.


## <a name="create-a-bank-account"></a>Opret en bankkonto
1. Gå til Debitor > Kunder > Alle kunder.
2. Vælg f.eks. US-001
3. Klik på Kunde i handlingsruden.
4. Klik på Bankkonti.
5. Klik på Ny.
6. Skriv en værdi i feltet Bankkonto.
7. Skriv en værdi i feltet Navn.
8. Skriv en værdi i feltet IBAN.
9. Skriv en værdi i feltet Valuta.
10. Klik på Gem.
11. Luk siden.
12. Gå til Kontant- og bankstyring > Bankkonti > Bankkonti.
13. Find og vælg den ønskede post på listen.
14. Klik op linket i den valgte række på listen.
15. Klik på Rediger.
16. Udvid sektionen Yderligere identifikation.
17. Skriv en værdi i feltet Direct Debit-id.
18. Skriv en værdi i feltet IBAN.
19. Luk siden.
20. Luk siden.

## <a name="define-the-electronic-payment-method"></a>Definer den elektroniske betalingsmåde
1. Gå til Debitor > Betalingsopsætning > Betalingsmetoder.
2. Klik på Ny.
3. Indtast en værdi i feltet Betalingsmåde.
4. Skriv en værdi i feltet Beskrivelse.
5. Betalingstypen for en betalingsmåde med bemyndigelse til direkte debitering skal være elektronisk betaling.
6. Vælg Ja i feltet Kræv bemyndigelse.
7. Luk siden.

## <a name="add-a-direct-debit-mandate-to-a-customer"></a>Føj en bemyndigelse til direkte debitering til en debitor.
1. Gå til Debitor > Kunder > Alle kunder.
2. Vælg f.eks. US-001
3. Klik på Rediger.
4. Udvid sektionen Betalingsstandarder.
5. Indtast eller vælg en værdi i feltet Betalingsmåde.
6. Udvid sektionen Betalingsstandarder.
7. Udvid sektionen Bemyndigelser til Direct Debit.
8. Klik på Tilføj.
9. Indtast eller vælg en værdi i feltet Bankkonto.
10. Indtast eller vælg en værdi i feltet Kreditors bankkonto.
11. Angiv antallet af betalinger, du forventer at behandle for denne bemyndigelse.
12. Klik på OK.
13. Klik på Udskriv.
14. Klik på Bemyndigelsesrapport.
15. Luk siden.
16. Klik på Rediger.
17. Angiv en dato i feltet Dato for signatur.
18. Klik på Ja.
19. Angiv den lokalitet, hvor bemyndigelsen blev signeret.
20. Klik på OK.
21. Luk siden.

## <a name="create-a-free-text-invoice-with-mandate"></a>Opret en fritekstfaktura med bemyndigelse
1. Gå til Debitor > Fakturaer > Alle fritekstfakturaer.
2. Klik på Ny.
3. Vælg den debitor, du har føjet mandatet til.
4. Indtast eller vælg en værdi i feltet Id for bemyndigelse til Direct Debit.


