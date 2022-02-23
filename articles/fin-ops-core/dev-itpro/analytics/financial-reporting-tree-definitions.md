---
title: Rapportering af trædefinitioner i økonomiske rapporter
description: Denne artikel indeholder oplysninger om definitioner af rapporteringstræer. En rapporteringstrædefinition er en rapportkomponent eller en dokumentkomponent, der hjælper med at definere strukturen og hierarkiet i din organisation.
author: ShylaThompson
manager: AnnBe
ms.date: 10/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 57592
ms.assetid: 747faa47-9a23-4277-bc11-8d0a1267c3a4
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 8ae024c2d791e1219c7383dc95283219a9300eac
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682667"
---
# <a name="reporting-tree-definitions-in-financial-reports"></a>Rapportering af trædefinitioner i økonomiske rapporter

[!include [banner](../includes/banner.md)]

Denne artikel indeholder oplysninger om definitioner af rapporteringstræer. En rapporteringstrædefinition er en rapportkomponent eller en dokumentkomponent, der hjælper med at definere strukturen og hierarkiet i din organisation.

Økonomirapportering understøtter fleksibel rapportering, så du kan nemt foretage ændringer, i takt med at din virksomhedsstruktur ændres. Rapporter bygges på forskellige komponenter eller dokumentkomponenter. En af disse komponenter er en definition af et rapporteringstræ. En rapporteringstrædefinition hjælper med at definere strukturen og hierarkiet i din organisation. Det er en krydsdimensionale hierarkisk struktur, der er baseret på de størrelsesmæssige relationer i dine økonomiske data. Den giver oplysninger på rapporteringsenhedsniveau og på oversigtsniveau for alle enheder i træet. Rapporteringstrædefinitioner kan kombineres med kolonnedefinitioner og rapportdefinitioner, så de danner en komponentgruppe, der kan bruges af flere firmaer. Der bruges en rapporteringsenhed for hver boks i et organisationsdiagram. En enhed i trædiagrammet kan være en enkelt afdeling fra de økonomiske data, eller det kan være en summeringsenhed på et højere niveau, der kombinerer oplysninger fra andre enheder i trædiagrammet. For en rapportdefinition, der omfatter et rapporteringstræ, oprettes der én rapport for hver rapporteringsenhed og for oversigtsniveauet. Alle disse rapporter bruger de række- og kolonnedefinitioner, der er angivet i rapportdefinitionen, medmindre rapportdefinitionen angiver, at rapporteringstræet fra rækkedefinitionen skal bruges. Række- og kolonnedefinitioner er vigtige komponenter i udformningen af og funktionaliteten for økonomiske rapporter. Rapporteringstræer øger styrken af komponenter og understøtter fleksibel rapportering i takt med, at virksomhedsstrukturen ændres. Økonomiske rapporter, der ikke er baseret på et rapporteringstræ, anvender kun nogle af funktionerne i økonomirapportering. Du kan bruge flere rapporteringstrædefinitioner sammen med de samme række- og kolonnedefinitioner for at få vist organisationens data på forskellige måder.

## <a name="reporting-tree-best-practices"></a>Bedste fremgangsmåder for rapporteringstræ
Inden du opretter et rapporteringstræ, bør du overveje følgende bedste fremgangsmåder:

- Først skal du afgøre, hvilke rapporteringsdimensioner din juridiske enhed eller virksomhed kræver.
- Overvej, hvordan du har oprettet din struktur, og tegn derefter et organisationsdiagram for din virksomhed. Organisationsdiagrammet er med til at visualisere, hvordan du skal gruppere enhederne i trædiagrammet i et eller flere trædiagrammer.
- Start med det laveste detaljeniveau, for eksempel afdelinger og projekter, der er defineret i de økonomiske data. Føj så mange bokse til detaljeniveauet, som er nødvendige for at vise divisioner eller områder på højere niveauer. Hver boks repræsenterer en potentiel rapporteringsenhed i et hvilket som helst rapporteringstræ, du opretter.
- Du skal også overveje, hvordan du bedst opbygger din træer. Du kan bruge en automatiseret proces til at generere et rapporteringstræ, eller du kan oprette en rapporteringstræ manuelt. Det er vigtigt, at du forstår begge metoder, før du designer dine træer.
- Du kan bruge de rapporteringsenheder, der er defineret i systemet for økonomiske data, til at føje rapporteringsenheder til definitionen af rapporteringstræet.

## <a name="create-multiple-reporting-trees"></a>Oprette flere rapporteringstræer
Du kan oprette et ubegrænset antal rapporteringstræer for at få vist organisationens data på forskellige måder. Hvert trædiagram kan indeholde en hvilken som helst kombination af afdelinger og summeringsenheder. En rapportdefinition kan kun indeholde et link til et rapporteringstræ ad gangen. Ved at omarrangere strukturen af rapporteringsenhederne kan du oprette forskellige rapporteringstræer. Du kan derefter bruge de samme række- og kolonnedefinitioner for hvert rapporteringstræ. På denne måde kan du hurtigt oprette forskellige økonomirapportlayout. Hvis du opretter flere rapporteringstræer, kan du udskrive en række regnskaber hver måned, som analyserer og præsenterer din virksomheds operationer på mange forskellige måder. Du kan se eksempler på rapporteringsenhedsstrukturer i slutningen af denne artikel.

## <a name="create-a-reporting-tree-definition"></a>Oprette en rapporteringstrædefinition
En rapporteringstrædefinition indeholder de kolonner, der er beskrevet i følgende tabel.

| Kolonne i rapporteringstræ | Beskrivelse |
|-----------------------|-------------|
| Regnskab               | Firmanavnet på rapporteringsenheden. Værdien **\@ANY**, som normalt kun tildeles summeringsniveauet, gør det muligt at anvende trædiagrammet til alle firmaer. Alle underordnede grene har et firma tilknyttet. |
| Enhedsbetegnelse             | Den kode, der identificerer denne rapporteringsenhed i det grafiske rapporteringstræ. Sørg for at oprette et entydigt kodesystem, der er konsistent, og som vil være let for brugerne at forstå. |
| Enhedsbeskrivelse      | Rapporteringsenhedens titel vises i rapportens sidehoved eller sidefod, hvis du angiver **UnitDesc** som kode på fanen **Sidehoveder og sidefødder** i rapportdefinitionen. Titlen vises i rapportrækkebeskrivelsen, hvis du angiver **UnitDesc** i cellen **Beskrivelse** i rækkedefinitionen. |
| Dimensioner            | En rapporteringsenhed henter oplysninger direkte fra de økonomiske data. Den definerer den logiske placering og længder for kontoen og relaterede segmenter. Hver rapporteringsenhedsrække skal have en dimension i denne kolonne. Du kan også placere en dimension i en oversigtsrække (for eksempel for udgifter, der er direkte relateret til denne enhed). Hvis du angiver en dimension i en oversigtsrække, bør konti, der bruges i overordnede enheder, ikke bruges i underordnede enheder. Ellers kan beløb blive dubleret. |
| Rækkedefinitioner       | Navnet på rækkedefinitionen for rapporteringsenheden. Den samme rækkedefinition bruges til hver enkelt enhed i trædiagrammet. Når du opretter en rapport, bruges denne rækkedefinition til hver enhed i trædiagrammet. Rækkedefinitionen kan indeholde flere sammenkædninger af økonomiske dimensioner. Hvis der er angivet en rækkedefinition i rapporteringstræet, skal du markere afkrydsningsfeltet **Brug rækkedefinition fra rapporteringstræ** under fanen **Rapport** i rapportdefinitionen. |
| Rækkelink              | Det rækkelink, der skal bruges til enheden i trædiagrammet. Rækkelinks defineres for rækkedefinitionen for at identificere de økonomiske dimensioner, der skal linkes til. |
| Eksternt link         | Det rækkelink, der skal bruges til enheden i trædiagrammet. Der er defineret link til rækker for rækkedefinitionen for at identificere den rapport, der skal være link til. |
| Ekstern fil         | Filstien til økonomirapporteringsregnearket, der skal hentes data fra. |
| Sideindstillinger          | Denne kolonne angiver, om detaljerne for den rapporteringsenheden tilsidesættes, når rapporten vises eller udskrives. |
| Opløsning %              | Procentdelen af rapporteringsenheden, der skal allokeres til den overordnede enhed. Den procentdel, du angiver i denne kolonne, gælder for hver række i rækkedefinitionen, før værdien i rækken føjes til den overordnede rapport. Hvis en underordnet enhed for eksempel skal være fordelt ligeligt mellem to afdelinger, skal beløbene i hver række ganges med 50 procent, før værdien føjes til afdelingsrapporten. En rapporteringsenhed kan ikke have to overordnede enheder. Hvis du vil tildele beløbene fra en rapporteringsenhed til to overordnede enheder, skal du oprette en anden rapporteringsenhed, der har samme dimension, for at få vist yderligere 50 procent. Angiv hele procentsatser uden et decimaltegn. For eksempel repræsenterer **25** 25 procent allokering til den overordnede enhed. Hvis du medtager et decimaltegn (**0,25**), fordeles 0,25 procent til den overordnede enhed. Hvis du vil bruge en procentdel, der er mindre end 1 procent, skal du anvende indstillingen **Tillad opløftning på &lt;1 %** i rapportdefinitionen. Denne indstilling er på fanen **Flere indstillinger** i dialogboksen **Rapportindstillinger**. Denne dialogboks er tilgængelig via knappen **Andre** under fanen **Indstillinger** i rapportdefinitionen. |
| Sikkerhed for enhed         | Begrænsninger for de brugere og grupper, der har adgang til oplysninger for rapporteringsenheden. |
| Supplerende tekst       | Tekst, der medtages i rapporten. |

Hvis du vil oprette et rapporteringstræ, skal du følge disse trin.

1. Åbn Report Designer.
2. Klik på **Filer** &gt; **Ny** &gt; **Rapporteringstrædefinition**.
3. Klik på **Rediger** &gt; **Indsæt rapporteringsenheder fra dimensioner**.
4. I dialogboksen **Indsæt rapporteringsenheder fra dimensioner** skal du markere afkrydsningsfeltet for alle de dimensioner, der skal medtages i rapporteringstræet. Dialogboksen **Indsæt rapporteringsenheder fra dimensioner** indeholder følgende afsnit.

    | Sektion                          | Beskrivelse |
    |----------------------------------|-------------|
    | Segmentering af rapporteringsdimensioner | Brug knapperne **Opdel segmenter** og **Kombiner segmenter** til at ændre antallet og længden af segmenter.<blockquote>[!NOTE] Du kan kun kombinere segmenter, som du har opdelt. Hvis du vil kombinere flere dimensioner, skal du bruge jokertegn i dine dimensionsværdier.</blockquote> |
    | Medtag/tegnposition       | I dette afsnit vises de dimensioner, der er defineret i de økonomiske data, og antallet af tegn i den længste værdi, der er defineret for hver dimension. Marker afkrydsningsfeltet for en dimension for at medtage den i rapporteringstræhierarkiet. |
    | Hierarki og intervaller for segmenter     | I dette afsnit vises dimensionshierarkiet. Du kan flytte dimensionerne på listen for at ændre deres rapporteringsrækkefølge. I felterne **Fra dimension** og **Til dimension** kan angive et interval af værdier inden for hver dimension. Hvis du ikke angiver et interval, indsættes alle dimensionsværdier i rapporteringstræet.<blockquote>[!NOTE] Hvis du bruger mere end én dimension, er det kun kombinationer af de dimensioner, der er bogført til, som returneres i resultaterne.</blockquote> |

    Du kan finde et skærmbillede, der viser et eksempel på dialogboksen **Indsæt rapporteringsenheder fra dimensioner**, i afsnittet "Eksempel på dialogboksen Indsæt rapporteringsenheder fra dimensioner" senere i denne artikel.

5. Hvis du vil oprette flere segmenter (f.eks ved at opdele ét segment i to kortere segmenter), skal du klikke på den korrekte placering i et felt af typen **Tegnposition** og derefter klikke på **Opdel segmenter**.
6. Hvis du vil flette to segmenter i ét segment, skal du klikke i en af boksene for segmentet, der skal flettes, og derefter klikke på **Kombiner segmenter**.
7. Hierarkiet definerer, hvordan dimensioner rapporterer til hinanden og området for hver dimension. Hvis du vil ændre hierarkiet for dimensionerne i området **Segmenthierarki og -intervaller**, skal du markere den dimension, du vil flytte, og derefter klikke på **Flyt op** eller **Flyt ned**.
8. Hvis du vil angive et interval af dimensionsværdier, som skal føjes til det nye rapporteringstræ, skal du benytte nedenstående fremgangsmåde i området **Segmenthierarki og -intervaller**:

    1. I feltet **Fra dimension** for den pågældende dimension skal du angive den første værdi i intervallet.
    2. I feltet **Til dimension** skal du angive den sidste værdi i intervallet.

9. Gentag trin 7 og 8 for hver dimension i området **Segmenthierarki og -intervaller**.
10. Når du er færdig med at definere, hvordan dine rapporteringsenheder skal hentes til det nye rapporteringstræ, skal du klikke på **OK**.
11. Klik på **Filer** &gt; **Gem** for at gemme rapporteringstræet. Angiv et entydigt navn og en entydig beskrivelse for rapporteringstræet, og klik derefter på **OK**.

### <a name="open-an-existing-reporting-tree-definition"></a>Åbne en eksisterende rapporteringstrædefinition

1. Klik på **Rapporteringstrædefinitioner** i navigationsruden i Report Designer.
2. Dobbeltklik på et navn på listen med rapporteringstræer for at åbne det.
3. For at få vist komponenter, der er knyttet til rapporteringstræet, skal du højreklikke på rapporteringstrædefinitionen og derefter vælge **Tilknytninger**.

### <a name="roll-up-data-in-a-reporting-tree"></a>Opsummere data i et rapporteringtræ

Når du bruger et rapporteringstræ, kan du indsamle beløb fra underordnede rapporteringsenheder på niveauet for den overordnede rapporteringsenhed. Denne aggregering kaldes også akkumulering af data. Følgende regler bruges til at akkumulere beløb til overordnede enheder i et rapporteringstræ:

- I et rapporteringstræ skal underordnede enheder indeholde dimensioner, medmindre rapporteringstræet er et træ med et enkelt niveau. Overordnede enheder indeholder normalt ikke dimensioner i et rapporteringstræ.

    > [!NOTE]
    > Hvis du angiver dimensioner for både underordnede enheder og overordnede enheder, kan det medføre dubletter af data i rapporten.

- Rapporteringsenheder, som indeholder dimensioner i rapporteringtræet, svarer til de dimensioner, der anvendes i række- og kolonnedefinitioner. Kombinationen af dimensioner bestemmer de beløb, der returneres for denne enhed. For eksempel, i eksempel 2 senere i denne artikel returnerer linje 6 og 7 kun værdier for henholdsvis afdeling 00 og 01.
- Beløbene for overordnede rapporteringsenheder, der ikke indeholder dimensioner i rapporteringstræet, bestemmes på basis af rapporten for den underordnede rapport og akkumulerer beløbet til den angivne overordnede enhed. Hvis den overordnede enhed (se Contoso USA i eksempel 2 med eksempler på dataakkumulering) for eksempel har to underordnede enheder (022 og 023) og ikke indeholder dimensioner, genereres der en rapport for hver underordnet og overordnet enhed. Den overordnede total er summen af de to underordnede beløb.

### <a name="manage-reporting-units"></a>Administrere rapporteringsenheder

Hver rapportingstrædefinition vises i entydige visninger. Der er en grafisk visning, der viser det overordnede/underordnede hierarki og en regnearksvisning, der viser de specifikke oplysninger om hver rapporteringsenhed. Den grafiske visning og visningen af regnearket er forbundne. Når du vælger en rapporteringsenhed i én visning, er den også valgt i den anden visning. Du kan opbygge krydsdimensionale hierarkier, der er baseret på de størrelsesmæssige relationer i de økonomiske data. Når du opretter en rapporteringstrædefinition, kan du bruge de samme rækkedefinitioner flere gange, uanset om du genererer en afdelings resultatopgørelse eller en konsolideret oversigt over resultatopgørelsen. De dimensioner, der er defineret i rækkedefinitionen, kan kombineres med dimensioner i rapporteringstrædefinitionen for at få flere forskellige visninger af organisationens performance.

### <a name="reporting-unit-structure"></a>Rapporteringsenhedens struktur

Der anvendes følgende typer rapporteringsenheder i økonomirapportering:

- En detaljeenhed henter oplysninger direkte fra de økonomiske data, fra et Excel-regneark eller fra et andet regneark til økonomirapportering.
- En oversigtsenhed opsummerer data fra enheder på et lavere niveau.

En overordnet rapporteringsenhed er en oversigtsenhed, der indsamler opsummerede oplysninger fra en detaljeenhed. En oversigtsenhed kan være både en detaljeenhed og en sammenfattende enhed. Derfor kan en oversigtsenhed hente oplysninger fra en enhed på et lavere niveau, de økonomiske data eller et Excel-regneark. En overordnet enhed kan være underordnet enhed for en overordnet enhed på et højere niveau. En underordnet rapporteringsenhed kan være en detaljeenhed, der henter oplysninger direkte fra de økonomiske data eller et Excel-regneark. En underordnet rapporteringsenhed kan også være en midlertidig oversigtsenhed. Med andre ord kan det være den overordnede enhed for en enhed på et lavere niveau og også den underordnede enhed i en oversigtsenhed på et højere niveau. I det mest almindelige scenario for rapporteringsenheder har overordnede enheder en tom celle i kolonnen **Dimensioner**, og underordnede enheder har links til kombinationer af specifikke dimensioner eller dimensioner med jokertegn.

### <a name="organize-reporting-units"></a>Organisere rapporteringsenheder

Du kan omarrangere den organisatoriske struktur i en rapporteringstrædefinition ved at flytte rapporteringsenheder i den grafiske visning. Du kan også hæve rapporteringsenheder til et højere niveau i rapporteringstræet eller sænke dem til et lavere niveau.

1. Åbn den rapporteringstrædefinition, der skal ændres, i Report Designer.
2. Vælg en rapporteringsenhed i den grafiske visning af rapporteringstrædefinitionen.
3. Træk enheden til en ny placering. Du kan også højreklikke på enheden og derefter vælge **Hæv rapporteringsenhed** eller **Sænk rapporteringsenhed.**
4. Klik på **Filer** &gt; **Gem** for at gemme ændringerne.

### <a name="add-text-about-a-reporting-unit"></a>Tilføje tekst om en rapporteringsenhed

Ekstra indtastet tekst er en statisk tekststreng på op til 255 tegn, der føjer oplysninger til rapporteringstrædefinitionen. Supplerende tekst kan eksempelvis være en kort virksomhedsbeskrivelse. Du kan oprette op til ti ekstra tekstelementer for hver rapporteringsenhed i en rapporteringstrædefinition. Den ekstra tekst vises i rapporten for den rapporteringsenhed, som teksten er tildelt til. Du kan tilføje tekst fra kolonnen **Beskrivelse** i rækkedefinitionen og fra fanen **Sidehoveder og sidefødder** i rapportdefinitionen.

1. Åbn den rapporteringstrædefinition, der skal ændres, i Report Designer.
2. Dobbeltklik på cellen **Supplerende tekst** for rapporteringsenhedsrækken.
3. Skriv teksten i den første tomme række i dialogboksen **Supplerende tekst**. Den første række, der indeholder tekst, refereres til som UnitText1, uanset dens placering i dialogboksen **Supplerende tekst**.
4. Hvis du vil tilføje mere tekst til denne rapporteringsenhed, skal du skrive teksten i en tom række.
5. Klik på **OK**.

### <a name="remove-additional-text-from-a-reporting-unit"></a>Fjerne supplerende tekst fra en rapporteringsenhed

1. Åbn den trædiagramdefinition, der skal redigeres, i Rapportdesigner.
2. Dobbeltklik på cellen **Supplerende tekst** for rækken for enheden i trædiagrammet.
3. Vælg den tekst, der skal fjernes, i dialogboksen **Supplerende tekst**, og klik derefter på **Ryd**. Du kan også højreklikke på posten og derefter vælge **Klip**.
4. Klik på **OK**.

### <a name="restrict-access-to-a-reporting-unit"></a>Begrænse adgangen til en rapporteringsenhed

Du kan forhindre bestemte brugere og grupper i at få adgang til en rapporteringsenhed. Du kan også definere begrænsninger, så de gælder for underordnede rapporteringsenheder i rapporteringsenheden.

1. Åbn den rapporteringstrædefinition, der skal ændres, i Report Designer.
2. Dobbeltklik på cellen **Enhedssikkerhed** for den række med enheden i trædiagrammet, som du vil begrænse adgangen til.
3. I dialogboksen **Sikkerhed for enhed** skal du klikke på **Brugere og grupper**.
4. Vælg de brugere eller grupper, der skal have adgang til rapporteringsenheden, og klik derefter på **OK**.
5. Hvis du vil begrænse adgangen til underordnede rapporteringsenheder, skal du markere afkrydsningsfeltet **Føj sikkerhed til underordnede rapporteringsenheder**.
6. Klik på **OK**.

### <a name="remove-access-to-a-reporting-unit"></a>Fjerne adgangen til en rapporteringsenhed

1. Åbn den rapporteringstrædefinition, der skal ændres, i Report Designer.
2. Dobbeltklik på cellen **Sikkerhed for enhed** for den rapporteringsenhedsrække, du vil fjerne adgangen til.
3. Marker et navn i dialogboksen **Sikkerhed for enhed**, og klik derefter på **Fjern**.
4. Klik på **OK**.

### <a name="link-to-reports"></a>Link til rapporter

Når du har oprettet en **rapport**-kolonne i rækkedefinitionen og har angivet den rapport, der skal medtages i rapporten, skal du opdatere rapporteringstræet med den tilknyttede kolonne og oplysningerne om rapporten. Der kan importeres en rapport til enhver enhed i rapporteringstræet.

### <a name="identify-the-report-in-a-reporting-tree"></a>Identificer rapporten i et rapporteringstræ

1. Åbn den rapporteringstrædefinition, der skal ændres, i Report Designer.
2. I kolonnen **Rækkedefinitioner** er oplysningerne i cellerne baseret på oplysningerne for den valgte række, fordi det samme rækkedefinition skal bruges i alle rapporteringstræets enheder. Dobbeltklik på cellen **Rækkedefinitioner**, og vælg derefter den rækkedefinition, der indeholder oplysninger om rapporten.
3. I cellen **Link til regneark** for en rapporteringsenhed skal du vælge det linknavn, der svarer til rapporten.
4. I cellen **Projektmappe eller rapportsti** for en rapporteringsenhed, skal du angive navnet på rapporten eller søge efter og vælge rapporten.
5. Hvis du vil angive et regneark i en rapport, skal du angive navnet på regnearket i cellen **Navn på regneark**.
6. Gentag trin 3 til og med 5 for hver rapporteringsenhed, der skal modtage data fra en rapport. For at forhindre, at der vises forkerte data i rapporten, skal du sørge for, at de korrekte rapportnavne vises i den tilsvarende enhed i rapporteringstræet.

## <a name="examples"></a>Eksempler
### <a name="reporting-unit-structure--example-1"></a>Rapporteringsenhedstruktur – eksempel 1

Her er strukturen for rapporteringsenhederne i følgende rapporteringstræ:

- Contoso Japan-rapporteringsenheden er en overordnet enhed af Contoso Japan-salg og Contoso Japan Consulting underordnede enheder.
- Divisionsenheden Contoso Japan-salg er både en underordnet enhed til Contoso Japan-enheden og en overordnet enhed til enhederne Hjemmesalg og Autosalg.
- Rapporteringsenhederne på det laveste niveau (Hjemmesalg, Autosalg, Kundeservice og Operationer) repræsenterer afdelinger i de økonomiske data. Disse rapporteringsenheder er i det nedtonede område i diagrammet.
- Oversigtsenhederne på de højere niveauer opsummerer oplysninger fra detaljeenhederne.

[![ContosoEntertainmentSummaryReportStructure](./media/contosoentertainmentsummaryreportstructure.png)](./media/contosoentertainmentsummaryreportstructure.png)

### <a name="reporting-unit-structure--example-2"></a>Rapporteringsenhedstruktur – eksempel 2

I følgende diagram har rapporteringstræet en organisationsstruktur, der er opdelt efter forretningsfunktion.

[![summaryofallunitscontoso](./media/summaryofallunitscontoso.png)](./media/summaryofallunitscontoso.png)

### <a name="example-of-the-insert-reporting-units-from-dimensions-dialog-box"></a>Eksempel på dialogboksen Indsæt rapporteringsenheder fra Dimensioner

Følgende illustration viser et eksempel på dialogboksen **Indsæt rapporteringsenheder fra Dimensioner**. I dette eksempel returnerer resultaterne kombinationen af virksomhedsenheder, bærere og afdelinger.

[![InsertReportingUnits](./media/insertreportingunits.png)](./media/insertreportingunits.png)

Den resulterende rapporteringstrædefinition er sorteret efter virksomhedsenhed og derefter efter bærer og derefter efter afdeling. Dimensionen for den femte rapporteringsenhed er **Virksomhedsenhed = \[001\] Bærer =\[\], Afdeling = \[022\]**, og den identificerer en rapporteringsenhed for konti, der er specifikke for virksomhedsenhed 001 og afdeling 022.

[![ReportingTree](./media/reportingtree-1024x646.png)](./media/reportingtree.png)

### <a name="examples-of-data-roll-up"></a>Eksempler på dataakkumulering

Følgende eksempler viser mulige oplysninger, der bruges i en definition af et rapporteringstræ for akkumulerede data.

#### <a name="example-1"></a>Eksempel 1

[![MutliCompanyRollUp](./media/mutlicompanyrollup.png)](./media/mutlicompanyrollup.png)

#### <a name="example-2"></a>Eksempel 2

[![CrossCompanyDepartmentRollUp](./media/crosscompanydepartmentrollup.png)](./media/crosscompanydepartmentrollup.png)

## <a name="additional-resources"></a>Yderligere ressourcer

[Økonomirapportering](financial-reporting-intro.md)
