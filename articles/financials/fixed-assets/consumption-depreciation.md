---
title: Forbrugsafskrivning
description: Denne artikel indeholder en oversigt over afskrivningsmetoden Forbrug.
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13751
ms.assetid: d25a681f-49a5-4bfc-aa76-1c6373e35dd8
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f48eabb3c07f53e8a086be4e0d1597b8ea4d401b
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="consumption-depreciation"></a>Forbrugsafskrivning

[!include [banner](../includes/banner.md)]

Denne artikel indeholder en oversigt over afskrivningsmetoden Forbrug.

Hvis du konfigurerer en afskrivningsprofil for anlægsaktiver og vælger **Forbrug** i feltet **Metode** på siden **Afskrivningsprofiler**, tildeles anlægsaktiver til denne afskrivningsprofilen baseret på deres brug. Du behøver ikke at definere procenter og intervaller på siden **Afskrivningsprofiler**. Når du har oprettet en afskrivningsprofil, der bruger metoden Forbrug, kan du angive metoden på forskellige måder.

## <a name="set-up-and-use-consumption-depreciation"></a>Definere og bruge forbrugsafskrivning
1.  Opret afskrivningsprofilen på siden **Afskrivningsprofiler**. I forbindelse med beregninger af forbrug skal afskrivningsprofilen have et id og et navn, og **Forbrug** skal være valgt i feltet **Metode**.
2.  På siden **Forbrugsfaktorer** skal du konfigurere forbrugsfaktorer. De enkelte forbrugsfaktorer skal have et id og et navn samt en forbrugsfaktor, der er angivet som enten en mængde eller procent.
3.  På siden **Forbrugsenheder** skal du konfigurere forbrugsenheder. Hver forbrugsenhed skal have et id og et navn. Afskrivningsenheder bruges til at beregne forbrugsafskrivning på siden **Forbrugsafskrivning**. En km (kilometer), et kg (kilogram) eller en time er eksempler på enheder.
4.  På siden **Anlægsaktiver** skal du definere individuelle anlægsaktiver. Til de enkelte anlægsaktiver skal du vælge værdimodeller og afskrivningsmodeller, der har afskrivningsprofiler. Du skal oprette værdimodeller eller afskrivningsmodeller til forbrugsafskrivning, hvis du har anlægsaktiver, der bruger afskrivningsprofiler, som er baseret på metoden Forbrug. Denne konfiguration udføres enten under fanen **Afskrivning** på siden **Værdimodeller** eller i oversigtspanelet **Generelt** på siden **Afskrivningsprofil**. Du kan bruge samme værdimodel til flere anlægsaktiver. Afskrivningsmetoder er del af den værdimodel eller afskrivningskladde, som du vælger til hvert anlægsaktiv. Du kan ikke tilføje eller redigere afskrivningsprofiler direkte på siden **Anlægsaktiver**. Du kan kun ændre afskrivningsprofilerne på siden **Afskrivningsprofiler**.
5.  På siden **Værdimodeller** eller siden **Afskrivningsmodeller** skal du i feltgruppen **Forbrugsafskrivning** angive oplysninger i følgende felter:
    -   Forbrugsfaktor
    -   Enhed
    -   Enhedsafskrivning
    -   Forventet forbrug

    I feltet **Bogført forbrug** vises forbrugsafskrivning i enheder, der allerede er bogført enten for kombinationen af anlægsaktiv og værdimodel eller for afskrivningsmodellen. Værdien i dette felt kan ikke opdateres manuelt.

## <a name="examples"></a>Eksempler
### <a name="example-1"></a>Eksempel 1

Der er defineret følgende forbrugsfaktor pr. 31. januar:

-   Antallet er 1.000.
-   Den enhedsafskrivningspris, der er angivet for anlægsaktivet, er 1,5.

Afskrivningsforslaget den 31. januar er som følger: Antal × Enhedsafskrivning 1.000 × 1,5 = 1.500, hvis den faktor, der er angivet for anlægsaktivet, er en procentfaktor, den mængde, der anslås i feltet **Forkalkuleret forbrug** for værdimodellen for anlægsaktivet, ganges med den procentdel, der er angivet for den valgte slutdato. Resultatmængden foreslås derefter som afskrivningsmængden for perioden.

### <a name="example-2"></a>Eksempel 2

Der er defineret følgende faktorer for forbrugsafskrivning pr. 31. januar:

-   Procentsatsen er 10 procent.
-   Den enhedsafskrivningspris, der er angivet for anlægsaktivet, er 1,5.
-   Det forkalkulerede antal for anlægsaktivet er 2.000.

Afskrivningsforslaget den 31. januar er som følger: Anslået mængde × Procent × Enhedsafskrivning 2.000 × 0,10 × 1,5 = 300




