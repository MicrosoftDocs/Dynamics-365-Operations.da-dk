---
title: Sidehovedmodul
description: Dette emne omhandler sidehovedmoduler og beskriver, hvordan du kan oprette dem i Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: cc98419077f6f563ea2265d4e68ba809971cfbd6
ms.sourcegitcommit: ff93b8f6a11993f2cd00be2da7aa77ef0d950ab8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/03/2019
ms.locfileid: "2885472"
---
# <a name="header-module"></a>Overskriftsmodul

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dette emne omhandler sidehovedmoduler og beskriver, hvordan du kan oprette dem i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Et sidehovedmodul er en særlig container, der bruges som vært for alle de moduler, der vises i et sidehoved. Det kan f.eks. indeholde dit websteds logo, links til navigationshierarkiet, links til andre sider på webstedet og søgepanelet.

Et sidehovedmodul optimeres automatisk for den enhed, som webstedet vises på (dvs. en stationær enhed eller en mobilenhed). På en mobilenhed er navigationslinjen f.eks. skjult på **Menu**-knappen (som undertiden kaldes en *hamburgermenu*).

## <a name="properties-of-a-header"></a>Egenskaber for et sidehoved

Ligesom generiske containere understøtter et sidehovedmodulet egenskaberne **overskrift** og **bredde**.

Et sidehovedmodul har flere pladser. Der er f.eks. pladser til en oplysningsmeddelelse, navigationsmenu, logo, søgepanel, indkøbsvognsikon, ønskelisteikon og kontooplysninger. Hver plads understøtter et bestemt sæt moduler.

## <a name="modules-that-are-available-in-a-header-module"></a>Moduler, der er tilgængelige i et sidehovedmodul

Følgende moduler kan bruges i et sidehovedmodul:

- **Navigationsmenu** – Navigationsmenuen repræsenterer hierarkiet for kanalnavigation og andre statiske navigationslinks. Kanalnavigationshierarkiet kan konfigureres i Dynamics 365 Retail. Konfigurerede elementer vises derefter som sidehovednavigation. Desuden kan statiske navigationslinks konfigureres, og der kan angives relative links til andre sider på e-handelsstedet. Selve sidehovedet kan justeres til venstre, højre eller i midten.
- **Indkøbsvogn** – Indkøbsvogn-ikonet er et særligt ikon, der repræsenterer indkøbsvognen. Det vises i sidehovedet og angiver antallet af varer i indkøbsvognen. Et link til siden med indkøbsvognen skal ledsage indkøbsvognikonet, så kunderne kan blive omdirigeret til indkøbsvognen, når de bruger ikonet.
- **Ønskelisteikon** – Ønskelisteikonet vises i sidehovedet og angiver det antal varer, der er føjet til kundens ønskeliste. Et link til siden med ønskelisten skal ledsage dette ikon, så kunderne kan blive omdirigeret til ønskelistesiden, når de bruger ikonet.
- **Logonmodul** – Logonmodulet vises i sidehovedet. Her kan kunderne enten logge på deres konto eller tilmelde sig en konto. Hvis kunden allerede er logget på, kan modulet konfigureres til at vise links til kontosiden, ordrehistoriksiden eller en anden side.
- **Logomodul** – Dette modul viser det logo, der repræsenterer detailhandleren og varemærket. Det er et billede, der har et link. Linket konfigureres typisk, så det har en omdirigering til startsiden, og derfor kan kunderne hurtigt vende tilbage til startsiden fra en hvilken som helst side på webstedet.
- **Påmindelse** – Der vises en påmindelse i sidehovedet, og den bruges til at vise en indbygget meddelelse, der gælder for alle sider på webstedet. En påmindelse kan være en meddelelse som f.eks. "Det årlige udsalgs slutter om to dage".
- **Søgepanel** – Søgepanelet giver brugerne mulighed for at angive søgeord, så de kan søge efter produkter. Modulet skal konfigureres med URL-adressen til siden med søgeresultater. Parameteren for forespørgselsstrengen kan konfigureres (standardværdien er **"q"**). Søgepanelet har en plads til automatiske forslag, hvor modulet med automatiske forslag skal tilføjes.
- **Automatiske forslag** – Modulet til automatiske forslag viser automatisk resultatforslag. Disse resultater kan være nøgleord, produkter eller kategorier, hvor søgeordet indgår i.

## <a name="create-a-header-module"></a>Oprette et sidehovedmodul

Følg disse trin for at oprette et sidehovedmodul.

1. Opret et sidefragment, der indeholder et sidehovedmodul.
1. Tilføj moduler på pladserne i sidehovedmodulet.
1. Opdater indstillingerne for de enkelte moduler.
1. Gem sidefragmentet. 
1. Tjek siden ind, og publicer den.

Du kan medvirke til at sikre, at der vises et sidehoved på hver side, ved at følge disse trin i hver sideskabelon, der oprettes for webstedet.

1. På standardsiden skal du føje det sidefragment, der indeholder sidehovedmodulet, til sidehovedet på hovedpladsen.
1. Gem skabelonen. 
1. Tjek skabelonen ind, og publicer den.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over startsæt](starter-kit-overview.md)

[Modulet Container](add-container-module.md)

[Købefeltmodul](add-buy-box.md)

[Indkøbsvognmodul](add-cart-module.md)

[Betalingsmodul](add-checkout-module.md)

[Ordrebekræftelsesmodul](order-confirmation-module.md)

[Sidehovedmodul](author-header-module.md)

[Sidefodsmodul](author-footer-module.md)
