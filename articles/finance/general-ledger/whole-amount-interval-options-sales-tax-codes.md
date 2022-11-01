---
title: Indstillinger for beregning af hele beløbet og intervaller for momskoder
description: I denne artikel beskrives indstillingerne for feltet Beregningsmåde for momskoder, og hvordan der beregnes moms for intervaller og hele beløb.
author: kailiang
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxData, TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 5624
ms.assetid: 96166db4-b7ca-470b-aeb7-0a66fe0554c4
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0b81780e60825021ad7a700d85257ba0f5a2447a
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715235"
---
# <a name="whole-amount-and-interval-calculation-options-for-sales-tax-codes"></a>Indstillinger for beregning af hele beløbet og intervaller for momskoder

[!include [banner](../includes/banner.md)]

Denne artikel beskriver indstillingerne for feltet **Beregningsmetode** til momskoder, og hvordan der beregnes moms for intervaller og hele beløb.

Du kan konfigurere, at en momskode skal beregnes på grundlag af hele beløbet eller et intervalbeløb. På siden **Momskoder** skal du bruge feltet **Beregningsmåde** på oversigtspanelet **Beregning** til at vælge beregningsmetoden for en momskode.
- Hele beløb – En momssats anvendes på hele det momspligtige beløb.
- Interval – Det momspligtige beløb er opdelt i dele, hvor hver del ligger inden for et beløbsinterval, der er underlagt en bestemt momssats. Den del af beløbet, der ligger inden for et bestemt interval, pålægges moms i henhold til momssatsen for dette interval. Momsen er summen af de momsbeløb, der beregnes for hvert beløbsinterval.
  > [!NOTE]                                                                                                                              
  > Indstillingen Interval er kun tilgængelig, når du vælger Linje i en feltet Beregningsmåde i området Moms på siden Finansparametre. 

Du angiver Intervaller på siden Momskodeværdier ved at angive minimum- og maksimumgrænsebeløb pr. momssats. For moms, der skal beregnes af alle momspligtige beløb, uanset den valgte beregningsmetode, skal intervallerne overholde følgende regler:
-   Første interval skal have en minimumgrænse på nul.
-   Det sidste interval, der skal have en maksimumgrænse på nul, angiver uendeligt.
-   Maksimumgrænsen for alle intervaller er minimumgrænsen for det næste interval.

Hvis et beløb er maksimumgrænsen for det forrige interval og minimumgrænsen for det næste interval, gælder momssatsen for det første interval for beløbet. Hvis et beløb ligger uden for de intervaller, der er defineret af de øvre og nedre grænser, anvendes momssatsen 0.

## <a name="example-whole-amount-method-of-calculation"></a>Eksempel: Beregningsmåden er hele beløbet
På siden Momskodeværdier er momssatserne defineret i følgende intervaller i:

| Minimumsgrænse     | Maksimumgrænse     | Momssats     |
|-------------------|-------------------|--------------|
| 0,00              | 50,00             | 30 %          |
| 50,00             | 100,00            | 20 %          |
| 100,00            | 0,00              | 10 %          |

Momsen beregnes af hele det momspligtige beløb.

| Momspligtigt beløb (pris) | Kalkulation    | Moms |
|------------------------|----------------|-----------|
| 35,00                  | 35,00 \* 0,30  | 10,50     |
| 50,00                  | 50,00 \* 0,30  | 15,00     |
| 85,00                  | 85,00 \* 0,20  | 17,00     |
| 305,00                 | 305,00 \* 0,10 | 30,50     |

## <a name="example-interval-method-of-calculation"></a>Eksempel: Beregningsmåde er interval
På siden Værdier er momssatserne defineret i følgende intervaller:

| Minimumsgrænse     | Maksimumgrænse     | Momssats     |
|-------------------|-------------------|--------------|
| 0,00              | 50,00             | 30 %          |
| 50,00             | 100,00            | 20 %          |
| 100,00            | 0,00              | 10 %          |

Momsen er summen af de momsbeløb, der beregnes for hvert beløbsinterval.

| Momspligtigt beløb (pris) | Kalkulation                                                               | Moms |
|------------------------|---------------------------------------------------------------------------|-----------|
| 35,00                  | 35,00 \* 0,30                                                             | 10,50     |
| 50,00                  | 50,00 \* 0,30                                                             | 15,00     |
| 85,00                  | (50,00 \* 0,30 = 15,00) + (35,00 \* 0,20 = 7,00)                          | 22,00     |
| 305,00                 | (50,00 \* 0,30 = 15,00) + (50,00 \* 0,20 = 10,00) + (205 \* 0,10 = 20,50) | 45.50     |



Du kan finde flere oplysninger i [Momssatser baseret på beregningsgrundlaget og felter for beregningsmetoder](marginal-base-field.md).







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
