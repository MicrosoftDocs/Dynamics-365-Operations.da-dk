---
title: 150 % saldoafskrivning
description: Denne artikel indeholder en oversigt over afskrivningsmetoden 150 % saldoafskrivning.
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
ms.custom: 13891
ms.assetid: 36d1112d-921c-4fff-abe0-0ff2429848d3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 8e89a57dda8f2d392483ed13c686ea97b74926b0
ms.openlocfilehash: d256feeadcf19550995c145f4e9a171acaeaeec3
ms.lasthandoff: 03/31/2017


---

# <a name="150-percent-reducing-balance-depreciation"></a>150 % saldoafskrivning

[!include[banner](../includes/banner.md)]


Denne artikel indeholder en oversigt over afskrivningsmetoden 150 % saldoafskrivning.

Når du opretter en afskrivningsprofil til et anlægsaktiv og vælger **150% saldoværdi** i feltet **Metode** på siden **Afskrivningsprofiler**, bliver de anlægsaktiver, der er tildelt afskrivningsprofilen, afskrevet med den samme procent i hver afskrivningsperiode. Denne procentdel beregnes på basis af aktivets levetid. Hvis et aktiv f.eks. har en levetid på fem år, beregnes procentdelen som 30 % (150 % ÷ 5). 

Hvis du vil oprette en 150 % saldoafskrivning, skal du også foretage valg i feltet **Afskrivningsår** og feltet **Periodefrekvens** på siden **Afskrivningsprofiler**. Hvilke indstillinger , der er tilgængelige i feltet **Periodefrekvens**, varierer, afhængigt af den værdi der er valgt i feltet **Afskrivningsår**.

## <a name="selection-of-depreciation-year"></a>Valg af afskrivningsår
Du kan vælge enten **Kalender** eller **Regnskabsår** i feltet **Afskrivningsår** på siden **Afskrivningsprofiler**. 

Standardværdien er **Kalender**. Dit valg bestemmer, hvad der kan vælges i feltet **Periodefrekvens**. Dette felt definerer datoer og beløb for periodiseringen af afskrivningsposteringerne i hele kalenderåret.

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

Hvis du vælger **Regnskabsår** i feltet **Afskrivningsår**, beregnes 150 % saldoafskrivning på grundlag af regnskabsåret for den regnskabskalender, der er angivet for modellen eller den regnskabskalender, der er valgt på siden **Finans**. Regnskabskalendere oprettes på siden **Regnskabskalendere**. 

I forbindelse med regnskabsåret fra d. 1. juli til og med d. 30. juni starter afskrivningsberegningen f.eks. d. 1. juli. Regnskabsåret kan være længere eller kortere end 12 måneder. Afskrivningen reguleres for hver periode. Længden på det næste regnskabsår bestemmes af konfigurationen af perioderne på siden **Regnskabskalendere**. 

Hvis du vælger **Regnskabsår** som afskrivningsår, er følgende indstillinger tilgængelige i feltet **Periodefrekvens**:

-   **Årlig** bogfører det samlede afskrivningsbeløb, der beregnes for regnskabsåret på den sidste dag i regnskabsåret.
-   **Regnskabsperiode** bogfører det samlede afskrivningsbeløb, der er beregnet for regnskabsåret. Dette beløb periodiseres for de regnskabsperioder, der er defineret på siden **Regnskabskalendere**.

## <a name="example-of-150-reducing-balance-depreciation"></a>Eksempel på en 150 % saldoafskrivning
|                                |        |
|--------------------------------|--------|
| Anskaffelsesomkostning               | 11.000 |
| Restværdi                  | 1.000  |
| Afskrivningsgrundlag              | 10.000 |
| Levetid i år             | 5      |
| Årlig afskrivningsprocent | 30 %    |

Metoden med 150 % saldoafskrivning dividerer de 150 % med levetiden i år. Denne procent ganges med aktivets bogførte nettoværdi for at beregne årets afskrivningsbeløb.

| Periode | Beregning af det årlige afskrivningsbeløb | Bogført værdi             | Den bogførte nettoværdi ved årets afslutning |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| År 1 | (11.000 – 1.000) × 30 % = 3.000                | 11.000 – 3.000 = 8.000 | 11.000 – 1.000 – 3.000 = 7.000        |
| År 2 | 7.000 × 30 % = 2.100                           | 8.000 – 2.100 = 5.900  | 7.000 – 2.100 = 4.900                 |
| År 3 | 4.900 × 30 % = 1.470                           | 5.900 – 1.470 = 4.430  | 4.900 – 1.470 = 3.430                 |

> [!NOTE]
> Når det beløb, der er beregnet ved hjælp af metoden til 150 % saldoafskrivning bliver mindre end det beløb, der skal beregnes ved hjælp af den lineære metode, er der en konvertering til lineær afskrivningsmetode for resten af levetiden.




