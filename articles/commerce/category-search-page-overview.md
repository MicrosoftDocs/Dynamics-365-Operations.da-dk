---
title: Oversigt over standardlandingsside for kategori og side for søgeresultater
description: Dette emne indeholder en oversigt over standardlandingsside for kategori og side for søgeresultater i Dynamics 365 Commerce.
author: ashishmsft
manager: annbe
ms.date: 06/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 2a7eab8e7f5d300930f8a093afff2d848d8a2db7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4997841"
---
# <a name="default-category-landing-page-and-search-results-page-overview"></a>Oversigt over standardlandingsside for kategori og side for søgeresultater

[!include [banner](includes/banner.md)]

Dette emne indeholder en oversigt over standardlandingssiden for kategorier og søgeresultatsiden for e-handel i Microsoft Dynamics 365 Commerce.

## <a name="default-category-landing-page"></a>Standardlandingsside for kategorier

Standardlandingssiden for kategorier er den side, som brugerne af et websted typisk får vist, når de vælger en kategori i navigationshierarkiet. Du kan gennemse kategorisiden, og du kan også sortere og finpudse de kategoriserede produkter.

![Standardlandingsside for kategorier](./media/SimpleCategoryLandingDressCategory.png)

Øverst på siden findes et sidehoved, der viser alle produktkategorierne og andre sider, som produktchefen har kategoriseret. Konfigurationen udføres som en del af konfigurationen af kanalnavigationshierarkiet. Nederst på startsiden findes en sidefod med hurtige links til forskellige emner, som kan have interesse for kunderne.

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

- **Sideinddeling** lader de besøgende på webstedet flytte fra én side med kategoriserede produktresultater til en anden side.
- **Samlet antal** viser det samlede antal produkter, der er defineret i en kategori.

## <a name="enrich-a-category-landing-page"></a>Forbedre en kategorilandingsside

Hvis du ønsker, at en landingsside for en kategori skal have en mere skræddersyet oplevelse for en bestemt kategori, kan du "forbedre" kategorilandingssiden for den pågældende kategori. Du kan f.eks. tilføje en marketingvideo og fortælle om kategorien for at få kundernes opmærksomhed. Du kan finde flere oplysninger under [Forbedre en kategorilandingsside](enrich-category-page.md).

![Forbedre en kategorilandingsside](./media/CategoryLandingPages.png)

## <a name="auto-suggest-and-search-results-pages"></a>Sider med automatiske forslag og søgeresultater

Brugere af websteder kan udforske et websted ved enten at gå til en kategori fra navigationshierarkiet eller ved at angive et søgeord i søgefeltet.

Så snart brugerne går i gang med at skrive i søgefeltet, oplever de den avancerede funktion til automatiske forslag, der foreslår søgeord.

Her er nogle af de typer forslag, der kan vises:

- **Nøgleord** bruges til at finde produkter på tværs af alle produkter, der er udvalgt til kanalen.
- **Produkter** giver direkte links til siden med produktdetaljer.
- **Søgeforslag for kategoriområde** viser forskellige kategorier og lader brugere søge efter nøgleordet i en bestemt kategori.

![Avancerede automatiske forslag](./media/ImmersiveAutoSuggestUX.png)

Når brugerne vælger et af søgeforslagene for nøgleord eller områdekategori, eller når der ikke er nogen forslag til det søgeord, de angiver, omdirigeres de til en side med søgeresultater. Brugerne kan derefter gennemse, sortere og finjustere listen over søgeresultater for at finde det ønskede produkt.

![Landingsside for søgeresultater](./media/SearchLanding.png)

Følgende komponenter er vigtige for en søgeresultatside:

- **Produktplaceringsfelter** viser produkterne til brugerens søgning. Disse felter sorteres som standard af det skybaserede søgerelevansresultat for brugersøgningen.
- **Oversigt over afgrænsere og valg** er filtre, der viser antal, og som kan bruges til at afgrænse elementer. Produktchefen konfigurerer dem som en del af konfigurationen af metadataene for "kanalkategorier og produktattributter".
- **Sorteringsindstillinger** bruges af besøgende på webstedet til at sortere produkterne. Følgende sorteringsindstillinger er som standard tilgængelige:

    - Pris – lav til høj
    - Pris – høj til lav
    - Produktnavn – \[A-Z\]
    - Produktnavn – \[Z-A\]
    - Vurderinger – lav til høj
    - Vurderinger – høj til lav
    - Standard

- **Sideinddeling** lader de besøgende på webstedet flytte fra én side med kategoriserede produktresultater til en anden side.
- **Samlet antal** viser det samlede antal produkter, der er defineret i en kategori, og som opfylder søgekriterierne.

>[!NOTE]
>Disse cloud-aktiverede søgemuligheder er tilgængelige fra og med version 10.0.8. Kontroller, at der er en post for "ProductSearch.UseAzureSearch, der er indstillet til 'sand' under **Commerce-parametre > Konfigurationsparametre**. 
![Konfigurationsparametre for cloud-baseret søgning](./media/CloudPoweredSearchConfigurationParameters.png)

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over skybaseret søgning](cloud-powered-search-overview.md)

[Oversigt over startside](quick-tour-home-page.md)

[Oversigt over sider med produktdetaljer](quick-tour-pdp.md)

[Oversigt over sider til indkøbsvogn og betaling ved kassen](quick-tour-cart-checkout.md)

[Oversigt over sider til kontostyring](quick-tour-account-management.md)

