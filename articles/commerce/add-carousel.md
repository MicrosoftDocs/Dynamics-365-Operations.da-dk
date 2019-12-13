---
title: Karruselmodul
description: Dette emne omhandler karruselmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: c2c5adc8ab2e0330f7b07e5153fd8332ab0203e5
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785231"
---
# <a name="carousel-module"></a>Karruselmodul

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dette emne omhandler karruselmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Et karruselmodul bruges til at placere flere kampagnevarer i en karrusel, som kunderne kan gennemse. Det er et særligt containermodul, der er vært for andre moduler. En detailhandler kan f. eks. bruge et karruselmodul på en hjemmeside for at vise flere nye produkter eller kampagner.

Du kan tilføje hero- og funktionsmoduler inde i et karruselmodul. Egenskaberne for karruselmodulet definerer derefter, hvordan disse moduler gengives.

## <a name="examples-of-carousel-modules-in-e-commerce"></a>Eksempler på karruselmoduler i e-handel

- En karrusel, der indeholder flere kampagnemoduler, kan bruges på en startside.
- En karrusel, der indeholder flere kampagnemoduler, kan bruges på en side med produktdetaljer.
- En karrusel kan bruges på en hvilken som helst marketingside til at vise flere kampagner eller produkter.

## <a name="carousel-module-properties"></a>Egenskaber for karruselmodul

| Egenskabsbetegnelse             | Værdi                                | Beskrivelse |
|---------------------------|--------------------------------------|-------------|
| Automatisk afspilning                  | **Sand** eller **Falsk**                | Hvis værdien er angivet til **Sand**, sker overgangen mellem varerne inde i karrusellen automatisk. Hvis værdien er angivet til **Falsk**, sker der ingen overgang, medmindre kunden bruger tastaturet eller musen til at flytte fra en vare til den næste. |
| Interval for glidende interval | En værdi i sekunder                   | Intervallet for overgange mellem varerne. |
| Animation af overgang      | **Dias** eller **Udtoning**                | Overgangseffekten. |
| Bredde                     | **Tilpas til container** eller **Udfyld skærm** | Hvis værdien er angivet til **Tilpas til container**, begrænses varerne i karrusellen til karrusellens bredde. Hvis værdien er angivet til **Udfyld skærm**, begrænses varerne ikke til karrusel bredden, men kan gå i fuldskærmstilstand. Du kan ændre værdien for at opnå det ønskede layout. |

## <a name="add-a-carousel-module-to-a-page"></a>Føje et karruselmodul til en side

Hvis du vil føje et karruselmodul til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.

1. Opret en sideskabelon med navnet **karruselskabelon**.
1. Tilføj et karruselmodul på pladsen **Hoved** på standardsiden.
1. Føj et hero-modul til karruselmodulet.
1. Føj et funktionsmodul til karruselmodulet.
1. Tjek skabelonen ind, og publicer den. 
1. Brug den karruselskabelon, som du netop har oprettet, til at oprette en side med navnet **karruselside**.
1. Tilføj et karruselmodul på pladsen **Hoved** på den nye side.
1. Angiv egenskaben **Bredde** i karruselmodulet til **Udfyld skærm**. 
1. Angiv egenskaben **Animation af overgang** til **Dias**.
1. Føj et hero-modul til karruselmodulet.
1. Tilføj et billede og en overskrift i hero-modulet, og vælg derefter **Gem**.
1. Føj et funktionsmodul til karruselmodulet.
1. Tilføj et billede, en overskrift og et tekstafsnit i funktionsmodulet.
1. Gem siden, og se en forhåndsvisning af den. Siden skal vise en karrusel, der indeholder to moduler (et hero-modul og et funktionsmodul). Du kan ændre flere egenskaber for karrusel-, hero- og med funktionsmoduler for at opnå den ønskede effekt.
1. Tjek siden ind, og publicer den.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over startsæt](starter-kit-overview.md)

[Påmindelsesmodul](add-alert.md)

[Indholdsrig blok-modul](add-content-rich-block.md)

[Indholdsplaceringsmodul](add-content-placement-modules.md)

[Funktionsmodul](add-feature-module.md)

[Hero-modul](add-hero-module.md)

[Videoafspillermodul](add-video-player.md)
