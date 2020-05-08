---
title: Tilpasse navigation på webstedet
description: I dette emne beskrives, hvordan du opretter et tilpasset onlinenavigationshierarki for at organisere dine produkter til gennemsyn på dit Microsoft Dynamics 365 Commerce-websted.
author: bicyclingfool
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ae7696dcb5cdd99cd46b89ed1de1b03c16146e2d
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269653"
---
# <a name="customize-site-navigation"></a>Tilpasse navigation på webstedet


[!include [banner](includes/banner.md)]

I dette emne beskrives, hvordan du opretter et tilpasset onlinenavigationshierarki for at organisere dine produkter til gennemsyn på dit Microsoft Dynamics 365 Commerce-websted.

## <a name="overview"></a>Oversigt

Onlinestorefronts giver typisk kunderne mulighed for at finde og gennemse produkter ved at navigere gennem produktkategorier. Denne egenskab leveres normalt af faner øverst på siden eller af en navigationslinje i venstre side. I Dynamics 365 Commerce kan du oprette og administrere hierarkistrukturen i kategorinavigationen og de produkter, der er inkluderet i de forskellige kategorier.

## <a name="create-a-channel-navigation-hierarchy"></a>Opret et navigationshierarki for kanal

Benyt følgende fremgangsmåde for at oprette et navigationshierarki for en kanal.

1. Gå til **Retail og Commerce \> Produkter og kategorier \> Kategori og produktstyring**.
1. Vælg **Kategorihierarkier**, og vælg derefter **Ny**.
1. Giv hierarkiet et navn.

    > [!NOTE]
    > Den øverste kategori, du opretter, er rodnoden for kategorien. Den vises ikke på webstedet. Hvis du vil oprette et kategorihierarki, hvor der vises en enkelt node på øverste niveau på webstedet, skal du oprette og navngive kategorien som underordnet i rodkategorien.

1. Vælg **Ny kategorinode**, og navngiv kategorien.
1. Fortsæt med at oprette sideordnede og underordnede kategorier efter behov.

Du kan nu tildele produkter til hver kategori, som du oprettede under kategorien på øverste niveau.

## <a name="customize-the-order-of-categories"></a>Tilpasse rækkefølgen af kategorier

De kategorier, du definerer, vises som standard i alfabetisk rækkefølge på dit websted. Du kan dog også tilpasse visningsrækkefølgen for kategorier.

## <a name="assign-a-category-hierarchy-type"></a>Tildele en kategorihierarkitype

1. Gå til **Retail og Commerce \> Produkter og kategorier \> Kategori og produktstyring**.
1. Vælg **Kategorihierarkier**.
1. Vælg **Tilknyt hierarkitype** i gruppen **Konfigurer** under fanen **Kategorihierarki** i handlingsruden.
1. Vælg **Ny**.
1. Vælg **Navigationshierarki for kanal** i feltet **Kategori for hierarkitype**.
1. I feltet **Kategorihierarki** skal du vælge det kanalnavigationshierarki, du har oprettet tidligere.

## <a name="publish-new-or-updated-navigation-hierarchies"></a>Publicere nye eller opdaterede navigationshierarkier

Udfør følgende trin for at gøre navigationshierarkiet tilgængeligt for din onlinestorefront.

1. Gå til **Retail og Commerce \> Konfiguration af kanal \> Kanalkategorier og produktattributter**.
1. Vælg din onlinebutik i træet til venstre.
1. Vælg **Publicer kanalopdateringer**.
1. Gå til **Retail og Commerce \> Retail og Commerce IT \> Distributionsplan**.
1. Find og vælg **Job 1040** på listen.
1. Vælg **Kør nu**.
1. Gentag trin 5 og 6 for job 1070 og 1150.

## <a name="show-categories-on-your-site"></a>Vise kategorier på dit websted

Hvis du vil have vist din kategorihierarki i din onlinestorefront, skal du tilføje navigationsmenumodulet på den relevante placering i en skabelon eller et fragment. Navigationsmenumodulet viser derefter dit navigationshierarki, hvis du har publiceret dit navigationshierarki til den kanal, som dit websted er bundet til.

> [!NOTE]
> Det navigationsmenumodul, der er inkluderet i butikkens startpakke, gør det kun muligt for brugere at navigere til kategorier, der ikke har underkategorier. Hvis kunderne skal kunne navigere til kategorier, der har underkategorier, skal du tilpasse navigationsmenumodulet.

## <a name="add-custom-navigation-options"></a>Tilføje brugerdefinerede navigationsindstillinger

I navigationsmenuen kan du tilføje navigationsindstillinger, der ikke er en del af dit produktkategorihierarki. I slutningen af listen over produktkategorier kan du f.eks. tilføje et **Kontakt os**-element, der peger på en kontaktside, du har bygget til webstedet.

Hvis du vil føje brugerdefinerede navigationsindstillinger til navigationsmenuen, skal du følge disse trin.

1. Vælg navigationsmenumodulet i den skabelon eller det fragment, du vil tilpasse.
1. Vælg **Tilføj element** under fanen **Data** i egenskabsruden for at oprette et nyt (CMS)-navigationselement i indholdsstyringssystemet.
1. Indtast linktekst og en URL-adresse.
1. Gentag trin 2 og 3 for at tilføje flere brugerdefinerede navigationsindstillinger.
1. Når du er færdig, skal du vælge **Gem** for at gemme skabelonen eller fragmentet og derefter vælge **Afslut redigering** for at tjekke den ind.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over skabeloner og layout](templates-layouts-overview.md)

[Arbejde med skabeloner](work-with-templates.md)

[Arbejde med forudindstillede layout](work-with-layouts.md)

[Arbejde med fragmenter](work-with-fragments.md)

[Arbejde med moduler](work-with-modules.md)

[Oprette en side-URL](create-page-url.md)

[Arbejd med publiceringsgrupper](publish-groups.md)
