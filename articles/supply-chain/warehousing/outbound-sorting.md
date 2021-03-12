---
title: Udgående sortering
description: Dette emne indeholder oplysninger om udgående sortering. Denne funktion gør det nemmere at håndtere mindre containere og hjælper lagermedarbejderne med bedre at planlægge og organisere pallekapaciteten i lastbilen.
author: Mirzaab
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPack, WHSOutboundSortTemplate, WHSOutboundSortPositionAssignments, WHSLocationType, WHSLoactionProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 2b0049269b69c0777420b3ecd9b1f649c4a1ab11
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963404"
---
# <a name="outbound-sorting"></a>Udgående sortering

[!include [banner](../includes/banner.md)]

Denne funktion gør det nemmere at håndtere mindre containere og hjælper lagermedarbejderne med bedre at planlægge og organisere pallekapaciteten i lastbilen. Når du bruger udgående sortering, kan du sortere pakkede containere til den korrekte palle, når de har været på en pakkestation. Du kan også opbygge et pakkehierarki.

Med denne funktionalitet kan du opbygge paller fra beholdere, der er pakket via pakkefunktionen. Containeren sendes ikke til den endelige afsendelseslokation, fordi den er i det oprindelige emballeringsflow. I stedet kan arbejderne lukke containeren og flytte den til en sorteringstypelokation. De kan derefter sortere containere til positioner, der hver har en nummerplade (NP). Når containerne er blevet sorteret, kan der oprettes arbejde for at sende hele NP'en til det endelige afsendelsesområde eller stadielokation baseret på lokationsvejledninger eller dine egne krav. Derudover kan den handling, der udføres ved lukning af sorteringspositionen, straks flytte lageret til det endelige afsendelsessted og plukke det til ordren.

## <a name="turn-on-the-outbound-sorting-feature"></a>Aktivere funktionen for udgående sortering

Før du kan bruge funktionen, skal den være slået til i dit system. Administratorer kan bruge området [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov. Dér vises funktionen på følgende måde:

- **Modul:** *Lokationsstyring*
- **Funktionsnavn:** *Udgående sortering*

## <a name="setup"></a>Konfiguration

I dette scenarie skal du bruge standarddemodata for **USMF** og lagerstedet *62*. Du skal også udføre den opsætning, der er beskrevet i følgende underafsnit.

### <a name="set-up-a-wave-template"></a>Konfigurere en bølgeskabelon

Denne konfiguration behandler automatisk bølgen og opretter arbejde, når en linje er frigivet til lagerstedet.

1. Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgeskabeloner**.
1. Vælg **Lagersted 62** på skabelonlisten.
1. I oversigtspanelet **Generelt** skal du kontrollere, at indstillingen **Udfør behandling af bølgen ved frigivelse til lagerstedet** er angivet til *Ja*.

### <a name="set-up-a-worker"></a>Konfigurere en arbejder

Pakkestationen betragtes som en lokation. De lagermedarbejdere, der logger på ved pakkestationen, kan kun se og arbejde på forsendelser og containere, der er planlagt på den pågældende pakkelokation. En bruger, der logger på Microsoft Dynamics 365, skal være konfigureret som en arbejder i lokationsstyringen. Hvis brugerens navn ikke vises på listen over arbejdsbrugere, skal du benytte følgende fremgangsmåde for at tilføje det.

> [!NOTE]
> I disse trin antages det, at brugeren allerede findes i systemet og er blevet tilknyttet som medarbejder eller arbejder i modulet **Human Resources**.

1. Gå til **Lokationsstyring \> Konfiguration \> Arbejder**.
1. Vælg **Ny**.
1. I feltet **Arbejder** skal du vælge destinationsbrugeren på listen over medarbejdere.
1. Vælg **Vælg**.
1. Vælg **Gem** i handlingsruden.
1. Gå til oversigtspanelet **Brugere**, og vælg **Ny** for at oprette en mobilenhedskonto, og angiv følgende værdier for den:

    - **Bruger-id:** Angiv et entydigt id.
    - **Brugernavn:** Angiv et navn til id'et.
    - **Standardlagersted:** *62*
    - **Menunavn:** *Hoved*

1. Vælg **Gem** i handlingsruden.
1. Dialogboksen **Angiv adgangskode** viser, hvor du kan oprette en simpel adgangskode, som brugeren kan bruge til at logge på mobilappen. Angiv følgende værdier:

    - **Adgangskode:** Angiv en enkel adgangskode.
    - **Bekræft adgangskode:** Angiv den samme adgangskode igen.

1. Vælg **Angiv adgangskode**.

    En besked i Handlingscenter indeholder en meddelelse om, at adgangskoden er angivet for den bruger, du har oprettet.

### <a name="create-a-location-type"></a>Oprette en ny lokationstype

1. Gå til **Lokationsstyring \> Konfiguration \> Lagersted \> Lokationstyper**.
1. Vælg **Ny** i i handlingsruden for at oprette lokationstype, og angiv følgende værdier for den:

    - **Lokationstype:** *SORTER*
    - **Beskrivelse:** *Sorter*

1. Vælg **Gem** i handlingsruden.

### <a name="set-up-warehouse-management-parameters"></a>Konfigurere parametre for lokationsstyring

1. Gå til **Lagerstedsstyring \> Opsætning \> Parametre til lagerstedsstyring**.
1. Gå til fanen **Generelt**, og angiv feltet **Sorteringslokationstype** til **SORTER** i oversigtspanelet *Lokationstyper*.
1. Vælg **Gem** i handlingsruden.

### <a name="set-up-a-location-profile"></a>Konfigurere en lokationsprofil

1. Gå til **Lagerstedsstyring \> Konfiguration \> Lagersted \> Lokationsprofiler**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Angiv følgende værdier i overskriften:

    - **Lokationsprofil-id:** *Sortering*
    - **Navn:** *Sortering*

1. I oversigtspanelet **Generelt** kan du angive følgende værdier:

    - **Lokationsformat:** *ASRB* (gang – reol-hylde-beholder)
    - **Lokationstype:** *SORTER*
    - **Brug sporing af nummerplader:** *Ja*
    - **Tillad blandede varer:** *Ja* (når du angiver denne indstilling til *Ja*, angives indstillingen **Tillad blandede lagerbatchnumre** automatisk til *Ja* og kan ikke ændres uafhængigt.)

1. Vælg **Gem**.

### <a name="set-up-a-location"></a>Konfigurere en lokation

1. Gå til **Lokationsstyring \> Konfiguration \> Lagersted \> Lokationer**.
1. I hovedet skal du fjerne markeringen i afkrydsningsfeltet **Generér kontrolcifre for lokation**.
1. Vælg **Ny** i i handlingsruden for at oprette lokation, og angiv følgende værdier for den:

    - **Lagersted:** *62*
    - **Lokation:** *SORT*
    - **Lokationsprofil-id:** *SORTERING*

1. Vælg **Gem**.

### <a name="set-up-an-outbound-sorting-template"></a>Oprette en skabelon til udgående sortering

Skabelonen til udgående sortering bestemmer, om der er oprettet arbejde uden for sorteringslokationen, og om sorteringen skal udføres manuelt eller automatisk.

I dette scenario skal du oprette en skabelon til udgående sortering for at oprette paller efter pakkestationen.

1. Gå til **Lokationsstyring \> Konfiguration \> Emballage \> Skabelon til udgående sortering**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Angiv følgende værdier i hoveddelen for den nye skabelon:

    - **Id for skabelon til udgående sortering:** *AutoArbejde*
    - **Beskrivelse:** *Oprettelse af automatisk arbejde*
    - **Skabelontype for udgående sortering:** *Container*
    - **Lagersted:** *62*
    - **Lokation:** *SORT*

1. I oversigtspanelet **Generelt** kan du angive følgende værdier:

    - **Sorter verifikation:** *Positionsscanning*
    - **Opret arbejde lukning af position:** *Ja*

        Hvis indstillingen er angivet til *Ja*, når positionen er lukket, oprettes arbejde for at flytte lageret til den endelige afsendelseslokation. Hvis den er indstillet til *Nej*, vil lageret straks blive plukket til ordren, når positionen er lukket.

    - **Positiontildeling:** *Automatisk*

        Hvis dette felt er indstillet til *Manuelt*, skal brugeren altid angive, hvilken position lageret skal sorteres til. Hvis det er indstillet til *Automatisk*, guider systemet automatisk lageret til en position, hvor det kan, baseret på sorteringsskabelonskiftene.

1. Vælg **Gem** for at gøre knappen **Rediger forespørgsel** i handlingsruden tilgængelig.
1. Vælg **Rediger forespørgsel** i handlingsruden.
1. I forespørgselseditor skal du under fanen **Sortering** tilføje en linje, der har følgende værdier:

    - **Tabel:** *Forsendelser*
    - **Afledt tabel:** *Forsendelser*
    - **Felt:** *Fragttjeneste*

        Når du vælger denne værdi, får du muligvis vist følgende meddelelse: "Feltet Fragttjeneste er ikke et indeksfelt. Vil du tilføje sortering på dette?" Vælg **Ja**.

    - **Søgeretning:** *Stigende*

1. Vælg **OK**.
1. Du kan få vist følgende meddelelse: "Gruppering vil blive nulstillet, vil du fortsætte?" Vælg **Ja**.

    Knappen **Udgående sorteringsskabelonskift** i handlingsruden bliver tilgængelige.

1. I handlingsruden skal du vælge **Udgående sorteringsskabelonskift**.
1. I dialogboksen **Kriterier for udgående sortering** skal du angive følgende værdier:

    - **Referencetabelnavn:** *Forsendelser*
    - **Referencefeltnavn:** *Fragttjeneste*
    - **Gruppér efter felt:** Marker dette afkrydsningsfelt for at gruppere forsendelser efter fragtmand.

1. Vælg **OK** for at gemme dine indstillinger og lukke dialogboksen.

### <a name="set-up-container-packing-policies"></a>Konfigurere politik for containerpakning

1. Gå til **Lokationsstyring \> Konfiguration \> Containere \> Politikker for containerpakning**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Angiv følgende værdier i hoveddelen for den nye politik:

    - **Politik for containerpakning:** *Sorter*
    - **Beskrivelse:** *Sorter*

1. I oversigtspanelet **Oversigt** kan du angive følgende værdier:

    - **Lagersted:** *62*
    - **Standardlokationen for sortering:** *SORTER*
    - **Vægtenhed:** *kg*
    - **Politik for containerlukning:** *Automatisk frigivelse*
    - **Politik for containerfrigivelse:** *Tildel container til position for udgående sortering*

1. Vælg **Gem**.

### <a name="set-up-packing-profiles"></a>Konfigurere pakkeprofiler

Opret en ny pakkeprofil, der skal bruges sammen med sorteringsfunktionen.

1. Gå til **Lokationsstyring \> Konfiguration \> Emballage \> Pakningsprofiler**.
1. Vælg **Ny** i i handlingsruden for at oprette en linje, og angiv følgende værdier for den:

    - **Pakkeprofil-id:** *Sorter*
    - **Beskrivelse:** *Sorter*
    - **Politik for containerpakning:** *Sorter*
    - **Container-id-tilstand:** *Auto*
    - **Containertype:** *Kasse-Stor*
    - **Opret automatisk container ved containerlukning:** Ryddet (= *Nej*)

1. Vælg **Gem**.

### <a name="set-up-work-classes"></a>Konfigurere arbejdsklasser

Konfigurer en arbejdsklasse, der skal bruges sammen med sortering.

1. Gå til **Lokationsstyring \> Opsætning \> Arbejde \> Arbejdsklasser**.
1. Vælg **Ny** i i handlingsruden for at oprette en arbejdsklasse til sortering, og angiv følgende værdier for den:

    - **Arbejdsklasse-id:** *Sorter*
    - **Beskrivelse:** *Sorter*
    - **Ordretype:** *Sorteret lagerplukning*

1. Vælg **Gem**.

### <a name="set-up-mobile-device-menu-items"></a>Opsætning af mobilenhedsmenupunkter

#### <a name="set-up-a-new-pallet-menu-item"></a>Konfigurere nyt pallemenupunkt

Opret et menupunkt til mobilenhed for at opbygge paller under sortering.

1. Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Menupunkter i mobilenhed**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Angiv følgende værdier i overskriften:

    - **Navn på menupunkt:** *Palle-build*
    - **Titel:** *Palle-build*
    - **Tilstand:** *Indirekte*
    - **Brug eksisterende arbejde:** *Nej*

1. I oversigtspanelet **Generelt** kan du angive følgende værdier:

    - **Aktivitetskode:** *Udgående sortering*

        Når dette felt er angivet til *Udgående sortering*, vises feltet udgående **Skabelon-id for udgående sortering**.

    - **Brug procesvejledning:** *Ja*

        Når feltet **Aktivitetskode** er angivet til *Udgående sortering*, angives denne indstilling automatisk til *Ja*.

    - **Id for skabelon til udgående sortering:** *AutoArbejde*

1. Vælg **Gem**.

#### <a name="set-up-a-new-loading-menu-item"></a>Konfigurere nyt lastmenupunkt

Derefter skal du oprette et menupunkt, som giver brugerne mulighed for at flytte de sorterede lagervarer til afsendelsesstedet.

1. Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Menupunkter i mobilenhed**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Angiv følgende værdier i overskriften:

    - **Navn på menupunkt:** *Sortering efter last fra*
    - **Titel:** *Sortering efter last fra*
    - **Tilstand:** *Arbejde*
    - **Brug eksisterende arbejde:** *Ja*

1. I oversigtspanelet **Generelt** skal du indstille feltet **Styret af** til *Brugerstyret*.
1. I oversigtspanelet **Arbejdsklasser** skal du vælge **Ny** og derefter indstille følgende værdier:

    - **Arbejdsklasse-id:** *SORTER*
    - **Ordretype:** *Sorteret lagerplukning*

1. Vælg **Gem**.

### <a name="set-up-the-mobile-device-menu"></a>Konfigurere mobilenhedsmenuen

Du skal nu føje de nye menupunkter til mobilenhedsmenuen.

1. Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Mobilenhedsmenu**.
1. Vælg menuen **Udgående**.
1. Vælg **Rediger** i handlingsruden.
1. I kolonnen **Tilgængelige menuer og menupunkter** skal du finde og vælge **Palle-build**.
1. Vælg den højre piletast for at flytte **Palle-build** til kolonnen **Menustruktur**.
1. Brug knapperne pil op og pil ned for at placere menupunktet **Palle-build** i den ønskede placering i mobilenhedsmenuen.
1. Vælg **Gem**.
1. Gentag denne procedure for at føje menupunktet **Sortering efter last fra** til menuen **Udgående**.

### <a name="set-up-location-directives"></a>Konfigurer lokationsvejledninger

*Lokalitetsvejledninger* er regler, der hjælper med at identificere pluk og læg-lokationer for lagerbevægelser. Du skal nu oprette en regel for at administrere sorteringsarbejdet.

#### <a name="set-up-a-single-sku-directive"></a>Konfigurere vejledning for enkelt varenummer

1. Gå til **Lokationsstyring \> Opsætning \> Lokationsvejledninger**.
1. I ruden til venstre skal du ændre værdien i feltet **Arbejdsordretype** til *Sorteret lagerpluk*.
1. Gå til handlingsruden, og vælg **Ny**.
1. Angiv følgende værdier i overskriften:

    - **Sekvens:** *1*
    - **Navn:** *Båsedør*

1. I oversigtspanelet **Lokationsvejledninger** kan du angive følgende værdier:

    - **Arbejdstype:** *Læg på lager*
    - **Lokation:** *6*
    - **Lagersted:** *62*
    - **Flere SKU'er:** *Nej*

1. Vælg **Gem** for at gøre værktøjslinjen i oversigtspanelet **Linjer** tilgængelig.
1. I oversigtspanelet **Linjer** skal du vælge **Ny** og derefter indstille følgende værdier på den nye linje: Accepter standardværdierne for alle de andre felter.

    - **Sekvens:** *1*
    - **Fra:** *0*
    - **Til:** *1.000.000*

1. Vælg **Gem** for at gøre værktøjslinjen i oversigtspanelet **Handlinger i lokationsvejledning** tilgængelig.
1. I oversigtspanelet **Handlinger i lokationsvejledninger** skal du vælge **Ny** og derefter indstille følgende værdier på den nye linje: Accepter standardværdierne for alle de andre felter.

    - **Sekvens:** *1*
    - **Navn:** *Båsedør*

1. Vælg **Gem**.
1. Vælg **Rediger forespørgsel** i oversigtspanelet **Handlinger for lokationsvejledninger**.
1. Gå til forespørgselseditoren under fanen **Område**, og find den række, hvor feltet **Felt** er indstillet til *Lokation*. Angiv feltet **Kriterier** for denne række til *Lagerport*.
1. Vælg **OK** for at gemme dine indstillinger og lukke forespørgselseditoren.

#### <a name="set-up-a-multiple-sku-directive"></a>Konfigurere vejledning for flere varenumre

1. Gå til **Lokationsstyring \> Opsætning \> Lokationsvejledninger**.
1. I ruden til venstre skal du ændre værdien i feltet **Arbejdsordretype** til *Sorteret lagerpluk*.
1. Gå til handlingsruden, og vælg **Ny**.
1. Angiv følgende værdier i overskriften:

    - **Sekvens:** *2*
    - **Navn:** *Lagerport – flere*

1. I oversigtspanelet **Lokationsvejledninger** kan du angive følgende værdier:

    - **Arbejdstype:** *Læg på lager*
    - **Lokation:** *6*
    - **Lagersted:** *62*
    - **Flere varenumre:** *Ja*

1. Vælg **Gem** for at gøre værktøjslinjen i oversigtspanelet **Linjer** tilgængelig.
1. I oversigtspanelet **Linjer** skal du vælge **Ny** og derefter indstille følgende værdier på den nye linje: Accepter standardværdierne for alle de andre felter.

    - **Sekvens:** *1*
    - **Fra:** *0*
    - **Til:** *1.000.000*

1. Vælg **Gem** for at gøre værktøjslinjen i oversigtspanelet **Handlinger i lokationsvejledning** tilgængelig.
1. I oversigtspanelet **Handlinger i lokationsvejledninger** skal du vælge **Ny** og derefter indstille følgende værdier på den nye linje: Accepter standardværdierne for alle de andre felter.

    - **Sekvens:** *1*
    - **Navn:** *Lagerport – flere*

1. Vælg **Gem**.
1. Vælg **Rediger forespørgsel** i oversigtspanelet **Handlinger for lokationsvejledninger**.
1. Gå til forespørgselseditoren under fanen **Område**, og find den række, hvor feltet **Felt** er indstillet til *Lokation*. Angiv feltet **Kriterier** for denne række til *Lagerport*.
1. Vælg **OK** for at gemme dine indstillinger og lukke forespørgselseditoren.

### <a name="set-up-work-templates"></a>Konfigurer arbejdsskabeloner

1. Gå til **Lagerstedsstyring \> Opsætning \> Arbejde \> Arbejdsskabeloner**.
1. Skift værdien af feltet **Arbejdsordretype** til *Sorteret lagerpluk*.
1. Vælg **Ny** i handlingsruden for at oprette en arbejdsskabelon.
1. På fanen **Oversigt** kan du angive følgende værdier:

    - **Sekvens:** *1*
    - **Arbejdsskabelon:** *Sorter*
    - **Beskrivelse af arbejdsskabelon:** *Sorter*

1. Vælg **Gem** for at gøre oversigtspanelet **Arbejdsskabelondetaljer** tilgængeligt.
1. Gå til oversigtspanelet **Arbejdsskabelondetaljer**, og vælg **Ny** for at tilføje en linje, og indstil derefter følgende værdier for den:

    - **Arbejdstype:** *Pluk*
    - **Arbejdsklasse-id:** *SORTER*

1. Vælg **Ny** igen for at tilføje en anden linje, og angiv derefter følgende værdier for den:

    - **Arbejdstype:** *Læg på lager*
    - **Arbejdsklasse-id:** *SORTER*

1. Vælg **Gem**.

## <a name="scenario"></a>Scenario

Dette scenarie simulerer en situation, hvor pakkede containere automatisk sorteres til andre placeringer (paller) efter pakkestationen, afhængigt af fragtmanden. Når alle varer fra lasten pakkes og sorteres efter adresse, og pallerne flyttes til lagerporten.

### <a name="create-sales-orders-and-picking-work"></a>Oprette ordrer og plukarbejde

#### <a name="create-sales-order-1"></a>Opret salgsordre 1

1. Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Angiv følgende værdier i dialogboksen **Opret salgsordre**:

    - **Debitorkonto:** *US-005*
    - **Lagersted:** *62*

1. Vælg **OK** for at lukke dialogboksen.

    Den nye indkøbsordre åbnes.

1. Skift til **overskriftsvisningen**.
1. Gå til oversigtspanelet **Levering** i sektionen **Transport**, og angiv følgende værdier:

    - **Fragtmand:** *Air Cargo*
    - **Fragttjeneste:** *Air*

1. Skift til visningen **Linjer**.
1. Hvis en ny tom linje ikke automatisk føjes til gitteret i oversigtspanelet **Salgsordrelinjer**, skal du vælge **Tilføj linje** for at tilføje en.
1. På den nye ordrelinje skal du angive følgende værdier:

    - **Varenummer:** *A0001*
    - **Antal:** *2*

1. Mens den nye ordrelinje stadig er valgt i oversigtspanelet **Salgsordrelinjer**, skal du vælge **Reservation** i menuen **Lager** oven over gitteret.
1. På siden **Reservation** skal du vælge **Reserver parti** for at reservere det fulde antal på den valgte linje på lagerstedet.
1. Luk siden **Reservation** for at vende tilbage til salgsordren.
1. Vælg **Frigiv til lagersted** i gruppen **Handlinger** under fanen **Lagersted** i handlingsruden.
1. Du modtager en informativ meddelelse, der viser forsendelsen og bølgen for denne ordre. Noter dig bølge-id og forsendelses-id-numrene.

#### <a name="sales-order-2"></a>Salgsordre 2

1. Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Angiv følgende værdier i dialogboksen **Opret salgsordre**:

    - **Debitorkonto:** *US-006*
    - **Lagersted:** *62*

1. Vælg **OK** for at lukke dialogboksen.
1. Den nye indkøbsordre åbnes. Den skal omfatte en ny tom linje i gitteret i oversigtspanelet **Salgsordrelinjer**. Indstil følgende værdier på denne ordrelinje:

    - **Vare:** *A0001*
    - **Antal:** *1*

1. I oversigtspanelet **Linjedetaljer** under fanen **Levering** skal du angive feltet **Leveringsmåde** til *Flow-STD*.
1. I oversigtspanelet **Salgsordrelinjer** skal du vælge **Tilføj linje** og derefter indstille følgende værdier på den anden linje:

    - **Vare:** *A0002*
    - **Antal:** *1*

1. I oversigtspanelet **Linjedetaljer** under fanen **Levering** ændre værdien af feltet **Leveringsmåde** til *Luft C-Luft*.
1. I oversigtspanelet **Salgsordrelinjer** skal du vælge den første ordrelinje. Vælg derefter **Reservation** i menuen **Lager** oven over gitteret.
1. På siden **Reservation** skal du vælge **Reserver parti** for at reservere det fulde antal på den valgte linje på lagerstedet.
1. Luk siden **Reservation** for at vende tilbage til salgsordren.
1. I oversigtspanelet **Salgsordrelinjer** skal du vælge den anden ordrelinje. Vælg derefter **Reservation** i menuen **Lager** oven over gitteret.
1. På siden **Reservation** skal du vælge **Reserver parti** for at reservere det fulde antal på den valgte linje på lagerstedet.
1. Luk siden **Reservation** for at vende tilbage til salgsordren.
1. Vælg **Frigiv til lagersted** i gruppen **Handlinger** under fanen **Lagersted** i handlingsruden.
1. Du modtager en informativ meddelelse, der viser forsendelsen og bølgen for denne ordre. Bemærk, at der er oprettet to bølge-numre og to forsendelses-id-numre er blevet oprettet, et for hver leveringsmåde for salgsordrelinjerne.

#### <a name="get-the-work-ids-from-the-work-details"></a>Få arbejds-id'erne fra arbejdsdetaljerne

1. Gå til **Lokationsstyring \> Arbejde \> Arbejdsdetaljer**.
1. På siden vises de arbejds-id'er, der er oprettet ud fra salgsordrer. Brug bølge-id'erne og forsendelses-id'erne fra de salgsordrer, du har oprettet, til at finde arbejds-id'et for hver enkelt bølge og forsendelse. Noter dig disse arbejds-id'er, fordi du skal bruge dem i de næste trin. Bemærk, at der er oprettet to arbejds-id'er for den anden salgsordre. Hvis der plukkes forskellige varer fra forskellige lokationer, genereres der separate arbejds-id'er.

### <a name="pick-items-for-the-sales-orders"></a>Plukke varer til salgsordrerne

Fuldfør det oprettede arbejde ved at bruge mobilenheden til at flytte varerne til pakkestationen.

1. På mobilenheden skal du logge på lagerstedet *62* ved hjælp af det bruger-id, du har oprettet til dette scenarie (eller bruger-id'et for en eksisterende bruger af demodata).
1. I hovedmenuen skal du vælge **Udgående**.
1. I menuen **Udgående** skal du vælge **Salgspluk**.
1. I feltet **Id** skal du angive det arbejds-id, der er oprettet for salgsordre 1.
1. Vælg **OK**.
1. På siden **Salgsordrer – pluk** skal du angive et mål-NO, der blev oprettet til salgsordre 1. Bemærk, at pluklokation (*batch-001*), vare (*A0001*) og antal (*2 stk.*) vises.
1. Vælg **OK**.
1. Gennemse oplysningerne på siden **Salgsordrer – læg på lager**. Feltet **Lok** skal angive, at de plukkede varer skal placeres på lokationen *Pakke*.
1. Vælg **OK**.

    På siden **Scan et arbejds-id/nummerplade-id** modtager du en meddelelse om, at "Arbejde fuldført", hvilket angiver, at arbejds-id'et fra salgsordre 1 er blevet fuldført.

    Du skal nu plukke salgsordre 2.

1. I feltet **Id** skal du angive det arbejds-id, der er oprettet for salgsordre 2, hvor linje 1 har varen *A0001*.
1. Vælg **OK**.
1. På siden **Salgsordrer – pluk** skal du angive en mål-NP. Bemærk, at pluklokation (*batch-001*), vare (*A0001*) og antal (*1 stk.*) vises.
1. Vælg **OK**.
1. Gennemse oplysningerne på siden **Salgsordrer – læg på lager**. Feltet **Lok** skal angive, at de plukkede varer skal placeres på lokationen *Pakke*.
1. Vælg **OK**.

    På siden **Scan et arbejds-id/nummerplade-id** modtager du en meddelelse om, at "Arbejde er fuldført". Denne meddelelse angiver, at arbejds-id'et fra linje 1 i salgsordre 2 er fuldført.

1. I feltet **Id** skal du angive det arbejds-id, der er oprettet for salgsordre 2, hvor linje 2 har varen *A0002*.
1. Vælg **OK**.
1. På siden **Salgsordrer – pluk** skal du angive en mål-NP. Bemærk, at pluklokation (*batch-002*), vare (*A0001*) og antal (*1 stk.*) vises.
1. Vælg **OK**.
1. Gennemse oplysningerne på siden **Salgsordrer – læg på lager**. Feltet **Lok** skal angive, at de plukkede varer skal placeres på lokationen *Pakke*.
1. Vælg **OK**.

    På siden **Scan et arbejds-id/nummerplade-id** modtager du en meddelelse om, at "Arbejde er fuldført". Denne meddelelse angiver, at arbejds-id'et fra linje 2 i salgsordre 2 er fuldført.

### <a name="pack-sales-orders-into-containers"></a>Pakke salgsordrer i containere

#### <a name="pack-sales-order-1-into-containers"></a>Pakke salgsordre 1 i containere

1. Gå til **Lokationsstyring \> Pakning og containerisering \> Pakke**.

    Dialogboksen **Vælg pakkestation** vises. Som standard skal feltet **Arbejder** angives til navnet på den arbejder, som du konfigurerede tidligere.

1. Angiv følgende værdier for at få vist og arbejde med forsendelser og containere, der er planlagt på den specifikke pakkelokation:

    - **Lokation:** *6*
    - **Lagersted:** *62*
    - **Lokation:** *Pakke*
    - **Pakkeprofil-id:** *Sorter*

1. Vælg **OK** for at lukke dialogboksen.
1. Gå til siden **Pakke**, og angiv mål-NP'en for salgsordre 1 i feltet **Nummerplade eller forsendelse**. Vælg derefter tasten **Tabulator** eller **Retur** på tastaturet for at gå ud af feltet.
1. Gå til handlingsruden, og vælg **Ny container**.
1. Accepter alle standardindstillinger, og vælg **OK**. Notér dig container-id'et.
1. I oversigtspanelet **Varepakning** kan du angive følgende værdier:

    - **Antal:** *1*
    - **Id:** Vare *A0001*

1. Gå til handlingsruden, og vælg **Luk container**.
1. I dialogboksen **Luk container** skal du vælge **Hent systemvægt** for at få systemet til at opdatere feltet **Bruttovægt**.
1. Vælg **OK**. Containeren flyttes til lokationen *SORTER* og er klar til sortering.
1. Opret en anden container for at føje den anden vare fra NP'en til salgsordre 1 til en ny container.
1. Gå til handlingsruden, og vælg **Ny container**.
1. Accepter alle standardindstillinger, og vælg **OK**. Notér dig container-id'et.
1. I oversigtspanelet **Varepakning** kan du angive følgende værdier:

    - **Antal:** *1*
    - **Id:** Vare *A0001*

1. Gå til handlingsruden, og vælg **Luk container**.
1. I dialogboksen **Luk container** skal du vælge **Hent systemvægt** for at få systemet til at opdatere feltet **Bruttovægt**.
1. Vælg **OK**. Containeren flyttes til lokationen *SORTER* og er klar til sortering.

#### <a name="pack-sales-order-2-into-containers"></a>Pakke salgsordre 2 i containere

1. Gå til siden **Pakke**, og angiv mål-NP'en for linje 1 i salgsordre 2 i feltet **Nummerplade eller forsendelse**. Vælg derefter tasten **Tabulator** eller **Retur** på tastaturet for at gå ud af feltet.
1. Gå til handlingsruden, og vælg **Ny container**.
1. Accepter alle standardindstillinger, og vælg **OK**. Notér dig container-id'et.
1. I oversigtspanelet **Varepakning** kan du angive følgende værdier:

    - **Antal:** *1*
    - **Id:** Vare *A0001*

1. Gå til handlingsruden, og vælg **Luk container**.
1. I dialogboksen **Luk container** skal du vælge **Hent systemvægt** for at få systemet til at opdatere feltet **Bruttovægt**.
1. Vælg **OK**. Containeren flyttes til lokationen *SORTER* og er klar til sortering.
1. I feltet **Nummerplade eller forsendelse** skal du angive mål-NP for linje i salgsordre 2. Vælg derefter tasten **Tabulator** eller **Retur** på tastaturet for at gå ud af feltet.
1. Gå til handlingsruden, og vælg **Ny container**.
1. Accepter alle standardindstillinger, og vælg **OK**. Notér dig container-id'et.
1. I oversigtspanelet **Varepakning** kan du angive følgende værdier:

    - **Antal:** *1*
    - **Id-felt:** Vare *A0002*

1. Gå til handlingsruden, og vælg **Luk container**.
1. I dialogboksen **Luk container** skal du vælge **Hent systemvægt** for at få systemet til at opdatere feltet **Bruttovægt**.
1. Vælg **OK**. Containeren flyttes til lokationen *SORTER* og er klar til sortering.

Hvis du vil have vist containerdetaljerne, skal du gå til **Lokationsstyring \> Pakning og containerisering \> Containere** og søge efter det container-id, der blev oprettet under pakning.

### <a name="sort-the-containers"></a>Sortere containerne

> [!IMPORTANT]
> Når du åbner menupunktet **Palle-build** i mobilappen for at udføre udgående sortering, vises en knap med teksten **Fuld**. *Brug ikke knappen **Fuld** til at sortere eller lukke positionen.*
>
> Knappen **Fuld** er som standard tilgængelig og kan ikke deaktiveres eller fjernes fra siden. Den bruges ikke til den funktionen *Udgående sortering*.

#### <a name="sort-the-first-container"></a>Sortere den første beholder

1. På mobilenheden skal du logge på lagerstedet *62* ved hjælp af det bruger-id, du har oprettet til dette scenarie (eller bruger-id'et for en eksisterende bruger af demodata).
1. I hovedmenuen skal du vælge **Udgående**.
1. I menuen **Udgående** skal du vælge **Palle-build**.
1. Angiv det første container-id, der er knyttet til salgsordre 1, i feltet **NP/con**.
1. Vælg **OK**.
1. Da der ikke findes nogen sorteringspositioner i øjeblikket, skal du angive en. I feltet **Sorteringsposition-id** skal du angive *SP01*.
1. Da der i øjeblikket ikke er knyttet en NP til sorteringsplaceringen *SP01*, skal du angive en. I feltet **NP** skal du angive *PLP01*.
1. Vælg **OK**.
1. Da validering af sorteringsposition er slået til, skal du angive id'et for for sorteringspositionen igen. I feltet **Sorteringsposition-id** skal du angive *SP01*.
1. Vælg **OK**.

    Du modtager en meddelelse om, at "arbejde er fuldført".

> [!TIP]
> Hvis du vil have vist sorteringspositionen og NP'en på den, skal du gå til **Lokationsstyring \> Pakning og containerisering \> Positionstildelinger for udgående sortering**.
>
> Siden **Positionstildelinger for udgående sortering** vises alle de sorteringspositioner, der aktuelt er aktive. I feltet **Sorteringspositionstransaktioner** vises den NP, der er knyttet til hver enkelt sorteringsposition, og de containere, der findes i sorteringsposition. Bemærk, at der aktuelt findes én sorteringsposition, og at oversigtspanelet **Kriterier for sorteringsposition** viser et kriterium for **Forsendelsessted – fragtmand fly**.

#### <a name="sort-the-remaining-containers"></a>Sortere de resterende containerne

1. På mobilenheden skal du logge på lagerstedet *62* ved hjælp af det bruger-id, du har oprettet til dette scenarie (eller bruger-id'et for en eksisterende bruger af demodata).
1. I hovedmenuen skal du vælge **Udgående**.
1. I menuen **Udgående** skal du vælge **Palle-build**.
1. Angiv det andet container-id, der er knyttet til salgsordre 1, i feltet **NP/con**.
1. Vælg **OK**. Da sorteringsskabelonen er indstillet til automatisk sortering, og der allerede findes en sorteringsposition med overensstemmende kriterier, bliver du automatisk dirigeret til den korrekte sorteringsposition.
1. Vælg **OK**.
1. Bekræft sorteringspositions-id'et for at angive, at lageret er på det korrekte sted. I feltet **Sorteringsposition-id** skal du angive *SP01*.
1. Vælg **OK**.

    Arbejdet er fuldført på den anden container fra salgsordre 1. Du skal nu sortere de øvrige containere fra salgsordre 2.

1. Angiv container-id'et for containeren fra salgsordre 2, der indeholder vare **A0001**, i feltet *NP/con*. Da fragttjenesten er anderledes, bliver du bedt om at angive en ny sorteringsposition og tildele en NP til denne position. Brug sorteringsposition *SP02* og NP *PLP02*.
1. Vælg **OK**.
1. Bekræft sorteringspositionen ved at angive *SP02* i feltet **Sorteringsposition-id**.
1. Vælg **OK**.

    Arbejdet på containeren er udført.

1. Angiv container-id'et for den resterende container fra salgsordre 2, der indeholder vare **A0002**, i feltet *NP/con*. Da fragttjenesten er den samme som fragttjenesten for salgsordre 1, vil systemet vise den eksisterende sorteringsposition, der har de samme kriterier.
1. Vælg **OK**.
1. Bekræft sorteringspositionen ved at angive *SP01* i feltet **Sorteringsposition-id**.
1. Vælg **OK**.

    Arbejdet på containeren er udført.

### <a name="close-the-outbound-sorting-positions"></a>Luk positionerne for udgående sortering

Når alle lagre er sorteret, skal positionen lukkes, før der kan oprettes et arbejde. Der oprettes sorteret lagerpluk for at føre lageret til lagerporten.

#### <a name="close-a-position-from-the-mobile-device"></a>Lukke en position fra mobilenheden

1. På mobilenheden skal du logge på lagerstedet *62* ved hjælp af det bruger-id, du har oprettet til dette scenarie (eller bruger-id'et for en eksisterende bruger af demodata).
1. I hovedmenuen skal du vælge **Udgående**.
1. I menuen **Udgående** skal du vælge **Palle-build**.
1. I feltet **NP/con** skal du angive et container-id, der blev sorteret til sorteringsposition *SP01*.
1. Vælg **OK**.
1. Du får vist følgende meddelelse: "Containeren er allerede sorteret til position SP01. Vil du lukke positionen?" Vælg **Luk**.

    Arbejde er fuldført.

#### <a name="close-a-position-from-outbound-sorting-position-assignments"></a>Luk en position fra positionstildeling for udgående sortering

1. Gå til **Lagerlokation \> Pakning og containerisering \> Positonstildelinger for udgående sortering**.
1. I den venstre kolonne skal du vælge **SP02**. Denne position for udgående sortering er den, du vil lukke.
1. Gå til handlingsruden, og vælg **Luk position**. Posten med sorteringspositionen er lukket og vises ikke længere.

    > [!TIP]
    > Marker afkrydsningsfeltet **Vis lukket** for at få vist alle lukkede positionsposter.

### <a name="sorted-inventory-picking"></a>Sorteret lagerplukning

Du skal fuldføre arbejdet med sorteret lagerpluk. Når den er fuldført, plukkes lageret til salgsordren. På dette tidspunkt gælder alle andre lagerprocesser.

1. På mobilenheden skal du logge på lagerstedet *62* ved hjælp af det bruger-id, du har oprettet til dette scenarie (eller bruger-id'et for en eksisterende bruger af demodata).
1. I hovedmenuen skal du vælge **Udgående**.
1. I menuen **Udgående** skal du vælge **Sortering efter last fra**.
1. Angiv destinationens-NP-id fra den første sorteringsposition, *SP01*. Angiv feltet **Id** til *PLP01*.
1. Vælg **OK**.
1. Siden **Sorteret lagerpluk: pluk** viser det plukarbejde, der skal udføres. Pluk fra lokationen *SORTER* og mål-NP *PLP01*, der har flere varer og et antal på *3*.
1. Vælg **OK**.
1. Siden **Sorteret lagerpluk: læg på lager** viser det læg på lager-arbejde, der skal udføres. Læg på lager til lokationen *Lagerport* og mål-NP *PLP01*, der har flere varer og et antal på *3*.
1. Vælg **OK**.

    Arbejde er fuldført.

1. Angiv destinationsnummerplade-id'et fra den anden sorteringsposition, *SP02*. Angiv feltet **Id** til *PLP02*.
1. Vælg **OK**.
1. Siden **Sorteret lagerpluk: pluk** viser det plukarbejde, der skal udføres. Pluk fra lokationen *SORTER* og mål-NP *PLP02*, der har flere varer og et antal på *1*.
1. Vælg **OK**.
1. Siden **Sorteret lagerpluk: læg på lager** viser det læg på lager-arbejde, der skal udføres. Læg på lager til lokationen *Lagerport* og mål-NP *PLP02*, der har flere varer og et antal på *1*.
1. Vælg **OK**.

    Arbejde er fuldført.

Fra dette tidspunkt gælder alle andre lagerprocesser.
