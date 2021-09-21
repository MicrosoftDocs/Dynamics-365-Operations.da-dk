---
title: Oversigt over tilføjelsesprogram for lagersynlighed
description: Dette emne forklarer, hvad lagersynlighed er og beskriver funktionerne.
author: sherry-zheng
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 644eb0d682c35bd604c188aa02e4a6c69b3ff209
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7474982"
---
# <a name="inventory-visibility-add-in-overview"></a>Oversigt over tilføjelsesprogram for lagersynlighed

[!include [banner](../includes/banner.md)]

Tilføjelsesprogrammet Lagersynlighed (kaldes også *Lagersynlighed*) er en uafhængig og meget skalerbar mikrotjeneste, der muliggør sporing af disponibel lagerbeholdning i realtid. Den giver derfor en global visning af lageret.

Eksterne systemer får adgang til tjenesten via RESTful API'er. På den måde kan de enten oprette en forespørgsmål om disponibel lagerbeholdning for et bestemt sæt dimensioner eller foretage ændringer af lageret for forskellige brugerdefinerede datakilder.

Som en mikrotjeneste, der er baseret på Microsoft Dataverse, muliggør udvidelse med Lagersynlighed. Du kan bruge Power Apps til at bygge apps. Du kan også anvende Power BI til at tilpasse funktioner, der opfylder dine forretningsbehov.

Du kan integrere Lagersynlighed med flere tredjepartssystemer ved at angive konfigurationsindstillinger for standardiserede lagerdimensioner og konfigurere transaktionstyper. Lagersynlighed understøtter også tilpasset udvidelse via konfigurerbare beregnede antal.

## <a name="inventory-visibility-integration-with-dynamics-365-supply-chain-management"></a>Integration af Lagersynlighed i Dynamics 365 Supply Chain Management

Den integrerede løsning trækker lagerdata fra Dynamics 365 Supply Chain Management og sporer løbende lagerændringerne. Du kan finde flere oplysninger under [Installere og konfigurere lagersynlighed](inventory-visibility-setup.md) og [konfigurere lagersynlighed](inventory-visibility-configuration.md).

## <a name="get-a-global-view-of-inventory"></a>Få en global visning af lageret

Den integrerede løsning gør det muligt at definere dine egne datakilder og centralisere lagerdata. Du kan finde flere oplysninger i [Konfiguration af Lagersynlighed](inventory-visibility-configuration.md).

Du kan få vist lageret på to måder:

- Send en forespørgsel via API'en med høj ydeevne. Denne API kan returnere lagerdata i næsten realtid direkte fra en cachelagret forekomst. Du kan finde kontrakter og prøver i [Offentlige API'er for Lagersynlighed](inventory-visibility-api.md).
- Vis den ubehandlede liste over disponibel lagerbehandling. Denne liste synkroniseres jævnligt fra en cachelagret forekomst og kan ses i Dataverse. Du kan finde flere oplysninger i [appen Lagersynlighed](inventory-visibility-power-platform.md).

## <a name="soft-reservations"></a>Foreløbige reservationer

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Foreløbige reservationer anvendes, når en virksomhed skal reservere en bestemt antal produkter f.eks. for at understøtte opfyldelsen af en salgsordre, der forebygger oversalg. Når en salgsordre oprettes og bekræftes i Supply Chain Management eller andre ordrestyringssystemer, sendes der en anmodning om reservering af antallet til Lagersynlighed. Med Lagersynlighed kan du reservere produkter, der har dimensionsdetaljer og specifikke lagertransaktionstyper. (Du kan finde flere oplysninger i [appen Lagersynlighed](inventory-visibility-power-platform.md)). Når antallet er reserveret korrekt, returneres et reservations-id. Du kan bruge dette reservations-id til at oprette forbindelse til den oprindelige ordre i Supply Chain Management eller andre ordrestyringssystemer.

Funktionen er designet, så en reservation i Lagersynlighed ikke ændrer det samlede antal. Den markerer i stedet kun det reserverede antal. (Derfor kaldes det en *foreløbig reservation*). Det foreløbigt reserverede antal kan modkonteres, når produkterne forbruges i Supply Chain Management, eller af et tredjepartssystem, ved at kalde API'en igen for at foretage et mængdefradrag og opdatere det samlede antal i Lagersynlighed. Du kan finde flere oplysninger i [Reservationer i Lagersynlighed](inventory-visibility-reservations.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
