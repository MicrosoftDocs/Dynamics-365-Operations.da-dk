---
title: Budgetplanlægningsoversigt
description: I denne artikel introduceres budgetplanlægning, og du får oplysninger, der kan hjælpe dig med at konfigurere budgetplanlægning og konfigurere budgetplanlægningsprocesser.
author: ShylaThompson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 17251
ms.assetid: a2e06633-a800-4840-a962-88fed8462104
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8a262b5200c8071bec78ff6d3ed7976d4b2057ea
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570966"
---
# <a name="budget-planning-overview"></a>Budgetplanlægningsoversigt

[!include [banner](../includes/banner.md)]

I denne artikel introduceres budgetplanlægning, og du får oplysninger, der kan hjælpe dig med at konfigurere budgetplanlægning og konfigurere budgetplanlægningsprocesser.

<a name="overview-of-budget-planning"></a>Oversigt over budgetplanlægning
---------------------------

Du udfører budgetplanlægning, når du forberede budgetterne, som en organisation skal implementere. En organisation kan konfigurere budgetplanlægning og derefter oprette budgetplanlægningsprocesser for at opfylde sine politikker, procedurer og krav til budgetudarbejdelse. 

Når du forstår de begreber og terminologi, der bruges i Microsoft Dynamics 365 for Finance and Operations, bliver det nemmere at implementere budgetplanlægning i organisationen.

### <a name="key-terms"></a>Vigtige termer

-   **Budgetplanlægningsprocesser** – Budgetplanlægningsprocesser bestemmer, hvordan budgetplaner kan opdateres, distribueres, gennemses og godkendes i organisationshierarkiet for budgettering. En budgetplanlægningsproces er knyttet til en budgetcyklus og en organisation via en juridisk enhed.
-   **Budgetplaner** – Budgetplaner indeholder budgetdataene til en budgetcyklus. Du kan have flere budgetplaner, der bruges til forskellige formål. Budgetplaner kan for eksempel bruges til at oprette budgetbeløb for forskellige organisationsenheder, eller de kan hjælpe dig med at foretage sammenligninger og velovervejede beslutninger.
-   **Budgetplanscenarier** – Budgetplansscenarier definerer kategorier af data for budgetplanerne. Du kan definere scenarier for budgetplaner for at understøtte monetære og andre måleenhedsklasser, f.eks. mængde. Eksempler på scenarier med monetære budgetplaner inkluderer Afdeling forrige år og Afdelingsforespørgsler. Eksempler på budgetplansscenarier, der bruger antal, omfatter forrige års supportopkald og antal fuldtidsækvivalenter.
-   **Budgetplanlægningsstadier** – Budgetplanlægningsfaser definerer de trin, som en budgetplan følger fra start til endelig godkendelse. Budgetplanlægningsstadier er arrangeret i arbejdsgange i budgetplanlægningen.
-   **Budgetplanlægningsarbejdsgange** – Budgetplanlægningsarbejdsgange består af og definere stadier i budgetplanlægningen. Arbejdsgange i budgetplanlægningen er knyttet til arbejdsgange i budgettering. Arbejdsgange i budgetteringen er automatiserede og manuelle processer, der flytter budgetplaner gennem budgetplanlægningsstadier.

[![Budgetplanlægningsterminologi](./media/budgetplanning-terms-1024x504.png)](./media/budgetplanning-terms.png)

### <a name="common-tasks"></a>Almindelige opgaver

Du kan bruge budgetplanlægning til at udføre følgende opgaver:

-   Opret budgetplaner for at definere de forventede indtægter og udgifter for en budgetcyklus.
-   Analyser og opdater budgetplaner for flere scenarier.
-   Send automatisk budgetplanerne sammen med regneark, berettigelsesdokumenter og andre vedhæftede filer til gennemsyn og godkendelse.
-   Konsolider flere budgetplaner fra et lavere niveau af organisationen i én overordnet budgetplan på et højere niveau i organisationen. Du kan også udarbejde én budgetplan på et højere niveau i organisationen, og allokere budgetestimaterne til lavere niveauer i organisationen.

Budgetplanlægning er integreret med andre Microsoft Dynamics 365 for Finance and Operations-moduler. Derfor kan du hente oplysninger fra tidligere budgetter, faktiske udgifter, anlægsaktiver og personale. Eftersom budgetplanlægning også er integreret med Microsoft Excel og Microsoft Word, kan du bruge disse programmer til at arbejde med budgetplanlægningsdata. En budgetadministrator kan f.eks. eksportere en afdelings budgetanmodning fra et budgetplanscenarie til et Excel-regneark. Dataene kan analyseres, opdateres og opstilles i diagrammer i regnearket og derefter udgives tilbage til budgetplanlinjerne.

## <a name="configuring-budget-planning"></a>Konfigurere budgetplanlægning
Siden **Budgetplanlægningskonfiguration** indeholder de fleste af de indstillinger, du har brug for at konfigurere budgetplanlægning. I følgende afsnit beskrives nogle vigtige faktorer, der skal overvejes, når du konfigurerer budgetplanlægning. Når du har fuldført konfigurationen, skal du konfigurere budgetplanlægningsprocesser.

### <a name="create-a-budget-planning-schema"></a>Oprette et budgetplanlægningsskema

Et valgfrit, men anbefalet første trin er at oprette et skema, der viser din organisations procedure til udarbejdelse af et budget. Du kan bruge en hvilken som helst metode, du vil, til at oprette dette skema. Følgende illustration viser et generisk eksempel, hvor der oprettes separate arbejdsgange i budgetplanlægningen til forskellige niveauer af organisationen. Stadier er defineret i hver arbejdsproces, og bestemte scenarier er tildelt til hvert stadie til at indeholde budgetdata. Opgaver udføres for at flytte data fra ét stadie til det næste. Beløb kan f.eks. tildeles eller samles til forskellige konti, godkendelser eller andre undersøgelser. I dette eksempel angiver kursiveret tekst et scenarie, der ikke kan redigeres i løbet af stadiet, eller data, der er historiske eller er blevet godkendt i et tidligere stadie og derfor ikke bør ændres. 

[![Generisk skema for budgetplanlægning](./media/budgetplanninggenericschema-300x145.png)](./media/budgetplanninggenericschema.png) 

I det følgende eksempel beregner virksomhedens hovedkvarter startbudgettets oprindelige beløb og distribuerer dem til salgsafdelingerne. Salgsafdelingerne beregner og sender derefter deres budget tilbage til hovedkontoret, hvor budgetadministratoren samler og justerer budgettet. Endelig sender budgetadministratoren regulerede budgetbeløb til regnskabsdirektøren til gennemsyn, endelige justeringer og godkendelse. 

[![Eksempel på skema til budgetplanlægning](./media/budgetplanningexampleschema-300x145.png)](./media/budgetplanningexampleschema.png)

###  <a name="organization-hierarchy-for-budget-planning"></a>Organisationshierarkiet til budgetplanlægning

På siden **Organisationshierarki** kan du angive et organisationshierarki som et budgetplanlægningshierarki til hver budgetplanlægningsproces. Budgetplanlægningshierarkiet behøver ikke at matche det standardorganisationshierarki, der bruges til andre formål. Da dette hierarki bruges til at samle og distribuere data, vil du måske have en anden struktur. I eksemplet på skemaet er salgsafdelingerne under et hovedkvarterniveau, der omfatter budget-og økonomiafdelinger. Denne struktur er sandsynligvis forskellig fra den struktur, der bruges til at styre operationer for salgsafdelingerne. Kun et organisationshierarki kan tildeles til hver budgetplanlægningsproces. 

Du kan finde flere oplysninger i [Organisationer og organisationshierarkier](../../fin-and-ops/organization-administration/organizations-organizational-hierarchies.md).

### <a name="user-security"></a>Brugersikkerhed

Budgetplanlægning kan følge en af de to sikkerhedsmodeller for at definere brugertilladelser. For at angive sikkerhedsmodellen skal du angive budgetplanlægningsparameter på siden **Budgetplanlægningskonfiguration**.

### <a name="budget-planning-workflows-stages"></a>Arbejdsgangstadier i budgetplanlægning

Arbejdsgange i budgetplanlægning bruges sammen med budgetteringsarbejdsgange til at styre oprettelse og udvikling af budgetplaner.

Arbejdsgangen for en budgetplanlægning består af et bestemt sæt stadier, som en budgetplan bevæger sig igennem. Hver arbejdsgang i budgetplanlægningen er knyttet til en budgetteringsarbejdsgang. Budgetteringsarbejdsgange er en af de typer arbejdsgange, der bruges i hele Finance and Operations. Budgetteringsarbejdsgangen dirigerer budgetplanerne sammen med regneark, berettigelser og vedhæftede filer gennem organisationen til gennemgang og godkendelse. 

Du opretter budgetplanlægningens arbejdsgang i sektionen **Arbejdsgangsstadier** på siden **Budgetplanlægningskonfiguration**. Der kan du vælge de stadier og den budgetteringsarbejdsgang, der skal bruges, og også konfigurere yderligere indstillinger. 

Det er en god idé at oprette en budgetplanlægningsarbejdsgang for hvert niveau i et budgetteringshierarki. Derefter kan du tildele en budgetteringsarbejdsgang, der indeholder elementer, som svarer til stadierne i arbejdsgangen i budgetplanlægningen. I eksemplet på skemaet, der blev vist tidligere i denne artikel, ville der blive oprettet én arbejdsgang i budgetplanlægningen for salgsafdelingerne og en anden ville være oprettet for hovedkontoret. En arbejdsgang i budgettering flytter budgetplaner gennem stadierne. 

Du opretter en arbejdsgang i Budgettering for budgetplanlægning på siden **Arbejdsgange i Budgettering**. Fremgangsmåden minder om processen til oprettelse af andre arbejdsgange i Finance and Operations. Følgende illustration viser et eksempel på en arbejdsgang i hovedkvarteret. 

[![Budgetteringsarbejdsgang for budgetplanlægning](./media/budgetingworkflowforbudgetplanning-300x300.png)](./media/budgetingworkflowforbudgetplanning.png) 

Arbejdsgangen indeholder elementer til allokering til salgsafdelingerne og sammenlægning af deres afsendelser, gennemgang af budgetadministrator, godkendelse af regnskabsdirektøren og stadieovergange mellem hvert stadie. 

Du tildeler budgetteringsarbejdsgangen til hver arbejdsgang i budgetplanlægningen i sektionen **Arbejdsgangsstadier** på siden **Budgetplanlægningskonfiguration**.

### <a name="parameters-scenarios-and-stages"></a>Parametre, scenarier og stadier

Med de oprindelige indstillinger på siden **Budgetplanlægningskonfiguration** kan du oprette byggesten til senere konfigurationstrin:

-   **Parametre** – Parametre definerer de sikkerhedsregler, der skal anvendes til budgetplaner og de økonomiske standarddimensioner, der skal bruges, når brugere foretager detailudledning for beløb i budgetplansscenarier.
-   **Scenarier** – Scenarier omfatter de datakategorier, som du vil bruge til budgetplaner. Du kan definere scenarier for budgetplaner for at understøtte monetære og andre måleenhedsklasser, f.eks. mængde. I en budgetplan repræsenterer scenarier én version af data i budgetplanlægningen. Eksempler på scenarier med monetære budgetplaner inkluderer salg for forrige år og underskrevne kontrakter. Eksempler på scenarier, der bruger mænger, omfatter antal salgsopkald og antal fuldtidsækvivalenter.
-   **Stadier** – Stadier definer de trin, som en budgetplan følger fra start til endelig godkendelse. Eksempler på stadier i budgetplanlægning omfatter hovedkvarterets aggregering, regnskabsdirektørens gennemgang og endelig.

### <a name="allocation-schedules"></a>Fordelingsplaner

I budgetplanlægning kan du allokere beløb eller mængder på budgetplanlinjer fra ét scenarie til et andet eller endda til det samme scenarie. Du kan for eksempel fordele til det samme scenarie, hvis du vil anvende ændringer til de økonomiske dimensioner eller datoerne for beløbene i det pågældende scenarie. En tildeling kan udføres inden fore en budgetplan eller fra én budgetplan til en anden. 

Fordelingsplaner fordeler automatisk budgetplanlinjer under behandling af arbejdsgangen. Du kan udføre fordelinger ved hjælp en af følgende fordelingsmetoder på listen **Fordelingsmetode**:

- <strong>Fordel hen over perioder</strong> – Du bruger en periodefordelingsnøgle til at fordele budgetplanlinjer fra kildescenariets budgetplan hen over perioder i destinationsscenariet. <strong>Bemærk!</strong> Før du kan fordele på tværs af perioder, skal du oprette periodefordelingsnøgler på siden *<strong><em>Periodefordelingskategorier</em></strong>*.
- <strong>Fordel på dimensioner</strong> – Budgetplanlinjerne fordeles fra kildescenariet for budgetplanen på tværs af de økonomiske dimensioner i destinationsscenariet. <strong>Bemærk!</strong> Før du kan fordele til dimensioner, skal du konfigurere budgetfordelingsbetingelser på siden *<strong><em>Budgetfordelingsbetingelser</em></strong>*.
- **Aggreger** – Budgetplanlinjer aggregeres fra kildescenariets budgetplan i de tilknyttede budgetplaner til destinationsscenariet i den overordnede budgetplan.
- **Fordel** – Budgetplanlinjer distribueres fra kildescenariets budgetplan i den overordnede budgetplan for destinationsscenariet i de tilknyttede budgetplaner.
- **Brug finansfordelingsregler** – Budgetplanlinjerne fordeles fra kildescenariets budgetplanlæg til destinationsscenariet på basis af den valgte finansfordelingsregel.
- **Kopier fra budgetplanen** – du kan vælge en anden budgetplan, der skal bruges som kilde til fordelingen.

### <a name="stage-allocations"></a>Trinfordelinger

Stadiefordelinger bruges til automatisk at fordele budgetplanlinjer under behandling af arbejdsgangen. Når der bruges stadiefordelinger, kan budgetplanlinjer oprettes og ændres i destinationsscenariet uden indgriben fra klargøreren af budgetplanen eller revieweren.

Når du konfigurerer en stadietildeling, skal du knytte arbejdsgangen og stadiet i budgetplanlægningen til fordelingstidsplanen. Arbejdsgangen i budgetplanlægningen skal være tilknyttet en arbejdsgang i Budgettering, der bruger *<strong><em>Trinfordeling for budgetplanlægning</em></strong>* som automatiseret arbejdsgangsopgave. Når arbejdsgangen når det angivne stadie, sker fordelingen automatisk. Denne automatiserede opgave kan bruges til at oprette budgetplanlinjer i et nyt scenario. 

I eksempelskemaet, der vises tidligere i denne artikel, foretages en fordeling for at overføre beløb fra en budgetplan og scenarier i hovedkvarterets oprindelige stadie til en anden budgetplan og scenarier i salgsafdelingens estimatstadie. Følgende illustration viser det relevante afsnit i eksempelskemaet.

[![Stadiefordeling](./media/stageallocation-204x300.png)](./media/stageallocation.png) 

Desuden udføres en aggregering i eksempelskemaet fra budgetplaner og scenarier i salgsafdelingens stadie Sendt til en overordnet plan i stadiet med hovedkvarterets aggregering. Følgende illustration viser det relevante afsnit i eksempelskemaet.

[![Aggregering](./media/aggregation-109x300.png)](./media/aggregation.png)

### <a name="priorities"></a>Prioriteter

Du kan eventuelt bruge prioriteter for budgetplanen til at definere kategorier og målsætninger for de budgetplaner, som du har oprettet. Du kan også bruge prioriteter til at organisere, klassificere og evaluere flere budgetplaner. Du kan f.eks. oprette en prioritet i en budgetplanlægning for sundhed og sikkerhed og derefter evaluere budgetplaner, der er tildelt den pågældende prioritet. Du kan også tildele et nummer til rangerede budgetplaner på tværs af alle budgetplaner.

### <a name="columns-and-layouts"></a>Kolonner og layout

Budgettallene vises på en budgetplan i rækker og kolonner. Du skal først definere kolonnerne, og derefter kan du oprette et layout for at definere præsentationen af kolonnerne. 

Når du vil definere en kolonne, skal du vælge et budgetplansscenarie. Linjebeløb fra dette scenario vises i budgetplanen. Du kan vælge en periode for at filtrere beløbet, og du kan også angive filtre, der er baseret på finanskontoen. 

Når du definerer et layout, skal du vælge et finansdimensionssæt for at oprette budgetplanrækker, som du vil have vist, og vælge kolonnerne som layoutelementer. Du kan oprette flere layout, så en budgetplan, der viser de data, der skal være på forskellige stadier i planlægningsprocessen. 

Ud over kolonner til budgetbeløb kan du definere kolonner til projektet, foreslået projekt, aktiv og foreslåede aktivfelter fra budgetplanen . Du kan også definere en kolonne for budgetterede stillinger. Denne indstilling er nyttig, når du skal analysere personalebudgetter. 

Til eksempelskemaet kan du oprette kolonner til PY-salg, kontrakter og prognosescenarier (i følgende illustration vises det relevante afsnit i skemaet). Du kan derefter opbryde en eller flere af disse scenarier i separate kolonner for hvert kvartal af regnskabsåret, så lederen af salgsafdelingen præcist kan angive budgetterede beløb for hver periode.

[![Kolonner](./media/columns.png)](./media/columns.png) 

Du kan også angive, om hvert layoutelement (kolonne) kan redigeres, og om det er tilgængeligt i en regnearksskabelon, der er oprettet for dette layout. Til eksempelskemaet kan budgetkolonner redigeres i det layout, der bruges til stadiet Estimat, hvorimod kolonnerne PY-salg og kontrakter er skrivebeskyttet.

### <a name="templates"></a>Skabeloner

I sektionen **Layout** på siden **Budgetplanlægningskonfiguration** kan du også oprette, få vist eller sende Excel-skabeloner. Disse skabeloner er de projektmapper, der er knyttet til hver enkelt budgetplan til yderligere analyse, diagrammer og muligheder for indtastning af data. 

Du kan oprette, få vist eller sende en skabelon til hvert layout. Når der oprettes en skabelon, er layoutet låst og kan ikke redigeres. Denne låsning hjælper med at sikre, at skabelonformatet svarer stil layoutet for budgetplanen og indeholder de samme data. Når der oprettes en skabelon, kan den vises og redigeres. Du kan for eksempel føje diagrammer til skabelonen eller tilpasse udseendet.

> [!NOTE] 
> Skabelonen skal gemmes på en placering, som brugeren har adgang til, så de kan overføres til layoutet, efter at redigering er fuldført. På den måde bruges skabelonen sammen med budgetplaner, der bruger layoutet.

### <a name="descriptions"></a>Beskrivelser

De beskrivelser, som du kan tildele i afsnittet **Layout**, bruges til at få vist navnet på en økonomisk dimension, der er inkluderet i et layout. En organisation vil f.eks. muligvis have vist navnet på hovedkontoen ved siden af hovedkontonummeret i en budgetplan, men måske ønsker at udelade navnene på andre økonomiske dimensioner for at holde visningen overskuelig.

## <a name="setting-up-budget-planning-processes"></a>Konfigurere budgetplanlægningsprocesser

Når du er færdig med at konfigurere budgetplanlægning, kan du angive budgetplanlægningsprocesser på siden **Budgetplanlægningsproces**. Budgetplanlægningsprocesser er et sæt regler, der bestemmer, hvordan budgetplaner kan opdateres, distribueres, gennemses og godkendes i organisationshierarkiet for budgettering. 

For hver budgetplanlægningsproces skal du først vælge en budgetcyklus og en finanskonto. Hver budgetplanlægningsproces er kun relateret til én budgetcyklus og én finans. Vælg derefter budgetorganisationshierarkiet i oversigtspanelet **Administration for budgetplanlægningsproces**, og tildel en arbejdsgang i budgetplanlægningen til alle de ansvarscentre i organisationen, der vises i gitteret. 

Klik på **Tildel arbejdsgang** for at tildele eller ændre arbejdsgangen i budgetplanlægningen for lignende ansvarscentre, og vælg derefter den ønskede organisationstype og den arbejdsgang i budgetplanlægningen, der skal bruges. Det arbejdsgangs-id for budgettering, der er knyttet til de enkelte arbejdsgange i budgetplanlægningen, føjes automatisk til gitteret. 

Når du definerer stadieregler og skabeloner i oversigtspanelet **Stadieregler og layouts for budgetplanlægning**, kan du definere et andet sæt regler og standardlayout for hvert budgetplanlægningsstadie. Salgsafdelingens stadie Estimat kan f.eks. lade brugerne ændre linjerne i en budgetplan, men forhindre brugere i at tilføje linjer. Stadiet Sendt kan lade brugerne få vist linjer, men ikke tilføje eller ændre dem, da arbejdet i dette stadie er afsluttet, og ændringer til budgetplaner skal undgås. For at vælge de layout, der er tilgængelige for budgetplaner, skal du klikke på **Alternative layouts**. 

Du kan også vælge prioriteter for budgetplanlægningens i oversigtspanelet **Begrænsninger af budgetplansprioritet**. Derefter kan der vælges prioriteter for budgetplaner 

Det sidste trin er at aktivere budgetplanlægningsprocessen via menuen **Handlinger** En budgetplanlægningsproces ikke kan bruges, før den er blevet aktiveret i menuen. 

I menuen **Handlinger** kan du også oprette en ny proces ved at kopiere en eksisterende proces. Denne funktion er nyttig for organisationer, der følger samme procesforløb for hver budgetcyklus og foretage få eller ingen ændringer. 

En anden nyttig kommando i menuen **Handlinger** er **Vis budgetprocesstatus**. Denne kommando viser grafisk budgetplanerne i en proces sammen med relevante data, f.eks. planernes arbejdsgangsstatus, oversigt efter beløb og efter enhed og navigation med et enkelt klik til selve budgetplanerne.

[![Status for budgetplanlægningsproces](./media/budgetplanningprocessstatus-300x171.png)](./media/budgetplanningprocessstatus.png)



