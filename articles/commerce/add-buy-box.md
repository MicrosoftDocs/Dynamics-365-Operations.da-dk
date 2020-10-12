---
title: Købefeltmodul
description: Dette emne omhandler købefeltmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e07bf02f10c943947fdf9ed3333373b859ff5b6c
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817079"
---
# <a name="buy-box-module"></a>Købefeltmodul

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Dette emne omhandler købefeltmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Termen *købefelt* refererer normalt til det område på en produktdetaljeside, der er "over folden", og som omfatter alle de vigtigste oplysninger, der kræves for at foretage et produktkøb. (et område, der er "over folden", er synligt med det samme, når siden indlæses, så brugerne ikke behøver at rulle ned for at se den).

Et købefeltmodul er en særlig container, der omfatter alle de moduler, som vises i købefeltområdet på en side med produktdetaljer.

URL-adressen for siden produktdetaljer indeholder produkt-id'et. Alle de oplysninger, der kræves for at gengive et købefeltmodul, er afledt af dette produkt-id. Hvis der ikke er angivet et produkt-ID, gengives købefeltmodulet ikke korrekt på en side. Derfor kan et købsfeltmodul kun bruges på sider med en produktkontekst. Hvis du vil bruge den på en side, der ikke har en produktkontekst (f.eks. en startside eller en marketingside), skal du udføre flere tilpasninger.

Det følgende billede viser et eksempel på et købefeltmodul på en side med produktdetaljer.

![Eksempel på et købefeltmodul](./media/ecommerce-pdp-buybox.PNG)

## <a name="buy-box-module-properties-and-slots"></a>Egenskaber og pladser i købefeltmodulet 

På siden med produktdetaljer er et købefelt opdelt i to områder: et medieområde til venstre og et indholdsområde til højre. Forholdet mellem bredden af kolonnen med medieområder og bredden af kolonnen med indholdsområder er som standard 2:1. På mobile enheder er de to områder stablet, så det ene område vises under det andet område. Du kan bruge temaer til at tilpasse kolonnebredder og stablingsrangering.

I et købsfeltmodul vises titlen, beskrivelsen, prisen og klassifikationen for et produkt. Kunderne kan også vælge produktvarianter, der har forskellige produktattributter, f.eks. størrelse, typografi og farve. Når der er valgt en produktvariant, opdateres andre egenskaber i købefeltet (f. eks. produktbeskrivelsen og -billederne), så de afspejler variantoplysningerne. 

Der angives en mængdevælger, så debitorer kan angive antallet af varer, der skal købes. Det maksimale antal, der kan købes, kan defineres i indstillingerne for webstedet.

Fra købsfeltet kan kunderne også udføre handlinger, som f.eks. føje et produkt til indkøbsvognen, føje et produkt til ønskelisten og vælge et afhentningssted. Disse handlinger kan udføres på et produkt eller en produktvariant. Hvis du vil føje et produkt til en ønskeliste, skal kunden være logget på.

Temaer kan bruges til at fjerne eller ændre rækkefølgen af købsfeltets produktegenskaber og handlingskontroller. 

## <a name="module-properties"></a>Modulegenskaber

- **Overskriftskode** – Denne egenskab definerer overskriftskoden for produkttitlen. Hvis købsfeltet vises øverst på siden, skal denne egenskab indstilles til **h1** for at overholde tilgængelighedsstandarder. 

- **Aktivér anbefalinger af "Køb tilsvarende"** – Denne egenskab giver feltet Køb mulighed for at vise links til produkter, der ligner den aktuelt viste vare. Denne funktion er tilgængelig i Commerce version 10.0.13 og nyere.

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a>Moduler, der kan bruges i et købefeltmodul

- **Mediegalleri** – dette modul bruges til at vise billeder af et produkt på en side med produktdetaljer. Yderligere oplysninger om dette modul finder du i [Mediegallerimodul](media-gallery-module.md).
- **Butiksvælger** – Dette modul viser en liste over butikker i nærheden, hvor en vare kan afhentes. Det giver brugerne mulighed for at angive en placering for butikker, der er i nærheden. Yderligere oplysninger om dette modul finder du i [Butiksvælgermodul](store-selector.md).
- **Social deling** - Dette modul kan føjes til feltet Køb for at give brugere mulighed for at dele produktoplysninger på sociale medier. Du kan få flere oplysninger under [Modulet Social deling](social-share-module.md).

## <a name="buy-box-module-settings"></a>Indstillinger for købefeltmodul

De følgende indstillinger for købefeltmoduler kan konfigureres under **Indstillinger for websted \> Udvidelser**:

- **Grænse for antal linjevarer i indkøbsvogn** – Denne egenskab bruges tl at angive det maksimale antal af hver vare, der kan føjes til indkøbsvognen. En detailhandler kan f. eks. beslutte, at der kun kan sælges 10 stk. af hvert produkt i en enkelt transaktion.
- **Lager** – Du finder oplysninger om, hvordan du anvender lagerindstillinger, under [Anvendelse af lagerindstillinger](inventory-settings.md).
- **Føj til indkøbsvogn** – Denne egenskab bruges til at angive proceduren, når en vare er føjet til indkøbsvognen. De mulige værdier er **Naviger til indkøbsvogn**, **Naviger ikke til indkøbsvogn** og **Vis beskeder**. Når værdien er angivet til **Naviger til indkøbsvogn**, sendes brugeren til indkøbsvognen, når der er tilføjet en vare. Når værdien er angivet til **Naviger ikke til indkøbsvogn**, sendes brugeren ikke til siden med indkøbsvognen, når der er tilføjet en vare. Når værdien er angivet til **Vis beskeder**, får brugerne vist en bekræftelsesmeddelelse og kan fortsætte med at søge på siden produktdetaljer. 

> [!IMPORTANT]
> Indstillingerne for webstedet **Føj til indkøbskurv** er tilgængelige i Dynamics 365 Commerce version 10.0.11. Hvis du opdaterer fra en ældre version af Dynamics 365 Commerce, skal du opdatere filen appsettings.json manuelt. Oplysninger om opdatering af filen appsettings.json finder du under [Opdateringer til SDK og modulbibliotek](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file). 

Det følgende billede viser et eksempel på en besked med bekræftelse af handlingen "Føjet til indkøbsvogn" på Fabrikam-webstedet.

![Eksempel på et beskedmodul](./media/ecommerce-addtocart-notifications.PNG)

## <a name="commerce-scale-unit-interaction"></a>Enhedsinteraktion i Commerce Scale

Købsfeltmodulet henter produktoplysninger ved hjælp af Commerce Scale Unit-API'er (Application Programming Interfaces). Produkt-id'et fra siden med produktdetaljer bruges til at hente alle oplysninger.

## <a name="add-a-buy-box-module-to-a-page"></a>Føje et købefeltmodul til en side

Hvis du vil føje et købefeltmodul til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.

1. Gå til **Fragmenter**, og vælg **Nyt** for at oprette et nyt fragment.
1. Vælg modulet **Købefelt** i dialogboksen **Nyt fragment**.
1. Under **Fragmentnavn** skal du angive navnet **Købefeltfragment** og derefter vælge **OK**.
1. På pladsen **Media Gallery** i købefeltmodulet skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Media Gallery** og derefter **OK**.
1. På pladsen **Butiksvælger** i købefeltmodulet skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Butiksvælger** og derefter **OK**.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke fragmentet ind, og vælg derefter **Publicer** for at publicere det.
1. Gå til **Skabeloner**, og vælg **Ny** for at oprette en ny skabelon.
1. Angiv **PDP-skabelon** under **Skabelonnavn** i dialogboksen **Ny skabelon**, og vælg derefter **OK**.
1. På pladsen **Brødtekst** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. dI dialogboksen **Tilføj modul** skal du vælge modulet **Standardside** og derefter **OK**.
1. Vælg pladsen **Hoved** på standardsiden, vælg ellipsen (**...**) og derefter **Tilføj fragment**.
1. I dialogboksen **Vælg fragment** skal du vælge det **Købefeltfragment**, som du tidligere har valgt, og derefter vælge **OK**.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.
1. Gå til **Sider**, og vælg **Ny** for at oprette en ny side.
1. Vælg dialogboksen **Vælg en skabelon**, og vælg skabelonen **PDP-skabelon**. Under **Sidenavn** skal du angive **PDP-side** og derefter vælge **OK**.
1. Vælg pladsen **Hoved** på den nye side, vælg ellipsen (**...**), og vælg derefter **Tilføj fragment**.
1. I dialogboksen **Vælg fragment** skal du vælge det **Købefeltfragment**, som du tidligere har valgt, og derefter vælge **OK**.
1. Gem siden, og se en forhåndsvisning af den. Føj forespørgselsstrengparameteren **?productid=&lt;product id&gt;** til URL-adressen for eksempelsiden. På denne måde bruges produktkonteksten til at indlæse og gengive eksempelsiden.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den. Der vises et købefelt på siden med produktdetaljer.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over modulbibliotek](starter-kit-overview.md)

[Butiksvælgermodul](store-selector.md)

[Mediegallerimodul](media-gallery-module.md)

[Container-modul](add-container-module.md)

[Indkøbskurvsmodul](add-cart-module.md)

[Betalingsmodul](add-checkout-module.md)

[Ordrebekræftelsesmodul](order-confirmation-module.md)

[Overskriftsmodul](author-header-module.md)

[Sidefodsmodul](author-footer-module.md)

[Modul til deling på sociale medier](social-share-module.md)

[Beregne lagertilgængelighed for detailkanaler](calculated-inventory-retail-channels.md)

[Opdateringer til SDK og modulbibliotek](e-commerce-extensibility/sdk-updates.md)
