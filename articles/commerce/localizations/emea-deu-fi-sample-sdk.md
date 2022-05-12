---
title: Retningslinjer for installation af eksempel på integration af regnskabsregistreringsservice i Tyskland (ældre)
description: Dette emne indeholder retningslinjer for implementering af eksempel på regnskabsintegration for Tyskland fra Microsoft Dynamics 365 Commerce Retail SDK (Software Development Kit).
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: c49e6cedcce1d336486e9fbcc0620bcdf455cc9d
ms.sourcegitcommit: 7faf82fa7ce269c0201abb8473af861ef7ce00bf
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/19/2022
ms.locfileid: "8614118"
---
# <a name="deployment-guidelines-for-the-fiscal-registration-service-integration-sample-for-germany-legacy"></a>Retningslinjer for installation af eksempel på integration af regnskabsregistreringsservice i Tyskland (ældre)

[!include [banner](../includes/banner.md)]

Dette emne indeholder retningslinjer for implementering af eksempel på integration af regnskabsregistreringstjeneste for Tyskland fra Microsoft Dynamics 365 Commerce Retail SDK (Software Development Kit) på en virtuel maskine (VM) til udviklere i Microsoft Dynamics Lifecycle Services (LCS). Du kan finde flere oplysninger om regnskabsintegrationseksemplet i [Eksempel på regnskabsintegrationsservice for Tyskland](emea-deu-fi-sample.md). 

Eksemplet på regnskabsintegration for Tyskland er en del af Retail SDK. Du kan finde oplysninger om, hvordan du installerer og bruger SDK, i [Arkitektur for udviklingsværktøjskasse (SDK) til Retail](../dev-itpro/retail-sdk/retail-sdk-overview.md). Dette eksempel består af udvidelser til Commerce Runtime (CRT) og Hardwarestation. Hvis du vil køre dette eksempel, skal du redigere og bygge CRT og Hardwarestationsprojekter. Det anbefales, at du bruger en ikke-ændret Retail SDK til at foretage de ændringer, der er beskrevet i dette emne. Det anbefales også, at du bruger et kildekontrolsystem som f.eks. Azure DevOps, hvor ingen filer er ændret endnu.

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
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsGermany" />
    ```

### <a name="enable-fiscal-connector-extensions"></a>Aktivere regnskabsconnectorudvidelser

Du kan aktivere regnskabsconnectorudvidelser på [hardwarestationen](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station) eller [POS-kasseapparatet](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-or-service-in-the-local-network).

#### <a name="enable-hardware-station-extensions"></a>Aktivere hardwarestationsudvidelser

Udvidelseskomponenterne for hardwarestationen er inkluderet i eksemplerne til Hardwarestation. Du kan fuldføre følgende procedurer ved at åbne løsningen **HardwareStationSamples.sln** under **RetailSdk\\SampleExtensions\\HardwareStation**.

##### <a name="efrsample-component"></a>Komponenten EFRSample

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

#### <a name="enable-pos-extensions"></a>Aktivere POS-udvidelser

Eksemplet på POS-udvidelse findes i mappen **src\\FiscalIntegration\\PosFiscalConnectorSample** i lageret til [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions/).

Udfør følgende trin for at bruge POS-udvidelseseksemplet i den ældre SDK.

1. Kopiér mappen **Pos.Extension** til POS-mappen **Extensions** i det ældre SDK (f.eks. `C:\RetailSDK\src\POS\Extensions`).
1. Omdøb kopien af **Pos.Extension**-mappen **PosFiscalConnector**.
1. Fjern følgende mapper og filer fra mappen **PosFiscalConnector**:

    - bin
    - DataService
    - devDependencies
    - Biblioteker
    - obj
    - Contoso.PosFiscalConnectorSample.Pos.csproj
    - RetailServerEdmxModel.g.xml
    - tsconfig.json

1. Åbn løsningen **CloudPos.sln** eller **ModernPos.sln**.
1. I projektet **Pos.Extensions** skal du medtage mappen **PosFiscalConnector**.
1. Åbn filen **extensions.json**, og tilføj udvidelsen **PosFiscalConnector**.
1. Opbyg SDK.

### <a name="production-environment"></a>Produktionsmiljø

Den foregående procedure aktiverer de udvidelser, der er komponenter i eksemplet til regnskabsintegrationstjenesten. Derudover skal du følge disse trin for at oprette installerbare pakker, der indeholder Commerce-komponenter, og for at anvende disse pakker i et produktionsmiljø.

1. Foretag følgende ændringer i pakkekonfigurationsfilerne under mappen **RetailSdk\\Assets**:

    - I konfigurationsfilerne **commerceruntime.ext.config** og **CommerceRuntime.MPOSOffline.Ext.config** skal du føje følgende linjer til afsnittet **komposition**.

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsGermany" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        ```

    - Føj følgende linjer til sektionen **komposition** i konfigurationsfilen **HardwareStation.Extension.config**.

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

    - Tilføj følgende linjer for at inkludere Hardwarestation-udvidelser i installationspakkerne.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EFRSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

3. Start MSBuild-kommandoprompten for Visual Studio-hjælpeværktøjet, og kør **msbuild** under Retail SDK-mappen for at oprette installationspakkerne.
4. Anvend pakkerne via LCS eller manuelt. Du kan finde flere oplysninger under [Oprette installerbare pakker](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
5. Udfør alle de nødvendige opsætningsopgaver, der er beskrevet i [Konfigurere Commerce for Tyskland](emea-deu-fi-sample.md#set-up-commerce-for-germany).

## <a name="design-of-extensions"></a>Design af udvidelser

Regnskabsintegrationstjenestens eksempel til Tyskland er baseret på [funktionaliteten af regnskabsintegration](fiscal-integration-for-retail-channel.md). Du kan finde flere oplysninger om designet af løsningen til regnskabsintegration i [Oversigt over eksempeldesign til regnskabsintegration](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

### <a name="commerce-runtime-extension-design"></a>Design af Commerce Runtime-udvidelse

Formålet med udvidelsen, som er en udbyder af regnskabsdokumenter, er at generere servicespecifikke dokumenter og håndtere svar fra tjenesten til regnskabsregistrering.

Udvidelsen CRT er **Runtime.Extensions.DocumentProvider.EFRSample**. Du kan finde flere oplysninger om designet af løsningen til regnskabsintegration i [Oversigt over regnskabsintegration for Commerce-kanaler](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

#### <a name="request-handler"></a>Anmodningshandler

Der er en enkelt anmodningshandler til dokumentudbyder, **DocumentProviderEFRFiscalDEU**. Den bruges til at generere regnskabsdokumenter til regnskabsregistreringstjenesten. Den er nedarvet fra brugergrænsefladen i **INamedRequestHandler**. Metoden **HandlerName** er ansvarlig for at returnere navnet på handleren. Navnet på handleren skal svare til navnet på connector-dokumentudbyderen, der er angivet i Commerce Headquarters.

Connectoren understøtter følgende anmodninger:

- **GetFiscalDocumentDocumentProviderRequest** – Denne anmodning indeholder oplysninger om, hvilket dokument der skal genereres. Den returnerer et servicespecifikt dokument, der skal registreres i tjenesten til regnskabsregistrering.
- **GetFiscalTransactionExtendedDataDocumentProviderRequest** – Denne anmodning returnerer svaret sammen med udvidede data.

#### <a name="configuration"></a>Konfiguration

Konfigurationsfilen **DocumentProviderFiscalEFRSampleGermany** findes i mappen **Konfiguration** for udvidelsesprojektet. Formålet med filen er at aktivere indstillinger for dokumentudbyderen, der skal konfigureres fra Commerce Headquarters. Filformatet er tilpasset kravene til konfiguration af regnskabsintegration.

Følgende indstillinger tilføjes:

- **Tilknytning af momssatser** – Tilknytning af momsprocentværdier, der er konfigureret for momskoderne til værdier af attributten **TaxG** (momsgruppe) i anmodninger, der sendes til regnskabstjenesten.
- **Momsgruppe for gavekort og indbetalinger** – Værdien af **TaxG**-attributten i anmodninger, der sendes til regnskabstjenesten, baseret på operationer, der involverer gavekort eller indbetalinger.
- **Tilknytning af betalingsmiddeltype** – Tilknytning af betalingsmåder til værdier af attributten **PayG** (betalingsgruppe) i anmodninger, der sendes til regnskabstjenesten.
- **Momsgruppe for momsfritagelse** – Værdien af **TaxG**-attributten i anmodninger, der sendes til regnskabstjenesten, baseret på operationer, der er fritaget for momsforpligtelser.
- **Medtag debitordata** – Hvis denne parameter er aktiveret, indeholder anmodninger til regnskabstjenesten debitoroplysninger, f.eks. navne og adresser, i tilfælde, hvor en debitor føjes til en transaktion.

### <a name="hardware-station-extension-design"></a>Design af hardwarestationsudvidelse

Formålet med den forlængelse, der er en regnskabsmæssig connector, er at kommunikere med tjenesten til regnskabsregistrering.

Udvidelsen til Hardwarestation er **HardwareStation.Extension.EFRSample**. Den bruger HTTP-protokollen til at sende dokumenter, som CRT-udvidelsen genererer til regnskabsregistreringstjenesten. Den håndterer også de svar, der er modtaget fra tjenesten til regnskabsregistrering.

#### <a name="request-handler"></a>Anmodningshandler

Anmodningshandleren **EFRHandler** er indgangspunktet for håndtering af anmodninger til tjenesten til regnskabsregistrering. Denne handler er nedarvet fra brugergrænsefladen i **INamedRequestHandler**. Metoden **HandlerName** er ansvarlig for at returnere navnet på handleren. Navnet på handleren skal svare til navnet på den regnskabsconnector, der er angivet i Commerce Headquarters.

Connectoren understøtter følgende anmodninger:

- **SubmitDocumentFiscalDeviceRequest** – Denne anmodning sender dokumenter til tjenesten til regnskabsregistrering og returnerer et svar fra den.
- **IsReadyFiscalDeviceRequest** – Denne anmodning bruges til tilstandskontrol af tjenesten til regnskabsregistrering.
- **InitializeFiscalDeviceRequest** – Denne anmodning bruges til at initialisere tjenesten til regnskabsregistrering.

#### <a name="configuration"></a>Konfiguration

Konfigurationsfilen findes i mappen **Konfiguration** for udvidelsesprojektet. Formålet med filen er at aktivere indstillinger for regnskabsconnectoren, der skal konfigureres fra Commerce Headquarters. Filformatet er tilpasset kravene til konfiguration af regnskabsintegration.

Følgende indstillinger tilføjes:

- **Slutpunktadresse** – URL-adressen for tjenesten til regnskabsregistrering.
- **Timeout** – Den tid i millisekunder (ms), som driveren vil vente på et svar fra tjenesten til regnskabsregistrering.
- **Vis beskeder om regnskabsregistrering** – Hvis denne parameter er aktiveret, vises beskeder fra regnskabstjenesten som brugermeddelelser i POS.

### <a name="pos-fiscal-connector-extension-design"></a>Design af udvidelsen POS-regnskabsconnector

Formålet med POS-regnskabsconnector-udvidelsen er at kommunikere med tjenesten til regnskabsregistrering fra POS. Den bruger HTTPS-protokollen til kommunikation.

#### <a name="fiscal-connector-factory"></a>Fabrik for regnskabsconnector

Fabrikken for regnskabsconnector knytter connectornavnet til implementeringen af regnskabsconnector og er placeret i filen **Pos.Extension\\Connectors\\FiscalConnectorFactory.ts**. Navnet på connectoren skal svare til navnet på den regnskabsconnector, der er angivet i Commerce-hovedkontoret.

#### <a name="efr-fiscal-connector"></a>EFR-regnskabsconnector

EFR-regnskabsconnectoren er placeret i filen **Pos.Extension\\Connectors\\Efr\\EfrFiscalConnector.ts**. Den implementerer brugergrænsefladen **IFiscalConnector**, der understøtter følgende anmodninger:

- **FiscalRegisterSubmitDocumentClientRequest** – Denne anmodning sender dokumenter til tjenesten for regnskabsregistrering og returnerer et svar fra den.
- **FiscalRegisterIsReadyClientRequest** – Denne anmodning bruges til tilstandskontrol af tjenesten til regnskabsregistrering.
- **FiscalRegisterInitializeClientRequest** – Denne anmodning bruges til at initialisere tjenesten til regnskabsregistrering.

#### <a name="configuration"></a>Konfiguration

Konfigurationsfilen findes i mappen **src\\FiscalIntegration\\Efr\\Configurations\\Connectors** i lageret [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Formålet med filen er at aktivere indstillinger for regnskabsconnectoren, der skal konfigureres fra Commerce Headquarters. Filformatet er tilpasset kravene til konfiguration af regnskabsintegration. Følgende indstillinger tilføjes:

- **Slutpunktadresse** – URL-adressen for tjenesten til regnskabsregistrering.
- **Timeout** – Den tid i millisekunder, som connectoren vil vente på et svar fra tjenesten til regnskabsregistrering.
