---
title: Eksempel på integration af regnskabsregistreringsservice i Tyskland
description: Denne artikel indeholder en oversigt over eksemplet på regnskabsintegration for Tyskland i Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-05-29
ms.openlocfilehash: 40f2b7ece62c495e4a719121019070a9961fa915
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280300"
---
# <a name="fiscal-registration-service-integration-sample-for-germany"></a>Eksempel på integration af regnskabsregistreringsservice i Tyskland

[!include[banner](../includes/banner.md)]

Denne artikel indeholder en oversigt over eksemplet på regnskabsintegration for Tyskland i Microsoft Dynamics 365 Commerce.

For at opfylde lokale regnskabsmæssige krav til kasseapparater i Tyskland omfatter Microsoft Dynamics 365 Commerce-funktionaliteten for Tyskland en eksempelintegration af POS med en ekstern tjeneste til regnskabsregistrering. Eksemplet udvider [funktionen til regnskabsintegration](fiscal-integration-for-retail-channel.md). Den er baseret på [EFR-løsningen (Electronic Fiscal Register)](https://www.efsta.eu/de/fiskalloesungen/deutschland) fra [EFSTA](https://www.efsta.eu/de/) og giver mulighed for kommunikation med EFR-tjenesten via HTTPS-protokollen. Tjenesten EFR skal være have enten Retail Hardwarestation eller en separat computer som vært, der kan oprettes forbindelse til fra hardwarestationen. Eksemplet findes i form af kildekode og er en del af Retail SDK (Software Development Kit).

Microsoft frigiver ikke hardware, software eller dokumentation fra EFSTA. Du kan få oplysninger om, hvordan du henter EFR-løsningen og bruger den, ved at kontakte [EFSTA](https://www.efsta.eu/de/kontakt/kontakt).

## <a name="scenarios"></a>Scenarier

Følgende scenarier dækkes af eksemplet på integration af tjenesten til regnskabsregistrering for Tyskland.

### <a name="sales-operations"></a>Salgsoperationer

- **Registrering af cash and carry-salg og returneringer i tjenesten til regnskabsregistrering:**

    Registrering af salgsoperationer omfatter følgende trin:

    1. Registrering af transaktionsstart

        Starten af hver transaktion registreres i et teknisk sikkerhedselement (TSE), der er tilknyttet EFR-tjenesten. Som et resultat af registreringen tildeler en TSE et transaktions-id (TID).

    2. Registrering af transaktionsafslutning

        Når en transaktion afsluttes i POS, registreres den ved hjælp af det samme TID, som blev tildelt under registreringen af transaktionens start. På dette tidspunkt sendes detaljerede transaktionsdata til regnskabsregistreringstjenesten. Disse data omfatter oplysninger om salgslinjer og oplysninger om rabatter, betalinger og moms.

    3. Indlæsning af et svar fra regnskabsregistreringstjenesten

        Sikkerhedsdata modtages fra en TSE som en del af et svar og gemmes i transaktionen i kanaldatabasen. Sikkerhedsdataene består af følgende oplysninger:

        - TID
        - Startdato og -klokkeslæt for transaktionen
        - Slutdato og -klokkeslæt for transaktionen
        - Signaturtæller
        - Kontrolværdi
        - Serienummer for TSE

- **Registrering af kundeordrer i regnskabsregistreringstjenesten**: Registreringsprocessen er den samme som processen for cash-and-carry-salg og returneringer.
- **Registrering af operationer, der involverer gavekort og indbetalinger**: Registreringsprocessen er den samme som processen for cash-and-carry-salg og returneringer.

#### <a name="notifying-users-about-fiscal-registration-failures"></a>Brugerbesked om fejl i regnskabsregistreringer

Tjenesten til regnskabsregistrering kan give brugere besked om fejl, der er opstået under regnskabsregistreringen, på to måder:

- Udskriv yderligere oplysninger fra svaret i feltet **Informationsmeddelelse** på kvitteringer.
- Vis beskeder fra regnskabstjenesten som brugermeddelelser i POS.

    > [!NOTE]
    > Denne beskedmekanisme kræver, at parameteren **Vis beskeder om regnskabsregistrering** på siden **Connector-tekniske profiler** er aktiveret.

#### <a name="printing-receipts"></a>Udskrivning af kvitteringer

Udskrivning af kvitteringer er obligatorisk i Tyskland. Alle kvitteringer skal som minimum indeholde følgende oplysninger:

- Firmaets navn og adresse
- Oplysninger om varer, herunder deres priser og antal
- Oplysninger om betalinger, der er modtaget
- Oplysninger om moms, herunder samlede beløb pr. momssats
- Sikkerhedsdata:

    - TID
    - Startdato og -klokkeslæt for transaktionen
    - Slutdato og -klokkeslæt for transaktionen
    - Signaturtæller
    - Kontrolværdi
    - Serienummer for TSE

- Informationsmeddelelse

> [!NOTE]
> En QR-kode kan også udskrives på kvitteringer. Selvom QR-koden er valgfri, anbefales den kraftigt. Yderligere oplysninger om, hvordan du henter QR-kode som en del af et svar fra regnskabsregistreringstjenesten, finder du i dokumentet "EFR Guide \[DE\]", der er udgivet på webstedet for [EFSTA-dokumentationen](https://public.efsta.net/efr/).
>
> I feltet **Informationsmeddelelse** på kvitteringer vises en besked fra regnskabsregistreringstjenesten. Hvis f.eks. en underskriftsenhed er ødelagt, kan der udskrives specialtekst på en kvittering.

#### <a name="voided-suspended-and-recalled-transactions"></a>Afviste, suspenderede og tilbagekaldte transaktioner

- En afvist transaktion registreres som en anmodning om at afslutte en transaktion i tjenesten til regnskabsregistrering.
- En suspenderet transaktion registreres som en anmodning om at afslutte en transaktion i tjenesten til regnskabsregistrering.
- Tilbagekald af en suspenderet transaktion registreres som starten på en ny transaktion i tjenesten til regnskabsregistrering.

### <a name="non-sales-transactions-and-shift-closing"></a>Iikke-salgstransaktioner og lukning af skifte

Følgende transaktioner, der ikke er salgstransaktioner, registreres som ikke-regnskabsmæssige operationer i tjenesten til regnskabsregistrering ved hjælp af **NFS**-koden:

- Angiv startbeløb
- Kassebeholdning
- Fjernelse af betalingsmiddel
- Deponering til pengeskab
- Indsættelse i banken
- Indtægtskonti
- Udgiftskonti

Handlingen **Luk skift** registreres også som ikke-regnskabsmæssig handlinh i tjenesten til regnskabsregistrering ved hjælp af **NFS**-koden.

### <a name="data-export-and-audit"></a>Dataeksport og -revision

Alle transaktioner skal signeres af en TSE for at sikre deres integritet, ægthed og fuldstændighed og for at forhindre manipulering af registrerede data.

> [!WARNING]
> Kun en certificeret TSE kan anvendes. Oplysninger om de typer og modeller af TSE'er, der understøttes i EFR-løsningen, finder du i dokumentet "EFR Guide \[DE\]", der er udgivet på webstedet for [EFSTA-dokumentationen](https://public.efsta.net/efr/). Oplysninger om, hvordan du vælger og anskaffer en TSE, får du ved at kontakte [EFSTA](https://www.efsta.eu/at/kontakt).

Lovgivningen i Tyskland kræver understøttelse af DSFinV-K-eksporten. Eksporten af DSFinV-K kan udløses i EFR-løsningen. Yderligere oplysninger om DSFinV-K-eksporten finder du i dokumentet "EFR Guide \[DE\]", der er udgivet på webstedet for [EFSTA-dokumentationen](https://public.efsta.net/efr/).

### <a name="limitations-of-the-sample"></a>Begrænsninger for eksemplet

Tjenesten til regnskabsregistrering understøtter kun scenarier, hvor moms er inkluderet i prisen. Derfor skal indstillingen **Priserne inkluderer moms** angives til **Ja** for både butikker og kunder.

Regnskabstjenesten understøtter ikke situationer, hvor mere end én momskode anvendes på samme transaktionslinje.

Strukturen til regnskabsintegration understøtter ikke salgstilbud. Derfor er disse operationer ikke registreret i regnskabstjenesten.

## <a name="set-up-commerce-for-germany"></a>Konfigurere Commerce for Tyskland

I dette afsnit beskrives de Commerce -indstillinger, der er specifikke for og anbefales for Tyskland. Du kan finde flere konfigurationsoplysninger på [Startside for Commerce](../index.md).

Hvis du vil bruge den specifikke funktion for Tyskland, skal du angive følgende indstillinger.

- Angiv feltet **Land/område** til **DEU** (Tyskland) i den juridiske enheds primære adresse.
- I POS-funktionalitetsprofilen for alle butikker i Tyskland skal du angive feltet **ISO-kode** til **DE** (Tyskland).

Du skal også angive følgende indstillinger for Tyskland. Du skal køre de relevante distributionsjob, når du har fuldført opsætningen.

### <a name="set-up-vat-per-german-requirements"></a>Konfigurere moms pr. tyske krav

Du skal oprette momskoder, momsgrupper og varemomsgrupper. Du skal også angive momsoplysninger for produkter og tjenester. Du kan finde flere oplysninger om opsætning og brug af momsfunktioner under [Momsoversigt](../../finance/general-ledger/indirect-taxes-overview.md).

På kvitteringer kan du udskrive en forkortet kode for en momskode (f.eks. "A" eller "B"). Du kan gøre denne funktion tilgængelig ved at angive feltet **Kode til udskrivning** på siden **Momskoder**.

### <a name="set-up-stores"></a>Konfigurere butikker

Opdater butiksoplysningerne på siden **Alle butikker**. Du skal angive følgende parametre:

- Vælg den momsgruppe, der skal bruges for salg til standardkunden, i feltet **Momsgruppe**.
- Angiv indstillingen **Priserne inkluderer moms** til **Ja**.
- Angiv feltet **Navn** til firmanavnet. Denne ændring er med til at sikre, at firmanavnet vises på en salgskvittering. Du kan også føje firmanavnet til layoutet for salgskvitteringen som fritekst.
- Angiv feltet **Momsidentifikationsnummer (TIN)** til firmaets identifikationsnummer. Denne ændring er med til at sikre, at firmaets identifikationsnummer vises på en salgskvittering. Du kan også føje firmaets identifikationsnummer til layoutet for salgskvitteringen som fritekst.

### <a name="set-up-functionality-profiles"></a>Konfigurere funktionalitetsprofiler

Konfigurer POS-funktionalitetsprofiler. I oversigtspanelet **Kvitteringsnummerering** skal du oprette kvitteringsnummerering ved at oprette eller opdatere poster for kvitteringstransaktionstyperne **Salg**, **Salgsordre** og **Returnering**.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Konfigurere brugerdefinerede felter, så de kan bruges i kvitteringsformater for salgskvittering

Du kan konfigurere sprogteksten og brugerdefinerede felter, der bruges i POS-kvitteringsformaterne. Standardfirmaet for den bruger, der opretter kvitteringsopsætningen, skal være den samme juridiske enhed, hvor opsætningen af sprogtekster oprettes. Du kan også oprette de samme sprogtekster i både brugerens standardfirma og den juridiske enhed for den butik, som opsætningen oprettes for.

På siden **Sprogtekst** kan du tilføje følgende poster for etiketterne i de brugerdefinerede felter til kvitteringslayout. Bemærk, at værdierne for **Sprog-id**, **Tekst-id** og **Tekst**, der vises i tabellen, kun er eksempler. Du kan nemt ændre dem, så de opfylder dine behov. Men de værdier for **Tekst-id**, du bruger, skal dog være entydige, og de skal være lig med eller større end 900001.

Føj følgende POS-etiketter til sektionen **POS** på siden **Sprogtekst**.

| Sprog-id | Tekst-id | Tekst                                  |
|-------------|---------|---------------------------------------|
| en-US       | 900001  | QR-kode                               |
| en-US       | 900002  | Posterings-id                        |
| en-US       | 900003  | Detailudskriftskode for moms                 |
| en-US       | 900004  | Momsbeløb (salg)                    |
| en-US       | 900005  | Momsgrundlag (salg)                     |
| en-US       | 900006  | Transaktionens startdato/-klokkeslæt           |
| en-US       | 900007  | Slutdato/-klokkeslæt for transaktion             |
| en-US       | 900008  | Serienummeret på sikkerhedselementet |
| en-US       | 900009  | Signaturtæller                     |
| en-US       | 900010  | Kontrolværdi                           |
| en-US       | 900011  | Informationsmeddelelse                          |

På siden **Brugerdefinerede felter** kan du tilføje følgende poster for de brugerdefinerede felter til kvitteringslayout. Bemærk, at værdierne for **Tekst-id for billedtekst** skal svare til de værdier for **Tekst-id**, som du har angivet på siden **Sprogtekst**.

| Navn                            | Type    | Tekst-id for billedtekst |
|---------------------------------|---------|-----------------|
| QRCODE\_DE                      | Kvittering | 900001          |
| TRANSACTIONID\_DE               | Kvittering | 900002          |
| RETAILPRINTCODE\_DE             | Kvittering | 900003          |
| SALESTAXAMOUNT\_DE              | Kvittering | 900004          |
| SALESTAXBASIS\_DE               | Kvittering | 900005          |
| TRANSACTIONSTARTDATETIME\_DE    | Kvittering | 900006          |
| TRANSACTIONENDDATETIME\_DE      | Kvittering | 900007          |
| SECURITYELEMENTSERIALNUMBER\_DE | Kvittering | 900008          |
| SIGNCOUNTER\_DE                 | Kvittering | 900009          |
| SIGN\_DE                        | Kvittering | 900010          |
| INFOMESSAGE\_DE                 | Kvittering | 900011          |

> [!NOTE]
> Det er vigtigt, at du angiver korrekte brugerdefinerede feltnavne, som vist i den foregående tabel. Et forkert felt medfører, at der mangler data ved i kvitteringer.

### <a name="configure-receipt-formats"></a>Konfigurere kvitteringsformater

For hvert påkrævet kvitteringsformat skal du ændre værdien i feltet **Udskriftsfunktion** til **Udskriv altid**.

I designeren til kvitteringsformater skal du føje følgende brugerdefinerede felter til de relevante kvitteringssektioner. Bemærk, at feltnavnene svarer til de sprogtekster, du har defineret i forrige afsnit.

- **Overskrift:** Tilføj følgende felter:

    - Felterne **Butiksnavn** og **Momsidentifikationsnummer**, som bruges til at udskrive firmaets navn og id-nummer på kvitteringer. Du kan også føje firmanavnet og id-nummeret til layoutet som fritekst.
    - Felterne **Butiksadresse**, **Dato**, **24-timerstid**, **Kvitteringsnummer** og **Kassenummer**.

- **Linjer:** Tilføj følgende felter:

    - Feltet **Varenavn**
    - Feltet **Antal**
    - Feltet **Pris i alt med moms**
    - Feltet **Detailudskriftskode for moms**, der bruges til at udskrive den forkortede kode, der svarer til den momskode, der gælder for varen

- **Sidefod:** Tilføj følgende felter:

    - Betalingsfelter, så betalingsbeløbene for de enkelte betalingsmåder udskrives. Føj f.eks. felterne **Navn på betalingsmiddel** og **Beløb for betalingsmiddel** til én linje i layoutet.
    - Felter i feltgruppen **Momsoversigt**. Alle felterne i denne feltgruppe skal udskrives på én separat linje.

        - Feltet **Moms-id**, der er et standardfelt, der gør det muligt at udskrive en momsoversigt for hver momskode. Feltet skal føjes til en ny linje.
        - Feltet **Momsprocent**, som er et standardfelt, der bruges til at udskrive den gældende momssats for momskoden.
        - Feltet **Momsgrundlag (salg)**, som bruges til at udskrive kvitteringens samlede kontantsalgsbeløb for momskoden. Forudbetalinger og gavekorthandlinger er ikke medtaget.
        - Feltet **Momsbeløb (salg)**, som bruges til at udskrive kvitteringens momsbeløb i kontantsalg for momskoden.
        - Feltet **Detailudskriftskode for moms**, der bruges til at udskrive den forkortede kode, der svarer til momskoden.

    - Felter, der indeholder sikrede transaktionsdata, som returneres af tjenesten til regnskabsregistrering:

        - Feltet **Transaktions-id**, som identificerer nummeret på kontanttransaktionen i tjenesten til regnskabsregistrering
        - Feltet **Transaktionens startdato/-klokkeslæt**
        - Feltet **Transaktionens slutdato/-klokkeslæt**
        - Feltet **Serienummeret på sikkerhedselementet**
        - Feltet **Signaturtæller**
        - Feltet **Kontrolværdi**
        - Feltet **QR-kode**, som bruges til at udskrive referencen til den registrerede kontanttransaktion i form af en QR-kode

        > [!NOTE]
        > Værdien af **QR-kode** hentes fra regnskabsregisterets svar. EFR returnerer kun en QR-kode i svaret, hvis værdien af feltet **Attributter** i EFR-konfigurationen er beskrevet i EFSTA-dokumentationen. QR-kodeformatet i feltet **Attributter** i EFR-konfigurationen skal angives til **BMP**.

    - Feltet **Informationsmeddelelse**, så der vises en besked fra regnskabsregistreringstjenesten på kvitteringer. Hvis f.eks. en underskriftsenhed er ødelagt, kan der udskrives specialtekst på en kvittering.

Du kan finde flere oplysninger om, hvordan du arbejder med kvitteringsformater, i [Konfigurere og designe kvitteringsformater](../receipt-templates-printing.md).

## <a name="set-up-fiscal-integration-for-germany"></a>Konfigurere regnskabsintegration for Tyskland

Regnskabsintegrationstjenestens eksempel til Tyskland er baseret på [funktionaliteten af regnskabsintegration](fiscal-integration-for-retail-channel.md) og er en del af Retail SDK. Eksemplet findes i mappen **src\\FiscalIntegration\\Efr** i lageret til [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (f.eks. [eksemplet i frigivelse/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Eksemplet [består](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) af en regnskabsdokumentudbyder, som er en udvidelse af Commerce Runtime (CRT), og en regnskabsconnector, som er en udvidelse af Commerce Hardware Station. Yderligere oplysninger om, hvordan du bruger Retail SDK, finder du i [Retail SDK-arkitekturen](../dev-itpro/retail-sdk/retail-sdk-overview.md) og [Konfigurere en build-pipeline til uafhængige SDK-pakker](../dev-itpro/build-pipeline.md).

> [!WARNING]
> På grund af begrænsningerne ved den [nye uafhængige pakke- og udvidelsesmodel](../dev-itpro/build-pipeline.md) kan den ikke aktuelt bruges til dette eksempel på regnskabsintegration. Du skal bruge den tidligere version af Retail SDK på en virtuel maskine til udviklere (VM) i Microsoft Dynamics Lifecycle Services (LCS). Du kan få flere oplysninger i [Retningslinjer for installation af eksempel på integration af regnskabsregistreringsservice i Tyskland (ældre)](emea-deu-fi-sample-sdk.md).
>
> Understøttelse af den nye uafhængige pakke- og udvidelsesmodel til eksempler på regnskabsintegration er planlagt til senere versioner.

Fuldfør trinnene til opsætning af regnskabsintegration som beskrevet i [Konfigurere regnskabsintegration for Commerce-kanaler](setting-up-fiscal-integration-for-retail-channel.md):

1. [Konfigurer en regnskabsregistreringsproces](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Du skal også notere dig indstillingerne for den regnskabsregistreringsproces, der er [specifik for dette eksempel til integration af regnskabsregistreringstjenesten](#set-up-the-registration-process).
1. [Angive indstillinger for fejlhåndtering](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

    > [!WARNING]
    > Egenskaberne til håndtering af fejl i regnskabsintegrationsstruktur er muligvis ikke fuldstændigt tilpasset de lokale regnskabsregler.
    >
    > - Det anbefales, at du lader indstillingen **Fortsæt ved fejl** på siden **Regnskabsregistreringsproces** være deaktiveret, da alle transaktioner skal registreres korrekt, selvom det første forsøg på registreringen af regnskabet ikke lykkedes.
    > - Før du aktiverer indstillingen **Spring over** eller **Markér som registreret** på siden **Regnskabsregistreringsproces**, bør du diskutere disse ændringer i processen til regnskabsregistrering med skattemyndighederne eller det lokale skattekontor.

1. [Aktiver manuel udførelse af udsatte regnskabsregistreringer](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Konfigurere kanalkomponenter](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Konfigurere registreringsprocessen

Hvis du vil aktivere registreringsprocessen, skal du følge disse trin for at konfigurere Commerce Headquarters. Du kan finde flere oplysninger i [Konfigurere regnskabsintegration for Commerce-kanaler](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Download konfigurationsfiler for regnskabsconnectoren og regnskabsdokumentudbyderen:

    1. Åbn lageret il [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions/).
    1. Vælg en korrekt version af frigivelsesafdelingen i overensstemmelse med din SDK/programversion (f.eks. **[release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Åbn **src \> FiscalIntegration \> Efr**.
    1. Hent konfigurationsfilen til regnskabsdokumentudbyderen på **Konfigurationer \> DocumentProviders \> DocumentProviderFiscalEFRSampleGermany.xml** (for eksempel [filen til frigivelse/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/DocumentProviders/DocumentProviderFiscalEFRSampleGermany.xml)).
    1. Hent konfigurationsfilen til regnskabsconnectoren på **Konfigurationer \> Connectorer \> ConnectorEFRSample.xml** (for eksempel [filen til frigivelse/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/Connectors/ConnectorEFRSample.xml)).

    > [!WARNING]
    > På grund af begrænsningerne ved den [nye uafhængige pakke- og udvidelsesmodel](../dev-itpro/build-pipeline.md) kan den ikke aktuelt bruges til dette eksempel på regnskabsintegration. Du skal bruge den tidligere version af Retail SDK på en virtuel maskine til udviklere i LCS. Konfigurationsfilerne til dette eksempel på regnskabsintegration findes i følgende mapper i Retail SDK på en udvikler VM i LCS:
    >
    > - **Konfigurationsfilen til regnskabsdokumentudbyder:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.EFRSample\\Configuration\\DocumentProviderFiscalEFRSampleGermany.xml
    > - **Konfigurationsfil til regnskabsconnector:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.EFRSample\\Configuration\\ConnectorEFRSample.xml
    > 
    > Understøttelse af den nye uafhængige pakke- og udvidelsesmodel til eksempler på regnskabsintegration er planlagt til senere versioner.

1. Gå til **Retail og Commerce \> Konfiguration af Headquarters \> Parametre \> Delte Commerce-parametre**. Under fanen **Generelt** skal du angive indstillingen **Aktivér regnskabsintegration** til **Ja**.
1. Gå til **Retail og Commerce \> Konfiguration af kanal \> Regnskabsintegration \> Udbydere af regnskabsdokumenter**, og indlæs den konfigurationsfil til regnskabsdokumentudbyderen, du hentede tidligere.
1. Gå til **Retail og Commerce \> Konfiguration af kanal \> Regnskabsintegration \> Regnskabsconnectorer**, og indlæs den konfigurationsfil til regnskabsconnectoren, du hentede tidligere.
1. Gå til **Retail og Commerce \> Konfiguration af kanal \> Regnskabsintegration \> Funktionelle profiler for connector**. Opret en ny funktionel profil for connector. Vælg dokumentprovideren og den connector, du har indlæst tidligere. Opdater [indstillingerne for datatilknytning](#default-data-mapping) efter behov.
1. Gå til **Retail og Commerce \> Konfiguration af kanal \> Regnskabsintegration \> Tekniske profiler for connector**. Opret en ny teknisk profil for connector, og vælg den regnskabsconnector, du indlæste tidligere. Opdater [indstillingerne for connector](#fiscal-connector-settings) efter behov.
1. Gå til **Retail og Commerce \> Konfiguration af kanal \> Regnskabsintegration \> Regnskabsconnectorgrupper**. Opret en ny regnskabsconnector-gruppe for den funktionsprofil for connector, som du oprettede tidligere.
1. Gå til **Retail og Commerce \> Konfiguration af kanal \> Regnskabsintegration \> Processer for regnskabsregistrering**. Opret en ny regnskabsregistreringsproces og et trin i processen til regnskabsregistrering, og vælg den regnskabsconnector-gruppe, du oprettede tidligere.
1. Gå til **Retail og Commerce \> Konfiguration af kanal \> POS-opsætning \> POS-profiler \> Funktionalitetsprofiler**. Vælg en funktionalitetsprofil, der er knyttet til den butik, hvor registreringsprocessen skal aktiveres. Vælg den regnskabsregistreringsproces, du oprettede tidligere, i oversigtspanelet **Regnskabsregistreringsproces**.
1. Gå til **Retail og Commerce \> Konfiguration af kanal \> POS-opsætning \> POS-profiler \> Hardwareprofiler**. Vælg en hardwareprofil, der er tilknyttet den hardwarestation, som bonprinteren skal være tilknyttet. Vælg den tekniske profil for connectoren, du oprettede tidligere, i oversigtspanelet **Eksterne regnskabsenheder**.
1. Åbn distributionsplanen (**Retail og Commerce \> Retail og Commerce IT \> Distributionsplan**), og vælg job **1070** og **1090** for at overføre data til kanaldatabasen.

#### <a name="default-data-mapping"></a>Tilknytning af standarddata

Følgende standarddatatilknytning er inkluderet i konfigurationen af regnskabsdokumentudbyderen som en del af eksemplet på regnskabsintegration:

- **Tilknytning af betalingsmiddeltype** – Tilknytning af betalingsmåder til værdier af attributten **PayG** (betalingsgruppe) i anmodninger, der sendes til regnskabstjenesten. Her er standardtilknytningen:

    ```
    1: 0; 2: 1; 3: 3; 4: 8; 5: 2; 6: 0; 7: 7; 8: 6; 9: 0; 10: 8; 11: 1
    ```

    Den første komponent i de enkelte par repræsenterer en betalingsmetode, der er konfigureret for butikken. Den anden komponent repræsenterer den tilsvarende betalingsgruppe, der understøttes af EFR-regnskabsregistreringsservice. Yderligere oplysninger om betalingsgrupper, som EFR understøtter i Tyskland, finder du i [EFR-referencen](https://public.efsta.net/efr/).

    Eksempeltilknytningen af betalingsmetoder svarer til de butiksbetalingsmetoder, der er konfigureret i standarddemodataene.

    | Betalingsmetode | Navn på betalingsmetode |
    |----------------|---------------------|
    | 1              | Indløsning                |
    | 2              | Tjek               |
    | 3              | Kort                |
    | 4              | Debitorkonto    |
    | 5              | Andet               |
    | 6              | Valuta            |
    | 7              | Bilag             |
    | 8              | Gavekort           |
    | 9              | Betalingsmiddel fjern/variabel |
    | 10             | Fordelskundekort       |
    | 11             | Ikke-lokale checks    |

    Du skal derfor redigere eksempeltilknytningen i overensstemmelse med de betalingsmetoder, der er konfigureret i programmet.

- **Medtag debitordata** – Hvis denne parameter er aktiveret, indeholder anmodninger til regnskabstjenesten debitoroplysninger, f.eks. navne og adresser, i tilfælde, hvor en debitor føjes til en transaktion.
- **Tilknytning af momssatser** – Tilknytning af momsprocentværdier, der er konfigureret for momskoderne til værdier af attributten **TaxG** (momsgruppe) i anmodninger, der sendes til regnskabstjenesten. Her er standardtilknytningen:

    ```
    A: 19.00; B: 7.00; C: 10.70; D: 5.50; E: 0.00
    ```

    Den første komponent i hvert par repræsenterer en momsgruppe, der understøttes af EFR-regnskabsregistreringsservice. Den anden komponent repræsenterer den tilsvarende momssats. Yderligere oplysninger om momsgrupper, som EFR understøtter i Tyskland, finder du i [EFR-referencen](https://public.efsta.net/efr/).

- **Momsgruppe for gavekort og indbetalinger** – Værdien af **TaxG**-attributten i anmodninger, der sendes til regnskabstjenesten, baseret på operationer, der involverer gavekort eller indbetalinger. Her er standardtilknytningen:

    ```
    G
    ```

- **Momsgruppe for momsfritagelse** – Værdien af **TaxG**-attributten i anmodninger, der sendes til regnskabstjenesten, baseret på operationer, der er fritaget for momsforpligtelser. Her er standardtilknytningen:

    ```
    F
    ```

> [!NOTE]
> Momsindstillingerne i standarddatatilknytningen er ansvarlige for sammenholdelse af momsindstillinger i systemet og momsgrupperne i EFR-tjenesten. Momsgrupper kan kun udskrives på kvitteringer, hvis feltet **Kode for udskrivning** er angivet på siden **Momskoder**.

#### <a name="fiscal-connector-settings"></a>Indstillinger af regnskabsconnector

Følgende indstillinger er inkluderet i konfigurationen af regnskabsconnectoren som en del af eksemplet på regnskabsintegration:

- **Slutpunktadresse** – URL-adressen for tjenesten til regnskabsregistrering.
- **Timeout** – Den tid i millisekunder, som regnskabsconnectoren vil vente på et svar fra tjenesten til regnskabsregistrering.
- **Vis beskeder om regnskabsregistrering** – Dette flag styrer, om beskeder, som tjenesten til regnskabsregistrering returnerer, skal vises til operatøren.

### <a name="configure-channel-components"></a>Konfigurere kanalkomponenter

> [!WARNING]
> På grund af begrænsningerne ved den [nye uafhængige pakke- og udvidelsesmodel](../dev-itpro/build-pipeline.md) kan den ikke aktuelt bruges til dette eksempel på regnskabsintegration. Du skal bruge den tidligere version af Retail SDK på en virtuel maskine til udviklere i LCS. Du kan få flere oplysninger i [Retningslinjer for installation af eksempel på integration af regnskabsregistreringsservice i Tyskland (ældre)](emea-deu-fi-sample-sdk.md).
>
> Understøttelse af den nye uafhængige pakke- og udvidelsesmodel til eksempler på regnskabsintegration er planlagt til senere versioner.

#### <a name="set-up-the-development-environment"></a>Konfigurere udviklingsmiljøet

Følg disse trin for at konfigurere et udviklingsmiljø, så du kan teste og udvide eksemplet.

1. Klon eller download lageret til [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions). Vælg en korrekt version af frigivelsesafdelingen i overensstemmelse med din SDK/programversion. Yderligere oplysninger finder du i [Hente Retail SDK-eksempler og -referencepakker fra GitHub og NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Åbn EFR-løsningen på **Dynamics365Commerce.Solutions\\FiscalIntegration\\Efr\\EFR.sln**, og opbyg den.
1. Installere Commerce Runtime-udvidelser:

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

Regnskabsintegrationstjenestens eksempel til Tyskland er baseret på [funktionaliteten af regnskabsintegration](fiscal-integration-for-retail-channel.md) og er en del af Retail SDK. Eksemplet findes i mappen **src\\FiscalIntegration\\Efr** i lageret til [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (f.eks. [eksemplet i frigivelse/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Eksemplet [består](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) af en regnskabsdokumentudbyder, som er en udvidelse af CRT, og en regnskabsconnector, som er en udvidelse af Commerce Hardware Station. Yderligere oplysninger om, hvordan du bruger Retail SDK, finder du i [Retail SDK-arkitekturen](../dev-itpro/retail-sdk/retail-sdk-overview.md) og [Konfigurere en build-pipeline til uafhængige SDK-pakker](../dev-itpro/build-pipeline.md).

> [!WARNING]
> På grund af begrænsningerne ved den [nye uafhængige pakke- og udvidelsesmodel](../dev-itpro/build-pipeline.md) kan den ikke aktuelt bruges til dette eksempel på regnskabsintegration. Du skal bruge den tidligere version af Retail SDK på en virtuel maskine til udviklere i LCS. Du kan få flere oplysninger i [Retningslinjer for installation af eksempel på integration af regnskabsregistreringsservice i Tyskland (ældre)](emea-deu-fi-sample-sdk.md). Understøttelse af den nye uafhængige pakke- og udvidelsesmodel til eksempler på regnskabsintegration er planlagt til senere versioner.

### <a name="crt-extension-design"></a>Design af CRT-udvidelse

Formålet med udvidelsen, som er en udbyder af regnskabsdokumenter, er at generere servicespecifikke dokumenter og håndtere svar fra tjenesten til regnskabsregistrering.

#### <a name="request-handler"></a>Anmodningshandler

Der er en enkelt anmodningshandler til dokumentudbyder, **DocumentProviderEFRFiscalDEU**. Den bruges til at generere regnskabsdokumenter til regnskabsregistreringstjenesten. Den er nedarvet fra brugergrænsefladen i **INamedRequestHandler**. Metoden **HandlerName** er ansvarlig for at returnere navnet på handleren. Navnet på handleren skal svare til navnet på connector-dokumentudbyderen, der er angivet i Commerce Headquarters.

Connectoren understøtter følgende anmodninger:

- **GetFiscalDocumentDocumentProviderRequest** – Denne anmodning indeholder oplysninger om, hvilket dokument der skal genereres. Den returnerer et servicespecifikt dokument, der skal registreres i tjenesten til regnskabsregistrering.
- **GetFiscalTransactionExtendedDataDocumentProviderRequest** – Denne anmodning returnerer svaret sammen med udvidede data.

#### <a name="configuration"></a>Konfiguration

Konfigurationsfilen til regnskabsdokumentudbyderen er placeret i **src\\FiscalIntegration\\Efr\\Configurations\\DocumentProviders\\DocumentProviderFiscalEFRSampleGermany.xml** i lageret for [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Formålet med filen er at aktivere indstillinger for regnskabsdokumentudbyderen, der skal konfigureres fra Commerce Headquarters. Filformatet er tilpasset kravene til konfiguration af regnskabsintegration.

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
