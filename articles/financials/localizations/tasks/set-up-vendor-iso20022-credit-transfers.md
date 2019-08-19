---
title: Konfigurere kreditorer og kreditorbankkonti for ISO20022-kreditoverførsler
description: Denne fremgangsmåde viser, hvordan du konfigurerer kreditoren og de kreditorspecifikke bankkontooplysninger, der kræves til generering af ISO20022-kreditoroverførsel eller andre betalingsfiler.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab8c52b9b457505c2cf2bfca46cb938e73c0142e
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/02/2019
ms.locfileid: "1848667"
---
# <a name="set-up-vendors-and-vendor-bank-accounts-for-iso20022-credit-transfers"></a>Konfigurere kreditorer og kreditorbankkonti for ISO20022-kreditoverførsler

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

