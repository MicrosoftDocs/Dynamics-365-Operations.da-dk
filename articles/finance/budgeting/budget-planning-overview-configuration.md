---
title: Oversigt over budgetplanlægning
description: I dette emne beskrives budgetplanlægning. Det indeholder oplysninger, der kan hjælpe dig med at konfigurere budgetplanlægning og budgetplanlægningsprocesser.
author: panolte
ms.date: 01/11/2018
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "17251"
- intro-internal
ms.assetid: a2e06633-a800-4840-a962-88fed8462104
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 391f62f42e482f79420bbe1bbd4cec4930790229
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2022
ms.locfileid: "7982059"
---
# <a name="budget-planning-overview"></a>Oversigt over budgetplanlægning

[!include [banner](../includes/banner.md)]

I dette emne beskrives budgetplanlægning. Det indeholder oplysninger, der kan hjælpe dig med at konfigurere budgetplanlægning og budgetplanlægningsprocesser.

## <a name="overview-of-budget-planning"></a>Oversigt over budgetplanlægning

En organisation kan konfigurere budgetplanlægning og derefter oprette budgetplanlægningsprocesser for at opfylde sine politikker, procedurer og krav til budgetudarbejdelse. Når du forstår de begreber og den terminologi, der bruges i Microsoft Dynamics 365 Finance, kan du nemmere og mere effektivt implementere budgetplanlægning i organisationen.

### <a name="key-terms"></a>Vigtige termer

- **Budgetplanlægningsprocesser** – Budgetplanlægningsprocesser bestemmer, hvordan budgetplaner kan opdateres, distribueres, gennemses og godkendes i organisationshierarkiet for budgettering. En budgetplanlægningsproces er knyttet til en budgetcyklus og en organisation gennem en juridisk enhed.
- **Budgetplaner** – Budgetplaner indeholder budgetdataene til en budgetcyklus. Du kan have flere budgetplaner, der bruges til forskellige formål. Du kan f.eks. bruge budgetplaner til at oprette budgetbeløb for forskellige organisationsenheder. Du kan også bruge dem til at udføre sammenligninger og træffe velovervejede beslutninger.
- **Budgetplanscenarier** – Budgetplansscenarier definerer kategorier af data for budgetplanerne. Du kan definere scenarier for budgetplaner for at understøtte monetære klasser og andre måleenhedsklasser, f.eks. mængder. Eksempler på scenarier med monetære budgetplaner inkluderer "Afdeling forrige år" og "Afdelingsforespørgsler". Eksempler på budgetplansscenarier, der bruger antal, omfatter "Forrige års supportopkald" og "Antal fuldtidsækvivalenter".
- **Budgetplanlægningsstadier** – Budgetplanlægningsfaser definerer de trin, som en budgetplan følger fra begyndelsen til den endelige godkendelse. Budgetplanlægningsstadier er arrangeret i arbejdsgange i budgetplanlægningen.
- **Budgetplanlægningsarbejdsgange** – Budgetplanlægningsarbejdsgange består af og definere stadier i budgetplanlægningen. Arbejdsgange i budgetplanlægningen er knyttet til arbejdsgange i budgettering. Arbejdsgange i budgetteringen er automatiserede og manuelle processer, der flytter budgetplaner gennem budgetplanlægningsstadier.

[![Budgetplanlægningsterminologi.](./media/budgetplanning-terms-1024x504.png)](./media/budgetplanning-terms.png)

### <a name="typical-tasks"></a>Typiske opgaver

Du kan bruge budgetplanlægning til at udføre følgende opgaver:

- Opret budgetplaner for at definere de forventede indtægter og udgifter for en budgetcyklus.
- Analyser og opdater budgetplaner for flere scenarier.
- Send automatisk budgetplanerne sammen med regneark, berettigelsesdokumenter og andre vedhæftede filer til gennemsyn og godkendelse.
- Konsolider flere budgetplaner fra et lavere niveau af organisationen i én overordnet budgetplan på et højere niveau. Du kan også udarbejde én budgetplan på et højere niveau i organisationen, og allokere budgetestimaterne til lavere niveauer.

Budgetplanlægning er integreret med andre moduler. Derfor kan du inkludere oplysninger fra tidligere budgetter, faktiske udgifter, anlægsaktiver og HR. Eftersom budgetplanlægning også er integreret med Microsoft Excel og Microsoft Word, kan du bruge disse programmer til at arbejde med budgetplanlægningsdata. En budgetadministrator kan f.eks. eksportere en afdelings budgetanmodning fra et budgetplanscenarie til et Excel-regneark. Dataene kan derefter analyseres, opdateres og opstilles i diagrammer i regnearket og derefter udgives tilbage til budgetplanlinjerne.

## <a name="configuring-budget-planning"></a>Konfigurere budgetplanlægning

Funktioner, der blev introduceret i Dynamics 365 Finance version 10.0.9 (april 2020), omfatter en funktion, der hjælper med at forbedre ydeevnen, når du bruger knappen **Publicer** til at opdatere eksisterende poster i Excel og derefter udgive dem tilbage til klienten. Denne funktion gør opdateringsprocessen hurtigere og hjælper også med at reducere sandsynligheden for, at en opdatering bliver blokeret, når du opdaterer mange poster samtidig. Hvis du vil gøre denne funktionalitet tilgængelig, skal gå til arbejdsområdet **Funktionsstyring** og slå funktionen **Optimering af forespørgsler om budgetplanlægning** til under **Budgettering**. Det anbefales, at du slår denne funktion til.

Siden **Budgetplanlægningskonfiguration** indeholder de fleste af de indstillinger, der er påkrævet for at konfigurere budgetplanlægning. I følgende afsnit beskrives nogle af de faktorer, du skal overveje at bruge, når du konfigurerer budgetplanlægning. Når du har fuldført konfigurationen, kan du konfigurere budgetplanlægningsprocesser.

### <a name="budget-planning-schema-optional"></a>Budgetplanlægningsskema (valgfrit)

Et valgfrit, men anbefalet første trin er at oprette et skema, der viser din organisations procedure til udarbejdelse af et budget. Du kan bruge en hvilken som helst metode, du vil, til at oprette dette skema.

Følgende illustration viser et generisk eksempel, hvor der oprettes separate arbejdsgange i budgetplanlægningen til forskellige niveauer af organisationen. Stadier er defineret i hver arbejdsproces, og bestemte scenarier er tildelt til hvert stadie til at indeholde budgetdata. Opgaver fuldføres for at flytte data fra ét stadie til det næste. Beløb kan f.eks. tildeles eller samles til forskellige konti, godkendelser eller andre undersøgelser. I denne illustration angiver kursiveret tekst et scenarie, der ikke kan redigeres i løbet af stadiet, eller data, der er historiske eller er blevet godkendt i et tidligere stadie og derfor ikke bør ændres.

[![Generisk skema for budgetplanlægning.](./media/budgetplanninggenericschema-300x145.png)](./media/budgetplanninggenericschema.png) 

I følgende illustration vises et eksempel, hvor virksomhedens hovedkvarter beregner de oprindelige beløb for startbudgettet og distribuerer dem til salgsafdelingerne. Salgsafdelingerne beregner og sender derefter deres budget tilbage til hovedkontoret, hvor budgetadministratoren samler og justerer budgettet. Endelig sender budgetadministratoren de regulerede budgetbeløb til regnskabsdirektøren (CFO) til gennemsyn, endelige justeringer og godkendelse.

[![Eksempel på skema til budgetplanlægning.](./media/budgetplanningexampleschema-300x145.png)](./media/budgetplanningexampleschema.png)

### <a name="organization-hierarchy-for-budget-planning"></a>Organisationshierarkiet til budgetplanlægning

På siden **Organisationshierarki** kan du angive et organisationshierarki som et budgetplanlægningshierarki til hver budgetplanlægningsproces. Budgetplanlægningshierarkiet behøver ikke at matche det standardorganisationshierarki, der bruges til andre formål. Da dette hierarki bruges til at samle og distribuere data, vil du måske have en anden struktur. I eksempelskemaet er salgsafdelingerne under et hovedkvarterniveau, der omfatter budget- og økonomiafdelinger. Denne struktur er sandsynligvis forskellig fra den struktur, der bruges til at styre handlinger for salgsafdelingerne. Kun et organisationshierarki kan tildeles til hver budgetplanlægningsproces.

Du kan finde flere oplysninger i [Organisationer og organisationshierarkier](../../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md).

### <a name="user-security"></a>Brugersikkerhed

Budgetplanlægning kan følge en af de to sikkerhedsmodeller for at definere brugertilladelser. For at angive sikkerhedsmodellen skal du angive budgetplanlægningsparameter på siden **Budgetplanlægningskonfiguration**.

### <a name="budget-planning-workflows-stages"></a>Arbejdsgangstadier i budgetplanlægning

Arbejdsgange i budgetplanlægning bruges sammen med budgetteringsarbejdsgange til at styre oprettelse og udvikling af budgetplaner.

Arbejdsgangen for en budgetplanlægning består af et bestemt sæt stadier, som en budgetplan bevæger sig igennem. Hver arbejdsgang i budgetplanlægningen er knyttet til en budgetteringsarbejdsgang. Budgetteringsarbejdsgange er en af de typer arbejdsgange, der bruges i hele Dynamics 365 Finance. De dirigerer budgetplanerne sammen med regneark, berettigelser og vedhæftede filer gennem organisationen til gennemgang og godkendelse.

Du opretter en arbejdsgang for budgetplanlægning i afsnittet **Arbejdsgangsstadier** på siden **Budgetplanlægningskonfiguration**. Der kan du vælge de stadier og den budgetteringsarbejdsgang, der skal bruges, og du kan konfigurere yderligere indstillinger.

Det er en god idé at oprette en budgetplanlægningsarbejdsgang for hvert niveau i et budgetteringshierarki. Derefter kan du tildele en budgetteringsarbejdsgang, der indeholder elementer, som svarer til stadierne i arbejdsgangen i budgetplanlægningen. I eksempelskemaet, der blev vist tidligere i dette emne, vil der blive oprettet én arbejdsgang i budgetplanlægningen for salgsafdelingerne, og en anden vil blive oprettet for hovedkontoret. En arbejdsgang i budgettering flytter budgetplaner gennem stadierne.

Du opretter en arbejdsgang i budgettering for budgetplanlægning på siden **Arbejdsgange i budgettering**. Fremgangsmåden minder om processen til oprettelse af andre arbejdsgange. I følgende illustration vises et eksempel på en arbejdsgang i hovedkvartererne.

[![Budgetteringsarbejdsgang for budgetplanlægning.](./media/budgetingworkflowforbudgetplanning-300x300.png)](./media/budgetingworkflowforbudgetplanning.png) 

Arbejdsgangen indeholder følgende elementer:

- Fordeling til salgsafdelingerne og aggregering af deres indsendelser
- Budgetchefens gennemgang
- CFO-godkendelse
- Midlertidige overgange mellem hvert stadie i budgetplanlægningsarbejdsgangen

Du tildeler budgetteringsarbejdsgangen til hver arbejdsgang i budgetplanlægningen i afsnittet **Arbejdsgangsstadier** på siden **Budgetplanlægningskonfiguration**.

### <a name="parameters-scenarios-and-stages"></a>Parametre, scenarier og stadier

Med de oprindelige indstillinger på siden **Budgetplanlægningskonfiguration** kan du oprette byggesten til senere konfigurationstrin:

- **Parametre** – Parametre definerer de sikkerhedsregler, du vil anvende i budgetplaner og de økonomiske standarddimensioner, der skal bruges, når brugere foretager detailudledning for beløb i budgetplansscenarier.
- **Scenarier** – Scenarier omfatter de datakategorier, som du vil bruge til budgetplaner. Du kan definere scenarier for budgetplaner for at understøtte monetære klasser og andre måleenhedsklasser, f.eks. mængde. I en budgetplan repræsenterer scenarier én version af data i budgetplanlægningen. Eksempler på scenarier med monetære budgetplaner inkluderer "Salg for forrige år" og "Underskrevne kontrakter". Eksempler på scenarier, der bruger mænger, omfatter "Antal salgsopkald" og "Antal fuldtidsækvivalenter".
- **Stadier** – Stadier definer de trin, som en budgetplan følger fra starten til den endelige godkendelse. Eksempler på stadier i budgetplanlægning omfatter "Hovedkvarterets aggregering", "Regnskabsdirektørens gennemgang" og "Endelig".

### <a name="allocation-schedules"></a>Fordelingsplaner

I budgetplanlægning kan du allokere beløb eller mængder på budgetplanlinjer fra ét scenarie til et andet eller endda til det samme scenarie. Du kan f.eks. fordele beløb eller mængder til det samme scenarie, hvis du vil anvende ændringer på de økonomiske dimensioner eller datoerne for beløbene i det pågældende scenarie. En tildeling kan udføres inden fore en budgetplan eller fra én budgetplan til en anden.

Fordelingsplaner fordeler automatisk budgetplanlinjer under behandling af arbejdsgangen. Du kan udføre fordelinger ved hjælp en af følgende fordelingsmetoder på listen **Fordelingsmetode**:

- **Fordel hen over perioder** – Du bruger en periodefordelingsnøgle til at fordele budgetplanlinjer fra kildescenariets budgetplan hen over perioder i destinationsscenariet.

    > [!NOTE]
    > Før du kan fordele på tværs af perioder, skal du oprette periodefordelingsnøgler på siden **Periodefordelingskategorier**.

- **Fordel på dimensioner** – Budgetplanlinjerne fordeles fra kildescenariet for budgetplanen på tværs af de økonomiske dimensioner i destinationsscenariet.

    > [!NOTE]
    > Før du kan fordele til dimensioner, skal du konfigurere budgetfordelingsbetingelser på siden **Budgetfordelingsbetingelser**.

- **Aggreger** – Budgetplanlinjer aggregeres fra kildescenariets budgetplan i de tilknyttede budgetplaner til destinationsscenariet i den overordnede budgetplan.
- **Fordel** – Budgetplanlinjer distribueres fra kildescenariets budgetplan i den overordnede budgetplan for destinationsscenariet i de tilknyttede budgetplaner.
- **Brug finansfordelingsregler** – Budgetplanlinjerne fordeles fra kildescenariets budgetplanlæg til destinationsscenariet på basis af den valgte finansfordelingsregel.
- **Kopier fra budgetplanen** – du kan vælge en anden budgetplan, der skal bruges som kilde til fordelingen.

### <a name="stage-allocations"></a>Trinfordelinger

Stadiefordelinger bruges til automatisk at fordele budgetplanlinjer under behandling af arbejdsgangen. Når der bruges stadiefordelinger, kan budgetplanlinjer oprettes og ændres i destinationsscenariet uden indgriben fra den person, som klargjorde budgetplanen, eller validatoren.

Når du konfigurerer en stadietildeling, skal du knytte arbejdsgangen og stadiet i budgetplanlægningen til fordelingstidsplanen. Arbejdsgangen i budgetplanlægningen skal være tilknyttet en arbejdsgang i budgettering, der bruger **Trinfordeling for budgetplanlægning** som automatiseret arbejdsgangsopgave. Når arbejdsgangen når det angivne stadie, sker fordelingen automatisk. Denne automatiserede opgave kan bruges til at oprette budgetplanlinjer i et nyt scenario.

I eksempelskemaet, der vises tidligere i dette emne, foretages en fordeling for at overføre beløb fra en budgetplan og scenarier i hovedkvarterets "Oprindelige" stadie til en anden budgetplan og scenarier i stadiet "Estimat" for salgsafdelingen. Følgende illustration viser det relevante afsnit i eksempelskemaet.

[![Stadiefordeling.](./media/stageallocation-204x300.png)](./media/stageallocation.png) 

Desuden udføres en aggregering i eksempelskemaet fra budgetplaner og scenarier i stadiet "Sendt" for salgsafdelingerne til en overordnet plan i stadiet "Opløsning" for hovedkvartererne. Følgende illustration viser det relevante afsnit i eksempelskemaet.

[![Aggregering.](./media/aggregation-109x300.png)](./media/aggregation.png)

### <a name="priorities"></a>Prioriteter

Du kan eventuelt bruge prioriteter for budgetplanen til at definere kategorier og målsætninger for de budgetplaner, som du har oprettet. Du kan også bruge prioriteter til at organisere, klassificere og evaluere flere budgetplaner. Du kan f.eks. oprette en prioritet i en budgetplanlægning for sundhed og sikkerhed og derefter evaluere budgetplaner, der er tildelt den pågældende prioritet. Du kan også tildele et nummer til budgetplanerne for at angive et rangering.

### <a name="columns-and-layouts"></a>Kolonner og layout

I en budgetplan vises budgettallene i rækker og kolonner. Du skal først definere kolonnerne, og derefter kan du oprette et layout for at definere præsentationen af disse kolonner.

Når du vil definere en kolonne, skal du vælge et budgetplansscenarie. Linjebeløb fra dette scenarie vises i budgetplanen. Du kan vælge en periode for at filtrere beløbet, og du kan også angive filtre, der er baseret på finanskontoen.

Når du definerer et layout, skal du vælge et finansdimensionssæt for at oprette budgetplanrækker, som du vil vise, og vælge kolonnerne som layoutelementer. Du kan oprette flere layout, så en budgetplan viser de ønskede data på forskellige stadier i budgetplanlægningsprocessen.

Ud over kolonner til budgetbeløb kan du definere kolonner til projektet, foreslået projekt, aktiv og foreslåede aktivfelter fra budgetplanen . Du kan også definere en kolonne for budgetterede stillinger. Denne indstilling er nyttig, når du skal analysere personalebudgetter.

I eksempelskemaet kan du oprette kolonner til scenarierne "PY-salg", "Kontrakter" og "Prognose". (I følgende illustration vises skemaets relevante afsnit). Du kan derefter opbryde en eller flere af disse scenarier i separate kolonner for hvert kvartal af regnskabsåret, så lederen af salgsafdelingen præcist kan angive budgetterede beløb for hver periode.

[![Illustration af sektioner i skemaet til tilføjelse af kolonner.](./media/columns.png)](./media/columns.png)

Du kan også angive, om hvert layoutelement (kolonne) kan redigeres, og om det er tilgængeligt i en regnearksskabelon, der er oprettet for dette layout. Til eksempelskemaet kan kolonnerne "Prognose", der bruges til layoutet til stadiet "Estimat", redigeres, hvorimod kolonnerne "PY-salg" og "Kontrakter" er skrivebeskyttet.

> [!NOTE]
> Som standard vil du være begrænset til 36 kolonner, medmindre du udvider budgetplanlægningen ved at følge trinnene i [Udvide budgetplanlægningslayout](./extending-budget-planning-layout.md).

### <a name="templates"></a>Skabeloner

I afsnittet **Layout** på siden **Budgetplanlægningskonfiguration** kan du oprette, få vist eller uploade en Excel-skabelon for hvert layout. Disse skabeloner er de projektmapper, der er knyttet til hver enkelt budgetplan til yderligere analyse, diagrammer og muligheder for indtastning af data.

Når der oprettes en skabelon, er layoutet låst og kan ikke redigeres. Denne lås sikrer, at skabelonformatet svarer stil layoutet for budgetplanen og indeholder de samme data. Når der oprettes en skabelon, kan den vises og redigeres. Du kan for eksempel føje diagrammer til skabelonen eller tilpasse udseendet.

> [!NOTE]
> En skabelon skal gemmes på en placering, som brugeren har adgang til, så de kan uploade til layoutet, efter at redigering er fuldført. På den måde bruges skabelonen sammen med budgetplaner, der bruger layoutet.

### <a name="descriptions"></a>Beskrivelser

I afsnittet **Layout** kan du tildele beskriver for at vise navnet på en økonomisk dimension, der er inkluderet i et layout. En organisation vil f.eks. at vise navnet på hovedkontoen ved siden af hovedkontonummeret i en budgetplan. Det kan dog være en god ide at udelade navnene på andre økonomiske dimensioner for at undgå at overfylde visningen.

## <a name="setting-up-budget-planning-processes"></a>Konfigurere budgetplanlægningsprocesser

Når du er færdig med at konfigurere budgetplanlægning, kan du angive budgetplanlægningsprocesser på siden **Budgetplanlægningsproces**. Budgetplanlægningsprocesser er et sæt regler, der bestemmer, hvordan budgetplaner kan opdateres, distribueres, gennemses og godkendes i organisationshierarkiet for budgettering.

For hver budgetplanlægningsproces skal du først vælge en budgetcyklus og en finanskonto. Hver budgetplanlægningsproces er kun relateret til én budgetcyklus og én finans. Du vælger derefter budgetorganisationshierarkiet i oversigtspanelet **Administration for budgetplanlægningsproces** og tildeler en arbejdsgang i budgetplanlægningen til alle de ansvarscentre i organisationen, der vises i gitteret.

Klik på **Tildel arbejdsgang** for at tildele eller ændre arbejdsgangen i budgetplanlægningen for lignende ansvarscentre, og vælg derefter den ønskede organisationstype og den arbejdsgang i budgetplanlægningen, der skal bruges. Det arbejdsgangs-id for budgettering, der er knyttet til de enkelte arbejdsgange i budgetplanlægningen, føjes automatisk til gitteret.

Når du definerer stadieregler og skabeloner i oversigtspanelet **Stadieregler og layouts for budgetplanlægning**, kan du definere et andet sæt regler og standardlayout for hvert budgetplanlægningsstadie. Salgsafdelingernes stadie "Estimat" kan f.eks. lade brugerne ændre linjerne i en budgetplan, men forhindre brugere i at tilføje linjer. Stadiet "Sendt" kan lade brugerne få vist linjer, men ikke tilføje eller ændre dem, da arbejdet i dette stadie er afsluttet, og ændringer til budgetplaner skal undgås. Vælg **Alternative layouts** for at vælge de layout, der er tilgængelige for budgetplaner.

Du kan også vælge prioriteter for budgetplanlægningens i oversigtspanelet **Begrænsninger af budgetplansprioritet**. Derefter kan der vælges prioriteter for budgetplaner

Det sidste trin er at aktivere budgetplanlægningsprocessen ved hjælp af menuen **Handlinger**. En budgetplanlægningsproces kan ikke bruges, før den er aktiveret.

Du kan også bruge menuen **Handlinger** til at oprette en ny proces ved at kopiere en eksisterende proces. Denne funktion er nyttig for organisationer, der følger samme procesforløb for hver budgetcyklus og foretage få eller ingen ændringer.

En anden nyttig kommando i menuen **Handlinger** er **Vis budgetprocesstatus**. Denne kommando giver en grafisk visning af budgetplanerne i en proces sammen med relevante data, f.eks. planens arbejdsgangsstatus, oversigt efter beløb og efter enhed og navigation med et enkelt klik til selve budgetplanerne.

[![Status for budgetplanlægningsproces.](./media/budgetplanningprocessstatus-300x171.png)](./media/budgetplanningprocessstatus.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
