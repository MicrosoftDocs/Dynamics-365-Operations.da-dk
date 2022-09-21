---
title: Eksempel på integration af bonprinter i Polen
description: Denne artikel indeholder en oversigt over eksemplet på regnskabsintegration for Polen i Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 08/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-02-01.
ms.openlocfilehash: d4e99854f5e3ab9a6ae802f4f6bcde7918f72e6d
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473761"
---
# <a name="fiscal-printer-integration-sample-for-poland"></a>Eksempel på integration af bonprinter i Polen

[!include [banner](../includes/banner.md)]

Denne artikel indeholder en oversigt over eksemplet på regnskabsintegration for Polen i Microsoft Dynamics 365 Commerce.

Funktionaliteten af Dynamics 365 Commerce for Polen omfatter en eksempelintegration af POS med en bonprinter. Eksemplet udvider [funktionaliteten af regnskabsintegration](fiscal-integration-for-retail-channel.md) og understøtter POSNET THERMAL HD 2.02-protokol for bonprintere fra [Posnet Polska S.A.](https://www.posnet.com.pl) Eksemplet giver mulighed for at kommunikere med en bonprinter, der er tilsluttet via en COM-port med en indbygget softwaredriver. Den er implementeret og testet ved hjælp af en software-emulator, som Posnet har leveret til bonprinteren Posnet Thermal HD FV EJ. Eksemplet findes i form af kildekode og er en del af Commerce SDK (Software Development Kit).

Microsoft frigiver ikke hardware, software eller dokumentation fra Posnet. Oplysninger om, hvordan du henter bonprinteren og bruger den, får du ved at kontakte [Posnet Polska S.A.](https://www.posnet.com.pl)

## <a name="scenarios"></a>Scenarier

Følgende scenarier dækkes af eksemplet på integration af bonprinter for Polen:

- Salgsscenarier:

    - Udskriv en regnskabskvittering for cash-and-carry-salg og returneringer.
    - Hent et svar fra bonprinteren, og gem det i kanaldatabasen.
    - Moms:

        - Knyt til bonprinterens momskoder (afdelinger).
        - Overfør tilknyttede momsdata til bonprinteren.

    - Betalinger:

        - Knyt til bonprinterens betalingsmetoder.
        - Udskriv betalinger på en regnskabskvittering.
        - Udskriv ændringsoplysninger.

    - Udskriv linjerabatter.
    - Gavekort:

        - Udelad en udstedt/genopfyldt gavekortlinje fra en regnskabskvittering for et salg.
        - Udskriv en betaling, der bruger et gavekort som almindelig betalingsmåde.

    - Udskriv regnskabskvitteringer for kundeordreoperationer:

        - En regnskabskvittering udskrives ikke for en indbetaling af en kundeordre.
        - Udskriv en regnskabskvittering for udførelseslinjer i en hybridkundeordre.
        - Udskriv en regnskabskvittering for afhentningsoperationen for en kundeordre.
        - Udskriv en regnskabskvittering for en returordre.

    - Udskriv de [kundeoplysninger](emea-pol-customer-information.md), der er angivet for en salgstransaktion, på en regnskabskvittering. Dette er f.eks. kundens momsnummer.

- Opgørelser ved lukketid (regnskabsmæssige X- og Z-rapporter).
- Fejlhåndtering som f.eks. følgende muligheder:

    - Forsøg at registrere et regnskab igen, hvis der kan udføres et nyt forsøg, f.eks. hvis bonprinteren ikke er tilsluttet, eller hvis printeren ikke er klar eller ikke svarer, printeren er løbet tør for papir, eller der er papirstop.
    - Udskyd regnskabsregistrering.
    - Undlad regnskabsregistrering, eller markér transaktionen som registreret, og inkluder infokoder for at registrere årsagen til fejlen og flere oplysninger.
    - Kontrollér, om bonprinteren er tilgængelig, før en ny salgstransaktion åbnes, eller en salgstransaktion færdiggøres.

### <a name="gift-cards"></a>Gavekort

I eksemplet med integration af bonprinter implementeres følgende regler, der er relateret til gavekort:

- Udelad salgslinjer, der er relateret til handlingerne *Udsted gavekort* og *Føj til gavekort* fra regnskabskvitteringen.
- Udskriv ikke en regnskabskvittering, hvis den kun består af gavekortlinjer.
- Fratræk det samlede beløb af gavekort, der er udstedt eller genopfyldt i en transaktion, fra betalingslinjer i regnskabskvitteringen.
- Gem beregnede reguleringer af betalingslinjer i kanaldatabasen med en reference til en tilsvarende regnskabstransaktion.
- Betaling med gavekort betragtes som en almindelig betaling.

### <a name="customer-deposits-and-customer-order-deposits"></a>Kundeindbetalinger og indbetalinger for kundeordrer

I eksemplet med integration af bonprinter implementeres følgende regler, der er relateret til kundeindbetalinger og indbetalinger for kundeordrer:

- Udskriv ikke en regnskabskvittering, hvis en transaktion er en kundeindbetaling.
- Udskriv ikke en regnskabskvittering, hvis en transaktion kun indeholder en kundeordreindbetaling eller en refusion af en kundeordreindbetaling.
- Udskriv beløbet af den tidligere betalte indbetaling på en regnskabskvittering for en operation med afhentning af en kundeordre.
- Træk indbetalingsbeløbet for kundeordren fra betalingslinjerne, når der oprettes en hybridkundeordre.
- Gem beregnede reguleringer af betalingslinjer i kanaldatabasen med en reference til en tilsvarende regnskabstransaktion for en hybrid kundeordre.

### <a name="limitations-of-the-sample"></a>Begrænsninger for eksemplet

- Bonprinteren understøtter kun scenarier, hvor moms er inkluderet i prisen. Derfor skal indstillingen **Prisen inkluderer moms** angives til **Ja** for både butikker og kunder.
- Daglige rapporter (regnskab X og regnskab Z) udskrives ved hjælp af det integrerede *Skift rapport*-format.
- Udskrivning af en stregkode på regnskabskvitteringerne betragtes som en potentiel tilpasning, da denne funktion ikke understøttes i de integrerede formater og kun kan implementeres ved hjælp af rapporten **Super-format**, der kan tilpasses.
- Bonprinteren understøtter ikke blandede transaktioner. Indstillingen **Forbyd blanding af salg og returneringer på én kvittering** skal angives til **Ja** i POS-funktionsprofiler.

## <a name="set-up-fiscal-integration-for-poland"></a>Konfigurere regnskabsintegration for Polen

Bonprinterintegrationens eksempel til Polen er baseret på [funktionaliteten af regnskabsintegration](fiscal-integration-for-retail-channel.md) og er en del af Commerce SDK. Eksemplet på POS-udvidelse findes i mappen **src\\FiscalIntegration\\Posnet** i lageret til [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions/). [Eksemplet](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) består af en regnskabsdokumentudbyder, som er en udvidelse af Commerce Runtime (CRT), og en regnskabsconnector, som er en udvidelse af Commerce Hardware Station. Yderligere oplysninger om, hvordan du bruger Commerce SDK, finder du i [Download Commerce SDK-prøver og -referencepakker fra GitHub og NuGet](../dev-itpro/retail-sdk/sdk-github.md) og [oprette en build-pipeline til den uafhængige emballage SDK](../dev-itpro/build-pipeline.md).

> [!NOTE]
> Integration af regnskabsprinter for Polen er tilgængelig i Commerce SDK som pr. Commerce-version 10.0.29. I Commerce-version 10.0.28 eller tidligere skal du bruge den tidligere version af Retail SDK på en virtuel maskine til udviklere (VM) i Microsoft Dynamics Lifecycle Services (LCS). Du kan få flere oplysninger i [Retningslinjer for installation af eksempel på integration af bonprinter i Polen (ældre)](emea-pol-fpi-sample-sdk.md).

Fuldfør trinnene til opsætning af regnskabsintegration som beskrevet i [Konfigurere regnskabsintegration for Commerce-kanaler](setting-up-fiscal-integration-for-retail-channel.md).

1. [Konfigurer en regnskabsregistreringsproces](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Du skal også notere dig indstillingerne for den regnskabsregistreringsproces, der er [specifik for dette eksempel på integration af bonprinter](#set-up-the-registration-process).
1. [Angive indstillinger for fejlhåndtering](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Oprette X/Z-regnskabsrapporter fra POS](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos).
1. [Aktiver manuel udførelse af udsatte regnskabsregistreringer](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Konfigurere kanalkomponenter](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Konfigurere registreringsprocessen

Hvis du vil aktivere registreringsprocessen, skal du følge disse trin for at konfigurere Commerce Headquarters. Du kan finde flere oplysninger i [Konfigurere regnskabsintegration for Commerce-kanaler](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Download konfigurationsfiler for regnskabsconnectoren og regnskabsdokumentudbyderen:

    1. Åbn lageret il [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions/).
    1. Vælg en korrekt version af frigivelsesafdelingen i overensstemmelse med din SDK/programversion.
    1. Åbn **src \> FiscalIntegration \> Posnet**.
    1. Hent konfigurationsfilen til regnskabsdokumentudbyderen på **CommerceRuntime \> DocumentProvider.PosnetSample \> Konfiguration \> DocumentProviderPosnetSample.xml**.
    1. Hent konfigurationsfilen til regnskabsconnectoren på **HardwareStation \> ThermalDeviceSample \> Konfiguration \> ThermalDeviceSample.xml**.

    > [!NOTE]
    > I Commerce-version 10.0.28 eller tidligere skal du bruge den tidligere version af Retail SDK på en virtuel maskine til udviklere i LCS. Konfigurationsfilerne til dette eksempel på regnskabsintegration findes i følgende mapper i Retail SDK på en udvikler VM i LCS:
    >
    > - **Konfigurationsfilen til regnskabsdokumentudbyder:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extension.DocumentProvider.PosnetSample\\Configuration\\DocumentProviderPosnetSample.xml
    > - **Konfigurationsfil til regnskabsconnector:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.Posnet.ThermalDeviceSample\\Configuration\\ConnectorPosnetThermalFVEJ.xml

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

- **Tilknytning af momssatser** – Tilknytning af momsprocentværdier, der er oprettet for momskoder til bonprinterspecifikke momssatser. Her er standardtilknytningen:

    ```
    0 : 23.00 ; 1 : 8.00 ; 2 : 5.00 ; 3 : 0.00
    ```

    Den første komponent i hvert par repræsenterer et momssatsnummer, der er konfigureret i bonprinteren. Den anden komponent repræsenterer den tilsvarende momssats. Yderligere oplysninger om konfiguration af momssats for bonprinteren finder du i dokumentationen til POSNET-driveren.

- **Tilknytning af betalingsmiddeltype** – Tilknytning af betalingsmetoder, der er konfigureret for butikken, til betalingstyper, som bonprinteren understøtter. Her er standardtilknytningen:

    ```
    0 : 0 ; 1 : 0 ; 2 : 2 ; 3 : 2 ; 4 : 0 ; 5 : 0 ; 6 : 0 ; 7 : 2 ; 8 : 0
    ```

    Den første komponent i de enkelte par repræsenterer en betalingsmetode, der er konfigureret for butikken. Den anden komponent repræsenterer den tilsvarende betalingsmåde, der understøttes af bonprinteren. Yderligere oplysninger om betalingsmåder, som bonprinteren understøtter, finder du i dokumentationen til POSNET-driveren. Du skal redigere eksempeltilknytningen i overensstemmelse med de betalingsmetoder, der er konfigureret i dit program.

#### <a name="fiscal-connector-settings"></a>Indstillinger af regnskabsconnector

Følgende indstillinger er inkluderet i konfigurationen af regnskabsconnectoren som en del af eksemplet på regnskabsintegration:

- **Forbindelsesstreng** – En streng, der beskriver detaljerne om forbindelsen til enheden i et format, som driveren understøtter. Yderligere oplysninger finder du i dokumentationen til POSNET-driveren.
- **Dato- og tidssynkronisering** – En værdi, der angiver, om datoen og klokkeslættet for printeren skal synkroniseres med den tilknyttede hardwarestation.
- **Timeout for enhed** – Den tid i millisekunder, som driveren vil vente på et svar fra enheden. Yderligere oplysninger finder du i dokumentationen til POSNET-driveren.

### <a name="configure-channel-components"></a>Konfigurere kanalkomponenter

> [!NOTE]
> - Integration af regnskabsprinter for Polen er tilgængelig i Commerce SDK som pr. Commerce-version 10.0.29. I Commerce-version 10.0.28 eller tidligere skal du bruge den tidligere version af Retail SDK på en virtuel maskine til udviklere i LCS. Du kan få flere oplysninger i [Retningslinjer for installation af eksempel på integration af bonprinter i Polen (ældre)](emea-pol-fpi-sample-sdk.md).
> - Handelsprøver, der implementeres i dit miljø, opdateres ikke automatisk, når du anvender tjeneste- eller kvalitetsopdateringer på Commerce-komponenter. Du skal opdatere de påkrævede prøver manuelt.

#### <a name="set-up-the-development-environment"></a>Konfigurere udviklingsmiljøet

Følg disse trin for at konfigurere et udviklingsmiljø, så du kan teste og udvide eksemplet.

1. Klon eller download lageret til [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions). Vælg en korrekt version af frigivelsesafdelingen i overensstemmelse med din SDK/programversion. Yderligere oplysninger finder du i [Hente Commerce SDK-eksempler og -referencepakker fra GitHub og NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Åbn løsningen til integration af regnskabsprinter på **Dynamics365Commerce.Solutions\\FiscalIntegration\\Posnet\\Posnet.sln**, og opbyg den.
1. Installer CRT-udvidelser:

    1. Find installationsprogrammet til CRT-udvidelsen:

        - **Commerce Scale Unit:** I mappen **Posnet\\ScaleUnit\\ScaleUnit.Posnet.Installer\\bin\\Debug\\net461** skal du finde installationsprogrammet **ScaleUnit.Posnet.Installer**.
        - **Lokal CRT på Modern POS:** I mappen **Posnet\\ModernPOS\\ModernPOS.Posnet.Installer\\bin\\Debug\\net461** skal du finde installationsprogrammet **ModernPOS.Posnet.Installer**.

    1. Start installationsprogrammet til CRT-udvidelsen fra kommandolinjen:

        - **Commerce Scale Unit:**

            ```Console
            ScaleUnit.Posnet.Installer.exe install --verbosity 0
            ```

        - **Lokal CRT på Modern POS:**

            ```Console
            ModernPOS.Posnet.Installer.exe install --verbosity 0
            ```

1. Installer udvidelser til Hardwarestation:

    1. I mappen **Posnet\\HardwareStation\\HardwareStation.PosnetThermalFVFiscalPrinter.Installer\\bin\\Debug\\net461** finder du installationsprogrammet **HardwareStation.PosnetThermalFVFiscalPrinter.Installer**.
    1. Start installationsprogrammet til udvidelsen fra kommandolinjen:

        ```Console
        HardwareStation.PosnetThermalFVFiscalPrinter.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Produktionsmiljø

Følg trinnene i [Konfigurere en build-pipeline til et eksempel på regnskabsintegration](fiscal-integration-sample-build-pipeline.md) for at generere og frigive Cloud Scale Unit og pakker, der kan implementeres med selvbetjening, til eksemplet på regnskabsintegration. **Posnet build-pipeline.yml**-skabelonens YAML-fil findes i mappen **Pipeline\\YAML_Files** i lageret til [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions).

## <a name="design-of-extensions"></a>Design af udvidelser

Bonprinterintegrationens eksempel til Polen er baseret på [funktionaliteten af regnskabsintegration](fiscal-integration-for-retail-channel.md) og er en del af Commerce SDK. Eksemplet på POS-udvidelse findes i mappen **src\\FiscalIntegration\\Posnet** i lageret til [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions/). [Eksemplet](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) består af en regnskabsdokumentudbyder, som er en udvidelse af CRT, og en regnskabsconnector, som er en udvidelse af Commerce Hardware Station. Yderligere oplysninger om, hvordan du bruger Commerce SDK, finder du i [Download Commerce SDK-prøver og -referencepakker fra GitHub og NuGet](../dev-itpro/retail-sdk/sdk-github.md) og [oprette en build-pipeline til den uafhængige emballage SDK](../dev-itpro/build-pipeline.md).

> [!NOTE]
> Integration af regnskabsprinter for Polen er tilgængelig i Commerce SDK som pr. Commerce-version 10.0.29. I Commerce-version 10.0.28 eller tidligere skal du bruge den tidligere version af Retail SDK på en virtuel maskine til udviklere i LCS. Du kan få flere oplysninger i [Retningslinjer for installation af eksempel på integration af bonprinter i Polen (ældre)](emea-pol-fpi-sample-sdk.md).

### <a name="commerce-runtime-extension-design"></a>Design af Commerce Runtime-udvidelse

Formålet med udvidelsen, som er en udbyder af regnskabsdokumenter, er at generere printerspecifikke dokumenter og håndtere svar fra bonprinteren. Denne udvidelse genererer et sæt printerspecifikke kommandoer i JSON-format (JavaScript Object Notation), der er defineret af POSNET-specifikation 19-3678.

#### <a name="request-handler"></a>Anmodningshandler

Anmodningshandleren **DocumentProviderPosnetProtocol** er indgangspunktet for anmodningen om at generere dokumenter fra bonprinteren.

Denne handler er nedarvet fra brugergrænsefladen i **INamedRequestHandler**. Metoden **HandlerName** er ansvarlig for at returnere navnet på handleren. Navnet på handleren skal svare til navnet på connector-dokumentudbyderen, der er angivet i Commerce Headquarters.

Connectoren understøtter følgende anmodninger:

- **GetFiscalDocumentDocumentProviderRequest** – Denne anmodning indeholder oplysninger om, hvilket dokument der skal genereres. Den returnerer et printerspecifikt dokument, der skal registreres i bonprinteren.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Denne anmodning returnerer listen over hændelser, der skal abonneres på. Aktuelt understøttes følgende hændelser: salg, udskrivning af X-rapport og udskrivning af Z-rapport.

#### <a name="configuration"></a>Konfiguration

Konfigurationsfilen til regnskabsdokumentudbyderen er placeret i **src\\FiscalIntegration\\Posnet\\CommerceRuntime\\DocumentProvider.PosnetSample\\Configuration\\DocumentProviderPosnetSample.xml** i lageret til [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Formålet med filen er at aktivere indstillinger for regnskabsdokumentudbyderen, der skal konfigureres fra Commerce Headquarters. Filformatet er tilpasset kravene til konfiguration af regnskabsintegration.

### <a name="hardware-station-extension-design"></a>Design af hardwarestationsudvidelse

Formålet med den forlængelse, der er en regnskabsmæssig connector, er at kommunikere med bonprinteren. Denne udvidelse kalder POSNET-driverens funktioner for at sende kommandoer, som CRT-udvidelsen genererer, til bonprinteren. Den håndterer også enhedsfejl.

#### <a name="request-handler"></a>Anmodningshandler

Anmodningshandleren **FiscalPrinterHandler** er indgangspunktet for håndtering af anmodningen til den eksterne regnskabsenhed.

Denne handler er nedarvet fra brugergrænsefladen i **INamedRequestHandler**. Metoden **HandlerName** er ansvarlig for at returnere navnet på handleren. Navnet på handleren skal svare til navnet på den regnskabsconnector, der er angivet i Commerce Headquarters.

Connectoren understøtter følgende anmodninger:

- **SubmitDocumentFiscalDeviceRequest** – Denne anmodning sender dokumenter til printere og returnerer svar fra bonprinteren.
- **IsReadyFiscalDeviceRequest** – Denne anmodning bruges til tilstandskontrol af enheden.
- **InitializeFiscalDeviceRequest** – Denne anmodning bruges til at initialisere printeren.

#### <a name="configuration"></a>Konfiguration

Konfigurationsfilen til regnskabsconnectoren er placeret i **src\\FiscalIntegration\\Posnet\\HardwareStation\\ThermalDeviceSample\\Configuration\\ConnectorPosnetThermalFVEJ.xml** i lageret til [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Formålet med filen er at aktivere indstillinger for regnskabsconnectoren, der skal konfigureres fra Commerce Headquarters. Filformatet er tilpasset kravene til konfiguration af regnskabsintegration.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
