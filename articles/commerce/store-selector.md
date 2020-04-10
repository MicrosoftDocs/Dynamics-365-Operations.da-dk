---
title: Modulet Butiksvælger
description: Dette emne omhandler modulet Butiksvælger og beskriver, hvordan du kan føje det til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 03/19/2020
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
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8efc2345ded52bfaee2d400815795906f326f4fd
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/21/2020
ms.locfileid: "3157334"
---
# <a name="store-selector-module"></a>Modulet Butiksvælger

[!include [banner](includes/banner.md)]

Dette emne omhandler modulet Butiksvælger og beskriver, hvordan du kan føje det til sider på websteder i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overblik

Et butiksvælgermodul bruges til kundescenariet "Køb online, afhent i butikken" (BOPIS). I modulet vises en liste over butikker, hvor et produkt kan afhentes, samt åbningstider og produktbeholdning for hver butik.

Butiksvælgermodulet kræver en produktkontekst og en søgeplacering, når du vil finde butikker. Hvis der ikke findes en søgeplacering, bruges som standard kundens browserplacering, hvis kunden giver samtykke. Modulet har et inputfelt, som giver kunden mulighed for at angive et sted (postnummer eller by og stat) for at finde butikker i nærheden.

Modulet Butiksvælger er integreret med Bing Maps Geocoding-API'en (Application Programming Interface) til at konvertere det sted, som kunden indtastede, til en bredde- og en længdegrad. Der kræves en Bing Kort-API-nøgle, og den skal føjes til siden med delte parametre for Commerce i Dynamics 365 Commerce.

Butiksvælgermodulet kan føjes til et købefeltmodul på siden med produktdetaljer (PDP), hvis du vil have vist butikker, hvor et produkt kan afhentes. Modulet kan også føjes til et indkøbsvognmodul. Når butiksvælgermodulet føjes til et indkøbsvognmodul, vises afhentningsindstillinger for de enkelte linjevarer i indkøbsvognen. Desuden kan dette modul ved hjælp af brugerdefineret kodning føjes til andre sider eller moduler via udvidelser og tilpasninger.

Hvis BOPIS-scenariet skal fungere, skal produkterne konfigureres med leveringstilstanden "kundeafhentning". Ellers bliver modulet ikke vist på de respektive sider. Du kan finde flere oplysninger om, hvordan du kan konfigurere leveringsmåden, i [Konfigurere leveringsmåder](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Følgende billede viser et eksempel på et butiksvælgermodul, der bruges på en produktoplysningsside (PDP).

![Eksempel på et butiksvælgermodul](./media/BOPIS.PNG)

## <a name="store-selector-module-usage-in-e-commerce"></a>Brug af butiksvælgermodul i e-handel

- Et butiksvælgermodul kan bruges på en side med produktdetaljer (PDP) til at finde butikker i nærheden, hvor et produkt kan afhentes.
- Et butiksvælgermodul kan bruges på en indkøbsvognside til at finde butikker i nærheden, hvor et produkt i indkøbsvognen kan afhentes.

## <a name="store-selector-module-properties"></a>Egenskaber for modulet Butiksvælger

| Egenskabsbetegnelse             | Værdi                 | Beskrivende tekst |
|---------------------------|-----------------------|-------------|
| Søgeradius | Tal | Definerer søgeradius for butikker, i miles. Hvis der ikke er angivet en værdi, bruges standardradiussen på 50 miles.|
|Vilkår for brug | URL-adresse    |  URL-adressen til servicebetingelserne skal angives for Bing Kort-tjenesten. |

## <a name="add-a-store-selector-module-to-a-page"></a>Føje et butiksvælgermodul til en side

Et butiksvælgermodul skal bruge en produktkontekst, så det kan kun bruges i forbindelse med købefelt- og indkøbsvognmoduler. Butiksvælgermoduler fungerer ikke uden for disse moduler.

- Yderligere oplysninger om, hvordan du føjer et butiksvælgermodul til et købefeltmodul, finder du under [Købefeltmodul](add-buy-box.md). 
- Oplysninger om, hvordan du føjer et butiksvælgermodul til et indkøbsvognmodul, finder du under [Indkøbsvognmodul](add-cart-module.md)

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over startsæt](starter-kit-overview.md)

[Boksmodul til køb](add-buy-box.md)

[Indkøbskurvsmodul](add-cart-module.md)

[Hurtig rundvisning i PDP](quick-tour-pdp.md)

[Hurtig rundvisning i Indkøbsvogn og betaling](quick-tour-cart-checkout.md)

[Konfigurer leveringsmåder](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)
