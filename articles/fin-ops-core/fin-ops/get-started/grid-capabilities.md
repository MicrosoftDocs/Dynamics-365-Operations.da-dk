---
title: Gitteregenskaber
description: I dette emne beskrives flere stærke funktioner i gitterkontrolelementet. Den nye gitterfunktion skal være aktiveret for at få adgang til disse egenskaber.
author: jasongre
ms.date: 03/03/2022
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
ms.openlocfilehash: 58a05f893549a8b9e2e5cb83d02475d0fb5b7277
ms.sourcegitcommit: 2e554371f5005ef26f8131ac27eb171f0bb57b4e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/04/2022
ms.locfileid: "8384423"
---
# <a name="grid-capabilities"></a>Gitteregenskaber

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Det nye gitterkontrolelement omfatter en række nyttige og effektive funktioner, du kan bruge til at forbedre brugernes produktivitet, oprette mere interessante visninger af dine data og få meningsfuld indsigt i dine data. Denne artikel dækker følgende funktioner: 

- Beregner totaler
- Skrive forud i forhold til systemet
- Evaluere matematiske udtryk 
- Gruppere data i tabelformat (aktiveres separat ved hjælp af funktionen **Gruppering i gitre**)
- Frysning af kolonner (aktiveres separat ved hjælp af funktionen **Frysning af kolonner i gitre**)
- Tilpasse kolonnebredde automatisk
- Kolonner, der kan strækkes

## <a name="calculating-totals"></a>Beregner totaler
I Finans- og driftsapps har brugerne mulighed for at få vist totaler nederst i numeriske kolonner i gitre. Disse totaler vises i en sektion med sidefod nederst i gitteret. 

### <a name="showing-the-grid-footer"></a>Visning af gitterets sidefod
Der er et sidefodsområde i bunden af alle tabelgitre i Finans- og driftsapps. Sidefoden kan vise værdifulde oplysninger, der er relateret til de data, der vises i gitteret. Her er nogle eksempler på sådanne oplysninger:

- Antallet af markerede rækker i tabellen (når du markerer mere end én post)
- Samlede beløb nederst i konfigurerede og numeriske kolonner
- Antallet af rækker i datasættet 

Denne sidefod er som standard skjult, men du kan slå den til. Hvis du vil have vist sidefoden for et gitter, skal du vælge knappen **Gitterindstillinger** i gitteroverskriften og vælge indstillingen **Vis sidefod**. Når du har aktiveret sidefoden i et bestemt gitter, huskes denne indstilling, indtil brugeren vælger at skjule sidefoden. Hvis du vil skjule sidefoden, skal du vælge **Skjul sidefod** i menuen **Gitterindstillinger**.

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

Hvis beregningen tager lang tid at fuldføre, kan du annullere operationen ved at klikke på knappen **Annuller**. Nogle gange vil datasættet være for stort til at kunne beregne totaler (en begrænsning, der er pålagt af organisationen), og du vil i stedet blive mindet om at filtrere dine data mere. 

> [!NOTE]
> Systemadministrationer kan ændre grænsen for det antal poster, der er tilgængelige til beregning af totaler, ved at justere det **maksimale antal lokale poster for hver gitter**-parameteren på siden **Indstillinger for klientydeevne**. Standardværdien er 25.000 poster. Administratorer skal være omhyggelige, når de justerer denne værdi, da en for stor værdi kan opbruge den ledige hukommelse på brugerens computer. Anbefalingen er ikke at overstige 50.000 poster.   

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
Brugerne har altid været i stand til at eksportere data fra gitre i Finans- og driftsapps til Microsoft Excel ved hjælp af mekanismen **Eksportér til Excel**. Muligheden for at indtaste data forud i systemet gør det dog muligt for det nye gitter at understøtte kopiering af tabeller fra Excel og indsætning af dem direkte i gitre i Finans- og driftsapps. Den gittercelle, som indsætningen er initieret fra, bestemmer, hvor den kopierede tabel begynder at blive indsat. Indholdet af gitteret overskrives med indholdet af den kopierede tabel, undtagen i to tilfælde:

- Hvis antallet af kolonner i den kopierede tabel overstiger antallet af kolonner, der er tilbage i gitteret, startende fra indsætningens sted, får brugeren besked om, at de ekstra kolonner er blevet ignoreret. 
- Hvis antallet af rækker i den kopierede tabel overstiger antallet af rækker i gitteret med start fra indsætningens sted, overskrives de eksisterende celler af det indsatte indhold, og eventuelle ekstra rækker fra den kopierede tabel indsættes som nye rækker nederst i gitteret. 

## <a name="evaluating-math-expressions"></a>Evaluere matematiske udtryk
Som en produktivitetsbooster kan brugerne indtaste matematiske formler i numeriske celler i et gitter. De behøver ikke at foretage beregningen i en app uden for systemet. Hvis du f.eks. angiver **=15\*4** og derefter trykker på tasten **Tab** for at flytte ud af feltet, evalueres udtrykket, og værdien **60** gemmes for feltet.

Hvis du vil have systemet til at genkende en værdi som et udtryk, skal du starte værdien med et lighedstegn (**=**). Du kan få flere oplysninger om de understøttede operatorer og den understøttede syntaks i [Understøttede matematiske symboler](http://bugwheels94.github.io/math-expression-evaluator/#supported-maths-symbols).

## <a name="grouping-tabular-data"></a>Gruppere data i tabelformat
Forretningsbrugere har ofte brug for at udføre ad hoc-analyse af data. Dette kan gøres ved at eksportere data til Microsoft Excel og bruge pivottabeller, men funktionen **Gruppering i gitre**, der er afhængig af den nye gitterkontrol, tillader brugere at organisere deres tabeldata på interessante måder i Finans- og driftsapps. Da denne funktion udvider funktionen **Totaler**, giver **Gruppering** også mulighed for at få meningsfuld indsigt i dataene ved at levere subtotaler på gruppeniveau.

Hvis du vil bruge denne funktion, skal du højreklikke på den kolonne, du vil gruppere efter, og vælge **Gruppér efter denne kolonne**. Denne handling sorterer dataene efter den valgte kolonne, føjer en ny **Gruppér efter**-kolonne til starten af gitteret og indsætter "overskriftsrækker" i starten af hver gruppe. Disse kolonneoverskrifter indeholder følgende oplysninger om hver enkelt gruppe:

- Dataværdi for gruppen 
- Kolonnenavn (disse oplysninger vil især være nyttige, når du har flere grupperingsniveauer)
- Antallet af datarækker i denne gruppe
- Subtotaler for enhver kolonne, der er konfigureret til at vise totaler

Når [Gemte visninger](saved-views.md) er aktiveret, kan denne gruppering gemmes via tilpasning som del af en visning for at få hurtig adgang, når du næste gang besøger siden.

### <a name="multiple-levels-of-grouping"></a>Flere grupperingsniveauer
Når du har grupperet data efter en enkelt kolonne, kan du gruppere dataene efter en anden kolonne ved at vælge **Gruppér efter denne kolonne** i den ønskede kolonne. Denne proces kan gentages, indtil du har fem indlejrede grupperingsniveauer, hvilket er den maksimalt understøttede dybde. Derefter kan du ikke længere gruppere efter yderligere kolonner.

Du kan altid fjerne grupperingen efter en hvilken som helst kolonne ved at højreklikke på den pågældende kolonne og vælge **Opdel gruppe**. Du kan også fjerne grupperingen fra alle kolonner ved at vælge **Gitterindstillinger** og derefter **Opdele alle**.

### <a name="sorting-grouped-data"></a>Sortere grupperede data
Når du har grupperet data efter en eller flere kolonner, kan du ændre sorteringsretningen for enhver grupperingskolonne gennem den tilsvarende kolonneoverskrift. 

Funktionaliteten, når du sorterer på ikke-grupperede kolonner, afhænger af produktversionen:

- Hvis du sorterer en kolonne, der ikke er grupperet, i version 10.0.24 og tidligere, fjernes grupperingen fra alle kolonner, og dataene sorteres i den valgte kolonne. 
- Hvis du sorterer en kolonne, der ikke er grupperet, i version 10.0.25 og senere, bevares grupperingen, og dataene sorteres i hver gruppe på basis af den valgte kolonne.

### <a name="expanding-and-collapsing-groups"></a>Udvide og skjule grupper
Den oprindelige gruppering af data vil få alle grupper udvidet. Du kan oprette opsummerede visninger af dataene ved at skjule de enkelte grupper, eller du kan bruge gruppeudvidelse og skjulning som hjælp til at navigere gennem dataene. Hvis du vil udvide eller skjule en gruppe, skal du vælge knappen vinkeltegn (>) i den tilsvarende gruppeoverskriftsrække. Bemærk, at de enkelte gruppers udvidede/skjulte tilstand **ikke** gemmes i personlig tilpasning.

### <a name="selecting-and-unselecting-rows-at-the-group-level"></a>Markere og fjerne markering af rækker på gruppeniveau
På samme måde som du kan markere (eller fjerne markeringen af) alle rækker i gitteret ved at markere afkrydsningsfeltet øverst i den første kolonne af gitteret, kan du også hurtigt markere (eller fjerne markeringen af) alle rækkerne i en gruppe ved at markere afkrydsningsfeltet i den tilsvarende gruppehovedrække. Afkrydsningsfeltet i gruppehovedrækken afspejler altid den aktuelle valgtilstand for rækker i den pågældende gruppe, uanset om alle eller ingen rækker er markeret, eller kun bestemte rækker er markeret.

### <a name="hiding-column-names"></a>Skjule kolonnenavne
Ved gruppering af data viser standardfunktionsmåden kolonnenavnet i gruppehovedrækken. Du kan vælge at udelade kolonnenavnet i gruppehovedrækker ved at vælge **Gitterindstillinger** > **Skjul gruppekolonnenavn**.

### <a name="grouping-on-date-and-time-columns"></a>Gruppering af dato- og klokkeslætskolonner
Fra og med version 10.0.24 er indstillingen føjet til gruppen efter år, måned eller dag for dato- eller dato/klokkeslætsfelter. Gruppens "værdi" i den tilsvarende overskriftsrække vil svare til formatet i det pågældende felt. Derudover kan du til dato/klokkeslæts- og klokkeslætsfelter gruppere efter time, minut eller sekund. 

## <a name="freezing-columns"></a>Fryse kolonner
Visse kolonner i et gitter kan være så vigtige for sammenhængen, at de ikke skal rulle ud af visningen. Du vil i stedet have, at værdierne i disse kolonner altid er synlige. Funktionen **Frys kolonner i gitteret** giver denne fleksibilitet for brugerne. 

Hvis du vil fryse en kolonne, skal du højreklikke på kolonnens overskrift og derefter vælge **Frys kolonne**. Første gang du fuldfører dette trin, bliver den valgte kolonne den første kolonne, og den rulles ikke længere ud af visningen. En efterfølgende kolonne, som du fryser, vil blive tilføjet til højre for den sidste frosne kolonne. Du kan bruge standardfunktionen Flyt til at sortere frosne kolonner efter behov. Frosne kolonner kan dog ikke flyttes, så de vises mellem sættet af ikke-frosne kolonner. Frosne kolonner kan heller ikke flyttes, så de vises mellem sættet af frosne kolonner.

Hvis du vil frigøre en kolonne, skal du højreklikke på den frosne kolonnes overskrift og derefter vælge **Frigør kolonne**. 

Bemærk, at rækkevalget og rækkestatuskolonnerne i det nye gitter altid fryses som de første to kolonner. Når disse kolonner er medtaget i et gitter, er de derfor altid synlige for brugerne, uanset den vandrette rulleposition i gitteret. Disse to kolonner kan ikke omrokeres.

## <a name="autofit-column-width"></a>Tilpasse kolonnebredde automatisk
På samme måde som i Excel kan brugere automatisk tvinge en kolonne til at ændre størrelsen på baggrund af det indhold, der aktuelt vises i den pågældende kolonne. Det gør du ved at dobbeltklikke på størrelseshåndtagene i kolonnen eller ved at fokusere i kolonneoverskriften og trykke på **A** (for automatisk tilpasning). Denne funktion er tilgængelig fra og med version 10.0.23.

## <a name="frequently-asked-questions"></a>Ofte stillede spørgsmål
### <a name="how-do-i-enable-the-new-grid-control-in-my-environment"></a>Hvordan aktiverer jeg det nye gitterkontrolelement i mit miljø? 

Funktionen **Nyt gitterkontrolelement** er tilgængelig direkte i funktionsstyring i ethvert miljø. Når funktionen er aktiveret i Funktionsstyring, vil alle efterfølgende brugersessioner bruge det nye gitterkontrolelement. 

Denne funktion aktiveres som standard med start i version 10.0.21 og er planlagt til at blive obligatorisk i version 10.0.25. 

## <a name="developer-opting-out-individual-pages-from-using-the-new-grid"></a>[Udvikler] Framelde enkelte sider brug af det nye gitter 
Hvis din organisation finder en side, der har nogle problemer med at bruge det nye gitter, er der en API, der giver mulighed for, at en individuel formular kan benytte det ældre gitter, samtidig med at det stadig tillader resten af systemet at anvende det nye gitterkontrolelement. Hvis du framelder en enkelt side fra det nye gitter, skal du tilføje følgende opkaldspost `super()` i `run()`-metoden for formularen.

```this.forceLegacyGrid();```

Denne API anvendes, indtil det nye gitterkontrolelement bliver obligatorisk. Denne ændring er i øjeblikket programsat til oktober 2022. Hvis der er problemer, der kræver, at denne API bruges, skal du rapportere dem til Microsoft.

### <a name="forcing-a-page-to-use-the-new-grid-after-previously-opting-out-the-grid"></a>Tvinge en side til at bruge det nye gitter, når gitteret tidligere er fravalgt
Hvis du har valgt en enkelt side fra til brug af det nye gitter, kan du senere aktivere det nye gitter igen, når de underliggende problemer er løst. Hvis du vil gøre dette, skal du blot fjerne kaldet til `forceLegacyGrid()`. Ændringen træder først i kraft, når en af følgende ting er sker:

- **Geninstallation af miljøet**: Når et miljø opdateres og geninstalleres, ryddes den tabel, der gemmer de sider, der er valgt ud af det nye gitter (FormControlReactGridState), automatisk.
- **Manuel rydning af tabellen**:Til udviklingsscenarier skal du bruge SQL til at rydde tabellen FormControlReactGridState og derefter genstarte AOS. Denne kombination af handlinger nulstiller den cachelagring af sider, der er valgt ud af det nye gitter.

## <a name="developer-opting-individual-grids-out-of-the-typing-ahead-of-the-system-capability"></a>[Udvikler] Vælge individuelle gitre uden for funktionaliteten af Skrive forud i forhold til systemet
Der er opstået scenarier, der ikke egner sig til at fungere godt sammen med *Skrive forud i forhold til systemet* i gitteret. (F.eks. vil en kode, der udløses, når en række valideres, udløse en datakildeundersøgelse, og undersøgelsen kan derefter ødelægge ikke-bekræftede redigeringer på eksisterende rækker). Hvis din organisation opdager et sådant scenario, findes der en API, som giver en udvikler mulighed for at vælge et individuelt gitter ud af den asynkrone rækkevalidering og gå tilbage til den tidligere funktionalitet.

Når asynkron rækkevalidering er deaktiveret i et gitter, kan brugere ikke oprette en ny række eller flytte til en anden eksisterende række i gitteret, mens der er valideringsproblemer for den aktuelle række. Som en sidevirkning af denne handling kan tabeller ikke indsættes fra Excel i finans- og driftsgitre.

Hvis du fjerne en enkelt side fra asynkron rækkevalidering, skal du tilføje følgende kald efter `super()` i `run()`-metoden for formularen.

```<gridControl>.allowPreemptiveClient(false);```

> [!NOTE]
> - Dette kald skal kun startes i særlige tilfælde og bør ikke være normen for alle gitre.
> - Det anbefales ikke, at du skifter API under kørslen, efter at formularen er indlæst.

## <a name="developer-size-to-available-width-columns"></a>[Udvikler] "Tilpas størrelsen til tilgængelig bredde"-kolonner
Hvis en udvikler angiver egenskaben **WidthMode** til **SizeToAvailable** for kolonner i det nye gitter, har disse kolonner som udgangspunkt samme bredde, som de ville have, hvis egenskaben var angivet til **SizeToContent**. De strækkes dog for at bruge eventuel ekstra tilgængelig bredde i gitteret. Hvis egenskaben er angivet til **SizeToAvailable** for flere kolonner, deler alle kolonnerne eventuel ekstra tilgængelig bredde i gitteret. Men hvis en bruger manuelt tilpasser størrelsen på en af disse kolonner, bliver kolonnen statisk. Den forbliver på denne bredde og kan ikke længere strækkes for at bruge den ekstra tilgængelige gitterbredde.

## <a name="known-issues"></a>Kendte problemer
I dette afsnit vedligeholdes en liste over kendte problemer for det nye gitterkontrol.

### <a name="open-issues"></a>Aktuelle problemer
- Når funktionen **Nyt gitterkontrolelement** er aktiveret, vil nogle sider fortsat anvende det eksisterende gitterkontrolelement. Det sker i følgende situationer:
 
    - Der findes en kortliste på siden, som gengives i flere kolonner.
    - Der findes en grupperet kortliste på siden.
    - En gitterkolonne med et ikke-reagerende kontrolelement, der kan udvides.

    Når en bruger først støder på en af disse situationer, vises der en meddelelse om opdatering af siden. Når denne meddelelse vises, vil siden fortsat anvende det eksisterende gitter for alle brugere indtil den næste opdatering af produktversionen. En bedre håndtering af disse scenarier, så det nye gitter kan anvendes, vil blive betragtet som en fremtidig opdatering.

- [KB 4582758] Poster er slørede, når du ændrer zoom fra 100 til en hvilken som helst anden procent
- [KB 4592012] Uventet klientfejl i IE11, når der indsættes flere linjer fra Excel

    Microsoft gør ikke noget ved dette problem


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
