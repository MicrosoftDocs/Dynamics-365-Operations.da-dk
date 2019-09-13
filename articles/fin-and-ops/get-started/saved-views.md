---
title: Gemte visninger
description: Dette emne beskriver, hvordan du bruger de gemte visningsfunktioner.
author: jasongre
manager: AnnBe
ms.date: 08/01/2019
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
ms.openlocfilehash: 43f25796e6271f14acfc72f931398ab63338a307
ms.sourcegitcommit: b068b17ef708a0b349db8df1542e4244bb983d13
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2019
ms.locfileid: "1870827"
---
# <a name="saved-views"></a>Gemte visninger

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="introduction"></a>Introduktion
Personlig tilpasning spiller en vigtig rolle, når brugere og organisationer skal have mulighed for at optimere brugeroplevelsen i Microsoft Dynamics 365 for Finance and Operations, så den opfylder deres behov. Du kan finde oplysninger om brugertilpasning i [Tilpasse brugeroplevelsen](personalize-user-experience.md).

Med traditionel brugertilpasning havde brugerne kun et enkelt sæt tilpasninger pr. formular. Gemte visninger udvides ved tilpasning på flere vigtige måder:

-    I visningerne kan brugerne have flere navngivne sæt tilpasninger pr. formular, som de hurtigt kan skifte mellem efter behov. Det giver brugeren mulighed for at oprette flere optimerede visninger af en side, hvor hver visning er tilpasset til behovet, når brugeren udfører en bestemt forretningsopgave. 

-    Visninger, der oprettes til bestemte sidetyper, kan også indeholde brugertilføjede filtre eller sorteringer, som giver brugerne mulighed for hurtigt at vende tilbage til almindeligt filtrerede datasæt. Se afsnittet [Hvilke sider understøtter visninger](saved-views.md#what-pages-support-views) for at få yderligere oplysninger. 

-    Visninger kan publiceres til sikkerhedsroller, hvilket betyder, at alle brugere med den pågældende rolle kan få adgang til og bruge denne visning, uanset brugerens øvrige tilpasningsmuligheder. Denne publiceringsfunktion giver organisationer mulighed for at definere de standardvisninger i firmaet, der er optimeret til deres virksomhed. Yderligere oplysninger finder du i afsnittet [Administrere tilpasninger på organisationsniveau med visninger](saved-views.md#managing-personalizations-at-an-organizational-level-with-views).

-    I modsætning til traditionelle tilpasninger gemmes visninger ikke automatisk, når en bruger udfører eksplicitte tilpasninger eller filtrerer en liste. Eksplicitte lagringer er påkrævede for at kunne oprette en visning før eller efter de ændringer, der er knyttet til den pågældende visning, og for at sikre, at visningsdefinitioner ikke utilsigtet ændres af filtre eller tilpasninger, der ikke er beregnet til brug i længere tid.  

## <a name="switching-between-views"></a>Skifte mellem visninger
Når visninger er aktiveret for et miljø, vil alle sider, der understøtter visninger, indeholde et skjult kontrolelement til valg af visninger i visningsområdet øverst i formularen, som viser navnet på den aktuelle visning.  

Visningsvælgeren har to størrelsesvariationer: 

-   **Store visningsvælgere**: Sider, der har en tydelig liste, har en større visningsvælger af forskellige årsager. Den vigtigste er, at den store visningsvælger angiver de sider, hvor visningen kan indeholde brugerdefinerede filtre. Der indgår filtre i visningerne, og derfor er den største vælger også påkrævet, fordi visningsnavnene ofte er den bedste beskrivelse af de data, der vises på skærmen, og forventningen er, at brugerne skifter mellem visninger ofte på disse sidetyper.  
 
-   **Små visningsvælgere**: alle andre formularer i fuld størrelse (med undtagelse af arbejdsområder og dashboardet) har en mindre visningsvælger, der vises ud for sidens billedtekst. Visningerne på disse sider indeholder kun tilpasninger (og ikke brugerdefinerede filtre). På disse sider er formularteksten eller posttitlen ofte de vigtigste oplysninger øverst i formularen. Den mindre størrelse afspejler også en lavere forventet frekvens for skift af visninger på disse sider. 
 
Hvis du klikker på visningsnavnet, åbnes visningsvælgeren med listen over tilgængelige visninger for denne side.

-    **Klassisk visning**: Den klassiske visning er out-of-the-box-visningen af siden, hvor der ikke er anvendt eksplicitte brugertilpasninger.  
-    **Personlige visninger**: Visningerne uden hængelåse repræsenterer dine personlige visninger. Dette er visninger, som enten du har oprettet, eller som er tildelt af en administrator.  
-    **Låste visninger**: Nogle visninger (som f.eks. klassisk visning og visninger, der måtte være udgivet til din rolle) har en hængelås i visningsvælgeren som tegn på, at de ikke kan redigeres. Implicitte tilpasninger, som afspejler sidens anvendelse, gemmes dog automatisk, f.eks. når bredden af en gitterkolonne ændres, eller et oversigtspanel udvides eller skjules. Du kan dog oprette en personlig visning, der er baseret på en låst visning, ved hjælp af handlingen **Gem en kopi**, hvis du har rettigheder til personlige indstillinger.
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
     1.    Vælg **Gem en kopi**. 
     2.    Indtast et visningsnavn og evt. en beskrivelse.
     3.    Vælg **Gem**.

## <a name="changing-the-default-view"></a>Ændre standardvisningen
Standardvisningen er den visning, som systemet vil forsøge at åbne, første gang du navigerer til siden. Du skal indstille dette til den visning, du forventer at bruge oftest.  

For at ændre standardvisningen for en side skal du følge disse trin: 
1.  Skift til den visning, du bruger som standard. 
2.  Vælg visningsnavnet for at åbne visningsvælgeren. 
3.  Vælg **Flere** og derefter **Vælg som standard**.  

Når du opretter en ny visning (ved hjælp af handlingen **Gem en kopi**), kan du også gøre den nye visning til standardvisningen ved at indstille **Vælg som standard**, før du gemmer visningen.  

Bemærk, at i nogle tilfælde udføres den forespørgsel, der er knyttet til standardvisningen, ikke, første gang du navigerer til en side. Hvis du f.eks. navigerer via et felt til en side, udføres feltets forespørgsel, uanset hvilken forespørgsel der er knyttet til standardvisningen. Hvis du navigerer til en side, hvis klassiske visning allerede har en defineret forespørgsel, udføres den oprindelige forespørgsel i stedet for standardvisningens forespørgsel. Når dette sker, får du besked om det, når visningen indlæses. Hvis du skifter visning, efter at siden er indlæst, skulle visningsforespørgslen blive udført som forventet.

## <a name="managing-personal-views"></a>Administrere personlige visninger 
Dialogboksen **Administrer mine visninger** indeholder grundlæggende vedligeholdelsesfunktioner til dine personlige visninger og rækkefølgen af visninger i visningsvælgeren. Når du vil åbne denne side, skal du klikke på navnet på visningen for at åbne rullemenuen for visningsvælger, vælge **Flere** og derefter vælge **Administrer mine visninger**.  

Hvis du vil se en liste over tilgængelige visninger for den pågældende side, kan du bruge følgende sæt handlinger.  
-    **Ændre standardvisningen**: Brug handlingen **Vælg som standard** for at gøre den aktuelt fremhævede visning til standardvisning for denne side.  
-    **Omarranger dine visninger**: Brug handlingerne **Flyt op** og **Flyt ned** for at arrangere dine visninger i en bestemt rækkefølge.  
-    **Omdøb en visning**: Brug handlingen **Omdøb** til at ændre navnet på den aktuelt markerede personlige visning. Denne handling er slået fra for låste visninger. 
-    **Slet en visning**: Brug handlingen **Fjern** til at slette den markerede visning permanent fra siden. Det er ikke muligt at gendanne en visning efter at have fjernet den.  

De ændringer, der er foretaget i denne dialogboks, træder i kraft, når du vælger knappen **Gem**.

## <a name="managing-personalizations-at-an-organizational-level-with-views"></a>Administrere personlige indstillinger på organisationsniveau med visninger
For at forstå forbedringerne af administrationen af personlige indstillinger på et organisationsniveau skal du først se på, hvordan administration af personlige indstillinger fungerede før visninger.  

Uden visninger skulle administratorer anvende et sæt tilpasninger på en side for en bruger, en gruppe af brugere via siden Tilpasning. Hvis disse brugere havde rettigheder til at tilpasse personlige indstillinger, blev tilpasningerne anvendt på den pågældende side. Men der var ikke nogen mulighed for at forhindre brugerne i at tilpasse siden yderligere, hvilket betød, at organisationen ikke kunne sikre, at brugerne havde en ensartet brugergrænseflade. Hvis nogen af disse brugere ikke havde rettigheder til personlig tilpasning, blev de tilpasninger, som de fik af en administrator, ikke indlæst. Hvis der desuden blev ansat nye brugere i en organisation, skulle administratorer manuelt indlæse et sæt tilpasninger for brugeren. Der var ikke nogen automatisk mekanisme til angivelse af, at et bestemt sæt tilpasninger skulle være tilgængeligt for brugere i den pågældende rolle.

Med funktionen Gemte visninger er det væsentligt lettere at administrere tilpasninger, primært på grund af muligheden for at publicere visninger til sikkerhedsroller. Når en visning er publiceret, kan alle brugere med den pågældende rolle kan få adgang til visningen og bruge den, uanset brugerens øvrige tilpasningsmuligheder. Hver bruger har en kopi af den publicerede visning, hvor brug af siden (implicitte tilpasninger) automatisk anvendes, og ingen bruger kan gemme eksplicitte tilpasninger eller opdateringer af forespørgslen i den publiceret visning (dvs. at publicerede visninger er låst). Hvis nye brugere derudover får tildelt en rolle, som visningen er publiceret til, får de automatisk vist de visninger, der er knyttet til deres rolle, uden administratorhandlinger. Hvis en bruger ændrer roller i en organisation, vil de visninger, der er knyttet til vedkommendes gamle rolle, ikke længere være tilgængelige for dem. Også dette sker uden administratorhandlinger. Opdateringer til en publiceret visning kan let distribueres til brugere ved igen at publicere visningen til de relevante sikkerhedsroller.

Publiceringsfunktionen giver organisationer mulighed for at definere de standardvisninger i firmaet, der er optimeret til deres virksomhed, målrettet brugere i bestemte sikkerhedsroller.  

## <a name="publishing-views"></a>Publicere visninger
Under publiceringsprocessen kan visninger tildeles til en eller flere sikkerhedsroller, hvilket betyder, at alle brugere med den pågældende rolle kan få adgang til og bruge denne visning, men de kan ikke redigere visningen. I øjeblikket er det kun systemadministratorer, der har rettigheder til handlingen **Udgiv** i rullemenuen for visningsvælger, men en ny sikkerhedsrolle vil være tilgængelig i en fremtidig opdatering for at give publiceringsrettigheder til andre betroede brugere.  

Følg disse trin for at publicere en visning: 
1.  Opret og gem en personlig kopi af den visning, du vil publicere. 
2.  Når denne visning indlæst skal du vælge navnet på visningen for at åbne visningsvælgerens rullemenu. 
3.  Vælg knappen **Flere**, og vælg derefter **Publicer**. Dialogboksen Publicer åbnes.  
4.  Angive et navn til og evt. en beskrivelse af visningen. Dette er det navn, som brugere, der modtager denne visning, får vist i deres visningsvælgere. Bemærk, at identiske navne til publicerede visninger for en side ikke er tilladt, selvom listen over roller, som de anvendes på, er anderledes.  
5.  Tilføj eventuelle sikkerhedsroller, der svarer til de brugere, der skal have denne visning.  
6.  Vælg **Publicer**.

Bemærk, at det kan tage et stykke tid (op til en time) i nogle miljøer, før brugerne kan se den publicerede visning.

## <a name="modifying-a-published-view"></a>Redigere en publiceret visning
Når du har publiceret en visning, kan du beslutte, at du vil foretage ændringer af en publiceret visning. Selvom du ikke kan foretage direkte ændringer i en publiceret visning, fordi disse visninger er låst for redigering for alle brugere (også udgiverne), kan du publicere en visning igen for at foretage opdateringer.  

Hvis de ændringer, du vil foretage i en publiceret visning, kun omfatter publiceringsparametrene (navnet på og beskrivelsen af visningen, eller de sikkerhedsroller, visningen publiceres til), skal du gøre følgende: 
1.  Skift til den publicerede visning for de parametre, du vil opdatere. 
2.  Vælg **Publicer** i visningsvælgerens rullemenu. 
3.  Vælg **Ja**, hvis du vil opdatere den eksisterende visning (eller **Nej**, hvis du vil publicere denne under et andet navn).
4.  Opdater navnet, beskrivelsen og/eller sikkerhedsrollerne for visningen. 
5.  Vælg **Publicer**. 
6.  Hvis du har opdateret navnet på den publicerede visning, skal du også slette den publicerede visning med det gamle navn (se afsnittet **Administrere publicerede visninger** for at få flere oplysninger). 

Hvis ændringerne af den publicerede visning omfatter redigering af de tilpasninger eller filtre, der er tilknyttet visningen, skal du følge disse trin: 
1.  Skift til den publicerede visning, du vil redigere. 
2.  Gem en kopi af den publicerede visning for at oprette en lokal kladde til den publicerede visning. 
3.  Rediger den lokale kladde med de nødvendige ændringer.
4.  Publicer visningen med det oprindelige navn. 

## <a name="managing-published-views"></a>Administrere publicerede visninger
Som ved administration af personlige visninger giver dialogboksen **Administrer mine visninger** brugerne med publiceringsrettigheder grundlæggende vedligeholdelsesfunktioner over den pågældende sides publiceringsvisninger (ud over deres egne personlige visninger). Når du vil åbne denne side, skal du vælge navnet på visningen for at åbne rullemenuen for visningsvælger, vælge **Flere** og derefter vælge **Administrer mine visninger**.

Mens alle brugere kan se fanen **Mine visninger** med deres personlige visninger, kan brugere med publiceringsrettigheder også se fanen **Publiceret**, der viser alle de publicerede visninger for den pågældende side. Da der kan være flere brugere, der publicerer visninger, er det vigtigt at kunne administrere den fulde liste over publicerede visninger, uanset om du var den bruger, der faktisk publicerede visningen.

Hvis du vil se listen over alle publicerede visninger for siden, kan du bruge følgende sæt handlinger. 

-    **Publicer**: Brug handlingen **Publicer** til at publicere en visning med ændrede publiceringsparametre (navn, beskrivelse, sikkerhedsroller).  
-    **Fjern**: Brug handlingen **Fjern** til at slette en publiceret visning permanent. Denne handling fjerner visningen for alle brugere i systemet.  
 
De ændringer, der er foretaget i denne dialogboks, træder i kraft, når knappen **Gem** vælges.

## <a name="frequently-asked-questions"></a>Ofte stillede spørgsmål
### <a name="how-do-i-enable-saved-views-in-my-environment"></a>Hvordan kan jeg aktivere gemte visninger i mit miljø? 
Hvis du vil aktivere gemte visninger, mens funktionen er i eksempelvisning, skal du følge trinnene nedenfor: 

1.  **Aktivér flyvningen**: Udfør følgende SQL-sætning: 

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, enabled, FLIGHTSERVICEID, PARTITION) VALUES('CLISavedViewsEnableFeature', 1, 0, 5637144576);`

2. **Nulstil IIS** for at rydde den statiske flighting-cache. 

3.  **Find funktionen**: Gå til arbejdsområdet **Funktionsstyring**. Hvis **Gemte visninger** ikke fremgår af listen, skal du vælge **Søg efter opdateringer**.   

4.  **Aktivér funktionen**: Find funktionen **Gemte visninger** på listen over funktioner, og vælg **Aktivér nu** i detaljeruden.

Alle efterfølgende brugersessioner vil starte med gemte visninger aktiveret.  

Bemærk, at hvis brugertilpasning er slået fra for miljøet, deaktiveres visningerne, også selvom du følger ovenstående trin. Det skyldes, at visningsfunktionen er bygget oven på tilpasningsundersystemet.

### <a name="what-happens-to-existing-personalizations-when-views-are-enabled"></a>Hvad sker der med eksisterende tilpasninger, når visninger er aktiveret? 
Når visninger er aktiveret, gemmes eventuelle eksisterende tilpasninger af en bruger og en formular i en ny visning kaldet **Min visning**, der automatisk indstilles som standardvisningen. Formålet med dette er, at der er en ensartet brugeroplevelse, før og efter at visninger aktiveres, bortset fra visningsvælgerkontrolelementet, der vises i formularer.  

### <a name="what-pages-support-views"></a>Hvilke sider understøtter visninger? 
Visninger er tilgængelige på de fleste men ikke på alle sider i Finance and Operations. Visninger er især aktuelt tilgængelige på alle fuldskærmssider bortset fra dashboards og arbejdsområder. Sider, der ikke vises som fuldskærmssider, og som omfatter dialogbokse, rullelister, opslag, udvidede eksempler, understøtter i øjeblikket heller ikke visninger. Understøttelse af visninger for yderligere sidetyper, f.eks. arbejdsområder og dialogbokse, kan komme i betragtning ved en senere opdatering.   

### <a name="who-is-allowed-to-publish-views"></a>Hvem har tilladelse til at publicere visninger?
Aktuelt er systemadministratorer de eneste brugere, der har rettigheder til at publicere visninger.  Der planlægges en ny sikkerhedsrolle i en kommende opdatering, som giver kunderne større fleksibilitet mht., hvem der kan publicere.  

### <a name="why-am-i-not-able-to-save-filters-with-this-view"></a>Hvorfor kan jeg ikke gemme filtre i denne visning? 
Der er flere grunde til, at et filter muligvis ikke kan gemmes med en visning: 

- Siden understøtter muligvis ikke lagring af filtre som en del af visningsdefinitionen. Bemærk, at det kun er sider med store visningsvælgere, der tillader, at tilpasninger og forespørgselsændringer gemmes som en visning. Du kan finde flere oplysninger i afsnittet "Skifte visninger". 

- Hvis visningen er standardvisningen, og navigationsstien til siden omfatter en forespørgsel, anvendes visningsforespørgslen muligvis ikke i starten. De to primære scenarier for dette er: 
     - Hvis du navigerer til en side fra et felt, udføres feltforespørgslen, uanset hvilken forespørgsel der er knyttet til standardvisningen. 
     - Hvis du navigerer til en side, og dette adgangspunkt omfatter en forespørgsel, udføres den oprindelige forespørgsel i stedet for standardvisningens forespørgsel. 
     
  Du skulle få besked, når visningen indlæses, i sådanne situationer. Du kan også bekræfte ved at skifte til denne visning, når siden er indlæst, fordi visningsforespørgslen skulle kunne udføres under alle omstændigheder.  

- Den pågældende side understøtter muligvis ikke visninger korrekt, da den kan ignorere visningsforespørgslen helt eller bruger en midlertidig tabel, hvis data ikke er vedholdende. 
