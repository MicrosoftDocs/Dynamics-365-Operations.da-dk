---
title: Commerce-analyser (forhåndsversion)
description: Dette emne forklarer, hvordan du installerer og bruger analysefunktionaliteten i Microsoft Dynamics 365 Commerce.
author: AamirAllaq
ms.date: 02/24/2022
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2021-11-12
ms.openlocfilehash: 63d6e5ef7e883578106495d5ec778bbd686ee92d
ms.sourcegitcommit: 722854cb0d302d01ce3d9580ac80dc7c23d19bf5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/06/2022
ms.locfileid: "8550001"
---
# <a name="commerce-analytics-preview"></a>Commerce-analyser (forhåndsversion)

[!include [banner](includes/banner.md)]

Dette emne forklarer, hvordan du installerer Commerce-analyser (forhåndsversion), den funktionelle analysefunktionalitet, der findes i Microsoft Dynamics 365 Commerce.

## <a name="commerce-analytics-preview-live-demo"></a>Commerce-analyser (forhåndsversion) live demo

Du kan prøve en [live demo af Commerce-analyser (forhåndsversion)](https://aka.ms/CommerceAnalyticsDemo).

![Commerce-analyser (forhåndsversion) Oversigt](media/CommerceAnalytics_Summary.png)
![Commerce-analyser (forhåndsversion) Betalinger](media/CommerceAnalytics_Payments.png)
![Commerce-analyser (forhåndsversion) Web-aktivitet](media/CommerceAnalytics_WebActivity.png)

## <a name="commerce-analytics-preview-system-architecture"></a>Systemarkitektur i Commerce-analyser (forhåndsversion)

### <a name="key-components"></a>Nøglekomponenter

Commerce-analyser (forhåndsversion) består af følgende nøglekomponenter:

- Interaktive Power BI-rapporter, der er klar til brug
- SQL-visninger i Azure Synapse Analytics
- Enhedsdata og ontologidata i Azure Data Lake
- Rådata i Data Lake

![Nøglekomponenter i systemarkitektur i Commerce-analyser](media/CommerceAnalyticsArchitecture_v2.png)

### <a name="data-flow"></a>Dataflow

#### <a name="step-1-data-generation"></a>Trin 1: Generering af data

Data stammer enten som transaktionsdata eller adfærdsmæssige data fra en af følgende kilder:

- Et callcenter, der tilknyttes, bruger Commerce HQ-klienten til at behandle salgsordrer.
- En kasserer på POS behandler salgstransaktioner.
- Salg oprettes i tilpassede programmer ved hjælp af Headless Commerce (Commerce Scale Unit).
- En e-handelskunde gennemser dit e-handelswebsted.
- En e-handelskunde placerer en ordre på dit e-handelswebsted.
- Data produceres af andre systemer, f.eks. Dynamics 365 Connected Spaces.

#### <a name="step-2-ingestion-and-pre-processing"></a>Trin 2: Indtagelse og forbehandling

Transaktionsdata går til Commerce HQ enten direkte (hvis det drejer sig om ordrer, der er registreret direkte i Commerce HQ-klienten) eller via Commerce Scale Unit (ved ordrer, der registreres i pos, i e-handel eller i brugerdefinerede klienter, der bruger headless commerce).

Funktionen Eksporter til Data Lake bruges derefter til at kopiere transaktionsdataene til din datasø som rådata. I datasøen gemmes de rådata i mappen Tabeller.

Webaktivitetsdata for e-handel sendes direkte til datasøen. Data, der produceres af andre systemer, f.eks. Dynamics 365 Connected Spaces sendes direkte til datasøen af disse systemer.

#### <a name="step-3-transformation-and-aggregation"></a>Trin 3: Transformation og aggregering

Når rådata er i din datasø, læser Commerce-analyser det, transformerer det, aggregerer det og skriver det tilbage til datasøen i form af logiske enheder (i mappen Enheder) og aggregerede metriske værdier (i mappen Ontologier).

#### <a name="step-4-querying"></a>Trin 4: Forespørgsel

Azure Synapse Analytics bruges til at forespørge på data i datasøen via en Transact-SQL-grænseflade (T-SQL). Denne brugergrænseflade indeholder SQL-visninger. SQL-visninger gør det muligt at sammenkæde forespørgsler på data i datasøen, enten direkte via en T-SQL-klient (til ad hoc-analyse) eller via et visualiseringsværktøj som f.eks. Power BI.

#### <a name="step-5-modeling-and-serving"></a>Trin 5: Modellering og betjening

Data, der forespørges af Azure Synapse Analytics, går til den semantiske model i Power BI. Afhængigt af datatypen importeres den enten periodisk i hukommelsen til Power BI eller forespørges direkte under kørslen.

Endelig gengives dataene i Power BI-visuelle billeder, så brugerne kan se og bruge dem.

## <a name="commerce-analytics-preview-functional-overview"></a>Commerce-analyser (forhåndsversion) af funktionel oversigt

### <a name="summary"></a>Resumé

Appen til skabelonen Commerce-analyser indeholder følgende hovedrapportsider:

1. [Filtre på øverste niveau](#TopLevelFilters)
2. [Produkter](#ProductsPage)
3. [Kunder](#CustomersPage)
4. [Kanaler](#ChannelsPage)
5. [Salg](#SalesPage)
6. [Margener](#MarginsPage)
7. [Returvarer](#ReturnsPage)
8. [Rabatter](#DiscountsPage)
9. [Betalinger](#PaymentsPage)
10. [Kunder](#CustomersPage)
11. [Sammenligning](#ComparisonPage)
12. [Web-aktivitet](#WebActivityPage)
13. [Webaktivitet - Filter på øverste niveau](#WebActivityTopLevelFilters)

#### <a name="top-level-filters"></a><a name="TopLevelFilters"></a> Filtre på øverste niveau

- Datoindstillinger

    - År
    - Kvartal
    - Måned
    - Uge
    - Dag

- Kanalindstillinger

    - Juridisk enhed
    - Kanaltype
    - Kundetype
    - Salgstype
    - Kanal
    - Organisationshierarki

- Produktindstillinger

    - Kategorihierarki
    - Kategori

#### <a name="products"></a><a name="ProductsPage"></a> Produkter

- Sales
- Avance
- Returvarer

#### <a name="customers"></a><a name="CustomersPage"></a> Kunder

- Sales
- Avance
- Returvarer

#### <a name="channels"></a><a name="ChannelsPage"></a> Kanaler

- Sales
- Avance
- Returvarer

### <a name="sales"></a>Salg <a name="SalesPage"></a>

- Levering efter lokation
- Efter kanal/butik/terminal
- Efter medarbejder
- Efter dato
- Efter time
- Efter produktkategori

### <a name="margins"></a><a name="MarginsPage"></a> Margener

- Levering efter lokation
- Biprodukt
- Efter dato

### <a name="returns"></a><a name="ReturnsPage"></a> Returvarer

- Retur efter beløb

    - Via lager
    - Biprodukt
    - Efter dato

- Retur efter transaktion

    - Via lager
    - Biprodukt
    - Efter dato

### <a name="discounts"></a><a name="DiscountsPage"></a> Rabatter

- Via lager
- Biprodukt
- Efter dato
- Opdeling

    - Juridisk enhed
    - Gem
    - Rabattype
    - Rabatnavn
    - Produkt

### <a name="payments"></a><a name="PaymentsPage"></a> Betalinger

- Efter kanal/terminal
- Efter betalingsmetode/-type
- Efter dato
- Opdeling

    - Juridisk enhed
    - Kanaltype
    - Gem
    - Terminal
    - Betalingsmetode

### <a name="customers"></a><a name="CustomersPage"></a> Kunder

- Levetidsværdi (LTV)

    LTV beregnes på basis af det samlede beløb, som en kunde bruger på tværs af alle Dynamics 365 Commerce-salgskanaler (herunder POS, e-handel og callcenter).

- Recency

    Recency beregnes på basis af det antal dage, der er gået, siden en debitors seneste transaktionsreaktion med organisationen. I øjeblikket tager Recency ikke højde for ikke-transaktionsbaserede engagementssignaler, som f.eks. via browser-aktivitet i e-handel.

- Frekvens

    Frekvens beregnes på basis af debitors seneste transaktionsengagement med organisationen. I øjeblikket tager frekvens ikke højde for ikke-transaktionsbaserede engagementssignaler, som f.eks. via browser-aktivitet i e-handel.

- Relationslængde

    Relationslængde beregnes på basis af det antal dage, siden debitorposten blev oprettet i systemet.

- Antal transaktioner

### <a name="comparison"></a><a name="ComparisonPage"></a> Sammenligning

- Produktsammenligning efter tidsperiode

    - Salgs- og salgsdifference
    - Margen og margendifference

- Debitor efter tidsperiode

    - Salgs- og salgsdifference
    - Margen og margendifference

### <a name="web-activity"></a><a name="WebActivityPage"></a> Web-aktivitet

#### <a name="top-level-filters"></a><a name="WebActivityTopLevelFilters"></a> Filtre på øverste niveau

- Datointerval
- Kanaltype
- Kanal
- Kategorihierarki

#### <a name="acquisitions"></a>Anskaffelser

- Sidevisninger

    - Efter land eller område
    - Biprodukt
    - Efter brugers status som logget på
    - Efter dato

- E-handelsordrer
- Konverteringsfrekvens

    - Efter dato

- Omregningstragt

    - Sidevisning efter sidetype (startside, kategoriside eller produktdetaljeside)
    - Føj til indkøbsvogn
    - Kasse
    - Køb

#### <a name="sessions"></a>Sessioner

En session er en del af en brugers besøg på dit e-handelswebsted. En session betragtes som afsluttet efter 30 minutters inaktivitet eller 24 timers aktiv brug.

- Efter land eller område
- Efter oprindelse (ekstern reference)
- Efter brugers status som logget på
- Sessionsoptælling

    - Efter dato
    - Efter indtastningsside

- Ordre efter session

    - Efter dato

- Sats for sessionsabsorbering

    En sessionsabsorbering er en session, hvor en bruger forlader dit e-handelswebsted umiddelbart efter, at de har besøget dit e-handelswebsted. Du kan finde flere oplysninger under [Absorberingssats](https://en.wikipedia.org/wiki/Bounce_rate).

- Klik pr. session

#### <a name="visitors"></a>Besøgende

En anonymt besøgende på dit e-handelswebsted er entydigt identificeret ud fra den specifikke browser og den specifikke enhed, som brugeren bruger. Commerce-analyser sporer ikke anonyme brugere på tværs af forskellige browsere eller enheder. En anonym besøgende, der bruger samme browser på samme enhed, identificeres entydigt på tværs af flere brugersessioner, indtil enten browserens cache-lagrede data er ryddet, eller en periode (typisk 12 måneder) er passeret, afhængigt af hvad der indtræffer først.

Hvis brugere gennemser dit e-handelswebsted, mens de er logget på, kan Commerce-analyser indeholde flere oplysninger om dem. Disse oplysninger er baseret på den eksisterende relation, som organisationen har med de foregående indkøb på tværs af alle Dynamics 365 Commerce-salgskanaler (herunder POS, e-handel og callcenter). De yderligere oplysninger omfatter recency, relationslængde, levetidsværdi og frekvensdata.

- Margen for besøgende
- Gennemsnitsordrer for besøgende
- Gennemsnitssalg for besøgende
- Optælling af e-handelsbesøgende

    - Efter dato
    - Efter placering

        I øjeblikket kan Commerce-analyser kun give granularitet på lande-/områdeniveau til lokationsindsigt for e-handelskunder.

    - Efter recency

        Recency beregnes på basis af det antal dage, der er gået, siden en debitors seneste transaktionsreaktion med organisationen. I øjeblikket tager Recency ikke højde for ikke-transaktionsbaserede engagementssignaler, som f.eks. via browser-aktivitet i e-handel.

    - Efter relationslængde

        Relationslængde beregnes på basis af det antal dage, siden debitorposten blev oprettet i systemet.

    - Efter levetidsværdi (LTV)

        LTV beregnes på basis af det samlede beløb, som en kunde bruger på tværs af alle Dynamics 365 Commerce-salgskanaler (herunder POS, e-handel og callcenter).

    - Efter frekvens

        Frekvens beregnes på basis af debitors seneste transaktionsengagement med organisationen. I øjeblikket tager frekvens ikke højde for ikke-transaktionsbaserede engagementssignaler, som f.eks. via browser-aktivitet i e-handel.

#### <a name="impressions"></a>Udtryk

Et eksempel er et enkelt visning af en produkt-visual efter en e-handelsbesøgende. En e-handel går f.eks. til startsiden for e-handelswebstedet og ser et produkt på et yogamåtteprodukt i et modul med **Topsalgsliste**. På den måde vises det samme produkt på rullelisten i et listemodul **Udvalgt til dig**. I dette tilfælde er der to produktudtryk.

Aktuelt spores det efter følgende fremgangsmåder:

- Lister (f.eks. **Anbefalet**, **Topsalg**, **Udvalgt til dig** og **Tendenser**)
- Indkøbskurvsmodul
- Søg i resultatcontainer
- Kategorisøgning i resultatcontainer

I øjeblikket tælles produkter, der er gengivet i et karruselmodul eller i brugerdefineret visuel visning, tælles ikke impressionsrelaterede målepunkter.

Siden **Impressionsrapport** indeholder følgende målepunkter:

- Impressionsoptælling

    - Efter sidetype og modul

        Sidetype er den generiske type side, der er defineret for hver side på dit e-handelswebsted. Modultype er den type visuelt modul til e-handel, som produktet vises i.

        Hvis du vil have vist elementer efter modul, kan du være nødt til at foretage en detailudsigt for siden og modulet visuel visning.

    - Biprodukt
    - Efter brugers status som logget på
    - Efter dato

- Impressionsklikoptælling

    Et impressionsklik forekommer, når en e-handel markerer en visuel visning af produkt. Typisk bliver den besøgende ført til siden med produktdetaljer for produktet.

- Klik på gennemsynssats (CTR)

    CTR beregnes som det samlede antal klik på klik, der er opdelt i det samlede antal udtryk.

## <a name="commerce-analytics-preview-installation"></a>Commerce-analyser (forhåndsversion), installation

> [!NOTE]
> Commerce-analyser (forhåndsversion) er som forhåndsversion i USA, Canada, Storbritannien, Europa, Sydøstasien, Østasien, Australien og Japan. Hvis dit Finans- og driftsmiljø findes i nogen af disse områder, kan du aktivere denne funktion i dit miljø ved hjælp af Microsoft Dynamics Lifecycle Services (LCS). Før du kan bruge denne funktion, skal du se [Konfigurere eksport til Azure Data Lake](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

### <a name="enable-and-configure-commerce-analytics-preview"></a><a name="enableCommerceAnalytics"></a>Aktivere og konfigurere Commerce-analyser (forhåndsversion)

Hvis du vil installere Commerce-analyser (forhåndsversion), skal du have rettigheder til at oprette ressourcer i et Azure-abonnement. Du skal også have rettigheder til at installere tilføjelsesprogram i LCS.

Hvis du vil aktivere og konfigurere Commerce-analyser (forhåndsversion), skal du følge disse trin.

1. [Send formen Forhåndsversionsindtagelse for Commerce-analyse (forhåndsversion)](#joinPreview)
2. [Aktivere og konfigurere tilføjelsesprogrammet Eksportér til Data Lake](#enableExportToDataLake).
3. [Installer og konfigurer et Azure Synapse workspace](#configureAzureSynapse).
4. [Føj hemmeligheder til Key Vault](#addSecrets).
5. [Aktivere og konfigurere tilføjelsesprogram for Commerce-analyser (forhåndsversion)](#enableCommerceAnalyticsAddin).
6. [Installere skabelonappen Power BI](#powerbi).

### <a name="submit-the-preview-intake-form-for-commerce-analytics-preview"></a><a name="joinPreview"></a>Send formen Forhåndsversionsindtagelse for Commerce-analyse (forhåndsversion)

Send [Formen Forhåndsversionsindtagelse for Commerce-analyse (forhåndsversion)](https://forms.office.com/r/vW5VLJGXZ2). Når din anmodning er behandlet, sendes der en bekræftelsesmail til den mailadresse, du har angivet i formen.

### <a name="enable-and-configure-the-export-to-data-lake-add-in"></a><a name="enableExportToDataLake"></a>Aktivere og konfigurere tilføjelsesprogrammet Eksportér til Data Lake

> [!IMPORTANT]
> Når du konfigurerer tilføjelsesprogrammet Eksportér til Data Lake, skal du fjerne markeringen i afkrydsningsfeltet **Ændringer af data i realtid** på siden Konfigurer tilføjelsesprogrammet Eksportér til Data Lake for at sikre, at dataændringer i realtid ikke er aktiveret. Funktionen **Ændringer af data i realtid** er i forhåndsversion, og den understøttes ikke i øjeblikket af Commerce-analyser. Hvis du aktiverer funktionen, vil Commerce-analyser ikke kunne behandle dine data i datasøen, og de fleste af Power BI-rapporterne indeholder ingen data.

Commerce-analyser (forhåndsversion) er baseret på funktionen Eksportér til Data Lake til at eksportere Commerce-hovedkontorets data til Data Lake og holde dataene opdateret. Før du konfigurerer Commerce-analyser (Forhåndsversion), skal du aktivere og konfigurere Eksport til Data Lake ved at følge trinnene i [Konfigurer eksport til Azure Data Lake](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

Når du konfigurerer tilføjelsesprogrammet Eksportér til Data Lake, skal du notere følgende oplysninger, da du skal angive dem senere:

- <a name="keyVault"></a>DNS-navnet (Domain Name System) for den Key Vault, du har angivet.
- De hemmelige navne, du har angivet, og som indeholder program-id'et og programhemmeligheden. Du kan finde flere oplysninger i [Tilføj hemmeligheder til Key Vault](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#addsecrets).

### <a name="install-and-configure-an-azure-synapse-workspace"></a><a name="configureAzureSynapse"></a>Installer og konfigurer et Azure Synapse workspace

Commerce-analyser (forhåndsvisning) kræver, at Synapse SQL efter anmodning klargøres i Azure Synapse workspace. Hvis du vil installere og konfigurere et Azure Synapse workspace, skal du følge disse trin.

1. Installer et Azure Synapse workspace i dit Azure-abonnement. Du kan finde flere oplysninger under [Hurtig start: Opret et Synapse-arbejdsområde](/azure/synapse-analytics/quickstart-create-workspace).
1. <a name="serverlessep"></a>Når arbejdsområdet er klargjort, skal du åbne oversigtssiden for ressourcer og notere dig værdien af **Serverløst SQL-slutpunkt**. Denne værdi skal lagres i Key Vault i næste afsnit.
1. Vælg linket **Åbn Synapse Studio** på oversigtssiden for at åbne Azure Synapse Studio til dit arbejdsområde.
1. Vælg **Administrer** i menuen til venstre. Hvis du vil se menunavnene, skal du muligvis vælge udvid-linket i venstre menu.
1. Vælg **Adgangskontrol** under **Sikkerhedsgruppe**. 
1. Vælg **Tilføj**.
1. I ruden **Tilføj rolletildeling** skal du angive indstillingerne som beskrevet i følgende tabel.

    | Indstilling | Værdi |
    |--------|-------|
    | Område | Vælg **Arbejdsområde**. |
    | Rolle | Vælg **Synapse SQL-administrator**.|
    | Vælg bruger | Søg efter navnet på det program, du [oprettede under installationen af tilføjelsesprogrammet Eksportér til Data Lake](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createapplication). Når programmet vises i søgeresultaterne, skal du vælge det. Programmet vises nu i sektionen **Valgte brugere, grupper eller tjenesteprincipaler**. |

1. Vælg **Anvend** for at fuldføre rolletildelingen. Programmet tildeles rettigheder som Synapse SQL-administrator. Det kan derfor oprette de påkrævede visninger under konfigurationen af LCS-tilføjelsesprogrammet Commerce-analyser (forhåndsversion).

### <a name="add-secrets-to-the-key-vault"></a><a name="addSecrets"></a>Føj hemmeligheder til Key Vault

I den samme [Key Vault](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createkeyvault), som du brugte, da du konfigurerede tilføjelsesprogrammet Eksportér til Data Lake,skal du tilføje de hemmeligheder, der er vist i følgende tabel. Du skal angive et hemmeligt navn og den angivne værdi for hver hemmelighed.

| Foreslået hemmeligt navn | Hemmelig værdi | Eksempel på hemmelig værdi |
|---------|---------|---------|
| synapse-sql-server | Den serverløse SQL-slutpunktsværdi, du noterede, da du [konfigurerede Azure Synapse workspace](#serverlessep). | `test-ondemand.sql.azuresynapse.net` |
| <a name="roUser"></a>readonly-sql-pwd | Den adgangskode, der skal angives for den skrivebeskyttede SQL-bruger. Rapporten i Power BI bruger denne adgangskode til at oprette forbindelse til den serverløse SQL. Følg din organisations adgangskodepolitikker for at angive adgangskoden. | |

### <a name="enable-and-configure-the-commerce-analytics-preview-add-in"></a><a name="enableCommerceAnalyticsAddin"></a>Aktivere og konfigurere tilføjelsesprogram til Commerce-analyser (forhåndsversion)

Hvis du vil installere tilføjelsesprogrammet Commerce-analyser (forhåndsversion) i LCS, skal du være miljøadministrator i LCS for det miljø, du vil bruge.

Hvis du vil installere og konfigurere tilføjelsesprogram i Commerce-analyser (forhåndsversion), skal du følge dette trin.

1. Log på [LCS](https://lcs.dynamics.com/), og gå til dit miljø.
2. Vælg **Installér et nyt tilføjelsesprogram** på fanen **Tilføjelsesprogrammer for miljø** på siden **Miljø**.
3. Vælg **Handelsanalyser (forhåndsversion)** i dialogboksen.
4. I dialogboksen **Konfigurer tilføjelse** skal du angive følgende oplysninger.

    | Oplysninger | Kilde | Eksempelværdi |
    |---|---|---|
    | Azure Active Directory-lejer-id (Azure AD) | Log på [Azure-portalen](https://portal.azure.com/), og åbn **Azure Active Directory**-tjenesten. Åbn derefter siden **Egenskaber**, og kopiér værdien i feltet **Lejer-id**. | `72f988bf-0000-0000-00000-2d7cd011db47` |
    | DNS-navn for din Azure Key Vault | Angiv DNS-navn for Key Vault. Du skulle have noteret dig denne værdi, da du [konfigurerede tilføjelsesprogrammet Eksportér til Data Lake](#keyVault). | `https://contosod365datafeedpoc.vault.azure.net/` |
    | Hemmeligt navn, der indeholder program-id | Angiv det hemmelige navn på den adresse, hvor program-id opbevares. Du skulle have noteret dig denne værdi, da du [konfigurerede tilføjelsesprogrammet Eksportér til Data Lake](#keyVault). | `app-id` |
    | Hemmeligt navn, der indeholder programhemmelighed | Angiv det hemmelige navn på den adresse, hvor programhemmelighed opbevares. Du skulle have noteret dig denne værdi, da du [konfigurerede tilføjelsesprogrammet Eksportér til Data Lake](#keyVault). | `app-secret` |
    | Hemmeligt navn, der indeholder det serverløse SQL-slutpunkt til Azure Synapse | Angiv det hemmelige navn, hvor det serverløse SQL-slutpunkt opbevares. Du skulle have oprettet hemmeligheden, mens du [føjede hemmeligheder til nøgleværdien](#addSecrets). | `synapse-sql-server` |
    | Hemmeligt navn, der indeholder den adgangskode, der skal angives for skrivebeskyttede SQL-brugere i Azure Synapse | Angiv det hemmelige navn, der gemmer den adgangskode, der skal angives for den serverløse, skrivebeskyttede SQL-bruger. Denne bruger oprettes for dig og skal bruges i Power BI-rapporten til at oprette forbindelse til den serverløse SQL-server. Du skulle have oprettet hemmeligheden, mens du [føjede hemmeligheder til nøgleværdien](#addSecrets). | `readonly-sql-pwd` |

1. Accepter tilbuddets betingelser ved at markere afkrydsningsfeltet, og vælg derefter **Installer**.

    Systemet installerer og konfigurerer tilføjelsesprogrammet Commerce-analyse (forhåndsversion) for miljøet. Denne proces kan tage nogle få minutter. Når den er fuldført, skal **Commerce-analyse (Forhåndsversion)** vises på siden **Miljø**, og status skal være **Installeret**.

### <a name="install-the-power-bi-template-app"></a><a name="powerbi"></a>Installér Power BI-skabelonapp

Hvis du vil installere Power BI-skabelonapp til Commerce-analyser (forhåndsversion), skal du følge disse trin.

1. Log på portalen [Power BI](https://powerbi.microsoft.com/) ved hjælp af dit organisations-id.
1. Installer Commerce-analyser (Forhåndsversion) Power BI-skabelonappen ved at gå til [https://aka.ms/cdireport-installapp](https://aka.ms/cdireport-installapp). Du kan også gå til [AppSource-siden for Dynamics 365 Commerce-analyser](https://appsource.microsoft.com/product/power-bi/dynamics-365-commerce.dydnamics-365-commerce-analytics) og vælge **Hent den nu**.
1. Hvis du installerer appen første gang, skal du gå videre til trin 5. Hvis du har installeret den før, vises følgende indstillinger for opdatering af appen:

    - **Opdater arbejdsområdet og appen** – Opdater den eksisterende skabelonapp, og overskriv dine eksisterende appindstillinger, f.eks. konfigurationer af appforekomster og tilladelser.
    - **Opdater kun indholdet på arbejdsområdet uden at opdatere appen** – Opdater den eksisterende skabelonapp, men behold dine eksisterende appindstillinger. *Denne indstilling er den anbefalede indstilling for appopdateringer.*
    - **Installer en anden kopi af appen i et nyt arbejdsområde** – Opret et nyt arbejdsområde, og opret derefter en kopi af den eksisterende skabelonapp i det. Det eksisterende arbejdsområde bevares.

1. Vælg en af opdateringsindstillingerne, og vælg derefter **Installer**.
1. Åbn den installerede app ved at vælge **Apps** i venstre rude og derefter vælge appen.
1. Opret forbindelse mellem appen og datakilden ved at vælge **Tilslut**. Hvis du har installeret appen før, skal du vælge linket **Tilknyt dit datalink** på den gule meddelelseslinje.
1. Angiv følgende felter.

    | Felt | Værdi |
    |---|---|
    | Server | Angiv det serverløse SQL-slutpunkt, du noterede, efter at du [oprettede Azure Synapse workspace](#serverlessep). |
    | Database | Angiv **CommerceAnalytics**. |
    | Sprog | Vælg en værdi fra listen. Dette felt bruges til lokale produkt- og kategorinavne. Værdien er følsom over for store og små bogstaver. |
    | Datointerval | Vælg en værdi fra listen. Data for det valgte antal måneder importeres til Power BI-datasættet. Den værdi, du vælger, har indflydelse på størrelsen på datasættet og den tid, der kræves til synkroniseringen. |

1. Vælg **Næste**. Når du bliver bedt om at angive legitimationsoplysningerne til oprettelse af forbindelse til Azure Synapse SQL-databasen, skal du angive feltværdierne som vist i følgende tabel.

    | Felt | Værdi |
    |---|---|
    | Godkendelsesmetode | Vælg **Basis**. |
    | Brugernavn | Angiv **reportreadonlyuser**. |
    | Adgangskode | Angiv den adgangskode, du har [gemt for den skrivebeskyttede SQL-bruger i Key Vault](#roUser). |

1. Vælg **log på, og opret forbindelse**.
1. Vent, indtil datasættet er opdateret korrekt. Vælg derefter **Rediger app** for at åbne App-arbejdsområdet, hvor du kan få vist opdateringsstatus for datasættet. I apparbejdsområdet kan du også vælge at oprette automatiske opdateringsplaner for dit datasæt, administrere tilladelser og omdøbe app-forekomsten.

### <a name="privacy"></a><a name="privacy"></a>Beskyttelse

Det er vigtigt for os at beskytte dine personlige oplysninger. Du kan få mere at vide ved at læse vores [erklæring om beskyttelse af personlige oplysninger](https://go.microsoft.com/fwlink/?LinkId=521839).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
