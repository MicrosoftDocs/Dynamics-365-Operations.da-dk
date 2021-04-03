---
title: Grænseflade for materialehåndteringsudstyr (MHAX)
description: I dette emne beskrives, hvordan du kan konfigurere MHAX-grænsefladen til materialehåndtering, så du kan oprette forbindelse til eksterne MH-systemer for fysisk materialehåndtering.
author: Mirzaab
manager: tfehr
ms.date: 03/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMHEParameters, WMHESubscription, WMHEQueueManagerWorkspace, WMHEInboundQueue, WMHEOutboundQueue
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-04
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: ea021529d7417fb3170c859c7fffcb2cfd23a43f
ms.sourcegitcommit: d7c18228256daeefbf6518c3ef82fed4f7dbc161
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5571836"
---
# <a name="material-handling-equipment-interface-mhax"></a>Grænseflade for materialehåndteringsudstyr (MHAX)

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Du kan bruge *grænsefladen til materialehåndtering* (MHAX) til at knytte eksterne MH-systemer for fysisk materialehåndtering til et lagersted, der administreres af den avancerede lokationsstyring (WMS) i Microsoft Dynamics 365 Supply Chain Management. Grænsefladen mellem WMS- og MH-systemerne består af to køer: en til udgående hændelser (WMS til MH) og en til indgående hændelser (MH til WMS). WMS-systemet genererer udgående hændelser baseret på arbejdslinjer, der er oprettet under forskellige arbejdsoprettelses- og udførelsesprocesser. MH-systemet poller derefter jævnligt WMS-systemet for nye hændelser og behandler svarene. Når MH-systemet er færdig med at håndtere hændelserne i overensstemmelse med arbejdsinstruktioner, sender det indgående hændelser som f.eks. færdiggørelse af en arbejdslinje og kort pluk.

I følgende illustration vises de forskellige elementer og den rækkefølge, de forekommer i, når du bruger MHAX-integration.

![MHAX-komponenter og -interaktioner](media/mhax-components.png "MHAX-komponenter og -interaktioner")

Her er en forklaring på interaktionerne, der vises i foregående illustration:

1. Under oprettelse af arbejde eller arbejdsudførelse oprettes der udgående hændelser i den udgående kø.
2. MH-udstyret opretter forbindelse til MH-udstyrstjenesten, søger efter eventuelle nye hændelser, der er relevante for den, og behandler disse hændelser.
3. Når MH-udstyret er klar til at rapportere tilbage, opretter det forbindelse til tjenesten igen og sender indgående hændelser. Disse hændelser behandles med det samme af køprocessoren.
4. På baggrund af de indgående hændelsesdata kan køprocessoren køre eksisterende arbejde, redigere det eller oprette nyt arbejde.

## <a name="turn-on-the-mhax-feature"></a>Slå MHAX-funktionen til

Før du kan bruge MHAX-funktionen, skal du aktivere både funktionen og dens konfigurationsnøgle.

1. Gå til **Systemadministration \> Arbejdsområder \> Funktionsstyring**.
2. I arbejdsområdet **[Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** skal du aktivere den funktion, der hedder *Grænseflade for materialehåndteringsudstyr*.
3. Sæt systemet i vedligeholdelsestilstand som beskrevet under [Vedligeholdelsestilstand](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
4. Gå til **Systemadministration \> Opsætning \> Licenskonfiguration**.
5. Udvid **Handel \> Lagersteds- og transportstyring**, og markér derefter afkrydsningsfeltet **Grænseflade for materialehåndteringsudstyr**.
6. Slå vedligeholdelsestilstand fra som beskrevet under [Vedligeholdelsestilstand](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).

## <a name="set-mhax-parameters"></a>Angive MHAX-parametre

Du skal angive nogle få generelle parametre på siden **Parametre til grænseflade for materialehåndteringsudstyr** for at konfigurere funktionen.

1. Gå til **Grænseflade for materialehåndteringsudstyr \> Konfiguration \> Parametre til grænseflade for materialehåndteringsudstyr**.
2. Under fanen **Generelt** skal du angive følgende felter:

    - **Bruger-id** – Vælg en arbejder. Denne arbejder bruges til at køre alle de arbejdsoperationer (pluk og læg), der behandles via den indgående kø.
    - **Aktivér id for indgående meddelelse** – Når denne indstilling er angivet til *Ja*, vil meddelelsen blive afvist, hvis der modtages et dublet-id til indgående meddelelse, og der vises en fejlmeddelelse om, at meddelelsen allerede findes. Når denne indstilling er angivet til *Nej*, tillades dubletter af indgående meddelelses-id'er.

3. Under fanen **Nummerserier** skal du vælge de nummerserier, der skal bruges til at generere entydige id'er til indgående køelementer, udgående køelementer og arbejdslinjepar.

## <a name="outbound-events"></a>Udgående hændelser

På specifikke punkter under oprettelse af arbejde eller arbejdsudførelse bestemmer systemet, om det skal generere udgående hændelser, der skal sendes til MH-systemet. Hvis et abonnement er konfigureret til et bestemt punkt under behandlingen af lagerstedet, genererer systemet hændelsen i overensstemmelse med abonnementsopsætningen.

### <a name="structure-of-outbound-events"></a>Struktur for udgående hændelser

Hver udgående hændelse er entydigt identificeret af et id for en udgående kø. Den udgående transaktionstype bestemmer hændelsens type. Lagerstedet og id'et for det abonnement, der genererede hændelsen, registreres også i hændelsen.

For at føre data til MH-systemet indeholder den udgående hændelse 10 datafelter (**data01** til og med **data10**). Disse datafelter har en en til en-tilknytning (1:1) til eksisterende databasefelter. De udtrækkes specifikt fra felter i arbejdslinjen og arbejdshovedtabellerne. Der kan frit vælges felter. Du konfigurerer dem, når du opretter abonnementet.

Udover de 10 datafelter, der har en 1:1-tilknytning til eksisterende databasefelter, kan hændelsen indeholde et ekstra datafelt, der kaldes *nyttedata*. Indholdet af dette felt genereres af brugerdefineret X++-kode, der kaldes en *nyttedatagenerator*. Der konfigureres en nyttedatagenerator, der skal bruges, i abonnementet.

For at sikre, at MH-systemet kun modtager hvert udgående kø-id én gang, bruges et statusfelt til at angive, om en hændelse er klar til at blive sendt til det eksterne system, eller om den allerede er sendt.

### <a name="outbound-queue-subscriptions"></a>Udgående køabonnementer

Før der genereres hændelser, skal der være konfigureret et abonnement, som fortæller MHAX-funktionen, om og hvordan hændelserne skal genereres. Genererede hændelser mærkes af abonnements-id'et. Derfor kan flere MH-systemer oprette forbindelse til det samme WMS-system, men holde deres hændelser adskilt. Når MHAX-tjenesten polles for nye hændelser, er et abonnement en af de tilgængelige indstillinger for hentning af hændelserne.

Du kan oprette et abonnement ved at gå til **Grænseflade for materialehåndteringsudstyr \> Konfiguration \> Abonnementer**. For hvert abonnement er der følgende tilgængelige parametre:

- **Abonnements-id** – et entydigt navn, der identificerer abonnementet.
- **Beskrivelse** – En fritekstbeskrivelse af abonnementet.
- **Lagersted** – De specifikke lagersteder, som hændelser skal filtreres efter.
- **Udgående transaktionstype** – Den type hændelser, som abonnementet skal indeholde.
- **Nyttedatagenerator** – En valgfri kodeudvidelse, der kan angive yderligere oplysninger i feltet **Nyttedata** i den udgående hændelse.

Der kan knyttes en forespørgsel til de enkelte abonnementer. Denne forespørgsel filtrerer arbejdslinjer og overskrifter for yderligere at begrænse det arbejde, der skal bruge abonnementet til at generere hændelser. Hvis du vil føje en forespørgsel til et abonnement, skal du markere afkrydsningsfeltet **Kør forespørgsel** for det relevante abonnement på siden **Abonnementer** og derefter vælge **Rediger forespørgsel** i handlingsruden. Forespørgselseditoren til Supply Chain Management vises som standard.

Abonnementet indeholder desuden en *abonnementstilknytning*, som knytter felter fra enten arbejdshovedet eller arbejdslinjen til nogle af eller alle de ti gratis datafelter i den udgående hændelse efter behov. Hvis du vil returnere oplysninger til MHAX-tjenesten, skal du normalt medtage arbejdslinjepost-id'et eller *id'et for arbejdslinjens par*. (Arbejdslinjepar-id'et er en ny egenskab, der giver systemet mulighed for at bruge en enkelt returkommando til behandling af pluk- og læg-linjer). De resterende felter afhænger af brugstilfældet. Der findes nogle eksempler senere i dette emne.

Hvis du vil oprette en abonnementstilknytning, skal du vælge det relevante abonnement på siden **Abonnementer** og derefter vælge **Abonnementstilknytning** i handlingsruden. I dialogboksen **Abonnementstilknytning**, der vises, kan du tildele en tabel og et felt til hvert tilgængelige datafelt efter behov.

### <a name="outbound-event-types"></a>Udgående hændelsestyper

I dette afsnit beskrives de forskellige hændelsestyper, der er tilgængelige. (Hændelsestyper kaldes også *transaktionstyper*). Det forklarer også, hvornår hver hændelsestype oprettes i WMS-systemet.

#### <a name="work-creation-events"></a>Hændelser til oprettelse af arbejde

Hændelser til oprettelse af arbejde oprettes, efter at arbejdet er genereret af programmet. Denne funktionalitet gælder for de fleste typer arbejdsoprettelsesprocesser, ikke mindst til oprettelse af pluk- og genopfyldningsarbejde. Hvis arbejdet oprettes i en *åben* tilstand, hvilket angiver, at arbejdet er klar til at blive kørt af en arbejder, genereres der generelt en hændelse til oprettelse af arbejde. Desuden genereres hændelser til oprettelse af arbejde for grundlæggende flyttearbejde (ikke bevægelse efter skabelonarbejde), selvom det arbejde ikke er oprettet som åbent arbejde.

En vigtig undtagelse i denne funktionsmåde er cyklusoptællingsarbejdet, som aktuelt ikke understøttes. Lagerbeholdningsantal i MH-systemet ligger uden for området af MHAX, og resultater af optællingen skal importeres til en lageroptællingskladde.

Når arbejdet er blevet oprettet, behandler MHAX-tjenesten de arbejdslinjer, der er genereret, og tildeler et arbejdslinjepar-id til alle genererede arbejdslinjer for hvert arbejdshoved. Målsætningen er at gruppere alle plukarbejdslinjer med efterfølgende læg på lager under ét arbejdslinjepar-id. (Grupperne svarer til pluk/læg-par i arbejdsskabeloner). På denne måde kan du bruge et enkelt id til at rapportere færdiggørelse af arbejde for alle relaterede pluk- og læglinjer. Grupperingsprocessen starter med den første linje og fortsætter derefter med det samme id, indtil der findes et efterfølgende par arbejdslinjer for læg/pluk. Det løbende id tildeles læg-linjen for det pågældende par. Et nyt id, som derefter bruges for pluklinjen i parret og fremad. Denne proces fortsætter, indtil den har behandlet alle linjer, der tilhører arbejdshovedet.

Som et specielt element i hændelser til oprettelse af arbejde, hvis **Blokeret bølge** er indstillet til *Ja* i arbejdshovedet, genereres der hændelser med statussen *Blokeret* i stedet for den normale status ad *Klar*, som bruges til at sende dem til MH-systemet. Flaget **Blokeret bølge** i arbejdshovedet angiver, at arbejdshovedet endnu ikke er klar til, at arbejderne kan køre, måske på grund af ikke-afsluttet genopfyldningsarbejde. Når flaget **Blokeret bølge** fjernes, frigøres de hændelser, der allerede er genereret, og de er tilgængelige, så MH-systemet kan hente dem fra køen.

#### <a name="work-initiation-events"></a>Hændelser til initiering af arbejde

Hændelser, der initierer arbejde, udløses, når arbejdsstatus ændres fra *Åben* til *Under behandling* under arbejdsopdatering.

#### <a name="work-completion-events"></a>Hændelser til fuldførelse af arbejde

Hændelser, der fuldfører arbejde, udløses, når arbejdsstatus ændres fra *Under behandling* til *Lukket* under arbejdsopdatering.

#### <a name="work-cancellation-events"></a>Hændelser til annullering af arbejde

Hændelser, der annullerer arbejde, udløses, når arbejdsstatus ændres fra enhver status undtagen *Annulleret* til *Annulleret* under arbejdsopdatering. Derudover slettes alle andre hændelser, der er relateret til arbejdshovedet, fra køen for alle abonnementer. På denne måde forhindres eksterne systemer i at behandle hændelser, der ikke er nødvendige.

#### <a name="pickput-completion-events"></a>Pluk-/læg-færdiggørelseshændelser

Pluk-/læg-færdiggørelseshændelser udløses, når status for pluk/læg-linjen ændres fra *Under behandling* til *Lukket* under arbejdslinjeopdatering.

### <a name="monitor-the-outbound-queue"></a>Overvåge den udgående kø

Du kan gennemse den udgående kø ved at gå til **Grænseflade for materialehåndteringsudstyr \> Fælles \> Udgående kø**. På siden **Udgående kø** vises alle udgående køelementer og statussen for dem. Vælg et køelement for at få vist oplysninger om det. Disse oplysninger omfatter elementets transaktionstype, det abonnement, der bruges, og værdier for hvert datafelt (**data01** til og med **data10**) og nyttelasten.

### <a name="clean-up-the-outbound-queue"></a>Rydde op i den udgående kø

I den sidste ende begynder din udgående kø at blive fuld af køelementer, der allerede er blevet sendt. Hvis du vil fjerne disse elementer, skal du gå til **Grænseflade for materialehåndteringsudstyr \> Periodiske opgaver \> Oprydning \> Oprydning af udgående kø**.

## <a name="inbound-events"></a>Indgående hændelser

I dette afsnit beskrives de forskellige typer indgående hændelser, som MH-systemet kan rapportere tilbage til WMS-systemet. Det forklarer også, hvilke data der skal leveres af MH-systemet, og hvad hver indgående hændelse gør i WMS-systemet.

### <a name="structure-of-inbound-events"></a>Struktur for indgående hændelser

Når der sendes en indgående hændelse, skal det eksterne system levere den indgående transaktionstype sammen med op til 10 parametre (**data01** til og med **data10**). Valgfri validering kan sikre, at MHAX-tjenesten ikke modtager samme indgående hændelse mere end én gang. Hvis du vil aktivere denne validering, skal hver indgående hændelse have et entydigt meddelelses-id. Hvis der modtages et identisk meddelelses-id, og hvis indstillingen **Aktiver indgående meddelelses-id** er angivet til *Ja* på siden **Parametre til grænseflade for materialehåndteringsudstyr**, vil meddelelsen blive afvist. Der vises en fejlmeddelelse om, at meddelelsen allerede findes.

Udover de indgående datafelter tildeler systemet et entydigt indgående kø-id til hændelsen.

### <a name="inbound-event-types"></a>Indgående hændelsestyper

I dette afsnit beskrives de indgående hændelsestyper (transaktionstyper), der understøttes, og de data, der skal angives for hændelser, der skal behandles.

#### <a name="work-confirm-events"></a>Arbejdsbekræftende hændelser

Arbejdsbekræftende hændelser kræver, at de indgående datafelter indeholder følgende oplysninger:

- **data01** – Id'et for arbejdslinjens par.
- **data02** – Post-id for arbejdslinje (`RecId`-værdi).

    > [!NOTE]
    > *Enten* feltet **data01** *eller* feltet **data02** skal være til stede.

- **data03** – Id'et for den nummerplade, der skal plukkes fra.
- **data04** – Arbejdshovedets målnummerplade-id.

Hvis id'et for arbejdslinjeparret er angivet, køres alle pluk-, læg- eller brugerdefinerede arbejdslinjer, der er markeret med id'et for arbejdslinjens par, og som har statussen *Åben* eller *Under behandling*, fortløbende. Hvis der angives et arbejdslinjepost-id (værdien `RecId`), skal arbejdslinjen være en pluk-, læg- eller brugerdefineret arbejdslinje, der har statussen *Åben* eller *Under behandling*.

Pluklinjer fra nummerpladestyrede lokationer kræver, at **data03** angiver den nummerplade, der skal plukkes fra, uanset om linjerne er markeret med arbejdslinjepost-id eller arbejdslinjepar-id. Feltet **data04** skal angive arbejdshovedets målnummerplade for plukket.

Læg-linjer accepterer ikke yderligere oplysninger. De køres kun på baggrund af den aktuelle arbejdslinjes lokation og arbejdets målnummerplade. Hvis lægningen skal angives på en anden lokation, skal du ændre arbejdslinjens lokation, som det beskrives i afsnittet [Tilsidesættelseshændelser](#override-events) senere i dette emne.

Brugerdefinerede arbejdslinjer kræver ikke eller understøtter ikke yderligere oplysninger i den indgående hændelse.

#### <a name="short-pick-events"></a>Korte plukhændelser

Korte plukhændelser kræver, at de indgående datafelter indeholder følgende oplysninger:

- **data02** – Post-id for arbejde (`RecId`-værdi).
- **data03** – Id'et for den nummerplade, der skal plukkes fra.
- **data04** – Det antal, der skal plukkes.
- **data05** – Undtagelseskoden for kort pluk.
- **data06** – Arbejdshovedets målnummerplade-id.

> [!NOTE]
> Feltet **data01** bruges ikke til korte plukhændelser.

Denne hændelse ligner hændelsen til bekræftelse af arbejde, men den gælder kun for pluklinjer.

#### <a name="override-events"></a><a id="override-events"></a>Tilsidesættelseshændelser

Tilsidesættelseshændelser kræver, at de indgående datafelter indeholder følgende oplysninger:

- **data01** – Post-id for arbejde (`RecId`-værdi).
- **data02** – Det nye lokations-id.

Arbejdslinjen skal have statussen *Åben* eller *Under behandling*, og den nye lokation skal findes.

#### <a name="license-plate-receipt-events"></a>Modtagelseshændelser for nummerplader

Modtagelseshændelser for nummerplader kræver, at de indgående datafelter indeholder følgende oplysninger:

- **data01** – Id'et for den indgående nummerplade, der skal modtages.

Systemet udfører en modtagehandling for nummerplader ud fra den nummerplade, der overføres som værdien i feltet **data01**.

### <a name="monitor-the-inbound-queue"></a>Overvåge den indgående kø

Du kan gennemse den indgående kø ved at gå til **Grænseflade for materialehåndteringsudstyr \> Fælles \> Indgående kø**. På siden **Indgående kø** vises alle indgående køelementer og statussen for dem. Vælg et køelement for at få vist oplysninger om det. Disse oplysninger omfatter elementets transaktionstype, meddelelses-id og værdier for hvert datafelt (**data01** til og med **data10**).

Hvis der opstod en fejl eller en anden type logelement, mens indgående hændelser blev behandlet, kan du kontrollere logfilen ved at vælge **Fejllog** i handlingsruden.

### <a name="inbound-event-processing"></a>Behandling af indgående hændelse

Indgående hændelser skrives først til databasen, og de køres derefter med det samme (synkront). Hvis der opstår en fejl under behandlingen, skrives hændelsen stadig til køen, men status er angivet til *Fejlbehæftet*. MHAX-tjenesten returnerer en fejlmeddelelse til MH-systemet og gemmer fejlloggen i den indgående hændelsespost, så den kan undersøges senere.

Hændelser med status *Fejlbehæftet* kan behandles igen senere, hvis fejltilstanden er løst. Følg et af disse trin for at behandle dem igen:

- Gå til **Grænseflade for materialehåndteringsudstyr \> Fælles \> Indgående kø**. Vælg den relevante indgående kø, og vælg derefter **Genbehandling** i handlingsruden.
- Gå til **Grænseflade for materialehåndteringsudstyr \> Fælles \> Genbehandling af fejlbehæftet indgående kø**. Der vises en standarddialogboks til batchjob. Her kan du konfigurere et postfilter og planlægge eller køre et batchjob til genbehandling af køen.

Alle arbejdsoperationer (pluk og lægning) køres med brug af den arbejder, der er valgt i feltet **Bruger-id** på siden **Parametre til grænseflade for materialehåndteringsudstyr**.

### <a name="clean-up-the-inbound-queue"></a>Rydde op i den indgående kø

I den sidste ende begynder din indgående kø at blive fuld af køelementer, der allerede er blevet behandlet. Hvis du vil fjerne disse elementer, skal du gå til **Grænseflade for materialehåndteringsudstyr \> Periodiske opgaver \> Oprydning \> Oprydning af indgående kø**.

## <a name="get-a-quick-overview-by-using-the-queue-manager"></a>Få et hurtigt overblik ved hjælp af køstyring

Du kan få et hurtigt overblik over alle de aktiviteter, der er relateret til dine indgående og udgående køer, ved at gå til **Grænseflade for materialehåndteringsudstyr \> Arbejdsområder \> Køstyring**. Siden **Køstyring** indeholder et sæt faner og felter, du kan bruge til at overvåge og undersøge køerne. Den giver også nyttige links til de fleste andre sider, der nævnes i dette emne.

## <a name="connect-to-the-mhax-service"></a>Oprette forbindelse til MHAX-tjenesten

MHAX er implementeret som en brugerdefineret tjeneste. Der er derfor adgang til den via SOAP- og REST-opkald. Her er adresserne på SOAP- og REST-slutpunkterne:

- **SOAP:** `https://base_environment_URL/soap/services/WMHEServices`
- **REST:** `https://base_environment_URL/api/services/WMHEServices/WMHEService`

## <a name="retrieve-messages-from-the-outbound-queue"></a>Modtage meddelelser fra den udgående kø

Hvis du vil modtage meddelelser fra den udgående kø, skal du benytte en af følgende metoder:

- Brug `readOutboundSubscriptionQueue` til at hente hændelserne baseret på abonnements-id'et.
- Brug `readOutboundWarehouseQueue` til at hente hændelserne baseret på hændelsestypen og lagersteds-id'et på tværs af flere abonnementer.
