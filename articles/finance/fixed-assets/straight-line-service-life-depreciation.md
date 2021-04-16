---
title: Lineær afskrivning for levetiden
description: Denne artikel indeholder en oversigt over afskrivningsmetoden Lineær afskrivning for levetiden.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 3341
ms.assetid: ae5ceaeb-aeb7-45cd-b835-23cf9c5cf95a
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 39366716463eda03aa3f9c0ed802eb3f6099b48c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818482"
---
# <a name="straight-line-service-life-depreciation"></a>Lineær afskrivning for levetiden

[!include [banner](../includes/banner.md)]

Denne artikel indeholder en oversigt over afskrivningsmetoden Lineær afskrivning for levetiden.

Når du opretter en afskrivningsprofil for anlægsaktiver og vælger Lineær afskrivning over servicelevetiden i feltet Metode på siden Afskrivningsprofiler, baseres afskrivningen af aktiver med denne tilknyttede afskrivningsprofil, på baggrund af den samlede levetid for anlægsaktivet. Det vil normalt sige med det samme afskrivningsbeløb for hver afskrivningsperiode. 

Den eneste forskel, der er på det afskrivningsbeløb, der beregnes for den lineær afskrivningsmetode for den resterende levetid og lineær afskrivningsmetode for levetiden, er ved postering af en regulering for anlægsaktivet. 

Hvis du vil oprette en lineær afskrivning for servicelevetiden, skal du også foretage valg i felterne Afskrivningsår og Periodefrekvens på siden Afskrivningsprofiler.

## <a name="select-a-depreciation-year"></a>Vælge et afskrivningsår
Du kan vælge enten Kalender eller Regnskabsår i feltet Afskrivningsår på siden Afskrivningsprofiler. Dit valg bestemmer, hvad der kan vælges i feltet Periodefrekvens. Standardindstillingen er Kalender.

### <a name="calendar"></a>Kalender

Hvis du vælger Kalender, vises der som standard et år fra d. 1. januar til d. 31. december, også selvom du har defineret regnskabsåret anderledes. 

Indstillingen Kalender opdaterer afskrivningsgrundlaget (typisk bogført nettoværdi minus scrapværdi) d. 1. januar hvert år. I eksemplerne senere i dette emne er afskrivningsgrundlaget tælleren i det første udtryk i beregningen i beregningskolonnen. 

Hvis du vælger Kalender, kan du vælge mellem følgende indstillinger i feltet Periodefrekvens, der definerer datoer og beløb for periodiseringen af afskrivningsposteringerne i hele kalenderåret.
-   Årligt bogfører et beløb d. 31. december.
-   Ved Månedligt bogføres et månedligt beløb sidst i hver kalendermåned.
-   Ved Kvartalsvis bogføres et kvartalsmæssigt beløb sidst i hvert kalenderkvartal (d. 31. marts, d. 30. juni, d. 30. september og d. 31. december).
-   Halvårlig bogføres et halvårligt beløb sidst i hvert kalenderhalvår (d. 30. juni og d. 31. december).
-   Ved Dagligt bogføres afskrivningsbeløbet for afskrivningsmetoden dagligt ved hjælp af en postering for hver dag.

Hvis du f.eks. vælger Årligt, bogføres den årlige afskrivning kun én gang, nemlig d. 31. december hvert år. Hvis du vælger Månedligt, bogføres den månedlige afskrivning hver måned med 1/12 af det årlige afskrivningsbeløb.

### <a name="fiscal"></a>Regnskabsår

Hvis du vælger Regnskabsår i feltet Afskrivningsår, bruges den lineære afskrivningsmetode. Den beregnes efter regnskabsår, som defineret af den regnskabskalender, der er angivet for bogen, eller efter den regnskabskalender, der er valgt på siden Finans. Regnskabskalendere oprettes på siden Regnskabskalendere.

I forbindelse med regnskabsåret fra d. 1. juli til og med d. 30. juni starter afskrivningsberegningen f.eks. d. 1. juli. Regnskabsåret kan være længere eller kortere end 12 måneder. Afskrivningen reguleres automatisk for hver regnskabsperiode. Længden på regnskabsåret er baseret på de regnskabsperioder, du angiver, når du opretter et nyt regnskabsår i formen Regnskabskalendere. 

Hvis du vælger Regnskab, kan du vælge mellem følgende indstillinger i feltet Periodefrekvens:
-   Årligt bogfører det samlede afskrivningsbeløb, der beregnes for regnskabsåret som ét beløb på den sidste dag i regnskabsåret.
-   Regnskabsperiode beregner det samlede afskrivningsbeløb for regnskabsåret, der periodiseres for de perioder, der er defineret i formen Regnskabskalendere for regnskabskalenderen.

## <a name="example-straight-line-depreciation-of-an-unchanged-fixed-asset"></a>Eksempel: Lineær afskrivning af et uændret anlægsaktiv
Det antages, at anlægsaktivet har følgende karakteristika.

|                     |        |
|---------------------|--------|
| Anskaffelsesomkostninger    | 11.000 |
| Restværdi       | 1.000  |
| Afskrivningsgrundlag   | 10.000 |
| Levetid i år  | 5      |
| Årlig afskrivning | 2.000  |

Dette giver det samme afskrivningsbeløb for hvert år. (Anskaffelsesomkostninger - restværdi)/levetiden i år

| Periode | Beregning af det årlige afskrivningsbeløb | Den bogførte nettoværdi ved årets afslutning |
|--------|-------------------------------------------|---------------------------------------|
| År 1 | (11.000 - 1.000) / 5 = 2.000              | 9.000                                 |
| År 2 | (11.000 - 1.000) / 5 = 2.000              | 7.000                                 |
| År 3 | (11.000 - 1.000) / 5 = 2.000              | 5.000                                 |
| År 4 | (11.000 - 1.000) / 5 = 2.000              | 3.000                                 |
| År 5 | (11.000 - 1.000) / 5 = 2.000              | 1.000                                 |

## <a name="example-straight-line-depreciation-of-a-modified-fixed-asset"></a>Eksempel: Lineær afskrivning af et ændret anlægsaktiv

Forestil dig, at du føjer en anskaffelsesregulering på 4.000 i år 2 til det samme anlægsaktiv. 

Levetiden for anskaffelsesreguleringen er den samme som for anlægsaktivet og begynder ved anskaffelsen. Der er en bogført nettoværdi tilbage ved afslutningen af år 5. Denne svarer til den bogført nettoværdi for anskaffelsesreguleringen. Den periodeopdelte afskrivning beregnes som angivet i følgende tabel.

| Periode | Beregning af det årlige afskrivningsbeløb | Den bogførte nettoværdi ved årets afslutning |
|--------|-------------------------------------------|---------------------------------------|
| År 1 | 10.000 / 5 = 2.000                        | 11.000 - 2.000 = 9.000                |
| År 2 | 4000 (anskaffelsesregulering)            | 9.000 + 4.000 =13.000                 |
| År 2 | 14.000 / 5 = 2.800                        | 13.000 - 2.800 = 10.200               |
| År 3 | 14.000 / 5 = 2.800                        | 10.200 - 2.800 = 7.400                |
| År 4 | 14.000 / 5 = 2.800                        | 7.400 - 2.800 = 4.600                 |
| År 5 | 14.000 / 5 = 2.800                        | 4.600 - 2.800 = 1.800                 |
| År 6 | Resterende 800\*                           | 1.800 – 800 = 1.000                   |

\*Da restbeløbet er mindre end afskrivningsbeløbet, er det kun restbeløbet minus restværdien der angives.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]