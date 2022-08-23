---
title: Oversigt over skybaseret søgning
description: Denne artikel indeholder en oversigt over skybaseret søgning i Microsoft Dynamics 365 Commerce.
author: ashishmsft
ms.date: 02/28/2022
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
ms.openlocfilehash: ed80ff42ea5c6e6a904ea2855953d006f66aad37
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273660"
---
# <a name="cloud-powered-search-overview"></a>Oversigt over skybaseret søgning

[!include [banner](includes/banner.md)]

Denne artikel indeholder en oversigt over skybaseret søgning i Microsoft Dynamics 365 Commerce.

Produktregistrering hjælper dig med at sikre, at kunder hurtigt og nemt kan finde produkter ved at gennemse kategorier, foretage søgninger og filtrere. Detailhandlende vurderer, at produktregistrering er et primært værktøj for kundeinteraktion på tværs af kanaler, der drives af Cloud Scale Unit (CSU), f.eks. e-handel og POS.

Kunder er vant til de næsten øjeblikkelige svartider fra websøgemaskiner, sofistikerede e-handelswebsteder, sociale apps, automatiske forslag, der vises, når de skriver søgeord, filterbaseret navigation og fremhævning. Hvis kunderne ikke hurtigt kan finde det produkt, som de leder efter, i én e-handelsbutik, går de straks videre til en anden e-handelsbutik.

Den skybaserede produktregistrering i Commerce hjælper detailhandlerne med at holde på kunderne og øge omregningskurserne på tværs af alle kanaler, der er styret af CSU.

Søgeoplevelsen i Commerce har forbedrede muligheder, som kan hjælpe forhandlerne med at opnå en bedre produktregistrering. Samtidig leverer disse funktioner den skalerbarhed og ydeevne, der kræves til e-handelstrafik.

## <a name="browse-and-search"></a>Gennemsyn og søgning

Søgerelevansen og ydeevnen er nøglefaktorer i omnikanaloplevelsen, da produktregistrering primært er baseret på søgefunktionalitet til hentning af oplysninger og indholdsnavigation. Effektivt gennemsyn og søgning er med til at øge konverteringen.

I følgende illustration vises et eksempel på typiske gennemsyns- og søgefunktioner.

![Landingsside for søgninger.](./media/SearchLanding.png)

## <a name="faceted-navigation-and-choice-summary"></a>Filterbaseret navigation og oversigt over valg 

Filterbaseret navigation gør det lettere for kunderne at søge efter indhold ved at lade dem filtrere på afgrænsere, der er sammenkædet med ord i et ordsæt. Når en kunde har valgt og anvendt afgrænsere, vises en oversigt over valgmulighederne. 

Ved at bruge filterbaseret navigation kan du konfigurere forskellige afgrænsere for forskellige ord i et ordsæt uden at skulle oprette yderligere sider. 

I følgende illustration vises et eksempel, hvor der bruges filterbaseret navigation i en søgning.

![Oversigt over valgmuligheder.](./media/ChoiceSummary.png)

## <a name="immersive-autosuggest"></a>Avancerede automatiske forslag

Den aktuelle funktion til automatiske forslag viser nøgleord, der udløser en søgning efter det tilsvarende nøgleord. På grund af nye forbedringer i Commerce kan kunder ofte finde links til produkter, før de er færdige med at skrive.

Commerce understøtter også funktioner for nøgleordsforekomster i forskellige kategorier. Med denne funktion kan kunderne se antallet af nøgleord, der passer på tværs af kategorier, og udløse en søgning efter et nøgleord i andre kategorier.

I følgende illustration vises et eksempel, hvor der bruges avancerede automatiske forslag.

![avancerede automatiske forslag.](./media/ImmersiveAutoSuggestUX.png)

## <a name="sort"></a>Sortér

Med sortering kan kunderne sortere, søge efter og gennemse kategoriresultater og begrænse dem efter kriterier som f.eks. pris, produktnavn og produktnummer. Hvis du aktiverer [Produktanbefalinger](product-recommendations.md) i dit miljø, kan kunder også sortere resultater ud fra avancerede sorteringskriterier som f.eks. nye, mest sælgende og mest populære.


> [!NOTE]
> Disse cloud-aktiverede søgemuligheder er tilgængelige fra og med version 10.0.8. Kontrollér, at der er en post for "ProductSearch.UseAzureSearch", der er indstillet til 'true' i **Commerce-parametre > Konfigurationsparametre**. 
![Konfigurationsparametre for cloud-baseret søgning.](./media/CloudPoweredSearchConfigurationParameters.png)
>Der findes avancerede sorteringsindstillinger som f.eks. nye, mest sælgende og mest populære i Commerce SSK version 9.35+ og Dynamics 365 Commerce 10.0.20 release.  


## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over standardlandingsside for kategori og side for søgeresultater](category-search-page-overview.md)

[Administrere SEO-metadata](manage-seo-metadata.md)


[!INCLUDE [footer-include](../includes/footer-banner.md)]
