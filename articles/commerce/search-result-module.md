---
title: Modul til søgeresultater
description: Dette emne omhandler søgeresultater-moduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: bae825ed7093494c48abac119c480be0dba4f951
ms.sourcegitcommit: 9c2bc045eafc05b39ed1a6b601ccef48bd62ec55
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/14/2021
ms.locfileid: "7919468"
---
# <a name="search-results-module"></a>Modul til søgeresultater

[!include [banner](includes/banner.md)]


Dette emne omhandler søgeresultater-moduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.

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

## <a name="enable-inventory-awareness-for-the-search-results-module"></a>Aktivere lagervågenhed for modulet til søgeresultater

Kunder forventer generelt, at et e-handelswebsted er lagerbaseret i hele søgeoplevelsen, så de kan beslutte, hvad de skal gøre, hvis et bestemt produkt ikke er på lager. Modulet med søgeresultater kan forbedres, så det omfatter lagerdata og giver følgende oplevelser:

- Få vist en etiket for lagertilgængelighed sammen med produkter.
- Skjul produkter, der ikke er på lager.
- Få vist produkter, der ikke er på lager, nederst på listen over søgeresultater.
    
Hvis du vil aktivere disse oplevelser, skal du konfigurere følgende nødvendige indstillinger i Commerce Headquarters.

### <a name="enable-the-enhanced-e-commerce-product-discovery-to-be-inventory-aware-feature"></a>Aktivere funktionen Udvidet e-handelsproduktregistrering, der er lagerfølsom

> [!NOTE]
> Funktionen **Udvidet e-handelsproduktregistrering, der er lagerfølsom** er tilgængelig fra og med Commerce version 10.0.20.

Hvis du vil aktivere funktionen **Udvidet e-handelsproduktregistrering, der er lagerfølsom** i Commerce Headquarters, skal du følge disse trin.

1. Gå til **Arbejdsområder \> Funktionsstyring**.
1. Søg efter funktionen **Udvidet e-handelsproduktregistrering, der er lagerfølsom**, og aktivér den.

### <a name="configure-the-populate-product-attributes-with-inventory-level-job"></a>Konfigurere jobbet Udfyld produktattributter med lagerniveau

Jobbet **Udfyld produktattributter med lagerniveau** opretter en ny produktattribut til registrering af lagertilgængelighed og angiver derefter den pågældende attribut til den seneste lagerværdi for de enkelte masterprodukter. Da lagerbeholdningen af et produkt eller et sortiment, der sælges, ændres konstant, anbefales det på det kraftigste, at du planlægger jobbet som en batchproces.

Hvis du vil konfigurere jobbet **Udfyld produktattributter med lagerniveau** i Commerce Headquarters, skal du følge disse trin.

1. Gå til **Retail og Commerce \> Retail og Commerce IT \> Produkter og lager**.
1. Vælg **Udfyld produktattributter med lagerniveau**.
1. Benyt følgende fremgangsmåde i dialogboksen **Udfyld produktattributter med lagerniveau**:

    1. Under **Parametre** skal du gå til feltet **Produktattribut og typenavn** og angive et navn for den dedikerede produktattribut, der skal oprettes til registrering af lagertilgængelighed.
    1. Under **Parametre** skal du gå til feltet **Lagertilgængelighed baseret på** og vælge det antal, som beregningen på lagerniveau skal baseres på (for eksempel **Fysisk disponibelt**).
    1. Under **Kør i baggrunden** skal du konfigurere det job, der skal køres i baggrunden, og eventuelt slå indstillingen **Batchbehandling** til. 

> [!NOTE]
> Hvis du vil udføre ensartede beregninger af lagerniveau på tværs af PDP'er og produktlistesider på e-handelswebstedet, skal du sikre dig, at du vælger den samme indstilling for antal for både **Lagertilgængelighed baseret på** i Commerce Headquarters og indstillingen **Lagerniveau baseret på** i Commerce-webstedsgeneratoren. Du kan finde flere oplysninger om lagerindstillinger i webstedsgeneratoren under [Anvend lagerindstillinger](inventory-settings.md).

### <a name="configure-the-new-product-attribute"></a>Konfigurere den nye produktattribut

Når jobbet **Udfyld produktattributter med lagerniveau** er kørt, skal du konfigurere den netop oprettede produktattribut på det e-handelswebsted, hvor du vil aktivere lagervågenhed for modulet med søgeresultater.

Følg disse trin for at konfigurere den nye produktattribut i Commerce Headquarters.

1. Gå til **Retail og Commerce \> Konfiguration af kanal \> Kanalkategorier og produktattributter**, og vælg et e-handelswebsted.
1. Vælg og åbn en tilknyttet attributgruppe, føj den netop oprettede produktattribut til den, og luk derefter siden.
1. Vælg **Angiv attributmetadata**, vælg den netop tilføjede produktattribut, og slå derefter indstillingerne **Vis attribut på kanal**, **Kan hentes**, **Kan redigeres** og **Kan forespørges** til.

> [!NOTE]
> For produkter, der vises i modulet med søgeresultater, angives lagerniveauet på masterproduktniveau i stedet for på niveauet for de individuelle varianter. Det har kun to mulige værdier: "tilgængelig" og "ikke på lager". Den faktiske tekst til værdierne hentes fra definitionen på [lagerniveauprofilen](inventory-buffers-levels.md). Et masterprodukt anses kun for ikke at være på lager, når alle varianterne ikke er på lager. Lagerniveauet for en variant bestemmes på basis af produktets profildefinition på lagerniveau. 

Når alle de foregående konfigurationstrin er udført, viser afgrænsningerne på siden med søgeresultater et lagerbaseret filter, og modulet med søgeresultater henter lagerdataene bag fremgangsmåden. Du kan derefter konfigurere indstillingen **Lagerindstillinger for produktlistesider** i Commerce-webstedsgeneratoren til at styre, hvordan modulet med søgeresultater viser produkter, der ikke er på lager. Du finder flere oplysninger under [Anvendelse af lagerindstillinger](inventory-settings.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over standardlandingsside for kategori og side for søgeresultater](category-search-page-overview.md)

[Modulbibliotek, oversigt](starter-kit-overview.md)

[Hurtig visning-.modul](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
