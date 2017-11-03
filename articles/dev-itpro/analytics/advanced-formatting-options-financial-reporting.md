---
title: "Avancerede formateringsindstillinger i økonomirapportering"
description: "Når du opretter en rapport til økonomirapportering, er flere formateringsfunktioner tilgængelige, herunder filtre for dimensioner, begrænsninger for kolonner og rapporteringsenheder, rækker, der ikke udskrives, og IF/ELSE-sætninger i beregninger."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.custom: 106571
ms.assetid: 895b5127-01d6-4495-b127-343387b743aa
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4064a44601712a860d2a70a84ed415fda4669db3
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="advanced-formatting-options-in-financial-reporting"></a>Avancerede formateringsindstillinger i økonomirapportering

[!include[banner](../includes/banner.md)]


Når du opretter en rapport til økonomirapportering, er flere formateringsfunktioner tilgængelige, herunder filtre for dimensioner, begrænsninger for kolonner og rapporteringsenheder, rækker, der ikke udskrives, og IF/ELSE-sætninger i beregninger. 

I følgende tabel beskrives de avancerede formateringsfunktioner, der er tilgængelige, når du opretter rapporter.

| Funktion                   | Beskrivelse          |
|----------------------------|-------------------------------|
| Dimensionsfilter           | For at få adgang til bestemte datasæt, kan du bruge dimensioner i række- og kolonnedefinitionen. Mange rapporter bruger kun det naturlige segment i rækkeformatet. Rækker kan dog ændres, så de inkluderer dimensionsværdier. Dimensionsfiltre i kolonnedefinitionen bruges til at få adgang til bestemte dimensionsværdier. |
| Begrænsning for rapporteringsenhed | Du kan oprette en række i en rapport, så den kun viser oplysninger, der er knyttet til en bestemt rapporteringsenhed.     |
| Rækker, der ikke udskrives (NP)     | Rækker, der ikke udskrives, er nyttige i mange rapporter. Hvis flere beregninger er nødvendige for at opnå en værdi, kan disse beregninger være skjult på den udskrevne rapport. Rækker, der ikke udskrives, også nyttige til fejlfinding af rapportdesign og til avanceret celleplacering.                                                    |
| Kolonnebegrænsning         | Kolonnebegrænsning i rækkedefinitionen kan bruges til at skjule værdier, der kun er relevante på nogle rækker i rapporten. Når der udføres beregninger af procentdele på en række, forhindrer kolonnebegrænsningen, at total-kolonner eller andre kolonner bliver udskrevet, når disse tal ikke gælder.                              |
| Kolonneskift               | Du kan tilføje kolonneskift i en rækkedefinition for at vise rapportoplysninger ved siden af hinanden. Du kan tilføje flere kolonneskift i en enkelt rækkedefinition, og kolonneoverskrifter gentages øverst i hver kolonne efter kolonneskiftet. Bemærkninger til en rapport vises mellem kolonneskiftene.                              |
| IF/THEN/ELSE-sætning     | Du kan ændre beregninger i en rækkedefinition eller en kolonnedefinition.  |

## <a name="advanced-cell-placement"></a>Avanceret celleplacering
Avanceret celleplacering eller *tvang* omfatter placering af bestemte værdier i bestemte celler. Tvang anvendes for eksempel ofte til at flytte den korrekte saldo i en likviditetsopgørelse. Du kan bruge tvang til følgende formål:

-   Flytte værdier fra Microsoft Excel til bestemte celler.
-   Placere specifikke værdier permanent i en rapport.
-   Ændre tegn ved at kopiere en værdi fra en tidligere celle og gange værdien med -1.

**Bemærk:** I mange tilfælde skal du konfigurere din rapportdefinition, så kolonneberegninger foretages før rækkeberegninger. Benyt denne fremgangsmåde for at fuldføre denne konfiguration.

1.  Åbn rapportdefinitionen i Report Designer.
2.  På fanen **Indstillinger** under **Beregningsprioritet** skal du vælge **Udfør kolonneberegning først og derefter rækkeberegning**.

## <a name="designing-the-report"></a>Designe rapporten
Når du designer en rapport, skal du oprette alle detaljerækkerne først for at sikre, at værdierne hentes ind som forventet. Tilføj derefter formattilsidesættelsen **NP** (ingen udskrift) for at undertrykke de detaljer, der omfatter de endelige værdier. **Vigtigt:** når du bruger formateringskoden **CAL** i rækkedefinitionen, kan du ikke udlede transaktionsdetaljer. I forbindelse med tvang bruge følgende format til formler: &lt;destinationskolonne&gt;=&lt;den oprindelige kolonne&gt;.&lt;rækkekode&gt; Adskil eventuelle yderligere placeringer for en række med et komma og et mellemrum. Her er et eksempel: D=C.190,E=C.100

## <a name="examples-of-advanced-formatting-options"></a>Eksempler på avancerede formateringsindstillinger
Følgende eksempler viser, hvordan du formaterer rækkedefinitionen og kolonnedefinitionen for at gennemtvinge en grundlæggende pengestrømsrapport (eksempel 1) og en statistisk rapport (eksempel 2).

### <a name="example-1-basic-forcing"></a>Eksempel 1: Grundlæggende tvang

Følgende tabel viser et eksempel på en rækkedefinition, der bruger grundlæggende tvang.

| Rækkekode | Betegnelse                      | Formatkode | Relaterede formler/rækker/enheder | Rækkemodifikator | Link til økonomiske dimensioner |
|----------|----------------------------------|-------------|-----------------------------|----------------|----|
| 100      | Likvide midler i starten af perioden (NP) |             |                             | Kontomodifikator = \[/BB\] | +Segment2 = \[1100\]         |
| 130      | Likvid beholdning - periodens start      | CAL         | C=C.100,F=D.100             |               |     |   |
| 160      |                                  |             |                             |              |     |   |
| 190      |                                  |             |                             |                 |     |   |

> [!NOTE] 
> Tomme kolonner blev fjernet fra den forrige tabel af hensyn til præsentationen: Kolonnerne Tilsidesæt format, Normal saldo, Udskriftsstyring og Kolonnebegrænsning vises ikke.

Følgende tabel viser et eksempel på en kolonnedefinition, der bruger grundlæggende tvang i rækken.

|                              | A   | B    | K        | D      | E      | F    |
|------------------------------|-----|------|----------|--------|--------|------|
| Overskrift 1                     |     |      |          |        |        |      |
| Overskrift 2                     | A   | B    | K        | D      | E      | F    |
| Overskrift 3                     |     |      |          |        |        |      |
| Kolonnetype                  | ROW | DESC | FD       | FD     | FD     | CALC |
| Bogkode/attributkategori |     |      | ACTUAL   | ACTUAL | ACTUAL |      |
| Regnskabsår                  |     |      | BASE     | BASE   | BASE   |      |
| Periode                       |     |      | BASE     | BASE   | BASE   |      |
| Perioder, der er omfattet              |     |      | PERIODIC | YTD/BB | YTD    |      |
| Formel                      |     |      |          |        |        | E-D  |
| Kolonnebredde                 | 5   | 30   | 14       | 14     | 14     | 14   |

### <a name="example-2-statistical-reports"></a>Eksempel 2: Statistiske rapporter

Følgende tabel viser et eksempel på en rækkedefinition, der bruger tvang til en statistisk rapport.

| Rækkekode | Beskrivelse               | formateringskode | Relaterede formler/rækker/enheder     | Tilsidesæt format      | Normal saldo | Link til økonomiske dimensioner               |
|----------|---------------------------|-------------|---------------------------------|----------------------|----------------|--------------------|
| 50       | Statistiske oplysninger   | REM         |                                 |                      |                |            
| 100      | Antal beskæftigede - USA            | CAL         | 4                               | \#\#\#0.;($\#\#\#0.) |                |                  
| 115      | Antal beskæftigede - International | CAL         | 11                              | \#\#\#0.;($\#\#\#0.) |                |          
| 130      |                           |             |                                 |                      |                |               
| 190      | Salg USA                  |             |                                 |                      | K              |                             +Segment2 = \[41\*\], Segment3 = \[00\]    |
| 220      | Salg international       |             |                                 |                      | K              |                              +Segment2 = \[41\*\], Segment3 = \[01:99\] |
| 250      |                           |             |                                 |                      |                |               |  
| 280      |                           |             |                                 |                      |                |                         |
| 310      | Salg USA                  | CAL         | D=C.190,E=C.100,F=(C.100/C.190) |                      |                |              
| 340      | Salg international       | CAL         | D=C.220,E=C115,F=(C.220/C.115)  |                      |                |               |

> [!NOTE] 
> Tomme kolonner blev fjernet fra den forrige tabel af hensyn til præsentationen: Kolonnerne Udskriftsstyring, Kolonnebegrænsning og Rækkemodifikator vises ikke.

Følgende tabel viser et eksempel på en kolonnedefinition, der bruger tvang til en statistisk rapport.

|                              | A   | B    | K      | D            | E     | F            |
|------------------------------|-----|------|--------|--------------|-------|--------------|
| Overskrift 1                     | A   | B    | K      | D            | E     | F            |
| Overskrift 2                     | -   | -    | ÅTD    | Årligt salg | Personale | $ pr. Person |
| Overskrift 3                     |     |      |        |              |       |              |
| Kolonnetype                  | ROW | DESC | FD     | CALC         | CALC  | CALC         |
| Bogkode/attributkategori |     |      | ACTUAL |              |       |              |
| Regnskabsår                  |     |      | BASE   |              |       |              |
| Periode                       |     |      | BASE   |              |       |              |
| Perioder, der er omfattet              |     |      | YTD    |              |       |              |
| Formel                      |     |      |        |              |       | E-D          |
| Kolonnebredde                 | 5   | 30   | 14     | 14           | 14    | 14           |

## <a name="restricting-a-row-to-a-specific-reporting-unit"></a>Begrænsning af en række til en bestemt rapporteringsenhed
Når en række i rapporten er begrænset til en bestemt rapporteringsenhed, viser den pågældende række kun de sammenkædede data for den angivne rapporteringsenhed og ignorerer data for andre rapporteringsenheder i rapporteringstræet. Du kan for eksempel oprette en række, der indeholder oplysninger om de samlede driftsudgifter for en bestemt afdeling. Rapporten kan indeholde dublerede data, hvis rapporten indeholder både et rapporteringstræ og en rækkedefinition, der har mere end blot den fysiske konto. Du kan for eksempel have et rapporteringstræ, der viser de seks afdelinger i organisationen, og du har også en rækkedefinition, der viser en bestemt kombination af en konto og en afdeling i rækken. Når du genererer rapporten, udskrives den specifikke kombination af en konto og en afdeling på alle niveauer i rapporteringstræet, selvom den pågældende afdeling ikke kan svarer til det, der er i træet. Dette problem opstår, fordi rækken tilsidesætter det, der normalt filtreres fra af rapportdefinitionen. Du kan undgå dubletter af data ved at begrænse en række til en bestemt rapporteringsenhed. **Bemærk:** Hvis en række indeholder dimensioner, og du begrænser rækken til en underordnet rapporteringsenhed, medtages rækkebeløbet for den pågældende underordnede enhed og dens overordnede enheder, men der forekommer ikke dubletter af data.

### <a name="restrict-a-row-to-a-reporting-unit"></a>Begrænse en række til en rapporteringsenhed

1.  Klik på **Rækkedefinitioner** i Report Designer, og vælg derefter den rækkedefinition, der skal ændres.
2.  Dobbeltklik på den relevante celle af typen **Relaterede formler/rækker/enheder**.
3.  Vælg det trædiagram, der er tildelt i rapportdefinitionen, i feltet **Trædiagram** i dialogboksen **Valg af enhed i trædiagram**.
4.  Vælg en rapporteringsenhed, og klik derefter på **OK**. Begrænsningen vises i cellen i rækkedefinitionen.
5.  Dobbeltklik på cellen i kolonnen **Link til økonomiske dimensioner** i den begrænsede række, og angiv derefter et hyperlink til systemet med økonomiske data.

## <a name="selecting-print-control-in-a-row-definition"></a>Vælge udskriftsstyring i en rækkedefinition
Du kan angive udskriftskontrolkoder for hver kolonne ved hjælp af cellen **Udskriftsstyring**.

### <a name="add-print-control-codes-to-a-report-row"></a>Tilføje udskriftskontrolkoder i en rapportrække

1.  Åbn den rækkedefinition, der skal ændres, i Report Designer.
2.  Dobbeltklik på cellen **Udskriftsstyring**.
3.  I dialogboksen **Udskriftsstyring** skal du vælge en udskriftskontrolkode eller trykke på og holde Ctrl-tasten nede for at vælge flere koder. Du kan også indtaste udskriftskontrolkoder direkte i cellen **Udskriftsstyring**. Flere udskriftskontrolkoder skal adskilles med kommaer.
4.  Vælg betingede udskriftsindstillinger.
5.  Klik på **OK**.

### <a name="regular-print-control-codes"></a>Almindelige koder til udskriftsstyring

I følgende tabel beskrives almindelige udskriftskontrolkoder til en rækkedefinition.

| Kode til udskriftstyring | Fortolkning af udskriftskontrolkoden         | Beskrivelse                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NP                 | Rækker, der ikke udskrives                                 | Forhindrer, at beløbene i rækken udskrives på rapporten, og sørger for, at beløbene ikke medtages i beregninger. Hvis du vil medtage en kolonne, der ikke udskrives, i en beregning, skal du henvise direkte til kolonnen i formlen til beregning. Rækken 240, som ikke udskrives, medtages for eksempel i følgende beregning: **230 + 240 + 250**. Rækken 240, som ikke udskrives, medtages dog ikke i følgende beregning: **230:250**. |
| CS                 | Valutasymbolet; anvend valutaformatet i denne række | Medtag valutasymbolet i alle beløb, som ikke angiver procenter. Procentværdier får aldrig et valutasymbol.                                                                                                                                                                                                                                                                                                |
| XD                 | Undertryk række i kontodetaljerapport            | Undertryk visningen af konti på kontodetaljerapporter og transaktionsdetaljerapporter. Denne udskriftsstyring er nyttig, hvis en række indeholder flere konti, der ikke skal vises på kontodetaljerapporten eller transaktionsdetaljerapporten.                                                                                                                                                           |
| X0                 | Undertryk række, hvis alle indeholder nulværdi                        | Medtag ikke en række i rapporten, hvis alle celler i den pågældende række enten er tomme eller indeholder nulværdiler. Denne udskriftsstyring er kun relevant, når muligheden for at undertrykke nul-saldo ikke er markeret i rapportdefinitionen.                                                                                                                                                                                            |
| B0                 | Lad nul-kolonner være tomme                         | Lad kolonner være tomme i en række, som indeholder beløb med værdien nul.                                                                                                                                                                                                                                                                                                                                                      |
| XR                 | Undertryk akkumulering                                  | Undertryk en akkumulering. Hvis rapporten bruger et rapporteringstræ, akkumuleres beløbene i denne række ikke til efterfølgende overordnede noder.                                                                                                                                                                                                                                                                               |
| SR                 | Undertryk afrunding                                | Undgå, at beløbene i denne række bliver afrundet.                                                                                                                                                                                                                                                                                                                                                          |
| XT                 | Undertryk række i transaktionsdetaljerapport        | Undertryk visning af transaktioner på transaktionsdetaljerapporter. Denne udskriftsstyring er nyttig, hvis en række indeholder flere konti, der ikke skal vises på en transaktionsdetaljerapport.                                                                                                                                                                                                             |

### <a name="conditional-print-control-codes"></a>Betingede koder til udskriftsstyring

I følgende tabel beskrives de betingede udskriftskontrolkoder til en rækkedefinition.

| Kode til udskriftstyring | Beskrivelse                                  |
|--------------------|----------------------------------------------|
| (ingen)             | Fjern valget af betinget udskrivning.       |
| DR                 | Udskriv kun debetsaldi for denne række.  |
| CR                 | Udskriv kun kreditsaldi for denne række. |

## <a name="column-restriction-cell-in-a-row-definition"></a>Celle til kolonnebegrænsning i en rækkedefinition
Den celle til **kolonnebegrænsning** i en rækkedefinition har flere formål. Afhængigt af rækketypen kan du bruge cellen til **kolonnebegrænsning** til at angive en af følgende funktioner:

-   Cellen kan begrænse udskrivning af rækkebeløb til en bestemt kolonne. Denne funktion er nyttig, hvis du vil oprette en balance i tabelformat.
-   Cellen kan angive kolonnen med beløb, der skal sorteres.

## <a name="using-a-calculation-formula-in-a-row-definition"></a>Bruge en beregningsformel i en rækkedefinition
En beregningsformel i en rækkedefinition kan omfatte operatorerne **+**, **-**, **\*** og **/** og også **IF/THEN/ELSE**-sætninger. Desuden kan en beregning omfatte individuelle celler og absolutte beløb (faktiske tal, der indgår i formlen). Formlen kan indeholde op til 1.024 tegn. Beregninger kan ikke anvendes til rækker, der indeholder celler af typen **Link til økonomiske dimensioner** (FD). Du kan dog medtage beregninger på fortløbende rækker, undertrykke udskrivning af disse rækker og derefter lægge beregningsrækkerne sammen.

### <a name="operators-in-a-calculation-formula"></a>Operatorer i en formel til beregning

En formel til beregning bruger mere komplekse operatorer end en formel til sammenlægning af beløb i rækker. Du kan dog bruge operatorerne **\*** og **/** sammen med de ekstra operatorer, hvis du vil gange (\*) og dividere (/) beløb. Hvis du vil bruge et interval eller en sum i en formel til beregning, skal du bruge @-tegnet foran en rækkekode, medmindre du bruger en kolonne i rækkedefinitionen. Hvis du for eksempel vil lægge beløbet i række 100 sammen med beløbet i række 330, kan du bruge rækketotalformlen **100+330** eller beregningsformlen **@100+@330**. **Bemærk:** du skal @-tegnet før hver rækkekode, der bruges i en beregningsformel. I modsat fald læses tallet som et absolut beløb. Formlen **@100+330** føjer f.eks. 330 kr. til beløbet i række 100. Når du henviser til en kolonne i en beregningsformel, er tegnet (@) ikke påkrævet.

### <a name="create-a-calculation-formula"></a>Oprette en beregningsformel

1.  Klik på **Rækkedefinitioner** i Report Designer, og åbn derefter den rækkedefinition, der skal ændres.
2.  Dobbeltklik på cellen **formateringskode**, og vælg derefter **CAL**.
3.  Angiv beregningsformlen i cellen **Relaterede formler/rækker/enheder**.

### <a name="example-of-a-calculation-formula-for-specific-rows"></a>Eksempel på en beregningsformel for bestemte rækker

I dette eksempel betyder beregningsformlen **@100+@330**, at beløbet i række 100 lægges til beløbet i række 330. Rækketotalformlen **340 + 370** føjer beløbet i række 340 til beløbet i række 370. (Beløbet i række 370 er beløbet fra beregningsformlen).

| Rækkekode | Beskrivelse                 | formateringskode | Relaterede formler/rækker/enhed | Udskriftsstyring | Rækkemodifikator | Link til økonomiske dimensioner |
|----------|-----------------------------|-------------|----------------------------|---------------|--------------|------------------------------|
| 340      | Likvide midler i starten af perioden |             |                            | NP            | BB           | +Konto = \[1100:1110\]       |
| 370      | Likvide midler i starten af året   | CAL         | @100+@330                  | NP            |              |                              |
| 400      | Likvide midler i starten af perioden | TOT         | 340+370                    |               |              |                              |

Når rækken i en rækkedefinition har formateringskoden **CAL**, og du indtaster en matematisk beregning i cellen **Relaterede formler/rækker/enheder**, skal du også angive bogstavet for den tilknyttede kolonne og række i rapporten. Angiv f.eks. **A.120** for at repræsentere kolonne A, række 120. Du kan også bruge et (@) tegn til at angive alle kolonnerne. Angiv f.eks. **@120** for at repræsentere alle kolonner i række 120. En matematisk beregning, der ikke har et kolonnebogstav eller et (@) tegn antages at være et reelt tal. **Bemærk:** hvid du bruger en etiketrækkekode til at henvise til en række, skal du bruge et punktum (.) som separator mellem kolonnebogstavet og etiketten (for eksempel **A.GROSS\_MARGIN/A.SALES**). Hvis du bruger et @-tegn, er en separator ikke påkrævet (for eksempel **@GROSS\_MARGIN/@SALES**).

### <a name="example-of-a-calculation-formula-for-a-specific-column"></a>Eksempel på en beregningsformel for en bestemt kolonne

I dette eksempel angiver beregningsformlen **E=C.340**, at beregningen i cellen i kolonne C, række 340, kun udføres på kolonne E. **Bemærk:** når du refererer til en kolonne i en beregningsformel, er et @-tegn ikke påkrævet.

| Rækkekode | Beskrivelse                 | formateringskode | Relaterede formler/rækker/enhed | Udskriftsstyring | Rækkemodifikator | Link til økonomiske dimensioner |
|----------|-----------------------------|-------------|----------------------------|---------------|--------------|------------------------------|
| 340      | Likvide midler i starten af perioden |             |                            | NP            | BB           | +Konto = \[1100:1110\]       |
| 370      | Likvide midler i starten af året   | CAL         | E=C.340                    | NP            |              |                              |
| 400      | Likvide midler i starten af perioden | TOT         | 340+370                    |               |              |                              |

### <a name="modifying-a-number-in-selected-columns"></a>Ændring af et tal i markerede kolonner

Når du ændrer et tal eller en beregning i en kolonne i en bestemt række men ikke vil påvirke andre kolonner i rapporten, kan du angive **CAL** (beregning) i kolonnen **Formateringskode** i rækkedefinitionen.

-   Hvis du vil udføre en beregning på alle rapportkolonner (**FD**), skal du ikke angive en kolonnetildeling.
-   Hvis du vil begrænse en formel til bestemte kolonner, skal du indtaste kolonnebogstavet, et lighedstegn (**=**) og derefter formlen.
-   Du kan angive flere kolonner. Når du bruger et @-tegn med en bestemt kolonneplacering, er @-tegnet relateret til rækken.
-   Du kan angive flere kolonneformler i én række. Adskil formlerne med kommaer.

### <a name="calculation-examples"></a>Eksempler på beregninger

| Kalkulation            | Handling, der oprettes                                                                                                   |
|------------------------|--------------------------------------------------------------------------------------------------------------------------|
| @130\*.75              | For hver kolonne ganges værdien i rækken 130 med 0,75. Resultatet anbringes derefter i den aktuelle række for hver kolonne. |
| B=@130\*.75            | Samme beregning udføres kun på kolonne B.                                                                      |
| A,B,C=(@100/@130)\*.75 | A=(A.100/A.130)\*.75 B=(B.100/B.130)\*.75 C=(C.100/C.130)\*.75                                                           |

### <a name="ifthenelse-statements-in-a-row-definition"></a>IF/THEN/ELSE-sætninger i en rækkedefinition

**IF/THEN/ELSE**-sætninger kan føjes til en hvilken som helst gyldig beregning og bruges sammen med formatet **CAL**. Du indtaster **IF/THEN/ELSE**-beregningsformler i cellen i kolonnen **Relaterede formler/rækker/enheder**. **IF/THEN/ELSE**-beregningsformler bruger følgende format: IF &lt;sand/falsk-sætning&gt; THEN &lt;formel&gt; ELSE &lt;formel&gt; Delen **ELSE &lt;formel&gt;** af sætningen er valgfri.

#### <a name="if-statements"></a>IF-sætninger

Den sætning, der følger efter **IF**-sætningen, kan være enhver sætning, der kan evalueres som sand eller falsk. Den sætning, der følger efter **IF**-sætningen, kan omfatte en enkel vurdering, eller det kan være en kompleks sætning, der kan indeholde flere udtryk. Her er nogle eksempler:

-   **IF A.200&gt;0** (enkel evaluering)
-   **IF A.200&gt;0 AND A.200&lt;10,000** (kompleks sætning)
-   **IF A.200&gt;10000 OR ((A.340/B.1200)\*2 &lt;1200)** (kompleks sætning, der indeholder flere udtryk)

Udtrykket **Perioder** i en **IF**-sætning angiver antallet af perioder for rapporten. Dette udtryk bruges typisk til at beregne et gennemsnit for år til dato. Når du for eksempel kører en rapport for perioden 7 år til dato, betyder sætningen **B.150/perioder**, at værdien i række 150 i kolonne B divideres med 7.

#### <a name="then-and-else-formulas"></a>THEN- og ELSE-formler

**THEN**- og **ELSE**-formler kan være en hvilken som helst gyldig beregning fra meget enkle værditildelinger til komplekse formler. Eksempelvis betyder sætningen **IF A.200&gt;0 THEN A=B.200** "hvis værdien i cellen i kolonne A i række 200 er større end 0 (nul), skal værdien i cellen i kolonne B i række 200 placeres i cellen i kolonne A i den aktuelle række." Den foregående **IF/THEN**-sætning anbringer en værdi i en kolonne i den aktuelle række. Du kan dog også bruge @-tegnet i sand/falsk-vurderinger eller formlen til at repræsentere alle kolonner. Her er nogle eksempler, der er beskrevet i følgende afsnit:

-   **IF A.200 &gt;0 THEN B.200**: Hvis værdien i celle A.200 er positiv, anbringes værdien fra celle B.200 i hver kolonne i den aktuelle række.
-   **IF A.200 &gt;0 THEN @200**: Hvis værdien i celle A.200 er positiv, anbringes værdien fra hver kolonne i række 200 i den tilsvarende kolonne i den aktuelle række.
-   **IF @200 &gt;0 THEN @200**: Hvis værdien i række 200 i den aktuelle kolonne er positiv, anbringes værdien fra række 200 i den samme kolonne i den aktuelle række.

### <a name="restricting-a-calculation-to-a-reporting-unit-in-a-row-definition"></a>Begrænse en beregning til en rapporteringsenhed i en rækkedefinition

For at begrænse en beregning til en enkelt rapporteringsenhed i et rapporteringstræ, så det beregnede beløb ikke akkumuleres til en enhed på et højere niveau, kan du bruge koden **@Unit** i cellen **Relaterede formler/rækker/enheder** i rækkedefinitionen. Koden **@Unit** er angivet i kolonne B i rapporteringstræet **Enhedsnavn**. Når du bruger koden **@Unit**, akkumuleres værdierne ikke, men beregningen evalueres på hvert niveau i rapporteringstræet. **Bemærk:** hvis du vil bruge denne funktion, skal der knyttes et rapporteringstræ til rækkedefinitionen. Beregningsrækken kan henvise til en beregningsrække eller en række med økonomiske data. Beregningen er registreret i cellen **Relaterede formler/rækker/enheder** i rækkedefinitionen og begrænsningen af typen økonomiske data. Beregningen skal bruge en betinget beregning, der starter med en **IF @Unit**-konstruktion. Her er et eksempel: IF @Unit(SALES) THEN @100 ELSE 0 Denne beregning medtager beløbet fra række 100 i hver kolonne i rapporten men kun for enheden SALG. Hvis flere enheder navngives SALG, vises beløbet i hver af disse enheder. Desuden kan række 100 være en række med økonomiske data række og kan defineres som en række, der ikke udskrives. I så fald forhindres beløbet i at blive vist i alle enheder i træet. Du kan også begrænse beløbet til en enkelt kolonne i rapporten, såsom kolonne H, ved hjælp af en kolonnebegrænsning, så værdien kun udskrives i den pågældende kolonne i rapporten. Du kan medtage **OR**-kombinationer i en **IF**-sætning. Her er et eksempel: IF @Unit(SALES) OR @Unit(SALESWEST) og THEN 5 ELSE @100 Du kan angive en enhed i en begrænsning af typen beregning på en af følgende måder:

-   Indtast et enhedsnavn for at medtage enheder, der matcher. For eksempel aktiverer **IF @Unit(SALES)** beregningen af enhver enhed med navnet SALG, selvom der er flere enheder med navnet SALG i rapporteringstræet.
-   Angiv navnet på virksomheden og enheden for at begrænse beregningen til bestemte enheder i en bestemt virksomhed. Indtast for eksempel **IF @Unit(ACME:SALES**) for at begrænse beregningen til enheder med navnet SALG i firmaet ACME.
-   Angiv den fulde hierarkikode fra rapporteringstræet for at begrænse beregningen til en bestemt enhed. Angiv for eksempel **IF @Unit(SUMMARY^ACME^WEST COAST^SALES)**. **Bemærk:** du kan finde den fulde hierarkikode ved at højreklikke på definitionen af rapporteringstræet og derefter vælge **Kopiér rapporteringsenhedsidentifikator (H-kode)**.

#### <a name="restrict-a-calculation-to-a-reporting-unit"></a>Begrænse en beregning til en enhed i trædiagram

1.  Klik på **Rækkedefinitioner** i Rapportdesigner, og åbn derefter en rækkedefinition, der skal ændres.
2.  Dobbeltklik på cellen **formateringskode**, og vælg derefter **CAL**.
3.  Klik på cellen **Relaterede formler/rækker/enheder**, og angiv derefter en betinget beregning, der starter med en **IF @Unit**-konstruktion.

### <a name="ifthenelse-statements-in-a-column-definition"></a>IF/THEN/ELSE-sætninger i en kolonnedefinition

En **IF/THEN/ELSE**-sætning gør det muligt for enhver beregning at afhænge af resultaterne fra en anden kolonne. Du kan henvise til andre kolonner, men du kan ikke referere til en celle i rapporten i **IF**-sætningen. En beregning skal gælde for hele kolonnen. For eksempel betyder sætningen **IF B&gt;100 THEN B ELSE C\*1,25** betyder "Hvis beløbet i kolonne B er større end 100, placeres værdien fra kolonne B i kolonnen **CALC**. Hvis beløbet i kolonne B ikke er større end 100, ganges værdien i kolonne C med 1,25, og resultatet placeres i kolonnen **CALC**. " **IF**-sætningen skal altid ledsages af en logisk sætning, der kan evalueres som sand eller falsk. De formler, du bruger til både **THEN**-sætningen og **ELSE**-sætningen kan indeholde henvisninger til et vilkårligt antal kolonner, og disse formler kan være lige så komplekse, du ønsker. **Bemærk:** du kan ikke placere resultaterne af en beregning i en anden kolonne. Resultaterne skal være i den kolonne, der indeholder formlen.




