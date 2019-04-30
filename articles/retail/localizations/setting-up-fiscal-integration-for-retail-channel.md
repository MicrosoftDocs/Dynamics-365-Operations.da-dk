---
title: Konfigurere regnskabsintegration for detailkanaler
description: Dette emne indeholder retningslinjer for opsætning af regnskabsintegrationsfunktionen for detailkanaler.
author: josaw
manager: annbe
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-11-1
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 060075757dec64e83c46498380a920d580ac09e4
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/12/2019
ms.locfileid: "898971"
---
# <a name="set-up-the-fiscal-integration-for-retail-channels"></a>Konfigurere regnskabsintegration for detailkanaler

[!include [banner](../includes/banner.md)]

## <a name="introduction"></a>Introduktion

Dette emne indeholder retningslinjer for opsætning af regnskabsintegrationsfunktionen for detailkanaler. Du kan finde flere oplysninger om regnskabsintegrationen i [Oversigt over regnskabsintegration for detailkanaler](fiscal-integration-for-retail-channel.md).

Regnskabsintegrationsprocessen består af følgende opgaver:

1. Konfigurer regnskabsconnectorer, som repræsenterer regnskabsenheder eller -tjenester, der bruges til regnskabsmæssige registreringsformål, f.eks. bonprintere.
2. Konfigurer udbydere af dokumenter, der opretter regnskabsdokumenter, som bliver registreret i regnskabsenheder eller -tjenester ved hjælp af regnskabsconnectorer.
3. Konfigurer regnskabsregistreringsprocessen, der definerer en række trin i regnskabsregistreringen og regnskabsconnectorer og regnskabsdokumentudbydere, der bruges til hvert trin.
4. Tildel regnskabsregistreringsprocesser til POS-funktionalitetsprofiler.
5. Tildel tekniske connectorprofiler til hardwareprofiler.

## <a name="set-up-a-fiscal-registration-process"></a>Konfigurer en regnskabsregistreringsproces

Før du bruger funktionen til regnskabsintegration, skal du konfigurere følgende indstillinger:

1. Opdater detailparametre.

    1. På siden **Delte parametre for detail** under fanen **Generelt** skal du vælge **Ja** i indstillingen **Aktivér regnskabsintegration** . Definer nummerserierne for følgende referencer under fanen **Nummerserier**:

        - Regnskabsteknisk profilnummer
        - Regnskabsconnectorgruppenummer
        - Registreringsprocesnummer

    2. Definer nummerserien for regnskabsfunktionens profilnummer på siden **Detailparametre**.

    > [!NOTE]
    > Nummerserier er valgfrie. Der kan genereres numre til alle regnskabsintegrationsenheder fra nummerserier eller manuelt.

2. Overfør konfigurationer for regnskabsforbindelser og regnskabsdokumentudbydere.

    En regnskabsdokumentudbyder er ansvarlig for at generere regnskabsdokumenter, der repræsenterer detailtransaktioner og -hændelser, der er registreret på POS i et format, der også bruges til interaktion med en regnskabsenhed eller -tjeneste. F.eks. kan en udbyder af regnskabsdokumenter generere en repræsentation af en regnskabskvittering i et XML-format.

    En regnskabsconnector er ansvarlig for kommunikationen med en regnskabsenhed eller -tjeneste. En regnskabsconnector kan for eksempel sende en regnskabskvittering, som en regnskabsdokumentudbyder har oprettet i et XML-format, til en bonprinter. Du kan finde flere oplysninger om regnskabsintegrationskomponenter i [Regnskabsregistreringsprocessen og eksempler på regnskabsintegration for regnskabsenheder](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices).

    1. På siden **Regnskabsconnectorer** (**Retail \> Konfiguration af kanal \> Regnskabsintegration \> Regnskabsconnectorer**) skal du overføre en XML-konfiguration for hver enhed eller tjeneste, du planlægger at bruge til regnskabsintegration.

        > [!TIP]
        > Vælg **Vis** for at få vist alle funktionelle og tekniske profiler, der er relateret til den aktuelle regnskabsconnector.

    2. På siden **Udbydere af regnskabsdokumenter** (**Retail \> Konfiguration af kanal \> Regnskabsintegration \> Udbydere af regnskabsdokumenter**) skal du overføre en XML-konfiguration for hver enhed eller tjeneste, du planlægger at bruge.

        > [!TIP]
        > Vælg **Vis** for at få vist alle funktionelle profiler, der er relateret til den aktuelle udbyder af regnskabsdokumenter.

    Du kan finde eksempler på konfigurationer af regnskabsconnectorer og regnskabsdokumentudbydere i [Eksempler på regnskabsintegration i Retail SDK](fiscal-integration-for-retail-channel.md#fiscal-integration-samples-in-the-retail-sdk).

    > [!NOTE]
    > Datatilknytning betragtes som en del af en regnskabsdokumentudbyder. Hvis du vil oprette andre datatilknytninger for samme connector (som f.eks. specifik lovgivning), skal du oprette forskellige regnskabsdokumentudbydere.

3. Opret funktionelle connectorprofiler og tekniske connectorprofiler.

    1. På siden **Funktionelle profiler for connector** (**Retail \> Konfiguration af kanal \> Regnskabsintegration \> Funktionelle profiler for connector**) skal du oprette en funktionel connectorprofil for hver kombination af en regnskabsconnector og en regnskabsdokumentudbyder, der er relateret til denne regnskabsconnector.

        1. Vælg et connectornavn.
        2. Vælg en dokumentudbyder.

        Du kan ændre parametrene for datatilknytning i en funktionel connectorprofil. Hvis du vil gendanne de standardparametre, der er defineret i konfigurationen af regnskabsdokumentudbyderen, skal du vælge **Opdater**.

        **Eksempler**
    
        |   | Formater | Eksempel |
        |---|--------|---------|
        | **Indstillinger for momssats** | værdi : VATrate | 1 : 2000, 2 : 1800 |
        | **Tilknytning af momskoder** | VATcode : værdi | vat20 : 1, vat18 : 2 |
        | **Tilknytning af betalingsmiddeltyper** | TenderType : værdi | Kontant : 1, Kort : 2 |

        > [!NOTE]
        > Funktionelle connectorprofiler er firmaspecifikke. Hvis du planlægger at bruge den samme kombination af regnskabsconnector og regnskabsdokumentudbyder i forskellige firmaer, skal du oprette en funktionel connectorprofil for hvert firma.

    2. På siden **Tekniske profiler for connector** (**Retail \> Konfiguration af kanal \> Regnskabsintegration \> Tekniske profiler for connector**) skal du oprette en teknisk connectorprofil for hver regnskabsconnector.

        1. Vælg et connectornavn.
        2. Vælg en connectortype. For enheder, der er forbundet med en hardwarestation, skal du vælge **Lokal**.

            > [!NOTE]
            > Kun lokale connectorer understøttes i øjeblikket.

        Parametrene under fanerne **Enhed** og **Indstillinger** i en teknisk connectorprofil kan ændres. Hvis du vil gendanne de standardparametre, der er defineret i konfigurationen af regnskabsconnectoren, skal du vælge **Opdater**. Mens der indlæses en ny version af en XML-konfigurationsfil, modtager du en meddelelse om, at den aktuelle regnskabsconnector eller regnskabsdokumentudbyder allerede bruges. Denne procedure tilsidesætter ikke manuelle ændringer, der tidligere er foretaget i funktionelle connectorprofiler og tekniske connectorprofiler. Hvis du vil anvende standardsættet af parametre fra en ny konfiguration, skal du vælge **Opdater** på siden **Funktionelle profiler for connector** eller siden **Tekniske profiler for connector**.

4. Opret regnskabsconnectorgrupper.

    En regnskabsconnectorgruppe kombinerer funktionelle profiler for regnskabsconncetorer, der udfører samme funktioner og bruges på samme trin i en regnskabsregistreringsproces. Hvis der eksempelvis kan bruges forskellige bonprintermodeller i en detailbutik, kan regnskabsconnectorer for disse bonprintere kombineres i en regnskabsconnectorgruppe.
    
    1. På siden **Regnskabsconnectorgruppe** (**Retail \> Konfiguration af kanal \> Regnskabsintegration \> Regnskabsconnectorgrupper**) skal du oprette en ny regnskabsconnectorgruppe.
    2. Tilføj funktionelle profiler til connectorgruppen. Vælg **Tilføj** under fanen **Funktionsprofiler**, og vælg et profilnummer. I en connectorgruppe kan hver regnskabsconnector kun have én funktionel profil.
    3. Hvis du vil afbryde brugen af den funktionelle profil, kan du indstille **Deaktiver** til **Ja**. Denne ændring påvirker kun den aktuelle connectorgruppe. Du kan fortsætte med at bruge den samme funktionelle profil i andre connectorgrupper.

5. Opret en regnskabsregistreringsproces.

    En regnskabsregistreringsproces defineres af rækkefølgen af trinnene i registreringen og den connectorgruppe, der bruges i hvert trin.
    
    1. På siden **Proces for regnskabsregistrering** (**Retail \> Konfiguration af kanal \> Regnskabsintegration \> Processer for regnskabsregistrering**) skal du oprette en ny post for hver entydige regnskabsregistreringsproces.
    2. Føj registreringstrin til processen:

        1. Vælg **Tilføj**.
        2. Vælg en regnskabsconnectortype.
        3. I feltet **Gruppenummer** skal du vælge en passende regnskabsconnectorgruppe.

6. Tildel enheder i regnskabsregistreringsprocessen til POS-profiler.

    1. På siden **POS-funktionalitetsprofiler** (**Retail \> Konfiguration af kanal \> POS-opsætning \> POS-profiler \> Funktionalitetsprofiler**) skal du tildele regnskabsregistreringsprocessen til en POS-funktionalitetsprofil. Vælg **Rediger**, og vælg en proces under fanen **Proces for regnskabsregistrering** i feltet **Procesnummer**.
    2. På siden **POS-hardwareprofil** (**Retail \> Konfiguration af kanal \> POS-opsætning \> POS-profiler \> Hardwareprofiler**) skal du tildele tekniske connectorprofiler til en hardwareprofil. Vælg **Rediger**, tilføj en linje under fanen **Eksterne regnskabsenheder**, og vælg derefter i feltet **Profilnummer** en teknisk connectorprofil.

    > [!NOTE]
    > Du kan føje flere tekniske profiler til en den samme hardwareprofil. Men en hardwareprofil eller POS-funktionalitetsprofil skal kun have ét skæringspunkt med en regnskabsconnectorgruppe.

    Regnskabsregistreringsflowet defineres af regnskabsregistreringsprocessen og også af nogle af parametrene for regnskabsintegrationskomponenter: CRT-udvidelsen (Commerce runtime) for udbyderen af regnskabsdokumenter og Hardwarestation-udvidelsen for regnskabsconnectoren.

    - Abonnementet på hændelser og transaktioner til regnskabsregistrering er foruddefineret i regnskabsdokumentudbyderen.
    - Udbyderen af regnskabsdokumenter er også ansvarlig for at identificere den regnskabsconnector, der bruges til regnskabsregistrering. Den sammenligner de funktionelle connectorprofiler, der indgår i den regnskabsconnectorgruppe, der er angivet for det aktuelle trin i regnskabsregistreringsprocessen, med den tekniske connectorprofil, der er tildelt til hardwareprofilen for den hardwarestation, der hører sammen med POS.
    - Udbyderen af regnskabsdokumenter bruger indstillingerne for datatilknytning fra konfigurationen af regnskabsdokumentudbyderen til at konvertere transaktions-/hændelsesdata som f.eks. moms og betalinger, mens der oprettes et regnskabsdokument.
    - Når regnskabsdokumentudbyderen genererer et regnskabsdokument, kan regnskabsconnectoren enten sende det til regnskabsenheden, som det er, eller opdele det og omdanne det til en sekvens af kommandoer for enhedens API (application programming interface), afhængigt af den kommunikation, der håndteres.

7. På siden **Proces for regnskabsregistrering** (**Retail \> Konfiguration af kanal \> Regnskabsintegration \> Processer for regnskabsregistrering**) skal du vælge **Kontroller** for at validere regnskabsregistreringsprocessen.

    Det anbefales, at du kører denne type validering i følgende tilfælde:
    
    - Når du har angivet alle indstillinger for en ny registreringsproces, herunder når du tildeler registreringsprocesser til POS-funktionalitetsprofiler og hardwareprofiler.
    - Når du har ændret en regnskabsregistreringsproces, og ændringerne kan medføre, at en anden regnskabsconnector bliver valgt på kørselstidspunktet (f.eks. hvis du ændrer connectorgruppen for et trin i regnskabsregistreringsprocessen, aktiverer en funktionel connectorprofil i en connectorgruppe eller føjer en ny funktionel connectorprofil til en connectorgruppe).
    - Når du har foretaget ændringer i tildelingen af tekniske connectorprofiler til hardwareprofiler.

8. På siden **Distributionstidsplan** skal du køre jobbene **1070** og **1090** for at overføre data til kanaldatabasen.

## <a name="set-up-fiscal-texts-for-discounts"></a>Oprette regnskabstekster for rabatter

Der skal i nogle tilfælde udskrives en særlig tekst på en regnskabskvittering, hvis der anvendes en rabat. Du kan oprette regnskabstekster for rabatter på siden **Regnskabsconnectorgruppe** (**Retail \> Konfiguration af kanal \> Regnskabsintegration \> Regnskabsconnectorgrupper**).

- For manuelle rabatter, der anvendes på POS, kan du konfigurere en regnskabstekst for den årsagskode eller årsagskodegruppe, der er angivet som **Produktrabat**-årsagskoden i POS-funktionalitetsprofilen.

    1. På siden **Regnskabsconnectorgruppe** skal du vælge **Tekst til regnskabskvittering**.
    2. Under fanen **Årsagskoder** skal du vælge **Tilføj** og vælg en årsagskode eller årsagskodegruppe.
    3. I **Nummer på årsagskode** skal du vælge en værdi.
    4. I feltet **Underkodenummer** skal du vælge en værdi, hvis der kræves en underkode for den valgte årsagskode.
    5. I feltet **Tekst til regnskabskvittering** skal du angive en regnskabstekst, der skal udskrives på en regnskabskvittering.
    6. Vælg **Ja** i **Udskriv brugerinput på regnskabskvitteringen** for at tilsidesætte teksten på en regnskabskvittering og erstatte den med oplysninger, som en bruger angiver manuelt ved POS. Denne indstilling gælder kun for årsagskoder med inputtypen **Tekst**.

    > [!NOTE]
    > Du kan angive en regnskabstekst til flere årsagskoder for at understøtte scenarier, hvor årsagskodegrupper, tilknyttede årsagskoder og udløste årsagskoder bruges. I disse tilfælde indeholder regnskabskvitteringen regnskabstekster fra alle årsagskoder, der er knyttet til den posteringslinje, hvor rabatten blev anvendt.

- For kanalspecifikke rabatter skal du definere en regnskabstekst for rabat-id'et.

    1. På siden **Regnskabsconnectorgruppe** skal du vælge **Tekst til regnskabskvittering**.
    2. Under fanen **Rabatter** skal du vælge **Tilføj** og vælg et rabat-id.
    3. I feltet **Tekst til regnskabskvittering** skal du angive en regnskabstekst, der skal udskrives på en regnskabskvittering.

    > [!NOTE]
    > Hvis du anvender flere rabatter på den samme posteringslinje, indeholder regnskabskvitteringen regnskabstekster fra alle rabatter, der er knyttet til denne posteringslinje.

## <a name="set-error-handling-settings"></a>Angive indstillinger for fejlhåndtering

De fejlhåndteringsindstillinger, der er tilgængelige i regnskabsintegrationen, angives i regnskabsregistreringsprocessen. Du kan finde flere oplysninger om fejlhåndtering i finansiel integrationen i [Fejlhåndtering](fiscal-integration-for-retail-channel.md#error-handling).

1. På siden **Proces for regnskabsregistrering** (**Retail \> Konfiguration af kanal \> Regnskabsintegration \> Processer for regnskabsregistrering**) kan du angive følgende parametre for hvert trin i regnskabsregistreringsprocessen:

    - **Tillad overspring** – Denne parameter aktiverer indstillingen **Spring over** i dialogboksen til fejlhåndtering.
    - **Tillad markering som registreret** – Denne parameter aktiverer indstillingen **Markér som registreret** i dialogboksen til fejlhåndtering.
    - **Fortsæt ved fejl** – Hvis dette parameter er aktiveret, kan regnskabsregistreringsprocessen fortsætte i POS-registreret, hvis regnskabsregistreringen af en transaktion eller hændelse slår fejl. I modsat fald skal operatøren, for at køre regnskabsregistreringen af den næste transaktion eller hændelse, prøve den fejlslagne regnskabsregistrering igen, springe den over eller markere transaktionen eller hændelsen som registreret. Du kan finde yderligere oplysninger under [Valgfri regnskabsregistrering](fiscal-integration-for-retail-channel.md#optional-fiscal-registration).

    > [!NOTE]
    > Såfremt parametret **Fortsæt ved fejl** er slået til, deaktiveres parametrene **Tillad overspring** og **Tillad at markere som registreret** automatisk.

2. Indstillingerne **Spring over** og **Marker som registreret** i dialogboksen til fejlhåndtering kræver rettigheden **Tillad, at registrering springes over, eller marker som registreret**. Derfor skal du på siden **Rettighedsgrupper** (**Detail \> Medarbejdere \> Rettighedsgrupper**) aktivere rettigheden **Tillad, at registrering springes over, eller marker som registreret**.
3. Med indstillingerne **Spring over** og **Markér som registreret** kan operatører angive yderligere oplysninger, hvis regnskabsregistreringen mislykkes. For at gøre denne funktionalitet tilgængelig skal du angive årsagskoderne **Spring over** og **Markér som registreret** i en regnskabsconnectorgruppe. De oplysninger, som operatører angiver, gemmes derefter som en årsagskodetransaktion, der er knyttet til regnskabstransaktionen. Du kan finde flere oplysninger om årsagskoder i [Årsagskoder og årsagskodegrupper](../info-codes-retail.md).

    > [!NOTE]
    > **Produkt**-udløserfunktionen understøttes ikke for årsagskoder, der bruges til **Spring over** og **Markér som registreret** i regnskabsconnectorgrupper.

    - På siden **Regnskabsconnectorgruppe** under fanen **Årsagskoder** skal du vælge årsagskoder eller årsagskodegrupper i felterne **Spring over** og **Markér som registreret**.

    > [!NOTE]
    > Et regnskabsdokument og ét ikke-regnskabsmæssigt dokument kan oprettes på ethvert trin i en regnskabsregistreringsprocessen. Et regnskabsdokumentudbyder-udvidelse identificerer hver type postering eller en hændelse i forbindelse med regnskabs- eller ikke-regnskabsmæssige dokumenter. Funktionen til håndtering af fejl gælder kun for regnskabsdokumenter.
    >
    > - **Regnskabsdokument** – Et obligatorisk dokument, der skal registreres korrekt (f.eks. en regnskabskvittering).
    > - **Ikke-regnskabsdokument** – Et supplerende dokument for posteringen eller hændelsen (f.eks. et gavekort).

4. Hvis operatøren skal kunne fortsætte med at behandle den aktuelle operation (f.eks. oprettelse elle afslutning af en transaktion) efter, at der er opstået en sundhedskontrolfejl, skal du aktivere rettigheden **Tillad, at sundhedskontrolfejl springes over** på siden for **Rettighedsgrupper** (**Detail \> Medarbejdere \> Rettighedsgrupper**). Du kan finde flere oplysninger om proceduren for sundhedskontrol under [Sundhedskontrol af regnskabsregistreringen](fiscal-integration-for-retail-channel.md#fiscal-registration-health-check).

## <a name="set-up-fiscal-xz-reports-from-the-pos"></a>Oprette X/Z-regnskabsrapporter fra POS

Hvis du vil køre X/Z-regnskabsrapporter fra POS, skal du føje nye knapper til et POS-layout.

- På siden **Knapmatricer** skal du følge vejledningen i [Føj en brugerdefineret handlingsknap til POS-layoutet i Retail Headquarters](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters) for at installere designeren og opdatere et POS-layout.

    1. Vælg det layout, der skal opdateres. 
    2. Tilføj en ny knap, og indstil **Udskriv regnskab X**-knapegenskaben.
    3. Tilføj en ny knap, og indstil **Udskriv regnskab Z**-knapegenskaben.
    4. På siden **Distributionsplan** skal du køre jobbet **1090** for at overføre ændringer til kanaldatabasen.

## <a name="enable-manual-execution-of-postponed-fiscal-registration"></a>Aktiver manuel udførelse af udsatte regnskabsregistreringer

For at aktivere manuel udførelse af en udsat regnskabsregistreringer skal du tilføje en ny knap til POS-layoutet.

- På siden **Knapmatricer** skal du følge vejledningen i [Føj en brugerdefineret handlingsknap til POS-layoutet i Retail Headquarters](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters) for at installere designeren og opdatere et POS-layout.

    1. Vælg det layout, der skal opdateres.
    2. Tilføj en ny knap, og indstil knappens egenskaber for **Fuldfør regnskabsregistreringsprocessen**.
    3. På siden **Distributionstidsplan** skal du køre jobbet **1090** for at overføre dine ændringer til kanaldatabasen.
