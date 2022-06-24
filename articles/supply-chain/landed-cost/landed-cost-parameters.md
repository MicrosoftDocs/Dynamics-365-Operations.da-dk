---
title: Opsætning af parametre for landingsomkostninger
description: Denne artikel beskriver, hvordan du kan konfigurere generelle oplysninger og konfigurationsindstillinger, der bruges på tværs af modulet Landingsomkostninger til bogføring, statusopdateringer, nummerserier og funktionalitet.
author: Weijiesa
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 99dbe17d4e83c2c75d52ca3fd22a1772d8045355
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871972"
---
# <a name="landed-cost-parameters-setup"></a>Opsætning af parametre for landingsomkostninger

[!include [banner](../../includes/banner.md)]

Du bruger siden **Parametre for landingsomkostninger** til at konfigurere generelle oplysninger og konfigurationsindstillinger, der bruges på tværs af modulet **Landingsomkostninger** til bogføring, statusopdateringer, nummerserier og funktionalitet. Konfigurationen af parametre deles på tværs af juridiske enheder og kan redigeres af en administrator.

## <a name="open-the-landed-cost-parameters-page"></a>Åbne siden Parametre for landingsomkostninger

Hvis du vil arbejde med parametrene, skal du gå til **Landingsomkostninger \> Opsætning \> Parametre for landingsomkostninger** og derefter angive felterne som beskrevet i følgende undersektioner.

![Siden Parametre for landingsomkostninger.](media/landed-cost-parameters.png "Siden Parametre for landingsomkostninger")

## <a name="general-tab"></a>Fanen Generelt

### <a name="general-fasttab"></a>Oversigtspanelet Generelt

I følgende tabel beskrives de felter, der er tilgængelige under fanen **Generelt** i oversigtspanelet **Generelt** på siden **Parametre for landingsomkostninger**.

| Indstilling | Beskrivelse |
|---|---|
| Brug forsendelsessats | En forsendelsessats angives for en defineret periode og bruges til forkalkulerede omkostninger for varer, der bruger flere valutaer. Angiv denne indstilling til *Ja*, hvis du vil bruge en forsendelsessats. |
| Valutakurstype | Den standardsamling af valutakurser, der bruges til beregninger af flere valutaer for en fragt og fragtomkostninger. |
| Opdater indkøbsordreantallet | Vælg, hvad der skal ske, hvis en bruger ændrer antallet på en indkøbsordrelinje:<ul><li>**Acceptér** – Fragtantallet justeres automatisk.</li><li>**Advarsel** – Hvis linjen er tilknyttet en fragt, vises en advarsel, men fragtantallet opdateres.</li><li>**Fejl** – Hvis linjen er tilknyttet en fragt, vises en fejlmeddelelse, og indkøbsordren kan ikke opdateres. Ordrelinjen skal derfor først fjernes fra fragten.</li></ul> |
| Opdater antal kartoner automatisk | Når denne indstilling er angivet til *Ja*, lægges alle kartoner sammen og vises på fragt- og containerniveau. Når den er angivet til *Nej*, angives antallet af kartoner som udgangspunkt til 0 (nul), og det kan redigeres manuelt efter behov. |

### <a name="costing-fasttab"></a>Oversigtspanelet Efterkalkulation

I følgende tabel beskrives de felter, der er tilgængelige under fanen **Generelt** i oversigtspanelet **Efterkalkulation** på siden **Parametre for landingsomkostninger**.

| Indstilling | Beskrivelse |
|---|---|
| Bogføringsspecifikation | Vælg værdireguleringen i Finans:<ul><li>**Total** – Et totalbeløb bogføres i finansmodulet.</li><li>**Varegruppe** – Reguleringen angives pr. varegruppe.</li><li>**Varenummer** – Reguleringen angives pr. vare. Denne værdi indeholder flest detaljer.</li></ul> |
| Tillad nul omkostninger | Angiv denne indstilling til *Nej* for at vise en fejl, hvis en bruger forsøger at bogføre et omkostningsestimat for en fragtfaktura eller indkøbsordre, der ikke indeholder en værdi for den forventede fragtomkostning. Fejlmeddelelsen viser, at der ikke kan fordeles en omkostning på 0 (nul), og at fakturabogføringen mislykkes. I dette tilfælde kan brugeren opdatere estimatet manuelt (eller genkonfigurere den automatiske omkostning) og derefter enten trække den opdaterede værdi ind eller slette omkostningen, hvis den ikke gælder.<p>Angiv denne indstilling til *Ja*, hvis du vil tillade, at fragtomkostningen er tom. I dette tilfælde vil der blive tildelt en pris på 0 (nul) i henhold til omkostningsområdet. Derefter kan en kreditorkostfaktura behandles i forhold til nulpriskostomkostningen, når fragten modtages.</p><p>Det anbefales, at du konfigurerer estimatet i den automatiske omkostningspost for at forhindre, at en nulprisomkostning vises. Selvom dette estimat ikke er helt korrekt, skulle det stadig være mere nøjagtigt end en antaget nulomkostning.</p> |
| Bogføringsdato for regulering | Når du bogfører en kreditorkostprisfaktura for fragt, opdateres udligningstabellen (lagerreguleringer) også. Vælg den dato, der er angivet som standard på siden **Vælg fragtomkostninger**, mens du er i fakturakladden:<ul><li>**Transaktionsdato** – Brug kladdedatoen (transaktionsdatoen).</li><li>**Fakturadato for indkøbsordre** – Brug den økonomiske bogføringsdato for lagerbeholdningsfakturaen (indkøbsordren).</li><li>**Valgt dato** – Brugeren kan angive en bogføringsdato. Selvom datoen kan være tom, hvis den stadig er tom, når omkostningsfakturaen bogføres, modtager brugeren en fejl.</li></ul> |
| Brug indkøbsfakturabilag | Når denne indstilling er angivet til *Ja*, bruger omkostningsperiodiseringens transaktioner samme bilagsnummer, som bruges til indkøbsfakturaen. Når den er angivet til *Nej*, bruger systemet det næste tilgængelige nummer til nummerserien **Bilag til omkostningsperiodisering**, der er konfigureret under fanen **Nummerserier** på siden **Parametre for landingsomkostninger**.<p>Denne indstilling har kun virkning, når indstillingen **Bogfør på omkostningskontoen i finans** er angivet til *Ja* under fanen **Faktura** på siden **Kreditorparametre**.</p> |
| Bloker manuel bogføring på clearingkonto | Angiv denne indstilling til *Ja* for at forhindre bogføring på clearingkonti, hvor transaktionen ikke er kædet sammen med en fragt, ved at vælge **Funktioner \> Vælg fragtomkostninger** i handlingsruden for kreditorfakturakladden. Det anbefales, at du angiver denne indstilling til *Ja*, så fragt- og clearingkontoen kan udlignes korrekt. |
| Brug gebyrperiodiseringskonto for omkostningstypen | Når denne indstilling er angivet til *Ja*, bruges den periodiseringskonto til gebyr, der er konfigureret for den relevante omkostningstypekode på siden **Omkostningstypekoder**, til at periodisere omkostninger som en udgift.<p>Denne indstilling har kun virkning, når indstillingen **Bogfør på omkostningskontoen i finans** er angivet til *Ja* under fanen **Faktura** på siden **Kreditorparametre**. |
| Bogfør reguleringer som afvigelse | Når denne indstilling er angivet til *Ja*, tilsidesætter den standardfunktionaliteten og tvinger de lagerreguleringstransaktioner, der er relateret til afvigelser mellem forkalkulerede omkostninger og faktiske omkostninger, til at blive bogført på en afvigelseskonto.<p>Når denne indstilling er angivet til *Nej*, håndteres de lagerreguleringstransaktioner, der vedrører afvigelser, på basis af konfigurationen af efterkalkulationsmetoden og koden for omkostningstypen. I forbindelse med standardomkostninger bogføres afvigelser stadig på kontoen for afvigelser. For glidende vægtet gennemsnit (WMA) bogføres afvigelser enten på afvigelseskontoen eller lageret.</p><p>Denne indstilling har kun virkning, når indstillingen **Bogfør på omkostningskontoen i finans** er angivet til *Ja* under fanen **Faktura** på siden **Kreditorparametre**.</p> |

### <a name="validation-fasttab"></a>Oversigtspanelet Validering

I følgende tabel beskrives de felter, der er tilgængelige under fanen **Generelt** i oversigtspanelet **Validering** på siden **Parametre for landingsomkostninger**.

| Indstilling | Beskrivelse |
|---|---|
| Fakturaer med flere omkostninger | Vælg, hvad der skal ske, hvis mere end én faktura behandles i forhold til en fragt, folio eller container for det samme gebyr.<ul><li>**Acceptér** – Systemet skal tillade flere omkostningsfakturaer.</li><li>**Advarsel** – Der vises en advarsel.</li><li>**Fejl** - Der vises en fejlmeddelelse.</li></ul> |
| Flere leverandører pr. database | Vælg, hvad der skal ske, hvis der føjes mere end én leverandørs indkøbsordrer til en folio.<ul><li>**Acceptér** – Systemet skal tillade handlingen.</li><li>**Advarsel** – Der vises en advarsel, men handlingen kan stadig udføres.</li><li>**Fejl** – Der vises en fejlmeddelelse, og handlingen forhindres.</li></ul><p>Din toldagent eller lokale love kan give mandat til en bestemt værdi i dette felt.</p> |
| Tolerance for flere leveringsmåder | Vælg, hvad der skal ske, hvis varer fra en indkøbsordre, der bruger en anden leveringsmåde end fragten, føjes til denne fragt.<ul><li>**Acceptér** – Systemet skal tillade handlingen.</li><li>**Advarsel** – Der vises en advarsel, men handlingen kan stadig udføres.</li><li>**Fejl** – Der vises en fejlmeddelelse, og handlingen forhindres.</li></ul> |
| Tolerance for flere lagersteder | Vælg, hvad der skal ske, hvis en fragt omfatter flere ordrelinjer, som skal leveres til forskellige lagersteder. Disse ordrelinjer kan spredes ud over en eller flere indkøbsordrer.<ul><li>**Acceptér** – Systemet skal tillade handlingen.</li><li>**Advarsel** – Der vises en advarsel.</li><li>**Fejl** - Der vises en fejlmeddelelse.</li></ul> |
| Manglende volumen | Vælg, hvad der skal ske, hvis en bruger føjer en vare uden volumen til en fragt.<ul><li>**Acceptér** – Systemet skal acceptere varen.</li><li>**Advarsel** – Der vises en advarsel.</li><li>**Fejl** - Der vises en fejlmeddelelse.</li></ul><p>Hvis der bruges volumen til beregning og fordeling af omkostninger, anbefales det, at du vælger enten *Advarsel* eller *Fejl*.</p> |
| Tjenesteudbyder uden ruteomkostninger | Vælg, hvad der skal ske, hvis en bruger forsøger at behandle en faktura for en serviceudbyder, der ikke er tilknyttet en fragt. <ul><li>**Acceptér** – Systemet skal tillade handlingen.</li><li>**Advarsel** – Der vises en advarsel.</li><li>**Fejl** - Der vises en fejlmeddelelse.</li></ul><p>Det anbefales, at du vælger *Advarsel*.</p> |

### <a name="defaults-fasttab"></a>Oversigtspanelet Standarder

I følgende tabel beskrives de felter, der er tilgængelige under fanen **Generelt** i oversigtspanelet **Standarder** på siden **Parametre for landingsomkostninger**.

| Indstilling | Beskrivelse |
|---|---|
| Kladdenavn | Vælg den standardkladde, som funktionen *Opret modtagelseskladde* skal bruge. |
| Fragtstatus | Vælg den status, som fragten skal have, før brugerne kan konfigurere en forsendelsescontainer til leje i systemet. Denne handling finder typisk sted, når varerne er i transit eller dokken. |
| Ruteskabelon | Vælg den standardrejseskabelon, der skal bruges til nye lejeforsendelsescontainere. Du skal normalt vælge en rejseskabelon, der indeholder lejeomkostninger. |
| Bevægelse | Hvis over-/underantallet for en levering ligger inden for den definerede tolerance, behandles der automatisk en bevægelseskladde. Vælg den bevægelseskladde, der skal bruges som standard. Feltet **Modkonto** for navnet på den valgte bevægelseskladde skal have en værdi. |
| Overførsel | Når en underlevering behandles, vil det korte tilgangsantal blive overført til et underleveringslagersted. Vælg den overførselskladde, der skal bruges som standard. |
| Deaktiver indkøbsordrer uden rute | Deaktiver funktionen for over-/underlevering af landingsomkostninger for indkøbsordrer, der ikke er tilknyttet en fragt. |
| Deaktiver indkøbsordrer for ikke varer i transit | Deaktiver funktionen for over-/underlevering af landingsomkostninger for indkøbsordrer, der ikke bruger varer i transit. |
| Frist for overtilgang for varer i transit | Angiv, hvor mange dage efter den første modtagelse af en forsendelsescontainer, der stadig kan fuldføres yderligere overtilgang for den pågældende forsendelsescontainer. |

## <a name="status-updates-tab"></a>Fanen Statusopdateringer

Systemet bruger statusværdier til at angive status for hver fragt. Værdier af denne fragtstatus kan automatisk anvendes på fragter via fragtsporing eller periodiske batchjob. Du kan også anvende dem manuelt ved at åbne fragten og derefter vælge en status i gruppen **Fragtopdatering** under fanen **Administrer** i handlingsruden. 

Du kan oprette lige så mange fragtstatusværdier, som du vil. Men fire af dem skal defineres som anvendt til et bestemt formål under fanen **Statusopdateringer** på siden **Parametre for landingsomkostninger**. I følgende tabel forklares de felter, der er tilgængelige her.

| Indstilling | Beskrivelse |
|---|---|
| Efterkalkuleret | Vælg den fragtstatus, der angiver, at en fragt er blevet færdiggjort. |
| I transit | Vælg den fragtstatus, der angiver, at en fragt er i transit. |
| Klar til efterkalkulation | Vælg den fragtstatus, der angiver, at en fragt er klar til efterkalkulation. Denne status bruges, når alle lagerindkøbsfakturaer og fragtkostfakturaer, hvor feltet **Kredit på fragtomkostning** er angivet til *Kreditor*, er behandlet for fakturaen. De fragter, der mislykkes i den efterkalkulerede proces, vil have statussen *Klar til efterkalkulation*.|
| Efterkalkuleret på forhånd | Vælg den fragtstatus, der angiver, at en fragt er ved at blive efterkalkuleret på forhånd. Denne status bruges, når en ny omkostningstransaktion føjes til en fragt, når den allerede er efterkalkuleret. Der kan føjes nye omkostningstransaktioner til en tidligere efterkalkuleret fragt, når der modtages endnu en fragtfaktura eller et uventet overliggegebyr. Denne status anvendes automatisk, når der føjes en ny fragtomkostning til en efterkalkuleret fragt. |

## <a name="voyage-creator-tab"></a>Fanen Fragtopretter

Følgende tabel indeholder en beskrivelse af afsnittene under fanen **Fragtopretter** på siden **Parametre for landingsomkostninger**.

| Sektion | Beskrivelse |
|---|---|
| Tolerancer | I felterne **Tolerance for overvolumen** og **Tolerance for overvægt** defineres tærskler, over hvilke varer betragtes som overvolumen og overvægt. Når en bruger tilføjer varer på siden **Fragteditor**, vises der en advarsel, hvis volumen eller vægt overstiger den værdi, du angiver her. Værdien for de enkelte felter er udtrykt som en procentdel af den maksimale volumen eller vægt, der er angivet for den relevante forsendelsescontainertype. Det anbefales, at værdien er mellem 5 og 10 procent af den maksimale volumen eller vægt. |
| Opsætning af databaseoprettelse | Systemet kan oprette flere folioer under oprettelsen af fragten. Du kan bruge dette afsnit til at definere, hvornår der skal oprettes en ny folio. For hver række i denne sektion kontrollerer systemet den angivne tabel og det angivne felt og opretter en folio for hver entydige feltværdi. |

## <a name="cost-estimates-tab"></a>Fanen Omkostningsestimater

Fanen **Omkostningsestimater** på siden **Parametre for landingsomkostninger** indeholder kun ét felt: **Standardefterkalkulationsversion**. Dette felt gælder kun, når efterkalkulationsmetoden er *Standardefterkalkulation*. Vælg den standardefterkalkulationsversion, der skal bruges til den periodiske opgave *Opdatering af varens kostpris*. Du skal muligvis ændre denne indstilling, hver gang et nyt regnskabsår begynder.

## <a name="inventory-dimensions-tab"></a>Fanen Lagerdimensioner

Du kan bruge fanen **Lagerdimensioner** på siden **Parametre for landingsomkostninger** til at styre, hvilke tilgængelige lagerdimensioner der som standard skal vises på de enkelte sider for landingsomkostninger, hvor dimensionerne anvendes.

Vælg en dimension, og angiv derefter indstillingen **Fragtlinjer**, **Varer i transit** og/eller **Omkostningsestimater** til *Ja* for hver side, hvor dimensionen skal vises som standard. Gentag dette trin for andre dimensioner efter behov.

Indstillingerne under denne fane opretter standarddimensionerne for hver angivet side på tværs af juridiske enheder. Men brugere, der arbejder på en af de angivne sider, kan tilsidesætte standarddimensionerne ved at vælge **Lager \> Vis dimensioner** i handlingsruden.

## <a name="number-sequences-tab"></a>Fanen Nummerserier

Fanen **Nummerserier** på siden **Parametre for landingsomkostninger** viser de enkelte typer referencenummerserier, som landingsomkostninger kræver, men som ikke deles på tværs af juridiske enheder. Vælg en nummerseriekode for hver reference på listen.

> [!NOTE]
> I en konfiguration med flere virksomheder skal der oprettes forskellige nummerserier for hver virksomhed (juridisk enhed).

## <a name="shared-number-sequences-tab"></a>Fanen Delte nummerserier

Fanen **Delte nummerserier** på siden **Parametre for landingsomkostninger** viser de enkelte typer referencenummerserier, som deles på tværs af juridiske enheder for landingsomkostninger. Der findes i øjeblikket kun én nummerserie på listen. Denne nummerserie bruges til fragt-id'et.

På siden **Alle fragter** kan brugere se alle fragter på tværs af alle juridiske enheder. Hvis du vil redigere og behandle en fragt, skal du dog være i den juridiske enhed for den valgte post.

## <a name="feature-visibility-tab"></a>Fanen Funktionssynlighed

Landingsomkostninger føjer funktioner (felter og funktioner) til flere sider, der ofte bruges i Microsoft Dynamics 365 Supply Chain Management. Disse sider omfatter sider, der er relateret til kreditormasterdata, frigivne produkter, indkøbsordrer, flytteordrer og lagerstedsopsætning. Hvis du bruger landingsomkostninger, skal du gøre disse funktioner synlige overalt, før du kan udnytte dem. Hvis du ikke bruger Landingsomkostninger, kan du skjule funktionerne for at holde dem ude af vejen.

Under fanen **Funktionssynlighed** på siden **Parametre for landingsomkostninger** skal du angive indstillingen **Aktivér** til *Ja* for at gøre funktioner for landingsomkostninger synlige alle de steder, hvor de er tilgængelige. Angiv den til *Nej* for at skjule funktionerne på almindelige sider uden for Landingsomkostninger. Men selv når indstillingen er angivet til *Nej*, vil selve modulet, herunder siden **Parametre for landingsomkostninger**, stadig være tilgængeligt for brugere, der har de korrekte adgangstilladelser til den.
