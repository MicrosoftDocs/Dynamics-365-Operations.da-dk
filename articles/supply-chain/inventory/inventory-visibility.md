---
title: Tilføjelsesprogrammet Lagersynlighed
description: Dette emne beskriver, hvordan du installerer og konfigurerer tilføjelsesprogrammet Lagersynlighed til Dynamics 365 Supply Chain Management.
author: sherry-zheng
manager: tfehr
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 4e6f7e0a3978bbf7e520f8cbcfd27c4cfe507777
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114664"
---
# <a name="inventory-visibility-add-in"></a>Tilføjelsesprogrammet Lagersynlighed

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Tilføjelsesprogrammet Lagersynlighed er en uafhængig og meget skalerbar mikrotjeneste, der gør det muligt at registrere disponibel lagerbeholdning i realtid, hvilket giver en global visning af lagersynlighed.

Alle oplysninger, der vedrører disponibel lagerbeholdning, eksporteres for tjenesten næsten i realtid via SQL-integration på lavt niveau. Eksterne systemer får adgang til tjenesten via RESTful-API'er for at forespørge på disponible oplysninger om bestemte sæt dimensioner, så der hentes en liste over tilgængelige disponible positioner.

Lagersynlighed er en mikrotjeneste, der bygger på Microsoft Dataverse, hvilket betyder, at du kan udvide den ved at opbygge Power Apps og anvende Power BI for at levere brugerdefinerede funktioner, der opfylder virksomhedens behov. Du kan også opgradere indekset for at foretage lagerforespørgsler.

Lagersynlighed angiver konfigurationsindstillinger, så den kan integreres med flere tredjepartssystemer. Den understøtter den standardiserede lagerdimension, tilpassede udvidelsesmuligheder og standardiserede, beregnede antal, der kan konfigureres.

Dette emne beskriver, hvordan du installerer og konfigurerer tilføjelsesprogrammet Lagersynlighed til Dynamics 365 Supply Chain Management, og hvordan du bruger dets API (Application Programming Interface).

## <a name="install-the-inventory-visibility-add-in"></a>Installere tilføjelsesprogrammet Lagersynlighed

Du skal installere tilføjelsesprogrammet Lagersynlighed ved hjælp af Microsoft Dynamics Lifecycle Services (LCS). LCS er en samarbejdsportal, der leverer et miljø og et sæt regelmæssigt opdaterede tjenester, der hjælper dig med at administrere programlivscyklussen for dine Dynamics 365 Finance and Operations-apps.

Yderligere oplysninger finder du i [Ressourcer til Lifecycle Services](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).

### <a name="prerequisites"></a>Forudsætninger

Før du installerer tilføjelsesprogrammet Lagersynlighed, skal du gøre følgende:

- Få et LCS-implementeringsprojekt med mindst ét miljø installeret.
- Generér betanøglerne til dit tilbud i LCS.
- Aktivér betanøglerne for dit tilbud til din bruger i LCS.
- Kontakt Microsoft-produktteamet for Lagersynlighed, og levér et miljø-id, hvor du vil installere tilføjelsesprogrammet Lagersynlighed.

Hvis du har spørgsmål om disse forudsætninger, skal du kontakte produktteamet for Lagersynlighed.

### <a name="install-the-add-in"></a><a name="install-add-in"></a>Installer tilføjelsesprogrammet

For at installere tilføjelsesprogrammet Lagersynlighed skal du gøre følgende:

1. Log på portalen [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).
1. Vælg det projekt, dit miljø skal implementeres i, på startsiden.
1. Vælg det miljø, som tilføjelsesprogrammet skal installeres i, på projektsiden.
1. Rul ned på miljøsiden, indtil du ser afsnittet **Miljøtilføjelsesprogrammer**. Hvis sektionen ikke vises, skal du kontrollere, at de nødvendige betanøgler er blevet behandlet fuldt ud.
1. Vælg **Installér et nyt tilføjelsesprogram** i afsnittet **Tilføjelsesprogrammer for miljø**.
    ![Miljøsiden i LCS](media/inventory-visibility-environment.png "Miljøsiden i LCS")
1. Vælg linket **Installer et nyt tilføjelsesprogram**. Der åbnes en liste over tilgængelige tilføjelsesprogrammer.
1. Vælg **Lagerservice** på listen. (Bemærk, at den nu kan være angivet som **Tilføjelsesprogrammet Lagersynlighed til Dynamics 365 Supply Chain Management**).
1. Angiv værdier for følgende felter til dit miljø:

    - **AAD-program-id**
    - **AAD-lejer-id**

    ![Konfigurationsside for tilføjelsesprogram](media/inventory-visibility-setup.png "Konfigurationsside for tilføjelsesprogram")

1. Acceptér vilkårene og betingelsen ved at markere afkrydsningsfeltet **Vilkår og betingelser**.
1. Vælg **Installer**. Status for tilføjelsesprogrammet vil blive vist som **installerer**. Når det er gjort, skal du opdatere siden for at se statusændringen til **Installeret**.

### <a name="get-a-security-service-token"></a>Få et token til sikkerhedsservice

Få et token til sikkerhedsservice ved at gøre følgende:

1. Log på Azure-portalen, og brug den til at finde `clientId` og `clientSecret` til din Supply Chain Management-applikation.
1. Hent et Azure Active Directory-token (`aadToken`) ved at sende en HTTP-anmodning med følgende egenskaber:
    - **URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`
    - **metode** - `GET`
    - **Brødtekst (formulardata)**:

        | nøgle | værdi |
        | --- | --- |
        | client_id | ${aadAppId} |
        | client_secret | ${aadAppSecret} |
        | grant_type | client_credentials |
        | ressource | 0cdb527f-a8d1-4bf8-9436-b352c68682b2 |
1. Du modtager et `aadToken` i svaret, der ligner følgende eksempel.

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

1. Formuler en JSON-anmodning, der ligner følgende:

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type":"aad_app",
        "client_assertion": "{Your_AADToken}",
        "scope":"https://inventoryservice.operations365.dynamics.com/.default",
        "context": "5dbf6cc8-255e-4de2-8a25-2101cd5649b4",
        "context_type": "finops-env"
    }
    ```

    Placering:
    - Værdien `client_assertion` skal være det `aadToken`, du har modtaget i det forrige trin.
    - Værdien `context` skal være det miljø-id, hvor du vil implementere tilføjelsesprogrammet.
    - Angiv alle andre værdier som vist i eksemplet.

1. Send en HTTP-anmodning med følgende egenskaber:
    - **URL** - `https://securityservice.operations365.dynamics.com/token`
    - **metode** - `POST`
    - **HTTP-overskrift** – Medtag API-versionen (nøglen er `Api-Version`, og værdien er `1.0`)
    - **Brødtekst** – Medtag den JSON-anmodning, du oprettede i det forrige trin.

1. Du vil få et `access_token` i svaret. Det skal du bruge som ihændehavertoken for at kalde Lagersynlighed-API'et. Her er et eksempel.

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="uninstall-the-add-in"></a>Fjern tilføjelsesprogrammet

Hvis du vil fjerne tilføjelsesprogrammet, skal du vælge **Fjern**. Opdater LCS, så tilføjelsesprogrammet Lagersynlighed fjernes. Fjernelsesprocessen fjerner registreringen af tilføjelsesprogrammet og starter et job for at rydde op i alle de forretningsdata, der er gemt i tjenesten.

## <a name="inventory-visibility-add-in-public-api"></a>Offentlig API for tilføjelsesprogrammet Lagersynlighed

Den offentlige REST-API til tilføjelsesprogrammet Lagersynlighed viser flere specifikke integrationsslutpunkter. Det understøtter tre overordnede interaktionstyper:

- Bogføring af ændret lagerbeholdning i tilføjelsesprogrammet fra et eksternt system.
- Forespørgsel om aktuelle disponible lagerantal fra et eksternt system.
- Automatisk synkronisering med lagerbeholdning i Supply Chain Management.

Den automatiske synkronisering er ikke en del af det offentlige API, men bliver i stedet håndteret i baggrunden for miljøer, der har aktiveret tilføjelsesprogrammet Lagersynlighed.

### <a name="authentication"></a>Godkendelse

Platformens sikkerhedstoken bruges til at kalde tilføjelsesprogrammet Lagersynlighed, så du skal generere et Azure Active Directory-token ved hjælp af dit Azure Active Directory-program.

Du kan finde flere oplysninger om, hvordan du får fat i sikkerhedstoken, i [Installere tilføjelsesprogrammet Lagersynlighed](#install-add-in).

### <a name="configure-the-inventory-visibility-api"></a>Konfigurere API'et til Lagersynlighed

Før du bruger tjenesten, skal du udføre de konfigurationer, der er beskrevet i følgende underafsnit. Konfigurationen kan variere afhængigt af detaljerne i dit miljø. Den består primært af fire dele:

- [Partitionering](#partitioning)
- [Dimensionskonfigurationer](#dimension-configurations)
- [Indeksering](#indexing)
- [Brugerdefineret måling](#custom-measurement)

#### <a name="partitioning"></a>Partitionering

Partitionering kan have stor indflydelse på ydeevnen af Lagersynlighed-API'et. Det er en god ide at definere et skema, der giver mulighed for mindre gruppering af data, mens det stadig er muligt at give meningsfulde dataforespørgsler.

Elementet `organizationId` (`dataAreaId` i Supply Chain Management) vil altid være en del af partitionen, og Lagersynlighede er som standard angivet til at partitionere efter dimensioner som *Sted + lokation*. Det betyder, at der altid skal sendes forespørgsler til tjenesten med de dimensioner, der er defineret på filtrene.

> [!NOTE]
> *Sted* og *Lokation* er to generelle standarddimensioner i Lagersynlighed. I Supply Chain Management kaldes disse dimensioner *Sted* (`InventSiteId`) og *Lagersted* (`InventLocationId`).

### <a name="dimension-configurations"></a>Dimensionskonfigurationer

Lagersynlighed vil indeholde en liste over generelle standarddimensioner, der gør det muligt at integrere flere kildesystemer.

I følgende tabel vises de lagerdimensioner, der vil være standarddimensionsnavne i Lagersynlighed.

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

> [!NOTE]
> Den dimensionstype, der er angivet i forrige tabel, er kun til reference. Du behøver ikke definere dimensionstypen i Lagersynlighed.

Hvis der findes en brugerdefineret dimension, som skal overføres til en standardværdi, når den forbruges af Lagersynlighed, kan du konfigurere navnet **Brugerdefineret dimension** i Lagersynlighed.

Eksterne systemer får adgang til Lagersynlighed gennem RESTful API'er, der muliggør disponible oplysninger om bestemte sæt dimensioner, der skal forespørges. I forbindelse med integrationen giver Lagersynlighed dig mulighed for at konfigurere den *eksterne kanals datakilde* og kildedimensionen til *måldimensionerne* i Lagersynlighed.

Måldimensionerne skal være en af følgende:

- Standarddimensioner i Lagersynlighed
- Brugerdefinerede dimensioner

Formålet med dimensionskonfiguration er at standardisere integrationen af flere systemer til forespørgslen på dimensioner og bogføringshændelsen med dimensioner.

#### <a name="indexing"></a>Indeksering

I de fleste tilfælde vil lagerbeholdningsforespørgslen ikke kun være på det højeste "totale" niveau, men du ønsker måske at se de samlede resultater på baggrund af lagerdimensionerne.

Lagersynlighed giver fleksibilitet, fordi du kan konfigurere de indekser, der er baseret på dimensionen eller kombinationen af dimensionerne.

> [!NOTE]
> I øjeblikket kan du kun konfigurere indekser til maksimalt fem. Du skal nøje overveje, hvilken dimension eller dimensionskombination du vil bruge før implementeringen for at sikre, at den opfylder dine forretningsbehov. Hvis du f.eks. vil forespørge på produkter på følgende måde:

- Forespørg på den samlede disponible beholdning via *Farve*- og *Størrelse*-dimensionerne.
- I nogle tilfælde vil du kun forespørge på produktet i alt.

Du skal have defineret to indekser som følgende:

- `["ColorId", "SizeId"]`
- `[]`

Den tomme kantede parentes samles på basis af produkt-id'et i partitionen.

Indekseringen definerer, hvordan du kan gruppere resultaterne baseret på `groupBy`-forespørgselsindstillingen. Hvis du ikke definerer `groupBy`-værdier, får du totaler med `productid`. Hvis du definerer `groupBy` som `groupBy=ColorId&groupBy=SizeId`, får du flere linjer baseret på de forskellige kombinationer af farve og størrelse i systemet.

Du kan sætte dine forespørgselskriterier i anmodningsteksten.

Her er et eksempel på en forespørgsel på produktet med en kombination af farve og størrelse.

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="custom-measurement"></a>Brugerdefineret måling

Standardmålingen af antal er knyttet til Supply Chain Management, men det kan være en god ide at have et antal, der består af en kombination af standardmålingerne. Hvis du vil gøre dette, kan du have en konfiguration af brugerdefinerede antal, der føjes til outputtet af forespørgsler på den disponible lagerbeholdning.

Denne funktion giver dig mulighed for at definere et sæt målinger, der skal tilføjes, og/eller et sæt målinger, der skal trækkes fra, så de danner den brugerdefinerede måling.

I følgende forespørgselsbetingelse skal du f.eks. konfigurere det brugerdefinerede måleanta som `MyCustomAvailableforReservation`, der skal forbruges af forbrugssystemet.

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]

```



| Forbrugssystem | Beregnede målinger | Datakilde | Modifikator | Modifikator som beregningstype |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | Addition |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | Addition |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | Subtraktion |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | Addition |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | Subtraktion |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | Addition |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | Addition |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | Subtraktion |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | Subtraktion |

Med denne fremgangsmåde vil forespørgslen på det brugerdefinerede måleantal returnere følgende output.

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
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

Outputtet `MyCustomAvailableforReservation` er baseret på beregningsindstillingen i de brugerdefinerede målinger som:  
 *100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*

### <a name="posting-on-hand-changes"></a>Bogføring af ændret lagerbeholdning

Den præcise URL-adresse, som hændelsen vil blive bogført til, afhænger af dit geografiske område. Den har formatet:

`https://{serviceURL}/api/environment/{environmentId}/onhand`

Når denne URL-adresse er godkendt, kan den bruges sammen med HTTP-`POST`-metoden til at sende hændelser for beholdningsændring til tjenesten.

En speciel header bruges til kommunikation med Dynamics 365-tjenester via HTTP-anmodninger, der angiver miljø-id'et for Supply Chain Management-forekomst, som dataene er kædet sammen med. F.eks.:

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a>Bogføring af forespørgsel på lagerbeholdningsændringer, eksempel 1

I dette eksempel vises et scenario, hvor du konfigurerer dimensionskonfigurationen i Power Apps.

Brug følgende forespørgsel til at konfigurere dimensionstilknytningen i Power Apps:

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

Nu kan du angive `dimensionDataSource` og bruge brugerdefinerede dimensioner i forespørgslerne. Systemet vil automatisk konvertere brugerdefinerede dimensioner til basisdimensioner.

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensionDataSource": "pos",
    "dimensions": {
        "PosSizeId": "Large",
        "PosColorId": "Red",
        "PosSiteId": "2",
        "PosLocationId": "21"
    }
}
```

#### <a name="posting-on-hand-changes-query-example-2"></a>Bogføring af forespørgsel på lagerbeholdningsændringer, eksempel 2

I dette eksempel vises et scenario, hvor der ikke er konfigureret tilknytninger for dimensionskonfigurationen i Power Apps, så bogføringen skal også bruge basisdimensionerne. Alle dimensioner skal være basisdimensioner, når `dimensionDataSource`-feltet er null, tomt eller blanktegn.

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensions": {
        "SizeId": "Large",
        "ColorId": "Red",
        "SiteId": "2",
        "LocationId": "21"
    }
}
```

#### <a name="json-document-field-properties"></a>JSON-dokumentfeltegenskaber

Felterne fra de JSON-forespørgselseksempler, der tidligere blev vist, har de egenskaber, der er angivet i følgende tabel.

| Felt-id | Beskrivelse |
|---|---|
| `id` | Et entydigt id for den specifikke ændringshændelse. Dette id bruges til at sikre, at hvis kommunikationen med tjenesten mislykkes under bogføring, vil genafsendelse af hændelsen ikke resultere i, at den samme hændelse tælles to gange i systemet. |
| `organizationId` | Identifikatoren for den organisation, der er knyttet til hændelsen. Dette knytter data til Supply Chain Management-organisationer eller dataområde-id'er. |
| `productId` | Produktets identifikator. |
| `quantity` | Det antal, som lagerbeholdningen skal ændres med. Hvis der f.eks. er føjet 10 nye bagels til en hylde, vil denne værdi være 10. Hvis 3 bagels blev fjernet fra hylden eller solgt, vil denne værdi være -3. |
| `dimensionDataSource` | Datakilden til de dimensioner, der bruges i bogføring af ændringshændelsen og forespørgsel. Hvis du angiver datakilden, kan du bruge de brugerdefinerede dimensioner fra den angivne datakilde. Med dimensionskonfigurationen kan Lagersynlighed knytte de tilpassede dimensioner til de generelle standarddimensioner. Hvis `dimensionDataSource` ikke er angivet, kan du kun bruge de generelle standarddimensioner i forespørgslerne.   |
| `dimensions` | En dynamisk pose med nøgle/værdi-par. De vil blive knyttet til nogle af dimensionerne i Supply Chain Management, men du kan også tilføje brugerdefinerede dimensioner (som f.eks. *Kilde*), der kan angive, om hændelsen kommer fra Supply Chain Management eller et eksternt system. |

### <a name="querying-current-on-hand"></a>Forespørgsel på aktuel disponibel lagerbeholdning

Slutpunktet for forespørgsel på den aktuelle disponible lagerbeholdning vil have en lignende URL-adresse:

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

Den vil blive forespurgt efter HTTP-`POST`-metoden.

#### <a name="current-on-hand-query-example-1"></a>Forespørgsel på aktuel disponibel lagerbeholdning, eksempel 1

I dette eksempel vises et scenario, hvor du allerede har fuldført dimensionskonfigurationen i Power Apps.

Brug følgende forespørgsel til at konfigurere dimensionstilknytningen i Power Apps:

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

Nu kan du angive `dimensionDataSource` og bruge brugerdefinerede dimensioner i forespørgslerne. Systemet vil automatisk konvertere brugerdefinerede dimensioner til basisdimensioner. Du kan angive `DimensionDataSource` i `filters` og angive brugerdefinerede dimensioner i både `filters` og `groupByValues`. Systemet vil automatisk konvertere brugerdefinerede dimensioner til basisdimensioner.

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "DimensionDataSource": ["Pos"],
        "PosLocationId": ["21"],
        "PosSiteId": ["2"],
        "PosColorId": ["Red"]
    },
    "groupByValues": [
        "PosSizeId",
        "PosColorId"
    ],
    "returnNegative": true
}
```

#### <a name="current-on-hand-query-example-2"></a>Forespørgsel på aktuel disponibel lagerbeholdning, eksempel 2

I dette eksempel vises et scenario, hvor der ikke er konfigureret tilknytninger for dimensionskonfigurationen i Power Apps, så bogføringen skal også bruge basisdimensionerne. Alle dimensioner skal være basisdimensioner, når `dimensionDataSource`-feltet under `filters` er null, tomt eller blanktegn.

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="example-return-result"></a>Eksempel på returnering af resultat

De forespørgsler, der vises i de foregående eksempler, kunne returnere et resultat som dette.

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
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

Bemærk, at antalsfelterne er struktureret som en ordbog med målinger og deres tilknyttede værdier.
