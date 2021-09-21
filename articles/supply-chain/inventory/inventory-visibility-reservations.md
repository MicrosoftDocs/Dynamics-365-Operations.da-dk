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
ms.openlocfilehash: acc5d5f93f3f625892aac37780a44e221b6eb5ac
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475030"
---
# <a name="inventory-visibility-reservations"></a>Reservationer for lagersynlighed

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

I dette emne beskrives, hvordan du kan konfigurere reservationsfunktionen til at oprette reservationer, forbruge reservationer og/eller annullere reservationen af angivne lagerantal ved hjælp af Lagersynlighed.

Reservationer markerer et antal lagervarer, der skal bruges i fremtiden. Når du opretter en reservation, forhindrer systemet, at andre ordrer reserverer eller bruger de reserverede varer, indtil reservationen enten bliver forbrugt eller annulleret. Reservationer oprettes, forbruges og annulleres ved hjælp af API-kald til tjenesten Lagersynlighed.

Du kan vælge at oprette Microsoft Dynamics 365 Supply Chain Management (og andre tredjepartssystemer) for automatisk at modkontere det antal, der er reserveret ved hjælp af Lagersynlighed. Det modkonterede antal slettes fra reservationsposterne i Lagersynlighed.

Når du aktiverer reservationsfunktionen, bliver Supply Chain Management automatisk klar til at modpostere reservationer, der foretages ved hjælp af Lagersynlighed.

## <a name="turn-on-and-set-up-the-reservation-feature"></a><a name="turn-on"></a>Aktivere og konfigurere reservationsfunktionen

Hvis du vil aktivere reservationsfunktionen, skal du følge disse trin.

1. Logge på Power Apps og åbne **Lagersynlighed**.
1. Åbn siden **Konfiguration**.
1. Aktivér funktionen **OnHandReservation** under fanen *Funktionsstyring*.
1. Log på Supply Chain Management.
1. Gå til arbejdsområdet til **[funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)**, og aktiver *integration med synlighed for lager med funktionen til reservationsmodkonto* (kræver version 10.0.22 eller senere).
1. Gå til parametre for **lagerstyring \> Opsætning\> lagersynlighedsintegration**, åbn fanen **Reservationsmodkonto**, og foretag følgende indstillinger:
    - **Aktiver reservationsmodkonto** – Angiv til *Ja* for at aktivere denne funktion.
    - **Modifikator for reservation** – Vælg den lagertransaktionsstatus, der skal modpostere reservationer, der foretages ved lagersynlighed. Denne indstilling bestemmer det ordrebehandlingstrin, der udløser modregninger. Stadiet spores af ordrens lagerposteringsstatus. Vælg en af følgende muligheder:
        - *I bestilling* – For statussen *I transaktion* sender en ordre en anmodning om modkontering, når den oprettes. Modantallet er antallet for den oprettede ordre.
        - *Reserver* – For statussen *Reservér bestilt transaktion* sender en ordre en anmodning om modkontering, når den reserveres, plukkes, følgesedlen bogføres eller faktureres. Anmodningen udløses kun én gang for det første trin, når den nævnte proces finder sted. Modantallet er det antal, hvor lagertransaktionens status ændres fra *I bestilling* til *Reserveret bestilt* (eller senere status) på den tilsvarende ordrelinje.

## <a name="use-the-reservation-feature-in-inventory-visibility"></a>Brug reservationsfunktionen i Lagersynlighed

Når du kalder reservations-API'en, markerer systemet reservationen for de angivne varer og mængder. Du skal definere et reservationshierarki og bogføre anmodninger, der svarer til dette reservationshierarki. Reservationerne kan derefter foretages ved at kalde reservations-API'erne direkte.

### <a name="configure-the-reservation-hierarchy"></a>Konfigurere reservationshierarkiet

Reservationshierarkiet beskriver den dimensionsrækkefølge, der skal angives, når der foretages reservationer. Det fungerer på samme måde, som indekshierarkiet fungerer i forbindelse med forespørgsler om disponibel lagerbeholdning.

Reservationshierarkiet kan afvige fra indekshierarkiet. Dette afhængighedsforhold gør det muligt at implementere kategoristyring, hvor brugerne kan opdele dimensionerne for at angive detaljerede krav og kunne foretage mere præcise reservationer.

Hvis du vil konfigurere et foreløbigt reservationshierarki i Power Apps, skal du åbne siden **Konfiguration** og derefter konfigurere reservationshierarkiet under fanen **Foreløbig reservationshierarki** ved at tilføje og/eller redigere dimensioner og deres hierarkiniveauer.

Det forhåndsreservationshierarki skal indeholde `SiteId` og `LocationId` som komponenter, da de opbygger partitionskonfigurationen.

Få flere oplysninger om, hvordan du kan konfigurere reservationer i [Konfigurere reservationer](inventory-visibility-configuration.md#reservation-configuration).

### <a name="call-the-reservation-api"></a>Kalde reservations-API'en

Reservationer foretages i tjenesten Lagersynlighed ved at sende en POST-anmodning til tjenestens URL-adresse, f.eks. `/api/environment/{environment-ID}/onhand/reserve`.

I forbindelse med en reservation skal anmodningsteksten indeholde et organisations-id, et produkt-id, reserverede antal og dimensioner. Anmodningen genererer et entydigt reservations-id for hver reservationspost. Reservationsposten indeholder den entydige kombination af produkt-id'et og dimensionerne.

Når du kalder reservations-API'en, kan du styre valideringen af reservationen ved at angive parameteren Boolesk `ifCheckAvailForReserv` i brødteksten. Værdien `True` betyder, at valideringen er påkrævet, mens værdien `False` betyder, at valideringen ikke er nødvendig. Standardværdien er `True`.

Hvis du vil annullere en reservation eller ikke-reservere angivne lagerantal, skal du angive antallet til en negativ værdi og angive parameteren `ifCheckAvailForReserv` til `False` for at springe valideringen over.

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

### <a name="set-up-the-reservation-offset-modifier"></a>Konfigurere modkontomodifikatoren for reservationer

Hvis du ikke allerede har gjort det, skal du konfigurere reservationsmodifikatoren som beskrevet i [Aktivere og konkfigurere reservationsfunktionen](#turn-on).

### <a name="set-up-reservation-ids"></a>Konfigurere reservations-id'er

Reservations-id'et markerer en reservationspost entydigt i Lagersynlighed. I Supply Chain Management placerer brugere reservationer på ordrelinjer for at markere modkontoen for den tilsvarende reservationspost.

Hvis du vil konfigurere reservations-id'er i Supply Chain Management, skal følge disse trin.

1. Åbn en salgsordre (f.eks. fra siden **Alle salgsordrer**).
1. I oversigtspanelet **Salgsoprdrelinjer** skal du vælge en ordrelinje.
1. I oversigtspanelet **Salgsordrelinjer** skal du vælge **Opdater linje \> Lager \> Integration af Lagersynlighed** på værktøjslinjen.
1. Angiv de relevante reservations-id'er.

Ændringen af lagerstatus stemmer overens med opsætningen af modkontomodifikatoren.
