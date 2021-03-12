---
title: Kontostyringssider og -moduler
description: Dette emne omfatter sider og moduler til kontostyring i Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6c465b8883438eee886b177274bf89ddb86aa00b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980550"
---
# <a name="account-management-pages-and-modules"></a>Kontostyringssider og -moduler

[!include [banner](includes/banner.md)]

Dette emne omfatter sider og moduler til kontostyring i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Kontostyring henviser til en gruppe sider, der bruges til at administrere brugerkontorelaterede oplysninger i Dynamics 365 Commerce. Kontostyringssider omfatter landingssiden til kontostyring, brugerprofilside, brugeradresseside, ordrehistorikside, ordreoplysningside, fordelskundeside og ønskelisteside.

### <a name="account-management-landing-page"></a>Landingsside for kontostyring

Landingssiden til kontostyring bruger følgende moduler:

- **Container** - Alle sidemoduler for kontoadministration skal placeres i en container. 
- **Velkomsttitel for konto** – Dette modul bruges til at angive en velkomstmeddelelse på kontostyringssiden. Den indeholder egenskaber for overskriften.
- **Generisk kontotitel** – Dette modul kan bruges til at angive overskrifter og links til kontostyringssider, f.eks. siderne "Ordreoversigt" eller "Min profil". Det generiske flisemodul kan bruges til at konfigurere en flise for en side. I Fabrikam bruges dette modul til sidelinkene "Ordreoversigt" og "Min profil" på siden til start af kontostyring.
- **Ønskelisteflise for konto** – Dette modul bruges til at angive en oversigt over varerne på kundens ønskeliste. Det kan f. eks. angive, at "Du har 10 varer på din ønskeliste". Det indeholder egenskaber for overskriften og linket "Vis detaljer". Linket "Vis detaljer" skal konfigureres, så der omdirigeres til ønskelistesiden. 
- **Adresseflise for konto** – Dette modul bruges til at angive en oversigt over brugerens adresser. Det kan f. eks. angive, at "Du har føjet 2 adresser til din konto". Det indeholder egenskaber for overskriften og linket "Vis detaljer". Linket "Vis detaljer" skal konfigureres, så der omdirigeres til brugeradressesiden.
- **Fordelskundeflise for konto** – Dette modul bruges til at få vist og indsætte et link til oplysninger om fordelskundeprogrammet. Dette felt indeholder to tilstande: en tilstand viser link til at deltage i et fordelskundeprogam, hvis brugeren ikke allerede er medlem. I den anden tilstand vises links til visning af siden Fordelskundeoplysninger, når brugeren allerede er medlem. Egenskaber omfatter overskriften, linket "Tilmeld" og linket "Vis fordelskunde". Linket "Vis fordelskunde" skal konfigureres, så der omdirigeres til fordelskundesiden. Linket "Tilmeld" skal konfigureres, så det omdirigeres til en side, hvor brugerne kan komme med i fordelskundeprogrammet. 

### <a name="order-history-page"></a>Ordrehistorikside

På ordrehistoriksiden bruges modulet for ordrehistorik til at vise alle de seneste ordrer, som brugeren har afgivet.

### <a name="order-details-page"></a>Ordredetaljeside

På ordredetaljesiden vises der detaljerede oplysninger om hver enkelt ordre, og du kan få adgang til den fra ordrehistoriksiden. Den bruger ordredetaljemodulet, som kræver salgs-id'et eller transaktions-id'et for at kunne hente ordreoplysningerne.

### <a name="user-profile-page"></a>Brugerprofilside

På brugerprofilsiden forevises detaljer om brugerkonti, f.eks. en brugers navn og mailadresse. Den bruger brugerprofilen og redigeringsmodulerne til brugerprofiler. Mailadressen kan ikke fjernes, men den kan redigeres. Brugerprofilsiden viser også brugerpræferencer, der giver en bruger mulighed for at tilmelde sig eller fravælge visse funktioner som f.eks. personalisering af anbefalingslister. 

### <a name="user-address-page"></a>Brugeradresseside

På siden brugeradresse vises listen over de adresser, der er knyttet til brugerkontoen. Brugeren har enten angivet disse adresser under betalingen eller tilføjet dem direkte på denne side. Brugeradressemodulet bruges til at tilføje og redigere adresser, angive den primære adresse og gengive eksisterende adresser på siden.

### <a name="wish-list-page"></a>Ønskelisteside

På ønskelistesiden vises de varer, som er føjet til kundens ønskeliste. Den bruger ønskelistemodulet ønske til at gengive ønskelisteelementer.

### <a name="loyalty-page"></a>Side for fordelskunde

På fordelskundesiden kan kunderne få vist deres fordelskundedetaljer, hvis de allerede er medlem af fordelskundeprogrammet. De kan også få vist de point, de har optjent og indløst i seneste transaktioner. På denne side bruges modulet fordelskundeoplysninger til at vise fordelskundeoplysningerne. 

Hvis du vil deltage i fordelskundesprogrammet, kan der oprettes en marketingside med modulerne til fordelskundetilmelding og fordelskundebetingelserne. Hvis brugeren ikke er medlem af et fordelskundeprogram, vil disse moduler give brugeren mulighed for at tilmelde sig.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over modulbibliotek](starter-kit-overview.md)

[Container-modul](add-container-module.md)

[Boksmodul til køb](add-buy-box.md)

[Indkøbskurvsmodul](add-cart-module.md)

[Betalingsmodul](add-checkout-module.md)

[Ordrebekræftelsesmodul](order-confirmation-module.md)

[Sidehovedmodul](author-header-module.md)

[Sidefodsmodul](author-footer-module.md)
