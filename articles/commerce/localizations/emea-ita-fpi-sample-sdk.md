---
title: Retningslinjer for installation af eksempel på integration af bonprinter for Italien (ældre)
description: Dette emne indeholder retningslinjer for implementering af eksempel på bonprinter for Italien fra Microsoft Dynamics 365 Commerce Retail SDK (Software Development Kit).
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: a7b5f4f042aa5457ff33e9762f0902c5c72f5921
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944834"
---
# <a name="deployment-guidelines-for-the-fiscal-printer-integration-sample-for-italy-legacy"></a>Retningslinjer for installation af eksempel på integration af bonprinter for Italien (ældre)

[!include[banner](../includes/banner.md)]

Dette emne indeholder retningslinjer for implementering af eksempel på integration af bonprinter for Italien fra Microsoft Dynamics 365 Commerce Retail SDK (Software Development Kit) på en virtuel maskine (VM) til udviklere i Microsoft Dynamics Lifecycle Services (LCS). Du kan finde flere oplysninger om regnskabsintegrationseksemplet i [Eksempel på integration af bonprinter for Italien](emea-ita-fpi-sample.md). 

Eksemplet på regnskabsintegration for Italien er en del af Retail SDK. Du kan finde oplysninger om, hvordan du installerer og bruger SDK, i [Arkitektur for udviklingsværktøjskasse (SDK) til Retail](../dev-itpro/retail-sdk/retail-sdk-overview.md). Dette eksempel består af udvidelser til Commerce Runtime (CRT) og Hardwarestation. Hvis du vil køre dette eksempel, skal du redigere og bygge CRT og Hardwarestationsprojekter. Det anbefales, at du bruger en ikke-ændret Retail SDK til at foretage de ændringer, der er beskrevet i dette emne. Det anbefales også, at du bruger et kildekontrolsystem som f.eks. Azure DevOps, hvor ingen filer er ændret endnu.

## <a name="development-environment"></a>Udviklingsmiljø

Følg disse trin for at konfigurere et udviklingsmiljø, så du kan teste og udvide eksemplet.

### <a name="commerce-runtime-extension-components"></a>Komponenter til Commerce Runtime-udvidelse

CRT-udvidelseskomponenterne er inkluderet i Retail SDK. Du kan fuldføre følgende procedurer ved at åbne løsningen **CommerceRuntimeSamples.sln** under **RetailSdk\\SampleExtensions\\CommerceRuntime**.

1. Find projektet **Runtime.Extensions.DocumentProvider.EpsonFP90IIISample**, og opbyg det.
2. I mappen **Runtime.Extensions.DocumentProvider.EpsonFP90IIISample\\bin\\Debug** kan du finde assemblyfilen **Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.dll**.
3. Kopiér assembly-filen til CRT-udvidelsesmappen:

    - **Commerce Scale Unit:** Kopiér filen til mappen **\\bin\\ext** under IIS-webstedet (Internet Information Services) for Commerce Scale Unit.
    - **Lokal CRT på Modern POS:** Kopiér filen til mappen **\\ext** under den lokale CRT Client Broker-placering.

4. Find konfigurationsfilen til CRT-udvidelse:

    - **Commerce Scale Unit:** Filen kaldes **commerceruntime.ext.config**, og den findes i mappen **bin\\ext** under placeringen af webstedet IIS Commerce Scale Unit.
    - **Lokal CRT på Modern POS:** Filen hedder **CommerceRuntime.MPOSOffline.Ext.config**, og den findes under den lokale placering af CRT Client Broker.

5. Registrer CRT-ændringen i konfigurationsfilen til udvidelsen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample" />
    ```

6. Genstart Commerce Scale Unit:

    - **Commerce Scale Unit:** Genstart webstedet Commerce Scale Unit fra IIS Manager.
    - **Client Broker:** Afslut processen **dllhost.exe** i Jobliste, og genstart derefter Modern POS.

### <a name="hardware-station-extension-components"></a>Komponenter til udvidelse af Hardwarestation

Hardwarestation-udvidelseskomponenterne er inkluderet i Retail SDK. Du kan fuldføre følgende procedurer ved at åbne løsningen **HardwareStationSamples.sln** under **RetailSdk\\SampleExtensions\\HardwareStation**.

1. Find projektet **HardwareStation.Extensions.EpsonFP90IIIFiscalDeviceSample**, og opbyg det.
2. I mappen **Extensions.EpsonFP90IIIFiscalDeviceSample\\bin\\Debug** kan du finde assemblyfilen **Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample.dll**.
3. Kopiér assembly-filen til en implementeret hardwarestationsmaskine:

    - **Ekstern hardwarestation:** Kopiér filen til mappen **bin** under placeringen af IIS-webstedet for Hardwarestation.
    - **Lokal hardwarestation:** Kopiér filen til Client Broker-placeringen for Modern POS.

4. Find konfigurationsfilen til hardwarestationens udvidelser. Filen hedder **HardwareStation.Extension.config**:

    - **Ekstern hardwarestation:** Filen ligger under placeringen af IIS-webstedet for Hardwarestation.
    - **Lokal hardwarestation:** Filen ligger under Client Broker-placeringen for Modern POS.

5. Føj følgende sektion til sektionen **komposition** i konfigurationsfilen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample" />
    ```

6. Genstart tjenesten Hardwarestation:

    - **Ekstern hardwarestation:** Genstart webstedet Hardwarestation fra IIS Manager.
    - **Lokal hardwarestation:** Afslut processen **dllhost.exe** i Jobliste, og genstart derefter Modern POS.

## <a name="production-environment"></a>Produktionsmiljø

Følg disse trin for at oprette installerbare pakker, der indeholder Commerce-komponenter, og for at anvende disse pakker i et produktionsmiljø.

1. Udfør de trin, der er beskrevet i afsnittet [Udviklingsmiljø](#development-environment) tidligere i dette emne.
2. Foretag følgende ændringer i pakkekonfigurationsfilerne under mappen **RetailSdk\\Assets**:

    - I konfigurationsfilerne **commerceruntime.ext.config** og **CommerceRuntime.MPOSOffline.Ext.config** skal du føje følgende linje til afsnittet **komposition**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample" />
        ```

    - Føj følgende linje til sektionen **komposition** i konfigurationsfilen **HardwareStation.Extension.config**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample" />
        ```

3. Foretag følgende ændringer i konfigurationsfilen til **Customization.settings**-pakkeindstillinger under mappen **BuildTools**:

    - Tilføj følgende linje for at inkludere CRT-udvidelsen i installationspakkerne.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.dll"/>
        ```

    - Tilføj følgende linjer for at inkludere Hardwarestation-udvidelsen i installationspakkerne.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample.dll"/>
        ```

4. Start MSBuild-kommandoprompten for Visual Studio-hjælpeværktøjet, og kør derefter **msbuild** under Retail SDK-mappen for at oprette installationspakkerne.
5. Anvend pakkerne via LCS eller manuelt. Du kan finde flere oplysninger under [Oprette installerbare pakker](../dev-itpro/retail-sdk/retail-sdk-packaging.md).

## <a name="design-of-extensions"></a>Design af udvidelser

### <a name="commerce-runtime-extension-design"></a>Design af Commerce Runtime-udvidelse

Formålet med udvidelsen, som er en udbyder af regnskabsdokumenter, er at generere printerspecifikke dokumenter og håndtere svar fra bonprinteren.

Udvidelsen CRT er **Runtime.Extensions.DocumentProvider.EpsonFP90IIISample**.

Du kan finde flere oplysninger om designet af løsningen til regnskabsintegration i [Regnskabsregistreringsprocessen og eksempler på regnskabsintegration for regnskabsenheder](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices).

#### <a name="request-handler"></a>Anmodningshandler

Anmodningshandleren **DocumentProviderEpsonFP90III** er indganspunktet for anmodningen om at generere dokumenter fra bonprinteren.

Denne handler er nedarvet fra brugergrænsefladen i **INamedRequestHandler**. Metoden **HandlerName** er ansvarlig for at returnere navnet på handleren. Navnet på handleren skal svare til navnet på connector-dokumentudbyderen, der er angivet i Commerce Headquarters.

Connectoren understøtter følgende anmodninger:

- **GetFiscalDocumentDocumentProviderRequest** – Denne anmodning indeholder oplysninger om, hvilket dokument der skal genereres. Den returnerer et printerspecifikt dokument, der skal registreres i bonprinteren.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Denne anmodning returnerer listen over hændelser, der skal abonneres på. Aktuelt understøttes følgende hændelser: salg, udskrivning af X-rapport og udskrivning af Z-rapport.

#### <a name="configuration"></a>Konfiguration

Konfigurationsfilen findes i mappen **Konfiguration** for udvidelsesprojektet. Formålet med filen er at aktivere indstillinger for dokumentudbyderen, der skal konfigureres fra Commerce Headquarters. Filformatet er tilpasset kravene til konfiguration af regnskabsintegration. Følgende indstillinger tilføjes:

- Tilknytning af momskoder
- Tilknytning af momssatser
- Tilknytning af betalingsmiddeltype
- Stregkodetype for kvitteringsnummer
- Bankindbetalingstype

### <a name="hardware-station-extension-design"></a>Design af hardwarestationsudvidelse

Formålet med den forlængelse, der er en regnskabsmæssig connector, er at kommunikere med bonprinteren.

Udvidelsen til Hardwarestation er **HardwareStation.Extension.EpsonFP90IIIFiscalDeviceSample**. Denne udvidelse bruger HTTP-protokollen til at sende dokumenter, som CRT-udvidelsen genererer til bonprinteren. Den håndterer også de svar, der er modtaget fra bonprinteren.

#### <a name="request-handler"></a>Anmodningshandler

Anmodningshandleren **EpsonFP90IIISample** er indgangspunktet for håndtering af anmodninger til den eksterne regnskabsenhed.

Denne handler er nedarvet fra brugergrænsefladen i **INamedRequestHandler**. Metoden **HandlerName** er ansvarlig for at returnere navnet på handleren. Navnet på handleren skal svare til navnet på den regnskabsconnector, der er angivet i Commerce Headquarters.

Connectoren understøtter følgende anmodninger:

- **SubmitDocumentFiscalDeviceRequest** – Denne anmodning sender dokumenter til printere og returnerer svar fra bonprinteren.
- **IsReadyFiscalDeviceRequest** – Denne anmodning bruges til tilstandskontrol af enheden.
- **InitializeFiscalDeviceRequest** – Denne anmodning bruges til at initialisere printeren.

#### <a name="configuration"></a>Konfiguration

Konfigurationsfilen findes i mappen **Konfiguration** for udvidelsesprojektet. Formålet med filen er at aktivere indstillinger for connectoren, der skal konfigureres fra Commerce Headquarters. Filformatet er tilpasset kravene til konfiguration af regnskabsintegration. Følgende indstillinger tilføjes:

- **Slutpunktadresse** – Printerens URL-adresse.
- **Dato- og tidssynkronisering** – En værdi, der angiver, om datoen og klokkeslættet for printeren skal synkroniseres med den tilknyttede hardwarestation.
