---
title: Forbedre planlægningsprogrammets ydeevne
description: Denne artikel giver oplysninger om planlægningsprogrammet, og hvordan ydeevnen kan forbedres.
author: t-benebo
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: ''
ms.author: benebotg
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: ''
ms.openlocfilehash: f5ece3672bba352e02808248c91366539423d682
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854291"
---
# <a name="improve-scheduling-engine-performance"></a>Forbedre planlægningsprogrammets ydeevne

[!include [banner](../includes/banner.md)]

Ressourceplanlægningsprogrammet bruges ved planlægning af ruter for planlagte og frigivne produktionsordrer. Programmet blev oprindeligt frigivet som en del af Dynamics AX 2012 og har gennemgået flere forbedringer siden frigivelsen.

[Problemet med jobbet til produktionsplanlægning](https://en.wikipedia.org/wiki/Job_shop_scheduling) er et særdeles komplekst kombinationsproblem, hvor løsningstiden vokser eksponentielt med antallet af beslutningsvariabler. Ofte konfigurerer kunder produktionsruter og relaterede data på en måde, der resulterer i et planlægningsproblem, der ikke kan løses i et rimeligt tidsrum selv på den mest moderne hardware. Denne artikel vil hjælpe dig med at forstå planlægningsprogrammet, og hvordan en bestemt opsætning kan have indflydelse på ydeevnen.

Når det drejer sig om at forbedre planlægningens ydeevne, anbefaler de generelle retningslinjer at reducere kompleksiteten af det problem, du skal løse. Nogle af de vigtigste faktorer, der kan påvirke ydeevnen, omfatter:

- Ruter med mange handlinger
- Ruter med parallelle handlinger
- Operationer med et antal ressourcer, der er større end én
- Operationer med mange relevante ressourcer
- Brug af hårde links
- Brug af kapacitetsbegrænsning
- Antallet af forskellige kalendere, der bruges
- Antallet af arbejdstidsrubrikker pr. dag i kalenderen
- Rutens samlede varighed
- Kørsel af flere planlægningsprogrammer parallelt

## <a name="overview-of-basic-scheduling-flow"></a>Oversigt over grundlæggende planlægningsflow

For at forstå, hvordan en bestemt opsætning kan påvirke ydeevnen, er det vigtigt at forstå noget om, hvordan processen flyder, både inde i programmet og i X++-kode, der omgiver det.

Den grundlæggende proces til planlægning af en ordre består af tre hovedtrin:

- **Indlæsning af data** – Her omdannes X++-datamodellerne til programmets interne datamodel i form af job og begrænsninger.
- **Planlægning** – Dette er den overordnede kilde til planlægning, der behandler de angivne modeller og begrænsninger, og som genererer et resultat. Under denne proces vil programmet anmode om oplysninger om arbejdstiden og eksisterende kapacitetsreservationer fra X++ efter behov.
- **Gem data** – Programresultatet i form af jobkapacitetsreservationspladser behandles af X++-kode for at gemme kapacitetsreservationer og opdatere start- og sluttidspunkter for jobbene/operationen/ordren.

## <a name="load-data-into-the-engine"></a>Indlæse data i programmet

Planlægningsprogrammet har en mere abstrakt datamodel end Supply Chain Management-databasen, fordi det er bygget som et generisk program, der kan håndtere forskellige datakilder. Koncepterne for rute, sekundære operationer og kørselstid skal "oversættes" til det generiske job og den begrænsningsmodel, som programmet viser. Logikken for opbygning af modellen har en stor mængde forretningslogik og varierer alt efter kildedataene. Den ansvarlige X++-klasse er `WrkCtrScheduler` og har afledte klasser for produktionsordreforslag, frigivne produktionsordrer og projektprognoser.

Overvej f.eks. en rute, der vises i følgende tabel og billede, som ser relativt enkel ud.

| Opr. Nej | Prioritet | Opstillingstid | Procestid | Køventetid efter | Antal ressourcer | Næste |
| --- | --- | --- | --- | --- | --- | --- |
| 10 | Primær | 1.00 | 2.00 | | 1 | 20 |
| 10 | Sekundær&nbsp;1 | | | | 1 | 20 |
| 20 | Primær | | 3.00 | 1.00 | 3 | 0 |

![Eksempel på rutediagram.](media/scheduling-engine-route.png "Eksempel på rutediagram")

Når du sender dette til programmet, opdeles det i otte job som vist i følgende illustration (vælg billedet for at forstørre det).

[![Planlægning af programjob](media/scheduling-engine-jobs.png "Planlægning af programjob.")](media/scheduling-engine-jobs-large.png)

Standardforbindelsen mellem to job er `FinishStart`, hvilket betyder, at sluttidspunktet for ét job skal ligge før starttidspunktet for et andet job. Da opsætningen skal udføres af den samme ressource, der senere udfører processen, vil der være `OnSameResource`-begrænsninger mellem dem. Mellem jobbene for primær og sekundær operation for 10 er der `StartStart`- og `FinishFinish`-links, hvilket betyder, at jobbene både skal starte og slutte på samme tid, og der er `NotOnSameResource`-begrænsninger, som vil forhindre den samme ressource til primær og sekundær.

Ved operation 20, hvor antallet af ressourcer er angivet til 3, er procesjobbet opdelt i tre forskellige job, hvor alle job skal køres på nøjagtigt samme tidspunkt.
I dette tilfælde er rutegruppen konfigureret til ikke at reservere kapacitet for kø efter tider, hvilket betyder, at der kun er ét job for køen efter.

Planlægningsprogrammet forstår kun begreberne for job og har intet begreb om operationer. Det betyder, at når operationsplanlægningen udføres, opdeles operationerne også i job, selvom de ikke bevares i databasen.

For hvert job definerer vi også jobkapacitetskravet (antal påkrævede sekunder). Afhængigt af, hvordan ressourcekravene er defineret, kan vi også for hvert job sende en liste over alle de potentielle relevante ressourcer, som jobbet kunne køre på, og hvad kapacitetskravet er for den pågældende ressource. Selvom listen over relevante ressourcer sendes, når modellen bygges, skal programmet stadig sikre, at ressourcetildelingen er gyldig for hele varigheden af jobbet.

## <a name="scheduling-engine-internals"></a>Planlægning af programmets indre

### <a name="scheduling-engine-interface"></a>Planlægning af programmets grænseflade

Hvis du vil have en ide om, hvordan programmets indre fungerer, er det bedst at se på de funktioner, det viser eksternt. I X++ er hovedgrænsefladen `WrkCtrSchedulerEngineInterface`. Den indeholder de metoder, der er beskrevet i følgende underafsnit.

#### <a name="general-engine"></a>Generisk program

| **metode** | **Formål** |
| --- | --- |
| `run` | Planlægger alle indlæste job og returnerer fejlkoden. |
| `getJobSchedulingSequenceResult` | Henter planlægningsresultatet og det første fejljob for den sekvens, der identificeres af et bestemt job. |
| `validateJobCapacityReservations` | Validerer kapacitetsreservationerne for alle job, der er gemt af programmet. |
| `setReservationsTimeStamp` | Sender et tidsstempel til programmet, der er angivet på alle nye kapacitetsreservationer for de planlagte job i programmets cache. |
| `addPropertyToGroupAggregation` | Føjer et egenskabspræfiks til det sæt egenskaber, der bruges, når kapaciteten samles. |
| `addResource` | Føjer en ressource til planlægningsprogrammets ressourcepulje. |
| `addResourceGroup` | Føjer en ressourcegruppe til planlægningsprogrammets ressourcegruppepulje. |
| `addResourceGroupMembership` | Føjer en ressource som medlem til en ressourcegruppe. |
| `addOptimizationGoal` | Tilføjer et mål for planlægningsoptimering (varighed eller prioritet). |

#### <a name="individual-jobs"></a>Individuelle job

| **metode** | **Formål** |
| --- | --- |
| `addJobInfo` | Tilføjer en post med joboplysninger, der oplyser programmet om et job, der skal planlægges. |
| `addConstraintJobEndsAt` | Tilføjer en begrænsning, hvor et job skal slutte på en bestemt dato og et bestemt tidspunkt. |
| `addConstraintJobStartsAt` | Tilføjer en begrænsning, hvor et job skal starte på en bestemt dato og et bestemt tidspunkt. |
| `addConstraintMaxJobDays` | Definerer en begrænsning, hvor et job kan spænde over et angivet maksimalt antal dage. |
| `addConstraintResourceRequirement` | Tilføjer en begrænsning, hvor jobbet skal planlægges på en bestemt ressource. |
| `addJobBindPriority` | Tilføjer en prioritet af jobbinding for et par (job, begrænsningsniveau). En højere prioritetsværdi betyder, at jobvariablerne bindes tidligere. Jobbet behandles før job med lavere prioritetsværdi i samme sekvens. |
| `addJobCapacity` | Tilføjer kapacitetsbelastningsoplysninger for et job (som den påkrævede jobkørselstid) uafhængigt af, hvilken ressource jobbet kører på. |
| `addJobResourceCapacity` | Føjer en ressource til det sæt ressourcer, der kan bruges til at udføre et job, og angiver den kapacitet, der kræves, når der køres på den pågældende ressource. |
| `addJobGoal` | Tilføjer oplysninger om jobmål for et specifikt begrænsningsniveau (tidligste sluttidspunkt eller seneste starttidspunkt). |
| `addJobResourcePriority` | Tilføjer den prioritet, der skal bruges, når et job planlægges på en ressource. |
| `addJobResourceRuntime` | Angiver en jobtid, der er afhængig af den ressource, som jobbet planlægges på. |
| `addJobRuntime` | Angiver en jobtid, der er uafhængig af den ressource, som jobbet planlægges på. |
| `scheduleJobOnResourceGroup` | Markerer et job til planlægning på ressourcegruppeniveau. |
| `setJobResourcePreemptionAllowed` | Angiver, om jobforkøbsret er tilladt for et job på en ressource (hvis programmet har tilladelse til at planlægge jobbet i ikke-sammenhængende kapacitetspladser). |
| `setRequiredNumberOfResources` | Angiver det antal ressourcer, der kræves for at planlægge et job (kun til operationsplanlægning). |

#### <a name="constraints-between-jobs"></a>Begrænsninger mellem job

| **metode** | **Formål** |
| --- | --- |
| `addJobLink` | Tilføjer et link (som f.eks. slut\>start) mellem to job. |
| `addConstraintEndsDelayed` | Definerer den begrænsning, at et job ikke må slutte, før et andet job afsluttes plus en vis forsinkelsestid. |
| `addConstraintJobListWorkingTimeIntersect` | Tilføjer en begrænsning, hvor de kapacitetspladser, der er reserveret til jobbene, skal være på skæringsarbejdstider for de to ressourcer, der bruges af jobbene. |
| `addConstraintJobOverlap` | Tilføj en begrænsning, der definerer, hvordan jobsekvens beregnes, når et bestemt antal af en vare kan flyttes mellem to ressourcer, mens den første ressource stadig ikke er færdigbehandlet, så den anden ressource kan starte behandlingen. |
| `addConstraintNotOnSameResource` | Tilføjer en begrænsning for, at to job ikke må planlægges på samme ressource. |
| `addConstraintOnSameResource` | Tilføjer en begrænsning for, at to job skal bruge samme ressource. |
| `addJobSameReservations` | Tilføjer en begrænsning, hvor et job skal have kapacitetsreservationer i samme tidsrum som det primære job. |
| `setPrimaryParallelJob` | Tilføjer oplysninger om det primære job i et sæt parallelle job. |

### <a name="solver"></a>Problemløser

Selve programmet er egentligt en specialiseret begrænsningsløser med brugerdefineret heuristisk tilføjelse. Problemløseren er baseret på to hovedelementer: variabler og begrænsninger.

#### <a name="variable"></a>Variabelt

En variabel repræsenterer et domæne af mulige værdier. Planlægningsprogrammet har to typer variabler:

- **DateTime-variabel** - Har et domæne for alle datoer og klokkeslæt, og domænet kan begrænses ved at flytte den nedre og øvre grænse for tidspunktet for variablen tættere på hinanden.
- **Ressourcevariabel** – Har et domæne med relevante ressourcer, og domænet kan begrænses ved at fjerne ressourcer fra listen.

#### <a name="constraint"></a>Begrænsning

En begrænsning fungerer på variabler ved at begrænse deres domæner, men den afhænger også af variabler, så den aktiveres, når variabler ændres. Processen med "begrænsningsudbredelse" er, når en begrænsning udfører sin hovedfunktion og rapporterer tilbage til hovedlogikken, hvis den lykkes.

En variabel betragtes som bundet, når den ikke kan begrænses yderligere, hvilket for en DateTime-variabel betyder, at den øvre og nedre grænse er den samme og for ressourcevariablen, at den kun har en enkelt anvendelig ressource. Når alle variabler er bundet, findes der en løsning.

### <a name="constraint-levels"></a>Begrænsningsniveauer

Når der udføres planlægning som en del af materialebehovsplanlægning (MRP), planlægges ordrerne bagud fra behovsdatoen. Men hvis det ikke er muligt at finde en tidsplan, der starter i dag eller senere og slutter før behovsdatoen, ændres planlægningsretningen til fremad fra i dag.

Denne hovedforretningsregel håndteres ved at organisere begrænsningerne i niveauer. Hvis der ikke findes en løsning, når du bruger begrænsningerne på det højeste niveau, droppes alle begrænsningerne på det pågældende niveau, og det lavere niveau afprøves. I praksis betyder det, at i forbindelse med planlægning bagud vil modellen indeholde et niveau 1 med jobmål for det seneste givne starttidspunkt og en maksimal sluttid som begrænsning (behovsdatoen), og et niveau 0 med jobmål for det tidligste sluttidspunkt og en given minimumstarttid af i dag.

### <a name="algorithm"></a>Algoritme

Hovedtrin i programalgoritmen er:

1. Find sekvenser (jobkæder), der kan løses særskilt.
1. Prøv at finde en indledende løsning på sekvensen for det højeste begrænsningsniveau.
    1. Sortér job i rækkefølge baseret på jobmål og -prioriteter, så der findes et startjob.
    1. Gentag jobbene i følgende rækkefølge:
        1. Find alle de begrænsninger, der skal udbredes, og kør udbredelse.
        1. Hvis alle variabler for jobbet er bundet, er der fundet en løsning til det pågældende job.
        1. Hvis en af variablerne ikke kan bindes, uden at begrænsningerne overtrædes, skal du annullere variabelbindingen, prøve en anden værdi i domænet (for ressourcevariablen) og køre begrænsningsudbredelsen igen.
1. Hvis der ikke blev fundet en løsning, fjernes alle begrænsninger på det aktuelle begrænsningsniveau, mens begrænsningsniveauet sænkes (hvis der er nogle lavere tilgængelige niveauer), og søgning efter løsninger blev forsøgt igen med det nye sæt begrænsninger.
1. Hvis der findes en passende løsning, startes optimeringsfasen, som vil forsøge at finde en bedre løsning, indtil timeout for optimering opstår, eller alle ressourcekombinationer er opbrugt.

Begrænsningsløseren er ikke klar over de specifikke oplysninger om planlægningsalgoritmen. Den har en definition og en kombination af de forskellige begrænsninger, som forekommer.

### <a name="determining-working-times"></a>Fastlægge arbejdstider

En stor del af begrænsningerne (interne) i programmet styrer en ressources arbejdstid og kapacitet. Opgaven er grundlæggende at føre arbejdstidsrummet for en ressource fra et givent sted i en given retning og finde et langt nok interval, hvor den krævede jobkapacitet (tid) kan være.

Hvis du vil gøre det, skal programmet kende en ressources arbejdstider. Modsat hovedmodeldata bliver arbejdstiderne *gradvist indlæst*, hvilket betyder, at de indlæses i programmet efter behov. Årsagen til denne metode er, at der ofte er arbejdstider i Supply Chain Management for en kalender i en meget lang periode, og der findes typisk mange kalendere, så dataene bliver meget store at indlæse på forhånd.

Der anmodes om kalenderoplysninger af programmet i segmenter ved at kalde X++-klassemetoden `WrkCtrSchedulingInteropDataProvider.getWorkingTimes`. Anmodningen gælder for et bestemt kalender-id i et bestemt tidsinterval. Afhængigt af servercachens tilstand i Supply Chain Management kan hver enkelt af disse anmodninger ende med flere databasekald, hvilket tager lang tid (i forhold til den rene beregningstid). Hvis kalenderen desuden indeholder meget komplekse arbejdstidsdefinitioner med mange arbejdstidsintervaller pr. dag, giver det en længere indlæsningstid.

Når der indlæses arbejdstidsdata i planlægningsprogrammet, bevares de i dens interne cache for den specifikke kalender, hvilket betyder, at hvis andre job eller ressourcer bruger samme kalender, kan de næste opslag hurtigt udføres fra hukommelsen. En almindelig årsag til dårlig ydeevne er, hvis der bruges et separat kalender-id til hver ressource, da der så kræves data for hver kalender, selvom indholdet i kalenderne kan være ens.

### <a name="finite-capacity"></a>Kapacitetsbegrænsning

Når der bruges kapacitetsbegrænsning, vil arbejdstiden fra kalenderen blive opdelt og reduceret ud fra de eksisterende kapacitetsreservationer. Disse reservationer hentes også via samme `WrkCtrSchedulingInteropDataProvider`-klasse som kalenderne, men i stedet bruges metoden `getCapacityReservations`. Når der planlægges under varedisponering, betragtes reservationerne for den specifikke behovsplan, og hvis den er aktiveret på siden **Varedisponeringsparametre**, medtages reservationer fra autoriserede produktionsordrer også. Når en produktionsordre planlægges, kan du også vælge at medtage reservationer fra eksisterende ordreforslag, selvom dette ikke er så almindeligt som den anden metode.

Hvis du bruger kapacitetsbegrænsning, kan planlægningen tage længere tid af flere årsager:

- Hentning af kapacitetsoplysninger fra databasen er en langsom operation, og cachelagringen af kapacitetsoplysninger på serversiden er typisk ikke så god som for arbejdstider, fordi de ikke deles mellem ressourcer som f.eks. kalendere.
- Antallet af arbejdstider, der skal håndteres, øges på grund af opdelingerne, og tidsintervaller for en længere tidsperiode skal normalt undersøges, før der kan findes en løsning.
- Når planlægningen er fuldført, skal der udføres en kontrol af, om der er uoverensstemmende reservationer (se afsnittet "Kørsel af flere planlægningsprogrammer parallelt" for at få flere oplysninger).

### <a name="examining-the-resource-combinations"></a>Undersøgelse af ressourcekombinationerne

Hvis jobrækkefølgen kun indeholder standardlinks `FinishStart`, hvilket betyder, at den udgør en simpel kæde uden forgreninger, kan der opnås et optimalt resultat (set fra den enkelte ordres side, ikke på tværs af ordrer) ved at finde den bedste løsning til det første job og derefter finde den bedste løsning til det næste job. Den bedste løsning til et job betyder, at du finder den ressource, der kan hente fra- og til-datoen for det job, der er tættest på jobmålet (i forlæns planlægning betyder det at få slutdatoen i jobbet så tidligt som muligt), samtidig med at begrænsningerne overholdes.

Når der er parallelle job, kan søgning efter en løsning omfatte forskellige kombinationer af ressourcer. Antallet af mulige ressourcekombinationer er produktet af antallet af relevante ressourcer for de forbundne parallelle job. Specielt når du planlægger en ordre baglæns fra en behovsdato, kan det tage ret lang tid for logikken at indse, at der ikke er nogen løsning på det problem, der vil kunne opfylde de parallelle job før dags dato, da det vil være nødvendigt at kontrollere alle kombinationerne, fordi der kan være ressourcer med en højere effektivitet eller en anden kalender, der kan give et resultat. Det betyder, at hvis der ikke er angivet timeoutgrænse, køres den i lang tid, før retningen ændres til fremad.

Denne kombinationslogik betyder også, at hvis du tilføjer mere relevante ressourcer, kan programmet blive kørt langsommere. Hvis der opstår ydeevneproblemer, når der er parallelle operationer og planlægning med ubegrænset kapacitet, kan den rettes delvist ved at få rutedesignere til at træffe en beslutning om, hvilken ressource der skal bruges, og derefter tildele ressourcen direkte til operationen (da programmet i de fleste tilfælde altid vil ende med at vælge den samme ressource, så slutresultatet vil være det samme).

### <a name="hard-links"></a>Hårde links

Hvis du angiver linktypen mellem to job til hård, sikrer du, at der ikke er tidskløfter mellem afslutningen på ét job og begyndelsen af det næste. Dette kan være meget nyttigt i scenarier, hvor metal f.eks. opvarmes i ét job og derefter behandles i det næste job, hvor det ikke er ønskeligt at få metal afkølet i mellemtiden.

Hvis ruten udgør en simpel kæde uden forgreninger, kan der opnås et resultat med bløde standardlinks og forlæns planlægning ved at finde en løsning til det første job, der opfylder sine egne begrænsninger, og derefter gå videre igennem kæden og overføre sluttidspunktet fra det forrige job til det næste job. Hvis det aktuelle job ikke kan finde en kapacitet, vil starttidspunktet for det blive flyttet yderligere uden risiko for, at de tidligere job skaber pauser mellem jobbene. Men med hårde links (især i forbindelse med kapacitetsbegrænsning) for det samme scenarie er det faktum, at ét job senere i kæden ikke kan finde kapacitet, hvilket vil sige, at alle tidligere planlagte job skal "trækkes" med ét efter ét og derved omplanlægges et antal gange. Især i scenarier med høj belastning af flere ressourcer kan hårde links forårsage en kædereaktion, hvor jobbene påvirker hinanden, og der skal udføres et antal gentagelser, før resultatet bliver stabiliseret ind i en gennemførlig plan.

## <a name="running-scheduling-engines-in-parallel"></a>Kørsel af planlægningsprogrammer parallelt

Når der udføres planlægning som del af en varedisponeringskørsel, hvor der bruges hjælpefunktioner, kan hvert af hjælpetrådene for varedisponering også vælge produktionsordres planlægningsopgaver. Det betyder, at der kan køre flere planlægningsprogrammer samtidigt. Mens flertrådede funktioner i almindelighed er en stor fordel for ydeevnen, er der også nogle funktionelle ulemper, når det kommer til planlægning.

I MRP planlægges alle produktionsordrer for et bestemt styklisteniveau i behovsdatodatosekvensen, hvilket betyder, at de ordrer, der har den tidligste behovsdato, skal planlægges først og dermed have størst chance for at få den tilgængelige ressourcekapacitet. Men når flere programmer plukker fra listen over ikke-planlagte ordrer er sekvensen ikke længere sikret, da den kan være fuldført hurtigere end en anden.

Når der planlægges med kapacitetsbegrænsning, og når flere programforekomster forsøger at planlægge ordrer, der potentielt bruger de samme ressourcer i samme tidsinterval, kan der forekomme et kapløb. Antallet af sådanne kapløbsbetingelser registreres i feltet **Planlægningskonflikter** på siden historik for behovsplaner. Konfliktløsningslogikken er følgende:

- Planlæg en ordre (låsefri), og få kapacitetsreservationer.
- Tag låsen.
- Kontrollér, om der findes nyere kapacitetsreservationer for de planlagte ressourcer i tidsintervallet.
  - Hvis ikke, skal du skrive kapaciteten og frigive låsen.
  - Hvis ja, skal du frigive låsen og genplanlægge ordren fra begyndelsen.

Når der planlægges med flere programforekomster, vil resultatet derfor ikke være fuldstændigt fastlagt, da det afhænger af den nøjagtige timing af hver tråd.

## <a name="operation-scheduling-performance"></a>Ydeevne af grovplanlægning

Selvom operationsplanlægning også kaldes en grov planlægning af kapaciteten set fra et programsynspunkt, kan det være et sværere problem at løse, hvis kapacitetsbegrænsning bruges, da der er behov for flere data til at fastlægge gennemførligheden.

Kapaciteten for en ressourcegruppe afhænger af, hvilke og hvor mange ressourcer der er medlemmer af ressourcegruppen. En ressourcegruppe har i sig selv ingen kapacitet. Når ressourcer er medlem af gruppen, har de kapacitet. Da medlemskabet af ressourcegruppen kan variere over tid, skal kapacitet evalueres pr. dag.

Ved grovplanlægning bruges ressourcegruppens kalender til at bestemme start- og sluttidspunkter for hver operation. Det betyder, at ressourcegruppens kalender angiver en grænse for, hvor lang tid der kan planlægges operationer for én operation på én dag i én ressourcegruppe. Modsat kalenderen for de specifikke ressourcer ignoreres kalenderens effektivitetsdata for ressourcegruppen, da den blot angiver åbningstider og ikke faktisk kapacitet.

Hvis arbejdstiden for en ressourcegruppe på en bestemt dato f.eks. er fra 8:00 til 16:00, kan en operation ikke lægge mere belastning på ressourcegruppen, end der kan være i løbet af 8 timer, uanset hvor meget kapacitet ressourcegruppen har tilgængelig i alt på den pågældende dag. Den tilgængelige kapacitet kan dog begrænse belastningen yderligere.

Belastningen fra finplanlægning for alle de ressourcer, der er medtaget i ressourcegruppen på en given dag, tages i betragtning, når den tilgængelige kapacitet for ressourcegruppen på samme dag beregnes. For hver dato er beregningen:

*Tilgængelig ressourcegruppekapacitet = kapaciteten for ressourcer i gruppen baseret på deres kalender &ndash; finplanlagt belastning af ressourcerne i gruppen &ndash; grovplanlagt belastning af ressourcerne i gruppen &ndash; grovplanlagt belastning af ressourcegruppen*

Under fanen **Ressourcekrav** i ruteoperationen kan ressourcekrav angives ved hjælp af enten en bestemt ressource (i dette tilfælde planlægges operationen ved hjælp af den pågældende ressource) for en ressourcegruppe, for en ressourcetype eller for en eller flere egenskaber, færdighed, kursus eller certifikat. Når du bruger alle disse indstillinger, giver det en stor fleksibilitet for rutedesignet, men det komplicerer også planlægningen af programmet, som kapaciteten skal redegøres for pr. "egenskab" (det abstrakte navn, der bruges i programmet, for egenskab, kompetencer osv.).

Ressourcegruppens kapacitet for en egenskab er summen af kapaciteten for alle ressourcer i den ressourcegruppe, der har den pågældende egenskab. Hvis en ressource i gruppen har en egenskab, medregnes den, uanset hvilket kapacitetsniveau der kræves.

I forbindelse med grovplanlægning reduceres den disponible kapacitet for en bestemt egenskab i en ressourcegruppe, når den indlæses med en operation, der kræver den pågældende egenskab. Hvis operationen kræver mere end én egenskab, vil kapaciteten blive reduceret for alle de krævede egenskaber.

For hver dato er den påkrævede beregning:

*Ledig kapacitet for en egenskab = kapacitet for egenskaben &ndash; finplanlagt belastning af ressourcerne med den specifikke egenskab, der er medtaget i ressourcegruppen &ndash; grovplanlagt belastning af ressourcer med den specifikke egenskab, der er medtaget i ressourcegruppen &ndash; grovplanlagt belastning af selve ressourcegruppen, der kræver den specifikke egenskab*

Det betyder, at hvis der er belastning på en bestemt ressource, tages der højde for belastningen i beregningen af ressourcegruppens ledige kapacitet pr. egenskab, fordi belastningen på en bestemt ressource reducerer dens bidrag til ressourcegruppens kapacitet for en egenskab, uanset om belastningen på den specifikke ressource er for den pågældende egenskab. Hvis der er belastning på ressourcegruppeniveauet, medtages den kun i beregningen af ressourcegruppens ledige kapacitet pr. egenskab, hvis belastningen er fra en operation, der kræver den specifikke egenskab.

Ovenstående logik er kompliceret, da det er den samme for hver type "egenskab", så hvis du bruger en grovplanlægning med begrænset kapacitet, kræver det en stor mængde data, der skal indlæses.

## <a name="viewing-scheduling-engine-input-and-output"></a>Visning af input og output for planlægningsprogrammet

Hvis du vil have specifikke detaljer om input og output for planlægningsprocessen, skal du aktivere logføring ved at gå til **Organisationsadministrations \> Konfiguration \> Planlægning \> Planlægning af sporing af cockpit**.

På denne side skal du først vælge **Aktivér logføring** i handlingsruden. Kør derefter planlægningen for produktionsordren. Når den er færdig, skal du vende tilbage til siden **Planlægning af sporing af cockpit** og vælge **Deaktiver logføring** i handlingsruden. Opdater siden, hvorefter der vises en ny linje i gitteret. Vælg den nye linje, og vælg **Download** i handlingsruden. Dette giver dig en .zip-komprimeret mappe, der indeholder følgende filer:

- **Log.txt** - Dette er den logfil, der beskriver de trin, som programmet gennemgår. Det er meget avanceret og kan være en smule overvældende, men når den bruges som led i at eksperimentere med ruteopsætningen for at løse problemer med ydeevnen, er det første, du skal se efter, forskellen i tiden mellem den første og den sidste linje, som giver dig den nøjagtige tid, du har brugt til planlægningen.
- **XmlModel.xml** - Den indeholder den model, der er indbygget i X++, og som programmet kører på. Det `JobId`, der bruges i filen, svarer til `RecId` fra den kildetabel, der indeholder jobbene (`ReqRouteJob` eller `ProdRouteJob`). Du skal typisk i denne fil se efter, om de datoer, der er angivet i `ConstraintJobStartsAt` og `ConstraintJobEndsAt`, er som forventet, at `JobGoal`-egenskaben er angivet korrekt, og at jobbene er relateret til hinanden via `JobLink`-begrænsningerne.
- **XmlSlots.xml** - Den indeholder alle de arbejdstider og kapacitetsreservationer, som programmet har anmodet om. Kalenderens arbejdstider og reservationer anmodes kun af programmet for de tidsperioder, hvor der gøres forsøg på at placere jobbene (og en ekstra buffer), så hvis filen indeholder tider langt ude i fremtiden, kan det være en indikation på et problem med konfigurationen. `ResourceProperty`-noderne vises for hver ressource, som ressourcegruppen og egenskaberne er tilknyttet, og for hvilke perioder.
- **Result.xml** - Den indeholder resultatet af planlægningskørslen.

Bemærk, at sporingsfunktionen kan give et betydeligt forbrug af ydeevne, så brug den kun til at undersøge planlægningen af specifikke ordrer på en kontrolleret måde. Hvis den er aktiveret under en varedisponeringskørsel, vil den hurtigt nå størrelsesgrænsen og stoppe.

## <a name="troubleshooting-performance"></a>Fejlfinding af ydeevne

Som det fremgår af alle tidligere afsnit, er der nogle faldgruber, når det kommer til opsætning og brug af planlægningsprogrammet, hvilket kan medføre problemer med ydeevnen. Følgende kontrolliste kan bruges til fejlfinding af sådanne problemer. Det er vigtigt at kigge på alle punkter, da det ofte er en kombination af flere faktorer, der fører til problemer.

### <a name="performing-scheduling-as-part-of-mrp-when-it-is-not-needed"></a>Planlægning, der udføres som del af MRP, når det ikke er nødvendigt

Selvom der bruges ruter til produktionskontrolformål, f.eks. efterkalkulation og rapportering, er det muligvis ikke nødvendigt at overveje dem under MRP. I nogle tilfælde vil en standardproduktionsgennemløbstid for varen være tilstrækkelig til planlægningen. Hvis du vil deaktivere ruteplanlægning, skal du angive kapacitetstidshorisonten til nul. Hvis planlægningen skal foretages, skal kapacitetshorisonten angives omhyggeligt, da det muligvis ikke er nødvendigt at overveje ruter for hele MPS-disponeringstidshorisonten.

Bemærk, at hvis ordren ikke planlægges under MPS, skal den i stedet planlægges, når ordreforslaget autoriseres. Det betyder, at autorisationsprocessen tager længere tid, så afhængigt af, hvor mange af de foreslåede ordreforslag der får den autoriserede ydeevnegevinst i MRP, kan den gå tabt ved autorisation.

### <a name="route-with-unnecessary-operations"></a>Rute med unødvendige handlinger

Når du designer ruten, er det fristende at prøve at modellere den virkelige verden nøjagtigt med alle de trin, som produktionen gennemgår. Dette kan være nyttigt i nogle tilfælde, men det er ikke godt for ydeevnen, da den model, som programmet skal arbejde på, bliver større (både hvad angår job og begrænsninger), og der vil blive udført flere SQL-sætninger for indsætning og opdatering af job og kapacitetsreservationer. Der er desuden en downstream-effekt, hvor det er nødvendigt at rapportere fremskridt på jobbene, hvilket kan afhjælpes med automatiske posteringer. Hvis dataene ikke bruges til noget, oprettes der en unødvendig belastning.

Det anbefales, at du kun opretter operationer, der er strengt nødvendige for planlægning (som typisk vil være flaskehalsressourcer) og/eller efterkalkulationsformål. Alternativt kan du gruppere mange mindre handlinger i én større handling, der repræsenterer en større del af processen.

### <a name="many-applicable-resources-for-an-operation"></a>Operation med mange relevante ressourcer

Antallet af relevante ressourcer til en operation bestemmes af de ressourcekrav, der er angivet for operationsrelationen. Kravet kan enten være til en bestemt ressource (individuel), eller det kan være baseret på ressourcens medlemskab af en ressourcegruppe eller egenskab.

Hvis der ikke foretages planlægning ved hjælp af kapacitetsbegrænsning, og alle de relevante ressourcer har samme kalender og effektivitet, vil planlægningsprogrammet altid ende med at vælge den samme ressource for en operation, men kun efter at have forsøgt alle de relevante ressourcer for at kontrollere, om der er en "bedre" end de andre. I dette tilfælde kan belastningen af planlægningen reduceres væsentligt ved ganske enkelt at tildele en bestemt ressource til operationen på rutedesigntidspunktet.

### <a name="route-with-parallel-operations"></a>Rute med parallelle handlinger

Parallelle operationer (primær/sekundær) er et effektivt værktøj til modelscenarier, som f.eks. når en maskine og en operatør begge er nødvendige for at udføre en bestemt opgave, med er også kilden til mange problemer med ydeevnen. Hvis et krav om en bestemt individuel ressource er tildelt både den primære og den sekundære operation, er det normalt ikke et problem. Men hvis der er mange mulige ressourcer for hver af operationerne, føjer den betydelig beregningskompleksitet til planlægningen.

Et alternativ til at bruge parallelle operationer er enten at udforme parrene som "virtuelle" ressourcer (hvilket derefter vil repræsentere det team, der altid samles for operationen) eller blot at modellere en af operationerne, hvis den ikke udgør en flaskehals.

### <a name="route-with-quantity-of-resources-higher-than-1"></a>Rute med et antal ressourcer, der er større end 1

Hvis du angiver det antal ressourcer, der skal bruges til en operation, til over ét, giver det i praksis de samme primære/sekundære operationer, da der sendes flere parallelle job til programmet. I dette tilfælde er der dog ikke mulighed for at bruge bestemte ressourcetildelinger, da et større antal end ét kræver, at mere end én ressource kan anvendes til operationen.

### <a name="excessive-use-of-finite-capacity"></a>Overdreven brug af kapacitetsbegrænsning

Brug af kapacitetsbegrænsning kræver, at programmet indlæser kapacitetsoplysningerne fra en database og kan have et beregningsoverskud, da det vil være sværere at finde en løsning, især i miljøer, hvor ressourcerne er reserveret tæt på den maksimale kapacitet. Derfor er det vigtigt at vurdere, om en ressource virkelig har brug for kapacitetsbegrænsning, eller den kan overbookes. Da der kan være forskel på kapacitetsbegrænsninger for ressourcerne på, hvor vigtigt det er, at de ikke er overbooket, anbefales det, at du bruger flaskehalsindstillingen i en ressource kombineret med en separat værdi i planen "Kapacitetstidshorisont for flaskehalsressourcer". Ved at bruge flaskehalse kan du sikre, at den generelle tidshorisont for kapacitetsbegrænsning kan sænkes.

### <a name="setting-hard-links"></a>Indstilling af hårde links

Rutens standardlinktype er *blød*, hvilket betyder, at der tillades et tidsinterval mellem sluttidspunktet for en operation og starten af den næste. Hvis du tillader dette, kan det have den uheldige virkning at, hvis der ikke er materialer eller kapacitet til rådighed for en af operationerne i meget lang tid, så kan produktionen være inaktiv i et langt tidsrum, hvilket vil sige en mulig forøgelse af igangværende arbejde. Dette sker ikke med hårde links, fordi afslutningen og starten skal justeres perfekt. Men hvis der angives hårde links, bliver planlægningsproblemet vanskeligere, fordi der skal beregnes arbejdstid og kapacitetsskæringspunkter for de to ressourcer til operationerne. Hvis der også er parallelle operationer, tilføjer dette betydelig beregningstid. Hvis ressourcerne i de to operationer har forskellige kalendere, der slet ikke overlapper, er problemet uløseligt.

Det anbefales, at du kun bruger hårde links, når det er strengt nødvendigt, og nøje overvejer, om det er nødvendigt for hver operation i ruten.

Hvis du vil reducere det igangværende arbejde uden at anvende hårde links, er det en fordel at planlægge ordren to gange med skifte til den modsatte retning for det andet gennemløb. Hvis den første plan blev udført bagud fra leveringsdatoen, skal den anden ske fremad fra den planlagte startdato. Det vil resultere i, at jobbene komprimeres så meget som muligt, så igangværende arbejde minimeres.

### <a name="separate-calendar-for-each-resource"></a>Separat kalender for hver ressource

En af de vigtigste datakilder for planlægningsprogrammet er kalenderoplysninger, som kan være kostbare at indlæse fra databasen. Da der genereres kalendere på basis af skabeloner, vil det være fristende at generere en kalender for hver ressource og derefter justere oplysningerne i denne kalender, når ressourcen har nedetid og andre problemer. Hvis du gør dette, vil det dog begrænse programmets mulighed for at cachelagre kalenderdataene, da det ville være nødvendigt at anmode om nye data for hver ressource, og det kan være en stor kilde til problemer med ydeevnen. Vi anbefaler i stedet, at du genbruger kalenderne så meget som muligt mellem ressourcerne og derefter styrer ændringerne af nedetiden ved at tildele et andet kalender-id for en periode.

### <a name="high-number-of-working-time-slots-per-calendar-day"></a>Højt antal arbejdstidsrubrikker pr. dag i kalenderen

Da programmet fungerer ved at undersøge tidsrubrikkers kapacitet én for én, er det en fordel at minimere antallet af tidsrubrikker pr. kalenderdag. Dette kan f.eks. ske ved at overveje, om det er vigtigt for tidsplanen at afspejle, at arbejderne har en pause på 5 minutter hver time.

### <a name="large-or-none-scheduling-timeouts"></a>Store (eller ingen) planlægningstimeout

Planlægningsprogrammets ydeevne kan optimeres ved hjælp af parametre, der findes på siden **Planlægningsparametre**. Indstillingerne **Timeout for planlægning er aktiveret** og **Timeout for planlægningsoptimering er aktiveret** skal altid angives til **Ja**. Hvis angivet til **Nej**, kan planlægningen muligvis løbe uendeligt, hvis der er oprettet en umulig rute med mange indstillinger.

Værdien for **Maksimal planlægningstid pr. sekvens** styrer, hvor mange sekunder der højst må bruges på at forsøge at finde en løsning for en enkelt sekvens (i de fleste tilfælde svarer en sekvens til en enkelt ordre). Den værdi, der skal bruges her, afhænger af kompleksiteten af ruten og indstillinger som kapacitetsbegrænsning, og maksimalt ca. 30 sekunder er et godt udgangspunkt.

Værdien for **Timeout for optimeringsforsøg** styrer, hvor mange sekunder der højst må bruges på at finde en bedre løsning end den, der oprindeligt blev fundet. Dette vil kun påvirke ruter, der bruger parallelle operationer, da disse gør det nødvendigt at teste forskellige kombinationer.

> [!NOTE]
> De værdier, der er angivet for timeout, anvendes både til planlægning af frigivne produktionsordrer og ordreforslag som en del af MRP. Derfor kan angivelse af meget høje værdier betyde markant længere kørselstid for MRP, når der køres for en plan med mange produktionsordreforslag.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]