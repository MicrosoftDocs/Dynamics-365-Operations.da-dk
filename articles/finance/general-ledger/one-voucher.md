---
title: Ét bilag
description: Ét bilag til økonomikladder (finanskladde, anlægsaktivkladde, kreditorbetalingskladde osv.) giver dig mulighed for at angive flere reskontrotransaktioner i forbindelse med et enkelt bilag.
author: kweekley
ms.date: 11/05/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerParameters, AssetProposalDepreciation
audience: Application User
ms.reviewer: roschlom
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-03-16
ms.dyn365.ops.version: 8.0.2
ms.openlocfilehash: e98f1803e43df0fbd5ab700b959faaeee017b7a9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834494"
---
# <a name="one-voucher"></a>Ét bilag

[!include [banner](../includes/banner.md)]


## <a name="what-is-one-voucher"></a>Hvad er Ét bilag?

Den eksisterende funktion til økonomikladder (finanskladde, anlægsaktivkladde, kreditorbetalingskladde osv.) giver dig mulighed for at angive flere reskontrotransaktioner (debitor, kreditor, anlægsaktiver, projekt og bank) samlet i et enkelt bilag. Microsoft refererer til denne funktion som *Ét bilag*. Du kan oprette et enkelt bilag ved hjælp af en af følgende metoder:

- Angiv kladdenavnet (**Finans** \> **Kladdeopsætning** \> **Kladdenavne**), så feltet **Nyt bilag** indstilles til **Kun ét bilagsnummer**. Hver linje, du føjer til kladden, inkluderes nu på det samme bilag. Derfor kan bilaget angives som et bilag med flere linjer, som en konto/modkonto på samme linje eller som en kombination.

    [![Enkelt linje](./media/same-line.png)](./media/same-line.png)

    > [!IMPORTANT]
    > Definitionen af Ét bilag omfatter **ikke** tilfælde, hvor kladdenavne er angivet som **Kun ét bilagsnummer**, og hvor brugeren derefter angiver et bilag, som kun omfatter finanskontotyper. I dette emne betyder Ét bilag, at der er er et enkelt bilag, der indeholder mere end én kreditor, debitor, bank, ét anlægsaktiv eller projekt.

- Angiv et bilag med flere linjer, hvor der ikke er nogen modkonto.

    [![Bilag med flere linjer](./media/Multi-line.png)](./media/Multi-line.png)

- Angiv et bilag, hvor både på kontoen og modkontoen indeholder en reskontrokontotype, som f.eks. **Kreditor**/**Kreditor**, **Debitor**/**Debitor**, **Kreditor**/**Debitor** eller **Bank**/**Bank**.

    [![Reskontrobilag](./media/subledger.png)](./media/subledger.png)

## <a name="issues-with-one-voucher"></a>Problemer med ét bilag

Funktionen ét bilag forårsager problemer under udligning, momsberegning, tilbageførsel af postering, afstemning af en reskontrokladde til Finans, regnskabsaflæggelse og meget mere. (Du kan finde flere oplysninger om problemer, der kan opstå under udligning, f.eks. i [Enkelt bilag med flere debitor- eller kreditorposter](https://docs.microsoft.com/dynamics365/finance/accounts-payable/single-voucher-multiple-customer-vendor-records).) For at kunne fungere og rapportere korrekt kræver disse processer og rapporter transaktionsdetaljer. Selvom nogle scenarier stadig kan fungere korrekt, afhængigt af organisationens opsætning, er der ofte problemer, når flere posteringer angives i ét bilag.

Du bogfører f.eks. følgende bilag med flere linjer.

[![Eksempel på et samkøbsbilag](./media/example.png)](./media/example.png)

Du genererer derefter rapporten **Udgifter efter kreditor** i arbejdsområdet **Økonomisk indsigt**. I denne rapport er udgiftskontosaldi grupperet under kreditorgruppe og derefter kreditor. Når rapporten genereres, kan systemet ikke bestemme, hvilke kreditorgrupper/kreditorer der medførte udgiften på 250,00. Da der mangler transaktionsdetaljer, antager systemet, at hele udgiften på 250,00 vedrører den første kreditor, der findes i bilaget. Derfor vises udgiften på 250,00, der er inkluderet i saldoen for hovedkontoen 600120, under den pågældende kreditorgruppe/kreditor. Det er dog meget sandsynligt, at den første kreditor i bilaget ikke er den korrekte kreditor. Derfor er rapporten sandsynligvis forkert.

[![rapport over udgifter efter kreditor](./media/expenses.png)](./media/expenses.png)

## <a name="the-future-of-one-voucher"></a>Fremtiden for ét bilag

På grund af de problemer, der kan forekomme, når der bruges ét bilag, vil denne funktion med tiden blive frarådet. Men da der er nogle funktionsmæssige kløfter, som er afhængige af denne funktion, udfases funktionen ikke på én gang. I stedet bruges følgende tidsplan:

- **Versionen foråret 2018** – Denne funktion var deaktiveret som standard via parameteren **Tillad flere transaktioner i ét bilag** under fanen **Generelt** på siden **Finansparametre**. Men du kan aktivere funktionen igen, hvis organisationen har et scenario, der falder i et af de funktionsmæssige kløfter, der er angivet senere i dette emne.

    - Hvis der ikke kræves ét bilag i dit forretningsscenarie, anbefales det, at du lader funktionen være deaktiveret. Hvis denne funktion bruges, selvom der findes en anden løsning, retter Microsoft ikke "fejl" i de områder, der identificeres senere i dette emne.
    - Vi anbefaler, at du stopper med at bruge ét bilag til integrationer i , medmindre funktionen er påkrævet til et af de dokumenterede funktionelle kløfter.

- **Senere versioner** – Flere af disse forretningskrav kan kun opfyldes ved hjælp af ét bilag. Microsoft skal sikre, at alle de identificerede forretningskrav stadig kan opfyldes i systemet, når funktionaliteten frarådes. Derfor vil der sandsynligvis skulle tilføjes nye funktioner for at udfylde funktionelle kløfter. Microsoft kan ikke tilbyde en bestemt løsning, da de enkelte funktionskløfter er forskellige og skal evalueres ud fra forretningsbehovet. Nogle funktionelle kløfter vil sandsynligvis blive erstattet af funktioner, der er med til at opfylde bestemte forretningsbehov. Andre huller kan dog udfyldes ved fortsat at gøre det muligt at angive oplysninger i en kladde, som ved anvendelse af ét bilag, men systemet kan efterhånden spore flere detaljer efter behov.

Når alle funktionelle kløfter er udfyldt, kommunikerer Microsoft, at det frarådes at bruge funktionen. Afskrivningen vil dog ikke være gældende i mindst ét år efter den pågældende kommunikation. Selvom Microsoft ikke kan give et præcist estimat over, hvornår funktionen Ét bilag frarådes, vil der højst sandsynligt gå to år, før afskrivningen finder sted. Microsofts politik er at holde mindst 12 måneder mellem ofring af forældet funktionalitet og den faktiske afskrivning, så kunder og uafhængige softwareleverandører har tid til at reagere på ændringen. For eksempel skal en organisation muligvis opdatere forretningsprocesser, enheder og integrationer.

Når ét bilag afskrives, er det en vigtig ændring, der kommunikeres i vidt omfang. Som en del af denne kommunikation vil Microsoft opdatere dette emne, skrive et blog-opslag på Microsoft Dynamics 365 Finance-bloggen, opdatere emnet "Fjernede eller forældet funktioner", kommunikere ændringen på det relevante Microsoft-websted osv.

## <a name="why-use-one-voucher"></a>Hvorfor bruge ét bilag?

Baseret på samtaler med kunderne, har Microsoft samlet følgende liste over de scenarier, hvor kunderne bruger funktionen ét bilag, eller årsager til at de bruger den. Nogle af disse forretningskrav kan kun opfyldes ved hjælp af ét bilag. Men i mange situationer kan alternativer opfylde de samme forretningsbehov.

### <a name="scenarios-that-require-one-voucher"></a>Scenarier, der kræver ét bilag

Følgende scenarier kan kun udføres ved hjælp af funktionen ét bilag. Hvis din organisation har et af disse scenarier, skal du aktivere flere transaktioner, der skal angives i et bilag, ved at ændre indstillingen af parameteren **Tillad flere transaktioner i ét bilag** på siden **Finansparametre**. Disse funktionsmæssige huller udfyldes via andre funktioner i senere versioner.

> [!Note]
> [For hver af følgende situationer skal **Tillad flere posteringer inden for ét bilagsfelt** være angivet til Ja i oversigtspanelet **Generelt** på siden **Finansparametre**.]

### <a name="post-vendor-or-customer-payments-in-summary-form-to-a-bank-account"></a>Bogføre kreditor- eller debitorbetalinger i oversigtsform til en bankkonto

**Scenario** En organisation sender en liste over kreditorer og beløb til banken, og banken bruger denne liste til at betale kreditorerne på organisationens vegne. Banken bogfører summen af betalinger som et enkelt træk på bankkontoen.

Opsummering af kreditorbetalinger understøttes kun via ét bilag. Hver kreditor angives som en separat linje for at bevare detaljer i kreditorreskontroen. Dog modposteres det opsummerede beløb for alle betalinger på en enkelt linje for bankkontoen. Derfor vises trækket som et enkelt opsummeret beløb i bankreskontroen.

**Scenario** En organisation indbetaler debitorbetalinger, eller banken indbetaler debitorbetalinger på organisationens vegne, og indbetalingen vises som et engangsbeløb på bankkontoen.

Opsummering af debitorbetalinger understøttes typisk via indbetalingsfunktionen. Men hvis du bruger "mellemkonto" på betalingsmåden, understøttes denne situation kun via ét bilag. Debitorbetalinger angives på samme måde, der er beskrevet for opsummering af kreditorbetaling.

### <a name="mechanism-to-group-transactions-from-a-business-event"></a>Mekanisme til at gruppere transaktioner fra en forretningshændelse

**Scenario** En organisation har en enkelt forretningshændelse, der udløser flere transaktioner. Men regnskabsafdelingen ønsker at få vist regnskabsposterne sammen for at opnå en bedre revisionsegnethed.

Hvis en organisation skal have vist regnskabsposterne fra en forretningshændelse sammen, skal den bruge ét bilag. 

### <a name="country-specific-features"></a>Landespecifikke funktioner

**Scenario** Funktionen et enkelt administrativt dokument (SAD) for Polen kræver i øjeblikket, at der bruges et enkelt bilag. Indtil en indstilling for gruppering er tilgængelig for denne funktion, skal du fortsætte med at bruge funktionen ét bilag. Der kan være flere landespecifikke funktioner, der kræver funktionen ét bilag.

### <a name="customer-prepayment-payment-journal-that-has-taxes-on-multiple-lines"></a>Betalingskladde for debitorforudbetaling med moms på flere "linjer"

I dette scenario er debitorerne i det enkelte bilag den samme debitor, fordi transaktionen simulerer linjerne i en debitorordre. Forudbetalingen skal angives i et enkelt bilag, da beregningen af moms skal foretages på "linjerne" i den individuelle betaling, som debitoren har foretaget.

### <a name="customer-reimbursement"></a>Debitorrefusion

**Scenario** En debitor foretager en forudbetaling for en ordre, og linjerne i ordren har forskellige momsbeløb, der skal registreres for forudbetalingen. Den forudbetalte debitorbetaling er én postering, der simulerer linjerne i ordren, så den relevante moms kan registreres for beløbet på hver linje.

Hvis den periodiske refusionsopgave køres fra debitormodulet, oprettes der en postering for at flytte saldoen fra en debitor til en kreditor. I dette scenario skal Ét bilag bruges til at refundere kunden.

### <a name="fixed-asset-maintenance-catch-up-depreciation-split-asset-calculate-depreciation-on-disposal"></a>Vedligeholdelse af anlægsaktiver: Catch-up-afskrivning, opdelt aktiv, beregne afskrivning ved salg
De følgende anlægsaktivposteringer kan også oprette flere transaktioner i et enkelt bilag:

- Der foretages en yderligere anskaffelse til et aktiv, og "catch-up"-afskrivning beregnes.
- Et aktiv opdeles.
- En parameter til at beregne afskrivning på kassation aktiveres, og derefter kasseres anlægsaktivet.
- Et aktivs servicedato ligger før anskaffelsesdatoen. Derfor bogføres en afskrivningsregulering.

> [!Note]
> Når du indtaster transaktioner, skal du kontrollere, at alle transaktioner gælder for det samme anlægsaktiv. Bilaget bogføres ikke, hvis det indeholder mere end ét anlægsaktiv, selvom feltet **Nyt bilag** kun er angivet som ét bilagsnummer på siden **Kladdenavne** i Finans. Hvis du medtager mere end ét anlægsaktiv i bilaget, vises meddelelsen **Der kan kun være én anlægsaktivpostering pr. bilag**, og du kan ikke bogføre bilaget.  

### <a name="bills-of-exchange-and-promissory-notes"></a>Veksler og egenveksler
Veksler og egenveksler kræver, at Ét bilag bruges, fordi posteringerne flytter debitor- eller kreditorsaldoen fra én debitor/konti- finanskonto til en anden, baseret på status for betalingen.

## <a name="scenarios-that-dont-require-one-voucher"></a>Scenarier, der ikke kræver ét bilag

Følgende scenarier kan opnås på andre måder og bør ikke bruge funktionen Ét bilag.

### <a name="post-customer-payments-in-summary-form-to-the-bank-account"></a>Bogføre debitorbetalinger i oversigtsform til bankkontoen

En organisation indbetaler debitorbetalinger, eller banken indbetaler debitorbetalinger på organisationens vegne, og indbetalingen vises som et engangsbeløb på bankkontoen.

Opsummering af debitorbetalinger understøttes via funktionen indbetaling, når "mellemkontoen" ikke bruges på betalingsmåden.

### <a name="netting"></a>Modregning

I modregning modregnes saldi for kreditor og debitor mod hinanden, fordi kreditoren og kunden er den samme part. Denne fremgangsmåde minimerer udveksling af penge mellem en organisation og parten debitor/kreditor.

Modregning kan foretages ved at angive stigningen og faldet i separate bilag og derefter bogføre forskydningen på en clearingsfinanskonto.

### <a name="post-in-summary-to-the-general-ledger"></a>Bogføre oversigt i Finans

Organisationer ønsker ofte at bogføre i finansmodulet i oversigtsform for at minimere mængden af data. Dog kræver de pågældende organisationerne stadig typisk, at transaktionsoplysningerne opretholdes. Når bogføringen foretages i oversigtsform via et enkelt bilag, er transaktionsdetaljerne ikke kendt, og de kan ikke vedligeholdes.

- Da posteringsdetaljerne i øjeblikket ikke kan vedligeholdes, anbefales det, at organisationen ikke bruger **Ét bilag** til bogføring af oversigtsformularen.
- Når support for Ét bilag er fjernet, kan strukturerne Kildedokument og Regnskab implementeres i kladderne. Disse strukturer vil derefter bevare transaktionsdetaljerne og understøtte opsummering i Finans.


### <a name="settle-multiple-unposted-payments-to-the-same-invoice"></a>Udligne flere ikke-bogførte betalinger til den samme faktura

Dette scenario findes som regel i organisationer, hvor kunderne kan bruge flere betalingsmåder til at betale for indkøb. I dette scenario skal organisationen kunne registrere flere ikke-bogførte betalinger og udligne dem mod debitorfakturaen.

En ny funktion, der blev tilføjet i Microsoft Dynamics 365 for Operations version 1611 (november 2016) giver mulighed for, at flere ikke-bogførte betalinger kan udlignes mod en enkelt faktura. Flere kundebetalinger behøver ikke længere at blive anført i et enkelt bilag.

### <a name="import-bank-statement-transactions"></a>Importere bankkontoudtogstransaktioner

Banker betaler og modtager ofte betalinger på vegne af en organisation, og disse transaktioner registreres i Finans via en fil, der modtages fra banken. Organisationer vil ofte gruppere disse transaktioner ved hjælp af bankkontonummeret i filen. Da hver transaktion vises med detaljer på bankens kontoudtog, kræves der ingen opsummering i bankreskontroen.

Transaktioner kan grupperes ved hjælp af andre felter i kladden, f.eks. selve kladdens batchnummer eller dokumentnummeret.


### <a name="transfer-balances"></a>Overfør saldi

En organisation er måske nødt til at overføre en balance fra en kreditor til en anden, enten på grund af en fejl, eller fordi en anden kreditor har overtaget passivet. Overførsler af denne type kan også ske til kontotyper som f.eks. **Debitorer** og **Bank**.

Saldooverførsler fra én konto (kreditor, debitor, bank osv.) til en anden konto kan foretages via separate bilag, og forskydningen kan bogføres på en clearingsfinanskonto.

### <a name="enter-beginning-balances"></a>Angive primosaldi.

Organisationer angiver ofte primosaldi for reskontrokonti (kreditorer, debitorer, anlægsaktiver og så videre) som en transaktion med ét bilag. Primosaldi for hver reskontrokonto kan angives som separate bilag, og forskydningen kan bogføres på en clearingsfinanskonto.

### <a name="correct-the-accounting-entry-of-a-posted-customer-or-vendor-document"></a>Rette regnskabsposten for et bogført debitor- eller kreditordokument

En organisation har muligvis brug for at rette debitor- eller kreditorkontoen i Finans for en regnskabspostering af en bogført faktura, men fakturaen kan ikke tilbageføres eller korrigeres gennem en anden mekanisme.

Hvis der skal foretages en korrektion af Debitor- eller Kreditorkontoen i Finans, skal der foretages en regulering direkte på finanskontoen. Reguleringen kan ikke foretages ved at bogføre via kreditoren eller debitoren. Denne metode kræver, at justeringen foretages under en "nedetid", så finanskontoen midlertidigt tillader manuel indtastning.

### <a name="the-system-allows-it"></a>"Systemet tillader det"

Organisationer bruger ofte udelukkende funktionen ét bilag, fordi systemet lader dem bruge den, uden at de forstår konsekvenserne.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]