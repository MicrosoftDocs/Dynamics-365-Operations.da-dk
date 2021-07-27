---
title: Oversigt over sider med produktdetaljer
description: Dette emne indeholder en oversigt over sider med produktdetaljer (PDP'er) i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: intro-internal
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3a1fbd6a71c8d00e862183c32fb9f7e17dcc5bd1
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2021
ms.locfileid: "6351982"
---
# <a name="product-details-pages-overview"></a>Oversigt over sider med produktdetaljer

[!include [banner](includes/banner.md)]

Dette emne indeholder en oversigt over sider med produktdetaljer (PDP'er) i Microsoft Dynamics 365 Commerce.

En PDP viser detaljerede oplysninger om et produkt og gør det muligt for kunderne at vælge produktindstillinger, f.eks. størrelse, stil og farve. En PDP bør vise alle de produktoplysninger, en kunde har brug for til at kunne træffe en beslutning om køb.

Følgende illustration viser et eksempel på en PDP.

![Eksempel på en side med produktdetaljer.](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a>Overskrifts- og sidefodsmoduler

Den øverste del af en PDP har et sidehoved, der viser alle produktkategorierne og andre sider, som forhandleren ønsker, at kunderne skal gennemse. Nederst på siden er der en sidefod, der indeholder hurtige links til forskellige emner, som kan have interesse for kunderne.

## <a name="buy-box-module"></a>Boksmodul til køb

Det vigtigste modul på en PDP er modulet med købsfeltet, som vises som det første element i hovedsektionen på siden. I et købsfeltmodul vises vigtige produktoplysninger, f.eks. produktnavn, produktbeskrivelse, produktpris, produktbilleder og produktvurderinger.

I boksmodulet til køb kan kunden vælge produktindstillinger (f.eks. en størrelse, en stil og en farve) og føje produktet til indkøbsvognen. Det giver også kunden mulighed for at købe produktet online og plukke det på et lager. Køb online, og afhent i butikken-modulet bruger integration med Bing Kort-API'er (Application Programming Interfaces) til at finde butikker i nærheden eller butikker på et andet sted, som kunden angiver.

Et boksmodul til køb kræver et produkt-id. Dette id er afledt af sidekonteksten. Hvis der føjes et boksmodul til køb på en side, hvor sidekonteksten ikke indeholder et produkt-id, gengives oplysningerne ikke korrekt.

## <a name="product-specifications-module"></a>Modul til produktspecifikationer

Modulet til produktspecifikationer kan bruges til at vise yderligere oplysninger om produktet. Disse oplysninger hentes fra produktattributter i Commerce. I modulet til produktspecifikationer vises alle attributter, hvor egenskaben **synlig** er angivet til **sand**. Der kræves et produkt-id for at hente produktattributterne.

## <a name="recommendations-module"></a>Anbefalingsmodulet

Anbefalingsmodulet er et vigtigt modul på en PDP. Mens kunder søger efter produkter, bør der fremlægges flere produktmuligheder for dem, så de kan finde det rigtige produkt og foretage et køb. Anbefalinger hjælper kunderne med nemt at finde relateret indhold og fortsætte med at handle.

Der findes forskellige typer af anbefalingslister:

- Listen **Personer synes også om** er baseret på maskinel indlæring. Den bruger transaktionshistorikken fra andre kunder til at give anbefalinger. Denne liste genereres af anbefalingstjenesten og minder om listetypen "Kunder, der købte dette, købte også...". Der kræves et produkt-id for at generere denne liste.
- Der kan konfigureres en **Relateret**-liste for et produkt i Commerce. Til en brun rejsetaske i læder kan der f.eks. være konfigureret flere tasker, der er fremstillet af læder eller designet til rejsebrug, på den relaterede liste. Andre typer af relaterede lister som f.eks. **Tilbehør** og **Mere som dette** kan også konfigureres i Commerce. Der kræves et produkt-id for at generere denne liste. Hvis sidekonteksten ikke omfatter et produkt-id, vil listen derfor være tom, hvis den føjes til en startside.
- Algoritmisk genererede anbefalingslister, f.eks. **Mest populære**, **Mest solgte** og **Nyt**, kan bruges på PDP'er. Selvom disse lister ikke er direkte relateret til produktet på PDP, kan de også hjælpe kunderne med at finde produkter, der er interessante for dem. Disse typer lister kræver ikke et produkt-id. De er standardlister, der genereres på basis af indkøbsmønstre på tværs af webstedet.
- Redaktionelle lister er manuelt fremstillede lister. En forhandler kan f.eks. manuelt fremstille lister over produkter, der skal vises frem.

## <a name="ratings-and-reviews-modules"></a>Moduler til vurderinger og anmeldelser

Tre moduler kan bruges til at vise og tilføje anmeldelser:

- **Anmeldelser** – Modulet indeholder vurderinger og anmeldelser, der er leveret af andre kunder. Kunderne kan sortere og filtrere anmeldelserne. Dette modul giver også kunder mulighed for at synes om eller ikke synes om anmeldelser, og de kan rapportere problemer.
- **Skriv anmeldelse** – Med dette modul kan kunderne skrive deres egne anmeldelser af et produkt.
- **Vurderingshistogram** – Dette modul indeholder et histogram, der viser vurderingstendensen for et produkt.

Du kan finde flere oplysninger under [Oversigt over vurderinger og anmeldelser](ratings-reviews-overview.md).

## <a name="marketing-modules"></a>Marketingmoduler

Hvis marketingindhold er entydigt for et bestemt produkt, kan der føjes et marketingmodul til PDP. Du kan føje marketingmoduler til en PDP ved at "forbedre" siden. Du kan finde flere oplysninger under [Forbedre en produktside](enrich-product-page.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over startside](quick-tour-home-page.md)

[Oversigt over sider til indkøbsvogn og betaling ved kassen](quick-tour-cart-checkout.md)

[Oversigt over sider til kontostyring](quick-tour-account-management.md)

[Forbedre en side med produktdetaljer](enrich-product-page.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
