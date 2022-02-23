---
title: Udlign en delvis debitorbetaling med rabatter på kreditnotaer
description: Denne artikel fører dig gennem et scenarie, hvor en kasserabat er anvendt på en kreditnota, når den oprindelige faktura også havde en kasserabat.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14564
ms.assetid: d9984cef-ddcf-46bd-816d-c01b8cc5cf48
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: da4353849b053ff94cf1fda7a03568438d0111da
ms.sourcegitcommit: 092ef6a45f515b38be2a4481abdbe7518a636f85
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4441730"
---
# <a name="settle-a-partial-customer-payment-that-has-discounts-on-credit-notes"></a>Udlign en delvis debitorbetaling med rabatter på kreditnotaer

[!include [banner](../includes/banner.md)]

Denne artikel fører dig gennem et scenarie, hvor en kasserabat er anvendt på en kreditnota, når den oprindelige faktura også havde en kasserabat. 

Fabrikam gør det muligt at anvende kasserabatter på delvise betalinger samt på kreditnotaer. En kasserabat kan anvendes på en kreditnota, når der udstedes en kreditnota for en faktura, som kunden fik en kasserabat på. I stedet for at oprette en kreditnota for det fulde beløb, kan du kreditere kundens saldo for et beløb, der udelukker den kasserabatprocent, kunden har fået. Udligningsparametrene er placeret på siden **Kreditorparametre**.

## <a name="invoice-and-credit-note"></a>Faktura og kreditnota
Debitor 4035 har en faktura på 1.000,00 og en kreditnota på 100,00. Hvert dokument har en rabat på 1 procent, hvis der betales inden 14 dage. Arnie kan se disse oplysninger på siden **Debitorposteringer**.

| Bilag    | Transaktionstype | Dato      | Faktura  | Beløb i transaktionsvalutadebet | Beløb i transaktionsvalutakredit | Saldo  | Valuta |
|------------|------------------|-----------|----------|--------------------------------------|---------------------------------------|----------|----------|
| FTI 10050  | Faktura          | 28-6-2015 | 10050    | 1.000,00                             |                                       | 1.000,00 | USD      |
| CCRN-10050 | Kreditnota      | 28-6-2015 | CR-10050 |                                      | 100,00                                | -100,00  | USD      |

## <a name="settle-a-credit-note-with-an-invoice"></a>Udlign en kreditnota med en faktura.
Fra siden **Kundetransaktioner** åbner Arnie siden **Udlign transaktioner**. Han kan bruge siden **Udlign transaktioner** til at udligne fakturaen og kreditnotaen. Som en del af udligningsprocessen får han datoer og beløb for kasserabatten. Han markerer de to dokumenter og klikker derefter på **Bogfør** for at udligne posteringer. Der er en rabat på -1,00 på kreditnotaen, fordi Fabrikam guver rabatter på kreditnotaer.

| Foretag afmærkning     | Anvend kasserabat | Bilag    | Konto | Dato      | Forfaldsdato  | Faktura  | Beløb i transaktionsvaluta | Valuta | Beløb, der skal udlignes |
|----------|-------------------|------------|---------|-----------|-----------|----------|--------------------------------|----------|------------------|
| Markeret | Almindelig            | FTI 10050  | 4035    | 28-6-2015 | 28-7-2015 | 10050    | 1.000,00                       | USD      | 990,00           |
| Valgt | Almindelig            | CCRN-10050 | 4035    | 28-6-2015 | 28-7-2015 | CR-10050 | -100,00                        | USD      | -99,00           |

Rabatoplysninger vises nederst på siden **Udlign transaktioner**.

- **Kasserabatdato**: 12-7-2015 
- **Kasserabatbeløb**: -1,00     
- **Anvend kasserabat**: Normal    
- **Medtaget kasserabat**: 0,00      
- **Kasserabatbeløb, der skal medtages**: -1,00     

Udligningen er på 100,00 og indeholder en betaling på 99,00 og en rabat på 1,00.



