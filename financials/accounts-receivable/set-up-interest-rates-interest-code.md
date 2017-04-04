---
title: Angive rentesatser for en rentekode
description: "Rentekoder omfatter indstillinger, der bestemmer, hvornår der opkræves rente, og hvordan det beregnes på forfaldne konti."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 59402
ms.assetid: 3b945333-1eaf-4658-ab5a-1a7791a7eb40
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: 9656718d7afbcc6d89e650ab9379900c083507fe
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-interest-rates-for-an-interest-code"></a>Angive rentesatser for en rentekode

Rentekoder omfatter indstillinger, der bestemmer, hvornår der opkræves rente, og hvordan det beregnes på forfaldne konti.

Du kan oprette en enkelt rentekode og anvende den på flere debitorposteringsprofiler, faktureringskoder eller på bestemte fakturalinjer. Når oplysningerne om rentekoden ændres, implementeres ændringerne automatisk i forbindelse med nye transaktioner for alle funktioner, der bruger koden. Du kan oprette to typer af satser for hver rentekode:
-   Satser for renteindtægter − Repræsentere indtægter, der er opnået ved opkrævning af renter på fakturaer eller rentenotaer.
-   Satser for rentebetalinger − Repræsenterer en omkostning, der betales for renter på kreditnotaer.

Begge typer kan findes på samme tid og i samme rentekode. Rentesatser kan være baseret på tre beregningstyper:
-   Rente efter procent.
-   Rente efter beløb.
-   Rente efter interval, der resulterer i en enkelt procent eller beløb.

Når en rentekode bruges til at beregne renter, oprettes en separat rentenota for hver rentesats, der er gældende på det tidspunkt, hvor betalingen har overskredet forfaldsdatoen. Du bruger fanen **Indtægter** på siden **Rentekode** til at angive rentesatser for renter, du tjener ved opkrævning af renter. Brug fanen **Betalinger** til at oprette rentesatser for den rente, du betaler.

## <a name="interest-rates-based-on-a-percentage"></a>Rentesatser baseret på en procentdel
Du kan oprette rentesatser, der beregner en angivet procentdel.

-   Rentebeløb, der gælder for alle valutaer.
-   Valgfri rentebeløbsgrænser kan angives.
-   **Procentdel** er markeret ** ** i det **beregning af renter, der er baseret på** på den **oprette rentekoder** side.

For at oprette en rentekode, der opkræver rente på 5 procent for hver anden måned, hvor fakturabetalingen overskrider posteringens forfaldsdato, du skal skrive 2 i den **beregne renter hvert** og vælg **måned**.

## <a name="interest-rates-based-on-amounts"></a>Rentesatser baseret på beløb
Du kan oprette rentesatser, der beregner et bestemt beløb pr. valuta.
-   Der angives et rentebeløb for hver valuta i rentekoden.
-   Valgfri rentebeløbsgrænser kan angives.
-   ** Beløb ** er valgt i den **beregning af renter, der er baseret på** på den **oprette rentekoder** side.

For at oprette en rentekode, der opkræver rente af 25,00 for hver 20 dage, hvor fakturabetalingen overskrider posteringens forfaldsdato, ville du indtaster 20 i den **beregne renter hvert**, og vælg **dag**.

## <a name="interest-rates-based-on-ranges"></a>Rentesatser baseret på intervaller
Du kan oprette rentesatser, der varierer afhængigt af det forfaldne beløb, antallet dage, betalingen er forsinket, eller antallet af måneder, betalingen er forsinket.
-   Du kan bruge fanen **Overskud efter valuta** til at angive indstillinger for din rente for hver valuta. Det er også der, hvor du kan definere området.
-   Brug knappen **Afgrænsninger** for at tilføje linjer, der repræsenterer de afgrænsninger, du vil konfigurere. Værdien **Fra** repræsenterer starten af afgrænsningen, og tallet **Renteværdi** repræsenterer en procentdel eller et beløb, afhængigt af valget i feltet **Beregn renter på baggrund af** på siden **Konfigurer rentekoder**.

## <a name="example-1-interest-by-range--amount"></a>Eksempel 1: Renter efter interval = beløb
Du har oprettet en rentekode, der opkræver rente én gang for hver tre måneder, hvor fakturabetalingen overskrider posteringens forfaldsdato. Du vil basere beregningen på en procentvis renteværdi i henhold til de trinvise beløbsintervaller. Renteværdien vil være 1 procent for fakturabeløb op til 1.000,00, 2 procent for beløb fra 1,001.00 til 5,000.00, og 3 procent for beløb, der er større end 5,000.00. Indstil rentekodeværdierne på følgende måde.

| **Feltnavn**                  | **Feltværdi** |
|---------------------------------|-----------------|
| **Rentekode**               | 3M%ByAmt        |
| **Beregn rente hver**    | 3/måned         |
| **Rente efter interval**           | Beløb          |
| **Beregn renten på baggrund af** | Procentdel      |

Du angiver intervaloplysninger på følgende måde.

| **From value** | **Interest value** |
|----------------|--------------------|
| 0              | 1                  |
| 1,001          | 2                  |
| 5,001          | 3                  |

 
## <a name="example-2-interest-by-range--days"></a>Eksempel 2: Renter efter interval = dage
--------------------------------------------------

Du har oprettet en rentekode, der opkræver rente én gang for hver 15 dage, hvor fakturabetalingen overskrider posteringens forfaldsdato. Du vil basere beregningen på en beløbsmæssig renteværdi i henhold til de trinvise dagsintervaller. Renteværdien vil være 10,00 pr. 15 dage i de første 60 dage, 15,00 pr. 15 dag i dagene 61-90 og 20,00 pr. 15 dage fra dag 91 og efter. Indstil rentekodeværdierne på følgende måde.

| **Feltnavn**                  | **Feltværdi** |
|---------------------------------|-----------------|
| **Rentekode**               | 15DAmtXDay      |
| **Beregn rente hver**    | 15/Dag          |
| **Rente efter interval**           | Dage            |
| **Beregn renten på baggrund af** | Beløb          |

Du angiver intervaloplysninger på følgende måde.

| **From value** | **Interest value** |
|----------------|--------------------|
| 0              | 10                 |
| 61             | september                 |
| 91             | 20                 |

 
## <a name="example-3-interest-by-range--months"></a>Eksempel 3: Renter efter interval = måneder
----------------------------------------------------

Du har oprettet en rentekode, der opkræver rente én gang for hver måned, hvor fakturabetalingen overskrider posteringens forfaldsdato. Du vil basere beregningen på en procentvis renteværdi i henhold til de trinvise månedsintervaller. Renteværdien vil være 1,5 procent pr. måned for de første tre måneder, 2,0 procent pr. måned for de næste tre måneder og 2,5 procent pr. måned for hver måned ud over de første seks måneder. Indstil rentekodeværdierne på følgende måde.

| **Feltnavn**                  | **Feltværdi** |
|---------------------------------|-----------------|
| **Rentekode**               | 1M%ByMth        |
| **Beregn rente hver**    | 1/måned         |
| **Rente efter interval**           | Måneder          |
| **Beregn renten på baggrund af** | Procentdel      |

Du angiver intervaloplysninger på følgende måde.

| **From value** | **Interest value** |
|----------------|--------------------|
| 0              | 1.5                |
| 4              | 2                  |
| 7              | 2,5                |

## <a name="new-versions"></a>Nye versioner
Rentekoder er for gældende dato. Hvis du vil ændre renten, kan du oprette en **ny version**, der er gældende for en fremtidig dato.

For at få vist forskellige versioner kan du bruge menupunktet **Pr. dato** til at vælge skæringsdatoen. Du kan også vælge **Vis alle poster** for at få vist alle rentekoderne på siden.


