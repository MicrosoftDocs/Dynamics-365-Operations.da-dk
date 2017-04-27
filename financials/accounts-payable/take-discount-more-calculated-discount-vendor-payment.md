---
title: "Brug en rabat, der er større end den beregnede rabat, til en kreditorbetaling"
description: "Denne artikel fører dig gennem en situation, hvor en kasserabat anvendes for et beløb, der er større end den rabat, der oprindeligt blev brugt på fakturaen. Denne situation kan opstå, hvis en organisation har en aftale med leverandøren om at betale et mindre beløb på fakturaen."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 22ba73681faa509a5144517163cc173a1267a534
ms.lasthandoff: 03/31/2017


---

# <a name="take-a-discount-that-is-more-than-the-calculated-discount-for-a-vendor-payment"></a>Brug en rabat, der er større end den beregnede rabat, til en kreditorbetaling

[!include[banner](../includes/banner.md)]


Denne artikel fører dig gennem en situation, hvor en kasserabat anvendes for et beløb, der er større end den rabat, der oprindeligt blev brugt på fakturaen. Denne situation kan opstå, hvis en organisation har en aftale med leverandøren om at betale et mindre beløb på fakturaen. 

Leverandøren 3051 giver Fabrikam en kasserabat på 4 %, hvis en faktura betales i løbet af syv dage. Den 29. juni angiver April en faktura på 1.000,00. Kreditoren tillader, at April medtager en rabat på 60,00 i stedet for standardrabatten på 40,00, der er tilgængelig for denne faktura. April registrerer en engangsbetaling ved hjælp af kreditorbetalingskladden. Hun angiver kreditoren for betalingen og åbner derefter siden **Udlign transaktioner**. Hun markerer fakturaen og ændrer værdien i feltet **Kasserabatbeløb** til **60,00**.
| Foretag afmærkning     | Anvend kasserabat | Bilag   | Konto | Dato      | Forfaldsdato  | Faktura | Beløb i transaktionsvaluta | Valuta | Beløb, der skal udlignes |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Markeret | Almindelig            | Fak-10040 | 3051    | 29-6-2015 | 29-7-2015 | 10040   | 1.000,00                       | USD      | 940,00           |

Rabatoplysninger vises nederst på siden **Udlign transaktioner**.
|                              |           |
|------------------------------|-----------|
| Kasserabatdato           | 12-7-2015 |
| Kasserabatbeløb         | 60,00     |
| Anvend kasserabat            | Almindelig    |
| Medtaget kasserabat          | 0,00      |
| Kasserabatbeløb, der skal medtages | 60,00     |

Derefter bogfører April betalingskladden. Fakturaen udlignes fuldt ud med en betaling på 940,00 og en rabat på 60,00.




