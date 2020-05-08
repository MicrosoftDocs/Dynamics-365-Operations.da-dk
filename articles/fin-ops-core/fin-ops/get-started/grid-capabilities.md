---
title: Gitteregenskaber
description: I dette emne beskrives flere stærke funktioner i gitterkontrolelementet. Den nye gitterfunktion skal være aktiveret, hvis der skal være adgang til disse egenskaber.
author: jasongre
manager: AnnBe
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: fd45f71fc15e467c461433682310ab7b7cc0158a
ms.sourcegitcommit: 0d7b700950b1f95dc030ceab5bbdfd4fe1f79ace
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/23/2020
ms.locfileid: "3284398"
---
# <a name="grid-capabilities"></a>Gitteregenskaber

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Det nye gitterkontrolelement omfatter en række nyttige og effektive funktioner, der kan bruges til at forbedre brugernes produktivitet, oprette mere interessante visninger af dine data og få meningsfuld indsigt i dine data. Denne artikel dækker følgende funktioner: 

-  Beregner totaler
-  Gruppering af data
-  Skrive forud i forhold til systemet
-  Evaluere matematiske udtryk 

## <a name="calculating-totals"></a>Beregner totaler
I Finance and Operations-apps har brugerne mulighed for at få vist totaler nederst i numeriske kolonner i gitre. Disse totaler vises i en sektion med sidefod nederst i gitteret. 

### <a name="showing-the-grid-footer"></a>Visning af gitterets sidefod
Der er et sidefodsområde i bunden af alle tabelgitre i Finance and Operations-apps. Sidefoden kan vise værdifulde oplysninger, der er relateret til de data, der vises i gitteret. Her er nogle eksempler på sådanne oplysninger:

- Antallet af markerede rækker i tabellen (når der er valgt mere end én post)
- Samlede beløb nederst i konfigurerede og numeriske kolonner
- Antallet af rækker i datasættet 

Denne sidefod er som standard skjult, men den kan let aktiveres. Hvis du vil have vist sidefoden for et gitter, skal du højreklikke på kolonneoverskriften i gitteret og vælge indstillingen **Vis sidefod**. Når sidefoden er aktiveret for et bestemt gitter, vil denne indstilling blive husket, indtil brugeren vælger at skjule sidefoden, hvilket kan gøres ved at højreklikke på en kolonneoverskrift og vælge **Skjul sidefod**.  Bemærk, at handlingen **Vis sidefod/Skjul sidefod** forventes at få ny placering i en senere opdatering. 

### <a name="specifying-columns-with-totals"></a>Angive kolonner med totaler
I øjeblikket vil ingen kolonner blive konfigureret til at vise totaler som standard. Dette betragtes i stedet for som en aktivitet til engangsopsætning, der svarer til at justere kolonnebredden i gitre. Når du har angivet, at du vil have vist totaler for en kolonne, vil denne indstilling blive husket, næste gang du besøger siden.  

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

## <a name="grouping-data"></a>Gruppering af data
Forretningsbrugere har ofte brug for at udføre ad hoc-analyse af data. Dette kan gøres ved at eksportere data til Microsoft Excel, og ved brug af pivottabeller tillader funktionen **Gruppering** i gitre i tabelform brugere at organisere deres data på interessante måder i Finance and Operations-apps. Da denne funktion udvider funktionen **Totaler**, giver **Gruppering** også mulighed for at få meningsfuld indsigt i dataene ved at levere subtotaler på gruppeniveau.

Hvis du vil bruge denne funktion, skal du højreklikke på den kolonne, du vil gruppere efter, og vælge **Gruppér efter denne kolonne**. Denne handling sorterer dataene efter den valgte kolonne, føjer en ny "Gruppér efter kolonne" til starten af gitteret og indsætter "overskriftsrækker" i starten af hver gruppe. Disse kolonneoverskrifter indeholder følgende oplysninger om hver enkelt gruppe: 
-  Dataværdi for gruppen 
-  Kolonneetiket (disse oplysninger vil især være nyttige, når der ydes støtte til grupper på flere niveauer.)
-  Antallet af datarækker i denne gruppe
-  Subtotaler for enhver kolonne, der er konfigureret til at vise totaler

Når [Gemte visninger](saved-views.md) er aktiveret, kan denne gruppering gemmes via tilpasning som del af en visning for at få hurtig adgang, når du næste gang besøger siden.  

Hvis du vælger **Gruppér efter denne kolonne** for en anden kolonne, erstattes den oprindelige gruppering, da kun et grupperingsniveau understøttes i version 10.0.9 med platformsopdatering 33.

Hvis du vil fortryde gruppering i et gitter, skal du højreklikke på grupperingskolonnen og vælge **Opdel gruppe**.  

## <a name="typing-ahead-of-the-system"></a>Skrive forud i forhold til systemet
I mange forretningsscenarier er muligheden for hurtigt at indtaste data i systemet meget vigtig. Før det nye gitterkontrolelement blev introduceret, kunne brugerne kun ændre data i den aktuelle række. Før de kunne oprette en ny række eller skifte til en anden række, var de tvunget til at vente på, at systemet havde valideret eventuelle ændringer. I et forsøg på at reducere den mængde tid, som brugerne venter på, at disse valideringer udføres, og for at forbedre brugerproduktiviteten justerer det nye gitter disse valideringer, så de er asynkrone. Brugeren kan derfor flytte til andre rækker for at foretage ændringer, mens tidligere valideringer af rækker venter. 

For at understøtte denne nye funktionsmåde er der tilføjet en ny kolonne for rækkestatus øverst i gitteret, når gitteret er i redigeringstilstand. Denne kolonne angiver en af følgende statusser:

- **Tom** – Intet statusbillede angiver, at rækken er blevet gemt af systemet.
- **Afventer behandling** – Denne status angiver, at ændringerne i rækken endnu ikke er gemt af serveren, men de er i en kø med ændringer, der skal behandles. Før du udfører en handling uden for gitteret, skal du vente på, at alle ventende ændringer behandles. Desuden er teksten i disse rækker kursiv for at angive den ikke-gemte status for rækkerne. 
- **Valideringsadvarsel** – Denne status angiver, at systemet ikke kan gemme ændringerne i rækken grundet et valideringsproblem. I det gamle gitter blev du tvunget tilbage til rækken for at løse problemet med det samme. Men i det nye gitter får du besked om, at der er opstået et valideringsproblem, men du kan beslutte, hvornår eventuelle problemer skal løses i rækken. Når du er klar til at løse problemet, kan du manuelt flytte fokus tilbage til rækken. Du kan også vælge funktionen **Løs dette problem**. Denne handling flytter øjeblikkeligt fokus tilbage til den række, hvor problemet er, og giver dig mulighed for at foretage ændringer i eller uden for gitteret. Bemærk, at behandlingen af efterfølgende ventende rækker standses, indtil denne valideringsadvarsel er løst. 
- **Midlertidigt afbrudt** – Denne status angiver, at behandlingen af serveren er sat på pause, fordi validering af rækken udløste en pop op-dialogboks, der kræver brugerinput. Da brugeren måske indtaster data i en anden række, vises pop op-dialogboksen ikke med det samme for den pågældende bruger. Den vises i stedet, når brugeren vælger at genoptage behandlingen. Denne status er ledsaget af en besked, der oplyser brugeren om situationen. Beskeden indeholder handlingen **Fortsæt behandling**, der vil udløse pop op-dialogboksen.  
    
Når brugerne indtaster data før det sted, hvor serveren behandler data, kan de forvente en række degraderinger i dataindtastningsoplevelsen, f.eks. manglende opslag, validering på kontrolniveau og indtastning af standardværdier. Brugere, der har brug for en rulleliste til at finde en værdi, anbefales at vente på, at serveren når til den aktuelle række. Validering på kontrolniveau og angivelse af standardværdier vil også finde sted, når serveren behandler den pågældende række.   

### <a name="pasting-from-excel"></a>Indsætning fra Excel
Brugerne har altid været i stand til at eksportere data fra gitre i Finance and Operations-apps til Excel ved hjælp af mekanismen **Eksportér til Excel**. Muligheden for at indtaste data forud i systemet gør det dog muligt for det nye gitter at understøtte kopiering af tabeller fra Excel og indsætning af dem direkte i gitre i Finance and Operations-apps. Den gittercelle, som indsætningen er initieret fra, bestemmer, hvor den kopierede tabel begynder at blive indsat. Indholdet af gitteret overskrives med indholdet af den kopierede tabel, undtagen i to tilfælde:

- Hvis antallet af kolonner i den kopierede tabel overstiger antallet af kolonner, der er tilbage i gitteret, startende fra indsætningens sted, får brugeren besked om, at de ekstra kolonner er blevet ignoreret. 
- Hvis antallet af rækker i den kopierede tabel overstiger antallet af rækker i gitteret med start fra indsætningens sted, overskrives de eksisterende celler af det indsatte indhold, og eventuelle ekstra rækker fra den kopierede tabel indsættes som nye rækker nederst i gitteret. 

## <a name="evaluating-math-expressions"></a>Evaluere matematiske udtryk
Som en produktivitetsbooster kan brugerne indtaste matematiske formler i numeriske celler i et gitter. De behøver ikke at foretage beregningen i en app uden for systemet. Hvis du f.eks. angiver **=15\*4** og derefter trykker på tasten **Tab** for at flytte ud af feltet, evalueres udtrykket, og værdien **60** gemmes for feltet.

Hvis du vil have systemet til at genkende en værdi som et udtryk, skal du starte værdien med et lighedstegn (**=**). Du kan få flere oplysninger om de understøttede operatorer og den understøttede syntaks i [Understøttede matematiske symboler](http://bugwheels94.github.io/math-expression-evaluator/#supported-maths-symbols).

## <a name="frequently-asked-questions"></a>Ofte stillede spørgsmål
### <a name="how-do-i-enable-the-new-grid-control-in-my-environment"></a>Hvordan aktiverer jeg det nye gitterkontrolelement i mit miljø? 

**10.0.9/Platformopdatering 33 og nyere** **Nyt gitterkontrolelement**-funktionen er tilgængelig direkte i Funktionsstyring i et hvilket som helst miljø. Ligesom andre funktioner i offentlige prøveversioner er aktivering af denne funktion i produktion underlagt [Supplerende aftale om vilkår for anvendelse](https://go.microsoft.com/fwlink/?linkid=2105274).  

**10.0.8/Platformopdatering 32 og10.0.7/Platformopdatering 31** Funktionen **Nyt gitterkontrolelement** kan aktiveres i miljøer på niveau 1 (udvikling/test) og niveau 2 (sandkasse), hvis du vil foretage yderligere test- og designændringer ved at følge trinnene nedenfor.

1.  **Aktivér flyvningen**: Udfør følgende SQL-sætning: 

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, enabled, FLIGHTSERVICEID, PARTITION) VALUES('CLIReactGridEnableFeature', 1, 0, 5637144576);`

2. **Nulstil IIS** for at rydde den statiske flighting-cache. 

3.  **Find funktionen**: Gå til arbejdsområdet **Funktionsstyring**. Hvis **Nyt gitterkontrolelement** ikke vises på listen over alle funktioner, skal du vælge **Søg efter opdateringer**.   

4.  **Aktivér funktionen**: Find funktionen **Nyt gitterkontrolelement** på listen over funktioner, og vælg **Aktivér nu** i detaljeruden. Bemærk, at browseren skal opdateres. 

Alle efterfølgende brugersessioner vil starte med det nye kontrolelement aktiveret.

## <a name="known-issues"></a>Kendte problemer
I dette afsnit findes en liste over kendte problemer i forbindelse med den nye gitterkontrol, mens funktionen er i prøvetilstand.  

### <a name="open-issues"></a>Aktuelle problemer

- Kortlister, der blev gengivet som flere kolonner, gengives nu som en enkelt kolonne.
- Grupperede lister gengives ikke som grupper eller i separate kolonner.
- Der vises ikke værktøjstip til billeder.
- Visningen af gitterlinjer fungerer ikke for alle felttyper.
- Periodisk kan du ikke klikke uden for gitteret, når du f.eks. vælger flere rækker.
- Indstillingerne **Valider** og **Kopiér** i Arbejdsrutineoptager er ikke tilgængelige for dato- og nummerkontrolelementer.

### <a name="fixed-as-part-of-10012"></a>Rettet i 10.0.12

> [!Note]
> Følgende oplysninger er tilgængelige, så du kan planlægge i overensstemmelse hermed. Du kan finde flere oplysninger om tidsplanen for version 10.0.12 under [Tilgængelighed af tjenesteopdatering](../../fin-ops/get-started/public-preview-releases.md).

- [Problem 429126] Kontrolelementer uden for gitteret opdateres ikke, når den sidste post er slettet.
- [Problem 430575] Tabelkontrolelementer opdaterer ikke indholdet af viste elementer.
- [KB 4558570] Der vises stadig elementer på siden, når posten er blevet slettet.
- [KB 4558584] Negative tal gengives ikke korrekt.
- [KB 4558575] Felter opdateres ikke, når en rækkeændring/gitterbehandling sidder fast efter sletning af rækker.
- [Problem 436980] Den formatering, der er knyttet til listepanelet **ExtendedStyle**, anvendes ikke.
- [KB 4558573] Valideringsfejl kan ikke rettes, når den nødvendige ændring er uden for gitteret.
    
### <a name="quality-update-for-10011"></a>Kvalitetsopdatering for 10.0.11

- [KB 4558381] Negative tal gengives ikke korrekt, og brugerne vil sommetider blive fastlåst, efter at der er registreret valideringsproblemer.

### <a name="fixed-as-part-of-10011"></a>Rettet i 10.0.11

- [KB 4558374] Poster, der kræver dialogboks med polymorf vælger, kan ikke oprettes.
- [KB 4558382] Der opstår uventede klientfejl.
- [KB 4558375] Der vises ingen hjælpetekst på kolonner i det nye gitter.
- [KB 4558376] Listepanelets gitre gengives ikke med den korrekte højde i Internet Explorer.
- [KB 4558377] Kombinationsfeltkolonner, der har **SizeToAvailable**-bredde, gengives ikke på visse sider.
- [KB 4549711] Linjer i et betalingsforslag kan ikke fjernes korrekt, når det nye gitterkontrolelement er aktiveret.
- [KB 4558378] Detaljeadgang åbner nogle gange den forkerte post.
- [KB 4558379] Der opstår en fejl, når opslag åbnes, hvor **ReplaceOnLookup**=**Nej**.
- [KB 4558380] Den ledige plads i gitteret udfyldes ikke straks, når en del af siden er skjult.
- [Problem 432458] Tomme eller dublerede linjer vises i starten af nogle underordnede samlinger.
- [KB 4558587] Referencegrupper, der indeholder kombinationsbokse for erstatningsfelter, viser ikke værdier.

### <a name="fixed-as-part-of-10010"></a>Rettet i 10.0.10

- [Problem 414301] Nogle data fra tidligere linjer forsvinder, når der oprettes nye linjer.
- [KB 4550367] Tidsværdier formateres ikke korrekt.
- [KB 4549734] Aktive rækker behandles ikke som markerede, hvis markeringskolonnen er skjult.
- [Fejl 417044] Der er ingen meddelelse om tomt gitter for listetypegitre.
- [KB 4558367] Tekstmarkering er inkonsekvent, når rækkerne ændres.
- [KB 4558372] Det nye gitter sidder fast i behandlingstilstand, hvis antallet af kolonner i det indhold, der indsættes, overstiger antallet af resterende kolonner i gitteret.
- [KB 4558368] Flere valg via tastaturet er tilladt i enkeltvalgsscenarier.
- [KB 4539058] Nogle gitre (typisk i oversigtspanelerne) kan nogle gange ikke gengives (men gengives, hvis du zoomer ud).
- [KB 4558369] Statusbilleder forsvinder i det hierarkiske gitter.
- [KB 4558370] En ny række rulles ikke ind i visningen.
- [KB 4549796] Værdier kan ikke redigeres i et gitter, når det er i visningstilstand.

### <a name="quality-update-for-1009platform-update-33"></a>Kvalitetsopdatering til 10.0.9/Platform update 33

- [KB 4550367] Tidsværdier formateres ikke korrekt.
