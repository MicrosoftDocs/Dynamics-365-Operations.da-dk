---
title: Aktivere personlige produktanbefalinger
description: Dette emne beskriver, hvordan du stiller personligt tilpassede produktanbefalinger til rådighed for kunder i Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 01/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6b3c6140b8bd3ea15458223c0f61810421d0b2bc
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/04/2020
ms.locfileid: "3025235"
---
# <a name="enable-personalized-recommendations"></a>Aktivere personlige anbefalinger

[!include [banner](includes/banner.md)]

Dette emne beskriver, hvordan du stiller personligt tilpassede produktanbefalinger til rådighed for kunder i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

I Dynamics 365 Commerce kan detailhandlere gøre personligt tilpassede produktanbefalinger tilgængelige. På denne måde kan personlige anbefalinger indarbejdes i kundeoplevelsen online og på salgsstedet (POS). Når tilpasningsfunktionen er slået til, kan systemet tilknytte en brugers købs- og produktoplysninger for at generere individuelle produktanbefalinger.

## <a name="personalization-prerequisites"></a>Forudsætninger for personlig tilpasning

Før du stiller personlige produktanbefalinger til rådighed for kunderne, skal du bemærke, at produktanbefalinger kun understøttes af Commerce-brugere, der har overflyttet deres lager til Azure Data Lake Storage. Før kunder kan modtage personlige produktanbefalinger, skal forhandlerne [aktivere produktanbefalinger](enable-product-recommendations.md).

> [!NOTE]
> Når du aktiverer produktanbefalinger, kan du også aktivere personlig tilpasning. Men hvis du deaktiverer personlig tilpasning, slår du ikke andre typer produktanbefalinger fra.

Yderligere oplysninger om produktanbefalinger finder du under [Oversigt over produktanbefalinger](product-recommendations.md).

## <a name="turn-on-personalization"></a>Aktivere personlig tilpasning

Udfør følgende trin for at aktivere personlig tilpasning.

1. Gå til **Retail og Commerce \> Produktanbefalinger \> Anbefalingsparametre**.
1. Vælg **Anbefalingslister** på listen over delte Retail-parametre.
1. Angiv indstillingen **Aktivér tilpasning** til **Ja**.

![Aktivere tilpasning](./media/enablepersonalization.png)

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

![Online Udvalgt til dig-liste](./media/picksforyou.png)

### <a name="recommended-for-customer-lists-at-the-pos"></a>Listerne "Anbefalet til kunde" på POS

For at forbedre deres kundeaktiviteter kan detailhandlere personligt tilpasse eksisterende kundedetaljesider ved at tilføje en kontekstafhængig "Anbefalet til kunde"-liste.

I følgende illustration vises et eksempel på en liste over "Anbefalet til kunde" på en POS-klient.

![Listen Anbefalet til kunde på POS](./media/picksonpos.png)

## <a name="apply-personalization-to-existing-recommendation-lists"></a>Anvende personlige tilpasninger på eksisterende anbefalingslister

Detailhandlere kan anvende personlige tilpasninger på eksisterende anbefalingslister, f.eks. "Nyhed", "Mest populære", "Mest solgte", "Folk kan også godt lide" og "Ofte købt sammen". Når personlig tilpasning anvendes på eksisterende lister, fjernes de varer, som en bruger har købt tidligere, fra listerne. For både anonyme brugere og brugere, der har fravalgt at modtage personlige anbefalinger, vises standardversioner af de eksisterende lister. Derfor behøver detailhandlerne ikke at vedligeholde særskilte sideoplevelser manuelt.

En bruger, der er logget på, har f.eks. allerede købt det sorte ur og de brune arbejdsstøvler, der vises på listen "Trending - default" på følgende illustration. Brugeren får derfor vist nye produkter i stedet for disse produkter, som vist på listen "Trending - personalized".

![Anvende personlig tilpasning](./media/applypersonalization.png)

Hvis du vil anvende tilpasning på en eksisterende anbefalingsliste i Commerce-webstedsgeneratoren, skal du følge disse trin.

1. Åbn en eksisterende side med webstedsgeneratoren, der indeholder et modul til produktsamling.
1. Vælg produktsamlingsmodulet i navigationsruden til venstre.
1. Vælg listen under **Produkter** i navigationsruden til højre.
1. Vælg listetypen under **Type** i dialogboksen **Vælg produktlistekonfiguration**.
1. Markér afkrydsningsfeltet **Anvend personlig tilpasning**, og vælg derefter **OK**.

    ![Anvende personlig tilpasning på en tendensliste](./media/ApplyPersonalizationToTrending.PNG)

1. Gem siden, afslut redigeringen af den, og publicer den. Når siden er publiceret, vil de brugere, der er logget på, se en personligt tilpasset tendensliste.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over produktanbefalinger](product-recommendations.md)

[Aktivér produktanbefalinger](enable-product-recommendations.md)

[GDPR og produktanbefalinger](personalization-gdpr.md)

[Tilføje lister med produktanbefalinger på sider](add-reco-list-to-page.md)

[Føje anbefalingspanel til POS-enheder](add-recommendations-control-pos-screen.md)

[Oversigt over modulet Produktsamling](product-collection-module-overview.md)
