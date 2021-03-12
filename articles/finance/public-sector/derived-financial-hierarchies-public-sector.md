---
title: Afledte finansielle hierarkier i den offentlige sektor
description: I denne artikel beskrives de funktioner for afledte økonomiske hierarkier, der er tilgængelige for den offentlige sektor.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResCategory, EcoResCategoryHierarchyListPage, EcoResCategoryHierarchyRole, LedgerDerivedFinHierarchies, LedgerDerivedFinHierarchyFilterResults, LedgerDerivedFinHierarchyLegalEntities
audience: Application User
ms.reviewer: roschlom
ms.custom: 20911
ms.assetid: a1b30d2a-a370-402a-b3bd-d562adca55f0
ms.search.region: Global
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 886eeab582934ca86a08114fb3f3adefbdbd717f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971171"
---
# <a name="derived-financial-hierarchies-in-the-public-sector"></a>Afledte finansielle hierarkier i den offentlige sektor

[!include [banner](../includes/banner.md)]

I denne artikel beskrives de funktioner for afledte økonomiske hierarkier, der er tilgængelige for den offentlige sektor. 

For at opfylde CGAC-krav (Government-wide Accounting Classification) skal organisationer i den offentlige sektor bruge afledte finansielle hierarkier for at indsamle og analysere bogførte posteringsdata for specifikke hovedkontonumre, fulde kontonumre og økonomiske dimensionsværdier. 

Kategorihierarkier konfigureres normalt for at klassificere posteringer til rapportering og analyse ud fra de økonomiske dimensioner i en kontostruktur på bogføringstidspunktet. Ved hjælp af kategorihierarkier med kategoritypen Afledt finansielt hierarki kan du oprette filterregler, der opretter økonomiske kategorier og de dimensionsværdier, der ikke er en del af kontonummeret. De økonomiske kategorier og dimensionsværdier, der er defineret i filterreglerne, er afledt fra kontonummerets dimensionsværdier, som bruges i de bogførte posteringer.

Afledte finansielle hierarkier giver dig en mere fleksibel tilgang i forhold til at gruppere posteringer til ad hoc-analyse. De giver dig mulighed for at kategorisere posteringer uden at skulle udvide kontostrukturen, så den omfatter de ekstra kategorier eller dimensioner, du vil spore.

## <a name="example"></a>Eksempel
En organisation har et medarbejdersundhedsprogram og et medarbejderuddannelsesprogram. Disse programmer er ikke knyttet til økonomiske dimensioner. Hvis du vil indsamle kontonumre, der er brugt i de bogførte posteringer til disse programmer, kan du gøre følgende:

-   **Oprette kategorihierarkier og de afledte finansielle hierarkier:** Opret et kategorihierarki, der hedder "Medarbejderprogrammer", med en overordnet node, der hedder "Programmer", og to underordnede noder, der hedder "Medarbejdersundhed" og "Medarbejderuddannelse". Tildel kategoritypen **Afledt økonomisk hierarki** til kategorihierarkiet "Medarbejderprogrammer". Knyt det afledte finansielle hierarki for "Medarbejderprogrammer" til den juridiske enhed.
-   **Konfigurere filterregler** Brug siden **Afledte økonomiske hierarkier** til at oprette filterregler for hovedkonti og økonomiske dimensionsværdier, der er knyttet til noderne "Medarbejdersundhed" og "Medarbejderuddannelse" i det afledte finansielle hierarki for "Medarbejderprogrammer". **Tip!** Hvis du vil angive mere end én dimensionsværdi i et filter, skal du bruge et komma uden mellemrum som skilletegn. Angiv for eksempel 100,110 eller Frynsegoder,Forsikring.
-   **Analysere bogførte transaktionsdata:** I de filtrerede resultater skal du se på kontonumre og kontooplysninger og oplysninger om økonomisk dimension.






