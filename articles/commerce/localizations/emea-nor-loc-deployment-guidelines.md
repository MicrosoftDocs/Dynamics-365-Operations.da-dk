---
title: Retningslinjer for installation af kasseapparater for Norge (ældre)
description: Denne artikel indeholder en installationsvejledning, der viser, hvordan Microsoft Dynamics 365 Commerce-lokaliseringen for Norge aktiveres.
author: EvgenyPopovMBS
ms.date: 08/23/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-2-28
ms.openlocfilehash: fb597add48ac3508a88142e63d80f405b6b5f8b4
ms.sourcegitcommit: 1dbff0b5fa1f4722a1720fac35cce94606fa4320
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/24/2022
ms.locfileid: "9346039"
---
# <a name="deployment-guidelines-for-cash-registers-for-norway-legacy"></a>Retningslinjer for installation af kasseapparater for Norge (ældre)

[!include [banner](../includes/banner.md)]

> [!WARNING]
> Dette eksempel på funktionen til regnskabsintegration kan ikke bruge [struktur til regnskabsintegration](./fiscal-integration-for-retail-channel.md) og bliver udfaset i senere opdateringer. Du skal i stedet bruge den [funktionalitet, der er baseret på regnskabsintegration.](./emea-nor-fi-deployment.md)

Denne artikel indeholder en installationsvejledning, der viser, hvordan Microsoft Dynamics 365 Commerce-lokaliseringen for Norge aktiveres. Lokaliseringen består af flere udvidelser af Commerce-komponenter. Med disse udvidelser kan du f.eks. udskrive brugerdefinerede felter på kvitteringer, registrere yderligere revisionshændelser, salgstransaktioner og betalingstransaktioner i POS, signere salgstransaktioner digitalt og udskrive X- og Z-rapporter i lokale formater. Yderligere oplysninger om lokalisering for Norge finder du i [Kasseapparatfunktionalitet til Norge](./emea-nor-cash-registers.md).

Dette eksempel er en del af Retail SDK (Software Development Kit). Du kan finde oplysninger om SDK i [Arkitektur for Retail SDK (Software Development Kit)](../dev-itpro/retail-sdk/retail-sdk-overview.md).

Dette eksempel består af udvidelser til Commerce Runtime (CRT), Retail Server og POS. Hvis du vil køre dette eksempel, skal du redigere og bygge CRT, Retail Server og POS-projekter. Det anbefales, at du bruger en ikke-ændret Retail SDK til at foretage de ændringer, der er beskrevet i denne artikel. Det anbefales også, at du bruger et kildekontrolsystem som f.eks. Microsoft Visual Studio Online (VSO), hvor ingen filer er ændret endnu.

> [!NOTE]
> I Commerce 10.0.8 og derover kaldes Retail Server for Commerce Scale Unit. Da denne artikel gælder for flere tidligere versioner af appen, bruges *Retail Server* i hele artiklen.
>
> Der er forskellige trin i procedurerne i denne artikel, afhængigt af hvilken version af Commerce du bruger. Du kan finde flere oplysninger i [Nyheder eller ændringer i Dynamics 365 Retail](../get-started/whats-new.md).

### <a name="using-certificate-profiles-in-commerce-channels"></a>Brug af certifikatprofiler i Commerce-kanaler

I Commerce version 10.0.15 og senere kan du bruge den [Brugerdefinerede certifikatprofiler for detailbutikker](./certificate-profiles-for-retail-stores.md)-funktion, der understøtter failover til offline, når Key Vault eller Commerce Headquarters ikke er tilgængelige. Funktionen udvider funktionen [Administrer hemmeligheder for Retail-kanaler](../dev-itpro/manage-secrets.md).

Udfør følgende trin for at bruge funktionen i CRT-udvidelsen.

1. Opret et nyt CRT-udvidelsesprojekt (projekttypen C#-klassebibliotek). Brug eksempelskabelonerne fra Retail SDK (Software Development Kit) (RetailSDK\SampleExtensions\CommerceRuntime).

2. Tilføj brugerdefineret handler for CertificateSignatureServiceRequest i projektet SequentialSignatureRegister.

3. Til at læse et hemmeligt kald bruger `GetUserDefinedSecretCertificateServiceRequest` en konstruktør med parameteren profileId. Det vil starte funktionen med at arbejde med indstillinger fra Certifikatprofiler. På baggrund af indstillingerne hentes certifikatet enten fra Azure Key Vault eller det lokale maskinlager.

    ```csharp
    GetUserDefinedSecretCertificateServiceRequest getUserDefinedSecretCertificateServiceRequest = new GetUserDefinedSecretCertificateServiceRequest(profileId: "ProfileId", secretName: null, thumbprint: null, expirationInterval: null);
    GetUserDefinedSecretCertificateServiceResponse getUserDefinedSecretCertificateServiceResponse = request.RequestContext.Execute<GetUserDefinedSecretCertificateServiceResponse>(getUserDefinedSecretCertificateServiceRequest);

    X509Certificate2 Certificate = getUserDefinedSecretCertificateServiceResponse.Certificate;
    ```

4. Når certifikatet er hentet, skal du fortsætte med datasigneringen.

5. Opbyg CRT-udvidelsesprojektet.

6. Kopiér biblioteket med outputklassen, og indsæt det i ...\RetailServer\webroot\bin\Ext til manuel test.

7. I filen CommerceRuntime.Ext.config skal du opdatere afsnittet om udvidelseskomposition med oplysningerne om det brugerdefinerede bibliotek.

## <a name="development-environment"></a>Udviklingsmiljø

Udfør disse procedurer for at konfigurere et udviklingsmiljø, så du kan teste og udvide eksemplet.

### <a name="the-crt-extension-components"></a>Komponenter til CRT-udvidelse

CRT-udvidelseskomponenterne er inkluderet i CRT-eksemplerne. Du kan fuldføre følgende procedurer ved at åbne CRT-løsningen **CommerceRuntimeSamples.sln** under **RetailSdk\\SampleExtensions\\CommerceRuntime**.

#### <a name="receiptsnorway-component"></a>Komponenten ReceiptsNorway

1. Find projektet **Runtime.Extensions.ReceiptsNorway**, og opbyg det.
2. I mappen **Extensions.ReceiptsNorway\\bin\\Debug** kan du finde assemblyfilen **Contoso.Commerce.Runtime.ReceiptsNorway.dll**.
3. Kopiér assembly-filen til CRT-udvidelsesmappen:

    - **Retail Server:** Kopiér assembly til mappen **\\bin\\ext** under Microsoft IIS-webstedet (Internet Information Services) for Retail Server.
    - **Lokal CRT på Modern POS:** Kopiér assembly-filen til mappen **\\ext** under den lokale CRT Client Broker-placering.

4. Find konfigurationsfilen til CRT-udvidelse:

    - **Retail Server:** Filen kaldes **commerceruntime.ext.config**, og den findes i mappen **bin\\ext** under placeringen af webstedet IIS commerceruntime.
    - **Lokal CRT på Modern POS:** Filen hedder **CommerceRuntime.MPOSOffline.Ext.config**, og den findes under den lokale placering af CRT Client Broker.

5. Registrer CRT-ændringen i konfigurationsfilen til udvidelsen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
    ```

    > [!WARNING]
    > Du må **ikke** redigere filerne commerceruntime.config og CommerceRuntime.MPOSOffline.config. Disse filer er ikke beregnet til tilpasninger.

#### <a name="salespaymenttransext-component"></a>Komponenten SalesPaymentTransExt

1. Find projektet **Runtime.Extensions.SalesPaymentTransExt**, og opbyg det.
2. I mappen **Extensions.SalesPaymentTransExt\\bin\\Debug** kan du finde assemblyfilen **Contoso.Commerce.Runtime.SalesPaymentTransExt.dll**.
3. Kopiér assembly-filen til CRT-udvidelsesmappen:

    - **Retail Server:** Kopiér assembly til mappen **\\bin\\ext** under webstedet for IIS Retail Server.
    - **Lokal CRT på Modern POS:** Kopiér assembly-filen til mappen **\\ext** under den lokale CRT Client Broker-placering.

4. Find konfigurationsfilen til CRT-udvidelse:

    - **Retail Server:** Filen kaldes **commerceruntime.ext.config**, og den findes i mappen **bin\\ext** under placeringen af webstedet IIS commerceruntime.
    - **Lokal CRT på Modern POS:** Filen hedder **CommerceRuntime.MPOSOffline.Ext.config**, og den findes under den lokale placering af CRT Client Broker.

5. Registrer CRT-ændringen i konfigurationsfilen til udvidelsen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
    ```

    > [!WARNING]
    > Du må **ikke** redigere filerne commerceruntime.config og CommerceRuntime.MPOSOffline.config. Disse filer er ikke beregnet til tilpasninger.

#### <a name="xzreportsnorway-component"></a>Komponenten XZReportsNorway

1. Find projektet **Runtime.Extensions.XZReportsNorway**, og opbyg det.
2. I mappen **Extensions.XZReportsNorway\\bin\\Debug** kan du finde assembly-filen **Contoso.Commerce.Runtime.XZReportsNorway.dll**.
3. Kopiér assembly-filen til CRT-udvidelsesmappen:

    - **Retail Server:** Kopiér assembly til mappen **\\bin\\ext** under webstedet for IIS Retail Server.
    - **Lokal CRT på Modern POS:** Kopiér assembly-filen til mappen **\\ext** under den lokale CRT Client Broker-placering.

4. Find konfigurationsfilen til CRT-udvidelse:

    - **Retail Server:** Filen kaldes **commerceruntime.ext.config**, og den findes i mappen **bin\\ext** under placeringen af webstedet IIS commerceruntime.
    - **Lokal CRT på Modern POS:** Filen hedder **CommerceRuntime.MPOSOffline.Ext.config**, og den findes under den lokale placering af CRT Client Broker.

5. Registrer CRT-ændringen i konfigurationsfilen til udvidelsen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
    ```

    > [!WARNING]
    > Du må **ikke** redigere filerne commerceruntime.config og CommerceRuntime.MPOSOffline.config. Disse filer er ikke beregnet til tilpasninger.

# <a name="application-update-4"></a>[Applikationsopdatering 4](#tab/app-update-4)

#### <a name="registerauditevent-sample-component"></a>Eksempelkomponenten RegisterAuditEvent

1. Find projektet **Runtime.Extensions.RegisterAuditEventSample**, og opbyg det.
2. I mappen **Extensions.RegisterAuditEventSample\\bin\\Debug** kan du finde assembly-filen **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll**.
3. Kopiér assembly-filen til CRT-udvidelsesmappen:

    - **Retail Server:** Kopiér assembly til mappen **\\bin\\ext** under webstedet for IIS Retail Server.
    - **Lokal CRT på Modern POS:** Kopiér assembly-filen til mappen **\\ext** under den lokale CRT Client Broker-placering.

4. Find konfigurationsfilen til CRT-udvidelse:

    - **Retail Server:** Filen kaldes **commerceruntime.ext.config**, og den findes i mappen **bin\\ext** under placeringen af webstedet IIS commerceruntime.
    - **Lokal CRT på Modern POS:** Filen hedder **CommerceRuntime.MPOSOffline.Ext.config**, og den findes under den lokale placering af CRT Client Broker.

5. Registrer CRT-ændringen i konfigurationsfilen til udvidelsen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > Du må **ikke** redigere filerne commerceruntime.config og CommerceRuntime.MPOSOffline.config. Disse filer er ikke beregnet til tilpasninger.

#### <a name="salestransactionsignature-sample-component"></a>Eksempelkomponenten SalesTransactionSignature

1. Find projektet **Runtime.Extensions.SalesTransactionSignatureSample**, og opbyg det.
2. Rediger filen **App.config** ved at angive aftryk, butiksadresse og butiksnavn for det certifikat, der skal bruges til at signere salgstransaktioner.
3. Opbyg projektet.
4. Find følgende filer i mappen **Extensions.SalesTransactionSignatureSample\\bin\\Debug**:

    - Assembly-filen **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll**
    - Konfigurationsfilen **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**

5. Kopiér filerne til CRT-udvidelsesmappen:

    - **Retail Server:** Kopiér assembly til mappen **\\bin\\ext** under webstedet for IIS Retail Server.
    - **Lokal CRT på Modern POS:** Kopiér assembly-filen til mappen **\\ext** under den lokale CRT Client Broker-placering.

6. Find konfigurationsfilen til CRT-udvidelse:

    - **Retail Server:** Filen kaldes **commerceruntime.ext.config**, og den findes i mappen **bin\\ext** under placeringen af webstedet IIS commerceruntime.
    - **Lokal CRT på Modern POS:** Filen hedder **CommerceRuntime.MPOSOffline.Ext.config**, og den findes under den lokale placering af CRT Client Broker.

7. Registrer CRT-ændringen i konfigurationsfilen til udvidelsen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > Du må **ikke** redigere filerne commerceruntime.config og CommerceRuntime.MPOSOffline.config. Disse filer er ikke beregnet til tilpasninger.

# <a name="application-update-5-and-later"></a>[Applikationsopdatering 5 og senere](#tab/app-update-5-and-later)

#### <a name="registerauditevent-sample-component"></a>Eksempelkomponenten RegisterAuditEvent

1. Find projektet **Runtime.Extensions.RegisterAuditEventSample**, og opbyg det.
2. I mappen **Extensions.RegisterAuditEventSample\\bin\\Debug** kan du finde assembly-filen **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll**.
3. Kopiér assembly-filen til CRT-udvidelsesmappen:

    - **Retail Server:** Kopiér assembly til mappen **\\bin\\ext** under webstedet for IIS Retail Server.
    - **Lokal CRT på Modern POS:** Kopiér assembly-filen til mappen **\\ext** under den lokale CRT Client Broker-placering.

4. Find konfigurationsfilen til CRT-udvidelse:

    - **Retail Server:** Filen kaldes **commerceruntime.ext.config**, og den findes i mappen **bin\\ext** under placeringen af webstedet IIS commerceruntime.
    - **Lokal CRT på Modern POS:** Filen hedder **CommerceRuntime.MPOSOffline.Ext.config**, og den findes under den lokale placering af CRT Client Broker.

5. Registrer CRT-ændringen i konfigurationsfilen til udvidelsen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > Du må **ikke** redigere filerne commerceruntime.config og CommerceRuntime.MPOSOffline.config. Disse filer er ikke beregnet til tilpasninger.

#### <a name="salestransactionsignature-sample-component"></a>Eksempelkomponenten SalesTransactionSignature

1. Find projektet **Runtime.Extensions.SalesTransactionSignatureSample**, og opbyg det.
2. Rediger filen **App.config** ved at angive aftryk, butiksadresse og butiksnavn for det certifikat, der skal bruges til at signere salgstransaktioner.
3. Opbyg projektet.
4. Find følgende filer i mappen **Extensions.SalesTransactionSignatureSample\\bin\\Debug**:

    - Assembly-filen **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll**
    - Konfigurationsfilen **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**

5. Kopiér filerne til CRT-udvidelsesmappen:

    - **Retail Server:** Kopiér assembly til mappen **\\bin\\ext** under webstedet for IIS Retail Server.
    - **Lokal CRT på Modern POS:** Kopiér assembly-filen til mappen **\\ext** under den lokale CRT Client Broker-placering.

6. Find konfigurationsfilen til CRT-udvidelse:

    - **Retail Server:** Filen kaldes **commerceruntime.ext.config**, og den findes i mappen **bin\\ext** under placeringen af webstedet IIS commerceruntime.
    - **Lokal CRT på Modern POS:** Filen hedder **CommerceRuntime.MPOSOffline.Ext.config**, og den findes under den lokale placering af CRT Client Broker.

7. Registrer CRT-ændringen i konfigurationsfilen til udvidelsen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > Du må **ikke** redigere filerne commerceruntime.config og CommerceRuntime.MPOSOffline.config. Disse filer er ikke beregnet til tilpasninger.

#### <a name="salestransactionsignaturesamplemessages-component"></a>Komponenten SalesTransactionSignatureSample.Messages

1. Find projektet **Runtime.Extensions.SalesTransactionSignatureSample.Messages**, og opbyg det.
2. I mappen **Extensions.SalesTransactionSignatureSample.Messages\\bin\\Debug** kan du finde assembly-filen **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll**.
3. Kopiér assembly-filen til CRT-udvidelsesmappen:

    - **Retail Server:** Kopiér assembly til mappen **\\bin\\ext** under webstedet for IIS Retail Server.
    - **Lokal CRT på Modern POS:** Kopiér assembly-filen til mappen **\\ext** under den lokale CRT Client Broker-placering.

4. Find konfigurationsfilen til CRT-udvidelse:

    - **Retail Server:** Filen kaldes **commerceruntime.ext.config**, og den findes i mappen **bin\\ext** under placeringen af webstedet IIS commerceruntime.
    - **Lokal CRT på Modern POS:** Filen hedder **CommerceRuntime.MPOSOffline.Ext.config**, og den findes under den lokale placering af CRT Client Broker.

5. Registrer CRT-ændringen i konfigurationsfilen til udvidelsen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
    ```

    > [!WARNING]
    > Du må **ikke** redigere filerne commerceruntime.config og CommerceRuntime.MPOSOffline.config. Disse filer er ikke beregnet til tilpasninger.

# <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

#### <a name="registerauditevent-sample-component"></a>Eksempelkomponenten RegisterAuditEvent

1. Find projektet **Runtime.Extensions.RegisterAuditEventSample**, og opbyg det.
2. I mappen **Extensions.RegisterAuditEventSample\\bin\\Debug** kan du finde assembly-filen **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll**.
3. Kopiér assembly-filen til CRT-udvidelsesmappen:

    - **Retail Server:** Kopiér assembly til mappen **\\bin\\ext** under webstedet for IIS Retail Server.
    - **Lokal CRT på Modern POS:** Kopiér assembly-filen til mappen **\\ext** under den lokale CRT Client Broker-placering.

4. Find konfigurationsfilen til CRT-udvidelse:

    - **Retail Server:** Filen kaldes **commerceruntime.ext.config**, og den findes i mappen **bin\\ext** under placeringen af webstedet IIS commerceruntime.
    - **Lokal CRT på Modern POS:** Filen hedder **CommerceRuntime.MPOSOffline.Ext.config**, og den findes under den lokale placering af CRT Client Broker.

5. Registrer CRT-ændringen i konfigurationsfilen til udvidelsen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > Du må **ikke** redigere filerne commerceruntime.config og CommerceRuntime.MPOSOffline.config. Disse filer er ikke beregnet til tilpasninger.

#### <a name="salestransactionsignature-sample-component"></a>Eksempelkomponenten SalesTransactionSignature

1. Find projektet **Runtime.Extensions.SalesTransactionSignatureSample**, og opbyg det.
2. Rediger filen **App.config** ved at angive aftryk, butiksadresse og butiksnavn for det certifikat, der skal bruges til at signere salgstransaktioner.
3. Opbyg projektet.
4. Find følgende filer i mappen **Extensions.SalesTransactionSignatureSample\\bin\\Debug**:

    - Assembly-filen **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll**
    - Konfigurationsfilen **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**

5. Kopiér filerne til CRT-udvidelsesmappen:

    - **Retail Server:** Kopiér assembly til mappen **\\bin\\ext** under webstedet for IIS Retail Server.
    - **Lokal CRT på Modern POS:** Kopiér assembly-filen til mappen **\\ext** under den lokale CRT Client Broker-placering.

6. Find konfigurationsfilen til CRT-udvidelse:

    - **Retail Server:** Filen kaldes **commerceruntime.ext.config**, og den findes i mappen **bin\\ext** under placeringen af webstedet IIS commerceruntime.
    - **Lokal CRT på Modern POS:** Filen hedder **CommerceRuntime.MPOSOffline.Ext.config**, og den findes under den lokale placering af CRT Client Broker.

7. Registrer CRT-ændringen i konfigurationsfilen til udvidelsen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > Du må **ikke** redigere filerne commerceruntime.config og CommerceRuntime.MPOSOffline.config. Disse filer er ikke beregnet til tilpasninger.

#### <a name="sequentialsignatureregistercontracts-component"></a>Komponenten SequentialSignatureRegister.Contracts

1. Find projektet **Runtime.Extensions.SequentialSignatureRegister.Contracts**, og opbyg det.
2. I mappen **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** kan du finde assembly-filen **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll**.
3. Kopiér assembly-filen til CRT-udvidelsesmappen:

    - **Retail Server:** Kopiér assembly til mappen **\\bin\\ext** under webstedet for IIS Retail Server.
    - **Lokal CRT på Modern POS:** Kopiér assembly-filen til mappen **\\ext** under den lokale CRT Client Broker-placering.

# <a name="retail-732-and-later"></a>[Retail 7.3.2 og nyere](#tab/retail-7-3-2)

#### <a name="registerauditevent-sample-component"></a>Eksempelkomponenten RegisterAuditEvent

1. Find projektet **Runtime.Extensions.RegisterAuditEventSample**, og opbyg det.
2. I mappen **Extensions.RegisterAuditEventSample\\bin\\Debug** kan du finde assembly-filen **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll**.
3. Kopiér assembly-filen til CRT-udvidelsesmappen:

    - **Retail Server:** Kopiér assembly til mappen **\\bin\\ext** under webstedet for IIS Retail Server.
    - **Lokal CRT på Modern POS:** Kopiér assembly-filen til mappen **\\ext** under den lokale CRT Client Broker-placering.

4. Find konfigurationsfilen til CRT-udvidelse:

    - **Retail Server:** Filen kaldes **commerceruntime.ext.config**, og den findes i mappen **bin\\ext** under placeringen af webstedet IIS commerceruntime.
    - **Lokal CRT på Modern POS:** Filen hedder **CommerceRuntime.MPOSOffline.Ext.config**, og den findes under den lokale placering af CRT Client Broker.

5. Registrer CRT-ændringen i konfigurationsfilen til udvidelsen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > Du må **ikke** redigere filerne commerceruntime.config og CommerceRuntime.MPOSOffline.config. Disse filer er ikke beregnet til tilpasninger.

#### <a name="sequentialsignatureregister-component"></a>Komponenten SequentialSignatureRegister

1. Find projektet **Runtime.Extensions.SequentialSignatureRegister**.
2. Rediger filen **App.config** ved at angive aftryk, butiksadresse og butiksnavn for det certifikat, der skal bruges til at signere salgstransaktioner.
3. Opbyg projektet.
4. Find følgende filer i mappen **Extensions.SequentialSignatureRegister\\bin\\Debug**:

    - Assembly-filen **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll**
    - Konfigurationsfilen **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**

5. Kopiér filerne til CRT-udvidelsesmappen:

    - **Retail Server:** Kopiér assembly til mappen **\\bin\\ext** under webstedet for IIS Retail Server.
    - **Lokal CRT på Modern POS:** Kopiér assembly-filen til mappen **\\ext** under den lokale CRT Client Broker-placering.

6. Find konfigurationsfilen til CRT-udvidelse:

    - **Retail Server:** Filen kaldes **commerceruntime.ext.config**, og den findes i mappen **bin\\ext** under placeringen af webstedet IIS commerceruntime.
    - **Lokal CRT på Modern POS:** Filen hedder **CommerceRuntime.MPOSOffline.Ext.config**, og den findes under den lokale placering af CRT Client Broker.

7. Registrer CRT-ændringen i konfigurationsfilen til udvidelsen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > Du må **ikke** redigere filerne commerceruntime.config og CommerceRuntime.MPOSOffline.config. Disse filer er ikke beregnet til tilpasninger.

#### <a name="salestransactionsignaturenorway-component"></a>Komponenten SalesTransactionSignatureNorway

1. Find projektet **Runtime.Extensions.SalesTransactionSignatureNorway**.
2. I mappen **Extensions.SalesTransactionSignatureNorway\\bin\\Debug** kan du finde assembly-filen **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll**.
3. Kopiér assembly-filen til CRT-udvidelsesmappen:

    - **Retail Server:** Kopiér assembly til mappen **\\bin\\ext** under webstedet for IIS Retail Server.
    - **Lokal CRT på Modern POS:** Kopiér assembly-filen til mappen **\\ext** under den lokale CRT Client Broker-placering.

4. Find konfigurationsfilen til CRT-udvidelse:

    - **Retail Server:** Filen kaldes **commerceruntime.ext.config**, og den findes i mappen **bin\\ext** under placeringen af webstedet IIS commerceruntime.
    - **Lokal CRT på Modern POS:** Filen hedder **CommerceRuntime.MPOSOffline.Ext.config**, og den findes under den lokale placering af CRT Client Broker.

5. Registrer CRT-ændringen i konfigurationsfilen til udvidelsen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > Du må **ikke** redigere filerne commerceruntime.config og CommerceRuntime.MPOSOffline.config. Disse filer er ikke beregnet til tilpasninger.

#### <a name="sequentialsignatureregistercontracts-component"></a>Komponenten SequentialSignatureRegister.Contracts

1. Find projektet **Runtime.Extensions.SequentialSignatureRegister.Contracts**, og opbyg det.
2. I mappen **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** kan du finde assembly-filen **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll**.
3. Kopiér assembly-filen til CRT-udvidelsesmappen:

    - **Retail Server:** Kopiér assembly til mappen **\\bin\\ext** under webstedet for IIS Retail Server.
    - **Lokal CRT på Modern POS:** Kopiér assembly-filen til mappen **\\ext** under den lokale CRT Client Broker-placering.

#### <a name="salespaymenttransextnorway-component"></a>Komponenten SalesPaymentTransExtNorway

1. Find projektet **Runtime.Extensions.SalesPaymentTransExtNorway**, og opbyg det.
2. I mappen **Extensions.SalesPaymentTransExtNorway\\bin\\Debug** kan du finde assembly-filen **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll**.
3. Kopiér assembly-filen til CRT-udvidelsesmappen:

    - **Retail Server:** Kopiér assembly til mappen **\\bin\\ext** under webstedet for IIS Retail Server.
    - **Lokal CRT på Modern POS:** Kopiér assembly-filen til mappen **\\ext** under den lokale CRT Client Broker-placering.

4. Find konfigurationsfilen til CRT-udvidelse:

    - **Retail Server:** Filen kaldes **commerceruntime.ext.config**, og den findes i mappen **bin\\ext** under placeringen af webstedet IIS commerceruntime.
    - **Lokal CRT på Modern POS:** Filen hedder **CommerceRuntime.MPOSOffline.Ext.config**, og den findes under den lokale placering af CRT Client Broker.

5. Registrer CRT-ændringen i konfigurationsfilen til udvidelsen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > Du må **ikke** redigere filerne commerceruntime.config og CommerceRuntime.MPOSOffline.config. Disse filer er ikke beregnet til tilpasninger.

# <a name="retail-735-and-later"></a>[Retail 7.3.5 og nyere](#tab/retail-7-3-5)

#### <a name="registerauditeventnorway-component"></a>Komponenten RegisterAuditEventNorway

1. Find konfigurationsfilen til CRT-udvidelse:

    - **Retail Server:** Filen kaldes **commerceruntime.ext.config**, og den findes i mappen **bin\\ext** under placeringen af webstedet IIS commerceruntime.
    - **Lokal CRT på Modern POS:** Filen hedder **CommerceRuntime.MPOSOffline.Ext.config**, og den findes under den lokale placering af CRT Client Broker.

2. Registrer CRT-ændringen i konfigurationsfilen til udvidelsen.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
    ```

    > [!WARNING]
    > Du må **ikke** redigere filerne commerceruntime.config og CommerceRuntime.MPOSOffline.config. Disse filer er ikke beregnet til tilpasninger.

#### <a name="sequentialsignatureregister-component"></a>Komponenten SequentialSignatureRegister

1. Find projektet **Runtime.Extensions.SequentialSignatureRegister**.
2. Rediger filen **App.config** ved at angive aftryk, butiksadresse og butiksnavn for det certifikat, der skal bruges til at signere salgstransaktioner.
3. Opbyg projektet.
4. Find følgende filer i mappen **Extensions.SequentialSignatureRegister\\bin\\Debug**:

    - Assembly-filen **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll**
    - Konfigurationsfilen **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**

5. Kopiér filerne til CRT-udvidelsesmappen:

    - **Retail Server:** Kopiér assembly til mappen **\\bin\\ext** under webstedet for IIS Retail Server.
    - **Lokal CRT på Modern POS:** Kopiér assembly-filen til mappen **\\ext** under den lokale CRT Client Broker-placering.

6. Find konfigurationsfilen til CRT-udvidelse:

    - **Retail Server:** Filen kaldes **commerceruntime.ext.config**, og den findes i mappen **bin\\ext** under placeringen af webstedet IIS commerceruntime.
    - **Lokal CRT på Modern POS:** Filen hedder **CommerceRuntime.MPOSOffline.Ext.config**, og den findes under den lokale placering af CRT Client Broker.

7. Registrer CRT-ændringen i konfigurationsfilen til udvidelsen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > Du må **ikke** redigere filerne commerceruntime.config og CommerceRuntime.MPOSOffline.config. Disse filer er ikke beregnet til tilpasninger.

#### <a name="salestransactionsignaturenorway-component"></a>Komponenten SalesTransactionSignatureNorway

1. Find projektet **Runtime.Extensions.SalesTransactionSignatureNorway**.
2. I mappen **Extensions.SalesTransactionSignatureNorway\\bin\\Debug** kan du finde assembly-filen **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll**.
3. Kopiér assembly-filen til CRT-udvidelsesmappen:

    - **Retail Server:** Kopiér assembly til mappen **\\bin\\ext** under webstedet for IIS Retail Server.
    - **Lokal CRT på Modern POS:** Kopiér assembly-filen til mappen **\\ext** under den lokale CRT Client Broker-placering.

4. Find konfigurationsfilen til CRT-udvidelse:

    - **Retail Server:** Filen kaldes **commerceruntime.ext.config**, og den findes i mappen **bin\\ext** under placeringen af webstedet IIS commerceruntime.
    - **Lokal CRT på Modern POS:** Filen hedder **CommerceRuntime.MPOSOffline.Ext.config**, og den findes under den lokale placering af CRT Client Broker.

5. Registrer CRT-ændringen i konfigurationsfilen til udvidelsen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > Du må **ikke** redigere filerne commerceruntime.config og CommerceRuntime.MPOSOffline.config. Disse filer er ikke beregnet til tilpasninger.

#### <a name="sequentialsignatureregistercontracts-component"></a>Komponenten SequentialSignatureRegister.Contracts

1. Find projektet **Runtime.Extensions.SequentialSignatureRegister.Contracts**, og opbyg det.
2. I mappen **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** kan du finde assembly-filen **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll**.
3. Kopiér assembly-filen til CRT-udvidelsesmappen:

    - **Retail Server:** Kopiér assembly til mappen **\\bin\\ext** under webstedet for IIS Retail Server.
    - **Lokal CRT på Modern POS:** Kopiér assembly-filen til mappen **\\ext** under den lokale CRT Client Broker-placering.

#### <a name="salespaymenttransextnorway-component"></a>Komponenten SalesPaymentTransExtNorway

1. Find projektet **Runtime.Extensions.SalesPaymentTransExtNorway**, og opbyg det.
2. I mappen **Extensions.SalesPaymentTransExtNorway\\bin\\Debug** kan du finde assembly-filen **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll**.
3. Kopiér assembly-filen til CRT-udvidelsesmappen:

    - **Retail Server:** Kopiér assembly til mappen **\\bin\\ext** under webstedet for IIS Retail Server.
    - **Lokal CRT på Modern POS:** Kopiér assembly-filen til mappen **\\ext** under den lokale CRT Client Broker-placering.

4. Find konfigurationsfilen til CRT-udvidelse:

    - **Retail Server:** Filen kaldes **commerceruntime.ext.config**, og den findes i mappen **bin\\ext** under placeringen af webstedet IIS commerceruntime.
    - **Lokal CRT på Modern POS:** Filen hedder **CommerceRuntime.MPOSOffline.Ext.config**, og den findes under den lokale placering af CRT Client Broker.

5. Registrer CRT-ændringen i konfigurationsfilen til udvidelsen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > Du må **ikke** redigere filerne commerceruntime.config og CommerceRuntime.MPOSOffline.config. Disse filer er ikke beregnet til tilpasninger.

# <a name="retail-811-and-later"></a>[Retail 8.1.1 og nyere](#tab/retail-8-1-1)

#### <a name="registerauditeventnorway-component"></a>Komponenten RegisterAuditEventNorway

1. Find konfigurationsfilen til CRT-udvidelse:

    - **Retail Server:** Filen kaldes **commerceruntime.ext.config**, og den findes i mappen **bin\\ext** under placeringen af webstedet IIS commerceruntime.
    - **Lokal CRT på Modern POS:** Filen hedder **CommerceRuntime.MPOSOffline.Ext.config**, og den findes under den lokale placering af CRT Client Broker.

2. Registrer CRT-ændringen i konfigurationsfilen til udvidelsen.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
    ```

    > [!WARNING]
    > Du må **ikke** redigere filerne commerceruntime.config og CommerceRuntime.MPOSOffline.config. Disse filer er ikke beregnet til tilpasninger.

#### <a name="sequentialsignatureregister-component"></a>Komponenten SequentialSignatureRegister

1. Find projektet **Runtime.Extensions.SequentialSignatureRegister**.
2. Rediger filen **App.config** ved at angive aftryk, butiksadresse og butiksnavn for det certifikat, der skal bruges til at signere salgstransaktioner.
3. Opbyg projektet.
4. Find følgende filer i mappen **Extensions.SequentialSignatureRegister\\bin\\Debug**:

    - Assembly-filen **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll**
    - Konfigurationsfilen **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**

5. Kopiér filerne til CRT-udvidelsesmappen:

    - **Retail Server:** Kopiér assembly til mappen **\\bin\\ext** under webstedet for IIS Retail Server.
    - **Lokal CRT på Modern POS:** Kopiér assembly-filen til mappen **\\ext** under den lokale CRT Client Broker-placering.

6. Find konfigurationsfilen til CRT-udvidelse:

    - **Retail Server:** Filen kaldes **commerceruntime.ext.config**, og den findes i mappen **bin\\ext** under placeringen af webstedet IIS commerceruntime.
    - **Lokal CRT på Modern POS:** Filen hedder **CommerceRuntime.MPOSOffline.Ext.config**, og den findes under den lokale placering af CRT Client Broker.

7. Registrer CRT-ændringen i konfigurationsfilen til udvidelsen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > Du må **ikke** redigere filerne commerceruntime.config og CommerceRuntime.MPOSOffline.config. Disse filer er ikke beregnet til tilpasninger.

#### <a name="salestransactionsignaturenorway-component"></a>Komponenten SalesTransactionSignatureNorway

1. Find projektet **Runtime.Extensions.SalesTransactionSignatureNorway**.
2. I mappen **Extensions.SalesTransactionSignatureNorway\\bin\\Debug** kan du finde assembly-filen **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll**.
3. Kopiér assembly-filen til CRT-udvidelsesmappen:

    - **Retail Server:** Kopiér assembly til mappen **\\bin\\ext** under webstedet for IIS Retail Server.
    - **Lokal CRT på Modern POS:** Kopiér assembly-filen til mappen **\\ext** under den lokale CRT Client Broker-placering.

4. Find konfigurationsfilen til CRT-udvidelse:

    - **Retail Server:** Filen kaldes **commerceruntime.ext.config**, og den findes i mappen **bin\\ext** under placeringen af webstedet IIS commerceruntime.
    - **Lokal CRT på Modern POS:** Filen hedder **CommerceRuntime.MPOSOffline.Ext.config**, og den findes under den lokale placering af CRT Client Broker.

5. Registrer CRT-ændringen i konfigurationsfilen til udvidelsen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > Du må **ikke** redigere filerne commerceruntime.config og CommerceRuntime.MPOSOffline.config. Disse filer er ikke beregnet til tilpasninger.

#### <a name="sequentialsignatureregistercontracts-component"></a>Komponenten SequentialSignatureRegister.Contracts

1. Find projektet **Runtime.Extensions.SequentialSignatureRegister.Contracts**, og opbyg det.
2. I mappen **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** kan du finde assembly-filen **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll**.
3. Kopiér assembly-filen til CRT-udvidelsesmappen:

    - **Retail Server:** Kopiér assembly til mappen **\\bin\\ext** under webstedet for IIS Retail Server.
    - **Lokal CRT på Modern POS:** Kopiér assembly-filen til mappen **\\ext** under den lokale CRT Client Broker-placering.

#### <a name="salespaymenttransextnorway-component"></a>Komponenten SalesPaymentTransExtNorway

1. Find projektet **Runtime.Extensions.SalesPaymentTransExtNorway**, og opbyg det.
2. I mappen **Extensions.SalesPaymentTransExtNorway\\bin\\Debug** kan du finde assembly-filen **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll**.
3. Kopiér assembly-filen til CRT-udvidelsesmappen:

    - **Retail Server:** Kopiér assembly til mappen **\\bin\\ext** under webstedet for IIS Retail Server.
    - **Lokal CRT på Modern POS:** Kopiér assembly-filen til mappen **\\ext** under den lokale CRT Client Broker-placering.

4. Find konfigurationsfilen til CRT-udvidelse:

    - **Retail Server:** Filen kaldes **commerceruntime.ext.config**, og den findes i mappen **bin\\ext** under placeringen af webstedet IIS commerceruntime.
    - **Lokal CRT på Modern POS:** Filen hedder **CommerceRuntime.MPOSOffline.Ext.config**, og den findes under den lokale placering af CRT Client Broker.

5. Registrer CRT-ændringen i konfigurationsfilen til udvidelsen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > Du må **ikke** redigere filerne commerceruntime.config og CommerceRuntime.MPOSOffline.config. Disse filer er ikke beregnet til tilpasninger.

---

### <a name="the-retail-server-extension-components"></a>Udvidelseskomponenterne i Retail Server

#### <a name="salestransactionsignature-retail-server-sample-component"></a>Retail Server-eksempelkomponenten SalesTransactionSignature

1. I mappen **RetailSDK\\SampleExtensions\\RetailServer\\RetailServer.Extensions.SalesTransactionSignatureSample** skal du finde projektet **RetailServer.Extensions.SalesTransactionSignatureSample** og opbygge det.
2. I mappen **RetailServer\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** kan du finde assembly-filen **Contoso.RetailServer.SalesTransactionSignatureSample.dll**.
3. Kopiér assembly-filen til Retail Server-udvidelsesmappen.

    # <a name="application-update-4"></a>[Applikationsopdatering 4](#tab/app-update-4)

    Mappen er **\\bin**-mappen under placeringen af IIS Retail Server-webstedet.

    # <a name="application-update-5-and-later"></a>[Applikationsopdatering 5 og senere](#tab/app-update-5-and-later)

    Mappen er **\\bin**-mappen under placeringen af IIS Retail Server-webstedet.

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    Mappen er **\\bin\\ext**-mappen under placeringen af IIS Retail Server-webstedet.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 og nyere](#tab/retail-7-3-2)

    Mappen er **\\bin\\ext**-mappen under placeringen af IIS Retail Server-webstedet.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 og nyere](#tab/retail-7-3-5)

    Mappen er **\\bin\\ext**-mappen under placeringen af IIS Retail Server-webstedet.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 og nyere](#tab/retail-8-1-1)

    Mappen er **\\bin\\ext**-mappen under placeringen af IIS Retail Server-webstedet.

    ---

4. Find konfigurationsfilen til Retail Server. Filen kaldes **web.config**, og den findes i rodmappen under placeringen af webstedet IIS Retail Server.
5. Registrer Retail Server-udvidelserne i afsnittet **extensionComposition** i konfigurationsfilen.

    ``` xml
    <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />
    ```

6. Registrer afhængighederne af Retail Server-udvidelserne.

    # <a name="application-update-4"></a>[Applikationsopdatering 4](#tab/app-update-4/)

    1. Find følgende filer i mappen **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug**:

        - Assembly-filen **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll**
        - Konfigurationsfilen **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**

    2. Kopiér filerne til mappen **\\bin** under placeringen af IIS Retail Server-webstedet.
    3. Registrer CRT-ændringen i konfigurationsfilen til udvidelsen for CRT. Filen kaldes **commerceruntime.ext.config**, og den findes i mappen **bin** under placeringen af webstedet IIS Retail Server.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        ```

    # <a name="application-update-5-and-later"></a>[Applikationsopdatering 5 og senere](#tab/app-update-5-and-later/)

    1. I mappen **CommerceRuntime\\Extensions.SalesTransactionSignatureSample.Messages\\bin\\Debug** kan du finde assembly-filen **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll**.
    2. Kopiér filen til mappen **\\bin** under placeringen af IIS Retail Server-webstedet.
    3. Registrer CRT-ændringen i konfigurationsfilen til udvidelsen for CRT. Filen kaldes **commerceruntime.ext.config**, og den findes i mappen **bin** under placeringen af webstedet IIS Retail Server.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
        ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > Ingen handlinger er påkrævet.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 og nyere](#tab/retail-7-3-2)

    > [!NOTE]
    > Ingen handlinger er påkrævet.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 og nyere](#tab/retail-7-3-5)

    > [!NOTE]
    > Ingen handlinger er påkrævet.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 og nyere](#tab/retail-8-1-1)

    > [!NOTE]
    > Ingen handlinger er påkrævet.

    ---

### <a name="the-modern-pos-extension-components"></a>Komponenter til udvidelse af Modern POS

#### <a name="implement-the-proxy-code-for-offline-mode"></a>Implementere proxykoden for offlinetilstand

Denne del svarer til Retail Server-controlleren, men den udvider den lokale CRT, der bruges, når klienten ikke har forbindelse.

1. Rediger afsnittet **@(RetailServerLibraryPathForProxyGeneration)** i filen **customization.settings**, så den bruger den nye Retail Server-assembly til proxygenerering.
2. Implementer følgende brugergrænseflademetoder i klassen **StoreOperationsManager**. Tilføj følgende kode for den første gentagelse:

    # <a name="application-update-4"></a>[Applikationsopdatering 4](#tab/app-update-4)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady()
    {
        throw new NotImplementedException();
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        throw new NotImplementedException();
    }
    ```

    # <a name="application-update-5-and-later"></a>[Applikationsopdatering 5 og senere](#tab/app-update-5-and-later)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady(string correlationId)
    {
        throw new NotImplementedException();
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        throw new NotImplementedException();
    }
    ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > Dette trin gælder ikke for denne version.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 og nyere](#tab/retail-7-3-2)

    > [!NOTE]
    > Dette trin gælder ikke for denne version.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 og nyere](#tab/retail-7-3-5)

    > [!NOTE]
    > Dette trin gælder ikke for denne version.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 og nyere](#tab/retail-8-1-1)

    > [!NOTE]
    > Dette trin gælder ikke for denne version.

    ---

3. Hvis du vil generere proxykoden igen, skal du bygge **Proxies**-mappen fra kommandolinjen ved hjælp af kommandoen **msbuild/t:Rebuild**.
4. Løs projektafhængighederne **Proxies.RetailProxy**:

    # <a name="application-update-4"></a>[Applikationsopdatering 4](#tab/app-update-4)

    Åbn **RetailSDK\\Proxies\\RetailProxy\\Proxies.RetailProxy.csproj**, føj projektet **RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\CommerceRuntime.Extensions.SalesTransactionSignatureSample** til løsningen, og føj en projektreference til projektet **RetailProxy** for at referere til **SalesTransactionSignatureSample**.

    # <a name="application-update-5-and-later"></a>[Applikationsopdatering 5 og senere](#tab/app-update-5-and-later)

    Åbn **RetailSDK\\Proxies\\RetailProxy\\Proxies.RetailProxy.csproj**, føj projektet **RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.SalesTransactionSignatureSample.Messages\\CommerceRuntime.Extensions.SalesTransactionSignatureSample.Messages** til løsningen, og føj en projektreference til projektet **RetailProxy** for at referere til **SalesTransactionSignatureSample.Messages**.

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > Dette trin gælder ikke for denne version.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 og nyere](#tab/retail-7-3-2)

    > [!NOTE]
    > Dette trin gælder ikke for denne version.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 og nyere](#tab/retail-7-3-5)

    > [!NOTE]
    > Dette trin gælder ikke for denne version.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 og nyere](#tab/retail-8-1-1)

    > [!NOTE]
    > Dette trin gælder ikke for denne version.

    ---

5. Juster brugergrænseflademetoderne i klassen **StoreOperationsManager**:

    # <a name="application-update-4"></a>[Applikationsopdatering 4](#tab/app-update-4)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady()
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<SalesTransactionSignatureServiceIsReadyResponse>(new SalesTransactionSignatureServiceIsReadyRequest(), null).IsReady);
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<GetLastFiscalTransactionResponse>(new GetLastFiscalTransactionRequest(), null).FiscalTransaction);
    }
    ```

    # <a name="application-update-5-and-later"></a>[Applikationsopdatering 5 og senere](#tab/app-update-5-and-later)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady(string correlationId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<SalesTransactionSignatureServiceIsReadyResponse>(new SalesTransactionSignatureServiceIsReadyRequest(), null).IsReady);
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<GetLastFiscalTransactionResponse>(new GetLastFiscalTransactionRequest(), null).FiscalTransaction);
    }
    ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > Dette trin gælder ikke for denne version.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 og nyere](#tab/retail-7-3-2)

    > [!NOTE]
    > Dette trin gælder ikke for denne version.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 og nyere](#tab/retail-7-3-5)

    > [!NOTE]
    > Dette trin gælder ikke for denne version.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 og nyere](#tab/retail-8-1-1)

    > [!NOTE]
    > Dette trin gælder ikke for denne version.

    ---

6. Opdater filen **dllhost.exe.config**, så Client Broker indlæser den nye RetailProxy-assembly.

    ``` xml
    <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy" />
    <add key="AdaptorCallerFullTypeName" value="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller" />
    ```

#### <a name="retail-proxy-extension-component-retail-731-and-later"></a>Udvidelseskomponent for Retail-proxy (Retail 7.3.1 og senere)

Udfør kun følgende procedure, hvis du bruger Retail 7.3.1 og senere.

1. I mappen **RetailSDK\\SampleExtensions\\RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample** skal du finde projektet **RetailServer.Extensions.SalesTransactionSignatureSample** og opbygge det.
2. I mappen **RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample\\bin\\Debug** kan du finde assembly-filen **Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample**.
3. Kopiér assembly-filerne til mappen **\\ext** under den lokale CRT Client Broker-placering.
4. Registrer Retail proxy-ændringen i konfigurationsfilen til udvidelsen. Filen hedder **RetailProxy.MPOSOffline.ext.config**, og den findes under den lokale placering af CRT Client Broker.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
    ```

#### <a name="modern-pos-extension-components"></a>Komponenter til udvidelse af Modern POS

1. Åbn løsningen på **RetailSdk\\POS\\ModernPOS.sln**, og kontrollér, at den kan kompileres uden fejl. Derudover skal du sørge for, at du kan køre Modern POS fra Microsoft Visual Studio ved hjælp af kommandoen **Kør**.

    > [!NOTE]
    > Modern POS må ikke tilpasses. Du skal aktivere User Account Control (UAC), og du skal afinstallere tidligere installerede forekomster af Modern POS efter behov.

2. Medtag følgende eksisterende kildekodemapper i projektet **Pos.Extensions**.

    # <a name="application-update-4"></a>[Applikationsopdatering 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[Applikationsopdatering 5 og senere](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 og nyere](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 og nyere](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 og nyere](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

3. Aktivér udvidelserne, så de kan kompileres i **tsconfig.json**, ved at fjerne følgende mapper fra udeladelseslisten.

    # <a name="application-update-4"></a>[Applikationsopdatering 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[Applikationsopdatering 5 og senere](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 og nyere](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 og nyere](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 og nyere](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

4. Aktivér udvidelserne til indlæsning i **extensions.json** ved at tilføje følgende linjer det rette sted.

    # <a name="application-update-4"></a>[Applikationsopdatering 4](#tab/app-update-4)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="application-update-5-and-later"></a>[Applikationsopdatering 5 og senere](#tab/app-update-5-and-later)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 og nyere](#tab/retail-7-3-2)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 og nyere](#tab/retail-7-3-5)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 og nyere](#tab/retail-8-1-1)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    ---

    > [!NOTE]
    > Yderligere oplysninger og eksempler, der viser, hvordan du medtager kildekodemapper og aktiverer udvidelser, der skal indlæses, finder du i instruktionerne i readme.md-filen i projektet **Pos.Extensions**.

5. Genopbyg løsningen.
6. Kør Modern POS i fejlfindingsfunktionen, og test funktionaliteten.

### <a name="cloud-pos-extension-components"></a>Komponenter for udvidelse af Cloud POS

1. Åbn løsningen på **RetailSdk\\POS\\CloudPOS.sln**, og kontrollér, at den kan kompileres uden fejl.
2. Medtag følgende eksisterende kildekodemapper i projektet **Pos.Extensions**.

    # <a name="application-update-4"></a>[Applikationsopdatering 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[Applikationsopdatering 5 og senere](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 og nyere](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 og nyere](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 og nyere](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

3. Aktivér udvidelserne, så de kan kompileres i **tsconfig.json**, ved at fjerne følgende mapper fra udeladelseslisten.

    # <a name="application-update-4"></a>[Applikationsopdatering 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[Applikationsopdatering 5 og senere](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 og nyere](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 og nyere](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 og nyere](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

4. Aktivér udvidelserne til indlæsning i **extensions.json** ved at tilføje følgende linjer det rette sted.

    # <a name="application-update-4"></a>[Applikationsopdatering 4](#tab/app-update-4)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="application-update-5-and-later"></a>[Applikationsopdatering 5 og senere](#tab/app-update-5-and-later)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 og nyere](#tab/retail-7-3-2)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 og nyere](#tab/retail-7-3-5)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 og nyere](#tab/retail-8-1-1)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    ---

    > [!NOTE]
    > Yderligere oplysninger og eksempler, der viser, hvordan du medtager kildekodemapper og aktiverer udvidelser, der skal indlæses, finder du i instruktionerne i readme.md-filen i projektet **Pos.Extensions**.

5. Genopbyg løsningen.
6. Kør løsningen ved at bruge kommandoen **Kør** og følge trinnene i Retail SDK-håndbogen.
7. Test funktionaliteten.

### <a name="set-up-required-parameters-in-headquarters"></a>Konfigurere påkrævede parametre i Headquarters

Du kan finde flere oplysninger under [Kasseapparatfunktionalitet til Norge](./emea-nor-cash-registers.md).

## <a name="production-environment"></a>Produktionsmiljø

Følg disse trin for at oprette installerbare pakker, der indeholder Commerce-komponenter, og for at anvende disse pakker i et produktionsmiljø.

1. Gennemfør trinnene i afsnittet [Komponenter for udvidelse af Cloud POS](#cloud-pos-extension-components) eller [Komponenter til udvidelse af Modern POS](#modern-pos-extension-components) tidligere i denne artikel.
2. Foretag følgende ændringer i pakkekonfigurationsfilerne under mappen **RetailSdk\\Assets**:

    1. I konfigurationsfilerne **commerceruntime.ext.config** og **CommerceRuntime.MPOSOffline.Ext.config** skal du føje følgende linjer til afsnittet **komposition**:

        # <a name="application-update-4"></a>[Applikationsopdatering 4](#tab/app-update-4)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="application-update-5-and-later"></a>[Applikationsopdatering 5 og senere](#tab/app-update-5-and-later)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 og nyere](#tab/retail-7-3-2)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 og nyere](#tab/retail-7-3-5)

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 og nyere](#tab/retail-8-1-1)

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        ---

    2. Aktivér tilpasning af Commerce Proxy:

        # <a name="application-update-4"></a>[Applikationsopdatering 4](#tab/app-update-4)

        I konfigurationsfilen **dllhost.exe.config** skal du føje følgende linjer til underafsnittet **appSettings** i sektionen **konfiguration**.

        ``` xml
        <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy"/>
        <add key="AdaptorCallerFullTypeName" value ="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller"/>
        ```

        # <a name="application-update-5-and-later"></a>[Applikationsopdatering 5 og senere](#tab/app-update-5-and-later)

        I konfigurationsfilen **dllhost.exe.config** skal du føje følgende linjer til underafsnittet **appSettings** i sektionen **konfiguration**.

        ``` xml
        <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy"/>
        <add key="AdaptorCallerFullTypeName" value ="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller"/>
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        Føj følgende linjer til sektionen **komposition** i konfigurationsfilen **RetailProxy.MPOSOffline.ext.config**:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 og nyere](#tab/retail-7-3-2)

        Føj følgende linjer til sektionen **komposition** i konfigurationsfilen **RetailProxy.MPOSOffline.ext.config**:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 og nyere](#tab/retail-7-3-5)

        Føj følgende linjer til sektionen **komposition** i konfigurationsfilen **RetailProxy.MPOSOffline.ext.config**:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 og nyere](#tab/retail-8-1-1)

        Føj følgende linjer til sektionen **komposition** i konfigurationsfilen **RetailProxy.MPOSOffline.ext.config**:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        ---

3. Foretag følgende ændringer i konfigurationsfilen til **Customization.settings**-pakketilpasning:

    1. Aktivér tilpasning af Retail Proxy.

        # <a name="application-update-4"></a>[Applikationsopdatering 4](#tab/app-update-4)

        Føj følgende linjer til sektionen **&lt;ItemGroup Condition="'@(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;**.

        ``` xml
        <RetailServerLibraryPathForProxyGeneration Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll"/>
        ```

        # <a name="application-update-5-and-later"></a>[Applikationsopdatering 5 og senere](#tab/app-update-5-and-later)

        Føj følgende linjer til sektionen **&lt;ItemGroup Condition="'@(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;**.

        ``` xml
        <RetailServerLibraryPathForProxyGeneration Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll"/>
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        Føj følgende linjer til sektionen **ItemGroup** for at medtage Retail proxy-udvidelsen i de installerbare pakker:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 og nyere](#tab/retail-7-3-2)

        Føj følgende linjer til sektionen **ItemGroup** for at medtage Retail proxy-udvidelsen i de installerbare pakker:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 og nyere](#tab/retail-7-3-5)

        Føj følgende linjer til sektionen **ItemGroup** for at medtage Retail proxy-udvidelsen i de installerbare pakker:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 og nyere](#tab/retail-8-1-1)

        Føj følgende linjer til sektionen **ItemGroup** for at medtage Retail proxy-udvidelsen i de installerbare pakker:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        ---

    2. Føj følgende linjer til sektionen **ItemGroup** for at medtage CRT-udvidelserne i de installerbare pakker:

        # <a name="application-update-4"></a>[Applikationsopdatering 4](#tab/app-update-4)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="application-update-5-and-later"></a>[Applikationsopdatering 5 og senere](#tab/app-update-5-and-later)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 og nyere](#tab/retail-7-3-2)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 og nyere](#tab/retail-7-3-5)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 og nyere](#tab/retail-8-1-1)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        ---

    3. Føj følgende linjer til sektionen **ItemGroup** for at medtage Retail Server-udvidelsen i de installerbare pakker:

        # <a name="application-update-4"></a>[Applikationsopdatering 4](#tab/app-update-4)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        ```

        # <a name="application-update-5-and-later"></a>[Applikationsopdatering 5 og senere](#tab/app-update-5-and-later)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll" />
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 og nyere](#tab/retail-7-3-2)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 og nyere](#tab/retail-7-3-5)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 og nyere](#tab/retail-8-1-1)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        ---

4. Rediger følgende filer for at medtage ressourcefilerne for Norge i pakker, der kan implementeres:
    - Packages\_SharedPackagingProjectComponents\Sdk.ModernPos.Shared.csproj
    - Packages\RetailServer\Sdk.RetailServerSetup.proj
  
  - For filen **Sdk.ModernPos.Shared.csproj** 
    - Tilføj linje i sektionen **ItemGroup**
    
        ``` xml
        <<File_name> Include="$(SdkReferencesPath)\nb-NO\*" />
        ```
    > [!Note]
    > I stedet for <File_name> skal du angive navnet på ressourcefilen. Det samme er relevant for de andre eksempler, der er angivet nedenfor.
 
    - Tilføj linje i afsnittet **Target Name="CopyPackageFiles"**
       ``` xml
        <Copy SourceFiles="@(<File_name>)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\nb-NO" SkipUnchangedFiles="true" />
        ```
  
  - Til filen **Sdk.RetailServerSetup.proj** 
    - Tilføj linje i sektionen **ItemGroup**
        ``` xml
        <<File_name> Include="$(SdkReferencesPath)\nb-NO\*" />
        ```    
    - Tilføj linje i afsnittet **Target Name="CopyPackageFiles"**
         ``` xml
        <Copy SourceFiles="@(<File_name>)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\nb-NO" SkipUnchangedFiles="true" />
        ```    

5. Rediger certifikatets konfigurationsfil ved at angive aftryk, butiksadresse og butiksnavn for det certifikat, der skal bruges til at signere salgstransaktioner. Kopiér derefter konfigurationsfilen til mappen **Referencer**.

    # <a name="application-update-4"></a>[Applikationsopdatering 4](#tab/app-update-4)

    Filen hedder **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** og ligger under **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug**.

    # <a name="application-update-5-and-later"></a>[Applikationsopdatering 5 og senere](#tab/app-update-5-and-later)

    Filen hedder **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** og ligger under **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug**.

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    Filen hedder **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** og ligger under **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug**.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 og nyere](#tab/retail-7-3-2)

    Filen hedder **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** og ligger under **Extensions.SequentialSignatureRegister\\bin\\Debug**.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 og nyere](#tab/retail-7-3-5)

    Filen hedder **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** og ligger under **Extensions.SequentialSignatureRegister\\bin\\Debug**.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 og nyere](#tab/retail-8-1-1)

    Filen hedder **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** og ligger under **Extensions.SequentialSignatureRegister\\bin\\Debug**.

    ---

6. Opdater konfigurationsfilen til Retail Server. I filen **RetailSDK\\Packages\\RetailServer\\Code\\web.config** skal du føje følgende linjer til sektionen **extensionComposition**.

    ``` xml
    <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />
    ```

7. Kør **msbuild** for hele Retail SDK for at oprette installerbare pakker.
8. Anvend pakkerne via Microsoft Dynamics Lifecycle Services (LCS) eller manuelt. Du kan finde flere oplysninger under [Oprette installerbare pakker](../dev-itpro/retail-sdk/retail-sdk-packaging.md).

### <a name="enable-the-digital-signature-in-offline-mode-for-modern-pos"></a>Aktivere den digitale signatur i offlinetilstand for Modern POS

Hvis du vil aktivere den digitale signatur i offlinetilstand for Modern POS, skal du følge disse trin, når du har aktiveret Modern POS på en ny enhed.

1. Log på POS.
2. Sørg for, at offlinedatabasen er synkroniseret fuldstændigt på siden **Databaseforbindelsesstatus**. Når værdien i feltet **Ventende overførsler** er **0** (nul), er databasen synkroniseret fuldstændigt.
3. Log af POS.
4. Vent lidt, indtil offlinedatabasen er synkroniseret fuldstændigt.
5. Log på POS.
6. Sørg for, at offlinedatabasen er synkroniseret fuldstændigt på siden **Databaseforbindelsesstatus**. Når værdien i feltet **Afventende transaktioner i offlinedatabasen** er **0** (nul), er databasen synkroniseret fuldstændigt.
7. Genstart Modern POS.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
