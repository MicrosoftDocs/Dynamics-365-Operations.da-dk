---
title: Sky- og kantskaleringsenheder til arbejdsbyrder i warehouse management
description: Dette emne indeholder oplysninger om funktionen, der gør det muligt for skaleringsenheder at køre udvalgte processer fra din arbejdsbyrde i warehouse management.
author: perlynne
ms.date: 09/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, SysSecRolesEditUsers, SysWorkloadDuplicateRecord
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: c3f703e39e5e9d475dcb4f96dfb400a961ae2dcf
ms.sourcegitcommit: ecd4c148287892dcd45656f273401315adb2805e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/18/2021
ms.locfileid: "7500421"
---
# <a name="warehouse-management-workloads-for-cloud-and-edge-scale-units"></a>Arbejdsbelastninger i forbindelse med Warehouse Management for sky- og edge-skaleringsenheder

[!include [banner](../includes/banner.md)]

> [!WARNING]
> Ikke alle forretningsfunktioner i Warehouse Management understøttes fuldt ud på lagersteder, der kører en arbejdsbyrde på en skaleringsenhed. Sørg for kun at bruge de processer, som dette emne direkte beskriver som understøttede.

## <a name="warehouse-execution-on-scale-units"></a>Lagerudførelse på skaleringsenheder

Warehouse management-arbejdsbelastninger giver mulighed for, at der kan køres sky- og kantskalaenheder, så udvalgte processer køres fra funktionerne til Warehouse management.

## <a name="prerequisites"></a>Forudsætninger

Du skal have en Dynamics 365 Supply Chain Management-hub og en skaleringsenhed, der er implementeret med arbejdsbyrden for warehouse management. Du kan finde flere oplysninger om arkitekturen og installationsprocessen i [Skaler enheder i en distribueret hybridtopologi](cloud-edge-landing-page.md).

## <a name="how-the-warehouse-execution-workload-works-on-scale-units"></a>Sådan fungerer udførelse af lagerstedsarbejdsbyrde på skaleringsenheder

I forbindelse med processerne i arbejdsbyrden for Warehouse Management synkroniseres dataene mellem hubben og skaleringsenhederne.

En skaleringsenhed kan kun vedligeholde de data, som den ejer. Dataejerskabsbegrebet for skaleringsenheder medvirker til at forhindre multimasterkonflikter. Det er derfor vigtigt, at du forstår, hvilke procesdata der ejes af hubben, og hvilke som ejes af skaleringsenhederne.

Afhængigt af forretningsprocesserne kan samme datapost skifte ejer mellem hub og skaleringsenheder. Du kan se et eksempel på dette scenario i følgende afsnit.

> [!IMPORTANT]
> Nogle data kan oprettes både på hub'en og på vægtenheden. Det kan f.eks. være **id'er** og **batchnumre**. Der findes til den givne konflikthåndteringer i tilfælde af et scenario, hvor den samme entydige post både oprettes på hub'en og en vægtenhed under samme synkroniseringscyklus. Når det sker, mislykkes den næste synkronisering, og du skal gå til **Systemadministration > Forespørgsler > Forespørgsler > Dubletter af poster**, hvor du kan få vist og flette dataene.

## <a name="outbound-process-flow"></a>Udgående procesflow

Den udgående dataejerproces afhænger af, om du bruger belastningsplanlægningsprocessen. I alle tilfælde ejer hub *kildedokumenterne*, f.eks. salgsordrer og flytteordrer, ordrefordelingsprocessen og de relaterede ordretransaktionsdata. Men når du bruger belastningsplanlægningsprocessen, oprettes belastningerne i hub og ejes derfor i begyndelsen af hub. Som en del af processen for *frigivelse til lagersted* overføres ejerskabet af belastningsdataene til den tildefinerede implementering af vægtenheden, som vil blive ejer af den efterfølgende *behandling af forsendelser* (f.eks. arbejdsfordeling, opfyldningsarbejde og oprettelse af efterspørgselsarbejde). Lagerarbejdere kan derfor kun behandle udgående salgs- og flytteordrearbejde ved hjælp af en mobilapp til Warehouse Management, der er knyttet til den installation, der kører den specifikke arbejdsbyrde for vægtenheden.

Så snart den endelige arbejdsproces placerer lagerbeholdningen på en endelig forsendelseslokation (Baydoor), signalerer skaleringsenheden til hubben om at opdatere lagertransaktionerne for kildedokumentet til *Plukket*. Indtil denne proces køres og synkroniseres tilbage, reserveres den lagerbaserede arbejdsbyrde på lagerstedsniveau fysisk, og du kan med det samme behandle den udgående forsendelsesbekræftelse uden at vente på, at denne synkronisering fuldføres. Den efterfølgende salgs følgeseddel og fakturering eller flytteordreforsendelse for aflæsningen håndteres i hubben.

I følgende diagram vises udgående processer, og det angives, hvor de enkelte forretningsprocesser finder sted. (Vælg diagrammet for at markere det.)

[![Udgående behandlingsflow.](media/wes_outbound_warehouse_processes-small.png "Udgående behandlingsflow")](media/wes_outbound_warehouse_processes.png)

### <a name="outbound-processing-with-load-planning"></a>Udgående behandling med planlægning af last

Når du bruger proces til planlægning af belastninger, oprettes der belastninger og forsendelser i hub'et, og ejerskabet af dataene overføres til vægtenhederne som en del af processen for *frigivelse til lagersted*, som det er illustreret i nedenstående illustration.

![Udgående behandling med planlægning af last.](./media/wes_outbound_processing_with_load_planning.png "Udgående behandling med planlægning af last")

### <a name="outbound-processing-without-load-planning"></a>Udgående behandling uden planlægning af last

Når du ikke bruger belastningsplanlægningsprocessen, oprettes der forsendelser på vægtenhederne. Der oprettes også belastninger på vægtenhederne som en del af bølgeprocessen.

![Udgående behandling uden planlægning af last.](./media/wes_outbound_processing_without_load_planning.png "Udgående behandling uden planlægning af last")

## <a name="inbound-process-flow"></a>Indgående procesflow

Hubben ejer følgende data:

- Alle kildedokumenter, f.eks. indkøbsordrer og produktionsordrer
- Indgående lastbehandling
- Alle opdateringer af omkostning og økonomi

> [!NOTE]
> Det indgående indkøbsordreflow er grundlæggende forskelligt fra det udgående flow. Du kan operere det samme lagersted på enten skaleringsenheden eller hubben, afhængigt af om indkøbsordren er frigivet til lagerstedet. Når du har frigivet en ordre til lagerstedet, kan du kun arbejde med den pågældende ordre, når du er logget på skaleringsenheden.
>
> Hvis du bruger *Frigiv til lagersted* som proces, oprettes der [*lagerstedsordrer*](cloud-edge-warehouse-order.md), og ejerskabet af det tilknyttede modtagelsesflow tildeles til skaleringsenheden. Hubben kan ikke registrere indgående modtagelse.

Du skal logge på hubben for at bruge *Frigiv til lagersted*-processen. Mht købsordrebehandling skal du gå til en af følgende sider for at køre eller planlægge det:

- **Indkøb og forsyning > Indkøbsordrer > Alle indkøbsordrer > Lagersted > Handlinger > Frigiv til lagersted**.
- **Warehouse Management > Frigiv til lagersted > Automatisk frigivelse af indkøbsordrer**

Når du bruger **Automatisk frigivelse af indkøbsordrer**, kan du vælge bestemte indkøbsordrelinjer ud fra en forespørgsel. Det vil typisk være at konfigurere et tilbagevendende batchjob, der frigiver alle de bekræftede indkøbsordrelinjer, der forventes at ankomme næste dag.

Arbejderne kan køre modtagelsen ved hjælp af mobilappen Warehouse Management, der er tilknyttet skaleringsenheden. Dataene registreres derefter af skaleringsenheden og rapporteres i forhold til den indgående lagerordre. Oprettelsen og afviklingen af det efterfølgende læg på lager-arbejde vil også blive håndteret af skaleringsenheden.

Hvis du ikke bruger processen *frigivelse til lagersted*, og du derfor ikke bruger *lagerordrer*, kan hubben behandle lagermodtagelse og arbejde uafhængigt af skaleringsenheder.

![Indgående procesflow.](./media/wes-inbound-ga.png "Indgående procesflow")

Når en arbejder registrerer indgående registrering ved hjælp af en modtagelsesproces i Warehouse Management-mobilappen i forhold til vægtenheden, registreres der en tilgang i forhold til den tilknyttede lagerstedsordre, som gemmes på vægtenheden. Arbejdsbyrden for vægtens enhed signalerer derefter til hub'en, om de relaterede indkøbsordrelinjetransaktioner opdateres til *Registreret*. Når dette er gjort, kan du køre en indkøbsordreproduktkvittering på hubben.

I følgende diagram vises indgående processer, og det angives, hvor de enkelte forretningsprocesser finder sted. (Vælg diagrammet for at markere det.)

[![Indgående behandlingsflow](media/wes_inbound_warehouse_processes-small.png "Indgående behandlingsflow")](media/wes_inbound_warehouse_processes.png)

## <a name="supported-processes-and-roles"></a>Understøttede processer og roller

Ikke alle processer til Warehouse Management understøttes i en udførelse af lagerstedsarbejdsbyrde på en skaleringsenhed. Det anbefales derfor, at du tildeler roller, der stemmer overens med de funktioner, der er tilgængelige for de enkelte brugere.

For at lette denne proces inkluderes en eksempelrolle med navnet *Lagerchef på arbejdsbyrde* i demodataene i **Systemadministration \> Sikkerhed \> Sikkerhedskonfiguration**. Formålet med denne rolle er at gøre det muligt for lagercheferne at få adgang til udførelse af lagerstedsarbejdsbyrde på skaleringsenheden. Rollen giver adgang til de sider, der er relevante i forbindelse med en arbejdsbyrde, der har en skaleringsenhed som vært.

Brugerroller på en skaleringsenhed tildeles som en del af den første datasynkronisering fra hubben til skaleringsenheden.

Hvis du vil redigere de roller, der er tildelt til en bruger, skal du gå til **Systemadministration \> Sikkerhed \> Tildele brugere til roller**. Brugere, der kun fungerer som lagerchefer på skaleringsenheder, bør kun tildeles rollen *Lagerchef på arbejdsbyrde*. Denne fremgangsmåde sikrer, at de pågældende brugere kun har adgang til de understøttede funktioner. Fjern eventuelle andre roller, der er tildelt til disse brugere.

Brugere, der kun fungerer som lagerchefer på både hubben og skaleringsenheder, bør tildeles den eksisterende rolle *Lagerarbejder*. Bemærk, at denne rolle giver lagerarbejderne adgang til funktioner (f.eks. modtagelsesbehandling af flytteordre), der vises i brugergrænsefladen, men ikke understøttes i øjeblikket på skaleringsenheder.

### <a name="supported-warehouse-execution-processes"></a>Understøttede afviklingsprocesser for lagersteder

Følgende processer til lagerudførelse kan aktiveres for en udførelse af lagerstedsarbejdsbyrde på en skaleringsenhed:

- Udvalgte metoder til salgs- og flytteordrer (validering, oprettelse af last, fordeling, efterspørgselsopfyldning, containerisering, oprettelse af arbejde og udskrivning af label til bølge)

- Behandle arbejde med salgs- og flytteordrelagersteder ved hjælp af lagerstedsappen (herunder genopfyldningsarbejde)
- Forespørge på disponibel lagerbeholdning ved hjælp af lagerstedsappen
- Oprette og køre lagerbevægelser ved hjælp af lagerstedsappen
- Oprette og behandle procesoptællingsarbejde ved hjælp af lagerstedsappen
- Foretage lagerreguleringer ved hjælp af lagerstedsappen
- Registrere indkøbsordrer og udføre læg på lager-arbejde med lagerstedsappen

Følgende arbejdstyper kan oprettes på en vægtenhed og kan derfor behandles som en del af en udførelse af lagerstedsarbejdsbyrde:

- **Lagerbevægelser** - manuel bevægelse og bevægelse efter skabelonarbejde.
- **Cyklusoptælling** - herunder en afvigende godkendelses- og afvisningsproces som en del af optællingsoperationer.
- **Indkøbsordrer** - læg på lager-arbejde via en lagerstedsordre, når indkøbsordrer ikke er tilknyttet laster.
- **Salgsordrer** - simpelt pluk- og lastarbejde.
- **Overfør afgang** – Simpel pluk og indlæsning.
- **Genopfyldning** - uden råvarer til produktion.
- **Færdigvarer, der er blevet lagt på lager** – Efter produktionsprocessen for færdigmeldingen.
- **Med-produkt og under-produkt, der er lagt væk** – Efter produktionsprocessen er færdigmeldt.

Ingen anden behandling af kildedokumenter eller lagerstedsarbejde understøttes i øjeblikket på skaleringsenheder. I forbindelse med en udførelse af lagerstedsarbejdsbyrde på en skaleringsenhed kan du f.eks. ikke udføre en modtagelsesproces for overførselsordrer (overførselskvittering). Den skal i stedet behandles af hubforekomsten.

> [!NOTE]
> Menupunkter og knapper til mobilenheder til funktioner, der ikke understøttes, vises ikke i _mobilappen Warehouse Management_, når den er knyttet til en implementering af skaleringsenhed.
> 
> Når du kører en arbejdsbyrde i en skaleringsenhed, kan du ikke køre processer, der ikke understøttes, for det specifikke lagersted på hubben. Tabellerne senere i dette emne dokumenterer de understøttede egenskaber.
>
> Valgte arbejdstyper for lagersteder kan oprettes både på hubben og skaleringsenheder, men kan kun vedligeholdes af ejerhubben eller -skaleringsenheden (den installation, der har oprettet dataene).
>
> Selv når en bestemt proces understøttes i skaleringsenheden, skal du være opmærksom på, at alle nødvendige data muligvis ikke bliver synkroniseret fra hubben til skaleringsenheden eller fra skaleringsenheden til hubben, hvilket udgør en risiko for uventet systembehandling. Eksempler på dette scenario omfatter:
> 
> - Hvis du bruger en forespørgsel om lokationsvejledning, der tilknytter en datatabelpost, som kun findes i hubimplementeringen.
> - Hvis du bruger lokationsstatus og/eller lokationsmængder som lastfunktioner. Disse data synkroniseres ikke mellem implementeringerne og vil derfor kun fungere, når lokationslagerbeholdningen opdateres for en af installationerne.

Følgende warehouse management-funktioner understøttes ikke i øjeblikket i arbejdsbelastninger på skaleringsenheder:

- Indgående behandling af indkøbsordrelinjer, der er tilknyttet en last.
- Indgående behandling af indkøbsordrer for et projekt.
- Administration af landingsomkostninger, der bruger rejser, og sporing af varer undervejs.
- Indgående og udgående behandling af varer, der har aktive sporingsdimensioner **Ejer** og/eller **Serienummer**.
- Behandling af lager, der har en blokeringsstatusværdi.
- Ændring af lagerstatus under en hvilken som helst arbejdsbevægelsesproces.
- Ordrebekræftede fleksible reservationer for dimension på lagerstedsniveau.
- Brug af funktionen *Lokationsstatus for lagersted* (dataene synkroniseres ikke mellem implementeringerne).
- Brug af funktionen *Placering af lokations-id*.
- Brug af *Produktfiltre* og *Produktfiltergrupper*, herunder indstillingen **Antal dage til at sammensætte batches**.
- Integration med kvalitetsstyring.
- Behandling med fastvægtvarer.
- Behandling med varer, der kun er aktiveret til transportstyring (TMS).
- Behandling med negativ disponibel lagerbeholdning.
- Behandling af lagerstedsarbejde med forsendelsesnotaer.
- Behandling af lagerstedsarbejde med materialehåndtering/warehouse automation.
- Brug af billede af produktmasterdata (f.eks. på mobilappen Warehouse Management).

> [!WARNING]
> Nogle af lagerstedsfunktionerne er ikke tilgængelige for lagersteder, der kører arbejdsbyrderne for Warehouse Management på en skaleringsenhed, og de understøttes heller ikke i hubben eller i arbejdsbyrden for skaleringsenheden.
> 
> Andre egenskaber kan behandles på begge, men vil kræve nøje brug i visse scenarier, f.eks. når lagerbeholdning opdateres for det samme lagersted på både hubben og skaleringsenheden på grund af den asynkrone dataopdateringsproces.
> 
> Specifikke funktioner (som f.eks. *blokringsarbejde*), der understøttes på både hubben og skaleringsenheder, vil kun blive understøttet for ejeren af dataene.

### <a name="outbound-supported-only-for-sales-and-transfer-orders"></a>Udgående (kun understøttet for salgsordrer og flytteordrer)

I følgende tabel vises, hvilke udgående funktioner der understøttes, og hvor de understøttes, når arbejdsbelastningen for Warehouse Management bruges i sky- og kantskaleringsenheder.

| Behandling                                                      | Hub | Udførelse af lagerstedsarbejdsbyrde på skaleringsenheder |
|--------------------------------------------------------------|-----|------------------------------|
| Behandling af kildedokument                                   | Ja | Ingen |
| Last- og transportstyringsbehandling                | Ja, men kun processerne til belastningsplanlægning. Behandlingen af transportstyring understøttes ikke  | Ingen |
| Modtagelse af varer undervejs og landingsomkostninger                                         | Ja | Ingen |
| Frigiv til lagersted                                         | Ja | Ingen |
| Planlagt direkte levering                                        | Ingen  | Ingen |
| Konsolidering af forsendelse                                       | Ja, når du bruger belastningsplanlægning | Ja |
| Behandling af forsendelsesbølge                                     | Ingen  |Ja, undtagen **Indlæs bygning og sortering** |
| Vedligeholde forsendelser for bølge                                  | Ingen  | Ja|
| Lagerstedsbehandling (inkl. udskrivning af nummerplade)        | Ingen  | Ja, men kun for ovennævnte understøttede egenskaber |
| Klyngepluk                                              | Ingen  | Ja|
| Manuel behandling af emballage, herunder arbejdet "Plukning af pakket container" | Ingen <P>En del af behandlingen kan udføres efter den første plukproces, der håndteres af en skaleringsenhed, men det frarådes på grund af følgende blokerede operationer.</p>  | Ingen |
| Fjern container fra gruppe                                  | Ingen  | Ingen |
| Behandling af udgående sortering                                  | Ingen  | Ingen |
| Udskrivning af lastrelaterede dokumenter                           | Ja | Ja|
| Fragtseddel og ASN-generering                            | Ingen  | Ja|
| Forsendelsesbekræftelse                                             | Ingen  | Ja|
| Forsendelsesbekræftelse med "Bekræft og flyt"            | Ingen  | Ingen |
| Behandling af følgesedler og fakturering                        | Ja | Ingen |
| Kort pluk (salgs- og flytteordrer)                    | Ingen  | Ja, uden at fjerne reservationer for kildedokumenter|
| Overpluk (salgs- og flytteordrer)                     | Ingen  | Ja|
| Ændring af arbejdssteder (salgs- og flytteordrer)         | Ingen  | Ja|
| Fuldføre arbejde (salgs- og flytteordrer)                    | Ingen  | Ja|
| Udskrive arbejdsordrerapport                                            | Ja | Ja|
| Bølgelabel                                                   | Ingen  | Ja|
| Arbejdsopdeling                                                   | Ingen  | Ja|
| Arbejdsbehandling – Styres af "Lastning af transport"            | Ingen  | Ingen |
| Reducer det antal, der er plukket                                       | Ingen  | Ingen |
| Tilbagefør arbejde                                                 | Ingen  | Ingen |
| Tilbagefør forsendelsesbekræftelse                                | Ingen  | Ja|

### <a name="inbound"></a>Indgående

I følgende tabel vises, hvilke indgående funktioner der understøttes, og hvor de understøttes, når arbejdsbelastningen for Warehouse Management bruges i sky- og kantskaleringsenheder.

| Behandling                                                          | Hub | Udførelse af lagerstedsarbejdsbyrde på skaleringsenheder<BR>*(Varer, der er markeret "Ja", gælder kun for lagerstedsordrer)* |
|------------------------------------------------------------------|-----|----------------------------------------------------------------------------------|
| Behandling&nbsp;af&nbsp;kildedokument                             | Ja | Ingen |
| Last- og transportstyringsbehandling                    | Ja | Ingen |
| Bekræftelse af indgående forsendelse                                    | Ja | Ingen |
| Frigivelse af indkøbsordre til lagersted (behandling af lagerstedsordre) | Ja | Ingen |
| Annullering af ordrelinjer på lagersted<p>Bemærk, at dette kun understøttes, når der ikke er sket nogen registrering for linjen</p> | Ja | Ingen |
| Indkøbsordrevare til modtagelse og læg på lager                       | <p>Ja,&nbsp;når&nbsp;der&nbsp;ikke er en lagerordre</p><p>Nej, når der er en lagerordre</p> | <p>Ja, når en indkøbsordre ikke er del af en <i>last</i></p> |
| Indkøbsordrelinje til modtagelse og læg på lager                       | <p>Ja, når der ikke er en lagerordre</p><p>Nej, når der er en lagerordre</p> | <p>Ja, når en indkøbsordre ikke er del af en <i>last</i></p></p> |
| Modtagelse af returordre og placering på lager                              | Ja | Ingen |
| Modtagelse af blandede id'er og placering på lager                       | <p>Ja, når der ikke er en lagerordre</p><p>Nej, når der er en lagerordre</p> | Ja |
| Modtagelse af varelast                                              | <p>Ja, når der ikke er en lagerordre</p><p>Nej, når der er en lagerordre</p> | Nej |
| Modtagelse af nummerplade og placering på lager                             | <p>Ja, når der ikke er en lagerordre</p><p>Nej, når der er en lagerordre</p> | Nej |
| Modtagelse af vare i flytteordre og placering på lager                       | Ja | Ingen |
| Flytteordrelinje til modtagelse og placering på lager                       | Ja | Ingen |
| Annuller arbejde (indgående)                                            | <p>Ja, når der ikke er en lagerordre</p><p>Nej, når der er en lagerordre</p> | <p>Ja, men kun når indstillingen <b>Fjern registrering af modtagelse, når du annullerer arbejde</b> (på siden <b>Parametre til warehouse management</b>) er ryddet</p> |
| Behandle indkøbsordre - produktkvittering                        | Ja | Ingen |
| Indkøbsordre, der modtages med underlevering                      | <p>Ja, når der ikke er en lagerordre</p><p>Nej, når der er en lagerordre</p> | Ja, men kun ved at foretage en annulleringsanmodning fra hubben |
| Indkøbsordre, der modtages med overlevering                       | <p>Ja, når der ikke er en lagerordre</p><p>Nej, når der er en lagerordre</p> | Ja  |
| Modtagelse med oprettelse af *Cross-docking*-arbejde                 | <p>Ja, når der ikke er en lagerordre</p><p>Nej, når der er en lagerordre</p> | Ingen |
| Modtagelse med oprettelse af *Kvalitetsordre*-arbejde                  | <p>Ja, når der ikke er en lagerordre</p><p>Nej, når der er en lagerordre</p> | Ingen |
| Modtagelse med oprettelse af *Kvalitetsvareprøve*-arbejde          | <p>Ja, når der ikke er en lagerordre</p><p>Nej, når der er en lagerordre</p> | Ingen |
| Modtagelse med oprettelse af *Kvalitet i kvalitetskontrol*-arbejde       | <p>Ja, når der ikke er en lagerordre</p><p>Nej, når der er en lagerordre</p> | Ingen |
| Modtagelse med oprettelse af kvalitetsordre                            | <p>Ja, når der ikke er en lagerordre</p><p>Nej, når der er en lagerordre</p> | Ingen |
| Arbejdsbehandling – Styres af *Læg på lager-klynge*                 | Ja | Ingen |
| Arbejdsbehandling med *Kort pluk*                               | Ja | Ingen |
| Indlæsning af nummerplade                                           | Ja | Ja |

### <a name="warehouse-operations-and-exception-handing"></a>Lagerstedsoperationer og håndtering af undtagelser

I følgende tabel vises, hvilke funktioner til håndtering af lageroperationer og undtagelser der understøttes, og hvor de understøttes, når arbejdsbelastningen for Warehouse Management bruges i sky- og kantskaleringsenheder.

| Behandling                                            | Hub | Udførelse af lagerstedsarbejdsbyrde på skaleringsenheder |
|----------------------------------------------------|-----|------------------------------|
| Forespørge på nummerplade                              | Ja | Ja                          |
| Vareforespørgsel                                       | Ja | Ja                          |
| Lokationsforespørgsel                                   | Ja | Ja                          |
| Skift lagersted                                   | Ja | Ja                          |
| Bevægelse                                           | Ja | Ja                          |
| Bevægelse efter skabelon                               | Ja | Ja                          |
| Overførsel af lagersted                                 | Ja | Ingen                           |
| Oprette flytteordre fra lagerstedsappen           | Ja | Ingen                           |
| Regulering (ind/ud)                                | Ja | Ja, men ikke for det udreguleringsscenarie, hvor lagerreservationen skal fjernes ved hjælp af indstillingen **Fjern reservationer** for lagerreguleringstyperne</p>                           |
| Ændring af lagerstatus                            | Ja | Ingen                           |
| Behandling af cyklusoptælling og optællingsafvigelser | Ja | Ja                           |
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
| Behandle allokeringsgenopfyldning                  | Ja  | Ja<p>Bemærk, at opsætningen skal udføres på skaleringsenheden</p>                           |
| Blokere og fjerne blokering af arbejde                             | Ja | Ja                          |
| Skift bruger                                        | Ja | Ja                          |
| Skift arbejdspulje på arbejde                           | Ja | Ja                          |
| Annuller arbejde                                        | Ja | Ja                          |

### <a name="production"></a>Produktion

I følgende tabel vises en oversigt over produktionsscenarier for warehouse management, der (ikke) understøttes i øjeblikket i arbejdsbelastninger på skaleringsenheder.

| Behandling | Hub | Udførelse af lagerstedsarbejdsbyrde på skaleringsenheder |
|---------|-----|------------------------------|
| Færdigmelde og lægge færdigvarer på lager | Ja | Ja |
| Samprodukt og biprodukt, læg på lager | Ja | Ja |
| <p>Alle andre warehouse management-processer, der er relateret til produktion, omfatter:</p><li>Frigiv til lagersted</li><li>Produktionsbølgebehandling</li><li>Råvarepluk</li><li>Kanban-læg på lager</li><li>Kanban-pluk</li><li>Start produktionsordre</li><li>Produktionsspild</li><li>Sidste produktionspalle</li><li>Registrer materialeforbrug</li><li>Tøm kanban</li></ul> | Ja | Ingen |
| Genopfyldning af råvarer | Ingen | Ingen |

## <a name="maintaining-scale-units-for-warehouse-execution"></a>Vedligeholde skaleringsenheder til lagerstedsudførelse

Flere batchjob kører på både hubben og skaleringsenheder.

Under installationen af hub kan du vedligeholde batchjobbene manuelt. Du kan administrere følgende batchjob i **Warehouse Management \> Periodiske opgaver \> Backoffice-styring af arbejdsbyrder**:

- Skaleringsenhed til meddelelsesprocessors hub
- Registrer kvitteringer på kildeordre
- Fuldfør lagerstedsordrer

På arbejdsbyrden i skaleringsenheder kan du administrere følgende batchjob i **Warehouse Management \> Periodiske opgaver \> Styring af arbejdsbyrder**:

- Behandle bølgetabelposter
- Meddelelsesprocessor for lagerstedshub til skaleringsenhed
- Foretag behandling af anmodninger om opdatering af antal for lagerstedsordrelinjer

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
