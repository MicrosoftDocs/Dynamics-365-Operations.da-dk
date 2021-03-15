---
title: Konfigurere et menupunkt for en mobilenhed for at oprette en pluklinjeoversigt
description: I dette emne forklares det, hvordan du definerer, hvornår der skal vises en liste over alle arbejdslinjer for lagermedarbejdere, der behandler lagerarbejde på en mobilenhed. Denne funktion kan være nyttig for lagermedarbejdere, der ofte kræver en oversigt over pluklinjerne i en arbejdsordre, så de kan optimere plukrækkefølgen.
author: MarkusFogelberg
manager: tfehr
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 433ed2152c47dbe698a640b099cb34727fe63452
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989687"
---
# <a name="set-up-a-mobile-device-menu-item-to-provide-a-pick-line-overview"></a>Konfigurere et menupunkt for en mobilenhed for at oprette en pluklinjeoversigt

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

I dette emne forklares, hvordan du kan konfigurere indstillinger, der er relateret til pluklinjeoversigten for menupunkter for mobilenheder, der bruges til at behandle plukarbejde. Med pluklinjeoversigten kan lagermedarbejderne få vist og vælge fra en liste over alle de arbejdslinjer, der er relateret til deres aktuelle opgave. Denne funktion kan hjælpe arbejdere med at optimere deres plukrækkefølge. Funktionen indeholder indstillinger, der erstatter standardknappen **Spring over**, så arbejderne kan gå gennem linjerne én ad gangen i en fast rækkefølge. (Det er dog stadig muligt at bruge denne knap).

Administratorer kan konfigurere de enkelte menupunkter individuelt for at styre, hvordan, hvornår og hvor lagerstedsappen viser pluklinjeoversigten.

## <a name="turn-on-the-work-pick-line-overview-feature"></a>Aktivere funktionen Arbejdspluklinje, oversigt

Før du kan bruge denne funktion, skal den være slået til i dit system. Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov. I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:

- **Modul:** _Lokationsstyring_
- **Funktionsnavn:** _Arbejdspluklinje, oversigt_

## <a name="configure-menu-items-to-show-a-list-of-all-work-lines"></a>Konfigurere menupunkter for at få vist en liste over alle arbejdslinjer

Du kan konfigurere et menupunkt for en mobilenhed for at oprette en pluklinjeoversigt ved at følge nedenstående trin.

1. Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Menupunkter i mobilenhed**.
1. Vælg eller opret et menupunkt, der er relateret til plukarbejde, og angiv følgende værdier:

    - **Tilstand:** *Arbejde*
    - **Brug eksisterende arbejde:** *Ja*
    - **Styret af:** *Brugerstyret* eller *Systemstyret*

    Du kan finde flere oplysninger om, hvordan du opretter menupunkter og bruger de forskellige indstillinger, der er tilgængelige på siden **Menupunkter for mobilenheder**, i [Konfigurere mobilenheder til lagerstedsarbejde](configure-mobile-devices-warehouse.md).

1. I oversigtspanelet **Generelt** kan du konfigurere funktionen ved at angive feltet **Vis liste over arbejdslinje** til en af følgende værdier:

    - **Vis kun efter anmodning** – arbejdere kan vælge at få vist pluklinjelisten ved at vælge **Spring til** i lagerstedsappen.
    - **Vis ved start af alle pluk** – medarbejdere kan se listen, hver gang de påbegynder eller afslutter en pluklinje. De kan også få vist listen igen ved at vælge knappen **Spring til** i lagerstedsappen.
    - **Vis kun ved starten af første pluk** – medarbejderne ser listen, hver gang de påbegynder et nyt plukarbejde, men ikke efter hver linje. De kan også få vist listen igen ved at vælge knappen **Spring til** i lagerstedsappen.
    - **Vis aldrig** – standardknappen **Spring over** i lagerstedsappen vises, og visning af listen over arbejdslinjer er slået fra. Knappen **Spring over** giver arbejdere mulighed for at gå gennem linjerne én ad gangen i en fast rækkefølge. De kan også gå gennem listen så mange gange, de har brug for, indtil alle linjer er blevet behandlet.

1. Vælg **Gem** i handlingsruden.

    Hvis du angiver feltet **Vis liste over arbejdslinje** til en hvilken som helst værdi undtagen *Vis aldrig*, bliver knappen **Feltliste** i handlingsruden tilgængelig.

1. Vælg **Feltliste** i handlingsruden.
1. På siden **Feltliste** skal du konfigurere de oplysninger, som lagerstedsappen viser for hver linje på listen.

    - Feltet **Primært kontrolelement** er altid angivet til *LineNum*. Derfor begynder hver række på listen med et linjenummer.
    - Brug de resterende **Visningsfelt**-felter til at tilføje op til syv yderligere visningsfelter efter dit behov. I hvert **Visningsfelt**-felt skal du vælge navnet på et arbejdslinjefelt. Hver linje vil derefter vise en værdi for det pågældende felt. Værdierne vises i den rækkefølge, du vælger her. Du kan lade nogle af **Visningsfelt**-felterne være tomme, hvis du ikke har brug for alle syv værdier.

1. Vælg **Gem** i handlingsruden, og luk derefter siden **Feltliste**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]