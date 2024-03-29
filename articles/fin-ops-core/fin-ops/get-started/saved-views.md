---
title: Gemte visninger
description: Denne artikel beskriver, hvordan du bruger de gemte visningsfunktioner.
author: jasongre
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: Platform update 28
ms.openlocfilehash: 571a4f403da0d20256f788c791cab273827c91b5
ms.sourcegitcommit: fb9b6969218f2b82f0a4c72bfad75387fe00395c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/22/2022
ms.locfileid: "9799485"
---
# <a name="saved-views"></a>Gemte visninger

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

[!INCLUDE [PEAP](../../../includes/peap-1.md)]

## <a name="introduction"></a>Start her

Personlig tilpasning spiller en vigtig rolle, når brugere og organisationer skal have mulighed for at optimere brugeroplevelsen efter deres behov. Du kan finde oplysninger om brugertilpasning i [Tilpasse brugeroplevelsen](personalize-user-experience.md).

Med traditionel personlig tilpasning kan brugerne kun have et enkelt sæt tilpasninger pr. side. **Gemte visninger** udvides ved tilpasning på flere vigtige måder:

- I visningerne kan brugerne have flere navngivne sæt tilpasninger pr. formular, som de hurtigt kan skifte mellem efter behov. Det giver brugeren mulighed for at oprette flere optimerede visninger af en side, hvor hver visning er tilpasset til behovet, når brugeren udfører en bestemt forretningsopgave. 
- Visninger, der oprettes til bestemte sidetyper, kan også indeholde brugertilføjede filtre eller sorteringer, som giver brugerne mulighed for hurtigt at vende tilbage til almindeligt filtrerede datasæt. Se afsnittet [Hvilke sider understøtter visninger](saved-views.md#what-pages-support-views) for at få yderligere oplysninger. 
- Visninger kan publiceres til brugere i bestemte sikkerhedsroller og bestemte juridiske enheder. Derfor kan alle brugere, der har en bestemt rolle og adgang til en angivet juridisk enhed, få adgang til at bruge denne visning, også selvom den pågældende bruger ikke har tilladelse til at tilpasse den. Denne publiceringsfunktion giver organisationer mulighed for at definere de standardvisninger i firmaet, der er optimeret til deres virksomhed. Yderligere oplysninger finder du i afsnittet [Administrere tilpasninger på organisationsniveau med visninger](saved-views.md#managing-personalizations-at-an-organizational-level-with-views).
- I modsætning til traditionelle tilpasninger gemmes visninger ikke automatisk, når en bruger udfører tilpasninger eller filtrerer en liste. Eksplicitte lagringer er nødvendige for at give brugerne fleksibiliteten til at oprette en visning før eller efter de ændringer, der er knyttet til den pågældende visning, er foretaget. Dette krav sikrer, at visningsdefinitioner ikke ændres utilsigtet af filtre eller brugertilpasninger, der ikke er beregnet til lang tids brug. De varer, som automatisk gemmes som en del af det typiske sideforbrug (f.eks. kolonnebredder eller den udvidede eller skjulte sektionstilstand) gemmes pr. visning.
- Visninger kan føjes til arbejdsområder som felter, lister eller links. Derfor kan et filtreret datasæt placeres i et arbejdsområde, og brugerne kan knytte et sæt tilpasninger, der er relevante for det pågældende datasæt, med et felt eller link.

## <a name="switching-between-views"></a>Skifte mellem visninger

Når visninger er blevet tilgængelige for et miljø, vil toppen af alle sider, der understøtter visninger, indeholde et skjult kontrolelement til valg af visninger, som viser navnet på den aktuelle visning.

Visningsvælgeren har to størrelsesvariationer: 

- **Store visningsvælgere** – Sider, der har en tydelig liste, har en større visningsvælger af forskellige årsager. Den vigtigste er, at den store visningsvælger angiver de sider, hvor visningen kan indeholde brugerdefinerede filtre og sorter. Der indgår filtre og sorter i visningerne, og derfor er den største vælger også påkrævet, fordi visningsnavnene ofte er den bedste beskrivelse af de data, der vises på skærmen, og forventningen er, at brugerne skifter mellem visninger ofte på disse sidetyper. Gruppering i et gitter kan også gemmes for visninger på en side med store visningsvælger. 
    
    [![Stor visningsvælger, der understøtter ændringer af forespørgsler i visningen.](./media/views-largeViewSelector.png)](./media/views-largeViewSelector.png)

- **Små visningsvælgere** – Alle andre sider i fuld skærmstørrelse (med undtagelse af arbejdsområder og dashboardet) har en mindre visningsvælger, der vises ud for sidens billedtekst. Visningerne på disse sider indeholder kun brugertilpasninger, og ikke brugerdefinerede filtre. På disse sider er formularteksten eller posttitlen ofte de vigtigste oplysninger øverst på siden. Den mindre størrelse af visningsvælgeren afspejler også en lavere forventet frekvens for skift af visninger på disse sider. 
    
    [![Lille visningsvælger, der ikke understøtter ændringer af forespørgsler i visningen.](./media/views-smallViewSelector.png)](./media/views-smallViewSelector.png)
 
Hvis du vælger visningsnavnet, åbnes visningsvælgeren med listen over tilgængelige visninger for denne side.

Hvis funtionen **Forbedret understøttelse af juridisk enhed for gemte visninger** er aktiveret, viser visningsvælgeren de tilgængelige visninger i to sektioner. Den første sektiont indeholder visninger, der er specifikke for den aktuelle juridiske enhed, og den anden indeholder visninger, der er tilgængelige for alle juridiske enheder. Den første sektion er kun synlig, hvis der er visnnger for siden, som er specifikke for de juridiske enheder.

- **Standardvisning** – Visningen **Standard** er den indbyggede visning af siden, hvor der ikke er anvendt brugertilpasninger.
- **Personlige visninger** – Visningerne uden hængelåse repræsenterer dine personlige visninger. Dette er visninger, som enten du har oprettet, eller som er tildelt af en administrator.
- **Låste visninger** – Nogle visninger (f.eks. **Standard**-visningen og eventuelle visninger, der er udgivet til din rolle) har et hængelåssymbol ved siden af dem i visningsvælgeren. Dette symbol angiver, at du ikke kan redigere disse visninger. Men ændringer, der afspejler sideforbruget, gemmes dog automatisk. Disse ændringer omfatter ændringer i bredden af en gitterkolonne og ændringer af den udvidede eller skjulte tilstand for et oversigtspanel. Du kan dog oprette en personlig visning, der er baseret på en låst visning, ved hjælp af handlingen **Gem som**, hvis du har rettigheder til personlige indstillinger.
- **Nye visninger** – Publicerede visninger, der endnu ikke er åbnet, har et spark-symbol til venstre for visningsnavnet.

Hvis du vil skifte til en anden visning, skal du først åbne visningsvælgeren og derefter vælge den visning, du vil indlæse. 

## <a name="creating-and-modifying-views"></a>Oprette og ændre visninger

I modsætning til traditionelle brugertilpasninger gemmes visninger ikke automatisk, når en bruger tilpasser siden, eller når en bruger anvender et filter på en liste eller sorterer den. Der kræves en eksplicit handling for at gemme disse ændringer i en visning. Dette krav giver brugerne fleksibiliteten til at oprette en visning før eller efter de ændringer, der er knyttet til den pågældende visning, er foretaget. Det sikrer også, at visningsdefinitioner ændres utilsigtet med engangsfiltre eller brugertilpasninger. Bemærk, at elementer i det typiske sideforbrug (f.eks. kolonnebredder eller den udvidede eller skjulte sektionstilstand) gemmes automatisk i den aktuelle visning, selv for låste visninger.

Hvis du vil sikre, at visningens aktuelle tilstand er kendt, når du begynder at ændre en visning ved at tilpasse eller filtrere den, vises der en stjerne (\*) ud for navnet på den aktuelle visning. Dette symbol angiver, at du kigger på en ikke-gemt, ændret version af denne visning.

[![Ikke-gemte ændringer i en visning.](./media/views-unsavedChanges.png)](./media/views-unsavedChanges.png)

Hvis du vil gemme disse ændringer, skal du følge nedenstående trin.

1. Vælg visningsnavnet for at åbne visningsvælgeren.
2. Rediger den eksisterende visning ved at vælge **Gem**. Bemærk, at denne handling ikke er tilgængelig for låste visninger. 
3. Sådan oprettes en ny visning:

    1. Vælg **Gem som**. 
    2. Angiv et navn og eventuelt en beskrivelse af visningen i ruden **Gem visnsing som**.
    3. Hvis denne visning skal være din standardvisning, skal du vælge **Fastgør som standard**. Yderligere oplysninger om standardvisninger finder du i afsnittet [Ændring af standardvisningen](#changing-the-default-view) nedenfor. 
    4. Hvis funktionen **Forbedret understøttelse af juridisk enhed for gemte visninger** er aktiveret, kan du vælge, om denne visning skal være tilgængelig for alle juridiske enheder eller kun for et delsæt af dem.
    5. Vælg **Gem**.

## <a name="changing-the-default-view"></a>Ændre standardvisningen

Standardvisningen er den visning, som systemet vil forsøge at åbne, første gang du åbner siden. Du skal indstille standardvisningen til den visning, du forventer at bruge oftest. 

> [!NOTE]
> - I den grundlæggende funktion **Gemte visninger** er der en enkelt global standardvisning på tværs af juridiske enheder. Hvis du ændrer standardvisningen, åbnes denne visning som standard, uanset hvilken juridisk enhed du aktuelt befinder dig i.
> - Når funktionen **Forbedret understøttelse af juridisk enhed for gemte visninger** er slået til, kan hver juridiske enhed få sin egen standardvisning pr. side.

For at ændre standardvisningen for en side skal du følge disse trin:

1. Skift til den visning, du bruger som standard. 
2. Vælg visningsnavnet for at åbne visningsvælgeren. 
3. Vælg **Flere** og derefter **Vælg som standard**.

Når du opretter en ny visning (ved hjælp af handlingen **Gem som**), kan du også gøre den nye visning til standardvisningen ved at indstille **Vælg som standard**, før du gemmer visningen.

> [!WARNING]
> I nogle tilfælde køres den forespørgsel, der er knyttet til standardvisningen, ikke, første gang du åbner en side. Hvis du f.eks. åbner siden via et felt, køres feltets forespørgsel, uanset hvilken forespørgsel der er knyttet til standardvisningen. Hvis du åbner en side med en **standardvisning**, som allerede har en defineret forespørgsel, køres den oprindelige forespørgsel i stedet for standardvisningens forespørgsel. I dette tilfælde modtager du en informativ meddelelse, når visningen indlæses, med en integreret handling, der giver dig mulighed for at indlæse forespørgslen i standardvisningen direkte. Hvis du skifter visning, efter at siden er blevet indlæst, skal visningsforespørgslen kunne køres som forventet. 

## <a name="managing-personal-views"></a>Administrere personlige visninger

Dialogboksen **Administrer mine visninger** indeholder grundlæggende vedligeholdelsesfunktioner til dine personlige visninger og rækkefølgen af visninger i visningsvælgeren. Når du vil åbne denne side, skal du vælge navnet på visningen for at åbne rullemenuen for visningsvælger, vælge **Flere** og derefter vælge **Administrer mine visninger**.

Hvis funktionen **Forbedret understøttelse af juridisk enhed for gemte visninger** er aktiveret, viser sektionen **Mine visninger** i dialogboksen **Administrer mine visninger** de tilgængelige visninger for siden i sektioner. Eventuelle visninger, der er specifikke for den aktuelle juridiske enhed, vises i deres egen sektion. Sektionen **Globale visninger** vises altid, så du kan administrere de visninger, der er tilgængelige for siden i alle juridiske enheder. 

Hvis du vil se en liste over tilgængelige visninger for den pågældende side, kan du bruge følgende sæt handlinger.

- **Ændre standardvisningen** – Brug handlingen **Fastgør som standard** for at gøre den aktuelt valgte visning til standardvisning for denne side. Hvis funktionen **Importér understøttelse af juridisk enhed for gemte visninger** er aktiveret, giver sektionen **Globale visninger** dig mulighed for at få vist standardvisningen for enten den aktuelle juridiske enhed eller alle juridiske enheder.
- **Omarranger dine visninger** – Brug handlingerne **Flyt op** og **Flyt ned** for at arrangere dine visninger i en bestemt rækkefølge.
- **Omdøb en visning** – Brug handlingen **Omdøb** til at ændre navnet på den aktuelt valgte personlige visning. Denne handling er slået fra for låste visninger. 
- **Slet en visning** – Brug handlingen **Fjern** til at slette den valgte visning permanent fra siden. Det er ikke muligt at gendanne en visning efter at have fjernet den.

De ændringer, der er foretaget i denne dialogboks, træder i kraft, når du vælger knappen **Opdater**.

## <a name="managing-personalizations-at-an-organizational-level-with-views"></a>Administrere personlige indstillinger på organisationsniveau med visninger

For at hjælpe dig med at forstå, hvordan gemte visninger er med til at forbedre administrationen af tilpasninger på et organisationsniveau, beskriver dette afsnit nogle forskelle i administration af personlige tilpasninger med og uden **Gemte visninger**.

Uden visninger skulle administratorer anvende et sæt tilpasninger på en side for en bruger, en gruppe af brugere via siden Tilpasning. Hvis disse brugere havde rettigheder til at tilpasse personlige indstillinger, blev tilpasningerne anvendt på den pågældende side. Men der var ikke nogen mulighed for at forhindre brugerne i at tilpasse siden yderligere, hvilket betød, at organisationen ikke kunne sikre, at brugerne havde en ensartet brugergrænseflade. Hvis nogen af disse brugere ikke havde rettigheder til personlig tilpasning, blev de tilpasninger, som de fik af en administrator, ikke indlæst. Hvis der desuden blev ansat nye brugere i en organisation, skulle administratorer manuelt indlæse et sæt tilpasninger for brugeren. Der var ikke nogen automatisk mekanisme til angivelse af, at et bestemt sæt tilpasninger skulle være tilgængeligt for brugere i den pågældende rolle.

Med funktionen **Gemte visninger** er det væsentligt lettere at administrere tilpasninger, primært på grund af muligheden for at publicere visninger til brugergrupper. Når en visning er blevet publiceret, kan alle brugere, der har en af de definerede sikkerhedsroller og adgang til en af de angivne juridiske enheder, se og bruge visningen, også selvom den pågældende bruger muligvis ikke kan tilpasse den. Selvom hver bruger har en kopi af den publicerede visning, hvor forbrugselementer på siden automatisk anvendes, kan ingen bruger gemme brugertilpasninger eller forespørge på opdateringer til en publiceret visning. Med andre ord er publicerede visninger låst. Hvis nye brugere får tildelt roller i juridiske enheder, som visninger er publiceret til, kan de automatisk se de visninger, der er knyttet til deres roller og juridiske enheder. Der kræves ingen yderligere handlinger af administratoren. På samme måde, hvis brugere ændrer roller i en organisation eller får adgang til forskellige juridiske enheder, kan de muligvis ikke længere få adgang til de visninger, der tidligere er publiceret til dem. Igen kræves der ikke yderligere handlinger af administratoren.

Opdateringer til en publiceret visning kan let distribueres til brugere ved igen at publicere visningen til de relevante sikkerhedsroller og juridiske enheder.

Publiceringsfunktionen giver organisationer mulighed for at definere de standardvisninger i firmaet, der er optimeret til deres virksomhed, målrettet brugere i bestemte sikkerhedsroller.

## <a name="publishing-views"></a>Publicere visninger

Under publiceringsprocessen kan visninger tildeles en eller flere sikkerhedsroller for en eller flere juridiske enheder. Derfor kan alle brugere, der har adgang til en juridisk enhed, og som er tildelt en af disse roller, få adgang til at bruge visningerne. Men brugeren kan ikke redigere visningerne. Systemadministratorer har som standard adgang til handlingen **Publicer** i rullemenuen til visningsvælgeren. Andre brugere, der er tillid til i organisationen, kan dog også få adgang til at se udgivelsen via den nye administratorrolle **Gemte visninger**.

Følg disse trin for at publicere en visning:

1. Opret og gem en personlig kopi af den visning, du vil publicere. 
2. Når denne visning indlæst skal du vælge navnet på visningen for at åbne visningsvælgerens rullemenu. 
3. Vælg knappen **Flere**, og vælg derefter **Publicer**. Dialogboksen **Publicer** åbnes.
4. Angiv et navn til visningen. Dette er det navn, som brugere, der modtager denne visning, får vist i deres visningsvælgere. Navnene på publicerede visninger for en side skal være entydige. Der tillades ingen dublerede navne, selvom listen over roller eller juridiske enheder, som visningerne gælder for, er forskellige.
5. Hvis funktionen **Understøttelse af oversættelse for organisationsvisninger** er aktiveret, kan du føje oversættelser for dit visningsnavn på så mange sprog, som organisationen har brug for, ved at vælge knappen **Oversættelser** ud for feltet **Navn**. Visningsnavnet vises derefter til brugerne på deres aktuelle sprog. Du kan også angive standardsproget for at angive den oversættelse, der skal vises til brugere, som kører sprog, der ikke er defineret oversættelse for.
5. Valgfrit: Angiv en beskrivelse af visningen, så brugere, der modtager denne visning, bedre kan forstå formålet med visningen. 
6. Afgør, om visningen skal publiceres som standardvisning for de valgte brugere. Når du gør en visning til standarden, vil brugerne se denne visning, næste gang de åbner destinationssiden. Den ene, globale standardvisning for alle målbrugere vil blive ændret. Brugerne kan dog stadig ændre deres standardvisning, når der er foretaget publicering.

    > [!NOTE]
    > Vær opmærksom på følgende funktionsmåde, når du publicerer en visning som standardvisning:
    >
    > - Hvis du publicerer en visning som standardvisning for nogle eller alle juridiske enheder, forekommer følgende funktionsmåde:
    >
    >    - Hvis det kun er basisfunktionen **Gemte visninger**, der er aktiveret, vil den globale visning blive ændret for hver målbruger. 
    >    - Hvis funktionen **Forbedret understøttelse af juridisk enhed for gemte visninger** er slået til, og du publicerer visningen til et undersæt af juridiske enheder, vil standardvisningen for disse juridiske enheder blive ændret for alle målbrugere.
    >
    > - Hvis en bruger har roller, hvor flere visninger er publiceret som standardvisning, vil den sidst publicerede visning blive brugt som brugerens standardvisning. 
    > - Udgivelse fungerer ikke for rolletildelinger, der er foretaget vha. AAD-grupper. 

8. Tilføj sikkerhedsroller, der svarer til de brugere, der skal have adgang til denne visning. 
9. Afgør, om du vil publicere visningen til de underordnede roller for de enkelte sikkerhedsroller, der er valgt. Hvis du gør det, skal du markere afkrydsningsfeltet **Medtag underordnede roller** i rækken for de relevante sikkerhedsroller. Bemærk, at dette afkrydsningsfelt ikke er tilgængeligt for roller, der ikke har underordnede roller.
10. Tilføj de juridiske enheder, som denne visning skal være tilgængelig for. 

    > [!NOTE]
    > Vær opmærksom på følgende funktionsmåde, hvis du publicerer en visning for en bestemt juridisk enhed, men du ikke publicerer visningen som standardvisning.
    >
    > - Hvis det kun er basisfunktionen **Gemte visninger**, der er aktiveret, viser brugerens visningsvælger for siden først visningen for de angivne juridiske enheder. Når visningen er indlæst for første gang, vil visningsvælgeren for siden altid vise den, uanset den juridiske enhed.
    > - Hvis funktionen **Forbedret understøttelse af juridisk enhed for gemte visninger** er aktiveret, viser visningsvælgeren kun visningen for de angivne juridiske enheder.

11. Vælg **Publicer**.

Bemærk, at det kan tage et stykke tid (op til en time) i nogle miljøer, før brugerne kan se den publicerede visning.

## <a name="modifying-a-published-view"></a>Redigere en publiceret visning

Når du har publiceret en visning, kan du opdage, at du vil ændre den. Selvom du ikke kan foretage direkte ændringer af en publiceret visning, fordi disse visninger er låst for redigering for alle brugere (også udgiverne), kan du publicere en visning igen for at opdatere den.

Hvis de ændringer, du vil foretage i en publiceret visning, kun omfatter publiceringsparametrene (navnet på og beskrivelsen af visningen, eller de sikkerhedsroller, visningen publiceres til), skal du gøre følgende:

1. Skift til den publicerede visning for de parametre, du vil opdatere. 
2. Vælg **Publicer igen** i visningsvælgerens rullemenu. Hvis du bruger version 10.0.12 eller tidligere, skal du vælge **Publicer** og derefter **Ja** for at opdatere den eksisterende visning.
3. Opdater navnet, beskrivelsen, sikkerhedsrollerne og juridiske enheder for visningen. 
4. Vælg **Publicer**. Hvis du oprindeligt har valgt denne publicerede visning som standardvisning, vil den være standardvisningen for brugere igen, når du har publiceret den igen. 

Hvis ændringerne af den publicerede visning omfatter redigeringer af de tilpasninger eller filtre, der er tilknyttet visningen, skal du følge disse trin.

1. Indlæs den publicerede visning, du vil ændre. 
2. Foretag de nødvendige ændringer i den lokale kladde.
3. Vælg **Publicer igen** i visningsvælgerens rullemenu.
4. Vælg **Ja** for at angive, at du vil publicere visningen sammen med de ændringer, der ikke er gemt. 
5. Juster eventuelle publiceringsparametre, der kræver justering, og vælg derefter **Publicer**. 

## <a name="managing-published-views"></a>Administrere publicerede visninger

Som ved administration af personlige visninger giver dialogboksen **Administrer mine visninger** brugerne med publiceringsrettigheder grundlæggende vedligeholdelsesfunktioner over den pågældende sides publiceringsvisninger (ud over deres egne personlige visninger). Når du vil åbne denne side, skal du vælge navnet på visningen for at åbne rullemenuen for visningsvælger, vælge **Flere** og derefter vælge **Administrer mine visninger**.

Mens alle brugere kan se fanen **Mine visninger** med deres personlige visninger, kan brugere med publiceringsrettigheder også se fanen **Organisationsvisninger**, der viser alle de publicerede og ikke-publicerede visninger for den pågældende side. Da der kan være flere brugere, der publicerer visninger, er det vigtigt, at du kan administrere den fulde liste over publicerede visninger, selvom du ikke er den bruger, der publicerede visningen.

Hvis du vil se listen over alle publicerede visninger for siden, kan du bruge følgende sæt handlinger. 

- **Publicer igen** – Brug handlingen **Publicer igen** til at publicere en visning igen, når publiceringsparametre (navn, beskrivelse, sikkerhedsroller eller juridiske enheder) er ændret.
- **Publicer** – Brug handlingen **Publicer** til at publicere en visning, der ikke er publiceret i øjeblikket. 
- **Annuller publicering** – Brug handlingen **Annuller publicering** til at gøre en visning inaktiv. Visningen vil stadig være tilgængelig i systemet, men brugerne kan ikke se den i visningsvælgeren, før visningen publiceres igen.
- **Gem som personlig** – Brug handlingen **Gem som personlig** til at oprette en personlig kladdekopi af den publicerede visning. Denne egenskab kan hjælpe dig med at forstå indholdet af en visning, der ikke blev publiceret til dig, eller som endnu ikke er publiceret. Du kan også bruge den til at redigere og derefter publicere en visning igen.
- **Slet** – Brug handlingen **Slet** til at slette en publiceret eller ikke-publiceret visning permanent. Denne handling fjerner også visningen for alle brugere i systemet. Når publicerede visninger fjernes, træder det i kraft, når knappen **Gem** er valgt. Når en visning er slettet, kan den ikke gendannes. 

## <a name="managing-views-globally"></a>Administrere visninger globalt

Selvom nogle administrationsmuligheder vises på alle sider som angivet i denne artikel, kan **systemadministratorer** og **gemte visningsadministratorer** administrere visninger mere enkelt for systemet via siden **Brugertilpasning**. Denne side indeholder bl. a. følgende afsnit og funktioner: 

- **Publicerede visninger** – i dette afsnit beskrives alle de visninger, der er publiceret for din organisation. Herfra kan du publicere en visning igen, efter at du har justeret de sikkerhedsroller eller juridiske enheder, som visningen er mål for. Du kan også eksportere, slette eller annullere publicering af visninger. Du kan bruge handlingen **Gem som personlig** til at oprette en personlig kopi af en visning, så du kan opdatere visningen eller få en bedre forståelse af dens indhold. 
- **Ikke-publicerede visninger** – I dette afsnit vises alle organisationsvisninger i systemet, der ikke aktuelt er publiceret. Disse visninger kommer oftest ind i systemet via importfunktionen. Du kan publicere, eksportere eller slette disse visninger. Handlingen **Hurtig publicering**, der blev tilføjet i version 10.0.12, gør det muligt at publicere flere visninger fra dette afsnit i én handling ved hjælp af de eksisterende konfigurationer af sikkerhedsroller og juridiske enheder. Du kan bruge handlingen **Gem som personlig** til at oprette personlige kopier af disse visninger, så du kan få en bedre forståelse af deres indhold.
- **Personlige visninger** – Dette afsnit beskriver alle de visninger, der er oprettet af brugere i systemet. Herfra kan du publicere en personlig visning i organisationen eller kopiere en eller flere af disse visninger til andre brugere. Du kan også eksportere eller slette disse visninger efter behov.
- **Brugerindstillinger** – Vælg en bruger, der skal vises, eller juster brugerens mulighed for brugertilpasning enten for hele systemet eller for bestemte sider, som brugeren har besøgt. Du kan se og arbejde interaktivt med brugerens tilpasninger i systemet. Du kan også slette alle tilpasninger for den pågældende bruger eller nulstille billedforklaringer for brugeren. Hvis billedforklaringer til funktioner nulstilles, bliver pop op-vinduer, der introducerede nye funktioner, og som brugeren tidligere har afvist, vist igen, næste gang brugeren støder på disse funktioner.
- **Systemindstillinger** - Du kan midlertidigt deaktivere tilpasninger for alle brugere i systemet. I dette tilfælde anvendes ingen tilpasninger for nogen bruger, og alle sider nulstilles til deres standardtilstand. Hvis du senere aktiverer tilpasninger igen, anvendes alle tilpasninger igen. Du kan også permanent slette alle tilpasninger for alle brugere i systemet. Det er ikke muligt at gendanne tilpasninger, som er blevet slettet. Før du udfører denne opgave, skal du derfor sørge for at eksportere de brugertilpasninger, som du eventuelt vil bruge senere.

Brugere, der har adgang til siden **Brugertilpasning**, kan også importere personlige visninger eller organisationsvisninger ved hjælp af knappen **Importér visninger** i handlingsruden. I forbindelse med organisationsvisninger kan du vælge **Publicer med det samme** for at gøre visningerne tilgængelige for brugere uden yderligere eksplicit publicering.

## <a name="known-issues"></a>Kendte problemer

Du kan få vist en liste over kendte problemer med gemte visninger ved at se [Opbygge formularer, der fuldt ud anvender gemte visninger](../../dev-itpro/user-interface/understanding-saved-views.md).

## <a name="frequently-asked-questions"></a>Ofte stillede spørgsmål

### <a name="how-do-i-enable-saved-views-in-my-environment"></a>Hvordan kan jeg aktivere gemte visninger i mit miljø?

> [!NOTE]
> Funktionen **Gemte visninger** kræver, at tilpasningssystemet i programmer til finans og drift er aktiveret. Hvis brugertilpasning er slået fra for hele miljøet, deaktiveres visningerne, også selvom du følger nedenstående trin. 

Du kan aktivere og deaktivere funktionen **Gemte visninger** via Funktionsstyring i alle miljøer. Når den er aktiveret, aktiveres gemte visninger i alle efterfølgende brugersessioner.

### <a name="what-happens-to-existing-personalizations-when-views-are-enabled"></a>Hvad sker der med eksisterende tilpasninger, når visninger er aktiveret? 

Når visninger er aktiveret, gemmes eventuelle eksisterende tilpasninger af en bruger og en formular i en ny visning kaldet **Min visning**, der automatisk indstilles som standardvisningen. Formålet med dette er, at der er en ensartet brugeroplevelse, før og efter at visninger aktiveres, bortset fra visningsvælgerkontrolelementet, der vises i formularer.

### <a name="what-pages-support-views"></a>Hvilke sider understøtter visninger? 

Visninger er tilgængelige på de fleste, men ikke på alle sider. Visninger er især aktuelt tilgængelige på alle fuldskærmssider bortset fra dashboards. Visningsunderstøttelse af arbejdsområder er tilgængelig via funktionen **Understøttelse af gemte visninger for arbejdsområder**. De fleste fuldskærmssider, som omfatter dialogbokse med rullelister, opslag og udvidede eksempler, understøtter i øjeblikket ikke visninger. Visningsunderstøttelse af dialogbokse er tilgængelig via funktionen **Understøttelse af gemte visninger for dialogbokse**.

### <a name="who-is-allowed-to-publish-views"></a>Hvem har tilladelse til at publicere visninger?

Kun systemadministratorer og brugere, der er tildelt administratorrollen **Gemte visninger**, har rettigheder til at publicere visninger. 

### <a name="why-am-i-not-able-to-save-filters-with-this-view"></a>Hvorfor kan jeg ikke gemme filtre i denne visning? 

Der er flere grunde til, at et filter muligvis ikke kan gemmes med en visning: 

- Siden understøtter muligvis ikke lagring af filtre som en del af visningsdefinitionen. Bemærk, at det kun er sider med store visningsvælgere, der tillader, at tilpasninger og forespørgselsændringer gemmes som en visning. Du kan finde flere oplysninger i afsnittet **Skifte visninger**. 
- Den pågældende side understøtter muligvis ikke visninger korrekt, da den kan ignorere visningsforespørgslen helt eller bruger en midlertidig tabel, hvis data ikke er vedholdende. 

### <a name="what-data-will-i-see-when-i-visit-a-page"></a>Hvilke data får jeg vist, når jeg besøger en side?

På sider med små visningsvælgere (kun personlige tilpasninger kan gemmes i visningen) kan du se de samme data som før, når du besøger siden. 

For sider med store visningsvælgere (både brugertilpasninger og forespørgsler kan gemmes i visningen) kan du typisk se de data, der er knyttet til den forespørgsel, som er knyttet til din standardvisning. Der findes to hovedundtagelser:

- Hvis du navigerer til en side fra et felt, udføres feltforespørgslen, uanset hvilken forespørgsel der er knyttet til standardvisningen. Hvis du har oprettet det pågældende felt, efter at visninger er blevet aktiveret, vil valg af et felt åbne siden med den visning, der er knyttet til feltet.
- Hvis du navigerer til en side, og dette adgangspunkt omfatter en forespørgsel, udføres den oprindelige forespørgsel i stedet for standardvisningens forespørgsel. Når dette sker, skulle du få besked om det, når visningen indlæses. Du kan også bekræfte ved at skifte til denne visning, når siden er indlæst, fordi visningsforespørgslen skulle kunne udføres under alle omstændigheder.

### <a name="why-is-a-view-that-was-published-for-a-specific-legal-entity-visible-in-all-legal-entities"></a>Hvorfor er en visning, der er publiceret for en bestemt juridisk enhed, synlig for alle juridiske enheder?

Hvis publicerer en visning for en bestemt juridisk enhed, men du ikke publicerer visningen som standardvisning, sker følgende:

- Hvis det kun er basisfunktionen **Gemte visninger**, der er aktiveret, viser brugerens visningsvælger for siden først visningen for de angivne juridiske enheder. Når visningen er indlæst for første gang, vil visningsvælgeren for siden altid vise den, uanset den juridiske enhed. Denne funktionsmåde forekommer, fordi brugere får deres egen personlige kopi af den publicerede visning, når den indlæses, og personlige visninger er globale.
- Hvis funktionen **Forbedret understøttelse af juridisk enhed for gemte visninger** er aktiveret, viser visningsvælgeren kun visningen for de angivne juridiske enheder. Denne funktionsmåde forekommer, fordi funktionen giver mulighed for at sammenkæde visninger (herunder personlige visninger) med bestemte juridiske enheder.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

