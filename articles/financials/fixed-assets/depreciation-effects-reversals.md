---
title: "Virkninger af afskrivninger med tilbageførsler"
description: "I denne artikel beskrives mulige konsekvenser af tilbageførsel af en anlægsaktivtransaktion."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2961
ms.assetid: 63a3ac92-c321-4379-a86a-b1b14915f340
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: d061ad8df477943259bff853d032c3df620e0b27
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017

---

# <a name="depreciation-effects-with-reversals"></a>Virkninger af afskrivninger med tilbageførsler

[!include[banner](../includes/banner.md)]


I denne artikel beskrives mulige konsekvenser af tilbageførsel af en anlægsaktivtransaktion. 

Du kan tilbageføre anlægsaktivposteringer og de transaktioner, der er knyttet til et anlægsaktiv. Du kan også annullere en tilbageført postering. 

Du kan tilbageføre eller tilbagekalde en transaktion, der ikke er den seneste transaktion, som er bogført i modellen for aktivet. Du skal først afgøre, om der er blevet bogført nogen afskrivningsposteringer efter den postering, du vil tilbageføre. Det skyldes, at afskrivning ikke genberegnes, når du tilbagefører en postering. Afskrivningen vil derfor ofte blive overvurderet eller undervurderet efter tilbageførslen, som det fremgår af eksemplerne. 

Hvis du vil sikre, at afskrivningen er korrekt, når du tilbagefører en postering, skal du ikke fortsætte med tilbageførslen, hvis du modtager en besked om, at afskrivningen ikke genberegnes. Du skal i stedet først tilbageføre den afskrivningspostering, der blev bogført efter den postering, du prøvede at tilbageføre, og derefter fortsætte med tilbageførslen. Du bliver ikke advaret om genberegning af afskrivningen, og du kan fortsætte med tilbageførslen. 

I nedenstående eksempler vises de beregninger, der forekommer, hvis du fortsætter efter advarslen uden først at tilbageføre afskrivningsposteringerne.

## <a name="example-1-depreciation-is-overstated"></a>Eksempel 1: Afskrivningen overvurderes
Der er konfigureret et aktiv med en levetid på 5 år og lineær afskrivning (60 afskrivningsperioder). I dette eksempel overvurderes afskrivningen.
#### <a name="asset-transaction-history"></a>Posteringshistorik for aktiv

| Dato       | Posttype                                                          | Beløb                                    |
|------------|---------------------------------------------------------------------------|-------------------------------------------|
| 1. januar  | Anskaffelse                                                               | 59.000,00                                 |
| 1. januar  | Anskaffelsesregulering                                                    | 1.000,00                                  |
| 31. januar | Afskrivning (oprettet ved hjælp af et forslag for én afskrivningsperiode) | 1.000,00Beregning: Bogført værdi (59.000 + 1.000) / Antal resterende afskrivningsperioder (60) |

#### <a name="reversal-action"></a>Tilbageførselshandling

| Dato      | Transaktionstype                | Beløb    |
|-----------|---------------------------------|-----------|
| 1. januar | Tilbageførsel af anskaffelsesregulering | –1.000,00 |

#### <a name="depreciation-effect"></a>Virkning af afskrivning

| Dato        | Transaktionstype        | Beløb                                                                                |
|-------------|-------------------------|---------------------------------------------------------------------------------------|
| 28. februar | Afskrivning (forslag) | 983,05Beregning: Bogført værdi (59.000 - 1.000 afskrivning) / Antal resterende afskrivningsperioder (59) |

Afskrivningen er overvurderet med 16,95 (1.000 - 983,05).

## <a name="example-2-depreciation-is-understated"></a>Eksempel 2: Afskrivningen undervurderes
Der er konfigureret et aktiv med en levetid på 5 år og lineær afskrivning (60 afskrivningsperioder). I dette eksempel undervurderes afskrivningen.
#### <a name="asset-transaction-history"></a>Posteringshistorik for aktiv

| Dato       | Posteringstype                                                          | Beløb                                      |
|------------|---------------------------------------------------------------------------|---------------------------------------------|
| 1. januar  | Anskaffelse                                                               | 59.000,00                                   |
| 1. januar  | Nedskrivningsregulering                                                     | 1.000,00                                    |
| 31. januar | Afskrivning (oprettet ved hjælp af et forslag for én afskrivningsperiode) | 966,67Beregning: Bogført værdi (59.000 - 1.000) / Antal resterende afskrivningsperioder (60) |

#### <a name="reversal-action"></a>Tilbageførselshandling

| Dato      | Transaktionstype               | Beløb    |
|-----------|--------------------------------|-----------|
| 1. januar | Tilbageførsel af nedskrivningsregulering | –1.000,00 |

#### <a name="depreciation-effect"></a>Virkning af afskrivning

| Dato        | Transaktionstype        | Beløb                                                                                       |
|-------------|-------------------------|----------------------------------------------------------------------------------------------|
| 28. februar | Afskrivning (forslag) | 983,62Beregning: Bogført værdi (59.000 - 966,67 afskrivning) / Antal resterende afskrivningsperioder (59) |

Afskrivningen er undervurderet med 16,95 (983,62 - 966,67).



<a name="see-also"></a>Se også
--------

[Afskrivning af anlægsaktiv](fixed-asset-depreciation.md)



