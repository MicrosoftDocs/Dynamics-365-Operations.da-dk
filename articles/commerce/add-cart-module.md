---
title: Indkøbsvognmodul
description: Dette emne omhandler indkøbsvognmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3ba46fd90507a9cf8da92598c8449a2e553da352
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411267"
---
# <a name="cart-module"></a>Indkøbsvognmodul

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dette emne omhandler indkøbsvognmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overblik

Et indkøbsvognmodul viser de varer, der er føjet til indkøbsvognen, før kunden fortsætter med at betale. Modulet viser også en ordreoversigt, og kunden kan anvende eller fjerne kampagnekoder.

Indkøbsvognmodulet understøtter udtjekning og udlevering via gæst. Den understøtter også et **Tilbage til indkøb**-link. Du kan konfigurere ruten for dette link på **Indstillinger for webside \> Udvidelser \> Ruter**.

I indkøbsvognmodulet gengives data baseret på indkøbsvogn-id'et, som er en browsercookie, der er tilgængelig på hele webstedet. 

Det følgende billede viser et eksempel på en side med en indkøbsvogn på Fabrikam-webstedet.

![Eksempel på et indkøbvognmodul](./media/cart2.PNG)

## <a name="cart-module-properties-and-slots"></a>Egenskaber og pladser i indkøbsvognmodulet

Indkøbsvognmodulet har en **Overskrift**-egenskab, der kan angives til værdier som f.eks. **Indkøbspose** og **Varer i indkøbsvognen**. 

## <a name="modules-that-can-be-used-in-a-cart-module"></a>Moduler, der kan bruges i et indkøbsvognmodul

- **Tekstblok** – Dette modul understøtter brugerdefinerede meddelelser i indkøbsvognmodulet. Meddelelserne styres af CMS (Content Management system). Der kan tilføjes en hvilken som helst besked f.eks. "Kontakt 1-800-Fabrikam, hvis der er problemer med din ordre".
- **Butiksvælger** – Dette modul viser en liste over butikker i nærheden, hvor en vare kan afhentes. Det giver brugerne mulighed for at angive en placering for butikker, der er i nærheden. Du kan få flere oplysninger om dette modul i [Butiksvælgermodul](store-selector.md).

## <a name="module-properties"></a>Modulegenskaber

De følgende indstillinger for indkøbsvognmodul kan konfigureres under **Indstillinger for websted \> Udvidelser**:

- **Maks. antal** – Denne egenskab bruges tl at angive det maksimale antal af hver vare, der kan føjes til indkøbsvognen. En detailhandler kan f. eks. beslutte, at der kun kan sælges 10 stk. af hvert produkt i en enkelt transaktion.
- **Lager** – Du finder oplysninger om, hvordan du anvender lagerindstillinger, under [Anvendelse af lagerindstillinger](inventory-settings.md).
- **Tilbage til indkøb** – Denne egenskab bruges til at angive ruten for linket **Tilbage til indkøb**. Ruten kan konfigureres på webstedsniveau, så detailhandlere kan føre kunden tilbage til startsiden eller en anden side på webstedet.

## <a name="commerce-scale-unit-interaction"></a>Enhedsinteraktion i Commerce Scale

Indkøbsvognmodulet henter produktoplysninger vha. Commerce Scale Unit-API'er. Indkøbs-id'et fra browsercookien bruges til at hente alle produktoplysningerne fra Commerce Scale Unit.

## <a name="add-a-cart-module-to-a-page"></a>Føje et indkøbsvognmodul til en side

Hvis du vil føje et indkøbsvognmodul til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.

1. Gå til **Sidefragmenter**, og vælg **Nyt** for at oprette et nyt fragment.
1. Vælg modulet **Indkøbsvogn** i dialogboksen **Nyt sidefragment**.
1. Under **Sidefragmentsnavn** skal du angive navnet **Indkøbsvognfragment** og derefter vælge **OK**.
1. Vælg **Indkøbsvogn**-pladsen.
1. Vælg blyantsymbolet i ruden Egenskaber til højre. Skriv overskriften i feltet, og vælg derefter markeringssymbolet.
1. På pladsen **Indkøbsvogn** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Butiksvælger** og derefter **OK**.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke fragmentet ind, og vælg derefter **Publicer** for at publicere det.
1. Gå til **Skabeloner**, og vælg **Ny** for at oprette en ny skabelon.
1. Angiv et navn for skabelonen under **Skabelonnavn** i dialogboksen **Ny skabelon**.
1. Vælg pladsen **Brødtekst** i dispositionstræet, vælg ellipsen (**...**), og vælg derefter **Tilføj modul**.
1. I dialogboksen **Vælg sidefragment** skal du vælge **Indkøbsvognfragmentet** og derefter **OK**.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.
1. Gå til **Sider**, og vælg **Ny** for at oprette en ny side.
1. I dialogboksen **Vælg en skabelon** skal du vælge den skabelon, du har oprettet, angive et sidenavn og derefter vælge **OK**.
1. Vælg **Gem**, og vælg derefter **Vis** for at få vist siden.
1. Vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over startsæt](starter-kit-overview.md)

[Container-modul](add-container-module.md)

[Butiksvælgermodul](store-selector.md)

[Boksmodul til køb](add-buy-box.md)

[Ikon for indkøbskurvsmodul](cart-icon-module.md)

[Betalingsmodul](add-checkout-module.md)

[Ordrebekræftelsesmodul](order-confirmation-module.md)

[Overskriftsmodul](author-header-module.md)

[Sidefodsmodul](author-footer-module.md)

[Beregne lagertilgængelighed for detailkanaler](calculated-inventory-retail-channels.md)
