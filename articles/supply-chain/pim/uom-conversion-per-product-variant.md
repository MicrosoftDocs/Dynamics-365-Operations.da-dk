---
title: Måleenhedskonvertering pr. produktvariant
description: Dette emne beskriver, hvordan måleenhedskonverteringer kan konfigureres for produktvarianter.
author: johanhoffmann
manager: tfehr
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: UnitOfMeasureConversion
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: e50be7fa6fa686a90b2dd5c5200c881e4629f019
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204487"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a>Måleenhedskonvertering pr. produktvariant

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan måleenhedskonverteringer kan konfigureres for produktvarianter. Emnet indeholder et eksempel på opsætningen.

Denne funktion gør det muligt for virksomheder at definere forskellige enhedsomregninger mellem varianterne af det samme produkt. I dette emne bruges følgende eksempel. Et firma sælger T-shirts i størrelse lille, mellem, stor og ekstra stor. Disse T-shirts er defineret som et produkt, og de forskellige størrelser er defineret som varianter af produktet. T-shirts er pakket i kasser, og der kan være fem T-shirts i en kasse med undtagelse af de ekstra store, hvor der er kun plads til fire T-shirts. Virksomheden ønsker at spore de forskellige varianter af sine T-shirts i enheden **Styk**, men sælger T-shirts i enheden **Kasser**. Konverteringen mellem lagerenheden og salgsenheden er 1 kasse = 5 stk. undtagen varianten ekstra stor, hvor konverteringen er 1 kasse = 4 styk.

### <a name="set-up-a-product-for-unit-conversion-per-variant"></a>Konfigurere et produkt til enhedsomregning pr. variant

Produktvarianter kan kun oprettes for produkter af **produktundertypen**: **Produktmaster**. Du kan finde flere oplysninger i [Oprette en produktmaster](tasks/create-product-master.md).

Funktionen er ikke aktiveret for produkter, der er konfigureret til fastvægtprocesser. 

Når produktmasteren er oprettet med frigivne produktvarianter, kan du angive enhedsomregninger pr. variant. Du kan finde menupunktet, hvor du kan åbne siden til enhedsomregning i forbindelse med et produkt eller en produktvariant på følgende sider.

-   Siden **Produktdetaljer**
-   Siden **Oplysninger om frigivne produkter**
-   Siden **Frigivne produktvarianter**

Når du åbner siden **Enhedsomregning** i forbindelse med en produktmaster eller en frigivet produktvariant, kan du vælge, om du vil definere enhedsomregningen for produktet eller for en produktvariant. Det gør du ved at vælge enten **Produktvariant** eller **Produkt** i feltet **Opret konvertering for**.

### <a name="product-variant"></a>Produktvariant

Hvis du vælger **Produktvariant**, kan du vælge, hvilken variant du vil definere enhedsomregning for, i feltet **Produktvariant**.

### <a name="product"></a>Produkt

Hvis du vælger **Produkt**, kan du konfigurere en enhedsomregning for produktmasteren. Denne enhedsomregning skal gælde for alle produktvarianter uden defineret enhedsomregning.

### <a name="example"></a>Eksempel

En produktmaster, **T-shirt**, har fire frigivne produktvarianter: lille, mellem, stor og ekstra stor. T-shirts er pakket i kasser, og der kan være fem T-shirts i en kasse med undtagelse af de ekstra store, hvor der er kun plads til fire T-shirts.

Først skal du åbne siden **Enhedsomregning** fra siden Frigivne produktdetaljer for **T-shirt.**

På siden **Enhedsomregning** skal du definere enhedsomregningen for produktvarianten ekstra stor.

| **Felt**             | **Indstilling**             |
|-----------------------|-------------------------|
| Opret konvertering for | Produktvariant         |
| Produktvariant       | T-shirt : : Ekstra stor : : |
| Fra enhed             | Kasser                   |
| Faktor                | 4                       |
| Til enhed               | Styk                  |

De frigivne produktvarianter lille, mellem og stor har samme enhedsomregning mellem enhedens Kasser og styk, hvilket betyder, at du kan definere enhedsomregningen for disse produktvarianter på produktmasteren.

| **Felt**             | **Indstilling** |
|-----------------------|-------------|
| Opret konvertering for | Produkt     |
| Produkt               | T-shirt     |
| Fra enhed             | Kasser       |
| Faktor                | 5           |
| Til enhed               | Styk      |

### <a name="using-excel-to-update-the-unit-conversions"></a>Bruge Excel til at opdatere enhedsomregningerne

Hvis et produkt har mange produktvarianter med forskellige enhedsomregninger, er det en god ide at eksportere enhedsomregninger fra siden **Enhedsomregning** til et Excel-regneark, opdatere konverteringerne og derefter publicere dem tilbage til Supply Chain Management.

Muligheden for at eksportere til Excel og publicere ændringerne tilbage til Supply Chain Management aktiveres fra menupunktet **Åbn i Microsoft Office** i handlingsruden på siden **Enhedsomregning**.
