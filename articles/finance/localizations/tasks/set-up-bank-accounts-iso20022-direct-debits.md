---
title: Konfigurere debitorer og debitorbankkonti for direkte ISO20022-debiteringer
description: Denne opgave fører dig gennem oprettelse af en debitorbankkonto og en bemyndigelsen til direkte kundedebitering, som er nødvendige for at generere en kundebetalingsfil som ISO20022 Direct Debit.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, CustDirectDebitMandate, BankAccountTableLookUp,  LogisticsAddressCityLookup
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 595e89faa1e24ca937d399994e15ce53e3f5308b1c6fd7f43e4e831e70c15ad8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6736861"
---
# <a name="set-up-customers-and-customer-bank-accounts-for-iso20022-direct-debits"></a>Konfigurere debitorer og debitorbankkonti for direkte ISO20022-debiteringer

[!include [banner](../../includes/banner.md)]

Denne opgave fører dig gennem oprettelse af en debitorbankkonto og en bemyndigelsen til direkte kundedebitering, som er nødvendige for at generere en kundebetalingsfil som ISO20022 Direct Debit. Afhængigt af de formater for debitorbetalinger, der er konfigureret, kræves der yderligere oplysninger, der ikke er dækket i denne procedure, for en kunde eller en debitorbankkonto. 

Denne opgave blev oprettet ved hjælp af demodatafirmaet DEMF med primær adresse for en juridisk enhed i Tyskland.



Det er den fjerde procedure af fem, der illustrerer kundens betalingsproces ved hjælp af konfigurationer af elektronisk rapportering.


## <a name="set-up-a-customer-bank-account"></a>Konfigurer en debitorbankkonto
1. Gå til Debitor > Kunder > Alle kunder.
2. Brug Quick Filter til at finde poster. Filtrer f.eks. efter feltet Konto med værdien "DE-010".
3. Klik op linket i den valgte række på listen.
4. Klik på Kunde i handlingsruden.
5. Klik på Bankkonti.
6. Klik på Ny.
7. Skriv en værdi i feltet Bankkonto.
8. Skriv en værdi i feltet Navn.
    * Du kan f.eks. skrive 'EUR bank'.  
9. Indtast eller vælg en værdi i feltet Bankgrupper.
10. Skriv en værdi i feltet IBAN.
    * Skriv f.eks. 'DE36200400000628808808'.  
11. Indtast en værdi i feltet SWIFT-kode.
    * For eksempel: Angiv "COBADEFFXXX".  Bemærk, at SWIFT\BIC ikke er påkrævet for mange betalingsformater, men det anbefales at få det registreret for en bankkonto.  
12. Klik på Gem.
13. Luk siden.
14. Klik på Rediger.
15. Udvid sektionen Betalingsstandarder.
16. Indtast eller vælg en værdi i feltet Bankkonto.

## <a name="add-a-direct-debit-mandate"></a>Tilføj en bemyndigelse til direkte debet
1. Udvid sektionen Bemyndigelser til Direct Debit.
2. Klik på Tilføj.
3. Indtast eller vælg en værdi i feltet Kreditors bankkonto.
    * Vælg for eksempel DEMF OPER.  
4. Angiv en dato i feltet Dato for signatur.
5. Klik på Ja for at bekræfte datoopdateringen.
6. Indtast eller vælg en værdi i feltet Sted for signatur.
7. Angiv et tal i feltet Forventet antal betalinger.
8. Klik på OK.
9. Klik på Gem.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]