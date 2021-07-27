---
title: Tilføjelsesprogrammet Lagersynlighed
description: Dette emne beskriver, hvordan du installerer og konfigurerer tilføjelsesprogrammet Lagersynlighed til Dynamics 365 Supply Chain Management.
author: sherry-zheng
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 8709b91b354fa4e1319b406c009bfdadeef48a41
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2021
ms.locfileid: "6358092"
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

Yderligere oplysninger finder du i [Ressourcer til Lifecycle Services](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

### <a name="inventory-visibility-add-in-prerequisites"></a>Forudsætninger for tilføjelsesprogrammet Lagersynlighed

Før du installerer tilføjelsesprogrammet Lagersynlighed, skal du gøre følgende:

- Få et LCS-implementeringsprojekt med mindst ét miljø installeret.
- Kontrollér, at forudsætningerne for opsætning af tilføjelsesprogrammer, der er angivet i [oversigten over tilføjelsesprogrammer](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md), er fuldført. Lagersynlighed kræver ikke sammenkædning af dobbeltskrivning.
- Kontakt teamet for lagersynlighed på [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) for at få følgende tre krævede filer:
  - `Inventory Visibility Dataverse Solution.zip`
  - `Inventory Visibility Configuration Trigger.zip`
  - `Inventory Visibility Integration.zip` (hvis den version af Supply Chain Management, du kører, er tidligere end version 10.0.18)
- Du kan også kontakte teamet for lagersynlighed på [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) for at få Package Deployer-pakkerne. Disse pakker kan bruges af et officielt Package Deployer-værktøj.
  - `InventoryServiceBase.PackageDeployer.zip`
  - `InventoryServiceApplication.PackageDeployer.zip` (denne pakke indeholder alle ændringerne i `InventoryServiceBase`-pakken samt yderligere komponenter til brugergrænsefladen)
- Følg instruktionerne i [Hurtig start: Registrer et program med platformen Microsoft-identitet](/azure/active-directory/develop/quickstart-register-app) for at registrere et program og føje en klient til AAD under dit Azure-abonnement.
  - [Registrere en applikation](/azure/active-directory/develop/quickstart-register-app)
  - [Tilføje en klienthemmelighed](/azure/active-directory/develop/quickstart-register-app#add-a-certificate)
  - **Program-id (klient)**, **Klienthemmelighed** og **Lejer-id** bruges i følgende trin.

> [!NOTE]
> De lande og områder, der i øjeblikket understøttes, omfatter Canada, USA og EU.

Hvis du har spørgsmål om disse forudsætninger, skal du kontakte produktteamet for Lagersynlighed.

### <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a>Konfigurere Dataverse

Hvis du vil konfigurere Dataverse til brug med Lagersynlighed, skal du først forberede forudsætningerne og derefter beslutte, om du vil konfigurere Dataverse med Package Deployer-værktøjet eller ved manuelt at importere løsningerne (du behøver ikke at gøre begge dele). Installer derefter tilføjelsesprogrammet Lagersynlighed. I følgende underafsnit beskrives, hvordan du udfører hver af disse opgaver.

#### <a name="prepare-dataverse-prerequisites"></a>Forberede Dataverse-forudsætninger

Før du begynder at konfigurere Dataverse, kan du føje et serviceprincip til din lejer på følgende måde:

1. Installer Azure AD PowerShell-modul v2 som beskrevet i [Installere Azure Active Directory PowerShell til Graph](/powershell/azure/active-directory/install-adv2).

1. Kør følgende PowerShell-kommando:

    ```powershell
    Connect-AzureAD # (open a sign in window and sign in as a tenant user)
    
    New-AzureADServicePrincipal -AppId "3022308a-b9bd-4a18-b8ac-2ddedb2075e1" -DisplayName "d365-scm-inventoryservice"
    ```

#### <a name="set-up-dataverse-using-the-package-deployer-tool"></a>Konfigurere Dataverse ved hjælp af Package Deployer-værktøjet

Når du har forudsætningerne på plads, skal du benytte følgende fremgangsmåde, hvis du foretrækker at konfigurere Dataverse ved hjælp af Package Deployer-værktøjet. Se næste afsnit for at få oplysninger om, hvordan du importerer løsningerne manuelt i stedet (du skal ikke gøre begge dele).

1. Installer udviklerværktøjer som beskrevet i [Hent værktøjer fra NuGet](/dynamics365/customerengagement/on-premises/developer/download-tools-nuget).

1. Vælg `InventoryServiceBase`- eller `InventoryServiceApplication`-pakken ud fra dine forretningsbehov.

1. Importer løsningerne:
    1. For `InventoryServiceBase`-pakken:
        - Pak `InventoryServiceBase.PackageDeployer.zip` ud
        - Find `InventoryServiceBase`-mappen, filen `[Content_Types].xml`, filen `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll`, filen `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config` og filen `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config`. 
        - Kopier hver af disse mapper og filer til den `.\Tools\PackageDeployment`-mappe, der blev oprettet, da du installerede udviklerværktøjerne.
    1. For `InventoryServiceApplication`-pakken:
        - Pak `InventoryServiceApplication.PackageDeployer.zip` ud
        - Find `InventoryServiceApplication`-mappen, filen `[Content_Types].xml`, filen `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll`, filen `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config` og filen `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config`.
        - Kopier hver af disse mapper og filer til den `.\Tools\PackageDeployment`-mappe, der blev oprettet, da du installerede udviklerværktøjerne.
    1. Udfør `.\Tools\PackageDeployment\PackageDeployer.exe`. Følg instruktionerne på skærmen for at importere løsningerne.

1. Tildel sikkerhedsroller til programbrugeren.
    1. Åbn URL-adressen til dit Dataverse-miljø.
    1. Gå til **Avancerede indstillinger \> System \> Sikkerhed \> Brugere**, og find brugeren med navnet **# InventoryVisibility**.
    1. Vælg **Tildel rolle**, og vælg derefter **Systemadministrator**. Hvis der er en rolle med navnet **Common Data Service Bruger**, skal du også vælge den.

#### <a name="set-up-dataverse-manually-by-importing-solutions"></a>Oprette Dataverse manuelt ved at importere løsninger

Når du har forudsætningerne på plads, skal du benytte følgende fremgangsmåde, hvis du foretrækker at konfigurere Dataverse ved at importere løsninger manuelt. Se forrige afsnit for at få oplysninger om, hvordan du bruger Package Deployer-værktøjet i stedet (du skal ikke gøre begge dele).

1. Opret en programbruger til lagersynlighed i Dataverse:

    1. Åbn URL-adressen til dit Dataverse-miljø.
    1. Gå til **Avancerede indstillinger \> System \> Sikkerhed \> Brugere**, og opret en programbruger. Brug menuen Vis til at ændre sidevisningen til **Applikationsbrugere**.
    1. Vælg **Ny**. Indstil program-id til *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*. (Objekt-id'et indlæses automatisk, når du gemmer ændringerne). Du kan tilpasse navnet. Du kan f.eks. ændre det til *Lagsynlighed*. Vælg **Gem**, når du er færdig.
    1. Vælg **Tildel rolle**, og vælg derefter **Systemadministrator**. Hvis der er en rolle med navnet **Common Data Service Bruger**, skal du også vælge den.

    Du kan finde flere oplysninger under [Oprette en programbruger](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).

1. Hvis dit standardsprog for Dataverse ikke er **engelsk**:

    1. Gå til **Avancerede indstillinger \> Administration \> Sprog**.
    1. Vælg **Engelsk (LanguageCode=1033)**, og vælg **Anvend**.

1. Importér `Inventory Visibility Dataverse Solution.zip`-filen, der indeholder Dataverse-konfigurationsrelaterede enheder, og Power Apps:

    1. Gå til siden **Løsninger**.
    1. Vælg **Importér**.

1. Importér udløserflowet for konfigurationsopgradering:

    1. Gå til siden Microsoft Flow.
    1. Kontrollér, at forbindelsen med navnet *Dataverse (ældre)* findes. (Hvis den ikke findes, skal du oprette den).
    1. Importér filen `Inventory Visibility Configuration Trigger.zip`. Når den er importeret, vises udløseren under **Mine flow**.
    1. Start følgende fire variabler på basis af miljøoplysningerne:

        - Azure-lejer-id
        - Azure-programklient-id
        - Azure-programklienthemmelighed
        - Slutpunkt for lagersynlighed

            Du kan finde flere oplysninger om denne variabel under [Konfigurere integration af lagersynlighed](#setup-inventory-visibility-integration) senere i dette emne.

        ![Konfigurationsudløser.](media/configuration-trigger.png "Konfigurationsudløser")

    1. Vælg **Slå til**.

### <a name="install-the-add-in"></a><a name="install-add-in"></a>Installer tilføjelsesprogrammet

For at installere tilføjelsesprogrammet Lagersynlighed skal du gøre følgende:

1. Log på portalen [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).
1. Vælg det projekt, dit miljø skal implementeres i, på startsiden.
1. Vælg det miljø, som tilføjelsesprogrammet skal installeres i, på projektsiden.
1. Rul ned på miljøsiden, indtil du ser afsnittet **Miljøtilføjelsesprogrammer** i sektionen **Power Platform-integration**, hvor du kan finde Dataverse-miljønavnet.
1. Vælg **Installér et nyt tilføjelsesprogram** i afsnittet **Tilføjelsesprogrammer for miljø**.

    ![Miljøsiden i LCS.](media/inventory-visibility-environment.png "Miljøsiden i LCS")

1. Vælg linket **Installer et nyt tilføjelsesprogram**. Der åbnes en liste over tilgængelige tilføjelsesprogrammer.
1. Vælg **Lagersynlighed** på listen.
1. Angiv værdier for følgende felter til dit miljø:

    - **AAD-program-id (klient)**
    - **AAD-lejer-id**

    ![Konfigurationsside for tilføjelsesprogram.](media/inventory-visibility-setup.png "Konfigurationsside for tilføjelsesprogram")

1. Acceptér vilkårene og betingelsen ved at markere afkrydsningsfeltet **Vilkår og betingelser**.
1. Vælg **Installer**. Status for tilføjelsesprogrammet vil blive vist som **installerer**. Når det er gjort, skal du opdatere siden for at se statusændringen til **Installeret**.

### <a name="uninstall-the-add-in"></a><a name="uninstall-add-in"></a>Fjern tilføjelsesprogrammet

Hvis du vil fjerne tilføjelsesprogrammet, skal du vælge **Fjern**. Når du opdaterer LCS, fjernes tilføjelsesprogrammet Lagersynlighed. Fjernelsesprocessen fjerner registreringen af tilføjelsesprogrammet og starter også et job for at rydde op i alle de forretningsdata, der er gemt i tjenesten.

## <a name="consume-on-hand-inventory-data-from-supply-chain-management"></a>Forbruge data i den tilgængelige lagerbeholdning fra Supply Chain Management

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a>Implementere integrationspakken Lagersynlighed

Hvis du kører Supply Chain Management version 10.0.17 eller tidligere, skal du kontakte supportteamet for onboarding af lagersynlighed på [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) for at hente pakkefilen. Implementer derefter pakken i LCS.

> [!NOTE]
> Hvis der opstår uoverensstemmelse mellem versioner under installationen, skal du importere projektet X++ manuelt til udviklingsmiljøet. Opret derefter implementeringspakken i udviklingsmiljøet, og implementer den i produktionsmiljøet.
> 
> Koden er inkluderet i Supply Chain Management version 10.0.18. Hvis du kører denne version eller en senere, er det ikke påkrævet.

Sørg for, at følgende funktioner er aktiveret i dit Supply Chain Management-miljø. (Som standard er de aktiveret).

| Funktionsbeskrivelse | Kodeversion | Skifte klasse |
|---|---|---|
| Aktivere eller deaktivere ved hjælp af lagerdimensioner i tabellen InventSum | 10.0.11 | InventUseDimOfInventSumToggle |
| Aktivere eller deaktivere ved hjælp af lagerdimensioner i tabellen InventSumDelta | 10.0.12 | InventUseDimOfInventSumDeltaToggle |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a>Konfigurer integration af lagersynlighed

1. I Supply Chain Management skal du åbne arbejdsområdet **[Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** og aktivere funktionen **Integration af lagersynlighed**.
1. Gå til **Lagerstyring \> Konfiguration \> Parametre for integration af lagersynlighed**, og angiv URL-adressen for det miljø, hvor du kører lagersynlighed.

    Find LCS-miljøets Azure-område, og angiv derefter URL-adressen. URL-adressen har følgende format:

    `https://inventoryservice.<RegionShortName>-il301.gateway.prod.island.powerapps.com`

    Hvis du f.eks. er i Europa, har dit miljø en af følgende URL-adresser:

    - `https://inventoryservice.neu-il301.gateway.prod.island.powerapps.com`
    - `https://inventoryservice.weu-il301.gateway.prod.island.powerapps.com`

    Følgende områder er tilgængelige i øjeblikket.

    | Azure-region | Områdets korte navn |
    |---|---|
    | Det østlige Australien | eau |
    | Det sydøstlige Australien | seau |
    | Det centrale Canada | cca |
    | Det østlige Canada | eca |
    | Nordeuropa | neu |
    | Vesteuropa | weu |
    | Det østlige USA | eus |
    | Det vestlige USA | wus |

1. Gå til **Lagerstyring \> Periodisk \> Integration af lagersynlighed**, og aktivér jobbet. Alle hændelser med lagerændringer fra Supply Chain Management vil nu blive bogført i Lagersynlighed.

## <a name="the-inventory-visibility-add-in-public-api"></a><a name="inventory-visibility-public-api"></a>Den offentlige API for tilføjelsesprogrammet Lagersynlighed

Den offentlige REST-API til tilføjelsesprogrammet Lagersynlighed viser flere specifikke slutpunkter for integration. Det understøtter tre overordnede interaktionstyper:

- Bogføring af ændret lagerbeholdning i tilføjelsesprogrammet fra et eksternt system
- Forespørgsel om aktuelle disponible lagerantal fra et eksternt system
- Automatisk synkronisering med lagerbeholdning i Supply Chain Management

Automatisk synkronisering er ikke en del af den offentlige API. Den håndteres i stedet i baggrunden for miljøer, hvor tilføjelsesprogrammet Lagersynlighed er aktiveret.

### <a name="authentication"></a><a name="inventory-visibility-authentication"></a>Godkendelse

Sikkerhedstoken til platformen bruges til at kalde tilføjelsesprogrammet Lagersynlighed. Du skal derfor generere et *Azure Active Directory-token (Azure AD)* ved hjælp af Azure AD-programmet. Du skal derefter bruge Azure AD-tokenet til at hente *adgangstoken* fra sikkerhedstjenesten.

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

### <a name="sample-request"></a><a name="inventory-visibility-sample-request"></a>Eksempelanmodning

Til reference er der en eksempel http-anmodning, og du kan bruge værktøjer eller kodningssprog til at sende denne anmodning, f.eks. ``Postman``.

```json
# Url
# replace {RegionShortName} and {EnvironmentId} with your value
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand

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
    "quantities": {
        "pos": {
            "inbound": 5
        }  
    },
    "dimensions": {
        "SizeId": "Small",
        "ColorId": "Red",
        "SiteId": "1",
        "LocationId": "11"
    }
}
```

### <a name="configure-the-inventory-visibility-api"></a><a name="inventory-visibility-configuration"></a>Konfigurere API'et til Lagersynlighed

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

Indekseringen definerer, hvordan du kan gruppere resultaterne baseret på `groupBy`-forespørgselsindstillingen. Hvis du ikke definerer `groupBy`-værdier, får du totaler med `productid`. Hvis du definerer `groupBy` som `groupBy=ColorId&groupBy=SizeId`, får du ellers flere linjer baseret på de forskellige kombinationer af farve og størrelse i systemet.

Du kan sætte dine forespørgselskriterier i anmodningsteksten.

Her er et eksempel på en forespørgsel på produktet med en kombination af farve og størrelse.

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct1", "MyProduct2"],
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

For feltet `filters` understøtter kun `ProductId` i øjeblikket flere værdier. Hvis `ProductId` er en tom matrix, forespørges på alle produkter.

#### <a name="custom-measurement"></a>Brugerdefineret måling

Standardmåleantallet er kædet sammen med Supply Chain Management. Det kan dog være en god ide at have et antal, der består af en kombination af standardmålene. Hvis du vil gøre dette, kan du have en konfiguration af brugerdefinerede antal, der føjes til outputtet af forespørgsler på den disponible lagerbeholdning.

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
