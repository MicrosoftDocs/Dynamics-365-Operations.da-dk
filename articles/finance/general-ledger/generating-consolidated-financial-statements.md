---
title: Generere konsoliderede regnskaber
description: I dette emne beskrives de forskellige scenarier, hvor du kan generere konsoliderede regnskaber.
author: aprilolson
manager: AnnBe
ms.date: 07/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 0078d536e55da0bfd3d8b808eb05c8273aba792d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249137"
---
# <a name="generate-consolidated-financial-statements"></a>Generere konsoliderede regnskaber

[!include [banner](../includes/banner.md)]

I dette emne beskrives de forskellige scenarier, hvor du kan generere konsoliderede regnskaber.

## <a name="single-level-and-multilevel-consolidations-across-legal-entities"></a>Konsolideringer på enkeltniveau og på flere niveauer på tværs af juridiske enheder
Den mest enkle metode til konsolidering ved hjælp af Økonomirapportering er at bruge trædiagrammer til at indsamle data på tværs af regnskaber, der har samme kontoplan og regnskabsperioder. Her er de overordnede trin til at udføre konsolidering ved hjælp af et trædiagram.

1. Opret en rækkedefinition, og sørg for, at alle relevante konti i alle regnskaber er medtaget i rækkerne.
2. Opret en kolonnedefinition, der indeholder alle de kolonner, der kræves til den rapport, du vil oprette.
3. Opret et trædiagram, der indeholder en rapporteringsnode for hvert regnskab, du bruger i konsoliderede rapporter.

> [!TIP]
> Du kan finde flere oplysninger om, hvordan du kan oprette og administrere rækkedefinitioner, kolonnedefinitioner og trædiagrammer, i [Komponenter i økonomisk rapport](../../dev-itpro/analytics/financial-report-components.md).

I følgende illustration vises, hvordan du kan bruge en trædiagramdefinition i Økonomirapportering til at identificere hvert regnskab, du vil konsolidere.

![Rapporteringstrædefinition](./media/reporting-tree-definition.png "Rapporteringstrædefinition")

Som den konsoliderede rapport i følgende illustration viser, kan du se hvert firma separat, når du bruger trædiagrammet sammen med en rapportdefinition. De konsoliderede beløb vises på oversigtsniveau.

![Oversigtsniveau for konsoliderede beløb](./media/consolidate-amount-summary-level.png "Oversigtsniveau for konsoliderede beløb")

Du kan også oprette et trædiagram med flere niveauer. Diagrammet kan indeholde så mange niveauer, som du har brug for. I følgende illustration vises en trædiagramdefinition med flere niveauer, der indeholder akkumuleringer fra områder verden over.

![Trædefinition i flere niveauer med akkumuleringer efter område](./media/multilevel-reporting-tree-definition-roll-ups-worldwide-region.png "Trædefinition i flere niveauer med akkumuleringer efter område")

I følgende illustration vises en trædiagramdefinition med flere niveauer, der indeholder akkumuleringer efter funktion.

![Trædefinition i flere niveauer med akkumuleringer efter funktion](./media/multilevel-reporting-tree-definition-roll-ups-by-function.png "Trædefinition i flere niveauer med akkumuleringer efter funktion")

### <a name="viewing-companies-side-by-side"></a>Regnskaber vist ved siden af hinanden
Mange kunder foretrækker rapporter, hvor regnskaberne vises ved siden af hinanden, og hvor en kolonne viser den konsoliderede total. Dette format er let at opnå, når du har oprettet trædiagrammet. Her er de overordnede trin, du skal bruge for at få vist regnskaber side om side i konsoliderede regnskaber.

1. Opret en kolonnedefinition, der indeholder kolonnen **Økonomisk dimension** for hvert firma.
2. Brug feltet **Enhed i trædiagram** til at vælge træet og enheden i trædiagrammet for hver kolonne.
3. Valgfrit: Tilføj overskrifter og kolonner til totaler.

I følgende illustration vises en kolonnedefinition i side om side-format.

![Kolonnedefinition i et side om side-format](./media/column-definition-side-by-side-format.png "Kolonnedefinition i et side om side-format")

## <a name="consolidations-that-use-organization-structures-that-are-created-from-legal-entities"></a>Konsolideringer, der bruger organisationsstrukturer, der er oprettet ud fra juridiske enheder
Organisationshierarkier, der indeholder dimensioner eller juridiske enheder, opretter dynamisk trædiagramdefinitioner i Økonomirapportering. En nem måde at strømline konsolideringer på er ved at føje et organisationshierarki til rapporten i Økonomirapportering. Baseret på rapportdatoen vælger Financial Reporting organisationshierarkiet på eller før ikrafttrædelsesdatoen, som vist i følgende illustration.

![Dynamisk oprettelse af trædiagramdefinition](./media/dynamically-create-reporting-tree-definitions.png "Dynamisk oprettelse af trædiagramdefinition")

## <a name="consolidations-that-involve-eliminations"></a>Konsolideringer, der omfatter elimineringer
Elimineringstransaktioner er en almindelig del af konsolideringsprocessen. I dette eksempel elimineres fem konti under konsolideringen: 142600, 211400, 401420, 401180 og 510820. Virksomheder kan oprette deres mellemregningskonti anderledes. Nogle virksomheder vælger f.eks. at indstille det sidste ciffer til 9, hvis kontoen bruges i mellemregningstransaktioner. Uanset metoden, hvis du kender mellemregningskontiene, kan du vise elimineringer i dine konsoliderede regnskaber.

Følgende illustration viser en kolonnedefinitionen for en konsolideret resultatopgørelse. Der er defineret tre driftsmellemregningskonti for hvert regnskab ved hjælp af dimensionsfilteret. Kolonnerne F, G og H omfatter kun elimineringskontiene for USMF-, USRT- og DEMF-regnskaberne. Disse kolonner er konfigureret, så de **ikke** udskrives i regnskabet.

![Kolonnedefinitionen for en konsolideret resultatopgørelse](./media/column-definition-consolidated-income-statement.png "Kolonnedefinitionen for en konsolideret resultatopgørelse")

Når rapporten oprettes, beregnes elimineringsbeløbene i kolonne F, G og H, og de lægges sammen i kolonne I. J viser de konsoliderede beløb. Disse konsolideringsbeløb udelader elimineringer for firmaerne USMF, USRT og DEMF.

> [!TIP]
> Du kan oprette endnu en rapport, der kun viser elimineringsposterne, og bruge den i en rapportgruppe, der indeholder den konsoliderede rapport. På denne måde kan du have de nødvendige oplysninger til at oprette alle kladdeposteringer, der kræves.

Følgende illustration viser den konsoliderede rapport.

![Konsolideret rapport for resultatopgørelse](./media/consolidated-report-income-statement.png "Konsolideret rapport for resultatopgørelse")

Om du bruger konti, dimensioner eller begge dele, kan du i Økonomirapportering filtrere elimineringsposter ved hjælp af dimensionsfiltreringsfunktionerne.

## <a name="minority-interest"></a>Minoritetsinteresse
Et firma ejer muligvis kun en procentdel af et andet firma. I denne situation, når du udarbejder en konsolideret rapport, er det vigtigt kun at medregne den procentdel, som firmaet ejer. Økonomirapportering har flere forskellige måder at vise minoritetsinteresse, afhængigt af brugerindstillinger. Én måde er at bruge en akkumuleringsprocentdel i trædiagramdefinitionen. En anden måde er at vise minoritetsejerskab som en separat linje i en rapport.

### <a name="using-the-reporting-tree-definition"></a>Bruge trædiagramdefinitionen
I trædiagramdefinitionen skal du angive procentdelen af ejerskab i kolonnen **Aggregeringsprocent** (kolonne H) som vist i følgende illustration. Når rapporten oprettes, bruges denne procentdel til beregning af det konsoliderede beløb. I dette eksempel har Contoso kun 80 % af Contoso Germany. Du kan angive enten **80** eller **0,8** i kolonnen **Aggregeringsprocent**, og 80 procent skal akkumuleres til det konsoliderede niveau.

> [!NOTE]
> Du kan anvende denne procentdel af ejerskabet på alle rapporteringsenheder, ikke kun på firmaniveau. 

![Bruge procentdel i trædiagramdefinition](./media/Using-reporting-tree-definition-percentage.png "Bruge procentdel i trædiagramdefinition")

Når rapporten oprettes, viser rapporten Contoso Germany 100 procent af salgsbeløbet, og 80 procent af beløbet bliver fordelt og aggregeret til det konsoliderede niveau for salg.

Hvis du har mindre end 1 % af et firma, kan du markere afkrydsningsfeltet **Tillad aggregering på mindre end 1%** under fanen **Flere indstillinger** på siden **Rapportindstillinger** som vist i følgende illustration. I så fald behandles værdier i kolonnen **Aggregeringsprocent** i diagramtræet som mindre end 1 %. Hvis du f.eks. angiver **0,8**, aggregeres 0,8 % til det konsoliderede niveau, og ikke 80 procent. Alternativt kan du opnå samme resultat ved ikke at markere afkrydsningsfeltet **Tillad aggregering på mindre end 1%** og angive **0,008** i kolonnen **Aggregeringsprocent**.

![Indstillinger for rapporteringsindstillinger](./media/reporting-setting-options.png "Indstillinger for rapporteringsindstillinger")

### <a name="showing-ownership-as-a-separate-row-on-the-consolidated-report"></a>Viser ejerskab som en separat række i den konsoliderede rapport
En anden indstilling for minoritetsinteresse er at vise 100 procent af datterselskabet for hver linje i rapporten, men fratrække den ikke-bestemmende aktiepost fra nettofortjenesten.

Som følgende illustration viser, kan en **ikke-bestemmende aktiepost**-sætning og kolonnebegrænsning i rækkedefinitionen bruges til at beregne minoritetsinteresse i økonomirapporter.

![Viser ejerskab som en separat række i den konsoliderede rapport](./media/Showing-ownership-separate-row-consolidated-report.png "Viser ejerskab som en separat række i den konsoliderede rapport")

## <a name="multiple-charts-of-accounts-across-legal-entities"></a>Flere kontoplaner på tværs af juridiske enheder
Ofte har forskellige juridiske enheder forskellige kontoplaner, men vil alligevel oprette konsoliderede regnskaber. I så fald kan Økonomirapportering bruges til at konsolidere dataene, så du kan oprette konsoliderede økonomirapporter. Her er de overordnede konsolideringstrin, når der findes forskellige kontoplaner på tværs af juridiske enheder.

1. Opret en rækkedefinition, der har flere links til økonomiske dimensioner. Der bør være ét hyperlink for hver kontoplan.
2. Brug begrænsningen af enheden i trædiagrammet i kolonnedefinitionen til at tildele hvert firma til den relevante kolonne.


Der kan tilføjes flere links til økonomiske dimensioner i hver række i rækkedefinitionen for hvert entydigt firmas kontoplanen. I følgende illustration bruger USMF-firmaet kontosættet i den først **Link til økonomiske dimensioner**-kolonne (kolonne J), og DEMF-firmaet bruger kontiene i anden **Link til økonomiske dimensioner**-kolonne (kolonne K).

> [!TIP]
> Du kan finde flere oplysninger om cellen **Link til økonomiske dimensioner** under Angiv link til cellen Økonomiske dimensioner.

![Sæt konti først-link til økonomiske dimensioner](./media/set-accounts-first-Link-to-Financial-Dimensions.png "Sæt konti først-link til økonomiske dimensioner")

Du kan bruge et trædiagram til at definere, hvilket link til økonomiske dimensioner fra rækkedefinitionen, der bruges sammen med hvert firma. Vælg rækkedefinitionen i kolonne E, og vælg derefter det relevante rækkelink i kolonne F, som vist i følgende illustration.

![Anvendt rækkedefinition for link til økonomiske dimensioner](./media/link-financial-dimensions-row-definition-used.png "Anvendt rækkedefinition for link til økonomiske dimensioner")

> [!TIP]
> Når du opretter links til økonomiske dimensioner, skal du bruge beskrivelsen til at identificere de firmaer, som hvert hyperlink gælder for. På denne måde kan du lettere vælge det rigtige firma, når du opretter et trædiagram. I kolonnedefinitionen kan du i feltet **Enhed i trædiagram** begrænse hver kolonne til en enhed i træet, så du kan få vist dataene ved siden af hinanden. Hvis du ikke angiver et bestemt firma for en kolonne, vises konsoliderede data for alle firmaer.

## <a name="different-fiscal-calendars-across-multiple-legal-entities"></a>Forskellige regnskabskalendere på tværs af flere juridiske enheder
Forskellige juridiske enheder kan have forskellige regnskabskalendere, men vil alligevel skulle oprette konsoliderede regnskaber. Der findes to konsolideringsmåder, når der findes forskellige regnskabsperioder på tværs af juridiske enheder:

- Opret en kolonnedefinition, og brug perioden og året til at tilknytte de relevante perioder for hvert regnskab.
- Vælg **Indstillinger** \> **Andre** \> **Flere indstillinger**, vælg, om konsolideringen skal udføres ved hjælp af periodens slutdato eller periodenummeret.

Når du udformer kolonnedefinitionen for flere firmaer, der har forskellige regnskabsperioder, er det vigtigt, at du overvejer, hvilket firma der skal tildeles til feltet **Firmanavn** i rapportdefinitionen. Det pågældende firmas regnskabskalender bruges som basisregnskabskalender for rapportdefinitionen. Tabellen nedenfor viser f.eks. regnskabsperiodeopsætningen for firmaerne USMF og INMF. For konsoliderede rapporter skal du bruge den regnskabskalender, som USMF bruger. Kolonnen "Tilknytning" viser den tilsvarende periode og det tilsvarende år for hvert regnskab, hvis en rapport er oprettet for den 30. juni 2018.

| Regnskab   | Regnskabsår                                  | Overførsel                     |
|-----------|----------------------------------------------|-----------------------------|
| USMF      | Regnskabsåret 1. juli til og med 30. juni          | Periode 12, regnskabsåret 2018 | 
| INMF      | Kalenderåret 1. januar til 31. december | Periode 6, regnskabsåret 2018  |

I følgende illustration er firmaet USMF angivet i feltet **Firmanavn** i rapportdefinitionen. Derfor bruges USMF-firmaets regnskabskalender som basisregnskabskalender. Når der i dette eksempel genereres en rapport til 30. juni 2018, bruger firmaet USMF den grundlæggende BASE-periode, der er defineret som periode 12 i rapportdefinitionen. INMF-firmaet bruger BASE–6, som er periode 6. Begge kolonner indeholder data for juni 2018.

![Grundlæggende rapportperiode](./media/report-base-period.png "Grundlæggende rapportperiode")

I følgende illustration vises de indstillinger i rapportdefinitionen, hvor du kan vælge, om periodenummeret eller periodens slutdato skal bruges til konsolideringen.

![Indstillinger for rapportdefinitionens periodenummer](./media/options-report-definition-period-number.png "Indstillinger for rapportdefinitionens periodenummer")

## <a name="business-unit-consolidations"></a>Konsolideringer af virksomhedsenheder
Dette emne har fokuseret på at bruge trædiagramdefinitioner og organisationshierarkier i Økonomirapportering med henblik på konsolidering. Du kan også bruge trædiagrammet til at oprette konsolideringsrapporter for virksomhedsenheden, f.eks. rapporter om globalt salg eller operationer. Disse rapporter er et almindelig krav. Du kan oprette dem ved at vælge et firma og en dimension for hver enhed, som du vil konsolidere for. F.eks. i følgende illustration er akkumuleringen for virksomhedsenheden opnået ved at gentage hver virksomhed i kolonnen **Firma** (kolonne A) og identificere en gruppe af Dimensionsværdi for afdeling pr. firma i kolonnen **Dimensioner** (kolonne D).

![Konsolideringsrapporter for virksomhedsenheder](./media/business-unit-consolidation-reports.png "Konsolideringsrapporter for virksomhedsenheder")

## <a name="consolidations-that-involve-multiple-reporting-currencies"></a>Konsolideringer, der involverer flere rapporteringsvalutaer
Økonomirapportering giver øget fleksibilitet, når du får vist faktiske data, budgetdata, budgetstyrings- og budgetplanlægningsdata i flere valutaer. Når du leverer på tværs af nøgleopsætningsdata behøver du ikke at fortage yderligere opsætning i Økonomirapportering for at få vist en rapport i en hvilken som helst valuta til enhver tid for alle brugere.

### <a name="prerequisites"></a>Forudsætninger
Hvis du vil beregne korrekt oversatte saldi, kræver Økonomirapportering, at kategorien **Konto for overført overskud** knyttes til kontoen for overført overskud på **Hovedkonto**-listen. Økonomirapportering understøtter ikke bogføring på kontoen for overført overskud. Hvis der bogføres posteringer på kontoen for overført overskud, beregnes de oversatte saldi ikke korrekt. Vi anbefaler, at brugerne opretter en ekstra konto for overført overskud til bogføring af reguleringer af kontoen for overført overskud.

På hovedkontoen skal felterne **Valutakurstype for økonomirapportering** og **Valutaomregningstype** i oversigtspanelet **Økonomirapportering** indstilles for hver konto, som vist i følgende illustration. Du kan udføre denne opgave konto for konto, eller du kan bruge kontoskabelonerne til let at implementere ændringer.

- I feltet **Valutakurstype for økonomirapportering** skal du vælge den valutakurstype, der indeholder de valutaer og valutakurser, der skal gælde for kontoen. Denne tabel over valutaer og valutakurser vil blive anvendt til faktiske data i Økonomirapportering.
- I feltet **Valutaomregningstype** skal du vælge metoden, der bruges til at beregne valutakursen for kontoen. Denne valutametode bruges til både faktiske og budgetterede data i Økonomirapportering.

![Hovedkonti for økonomisk rapportering](./media/Financial-reporting-main-accounts.png "Hovedkonti for økonomisk rapportering")

For budget-, budgetstyrings- og budgetplanlægningsdata defineres valutakurstypen på siden **Finans**. Denne tabel skal bruges til at trække valutakurserne, og den valutaomregningstype, der er tildelt til kontoen, bruges.

### <a name="currency-translation-methods"></a>Valutaomregningsmetoder
Der er fire indstillinger til beregning af valutakurser i Økonomirapportering:

- **Vægtet gennemsnit** – Denne metode bruges oftest til driftskonti. Den bruger følgende formel:

    (Valutakurs × dage i kraft) ÷ dage i periode

- **Gennemsnit** – Denne metode er et alternativ til driftskonti. Den bruger følgende formel:

    Summen af valutakurser ÷ antal valutakurser

- **Aktuelt** – Denne metode bruges oftest til statuskonti. Den valutakurs, der bruges, er kursen på eller før datoen for rapporten eller kolonnen i Økonomirapportering.
- **Posteringsdato** – Denne metode bruges til anlægskonti. Den valutakurs, der bruges, er kursen på den dag, hvor anlægsaktivet blev anskaffet. Hvis der ikke er angivet en kurs for denne dato, bruges den tidligere kurs, der blev angivet tættest på anskaffelsesdatoen for aktivet.

### <a name="report-designer-options-for-currency-translation"></a>Indstillinger for rapportdesigner for omregning af valuta
I Økonomirapportering kan enhver rapport vises i et hvilket som helst antal rapporteringsvalutaer. Følgende felter i rapportdefinitionen understøtter denne funktion:

- Sektionen **Valutaoplysninger** på siden **Rapportdefinition**. Denne sektion beskriver den valuta, som værdierne vises i, når der oprettes en rapport.
- Et nyt **Medtag alle rapporteringsvalutaer**-afkrydsningsfelt. Når dette afkrydsningsfelt er markeret, føjes der en rapport for hver rapporteringsvaluta til rapportkøen, når den rapport, der anvender firmaets funktionelle valuta, er genereret. Hvis markeringen i afkrydsningsfeltet fjernes, kan du stadig vælge en rapporteringsvaluta i Webfremviser. I så fald behandles rapporteringsvalutaen, når du vælger den.

Med indstillingerne i rapportdefinitionen kan du nemt at omregne en rapport til alle dine rapporteringsvalutaer. Derfor kan du måske fjerne dublerede rapportdefinitioner, som kun afviger de valutaer, der bruges. Hvis du har brug for en rapport, der viser flere valutaer ved siden af hinanden, kan du fortsætte med at bruge feltet **Valutavisning** på siden **Kolonnedefinition** til at omregne netop denne kolonne i rapporten til en anden rapporteringsvaluta.

### <a name="currency-translation-adjustment"></a>Regulering af valutaomregning
Regulering af valutaomregning (CTA) er forskellen mellem de kurser, der bruges til at beregne statuskontiene og den kurs, der bruges til resultatopgørelseskontiene. Denne forskel medfører, at balancen ikke balancerer. Du kan bruge Økonomirapportering til at beregne CTA på to måder:

- Brug siden **Afrundingsdifferencer** i rækkedefinitionen, som vist i følgende illustration.

    ![Afrundingsdifferencer ved regulering af valutaomregning](./media/Currency-translation-adjustment-rounding-adjustments.png "Afrundingsdifferencer ved regulering af valutaomregning")

    Når du angiver den række, der skal vise afrundingsdifferencer (CTA), den samlede række aktiver, de samlede passiver og egenkapitalrækken og den grænse, som du finder i orden, beregner Økonomirapportering forskellen og placerer den i den ønskede række. Der oprettes en linje, **Afrundingsdifference**, som vises ved detailudledning, som vist i følgende illustration.

    ![Detailudledning for afrundingsdifference](./media/rounding-adjustment-drill-down.png "Detailudledning for afrundingsdifference")

- Placer alle konti i et område fra aktiver til udgifter. Som vist i følgende illustration bliver forskellen samme beløb som afrundingsdifferencen. Derfor kan du bruge den som en kontroltotal for at sikre, at siden med afrundingsdifferencen ikke indeholder nogen kontosaldi, som er sprunget over.

    ![Formular til kontrol af afrundingsdifference](./media/rounding-adjustment-form-check.png "Formular til kontrol af afrundingsdifference")

### <a name="balance-calculation-approach"></a>Saldoberegningsmetode
For at få korrekt omregnede beløb, når valutaer bruges, bruger Økonomirapportering følgende beregningsmåder for saldi:

- **Vægtet gennemsnit og gennemsnit** – Hver periode beregnes som sit vægtede gennemsnit og lægges sammen for kolonner, f.eks. kvartalsvis og år til dato.
- **Historisk** – Alle konti, der bruger den historiske omregningsmetode, går altid tilbage til posteringsdatoen. Hvis anskaffelsesdatoen er knyttet til posteringen, bruges denne dato til at få valutakursen. Hver periode lægges herefter sammen og gemmes for at forbedre beregningstiden.
- **Aktuelt** – Beregnede kolonner og kolonner med totaler, f.eks. kolonner til kvartalsvis og år til dato, beregnes med den spotkurs, som beregnes i kolonnen eller i rapporten. For eksempel bruger kolonnen **1. kvartal** kursen fra den 31. marts, hvis der bruges et kalenderår.

## <a name="additional-resources"></a>Yderligere ressourcer

Du kan finde flere oplysninger om konsolidering og valutaomregning i det overordnede emne til dette emne, [Oversigt over økonomiske konsolideringer og valutaomregning](./financial-consolidations-currency-translation.md).

Du kan få flere oplysninger om, hvordan du angiver oplysninger om konsolideringer online, under [Økonomiske konsolideringer online](./consolidate-online.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]