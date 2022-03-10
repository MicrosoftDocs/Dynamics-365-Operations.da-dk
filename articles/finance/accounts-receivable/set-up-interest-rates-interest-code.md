---
title: Angive rentesatser for en rentekode
description: Rentekoder omfatter indstillinger, der bestemmer, hvornår der opkræves rente, og hvordan det beregnes på forfaldne konti.
author: ShivamPandey-msft
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Interest
audience: Application User
ms.reviewer: roschlom
ms.custom: 59402
ms.assetid: 3b945333-1eaf-4658-ab5a-1a7791a7eb40
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 09808433140f71bf2d7bfaaca87b6c27adb56d86c4c14ad44b37592d416fa2b9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716711"
---
# <a name="set-up-interest-rates-for-an-interest-code"></a>Angive rentesatser for en rentekode

[!include [banner](../includes/banner.md)]

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

- Rentebeløb, der gælder for alle valutaer.
- Valgfri rentebeløbsgrænser kan angives.
- **Procent** vælges i feltet **Beregn renten på baggrund af** på siden **Konfigurer rentekoder**.

Hvis du f.eks. vil oprette en rentekode, der opkræver 5 procent rente for hver to måneder, hvor fakturabetalingen overskrider posteringens forfaldsdato, skal du skrive 2 i feltet **Beregn rente hver** og vælge **Måned**.

> [!NOTE] 
> Den nye algoritme til beregning af rentenotaer tilføjes ved hjælp af funktionsstyring. Hvis du vil bruge denne algoritme, skal du aktivere funktionen **(GBL) Tillad beregning af rente pr. dag som en årsprocent divideret med funktionen 365**. Du kan finde flere oplysninger om aktivering af funktionen under [Oversigt over funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
> 
> Formlen til beregning af rentenotabeløbet er: 
>  
> Rentenotabeløb = Skyldige beløb * Årligt rentebeløb % / 365 * Antal dage for sent
>  
> Denne funktion er tilgængelig i version 10.0.18 eller nyere.    
 
## <a name="interest-rates-based-on-amounts"></a>Rentesatser baseret på beløb
Du kan oprette rentesatser, der beregner et bestemt beløb pr. valuta.
- Der angives et rentebeløb for hver valuta i rentekoden.
- Valgfri rentebeløbsgrænser kan angives.
- **Beløb** vælges i feltet **Beregn rente på baggrund af** på siden **Konfigurer rentekoder**.

Hvis du f.eks. vil oprette en rentekode, der opkræver en rente på 25,00 for hver 20 dage, hvor fakturabetalingen overskrider posteringens forfaldsdato, skal du skrive 20 i feltet **Beregn rente hver** og vælge **Dag**.

## <a name="interest-rates-based-on-ranges"></a>Rentesatser baseret på intervaller
Du kan oprette rentesatser, der varierer afhængigt af det forfaldne beløb, antallet dage, betalingen er forsinket, eller antallet af måneder, betalingen er forsinket.
-   Du kan bruge fanen **Overskud efter valuta** til at angive indstillinger for din rente for hver valuta. Det er også der, hvor du kan definere området.
-   Brug knappen **Afgrænsninger** for at tilføje linjer, der repræsenterer de afgrænsninger, du vil konfigurere. Værdien **Fra** repræsenterer starten af afgrænsningen, og tallet **Renteværdi** repræsenterer en procentdel eller et beløb, afhængigt af valget i feltet **Beregn renter på baggrund af** på siden **Konfigurer rentekoder**.

## <a name="example-1-interest-by-range--amount"></a>Eksempel 1: Renter efter interval = beløb
Du har oprettet en rentekode, der opkræver rente én gang for hver tre måneder, hvor fakturabetalingen overskrider posteringens forfaldsdato. Du vil basere beregningen på en procentvis renteværdi i henhold til de trinvise beløbsintervaller. Renteværdien vil være 1 procent for fakturabeløb op til 1.000,00, 2 procent for beløb fra 1,001.00 til 5,000.00, og 3 procent for beløb, der er større end 5,000.00. Indstil rentekodeværdierne på følgende måde.

| **Feltnavn**                  | **Feltværdi** |
|---------------------------------|-----------------|
| **Rentekode**               | 3M%ByAmt        |
| **Beregn rente hver**    | 3/Måned         |
| **Rente efter interval**           | Beløb          |
| **Beregn renten på baggrund af** | Procentdel      |

Du angiver intervaloplysninger på følgende måde.

| **Fra værdi** | **Renteværdi** |
|----------------|--------------------|
| 0              | 1                  |
| 1,001          | 2                  |
| 5,001          | 3                  |


## <a name="example-2-interest-by-range--days"></a>Eksempel 2: Renter efter interval = dage

Du har oprettet en rentekode, der opkræver rente én gang for hver 15 dage, hvor fakturabetalingen overskrider posteringens forfaldsdato. Du vil basere beregningen på en beløbsmæssig renteværdi i henhold til de trinvise dagsintervaller. Renteværdien vil være 10,00 pr. 15 dage i de første 60 dage, 15,00 pr. 15 dag i dagene 61-90 og 20,00 pr. 15 dage fra dag 91 og efter. Indstil rentekodeværdierne på følgende måde.

| **Feltnavn**                  | **Feltværdi** |
|---------------------------------|-----------------|
| **Rentekode**               | 15DAmtXDay      |
| **Beregn rente hver**    | 15/Dag          |
| **Rente efter interval**           | Dage            |
| **Beregn renten på baggrund af** | Beløb          |

Du angiver intervaloplysninger på følgende måde.

| **Fra værdi** | **Renteværdi** |
|----------------|--------------------|
| 0              | 10                 |
| 61             | 15                 |
| 91             | 20                 |


## <a name="example-3-interest-by-range--months"></a>Eksempel 3: Renter efter interval = måneder

Du har oprettet en rentekode, der opkræver rente én gang for hver måned, hvor fakturabetalingen overskrider posteringens forfaldsdato. Du vil basere beregningen på en procentvis renteværdi i henhold til de trinvise månedsintervaller. Renteværdien vil være 1,5 procent pr. måned for de første tre måneder, 2,0 procent pr. måned for de næste tre måneder og 2,5 procent pr. måned for hver måned ud over de første seks måneder. Indstil rentekodeværdierne på følgende måde.

| **Feltnavn**                  | **Feltværdi** |
|---------------------------------|-----------------|
| **Rentekode**               | 1M%ByMth        |
| **Beregn rente hver**    | 1/Måned         |
| **Rente efter interval**           | Måneder          |
| **Beregn renten på baggrund af** | Procentdel      |

Du angiver intervaloplysninger på følgende måde.

| **Fra værdi** | **Renteværdi** |
|----------------|--------------------|
| 0              | 1.5                |
| 4              | 2                  |
| 7              | 2,5                |

## <a name="new-versions"></a>Nye versioner
Rentekoder er for gældende dato. Hvis du vil ændre renten, kan du oprette en **ny version**, der er gældende for en fremtidig dato.

For at få vist forskellige versioner kan du bruge menupunktet **Pr. dato** til at vælge skæringsdatoen. Du kan også vælge **Vis alle poster** for at få vist alle rentekoderne på siden.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
