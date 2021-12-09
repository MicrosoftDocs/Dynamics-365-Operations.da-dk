---
title: Commerce-analyser (forhåndsversion)
description: Dette emne forklarer, hvordan du installerer og bruger analysefunktionaliteten i Microsoft Dynamics 365 Commerce.
author: AamirAllaq
ms.date: 11/23/2021
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2021-11-12
ms.openlocfilehash: 8cfe2af756315b5be3eb22d99376a96166fffc52
ms.sourcegitcommit: f9fca3d55b47e615e5ef64669dab184e057ec234
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/23/2021
ms.locfileid: "7862767"
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
- SQL-visninger i Azure Synapse-analyser
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

Azure Synapse-analyser bruges til at forespørge på data i datasøen via en Transact-SQL-grænseflade (T-SQL). Denne brugergrænseflade indeholder SQL-visninger. SQL-visninger gør det muligt at sammenkæde forespørgsler på data i datasøen, enten direkte via en T-SQL-klient (til ad hoc-analyse) eller via et visualiseringsværktøj som f.eks. Power BI.

#### <a name="step-5-modeling-and-serving"></a>Trin 5: Modellering og betjening

Data, der forespørges af Azure Synapse-analyser går til den semantiske model i Power BI. Afhængigt af datatypen importeres den enten periodisk i hukommelsen til Power BI eller forespørges direkte under kørslen.

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

####  <a name="top-level-filters"></a><a name="TopLevelFilters"></a> Filtre på øverste niveau

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

####  <a name="products"></a><a name="ProductsPage"></a> Produkter

- Sales
- Avance
- Returvarer

####  <a name="customers"></a><a name="CustomersPage"></a> Kunder

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
> Commerce-analyser (forhåndsversion) er som forhåndsversion i USA, Canada, Storbritannien, Europa, Sydøstasien, Østasien, Australien og Japan. Hvis dit Finance and Operations-miljø findes i nogen af disse områder, kan du aktivere denne funktion i dit miljø ved hjælp af Microsoft Dynamics Lifecycle Services (LCS). Før du kan bruge denne funktion, skal du se [Konfigurere eksport til Azure Data Lake](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

### <a name="enable-and-configure-commerce-analytics-preview"></a><a name="enableCommerceAnalytics"></a>Aktivere og konfigurere Commerce-analyser (forhåndsversion)

Hvis du vil installere Commerce-analyser (forhåndsversion), skal du have rettigheder til at oprette ressourcer i et Azure-abonnement. Du skal også have rettigheder til at installere tilføjelsesprogram i LCS. Her er en oversigt over trinnene:

1. [Send formen Forhåndsversionsindtagelse for Commerce-analyse (forhåndsversion)](#joinPreview).
2. [Aktivere og konfigurere Eksportér til Data Lake](#enableExportToDataLake).
3. [Aktivere og konfigurere tilføjelsesprogram for Commerce-analyser (forhåndsversion)](#enableCommerceAnalyticsAddin).
4. [Generér et token for delt adgangsunderskrift (SAS) til din lagerkonto](#getSASToken).
5. [Hent installationsscriptene til Azure Synapse-visninger](#downloadSynapseDeploymentScripts).
6. [Installer og konfigurer et Azure Synapse workspace](#configureAzureSynapse).
7. [Installere skabelonappen Power BI](#powerbi).

### <a name="submit-the-preview-intake-form-for-commerce-analytics-preview"></a><a name="joinPreview"></a>Send formen Forhåndsversionsindtagelse for Commerce-analyse (forhåndsversion)

Send [Formen Forhåndsversionsindtagelse for Commerce-analyse (forhåndsversion)](https://forms.office.com/r/vW5VLJGXZ2). Giv op til tre arbejdsdage til den form, der skal behandles. Når den er behandlet, sendes der en bekræftelses-mail til den e-mailadresse, du har angivet i formen.

### <a name="enable-and-configure-export-to-data-lake"></a><a name="enableExportToDataLake"></a>Aktivere og konfigurere Eksportér til Data Lake

Commerce-analyser (Forhåndsversion) er baseret på funktionen Eksporter til Data Lake til at eksportere HQ-data (Commerce HQ-data) til Data Lake, og de skal være nye. Før du konfigurerer Commerce-analyser (Forhåndsversion), skal du aktivere og konfigurere Eksport til Data Lake ved at følge trinnene i [Konfigurer eksport til Azure Data Lake](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

Når du konfigurerer Eksporter til Data Lake, skal du notere følgende oplysninger, da du skal angive dem senere:

- <a name="keyVault"></a>DNS-navnet (Domain Name System) for key vault og de hemmelige navne, hvor du gemmer program-id'et og applikationen. Du kan finde flere oplysninger i [Tilføj hemmeligheder til Key Vault](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#addsecrets).
- <a name="storageAccount"></a>Navnet på lagerkontoen for forekomsten af Data Lake. Du kan finde flere oplysninger under [Oprette et Data Lake-lager Gen2-konto i dit abonnement](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createsubscription).

### <a name="enable-and-configure-the-commerce-analytics-preview-add-in"></a><a name="enableCommerceAnalyticsAddin"></a>Aktivere og konfigurere tilføjelsesprogram til Commerce-analyser (forhåndsversion)

Hvis du vil installere tilføjelsesprogrammet Commerce-analyser (forhåndsversion) i LCS, skal du være miljøadministrator i LCS for det miljø, du vil bruge.

Hvis du vil installere og konfigurere tilføjelsesprogram i Commerce-analyser (forhåndsversion), skal du følge dette trin.

1. Log på [LCS](https://lcs.dynamics.com/), og gå til dit miljø.
2. Vælg **Installér et nyt tilføjelsesprogram** på fanen **Tilføjelsesprogrammer for miljø** på siden **Miljø**.
3. Vælg **Handelsanalyser (forhåndsversion)** i dialogboksen.

    Hvis **Commerce-analyser (Forhåndsversion)** ikke er angivet, skal du sørge for, at du har aktiveret Insider Program.

4. I dialogboksen **Konfigurer tilføjelse** skal du angive følgende oplysninger.

    | Oplysninger | Kilde | Eksempelværdi |
    |---|---|---|
    | Azure AD Lejer-id for dit miljø | Log på [Azure-portalen](https://portal.azure.com/), og åbn **Azure Active Directory**-tjenesten. Åbn derefter siden **Egenskaber**, og kopier værdien i feltet **Mappe-id**. | 72f988bf-0000-0000-00000-2d7cd011db47 |
    | Angiv DNS-navn for Key Vault | Angiv [DNS-navn](#keyVault) for Key Vault. Du skulle have gjort opmærksom på denne værdi i det foregående afsnit. | `https://contosod365datafeedpoc.vault.azure.net/` |
    | Tekst, der indeholder ansøgnings-id | Angiv [det hemmelige navn på den adresse, hvor program-id opbevares](#keyVault). Du skulle have gjort opmærksom på denne værdi i det foregående afsnit. | app-id |
    | Tekst, der indeholder ansøgningshemmelighed | Angiv [det hemmelige navn på den adresse, hvor programhemmelighed opbevares](#keyVault). Du skulle have gjort opmærksom på denne værdi i det foregående afsnit. | app-hemmelighed |

5. Accepter tilbuddets betingelser ved at markere afkrydsningsfeltet, og vælg derefter **Installer**.

    Systemet installerer og konfigurerer tilføjelsesprogrammet Commerce-analyse (forhåndsversion) for miljøet. Denne proces kan tage nogle få minutter. Når den er fuldført, skal **Commerce-analyse (Forhåndsversion)** vises på siden **Miljø**, og status skal være **Installeret**.

### <a name="generate-a-sas-token-for-your-storage-account"></a><a name="getSASToken"></a>Generere et SAS-token til lagerkontoen

Et SAS-token giver eksterne enheder adgang til din lagerkonto og har et bestemt sæt rettigheder til et begrænset tidsrum. Azure Synapse vil bruge SAS-token til at få adgang til de underliggende data i Data Lake.

> [!NOTE]
> På grund af en kendt begrænsning af Commerce-analyse (Forhåndsversion) mister Azure Synapse-forekomsten adgangen til datasøen, når SAS-token udløber. Når du genererer SAS-token, skal du derfor angive den maksimumudløbsdato, som organisationens sikkerhedspolitikker tillader.

Benyt følgende fremgangsmåde for at generere SAS-token.

1. På Azure-portalen skal du gå til den [lagerkonto](#storageAccount), du oprettede, da du konfigurerede Eksport til Data Lake.
2. I venstre rude under lagerkontoen skal du vælge **Delt adgangsunderskrift**.
3. På siden **SAS-indstillinger** skal du angive følgende felter.

    | Felt | Værdi |
    |---|---|
    | Tilladte tjenester | Vælg **Blob**. |
    | Tilladte ressourcetyper | Vælg **Service**, **Container** og **Objekt**. |
    | Tilladte tilladelser | Vælg **Læs**, **Skriv**, **Slet**, **Liste**, **Tilføj** og **Opret**. |
    | Tilladelser til Blob-version | Marker **Aktiverer sletning af versioner**. |
    | Start-og udløbsdato/-klokkeslæt | Angiv en start- og slutdato og et tidspunkt for SAS-token efter behov. |
    | Tilladte IP-adresser | Lad feltet være tomt. |
    | Tilladte protokoller | Vælg kun **HTTPS**. |
    | Foretrukket ruteniveau | Vælg **basis (standard)**. |
    | Signeringsnøgle | Vælg **nøgle 1** eller **nøgle 2** efter behov. |

4. Vælg **Generer SAS og forbindelsesstreng**.
5. Kopiér værdien i **SAS-token**-feltet, og indsæt den i en teksteditor, f.eks. Notesblok.

### <a name="download-the-deployment-scripts-for-azure-synapse-views"></a><a name="downloadSynapseDeploymentScripts"></a>Hent installationsscriptene til Azure Synapse-visninger

Hvis du vil oprette og udgive de påkrævede visninger i et Azure Synapse workspace, skal du køre et sæt scripts. Følg disse trin for at hente scripts.

1. På GitHub skal du gå til [microsoft/Dynamics365Commerce.Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions)-lageret.
2. Download scriptene til den lokale computer ved at klone repo'en eller hente den som en zip-fil.

### <a name="install-and-configure-an-azure-synapse-workspace"></a><a name="configureAzureSynapse"></a>Installer og konfigurer et Azure Synapse workspace

Hvis du vil installere og konfigurere et Azure Synapse workspace, skal du følge disse trin.

1. Installer et Azure Synapse workspace i dit Azure-abonnement. Du kan finde flere oplysninger under [Hurtig start: Opret et Synapse-arbejdsområde](/azure/synapse-analytics/quickstart-create-workspace).
2. I Notesblok eller en anden teksteditor skal du åbne Scriptfilen **SetupSynapse.sql** fra mappen på den lokale computer, som du klonede eller hentede Dynamics365Commerce.Solutions-repo til i forrige afsnit. Scriptfilen findes under mappen /Pipeline/CommerceAnalyticsSynapse/. I scriptet skal du erstatte pladsholdertekst med værdier, som vist i følgende tabel.

    | Pladsholdertekst | Erstatningsværdi |
    |---|---|
    | placeholder_storageaccount | Navnet på den [lagerkonto](#storageAccount), du oprettede, da du konfigurerede Eksport til Data Lake. |
    | <a name="phContainer"></a>placeholder_container | Navnet på den lagercontainer, der blev oprettet i din forekomst af Data Lake, efter at du installerede tilføjelsesprogrammet Export to Data Lake i LCS. Hvis du vil hente containernavnet, skal du bruge Storage Explorer i Azure-portalen til at gennemse din lagerkonto. |
    | placeholder_sastoken | Den [SAS-token](#getSASToken), som du genererede. Sørg for at fjerne spørgsmålstegnet (**?**) fra starten af SAS-token-værdien. |
    | <a name="phUserPwd"></a>placeholder_password | En stærk adgangskode efter eget valg. Noter adgangskoden. Den angives som adgangskoden til den nye **reportreadonlyuser**-konto, som scriptet opretter. Angiv **ikke** adgangskoden til **sqladminuser**-kontoen. |

3. Kopier det opdaterede indhold i scriptfilen.
4. Gå til det nye Azure Synapse workspace i Azure-portalen. Vælg **Åbn Synapse Studio** på siden **Oversigt**.
5. Vælg **Nyt \> SQL-script** i Synapse Studio, og indsæt indholdet af scriptfilen i SQL-scripteditoren.
6. Kontrollér, at feltet **Brug database** er angivet til **master**.
7. Vælg **Kør**, og vent på, at scriptet er færdig med at køre. Hvis scriptet udføres korrekt, oprettes databasen til handelsanalyser, legitimationsoplysningerne til adgang til datasøen og en skrivebeskyttet brugerkonto, som Power BI skal bruge til at oprette forbindelse til Azure Synapse-forekomsten.
8. Åbn Windows PowerShell i admin-tilstand på din lokale computer, og gå til mappen /Pipeline/CommerceAnalyticsSynapse/ under den mappe, du klonede eller som du hentede Dynamics365Commerce.Solutions-repo til.
9. Konfigurer udførelsespolitikken for Windows PowerShell ved at køre følgende kommando.

    ```powershell
    Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
    ```

10. Hvis SQL Server PowerShell-modulet ikke allerede er installeret, kan du installere det ved at køre følgende kommando.

    ```powershell
    Install-Module sqlserver
    ```

    > [!NOTE]
    > Under installationen af modulet bliver du måske bedt om at installere en NuGet-udbyder. I dette tilfælde skal du vælge **J** for at installere NuGet-udbyderen. Du kan også blive bedt om at bekræfte, at du er ved at geninstallere moduler fra et lager, der ikke er i brug. I dette tilfælde skal du vælge **J** for at fortsætte installationen. Du kan vælge at køre **Set-PSRepository** cmdlet for at have tillid til **PSGallery-lageret**.

11. Udgiv Azure Synapse-visningerne ved at køre følgende kommando.

    ```powershell
    .\PublishSynapseViews.ps1 -serverName SERVER_NAME -password PASSWORD -storageAccount STORAGE_ACCOUNT -containerName CONTAINER_NAME -datarootpath DATA_ROOT_PATH
    ```

    Når du kører denne kommando, erstattes pladsholderværdier, som vist i følgende tabel.

    | Pladsholderværdi | Erstatningsværdi |
    |---|---|
    | SERVER_NAME | Navnet på Azure Synapse Serverless SQL-slutpunkt. Du kan hente denne værdi fra **oversigtssiden** for Azure Synapse workspace i Azure-portalen. |
    | ADGANGSKODE | Adgangskoden til **sqladminuser-kontoen**. |
    | STORAGE_ACCOUNT | Navnet på lagerkontoen for forekomsten af Data Lake. |
    | CONTAINER_NAME | Navnet på den container, der blev oprettet af funktionen Eksporter til Data Lake. Denne container er den samme container, som du angav [placeholder_container](#phContainer) i trin 2. |
    | DATA_ROOT_PATH | Mappenavnet under den container, der indeholder alle dataene. |

    > [!NOTE]
    > Du kan finde navnet på lagringskontoen, containernavnet og datarodsstien ved hjælp af Azure-lagerbrowseren og din Data Lake-lagerkonto på Azure-portalen.

12. Vent på, at scriptet er færdig med at køre. Hvis scriptet udføres korrekt, oprettes SQL-visninger i Azure Synapse-serverløse SQL-forekomsten.

### <a name="install-the-power-bi-template-app"></a><a name="powerbi"></a>Installér Power BI-skabelonapp

Hvis du vil installere Power BI-skabelonapp til Commerce-analyser (forhåndsversion), skal du følge disse trin.

1. Log på portalen [Power BI](https://powerbi.microsoft.com/) ved hjælp af dit organisations-id.
2. Installer Commerce-analyser (Forhåndsversion) Power BI-skabelonappen ved at gå til [https://aka.ms/cdireport-installapp](https://aka.ms/cdireport-installapp). Du kan modtage en advarsel, der viser, at appen ikke er vist på AppSource. Vælg **Installer**.
3. Hvis du installerer appen første gang, skal du gå videre til trin 5. Hvis du har installeret denne app før, vises følgende indstillinger for opdatering af appen:

    - **Opdater arbejdsområdet og appen** – Opdater den eksisterende skabelonapp, og overskriv dine eksisterende appindstillinger, f.eks. konfigurationer af appforekomster og tilladelser.
    - **Opdater kun indholdet på arbejdsområdet uden at opdatere appen** – Opdater den eksisterende skabelonapp, men behold dine eksisterende appindstillinger. *Denne indstilling er den anbefalede indstilling for appopdateringer.*
    - **Installer en anden kopi af appen i et nyt arbejdsområde** – Opret et nyt arbejdsområde, og opret derefter en kopi af den eksisterende skabelonapp i det. Det eksisterende arbejdsområde bevares.

4. Vælg en af opdateringsindstillingerne, og vælg derefter **Installer**.
5. Åbn den installerede app ved at vælge **Apps** i venstre rude og derefter vælge appen.
6. Opret forbindelse mellem appen og datakilden ved at vælge **Tilslut**. Hvis du har installeret appen før, skal du vælge linket **Tilknyt dit datalink** på den gule meddelelseslinje.
7. Angiv følgende felter.

    | Felt | Værdi |
    |---|---|
    | Server | Angiv navnet på Azure Synapse Serverless SQL-slutpunkt, du oprettede i forrige afsnit. Du kan hente denne værdi fra **oversigtssiden** for Azure Synapse workspace i Azure-portalen. |
    | Database | Angiv **CommerceAnalytics**. |
    | Sprog | Vælg en værdi fra listen. Dette felt bruges til lokale produkt- og kategorinavne. Værdien er følsom over for store og små bogstaver. |
    | Datointerval | Vælg en værdi fra listen. Data for det valgte antal måneder importeres til Power BI-datasættet. Den værdi, du vælger, har indflydelse på størrelsen på datasættet og den tid, der kræves til synkroniseringen. |

8. Vælg **Næste**. Du bliver bedt om at angive legitimationsoplysningerne til oprettelse af forbindelse til Azure Synapse SQL-databasen. Indstil felterne som beskrevet i følgende tabel.

    | Felt | Værdi |
    |---|---|
    | Godkendelsesmetode | Vælg **Basis**. |
    | Brugernavn | Angiv **reportreadonlyuser**. |
    | Adgangskode | Angiv den værdi, du har erstattet med [placeholder_password](#phUserPwd)-pladsholderen i setupSynapse.sql-scriptet. Denne adgangskode er adgangskoden til **reportreadonlyuser-kontoen**. |

9. Vælg **log på, og opret forbindelse**.
10. Vent, indtil datasættet er opdateret. Vælg derefter knappen **Rediger app** for at åbne app-arbejdsområdet, hvor du kan få vist opdateringsstatus for datasættet. I apparbejdsområdet kan du også vælge at oprette automatiske opdateringsplaner for dit datasæt, administrere tilladelser og omdøbe app-forekomsten.

### <a name="privacy"></a><a name="privacy"></a>Beskyttelse

Det er vigtigt for os at beskytte dine personlige oplysninger. Du kan få mere at vide ved at læse vores [erklæring om beskyttelse af personlige oplysninger](https://go.microsoft.com/fwlink/?LinkId=521839).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
