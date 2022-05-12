---
title: Eksempel på integration af regnskabsregistreringsservice i Østrig
description: Dette emne indeholder en oversigt over eksemplet på regnskabsintegration for Østrig i Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: 826c1cb0fba7025b16dadbfa6157683392945103
ms.sourcegitcommit: 7faf82fa7ce269c0201abb8473af861ef7ce00bf
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/19/2022
ms.locfileid: "8614145"
---
# <a name="fiscal-registration-service-integration-sample-for-austria"></a>Eksempel på integration af regnskabsregistreringsservice i Østrig

[!include[banner](../includes/banner.md)]

Dette emne indeholder en oversigt over eksemplet på regnskabsintegration for Østrig i Microsoft Dynamics 365 Commerce.

For at opfylde lokale regnskabsmæssige krav til kasseapparater i Østrig omfatter Dynamics 365 Retail-funktionaliteten for Østrig en eksempelintegration af POS med en ekstern tjeneste til regnskabsregistrering. Eksemplet udvider [funktionen til regnskabsintegration](fiscal-integration-for-retail-channel.md). Den er baseret på [EFR-løsningen (Electronic Fiscal Register)](https://www.efsta.eu/at/fiskalloesungen/oesterreich) fra [EFSTA](https://www.efsta.eu/at/) og giver mulighed for kommunikation med EFR-tjenesten via HTTPS-protokollen. Tjenesten EFR skal være have enten Retail Hardwarestation eller en separat maskine som vært, der kan oprettes forbindelse til fra hardwarestationen. Eksemplet findes i form af kildekode og er en del af Retail SDK (Software Development Kit).

Microsoft frigiver ikke hardware, software eller dokumentation fra EFSTA. Du kan få oplysninger om, hvordan du henter EFR-løsningen og bruger den, ved at kontakte [EFSTA](https://www.efsta.eu/at/kontakt).

## <a name="scenarios"></a>Scenarier

Følgende scenarier dækkes af eksemplet på integration af tjenesten til regnskabsregistrering for Østrig:

- Registrering af kontanttransaktioner i regnskabsregistreringstjenesten:

    - Send detaljerede transaktionsdata til regnskabsregistreringstjenesten. Disse data omfatter oplysninger om salgslinjer og oplysninger om rabatter, betalinger og moms.
    - Indlæs et svar fra regnskabsregistreringstjenesten. Dette svar omfatter en digital signatur og et link til den registrerede transaktion.
    - Registrer moms, og knyt dem til regnskabsregistreringstjenestens momskoder.
    - Udskriv QR-koden for en registreret transaktion på kvitteringen.

- Registrering af gavekorthandlinger og kundeindbetalinger som ikke-kontante transaktioner i regnskabsregistreringstjenesten:

    - Udsted eller tilføj penge på et gavekort.
    - Registrer en indbetaling på kundekonto.
    - Registrer en indbetaling på kundeordre.

- Registrering af ikke-salgstransaktioner og hændelser som ikke-kontante transaktioner i regnskabsregistreringstjenesten:

    - Åbne skift og lukke skift
    - Startbeløb, kassebeholdning og fjernelse af betalingsmiddel
    - Prisændring
    - Momsændring
    - Udskriv kopi af kvittering
    - Åbn kasseskuffe
    - Udskriv X-rapport
    - Udskriv Z-rapport

- Udskrivning af opgørelser ved lukketid (X/Z-rapporter), der har felter, som er specifikke for Østrig:

    - Det samlede antal produkter eller tjenester, der er leveret til kunder
    - Oversigt over salg efter momssats
    - Oversigt over betalinger efter kasserer/kasseekspedient
    - Prisrabatter og returneringer, der reducerer det daglige salg
    - Nulsalg (gaver)

- Fejlhåndtering som f.eks. følgende muligheder:

    - Forsøg at registrere et regnskab igen, hvis et nyt forsøg er muligt, f.eks. hvis tjenesten til regnskabsregistrering ikke er tilgængelig, ikke er klar eller ikke svarer.
    - Udskyd regnskabsregistrering.
    - Undlad regnskabsregistrering, eller markér transaktionen som registreret, og inkluder infokoder for at registrere årsagen til fejlen og flere oplysninger.
    - Kontrollér, om tjenesten til regnskabsregistrering er tilgængelig, før en ny salgstransaktion åbnes, eller en salgstransaktion færdiggøres.

### <a name="gift-cards"></a>Gavekort

I eksemplet med integration af tjenester til regnskabsregistrering implementeres følgende regler, der er relateret til gavekort:

- Udelad salgslinjer, der er relateret til handlingerne *Udsted gavekort* og *Føj til gavekort* fra en kontanttransaktion. I stedet for at registrere disse linjer som en del af en kontanttransaktion skal de registreres som en separat ikke-kontanttransaktion i tjenesten til regnskabsregistrering.
- Udskriv ikke en momsgruppeoversigt og en QR-kode på en kvittering, hvis kvitteringen kun består af gavekortlinjer.
- Udskriv det samlede beløb af gavekort, der er udstedt eller genopfyldt i en transaktion, uafhængigt af kontanttransaktionsbeløbet på kvitteringen.
- Gem beregnede reguleringer af betalingslinjer i kanaldatabasen med en reference til en tilsvarende regnskabstransaktion.
- Betaling med gavekort betragtes som en almindelig betaling.

### <a name="customer-deposits-and-customer-order-deposits"></a>Kundeindbetalinger og indbetalinger for kundeordrer

I eksemplet med integration af tjenester til regnskabsregistrering implementeres følgende regler, der er relateret til kundeindbetalinger og indbetalinger for kundeordrer:

- Registrer en ikke-kontanttransaktion, hvis en transaktion er en kundeindbetaling.
- Registrer en ikke-kontanttransaktion, hvis en transaktion kun indeholder en kundeordreindbetaling eller en refusion af en kundeordreindbetaling.
- Træk indbetalingsbeløbet for kundeordren fra betalingslinjerne, når der oprettes en hybridkundeordre.
- Gem beregnede reguleringer af betalingslinjer i kanaldatabasen med en reference til en tilsvarende regnskabstransaktion for en hybrid kundeordre.

### <a name="limitations-of-the-sample"></a>Begrænsninger for eksemplet

Tjenesten til regnskabsregistrering understøtter kun scenarier, hvor moms er inkluderet i prisen. Derfor skal indstillingen **Prisen inkluderer moms** angives til **Ja** for både butikker og kunder.

## <a name="set-up-commerce-for-austria"></a>Konfigurere Commerce for Østrig

I dette afsnit beskrives de Commerce -indstillinger, der er specifikke for og anbefales for Østrig. Yderligere oplysninger om opsætning finder du på [Startside for Commerce](../index.md).

Hvis du vil bruge den specifikke østrigske funktion, skal du angive følgende indstillinger:

- Angiv feltet **Land/område** til **AUT** (Østrig) i den juridiske enheds primære adresse.
- I POS-funktionalitetsprofilen for alle butikker i Østrig skal du angive feltet **ISO-kode** til **AT** (Østrig).

Du skal også angive følgende indstillinger for Østrig. Bemærk, at du skal køre de relevante distributionsjob, når du har fuldført opsætningen.

### <a name="set-up-vat-per-austrian-requirements"></a>Konfigurere moms pr. østrigske krav

Du skal oprette momskoder, momsgrupper og varemomsgrupper. Du skal også angive momsoplysninger for produkter og tjenester. Du kan finde flere oplysninger om opsætning og brug af momsfunktioner under [Momsoversigt](../../finance/general-ledger/indirect-taxes-overview.md).

På kvitteringer kan du udskrive en forkortet kode for en momskode (f.eks. "A" eller "B"). Du kan gøre denne funktion tilgængelig ved at angive feltet **Udskriv kode** på siden **Momskoder**.

### <a name="set-up-stores"></a>Konfigurere butikker

Opdater butiksoplysningerne på siden **Alle butikker**. Du skal angive følgende parametre:

- Vælg den momsgruppe, der skal bruges for salg til standardkunden, i feltet **Momsgruppe**.
- Angiv indstillingen **Priserne inkluderer moms** til **Ja**.
- Angiv feltet **Navn** til firmanavnet. Denne ændring er med til at sikre, at firmanavnet vises på en salgskvittering. Du kan også føje firmanavnet til layoutet for salgskvitteringen som fritekst.
- Angiv feltet **Momsidentifikationsnummer (TIN)** til firmaets identifikationsnummer. Denne ændring er med til at sikre, at firmaets identifikationsnummer vises på en salgskvittering. Du kan også føje firmaets identifikationsnummer til layoutet for salgskvitteringen som fritekst.

### <a name="set-up-functionality-profiles"></a>Konfigurere funktionalitetsprofiler

Konfigurere POS-funktionalitetsprofiler:

- I oversigtspanelet **Kvitteringsnummerering** skal du oprette kvitteringsnummerering ved at oprette eller opdatere poster for kvitteringstransaktionstyperne **Salg**, **Salgsordre** og **Returnering**.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Konfigurere brugerdefinerede felter, så de kan bruges i kvitteringsformater for salgskvittering

Du kan konfigurere sprogteksten og brugerdefinerede felter, der bruges i POS-kvitteringsformaterne. Standardfirmaet for den bruger, der opretter kvitteringsopsætningen, skal være den samme juridiske enhed, hvor opsætningen af sprogtekster oprettes. Du kan også oprette de samme sprogtekster i både brugerens standardfirma og den juridiske enhed for den butik, som opsætningen oprettes for.

På siden **Sprogtekst** kan du tilføje følgende poster for etiketterne i de brugerdefinerede felter til kvitteringslayout. Bemærk, at værdierne for **Sprog-id**, **Tekst-id** og **Tekst**, der vises i tabellen, kun er eksempler. Du kan nemt ændre dem, så de opfylder dine behov. Men de værdier for **Tekst-id**, du bruger, skal dog være entydige, og de skal være lig med eller større end 900001.

Føj følgende POS-etiketter til sektionen **POS** i **Sprogtekst** fra tabellen:

| Sprog-id | Tekst-id | Tekst                      |
|-------------|---------|---------------------------|
| en-US       | 900001  | QR-kode                   |
| en-US       | 900002  | Fortløbende nummer         |
| en-US       | 900003  | Detailudskriftskode for moms     |
| en-US       | 900004  | I alt (salg)             |
| en-US       | 900005  | Samlet moms (salg)         |
| en-US       | 900006  | Total inkluderer moms (salg) |
| en-US       | 900007  | Momsbeløb (salg)        |
| en-US       | 900008  | Momsgrundlag (salg)         |

På siden **Brugerdefinerede felter** kan du tilføje følgende poster for de brugerdefinerede felter til kvitteringslayout. Bemærk, at værdier for **Tekst-id for billedtekst** skal svare til de værdier for **Tekst-id**, som du har angivet på siden **Sprogtekst**:

| Navn                 | Type    | Tekst-id for billedtekst |
|----------------------|---------|-----------------|
| QRCODE               | Kvittering | 900001          |
| CONTINUOUSNUMBER     | Kvittering | 900002          |
| RETAILPRINTCODE      | Kvittering | 900003          |
| SALESTOTAL           | Kvittering | 900004          |
| SALESTOTALTAX        | Kvittering | 900005          |
| SALESTOTALINCLUDETAX | Kvittering | 900006          |
| SALESTAXAMOUNT       | Kvittering | 900007          |
| SALESTAXBASIS        | Kvittering | 900008          |

> [!NOTE]
> Det er vigtigt, at du angiver korrekte brugerdefinerede feltnavne, som vist i den foregående tabel. Et forkert felt medfører, at der mangler data ved i kvitteringer.

### <a name="configure-receipt-formats"></a>Konfigurere kvitteringsformater

For hvert påkrævet kvitteringsformat skal du ændre værdien i feltet **Udskriftsfunktion** til **Udskriv altid**.

I designeren til kvitteringsformater skal du føje følgende brugerdefinerede felter til de relevante kvitteringssektioner. Bemærk, at feltnavnene svarer til de sprogtekster, du har defineret i forrige afsnit.

- **Overskrift:** Tilføj følgende felter:

    - Felterne **Butiksnavn** og **Momsidentifikationsnummer**, som bruges til at udskrive firmaets navn og id-nummer på kvitteringer. Du kan også føje firmanavnet og id-nummeret til layoutet som fritekst.
    - Felterne **Butiksadresse**, **Dato**, **24-timerstid**, **Kvitteringsnummer** og **Kassenummer**.
    - Felterne **Fortløbende nummer**, der identificerer nummeret på kontanttransaktionen i tjenesten til regnskabsregistrering.

- **Linjer:** Tilføj følgende felter:

    - **Varenavn**.
    - **Antal**.
    - **Pris i alt med moms**.
    - **Detailudskriftskode for moms**, der bruges til at udskrive den forkortede kode, der svarer til den momskode, der gælder for varen.

- **Sidefod:** Tilføj følgende felter:

    - Betalingsfelter, så betalingsbeløbene for de enkelte betalingsmåder udskrives. Føj f.eks. felterne **Navn på betalingsmiddel** og **Beløb for betalingsmiddel** til én linje i layoutet.
    - Feltgruppen **Salgstotal**:

        - Feltet **Total (salg)**, som bruges til at udskrive kvitteringens samlede kontantsalgsbeløb. Beløbet er uden moms. Forudbetalinger og gavekorthandlinger er ikke medtaget.
        - Feltet **Total inkluderer moms (salg)**, som bruges til at udskrive kvitteringens samlede kontantsalgsbeløb. Beløbet inkluderer moms. Forudbetalinger og gavekorthandlinger er ikke medtaget.
        - Feltet **Samlet moms (salg)**, som bruges til at udskrive kvitteringens samlede momsbeløb for kontantsalg. Forudbetalinger og gavekorthandlinger er ikke medtaget.

    - Feltgruppen **Momsoversigt**. Alle felterne i denne feltgruppe skal udskrives på én separat linje.

        - Feltet **Moms-id**, der er et standardfelt, der gør det muligt at udskrive en momsoversigt for hver momskode. Feltet skal føjes til en ny linje.
        - Feltet **Momsprocent**, som er et standardfelt, der bruges til at udskrive den gældende momssats for momskoden.
        - Feltet **Momsgrundlag (salg)**, som bruges til at udskrive kvitteringens samlede kontantsalgsbeløb for momskoden. Forudbetalinger og gavekorthandlinger er ikke medtaget.
        - Feltet **Momsbeløb (salg)**, som bruges til at udskrive kvitteringens momsbeløb i kontantsalg for momskoden.
        - Feltet **Detailudskriftskode for moms**, der bruges til at udskrive den forkortede kode, der svarer til momskoden.

    - Feltet **QR-kode**, som bruges til at udskrive referencen til den registrerede kontanttransaktion i form af QR-kode.

        > [!NOTE]
        > Værdien af **QR-kode** hentes fra regnskabsregisterets svar. EFR returnerer kun en QR-kode i svaret, hvis værdien af feltet **Attributter** i EFR-konfigurationen er beskrevet i EFSTA-dokumentationen. QR-kodeformatet i feltet **Attributter** i EFR-konfigurationen skal angives til **BMP**.

Du kan finde flere oplysninger om, hvordan du arbejder med kvitteringsformater, i [Konfigurere og designe kvitteringsformater](../receipt-templates-printing.md).

## <a name="set-up-fiscal-integration-for-austria"></a>Konfigurere regnskabsintegration for Østrig

Regnskabsintegrationstjenestens eksempel til Østrig er baseret på [funktionaliteten af regnskabsintegration](fiscal-integration-for-retail-channel.md) og er en del af Retail SDK. Eksemplet findes i mappen **src\\FiscalIntegration\\Efr** i lageret til [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (f.eks. [eksemplet i frigivelse/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Eksemplet [består](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) af en regnskabsdokumentudbyder, som er en udvidelse af Commerce Runtime (CRT), og en regnskabsconnector, som er en udvidelse af Commerce Hardware Station. Yderligere oplysninger om, hvordan du bruger Retail SDK, finder du i [Retail SDK-arkitekturen](../dev-itpro/retail-sdk/retail-sdk-overview.md) og [Konfigurere en build-pipeline til uafhængige SDK-pakker](../dev-itpro/build-pipeline.md).

> [!WARNING]
> På grund af begrænsningerne ved den [nye uafhængige pakke- og udvidelsesmodel](../dev-itpro/build-pipeline.md) kan den ikke aktuelt bruges til dette eksempel på regnskabsintegration. Du skal bruge den tidligere version af Retail SDK på en virtuel maskine til udviklere (VM) i Microsoft Dynamics Lifecycle Services (LCS). Du kan få flere oplysninger i [Retningslinjer for installation af eksempel på integration af regnskabsregistreringsservice i Østrig (ældre)](emea-aut-fi-sample-sdk.md). Understøttelse af den nye uafhængige pakke- og udvidelsesmodel til eksempler på regnskabsintegration er planlagt til senere versioner.

Fuldfør trinnene til opsætning af regnskabsintegration som beskrevet i [Konfigurere regnskabsintegration for Commerce-kanaler](setting-up-fiscal-integration-for-retail-channel.md):

1. [Konfigurer en regnskabsregistreringsproces](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Du skal også notere dig indstillingerne for den regnskabsregistreringsproces, der er [specifik for dette eksempel til integration af regnskabsregistreringstjenesten](#set-up-the-registration-process).
1. [Angive indstillinger for fejlhåndtering](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Aktiver manuel udførelse af udsatte regnskabsregistreringer](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Konfigurere kanalkomponenter](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Konfigurere registreringsprocessen

Hvis du vil aktivere registreringsprocessen, skal du følge disse trin for at konfigurere Commerce Headquarters. Du kan finde flere oplysninger i [Konfigurere regnskabsintegration for Commerce-kanaler](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Download konfigurationsfiler for regnskabsconnectoren og regnskabsdokumentudbyderen:

    1. Åbn lageret il [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions/).
    1. Vælg en korrekt version af frigivelsesafdelingen i overensstemmelse med din SDK/programversion (f.eks. **[release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Åbn **src \> FiscalIntegration \> Efr**.
    1. Åbn **Konfigurationer \> DocumentProviders**, og hent konfigurationsfiler til regnskabsdokumentudbyderen: **DocumentProviderFiscalEFRSampleAustria.xml** og **DocumentProviderNonFiscalEFRSampleAustria.xml** (f.eks. [placeringen af filerne til frigivelse/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr/Configurations/DocumentProviders)).
    1. Hent konfigurationsfilen til regnskabsconnectoren på **Konfigurationer \> Connectorer \> ConnectorEFRSample.xml** (for eksempel [filen til frigivelse/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/Connectors/ConnectorEFRSample.xml)).

    > [!WARNING]
    > På grund af begrænsningerne ved den [nye uafhængige pakke- og udvidelsesmodel](../dev-itpro/build-pipeline.md) kan den ikke aktuelt bruges til dette eksempel på regnskabsintegration. Du skal bruge den tidligere version af Retail SDK på en virtuel maskine til udviklere i LCS. Konfigurationsfilerne til dette eksempel på regnskabsintegration findes i følgende mapper i Retail SDK på en udvikler VM i LCS:
    >
    > - **Konfigurationsfiler til regnskabsdokumentudbyder:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.EFRSample\\Configuration
    > - **Konfigurationsfil til regnskabsconnector:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.EFRSample\\Configuration
    > 
    > Understøttelse af den nye uafhængige pakke- og udvidelsesmodel til eksempler på regnskabsintegration er planlagt til senere versioner.

1. Gå til **Retail og Commerce \> Konfiguration af Headquarters \> Parametre \> Delte Commerce-parametre**. Under fanen **Generelt** skal du angive indstillingen **Aktivér regnskabsintegration** til **Ja**.
1. Gå til **Retail og Commerce \> Konfiguration af kanal \> Regnskabsintegration \> Udbydere af regnskabsdokumenter**, og indlæs de konfigurationsfiler til regnskabsdokumentudbyderen, du hentede tidligere.
1. Gå til **Retail og Commerce \> Konfiguration af kanal \> Regnskabsintegration \> Regnskabsconnectorer**, og indlæs den konfigurationsfil til regnskabsconnectoren, du hentede tidligere.
1. Gå til **Retail og Commerce \> Konfiguration af kanal \> Regnskabsintegration \> Funktionelle profiler for connector**. Opret to nye funktionelle connector-profiler, én for hver udbyder af regnskabsdokumenter, du indlæste tidligere, og vælg den regnskabsconnector, du indlæste tidligere. Opdater [indstillingerne for datatilknytning](#default-data-mapping) efter behov.
1. Gå til **Retail og Commerce \> Konfiguration af kanal \> Regnskabsintegration \> Tekniske profiler for connector**. Opret en ny teknisk profil for connector, og vælg den regnskabsconnector, du indlæste tidligere. Opdater [indstillingerne for connector](#fiscal-connector-settings) efter behov.
1. Gå til **Retail og Commerce \> Konfiguration af kanal \> Regnskabsintegration \> Regnskabsconnectorgrupper**. Opret to nye regnskabsconnector-grupper, én for hver funktionsprofil for connector, som du oprettede tidligere.
1. Gå til **Retail og Commerce \> Konfiguration af kanal \> Regnskabsintegration \> Processer for regnskabsregistrering**. Opret en ny regnskabsregistreringsproces og to trin i processen til regnskabsregistrering, og vælg de regnskabsconnector-grupper, du oprettede tidligere.
1. Gå til **Retail og Commerce \> Konfiguration af kanal \> POS-opsætning \> POS-profiler \> Funktionalitetsprofiler**. Vælg en funktionalitetsprofil, der er knyttet til den butik, hvor registreringsprocessen skal aktiveres. Vælg den regnskabsregistreringsproces, du oprettede tidligere, i oversigtspanelet **Regnskabsregistreringsproces**. Hvis du vil aktivere registrering af ikke-regnskabshændelser på POS, skal du angive indstillingen **Overvågning** til **Ja** i oversigtspanelet **Funktioner** under **POS**.
1. Gå til **Retail og Commerce \> Konfiguration af kanal \> POS-opsætning \> POS-profiler \> Hardwareprofiler**. Vælg en hardwareprofil, der er tilknyttet den hardwarestation, som bonprinteren skal være tilknyttet. Vælg den tekniske profil for connectoren, du oprettede tidligere, i oversigtspanelet **Eksterne regnskabsenheder**.
1. Åbn distributionsplanen (**Retail og Commerce \> Retail og Commerce IT \> Distributionsplan**), og vælg job **1070** og **1090** for at overføre data til kanaldatabasen.

#### <a name="default-data-mapping"></a>Tilknytning af standarddata

Følgende standarddatatilknytning er inkluderet i konfigurationen af regnskabsdokumentudbyderen som en del af eksemplet på regnskabsintegration:

- **Tilknytning af momssatser** – Tilknytning af momsprocentværdier, der er konfigureret for momskoderne til værdier af attributten **TaxG** (momsgruppe) i anmodninger, der sendes til regnskabstjenesten. Her er standardtilknytningen:

    ```
    A: 20.00; B: 10.00; C: 13.00; D: 0.00; E: 19.00; F: 7.00
    ```

    Den første komponent i hvert par repræsenterer en momsgruppe, der understøttes af EFR-regnskabsregistreringsservice. Den anden komponent repræsenterer den tilsvarende momssats. Yderligere oplysninger om momsgrupper, som EFR understøtter i Østrig, finder du i [EFR-referencen](https://public.efsta.net/efr/).

#### <a name="fiscal-connector-settings"></a>Indstillinger af regnskabsconnector

Følgende indstillinger er inkluderet i konfigurationen af regnskabsconnectoren som en del af eksemplet på regnskabsintegration:

- **Slutpunktadresse** – URL-adressen for tjenesten til regnskabsregistrering.
- **Timeout for enhed** – Den tid i millisekunder, som regnskabsconnectoren vil vente på et svar fra tjenesten til regnskabsregistrering.
- **Vis beskeder om regnskabsregistrering** – Dette flag styrer, om beskeder, som tjenesten til regnskabsregistrering returnerer, skal vises til operatøren.

### <a name="configure-channel-components"></a>Konfigurere kanalkomponenter

> [!WARNING]
> På grund af begrænsningerne ved den [nye uafhængige pakke- og udvidelsesmodel](../dev-itpro/build-pipeline.md) kan den ikke aktuelt bruges til dette eksempel på regnskabsintegration. Du skal bruge den tidligere version af Retail SDK på en virtuel maskine til udviklere i LCS. Du kan få flere oplysninger i [Retningslinjer for installation af eksempel på integration af regnskabsregistreringsservice i Østrig (ældre)](emea-aut-fi-sample-sdk.md).
>
> Understøttelse af den nye uafhængige pakke- og udvidelsesmodel til eksempler på regnskabsintegration er planlagt til senere versioner.

#### <a name="set-up-the-development-environment"></a>Konfigurere udviklingsmiljøet

Følg disse trin for at konfigurere et udviklingsmiljø, så du kan teste og udvide eksemplet.

1. Klon eller download lageret til [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions). Vælg en korrekt version af frigivelsesafdelingen i overensstemmelse med din SDK/programversion. Yderligere oplysninger finder du i [Hente Retail SDK-eksempler og -referencepakker fra GitHub og NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Åbn EFR-løsningen på **Dynamics365Commerce.Solutions\\FiscalIntegration\\Efr\\EFR.sln**, og opbyg den.
1. Installer CRT-udvidelser:

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

Regnskabsintegrationstjenestens eksempel til Østrig er baseret på [funktionaliteten af regnskabsintegration](fiscal-integration-for-retail-channel.md) og er en del af Retail SDK. Eksemplet findes i mappen **src\\FiscalIntegration\\Efr** i lageret til [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (f.eks. [eksemplet i frigivelse/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Eksemplet [består](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) af en regnskabsdokumentudbyder, som er en udvidelse af CRT, og en regnskabsconnector, som er en udvidelse af Commerce Hardware Station. Yderligere oplysninger om, hvordan du bruger Retail SDK, finder du i [Retail SDK-arkitekturen](../dev-itpro/retail-sdk/retail-sdk-overview.md) og [Konfigurere en build-pipeline til uafhængige SDK-pakker](../dev-itpro/build-pipeline.md).

> [!WARNING]
> På grund af begrænsningerne ved den [nye uafhængige pakke- og udvidelsesmodel](../dev-itpro/build-pipeline.md) kan den ikke aktuelt bruges til dette eksempel på regnskabsintegration. Du skal bruge den tidligere version af Retail SDK på en virtuel maskine til udviklere i LCS. Du kan få flere oplysninger i [Retningslinjer for installation af eksempel på integration af regnskabsregistreringsservice i Østrig (ældre)](emea-aut-fi-sample-sdk.md). Understøttelse af den nye uafhængige pakke- og udvidelsesmodel til eksempler på regnskabsintegration er planlagt til senere versioner.

### <a name="commerce-runtime-extension-design"></a>Design af Commerce Runtime-udvidelse 

Formålet med udvidelsen, som er en udbyder af regnskabsdokumenter, er at generere servicespecifikke dokumenter og håndtere svar fra tjenesten til regnskabsregistrering.

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

Konfigurationsfilerne til udbyderen af regnskabsdokumentet findes i mappen **src\\FiscalIntegration\\Efr\\Configurations\\DocumentProviders** til lageret for [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions/):

- **DocumentProviderFiscalEFRSampleAustria** – Konfigurationsfilen til regnskabsdokumentudbyderen af regnskabsdokumenter.
- **DocumentProviderNonFiscalEFRSampleAustria** – Konfigurationsfilen til regnskabsdokumentudbyderen af ikke-regnskabsdokumenter.

Formålet med disse filer er at aktivere indstillinger for regnskabsdokumentudbyderen, der skal konfigureres fra Commerce Headquarters. Filformatet er tilpasset kravene til konfiguration af regnskabsintegration.

### <a name="hardware-station-extension-design"></a>Design af hardwarestationsudvidelse

Formålet med regnskabsconnector-udvidelsen er at kommunikere med tjenesten til regnskabsregistrering. Udvidelsen til Hardwarestation bruger HTTP- og HTTPS-protokoller til at sende dokumenter, som CRT-udvidelsen genererer til regnskabsregistreringstjenesten. Den håndterer også de svar, der er modtaget fra tjenesten til regnskabsregistrering.

#### <a name="request-handler"></a>Anmodningshandler

Anmodningshandleren **EFRHandler** er indgangspunktet for håndtering af anmodninger til tjenesten til regnskabsregistrering.

Denne handler er nedarvet fra brugergrænsefladen i **INamedRequestHandler**. Metoden **HandlerName** er ansvarlig for at returnere navnet på handleren. Navnet på handleren skal svare til navnet på den regnskabsconnector, der er angivet i Commerce Headquarters.

Regnskabsconnector understøtter følgende anmodninger:

- **SubmitDocumentFiscalDeviceRequest** – Denne anmodning sender dokumenter til tjenesten til regnskabsregistrering og returnerer et svar fra den.
- **IsReadyFiscalDeviceRequest** – Denne anmodning bruges til tilstandskontrol af tjenesten til regnskabsregistrering.
- **InitializeFiscalDeviceRequest** – Denne anmodning bruges til at initialisere tjenesten til regnskabsregistrering.

#### <a name="configuration"></a>Konfiguration

Konfigurationsfilen til regnskabsconnectoren er placeret i **src\\FiscalIntegration\\Efr\\Configurations\\Connectors\\ConnectorEFRSample.xml** i lageret for [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Formålet med filen er at aktivere indstillinger for regnskabsconnectoren, der skal konfigureres fra Commerce Headquarters. Filformatet er tilpasset kravene til konfiguration af regnskabsintegration.

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

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
