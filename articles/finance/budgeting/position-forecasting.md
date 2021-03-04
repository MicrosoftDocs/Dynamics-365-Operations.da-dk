---
title: Budgetteret stilling
description: Udgifter, der er relateret til arbejdere, udgør ofte en stor andel af udgifterne til en organisation. Stillingsprognoser gør det muligt at planlægge disse udgifter og inkludere dem i planlægningen af budgetter.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmPositionForecast
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 64413
ms.assetid: 35e791d2-1905-4808-a579-7f181ddddd91
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d5bae90cf7c8f11fa5409014023d36cc68ae1bd0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441599"
---
# <a name="position-forecasting"></a>Budgetteret stilling

[!include [banner](../includes/banner.md)]

Udgifter, der er relateret til arbejdere, udgør ofte en stor andel af udgifterne til en organisation. Stillingsprognoser gør det muligt at planlægge disse udgifter og inkludere dem i planlægningen af budgetter.

## <a name="position-forecasting-in-budget-planning"></a>Stillingsprognoser i budgetplanlægning

[![Komponenter i stillingsprognoser](./media/graphic-top.png)](./media/graphic-top.png) 

Stillingsprognoser bruger tre hovedkomponenter til at angive nøjagtige budgetbeløb for stillingsudgifter. Disse beløb kan derefter integreres i en budgetplan for budgetberegninger. 

Den primære komponent er **prognosestillingen**, der repræsenterer alle de omkostningsdata, der er relateret til en enkelt stilling. Du kan oprette flere versioner af en prognosestilling ved at tildele et andet budgetplanscenarie til hver version. Flere versioner giver mulighed for en iterativ metode til budgettering og gør det muligt at sammenligne what-if-scenarier. Hver prognosestilling har en tilsvarende stilling i Personale.

Et **budgetomkostningselement** er en af installationskomponent, der repræsenterer en bestemt omkostning, der er knyttet til en stilling som f.eks. grundløn, arbejdsgiverbetalt sygesikring, betaling af mobiltelefon osv. Et budgetomkostningselement omfatter den hovedkonto, der bruges til omkostninger, og indstillinger for beregning. Hvert budgetomkostningselement kan tildeles til flere prognosestillinger. 

En **kompensationsgruppe** er en valgfri konfigurationskomponent, der bruges til at anvende et sæt budgetomkostningselementer og betale beregninger til stillinger, der har de samme lønkarakteristika. En løngruppe kan indeholde et kompensationsgitter for lønsatser. Når gruppen er tildelt en prognosestilling, kan et niveau og trin i gitteret tildele prognosestillingens indtjening. Sættet af omkostningselementer tilføjes automatisk.

### <a name="position-forecasting-processes"></a>Processer til stillingsprognoser

[![Processer til stillingsprognoser](./media/graphic1b.png)](./media/graphic1b.png) 

I en typisk proces for stillingsprognose opretter du først opsætningskomponenterne (budgetomkostningselementer og løngruppe). Prognosestillinger oprettes derefter baseret på eksisterende stillinger. Du kan derefter foretage justeringer. Du kan for eksempel tilføje eller afslutte stillinger, ændre lønsatser og fordelsomkostninger og tilføje lønstigninger. Du kan oprette flere versioner af en prognosestilling for at give mulighed for sammenligninger mellem forskellige budgetteringsscenarier. Du kan derefter medtage prognosestillingerne i budgetplaner og indsætte omkostningerne fra prognosestillingerne som budgetplanlinjer.

Du kan oprette flere versioner af prognosestillinger, efterhånden som budgetplanerne bliver revideret. Disse nye versioner danner grundlag for revisionerne.

## <a name="position-forecasting-setup"></a>Opsætning af stillingsprognose
[![Indstilling for fremhævning af illustration](./media/graphic2-1024x327.png)](./media/graphic2.png)

### <a name="budget-cost-elements"></a>Budgetomkostningselementer

Budgetomkostningselementer bruges til at definere omkostningsoplysninger for en prognosestilling. Disse oplysninger omfatter typen af omkostninger, hvordan omkostningerne beregnes, og om omkostningerne fordeles på flere datoer, når prognosestillingen er inkluderet i en budgetplan. 

Bestemte felter definerer funktionsmåden for budgetomkostningselementet. Hvert budgetomkostningselement er tildelt en budgetomkostningstype for **Indtjening**, **Fordel**, **Skat** eller **Andet**. Budgetomkostningstyperne anvendes primært til at beregne totaler. Værdien **Tilsidesættelse af budgetteret stilling** angiver, om beløbene på elementet kan ændres på prognosestillingen. Feltet **Fordelingsmetode** bruges, når der føjes en prognosestilling til en budgetplan. Du kan opdele omkostningsbeløbet på separate budgetplanlinjer, der har forskellige datoer, på månedsbasis, kvartalsvis, ugebasis eller for hver to uger. Ved at vælge en startdato kan du tildele omkostningen som et enkeltbeløb på den startdato, der er indstillet på prognosestillingen. 

Beregningen af budgetomkostningselementets omkostningsbeløb bruger ikrafttrædelsesdatoer for at muliggøre, at det samme omkostningselement kan bruges i forskellige perioder. En enkelt hovedkonto er tildelt i hver periode sammen med en procentdel eller et årligt beløb, der angiver omkostningsbeløbet. Et budgetomkostningselement kan bruge en procentdel af andre omkostningselementer eller et årligt beløb, men ikke begge. Du kan også angive en årlig grænse. 

Hvis omkostningselementet er baseret på en procentdel, skal du angive de budgetomkostningselementer, der bruges som grundlag for beregningen.

**Eksempel** 

Jodis organisation giver kursusrabat på 5 % af en medarbejders grundløn. Jodi vil gerne oprette et budgetomkostningselement for denne omkostning. Hun opretter et nyt budgetomkostningselement og giver det budgetomkostningstypen **Frynsegode**.

Jodi ønsker ikke, at chefer skal kunne ændre beløbet på frynsegoden. Hun vælger derfor **Tillad ikke omkostningsændringer** i feltet **Tilsidesættelse af budgetteret stilling**. Organisationen ønsker, at denne omkostning skal fordeles ligeligt på hver måned. Derfor vælger Jodi **Kvartalsvis** i feltet **Fordelingsmetode**. 

Derefter tilføjer Jodi en omkostningsberegningslinje, angiver datoerne og hovedkontoen og indtaster **5,00** som procentdelen. Hendes organisation har et maksimum på $ 5,000 om året til dette frynsegode. Jodi angiver derfor dette beløb som den årlige grænse. 

Endelig tilføjer Jodi de indtjeningsomkostningselementer, der bruges til grundløn, som beregningsgrundlag. Hendes budgetomkostningselement er nu klar til at blive brugt.

### <a name="compensation-groups"></a>Kompensationsgrupper

Løngrupper kan bruges til at gruppere prognosestillinger, der har lignende lønattributter. De kan også bruges til at definere en indtjening og årlige stigninger for en prognosestilling og til at tildele et sæt fælles budgetomkostningselementer. 

En grundlæggende funktion for løngrupper er at tildele et sæt budgetomkostningselementer til en prognosestilling. Løngrupper kan derfor bruges til at tilføje fælles omkostninger f.eks. frynsegodeplaner og skatter. En chef, der opretter en prognosestilling, behøver ikke at kende alle de omkostningselementer, der skal tilføjes. I stedet kan omkostningselementerne tilføjes, når løngruppen er valgt. Elementerne føjes til opsætningen af løngruppen under fanen **Budgetomkostningselementer**. 

Løngrupper kan også bestemme indtjeningssatserne for en prognosestilling. Du kan konfigurere en gruppe til at bruge timebasis eller årsbasis for løn for at beregne indtjening for prognosestilling. Under fanen **Lønsatstabeller** bestemmer et løngitter over lønsatser de indtjeninger, der føjes til en prognosestilling ud fra et tildelt niveau og trin. Disse gitre kan være baseret på eksisterende løngitre i Personale. Du kan også oprette nye løngitre til budgetplanlægning. 

Ikrafttrædelsesdatoer og udløbsdatoer i lønsatstabellerne gør det muligt at ændre lønsatser på en given dato. Denne funktion er nyttig, når en forhandlingsenhed har forhandlet en generel stigning midt i en budgetcyklus. I dette tilfælde ændrer du udløbsdatoen for den eksisterende tabel til dagen før datoen for satsændringen og tilføjer en ny satstabel, der starter på den nye dato. Når du opretter en ny satstabel, kan du vælge en eksisterende tabel over omkostningssatser personale, hvis du vælger **Opret et nyt kompensationsgitter ud fra et eksisterende gitter**. I den satstabel, der oprettes, giver indstillingen **Masseændring** dig mulighed for at anvende en procentvis stigning eller stigning med fladt beløb på alle satser i gitteret. 

Felterne **Stigningsplan** og **Dato for stigning** i løngruppen bruges, når du skal oprette lønstigninger, fordi stillinger går fra et trin til det næste. En årlig lønstigning er et typisk scenario. Stigningsplanen bestemmer, om stillingens årsdag eller en enkelt fælles dato bruges til trinstigningen. Stigningstidsplanen gælder for alle prognosestillinger i løngruppen. 

Det indtjeningsomkostningselement, der er valgt i løngruppen, bruges, når du opretter indtjeninger for prognosestillingerne i gruppen, herunder deres grundløn og de eventuelle trinstigninger. Feltet **Kompensation - fast struktur** kæder løngruppen sammen med en kompensationsplan med fast struktur i Personale. Denne sammenkædning kan tildele en arbejders oplysninger om fast løn til en prognosestilling og kan derfor gøre budgetplanlægningen mere nøjagtig. Husk, at strukturen af kompensationsgitteret (niveauer og trin) for løngruppen skal svare til den faste lønstruktur. Systemet kan ellers ikke kæde løngruppen og den faste lønstruktur sammen korrekt.

## <a name="creating-forecast-positions"></a>Oprette prognosestillinger
[![Illustration af fremhævning af "opret stillingsprognoser"](./media/graphic3-1024x327.png)](./media/graphic3.png)

### <a name="creating-forecast-positions-for-existing-positions"></a>Oprette prognosestillinger for eksisterende stillinger

For at få den mest nøjagtige budgetplanlægning kan du oprette budgetterede stillinger ved at bruge oplysninger fra eksisterende stillinger, uanset om stillingen i øjeblikket er besat eller ubesat. 

Funktionen **Tilføj eksisterende stillinger** viser alle stillinger for en organisation. Ved at angive datoen **Pr. dato** kan du ændre listen over stillinger, så den indeholder de stillinger, der fandtes på en dato i fortiden, eller mere almindeligt i fremtiden (for eksempel start på næste budgetcyklus). Vælg en budgetplanlægningsproces og et budgetplanscenarie, vælg stillinger på listen, og klik derefter på **OK** for at oprette prognosestillinger for de valgte stillinger. Bemærk, at du kun kan oprette en prognosestilling for hver eksisterende stilling i en budgetplanlægningsproces og et scenarie. Du kan dog oprette flere versioner ved at tildele forskellige budgetplanscenarier. 

Hvis budgetomkostningselementer er tildelt til stillingen i Personale, tildeles disse budgetomkostningselementer også til prognosestillingen, og standardbeløbene bruges. Feltet **Tildelt arbejder** på prognosestilling er angivet til navnet på den arbejder, der er tilknyttet stillingen, hvis en arbejder er tildelt. Dette felt er et simpelt tekstfelt. Der oprettes ikke noget direkte link. 

Hvis et budgetomkostningselement er markeret, tildeles det årlige beløb for fast løn til prognosestillingen ved hjælp af det valgte omkostningselement, hvis den tildelte arbejder har en fast lønstruktur. Hvis arbejderen ikke har en fast lønstruktur, eller hvis ingen arbejder er tildelt, bruges standardbeløbet til budgetomkostningselementet. 

Når indstillingen **Tildel en løngruppe** er angivet til **Ja**, og hvis den arbejder, der er tildelt stillingen, har en trinbaseret fast lønstruktur, der er knyttet til en løngruppe (som beskrevet tidligere), bliver arbejderens niveau og trin tilknyttet prognosestillingen sammen med løngruppen. Indtjeningsbudgetomkostningselementet fra løngruppen føjes til prognoseindstillingen, og lønsatsen på niveauet og trinnet fra løngruppen bruges. 

Indstillingen for indstillingen **Tildel en løngruppe** har højere prioritet end indstillingen **Tildeling af budgetomkostningselement**. De to indstillinger kan bruges på samme tid. 

[![Diagrammet "Tildel en løngruppe"](./media/graphic4.png)](./media/graphic4.png) 

En anden mulighed er at tildele en jubilæumsdato. Den valgte dato (justeret startdato, startdato for arbejder, startdato for ansættelse eller anciennitetsdato) fra den tildelte arbejder angives derefter som prognosestillingens årsdag og anvendes til oplysninger, og når der genereres lønstigninger.

### <a name="creating-new-forecast-positions"></a>Oprette nye prognosestillinger

Du kan oprette nye prognosepositioner på to måder: ved at kopiere en eksisterende prognosestilling og ved at oprette en helt ny prognosestilling. 

Når en prognosestilling er valgt, kan du vælge **Kopiér den valgte budgetterede stilling** for at oprette en ny prognosestilling, der har en prognosestatussen **Foreslået**. Denne prognosestilling har alle de samme data som den prognosestilling, der er kopieret, bortset fra den tildelte arbejder og eventuelle noter om budgetomkostningselementerne. Bemærk, at en tilsvarende ny stilling også er oprettet i Personale. Denne stilling har en beskrivelse af **Oprettet efter budget**. 

Du kan også oprette en helt ny prognosestilling. Vælg et eksisterende job, og vælg også budgetplanlægningsproces og budgetplansscenarie. Derefter kan du tilføje andre oplysninger, du vil tilføje. Igen oprettes der samtidigt en ny stilling i Personale.

## <a name="working-with-forecast-positions"></a>Arbejde med prognosestillinger
[![Illustration af fremhævning af "modificer stillingsprognoser"](./media/graphic5-1024x327.png)](./media/graphic5.png)

### <a name="multiple-versions-of-a-forecast-position"></a>Flere versioner af en prognosestilling

Du kan ændre prognosestillinger enten for at anvende kendte ændringer for budgetcyklussen eller for at modellere forslåede ændringer. En almindelig fremgangsmåde er at oprette et oprindeligt sæt prognosestillinger, oprette kopier af disse prognosestillinger og derefter bruge kopierne til at modellere forskellige sæt af ændringer. Kopierne tildeles til et andet budgetplanscenarie, som minimum indtil ændringerne er foretaget, og er ellers identiske med de prognosestillinger, de kopieres fra. Originaler og kopier deler samme stilling i Personale. 

Funktionen **Kopiér til scenarie** har denne funktion. Bemærk, at den enkelte stilling i Personale kun have én prognosestilling i hver budgetplanscenarie.

### <a name="modifying-forecast-positions"></a>Ændre prognosestillinger

Ændringer, der foretages til prognosestillinger, er begrænset til disse prognosestillinger. Ændringerne påvirker ikke stillingsposter i Personale. De fleste ændringer er også begrænset til den prognosestilling, der redigeres. Ændringerne er med andre ord specifikke for den budgetplanlægningsproces og det budgetplanscenarie, der er tildelt. Undtagelserne er ændringer af felter, der er fælles for stillingen på tværs af processer og scenarier. Disse felter omfatter felterne under fanen **Generelt** og fanen **Økonomiske dimensioner**. Når disse felter er ændret, gælder de nye værdier for stillingen i alle budgetplanlægningsscenarier. Derfor kan du med disse felter hurtigt opdatere alle versioner.

#### <a name="budget-cost-elements"></a>Budgetomkostningselementer

Budgetomkostningselementer indeholder de vigtigste oplysninger om budgetplaner: budgetbeløbet og en hovedkonto. Budgetbeløbet er det beløb, der sendes til budgetplanen, når en prognosestilling indgår i en plan. Budgetbeløbet beregnes og kan ikke ændres direkte. Dette beløb er enten det årlige beløb eller en beregning af procentdelen af det årlige beløbs basiselementer (som defineret i opsætningen af budgetomkostningselementet). Beløbet indregnes derefter med antallet af dage i elementets datoområde (startdato til slutdato) og også af værdien **Fuldtidsækvivalent** for prognosestillingen. 

For eksempel beregnes et budgetomkostningselementlinje fra 1. januar 2017 til 30. juni 2017, med et årligt beløb på 100.000 og en FTE-værdi på **0,50**, som 100.000 × (181 dage ÷ 365 dage) × 0,50 = 24,794.52. 

Budgetelementomkostningslinjerne skal genberegnes, når værdien for fuldtidsansatte ændres på prognosestillingen. Linjerne skal også genberegnes, når aktiveringsdatoer eller ophørsdatoer ændres. Ændringer af disse datoer kan medføre en opdatering af budgetomkostningselementets start- og slutdatoer, som skal ligge inden for datoerne for prognosestillingen. Når genberegningen er påkrævet, bliver knappen **Genberegn** tilgængelig, og meddelelsen "Kræver beregning" vises. Genberegning er også nødvendig, hvis du tilføjer eller fjerner et budgetomkostningselement.

**Eksempel** 

Organisationen overvejer to muligheder angående reducering af omkostningerne ved en bogholderstilling. En mulighed er at afslutte stilling halvvejs gennem året. Den anden mulighed er at ændre stillingen til halv tid for hele året. Brad har oprettet en prognosestilling for den eksisterende bogholderstilling i et grundscenarie. Han kopierer denne grundprognosestilling til scenarie A, indstiller ophørsdatoen til den 31 maj og genberegner. Brad kopierer derefter den oprindelige prognosestilling til scenarie B, ændrer værdien for fuldtidsansatte til **0,50** og genberegner. Brad har nu tre versioner, der hver især har omkostningstotaler, der er justeret med indstillingerne.

#### <a name="assigning-a-compensation-group"></a>Tildele en løngruppe

Når du første gang tildeler en løngruppe til en prognosestilling, tilføjes standardbudgetomkostningselementerne fra løngruppen. Hvis omkostningselementer allerede er tildelt til prognosestillingen, bevares disse omkostningselementer. Hvis en løngruppe allerede har tildelt og er blevet ændret, fjernes de eksisterende budgetomkostningselementer og udskiftes af sættet fra løngruppen. 

Når du vælger et lønniveau og -trin, føjes et omkostningselement for indtjeningsoverskud (som defineret i løngruppen). Det årlige beløb beregnes ved hjælp af satsen på det valgte niveau og trin, og de årlige timer i løngruppen (eller for en årsbaseret løn, det fulde beløb i niveau og trin). Dette beløb indgår igen ved omkostningselementlinjens datointerval og prognosestillingens fultidsværdi.

#### <a name="generating-increases"></a>Generere stigninger

Årlige stigninger (én pr. kalenderår) kan oprettes automatisk for de prognosestillinger, der har fået tildelt en trinbaseret løngruppe. Klik på **Generer stigninger** for at tilføje en budgetomkostningselement for indtjening på det næste højeste trin. Startdatoen for det budgetomkostningselement for indtjening er den planlagte stigningsdato, der vises på prognosestillingen. Denne dato angives fra løngruppen på to måder. Hvis løngruppens stigningsplan er indstillet til **Fælles dato**, er stigningsdatoen angivet for løngruppen. Hvis stigningsplanen er indstillet til **Årsdag**, bruges årsdagsfeltet på prognosestillingen, og budgetcyklussen angiver året. Hvis der er flere kalenderår i en budgetcyklus, tilføjes flere stigninger. 

Slutdatoen for det aktuelle budgetomkostningselement for indtjening opdateres med dagen før datostigningen. Genberegningsprocessen bruges automatisk, når der genereres stigninger. Du behøver derfor ikke genberegne manuelt. 

Hvis du klikker på **Generer stigninger** en gang mere, kører processen igen, men tilføjer ikke flere poster. Der oprettes kun én stigning pr. kalenderår.

#### <a name="changes-from-other-pages"></a>Ændringer fra andre sider

Opdateringer til prognosestillinger kan også stamme fra andre områder som f.eks. opsætningssiderne til budgetomkostningselementet og løngruppen. Du kan også ændre prognosestillinger ved hjælp af processen til masseopdatering. 

To indstillinger er tilgængelige på opsætningssiden **Budgetomkostningselement**: **Føj til stillinger** og **Opdater stillinger**. Indstillingen **Føj til stillinger** føjer budgetomkostningselementet til de valgte prognoseindstillinger. Hvis elementet allerede er tildelt en prognosestilling, springes den prognosestilling over. Indstillingen **Opdater stillinger** anvender de aktuelle værdier (hovedkonto, procent, årligt beløb osv.) på de valgte prognosestillinger. 

Hver proces har en lignende side, hvor du kan vælge prognosestillinger. Siden **Føj til stillinger** vises alle prognosestillinger, der kan vælges, hvorimod siden **Opdater stillinger** kun viser de prognosestillinger, der allerede har fået tildelt budgetomkostningselementet. (Derfor giver siden **Opdater stillinger** dig mulighed for at finde ud af, hvilke budgetterede stillinger der allerede har et vedhæftet omkostningselement). Du kan flytte budgettere stillinger fra et øvre gitter til et lavere gitter for at inkludere dem i opdateringen. 

Bemærk, at funktionen **Ret datoer** under fanen **Omkostningsberegning** øjeblikkeligt ændrer budgetomkostningselementets start- og slutdatoer på prognosestillingerne. Ingen udvælgelsesindstillinger er tilgængelige. 

På siden **Løngruppe** anvender funktionen **Opdater stillingssatser** de aktuelle lønsatstabellerne på de prognosestillinger, der er tildelt gruppen. Satserne opdateres, og der tilføjes flere omkostningselementlinjer for eventuelle nye tabelsatslinjer (baseret på datoer). Budgetomkostningselementerne og stigningen opdateres imidlertid ikke. Du kan vælge, hvilken budgetplanlægningsproces og hvilket budgetplanscenarie der skal opdateres. Du kan derfor opdatere et scenario, men lade andre scenarier forblive uændret til sammenligning. 

Ved at vælge prognosestillinger og derefter klikke på **Masseopdatering** kan du tilføje eller ændre mere end en prognosestilling på samme tid. Der er mange tilgængelige indstillinger. En indstilling under fanen **Økonomiske dimensioner** varierer en smule fra de andre og er relateret til budgetomkostningselementer. Du kan tilføje budgetomkostningselementer ved at angive indstillingen **Budgetstandarder** til **Ja**. Hvis ingen budgetomkostningselementer er valgt, men **Budgetstandarder** er angivet til **Ja**, fjernes alle budgetomkostningselementer, der er tildelt i øjeblikket. 

Genberegningsprocessen anvendes automatisk på alle prognosestillinger, der er ændret.

## <a name="bringing-forecast-positions-into-budget-plans"></a>Overføre prognosestillinger til budgetplaner

[![Illustration, der fremhæver "Tilføj til budgetplan"](./media/graphic6-1024x327.png)](./media/graphic6.png)

Formålet med at oprette og ændre prognosestillinger er at føje dem til budgetplaner, så budgetplanerne omfatter de mest nøjagtige budgetbeløb. Der er to metoder til at føje prognosestillinger til budgetplaner. Du kan enten bruge enten en genereringsproces eller en udvælgelsesproces i budgetplanen.

### <a name="generating-a-budget-plan-from-forecast-positions"></a>Oprette en budgetplan fra prognosestillinger

Funktionen **Opret budgetplaner fra budgetpositioner** opretter eller opdaterer budgetplaner, så de har budgetbeløbene og optælling af fuldtidsansatte fra prognosestillinger. Budgetbeløbene fra prognosestillingen bliver til linjebeløbene i budgetplanen og aggregeres med dimensionsværdier og en ikrafttrædelsesdato. Oprettelsesprocessen tildeler kildeprognosestillingen til budgetplanlinjen. Du kan få vist stillingen ved enten at tilføje prognosestillingen som en række i budgetplanlayoutet eller bruge forespørgslen **Budgetplanlinjer**. Du kan springe denne tildeling over ved at angive indstillingen **Medtag position på budgetplanlinje** til **Nej**. 

Du kan vælge et budgetplanscenarie med fuldtidsækvivalenter for at medtage antallet af fuldtidsækvivalenter i budgetplanen. Du kan kun vælge scenarier af den mængdetype, der er medtaget i layoutet for målbudgetplanen. Når du vælger et scenarie med fuldtidsækvivalenter, skal du også angive en hovedkonto med fuldtidsækvivalenter. Denne konto bruges til at oprette budgetplanlinjer med antal. 

Den budgetplanlægningsproces og det budgetplanscenarie, der er valgt i kilden, bestemmer budgetplanlægningsprocessen og scenariet for målscenariet. Da disse attributter tildeles til prognosestillinger, skal de synkroniseres med budgetplanen. Attributterne kan derfor ikke redigeres på målet. 

For andre oprettelsesprocesser er der tre tilgængelige indstillinger:

-   **Opret en ny budgetplan**– opretter en ny plan, der har de attributter, der er valgt i sektionen **Mål**.
-   **Erstat det eksisterende budgetplanscenarie** – Sletter alle data i målbudgetplanen i det valgte budgetplanscenarie, og opretter nye linjer, der har de valgte prognosestillingsdata.
-   **Opdater det eksisterende budgetplansscenarie, og tilføj nye data** – opdaterer eksisterende linjer i den målplan, der matcher kildelinjerne, og tilføjer også nye linjer til nye data. Overensstemmelsen er baseret på finanskontoen, datoen, budgetklassen og andre værdier som f.eks. prognosestillingen. Alle linjer, der har et stillingsnummer, der svarer til kildestillingsnummeret, erstattes med de nye linjer fra kilden.

### <a name="selecting-forecast-positions"></a>Vælge prognosestillinger

Du kan også føje prognosestillingsbudgetbeløb direkte til en budgetplan. Brug funktionen **Tilføj stillinger** over budgetplanlinjerne for at vælge de prognosestillinger, der skal medtages. 

De budgetplanscenarier, du kan vælge som kilde, er begrænset til scenarier, der er inkluderet i planens layout. En indstilling på under fanen **Mål** gør det muligt at angive scenariet for fuldtidsækvivalenter, og hovedkontoen er tilgængelig til medtagelse af fuldtidsækvivalenter, men ikke er nødvendig. 

Denne udvælgelsesproces fungerer som indstillingen **Opdater det eksisterende budgetplansscenarie, og tilføj nye data** for en oprettelsesproces. Alle eksisterende budgetplanslinjer, hvor prognosestillingen tilføjes, fjernes og erstattes af nye linjer, der er baseret på den aktuelle tilstand for prognosestillingen.

#### <a name="date-options"></a>Datoindstillinger

For både oprettelsesprocessen og udvælgelsesprocessen gælder det, at startdatoen på budgetomkostningslinjeelementet bestemmer ikrafttrædelsesdatoen for den tilhørende budgetplanlinje. Feltet **Fordelingsmetode** på konfigurationssiden for budgetsomkostningselementet angiver fordelingsmetoden:

-   **Startdato** – budgetomkostningselementets startdato bruges som budgetplanlinjens ikrafttrædelsesdato.
-   **Månedligt** – budgetbeløbet divideres ligeligt med antallet af måneder i datointervallet for at producere et typisk månedligt beløb, der tildeles på den første dag i hver måned. Hvis den første periode er en delvis måned, indregnes beløbet for den pågældende måned med antallet af dage, hvor omkostningen er aktiv i den måned, og resultatet er knyttet til startdatoen. Beløbet for den sidste måned er forskellen mellem det samlede budgetbeløb og summen af alle andre måneder. Derfor kan afrunding påvirke beløbet for den sidste måned.
-   **Kvartalsvist** – denne metode er den samme som **Månedligt**, men beregningerne foretages for perioder på tre måneder.
-   **Ugentligt** – logikken minder om logikken i metoderne for **Månedligt** og **Kvartalsvist**. Budgetbeløbet divideres ligeligt med antallet af uger i datointervallet for at producere et typisk ugentligt beløb, der tildeles på den første dag i hver uge. Hvis den første periode er en delvis uge, indregnes beløbet for den pågældende uge med antallet af dage, hvor omkostningen er aktiv i den uge, og resultatet er knyttet til startdatoen. Beløbet for den sidste uge er forskellen mellem det samlede budgetbeløb og summen af alle andre uger. Derfor kan afrunding påvirke beløbet for den sidste uge.
-   **Hver 14. dag** – denne metode er den samme som **Ugentligt**, men beregningerne foretages for perioder på to uger.

#### <a name="changing-budget-plan-lines-that-have-forecast-positions"></a>Ændre budgetplanslinjer, der har prognosestillinger

Budgetplanlinjer viser kilden til budgetbeløbene (nummeret på prognosestillingen), men er ikke sammenkædet. Derfor vises ændringer i prognosestillingen ikke på budgetplanlinjen, og ændringer i budgetplanlinjen vises i prognosestillingen. Hvis du ændrer en prognosestilling og ønsker, at de opdateringer skal medtages i en budgetplan, skal du sætte prognosestillingen ind i planen igen. Men husk, at denne proces fjerner alle de linjer, hvor der prognosestillingen er blevet tildelt. Derfor fjernes alle ændringer, du har foretaget i disse linjer. 

Hvis du vil se, hvilke budgetplaner en prognosestilling indgår i, kan du oprette rapporten **Budgetpositioner efter budgetplan**. Ellers kan du åbne faktaboksen **Tilknyttede budgetplaner** på prognosestillingen for at få vist planerne.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]