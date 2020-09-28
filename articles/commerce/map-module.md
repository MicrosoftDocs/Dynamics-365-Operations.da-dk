---
title: Kortmodul
description: Dette emne omhandler kortmoduler og beskriver, hvordan du kan konfigurere dem i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 07/31/2020
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
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: ca531e6cbf0a1044b0a13e5cdf42c7b4f0498fe5
ms.sourcegitcommit: 629988f1a704d62648d98649056931b8c33b9e08
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/14/2020
ms.locfileid: "3811178"
---
# <a name="map-module"></a>Kortmodul

[!include [banner](includes/banner.md)]


Dette emne omhandler kortmoduler og beskriver, hvordan du kan konfigurere dem i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overblik

Et kortmodul viser butikkernes placering på et interaktivt kort, der gengives ved hjælp af [Webkontrolelementet Bing Kort V8](https://docs.microsoft.com/bingmaps/v8-web-control/). Der kræves en Bing Kort-API-nøgle, og den skal føjes til siden med delte parametre for Commerce-hovedkontoret. Kortmoduler indeholder forskellige visninger, f.eks. veje, fra luften og gadeniveau, som brugerne kan vælge for at se kortplaceringer. De giver også mulighed for interaktioner som f.eks. zoom og udnyttelse af brugerens placering.

Et kortmodul fungerer sammen med modulet for butiksvælger for at bestemme de geografiske placeringer af butikker, der skal gengives på et kort. Butiksvælger og kortmoduler fungerer interaktivt, når en bruger vælger en butik i et af disse moduler på en webside. Kortmoduler kan udvides til andre scenarier udover interaktion med butiksvælgermoduler. Modultilpasning er dog påkrævet.

Kortmodulet blev introduceret i Commerce version 10.0.13.

Det følgende billede viser et eksempel på et kortmodul, der bruges på en side med butiksadresser.

![Eksempel på et butiksvælgermodul](./media/ecommerce-Storelocator.PNG)

## <a name="module-properties"></a>Modulegenskaber

| Egenskabsbetegnelse             | Værdi                 | Beskrivende tekst |
|---------------------------|-----------------------|-------------|
| Overskrift | Tekst | Overskrift for modulet. |
| Indstillinger for opslagsnål: standardikon | Billede | Det symbolbillede for opslagsnål, der bruges til butikker, som vises på et kort. |
| Indstillinger for opslagsnål: aktivt ikon | Billede | Det symbolbillede for opslagsnål, der bruges til en butik, der er valgt på et kort. |
| Indstillinger for opslagsnål: standardikonfarve | Tegnstreng | Teksten eller den hexadecimale værdi for farven på symboler for opslagsnål på et kort. |
| Indstillinger for opslagsnål: farve på aktivt ikon | Tegnstreng | Teksten eller den hexadecimale værdi for farven på symboler for den valgte opslagsnål på et kort. |
| Vis indeks | **Sand** eller **Falsk** | Hvis denne egenskab er indstillet til **Sand**, viser alle symboler på opslagsnål, der indikerer en butik, et indeks. Dette indeks vil svare til indekset i listevisningen, som butiksvælgermodulet viser. |

## <a name="add-allowed-mapping-urls-to-a-sites-content-security-policy-directives"></a>Føje tilladte URL-adresser til et websteds direktiver for sikkerhedspolitik

For at kortmodulet kan fungere interaktivt med Bing Kort, skal du sikre dig, at følgende tilknytnings-URL-adresser er tilladt (også kaldet "hvidlistede") pr. dit websteds sikkerhedspolitik for indhold (CSP). Denne opsætning udføres i Commerce-webstedsgeneratoren ved at tilføje tilladte URL-adresser i forskellige CSP-direktiver (f.eks. **img-src**). Du kan finde flere oplysninger under [Sikkerhedspolitik for indhold](manage-csp.md). 

- Til **connect-src**-direktivet skal du tilføje **&#42;.bing.com**.
- Til **img-src**-direktivet skal du tilføje **&#42;.virtualearth.net**.
- Til direktivet **script-src** skal du tilføje **&#42;.bing.com, &#42;.virtualearth.net**.
- Til direktivet **script style-src** skal du tilføje **&#42;.bing.com**.

## <a name="add-a-map-module-to-a-page"></a>Føje et kortmodul til en side

Du kan finde detaljerede oplysninger om, hvordan du konfigurerer et kortmodul på en side, under [Butiksvælgermodul](store-selector.md). 
 
## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over startsæt](starter-kit-overview.md)

[Boksmodul til køb](add-buy-box.md)

[Indkøbskurvsmodul](add-cart-module.md)

[Butiksvælgermodul](store-selector.md)

[Administrere Bing Kort for din organisation](./dev-itpro/manage-bing-maps.md)

[Webkontrolelementet Bing Kort V8](https://docs.microsoft.com/bingmaps/v8-web-control/)
