---
title: Offentlige API'er for Lagersynlighed
description: Dette emne beskriver de offentlige API'er, der leveres via Lagersynlighed.
author: yufeihuang
ms.date: 09/30/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 43fa94118c4d76e021bb635d720208d5f971db19
ms.sourcegitcommit: 49f29aaa553eb105ddd5d9b42529f15b8e64007e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2021
ms.locfileid: "7592482"
---
# <a name="inventory-visibility-public-apis"></a>Offentlige API'er for Lagersynlighed

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Dette emne beskriver de offentlige API'er, der leveres via Lagersynlighed.

Den offentlige REST-API til tilføjelsesprogrammet Lagersynlighed viser flere specifikke slutpunkter for integration. Det understøtter fire overordnede interaktionstyper:

- Bogføring af ændret lagerbeholdning i tilføjelsesprogrammet fra et eksternt system
- Angive eller tilsidesætte antal for disponibel lagerbeholdningl i tilføjelsesprogrammet fra et eksternt system
- Bogføring af reservationshændelser i tilføjelsesprogrammet fra et eksternt system
- Forespørgsel om aktuelle disponible lagerantal fra et eksternt system

I følgende tabel vises de API'er, der er tilgængelige i øjeblikket:

| Sti | metode | Betegnelse |
|---|---|---|
| /api/environment/{environmentId}/onhand | Bogfør | [Oprette en ændringshændelse for disponibelt antal](#create-one-onhand-change-event) |
| /api/environment/{environmentId}/onhand/bulk | Bogfør | [Oprette flere ændringshændelser](#create-multiple-onhand-change-events) |
| /api/environment/{environmentId}/setonhand/{inventorySystem}/bulk | Bogfør | [Angive/tilsidesætte disponibelt antal](#set-onhand-quantities) |
| /api/environment/{environmentId}/onhand/reserve | Bogfør | [Oprette én reservationshændelse](#create-one-reservation-event) |
| /api/environment/{environmentId}/onhand/reserve/bulk | Bogfør | [Oprette flere reservationshændelser](#create-multiple-reservation-events) |
| /api/environment/{environmentId}/onhand/indexquery | Hent | [Forespørgsel ved hjælp af opslagsmetoden](#query-with-post-method) |
| /api/environment/{environmentId}/onhand/indexquery | Bogfør | [Forespørgsel ved hjælp af hentningsmetoden](#query-with-get-method) |

Microsoft har leveret den brugsklare anmodningssamling *Postman*. Du kan importere denne samling til softwaren *Postman* med følgende delte link: <https://www.getpostman.com/collections/90bd57f36a789e1f8d4c>.

> [!NOTE]
> {environmentId}-delen af stien er miljø-id'et i Microsoft Dynamics Lifecycle Services (LCS).

## <a name="find-the-endpoint-according-to-your-lifecycle-services-environment"></a>Find slutpunktet i overensstemmelse med Lifecycle Services-miljøet

Mikrotjenesten for Lagersynlighed installeres på Microsoft Azure Service Fabric i flere geografier og flere områder. Der er i øjeblikket ikke et centralt slutpunkt, der automatisk kan omdirigere din anmodning til den tilsvarende geografi eller det tilsvarende område. Du skal derfor skrive oplysningerne i en URL-adresse efter følgende mønster:

`https://inventoryservice.<RegionShortName>-il<IsLandNumber>.gateway.prod.island.powerapps.com`

Områdets korte navn findes i Microsoft Dynamics Lifecycle Services-miljøet (LCS). I følgende tabel vises de områder, der er tilgængelige i øjeblikket.

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
| Sydbrasilien        | sbr               |
| Den sydlige del af det centrale USA    | scus              |

Ø-nummeret er det sted, hvor LCS-miljøet installeres på Service Fabric. Du kan i øjeblikket ikke hente disse oplysninger fra brugersiden.

Microsoft har bygget en brugergrænseflade (UI) i Power Apps, så du kan hele hele slutpunktet for mikrotjenesten. Du kan finde flere oplysninger i [Finde tjenestens slutpunkt](inventory-visibility-configuration.md#get-service-endpoint).

## <a name="authentication"></a><a name="inventory-visibility-authentication"></a>Godkendelse

Sikkerhedstoken for platformen bruges til at kalde det offentlige API for Lagersynlighed. Du skal derfor generere et _Azure Active Directory-token (Azure AD)_ ved hjælp af Azure AD-programmet. Du skal derefter bruge Azure AD-tokenet til at hente _adgangstoken_ fra sikkerhedstjenesten.

Microsoft leverer den brugsklare hent token-samling *Postman*. Du kan importere denne samling til softwaren *Postman* med følgende delte link: <https://www.getpostman.com/collections/496645018f96b3f0455e>.

Hvis du vil hente et token for sikkerhedstjenesten, skal du følge disse trin.

1. Log på Azure-portalen, og brug den til at finde værdierne `clientId` og `clientSecret` for Dynamics 365 Supply Chain Management-appen.
1. Hent et Azure AD-token (`aadToken`) ved at sende en HTTP-anmodning, der har følgende egenskaber:

   - **URL:** `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`
   - **Metode:** `GET`
   - **Brødtekst (formulardata):**

     | Nøgle           | Værdi                                |
     | ------------- | ------------------------------------ |
     | client_id     | ${aadAppId}                          |
     | client_secret | ${aadAppSecret}                      |
     | grant_type    | client_credentials                   |
     | ressource      | 0cdb527f-a8d1-4bf8-9436-b352c68682b2 |

   Du skal modtage et Azure AD-token (`aadToken`) som svar. Den skulle ligne følgende eksempel:

   ```json
   {
       "token_type": "Bearer",
       "expires_in": "3599",
       "ext_expires_in": "3599",
       "expires_on": "1610466645",
       "not_before": "1610462745",
       "resource": "0cdb527f-a8d1-4bf8-9436-b352c68682b2",
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
       "context": "5dbf6cc8-255e-4de2-8a25-2101cd5649b4",
       "context_type": "finops-env"
   }
   ```

   Vær opmærksom på følgende punkter:

   - Værdien `client_assertion` skal være det Azure AD-token (`aadToken`), som du har modtaget i det forrige trin.
   - Værdien `context` skal være det LCD-miljø-id, hvor du vil implementere tilføjelsesprogrammet.
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
> Når du bruger anmodningssamlingen *Postman* til at kalde offentlige API'er for lagersynlighed, skal du tilføje et ihændehaver-token for hver anmodning. Hvis du vil finde dit ihændehaver-token, skal du vælge fanen **Godkendelse** under URL-adressen til anmodningen, vælge typen **Ihændehaver-token** og kopiere det adgangstoken, der blev hentet i det sidste trin. I senere afsnit til dette emne bruges `$access_token` til at repræsentere det token, der blev hentet i sidste trin.

## <a name="create-on-hand-change-events"></a><a name="create-onhand-change-event"></a>Oprette ændringshændelser for disponibelt antal

Der findes to API'er til oprettelse af ændringshændelser for disponibelt antal:

- Oprette én post: `/api/environment/{environmentId}/onhand`
- Oprette flere poster: `/api/environment/{environmentId}/onhand/bulk`

I følgende tabel opsummeres betydningen af hvert felt i JSON-brødteksten.

| Felt-id | Betegnelse |
|---|---|
| `id` | Et entydigt id for den specifikke ændringshændelse. Dette id bruges til at sikre, at hvis kommunikationen med tjenesten mislykkes under bogføringen, vil hændelsen ikke blive talt med to gange i systemet, hvis den sendes igen. |
| `organizationId` | Identifikatoren for den organisation, der er knyttet til hændelsen. Denne værdi er tilknyttet et organisations-id eller et dataområde-id i Supply Chain Management. |
| `productId` | Id'et for produktet. |
| `quantities` | Det antal, som det disponible antal skal ændres med. Hvis der f.eks. føjes 10 nye bøger til en hylde, vil denne værdi være `quantities:{ shelf:{ received: 10 }}`. Hvis der fjernes tre bøger fra hylden eller de sælges, er denne værdi `quantities:{ shelf:{ sold: 3 }}`. |
| `dimensionDataSource` | Datakilden for de dimensioner, der bruges i bogføringens ændringshændelse og forespørgslen. Hvis du angiver datakilden, kan du bruge de brugerdefinerede dimensioner fra den angivne datakilde. Lagersynlighed kan bruge dimensionskonfigurationen til at knytte de brugerdefinerede dimensioner til de generelle standarddimensioner. Hvis der ingen værdi for `dimensionDataSource` er angivet, kan du kun bruge de generelle [basisdimensioner](inventory-visibility-configuration.md#data-source-configuration-dimension) i forespørgslerne. |
| `dimensions` | Et dynamisk nøgle/værdi-par. Værdierne knyttes til nogle af dimensionerne i Supply Chain Management. Du kan dog også tilføje brugerdefinerede dimensioner (f.eks. _Kilde_) for at angive, om hændelsen kommer fra Supply Chain Management eller et eksternt system. |

> [!NOTE]
> Parametrene `SiteId` og `LocationId` opbygger [partitionskonfigurationen](inventory-visibility-configuration.md#partition-configuration). Du skal derfor angive dem i dimensioner, når du opretter hændelser med disponible ændringer, angiver eller tilsidesætter disponible antal eller opretter reservationshændelser.

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

Følgende er et eksempel på brødtekst. I dette eksempel kan du bogføre en ændringshændelse for produktet *T-shirt*. Denne hændelse kommer fra POS-systemet, og kunden har returneret en rød T-shirt til butikken. Denne hændelse øger antallet for produktet *T-shirt* med 1.

```json
{
    "id": "123456",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensionDataSource": "pos",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "PosMachineId": "0001",
        "ColorId&quot;: &quot;Red"
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
    "id": "123456",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

### <a name="create-multiple-change-events"></a><a name="create-multiple-onhand-change-events"></a>Oprette flere ændringshændelser

Denne API kan oprette flere poster samtidigt. De eneste forskelle mellem denne API og [API'en for enkelthændelser](#create-one-onhand-change-event) er værdierne for `Path` og `Body`. For denne API leverer `Body` en række af poster.

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
        "id": "123456",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
            "PosSiteId": "1",
            "PosLocationId": "11",
            "PosMachineId&quot;: &quot;0001"
        },
        "quantities": {
            "pos": { "inbound": 1 }
        }
    },
    {
        "id": "654321",
        "organizationId": "usmf",
        "productId": "Pants",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId&quot;: &quot;black"
        },
        "quantities": {
            "pos": { "outbound": 3 }
        }
    }
]
```

## <a name="setoverride-on-hand-quantities"></a><a name="set-onhand-quantities"></a>Angive/tilsidesætte disponible antal

API'en for _Konfigurer disponibelt antal_ tilsidesætter de aktuelle data for det angivne produkt.

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

Følgende er et eksempel på brødtekst. Funktionsmåden for denne API er forskellig fra funktionsmåden for de API'er, der er beskrevet i afsnittet [Oprette ændringshændelser for disponibelt antal](#create-onhand-change-event) tidligere i dette emne. I dette eksempel vil antallat for produktet *T-shirt* blive angivet til 1.

```json
[
    {
        "id": "123456",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
             "PosSiteId": "1",
            "PosLocationId": "11",
            "PosMachineId": "0001"
        },
        "quantities": {
            "pos": {
                "inbound": 1
            }
        }
    }
]
```

## <a name="create-reservation-events"></a>Oprette reservationshændelser

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Hvis du vil bruge API'en for *Reservér*, skal du åbne reservationsfunktionen og fuldføre reservationskonfigurationen. Du kan finde flere oplysninger i [Konfiguration af reservationer (valgfri)](inventory-visibility-configuration.md#reservation-configuration).

### <a name="create-one-reservation-event"></a><a name="create-one-reservation-event"></a>Oprette én reservationshændelse

Der kan foretages en reservation i forhold til de forskellige datakildeindstillinger. Hvis du vil konfigurere denne reservationstype, skal du først angive datakilden i `dimensionDataSource`-parameteren. Angiv derefter dimensionerne i forhold til dimensionsindstillingerne i måldatakilden i parameteren `dimensions`.

Når du kalder reservations-API'en, kan du styre valideringen af reservationen ved at angive parameteren Boolesk `ifCheckAvailForReserv` i brødteksten. Værdien `True` betyder, at valideringen er påkrævet, mens værdien `False` betyder, at valideringen ikke er nødvendig. Standardværdien er `True`.

Hvis du vil annullere en reservation eller ikke-reservere angivne lagerantal, skal du angive antallet til en negativ værdi og angive parameteren `ifCheckAvailForReserv` til `False` for at springe valideringen over.

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
    "organizationId": "usmf",
    "productId": "T-shirt",
    "quantity": 1,
    "quantityDataSource": "iv",
    "modifier": "softreservordered",
    "ifCheckAvailForReserv": true,
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red",
        "SizeId&quot;: &quot;Small"
    }
}
```

### <a name="create-multiple-reservation-events"></a><a name="create-multiple-reservation-events"></a>Oprette flere reservationshændelser

Denne API er en bulkversion af [API'en for enkelthændelser](#create-one-reservation-event).

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

## <a name="query-on-hand"></a>Forespørg om disponibelt antal

API'en for _Forespørg om disponibelt antal_ bruges til at hente aktuelle data om disponibelt antal for dine produkter.

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

Parameteren `groupByValues` skal følge din konfiguration til indeksering. Du kan få flere oplysninger i [Konfiguration af produktindekshierarki](./inventory-visibility-configuration.md#index-configuration).

Parameteren `returnNegative` bestemmer, om resultaterne indeholder negative poster.

Følgende er et eksempel på brødtekst.

```json
{
    "dimensionDataSource": "pos",
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["T-shirt"],
        "siteId": ["1"],
        "LocationId": ["11"],
        "ColorId": ["Red"]
    },
    "groupByValues": ["ColorId", "SizeId"],
    "returnNegative": true
}
```

I følgende eksempler vises, hvordan du forespørger på alle produkter på en bestemt lokation og lokation.

```json
{
    "filters": {
        "organizationId": ["usmf"],
        "productId": [],
        "siteId": ["1"],
        "LocationId": ["11"],
    },
    "groupByValues": ["ColorId", "SizeId"],
    "returnNegative": true
}
```

### <a name="query-by-using-the-get-method"></a><a name="query-with-get-method"></a>Forespørgsel ved hjælp af hentningsmetoden

```txt
Path:
    /api/environment/{environmentId}/onhand/indexquery
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

Her er et eksempel på en URL-adresse for hentningsmetoden. Denne anmodning er nøjagtigt den samme som det opslagseksempel, som blev angivet tidligere.

```txt
/api/environment/{environmentId}/onhand/indexquery?organizationId=usmf&productId=T-shirt&SiteId=1&LocationId=11&ColorId=Red&groupBy=ColorId,SizeId&returnNegative=true
```

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
