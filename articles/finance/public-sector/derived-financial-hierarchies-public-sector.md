---
title: Afledte finansielle hierarkier i den offentlige sektor
description: I denne artikel beskrives de funktioner for afledte økonomiske hierarkier, der er tilgængelige for den offentlige sektor.
author: v-kiarnd
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResCategory, EcoResCategoryHierarchyListPage, EcoResCategoryHierarchyRole, LedgerDerivedFinHierarchies, LedgerDerivedFinHierarchyFilterResults, LedgerDerivedFinHierarchyLegalEntities
audience: Application User
ms.reviewer: twheeloc
ms.custom: 20911
ms.assetid: a1b30d2a-a370-402a-b3bd-d562adca55f0
ms.search.region: Global
ms.search.industry: Public sector
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 95660051cadc4a4dedc13d1380b55209fd8d6a25
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891454"
---
# <a name="derived-financial-hierarchies-in-the-public-sector"></a>Afledte finansielle hierarkier i den offentlige sektor

[!include [banner](../includes/banner.md)]

I denne artikel beskrives de funktioner for afledte økonomiske hierarkier, der er tilgængelige for den offentlige sektor. 

For at opfylde CGAC-krav (Government-wide Accounting Classification) skal organisationer i den offentlige sektor bruge afledte finansielle hierarkier for at indsamle og analysere bogførte posteringsdata for specifikke hovedkontonumre, fulde kontonumre og økonomiske dimensionsværdier. 

Kategorihierarkier konfigureres normalt for at klassificere posteringer til rapportering og analyse ud fra de økonomiske dimensioner i en kontostruktur på bogføringstidspunktet. Ved hjælp af kategorihierarkier med kategoritypen Afledt finansielt hierarki kan du oprette filterregler, der opretter økonomiske kategorier og de dimensionsværdier, der ikke er en del af kontonummeret. De økonomiske kategorier og dimensionsværdier, der er defineret i filterreglerne, er afledt fra kontonummerets dimensionsværdier, som bruges i de bogførte posteringer.

Afledte finansielle hierarkier giver dig en mere fleksibel tilgang i forhold til at gruppere posteringer til ad hoc-analyse. Hierarkierne giver dig mulighed for at kategorisere posteringer uden at skulle udvide kontostrukturen, så den omfatter de ekstra kategorier eller dimensioner, du vil spore.

## <a name="example"></a>Eksempel
En organisation har et medarbejdersundhedsprogram og et medarbejderuddannelsesprogram. Disse programmer er ikke knyttet til økonomiske dimensioner. Hvis du vil indsamle kontonumre, der er brugt i de bogførte posteringer til disse programmer, kan du gøre følgende:

-   **Oprette kategorihierarkier og de afledte finansielle hierarkier:** Opret et kategorihierarki, der hedder "Medarbejderprogrammer", med en overordnet node, der hedder "Programmer", og to underordnede noder, der hedder "Medarbejdersundhed" og "Medarbejderuddannelse". Tildel kategoritypen **Afledt økonomisk hierarki** til kategorihierarkiet "Medarbejderprogrammer". Knyt det afledte finansielle hierarki for "Medarbejderprogrammer" til den juridiske enhed.
-   **Konfigurere filterregler** Brug siden **Afledte økonomiske hierarkier** til at oprette filterregler for hovedkonti og økonomiske dimensionsværdier, der er knyttet til noderne "Medarbejdersundhed" og "Medarbejderuddannelse" i det afledte finansielle hierarki for "Medarbejderprogrammer". **Tip!** Hvis du vil angive mere end én dimensionsværdi i et filter, skal du bruge et komma uden mellemrum som skilletegn. Angiv for eksempel 100,110 eller Frynsegoder,Forsikring.
-   **Analysere bogførte transaktionsdata:** I de filtrerede resultater skal du se på kontonumre og kontooplysninger og oplysninger om økonomisk dimension.








[!INCLUDE[footer-include](../../includes/footer-banner.md)]
