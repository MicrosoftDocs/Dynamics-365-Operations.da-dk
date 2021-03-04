---
title: Konfigurere og bruge bølgeetiketudskrivning
description: Dette emne beskriver udskrivning af bølgeetiketter og forklarer, hvordan du konfigurerer det.
author: GarmMSFT
manager: PJacobse
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveLabel, WHSWaveLabelTemplate, WHSWaveLabelLayoutRow, WHSDocumentRouting, WHSWaveTableListPage, WHSPostMethod, WHSMobileDisplayWaveLabelListLookup, WHSWaveLabelType, WHSWaveLabelTemplateGroup, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: PJacobse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: yyyy-mm-dd
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 6314fd25d8d8a0013984d484f57a832c26f82b5a
ms.sourcegitcommit: a26e4963d40796da21ce6581cfb2f4d9db4f6776
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/27/2020
ms.locfileid: "4425069"
---
# <a name="set-up-and-use-wave-label-printing"></a>Konfigurere og bruge bølgeetiketudskrivning

[!include [banner](../includes/banner.md)]

Ved udskrivning af bølgeetiket kan du vælge en alternativ metode til udskrivning af etiketter ved at introducere en ny metode til bølgetrin, der giver dig mulighed for at oprette og udskrive etiketter direkte fra bølgeskabelonen under bølgeudførelse. Etiketterne vil derfor allerede være tilgængelige, før arbejderne kører arbejdsordren på en mobilenhed. Arbejderne kan derefter tilknytte de nødvendige etiketter under plukning i stedet for efter plukning.

Ved udskrivning af bølgeetiketter bruges ZPL (Zebra Programming Language) til oprettelse af etiketlayout. Et etiketlayout er inddelt i tre sektioner (overskrift, brødtekst og sidefod) for at give mulighed for etiketter med gentagelsesstruktur. Med bølgeetiketskabeloner kan du fortælle systemet, hvilket etiketlayout der skal bruges. Brugerne kan angive, hvilken printer der skal bruges. De kan også udskrive etiketter på flere printere på samme tid efter behov. Siden **Historik over bølgeetiketter** viser en oversigt over alle de etiketter, der er oprettet med denne opsætning.

Du kan udskrive og sortere etiketter ud fra arbejdsoverskrifterne, du kan udskrive brudetiketter efter arbejdsoverskrift, og og du kan udskrive containerindholdsetiketter, kasseetiketter og andre lignende etiketter.

> [!NOTE]
> Denne funktionalitet erstatter ikke eksisterende udskrivningsfunktioner for etiketter, der er baseret på dokumentdistribution.

Ved udskrivning af bølgeetiketter kan du vælge mellem følgende forbedringer:

- Udskriv etiketter i overensstemmelse med antallet af kartoner på en enkelt arbejdslinje uden brug af containerisering. (En "karton" er en enhed, der er angivet i enhedsseriegruppelinjer.)
- Udskriv flere forskellige etiketserier (f.eks. kartoner og palleetiketter).
- Medtag etiketfasttekst (f.eks. 1/124, 2/124,... 124/124), og definer intervallet for fasttekst (f.eks. arbejdslinje, lastlinje eller forsendelse).
- Opret og udskriv et fragtseddel-id på etiketter, før fragtsedlen genereres.
- Opret en entydig SSCC (serial shipping container code) for hver enkelt karton, og medtag den på hver etiket.
- Opret GS1-kompatible nummerserier til fragtseddel-id'er og SSCC'er.
- Genudskriv etiketter både fra mobilenheder og den detaljerede klient.
- Annuller etiketter (f.eks. i korte pluk-scenarier), og udskriv dem igen.
- Rydde op i historikken over bølgeetiketter.
- Forbedringer af layoutene til dokumentruteplanlægning deles mellem layoutene til dokumentruteplanlægning og bølgeetiketlayout. (Yderligere oplysninger finder du i [Dokumentruteplanlægning for layout til id-etiketter](../warehousing/document-routing-layout-for-license-plates.md).)

Disse forbedringer gør det mere effektivt at mærke kartoner før palletisering. De er særligt fordelagtige for firmaer, der leverer til store detailhandlere, der automatisk bekræfter ordretilgang ved at scanne hver enkelt karton separat.

> [!NOTE]
> Du kan implementere de konfigurationsscenarier, der er beskrevet i dette emne, enten enkeltvis eller i kombination, afhængigt af dine forretningskrav. Du kan designe flere bølgeetiketskabeloner, der fungerer i rækkefølge (som vist i scenarie 3). Du kan f.eks. bruge scenarie 1 til at udskrive kartoner og scenarie 2 til at udskrive palleetiketter (hvis paller på lager er forskellig i størrelse og sammensætning).

## <a name="turn-on-the-wave-label-printing-feature"></a>Slå funktionen til udskrivning af bølgeetiketter til

Før du kan bruge funktionen *Udskrivning af bølgeetiketter*, skal den være aktiveret i dit system. Administratorer kan bruge området [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov. Dér vises funktionen på følgende måde:

- **Modul:** *Lokationsstyring*
- **Funktionsnavn:** *Udskrivning af bølgeetiketter*

## <a name="scenario-1-wave-label-printing-where-a-single-wave-label-is-generated"></a>Scenarie 1: Udskrivning af bølgeetiketter, hvor der genereres en enkelt bølgeetiket

Dette scenarie viser, hvordan et firma kan udskrive forsendelsesetiketter for en stor forhandler, der automatisk bekræfter ordretilgange ved at scanne hver enkelt karton for sig.

Dette scenarie viser forløbet fra start til slut.

### <a name="make-demo-data-available"></a>Gøre demodata tilgængelige

Hvis du vil følge dette scenarie skal du have installeret demodata, og du skal bruge den juridiske enhed **USMF**.

### <a name="make-sure-that-the-wave-label-method-is-available"></a>Kontroller, at bølgeetiketmetoden er tilgængelig

Du skal muligvis oprette bølgeprocesmetoderne igen for at gøre metoden til bølgeetiketudskrivning tilgængelig.

1. Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgeprocesmetoder**.
1. Kontroller, at **bølgeEtiketUdskrivning** findes på listen. Hvis den ikke gør det, skal du vælge **Genopret metoder** i handlingsruden for at tilføje den.

### <a name="configure-a-wave-template"></a>Konfigurere en bølgeskabelon

Med bølgeskabeloner kan du knytte bestemte forekomster af bølgemetoder til en tilsvarende bølgeetiketskabelon.

1. Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgeskabeloner**.
1. Vælg en skabelon som f.eks. **62 Forsendelsesstandard**.
1. I oversigtspanelet **Metoder** skal du flytte metoden **Udskrivning af bølgeetiketter** til kolonnen **Valgte metoder**.
1. I kolonnen **Valgte metoder** skal du vælge metoden **Udskrivning af bølgeetiketter** og angive feltet **Bølgetrinskode** til *UdskrivEtiket*. Du kan få flere oplysninger om bølgetrinkoder under [Bølgetrinkoder](wave-step-codes.md).

### <a name="create-a-wave-label-layout"></a>Oprette et bølgeetiketlayout

Etiketlayoutet bestemmer, hvilke oplysninger der udskrives på etiketten, og hvordan de er opstillet. Her skal du angive den ZPL-kode, der sendes til printeren.

1. Gå til **Lokationsstyring \> Opsætning \> Dokumentruteplanlægning \> Bølgeetiketlayout**.
1. Opret en post, der har følgende indstillinger:

    - **Etiketlayout-id:** *karton*
    - **Beskrivelse:** *Karton (SSCC)*

1. Vælg **Gem** i handlingsruden.
1. Vælg **Indstillinger for bølgeetiketrækker** i handlingsruden.

    Siden **Indstillinger for bølgeetiketrækker** vises. Her kan du konfigurere den dynamiske del af etiketten.

1. Tilføj en række, der har følgende indstillinger:

    - **Række-id:** *Bølgeetiket*
    - **Rækketabelnavn:** *WHS-bølgeetiket*
    - **Startposition for række:** *0*

        I dette felt defineres den lodrette position, hvor rækken skal begynde på etiketten.

    - **Rækkehøjde:** *0*

        I dette felt defineres højden af hver række (i punkter) i henhold til ZPL-standarden. Rækkehøjden er positiv for vandrette etiketter og negative for lodrette etiketter. Da der kun er én række i dette eksempel, kan du angive værdien til *0* (nul).

    - **Rækker pr. side:** *1*

        Dette felt definerer det antal rækker, der kan udskrives på hver etiket.

        > [!NOTE]
        > Denne opsætning medfører, at der udskrives en separat ZPL-etiket for hver post i tabellen Bølgeetiketter.

1. Luk siden.
1. Vælg **Rediger forespørgsel** i handlingsruden.
1. I dialogboksen for forespørgselseditor skal du under fanen **Område** tilføje en række, der har følgende indstillinger:

    - **Tabel:** *Arbejdslinjer*
    - **Afledt tabel:** *Arbejdslinjer*
    - **Felt:** *Arbejdstype*
    - **Kriterier:** *Pluk*

    Denne forespørgsel sikrer, at der kun udskrives arbejdslinjer af pluktypen på etiketten og ikke arbejdslinjer af læg på lager-typen.

1. Hvis du vil have mulighed for at udskrive fragtseddel-id'et, skal du under fanen **Join-forbindelser** vælge tabellen **Arbejdslinje** og knytte tabellen **Forsendelser** til den.
1. Luk dialogboksen for forespørgselseditoren.
1. Oversigtspanelet **Layout af printertekst** indeholder tre sektioner, hvor du kan skrive printerkode: **Sidehoved**, **Brødtekst** og **Sidefod**. I sektionen **Sidehoved** skal du i feltet **Etiketsidehoved** angiv en kode for det påkrævede sidehoved. Hvis du f. eks. bruger Zebra-printere, kan du bruge følgende kode.

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. I sektionen **Brødtekst** skal du i feltet **Etiketbrødtekst** angiv en ZPL-kode for den påkrævede brødtekst. Her er et eksempel.

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. I sektionen **Brødtekst** skal du i feltet **Etiketsidefod** angiv en ZPL-kode for den påkrævede sidefod. Her er et eksempel.

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > Denne opsætning vil udskrive én kopi af hver etiket. Hvis du har brug for flere kopier (f.eks. én kopi for hver side af pallen), skal du angive værdien **n-** for **\^PQn** i sidefoden til det påkrævede antal kopier. Hvis du f.eks. vil udskrive fire kopier af hver etiket, skal du angive **\^PQ4**.

Din etiket er nu klar til brug.

### <a name="create-a-wave-label-type"></a>Oprette et bølgeetikettype

Bølgeetikettyper bruges til at knytte bølgeetiketskabeloner til en enhed på enhedsseriegruppelinjer.

1. Gå til **Lokationsstyring \> Opsætning \> Dokumentruteplanlægning \> Bølgeetikettyper**.
1. Tilføj en bølgetype, der har følgende indstillinger:

    - **Etikettype:** *Karton*
    - **Beskrivelse:** *Karton*

### <a name="set-up-unit-sequence-groups"></a>Konfigurer enhedsseriegrupper

Konfigurer derefter enhedsseriegruppen for bølgeetikettypen.

1. Gå til **Lokationsstyring \> Opsætning \> Lagersted \> Enhedsseriegrupper**.
1. Vælg gruppen **Hver boks PL**.
1. For linjen **Boks** skal du indstille feltet **Bølgeniveautype** til *Karton*.

### <a name="create-a-wave-label-template"></a>Oprette et bølgeetiketskabelon

Opret derefter en bølgeetiketskabelon til bølgeetikettypen.

1. Gå til **Lokationsstyring \> Opsætning \> Dokumentruteplanlægning \> Bølgeetiketskabeloner**.
1. Føj en bølgeniveauskabelon, og angiv følgende værdier i sidehovedet:

    - **Navn på etiketskabelon:** *Kartonetiketter*
    - **Beskrivelse:** *Kartonetiketter*
    - **Kode for bølgetrin:** *UdskrivEtiket*
    - **Lagersted:** *62*

1. Gå til oversigtspanelet **Generelt**, og indstil feltet **Bølgeetikettype**  til *Karton*.
1. I oversigtspanelet **Detaljer om bølgeetiketskabeloner** skal du tilføje en ny række, der har følgende indstillinger:

    - **Etiketlayout-id:** *karton*
    - **Printernavn:** Vælg en relevant ZPL-printer.
    - **Kør forespørgsel:** *Ja* (denne indstilling er valgfri, men den anbefales for at opnå den optimale ydeevne).

1. Vælg **Gem** i handlingsruden.
1. Valgfrit: Hvis du konfigurerer et kundespecifikt etiketdesign, skal du oprette en forespørgsel for at finde kundens konto. Gå til oversigtspanelet **Detaljer om bølgeetiketskabeloner**, og vælg **Rediger forespørgsel**. I dialogboksen for forespørgselseditor skal du derefter under fanen **Område** tilføje en række, der har følgende indstillinger:

    - **Tabel:** *Forsendelser*
    - **Afledt tabel:** *Forsendelser*
    - **Felt:** *Kontonummer*
    - **Kriterier:** Angiv det relevante debitorkontonummer.

    Når du er færdig, skal du vælge **OK** for at lukke dialogboksen for forespørgselseditor.

1. I handlingsruden skal du vælge **Rediger forespørgsel** for at at åbne dialogboksen for forespørgselseditoren for hele etiketskabelonen.
1. I dialogboksen for forespørgselseditor skal du under fanen **Sortering** tilføje en række, der har følgende indstillinger:

    - **Tabel:** *Arbejdslinjer*
    - **Afledt tabel:** *Arbejdslinjer*
    - **Felt:** *Referencelastlinje-id (post-id)*
    - **Søgeretning:** *Stigende*

1. Vælg **OK** for at lukke dialogboksen for forespørgselseditoren.
1. I en meddelelsesboks beder dig om at bekræfte nulstillingen af grupperingsfunktionen. Vælg **Ja** for at fortsætte.
1. Gå til handlingsruden, og vælg **Gruppe af bølgeetiketskabeloner**.
1. I dialogboksen **Gruppe af bølgeetiketskabeloner** skal du vælge den række, hvor feltet **Referencefeltnavn** er indstillet til *Referencelastlinje-id* og derefter markere afkrydsningsfeltet **Etiket-build-id** for denne række.

    > [!NOTE]
    > Denne opsætning opretter en etiketserie ("karton 1 af X") pr. lastlinje i hele bølgen, uanset opsætningen af arbejdsgrupperingen. Denne etiketserie kan udskrives på etiketlayoutet.

### <a name="configure-number-sequence-extensions"></a>Konfigurere nummerserieudvidelser

Nummerserieudvidelser styrer GS1-overholdelse af specifikke nummerserier. Denne konfiguration er valgfri for det aktuelle scenarie. Du kan finde flere oplysninger og konfigurationsinstruktioner under [Konfigurere nummerserieudvidelser](../warehousing/configure-number-sequence-extensions.md).

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Oprette en salgsordre og frigive den til lagerstedet

1. Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.
1. Opret salgsordre, der har følgende indstillinger:

    - **Debitorkonto:** *US-001*
    - **Lagersted:** *62*

1. Tilføj to salgslinjer, der har følgende indstillinger.

    - Salgsordrelinje 1:

        - **Varenummer:** *A0001*
        - **Antal:** *9024*
        - **Enhed:** *hver* (9024 hver = 376 boks = 47 PL)

    - Salgsordrelinje 2:

        - **Varenummer:** *A0002*
        - **Antal:** *9016*
        - **Enhed:** *hver* (9016 hver = 322 boks = 46 PL)

    > [!NOTE]
    > De varer og antal, der angives her, er kun eksempler. De skal bruge den enhedsseriegruppe, du har defineret tidligere, relevante enhedskonverteringer fra *hver* til *boks* til *PL* skal defineres for dem, og de skal have lager på lagerstedet *62*. Du kan finde flere oplysninger i [Måleenhed og lagerføringspolitikker](unit-measure-stocking-policies.md).

1. Vælg salgsordrelinje 1. I sektionen **Salgsordrelinje** skal du i menuen **Lager** vælge **Reservationer**.
1. På siden **Reservation** skal du i handlingsruden vælge **Reserver parti** og derefter lukke siden.
1. Gentag trin 4 og 5 for salgsordrelinje 2.
1. Vælg **Frigør til lagersted** under fanen **Lagersted** i handlingsruden.

    Følgende hændelser forekommer:

    - Systemet behandler den oprettede forsendelse ved hjælp af den skabelon, der indeholder trinnet til udskrivning af etiketter. Etiketlayoutet bruges til at definere etikettens format, og resultatet vil være en etiket, der udskrives på den printer, der er valgt i etiketskabelonen.
    - Der genereres og udskrives bølgeetiketter. Antallet af etiketter vil være lig med antallet af kartoner (i dette eksempel 376 boks-etiketter til linje 1 og 322 boks-etiketter til linje 2).
    - Der genereres et nyt fragtseddel-id for forsendelserne. Hvis du har konfigureret nummerserieudvidelserne, følger bølgeetiket-id'erne **SSCC-18**-nummerformatet. 

Du kan få vist og udskrive bølgeetiketter fra følgende sider. Gå til handlingsruden på enhver side, og vælg **Bølgeetiketter** i gruppen **Relaterede oplysninger** under fanen **Forsendelser**.

- Alle forsendelser \> Forsendelsesoplysninger
- Alle laster \> Lastdetaljer
- Alle bølger
- Bølgelabels
- Historik for bølgelabel

## <a name="scenario-2-wave-label-printing-for-containerization-without-wave-label-records"></a>Scenarie 2: Udskrivning af bølgeetiketter til containerisering (uden bølgeetiketposter)

I dette scenarie kan du udskrive bølgeetiketter, når du bruger containerisering, til automatisk opdeling af varer i kartoner, og du har derfor ikke brug for en bølgeetiketpost. I dette tilfælde fungerer container-id'et som pladsholder for SSCC.

Her er de væsentligste forskelle mellem dette scenarie og scenario 1:

- **Bølgeetiketskabeloner:** Du kan ikke vælge en bølgeetikettype, og du behøver ikke en gruppering af etiketbuilds. Ellers skal du konfigurere bølgeetiketskabelonen og oprette en kæde til bølgeskabelonen på samme måde som beskrevet i scenarie 1. Du skal lade bølgeetikettypen være tom, hvis der ikke skal genereres bølgeetiketter.
- **Bølgeetiketlayout:** Du kan konfigurere række indstillingerne for bølgeetiketlayoutet for arbejdslinjer i stedet for bølgeetiketposter. Du skal konfigurere rækkeindstillingen for etiketlayoutet ved hjælp af tabellen **WHSArbejdslinje** i stedet for tabellen **WHS-Bølgeetiket**. Indstillingen **Rækker pr. side** bestemmer det antal rækker, som brødtekstsektionen skal indeholde. 

Denne konfiguration er også velegnet til forretningssituationer, hvor flere forskellige varer pakkes ind i én mærket boks eller på en palle, og denne pakkeproces kan defineres ved oprettelse af arbejde (f.eks. arbejde, der er grupperet efter forsendelse).

Dette scenarie viser forløbet fra start til slut.

### <a name="make-demo-data-available"></a>Gøre demodata tilgængelige

Hvis du vil følge dette scenarie skal du have installeret demodata, og du skal bruge den juridiske enhed **USMF**.

### <a name="make-sure-that-the-wave-label-method-is-available"></a>Kontroller, at bølgeetiketmetoden er tilgængelig

Du skal muligvis oprette bølgeprocesmetoderne igen for at gøre metoden til bølgeetiketudskrivning tilgængelig.

1. Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgeprocesmetoder**.
1. Kontroller, at **bølgeEtiketUdskrivning** findes på listen. Hvis den ikke gør det, skal du vælge **Genopret metoder** i handlingsruden for at tilføje den.

### <a name="set-up-a-wave-template"></a>Konfigurere en bølgeskabelon

Med bølgeskabeloner kan du knytte bestemte forekomster af bølgemetoder til en tilsvarende bølgeetiketskabelon.

1. Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgeskabeloner**.
1. Vælg en skabelon som f.eks. **63 Containerisering**.
1. I oversigtspanelet **Metoder** skal du flytte metoden **Udskrivning af bølgeetiketter** til kolonnen **Valgte metoder**.
1. I kolonnen **Valgte metoder** skal du vælge metoden **Udskrivning af bølgeetiketter** og angive feltet **Bølgetrinskode** til *UdskrivEtiket*. Du kan få flere oplysninger om bølgetrinkoder under [Bølgetrinkoder](wave-step-codes.md).

### <a name="create-a-wave-label-layout"></a>Oprette et bølgeetiketlayout

1. Gå til **Lokationsstyring \> Opsætning \> Dokumentruteplanlægning \> Bølgeetiketlayout**.
1. Opret en post, der har følgende indstillinger:

    - **Etiketlayout-id:** *karton*
    - **Beskrivelse:** *Karton (SSCC)*

1. Vælg **Gem** i handlingsruden.
1. Vælg **Indstillinger for bølgeetiketrækker** i handlingsruden.

    Siden **Indstillinger for bølgeetiketrækker** vises. Her kan du konfigurere den dynamiske del af etiketten.

1. Tilføj en række, der har følgende indstillinger:

    - **Række-id:** *Arbejdslinje*
    - **Rækketabelnavn:** *WHS-arbejdslinje*
    - **Startposition for række:** *500*

        I dette felt defineres den lodrette position, hvor rækken skal begynde på etiketten.

    - **Rækkehøjde:** *-50*

        I dette felt defineres højden af hver række. Rækkehøjden er positiv for vandrette etiketter og negative for lodrette etiketter.

    - **Rækker pr. side:** *5*

        Dette felt definerer det antal rækker, der kan udskrives på hver etiket.

        > [!NOTE]
        > Denne opsætning vil udskrive flere ZPL-etiketter pr. arbejde, hvor hver side kan indeholde op til fem arbejdslinjer. Hvis der f.eks. udskrives en etiket for en container med 12 linjer, udskrives der tre etiketter. Hvis du vil udskrive en separat label for hver pluklinje, skal du angive denne værdi til *1*.

1. Luk siden.
1. Vælg **Rediger forespørgsel** i handlingsruden.
1. I dialogboksen for forespørgselseditor skal du under fanen **Område** tilføje en række, der har følgende indstillinger:

    - **Tabel:** *Arbejdslinjer*
    - **Afledt tabel:** *Arbejdslinjer*
    - **Felt:** *Arbejdstype*
    - **Kriterier:** *Pluk*

1. Hvis du vil have mulighed for at udskrive fragtseddel-id'et, skal du under fanen **Join-forbindelser** vælge tabellen **Arbejdslinje** og knytte tabellen **Forsendelser** til den.
1. Luk dialogboksen for forespørgselseditoren.
1. Oversigtspanelet **Layout af printertekst** indeholder tre sektioner, hvor du kan skrive printerkode: **Sidehoved**, **Brødtekst** og **Sidefod**. I sektionen **Sidehoved** skal du i feltet **Etiketsidehoved** angiv en kode for det påkrævede sidehoved. Hvis du f. eks. bruger Zebra-printere, kan du bruge følgende kode.

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkTable.ContainerId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. I sektionen **Brødtekst** skal du i feltet **Etiketbrødtekst** angiv en ZPL-kode for den påkrævede brødtekst. Her er et eksempel.

    ```plaintext
    <Row name="WorkLine">
    <Heading>
    //Optional heading for section of rows
    </Heading>
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWorkLine.ItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWorkLine.QtyWork$ ^FS
    </Row>
    ```

1. I sektionen **Brødtekst** skal du i feltet **Etiketsidefod** angiv en ZPL-kode for den påkrævede sidefod. Her er et eksempel.

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > Denne opsætning vil udskrive én kopi af hver etiket. Hvis du har brug for flere kopier (f.eks. én kopi for hver side af pallen), skal du angive værdien **n-** for **\^PQn** i sidefoden til det påkrævede antal kopier. Hvis du f.eks. vil udskrive fire kopier af hver etiket, skal du angive **\^PQ4**.

Din etiket er nu klar til brug.

### <a name="create-a-wave-label-template"></a>Oprette et bølgeetiketskabelon

1. Gå til **Lokationsstyring \> Opsætning \> Dokumentruteplanlægning \> Bølgeetiketskabeloner**.
1. Føj en bølgeniveauskabelon, og angiv følgende værdier i sidehovedet:

    - **Navn på etiketskabelon:** *Containeretiketter*
    - **Beskrivelse:** *Containeretiketter*
    - **Kode for bølgetrin:** *UdskrivEtiket*
    - **Lagersted:** *63*

1. I oversigtspanelet **Detaljer om bølgeetiketskabeloner** skal du tilføje en række, der har følgende indstillinger:

    - **Etiketlayout-id:** *Container*
    - **Printernavn:** Vælg en relevant ZPL-printer.
    - **Kør forespørgsel:** *Ja* (denne indstilling er valgfri, men den anbefales for at opnå den optimale ydeevne).

1. Vælg **Gem** i handlingsruden.
1. Valgfrit: Hvis du konfigurerer et kundespecifikt etiketdesign, skal du oprette en forespørgsel for at finde kundens konto. Gå til oversigtspanelet **Detaljer om bølgeetiketskabeloner**, og vælg **Rediger forespørgsel**. I dialogboksen for forespørgselseditor skal du derefter under fanen **Område** tilføje en række, der har følgende indstillinger:

    - **Tabel:** *Forsendelser*
    - **Afledt tabel:** *Forsendelser*
    - **Felt:** *Kontonummer*
    - **Kriterier:** Angiv det relevante debitorkontonummer.

    Når du er færdig, skal du vælge **OK** for at lukke dialogboksen for forespørgselseditor.

### <a name="configure-number-sequence-extensions"></a>Konfigurere nummerserieudvidelser

Nummerserieudvidelser styrer GS1-overholdelse af specifikke nummerserier. Denne konfiguration er valgfri for det aktuelle scenarie. Du kan finde flere oplysninger og konfigurationsinstruktioner under [Konfigurere nummerserieudvidelser](../warehousing/configure-number-sequence-extensions.md).

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Oprette en salgsordre og frigive den til lagerstedet

1. Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.
1. Opret salgsordre, der har følgende indstillinger:

    - **Debitorkonto:** *US-001*
    - **Lagersted:** *63*

1. Tilføj fem salgsordrelinjer:

    - Salgsordrelinje 1:

        - **Varenummer:** *A0001*
        - **Antal:** *10*

    - Salgsordrelinje 2:

        - **Varenummer:** *A0002*
        - **Antal:** *20*

    - Salgsordrelinje 3:

        - **Varenummer:** *L0006*
        - **Antal:** *20*

    - Salgsordrelinje 4:

        - **Varenummer:** *L0100*
        - **Antal:** *40*

    - Salgsordrelinje 5:

        - **Varenummer:** *L0101*
        - **Antal:** *50*

    > [!NOTE]
    > De varer og antal, der angives her, er kun eksempler. De skal være lager på det angivne lagersted.

1. Vælg salgsordrelinje 1. I sektionen **Salgsordrelinje** skal du i menuen **Lager** vælge **Reservationer**.
1. På siden **Reservation** skal du i handlingsruden vælge **Reserver parti** og derefter lukke siden.
1. Gentag trin 4 og 5 for hver ekstra salgsordrelinje.
1. Vælg **Frigør til lagersted** under fanen **Lagersted** i handlingsruden.

    Følgende hændelser forekommer:

    - Systemet behandler den oprettede forsendelse ved hjælp af den skabelon, der indeholder trinnet til udskrivning af etiketter. Etiketlayoutet bruges til at definere etikettens format, og slutresultatet vil være en etiket, der har fem linjer, og som udskrives på den printer, der er valgt i etiketskabelonen.
    - Der genereres et nyt fragtseddel-id for forsendelserne. Hvis du har konfigureret nummerserieudvidelserne, følger bølgeetiket-id'erne **SSCC-18**-nummerformatet. 

Du kan udskrive disse bølgeetiketter igen ved at gå til **Lokationsstyring \> Forespørgsler og rapporter \> Historik over bølgeetiketter**.

## <a name="scenario-3-wave-label-printing-for-multi-tiered-labels"></a>Scenarie 3: Udskrivning af bølgeetiketter til etiketter med flere niveauer

Dette scenarie viser, hvordan du kan bruge funktionen til udskrivning af bølgeetiketter, når lagerprocesserne kræver flere niveauer af forsendelsesetiketter. Der kan f eks. være adskilte etiketter for kartoner og paller, og det kan være nødvendigt at udskrive en brudetiket for hele forsendelsen. Brudetiketter er en separat type etiket, der kan bruges som delelinje mellem ruller og containere, f eks. etiketter til forsendelses-id'et og en stregkode, så etiketterne nemt kan sorteres, når de er udskrevet.

Den væsentligste forskel mellem konfigurationen af dette scenarie og konfigurationen af scenarie 1, ud over det faktum, at etiketter er aktiveret, er, at der skal knyttes flere bølgeetikettyper til linjerne i enhedsseriegrupperne. Hvis du vil udføre denne konfiguration, skal du konfigurere følgende elementer for dette scenarie:

- **Bølgebehandlingsmetoder:** Du kan markere bølgeetiketmetoden som "kan gentages", føje den to (eller flere) gange til bølgeskabelonen og angive forskellige bølgetrinskoder.
- **Bølgeetiketskabeloner:** Du kan konfigurere bølgeetiketskabelonerne og knytte dem til bølgeskabelonen. Hver enkelt bølgeetiketskabelon har sin egen bølgeetikettype.
- **Bølgeetiketlayout:** Du kan oprette flere bølgeetiketlayout. Der vil være et separat etiketlayout for hvert "lag" af etiketter, og der vil også være et brudetiketlayout.

Dette scenarie viser forløbet fra start til slut.

### <a name="make-demo-data-available"></a>Gøre demodata tilgængelige

Hvis du vil følge dette scenarie skal du have installeret demodata, og du skal bruge den juridiske enhed **USMF**.

### <a name="set-up-a-wave-process-method"></a>Konfigurere en bølgebehandlingsmetode

1. Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgeprocesmetoder**.
1. Kontroller, at **bølgeEtiketUdskrivning** findes på listen. Hvis den ikke gør det, skal du vælge **Genopret metoder** i handlingsruden for at tilføje den.
1. Når det gælder metoden **bølgeEtiketUdskrivning** skal du markere afkrydsningsfeltet **Gør metode reperterbar**.

### <a name="set-up-a-wave-template"></a>Konfigurere en bølgeskabelon

1. Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgeskabeloner**.
2. Vælg en skabelon som f.eks. **62 Forsendelsesstandard**.
3. I oversigtspanelet **Metoder** skal du flytte metoden **Udskrivning af bølgeetiketter** til kolonnen **Valgte metoder**.
4. I kolonnen **Valgte metoder** skal du tildele en værdi for **Bølgetrinkode** som f.eks. *Karton* til metoden **Udskrivning af bølgeetiketter**. Du kan få flere oplysninger om bølgetrinkoder under [Bølgetrinkoder](wave-step-codes.md).
5. Flyt metoden **Udskrivning af bølgeetiketter** til kolonnen **Valgte metoder** en gang mere.
6. I kolonnen **Valgte metoder** skal du tildele en anden værdi for **Bølgetrinkode** som f.eks. *Palle* til den anden metode til **Udskrivning af bølgeetiketter**. Du kan få flere oplysninger om bølgetrinkoder under [Bølgetrinkoder](wave-step-codes.md).

### <a name="create-three-wave-label-layouts"></a>Oprette tre bølgeetiketlayout

1. Gå til **Lokationsstyring \> Opsætning \> Dokumentruteplanlægning \> Bølgeetiketlayout**.
1. Opret en post, der har følgende indstillinger:

    - **Etiketlayout-id:** *karton*
    - **Beskrivelse:** *Karton (SSCC)*

1. Vælg **Gem** i handlingsruden.
1. Vælg **Indstillinger for bølgeetiketrækker** i handlingsruden.

    Siden **Indstillinger for bølgeetiketrækker** vises. Her kan du konfigurere den dynamiske del af etiketten.

1. Tilføj en række, der har følgende indstillinger:

    - **Række-id:** *Bølgeetiket*
    - **Rækketabelnavn:** *WHS-bølgeetiket*
    - **Startposition for række:** *0*

        I dette felt defineres den lodrette position, hvor rækken skal begynde på etiketten.

    - **Rækkehøjde:** *0*

        I dette felt defineres højden af hver række (i punkter) i henhold til ZPL-standarden. Rækkehøjden er positiv for vandrette etiketter og negative for lodrette etiketter. Da der kun er én række i dette eksempel, kan du angive værdien til *0* (nul).

    - **Rækker pr. side:** *1*

        Dette felt definerer det antal rækker, der kan udskrives på hver etiket.

        > [!NOTE]
        > Denne opsætning medfører, at der udskrives en separat ZPL-etiket for hver post i tabellen Bølgeetiketter.

1. Luk siden.
1. Vælg **Rediger forespørgsel** i handlingsruden.
1. I dialogboksen for forespørgselseditor skal du under fanen **Område** tilføje en række, der har følgende indstillinger:

    - **Tabel:** *Arbejdslinjer*
    - **Afledt tabel:** *Arbejdslinjer*
    - **Felt:** *Arbejdstype*
    - **Kriterier:** *Pluk*

    Denne forespørgsel sikrer, at der kun udskrives arbejdslinjer af pluktypen på etiketten og ikke arbejdslinjer af læg på lager-typen.

1. Hvis du vil have mulighed for at udskrive fragtseddel-id'et, skal du under fanen **Join-forbindelser** vælge tabellen **Arbejdslinje** og knytte tabellen **Forsendelser** til den. 
1. Luk dialogboksen for forespørgselseditoren.
1. Oversigtspanelet **Layout af printertekst** indeholder tre sektioner, hvor du kan skrive printerkode: **Sidehoved**, **Brødtekst** og **Sidefod**. I sektionen **Sidehoved** skal du i feltet **Etiketsidehoved** angiv en kode for det påkrævede sidehoved. Hvis du f. eks. bruger Zebra-printere, kan du bruge følgende kode.


    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. I sektionen **Brødtekst** skal du i feltet **Etiketbrødtekst** angiv en ZPL-kode for den påkrævede brødtekst. Her er et eksempel.

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. I sektionen **Brødtekst** skal du i feltet **Etiketsidefod** angiv en ZPL-kode for den påkrævede sidefod. Her er et eksempel.

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > Denne opsætning vil udskrive én kopi af hver etiket. Hvis du har brug for flere kopier (f.eks. én kopi for hver side af pallen), skal du angive værdien **n-** for **\^PQn** i sidefoden til det påkrævede antal kopier. Hvis du f.eks. vil udskrive fire kopier af hver etiket, skal du angive **\^PQ4**.

1. Den første etiket er nu klar til brug.
1. Opret en anden layoutpost, der har følgende indstillinger:

    - **Etiketlayout-id:** *Pakke*
    - **Beskrivelse:** *Palle*

1. Vælg **Gem** i handlingsruden.
1. Vælg **Indstillinger for bølgeetiketrækker** i handlingsruden.

    Siden **Indstillinger for bølgeetiketrækker** vises. Her kan du konfigurere den dynamiske del af etiketten.

1. Tilføj en række, der har følgende indstillinger:

    - **Række-id:** *Bølgeetiket*
    - **Rækketabelnavn:** *WHS-bølgeetiket*
    - **Startposition for række:** *0*

        I dette felt defineres den lodrette position, hvor rækken skal begynde på etiketten.

    - **Rækkehøjde:** *0*

        I dette felt defineres højden af hver række (i punkter) i henhold til ZPL-standarden. Rækkehøjden er positiv for vandrette etiketter og negative for lodrette etiketter. Da der kun er én række i dette eksempel, kan du angive værdien til *0* (nul).

    - **Rækker pr. side:** *1*

        Dette felt definerer det antal rækker, der kan udskrives på hver etiket.

        > [!NOTE]
        > Denne opsætning medfører, at der udskrives en separat ZPL-etiket for hver post i tabellen Bølgeetiketter.

1. Luk siden.
1. Vælg **Rediger forespørgsel** i handlingsruden.
1. I dialogboksen for forespørgselseditor skal du under fanen **Område** tilføje en række, der har følgende indstillinger:

    - **Tabel:** *Arbejdslinjer*
    - **Afledt tabel:** *Arbejdslinjer*
    - **Felt:** *Arbejdstype*
    - **Kriterier:** *Pluk*

    Denne forespørgsel sikrer, at der kun udskrives arbejdslinjer af pluktypen på etiketten og ikke arbejdslinjer af læg på lager-typen.

1. Hvis du vil have mulighed for at udskrive fragtseddel-id'et, skal du under fanen **Join-forbindelser** vælge tabellen **Arbejdslinje** og knytte tabellen **Forsendelser** til den.
1. Luk dialogboksen for forespørgselseditoren.
1. Oversigtspanelet **Layout af printertekst** indeholder tre sektioner, hvor du kan skrive printerkode: **Sidehoved**, **Brødtekst** og **Sidefod**. I sektionen **Sidehoved** skal du i feltet **Etiketsidehoved** angiv en kode for det påkrævede sidehoved. Hvis du f. eks. bruger Zebra-printere, kan du bruge følgende kode.

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWaveLabel.WaveLabelId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. I sektionen **Brødtekst** skal du i feltet **Etiketbrødtekst** angiv en ZPL-kode for den påkrævede brødtekst. Her er et eksempel.

    ```plaintext
    <Row name="WaveLabel">
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWaveLabel.LabelItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWaveLabel.QtyWork$ ^FS
    </Row>
    ```

1. I sektionen **Brødtekst** skal du i feltet **Etiketsidefod** angiv en ZPL-kode for den påkrævede sidefod. Her er et eksempel.

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > Denne opsætning vil udskrive én kopi af hver etiket. Hvis du har brug for flere kopier (f.eks. én kopi for hver side af pallen), skal du angive værdien **n-** for **\^PQn** i sidefoden til det påkrævede antal kopier. Hvis du f.eks. vil udskrive fire kopier af hver etiket, skal du angive **\^PQ4**.

1. Den anden etiket er nu klar til brug.
1. Opret en tredje layoutpost, der har følgende indstillinger:

    - **Etiketlayout-id:** *Brud*
    - **Beskrivelse:** *Brudetiket*

1. Vælg **Gem** i handlingsruden.
1. Oversigtspanelet **Layout af printertekst** indeholder tre sektioner, hvor du kan skrive printerkode: **Sidehoved**, **Brødtekst** og **Sidefod**. I sektionen **Sidehoved** skal du i feltet **Etiketsidehoved** angiv en ZPL-kode for det påkrævede sidehoved. Her er et eksempel.

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ```

1. Denne gang er brødtekst ikke nødvendig. Du skal derfor blot angive den nødvendige tekst i sektionen **Sidefod**. Her er et eksempel.

    ```plaintext
    ^XZ
    ```

    Den tredje etiket er nu klar til brug.

    > [!NOTE]
    > Denne tredje etiket er en brudetiket, der vil blive brugt som delelinje mellem etiketruller.

### <a name="create-two-wave-label-types"></a>Oprette to bølgeetikettyper

1. Gå til **Lokationsstyring \> Opsætning \> Dokumentruteplanlægning \> Bølgeetikettyper**.
1. Opret en post, der har følgende indstillinger:

    - **Etikettype:** *Karton*
    - **Beskrivelse:** *Karton*

1. Opret en anden post, der har følgende indstillinger:

    - **Etikettype:** *Palle*
    - **Beskrivelse:** *Palle*

### <a name="set-up-unit-sequence-groups"></a>Konfigurer enhedsseriegrupper

1. Gå til **Lokationsstyring \> Opsætning \> Lagersted \> Enhedsseriegrupper**.
1. Vælg eller opret en **Hver boks PL**-gruppe.
1. For linjen **Boks** skal du indstille feltet **Bølgeniveautype** til *Karton*.
1. For linjen **PL** skal du indstille feltet **Bølgeniveautype** til *Palle*.

### <a name="create-wave-label-templates"></a>Oprette bølgeetiketskabeloner

1. Gå til **Lokationsstyring \> Opsætning \> Dokumentruteplanlægning \> Bølgeetiketskabeloner**.
1. Opret en etiketskabelon, der har følgende indstillinger:

    - **Navn på etiketskabelon:** *Kartonetiketter*
    - **Beskrivelse:** *Kartonetiketter*
    - **Kode for bølgetrin:** *Karton*
    - **Lagersted:** *62*

1. I oversigtspanelet **Generelt** skal du i feltet **Bølgeetikettype** vælge en værdi som f.eks. *Karton*.
1. I oversigtspanelet **Detaljer om bølgeetiketskabeloner** skal du tilføje en række, der har følgende indstillinger:

    - **Etiketlayout-id:** *karton*
    - **Printernavn:** Vælg en relevant ZPL-printer.
    - **Kør forespørgsel:** *Ja* (denne indstilling er valgfri, men den anbefales for at opnå den optimale ydeevne).

1. Vælg **Gem** i handlingsruden.
1. Valgfrit: Hvis du konfigurerer et kundespecifikt etiketdesign, skal du oprette en forespørgsel for at finde kundens konto. Gå til oversigtspanelet **Detaljer om bølgeetiketskabeloner**, og vælg **Rediger forespørgsel**. I dialogboksen for forespørgselseditor skal du derefter under fanen **Område** tilføje en række, der har følgende indstillinger:

    - **Tabel:** *Forsendelser*
    - **Afledt tabel:** *Forsendelser*
    - **Felt:** *Kontonummer*
    - **Kriterier:** Angiv det relevante debitorkontonummer.

    Når du er færdig, skal du vælge **OK** for at lukke dialogboksen for forespørgselseditor.

1. I handlingsruden skal du vælge **Rediger forespørgsel** for at at åbne dialogboksen for forespørgselseditoren for hele etiketskabelonen.
1. I dialogboksen for forespørgselseditor skal du under fanen **Sortering** tilføje en række, der har følgende indstillinger:

    - **Tabel:** *Arbejdslinjer*
    - **Afledt tabel:** *Arbejdslinjer*
    - **Felt:** *Referencelastlinje-id (post-id)*
    - **Søgeretning:** *Stigende*

1. Tilføj en anden række, der har følgende indstillinger:

    - **Tabel:** *Arbejdslinjer*
    - **Afledt tabel:** *Arbejdslinjer*
    - **Felt:** *Forsendelses-id*
    - **Søgeretning:** *Stigende*

1. Vælg **OK** for at lukke dialogboksen for forespørgselseditoren.
1. I en meddelelsesboks beder dig om at bekræfte nulstillingen af grupperingsfunktionen. Vælg **Ja** for at fortsætte.
1. Gå til handlingsruden, og vælg **Gruppe af bølgeetiketskabeloner**.
1. Gå til dialogboksen **Gruppe af bølgeetiketskabeloner**, og angiv følgende værdier for hver række i feltet **Referencefeltnavn**, der er angivet til *Forsendelses-id*:

    - **Udskriv brudetiket:** Markér dette afkrydsningsfelt.
    - **Etiketlayout-id:** Vælg en brudetiket. (Du kan f.eks. vælge det etiketlayout for *Brud*, som du har oprettet tidligere i dette scenarie.)
    - **Printernavn:** Vælg printeren til brudetiketten. (Hvis du vil opdele etiketten, skal du son regel vælge den samme printer, som er valgt i oversigtspanelet **Detaljer om bølgetiketskabeloner**. Andre scenarier er dog mulige.)

1. Når det gælder den række, hvor feltet **Referencefeltnavn** er indstillet til *Referencelastlinje-id*, skal du markere afkrydsningsfeltet **Etiket-build-id**.

    > [!NOTE]
    > Denne opsætning opretter en etiketserie ("karton 1 af X") pr. lastlinje i hele bølgen, uanset opsætningen af arbejdsgrupperingen. Denne etiketserie kan udskrives på et etiketlayout. Derudover vil etiketter til forskellige forsendelser blive adskilt af den valgte brudetiket.

1. Vælg **OK** for at lukke dialogboksen **Gruppe af bølgeetiketskabeloner**.
1. Opret en anden etiketskabelon, der har følgende indstillinger:

    - **Navn på etiketskabelon:** *Palleetiketter*
    - **Beskrivelse:** *Palleetiketter*
    - **Kode for bølgetrin:** *Palle*
    - **Lagersted:** *62*

1. I oversigtspanelet **Generelt** skal du i feltet **Bølgeetikettype** vælge en værdi som f.eks. *Palle*.
1. I oversigtspanelet **Detaljer om bølgeetiketskabeloner** skal du tilføje en række, der har følgende indstillinger:

    - **Etiketlayout-id:** *Pakke*
    - **Printernavn:** Vælg en relevant ZPL-printer.
    - **Kør forespørgsel:** *Ja* (denne indstilling er valgfri, men den anbefales for at opnå den optimale ydeevne).

1. Vælg **Gem** i handlingsruden.
1. Valgfrit: Hvis du konfigurerer et kundespecifikt etiketdesign, skal du oprette en forespørgsel for at finde kundens konto. Gå til oversigtspanelet **Detaljer om bølgeetiketskabeloner**, og vælg **Rediger forespørgsel**. I dialogboksen for forespørgselseditor skal du derefter under fanen **Område** tilføje en række, der har følgende indstillinger:

    - **Tabel:** *Forsendelser*
    - **Afledt tabel:** *Forsendelser*
    - **Felt:** *Kontonummer*
    - **Kriterier:** Angiv det relevante debitorkontonummer.

    Når du er færdig, skal du vælge **OK** for at lukke dialogboksen for forespørgselseditor. 

1. I handlingsruden skal du vælge **Rediger forespørgsel** for at at åbne dialogboksen for forespørgselseditoren for hele etiketskabelonen.
1. I dialogboksen for forespørgselseditor skal du under fanen **Sortering** tilføje en række, der har følgende indstillinger:

    - **Tabel:** *Arbejdslinjer*
    - **Afledt tabel:** *Arbejdslinjer*
    - **Felt:** *Referencelastlinje-id (post-id)*
    - **Søgeretning:** *Stigende*

1. Tilføj en anden række, der har følgende indstillinger:

    - **Tabel:** *Arbejdslinjer*
    - **Afledt tabel:** *Arbejdslinjer*
    - **Felt:** *Forsendelses-id*
    - **Søgeretning:** *Stigende*

1. Vælg **OK** for at lukke dialogboksen for forespørgselseditoren.
1. I en meddelelsesboks beder dig om at bekræfte nulstillingen af grupperingsfunktionen. Vælg **Ja** for at fortsætte.
1. Gå til handlingsruden, og vælg **Gruppe af bølgeetiketskabeloner**.
1. Gå til dialogboksen **Gruppe af bølgeetiketskabeloner**, og angiv følgende værdier for hver række i feltet **Referencefeltnavn**, der er angivet til *Forsendelses-id*:

    - **Udskriv brudetiket:** Markér dette afkrydsningsfelt.
    - **Etiketlayout-id:** Vælg en brudetiket. (Du kan f.eks. vælge det etiketlayout for *Brud*, som du har oprettet tidligere i dette scenarie.)
    - **Printernavn:** Vælg printeren til brudetiketten. (Hvis du vil opdele etiketten, skal du son regel vælge den samme printer, som er valgt i oversigtspanelet **Detaljer om bølgetiketskabeloner**. Andre scenarier er dog mulige.)

1. Når det gælder den række, hvor feltet **Referencefeltnavn** er indstillet til *Referencelastlinje-id*, skal du markere afkrydsningsfeltet **Etiket-build-id**.

    > [!NOTE]
    > Denne opsætning opretter en etiketserie ("karton 1 af X") pr. lastlinje i hele bølgen, uanset opsætningen af arbejdsgrupperingen. Denne etiketserie kan udskrives på et etiketlayout. Derudover vil etiketter til forskellige forsendelser blive adskilt af den valgte brudetiket.

### <a name="configure-number-sequence-extensions"></a>Konfigurere nummerserieudvidelser

Nummerserieudvidelser styrer GS1-overholdelse af specifikke nummerserier. Denne konfiguration er valgfri for det aktuelle scenarie. Du kan finde flere oplysninger og konfigurationsinstruktioner under [Konfigurere nummerserieudvidelser](../warehousing/configure-number-sequence-extensions.md).

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Oprette en salgsordre og frigive den til lagerstedet

1. Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.
1. Opret salgsordre, der har følgende indstillinger:

    - **Debitorkonto:** *US-001*
    - **Lagersted:** *62*

1. Tilføj to salgsordrelinjer:

    - Salgsordrelinje 1:

        - **Varenummer:** *A0001*
        - **Antal:** *9024*
        - **Enhed:** *hver* (9024 hver = 376 boks = 47 PL)

    - Salgsordrelinje 2:

        - **Varenummer:** *A0002*
        - **Antal:** *9016*
        - **Enhed:** *hver* (9016 hver = 322 boks = 46 PL)

    > [!NOTE]
    > De varer og antal, der angives her, er kun eksempler. De skal bruge den enhedsseriegruppe, du har defineret tidligere, relevante enhedskonverteringer fra *hver* til *boks* til *PL* skal defineres for dem, og de skal have lager på lagerstedet *62*. Du kan finde flere oplysninger i [Måleenhed og lagerføringspolitikker](unit-measure-stocking-policies.md).

1. Vælg salgsordrelinje 1. I sektionen **Salgsordrelinje** skal du i menuen **Lager** vælge **Reservationer**.
1. På siden **Reservation** skal du i handlingsruden vælge **Reserver parti** og derefter lukke siden.
1. Gentag trin 4 og 5 for salgsordrelinje 2.
1. Vælg **Frigør til lagersted** under fanen **Lagersted** i handlingsruden.

    Følgende hændelser forekommer: 

    - Systemet behandler den oprettede forsendelse ved hjælp af den skabelon, der indeholder trinnet til udskrivning af etiketter. Etiketlayoutet bruges til at definere etikettens format, og resultatet vil være en etiket, der udskrives på den printer, der er valgt i etiketskabelonen.
    - Der genereres og udskrives bølgeetiketter. Antallet af etiketter vil være lig med antallet af kartoner (i dette eksempel 376 boks-etiketter til linje 1, 322 boks-etiketter til linje 2, 47 palle-etiketter til linje 1, 47 palle-etiketter til linje 2 og to brudetiketter, der har forsendelses-id'et).
    - Der genereres et nyt fragtseddel-id for forsendelserne. Hvis du har konfigureret nummerserieudvidelserne, følger bølgeetiket-id'erne **SSCC-18**-nummerformatet. 

Du kan få vist og udskrive bølgeetiketter fra følgende sider:

- Alle forsendelser \> Forsendelsesoplysninger
- Alle laster \> Lastdetaljer
- Alle bølger
- Bølgelabels
- Historik for bølgelabel

På de fleste af disse sider kan du finde den relevante funktion ved at vælge **Bølgeetiketter** i gruppen **Relaterede oplysninger** under fanen **Forsendelser** i handlingsruden.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]