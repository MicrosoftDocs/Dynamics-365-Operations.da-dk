---
title: Konfigurere regnskabsintegration for Commerce-kanaler
description: Denne artikel indeholder retningslinjer for opsætning af regnskabsintegrationsfunktionen for Commerce-kanaler.
author: EvgenyPopovMBS
ms.date: 10/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 28097341c7b39660b834eb81786c3f56045e1496
ms.sourcegitcommit: 2bc6680dc6b12d20532d383a0edb84d180885b62
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/06/2022
ms.locfileid: "9631417"
---
# <a name="set-up-the-fiscal-integration-for-commerce-channels"></a>Konfigurere regnskabsintegration for Commerce-kanaler

[!include [banner](../includes/banner.md)]

Denne artikel indeholder retningslinjer for opsætning af regnskabsintegrationsfunktionen for Commerce-kanaler. Du kan finde flere oplysninger om regnskabsintegrationen i [Oversigt over regnskabsintegration for Commerce-kanaler](fiscal-integration-for-retail-channel.md).

## <a name="enable-features-in-commerce-headquarters"></a>Aktivere funktionen i Commerce Headquarters

Hvis du vil aktivere funktioner, der er relateret til funktioner til regnskabsintegration for handelskanaler, skal du følge disse trin.

1. I Commerce headquarters skal du gå til **Systemadministration \> Arbejdsområder \> Funktionsstyring**.
1. Find og aktiver følgende funktioner:

    - **Direkte regnskabsintegration fra kasseapparater** – Denne funktion udvider struktur for regnskabsintegration ved at tilføje funktionen til oprettelse af regnskabsforbindelser, der vil blive kørt i POS. Denne type connector kommunikerer med en finansiel enhed eller tjeneste, der indeholder en API (HTTP Application Programming Interface), og kræver ikke en dedikeret fysisk maskine i butikken. Denne funktionalitet giver f.eks. mulighed for skattemæssig integration for mobile enheder uden at kræve delt hardwarestation.
    - **Tilsidesættelser af teknisk profil for regnskabsintegration** – Denne funktion gør det muligt at udvide konfigurationen af regnskabsintegration og tilføjer muligheden for at tilsidesætte parametre for en teknisk profil. Det er f.eks. muligt at angive forbindelsesstrenge til regnskabsenhed på individuelt POS-niveau. Denne funktion giver også mulighed for at kontrollere forbindelsesparametrene på siden **Indstillinger** på POS. 
    - **Regnskabsregistreringstilstand for POS-registre** – Når denne funktion er aktiveret, kan du deaktivere processen til regnskabsregistrering for bestemte POS-registre. Hvis regnskabsregistrering er deaktiveret for et POS-register, kan salgstransaktioner ikke fuldføres på det pågældende kasseapparat.
    - **Sikkerhedskopiering af lokallager for regnskabsmæssig integration** – Denne funktion udvider fejlhåndteringskapaciteter i regnskabsintegrationsstrukturen ved at aktivere automatisk sikkerhedskopiering af regnskabsregistreringsdataene, så data i det lokale lager kan gendannes, når en enhed aktiveres.
    - **Udskudt registrering af dokumenter** – Denne funktion udvider egenskaberne til håndtering af fejl i struktur for regnskabsintegration ved at gøre det muligt at udskyde regnskabsregistrering, hvis der opstår fejl i en regnskabsregistrering, og bruge en indstilling til sikkerhedskopiering af regnskabsregistrering eller fuldføre regnskabsregistrering senere på anden måde end regnskabsintegrationsstruktur.

## <a name="set-up-commerce-parameters"></a>Konfigurere Commerce-parametre

Følg disse trin for at konfigurere Commerce-parametre.

1. På siden **Delte parametre for Commerce** under fanen **Generelt** skal du vælge **Ja** i indstillingen **Aktivér regnskabsintegration**.
1. Definer nummerserierne for følgende referencer under fanen **Nummerserier**:

    - Regnskabsteknisk profilnummer
    - Regnskabsconnectorgruppenummer
    - Registreringsprocesnummer

1. Definer nummerserien for regnskabsfunktionens profilnummer på siden **Commerce-parametre**.

> [!NOTE]
> Nummerserier er valgfrie. Der kan genereres numre til alle regnskabsintegrationsenheder fra nummerserier eller manuelt.

## <a name="set-up-a-fiscal-registration-process"></a>Konfigurer en regnskabsregistreringsproces

Regnskabsintegrationsprocessen består af følgende opgaver:

- Konfigurer regnskabsconnectorer, som repræsenterer regnskabsenheder eller -tjenester, der bruges til regnskabsmæssige registreringsformål, f.eks. bonprintere.
- Konfigurer udbydere af dokumenter, der opretter regnskabsdokumenter, som bliver registreret i regnskabsenheder eller -tjenester ved hjælp af regnskabsconnectorer.
- Konfigurer regnskabsregistreringsprocessen, der definerer en række trin i regnskabsregistreringen og regnskabsconnectorer og regnskabsdokumentudbydere, der bruges til hvert trin.
- Tildel regnskabsregistreringsprocessen til POS-funktionalitetsprofiler.
- Tildel tekniske connectorprofiler til hardwareprofiler.
- Tildel tekniske connectorprofiler til POS-hardware- eller funktionalitetsprofiler.

### <a name="upload-configurations-of-fiscal-document-providers"></a>Uploade konfigurationer af regnskabsdokumentudbydere

En regnskabsdokumentudbyder er ansvarlig for at generere regnskabsdokumenter, der repræsenterer transaktioner og -hændelser, der er registreret på POS i et format, der også bruges til interaktion med en regnskabsenhed eller -tjeneste. F.eks. kan en udbyder af regnskabsdokumenter generere en repræsentation af en regnskabskvittering i et XML-format.

Følg disse trin for at uploade konfigurationer af regnskabsdokumentudbydere.

1. Gå i Commerce Headquarters til siden **Udbydere af regnskabsdokumenter** (**Retail og Commerce \> Konfiguration af kanal \> Regnskabsintegration \> Udbydere af regnskabsdokumenter**).
1. Upload en XML-konfiguration for hver enhed eller tjeneste, du vil bruge.

> [!TIP]
> Vælg **Vis** for at få vist alle funktionelle profiler, der er relateret til den aktuelle udbyder af regnskabsdokumenter.

> [!NOTE]
> Datatilknytning betragtes som en del af en regnskabsdokumentudbyder. Hvis du vil oprette andre datatilknytninger for samme connector (som f.eks. specifik lovgivning), skal du oprette forskellige regnskabsdokumentudbydere.

### <a name="upload-configurations-of-fiscal-connectors"></a>Uploade konfigurationer af regnskabsconnectorer

En regnskabsconnector er ansvarlig for kommunikationen med en regnskabsenhed eller -tjeneste. En regnskabsconnector kan for eksempel sende en regnskabskvittering, som en regnskabsdokumentudbyder har oprettet i et XML-format, til en bonprinter. Du kan finde flere oplysninger om regnskabsintegrationskomponenter i [Regnskabsregistreringsprocessen og eksempler på regnskabsintegration for regnskabsenheder og -tjenester](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

Følg disse trin for at uploade konfigurationer af regnskabsconnectorer.

1. Gå i Commerce Headquarters til siden **Regnskabsconnectorer** (**Retail og Commerce \> Konfiguration af kanal \> Regnskabsintegration \> Regnskabsconnectorer**).
1. Upload en XML-konfiguration for hver enhed eller tjeneste, du vil bruge til regnskabsintegration.

> [!TIP]
> Vælg **Vis** for at få vist alle funktionelle og tekniske profiler, der er relateret til den aktuelle regnskabsconnector.

Du kan finde eksempler på konfigurationer af regnskabsconnectorer og regnskabsdokumentudbydere i [Eksempler på regnskabsintegration i Commerce SDK](fiscal-integration-for-retail-channel.md#fiscal-integration-samples-in-the-commerce-sdk).

### <a name="create-connector-functional-profiles"></a>Oprette funktionelle profiler for connector

Opret funktionelle connectorprofiler ved at følge disse trin.

1. Gå i Commerce Headquarters til siden **Funktionelle profiler for connector** (**Retail og Commerce \> Konfiguration af kanal \> Regnskabsintegration \> Funktionelle profiler for connector**).
1. For hver kombination af regnskabsconnector og regnskabsdokumentudbyder, der er relateret til denne regnskabsconnector, skal du oprette en funktionel connectorprofil ved at følge disse trin:

    1. Vælg et connectornavn.
    1. Vælg en dokumentudbyder.

#### <a name="change-data-mapping-parameters-in-a-connector-functional-profile"></a>Ændre parametrene for datatilknytning i en funktionel connectorprofil

Du kan ændre parametrene for datatilknytning i en funktionel connectorprofil. Følgende tabel indeholder nogle eksempler på parametre for datatilknytning i en funktionel connectorprofil.

| Parameter | Formater | Eksempel |
|-----------|--------|---------|
| Indstillinger for momssats | værdi : VATrate | 1 : 2000, 2 : 1800 |
| Tilknytning af momskoder | VATcode : værdi | vat20 : 1, vat18 : 2 |
| Tilknytning af betalingsmiddeltyper | TenderType : værdi | Kontant : 1, Kort : 2 |

Hvis du vil gendanne de standardparametre, der er defineret i konfigurationen af regnskabsdokumentudbyderen, skal du vælge **Opdater** på siden **Funktionelle profiler for connector**.

> [!NOTE]
> Funktionelle connectorprofiler er firmaspecifikke. Hvis du planlægger at bruge den samme kombination af regnskabsconnector og regnskabsdokumentudbyder til forskellige firmaer, skal du oprette en funktionel connectorprofil for hvert firma.

### <a name="create-connector-technical-profiles"></a>Oprette tekniske profiler for connector

Opret tekniske connectorprofiler ved at følge disse trin.

1. Gå i Commerce Headquarters til siden **Tekniske profiler for connector** (**Retail og Commerce \> Konfiguration af kanal \> Regnskabsintegration \> Tekniske profiler for connector**).
1. Opret en teknisk profil for connector til hver regnskabsconnector ved at følge disse trin:

    1. Vælg et connectornavn.
    1. Vælg en connectortype:

        - For enheder eller tjenester, der er tilsluttet en hardwarestation eller som findes på det lokale netværk, skal du vælge **Lokal**.
        - For eksterne tjenester skal du vælge **Ekstern**.
        - For interne connectorer i Commerce Runtime (CRT) skal du vælge **Intern**. 

    1. Vælg en connectorlokation:

        - Hvis connectoren er placeret på hardwarestationen, skal du vælge **Hardwarestation**.
        - Hvis connectoren er placeret på kasseapparatet, skal du vælge **Kasseapparat**.

Parametrene under fanerne **Enhed** og **Indstillinger** i en teknisk connectorprofil kan ændres. Hvis du vil gendanne de standardparametre, der er defineret i konfigurationen af regnskabsconnectoren, skal du vælge **Opdater**. Mens der indlæses en ny version af en XML-konfigurationenl, modtager du en meddelelse om, at den aktuelle regnskabsconnector eller regnskabsdokumentudbyder allerede bruges. Denne procedure tilsidesætter ikke manuelle ændringer, der tidligere er foretaget i funktionelle connectorprofiler og tekniske connectorprofiler. Hvis du vil anvende standardsættet af parametre fra en ny konfiguration, skal du vælge **Opdater** på siden **Funktionelle profiler for connector** eller siden **Tekniske profiler for connector**.

Hvis du skal konfigurere specifikke parametre for et enkelt kasseapparat eller en enkelt butik, skal du følge disse trin.

1. Vælg menupunktet **Tilsidesæt**.
1. Opret en ny post på siden **Tilsidesæt**.
1. Vælg en butik eller et kasseapparat. Du kan tilsidesætte parametre for den valgte tekniske profil for et enkelt kasseapparat eller alle kasseapparater i en enkelt butik.
1. Angiv parametre for det valgte kasseapparat eller den valgte butik under fanen **Enhed**.

### <a name="create-fiscal-connector-groups"></a>Oprette regnskabsconnectorgrupper

En regnskabsconnectorgruppe kombinerer funktionelle profiler for regnskabsconncetorer, der udfører samme funktioner og bruges på samme trin i en regnskabsregistreringsproces. Hvis der eksempelvis kan bruges forskellige bonprintermodeller i en butik, kan regnskabsconnectorer for disse bonprintere kombineres i en regnskabsconnectorgruppe.

Følg disse trin for at oprette en regnskabsconnectorgruppe.

1. Gå til siden **Regnskabsconnectorgruppe** (**Retail og Commerce \> Konfiguration af kanal \> Regnskabsintegration \> Regnskabsconnectorgrupper**).
1. Opret en ny regnskabsconnectorgruppe.
1. Tilføj funktionelle profiler til connectorgruppen. Vælg **Tilføj** under fanen **Funktionsprofiler**, og vælg et profilnummer. I en connectorgruppe kan hver regnskabsconnector kun have én funktionel profil.
1. Hvis du vil afbryde brugen af den funktionelle profil, kan du indstille **Deaktiver** til **Ja**. Denne ændring påvirker kun den aktuelle connectorgruppe. Du kan fortsætte med at bruge den samme funktionelle profil i andre connectorgrupper.

### <a name="create-a-fiscal-registration-process"></a>Oprette en regnskabsregistreringsproces

En regnskabsregistreringsproces defineres af rækkefølgen af trinnene i registreringen og den connectorgruppe, der bruges i hvert trin.

Følg disse trin for at oprette en regnskabsregistreringsproces.

1. Gå i Commerce Headquarters til siden **Regnskabsregistreringsproces** (**Retail og Commerce \> Konfiguration af kanal \> Regnskabsintegration \> Regnskabsregistreringsprocesser**).
1. Opret en ny post for hver entydig regnskabsregistreringsproces.
1. Føj registreringstrin til processen ved at følge disse trin:

    1. Vælg **Tilføj**.
    1. Vælg en regnskabsconnectortype.
    1. I feltet **Gruppenummer** skal du vælge en passende regnskabsconnectorgruppe.

### <a name="assign-entities-of-the-fiscal-registration-process-to-pos-profiles"></a>Tildele enheder i regnskabsregistreringsprocessen til POS-profiler

Tildel enheder i regnskabsregistreringsprocessen til POS-profiler ved at følge disse trin.

1. Gå i Commerce Headquarters til siden **POS-funktionalitetsprofiler** (**Retail og Commerce \> Konfiguration af kanal \> POS-opsætning \> POS-profiler \> Funktionalitetsprofiler**). 
1. Tildel regnskabsregistreringsprocessen til POS-funktionalitetsprofilen.
1. Vælg **Rediger**, og vælg en proces under fanen **Proces for regnskabsregistrering** i feltet **Procesnummer**.
1. Under fanen **Regnskabsservices** skal du vælge connector-tekniske profiler med connectorplaceringen **Kasseapparat**.
1. Gå til siden **POS-hardwareprofil** (**Retail og Commerce \> Konfiguration af kanal \> POS-opsætning \> POS-profiler \> Hardwareprofiler**).
1. Tildel tekniske connectorprofiler til en hardwareprofil. 
1. Vælg **Rediger**, og tilføj derefter en linje under fanen **Eksterne regnskabsenheder**. 
1. Vælg en teknisk connectorprofil i feltet **Profilnummer**.
1. Under fanen **Eksterne regnskabsenheder** skal du vælge connector-tekniske profiler med connectorplaceringen **Hardwarestation**.

> [!NOTE]
> Du kan føje flere tekniske profiler til en den samme hardwareprofil. Men en hardwareprofil eller POS-funktionalitetsprofil skal kun have ét skæringspunkt med en regnskabsconnectorgruppe.

Regnskabsregistreringsflowet defineres af regnskabsregistreringsprocessen og også af nogle af parametrene for regnskabsintegrationskomponenter: CRT-udvidelsen for udbyderen af regnskabsdokumenter og Hardwarestation-udvidelsen for regnskabsconnectoren.

- Abonnementet på hændelser og transaktioner til regnskabsregistrering er foruddefineret i regnskabsdokumentudbyderen.
- Udbyderen af regnskabsdokumenter er også ansvarlig for at identificere den regnskabsconnector, der bruges til regnskabsregistrering. Den sammenligner de funktionelle connectorprofiler, der indgår i den regnskabsconnectorgruppe, der er angivet for det aktuelle trin i regnskabsregistreringsprocessen, med den tekniske connectorprofil, der er tildelt til hardwareprofilen for den hardwarestation, der hører sammen med POS.
- Udbyderen af regnskabsdokumenter bruger indstillingerne for datatilknytning fra konfigurationen af regnskabsdokumentudbyderen til at konvertere transaktions-/hændelsesdata som f.eks. moms og betalinger, mens der oprettes et regnskabsdokument.
- Når regnskabsdokumentudbyderen genererer et regnskabsdokument, kan regnskabs-connectoren enten sende det til regnskabsenheden, som det er, eller opdele det og omdanne det til en sekvens af kommandoer for enhedens API, afhængigt af den kommunikation, der håndteres.

### <a name="set-up-registers-with-fiscal-registration-restrictions"></a>Konfigurere kasseapparater med begrænsninger for regnskabsregistrering

Du kan vælge kasseapparater, hvor regnskabsregistrering ikke er tilladt, hvis du f.eks. kun skal levere ikke-regnskabsmæssige handlinger, f.eks. søgning i produktkatalog, kundeopslag eller oprettelse af transaktionskladde på disse enheder.

Følg disse trin for at konfigurere kasseapparater med begrænsninger for regnskabsregistrering.

1. Gå i Commerce Headquarters til **Retail og Commerce \> Konfiguration af kanal \> Regnskabsintegration \> Processer for regnskabsregistrering**.
1. Vælg den ønskede proces.
1. Vælg fanen **POS-kasseapparater med begrænsninger i regnskabsprocessen**.
1. Tilføj kasseapparater med begrænsninger i regnskabsprocessen efter behov.

### <a name="validate-the-fiscal-registration-process"></a>Validere processen til regnskabsregistrering

Det anbefales, at du validerer processen til regnskabsregistrering i følgende tilfælde:

- Du har fuldført alle indstillingerne for en ny registreringsproces. Disse indstillinger omfatter tildeling af registreringsprocesser til POS-funktionalitetsprofiler og hardwareprofiler.
- Du har ændret en eksisterende regnskabsregistreringsproces, og disse ændringer kan bevirke, at der vælges en anden regnskabsconnector under kørslen. (Du har f.eks. ændret connectorgruppen for et trin i en regnskabsregistreringsprocessen, aktiveret en funktionel profil for connectoren i en connectorgruppe eller tilføjet en ny funktionel connectorprofil i en connectorgruppe).
- Du har foretaget ændringer i tildelingen af tekniske connectorprofiler til hardwareprofiler.

Følg disse trin for at validere en regnskabsregistreringsproces.

1. Gå i Commerce Headquarters til siden **Regnskabsregistreringsproces** (**Retail og Commerce \> Konfiguration af kanal \> Regnskabsintegration \> Regnskabsregistreringsprocesser**).
1. Vælg **Valider** for at validere processen til regnskabsregistrering.
1. På siden **Distributionstidsplan** skal du køre jobbene **1070** og **1090** for at overføre data til kanaldatabasen.

## <a name="set-up-fiscal-texts-for-discounts"></a>Oprette regnskabstekster for rabatter

Der skal i nogle tilfælde udskrives en særlig tekst på en regnskabskvittering, hvis der anvendes en rabat. Du kan oprette regnskabstekster for rabatter på siden **Regnskabsconnectorgruppe** (**Retail og Commerce \> Konfiguration af kanal \> Regnskabsintegration \> Regnskabsconnectorgrupper**).

- For manuelle rabatter, der anvendes på POS, kan du konfigurere en regnskabstekst for den årsagskode eller årsagskodegruppe, der er angivet som **Produktrabat**-årsagskoden i POS-funktionalitetsprofilen.

    1. På siden **Regnskabsconnectorgruppe** skal du vælge **Tekst til regnskabskvittering**.
    1. Under fanen **Årsagskoder** skal du vælge **Tilføj** og vælg en årsagskode eller årsagskodegruppe.
    1. I feltet **Nummer på årsagskode** skal du vælge en værdi.
    1. I feltet **Underkodenummer** skal du vælge en værdi, hvis der kræves en underkode for den valgte årsagskode.
    1. I feltet **Tekst til regnskabskvittering** skal du angive en regnskabstekst, der skal udskrives på en regnskabskvittering.
    1. Vælg **Ja** i **Udskriv brugerinput på regnskabskvitteringen** for at tilsidesætte teksten på en regnskabskvittering og erstatte den med oplysninger, som en bruger angiver manuelt ved POS. Denne indstilling gælder kun for årsagskoder med inputtypen **Tekst**.

    > [!NOTE]
    > Du kan angive en regnskabstekst til flere årsagskoder for at understøtte scenarier, hvor årsagskodegrupper, tilknyttede årsagskoder og udløste årsagskoder bruges. I disse tilfælde indeholder regnskabskvitteringen regnskabstekster fra alle årsagskoder, der er knyttet til den posteringslinje, hvor rabatten blev anvendt.

- For kanalspecifikke rabatter skal du definere en regnskabstekst for rabat-id'et.

    1. På siden **Regnskabsconnectorgruppe** skal du vælge **Tekst til regnskabskvittering**.
    1. Under fanen **Rabatter** skal du vælge **Tilføj** og vælg et rabat-id.
    1. I feltet **Tekst til regnskabskvittering** skal du angive en regnskabstekst, der skal udskrives på en regnskabskvittering.

    > [!NOTE]
    > Hvis du anvender flere rabatter på den samme posteringslinje, indeholder regnskabskvitteringen regnskabstekster fra alle rabatter, der er knyttet til denne posteringslinje.

## <a name="set-error-handling-settings"></a>Angive indstillinger for fejlhåndtering

De fejlhåndteringsindstillinger, der er tilgængelige i regnskabsintegrationen, angives i regnskabsregistreringsprocessen. Du kan finde flere oplysninger om fejlhåndtering i finansiel integrationen i [Fejlhåndtering](fiscal-integration-for-retail-channel.md#error-handling).

Hvis du vil angive indstillinger for fejlhåndtering, skal du følge disse trin.

1. På siden **Proces for regnskabsregistrering** (**Retail og Commerce \> Konfiguration af kanal \> Regnskabsintegration \> Processer for regnskabsregistrering**) kan du angive følgende parametre for hvert trin i regnskabsregistreringsprocessen:

    - **Tillad overspring** – Denne parameter aktiverer indstillingen **Spring over** i dialogboksen til fejlhåndtering.
    - **Tillad markering som registreret** – Denne parameter aktiverer indstillingen **Markér som registreret** i dialogboksen til fejlhåndtering.
    - **Tillad udskydelse** – Denne parameter aktiverer indstillingen **Udskyd** i dialogboksen til fejlhåndtering.
    - **Fortsæt ved fejl** – Hvis dette parameter er aktiveret, kan regnskabsregistreringsprocessen fortsætte i POS-registreret, hvis regnskabsregistreringen af en transaktion eller hændelse slår fejl. I modsat fald skal operatøren, for at køre regnskabsregistreringen af den næste transaktion eller hændelse, prøve den fejlslagne regnskabsregistrering igen, springe den over eller markere transaktionen eller hændelsen som registreret. Du kan finde yderligere oplysninger under [Valgfri regnskabsregistrering](fiscal-integration-for-retail-channel.md#optional-fiscal-registration).

    > [!NOTE]
    > Såfremt parametret **Fortsæt ved fejl** er slået til, deaktiveres parametrene **Tillad overspring** og **Tillad at markere som registreret** automatisk.

1. Indstillingerne **Spring over** og **Marker som registreret** i dialogboksen til fejlhåndtering kræver, at rettigheden **Tillad, at registrering springes over, eller marker som registreret** er aktiveret. Du kan aktivere denne tilladelse ved at gå til siden **Rettighedsgrupper** (**Retail og Commerce \> Medarbejdere \> Rettighedsgrupper**) og angive rettigheden **Tillad, at registrering springes over, eller marker som registreret** til **Ja**.
1. Indstillingen **Udskyd** i dialogboksen til fejlhåndtering kræver, at tilladelsen **Tillad udskydelse** er aktiveret. Du kan aktivere tilladelsen ved at gå til siden **Rettighedsgrupper** (**Retail og Commerce \> Medarbejdere \> Rettighedsgrupper**) og angive indstillingen **Tillad udskydelse** til **Ja**.
1. Med indstillingerne **Spring over**, **Markér som registreret** og **Udskyd** kan operatører angive yderligere oplysninger, hvis regnskabsregistreringen mislykkes. For at gøre denne funktionalitet tilgængelig skal du angive infokoderne **Spring over**, **Markér som registreret** og **Udskyd** i en regnskabsconnectorgruppe. De oplysninger, som operatører angiver, gemmes derefter som en årsagskodetransaktion, der er knyttet til regnskabstransaktionen. Du kan finde flere oplysninger om årsagskoder i [Årsagskoder og årsagskodegrupper](../info-codes-retail.md).

    > [!NOTE]
    > **Produkt**-udløserfunktionen understøttes ikke for årsagskoder, der bruges til **Spring over** og **Markér som registreret** i regnskabsconnectorgrupper.

    - På siden **Regnskabsconnectorgruppe** under fanen **Infokoder** skal du vælge infokoder eller infokodegrupper i felterne **Spring over**, **Markér som registreret** og **Udskyd**.

    > [!NOTE]
    > Et regnskabsdokument og ét ikke-regnskabsmæssigt dokument kan oprettes på ethvert trin i en regnskabsregistreringsprocessen. Et regnskabsdokumentudbyder-udvidelse identificerer hver type postering eller en hændelse i forbindelse med regnskabs- eller ikke-regnskabsmæssige dokumenter. Funktionen til håndtering af fejl gælder kun for regnskabsdokumenter.
    >
    > - **Regnskabsdokument** – Et obligatorisk dokument, der skal registreres korrekt (f.eks. en regnskabskvittering).
    > - **Ikke-regnskabsdokument** – Et supplerende dokument for posteringen eller hændelsen (f.eks. et gavekort).

1. Hvis operatøren skal kunne fortsætte med at behandle den aktuelle operation (f.eks. oprettelse elle afslutning af en transaktion) efter, at der er opstået en sundhedskontrolfejl, skal du aktivere rettigheden **Tillad, at sundhedskontrolfejl springes over** på siden for **Rettighedsgrupper** (**Retail og Commerce \> Medarbejdere \> Rettighedsgrupper**). Du kan finde flere oplysninger om proceduren for sundhedskontrol under [Sundhedskontrol af regnskabsregistreringen](fiscal-integration-for-retail-channel.md#fiscal-registration-health-check).

## <a name="set-up-fiscal-xz-reports-from-the-pos"></a>Oprette X/Z-regnskabsrapporter fra POS

Hvis du vil køre X/Z-regnskabsrapporter fra POS, skal du føje nye knapper til et POS-layout.

- På siden **Knapmatricer** skal du følge vejledningen i [Tilføj POS-operationer til POS-layout ved at anvende Knapmatricedesigneren](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters) for at installere designeren og opdatere et POS-layout.

    1. Vælg det layout, der skal opdateres. 
    1. Tilføj en ny knap, og indstil **Udskriv regnskab X**-knapegenskaben.
    1. Tilføj en ny knap, og indstil **Udskriv regnskab Z**-knapegenskaben.
    1. På siden **Distributionsplan** skal du køre jobbet **1090** for at overføre ændringer til kanaldatabasen.

## <a name="enable-manual-execution-of-deferred-fiscal-registration"></a>Aktiver manuel udførelse af udskudte regnskabsregistreringer

For at aktivere manuel udførelse af en udskudte regnskabsregistreringer skal du tilføje en ny knap til POS-layoutet.

- På siden **Knapmatricer** skal du følge vejledningen i [Tilføj POS-operationer til POS-layout ved at anvende Knapmatricedesigneren](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters) for at installere designeren og opdatere et POS-layout.

    1. Vælg det layout, der skal opdateres.
    1. Tilføj en ny knap, og indstil knappens egenskaber for **Fuldfør regnskabsregistreringsprocessen**.
    1. På siden **Distributionstidsplan** skal du køre jobbet **1090** for at overføre dine ændringer til kanaldatabasen.

## <a name="view-connection-parameters-and-other-information-in-pos"></a>Få vist forbindelsesparametre og andre oplysninger i POS

Få vist forbindelsesparametre og andre oplysninger i POS ved at gøre følgende.

1. Åbn MPOS (Modern POS) eller Cloud POS (CPOS).
1. Vælg **Indstillinger**. Hvis regnskabsintegration er aktiveret, vises følgende oplysninger i sektionen **Finansiel integration** til højre:

    - Status for regnskabsregistrering
    - Tilstand i sidste regnskabstransaktion
    - Antallet af afventende hændelser

1. Vælg **Detaljer** for at få vist følgende oplysninger:

    - Registreringsprocestrin
    - Forbindelsesparametre
    - Detaljer i revisionshændelser
 
[!INCLUDE[footer-include](../../includes/footer-banner.md)]
