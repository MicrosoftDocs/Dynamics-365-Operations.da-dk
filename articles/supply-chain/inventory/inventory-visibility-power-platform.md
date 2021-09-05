---
title: Appen Lagersynlighed
description: Dette emne beskriver, hvordan du bruger appen Lagersynlighed.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: cc09dd82547ec42041889e9a96662cd17549a3ea
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344996"
---
# <a name="inventory-visibility-app"></a>Appen Lagersynlighed

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Dette emne beskriver, hvordan du bruger appen Lagersynlighed.

Lagersynlighed indeholder en modelbaseret app til visualisering. Appen indeholder tre sider: **Konfiguration**, **Operationel synlighed** og **Lageroversigt**. Den har følgende funktioner:

- Den leverer en brugergrænseflade (UI) til konfiguration af disponibel lagerbeholdning og konfiguration af foreløbige reservationer.
- Den understøtter forespørgsler om disponibel lagerbeholdning i realtid for forskellige dimensionskombinationer.
- Den indeholder en brugergrænseflade til bogføring af reservationsanmodninger.
- Den tilbyder en tilpasset visning af den disponible lagerbeholdning for produkter sammen med alle dimensioner

## <a name="prerequisites"></a>Forudsætninger

Før du går i gang, skal du installere og konfigurere tilføjelsesprogrammet Lagersynlighed som beskrevet i [Konfigurere lagersynlighed](inventory-visibility-setup.md).

## <a name="configuration"></a><a name="configuration"></a>Variantkonfiguration

På siden **Konfiguration** kan du konfigurere konfigurationen af disponibel lagerbeholdning og konfigurationen af foreløbige reservationer. Når tilføjelsesprogrammet er installeret, indeholder standardkonfigurationen værdien fra Microsoft Dynamics 365 Supply Chain Management (datakilden `fno`). Du kan gennemse standardindstillingen. Afhængigt af forretningsbehovene og det eksterne systems krav til lagerbogføring kan du desuden redigere konfigurationen i [Dataverse](/powerapps/maker/common-data-service/data-platform-intro) for at standardisere, hvordan lagerændringer kan bogføres, organiseres og forespørges på på tværs af flere systemer.

### <a name="define-data-sources"></a>Definere datakilder

Du kan definere hver *datakilde*, som du vil integrere i Lagersynlighed. Lagersynlighed understøtter integration med forskellige datakilder, som f.eks. dit POS-system, Supply Chain Management og andre eksterne systemer. Supply Chain Management er som standard konfigureret som standarddatakilde (`fno`) i Lagersynlighed.

Hvis du vil tilføje en datakilde, skal du følge disse trin.

1. Log på Power Apps-miljøet, og åbn **Lagersynlighed**.
1. Åbn siden **Konfiguration**.
1. Vælg **Ny datakilde** under fanen **Datakilde** for at tilføje en datakilde.

> [!NOTE]
> Når du tilføjer en datakilde, skal du sørge for at validere datakildens navn, fysiske målinger og dimensionstilknytninger, før du opdaterer konfigurationen af tjenesten Lagersynlighed. Du kan ikke ændre disse indstillinger, når du har valgt **Opdater konfiguration**.

### <a name="set-up-dimension-mappings"></a>Konfigurere dimensionstilknytninger

Lagersynlighed indeholder en liste over basisdimensioner, der kan tilknyttes fra dimensionerne for datakilden. Der er 33 tilgængelige dimensioner ved tilknytning.

- Hvis du bruger Supply Chain Management som en af datakilderne, knyttes der som standard 13 dimensioner til standarddimensionerne for Supply Chain Management. 12 andre dimensioner (`inventDimension1` til `inventDimension12`) tilknyttes brugerdefinerede dimensioner i Supply Chain Management. De resterende otte dimensioner er udvidede dimensioner, du kan knytte til eksterne datakilder.
- Hvis du ikke bruger Supply Chain Management som en af datakilderne, kan du frit tilknytte dimensionerne. I følgende tabel vises hele listen over tilgængelige dimensioner.

> [!NOTE]
> Hvis dimensionen ikke findes på standarddimensionslisten, og du bruger en ekstern datakilde, anbefales det at bruge `ExtendedDimension1` til `ExtendedDimension8` til at udføre tilknytningen.

| Dimensionstype | Dimensionens navn |
|---|---|
| Produkt | `ColorId` |
| Produkt | `SizeId` |
| Produkt | `StyleId` |
| Produkt | `ConfigId` |
| Sporing | `BatchId` |
| Sporing | `SerialId` |
| Adresse | `LocationId` |
| Adresse | `SiteId` |
| Lagerstatus | `StatusId` |
| Lagerstedsspecifik | `WMSLocationId` |
| Lagerstedsspecifik | `WMSPalletId` |
| Lagerstedsspecifik | `LicensePlateId` |
| Anden | `VersionId` |
| Lager (Brugerdefineret) | `InventDimension1` til `InventDimension12` |
| Anden | `ExtendedDimension1` til `ExtendedDimension8` |

Hvis du vil tilføje dimensionstilknytninger, skal du følge disse trin.

1. Log på Power Apps-miljøet, og åbn **Lagersynlighed**.
1. Åbn siden **Konfiguration**.
1. Under fanen **Datakilde** i sektionen **Dimensionstilknytninger** skal du vælge **Tilføj** for at tilføje dimensionstilknytninger.
1. Angiv kildedimensionen i feltet **Dimensionsnavn**.
1. Vælg den dimension i Lagersynlighed, du vil tilknytte, i feltet **Til basisdimension**.
1. Vælg **Gem**.

![Tilføjelse af dimensionstilknytninger](media/inventory-visibility-dimension-mapping.png "Tilføjelse af dimensionstilknytninger")

Hvis datakilden f.eks. indeholder en produktfarvedimension, kan du knytte den til basisdimensionen `ColorId` for at tilføje en brugerdefineret dimension for `ProductColor` i datakilden `exterchannel`. Den knyttes derefter til `ColorId`-basisdimensionen.

## <a name="create-a-physical-measure"></a>Oprette en fysisk måling

Når en datakilde bogfører en lagerændring til Lagersynlighed, bogføres ændringen ved hjælp af *fysiske målinger*. Fysiske målinger er modifikatorer, der afspejler statusser for de opsummerede lagerposteringer. Forespørgsler kan baseres på de fysiske målinger.

Lagersynlighed indeholder en liste over fysiske standardmålinger. Disse fysiske standardmålinger hentes fra lagertransaktionens statusser på siden **Liste over disponibel lagerbeholdning** i Supply Chain Management (**Lagerstyring \> Forespørgsler og rapport \> Liste over disponibel lagerbeholdning**).

| Modifikator | Navn |
|---|---|
| `PhysicalInvent` | Fysisk lager |
| `ReservPhysical` | Fysiske reserverede |
| `AvailPhysical` | Fysisk disponibelt |
| `ReservOrdered` | Bestilte reserverede |
| `PostedQty` | Bogført antal |
| `Deducted` | Trukket |
| `Picked` | Plukket |
| `Received` | Modtaget |
| `Registered` | Registreret |
| `Arrived` | Ankommet |
| `Ordered` | Bestilt |
| `OnOrder` | I bestilling |
| `QuotationReceipt` | Tilbudstilgang |
| `QuotationIssue` | Tilbudsafgang |

Hvis datakilden er Supply Chain Management, behøver du ikke oprette de fysiske standardmålinger igen. For eksterne datakilder kan du dog oprette nye fysiske målinger ved at følge disse trin.

1. Log på Power Apps-miljøet, og åbn **Lagersynlighed**.
1. Åbn siden **Konfiguration**.
1. Vælg **Tilføj**, angiv navnet på en kildemåling i sektionen **Fysiske målinger** under fanen **Datakilde**, og gem ændringerne.

## <a name="define-the-product-hierarchy-index"></a>Definere produkthierarkiindekset

Når du opretter aggregerede dimensionsgrupper, kan du bruge Lagersynlighed til at forespørge på status for den disponible lagerbeholdning. I Lagersynlighed kaldes hver dimensionsgruppe et *indeks*. Hvert indeks svarer til et angivet nummer. Du kan bestemme, hvilke dimensioner der skal bruges til konfigurationen af indekseringen ud fra, hvordan du vil forespørge på Lagersynlighed.

Hvis du vil konfigurere produkthierarkiindekset, skal du følge disse trin.

1. Log på Power Apps-miljøet, og åbn **Lagersynlighed**.
1. Åbn siden **Konfiguration**.
1. Vælg **Tilføj** i sektionen **Dimensionstilknytninger** under fanen **Produkthierarkiindeks** for at tilføje dimensionstilknytninger.
1. Der er som standard angivet en liste over indekser. Hvis du vil redigere et eksisterende indeks, skal du vælge **Rediger** eller **Tilføj** i sektionen for det relevante indeks. Hvis du vil oprette et nyt indekssæt, skal du vælge **Nyt indekssæt**. For hver række i hvert indekssæt skal du i feltet **Dimension** vælge fra listen over basisdimensioner. Der generes automatisk værdier for følgende felter:

    - **Sætnummer** – Dimensioner, der tilhører samme gruppe (indeks), grupperes sammen og tildeles det samme sætnummer.
    - **Hierarki** – Hierarkiet bruges til at definere de understøttede dimensionskombinationer, der kan oprettes forespørgsler på i en dimensionsgruppe (indeks). Hvis du f.eks. konfigurerer en dimensionsgruppe, der har hierarkirækkefølgen *Typografi*, *Farve* og *Størrelse*, understøtter systemet resultatet af tre forespørgselsgrupper. Den første gruppe er kun typografi. Den anden gruppe er en kombination af typografi og farve. Og den tredje gruppe er en kombination af typografi, farve og størrelse. De andre kombinationer understøttes ikke.

Du kan få flere oplysninger i [Konfiguration af produktindekshierarki](inventory-visibility-configuration.md#index-configuration).

### <a name="example"></a>Eksempel

Dette afsnit indeholder et eksempel på, hvordan hierarkiet fungerer. Følgende tabel indeholder en liste over den tilgængelige lagerbeholdning i dette eksempel.

| Post | Type | Farve | Størrelse | Mængde |
|---|---|---|---|---|
| I0001 | Bred | Sort | Lille | 1 |
| I0001 | Bred | Sort | Stor | 2 |
| I0001 | Bred | Rød | Lille | 3 |
| I0001 | Regulær | Sort | Lille | 4 |
| I0001 | Regulær | Sort | Stor | 5 |
| I0001 | Regulær | Rød | Lille | 6 |
| I0001 | Regulær | Rød | Stor | 7 |

Følgende tabel viser, hvordan indekshierarkiet er konfigureret.

| Nøgle | Sætnummer | Hierarki |
|---|---|---|
| `StyleId` | 1 | 1 |
| `ColorId` | 1 | 2 |
| `SizeId` | 1 | 3 |

På baggrund af de foregående indstillinger er dimensionskombinationen i forespørgslen til Lagersynlighed *Typografi*, *Farve* og *Størrelse*. Hierarkiopsætningen giver eksterne systemer mulighed for at forespørge på den disponible lagerbeholdning på følgende måder:

- `()` – Grupperet efter alle. Her er outputtet:

    - I0001, 28

- `(StyleId)` – Gruppér efter typografi. Her er outputtet:

    - I0001, Bred, 6
    - I0001, Almindelig, 22

- `(StyleId, ColorId)` – Grupperet efter kombinationen af typografi og farve. Her er outputtet:

    - I0001, Bred, Sort, 3
    - I0001, Bred, Rød, 3
    - I0001, Almindelig, Sort, 9
    - I0001, Almindelig, Rød, 13

- `(StyleId, ColorId, SizeId)` – Grupperet efter kombinationen af typografi, farve og størrelse. Her er outputtet:

    - I0001, Bred, Sort, Lille, 1
    - I0001, Bred, Sort, Stor, 2
    - I0001, Bred, Rød, Lille, 3
    - I0001, Almindelig, Sort, Lille, 4
    - I0001, Almindelig, Sort, Stor, 5
    - I0001, Almindelig, Rød, Lille, 6
    - I0001, Almindelig, Rød, Stor, 7

## <a name="set-up-a-custom-calculated-measure"></a>Konfigurere en brugerdefineret beregnet måling

Du kan bruge Lagersynlighed til at forespørge på både fysiske målinger for lagerbeholdning og *brugerdefinerede beregnede målinger*.

Med konfigurationen kan du definere et sæt modifikatorer, der skal lægges til eller trækkes fra for at få det totale aggregerede outputantal.

1. Log på Power Apps-miljøet, og åbn **Lagersynlighed**.
1. Åbn siden **Konfiguration**.
1. Vælg **Ny beregnet måling** under fanen **Beregnet måling** for at tilføje en beregnet måling. Derefter skal du angive felterne som beskrevet i følgende tabel.

    | Felt | Værdi |
    |---|---|
    | Navn på ny beregnet måling | Angiv navnet på den beregnede måling. |
    | Datakilde | Forespørgselssystemet er en datakilde. |
    | Modifikators datakilde | Angiv datakilden for modifikatoren. |
    | Modifikator | Angiv modifikatorens navn. |
    | Modifikatortype | Vælg modifikatortypen (*Addition* eller *Subtraktion*). |

Tabellen nedenfor viser et eksempel på den brugerdefinerede beregnede måling for `MyCustomAvailableforReservation`. Yderligere oplysninger om dette eksempel finder du i [Konfiguration af datakilde](inventory-visibility-configuration.md#data-source-configuration).

| Datakilde for beregnet måling | Beregnet måling | Modifikators datakilde | Modifikator | Modifikatortype |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `Inbound` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `Outbound` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `Exteexterchannelrchannel` | `reserved` | `Subtraction` |

### <a name="set-up-a-soft-reservation-mapping"></a><a name="setup-reservation-mapping"></a>Konfigurere en foreløbig reservation

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Før du kan redigere fanen **Tilknytning af foreløbige reservationer**, skal du aktivere funktionen *OnHandReservation* under fanen **Funktionsstyring**.

Når du opretter tilknytningen fra den fysiske måling til den beregnede måling, aktiverer du tjenesten Lagersynlighed til automatisk at validere reservationens tilgængelighed ud fra den fysiske måling.

Før du konfigurerer denne tilknytning, skal de fysiske målinger, beregnede målinger og deres datakilder defineres under fanerne **Datakilde** og **Beregnet måling** på siden **Konfiguration** i Power Apps (som beskrevet tidligere i dette emne).

Hvis du vil definere tilknytningen for en foreløbig reservation, skal du følge disse trin.

1. Definer den fysiske måling, der fungerer som måling for foreløbige reservationer (f.eks. `softreservordered`).
1. Definer på siden **Konfiguration** under fanen **Beregnet måling** den beregnede måling for *tilgængelig lagerbeholdning for reservation* (AFR), der indeholder den AFR-beregningsformel, som du vil knytte til den fysiske måling. Du kan f.eks. konfigurere `availforreserv` (tilgængelig for reservation), så den knyttes til den tidligere definerede fysiske måling `softreservordered`. På den måde kan du finde ud af, hvilke antal med lagerstatussen `softreservordered`, der er tilgængelige for reservation. Følgende tabel viser AFR-beregningsformlen.

    | Modifikator | Datakilde | Målepunkt |
    |---|---|---|
    | `Addition` | `fno` | `availphysical` |
    | `Addition` | `pos` | `inbound` |
    | `Subtraction` | `pos` | `outbound` |
    | `Subtraction` | `iv` | `softreservordered` |

1. Åbn siden **Konfiguration**.
1. Konfigurer tilknytningen fra den fysiske måling til den beregnede måling under fanen **Tilknytning af foreløbig reservation**. I det forrige eksempel kan du bruge følgende indstillinger til at knytte `availforreserv` til den tidligere definerede fysiske måling `softreservordered`.

    | Datakilde for fysisk måling | Fysisk måling | Tilgængelig for reservations datakilde | Tilgængelig for beregnet måling for reservation |
    |---|---|---|---|
    | `iv` | `softreservordered` | `iv` | `availforreserv` |

### <a name="set-up-a-soft-reservation-hierarchy"></a><a name="setup-reservation-hierarchy"></a>Konfigurere et hierarki for foreløbige reservationer

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Før du kan redigere fanen **Hierarki for foreløbige reservationer**, skal du aktivere funktionen *OnHandReservation* under fanen **Funktionsstyring**.

Reservationshierarkiet beskriver den dimensionsrækkefølge, der skal angives, når der foretages reservationer. Det fungerer på samme måde, som produktindekshierarkiet fungerer i forbindelse med forespørgsler om disponibel lagerbeholdning.

Reservationshierarkiet kan afvige fra indekshierarkiet for disponibel lagerbeholdning. Dette afhængighedsforhold gør det muligt at implementere kategoristyring, hvor brugerne kan opdele dimensionerne for at angive detaljerede krav og kunne foretage mere præcise reservationer.

#### <a name="example"></a>Eksempel

Følgende reservationshierarki er konfigureret i systemet.

| Dimension | Hierarki |
|---|---|
| `ColorId` | 1 |
| `SizeId ` | 2 |
| `StyleId` | 3 |

Med dette reservationshierarki kan du foretage reservationer i følgende dimensionsrækkefølger:

- `()` – Der er ikke oplyst en dimension.
- `(ColorId)`
- `(ColorId, SizeId)`
- `(ColorId, SizeId, StyleId)`

Dimensionsrækkefølgen skal følge reservationshierarkiets rækkefølge nøje, dimension for dimension. Reservationer med `(ColorId, StyleId)` er ikke tilladt i dette eksempel, fordi denne rækkefølge ikke er defineret i reservationshierarkiet.

### <a name="control-feature-management"></a><a name="feature-switch"></a>Kontrollere funktionsstyring

Tilføjelsesprogrammet Lagersynlighed indeholder funktioner som f.eks. *OnHandReservation* og *OnHandMostSpecificBackgroundService*. Disse funktioner er som standard deaktiverede. Hvis du vil bruge dem, skal du åbne siden **Konfiguration** i Power Apps og derefter aktivere dem under fanen **Funktionsstyring**.

### <a name="complete-and-update-the-configuration"></a>Fuldføre og opdatere konfigurationen

Når du har fuldført konfigurationen, skal du foretage alle ændringer af Lagersynlighed. Hvis du vil foretage ændringer, skal du vælge **Opdater konfiguration** øverst til højre på siden **Konfiguration** i Power Apps.

Første gang du vælger **Opdater konfiguration**, beder systemet om dine legitimationsoplysninger.

- **Klient-id** – Det program-id for Azure, som du har oprettet for Lagersynlighed.
- **Lejer-id** – Dit lejer-id for Azure.
- **Klienthemmelighed** – Den programhemmelighed for Azure, som du har oprettet for Lagersynlighed.

Når du er logget på, opdateres konfigurationen i tjenesten Lagersynlighed.

> [!NOTE]
> Sørg for at validere datakildens navn, fysiske målinger og dimensionstilknytninger, før du opdaterer konfigurationen af tjenesten Lagersynlighed. Du kan ikke ændre disse indstillinger, når du har valgt **Opdater konfiguration**.

### <a name="find-the-service-endpoint"></a><a name="get-service-endpoint"></a>Finde tjenestens slutpunkt

Hvis du ikke kender det korrekte slutpunkt for tjenesten Lagersynlighed, skal du åbne siden **Konfiguration** i Power Apps og derefter vælge **Vis tjenesteslutpunkt** i øverste højre hjørne. Siden viser det korrekte slutpunkt for tjenesten.

## <a name="operational-visibility"></a>Driftssynlighed

Siden **Driftssynlighed** indeholder resultaterne af en forespørgsel om lagerbeholdning i realtid baseret på forskellige dimensionskombinationer. Når funktionen *OnHandReservation* er aktiveret, kan du også bogføre reservationsanmodninger fra siden **Driftssynlighed**.

### <a name="on-hand-query"></a>Forespørgsel om disponibel lagerbeholdning

Fanen **Forespørgsel om disponibel lagerbeholdning** viser resultaterne af en forespørgsel om den disponible lagerbeholdning i realtid.

Når du vælger fanen **Forespørgsel om disponibel lagerbeholdning**, beder systemet om dine legitimationsoplysninger, så det kan hente det ihændebærertoken, der kræves for at kunne forespørge på tjenesten Lagersynlighed. Du kan nøjes med at indsætte i ihændehavertokenet i feltet **Ihændehavertoken** og lukke dialogboksen. Du kan derefter bogføre en anmodning om en forespørgsel på disponibel lagerbeholdning.

Hvis indhændehavertokenet ikke er gyldigt, eller hvis det er udløbet, skal du indsætte et nyt i feltet **Ihændehavertoken**. Angiv de korrekte værdier for **Klient-id**, **Lejer-id**, **Klienthemmelighed**, og vælg derefter **Opdater**. Systemet henter automatisk et nyt gyldigt ihændehavertoken.

Hvis du vil bogføre en forespørgsel om disponibel lagerbeholdning, skal du angive forespørgslen i brødteksten. Brug det mønster, der er beskrevet i [Forespørgsel ved hjælp af bogføringsmetoden](inventory-visibility-api.md#query-with-post-method).

![Indstillinger for forespørgsel om disponibel lagerbeholdning](media/inventory-visibility-query-settings.png "Indstillinger for forespørgsel om disponibel lagerbeholdning")

### <a name="reservation-posting"></a>Reservationsbogføring

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Brug fanen **Reservationsbogføring** til at bogføre en reservationsanmodning. Før du kan bogføre en reservationsanmodning, skal du aktivere funktionen *OnHandReservation*. Du kan finde flere oplysninger om denne funktion i [Reservationer i Lagersynlighed](inventory-visibility-reservations.md).

Hvis du vil bogføre en reservationsanmodning, skal du angive en værdi i anmodningsteksten. Brug det mønster, der er beskrevet i [Oprette én reservationshændelse](inventory-visibility-api.md#create-one-reservation-event). Vælg derefter **Bogfør**. Hvis du vil have vist oplysninger om svaret på anmodningen, skal du vælge **Vis detaljer**. Du kan også hente værdien for **reservationId** fra svaroplysningerne.

## <a name="inventory-summary"></a>Lageroversigt

**Lageroversigt** er en tilpasset visning for *Opsummering af disponibel lagerbeholdning*. Den giver en lageroversigt for produkter sammen med alle dimensioner. Ved hjælp af **Avanceret filter**, som findes i Dataverse, kan du oprette en tilpasset visning af de rækker, der er vigtige for dig. Med de avancerede filterindstillinger kan du oprette mange forskellige visninger, fra de mest simple til de mest komplekse. De gør det også muligt at føje grupperede og indlejrede betingelser til filtrene.

Du kan få mere at vide om, hvordan du bruger **Aanceret filter**, i [Redigere eller oprette personlige visninger ved hjælp af avancerede gitterfiltre](/powerapps/user/grid-filters-advanced)

Øverst i den tilpassede visning er der tre felter: **Standarddimension**, **Brugerdefineret dimension** og **Måling**. Du kan bruge disse felter til at bestemme, hvilke kolonner der skal være synlige.

Du kan markere kolonneoverskriften for at filtrere eller sortere det aktuelle resultat.

Nederst i den tilpassede visning vises oplysninger som f.eks. "50 poster (29 valgte)" eller "50 poster". Disse oplysninger henviser til de poster, der er indlæst fra resultatet for **Avanceret filter**. Teksten "29 valgte" henviser til det antal poster, der er valgt ved hjælp af kolonneoverskriftens filter for de indlæste poster.

Nederst i visningen kan du bruge knappen **Indlæs mere** til at indlæse flere poster fra Dataverse. Standardantallet af indlæste poster er 50. Når du vælger **Indlæs mere**, indlæses de næste 1.000 tilgængelige poster i visningen. Tallet på knappen **Indlæs mere** angiver de aktuelt indlæste poster og det samlede antal poster i resultatet for **Avanceret filter**.

![Lageroversigt](media/inventory-visibility-onhand-list.png "Lageroversigt")
