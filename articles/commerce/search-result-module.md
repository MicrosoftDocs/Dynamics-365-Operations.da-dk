---
title: Modul til søgeresultater
description: Denne artikel omhandler søgeresultater-moduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 08/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: eeb7cd0769fcb866a3d7dcc03e8e87daf24b2c5d
ms.sourcegitcommit: 1d5cebea3e05b6d758cd01225ae7f566e05698d2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/02/2022
ms.locfileid: "9405287"
---
# <a name="search-results-module"></a>Modul til søgeresultater

[!include [banner](includes/banner.md)]

Denne artikel omhandler søgeresultater-moduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.

I modulet med søgeresultater returneres resultaterne af produktsøgningen og en liste over relevante forfinere for produkterne. Du kan bruge Dynamics 365 Commerce-søgeresultatmoduler på websteder til at vise sider i følgende scenarier:

- Søgeresultater, der er startet af en brugersøgning
- Søgeresultater, der viser et bestemt sæt produkter, f.eks. "Køb tilsvarende"
- Lister over produkter, der tilhører en given kategori

Yderligere oplysninger om arts- og søgeresultatsider finder du i [oversigtsoversigten over Standardkategorilandingsside og søgeresultater](category-search-page-overview.md).

I følgende illustration vises et eksempel på et søge resultater-side for kategori på Fabrikam-webstedet.

![Eksempel på en søgeresultatside på Fabrikam-webstedet.](./media/SimpleCategoryLandingDressCategory.png)

## <a name="search-results-module-properties"></a>Modulegenskaber til søgeresultater

Følgende tabel indeholder egenskaberne for søgeresultatmoduler sammen med deres værdier og beskrivelser.

| Egenskab | Værdier | Beskrivelse |
|----------|--------|-------------|
| Elementer pr. side | Heltal | Det antal elementer, der skal vises på hver side. |
| Tillad at gå tilbage til PDP | **Sand** eller **Falsk** | Hvis denne egenskab er angivet til **Sand**, når en bruger vælger et produkt på siden med søgeresultater, vil den navigation på produktdetaljerne (PDP), der åbnes, vise linket "Tilbage til resultater". |
| Udvid afgrænsninger | **Alle**, **1**, **2**, **3** eller **4** | Det antal af de øverste afgrænsningerne, der skal udvides, når en side indlæses. Hvis denne egenskab f.eks. er angivet til **3**, udvides de første tre afgrænsninger på siden. |
| Skjul visning af kategorihierarki | **Sand** eller **Falsk** | Hvis denne egenskab er angivet til **Sand**, vil visningen af kategorihierarkiet på siden være skjult. Denne egenskab skal angives til **Sand**, hvis du bruger [modulet brødkrumme](add-breadcrumb.md) til at få vist kategorihierarkiet.|
| Inkluder produktattributter i søgeresultater | **Sand** eller **Falsk** | Hvis denne egenskab er angivet til **Sand**, returneres attributter for produkterne i søgeresultaterne. Selvom disse attributter kan vises på et handelswebsted, skal der angives en filtype.|
| Vis tilknytningspriser | **Sand** eller **Falsk** | Hvis denne egenskab er angivet til **Sand**, vises tilknytningspriserne for produkter i søgeresultaterne, når en bruger, der er logget på, gennemser siden. |
| Opdatere afgrænsningspanel | **Sand** eller **Falsk** | Hvis denne egenskab er angivet til **Sand**, opdateres afgrænsningspanelet, når afgrænsninger vælges. I denne tilstand opfører nogle afgrænsere med flere markeringer sig som afgrænsere med ét valg, når afgrænserpanelet opdateres. |

> [!IMPORTANT]
> I Commerce version 10.0.16 og senere kan konfigurationen **Vis tilknytningspriser** bruges til at vise tilknytningspriser på siden.
>
> I Commerce version 10.0.20 og nyere versioner kan konfigurationen **Opdater afgrænsningspanel** bruges til at opdatere afgrænsningspanelet under valg af afgrænser.

## <a name="supported-modules"></a>Understøttede moduler

Modulet søgeresultater understøtter [modulet Hurtig visning](quick-view-module.md), som giver brugerne mulighed for at få vist produktoplysninger og føje varer til indkøbsvognen fra en søgeresultater-side.

## <a name="add-a-search-results-module-to-a-category-page"></a>Føje et modul med søgeresultater til en kategoriside

Hvis du vil tilføje et modul til søgeresultater på en kategoriside i webstedsgeneratoren, skal du benytte følgende fremgangsmåde.

1. Gå til **Skabeloner**, og vælg **Ny** for at oprette en ny skabelon.
1. Angiv **Nu skabelon** i dialogboksen, angiv navnet **Søgeresultater**, og vælg derefter **OK**.
1. På pladsen **Brødtekst** skal du vælge ellipsen (...) og derefter **Tilføj modul**.
1. I dialogboksen **Vælg moduler** skal du vælge modulet **Standardside** og derefter **OK**.
1. På pladsen **Hoved** i modulet **Standardside** skal du vælge ellipsen (...) og derefter **Tilføj modul**.
1. I dialogboksen **Vælg moduler** skal du vælge modulet **Container** og derefter **OK**.
1. På pladsen **Container** skal du vælge ellipsen (...) og derefter **Tilføj modul**.
1. I dialogboksen **Vælg moduler** skal du vælge modulet **Brødkrumme** og derefter **OK**.
1. Angiv værdien **1** for **Min. indtræffer** i ruden **Brødkrumme**-egenskaber.
1. På pladsen **Container** skal du vælge ellipsen (...) og derefter **Tilføj modul**.
1. I dialogboksen **Vælg moduler** skal du vælge modulet **Søgeresultater** og derefter **OK**.
1. I ruden **Søgeresultater**-egenskaber skal du angive værdien **1** for **Min. indtræffer**, og derefter angive eventuelle andre nødvendige egenskaber for søgeresultaterne. Når du angiver disse egenskaber i skabelonen, sikrer du, at eventuelle tilpasninger af en bestemt kategoriside automatisk medtager disse indstillinger.
1. Vælg **Afslut redigering**, og vælg derefter **Publicer** for at publicere skabelonen.
1. Gå til **Sider**, og vælg **Ny** for at oprette en ny side.
1. Angiv **Kategoriside** under **Sidenavn** i dialogboksen **Opret en ny side**, og vælg derefter **Næste**.
1. Vælg **Søgeresultater**-skabelonen, du oprettede, under **Vælg en skabelon**, og vælg derefter **Næste**.
1. Vælg et sidelayout (f.eks. **Fleksibelt layout**) under **Vælg et layout**, og vælg derefter **Næste**.
1. Gennemse sidekonfigurationen under **Gennemse og afslut**. Hvis du vil redigere sideoplysningerne, skal du vælge **Tilbage**. Hvis sideoplysningerne er korrekte, skal du vælge **Opret side**.
1. Vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.

## <a name="inventory-aware-search-results-module"></a>Modul med lagerbaserede søgeresultater

Modulet med søgeresultater kan forbedres, så det omfatter lagerdata og giver følgende oplevelser:

- Vis lagerniveaulabels sammen med produkter.
- Skjul produkter, der ikke er på lager, på produktlisten.
- Vis produkter, der ikke er på lager, nederst på produktlisten.
- Understøt lagerbaseret produktfiltrering.

Hvis du vil aktivere disse oplevelser, skal du først aktivere funktionen **Udvidet e-handels-produktregistrering, der er lagerfølsom** og derefter konfigurere forudsætningsindstillinger i Commerce headquarters. Du finder flere oplysninger under [Lagerbaseret produktliste](inventory-aware-product-listing.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over standardlandingsside for kategori og side for søgeresultater](category-search-page-overview.md)

[Modulbibliotek, oversigt](starter-kit-overview.md)

[Hurtig visning-.modul](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
