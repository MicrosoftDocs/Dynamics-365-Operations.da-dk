---
title: Redigere en eksisterende webstedsside
description: Dette emne indeholder en beskrivelse af, hvordan du kan redigere en eksisterende webstedsside i Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 10/01/2019
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
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 50373d3681e269bf6164b2a425bbafebdd93d64f
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945691"
---
# <a name="modify-an-existing-site-page"></a>Redigere en eksisterende webstedsside

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dette emne indeholder en beskrivelse af, hvordan du kan redigere en eksisterende webstedsside i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Når du skal redigere en side, skal du først åbne den i sideeditoren. Gå til det websted, der indeholder siden, og søg derefter efter den ønskede side på listen over sider. Hvis du ikke kan finde siden, kan du bruge funktionen til avanceret søgning i oprettelsesværktøjet. Skriv enten det præcise sidenavn, eller skriv de første par bogstaver i navnet og derefter en stjerne (\*). Der vises en filtreret liste over sider. Du kan bruge denne liste til at finde den ønskede side. Når du har fundet siden, skal du vælge sidenavnet for at åbne siden i sideeditoren.

> [!TIP]
> Hvis siden er synlig i sidefremviseren, kan du vælge den og checke den ud, før du åbner den i sideeditoren. På denne måde kan du checke flere sider ud på samme tid.

Når siden er åben i sideeditoren, skal du sørge for, at den er checket ud til dig. Kommandolinjen i oprettelsesværktøjet er dynamisk, kontekstafhængig og tilstandsfølsom. Derfor viser den kun de handlinger, du i øjeblikket kan udføre på siden. Hvis siden f.eks. ikke er checket ud til dig, vises knapperne **Gem** og **Check ind** ikke på kommandolinjen. Sidetilstanden vises også i højre side af vinduet.

Hvis siden ikke allerede er checket ud til dig, skal du vælge **Check ud** på kommandolinjen. Kommandolinjen ændres, så den afspejler sidens nye tilstand. Du modtager også en besked om, at siden blev checket ud til dig.

Det næste trin er at foretage de faktiske ændringer. Du skal ofte bruge sidens dispositionstræ til venstre for at finde og vælge det modul, du vil ændre, og derefter foretage ændringer i egenskabsruden til højre. 

Men ændringen kan undertiden omfatte tilføjelse eller fjernelse af modeller eller fragmenter. Hvis du vil tilføje et fragment eller et modul, skal du bruge sidens dispositionstræ til at finde den plads, hvor du vil tilføje modulet eller fragmentet og derefter vælge ellipseknappen (**...**) for den pågældende plads. Der vises en menu, der indeholder kommandoer til tilføjelse af et modul eller fragment. Hvis du vil fjerne et modul eller fragment, skal du finde og markere det i sidedispositionstræet, vælge ellipseknappen og derefter vælge den kommando, der sletter modulet eller fragmentet.

> [!TIP]
> Du kan også få vist og redigere egenskaberne for et modul, der er synligt i forhåndsvisningen "what you see is what you get" (WYSIWYG), ved at vælge det direkte.

Når du er færdig med at foretage ændringer og få vist deres effekt, skal du checke siden ind ved at vælge **Check ind** på kommandolinjen. 

Vælg **Publicer** på kommandolinjen for at publicere dine ændringer med det samme. Den senest indcheckede version af den side, du har ændret, publiceres og bliver tilgængelig for eksterne brugere, der går ind dit websted. 

## <a name="example-change-the-video-on-the-home-page"></a>Eksempel: Ændre videoen på startsiden

I følgende eksempel vises, hvordan du kan ændre startsiden ved at ændre den video, der vises i videoafspillermodulet.

1. Vælg **Fabrikam** (eller navnet på dit websted) under **Websteder**.
1. Vælg **Sider** i navigationsruden til venstre.
1. Find og vælg startsiden for at åbne den i sideeditoren.
1. Vælg **Check ud** på kommandolinjen.
1. Vælg **Hoved**-pladsen i sidedispositionen.
1. Udvid alle flydende containermoduler under **Hoved**-pladsen.
1. Find og vælg videoafspillermodulet.
1. Vælg egenskaben **Video** i egenskabsruden til højre. Aktivvælgeren vises.
1. Vælg et tilgængeligt videoaktiv i aktivvælgeren, eller vælg **Upload nyt aktiv** for at overføre et nyt videoaktiv.
1. Vælg **OK**.
1. Vælg **Gem**, og vælg derefter **Tjek ind**.
1. Angiv **Ændrede videoen** i feltet **Kommentarer**, og vælg derefter **OK**.
1. Vælg **Eksempel** for at få vist den opdaterede side. Når du er færdig, skal du lukke eksempelfanen for at vende tilbage til oprettelsesværktøjet.
1. Vælg **Publicer**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Tilføje en ny webstedsside](add-new-page.md)

[Vælge sidelayout](select-page-layouts.md)

[Administrere SEO-metadata](manage-seo-metadata.md)

[Gemme, få vist og udgive en side](save-preview-publish-page.md)

[Forbedre en produktside](enrich-product-page.md)

[Forbedre en kategorilandingsside](enrich-category-page.md)

[Bekræft tilgængelighed af sideindhold](verify-accessibility.md)
