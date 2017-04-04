---
title: 200 % saldoafskrivning
description: Denne artikel indeholder en oversigt over afskrivningsmetoden 200 % saldoafskrivning.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13951
ms.assetid: 69b4e010-7683-4dc2-8a06-6d572f37e903
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 8e89a57dda8f2d392483ed13c686ea97b74926b0
ms.openlocfilehash: 617d643517f4c40d6e870d1e7e676b0be28092dd
ms.lasthandoff: 03/31/2017


---

# <a name="200-percent-reducing-balance-depreciation"></a>200 % saldoafskrivning

Denne artikel indeholder en oversigt over afskrivningsmetoden 200 % saldoafskrivning.

Når du opretter en afskrivningsprofil til et anlægsaktiv og vælger **200% saldoværdi** i feltet **Metode** på siden **Afskrivningsprofiler**, bliver de anlægsaktiver, der er tildelt afskrivningsprofilen, afskrevet med den samme procent i hver afskrivningsperiode. Denne procentdel beregnes på basis af aktivets levetid. Hvis et aktiv f.eks. har en levetid på fem år, beregnes procentdelen som 40 % (200 % ÷ 5). 

Denne metode kaldes også for dobbelt saldoafskrivning.

Hvis du vil oprette en 200 % saldoafskrivning, skal du også foretage valg i feltet **Afskrivningsår** og feltet **Periodefrekvens** på siden **Afskrivningsprofiler**. Hvilke indstillinger der er tilgængelige i feltet **Periodefrekvens**, varierer, afhængigt af den værdi du vælger i feltet **Afskrivningsår**.

## <a name="select-a-depreciation-year"></a>Vælge et afskrivningsår
Du kan vælge enten **Kalender** eller **Regnskabsår** i feltet **Afskrivningsår** på siden **Afskrivningsprofiler**. Standardværdien er **Kalender**. 

Dit valg bestemmer, hvad der kan vælges i feltet **Periodefrekvens**. Dette felt definerer datoer og beløb for periodiseringen af afskrivningsposteringerne i hele kalenderåret.

### <a name="calendar"></a>Kalender

Du kan vælge at beholde standardværdien i feltet **Afskrivningsår**, **Kalender**. 

Indstillingen **Kalender** opdaterer afskrivningsgrundlaget d. 1. januar hvert år. Afskrivningen er typisk bogført nettoværdi minus scrapværdi. I eksemplerne senere i dette emne er afskrivningsgrundlaget tælleren i det første udtryk i beregningen i beregningskolonnen. 

Hvis du vælger **Kalender** som afskrivningsår, er følgende indstillinger tilgængelige i feltet **Periodefrekvens**:

-   **Årligt** bogfører et beløb d. 31. december.
-   **Månedligt** bogfører et månedligt beløb sidst i hver kalendermåned.
-   **Kvartalsvis** bogfører et kvartalsmæssigt beløb sidst i hvert kalenderkvartal (d. 31. marts, d. 30. juni, d. 30. september og d. 31. december).
-   **Halvårlig** bogfører et halvårligt beløb sidst i kalenderhalvåret (d. 30. juni og d. 31. december).
-   **Daglig** bogfører afskrivningsbeløbet for afskrivningsmetoden dagligt ved hjælp af en postering for hver dag.

### <a name="fiscal"></a>Regnskabsår

Hvis du vælger **Regnskabsår** i feltet **Afskrivningsår**, beregnes 200 % saldoafskrivning på grundlag af regnskabsåret for den regnskabskalender, der er angivet for modellen eller den regnskabskalender, der er valgt på siden **Finans**. Regnskabskalendere oprettes på siden **Regnskabskalendere**. 

For eksempel for regnskabsåret d. 1 til 30 begynder beregningen af afskrivninger den 1. Regnskabsåret kan være længere eller kortere end 12 måneder. Afskrivningen reguleres for hver periode. Længden på det næste regnskabsår bestemmes af konfigurationen af perioderne på siden **Regnskabskalendere**. 

Npr du har valgt **Regnskabsår** som afskrivningsår, er følgende indstillinger tilgængelige i feltet **Periodefrekvens**:

-   **Årligt** bogfører det samlede afskrivningsbeløb, der beregnes for regnskabsåret som ét beløb på den sidste dag i regnskabsåret.
-   **Regnskabsperiode** bogfører det samlede afskrivningsbeløb, der er beregnet for regnskabsåret. Dette beløb periodiseres for de regnskabsperioder, der er defineret på siden **Regnskabskalendere**.

## <a name="example-of-200-reducing-balance-depreciation"></a>Eksempel på en 200 % saldoafskrivning
|                                |        |
|--------------------------------|--------|
| Anskaffelsesomkostning               | 11.000 |
| Restværdi                  | 1.000 |
| Afskrivningsgrundlag              | 10.000 |
| Levetid i år             | 5      |
| Årlig afskrivningsprocent | 40 %    |

Metoden med 200 % saldoafskrivning dividerer de 200 % med levetiden i år. Denne procent ganges med aktivets bogførte nettoværdi for at beregne årets afskrivningsbeløb.

| Periode | Beregning af det årlige afskrivningsbeløb | Bogført værdi             | Den bogførte nettoværdi ved årets afslutning |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| År 1 | (11.000 – 1.000) × 40 % = 4.000                | 11.000-4.000 = 7.000 | 11.000 - 1.000 - 4.000 = 6.000        |
| År 2 | 6.000 × 40 % = 2.400                           | 7.000 - 2.400 = 4.600  | 6.000 - 2.400 = 3.600                 |
| År 3 | 3.600 × 40 % = 1.440                           | 4.600 - 1.440 = 3.160  | 3.600 - 1.440 = 2.160                 |

> [!NOTE] 
> Typisk, når det beløb, der beregnes ved hjælp af de 200 % reduktion af afskrivningsmetoden saldoværdi bliver mindre end det beløb, der skal beregnes ved hjælp af den lineære metode, der er en konvertering til lineær afskrivningsmetode for resten af levetiden.


