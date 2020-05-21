---
title: Definere varedisponering
description: I dette emne beskrives forskellige vigtige strategier og parametre, der bruges til definition af varedisponering.
author: t-benebo
manager: tfehr
ms.date: 07/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-05-31
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 1e7775e797708668a339b6b02ed822261406c829
ms.sourcegitcommit: 68092ed283bfbb7b6f611cce1b62c791f9b6a208
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/30/2020
ms.locfileid: "3323663"
---
# <a name="set-up-master-planning"></a>Definere varedisponering

[!include [banner](../includes/banner.md)]

I dette emne beskrives forskellige vigtige strategier og parametre, der bruges til definition af varedisponering. Den indeholder en oversigt over de typer planer, der bruges af varedisponeringen, og forklarer, hvilken planstrategi du skal bruge, afhængigt af firmaets behov. Den beskriver også de hovedparametre, der påvirker planen, og forklarer, hvordan disse parametre påvirker de foreslåede ordreforslag.

## <a name="types-of-master-plans"></a>Typer af behovsplaner

Varedisponering indeholder to typer planer: statisk og dynamisk. Hver type er designet til forskellige formål. Det anbefales, at du bruger den relevante plan til dit scenario for at opnå den bedste ydeevne.

### <a name="static-plan"></a>Statisk plan

Den statiske plan forbliver uændret, uanset eventuelle ændringer i forsyningen og behovet, indtil den næste gang varedisponering køres.

Den statiske plan bruges til at godkende og autorisere de ordrer, der foreslås. Det er en driftsplan, som forskellige medarbejdere i firmaet, f.eks. en indkøber eller produktionsplanlægger, kan bruge til at basere deres beslutninger på og bruge til at udføre deres daglige opgaver og aktiviteter.

Den statiske plan understøtter også regenerering. En fuldstændig ny optimeret plan beregnes, hver gang varedisponering køres, og eksisterende ordrer, der ikke er godkendt, slettes.

### <a name="dynamic-plan"></a>Dynamisk plan

Den dynamiske plan startes som regel som en kopi af den statiske plan, men den kan opdateres, hver gang masterdataene ændres. Hvis dataene f.eks. ændres, oprettes der en ny salgsordre.

Den dynamiske plan bruges til ad hoc-planlægning. Den lader firmaet overvåge netværket med ordreændringer og varetilgængelighed uden at forstyrre den statiske plan, som andre bruger i deres arbejdsprocesser. Det bruges især til leveringsevne. Den dynamiske plan er standardplanen, når nettobehovene åbnes fra ordresider (f.eks. sider for salgsordrer, indkøbsordrer eller produktionsordrer).

Den dynamiske plan bruger nettoændring. Derfor er det en hjælp til at sikre en hurtigere kørselstid.

## <a name="strategies-for-using-master-plans"></a>Strategier til brug af behovsplaner

Du kan bruge enten én plan eller to planer i varedisponering. Den strategi, du bruger, afhænger af dine forretningskrav.

### <a name="one-plan-strategy"></a>Strategi med én plan

I forbindelse med en strategi med én plan kan du bruge samme behovsplan for den statiske plan og den dynamiske plan. Denne strategi bruges til scenarier med produktion til lager, hvor du normalt ikke behøver simulere en plan, der opfylder en ordre.

Strategien med én plan bruges typisk i detail- og distributionsindustrier, eller hvor datoer for salgslevering bekræftes baseret på serviceniveauaftaler eller leveringstider. Når det gælder planen, kan leveringsdatokontrol bruges uden LE.

Hvis du skal foretage en simulering, kan planen køres igen for de varer, der kræver simulering. De ordreforslag, som ordresimuleringer producerer, er normalt autoriserede.

### <a name="two-plan-strategy"></a>Strategi med to planer

Når det gælder strategien med to planer, bruger du en statisk plan og en anden dynamisk plan. Strategien med to planer bruges typisk til at scenarier med konfigurere til ordre eller producere til ordre, hvor du skal foretage simuleringer af salgsordrer og beregne præcisee leveringsdatoer for salgsordrer, men beregningerne må ikke påvirke den daglige drift. Disse simuleringer udføres altid i den dynamiske plan. Strategien med to planer er f.eks. nyttig i forbindelse med bilindustrien og OEM-producenter.

Når det gælder strategien med to planer, kan leveringsdatokontrollen LE bruges. Når LE bruges, udløser den automatisk kørslen i den dynamiske plan.

### <a name="setting-up-the-plans"></a>Opsætning af planerne

Du kan oprette planer på siden **Behovsplaner** (**Varedisponering\> Opsætning \> Planer \> Behovsplaner**).

Du kan angive, hvilke planer der skal bruges til den statiske plan og den dynamiske plan, ved at indstille felterne **Aktuel statisk behovsplan** og **Aktuel dynamiske behovsplan** på siden **Varedisponeringsparametre** ( **Varedisponering \> Opsætning \> Varedisponeringsparametre**). Hvis du vil bruge en strategi med én plan, skal du vælge felterne **Aktuel statisk behovsplan** og **Aktuel dynamisk behovsplan**.

## <a name="types-of-planning-methods"></a>Typer af planlægningsmetoder

Der kan bruges tre beregningsmetoder til kørsel af varedisponering: regenerering og nettoændring. Hver metode giver en forskellig plan, når den køres.

Du kan angive planlægningsmetoden i dialogboksen **Kørsel af en varedisponering**. Hvis du vil åbne denne dialogboks, skal du gå til **Varedisponering \> Varedisponering \> Kør \> Varedisponering** eller vælge **Kør** i arbejdsområdet **Varedisponering**.

### <a name="regeneration"></a>Genopbygning

Metoden til regenerering af planlægningsmetoden sletter eksisterende ordre, medmindre de er autoriseret. Den genererer nye ordrer ud fra alle behovene. Regenering er den eneste planlægningsmetode, der er tilgængelig for statiske planer.

- Ændringer i forsyningen tages i betragtning. Disse ændringer omfatter ændringer i budgettet.
- Denne metode respekterer disponeringskoden **Periode**.
- Denne metode understøtter funktionen til produkterstatning (PI).

### <a name="net-change"></a>Netto ændring

Planlægningsmetoden med nettoændring genererer ordre til disponering af de behov, der er oprettet eller ændret, siden den seneste varedisponering blev kørt. Ændringer i forsyningen tages ikke i betragtning, når denne metode køres. Systemet tager ikke højde for ikke nye forsyninger, og tidligere oprettede ordrer slettes ikke, hvis der ikke længere er brug for dem. Planlægningsmetoden med nettoplanlægning kører hurtigere end metoden til regenerering. Den er kun tilgængelig for dynamiske planer.

- Handlings- og terminsdatoer opdateres for alle behov.
- Denne metode respekterer ikke disponeringskoden **Periode**.
- Denne metode opfylder ikke budgettet, selvom den er valgt i planen.
- Denne metode understøtter ikke funktionen til produkterstatning (PI).

### <a name="net-change-minimized"></a>Netto-ændring minimeret

Planlægningsmetoden med nettoændring minimeret genererer kun ordrer til disponering af de behov, der er oprettet eller ændret, siden den seneste varedisponering blev kørt. I modsætning til nettoændringsmetoden opdateres handlings- og terminsdatoer kun for nye eller ændrede behov. Denne planlægningsmetode er kun tilgængelig for dynamiske planer.

## <a name="types-of-scheduling-methods"></a>Typer af planlægningsmetoder

For hver af planerne i oversigtspanelet **Generelt** på siden **Behovspalner** (**Varedisponering \> Opsætning \> Planer\> Behovsplaner** ) skal du vælge den planlægningsmetode, der bruges til produktionsordrer. Du kan planlægge produktion på driftsniveau og jobniveau.

### <a name="operations-scheduling"></a>Grovplanlægning

Du kan bruge grovplanlægning til at få et generelt estimat af produktionsprocessens over tid. Grovplanlægning udfolder ikke operationerne til produktionsruten i job. Yderligere oplysninger om grovplanlægning finder du under [Grovplanlægning](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/operations-scheduling).

### <a name="job-scheduling"></a>Finplanlægning

Finplanlægning er en mere detaljeret planlægningsmetode, hvor hver operation inddeles i de enkelte opgaver eller job. Finplanlægning indeholder oplysninger om kapaciteten. Den bruges typisk til at planlægge individuelle job i produktionen til en aktuel eller kortsigtet tidsramme. Yderligere oplysninger om finplanlægning finder du under [Finplanlægning](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/job-scheduling).

## <a name="time-fences-in-days"></a>Tidshorisonter i dage

For hver enkelt plan kan du vælge, hvor langt ud i fremtiden de forskellige krav og andre overvejelser skal beregnes af varedisponeringen. Perioden kaldes en *tidshorisont*. For at opnå den bedste ydeevne i varedisponeringen anbefales det, at du justerer de forskellige tidshorisonter for at opfylde virksomhedens behov. For hver plan kan du finde tidshorisonterne i oversigtspanelet **Tidshorisonter i dage** på siden **Behovsplaner** (**Varedisponering \> Opsætning \>Planer \>Behovsplaner**).

> [!NOTE]
> Tidshorisonenter angiver, hvor langt ud i fremtiden de forskellige krav og andre overvejelser beregnes af varedisponeringen. De tidshorisonter, der vælges på denne side, tilsidesætter de tidshorisonter, der er defineret i disponeringsgruppen. Det betyder, at indstillingen for en tidshorisont angives til ja, og definitionen af dage til tilsidesætte den tidshorisont, der er defineret i disponeringsgruppen. Når der angives til Nej, vil tidshorisonten blive defineret i disponeringsgruppen. Hvis du endeligt ikke ønsker eller skal bruge en indstilling (f.eks. hvis du ikke vil bruge handlingsmeddelelser), skal du angive den til **Ja**og derefter angive tidshorisonten til **0** (nul) dage.

### <a name="coverage"></a>Disponering

Disponeringstidshorisonten repræsenterer planlægningsperioden, eller hvor langt ud behovet skal medtages. Det angiver med andre ord din planlægningshorisont.

Hvis du angiver indstillingen **Disponering** til **Ja**, kan du tilsidesætte den disponeringstidshorisont, der er defineret for varen ved behovsplanlægning. I dette tilfælde skal du angive det antal dage, hvor beregningen af behovsplanlægningen skal dække behov. Disponeringstidshorisonten beregnes fremad fra den aktuelle dato. Behov, der ligger før den aktuelle dato, behandles altid.

> [!NOTE]
> For at opnå den bedste ydeevne i varedisponeringen anbefales det, at du justerer disponeringstidshorisonten til din planlægningshorisont.

### <a name="freeze"></a>Låsning

Den fastlagte tidshorisont repræsenterer den periode, hvor eksisterende ordrer ikke ændres, når der køres en ny behovsplanlægning. Ordreforslagene fastfryses, og der foreslås ingen nye ordreforslag.

Hvis du angiver indstillingen **Låsning** til **Ja**, kan du tilsidesætte den låsningstidshorisont, der er defineret for varen ved behovsplanlægning. I dette tilfælde skal du angive det antal dage, hvor planlægningsaktivitet låses. Husk, i denne periode kan der ikke oprettes nye ordreforslag, og eksisterende ordreforslag kan ikke ændres.

### <a name="firming"></a>Autorisation

Autorisationstidshorisonten angiver den tidshorisont, i hvilken ordrene automatisk konverteres i til produktions- og indkøbsordrer. Denne proces kaldes også *automatisk autorisation af ordreforslag*.

Hvis du angiver indstillingen **Autorisation** til **Ja**, kan du tilsidesætte den autorisationstidshorisont, der er defineret for varen ved behovsplanlægning. I dette tilfælde skal du angive det antal dage, hvor indkøbsordreforslag og produktionsordreforslag skal autoriseres automatisk. Autorisationstidshorisonten beregnes fremad fra behovsplanlægningsdatoen. Automatisk autorisation af et indkøbsordreforslag kan kun forekomme, hvis varen er knyttet til en kreditor.

### <a name="forecast-plan"></a>Hovedplan

Hovedplanstidshorisonten angiver, hvor langt ude i den fremtidige varedisponering opretter ordrer for varer, der har en estimeret efterspørgsel.

Hvis du angiver indstillingen **Hovedplan** til **Ja**, kan du tilsidesætte den hovedplanstidshorisont, der er defineret for varen ved behovsplanlægning. I dette tilfælde skal du angive det antal dage, hvor salgsprognosen fra hovedplanen skal tages med i varedisponeringen.

### <a name="capacity"></a>Kapacitet

Kapacitetstidshorisonten angiver, hvor langt ude i fremtiden systemet tager højde for den maksimale kapacitet af dine ressourcer, når det planlægger ordrer. Med andre ord planlægger planen produktionsordrerne ved hjælp af produktionsruten for varerne, og den betragter produktionsrutens ressourcer og den maksimale kapacitet for hver ressource.

Hvis du angiver indstillingen **Kapacitet** til **Ja**, kan du tilsidesætte den kapacitetstidshorisont, der er defineret for varen ved behovsplanlægning. I dette tilfælde skal du angive det antal dage, som kapacitet skal planlægges for, i produktionsordreforslag. Ved behovsplanlægningen anvendes varens aktive produktionsrute, og der planlægges bagud fra behovsdatoen. Hvis behovsdatoen for et produktionsordreforslag ligger ud over kapacitetstidshorisonten, bestemmes gennemløbstiden på grundlag af varens leveringstid. Kapacitetstidshorisonten beregnes fremad fra den aktuelle dato.

### <a name="action-message"></a>Handlingsmeddelelse

Handlingsmeddelelser foreslår ændringer, der kan foretages i den eksisterende forsyningsordre for at optimere forsyningsplanen. De kan f.eks. anbefale, at du går fremrykker eller udskyder ordrer, eller at du forøger eller reducerer ordreantallet.

Hvis du angiver indstillingen **Handlingsmeddelelse** til **Ja**, kan du tilsidesætte den handlingsmeddelelsestidshorisont, der er defineret for varen ved behovsplanlægning. I dette tilfælde skal du angive det antal dage, hvor behovsplanlægningen skal opretter handlingsmeddelelser for behov. Handlingsmeddelelsestidshorisonten beregnes fremad fra den aktuelle dato.

Du kan finde flere oplysninger om handlingsmeddelelser under [Handlingsmeddelelser](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/master-planning/action-messages).

> [!NOTE]
> Beregningen af handlingsmeddelelser medfører en længere kørselstid for varedisponering. Hvis handlingsmeddelelser ikke regelmæssigt analyseres og anvendes (dagligt, ugentligt osv.), skal du overveje at deaktivere beregningen under kørslen af varedisponeringen. Hvis du vil deaktivere beregningen fra, skal du på siden **Behovsplaner** angive tidshorisonten for **Handlingsmeddelelse** til **0** (nul) for den behovsplan, du kører. Kontroller også, at indstillingen **Handlingsmeddelelser** er slået fra for alle disponeringsgrupper.

### <a name="calculated-delays"></a>Beregnede forsinkelser

Du kan angive, hvor langt ude i fremtiden mulige forsinkelser i ordreforslagene skal registreres og rapporteres. På denne måde kan du planlægge mulige (forsinkede) leveringsdatoer.

Hvis et ordreforslag ikke kan opfyldes for den ønskede dato, planlægges det til den tidligste indfrielsesdato for en transaktion, baseret på leveringstider samt tilgængelighed af og materiale og kapacitet.

### <a name="approved-requisitions-time-fence"></a>Tidshorisont for godkendte rekvisitioner

Du kan konfigurere varedisponering til at oprette ordreforslag til rekvisitionsbehov. Angiv indstillingen **Medtag rekvisitioner** til **Ja** i oversigtspanelet **Generelt** på siden **Behovsplaner**. Når formålet med en godkendt rekvisition er genopfyldning, opretter varedisponeringen automatisk et tilsvarende ordreforslag for at opfylde det. Genopfyldningsmetoden bestemmes af de leveringspolitikker, der er defineret for varerne i din organisation. Når en genopfyldningsrekvisition er oprettet og godkendt, kræves der ingen yderligere brugerhandling.

Ved at angive indstillingen **Tidshorisont for godkendte rekvisitioner** til **Ja** i oversigtspanelet **Tidshorisonter i dage** kan du tilsidesætte tidshorisonten for godkendte rekvisitioner, der er defineret for varen under behovsplanlægning. I dette tilfælde skal du angive det antal forløbne dage, hvor efterspørgsel fra godkendte rekvisitioner, der har formålet genopfyldning, skal medtages i behovsplanlægning. Du kan f.eks. angive, om det kun er uopfyldte, forfaldne behov fra godkendte rekvisitioner, der er oprettet inden for de sidste 10 dage, der skal medtages og planlægges.

### <a name="sequencing"></a>Rækkefølge

Brug af rækkefølge gør det muligt at arrangere ordreforslag baseret på rækkefølgeattributter, der er knyttet til det færdige produkt. Den bruges ofte til at forberede produktionsordrer til emballering. Den kan f eks. bruges til at emballere bokse i en bestemt rækkefølge baseret på farve og størrelse.

Hvis du angiver indstillingen **Rækkefølge** til **Ja**, kan du angive, hvor langt ude i fremtiden operationer eller job skal sorteres i. Vær opmærksom på, at jo længere tidshorisonten er, jo længere tager det at udføre varedisponeringen.

### <a name="calculated-delays"></a>Beregnede forsinkelser

Forsinkelsesindstillinger sikrer, at ordrerne har mulige planlagte datoer. Følgende indstillinger er tilgængelige i oversigtspanelet **Beregnede forsinkelser** på siden **Behovsplaner**:

- **Sørg for, at de planlagte ordrer ikke oprettes inden varedisponeringens kørselsdato**  – angiv denne indstilling til **Ja** for at sikre, at ordrerne ikke kan planlægges til datoer i fortiden.
- **Tilføj den beregnede forsinkelse til behovsdatoen** (under **Indkøbsordreforslag**) – angiv denne indstilling til **Ja** for at føje den beregnede forsinkelse til behovene.
- **Tilføj den beregnede forsinkelse til behovsdatoen** (under **Indkøbsproduktionsforslag**) – angiv denne indstilling til **Ja** for at føje den beregnede forsinkelse til behovene.
- **Tilføj den beregnede forsinkelse til behovsdatoen** (under **Planlagt overførsel**) – angiv denne indstilling til **Ja** for at føje den beregnede forsinkelse til behovene.
- **Tilføj den beregnede forsinkelse til behovsdatoen** (under **Planlagt kanban**) – angiv denne indstilling til **Ja** for at føje den beregnede forsinkelse til behovene.

Når du angiver indstillingerne for **Tilføj den beregnede forsinkelse til behovsdatoen** til **Ja** for at føje forsinkelserne til behovene, tager systemet højde for kapaciteten af ressourcerne og opretter mulige ordreforslag. Genberegning af datoerne for ordreforslagene øger kørselstiden for varedisponering. Hvis du derfor ikke behøver at bruge forsinkelser, skal du angive indstillingerne til **Nej**.

## <a name="positive-and-negative-days"></a>Positive og negative dage

Positive og negative dage påvirker den måde, varedisponering foreslår ordreforslag og handlinger på. Positive og negative dage er angivet for varens varedisponeringsgruppe. Du kan definere de forskellige disponeringsgrupper og angive deres parametre på siden **Disponeringsgrupper**  (**Varedisponering \> Opsætning  \> Disponering \> Disponeringsgrupper**).

### <a name="positive-days"></a>Positive dage

Positive dage angiver, hvor langt ude i fremtiden varedisponeringen tager højde for den aktuelle lagerbeholdning eller tilgange for at opfylde et fremtidigt behov. Hvis f.eks. de positive dage angives til **100**, kan den aktuelle lagerbeholdning bruges til at opfylde behovet i de næste 100 dage. Hvis der er en ordre på 150 dage fra dags dato, opretter varedisponeringen et ordreforslag for at opfylde dette behov, selvom den disponible lagerbeholdning for varen kan opfylde ordren. I forbindelse med hurtigtomsættelige varer, der har en kort leveringstid, er det måske ikke en god ide at bruge den disponible lagerbeholdning til en ordre, der ligger langt ude i fremtiden. I denne eksempel med hurtig omsætning vil den aktuelle disponible lagerbeholdning hurtigt gå væk, og flere ordrer kan placeres i fremtiden for at opfylde et fremtidigt behov, hvilket ville være muligt på grund af det korte leveringstidspunkt for varen.

De positive dage påvirker også handlingsmeddelelserne. Systemet kan f.eks. anbefale, at du øger et indkøbsordreforslag, så det omfatter et behov, der ligger inden for antallet af positive dage i fremtiden. Hvis de positive dage er angivet til **100**, og hvis der er behov for en vare om 30 dage fra dags dato, vil systemet oprette et ordreforslag for at opfylde dette behov. Hvis der er behov for den samme vare om 90 dage fra dags dato, anbefales det, at du øger ordreantallet om 30 dage fra dags dato, så ordren også dækker behovet om 90 dage. Hvis der imidlertid er behov for varen om 150 dage fra dags dato, anbefales det dog ikke, at du forøger antallet i den ordre, der allerede er planlagt. Der oprettes i stedet et nyt ordreforslag.

Som regel angives de positive dage til et tal, der ligger mellem den længste leveringstid for varerne og disponeringstidshorisonten. Det anbefales, at du tildeler varer, der regelmæssigt fremskaffes eller produceres til en disponeringsgruppe, hvor de positive dage svarer til varens gennemløbstid.

### <a name="negative-days"></a>Negative dage

Negative dage angiver, hvor sent varetilgange tillades. De repræsenterer det antal dage, du er villig til at vente, før du bestiller en ny genopfyldning, når du har negativ lagerbeholdning eller ikke har tilstrækkelig lagerbeholdning. Negative dage svarer på spørgsmålet: Skal vi oprette en ny indkøbsordre for varen, eller skal vi bruge et eksisterende indkøb, selvom vi ved, at varen kommer for sent?

Du har f.eks. en salgsordre på en vare 15 dage fra dags dato. Du har også en indkøbsordre for samme vare. Denne indkøbsordre vil blive modtaget om 20 dage fra dags dato. Vil du have systemet til at oprette en indkøbsordre for den pågældende salgsordre, eller vil du bruge den eksisterende ordre, også selvom du ikke kan opfylde salgsordren til tiden? Hvis de negative dage er angivet til mindre end **5** for at angive, at varen kan forsinkes maksimalt fem dage, opretter systemet et nyt indkøbsordreforslag for at opfylde salgsordren. Hvis de negative dage er angivet til større end **5**, bruger systemet den eksisterende ordre til varen.

De negative dage påvirker også resultaterne af varedisponeringen. Hvis de negative dage er angivet til et højt tal, vil der blive genereret mange handlingsmeddelelser.

Vi anbefaler, at du angiver de negative dage til et tal, der er mindre end leveringstiden for varen.

### <a name="dynamic-negative-days"></a>Dynamiske negative dage

Dynamiske negative dage tager højde for varens leveringstid og de negative dage, du har angivet. Systemet opretter et nyt indkøbsordreforslag på basis af den negative tidshorisont, der beregnes ved hjælp af følgende formel:

Leveringstid + negative dage + dags dato – behovsdato

Systemet bruger kun de planlagte forsyningsordrer, der ligger inden for denne tidshorisont, og opretter et nyt ordreforslag uden for det. Fordelen ved dynamiske negative dage er, at det vil medtage det enkelte produkts leveringstid for at genbruge eksisterende ordrer og undgå at oprette nye ordreforslag, der vil blive afsluttet på en dag i fremtiden på grund af forsinkelser, der skyldes leveringstidspunktet. 

Du kan finde flere oplysninger [Negative dage og dynamiske negative dage](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/master-planning/more-about-dynamic-negative-days).
