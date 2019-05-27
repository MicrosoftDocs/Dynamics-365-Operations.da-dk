---
title: Konfigurere firmas bankkonti for ISO20022-kreditoverførsler
description: Denne procedure viser, hvordan du konfigurerer de firmaspecifikke bankkontooplysninger, der kræves til generering af SEPA-betalingsfilen.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, OMLegalEntity, BankAccountTableLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2a84408ea24e4221b041782b681c2a2bf1bd8436
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552417"
---
# <a name="set-up-company-bank-accounts-for-iso20022-credit-transfers"></a>Konfigurere firmas bankkonti for ISO20022-kreditoverførsler

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du konfigurerer de firmaspecifikke bankkontooplysninger, der kræves til generering af SEPA-betalingsfilen. Du kan angive oplysninger, der kræves for at oprette ISO 20022-kreditoverførselsformatet, men afhængigt af formatet kan der være andre oplysninger, der kræves, såsom firma-id eller sorteringskode. 

Det demodatafirma, der bruges til at oprette denne procedure, er DEMF.

Det er den anden procedure af fem, der illustrerer kreditors betalingsproces ved hjælp af konfigurationer af elektronisk rapportering. Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.


## <a name="set-up-iban-and-swift-code"></a>Konfigurer IBAN- og SWIFT-kode
1. Gå til Kontant- og bankstyring > Bankkonti.
2. Brug Quick Filter til at filtrere på feltet Bankkonto med værdien "DEMF OPER".
3. Klik på DEMF OPER for at åbne bankkontooplysninger.
4. Klik på Rediger.
5. Udvid sektionen Yderligere identifikation.
6. Angiv "DE89370400440532013000" i feltet IBAN.
7. Skriv "DEUTDEFF" i feltet SWIFT-kode.
    * Bemærk, at SWIFT\BIC ikke er påkrævet for mange betalingsformater, men det anbefales at få det registreret for en bankkonto.  
8. Klik på Gem.

## <a name="set-up-bank-account-for-the-legal-entity"></a>Konfigurer den juridiske enheds bankkonto
1. Gå til Virksomhedsadministration > Organisationer > Juridiske enheder.
2. Klik på Rediger.
3. Udvid sektionen Bankkontooplysninger.
4. Indtast eller vælg en værdi i feltet Bankkonto.
5. Klik på Gem.

