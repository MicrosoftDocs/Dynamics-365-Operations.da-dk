---
title: Konfigurere firmas bankkonti for direkte ISO20022-debiteringer
description: Denne opgave fører dig gennem oprettelse af firmaspecifikke bankkontooplysninger, der skal bruges til generering af kundebetalingsfiler.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankAccountTable, OMLegalEntity, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a0f8ac369bb6b9a7a0f21c23aaddab2601ae3f8f37e2427cbb10b5509a7a2f23
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768711"
---
# <a name="set-up-company-bank-accounts-for-iso20022-direct-debits"></a>Konfigurere firmas bankkonti for direkte ISO20022-debiteringer

[!include [banner](../../includes/banner.md)]

Denne opgave fører dig gennem oprettelse af firmaspecifikke bankkontooplysninger, der skal bruges til generering af kundebetalingsfiler. Denne procedure bruger formatet ISO 20022 for Direct Debit som eksempel. Andre formater kan kræve yderligere konfigurationsoplysninger som firma-id eller sorteringskode.



Denne opgave blev oprettet ved hjælp af demodatafirmaet DEMF.



Det er den anden procedure af fem, der illustrerer kundens betalingsproces ved hjælp af konfigurationer af elektronisk rapportering.


## <a name="set-up-the-iban-and-swift-codes"></a>Konfigurer IBAN- og SWIFT-koderne.
1. Gå til Kontant- og bankstyring > Bankkonti.
2. Brug Quick Filter til at filtrere på feltet Bankkonto med værdien "DEMF OPER".
3. Klik op linket i den valgte række på listen.
    * For eksempel: Klik på "DEMF OPER" for at åbne bankkontooplysninger.  
4. Klik på Rediger.
5. Udvid eller skjul sektionen Yderligere identifikation.
6. Skriv en værdi i feltet IBAN.
    * Skriv f.eks. 'DE89370400440532013000'.  
7. Indtast en værdi i feltet SWIFT-kode.
    * For eksempel: Angiv "DEUTDEFF".    Bemærk, at SWIFT\BIC ikke er påkrævet for mange betalingsformater, men det anbefales at få det registreret for en bankkonto.  
8. Klik på Gem.

## <a name="set-up-a-bank-account-for-the-legal-entity"></a>Konfigurer en bankkonto for den juridiske enhed
1. Gå til Virksomhedsadministration > Organisationer > Juridiske enheder.
2. Klik på Rediger.
3. Udvid eller skjul sektionen Bankkontooplysninger.
4. Klik på rullelisten i feltet Bankkonto for at åbne opslaget.
5. Klik op linket i den valgte række på listen.
    * For eksempel: Vælg "DEMF OPER"-bankkonto.  
6. Klik på Gem.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]