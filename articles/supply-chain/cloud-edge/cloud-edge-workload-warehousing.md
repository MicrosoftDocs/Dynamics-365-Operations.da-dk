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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 4ac76ad5cd88c35ac312b8e73d942a692f35c8aa
ms.sourcegitcommit: 8eefb4e14ae0ea27769ab2cecca747755560efa3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/13/2020
ms.locfileid: "4516750"
---
# <a name="warehouse-management-workloads-for-cloud-and-edge-scale-units"></a>Sky- og kantskalaenheder til arbejdsbyrder i lokationsstyring

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> Ikke alle forretningsfunktioner understøttes fuldt ud i den offentlige prøveversion, når der anvendes skalaenheder for arbejdsbyrder. Sørg for kun at bruge de processer, som dette emne direkte beskriver som understøttede.

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

    - Lagerbevægelser (manuel bevægelse og bevægelse efter skabelonarbejde)
    - Indkøbsordrer (læg på lager-arbejde via en lagerordre)
    - Salgsordrer (simpelt pluk- og lastarbejde)

- **Kvitteringsdata for lagerstedsordre** – Disse data bruges kun til indkøbsordrer, der frigives manuelt til et lagersted.
- **Nummerpladedata** – Nummerplader kan oprettes på hubben og skalaenheden. Der er leveret dedikeret konflikthåndtering. Bemærk, at disse data ikke er lagerstedsspecifikke.

## <a name="outbound-process-flow"></a>Udgående procesflow

Hubben ejer følgende data:

- Alle kildedokumenter, f.eks. salgsordrer og flytteordrer
- Ordrefordeling og behandling af udgående last
- Processerne Frigiv til lagersted, forsendelsesoprettelse og bølgeoprettelse

Skalaenhederne ejer den faktiske bølgebehandling (f.eks. arbejdsfordeling, genopfyldningsarbejde og oprettelse af behovsarbejde) efter frigivelsen af bølgen. Lagermedarbejderne kan derfor behandle udgående arbejde ved hjælp af en lagerstedsapp, der er tilknyttet skalaenheden.

![Bølgebehandlingsflow](./media/wes_wave_processing_flow.png "Bølgebehandlingsflow")

## <a name="inbound-process-flow"></a>Indgående procesflow

Hubben ejer følgende data:

- Alle kildedokumenter, f.eks. indkøbsordrer og salgsreturordrer
- Indgående lastbehandling

> [!NOTE]
> Det indgående indkøbsordreflow er konceptuelt anderledes end det udgående flow, hvor den skalaenhed, der udfører behandlingen, afhænger af, om ordren er frigivet til et lagersted.

Hvis du bruger *frigivelse til lagersted* som proces, oprettes der lagerordrer, og ejerskabet af det tilknyttede modtagelsesflow tildeles til skalaenheden. Hubben kan ikke registrere indgående modtagelse.

Arbejderne kan køre modtagelsen ved hjælp af en lagerstedsapp, der er tilknyttet skalaenheden. Dataene registreres derefter af skalaenheden og rapporteres i forhold til den indgående lagerordre. Oprettelsen og afviklingen af det efterfølgende læg på lager-arbejde vil også blive håndteret af skalaenheden.

Hvis du ikke bruger processen *frigivelse til lagersted*, og du derfor ikke bruger *lagerordrer*, kan hubben behandle lagermodtagelse og arbejde uafhængigt af skalaenheder.

![Indgående procesflow](./media/wes_Inbound_flow.png "Indgående procesflow")

## <a name="supported-processes-and-roles"></a>Understøttede processer og roller

Ikke alle processer til lokationsstyring understøttes i en WES-arbejdsbyrde på en skalaenhed. Det anbefales derfor, at du tildeler roller, der stemmer overens med de funktioner, der er tilgængelige for de enkelte brugere.

For at lette denne proces inkluderes en eksempelrolle med navnet *Lagerchef på arbejdsbyrde* i demodataene i **Systemadministration \> Sikkerhed \> Sikkerhedskonfiguration**. Formålet med denne rolle er at gøre det muligt for lagercheferne at få adgang til WES på skalaenheden. Rollen giver adgang til de sider, der er relevante i forbindelse med en arbejdsbyrde, der har en skalaenhed som vært.

Brugerroller på en skalaenhed tildeles som en del af den første datasynkronisering fra hubben til skalaenheden.

Hvis du vil redigere de roller, der er tildelt til en bruger, skal du gå til **Systemadministration \> Sikkerhed \> Tildele brugere til roller** på skalaenheden. Brugere, der kun fungerer som lagerchefer på skalaenheder, bør kun tildeles rollen *Lagerchef på arbejdsbyrde*. Denne fremgangsmåde sikrer, at de pågældende brugere kun har adgang til de understøttede funktioner. Fjern eventuelle andre roller, der er tildelt til disse brugere.

Brugere, der kun fungerer som lagerchefer på både hubben og skalaenheder, bør tildeles den eksisterende rolle *Lagerarbejder*. Bemærk, at denne rolle giver lagerarbejderne adgang til funktioner (f.eks. flytteordrebehandling), der vises i brugergrænsefladen, men ikke understøttes i i øjeblikket på skalaenheder.

## <a name="supported-wes-processes"></a>Understøttede WES-processer

Følgende processer til lagerudførelse kan aktiveres for en WES-arbejdsbyrde på en skalaenhed:

- Udvalgte bølgemetoder for salgsordrer og behovsgenopfyldning
- Køre arbejdsordrer fra salgsordrer og behovsgenopfyldning ved hjælp af lagerstedsappen
- Forespørge på disponibel lagerbeholdning ved hjælp af lagerstedsappen
- Oprette og køre lagerbevægelser ved hjælp af lagerstedsappen
- Registrere indkøbsordrer og udføre læg på lager-arbejde med lagerstedsappen

Følgende arbejdsordretyper understøttes i øjeblikket for WES-arbejdsbyrder på implementeringer af skalaenheder:

- Salgsordre
- Opfyldning
- Lagerbevægelse
- Indkøbsordrer, der er knyttet til lagerordrer

Ingen anden behandling af kildedokumenter understøttes i øjeblikket på skalaenheder. For en WES-arbejdsbyrde på en skalaenhed kan du f.eks. ikke udføre følgende handlinger:

- Frigive en flytteordre.
- Behandle udgående lagerpluk og forsendelsesoperationer.

> [!IMPORTANT]
> Hvis du bruger en arbejdsbyrde i en skalaenhed, kan du ikke køre processer, der ikke understøttes, for det specifikke lagersted på hubben.

Følgende lokationsstyringsfunktioner understøttes ikke i øjeblikket i skalaenheder:

- Indgående og udgående behandling af varer, der har aktive sporingsdimensioner (f.eks. batch- eller serienummerdimensioner)
- Behandling af ændringer i lagerstatus
- Behandling af lager, der har en blokeringsstatusværdi
- Integration med kvalitetsstyring
- Integration med produktion
- Behandling af fastvægtvarer
- Behandling af overlevering og underlevering
- Behandling af negativ disponibel lagerbeholdning

### <a name="outbound-supported-only-for-sales-orders-and-demand-replenishment"></a>Udgående (kun understøttet for salgsordrer og behovsgenopfyldning)

I følgende tabel vises, hvilke udgående funktioner der understøttes, og hvor de understøttes, når arbejdsbelastningen for lokationsstyring bruges i sky- og kantskalaenheder.

> [!WARNING]
> Da der kun understøttes salgsordrebehandling, kan udgående behandling af lokationsstyring ikke bruges til flytteordrer.
>
> Nogle lagerfunktioner er ikke tilgængelige på lagersteder, der kører arbejdsbelastningen for lokationsstyring i en skalaenhed.

| Behandling                                                      | Hub | WES-arbejdsbyrde på en skalaenhed |
|--------------------------------------------------------------|-----|------------------------------|
| Behandling af kildedokument                                   | Ja | Nej |
| Last- og transportstyringsbehandling                | Ja | Nej |
| Frigiv til lagersted                                         | Ja | Nej |
| Konsolidering af forsendelse                                       | Nej  | Nej |
| Cross-docking (plukarbejde)                                 | Nej  | Nej |
| Behandling af forsendelsesbølge                                     | Nej, men afslutning af bølgestatus håndteres i hubben |<p>Ja, men følgende funktioner understøttes ikke:</p><ul><li>Oprettelse af parallelarbejde</li><li>Lastopbygning og -sortering</li><li>Containerisering</li><li>Bølgeetiketudskrivning</li></li></ul><p><b>Bemærk:</b> Der kræves adgang til denne hub for at færdiggøre bølgestatussen som en del af bølgebehandlingen.</p> |
| Lagerstedsbehandling (inkl. udskrivning af nummerplade)     | Nej  | <p>Ja, men kun for følgende egenskaber:</p><ul><li>Salgspluk (uden brug af aktive sporingsdimensioner)</li><li>Salgslast (uden brug af aktive sporingsdimensioner)</li></ul> |
| Klyngepluk                                              | Nej  | Nej |
| Emballagebehandling                                           | Nej  | Nej |
| Behandling af udgående sortering                                  | Nej  | Nej |
| Udskrivning af lastrelaterede dokumenter                           | Ja | Nej |
| Fragtseddel og ASN-generering                            | Ja | Nej |
| Behandling af forsendelsesbekræftelse og følgeseddel                | Ja | Nej |
| Kort pluk (salgsordrer)                                 | Nej  | Nej |
| Annullering af arbejde                                            | Nej  | Nej |
| Ændring af arbejdssteder (salgsordrer)                      | Nej  | Nej |
| Fuldføre arbejde (salgsordrer)                                 | Nej  | Nej |
| Blokere og fjerne blokering af arbejde                                       | Nej  | Nej |
| Skift bruger                                                  | Nej  | Nej |
| Udskrive arbejdsordrerapport                                            | Nej  | Nej |
| Bølgelabel                                                   | Nej  | Nej |
| Tilbagefør arbejde                                                 | Nej  | Nej |

### <a name="inbound"></a>Indgående

I følgende tabel vises, hvilke indgående funktioner der understøttes, og hvor de understøttes, når arbejdsbelastningen for lokationsstyring bruges i sky- og kantskalaenheder.

| Behandling                                                          | Hub | WES-arbejdsbyrde på en skalaenhed |
|------------------------------------------------------------------|-----|------------------------------|
| Behandling af kildedokument                                       | Ja | Nej |
| Last- og transportstyringsbehandling                    | Ja | Nej |
| Forsendelsesbekræftelse                                            | Ja | Nej |
| Frigivelse af indkøbsordre til lagersted (behandling af lagerstedsordre) | Ja | Nej |
| Indkøbsordrevare til modtagelse og læg på lager                        | <p>Ja,&nbsp;når&nbsp;der&nbsp;ikke er en lagerordre</p><p>Nej, når der er en lagerordre</p> | <p>Ja, når der er en lagerordre, og når en indkøbsordre ikke er en del af en <i>last</i>. Men der skal bruges to menupunkter i mobilenheder, én til modtagelse (<i>Indkøbsordrevare til modtagelse</i>) og en anden med indstillingen <b>Brug eksisterende arbejde</b> aktiveret til at behandle læg på lager.</p><p>Nej, når der ikke er en lagerordre.</p> |
| Indkøbsordrelinje til modtagelse og læg på lager                        | <p>Ja, når der ikke er en lagerordre</p><p>Nej, når der er en lagerordre</p> | Nej |
| Modtagelse af returordre og placering på lager                               | Ja | Nej |
| Modtagelse af blandede id'er og placering på lager                        | <p>Ja, når der ikke er en lagerordre</p><p>Nej, når der er en lagerordre</p> | Nej |
| Modtagelse af varelast                                              | <p>Ja, når der ikke er en lagerordre</p><p>Nej, når der er en lagerordre</p> | Nej |
| Modtagelse af nummerplade og placering på lager                              | <p>Ja, når der ikke er en lagerordre</p><p>Nej, når der er en lagerordre</p> | Nej |
| Modtagelse af vare i flytteordre og placering på lager                        | Ja | Nej |
| Flytteordrelinje til modtagelse og placering på lager                        | Ja | Nej |
| Annullering af arbejde                                                | <p>Ja, når der ikke er en lagerordre</p><p>Nej, når der er en lagerordre</p> | <p>Ja, men indstillingen <b>Fjern registrering af modtagelse, når du annullerer arbejde</b> (på siden <b>Parametre til lokationsstyring</b>) understøttes ikke.</p> |
| Behandle indkøbsordre - produktkvittering                        | Ja | Nej |
| Oprette cross-docking som en del af modtagelsen                 | <p>Ja, når der ikke er en lagerordre</p><p>Nej, når der er en lagerordre</p> | Nej |

### <a name="warehouse-operations-and-exception-handing"></a>Lagerstedsoperationer og håndtering af undtagelser

I følgende tabel vises, hvilke funktioner til håndtering af lageroperationer og undtagelser der understøttes, og hvor de understøttes, når arbejdsbelastningen for lokationsstyring bruges i sky- og kantskalaenheder.

| Behandling                                            | Hub | WES-arbejdsbyrde på en skalaenhed |
|----------------------------------------------------|-----|------------------------------|
| Forespørge på nummerplade                              | Ja | Ja                          |
| Vareforespørgsel                                       | Ja | Ja                          |
| Lokationsforespørgsel                                   | Ja | Ja                          |
| Skift lagersted                                   | Ja | Ja                          |
| Bevægelse                                           | Nej  | Ja                          |
| Bevægelse efter skabelon                               | Nej  | Ja                          |
| Regulering (ind/ud)                                | Ja | Nej                           |
| Behandling af cyklusoptælling og optællingsafvigelser | Ja | Nej                           |
| Genudskrive etiket (udskrive nummerplade)             | Ja | Nej                           |
| Id-build                                | Ja | Nej                           |
| Id-pause                                | Ja | Nej                           |
| Chaufførens check-in                                    | Ja | Nej                           |
| Chaufførens check-ud                                   | Ja | Nej                           |
| Skifte batchdispositionskode                      | Ja | Nej                           |
| Vis oversigt over åbne opgaver                             | Ja | Nej                           |
| Konsolider id'er                         | Nej  | Nej                           |
| Fjern container fra gruppe                        | Nej  | Nej                           |
| Annuller arbejde                                        | Nej  | Nej                           |
| Behandle min./maks. genopfyldning                   | Nej  | Nej                           |
| Behandle allokeringsgenopfyldning                  | Nej  | Nej                           |

### <a name="production"></a>Produktion

Integration af lokationsstyring for produktionsscenarier understøttes ikke i øjeblikket som angivet i følgende tabel.

| Behandling | Hub | WES-arbejdsbyrde på en skalaenhed |
|---------|-----|------------------------------|
| <p>Alle de lokationsstyringsprocesser, der er relateret til produktion. Her er nogle eksempler:</p><li>Frigiv til lagersted</li><li>Produktionsbølgebehandling</li><li>Råvarepluk</li><li>Færdige varer, læg på lager</li><li>Samprodukt og biprodukt, læg på lager</li><li>Kanban-læg på lager</li><li>Kanban-pluk</li><li>Start produktionsordre</li><li>Produktionsspild</li><li>Sidste produktionspalle</li><li>Registrer materialeforbrug</li><li>Tøm kanban</li></ul> | Nej | Nej |

## <a name="maintaining-scale-units-for-wes"></a>Bevare skalaenheder for WES

Flere batchjob kører på både hubben og skalaenheder.

Under installationen af hub kan du vedligeholde batchjobbene manuelt. Du kan administrere følgende tre job i **Lokationsstyring \> Periodiske opgaver \> Backoffice-styring af arbejdsbyrder**:

- Opdateringshændelse for arbejdsstatusproces
- Kontrollér overførselshændelser ved udførelse af bølgestyring
- Registrer kvitteringer på kildeordre

På arbejdsbyrden i skalaenheder kan du administrere følgende to job i **Lokationsstyring \> Periodiske opgaver \> Styring af arbejdsbyrder**:

- Behandle bølgetabelposter
- Kontrollér overførselshændelser ved udførelse af bølgestyring


[!INCLUDE[footer-include](../../includes/footer-banner.md)]