---
title: Sidehovedmodul
description: Dette emne omhandler sidehovedmoduler og beskriver, hvordan du kan oprette sidehoveder i Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 04/13/2020
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
ms.openlocfilehash: cec138ebefbd2beb2f1cf6302ce58d8bbc5c4bbd
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261438"
---
# <a name="header-module"></a>Overskriftsmodul


[!include [banner](includes/banner.md)]

Dette emne omhandler sidehovedmoduler og beskriver, hvordan du kan oprette sidehoveder i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

I Dynamics 365 Commerce indeholder et sidehoved flere moduler, f.eks. sidehoved, navigationsmenu, søg, kampagnebanner og moduler til cookie-samtykke. 

Sidehovedmodulet indeholder et websteds logo, links til navigationshierarkiet, links til andre sider på webstedet, et indkøbskurvsymbol, et hvidlistesymbol, logonindstillinger og søgelinjen. Et sidehovedmodul optimeres automatisk for den enhed, som webstedet vises på (med andre ord en stationær enhed eller en mobilenhed). På en mobilenhed er navigationslinjen f.eks. skjult på **Menu**-knappen (som undertiden kaldes en *hamburgermenu*).

## <a name="properties-of-a-header-module"></a>Egenskaber for et sidehovedmodul

Et sidehovedmodul understøtter egenskaberne **Logo-billede**, **Logo** og **Min konto-link**. 

Egenskaberne **Logo-billede** og **Logo-link** bruges til at definere et logo på siden. Du kan finde flere oplysninger under [Tilføj et logo](add-logo.md). 

Egenskaben **Min konto-link** kan bruges til at definere kontosider, som ejeren af webstedet ønsker at vise hurtige links for i sidehovedet.

## <a name="modules-that-are-available-in-a-header-module"></a>Moduler, der er tilgængelige i et sidehovedmodul

Følgende moduler kan bruges i et sidehovedmodul:

- **Navigationsmenu** – Navigationsmenuen repræsenterer hierarkiet for kanalnavigation og andre statiske navigationslinks. Kanalnavigationshierarkiet kan konfigureres i Dynamics 365 Commerce. Navigationsmenuen indeholder egenskaben **Navigationskilde**, der bruges til at angive navigationsmenupunkter i Detailservere og statiske menupunkter som en kilde. Hvis statiske menupunkter angives som kilde, kan der angives relative links til andre sider på webstedet. Konfigurerede elementer vises derefter som sidehovednavigation. 
- **Søg** – Søgemodulet giver brugerne mulighed for at angive søgeord, så de kan søge efter produkter. URL-adressen til standardsøgesiden og parametrene for søgeforespørgslen skal angives på **Indstillinger for webside \> Udvidelser**. Søgemodulet har egenskaber, du kan bruge til at undertrykke søgeknappen eller -etiketten efter behov. Søgemodulet understøtter også indstillinger for automatisk at foreslå, f.eks. produkt-, nøgleords- og kategorisøgeresultater.
- **Indkøbsvognikon** – Indkøbsvognikonmodulet repræsenterer indkøbsvognikonet, som viser antallet af varer i en indkøbsvogn på et givet tidspunkt. Du kan få flere oplysninger i [Modulet for indkøbsvognikon](cart-icon-module.md).

## <a name="create-a-header-module-for-a-page"></a>Opret et sidehovedmodul for en side

Følg disse trin for at oprette et sidehovedmodul.

1. Opret et fragment med navnet **Sidehovedfragment**, og føj et containermodul til det.
1. Angiv egenskaben **Bredde** til **Fyld container**i egenskabsruden for containermodulet.
1. Føj et kampagnebanner og cookie-samtykkemoduler til containermodulet.
1. Føj et andet containermodul til fragmentet, og indstil egenskaben **Bredde** til **Fyld container**.
1. Føj et sidehovedmodul til det andet containermodul.
1. Tilføj et navigationsmenumodul i **Navigationsmenu**pladsen i sidehovedmodulet. 
1. Konfigurer egenskaberne for navigationsmenumodulet i egenskabsruden for navigationsmenumodulet.
1. Tilføj et søgemodul i **Søg**pladsen i sidehovedmodulet. 
1. Konfigurer egenskaberne for søgemodulet i egenskabsruden for søgemodulet. 
1. Tilføj et indkøbsvognikonmodul i pladsen **Indkøbsvognikon**. 
1. Konfigurer egenskaberne for indkøbsvognikonmodulet i egenskabsruden for ikonet for indkøbsvognikonmodulet. Hvis indkøbsvognikonet skal vise en minivogn, når der peges på den, skal du vælge **Sand** for **Vis minivogn**.
1. Gem sidefragmentet, afslut redigeringen, og udgiv det. 


Du kan medvirke til at sikre, at der vises et sidehoved på hver side, ved at følge disse trin i hver sideskabelon, der oprettes for webstedet.

1. Tilføj det sidehovedfragment, der indeholder sidehovedmodulet af sidehovedet, i **Hoved**pladsen af standardsiden.
1. Gem skabelonen, afslut redigeringen, og udgiv den.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over startsæt](starter-kit-overview.md)

[Container-modul](add-container-module.md)

[Boksmodul til køb](add-buy-box.md)

[Indkøbskurvsmodul](add-cart-module.md)

[Modulet Indkøbskurvikon](cart-icon-module.md)

[Betalingsmodul](add-checkout-module.md)

[Ordrebekræftelsesmodul](order-confirmation-module.md)

[Overskriftsmodul](author-header-module.md)

[Sidefodsmodul](author-footer-module.md)
