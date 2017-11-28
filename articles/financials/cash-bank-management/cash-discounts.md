---
title: Kasserabatter
description: "Kasserabatter konfigureres og deles for kreditor og debitor.  Den tilgængelige kasserabat kan defineres på debitorfakturaen eller kreditorfakturaen og benyttes, hvis fakturaen betales inden kasserabatdatoen."
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CashDisc
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3741
ms.assetid: c25f9d85-2702-46aa-8e61-0b4886e069b3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 9960af8c4961a42e7e829077da40bcbbf3bc71c2
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="cash-discounts"></a>Kasserabatter

[!include[banner](../includes/banner.md)]


Kasserabatter konfigureres og deles for kreditor og debitor.  Den tilgængelige kasserabat kan defineres på debitorfakturaen eller kreditorfakturaen og benyttes, hvis fakturaen betales inden kasserabatdatoen. 

<a name="cash-discounts"></a>Kasserabatter
--------------

Kasserabatter for både debitorer eller kreditorer kan oprettes på siden Kasserabatter. Du kan også bruge feltet Næste rabatkode til at definere en række kasserabatter, der følger efter hinanden, efterhånden som tidligere kasserabatdatoer udløber. Du kan finde flere oplysninger i "Eksempel: En række kasserabatter" senere i dette emne. Hvis fakturaen, kreditposteringen (enten en betaling eller en kreditnota) eller begge angives en anden valuta end regnskabsvalutaen for den juridiske enhed, beregnes kasserabatten ved hjælp af valutakursen baseret på datoen for betalingen eller kreditnotaen. Hvis fakturaen eller kreditdokumentet er angivet for forskellige juridiske enheder, og hvis regnskabsvalutaen for de juridiske enheder er forskellig, tages valutakursen fra den juridiske enhed for fakturaen på datoen for kreditdokumentet. Du kan finde flere oplysninger i "Eksempel: Valutakurser for kasserabatter" senere i dette emne.
Standardrækkefølge af hovedkonto for kasserabat
----------------------------------------------

Hvis en faktura udlignes inden for det tidsrum, der medfører en kasserabat, bogføres kasserabatten automatisk på en hovedkonto for kasserabatter i overensstemmelse med følgende standardprioritet:
1.  Den hovedkonto, der er angivet i feltet Alternativ kasserabatkonto på debitorsiden Udlign åbne posteringer eller kreditorsiden Udlign åbne posteringer.
2.  Den hovedkonto, der er angivet i feltet Debitor, kasserabat eller feltet Kreditor kasserabat i den finanskonteringsgruppe, der er knyttet til fakturaens momskode. Konfigurer finanskonteringsgrupper på siden Finanskonteringsgrupper, og tildel dem til momskoder på siden Momskoder.
3.  Hovedkonteringsgruppen på siden Kasserabatter i feltet Hovedkonto til debitorrabatter eller feltet Hovedkonto til kreditorrabatter for kasserabatkoden, der er anført på den udlignede faktura.
4.  Hovedkontoen til kasserabatter, som defineret på siden Konti til automatiske posteringer.

## <a name="example-series-of-cash-discounts"></a> Eksempel: En række kasserabatter
Opret tre kasserabatkoder på følgende måde:
-   Kode 5D10% – En kasserabat på 10 %, når beløbet betales inden for fem dage.
-   Kode 10D5% – En kasserabat på 5 %, når beløbet betales inden for 10 dage.
-   Kode 14D2% – En kasserabat på 2 %, når beløbet betales inden for 14 dage.

I feltet Næste rabatkode:
-   Vælg 10D5% for koden 5D10%.
-   Vælg 14D2% for koden 10D5%.
-   For koden 14D2% skal du lade feltet Næste rabatkode være tomt.

De tre kasserabatter følger efter hinanden, når betalingsdatoen overskrider den tidligere kasserabatdato på fakturaen. Der gives kun én kasserabat, når fakturaen betales, ud fra hvilken dato for kasserabat, der opfyldes i rækkefølgen af kasserabatter.

## <a name="example-exchange-rates-for-cash-discounts"></a> Eksempel: Valutakurser for kasserabatter
Din juridiske enheds regnskabsvaluta i EUR og de følgende valutakurser, der er angivet for USD:
-   1. februar = 110
-   1. marts = 80

En faktura på 1000 USD med kasserabatbetingelserne for 20D2% bogføres den 15. februar. Beløbet i regnskabsvalutaen for fakturaen er 1100 EUR. Der foretages en betaling på 980 USD for fakturaen den 1. marts. Kasserabatbeløbet er 20 USD. Regnskabsvalutabeløbet for betalingen er 784 EUR. Regnskabsvalutabeløbet for kasserabatten beregnes ved hjælp af valutakursen for 1. marts: 20 \* 80/100 = 16 EUR.
| **Bemærk!**                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Hvis indstillingen Beregn kasserabatter for delvise betalinger er valgt på siden Debitorparametre eller siden Kreditorparametre, bruges den valutakurs, der er gældende på datoen for hver delvise betaling. |

 
=

 




