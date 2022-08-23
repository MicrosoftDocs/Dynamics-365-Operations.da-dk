---
title: Eksempel på integration med kontrolenhed for Sverige
description: Denne artikel indeholder en oversigt over eksemplet på regnskabsintegration for Sverige i Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-08
ms.openlocfilehash: 3376e6a901b692371a44b5c74c1e6b4afd0cd573
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275060"
---
# <a name="control-unit-integration-sample-for-sweden"></a>Eksempel på integration med kontrolenhed for Sverige

[!include [banner](../includes/banner.md)]

Denne artikel indeholder en oversigt over eksemplet på regnskabsintegration for Sverige i Microsoft Dynamics 365 Commerce.

> [!NOTE]
> Denne eksempelfunktionalitet til regnskabsintegration erstatter det tidligere [eksempel på POS-integration med kontrolenheder for Sverige](retail-sdk-control-unit-sample.md). Det tidligere eksempel kan ikke bruge [struktur til regnskabsintegration](./fiscal-integration-for-retail-channel.md) og bliver forældet i senere opdateringer. Du kan finde oplysninger om, hvordan du overgår fra det tidligere eksempel til det eksempel, der svarer til Dynamics 365 Commerce version **10.0.22 og tidligere**, i [Overføre fra det tidligere eksempel på integration](emea-swe-fi-sample-sdk.md#migrating-from-the-earlier-integration-sample).

Commerce-funktionaliteten for Sverige omfatter en eksempelintegration af POS med regnskabsenheder, der er specifikke for Sverige, og som kaldes *kontrolenheder*. Dette eksempel udvider [funktionen til regnskabsintegration](fiscal-integration-for-retail-channel.md). Det antages, at en kontrolenhed er fysisk forbundet med en hardwarestation, som POS er parret med. I eksemplet bruges API (Application Programming Interface) til [CleanCash Type A](https://www.retailinnovation.se/produkter)-kontrolenheden af Retail Innovation HTT AB. Version 1.1.4 af CleanCash API anvendes.

Eksemplet findes i form af kildekode og er en del af Retail SDK (Software Development Kit).

Microsoft frigiver ikke hardware, software eller dokumentation fra Retail Innovation HTT AB. Du kan få oplysninger om, hvordan du henter kontrolenheden og bruger den, ved at kontakte [Retail Innovation HTT AB](https://www.retailinnovation.se/).

## <a name="scenarios"></a>Scenarier

Eksemplet på integration af kontrolenhed for Sverige omfatter følgende funktioner:

- Salg, returneringer og kvitteringskopier registreres automatisk i en kontrolenhed, der er tilknyttet hardwarestationen, som er parret med POS.
- Kontrolkoden og produktionsnummeret for kontrolenheden for en registreret transaktion registreres fra kontrolenheden og gemmes i transaktionen. Disse data kaldes også et *regnskabssvar*. Regnskabssvaret kan ses på siden **Butikstransaktioner**.
- Brugerdefinerede felter til kontrolkoden og produktionsnummeret for kontrolenheden kan føjes til et kvitteringslayout. På den måde kan du udskrive regnskabssvaret for en transaktion på en kvittering.
- Regnskabssvaret for en transaktion vises i kanalrapporten **Elektronisk kladde (Sverige)**.
- Der findes flere muligheder for håndtering af fejl. Her er nogle eksempler:

    - Forsøg at registrere et regnskab igen, hvis et nyt forsøg er muligt. Du kan gentage regnskabsregistrering, hvis kontrolenheden f.eks. ikke er tilknyttet, ikke er klar eller ikke svarer.
    - Udskyd regnskabsregistrering.
    - Undlad regnskabsregistrering, eller markér transaktionen som registreret, og inkluder infokoder for at registrere årsagen til fejlen og flere oplysninger.
    - Kontrollér, om kontrolenheden er tilgængelig, før en ny salgstransaktion åbnes, eller en salgstransaktion færdiggøres.

### <a name="limitations-of-the-sample"></a>Begrænsninger for eksemplet

Eksemplet med integration af kontrolenheden for Sverige understøtter i øjeblikket ikke kundeordrescenarier.

## <a name="setting-up-the-integration-with-control-units"></a>Konfiguration af integrationen med kontrolenheder

Yderligere oplysninger om den konfiguration, der kræves for Sverige, finder du under [Konfigurere Commerce for Sverige](./emea-swe-cash-registers.md#setting-up-commerce-for-sweden).

### <a name="configuring-swedenspecific-receipts"></a>Konfigurere kvitteringer, der er specifikke for Sverige

#### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Konfigurere brugerdefinerede felter, så de kan bruges i kvitteringsformater for salgskvittering

Du kan konfigurere sprogteksten og brugerdefinerede felter, der bruges i POS-kvitteringsformaterne. Standardfirmaet for den bruger, der opretter kvitteringsopsætningen, skal være den samme juridiske enhed, hvor opsætningen af sprogtekster oprettes. Du kan også oprette de samme sprogtekster i både brugerens standardfirma og den juridiske enhed for den butik, som opsætningen oprettes for.

På siden **Sprogtekst** kan du tilføje følgende poster for etiketterne i de brugerdefinerede felter til kvitteringslayout. Bemærk, at værdierne for **Sprog-id**, **Tekst-id** og **Tekst**, der vises i tabellen, kun er eksempler. Du kan ændre dem, så de opfylder dine behov. Men de værdier for **Tekst-id**, du bruger, skal dog være entydige, og de skal være lig med eller større end 900001.

Føj følgende POS-etiketter til sektionen **POS** på siden **Sprogtekst**.

| Sprog-id | Tekst-id | Tekst                  |
|-------------|---------|-----------------------|
| en-US       | 900001  | Registrer kontrolkode |
| en-US       | 900002  | Registrer enhed       |

På siden **Brugerdefinerede felter** kan du tilføje følgende poster for de brugerdefinerede felter til kvitteringslayout. Bemærk, at værdier for **Tekst-id for billedtekst** skal svare til de værdier for **Tekst-id**, som du har angivet på siden **Sprogtekst**.

| Navn                         | Type    | Tekst-id for billedtekst |
|------------------------------|---------|-----------------|
| SE_FISCALREGISTERCONTROLCODE | Kvittering | 900001          |
| SE_FISCALREGISTERID          | Kvittering | 900002          |

> [!NOTE]
> Det er vigtigt, at du angiver korrekte brugerdefinerede feltnavne, som vist i ovenstående tabel. Et forkert felt medfører, at der mangler data ved i kvitteringer.

#### <a name="configure-receipt-formats"></a>Konfigurere kvitteringsformater

For hvert påkrævet kvitteringsformat skal du ændre værdien i feltet **Udskriftsfunktion** til **Udskriv altid**.

I designeren til kvitteringsformater skal du føje følgende brugerdefinerede felter til sektionen **Sidefod**. Bemærk, at feltnavnene svarer til de sprogtekster, du har defineret i forrige afsnit af denne artikel.

- **Registrer kontrolkode** – Dette felt udskriver kontrolkoden.
- **Registrer enhed** – Dette felt udskriver kontrolenhedens produktionsnummer.

Du kan finde flere oplysninger om, hvordan du arbejder med kvitteringsformater, i [Kvitteringsskabeloner og udskrivning](../receipt-templates-printing.md).

### <a name="set-up-fiscal-integration-for-sweden"></a>Konfigurere regnskabsintegration for Sverige

Integrationseksemplet for kontrolenheden til Sverige er baseret på [funktionaliteten af regnskabsintegration](fiscal-integration-for-retail-channel.md) og er en del af Retail SDK. Eksemplet findes i mappen **src\\FiscalIntegration\\CleanCash** i lageret til [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (f.eks. [eksemplet i frigivelse/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/CleanCash)). Eksemplet [består](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) af en regnskabsdokumentudbyder, som er en udvidelse af Commerce Runtime (CRT), og en regnskabsconnector, som er en udvidelse af Commerce Hardware Station. Yderligere oplysninger om, hvordan du bruger Retail SDK, finder du i [Retail SDK-arkitekturen](../dev-itpro/retail-sdk/retail-sdk-overview.md) og [Konfigurere en build-pipeline til uafhængige SDK-pakker](../dev-itpro/build-pipeline.md).

> [!WARNING]
> På grund af begrænsningerne ved den [nye uafhængige pakke- og udvidelsesmodel](../dev-itpro/build-pipeline.md) kan den ikke aktuelt bruges til dette eksempel på regnskabsintegration. Du skal bruge den tidligere version af Retail SDK på en virtuel maskine til udviklere (VM) i Microsoft Dynamics Lifecycle Services (LCS). Du kan få flere oplysninger i [Retningslinjer for eksempel på integration af kontrolenhed for Sverige (ældre)](emea-swe-fi-sample-sdk.md).
>
> Understøttelse af den nye uafhængige pakke- og udvidelsesmodel til eksempler på regnskabsintegration er planlagt til senere versioner.

Fuldfør trinnene til opsætning af regnskabsintegration som beskrevet i [Konfigurere regnskabsintegration for Commerce-kanaler](setting-up-fiscal-integration-for-retail-channel.md).

1. [Konfigurer en regnskabsregistreringsproces](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Du skal også notere dig indstillingerne for den regnskabsregistreringsproces, der er [specifik for dette eksempel på integration af kontrolenhed](#set-up-the-registration-process).
1. [Angive indstillinger for fejlhåndtering](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Aktiver manuel udførelse af udsatte regnskabsregistreringer](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Konfigurere kanalkomponenter](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Konfigurere registreringsprocessen

Hvis du vil aktivere registreringsprocessen, skal du følge disse trin for at konfigurere Commerce Headquarters. Du kan finde flere oplysninger i [Konfigurere regnskabsintegration for Commerce-kanaler](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Download konfigurationsfiler for regnskabsconnectoren og regnskabsdokumentudbyderen:

    1. Åbn lageret il [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions/).
    1. Vælg en korrekt version af frigivelsesafdelingen i overensstemmelse med din SDK/programversion (f.eks. **[release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Åbn **src \> FiscalIntegration \> CleanCash**.
    1. Hent konfigurationsfilen til regnskabsdokumentudbyderen på **CommerceRuntime \> DocumentProvider.CleanCashSample \> Configuration \> DocumentProviderFiscalCleanCashSample.xml** (for eksempel [filen til frigivelse/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/CleanCash/CommerceRuntime/DocumentProvider.CleanCashSample/Configuration/DocumentProviderFiscalCleanCashSample.xml)).
    1. Hent konfigurationsfilen til regnskabsconnectoren på **HardwareStation \> Connector.CleanCashSample \> Configuration \> ConnectorCleanCashSample.xml** (for eksempel [filen til frigivelse/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/CleanCash/HardwareStation/Connector.CleanCashSample/Configuration/ConnectorCleanCashSample.xml)).

    > [!WARNING]
    > På grund af begrænsningerne ved den [nye uafhængige pakke- og udvidelsesmodel](../dev-itpro/build-pipeline.md) kan den ikke aktuelt bruges til dette eksempel på regnskabsintegration. Du skal bruge den tidligere version af Retail SDK på en virtuel maskine til udviklere i LCS. Konfigurationsfilerne til dette eksempel på regnskabsintegration findes i følgende mapper i Retail SDK på en udvikler VM i LCS:
    >
    > - **Konfigurationsfilen til regnskabsdokumentudbyder:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.CleanCashSample\\Configuration\\DocumentProviderFiscalCleanCashSample.xml
    > - **Konfigurationsfil til regnskabsconnector:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.CleanCashSample\\Configuration\\ConnectorCleanCashSample.xml
    > 
    > Understøttelse af den nye uafhængige pakke- og udvidelsesmodel til eksempler på regnskabsintegration er planlagt til senere versioner.

1. Gå til **Retail og Commerce \> Konfiguration af Headquarters \> Parametre \> Delte Commerce-parametre**. Under fanen **Generelt** skal du angive indstillingen **Aktivér regnskabsintegration** til **Ja**.
1. Gå til **Retail og Commerce \> Konfiguration af kanal \> Regnskabsintegration \> Udbydere af regnskabsdokumenter**, og indlæs den konfigurationsfil til regnskabsdokumentudbyderen, du hentede tidligere.
1. Gå til **Retail og Commerce \> Konfiguration af kanal \> Regnskabsintegration \> Regnskabsconnectorer**, og indlæs den konfigurationsfil til regnskabsconnectoren, du hentede tidligere.
1. Gå til **Retail og Commerce \> Konfiguration af kanal \> Regnskabsintegration \> Funktionelle profiler for connector**. Opret en ny funktionel profil for connector. Vælg dokumentprovideren og den connector, du har indlæst tidligere. Opdater [indstillingerne for datatilknytning](#default-data-mapping) efter behov.
1. Gå til **Retail og Commerce \> Konfiguration af kanal \> Regnskabsintegration \> Tekniske profiler for connector**. Opret en ny teknisk profil for connector, og vælg den regnskabsconnector, du indlæste tidligere. Opdater [indstillingerne for connector](#fiscal-connector-settings) efter behov.
6. Gå til **Retail og Commerce \> Konfiguration af kanal \> Regnskabsintegration \> Regnskabsconnectorgrupper**. Opret en ny regnskabsconnector-gruppe for den funktionsprofil for connector, som du oprettede tidligere.
7. Gå til **Retail og Commerce \> Konfiguration af kanal \> Regnskabsintegration \> Processer for regnskabsregistrering**. Opret en ny regnskabsregistreringsproces og et trin i processen til regnskabsregistrering, og vælg den regnskabsconnector-gruppe, du oprettede tidligere.
8. Gå til **Retail og Commerce \> Konfiguration af kanal \> POS-opsætning \> POS-profiler \> Funktionalitetsprofiler**. Vælg en funktionalitetsprofil, der er knyttet til den butik, hvor registreringsprocessen skal aktiveres. Vælg den regnskabsregistreringsproces, du oprettede tidligere, i oversigtspanelet **Regnskabsregistreringsproces**.
9. Gå til **Retail og Commerce \> Konfiguration af kanal \> POS-opsætning \> POS-profiler \> Hardwareprofiler**. Vælg en hardwareprofil, der er tilknyttet den hardwarestation, som bonprinteren skal være tilknyttet. Vælg den tekniske profil for connectoren, du oprettede tidligere, i oversigtspanelet **Eksterne regnskabsenheder**.
10. Åbn distributionsplanen (**Retail og Commerce \> Retail og Commerce IT \> Distributionsplan**), og vælg job **1070** og **1090** for at overføre data til kanaldatabasen.

#### <a name="default-data-mapping"></a>Tilknytning af standarddata

Følgende standarddatatilknytning er inkluderet i konfigurationen af regnskabsdokumentudbyderen som en del af eksemplet på regnskabsintegration:

- **Momskodetilknytning** – Denne tilknytning angiver enhedsspecifikke momskoder for tilsvarende momskoder. Tilknytningen af momskoden skal have følgende format:

    ```
    1 : code1 ; 2 : code2
    ```

    Her er en beskrivelse af dette format:

    - *1* og *2* er enhedsspecifikke momskoder.
    - Et semikolon (;) bruges som separator.
    - *code1* og *code2* er momskoder, der er konfigureret i Commerce Headquarters. Du skal redigere eksempeltilknytningen i overensstemmelse med de momskoder, der er konfigureret i programmet.

    Kontrolenheder understøtter op til fire forskellige momskoder. Tilknytningen af momskoden kan derfor konfigureres på følgende måde:

    ```
    1 : code1 ; 2 : code2 ; 3 : code3 ; 4 : code4
    ```

    > [!NOTE]
    > Flere momskoder kan knyttes til den samme enhedsspecifikke momskode.

#### <a name="fiscal-connector-settings"></a>Indstillinger af regnskabsconnector

Følgende indstillinger er inkluderet i konfigurationen af regnskabsconnectoren som en del af eksemplet på regnskabsintegration:

- **Forbindelsesstreng** – Forbindelsesindstillingerne for kontrolenheden.
- **Timeout** – Den tid i millisekunder, som driveren vil vente på et svar fra tjenesten til kontrolenheden.

### <a name="configure-channel-components"></a>Konfigurere kanalkomponenter

> [!WARNING]
> På grund af begrænsningerne ved den [nye uafhængige pakke- og udvidelsesmodel](../dev-itpro/build-pipeline.md) kan den ikke aktuelt bruges til dette eksempel på regnskabsintegration. Du skal bruge den tidligere version af Retail SDK på en virtuel maskine til udviklere i LCS. Du kan få flere oplysninger i [Retningslinjer for eksempel på integration af kontrolenhed for Sverige (ældre)](emea-swe-fi-sample-sdk.md).
>
> Understøttelse af den nye uafhængige pakke- og udvidelsesmodel til eksempler på regnskabsintegration er planlagt til senere versioner.

#### <a name="set-up-the-development-environment"></a>Konfigurere udviklingsmiljøet

Følg disse trin for at konfigurere et udviklingsmiljø, så du kan teste og udvide eksemplet.

1. Klon eller download lageret til [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions). Vælg en korrekt version af frigivelsesafdelingen i overensstemmelse med din SDK/programversion. Yderligere oplysninger finder du i [Hente Retail SDK-eksempler og -referencepakker fra GitHub og NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Åbn løsningen til integration af bonprinter på **Dynamics365Commerce.Solutions\\FiscalIntegration\\CleanCash\\CleanCash.sln**, og opbyg den.
1. Installer CRT-udvidelser:

    1. Find installationsprogrammet til CRT-udvidelsen:

        - **Commerce Scale Unit:** I mappen **CleanCash\\ScaleUnit\\ScaleUnit.CleanCash.Installer\\bin\\Debug\\net461** skal du finde installationsprogrammet **ScaleUnit.CleanCash.Installer**.
        - **Lokal CRT på Modern POS:** I mappen **CleanCash\\ModernPOS\\ModernPOS.CleanCash.Installer\\bin\\Debug\\net461** skal du finde installationsprogrammet **ModernPOS.CleanCash.Installer**.

    2. Start installationsprogrammet til CRT-udvidelsen fra kommandolinjen:

        - **Commerce Scale Unit:**

            ```Console
            ScaleUnit.CleanCash.Installer.exe install --verbosity 0
            ```

        - **Lokal CRT på Modern POS:**

            ```Console
            ModernPOS.CleanCash.Installer.exe install --verbosity 0
            ```

1. Installer udvidelser til Hardwarestation:

    1. I mappen **CleanCash\\HardwareStation\\HardwareStation.CleanCash.Installer\\bin\\Debug\\net461** skal du finde installationsprogrammet **HardwareStation.CleanCash.Installer**.
    1. Start installationsprogrammet til udvidelsen fra kommandolinjen:

        ```Console
        HardwareStation.CleanCash.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Produktionsmiljø

Følg trinnene i [Konfigurere en build-pipeline til et eksempel på regnskabsintegration](fiscal-integration-sample-build-pipeline.md) for at generere og frigive Cloud Scale Unit og pakker, der kan implementeres med selvbetjening, til eksemplet på regnskabsintegration. **CleanCash build-pipeline.yml**-skabelonens YAML-fil findes i mappen **Pipeline\\YAML_Files** i lageret til [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions).

## <a name="design-of-the-extensions"></a>Design af udvidelserne

Integrationseksemplet for kontrolenheden til Sverige er baseret på [funktionaliteten af regnskabsintegration](fiscal-integration-for-retail-channel.md) og er en del af Retail SDK. Eksemplet findes i mappen **src\\FiscalIntegration\\CleanCash** i lageret til [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (f.eks. [eksemplet i frigivelse/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/CleanCash)). Eksemplet [består](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) af en regnskabsdokumentudbyder, som er en udvidelse af CRT, og en regnskabsconnector, som er en udvidelse af Commerce Hardware Station. Yderligere oplysninger om, hvordan du bruger Retail SDK, finder du i [Retail SDK-arkitekturen](../dev-itpro/retail-sdk/retail-sdk-overview.md) og [Konfigurere en build-pipeline til uafhængige SDK-pakker](../dev-itpro/build-pipeline.md).

> [!WARNING]
> På grund af begrænsningerne ved den [nye uafhængige pakke- og udvidelsesmodel](../dev-itpro/build-pipeline.md) kan den ikke aktuelt bruges til dette eksempel på regnskabsintegration. Du skal bruge den tidligere version af Retail SDK på en virtuel maskine til udviklere i LCS. Du kan få flere oplysninger i [Retningslinjer for eksempel på integration af kontrolenhed for Sverige (ældre)](emea-swe-fi-sample-sdk.md). Understøttelse af den nye uafhængige pakke- og udvidelsesmodel til eksempler på regnskabsintegration er planlagt til senere versioner.

### <a name="crt-extension-design"></a>Design af CRT-udvidelse

Formålet med udvidelsen, som er en udbyder af regnskabsdokumenter, er at generere servicespecifikke dokumenter og håndtere svar fra kontrolenheden.

#### <a name="request-handler"></a>Anmodningshandler

Der er en enkelt **DocumentProviderCleanCash**-anmodningshandler til dokumentudbyder. Den bruges til at generere regnskabsdokumenter til kontrolenheden.

Denne handler er nedarvet fra brugergrænsefladen i **INamedRequestHandler**. Metoden **HandlerName** er ansvarlig for at returnere navnet på handleren. Navnet på handleren skal svare til navnet på connector-dokumentudbyderen, der er angivet i Commerce Headquarters.

Connectoren understøtter følgende anmodninger:

- **GetFiscalDocumentDocumentProviderRequest** – Denne anmodning indeholder oplysninger om, hvilket dokument der skal genereres. Den returnerer et servicespecifikt dokument, der skal registreres i kontrolenheden.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Denne anmodning returnerer listen over hændelser, der skal abonneres på. Salgshændelser og revisionshændelser understøttes i øjeblikket.

#### <a name="configuration"></a>Konfiguration

Konfigurationsfilen til regnskabsdokumentudbyderen er placeret i **src\\FiscalIntegration\\CleanCash\\CommerceRuntime\\DocumentProvider.CleanCashSample\\Configuration\\DocumentProviderFiscalCleanCashSample.xml** i lageret til [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Formålet med filen er at aktivere indstillinger for dokumentudbyderen, der skal konfigureres fra Commerce Headquarters. Filformatet er tilpasset kravene til konfiguration af regnskabsintegration.

### <a name="hardware-station-extension-design"></a>Design af hardwarestationsudvidelse

Formålet med den forlængelse, der er en regnskabsmæssig connector, er at kommunikere med kontrolenheden. Den bruger HTTP-protokollen til at sende dokumenter, som CRT-udvidelsen genererer til kontrolenheden. Den håndterer også de svar, der er modtaget fra kontrolenheden.

#### <a name="request-handler"></a>Anmodningshandler

Anmodningshandleren **CleanCashHandler** er indgangspunktet for håndtering af anmodninger til kontrolenheden.

Denne handler er nedarvet fra brugergrænsefladen i **INamedRequestHandler**. Metoden **HandlerName** er ansvarlig for at returnere navnet på handleren. Navnet på handleren skal svare til navnet på den regnskabsconnector, der er angivet i Commerce Headquarters.

Connectoren understøtter følgende anmodninger:

- **SubmitDocumentFiscalDeviceRequest** – Denne anmodning sender dokumenter til kontrolenheden og returnerer et svar fra den.
- **IsReadyFiscalDeviceRequest** – Denne anmodning bruges til tilstandskontrol af kontrolenheden.
- **InitializeFiscalDeviceRequest** – Denne anmodning bruges til at initialisere kontrolenheden.

#### <a name="configuration"></a>Konfiguration

Konfigurationsfilen til regnskabsconnectoren er placeret i **src\\FiscalIntegration\\CleanCash\\HardwareStation\\Connector.CleanCashSample\\Configuration\\ConnectorCleanCashSample.xml** i lageret for [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Formålet med filen er at aktivere indstillinger for regnskabsconnectoren, der skal konfigureres fra Commerce Headquarters. Filformatet er tilpasset kravene til konfiguration af regnskabsintegration.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
