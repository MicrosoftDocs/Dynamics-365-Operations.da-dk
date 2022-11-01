---
title: Kasserabatter
description: Kasserabatter konfigureres og deles for kreditor og debitor.  Den tilgængelige kasserabat kan defineres på debitorfakturaen eller kreditorfakturaen og benyttes, hvis fakturaen betales inden kasserabatdatoen.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CashDisc
audience: Application User
ms.reviewer: kfend
ms.custom: 3741
ms.assetid: c25f9d85-2702-46aa-8e61-0b4886e069b3
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1db95720d56cc538f2d702137889467a9892d99c
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715175"
---
# <a name="cash-discounts"></a>Kasserabatter

[!include [banner](../includes/banner.md)]

Kasserabatter konfigureres og deles for kreditor og debitor.  Den tilgængelige kasserabat kan defineres på debitorfakturaen eller kreditorfakturaen og benyttes, hvis fakturaen betales inden kasserabatdatoen. 

## <a name="cash-discounts"></a>Kasserabatter

Kasserabatter for både debitorer eller kreditorer kan oprettes på siden Kasserabatter. Du kan også bruge feltet Næste rabatkode til at definere en række kasserabatter, der følger efter hinanden, efterhånden som tidligere kasserabatdatoer udløber. Du kan finde flere oplysninger i "Eksempel: En række kasserabatter" senere i denne artikel. Hvis fakturaen, kreditposteringen (enten en betaling eller en kreditnota) eller begge angives en anden valuta end regnskabsvalutaen for den juridiske enhed, beregnes kasserabatten ved hjælp af valutakursen baseret på datoen for betalingen eller kreditnotaen. Hvis fakturaen eller kreditdokumentet er angivet for forskellige juridiske enheder, og hvis regnskabsvalutaen for de juridiske enheder er forskellig, tages valutakursen fra den juridiske enhed for fakturaen på datoen for kreditdokumentet. Du kan finde flere oplysninger i "Eksempel: Valutakurser for kasserabatter" senere i denne artikel.

## <a name="defaulting-order-of-cash-discount-main-account"></a>Standardrækkefølge af hovedkonto for kasserabat

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

> [!NOTE]
> Hvis indstillingen Beregn kasserabatter for delvise betalinger er valgt på siden Debitorparametre eller siden Kreditorparametre, bruges den valutakurs, der er gældende på datoen for hver delvise betaling. 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
