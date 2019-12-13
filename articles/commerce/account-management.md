---
title: Kontostyringssider og -moduler
description: Dette emne omfatter sider og moduler til kontostyring i Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
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
ms.openlocfilehash: 3986505a7e0e8d33d5b8ff2c06f493335731a8d9
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785370"
---
# <a name="account-management-pages-and-modules"></a>Kontostyringssider og -moduler

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dette emne omfatter sider og moduler til kontostyring i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Kontostyring henviser til en gruppe sider, der bruges til at administrere brugerkontorelaterede oplysninger i Dynamics 365 Commerce. Kontostyringssider omfatter landingssiden til kontostyring, brugerprofilside, brugeradresseside, ordrehistorikside, ordreoplysningside, fordelskundeside og ønskelisteside.

### <a name="account-management-landing-page"></a>Landingsside for kontostyring

Landingssiden til kontostyring bruger følgende moduler:

- **Indholdsplacering** – dette modul er et containermodul, der indeholder alle modulerne på landingssiden til kontostyring.
- **Velkomstelement for konto** – dette modul bruges til at angive en velkomstmeddelelse på kontostyringssiden. Det indeholder egenskaber for overskriften og feltstørrelsen. Egenskaben **Feltstørrelse** definerer bredden af modulet i indholdsplaceringsmodulet. Værdierne går fra **1** til **12**, hvor **12** repræsenterer den fulde bredde på containeren til indholdsplacering.
- **Ordreafgivelseselement for konto** – dette modul bruges til at angive en oversigt over antallet af ordrer, der er afgivet af brugerkontoen. Det indeholder egenskaber for overskriften, feltstørrelsen og linket "vis detaljer". Linket "vis detaljer" skal konfigureres, så der omdirigeres til ordrehistoriksiden.
- **Profilplaceringselement for konto** – dette modul bruges til at angive en oversigt over brugerprofilen. Det indeholder egenskaber for overskriften, feltstørrelsen og linket "vis detaljer". Linket "vis detaljer" skal konfigureres, så der omdirigeres til brugerprofilsiden.
- **Ønskelisteelement for konto** – dette modul bruges til at angive en oversigt over varerne på kundens ønskeliste. Det kan f. eks. angive, at "Du har 10 varer på din ønskeliste". Det indeholder egenskaber for overskriften, feltstørrelsen og linket "vis detaljer". Linket "vis detaljer" skal konfigureres, så der omdirigeres til ønskelistesiden.
- **Adresseelement for konto** – dette modul bruges til at angive en oversigt over brugerens adresser. Det kan f. eks. angive, at "Du har føjet 2 adresser til din konto". Det indeholder egenskaber for overskriften, feltstørrelsen og linket "vis detaljer". Linket "vis detaljer" skal konfigureres, så der omdirigeres til brugeradressesiden.
- **Fordelskundeelement for konto** – dette modul bruges til at få vist og indsætte et link til oplysninger om fordelskundeprogrammet. Det indeholder egenskaber for overskriften, feltstørrelsen, linket "vis detaljer" samt linket "bliv medlem". Linket "vis detaljer" skal konfigureres, så der omdirigeres til fordelskundesiden. Linket "bliv medlem" skal konfigureres, så det omdirigeres til en side, hvor brugerne kan komme med i fordelskundeprogrammet.

### <a name="order-history-page"></a>Ordrehistorikside

På ordrehistoriksiden bruges modulet for ordrehistorik til at vise alle de seneste ordrer, som brugeren har afgivet.

### <a name="order-details-page"></a>Ordredetaljeside

På ordredetaljesiden vises der detaljerede oplysninger om hver enkelt ordre, og du kan få adgang til den fra ordrehistoriksiden. Den bruger ordredetaljemodulet, som kræver salgs-id'et eller transaktions-id'et for at kunne hente ordreoplysningerne.

### <a name="user-profile-page"></a>Brugerprofilside

På brugerprofilsiden vises der detaljer om brugerkonti, f. eks. brugerens navn og mailadresse. Den bruger brugerprofilmodulet. Mailadressen kan ikke fjernes, men den kan redigeres.

### <a name="user-address-page"></a>Brugeradresseside

På siden brugeradresse vises listen over de adresser, der er knyttet til brugerkontoen. Brugeren har enten angivet disse adresser under betalingen eller tilføjet dem direkte på denne side. Brugeradressemodulet bruges til at tilføje og redigere adresser, angive den primære adresse og gengive eksisterende adresser på siden.

### <a name="wish-list-page"></a>Ønskelisteside

På ønskelistesiden vises de varer, som er føjet til kundens ønskeliste. Den bruger ønskelistemodulet ønske til at gengive ønskelisteelementer.

### <a name="loyalty-page"></a>Side for fordelskunde

På fordelskundesiden kan kunderne blive medlem af et fordelskundeprogram eller, hvis de allerede er medlem af fordelskundeprogrammet, få vist oplysninger om deres program. De kan også få vist de point, de har optjent og indløst i seneste transaktioner.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over startsæt](starter-kit-overview.md)

[Modulet Container](add-container-module.md)

[Købefeltmodul](add-buy-box.md)

[Indkøbsvognmodul](add-cart-module.md)

[Betalingsmodul](add-checkout-module.md)

[Ordrebekræftelsesmodul](order-confirmation-module.md)

[Sidehovedmodul](author-header-module.md)

[Sidefodsmodul](author-footer-module.md)
