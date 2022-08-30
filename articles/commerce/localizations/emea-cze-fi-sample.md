---
title: Eksempel på integration af regnskabsregistreringstjeneste i Den Tjekkiske Republik
description: Denne artikel indeholder en oversigt over eksemplet på regnskabsintegration for Den Tjekkiske Republik i Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 08/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-04-01
ms.openlocfilehash: 3838792c0a420fb88ea9daab0a67c2e644c80681
ms.sourcegitcommit: 0feb5d0b06e04f99903069ff2801577be86b8555
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/18/2022
ms.locfileid: "9313742"
---
# <a name="fiscal-registration-service-integration-sample-for-the-czech-republic"></a>Eksempel på integration af regnskabsregistreringstjeneste i Den Tjekkiske Republik

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Denne artikel indeholder en oversigt over eksemplet på regnskabsintegration for Den Tjekkiske Republik i Microsoft Dynamics 365 Commerce.

For at opfylde lokale regnskabsmæssige krav til kasseapparater i Den Tjekkiske Republik omfatter Dynamics 365 Commerce-funktionaliteten for Den Tjekkiske Republik en eksempelintegration af POS med en ekstern tjeneste til regnskabsregistrering. Eksemplet udvider [funktionen til regnskabsintegration](fiscal-integration-for-retail-channel.md). Den er baseret på [EFR-løsningen (Electronic Fiscal Register)](https://efsta.org/sicherheitsloesungen/) fra [EFSTA](https://efsta.org/) og giver mulighed for kommunikation med EFR-tjenesten via HTTPS-protokollen. EFR-tjenesten sikrer elektronisk registrering af salg (Elektronická evidence tržeb \[EET\]). Med andre ord sikrer den onlineoverførsel af salgsdataene til skattemyndighedens regnskabswebtjeneste. Tjenesten EFR skal være have enten Commerce Hardwarestation eller en separat maskine som vært, der kan oprettes forbindelse til fra hardwarestationen. Eksemplet findes i form af kildekode og er en del af Commerce SDK (Software Development Kit).

Microsoft frigiver ikke hardware, software eller dokumentation fra EFSTA. Du kan få oplysninger om, hvordan du henter EFR-løsningen og bruger den, ved at kontakte [EFSTA](https://efsta.org/kontakt/).

## <a name="scenarios"></a>Scenarier

Følgende scenarier dækkes af eksemplet på integration af tjenesten til regnskabsregistrering for Den Tjekkiske Republik:

- Registrering af kontanttransaktioner i regnskabsregistreringstjenesten.

    - Send detaljerede transaktionsdata til regnskabsregistreringstjenesten. Disse data omfatter oplysninger om salgslinjer og oplysninger om rabatter, betalinger og moms. Tjenesten til regnskabsregistrering sender dataene til skattemyndighederne på internettet og modtager en bekræftelse fra dem, der indeholder regnskabs-id'et for transaktionen.
    - Indlæs et svar fra regnskabsregistreringstjenesten. Dette svar omfatter regnskabsdata som f.eks. regnskabs-id-koden og sikkerhedskoden for transaktionen osv.
    - Udskriv regnskabsdata for en registreret transaktion på kvitteringen.

- Registrering af gavekorthandlinger og kundeindbetalinger i regnskabsregistreringstjenesten.

    - Udsted eller tilføj penge på et gavekort.
    - Registrer en indbetaling på kundekonto.
    - Opret en kundeordre, og registrer en indbetaling for ordren.
    - Rediger en kundeordre, og tilsidesæt indbetalingen for ordren.
    - Annuller en kundeordre, og refunder indbetalingen for ordren.

- Fejlhåndtering som f.eks. følgende muligheder.

    - Forsøg at registrere et regnskab igen, hvis et nyt forsøg er muligt, f.eks. hvis tjenesten til regnskabsregistrering ikke er tilgængelig, ikke er klar eller ikke svarer.
    - Udskyd regnskabsregistrering.
    - Undlad regnskabsregistrering, eller markér transaktionen som registreret, og inkluder infokoder for at registrere årsagen til fejlen og flere oplysninger.
    - Kontrollér, om tjenesten til regnskabsregistrering er tilgængelig, før en ny salgstransaktion åbnes, eller en salgstransaktion færdiggøres.

### <a name="gift-cards"></a>Gavekort

I eksemplet med integration af tjenester til regnskabsregistrering implementeres følgende regler, der er relateret til gavekort.

- Salgslinjer, der er relateret til handlingerne *Udsted gavekort* eller *Føj til gavekort* i en salgstransaktion, er markeret med en særlig attribut, når transaktionen registreres i tjenesten til regnskabsregistrering.
- En betaling med gavekort betragtes som en almindelig betaling og markeres med en særlig attribut, når transaktionen registreres i regnskabsregistreringstjenesten.

### <a name="customer-account-deposits-and-customer-order-deposits"></a>Indbetalinger på kundekonto og indbetalinger for kundeordre

I eksemplet med integration af tjenester til regnskabsregistrering implementeres følgende regler, der er relateret til kundekontoindbetalinger og indbetalinger for kundeordrer.

- En transaktion, der er relateret til en kundekontoindbetaling eller en indbetaling for en kundeordre, registreres i regnskabsregistreringstjenesten som en enkelt linjetransaktion og er markeret med en særlig attribut. Indbetalingsmomsgruppen er angivet på denne linje.
- Når der oprettes en hybridkundeordre, dvs. en kundeordre, der indeholder produkter, som kunden kan bære ud af butikken, samt produkter, der skal afhentes eller leveres senere, indeholder den transaktion, der er registreret i tjenesten til regnskabsregistrering, linjer for de produkter, der bæres ud, samt en linje for ordreindbetalingen.
- En betaling fra en kundekonto betragtes som en almindelig betaling og markeres med en særlig attribut, når transaktionen registreres i regnskabsregistreringstjenesten.
- Det indbetalingsbeløb på kundeordren, der anvendes på en kundeordres afhentningshandling, betragtes som en almindelig betaling og er markeret med en særlig attribut, når transaktionen registreres i tjenesten til regnskabsregistrering.

### <a name="offline-registration"></a>Offlineregistrering

Hvis regnskabsregistreringstjenesten ikke sender transaktionsdata til skattemyndighedernes webjeneste (f.eks. pga. timeout for svar) og ikke modtager en bekræftelse fra webtjenesten (dvs. regnskabs-id-koden for transaktionen), genererer den en lokal signatur for transaktionen og medtager den og en særlig fejlkode i svaret. Tjenesten til regnskabsregistrering sender transaktioner i oprindelig rækkefølge i baggrunden, så snart netværksforbindelsen gendannes.

### <a name="limitations-of-the-sample"></a>Begrænsninger for eksemplet

Tjenesten til regnskabsregistrering understøtter kun scenarier, hvor moms er inkluderet i prisen. Derfor skal indstillingen **Prisen inkluderer moms** angives til **Ja** for både butikker og kunder.

## <a name="set-up-commerce-for-the-czech-republic"></a>Konfigurere Commerce for Den Tjekkiske Republik

I dette afsnit beskrives de Commerce-indstillinger, der er specifikke for og anbefales for Den Tjekkiske Republik. Du kan finde flere oplysninger på [Startside for Commerce](../index.md).

Hvis du vil bruge den specifikke tjekkiske funktion, skal du angive følgende indstillinger.

- Angiv feltet **Land/område** til **CZE** (Den Tjekkiske Republik) i den juridiske enheds primære adresse.
- I POS-funktionalitetsprofilen for alle butikker i Den Tjekkiske Republik skal du angive feltet **ISO-kode** til **CZ** (Den Tjekkiske Republik).

Du skal også angive følgende indstillinger for Den Tjekkiske Republik. Bemærk, at du skal køre de relevante distributionsjob, når du har fuldført opsætningen.

### <a name="set-up-vat-per-czech-republic-requirements"></a>Konfigurere moms pr. krav fra Den Tjekkiske Republik


Du skal oprette momskoder, momsgrupper og varemomsgrupper. Du skal også angive momsoplysninger for produkter og tjenester. Du kan finde flere oplysninger om opsætning og brug af momsfunktioner under [Momsoversigt](../../finance/general-ledger/indirect-taxes-overview.md).

### <a name="set-up-stores"></a>Konfigurere butikker

Opdater butiksoplysningerne på siden **Alle butikker**. Du skal angive følgende parametre.

- Vælg den momsgruppe, der skal bruges for salg til standardkunden, i feltet **Momsgruppe**.
- Angiv indstillingen **Priserne inkluderer moms** til **Ja**.
- Angiv feltet **Navn** til firmanavnet. Denne ændring er med til at sikre, at firmanavnet vises på en salgskvittering. Du kan også føje firmanavnet til layoutet for salgskvitteringen som fritekst.
- Angiv feltet **Momsidentifikationsnummer (TIN)** til firmaets identifikationsnummer. Denne ændring er med til at sikre, at firmaets identifikationsnummer vises på en salgskvittering. Du kan også føje firmaets identifikationsnummer til layoutet for salgskvitteringen som fritekst.

### <a name="set-up-functionality-profiles"></a>Konfigurere funktionalitetsprofiler

Konfigurer POS-funktionalitetsprofiler.

- I oversigtspanelet **Kvitteringsnummerering** skal du oprette kvitteringsnummerering ved at oprette eller opdatere poster for kvitteringstransaktionstyperne **Salg**, **Salgsordre** og **Returnering**.

### <a name="set-up-registration-numbers"></a>Konfigurere registreringsnumre

1. Gå til **Virksomhedsadministration \> Globalt adressekartotek \> Registreringstyper \> Registreringstyper**. Opret en ny registreringstype. Angiv feltet **Land/område** til **CZE** (Den Tjekkiske Republik), og gør det begrænset til Organisation.
2. Gå til **Virksomhedsadministration \> Globalt adressekartotek \> Registreringstyper \> Registreringskategorier**. Opret en ny registreringskategori. Vælg registreringstypen fra det forrige trin, og angiv **Registreringskategori** til Id for **Virksomhedslokalitets-id**.
3. Gå til **Organisationsadministration \> Organisationer \> Driftsenheder**. For hver butik, der ligger i Den Tjekkiske Republik, skal du vælge den enhed, der er relateret til butikken. Udvid rullelisten **Flere indstillinger** i oversigtspanelet **Adresse**, og vælg derefter **Avanceret**. 
4. På siden **Håndter adresser**, der åbnes, skal du angive følgende indstillinger.

    - Angiv feltet **Land/område** til **CZE** i oversigtspanelet **Adresse**.
    - Opret en ny post i oversigtspanelet **Registrerings-id**. Vælg den registreringstype, du har oprettet tidligere, og angiv registreringsnummeret.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Konfigurere brugerdefinerede felter, så de kan bruges i kvitteringsformater for salgskvittering

Du kan konfigurere sprogteksten og brugerdefinerede felter, der bruges i POS-kvitteringsformaterne. Standardfirmaet for den bruger, der opretter kvitteringsopsætningen, skal være den samme juridiske enhed, hvor opsætningen af sprogtekster oprettes. Du kan også oprette de samme sprogtekster i både brugerens standardfirma og den juridiske enhed for den butik, som opsætningen oprettes for.

På siden **Sprogtekst** kan du tilføje følgende poster for etiketterne i de brugerdefinerede felter til kvitteringslayout. Bemærk, at værdierne for **Sprog-id**, **Tekst-id** og **Tekst**, der vises i tabellen, kun er eksempler. Du kan ændre dem, så de opfylder dine behov. Men de værdier for **Tekst-id**, du bruger, skal dog være entydige, og de skal være lig med eller større end 900001.

Føj følgende POS-etiketter til sektionen **POS** i **Sprogtekst** fra tabellen:

| Sprog-id | Tekst-id | Tekst                   |
|-------------|---------|------------------------|
| en-US       | 900001  | ID provozovny/pokladny |
| en-US       | 900002  | BKP                    |
| en-US       | 900003  | PKP                    |
| en-US       | 900004  | FIK                    |
| en-US       | 900005  | Info                   |
| en-US       | 900006  | Løbenummer        |

På siden **Brugerdefinerede felter** kan du tilføje følgende poster for de brugerdefinerede felter til kvitteringslayout. Bemærk, at værdier for **Tekst-id for billedtekst** skal svare til de værdier for **Tekst-id**, som du har angivet på siden **Sprogtekst**:

| Navn                 | Type    | Tekst-id for billedtekst |
|----------------------|---------|-----------------|
| TLT                  | Kvittering | 900001          |
| SEC                  | Kvittering | 900002          |
| SIGN                 | Kvittering | 900003          |
| FISCAL               | Kvittering | 900004          |
| INFO                 | Kvittering | 900005          |
| CONTINUOUSNUMBER     | Kvittering | 900006          |

> [!NOTE]
> Det er vigtigt, at du angiver korrekte brugerdefinerede feltnavne, som vist i den foregående tabel. Et forkert felt medfører, at der mangler data ved i kvitteringer.

### <a name="configure-receipt-formats"></a>Konfigurere kvitteringsformater

For hvert påkrævet kvitteringsformat skal du ændre værdien i feltet **Udskriftsfunktion** til **Udskriv altid**.

I designeren til kvitteringsformater skal du føje følgende brugerdefinerede felter til de relevante kvitteringssektioner. Bemærk, at feltnavnene svarer til de sprogtekster, du har defineret i forrige afsnit.

- **Overskrift:** Tilføj følgende felter.

    - **Butiksnavn** og **Momsidentifikationsnummer**: Disse felter bruges til at udskrive firmaets navn og id-nummer på kvitteringer. Du kan også føje firmanavnet og id-nummeret til layoutet som fritekst.
    - **Butiksadresse**, **Dato**, **24-timerstid**, **Kvitteringsnummer** og **Kassenummer**.
    - **Sekvensnummer**: Dette felt identificerer nummeret på kontanttransaktionen i tjenesten til regnskabsregistrering.

- **Linjer:** Tilføj følgende felter.

    - **Varenavn**
    - **Antal**
    - **Pris i alt med moms**

- **Sidefod:** Tilføj følgende felter.

    - Betalingsfelter, så betalingsbeløbene for de enkelte betalingsmåder udskrives. Føj f.eks. felterne **Navn på betalingsmiddel** og **Beløb for betalingsmiddel** til én linje i layoutet.
    - **ID provozovny/pokladny**: I dette felt udskrives id'erne for virksomhedens lokaler og kasseapparat.
    - **BKP**: Dette felt udskriver skatteyderens sikkerhedskode, der er tildelt af regnskabsregistreringstjenesten.
    - **FIK**: Dette felt udskriver regnskabs-id'et for den transaktion, der er tildelt af skattemyndighedernes webtjeneste, hvis der er gennemført onlineregistrering.
    - **PKP**: Dette felt udskriver skatteyderens underskriftskode, som genereres af regnskabsregistreringstjenesten i tilfælde af offlineregistrering.
    - **Info**: I dette felt udskrives yderligere oplysninger fra regnskabsregistreringstjenesten.

Du kan finde flere oplysninger om, hvordan du arbejder med kvitteringsformater, i [Konfigurere og designe kvitteringsformater](../receipt-templates-printing.md).

## <a name="set-up-fiscal-integration-for-the-czech-republic"></a>Konfigurere regnskabsintegration for Den Tjekkiske Republik

Regnskabsintegrationstjenestens eksempel til Den Tjekkiske Republik er baseret på [funktionaliteten af regnskabsintegration](fiscal-integration-for-retail-channel.md) og er en del af Commerce SDK. Eksemplet på POS-udvidelse findes i mappen **src\\FiscalIntegration\\Efr** i lageret til [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions/). [Eksemplet](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) består af en regnskabsdokumentudbyder, som er en udvidelse af Commerce Runtime (CRT), og en regnskabsconnector, som er en udvidelse af Commerce Hardware Station. Yderligere oplysninger om, hvordan du bruger Commerce SDK, finder du i [Download Commerce SDK-prøver og -referencepakker fra GitHub og NuGet](../dev-itpro/retail-sdk/sdk-github.md) og [oprette en build-pipeline til den uafhængige emballage SDK](../dev-itpro/build-pipeline.md).

> [!NOTE]
> Eksempel på integration af regnskabsregistreringstjeneste for Tjekkiet tilgængelig i Commerce Software Development Kit (SDK) pr. Commerce-version 10.0.29. I Commerce-version 10.0.28 eller tidligere skal du bruge den tidligere version af Retail SDK på en virtuel maskine til udviklere (VM) i Microsoft Dynamics Lifecycle Services (LCS). Du kan få flere oplysninger i [Retningslinjer for installation af eksempel på integration af regnskabsregistreringsservice i Den Tjekkiske Republik (ældre)](emea-cze-fi-sample-sdk.md).

Fuldfør trinnene til opsætning af regnskabsintegration som beskrevet i [Konfigurere regnskabsintegration for Commerce-kanaler](setting-up-fiscal-integration-for-retail-channel.md):

1. [Konfigurer en regnskabsregistreringsproces](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Du skal også notere dig indstillingerne for den regnskabsregistreringsproces, der er [specifik for dette eksempel til integration af regnskabsregistreringstjenesten](#set-up-the-registration-process).
1. [Angive indstillinger for fejlhåndtering](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Aktiver manuel udførelse af udsatte regnskabsregistreringer](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Konfigurere kanalkomponenter](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Konfigurere registreringsprocessen

Hvis du vil aktivere registreringsprocessen, skal du følge disse trin for at konfigurere Commerce Headquarters. Du kan finde flere oplysninger i [Konfigurere regnskabsintegration for Commerce-kanaler](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Download konfigurationsfiler for regnskabsconnectoren og regnskabsdokumentudbyderen:

    1. Åbn lageret il [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions/).
    1. Vælg en korrekt version af frigivelsesafdelingen i overensstemmelse med din SDK/programversion.
    1. Åbn **src \> FiscalIntegration \> Efr**.
    1. Hent konfigurationsfilen til regnskabsdokumentudbyderen på **Konfigurationer \> DocumentProviders \> DocumentProviderFiscalEFRSampleCzech.xml**.
    1. Hent konfigurationsfilen til regnskabsconnectoren på **Konfigurationer \> Connectors \> ConnectorEFRSample.xml**.

    > [!NOTE]
    > I Commerce-version 10.0.28 eller tidligere skal du bruge den tidligere version af Retail SDK på en virtuel maskine til udviklere i LCS. Konfigurationsfilerne til dette eksempel på regnskabsintegration findes i følgende mapper i Retail SDK på en udvikler VM i LCS:
    >
    > - **Konfigurationsfilen til regnskabsdokumentudbyder:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.EFRSample\\Configuration\\DocumentProviderFiscalEFRSampleCzech.xml
    > - **Konfigurationsfil til regnskabsconnector:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.EFRSample\\Configuration\\ConnectorEFRSample.xml

1. Gå til **Retail og Commerce \> Konfiguration af Headquarters \> Parametre \> Delte Commerce-parametre**. Under fanen **Generelt** skal du angive indstillingen **Aktivér regnskabsintegration** til **Ja**.
1. Gå til **Retail og Commerce \> Konfiguration af kanal \> Regnskabsintegration \> Udbydere af regnskabsdokumenter**, og indlæs den konfigurationsfil til regnskabsdokumentudbyderen, du hentede tidligere.
1. Gå til **Retail og Commerce \> Konfiguration af kanal \> Regnskabsintegration \> Regnskabsconnectorer**, og indlæs den konfigurationsfil til regnskabsconnectoren, du hentede tidligere.
1. Gå til **Retail og Commerce \> Konfiguration af kanal \> Regnskabsintegration \> Funktionelle profiler for connector**. Opret en ny funktionel profil for connector. Vælg dokumentprovideren og den connector, du har indlæst tidligere. Opdater [indstillingerne for datatilknytning](#default-data-mapping) efter behov.
1. Gå til **Retail og Commerce \> Konfiguration af kanal \> Regnskabsintegration \> Tekniske profiler for connector**. Opret en ny teknisk profil for connector, og vælg den regnskabsconnector, du indlæste tidligere. Opdater [indstillingerne for connector](#fiscal-connector-settings) efter behov.
1. Gå til **Retail og Commerce \> Konfiguration af kanal \> Regnskabsintegration \> Regnskabsconnectorgrupper**. Opret en ny regnskabsconnector-gruppe for den funktionsprofil for connector, som du oprettede tidligere.
1. Gå til **Retail og Commerce \> Konfiguration af kanal \> Regnskabsintegration \> Processer for regnskabsregistrering**. Opret en ny regnskabsregistreringsproces og et trin i processen til regnskabsregistrering, og vælg den regnskabsconnector-gruppe, du oprettede tidligere.
1. Gå til **Retail og Commerce \> Konfiguration af kanal \> POS-opsætning \> POS-profiler \> Funktionalitetsprofiler**. Vælg en funktionalitetsprofil, der er knyttet til den butik, hvor registreringsprocessen skal aktiveres. Vælg den regnskabsregistreringsproces, du oprettede tidligere, i oversigtspanelet **Regnskabsregistreringsproces**.
1. Gå til **Retail og Commerce \> Konfiguration af kanal \> POS-opsætning \> POS-profiler \> Hardwareprofiler**. Vælg en hardwareprofil, der er tilknyttet den hardwarestation, som regnskabsregistreringstjenesten skal være tilknyttet. Vælg den tekniske profil for connectoren, du oprettede tidligere, i oversigtspanelet **Eksterne regnskabsenheder**.
1. Åbn distributionsplanen (**Retail og Commerce \> Retail og Commerce IT \> Distributionsplan**), og vælg job **1070** og **1090** for at overføre data til kanaldatabasen.

#### <a name="default-data-mapping"></a>Tilknytning af standarddata

Følgende standarddatatilknytning er inkluderet i konfigurationen af regnskabsdokumentudbyderen som en del af eksemplet på regnskabsintegration:

- **Tilknytning af momssatser** – Tilknytning af momsprocentværdier, der er konfigureret for momskoderne til værdier af attributten **TaxG** (momsgruppe) i anmodninger, der sendes til regnskabstjenesten. Her er standardtilknytningen:

    ```
    A: 21.00; B: 15.00; C: 10.00; Z: 0.00
    ```

    Den første komponent i hvert par repræsenterer en momsgruppe, der understøttes af EFR-regnskabsregistreringsservice. Den anden komponent repræsenterer den tilsvarende momssats. Yderligere oplysninger om momsgrupper, som EFR understøtter i Den Tjekkiske Republik, finder du i [EFR-referencen](https://public.efsta.net/efr/).

- **Tilknytning af standardmomsgrupper** – Alle momsbeløb, der ikke kan knyttes til en af de foruddefinerede momsgrupper, knyttes til standardmomsgruppen (grundlæggende). Her er standardtilknytningen:

    ```
    A
    ```

- **Tilknytning af indbetalingsmomsgruppe** – Kundeindbetalingsbeløb og kundeordreindbetalingsbeløb knyttes til indbetalingsmomsgruppen. Her er standardtilknytningen:

    ```
    Z
    ```

#### <a name="fiscal-connector-settings"></a>Indstillinger af regnskabsconnector

Følgende indstillinger er inkluderet i konfigurationen af regnskabsconnectoren som en del af eksemplet på regnskabsintegration:

- **Slutpunktadresse** – URL-adressen for tjenesten til regnskabsregistrering.
- **Timeout** – Den tid i millisekunder, som regnskabsconnectoren vil vente på et svar fra tjenesten til regnskabsregistrering.

### <a name="configure-channel-components"></a>Konfigurere kanalkomponenter

> [!NOTE]
> - Eksempel på integration af regnskabsregistreringstjeneste for Tjekkiet tilgængelig i Commerce Software Development Kit (SDK) pr. Commerce-version 10.0.29. I Commerce-version 10.0.28 eller tidligere skal du bruge den tidligere version af Retail SDK på en virtuel maskine til udviklere i LCS. Du kan få flere oplysninger i [Retningslinjer for installation af eksempel på integration af regnskabsregistreringsservice i Den Tjekkiske Republik (ældre)](emea-cze-fi-sample-sdk.md).
> - Handelsprøver, der implementeres i dit miljø, opdateres ikke automatisk, når du anvender tjeneste- eller kvalitetsopdateringer på Commerce-komponenter. Du skal opdatere de påkrævede prøver manuelt.

#### <a name="set-up-the-development-environment"></a>Konfigurere udviklingsmiljøet

Følg disse trin for at konfigurere et udviklingsmiljø, så du kan teste og udvide eksemplet.

1. Klon eller download lageret til [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions). Vælg en korrekt version af frigivelsesafdelingen i overensstemmelse med din SDK/programversion. Yderligere oplysninger finder du i [Hente Commerce SDK-eksempler og -referencepakker fra GitHub og NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Åbn EFR-løsningen på **Dynamics365Commerce.Solutions\\FiscalIntegration\\Efr\\EFR.sln**, og opbyg den.
1. Installer CRT-udvidelser:

    1. Find installationsprogrammet til CRT-udvidelsen:

        - **Commerce Scale Unit:** I mappen **Efr\\ScaleUnit\\ScaleUnit.EFR.Installer\\bin\\Debug\\net461** skal du finde installationsprogrammet **ScaleUnit.EFR.Installer**.
        - **Lokal CRT på Modern POS:** I mappen **Efr\\ModernPOS\\ModernPOS.EFR.Installer\\bin\\Debug\\net461** skal du finde installationsprogrammet **ModernPOS.EFR.Installer**.

    1. Start installationsprogrammet til CRT-udvidelsen fra kommandolinjen:

        - **Commerce Scale Unit:**

            ```Console
            ScaleUnit.EFR.Installer.exe install --verbosity 0
            ```

        - **Lokal CRT på Modern POS:**

            ```Console
            ModernPOS.EFR.Installer.exe install --verbosity 0
            ```

1. Installere regnskabsconnectorudvidelser:

    Du kan installere regnskabsconnectorudvidelser på [hardwarestationen](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station) eller [POS-kasseapparatet](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-or-service-in-the-local-network).

    1. Installer udvidelser til Hardwarestation:

        1. I mappen **Efr\\HardwareStation\\HardwareStation.EFR.Installer\\bin\\Debug\\net461** skal du finde installationsprogrammet **HardwareStation.EFR.Installer**.
        1. Start installationsprogrammet for udvidelsen fra kommandolinjen ved at køre følgende kommando.

            ```Console
            HardwareStation.EFR.Installer.exe install --verbosity 0
            ```

    1. Installer POS-udvidelser:

        1. Åbn POS-regnskabsconnectorens eksempelløsning på **Dynamics365Commerce.Solutions\\FiscalIntegration\\PosFiscalConnectorSample\\Contoso.PosFiscalConnectorSample.sln**, og opbyg den.
        1. I meppen **PosFiscalConnectorSample\\StoreCommerce.Installer\\bin\\Debug\\net461** skal du finde installationsprogrammet **Contoso.PosFiscalConnectorSample.StoreCommerce.Installer**.
        1. Start installationsprogrammet for udvidelsen fra kommandolinjen ved at køre følgende kommando.

            ```Console
            Contoso.PosFiscalConnectorSample.StoreCommerce.Installer.exe install --verbosity 0
            ```

#### <a name="production-environment"></a>Produktionsmiljø

Følg trinnene i [Konfigurere en build-pipeline til et eksempel på regnskabsintegration](fiscal-integration-sample-build-pipeline.md) for at generere og frigive Cloud Scale Unit og pakker, der kan implementeres med selvbetjening, til eksemplet på regnskabsintegration. **EFR build-pipeline.yml**-skabelonens YAML-fil findes i mappen **Pipeline\\YAML_Files** i lageret til [Dynamics 365 Commerce-løsning](https://github.com/microsoft/Dynamics365Commerce.Solutions).

## <a name="design-of-extensions"></a>Design af udvidelser

Regnskabsintegrationstjenestens eksempel til Den Tjekkiske Republik er baseret på [funktionaliteten af regnskabsintegration](fiscal-integration-for-retail-channel.md) og er en del af Commerce SDK. Eksemplet på POS-udvidelse findes i mappen **src\\FiscalIntegration\\Efr** i lageret til [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions/). [Eksemplet](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) består af en regnskabsdokumentudbyder, som er en udvidelse af CRT, og en regnskabsconnector, som er en udvidelse af Commerce Hardware Station. Yderligere oplysninger om, hvordan du bruger Commerce SDK, finder du i [Download Commerce SDK-prøver og -referencepakker fra GitHub og NuGet](../dev-itpro/retail-sdk/retail-sdk-overview.md) og [oprette en build-pipeline til den uafhængige emballage SDK](../dev-itpro/build-pipeline.md).

> [!NOTE]
> Eksempel på integration af regnskabsregistreringstjeneste for Tjekkiet tilgængelig i Commerce Software Development Kit (SDK) pr. Commerce-version 10.0.29. I Commerce-version 10.0.28 eller tidligere skal du bruge den tidligere version af Retail SDK på en virtuel maskine til udviklere i LCS. Du kan få flere oplysninger i [Retningslinjer for installation af eksempel på integration af regnskabsregistreringsservice i Den Tjekkiske Republik (ældre)](emea-cze-fi-sample-sdk.md).

### <a name="commerce-runtime-extension-design"></a>Design af Commerce Runtime-udvidelse

Formålet med udvidelsen, som er en udbyder af regnskabsdokumenter, er at generere servicespecifikke dokumenter og håndtere svar fra tjenesten til regnskabsregistrering.

#### <a name="request-handler"></a>Anmodningshandler

Der findes en enkelt **DocumentProviderEFRFiscalCZE**-anmodningshandler til dokumentudbyder, som bruges til at generere regnskabsdokumenter til tjenesten for regnskabsregistrering.

Denne handler er nedarvet fra brugergrænsefladen i **INamedRequestHandler**. Metoden **HandlerName** er ansvarlig for at returnere navnet på handleren. Navnet på handleren skal svare til navnet på connector-dokumentudbyderen, der er angivet i Commerce Headquarters.

Connectoren understøtter følgende anmodninger.

- **GetFiscalDocumentDocumentProviderRequest** – Denne anmodning indeholder oplysninger om, hvilket dokument der skal genereres. Den returnerer et servicespecifikt dokument, der skal registreres i tjenesten til regnskabsregistrering.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Denne anmodning returnerer listen over hændelser, der skal abonneres på. I øjeblikket understøttes følgende hændelser: salg, indbetalinger til kundekonti og indbetalinger for kundeordrer.
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** – Denne anmodning returnerer svaret fra tjenesten til regnskabsregistrering. Dette svar er serialiseret, så det danner en streng og er klar til at blive gemt.

#### <a name="configuration"></a>Konfiguration

Konfigurationsfilen til regnskabsdokumentudbyderen er placeret i **src\\FiscalIntegration\\Efr\\Configurations\\DocumentProviders\\DocumentProviderFiscalEFRSampleCzech.xml** i lageret for [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Formålet med filen er at aktivere indstillinger for regnskabsdokumentudbyderen, der skal konfigureres fra Commerce Headquarters. Filformatet er tilpasset kravene til konfiguration af regnskabsintegration.

### <a name="hardware-station-extension-design"></a>Design af hardwarestationsudvidelse

Formålet med den forlængelse, der er en regnskabsmæssig connector, er at kommunikere med tjenesten til regnskabsregistrering. Udvidelsen til Hardwarestation bruger HTTP-protokollen til at sende dokumenter, som CRT-udvidelsen genererer til regnskabsregistreringstjenesten. Den håndterer også de svar, der er modtaget fra tjenesten til regnskabsregistrering.

#### <a name="request-handler"></a>Anmodningshandler

Anmodningshandleren **EFRHandler** er indgangspunktet for håndtering af anmodninger til tjenesten til regnskabsregistrering.

Denne handler er nedarvet fra brugergrænsefladen i **INamedRequestHandler**. Metoden **HandlerName** er ansvarlig for at returnere navnet på handleren. Navnet på handleren skal svare til navnet på den regnskabsconnector, der er angivet i Commerce Headquarters.

Connectoren understøtter følgende anmodninger.

- **SubmitDocumentFiscalDeviceRequest** – Denne anmodning sender dokumenter til tjenesten til regnskabsregistrering og returnerer et svar fra den.
- **IsReadyFiscalDeviceRequest** – Denne anmodning bruges til tilstandskontrol af tjenesten til regnskabsregistrering.
- **InitializeFiscalDeviceRequest** – Denne anmodning bruges til at initialisere tjenesten til regnskabsregistrering.

#### <a name="configuration"></a>Konfiguration

Konfigurationsfilen til regnskabsconnectoren er placeret i **src\\FiscalIntegration\\Efr\\Configurations\\Connectors\\ConnectorEFRSample.xml** i lageret for [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Formålet med filen er at aktivere indstillinger for regnskabsconnectoren, der skal konfigureres fra Commerce Headquarters. Filformatet er tilpasset kravene til konfiguration af regnskabsintegration.

### <a name="pos-fiscal-connector-extension-design"></a>Design af udvidelsen POS-regnskabsconnector

Formålet med POS-regnskabsconnector-udvidelsen er at kommunikere med tjenesten til regnskabsregistrering fra POS. Den bruger HTTPS-protokollen til kommunikation.

#### <a name="fiscal-connector-factory"></a>Fabrik for regnskabsconnector

Fabrikken for regnskabsconnector knytter connectornavnet til implementeringen af regnskabsconnector og er placeret i filen **Pos.Extension\\Connectors\\FiscalConnectorFactory.ts**. Navnet på connectoren skal svare til navnet på den regnskabsconnector, der er angivet i Commerce Headquarters.

#### <a name="efr-fiscal-connector"></a>EFR-regnskabsconnector

EFR-regnskabsconnectoren er placeret i filen **Pos.Extension\\Connectors\\Efr\\EfrFiscalConnector.ts**. Den implementerer brugergrænsefladen **IFiscalConnector**, der understøtter følgende anmodninger:

- **FiscalRegisterSubmitDocumentClientRequest** – Denne anmodning sender dokumenter til tjenesten for regnskabsregistrering og returnerer et svar fra den.
- **FiscalRegisterIsReadyClientRequest** – Denne anmodning bruges til tilstandskontrol af tjenesten til regnskabsregistrering.
- **FiscalRegisterInitializeClientRequest** – Denne anmodning bruges til at initialisere tjenesten til regnskabsregistrering.

#### <a name="configuration"></a>Konfiguration

Konfigurationsfilen findes i mappen **src\\FiscalIntegration\\Efr\\Configurations\\Connectors** i lageret [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Formålet med filen er at aktivere indstillinger for regnskabsconnectoren, der skal konfigureres fra Commerce Headquarters. Filformatet er tilpasset kravene til konfiguration af regnskabsintegration. Følgende indstillinger tilføjes:

- **Slutpunktadresse** – URL-adressen for tjenesten til regnskabsregistrering.
- **Timeout** – Den tid i millisekunder, som connectoren vil vente på et svar fra tjenesten til regnskabsregistrering.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
