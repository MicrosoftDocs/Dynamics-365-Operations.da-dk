---
title: Karruselmodul
description: Dette emne omhandler karruselmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: f279d7db0a92df9e64b1d3f6ca01c65ca1478d79
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025775"
---
# <a name="carousel-module"></a>Karruselmodul


[!include [banner](includes/banner.md)]

Dette emne omhandler karruselmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Et karruselmodul bruges til at placere flere kampagnevarer (herunder detaljerede billeder) i et roterende karruselbanner, som kunderne kan gennemse. En detailhandler kan f. eks. bruge et karruselmodul på en hjemmeside for at vise flere nye produkter eller kampagner.

Du kan tilføje indholdsblokmoduler inde i et karruselmodul. Egenskaberne for karruselmodulet definerer derefter, hvordan disse moduler gengives.

## <a name="examples-of-carousel-modules-in-e-commerce"></a>Eksempler på karruselmoduler i e-handel

- En karrusel, der indeholder flere kampagnemoduler, kan bruges på en startside.
- En karrusel, der indeholder flere kampagnemoduler, kan bruges på en side med produktdetaljer.
- En karrusel kan bruges på en hvilken som helst marketingside til at vise flere kampagner eller produkter.

## <a name="carousel-module-properties"></a>Egenskaber for karruselmodul

| Egenskabsbetegnelse             | Værdi                 | Beskrivelse |
|---------------------------|-----------------------|-------------|
| Automatisk afspilning                  | **Sand** eller **Falsk** | Hvis værdien er angivet til **Sand**, sker overgangen mellem varerne inde i karrusellen automatisk. Hvis værdien er angivet til **Falsk**, sker der ingen overgang, medmindre kunden bruger tastaturet eller musen til at flytte fra en vare til den næste. |
| Interval for glidende interval | En værdi i sekunder    | Intervallet for overgange mellem varerne. |
| Overførselstype           | **Dias** eller **Udtoning** | Overgangseffekten mellem varer. |
| Skjul karruselslipper     | **Sand** eller **Falsk** | Hvis værdien er angivet til **Sand**, skjules karruselslipperen og sekvensindikatoren. |
| Tillad afvisning af karrusel    | **Sand** eller **Falsk** | Hvis værdien er angivet til **Sand**, kan brugerne afvise karrusellen. |

## <a name="add-a-carousel-module-to-a-page"></a>Føje et karruselmodul til en side

Hvis du vil føje et karruselmodul til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.

1. Opret en sideskabelon med navnet **karruselskabelon**.
1. På pladsen **Brødtekst** skal du tilføje et **Standardside**-modul.
1. Tjek skabelonen ind, og publicer den. 
1. Brug den karruselskabelon, som du netop har oprettet, til at oprette en side med navnet **karruselside**.
1. Tilføj et containermodul på pladsen **Hoved** på den nye side. 
1. Angiv værdien **Bredde** til **Fyld skærm** i ruden til højre.
1. Føj et karruselmodul til containermodulet under **Sidedisposition**.
1. Føj et indholdsblokmodul til karruselmodulet. Angiv egenskaberne for indholdsblokmodulet ved at angive **Overskrift**, **Link**, **Layout** og andre egenskaber.
1. Tilføj og konfigurer et andet indholdsblokmodul.
1. Angiv yderligere egenskaber for karruselmodulet efter behov.
1. Gem siden, og se en forhåndsvisning af den. Siden skal vise en karrusel, der indeholder to moduler (et hero-modul og et funktionsmodul). Du kan ændre flere egenskaber for karrusel-, hero- og med funktionsmoduler for at opnå den ønskede effekt.
1. Afslut redigeringen af siden, og udgiv den.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over startsæt](starter-kit-overview.md)

[Kampagnebannermodul](add-alert.md)

[Tekstblokmodul](add-content-rich-block.md)

[Indholdsblokmodul](add-hero-module.md)

[Videoafspillermodul](add-video-player.md)
