---
title: Gitteregenskaber
description: Denne artikel beskriver flere stærke funktioner i gitterkontrolelementet. Den nye gitterfunktion skal være aktiveret for at få adgang til disse egenskaber.
author: jasongre
ms.date: 08/09/2022
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
ms.openlocfilehash: a8968a1263dfafd67b07b4beb78c51493e95756e
ms.sourcegitcommit: 47534a943f87a9931066e28f5d59323776e6ac65
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/11/2022
ms.locfileid: "9258941"
---
# <a name="grid-capabilities"></a>Gitteregenskaber

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Det nye gitterkontrolelement omfatter en række nyttige og effektive funktioner, du kan bruge til at forbedre brugernes produktivitet, oprette mere interessante visninger af dine data og få meningsfuld indsigt i dine data. Denne artikel dækker følgende funktioner: 

- Vise beregnede værdier 
- Skrive forud i forhold til systemet
- Evaluere matematiske udtryk 
- Gruppere data i tabelformat (aktiveres separat ved hjælp af funktionen **Gruppering i gitre**)
- Frysning af kolonner (aktiveres separat ved hjælp af funktionen **Frysning af kolonner i gitre**)
- Tilpasse kolonnebredde automatisk
- Kolonner, der kan strækkes

## <a name="showing-calculated-values"></a>Vise beregnede værdier
I programmer til finans og drift kan brugere få vist en beregnet værdi for hver numeriske kolonne i et gitter. Disse beregnede værdier vises i en sektion med sidefod nederst i gitteret.

[![Vise beregnede værdier i gitre.](./media/grids-aggregation.png)](./media/grids-aggregation.png)

I versioner før 10.0.29 er totalen den eneste understøttede beregnede værdi. I version 10.0.29, efter at de har aktiveret funktionen **Udvidede egenskaber for gitteraggregering**, kan brugere dog vælge mellem følgende fire beregnede værdier:

- Minimum
- Maksimum
- Total
- Gennemsnit

En enkelt kolonne kan kun vise én type beregnet værdi. Men hver kolonne i gitteret kan konfigureres til at vise en anden type beregnet værdi.

### <a name="showing-the-grid-footer"></a>Visning af gitterets sidefod
Der er et sidefodsområde i bunden af alle tabelgitre i programmer til finans og drift. Sidefoden kan vise værdifulde oplysninger, der er relateret til de data, der vises i gitteret. Her er nogle eksempler på sådanne oplysninger:

- Antallet af markerede rækker i tabellen (når du markerer mere end én post)
- Beregnede værdier nederst i konfigurerede og numeriske kolonner (f.eks. samlede totaler)
- Antallet af rækker i datasættet 

Denne sidefod er som standard skjult, men du kan slå den til. Hvis du vil have vist sidefoden for et gitter, skal du vælge knappen **Gitterindstillinger** i gitteroverskriften og vælge indstillingen **Vis sidefod**. Når du har aktiveret sidefoden i et bestemt gitter, huskes denne indstilling, indtil brugeren vælger at skjule sidefoden. Hvis du vil skjule sidefoden, skal du vælge **Skjul sidefod** i menuen **Gitterindstillinger**.

### <a name="specifying-columns-with-calculated-values"></a>Angive kolonner med beregnede værdier
Aktuelt viser ingen kolonner som standard beregnede værdier. I stedet betragtes det som en engangsaktivitet, der svarer til at justere kolonnebredden i gitre. Når du har angivet, at du vil have vist en beregnet værdi for en kolonne, vil denne indstilling blive husket, næste gang du besøger siden.

Du kan konfigurere en kolonne på to måder for at vise en beregnet værdi:

- Vælg og hold (eller højreklik) i den kolonne, du vil have vist en beregnet værdi for. Hvis funktionen **Udvidede egenskaber for gitteraggregering** er aktiveret, skal du vælge **Vis kolonnetotaler** og derefter vælge den ønskede beregnede værdi. Hvis denne funktion ikke er aktiveret, skal du vælge **Total for denne kolonne**. Denne handling resulterer i tre hændelser:

    1. Sidefoden i gitteret bliver synlig. 
    2. Din præference for visning af en beregnet værdi for kolonnen gemmes. 
    3. Den ønskede beregning aktiveres for kolonnen og alle andre kolonner, som du tidligere har konfigureret til at vise en beregnet værdi. Den tid, der kræves for at få vist de beregnede værdier, afhænger af størrelsen på datasættet.

- Når sidefoden er synlig, skal du vælge **Vis total** (eller **Vælg beregnet værdi**, hvis funktionen **Udvidede egenskaber for gitteraggregering** er aktiveret) i området til sidefoden nederst i den kolonne, du vil have vist en beregnet værdi for. Hvis der ikke er nogen konfigurerede kolonner, vil knappen være tilgængelig i sidefoden til alle numeriske kolonner.

    Når mindst én kolonne er konfigureret til at vise en beregnet værdi, er knappen **Vis total** (eller **Vælg beregnet værdi**) kun tilgængelig, hvis du peger eller fokuserer på den. Ved at vælge knappen gemmer du din præference for at få vist en beregnet værdi i denne kolonne, så præferencen anvendes under fremtidige besøg på siden. I sidefoden er denne status angivet med en tankestreg, der vises i kolonnen. (Bemærk, at den beregnede værdi vises med det samme, hvis datasættet er lille nok).

Hvis du laver en fejl og ikke længere ønsker at få vist en beregnet værdi i en specifik kolonne, skal du markere og holde den i kolonnen (eller højreklikke) og derefter vælge **Skjul total** (eller **Vis kolonnetotaler \> Ingen**, hvis funktionen **Udvidede egenskaber for gitteraggregering** er aktiveret). Alternativt kan du vælge **Skjul total** (eller **Skjul beregnet værdi**) i sidefoden i den pågældende kolonne. Denne præference vil også blive gemt til fremtidige besøg på siden. 

### <a name="calculating-aggregate-values"></a>Beregne aggregerede værdier
Når du går til en side, hvor sidefoden er synlig, og kolonnerne allerede er konfigureret til at vise beregnede værdier, vises disse værdier muligvis ikke i sidefoden. Funktionsmåden afhænger af størrelsen af datasættet på siden. Hvis datasættet er tilstrækkeligt lille, vises beregnede værdier automatisk sammen med antallet af rækker i datasættet. Hvis der er bindestreger i sidefoden under de kolonner, du har konfigureret, er datasættet for stort til, at systemet kan vise beregnede værdier med det samme. I dette tilfælde kræves der en eksplicit handling for at beregne værdierne. Hvis du vil beregne værdierne, skal du vælge knappen **Beregn** i sidefoden. Du kan også markere og holde markøren på kolonnen (eller højreklikke), hvis total du vil se, og derefter vælge **Total for denne kolonne** (eller **Vis kolonnetotaler** og derefter den ønskede beregnede værdi, hvis funktionen **Udvidede egenskaber for gitteraggregering** er aktiveret).

Hvis beregningen tager lang tid at fuldføre, kan du annullere operationen ved at klikke på knappen **Annuller**. Sommetider vil datasættet være for stort til at beregne aggregerede værdier (en grænse, der pålægges af din organisation). I dette tilfælde får du i stedet besked om at filtrere dataene mere.

> [!NOTE]
> Systemadministrationer kan ændre grænsen for det antal poster, der er tilgængelige til beregning af aggregater, ved at justere det **Maksimale antal lokale poster for hver gitter**-parameteren på siden **Indstillinger for klientydeevne**. Standardværdien er 25.000 poster. Administratorer skal være omhyggelige, når de justerer denne værdi, da en for stor værdi kan opbruge den ledige hukommelse på brugerens computer. Vi anbefaler, at den ikke overstiger 50.000 poster.

Beregnede værdier opdateres automatisk, efterhånden som du opdaterer, sletter eller opretter rækker i datasættet.

## <a name="typing-ahead-of-the-system"></a>Skrive forud i forhold til systemet
I mange forretningsscenarier er muligheden for hurtigt at indtaste data i systemet meget vigtig. Før det nye gitterkontrolelement blev introduceret, kunne brugerne kun ændre data i den aktuelle række. Når de har foretaget ændringer i en række, kunne brugerne derfor ikke skifte til en anden række eller oprette en ny række, før systemet havde valideret ændringerne i den aktuelle række, og (hvis der er tale om rækkeoprettelse) kørt alle de logiker, der er knyttet til oprettelsen af en ny række. For at reducere den mængde tid, som brugerne venter på, at disse handlinger fuldføres, og for at forbedre brugerproduktiviteten justerer det nye gitter disse handlinger, så de er asynkrone. Brugeren kan oprette nye rækker eller flytte til andre rækker for at foretage ændringer, mens tidligere valideringer af rækker og rækkelogik venter. 

[![Skrive forud i forhold til systemet.](./media/gridFastEntry-07-25-2022.gif)](./media/gridFastEntry-07-25-2022.gif)

For at understøtte denne nye funktionsmåde er der tilføjet en ny kolonne for rækkestatus til højre for kolonnen for rækkevalg, når gitteret er i redigeringstilstand. Denne kolonne angiver en af følgende statusser:

- **Tom** – Intet statusbillede angiver, at rækken er blevet gemt af systemet.
- **Afventer behandling** – Denne status angiver, at ændringerne i rækken endnu ikke er gemt af serveren, men de er i en kø med ændringer, der skal behandles. Før du udfører en handling uden for gitteret, skal du vente på, at alle ventende ændringer behandles. Desuden er teksten i disse rækker kursiv for at angive den ikke-gemte status for rækkerne. 
- **Ugyldig tilstand** – Denne status angiver, at der blev udløst en eller anden advarsel eller meddelelse under behandlingen af rækken, og det kan have forhindret systemet i at gemme ændringerne i den pågældende række. I det gamle gitter blev du tvunget tilbage til rækken for at løse problemet med det samme, hvis gemmehandlingen ikke lykkedes. Men i det nye gitter får du besked om, at der er opstået et valideringsproblem, men du kan beslutte, hvornår eventuelle problemer skal løses i rækken. Når du er klar til at løse et problem, kan du manuelt flytte fokus tilbage til rækken. Du kan også vælge funktionen **Løs dette problem**. Denne handling flytter øjeblikkeligt fokus tilbage til den række, hvor problemet er, og giver dig mulighed for at foretage ændringer i eller uden for gitteret. Bemærk, at behandlingen af efterfølgende ventende rækker standses, indtil denne valideringsadvarsel er løst. 
- **Midlertidigt afbrudt** – Denne status angiver, at behandlingen af serveren er sat på pause, fordi validering af rækken udløste en pop op-dialogboks, der kræver brugerinput. Da brugeren måske indtaster data i en anden række, vises pop op-dialogboksen ikke med det samme for den pågældende bruger. Den vises i stedet, når brugeren vælger at genoptage behandlingen. Denne status er ledsaget af en besked, der oplyser brugeren om situationen. Beskeden indeholder handlingen **Fortsæt behandling**, der vil udløse pop op-dialogboksen.

### <a name="differences-when-entering-data-ahead-of-the-system"></a>Forskelle, når der indtastes data forud for systemet
Når du angiver data foran det sted, hvor systemet behandles, kan du forvente nogle få ændringer i dataindtastningsoplevelsen:

- Du bemærker, at der ikke er nogen opslags rullelister, feltværdierne valideres ikke, når du flytter til en anden kolonne i samme række, og kolonnerne viser ikke i begyndelsen standardværdier. Denne funktionsmåde opstår, når du opretter eller opdaterer forud for systemet. Når systemet imidlertid indhenter det sted, du er ved at redigere, genoptages standardoplevelsen. Hvis du har foretaget ændringer i et felt, der normalt modtager en standardværdi, tilsidesætter dine ændringer standardfeltværdien, når serveren begynder at behandle rækken.
- Hvis du opretter en ny række ved hjælp af **Pil ned**, vises alle kolonner i gitteret som redigerbare. Som standard sættes fokus i den første kolonne i den nye række. Denne kolonne er muligvis ikke den samme kolonne, som fik den første fokusering i det tidligere gitter, eller den samme kolonne, der får fokus, når du har valgt en **Ny**-knap. Din organisation kan tilpasse systemet og ændre den kolonne, der får det første fokus, når **Pil ned** vælges. Du kan finde flere oplysninger i afsnittet [Angive den kolonne, der får den første fokusering, når der oprettes nye rækker med tasten Pil ned](#developer-specifying-the-column-that-receives-the-initial-focus-when-new-rows-are-created-by-using-the-down-arrow-key). Uanset hvad kan du bruge personlig tilpasning til at optimere hvert gitter for dataindtastning. Du kan specifikt omarrangere felter, så den første kolonne er den kolonne, du vil starte med at indtaste data i. Du vil måske også ændre rækkefølgen af felter generelt for dataindtastning, reducere tabulatorstop og skjule felter, der ikke kræves ved dataindtastning i denne visning.

### <a name="pasting-from-excel"></a>Indsætning fra Excel
Brugerne har altid været i stand til at eksportere data fra gitre i programmer til finans og drift til Microsoft Excel ved hjælp af mekanismen **Eksportér til Excel**. Muligheden for at indtaste data forud i systemet gør det dog muligt for det nye gitter at understøtte kopiering af tabeller fra Excel og indsætning af dem direkte i gitre i programmer til finans og drift. Den gittercelle, som indsætningen er initieret fra, bestemmer, hvor den kopierede tabel begynder at blive indsat. Indholdet af gitteret overskrives med indholdet af den kopierede tabel, undtagen i to tilfælde:

- Hvis antallet af kolonner i den kopierede tabel overstiger antallet af kolonner, der er tilbage i gitteret, startende fra indsætningens sted, får brugeren besked om, at de ekstra kolonner er blevet ignoreret. 
- Hvis antallet af rækker i den kopierede tabel overstiger antallet af rækker i gitteret med start fra indsætningens sted, overskrives de eksisterende celler af det indsatte indhold, og eventuelle ekstra rækker fra den kopierede tabel indsættes som nye rækker nederst i gitteret. 

## <a name="evaluating-math-expressions"></a>Evaluere matematiske udtryk
Som en produktivitetsbooster kan brugerne indtaste matematiske formler i numeriske celler i et gitter. De behøver ikke at foretage beregningen i en app uden for systemet. Hvis du f.eks. angiver **=15\*4** og derefter trykker på tasten **Tab** for at flytte ud af feltet, evalueres udtrykket, og værdien **60** gemmes for feltet.

[![Evaluere matematiske udtryk.](./media/gridMathExpression-07-25-2022.gif)](./media/gridMathExpression-07-25-2022.gif)

Hvis du vil have systemet til at genkende en værdi som et udtryk, skal du starte værdien med et lighedstegn (**=**). Du kan få flere oplysninger om de understøttede operatorer og den understøttede syntaks i [Understøttede matematiske symboler](http://bugwheels94.github.io/math-expression-evaluator/#supported-maths-symbols).

Fra og med version 10.0.29 er muligheden for at evaluere matematiske udtryk i numeriske kontrolelementer udvidet og er nu også tilgængelig uden for gitteret.

## <a name="grouping-tabular-data"></a>Gruppere data i tabelformat
Erhvervsbrugere har ofte brug for at udføre ad hoc-analyse af data. Selvom denne analyse kan gøres ved at eksportere data til Microsoft Excel og bruge pivottabeller, kan funktionen **Gruppering i gitre**, der er afhængig af den nye gitterkontrol, tillade brugere at organisere deres tabeldata på interessante måder i programmer til finans og drift. Da denne funktion udvider funktionen **Beregnede værdier**, giver **Gruppering** også mulighed for at få meningsfuld indsigt i dataene ved at levere beregnede værdier (f.eks. subtotaler) på gruppeniveau.

[![Gruppering af data i et gitter.](./media/grids-groupingWithTotals.png)](./media/grids-groupingWithTotals.png)

Hvis du vil bruge denne funktion, skal du højreklikke på den kolonne, du vil gruppere efter, og vælge **Gruppér efter denne kolonne**. Denne handling sorterer dataene efter den valgte kolonne, føjer en ny **Gruppér efter**-kolonne til starten af gitteret og indsætter "overskriftsrækker" i starten af hver gruppe. Disse kolonneoverskrifter indeholder følgende oplysninger om hver enkelt gruppe:

- Dataværdi for gruppen 
- Kolonnenavn (disse oplysninger vil især være nyttige, når du har flere grupperingsniveauer)
- Antallet af datarækker i denne gruppe
- Beregnede værdier for eventuelle konfigurerede kolonner (f.eks. subtotaler, hvis kolonnen er konfigureret til at vise en total)

Når [Gemte visninger](saved-views.md) er aktiveret, kan du gemme gruppering som en del af en visning på sider, så forespørgsler kan gemmes i visninger. F.eks. personer med store visningsvælger. Du kan finde flere oplysninger i afsnittet [Skifte mellem visninger](saved-views.md#switching-between-views). 

### <a name="multiple-levels-of-grouping"></a>Flere grupperingsniveauer
Når du har grupperet data efter en enkelt kolonne, kan du gruppere dataene efter en anden kolonne ved at vælge **Gruppér efter denne kolonne** i den ønskede kolonne. Denne proces kan gentages, indtil du har fem indlejrede grupperingsniveauer, hvilket er den maksimalt understøttede dybde. Derefter kan du ikke længere gruppere efter yderligere kolonner.

Du kan altid fjerne grupperingen efter en hvilken som helst kolonne ved at højreklikke på den pågældende kolonne og vælge **Opdel gruppe**. Du kan også fjerne grupperingen fra alle kolonner ved at vælge **Gitterindstillinger** og derefter **Opdele alle**.

### <a name="sorting-grouped-data"></a>Sortere grupperede data
Når du har grupperet data efter en eller flere kolonner, kan du ændre sorteringsretningen for enhver grupperingskolonne gennem den tilsvarende kolonneoverskrift. 

Hvis du sorterer i en kolonne, der ikke er grupperet, forbliver gruppering intakt. Dataene sorteres i hver gruppe på basis af den valgte kolonne.

### <a name="expanding-and-collapsing-groups"></a>Udvide og skjule grupper
Den oprindelige gruppering af data vil få alle grupper udvidet. Du kan oprette opsummerede visninger af dataene ved at skjule de enkelte grupper, eller du kan bruge gruppeudvidelse og skjulning som hjælp til at navigere gennem dataene. Hvis du vil udvide eller skjule en gruppe, skal du vælge knappen vinkeltegn (>) i den tilsvarende gruppeoverskriftsrække. Bemærk, at de enkelte gruppers udvidede/skjulte tilstand **ikke** gemmes i personlig tilpasning.

### <a name="selecting-and-unselecting-rows-at-the-group-level"></a>Markere og fjerne markering af rækker på gruppeniveau
På samme måde som du kan markere (eller fjerne markeringen af) alle rækker i gitteret ved at markere afkrydsningsfeltet øverst i den første kolonne af gitteret, kan du også hurtigt markere (eller fjerne markeringen af) alle rækkerne i en gruppe ved at markere afkrydsningsfeltet i den tilsvarende gruppehovedrække. Afkrydsningsfeltet i gruppehovedrækken afspejler altid den aktuelle valgtilstand for rækker i den pågældende gruppe, uanset om alle eller ingen rækker er markeret, eller kun bestemte rækker er markeret.

### <a name="hiding-column-names"></a>Skjule kolonnenavne
Ved gruppering af data viser standardfunktionsmåden kolonnenavnet i gruppehovedrækken. Du kan vælge at udelade kolonnenavnet i gruppehovedrækker ved at vælge **Gitterindstillinger** > **Skjul gruppekolonnenavn**.

### <a name="grouping-on-date-and-time-columns"></a>Gruppering af dato- og klokkeslætskolonner
Du kan nu gruppere efter år, måned eller dag for dato- eller dato/klokkeslætsfelter. Gruppens "værdi" i den tilsvarende overskriftsrække vil svare til formatet i det pågældende felt. Derudover kan du til dato/klokkeslæts- og klokkeslætsfelter gruppere efter time, minut eller sekund.

> [!IMPORTANT]
> Brugere kan i øjeblikket ikke tilføje en grupperingskolonne, efter de har grupperet i et segment af en dato- eller tidskolonne.

## <a name="freezing-columns"></a>Fryse kolonner
Visse kolonner i et gitter kan være så vigtige for sammenhængen, at de ikke skal rulle ud af visningen. Du vil i stedet have, at værdierne i disse kolonner altid er synlige. Funktionen **Frys kolonner i gitteret** giver denne fleksibilitet for brugerne. 

[![Fastfrysning af kolonner i gitter.](./media/gridFreezingColumns-07-25-2022.gif)](./media/gridFreezingColumns-07-25-2022.gif)

Hvis du vil fryse en kolonne, skal du højreklikke på kolonnens overskrift og derefter vælge **Frys kolonne**. Første gang du fuldfører dette trin, bliver den valgte kolonne den første kolonne, og den rulles ikke længere ud af visningen. En efterfølgende kolonne, som du fryser, vil blive tilføjet til højre for den sidste frosne kolonne. Du kan bruge standardfunktionen Flyt til at sortere frosne kolonner efter behov. Frosne kolonner kan dog ikke flyttes, så de vises mellem sættet af ikke-frosne kolonner. Frosne kolonner kan heller ikke flyttes, så de vises mellem sættet af frosne kolonner.

Hvis du vil frigøre en kolonne, skal du højreklikke på den frosne kolonnes overskrift og derefter vælge **Frigør kolonne**. 

Bemærk, at rækkevalget og rækkestatuskolonnerne i det nye gitter altid fryses som de første to kolonner. Når disse kolonner er medtaget i et gitter, er de derfor altid synlige for brugerne, uanset den vandrette rulleposition i gitteret. Disse to kolonner kan ikke omrokeres.

## <a name="autofit-column-width"></a>Tilpasse kolonnebredde automatisk
På samme måde som i Excel kan brugere automatisk tvinge en kolonne til at ændre størrelsen på baggrund af det indhold, der aktuelt vises i den. Du skal blot dobbelttrykke på (eller dobbeltklik) størrelseshåndtagene i kolonnen. Alternativt kan du placere fokus i kolonneoverskriften og derefter vælge **A**-tasten (til automatisk tilpasning).

## <a name="frequently-asked-questions"></a>Ofte stillede spørgsmål
### <a name="how-do-i-enable-the-new-grid-control-in-my-environment"></a>Hvordan aktiverer jeg det nye gitterkontrolelement i mit miljø? 

Funktionen **Nyt gitterkontrolelement** er tilgængelig direkte i funktionsstyring i ethvert miljø. Når funktionen er aktiveret i Funktionsstyring, vil alle efterfølgende brugersessioner bruge det nye gitterkontrolelement. 

Denne funktion begyndte at blive aktiveret som standard i version 10.0.21. Den er planlagt til at blive obligatorisk i oktober 2022.

## <a name="developer-opting-out-individual-pages-from-using-the-new-grid"></a>[Udvikler] Framelde enkelte sider brug af det nye gitter 
Hvis din organisation finder en side, der har nogle problemer med at bruge det nye gitter, er der en API, der giver mulighed for, at en individuel formular kan benytte det ældre gitter, samtidig med at det stadig tillader resten af systemet at anvende det nye gitterkontrolelement. Hvis du framelder en enkelt side fra det nye gitter, skal du tilføje følgende opkaldspost `super()` i `run()`-metoden for formularen.

```this.forceLegacyGrid();```

Denne API vil blive udfaset for at tillade fjernelse af det tidligere gitterkontrolelement. Den vil dog være tilgængelig i mindst 12 måneder, efter at dens udfasning er offentliggjort. Hvis der er problemer, der kræver, at denne API bruges, skal du rapportere dem til Microsoft.

### <a name="forcing-a-page-to-use-the-new-grid-after-previously-opting-out-the-grid"></a>Tvinge en side til at bruge det nye gitter, når gitteret tidligere er fravalgt
Hvis du har valgt en enkelt side fra til brug af det nye gitter, kan du senere aktivere det nye gitter igen, når de underliggende problemer er løst. Hvis du vil gøre dette, skal du blot fjerne kaldet til `forceLegacyGrid()`. Ændringen træder først i kraft, når en af følgende ting er sker:

- **Geninstallation af miljøet**: Når et miljø opdateres og geninstalleres, ryddes den tabel, der gemmer de sider, der er valgt ud af det nye gitter (FormControlReactGridState), automatisk.
- **Manuel rydning af tabellen**:Til udviklingsscenarier skal du bruge SQL til at rydde tabellen FormControlReactGridState og derefter genstarte AOS. Denne kombination af handlinger nulstiller den cachelagring af sider, der er valgt ud af det nye gitter.

## <a name="developer-opting-individual-grids-out-of-the-typing-ahead-of-the-system-capability"></a>[Udvikler] Vælge individuelle gitre uden for funktionaliteten af Skrive forud i forhold til systemet
Der er opstået scenarier, der ikke egner sig til at fungere godt sammen med *Skrive forud i forhold til systemet* i gitteret. (F.eks. vil en kode, der udløses, når en række valideres, udløse en datakildeundersøgelse, og undersøgelsen kan derefter ødelægge ikke-bekræftede redigeringer på eksisterende rækker). Hvis din organisation opdager et sådant scenario, findes der en API, som giver en udvikler mulighed for at vælge et individuelt gitter ud af den asynkrone rækkevalidering og gå tilbage til den tidligere funktionalitet.

Når asynkron rækkevalidering er deaktiveret i et gitter, kan brugere ikke oprette en ny række eller flytte til en anden eksisterende række i gitteret, mens der er valideringsproblemer for den aktuelle række. Som en sidevirkning af denne handling kan tabeller ikke indsættes fra Excel i finans og drift-gitre.

Hvis du fjerne en enkelt side fra asynkron rækkevalidering, skal du tilføje følgende kald efter `super()` i `run()`-metoden for formularen.

```<gridControl>.allowPreemptiveClient(false);```

> [!NOTE]
> - Dette kald skal kun startes i særlige tilfælde og bør ikke være normen for alle gitre.
> - Det anbefales ikke, at du skifter API under kørslen, efter at formularen er indlæst.

## <a name="developer-size-to-available-width-columns"></a>[Udvikler] "Tilpas størrelsen til tilgængelig bredde"-kolonner
Hvis en udvikler angiver egenskaben **WidthMode** til **SizeToAvailable** for kolonner i det nye gitter, har disse kolonner som udgangspunkt samme bredde, som de ville have, hvis egenskaben var angivet til **SizeToContent**. De strækkes dog for at bruge eventuel ekstra tilgængelig bredde i gitteret. Hvis egenskaben er angivet til **SizeToAvailable** for flere kolonner, deler alle kolonnerne eventuel ekstra tilgængelig bredde i gitteret. Men hvis en bruger manuelt tilpasser størrelsen på en af disse kolonner, bliver kolonnen statisk. Den forbliver på denne bredde og kan ikke længere strækkes for at bruge den ekstra tilgængelige gitterbredde.

## <a name="developer-specifying-the-column-that-receives-the-initial-focus-when-new-rows-are-created-by-using-the-down-arrow-key"></a>[Udvikler] Du kan angive den kolonne, der får den første fokusering, når der oprettes nye rækker med tasten Pil ned.
Som det blev nævnt i afsnittet [Forskelle, når der indtastes data forud for systemet](#differences-when-entering-data-ahead-of-the-system), hvis funktionen "Skrive forud i forhold til systemet" er aktiveret, og en bruger opretter en ny række ved hjælp af tasten **Pil ned**, vil standardfunktionsmåden være at sætte fokus i den første kolonne i den nye række. Dette kan være forskelligt fra erfaringen i det tidligere gitter, eller når der er valgt en **Ny**-knap.

Brugere og organisationer kan oprette gemte visninger, der er optimeret til dataindtastning. (Du kan f.eks. omarrangere kolonner, så den første kolonne er den, du vil starte med at indtaste data i). Derudover kan organisationer fra og med version 10.0.29 regulere denne funktionsmåde ved at bruge metoden **selectedControlOnCreate()**. Med denne metode kan en udvikler angive den kolonne, der får den første fokusering, når der oprettes en ny række med tasten **Pil ned**. Som input har denne API det kontrol-id, der svarer til den kolonne, som skal have den første fokusering.

## <a name="known-issues"></a>Kendte problemer
I dette afsnit vedligeholdes en liste over kendte problemer for det nye gitterkontrol.

### <a name="open-issues"></a>Aktuelle problemer
- Når funktionen **Nyt gitterkontrolelement** er aktiveret, vil nogle sider fortsat anvende det eksisterende gitterkontrolelement. Det sker i følgende situationer:
 
    - Der findes en kortliste på siden, som gengives i flere kolonner.
    - Der findes en grupperet kortliste på siden.
    - En gitterkolonne med et ikke-reagerende kontrolelement, der kan udvides.

    Når en bruger først støder på en af disse situationer, vises der en meddelelse om opdatering af siden. Når denne meddelelse vises, vil siden fortsat anvende det eksisterende gitter for alle brugere indtil den næste opdatering af produktversionen. En bedre håndtering af disse scenarier, så det nye gitter kan anvendes, vil blive betragtet som en fremtidig opdatering.

- [KB 4582758] Poster er slørede, når du ændrer zoom fra 100 til en hvilken som helst anden procent

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

