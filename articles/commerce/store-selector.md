---
title: Butiksvælgermodul
description: Denne artikel omhandler modulet Butiksvælger og beskriver, hvordan du kan føje det til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
manager: annbe
ms.openlocfilehash: aa3aed837072cb6c3d4f7f92bec2f4b700408cf7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268313"
---
# <a name="store-selector-module"></a>Butiksvælgermodul

[!include [banner](includes/banner.md)]

Denne artikel omhandler modulet Butiksvælger og beskriver, hvordan du kan føje det til sider på websteder i Microsoft Dynamics 365 Commerce.

Kunder kan bruge butiksvælgermodulet til at hente et produkt i en valgt butik efter et onlineindkøb. I Commerce version 10.0.13 indeholder butiksvælgermodulet også yderligere egenskaber, der kan vise en **Find en butik**-side, der viser butikker i nærheden.

I butiksvælgermodulet kan brugerne angive en placering (by, stat, adresse osv.) til søgning efter butikker inden for en søgeradius. Når modulet åbnes første gang, bruges kundens browserplacering til at søge efter butikker (hvis der er givet samtykke).

## <a name="store-selector-module-usage"></a>Brug af butiksvælgermodul

- Et butiksvælgermodul kan bruges på siden med produktdetaljer (PDP) til at vælge en butik til afhentning.
- Et butiksvælgermodul kan bruges på en side med indkøbsvogn til at vælge en butik til afhentning.
- Et butiksvælgermodul kan bruges på en enkeltstående side, der viser alle tilgængelige butikker.

## <a name="fulfillment-group-setup-in-commerce-headquarters"></a>Konfigurere opfyldelsesgruppe i Commerce Headquarters

For at butiksvælgeren kan vise tilgængelige butikker, skal opfyldelsesgruppen være konfigureret i Commerce Headquarters. Du kan finde flere oplysninger under [Konfigurere opfyldelsesgrupper](customer-orders-overview.md#set-up-fulfillment-groups).

Derudover skal butikslokationens længdegrad og breddegrad defineres i hovedkontoret for hver butik i opfyldelsesgruppen.

Følg disse trin for at angive længde- og breddegrad for butiksadressen i Commerce Headquarters.

1. Gå til **Lagerstyring \> Opsætning \> Lageropdeling**.
1. Vælg lagerstedslokation i venstre rude.
1. Vælg **Avanceret** i oversigtspanelet **Adresser**.

    ![Eksempel på butiksoplysninger i hovedkvarter.](./media/Store-address.png)

1. Vælg **Rediger** i handlingsruden.
1. Angiv værdier for **Længdegrad** og **Breddegrad** i oversigtspanelet **Generelt**.

    ![Eksempel på konfiguration af breddegrad og længdegrad for en butik i hovedkontoret.](./media/Store-latitude-longitude.png)

1. Vælg **Gem** i handlingsruden. 

### <a name="hide-a-store-from-the-store-selector-module"></a>Skjule en butik fra modulet til butiksvælger

Nogle butikker i en opfyldelsesgruppe er muligvis ikke gyldige afhentningssteder. Hvis du vil sikre, at der kun vises gyldige afhentningssteder som indstillinger i modulet til butiksvælger, skal du følge disse trin i Commerce Headquarters.

1. Gå til **Retail og Commerce \> Konfiguration af Commerce \> Opfyldelsesgrupper \> Alle butikker**.
1. Vælg **Rediger** i handlingsruden.
1. Under **Konfiguration** skal du fjerne markeringen i afkrydsningsfeltet **Er afhentningslokation** for alle butikker, der ikke er en gyldig afhentningslokation.
1. Vælg **Gem** i handlingsruden.
1. Kør distributionstidsplanen 1070 **Kanalkonfiguration**.

## <a name="bing-maps-integration"></a>Bing Kort-integration

Butiksvælgermodulet er integreret med [Bing Kort REST-API'er (Application Programming Interfaces)](/bingmaps/rest-services/) der skal bruge funktionerne for Bings geokodnings- og automatiske forslagsfunktioner (Autosuggest). Der kræves en Bing Kort-API-nøgle, og den skal føjes til siden med delte parametre for Commerce Headquarters. Geokodnings-API'en bruges til at konvertere en placering til værdier for breddegrad og længdegrad. Integrationen med Autosuggest-API'en bruges til at vise søgeforslag, når brugerne angiver placeringer i søgefeltet.

For Autosuggest-REST-API'en skal du sikre, at følgende URL-adresser er tilladte pr. webstedets sikkerhedspolitik for indhold (CSP). Denne opsætning udføres i Commerce-webstedsgeneratoren ved at tilføje tilladte URL-adresser i forskellige CSP-direktiver for webstedet (f.eks. **img-src**). Du kan finde flere oplysninger under [Sikkerhedspolitik for indhold](manage-csp.md). 

- Til **connect-src**-direktivet skal du tilføje **&#42;.bing.com**.
- Til **img-src**-direktivet skal du tilføje **&#42;.virtualearth.net**.
- Til direktivet **script-src** skal du **tilføje &#42;.bing.com, &#42;.virtualearth.net**.
- Til direktivet **script style-src** skal du tilføje **&#42;.bing.com**.

## <a name="pickup-in-store-mode"></a>Afhent i butik-tilstand

Butiksvælgermodulet understøtter en **Afhent i butik**-tilstand, der viser en liste over butikker, hvor produktet er tilgængeligt for afhentning. Den viser også butiksåbningstider og produktlager for hver butik på listen. Butiksvælgermodulet kræver et produkts kontekst for at gengive produkttilgængeligheden og give brugeren mulighed for at føje produktet til indkøbsvognen, hvis produktets leveringsmåde er sat til **afhentning** i den valgte butik. Du finder flere oplysninger under [Lagerindstillinger](inventory-settings.md). 

Butiksvælgermodulet kan føjes til et købefeltmodul på siden med produktdetaljer (PDP) for at vise butikker, hvor et produkt kan afhentes. Modulet kan også føjes til et indkøbsvognmodul. I dette tilfælde viser butiksvælgermodulet afhentningsindstillinger for de enkelte linjeelementer i indkøbsvognen. Desuden kan butiksvælgermodulet føjes til andre sider eller moduler via udvidelser og tilpasninger.

Hvis dette scenarie skal fungere, skal produkterne konfigureres med leveringstilstanden **afhentning**. Ellers bliver modulet ikke vist på produktsiderne. Du kan finde flere oplysninger om, hvordan du kan konfigurere leveringsmåden, under [Konfigurere leveringsmåder](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Følgende billede viser et eksempel på et butiksvælgermodul, der bruges på en produktoplysningsside (PDP).

![Eksempel på et butiksvælgermodul, der bruges på en PDP.](./media/BOPIS.PNG)

> [!NOTE]
> I version 10.0.16 og nyere versioner kan der aktiveres en ny funktion, som giver en organisation mulighed for at definere flere afhentningsmåder i leveringsindstillinger for debitorer.  Hvis denne funktion er aktiveret, vil butiksvælgeren og andre e-handelsmoduler blive forbedret, så brugeren potentielt kan vælge mellem flere muligheder for at afhente leveringer, hvis de er konfigureret.  Yderligere oplysninger om denne funktion finder du i [denne dokumentation](./multiple-pickup-modes.md). 

## <a name="find-stores-mode"></a>Find butikker-tilstand

Butiksvælgermodulet understøtter også tilstanden **Find butikker**. Denne tilstand kan bruges til at oprette en side med butiksadresser, der viser de tilgængelige butikker og deres oplysninger. I denne tilstand fungerer butiksvælgermodulet uden produktkontekst og kan bruges som et enkeltstående modul på alle websider. Hvis de relevante indstillinger er slået til for modulet, kan brugerne også vælge en butik som deres foretrukne butik. Når der vælges en butik som en brugers foretrukne butik, gemmes butiks-id'et i browserens cookie. Brugeren skal derfor acceptere en meddelelse om samtykke til cookie.

I følgende illustration vises et eksempel på et butiksvælgermodul, der bruges sammen med et kortmodul på en butiksadresseside.

![Eksempel på et butiksvælgermodul og et kortmodul på en side med butiksadresser.](./media/ecommerce-Storelocator.PNG)

## <a name="render-a-map"></a>Gengive et kort

Butiksvælgermodulet kan bruges sammen med kortmodulet til at vise butiksadresser på et kort. Yderligere oplysninger om kortmodulet finder du i [Kortmodul](map-module.md)

## <a name="store-selector-module-properties"></a>Egenskaber for modulet Butiksvælger

| Egenskabsbetegnelse | Værdi | Beskrivende tekst |
|---------------|-------|-------------|
| Overskrift | Tekst | Overskrift for modulet. |
| Måde | **Find butikker** eller **Afhent i butik** | **Find butikker** viser tilgængelige butikker. **Afhent i butik** vælger en butik til afhentning. |
| Dessin | **Dialogboks** eller **Indbygget** | Modulet kan gengives enten indbygget eller i en dialogboks. |
| Indstil som foretrukken butik | **Sand** eller **Falsk** | Når denne egenskab angives til **Sand**, kan brugere angive en foretrukken butik. Denne funktion kræver, at brugere accepterer en meddelelse om samtykke til cookie. |
| Vis alle butikker | **Sand** eller **Falsk** | Når denne egenskab angives til **Sand**, kan brugere omgå egenskaben **Søgeradius** og få vist alle butikker. |
| Indstillinger for Autosuggest: maks. resultater | Tal | Denne egenskab definerer det maksimale antal automatiske forslagsresultater, der kan vises via Bing Autosuggest-API. |
| Søgeradius | Tal | Denne egenskab definerer søgeradius for butikker, i miles. Hvis der ikke er angivet en værdi, bruges standardradiussen på 50 miles. |
| Vilkår for brug | URL |  Denne egenskab specificerer de servicebetingelser for URL-adressen, der kræves for at kunne bruge tjenesten Bing Kort. |

## <a name="site-settings"></a>Indstillinger for websted

Modulet til butiksvælger overholder [indstillingerne for Tilføjelse af produkt til indkøbsvogn](add-cart-settings.md). Når en vare er føjet til indkøbsvognen fra modulet til butiksvælger, kan webstedsbrugerne se de relevante konfigurerede arbejdsgange.

## <a name="add-a-store-selector-module-to-a-page"></a>Føje et butiksvælgermodul til en side

For **Afhent i butik**-tilstand kan modulet kun bruges på PDP'er og kortsider. Du skal angive tilstanden til **Afhent i butik** i egenskabsruden for modulet.

- Yderligere oplysninger om, hvordan du føjer et butiksvælgermodul til et købefeltmodul, finder du under [Købefeltmodul](add-buy-box.md). 
- Oplysninger om, hvordan du føjer et butiksvælgermodul til et indkøbsvognmodul, finder du under [Indkøbsvognmodul](add-cart-module.md)

Hvis du vil konfigurere butiksvælgermodulet til at vise tilgængelige butikker for en side med butiksadresser som i den illustration, der vises tidligere i denne artikel, skal du følge disse trin.

1. Gå til **Skabeloner**, og vælg **Ny** for at oprette en ny skabelon.
1. I dialogboksen **Ny skabelon** skal du under **Skabelonnavn** angive **Marketingskabelon** og derefter klikke på **OK**.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.
1. Gå til **Sider**, og vælg **Ny** for at oprette en ny side.
1. Angiv **Butikslokationer** under **Sidenavn** i dialogboksen **Opret en ny side**, og vælg derefter **Næste**.
1. Vælg den **Marketingskabelon**, du oprettede, under **Vælg en skabelon**, og vælg derefter **Næste**.
1. Vælg et sidelayout (f.eks. **Fleksibelt layout**) under **Vælg et layout**, og vælg derefter **Næste**.
1. Gennemse sidekonfigurationen under **Gennemse og afslut**. Hvis du vil redigere sideoplysningerne, skal du vælge **Tilbage**. Hvis sideoplysningerne er korrekte, skal du vælge **Opret side**. 
1. På pladsen **Hoved** på den nye side skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Vælg moduler** skal du vælge modulet **Container** og derefter **OK**.
1. På pladsen **Container** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Vælg moduler** skal du vælge modulet **Container med 2 kolonner** og derefter vælge **OK**.
1. Angiv **Bredde**-værdien til **Fuld container** i egenskabsruden for modulet.
1. Angiv værdien af **Konfiguration af ekstra lille visningsport** til **100 %**.
1. Angiv værdien af **Konfiguration af lille visningsport** til **100 %**.
1. Angiv værdien af **Konfiguration af mellemstor visningsport** til **33 % 67 %**.
1. Angiv værdien af **Konfiguration af stor visningsport** til **33 % 67 %**.
1. På pladsen **Container med 2 kolonner** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Vælg moduler** skal du vælge modulet **Butiksvælger** og derefter **OK**.
1. Angiv **Tilstand**-værdien til **Find butikker** i egenskabsruden for modulet.
1. Angiv værdien **Søgeradius** i miles.
1. Angiv andre egenskaber som f.eks. **Angiv som foretrukken butik**, **Vis alle butikker** og **Aktivér automatisk forslag** efter behov.
1. På pladsen **Container med 2 kolonner** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.
1. I dialogboksen **Vælg moduler** skal du vælge modulet **Kort** og derefter **OK**.
1. Angiv eventuelle yderligere egenskaber efter behov i ruden med egenskaber for modulet.
1. Vælg **Gem**, vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.
 
## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over modulbibliotek](starter-kit-overview.md)

[Boksmodul til køb](add-buy-box.md)

[Indkøbskurvsmodul](add-cart-module.md)

[Hurtig rundvisning i PDP](quick-tour-pdp.md)

[Hurtig rundvisning i indkøbsvogn og betaling](quick-tour-cart-checkout.md)

[Konfigurer leveringsmåder](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[Administrere Bing Kort for din organisation](dev-itpro/manage-bing-maps.md)

[Bing Kort-REST-API'er](/bingmaps/rest-services/)

[Kortmodul](map-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
