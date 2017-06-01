---
title: 175 % saldoafskrivning
description: Denne artikel indeholder en oversigt over afskrivningsmetoden 175 % saldoafskrivning.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13911
ms.assetid: cc5d001f-bcfe-4602-9ec1-9e265e9fd188
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 40bbb07deb455d922244fc3856871cda7107543e
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="175-percent-reducing-balance-depreciation"></a>175 % saldoafskrivning

[!include[banner](../includes/banner.md)]


Denne artikel indeholder en oversigt over afskrivningsmetoden 175 % saldoafskrivning.

Når du opretter en afskrivningsprofil til et anlægsaktiv og vælger **175 % saldoværdi** i feltet **Metode** på siden **Afskrivningsprofiler**, bliver de anlægsaktiver, der er tildelt afskrivningsprofilen, afskrevet med den samme procent i hver afskrivningsperiode. 

Hvis du vil oprette en 175 % saldoafskrivning, skal du også foretage valg i feltet **Afskrivningsår** og feltet **Periodefrekvens** på siden **Afskrivningsprofiler**. Hvilke indstillinger , der er tilgængelige i feltet **Periodefrekvens**, varierer, afhængigt af den værdi der er valgt i feltet **Afskrivningsår**.

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

Hvis du vælger **Regnskabsår** i feltet **Afskrivningsår**, beregnes 175 % saldoafskrivning på grundlag af regnskabsåret for den regnskabskalender, der er angivet for modellen eller den regnskabskalender, der er valgt på siden **Finans**. Regnskabskalendere oprettes på siden **Regnskabskalendere**. Yderligere oplysninger finder du under [Regnskabskalendere, regnskabsår og perioder.](..\budgeting\fiscal-calendars-fiscal-years-periods.md).

I forbindelse med regnskabsåret fra d. 1. juli til og med d. 30. juni starter afskrivningsberegningen f.eks. d. 1. juli. Regnskabsåret kan være længere eller kortere end 12 måneder. Afskrivningen justeres automatisk for hver periode, og længden på det næste regnskabsår bestemmes af opsætningen af perioder på siden **Regnskabskalendere**. 

Hvis du vælger **Regnskabsår** som afskrivningsår, er følgende indstillinger tilgængelige i feltet **Periodefrekvens**:

-   **Årlig** bogfører det samlede afskrivningsbeløb, der beregnes for regnskabsåret på den sidste dag i regnskabsåret.
-   **Regnskabsperiode** beregner det samlede afskrivningsbeløb for regnskabsåret. Dette beløb periodiseres for de regnskabsperioder, der er defineret på siden **Regnskabskalendere**.

## <a name="example-of-175-reducing-balance-depreciation"></a>Eksempel på en 175 % saldoafskrivning
|                                |        |
|--------------------------------|--------|
| Anskaffelsesomkostning               | 11.000 |
| Restværdi                  | 1.000  |
| Afskrivningsgrundlag              | 10.000 |
| Levetid i år             | 5      |
| Årlig afskrivningsprocent | 35 %    |

Metoden med 175 % saldoafskrivning dividerer de 175 % med levetiden i år. Denne procent ganges med aktivets bogførte nettoværdi for at beregne årets afskrivningsbeløb.

| Periode | Beregning af det årlige afskrivningsbeløb | Bogført værdi                  | Den bogførte nettoværdi ved årets afslutning |
|--------|-----------------------------------------------|-----------------------------|---------------------------------------|
| År 1 | (11.000 – 1.000) × 35 % = 3.500                | 11.000 – 3.500 = 7.500      | 11.000 – 1.000 – 3.500 = 6.500        |
| År 2 | 6.500 × 35 % = 2.275                           | 7.500 – 2.275 = 5.225       | 6.500 – 2.275 = 4.225                 |
| År 3 | 4.225 × 35 % = 1.478,75                        | 5.225 – 1.478,75 = 3.746,25 | 4.225 – 1.478,75 = 2.746,25           |

> [!NOTE] 
> Når det beløb, der er beregnet ved hjælp af metoden til 175 % saldoafskrivning bliver mindre end det beløb, der skal beregnes ved hjælp af den lineære metode, er der en konvertering til lineær afskrivningsmetode for resten af levetiden.




