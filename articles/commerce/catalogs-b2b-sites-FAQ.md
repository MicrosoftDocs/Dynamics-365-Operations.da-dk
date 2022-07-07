---
title: Ofte stillede spørgsmål til Commerce-kataloger til B2B
description: Denne artikel indeholder svar på ofte stillede spørgsmål om Microsoft Dynamics 365 Commerce-kataloger.
author: ashishmsft
ms.date: 05/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: af69c3d27142a961049470dd1292ffbc3d8387a9
ms.sourcegitcommit: 6616b969afd6beb11a79d8e740560bf00016ea7f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/17/2022
ms.locfileid: "9027362"
---
# <a name="commerce-catalogs-for-b2b-faq"></a>Ofte stillede spørgsmål til Commerce-kataloger til B2B

[!include [banner](includes/banner.md)]

Denne artikel indeholder svar på ofte stillede spørgsmål om Microsoft Dynamics 365 Commerce [business-to-business (B2B)-kataloger](catalogs-b2b-sites.md).

## <a name="why-cant-i-configure-a-catalog-specific-navigation-hierarchy-or-see-an-option-to-associate-a-customer-hierarchy"></a>Hvorfor kan jeg ikke konfigurere et katalogspecifikt navigationshierarki eller få vist en indstilling for at tilknytte et debitorhierarki?

Kontroller, at funktionen **Aktivér brug af flere kataloger på detailkanaler** er aktiveret i arbejdsområdet til **funktionsstyring** i Commerce Headquarters. Sørg desuden for, at dit miljø bruger versionen af Commerce version 10.0.27 eller en senere version.

## <a name="can-i-view-the-catalog-specific-hierarchy-and-enrich-category-pages-in-commerce-site-builder"></a>Kan jeg få vist det katalogspecifikke hierarki og de katalogspecifikke kategorisider i Commerce site builder?

Ja, brugere af Commerce Site Builder, der har adgang til siden **Produkter** i Site Builder, kan vælge et katalog og få vist det katalogspecifikke hierarki. Fra siden **Produkter** kan brugere også være aktive på en kategoriside for en bestemt kategori i kataloget. Du kan finde flere oplysninger under [Forbedre en kategorilandingsside](enrich-category-page.md). Hvis du skal have en anderledes placering, end der er specifik for kataloget, anbefales det, at du har et specifikt og entydigt navigationshierarki til kataloget.

## <a name="can-a-b2b-shopper-purchase-from-multiple-catalogs-in-a-single-checkout"></a>Kan et B2B-køb køb fra flere kataloger med én betaling i kassen?

Ja, køb fra flere kataloger i en enkelt udtjekning er tilladt. B2B-kataloger kan bruge katalogindikatoren i indkøbsvognsvisningen til at bestemme, hvilke varer der er tilføjet fra hvilke kataloger.

## <a name="if-a-b2b-shopper-purchases-the-same-item-from-different-catalogs-what-is-the-expected-behavior"></a>Hvis en B2B-indkøber den samme vare fra forskellige kataloger, hvad er den forventede funktionsmåde?

Selv om en bestemt bruger kan have adgang til flere kataloger på et givet tidspunkt, er det vigtigt, at produkter i disse kataloger udelukker gensidigt hinanden. Det vil sige, at det samme produkt ideelt set ikke må indgå i mere end ét katalog for en bestemt bruger.

Hvis der opstår en situation, hvor det samme produkt tilhører flere kataloger, vedligeholder systemet dog flere indkøbsvognslinjer for det pågældende produkt. Der vil være en separat linje for hvert katalog. Det samme produkt fra to forskellige kataloger flettes ikke ved kassen.

## <a name="when-a-b2b-shopper-is-shopping-is-there-any-validation-for-catalog-availability"></a>Når et B2B-katalog er på indkøb, findes der så nogen validering af katalogtilgængelighed?

Ja. En B2B-kunde kan kun fortsætte til betaling ved kassen, hvis alle varerne i indkøbskurven er fra gyldige kataloger. Hvis indkøbsvognsvarer er fra udløbne eller åbnede kataloger, fjernes de, og brugeren får besked.

## <a name="during-the-shopping-experience-are-search-and-product-discovery-including-related-and-recommended-product-collections-catalog-specific"></a>Under indkøbsoplevelsen er der søge- og produktregistreringskatalogspecifik (herunder relateret og anbefalet produktsamling).

Ja. Så snart en bruger vælger et bestemt katalog, bliver hele indkøbskurven katalogspecifik. Disse oplysninger omfatter søgeerfaringer som f.eks. søgeforslag, søgeresultater, kategoriresultater, forfinere, priser, attributter og anbefalede produkter (f.eks. nye, bedst sælgende, tendensoplysninger, ofte købt sammen og relaterede produkter).

## <a name="can-a-b2b-shopper-purchase-from-the-default-assortment-catalogid0"></a>Kan et B2B-indkøb fra standardsortimmentet (catalogID=0)?

Nej, et B2B-produkt har ikke tilladelse til at købe fra standardsortimentet. Sortimentet er kun beregnet til anonym søgning. Hvis der mangler katalogtildelinger i B2B (mens de venter på at blive opdateret fra administrationen), kan de ikke se de kataloger, de kan vælge imellem, og der vil ikke blive vist et kategorihierarki.

## <a name="can-marketing-content-be-curated-for-a-product-that-is-specific-to-a-catalog"></a>Kan marketingindhold fremstilles for et produkt, der er specifikt for et katalog?

Aktuelt understøttes produktforbedring kun på websteds- og kanalniveau. Med andre ord: Hvis et produkt bliver åbnet, deles det på tværs af flere kataloger, og den tilsvarende side med produktdetaljer (PDP) for det pågældende produkt vil blive gengivet på samme måde på tværs af alle kataloger for et bestemt websted.

## <a name="is-catalog-support-available-for-both-b2b-and-business-to-consumer-b2c-online-channels"></a>Er katalogsupport tilgængelig for både B2B- og B2C-onlinekanaler?

I øjeblikket er det tilsigtet, at handelskataloger kun fungerer med B2B-kanaler.

## <a name="can-we-set-up-catalog-specific-upsellcross-sell-items"></a>Kan vi konfigurere katalogspecifikt mersalg /tillægssalg?

I øjeblikket understøttes kun relaterede produkter. Konfigurationerne af ups fejl og krydssalgsvare er dog tilgængelige for callcentre.

Følgende funktioner understøttes også kun for opkaldscentre:

- Katalogkildekoder
- Bruge kilde-id til at spore omkostninger og svarrater
- Katalogspecifikke ordre- og varescripts
- Analyse af katalogside
- Kataloganmodninger
- Betalingsplaner
- Gratis produkter baseret på kildekoder

## <a name="can-we-use-catalog-source-codes-for-b2b-orders-through-the-e-commerce-portal"></a>Kan vi bruge katalogkildekoder til B2B-ordrer via e-commerce-portalen?

Nej Katalogkildekoder understøttes kun for callcenter-kanaler.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oprette handelskataloger til B2B-websteder](catalogs-b2b-sites.md)

[Udvidet virkning af Commerce-kataloger til B2B-tilpasninger](catalogs-b2b-sites-dev.md)
