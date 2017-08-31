---
title: "Reduktionsnøgler"
description: "Denne artikel indeholder eksempler på, hvordan du konfigurerer en reduktionsnøgle. Den indeholder oplysninger om de forskellige indstillinger for reduktionsnøglen og resultaterne af hver. Du kan bruge en reduktionsnøgle til at definere, hvordan du kan reducere budgetbehov."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqPlanSched
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19251
ms.assetid: aa9e0dfb-6052-4a2e-9378-89507c02fdf2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: ce3ff2ac0a5bd9bd342baa05425d7d0957ab8a09
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017

---

# <a name="reduction-keys"></a>Reduktionsnøgler

[!include[banner](../includes/banner.md)]


Denne artikel indeholder eksempler på, hvordan du konfigurerer en reduktionsnøgle. Den indeholder oplysninger om de forskellige indstillinger for reduktionsnøglen og resultaterne af hver. Du kan bruge en reduktionsnøgle til at definere, hvordan du kan reducere budgetbehov.

<a name="example-1-percent---reduction-key-forecast-reduction-principle"></a>Eksempel 1: Budgetreduktionsprincip for Procent - reduktionsnøgle
---------------------------------------------------------------

Dette eksempel viser, hvordan en reduktionsnøgle reducerer efterspørgselsprognosebehovet i henhold til de procenter og tidsperioder, der er defineret i reduktionsnøglen.

1.  På siden **Reduktionsnøgler** skal du angive følgende linjer.
    | Byttepenge | Enhed  | Procent |
    |--------|-------|---------|
    | 1      | Måned | 100     |
    | 2      | Måned | 75      |
    | 3      | Måned | 50      |
    | 4      | Måned | 25      |

2.  Knyt reduktionsnøglen til varedisponeringsgruppen.
3.  Vælg **Procent - reduktionsnøgle** i feltet **Reduktionsprincip** på siden **Behovsplaner**.
4.  Opret en efterspørgselsprognose på 1000 enheder pr. måned.

Hvis du kører hovedplanlægning pr. 1. januar, forbruges efterspørgselsprognosebehovet i overensstemmelse med den procentdel, som du konfigurerer på siden **Reduktionsnøgler**. Følgende behovsantal overføres til behovsplanen.

| Måned                | Antal krævede enheder |
|----------------------|---------------------------|
| Januar              | 0                         |
| Februar             | 250                       |
| Marts                | 500                       |
| April                | 750                       |
| Maj-december | 1.000                     |

## <a name="example-2-transactions--reduction-key-forecast-reduction-principle"></a>Eksempel 2: Posteringer – reduktionsnøgle for budgetreduktionsprincip
Dette eksempel viser, hvordan de faktiske ordrer, der forekommer i de perioder, der er defineret i reduktionsnøglen, reducerer efterspørgselsprognosebehovet.

-   Vælg **Posteringer - reduktionsnøgle** i feltet **Reduktionsprincip** på siden **Behovsplaner**.

Der findes følgende salgsordrer pr. 1. januar.

| Måned    | Antal bestilte enheder |
|----------|--------------------------|
| Januar  | 956                      |
| Februar | 1.176                    |
| Marts    | 451                      |
| April    | 119                      |

Hvis du bruger samme efterspørgselsprognose på 1.000 enheder pr. måned anvendes, overføres følgende behovsantal til behovsplanen.

| Måned                | Antal krævede enheder |
|----------------------|---------------------------|
| Januar              | 44                        |
| Februar             | 0                         |
| Marts                | 549                       |
| April                | 881                       |
| Maj-december | 1.000                     |

## <a name="example-3-transactions--dynamic-period-forecast-reduction-principle"></a>Eksempel 3: Posteringer – reduktionsprincip for dynamisk budgetperiode
I de fleste tilfælde konfigureres systemer, så posteringer reducerer efterspørgselsprognose inden for specifikke budgetperioder: uger, måneder og så videre. Disse perioder er defineret i reduktionsnøglen. Men tiden mellem to linjer i behovsprognosen kan også *omfatte* en periode.

1.  Opret en behovsprognose for følgende datoer og antal.
    | Dato       | Behovsprognose |
    |------------|-----------------|
    | 1. januar  | 1.000           |
    | 5. januar  | 500             |
    | 12. januar | 1.000           |

    I dette budget er der ikke en klar periode mellem budgetdatoerne: mellem første og anden dato er der et interval på fire dage, og mellem den anden og tredje dato er det et interval på syv dage. Disse forskellige intervaller er dynamiske perioder.
2.  Opret salgsordrelinjer på følgende måde.
    | Dato                             | Salgsordremængde |
    |----------------------------------|----------------------|
    | 15. december forrige år | 500                  |
    | 3. januar                        | 100                  |
    | 10. januar                       | 200                  |

Budgettet reduceres på følgende måde:

-   Den første salgsordre er ikke inden for en periode, så det reducerer ikke et budget.
-   Den anden salgsordre ligger mellem d. 1-5. januar, så det vil reducere budgettet for den 1. januar med 100.
-   Den tredje salgsordre ligger mellem d. 5-12. januar, så det vil reducere budgettet for den 5. januar med 200.

Der oprettes følgende ordreforslaget for at imødekomme budgettet.

| Dato for behovsprognose | Reduceret antal |
|----------------------|------------------|
| 1. januar            | 900              |
| 5. januar            | 300              |
| 12. januar           | 1.000            |

Her er en oversigt over reduktionen **Posteringer - dynamisk periode**:

-   Budgetbehovet reduceres via de faktiske ordreposteringer, der forekommer i den dynamiske periode. Den dynamiske periode dækker de aktuelle budgetdatoer og slutter ved starten af det næste budget.
-   Til denne metode hverken bruges eller kræves en reduktionsnøgle.
-   Når denne indstilling bruges, forekommer følgende funktionsmåde:
    -   Hvis budgettet reduceres helt, bliver budgetbehovet for det aktuelle budget 0 (nul).
    -   Hvis der ikke er noget fremtidigt budget, bliver budgetbehovet fra det sidst angivne budget reduceret.
    -   Tidshorisonter medtages i beregningen af budgetreduktionen.
    -   Positive dage medtages i beregningen af budgetreduktionen.
    -   Hvis de faktiske ordreposteringer overstiger budgetbehovet, overføres de resterende posteringer ikke til den næste budgetperiode.


<a name="see-also"></a>Se også
--------

[Behovsplaner](master-plans.md)




