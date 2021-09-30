---
title: Gitteregenskaber
description: I dette emne beskrives flere stærke funktioner i gitterkontrolelementet. Den nye gitterfunktion skal være aktiveret for at få adgang til disse egenskaber.
author: jasongre
ms.date: 09/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 9aa79e6e61f3a53073dffa5f3030892cc921d246
ms.sourcegitcommit: 24e20b3b96834b23311f1bf5dbab28baf3323728
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/08/2021
ms.locfileid: "7483848"
---
# <a name="grid-capabilities"></a>Gitteregenskaber

[!include [banner](../includes/banner.md)]


Det nye gitterkontrolelement omfatter en række nyttige og effektive funktioner, du kan bruge til at forbedre brugernes produktivitet, oprette mere interessante visninger af dine data og få meningsfuld indsigt i dine data. Denne artikel dækker følgende funktioner: 

-  Beregner totaler
-  Skrive forud i forhold til systemet
-  Evaluere matematiske udtryk 
-  Gruppere data i tabelformat (aktiveres separat ved hjælp af funktionen **Gruppering i gitre**)
-  Fryse kolonner

## <a name="calculating-totals"></a>Beregner totaler
I Finance and Operations-apps har brugerne mulighed for at få vist totaler nederst i numeriske kolonner i gitre. Disse totaler vises i en sektion med sidefod nederst i gitteret. 

### <a name="showing-the-grid-footer"></a>Visning af gitterets sidefod
Der er et sidefodsområde i bunden af alle tabelgitre i Finance and Operations-apps. Sidefoden kan vise værdifulde oplysninger, der er relateret til de data, der vises i gitteret. Her er nogle eksempler på sådanne oplysninger:

- Antallet af markerede rækker i tabellen (når du markerer mere end én post)
- Samlede beløb nederst i konfigurerede og numeriske kolonner
- Antallet af rækker i datasættet 

Denne sidefod er som standard skjult, men du kan slå den til. Hvis du vil have vist sidefoden for et gitter, skal du højreklikke på kolonneoverskriften i gitteret og vælge indstillingen **Vis sidefod**. Når du har aktiveret sidefoden i et bestemt gitter, huskes denne indstilling, indtil brugeren vælger at skjule sidefoden. Hvis du vil skjule sidefoden, skal du højreklikke på kolonneoverskriften og vælge **Skjul sidefod**.  Placeringen af handlingen **Vis sidefod/Skjul sidefod** kan blive flyttet til en ny placering i en senere opdatering. 

### <a name="specifying-columns-with-totals"></a>Angive kolonner med totaler
Aktuelt viser ingen kolonner som standard totaler. Dette betragtes i stedet for som en aktivitet til engangsopsætning, der svarer til at justere kolonnebredden i gitre. Når du har angivet, at du vil have vist totaler for en kolonne, vil denne indstilling blive husket, næste gang du besøger siden.  

Du kan konfigurere en kolonne på to måder for at vise en total: 

- Højreklik i den kolonne, som du ønsker at se en total for, og vælg dernæst **Total for denne kolonne**. Denne handling resulterer i tre hændelser:

    1. Sidefoden bliver synlig. 
    2. Din præference om at få vist en total for denne kolonne gemmes. 
    3. En beregning af totaler for denne kolonne og alle andre kolonner, som du tidligere har konfigureret for at få vist totaler, indledes. Den tid, der kræves for at få vist en total, afhænger af størrelsen på det datasæt, du vil beregne totalen for.

- Når sidefoden er synlig, skal du vælge **Vis tabel** i sidefodsområdet nederst i den kolonne, du vil have vist en total for. Hvis der ikke er nogen konfigurerede kolonner, vil knappen **Vis total** være tilgængelig for alle numeriske kolonner. 

    Når der er konfigureret mindst én kolonne til totaler, er knapperne **Vis total** kun tilgængelige, når der peges eller fokuseres. Ved at vælge **Vis total** gemmer du din præference for at få vist en total i denne kolonne, således at præferencen anvendes under fremtidige besøg på siden. I sidefoden er denne status angivet med en tankestreg, der vises i kolonnen. (Hvis datasættet er lille nok, vises totalen i stedet med det samme.)

Hvis du laver en fejl og ikke længere vil have vist en total i en bestemt kolonne, skal du højreklikke på kolonnen og vælge **Skjul total** eller vælge knappen **Skjul total** i sidefoden i den pågældende kolonne. Denne præference vil også blive gemt til fremtidige besøg på siden. 

### <a name="calculating-totals"></a>Beregner totaler
Når du kommer til en side, hvor sidefoden er synlig, og der allerede er konfigureret kolonner for totaler, vises totalerne muligvis ikke i sidefoden. Funktionsmåden afhænger af størrelsen af datasættet på siden. Hvis datasættet er tilstrækkeligt lille, vises totaler automatisk sammen med antallet af rækker i datasættet. Hvis der er bindestreger i sidefoden under de kolonner, du har konfigureret til totaler, er datasættet for stort til, at systemet kan vise totaler med det samme, og der skal udføres en eksplicit handling for at beregne totalerne. Det gør du ved at klikke på knappen **Beregn** i sidefoden eller højreklikke på en kolonne, du vil beregne totalen for, og vælge **Total for denne kolonne**.  

Hvis beregningen tager for lang tid, kan du annullere operationen ved at klikke på knappen **Annuller**. Nogle gange vil datasættet imidlertid være for stort til at kunne beregne totaler (en begrænsning, der er pålagt af organisationen), og du vil i stedet blive mindet om at filtrere dine data mere.

Totaler opdateres automatisk, efterhånden som du opdaterer, sletter eller opretter rækker i datasættet.  

## <a name="typing-ahead-of-the-system"></a>Skrive forud i forhold til systemet
I mange forretningsscenarier er muligheden for hurtigt at indtaste data i systemet meget vigtig. Før det nye gitterkontrolelement blev introduceret, kunne brugerne kun ændre data i den aktuelle række. Før de kunne oprette en ny række eller skifte til en anden række, var de tvunget til at vente på, at systemet havde valideret eventuelle ændringer. I et forsøg på at reducere den mængde tid, som brugerne venter på, at disse valideringer udføres, og for at forbedre brugerproduktiviteten justerer det nye gitter disse valideringer, så de er asynkrone. Brugeren kan derfor flytte til andre rækker for at foretage ændringer, mens tidligere valideringer af rækker venter. 

For at understøtte denne nye funktionsmåde er der tilføjet en ny kolonne for rækkestatus til højre for kolonnen for rækkevalg, når gitteret er i redigeringstilstand. Denne kolonne angiver en af følgende statusser:

- **Tom** – Intet statusbillede angiver, at rækken er blevet gemt af systemet.
- **Afventer behandling** – Denne status angiver, at ændringerne i rækken endnu ikke er gemt af serveren, men de er i en kø med ændringer, der skal behandles. Før du udfører en handling uden for gitteret, skal du vente på, at alle ventende ændringer behandles. Desuden er teksten i disse rækker kursiv for at angive den ikke-gemte status for rækkerne. 
- **Ugyldig tilstand** – Denne status angiver, at der blev udløst en eller anden advarsel eller meddelelse under behandlingen af rækken, og det kan have forhindret systemet i at gemme ændringerne i den pågældende række. I det gamle gitter blev du tvunget tilbage til rækken for at løse problemet med det samme, hvis gemmehandlingen ikke lykkedes. Men i det nye gitter får du besked om, at der er opstået et valideringsproblem, men du kan beslutte, hvornår eventuelle problemer skal løses i rækken. Når du er klar til at løse et problem, kan du manuelt flytte fokus tilbage til rækken. Du kan også vælge funktionen **Løs dette problem**. Denne handling flytter øjeblikkeligt fokus tilbage til den række, hvor problemet er, og giver dig mulighed for at foretage ændringer i eller uden for gitteret. Bemærk, at behandlingen af efterfølgende ventende rækker standses, indtil denne valideringsadvarsel er løst. 
- **Midlertidigt afbrudt** – Denne status angiver, at behandlingen af serveren er sat på pause, fordi validering af rækken udløste en pop op-dialogboks, der kræver brugerinput. Da brugeren måske indtaster data i en anden række, vises pop op-dialogboksen ikke med det samme for den pågældende bruger. Den vises i stedet, når brugeren vælger at genoptage behandlingen. Denne status er ledsaget af en besked, der oplyser brugeren om situationen. Beskeden indeholder handlingen **Fortsæt behandling**, der vil udløse pop op-dialogboksen.  
    
Når brugerne indtaster data før det sted, hvor serveren behandler data, kan de forvente en række degraderinger i dataindtastningsoplevelsen, f.eks. manglende opslag, validering på kontrolniveau og indtastning af standardværdier. Brugere, der har brug for en rulleliste til at finde en værdi, anbefales at vente på, at serveren når til den aktuelle række. Validering på kontrolniveau og angivelse af standardværdier vil også finde sted, når serveren behandler den pågældende række.   

### <a name="pasting-from-excel"></a>Indsætning fra Excel
Brugerne har altid været i stand til at eksportere data fra gitre i Finance and Operations-apps til Excel ved hjælp af mekanismen **Eksportér til Excel**. Muligheden for at indtaste data forud i systemet gør det dog muligt for det nye gitter at understøtte kopiering af tabeller fra Excel og indsætning af dem direkte i gitre i Finance and Operations-apps. Den gittercelle, som indsætningen er initieret fra, bestemmer, hvor den kopierede tabel begynder at blive indsat. Indholdet af gitteret overskrives med indholdet af den kopierede tabel, undtagen i to tilfælde:

- Hvis antallet af kolonner i den kopierede tabel overstiger antallet af kolonner, der er tilbage i gitteret, startende fra indsætningens sted, får brugeren besked om, at de ekstra kolonner er blevet ignoreret. 
- Hvis antallet af rækker i den kopierede tabel overstiger antallet af rækker i gitteret med start fra indsætningens sted, overskrives de eksisterende celler af det indsatte indhold, og eventuelle ekstra rækker fra den kopierede tabel indsættes som nye rækker nederst i gitteret. 

## <a name="evaluating-math-expressions"></a>Evaluere matematiske udtryk
Som en produktivitetsbooster kan brugerne indtaste matematiske formler i numeriske celler i et gitter. De behøver ikke at foretage beregningen i en app uden for systemet. Hvis du f.eks. angiver **=15\*4** og derefter trykker på tasten **Tab** for at flytte ud af feltet, evalueres udtrykket, og værdien **60** gemmes for feltet.

Hvis du vil have systemet til at genkende en værdi som et udtryk, skal du starte værdien med et lighedstegn (**=**). Du kan få flere oplysninger om de understøttede operatorer og den understøttede syntaks i [Understøttede matematiske symboler](http://bugwheels94.github.io/math-expression-evaluator/#supported-maths-symbols).

## <a name="grouping-tabular-data"></a>Gruppere data i tabelformat
Forretningsbrugere har ofte brug for at udføre ad hoc-analyse af data. Dette kan gøres ved at eksportere data til Microsoft Excel og bruge pivottabeller, men funktionen **Gruppering i gitre**, der er afhængig af den nye gitterkontrol, tillader brugere at organisere deres tabeldata på interessante måder i Finance and Operations-apps. Da denne funktion udvider funktionen **Totaler**, giver **Gruppering** også mulighed for at få meningsfuld indsigt i dataene ved at levere subtotaler på gruppeniveau.

Hvis du vil bruge denne funktion, skal du højreklikke på den kolonne, du vil gruppere efter, og vælge **Gruppér efter denne kolonne**. Denne handling sorterer dataene efter den valgte kolonne, føjer en ny **Gruppér efter**-kolonne til starten af gitteret og indsætter "overskriftsrækker" i starten af hver gruppe. Disse kolonneoverskrifter indeholder følgende oplysninger om hver enkelt gruppe: 
-  Dataværdi for gruppen 
-  Kolonnenavn (disse oplysninger vil især være nyttige, når du har flere grupperingsniveauer)  
-  Antallet af datarækker i denne gruppe
-  Subtotaler for enhver kolonne, der er konfigureret til at vise totaler

Når [Gemte visninger](saved-views.md) er aktiveret, kan denne gruppering gemmes via tilpasning som del af en visning for at få hurtig adgang, når du næste gang besøger siden.  

### <a name="multiple-levels-of-grouping"></a>Flere grupperingsniveauer
Når du har grupperet data efter en enkelt kolonne, kan du gruppere dataene efter en anden kolonne ved at vælge **Gruppér efter denne kolonne** i den ønskede kolonne. Denne proces kan gentages, indtil du har fem indlejrede grupperingsniveauer, hvilket er den maksimalt understøttede dybde. Derefter kan du ikke længere gruppere efter yderligere kolonner.  

Du kan altid fjerne grupperingen efter en hvilken som helst kolonne ved at højreklikke på den pågældende kolonne og vælge **Opdel gruppe**. Du kan også fjerne grupperingen fra alle kolonner ved at vælge **Gitterindstillinger** og derefter **Opdele alle**.   

### <a name="expanding-and-collapsing-groups"></a>Udvide og skjule grupper
Den oprindelige gruppering af data vil få alle grupper udvidet. Du kan oprette opsummerede visninger af dataene ved at skjule de enkelte grupper, eller du kan bruge gruppeudvidelse og skjulning som hjælp til at navigere gennem dataene. Hvis du vil udvide eller skjule en gruppe, skal du vælge knappen vinkeltegn (>) i den tilsvarende gruppeoverskriftsrække. Bemærk, at de enkelte gruppers udvidede/skjulte tilstand **ikke** gemmes i personlig tilpasning.

### <a name="selecting-and-unselecting-rows-at-the-group-level"></a>Markere og fjerne markering af rækker på gruppeniveau
På samme måde som du kan markere (eller fjerne markeringen af) alle rækker i gitteret ved at markere afkrydsningsfeltet øverst i den første kolonne af gitteret, kan du også hurtigt markere (eller fjerne markeringen af) alle rækkerne i en gruppe ved at markere afkrydsningsfeltet i den tilsvarende gruppehovedrække. Afkrydsningsfeltet i gruppehovedrækken afspejler altid den aktuelle valgtilstand for rækker i den pågældende gruppe, uanset om alle eller ingen rækker er markeret, eller kun bestemte rækker er markeret.

### <a name="hiding-column-names"></a>Skjule kolonnenavne
Ved gruppering af data viser standardfunktionsmåden kolonnenavnet i gruppehovedrækken. Du kan vælge at udelade kolonnenavnet i gruppehovedrækker ved at vælge **Gitterindstillinger** > **Skjul gruppekolonnenavn**.

## <a name="freezing-columns"></a>Fryse kolonner
Visse kolonner i et gitter kan være så vigtige for sammenhængen, at de ikke skal rulle ud af visningen. Du vil i stedet have, at værdierne i disse kolonner altid er synlige. Funktionen **Frys kolonner i gitteret** giver denne fleksibilitet for brugerne. 

Hvis du vil fryse en kolonne, skal du højreklikke på kolonnens overskrift og derefter vælge **Frys kolonne**. Første gang du fuldfører dette trin, bliver den valgte kolonne den første kolonne, og den rulles ikke længere ud af visningen. En efterfølgende kolonne, som du fryser, vil blive tilføjet til højre for den sidste frosne kolonne. Du kan bruge standardfunktionen Flyt til at sortere frosne kolonner efter behov. Frosne kolonner kan dog ikke flyttes, så de vises mellem sættet af ikke-frosne kolonner. Frosne kolonner kan heller ikke flyttes, så de vises mellem sættet af frosne kolonner.

Hvis du vil frigøre en kolonne, skal du højreklikke på den frosne kolonnes overskrift og derefter vælge **Frigør kolonne**. 

Bemærk, at rækkevalget og rækkestatuskolonnerne i det nye gitter altid fryses som de første to kolonner. Når disse kolonner er medtaget i et gitter, er de derfor altid synlige for brugerne, uanset den vandrette rulleposition i gitteret. Disse to kolonner kan ikke omrokeres.

## <a name="frequently-asked-questions"></a>Ofte stillede spørgsmål
### <a name="how-do-i-enable-the-new-grid-control-in-my-environment"></a>Hvordan aktiverer jeg det nye gitterkontrolelement i mit miljø? 

Funktionen **Nyt gitterkontrolelement** er tilgængelig direkte i funktionsstyring i ethvert miljø. Når funktionen er aktiveret i Funktionsstyring, vil alle efterfølgende brugersessioner bruge det nye gitterkontrolelement. 

Denne funktion aktiveres som standard med start i version 10.0.21 og er planlagt til at blive obligatorisk i version 10.0.25. 

## <a name="developer-opting-out-individual-pages-from-using-the-new-grid"></a>[Udvikler] Framelde enkelte sider brug af det nye gitter 
Hvis din organisation finder en side, der har nogle problemer med at bruge det nye gitter, er der en API, der giver mulighed for, at en individuel formular kan benytte det ældre gitter, samtidig med at det stadig tillader resten af systemet at anvende det nye gitterkontrolelement. Hvis du framelder en enkelt side fra det nye gitter, skal du tilføje følgende opkaldspost `super()` i `run()`-metoden for formularen.

 ```this.forceLegacyGrid();```

Denne API vil blive opfyldt, indtil det nye gitterkontrolelement bliver obligatorisk, hvilket efter planen sker i april 2022. Hvis der er problemer, der kræver, at denne API bruges, skal du rapportere dem til Microsoft.

### <a name="forcing-a-page-to-use-the-new-grid-after-previously-opting-out-the-grid"></a>Tvinge en side til at bruge det nye gitter, når gitteret tidligere er fravalgt
Hvis du har valgt en enkelt side fra til brug af det nye gitter, kan du senere aktivere det nye gitter igen, når de underliggende problemer er løst. Hvis du vil gøre dette, skal du blot fjerne kaldet til `forceLegacyGrid()`. Ændringen træder først i kraft, når en af følgende ting er sker:

- **Geninstallation af miljøet**: Når et miljø opdateres og geninstalleres, ryddes den tabel, der gemmer de sider, der er valgt ud af det nye gitter (FormControlReactGridState), automatisk.

- **Manuel rydning af tabellen**:Til udviklingsscenarier skal du bruge SQL til at rydde tabellen FormControlReactGridState og derefter genstarte AOS. Denne kombination af handlinger nulstiller den cachelagring af sider, der er valgt ud af det nye gitter.  

## <a name="developer-size-to-available-width-columns"></a>[Udvikler] "Tilpas størrelsen til tilgængelig bredde"-kolonner
Hvis en udvikler angiver egenskaben **WidthMode** til **SizeToAvailable** for kolonner i det nye gitter, har disse kolonner som udgangspunkt samme bredde, som de ville have, hvis egenskaben var angivet til **SizeToContent**. De strækkes dog for at bruge eventuel ekstra tilgængelig bredde i gitteret. Hvis egenskaben er angivet til **SizeToAvailable** for flere kolonner, deler alle kolonnerne eventuel ekstra tilgængelig bredde i gitteret. Men hvis en bruger manuelt tilpasser størrelsen på en af disse kolonner, bliver kolonnen statisk. Den forbliver på denne bredde og kan ikke længere strækkes for at bruge den ekstra tilgængelige gitterbredde.  

## <a name="known-issues"></a>Kendte problemer
I dette afsnit vedligeholdes en liste over kendte problemer for det nye gitterkontrol.  

### <a name="open-issues"></a>Aktuelle problemer
-  Når funktionen **Nyt gitterkontrolelement** er aktiveret, vil nogle sider fortsat anvende det eksisterende gitterkontrolelement. Det sker i følgende situationer:  
    -  Der findes en kortliste på siden, som gengives i flere kolonner.
    -  Der findes en grupperet kortliste på siden.
    -  En gitterkolonne med et ikke-reagerende kontrolelement, der kan udvides.

    Når en bruger først støder på en af disse situationer, vises der en meddelelse om opdatering af siden. Når denne meddelelse vises, vil siden fortsat anvende det eksisterende gitter for alle brugere indtil den næste opdatering af produktversionen. En bedre håndtering af disse scenarier, så det nye gitter kan anvendes, vil blive betragtet som en fremtidig opdatering.    
    
-  [KB 4582758] Poster er slørede, når du ændrer zoom fra 100 til en hvilken som helst anden procent
-  [KB 4592012] Uventet klientfejl i IE11, når der indsættes flere linjer fra Excel
    -  Microsoft gør ikke noget ved dette problem

### <a name="fixed-as-part-of-10016"></a>Rettet i 10.0.16

-  [KB 4598335] Strengkontroller for flere linjer overholder ikke visningshøjder på lister/kort 
-  [KB 4591891] Fakturaforslagslinjer forsvinder, når linjer afmærkes
-  [KB 4592104] Det er ikke muligt at redigere poster efter klik på "Løs problem" og flytning til en anden række uden at rette valideringsproblemet
-  [KB 4594449] Knapperne "Aldrig" og "Ryd" mangler i datovælgeren 
-  [KB 4594448] Angivelse af tid behandles anderledes med det nye gitter
-  [KB 4600059] Uventet klientfejl med mailbegrænsning
-  [KB 4574584] Forhåndsvisning af vedhæftede udgifter er ikke tilgængelig, når du peger på kvitteringsikonet

### <a name="fixed-as-part-of-10015"></a>Rettet i 10.0.15    

-  (Kvalitetsopdatering) [KB 4594444] Uventet klientfejl med eksempelvisning af segmenteret postkontrolelement
-  [KB 4582723] Visningsindstillinger vises ikke, når det gøres senere i formularens livscyklus
-  [KB 4591988] Problemer med brug af tastaturet til valg af en værdi fra opslag i ReferenceGroup
-  [KB 4588958] Regression Suite Automation Tool (RSAT) testen mislykkes med fejl: TypeError: Kan ikke læse egenskaben 'tekst' for udefineret
-  [KB 4591970] Uventet klientfejl under indsættelse fra Excel, umiddelbart efter at der klikkes i gitteret
-  [KB 4591904] Dataændringer gemmes ikke efter redigering af et kontrolelement, hvis brugeren med det samme har klikket på og åbnet opslaget på et andet kontrolelement
-  [KB 4584752] Uventet klientfejl med siden med Projektfakturaforslag
-  [KB 4584540] Det er ikke muligt at forlade gitteret, når en enkelt række er indsat i en kladdelinje
-  [KB 4591908] Ved oprettelse af en ny række, forbliver fokus på den kolonne, du var i

### <a name="fixed-as-part-of-10014"></a>Rettet i 10.0.14

-  (Kvalitetsopdatering) [KB 4584752] Uventet klientfejl med siden med Projektfakturaforslag
-  [KB 4583880] Regression Suite Automation Tool (RSAT) test mislykkes på OpenLookup-handling med "Egenskaben RowIndex kan ikke læses af udefineret"
-  [KB 4583847] Uventet klientfejl ved navigering i opslag

### <a name="fixed-as-part-of-10013"></a>Rettet i 10.0.13

-  (Kvalitetsopdatering) [KB 4584752] Uventet klientfejl med siden med Projektfakturaforslag
-  (Kvalitetsopdatering) [KB 4583880] Regression Suite Automation Tool (RSAT) Test mislykkes på OpenLookup-handling med "Egenskaben RowIndex kan ikke læses af udefineret"
-  (Kvalitetsopdatering) [KB 4583847] Uventet klientfejl ved navigering i opslag 
-  (Kvalitetsopdatering) [Fejl 471777] Kan ikke vælge felter i et gitter for at redigere eller oprette en mobilapp
-  [KB 4582727] Gitter fryses, når brugeren får dialogboks til varer med flere antal
-  [Fejl 474851] Hyperlinks i referencegruppekontrolelementer virker ikke 
-  [Fejl 474848] Udvidede eksempler med gitre vises ikke
-  [KB 4582726] Egenskaben RotateSign overholdes ikke  
-  [Fejl 470173] Afkrydsningsfelter i inaktive rækker skifter, når der klikkes på blanktegnene i cellen
-  [Fejl 474848] Udvidede eksempler med gitre vises ikke
-  [Fejl 474851] Hyperlinks i referencegruppekontrolelementer virker ikke 
-  [Fejl 471777] Kan ikke vælge felter i et gitter for at redigere eller oprette en mobilapp
-  [KB 4569441] Problemer med at gengive kortlister med flere kolonner, værktøjstip på billeder og visningsindstillinger på nogle felter
-  [KB 4575279] Ikke alle markerede rækker slettes i finanskladden
-  [KB 4575233] Visningsindstillinger gendannes ikke efter flytning til en anden række
-  [Fejl 477884] Opslag returnerer den forkerte værdi/post, hvis det nye gitterkontrolelement er aktiveret
-  [KB 4571095] Bogføring af produktkvittering sker ved utilsigtet tryk på Enter (korrekt håndtering af en sides standardhandling)
-  [KB 4575437] Opslag med redigerbare kontrolelementer lukker uventet
-  [KB 4569418] Dubleret linje oprettes i leveranceplanens formular
-  [KB 4575435] Udvidet eksempel forsvinder nogle gange, selv når musemarkøren ikke er tæt på feltet
-  [KB 4575434] Opslaget filtreres ikke, når feltet er blevet ændret
-  [KB 4575430] Værdier i adgangskodefelter maskeres ikke i gitteret
-  [KB 4569438] "Behandlingen er stoppet på grund af et valideringsproblem" vises efter afmærkningslinjer under udligning af leverandørtransaktioner
-  [KB 4569434] Når du opdaterer formularen juridiske enheder, er der færre poster
-  [KB 4575297] Fokus bliver ved med at blive flyttet til ruden Arbejdsrutineoptager, når der redigeres og tabuleres gennem et gitter
-  [KB 4566773] Korrektionstransaktioner vises ikke som negative på forespørgsel om bilagstransaktioner 
-  [KB 4575288] Fokus nulstilles til den aktive række, når du markerer rammen mellem rækker på en simpel liste
-  [KB 4575287] Fokus vender ikke tilbage til første kolonne, når du bruger pil ned til at oprette en ny række i kladder
-  [KB 4564819] Kan ikke slette linjer i en fritekstfaktura (fordi datakilden ChangeGroupMode=ImplicitInnerOuter)
-  [KB 4563317] Der vises ikke værktøjstip/forbedrede eksempler til billeder

### <a name="fixed-as-part-of-10012"></a>Rettet i 10.0.12

- [KB 4558545] Tabelkontrolelementer opdaterer ikke indholdet af viste elementer.
- [KB 4558570] Der vises stadig elementer på siden, når posten er blevet slettet.
- [KB 4558572] Den formatering, der er knyttet til listepanelet **ExtendedStyle**, anvendes ikke.
- [KB 4558573] Valideringsfejl kan ikke rettes, når den nødvendige ændring er uden for gitteret.
- [KB 4558584] Negative tal gengives ikke korrekt.
- [KB-4560726] Der opstår "en uventet klientfejl", efter at der er skiftet mellem lister ved hjælp af listevisningskontrol.
- [KB-4562141] Gitterindeks er slået fra, efter at der er tilføjet en ny post.
- [KB 4562151] Indstillingerne **Valider** og **Kopiér** i Arbejdsrutineoptager er ikke tilgængelige for dato- og nummerkontrolelementer. 
- [KB-4562153] Afkrydsningsfelter med flere valg er ikke synlige på liste/kort-gitre.
- [KB 4562646] Undertiden kan du ikke klikke uden for gitteret, når du f.eks. vælger rækker i gitteret.
- [KB-4562647] Fokus nulstilles til det første kontrolelement i dialogboksen **Publicer**, efter at der er tilføjet en ny række i sikkerhedsrollegitteret.
- [KB-4563310] Den udvidede visning lukkes ikke, efter at en række er ændret.
- [KB-4563313] Der opstår en "uventet klientfejl" i Internet Explorer, når der vælges en værdi i et opslag.
- [KB 4564557] Opslag og rullemenuer åbnes ikke i Internet Explorer
- [KB-4563324] Navigationen fungerer ikke, når arbejdsområdet **Personalestyring** er blevet åbnet.

### <a name="fixed-as-part-of-10011"></a>Rettet i 10.0.11

- [Problem 432458] Tomme eller dublerede linjer vises i starten af nogle underordnede samlinger.
- [KB 4549711] Linjer i et betalingsforslag kan ikke fjernes korrekt, når det nye gitterkontrolelement er aktiveret.
- [KB 4558374] Poster, der kræver dialogboks med polymorf vælger, kan ikke oprettes.
- [KB 4558375] Der vises ingen hjælpetekst på kolonner i det nye gitter.
- [KB 4558376] Listepanelets gitre gengives ikke med den korrekte højde i Internet Explorer.
- [KB 4558377] Kombinationsfeltkolonner, der har **SizeToAvailable**-bredde, gengives ikke på visse sider.
- [KB 4558378] Detaljeadgang åbner nogle gange den forkerte post.
- [KB 4558379] Der opstår en fejl, når opslag åbnes, hvor **ReplaceOnLookup**=**Nej**.
- [KB 4558380] Den ledige plads i gitteret udfyldes ikke straks, når en del af siden er skjult.
- [KB 4558381] Negative tal gengives ikke korrekt, og brugerne vil sommetider blive fastlåst, efter at der er registreret valideringsproblemer.
- [KB 4558382] Der opstår uventede klientfejl.
- [KB 4558383] Kontrolelementer uden for gitteret opdateres ikke, når den sidste post er slettet.
- [KB 4558587] Referencegrupper, der indeholder kombinationsbokse for erstatningsfelter, viser ikke værdier.
- [KB 4562143] Felter opdateres ikke, når en rækkeændring/gitterbehandling sidder fast efter sletning af rækker.
- [KB 4562645] Der opstår en undtagelse, når der åbnes et opslag, mens Regression Suite Automation Tool RSAT-test kører.

### <a name="fixed-as-part-of-10010"></a>Rettet i 10.0.10

- [Problem 414301] Nogle data fra tidligere linjer forsvinder, når der oprettes nye linjer.
- [Fejl 417044] Der er ingen meddelelse om tomt gitter for listetypegitre.
- [KB 4539058] Nogle gitre (typisk i oversigtspanelerne) kan nogle gange ikke gengives (men gengives, hvis du zoomer ud).
- [KB 4549734] Aktive rækker behandles ikke som markerede, hvis markeringskolonnen er skjult.
- [KB 4549796] Værdier kan ikke redigeres i et gitter, når det er i visningstilstand.
- [KB 4558367] Tekstmarkering er inkonsekvent, når rækkerne ændres.
- [KB 4558368] Flere valg via tastaturet er tilladt i enkeltvalgsscenarier.
- [KB 4558369] Statusbilleder forsvinder i det hierarkiske gitter.
- [KB 4558370] En ny række rulles ikke ind i visningen.
- [KB 4558372] Det nye gitter sidder fast i behandlingstilstand, hvis antallet af kolonner i det indhold, der indsættes, overstiger antallet af resterende kolonner i gitteret.
- [KB 4562631] Tidsværdier formateres ikke korrekt.

### <a name="quality-update-for-1009platform-update-33"></a>Kvalitetsopdatering til 10.0.9/Platform update 33

- [KB 4550367] Tidsværdier formateres ikke korrekt.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
