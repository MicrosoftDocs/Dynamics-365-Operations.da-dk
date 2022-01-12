---
title: Retningslinjer for installation af eksempel på integration af regnskabsregistreringsservice i Østrig (ældre)
description: Dette emne indeholder retningslinjer for implementering af eksempel på regnskabsintegration for Østrig fra Microsoft Dynamics 365 Commerce Retail SDK (Software Development Kit).
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: c038773dc7c1c475f5852f0f0272b59516140593
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944657"
---
# <a name="deployment-guidelines-for-the-fiscal-registration-service-integration-sample-for-austria-legacy"></a>Retningslinjer for installation af eksempel på integration af regnskabsregistreringsservice i Østrig (ældre)

[!include [banner](../includes/banner.md)]

Dette emne indeholder retningslinjer for implementering af eksempel på integration af regnskabsregistreringstjeneste for Østrig fra Microsoft Dynamics 365 Commerce Retail SDK (Software Development Kit) på en virtuel maskine (VM) til udviklere i Microsoft Dynamics Lifecycle Services (LCS). Du kan finde flere oplysninger om regnskabsintegrationseksemplet i [Eksempel på regnskabsintegrationsservice for Østrig](emea-aut-fi-sample.md). 

Eksemplet på regnskabsintegration for Østrig er en del af Retail SDK. Du kan finde oplysninger om, hvordan du installerer og bruger SDK, i [Arkitektur for udviklingsværktøjskasse (SDK) til Retail](../dev-itpro/retail-sdk/retail-sdk-overview.md). Eksemplet på regnskabsintegration består af udvidelser til Commerce Runtime (CRT), Hardwarestation og POS. Hvis du vil køre dette eksempel, skal du redigere og bygge CRT, Hardwarestation og POS-projekter. Det anbefales, at du bruger en ikke-ændret Retail SDK til at foretage de ændringer, der er beskrevet i dette emne. Det anbefales også, at du bruger et kildekontrolsystem som f.eks. Azure DevOps, hvor ingen filer er ændret endnu.

## <a name="development-environment"></a>Udviklingsmiljø

Følg disse trin for at konfigurere et udviklingsmiljø, så du kan teste og udvide eksemplet.

### <a name="enable-commerce-runtime-extensions"></a>Aktivere Commerce Runtime-udvidelser

CRT-udvidelseskomponenterne er inkluderet i CRT-eksemplerne. Du kan fuldføre følgende procedurer ved at åbne løsningen **CommerceRuntimeSamples.sln** under **RetailSdk\\SampleExtensions\\CommerceRuntime**.

#### <a name="documentproviderefrsample-component"></a>Komponenten DocumentProvider.EFRSample

1. Find projektet **Runtime.Extensions.DocumentProvider.EFRSample**, og opbyg det.
2. I mappen **Runtime.Extensions.DocumentProvider.EFRSample\\bin\\Debug** kan du finde assemblyfilen **Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll**.
3. Kopiér assembly-filen til CRT-udvidelsesmappen:

    - **Commerce Scale Unit:** Kopiér filen til mappen **\\bin\\ext** under IIS-webstedet (Internet Information Services) for Commerce Scale Unit.
    - **Lokal CRT på Modern POS:** Kopiér filen til mappen **\\ext** under den lokale CRT Client Broker-placering.

4. Find konfigurationsfilen til CRT-udvidelse:

    - **Commerce Scale Unit:** Filen kaldes **commerceruntime.ext.config**, og den findes i mappen **bin\\ext** under placeringen af webstedet IIS Commerce Scale Unit.
    - **Lokal CRT på Modern POS:** Filen hedder **CommerceRuntime.MPOSOffline.Ext.config**, og den findes under den lokale placering af CRT Client Broker.

5. Registrer CRT-ændringen i konfigurationsfilen til udvidelsen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
    ```

#### <a name="documentproviderdatamodelefr-component"></a>Komponenten DocumentProvider.DataModelEFR

1. Find projektet **Runtime.Extensions.DocumentProvider.DataModelEFR**, og opbyg det.
2. I mappen **Runtime.Extensions.DocumentProvider.DataModelEFR\\bin\\Debug** kan du finde assemblyfilen **Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll**.
3. Kopiér assembly-filen til CRT-udvidelsesmappen:

    - **Commerce Scale Unit:** Kopiér filen til mappen **\\bin\\ext** under IIS-webstedet for Commerce Scale Unit.
    - **Lokal CRT på Modern POS:** Kopiér filen til mappen **\\ext** under den lokale CRT Client Broker-placering.

4. Find konfigurationsfilen til CRT-udvidelse:

    - **Commerce Scale Unit:** Filen kaldes **commerceruntime.ext.config**, og den findes i mappen **bin\\ext** under placeringen af webstedet IIS Commerce Scale Unit.
    - **Lokal CRT på Modern POS:** Filen hedder **CommerceRuntime.MPOSOffline.Ext.config**, og den findes under den lokale placering af CRT Client Broker.

5. Registrer CRT-ændringen i konfigurationsfilen til udvidelsen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
    ```

#### <a name="extension-configuration-file"></a>Konfigurationsfil til udvidelse

1. Find konfigurationsfilen til CRT-udvidelse:

    - **Commerce Scale Unit:** Filen kaldes **commerceruntime.ext.config**, og den findes i mappen **bin\\ext** under placeringen af webstedet IIS Commerce Scale Unit.
    - **Lokal CRT på Modern POS:** Filen hedder **CommerceRuntime.MPOSOffline.Ext.config**, og den findes under den lokale placering af CRT Client Broker.

2. Registrer CRT-ændringen i konfigurationsfilen til udvidelsen.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsAustria" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventAustria" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.XZReportsAustria" />
    ```

### <a name="enable-hardware-station-extensions"></a>Aktivere hardwarestationsudvidelser

Udvidelseskomponenterne for hardwarestationen er inkluderet i eksemplerne til Hardwarestation. Du kan fuldføre følgende procedurer ved at åbne løsningen **HardwareStationSamples.sln** under **RetailSdk\\SampleExtensions\\HardwareStation**.

#### <a name="efrsample-component"></a>Komponenten EFRSample

1. Find projektet **HardwareStation.Extension.EFRSample**, og opbyg det.
2. Find følgende assembly-filer i mappen **Extension.EFRSample\\bin\\Debug**:

    - Contoso.Commerce.HardwareStation.EFRSample.dll
    - Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll

3. Kopiér assembly-filerne til mappen med udvidelser til Hardwarestation:

    - **Delt hardwarestation:** Kopiér filerne til mappen **bin** under placeringen af IIS-webstedet for Hardwarestation.
    - **Dedikeret hardwarestation på Modern POS:** Kopiér filerne til Client Broker-placeringen for Modern POS.

4. Find udvidelsens konfigurationsfil til hardwarestationens udvidelser. Filen hedder **HardwareStation.Extension.config**.

    - **Delt hardwarestation:** Filen ligger under placeringen af IIS-webstedet for Hardwarestation.
    - **Dedikeret hardwarestation på Modern POS:** Filen ligger under Client Broker-placeringen for Modern POS.

5. Føj følgende linje til sektionen **komposition** i konfigurationsfilen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample.dll" />
    ```

### <a name="enable-modern-pos-extension-components"></a>Aktivere komponenter for udvidelse af Modern POS

1. Åbn løsningen **ModernPOS.sln** under **RetailSdk\\POS**, og kontrollér, at den kan kompileres uden fejl. Derudover skal du sørge for, at du kan køre Modern POS fra Visual Studio ved hjælp af kommandoen **Kør**.

    > [!NOTE]
    > Modern POS må ikke tilpasses. Du skal aktivere User Account Control (UAC), og du skal afinstallere tidligere installerede forekomster af Modern POS efter behov.

2. Aktivér udvidelserne til indlæsning ved at tilføje følgende linjer i filen **extensions.json**.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.AT"
            }
        ]
    }
    ```

    > [!NOTE]
    > Yderligere oplysninger og eksempler, der viser, hvordan du medtager kildekodemapper og aktiverer udvidelser, der skal indlæses, finder du i instruktionerne i readme.md-filen i projektet **Pos.Extensions**.

3. Genopbyg løsningen.
4. Kør Modern POS i fejlfindingsfunktionen, og test funktionaliteten.

### <a name="enable-cloud-pos-extension-components"></a>Aktivere komponenter for udvidelse af Cloud POS

1. Åbn løsningen **CloudPOS.sln** under **RetailSdk\\POS**, og kontrollér, at den kan kompileres uden fejl.
2. Aktivér udvidelserne til indlæsning ved at tilføje følgende linjer i filen **extensions.json**.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.AT"
            }
        ]
    }
    ```

    > [!NOTE]
    > Yderligere oplysninger og eksempler, der viser, hvordan du medtager kildekodemapper og aktiverer udvidelser, der skal indlæses, finder du i instruktionerne i readme.md-filen i projektet **Pos.Extensions**.

3. Genopbyg løsningen.
4. Kør løsningen ved at bruge kommandoen **Kør** og følge trinnene i Retail SDK-håndbogen.

## <a name="production-environment"></a>Produktionsmiljø

Den foregående procedure aktiverer de udvidelser, der er komponenter i eksemplet til regnskabsintegrationstjenesten. Derudover skal du følge disse trin for at oprette installerbare pakker, der indeholder Commerce-komponenter, og for at anvende disse pakker i et produktionsmiljø.

1. Foretag følgende ændringer i pakkekonfigurationsfilerne under mappen **RetailSdk\\Assets**:

    - I konfigurationsfilerne **commerceruntime.ext.config** og **CommerceRuntime.MPOSOffline.Ext.config** skal du føje følgende linjer til afsnittet **komposition**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsAustria" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventAustria" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.XZReportsAustria" />
        ```

    - Føj følgende linje til sektionen **komposition** i konfigurationsfilen **HardwareStation.Extension.config**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        ```

2. Foretag følgende ændringer i konfigurationsfilen til **Customization.settings**-pakkeindstillinger under mappen **BuildTools**:

    - Tilføj følgende linjer for at inkludere CRT-udvidelserne i installationspakkerne.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

    - Tilføj følgende linjer for at inkludere Hardwarestation-udvidelsen i installationspakkerne.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EFRSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

3. Start MSBuild-kommandoprompten for Visual Studio-hjælpeværktøjet, og kør **msbuild** under Retail SDK-mappen for at oprette installationspakkerne.
4. Anvend pakkerne via LCS eller manuelt. Du kan finde flere oplysninger under [Oprette installerbare pakker](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
5. Udfør alle de nødvendige opsætningsopgaver, der er beskrevet i [Konfigurere Commerce for Østrig](emea-aut-fi-sample.md#set-up-commerce-for-austria).

## <a name="design-of-extensions"></a>Design af udvidelser

Regnskabsintegrationstjenestens eksempel til Østrig er baseret på [funktionaliteten af regnskabsintegration](fiscal-integration-for-retail-channel.md). Du kan finde flere oplysninger om designet af løsningen til regnskabsintegration i [Oversigt over eksempeldesign til regnskabsintegration](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices).

### <a name="commerce-runtime-extension-design"></a>Design af Commerce Runtime-udvidelse

Formålet med udvidelsen, som er en udbyder af regnskabsdokumenter, er at generere servicespecifikke dokumenter og håndtere svar fra tjenesten til regnskabsregistrering.

Udvidelsen CRT er **Runtime.Extensions.DocumentProvider.EFRSample**.

#### <a name="request-handler"></a>Anmodningshandler

Der er to anmodningshandlere til dokumentudbydere:

- **DocumentProviderEFRFiscalAUT** – Denne handler bruges til at generere regnskabsdokumenter til regnskabsregistreringstjenesten.
- **DocumentProviderEFRNonFiscalAUT** – Denne handler bruges til at generere ikke-regnskabsdokumenter til regnskabsregistreringstjenesten.

Disse handlere er nedarvet fra brugergrænsefladen i **INamedRequestHandler**. Metoden **HandlerName** er ansvarlig for at returnere navnet på handleren. Navnet på handleren skal svare til navnet på connector-dokumentudbyderen, der er angivet i Commerce Headquarters.

Connectoren understøtter følgende anmodninger:

- **GetFiscalDocumentDocumentProviderRequest** – Denne anmodning indeholder oplysninger om, hvilket dokument der skal genereres. Den returnerer et servicespecifikt dokument, der skal registreres i tjenesten til regnskabsregistrering.
- **GetNonFiscalDocumentDocumentProviderRequest** – Denne anmodning indeholder oplysninger om, hvilket ikke-regnskabsdokument der skal genereres. Den returnerer et servicespecifikt dokument, der skal registreres i tjenesten til regnskabsregistrering.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Denne anmodning returnerer listen over hændelser, der skal abonneres på. Aktuelt understøttes følgende hændelser: salg, udskrivning af X-rapport, udskrivning af Z-rapport, indbetalinger på kundekonti, indbetalinger til kundeordrer, revisionshændelser og transaktioner, der ikke er salg.
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** – Denne anmodning returnerer svaret fra tjenesten til regnskabsregistrering. Dette svar er serialiseret, så det danner en streng og er klar til at blive gemt.

#### <a name="configuration"></a>Konfiguration

Konfigurationsfilerne findes i mappen **Konfiguration** for udvidelsesprojektet:

- **DocumentProviderFiscalEFRSampleAustria** – Til regnskabsdokumenter.
- **DocumentProviderNonFiscalEFRSampleAustria** – Til ikke-regnskabsdokumenter.

Formålet med disse filer er at aktivere indstillinger for dokumentudbyderen, der skal konfigureres fra Commerce Headquarters. Filformatet er tilpasset kravene til konfiguration af regnskabsintegration. Følgende indstilling tilføjes:

- Tilknytning af momssatser

### <a name="hardware-station-extension-design"></a>Design af hardwarestationsudvidelse

Formålet med den forlængelse, der er en regnskabsmæssig connector, er at kommunikere med tjenesten til regnskabsregistrering.

Udvidelsen til Hardwarestation er **HardwareStation.Extension.EFRSample**. Den bruger HTTP-protokollen til at sende dokumenter, som CRT-udvidelsen genererer til regnskabsregistreringstjenesten. Den håndterer også de svar, der er modtaget fra tjenesten til regnskabsregistrering.

#### <a name="request-handler"></a>Anmodningshandler

Anmodningshandleren **EFRHandler** er indgangspunktet for håndtering af anmodninger til tjenesten til regnskabsregistrering.

Denne handler er nedarvet fra brugergrænsefladen i **INamedRequestHandler**. Metoden **HandlerName** er ansvarlig for at returnere navnet på handleren. Navnet på handleren skal svare til navnet på den regnskabsconnector, der er angivet i Commerce Headquarters.

Connectoren understøtter følgende anmodninger:

- **SubmitDocumentFiscalDeviceRequest** – Denne anmodning sender dokumenter til tjenesten til regnskabsregistrering og returnerer et svar fra den.
- **IsReadyFiscalDeviceRequest** – Denne anmodning bruges til tilstandskontrol af tjenesten til regnskabsregistrering.
- **InitializeFiscalDeviceRequest** – Denne anmodning bruges til at initialisere tjenesten til regnskabsregistrering.

#### <a name="configuration"></a>Konfiguration

Konfigurationsfilen findes i mappen **Konfiguration** for udvidelsesprojektet. Formålet med filen er at aktivere indstillinger for regnskabsconnectoren, der skal konfigureres fra Commerce Headquarters. Filformatet er tilpasset kravene til konfiguration af regnskabsintegration. Følgende indstillinger tilføjes:

- **Slutpunktadresse** – URL-adressen for tjenesten til regnskabsregistrering.
- **Timeout** – Den tid i millisekunder, som driveren vil vente på et svar fra tjenesten til regnskabsregistrering.
