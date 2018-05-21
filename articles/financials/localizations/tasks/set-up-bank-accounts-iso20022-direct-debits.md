--- 
title: Konfigurere debitorer og debitorbankkonti for direkte ISO20022-debiteringer
description: "Denne opgave fører dig gennem oprettelse af en debitorbankkonto og en bemyndigelsen til direkte kundedebitering, som er nødvendige for at generere en kundebetalingsfil som ISO20022 Direct Debit."
author: mrolecki
manager: AnnBe
ms.date: 10/31/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 22fadf126dfa884520bc2fe6f94bc3fe3b612f77
ms.openlocfilehash: 86c3f62e17d4955c12d09b512624eb5f576a9cd3
ms.contentlocale: da-dk
ms.lasthandoff: 10/31/2017

---
# <a name="set-up-customers-and-customer-bank-accounts-for-iso20022-direct-debits"></a>Konfigurere debitorer og debitorbankkonti for direkte ISO20022-debiteringer

[!include [task guide banner](../../includes/task-guide-banner.md)]

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


