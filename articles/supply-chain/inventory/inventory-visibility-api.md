---
title: Offentlige API'er til Inventory Visibility
description: Denne artikel beskriver de offentlige API'er, der leveres via Lagersynlighed.
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 8b0b8ca261237fbb2190f2a94cc11b816ae05af5
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762828"
---
# <a name="inventory-visibility-public-apis"></a>Offentlige API'er til Inventory Visibility

[!include [banner](../includes/banner.md)]

Denne artikel beskriver de offentlige API'er, der leveres via Lagersynlighed.

Den offentlige REST-API til tilføjelsesprogrammet Lagersynlighed viser flere specifikke slutpunkter for integration. Det understøtter fire overordnede interaktionstyper:

- Bogføring af ændret lagerbeholdning i tilføjelsesprogrammet fra et eksternt system
- Angive eller tilsidesætte antal for disponibel lagerbeholdningl i tilføjelsesprogrammet fra et eksternt system
- Bogføring af reservationshændelser i tilføjelsesprogrammet fra et eksternt system
- Forespørgsel om aktuelle disponible lagerantal fra et eksternt system

I følgende tabel vises de API'er, der er tilgængelige i øjeblikket:

| Sti | metode | Beskrivelse |
|---|---|---|
| /api/environment/{environmentId}/onhand | Bogfør | [Oprette en ændringshændelse for disponibelt antal](#create-one-onhand-change-event)|
| /api/environment/{environmentId}/onhand/bulk | Bogfør | [Oprette flere ændringshændelser](#create-multiple-onhand-change-events) |
| /api/environment/{environmentId}/setonhand/{inventorySystem}/bulk | Bogfør | [Angive/tilsidesætte disponibelt antal](#set-onhand-quantities) |
| /api/environment/{environmentId}/onhand/reserve | Bogfør | [Oprette en forhåndsreservationshændelse](#create-one-reservation-event) |
| /api/environment/{environmentId}/onhand/reserve/bulk | Bogfør | [Oprette flere forhåndsreservationshændelser](#create-multiple-reservation-events) |
| /api/environment/{environmentId}/onhand/unreserve | Bogfør | [Tilbagefør én forhåndsreservationshændelse](#reverse-one-reservation-event) |
| /api/environment/{environmentId}/onhand/unreserve/bulk | Bogfør | [Tilbagefør flere forhåndsreservationshændelser](#reverse-multiple-reservation-events) |
| /api/environment/{environmentId}/onhand/changeschedule | Bogfør | [Oprette én planlagt ændring af disponibelt antal](inventory-visibility-available-to-promise.md) |
| /api/environment/{environmentId}/onhand/changeschedule/bulk | Bogfør | [Oprette flere ændringer med dato af disponibelt antal](inventory-visibility-available-to-promise.md) |
| /api/environment/{environmentId}/onhand/indexquery | Bogfør | [Forespørgsel ved hjælp af post-metoden](#query-with-post-method) (anbefalet) |
| /api/environment/{environmentId}/onhand | Hent | [Forespørgsel ved hjælp af hentningsmetoden](#query-with-get-method) |
| /api/environment/{environmentId}/onhand/exactquery | Bogfør | [Nøjagtig forespørgsel ved hjælp af POST-metoden](#exact-query-with-post-method) |
| /api/environment/{environmentId}/allocation<wbr>/allocate | Bogfør | [Oprette én fordelingshændelse](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation<wbr>/unallocate | Bogfør | [Oprette én ikke-fordelingshændelse](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation<wbr>/reallocate | Bogfør | [Oprette én omfordelingshændelse](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation<wbr>/consume | Bogfør | [Oprette én forbrugshændelse](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation<wbr>/query | Bogfør | [Resultat af forespørgselsfordeling](inventory-visibility-allocation.md#using-allocation-api) |

> [!NOTE]
> {environmentId}-delen af stien er miljø-id'et i Microsoft Dynamics Lifecycle Services.
> 
> Masse-API'en kan maksimalt returnere 512 poster for hver anmodning.

Microsoft har leveret den brugsklare anmodningssamling *Postman*. Du kan importere denne samling til softwaren *Postman* med følgende delte link: <https://www.getpostman.com/collections/95a57891aff1c5f2a7c2>.

## <a name="find-the-endpoint-according-to-your-lifecycle-services-environment"></a><a name = "endpoint-lcs"></a>Find slutpunktet i overensstemmelse med Lifecycle Services-miljøet

Mikrotjenesten for Lagersynlighed installeres på Microsoft Azure Service Fabric i flere geografier og flere områder. Der er i øjeblikket ikke et centralt slutpunkt, der automatisk kan omdirigere din anmodning til den tilsvarende geografi eller det tilsvarende område. Du skal derfor skrive oplysningerne i en URL-adresse efter følgende mønster:

`https://inventoryservice.<RegionShortName>-il<IsLandNumber>.gateway.prod.island.powerapps.com`

Områdets korte navn findes i Lifecycle Services-miljøet. I følgende tabel vises de områder, der er tilgængelige i øjeblikket.

| Azure-region        | Områdets korte navn |
| ------------------- | ----------------- |
| Det østlige Australien      | eau               |
| Det sydøstlige Australien | seau              |
| Det centrale Canada      | cca               |
| Det østlige Canada         | eca               |
| Nordeuropa        | neu               |
| Vesteuropa         | weu               |
| Det østlige USA             | eus               |
| Det vestlige USA             | wus               |
| Det sydlige Storbritannien            | suk               |
| Det vestlige Storbritannien             | wuk               |
| Østjapan          | øjp               |
| Vestjapan          | vjp               |
| Det centrale Indien       | cin               |
| Sydindien         | sin               |
| Det nordlige Schweiz   | nch               |
| Det vestlige Schweiz    | wch               |
| Det sydlige Frankrig        | sfr               |
| Østasien           | eas               |
| Sydøstasien     | seas              |
| Det nordlige Forenede Arabiske Emirater           | nae               |
| Det østlige Norge         | eno               |
| Det vestlige Norge         | wno               |
| Det vestlige Sydafrika   | wza               |
| Det nordlige Sydafrika  | nza               |

Ø-nummeret er det sted, hvor Lifecycle Services-miljøet installeres på Service Fabric. Du kan i øjeblikket ikke hente disse oplysninger fra brugersiden.

Microsoft har bygget en brugergrænseflade (UI) i Power Apps, så du kan hele hele slutpunktet for mikrotjenesten. Du kan finde flere oplysninger i [Finde tjenestens slutpunkt](inventory-visibility-configuration.md#get-service-endpoint).

## <a name="authentication"></a><a name="inventory-visibility-authentication"></a>Godkendelse

Sikkerhedstoken for platformen bruges til at kalde det offentlige API for Lagersynlighed. Du skal derfor generere et *Azure Active Directory-token (Azure AD)* ved hjælp af Azure AD-programmet. Du skal derefter bruge Azure AD-tokenet til at hente *adgangstoken* fra sikkerhedstjenesten.

Microsoft leverer den brugsklare hent token-samling *Postman*. Du kan importere denne samling til softwaren *Postman* med følgende delte link: <https://www.getpostman.com/collections/496645018f96b3f0455e>.

Hvis du vil hente et token for sikkerhedstjenesten, skal du følge disse trin.

1. Log på Azure-portalen, og brug den til at finde værdierne `clientId` og `clientSecret` for Dynamics 365 Supply Chain Management-appen.
1. Hent et Azure AD-token (`aadToken`) ved at sende en HTTP-anmodning, der har følgende egenskaber:

    - **URL:** `https://login.microsoftonline.com/${aadTenantId}/oauth2/v2.0/token`
    - **Metode:** `GET`
    - **Brødtekst (formulardata):**

        | Nøgle           | Værdi                                            |
        | ------------- | -------------------------------------------------|
        | client_id     | ${aadAppId}                                      |
        | client_secret | ${aadAppSecret}                                  |
        | grant_type    | client_credentials                               |
        | område         | 0cdb527f-a8d1-4bf8-9436-b352c68682b2/.default    |

    Du skal modtage et Azure AD-token (`aadToken`) som svar. Den skulle ligne følgende eksempel:

    ```json
    {
        "token_type": "Bearer",
        "expires_in": "3599",
        "ext_expires_in": "3599",
        "access_token": "eyJ0eX...8WQ"
    }
    ```

1. Formuler en JSON-anmodning (JavaScript Object Notation), der ligner følgende eksempel.

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type": "aad_app",
        "client_assertion": "{Your_AADToken}",
        "scope": "https://inventoryservice.operations365.dynamics.com/.default",
        "context": "{$LCS_environment_id}",
        "context_type": "finops-env"
    }
    ```

    Vær opmærksom på følgende punkter:

    - Værdien `client_assertion` skal være det Azure AD-token (`aadToken`), som du har modtaget i det forrige trin.
    - Værdien `context` skal være det Lifecycle Services miljø-id, hvor du vil implementere tilføjelsesprogrammet.
    - Angiv alle de andre værdier som vist i eksemplet.

1. Hent et adgangstoken (`access_token`) ved at sende en HTTP-anmodning, der har følgende egenskaber:

    - **URL:** `https://securityservice.operations365.dynamics.com/token`
    - **Metode:** `POST`
    - **HTTP-overskrift:** Medtag API-versionen. (Nøglen er `Api-Version`, og værdien er `1.0`).
    - **Brødtekst:** Medtag den JSON-anmodning, du oprettede i det forrige trin.

    Du skal modtage et adgangstoken (`access_token`) som svar. Du skal bruge dette token som ihændehavertoken for at kalde API'et for Lagersynlighed. Her er et eksempel.

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 3600
    }
    ```

> [!IMPORTANT]
> Når du bruger anmodningssamlingen *Postman* til at kalde offentlige API'er for lagersynlighed, skal du tilføje et ihændehaver-token for hver anmodning. Hvis du vil finde dit ihændehaver-token, skal du vælge fanen **Godkendelse** under URL-adressen til anmodningen, vælge typen **Ihændehaver-token** og kopiere det adgangstoken, der blev hentet i det sidste trin. I senere afsnit til denne artikel bruges `$access_token` til at repræsentere det token, der blev hentet i sidste trin.

## <a name="create-on-hand-change-events"></a><a name="create-onhand-change-event"></a>Oprette ændringshændelser for disponibelt antal

Der findes to API'er til oprettelse af ændringshændelser for disponibelt antal:

- Oprette én post: `/api/environment/{environmentId}/onhand`
- Oprette flere poster: `/api/environment/{environmentId}/onhand/bulk`

I følgende tabel opsummeres betydningen af hvert felt i JSON-brødteksten.

| Felt-id | Beskrivende tekst |
|---|---|
| `id` | Et entydigt id for den specifikke ændringshændelse. Dette id bruges til at sikre, at hvis genafsendelse forekommer på grund af en servicefejl, vil hændelsen ikke blive talt med to gange i systemet. |
| `organizationId` | Identifikatoren for den organisation, der er knyttet til hændelsen. Denne værdi er tilknyttet et organisations-id eller et dataområde-id i Supply Chain Management. |
| `productId` | Id'et for produktet. |
| `quantities` | Det antal, som det disponible antal skal ændres med. Hvis der f.eks. føjes 10 nye bøger til en hylde, vil denne værdi være `quantities:{ shelf:{ received: 10 }}`. Hvis der fjernes tre bøger fra hylden eller de sælges, er denne værdi `quantities:{ shelf:{ sold: 3 }}`. |
| `dimensionDataSource` | Datakilden for de dimensioner, der bruges i bogføringens ændringshændelse og forespørgslen. Hvis du angiver datakilden, kan du bruge de brugerdefinerede dimensioner fra den angivne datakilde. Lagersynlighed kan bruge dimensionskonfigurationen til at knytte de brugerdefinerede dimensioner til de generelle standarddimensioner. Hvis der ingen værdi for `dimensionDataSource` er angivet, kan du kun bruge de generelle [basisdimensioner](inventory-visibility-configuration.md#data-source-configuration-dimension) i forespørgslerne. |
| `dimensions` | Et dynamisk nøgle/værdi-par. Værdierne knyttes til nogle af dimensionerne i Supply Chain Management. Du kan dog også tilføje brugerdefinerede dimensioner (f.eks. *Kilde*) for at angive, om hændelsen kommer fra Supply Chain Management eller et eksternt system. |

> [!NOTE]
> Parametrene `siteId` og `locationId` opbygger [partitionskonfigurationen](inventory-visibility-configuration.md#partition-configuration). Du skal derfor angive dem i dimensioner, når du opretter hændelser med disponible ændringer, angiver eller tilsidesætter disponible antal eller opretter reservationshændelser.

Følgende undersektioner indeholder eksempler på, hvordan du kan bruge disse API'er.

### <a name="create-one-on-hand-change-event"></a><a name="create-one-onhand-change-event"></a>Oprette en ændringshændelse for disponibelt antal

Denne API opretter en ændringshændelse for disponibelt antal.

```txt
Path:
    /api/environment/{environmentId}/onhand
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
        dimensionDataSource: string, # Optional
        dimensions: {
            [key:string]: string,
        },
        quantities: {
            [dataSourceName:string]: {
                [key:string]: number,
            },
        },
    }
```

Følgende er et eksempel på brødtekst. I dette eksempel har virksomheden et POS-system, der behandler transaktioner i butikken og derfor foretager lagerændringer. Kunden har returneret en rød T-shirt til din butik. Du kan gengive ændringen ved at bogføre en ændringshændelse for produktet *T-shirt*. Denne hændelse øger antallet for produktet *T-shirt* med 1.

```json
{
    "id": "Test201",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensionDataSource": "pos",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "posMachineId": "0001",
        "colorId&quot;: &quot;red"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

Følgende er et eksempel på brødtekst uden `dimensionDataSource`. I dette tilfælde vil `dimensions` være [basisdimensionerne](inventory-visibility-configuration.md#data-source-configuration-dimension). Hvis `dimensionDataSource` er angivet, kan `dimensions` enten være datakildedimensionerne eller basisdimensionerne.

```json
{
    "id": "Test202",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

### <a name="create-multiple-change-events"></a><a name="create-multiple-onhand-change-events"></a>Oprette flere ændringshændelser

Denne API kan oprette ændringshændelser på samme måde som [enkelt-hændelses API](#create-one-onhand-change-event) kan. Den eneste forskel er, at denne API kan oprette flere poster samtidigt. Derfor er der forskel på `Path`- og `Body`-værdierne. For denne API leverer `Body` en række af poster. Det maksimale antal poster er 512. Derfor kan masse-API til ændringsplan understøtte op til 512 ændringshændelser ad gangen. 

En detailbutiks POS-maskine har f.eks. behandlet følgende to transaktioner:

- En returordre på én rød T-shirt
- En salgstransaktion med tre sort T-shirts

I dette tilfælde kan du medtage begge lageropdateringer i ét API-kald.

```txt
Path:
    /api/environment/{environmentId}/onhand/bulk
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
            dimensionDataSource: string, # Optional
            dimensions: {
                [key:string]: string,
            },
            quantities: {
                [dataSourceName:string]: {
                    [key:string]: number,
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
        "id": "Test203",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
            "SiteId": "Site1",
            "LocationId": "11",
            "posMachineId&quot;: &quot;0001"
            "colorId&quot;: &quot;red"
        },
        "quantities": {
            "pos": { "inbound": 1 }
        }
    },
    {
        "id": "Test204",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensions": {
            "siteId": "1",
            "locationId": "11",
            "colorId&quot;: &quot;black"
        },
        "quantities": {
            "pos": { "outbound": 3 }
        }
    }
]
```

## <a name="setoverride-on-hand-quantities"></a><a name="set-onhand-quantities"></a>Angive/tilsidesætte disponible antal

API'en for *Konfigurer disponibelt antal* tilsidesætter de aktuelle data for det angivne produkt. Denne funktion bruges typisk til opdatering af lageroptællinger. Ved den daglige lageroptælling kan en butik f.eks. finde ud af, at den faktiske beholdning for en rød T-shirt er 100. Derfor skal det indgående POS-antal opdateres til 100, uanset hvad det foregående antal var. Du kan bruge denne API til at tilsidesætte den eksisterende værdi.

```txt
Path:
    /api/environment/{environmentId}/setonhand/{inventorySystem}/bulk
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
            dimensionDataSource: string, # Optional
            dimensions: {
                [key:string]: string,
            },
            quantities: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
            modifiedDateTimeUTC: datetime,
        },
        ...
    ]
```

Følgende er et eksempel på brødtekst. Funktionsmåden for denne API er forskellig fra funktionsmåden for de API'er, der er beskrevet i afsnittet [Oprette ændringshændelser for disponibelt antal](#create-onhand-change-event) tidligere i denne artikel. I dette eksempel vil antallat for produktet *T-shirt* blive angivet til 1.

```json
[
    {
        "id": "Test204",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "posMachineId": "0001"
            "colorId": "red"
        },
        "quantities": {
            "pos": {
                "inbound": 100
            }
        }
    }
]
```

## <a name="create-reservation-events"></a>Oprette reservationshændelser

Hvis du vil bruge API'en for *Reservér*, skal du aktivere reservationsfunktionen og fuldføre reservationskonfigurationen. Yderligere oplysninger (herunder en dataflow og eksempelscenario) finder du i [Reservationskonfiguration (valgfrit)](inventory-visibility-configuration.md#reservation-configuration).

### <a name="create-one-reservation-event"></a><a name="create-one-reservation-event"></a>Oprette én reservationshændelse

Der kan foretages en reservation i forhold til de forskellige datakildeindstillinger. Hvis du vil konfigurere denne reservationstype, skal du først angive datakilden i `dimensionDataSource`-parameteren. Angiv derefter dimensionerne i forhold til dimensionsindstillingerne i måldatakilden i parameteren `dimensions`.

Når du kalder reservations-API'en, kan du styre valideringen af reservationen ved at angive parameteren Boolesk `ifCheckAvailForReserv` i brødteksten. Værdien `True` betyder, at valideringen er påkrævet, mens værdien `False` betyder, at valideringen ikke er nødvendig. Standardværdien er `True`.

Hvis du vil tilbageføre en reservation eller ikke-reservere angivne lagerantal, skal du angive antallet til en negativ værdi og angive parameteren `ifCheckAvailForReserv` til `False` for at springe valideringen over. Der findes også en dedikeret API, der ikke reserverer, til at gøre det samme. Forskellen er kun, hvordan de to API'er kaldes. Det er lettere at tilbageføre en bestemt reservationshændelse ved at bruge `reservationId` med API'en *unreserve*, der annullerer reservation. Du kan finde flere oplysninger i afsnittet [Annullere reservation af én reservationshændelse](#reverse-reservation-events).

```txt
Path:
    /api/environment/{environmentId}/onhand/reserve
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
        dimensionDataSource: string,
        dimensions: {
            [key:string]: string,
        },
        quantityDataSource: string, # optional
        quantities: {
            [dataSourceName:string]: {
                [key:string]: number,
            },
        },
        modifier: string,
        quantity: number,
        ifCheckAvailForReserv: boolean,
    }
```

Følgende er et eksempel på brødtekst.

```json
{
    "id": "reserve-0",
    "organizationId": "SCM_IV",
    "productId": "iv_postman_product",
    "quantity": 1,
    "quantityDataSource": "iv",
    "modifier": "softReservOrdered",
    "ifCheckAvailForReserv": true,
    "dimensions": {
        "siteId": "iv_postman_site",
        "locationId": "iv_postman_location",
        "colorId": "red",
        "sizeId&quot;: &quot;small"
    }
}
```

I følgende eksempel vises et korrekt svar.

```json
{
    "reservationId": "RESERVATION_ID",
    "id": "ohre~id-822-232959-524",
    "processingStatus": "success",
    "message": "",
    "statusCode": 200
}
``` 

### <a name="create-multiple-reservation-events"></a><a name="create-multiple-reservation-events"></a>Oprette flere reservationshændelser

Denne API er en bulkversion af [API'en for enkelthændelser](#create-reservation-events).

```txt
Path:
    /api/environment/{environmentId}/onhand/reserve/bulk
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
            quantities: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
            modifier: string,
            quantity: number,
            ifCheckAvailForReserv: boolean,
        },
        ...
    ]
```

## <a name="reverse-reservation-events"></a>Tilbageføre reservationshændelser

API'en *Unreserve* fungerer som tilbageførselshandling for [*Reservation*](#create-reservation-events)-hændelser. Den giver dig mulighed for at tilbageføre en reservationshændelse, der er angivet af `reservationId`, for at mindske reservationsantallet.

### <a name="reverse-one-reservation-event"></a><a name="reverse-one-reservation-event"></a>Tilbagefør én reservationshændelse

Når der oprettes en reservation, medtages `reservationId` i svarteksten. Du skal angive det samme `reservationId` for at annullere reservationen og medtage det samme `organizationId` og `dimensions`, der bruges til API-kaldet af reservation. Endelig skal du angive en `OffsetQty`-værdi, der angiver det antal varer, der skal frigøres fra den forrige reservation. En reservation kan enten tilbageføres helt eller delvist afhængigt af den angivne `OffsetQty`. Hvis der f.eks. . er reserveret *100* vareenheder, kan du angive `OffsetQty: 10` for at afreservere *10* af det oprindeligt reserverede antal.

```txt
Path:
    /api/environment/{environmentId}/onhand/unreserve
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
        reservationId: string,
        dimensions: {
            [key:string]: string,
        },
        OffsetQty: number
    }
```

Følgende kode viser et eksempel på brødtekstens indhold.

```json
{
    "id": "unreserve-0",
    "organizationId": "SCM_IV",
    "reservationId": "RESERVATION_ID",
    "dimensions": {
        "siteid":"iv_postman_site",
        "locationid":"iv_postman_location",
        "ColorId": "red",
        "SizeId&quot;: &quot;small"
    },
    "OffsetQty": 1
}
```

Følgende kode viser et eksempel på et korrekt svarindhold.

```json
{
    "reservationId": "RESERVATION_ID",
    "totalInvalidOffsetQtyByReservId": 0,
    "id": "ohoe~id-823-11744-883",
    "processingStatus": "success",
    "message": "",
    "statusCode": 200
}
```

> [!NOTE]
> Når `OffsetQty` i svaret er mindre end eller lig med reservationsantallet, vil `processingStatus` være "*success*", og `totalInvalidOffsetQtyByReservId` vil være *0*.
>
> Hvis `OffsetQty` er større end det reserverede antal, vil `processingStatus` være "*partialSuccess*", og `totalInvalidOffsetQtyByReservId` vil være forskellen mellem `OffsetQty` og det reserverede antal.
>
>Hvis reservationen f.eks. har et antal på *10* og `OffsetQty` har en værdi på *12*, vil værdien af `totalInvalidOffsetQtyByReservId` være *2*.

### <a name="reverse-multiple-reservation-events"></a><a name="reverse-multiple-reservation-events"></a>Tilbagefør flere reservationshændelser

Denne API er en bulkversion af [API'en for enkelthændelser](#reverse-one-reservation-event).

```txt
Path:
    /api/environment/{environmentId}/onhand/unreserve/bulk
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
            reservationId: string,
            dimensions: {
                [key:string]: string,
            },
            OffsetQty: number
        }
        ...
    ]
```

## <a name="query-on-hand"></a>Forespørg om disponibelt antal

Brug API'en *Forespørg om disponibelt antal* til at hente aktuelle data om disponibelt antal for dine produkter. Du kan bruge denne API, når du skal kende lageret, f.eks. hvornår du vil gennemse produktlagerniveauer på e-handelswebstedet, eller når du vil kontrollere, om produktet er tilgængeligt i flere områder eller i nærliggende butikker og lagersteder. API'en understøtter i øjeblikket forespørgsler på op til 5000 individuelle varer efter `productID`-værdi. Der kan også angives flere `siteID`- og `locationID`-værdier i hver forespørgsel. Maksimumgrænsen defineres af følgende ligning:

*NumOf(SiteID) \* NumOf(LocationID) <= 100*.

### <a name="query-by-using-the-post-method"></a><a name="query-with-post-method"></a>Forespørgsel ved hjælp af opslagsmetoden

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

I brødteksten i denne anmodning er `dimensionDataSource` stadig en valgfri parameter. Hvis den ikke er angivet, behandles `filters` som *basisdimensioner*. Der er fire obligatoriske felter til `filters`: `organizationId`, `productId`, `siteId` og `locationId`.

- `organizationId` skal kun indeholde én værdi, men det er stadig en matrix.
- `productId` kan indeholde en eller flere værdier. Hvis det er en tom matrix, returneres alle produkter.
- `siteId` og `locationId` bruges i partitionering i Lagersynlighed. Du kan angive mere end én `siteId` og `locationId`-værdi i en *Forespørgselsanmodning*. I den aktuelle version skal du angive både `siteId` og `locationId`-værdier.

Vi foreslår, at du bruger parameteren `groupByValues` til at følge din konfiguration til indeksering. Du kan få flere oplysninger i [Konfiguration af produktindekshierarki](./inventory-visibility-configuration.md#index-configuration).

Parameteren `returnNegative` bestemmer, om resultaterne indeholder negative poster.

> [!NOTE]
> Hvis du har aktiveret funktionerne til ændringsplan for disponibelt antal og disponibel til tilsagn (DTT), kan forespørgslen også indeholde den booleske `QueryATP`-parameter, der bestemmer, om forespørgselsresultaterne omfatter DTT-oplysninger. Du kan finde flere oplysninger og eksempler i [Ændringsplaner for disponibelt antal og disponibel til tilsagn i lagersynlighed](inventory-visibility-available-to-promise.md).

Følgende er et eksempel på brødtekst. Den viser, at du kan forespørge på den lagerbeholdning, der er på lager fra flere lokationer (lagersteder).

```json
{
    "dimensionDataSource": "pos",
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["T-shirt"],
        "siteId": ["1"],
        "locationId": ["11","12","13"],
        "colorId": ["red"]
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

I følgende eksempel vises, hvordan du forespørger på alle produkter på en bestemt lokation og lokation.

```json
{
    "filters": {
        "organizationId": ["usmf"],
        "productId": [],
        "siteId": ["1"],
        "locationId": ["11"],
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

### <a name="query-by-using-the-get-method"></a><a name="query-with-get-method"></a>Forespørgsel ved hjælp af hentningsmetoden

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

Her er et eksempel på en URL-adresse. Denne anmodning er nøjagtigt den samme som det opslagseksempel, som blev angivet tidligere.

```txt
/api/environment/{environmentId}/onhand?organizationId=SCM_IV&productId=iv_postman_product&siteId=iv_postman_site&locationId=iv_postman_location&colorId=red&groupBy=colorId,sizeId&returnNegative=true
```

## <a name="on-hand-exact-query"></a><a name="exact-query-with-post-method"></a>Forespørgsel om disponibel lagerbeholdning

Forespørgsler, der er nøjagtige for den findes, ligner almindelige forespørgsler på findes, men de giver dig mulighed for at angive et tilknytningshierarki mellem en lokation og en lokation. Du kan f.eks. have følgende to websteder:

- Websted 1, som er tilknyttet lokation A
- Websted 2, som er tilknyttet lokation B

Til en almindelig beholdningsforespørgsel skal du angive `"siteId": ["1","2"]` og `"locationId": ["A","B"]`, vil lagersynlighed automatisk forespørge på resultatet for følgende websteder og lokationer:

- Websted 1, lokation A
- Websted 1, lokation B
- Websted 2, lokation A
- Websted 2, lokation B

Som du kan se, anerkendes det i den almindelige forespørgsel ikke, at lokation A kun findes i websted 1, og lokation B findes kun i websted 2. Den foretager derfor overflødige forespørgsler. For at tilpasse denne hierarkiske tilknytning kan du bruge en præcis hierarkisk forespørgsel og angive lokalitetstilknytninger i forespørgselsteksten. I dette tilfælde forespørger og modtager du kun resultater for websted 1, lokation A og websted 2, lokation B.

### <a name="exact-query-by-using-the-post-method"></a><a name="exact-query-with-post-method"></a>Nøjagtig forespørgsel ved hjælp af bogføringsmetoden

```txt
Path:
    /api/environment/{environmentId}/onhand/exactquery
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
            dimensions: string[],
            values: string[][],
        },
        groupByValues: string[],
        returnNegative: boolean,
    }
```

I brødteksten i denne anmodning er `dimensionDataSource` en valgfri parameter. Hvis den ikke er angivet, behandles `dimensions` i `filters` som *basisdimensioner*. Der er fire obligatoriske felter til `filters`: `organizationId`, `productId`, `dimensions` og `values`.

- `organizationId` skal kun indeholde én værdi, men det er stadig en matrix.
- `productId` kan indeholde en eller flere værdier. Hvis det er en tom matrix, returneres alle produkter.
- I matrixen `dimensions` er `siteId` og `locationId` påkrævet, men kan blive vist med andre elementer i vilkårlig rækkefølge.
- `values` kan indeholde en eller flere specifikke tupler af værdier, der svarer til `dimensions`.

`dimensions` i `filters` bliver automatisk føjet til `groupByValues`.

Parameteren `returnNegative` bestemmer, om resultaterne indeholder negative poster.

Følgende er et eksempel på brødtekst.

```json
{
    "dimensionDataSource": "pos",
    "filters": {
        "organizationId": ["SCM_IV"],
        "productId": ["iv_postman_product"],
        "dimensions": ["siteId", "locationId", "colorId"],
        "values" : [
            ["iv_postman_site", "iv_postman_location", "red"],
            ["iv_postman_site", "iv_postman_location", "blue"],
        ]
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

I følgende eksempel vises, hvordan du forespørger på alle produkter på flere steder og lokationer.

```json
{
    "filters": {
        "organizationId": ["SCM_IV"],
        "productId": [],
        "dimensions": ["siteId", "locationId"],
        "values" : [
            ["iv_postman_site_1", "iv_postman_location_1"],
            ["iv_postman_site_2", "iv_postman_location_2"],
        ]
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

## <a name="available-to-promise"></a>Disponibel til tilsagn

Du kan konfigurere lagersynlighed, så du kan planlægge fremtidige ændringer af disponibelt antal og beregne DTT-mængder. DTT er antallet af en vare, der er tilgængelig og kan være lovet til en kunde i den næste periode. Brug af DTT-beregningen kan øge ordreopfyldningsfunktionaliteten væsentligt. Du kan få oplysninger om, hvordan du aktiverer denne funktion, og hvordan du bruger lagersynlighed via API'en, når funktionen er aktiveret, i [Ændringsplaner for disponibelt antal og disponibel til tilsagn i lagersynlighed](inventory-visibility-available-to-promise.md#api-urls).

## <a name="allocation"></a>Tildeling

Fordelingsrelaterede API'er findes i [Fordeling af lagersynlighed](inventory-visibility-allocation.md#using-allocation-api).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
