---
title: Oversigt over standardlandingsside for kategori og side for søgeresultater
description: Denne artikel indeholder en oversigt over standardlandingsside for kategori og side for søgeresultater i Dynamics 365 Commerce.
author: ashishmsft
ms.date: 06/30/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.assetid: ''
ms.openlocfilehash: 1f2e4eb8825dd690f926f7f0bdfc39f1eb5fb83c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276367"
---
# <a name="default-category-landing-page-and-search-results-page-overview"></a>Oversigt over standardlandingsside for kategori og side for søgeresultater

[!include [banner](includes/banner.md)]

Denne artikel indeholder en oversigt over standardlandingssiden for kategorier og søgeresultatsiden for e-handel i Microsoft Dynamics 365 Commerce.

## <a name="default-category-landing-page"></a>Standardlandingsside for kategorier

Standardlandingssiden for kategorier er den side, som brugerne af et websted typisk får vist, når de vælger en kategori i navigationshierarkiet. Du kan gennemse kategorisiden, og du kan også sortere og finpudse de kategoriserede produkter.

![Standardlandingsside for kategorier.](./media/SimpleCategoryLandingDressCategory.png)

Øverst på siden findes et sidehoved, der viser alle produktkategorierne og andre sider, som produktchefen har kategoriseret. Konfigurationen udføres som en del af konfigurationen af kanalnavigationshierarkiet. Nederst på startsiden findes en sidefod med hurtige links til forskellige artikler, som kan have interesse for kunderne.

Følgende komponenter er vigtige for en kategori:

- **Felter til produktplacering** viser de produkter, som produktchefen har defineret i en kategori som et let i konfigurationen af navigationshierarkiet.
- **Oversigt over afgrænsere og valg** er filtre, der viser antal, og som kan bruges til at afgrænse elementer. Produktchefen konfigurerer dem som en del af konfigurationen af de metadata, der er relateret til kanalkategorier og produktattributter.
- **Sorteringsindstillinger** bruges af besøgende på webstedet til at sortere produkterne. Følgende sorteringsindstillinger er som standard tilgængelige:

    - Pris – lav til høj
    - Pris – høj til lav
    - Produktnavn – \[A-Z\]
    - Produktnavn – \[Z-A\]
    - Vurderinger – lav til høj
    - Vurderinger – høj til lav

- **Avancerede sorteringsindstillinger** bruges af besøgende på webstedet til at sortere produkterne efter intelligente kriterier. Når du aktiverer [Produktanbefalinger](product-recommendations.md) er følgende sorteringsmuligheder tilgængelige: Du kan få flere oplysninger i artiklen [Typer af produktanbefalinger](product-recommendations.md#types-of-product-recommendations).

    - Ny(t)
    - Mest sælgende
    - Mest populære

- **Sideinddeling** lader de besøgende på webstedet flytte fra én side med kategoriserede produktresultater til en anden side.
- **Samlet antal** viser det samlede antal produkter, der er defineret i en kategori.

## <a name="enrich-a-category-landing-page"></a>Forbedre en kategorilandingsside

Hvis du ønsker, at en landingsside for en kategori skal have en mere skræddersyet oplevelse for en bestemt kategori, kan du "forbedre" kategorilandingssiden for den pågældende kategori. Du kan f.eks. tilføje en marketingvideo og fortælle om kategorien for at få kundernes opmærksomhed. Du kan finde flere oplysninger under [Forbedre en kategorilandingsside](enrich-category-page.md).

![Forbedre en kategorilandingsside.](./media/CategoryLandingPages.png)

## <a name="auto-suggest-and-search-results-pages"></a>Sider med automatiske forslag og søgeresultater

Brugere af websteder kan udforske et websted ved enten at gå til en kategori fra navigationshierarkiet eller ved at angive et søgeord i søgefeltet.

Så snart brugerne går i gang med at skrive i søgefeltet, oplever de den avancerede funktion til automatiske forslag, der foreslår søgeord.

Her er nogle af de typer forslag, der kan vises:

- **Nøgleord** bruges til at finde produkter på tværs af alle produkter, der er udvalgt til kanalen.
- **Produkter** giver direkte links til siden med produktdetaljer.
- **Søgeforslag for kategoriområde** viser forskellige kategorier og lader brugere søge efter nøgleordet i en bestemt kategori.

![Avancerede automatiske forslag.](./media/ImmersiveAutoSuggestUX.png)

Når brugerne vælger et af søgeforslagene for nøgleord eller områdekategori, eller når der ikke er nogen forslag til det søgeord, de angiver, omdirigeres de til en side med søgeresultater. Brugerne kan derefter gennemse, sortere og finjustere listen over søgeresultater for at finde det ønskede produkt.

![Landingsside for søgeresultater.](./media/SearchLanding.png)

Følgende komponenter er vigtige for en søgeresultatside:

- **Produktplaceringsfelter** viser produkterne til brugerens søgning. Disse felter sorteres som standard af det skybaserede søgerelevansresultat for brugersøgningen.
- **Oversigt over afgrænsere og valg** er filtre, der viser antal, og som kan bruges til at afgrænse elementer. Produktchefen konfigurerer dem som en del af konfigurationen af metadataene for "kanalkategorier og produktattributter".
- **Standardsorteringsindstillinger** bruges af besøgende på webstedet til at sortere produkterne. Følgende sorteringsindstillinger er som standard tilgængelige:

    - Pris – lav til høj
    - Pris – høj til lav
    - Produktnavn – \[A-Z\]
    - Produktnavn – \[Z-A\]
    - Vurderinger – lav til høj
    - Vurderinger – høj til lav
    - Standard 
    
    > [!NOTE]
    > Hvis der er defineret værdier af **Visningsrækkefølge** for produkterne i navigationshierarkiet, vil sortering som standard på en kategoriside overholde de værdier, der er defineret i **Visningsrækkefølge**. Ellers sorteres efter **Produktnummer**.
    
- **Avancerede sorteringsindstillinger** bruges af besøgende på webstedet til at sortere produkterne efter intelligente kriterier. Når du aktiverer [Produktanbefalinger](product-recommendations.md) er følgende sorteringsmuligheder tilgængelige: Du kan få flere oplysninger i artiklen [Typer af produktanbefalinger](product-recommendations.md#types-of-product-recommendations).

    - Ny(t)
    - Mest sælgende
    - Mest populære

- **Sideinddeling** lader de besøgende på webstedet flytte fra én side med kategoriserede produktresultater til en anden side.
- **Samlet antal** viser det samlede antal produkter, der er defineret i en kategori, og som opfylder søgekriterierne.

>[!NOTE]
>Disse cloud-aktiverede søgemuligheder er tilgængelige fra og med version 10.0.8. Kontroller, at der er en post for "ProductSearch.UseAzureSearch, der er indstillet til 'sand' under **Commerce-parametre > Konfigurationsparametre**. 
![Konfigurationsparametre for cloud-baseret søgning.](./media/CloudPoweredSearchConfigurationParameters.png)

>Hvis du vil bruge avancerede sorteringsindstillinger som f.eks. nye, mest sælgende og mest populære, skal du aktivere [Produktanbefalinger](product-recommendations.md) for dit miljø. Avancerede sorteringsindstillinger er tilgængelige med Commerce SDK version 9.35+ og Commerce version 10.0.20.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over skybaseret søgning](cloud-powered-search-overview.md)

[Oversigt over startside](quick-tour-home-page.md)

[Oversigt over sider med produktdetaljer](quick-tour-pdp.md)

[Oversigt over sider til indkøbsvogn og betaling ved kassen](quick-tour-cart-checkout.md)

[Oversigt over sider til kontostyring](quick-tour-account-management.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
