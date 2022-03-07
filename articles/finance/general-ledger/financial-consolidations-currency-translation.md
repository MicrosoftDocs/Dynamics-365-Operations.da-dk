---
title: Oversigt over økonomiske konsolideringer og valutaomregning
description: I dette emne beskrives økonomisk konsolideringer og valutaomregning i Finans.
author: jiwo
ms.date: 10/07/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: a77fe5e1970c617203706d9d629ac65e3a47909b
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2022
ms.locfileid: "7982399"
---
# <a name="financial-consolidations-and-currency-translation-overview"></a>Oversigt over økonomiske konsolideringer og valutaomregning

[!include [banner](../includes/banner.md)]

Dette emne gennemgår den fremgangsmåde, som både Microsoft Dynamics 365 Finance og Økonomirapportering bruger til konsolideringer. Emnet indeholder scenarier, der vedrører rapportering i flere regnskaber, aggregering, eliminering og minoritetsinteresse. Det forklarer også, hvordan du håndterer særlige situationer, f.eks. scenarier, hvor juridiske enheder har forskellige regnskabsperioder eller forskellige kontoplaner.

Dette emne er skrevet for brugere og funktionelle konsulenter, og det antages, at læserne har et generelt kendskab til Finance og Økonomirapportering. Grundlæggende opsætning er ikke omfattet.

> [!NOTE]
> Betegnelsen *juridisk enhed* bruges i Finance, og udtrykket *regnskab* bruges i Økonomirapportering. Begge disse udtryk anvendes i dette emne. Men i dette emne har de samme betydning.

## <a name="audience"></a>Målgruppe
Dette emne er beregnet til brugere af økonomi- og regnskabsbrugere og programkonsulenter, som vil bruge Finans og rapportering og Økonomirapportering til at konsolidere flere regnskaber og data med flere valutaer.

## <a name="approach"></a>Fremgangsmåde
Finance bruger en særskilt juridisk enhed til at behandle en konsolidering. Det anvender en enkelt forekomst til konsolidering, men giver mulighed for at hente data fra andre kilder. Konsolideringsprocessen skal køres, hver gang der foretages ændringer i kildens juridiske enheder.

Økonomirapportering kan konsolidere flere regnskaber under oprettelse af rapporter. Selvom dataene gemmes i et datamarked, er versionsspecifikke og kan eksporteres, er hvert kilderegnskab ejer af og container for dataene. Rapporten kan køres når som helst, selv hvert minut (for eksempel). Den giver mange andre fordele, f.eks. muligheden for at finde frem til alle regnskaber og dimensioner.

Brugerne kan bruge Konsolider online, Økonomirapportering eller en kombination. Deres valg afhænger af behovene i virksomheden og deres revisorers præferencer.

## <a name="consolidations"></a>Konsolideringer
Modulet **Konsolideringer** indeholder indstillinger til konsolidering af flere juridiske enheder under konsolideringsprocessen og til import eller eksport af et regnskabs balance. Du kan også konfigurere elimineringer og bogføre elimineringskladder.

## <a name="benefits-of-using-consolidate-online"></a>Fordele ved at bruge Konsolider online
Kunder, der bruger modulet **Konsolideringer** får forskellige fordele:

- **Dybde på data** – Du kan oprette konsoliderede rapporter, der samler faktiske data og budgetdata på både kontoniveau og dimensionsniveau.
- **Dynamiske konsolideringer** – Konsolideringer, der kan udføres flere gange.
- **Overvågningsegenskaber** – Dimensioner og konti vedligeholdes til analyse og overvågning, og der oprettes saldi efter dato.
- **Valutaomregning** – Du kan konfigurere de kontointervaller og satser, der skal oversættes fra regnskabsvalutaen i kilderegnskabet til regnskabsvalutaen i det konsoliderede regnskab.
- **Behandle elimineringer i et konsolideret regnskab eller et elimineringsregnskab** – Du kan behandle og bogføre elimineringer som en enkelt proces under konsolidering. Du kan også køre forslag separat.

## <a name="supported-consolidation-scenarios"></a>Understøttede konsolideringsscenarier
Her er nogle af de konsolideringsscenarier, som Konsolider online understøtter:

- Enkeltniveaukonsolideringer på tværs af juridiske enheder
- Konsolideringer, der omfatter elimineringer
- Minoritetsinteresse (i dette scenarie skal der bruges manuel beregning og postering i regnskabet).
- Flere kontoplaner på tværs af juridiske enheder
- Forskellige regnskabskalendere på tværs af flere juridiske enheder
- Konsolideringer, der involverer flere rapporteringsvalutaer

## <a name="legal-entity-setup"></a>Opsætning af juridisk enhed
Før du behandler en konsolidering, skal du indstille den juridiske enhed. Du kan køre konsolideringen, så mange gange du ønsker, og alle data oversættes fra kilderegnskabets regnskabsvaluta til den valuta, der er defineret for det konsoliderede regnskab. Derfor hvis du for følgende organisationsstruktur skal oversætte alle nordamerikanske regnskaber til amerikanske dollar (USD) først og derefter til euro (EUR), som er valutaen i det overordnede regnskab, skal du have mindst to konsoliderede regnskaber.

![Organisationsstruktur.](./media/organizational-structure.png "Organisationsstruktur")

I den foregående organisationsstruktur skal du have en juridisk enhed for den nordamerikanske konsolidering, fordi konsolideringer altid konsolideres fra regnskabsvalutaen for kilderegnskabet til valutaen for det konsoliderede regnskab. Hvis alle firmaer i eksemplet er inkluderet i en enkelt konsolidering, bliver det mexicanske datterselskab oversat fra mexicanske pesos (MXN) til EUR, og ikke fra MXN til USD til EUR.

Når du opretter den juridiske enhed, kan du angive, om regnskabet bruges til både konsolideringsprocessen og elimineringsprocessen eller til blot en af disse processer. I følgende illustration bruges regnskabet til begge processer. Bemærk, at du ikke kan bogføre kassekladder i et konsolideret regnskab, men at du kan bogføre dem i et elimineringsregnskab. Derfor vil du måske gerne have et separat elimineringsregnskab.

![Juridisk enhed, der bruges til både konsolidering og eliminering.](./media/sep-elimination-company.png "Juridisk enhed, der bruges til både konsolidering og eliminering")

## <a name="main-accounts-and-consolidation-account-groups"></a>Hovedkonti og koncernkontogrupper
Du skal foretage et valg af, hvordan du vil konsolidere din kontoplan. Under konsolideringsprocessen har du tre muligheder for at konsolidere hovedkonti.

Den første mulighed er at bruge hovedkontiene fra kilderegnskaberne. I så fald konsolideres alle konti fra alle regnskaber. Eksempelvis hvis Kontant er kontoen 100000 i USMF-regnskabet og kontoen 1100 i DEMF-regnskabet, omfatter det konsoliderede regnskab begge konti. Hver konto har sin egen saldo.

Den anden mulighed er at angive en standardkoncernkonto på siden **Hovedkonti**. Kontoen knyttes derefter til koncernkontoen. Denne mulighed kan være nyttig, når du har forskellige kontoplaner eller skal oprette tilknytning til en plan, der er defineret af hovedkontoret.

![Standardkoncernkonto, der er angivet på siden Hovedkonti.](./media/main-accounts.png "Standardkoncernkonto, der er angivet på siden Hovedkonti")

Den tredje mulighed er at bruge koncernkontogrupper. Du kan definere så mange koncernkontogrupper, som du har brug for. På siden **Yderligere koncernkonti** skal du derefter knytte hovedkontoen fra kontoplanen til den konto, du har brug for til den pågældende gruppe.

![Tilknytning på siden Flere koncernkonti.](./media/additional-consolidation-accounts.png "Tilknytning på siden Flere koncernkonti")

## <a name="consolidating-online"></a>Konsolidering online
Du kan finde oplysninger om, hvordan du angiver oplysninger om konsolideringer online, under [Økonomiske konsolideringer online](./consolidate-online.md).

## <a name="managing-consolidation-transactions"></a>Administrere konsolideringstransaktioner
Du kan få vist resultaterne af konsolideringen på flere måder:

- Opret en økonomisk rapport forhold til det konsoliderede regnskab.
- Gennemse listesiden **Råbalance** i det konsoliderede regnskab.
- På listen over konsolideringstransaktioner på siden **Konsolideringer** kan du se de saldi, der oprettes efter dato for hvert kilderegnskab for hver periode.

    ![Konsolideringstransaktioner på siden Konsolideringer.](./media/managing-consolidation-transactions.png "Konsolideringstransaktioner på siden Konsolideringer")

Hvis du vil køre konsolideringen igen, kan du kun behandle konsolideringen. Alternativt kan du først vælge **Fjern transaktioner** på siden **Konsolideringer**.
I tilfælde af, at saldiene på den konsoliderede konto ikke nøjagtige, kan disse saldi rettes via siden **Justeringer af ultimoperiode**.

## <a name="consolidate-with-import"></a>Konsolider med import
Funktionen Konsolider med import fungerer som funktionen Konsolider online. Når du vælger de juridiske enheder, skal du browse til kildefilen, der indeholder dataene.

## <a name="export-company-balances"></a>Eksportér virksomhedssaldi
Funktionen Eksportér virksomhedssaldi fungerer også som funktionen Konsolider online. Når du vælger de juridiske enheder, skal du angive en filsti til outputtet.

## <a name="elimination-rules"></a>Elimineringsregler
Hvis du vil eliminere interne transaktioner, skal du oprette en elimineringsregel. Alternativt kan du manuelt angive en eliminering i et regnskab, som er angivet som elimineringsregnskab. Hvis du opretter en elimineringsregel, har du to mulige elimineringsmetoder: **Nettoændring** og **Fast**.

### <a name="set-up-elimination-rules"></a>Konfigurere elimineringsregler
Når du opretter elimineringsregler i Finance, kan du oprette en økonomisk dimension, der bruges specifikt med henblik på eliminering. De fleste kunder navngiver den økonomiske dimension **Samhandelspartner** eller lignende. Hvis du beslutter ikke at bruge en økonomisk dimension, skal du kontrollere, at du har hovedkonti, der kun bruges til interne transaktioner.

Du kan finde opsætningen for elimineringer i området **Opsætning** i modulet **Konsolideringer**. Når du angiver en beskrivelse af reglen, skal du vælge det regnskab, som elimineringskladden skal bogføres til. I det regnskab, du vælger, skal **Brug til økonomisk eliminering** være markeret i opsætningen af den juridiske enhed.

Du kan angive den dato, hvor elimineringsreglen træder i kraft, og den dato, hvor den udløber, efter behov. Hvis du vil have, at elimineringsreglen skal være tilgængelig i elimineringsforslagsprocessen, skal du indstille **Aktiv** til **Ja**. Vælg et kladdenavn af typen **Eliminering**.

![Grundlæggende egenskaber for en elimineringsregel.](./media/ledger-elimination-rule-journal.png "Grundlæggende egenskaber for en elimineringsregel")

Når du har defineret de grundlæggende egenskaber, skal du vælge **Linjer** for at definere de faktiske behandlingsregler. Der er to elimineringsmuligheder: Du kan eliminere nettoændringsbeløbet eller definere et fast beløb.

Vælg kildekontiene. Du kan bruge en stjerne (\*) som jokertegn. For eksemplet vælger **1\**_ alle konti, der starter med _* 1** som en datakilde til tildelingen.

Når du har valgt kildekontiene, skal du bruge feltet **Specifikation af regnskab** til at angive den konto, der bruges fra destinationsregnskabet. Vælg **Kilde** for at bruge den hovedkonto, der er defineret i kildekontoen. Hvis du vælger **Brugerdefineret**, skal du angive en destinationskonto.

![Elimineringsregellinje på siden Finans.](./media/ledger-elimination-rule-line.png "Elimineringsregellinje på siden Finans")

Feltet **Specifikation af dimension** fungerer som feltet **Specifikation af regnskab**. Vælg **Kilde** for at bruge de samme dimensioner i modtagervirksomheden og i kilderegnskabet. Hvis du vælger **Brugerdefineret**, skal du angive dimensionerne i modtagervirksomheden ved at vælge menupunktet **Destinationsdimensioner**. Vælg derefter de kildedimensioner og de økonomiske dimensioner og værdier, der bruges som kilde til elimineringen.

### <a name="process-elimination-transactions"></a>Anvend elimineringsposter
Der er to måder at behandle elimineringsposteringer på. Transaktionen kan behandles under Konsolidering online-processen, eller du kan oprette en elimineringskladde og køre elimineringsprocessen. Dette afsnit fokuserer på den anden af de to muligheder.

Vælg **Elimineringskladde** i modulet **Konsolideringer** i en virksomhed, der er defineret som et elimineringsregnskab. Når du har valgt navnet på kladden, skal du vælge **Linjer**. For at køre forslaget skal du vælge **Forslag** \> **Elimineringsforslag**.

Vælg det regnskab, der er kilden til de konsoliderede data, og vælg derefter den regel, der skal behandles. Angiv start- og slutdatoer for at definere det datointerval, der søges i efter elimineringsbeløb. Feltet **Finansposteringsdato** angiver den dato, der bruges til at bogføre kladden i finans. Når du vælger **OK**, kan du gennemse beløbene og bogføre kladden.

> [!NOTE]
> Elimineringskladden viser de beløb for kontoværdierne i valutaen for deres oprindelige transaktioner, og ikke i regnskabsvalutaen. Når du gennemser beløbene i elimineringskladden, kan du finde funktionsmåden forvirrende.

Du kan finde flere oplysninger og eksempler i [Elimineringsregler](./elimination-rules.md).

## <a name="currency-revaluation-in-a-consolidation-company"></a>Værdiregulering af valuta i et konsolideret regnskab
Når du konsoliderer data fra én regnskabsvalutaen til en anden, skal du stadig køre værdiregulering af valuta, hvis valutakurser ændres, så dine kontosaldi værdireguleres korrekt. Når du oprindeligt konsoliderer dataene, skal du bruge fanen **Valutaomregning** for at markere de første valutakurser, der skal bruges til oversættelse under konsolideringsprocessen. Når en ny valutakurs er angivet (f.eks. i den næste måned), skal du værdiregulere kontosaldiene. Urealiserede gevinster eller tab opdateres derefter baseret på den nye valutakurs og dato.

Du kan finde flere oplysninger om værdiregulering af valuta i et konsolideret regnskab i [Værdiregulering af valuta i et konsolideret regnskab](currency-revaluation-consolidation-company.md).

Du kan finde flere oplysninger om, hvordan værdireguleringen af valuta fungerer i modulet **Finans**, i [Værdiregulering af udenlandsk valuta for Finans](./foreign-currency-revaluation-general-ledger.md).

### <a name="additional-information"></a>Yderligere oplysninger
- Når konsolideringen er behandlet, konsolideres alle posteringslag.
- Elimineringskladder kan kun bogføres for det aktuelle lag.
- Kun saldi for driftsenheder konsolideres. Derfor for at få vist primosaldi skal du stadig køre en ultimo ved årsafslutning i det konsoliderede regnskab.
- Du kan bogføre en kassekladde i et elimineringsregnskab, men ikke i et konsolideret regnskab.
- Justeringer af saldi i et konsolideret regnskab kan kun foretages ved hjælp af siden **Justeringer af ultimoperiode**. 

## <a name="benefits-of-using-financial-reporting-for-financial-consolidations-and-currency-translation-or-to-complement-consolidate-online-for-consolidated-reporting"></a>Fordele ved at bruge Økonomirapportering til økonomiske konsolideringer og valutaomregning eller at supplere Konsolider online til konsolideret rapportering
Kunder, der bruger Økonomirapportering til økonomiske konsolideringer og valutaomregning eller at supplere Konsolider online til konsolideret rapportering, får en række forskellige fordele:

- **Dybde på data** – Du kan oprette konsoliderede rapporter, der samler faktiske data og budgetdata på både kontoniveau og dimensionsniveau. For Finance omfatter disse data data fra budgetstyring og budgetplanlægning.
- **Dynamiske konsolideringer** – Konsolideringer kan udføres når som helst og på alle niveauer i organisationshierarkiet.
- **Komplette overvågningsegenskaber** – Alle dimensioner, konti og posteringsoplysninger vedligeholdes til analyse og overvågning. Desuden indeholder Økonomirapportering fuld tilbagerulning til den oprindelige postering i enhver af de juridiske enheder, der er konsolideret.
- **Strømlinet valutaomregning** – Efter minimal opsætning i Finance kan du omregne enhver Økonomirapportering-rapport til enhver rapporteringsvaluta, som er blevet oprettet. Du kan desuden oprette et ubegrænset antal rapporteringsvalutaer.
- **Bogføre elimineringer ved kilden** – Du kan oprette og udskrive en elimineringsrapport for at kontrollere elimineringsposteringer. Derefter kan du bogføre enhver ny eliminering som standard interne transaktioner. Du kan også bruge en juridisk enhed til eliminering for enhver postering, du ikke ønsker i dine juridiske enheder.

## <a name="supported-consolidation-scenarios-for-financial-reporting"></a>Understøttede konsolideringsscenarier for Financial Reporting

Her er nogle af de konsolideringsscenarier, som Økonomirapportering understøtter:

- Konsolideringer på enkeltniveau og på flere niveauer på tværs af juridiske enheder
- Konsolideringer, der bruger organisationsstrukturer, der er oprettet ud fra juridiske enheder
- Konsolideringer, der omfatter elimineringer
- Minoritetsinteresse
- Flere kontoplaner på tværs af juridiske enheder
- Forskellige regnskabskalendere på tværs af flere juridiske enheder
- Konsolideringer, der involverer flere rapporteringsvalutaer
- Konsolideringer af virksomhedsenheder

## <a name="generating-consolidated-financial-statements"></a>Generere konsoliderede regnskaber
Oplysninger om scenarier, hvor du kan generere konsoliderede regnskaber, finder du i [Generere konsoliderede regnskaber](./generating-consolidated-financial-statements.md).

## <a name="performance-enhancement-for-large-consolidations"></a>Ydeevneforbedring for store konsolideringer

Miljøer med mange finanstransaktioner kan køre langsommere end det optimale. For at løse dette problem kan du konfigurere parallel behandling af batches, der bruger et brugerdefineret antal datoer. For at sikre, at løsningen fungerer efter hensigten, skal du føje et filtypepunkt til konsolideringen for at returnere en objektbeholder med datointervaller. Basisimplementeringen skal indeholde ét datointerval for start- og slutdatoen for konsolideringen. Datointervaller i basisimplementeringen valideres for at sikre, at de ikke indeholder huller eller overlap. Datointervaller bruges til at oprette parallelle batchbundter for hvert enkelt regnskab.

Du kan tilpasse antallet af datointervaller for at opfylde organisationens behov. Når du tilpasser antallet af datointervaller, kan du forenkle testen og minimere effekten på eksisterende kode, da der ikke findes nogen fordelingslogik. De eneste nye test, der kræves, validerer oprettelsen af batchbundter, validerer datointervaller og tester en delmængde af datointervaller for at kontrollere, at batchene kan samles til den endelige batchopgave. 

Denne funktion forbedrer konsolideringsprocessen i Finans, når processen køres i et batch. Forbedringerne øger ydeevnen af processen til konsolidering af finansmodulet ved at opdele konsolideringen i flere opgaver, der kan behandles parallelt. I standardmetoden til kørsel af en konsolidering behandler hver opgave otte dage med brug af finansaktiviteten. Der er dog tilføjet et udvidelsespunkt, hvor du kan tilpasse de nummeropgaver, der oprettes.

Før du kan bruge denne funktion, skal den være slået til i dit system. Administratorer kan bruge området **Funktionsstyring** til at kontrollere funktionens status og slå den til efter behov. Dér vises funktionen på følgende måde:

- **Modul:** Finans
- **Funktionsnavn:** Ydeevneforbedring for store konsolideringer

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
