---
title: Lineær afskrivning for den resterende levetid
description: Denne artikel indeholder en oversigt over afskrivningsmetoden Lineær afskrivning for den resterende levetid.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13851
ms.assetid: 0fa2f71a-596c-414c-a6e6-8f7405a0bf81
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c12ca59203d6cad7f5699bc930f2af27427ca41b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441676"
---
# <a name="straight-line-life-remaining-depreciation"></a>Lineær afskrivning for den resterende levetid

[!include [banner](../includes/banner.md)]

Denne artikel indeholder en oversigt over afskrivningsmetoden Lineær afskrivning for den resterende levetid.

Når du opretter en afskrivningsprofil for et anlægsaktiv og vælger **Lineær afskrivning for den resterende levetid** i feltet **Metode** på siden **Afskrivningsprofiler**, er afskrivningen af anlægsaktiver, der er knyttet til afskrivningsprofilen, baseret på den resterende levetid for anlægsaktivet. Afskrivningsbeløbet er generelt det samme i hver afskrivningsperiode. Hvis du vil oprette en afskrivning for den resterende levetid, skal du også foretage valg i feltet **Afskrivningsår** og feltet **Periodefrekvens** på siden **Afskrivningsprofiler**. Hvilke indstillinger , der er tilgængelige i feltet **Periodefrekvens**, varierer, afhængigt af den værdi der er valgt i feltet **Afskrivningsår**.

## <a name="select-a-depreciation-year"></a>Vælge et afskrivningsår
Du kan vælge enten **Kalender** eller **Regnskabsår** i feltet **Afskrivningsår** på siden **Afskrivningsprofiler**. Standardværdien er **Kalender**. Dit valg bestemmer, hvad der kan vælges i feltet **Periodefrekvens**. Dette felt definerer datoer og beløb for periodiseringen af afskrivningsposteringerne i hele kalenderåret.

### <a name="calendar"></a>Kalender

Hvis du vælger **Kalender** i feltet ***Afskrivningsår***, vises der som standard et år fra d. 1. januar til d. 31. december, også selvom du har defineret regnskabsåret anderledes. Indstillingen **Kalender** opdaterer afskrivningsgrundlaget d. 1. januar hvert år. Afskrivningsgrundlaget er typisk den bogførte nettoværdi minus restværdien. I eksemplerne senere i dette emne er afskrivningsgrundlaget tælleren i det første udtryk i beregningen i beregningskolonnen. Hvis du vælger **Kalender** som afskrivningsår, er følgende indstillinger tilgængelige i feltet **Periodefrekvens**:

-   **Årligt** bogfører et beløb d. 31. december.
-   **Månedligt** bogfører et månedligt beløb sidst i hver kalendermåned.
-   **Kvartalsvis** bogfører et kvartalsmæssigt beløb sidst i hvert kalenderkvartal (d. 31. marts, d. 30. juni, d. 30. september og d. 31. december).
-   **Halvårlig** bogføres et halvårligt beløb sidst i hvert kalenderhalvår (d. 30. juni og d. 31. december).
-   **Daglig** bogfører afskrivningsbeløbet for afskrivningsmetoden dagligt ved hjælp af en postering for hver dag.

Hvis du f.eks. vælger **Årligt**, bogføres den årlige afskrivning kun én gang, nemlig d. 31. december hvert år. Hvis du vælger **Månedlig**, bogføres den månedlige afskrivning hver måned med 1/12 af det årlige afskrivningsbeløb.

### <a name="fiscal"></a>Regnskabsår

Hvis du vælger **Regnskabsår** i feltet **Afskrivningsår**, bruges den lineære afskrivning for den resterende levetid. Afskrivning beregnes på grundlag af de resterende regnskabsår. I forbindelse med regnskabsåret fra d. 1. juli 2015 til og med d. 30. juni 2016 starter afskrivningsberegningen f.eks. d. 1. juli. Regnskabsåret kan være længere eller kortere end 12 måneder. Afskrivningen reguleres for hver regnskabsperiode. Længden på det næste regnskabsår bestemmes af de regnskabsperioder, der er oprettet på siden **Regnskabskalendere**. Hvis du vælger **Regnskabsår** som afskrivningsår, er følgende indstillinger tilgængelige i feltet **Periodefrekvens**:

-   **Årligt** bogfører det samlede afskrivningsbeløb, der beregnes for regnskabsåret som ét beløb på den sidste dag i regnskabsåret.
-   **Regnskabsperiode** beregner det samlede afskrivningsbeløb for regnskabsåret. Dette beløb er derefter påløbet i regnskabsperioder, der er defineret på siden **Regnskabskalendere** for den regnskabskalender, der er angivet for bogen.

## <a name="example-of-straight-line-depreciation-of-an-unchanged-fixed-asset"></a>Eksempel på lineær afskrivning af et uændret anlægsaktiv
Et anlægsaktivet har følgende karakteristika.

|                     |        |
|---------------------|--------|
| Anskaffelsesomkostninger    | 11.000 |
| Restværdi       | 1.000  |
| Afskrivningsgrundlag   | 10.000 |
| Levetid i år  | 5      |
| Årlig afskrivning | 2.000  |

Afskrivningsbeløbet er det samme hvert år: (Anskaffelsesomkostning – Restværdi) ÷ Levetid i år

| Periode | Beregning af det årlige afskrivningsbeløb | Den bogførte nettoværdi ved årets afslutning |
|--------|-----------------------------------------------|---------------------------------------|
| År 1 | (11.000-1.000) ÷ 5 = 2.000                  | 9.000                                 |
| År 2 | (9.000-1.000) ÷ 4 = 2.000                   | 7.000                                 |
| År 3 | (7.000-1.000) ÷ 3 = 2.000                   | 5.000                                 |
| År 4 | (5.000-1.000) ÷ 2 = 2.000                   | 3.000                                 |
| År 5 | (3.000-1.000) ÷ 1 = 2.000                   | 1.000                                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]