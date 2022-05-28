---
title: Indtægts- og udgiftsudskydelser i abonnementsfakturering
description: Dette emne indeholder en forklaring på, hvordan du kan konfigurere udskydelse af indtægter og udgifter i Abonnementsfakturering.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 9a12cf52d904db0396aa9914b8e324060289710f
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8690942"
---
# <a name="revenue-and-expense-deferrals-in-subscription-billing"></a>Indtægts- og udgiftsudskydelser i abonnementsfakturering

Dette emne indeholder en forklaring på, hvordan du konfigurerer og bruger udskydelse af indtægter og udgifter i Abonnementsfakturering. Udskydelsesplaner er altid baseret på og afhænger af et underliggende oprindeligt dokument eller en faktureringsplan. Da de oprettes på basis af standardværdier, kan de ikke angives eller oprettes separat.

Processen til opsætning og brug af indtægts- og udgiftsudskydelser findes på flere sider:

- På siden **Udskydelsesparametre for indtægt og udgift** kan du definere firmaindstillingerne.
- På siden **Udskydelsesstandarder** kan du konfigurere de standardkonti og skabeloner, der bruges til udskydelsesplanerne.
- På siderne **Udskydelsesskabeloner** og **Hændelsesbaserede udskydelsesskabeloner** kan du definere de skabeloner, der bruges til udskydelsesplanerne.
- På siden **Alle udskydelsesplaner** kan du se og redigere en hvilken som udskydelsesplan.

Indtægts- og udgiftsudskydelser kan bruges sammen med tilbagevendende kontraktfakturering.

## <a name="revenue-and-expense-deferral-parameters"></a>Udskydelsesparameter til indtægter og udgifter

Siden **Udskydelsesparametre for indtægt og udgift** indeholder følgende felter.

| Felt | Beskrivelse |
|---|---| 
| Fanen **Tidsplan** | |
| Ens pr. periode | <p>Angiv, om antallet af dage i en periode bruges, når beløbet pr. periode beregnes for en udskydelsesplan:</p><ul><li>**Ja** – Beløbet for hver periode er det samme uanset antallet af dage i perioden. Delvise perioder (f.eks. perioder i starten eller slutningen af en udskydelsesplan) vil være forholdsmæssige.</li><li>**Nej** – Beløbet beregnes ud fra antal dage i hver periode.</li></ul><p>Du kan tilsidesætte denne indstilling på transaktionsniveau.</p> |
| Indstilling for udskydelse af salgsrabat | <p>Angiv, om der skal oprettes separate udskydelsesplaner til rabat- og salgsordrebeløbene:</p><ul><li>**Separat rabatplan** – Rabatbeløbet holdes adskilt fra indtægtsbeløbet.<p>I dette tilfælde oprettes der to udskydelsesplaner, når en salgsordre oprettes og derefter bogføres. Rabat- og indtægtsbeløbene bogføres på forskellige udskydelseskonti.</p></li><li>**Flet rabat med indtægt** – Rabatbeløbet kombineres med indtægtsbeløbet. Der oprettes én udskydelsesplan, og både rabatbeløbet og indtægtsbeløbet bogføres på samme udskydelseskonto.<p>I dette tilfælde oprettes der én udskydelsesplan, når en salgsordre oprettes og derefter bogføres. Både rabatbeløbet og indtægtsbeløbet bogføres på samme udskydelseskonto.</p></li></ul><p>**Bemærk:** Hvis du vil anvende rabatter på varer, der bruger funktionen for ikke-faktureret indtægt, skal du vælge indstillingen **Separat plan for rabat**. Rabatter kan derefter anvendes på alle varer, uanset om funktionen for ikke-faktureret indtægt anvendes. Hvis indstillingen **Flet rabat med indtægt** er valgt, kan rabatter ikke anvendes på varer, der bruger funktionen for ikke-faktureret indtægt.</p> |
| Indstilling for udskydelse af indkøbsrabat | <p>Angiv, om der skal oprettes separate udskydelsesplaner til rabat- og indkøbsordrebeløb:</p><ul><li>**Separat rabatplan** – Rabatbeløbet holdes adskilt fra udgiftsbeløbet.<p>I dette tilfælde oprettes der to udskydelsesplaner, når en indkøbsordre oprettes og derefter bogføres. Rabat- og udgiftsbeløbene bogføres på forskellige udskydelseskonti.</p></li><li>**Flet rabat med udgift** – Rabatbeløbet kombineres med udgiftsbeløbet. Der oprettes én udskydelsesplan, og både rabatbeløbet og udgiftsbeløbet bogføres på samme udskydelseskonto.<p>I dette tilfælde oprettes der én udskydelsesplan, når en indkøbsordre oprettes og derefter bogføres. Både rabatbeløbet og udgiftsbeløbet bogføres på samme udskydelseskonto.</p></li></ul> |
| Konsolider tidligere perioder | <p>Angiv, om du vil konsolidere udskydelsesplanlinjer for tidligere perioder:</p><ul><li>**Ja** – Hvis den startdatoen for udskydelse ligger i en periode før transaktionsdatoen, kombineres alle beløb op gennem perioden for transaktionsdatoen i en enkelt udskydelsesplanlinje.</li><li>**Nej** – Beløbene fra alle perioder holdes på separate udskydelsesplanlinjer.<p>Hvis udskydelsens startdato er i samme periode som eller en senere periode end transaktionsdatoen, har denne indstilling ingen virkning.</p></li></ul><p>Denne indstilling kan opdateres på transaktionsniveau.</p> |
| Startdato for standardudskydelse | <p>Vælg den regel, der skal bruges til at bestemme startdatoen for udskydelsesplanen:</p><ul><li>**Transaktionsdato** – Brug transaktionsdatoen som startdato.</li><li>**Starten af den aktuelle måned** – Brug den første i den aktuelle måned som startdato. Hvis transaktionsdatoen er den første i en måned, er den første i den aktuelle måned startdatoen.</li><li>**Starten af næste måned** – Brug den første i næste måned som startdato. Hvis transaktionsdatoen er den første, bruges transaktionsdatoen. Ellers bruges den første i næste måned.</li><li>**Regel 15** – Hvis transaktionsdatoen er mellem den første og den 15. dag, skal du bruge den første i den aktuelle måned som startdato. Hvis transaktionsdatoen er den 16. dag eller senere i en måned, er den første i næste måned startdatoen.</li></ul><p>Denne indstilling kan opdateres på transaktionsniveau.</p> |
| Kortsigtet udskydelsesmetode | <p>Vælg den kortsigtede udskydelsesmetode: **Ingen**, **Rullende perioder** eller **Fast år**.</p><p>|
| Bogføringsmetode for udskydelse | <p>Vælg den metode, der bruges til at oprette udskydelsestransaktioner.</p><ul><li>**Balance** – Brug metoden til bogføring af transaktion til at oprette udskydelsestransaktioner.</li><li>**Drift** – Brug driftsbogføringsmetoden til at oprette udskydelsestransaktioner. Når transaktioner er bogført, kan du gennemse fakturabilaget for at få vist de ekstra poster, der afstemmer de første førte beløb og modbeløb.</li></ul> |
| Tilbageføre overskud og tab ved kredit | <p>**Bemærk:** Dette felt er kun tilgængeligt, når feltet **Bogføringsmetode for udskydelse** er angivet til **Drift**.</p><p>Angiv, om driftsbeløbene skal tilbageføres, når der anvendes en tilbageførsel, afslutning eller refusion på en faktureringsplan eller salgsordre:</p><ul><li>**Ja** – Tilbagefør driftsbeløbene, og anvend et kreditreguleringsbeløb på udskydelsesplanen.<p>Hvis tilbageførslen sker halvvejs i en faktureringsperiode, er beløbene forholdsmæssige.</p></li><li>**Nej** – Der oprettes ingen tilbageførselstransaktion for drift, når der anvendes en tilbageførsel, afslutning eller refusion på en faktureringsplan eller salgsordre.</li></ul> |
| Fanen **Indregning** | |
| Bogfør finanskladder automatisk | <p>Angiv, om kladdeposter, der oprettes af indtægts- og udgiftsudskydelser, automatisk bogføres:</p><ul><li>**Ja** – Bogfør automatisk kladdeposter, der oprettes af indtægts- og udgiftsudskydelser.<p>**Tip:** Hvis du vælger **Ja**, kan du hjælpe med at forhindre, at der opstår bogføringsuoverensstemmelser, som skyldes manuelle ændringer af bilag.</p></li><li>**Nej** – Bogfør ikke automatisk kladdeposter, der oprettes af indtægts- og udgiftsudskydelser. Du skal bogføre kladder manuelt.</li></ul> |
| Opsummér føringskladder | <p>Angiv, om føringsbilag skal konsolideres som standard:</p><ul><li>**Ja** – Opret et enkelt bilag til alle de føringslinjer, der har samme dato. Alle linjer i et bilag, der har samme konto, konsolideres på én enkelt linje.</li><li>**Nej** – Opret et bilag for hver enkelt føringslinje.</li></ul><p>Du kan opdatere denne indstilling på siden **Føringsbehandling**.</p> |
| Standardkladdenavn | Vælg kladdenavnet til kladder, der er oprettet ud fra indtægts- og udgiftsudskydelsesprocesser, f.eks. føringsbehandling. |
| Beskrivelse af føringskladdelinje | <p>Vælg den beskrivelse, der skal vises i beskrivelsen af kladdebilagslinjen:</p><ul><li>**Planlinjedatoer** – Få vist planlinjedatoerne i kladdelinjebeskrivelsen.</li><li>**Oplysninger om oprindelig transaktion** – Vis de oprindelige transaktionsoplysninger i kladdelinjebeskrivelsen.<p>**Eksempel:** USMF-0001, CIV-00839, Softwareindtægt</p></li></ul> |
| Fanen **Nummerserier** | Brug denne fane til at angive standardværdierne for nummerserier til leasing. Guiden til generering af nummerserier bruges til automatisk at generere og tildele nummerserier. Du behøver ikke ændre nummerserien, medmindre du vil foretage manuelle ændringer af de genererede nummerserier. |
| Tidsplannummer | Den nummerserie, der bruges til udskydelsesplaner. |

## <a name="deferral-templates"></a>Udskydelsesskabeloner

Du kan bruge siden **Udskydelsesskabeloner** til at definere lineære skabeloner, der bruges til udskydelsesplaner.

Her er nogle af fordelene ved at bruge en skabelon:

* Længden af udskydelsen beregnes automatisk.
* Du tillader udskydelsesplaner, der har perioder, hvor føringen springes over.
* Du kan automatisere udskydelser ved at tildele skabelonen til et produkt, en produktgruppe, en produktkategori, kunder eller en kundegruppe. Skabelontildeling udføres fra siden **Udskydelsesstandarder**.

Der findes flere periodefrekvenser til skabeloner: dagligt, månedligt eller regnskabsperiode.

Skabelonlinjerne består af en type (**Ført** eller **Sprunget over**) og periodelængden. Linjer, der springes over, har et beløb på 0 (nul) på udskydelsesplanlinjerne. Denne funktionsmåde kan være nyttig, hvis du ikke vil føre indtægter i alle perioder.

### <a name="create-a-deferral-template"></a>Oprette en udskydelsesskabelon

Følg disse trin for at oprette en udskydelsesskabelon.

1. På siden **Udskydelsesskabeloner** skal du vælge **Ny**.
2. Angiv et navn i feltet **Skabelon**.
3. Indtast en beskrivelse i feltet **Beskrivelse**.
4. Vælg periodefrekvensen i feltet **Periodefrekvens**.
5. Vælg **Tilføj** for at tilføje en linje øverst på listen over linjer, eller vælg **Føj til** for at føje en linje til bunden af listen.
6. Vælg periodetypen i feltet **Type**.
7. Angiv længden af perioden i feltet **Periodelængde**.
8. Gentag trin 5 til 7 for hver ekstra linje, du skal bruge.
9. Vælg **Gem**.

## <a name="deferral-defaults"></a>Udskydelsesstandarder

Du kan bruge siden **Udskydelsesstandarder** til at oprette standardudskydelseskonti til varer og tildele standardskabeloner til varer, der kan udskydes. Du kan også oprette udskydelseskonti til gebyrer og tildele skabeloner til udskydelsesgebyrerne.

**Udskyd efter vare**

For transaktioner, der har en vare (f.eks. salgsordrer), kan du knytte konti og skabeloner til specifikke varer og kunder. Disse indstillinger bruges som standardværdier, når en transaktion udskydes. For at gøre transaktionen udskydelig som standard, skal du konfigurere varerne på siden **Varer, der kan udskydes**.

**Udskyd efter konto**

For transaktioner, der ikke har varer (f.eks. finanskladder), kan du angive udskydelseskontiene. Når disse konti bruges på en transaktionslinje, markeres transaktionen automatisk som udskudt. Transaktionslinjen tildeles den tilknyttede skabelon og føringskonto.

**Alle transaktionstyper (f.eks. under fanerne Salgsordre, Indkøb og Finanskladde).**

Kontiene på siden er de hovedkonti, der ikke har økonomiske dimensioner. De økonomiske dimensioner for føringskontoen er fra kunden eller varen, baseret på din organisation.

Hver skabelonlinje skal enten have en lineær skabelon eller en hændelsesbaseret skabelon. Den kan ikke have begge dele.

### <a name="for-sales-orders"></a>For salgsordrer

Benyt følgende fremgangsmåde for at angive standardværdierne for udskudte salgsordrer.

1. Vælg udskydelsestypen under fanen **Salgsordre**.
2. Vælg **Tilføj** for at tilføje en linje.
3. Vælg varekoden i feltet **Varekode**. Varekoden bestemmer, hvordan standardværdierne for udskydelse anvendes.
4. Angiv, hvordan varekoden anvendes:

    * Hvis feltet **Varekode** er angivet til **Tabel** eller **Gruppe**, skal du vælge varerelationen i feltet **Varerelation**.
    * Hvis feltet **Varekode** er angivet til **Kategori**, skal du vælge kategorirelationen i **Kategorirelation**.
    * Hvis feltet **Varekode** er angivet til **Alle**, gælder standardværdierne for alle relevante poster.

5. Angiv, hvordan kontokoden anvendes:

    * Hvis feltet **Kontokode** er angivet til **Tabel** eller **Gruppe**, skal du vælge kontorelationen i feltet **Kontorelation**.
    * Hvis feltet **Kontokode** er angivet til **Alle**, gælder kontoen for alle poster.

6. Vælg hovedkontoen for udskydelsen i feltet **Hovedkonto**.
7. Hvis feltet **Bogføringsmetode for udskydelse** er angivet til **Drift**,skal du vælge den første indtægtskonto i feltet **Første indtægtskonto** og indtægtsmodkontoen i feltet **Indtægtsmodkonto**.
8. Hvis feltet **Kortsigtet udskydelsesmetode** er angivet til **Rullende perioder** eller **Fast år**, skal du vælge den kortfristede udskydelseskonto i feltet **Kortsigtet udskydelseskonto**.
9. Du kan vælge **Tilføj** for at tilføje en linje i en skabelon.
10. Vælg varekoden i feltet **Varekode**.
11. Angiv, hvordan varekoden anvendes:

    * Hvis feltet **Varekode** er angivet til **Tabel** eller **Gruppe**, skal du vælge varerelationen i feltet **Varerelation**.
    * Hvis feltet **Varekode** er angivet til **Kategori**, skal du vælge kategorirelationen i feltet **Kategorirelation**.
    * Hvis feltet **Varekode** er angivet til **Alle**, gælder standardværdierne for alle relevante poster.

12. Angiv, hvordan kontokoden anvendes:

    * Hvis feltet **Kontokode** er angivet til **Tabel** eller **Gruppe**, skal du vælge kontorelationen i feltet **Kontorelation**.
    * Hvis feltet **Kontokode** er angivet til **Alle**, gælder kontoen for alle relevante poster.
    * Vælg den lineære skabelon i feltet **Lineær skabelon** eller den hændelsesbaserede skabelon i feltet **Hændelsesbaseret skabelon**.

13. Vælg **Gem**.

### <a name="for-purchase-orders"></a>For indkøbsordrer

Benyt følgende fremgangsmåde for at angive standardværdierne for udskudte indkøbsordrer.

1. Vælg udskydelsestypen under fanen **Indkøb**.
2. Vælg **Tilføj** for at tilføje en linje.
3. Vælg varekoden i feltet **Varekode**.
4. Angiv, hvordan varekoden anvendes:

    * Hvis feltet **Varekode** er angivet til **Tabel** eller **Gruppe**, skal du vælge varerelationen i feltet **Varerelation**.
    * Hvis feltet **Varekode** er angivet til **Kategori**, skal du vælge kategorirelationen i feltet **Kategorirelation**.
    * Hvis feltet **Varekode** er angivet til **Alle**, gælder standardværdierne for alle relevante poster.

5. Angiv, hvordan kontokoden anvendes:

    * Hvis feltet **Kontokode** er angivet til **Tabel** eller **Gruppe**, skal du vælge kontorelationen i feltet **Kontorelation**.
    * Hvis feltet **Kontokode** er angivet til **Alle**, gælder kontoen for alle relevante poster.

6. Vælg hovedkontoen for udskydelsen i feltet **Hovedkonto**.
7. Hvis feltet **Bogføringsmetode for udskydelse** er angivet til **Drift**,skal du vælge den første indtægtskonto i feltet **Første indtægtskonto** og indtægtsmodkontoen i feltet **Indtægtsmodkonto**.
8. Hvis feltet **Kortsigtet udskydelsesmetode** er angivet til **Rullende perioder** eller **Fast år**, skal du vælge den kortfristede udskydelseskonto i feltet **Kortsigtet udskydelseskonto**.
9. Vælg **Tilføj** for at tilføje en linje i en skabelon. 
10. Vælg varekoden i feltet **Varekode**.
11. Angiv, hvordan varekoden anvendes:

    * Hvis feltet **Varekode** er angivet til **Tabel** eller **Gruppe**, skal du vælge varerelationen i feltet **Varerelation**.
    * Hvis feltet **Varekode** er angivet til **Kategori**, skal du vælge kategorirelationen i feltet **Kategorirelation**.
    * Hvis feltet **Varekode** er angivet til **Alle**, gælder standardværdierne for alle relevante poster.

12. Angiv, hvordan kontokoden anvendes:

    * Hvis feltet **Kontokode** er angivet til **Tabel** eller **Gruppe**, skal du vælge kontorelationen i **Kontorelation**.
    * Hvis feltet **Kontokode** er angivet til **Alle**, gælder kontoen for alle relevante poster.
    * Vælg den lineære skabelon i feltet **Lineær skabelon** eller den hændelsesbaserede skabelon i feltet **Hændelsesbaseret skabelon**.

13. Vælg **Gem**.

### <a name="for-general-journals"></a>For finanskladder

Benyt følgende fremgangsmåde for at angive standardværdierne for udskudte finanskladdeposter.

1. Vælg fanen **Finanskladde**.
2. Vælg **Tilføj** for at tilføje en linje i en udskydelse.
3. Hvis feltet **Kortsigtet udskydelsesmetode** er angivet til **Rullende perioder** eller **Fast år**, skal du vælge den kortfristede udskydelseskonto i feltet **Kortsigtet udskydelseskonto**.
4. Vælg udskydelseskontoen i feltet **Udskydelseskonto**.
5. Vælg føringskontoen i feltet **Føringskonto**.
6. Hvis feltet **Bogføringsmetode for udskydelse** er angivet til **Drift**,skal du vælge den første indtægtskonto i feltet **Første indtægtskonto** og indtægtsmodkontoen i feltet **Indtægtsmodkonto**.
7. Vælg den lineære skabelon i feltet **Lineær skabelon** eller den hændelsesbaserede skabelon i feltet **Hændelsesbaseret skabelon**.
8. Vælg **Gem**.

### <a name="for-free-text-invoices"></a>For fritekstfakturaer

Benyt følgende fremgangsmåde for at angive standardværdierne for udskudte fritekstfakturaer.

1. Vælg fanen **Fritekstfaktura**.
2. Vælg **Tilføj** for at tilføje en linje i en udskydelse.
3. Angiv, hvordan kontokoden anvendes:

    * Hvis feltet **Kontokode** er angivet til **Tabel** eller **Gruppe**, skal du vælge kontorelationen i feltet **Kontorelation**.
    * Hvis feltet **Kontokode** er angivet til **Alle**, gælder kontokoden for alle relevante poster.

4. Vælg udskydelseskontoen i feltet **Udskydelseskonto**.
5. Hvis feltet **Kortsigtet udskydelsesmetode** er angivet til **Rullende perioder** eller **Fast år**, skal du vælge den kortfristede udskydelseskonto i feltet **Kortsigtet udskydelseskonto**.
6. Vælg føringskontoen i feltet **Føringskonto**.
7. Hvis feltet **Bogføringsmetode for udskydelse** er angivet til **Drift**,skal du vælge den første indtægtskonto i feltet **Første indtægtskonto** og indtægtsmodkontoen i feltet **Indtægtsmodkonto**.
8. Vælg den lineære skabelon i feltet **Lineær skabelon** eller den hændelsesbaserede skabelon i feltet **Hændelsesbaseret skabelon**.
9. Vælg **Gem**.

### <a name="for-invoice-journals"></a>For fakturakladder

Benyt følgende fremgangsmåde for at angive standardværdierne for udskudte fakturakladdeposter.

1. Vælg fanen **Fakturakladde**.
2. Vælg **Tilføj** for at tilføje en linje i en udskydelse.
3. Angiv, hvordan kontokoden anvendes:

    * Hvis feltet **Kontokode** er angivet til **Tabel** eller **Gruppe**, skal du vælge kontorelationen i feltet **Kontorelation**.
    * Hvis feltet **Kontokode** er angivet til **Alle**, gælder kontokoden for alle relevante poster.

4. Vælg udskydelseskontoen i feltet **Udskydelseskonto**.
5. Hvis feltet **Kortsigtet udskydelsesmetode** er angivet til **Rullende perioder** eller **Fast år**, skal du vælge den kortfristede udskydelseskonto i feltet **Kortsigtet udskydelseskonto**.
6. Vælg føringskontoen i feltet **Føringskonto**.
7. Hvis feltet **Bogføringsmetode for udskydelse** er angivet til **Drift**,skal du vælge den første indtægtskonto i feltet **Første indtægtskonto** og indtægtsmodkontoen i feltet **Indtægtsmodkonto**.
8. Vælg den lineære skabelon i feltet **Lineær skabelon** eller den hændelsesbaserede skabelon i feltet **Hændelsesbaseret skabelon**.
9. Vælg **Gem**.

### <a name="items-that-are-deferred-by-default"></a>Varer, der som standard er udskudt

Brug siden **Varer udskudt som standard** til at definere, hvilke varer der som standard skal udskydes. Du kan angive de transaktionstyper, som varerne skal udskydes for. Du kan angive, om en enkelt vare skal udskydes, eller om en hel varegruppe eller kategori.

Når du konfigurerer varer som udskudt, skal du vælge standardkonti og skabeloner på siden **Udskydelsesstandarder**. Hvis konti og skabeloner ikke er valgt, bliver transaktionslinjer, hvor de pågældende varer indtastes, ikke udskudt.

For varer, der er udskudt på baggrund af den salgs- eller indkøbskategori, de er tilknyttet, er udskydelsesindstillingerne baseret på kategorien. Men hvis kategorien ikke er valgt i **Kategorirelation**-feltet, bruges udskydelsesindstillingerne for den kategori, der er højere rangeret. Du kan f.eks. tilføje en salgskategori **Hjemmevideo**, men ikke en salgskategori for **TV**. Når du tilføjer en udskydelsesvare, der er knyttet til kategorien **TV**, bruges udskydelsesindstillingerne for **Hjemmevideo** for varen.

### <a name="set-up-deferred-items"></a>Konfigurere udskudte varer

Hvis du vil konfigurere varer, der som standard er udskudt, skal du følge disse trin.

1. Vælg den ønskede fane på siden **Varer, der er udskudt som standard**: **Salgsordre** eller **Indkøb**.
2. Vælg **Tilføj** for at tilføje en linje.
3. Vælg varekoden i feltet **Varekode**.
4. Angiv, hvordan varekoden anvendes:

    * Hvis feltet **Varekode** er angivet til **Tabel** eller **Gruppe**, skal du vælge varerelationen i feltet **Varerelation**.
    * Hvis feltet **Varekode** er angivet til **Kategori**, skal du vælge kategorirelationen i feltet **Kategorirelation**.

5. Gentag trin 2 til 4 for hver ekstra linje, du skal bruge.
6. Vælg **Gem**.

## <a name="deferred-charges"></a>Udskudte gebyrer

Du kan bruge siden **Udskudte gebyrer** til at definere, hvilke gebyrer der som standard udskydes.

> [!NOTE]
> * I øjeblikket er udskudte gebyrer kun tilgængelige for salgsordrer.
> * Gebyrer kan kun udskydes på linjeniveau. Hvis du vil udskyde et gebyr på salgsordrehovedniveau, kan du konfigurere gebyret som en udskudt vare på en separat linje i salgsordren.
> * Hvis du vil udskyde et gebyr for en fritekstfaktura, skal du angive gebyret som en separat udskudt fakturalinje.
> * Denne funktionalitet er ikke tilgængelig for supportgebyrer og funktionen til opdeling af indtægt.

### <a name="set-up-deferred-charges"></a>Konfigurere udskudte gebyrer

Følg disse trin for at konfigurere udskudte gebyrer.

1. På siden **Udskudte gebyrer** skal du vælge **Tilføj** for at tilføje en linje.
2. I feltet **Gebyrkode** skal du vælge gebyrkoden.
3. I feltet **Gebyrrelation** skal du vælge gebyrrelationen.
4. Gentag trin 1 til 3 for hver ekstra linje, du skal bruge.
5. Vælg **Gem**.

## <a name="event-based-deferral-templates"></a>Hændelsesbaserede udskydelsesskabeloner

Brug siden **Hændelsesbaserede udskydelsesskabeloner** til at definere hændelsesbaserede udskydelsesskabeloner, du kan bruge i udskydelsestransaktioner og tildele på siden **Udskydelsesstandarder**.

### <a name="create-an-event-based-template"></a>Oprette en hændelsesbaseret skabelon

Følg disse trin for at oprette en hændelsesbaseret udskydelsesskabelon.

1. På siden **Hændelsesbaserede udskydelsesskabeloner** skal du vælge **Ny**.
2. Angiv et entydigt navn til skabelonen i feltet **Skabelon**.
3. Indtast en beskrivelse i feltet **Beskrivelse**.
4. Vælg fordelingstypen i feltet **Fordelingstype**.

    * **Variabelt beløb** – Tildel et specifikt beløb for hver linje, der indtastes.
    * **Lige stort beløb** – Tildel det samme beløb for hver linje, der indtastes. 
    * **Procent** – Tildel et beløb på basis af den procentværdi, der er angivet for hver linje.
    * **Færdiggørelsesgrad** – Tildel en akkumuleret færdiggørelsesværdi til hver linje, der indtastes.
    * **Variabelt antal** – Tildel et specifikt antal for hver linje, der indtastes.

5. Angiv indstillingen **Opret separate hændelser pr. enhed** til **Ja**, hvis hver hændelseslinje skal opdeles ligeligt med antallet af enheder i fakturatransaktionen. Angiv det til **Nej**, hvis du ikke vil opdele hændelseslinjerne.
6. Vælg udløbskontoen i feltet **Udløbskonto**.
7. Vælg **Tilføj** for at tilføje en linje øverst på listen over linjer, eller vælg **Føj til** for at føje en linje til bunden af listen.
8. Indtast en beskrivelse af hændelsen i feltet **Beskrivelse**.
9. Hvis **Procent** er valgt som **Fordelingstype**, skal du angive fordelingsprocenten i feltet **Fordelingsprocent**. Procenten skal være mellem 0 (nul) og 100. Hvis du ikke udfylder feltet **Fordelingsprocent**, betragtes procenten som 0. Summen af alle procenter, der vises i feltet **Samlet procent** nederst på siden, skal være lig med 100.
10. Angiv det antal måneder, hændelsen er gyldig, i feltet **Måneder til udløb**. Udløbsdatoen for transaktionsudskydelsen angives automatisk på basis af denne værdi.
11. Markér afkrydsningsfeltet **Registrer, når der bogføres** for automatisk at føre indtægter, når transaktionen bogføres. Hvis du ikke markerer afkrydsningsfeltet, skal indtægten føres manuelt.
12. Vælg føringskontoen for hændelsen i feltet **Føringskonto**, hvis hændelsen bruger en anden konto end hele udskydelsesplanen. Dette felt bruges sammen med afkrydsningsfeltet **Registrer, når der bogføres**.
13. Gentag trin 7 til 12 for hver ekstra linje, du skal bruge.
14. Vælg **Gem**.
