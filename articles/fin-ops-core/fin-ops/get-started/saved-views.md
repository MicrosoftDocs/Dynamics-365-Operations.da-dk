---
title: Gemte visninger
description: Dette emne beskriver, hvordan du bruger de gemte visningsfunktioner.
author: jasongre
manager: AnnBe
ms.date: 05/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: Platform update 28
ms.openlocfilehash: f6b7f1c64c273f52dc1d414185ba54efdfb8e5c0
ms.sourcegitcommit: dc67232c9aa3223d42f22cc1f7aafbd121e7e616
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/30/2020
ms.locfileid: "3412324"
---
# <a name="saved-views"></a>Gemte visninger

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="introduction"></a>Introduktion
Personlig tilpasning spiller en vigtig rolle, når brugere og organisationer skal have mulighed for at optimere brugeroplevelsen efter deres behov. Du kan finde oplysninger om brugertilpasning i [Tilpasse brugeroplevelsen](personalize-user-experience.md).

Med traditionel brugertilpasning havde brugerne kun et enkelt sæt tilpasninger pr. formular. Gemte visninger udvides ved tilpasning på flere vigtige måder:

-    I visningerne kan brugerne have flere navngivne sæt tilpasninger pr. formular, som de hurtigt kan skifte mellem efter behov. Det giver brugeren mulighed for at oprette flere optimerede visninger af en side, hvor hver visning er tilpasset til behovet, når brugeren udfører en bestemt forretningsopgave. 

-    Visninger, der oprettes til bestemte sidetyper, kan også indeholde brugertilføjede filtre eller sorteringer, som giver brugerne mulighed for hurtigt at vende tilbage til almindeligt filtrerede datasæt. Se afsnittet [Hvilke sider understøtter visninger](saved-views.md#what-pages-support-views) for at få yderligere oplysninger. 

-    Visninger kan publiceres til brugere i bestemte sikkerhedsroller og bestemte juridiske enheder. Derfor kan alle brugere, der har en bestemt rolle og adgang til en angivet juridisk enhed, få adgang til at bruge denne visning, også selvom den pågældende bruger muligvis ikke kan tilpasse den. Denne publiceringsfunktion giver organisationer mulighed for at definere de standardvisninger i firmaet, der er optimeret til deres virksomhed. Yderligere oplysninger finder du i afsnittet [Administrere tilpasninger på organisationsniveau med visninger](saved-views.md#managing-personalizations-at-an-organizational-level-with-views).

-    I modsætning til traditionelle tilpasninger gemmes visninger ikke automatisk, når en bruger udfører eksplicitte tilpasninger eller filtrerer en liste. Eksplicitte lagringer er påkrævede for at kunne oprette en visning før eller efter de ændringer, der er knyttet til den pågældende visning, og for at sikre, at visningsdefinitioner ikke utilsigtet ændres af filtre eller tilpasninger, der ikke er beregnet til brug i længere tid.  

-    Visninger kan føjes til arbejdsområder som felter, lister eller links. Derfor kan et filtreret datasæt placeres i et arbejdsområde, og brugerne kan knytte et sæt tilpasninger, der er relevante for det pågældende datasæt, med feltet eller linket.

## <a name="switching-between-views"></a>Skifte mellem visninger
Når visninger er aktiveret for et miljø, vil alle sider, der understøtter visninger, indeholde et skjult kontrolelement til valg af visninger i visningsområdet øverst i formularen, som viser navnet på den aktuelle visning.  

Visningsvælgeren har to størrelsesvariationer: 

-   **Store visningsvælgere**: Sider, der har en tydelig liste, har en større visningsvælger af forskellige årsager. Den vigtigste er, at den store visningsvælger angiver de sider, hvor visningen kan indeholde brugerdefinerede filtre. Der indgår filtre i visningerne, og derfor er den største vælger også påkrævet, fordi visningsnavnene ofte er den bedste beskrivelse af de data, der vises på skærmen, og forventningen er, at brugerne skifter mellem visninger ofte på disse sidetyper.  
 
-   **Små visningsvælgere**: alle andre formularer i fuld størrelse (med undtagelse af arbejdsområder og dashboardet) har en mindre visningsvælger, der vises ud for sidens billedtekst. Visningerne på disse sider indeholder kun tilpasninger (og ikke brugerdefinerede filtre). På disse sider er formularteksten eller posttitlen ofte de vigtigste oplysninger øverst i formularen. Den mindre størrelse afspejler også en lavere forventet frekvens for skift af visninger på disse sider. 
 
Hvis du klikker på visningsnavnet, åbnes visningsvælgeren med listen over tilgængelige visninger for denne side.

-    **Standardvisning**: **Standard**-visningen (tidligere kendt som den **klassiske** visning) er den oprindelige visning af siden, hvor der ikke anvendes eksplicitte tilpasninger.
-    **Personlige visninger**: Visningerne uden hængelåse repræsenterer dine personlige visninger. Dette er visninger, som enten du har oprettet, eller som er tildelt af en administrator.  
-    **Låste visninger**: Nogle visninger (f.eks. **Standard**-visningen og eventuelle visninger, der er udgivet til din rolle) har et hængelåssymbol ved siden af dem i visningsvælgeren. Dette symbol angiver, at du ikke kan redigere disse visninger. Implicitte tilpasninger, der afspejler sideforbruget, gemmes dog automatisk. Disse implicitte tilpasninger omfatter en ændring af bredden på en gitterkolonne eller udvidelse eller skjulning af et oversigtspanel. Du kan dog oprette en personlig visning, der er baseret på en låst visning, ved hjælp af handlingen **Gem som**, hvis du har rettigheder til personlige indstillinger.
-    **Nye visninger**: Publicerede visninger, der endnu ikke er åbnet, er afgrænset med et spark til venstre for visningsnavnet.  

Hvis du vil skifte til en anden visning, skal du først åbne visningsvælgeren og derefter vælge den visning, du vil indlæse. 

## <a name="creating-and-modifying-views"></a>Oprette og ændre visninger
I modsætning til traditionelle tilpasninger gemmes visninger ikke automatisk, når en bruger udfører eksplicitte tilpasninger (eller filtrerer en liste). Der kræves en eksplicit handling for at gemme disse ændringer i en visning. Det giver brugerfleksibilitet, så der kan oprettes en visning før eller efter de ændringer, der er knyttet til den pågældende visning, og sikrer også, at visningsdefinitioner ikke utilsigtet ændres af engangsfiltre eller tilpasninger. Bemærk, at implicitte tilpasninger (f.eks. når et oversigtspanel udvides eller skjules, eller bredden af en gitterkolonne ændres eller udvides) automatisk gemmes i den aktuelle visning, også i låste visninger. 

Hvis du vil sikre, at visningens aktuelle tilstand er kendt, når du begynder at foretage ændringer i en visning ved at udføre en eksplicit tilpasning eller filtrering, vises der en stjerne ud for navnet på den aktuelle visning, som angiver, at du ser på en ikke-gemt, ændret version af denne visning.

Hvis du vil gemme disse ændringer, skal du følge nedenstående trin.
1.  Vælg visningsnavnet for at åbne visningsvælgeren.
2.  Sådan redigeres den eksisterende visning:
     1. Vælg **Gem**. Bemærk, at denne handling ikke vil blive aktiveret for låste visninger. 
3.  Sådan oprettes en ny visning:
     1.    Vælg **Gem som**. 
     2.    Indtast et visningsnavn og evt. en beskrivelse.
     3.    Vælg **Gem**.

## <a name="changing-the-default-view"></a>Ændre standardvisningen
Standardvisningen er den visning, som systemet vil forsøge at åbne, første gang du navigerer til siden. Du skal indstille dette til den visning, du forventer at bruge oftest.  

For at ændre standardvisningen for en side skal du følge disse trin: 
1.  Skift til den visning, du bruger som standard. 
2.  Vælg visningsnavnet for at åbne visningsvælgeren. 
3.  Vælg **Flere** og derefter **Vælg som standard**.  

Når du opretter en ny visning (ved hjælp af handlingen **Gem som**), kan du også gøre den nye visning til standardvisningen ved at indstille **Vælg som standard**, før du gemmer visningen.

Bemærk, at i nogle tilfælde udføres den forespørgsel, der er knyttet til standardvisningen, ikke, første gang du navigerer til en side. Hvis du f.eks. navigerer via et felt til en side, udføres feltets forespørgsel, uanset hvilken forespørgsel der er knyttet til standardvisningen. Hvis du navigerer til en side med en standardvisning, som allerede har en defineret forespørgsel, udføres den oprindelige forespørgsel i stedet for standardvisningens forespørgsel. Når dette sker, får du besked om det, når visningen indlæses. Hvis du skifter visning, efter at siden er indlæst, skulle visningsforespørgslen blive udført som forventet. Fra og med version 10.0.10 platformopdatering 34 vil meddelelsen indeholde en integreret handling, der giver dig mulighed for at indlæse forespørgslen i standardvisningen direkte.

## <a name="managing-personal-views"></a>Administrere personlige visninger 
Dialogboksen **Administrer mine visninger** indeholder grundlæggende vedligeholdelsesfunktioner til dine personlige visninger og rækkefølgen af visninger i visningsvælgeren. Når du vil åbne denne side, skal du klikke på navnet på visningen for at åbne rullemenuen for visningsvælger, vælge **Flere** og derefter vælge **Administrer mine visninger**.  

Hvis du vil se en liste over tilgængelige visninger for den pågældende side, kan du bruge følgende sæt handlinger.  
-    **Ændre standardvisningen**: Brug handlingen **Vælg som standard** for at gøre den aktuelt fremhævede visning til standardvisning for denne side.  
-    **Omarranger dine visninger**: Brug handlingerne **Flyt op** og **Flyt ned** for at arrangere dine visninger i en bestemt rækkefølge.  
-    **Omdøb en visning**: Brug handlingen **Omdøb** til at ændre navnet på den aktuelt markerede personlige visning. Denne handling er slået fra for låste visninger. 
-    **Slet en visning**: Brug handlingen **Fjern** til at slette den markerede visning permanent fra siden. Det er ikke muligt at gendanne en visning efter at have fjernet den.  

De ændringer, der er foretaget i denne dialogboks, træder i kraft, når du vælger knappen **Gem**.

## <a name="managing-personalizations-at-an-organizational-level-with-views"></a>Administrere personlige indstillinger på organisationsniveau med visninger
For at hjælpe dig med at forstå, hvordan gemte visninger er med til at forbedre administrationen af tilpasninger på et organisationsniveau, beskriver dette afsnit nogle forskelle i administration af personlige tilpasninger med og uden gemte visninger.

Uden visninger skulle administratorer anvende et sæt tilpasninger på en side for en bruger, en gruppe af brugere via siden Tilpasning. Hvis disse brugere havde rettigheder til at tilpasse personlige indstillinger, blev tilpasningerne anvendt på den pågældende side. Men der var ikke nogen mulighed for at forhindre brugerne i at tilpasse siden yderligere, hvilket betød, at organisationen ikke kunne sikre, at brugerne havde en ensartet brugergrænseflade. Hvis nogen af disse brugere ikke havde rettigheder til personlig tilpasning, blev de tilpasninger, som de fik af en administrator, ikke indlæst. Hvis der desuden blev ansat nye brugere i en organisation, skulle administratorer manuelt indlæse et sæt tilpasninger for brugeren. Der var ikke nogen automatisk mekanisme til angivelse af, at et bestemt sæt tilpasninger skulle være tilgængeligt for brugere i den pågældende rolle.

Med funktionen Gemte visninger er det væsentligt lettere at administrere tilpasninger, primært på grund af muligheden for at publicere visninger til brugergrupper. Når en visning er blevet publiceret, kan alle brugere, der har en af de definerede sikkerhedsroller og adgang til en af de angivne juridiske enheder, få adgang til at se og bruge visningen, også selvom den pågældende bruger muligvis ikke kan tilpasse den. Selvom hver bruger har en kopi af den publicerede visning, hvor brug af siden (implicitte tilpasninger) automatisk anvendes, kan ingen bruger gemme eksplicitte tilpasninger eller forespørge på opdateringer til den publiceret visning. Med andre ord er publicerede visninger låst. Hvis nye brugere får roller i juridiske enheder, som visninger er publiceret til, kan de automatisk se de visninger, der er knyttet til deres roller og juridiske enheder. Der kræves ingen yderligere handlinger af administratoren. På samme måde, hvis brugere ændrer roller i en organisation eller får adgang til forskellige juridiske enheder, kan de muligvis ikke længere få adgang til de visninger, der tidligere er publiceret til dem. Igen kræves der ikke yderligere handlinger af administratoren.

Opdateringer til en publiceret visning kan let distribueres til brugere ved igen at publicere visningen til de relevante sikkerhedsroller og juridiske enheder.

Publiceringsfunktionen giver organisationer mulighed for at definere de standardvisninger i firmaet, der er optimeret til deres virksomhed, målrettet brugere i bestemte sikkerhedsroller.  

## <a name="publishing-views"></a>Publicere visninger
Under udgivelsesprocessen kan visninger tildeles en eller flere sikkerhedsroller for en eller flere juridiske enheder. Derfor kan alle brugere, der har adgang til en juridisk enhed, og som er tildelt en af disse roller, få adgang til at bruge visningerne, selvom de ikke kan redigere dem. Systemadministratorer har adgang til handlingen **Publicer** i rullemenuen til visningsvælgeren. Andre brugere, der er tillid til i organisationen, kan dog også få adgang til at se udgivelsen via den nye administratorrolle **Gemte visninger**.

Følg disse trin for at publicere en visning: 
1.  Opret og gem en personlig kopi af den visning, du vil publicere. 
2.  Når denne visning indlæst skal du vælge navnet på visningen for at åbne visningsvælgerens rullemenu. 
3.  Vælg knappen **Flere**, og vælg derefter **Publicer**. Dialogboksen Publicer åbnes.  
4.  Angiv et navn til og evt. en beskrivelse af visningen. Dette er det navn, som brugere, der modtager denne visning, får vist i deres visningsvælgere. Navnene på publicerede visninger for en side skal være entydige. Der tillades ingen dublerede navne, selvom listen over roller eller juridiske enheder, som visningerne gælder for, er forskellige.
5.  Tilføj sikkerhedsroller, der svarer til de brugere, der skal have adgang til denne visning.
6. Tilføj de juridiske enheder, som denne visning skal være tilgængelig for. 
7. [10.0.9/Platformopdatering 33 eller nyere] Afgør, om visningen skal udgives som standardvisning for de valgte brugere. Hvis du gør en visning til standarden, vil brugerne se denne visning, næste gang de åbner destinationssiden. Dette vil ændre standardvisningen for disse brugere. Brugerne kan dog stadig ændre deres standardvisning, når udgivelsen er foretaget.    
8.  Vælg **Publicer**.

Bemærk, at det kan tage et stykke tid (op til en time) i nogle miljøer, før brugerne kan se den publicerede visning.

## <a name="modifying-a-published-view"></a>Redigere en publiceret visning
Når du har publiceret en visning, kan du beslutte, at du vil foretage ændringer af en publiceret visning. Selvom du ikke kan foretage direkte ændringer i en publiceret visning, fordi disse visninger er låst for redigering for alle brugere (også udgiverne), kan du publicere en visning igen for at foretage opdateringer.  

Hvis de ændringer, du vil foretage i en publiceret visning, kun omfatter publiceringsparametrene (navnet på og beskrivelsen af visningen, eller de sikkerhedsroller, visningen publiceres til), skal du gøre følgende: 
1.  Skift til den publicerede visning for de parametre, du vil opdatere. 
2.  Vælg **Publicer** i visningsvælgerens rullemenu. 
3.  Vælg **Ja**, hvis du vil opdatere den eksisterende visning (eller **Nej**, hvis du vil publicere denne under et andet navn).
4.  Opdater navnet, beskrivelsen og/eller sikkerhedsrollerne for visningen. 
5.  Vælg **Publicer**. 
6.  [10.0.8/Platformopdatering 32 eller tidligere] Hvis du har opdateret navnet på den publicerede visning, skal du også slette den publicerede visning med det gamle navn (se afsnittet **Administrere publicerede visninger** for at få flere oplysninger). 
7. [10.0.9/Platformopdatering 33 eller nyere] Hvis du oprindeligt har valgt, at denne publicerede visning skal være standardvisningen, vil den blive standardvisningen for disse brugere igen efter genudgivelsen.  

Hvis ændringerne af den publicerede visning omfatter redigering af de tilpasninger eller filtre, der er tilknyttet visningen, skal du følge disse trin: 
1.  Indlæs den publicerede visning, du vil redigere. 
2.  Gem en kopi af den publicerede visning for at oprette en lokal kladde til den publicerede visning. 
3.  Rediger den lokale kladde med de nødvendige ændringer.
4.  Publicer visningen med det oprindelige navn. 

## <a name="managing-published-views"></a>Administrere publicerede visninger
Som ved administration af personlige visninger giver dialogboksen **Administrer mine visninger** brugerne med publiceringsrettigheder grundlæggende vedligeholdelsesfunktioner over den pågældende sides publiceringsvisninger (ud over deres egne personlige visninger). Når du vil åbne denne side, skal du vælge navnet på visningen for at åbne rullemenuen for visningsvælger, vælge **Flere** og derefter vælge **Administrer mine visninger**.

Mens alle brugere kan se fanen **Mine visninger** med deres personlige visninger, kan brugere med publiceringsrettigheder også se fanen **Publiceret**, der viser alle de publicerede visninger for den pågældende side. Da der kan være flere brugere, der publicerer visninger, er det vigtigt at kunne administrere den fulde liste over publicerede visninger, uanset om du var den bruger, der faktisk publicerede visningen.

Hvis du vil se listen over alle publicerede visninger for siden, kan du bruge følgende sæt handlinger. 

-    **Publicer** – Brug handlingen **Publicer** til at publicere en visning igen, når publiceringsparametre (navn, beskrivelse, sikkerhedsroller eller juridiske enheder) er ændret.
-    **Gem som personlig** – Brug handlingen **Gem som personlig** til at oprette en personlig kladdekopi af den publicerede visning. Denne egenskab kan hjælpe dig med at forstå indholdet af en visning, der ikke blev publiceret til dig, eller som endnu ikke er publiceret. Du kan også bruge den til at redigere og derefter publicere en visning igen. Denne funktion introduceres i version 10.0.12.  
-    **Fjern** – Brug handlingen **Fjern** til at slette en publiceret visning permanent. Denne handling fjerner visningen for alle brugere i systemet. Når publicerede visninger fjernes, træder det i kraft, når knappen **Gem** er valgt.

## <a name="managing-views-globally"></a>Administrere visninger globalt
Selvom nogle administrationsmuligheder vises på alle sider som angivet i dette emne, kan **systemadministratorer** og **gemte visningsadministratorer** administrere visninger mere enkelt for systemet via siden **Brugertilpasning**. Denne side indeholder bl. a. følgende afsnit og funktioner: 

- **Publicerede visninger** – i dette afsnit beskrives alle de visninger, der er publiceret for din organisation. Herfra kan du publicere en visning igen, efter at du har justeret de sikkerhedsroller eller juridiske enheder, som visningen er mål for. Du kan også eksportere eller slette en eller flere publicerede visninger. I version 10.0.12 og nyere kan du bruge handlingen **Gem som personlig** til at oprette en personlig kopi af visningen, så du kan opdatere visningen eller få en bedre forståelse af dens indhold. 
- **Ikke-publicerede visninger** – Dette afsnit beskriver alle de visninger, der er importeret til systemet, men som endnu ikke er publiceret. Du kan publicere, eksportere eller slette disse visninger. Handlingen **Hurtig publicering**, der blev tilføjet i version 10.0.12, gør det muligt at publicere flere visninger fra dette afsnit i én handling ved hjælp af de eksisterende konfigurationer af sikkerhedsroller og juridiske enheder. I version 10.0.12 og nyere kan du bruge handlingen **Gem som personlig** til at oprette personlige kopier af disse visninger, så du kan få en bedre forståelse af deres indhold.   
- **Personlige visninger** – Dette afsnit beskriver alle de visninger, der er oprettet af brugere i systemet. Herfra kan du publicere en personlig visning i organisationen eller kopiere en eller flere af disse visninger til andre brugere. Du kan også eksportere eller slette disse visninger efter behov.
- **Brugere** – Vælg en bruger for at få vist listen over sider, som brugeren har besøgt. Du kan derefter justere brugerens mulighed for at bruge brugertilpasning til bestemte sider eller til hele systemet. Du kan også importere, eksportere eller rydde en tilpasning for brugeren. Derudover kan du nulstille billedforklaringer til funktioner for brugeren. Hvis brugeren således tidligere har lukket pop op-vinduer, der introducerede nye funktioner, vises disse pop op-vinduer igen, næste gang brugeren støder på disse funktioner.
- **System** - Du kan midlertidigt deaktivere tilpasninger for alle brugere i systemet. I dette tilfælde slettes alle tilpasninger for alle brugere, og alle sider nulstilles til deres standardtilstand. Hvis du senere aktiverer tilpasninger igen, anvendes alle tilpasninger igen. Du kan også permanent slette alle tilpasninger for alle brugere i systemet. Det er ikke muligt at gendanne tilpasninger, som er blevet slettet. Før du udfører denne opgave, skal du derfor sørge for at eksportere de brugertilpasninger, som du eventuelt vil bruge senere.

Brugere, der har adgang til siden **Brugertilpasning**, kan også importere personlige visninger eller skabelonvisninger ved hjælp af knappen **Importér visninger** i handlingsruden. I version 10.0.12 og nyere er der tilføjet en mekanisme til øjeblikkelig publicering af visninger, når de importeres.  

## <a name="frequently-asked-questions"></a>Ofte stillede spørgsmål
### <a name="how-do-i-enable-saved-views-in-my-environment"></a>Hvordan kan jeg aktivere gemte visninger i mit miljø? 
> [!NOTE]
> Funktionen **Gemte visninger** kræver, at Finance and Operations-tilpasningssystemet er aktiveret. Hvis brugertilpasning er slået fra for hele miljøet, deaktiveres visningerne, også selvom du følger nedenstående trin. 

**10.0.9/Platform Update 33 og nyere** **Gemte visninger**-funktionen er tilgængelig direkte i funktionsstyring i et hvilket som helst miljø. Ligesom det er tilfældet med andre funktioner i prøveversioner, er aktivering af denne funktion i produktion underlagt [Supplerende aftale om vilkår for anvendelse](https://go.microsoft.com/fwlink/?linkid=2105274).  

**10.0.8/Platform update 32 og før** **Gemte visninger**-funktionen kan aktiveres i miljøer på niveau 1 (udvikling/test) og niveau 2 (sandkasse), hvis du vil foretage yderligere test- og designændringer ved at følge trinnene nedenfor.

1.  **Aktivér flyvningen**: Udfør følgende SQL-sætning: 

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, enabled, FLIGHTSERVICEID, PARTITION) VALUES('CLISavedViewsEnableFeature', 1, 0, 5637144576);`

2. **Nulstil IIS** for at rydde den statiske flighting-cache. 

3.  **Find funktionen**: Gå til arbejdsområdet **Funktionsstyring**. Hvis **Gemte visninger** ikke fremgår af listen, skal du vælge **Søg efter opdateringer**.   

4.  **Aktivér funktionen**: Find funktionen **Gemte visninger** på listen over funktioner, og vælg **Aktivér nu** i detaljeruden.

Alle efterfølgende brugersessioner vil starte med gemte visninger aktiveret.


### <a name="what-happens-to-existing-personalizations-when-views-are-enabled"></a>Hvad sker der med eksisterende tilpasninger, når visninger er aktiveret? 
Når visninger er aktiveret, gemmes eventuelle eksisterende tilpasninger af en bruger og en formular i en ny visning kaldet **Min visning**, der automatisk indstilles som standardvisningen. Formålet med dette er, at der er en ensartet brugeroplevelse, før og efter at visninger aktiveres, bortset fra visningsvælgerkontrolelementet, der vises i formularer.  

### <a name="what-pages-support-views"></a>Hvilke sider understøtter visninger? 
Visninger er tilgængelige på de fleste, men ikke på alle sider. Visninger er især aktuelt tilgængelige på alle fuldskærmssider bortset fra dashboards og arbejdsområder. Sider, der ikke vises som fuldskærmssider, og som omfatter dialogbokse, rullelister, opslag, udvidede eksempler, understøtter i øjeblikket ikke visninger. Understøttelse af visninger for yderligere sidetyper, f.eks. arbejdsområder og dialogbokse, kan komme i betragtning ved en senere opdatering.   

### <a name="who-is-allowed-to-publish-views"></a>Hvem har tilladelse til at publicere visninger?
Kun systemadministratorer og brugere, der er tildelt administratorrollen **Gemte visninger**, har rettigheder til at publicere visninger. 

### <a name="why-am-i-not-able-to-save-filters-with-this-view"></a>Hvorfor kan jeg ikke gemme filtre i denne visning? 
Der er flere grunde til, at et filter muligvis ikke kan gemmes med en visning: 

- Siden understøtter muligvis ikke lagring af filtre som en del af visningsdefinitionen. Bemærk, at det kun er sider med store visningsvælgere, der tillader, at tilpasninger og forespørgselsændringer gemmes som en visning. Du kan finde flere oplysninger i afsnittet **Skifte visninger**. 

- Den pågældende side understøtter muligvis ikke visninger korrekt, da den kan ignorere visningsforespørgslen helt eller bruger en midlertidig tabel, hvis data ikke er vedholdende. 

### <a name="what-data-will-i-see-when-i-visit-a-page"></a>Hvilke data får jeg vist, når jeg besøger en side? 
På sider med små visningsvælgere (kun personlige tilpasninger kan gemmes i visningen) kan du se de samme data som før, når du besøger siden. 

For sider med store visningsvælgere (tilpasninger og forespørgsler kan gemmes i visningen) kan du primært se de data, der er knyttet til den forespørgsel, som er knyttet til din standardvisning. Der er to hovedundtagelser fra dette: Hvis du navigerer til en side fra et felt, udføres feltforespørgslen, uanset hvilken forespørgsel der er knyttet til standardvisningen. Hvis du har oprettet det pågældende felt, efter at visninger er blevet aktiveret, vil valg af et felt åbne siden med den visning, der er knyttet til feltet.   
     - Hvis du navigerer til en side, og dette adgangspunkt omfatter en forespørgsel, udføres den oprindelige forespørgsel i stedet for standardvisningens forespørgsel. Når dette sker, skulle du få besked om det, når visningen indlæses. Du kan også bekræfte ved at skifte til denne visning, når siden er indlæst, fordi visningsforespørgslen skulle kunne udføres under alle omstændigheder.  


