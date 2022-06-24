---
title: Ændringsplaner for disponibelt antal og disponibel til tilsagn i lagersynlighed
description: Denne artikel indeholder en beskrivelse af, hvordan du kan planlægge fremtidige ændringer i den disponible beholdning og beregne DTT-mængder (disponibel til tilsagn).
author: yufeihuang
ms.date: 05/11/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-03-04
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 4a0edeedfe42b43ef36c8ca091b01eef815f3632
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856187"
---
# <a name="inventory-visibility-on-hand-change-schedules-and-available-to-promise"></a>Ændringsplaner for disponibelt antal og disponibel til tilsagn i lagersynlighed

[!include [banner](../includes/banner.md)]

Denne artikel indeholder en beskrivelse af, hvordan du kan konfigurere funktionen *Ændringsplan for disponibelt antal*, så du kan planlægge fremtidige ændringer i den disponible beholdning og beregne DTT-mængder (disponibel til tilsagn). DTT er antallet af en vare, der er tilgængelig og kan være lovet til en kunde i den næste periode. Brug af denne beregning kan øge ordreopfyldelsesfunktionaliteten væsentligt.

For mange producenter, detailforhandlere eller sælgere er det ikke nok blot at vide, hvad der aktuelt er disponibelt. De skal have fuld synlighed af fremtidig tilgængelighed. I denne fremtidige tilgængelighed skal der tages højde for fremtidig forsyning, fremtidig efterspørgsel og DTT.

## <a name="enable-and-set-up-the-features"></a><a name="setup"></a>Aktivere og konfigurere funktionerne

Før du kan bruge DTT, skal du konfigurere en eller flere beregnede målinger for at beregne DTT-mængderne. Du skal også aktivere funktionen og konfigurere DTT-indstillinger i Microsoft Power Apps.

### <a name="set-up-calculated-measures-for-atp-quantities"></a>Konfigurere beregnede målinger for DTT-mængder

Det *beregnede DTT-målepunkt* er en foruddefineret beregnet måling, der typisk bruges til at finde det disponible antal, der aktuelt er tilgængeligt. *Leveringsantallet* er summen af antal for disse fysiske målinger, der har modifikatortypen *addition*, og *efterspørgselsantallet* er summen af antal fysiske målinger, der har modifikatortypen *subtraktion*.

Du kan tilføje flere beregnede målinger til beregning af flere DTT-mængder. Det samlede antal distinkte fysiske målinger på tværs af alle beregnede DTT-målinger skal være mindre end ni.

> [!IMPORTANT]
> En beregnet måling er en komposition af fysiske målinger. Formlen kan kun indeholde fysiske målinger uden dubletter, ikke beregnede målinger.

Du kan f.eks. konfigurere følgende beregnet måling:

**On-hand-available** = (*PhysicalInvent* + *OnHand* + *Unrestricted* + *QualityInspection* + *Inbound*) – (*ReservPhysical* + *SoftReservePhysical* + *Outbound*)

Summen (*PhysicalInvent* + *OnHand* + *Unrestricted* + *QualityInspection* + *Inbound*) repræsenterer forsyning, og summen (*ReservPhysical* + *SoftReservePhysical* + *Outbound*) repræsenterer efterspørgsel. Den beregnede måling kan derfor læses på følgende måde:

**On-hand-available** = *Forsyning* – *Efterspørgsel*

Du kan tilføje endnu en beregnet måling for at beregne det **disponible fysiske** DTT-antal.

**On-hand-physical** = (*PhysicalInvent* + *OnHand* + *Unrestricted* + *QualityInspection* + *Inbound*) – (*Outbound*)

Der er otte distinkte fysiske målinger på tværs af disse to DTT-beregnede målinger: *PhysicalInvent*, *OnHand*, *Unrestricted*, *QualityInspection*, *Inbound*, *ReservPhysical*, *SoftReservePhysical* og *Outbound*.

Du kan finde flere oplysninger beregnede målinger i [Beregnede målinger](inventory-visibility-configuration.md#calculated-measures).

### <a name="turn-on-the-on-hand-change-schedule-feature-and-configure-atp-settings"></a>Aktivere funktionen Ændringsplan for disponibelt antal og konfigurere indstillinger for DTT

Følg disse trin for at aktivere funktionen *Ændringsplan for disponibelt antal* i Power Apps og konfigurere DTT-indstillingerne.

1. Log på Power Apps, og åbn Lagersynlighed.
1. Åbn siden **Konfiguration**.
1. Aktivér funktionen **OnhandChangeSchedule** under fanen *Funktionsstyring*.
1. Vælg fanen **DTT-indstilling**.
1. Når du forespørger på Lagersynlighed, vil den give et resultat, der inkluderer hver enkelt DTT-beregnet måling, som du tilføjer her. Vælg **Tilføj** for at tilføje en ny beregnet måling for DTT.
1. Angiv følgende felter:

    - **Datakilde** – Vælg den datakilde, der er tilknyttet den beregnede måling.
    - **Beregnet måling** – Vælg den beregnede måling, der er tilknyttet den valgte datakilde, og som du vil bruge til at finde det aktuelt tilgængelige disponible antal.
    - **Planlægningsperiode** – Angiv det antal dage, som brugere kan se og sende planlagte ændringer i, når den valgte beregnede måling bruges. Brugere, som forespørger på lageroplysninger, vil få lagerbeholdning, planlagte ændringer i lagerbeholdningen og DTT for hver dag i denne periode med start fra dags dato. Vælg et heltal mellem 1 og 7.

    > [!IMPORTANT]
    > Planlægningsperioden indeholder dags dato. Brugerne kan derfor planlægge ændret lagerbeholdning til enhver dato fra dags dato (den dag, ændringen afsendes) til (planlægningsperiode – 1) dage senere.

1. Vælg **Gem**.
1. Gentag trin 5 til 7, indtil du har tilføjet alle de beregnede målinger, du kræver til DTT.
1. Når du er færdig med at konfigurere alle de nødvendige indstillinger, skal du vælge **Opdater konfiguration**.

Du kan finde flere oplysninger i [Fuldføre og opdatere konfigurationen](inventory-visibility-configuration.md).

## <a name="how-the-on-hand-change-schedule-and-atp-calculations-work"></a>Sådan fungerer ændringsplan for disponibelt antal og DTT-beregninger

En *ændringsplan for disponibelt antal* fastlægger de forventede datoer og antal for planlagte ændringer i det disponible antal. Du kan sende en ændringsplan for disponibelt antal til Lagersynlighed, forudsat at datoerne ligger inden for den periode, der er defineret i indstillingen **Planlægningsperiode** (se afsnittet [Aktivere og konfigurer funktionerne](#setup)). Brugere, som forespørger på lageroplysninger, vil få lagerbeholdning, planlagte ændringer i lagerbeholdningen og DTT for hver dag i denne periode.

Planlagte ændringer er først ikke-allokerede og påvirker derfor ikke det faktiske disponible antal i systemet. Hvis du vil bekræfte ændringerne, skal du sende en *ændringshændelse for disponibelt antal*, som opdaterer det faktiske disponible antal. Du skal derefter tilbageføre den planlagte ændring ved at sende en plan for ændring af beholdningen for et tilsvarende negativt antal.

Du kan f.eks. afgive en ordre på 10 cykler og forvente, at den ankommer i morgen. Derfor sender du en ændringsplan for disponibelt antal, der har et indgående antal på 10, og som er dateret til i morgen. Når ordren ankommer den næste dag, skal du føje cyklerne til din fysiske lagerbeholdning. Du skal derefter bekræfte ændringen i systemet for at opdatere det faktiske disponible antal. For at bekræfte ændringen skal du sende en ændringshændelse for disponibelt antal, der har et indgående antal på 10. Du skal derefter tilbageføre den planlagte ændring ved at sende en ændringsplan for disponibelt antal, der har et indgående antal på -10.

Når du forespørger på disponible antal og DTT-mængder i Lagersynlighed, returnerer den følgende oplysninger for hver dag i planlægningsperioden:

- **Dato** – Den dato, som resultatet gælder for. Tidszonen er Coordinated Universal Time (UTC).
- **Disponibelt antal** – Det faktiske disponible antal for den angivne dato. Denne beregning foretages i henhold til den DTT-beregnede måling, der er konfigureret til Lagersynlighed.
- **Planlagt forsyning** – Summen af alle planlagte indgående antal, der ikke er fysisk disponible til direkte forbrug eller forsendelse på den angivne dato.
- **Planlagt efterspørgsel** – Summen af alle planlagte udgående antal, der ikke er forbrugt eller afsendt på den angivne dato.
- **DTT-antal** – Det minimum projekterede disponible antal, der er tilgængeligt fra den angivne dato til slutningen af planlægningsperioden. Dette antal omfatter alle planlagte reguleringer af antal. Det er det maksimale antal, der kan loves på den aktuelle dato for levering eller forbrug den pågældende dag.

Hvis dags dato f.eks. er 1. februar 2022, og planlægningsperioden er 7, kan brugerne sende planlagte ændringer i disponibelt antal, der forventes at finde sted fra 1. februar til og med 7. februar 2022. I dette tilfælde beregnes DTT-antallet for 3. februar f.eks. på grundlag af den disponible beholdning for den pågældende dag og de planlagte antal fra 3. februar til og med 7. februar.

## <a name="example"></a>Eksempel

Følgende eksempel viser, hvordan en række planlagte ændringer i antal påvirker de disponible antal og DTT-antal, som Lagersynlighed rapporterer. Det viser også, hvordan du kan bekræfte en planlagt ændring, hvordan en bekræftet planændring påvirker resultaterne, og hvad der kan ske, hvis du ikke bekræfter en planlagt ændring.

Resultaterne i dette eksempel viser en *projekteret disponibel* værdi. Denne værdi omfatter alle planlagte opdateringer til illustrationsformål, men vil ikke blive rapporteret, når du forespørger på Lagersynlighed.

1. Følgende indstillinger konfigureres for systemet på siden **DTT-indstilling** i Power Apps:

    - **Beregnet DTT-måling** – Du har en beregnet måling med navnet *Disponibel*. Den beregnes som *Disponibel = Forsyning – Efterspørgsel*. Du kan vælge målingen her.
    - **Planlægningsperiode** – Du vælger *7*.

1. Følgende betingelser gælder også:

    - Dags dato er 1. februar 2022.
    - Det aktuelle disponible antal er 20.

1. For dags dato (1. februar 2022) sender du et planlagt efterspørgselsantal på 3 til Lagersynlighed. Det betyder, at det forventede disponible antal er 17. Resultatet vises i følgende tabel.

    | Dato | Disponibel | Planlagt forsyning | Planlagt efterspørgsel | Forventet disponibelt antal | DTT |
    | --- | --- | --- | --- | --- | --- |
    | 2022-02-01 | 20 | | 3 | 17 | 17 |
    | 2022-02-02 | 20 | | | 17 | 17 |
    | 2022-02-03 | 20 | | | 17 | 17 |
    | 2022-02-04 | 20 | | | 17 | 17 |
    | 2022-02-05 | 20 | | | 17 | 17 |
    | 2022-02-06 | 20 | | | 17 | 17 |
    | 2022-02-07 | 20 | | | 17 | 17 |

1. På dags dato (1. februar 2022) sender du et planlagt forsyningsantal på 10 for 3. februar 2022. Resultatet vises i følgende tabel.

    | Dato | Disponibel | Planlagt forsyning | Planlagt efterspørgsel | Forventet disponibelt antal | DTT |
    | --- | --- | --- | --- | --- | --- |
    | 2022-02-01 | 20 | | 3 | 17 | 17 |
    | 2022-02-02 | 20 | | | 17 | 17 |
    | 2022-02-03 | 20 | 10 | | 27 | 27 |
    | 2022-02-04 | 20 | | | 27 | 27 |
    | 2022-02-05 | 20 | | | 27 | 27 |
    | 2022-02-06 | 20 | | | 27 | 27 |
    | 2022-02-07 | 20 | | | 27 | 27 |

1. På dags dato (1. februar 2022) sender du følgende planlagte antalsændringer:

    - Efterspørgselsantal på 15 for 4. februar 2022
    - Forsyningsantal på 1 for 5. februar 2022
    - Forsyningsantal på 3 for 6. februar 2022

    Resultatet vises i følgende tabel.

    | Dato | Disponibel | Planlagt forsyning | Planlagt efterspørgsel | Forventet disponibelt antal | DTT |
    | --- | --- | --- | --- | --- | --- |
    | 2022-02-01 | 20 | | 3 | 17 | 12 |
    | 2022-02-02 | 20 | | | 17 | 12 |
    | 2022-02-03 | 20 | 10 | | 27 | 12 |
    | 2022-02-04 | 20 | | september | 12 | 12 |
    | 2022-02-05 | 20 | 1 | | 13 | 13 |
    | 2022-02-06 | 20 | 3 | | 16 | 16 |
    | 2022-02-07 | 20 | | | 16 | 16 |

1. På dags dato (1. februar 2022) sender du det planlagte efterspørgselsantal på 3. Du skal derfor bekræfte denne ændring, så den afspejles i den faktiske disponible beholdning. For at bekræfte ændringen skal du sende en ændringshændelse for disponibelt antal, der har et udgående antal på 3. Du skal derefter tilbageføre den planlagte ændring ved at sende en ændringsplan for disponibelt antal, der har et udgående antal på -3. Resultatet vises i følgende tabel.

    | Dato | Disponibel | Planlagt forsyning | Planlagt efterspørgsel | Forventet disponibelt antal | DTT |
    | --- | --- | --- | --- | --- | --- |
    | 2022-02-01 | 17 | | 0 | 17 | 12 |
    | 2022-02-02 | 17 | | | 17 | 12 |
    | 2022-02-03 | 17 | 10 | | 27 | 12 |
    | 2022-02-04 | 17 | | september | 12 | 12 |
    | 2022-02-05 | 17 | 1 | | 13 | 13 |
    | 2022-02-06 | 17 | 3 | | 16 | 16 |
    | 2022-02-07 | 17 | | | 16 | 16 |

1. Den næste dag (2. februar 2022) skifter planlægningsperioden fremad med én dag. Resultatet vises i følgende tabel.

    | Dato | Disponibel | Planlagt forsyning | Planlagt efterspørgsel | Forventet disponibelt antal | DTT |
    | --- | --- | --- | --- | --- | --- |
    | 2022-02-02 | 17 | | | 17 | 12 |
    | 2022-02-03 | 17 | 10 | | 27 | 12 |
    | 2022-02-04 | 17 | | september | 12 | 12 |
    | 2022-02-05 | 17 | 1 | | 13 | 13 |
    | 2022-02-06 | 17 | 3 | | 16 | 16 |
    | 2022-02-07 | 17 | | | 16 | 16 |
    | 2022-02-08 | 17 | | | 16 | 16 |

1. To dage senere (4. februar 2022) er forsyningsantallet på 10, der var planlagt til 3. februar, dog stadig ikke ankommet. Resultatet vises i følgende tabel.

    | Dato | Disponibel | Planlagt forsyning | Planlagt efterspørgsel | Forventet disponibelt antal | DTT |
    | --- | --- | --- | --- | --- | --- |
    | 2022-02-04 | 17 | | september | 2 | 2 |
    | 2022-02-05 | 17 | 1 | | 3 | 3 |
    | 2022-02-06 | 17 | 3 | | 6 | 6 |
    | 2022-02-07 | 17 | | | 6 | 6 |
    | 2022-02-08 | 17 | | | 6 | 6 |
    | 2022-02-09 | 17 | | | 6 | 6 |
    | 2022-02-10 | 17 | | | 6 | 6 |

    Som du kan se, har de planlagte (men ikke bekræftede) ændringer i den disponible beholdning ingen indflydelse på det faktiske disponible antal.

## <a name="submit-change-schedules-change-events-and-atp-queries-through-the-api"></a><a name="api-urls"></a>Sende ændringsplaner, ændringshændelser og DTT-forespørgsler via API

Du kan bruge følgende API-URL-adresser (Application Programming Interface) til at sende planlagte ændringer af disponibelt antal, ændringshændelser og forespørgsler.

| Sti | Metode | Beskrivelse |
| --- | --- | --- |
| `/api/environment/{environmentId}/onhand/changeschedule` | `POST` | Oprette én planlagt ændring af disponibelt antal. |
| `/api/environment/{environmentId}/onhand/changeschedule/bulk` | `POST` | Oprette flere planlagte ændringer af disponibelt antal. |
| `/api/environment/{environmentId}/onhand` | `POST` | Oprette en ændringshændelse for disponibelt antal. |
| `/api/environment/{environmentId}/onhand/bulk` | `POST` | Oprette flere ændringshændelser. |
| `/api/environment/{environmentId}/onhand/indexquery` | `POST` | Forespørgsel ved hjælp af `POST`-metoden. |
| `/api/environment/{environmentId}/onhand` | `GET` | Forespørgsel ved hjælp af `GET`-metoden. |

Du kan finde flere oplysninger i [Offentlige API'er til lagersynlighed](inventory-visibility-api.md).

### <a name="create-one-on-hand-change-schedule"></a>Oprette én tidsplan for ændring af disponibelt antal

Ændringsplaner for disponibelt antal oprettes ved at sende en `POST`-anmodning til den relevante URL-adresse for lagersynlighedstjenesten (se [Sende ændringsplaner, ændringshændelser og DTT-forespørgsler via API](#api-urls)). Du kan også sende masseanmodninger.

Ændringsplaner for disponibelt antal kan kun oprettes, hvis den planlagte dato er mellem dags dato og slutningen af den aktuelle planlægningsperiode. Datetime-formatet skal være *år-måned-dag* (f.eks. **2022-02-01**). Tidsformatet skal kun være nøjagtigt for dagen.

Denne API opretter en enkelt ændringsplan for disponibelt antal.

```txt
Path:
    /api/environment/{environmentId}/onhand/changeschedule
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        id: string,
        organizationId: string,
        productId: string,
        dimensionDataSource: string, # optional
        dimensions: {
            [key:string]: string,
        },
        quantitiesByDate: {
            [datetime:datetime]: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
        },
    }
```

Følgende er et eksempel på brødtekst uden `dimensionDataSource`.

```json
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red",
        "SizeId&quot;: &quot;Small"
    },
    "quantitiesByDate":
    {
        "2022-02-01": // today
        {
            "pos":{
                "inbound": 10
            }
        }
    }
}
```

### <a name="create-multiple-on-hand-change-schedules"></a>Oprette flere ændringsplaner for disponibelt antal

Denne API kan oprette flere poster samtidigt. De eneste forskelle mellem denne API og API'en for enkelthændelser er værdierne `Path` og `Body`. For denne API leverer `Body` en række af poster. Det maksimale antal poster er 512. Derfor kan masse-API til ændringsplan for disponibelt antal understøtte op til 512 planlagte ændringer ad gangen.

```txt
Path:
    /api/environment/{environmentId}/onhand/changeschedule/bulk
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    [
        {
            id: string,
            organizationId: string,
            productId: string,
            dimensionDataSource: string,
            dimensions: {
                [key:string]: string,
            },
            quantityDataSource: string, # optional
            quantitiesByDate: {
                [datetime:datetime]: {
                    [dataSourceName:string]: {
                        [key:string]: number,
                    },
                },
            },
        },
        ...
    ]
```

Følgende er et eksempel på brødtekst.

```json
[
    {
        "id": "id-bike-0001",
        "organizationId": "usmf",
        "productId": "Bike",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red",
            "SizeId&quot;: &quot;Small"
        },
        "quantitiesByDate":
        {
            "2022-02-01": // today
            {
                "pos":{
                    "inbound": 10
                }
            }
        }
    },
    {
        "id": "id-car-0002",
        "organizationId": "usmf",
        "productId": "Car",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red",
            "SizeId&quot;: &quot;Small"
        },
        "quantitiesByDate":
        {
            "2022-02-05":
            {
                "pos":{
                    "outbound": 10
                }
            }
        }
    }
]
```

### <a name="create-on-hand-change-events"></a>Oprette ændringshændelser for disponibelt antal

Ændringshændelser for disponibelt antal foretages ved at sende en `POST`-anmodning til den relevante URL-adresse for lagersynlighedstjenesten (se [Sende ændringsplaner, ændringshændelser og DTT-forespørgsler via API](#api-urls)). Du kan også sende masseanmodninger.

> [!NOTE]
> Ændringshændelser for disponibelt antal er ikke unikke for DTT-funktionaliteten, men er en del af standard-API til Lagersynlighed. Dette eksempel er medtaget, fordi hændelserne er relevante, når du arbejder med DTT. Ændringshændelser for disponibelt antal ligner ændringsreservationer, men hændelsesmeddelelser skal sendes til en anden API-URL-adresse, og hændelser bruger `quantities` i stedet for `quantityByDate` i meddelelsesteksten. Du kan finde flere oplysninger om ændringshændelser for disponibelt antal og andre funktioner i API'en til Lagersynlighed under [Offentlige API'er for Lagersynlighed](inventory-visibility-api.md#create-one-onhand-change-event).

Følgende eksempel viser en anmodningsbrødtekst, der indeholder en enkelt ændringshændelse for disponibelt antal.

```json
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "SizeId": "Big",
        "ColorId": "Red"
    },
    "quantities": {
        "pos": {
            "inbound": 10.0
        }
    }
}
```

## <a name="query-the-scheduled-on-hand-changes-and-atp-results"></a>Forespørge på de planlagte ændringer i disponibelt antal og DTT-resultater

Du kan forespørge på planlagte ændringer i disponibelt antal og DTT-resultater ved enten at sende en `POST`-anmodning eller en `GET`-anmodning til den relevante API-URL-adresse (se [Sende ændringsplaner, ændringshændelser og DTT-forespørgsler via API](#api-urls)).

I din anmodning skal du angive `QueryATP` som *true*, hvis du vil forespørge på planlagte ændringer i disponibelt antal og DTT-resultaterne.

- Hvis du sender anmodningen ved hjælp af metoden `GET`, skal du angive denne parameter i URL-adressen.
- Hvis du sender anmodningen ved hjælp af metoden `POST`, skal du angive denne parameter i anmodningsteksten.

> [!NOTE]
> Uanset om parameteren `returnNegative` er angivet til *true* eller *false* i anmodningsteksten, vil resultatet indeholde negative værdier, når du forespørger på planlagte ændringer i disponibelt antal og DTT-resultaterne. Disse negative værdier inkluderes, fordi hvis der kun planlægges behovsordrer, eller hvis forsyningsantal er mindre end behovsantal, vil de planlagte disponible ændringer i disponibelt antal være negative. Hvis negative værdier ikke er medtaget, vil resultaterne være forvirrende. Du kan finde flere oplysninger om denne indstilling, og hvordan den fungerer for andre typer forespørgsler, under [Offentlige API'er for Lagersynlighed](inventory-visibility-api.md#query-with-post-method).

```txt
Path:
    /api/environment/{environmentId}/onhand/indexquery
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        dimensionDataSource: string, # Optional
        filters: {
            organizationId: string[],
            productId: string[],
            siteId: string[],
            locationId: string[],
            [dimensionKey:string]: string[],
        },
        groupByValues: string[],
        returnNegative: boolean,
    }
```

Følgende eksempel viser, hvordan du opretter en anmodningstekst, der kan sendes til Lagersynlighed ved hjælp af `POST`-metoden.

```json
{
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["Bike"],
        "siteId": ["1"],
        "LocationId": ["11"]
    },
    "groupByValues": ["ColorId", "SizeId"],
    "returnNegative": true,
    "QueryATP":true
}
```

### <a name="get-method-example"></a>Eksempel på GET-metode

```txt
Path:
    /api/environment/{environmentId}/onhand
Method:
    Get
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Query(Url Parameters):
    groupBy
    returnNegative
    [Filters]
```

I følgende eksempel vises, hvordan du opretter en URL-adresse til anmodning som en `GET`-anmodning.

```txt
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand?organizationId=usmf&productId=Bike&SiteId=1&LocationId=11&groupBy=ColorId,SizeId&returnNegative=true&QueryATP=true
```

Resultatet af denne `GET`-anmodning er nøjagtigt det samme som resultatet af `POST`-anmodningen i forrige eksempel.

### <a name="query-result-example"></a>Eksempel på forespørgselsresultat

Begge ovenstående eksempler på forespørgsler kan give følgende svar. I dette eksempel er systemet konfigureret med følgende indstillinger:

- **Beregnet DTT-måling:** *iv.onhand = pos.inbound – pos.outbound*
- **Planlægningsperiode:** *7*

Her er et eksempel på svarteksten.

```json
[
    {
        "quantitiesByDate": {
            "2022-02-02T00:00:00": {
                "pos": {
                    "outbound": 5,
                    "inbound": 0,
                },
                "iv": {
                    "onhand": -5,
                },
            },
            "2022-02-06T00:00:00": {
                "pos": {
                    "inbound": 7,
                    "outbound": 0,
                },
                "iv": {
                    "onhand": 7,
                },
            }
        },
        "atpQuantities": {
            "2022-02-01T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-02T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-03T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-04T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-05T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-06T00:00:00Z": {
                "iv": {
                    "onhand": 12.0
                }
            },
            "2022-02-07T00:00:00Z": {
                "iv": {
                    "onhand": 12.0
                }
            }
        },
        "productId": "Bike ",
        "dimensions": {
            "ColorId": "Red",
            "SizeId": "Big",
            "siteid": "1",
            "locationid": "11"
        },
        "quantities": {
            "pos": {
                "inbound": 10.0,
                "outbound": 0,
            },
            "iv": {
                "onhand": 10.0,
            }
        }
    }
]
```
