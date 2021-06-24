---
title: Fejlfinde problemer med ydeevnen i ER-konfigurationer
description: Dette emne forklarer, hvordan du kan finde og rette problemer med ydeevne i ER-konfigurationer (elektronisk rapportering).
author: NickSelin
ms.date: 06/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner, ERFormatMappingRunJobTable, ERParameters, ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: maximbel
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: d77c2aad904ba911ac19009d6a981ea4153aaa48
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216859"
---
# <a name="troubleshooting-performance-issues-in-er-configurations"></a>Fejlfinde problemer med ydeevnen i ER-konfigurationer

Dette emne forklarer, hvordan du kan finde og løse problemer med ydeevne i [Elektronisk rapportering](general-electronic-reporting.md) (ER) [konfigurationer](general-electronic-reporting.md#Configuration).

Undersøgelser af ydeevne består typisk af flere trin.

1. [Indsamle](#collecting-data) data.
2. Analysere de indsamlede data.
3. På grundlag af resultaterne af analysen kan du bruge ER-konfigurationer til at [foretage ændringer](#making-changes) eller vælge at indsamle flere data.

## <a name="troubleshooting"></a>Fejlfinding

### <a name="analyze-execution-time"></a>Analysere udførelsestid

Udførelsestiden kan afhænge af uventede faktorer som f.eks. andre opgaver, der kører i samme miljø, og cachelagring, der bruger data, når de kaldes første gang. Derfor skal du gentage udførelsen og målingen flere gange.

Af og til forårsages ydeevneproblemer ikke af en ER-formatkonfiguration, der bruges til rapportering. De forårsages i stedet af den X++ kode, der bruges til at åbne konfigurationen af ER-formatet.

1. I enten [Handlingscenter](#infolog-time) eller [hændelsesloggen](#event-log-time) kan du se udførelsestiden for rapporten.
2. Sammenlign rapportens udførelsestid med den samlede udførelsestid i scenariet.
3. Hvis rapportens udførelsestid er meget mindre end den samlede udførelsestid, skal du overveje, hvor mange data rapporten behandler:

    - Hvis rapporten behandler en lille mængde data, kan problemet omfatte indlæsningstiden for konfigurationen.
    - Hvis rapporten behandler en stor mængde data, kan problemet omfatte forbehandling af X++. Brug [sporingsparser](#analyze-trace-parser-trace) til at analysere sagen.

    Du kan finde oplysninger om andre sager i de næste afsnit.

4. Kør flere test, der involverer forskellige datamængder, for at finde ud af, hvordan udførelsestiden afhænger af datamængden.

### <a name="analyze-trace-parser-traces"></a><a name="analyze-trace-parser-trace"></a>Analysere sporinger ved hjælp af sporingsparser

Forbered et lille eksempel, eller indsaml flere sporinger under tilfældige dele af rapportgenereringen.

Derefter skal du i [sporingsparser](#trace-parser) foretage en standardanalyse nedefra og op og besvare følgende spørgsmål:

- Hvilke topmetoder er der med hensyn til tidsforbrug?
- Hvilken del af den samlede tid bruger disse metoder?

Besvar de samme spørgsmål til forespørgsler.

Hvis du kan se, at metoderne har præfikset "ER", skal du gå videre til næste afsnit.

Hvis du kan se, at metoder eller forespørgsler er fra programpakken, skal du overveje generiske optimeringer (f.eks. oprette indekser).

Analysér antallet af kald. Hvis antallet er væsentligt højere end forventet, skal du overveje cachelagring af de tilsvarende noder for konfigurationen.

### <a name="analyze-database-calls"></a><a name="analyze-database-calls"></a>Analysere databasekald

Forbered et eksempel med en lille mængde data, så du kan indsamle en [ER-sporing](#electronic-reporting-traces).

Åbn derefter sporingen i ER-modeltilknytningsdesigneren, og se den nederst på siden. Besvar følgende spørgsmål:

- Er der nogen forespørgselsdublet? Hvis der er, skal du overveje en af følgende rettelser:

    - [Brug cachelagring](#use-caching), hvis du mener, at der er flere kald i én overordnet post.
    - [Brug et cachelagret, parameteriseret beregnet felt](#cached-parameterized), hvis du mener, at der er kald til samme post i forskellige poster.
    - [Brug en **JOIN**-datakilde](#use-join-datasource), hvis du skal læse et stort antal forskellige poster fra en database.

- Svarer antallet af forespørgsler og hentede poster til den overordnede mængde data? Hvis et dokument f.eks. indeholder 10 linjer, viser statistikken så, at rapporten udtrækker 10 linjer eller 1.000 linjer? Hvis du har stort antal hentede poster, skal du overveje en af følgende rettelser:

    - [Brug **FILTER**-funktionen i stedet for funktionen **WHERE**](#filter) til at behandle data på SQL Server-siden.
    - Brug cachelagring for at undgå at hente de samme data.
    - [Brug indsamlede datafunktioner](#collected-data) for at undgå at hente de samme data til opsummering.

### <a name="analyze-perfview-traces"></a>Analysere PerfView-sporinger

[PerfView](#perfview) er et værktøj til erfarne udviklere. Du kan finde mere detaljerede oplysninger om følgende trin i [Grundlæggende oplysninger om tidsundersøgelse af vægur](https://channel9.msdn.com/Series/PerfView-Tutorial/Tutorial-12-Wall-Clock-Time-Investigation-Basics).

1. Samle en sporing ved at bruge trådtid.
2. Medtag kun stakke, der bruger **runUnattended**, til kun at filtrere den tråd, der har konfigurationsudførelse. (Føj **runUnattended** til inputfeltet **IncPats**).
3. Fold al CPU-, netværks- og blokeret tid.
4. Indlæs [ER-forudindstillinger for PerfView](https://download.microsoft.com/download/2/d/0/2d037b0f-ffd1-4d65-b64f-fcdf51f2c81f/ER_PerfViewPresets.xml).
5. Vælg **ER** \> **Anden forudindstilling**.
6. Se på navnene:

    - Du vil sandsynligvis se den platformskode, der bruger mest tid.
    - Du kan dobbelttrykke (eller dobbeltklikke) og gå op gennem **opkaldsmodtagere**.

        Hvis du finder klasser, der har præfikset "ERExpression", og hvis de er funktioner, der er relateret til formler, kan du regne funktionsnavnet ud på basis af klassenavnet, og du kan se på ER-informationsbasen for at få vist attributterne.

### <a name="fixes"></a>Rettelser

- Hvis du kan se, at den meste CPU-tid forbruges af forespørgsler, skal du prøve at reducere antallet af forespørgsler:

    - [Gennemse ER-sporingen](#analyze-database-calls) for dublerede forespørgsler.
    - Se, hvor mange poster der hentes, og evaluer, hvor mange data der skal hentes teoretisk.

- Hvis du kan se, at den meste CPU-tid forbruges af de funktioner, der anvendes, skal du prøve at finde den plads i konfigurationen, der bruger de fleste ressourcer.
- Hvis du kan se, at den meste CPU-tid forbruges af funktioner til indsamling af data, skal du overveje at erstatte dem med *SQL group by* på modeltilknytningssiden.

### <a name="collecting-data"></a><a name="collecting-data"></a>Dataindsamling

Afhængigt af dit miljø kan du indsamle tilgængelige data på flere måder:

- Få den samlede kørselstid:

    - Fra handlingscenteret
    - Fra hændelsesloggen

- Sådan profilerer du udførelsen:

    - Ved hjælp af ER-værktøjer
    - Ved at bruge sporingsparser
    - Ved hjælp af PerfView

#### <a name="collecting-data-in-a-production-environment"></a>Indsamle data i et produktionsmiljø

Sommetider kan problemer kun genskabes i et produktionsmiljø. Du kan indsamle data på følgende måder:

- Med sporinger ved hjælp af [sporingsparser](../perf-test/trace-trace-tutorial.md)
- Ved at bruge [ER-udførelsesspor](trace-execution-er-troubleshoot-perf.md)
- Ved at bruge den samlede udførelsestid

#### <a name="collecting-data-in-a-development-environment"></a>Indsamle data i et udviklingsmiljø

Udover de værktøjer, der kan bruges i et produktionsmiljø, er der flere forskellige værktøjer, du kan bruge i et udviklingsmiljø:

- Hændelseslog (Microsoft-Dynamics-ElectronicReporting). Denne log kan give dig den samlede udførelsestid.
- Almindelige .NET-værktøjer, f.eks. PerfView.

Desuden giver et udviklingsmiljø dig større fleksibilitet til at eksperimentere. Du kan f.eks. deaktivere dele af rapporter for at se, hvordan udførelsestiden påvirkes.

### <a name="tools"></a><a name="tools"></a>Værktøjer

#### <a name="execution-time-in-the-action-center"></a><a name="infolog-time"></a>Udførelsestid i handlingscenteret

ER kan vise udførelsestiden for konfigurationen i handlingscenteret. Denne indstilling fungerer kun for en bestemt bruger og et bestemt firma og kun for interaktive sessioner. Benyt følgende fremgangsmåde for at gøre denne funktion tilgængelig.

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. På siden **Konfigurationer** i handlingsruden skal du under fanen **Konfigurationer** i gruppen **Avancerede indstillinger** vælge **Brugerparametre**.
3. I dialogboksen **Brugerparametre** skal du angive indstillingen **Vis filoprettelsestid** til **Ja**.

#### <a name="execution-time-in-the-event-log"></a><a name="event-log-time"></a>Udførelsestid i hændelsesloggen

1. Åbn Windows Logbog.
2. Åbn **Microsoft-Dynamics-ElectronicReporting/Operational** under **Program- og tjenestelogfiler**.
3. Søg efter **FormatMapingRun**-hændelser, hvor **EventID=2**, da disse hændelser indeholder oplysninger om tidsforløbet.

#### <a name="trace-parser-traces"></a><a name="trace-parser"></a>Sporinger ved hjælp af sporingsparser 

Da ER er implementeret i X++, kan du bruge almindelige X++ værktøjer til at analysere ydeevne. Du kan finde flere oplysninger i [Udføre sporinger ved hjælp af sporingsparser](../perf-test/trace-trace-tutorial.md).

Der er nogle få begrænsninger for denne metode. Da en del af ER er implementeret i C#, er det ikke alle detaljer, der er tilgængelige. Du kan dog få vist oplysningerne om dataforbrug. Lange rapportkørsler kan desuden overstige sporingens lagergrænse.

#### <a name="er-traces"></a><a name="electronic-reporting-traces"></a>ER-sporinger

ER kan indsamle egne sporinger og har visualiserings- og analyseværktøjer til disse sporinger. Du kan finde flere oplysninger i [Spore kørslen af ER-formater til fejlfinding af problemer med ydeevnen](trace-execution-er-troubleshoot-perf.md).

#### <a name="perfview"></a><a name="perfview"></a>PerfView

Da både X++ og ER er implementeret oven på .NET-platformen, kan du bruge almindelige .NET-værktøjer. Du kan f.eks. bruge det gratis værktøj [PerfView](https://github.com/Microsoft/perfview).

Du kan også indsamle data fra kommandolinjen. Følgende Windows PowerShell-script indsamler f.eks. udførelsestiden, indtil en formatudførelse stoppes på maskinen.

```powershell
c:\programs\PerfView collect "e:\traces\$(date -format "ddMMyyyy_hhmm").etl" `
    -CircularMB:20000 -ThreadTime `
    -NoNGenRundown `
    -StopOnEtwEvent:Microsoft-Dynamics-ElectronicReporting/FormatMappingRun/Stop
```

Der er nogle få begrænsninger for denne metode. Du skal have administrativ adgang til maskinen. Desuden skal du være en erfaren udvikler, fordi der er en stejl læringskurve.

### <a name="making-changes"></a><a name="making-changes"></a>Foretage ændringer

#### <a name="use-caching"></a><a name="use-caching"></a>Bruge cachelagring

Selvom cachelagring reducerer den tid, der kræves for at hente data igen, koster den hukommelse. Brug cachelagring i tilfælde, hvor mængden af hentede data ikke er meget stor. Du kan finde flere oplysninger om og et eksempel på, hvordan du bruger cachelagring, i [Forbedre modeltilknytning baseret på oplysninger fra udførelsessporet](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace).

#### <a name="use-a-cached-parameterized-calculated-field"></a><a name="cached-parameterized"></a>Bruge et cachelagret, parameteriseret beregnet felt

Sommetider skal værdier slås op gentagne gange. Det kan f.eks. være kontonavne og kontonumre. Du kan spare tid ved at oprette et beregnet felt med parametre på øverste niveau og derefter føje feltet til cachen.

Det anbefales, at du kun bruger denne fremgangsmåde, når størrelsen på cachelagrede data er lille. Yderligere oplysninger finder du i [Forbedre ER-løsningers ydeevne ved at tilføje parameteriserede BEREGNET FELT-datakilder](er-calculated-field-ds-performance.md).

#### <a name="use-a-join-data-source"></a><a name="use-join-datasource"></a>Bruge en JOIN-datakilde

Med en **JOIN**-datakilde kan du hente flere tilknyttede poster ved hjælp af én forespørgsel. Der behøver ikke bruge en separat forespørgsel til at hente hver tilknyttede post. Hvis du f.eks. har 1.000 linjer, og du henter varedata for hver linje efter relation, har du 1.001 forespørgsler (= 1.000 + 1). Hvis du bruger en **JOIN**-datakilde, bruger du kun én forespørgsel til at hente de samme data. Du kan finde flere oplysninger under [Bruge JOIN-datakilder til at hente data fra flere programtabeller i ER-modeltilknytninger](er-join-data-sources.md).

#### <a name="use-the-filter-function-instead-of-the-where-function"></a><a name="filter"></a>Bruge FILTER-funktionen i stedet for WHERE-funktionen

Funktionen **[FILTER](er-functions-list-filter.md)** kører betingelser på SQL Server, mens **WHERE**-funktionen henter alle data på listen, én post ad gangen, og anvender betingelsen for hver post. Du kan f.eks. vælge én post ud af 1.000 poster. Hvis du bruger **WHERE**, hentes alle 1.000 poster. Men hvis du bruger **FILTER**, hentes der præcis én post. **FILTER** kan også bruge indekser på databasesiden.

#### <a name="using-collected-data-functions-or-an-accumulated-data-data-source"></a><a name="collected-data"></a>Bruge indsamlede datafunktioner eller en akkumuleret datakilde

Hvis konfigurationen har en *Gruppér efter*-komponent, der opsummerer tidligere hentede data ved hjælp af en rapport, henter komponenten alle dataene igen. Ved at bruge indsamlede datafunktioner sætter du ER i stand til at akkumulere data under første hentning. Du kan finde flere oplysninger i [Konfigurere ER-format for at udføre optælling og sammenlægning](tasks/er-format-counting-summing-2.md).

#### <a name="rewrite-parts-of-the-configuration-in-x"></a>Omskrive dele af konfigurationen i X++

ER understøtter kaldmetoder for tabeller og klasser, herunder udvidelser. Overvej at omskrive dele af modeltilknytningen i X++ for at forbedre ydeevnen.

ER kan forbruge data fra følgende kilder:

- Klasser (datakilderne **objekt** og **klasse**)
- Tabeller (datakilderne **tabel** og **tabelposter**)

Med [ER API](er-apis-app73.md#how-to-access-internal-x-objects-by-using-erobjectsfactory) er det også muligt at sende forudberegnede data fra opkaldskoden. Programpakken indeholder adskillige eksempler på denne metode.
