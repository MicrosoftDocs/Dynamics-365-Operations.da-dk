---
title: 125 % saldoafskrivning
description: Denne artikel indeholder en oversigt over afskrivningsmetoden 125 % saldoafskrivning.
author: saraschi2
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13871
ms.assetid: 3abc263e-59d6-4f1a-986d-1be388948bd3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8ec88d799c44e035b6490861383557f8c3beda41
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="125-percent-reducing-balance-depreciation"></a>125 % saldoafskrivning

[!include[banner](../includes/banner.md)]


Denne artikel indeholder en oversigt over afskrivningsmetoden 125 % saldoafskrivning.

Når du opretter en afskrivningsprofil for et anlægsaktiv og vælger **125 % saldoværdi** i feltet **Metode** på siden **Afskrivningsprofiler**, bliver de anlægsaktiver, der er tildelt afskrivningsprofilen, afskrevet med den samme procent i hver afskrivningsperiode. Denne procentdel beregnes på basis af aktivets levetid. Hvis et aktiv f.eks. har en levetid på fem år, beregnes procentdelen som 25 % (125 % ÷ 5).

Hvis du vil oprette en 125 % saldoafskrivning, skal du også foretage valg i feltet **Afskrivningsår** og feltet **Periodefrekvens** på siden **Afskrivningsprofiler**. Hvilke indstillinger , der er tilgængelige i feltet **Periodefrekvens**, varierer, afhængigt af den værdi der er valgt i feltet **Afskrivningsår**.

## <a name="select-a-depreciation-year"></a>Vælge et afskrivningsår
Du kan vælge enten **Kalender** eller **Regnskabsår** i feltet **Afskrivningsår** på siden **Afskrivningsprofiler**. Standardværdien er **Kalender**. 

Dit valg bestemmer, hvad der kan vælges i feltet **Periodefrekvens**. Dette felt definerer datoer og beløb for periodiseringen af afskrivningsposteringerne i hele kalenderåret.

### <a name="calendar"></a>Kalender

Du kan vælge at beholde standardværdien i feltet **Afskrivningsår**, **Kalender**. 

Indstillingen **Kalender** opdaterer afskrivningsgrundlaget d. 1. januar hvert år. Afskrivningsgrundlaget er typisk bogført nettoværdi minus scrapværdi. I eksemplerne senere i dette emne er afskrivningsgrundlaget tælleren i det første udtryk i beregningen i beregningskolonnen. 

Hvis du vælger **Kalender** som afskrivningsår, er følgende indstillinger tilgængelige i feltet **Periodefrekvens**:

-   **Årligt** bogfører et beløb d. 31. december.
-   **Månedligt** bogfører et månedligt beløb sidst i hver kalendermåned.
-   **Kvartalsvis** bogfører et kvartalsmæssigt beløb sidst i hvert kalenderkvartal (d. 31. marts, d. 30. juni, d. 30. september og d. 31. december).
-   **Halvårlig** bogfører et halvårligt beløb sidst i kalenderhalvåret (d. 30. juni og d. 31. december).
-   **Daglig** bogfører afskrivningsbeløbet for afskrivningsmetoden dagligt ved hjælp af en postering for hver dag.

### <a name="fiscal"></a>Regnskabsår

Hvis du vælger **Regnskabsår** i feltet **Afskrivningsår**, beregnes 125 % saldoafskrivning på grundlag af regnskabsåret for den regnskabskalender, der er angivet for modellen eller den regnskabskalender, der er valgt på siden **Finans**. Regnskabskalendere oprettes på siden **Regnskabskalendere**. 

I forbindelse med regnskabsåret fra d. 1. juli til og med d. 30. juni starter afskrivningsberegningen f.eks. d. 1. juli. Regnskabsåret kan være længere eller kortere end 12 måneder. Afskrivningen justeres automatisk for hver periode, og længden på det næste regnskabsår bestemmes af opsætningen af perioder på siden **Regnskabskalendere**. 

Hvis du vælger **Regnskabsår** som afskrivningsår, er følgende indstillinger tilgængelige i feltet **Periodefrekvens**:

-   **Årligt** bogfører det samlede afskrivningsbeløb, der beregnes for regnskabsåret som ét beløb på den sidste dag i regnskabsåret.
-   **Regnskabsperiode** bogfører det samlede afskrivningsbeløb, der er beregnet for regnskabsåret. Dette beløb periodiseres for de regnskabsperioder, der er defineret på siden **Regnskabskalendere**.

## <a name="example-of-125-reducing-balance-depreciation"></a>Eksempel på en 125 % saldoafskrivning
|                                |        |
|--------------------------------|--------|
| Anskaffelsesomkostning               | 11.000 |
| Restværdi                  | 1.000  |
| Afskrivningsgrundlag              | 10.000 |
| Levetid i år             | 5      |
| Årlig afskrivningsprocent | 25 %    |

Metoden med 125 % saldoafskrivning dividerer de 125 % med levetiden i år. Denne procent ganges med aktivets bogførte nettoværdi for at beregne årets afskrivningsbeløb.

| Periode | Beregning af det årlige afskrivningsbeløb | Bogført værdi                    | Den bogførte nettoværdi ved årets afslutning |
|--------|-----------------------------------------------|-------------------------------|---------------------------------------|
| År 1 | (11.000-1.000) x 25 % = 2.500                | (11.000-2.500) = 8.500      | (11.000-1.000-2.500) = 7.500      |
| År 2 | 7.500 × 25 % = 1.875                           | (8.500-1.875) = 6.625       | (7.500-1.875) = 5.625               |
| År 3 | 5.625 × 25 % = 1.406,25                        | (6.625-1.406,25) = 5.218,75 | (5.625-1.406,25) = 4.218,75         |

> [!NOTE] 
> Når det beløb, der er beregnet ved hjælp af metoden til 125 % saldoafskrivning bliver mindre end det beløb, der skal beregnes ved hjælp af den lineære metode, er der en konvertering til lineær afskrivningsmetode for resten af levetiden.




