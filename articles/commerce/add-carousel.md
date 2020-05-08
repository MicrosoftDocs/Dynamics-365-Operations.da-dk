---
title: Karruselmodul
description: Dette emne omhandler karruselmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 04/14/2020
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
ms.openlocfilehash: f399e4c5618b65b781fdd3ec835e841614579313
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269722"
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

1. Vælg **Ny** for at oprette en sideskabelon.
1. Angiv **Karruselskabelonskabelon** under **Skabelonnavn** i dialogboksen **Ny skabelon**, og vælg derefter **OK**.
1. På pladsen **Brødtekst** skal du tilføje et **Standardside**-modul.
1. Vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.  
1. Brug den karruselskabelon, som du netop har oprettet, til at oprette en side med navnet **Karruselside**.
1. Tilføj et containermodul på pladsen **Hoved** på den nye side. 
1. Angiv værdien **Bredde** til **Fyld skærm** i ruden til højre.
1. Føj et karruselmodul til containermodulet under **Sidedisposition**.
1. Føj et indholdsblokmodul til karruselmodulet. Angiv egenskaberne for indholdsblokmodulet ved at angive **Overskrift**, **Link**, **Layout** og andre egenskaber.
1. Tilføj og konfigurer et andet indholdsblokmodul.
1. Angiv yderligere egenskaber for karruselmodulet efter behov.
1. Vælg **Gem**, og vælg derefter **Vis** for at få vist siden. Siden skal vise en karrusel, der indeholder to moduler (et hero-modul og et funktionsmodul). Du kan ændre flere egenskaber for karrusel-, hero- og med funktionsmoduler for at opnå den ønskede effekt.
1. Vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over startsæt](starter-kit-overview.md)

[Kampagnebannermodul](add-alert.md)

[Tekstblokmodul](add-content-rich-block.md)

[Indholdsblokmodul](add-hero-module.md)

[Videoafspillermodul](add-video-player.md)
