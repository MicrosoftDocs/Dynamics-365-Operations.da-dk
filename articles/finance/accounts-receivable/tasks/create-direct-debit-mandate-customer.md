---
title: Oprette en ny bemyndigelse til direkte debitering til en debitor
description: Denne opgaveguide viser, hvordan du kan oprette en bemyndigelse til direkte debitering og bruge den til en faktura.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, BankAccountTable, CustPaymMode, CustDirectDebitMandate, BankAccountTableLookUp, SrsReportViewerForm,  LogisticsAddressCityLookup, CustFreeInvoice, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 86d29782f616219b5d84e3567910cb28c60b65ae
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441453"
---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a>Oprette en ny bemyndigelse til direkte debitering til en debitor

[!include [banner](../../includes/banner.md)]

Denne opgaveguide viser, hvordan du kan oprette en bemyndigelse til direkte debitering og bruge den til en faktura.


## <a name="create-a-bank-account"></a>Opret en bankkonto
1. I **navigationsruden** skal du gå til **Moduler > Debitor > Debitorer > Alle kunder**.
2. Vælg en post på listen. Vælg f.eks. US-001
3. Klik på **Debitor** i handlingsruden.
4. Klik på **Bankkonti**.
5. Klik på **Ny**.
6. Skriv en værdi i feltet **Bankkonto**.
7. Skriv en værdi i feltet **Navn**.
8. Skriv en værdi i feltet **IBAN**.
9. Skriv en værdi i feltet **Valuta**.
10. Klik på **Gem**.
11. Luk siden.
12. Gå i **navigationsruden** til **Moduler > Kontant- og bankstyring > Bankkonti > Bankkonti**.
13. Find og vælg den ønskede post på listen.
14. Klik op linket i den valgte række på listen.
15. Klik på **Rediger**.
16. Udvid oversigtspanelet **Yderligere identifikation**.
17. Skriv en værdi i feltet **Direct Debit-id**.
18. Skriv en værdi i feltet **IBAN**.
19. Luk siden.
20. Luk siden.

## <a name="define-the-electronic-payment-method"></a>Definer den elektroniske betalingsmåde
1. I **navigationsruden** skal du gå til **Moduler > Debitor > Betalingsopsætning > Betalingsmåder**.
2. Klik på **Ny**.
3. Indtast en værdi i feltet **Betalingsmåde**.
4. Indtast en værdi i feltet **Beskrivelse**.
5. Vælg 'Elektronisk betaling' i feltet **Betalingstype**. Betalingstypen for en betalingsmåde med bemyndigelse til direkte debitering skal være elektronisk betaling.
6. Vælg Ja i feltet **Kræv bemyndigelse**.
7. Luk siden.

## <a name="add-a-direct-debit-mandate-to-a-customer"></a>Føj en bemyndigelse til direkte debitering til en debitor.
1. I **navigationsruden** skal du gå til **Moduler > Debitor > Debitorer > Alle kunder**.
2. Vælg en post på listen. Vælg f.eks. US-001
3. Klik på **Rediger**.
4. Udvid oversigtspanelet **Betalingsstandarder**.
5. Indtast eller vælg en værdi i feltet **Betalingsmåde**.
6. Udvid oversigtspanelet **Betalingsstandarder**.
7. Udvid oversigtspanelet **Bemyndigelser til Direct Debit**.
8. Klik på **Tilføj**.
9. Indtast eller vælg en værdi i feltet **Bankkonto**.
10. Indtast eller vælg en værdi i feltet **Kreditors bankkonto**.
11. Angiv antallet af betalinger, du forventer at behandle for denne bemyndigelse, i feltet **Betalingshyppighed**.
12. Klik på **OK**.
13. Klik på **Udskriv**.
14. Klik på **Bemyndigelsesrapport**.
15. Luk siden.
16. Klik på **Rediger**.
17. Angiv en dato i feltet **Dato for signatur**.
18. Klik på **Ja**.
19. Angiv den lokalitet, hvor bemyndigelsen blev signeret.
20. Klik på **OK**.
21. Luk siden.

## <a name="create-a-free-text-invoice-with-mandate"></a>Opret en fritekstfaktura med bemyndigelse
1. I **navigationsruden** skal du gå til **Moduler > Debitor > Fakturaer > Alle fritekstfakturaer**.
2. Klik på **Ny**.
3. Vælg den debitor, du har føjet mandatet til.
4. Indtast eller vælg en værdi i feltet **Id for bemyndigelse til Direct Debit**.

