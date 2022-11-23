---
title: Reservationer af Inventory Visibility
description: Denne artikel beskriver, hvordan du kan konfigurere reservationsfunktionen til at oprette reservationer, forbruge reservationer og/eller annullere reservationen af angivne lagerantal ved hjælp af Lagersynlighed.
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 0ae0589f8bac7ebf9b43cf0f3bc02680d324b29b
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762716"
---
# <a name="inventory-visibility-reservations"></a>Reservationer i Inventory Visibility

[!include [banner](../includes/banner.md)]

I denne artikel beskrives en typisk anvendelsessag til blød reservationer, og det forklares, hvordan de konfigureres i Lagersynlighed. Den indeholder oplysninger om, hvordan du kan oprette blød reservationer, modregne dem i fysisk forbrug og regulere eller ikke-reservere angivne lagerantal.

## <a name="sample-use-case-for-soft-reservation"></a>Eksempelsag til forhåndsreservation

Blød reservationer hjælper organisationer med at opnå en enkelt kilde til sandhed om tilgængelig beholdning, især under ordreopfyldningsprocessen. Denne funktionalitet er nyttig for organisationer, hvor følgende betingelser er til stede:

- Organisationen har mindst to forskellige systemer, der direkte tager udgående ordrer.
- Organisationen er meget stram og ønsker at forhindre dobbeltreservation af produktlager, hvilket kan ske, hvis flere systemer kan overbooke det sidste lager. Denne situation forhindres, når alle ordresystemer kan foretage API-opkald med instant forhåndsreservation til Lagersynlighed, hvilket giver en enkelt kilde til sandhed for tilgængeligheden af lagervarer.

[<img src="media/inventory-visibility-soft-reservation.png" alt="Inventory Visibility soft reservation." title="Forhåndsreservationer i lagersynlighed" width="720" />](media/inventory-visibility-soft-reservation.png)

I ovenstående illustration vises, hvordan forhåndsreservation fungerer, og følgende operationer fremhæves:

- Det første lagerniveau synkroniseres til synligheden af lageret fra Microsoft Dynamics 365 Supply Chain Management.
- Blød reservationer bogføres fra hver af dine bestillingskanaler eller systemer til lagersynlighed. Lagersynlighed validerer lagertilgængelighed og forsøger at foretage en forhåndsreservation. Hvis forhåndsreservationen lykkes, føjes synligheden af lageret til det forhånds reserverede antal, trækkes fra det disponible antal til reservation (AFR-antallet), og der reageres med et forhåndsreservations-id.
- På dette tidspunkt forbliver det fysiske lagerantal det samme.
- Du kan derefter synkronisere enten enkelte eller aggregerede forhåndsreservationsordrer (ordrelinjer) til Supply Chain Management for at foretage fysiske reservationer og frigive til lagerstedet eller opdatere det endelige lagerantal.
- Du kan angive, at systemet skal [modpostere reservationer](#offset-scm), når fysisk lager opdateres i Supply Chain Management.

Forhåndsreservationer oprettes, forbruges og annulleres normalt ved hjælp af API-kald til tjenesten Lagersynlighed.

> [!NOTE]
> Du kan vælge at oprette Supply Chain Management (og andre tredjepartssystemer) for automatisk at modkontere det antal, der er reserveret ved hjælp af Lagersynlighed. Det modkonterede antal slettes fra reservationsposterne i Lagersynlighed.
>
> Som standard aktiveres modposteringsfunktionen automatisk, når du aktiverer funktionen for forhåndsreservation.

## <a name="turn-on-and-set-up-the-reservation-feature"></a><a name="turn-on"></a>Aktivere og konfigurere reservationsfunktionen

Hvis du vil aktivere reservationsfunktionen, skal du følge disse trin.

1. Log på Power Apps, og åbn **Lagersynlighed**.
1. Åbn siden **Konfiguration**.
1. Aktivér funktionen **OnHandReservation** under fanen *Funktionsstyring*.
1. Log på dit Supply Chain Management-miljø.
1. Gå til arbejdsområdet til **[funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)**, og aktiver *integration med synlighed for lager med funktionen til reservationsmodkonto* (kræver version 10.0.22 eller senere).
1. Gå til parametre for **lagerstyring \> Opsætning\> lagersynlighedsintegration**, åbn fanen **Reservationsmodkonto**, og foretag følgende indstillinger:

    - **Aktiver reservationsmodkonto** – Angiv til *Ja* for at aktivere denne funktion.
    - **Modifikator for reservation** – Vælg den lagertransaktionsstatus, der skal modpostere reservationer, der foretages ved lagersynlighed. Denne indstilling bestemmer det ordrebehandlingstrin, der udløser modregninger. Stadiet spores af ordrens lagerposteringsstatus. Vælg en af følgende værdier:

        - *I bestilling* – Ordrer med statussen *I bestilling* sender en ordre en anmodning om modkontering, når den oprettes. Modantallet er antallet for den oprettede ordre (linje).
        - *Reserver* – Ordrer med status *Reserve* sender en modanmodning, når de enten er ordrereserverede eller fysisk reserverede. Når du modposterer ved statussen *Reserver*, sender ordren en modanmodning efter en eventuel ny lagerstatus, der er nærmest reserveret plukket (f.eks. pluk, følgeseddelbogføring eller faktureret). Denne funktionsmåde opstår, selvom du springer reservationen over i Supply Chain Management og fortsætter til en anden lagerstatus (f.eks. hvis du springer fra frigivelse til lagersted til pluk og pakke). Anmodningen udløses kun én gang. Hvis den er udløst ved pluk, duplikeres modkontoen ikke, når der bogføres en følgeseddel. Modantallet er det samme antal som lagertransaktionens status, når forskudt udløses (med andre ord *Reserveret bestilt*/*Reserver fysisk*, eller senere status på den tilsvarende ordrelinje).

1. Log på appen Lagerudligning, gå til **Konfigurationssiden**, og gennemse derefter standardhierarkiet for forhåndsreservationer under fanen **Forhåndsreservation**. Føj nye dimensioner til hierarkiet efter behov.
1. Få vist standardindstillingerne i afsnittet **Angiv tilknytning af forhåndsreservationer**. Som standard registreres de forhåndsreserverede lagerantal i forhold til `softreservephysical`-fysisk måling af datakilden `iv`. Den beregnede måling *Tilgængelig for reservation* er tilknyttet `availabletoreserve`. Hvis du vil opdatere den beregnede `availabletoreserve`-måling, skal du gå til siden **Konfiguration** og derefter på fanen **Beregnet måling** udvide og redigere den beregnede måleenhed.

Du kan finde flere oplysninger i [Konfiguration af Lagersynlighed](inventory-visibility-configuration.md).

> [!NOTE]
> Reservationshierarkiet beskriver den dimensionsrækkefølge, der skal angives, når der foretages reservationer. Det fungerer på samme måde, som indekshierarkiet fungerer i forbindelse med forespørgsler på lager, men det bruges uafhængigt, så brugerne kan angive dimensionsdetaljer for at foretage mere præcise reservationer.
>
> Din forhåndsreservationshierarki skal indeholde `SiteId` og `LocationId` som komponenter, da de opbygger partitionskonfigurationen for lagersynlighed.

Få flere oplysninger om, hvordan du kan konfigurere reservationer i [Konfigurere reservationer](inventory-visibility-configuration.md#reservation-configuration).

## <a name="use-the-reservation-feature-in-inventory-visibility"></a>Brug reservationsfunktionen i Lagersynlighed

Når du kalder reservations-API'en, markerer systemet reservationen for de angivne varer og mængder.

Her er et eksempelscenario og et eksempel på en API-forespørgsel. Firmaet Contoso sælger produktet D0002 (Cabinet) fra dets e-handelswebsted. En kunde placerer en salgsordre for en lille rød cabinet via webstedet. Contoso beslutter sig for at opfylde denne ordre ved at bruge følgende dimensioner:

- Organisations-id = usmf
- Sted = 1
- Lagersted = 11
- Produkt = D0002
- Farve = rød
- Størrelse = lille

Contoso har allerede oprettet en API-forbindelse til Lagersynlighed fra sit eget e-handelssystem. Når ordren modtages, udløser systemudløsende et API-opkald for at foretage en forhåndsreservation af det tidspunkt, hvor lageret er synligt.

### <a name="create-soft-reservations-using-the-reservation-api"></a>Oprette forhåndsreservationer ved hjælp af reservations-API'et

Reservationer foretages i tjenesten Lagersynlighed ved at sende en POST-anmodning til tjenestens URL-adresse, f.eks. `/api/environment/{environmentId}/onhand/reserve`.

I forbindelse med en reservation skal anmodningsteksten indeholde et organisations-id, et produkt-id, reserverede antal og dimensioner.

Når du kalder reservations-API'en, kan du styre valideringen af reservationen ved at angive parameteren Boolesk `ifCheckAvailForReserv` i brødteksten. Værdien `True` betyder, at valideringen er påkrævet, mens værdien `False` betyder, at valideringen ikke er nødvendig. Standardværdien er `True`.

Hvis du vil annullere en reservation eller ikke-reservere angivne lagerantal, skal du angive antallet til en negativ værdi og angive parameteren `ifCheckAvailForReserv` til `False` for at springe valideringen over.

Her er et eksempel på det brødtekst, der refererer til salgsordren i den foregående kontekst.

```json
# Url

#Replace {endpoint} with your system endpoint.
    {endpoint}/api/environment/{environmentId}/onhand/reserve

# Method
Post

# Header
# replace {access_token} with the one get from security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "id": "Testrequest-0005",
    "organizationId": "usmf",
    "productId": "D0002",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "red",
        "SizeId": "small"
    },
    "quantityDataSource": "iv",
    "modifier": "softreservphysical",
    "quantity": 1,
    "ifCheckAvailForReserv": true
}
```

En vellykket anmodning om forhåndsreservation returnerer et *forhåndsreservations-id* for hver reservationspost. Forhåndsreservations-id'et er ikke et entydigt id for en individuel post for forhåndsreservation, men en kombination af produkt-id'et og dimensionsværdierne, der er knyttet til anmodningen om forhåndsreservation. Du kan registrere forhåndsreservations-id'et på ordrelinjen, når du synkroniserer de reserverede ordrer til Supply Chain Management eller et andet ERP-system til modpostering.

### <a name="offset-soft-reservations-in-supply-chain-management"></a><a name="offset-scm"></a>Modkontere forhåndsreservationer i Supply Chain Management

Du kan modregne et forhåndsreserveret antal, når mængden i en ordre fysisk er fratrukket i Supply Chain Management eller et andet ERP-system. Med Lagersynlighed er der mulighed for forhåndsreservationsmodintegration med Supply Chain Management.

Hvis du vil forskyde en forhåndsreservation, skal du følge disse trin.

1. Log på Supply Chain Management.
1. Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Opret den eksterne salgsordre igen, og tilføj en salgslinje, der bruger nøjagtigt samme produkt-id, organisation, lokation, lagersted og dimensionsværdier.
1. I oversigtspanelet **Salgsordrelinjer** skal du vælge de slagslinjer, du lige har angivet, og derefter på værktøjslinen **Lager \> Reservations-id**.
1. Udfør ét af følgende trin:

    - Kopiér id'et for forhåndsreservationen i svaret på anmodningen om forhåndsreservation, og indsæt det i feltet **Reservations-id**.
    - Lad feltet **Reservations-id** være tomt, men marker afkrydsningsfeltet **Automatisk lagertjenestemodkonto**. Systemet bestemmer automatisk, hvilke produkt- og produktdimensioner der skal modposteres, baseret på vare-id og dimensionsværdier, der er angivet på den valgte linje.

1. Vælg **OK**.
1. Mens samme salgslinje stadig er valgt skal du fysisk reservere den bestilte mængde ved at vælge **Lager \> Reservation** på værktøjslinjen i oversigtspanelet **Salgsordrelinjer**.
1. Hvis du tidligere har angivet **modifikatoren for reservation** til *Reserveret*, udløses modkontoen, når ordrelinjen har statussen *Reserver fysisk* eller *Reserveret bestilt*. Et batchjob køres en gang i minuttet for at synkronisere modanmodninger fra Supply Chain Management til lagersynlighed.

> [!NOTE]
> For transaktionsstatusser, der omfatter en angivet modkontomodifikator for reservationer, modkonteres den tilsvarende reservationspost i transaktionsopdateringen, når følgende betingelser er opfyldt:
>
> - Reservations-id'et for lagertransaktionen svarer til reservations-id'et for reservationsposten i tjenesten Lagersynlighed.
> - Dimensions-id'et for lagertransaktionen svarer til dimensionerne for reservationsposten i tjenesten Lagersynlighed.
> - Ændringer i lagerposteringsstatus udløser modkonteringer for reservationer, når lagerposteringsstatus afspejler, at en ordreproces er fuldført eller sprunget over.

Det modkonterede antal følger det lagerantal, der er angivet i relevante lagerposteringer. Modkonteringen træder ikke i kraft, hvis der ikke er et reserveret antal tilbage i tjenesten Lagersynlighed.

### <a name="cancel-or-revert-a-soft-reservation"></a>Annullere eller omdanne en forhåndsreservation

Hvis en oprindelig ordrelinje annulleres eller slettes, og du skal tilbagefør den tilsvarende forhåndsreservation, skal du bogføre et negativt antal, der indeholder nøjagtigt de samme oplysninger i API-forespørgselsteksten.
