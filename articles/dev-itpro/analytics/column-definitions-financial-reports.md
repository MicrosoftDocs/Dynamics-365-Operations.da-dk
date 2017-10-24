---
title: "Kolonnedefinitioner i økonomirapporter"
description: "Denne artikel indeholder oplysninger om kolonnedefinitioner. En kolonnedefinition er en rapportkomponent eller byggesten, der definerer indholdet af kolonnerne i en rapport. Ligesom rækkedefinitioner kan grundlæggende kolonnedefinitioner bruges til flere rapporter."
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
ms.custom: 106601
ms.assetid: 66e72a48-edab-4e9d-815f-596a1623c258
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 924177f4974358d2283dfd46306d663c27ccd87b
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="column-definitions-in-financial-reports"></a>Kolonnedefinitioner i økonomirapporter

[!include[banner](../includes/banner.md)]


Denne artikel indeholder oplysninger om kolonnedefinitioner. En kolonnedefinition er en rapportkomponent eller byggesten, der definerer indholdet af kolonnerne i en rapport. Ligesom rækkedefinitioner kan grundlæggende kolonnedefinitioner bruges til flere rapporter.

<a name="create-and-modify-a-column-definition"></a>Oprette og redigere en kolonnedefinition
-------------------------------------

En kolonnedefinition kan indeholde 2-255 kolonner.

### <a name="create-a-column-definition"></a>Oprette en kolonnedefinition

1.  Klik på **Kolonnedefinitioner** i navigationsruden i Report Designer.
2.  Klik på **Ny** i menuen **Filer**, og klik derefter på **Kolonnedefinition**.
3.  Tilføj indholdet af kolonnedefinitionen.

### <a name="open-a-column-definition"></a>Åbne en kolonnedefinition

1.  Klik på **Kolonnedefinitioner** i navigationsruden i Report Designer.
2.  Dobbeltklik på en kolonnedefinition for at åbne den.

### <a name="add-a-column-to-a-column-definition"></a>Føje en kolonne til en kolonnedefinition

1.  Klik på **Kolonnedefinitioner** i Report Designer, og åbn derefter den kolonnedefinition, der skal ændres.
2.  Marker den kolonne, hvor der skal indsættes en ny kolonne.
3.  I menuen **Rediger** skal du klikke på **Indsæt kolonne**. Den nye kolonne vises til venstre for den kolonne, du har markeret.

### <a name="delete-a-column-from-a-column-definition"></a>Slette en kolonne fra en kolonnedefinition

1.  Klik på **Kolonnedefinitioner** i Rapportdesigner, og åbn derefter den rækkedefinition, der skal ændres.
2.  Markér den kolonne, der skal slettes.
3.  Klik på **Slet kolonne** i menuen **Rediger**.

## <a name="contents-of-a-column-definition"></a>Indholdet af en kolonnedefinition
En kolonnedefinition indeholder følgende oplysninger:

-   En kolonne med beskrivelser for rækkedefinitionen
-   Beløbskolonner, der viser data fra de økonomiske data, et Microsoft Excel-regneark eller beregninger, der er baseret på andre data i kolonnedefinitionen
-   Formateringskolonner
-   Attributkolonner

Disse oplysninger vises i følgende områder i kolonnedefinitionen:

-   Kolonnedefinitionens overskriftsområde indeholder den overskrift og formatering, der vises i rapporten. En overskrift kan enten gælde en enkelt kolonne med data, strække sig over flere kolonner eller gælde for kolonner baseret på betingelser. Kolonnedefinitionen kan omfatte så mange kolonneoverskriftsrækker, som du har brug for. **Bemærk:** kolonneoverskrifter gælder for hver datakolonne i rapporten. Rapportoverskrifter gælder for hele rapporten. Du kan definere rapportoverskrifter under fanen **Sidehoveder og sidefødder** i rapportdefinitionen.
-   Kolonnedetaljerækker er rækkerne under overskriftsrækkerne i kolonnedefinitionen. Kolonnedetaljerækker angiver de oplysninger, der skal medtages i rapporten. I følgende tabel vises og beskrives kolonnedetaljerækkerne.

    | Navn på kolonnedetaljerække                                                | Beskrivelse                                                                                            |
    |-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
    | Kolonnetype                                                           | (Påkrævet) Angiv datatypen i kolonnen.                                                     |
    | Bogkode/attributkategori                                          | Angiv oplysninger om økonomiske data for kolonner af typen **FD** og **ATTR**.                       |
    | Regnskabsåret Periode Perioder, der er omfattet                                    | Angiv oplysninger om økonomiske data for kolonner af typen **FD**.                                     |
    | Formel                                                               | Angiv en beregningsformel for kolonner af typen **CALC**.                                        |
    | Kolonnebredde Ekstra mellemrum før Tilsidesæt kolonneformat Udskriftsstyring | Angiv indstillinger for specialformat.                                                                        |
    | Kolonnebegrænsninger                                                   | Begræns data.                                                                                         |
    | Rapporteringsenhed                                                        | Begræns kolonnen, så den kun viser data for den angivne rapporteringsenhed.                      |
    | Visning af valuta Valutafilter                                      | Formater valuta.                                                                                       |
    | Dimensionsfilter                                                      | Angiv et filter for at begrænse data til bestemte rapporteringsenheder for økonomiske data.                           |
    | Attributfilter                                                      | Angiv et filter for at begrænse de økonomiske data.                                                       |
    | Startdato Slutdato                                                   | Begræns de økonomiske data til bestemte datoer.                                                         |
    | Berettigelse                                                         | Venstrejuster, centrer eller højrejuster den beskrivende tekst, der er angivet i rækkedefinitionen. |

## <a name="column-restrictions-in-a-column-definition"></a>Kolonnebegrænsninger i en kolonnedefinition
Du kan bruge kolonnebegrænsninger til at angive, hvordan en kolonnedefinition bruger data eller beregner oplysninger. Du kan også begrænse en rapportkolonne til en bestemt enhed eller bestemte datoer. **Bemærk:** En kode for **Kolonnebegrænsning** tilsidesætter alle uoverensstemmende indstillinger, der er tildelt i rækkedefinitionen.

### <a name="column-restrictions-cell"></a>Cellen Kolonnebegrænsninger

Cellen **Kolonnebegrænsninger** kan indeholde koder, der begrænser eller undertrykker oplysninger, såsom rækkeformatering, detaljer og beløb for den pågældende kolonne.

#### <a name="add-a-column-restriction-in-a-column-definition"></a>Tilføje en kolonnebegrænsning i en kolonnedefinition

1.  Åbn den kolonnedefinition, der skal ændres, i Report Designer.
2.  Dobbeltklik på cellen **Kolonnebegrænsninger** for den kolonne, der skal begrænses.
3.  I dialogboksen **Kolonnebegrænsninger** skal du markere en eller flere koder på listen og derefter klikke på **OK**.

### <a name="column-restriction-codes"></a>Kolonnebegrænsningskoder

I nedenstående tabel beskrives koderne for kolonnebegrænsning.

| Kolonnebegrænsningskode | Beskrivelse                                                                                                                                                                                                                                                                                                                             |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SU                      | Skjul understregning for en kolonne, hvor en kommando til understregning (**---**) eller en kommando til dobbelt understregning (**===**) er angivet i rækkedefinitionen. Du kan for eksempel ikke understrege beløb, der er produceret ved en procentberegning.                                                                        |
| ST                      | Skjul totaler, så kun detaljer vises i kolonnen (for eksempel en statistisk kolonne).                                                                                                                                                                                                                                      |
| SD                      | Skjul detaljer, så kun **TOT**- og **CAL**-rækker (fra rækkedefinitionen) vises i kolonnen.                                                                                                                                                                                                                              |
| DR                      | Begræns beløbene i en **FD**-kolonne til debetbeløb.                                                                                                                                                                                                                                                                              |
| CR                      | Begræns beløbene i en **FD**-kolonne til kreditbeløb.                                                                                                                                                                                                                                                                             |
| ADJ                     | Begræns beløbene i kolonnen til periodens reguleringsbeløb, hvis disse beløb er tilgængelige.                                                                                                                                                                                                                                        |
| XAD                     | Begræns beløbene i kolonnen, så periodens reguleringsbeløb udelades.                                                                                                                                                                                                                                                     |
| PT                      | Begræns beløbene i kolonnen, så kun bogførte transaktioner medtages, hvis disse transaktioner er tilgængelige.                                                                                                                                                                                                                 |
| UPT                     | Begræns beløbene i kolonnen, så kun transaktioner, der ikke er bogført, medtages, hvis disse transaktioner er tilgængelige. **Bemærk:** ikke alle dataudbydere understøtter ikke-bogførte transaktioner. Yderligere oplysninger finder du i [vejledningen i dataintegration](http://go.microsoft.com/fwlink/?LinkID=162565) til Microsoft Dynamics ERP-systemet. |

### <a name="restrict-a-column-to-a-reporting-unit"></a>Begrænse en kolonne til en rapporteringsenhed

1.  Åbn den kolonnedefinition, der skal ændres, i Report Designer.
2.  Dobbeltklik på cellen **Rapporteringsenhed** for den kolonne, der skal begrænses.
3.  I dialogboksen **Valg af rapporteringsenhed** på listen **Rapporteringstræ** skal du vælge et træ.
4.  Udvid eller skjul listen over enheder, vælg en rapporteringsenhed og klik derefter på **OK**.

## <a name="format-column-headers"></a>Formatere kolonneoverskrifter
Du kan tilføje, redigere og slette de overskrifter, der vises øverst i kolonnerne i en rapport. Du kan også konfigurere betingede udbredelseskolonneoverskrifter baseret på feltet **Periode** fra kolonnedefinitioner og feltet **Basisperiode** fra rapportdefinitioner. Med basisperiodefunktionen sparer du tid, når du opretter rullende prognoserapporter.

### <a name="create-and-manage-column-headers"></a>Oprette og administrere kolonneoverskrifter

Du kan bruge dialogboksen **Kolonneoverskrift** til at tilføje, redigere og slette de overskrifter, der vises øverst i kolonnerne i en rapport. I følgende tabel beskrives felterne i dialogboksen **Kolonneoverskrift**.

| Felt                 | Beskrivelse                                                                                                                                                                                                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kolonneoverskriftstekst    | Denne tekst vises i kolonneoverskriften. Du kan skrive tekst direkte i dette felt eller klikke på **Indsæt autotekst** for at vælge en indstilling, der opdaterer kolonneoverskriften, hver gang rapporten genereres. Hvis du vil medtage flere autotekstkoder, skal du klikke på **Indsæt autotekst** igen og derefter klikke på en anden kode på listen. |
| Formateringsindstillinger        | Anvend formatering for en kolonneoverskrift, f.eks. en boks eller understregning.                                                                                                                                                                                                                                                           |
| Opslag fra opslag til | Angiv den eller de kolonner, som overskriftsteksten vedrører.                                                                                                                                                                                                                                                            |
| Berettigelse         | Angiv, hvordan kolonneoverskriftsteksten skal justeres for den kolonne eller den række kolonner, der er angivet i felterne **Opslag fra** og **Opslag**.                                                                                                                                                               |

### <a name="create-a-column-header"></a>Oprette en kolonneoverskrift

1.  Åbn den kolonnedefinition, der skal ændres, i Report Designer.
2.  Dobbeltklik på en overskriftscelle.
3.  I dialogboksen **kolonneoverskrift** skal du indtaste kolonneoverskriftsteksten. Du kan også klikke på **Indsæt autotekst** og vælge en indstilling.
4.  I feltet **Formateringsindstillinger** skal du vælge et format til overskriften.
5.  I feltet **Opslag fra** skal du angive bogstavet for den kolonne, hvor kolonneoverskriften skal starte fra. I feltet **Opslag til** skal du angive bogstavet for den kolonne, hvor kolonneoverskriften skal slutte.
6.  Under **Justering** skal du vælge, om kolonneoverskriftsteksten skal være venstrejusteret, centreret eller højrejusteret.
7.  Klik på **OK**.

### <a name="add-a-column-header-row"></a>Tilføje en kolonneoverskriftsrække

1.  Åbn den kolonnedefinition, der skal ændres, i Report Designer.
2.  Marker en celle i overskriftsrækken.
3.  I menuen **Rediger** skal du klikke på **Indsæt række**. Den nye række indsættes over den række, du valgte i trin 2. **Bemærk!** Hvis du har fire eller flere rækker i rapporthoveder i en rapport, hvor hovederne overlapper, når rapporten udlæses til et Excel-regneark. Hvis du vil vise alle overskrifter i rapporten, skal du øge den øverste margen i rapportdefinitionen.

### <a name="delete-a-column-header-row"></a>Slette en kolonneoverskriftsrække

1.  Åbn den kolonnedefinition, der skal ændres, i Report Designer.
2.  Marker den celle, der skal slettes, i overskriftsrækken.
3.  I menuen **Rediger** skal du klikke på **Slet række**.

### <a name="create-an-automatically-generated-header"></a>Opret en automatisk genereret overskrift

Rapportdesigner kan generere kolonnehoveder automatisk ud fra autotekstkoder. Autotekstkoder er variabler, der opdateres, hver gang der genereres en rapport. Alle kolonneoverskrifter kan indeholde disse koder for at angive rapportoplysninger, som kan variere, f.eks datoer eller perioder tal. Du kan derfor bruge en kolonnedefinitionen til flere rapportdefinitioner, tidsperioder og rapporteringstræer. Da autotekstkoder afhænger af kalenderoplysningerne fra detaljerækkerne i kolonnedefinitionen, understøttes de kun for kolonnerne **CALC**, **FD** og **WKS**. Den måde, en autotekstkode vises på i kolonneoverskriftscellen, påvirker, hvordan oplysningerne vises i rapporten. I dialogboksen **kolonneoverskrift** vises autotekstkoder i forskellige situationer. Derfor vises teksten i forskellige situationer i rapporten. I et standardkalenderår oversætter **@CalMonthLong** for eksempel måned **7** til **juli**. Hvis navnet på måneden skal skrives med store bogstaver (for eksempel **JULI**), skal autotekstkoden skrives med store bogstaver i feltet **Kolonneoverskriftstekst**. Du kan f.eks. skrive **@CALMONTHLONG**. Du kan blande koder og tekst. Du skriver for eksempel følgende sidehovedtekst: **Periode @FiscalPeriod-@FiscalYear fra @StartDate til @EndDate**. Den rapportoverskrift, der genereres, ligner følgende tekst: **Periode 1-02 fra 01-01-02 til 01-31-02**. **Bemærk!** Formatet for noget af teksten, f.eks. den lange dato, afhænger af dine internationale indstillinger på Finance and Operations-serveren. Hvis du vil ændre disse indstillinger, skal du klikke på knappen **Start**, klikke på **Kontrolpanel** og derefter klikke på **Område og sprog**. I følgende tabel vises de tilgængelige indstillinger for autotekst til kolonneoverskrifter.

| Indstilling og kode for autotekst                | Betegnelse                                                                                                                                                                                                                                                                                      |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Navn på måned (@CalMonthLong)              | Udskriv navnet på den aktuelle måned i kolonneoverskriften. Hvis du beslutter dig for at afrunde beløbene i rapporten til tusinder, millioner eller milliarder, eller hvis du angiver kolonnebredden i rapporten til færre end ni tegn, forkortes månedens navn til de første tre tegn. |
| Forkortet månedsnavn (@CalMonthShort) | Udskriv det forkortede navn for måneden for den valgte regnskabsperiode.                                                                                                                                                                                                                          |
| Periodenummer (@FiscalPeriod)           | Udskriv det numeriske format for den regnskabsperiode, der er angivet for den pågældende kolonne. Hvis kolonnen strækker sig over flere perioder, udskrives den sidste periode i intervallet.                                                                                                                                   |
| Beskrivelse af perioden (@FiscalPeriodName)  | Udskriv den beskrivelse af regnskabsperioden, der er angivet i de økonomiske data.                                                                                                                                                                                                                    |
| Regnskabsår (@FiscalYear)               | Udskriv regnskabsåret for kolonnen i numerisk format.                                                                                                                                                                                                                                            |
| Kalenderår (@CalYear)                | Udskriv kalenderåret for kolonnen i numerisk format.                                                                                                                                                                                                                                          |
| Startdato (@StartDate)                 | Udskriv startdatoen for kolonnen.                                                                                                                                                                                                                                                             |
| Slutdato (@EndDate)                     | Udskriv slutdatoen for kolonnen.                                                                                                                                                                                                                                                               |
| Enhedsnavn fra træ (@UnitName)         | Hvis du begrænser en kolonne til en bestemt enhed af rapporteringstræet, kan du udskrive enhedsnavnet i kolonneoverskriften.                                                                                                                                                                                     |
| Enhedsbeskrivelse (@UnitDesc)            | Hvis du begrænser en kolonne til en bestemt enhed af rapporteringstræet, kan du udskrive beskrivelsen af enheden i kolonneoverskriften.                                                                                                                                                                              |
| Bogkode (@BookCode)                   | Udskriv den bogkode, der er angivet i kolonnen.                                                                                                                                                                                                                                             |
| Tom linje (@Blank)                     | Indsæt en tom linje i kolonneoverskriften.                                                                                                                                                                                                                                                       |

### <a name="create-a-conditional-spanning-header"></a>Oprette et betinget udbredelseshoved

Betingede udbredelseshovedet spænder over flere kolonner, der er baseret på data for bestemte periode. Hvis du har en budgetrapport for regnskabsåret og ønsker at få vist de faktiske budgetter af forgangne måneder sammen med de forventede budgetter for de kommende måneder, kan du for eksempel bruge et betinget udbredelseshoved til at opdatere rapporthovedet automatisk. Vær opmærksom på følgende situationer, når du opretter en betinget spanning-overskrift:

-   Alle stopbetingelser (feltet **Opslag til**), der er afstemt før startbetingelsen (feltet **Opslag fra**) ignoreres. Eksempelvis har kolonne B defineret opslagsbetingelsen som BASE+ 1 til BASE, BASE er i kolonne C, og BASE+ 1 er i kolonne D. I dette tilfælde ignoreres stopbetingelsen i kolonne C, og udskrivningen af overskriften i kolonne D.
-   Hvis du angiver kolonneoverskrifter, der overlapper hinanden, overlapper de, når de udskrives på rapporten. Rapporten genereres, men følgende advarsel vises i feltet **Status for rapportkø** felt: "Kolonneoverskrifter, der anvender Base, overlapper andre kolonneoverskrifter og kan forårsage overlappende tekst". For eksempel er overskriftsdefinitionen på kolonne B B til BASE+1, og overskriftsdefinitionen i kolonne D er BASE+1 til F. I dette tilfælde udskrives overskrifter oven på hinanden og er ulæselige. Når BASE bruges i en definition af typen **Opslag fra/opslag til**, skal du sørge for at få vist den rapport, der er genereret, for at se, om overskrifterne overlapper hinanden.
-   Hvis du angiver BASE i definitionen af opslag i en kolonne, der ikke udskrives (**NP**), ignoreret det, uanset hvad der er defineret i kolonnedefinitionen. Dette scenario svarer i praksis til ikke at oprette en kolonneoverskriftsdefinition.
-   For betingede udskrivningskolonner (**P &lt; B**, **P &gt; = B**) opfører betingede udbredelseshoveder sig som almindelige kolonneoverskriftsdefinitioner. Hvis betingelsen for eksempel er falsk, starter alle efterfølgende kolonner, der matcher udbredelsesbetingelsen, udskrivningen af overskriften.

#### <a name="create-a-conditional-spanning-header"></a>Oprette et betinget udbredelseshoved

1.  Åbn den kolonnedefinition, der skal ændres, i Report Designer.
2.  Dobbeltklik på en overskriftscelle.
3.  I dialogboksen **kolonneoverskrift** skal du indtaste kolonneoverskriftsteksten. Du kan også klikke på **Indsæt autotekst** og vælge en indstilling.
4.   I feltet **Formateringsindstillinger** skal du vælge en formateringstypografi til overskriften.
5.  Angiv en periode i forhold til den basisperiode, der angives, når rapporten oprettes. I felterne **Opslag fra** og **Opslag til** skal du angive en af følgende værdier: **BASE**, **BASE-X** eller **BASE+X**, hvor X er antallet af perioder fra basisperioden. Hvis du for eksempel angiver **BASE** i feltet **Opslag fra**, starter overskriftsteksten i den betingede udbredelseskolonne i kolonneoverskriften, hvor rapportdefinitionens værdi **Basisperiode** svarer til kolonnedefinitionens værdi **BASE**. Den slutter i den kolonne, der er angivet i feltet **Opslag til**. Hvis opslaget er BASE til M, og rapportdefinitionens værdi for **Basisperiode** er **4**, starter overskriften i den kolonne, hvor perioden er angivet til **4**, og den slutter i kolonne M. Sidehoveder stopper og starter kun på udskrivningskolonner.
6.  Under **Justering** skal du vælge, om kolonneoverskriftsteksten skal være venstrejusteret, centreret eller højrejusteret.
7.  Klik på **OK**.

#### <a name="example-of-a-conditional-spanning-header"></a>Eksempel på et betinget udbredelseshoved

Karina opretter en rapport til et dynamisk halvårligt budget. Hun vil have ordet "Faktisk" udskrevet over de kolonner, der indeholder faktiske data, og ordet "Budget" udskrevet over de kolonner, der indeholder budgetprognoser. Hver måned, hvor rapporten køres, er der én mere faktisk kolonne og én mindre budgetkolonne. Selvom Karina kan ændre kolonnedefinitionen manuelt, hver gang rapporten genereres, for at justere overskrifterne, beslutter hun for at spare tid og kræfter at oprette betingede udbredelseshoveder, der automatisk opretter overskrifter over de relevante kolonner, hver gang rapporten køres. Karina åbner Report Designer, klikker på **Kolonnedefinition** i navigationsruden og åbner kolonnedefinitionen for rapporten. Derefter indtaster hun følgende oplysninger. Basisperioden i rapportdefinitionen er 4.

|                     | A    | B             | K             | D             | E             | F             | G             | H             | I             | J             | K             | L             | M             |
|---------------------|------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|
| Overskrift 1            |      | Realiseret        | Budget        |               |               |               |               |               |               |               |               |               |               |
| Overskrift 2            |      | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong |
| Overskrift 3            |      |               |               |               |               |               |               |               |               |               |               |               |               |
| Kolonnetype         | DESC | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            |
| Bogkode/attribut |      | FAKTISK        | BUDGET2012    | FAKTISK        | BUDGET2012    | FAKTISK        | BUDGET2012    | FAKTISK        | BUDGET2012    | FAKTISK        | BUDGET2012    | FAKTISK        | BUDGET2012    |
| Regnskabsår         |      | BASE          | BASE          | BASE          | BASE          | BASE          | BASE          | BASE          | BASE          | BASE          | BASE          | BASE          | BASE          |
| Periode              |      | 1             | 1             | 2             | 2             | 3             | 3             | 4             | 4             | 5             | 5             | 6             | 6             |
| Dækningsperioder     |      | PERIODIC      | PERIODIC      | PERIODIC      | PERIODIC      | PERIODIC      | PERIODIC      | PERIODIC      | PERIODIC      | PERIODIC      | PERIODIC      | PERIODIC      | PERIODIC      |
| Kolonnebredde        | 30   | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            |
| Udskriftsstyring       |      | P &lt; = B       | P &gt; B        | P &lt; = B       | P &gt; B        | P &lt; = B       | P &gt; B        | P &lt; = B       | P &gt; B        | P &lt; = B       | P &gt; B        | P &lt; = B       | P &gt; B        |

Karina dobbeltklikker på en kolonneoverskriftscelle for at åbne dialogboksen **Kolonneoverskrift**, hvor hun skriver følgende oplysninger.

| Felt              | Værdi                 |
|--------------------|-----------------------|
| Kolonneoverskriftstekst | Faktisk                |
| Indsæt autotekst    | Der er ikke foretaget et valg. |
| Formateringsindstillinger     | Felt                   |
| Berettigelse      | Der er ikke foretaget et valg. |
| Opslag fra        | B                     |
| Opslag til          | BASE                  |
| Budgetoverskrift      | BASE+1 til slutkolonne  |

Når Karina er færdig med at indtaste oplysninger, klikker hun på **OK**. Derefter dobbeltklikker hun på kolonneoverskriftscellen i kolonne C for at åbne dialogboksen **Kolonneoverskrift**, hvor hun skriver følgende oplysninger.

| Felt              | Værdi                 |
|--------------------|-----------------------|
| Kolonneoverskriftstekst | Budget                |
| Indsæt autotekst    | Der er ikke foretaget et valg. |
| Formateringsindstillinger     | Felt                   |
| Berettigelse      | Der er ikke foretaget et valg. |
| Opslag fra        | C                     |
| Opslag til          | BASE+2                |

Hver gang denne rapport genereres, udskrives ordet "Faktisk" over de kolonner, der indeholder faktiske data, og ordet "Budget" udskrives over de kolonner, der indeholder budgetprognoser. Desuden justeres antallet af kolonner hver måned.

## <a name="apply-column-justification"></a>Anvend kolonnejustering
Cellen **Justering** bruges til at anvende ændret formatering for en beskrivelseskolonne i en rapport. Denne indstilling påvirker kun kolonnebeskrivelser, ikke de faktiske værdier.

1.  Åbn den kolonnedefinition, der skal ændres, i Report Designer.
2.  Dobbeltklik på cellen **Justering**.
3.  Vælg en af følgende værdier på listen:
    -   **Ingen** – der udføres ikke justeringer.
    -   **Venstre** – kolonnebeskrivelser venstrejusteres.
    -   **Center** – kolonnebeskrivelser centreres.
    -   **Højre** – kolonnebeskrivelser højrejusteres.

## <a name="add-special-formatting-options"></a>Tilføje specielle formateringsindstillinger
I kolonnedefinitionen anvender formateringskolonnedetaljerækkerne specialformatering for markerede kolonner. Selvom nogle af indstillingerne for **Udskriftsstyring** og **Kolonnebegrænsninger** er specifikke for **FD**-kolonner, gælder de fleste af indstillingerne for alle kolonnetyper. Den formatering, der er angivet i kolonnedefinitionen, tilsidesætter den formatering, der er angivet i rapportdefinitionen. Den formatering, der er angivet i rækkedefinitionen, tilsidesætter imidlertid den formatering, der er angivet i kolonnedefinitionen. Følgende rækker anses for at være formateringsrækker.

-   Kolonnebredde
-   Ekstra mellemrum før kolonne
-   Tilsidesættelse af format/valuta
-   Udskriftsstyring

### <a name="changing-the-column-width"></a>Ændre kolonnebredden

Cellen **Kolonnebredde** angiver antallet af tegn, der skal bruges til bredden af kolonnen i den udskrevne rapport. Kolonnebredden er vigtig for kolonner, som indeholder beløb (kolonner af typen **CALC**, **WKS** eller **FD**), beskrivelser (kolonner med den **DESC** type) eller fyld (kolonner af typen **FILL**). Indstillingen **Autotilpas** er som standard valgt, så bredden af hver kolonne justeres automatisk, så den passer til indholdet.

#### <a name="specify-the-width-of-a-column-on-a-report"></a>Angiv bredden på en kolonne i en rapport

1.  Åbn den kolonnedefinition, der skal ændres, i Report Designer.
2.  I cellen **Kolonnebredde** skal du angive antallet af mellemrum for bredden af kolonnen. Den maksimale bredde på en kolonne er 255 tegn (dette tal inkluderer procenttegn, kommaer og parenteser). Alternativt kan du aktivere rapportdesigneren for at vælge den rette bredde på kolonnen ud fra cellens indhold ved at dobbeltklikke på cellen **Kolonnebredde** og derefter klikke på **Autotilpas**.

### <a name="add-space-between-columns"></a>Tilføje afstand mellem kolonner

Cellen **Ekstra mellemrum før kolonne** angiver bredden af separatoren mellem én kolonne og tilgrænsende kolonner i kolonnedefinitionen. Indstillingen **Ekstra mellemrum før kolonne** påvirker alle detaljerækkerne for kolonnen men ikke kolonneoverskriftsrækkerne. Brug denne indstilling til at adskille grupper af kolonner eller til at tilføje nogle få mellemrum før beskrivelsen, så beskrivelseskolonnen indrykkes fra de venstrejusterede titler i rapporten. Standardantallet af mellemrum mellem hver kolonne er to. Du kan ændre denne indstilling på fanen **Indstillinger** i rapportdefinitionen.

#### <a name="specify-the-space-between-columns"></a>Angive afstanden mellem kolonner

1.  Åbn den kolonnedefinition, der skal ændres, i Report Designer.
2.  I cellen **Ekstra mellemrum før kolonne** skal du angive det antal mellemrum, der skal indsættes mellem kolonner.

### <a name="specify-a-currency"></a>Angiv en valuta

Cellen **Tilsidesættelse af format/valuta** angiver formateringen af decimal, valuta og procentbeløb i kolonnen. Denne formatering tilsidesætter formatering, der er angivet i rapportdefinitionen eller systemets standardindstillinger.

#### <a name="assign-a-format-currency-override-to-a-report-column"></a>Tildele en tilsidesættelse af format/valuta til en rapportkolonne

1.  Åbn den kolonnedefinition, der skal redigeres, i Rapportdesigner.
2.  Dobbeltklik på en celle af typen **Tilsidesættelse af format/valuta** i en beløbskolonne.
3.  Vælg formateringsindstillinger i dialogboksen **Tilsidesættelse af format**.

### <a name="add-a-print-control-code"></a>Tilføje en kode til udskriftstyring

Cellen **Udskriftsstyring** kan indeholde koder, der justerer visnings- eller udskriftsindstillingerne for en kolonne. Der findes to typer koder til udskriftsstyring: almindelige koder til udskriftsstyring og betingede koder til udskriftsstyring.

#### <a name="regular-print-control-codes"></a>Almindelige koder til udskriftsstyring

| Kode til udskriftstyring | Oversættelse                                     | Beskrivelse                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NP                 | Ingen udskrivning                                     | Beløbene i denne kolonne medtages ikke i beregninger og i rapporter, der udskrives. Hvis du vil medtage en kolonne, der ikke udskrives, i en beregning, skal du henvise direkte til kolonnen i formlen til beregning. Kolonnen C, der ikke udskrives, er for eksempel medtaget i følgende beregning: **B + C + D**. Derimod er kolonnen C, der ikke udskrives, ikke medtaget i følgende beregning: **B:D**.                                                                                                                                          |
| XCR                | Skift fortegn, hvis den typiske saldo for en række er et kreditbeløb | Opret et budget eller en sammenlignende rapport, hvor alle negative afvigelser (f.eks. en manko i omsætningen eller en overskridelse af en udgift) altid er negative. Anvend denne kode til en **CALC**-kolonne for at vende fortegnet på Kolonnebeløbet, hvis den normale saldo for en given række er et kreditbeløb (som angivet ved hjælp af et **C** i kolonnen **Normal saldo** i rækkedefinitionen). **Bemærk:** For **TOT**-rækker og **CAL**-rækker, der typisk har en kreditsaldo, skal du sørge for at angive et **C** i kolonnen **Normal saldo** i rækkedefinitionen. |
| X0                 | Skjul kolonne, hvis den kun indeholder nulværdier eller tomme værdier          | Medtag ikke en **FD**-kolonne i rapporten, hvis alle cellerne i denne kolonne enten er tomme eller indeholder nulværdiler.                                                                                                                                                                                                                                                                                                                                                                                                                             |
| SR                 | Undertryk afrunding                               | Undgå, at beløbene i denne kolonne bliver afrundet.                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| XR                 | Undertryk akkumulering                                 | Undertryk en akkumulering. Hvis rapporten bruger et rapporteringstræ, akkumuleres beløbene i denne kolonne ikke til efterfølgende overordnede noder.                                                                                                                                                                                                                                                                                                                                                                                                   |
| RP                 | Gentag kolonne på hver side                      | Gentag en bestemt kolonne på hver side i en rapport. Du kan for eksempel bruge koden **RP** for udskriftsstyring til at medtage en kolonne af typen **ROW**, der henter rækkekoder ind på hver side.                                                                                                                                                                                                                                                                                                                                           |
| WT                 |  Ombryd tekst                                      |  Hvis teksten i en kolonne er for lang til at kunne være på den tilgængelige plads, kan du ombryde teksten for at beholde hele teksten i kolonnen.                                                                                                                                                                                                                                                                                                                                                                                                                            |

#### <a name="conditional-print-control-codes"></a>Betingede koder til udskriftsstyring

| Betinget kode til udskriftsstyring | Betegnelse                                                                             |
|--------------------------------|-----------------------------------------------------------------------------------------|
| (ingen)                         | Fjern valget af betinget udskrivning.                                                  |
| P &lt; B                         | Få kun vist en bestemt kolonne, hvis perioden er mindre end basisperioden.             |
| P &gt; B                         | Få kun vist en bestemt kolonne, hvis perioden er længere end basisperioden.             |
| P=B                            | Få kun vist en bestemt kolonne, hvis perioden er lig med basisperioden.              |
| P &lt; = B                        | Få kun vist en bestemt kolonne, hvis perioden er kortere end eller lig med basisperioden. |
| P &gt; = B                        | Få kun vist en bestemt kolonne, hvis perioden er længere end eller lig med basisperioden. |

#### <a name="add-print-control-codes-to-a-report-column"></a>Tilføje koder til udskriftsstyring til en rapportkolonne

1.  Åbn den kolonnedefinition, der skal redigeres, i Rapportdesigner.
2.  Dobbeltklik på cellen **Udskriftsstyring**.
3.  I dialogboksen **Udskriftsstyring** skal du vælge en kode på listen **Angiv indstillinger for udskriftsstyring**. Hvis du vil markere mere end én kode, skal du holde Ctrl-tasten nede, mens du markerer koderne.
4.  Vælg en indstilling i feltet **Betingede udskriftsindstillinger**. **(ingen)** er valgt som standard. Du kan kun vælge én betinget udskriftskode ad gangen.
5.  Klik på **OK**.

> [!TIP]
> Du kan også angive udskriftskoderne direkte i cellen **Udskriftsstyring**. Adskil flere udskriftsstyringskoder med et komma.


## <a name="column-types"></a>Kolonnetyper
Typen af oplysninger, som hver kolonne i en rapport indeholder, er angivet med værdien i rækken **Kolonnetype** i kolonnedefinitionen. Hver kolonnedefinition skal indeholde mindst én beskrivelseskolonne (**DESC**) og én beløbskolonne (**FD**, **WKS** eller **CALC**). **Bemærk:** kolonnetypekoderne gælder ikke for alle regnskabssystemer. Hvis du vælger en type, der ikke er gyldig for dit regnskabssystem, er denne kolonne tom i rapporten.

### <a name="specify-a-column-type"></a>Angive en kolonnetype

1.  Åbn den kolonnedefinition, der skal ændres, i Report Designer.
2.  I den relevante kolonne skal du dobbeltklikke på en celle i rækken **Kolonnetype**.
3.  Vælg en kolonnetype på listen. Følgende tabel beskriver de forskellige kolonnetyper.
    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Kolonnetypekode</th>
    <th>Beskrivelse</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>FD</td>
    <td>Vis økonomiske data eller data fra et Excel-regneark, når du bruger en kolonne af typen <strong>Link til økonomiske dimensioner</strong> eller typen <strong>Link til regneark</strong> i rækkedefinitionen. Når du vælger kolonnetypen <strong>FD</strong>, angives standardindstillinger automatisk i følgende rækker: <ul>
    <li><strong>Bogkode/attributkategori</strong> FAKTISK</li>
    <li><strong>Bogkode/attributkategori</strong> FAKTISK</li>
    <li><strong>Regnskabsår:</strong> BASE</li>
    <li><strong>Periode:</strong> BASE</li>
    <li><strong>Dækningsperioder:</strong> PERIODIC</li>
    <li><strong>Kolonnebredde</strong> 14</li>
    </ul>
Du kan ændre disse standardindstillinger.</td>
    </tr>
    <tr class="even">
    <td>CALC</td>
    <td>Få vist resultatet af en enkel eller kompleks beregning, der er angivet i cellen <strong>Formel</strong>. Yderligere oplysninger finder du under <a href="advanced-formatting-options-financial-reporting.md">Avancerede formateringsindstillinger i økonomirapportering</a>.</td>
    </tr>
    <tr class="odd">
    <td>DESC</td>
    <td>Få vist rækkebeskrivelsen fra rækkedefinitionen. Selvom beskrivelseskolonnen ofte er den første kolonne i rapporten, kan den være placeret et hvilket som helst sted.</td>
    </tr>
    <tr class="even">
    <td>ROW</td>
    <td>Få vist de enkelte rækkekoder for økonomiske rækker fra kolonnen <strong>Rækkekode</strong> i rækkedefinitionen. Yderligere oplysninger finder du under <a href="row-definitions-financial-reporting.md">Rækkedefinitioner i økonomirapportering</a>.</td>
    </tr>
    <tr class="odd">
    <td>ACCT (kontokoder)</td>
    <td>Få vist de segmentværdier eller dimensionsværdier for økonomiske data, der gælder for hver række. For konto- og transaktionsdetaljerapporter udskrives den fuldt kvalificerede konto (f.eks. <strong>110140-070-0101</strong>). Hvis der er angivet områder i kolonnen <strong>Link til økonomiske dimensioner</strong>, i en tilknyttet rækkedefinition, står området i kantede parenteser og behandles, som om de var én værdi (f.eks. <strong>[110140:110700]-070-[0101:0200]</strong>). For økonomiske rapporter og rapporter på højt niveau, der er en kombination af flere konti, udskrives linket til de økonomiske data fra rækkedefinitionen (f.eks. <strong>1100:1200</strong>).</td>
    </tr>
    <tr class="even">
    <td>FILL</td>
    <td>Udfyld cellen med et tegn, som er omgivet af enkelt anførselstegn. Hvis du ikke indtaster et tegn, er kolonnen tom. Hvis du for eksempel til udfylde en kolonne med en ellipse (...), skal du angive <strong>FILL</strong> <strong>'.'</strong>.</td>
    </tr>
    <tr class="odd">
    <td>PAGE</td>
    <td>Indsæt et lodret sideskift i rapporten. De kolonner, der er til højre for kolonnen <strong>PAGE</strong>, vises på en anden side.</td>
    </tr>
    <tr class="even">
    <td>WKS</td>
    <td>Få vist data, der er hentet fra et Excel-regneark. Når du vælger kolonnetypen <strong>WKS</strong>, angives standardindstillinger automatisk i følgende rækker: <ul>
    <li><strong>Regnskabsår:</strong> PERIODIC</li>
    <li><strong>Periode:</strong> BASE</li>
    </ul>
Du kan ændre disse standardindstillinger.</td>
    </tr>
    <tr class="odd">
    <td>ATTR</td>
    <td>Hvis dit regnskabssystem understøtter attributter, vises en konto- eller transaktionsattribut i kolonnen. En attribut, som skal gælde for en enkelt fuld konto, udtrækker underliggende konto- eller transaktionsoplysninger fra de økonomiske data. Attributter på kontoniveau viser data fra de attributvisningsdata på konto- og transaktionsniveau, der forekom på det tidspunkt, hvor transaktionen blev bogført. Hvis du vælger <strong>ATTR</strong> som kolonnetype, skal du angive attributkategorien i kolonnedefinitionens detaljerække <strong>Bogkode/attributkategori</strong>.</td>
    </tr>
    </tbody>
    </table>

### <a name="financial-dimensions-column"></a>Kolonnen Økonomiske dimensioner

Følgende rækkefefinitioner for **Kolonnedefinition** gælder for kolonner, som har kolonnetypen **FD** (beløb fra økonomiske dimensioner).

#### <a name="book-codeattribute-category-cell"></a>Cellen Bogkode/attributkategori

Cellen **Bogkode/attributkategori** angiver bogkoden for dataene i kolonnen **FD**. En definition af en kolonne kan omfatte flere kolonner med faktiske, budgetterede og statistiske data. En definition af en kolonne kan også vise forskellige perioder, som aktuelt eller år til dato og forskellige beløb. Listen over bogkoder afspejler de faktiske, budgetterede og statistiske (ikke-finansielle) indstillinger, der er fastsat i de økonomiske data.

#### <a name="fiscal-year-cell"></a>Cellen Regnskabsår

Cellen **Regnskabsår** angiver det regnskabsår, som kolonnen skal indeholde. Året kan være relateret til det basisår, der angives, når rapporten oprettes. Følgende indstillinger er tilgængelige.

| Indstilling  | Beskrivelse                                                                                                                  |
|---------|------------------------------------------------------------------------------------------------------------------------------|
| BASE    | Brug det basisår, der er angivet på rapporteringstidspunktet.                                                                          |
| BASE+\# | Brug det år, der er \# år efter basisåret. Hvis du for eksempel vil bruge det tredje år efter basisåret, skal du skrive **BASE+ 3**. |
| BASE-\# | Brug det år, der er \# år før basisåret. Hvis du vil bruge det foregående år, skal du skrive **BASE- 1**.                 |
| \#      | Angiv det aktuelle regnskabsår.                                                                                                |

#### <a name="period-cell"></a>Cellen Periode

Cellen **Periode** angiver de regnskabsperioder, som kolonnen skal indeholde. Perioden kan være relateret til den basisperiode, der angives, når rapporten oprettes. Følgende indstillinger er tilgængelige.

| Indstilling          | Betegnelse                                                                                                                                                                                                                          |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BASE            | Brug basisperioden.                                                                                                                                                                                                                 |
| BASE+\#         | Brug den periode, der er \# perioder efter basisperioden. Hvis du for eksempel vil bruge den tredje periode efter basisperioden, skal du skrive **BASE+ 3**.                                                                                               |
| BASE-\#         | Brug den periode, der er \# perioder før basisperioden. Hvis du vil bruge den foregående periode, skal du skrive **BASE- 1**.                                                                                                                 |
| BASE-\#:BASE    | Brug flere perioder fra flere perioder før basisperioden til og med basisperioden. Hvis du vil bruge de tre foregående perioder og basisperioden, skal du skrive **BASE-3:BASE**.                                                |
| BASE:BASE+\#    | Brug flere perioder fra basisperioden til og med flere perioder efter basisperioden. Hvis du vil for eksempel vil bruge basisperioden og de efterfølgende to perioder, skal du skrive **BASE:BASE+ 2**.                                                  |
| BASE-\#:BASE+\# | Brug flere perioder fra flere perioder før basisperioden til flere perioder efter basisperioden. Hvis du for eksempel vil bruge de tre foregående perioder, basisperioden og de to efterfølgende perioder, skal du skrive **BASE-3:BASE+ 2**. |
| 1:BASE          | Brug flere perioder fra den første periode til og med basisperioden.                                                                                                                                                                 |
| \#              | Brug altid et bestemt periodenummer. Vi anbefaler ikke, at du bruger denne indstilling, fordi den reducerer kolonnedefinitionens fleksibilitet.                                                                                       |
| \#                                      : \#           | Brug altid et bestemt interval af perioder. Vi anbefaler ikke, at du bruger denne indstilling, fordi den reducerer kolonnedefinitionens fleksibilitet.                                                                                    |

Du kan gå ud over regnskabsårets grænser i en periodespecifikation, og du kan blande år i et interval af perioder. Du for eksempel angiver perioder som **BASE-5** (for at repræsentere seneste seks perioder) og kører en rapport, der er basisperioden 2. I dette tilfælde viser rapporten data for de to første perioder i det angivne regnskabsår og de sidste fire perioder i forrige regnskabsår.

### <a name="specify-the-periods-for-an-fd-column"></a>Angive perioderne for en FD-kolonne

1.  Åbn den kolonnedefinition, der skal redigeres, i Rapportdesigner.
2.  I en **FD**-kolonne skal du dobbeltklikke på cellen i rækken **Periode** og derefter vælge en indstilling på listen.
3.  På formellinjen over navigationsruden eller i cellen **Periode** skal du udfylde formlen. Erstat et nummertegn (\#) med den relevante værdi.

#### <a name="periods-covered-cell"></a>Cellen Perioder, der er omfattet

Cellen **Perioder, der er omfattet** angiver det beløb, som kolonnen skal vise. Dette beløb er i forhold til værdien i cellerne **Regnskabsår** og **Periode** for kolonnen. Følgende indstillinger er tilgængelige.

| Indstilling      | Beskrivelse                                                                 |
|-------------|-----------------------------------------------------------------------------|
| PERIODIC    | Få vist summen af aktiviteten for den aktuelle periode eller det aktuelle interval af perioder. |
| PERIODIC/BB | Få vist startsaldoen for den aktuelle periode eller det aktuelle interval af perioder.   |
| YTD         | Få vist summen af aktivitet år til dato.                               |
| YTD/BB      | Få vist startsaldoen for året.                                 |

### <a name="specify-the-periods-that-are-covered-for-an-fd-column"></a>Angive de perioder, der er omfattet for en FD-kolonne

1.  Åbn den kolonnedefinition, der skal ændres, i Report Designer.
2.  I en **FD**-kolonne skal du dobbeltklikke på cellen i rækken **Perioder, der er omfattet** og vælge en indstilling på listen.

### <a name="attribute-filter-in-a-column-definition"></a>Filteret Attribut i en kolonnedefinition

Attributter er økonomiske værdier, kan definerer en konto eller transaktion yderligere. Kontoattributterne omfatter **Aktiv**, **Passiv**, **Indtægt** og **Udgift**. Transaktionsattributterne omfatter **Beskrivelse af transaktionen** og **Dato for udførelse af transaktion**. Understøttelse af attributter kan variere fra et Microsoft Dynamics ERP-system til et andet. Cellen **Attributfilter** begrænser dataene i **FD**-kolonner til bestemte værdier eller intervaller for attributkategorier. Selvom denne funktion kan bruges sammen med en **ATTR**-kolonne, er **ATTR**-kolonne ikke påkrævet. I en **FD**-kolonne er der en grænse på de konti eller transaktioner, som rapporten medtager fra attributfilteret. **Bemærk:** I vejledningen i integration til dit system kan du se, hvilke attributter dit ERP-system understøtter.

#### <a name="apply-an-attribute-filter-for-an-fd-column-on-a-report"></a>Anvende et attributfilter til en FD-kolonne i en rapport

1.  Åbn den kolonnedefinition, der skal ændres, i Report Designer.
2.  Dobbeltklik på cellen **Attributfilter** for en kolonne af typen **FD**.
3.  Dobbeltklik på en celle i kolonnen **Attribut** i dialogboksen **Attributfilter**, og vælg derefter filtertypen.
4.  Du kan yderligere begrænse resultaterne ved at angive et interval i kolonnerne **Fra** og **Til**. Cellen **Fra** skal indeholde en værdi.
5.  Klik på **OK**.

#### <a name="example-of-an-attribute-filter"></a>Eksempel på et attributfilter

Følgende eksempel viser en del af en beskrivelse af kolonne, der har en kontoattribut i rækken **Bogkode/attributkategori**. Attributfilteret for denne kolonne angiver intervallet af værdier, der skal medtages i rapporten.

|                              | T    | B                    |
|------------------------------|------|----------------------|
| Kolonnetype                  | DESC | FD                   |
| Bogkode/attributkategori |      | FAKTISK               |
| Regnskabsår                  |      | BASE                 |
| Periode                       |      | 1:BASE               |
| Dækningsperioder              |      | PERIODIC             |
| ...                          |      |                      |
| Kolonnebredde                 | 30   |                      |
| ...                          |      |                      |
| Attributfilter             |      |  Reference = \[01:10\] |

### <a name="dimension-filter-in-a-column-definition"></a>Filteret Dimension i en kolonnedefinition

Et dimensionsfilter bruges til at begrænse **FD**-kolonnen til bestemte dimensionsværdier. Filteret kan omfatte en enkelt dimension, et interval af dimensioner eller en gruppe af dimensioner. Filteret kan også indeholde dimensionsværdisæt. Eftersom dimensionsværdier kan variere, behøver et ..\økonomiske dimensioner\dimensionsbaseret system ikke at overholde en bestemt længde. Filteret anvendes, uanset om rapporten indeholder et rapporteringstræ. Du kan bruge jokertegn (\* eller ?) i en hvilken som helst placering. Når du angiver flere konti, skal du indsætte et komma mellem firmaer, som i følgende eksempel: +konto=\[1200\], +konto=\[1100\], afdeling=\[01?\] For at modtage alle afdelinger for en bestemt konto du kan udelukke afdelingsdimensionen fra dimensionsfilteret. De to følgende dimensionsfiltre håndteres for eksempel på samme måde:

-   +Konto = \[1100\], Afdeling
-   +Konto = \[1100\]

Du kan også bruge en kombination af alfanumeriske tegn for at opnå et nøjagtigt match, og du kan definere delvise dimensioner. **Placering = \[10\*\]** omfatter for eksempel alle placeringsdimensionsværdier, der begynder med 10.

#### <a name="apply-a-dimension-filter-for-a-column-on-a-report"></a>Anvende et dimensionsfilter for en kolonne i en rapport

1.  Åbn den kolonnedefinition, der skal ændres, i Report Designer.
2.  Dobbeltklik på cellen **Dimensionsfilter** for en **FD**-kolonne.
3.  I dialogboksen **Dimensioner** skal du angive de filtre, som skal anvendes.
4.  Klik på **OK**.

### <a name="format-a-multiple-currency-report-in-a-column-definition"></a>Formatere en rapport med flere valutaer i en kolonnedefinition

En rapport med flere valutaer kan vise beløb i den naturlige (lokale) valuta, den funktionelle (standard) valuta eller rapporteringsvalutaen. En virksomheds funktionelle valuta er defineret i Microsoft Dynamics ERP-systemet. Du må ikke forveksle denne ERP-indstilling med operativsystemets internationale indstillinger, hvor du kan konfigurere de standardvalutasymboler, der bruges i rapporter. De følgende valutarelaterede celler er tilgængelige i kolonnedefinitionen:

-   **Visning af valuta** – Angiv typen af valuta (fysisk, funktionel eller rapportering), som posteringerne vises i. Denne funktion kaldes undertiden valutaomregning. Valutaomregning er muligheden for at rapportere finansbeløb i en valuta, der ikke nødvendigvis er firmaets funktionelle valuta for firmaet eller den valuta, som transaktionen blev angivet i.
-   **Valutafilter** – Angiv et valutafilter. Det er kun transaktioner, der er angivet i den valgte valuta, der vises i rapporten.

> [!NOTE]
> For at oprette rapporter, der benytter flere forskellige valutaer, skal du markere afkrydsningsfeltet **Medtag alle rapporteringsvalutaer** under fanen **Rapport** i rapportdefinitionen. Benyt nedenstående fremgangsmåde for at bestemme en virksomheds funktionelle valuta.

1.  Klik på **Firmaer** i menuen **Firma** i Report Designer.
2.  I dialogboksen **Firmaer** skal du vælge et firma og derefter klikke på **Vis**.
3.  I dialogboksen **Vis firma** kan du under **Internationale indstillinger** få vist den valuta, der er defineret for det valgte firma.

#### <a name="specify-the-currency-on-a-multiple-currency-report"></a>Angiv valutaen i en rapport med flere valutaer

1.  Åbn den kolonnedefinition, der skal ændres, i Report Designer.
2.  Dobbeltklik på cellen **Visning af valuta** i den relevante **FD**-kolonne, og vælg derefter indstillingen for visning af valutaoplysninger: **Naturlig/oprindelig valuta**, **Funktionel valuta fra firmaoplysninger** eller rapporteringsvalutaen.
3.  Dobbeltklik på cellen **Valutafilter** i den relevante **FD**-kolonne, og vælg derefter den relevante valutakode på listen. Det er kun transaktioner, der er angivet i denne valuta, der vises i rapporten.

> [!NOTE]
> De indstillinger, der er beskrevet her, kan variere afhængigt af ERP-systemet. Du kan finde flere oplysninger i [dokumentationen til Microsoft ERP-systemet](https://www.microsoft.com/en-us/download/details.aspx?id=5916).

### <a name="example-for-currency-display-and-currency-filter-cells"></a>Eksempel på cellerne Visning af valuta og Valutafilter

Karina har foretaget følgende valg af valuta i sin definition af kolonne:

-   **Valutafilter:** Yen
-   **Visning af valuta:** Funktionel (USD)

På grund af det valutafilter, Karina har valgt, omfatter rapporten kun transaktioner, der er angivet i japanske yen (JPY). I rapporten vises Transaktionerne i den funktionelle valuta, amerikanske dollar (USD), på grund af den visning af valuta, hun har valgt.

#### <a name="currency-filter-and-currency-display-combinations"></a>Kombinationer af Valutafilter og Visning af valuta

Følgende tabel viser de rapportresultater, der kan forekomme ved forskellige kombinationer af indstillingerne i cellerne **Visning af valuta** og **Valutafilter** på grund af de valg, Karina har foretaget. Den funktionelle valuta er USD.

| Cellen Visning af valuta                        | Cellen Valutafilter | Rapportresultat                                                                                                                                                                                    |
|----------------------------------------------|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Naturlig/oprindelig valuta                 | **YEN**              | **Y6.000** – resultatet viser kun de transaktioner, der er angivet i JPY.                                                                                                                        |
| Funktionel valuta fra virksomhedsoplysninger | **YEN**              | **$60** – resultatet viser kun de transaktioner, der er angivet i JPY og viser disse transaktioner i USD. **Bemærk:** Omregningskursen er ca. 100 JPY pr. USD.                    |
| Funktionel valuta fra virksomhedsoplysninger | Tom                | **$2,310\*\*** – resultatet viser alle data i den funktionelle valuta, der er angivet i firmaoplysningerne. **Bemærk:** dette beløb er summen af alle transaktioner i den funktionelle valuta. |
| Naturlig/oprindelig valuta                 | Tom                | **$2.250** – resultatet viser alle beløb i den valuta, som transaktionen blev udført i.                                                                                                 |

### <a name="calculation-column-in-a-column-definition"></a>Beregningskolonne i en kolonnedefinition

Kolonnetypen **CALC** i en kolonnedefinition understøtter komplekse beregninger i cellen **Formel** og kan indeholde operatorerne **+**, **-**, **\*** og **/** og også **IF/THEN/ELSE** sætninger. En kolonne af typen beregning kan også henvise til en anden kolonne, endda efterfølgende kolonner. Desuden kan en beregningskolonne også omfatte regnskabsåret og -perioden til at understøtte kolonnens overskrifter. Beregningsformlen kan indeholde op til 1.024 alfanumeriske tegn. Hvis du vil udtrykke resultatet i procent, skal du bruge tilsidesættelse for specialformat. **Bemærk:** resultaterne af beregningsformler medtager ikke værdierne i kolonneintervaller, der ikke udskrives. For eksempel udskriver **A:D** **0** (nul), mens **A + B + C** for værdier, der ikke udskrives, beregner værdien.

#### <a name="operators-in-calculation-columns"></a>Operatorer i beregningskolonner

Hvis du vil tilføje, fratrække, gange eller dividere kolonner, skal du angive kolonnebogstaverne i beregningsrækkefølgen og derefter bruge den relevante operator til at adskille de enkelte kolonnebogstaver. I følgende tabel beskrives de operatorer, du kan bruge i en beregningskolonne.

| Operatør | Eksempel på beregning | Betegnelse                                                                                                                                                                                                                                    |
|----------|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| +        | A+C                 | Beløbet i kolonne A lægges sammen med beløbet i kolonne C.                                                                                                                                                                                          |
| :        | A:C A:C-D           | Tilføj et interval af på hinanden følgende kolonner. For eksempel lægger formlen **A:C** summen af kolonnerne A til og med C sammen, og formlen **A:C-D** lægger summen af kolonnerne A til og med C sammen og fratrækker derefter beløbet i kolonne D.                          |
| -        | A-C                 | Beløbet i kolonne A trækkes fra beløbet i kolonne C. **Bemærk:** du kan også bruge minustegnet (-) til at vende tegnene om i en kolonne. Du kan for eksempel bruge **-A+B** til at lægge det negative beløb i kolonne A sammen med beløbet i kolonne B. |
| \*       | A\*C                | Beløbet i kolonne A ganges med beløbet i kolonne C.                                                                                                                                                                                     |
| /        | A/C                 | Beløbet i kolonne A divideres med beløbet i kolonne C.                                                                                                                                                                                       |

#### <a name="use-a-calculation-formula-in-a-column-definition"></a>Bruge en beregningsformel i en kolonnedefinition

1.  Åbn den kolonnedefinition, der skal ændres, i Report Designer.
2.  I den relevante **CALC**-kolonne skal du angive en formel i cellen **Formel**.

#### <a name="complex-calculations"></a>Komplekse beregninger

En kompleks beregning kan indeholde enhver kombination af cellereferencer, operatorer, værdier og niveauer af indlejrede parenteser. Hvis du for eksempel vil beregne gennemsnittet af kolonne A og B, skal du bruge formlen **((A+B)/2)**.

#### <a name="specify-report-cells-in-a-column-calculation"></a>Angive rapportceller i en kolonneberegning

Du kan henvise til en bestemt rapportcelle ved at angive et kolonnebogstav og en rækkekode. For eksempel henviser **B.100** til rækkekode 100 i kolonne B. Du kan dividere en hel kolonne med et beløb i en bestemt rapportcelle i den samme kolonne. For eksempel angiver beregningen **B/B.100**, at beløbet i kolonne B skal divideres med værdien i rækkekode 100 i kolonne B. Hvis beregningen henviser til en kolonne, der afhænger af en anden kolonne, læses den afhængige kolonne først. Hvis du henviser en kolonne til en anden kolonne, der henviser til den første kolonne, opstår der en fejl på grund af en cirkulær reference. **Bemærk:** beregning kan være forkert, hvis du ændrer beregningsprioriteten for rapporten. Du kan angive beregningsprioriteten på fanen **Indstillinger** i rapportdefinitionen.

#### <a name="multiply-or-divide-a-column-by-a-base-row"></a>Gange eller dividere en kolonne med en basisrække

Du kan oprette en kolonne, der viser alle værdier i en bestemt kolonne som en procentdel af et basistal. Du kan derfor vise relationer mellem rækker, såsom en procentdel af en række med salg eller en procentdel af en række med samlede udgifter. Hvis du vil gange eller dividere alle rækker i en bestemt kolonne med en basisrække, skal du angive den kolonne, som skal anvendes til beregningen, og derefter angive **\*BASEROW** eller **/BASEROW**. Angiv f.eks. **C\*BASEROW** eller **C/BASEROW**. **Bemærk:** når du benytter en basisrækkeberegning i en kolonnedefinition, skal du sørge for, at alle de rækkedefinitioner, der bruges sammen med denne kolonnedefinition, indeholder mindst én basisrække for beregningerne.

#### <a name="divide-the-amount-in-a-column-by-the-number-of-periods"></a>Dividere beløbet i en kolonne med antallet af perioder

Du kan dividere beløbet i en kolonne med et angivet antal perioder. Formlen **B/perioder** dividerer for eksempel værdien i kolonne B med antallet af perioder i kolonne B. Hvis beregningen strækker sig over flere kolonner, kan du angive antallet af perioder, der skal bruges i beregningen. Formlen **(B+C)/perioder** lægger for eksempel beløbene i kolonne B og kolonne C sammen og dividerer derefter resultatet af periodeværdien.

<a name="see-also"></a>Se også
--------

[Rækkedefinitioner i økonomirapportering](row-definitions-financial-reporting.md)

[Avancerede formateringsindstillinger i økonomirapportering](advanced-formatting-options-financial-reporting.md)




