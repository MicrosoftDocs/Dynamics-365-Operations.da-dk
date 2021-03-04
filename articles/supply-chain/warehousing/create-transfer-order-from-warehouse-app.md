---
title: Oprette flytteordrer fra lagerstedsappen
description: Dette emne beskriver, hvordan du opretter og behandler flytteordrer fra funktionen i lagerstedsappen
author: perlynne
manager: tfehr
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileDeviceQueueEvent
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: c30b0e74053480a08f84f4d7579021084ded5799
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424411"
---
# <a name="create-transfer-orders-from-the-warehouse-app"></a>Oprette flytteordrer fra lagerstedsappen

[!include [banner](../includes/banner.md)]

Denne funktion giver lagermedarbejderne mulighed for at oprette og behandle flytteordrer direkte fra lagerstedsappen. Lagermedarbejderne starter med at vælge destinationslagerstedet og kan derefter scanne et eller flere id'er ved hjælp af appen for at tilføje id'er i flytteordren. Når lagermedarbejderen vælger **Fuldfør ordre**, opretter et batchjob den krævede flytteordre og ordrelinjer, der er baseret på den disponible lagerbeholdning, som er registreret for disse id'er.

## <a name="enable-the-create-transfer-orders-from-warehouse-app-feature"></a><a name="enable-create-transfer-order-from-warehouse-app"></a>Aktivere funktionen, der opretter flytteordrer fra lagerstedsappen

Før du kan bruge denne funktion, skal både den og dens forudsætninger være aktiveret i dit system. Administratorer kan bruge siden [funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionsstatus og aktivere den, hvis det er nødvendigt.

1. Aktivér først funktionen [Hændelsesbehandling i lagerstedsapp](warehouse-app-events.md), der er angivet i [funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) som:
    - **Modul** – Lokationsstyring
    - **Funktionsnavn** - Hændelsesbehandling i lagerstedsapp
1. Aktivér derefter funktionen *Opret flytteordrer fra lagerstedsappen*, der er angivet som:
    - **Modul** – Lokationsstyring
    - **Funktionsnavn** - Oprette og behandle flytteordrer fra lagerstedsappen
1. Hvis du vil automatisere behandlingen af de udgående forsendelser, skal du også aktivere funktionen [Bekræft udgående forsendelser fra batchjob](confirm-outbound-shipments-from-batch-jobs.md). Funktionen er angivet som:
    - **Modul** – Lokationsstyring
    - **Funktionsnavn** – Bekræft udgående forsendelser fra batchjob

## <a name="set-up-a-mobile-device-menu-item-to-create-transfer-orders"></a><a name="setup-warehouse-app-menu"></a>Konfigurere et menupunkt for mobilenheden til oprettelse af flytteordrer

Her er generelle retningslinjer for opsætning af et menupunkt i mobilenheder til oprettelse af en flytteordre. Afhængigt af dine forretningsbehov for det automatiseringsniveau, der skal angives, når brugere opretter flytteordrer fra grunden, aktiveres forskellige konfigurationer. Scenariet i dette dokument indeholder en beskrivelse af konfigurationen.

1. Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Menupunkter i mobilenhed**.
1. Vælg **Ny** for at tilføje et nyt menupunkt. Foretag derefter følgende indstillinger for at komme i gang:

    - **Navn på menupunkt** - Tildel et navn, som det skal vises i Supply Chain Management.
    - **Titel** – Tildel et menunavn, som det skal vises for arbejdere i lagerstedsappen.
    - **Tilstand** - Angiv som *Indirekte* (denne lagerstedsapp vil ikke oprette arbejde).
    - **Aktivitetskode** – Angiv til *Opret flytteordre fra id'er* for at gøre det muligt for lagermedarbejderne at oprette en flytteordre ud fra en eller flere scannede nummerplader.

1. Brug indstillingen **Oprettelsespolitik for flytteordrelinje** til at styre, hvordan flytteordrelinjer oprettes af dette menupunkt. Linjerne oprettes/opdateres baseret på den disponible lagerbeholdning, der er registreret for de scannede nummerplader. Vælg en af følgende værdier:

    - **Ingen reservation** - Flytteordrelinjerne vil ikke blive reserveret.
    - **Nummerplade styret med linjereservation** – Flytteforslagslinjerne reserveres og bruger indstillingen for nummerpladestyret strategi, der gemmer de relevante nummerplade-id'er, der er tilknyttet ordrelinjerne. De fundne værdier af nummerplade-id kan derfor bruges som en del af arbejdsprocessen for flytteforslagslinjerne.

1. Brug indstillingen **Udgående forsendelsespolitik** til at føje mere automatisering til forsendelsesprocessen for udgående flytteordrer efter behov. Når en arbejder vælger knappen **Fuldfør ordre**, opretter appen den *Fuldfør ordre*-hændelse i lagerstedsappen, der gemmer den værdi, du vælger her, i feltet **Udgående forsendelsespolitik** for alle linjer i den aktuelle flytteordre. Senere, når hændelseskøen behandles af et batchjob for at oprette flytteordren, kan den værdi, der er gemt i dette felt, aflæses af batchjobbet og kan derfor kontrollere, hvordan jobbet behandler hver enkelt linje. Vælg en af følgende muligheder:

    - **Ingen** - Der foretages ingen automatisk behandling.
    - **Frigiv til lagersted** - Automatiserer frigivelsen til lagerstedsprocessen.
    - **Bekræft afsendelse** - Automatiserer bekræftelsesprocessen for afsendelsen.
    - **Frigiv og bekræft afsendelse** – Automatiserer både frigivelsen til lagerstedet og bekræftelsen af afsendelsen.

## <a name="add-the-mobile-device-menu-item-to-a-menu"></a>Føje menupunktet til en mobilenhedsmenu

1. Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Mobilenhedsmenu**
1. Vælg **Rediger**.
1. Vælg en eksisterende menu efter valget af det nye menupunkt under **Tilgængelige menuer og menupunkter**. Tilføj menupunktet ved at vælge knappen højre pil.

## <a name="create-a-transfer-order-based-on-license-plates"></a>Oprette en flytteordre på basis af nummerplader

Lagerstedsappen har en simpel proces til oprettelse af flytteordrer baseret på nummerplader. For at kunne gøre dette gør arbejderen følgende ved at bruge lagerstedsappen:

1. Opretter flytteordren og identificerer destinationslagerstedet.
1. Identificerer de enkelte nummerplader, der skal afsendes.
1. Vælg **Fuldfør ordre**.

>[!NOTE]
> Det er muligt for flere arbejdere at tildele nummerplader, der er beregnet til den samme flytteordre, ved at bruge knappen **Vælg flytteordre** til at vælge et eksisterende, ikke-behandlet, flytteordrenummer fra hændelseskøen i lagerstedsappen. Du kan finde oplysninger om, hvordan du finder nummerværdier i flytteordrer, under [Forespørge på lagerstedappens hændelser](#inquire-the-warehouse-app-events).

## <a name="example-scenario"></a>Eksempelscenario

Dette scenario giver en oversigt over processen for at få flytteordrer oprettet og behandlet automatisk på basis af den disponible lagerbeholdning, der er registreret på de valgte nummerplader.

Hvis du vil arbejde gennem dette scenarie ved hjælp af de foreslåede værdier, skal du arbejde på et system, hvor demonstrationsdata er installeret, og vælge den juridiske enhed *USMF*, før du går i gang.

I dette scenarie antages det, at du allerede har aktiveret både funktionen [Oprette og behandle flytteordrer fra lagersteds](#enable-create-transfer-order-from-warehouse-app) og funktionen [behandling af hændelser på lagerstedet](warehouse-app-events.md).

Ud over at definere oprettelse af en flytteordre i menupunkter på mobilenheden skal der også konfigureres og aktiveres flere skabeloner, lokationsvejledninger og batchjob.

### <a name="example-scenario-blueprint"></a>Eksempelscenarie for kursusplan

Du er en detailhandler og har flere nummerplader, der hver indeholder en blanding af varer, der er placeret på en bestemt lokation på et af lagerstederne (*Lagersted 51*). Du vil aktivere den proces, der giver arbejdere mulighed for at oprette en flytteordre til et andet lagersted (*Lagersted 61*) for en samling af scannede nummerplader. Du sender automatisk en opdatering af flytteordren, så snart den sidste nummerplade for ordren er identificeret.

![Eksempel på automatisk proces til flytteordre](media/create-transfer-order-from-app-example.png "Eksempel på automatisk proces til flytteordre")

### <a name="create-a-mobile-device-menu-item-for-creating-transfer-orders"></a>Oprette et menupunkt for mobilenheden til oprettelse af flytteordrer

Dette afsnit forklarer, hvordan du opretter et nyt menupunkt på mobilenheder til oprettelse af flytteordrer. Angiv **Tilstand** til *Indirekte* og **Aktivitetskode** til *Opret flytteordre fra nummerplader*.

1. Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Menupunkter i mobilenhed**.
1. Vælg **Ny**.
1. Indtast navnet **Opret flytteordre** i feltet *Navn på menupunkt*.
1. Indtast beskrivelsen af **Opret flytteordre** i feltet *Titel*.
1. Vælg **Indirekte** i feltet *Tilstand*.
1. Vælg *Opret flytteordre fra nummerplader* i **Aktivitetskode**.
1. I **Politik til oprettelse af ordrelinje** skal du vælge *Nummerpladestyret med linjereservation*.
1. Vælg **Frigiv og bekræft afsendelse** i *Udgående afsendelsespolitik*.
1. Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Mobilenhedsmenu**.
1. Vælg **Rediger**.
1. Vælg den eksisterende **Lager**-menu og derefter det nye menupunkt under **Tilgængelige menuer og menupunkter**. Tilføj menupunktet i menuen **Lager** ved at vælge knappen højre pil.

### <a name="set-up-work-templates-to-auto-process-and-break-work-by-located-license-plate"></a>Konfigurere arbejdsskabeloner til automatisk proces og arbejdspause efter fundet nummerplade

I dette afsnit forklares, hvordan du kan aktivere en arbejdsskabelon for automatisk at behandle det arbejde, der oprettes af skabelonen, når der frigives en bølge.

1. Gå til **Lagerstedsstyring \> Opsætning \> Arbejde \> Arbejdsskabeloner**.
1. I feltet **Arbejdsordretype** skal du vælge *Flytteafgang*.
1. Vælg **Ny** for at oprette en ny arbejdsskabelon.
1. Angiv **51 automatisk behandling af nummerplade** i feltet *Arbejdsskabelon*.
1. Angiv **51 automatisk behandling af nummerplade** i feltet *Beskrivelse af arbejdsskabelon*.
1. Markér afkrydsningsfeltet **Udfør automatisk behandling**. Dette skal vælges, før der kan behandles nogen automatiseringstrin.
1. I demonstrationsdataene findes der allerede en arbejdsskabelon *51 Flyt*, hvor du skal redigere feltet **Sekvensnummer**, så den nye arbejdsskabelon har et lavere sekvensnummer end den eksisterende arbejdsskabelons *51 Flyt*.
1. Vælg **Gem** på værktøjslinjen for at aktivere oversigtspanelet **Arbejdsskabelondetaljer**.
1. Vælg **Ny** på værktøjslinjen i oversigtspanelet **Arbejdsskabelondetaljer**. Du skal tilføje to linjer.
1. Vælg **Pluk** i feltet *Arbejdstype*.
1. Vælg *TransfOut* i feltet **Arbejdsklasse-id**.
1. Vælg **Ny** på værktøjslinjen **Arbejdsskabelondetaljer**.
1. Vælg **Læg på lager** i feltet *Arbejdstype*.
1. Vælg *TransfOut* i feltet **Arbejdsklasse-id**.
1. Vælg **Gem** for at aktivere feltet **Vejledningskode**.
1. Vælg **Vejledningskode** *Baydoor* på linjen **Læg på lager** for *Arbejdstype*. Sørg for, at denne nye arbejdsskabelon får det laveste **Sekvensnummer**.
1. Vælg **Rediger forespørgsel** på værktøjslinjen for at åbne forespørgselseditoren.
1. Vælg **Tilføj** under fanen **Interval**.
1. I **Felt** på linjen, der er tilføjet, skal du vælge *Lagersted*.
1. Vælg **51** i feltet *Kriterier*.
1. Vælg fanen **Sortering**.
1. Vælg **Tilføj**, og angiv **Felt** til *Fundet nummerplade-id*. Når du markerer dette felt, aktiveres værktøjslinjeknappen **Opgaveoverskriften skifter**.
1. Vælg **OK** efterfulgt af **Ja** for at nulstille grupperingen og vende tilbage til siden **Arbejdsskabeloner**.
1. Vælg **Opgaveoverskriften skifter**, og aktivér **Gruppér efter dette felt** for dette **Fundne nummerplade-id**, og luk ruden.

> [!NOTE]
> Det er ikke alle opsætninger, der kan behandles automatisk, f.eks. fastvægtvarer og brugen af blandede sporingsdimensioner.

### <a name="set-up-location-directives-for-the-license-plate-guided-strategy"></a>Konfigurere lokationsvejledninger for en nummerpladestyret strategi

I dette afsnit forklares, hvordan du konfigurerer en plukkeproces for en lokationsvejledning til at bruge **Nummerpladestyret** strategi.

1. Gå til **Lokationsstyring \> Opsætning \> Lokationsvejledninger**.
1. Vælg **Rediger**.
1. Vælg **Arbejdsordretype** *Flytteafgang* i overskriften på navigationslisten.
1. Vælg den eksisterende lokationsvejledning **51 pluk flytteordre** på navigationslisten.
1. I oversigtspanelet **Linjer** skal du markere afkrydsningsfeltet **Tillad opdeling**.
1. I oversigtspanelet **Handlinger i lokationsvejledning** skal du vælge **Ny** for at tilføje en ny handlingslinje.
1. I feltet **Navn** skal du angive *Nummerpladestyret*.
1. Vælg **Nummerpladestyret** i feltet *Strategi*. Denne handling skal bruge det laveste sekvensnummer.
1. Vælg **Gem** på værktøjslinjen.
1. Vælg sideikonet **Opdater** på værktøjslinjen.
1. I oversigtspanelet **Handlinger i lokationsvejledning** skal du vælge linjen *TOPick*.
1. Vælg **Flyt ned** på værktøjslinjen **Handlinger i lokationsvejledninger** for at ændre sekvensnummeret, så det er større end sekvensnummeret for den *Nummerpladestyret*, der lige er oprettet.

> [!NOTE]
> Den nummerpladestyrede strategi vil forsøge at reservere og oprette plukarbejde på de lokationer, hvor de anmodede nummerplader er knyttet til flytteordrelinjerne. Men hvis dette ikke er muligt, og du stadig gerne vil oprette plukarbejde, skal du gå tilbage til en anden handlingsstrategi for lokationsdirektiv og måske også søge efter en lagerplads i et andet område på lagerstedet, afhængigt af forretningsprocessens behov.

### <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a>Konfigurere et batchjob, der skal behandle hændelser i lagerstedsapp

I dette afsnit forklares, hvordan du kan konfigurere et planlagt batchjob til at behandle lagerstedsappens hændelser.

1. Gå til **Lokationsstyring \> Periodiske opgaver \> Hændelsesbehandling i lagerstedsapp**.
2. Aktivér **Batchbehandling** under **Kør i baggrunden** i dialogboksen.
3. Vælg **Gentagelse**, og konfigurer batchjobbet til at behandle på basis af det interval, der er nødvendigt for din virksomhed.
4. Vælg **OK** for at vende tilbage til hoveddialogboksen.
5. Vælg **OK** i hoveddialogboksen for at føje jobbet til batchkøen.

### <a name="set-up-a-batch-job-to-release-transfer-orders-automatically"></a>Konfigurere et batchjob til automatisk frigivelse af flytteordrer

I dette afsnit forklares, hvordan du kan konfigurere et planlagt batchjob for at frigive de flytteordrer, der er markeret som "klar til frigivelse".

1. Gå til **Lagerstedsstyring \> Frigiv til lagersted \> Automatisk frigivelse af flytteordrer**.
1. Udvid sektionen **Poster, der skal medtages** i dialogboksen.
1. Vælg **Filter** i sektionen **Poster, der skal indgå**.
1. Vælg **Tilføj** under fanen **Område** på forespørgselssiden **WHSTransferAutoRTWQuery** for at føje en ny linje til forespørgslen.
1. I feltet **Tabel** skal du vælge rullemenuen og vælge tabellen **Frigiv flyttelinje til lagersted**.
1. Vælg **Udgående forsendelsespolitik** i rullemenuen i **Felt**.
1. Vælg **Frigiv og bekræft afsendelse** i feltet **Kriterier**.
1. På linjen, hvor **Felt** er angivet til *Fra lagersted*, skal du i feltet **Kriterier** vælge *51*.
1. Vælg **OK** for at vende tilbage til hoveddialogboksen.
1. Udvid sektionen **Kør i baggrunden** for at konfigurere batchbehandling.
1. Aktivér **Batchbehandling** i sektionen **Kør i baggrunden**.
1. Vælg **Gentagelse**, og konfigurer batchjobbet til at behandle på basis af det interval, der er nødvendigt for din virksomhed.
1. Vælg **OK** for at vende tilbage til hoveddialogboksen.
1. Vælg **OK** i hoveddialogboksen for at føje batchjobbet til batchkøen.

### <a name="set-up-the-process-outbound-shipment-batch-job"></a>Konfigurere batchjobbet "Udfør behandling af udgående forsendelser"

Dette afsnit forklarer, hvordan du konfigurerer et planlagt batchjob til at køre bekræftelse af udgående forsendelse for laster, der er klar til afsendelse i forbindelse med flytteordrelinjer, der er "klar til afsendelse".

1. Gå til **Lokationsstyring \> Periodiske opgaver \> Behandle udgående forsendelser**.
1. Udvid sektionen **Poster, der skal indgå**.
1. Vælg **Filter**.
1. Vælg fanen **Joinforbindelser** i forespørgslen **WHSLoadShipConfirm**.
1. Udvid tabelhierarkiet, så **Laster** og **Lastdetaljer** er blevet udvidet.
1. Vælg tabelen **Lastdetaljer**.
1. Vælg knappen **Tilføj tabeljoin**.
1. På listen over tabelrelationer skal du filtrere eller søge efter kolonnen **Relation** for *Flytteordrelinjer (reference)*.
1. Fokusér på tabelrelationen på listen, og tryk derefter på knappen **Vælg**.
1. Vælg tabellen **Flytteordrelinjer**.
1. Vælg knappen **Tilføj tabeljoin**.
1. På listen over tabelrelationer skal du filtrere eller søge efter kolonnen **Relation** for *Flere felter i lageroverførsel (post-id)*.
1. Fokusér på tabelrelationen på listen, og tryk derefter på knappen **Vælg**.
1. Vælg fanen **Område**.
1. I forespørgselstabellerne **Område** skal du konfigurere tre forespørgselskriterieområder. Vælg knappen **Tilføj** for at tilføje en linje.
1. Tilføj et område for tabellen **Laster**. Indstil **Felt** til *Laststatus*, og angiv **Kriterier** til *Lastet*.
1. Tilføj et nyt område i tabellen **Flere felter i lageroverførsel**. Angiv **Felt** til *Udgående forsendelsespolitik*, og Angiv **Kriterier** til *Frigiv og bekræft afsendelse*.
1. Tilføj endnu et område for tabellen **Lastdetaljer**. Angiv **Felt** til *Reference* og **Kriterier** til *Forsendelse af flytteordre*.
1. Vælg **OK** for at vende tilbage til hoveddialogboksen.
1. Udvid sektionen **Kør i baggrunden**.
1. Aktivér **Batchbehandling**.
1. Vælg **Gentagelse**, og konfigurer batchjobbet til at behandle på basis af det interval, der er nødvendigt for din virksomhed.
1. Vælg **OK** for at vende tilbage til hoveddialogboksen.
1. Vælg **OK** i hoveddialogboksen for at føje batchjobbet til batchkøen.

> [!NOTE]
> Du kan finde flere oplysninger under [Bekræfte udgående forsendelser fra batchjob](confirm-outbound-shipments-from-batch-jobs.md).

## <a name="processing-the-example-for-create-transfer-order-from-the-warehouse-app"></a>Behandle eksemplet for "Oprette en flytteordre fra lagerstedsappen"

### <a name="add-on-hand-on-a-license-plate"></a>Tilføje beholdning på en nummerplade

Som udgangspunkt for dette scenario skal du have en nummerplade, der indeholder fysisk tilgængelig disponibel lagerbeholdning.

| Post | Lagersted | Lagerstatus | Adresse | Nummerplade | Kvantitet |
| --- | --- | --- | --- | --- | --- |
| A0001 | 51 | Ledig | LP-010 | LP10 | 1 |
| A0002 | 51 | Ledig | LP-010 | LP10 | 2 |

Tilføj antal af fysisk disponibel lagerbeholdning ved hjælp af følgende værdier:

> [!NOTE]
> Du skal oprette nummerpladen og bruge lokationer, der giver dig mulighed for at overføre blandede varer som f.eks. LP-010.

### <a name="create-and-process-transfer-orders-from-the-warehouse-app"></a>Opret, og behandl overførselsordrer fra lagersteds-appen

1. Åbn appen, og log på som bruger *51*. Det aktuelle brugerlagersted vil være 51.
1. Vælg menupunktet **Opret flytteordre** ud fra den menuplacering, du har tilføjet under konfigurationen.
1. Starte oprettelsen af en flytteordre ved at angive destinationslagerstedet (Til lagersted) i feltet **Lagersted** som *61*. Den nye flytteordre går fra det aktuelle lagersted 51 (Fra lagersted) til destinationslagerstedet *61*.
1. Vælg **OK**.
1. Scan et nummerplade-id i feltet **Nummerplade**. Angiv nummerpladen for det lager, der er tilføjet i et tidligere trin, *LP10*.
1. Vælg **OK**.
1. Vælg menuknappen, og vælg derefter **Fuldfør ordre** for at afslutte oprettelsen af flytteordren i lagerstedsappen.

For det nævnte eksempel bruges to **Hændelser i lagerstedsapp** (*Opret flytteordre* og *Fuldfør flytteordre*).

### <a name="inquire-the-warehouse-app-events"></a><a name="#inquire-the-warehouse-app-events"></a>Forespørge på lagerstedsappens hændelser

Du kan få vist hændelseskøen og de hændelsesmeddelelser, der er genereret af lagerstedsappen, ved at gå til **Lokationsstyring \> Forespørgsler og rapporter \> Mobilenhedslogge \> Hændelser i lagerstedsapp**.

Hændelses meddelelserne *Opret flytteordre* får statussen *Venter*, hvilket betyder, at batchjobbet **Hændelsesbehandling i lagerstedsapp** ikke vil registrere og behandle hændelsesmeddelelserne. Så snart hændelsesmeddelelsen opdateres til statussen *Sat i kø*, behandler batchjobbet hændelserne. Dette vil ske samtidig med oprettelsen af hændelsen *Fuldfør flytteordre* (når en arbejder vælger knappen **Fuldfør ordre** i lagerstedsappen). Når hændelsesmeddelelserne *Opret flytteordre* er blevet behandlet, opdateres statussen til *Fuldført* eller *Mislykket*. Når statussen *Fuldfør flytteordre* opdateres til *Fuldført*, slettes alle relaterede hændelser fra køen.

Da **Hændelser i lagerstedsapp** for oprettelse af flytteordredata ikke vil blive behandlet af batchjobbet, før meddelelsen er opdateret til status *Sat i kø*, skal du slå de ønskede flytteordrenumre op som en del af feltet **Identifikator**. Feltet **Identifikator** findes i overskriften på siden **Hændelser i lagerstedsapp**.

Som led i behandlingen af lagerstedshændelsen kan oprettelsen af flytteordrelinjen mislykkes. I dette tilfælde opdateres tilstanden for hændelsesmeddelelsen til *Mislykket*, og du kan bruge oplysningerne i **Batchlogfilen** til at få mere at vide om hvorfor og handle for at løse eventuelle problemer.

Typiske problemer kan relateres til manglende opsætning for processen, f.eks. et manglende transitlagersted for hændelsen *Opret flytteordre*. I et eksempel som dette skal du føje et transitlagersted til forsendelseslagerstedet og bruge indstillingen **Nulstil** til at ændre status for alle lagerstedsappens hændelsesmeddelelser fra *Mislykket* til *Sat i kø*, hvilket betyder, at batchjobbet behandler hændelsesmeddelelserne igen, når konfigurationsdataene er blevet rettet.

I produktionsmiljøer vil undtagelserne være mere procesrelaterede, f.eks. en anmodet nummerplade, som på behandlingstidspunktet for batchjobbet er tom, og der oprettes derfor ingen flytteordrelinjer. Denne fejlbehæftede hændelsesmeddelelse kan enten fjernes ved hjælp af indstillingen **Slet**, eller du kan tilføje den nødvendige fysiske lagerbeholdning på nummerpladen og bruge indstillingen **Nulstil** for alle relaterede hændelsesmeddelelser.

Du kan finde flere oplysninger under [Hændelsesbehandling i lagerstedsapp](warehouse-app-events.md).

### <a name="follow-up-on-the-example-scenario-processing"></a>Følge op på behandlingen af eksempelscenariet

I dette scenario skete følgende:

1. Ved hjælp af lagerstedsappen har du valgt et menupunkt, der bruger aktivitetskoden **Opret flytteordre fra nummerplader**.
1. Appen bad dig om at vælge destinationslagerstedet for flytteordren. Kildelagerstedet er altid det, du aktuelt er logget på som arbejder.
1. I forbindelse med valget af destinationslagerstedet har systemet reserveret et id-nummer for den kommende flytteordre (baseret på den flytteordrenummerserie, der er defineret på systemet), men har ikke oprettet flytteordren endnu.
1. Da du scannede nummerpladen *LP10*, der indeholder disponibel lagerbeholdning, som skulle flyttes til det nye lagersted, blev der føjet en **Hændelse i lagerstedsapp** til køen med hændelser, der skal behandles senere. Lagerstedshændelsen indeholdt meddelelsesoplysninger om scanningen, herunder det tiltænkte flytteordrenummer.
1. Når knappen **Fuldfør ordre** er valgt på lagerstedsappen, oprettes der en ny hændelse i lagerstedsappen, **Fuldfør flytteordre**, og den relaterede eksisterende hændelse, **Opret flytteordre**, ændrede status til **Sat i kø**.
1. På backend hentede **batchjobbet Hændelsesbehandling i lagerstedsapp** hændelsen **Sat i kø** og indsamlede den disponible lagerbeholdning, der er relateret til den scannede nummerplade. På baggrund af den disponible lagerbeholdning blev den faktiske flytteordrepost og de tilknyttede linjer oprettet. Jobbet udfyldte også feltet **Udgående forsendelsespolitik** for flytteordren med den værdi, der er baseret på den konfigurerede *Frigiv og bekræft afsendelse* og sammenkædede nummerpladen med linjerne til strategien **Nummerpladestyret**.
1. Baseret på feltværdien **Udgående forsendelsespolitik** for flytteordrelinjen resulterede forespørgslen **Automatisk frigivelse af batchjob for flytteordre** nu i, at flytteordren blev frigivet til afsendelseslagerstedet. Og på grund af opsætningen af de anvendte **Bølgeskabelon**, **Arbejdsskabelon** og **Lokationsvejledninger** fik arbejdet automatiske processer, der fik **Laststatus** opdateret til *Lastet*.
1. **Batchjobbet Udfør behandling af udgående forsendelser** blev udført for lasten, så flytteordren blev afsendt, og der blev genereret en ASN-meddelelse (Advance Shipment Notice).
1. Tidspunktet for alle disse hændelser afhænger af **Gentagelse**-indstillingerne for de oprettede batchjob.

## <a name="frequently-asked-questions"></a>Ofte stillede spørgsmål

### <a name="mobile-device-menu-item-setup"></a>Opsætning af et mobilenhedsmenupunkt

#### <a name="why-cant-i-see-create-transfer-order-from-license-plate-in-the-menu-item-work-activity-drop-down-list"></a>Hvorfor kan jeg ikke se "Opret flytteordre fra nummerplade" på rullelisten til menupunktet for arbejdsaktivitet?

Funktionen *Oprette og behandle flytteordrer fra lagerstedsappen* skal være aktiveret. Du kan finde flere oplysninger under [Aktivere funktionen, der opretter flytteordrer fra lagerstedsappen](#enable-create-transfer-order-from-warehouse-app).

### <a name="warehouse-app-processes"></a>Lagerstedsappens processer

#### <a name="why-cant-i-see-the-menu-button-complete-order"></a>Hvorfor kan jeg ikke se menuknappen "Fuldfør ordre"?

Der skal være tildelt mindst én nummerplade til flytteordren.

#### <a name="can-several-warehouse-app-users-add-license-plates-to-the-same-transfer-order-at-the-same-time"></a>Kan flere lagerstedsapp-brugere føje nummerplader til samme flytteordre på samme tid?

Ja, flere lagermedarbejdere kan scanne nummerplader i samme flytteordre.

#### <a name="can-the-same-license-plate-be-added-to-different-transfer-orders"></a>Kan den samme nummerplade føjes til forskellige flytteordrer?

Nej, en nummerplade kan kun føjes til én flytteordre på det pågældende tidspunkt.

#### <a name="after-having-selected-the-complete-order-button-can-i-then-add-more-license-plates-for-that-transfer-order"></a>Når jeg har valgt knappen "Fuldfør ordre", kan jeg så tilføje flere nummerplader for den pågældende flytteordre?

Nej, du kan ikke føje flere nummerplader til en flytteordre, der har en **Fuldfør flytteordre** som hændelse i lagerstedsappen.

#### <a name="how-can-i-find-existing-transfer-orders-to-be-used-via-the-select-transfer-order-button-in-the-warehouse-app-if-the-order-has-not-yet-been-created-in-the-backend-system"></a>Hvordan kan jeg finde eksisterende flytteordrer, der skal bruges via knappen "Vælg flytteordre" i lagerstedsappen, hvis ordren endnu ikke er oprettet i backend-systemet?

I øjeblikket kan du ikke slå flytteordrer op i appen, men du kan finde flytteordrenumrene på siden **Hændelser for lagerstedsapp**. Du kan finde flere oplysninger under [Forespørge på lagerstedsappens hændelser](#inquire-the-warehouse-app-events).

#### <a name="can-i-manually-select-the-transfer-order-number-to-be-used-from-the-warehouse-app"></a>Kan jeg manuelt vælge det flytteordrenummer, der skal bruges, fra lagerstedsappen?

Kun automatisk genererede flytteordrenumre via nummerserier understøttes.

### <a name="background-processing"></a>Baggrundsbehandling

#### <a name="how-should-i-clean-up-records-in-my-warehouse-app-events-queue-message-tables"></a>Hvordan skal jeg rydde op i poster i mine kømeddelelsestabeller i hændelser på lagerstedsappen?

Du kan se og vedligeholde dette på siden **Hændelser i lagerstedsapp**. Du kan finde flere oplysninger under [Forespørge på lagerstedsappens hændelser](#inquire-the-warehouse-app-events).

#### <a name="why-is-the-transfer-order-receipt-date-not-updated-according-to-my-delivery-date-control-setup"></a>Hvorfor bliver flytteordrens "Modtagelsesdato" ikke opdateret ifølge min konfiguration af "Leveringsdatokontrol"?

Flytteordrerne oprettes uden brug af funktionerne i **Leveringsdatokontrol**.

#### <a name="can-i-use-a-license-plate-having-physical-negative-inventory-on-hand"></a>Kan jeg bruge en nummerplade med fysisk negativ lagerbeholdning?

Funktionen understøtter kun positive fysiske lagerbeholdninger. Sørg for, at der er positive fysiske lagerbeholdninger på lagersteds- og lagerstatusniveau, før du tildeler nummerplader til en flytteordre.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]