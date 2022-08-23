---
title: Overskriftsmodul
description: Denne artikel omhandler sidehovedmoduler og beskriver, hvordan du kan oprette sidehoveder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 63c298f36f64f2e107d3df3c0c5f3b6445546aa1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275779"
---
# <a name="header-module"></a>Overskriftsmodul

[!include [banner](includes/banner.md)]

Denne artikel omhandler sidehovedmoduler og beskriver, hvordan du kan oprette sidehoveder i Microsoft Dynamics 365 Commerce.

I Dynamics 365 Commerce konfigureres et sidehoved som et sidefragment, der omfatter modulerne til sidehoved, kampagnebanner og cookie-samtykke. 

Sidehovedmodulet indeholder et websteds logo, links til navigationshierarkiet, links til andre sider på webstedet, et modul til indkøbskurveikon, et hvidlistesymbol, logonindstillinger og søgelinjen. Et sidehovedmodul optimeres automatisk for den enhed, som webstedet vises på (med andre ord en stationær enhed eller en mobilenhed). På en mobilenhed er navigationslinjen f.eks. skjult på **Menu**-knappen (som undertiden kaldes en *hamburgermenu*).

Det følgende billede viser et eksempel på et sidehovedmodul på en startside.

![Eksempel på et sidehovedmodul.](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a>Egenskaber for et sidehovedmodul

Et sidehovedmodul understøtter egenskaberne **Logo-billede**, **Logo** og **Min konto-link**. 

Egenskaberne **Logo-billede** og **Logo-link** bruges til at definere et logo på siden. Du kan finde flere oplysninger under [Tilføj et logo](add-logo.md). 

Egenskaben **Min konto-link** kan bruges til at definere kontosider, som ejeren af webstedet ønsker at vise hurtige links for i sidehovedet.

## <a name="modules-that-are-available-within-a-header-module"></a>Moduler, der er tilgængelige i et sidehovedmodul

Følgende moduler kan bruges i et sidehovedmodul:

- **Navigationsmenu** – Navigationsmenuen repræsenterer hierarkiet for kanalnavigation og andre statiske navigationslinks. Du kan finde flere oplysninger i [Navigationsmenumodul](nav-menu-module.md).

- **Søg** – Søgemodulet giver brugerne mulighed for at angive søgeord, så de kan søge efter produkter. URL-adressen til standardsøgesiden og parametrene for søgeforespørgslen skal angives på **Indstillinger for webside \> Udvidelser**. Søgemodulet har egenskaber, du kan bruge til at undertrykke søgeknappen eller -etiketten efter behov. Søgemodulet understøtter også indstillinger for automatisk at foreslå, f.eks. produkt-, nøgleords- og kategorisøgeresultater.

- **Indkøbsvognikon** – Indkøbsvognikonmodulet repræsenterer indkøbsvognikonet, som viser antallet af varer i en indkøbsvogn på et givet tidspunkt. Du kan få flere oplysninger i [Modulet for indkøbsvognikon](cart-icon-module.md).

- **Webstedsvælger**- Med webstedsvælgermodulet kan brugere gennemse forskellige foruddefinerede websteder baseret på marked, områder og landestandarder. Du kan få flere oplysninger under [Webstedsvælgermodul](site-selector.md).

- **Butiksvælger** - Butiksvælgermodulet kan medtages på et overskriftmoduls butiksvælgerplads. Det giver brugere mulighed for at søge efter og finde butikker i nærheden. Brugerne kan også angive en foretrukken butik. Butikken vil derefter blive vist i overskriften. Når butiksvælgermodulet er inkluderet i overskriftsmodulet, skal egenskaben **Tilstand** være angivet til **Find butikker**. Du kan få flere oplysninger under [Butiksvælgermodul](store-selector.md).

> [!NOTE]
> - Understøttelse af indkøbsvognikonets modul i overskriftsmoduler er tilgængelig pr. Dynamics 365 Commerce version 10.0.11.
> - Understøttelse af brug af webstedets vælgermodul i overskriftsmoduler er tilgængelig pr. Dynamics 365 Commerce version 10.0.14.
> - Understøttelse af brug af butikkens vælgermodul i overskriftsmoduler er tilgængelig pr. Dynamics 365 Commerce version 10.0.15.

## <a name="header-module-in-the-adventure-works-theme"></a>Overskriftsmodul i emnet Adventure Works

I emnet Adventure Works understøtter overskriftsmodulet egenskaben **Mobillogo**. Denne egenskab gør det muligt at angive et logo for mobile viewports. Egenskaben **Mobillogo** er tilgængelig som en moduldefinitionsudvidelse.

> [!IMPORTANT]
> Emnet Adventure Works er tilgængelige pr. Dynamics 365 Commerce version 10.0.20.

## <a name="create-a-header-fragment-for-a-page"></a>Oprette et sidehovedfragment for en side

Følg disse trin for at oprette et sidehovedfragment.

1. Gå til **Fragmenter**, og vælg **Nyt** for at oprette et nyt fragment.
1. I dialogboksen **Vælg et fragment** skal du vælge modulet **Container**, angive et navn for fragmentet og derefter vælge **OK**.
1. Vælg pladsen **Standardcontainer**, og angiv derefter egenskaben **Bredde** til **Udfyld skærm** i egenskabsruden til højre.
1. På pladsen **Standardcontainer** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Vælg moduler** skal du vælge modulerne **Cookie-samtykke**, **Sidehoved** og **Kampagnebanner**. Vælg derefter **OK**.
1. Vælg **Tilføj meddelelse** i ruden Egenskaber i modulet **Kampagnebanner**, og vælg derefter **Meddelelse**.
1. Tilføj tekst og links i kampagneindholdet i dialogboksen **Meddelelse**, og vælg derefter **OK**.
1. Tilføj og Konfigurer tekst og et link til websiden om beskyttelse af personlige oplysninger i ruden Egenskaber i modulet **Cookie-samtykke**.
1. På pladsen **Navigationsmenu** i sidehovedmodulet skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Vælg moduler** skal du vælge modulet **Navigationsmenu** og derefter **OK**.
1. Vælg **Detailserver** under **Kilde til navigationsmenu** i egenskabsruden for modulet navigationsmenu.
1. Vælg **Tilføj menupunkt** i egenskabsruden for modulet navigationsmenu under **Statiske menupunkter**, og vælg derefter **Menupunkt**. 
1. Angiv "Kontakt" i dialogboksen **Menupunkt** under **Menupunkttekst**.
1. Vælg **Tilføj et link** under **Linkdestination for menupunkt** i dialogboksen **Menupunkt**.
1. Vælg URL-adressen til websiden "Kontakt" i dialogboksen **Tilføj et link**, og vælg derefter **OK**.  
1. Vælg **OK** i dialogboksen **Menupunkt**.
1. På pladsen **Søg** i sidehovedmodulet skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Vælg moduler** skal du vælge modulet **Søg** og derefter **OK**.
1. Konfigurer egenskaberne som påkrævet i egenskabsruden for søgemodulet.
1. På pladsen **Kurv-ikon** i sidehovedmodulet skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Vælg moduler** skal du vælge modulet **Kurv-ikon** og derefter **OK**.
1. Konfigurer egenskaberne som påkrævet i egenskabsruden for indkøbskurvikonmodulet. Hvis du ønsker, at indkøbsvognen skal vise en indkøbsvognoversigt (også kaldet en minivogn), når brugerne bevæger dig hen over den, skal du vælge **Vis minivogn**.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke fragmentet ind, og vælg derefter **Publicer** for at publicere det.

Du kan medvirke til at sikre, at der vises et sidehoved på hver side, ved at følge disse trin i hver sideskabelon, der oprettes for webstedet.

1. På pladsen **Sidehoved** i modulet **Standardside** skal du tilføje det sidefodsfragment, som du har oprettet.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over modulbibliotek](starter-kit-overview.md)

[Container-modul](add-container-module.md)

[Ikonmodul for indkøbskurv](cart-icon-module.md)

[Kampagnebannermodul](add-alert.md)

[Navigationsmenumodul](nav-menu-module.md) 

[Samtykke til cookie](cookie-consent-module.md)

[Sidefodsmodul](author-footer-module.md)

[Webstedsvælgermodul](site-selector.md)

[Butiksvælgermodul](store-selector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
