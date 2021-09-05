---
title: Reservationer for lagersynlighed
description: I dette emne beskrives, hvordan du kan konfigurere reservationsfunktionen til at oprette reservationer, forbruge reservationer og/eller annullere reservationen af angivne lagerantal ved hjælp af Lagersynlighed.
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
ms.openlocfilehash: 6c87018cbfbe22fbbc441a1a23aee0ac44af9ddc
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/13/2021
ms.locfileid: "7345143"
---
# <a name="inventory-visibility-reservations"></a>Reservationer for lagersynlighed

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

I dette emne beskrives, hvordan du kan konfigurere reservationsfunktionen til at oprette reservationer, forbruge reservationer og/eller annullere reservationen af angivne lagerantal ved hjælp af Lagersynlighed.

Reservationer markerer et antal lagervarer, der skal bruges i fremtiden. Når du opretter en reservation, forhindrer systemet, at andre ordrer reserverer eller bruger de reserverede varer, indtil reservationen enten bliver forbrugt eller annulleret. Reservationer oprettes, forbruges og annulleres ved hjælp af API-kald til tjenesten Lagersynlighed.

Du kan vælge at oprette Microsoft Dynamics 365 Supply Chain Management (og andre tredjepartssystemer) for automatisk at modkontere det antal, der er reserveret ved hjælp af Lagersynlighed. Det modkonterede antal slettes fra reservationsposterne i Lagersynlighed.

Når du aktiverer reservationsfunktionen, bliver Supply Chain Management automatisk klar til at modpostere reservationer, der foretages ved hjælp af Lagersynlighed.

> [!NOTE]
> Modkonteringsfunktionen kræver Supply Chain Management version 10.0.22 eller senere. Hvis du vil bruge reservationer for Lagersynlighed, anbefales det, at du venter, indtil du har opgraderet Supply Chain Management til version 10.0.22 eller senere.

## <a name="turn-on-the-reservation-feature"></a>Aktivere reservationsfunktionen

Hvis du vil aktivere reservationsfunktionen, skal du følge disse trin.

1. I Power Apps skal du åbne **Lagersynlighed**.
1. Åbn siden **Konfiguration**.
1. Aktivér funktionen **OnHandReservation** under fanen *Funktionsstyring*.
1. Log på Supply Chain Management.
1. Gå til **Lagerstyring \> Opsætning \> Parametre for integration af lagersynlighed**.
1. Angiv indstillingen **Aktivér reservationsmodkonto** til **Ja** under *Reservationsmodkonto*.

## <a name="use-the-reservation-feature-in-inventory-visibility"></a>Brug reservationsfunktionen i Lagersynlighed

Når du kalder reservations-API'en, markerer systemet reservationen for de angivne varer og mængder. Du skal definere et reservationshierarki og bogføre anmodninger, der svarer til dette reservationshierarki. Reservationerne kan derefter foretages ved at kalde reservations-API'erne direkte.

### <a name="configure-the-reservation-hierarchy"></a>Konfigurere reservationshierarkiet

Reservationshierarkiet beskriver den dimensionsrækkefølge, der skal angives, når der foretages reservationer. Det fungerer på samme måde, som indekshierarkiet fungerer i forbindelse med forespørgsler om disponibel lagerbeholdning.

Reservationshierarkiet kan afvige fra indekshierarkiet. Dette afhængighedsforhold gør det muligt at implementere kategoristyring, hvor brugerne kan opdele dimensionerne for at angive detaljerede krav og kunne foretage mere præcise reservationer.

Hvis du vil konfigurere et foreløbigt reservationshierarki i Power Apps, skal du åbne siden **Konfiguration** og derefter konfigurere reservationshierarkiet under fanen **Tilknytning af foreløbig reservation** ved at tilføje og/eller redigere dimensioner og deres hierarkiniveauer.

### <a name="call-the-reservation-api"></a>Kalde reservations-API'en

Reservationer foretages i tjenesten Lagersynlighed ved at sende en POST-anmodning til tjenestens URL-adresse, f.eks. `/api/environment/{environment-ID}/onhand/reserve`.

I forbindelse med en reservation skal anmodningsteksten indeholde et organisations-id, et produkt-id, reserverede antal og dimensioner. Anmodningen genererer et entydigt reservations-id for hver reservationspost. Reservationsposten indeholder den entydige kombination af produkt-id'et og dimensionerne.

Her er et eksempel på anmodningsteksten til orientering.

```json
# Url
# replace {RegionShortName} and {EnvironmentId} with your value
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand/reserve

# Method
Post

# Header
# replace {access_token} with the one get from security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red",
        "SizeId": "small"
    },
    "quantityDataSource": "iv",
    "modifier": "SoftReservOrdered",
    "quantity": 1,
    "ifCheckAvailForReserv": true
}
```

## <a name="offset-reservations-in-supply-chain-management"></a>Modkontere reversationer i Supply Chain Management

For lagertransaktionsstatusser, der omfatter en angivet modkontomodifikator for reservationer, modkonteres den tilsvarende reservationspost i transaktionsopdateringen, når følgende betingelser er opfyldt:

- Reservations-id'et for lagertransaktionen svarer til reservations-id'et for reservationsposten i tjenesten Lagersynlighed.
- Dimensions-id'et for lagertransaktionen svarer til dimensionerne for reservationsposten i tjenesten Lagersynlighed.
- Ændringer i lagerposteringsstatus udløser modkonteringer for reservationer, når lagerposteringsstatus afspejler, at en ordreproces er fuldført eller sprunget over.

Det modkonterede antal følger det lagerantal, der er angivet i lagerposteringerne. Modkonteringen træder ikke i kraft, hvis der ikke er et reserveret antal tilbage i tjenesten Lagersynlighed.

> [!NOTE]
> Modkontofunktionen er tilgængelig fra og med version 10.0.22

### <a name="set-up-the-reserve-offset-modifier"></a>Konfigurere modkontomodifikatoren for reservationer

Modkontomodifikatoren for reservationer bestemmer det stadiet for ordrebehandlingen, der udløser modkonteringer. Stadiet spores af ordrens lagerposteringsstatus. Hvis du vil konfigurere modkontomodifikatoren for reservationer, skal du følge disse trin.

1. Gå til **Lagerstyring \> Opsætning \> Parametre for integration af lagersynlighed \> Reservationsmodkonto**.
1. Angiv feltet **Modkontomodifikator for reservationer** til en af følgende værdier:

    - *I bestilling* – For statussen *I transaktion* sender en ordre en anmodning om modkontering, når den oprettes.
    - *Reserver* – For statussen *Reservér bestilt transaktion* sender en ordre en anmodning om modkontering, når den reserveres, plukkes, følgesedlen bogføres eller faktureres. Anmodningen udløses kun én gang for det første trin, når den nævnte proces finder sted.

### <a name="set-up-reservation-ids"></a>Konfigurere reservations-id'er

Reservations-id'et markerer en reservationspost entydigt i Lagersynlighed. I Supply Chain Management placerer brugere reservationer på ordrelinjer for at markere modkontoen for den tilsvarende reservationspost.

Hvis du vil konfigurere reservations-id'er i Supply Chain Management, skal følge disse trin.

1. Åbn en salgsordre (f.eks. fra siden **Alle salgsordrer**).
1. I oversigtspanelet **Salgsoprdrelinjer** skal du vælge en ordrelinje.
1. I oversigtspanelet **Salgsordrelinjer** skal du vælge **Opdater linje \> Lager \> Integration af Lagersynlighed** på værktøjslinjen.
1. Angiv de relevante reservations-id'er.

Ændringen af lagerstatus stemmer overens med opsætningen af modkontomodifikatoren.
