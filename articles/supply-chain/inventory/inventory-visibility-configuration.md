---
title: Konfiguration af lagersynlighed
description: Dette emne beskriver, hvordan du konfigurerer Lagersynlighed.
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
ms.openlocfilehash: 92e42b22d424ab80303d771f760cfcf0599b9f4c
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/13/2021
ms.locfileid: "7345027"
---
# <a name="inventory-visibility-configuration"></a>Konfiguration af lagersynlighed

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Dette emne beskriver, hvordan du konfigurerer Lagersynlighed.

## <a name="introduction"></a><a name="introduction"></a>Start her

Før du begynder at arbejde med Lagersynlighed, skal du fuldføre følgende konfiguration som beskrevet i dette emne:

- [Konfiguration af datakilde](#data-source-configuration)
- [Partitionskonfiguration](#partition-configuration)
- [Konfiguration af produktindekshierarki](#index-configuration)
- [Konfiguration af reservationer (valgfrit)](#reservation-configuration)
- [Eksempel på standardkonfiguration](#default-configuration-sample)

> [!NOTE]
> Du kan få vist og redigere konfigurationer for Lagersynlighed i [Microsoft Power Apps](./inventory-visibility-power-platform.md#configuration). Når konfigurationen er fuldført, skal du vælge **Opdater konfiguration** i appen.

## <a name="data-source-configuration"></a><a name="data-source-configuration"></a>Konfiguration af datakilde

Datakilden repræsenterer det system, dataene kommer fra. Eksempler omfatter `fno` (hvilket betyder "Dynamics 365 Finance and Operations-apps") og `pos` (hvilket står for "point of sale" – salgssted).

Datakildekonfigurationen omfatter følgende dele:

- Dimension (dimensionstilknytning)
- Fysisk måling
- Beregnet måling

> [!NOTE]
> Datakilden `fno` er reserveret til Dynamics 365 Supply Chain Management.

### <a name="dimension-dimension-mapping"></a><a name="data-source-configuration-dimension"></a>Dimension (dimensionstilknytning)

Formålet med dimensionskonfigurationen er at standardisere integrationen af flere systemer for bogføringshændelser og -forespørgsler baseret på dimensionskombinationer.

Lagersynlighed understøtter følgende generelle basisdimensioner.

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

### <a name="physical-measures"></a>Fysiske målinger

Fysiske målinger ændrer antallet og afspejler lagerstatussen. Du kan definere dine egne fysiske mål ud fra dine behov.

Lagersynlighed indeholder en liste over fysiske standardmål, der er knyttet til Supply Chain Management (datakilden `fno`). Følgende tabel indeholder et eksempel på fysiske målinger.

| Navn på fysisk måling | Betegnelse |
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

### <a name="calculated-measures"></a><a name="data-source-configuration-calculated-measure"></a>Beregnede målinger

Beregnede målinger udgør en brugerdefineret beregningsformel, der består af en kombination af fysiske målinger. Denne funktion gør det muligt at definere et sæt fysiske målinger, der skal tilføjes, og/eller et sæt fysiske målinger, der skal trækkes fra, så de danner den tilpassede måling.

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

Outputtet `MyCustomAvailableforReservation`, der er baseret på beregningsindstillingen i de brugerdefinerede målinger, er 100 + 50 + 80 + 90 + 30 – 10 – 20 – 60 – 40 = 220.

## <a name="partition-configuration"></a><a name="partition-configuration"></a>Partitionskonfiguration

Konfigurationen af partitionen består af en kombination af basisdimensioner. Det definerer datafordelingsmønsteret. Datahandlinger i samme partition understøtter høj ydeevne og prisen er fordelagtig. Gode partitionsmønstre kan derfor bidrage til betydelige fordele.

Lagersynlighed omfatter følgende standardkonfiguration af partitioner.

| Basisdimension | Hierarki |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |

> [!NOTE]
> Standardkonfigurationen af partitioner er kun til reference. Du behøver ikke at definere den i Lagersynlighed. I øjeblikket understøttes opgraderingen af partitionskonfigurationen ikke.

## <a name="product-index-hierarchy-configuration"></a><a name="index-configuration"></a>Konfiguration af produktindekshierarki

Lagerbeholdningsforespørgslen vil det meste af tiden ikke kun være på det højeste "totalniveau". I stedet vil du måske også at få vist resultater, der aggregeres baseret på lagerdimensionerne.

Lagersynlighed giver fleksibilitet ved at lade dig konfigurere _indekserne_. Disse indekser er baseret på en dimension eller en kombination af dimensioner. Et indeks består af et *sætnummer*, en *dimension* og et *hierarki* som defineret i følgende tabel.

| Navn | Betegnelse |
|---|---|
| Sætnummer | Dimensioner, der tilhører samme sæt (indeks), grupperes sammen, og det samme sætnummer tildeles dem. |
| Dimension | Basisdimensioner, som resultatet af forespørgslen aggregeres på. |
| Hierarki | Hierarkiet bruges til at definere de understøttede dimensionskombinationer, der kan oprettes forespørgsler på. Du kan f.eks. konfigurere en dimensionssæt med en hierarkisekvens af `(ColorId, SizeId, StyleId)`. I dette tilfælde understøtter systemet forespørgsler på fire kombinationer af dimensioner. Den første kombination er tom, den anden er `(ColorId)`, den tredje er `(ColorId, SizeId)`, og den fjerde er `(ColorId, SizeId, StyleId)`. De andre kombinationer understøttes ikke. Du kan finde flere oplysninger i eksemplet, der følger. |

### <a name="example"></a>Eksempel

Dette afsnit indeholder et eksempel på, hvordan hierarkiet fungerer.

Du har følgende varer på lageret.

| Post | ColorId | SizeId | StyleId | Mængde |
|---|---|---|---|---|
| T-shirt | Sort | Lille | Bred | 1 |
| T-shirt | Sort | Lille | Regulær | 2 |
| T-shirt | Sort | Stor | Bred | 3 |
| T-shirt | Sort | Stor | Regulær | 4 |
| T-shirt | Rød | Lille | Bred | 5 |
| T-shirt | Rød | Lille | Regulær | 6 |
| T-shirt | Rød | Stor | Regulær | 7 |

Her er indekset.

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

> [!NOTE]
> Basisdimensioner, der er defineret i partitionskonfigurationen, bør ikke defineres i indekskonfigurationer.

## <a name="reservation-configuration-optional"></a><a name="reservation-configuration"></a>Konfiguration af reservationer (valgfrit)

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Konfiguration af reservationer er påkrævet, hvis du vil bruge funktionen til foreløbig reservation. Konfigurationen består af to grundlæggende dele:

- Tilknytning af foreløbige reservationer
- Hierarki for foreløbige reservationer

### <a name="soft-reservation-mapping"></a>Tilknytning af foreløbige reservationer

Når du foretager en reservation, vil du måske gerne vide, om den disponible lagerbeholdning er tilgængelig for reservation. Valideringen er knyttet til en beregnet måling, der repræsenterer en beregningsformel for en kombination af fysiske målinger.

En reservationsmåling er f.eks. baseret på den fysiske måling `SoftReservOrdered` fra datakilden `iv` (Lagersynlighed). I dette tilfælde kan du konfigurere den beregnede måling `AvailableToReserve` for datakilden `iv` som vist her.

| Kalkulationstype | Datakilde | Fysisk måling |
|---|---|---|
| Addition | `fno` | `AvailPhysical` |
| Addition | `pos` | `Inbound` |
| Subtraktion | `pos` | `Outbound` |
| Subtraktion | `iv` | `SoftReservOrdered` |

Opret derefter en tilknytning af foreløbige reservationer for at angive en tilknytning fra reservationsmålingen `SoftReservOrdered` til den beregnede måling `AvailableToReserve`.

| Datakilde for fysisk måling | Fysisk måling | Tilgængelig for reservations datakilde | Tilgængelig for beregnet måling for reservation |
|---|---|---|---|
| `iv` | `SoftReservOrdered` | `iv` | `AvailableToReserve` |

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

### <a name="soft-reservation-hierarchy"></a>Hierarki for foreløbige reservationer

Reservationshierarkiet beskriver den dimensionsrækkefølge, der skal angives, når der foretages reservationer. Det fungerer på samme måde, som produktindekshierarkiet fungerer i forbindelse med forespørgsler om disponibel lagerbeholdning.

Reservationshierarkiet er uafhængigt af produktindekshierarkiet. Dette afhængighedsforhold gør det muligt at implementere kategoristyring, hvor brugerne kan opdele dimensionerne for at angive detaljerede krav og kunne foretage mere præcise reservationer.

Her er et eksempel på et foreløbigt reservationshierarki.

| Basisdimension | Hierarki |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |
| `StyleId` | 5 |

I dette eksempel kan du foretage reservationer i følgende dimensionsserier:

- `()` – Der er ikke angivet en dimension.
- `(SiteId)`
- `(SiteId, LocationId)`
- `(SiteId, LocationId, ColorId)`
- `(SiteId, LocationId, ColorId, SizeId)`
- `(SiteId, LocationId, ColorId, SizeId, StyleId)`

En gyldig dimensionsrækkefølge skal nøje følge reservationshierarkiet, dimension for dimension. Hierarkirækkefølgen `(SiteId, LocationId, SizeId)` er f.eks. ikke gyldig, fordi `ColorId` mangler.

## <a name="default-configuration-sample"></a><a name="default-configuration-sample"></a>Eksempel på standardkonfiguration

Under initialiseringsstadiet opretter Lagersynlighed en standardkonfiguration. Du kan ændre konfigurationen efter behov.

### <a name="data-source-configuration"></a>Konfiguration af datakilde

#### <a name="configuration-of-the-iv-data-source"></a>Konfiguration af iv-datakilden

I dette afsnit beskrives, hvordan `iv`-datakilden konfigureres.

##### <a name="physical-measures-configured-for-the-iv-data-source"></a>Fysiske mål, der er konfigureret for iv-datakilden

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

#### <a name="configuration-of-the-fno-data-source"></a>Konfiguration af fno-datakilden

I dette afsnit beskrives, hvordan `fno`-datakilden konfigureres.

##### <a name="dimension-mappings-for-the-fno-data-source"></a>Dimensionstilknytninger for fno-datakilden

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

##### <a name="physical-measures-configured-for-the-fno-data-source"></a>Fysiske målinger, der er konfigureret for fno-datakilden

Der konfigureres følgende fysiske målinger for `fno`-datakilden:

- `Ordered`
- `Arrived`
- `AvailPhysical`
- `PhysicalInvent`
- `ReservPhysical`
- `ReservOrdered`
- `OnOrder`

#### <a name="configuration-of-the-pos-data-source"></a>Konfiguration af pos-datakilden

I dette afsnit beskrives, hvordan `pos`-datakilden konfigureres.

##### <a name="physical-measures-for-the-pos-data-source"></a>Fysiske målingeer for pos-datakilden

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

#### <a name="configuration-of-the-iom-data-source"></a>Konfiguration af iom-datakilden

Der konfigureres følgende fysiske mål for `iom`-datakilden (Intelligent Order Management):

- `OnOrder`
- `OnHand`

#### <a name="configuration-of-the-erp-data-source"></a>Konfiguration af erp-datakilden

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

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

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
