---
title: Eksempel på integration af bonprinter for Italien
description: Dette emne indeholder en oversigt over eksemplet på regnskabsintegration for Italien i Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2018-11-1
ms.openlocfilehash: 02226fd9f2c92db2518ca48baefb680a3d2f0ac1
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2022
ms.locfileid: "8076897"
---
# <a name="fiscal-printer-integration-sample-for-italy"></a>Eksempel på integration af bonprinter for Italien

[!include[banner](../includes/banner.md)]

Dette emne indeholder en oversigt over eksemplet på regnskabsintegration for Italien i Microsoft Dynamics 365 Commerce.

Funktionaliteten af Commerce for Italien omfatter en eksempelintegration af POS med en bonprinter. Eksemplet udvider [funktionaliteten af regnskabsintegration](fiscal-integration-for-retail-channel.md), så den fungerer med [Epson FP-90III-seriens](https://www.epson.it/products/sd/pos-printer/epson-fp-90iii-series) printere fra Epson, og det giver mulighed for kommunikation med en bonprinter i webservertilstand via webservicen EpsonFPMate ved hjælp af Fiscal ePOS-Print-API. Eksemplet understøtter kun tilstanden Registratore Telematico (RT). Eksemplet findes i form af kildekode og er en del af Retail SDK (Software Development Kit).

Microsoft frigiver ikke hardware, software eller dokumentation fra Epson. Oplysninger om, hvordan du henter bonprinteren og bruger den, får du ved at kontakte [Epson Italia S.p.A](https://www.epson.it).

## <a name="scenarios"></a>Scenarier

Følgende scenarier dækkes af eksemplet på integration af bonprinter for Italien:

- Salgsscenarier:

    - Udskriv en regnskabskvittering for cash-and-carry-salg og returneringer.
    - Hent et svar fra bonprinteren, og gem det i kanaldatabasen.
    - Moms:

        - Knyt til bonprinterens momskoder (afdelinger).
        - Overfør tilknyttede momsdata til bonprinteren.
        - Udskriv moms på en regnskabskvittering.

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

    - Udskriv en stregkode for kvitteringsnummeret på en regnskabskvittering.
    - Udskriv de [kundeoplysninger](emea-ita-customer-information.md), der er angivet for en salgstransaktion, på en regnskabskvittering. Dette er f.eks. kundens lotterikode. 

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
- Daglige rapporter (regnskab X og regnskab Z) udskrives ved hjælp af det format, der er integreret i bonprinterens firmware.
- Bonprinteren understøtter ikke blandede transaktioner. Indstillingen **Forbyd blanding af salg og returneringer på én kvittering** skal angives til **Ja** i POS-funktionsprofiler.
- Eksemplet understøtter kun integration med en bonprinter, der arbejder i tilstanden Registratore Telematico (RT).

## <a name="set-up-fiscal-integration-for-italy"></a>Konfigurere regnskabsintegration for Italien

Bonprinterintegrationens eksempel til Italien er baseret på [funktionaliteten af regnskabsintegration](fiscal-integration-for-retail-channel.md) og er en del af Retail SDK. Eksemplet findes i mappen **src\\FiscalIntegration\\EpsonFP90IIISample** i lageret til [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (f.eks. [eksemplet i frigivelse/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/EpsonFP90IIISample)). Eksemplet [består](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) af en regnskabsdokumentudbyder, som er en udvidelse af Commerce Runtime (CRT), og en regnskabsconnector, som er en udvidelse af Commerce Hardware Station. Yderligere oplysninger om, hvordan du bruger Retail SDK, finder du i [Retail SDK-arkitekturen](../dev-itpro/retail-sdk/retail-sdk-overview.md) og [Konfigurere en build-pipeline til uafhængige SDK-pakker](../dev-itpro/build-pipeline.md).

> [!WARNING]
> På grund af begrænsningerne ved den [nye uafhængige pakke- og udvidelsesmodel](../dev-itpro/build-pipeline.md) kan den ikke aktuelt bruges til dette eksempel på regnskabsintegration. Du skal bruge den tidligere version af Retail SDK på en virtuel maskine til udviklere (VM) i Microsoft Dynamics Lifecycle Services (LCS). Du kan få flere oplysninger i [Retningslinjer for installation af eksempel på integration af bonprinter i Italien (ældre)](emea-ita-fpi-sample-sdk.md).
>
> Understøttelse af den nye uafhængige pakke- og udvidelsesmodel til eksempler på regnskabsintegration er planlagt til senere versioner.

Fuldfør trinnene til opsætning af regnskabsintegration som beskrevet i [Konfigurere regnskabsintegration for Commerce-kanaler](setting-up-fiscal-integration-for-retail-channel.md).

1. [Konfigurer en regnskabsregistreringsproces](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Du skal også notere dig indstillingerne for den regnskabsregistreringsproces, der er [specifik for dette eksempel på integration af bonprinter](#set-up-the-registration-process).
1. [Oprette regnskabstekster for rabatter](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-texts-for-discounts).
1. [Angive indstillinger for fejlhåndtering](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Oprette X/Z-regnskabsrapporter fra POS](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos).
1. [Aktiver manuel udførelse af udsatte regnskabsregistreringer](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Konfigurer funktionaliteten til administration af kundeoplysninger i POS](emea-ita-customer-information.md#setup).
1. [Konfigurere kanalkomponenter](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Konfigurere registreringsprocessen

Hvis du vil aktivere registreringsprocessen, skal du følge disse trin for at konfigurere Commerce Headquarters. Du kan finde flere oplysninger i [Konfigurere regnskabsintegration for Commerce-kanaler](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Download konfigurationsfiler for regnskabsconnectoren og regnskabsdokumentudbyderen:

    1. Åbn lageret il [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions/).
    1. Vælg en korrekt version af frigivelsesafdelingen i overensstemmelse med din SDK/programversion (f.eks. **[release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Åbn **src \> FiscalIntegration \> EpsonFP90IIISample**.
    1. Hent konfigurationsfilen til regnskabsdokumentudbyderen på **CommerceRuntime \> DocumentProvider.EpsonFP90IIISample \> Configuration \> DocumentProviderEpsonFP90IIISample.xml** (for eksempel [filen til frigivelse/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/EpsonFP90IIISample/CommerceRuntime/DocumentProvider.EpsonFP90IIISample/Configuration/DocumentProviderEpsonFP90IIISample.xml)).
    1. Hent konfigurationsfilen til regnskabsconnectoren på **HardwareStation \> EpsonFP90IIIFiscalDeviceSample \> Configuration \> ConnectorEpsonFP90IIISample.xml** (for eksempel [filen til frigivelse/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/EpsonFP90IIISample/HardwareStation/EpsonFP90IIIFiscalDeviceSample/Configuration/ConnectorEpsonFP90IIISample.xml).

    > [!WARNING]
    > På grund af begrænsningerne ved den [nye uafhængige pakke- og udvidelsesmodel](../dev-itpro/build-pipeline.md) kan den ikke aktuelt bruges til dette eksempel på regnskabsintegration. Du skal bruge den tidligere version af Retail SDK på en virtuel maskine til udviklere i LCS. Konfigurationsfilerne til dette eksempel på regnskabsintegration findes i følgende mapper i Retail SDK på en udvikler VM i LCS:
    >
    > - **Konfigurationsfilen til regnskabsdokumentudbyder:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extension.DocumentProvider.EpsonFP90IIISample\\Configuration\\DocumentProviderEpsonFP90IIISample.xml
    > - **Konfigurationsfil til regnskabsconnector:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.EpsonFP90IIIFiscalDeviceSample\\Configuration\\ConnectorEpsonFP90IIISample.xml
    > 
    > Understøttelse af den nye uafhængige pakke- og udvidelsesmodel til eksempler på regnskabsintegration er planlagt til senere versioner.

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

- **Tilknytning af betalingsmiddeltype** – Tilknytning af betalingsmetoder, der er konfigureret for butikken, til betalingstyper, som bonprinteren understøtter. I følgende eksempel vises standardtilknytningen.

    ```JSON
    {"PaymentMethods": [
        {"StorePaymentMethod":"1", "PrinterPaymentType":"0", "PrinterPaymentIndex":"00"},
        {"StorePaymentMethod":"3", "PrinterPaymentType":"2", "PrinterPaymentIndex":"00"},
        {"StorePaymentMethod":"4", "PrinterPaymentType":"2", "PrinterPaymentIndex":"01"},
        {"StorePaymentMethod":"6", "PrinterPaymentType":"0", "PrinterPaymentIndex":"01"},
        {"StorePaymentMethod":"8", "PrinterPaymentType":"6", "PrinterPaymentIndex":"01"}
        ],
        "DepositPaymentMethod": {"PrinterPaymentType":"2", "PrinterPaymentIndex":"00"}}
    ```

    Her er en forklaring på attributterne i denne tilknytning:

    - **StorePaymentMethod** er en betalingsmåde, der er oprettet for butikken i **Retail og Commerce \> Konfiguration af kanal \> Betalingsmetoder \> Betalingsmetoder**.
    - **PrinterPaymentType** og **PrinterPaymentIndex** er den tilsvarende betalingstype og -indeks, der er defineret i bonprinterdokumentationen til Epson.
    - **DepositPaymentMethod** bruges til at angive en printers betalingstype og indeks for den del af kundeordrens afhentningsbeløb, der udlignes med indbetalingen til kundeordren.

    Følgende tabel viser eksempeltilknytningen af betalingsmetoder svarer til de butiksbetalingsmetoder, der er konfigureret i standarddemodataene.

    | Betalingsmetode | Navn på betalingsmetode |
    |----------------|---------------------|
    | 1              | Indløsning                |
    | 3              | Kort                |
    | 4              | Debitorkonto    |
    | 6              | Valuta            |
    | 8              | Gavekort           |

    Du skal redigere eksempeltilknytningen i overensstemmelse med de betalingsmetoder, der er konfigureret i dit program.

- **Stregkodetype for kvitteringsnummer** – Den type stregkode, der bruges til at vise et kvitteringsnummer på en regnskabskvittering. Standardværdien er **CODE128**.
- **Udskriv regnskabsdata i kvitteringshoved** – Hvis denne parameter er aktiveret, udskrives der butiksoplysninger på regnskabskvitteringen. Disse oplysninger omfatter butikkens navn, adresse og momsidentifikationsnummer samt kassererens navn.
- **Tilknytning af bonprinterafdeling** – Tilknytning af afdelinger for bonprinteren til momssatser, momsfritagelsesarter og produkttyper. I følgende eksempel vises standardtilknytningen.

    ```JSON
    {"Departments": [
        {"VATRate":"2200", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"01"},
        {"VATRate":"2200", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"02"},
        {"VATRate":"1000", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"03"},
        {"VATRate":"1000", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"04"},
        {"VATRate":"0500", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"05"},
        {"VATRate":"0500", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"06"},
        {"VATRate":"0400", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"07"},
        {"VATRate":"0400", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"08"},
        {"VATRate":"0000", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"09"},
        {"VATRate":"0000", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"10"},
        {"VATRate":"0000", "VATExemptNature":"NS", "ProductType":"0", "DepartmentNumber":"99"}]}
    ```

    Her er en forklaring på attributterne i denne tilknytning:

    - **VATRate** er en understøttet momssats, der er konfigureret som en momskode. Værdien i tilknytningen har to decimaler, men ingen decimalseparator. For eksempel repræsenterer **2200** 22 procent, og **1000** repræsenterer 10 procent.
    - **VATExemptNature** gælder kun i tilfælde, hvor momssatsen er 0 (nul), inklusive tilfælde, hvor der ikke er nogen moms. I øjeblikket understøttes **VATExemptNature** kun for gavekort, og værdien i tilknytningen skal svare til værdien af egenskaben **VATExemptNatureForGiftCard** i XML-konfigurationsfilen.
    - **ProductType** er produkttypen. En værdi på **0** repræsenterer varer, og en værdi på **1** angiver servicer.
    - **DepartmentNumber** er nummeret på den afdeling, der er konfigureret i printeren, og som svarer til de foregående tre attributter.

    Du skal redigere eksempeltilknytningen i overensstemmelse med de momssatser, der er konfigureret i dit program, og de tilsvarende afdelinger, der er konfigureret i bonprinteren.

- **Momsfritagelsestype for gavekort** – Den momsfritagelsestype, der skal anvendes ved udstedelse eller genopfyldning af et gavekort. Værdien skal svare til en post i bonprinterafdelingens tilknytning. Standardværdien er **NS**.
- **Aktivér gratis varer** – Hvis denne parameter er aktiveret, er den særlige *omaggio*-rabatjusteringstype for varer, der har en rabat på 100 %, aktiveret.
- **Infokode for returoprindelse** – Den infokode, der bruges til at hente oprindelsen af en returtransaktion, hvis der ikke er leveret en oprindelig salgskvittering. Denne parameter bruges sammen med parametrene **Infokode for oprindelig salgsdato** og **Tilknytning af returoprindelse** til at generere en korrekt meddelelse i regnskabskvitteringen om oprindelsen af en returtransaktion, hvis der ikke findes nogen oprindelig salgstransaktion. 

    Denne infokode skal konfigureres, så brugeren kan vælge eller angive en af de mulige oprindelser for returneringer i dine butikker. Den kan f.eks. konfigureres som en liste over underkoder (f.eks. **Returner fra site** eller **Return fra kiosk**). Parameteren **Tilknytning af returoprindelse** bruges derefter til at oversætte værdien af infokoden til en kommando for bonprinteren.

    Den infokode, der er valgt for **Infokode for returoprindelse**, skal konfigureres som en obligatorisk infokode, der udløses én gang pr. salgstransaktion. Den skal tildeles som infokoden **Returnprodukt** i POS-funktionalitetsprofilen, så den udløses, når handlingen **Returprodukt** køres.

    Der er ikke angivet en standardværdi for denne tilknytning. Du skal vælge en infokode, der er konfigureret i programmet.

- **Infokode for oprindelig salgsdato** – Den infokode, der bruges til at hente oprindelig salgsdato for en returtransaktion, hvis der ikke er leveret en oprindelig salgskvittering. Denne parameter bruges sammen med parametrene **Infokode for returoprindelse** og **Tilknytning af returoprindelse** til at generere en korrekt meddelelse i regnskabskvitteringen om oprindelsen af en returtransaktion, hvis der ikke findes nogen oprindelig salgstransaktion.

    Infokoden skal konfigureres, så feltet **Input-type** angives til **Dato**. Den skal konfigureres som en obligatorisk infokode, der udløses én gang pr. salgstransaktion. Den skal også tildeles som **Sammenkædet infokode** for den infokode, der er valgt for parameteren **Infokode for returoprindelse**, så de to infokoder udløses efter hinanden.

    Der er ikke angivet en standardværdi for denne tilknytning. Du skal vælge en infokode, der er konfigureret i programmet.

- **Tilknytning af returoprindelse** – Tilknytning af returoprindelser, der bruges til at udskrive oprindelsen af en returtransaktion, hvis der ikke er leveret en oprindelig salgskvittering. Denne parameter bruges sammen med parametrene **Infokode for returoprindelse** og **Infokode for oprindelig salgsdato** til at generere en korrekt meddelelse i regnskabskvitteringen om oprindelsen af en returtransaktion, hvis der ikke findes nogen oprindelig salgstransaktion. I følgende eksempel vises standardtilknytningen.

    ```JSON
    {"ReturnOrigins": [
        {"ReturnOrigin":"1", "PrinterReturnOrigin":"POS"},
        {"ReturnOrigin":"2", "PrinterReturnOrigin":"ND"}
        ],
        "PrinterReturnOriginWithoutFiscalData":"POS"}
    ```

    Her er en forklaring på attributterne i denne tilknytning:

    - **ReturnOrigin** er en af de mulige oprindelser for returneringer i dine butikker. Værdien skal svare til en værdi af parameteren **Infokode for returoprindelse**.
    - **PrinterReturnOrigin** er en af de returoprindelser, som bonprinteren accepterer (**POS**, **VR** eller **ND**).
    - **PrinterReturnOriginWithoutFiscalData** er den returoprindelse, som bonprinteren accepterer, og som svarer til en returtransaktion, der er knyttet til en oprindelig salgstransaktion, der ikke har tilknyttede regnskabsdata, fordi den ikke er registreret via en bonprinter. I dette tilfælde identificeres den oprindelige salgsdato som datoen for den oprindelige salgstransaktion.

Følgende standarddatatilknytninger er forældede og bevares kun til bagudkompatibilitet:

- Momskodetilknytning
- Bankindbetalingstype

#### <a name="fiscal-connector-settings"></a>Indstillinger af regnskabsconnector

Følgende indstillinger er inkluderet i konfigurationen af regnskabsconnectoren som en del af eksemplet på regnskabsintegration:

- **Slutpunktadresse** – Printerens URL-adresse.
- **Dato- og tidssynkronisering** – En værdi, der angiver, om datoen og klokkeslættet for printeren skal synkroniseres med den tilknyttede hardwarestation.

### <a name="configure-channel-components"></a>Konfigurere kanalkomponenter

> [!WARNING]
> På grund af begrænsningerne ved den [nye uafhængige pakke- og udvidelsesmodel](../dev-itpro/build-pipeline.md) kan den ikke aktuelt bruges til dette eksempel på regnskabsintegration. Du skal bruge den tidligere version af Retail SDK på en virtuel maskine til udviklere i LCS. Du kan få flere oplysninger i [Retningslinjer for installation af eksempel på integration af bonprinter i Italien (ældre)](emea-ita-fpi-sample-sdk.md).
>
> Understøttelse af den nye uafhængige pakke- og udvidelsesmodel til eksempler på regnskabsintegration er planlagt til senere versioner.

#### <a name="set-up-the-development-environment"></a>Konfigurere udviklingsmiljøet

Følg disse trin for at konfigurere et udviklingsmiljø, så du kan teste og udvide eksemplet.

1. Klon eller download lageret til [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions). Vælg en korrekt version af frigivelsesafdelingen i overensstemmelse med din SDK/programversion. Yderligere oplysninger finder du i [Hente Retail SDK-eksempler og -referencepakker fra GitHub og NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Åbn løsningen til integration af bonprinter på **Dynamics365Commerce.Solutions\\FiscalIntegration\\EpsonFP90IIISample\\EpsonFP90IIISample.sln**, og opbyg den.
1. Installer CRT-udvidelser:

    1. Find installationsprogrammet til CRT-udvidelsen:

        - **Commerce Scale Unit:** I mappen **EpsonFP90IIISample\\ScaleUnit\\ScaleUnit.EpsonFP90III.Installer\\bin\\Debug\\net461** skal du finde installationsprogrammet **ScaleUnit.EpsonFP90III.Installer**.
        - **Lokal CRT på Modern POS:** I mappen **EpsonFP90IIISample\\ModernPOS\\ModernPOS.EpsonFP90III.Installer\\bin\\Debug\\net461** skal du finde installationsprogrammet **ModernPOS.EpsonFP90III.Installer**.

    1. Start installationsprogrammet til CRT-udvidelsen fra kommandolinjen:

        - **Commerce Scale Unit:**

            ```Console
            ScaleUnit.EpsonFP90III.Installer.exe install --verbosity 0
            ```

        - **Lokal CRT på Modern POS:**

            ```Console
            ModernPOS.EpsonFP90III.Installer.exe install --verbosity 0
            ```

1. Installer udvidelser til Hardwarestation:

    1. I mappen **EpsonFP90IIISample\\HardwareStation\\HardwareStation.EpsonFP90III.Installer\\bin\\Debug\\net461** skal du finde installationsprogrammet **HardwareStation.EpsonFP90III.Installer**.
    1. Start installationsprogrammet til udvidelsen fra kommandolinjen:

        ```Console
        HardwareStation.EpsonFP90III.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Produktionsmiljø

Følg trinnene i [Konfigurere en build-pipeline til et eksempel på regnskabsintegration](fiscal-integration-sample-build-pipeline.md) for at generere og frigive Cloud Scale Unit og pakker, der kan implementeres med selvbetjening, til eksemplet på regnskabsintegration. **EpsonFP90III build-pipeline.yml**-skabelonens YAML-fil findes i mappen **Pipeline\\YAML_Files** i lageret til [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions).

## <a name="design-of-extensions"></a>Design af udvidelser

Bonprinterintegrationens eksempel til Italien er baseret på [funktionaliteten af regnskabsintegration](fiscal-integration-for-retail-channel.md) og er en del af Retail SDK. Eksemplet findes i mappen **src\\FiscalIntegration\\EpsonFP90IIISample** i lageret til [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (f.eks. [eksemplet i frigivelse/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/EpsonFP90IIISample)). Eksemplet [består](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) af en regnskabsdokumentudbyder, som er en udvidelse af CRT, og en regnskabsconnector, som er en udvidelse af Commerce Hardware Station. Yderligere oplysninger om, hvordan du bruger Retail SDK, finder du i [Retail SDK-arkitekturen](../dev-itpro/retail-sdk/retail-sdk-overview.md) og [Konfigurere en build-pipeline til uafhængige SDK-pakker](../dev-itpro/build-pipeline.md).

> [!WARNING]
> På grund af begrænsningerne ved den [nye uafhængige pakke- og udvidelsesmodel](../dev-itpro/build-pipeline.md) kan den ikke aktuelt bruges til dette eksempel på regnskabsintegration. Du skal bruge den tidligere version af Retail SDK på en virtuel maskine til udviklere i LCS. Du kan få flere oplysninger i [Retningslinjer for installation af eksempel på integration af bonprinter i Italien (ældre)](emea-ita-fpi-sample-sdk.md). Understøttelse af den nye uafhængige pakke- og udvidelsesmodel til eksempler på regnskabsintegration er planlagt til senere versioner.

### <a name="commerce-runtime-extension-design"></a>Design af Commerce Runtime-udvidelse

Formålet med udvidelsen, som er en udbyder af regnskabsdokumenter, er at generere printerspecifikke dokumenter og håndtere svar fra bonprinteren.

#### <a name="request-handler"></a>Anmodningshandler

Anmodningshandleren **DocumentProviderEpsonFP90III** er indganspunktet for anmodningen om at generere dokumenter fra bonprinteren.

Denne handler er nedarvet fra brugergrænsefladen i **INamedRequestHandler**. Metoden **HandlerName** er ansvarlig for at returnere navnet på handleren. Navnet på handleren skal svare til navnet på connector-dokumentudbyderen, der er angivet i Commerce Headquarters.

Connectoren understøtter følgende anmodninger:

- **GetFiscalDocumentDocumentProviderRequest** – Denne anmodning indeholder oplysninger om, hvilket dokument der skal genereres. Den returnerer et printerspecifikt dokument, der skal registreres i bonprinteren.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Denne anmodning returnerer listen over hændelser, der skal abonneres på. Aktuelt understøttes følgende hændelser: salg, udskrivning af X-rapport og udskrivning af Z-rapport.

#### <a name="configuration"></a>Konfiguration

Konfigurationsfilen til regnskabsdokumentudbyderen er placeret i **src\\FiscalIntegration\\EpsonFP90IIISample\\CommerceRuntime\\DocumentProvider.EpsonFP90IIISample\\Configuration\\DocumentProviderEpsonFP90IIISample.xml** i lageret til [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Formålet med filen er at aktivere indstillinger for dokumentudbyderen, der skal konfigureres fra Commerce Headquarters. Filformatet er tilpasset kravene til konfiguration af regnskabsintegration.

### <a name="hardware-station-extension-design"></a>Design af hardwarestationsudvidelse

Formålet med den forlængelse, der er en regnskabsmæssig connector, er at kommunikere med bonprinteren. Denne udvidelse bruger HTTP-protokollen til at sende dokumenter, som CRT-udvidelsen genererer til bonprinteren. Den håndterer også de svar, der er modtaget fra bonprinteren.

#### <a name="request-handler"></a>Anmodningshandler

Anmodningshandleren **EpsonFP90IIISample** er indgangspunktet for håndtering af anmodning til den eksterne regnskabsenhed.

Denne handler er nedarvet fra brugergrænsefladen i **INamedRequestHandler**. Metoden **HandlerName** er ansvarlig for at returnere navnet på handleren. Navnet på handleren skal svare til navnet på den regnskabsconnector, der er angivet i Commerce Headquarters.

Connectoren understøtter følgende anmodninger:

- **SubmitDocumentFiscalDeviceRequest** – Denne anmodning sender dokumenter til printere og returnerer svar fra bonprinteren.
- **IsReadyFiscalDeviceRequest** – Denne anmodning bruges til tilstandskontrol af enheden.
- **InitializeFiscalDeviceRequest** – Denne anmodning bruges til at initialisere printeren.

#### <a name="configuration"></a>Konfiguration

Konfigurationsfilen til regnskabsconnectoren er placeret i **src\\FiscalIntegration\\EpsonFP90IIISample\\HardwareStation\\EpsonFP90IIIFiscalDeviceSample\\Configuration\\ConnectorEpsonFP90IIISample.xml** i lageret for [Dynamics 365 Commerce-løsninger](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Formålet med filen er at aktivere indstillinger for connectoren, der skal konfigureres fra Commerce Headquarters. Filformatet er tilpasset kravene til konfiguration af regnskabsintegration.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
