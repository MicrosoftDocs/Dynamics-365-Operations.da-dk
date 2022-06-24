---
title: Reducer saldoafskrivning
description: Denne artikel indeholder en oversigt over afskrivningsmetoden Saldoafskrivning.
author: moaamer
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: kfend
ms.custom: 3281
ms.assetid: 1b86763d-d47c-4a6a-a9a6-d97a736750da
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 52bf9d4e9cbc9cabda5d5ab17c1a00ecea0d0348
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883265"
---
# <a name="reduce-balance-depreciation"></a>Reducer saldoafskrivning

[!include [banner](../includes/banner.md)]

Denne artikel indeholder en oversigt over afskrivningsmetoden Saldoafskrivning.

Når du opretter en afskrivningsprofil til et anlægsaktiv og vælger Saldoafskrivning i feltet **Metode** på siden **Afskrivningsprofiler**, afskrives der med den samme procent i hver afskrivningsperiode på de aktiver, der har denne afskrivningsprofil tilknyttet.

Hvis du vil oprette afskrivning efter saldoværdimetoden, skal du også angive indstillinger i felterne i oversigtspanelet **Generelt** på siden **Afskrivningsprofiler**. Først skal du vælge et år i feltet **Afskrivningsår**. Ud fra valget vises der forskellige indstillinger i feltet **Periodefrekvens**, som forklaret i følgende afsnit. 

Du skal også angive en værdi i feltet **Procent** for afskrivningsprofilen. Hvis du vælger indstillingen **Fuld afskrivning**, tages den resterende afskrivning i den sidste afskrivningsperiode, og den kan udgøre et stort beløb. I nogle lande/områder bruges der ikke en omlægning til lineær afskrivning. Der kan forekommer omlægninger, når beløbet for den alternative afskrivningsmetode er større end eller lig med beløbet for den primære afskrivningsprofil, og der brugte afskrivningsbeløb er beløbet for den alternative metode. 

Fordi et aktiv aldrig bliver fuldt afskrevet på basis af en procentberegning, skal du vælge indstillingen **Fuld afskrivning** for at afskrive et anlægsaktiv i fuldt omfang.

## <a name="select-a-depreciation-year"></a>Vælge et afskrivningsår
Du kan vælge enten **Kalender** eller **Regnskabsår** i feltet **Afskrivningsår** på siden **Afskrivningsprofiler**. Dit valg bestemmer, hvad der kan vælges i feltet **Periodefrekvens**. Standardindstillingen er **Kalender**.

### <a name="calendar"></a>Kalender

**Indstillingen Kalender** opdaterer afskrivningsgrundlaget (typisk bogført nettoværdi minus scrapværdi) d. 1. januar hvert år. I saldoværdieksemplet senere i denne artikel er afskrivningsgrundlaget tælleren i det første udtryk i beregningen i kolonnen Beregninger. 

Hvis du vælger **Kalender**, kan du vælge mellem følgende indstillinger i feltet **Periodefrekvens**, der definerer datoer og beløb for periodiseringen af afskrivningsposteringerne i hele kalenderåret.

- Ved Årligt bogføres d. 31. december.
- Ved Månedligt bogføres et månedligt beløb sidst i hver kalendermåned.
- Ved Kvartalsvis bogføres et kvartalsmæssigt beløb sidst i hvert kalenderkvartal (d. 31. marts, d. 30. juni, d. 30. september og d. 31. december).
- Ved Halvårlig bogføres et halvårligt beløb sidst i hvert kalenderhalvår (d. 30. juni og d. 31. december).
- Ved Dagligt bogføres afskrivningsbeløbet for afskrivningsmetoden dagligt ved hjælp af en postering for hver dag.

Hvis du f.eks. vælger **Årligt**, bogføres den årlige afskrivning kun én gang, nemlig d. 31. december hvert år. Hvis du vælger **Månedligt**, bogføres den månedlige afskrivning hver måned med 1/12 af det årlige afskrivningsbeløb.

### <a name="fiscal"></a>Regnskabsår

Hvis du vælger **Regnskab** i feltet **Afskrivningsår**, bruges den lineære afskrivningsmetode. Den beregnes baseret på det regnskabsår, der er angivet på siden **Regnskabskalendere** for den regnskabskalender, der er valgt på siden **Finans**. I forbindelse med regnskabsåret fra d. 1. juli til og med d. 30. juni starter afskrivningsberegningen f.eks. d. 1. juli. Regnskabsåret kan være længere eller kortere end 12 måneder. Afskrivningen reguleres for hver regnskabsperiode. Længden på regnskabsåret er baseret på de regnskabsperioder, du angiver, når du opretter et nyt regnskabsår på siden **Regnskabskalendere**.


Hvis du vælger **Regnskab**, kan du vælge mellem følgende indstillinger i feltet **Periodefrekvens**:

- Ved Årligt bogføres det samlede afskrivningsbeløb, der beregnes for regnskabsåret som ét beløb på den sidste dag i regnskabsåret.
- Ved Regnskabsperiode bogføres det samlede afskrivningsbeløb, der beregnes for regnskabsåret, der periodiseres for de regnskabsperioder, der er defineret for den regnskabskalender, der er valgt på siden **Finans**, eller for den regnskabskalender, der er valgt for bogen for et anlægsaktiv.

## <a name="example-of-reducing-balance-depreciation"></a>Eksempel på saldoafskrivning

Det antages, at anskaffelsesprisen for anlægsaktivet er 11.000, at scrapværdien er 1.000, og at afskrivningsprocentsatsen er 30. 

Når metoden Saldoværdi benyttes, beregnes der 30 % af afskrivningsgrundlaget (bogført nettoværdi minus scrapværdi) ved slutningen af den forrige afskrivningsperiode. Afskrivning i de første tre år er vist i følgende tabel.

| Periode | Beregning af det årlige afskrivningsbeløb | Den bogførte nettoværdi ved årets afslutning |
|--------|-------------------------------------------|---------------------------------------|
| År 1 | (11.000 - 1.000) \* 30 % = 3.000           | (11.000 - 1.000) - 3.000 = 7.000      |
| År 2 | (7.000 - 1.000) \* 30 % = 1.800            | (7.000 - 1.800) = 5.200                |
| År 3 | (5.200 - 1.000) \* 30 % = 1.260            | (5.200 - 1.260) = 3.940               |










[!INCLUDE[footer-include](../../includes/footer-banner.md)]
