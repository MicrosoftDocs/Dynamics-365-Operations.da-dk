---
title: Sidehovedmodul
description: Dette emne omhandler sidehovedmoduler og beskriver, hvordan du kan oprette sidehoveder i Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: a5f7ad7d9c5ff63c3c3a8fe38275eec0d138891d
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411194"
---
# <a name="header-module"></a>Overskriftsmodul

[!include [banner](includes/banner.md)]

Dette emne omhandler sidehovedmoduler og beskriver, hvordan du kan oprette sidehoveder i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

I Dynamics 365 Commerce indeholder et sidehoved flere moduler, f.eks. sidehoved, navigationsmenu, søg, kampagnebanner og moduler til cookie-samtykke. 

Sidehovedmodulet indeholder et websteds logo, links til navigationshierarkiet, links til andre sider på webstedet, et indkøbskurvsymbol, et hvidlistesymbol, logonindstillinger og søgelinjen. Et sidehovedmodul optimeres automatisk for den enhed, som webstedet vises på (med andre ord en stationær enhed eller en mobilenhed). På en mobilenhed er navigationslinjen f.eks. skjult på **Menu**-knappen (som undertiden kaldes en *hamburgermenu*).

Det følgende billede viser et eksempel på et sidehovedmodul på en startside.

![Eksempel på et sidehovedmodul](./media/ecommerce-header.png)

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

1. Gå til **Sidefragmenter**, og vælg **Nyt** for at oprette et nyt fragment.
1. I dialogboksen **Nyt sidefragment** skal du vælge modulet **Container**, angive et navn for sidefragmentet og derefter vælge **OK**.
1. Vælg pladsen **Standardcontainer**, og angiv derefter egenskaben **Bredde** til **Udfyld container**, i egenskabsruden til højre.
1. På pladsen **Standardcontainer** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulerne **Kampagnebanner** og **Cookie-samtykke**. Vælg derefter **OK**.
1. På pladsen **Standardcontainer** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Container** og derefter **OK**.
1. Vælg pladsen **Container**, og angiv derefter egenskaben **Bredde** til **Udfyld container**, i egenskabsruden til højre.
1. På pladsen **Container** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Sidehoved** og derefter **OK**.
1. På pladsen **Navigationsmenu** i sidehovedmodulet skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Navigationsmenu** og derefter **OK**.
1. Konfigurer egenskaberne som påkrævet i egenskabsruden for navigationsmenumodulet.
1. På pladsen **Søg** i sidehovedmodulet skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Søg** og derefter **OK**.
1. Konfigurer egenskaberne som påkrævet i egenskabsruden for søgemodulet.
1. På pladsen **Indkøbskurvikon** i sidehovedmodulet skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Indkøbskurvikon** og derefter **OK**.
1. Konfigurer egenskaberne som påkrævet i egenskabsruden for indkøbskurvikonmodulet. Hvis du ønsker, at indkøbsvognen skal vise en indkøbsvognoversigt (også kaldet en minivogn), når brugerne bevæger dig hen over den, skal du vælge **Vis minivogn**.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke fragmentet ind, og vælg derefter **Publicer** for at publicere det.

Du kan medvirke til at sikre, at der vises et sidehoved på hver side, ved at følge disse trin i hver sideskabelon, der oprettes for webstedet.

1. På pladsen **Sidehoved** i modulet **Standardside** skal du tilføje det sidefodsfragment, som du har oprettet.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.

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
