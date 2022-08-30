---
title: Retningslinjer for installation af eksempel på integration af bonprinter for Polen (ældre)
description: Denne artikel indeholder retningslinjer for implementering af eksempel på bonprinter for Polen fra Microsoft Dynamics 365 Commerce Retail SDK (Software Development Kit).
author: EvgenyPopovMBS
ms.date: 08/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-03-01
ms.openlocfilehash: 178301e6d8e5f87376ed893e4bf5f966260cad62
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336669"
---
# <a name="deployment-guidelines-for-the-fiscal-printer-integration-sample-for-poland-legacy"></a>Retningslinjer for installation af eksempel på integration af bonprinter for Polen (ældre)

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

> [!IMPORTANT]
> Du skal kun følge retningslinjerne i denne artikel, hvis du bruger Microsoft Dynamics 365 Commerce-version 10.0.28 eller tidligere. Pr. Commerce-version 10.0.29 er eksempel på integration af regnskabsprinter for Polen tilgængelig i Commerce Software Development Kit (SDK). Du kan finde flere oplysninger i [Konfigurere kanalkomponenter](./emea-pol-fpi-sample.md#configure-channel-components).

Denne artikel indeholder retningslinjer for implementering af eksempel på integration af bonprinter for Polen fra Dynamics 365 Commerce Retail SDK på en virtuel maskine (VM) til udviklere i Microsoft Dynamics Lifecycle Services (LCS). Du kan finde flere oplysninger om regnskabsintegrationseksemplet i [Eksempel på regnskabsbonprinter for Polen](emea-pol-fpi-sample.md). 

Eksemplet på regnskabsintegration for Polen er en del af Retail SDK. Du kan finde oplysninger om, hvordan du installerer og bruger SDK, i [Arkitektur for udviklingsværktøjskasse (SDK) til Retail](../dev-itpro/retail-sdk/retail-sdk-overview.md). Dette eksempel består af udvidelser til Commerce Runtime (CRT) og Hardwarestation. Hvis du vil køre dette eksempel, skal du redigere og bygge CRT og Hardwarestationsprojekter. Det anbefales, at du bruger en ikke-ændret Retail SDK til at foretage de ændringer, der er beskrevet i denne artikel. Det anbefales også, at du bruger et kildekontrolsystem som f.eks. Azure DevOps, hvor ingen filer er ændret endnu.

## <a name="development-environment"></a>Udviklingsmiljø

Følg disse trin for at konfigurere et udviklingsmiljø, så du kan teste og udvide eksemplet.

### <a name="commerce-runtime-extension-components"></a>Komponenter til Commerce Runtime-udvidelse

CRT-udvidelseskomponenterne er inkluderet i Retail SDK. Du kan fuldføre følgende procedurer ved at åbne løsningen **CommerceRuntimeSamples.sln** under **RetailSdk\\SampleExtensions\\CommerceRuntime**.

1. Find projektet **Runtime.Extensions.DocumentProvider.PosnetSample**, og opbyg det.
2. I mappen **Runtime.Extensions.DocumentProvider.PosnetSample\\bin\\Debug** kan du finde assemblyfilen **Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample.dll**.
3. Kopiér assembly-filen til CRT-udvidelsesmappen:

    - **Commerce Scale Unit:** Kopiér filen til mappen **\\bin\\ext** under IIS-webstedet (Internet Information Services) for Commerce Scale Unit.
    - **Lokal CRT på Modern POS:** Kopiér filen til mappen **\\ext** under den lokale CRT Client Broker-placering.

4. Find konfigurationsfilen til CRT-udvidelse:

    - **Commerce Scale Unit:** Filen kaldes **commerceruntime.ext.config**, og den findes i mappen **bin\\ext** under placeringen af webstedet IIS Commerce Scale Unit.
    - **Lokal CRT på Modern POS:** Filen hedder **CommerceRuntime.MPOSOffline.Ext.config**, og den findes under den lokale placering af CRT Client Broker.

5. Registrer CRT-ændringen i konfigurationsfilen til udvidelsen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample" />
    ```

6. Genstart Commerce-tjenesten:

    - **Commerce Scale Unit:** Genstart webstedet for Commerce-tjenesten fra IIS Manager.
    - **Client Broker:** Afslut processen **dllhost.exe** i Jobliste, og genstart derefter Modern POS.

### <a name="hardware-station-extension-components"></a>Komponenter til udvidelse af Hardwarestation

Hardwarestation-udvidelseskomponenterne er inkluderet i Retail SDK. Du kan fuldføre følgende procedurer ved at åbne løsningen **HardwareStationSamples.sln** under **RetailSdk\\SampleExtensions\\HardwareStation**.

1. Find projektet **HardwareStation.Extension.PosnetThermalFVFiscalPrinterSample**, og opbyg det.
2. I mappen **Extension.Posnet.ThermalFVFiscalPrinterSample\\bin\\Debug** kan du finde assemblyfilen **Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample.dll**.
3. Kopiér assembly-filen til en implementeret hardwarestationsmaskine:

    - **Ekstern hardwarestation:** Kopiér filen til mappen **bin** under placeringen af IIS-webstedet for Hardwarestation. Kopiér printerdriverbibliotekerne (**libposcmbth.dll**, **libcmbth\_serial.dll** og **cmbth\_pl.lng**).

4. Find konfigurationsfilen til hardwarestationens udvidelser. Filen hedder **HardwareStation.Extension.config**:

    - **Ekstern hardwarestation:** Filen ligger under placeringen af IIS-webstedet for Hardwarestation.

5. Føj følgende linje til sektionen **komposition** i konfigurationsfilen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample" />
    ```

6. Genstart tjenesten Hardwarestation:

    - **Ekstern hardwarestation:** Genstart webstedet Hardwarestation fra IIS Manager.

## <a name="production-environment"></a>Produktionsmiljø

Den foregående procedure aktiverer de udvidelser, der er komponenter i eksemplet til regnskabsintegrationstjenesten. Derudover skal du følge disse trin for at oprette installerbare pakker, der indeholder Commerce-komponenter, og for at anvende disse pakker i et produktionsmiljø.

1. Foretag følgende ændringer i pakkekonfigurationsfilerne under mappen **RetailSdk\\Assets**:

    - I konfigurationsfilerne **commerceruntime.ext.config** og **CommerceRuntime.MPOSOffline.Ext.config** skal du føje følgende linje til afsnittet **komposition**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample" />
        ```

    - Føj følgende linje til sektionen **komposition** i konfigurationsfilen **HardwareStation.Extension.config**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample" />
        ```

1. Foretag følgende ændringer i konfigurationsfilen til **Customization.settings**-pakkeindstillinger under mappen **BuildTools**:

    - Tilføj følgende linje for at inkludere CRT-udvidelsen i installationspakkerne.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample.dll"/>
        ```

    - Tilføj følgende linjer for at inkludere Hardwarestation-udvidelsen i installationspakkerne.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample.dll"/>
        ```

1. Start MSBuild-kommandoprompten for Visual Studio-hjælpeværktøjet, og kør **msbuild** under Retail SDK-mappen for at oprette installationspakkerne.
1. Anvend pakkerne via LCS eller manuelt. Du kan finde flere oplysninger under [Oprette installerbare pakker](../dev-itpro/retail-sdk/retail-sdk-packaging.md).

## <a name="design-of-extensions"></a>Design af udvidelser

Bonprinterintegrationens eksempel til Polen er baseret på [funktionaliteten af regnskabsintegration](fiscal-integration-for-retail-channel.md). Du kan finde flere oplysninger om designet af løsningen til regnskabsintegration i [Oversigt over eksempeldesign til regnskabsintegration](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

### <a name="commerce-runtime-extension-design"></a>Design af Commerce Runtime-udvidelse

Formålet med udvidelsen, som er en udbyder af regnskabsdokumenter, er at generere printerspecifikke dokumenter og håndtere svar fra bonprinteren.

Udvidelsen CRT er **Runtime.Extensions.DocumentProvider.PosnetSample**. Denne udvidelse genererer et sæt printerspecifikke kommandoer i JSON-format (JavaScript Object Notation), der er defineret af POSNET-specifikation 19-3678.

Du kan finde flere oplysninger om designet af løsningen til regnskabsintegration i [Regnskabsregistreringsprocessen og eksempler på regnskabsintegration for regnskabsenheder og -tjenester](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

#### <a name="request-handler"></a>Anmodningshandler

Anmodningshandleren **DocumentProviderPosnetProtocol** er indgangspunktet for anmodningen om at generere dokumenter fra bonprinteren.

Denne handler er nedarvet fra brugergrænsefladen i **INamedRequestHandler**. Metoden **HandlerName** er ansvarlig for at returnere navnet på handleren. Navnet på handleren skal svare til navnet på connector-dokumentudbyderen, der er angivet i Commerce Headquarters.

Connectoren understøtter følgende anmodninger:

- **GetFiscalDocumentDocumentProviderRequest** – Denne anmodning indeholder oplysninger om, hvilket dokument der skal genereres. Den returnerer et printerspecifikt dokument, der skal registreres i bonprinteren.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Denne anmodning returnerer listen over hændelser, der skal abonneres på. Aktuelt understøttes følgende hændelser: salg, udskrivning af X-rapport og udskrivning af Z-rapport.

#### <a name="configuration"></a>Konfiguration

Konfigurationsfilen findes i mappen **Konfiguration** for udvidelsesprojektet. Formålet med filen er at aktivere indstillinger for dokumentudbyderen, der skal konfigureres fra Commerce Headquarters. Filformatet er tilpasset kravene til konfiguration af regnskabsintegration. Følgende indstillinger tilføjes:

- Tilknytning af momssatser
- Tilknytning af betalingsmiddeltype
- Bankindbetalingstype

### <a name="hardware-station-extension-design"></a>Design af hardwarestationsudvidelse

Formålet med den forlængelse, der er en regnskabsmæssig connector, er at kommunikere med bonprinteren.

Udvidelsen til Hardwarestation er **HardwareStation.Extension.PosnetThermalFVFiscalPrinterSample**. Denne udvidelse kalder POSNET-driverens funktioner for at sende kommandoer, som CRT-udvidelsen genererer, til bonprinteren. Den håndterer også enhedsfejl.

#### <a name="request-handler"></a>Anmodningshandler

Anmodningshandleren **FiscalPrinterHandler** er indgangspunktet for håndtering af anmodningen til den eksterne regnskabsenhed.

Denne handler er nedarvet fra brugergrænsefladen i **INamedRequestHandler**. Metoden **HandlerName** er ansvarlig for at returnere navnet på handleren. Navnet på handleren skal svare til navnet på den regnskabsconnector, der er angivet i Commerce Headquarters.

Connectoren understøtter følgende anmodninger:

- **SubmitDocumentFiscalDeviceRequest** – Denne anmodning sender dokumenter til printere og returnerer svar fra bonprinteren.
- **IsReadyFiscalDeviceRequest** – Denne anmodning bruges til tilstandskontrol af enheden.
- **InitializeFiscalDeviceRequest** – Denne anmodning bruges til at initialisere printeren.

#### <a name="configuration"></a>Konfiguration

Konfigurationsfilen findes i mappen **Konfiguration** for udvidelsesprojektet. Formålet med filen er at aktivere indstillinger for connectoren, der skal konfigureres fra Commerce Headquarters. Filformatet er tilpasset kravene til konfiguration af regnskabsintegration. Følgende indstillinger tilføjes:

- **Forbindelsesstreng** – En streng, der beskriver detaljerne om forbindelsen til enheden i et format, som driveren understøtter. Yderligere oplysninger finder du i dokumentationen til POSNET-driveren.
- **Dato- og tidssynkronisering** – En værdi, der angiver, om datoen og klokkeslættet for printeren skal synkroniseres med den tilknyttede hardwarestation.
- **Timeout for enhed** – Den tid i millisekunder, som driveren vil vente på et svar fra enheden. Yderligere oplysninger finder du i dokumentationen til POSNET-driveren.
