---
title: Det maksimale antal decimaler for enheden til lagerenhed er 0
description: 'Når du forsøger at bogføre en lagertransaktion eller en lagerreservation, får du vist følgende fejlmeddelelse: "Maks. antal decimaler for lagerenheden er 0".'
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 9dec198e2d77efd2253c80e14d15791cc37f88e1
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475943"
---
# <a name="maximum-number-of-decimals-for-the-stock-keeping-unit-is-0"></a>Det maksimale antal decimaler for enheden til lagerenhed er 0


## <a name="symptoms"></a>Symptomer

Når du forsøger at bogføre en lagertransaktion eller en lagerreservation, vises følgende fejlmeddelelse:

> Det maksimale antal decimaler for enheden til lagerenhed er 0.

Denne fejl opstår, når lagertransaktionsantallet angives som en decimalværdi, der er under det præcisionsniveau, som feltet understøtter. Der er f.eks. angivet et antal på *0,5* for en lagertransaktion, men antal understøttes kun i heltal. Derfor skal værdien være *1* i stedet for *0,5*.

## <a name="resolution"></a>Løsning

1. Kør følgende script på SQL Server-forekomsten for at afrunde antallet i lagertransaktionerne. Dette script retter værdier i tabellen **InventTrans**.

    ```sql
    update it set it.QTY = round(it.qty, decimalPrecisionValue) from inventtrans it where it.DATAAREAID='XXXX' and it.PARTITION=XXXXXX and it.qty <> round(it.qty, decimalPrecisionValue) and exists (select 'x' from INVENTTABLEMODULE a, unitofmeasure b where  a.unitid =b.SYMBOL and a.partition=it.partition and a.PARTITION=b.PARTITION and  MODULETYPE =0 and  b.DECIMALPRECISION=decimalPrecisionValue and a.DATAAREAID='XXXX' and a.ITEMID =it.ITEMID and it.DATAAREAID=a.DATAAREAID)
    ```

1. Kør en konsistenskontrol beholdningen, hvor indstillingen **ret fejl** er aktiveret. Denne kontrol retter værdier i tabellen **InventSum**.

> [!IMPORTANT]
> Det anbefales på det kraftigste, at du nøje redigerer scriptet i dit miljø, tester det i et testmiljø og derefter kontrollerer de resulterende data, før du kører scriptet i et produktionsmiljø.
