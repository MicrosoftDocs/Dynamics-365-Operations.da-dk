---
title: Retningslinjer for eksempel på integration af kontrolenhed for Sverige (ældre)
description: Denne artikel indeholder retningslinjer for implementering af eksempel på integration af kontrolenhed for Sverige fra Retail SDK
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: fcc35a2203641b24fe4edd2ab34f2e4d5db9bb53
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/23/2022
ms.locfileid: "9324291"
---
# <a name="deployment-guidelines-for-the-control-unit-integration-sample-for-sweden-legacy"></a>Retningslinjer for eksempel på integration af kontrolenhed for Sverige (ældre)

[!include [banner](../includes/banner.md)]

Denne artikel indeholder retningslinjer for implementering af eksempel på integration af kontrolenhed for Sverige fra Retail SDK (Software Development Kit) på en virtuel maskine (VM) til udviklere i Microsoft Dynamics Lifecycle Services (LCS). Du kan finde flere oplysninger om regnskabsintegrationseksemplet i [Eksempel på integration ad kontrolenhed for Sverige](emea-swe-fi-sample.md). 

Eksemplet på regnskabsintegration for Sverige er en del af Retail SDK. Du kan finde oplysninger om, hvordan du installerer og bruger SDK, i [Arkitektur for udviklingsværktøjskasse (SDK) til Retail](../dev-itpro/retail-sdk/retail-sdk-overview.md). Dette eksempel består af udvidelser til Commerce Runtime (CRT), Hardwarestation og POS. Hvis du vil køre dette eksempel, skal du redigere og bygge CRT, Hardwarestation og POS-projekter. Det anbefales, at du bruger en ikke-ændret Retail SDK til at foretage de ændringer, der er beskrevet i denne artikel. Det anbefales også, at du bruger et kildekontrolsystem som f.eks. Azure DevOps, hvor ingen filer er ændret endnu.

## <a name="development-environment"></a>Udviklingsmiljø

Følg disse trin for at konfigurere et udviklingsmiljø, så du kan teste og udvide eksemplet.

### <a name="enable-crt-extensions"></a>Aktivere CRT-udvidelser

CRT-udvidelseskomponenterne er inkluderet i CRT-eksemplerne. Du kan fuldføre følgende procedurer ved at åbne løsningen **CommerceRuntimeSamples.sln** under **RetailSdk\\SampleExtensions\\CommerceRuntime**.

#### <a name="documentprovidercleancashsample-component"></a>Komponenten DocumentProvider.CleanCashSample

1. Find projektet **Runtime.Extensions.DocumentProvider.CleanCashSample**, og opbyg det.
2. I mappen **Runtime.Extensions.DocumentProvider.CleanCashSample\\bin\\Debug** kan du finde assemblyfilen **Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll**.
3. Kopiér assembly-filen til CRT-udvidelsesmappen:

    - **Commerce Scale Unit:** Kopiér filen til mappen **\\bin\\ext** under IIS-webstedet (Internet Information Services) for Commerce Scale Unit.
    - **Lokal CRT på Modern POS:** Kopiér filen til mappen **\\ext** under den lokale CRT Client Broker-placering.

4. Find konfigurationsfilen til CRT-udvidelse:

    - **Commerce Scale Unit:** Filen kaldes **commerceruntime.ext.config**, og den findes i mappen **bin\\ext** under placeringen af webstedet IIS Commerce Scale Unit.
    - **Lokal CRT på Modern POS:** Filen hedder **CommerceRuntime.MPOSOffline.Ext.config**, og den findes under den lokale placering af CRT Client Broker.

5. Registrer CRT-ændringen i konfigurationsfilen til udvidelsen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    ```

#### <a name="extension-configuration-file"></a>Konfigurationsfil til udvidelse

1. Find konfigurationsfilen til CRT-udvidelse:

    - **Commerce Scale Unit:** Filen kaldes **commerceruntime.ext.config**, og den findes i mappen **bin\\ext** under placeringen af webstedet IIS Commerce Scale Unit.
    - **Lokal CRT på Modern POS:** Filen hedder **CommerceRuntime.MPOSOffline.Ext.config**, og den findes under den lokale placering af CRT Client Broker.

2. Registrer CRT-ændringen i konfigurationsfilen til udvidelsen.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

### <a name="enable-hardware-station-extensions"></a>Aktivere hardwarestationsudvidelser

Udvidelseskomponenterne for hardwarestationen er inkluderet i eksemplerne til Hardwarestation. Du kan fuldføre følgende procedurer ved at åbne løsningen **HardwareStationSamples.sln** under **RetailSdk\\SampleExtensions\\HardwareStation**.

#### <a name="cleancash-component"></a>CleanCash-komponent

1. Find projektet **HardwareStation.Extension.CleanCashSample**, og opbyg det.
2. I mappen **Extension.CleanCashSample\\bin\\Debug** kan du finde assemblyfilerne **Contoso.Commerce.HardwareStation.CleanCashSample.dll** og **Interop.CleanCash\_1\_1.dll**.
3. Kopiér assembly-filerne til mappen med udvidelser til Hardwarestation:

    - **Delt hardwarestation:** Kopiér filerne til mappen **bin** under placeringen af IIS-webstedet for Hardwarestation.
    - **Dedikeret hardwarestation på Modern POS:** Kopiér filerne til Client Broker-placeringen for Modern POS.

4. Find udvidelsens konfigurationsfil til hardwarestationens udvidelser. Filen hedder **HardwareStation.Extension.config**.

    - **Delt hardwarestation:** Filen ligger under placeringen af IIS-webstedet for Hardwarestation.
    - **Dedikeret hardwarestation på Modern POS:** Filen ligger under Client Broker-placeringen for Modern POS.

5. Føj følgende linje til sektionen **komposition** i konfigurationsfilen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
    ```

### <a name="enable-modern-pos-extension-components"></a>Aktivere komponenter for udvidelse af Modern POS

1. Åbn løsningen **ModernPOS.sln** under **RetailSdk\\POS**, og kontrollér, at den kan kompileres uden fejl. Derudover skal du sørge for, at du kan køre Modern POS fra Visual Studio ved hjælp af kommandoen **Kør**.

    > [!NOTE]
    > Modern POS må ikke tilpasses. Du skal aktivere User Account Control (UAC), og du skal afinstallere tidligere installerede forekomster af Modern POS efter behov.

2. Aktivér udvidelserne, der skal indlæses, ved at tilføje følgende linjer i filen **extensions.json**.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
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
2. Aktivér udvidelserne, der skal indlæses, ved at tilføje følgende linjer i filen **extensions.json**.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

    > [!NOTE]
    > Yderligere oplysninger og eksempler, der viser, hvordan du medtager kildekodemapper og aktiverer udvidelser, der skal indlæses, finder du i instruktionerne i readme.md-filen i projektet **Pos.Extensions**.

3. Genopbyg løsningen.
4. Kør løsningen ved at bruge kommandoen **Kør** og følge trinnene i Retail SDK-håndbogen.

## <a name="production-environment"></a>Produktionsmiljø

Den foregående procedure aktiverer de udvidelser, der er komponenter i eksemplet til integration af kontrolenhed. Derudover skal du følge disse trin for at oprette installerbare pakker, der indeholder Commerce-komponenter, og for at anvende disse pakker i et produktionsmiljø.

1. Foretag følgende ændringer i pakkekonfigurationsfilerne under mappen **RetailSdk\\Assets**:

    - I konfigurationsfilerne **commerceruntime.ext.config** og **CommerceRuntime.MPOSOffline.Ext.config** skal du føje følgende linjer til afsnittet **komposition**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
        ```

    - Føj følgende linje til sektionen **komposition** i konfigurationsfilen **HardwareStation.Extension.config**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
        ```

2. Foretag følgende ændringer i konfigurationsfilen til **Customization.settings**-pakkeindstillinger under mappen **BuildTools**:

    - Tilføj følgende linje for at inkludere CRT-udvidelserne i installationspakkerne.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll" />
        ```

    - Tilføj følgende linjer for at inkludere Hardwarestation-udvidelsen i installationspakkerne.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.CleanCashSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Interop.CleanCash_1_1.dll" />
        ```

3. Aktivér POS-udvidelsen ved at tilføje følgende linjer i filen **extensions.json** under mappen **RetailSDK\\POS\\Extensions**.

    ``` json
    {
        "extensionPackages": [
            {
            "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

4. Start MSBuild-kommandoprompten for Visual Studio-hjælpeværktøjet, og kør **msbuild** under Retail SDK-mappen for at oprette installationspakkerne.
5. Anvend pakkerne via LCS eller manuelt. Du kan finde flere oplysninger under [Oprette installerbare pakker](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
6. Udfør alle de nødvendige opsætningsopgaver, der er beskrevet i [Konfigurere integration med kontrolenheder](emea-swe-fi-sample.md#setting-up-the-integration-with-control-units).

## <a name="design-of-the-extensions"></a>Design af udvidelserne

### <a name="crt-extension-design"></a>Design af CRT-udvidelse

Formålet med udvidelsen, som er en udbyder af regnskabsdokumenter, er at generere servicespecifikke dokumenter og håndtere svar fra kontrolenheden.

Udvidelsen CRT er **Runtime.Extensions.DocumentProvider.CleanCashSample**.

Du kan finde flere oplysninger om designet af løsningen til regnskabsintegration i [Regnskabsregistreringsprocessen og eksempler på regnskabsintegration for regnskabsenheder og -tjenester](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

#### <a name="request-handler"></a>Anmodningshandler

Der er en enkelt **DocumentProviderCleanCash**-anmodningshandler til dokumentudbyder. Den bruges til at generere regnskabsdokumenter til kontrolenheden.

Denne handler er nedarvet fra brugergrænsefladen i **INamedRequestHandler**. Metoden **HandlerName** er ansvarlig for at returnere navnet på handleren. Navnet på handleren skal svare til navnet på connector-dokumentudbyderen, der er angivet i Commerce Headquarters.

Connectoren understøtter følgende anmodninger:

- **GetFiscalDocumentDocumentProviderRequest** – Denne anmodning indeholder oplysninger om, hvilket dokument der skal genereres. Den returnerer et servicespecifikt dokument, der skal registreres i kontrolenheden.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Denne anmodning returnerer listen over hændelser, der skal abonneres på. Salgshændelser og revisionshændelser understøttes i øjeblikket.

#### <a name="configuration"></a>Konfiguration

Konfigurationsfilen **DocumentProviderFiscalCleanCashSample** findes i mappen **Konfiguration** for udvidelsesprojektet. Formålet med filen er at aktivere indstillinger for dokumentudbyderen, der skal konfigureres fra Commerce Headquarters. Filformatet er tilpasset kravene til konfiguration af regnskabsintegration. Følgende indstillinger tilføjes:

- Tilknytning af momskoder

### <a name="hardware-station-extension-design"></a>Design af hardwarestationsudvidelse

Formålet med den forlængelse, der er en regnskabsmæssig connector, er at kommunikere med kontrolenheden.

Udvidelsen til Hardwarestation er **HardwareStation.Extension.CleanCashSample**. Den bruger HTTP-protokollen til at sende dokumenter, som CRT-udvidelsen genererer til kontrolenheden. Den håndterer også de svar, der er modtaget fra kontrolenheden.

#### <a name="request-handler"></a>Anmodningshandler

Anmodningshandleren **CleanCashHandler** er indgangspunktet for håndtering af anmodninger til kontrolenheden.

Denne handler er nedarvet fra brugergrænsefladen i **INamedRequestHandler**. Metoden **HandlerName** er ansvarlig for at returnere navnet på handleren. Navnet på handleren skal svare til navnet på den regnskabsconnector, der er angivet i Commerce Headquarters.

Connectoren understøtter følgende anmodninger:

- **SubmitDocumentFiscalDeviceRequest** – Denne anmodning sender dokumenter til kontrolenheden og returnerer et svar fra den.
- **IsReadyFiscalDeviceRequest** – Denne anmodning bruges til tilstandskontrol af kontrolenheden.
- **InitializeFiscalDeviceRequest** – Denne anmodning bruges til at initialisere kontrolenheden.

#### <a name="configuration"></a>Konfiguration

Konfigurationsfilen findes i mappen **Konfiguration** for udvidelsesprojektet. Formålet med filen er at aktivere indstillinger for regnskabsconnectoren, der skal konfigureres fra Commerce Headquarters. Filformatet er tilpasset kravene til konfiguration af regnskabsintegration. Følgende indstillinger tilføjes:

- **Forbindelsesstreng** – Forbindelsesindstillingerne for kontrolenheden.
- **Timeout** – Den tid i millisekunder, som driveren vil vente på et svar fra tjenesten til kontrolenheden.

## <a name="migrating-from-the-earlier-integration-sample"></a>Overføre fra det tidligere eksempel på integration

Hvis du bruger det tidligere [eksempel på POS-integration med kontrolenheder for Sverige](retail-sdk-control-unit-sample.md), skal du muligvis migrere fra den til det aktuelle integrationseksempel. Hvis du vil indtage ændringen og modtage opdateringer i tide til funktionerne for Sverige i fremtiden, kan du blive nødt til at opgradere, foretage mindre kode- og konfigurationsreguleringer i de udvidelser, du har oprettet, og gendanne løsningerne. Der kræves ingen større ændringer i den udvidelseslogik, du har oprettet. Det tidligere eksempel på integration og dine tilpasninger fortsætter med at fungere, hvis der ikke foretages ændringer fra din side. Du kan derfor planlægge, forberede og inddrage det i dit miljø.

### <a name="migration-process"></a>Overflytningsproces

Overflytningen fra det tidligere integrationseksempel til det aktuelle integrationseksempel for kontrolenheden skal baseres på begrebet trinvis opdatering. Det vil sige, at alle komponenterne i Commerce Headquarters og Commerce Scale Unit allerede skal opdateres, før du begynder at opdatere komponenterne til POS og Hardwarestation.

Hvis du vil forhindre en situation, hvor en hændelse eller transaktion signeres to gange (det vil sige, at den er signeret af både den tidligere udvidelse og den aktuelle), eller hvor en hændelse eller transaktion ikke kan signeres på grund af den manglende konfiguration, anbefales det, at du deaktiverer alle POS- og Hardwarestation-enheder, der bruger det tidligere eksempel, og derefter opdaterer dem samtidigt. Den samtidige opdatering kan f.eks. udføres på butiksbasis ved at opdatere butikkens funktionalitetsprofil og hardwarestationens hardwareprofil.

Overflytningsprocessen bør omfatte følgende trin.

1. Opdater komponenterne i Commerce Headquarters.
1. Opdater komponenterne i Commerce Scale Unit, og aktivér udvidelserne af det aktuelle eksempel.
1. Kontrollér, at alle offlinetransaktioner er synkroniseret fra offlineaktiverede MPOS-enheder.
1. Deaktiver alle enheder, der bruger komponenterne i det tidligere eksempel.
1. Udfør alle de nødvendige opsætningsopgaver, der er beskrevet i [Konfigurere integration med kontrolenheder](emea-swe-fi-sample.md#setting-up-the-integration-with-control-units).
1. Opdater komponenterne til POS og Hardwarestation, deaktiver de udvidelser, der findes i det tidligere eksempel, og aktivér udvidelserne for det aktuelle eksempel.

    > [!NOTE]
    > Afhængigt af miljøtypen finder du mere tekniske detaljer om overflytningsprocessen i afsnittet [Overflytning i et udviklingsmiljø](#migration-in-a-development-environment) eller afsnittet [Overflytning i et produktionsmiljø](#migration-in-a-production-environment) i denne artikel.

### <a name="migration-in-a-development-environment"></a>Overflytning i et udviklingsmiljø

#### <a name="update-crt"></a>Opdater CRT

1. Find projektet **Runtime.Extensions.DocumentProvider.CleanCashSample**, og opbyg det.
2. I mappen **Runtime.Extensions.DocumentProvider.CleanCashSample\\bin\\Debug** kan du finde assemblyfilen **Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll**.
3. Kopiér assembly-filen til CRT-udvidelsesmappen:

    - **Commerce Scale Unit:** Kopiér filen til mappen **\\bin\\ext** under IIS-webstedet for Commerce Scale Unit.
    - **Lokal CRT på Modern POS:** Kopiér filen til mappen **\\ext** under den lokale CRT Client Broker-placering.

4. Find konfigurationsfilen til CRT-udvidelse:

    - **Commerce Scale Unit:** Filen kaldes **CommerceRuntime.ext.config**, og den findes i mappen **bin\\ext** under placeringen af webstedet IIS Commerce Scale Unit.
    - **Lokal CRT på Modern POS:** Filen hedder **CommerceRuntime.MPOSOffline.Ext.config**, og den findes i mappen **bin\\ext** under den lokale placering af CRT Client Broker.

    > [!WARNING]
    > Du må **ikke** redigere filerne CommerceRuntime.config og CommerceRuntime.MPOSOffline.config. Disse filer er ikke beregnet til tilpasninger.

5. Find og fjern den tidligere CRT-udvidelse fra udvidelsens konfigurationsfil.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.FiscalRegisterReceiptSample" />
    ```

    > [!WARNING]
    > Udfør ikke dette trin, før du har opdateret alle POS-enheder, der fungerer med denne CRT-forekomst.

6. Registrer de aktuelle CRT-eksempeludvidelser i konfigurationsfilen til udvidelser ved at tilføje følgende linjer.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

#### <a name="update-hardware-station"></a>Opdatere Hardwarestation

1. Find projektet **HardwareStation.Extension.CleanCashSample**, og opbyg det.
2. I mappen **Extension.CleanCashSample\\bin\\Debug** kan du finde assemblyfilerne **Contoso.Commerce.HardwareStation.CleanCashSample.dll** og **Interop.CleanCash\_1\_1.dll**.
3. Kopiér assembly-filerne til mappen med udvidelser til Hardwarestation:

    - **Delt hardwarestation:** Kopiér filerne til mappen **bin** under placeringen af IIS-webstedet for Hardwarestation.
    - **Dedikeret hardwarestation på Modern POS:** Kopiér filerne til Client Broker-placeringen for Modern POS.

4. Find udvidelsens konfigurationsfil, **HardwareStation.Extension.config**:

    - **Ekstern hardwarestation:** Filen ligger under placeringen af IIS-webstedet for Hardwarestation.
    - **Lokal hardwarestation på Modern POS:** Filen ligger under Client Broker-placeringen for Modern POS.

    > [!WARNING]
    > Du må **ikke** redigere filerne CommerceRuntime.config og CommerceRuntime.MPOSOffline.config. Disse filer er ikke beregnet til tilpasninger.

5. Find og fjern den tidligere Hardwarestation-udvidelse fra udvidelsens konfigurationsfil.

    # <a name="retail-73-and-earlier"></a>[Retail 7.3 og tidligere](#tab/retail-7-3)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-731-and-later"></a>[Retail 7.3.1 og nyere](#tab/retail-7-3-1)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-100-and-later"></a>[Retail 10.0 og nyere](#tab/retail-10-0)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.FiscalRegisterSample" />
    ```
    ---

6. Føj følgende linje til sektionen **komposition** i konfigurationsfilen for udvidelsen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
    ```

#### <a name="update-modern-pos"></a>Opdatere Modern POS

1. Åbn løsningen **CloudPOS.sln** under **RetailSdk\\POS**.
2. Deaktiver den tidligere POS-udvidelse ved at fjerne følgende linjer fra **extensions.json**-filen.

    ``` json
    {
        "baseUrl": "FiscalRegisterSample"
    }
    ```

2. Aktivér det aktuelle eksempel på POS-udvidelse ved at tilføje følgende linjer i filen **extensions.json**.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

#### <a name="update-cloud-pos"></a>Opdatere Cloud POS

1. Åbn løsningen **ModernPOS.sln** under **RetailSdk\\POS**.
2. Deaktiver den tidligere POS-udvidelse ved at fjerne følgende linjer fra **extensions.json**-filen.

    ``` json
    {
        "baseUrl": "FiscalRegisterSample"
    }
    ```

2. Aktivér det aktuelle eksempel på POS-udvidelse ved at tilføje følgende linjer i filen **extensions.json**.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

### <a name="migration-in-a-production-environment"></a>Overflytning i et produktionsmiljø

#### <a name="update-crt"></a>Opdater CRT

1. Fjern den tidligere CRT-udvidelse fra konfigurationsfilerne **CommerceRuntime.ext.config** og **CommerceRuntime.MPOSOffline.Ext.config** under mappen **RetailSdk\\Assets**.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.FiscalRegisterReceiptSample" />
    ```

    > [!WARNING]
    > Udfør ikke dette trin, før du har opdateret alle POS-enheder, der fungerer med denne CRT-forekomst.

2. Aktivér det aktuelle eksempel på CRT-udvidelser ved at foretage følgende ændringer i konfigurationsfilerne **CommerceRuntime.ext.config** og **CommerceRuntime.MPOSOffline.Ext.config** under mappen **RetailSdk\\Assets**.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

3. I konfigurationsfilen **Customization.settings** til pakketilpasning under mappen **BuildTools** skal du tilføje følgende linje for at medtage det aktuelle eksempel på CRT-udvidelse i pakker, der kan implementeres.

    ``` xml
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll" />
    ```

#### <a name="update-hardware-station"></a>Opdatere Hardwarestation

1. Fjern den tidligere Hardwarestation-udvidelse ved at redigere konfigurationsfilen **HardwareStation.Extension.config**.

    # <a name="retail-73-and-earlier"></a>[Retail 7.3 og tidligere](#tab/retail-7-3)

    Fjern følgende afsnit fra konfigurationsfilerne **HardwareStation.Shared.config** og **HardwareStation.Dedicated.config**.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-731-and-later"></a>[Retail 7.3.1 og nyere](#tab/retail-7-3-1)

    Fjern følgende sektion fra konfigurationsfilen **HardwareStation.Extension.config**.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-100-and-later"></a>[Retail 10.0 og nyere](#tab/retail-10-0)

    Fjern følgende sektion fra konfigurationsfilen **HardwareStation.Extension.config**.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.FiscalRegisterSample" />
    ```
    ---

2. Aktivér det aktuelle eksempel på udvidelse af Hardwarestation ved at føje følgende linje til sektionen **komposition** i konfigurationsfilen **HardwareStation.Extension.config**.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
    ```

3. Foretag følgende ændringer i konfigurationsfilen til **Customization.settings**-pakkeindstillinger under mappen **BuildTools**:

    - Fjern følgende linje for at udelade den tidligere Hardwarestation-udvidelse i installationspakkerne.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample.dll" />
        ```

    - Tilføj følgende linjer for at inkludere det aktuelle eksempel på udvidelse af Hardwarestation i installationspakkerne.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.CleanCashSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Interop.CleanCash_1_1.dll" />
        ```

#### <a name="update-modern-pos"></a>Opdatere Modern POS

1. Åbn løsningen **CloudPOS.sln** i **RetailSdk\\POS**.
2. Deaktiver den tidligere POS-udvidelse:

    - I filen **tsconfig.json** skal du føje mappen **FiscalRegisterSample** til udeladelseslisten.
    - Fjern følgende linjer fra filen **extensions.json** i mappen **RetailSDK\\POS\\Extensions**.

        ``` json
        {
            "baseUrl": "FiscalRegisterSample"
        }
        ```

3. Aktivér det aktuelle eksempel på POS-udvidelse ved at tilføje følgende linjer i filen **extensions.json** under mappen **RetailSDK\\POS\\Extensions**.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

#### <a name="update-cloud-pos"></a>Opdatere Cloud POS

1. Åbn løsningen **ModernPOS.sln** under **RetailSdk\\POS**.
2. Deaktiver den tidligere POS-udvidelse:

    - I filen **tsconfig.json** skal du føje mappen **FiscalRegisterSample** til udeladelseslisten.
    - Fjern følgende linjer fra filen **extensions.json** i mappen **RetailSDK\\POS\\Extensions**.

        ``` json
        {
            "baseUrl": "FiscalRegisterSample"
        }
        ```

3. Aktivér det aktuelle eksempel på POS-udvidelse ved at tilføje følgende linjer i filen **extensions.json** under mappen **RetailSDK\\POS\\Extensions**.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

#### <a name="create-deployable-packages"></a>Oprette installerbare pakker

Kør **msbuild** for hele Retail SDK for at oprette installerbare pakker. Anvend pakkerne via LCS eller manuelt. Du kan finde flere oplysninger i [Retail SDK-pakker](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
