---
title: Klyngeplacering fuld
description: Denne artikel indeholder oplysninger om funktionen Klyngeplacering fuld. Denne funktion er et alternativ til en mere stiv håndhævelse af regler for arbejdspause, når der bruges klyngepluk, da det giver mulighed for større fejlmargener i volumenbegrænsningerne af containere eller transport.
author: Mirzaab
ms.date: 08/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSClusterProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 4d46933b7c60317234b8e39cd6dfd63d383de860
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857135"
---
# <a name="cluster-position-full"></a>Klyngeplacering fuld

[!include [banner](../includes/banner.md)]

Funktionen *Klyngeplacering fuld* er et alternativ til en mere stiv håndhævelse af regler for arbejdspause, når der bruges klyngepluk, da det giver mulighed for større fejlmargener i volumenbegrænsningerne af containere eller transport. I et almindeligt scenarie er det ikke alle varer på en arbejdsordre, der passer ind i en valgt container. Lagermedarbejdere, der udfører klyngepluk, har få valgmuligheder i dette scenario: De skal enten skifte til en større container eller arbejde sammen med deres overordnede for at kunne finde frem til en anden løsning.

Denne funktion introducerer muligheden for at køre knappen **Fuld** knap på en af arbejdsenhederne i en klynge. I ældre versioner var denne indstilling kun tilgængelig ved almindeligt ordrepluk, ikke for klyngepluk. Men denne funktion adskiller sig fra standardknappen **Fuld**, da det resterende arbejde annulleres. Det foreslås ikke, at brugeren føjer en anden beholder til den samme klynge, og der oprettes ikke automatisk nyt arbejde.

## <a name="turn-the-cluster-position-full-feature-on-or-off"></a>Aktivere eller deaktivere funktionen Klyngeplacering fuld

Hvis du vil bruge den funktionalitet, der er beskrevet i denne artikel, skal funktionen *Klyngeplacering fuld* være aktiveret for systemet. Fra og med Supply Chain Management version 10.0.25 er denne funktion obligatorisk og kan ikke deaktiveres. Hvis du kører en version, der er ældre end 10.0.25, kan administratorer slå denne funktion til eller fra ved at søge efter funktionen *Klyngeplacering fuld* i arbejdsområdet [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="setup"></a>Konfiguration

Dette afsnit indeholder retningslinjer og et eksempel, der viser, hvordan du kan konfigurere og bruge funktionen *Klyngeplacering fuld*.

### <a name="make-sample-data-available"></a>Gøre eksempeldata tilgængelige

Hvis du vil arbejde dig gennem [eksempelscenariet](#example-scenario) ved hjælp af de eksempelposter og -værdier, der er angivet her, skal du være på et system, hvor [standarddemodataene](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er installeret. Derudover skal du vælge den juridiske enhed **USMF**, før du starter.

Du kan også bruge dette eksempelscenarie som vejledning til brug af funktionen i et produktionssystem. I dette tilfælde skal du dog erstatte dine egne værdier for hver af de indstillinger, der beskrives her.

### <a name="cluster-profiles"></a>Klyngeprofiler

Du skal angive, om klynge-id'er skal genereres automatisk, hvor mange placeringer der bruges, når klynger afbrydes, og hvordan plukarbejdet skal sættes i sekvens og kontrolleres.

1. Gå til **Lokationsstyring \> Opsætning \> Mobilenhed \> Klyngeprofiler**.
1. Vælg posten **Opret klynge** i listeruden.
1. I oversigtspanelet **Generelt** skal du kontrollere følgende værdier:

    - **Generér klynge-id:** *Ja*
    - **Aktivér placeringer:** *Ja*
    - **Antal placeringer:** *2*
    - **Navn på placering:** *Numerisk*
    - **Bryd klynge på:** *Læg på lager*
    - **Sortér bekræftelsestype:** *Scanning af placering*

1. I oversigtspanelet **Klyngesortering**. Gitteret skal være tomt (dvs. det må ikke indeholde linjer).

### <a name="work-templates"></a>Arbejdsskabeloner

Definer, hvordan du opretter plukarbejde til klyngepluk.

1. Gå til **Lagerstedsstyring \> Opsætning \> Arbejde \> Arbejdsskabeloner**.
1. Angiv feltet **Arbejdsordretype** til *Salgsordrer* øverst på siden.
1. Kontrollér, at følgende arbejdsskabeloner fra demonstrationsdataene vises. Hvis de ikke er tilgængelige, kan du ikke fuldføre scenariet.

    - 61 Salgsordrestadie
    - 61 Klyngepluk for slagsordre

### <a name="location-directives"></a>Lokationsvejledninger

Du skal angive, hvor varerne plukkes fra, og hvor de skal placeres.

1. Gå til **Lokationsstyring \> Opsætning \> Lokationsvejledninger**.
1. Indstil feltet **Arbejdsordretype** i listeoverskriften til *Salgsordrer*.
1. Kontrollér, at følgende salgsordredirektiver fra demonstrationsdataene vises. Hvis de ikke er tilgængelige, kan du ikke fuldføre scenariet.

    - 61 Klyngepluk
    - 61 Plukordre for slagsordre

### <a name="mobile-device-menu-items"></a>Menupunkter i mobilenhed

Du skal konfigurere et menupunkt på en mobilenhed til at bruge eksisterende arbejde, der er pålagt ved hjælp af klyngepluk. I mobilenhedens menupunkt til klyngepluk skal parameteren **Tillad opdeling af arbejde** være slået til, og arbejdsklassen *Salgsordrepluk* skal tilføjes.

1. Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Menupunkter i mobilenhed**.
1. Vælg posten **Opret klyngepluk** i listeruden.
1. Vælg **Rediger** i handlingsruden.
1. I oversigtspanelet **Generelt** kan du angive følgende værdier:

    - **Ledet af:** *Klyngepluk*
    - **Generer nummerplade:** *Ja*
    - **Tillad opdeling af arbejde:** *Ja*
    - **Klyngeprofil-id:** *Opret klynge*

    Accepter standardværdierne for alle andre felter.

1. I oversigtspanelet **Arbejdsklasser** skal du tilføje følgende to linjer efter behov:

    - Linje 1 (findes som regel i demonstrationsdata):

        - **Arbejdsklasse-id:** *Salg* 
        - **Arbejdsordretype:** *Salgsordrer*

    - Linje 2 (findes sikkert ikke i demonstrationsdata):

        - **Arbejdsklasse-id:** *Salgsordrepluk*
        - **Arbejdsordretype:** *Salgsordrer*

1. Gå til **Konfiguration af arbejdsbekræftelse** i handlingsruden.
1. Vælg **Rediger**.
1. Angiv følgende værdier på linjen i gitteret.
    - **Arbejdstype** - *Pluk*
    - **Produktbekræftelse** - *Markér afkrydsningsfeltet*

1. Vælg **Gem** i handlingsruden, og luk siden.

## <a name="create-picking-work"></a>Opret plukarbejde

Før du kan starte klyngepluk, skal du oprette udgående arbejde. Den klyngeprofil, du oprettede tidligere, angiver to klyngeplaceringer. Derfor skal der oprettes mindst to arbejds-id'er til salgsordrepluk. I dette scenarie sker der transaktioner på lagersted *61*, og de bruger varerne *L0101* og *T0100*. Demodataene skal have en tilstrækkelig disponibel lagerbeholdning af disse varer. Kontrollér, at du har tilstrækkeligt lager til at fuldføre transaktionerne.

### <a name="create-sales-order-1"></a>Opret salgsordre 1

1. Gå til **Sales and MArketing \> Salgsordrer \> Alle salgsordrer**.
1. Vælg **Ny** for at oprette salgsordre 1.
1. Angiv følgende værdier i dialogboksen **Opret salgsordre**:

    - **Debitorkonto:** *US-010*
    - **Lagersted:** *61*

1. Vælg **OK**.
1. Den nye indkøbsordre åbnes. I oversigtspanelet **Salgsordrelinjer** skal du tilføje en linje, der har følgende indstillinger:

    - **Varenummer:** *T0100*
    - **Antal:** *5*

1. I oversigtspanelet **Linjedetaljer** skal du under fanen **Levering** angive feltet **Bekræftet afsendelsesdato** til dags dato.
1. I oversigtspanelet **Salgsordrelinjer** skal du tilføje endnu en linje, der har følgende indstillinger:

    - **Varenummer:** *L0101*
    - **Antal:** *20*

1. I oversigtspanelet **Linjedetaljer** skal du under fanen **Levering** angive feltet **Bekræftet afsendelsesdato** til dags dato.
1. Udfør følgende trin for hver linje, du netop har tilføjet, for at reservere lager:

    1. Markér den linje, du vil reservere.
    2. Gå til oversigtspanelet **Salgsordrelinjer**, og vælg **Lager \> Reservation**.
    3. På siden **Reservation** skal du i handlingsruden vælge **Reserver parti** for at reservere lageret.
    4. Luk siden **Reservation**.

1. Vælg **Frigør til lagersted** under fanen **Lagersted** i handlingsruden.

    Når frigivelsen er fuldført, modtager du orienterende meddelelser, der viser bølgen og last-id'et, der blev oprettet.

### <a name="create-sales-order-2"></a>Opret salgsordre 2

1. Gå til **Sales and MArketing \> Salgsordrer \> Alle salgsordrer**.
1. Vælg **Ny** for at oprette salgsordre 2.
1. Angiv følgende værdier i dialogboksen **Opret salgsordre**:

    - **Debitorkonto:** *US-011*
    - **Lagersted:** *61*

1. Vælg **OK**.
1. Den nye indkøbsordre åbnes. I oversigtspanelet **Salgsordrelinjer** skal du tilføje en linje, der har følgende indstillinger:

    - **Varenummer:** *L0101*
    - **Antal:** *20*

1. I oversigtspanelet **Linjedetaljer** skal du under fanen **Levering** angive feltet **Bekræftet afsendelsesdato** til dags dato.
1. I oversigtspanelet **Salgsordrelinjer** skal du tilføje endnu en linje, der har følgende indstillinger:

    - **Varenummer:** *T0100*
    - **Antal:** *2*

1. I oversigtspanelet **Linjedetaljer** skal du under fanen **Levering** angive feltet **Bekræftet afsendelsesdato** til dags dato.
1. Udfør følgende trin for hver linje, du netop har tilføjet, for at reservere lager:

    1. Markér den linje, du vil reservere.
    2. Gå til oversigtspanelet **Salgsordrelinjer**, og vælg **Lager \> Reservation**.
    3. På siden **Reservation** skal du i handlingsruden vælge **Reserver parti** for at reservere lageret.
    4. Luk siden **Reservation**.

1. Vælg **Frigør til lagersted** under fanen **Lagersted** i handlingsruden.

    Når frigivelsen er fuldført, modtager du orienterende meddelelser, der viser bølgen og last-id'et, der blev oprettet.

### <a name="get-work-ids-and-license-plate-numbers"></a>Hent arbejds-id'er og id-numre

Der skal være oprettet to arbejds-id'er, som hver især har to pluklinjer. Udfør følgende trin for at finde arbejds-id'erne og id-tildelingerne.

1. Gå til **Lokationsstyring \> Arbejde \> Arbejdsdetaljer**.
1. Søg i gitteret **Oversigt** efter de to salgsordrer, du netop har oprettet, i kolonnen **Ordrenummer**. Notér dig arbejds-id'et for hver salgsordre.
1. Markér rækken for hver salgsordre for at få vist relaterede oplysninger i **Linjer**-gitteret. Notér dig den lokation, som de enkelte varer skal plukkes fra.
1. Gå til **Lagerstyring \> Forespørgsler og rapporter \> Beholdningsliste**.
1. I handlingsruden skal du vælge **Dimensioner** for at åbne dialogboksen **Dimensionsvisning**.
1. Sørg for, at afkrydsningsfelterne **Id** **Lagersted** og **Varenummer** er markeret, og vælg derefter **OK**.
1. I **Filter**-ruden skal du angive følgende filtre:

    - **Varenummer** – **er enten** – *L0101* eller *T100*
    - **Lagersted** – **begynder med** – *61*

1. Notér dit de viste værdier af **Id**.

## <a name="example-scenario"></a><a name="example-scenario"></a>Eksempelscenario

### <a name="mobile-device-flow-execution--work-confirmation-setup-for-the-product"></a>Udførelse af mobilenhedsproces – Konfiguration af arbejdsbekræftelse for produktet

1. Log på mobilappen Lokationsstyring som en bruger på lagersted *61*.
1. Gå til **Udgående \> Opret klyngepluk**.

    Siden **OPGAVE: Tildel arbejde til klynge** vises.

1. Angiv arbejds-id'et for salgsordre 1 for at tildele det klyngeplacering 1.
1. Vælg **OK** (markeringssymbol).
1. Angiv arbejds-id'et for salgsordre 2 for at tildele det klyngeplacering 2.
1. Vælg **OK** (markeringssymbol).

    Siden **OPGAVE: Opret klyngepluk: Pluk** vises, og der står *Vare L0101 2 PL*.

Da klyngeprofilen angav antallet af placeringer til 2, vil systemet automatisk henvise til det første konsoliderede pluk: to paller (PL) af vare *L0101*.

Du kan når som helst under følgende trin vælge fanen **Detaljer** for at få vist flere oplysninger om opgaven, f.eks. plukpladsen.

1. Angiv feltet **VARE** til *L0101*. Dette bekræfter det varenummer, der kræves til dette menupunkt (du har konfigureret dette tidligere ved at vælge **Konfiguration af arbejdsbekræftelse** på siden **Menupunkt på mobilenhed**, da du oprettede dette menupunkt).
1. Angiv det id-nummer, der er knyttet til varen på den lokation, der plukkes fra. Du skal vælge to paller.
1. Indstil feltet **LP** til *LP\_PICK\_01*.
1. Vælg **OK** (markeringssymbol).

    Siden **OPGAVE: Sortér: Opret klyngepluk** vises. Her skal du sortere de to plukkede paller i en plukplacering. Denne placering kan være en transportkasse eller container, der bruges til at adskille det plukkede lager efter salgsordre.

1. Se de detaljer, der vises for varen (*L0101*) og antal (*20* hver), som skal sorteres i position 1 (for salgsordre 1).
1. Indstil feltet **POSITIONSNAVN** til *1*.
1. Vælg **OK** (markeringssymbol).
1. Se de detaljer, der vises for varen (*L0101*) og antal (*20* hver), som skal sorteres i position 2 (for salgsordre 2).
1. Indstil feltet **POSITIONSNAVN** til *2*.
1. Vælg **OK** (markeringssymbol).

    Siden **OPGAVE: Opret klyngepluk: Pluk** vises, og der står *Vare T0100 7 hver*.

I dette scenario kan position 1 ikke acceptere det fulde antal varer, der skal plukkes for at opfylde salgsordre 1. En position skal være markeret som fuld. I dette scenario skal du foretage et delvist pluk af den anden vare. Den anden vare plukkes delvist til position 1, og der oprettes nyt arbejde for at plukke det resterende antal for at opfylde ordren.

1. Vælg menuknappen (kaldes også hamburger eller hamburgerknappen), og vælg derefter **Position fuld**.
1. Identificer den position, der er fuld, og vælg *1*.
1. Vælg **OK** (markeringssymbol).
1. Angiv det plukantal, der stadig kan plukkes til position 1. Systemet kan bestemme, hvilket varenummer der skal plukkes.
1. Angiv *2*.
1. Vælg **OK** (markeringssymbol).
1. Bekræft varenummeret for at fuldføre plukningen af den resterende vare på position 2.
1. Angiv feltet **VARE** til *T0100*.
1. Vælg **OK** (markeringssymbol).
1. Angiv det id, som varen plukkes fra, ved at indstille feltet **LP** til *LPREPL04*.
1. Vælg **OK** (markeringssymbol).
1. Se de detaljer, der vises for varen (*T0100*) og antal (*2* hver), som skal sorteres i position 2 (for salgsordre 2).
1. Indstil feltet **POSITIONSNAVN** til *2*.
1. Vælg **OK** (markeringssymbol).
1. Se de detaljer, der vises for varen (*T0100*) og antal (*2* hver), som skal sorteres i position 1 (for salgsordre 1).
1. Indstil feltet **POSITIONSNAVN** til *1*.
1. Vælg **OK** (markeringssymbol).

    Siden **OPGAVE: Opret klyngepluk: Læg på lager** vises.

I dette scenario er klyngeplukket fuldført, og brugeren dirigeres til at lægge de plukkede varer på lager fra position 1 og position 2 på lokationen for midlertidig lagring *STAGE01*.

1. Gennemgå oplysningerne på siden. De viser, at der vil blive lagt et samlet antal af *44* på lokationen for midlertidig lagring.
1. Vælg **OK** (markeringssymbol).

    Du modtager en meddelelse om "Klynge er fuldført".

Du kan nu bruge menupunktet **Salgspluk** til at plukke det resterende antal. Derefter kan du bruge menupunktet **Salgslastning** til at flytte varerne fra den midlertidige lagring til læsserampen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]