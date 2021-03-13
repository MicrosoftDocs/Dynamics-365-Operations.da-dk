---
title: Sky- og kantskalaenheder til arbejdsbyrder i lokationsstyring
description: Dette emne indeholder oplysninger om funktionen, der gør det muligt for skalaenheder at køre udvalgte processer fra din arbejdsbyrde i lokationsstyring.
author: perlynne
manager: tfeyr
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, SysSecRolesEditUsers
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 91e614889c719ae700b13e54150e5025d64e2b97
ms.sourcegitcommit: 289e9183d908825f4c8dcf85d9affd4119238d0c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104934"
---
# <a name="warehouse-management-workloads-for-cloud-and-edge-scale-units"></a>Arbejdsbelastninger i forbindelse med lokationsstyring for sky- og edge-skaleringsenheder

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> Ikke alle forretningsfunktioner i lokationsstyring understøttes fuldt ud på lagersteder, der kører en arbejdsbyrde på en skalaenhed. Sørg for kun at bruge de processer, som dette emne direkte beskriver som understøttede.

## <a name="warehouse-execution-on-scale-units"></a>Lagerudførelse på skalaenheder

Med denne funktion kan skalaenheder køre udvalgte processer fra funktionerne til lokationsstyring. Enheder i skyskala kører deres arbejdsbyrder i skyen ved at bruge dedikeret behandlingskapacitet i det valgte Microsoft Azure-område. I forbindelse med kantskalaenheder kan du køre nogle arbejdsbyrder uafhængigt i det lokale miljø, også selvom skalaenhederne midlertidigt afbrydes fra skyen.

I dette emne kaldes udførelse af lokationsstyring på et lagersted, der er defineret som en skalaenhed, for et *Lagerudførelsessystem* (*WES*).

## <a name="prerequisites"></a>Forudsætninger

Du skal have en Dynamics 365 Supply Chain Management-hub og en skalaenhed, der er implementeret med arbejdsbyrden for lokationsstyring. Du kan finde flere oplysninger om arkitektur og udrulningsprocesser under [Sky- og kantskalaenheder til arbejdsbyrder i produktion og lokationsstyring](cloud-edge-landing-page.md).

## <a name="how-the-wes-workload-works-on-scale-units"></a>Sådan fungerer WES-arbejdsbyrde på skalaenheder

I forbindelse med processerne i arbejdsbyrden for lokationsstyring synkroniseres dataene mellem hubben og skalaenhederne.

En skalaenhed kan kun vedligeholde de data, som den ejer. Dataejerskabsbegrebet for skalaenheder medvirker til at forhindre multimasterkonflikter. Det er derfor vigtigt, at du forstår, hvilke processer der ejes af hubben, og hvilke som ejes af skalaenhederne.

Skalaenhederne ejer følgende data:

- **Bølgebehandlingsdata** – Udvalgte bølgeprocesmetoder håndteres som en del af bølgebehandlingen på skalaenheden.
- **Data til arbejdsbehandling** – Følgende typer behandling af arbejdsordrer understøttes:

  - **Lagerbevægelser** (manuel bevægelse og bevægelse efter skabelonarbejde)
  - **Indkøbsordrer** (læg på lager-arbejde via en lagerstedsordre, når indkøbsordrer ikke er tilknyttet laster)
  - **Salgsordrer** (simpelt pluk- og lastarbejde)
  - **Flytteordrer** (kun udgående med simpel pluk- og lastarbejde)

- **Kvitteringsdata for lagerstedsordre** – Disse data bruges kun til indkøbsordrer, der frigives manuelt til et lagersted.
- **Nummerpladedata** – Nummerplader kan oprettes på hubben og skalaenheden. Der er leveret dedikeret konflikthåndtering. Bemærk, at disse data ikke er lagerstedsspecifikke.

## <a name="outbound-process-flow"></a>Udgående procesflow

Hubben ejer følgende data:

- Alle kildedokumenter, f.eks. salgsordrer og flytteordrer
- Ordrefordeling og behandling af udgående last
- Processerne frigiv til lagersted, forsendelsesoprettelse, bølgeoprettelse og bølgefærdiggørelse

Skalaenhederne ejer den faktiske bølgebehandling (f.eks. arbejdsfordeling, genopfyldningsarbejde og oprettelse af behovsarbejde) efter frigivelsen af bølgen. Lagermedarbejderne kan derfor behandle udgående arbejde ved hjælp af en lagerstedsapp, der er tilknyttet skalaenheden.

![Bølgebehandlingsflow](./media/wes-wave-processing-ga.png "Bølgebehandlingsflow")

## <a name="inbound-process-flow"></a>Indgående procesflow

Hubben ejer følgende data:

- Alle kildedokumenter, f.eks. indkøbsordrer og salgsreturordrer
- Indgående lastbehandling
- Alle opdateringer af omkostning og økonomi

> [!NOTE]
> Det indgående indkøbsordreflow er grundlæggende forskelligt fra det udgående flow. Du kan operere det samme lagersted på enten skalaenheden eller hubben, afhængigt af om indkøbsordren er frigivet til lagerstedet eller ej. Når du har frigivet en ordre til lagerstedet, kan du kun arbejde med den pågældende ordre, når du er logget på skalaenheden.

Hvis du bruger *frigivelse til lagersted* som proces, oprettes der [*lagerstedsordrer*](cloud-edge-warehouse-order.md), og ejerskabet af det tilknyttede modtagelsesflow tildeles til skalaenheden. Hubben kan ikke registrere indgående modtagelse.

Arbejderne kan køre modtagelsen ved hjælp af en lagerstedsapp, der er tilknyttet skalaenheden. Dataene registreres derefter af skalaenheden og rapporteres i forhold til den indgående lagerordre. Oprettelsen og afviklingen af det efterfølgende læg på lager-arbejde vil også blive håndteret af skalaenheden.

Hvis du ikke bruger processen *frigivelse til lagersted*, og du derfor ikke bruger *lagerordrer*, kan hubben behandle lagermodtagelse og arbejde uafhængigt af skalaenheder.

![Indgående procesflow](./media/wes-inbound-ga.png "Indgående procesflow")

## <a name="supported-processes-and-roles"></a>Understøttede processer og roller

Ikke alle processer til lokationsstyring understøttes i en WES-arbejdsbyrde på en skalaenhed. Det anbefales derfor, at du tildeler roller, der stemmer overens med de funktioner, der er tilgængelige for de enkelte brugere.

For at lette denne proces inkluderes en eksempelrolle med navnet *Lagerchef på arbejdsbyrde* i demodataene i **Systemadministration \> Sikkerhed \> Sikkerhedskonfiguration**. Formålet med denne rolle er at gøre det muligt for lagercheferne at få adgang til WES på skalaenheden. Rollen giver adgang til de sider, der er relevante i forbindelse med en arbejdsbyrde, der har en skalaenhed som vært.

Brugerroller på en skalaenhed tildeles som en del af den første datasynkronisering fra hubben til skalaenheden.

Hvis du vil redigere de roller, der er tildelt til en bruger, skal du gå til **Systemadministration \> Sikkerhed \> Tildele brugere til roller**. Brugere, der kun fungerer som lagerchefer på skalaenheder, bør kun tildeles rollen *Lagerchef på arbejdsbyrde*. Denne fremgangsmåde sikrer, at de pågældende brugere kun har adgang til de understøttede funktioner. Fjern eventuelle andre roller, der er tildelt til disse brugere.

Brugere, der kun fungerer som lagerchefer på både hubben og skalaenheder, bør tildeles den eksisterende rolle *Lagerarbejder*. Bemærk, at denne rolle giver lagerarbejderne adgang til funktioner (f.eks. modtagelsesbehandling af flytteordre), der vises i brugergrænsefladen, men ikke understøttes i øjeblikket på skalaenheder.

## <a name="supported-wes-processes"></a>Understøttede WES-processer

Følgende processer til lagerudførelse kan aktiveres for en WES-arbejdsbyrde på en skalaenhed:

- Udvalgte metoder til salgs- og flytteordrer (fordeling, efterspørgselsopfyldning, containerisering, oprettelse af arbejde og udskrivning af label til bølge)
- Behandle arbejde med salgs- og flytteordrelagersteder ved hjælp af lagerstedsappen (herunder genopfyldningsarbejde)
- Forespørge på disponibel lagerbeholdning ved hjælp af lagerstedsappen
- Oprette og køre lagerbevægelser ved hjælp af lagerstedsappen
- Registrere indkøbsordrer og udføre læg på lager-arbejde med lagerstedsappen

Følgende arbejdsordretyper understøttes i øjeblikket for WES-arbejdsbyrder på implementeringer af skalaenheder:

- Salgsordre
- Flytteafgang
- Opfyldning
- Lagerbevægelse
- Indkøbsordrer (knyttet til lagerstedsordrer)

Ingen anden behandling af kildedokumenter eller lagerstedsarbejde understøttes i øjeblikket på skalaenheder. I forbindelse med en WES-arbejdsbyrde på en skalaenhed kan du f.eks. ikke udføre en modtagelsesproces for overførselsordrer (overførselstilgang) eller behandle cyklusoptællingsarbejde.

> [!NOTE]
> Menupunkter og knapper til mobilenheder til funktioner, der ikke understøttes, vises ikke i _lagerstedsappen_, når den er knyttet til en implementering af skalaenhed.

> [!WARNING]
> Når du kører en arbejdsbyrde i en skalaenhed, kan du ikke køre processer, der ikke understøttes, for det specifikke lagersted på hubben. Tabellerne senere i dette emne dokumenterer de understøttede egenskaber.
>
> Valgte arbejdstyper for lagersteder kan oprettes både på hubben og skalaenheder, men kan kun vedligeholdes af ejerhubben eller -skalaenheden (den installation, der har oprettet dataene).
>
> Selv når en bestemt proces understøttes i skalaenheden, skal du være opmærksom på, at alle nødvendige data muligvis ikke bliver synkroniseret fra hubben til skalaenheden eller fra skalaenheden til hubben, hvilket udgør en risiko for uventet systembehandling. Eksempler som disse:
> 
> - Hvis du bruger en forespørgsel om lokationsvejledning, der tilknytter en datatabelpost, som kun findes i hubimplementeringen.
> - Hvis du bruger lokationsstatus og/eller lokationsmængder som lastfunktioner. Disse data synkroniseres ikke mellem implementeringerne og vil derfor kun fungere, når lokationslagerbeholdningen opdateres for en af installationerne.

Følgende lokationsstyringsfunktioner understøttes ikke i øjeblikket i arbejdsbelastninger på skalaenheder:

- Indgående behandling af indkøbsordrelinjer, der er tilknyttet en last
- Indgående behandling af indkøbsordrer for et projekt
- Indgående og udgående behandling af varer, der har aktive sporingsdimensioner **Ejer** og/eller **Serienummer**
- Behandling af lager, der har en blokeringsstatusværdi
- Ændring af lagerstatus under en hvilken som helst arbejdsbevægelsesproces
- Ordrebekræftede fleksible reservationer for dimension på lagerstedsniveau
- Brug af funktionen *Lokationsstatus for lagersted* (dataene synkroniseres ikke mellem implementeringerne)
- Brug af funktionen *Placering af lokations-id*
- Brug af *Produktfiltre* og *Produktfiltergrupper*, herunder indstillingen **Antal dage til at sammensætte batches**
- Integration med kvalitetsstyring
- Behandling med fastvægtvarer
- Behandling med varer, der kun er aktiveret til transportstyring (TMS)
- Behandling med negativ disponibel lagerbeholdning
- Behandling af lagerstedsarbejde med brugerdefinerede arbejdstyper
- Behandling af lagerstedsarbejde med forsendelsesnotaer
- Behandling af lagerstedsarbejde med grænseværdi for behandling af cyklusoptælling
- Behandling af lagerstedsarbejde med materialehåndtering/automatisk lagersted
- Brug af billede af produktmasterdata (f.eks. på lagerstedsappen)

> [!WARNING]
> Nogle af lagerstedsfunktionerne er ikke tilgængelige for lagersteder, der kører arbejdsbyrderne for lokationsstyring på en skalaenhed, og de understøttes heller ikke i hubben eller i arbejdsbyrden for skalaenheden.
> 
> Andre egenskaber kan behandles på begge, men vil kræve nøje brug i visse scenarier, f.eks. når lagerbeholdning opdateres for det samme lagersted på både hubben og skalaenheden på grund af den asynkrone dataopdateringsproces.
> 
> Specifikke funktioner (som f.eks. *blokringsarbejde*), der understøttes på både hubben og skalaenheder, vil kun blive understøttet for ejeren af dataene.

### <a name="outbound-supported-only-for-sales-and-transfer-orders"></a>Udgående (kun understøttet for salgsordrer og flytteordrer)

I følgende tabel vises, hvilke udgående funktioner der understøttes, og hvor de understøttes, når arbejdsbelastningen for lokationsstyring bruges i sky- og kantskalaenheder.

| Behandling                                                      | Hub | WES-arbejdsbyrde på en skalaenhed |
|--------------------------------------------------------------|-----|------------------------------|
| Behandling af kildedokument                                   | Ja | Nej |
| Last- og transportstyringsbehandling                | Ja | Ingen |
| Frigiv til lagersted                                         | Ja | Ingen |
| Planlagt direkte levering                                        | Ingen  | Ingen |
| Konsolidering af forsendelse                                       | Ja | Ingen |
| Behandling af forsendelsesbølge                                     | Ja, men kun initialisering og færdiggørelse af bølgen håndteres i hubben. Det betyder, at behandling af udgående flytte- og salgsordrer kun kan håndteres af skalaenheden.|<p>Nej, initialisering og færdiggørelse håndteres af hubben, og **Lastopbygning og -sortering** understøttes ikke<p><b>Bemærk:</b> Der kræves adgang til denne hub for at færdiggøre bølgestatussen som en del af bølgebehandlingen.</p> |
| Vedligeholde forsendelser for bølge                                  | Ja | Ingen |
| Lagerstedsbehandling (inkl. udskrivning af nummerplade)        | Ingen  | <p>Ja, men kun for ovennævnte understøttede egenskaber. |
| Klyngepluk                                              | Ingen  | Ja|
| Manuel behandling af emballage, herunder arbejdet "Plukning af pakket container"                                           | Ingen <P>En del af behandlingen kan udføres efter den første plukproces, der håndteres af en skalaenhed, men det frarådes på grund af følgende blokerede operationer.</p>  | Ingen  |
| Fjern container fra gruppe                        | Ingen  | Ingen                           |
| Behandling af udgående sortering                                  | Ingen  | Ingen |
| Udskrivning af lastrelaterede dokumenter                           | Ja | Ingen |
| Fragtseddel og ASN-generering                            | Ja | Ingen |
| Forsendelsesbekræftelse                    | Ja  | Ingen |
| Forsendelsesbekræftelse med "Bekræft og flyt"                    | Ingen  | Ingen |
| Behandling af følgesedler og fakturering                | Ja | Ingen |
| Kort pluk (salgs- og flytteordrer)                    | Ingen  | Ingen |
| Overpluk (salgs- og flytteordrer)                     | Ingen  | Ingen |
| Ændring af arbejdssteder (salgs- og flytteordrer)         | Ingen  | Ja|
| Fuldføre arbejde (salgs- og flytteordrer)                    | Ingen  | Ja|
| Udskrive arbejdsordrerapport                                            | Ja | Ingen |
| Bølgelabel                                                   | Ingen  | Ja|
| Arbejdsopdeling                                                   | Ingen  | Ja|
| Arbejdsbehandling – Styres af "Lastning af transport"            | Ingen  | Ingen |
| Reducer det antal, der er plukket                                       | Ingen  | Ingen |
| Tilbagefør arbejde                                                 | Ingen  | Ingen |
| Tilbagefør forsendelsesbekræftelse                                | Ja | Ingen |

### <a name="inbound"></a>Indgående

I følgende tabel vises, hvilke indgående funktioner der understøttes, og hvor de understøttes, når arbejdsbelastningen for lokationsstyring bruges i sky- og kantskalaenheder.

| Behandling                                                          | Hub | WES-arbejdsbyrde på en skalaenhed<BR>*(Varer, der er markeret "Ja", gælder kun for lagerstedsordrer)*</p> |
|------------------------------------------------------------------|-----|----------------------------------------------------------------------------------|
| Behandling af kildedokument                                       | Ja | Ingen |
| Last- og transportstyringsbehandling                    | Ja | Ingen |
| Bekræftelse af indgående forsendelse                                            | Ja | Ingen |
| Frigivelse af indkøbsordre til lagersted (behandling af lagerstedsordre) | Ja | Ingen |
| Annullering af ordrelinjer på lagersted<p>Bemærk, at dette kun understøttes, når der ikke er sket nogen registrering for linjen</p>          | Ja | Ingen |
| Indkøbsordrevare til modtagelse og læg på lager                       | <p>Ja,&nbsp;når&nbsp;der&nbsp;ikke er en lagerordre</p><p>Nej, når der er en lagerordre</p> | <p>Ja, når en indkøbsordre ikke er del af en <i>last</i></p> |
| Indkøbsordrelinje til modtagelse og læg på lager                        | <p>Ja, når der ikke er en lagerordre</p><p>Nej, når der er en lagerordre</p> | <p>Ja, når en indkøbsordre ikke er del af en <i>last</i></p></p> |
| Modtagelse af returordre og placering på lager                               | Ja | Ingen |
| Modtagelse af blandede id'er og placering på lager                        | <p>Ja, når der ikke er en lagerordre</p><p>Nej, når der er en lagerordre</p> | Nej |
| Modtagelse af varelast                                             | <p>Ja, når der ikke er en lagerordre</p><p>Nej, når der er en lagerordre</p> | Nej |
| Modtagelse af nummerplade og placering på lager                              | <p>Ja, når der ikke er en lagerordre</p><p>Nej, når der er en lagerordre</p> | Nej |
| Modtagelse af vare i flytteordre og placering på lager                        | Ja | Ingen |
| Flytteordrelinje til modtagelse og placering på lager                        | Ja | Ingen |
| Annuller arbejde (indgående)                                              | <p>Ja, når der ikke er en lagerordre</p><p>Nej, når der er en lagerordre</p> | <p>Ja, men kun når indstillingen <b>Fjern registrering af modtagelse, når du annullerer arbejde</b> (på siden <b>Parametre til lokationsstyring</b>) er ryddet</p> |
| Behandle indkøbsordre - produktkvittering                          | Ja | Ingen |
| Indkøbsordre, der modtages med underlevering                        | <p>Ja, når der ikke er en lagerordre</p><p>Nej, når der er en lagerordre</p> | Nej, da du kun kan annullere hele ordrelinjeantal på lagersted |
| Indkøbsordre, der modtages med overlevering                        | <p>Ja, når der ikke er en lagerordre</p><p>Nej, når der er en lagerordre</p> | Ja  |
| Modtagelse med oprettelse af *Cross-docking*-arbejde                   | <p>Ja, når der ikke er en lagerordre</p><p>Nej, når der er en lagerordre</p> | Ingen |
| Modtagelse med oprettelse af *Kvalitetsordre*-arbejde                  | <p>Ja, når der ikke er en lagerordre</p><p>Nej, når der er en lagerordre</p> | Ingen |
| Modtagelse med oprettelse af *Kvalitetsvareprøve*-arbejde          | <p>Ja, når der ikke er en lagerordre</p><p>Nej, når der er en lagerordre</p> | Ingen |
| Modtagelse med oprettelse af *Kvalitet i kvalitetskontrol*-arbejde       | <p>Ja, når der ikke er en lagerordre</p><p>Nej, når der er en lagerordre</p> | Ingen |
| Modtagelse med oprettelse af kvalitetsordre                            | <p>Ja, når der ikke er en lagerordre</p><p>Nej, når der er en lagerordre</p> | Ingen |
| Arbejdsbehandling – Styres af *Læg på lager-klynge*                             | Ja | Ingen |
| Arbejdsbehandling med *Kort pluk*                                           | Ja | Ingen |
| Indlæsning af nummerplade                                           | Ja | Ingen |

### <a name="warehouse-operations-and-exception-handing"></a>Lagerstedsoperationer og håndtering af undtagelser

I følgende tabel vises, hvilke funktioner til håndtering af lageroperationer og undtagelser der understøttes, og hvor de understøttes, når arbejdsbelastningen for lokationsstyring bruges i sky- og kantskalaenheder.

| Behandling                                            | Hub | WES-arbejdsbyrde på en skalaenhed |
|----------------------------------------------------|-----|------------------------------|
| Forespørge på nummerplade                              | Ja | Ja                          |
| Vareforespørgsel                                       | Ja | Ja                          |
| Lokationsforespørgsel                                   | Ja | Ja                          |
| Skift lagersted                                   | Ja | Ja                          |
| Bevægelse                                           | Ja | Ja                          |
| Bevægelse efter skabelon                               | Ja | Ja                          |
| Overførsel af lagersted                                 | Ja | Ingen                           |
| Oprette flytteordre fra lagerstedsappen           | Ja | Ingen                           |
| Regulering (ind/ud)                                | Ja | Ingen                           |
| Ændring af lagerstatus                            | Ja | Ingen                           |
| Behandling af cyklusoptælling og optællingsafvigelser | Ja | Ingen                           |
| Genudskrive etiket (udskrive nummerplade)             | Ja | Ja                          |
| Id-build                                | Ja | Ingen                           |
| Id-pause                                | Ja | Ingen                           |
| Pak til indlejrede id'er                                | Ja | Ingen                           |
| Chaufførens check-in                                    | Ja | Ingen                           |
| Chaufførens check-ud                                   | Ja | Ingen                           |
| Skifte batchdispositionskode                      | Ja | Ja                          |
| Vis oversigt over åbne opgaver                             | Ja | Ja                          |
| Konsolider id'er                         | Ja | Ingen                           |
| Behandling af min./maks. og zonetærskelopfyldning| Ja <p>Anbefalingen er ikke at medtage de samme lokationer som en del af forespørgslerne</p>| Ja                          |
| Behandle allokeringsgenopfyldning                  | Ja  | Ja<p>Bemærk, at opsætningen skal udføres på skalaenheden</p>                           |
| Blokere og fjerne blokering af arbejde                             | Ja | Ja                          |
| Skift bruger                                        | Ja | Ja                          |
| Skift arbejdspulje på arbejde                           | Ja | Ja                          |
| Annuller arbejde                                        | Ja | Ja                          |


### <a name="production"></a>Produktion

Produktionsscenarier for lokationsstyring understøttes ikke i øjeblikket i arbejdsbelastninger på skalaenheder, som angivet i følgende tabel.

| Behandling | Hub | WES-arbejdsbyrde på en skalaenhed |
|---------|-----|------------------------------|
| <p>Alle de lokationsstyringsprocesser, der er relateret til produktion. Her er nogle eksempler:</p><li>Frigiv til lagersted</li><li>Produktionsbølgebehandling</li><li>Råvarepluk</li><li>Færdigmeldte og færdige varer, læg på lager</li><li>Samprodukt og biprodukt, læg på lager</li><li>Kanban-læg på lager</li><li>Kanban-pluk</li><li>Start produktionsordre</li><li>Produktionsspild</li><li>Sidste produktionspalle</li><li>Registrer materialeforbrug</li><li>Tøm kanban</li></ul> | Ja | Ingen |

## <a name="maintaining-scale-units-for-wes"></a>Bevare skalaenheder for WES

Flere batchjob kører på både hubben og skalaenheder.

Under installationen af hub kan du vedligeholde batchjobbene manuelt. Du kan administrere følgende batchjob i **Lokationsstyring \> Periodiske opgaver \> Backoffice-styring af arbejdsbyrder**:

- Opdateringshændelse for arbejdsstatusproces
- Skalaenhed til meddelelsesprocessors hub
- Registrer kvitteringer på kildeordre
- Fuldfør lagerstedsordrer
- Foretag behandling af svar på opdatering af antal for lagerstedsordrelinjer

På arbejdsbyrden i skalaenheder kan du administrere følgende batchjob i **Lokationsstyring \> Periodiske opgaver \> Styring af arbejdsbyrder**:

- Behandle bølgetabelposter
- Meddelelsesprocessor for lagerstedshub til skalaenhed
- Foretag behandling af anmodninger om opdatering af antal for lagerstedsordrelinjer
