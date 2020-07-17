---
title: Oversigt over skybaseret søgning
description: Dette emne indeholder en oversigt over skybaseret søgning i Microsoft Dynamics 365 Commerce.
author: ashishmsft
manager: annbe
ms.date: 06/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 00a3de2515cea341f7529b8cb6cb2caae5e33d22
ms.sourcegitcommit: ce397c2759f642c595e30fef58a770b50360b2bd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/01/2020
ms.locfileid: "3527437"
---
# <a name="cloud-powered-search-overview"></a>Oversigt over skybaseret søgning


[!include [banner](includes/banner.md)]

Dette emne indeholder en oversigt over skybaseret søgning i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Produktregistrering hjælper dig med at sikre, at kunder hurtigt og nemt kan finde produkter ved at gennemse kategorier, foretage søgninger og filtrere. Detailhandlere regner produktopdagelse for et primært værktøj til kundeinteraktion på tværs af alle kanaler.

Kunder er vant til de næsten øjeblikkelige svartider fra websøgemaskiner, sofistikerede e-handelswebsteder, sociale apps, automatiske forslag, der vises, når de skriver søgeord, filterbaseret navigation og fremhævning. Hvis kunderne ikke kan finde det produkt, som de leder efter hurtigt nok i én e-handelsbutik, går de straks videre til en anden e-handelsbutik.

Den skybaserede produktregistrering i Dynamics 365 Commerce hjælper detailhandlerne med at holde på kunderne og øge omregningskurserne på tværs af alle kanaler, både e-handelskanaler og POS-kanaler.

Søgeoplevelsen i Dynamics 365 Commerce har forbedrede muligheder, som kan hjælpe forhandlerne med at opnå en bedre produktregistrering. Samtidig leverer disse funktioner den skalerbarhed og ydeevne, der kræves til e-handelstrafik.

## <a name="browse-and-search"></a>Gennemsyn og søgning

Søgerelevansen og ydeevnen er nøglefaktorer i omnikanaloplevelsen, da produktregistrering primært er baseret på søgefunktionalitet til hentning af oplysninger og indholdsnavigation. Effektivt gennemsyn og søgning er med til at øge konverteringen.

I følgende illustration vises et eksempel på typiske gennemsyns- og søgefunktioner.

![Landingsside for søgninger](./media/SearchLanding.png)

## <a name="faceted-navigation-and-choice-summary"></a>Filterbaseret navigation og oversigt over valg 

Filterbaseret navigation gør det lettere for kunderne at søge efter indhold ved at lade dem filtrere på afgrænsere, der er sammenkædet med ord i et ordsæt. Når en kunde har valgt og anvendt afgrænsere, vises en oversigt over valgmulighederne. 

Ved at bruge filterbaseret navigation kan du konfigurere forskellige afgrænsere for forskellige ord i et ordsæt uden at skulle oprette yderligere sider. 

I følgende illustration vises et eksempel, hvor der bruges filterbaseret navigation i en søgning.

![Oversigt over valgmuligheder](./media/ChoiceSummary.png)

## <a name="immersive-autosuggest"></a>Avancerede automatiske forslag

Den aktuelle funktion til automatiske forslag viser kun nøgleord, der udløser en søgning efter det tilsvarende nøgleord. På grund af nye forbedringer i Dynamics 365 Commerce kan kunder ofte finde links til produkter, før de er færdige med at skrive.

Dynamics 365 Commerce understøtter også funktioner for nøgleordsforekomster i forskellige kategorier. Med denne funktion kan kunderne se antallet af nøgleord, der passer på tværs af kategorier, og udløse en søgning efter et nøgleord i andre kategorier.

I følgende illustration vises et eksempel, hvor der bruges avancerede automatiske forslag.

![avancerede automatiske forslag](./media/ImmersiveAutoSuggestUX.png)

## <a name="sort"></a>Sortér

Med forbedret sortering i Dynamics 365 Commerce kan kunderne sortere, søge efter og gennemse søgeresultater og begrænse dem efter kriterier som f.eks. pris, produktnavn og produktnummer. Kunderne kan også sortere resultater, afhængigt af om et produkt er nyt, mest sælgende eller tilføjet for nylig.

>[!NOTE]
>Disse cloud-aktiverede søgemuligheder er tilgængelige fra og med version 10.0.8. Kontroller, at der er en post for "ProductSearch.UseAzureSearch, der er indstillet til 'sand' under **Commerce-parametre > Konfigurationsparametre**. 
![Konfigurationsparametre for cloud-baseret søgning](./media/CloudPoweredSearchConfigurationParameters.png)

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over standardlandingsside for kategori og side for søgeresultater](category-search-page-overview.md)

[Administrere SEO-metadata](manage-seo-metadata.md)
