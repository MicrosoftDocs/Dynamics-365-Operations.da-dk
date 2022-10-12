---
title: Retningslinjer for installation af kasseapparater for Norge
description: Denne artikel indeholder en vejledning til, hvordan du aktiverer kasseapparatfunktionaliteten til Microsoft Dynamics 365 Commerce-lokalisering for Norge.
author: EvgenyPopovMBS
ms.date: 10/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-03-01
ms.openlocfilehash: 0e66ef93e65fecaca23f0434c386507a0672d251
ms.sourcegitcommit: 2bc6680dc6b12d20532d383a0edb84d180885b62
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/06/2022
ms.locfileid: "9631309"
---
# <a name="deployment-guidelines-for-cash-registers-for-norway"></a>Retningslinjer for installation af kasseapparater for Norge

[!include[banner](../includes/banner.md)]

> [!IMPORTANT]
> Du skal kun implementere de trin, der er beskrevet i denne artikel, hvis du bruger Microsoft Dynamics 365 Commerce version 10.0.29 eller senere. I Commerce-version 10.0.28 eller tidligere skal du bruge den tidligere version af Retail SDK på en virtuel maskine til udviklere (VM) i Microsoft Dynamics Lifecycle Services (LCS). Yderligere oplysninger finder du i [Retningslinjer for installation af kasseapparater for Norge (ældre)](./emea-nor-loc-deployment-guidelines.md). Hvis du bruger Commerce version 10.0.28 eller tidligere og overfører til Commerce version 10.0.29 eller senere, skal du følge trinnene i [Overfør fra ældre Commerce-funktionalitet for Norge](./emea-nor-fi-migration.md).

Denne artikel indeholder en vejledning til, hvordan du aktiverer kasseapparatfunktionaliteten til Commerce-lokalisering for Norge. Lokaliseringen består af flere komponentudvidelser, der lader dig udføre handlinger som f.eks. at udskrive brugerdefinerede felter på kvitteringer, registrere yderligere revisionshændelser, salgstransaktioner og betalingstransaktioner i POS, signere salgstransaktioner digitalt og udskrive rapporter i lokale formater. Yderligere oplysninger om lokalisering for Norge finder du i [Kasseapparatfunktionalitet til Norge](./emea-nor-cash-registers.md). Du kan finde flere oplysninger om, hvordan du konfigurerer Commerce for Norge, i [Konfigurere Commerce for Norge](./emea-nor-cash-registers.md#setting-up-commerce-for-norway).

## <a name="set-up-fiscal-registration-for-norway"></a>Konfigurere regnskabsregistrering for Norge

Regnskabsregistreringens eksempel til Norge er baseret på [funktionaliteten af regnskabsintegration](fiscal-integration-for-retail-channel.md) og er en del af Commerce SDK. Eksemplet på POS-udvidelse findes i mappen **src\\FiscalIntegration\\SequentialSignatureNorway** i lageret til [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions/). [Eksemplet](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) består af en regnskabsdokumentudbyder og en regnskabsconnector, som er udvidelser til Commerce Runtime (CRT). Yderligere oplysninger om, hvordan du bruger Commerce SDK, finder du i [Download Commerce SDK-prøver og -referencepakker fra GitHub og NuGet](../dev-itpro/retail-sdk/sdk-github.md) og [oprette en build-pipeline til den uafhængige emballage SDK](../dev-itpro/build-pipeline.md).

Fuldfør trinnene til opsætning af regnskabsregistrering som beskrevet i [Konfigurere regnskabsintegration for Commerce-kanaler](./setting-up-fiscal-integration-for-retail-channel.md):

1. [Konfigurer en regnskabsregistreringsproces](./setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Notér indstillingerne for den regnskabsregistreringsproces, der er [specifikke for Norge](#configure-the-fiscal-registration-process).
1. [Angive indstillinger for fejlhåndtering](./setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Aktiver manuel udførelse af udskudt regnskabsregistrering](./setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-deferred-fiscal-registration).
1. [Konfigurere kanalkomponenter](#configure-channel-components).

### <a name="configure-the-fiscal-registration-process"></a>Konfigurere processen til regnskabsregistrering

Hvis du vil aktivere registreringsprocessen for regnskab til Norge, skal du følge disse trin i Commerce Headquarters.

1. Download konfigurationsfiler for regnskabsconnectoren og regnskabsdokumentudbyderen fra Commerce SDK:

    1. Åbn lageret il [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions/).
    1. Åbn den sidste tilgængelige frigivelsesgren.
    1. Åbn **src \> FiscalIntegration \> SequentialSignatureNorway \> CommerceRuntime**.
    1. Hent konfigurationsfilen til regnskabsdokumentudbyderen på **DocumentProvider.SequentialSignNorway \> Konfiguration \> DocumentProviderSequentialSignatureNorwaySample.xml**.
    1. Hent konfigurationsfilen til regnskabsconnectoren på **Connector.SequentialSignNorway \> Konfiguration \> ConnectorSequentialSignatureNorwaySample.xml**.

1. Gå til **Retail og Commerce \> Konfiguration af hovedkontor \> Parametre \> Delte parametre**. Under fanen **Generelt** skal du angive indstillingen **Aktivér regnskabsintegration** til **Ja**.
1. Gå til **Retail og Commerce \> Konfiguration af kanal \> Regnskabsintegration \> Regnskabsconnectorer**, og indlæs den konfigurationsfil til regnskabsconnectoren, du hentede tidligere.
1. Gå til **Retail og Commerce \> Konfiguration af kanal \> Regnskabsintegration \> Udbydere af regnskabsdokumenter**, og indlæs den konfigurationsfil til regnskabsdokumentudbyderen, du hentede tidligere.
1. Gå til **Retail og Commerce \> Konfiguration af kanal \> Regnskabsintegration \> Funktionelle profiler for connector**. Opret en ny funktionel profil for connector, og vælg den dokumentudbyder og connector, du indlæste tidligere.
1. Gå til **Retail og Commerce \> Konfiguration af kanal \> Regnskabsintegration \> Tekniske profiler for connector**. Opret en ny teknisk profil for connector, og vælg den connector, du indlæste tidligere. Angiv connector-typen til **Intern**.
1. Gå til **Retail og Commerce \> Konfiguration af kanal \> Regnskabsintegration \> Regnskabsconnectorgrupper**, og opret en ny regnskabsconnectorgruppe for den funktionsprofil for connector, som du oprettede tidligere.
1. Gå til **Retail og Commerce \> Konfiguration af kanal \> Regnskabsintegration \> Processer for regnskabsregistrering**. Opret en ny regnskabsregistreringsproces og et trin i processen til regnskabsregistrering, og vælg den regnskabsconnector-gruppe, du oprettede tidligere.
1. Gå til **Retail og Commerce \> Konfiguration af kanal \> POS-opsætning \> POS-profiler \> Funktionalitetsprofiler**. Vælg en funktionalitetsprofil, der er knyttet til den butik, hvor registreringsprocessen skal aktiveres. Vælg den regnskabsregistreringsproces, du oprettede tidligere, i oversigtspanelet **Regnskabsregistreringsproces**. Vælg den tekniske profil for connectoren, du oprettede tidligere, i oversigtspanelet **Regnskabsservices**. 
1. Gå til **Retail og Commerce \> Retail og Commerce IT \> Distributionsplan**. Åbn distributionstidsplanen, og vælg jobbene **1070** og **1090** for at overføre data til kanaldatabasen.

### <a name="configure-the-digital-signature-parameters"></a>Konfigurere parametrene for digital signatur

Du skal konfigurere certifikater, der vil blive brugt til digital signering af salgstransaktioner i en butik. Et digitalt certifikat, der gemmes i Azure Key Vault, bruges til signeringen. I forbindelse med offlinetilstanden af Modern POS kan signeringen også ske ved hjælp af et digitalt certifikat, som gemmes i det lokale lager for den maskine, som Modern POS er installeret på.

Før du kan bruge et digitalt certifikat, der er gemt i Key Vault-lageret, skal du fuldføre følgende trin.

1. Key Vault-lageret skal oprettes. Det anbefales, at du implementerer lageret i samme geografiske område som Commerce Scale Unit.
1. Certifikatet skal overføres til Key Vault-lageret som en hemmelig base64-streng.
1. AOS-programmet (Application Object Server) skal være godkendt til at læse hemmeligheder fra Key Vault-lageret.

Du kan finde flere oplysninger om, hvordan du arbejder med Key Vault, i [Kom i gang med Azure Key Vault](/azure/key-vault/key-vault-get-started).

På siden **Key Vault-parametre** skal du derefter angive parametrene for adgang til Key Vault-lageret:

- **Navn** og **Beskrivelse** – Navnet på og beskrivelsen af Key Vault-lageret.
- **URL-adresse til Key Vault** – URL-adressen til Key Vault-lageret.
- **Key Vault-klient** – Det interaktive klient-id for det Azure Active Directory-program (Azure AD), der er tilknyttet et Key Vault-lager til godkendelsesformål. Denne klient skal have adgang til at læse hemmeligheder fra lageret.
- **Nøgle-Vault hemmelig nøgle** – En nøgle, der er tilknyttet det Azure AD-program, som bruges til godkendelse i Key Vault-lageret.
- **Navn**, **Beskrivelse** og **Hemmelig reference** – Navnet på, beskrivelsen af og den hemmelige reference til certifikatet.

Derefter skal du konfigurere en connector til dine certifikater, som gemmes i Key Vault eller det lokale certifikatlager. Denne connector bruges til signering på kanalsiden.

1. Gå til **Retail og Commerce \> Konfiguration af kanal \> Regnskabsintegration \> Tekniske profiler for connector**.
1. Angiv følgende parametre for digitale signaturer i oversigtspanelet **Indstillinger**:

    - **Hemmeligt navn** – Vælg det hemmelige navn, som du tidligere har konfigureret på siden **Key Vault-parametre**.
    - **Lokalt certifikataftryk** – Angiv et aftryk for et certifikat, der er gemt lokalt.
    - **Hash-algoritme** – Angiv en af de hash-krypteringsalgoritmer, der understøttes af Microsoft .NET, f.eks. **SHA1**.
    - **Navn på certifikatlager** – Dette felt er valgfrit. Brug det til at angive et standardbutiksnavn, der skal bruges til søgning efter lokale certifikater.
    - **Placering af certifikatlager** – Dette felt er valgfrit. Brug det til at angive en standardbutiksplacering, der skal bruges til søgning efter lokale certifikater.
    - **Prøv lokalt certifikat først** – Vælg denne indstilling, hvis du som standard vil bruge certifikatet fra det lokale lager til signering af data i stedet for certifikatet fra Key Vault.
    - **Aktivér tilstandskontrol** – Du kan finde flere oplysninger om tilstandskontrol under [Tilstandskontrol af regnskabsregistreringen](./fiscal-integration-for-retail-channel.md#fiscal-registration-health-check).

> [!NOTE]
> - Det er i øjeblikket kun hash-krypteringsalgoritmen **SHA1**, der kan bruges til Norge.
> - Standardbutiksnavnet og butiksplaceringen tilføjes for at forenkle processen med søgning efter lokale certifikater i CRT. X509StoreProvider har en liste over mapper, hvor certifikater gemmes. Hvis standardbutiksnavnet og standardbutiksplaceringen ikke er angivet, forsøger X509StoreProvider at finde et certifikat i alle mapperne på listen.

### <a name="configure-channel-components"></a>Konfigurere kanalkomponenter

#### <a name="development-environment"></a>Udviklingsmiljø

Følg disse trin for at konfigurere et udviklingsmiljø, så du kan teste og udvide eksemplet.

1. Klon eller download lageret til [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions). Vælg en korrekt version af frigivelsesafdelingen i overensstemmelse med din SDK/programversion. Yderligere oplysninger finder du i [Hente Commerce SDK-eksempler og -referencepakker fra GitHub og NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Åbn løsningen **SequentialSignatureNorway.sln** under **Dynamics365Commerce.Solutions\\FiscalIntegration\\SequentialSignatureNorway**, og opbyg den.
1. Installer CRT-udvidelser:

    1. Find installationsprogrammet til CRT-udvidelsen:

        - **Commerce Scale Unit:** I mappen **SequentialSignatureNorway\\ScaleUnit\\ScaleUnit.SequentialSignNorway.Installer\\bin\\Debug\\net461** skal du finde installationsprogrammet **ScaleUnit.SequentialSignNorway.Installer**.
        - **Lokal CRT på Modern POS:** I mappen **SequentialSignatureNorway\\ModernPOS\\ModernPOS.SequentialSignNorway.Installer\\bin\\Debug\\net461** skal du finde installationsprogrammet **ModernPOS.SequentialSignNorway.Installer**.

    1. Start installationsprogrammet til CRT-udvidelsen fra kommandolinjen:

        - **Commerce Scale Unit:**

            ```Console
            ScaleUnit.SequentialSignNorway.Installer.exe install --verbosity 0
            ```

        - **Lokal CRT på Modern POS:**

            ```Console
            ModernPOS.SequentialSignNorway.Installer.exe install --verbosity 0
            ```

#### <a name="production-environment"></a>Produktionsmiljø

Følg trinnene i [Konfigurere en build-pipeline til et eksempel på regnskabsintegration](fiscal-integration-sample-build-pipeline.md) for at generere og frigive Cloud Scale Unit og pakker, der kan implementeres med selvbetjening, til eksemplet på regnskabsintegration. **SequentialSignatureNorway build-pipeline.yaml**-skabelonens YAML-fil findes i mappen **Pipeline\\YAML_Files** i lageret til [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions).

### <a name="enable-the-digital-signature-in-offline-mode-for-modern-pos"></a>Aktivere den digitale signatur i offlinetilstand for Modern POS

Hvis du vil aktivere den digitale signatur i offlinetilstand for Modern POS, skal du følge disse trin, når du har aktiveret Modern POS på en ny enhed.

1. Log på POS.
1. Sørg for, at offlinedatabasen er synkroniseret fuldstændigt på siden **Databaseforbindelsesstatus**. Når værdien i feltet **Ventende overførsler** er **0** (nul), er databasen synkroniseret fuldstændigt.
1. Log af POS.
1. Vent, indtil offlinedatabasen er synkroniseret fuldstændigt.
1. Log på POS.
1. Sørg for, at offlinedatabasen er synkroniseret fuldstændigt på siden **Databaseforbindelsesstatus**. Når værdien i feltet **Afventende transaktioner i offlinedatabasen** er **0** (nul), er databasen synkroniseret fuldstændigt.
1. Åbn Modern POS igen.
