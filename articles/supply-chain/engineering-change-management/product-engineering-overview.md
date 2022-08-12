---
title: Oversigt over teknisk ændringsstyring (indeholder video)
description: Denne artikel giver en oversigt over teknisk ændringsstyring, som hjælper dig med at planlægge og administrere produktversioner og administrere produktlivscyklusser og tekniske ændringer.
author: t-benebo
ms.date: 01/11/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 3a27548fff9728c74814fb92438da1d0c17b5e2b
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/29/2022
ms.locfileid: "9067386"
---
# <a name="engineering-change-management-overview"></a>Oversigt over teknisk ændringsstyring

[!include [banner](../includes/banner.md)]

## <a name="feature-summary"></a>Oversigt over funktioner

Moderne producenter kræver omfattende administration af produktdata, versionsstyring og styring af teknisk ændring for at opnå succes i en verden med konstant kortere produktlivscyklusser, højere kvalitets- og pålidelighedskrav og større fokus på produktsikkerhed.

Styring af tekniske ændringer bringer strukturen og disciplinen til administrationsprocessen for produktdata og gør det muligt at definere, frigive og revidere produkter på en kontrolleret måde, der understøttes af arbejdsprocesser. Ved hjælp af produktversioner og styring af tekniske ændringer kan du dokumentere, vurdere virkningen af og anvende tekniske ændringer under hele et produkts livscyklus.

Teknisk ændringsstyring hjælper dig med at planlægge og administrere produktversioner og administrere produktlivscyklusser og tekniske ændringer. Her er en oversigt over dens hovedfunktioner:

- Produktversioner
- Forbedrede produktudgivelsesfunktioner, der giver dig mulighed for at vedligeholde produktmasterdata i én juridisk enhed (den tekniske virksomhed) og publicere det fuldt konfigurerede, frigivne produkt til andre juridiske enheder
- Regler for validering af, at nødvendige oplysninger angives, før en produktversion aktiveres (parathedskontrol)
- Forbedret administration af produktets levetid med detaljeret styring af, hvornår et frigivet produkt kan bruges i bestemte forretningsprocesser
- Tekniske ændringsanmodninger, der understøttes af arbejdsprocesser
- Tekniske ændringsordrer, der understøttes af arbejdsprocesser

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4HE6B]

Den foregående video ([Styring af ændringer i Dynamics 365 Supply Chain Management](https://youtu.be/N313FqvRuBc)) er inkluderet i den [finans og drift-afspilningsliste](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), der er tilgængelig på YouTube.

## <a name="turn-on-the-engineering-change-management-features-for-your-system"></a>Aktivere styringen af tekniske funktionsændringer for systemet

Før du kan bruge styring af tekniske ændringer, skal du aktivere både funktionen *Styring af tekniske ændringer* og dens konfigurationsnøgle. Hvis du også vil spore versionsdimensionen for produkter i transaktioner (valgfrit), skal du også aktivere funktionen *Produktversionsdimension* og dens konfigurationsnøgle. Når disse forudsætninger er konfigureret som påkrævet, kan du aktivere yderligere valgfrie funktioner til ændringsstyring for teknikere.

### <a name="turn-the-basic-engineering-change-management-features-on-or-off"></a>Aktivere eller deaktivere styringen af tekniske basisfunktionsændringer

Følg disse trin for at aktivere eller deaktivere styringen af tekniske basisfunktionsændringer. Fra og med Supply Chain Management version 10.0.25 er funktionen *Styring af tekniske ændringer* som standard aktiveret.

1. Gå til arbejdsområdet [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
1. Søg efter opdateringer.
1. Slå den funktion, der hedder *Styring af tekniske ændringer*, til eller fra efter behov.
1. Hvis du også vil spore versionsdimensionen for produkter i transaktioner (valgfrit), skal du aktivere funktionen *Produktdimensionsversion*.

### <a name="turn-the-required-configuration-keys-on-or-off"></a>Slå de nødvendige konfigurationsnøgler til eller fra

Du skal derefter aktivere konfigurationsnøglerne ved at følge disse trin. Som standard er de ikke aktiveret.

1. Sæt systemet i vedligeholdelsestilstand som beskrevet under [Vedligeholdelsestilstand](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Gå til **Systemadministration \> Opsætning \> Licenskonfiguration**.
1. Udvid noden **Handel**.
1. Aktivér eller deaktiver konfigurationsnøglen for hovedfunktionen ved at markere afkrydsningsfeltet **Styring af tekniske ændringer**.
1. Udvid noden **Styring af tekniske ændringer**, og markér eller fjern markeringen i følgende afkrydsningsfelter efter behov (afhængigt af de funktioner du vil bruge):

    - **Attributsøgning** – Markér dette afkrydsningsfelt for at aktivere [funktionen til attributsøgning](engineering-attributes-and-search.md). Vi anbefaler, at du aktiverer denne funktion, men du kan fjerne markeringen i dette afkrydsningsfelt, hvis du ikke vil bruge den.
    - **Ændringsstyring for procesproduktion** – Markér dette afkrydsningsfelt, hvis du vil bruge funktioner til styring af tekniske ændringer til at administrere ændringer i formler til procesproduktion. Hvis du ikke skal administrere formler, kan du fjerne markeringen i dette afkrydsningsfelt. Du kan finde flere oplysninger under [Administrere ændringer i formler og deres stoffer](manage-formula-changes.md).

1. Hvis du også vil bruge versionsdimensionen, skal du markere afkrydsningsfeltet **Produktdimension – Version**. (Dette afkrydsningsfelt ligger længere nede på listen og er ikke indlejret under noden **Styring af tekniske ændringer**). Du kan fjerne markeringen i dette afkrydsningsfelt, hvis du ikke har brug for denne funktion.
1. Slå vedligeholdelsestilstand fra som beskrevet under [Vedligeholdelsestilstand](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Databasen skal synkroniseres for at sikre, at konfigurationsnøglerne er opdateret korrekt til at afspejle dine ændringer. Udfør et af følgende trin, afhængigt af den type miljø du arbejder på:
    - **Til Niveau 1-miljøer (udvikling)**: Åbn dit projekt i Microsoft Visual Studio, og vælg derefter **Dynamics 365 \> Synkroniser database \> Synkroniser**.
    - **Til Niveau 2-miljøer (og højere)**: Databasen synkroniseres automatisk, når du har sat miljøet i og uden for vedligeholdelsestilstand, så du kan springe dette trin over.

### <a name="turn-on-additional-engineering-change-management-features"></a>Aktivere styringen af tekniske yderligere funktionsændringer for systemet

Når du har aktiveret de grundlæggende funktioner til ændringsstyring for teknikerarbejde og aktiverer konfigurationsnøglerne, føjes flere ekstra og valgfri funktioner til ændringsstyring for teknikerarbejde til funktionsstyring. Hver af disse funktioner er angivet i modulet **Teknisk ændringsstyring**. I følgende tabel beskrives de enkelte valgfrie funktioner, og der er hyperlinks, som du kan finde flere oplysninger i. Fra og med Supply Chain Management version 10.0.25 er alle disse funktioner som standard aktiverede, men du kan stadig vælge at deaktivere dem.

| Funktionsnavn i funktionsstyring | Beskrivelse | Funktionstilstand |
|---|---|---|
| Aktivér administration af ændringer på eksisterende produkter | <p>Med denne funktion kan du konvertere eksisterende produkter til teknikere produkter, så du kan begynde at administrere dem ved hjælp af styring af engineering-ændringer.</p><p>Yderligere oplysninger finder du i [Aktivere administration af ændringer på eksisterende produkter](change-management-existing-products.md).</p> |
| Tekniske beskeder til produktion | <p>Når et produkt ændres inden for teknikerarbejde, kan det være vigtigt at give produktionen besked om disse ændringer. På den måde kan produktionsmedarbejdere træffe de relevante handlinger, f.eks. komponentsubstitution, styklisteerstatning eller ruteerstatning. Denne funktion giver dig mulighed for at give produktion besked om ændringer af produkter, der produceres.</p><p>Yderligere oplysninger finder du i [Administrere ændringer af tekniske produkter](engineering-change-management.md).</p> |
| Forbedret attributnedarvning for Administration af tekniske ændringer | <p>Denne funktion forenkler administrationen af attributter for færdigvarer eller mellemvarer. Når denne funktion er aktiveret, er det lettere at identificere alle de attributter, der hører til en vare, og du kan vælge de attributter, der skal overføres fra den pågældende vare til den overordnede vare. Denne funktion er nyttig, når én komponent i en færdig gode f.eks. er sårbar, giftig eller antændelig, da du nemt kan identificere den sårbar, giftige eller antændelige attribut og overføre den ud til den færdige vare.</p><p>Yderligere oplysninger finder du i [Tekniske attributter og søgning efter tekniske attributter](engineering-attributes-and-search.md).</p> |
| Kontroller af produktparathed | <p>Denne funktion giver også mulighed for at angive politikker for parathedskontroller for standardprodukter (ikke-tekniske). Brug parathedskontrol af produkter til at sikre, at hvert produkt er fuldt defineret, og at alle de nødvendige politikker er konfigureret, før produktet bliver tilgængeligt og bruges i transaktioner. Hvis du deaktiverer denne funktion, efter at du har brugt den et stykke tid, slettes alle eksisterende parathedskontroller for standardprodukter.</p><p>Du kan finde flere oplysninger under [Produktparathed](product-readiness.md).</p> |
| Administrer ændringer af formler og deres ingredienser | <p>Denne funktion giver dig mulighed for at spore ændringer af formelingredienser, ko-produkter og biprodukter.</p><p>Du kan finde flere oplysninger under [Administrere ændringer i formler og deres stoffer](manage-formula-changes.md).</p> |
| Variantgenerering af tekniske produkter | <p>Med denne funktion kan du generere varianter til teknikere produkter baseret på tilgængelige dimensionsværdier.</p><p>Du kan finde flere oplysninger i [Generere varianter for teknikprodukter](engineering-variants.md).</p> |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

