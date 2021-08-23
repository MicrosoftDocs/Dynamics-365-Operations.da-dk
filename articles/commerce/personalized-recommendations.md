---
title: Aktivere personlige produktanbefalinger
description: Dette emne beskriver, hvordan du stiller personligt tilpassede produktanbefalinger til rådighed for kunder i Microsoft Dynamics 365 Commerce.
author: bebeale
ms.date: 08/18/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 74bf2c96d744b8101151be9288a956d46ce3b6885f0cb593dc1b78728b018fb4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6770951"
---
# <a name="enable-personalized-recommendations"></a>Aktivere tilpassede anbefalinger

[!include [banner](includes/banner.md)]

Dette emne beskriver, hvordan du stiller personligt tilpassede produktanbefalinger til rådighed for kunder i Microsoft Dynamics 365 Commerce.

I Dynamics 365 Commerce kan detailhandlere gøre personligt tilpassede produktanbefalinger tilgængelige. På denne måde kan personlige anbefalinger indarbejdes i kundeoplevelsen online og på salgsstedet (POS). Når tilpasningsfunktionen er slået til, kan systemet tilknytte en brugers købs- og produktoplysninger for at generere individuelle produktanbefalinger.

## <a name="personalization-prerequisites"></a>Forudsætninger for personlig tilpasning

Før du stiller personlige produktanbefalinger til rådighed for kunderne, skal du bemærke, at produktanbefalinger kun understøttes af Commerce-brugere, der har overflyttet deres lager til Azure Data Lake Storage. Før kunder kan modtage personlige produktanbefalinger, skal forhandlerne [aktivere produktanbefalinger](enable-product-recommendations.md).

> [!NOTE]
> Når du aktiverer produktanbefalinger, kan du også aktivere personlig tilpasning. Men hvis du deaktiverer personlig tilpasning, slår du ikke andre typer produktanbefalinger fra.

Yderligere oplysninger om produktanbefalinger finder du under [Oversigt over produktanbefalinger](product-recommendations.md).

## <a name="turn-on-personalization"></a>Aktivere personlig tilpasning

Udfør følgende trin for at aktivere personlig tilpasning.

1. Søg efter **Funktionsstyring** i Commerce Headquarters.
1. Vælg **Alle** for at få vist en liste over tilgængelige funktioner. 
1. Skriv **Anbefalinger** i søgefeltet.
1. Vælg funktionen **Tilpassede produktanbefalinger**.
1. Vælg **Aktivér nu** i ruden med egenskaber for **Tilpassede produktanbefalinger**.

![Aktivere tilpasning.](./media/FeatureManagement_Personalized.PNG)

> [!NOTE]
> Når du aktiverer personlig tilpasning, startes processen til generering af lister over tilpassede produktanbefalinger. Der kan gå op til en dag, før disse lister er tilgængelige og synlige online og på POS.

## <a name="personalized-lists"></a>Personligt tilpassede lister

Udover at tillade personlig tilpasning af eksisterende maskingenererede lister giver anbefalingstjenesten mulighed for at tilpasse produktregistreringsoplevelsen både online og på POS.

Når tilpasning er slået til, kan detailhandlere vise kunderne personlige "Udvalgt til dig"-lister online eller "Anbefalet til kunde"-lister på POS-klienter. Desuden kan detailhandlere anvende personlig tilpasning på eksisterende produktanbefalingslister og levere GDPR-baseret framelding (generel forordning om databeskyttelse) til godkendte brugere. Hvis du deaktiverer personlig tilpasning, deaktiverer du også disse funktioner.

### <a name="online-picks-for-you-lists"></a>Online "Udvalgt til dig"-lister

Listen "Udvalgt til dig" er en kunstig intelligens-baseret maskinel læring (AI-ML), der viser en godkendt bruger en tilpasset liste over foreslåede produkter. Denne liste er baseret på brugerens omnikanal-indkøbshistorik. Personlige anbefalinger opdateres dynamisk, efterhånden som brugeren foretager flere køb. Denne type liste understøtter også filtrering af kategorier, så detailhandlere kan vise de bedste udvalg baseret på navigationshierarkier.

Før listen "Udvalgt til dig" kan vises på en e-handelsside, skal følgende brugerkrav være opfyldt:

- Brugere skal være logget på. Anonyme brugere kan ikke se personligt tilpassede anbefalinger.
- Brugere skal have mindst ét indkøb på deres konto.
- Brugerne skal være tilmeldt for at modtage personlige anbefalinger.

I følgende illustration vises et eksempel på en liste over "Udvalgt til dig" på en onlinebutiksside.

![Udvalgt til dig-onlineliste.](./media/picksforyou.png)

### <a name="recommended-for-customer-lists-at-the-pos"></a>Listerne "Anbefalet til kunde" på POS

For at forbedre deres kundeaktiviteter kan detailhandlere personligt tilpasse eksisterende kundedetaljesider ved at tilføje en kontekstafhængig "Anbefalet til kunde"-liste.

I følgende illustration vises et eksempel på en liste over "Anbefalet til kunde" på en POS-klient.

![Listen Anbefalet til kunde på POS.](./media/picksonpos.png)

## <a name="apply-personalization-to-existing-recommendation-lists"></a>Anvende personlige tilpasninger på eksisterende anbefalingslister

Detailhandlere kan anvende personlige tilpasninger på eksisterende anbefalingslister, f.eks. "Nyhed", "Mest populære", "Mest solgte", "Folk kan også godt lide" og "Ofte købt sammen". Når personlig tilpasning anvendes på eksisterende lister, fjernes de varer, som en bruger har købt tidligere, fra listerne. For både anonyme brugere og brugere, der har fravalgt at modtage personlige anbefalinger, vises standardversioner af de eksisterende lister. Derfor behøver detailhandlerne ikke at vedligeholde særskilte sideoplevelser manuelt.

En bruger, der er logget på, har f.eks. allerede købt det sorte ur og de brune arbejdsstøvler, der vises på listen "Trending - default" på følgende illustration. Brugeren får derfor vist nye produkter i stedet for disse produkter, som vist på listen "Trending - personalized".

![Anvende personlig tilpasning.](./media/applypersonalization.png)

Hvis du vil anvende tilpasning på en eksisterende anbefalingsliste i Commerce-webstedsgeneratoren, skal du følge disse trin.

1. Åbn en eksisterende side med webstedsgeneratoren, der indeholder et modul til produktsamling.
1. Vælg produktsamlingsmodulet i navigationsruden til venstre.
1. Vælg listen under **Produkter** i navigationsruden til højre.
1. Vælg listetypen under **Type** i dialogboksen **Vælg produktlistekonfiguration**.
1. Markér afkrydsningsfeltet **Anvend personlig tilpasning**, og vælg derefter **OK**.

    ![Anvende personlig tilpasning på en tendensliste.](./media/ApplyPersonalizationToTrending.PNG)

1. Gem siden, afslut redigeringen af den, og publicer den. Når siden er publiceret, vil de brugere, der er logget på, se en personligt tilpasset tendensliste.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over produktanbefalinger](product-recommendations.md)

[Aktivér Azure Data Lake Storage i et Dynamics 365 Commerce-miljø](enable-adls-environment.md)

[Aktivér produktanbefalinger](enable-product-recommendations.md)

[Aktivere anbefalinger af "Køb tilsvarende"](shop-similar-looks.md)

[Fravælge tilpassede anbefalinger](personalization-gdpr.md)

[Tilføje produktanbefalinger på POS](product.md)

[Føje anbefalinger til transaktionsskærmen](add-recommendations-control-pos-screen.md)

[Justere resultater for AI-ML-anbefalinger](modify-product-recommendation-results.md)

[Oprette overvågede anbefalinger manuelt](create-editorial-recommendation-lists.md)

[Oprette anbefalinger med demonstrationsdata](product-recommendations-demo-data.md)

[Ofte stillede spørgsmål om produktanbefalinger](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
