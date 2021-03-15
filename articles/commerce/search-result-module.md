---
title: Modul til søgeresultater
description: Dette emne omhandler søgeresultater-moduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3761be29955458099d01f2271057884fc1fd6f28
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2021
ms.locfileid: "5097172"
---
# <a name="search-results-module"></a>Modul til søgeresultater

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Dette emne omhandler søgeresultater-moduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.

I modulet med søgeresultater returneres resultaterne af produktsøgningen og en liste over relevante forfinere for produkterne. Du kan bruge Dynamics 365 Commerce-søgeresultatmoduler på websteder til at vise sider i følgende scenarier:

- Søgeresultater, der er startet af en brugersøgning
- Søgeresultater, der viser et bestemt sæt produkter, f.eks. "Køb tilsvarende"
- Lister over produkter, der tilhører en given kategori

Yderligere oplysninger om arts- og søgeresultatsider finder du i [oversigtsoversigten over Standardkategorilandingsside og søgeresultater](category-search-page-overview.md).

I følgende illustration vises et eksempel på et søge resultater-side for kategori på Fabrikam-webstedet.

![Eksempel på en søgeresultatside på Fabrikam-webstedet](./media/SimpleCategoryLandingDressCategory.png)

## <a name="search-results-module-properties"></a>Modulegenskaber til søgeresultater

Følgende tabel indeholder egenskaberne for søgeresultatmoduler sammen med deres værdier og beskrivelser.

| Egenskab | Værdier | Betegnelse |
|----------|--------|-------------|
| Elementer pr. side | Heltal | Det antal elementer, der skal vises på hver side. |
| Tillad at gå tilbage til PDP | **Sand** eller **Falsk** | Hvis denne egenskab er angivet til **Sand**, når en bruger vælger et produkt på siden med søgeresultater, vil den navigation på produktdetaljerne (PDP), der åbnes, vise linket "Tilbage til resultater". |
| Udvid afgrænsninger | **Alle**, **1**, **2**, **3** eller **4** | Det antal af de øverste afgrænsningerne, der skal udvides, når en side indlæses. Hvis denne egenskab f.eks. er angivet til **3**, udvides de første tre afgrænsninger på siden. |
| Skjul visning af kategorihierarki | **Sand** eller **Falsk** | Hvis denne egenskab er angivet til **Sand**, vil visningen af kategorihierarkiet på siden være skjult. Denne egenskab skal angives til **Sand**, hvis du bruger [modulet brødkrumme](add-breadcrumb.md) til at få vist kategorihierarkiet.|
| Inkluder produktattributter i søgeresultater | **Sand** eller **Falsk** | Hvis denne egenskab er angivet til **Sand**, returneres attributter for produkterne i søgeresultaterne. Selvom disse attributter kan vises på et handelswebsted, skal der angives en filtype.|
| Vis tilknytningspriser | **Sand** eller **Falsk** | Hvis denne egenskab er angivet til **Sand**, vises tilknytningspriserne for produkter i søgeresultaterne, når en bruger, der er logget på, gennemser siden. |

> [!IMPORTANT]
> I versionen Dynamics 365 Commerce 10.0.16 og senere kan konfigurationen **Vis tilknytningspriser** bruges til at vise tilknytningspriser på siden.

## <a name="supported-modules"></a>Understøttede moduler

Modulet søgeresultater understøtter [modulet Hurtig visning](quick-view-module.md), som giver brugerne mulighed for at få vist produktoplysninger og føje varer til indkøbsvognen fra en søgeresultater-side.

## <a name="add-a-search-results-module-to-a-category-page"></a>Føje et modul med søgeresultater til en kategoriside

Hvis du vil tilføje et søgeresultater-modul til en kategoriside, skal du følge disse trin.

1. Gå til **Skabeloner**, og vælg **Ny** for at oprette en ny skabelon.
1. Angiv **Nu skabelon** i dialogboksen, angiv navnet **Søgeresultater**, og vælg derefter **OK**.
1. På pladsen **Brødtekst** skal du vælge ellipsen (...) og derefter **Tilføj modul**.
1. dI dialogboksen **Tilføj modul** skal du vælge modulet **Standardside** og derefter **OK**.
1. På pladsen **Hoved** i modulet **Standardside** skal du vælge ellipsen (...) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Container** og derefter **OK**.
1. På pladsen **Container** skal du vælge ellipsen (...) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Brødkrumme** og derefter **OK**.
1. Angiv værdien **1** for **Min. indtræffer** i ruden **Brødkrumme**-egenskaber.
1. På pladsen **Container** skal du vælge ellipsen (...) og derefter **Tilføj modul**.
1. I dialogboksen **Tilføj modul** skal du vælge modulet **Søgeresultater** og derefter **OK**.
1. I ruden **Søgeresultater**-egenskaber skal du angive værdien **1** for **Min. indtræffer**, og derefter angive eventuelle andre nødvendige egenskaber for søgeresultaterne. Når du angiver disse egenskaber i skabelonen, sikrer du, at eventuelle tilpasninger af en bestemt kategoriside automatisk medtager disse indstillinger.
1. Vælg **Afslut redigering**, og vælg derefter **Publicer** for at publicere skabelonen.
1. Gå til **Sider**, og vælg **Ny** for at oprette en ny side.
1. I dialogboksen **Vælg en skabelon** skal du vælge den **Søgeresultater**-skabelon, du har oprettet, angive **Kategoriside** for **Sidenavn** og vælge **OK**. Da alle værdier er angivet i skabelonen, er siden klar til at blive publiceret.
1. Vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over standardlandingsside for kategori og side for søgeresultater](category-search-page-overview.md)

[Modulbibliotek, oversigt](starter-kit-overview.md)

[Hurtig visning-.modul](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]