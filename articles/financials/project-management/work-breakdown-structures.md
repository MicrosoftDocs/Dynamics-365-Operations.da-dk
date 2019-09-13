---
title: Oversigt over arbejdsopgavehierarkier
description: Et arbejdsopgavehierarki (WBS) er en beskrivelse af det arbejde, der udføres for et projekt. Det er et hierarki af opgaver, der repræsenterer projektgruppens kendskab til sammensætning af arbejde og til størrelse, omkostninger og varighed af den enkelte komponent eller opgave.
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWorkBreakdownStructure
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23861
ms.assetid: 241a0464-0056-4a69-b468-0afbe2d5f3ae
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 78509898d0c2279750df3860a670d3d7a6badfc0
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865574"
---
# <a name="work-breakdown-structures-overview"></a>Oversigt over arbejdsopgavehierarkier

[!include [banner](../includes/banner.md)]

Et arbejdsopgavehierarki (WBS) er en beskrivelse af det arbejde, der udføres for et projekt. Det er et hierarki af opgaver, der repræsenterer projektgruppens kendskab til sammensætning af arbejde og til størrelse, omkostninger og varighed af den enkelte komponent eller opgave. En WBS har tre overordnede formål:

-   Beskriv opdelingen eller sammensætningen af arbejde på opgaver.
-   Planlæg projektarbejdet.
-   Vurder omkostningen for hver opgave.

Detaljeringsgraden i et WBS afhænger af niveauet af nøjagtighed, der kræves i estimater og niveauet for registrering, der kræves mod disse estimater. Projekter, som har meget lav tolerance for forsinkelser i tidsplan eller omkostninger, kræver normalt en mere detaljeret WBS og omhyggelig sporing af igangværende arbejder og omkostninger i forhold til WBS. Denne type projekt er almindelige inden for bygge og anlæg og tekniske brancher. 

Projekter inden for brancher som medier og reklame, software og it-infrastruktur har derimod tendens til at være enkeltstående, og produktivitet er i forhold til erfaring og kompetence hos den person, der udfører opgaven. Derfor bruger disse brancher en WBS til at få en tilnærmelse af størrelsen af et projekt, ikke for at spore status for projektet i detaljer. 

Oprettelse af en Arbejdsopdelingsstruktur er en intensiv proces, der normalt sker over en lang periode, og som kræver samarbejde og oplysninger fra en lang række personer. Dette emne beskriver, hvordan du kan bruge WBS-forbedringer i Microsoft Dynamics 365 for Finance and Operations til at opfylde dine krav til estimater og sporing.

## <a name="prerequisites-for-creating-a-wbs"></a>Forudsætninger for oprettelse af en Arbejdsopdelingsstruktur
Hvis du vil oprette en WBS, skal du kunne oprette en arbejdsplan og anslå omkostningerne ved arbejde.

### <a name="prerequisites-for-creating-a-work-schedule"></a>Forudsætninger for oprettelse af en arbejdsplan

Hvis du vil bruge de fulde planlægningsfunktionerne i WBS-funktionerne, skal du udføre følgende opsætning:

1.  Oprette en standardkalender og en projektkalender:
    1.  Klik på **Projektstyring og regnskab** &gt; **Opsætning** &gt; **Parametre for projektstyring og regnskab** &gt; **Planlægning**. Angiv en standardkalender i feltet **Standardarbejdskalender**. Det vil være standardarbejdskalenderen for et nyt projekt, der oprettes.
    2.  Du kan ændre standardkalenderen for et bestemt projekt. Klik på projektets side med oplysninger, og opdater derefter feltet **Planlægningskalender** i oversigtspanelet **Projektteam og planlægning** ved at vælge en anden kalender.

2.  Konfigurer standardarbejdsdage og arbejdstimer. Den kalender, du angiver som arbejdskalenderen for projektet, vil blive brugt i WBS til at bestemme følgende oplysninger:

-   Arbejdsdage og fridage
-   Antallet af arbejdstimer i løbet af dagen

Når du vil angive arbejdsdage og arbejdstimer for en kalender eller oprette en ny kalender, skal du klikke på **Virksomhedsadministration** &gt; **Fælles** &gt; **Kalendere**.

### <a name="prerequisites-for-estimating-the-cost-of-work"></a>Forudsætningerne for forkalkulationen af omkostninger ved arbejde

Hvis du vil bruge den fulde funktionalitet til forkalkulation af WBS, skal du konfigurere omkostnings- og salgspriser for arbejdere, kategorier af arbejdskraft, udgifter og gebyrer og varer.

-   Hvis du vil konfigurere kost- og salgsprisen for arbejdskraft, udgifter og gebyrkategorier, skal du klikke på **Projektstyring og regnskab** &gt; **Opsætning** &gt; **Priser**.
-   Når du vil konfigurere kost-og salgsprisen for varer, skal du bruge siden **Samhandelsaftaler** for hvert element på listesiden **Frigivne produkter** i Administration af produktoplysninger.

## <a name="creating-a-wbs"></a>Oprettelse af en WBS
Oprettelse af en Arbejdsopdelingsstruktur (WBS) omfatter tre aktiviteter:

1.  **Arbejdsopdeling** – Opret en opdeling af arbejde i håndterbare dele eller opgaver.
2.  **Arbejdsplan** – Anslå den tid, det tager at fuldføre en opgave, angiv afhængigheder for opgaven, og vælg start- og slutdatoer for opgaver.
3.  **Forkalkulation** – Anslå omkostningerne for hver opgave.

Følgende afsnit beskriver, hvordan WBS-funktionerne kan hjælpe med hver af disse aktiviteter.

### <a name="work-decomposition"></a>Arbejdsopdeling

Oprettelse af en opdeling eller en nedbrydning af arbejdet er normalt det første trin i oprettelse af en Arbejdsopdelingsstruktur. WBS-funktionaliteten understøtter følgende grundlæggende konstruktioner til opdeling af arbejde eller nedbrydning. 

**Projektets rodopgave** Projektets rodopgave er hovedopgaven for et projekt på øverste niveau. Alle andre projektopgaver oprettes under den. Navnet på rodopgaven angives altid som projektets navn. Indsats, datoer og varighed af rodnoden opsummerer værdierne for opgaverne under rodopgaven. Du kan ikke ændre egenskaberne for rodnoden eller slette den.

**Oversigt eller containeropgaver** En hovedopgave er en opgave, som har underordnede opgaver eller konstituerede under sig. En hovedopgave indeholder i sig selv ingen arbejdsindsats eller omkostninger. I stedet er arbejdstidsindsatsen og omkostninger for en hovedopgave summen af arbejdstidsforbruget og omkostningerne for dens konstituerede opgaver. Den tidligste startdato for de konstituerede opgaver bruges som startdato for hovedopgaven, og den seneste slutdato for de konstituerede opgaver opgaver bruges som slutdato. Du kan ændre navnet på en hovedopgave, men du kan ikke redigere planlægningsegenskaberne for indsats, datoer og varighed. Hvis du sletter en hovedopgave, sletter du også alle dens alle konstituerede opgaver. 

**Bladenodeopgaver** En bladnodeopgave repræsenterer den mest detaljerede arbejdspakke i projektet. En node af typen blad har en anslået indsats, et planlagt antal ressourcer, en planlagt startdato og slutdato og varighed. 

Du kan fuldføre følgende hierarkioperationer for at aktivere oprettelsen af et arbejdshierarki eller nedbrydning for et projekt. 

**Ny opgave** Enhver ny opgave, som du opretter automatisk, tilføjes under rodnoden, og et WBS-nummer tildeles automatisk til opgaven. WBS-nummeret angiver opgavens niveau i hierarkiet. For opgaver på første niveau under projektets rodopgave bruges der et nummereringsskema med 1, 2, 3 osv. For opgaver, der er under første niveau, bruges der et nummereringsskema med 1.1, 1.2, 1.3, osv. For hvert niveau, der er tilføjet under et tidligere niveau, tilføjes der en ny stiplet række tal. 

I øjeblikket kan du ikke tilpasse WBS-nummereringen. 

**Indryk opgave** Når du indrykker en opgave, bliver den underordnet den opgave, der kommer før den. WBS-nummeret på den nye underordnede opgave beregnes automatisk baseret på WBS-nummeret på den nye overordnede opgave. Den overordnede opgave er nu en hovedopgave eller en containeropgave og derfor bliver en akkumulering af de enkelte opgaver. 

> [!NOTE] 
> Når du indrykker opgaver under en opgave, der var en bladnode før indrykningen, mister den nyligt oprettede hovedopgave sine egne dater, indsats og antal ressourcer. Der bruges nu en oversigt over værdierne af sin nye konstituerede opgaver. 

**Ryk opgave ud** Når du rykker en opgave ud, er den ikke længere en konstitueret opgave til sin overordnede opgave. WBS-nummeret på denne opgave genberegnes automatisk for at afspejle opgavens nye niveau i hierarkiet. Indsats, omkostning og datoerne for opgavens tidligere overordnede opgave genberegnes for at udelukke denne opgave. 

**Flyt op og Flyt** Når du klikker på **Flyt op** og **Flyt ned**, kan du ændre placeringen af en opgave i det overordnede hierarki. Placeringen af en opgave påvirker ikke opgavens indsats, omkostninger, datoer eller varighed. WBS-nummeret for opgaven genberegnes imidlertid automatisk for at afspejle opgavens nye placering.

### <a name="schedule-estimation"></a>Vurdering af tidsplan

Planlægningsskøn er normalt det andet trin i oprettelse af en Arbejdsopdelingsstruktur. Du skal fuldføre planlægningsskøn som en bedste fremgangsmåde, efter du har oprettet opgaverne. Siden **Arbejdsopgavehierarki** i Finance and Operations består af to sektioner. Den øverste rude er beregnet til vurdering af tidsplanen, og den nederste rude indeholder fanen **Forkalkulerede omkostninger og omsætning**, som du kan bruge til forkalkulation. 
**Opgaveafhængigheder** I et WBS kan du oprette foregående relationer mellem opgaver. Når du tildeler en opgave foregående opgaver, kan denne opgave først starte, når alle dens foregående opgaver er afsluttet. Den planlagte startdato for opgaven angives automatisk til den seneste dato for alle dens forgængere. 

**Opgaveplanlægning i Microsoft Dynamics 365 for Finance and Operations** Følgende faktorer bestemmer planlægningen af bladnodeopgaver:

-   Forgængere
-   Tidsforbrug
-   Antallet af ressourcer
-   Start- og slutdatoer

Startdatoen for en bladnodeopgave, der ikke har foregående opgaver, angives automatisk til startdatoen for projektplanlægningen. Varigheden af en bladnodeopgave beregnes altid som antallet af arbejdsdage mellem dens start- og slutdatoer. 

*<strong><em>Planlægningsregler</em></strong>* Når hjælp til automatisk planlægning er aktiveret, gælder følgende regler for opgaveplanlægningen for bladnodeopgaver:

-   Start- og slutdatoer for en opgave skal være arbejdsdage ifølge projektets planlægningskalender.
-   Startdatoen for en opgave, der har foregående opgaver, angives automatisk til den seneste slutdato for alle dens forgængere.
-   Indsats for en opgave beregnes automatisk på følgende måde:

Antal personer × varighed × antal timer på en almindelig arbejdsdag i projektkalenderen. 

I nogle tilfælde kan du eventuelt afvige fra disse regler. Du kan deaktivere automatisk planlægning for at forhindre Finance and Operations i automatisk at konfigurere eller rette eventuelle egenskaber for bladnodeopgaver. Når du angiver oplysninger om en opgave, der medfører en overtrædelse af eventuelle planlægningsregler, vises et ikon for planlægningsfejl for opgaven. Hvis du ikke vil have vist planlægningsfejl, skal du klikke på **Planlægningsfejl er vist** for at slå funktionen fra. 

> [!NOTE] 
> Værdierne for en hoved- eller containeropgave beregnes fortsat som summen af værdierne af de konstituerede opgaver, uanset om hjælp til automatisk planlægning er aktiveret eller deaktiveret. 

**Afhjælpning af planlægningsfejl** Når hjælp til automatisk planlægning er aktiveret, opstår der sandsynligvis ikke planlægningsfejl. Hvis du imidlertid deaktiverer hjælp til automatisk planlægning og derefter aktiverer den igen senere, vises der muligvis ikoner for planlægningsfejl i WBS. 

**Afhjælpning af planlægningsfejl efter opgave** Når du dobbeltklikker på ikonet for planlægningsfejl for en bestemt opgave, viser en dialogboks alle planlægningsfejl for den pågældende opgave. Du kan bestemme, hvilke planlægningsfejl der skal løses for opgaven. 

**Afhjælpning af alle planlægningsfejl** Hvis du vil have Finance and Operations til at rette alle planlægningsfejl i WBS, skal du i handlingsruden klikke på **Ret alle planlægningsafvigelser**. 

> [!NOTE] 
> Denne funktion kan medføre betydelige ændringer i WBS. Fejl rettes i følgende rækkefølge:

1.  Den anslåede indsats på alle opgaver ændres, så den er lig med den kapacitet, der er defineret i projektkalenderen.
2.  Startdatoen for hver opgave er ændret, så opgaven starter, efter alle dens foregående opgaver er afsluttet.
3.  Startdatoen for hver opgave er ændret for at fjerne huller i startdatoer for foregående opgaver.

### <a name="cost-estimation"></a>Forkalkulation af kost

Som nævnt tidligere i dette dokument kan du angive forkalkulation for hver bladnodeopgave ved hjælp af fanen **Forkalkulerede omkostninger og omsætning** i den nederste rude på siden **Arbejdsopgavehierarki**. 

> [!NOTE] 
> Du kan ikke ændre forkalkulation for en hoved- eller containeropgave. Forkalkulation for en hovedopgave er lig med summen af forkalkulationen af dens bladnodeopgaver. Den forkalkulerede samlede omkostning for hver opgave beregnes som summen af de forkalkulerede omkostningsbeløb for følgende posteringstyper:

-   Arbejdsløn
-   Vare eller materiale
-   Udgifter

Transaktionstypen **Gebyr** bruges til at anslå gebyrbaseret indtægt. Denne posteringstype har ikke en omkostningskomponent, og tages derfor ikke i betragtning ikke, når omkostninger forkalkuleres. 

Transaktionstypen **Aconto** bruges til at registrere den kontraherede salgsværdi i et projekt af typen fast værdi . Denne posteringstype tages heller ikke i betragtning, når omkostninger forkalkuleres. 

Når du forkalkulere omkostninger til arbejdsløn, materialer og omkostninger for hver opgave, skal du tildele en projektkategori til de anslåede omkostninger. 

**Forkalkulation af omkostninger til arbejdskraft** For hver bladnodeopgave tildeler du en indsats i arbejdet i timer og en standardkategori. Når du opretter en tidsplan for en opgave, tilføjes forkalkulationen af arbejdsomkostninger for opgaven derfor automatisk i standardkategorien for arbejdskraft. Denne forkalkulation vises under fanen **Forkalkulerede omkostninger og omsætning** under fanen i gitteret **Linjedetaljer** for den pågældende opgave. Hvis du har brug for flere estimater over arbejdsomkostninger, kan du tilføje dem under denne fane. Hvis du øger eller reducerer timer estimatet over arbejdsomkostninger, genberegnes tidsplanen for opgaven automatisk. 

**Forkalkulation af udgifter og materialeomkostninger** Under fanen **Forkalkulerede omkostninger og omsætning** kan du også beregne udgifts- og materialeomkostninger for en opgave, hvis du har brug for estimater. 

Kost- og salgsprisen for hver estimatlinje for arbejdskraft eller udgift er baseret på den opsætning, der er defineret for hver kategori i pristabellerne i **Projektstyring og regnskab** &gt; **Opsætning** &gt; **Priser**. For varer tilføjes kost- og salgspriser som standard fra varen eller handelsaftalen på listen **Frigivne produkter** i Administration af produktoplysninger.

## <a name="tracking-progress-on-the-wbs"></a>Registrering af status for WBS
Nogle brancher sporer fremdriften for et projekt mod en Arbejdsopdelingsstruktur på et meget detaljeret niveau, mens andre følger op på fremdriften på et højere niveau i WBS. I dette afsnit beskrives, hvordan du kan bruge WBS-sporing til dine projektkrav. 

Finance and Operations har tre visninger for WBS i et projekt: visningen Planlægning, visningen Sporing af tidsforbrug og visningen Sporing af omkostninger.

### <a name="planning-view"></a>Visningen Planlægning

Visningen Planlægning viser planlagte eller oprindelige overslag over oplysninger om tidsplan og omkostninger. Selvom der ikke er nogen funktioner til sporing af version og oprindelig plan for et projekt WBS, er værdierne i denne visning beregnet til at repræsentere den oprindelige version. Afsnittene Vurdering af tidsplan og Forkalkulation af kost i dette emne beskriver denne visning, og hvordan den bruges til at oprette en WBS.

### <a name="effort-tracking-view"></a>Visning af sporing af tidsforbrug

Visningen Sporing af tidsforbrug viser sporing af fremdriften for opgaver i WBS. Sammenligner de akkumulerede faktiske timer for en opgave med de planlagte indsatstimer. Følgende formler indeholder værdierne til visningen Sporing af tidsforbrug:

-   Status i procent = faktisk indsats til dato ÷ planlagt indsats for denne opgave
-   Resterende indsats (også kendt som forventet tid til fuldførelse \[[ETC\]) = planlagt indsats – faktisk indsats til dato
-   Vurder ved fuldførelse (EAC) = resterende indsats + faktisk arbejde til dato
-   Forventet indsatsvarians = planlagt indsats – EAC

Visningen Sporing af tidforbrug viser en projektion af indsatsvariansen for opgaven baseret på, om EAC er mere eller mindre end den planlagte indsats:

-   Hvis EAC er større end den planlagte indsats, er opgaven planlagt til at tage længere tid end oprindeligt planlagt og er bagud i forhold til tidsplanen.
-   Hvis EAC er mindre end den planlagte indsats, er opgaven planlagt til at tage kortere tid end oprindeligt planlagt og er forud i forhold til tidsplanen.

**Projektleders genprojektion af indsats** Projektlederen eller en anden person, der overvåger fremdriften af et projekt, må ind imellem revidere de oprindelige overslag for en opgave. Opgaven kan af forskellige årsager flytte, hurtigere eller langsommere end oprindeligt forventet. Området kan f.eks. være blevet reduceret, eller arbejdere har mindre erfaring end oprindeligt planlagt. Projektioner er en projektleders opfattelse af skøn, baseret på den aktuelle status for et projekt. Generelt bør du ikke ændre tallene på grundlinjen, da et projekts grundline repræsenterer et publiceret dokument for projektets tidsplan og forkalkulation, som alle interessenter i projektet har aftalt. 

Der er to måder, at projektledere kan ændre indsats på opgaver:

-   Ret den resterende indsats, der angives automatisk til at opdatere den faktiske resterende indsats i opgaven.
-   Ret den fremdriftsprocent, der automatisk er angivet til at opdatere den reelle fremdrift i opgaven.

Begge disse fremgangsmåder forårsager en genberegning af opgavens ETC, EAC og fremdriftsprocentdel, og den forventede indsatsafvigelse i opgaven. EAC, ETC og fremdriftsprocentdel for hovedopgaver genberegnes også, og deres forventede indsatsafvigelse opdateres. 

**Ændret indsats på hovedopgaver** Du kan ændre indsatsen for hoved- eller containeropgaver. Uanset om du ændrer disse værdier ved hjælp af den resterende indsats eller fremdriftsprocentdel for hovedopgaverne, udføres beregningerne automatisk i følgende rækkefølge:

1.  EAC, ETC, og fremdriftsprocentdel for opgaven beregnes.
2.  Den nye EAC fordeles til de underordnede opgaver i samme forhold som det oprindelige EAC-beløb.
3.  Den nye EAC på hver bladnodeopgave beregnes.
4.  Den resterende indsats og fremdriftsprocentdel genberegnes for alle de berørte underordnede opgaver, baseret på den nye EAC værdi. Indsatsafvigelsen for opgaverne genberegnes også.
5.  EAC på hovedopgaverne genberegnes også fra bladnoderne.

Klik på **Udvid til niveau** i visningen Sporing af tidsforbrug for at angive niveauet, hvor WBS skal spores og vedligeholdes. WBS udvides automatisk til det pågældende niveau i visningen Sporing af tidsforbrug, hver gang du åbner den.

### <a name="cost-tracking-view"></a>Viser sporing af omkostning

Visningen Sporing af omkostninger viser sporing af omkostningsforbrug for en opgave. I denne visning sammenlignes de faktiske omkostninger, der har været brugt på en opgave til dato, med de planlagte omkostninger for opgaven. Følgende formler indeholder værdierne til visningen Sporing af omkostninger:

-   Procentdel af forbrugte omkostninger = faktiske omkostninger til dato ÷ planlagte omkostninger for opgaven
-   Færdiggørelsesomkostninger (CTC) = Planlagte omkostninger – faktiske omkostninger til dato
-   Vurder ved fuldførelse (EAC) = CTC + faktiske omkostninger til dato
-   Forventet omkostningsafvigelse = planlagte omkostninger – EAC

Visningen Sporing af omkostninger viser en projektion af omkostningsvariansen for opgaven baseret på, om EAC er mere eller mindre end den planlagte omkostning:

-   Hvis EAC er større end den planlagte omkostning, er opgaven planlagt til at bruge flere penge end oprindeligt planlagt og ligger over budget.
-   Hvis EAC er mindre end den planlagte omkostning, er opgaven planlagt til at bruge færre penge end oprindeligt planlagt og ligger under budget.

**Projektleders genprojektion af omkostninger** Projektledere skal bruge CTC til at revidere den oprindelige forkalkulation for en opgave. Projektlederen kan ændre CTC-værdien til de omkostninger, der kræves for at fuldføre opgaven. Hvis du ændrer CTC-værdien, genberegnes opgavens CTC, EAC og procentdel af omkostninger, der er forbrugt, samt den forventede omkostningsafvigelse for en opgave. EAC, ETC og procentdel af forbrugte omkostninger for hovedopgaver genberegnes også, og deres forventede omkostningsafvigelse opdateres. 

> [!NOTE] 
> Når du reviderer indsats for en WBS-opgave i visningen Sporing af tidsforbrug, genberegnes opgavens CTC, EAC, procentdel af omkostning, der er forbrugt, og forventede omkostningsafvigelse alle i visningen Omkostningssporing. Dog påvirker omkostningsomkostninger ikke værdierne i visningen Sporing af tidsforbrug, fordi omkostning efter transaktionstype (arbejde, materiale eller udgift) eller projektkategori ikke revideres. 

**Projektionsrevision for omkostninger i hovedopgaver** Du kan revidere omkostninger for hovedopgaver, hvorefter beregningerne udføres automatisk i følgende rækkefølge:

1.  EAC og CTC og procentdel af omkostning, der er forbrugt på opgaven, genberegnes.
2.  Den nye EAC fordeles til de underordnede opgaver i samme forhold som det oprindelige EAC på opgaverne.
3.  Den nye EAC beregnes for hver opgave.
4.  CTS og procentdelen af omkostninger, der er forbrugt, genberegnes for de berørte underordnede opgaver baseret på EAC-værdien. Omkostningsafvigelsen for opgaverne genberegnes også.
5.  EAC for alle hovedopgaver genberegnes på grundlag af denne ændring.

Klik på **Udvid til niveau** i visningen Sporing af omkostninger for at angive niveauet, hvor WBS skal spores og vedligeholdes. WBS udvides automatisk til det pågældende niveau i visningen Sporing af omkostning, hver gang du åbner den.

### <a name="earned-value-management"></a>Administration af optjent værdi

Du kan bruge metoden for oparbejdet værdi (EVM) til at spore status for et projekt. Du kan få vist værdier for optjent værdi for projektlederens rollebaserede område. Diagramkomponenten for optjent værdi viser de tidsfaseinddelte værdier for planlagt værdi og faktiske omkostninger. Oparbejdet værdi pr. dags dato er vist som et punkt. Tidsfaseinddelte data for optjent værdi er ikke tilgængelig i øjeblikket. 

Tidsfasen i diagrammet over optjent værdi vises pr. uge eller pr. måned. I dette afsnit beskrives de tre grundpiller i EVM: planlagt værdi, optjent værdi og faktiske omkostninger. 

**Planlagt værdi** EVM-teorien siger, at grafikken over planlagt værdi repræsenterer den hastighed, hvormed projektgruppe har planlagt at optjene værdi af projektet. 

Finance and Operations bruger 0:100-indtægtsreglen, når der laves grafik over planlagt værdi. Ifølge denne regel bogføres værdien af opgaven til opgaven pr. slutdatoen. Ingen værdi bogføres, før opgaven er 100 procent fuldført. 

I Projektstyring og regnskab kan du angive slutdatoen for bladnoder og de planlagte omkostninger for dem. Når grafen for planlagt værdi vises efter uge, opsummeres planlagt værdi pr. uge for alle bladenodeopgaver i projektets varighed. 

**Optjent værdi** EVM-teorien siger, at grafikken over optjent værdi repræsenterer den hastighed, hvormed projektgruppen reelt optjener værdi i projektet. 

Finance and Operations bruger 0:100-indtægtsreglen, når der laves grafik over optjent værdi. Ifølge denne regel bogføres værdien af opgaven til opgaven pr. slutdatoen. Ingen værdi bogføres, før opgaven er 100 procent fuldført. 

Ved beregning af optjent værdi tages der højde for fremdriftsprocentdelen for hver opgave. Ifølge 0:100-indtægtsreglen tages der kun højde for opgaver, der er fuldført inden for en given periode, ved beregning af optjent værdi pr. afslutningen af den pågældende periode. Oparbejdet værdi for projektet beregnes for alle opgaver, der er fuldført, når diagrammet er oprettet. 

> [!NOTE] 
> Systemet til sporing af WBS har i øjeblikket ikke datastrukturer til at gemme historiske fremdriftsprocenter for hver opgave. Derfor kan der kun rapporteres optjent værdi pr. det tidspunkt, hvor kuben behandles. Kuben bør behandles regelmæssigt for at opdatere data for den optjente værdi, der er vist i det rollebaserede område. 

**Faktiske omkostninger** EVM-teorien angiver, at grafikken over de faktiske omkostninger repræsenterer den hastighed, hvormed der bruges penge på projektet. 

Transaktioner, der er bogført til et projekt, bruges til at afbilde den faktiske omkostningslinje. Omkostningerne er opsummeret efter dato. Disse data bruges derefter til at afbilde de faktiske omkostninger pr. uge eller pr. måned i diagrammet for optjent værdi.

### <a name="how-to-use-the-concepts-of-planned-value-earned-value-and-actual-cost"></a>Sådan bruges begreberne for planlagt værdi optjent værdi og faktiske omkostninger

**Tidsplanafvigelse** Under planlægning opretter du en prognose for arbejde på en tidslinje. Derfor er den planlagte værdi den hastighed, hvormed projektplanlæggere forventede, at arbejde ville være udført på projektet. Når et projekt er i gang, arbejdet er færdigt, og projektet indtjener værdi. Ved at sammenligne planlagte værdi med indtjent værdi, kan du se, hvordan arbejdet på et projekt skrider frem. Resultatet af sammenligningen kaldes afvigelse fra tidsplan. 

Hvis den planlagte værdi for en periode er større end den optjente værdi, er den mængde arbejde, der er udført på et projekt, mindre end hvad der var planlagt. Derfor er projektet bagud i forhold til tidsplanen. Da planlagt og optjent værdi er udtrykt som en pengemæssig værdi, angives forsinkelsen i projektet også som en pengemæssig værdi. 

Hvis den planlagte værdi for en periode er mindre end den optjente værdi, er den mængde arbejde, der er udført på et projekt, større end hvad der var planlagt. Derfor er projektet forud i forhold til tidsplanen. Denne gennemløbstid har også en pengemæssig værdi.

**Omkostningsafvigelse** Da optjent værdi bruger kostprisen som multiplikator, angiver optjent værdi omkostningen ved det arbejde, der er udført på et projekt. Efterhånden som et projekt skrider frem, indeholder transaktionslogfilen en registrering af penge, der faktisk er brugt på projektet. Ved at sammenligne optjent værdi med faktiske omkostninger, kan du få vist det pengebeløb, der er brugt kontra den værdi, der er optjent. Resultatet af sammenligningen kaldes omkostningsafvigelse. 

Hvis de faktiske omkostninger, der er brugt i en periode, er større end den optjente værdi, er der brugt flere penge, end der er optjent. Derfor overskrider projektet budgettet. 

Hvis de faktiske omkostninger, der er brugt i en periode, er mindre end den optjente værdi, er der optjent flere penge, end der er brugt. Derfor ligger projektet under budgettet.

## <a name="wbs-templates"></a>WBS-skabeloner
Du kan bruge funktionen WBS-skabeloner til at oprette standard skabeloner for projekter. Hvis de projekter, som firmaet tilbyder, involverer en masse gentaget arbejde, bør du overveje at oprette en WBS-skabelon. 

Du kan oprette en WBS-skabelon fra WBS til et eksisterende projekt, så viden og bedste praksis, som du har indsamlet under planlægning af det pågældende projekt, kan genbruges på lignende projekter i fremtiden. Men nogle gange giver det måske ikke mening at gemme hele WBS som en skabelon. Derfor kan du også oprette skabeloner fra dele af WBS for et projekt.

### <a name="saving-a-projects-wbs-as-a-template"></a>Gemme et projekts WBS som en skabelon

Når du opretter en skabelon, kan du importere det til et nyt projekts WBS under rodnoden eller under en vilkårlig opgave i projektets WBS.

### <a name="importing-a-wbs-template-into-a-projects-wbs"></a>Importere en WBS-skabelon til et projekts WBS

Når du importerer opgaver, organiseres opgaverne i skabelonen baseret på startdatoen for den opgave, de importeres under. Under import bruges forgængerrelationer i skabelonopgaverne til at beregne startdatoen for de importerede opgaver. Destinationprojektets standardarbejdskalender bruges til at beregne slutdatoerne for de importerede opgaver, så arbejdsdage og standardarbejdstimer, der er defineret i det aktuelle projekt arbejdskalender, bliver bevaret. 

Omkostningsbeløb og salgspriser på estimatlinjer anvendes for at sikre, at priser, der er specifikke for projektet eller projektkontrakten, har gyldige datoer.

### <a name="differences-between-a-projects-wbs-and-a-wbs-template"></a>Forskelle mellem et projekts WBS og en WBS-skabelon

-   Opgaverne i WBS-skabeloner har ikke startdatoer og slutdatoer.

Arbejds- og ikke-arbejdsdage er ikke angivet for WBS-skabeloner.

-   WBS-skabeloner bruger altid den planlægningskalender, der er defineret som standardkalender for alle projekter.

Standardplanlægningskalenderen bruges kun til at finde timer i en standardarbejdsdag.

-   Relationer mellem foregående opgaver kopieres ikke til en WBS-skabelon.

Da WBS-skabeloner ikke har datoer, er den startdatologik, der er baseret på den foregående opgaves slutdato, ikke nødvendig.

-   Der oprettes automatisk en estimatlinje for arbejdsomkostninger, når der oprettes en opgave i en WBS-skabelon. Salgspris og kostbeløbet kopieres fra den valgte arbejder.

Udgifts- og vareomkostninger kan oprettes manuelt på samme måde som i et projekts WBS.

-   Planlægningsfejl vises, når der er afvigelser fra følgende formel:

Indsats = antal ressourcer × varighed × antal timer på en almindelig arbejdsdag 

Du kan rette alle fejl i planlægningen på samme tid ved at klikke på **Ret alle tidsplanfejl**. 

Du kan også rette planlægningsfejl enkeltvis ved at klikke på advarselsikonet for hver opgave.



