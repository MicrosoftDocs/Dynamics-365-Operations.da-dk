---
title: Konfigurere kreditorer og kreditorbankkonti for ISO20022-kreditoverførsler
description: Denne fremgangsmåde viser, hvordan du konfigurerer kreditoren og de kreditorspecifikke bankkontooplysninger, der kræves til generering af ISO20022-kreditoroverførsel eller andre betalingsfiler.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f7a901591f9f3d1a892c29f92e59dc96c1f172143cae6bec571da33b4a50d274
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723713"
---
# <a name="set-up-vendors-and-vendor-bank-accounts-for-iso20022-credit-transfers"></a>Konfigurere kreditorer og kreditorbankkonti for ISO20022-kreditoverførsler

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåde viser, hvordan du konfigurerer kreditoren og de kreditorspecifikke bankkontooplysninger, der kræves til generering af ISO20022-kreditoroverførsel eller andre betalingsfiler. 

Det demodatafirma, der bruges til at oprette denne procedure, er DEMF.
Det er den fjerde procedure af fem, der illustrerer kreditors betalingsproces ved hjælp af konfigurationer af elektronisk rapportering. Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.


## <a name="set-up-bank-details"></a>Konfigurer bankoplysninger
1. Gå til Kreditor > Kreditorer > Alle kreditorer.
2. Brug Quick Filter til at finde poster. Filtrer f.eks. efter feltet Kreditorkonto med værdien "DE-001".
3. Klik på DE-001 åbne kreditoroplysninger.
4. Klik på Kreditor i handlingsruden.
5. Klik på Bankkonti.
6. Klik på Rediger.
    * Hvis der ikke er nogen bankkonto, skal du oprette en ny.  
7. Skriv "COBADEFFXXX" i feltet SWIFT-kode.
8. Angiv "DE36200400000628808808" i feltet IBAN.
9. Luk siden.

## <a name="set-up-a-method-of-payment-for-the-vendor"></a>Konfigurer en betalingsmåde for kreditoren
1. Klik på Rediger.
2. Vis eller skjul sektionen Betaling.
3. Klik på rullelisten i feltet Betalingsmåde for at åbne opslaget.
4. Klik på linket i rækken SEPA CT på listen.
5. Klik på Gem.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]