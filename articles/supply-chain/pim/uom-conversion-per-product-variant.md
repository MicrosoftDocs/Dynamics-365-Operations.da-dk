---
title: Måleenhedskonvertering pr. produktvariant
description: Dette emne beskriver, hvordan du konfigurerer måleenhedskonverteringer for produktvarianter. Emnet indeholder et eksempel på opsætningen.
author: johanhoffmann
manager: tfehr
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: UnitOfMeasureConversion
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: 5f327d1d0b38ad724da6a302cefc115262317812
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001693"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a>Måleenhedskonvertering pr. produktvariant

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du konfigurerer måleenhedskonverteringer for forskellige produktvarianter.

I stedet for at oprette flere individuelle produkter, der skal vedligeholdelse, kan du bruge produktvarianter til at oprette variationer af et enkelt produkt. En produktvariant kan f.eks. være en t-shirt af en given størrelse og farve.

Tidligere kunne enhedsomregninger kun konfigureres på produktmasteren. Derfor har alle produktvarianter de samme regler for enhedsomregning. Men når funktionen *Enhedsomregninger for produktvarianter*, er slået til, hvis t-shirts sælges i kasser, og antallet af t-shirts, der kan pakkes i en kasse, afhænger af størrelsen på T-shirts, kan du nu konfigurere enhedsomregninger mellem de forskellige t-shirt-størrelser og de kasser der bruges til pakning.

## <a name="turn-on-the-feature-in-your-system"></a>Aktivere funktionen i systemet

Hvis du ikke allerede kan se denne funktion i dit system, skal du gå til [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og aktivere funktionen *Enhedsomregninger for produktvarianter*.

## <a name="set-up-a-product-for-unit-conversion-per-variant"></a>Konfigurere et produkt til enhedsomregning pr. variant

Produktvarianter kan kun bruges til produkter, der er produktmastere. Du kan finde flere oplysninger i [Oprette en produktmaster](tasks/create-product-master.md). Funktionen *Enhedsomregninger for produktvarianter* er ikke tilgængelig for produkter, der er konfigureret til fastvægtsprocesser.

Udfør følgende trin for at konfigurere en produktmaster til at understøtte enhedsomregning pr. variant:

1. Gå til **Administration af produktoplysninger \> Produkter \> Produktmastere**.
1. Opret eller åbn en produktmaster for at gå til siden **Produktdetaljer**.
1. Angiv indstillingen **Aktivér enhedsomregning** til *Ja*.
1. Gå til handlingsruden, og vælg **Enhedsomregninger** i gruppen **Opsætning** under fanen **Produkt**.
1. Siden **Enhedsomregninger** åbnes. Vælg én af følgende faner:

    - **Omregninger i klasser** – vælg denne fane for at konvertere mellem enheder, der tilhører samme enhedsklasse.
    - **Omregninger mellem klasser** – vælg denne fane for at konvertere mellem enheder, der tilhører forskellige enhedsklasse.

1. Vælg **Ny** for at tilføje en ny enhedsomregning.
1. Indstil feltet **Opret omregning for** til en af følgende værdier:

    - **Produkt** – hvis du vælger denne værdi, kan du konfigurere en enhedsomregning for produktmasteren. Denne enhedsomregning vil blive brugt som reserve for alle produktvarianter, der ikke er defineret en enhedsomregning for.
    - **Produktvariant** – hvis du vælger denne værdi, kan du konfigurere en enhedsomregning for en specifik produktvariant. Brug feltet **Produktvariant** til at vælge varianten.

    ![Tilføje en ny enhedsomregning](media/uom-new-conversion.png "Tilføje en ny enhedsomregning")

1. Brug de andre felter, der er angivet, til at konfigurere din enhedsomregning.
1. Vælg **OK** for at gemme den nye enhedsomregning.

> [!TIP]
> Du kan åbne siden **Enhedsomregninger** for et produkt eller en produktvariant fra en af følgende sider:
> 
> - Produktdetaljer
> - Frigivne produktdetaljer
> - Frigivne produktvarianter

## <a name="example-scenario"></a>Eksempelscenario

I dette scenarie sælger et firma t-shirts i størrelserne lille, mellem, stor og ekstra stor. Disse t-shirts er defineret som et produkt, og de forskellige størrelser er defineret som varianter af det pågældende produkt. T-shirtene er pakket i kasser. I størrelser lille, mellem og stor kan der være fem t-shirts i hver kasse. Men i størrelsen ekstra stor er der kun plads til fire t-shirts i hver kasse.

Virksomheden ønsker at spore de forskellige varianter i enheden *Styk*, men sælger dem i enheden *Kasser*. I størrelserne lille, mellem og stor er omregningen mellem lagerenheden og salgsenheden 1 kasse = 5 stk. I størrelsen ekstra stor er omregningen 1 kasse = 4 styk.

1. På siden **Frigivne produktdetaljer** for produktet **T-shirt** skal du åbne siden **Enhedsomregninger**.
1. På siden **Enhedsomregning** skal du konfigurere følgende enhedsomregning for den frigivning produktvariant **Ekstra stor**.

    | Felt                 | Indstilling                 |
    |-----------------------|-------------------------|
    | Opret konvertering for | Produktvariant         |
    | Produktvariant       | T-shirt : : Ekstra stor : : |
    | Fra enhed             | Kasser                   |
    | Faktor                | 4                       |
    | Til enhed               | Styk                  |

1. Da produktvarianterne **Lille**, **Mellem** og **Stor** alle har samme enhedsomregning mellem *Kasse*- og *Styk*-enheder, kan du definere følgende enhedsomregning for dem på produktmasteren.

    | Felt                 | Indstilling |
    |-----------------------|---------|
    | Opret konvertering for | Produkt |
    | Produkt               | T-shirt |
    | Fra enhed             | Kasser   |
    | Faktor                | 5       |
    | Til enhed               | Styk  |

## <a name="using-excel-to-update-the-unit-conversions"></a>Bruge Excel til at opdatere enhedsomregningerne

Hvis et produkt har mange produktvarianter, der har forskellige enhedsomregninger, er det en god ide at eksportere enhedsomregninger til en Microsoft Excel-projektmappe, opdatere dem og derefter udgive dem igen i Dynamics 365 Supply Chain Management.

Hvis du vil eksportere enhedsomregninger til Excel, skal du på siden **Enhedsomregninger** vælge **Åbn i Microsoft Office** i handlingsruden.

## <a name="additional-resources"></a>Yderligere ressourcer

[Administrere måleenhed](tasks/manage-unit-measure.md)
