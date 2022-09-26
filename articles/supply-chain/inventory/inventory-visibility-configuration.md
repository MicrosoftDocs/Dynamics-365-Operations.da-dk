---
title: Konfigurere Inventory Visibility
description: Denne artikel beskriver, hvordan du konfigurerer Lagersynlighed.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 61819d9c5af64b58697e07be85beebc084ae5935
ms.sourcegitcommit: 20ce54cb40290dd116ab8b157c0a02d6757c13f5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/20/2022
ms.locfileid: "9542266"
---
# <a name="configure-inventory-visibility"></a>Konfigurere Inventory Visibility

[!include [banner](../includes/banner.md)]


Denne artikel beskriver, hvordan du konfigurerer tilføjelsesprogrammet Lagersynlighed ved hjælp af lagersynlighed-app i Power Apps.

## <a name="introduction"></a><a name="introduction"></a>Start her

Før du begynder at arbejde med Lagersynlighed, skal du fuldføre følgende konfiguration som beskrevet i denne artikel:

- [Konfiguration af datakilde](#data-source-configuration)
- [Partitionskonfiguration](#partition-configuration)
- [Konfiguration af produktindekshierarki](#index-configuration)
- [Konfiguration af reservationer (valgfrit)](#reservation-configuration)
- [Eksempel på standardkonfiguration](#default-configuration-sample)

## <a name="prerequisites"></a>Forudsætninger

Før du går i gang, skal du installere og konfigurere tilføjelsesprogrammet Lagersynlighed som beskrevet i [Installere og konfigurere lagersynlighed](inventory-visibility-setup.md).

## <a name="the-configuration-page-of-the-inventory-visibility-app"></a><a name="configuration"></a>Konfigurationssiden for appen Lagersynlighed

I Power Apps hjælper siden **Konfiguration** på [Lagersynlighed-app](inventory-visibility-power-platform.md) med at konfigurere konfigurationen af disponibel lagerbeholdning og konfigurationen af foreløbige reservationer. Når tilføjelsesprogrammet er installeret, indeholder standardkonfigurationen værdien fra Microsoft Dynamics 365 Supply Chain Management (datakilden `fno`). Du kan gennemse standardindstillinger. Afhængigt af forretningsbehovene og det eksterne systems krav til lagerbogføring kan du desuden redigere konfigurationen for at standardisere, hvordan lagerændringer kan bogføres, organiseres og forespørges på på tværs af flere systemer. I de resterende afsnit af denne artikel forklares, hvordan du kan bruge de enkelte dele af **konfigurationssiden**.

Når konfigurationen er fuldført, skal du vælge **Opdater konfiguration** i appen.

## <a name="enable-inventory-visibility-features-in-power-apps-feature-management"></a><a name="feature-switch"></a>Aktivere funktioner for lagersynlighed i Power Apps-funktionsstyring

Tilføjelsesprogrammet Lagersynlighed tilføjer flere nye funktioner i Power Apps-installationen. Disse funktioner er som standard deaktiverede. Hvis du vil bruge dem, skal du åbne siden **Konfiguration** og derefter aktivere følgende funktioner efter behov under fanen **Funktionsstyring**.

| Funktionsstyringsnavn | Beskrivelse |
|---|---|
| *OnHandReservation* | Med denne funktion kan du oprette reservationer, forbruge reservationer og/eller annullere reservationen af angivne lagerantal ved hjælp af Lagersynlighed. Du kan finde flere oplysninger i [Reservationer i Lagersynlighed](inventory-visibility-reservations.md). |
| *OnHandMostSpecificBackgroundService* | Denne funktion viser en lageroversigt for produkter sammen med alle dimensioner. Lageroversigtsdataene synkroniseres periodisk fra Lagersynlighed. Standardsynkroniseringsfrekvensen er en gang hvert 15. minut og kan angives som højt som en gang hvert 5. minut. Du finder flere oplysninger under [Lageroversigt](inventory-visibility-power-platform.md#inventory-summary). |
| *onHandIndexQueryPreloadBackgroundService* | Denne funktion gør det muligt at forudindlæse forespørgsler om synlighed for disponibel lagerbeholdning, så du kan samle lister over disponible lagerbeholdninger med foruddefinerede dimensioner. Standardhyppigheden for synkronisering er en gang hvert 15. minut. Du finder flere oplysninger under [Lageroversigt](inventory-visibility-power-platform.md#preload-the-inventory-visibility-onhand-query). |
| *OnhandChangeSchedule* | Denne valgfrie funktion aktiverer funktionerne til ændringsplan for disponibelt antal og disponibel til tilsagn (DTT). Du kan finde flere oplysninger i [Ændringsplan for disponibelt antal og disponibel til tilsagn i lagersynlighed](inventory-visibility-available-to-promise.md). |
| *Tildeling* | Denne valgfrie funktion gør det muligt for lagersynlighed at have mulighed for lagerbeskyttelse (ringorganisering) og overstyring. Yderligere oplysninger finder du i [Fordeling af tilføjelsesprogrammet Lagersynlighed](inventory-visibility-allocation.md). |
| *Aktivér lagerstedsvarer i lagersynlighed* | Denne valgfrie funktion gør det muligt for lagersynlighed at understøtte varer, der er aktiveret til lokationsstyringsprocesser (WMS). Du kan finde flere oplysninger i [Understøttelse af lagersynlighed for WMS-varer](inventory-visibility-whs-support.md). |

## <a name="find-the-service-endpoint"></a><a name="get-service-endpoint"></a>Finde tjenestens slutpunkt

Hvis du ikke kender det korrekte slutpunkt for tjenesten Lagersynlighed, skal du åbne siden **Konfiguration** i Power Apps og derefter vælge **Vis tjenesteslutpunkt** i øverste højre hjørne. Siden viser det korrekte slutpunkt for tjenesten.

## <a name="data-source-configuration"></a><a name="data-source-configuration"></a>Konfiguration af datakilde

Datakilden repræsenterer det system, dataene kommer fra. Datakildenavne omfatter f.eks. `fno` (hvilket står for "Dynamics 365-programmer til finans og drift") og `pos` (hvilket står for "point of sale" – salgssted). Supply Chain Management er som standard konfigureret som standarddatakilde (`fno`) i Lagersynlighed.

> [!NOTE]
> Datakilden `fno` er reserveret til Supply Chain Management. Hvis tilføjelsesprogrammet Lagersynlighed er integreret med et Supply Chain Management-miljø, anbefales det, at du ikke sletter konfigurationer, der er relateret til `fno` i datakilden.

Hvis du vil tilføje en datakilde, skal du følge disse trin.

1. Log på Power Apps-miljøet, og åbn **Lagersynlighed**.
1. Åbn siden **Konfiguration**.
1. Vælg **Ny datakilde** under fanen **Datakilde** for at tilføje en datakilde.

> [!NOTE]
> Når du tilføjer en datakilde, skal du sørge for at validere datakildens navn, fysiske målinger og dimensionstilknytninger, før du opdaterer konfigurationen af tjenesten Lagersynlighed. Du kan ikke ændre disse indstillinger, når du har valgt **Opdater konfiguration**.

Datakildekonfigurationen omfatter følgende dele:

- Dimensions (dimensionstilknytning)
- Fysiske målinger
- Beregnede målinger

### <a name="dimensions-dimension-mapping"></a><a name="data-source-configuration-dimension"></a>Dimensions (dimensionstilknytning)

Formålet med dimensionskonfigurationen er at standardisere integrationen af flere systemer for bogføringshændelser og -forespørgsler baseret på dimensionskombinationer. Lagersynlighed indeholder en liste over basisdimensioner, der kan tilknyttes fra dimensionerne for datakilden. Der er 33 tilgængelige dimensioner ved tilknytning.

- Hvis du bruger Supply Chain Management som en af datakilderne, knyttes der som standard 13 dimensioner til standarddimensionerne for Supply Chain Management. 12 andre dimensioner (`inventDimension1` til `inventDimension12`) tilknyttes brugerdefinerede dimensioner i Supply Chain Management. De resterende otte dimensioner er udvidede dimensioner, du kan knytte til eksterne datakilder.
- Hvis du ikke bruger Supply Chain Management som en af datakilderne, kan du frit tilknytte dimensionerne. I følgende tabel vises hele listen over tilgængelige dimensioner.

> [!NOTE]
> Hvis dimensionen ikke findes på standarddimensionslisten, og du bruger en ekstern datakilde, anbefales det at bruge `ExtendedDimension1` til `ExtendedDimension8` til at udføre tilknytningen.

| Dimensionstype | Basisdimension |
|---|---|
| Produkt | `ColorId` |
| Produkt | `SizeId` |
| Produkt | `StyleId` |
| Produkt | `ConfigId` |
| Sporing | `BatchId` |
| Sporing | `SerialId` |
| Lokation | `LocationId` |
| Lokation | `SiteId` |
| Lagerstatus | `StatusId` |
| Lagerstedsspecifik | `WMSLocationId` |
| Lagerstedsspecifik | `WMSPalletId` |
| Lagerstedsspecifik | `LicensePlateId` |
| Andre | `VersionId` |
| Lager (brugerdefineret) | `InventDimension1` til `InventDimension12` |
| Forlængelse | `ExtendedDimension1` til `ExtendedDimension8` |
| Sys | `Empty` |

> [!NOTE]
> Den dimensionstype, der er anført i den foregående tabel, er kun til reference. Du behøver ikke at definere dem i Lagersynlighed.
>
> Lagerdimensioner (brugerdefinerede) kan reserveres til Supply Chain Management. I dette tilfælde kan du bruge de udvidede dimensioner i stedet.

Eksterne systemer kan få adgang til Lagersynlighed via dens RESTful-API'er. Med henblik på integrationen kan du med Lagersynlighed konfigurere den _eksterne datakilde_ og tilknytningen fra de _eksterne dimensioner_ til _basisdimensionerne_. Her er et eksempel på en tabel for dimensionstilknytninger.

| Ekstern dimension | Basisdimension |
|---|---|
| `MyColorId` | `ColorId` |
| `MySizeId` | `SizeId` |
| `MyStyleId` | `StyleId` |
| `MyDimension1` | `ExtendedDimension1` |
| `MyDimension2` | `ExtendedDimension2` |

Ved at konfigurere en dimensionstilknytning kan du sende de eksterne dimensioner direkte til Lagersynlighed. Lagersynlighed konverterer automatisk eksterne dimensioner til basisdimensioner.

Hvis du vil tilføje dimensionstilknytninger, skal du følge disse trin.

1. Log på Power Apps-miljøet, og åbn **Lagersynlighed**.
1. Åbn siden **Konfiguration**.
1. Under fanen **Datakilde** i sektionen **Dimensionstilknytninger** skal du vælge **Tilføj** for at tilføje dimensionstilknytninger.
    ![Tilføjelse af dimensionstilknytninger](media/inventory-visibility-dimension-mapping.png "Tilføjelse af dimensionstilknytninger")

1. Angiv kildedimensionen i feltet **Dimensionsnavn**.
1. Vælg den dimension i Lagersynlighed, du vil tilknytte, i feltet **Til basisdimension**.
1. Vælg **Gem**.

Hvis datakilden f.eks. indeholder en produktfarvedimension, kan du knytte den til basisdimensionen `ColorId` for at tilføje en brugerdefineret dimension for `ProductColor` i datakilden `exterchannel`. Den knyttes derefter til `ColorId`-basisdimensionen.

### <a name="physical-measures"></a><a name="data-source-configuration-physical-measures"></a>Fysiske målinger

Når en datakilde bogfører en lagerændring til Lagersynlighed, bogføres ændringen ved hjælp af *fysiske målinger*. Fysiske målinger ændrer antallet og afspejler lagerstatussen. Du kan definere dine egne fysiske mål ud fra dine behov. Forespørgsler kan baseres på de fysiske målinger.

Lagersynlighed indeholder en liste over fysiske standardmål, der er knyttet til Supply Chain Management (datakilden `fno`). Disse fysiske standardmålinger hentes fra lagertransaktionens statusser på siden **Liste over disponibel lagerbeholdning** i Supply Chain Management (**Lagerstyring \> Forespørgsler og rapport \> Liste over disponibel lagerbeholdning**). Følgende tabel indeholder et eksempel på fysiske målinger.

| Navn på fysisk måling | Beskrivelse |
|---|---|
| `NotSpecified` | Ikke angivet |
| `Arrived` | Ankommet |
| `AvailOrdered` | Tilgængelige bestilt |
| `AvailPhysical` | Fysisk disponibelt |
| `Deducted` | Trukket |
| `OnOrder` | OnOrder |
| `Ordered` | Bestilt |
| `PhysicalInvent` | Fysisk lager |
| `Picked` | Plukket |
| `PostedQty` | Bogført antal |
| `QuotationIssue` | Tilbudsafgang |
| `QuotationReceipt` | Tilbudstilgang |
| `Received` | Modtaget |
| `Registered` | Registreret |
| `ReservOrdered` | Bestilt reserveret |
| `ReservPhysical` | Fysisk reserveret |

Hvis datakilden er Supply Chain Management, behøver du ikke oprette de fysiske standardmålinger igen. For eksterne datakilder kan du dog oprette nye fysiske målinger ved at følge disse trin.

1. Log på Power Apps-miljøet, og åbn **Lagersynlighed**.
1. Åbn siden **Konfiguration**.
1. Vælg **Tilføj**, angiv navnet på en kildemåling i sektionen **Fysiske målinger** under fanen **Datakilde**, og gem ændringerne.

### <a name="calculated-measures"></a>Beregnede målinger

Du kan bruge Lagersynlighed til at forespørge på både fysiske målinger for lagerbeholdning og *brugerdefinerede beregnede målinger*. Beregnede målinger udgør en brugerdefineret beregningsformel, der består af en kombination af fysiske målinger. Denne funktion gør det muligt at definere et sæt fysiske målinger, der skal tilføjes, og/eller et sæt fysiske målinger, der skal trækkes fra, så de danner den tilpassede måling.

> [!IMPORTANT]
> En beregnet måling er en komposition af fysiske målinger. Formlen kan kun indeholde fysiske målinger uden dubletter, ikke beregnede målinger.

Med konfigurationen kan du definere et sæt modifikatorer, der skal lægges til eller trækkes fra for at få det totale aggregerede outputantal.

Hvis du vil konfigurere en brugerdefineret beregnet måling, skal du gøre følgende.

1. Log på Power Apps-miljøet, og åbn **Lagersynlighed**.
1. Åbn siden **Konfiguration**.
1. Vælg **Ny beregnet måling** under fanen **Beregnet måling** for at tilføje en beregnet måling.
1. Angiv følgende felter for den nye beregnede måling:

    - **Navn på ny beregnet måling** – Angiv navnet på den beregnede måling.
    - **Datakilde** – Vælg den datakilde, der er tilknyttet den nye modifikator. Forespørgselssystemet er en datakilde.

1. Vælg **Tilføj** for at føje en modifikator til den nye beregnede måling.
1. Angiv følgende felter til den nye modifikator:

    - **Modifikator** – Vælg modifikatortypen (*Addition* eller *Subtraktion*).
    - **Datakilde** – Vælg den datakilde, hvor den måling, der angiver modifikatorværdien, findes.
    - **Måling** – Vælg navnet på den måling (fra den valgte datakilde), der angiver værdien for modifikatoren.

1. Gentag trin 5 til 6, indtil du har tilføjet alle nødvendige modifikatorer.
1. Vælg **Gem**.

Du kan f.eks. få følgende forespørgelsresultat.

```json
[
    {
        "productId": "T-shirt",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red"
        },
        "quantities": {
            "pos": {
                "inbound": 80.0,
                "outbound": 20.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "externalchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]
```

Derefter konfigurerer du en beregnet måling med navnet `MyCustomAvailableforReservation` som vist i følgende tabel. Denne beregnede måling forbruges i forbrugssystemet.

| Forbrugssystem | Beregnet måling | Datakilde | Fysisk måling | Kalkulationstype |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `pos` | `inbound` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `pos` | `outbound` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `received` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `scheduled` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `issued` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `reserved` | `Subtraction` |

Når denne beregningsformel bruges, omfatter det nye forespørgselsresultat den tilpassede måling.

```json
[
    {
        "productId": "T-shirt",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red"
        },
        "quantities": {
            "pos": {
                "inbound": 80.0,
                "outbound": 20.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "externalchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

Outputtet `MyCustomAvailableforReservation`, der er baseret på beregningsindstillingen i de brugerdefinerede målinger, er 100 + 50 – 10 + 80 – 20 + 90 + 30 – 60 – 40 = 220.

## <a name="partition-configuration"></a><a name="partition-configuration"></a>Partitionskonfiguration

I øjeblikket består partitionskonfigurationen af to basisdimensioner (`SiteId` og `LocationId`), der angiver, hvordan dataene fordeles. Operationer under samme partition kan give en højere ydeevne og lavere omkostninger. I følgende tabel vises den standardkonfiguration af partition, som tilføjelsesprogrammet Lagersynlighed leverer.

| Basisdimension | Hierarki |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |

Løsningen inkluderer som standard denne partitionskonfiguration. Du *behøver derfor ikke definere den selv*.

> [!IMPORTANT]
> Lad være med at tilpasse standardkonfigurationen af partitioner. Hvis du sletter eller ændrer den, opstår der højst sandsynligt en uventet fejl.

## <a name="product-index-hierarchy-configuration"></a><a name="index-configuration"></a>Konfiguration af produktindekshierarki

Lagerbeholdningsforespørgslen vil det meste af tiden ikke kun være på det højeste "totalniveau". I stedet vil du måske også se resultater, der aggregeres baseret på lagerdimensionerne.

Lagersynlighed giver fleksibilitet ved at lade dig konfigurere _indekserne_ for at forbedre ydeevnen af dine forespørgsler. Disse indekser er baseret på en dimension eller en kombination af dimensioner. Et indeks består af et *sætnummer*, en *dimension* og et *hierarki* som defineret i følgende tabel.

| Navn | Beskrivelse |
|---|---|
| Sætnummer | Dimensioner, der tilhører samme sæt (indeks), grupperes sammen, og det samme sætnummer tildeles dem. |
| Dimension | Basisdimensioner, som resultatet af forespørgslen aggregeres på. |
| Hierarki | Hierarkiet giver dig mulighed for at øge ydeevnen for bestemte kombinationer af dimension, når de bruges i filter- og grupper efter-forespørgselsparametre. Hvis du f.eks. konfigurerer et dimensionssæt med en hierarkisekvens af `(ColorId, SizeId, StyleId)`, kan systemet behandle forespørgsler, der er relateret til fire dimensionskombinationer hurtigere. Den første kombination er tom, den anden er `(ColorId)`, den tredje er `(ColorId, SizeId)`, og den fjerde er `(ColorId, SizeId, StyleId)`. Andre kombinationer kan ikke blive hurtigere. Filtrene er ikke begrænset af rækkefølgen, men skal være i disse dimensioner, hvis du vil forbedre deres ydeevne. Du kan finde flere oplysninger i eksemplet, der følger. |

Hvis du vil konfigurere produkthierarkiindekset, skal du følge disse trin.

1. Log på Power Apps-miljøet, og åbn **Lagersynlighed**.
1. Åbn siden **Konfiguration**.
1. Vælg **Tilføj** i sektionen **Dimensionstilknytninger** under fanen **Produkthierarkiindeks** for at tilføje dimensionstilknytninger.
1. Der er som standard angivet en liste over indekser. Hvis du vil redigere et eksisterende indeks, skal du vælge **Rediger** eller **Tilføj** i sektionen for det relevante indeks. Hvis du vil oprette et nyt indekssæt, skal du vælge **Nyt indekssæt**. For hver række i hvert indekssæt skal du i feltet **Dimension** vælge fra listen over basisdimensioner. Der generes automatisk værdier for følgende felter:

    - **Sætnummer** – Dimensioner, der tilhører samme gruppe (indeks), grupperes sammen og tildeles det samme sætnummer.
    - **Hierarki** – Hierarkiet øger ydeevnen for bestemte kombinationer af dimension, når de bruges i filter- og grupper efter-forespørgselsparametre.

> [!TIP]
> Du kan bruge et par tip, som du kan huske, når du konfigurerer indekshierarkiet:
>
> - Basisdimensioner, der er defineret i partitionskonfigurationen, bør ikke defineres i indekskonfigurationer. Hvis der igen defineres en basisdimension i indekskonfigurationen, kan du ikke forespørge på dette indeks.
> - Hvis du kun skal forespørge på lager, der aggregeres af alle dimensionskombinationer, kan du konfigurere et enkelt indeks, der indeholder basisdimensionen `Empty`.

### <a name="example"></a>Eksempel

Dette afsnit indeholder et eksempel på, hvordan hierarkiet fungerer.

Følgende tabel indeholder en liste over den tilgængelige lagerbeholdning i dette eksempel.

| Post | ColorId | SizeId | StyleId | Mængde |
|---|---|---|---|---|
| T-shirt | Sort | Lille | Bred | 1 |
| T-shirt | Sort | Lille | Regulær | 2 |
| T-shirt | Sort | Stor | Bred | 3 |
| T-shirt | Sort | Stor | Regulær | 4 |
| T-shirt | Rød | Lille | Bred | 5 |
| T-shirt | Rød | Lille | Regulær | 6 |
| T-shirt | Rød | Stor | Regulær | 7 |

Følgende tabel viser, hvordan indekshierarkiet er konfigureret.

| Sætnummer | Dimension | Hierarki |
|---|---|---|
| 1 | `ColorId` | 1 |
| 1 | `SizeId` | 2 |
| 1 | `StyleId` | 3 |

Med indekset kan du forespørge på den disponible lagerbeholdning på følgende måder:

- `()` – Grupperet efter alle

    - T-shirt, 28

- `(ColorId)`– Grupperet efter `ColorId`

    - T-shirt, Sort, 10
    - T-shirt, Rød, 18

- `(ColorId, SizeId)`– Grupperet efter kombinationen af `ColorId` og `SizeId`

    - T-shirt, Sort, Lille, 3
    - T-shirt, Sort, Stor, 7
    - T-shirt, Rød, Lille, 11
    - T-shirt, Rød, Stor, 7

- `(ColorId, SizeId, StyleId)`– Grupperet efter kombinationen af `ColorId`, `SizeId` og `StyleId`

    - T-shirt, Sort, Lille, Bred, 1
    - T-shirt, Sort, Lille, Almindelig, 2
    - T-shirt, Sort, Stor, Bred, 3
    - T-shirt, Sort, Stor, Almindelig, 4
    - T-shirt, Rød, Lille, Bred, 5
    - T-shirt, Rød, Lille, Almindelig, 6
    - T-shirt, Rød, Stor, Almindelig, 7

## <a name="reservation-configuration-optional"></a><a name="reservation-configuration"></a>Konfiguration af reservationer (valgfrit)

Konfiguration af reservationer er påkrævet, hvis du vil bruge funktionen til foreløbig reservation. Konfigurationen består af to grundlæggende dele:

- Tilknytning af foreløbige reservationer
- Hierarki for foreløbige reservationer

### <a name="soft-reservation-mapping"></a>Tilknytning af foreløbige reservationer

Når du foretager en reservation, vil du måske gerne vide, om den disponible lagerbeholdning er tilgængelig for reservation. Valideringen er knyttet til en beregnet måling, der repræsenterer en beregningsformel for en kombination af fysiske målinger.

Når du opretter tilknytningen fra den fysiske måling til den beregnede måling, aktiverer du tjenesten Lagersynlighed til automatisk at validere reservationens tilgængelighed ud fra den fysiske måling.

Før du konfigurerer denne tilknytning, skal de fysiske målinger, beregnede målinger og deres datakilder defineres under fanerne **Datakilde** og **Beregnet måling** på siden **Konfiguration** i Power Apps (som beskrevet tidligere i denne artikel).

Hvis du vil definere tilknytningen for en foreløbig reservation, skal du følge disse trin.

1. Definer den fysiske måling, der fungerer som måling for foreløbige reservationer (f.eks. `SoftReservOrdered`).
1. Definer på siden **Konfiguration** under fanen **Beregnet måling** den beregnede måling for *tilgængelig lagerbeholdning for reservation* (AFR), der indeholder den AFR-beregningsformel, som du vil knytte til den fysiske måling. Du kan f.eks. konfigurere `AvailableToReserve` (tilgængelig for reservation), så den knyttes til den tidligere definerede fysiske måling `SoftReservOrdered`. På den måde kan du finde ud af, hvilke antal med lagerstatussen `SoftReservOrdered`, der er tilgængelige for reservation. Følgende tabel viser AFR-beregningsformlen.

    | Kalkulationstype | Datakilde | Fysisk måling |
    |---|---|---|
    | Addition | `fno` | `AvailPhysical` |
    | Addition | `pos` | `Inbound` |
    | Subtraktion | `pos` | `Outbound` |
    | Subtraktion | `iv` | `SoftReservOrdered` |

    Det anbefales, at du konfigurerer den beregnede måleenhed, så den indeholder den fysiske måling, som reservationsmåleenheden er baseret på. På denne måde påvirkes det beregnede måleantal af antallet for reservationen. I dette eksempel skal det beregnede målepunkt `AvailableToReserve` for datakilden `iv` indeholde den fysiske måling `SoftReservOrdered` fra `iv` som en komponent.

1. Åbn siden **Konfiguration**.
1. Konfigurer tilknytningen fra den fysiske måling til den beregnede måling under fanen **Tilknytning af foreløbig reservation**. I det forrige eksempel kan du bruge følgende indstillinger til at knytte `AvailableToReserve` til den tidligere definerede fysiske måling `SoftReservOrdered`.

    | Datakilde for fysisk måling | Fysisk måling | Tilgængelig for reservations datakilde | Tilgængelig for beregnet måling for reservation |
    |---|---|---|---|
    | `iv` | `SoftReservOrdered` | `iv` | `AvailableToReserve` |

    > [!NOTE]
    > Hvis du ikke kan redigere fanen **Tilknytning af foreløbige reservationer**, skal du aktivere funktionen *OnHandReservation* under fanen **Funktionsstyring**.

Når du foretager reservationer på `SoftReservOrdered`, finder Lagersynlighed automatisk `AvailableToReserve` og den relaterede beregningsformel for at foretage reservationsvalideringen.

Du har f.eks. følgende disponible lagerbeholdninger i Lagersynlighed.

```json
{
    "productId": "T-shirt",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red"
    },
    "quantities": {
        "iv": {
            "SoftReservOrdered": 90
        },
        "fno": {
            "availphysical": 70.0,
        },
        "pos": {
            "inbound": 50.0,
            "outbound": 20.0
        }
    }
}
```

I dette tilfælde anvendes følgende beregning:

`AvailableToReserve` = `fno.availphysical` + `pos.inbound` – `pos.outbound` – `iv.SoftReservOrdered`  
= 70 + 50 – 20 – 90  
= 10

Hvis du forsøger at foretage reservationer for `iv.SoftReservOrdered`, og antallet er mindre end eller lig med `AvailableToReserve` (10), kan du derfor foretage reservationen.

> [!NOTE]
> Når du kalder reservations-API'en, kan du styre valideringen af reservationen ved at angive parameteren Boolesk `ifCheckAvailForReserv` i brødteksten. Værdien `True` betyder, at valideringen er påkrævet, mens værdien `False` betyder, at valideringen ikke er nødvendig. Standardværdien er `True`.

### <a name="soft-reservation-hierarchy"></a>Hierarki for foreløbige reservationer

Reservationshierarkiet beskriver den dimensionsrækkefølge, der skal angives, når der foretages reservationer. Det fungerer på samme måde, som produktindekshierarkiet fungerer i forbindelse med forespørgsler om disponibel lagerbeholdning.

Reservationshierarkiet er uafhængigt af produktindekshierarkiet. Dette afhængighedsforhold gør det muligt at implementere kategoristyring, hvor brugerne kan opdele dimensionerne for at angive detaljerede krav og kunne foretage mere præcise reservationer. Det forhåndsreservationshierarki skal indeholde `SiteId` og `LocationId` som komponenter, da de opbygger partitionskonfigurationen. Når du reserverer, skal du angive en partition for produktet.

Her er et eksempel på et foreløbigt reservationshierarki.

| Basisdimension | Hierarki |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |
| `StyleId` | 5 |

I dette eksempel kan du foretage reservationer i følgende dimensionsserier. Når du reserverer, skal du angive en partition for produktet. Det grundlæggende hierarki, du kan bruge, er derfor `(SiteId, LocationId)`.

- `(SiteId, LocationId)`
- `(SiteId, LocationId, ColorId)`
- `(SiteId, LocationId, ColorId, SizeId)`
- `(SiteId, LocationId, ColorId, SizeId, StyleId)`

En gyldig dimensionsrækkefølge skal nøje følge reservationshierarkiet, dimension for dimension. Hierarkirækkefølgen `(SiteId, LocationId, SizeId)` er f.eks. ikke gyldig, fordi `ColorId` mangler.

## <a name="available-to-promise-configuration-optional"></a>Konfiguration af disponibel til tilsagn (valgfrit)

Du kan konfigurere lagersynlighed, så du kan planlægge fremtidige ændringer af disponibelt antal og beregne DTT-mængder for disponibel til tilsagn. DTT er antallet af en vare, der er tilgængelig og kan være lovet til en kunde i den næste periode. Brug af denne beregning kan øge ordreopfyldelsesfunktionaliteten væsentligt. Hvis du vil bruge denne funktion, skal du aktivere den under fanen **Funktionsstyring** og derefter konfigurere den under fanen **DTT-indstilling**. Du kan finde flere oplysninger i [Ændringsplaner for disponibelt antal og disponibel til tilsagn i lagersynlighed](inventory-visibility-available-to-promise.md).

## <a name="complete-and-update-the-configuration"></a>Fuldføre og opdatere konfigurationen

Når du har fuldført konfigurationen, skal du foretage alle ændringer af Lagersynlighed. Hvis du vil foretage ændringer, skal du vælge **Opdater konfiguration** øverst til højre på siden **Konfiguration** i Power Apps.

Første gang du vælger **Opdater konfiguration**, beder systemet om dine legitimationsoplysninger.

- **Klient-id** – Det program-id for Azure, som du har oprettet for Lagersynlighed.
- **Lejer-id** – Dit lejer-id for Azure.
- **Klienthemmelighed** – Den programhemmelighed for Azure, som du har oprettet for Lagersynlighed.

Når du er logget på, opdateres konfigurationen i tjenesten Lagersynlighed.

> [!NOTE]
> Sørg for at validere datakildens navn, fysiske målinger og dimensionstilknytninger, før du opdaterer konfigurationen af tjenesten Lagersynlighed. Du kan ikke ændre disse indstillinger, når du har valgt **Opdater konfiguration**.

## <a name="default-configuration-sample"></a><a name="default-configuration-sample"></a>Eksempel på standardkonfiguration

Under initialiseringsstadiet opretter Lagersynlighed en standardkonfiguration, som er beskrevet her. Du kan ændre denne konfiguration efter behov.

### <a name="data-source-configuration"></a>Konfiguration af datakilde

#### <a name="configuration-of-the-iv-data-source"></a>Konfiguration af iv-datakilden

I dette afsnit beskrives, hvordan `iv`-datakilden konfigureres.

##### <a name="physical-measures-configured-for-the-iv-data-source"></a>Fysiske mål, der er konfigureret for "iv"-datakilden

Der konfigureres følgende fysiske målinger for `iv`-datakilden:

- `Ordered`
- `SoftReservPhysical`
- `SoftReservOrdered`
- `ReservOrdered`
- `ReservPhysical`

##### <a name="orderedtotal-calculated-measure"></a>Beregnet måling for OrderedTotal

Den beregnede måling for `OrderedTotal` konfigureres for `iv`-datakilden som vist i følgende tabel.

| Kalkulationstype | Datakilde | Fysisk måling |
|---|---|---|
| Addition | `fno` | `Ordered` |
| Addition | `fno` | `Arrived` |
| Addition | `iv` | `Ordered` |

##### <a name="onhand-calculated-measure"></a>Beregnet måling for OnHand

Den beregnede måling for `OnHand` konfigureres for `iv`-datakilden som vist i følgende tabel.

| Kalkulationstype | Datakilde | Fysisk måling |
|---|---|---|
| Addition | `fno` | `PhysicalInvent` |
| Addition | `iom` | `OnHand` |
| Addition | `erp` | `Unrestricted` |
| Addition | `erp` | `QualityInspection` |
| Addition | `pos` | `PosInbound` |
| Subtraktion | `pos` | `PosOutbound` |

##### <a name="reservedtotal-calculated-measure"></a>Beregnet måling for ReservedTotal

Den beregnede måling for `ReservedTotal` konfigureres for `iv`-datakilden som vist i følgende tabel.

| Kalkulationstype | Datakilde | Fysisk måling |
|---|---|---|
| Addition | `fno` | `ReservPhysical` |
| Addition | `fno` | `ReservOrdered` |
| Addition | `iv` | `SoftReservPhysical` |
| Addition | `iv` | `SoftReservOrdered` |
| Addition | `iv` | `ReservPhysical` |
| Addition | `iv` | `ReservOrdered` |

##### <a name="softreserved-calculated-measure"></a>Beregnet måling for SoftReserved

Den beregnede måling for `SoftReserved` konfigureres for `iv`-datakilden som vist i følgende tabel.

| Kalkulationstype | Datakilde | Fysisk måling |
|---|---|---|
| Addition | `iv` | `SoftReservPhysical` |
| Addition | `iv` | `SoftReservOrdered` |

##### <a name="hardreserved-calculated-measure"></a>Beregnet måling for HardReserved

Den beregnede måling for `HardReserved` konfigureres for `iv`-datakilden som vist i følgende tabel.

| Kalkulationstype | Datakilde | Fysisk måling |
|---|---|---|
| Addition | `fno` | `ReservPhysical` |
| Addition | `fno` | `ReservOrdered` |
| Addition | `iv` | `ReservPhysical` |
| Addition | `iv` | `ReservOrdered` |

##### <a name="openorder-calculated-measure"></a>Beregnet måling for OpenOrder

Den beregnede måling for `OpenOrder` konfigureres for `iv`-datakilden som vist i følgende tabel.

| Kalkulationstype | Datakilde | Fysisk måling |
|---|---|---|
| Addition | `fno` | `OnOrder` |
| Addition | `iom` | `OnOrder` |

##### <a name="onhandavailable-calculated-measure"></a>Beregnet måling for onHandAvailable

Den beregnede måling for `OnHandAvailable` konfigureres for `iv`-datakilden som vist i følgende tabel.

| Kalkulationstype | Datakilde | Fysisk måling |
|---|---|---|
| Addition | `fno` | `PhysicalInvent` |
| Addition | `iom` | `OnHand` |
| Addition | `erp` | `Unrestricted` |
| Addition | `erp` | `QualityInspection` |
| Addition | `pos` | `PosInbound` |
| Subtraktion | `fno` | `ReservPhysical` |
| Subtraktion | `iv` | `SoftReservPhysical` |
| Subtraktion | `pos` | `PosOutbound` |

##### <a name="availabletoreserve-calculated-measure"></a>Beregnet måling for AvailableToReserve

Den beregnede måling for `AvailableToReserve` konfigureres for `iv`-datakilden som vist i følgende tabel.

| Kalkulationstype | Datakilde | Fysisk måling |
|---|---|---|
| Addition | `fno` | `PhysicalInvent` |
| Addition | `iom` | `OnHand` |
| Addition | `erp` | `Unrestricted` |
| Addition | `erp` | `QualityInspection` |
| Addition | `pos` | `PosInbound` |
| Addition | `fno` | `Ordered` |
| Addition | `fno` | `Arrived` |
| Addition | `iv` | `Ordered` |
| Subtraktion | `fno` | `ReservPhysical` |
| Subtraktion | `fno` | `ReservOrdered` |
| Subtraktion | `iv` | `SoftReservPhysical` |
| Subtraktion | `iv` | `SoftReservOrdered` |
| Subtraktion | `iv` | `ReservPhysical` |
| Subtraktion | `iv` | `ReservOrdered` |
| Subtraktion | `pos` | `PosOutbound` |

##### <a name="inventorysupply-calculated-measure"></a>Beregnet måling for InventorySupply

Den beregnede måling for `InventorySupply` konfigureres for `iv`-datakilden som vist i følgende tabel.

| Kalkulationstype | Datakilde | Fysisk måling |
|---|---|---|
| Addition | `fno` | `Ordered` |
| Addition | `fno` | `Arrived` |
| Addition | `iv` | `Ordered` |
| Addition | `fno` | `PhysicalInvent` |
| Addition | `iom` | `OnHand` |
| Addition | `erp` | `Unrestricted` |
| Addition | `erp` | `QualityInspection` |
| Addition | `pos` | `PosInbound` |
| Subtraktion | `pos` | `PosOutbound` |

##### <a name="inventorydemand-calculated-measure"></a>Beregnet måling for InventoryDemand

Den beregnede måling for `InventoryDemand` konfigureres for `iv`-datakilden som vist i følgende tabel.

| Kalkulationstype | Datakilde | Fysisk måling |
|---|---|---|
| Addition | `fno` | `OnOrder` |
| Addition | `iom` | `OnOrder` |
| Addition | `iv` | `SoftReservPhysical` |
| Addition | `iv` | `SoftReservOrdered` |
| Addition | `fno` | `ReservPhysical` |
| Addition | `fno` | `ReservOrdered` |
| Addition | `iv` | `ReservPhysical` |
| Addition | `iv` | `ReservOrdered` |

#### <a name="configuration-of-the-fno-data-source"></a>Konfiguration af "fno"-datakilden

I dette afsnit beskrives, hvordan `fno`-datakilden konfigureres.

##### <a name="dimension-mappings-for-the-fno-data-source"></a>Dimensionstilknytninger for "fno"-datakilden

De dimensionstilknytninger, der vises i følgende tabel, er konfigureret for `fno`-datakilden.

| Ekstern dimension | Basisdimension |
|---|---|
| `InventBatchId` | `BatchId` |
| `InventColorId` | `ColorId` |
| `InventLocationId` | `LocationId` |
| `InventSerialId` | `SerialId` |
| `InventSiteId` | `SiteId` |
| `InventSizeId` | `SizeId` |
| `InventStatusId` | `StatusId` |
| `InventStyleId` | `StyleId` |
| `LicensePlateId` | `LicensePlateId` |
| `WMSLocationId` | `WMSLocationId` |
| `WMSPalletId` | `WMSPalletId` |
| `ConfigId` | `ConfigId` |
| `InventVersionId` | `VersionId` |
| `InventDimension1` | `CustomDimension1` |
| `InventDimension2` | `CustomDimension2` |
| `InventDimension3` | `CustomDimension3` |
| `InventDimension4` | `CustomDimension4` |
| `InventDimension5` | `CustomDimension5` |
| `InventDimension6` | `CustomDimension6` |
| `InventDimension7` | `CustomDimension7` |
| `InventDimension8` | `CustomDimension8` |
| `InventDimension9` | `CustomDimension9` |
| `InventDimension10` | `CustomDimension10` |
| `InventDimension11` | `CustomDimension11` |
| `InventDimension12` | `CustomDimension12` |

##### <a name="physical-measures-configured-for-the-fno-data-source"></a>Fysiske målinger, der er konfigureret for "fno"-datakilden

Der konfigureres følgende fysiske målinger for `fno`-datakilden:

- `Ordered`
- `Arrived`
- `AvailPhysical`
- `PhysicalInvent`
- `ReservPhysical`
- `ReservOrdered`
- `OnOrder`

#### <a name="configuration-of-the-pos-data-source"></a>Konfiguration af "pos"-datakilden

I dette afsnit beskrives, hvordan `pos`-datakilden konfigureres.

##### <a name="physical-measures-for-the-pos-data-source"></a>Fysiske målinger for "pos"-datakilden

Der konfigureres følgende fysiske målinger for `pos`-datakilden:

- `PosInbound`
- `PosOutbound`

##### <a name="availquantity-calculated-measure"></a>Beregnet måling for AvailQuantity

Den beregnede måling for `AvailQuantity` konfigureres for `pos`-datakilden som vist i følgende tabel.

| Kalkulationstype | Datakilde | Fysisk måling |
|---|---|---|
| Addition | `fno` | `AvailPhysical` |
| Addition | `pos` | `PosInbound` |
| Subtraktion | `pos` | `PosOutbound` |

#### <a name="configuration-of-the-iom-data-source"></a>Konfiguration af "iom"-datakilden

Der konfigureres følgende fysiske mål for `iom`-datakilden (Intelligent Order Management):

- `OnOrder`
- `OnHand`

#### <a name="configuration-of-the-erp-data-source"></a>Konfiguration af "erp"-datakilden

Der konfigureres følgende fysiske mål for `erp`-datakilden (Enterprise Resource Planning):

- `Unrestricted`
- `QualityInspection`

### <a name="partition-configuration"></a>Partitionskonfiguration

I følgende tabel vises standardkonfigurationen af partitioner.

| Basisdimension | Hierarki |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |

### <a name="index-configuration"></a>Indekskonfiguration

I følgende tabel vises standardkonfigurationen af indekser.

| Sætnummer | Dimension | Hierarki |
|---|---|---|
| 1 | `ColorId` | 1 |
| 1 | `SizeId` | 2 |
| 1 | `StyleId` | 3 |

### <a name="reservation-configuration"></a>Konfiguration af reservationer

I dette afsnit beskrives standardkonfigurationen af reservationer.

#### <a name="reservation-mapping"></a>Reservationstilknytning

I følgende tabel vises standardtilknytningen for reservationer.

| Datakilde for fysisk måling | Fysisk måling | Tilgængelig for reservations datakilde | Tilgængelig for beregnet måling for reservation |
|---|---|---|---|
| `iv` | `SoftReservOrdered` | `iv` | `AvailableToReserve` |

#### <a name="reservation-hierarchy"></a>Reservationshierarki

I følgende tabel vises standardhierarkiet for reservationer.

| Basisdimension | Hierarki |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |
| `StyleId` | 5 |
| `BatchId` | 6 |
| `SerialId` | 7 |
| `StatusId` | 8 |
| `LicensePlateId` | 9 |
| `WMSLocationId` | 10 |
| `WMSPalletId` | 11 |
| `ConfigId` | 12 |
| `VersionId` | 13 |
| `CustomDimension1` | 14 |
| `CustomDimension2` | 15 |
| `CustomDimension3` | 16 |
| `CustomDimension4` | 17 |
| `CustomDimension5` | 18 |
| `CustomDimension6` | 19 |
| `CustomDimension7` | 20 |
| `CustomDimension8` | 21 |
| `CustomDimension9` | 22 |
| `CustomDimension10` | 23 |
| `CustomDimension11` | 24 |
| `CustomDimension12` | 25 |
| `ExtendedDimension1` | 26 |
| `ExtendedDimension2` | 27 |
| `ExtendedDimension3` | 28 |
| `ExtendedDimension4` | 29 |
| `ExtendedDimension5` | 30 |
| `ExtendedDimension6` | 31 |
| `ExtendedDimension7` | 32 |
| `ExtendedDimension8` | 33 |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

