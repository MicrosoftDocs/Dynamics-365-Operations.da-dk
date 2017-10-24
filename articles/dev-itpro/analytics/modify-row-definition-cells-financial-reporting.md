---
title: "Ændre rækkedefinitionsceller"
description: "Denne artikel beskriver de oplysninger, der kræves for hver celle i en rækkedefinition i en økonomirapport, og forklarer, hvordan du angiver disse oplysninger."
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
ms.search.scope: Management Reporter, UnifiedOperations, Core
ms.custom: 58881
ms.assetid: 0af492df-a84e-450c-8045-78ef1211abaf
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: eb09c0bb28c2ba8e7b890854c444cec80fe8277c
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="modify-row-definition-cells"></a>Ændre rækkedefinitionsceller

[!include[banner](../includes/banner.md)]


Denne artikel beskriver de oplysninger, der kræves for hver celle i en rækkedefinition i en økonomirapport, og forklarer, hvordan du angiver disse oplysninger. 

# <a name="specify-a-row-code-in-a-row-definition"></a>Angiv en rækkekode i en rækkedefinition

I rækkedefinitioner angiver tal eller etiketter i cellen **Rækkekode** hver linje i rækkedefinitionen. Du kan angive rækkekoden til at referere til data i beregninger og totaler.

### <a name="row-code-requirements"></a>Krav til rækkekoder

Der kræves en rækkekode for alle rækker. Du kan blande numeriske, alfanumeriske og ikke-angivne (tomme) rækkekoder i en rækkedefinition. Rækkekoden kan være et positivt heltal (under 100.000.000) eller en beskrivende etiket, der identificerer den pågældende række. En beskrivende etiket skal følge disse regler:

-   etiketten skal begynde med et bogstav (a til z eller A til Z) og kan være enhver kombination af tal og bogstaver op til 16 tegn. 
    > [!NOTE]
    > En etiket kan indeholde understregningstegn (\_), men ingen andre specialtegn er tilladt.
-   Etiketten kan ikke bruge nogen af følgende reserverede ord: AND, OR, IF, THEN, ELSE, PERIODS, TO, BASEROW, UNIT, NULL, CPO eller RPO.

Følgende eksempler er gyldige rækkekoder:

-   320
-   TL\_NET\_INCOME
-   TL\_NET\_94

### <a name="change-a-row-code-in-a-row-definition"></a>Redigere en rækkekode i en rækkedefinition

1.  Klik på **Rækkedefinitioner** i Report Designer, og åbn derefter den rækkedefinition, der skal ændres.
2.  I den relevante række skal du angive den nye værdi i cellen i kolonnen **Rækkekode**.

### <a name="reset-numeric-row-codes"></a>Nulstille numeriske rækkekoder

1.  Klik på **Rækkedefinitioner** i Report Designer, og åbn derefter den rækkedefinition, der skal ændres.
2.  I menuen **Rediger** skal du klikke på **Nummerer rækker igen**.
3.  I dialogboksen **Nummerer rækker igen** skal du angive nye værdier for den første rækkekode og rækkekodeforøgelsen. Du kan nulstille de numeriske rækkekoder til værdier med samme mellemrum. I rapportdesigneren nummereres dog kun rækkekoder, der begynder med tal (eksempelvis 130 eller 246). Rækkekoder, der begynder med bogstaver (for eksempel INCOME\_93 eller TP0693) nummereres ikke igen. 
> [!NOTE]
> Når du nummererer rækkekoder igen, opdaterer rapportdesigneren automatisk referencerne **TOT** og **CAL**. Hvis en **TOT**-række for eksempel refererer til et område, der starter med rækkekoden 100, og du nummererer rækker igen, startende med 90, ændres **TOT**-referencen fra 100 til 90.

## <a name="add-a-description"></a>Tilføje en beskrivelse
Beskrivelsescellen indeholder en beskrivelse af de økonomiske oplysninger i rækken i rapporten, f.eks. "Omsætning" eller "Nettoindkomst". Teksten i cellen **Beskrivelse** vises i rapporten, nøjagtigt som du angiver dem i rækkedefinitionen. 
> [!NOTE]
> Bredden af beskrivelseskolonnen i rapporten er angivet i kolonnedefinitionen. Hvis teksten i kolonnen **Beskrivelse** i rækkedefinitionen er lang, skal du kontrollere bredden af **DESC**-kolonnen. Når du bruger dialogboksen **Indsæt rækker fra**, er værdierne i kolonnen **Beskrivelse** segmentværdierne eller dimensionsværdierne fra de økonomiske data. Du kan indsætte rækker for at tilføje beskrivende tekst, f.eks. en sektionsoverskrift eller en sektionstotal, og for at tilføje formatering, f.eks. en linje før en totalrække. Hvis rapporten indeholder et rapporteringstræ, kan du medtage den ekstra tekst, der er defineret for rapporteringsenhederne i rapporteringstræet. Du kan også begrænse den ekstra tekst til en bestemt rapporteringsenhed.

### <a name="add-the-description-for-a-line-on-a-report"></a>Tilføj beskrivelsen for en linje i en rapport

1.  Klik på **Rækkedefinitioner** i Report Designer, og åbn derefter den rækkedefinition, der skal ændres.
2.  Vælg cellen **Beskrivelse**, og angiv derefter navnet på rækken i rapporten.
3.  Anvend formatering.

### <a name="add-additional-text-from-a-reporting-tree-in-the-description"></a>Tilføje yderligere tekst fra et rapporteringstræ i beskrivelsen

1.  Klik på **Rækkedefinitioner** i Report Designer, og åbn derefter den rækkedefinition, der skal ændres.
2.  Angiv den supplerende tekstkode og anden tekst i den relevante **Beskrivelse**-celle.
3.  Anvend formatering.

### <a name="limit-the-additional-text-to-a-specific-reporting-unit"></a>Begrænse den ekstra tekst til en bestemt rapporteringsenhed

1.  Klik på **Rækkedefinitioner** i Report Designer, og åbn derefter den rækkedefinition, der skal ændres.
2.  Find den række, hvor ekstra tekst skal oprettes, og dobbeltklik derefter på cellen i kolonnen **Relaterede formler/rækker/enheder**.
3.  I dialogboksen **Valg af rapporteringsenhed** i feltet **Rapporteringstræ** skal du vælge et rapporteringstræ.
4.  I feltet **Vælg rapporteringsenhed til begrænsning** skal du udvide eller skjule rapporteringstræet og derefter vælge en rapporteringsenhed.

## <a name="add-a-format-code"></a>Tilføje en formatkode
Cellen **Formatkode** indeholder forskellige forudformaterede muligheder med hensyn til indholdet i rækken. Hvis cellen **Formatkode** er tom, fortolkes rækken som en række med detaljerede økonomiske data. 
> [!NOTE]
> Hvis en rapport indeholder formateringsrækker uden beløb, der vedrører beløbsrækker, der er undertrykt (for eksempel på grund af nul-saldi), kan du bruge kolonnen **Relaterede formler/rækker/enheder** for at forhindre, at der udskrives titel- og formatrækker.

### <a name="add-a-format-code-to-a-report-row"></a>Tilføje en formatkode til en rapportrække

1.  Klik på **Rækkedefinitioner** i Report Designer, og vælg derefter den rækkedefinition, der skal ændres.
2.  Dobbeltklik på cellen **Formatkode**.
3.  Vælg en formatkode på listen. Følgende tabel beskriver formatkoderne og deres handlinger.
    | Formatkode                   | Fortolkning af formatkoden | Handling|
    |---|---|---|
    | (Ingen)                        |                                    | Rydder cellen **Formatkode**.                                                                                                                                                                               |
    | TOT                           | I alt                              | Identificerer en række, der bruger matematiske operatorer i kolonnen **Relaterede formler/rækker/enheder**. Totaler indeholder enkle operatorer som f.eks. **+** eller **-**.                                                      |
    | CAL                           | Kalkulation                        | Identificerer en række, der bruger matematiske operatorer i kolonnen **Relaterede formler/rækker/enheder**. Beregningerne indeholder komplekse operatorer, f.eks. **+**, **-**, **\***, **/** og **IF/THEN/ELSE**-sætninger. |
    | DES                           | Betegnelse                        | Identificerer en overskriftslinje eller en tom linje i en rapport.                                                                                                                                                        |
    | LFT RGT CEN                   | Venstre Højre Centreret                  | Justerer rækkebeskrivelsesteksten på rapportsiden, uanset placeringen af teksten i kolonnedefinitionen.                                                                                               |
    | CBR                           | Rediger basisrække                    | Identificerer en række, der angiver basisrækken for kolonneberegninger.                                                                                                                                               |
    | COLUMN                        | Kolonneskift                       | Starter en ny kolonne i rapporten.                                                                                                                                                                             |
    | PAGE                          | Sideskift                         | Starter en ny side i rapporten.                                                                                                                                                                               |
    | ---                           | Enkelt understregning.                   | Placerer en enkelt streg under alle beløbskolonner i rapporten.                                                                                                                                                     |
    | ===                           | Dobbelt understregning.                   | Placerer en dobbelt streg under alle beløbskolonner i rapporten.                                                                                                                                                     |
    | LINE1                         | Tynd streg                          | Tegner en enkelt tynd streg på tværs af siden.                                                                                                                                                                      |
    | LINE2                         | Tyk linje                         | Tegner en enkelt tyk linje på tværs af siden.                                                                                                                                                                     |
    | LINE3                         | Stiplet linje                        | Tegner en enkelt punkteret streg på tværs af siden.                                                                                                                                                                    |
    | LINE4                         | Tyk og tynd streg           | Tegner en dobbelt streg på tværs af siden. Den øverste streg er tyk, og den nederste streg er tynd.                                                                                                                       |
    | LINE5                         | Tynd streg og tyk streg           | Tegner en dobbelt streg på tværs af siden. Den øverste streg er tynd, og den nederste streg er tyk.                                                                                                                       |
    | BXB BXC                       | Række i boks                          | Tegner en boks omkring de rækker i rapporten, der begynder med rækken **BXB** og slutter med rækken **BXC**.                                                                                                               |
    | REM                           | Bemærkning                             | Identificerer en række, der er en kommentarrække, og som ikke skal udskrives i rapporten. En bemærkning kan f.eks. forklare dine formateringsteknikker.                                                            |
    | SORT ASORT SORTDESC ASORTDESC | Sortér                               | Sorterer udgifter eller indtægter, sorterer en faktisk eller budgetafvigelsesrapport efter den største afvigelse eller sorterer rækkebeskrivelserne alfabetisk.                                                                   |

## <a name="specify-related-formulasrowsunits"></a>Angiv relaterede formler/rækker/enheder
Cellen **Relaterede formler/rækker/enheder** har flere formål. Afhængigt af typen af række kan cellen **Relaterede formler/rækker/enheder** udføre en af følgende funktioner:

-   Definere de rækker, der skal indgå i en beregning, når du bruger formatkoden **TOT** eller formatkoden **CAL**.
-   Sammenkæde en formateringsrække med en beløbsrække, så formateringen kun udskrives, når det relaterede beløb er udskrevet.
-   Begrænse en række til en bestemt rapporteringsenhed.
-   Definere basisrækken for beregninger, når du bruger formatkoden **BASEROW**.
-   Definere rækkerne, der skal sorteres, når du bruger en af sorteringsformatkoderne.

### <a name="use-a-row-total-in-a-row-definition"></a>Bruge en rækketotal i en rækkedefinition

Du kan bruge en formel for rækketotal til at tilføje eller fratrække beløbene i andre rækker. En formel til oprettelse af en rækketotal kan indeholde operatorerne + og - til at kombinere individuelle rækkekoder og områder. Områder er angivet med et kolon (:). Formlen kan indeholde op til 1.024 tegn. Her er et eksempel på en standardsammentællingsformel: 400 + 420 + 430 + 450 + 460LIABILITIES + EQUITY520:546520:546-LIABILITIES

### <a name="components-of-a-row-total-formula"></a>Komponenter i en rækketotalformel

Når du opretter en formel for rækketotal, skal du bruge rækkekoder til at angive, hvilke rækker der skal tilføjes eller fratrækkes i den aktuelle rækkedefinition, og du skal bruge operatorer til at angive, hvordan rækkerne kombineres. Totalrækker og beløbsrækker kan bruges i enhver kombination. **Bemærk:** Alle totalrækker, der er i et område, er udeladt. Hvis du vil oprette en samlet total, kan du angive området af rækker. Hvis den første række i et område er totalrække, medtages rækken i den nye total. I følgende tabel beskrives, hvordan operatorer bruges i rækketotalformler.

| Operatør | Elsempelformel | Betegnelse                                                 |
|----------|-----------------|-------------------------------------------------------------|
| +        | 100+330         | Lægger beløbet i række 100 til beløbet i række 330.        |
| :        | 100:330         | Lægger totalerne af alle rækker mellem række 100 og række 330 sammen.    |
| -        | 100-330         | Trækker beløbet i række 100 fra beløbet i række 330. |

### <a name="create-a-row-total"></a>Oprette en ny rækketotal

1.  Klik på **Rækkedefinitioner** i Rapportdesigner, og åbn derefter en rækkedefinition, der skal ændres.
2.  Dobbeltklik på cellen **Formatkode** i rækkedefinitionen, og vælg **TOT**.
3.  Angiv totalformlen i cellen **Relaterede formler/rækker/enheder**.

### <a name="relate-a-format-row-to-an-amount-row"></a>Relater en formatrække til en beløbsrække

I kolonnen **Formatkode** i en rækkedefinition, anvender formatkoderne **DES**, **LFT**, **RGT**, **CEN**, **---** og **===** formatering på rækker uden beløb. For at forhindre, at denne formatering udskrives, når de relaterede beløbsrækker undertrykkes (eksempelvis fordi beløbsrækkerne indeholder nulværdier eller ingen periodeaktivitet), skal du relatere formatrækkerne til de tilsvarende beløbsrækker. Denne funktion er nyttig, når du vil forhindre, at sidehoveder eller formatering, der er relateret til subtotaler, bliver udskrevet, når der ingen detaljer er at udskrive for perioden. 
    > [!NOTE]
    >  You can also prevent the detailed amount rows from being printed by clearing the option to display rows without amounts. This option is located on the **Settings** tab of the report definition. By default, transaction detail accounts that have a zero balance or no period activity are suppressed in reports. To show these transaction detail accounts, select the **Display rows without an amounts** check box on the **Settings** tab of the report definition.

### <a name="relate-a-format-row-to-an-amount-row"></a>Relater en formatrække til en beløbsrække

1.  Klik på **Rækkedefinitioner** i Report Designer, og vælg derefter den rækkedefinition, der skal ændres.
2.  I formateringsrækken i cellen **Relaterede formler/rækker/enheder** skal du angive rækkekoden for den beløbsrække, der skal undertrykkes. **Bemærk:** Hvis du vil undertrykke en beløbsrække, skal rækkens saldo være 0 (nul). En beløbsrække, som har en saldo, undertrykkes ikke.
3.  Klik på **Gem** i menuen **Filer**.

### <a name="example-of-preventing-printing-of-rows"></a>Eksempel på at forhindre udskrivning af rækker

I følgende eksempel ønsker Gitte at forhindre, at overskriften og understregningstegn i rækken **Total kontant** i sin rapport udskrives, fordi der ikke var aktivitet i nogen af kassekontiene. Derfor angiver hun i række 220 (der, som formatkoden **---** angiver, er en formateringsrække) i cellen **Relaterede formler/rækker/enheder** **250**, som er rækkekoden for den beløbsrække, hun ønsker at undertrykke. [![RelatedRowsRowDefinition](./media/relatedrowsrowdefinition-1024x144.png)](./media/relatedrowsrowdefinition.png)

## <a name="select-the-base-row-for-a-column-calculation"></a>Marker den række, der er basis for beregning af en kolonne
I relationel rapportering tildeler du en eller flere basisrækker i rækkedefinitionen ved hjælp af formatkoden **CBR** (rediger basisrække). En beregning i kolonnedefinitionen refererer derefter til en basisrække. Her er nogle typiske eksempler på CBR-beregninger:

-   Procentdel af samlet omsætning, som den er relateret til individuelle indtægter
-   Procentdel af samlet udgift, som den er relateret til individuelle udgifter
-   Procentdel af bruttoavance, som den er relateret til oplysninger om division eller afdeling.

Der er defineret en eller flere basisrækker i rækkedefinitionen, og derefter bestemmer kolonnedefinitionen den relation, som basisrækken rapporteres på. Den kode, der bruges i kolonneformlen er **BASEROW**. Følgende grundlæggende matematiske operationer bruges sammen med **BASEROW**: dividere, multiplicere, addere eller fratrække. Den operation, der oftest b ruges, er division med **BASEROW**, hvor resultatet vises som en procentdel. Kolonneberegninger, der bruger **BASEROW** i formlen, bruger rækkedefinitionen for de relaterede basisrækkekoder. **CBR**-rækker har følgende egenskaber:

-   **CBR**-rækker udskrives ikke på den færdige rapport.
-   **CBR**-formatkoden og dens relaterede rækkekode er placeret over den række eller sektion, der viser relaterede beregninger.

I en kolonnedefinition angiver kolonnetypen **CALC** en kolonne, hvor der angives en formel i rækken **Formel**. Denne formel fungerer på data for denne kolonne i rapporten og bruger nøgleordet Baserow for basisberegninger på **CBR**-formatkoder i rækken. I rækkedefinitionen definerer **CBR**-formatkoden basisrækken for kolonner, der beregner en procentdel af eller multipliceres med basisrækken for hver række i rapporten. Du kan have flere **CBR**-formatkoder i et rækkeformat, f.eks én for nettoomsætning, én til bruttosalg og én for samlede udgifter. Normalt bruges **CBR**-formatkoden til at oprette en procentdel for konti, der skal sammenlignes med en totallinje. En basisrække bruges til alle beregninger, indtil der defineres en anden basisrække. Du skal definere en start-**CBR**-formatkode og en slut-**CBR**-formatkode. Hvis du for eksempel vil bestemme udgifter som en procentdel af nettosalget, kan du dividere værdien i hver udgiftsrække med værdien i rækken for nettosalg. I så fald er rækken for nettosalg basisrækken. Du kan definere en kolonnedefinition, der rapporterer det aktuelle og år til dato-resultatet sammen med en basisprocentdel af hvert resultat, som vist i følgende eksempel. Start med en detaljeret resultatopgørelse.

### <a name="select-the-base-row-in-a-row-definition-for-a-column-calculation"></a>Vælg basisrækken i en rækkedefinition til en kolonneberegning

1.  Klik på **Kolonnedefinitioner** i Report Designer, og åbn derefter kolonnedefinitionen for en resultatopgørelse.
2.  Føj en ny kolonne til kolonnedefinitionen, og indstil kolonnetypen til **CALC**.
3.  I cellen **Formel** for den nye kolonne skal du indtaste formlen **X/BASEROW**, hvor **X** er den **FD**-kolonnetype, der skal vises en procentdel af.
4.  Dobbeltklik på cellen **Tilsidesæt format/valuta**.
5.  I dialogboksen **Tilsidesæt format** på listen **Formatkategori** skal du vælge **Procent** og derefter klikke på **OK**.
6.  I menuen **Filer** skal du klikke på **Gem som** for at gemme kolonnedefinitionen under et nyt navn. Tilføj **CBR** til det aktuelle filnavn (for eksempel **CUR\_YTD\_CBR**). Denne kolonnedefinition af din basisrækkekolonnedefinition.
7.  Klik på **Rækkedefinitioner** i Report Designer, og åbn derefter den rækkedefinition, der skal ændres ved hjælp af basisrækkeberegningen.
8.  Indsæt en ny række over den række, hvor basisrækkeberegningen skal starte.
9.  Dobbeltklik på cellen **Formatkode** i rækkedefinitionen, og vælg derefter **CBR**.
10. I cellen **Relaterede formler/rækker/enheder** skal du angive rækkekodenummeret for basisrækken.

### <a name="example-of-base-row-calculation"></a>Eksempel på beregning af basisrække

I følgende eksempel på en rækkedefinition viser række 100, at basisrækken for beregninger er række 280. [![Eksempel på beregning af basisrække.](./media/cbrrowdefinition.png)](./media/cbrrowdefinition.png) I følgende eksempel på en kolonnedefinition benyttes formatkoden **CBR** til beregningerne. Ved beregningen i kolonne C divideres værdien i kolonne B i rapporten med værdien i række 280 i kolonne B. Tilsidesættelsen af format i kolonne B udskriver resultatet af beregningen som en procentdel. På samme måde er hvert beløb i kolonne E beløbet i kolonne D som en procentdel af nettosalget. [![Eksempel på kolonnedefinition.](./media/cbrcolumndefinition2.png)](./media/cbrcolumndefinition2.png) Følgende eksempel viser en rapport, der kan genereres ud fra de tidligere beregninger. [![Eksempel på rapport baseret på tidligere eksempelberegninger.](./media/cbrreport-1024x272.png)](./media/cbrreport.png)

## <a name="select-a-sorting-code-for-a-row-definition"></a>Vælge en sorteringskode for en rækkedefinition
Sorteringskoder sorterer konti eller værdier, sorterer en faktisk eller budgetafvigelsesrapport efter den største afvigelse eller sorterer rækkebeskrivelserne alfabetisk. Følgende sorteringskoder er tilgængelige:

-   **SORT** – sorterer rapporten i stigende rækkefølge, baseret på værdier i den angivne kolonne.
-   **ASORT** – sorterer rapporten i stigende rækkefølge, baseret på den absolutte værdi af værdierne i den angivne kolonne. Med andre ord ignoreres tegnet for hver værdi, når værdierne er sorteret. Formatkoden ordner værdierne efter størrelsen af afvigelsen, uanset om afvigelsen er positiv eller negativ.
-   **SORTDESC** – sorterer rapporten i faldende rækkefølge, baseret på værdier i den angivne kolonne.
-   **ASORTDESC** – sorterer rapporten i faldende rækkefølge, baseret på den absolutte værdi af værdierne i den angivne kolonne.

### <a name="select-a-sorting-code"></a>Vælge en sorteringskode

1.  Klik på **Rækkedefinitioner** i Report Designer, og åbn derefter den rækkedefinition, der skal ændres.
2.  Dobbeltklik på cellen **Formatkode**, og vælg derefter en sorteringskode.
3.  I cellen **Relaterede formler/rækker/enheder** skal du angive intervallet for rækkekoder, der skal sorteres. For at angive et interval, skal du angive den første rækkekode, et kolon (:) og derefter den sidste rækkekode. Du kan f.eks. indtaste **160:490** for at angive, at intervallet er række 160 til og med række 490.
4.  I cellen **Kolonnebegrænsning** skal du angive bogstavet for den rapportkolonne, der skal bruges til sortering. 
    > [!NOTE]
    > Medtag kun beløbsrækker i en sorteringsberegning.

### <a name="examples-of-ascending-and-descending-column-values"></a>Eksempler på stigende og faldende kolonneværdier

I følgende eksempel sorteres værdierne i kolonne D i rapporten i stigende rækkefølge for række 160 til og med 490. Desuden skal de absolutte værdier i kolonne G i rapporten sorteres i faldende rækkefølge for række 610 til og med 940.

| Rækkekode | Beskrivelse                                         | Formatkode | Relaterede formler/rækker/enheder | Normal saldo | Kolonnebegrænsning | Link til økonomiske dimensioner |
|----------|-----------------------------------------------------|-------------|-----------------------------|----------------|--------------------|------------------------------|
| 100      | Sorteret efter månedlig afvigelse i stigende rækkefølge       | DES         |                             |                |                    |                              |
| 130      |                                                     | SORT        | 160:490                     |                | D                  |                              |
| 160      | Salg                                               |             |                             | C              |                    | 4100                         |
| 190      | Salgsstatistik                                       |             |                             |                |                    | 4110                         |
|          | ...                                                 |             |                             |                |                    |                              |
| 490      | Renteindtægt                                     |             |                             | C              |                    | 7000                         |
| 520      |                                                     | DES         |                             |                |                    |                              |
| 550      | Sorteret efter absolut afvigelse ÅTD i faldende rækkefølge | DES         |                             |                |                    |                              |
| 580      |                                                     | ASORTDESC   | 610:940                     |                | G                  |                              |
| 610      | Salg                                               |             |                             | C              |                    | 4100                         |
| 640      | Salgsreturneringer                                       |             |                             |                |                    | 4110                         |
|          | ...                                                 |             |                             |                |                    |                              |
| 940      | Renteindtægter                                     |             |                             | C              |                    | 7000                         |

Her er et eksempel på den rapport, der genereres.

|||||||||
|---|---|---|---|---|---|---|
|**Analyse af afvigelse (sorteret efter afvigelse)**|||||||

|**Beijing- og Atlanta-områder**|||||||

|**For de syv måneder, der slutter den 31. juli 2013**|||||||

||**juli**|**ÅTD**|||||

||**Faktiske**|**Budget**|**Afvigelse**|**Faktiske**|**Budget**|**Afvigelse**|

|**Sorteret efter månedlig afvigelse i stigende rækkefølge**|||||||

|VAREFORBRUG|873,872|236,144|(637,728)|4,864,274|1,590,315|(3,273,959)|

|Lønninger|97.624|65.573|(32.051)|653.884|441.664|(212.220)| |Salgsrabatter|36.383|24.152|(12.231)|241. 562|162.670|(78.892)| |Returvarer|10.917|7.246|(3.671)|62.809|48.803|(14.006)| |Lejeudgift|12.052|9.019|(3.033)|80.444|60.748|(19.696)| |Kontorudgifter|5.023|3.291|(1.732)|33.420|22.098|(11.322)| |Rejseudgifter|7. 656|7.641|(15)|51.062|51.469|407| |Salg|1.240.119|410.389|829.730|7.139.288|2.764.549|4.374.739| |**Sorteret efter år til dato absolutte afvigelse i faldende rækkefølge**||||||| |Salg|1.240.119|410.389|829.730|7.139.288|2.764.549|4.374.739| |Rejseudgifter|7.656|7.641|(15)|51.062|51.469|407| |Kontorudgifter|5.023|3.291|(1.732)|33.420|22.098|(11.322)| |Returvarer|10.917|7.246|(3.671)|62.809|48.803|(14.006)| |Lejeudgift|12.052|9.019|(3.033)|80.444|60.748|(19.696)| |Salgsrabatter|36.383|24.152|(12.231)|241.562|162.670|(78.892)| |Lønninger|97.624|65.573|(32.051)|653.884|441.664|(212.220)| |VAREFORBRUG|873.872|236.144|(637.728)|4.864.274|1.590.315|(3.273.959)|

## <a name="specify-a-format-override-cell"></a>Angiv en celle af typen Tilsidesæt format
Cellen **Tilsidesæt format** angiver den formatering, der anvendes til rækken, når rapporten udskrives. Denne formatering tilsidesætter den formatering, der er angivet i kolonnedefinitionen og rapportdefinitionen. Som standard er den formatering, der er angivet i disse definitioner, valuta. Hvis en række i rapporten angiver antallet af aktiver, såsom antallet af bygninger, og en anden række angiver pengeværdien af disse aktiver, kan du tilsidesætte valutaformateringen og angive numerisk formatering for den række, der angiver antallet af bygninger. Du angiver disse oplysninger i dialogboksen **Tilsidesæt format**. De tilgængelige indstillinger afhænger af den formatkategori, du vælger. Området **Prøve** i dialogboksen viser eksempelformater. Følgende formatkategorier er tilgængelige:

-   Formatering af valuta
-   Formatering af tal
-   Formatering af procenter
-   Brugerdefineret formatering

### <a name="override-cell-formatting"></a>Tilsidesæt celleformatering

1.  Åbn den rækkedefinition, der skal ændres, i Report Designer.
2.  I den række, som formatet skal tilsidesættes for, skal du dobbeltklikke på cellen i kolonnen **Tilsidesæt format**.
3.  I dialogboksen **Tilsidesæt format** skal du vælge de formateringsindstillinger, der skal bruges til denne række i rapporten.
4.  Klik på **OK**.

### <a name="currency-formatting"></a>Formatering af valuta

Formatering af valuta gælder for et regnskabsbeløb og inkluderer valutasymbolet. Følgende indstillinger er tilgængelige:

-   **Valutasymbol** – Valutasymbolet for rapporten. Værdien tilsidesætter indstillingen **Internationale indstillinger** for firmaoplysningerne.
-   **Negative tal** – negative tal kan have et minustegn (-), de kan vises i parentes, eller de kan have en trekant (∆).
-   **Decimaler** – antallet af cifre, der skal vises efter decimaltegnet.
-   **Tekst for tilsidesættelse ved nulværdi** – teksten, der skal medtages i rapporten, når beløbet er 0 (nul). Denne tekst vises som den sidste linje i området **Eksempel**. 
    > [!NOTE]
    >  Hvis udskrivning undertrykkes for nulværdier eller ingen periodeaktivitet, undertrykkes denne tekst.

### <a name="numeric-formatting"></a>Formatering af tal

Formatering af tal gælder for alle beløb og inkluderer ikke et valutasymbol. Følgende valgmuligheder er tilgængelige:

-   **Negative tal** – negative tal kan have et minustegn (-), de kan vises i parentes, eller de kan have en trekant (∆).
-   **Decimaler** – antallet af cifre, der skal vises efter decimaltegnet.
-   **Tekst for tilsidesættelse ved nulværdi** – teksten, der skal medtages i rapporten, når beløbet er 0 (nul). Denne tekst vises som den sidste linje i området **Eksempel**. 
    > [!NOTE]
    >  Hvis udskrivning undertrykkes for nulværdier eller ingen periodeaktivitet, undertrykkes denne tekst.

### <a name="percentage-formatting"></a>Formatering af procenter

Formatering af procenter indeholder procenttegnet (%). Følgende valgmuligheder er tilgængelige:

-   **Negative tal** – negative tal kan have et minustegn (-), de kan vises i parentes, eller de kan have en trekant (∆).
-   **Decimaler** – antallet af cifre, der skal vises efter decimaltegnet.
-   **Tekst for tilsidesættelse ved nulværdi** – teksten, der skal medtages i rapporten, når beløbet er 0 (nul). Denne tekst vises som den sidste linje i området **Eksempel**. 
    > [!NOTE]
    >  Hvis udskrivning undertrykkes for nulværdier eller ingen periodeaktivitet, undertrykkes denne tekst.

### <a name="custom-formatting"></a>Brugerdefineret formatering

Brug kategorien for brugerdefineret formatering til at oprette et brugerdefineret tilsidesættelse af format. Følgende valgmuligheder er tilgængelige:

-   **Type** – Det brugerdefinerede format.
-   **Tekst for tilsidesættelse ved nulværdi** – teksten, der skal medtages i rapporten, når beløbet er 0 (nul). Denne tekst vises som den sidste linje i området **Eksempel**. 
    > [!NOTE]
    >  Hvis udskrivning undertrykkes for nulværdier eller ingen periodeaktivitet, undertrykkes denne tekst.

Typen bør angive den positive værdi og derefter den negative værdi. Normalt angiver du et lignende format, som differentierer positive og negative værdier. Hvis du for eksempel vil angive, at både positive og negative værdier har to decimaler, men negative værdier vises i parenteser, skal du angive **0,00;(0,00)**. Følgende tabel viser brugerdefinerede formater, du kan bruge til at styre formatet af dine værdier. Alle eksempler er baseret på værdien 1234,56.

| Format                         | Positiv   | Negativ     | Nul    |
|--------------------------------|------------|--------------|---------|
| 0                              | 1235       | -1235        | 0       |
| 0;0                            | 1235       | 1235         | 0       |
| 0;(0);-                        | 1235       | 1235         | -       |
| \#,\#\#\#;(\#,\#\#\#);“”       | 1.235      | (1.235)      | (Tom) |
| \#,\#\#0,00;(\#,\#\#0,00);nul | 1.234,56   | (1.234,56)   | nul    |
| 0,00 %;(0,00 %)                  | 123456,00 % | (123456,00 %) | 0,00 %   |

## <a name="specify-a-normal-balance-cell"></a>Angiv en celle af typen Normal saldo
Cellen **Normal saldo** i en rækkedefinition styrer fortegnet på beløb i en række. Hvis du vil ændre fortegnet for en række, eller hvis den normale saldo for en konto er et kreditbeløb, skal du angive et **C** i cellen **Normal saldo** for den pågældende række. Report Designer vender fortegnet om på alle kreditstatuskonti i den pågældende række. Når rapportdesigneren konverterer disse konti, fjernes debet/kredit-egenskaber fra alle beløb, og gør derfor sammentællingen ligetil. Hvis du for eksempel vil beregne nettoresultatet, skal du trække udgifter fra indtægter. Sammentalte og beregnede rækker påvirkes normalt ikke af en **C**-kode. Men **XCR**-protokollen til udskrivning i kolonnedefinitionen vender tegnet for en række, der indeholder et **C** i kolonnen **Normal saldo**. Denne formatering er især vigtig, når du vil have vist alle negative afvigelser som negative beløb. Hvis et sammentalt eller beregnet tal har det forkerte fortegn, skal du angive et **C** i cellen **Normal saldo** for rækken for at vende fortegnet.

## <a name="specify-a-row-modifier-cell"></a>Angiv en celle af typen Rækkemodifikator
Indholdet af cellen **Rækkemodifikator** i en rækkedefinition tilsidesætter regnskabsårene, perioderne og andre oplysninger, der er angivet i kolonnedefinitionen for rækken. Den valgte modifikator gælder for alle konti i rækken. Du kan redigere hver række ved hjælp af en eller flere af følgende typer modifikatorer:

-   Kontomodifikatorer
-   Bogkodemodifikatorer
-   Konto- og transaktionsattributter

### <a name="override-a-column-definition"></a>Tilsidesætte en kolonnedefinition

1.  Åbn den rækkedefinition, der skal ændres, i Report Designer.
2.  I den række, hvor du vil tilsidesætte kolonnedefinitionen skal du dobbeltklikke på cellen **Rækkemodifikator**.
3.  I dialogboksen **Rækkemodifikator** skal du vælge en indstilling i feltet **Kontomodifikator**. Se en beskrivelse af indstillingerne i afsnittet "Kontomodifikatorer".
4.  I feltet **Bogkodemodifikator** skal du vælge den bogkode, der skal bruges til rækken.
5.  Under **Attributter** skal du benytte nedenstående fremgangsmåde for at tilføje en post for hver attribut, der skal medtages i rækkekoden:
    1.  Dobbeltklik på cellen **Attribut**, og vælg et attributnavn. **Advarsel:** erstat nummertegnet (\#) med en numerisk værdi.
    2.  Dobbeltklik på cellen **Fra**, og angiv den første værdi for området.
    3.  Dobbeltklik på cellen **Til**, og angiv den sidste værdi for området.

6.  Klik på **OK**.

### <a name="account-modifiers"></a>Kontomodifikatorer

Når du vælger en bestemt konto, kombinerer rapportdesigneren normalt kontoen og regnskabsårene, perioderne og andre oplysninger, du angiver i kolonnedefinitionen. Du kan bruge forskellige oplysninger, såsom forskellige regnskabsperioder for bestemte rækker. Følgende tabel viser de tilgængelige kontomodifikatorer. Erstat nummertegnet (\#) med en værdi, der er lig med eller mindre end antallet af perioder i et regnskabsår.

| Kontomodifikator | Hvad udskrives                                                                           |
|------------------|-------------------------------------------------------------------------------------------|
| /BB              | Startsaldoen for en konto                                                     |
| /\#              | Saldoen for den angivne periode.                                                     |
| /-\#             | Saldoen for den periode, der er \# perioder før den aktuelle periode.                  |
| /+\#             | Saldoen for den periode, der er \# perioder efter den aktuelle periode.                   |
| /C               | Saldoen for den aktuelle periode.                                                       |
| /K-\#            | Saldoen for den periode, der er \# perioder før den aktuelle periode.                  |
| /K+\#            | Saldoen for den periode, der er \# perioder efter den aktuelle periode.                   |
| /Y               | Saldoen år til dato i den aktuelle periode.                                      |
| /Y-\#            | Saldoen år til dato i den periode, der er \# perioder før den aktuelle periode. |
| /Y+\#            | Saldoen år til dato i den periode, der er \# perioder efter den aktuelle periode.  |

### <a name="book-code-modifiers"></a>Bogkodemodifikatorer

Du kan begrænse en række til en eksisterende kode. Kolonnedefinitionen skal indeholde mindst én **FD**-kolonne, der indeholder en bogkode. 
> [!NOTE]
> Bogkodebegrænsningen for en række tilsidesætter bogkodebegrænsningerne i kolonnedefinitionen for den pågældende række.

### <a name="account-and-transaction-attributes"></a>Konto- og transaktionsattributter

Nogle regnskabssystemer understøtter kontoattributter og transaktionsattributter i regnskaberne. Disse attributter fungerer som virtuelle kontosegmenter og kan indeholde yderligere oplysninger om kontoen eller transaktionen. Disse ekstra oplysninger kan være konto-id'er, batch-id'er, postnumre eller andre attributter. Hvis regnskabssystemet understøtter attributter, kan du bruge kontoattributter eller transaktionsattributter som rækkemodifikatorer i rækkedefinitionen. Du kan finde oplysninger om, hvordan du tilsidesætter rækkeoplysninger, i afsnittet "Tilsidesætte en kolonnedefinition" tidligere i denne artikel.

## <a name="specify-a-link-to-financial-dimensions-cell"></a>Angive et hyperlink til cellen Økonomiske dimensioner
Cellen **Link til økonomiske dimensioner** indeholder links til de økonomiske data, der skal medtages i hver række i en rapport. Denne celle indeholder dimensionsværdier, men du kan angive celler i et regneark i Microsoft Excel i stedet for eller sammen med segmentværdier eller dimensionsværdier. Dialogboksen **Dimensioner** åbnes ved at dobbeltklikke på cellen **Link til økonomiske dimensioner**. 
> [!NOTE]
> Report Designer kan ikke vælge konti, dimensioner eller felter fra Microsoft Dynamics ERP-systemet, der indeholder et af følgende reserverede tegn: &, \*, \[, \], { eller }. Hvis du vil angive oplysninger for en række, der allerede findes i rækkedefinitionen, skal du tilføje oplysningerne i cellen **Link til økonomiske dimensioner**. Hvis du vil tilføje nye rækker, der indeholder hyperlinks til de økonomiske data, skal du bruge dialogboksen **Indsæt rækker fra** for at oprette nye rækker i rapportdefinitionen. Kolonnens titel ændres, afhængigt af hvordan kolonnen er konfigureret, som vist i følgende tabel.

| Linktype, der er valgt       | Beskrivelsen af kolonnen Link ændres til dette |
|----------------------------------|----------------------------------------------------|
| Økonomiske dimensioner             | Link til økonomiske dimensioner                       |
| Eksternt regneark               | Link til regneark                                  |
| Økonomisk dimensioner + regneark | Link til økonomiske dimensioner + regneark           |
| Management Reporter-rapport       | Management Reporter-rapport                         |

### <a name="specify-a-dimension-or-range"></a>Angiv en dimension eller et interval

1.  Åbn den rækkedefinition, der skal ændres, i Report Designer.
2.  Dobbeltklik på en celle i kolonnen **Link til økonomiske dimensioner**.
3.  Dobbeltklik på en celle under dimensionsnavnet i dialogboksen **Dimensioner**.
4.  Vælg **Person eller interval** i dialogboksen for dimensionen.
5.  I feltet **Fra** skal du angive den første dimension eller klikke på ![Gennemse](https://i-technet.sec.s-msft.com/dynimg/IC679490.gif "Gennemse") for at søge efter tilgængelige dimensioner. Du kan angive en række dimensioner ved at angive den sidste dimension i feltet **Til**.
6.  Klik på **OK** for at lukke dialogboksen for dimensionen. Dialogboksen **Dimensioner** viser den opdaterede dimension eller det opdaterede interval.
7.  Klik på **OK** for at lukke dialogboksen **Dimensioner**.

## <a name="display-zero-balance-accounts-in-a-row-definition"></a>Få vist konti med nulsaldo i en rækkedefinition
Som standard udskriver rapportdesigneren ikke rækker, der ikke har en tilsvarende saldo i de økonomiske data. Du kan derfor oprette en rækkedefinition, der omfatter alle naturlige segmentværdier eller alle dimensionsværdier og derefter bruge denne rækkedefinition til alle dine afdelinger.

### <a name="modify-zero-balance-settings"></a>Ændre indstillingerne for nulsaldo

1.  Åbn den rapportdefinition, der skal ændres, i Report Designer.
2.  På fanen **Indstillinger** under **Anden formatering** skal du vælge indstillinger for den rækkedefinition, der bruges i rapportdefinitionen.
3.  Gå til menuen **Filer**, og klik på **Gem** for at gemme ændringerne.

## <a name="use-wildcard-characters-and-ranges-in-a-row-definition"></a>Bruge jokertegn og intervaller i en rækkedefinition
Når du angiver en naturlig segmentværdi i dialogboksen **Dimensioner**, kan du anbringe et jokertegn ? eller \*) i en hvilken som helst placering i et segment. Report Designer udtrækker alle værdierne for de definerede positioner uden at tage højde for jokertegnene. Rækkedefinitionen indeholder for eksempel kun naturlige segmentværdier, og naturlige segmenter har fire tegn. Ved at angive **6???** i en række beder du rapportdesigneren om at medtage alle konti, der har en naturligt segment-værdi, der starter med 6. Hvis du angiver **6\***, returneres det samme resultat, men resultaterne omfatter også variabel bredde-værdier som **60** og **600000**. rapportdesigneren erstatter de enkelte jokertegn (?) med et komplet udvalg af mulige værdier, som omfatter bogstaver og specialtegn. I intervallet fra **12?0** til og med **12?4** erstattes jokertegnet i **12?0** for eksempel af den laveste værdi i tegnsættet, og jokertegnet i **12?4** erstattes af den højeste værdi i tegnsættet. 
> [!NOTE]
> Du bør undgå at bruge jokertegn for start- og slutkonti i intervaller. Hvis du bruger jokertegn i den første konto eller den sidste konto, får du måske uventede resultater.

### <a name="single-segment-or-single-dimension-ranges"></a>Enkeltsegment- eller enkeltdimensionsområder

Du kan angive en række segmentværdier eller dimensionsværdier. Fordelen ved at angive et interval er, at du ikke behøver at opdatere rækkedefinitionen, hver gang der tilføjes en ny segmentværdi eller dimensionsværdi til de økonomiske data. Intervallet **+ konto = \[6100:6900\]** henter for eksempel værdierne fra konto 6100 til og med 6900 i rækkebeløbet. Når et interval indeholder et jokertegn (?), evaluerer rapportdesigneren ikke intervallet tegn for tegn. I stedet bestemmes den lave og høje ende af intervallet, og derefter medtages slutværdierne og alle værdier mellem dem. 
> [!NOTE]
> Report Designer kan ikke vælge konti, dimensioner eller felter fra Microsoft Dynamics ERP-systemet, der indeholder et af følgende reserverede tegn: &, \*, \[, \], { eller }. Du kan kun tilføje et plustegn (&), når du automatisk opretter rækkedefinitioner ved hjælp af dialogboksen **Indsæt rækker fra dimensioner**.

### <a name="multiple-segment-or-multiple-dimension-ranges"></a>Intervaller med flere segmenter eller flere dimensioner

Når du angiver et interval ved hjælp af kombinationer af flere dimensionsværdier, foretages intervalsammenligningen på basis af ..\financial-dimensions\dimension-by-dimension. Intervalsammenligningen kan ikke udføres tegn for tegn eller på basis af et delvist segment. Intervallet **+ konto = \[5000:6000\], afdeling = \[1000:2000\], bærer = \[00\]** omfatter for eksempel kun de konti, der svarer til hvert enkelt segment. I dette scenarie skal den første dimension være i intervallet fra 5000 til 6000, den anden dimension skal være i intervallet fra 1000 til 2000, og den sidste dimension skal være 00. For eksempel er **+ konto =\[5100\], afdeling =\[1100\], bærer =\[01\]** ikke medtaget i rapporten, da det sidste segment er uden for det angivne interval. Hvis en segmentværdi indeholder mellemrum, skal du sætte værdien i kantede parenteser (\[ \]). Følgende værdier er gyldige for et segment på fire tegn: **\[ 234\], \[123 \], \[1 34\]**. Dimensionsværdier skal omsluttes af kantede parenteser (\[ \]), og rapportdesigneren tilføjer disse parenteser for dig. Når et interval med flere segmenter eller flere dimensioner indeholder jokertegn (? eller \*) bestemmes den lave og høje ende af intervallet med flere segmenter eller flere dimensioner, og derefter medtages slutværdierne og alle værdier imellem dem. Hvis du har et stort interval, såsom hele rækken af konti fra 40000 til og med 99999, skal du angive en gyldig startkonto og slutkonto, hvis det er muligt. 
> [!NOTE]
> Report Designer kan ikke vælge konti, dimensioner eller felter fra Microsoft Dynamics ERP-systemet, der indeholder et af følgende reserverede tegn: &, \*, \[, \], { eller }. Du kan kun tilføje et plustegn (&), når du automatisk opretter rækkedefinitioner ved hjælp af dialogboksen **Indsæt rækker fra dimensioner**.

## <a name="add-or-subtract-from-other-accounts-in-a-row-definition"></a>Tilføje eller trække fra andre konti i en rækkedefinition
Hvis du vil tilføje eller fratrække pengebeløbene på en konto fra pengebeløbene på en anden konto, kan du bruge plustegnet (+) og minustegnet (-) i cellen **Link til økonomiske dimensioner**. Følgende tabel viser gyldige formater for links til addition og subtraktion til økonomiske data.

| Handling  | Brug dette format:  |
|------------|-----------------|
| Tilføj to fuldt kvalificerede konti.                                                       | + Division = \[000\], konto = \[1205\], afdeling = \[00\] + Division = \[100\], konto = \[1205\], afdeling = \[00\] |
| Tilføj to segmentværdier.                                                                 | + Konto = \[1205\] + konto = \[1210\]                                                                           |
| Tilføj segmentværdier, der indeholder jokertegn.                                    | + Konto = \[120? + konto = \[11??\]                                                                             |
| Tilføj et interval af fuldt kvalificerede konti.                                                | + Division = \[000:100\], konto = \[1205\], afdeling = \[00\]                                                   |
| Tilføj et interval af segmentværdier.                                                          | +Konto = \[1200:1205\]                                                                                       |
| Tilføj et interval af segmentværdier, der indeholder jokertegn.                         | +Konto = \[120?:130?\]                                                                                       |
| Træk en fuldt kvalificeret konto fra en anden fuldt kvalificeret konto.              | + Division = \[000\], konto = \[1205\], afdeling = \[00\] - Division = \[100\], konto = \[1205\], afdeling = \[00\] |
| Træk en segmentværdi fra en anden segmentværdi.                                  | + Konto = \[1205\] - konto = \[1210\]                                                                           |
| Træk en segmentværdi, der indeholder et jokertegn fra en anden segmentværdi. | + Konto = \[1200\] - konto = \[11??\]                                                                           |
| Træk et interval af fuldt kvalificerede konti fra.                                           | -Division = \[000:100\], konto = \[1200:1205\], afdeling = \[00:01\]                                           |
| Træk et interval af segmentværdier fra.                                                     | -Konto = \[1200:1205\]                                                                                       |
| Træk et interval af segmentværdier, der indeholder jokertegn, fra.                    | -Konto = \[120?:130?\]                                                                                       |

Selvom du kan redigere kontiene direkte, kan du også bruge dialogboksen **Dimensioner** til at anvende den korrekte formatering på dine hyperlinks til økonomiske data. Alle værdierne kan indeholde jokertegn (? eller \*). Report Designer kan dog ikke vælge konti, dimensioner eller felter fra Microsoft Dynamics ERP-systemet, der indeholder et af følgende reserverede tegn: &, \*, \[, \], {, eller }. 
> [!NOTE]
> For at trække værdier fra, skal du sætte parenteser omkring værdierne. Hvis du for eksempel angiver **450?-(4509)**, vises det som **+ konto = \[4509\] - konto = \[450?\]**, og du instruerer rapportdesigneren i at trække beløbet for kontosegment 4509 fra beløbet for et kontosegment. der starter med 450.

### <a name="add-or-subtract-accounts-from-other-accounts"></a>Lægge konti til eller trække konti fra andre konti

1.  Åbn den rækkedefinition, der skal ændres, i Report Designer.
2.  I den relevante række skal du dobbeltklikke på cellen i kolonnen **Link til økonomiske dimensioner**.
3.  I den første række i dialogboksen **Dimensioner** skal du benytte nedenstående fremgangsmåde:
    1.  I det første felt skal du markere alle dimensioner (standard) eller klikke for at åbne dialogboksen **Administrer dimensionssæt**, hvor du kan oprette, redigere, kopiere eller slette et sæt.
    2.  Dobbeltklik på cellen **Operator +/-** , og vælg plus- (**+**) eller minusoperatoren (**-**), der gælder for en eller flere dimensionsværdier eller sæt i rækken.
    3.  I den relevante kolonne med dimensionsværdier skal du dobbeltklikke på cellen for at åbne dialogboksen **Dimensioner** og vælge, om denne dimensionsværdi er for en enkelt dimension eller et interval, et dimensionsværdisæt eller samlekonti. Du finder beskrivelser af felterne i dialogboksen **Dimensioner** i afsnittet "Beskrivelse af dialogboksen Dimensioner".
    4.  Angiv segmentværdier i kolonnen **Fra** og kolonnen **Til**.

4.  Gentag trin 2-3 for at tilføje flere handlinger.

> [!NOTE]
> Operatoren gælder for alle dimensioner i rækken.

## <a name="description-of-the-dimensions-dialog-box"></a>Beskrivelse af dialogboksen Dimensioner
I følgende tabel beskrives felterne i dialogboksen **Dimensioner**.

| Vare                | Beskrivelse                                                                                                                                                                                                                                                                                             |
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Enkelt dimension eller interval | I feltet **Fra** skal du angive navnet på en konto eller klikke på knappen **Gennemse** ![Gennemse](https://i-technet.sec.s-msft.com/dynimg/IC679490.gif "Gennemse") for at søge efter kontoen. Hvis du vil vælge et interval, skal du søge efter en værdi i feltet **Til**.                                             |
| Dimensionsværdisæt | Angiv navnet på dimensionsværdisættet i feltet **Navn**. Hvis du vil oprette, redigere, kopiere eller slette e sæt, skal du klikke på **Administrer dimensionsværdisæt**. Feltet **Formel** udfyldes med formlen fra cellen **Link til økonomiske dimensioner** for dette dimensionsværdisæt i rækkedefinitionen. |
| Samlekonti   | I feltet **Navn** skal du indtaste eller søge efter en dimension af samlekonti. Feltet **Formel** udfyldes med formlen i cellen **Link til økonomiske dimensioner** for denne samlekonto i rapportdefinitionen.                                                                       |

## <a name="add-dimension-value-sets-in-a-row-definition"></a>Tilføje dimensionsværdisæt i en rækkedefinition
Et dimensionsværdisæt er en navngivet gruppe af dimensionsværdier. Et dimensionsværdisæt kan udelukkende indeholde værdier i en enkelt dimension, men du kan bruge et dimensionsværdisæt i flere rækkedefinitioner, kolonnedefinitioner, rapporteringstrædefinitioner og rapportdefinitioner. Du kan også kombinere dimensionsværdisæt i en rapportdefinition. Når en ændring af de økonomiske data kræver, at du ændrer dimensionsværdisættet, kan du opdatere definitionen af dimensionsværdisættet, og denne opdatering gælder for alle områder, der bruger dimensionsværdisættet. Hvis du for eksempel ofte angiver et interval af værdier, der skal knyttes til de økonomiske data, såsom værdierne fra 5100 til og med 5600, kan du tildele dette interval til et kontosæt med navnet Salg. Når dimensionsværdigruppen er oprettet, kan du vælge sættet som et link til de økonomiske data. I et andet eksempel, hvor et værdiområde fra 5100 til og med 5600 er tildelt Salg, og tildelt 4175 er tildelt Rabatter, kan du beregne det samlede salg ved at trække Rabatter fra Salg, som i (5100:5600)-4175. Denne handling er angivet som **(5100:5600)-4175**.

### <a name="create-a-set-of-dimension-values"></a>Oprette et dimensionsværdisæt

1.  Åbn den række-, kolonne- eller trædefinition, der skal ændres, i Report Designer.
2.  Klik på **Administrer dimensionsværdisæt** i menuen **Rediger**.
3.  I dialogboksen **Administrere dimensionsværdisæt** i feltet **Dimension** skal du vælge den type dimensionsværdisæt, der skal oprettes, og derefter klikke på **Ny**.
4.  Angiv et navn og en beskrivelse for sættet i dialogboksen **Ny**.
5.  I kolonnen **Fra** skal du dobbeltklikke i en celle.
6.  I dialogboksen **Konto** skal du vælge kontonavnet på listen eller søge efter posten i feltet **Søg**. Klik derefter på **OK**.
7.  Gentag trin 5 til 6 i kolonnen **Til** for at designe en formel for denne operator.
8.  Når formlen er fuldført, skal du klikke på **OK**.
9.  Klik på **Luk** i dialogboksen **Administrer dimensionsgrupper**.

### <a name="update-a-set-of-dimension-values"></a>Opdatere en gruppe af dimensionsværdier

1.  Åbn den række-, kolonne- og trædefinition, der skal redigeres, i Rapportdesigner.
2.  Klik på **Administrer dimensionsværdisæt** i menuen **Rediger**.
3.  I dialogboksen **Administrer dimensionsværdisæt** i feltet **Dimension** skal du vælge en dimensionstype.
4.  Vælg det dimensionsværdisæt, der skal opdateres, på listen, og klik derefter på **Rediger**.
5.  I dialogboksen **Rediger** skal du redigere de formelværdier, der skal medtages i sættet. 
    > [!NOTE]
    >  Hvis du tilføjer nye konti eller dimensioner, skal du sørge for at redigere de eksisterende dimensionsværdisæt, så ændringerne implementeres.
6.  Dobbeltklik på cellen, og vælg den relevante operator, **Fra** konto og **Til** konto.
7.  Klik på **OK** for at lukke dialogboksen **Rediger** og gemme ændringerne.

### <a name="copy-a-dimension-set"></a>Kopiere et dimensionssæt

1.  Åbn den række-, kolonne- eller trædefinition, der skal ændres, i Report Designer.
2.  Klik på **Administrer dimensionsværdisæt** i menuen **Rediger**.
3.  I dialogboksen **Administrer dimensionsværdisæt** i feltet **Dimension** skal du vælge en dimensionstype.
4.  Vælg det sæt, der skal kopieres, på listen, og klik derefter på **Gem som**.
5.  Angiv et nyt navn for det kopierede sæt, og klik derefter på **OK**.

### <a name="delete-a-dimension-set"></a>Slette en dimensionsgruppe

1.  Åbn den række-, kolonne- og trædefinition, der skal redigeres, i Rapportdesigner.
2.  Klik på **Administrer dimensionsværdisæt** i menuen **Rediger**.
3.  I dialogboksen **Administrer dimensionsværdisæt** i feltet **Dimension** skal du vælge en dimensionstype.
4.  Markér det sæt, der skal slettes, og klik derefter på **Slet**. Klik på **Ja** for at slette dimensionsværdisættet permanent.


<a name="see-also"></a>Se også
--------

[Økonomirapportering](financial-reporting-intro.md)




