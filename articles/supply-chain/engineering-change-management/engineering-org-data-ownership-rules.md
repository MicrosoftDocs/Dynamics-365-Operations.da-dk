---
title: Tekniske virksomheder og regler for ejerskab af data
description: Dette emne forklarer, hvordan du kan bruge et eller flere tekniske virksomheder til at sikre, at masterdata til produkter er centralt oprettet og vedligeholdt. En teknisk virksomhed repræsenterer det firma, der ejer tekniske produkter og de relevante tekniske data.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgEngineeringOrganization
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 837960a628ef03df4d73909e96713e256d0f5e60
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5262303"
---
# <a name="engineering-companies-and-data-ownership-rules"></a>Tekniske virksomheder og regler for ejerskab af data

[!include [banner](../includes/banner.md)]

## <a name="engineering-companies-and-operational-companies"></a>Tekniske virksomheder og driftsselskaber

For at sikre, at masterdata til produkter er centralt oprettet og vedligeholdt, kan du bruge en eller flere *tekniske virksomheder*. En teknisk virksomhed ejer de tekniske produkter og deres relevante tekniske data. Den har altid forbindelse til (baseret på) en eksisterende *juridisk enhed*, som også er en virksomhed. Via denne forbindelse opretter systemet et centralt indgangspunkt for alle relevante tekniske data til tekniske produkter i den tekniske virksomhed. I dette centrale indgangspunkt oprettes der tekniske produkter, og der vedligeholdes tekniske data. Herfra vil de tekniske produkter og tekniske data blive frigivet til *driftsselskaber*, som er andre juridiske enheder. (Yderligere oplysninger om frigivelsesstyring finder du i [Frigive produktstrukturer](release-product-structure.md)). Disse driftsselskaber bruger de tekniske data, som de er udviklet af den tekniske virksomhed. Alle logistiske data vedligeholdes lokalt af den enkelte tekniske virksomhed og driftsselskabet.

Hvis du vil oprette en teknisk virksomhed, skal du gå til **Teknisk ændringsstyring \> Konfiguration \> Tekniske organisationer**. Vælg **Ny**, angiv et navn til den tekniske virksomhed, og vælg den eksisterende virksomhed (juridisk enhed), som den er baseret på.

Hvis du integrerer med eksterne systemer til administration af produktlivscyklus (PLM), skal du oprette en afdeling (virksomhedstype), der bliver en ekstern virksomhed.

## <a name="engineering-product-categories-and-engineering-companies"></a>Tekniske produktkategorier og tekniske virksomheder

*Tekniske produktkategorier* er med til at sikre, at tekniske produkter oprettes i henhold til virksomhedens forretningsregler og fungerer efter behov. Du kan finde flere oplysninger om tekniske produktkategorier i [Tekniske versioner og tekniske produktkategorier](engineering-versions-product-category.md).

De enkelte tekniske produktkategorier tilhører en specifik teknisk virksomhed og kan kun oprette produkter, der tilhører den pågældende virksomhed. På samme måde tilhører rettigheden til vedligeholdelse af et teknisk produkt også den virksomhed, der er knyttet til produktets tekniske produktkategori.

## <a name="data-that-is-owned-by-the-engineering-company"></a>Data, der ejes af den tekniske virksomhed

Da den tekniske virksomhed ejer de teknisk relevante data, styrer den følgende processer:

- **Oprettelse af tekniske produkter:** Hver tekniske virksomhed kan kun oprette nye tekniske produkter, der er baseret på en teknisk produktkategori, som den ejer. I nogle tilfælde vedligeholder driftsselskaber deres egne lokale data, der er knyttet til disse produkter.
- **Oprettelse af tekniske versioner:** Når en virksomhed opretter et nyt teknisk produkt, opretter systemet automatisk en indledende teknisk version til den. Det er kun den tekniske ejervirksomhed, der kan oprette nye versioner af produktet.
- **Oprettelse og vedligeholdelse af tekniske attributter:** Når en virksomhed opretter et nyt teknisk produkt, føjer systemet automatisk tekniske attributter til det. Det er kun den tekniske ejervirksomhed, der kan oprette og vedligeholde værdierne for disse attributter. Yderligere oplysninger om tekniske attributter finder du i [Tekniske attributter og søgning efter tekniske attributter](engineering-attributes-and-search.md).
- **Oprettelse og vedligeholdelse af styklister, der er tilknyttet de tekniske versioner:** Den tekniske ejervirksomhed kan knytte en stykliste direkte til en teknisk produktversion. Når disse styklister frigives til andre juridiske enheder, begrænses ændringer af de tekniske data på styklisterne på følgende måder:

    - Driftsselskabet kan ikke fjerne frigivne styklistelinjer.
    - Tekniske felter på styklistelinjerne er skrivebeskyttede for driftsselskabet. Alle andre felter er logistiske implementeringsfelter og kan redigeres af driftsselskabet.
    - Driftsselskabet kan føje styklistelinjer til den samme stykliste. På denne måde kan den oprette lokale tilføjelser, f.eks. emballagematerialer eller smørevæsker.
    - Driftsselskabet kan tilføje en helt ny lokal stykliste. Denne ændring kan være påkrævet i de tilfælde, hvor der f.eks. ikke er angivet en stykliste under frigivelsen. Driftsselskabet ejer og vedligeholder disse lokale styklister. Du kan finde flere oplysninger om frigivelsesstyring i [Frigive produktstrukturer](release-product-structure.md).
    - Alle lokale styklister og styklistelinjer bevares, når den tekniske virksomhed opdaterer styklisten.

- **Oprettelse og vedligeholdelse af ruster, der er tilknyttet de tekniske versioner:** Den tekniske ejervirksomhed kan knytte en rute direkte til en teknisk produktversion. Når disse ruter frigives til andre juridiske enheder, begrænses ændringer af de tekniske data på ruterne på følgende måder:

    - De andre juridiske enheder kan ikke fjerne de tekniske data på ruterne.
    - De andre juridiske enheder kan føje operationer til ruten. På denne måde kan de tilføje lokale rutetrin.
    - Driftsselskaber kan tilføje helt nye lokale ruter. Denne ændring kan være påkrævet i de tilfælde, hvor du f.eks. ikke har angivet ruter under frigivelsen. Driftsselskaberne ejer og vedligeholder disse lokale ruter. Du kan finde flere oplysninger om frigivelsesstyring i [Frigive produktstrukturer](release-product-structure.md).
    - Alle ændringer, der foretages lokalt, bevares, når opdateringer fra den tekniske virksomhed frigives til ruterne igen.

- **Oprettelse og vedligeholdelse af tekniske dokumenter:** Den tekniske virksomhed kan tilknytte tekniske dokumenter til de enkelte tekniske versioner.

    - Når disse dokumenter frigives til andre juridiske enheder, er dokumenterne beskyttet mod at blive fjernet af driftsselskabet.
    - Andre juridiske enheder kan tilføje helt nye lokale dokumenter. Driftsselskabet ejer og vedligeholder disse lokale dokumenter.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]