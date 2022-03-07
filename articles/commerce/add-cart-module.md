---
title: Indkøbsvognmodul
description: Dette emne omhandler indkøbsvogn-moduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f2db61cf23c217365274297c6e9878a4eb5679f8d9502cb70484372ae43f6b18
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716878"
---
# <a name="cart-module"></a>Indkøbskurvsmodul

[!include [banner](includes/banner.md)]

Dette emne omhandler indkøbsvogn-moduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.

Et indkøbsvognmodul viser de varer, der er føjet til indkøbsvognen, før kunden fortsætter med at betale. Modulet viser også en ordreoversigt, og kunden kan anvende eller fjerne kampagnekoder.

Indkøbsvognmodulet understøtter udtjekning og udlevering via gæst. Den understøtter også et **Tilbage til indkøb**-link. Du kan konfigurere ruten for dette link på **Indstillinger for webside \> Udvidelser \> Ruter**.

I indkøbsvognmodulet gengives data baseret på indkøbsvogn-id'et, som er en browsercookie, der er tilgængelig på hele webstedet. 

Det følgende billede viser et eksempel på en side med en indkøbsvogn på Fabrikam-webstedet.

![Eksempel på et indkøbsvognmodul på Fabrikam-webstedet.](./media/cart2.PNG)

Det følgende billede viser et eksempel på en side med en indkøbsvogn på Fabrikam-webstedet. I dette eksempel er der et ekspeditionsgebyr for et linjeelement.

![Eksempel på et indkøbsvognmodul med et ekspeditionsgebyr for et linjeelement.](./media/ecommerce-handling-fee.png)

## <a name="cart-module-properties-and-slots"></a>Egenskaber og pladser i indkøbsvognmodulet

| Egenskab | Værdier | Betegnelse |
|----------------|--------|-------------|
| Overskrift | Overskriftstekst og en overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**) | En overskrift til vognen som f.eks. "Indkøbspose" eller "Varer i din indkøbsvogn". |
| Vis fejl for ikke på lager | **Sand** eller **Falsk** | Hvis denne egenskab er angivet til **Sand**, vil der blive vist lagerrelaterede fejl på siden for indkøbsvogn. Det anbefales, at du angiver denne egenskab til **Sand**, hvis der anvendes lagerkontroller på lokationen. |
| Vis forsendelsesgebyrer for linjeelementer | **Sand** eller **Falsk** | Hvis denne egenskab angives til **Sand**, vil linjeelementer i en indkøbsvogn vise forsendelsesgebyrer, hvis disse oplysninger er tilgængelige. Denne funktion understøttes ikke i Fabrikam-temaet, da brugere først vælger levering i betalingsflowet. Denne funktion kan dog aktiveres i andre arbejdsprocesser, hvis det er relevant. |
| Vis tilgængelige opprioriteringer| **Sand** eller **Falsk** | Hvis denne egenskab er angivet til **Sand**, viser indkøbsvognen tilgængelige kampagner baseret på varerne i indkøbsvognen. Denne egenskab er tilgængelig i version 10.0.16 af Dynamics 365 Commerce. |

## <a name="modules-that-can-be-used-in-a-cart-module"></a>Moduler, der kan bruges i et indkøbsvognmodul

- **Tekstblok** – Dette modul understøtter brugerdefinerede meddelelser i indkøbsvognmodulet. Meddelelserne styres af CMS (Content Management system). Der kan tilføjes en hvilken som helst besked f.eks. "Kontakt 1-800-Fabrikam, hvis der er problemer med din ordre".
- **Butiksvælger** – Dette modul viser en liste over butikker i nærheden, hvor en vare kan afhentes. Det giver brugerne mulighed for at angive en placering for butikker, der er i nærheden. Du kan få flere oplysninger om dette modul i [Butiksvælgermodul](store-selector.md).

## <a name="module-properties"></a>Modulegenskaber

De følgende indstillinger for indkøbsvognmodul kan konfigureres under **Indstillinger for websted \> Udvidelser**:

- **Maks. antal** – Denne egenskab bruges tl at angive det maksimale antal af hver vare, der kan føjes til indkøbsvognen. En detailhandler kan f. eks. beslutte, at der kun kan sælges 10 stk. af hvert produkt i en enkelt transaktion.
- **Lager** – Du finder oplysninger om, hvordan du anvender lagerindstillinger, under [Anvendelse af lagerindstillinger](inventory-settings.md).
- **Tilbage til indkøb** – Denne egenskab bruges til at angive ruten for linket **Tilbage til indkøb**. Ruten kan konfigureres på webstedsniveau, så detailhandlere kan føre kunden tilbage til startsiden eller en anden side på webstedet.

> [!IMPORTANT]
> I Dynamics 365 Commerce version 10.0.14 og senere samles varerne i indkøbsvognen ud fra de indstillinger, der er defineret i online funktionalitetsprofilen for onlinebutikken i Commerce Headquarters. Du kan finde flere oplysninger om, hvordan du opretter en online funktionalitetsprofil og angiver de egenskaber, der kræves til aggregering, i afsnittet [Oprette en online funktionalitetsprofil](online-functionality-profile.md).

## <a name="commerce-scale-unit-interaction"></a>Enhedsinteraktion i Commerce Scale

Indkøbsvognmodulet henter produktoplysninger vha. Commerce Scale Unit-API'er. Indkøbs-id'et fra browsercookien bruges til at hente alle produktoplysningerne fra Commerce Scale Unit.

## <a name="add-a-cart-module-to-a-page"></a>Føje et indkøbsvognmodul til en side

Hvis du vil føje et indkøbsvognmodul til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.

1. Gå til **Fragmenter**, og vælg **Nyt** for at oprette et nyt fragment.
1. Vælg modulet **Indkøbsvogn** i dialogboksen **Nyt fragment**.
1. Under **Fragmentnavn** skal du angive navnet **Indkøbsvognfragment** og derefter vælge **OK**.
1. Vælg **Indkøbsvogn**-pladsen.
1. Vælg blyantsymbolet i ruden Egenskaber til højre. Skriv overskriften i feltet, og vælg derefter markeringssymbolet.
1. På pladsen **Indkøbsvogn** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Butiksvælger** og derefter **OK**.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke fragmentet ind, og vælg derefter **Publicer** for at publicere det.
1. Gå til **Skabeloner**, og vælg **Ny** for at oprette en ny skabelon.
1. Angiv et navn for skabelonen under **Skabelonnavn** i dialogboksen **Ny skabelon**.
1. Vælg pladsen **Brødtekst** i dispositionstræet, vælg ellipsen (**...**), og vælg derefter **Tilføj fragment**.
1. I dialogboksen **Vælg fragment** skal du vælge **Indkøbsvognfragment** og derefter **OK**.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.
1. Gå til **Sider**, og vælg **Ny** for at oprette en ny side.
1. I dialogboksen **Vælg en skabelon** skal du vælge den skabelon, du har oprettet, angive et sidenavn og derefter vælge **OK**.
1. Vælg **Gem**, og vælg derefter **Vis** for at få vist siden.
1. Vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.

## <a name="additional-resources"></a>Yderligere ressourcer

[Ikonmodul for indkøbskurv](cart-icon-module.md)

[Betalingsmodul](add-checkout-module.md)

[Betalingsmodul](payment-module.md)

[Leveringsadressemodul](ship-address-module.md)

[Leveringsindstillingsmodul](delivery-options-module.md)

[Modul med afhentningsoplysninger](pickup-info-module.md)

[Ordredetaljer-modul](order-confirmation-module.md)

[Gavekortsmodul](add-giftcard.md)

[Beregne lagertilgængelighed for detailkanaler](calculated-inventory-retail-channels.md)

[Oprette en onlinefunktionalitetsprofil](online-functionality-profile.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]