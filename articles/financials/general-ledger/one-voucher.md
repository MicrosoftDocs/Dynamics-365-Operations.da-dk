---
title: "Ét bilag"
description: "Ét bilag til økonomikladder (finanskladde, anlægsaktivkladde, kreditorbetalingskladde osv.) giver dig mulighed for at angive flere reskontrotransaktioner i forbindelse med et enkelt bilag."
author: kweekley
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-03-16
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 9f996131830f9bd4efd534143b3fb761c5ccc756
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---

# <a name="one-voucher"></a>Ét bilag

[!INCLUDE [banner](../includes/banner.md)]

> [!NOTE]
>  Denne funktion bliver tilgængelig i Dynamics 365 for Finance and Operations version 8.0, der vil være tilgængelig i versionen foråret '18.   

<a name="what-is-one-voucher"></a>Hvad er "Ét bilag"?
======================

Den eksisterende funktion til økonomikladder (finanskladde, anlægsaktivkladde, kreditorbetalingskladde osv.) giver dig mulighed for at angive flere reskontrotransaktioner i forbindelse med et enkelt bilag. Vi refererer til denne funktion som "Ét bilag". Du kan oprette Ét bilag ved hjælp af en af følgende metoder:

-   Angiv kladdenavnet (**Finans** \> **Kladdeopsætning** \>**Kladdenavne**), så feltet **Nyt bilag** angives til **Kun ét bilagsnummer**. * Hver linje, du føjer til kladden, inkluderes nu på det samme bilag. Da hver linje føjes til det samme bilag, kan bilaget kan angives som et bilag med flere linjer, som en konto/modkonto på samme linje, eller som en kombination.

[![Enkelt linje](./media/same-line.png)](./media/same-line.png)
 
> [!IMPORTANT] 
> *  Bemærk, at definitionen af "Ét bilag" IKKE omfatter de kladdenavne, der er angivet som kun **Et bilagsnummer**, og brugeren angiver derefter et bilag, som kun omfatter finanskontotyper.  I dette dokument betyder "Ét bilag", at der er kun er bilag, der indeholder mere end en kreditor, debitor, bank, anlægsaktiv eller projekt. 

-   Angiv et bilag med flere linjer, hvor der ikke er nogen modkonto.

[![Bilag med flere linjer](./media/Multi-line.png)](./media/Multi-line.png)

-   Angiv et bilag, hvor både på kontoen og modkontoen indeholder en reskontrokontotype, som leverandør/leverandør, debitor/debitor, leverandør/debitor eller bank/bank.

[![Reskontrobilag](./media/subledger.png)](./media/subledger.png)

<a name="issues-with-one-voucher"></a>Problemer med ét bilag
=======================

Funktionen ét bilag forårsager problemer under udligning, momsberegning, afstemning af en reskontrokladde til Finans, regnskabsaflæggelse og meget mere. (Du kan f.eks. finde flere oplysninger om problemer, der kan opstå under udligning, i [Enkelt bilag med flere debitor- eller kreditorposter](https://docs.microsoft.com/en-us/dynamics365/unified-operations/financials/accounts-payable/single-voucher-multiple-customer-vendor-records).) For at kunne fungere og rapportere korrekt kræver disse processer og rapporter transaktionsdetaljer. Selvom nogle scenarier stadig kan fungere korrekt, baseret på organisationens opsætning, er der ofte problemer, når flere posteringer angives i ét bilag.

Du bogfører f.eks. følgende bilag med flere linjer.

[![Eksempel](./media/example.png)](./media/example.png)

Du genererer derefter rapporten **Udgifter efter kreditor** i arbejdsområdet **Økonomisk indsigt**. Rapporten grupperer udgiftskontosaldi under kreditorgruppe og derefter kreditor. Når du genererer rapporten, kan systemet ikke bestemme, hvilke kreditorgrupper/kreditorer der medførte udgiften på 250,00. Da der mangler transaktionsdetaljer, antager systemet at alle 250,00 vedrører den første kreditor, der findes i bilaget. De 250,00, der er inkluderet i saldoen for hovedkontoen 600120, vises derfor under den pågældende kreditorgruppe/kreditor. Det er meget sandsynligt, at den første kreditor i bilaget ikke var den korrekte kreditor, så rapporten er forkert.

[![Udgifter](./media/expenses.png)](./media/expenses.png)

<a name="the-future-of-one-voucher"></a>Fremtiden for ét bilag
=========================

På grund af de problemer, der tidligere blev nævnt, gøres funktionen ét bilag forældet. Men da der er funktionelle huller, der er afhængige af denne funktion, gøres funktionen ikke forældet på én gang. Vi bruger i stedet følgende tidsplan: 

- **Versionen foråret 2018** – Funktionen deaktiveres som standard via en parameter i Finans. Men du kan aktivere funktionen, hvis organisationen har et scenario, der falder i de huller i forretningsscenarier, der er angivet senere i dette emne.

  -   Hvis en kunde har et forretningsscenarie, der ikke kræver ét bilag, skal du ikke aktivere funktionen. Vi vil ikke rette "fejl" i de områder, der identificeres senere i dette emne, hvis denne funktion bruges, selvom der findes en anden løsning.

  -   Stop med at bruge ét bilag til integrationer i Microsoft Dynamics 365 Finance and Operations, medmindre funktionen er påkrævet til et af de funktionelle huller.

- **Efteråret 2018 og senere versioner** – De funktionelle huller bliver lukket. Når de funktionelle huller er blevet lukket, slås funktionen ét bilag permanent fra.

- > [!IMPORTANT]
  > Bemærk, at indstillingen **Kun ét bilagsnummer** IKKE er blevet fjernet fra opsætningen af kladdenavne.  Denne indstilling understøttes stadig, når bilaget kun indeholder kun finanskontotyper.  Debitorer skal være omhyggelige med denne indstilling, da bilaget ikke bogføres, hvis **Kun ét bilagsnummer** aktiveres, og der derefter angives mere end en debitor, kreditor, bank, anlægsaktiv eller projekt.  Debitorer kan stadig angive en blanding af kontotyper for reskontrokladder, f.eks. en betaling inden for et enkelt bilag, der indeholder kontotyper for kreditor/bank.  

<a name="why-use-one-voucher"></a>Hvorfor bruge ét bilag?
====================

Baseret på samtaler med kunderne, har vi samlet følgende liste over de scenarier, hvor kunderne bruger funktionen ét bilag, eller årsager til at de bruger den. Nogle af disse forretningskrav kan kun opfyldes ved hjælp af ét bilag. Men i mange situationer kan alternativer opfylde de samme forretningsbehov.

<a name="scenarios-that-require-one-voucher"></a>Scenarier, der kræver ét bilag
----------------------------------

Følgende scenarier kan kun udføres ved hjælp af funktionen ét bilag. Disse funktionelle huller udfyldes via andre funktioner i versionen efteråret 2018 og senere versioner.

-   **Bogføre kreditor- eller debitorbetalinger i oversigtsform til en bankkonto**

    -   En organisation sender en liste over kreditorer og beløb til banken, og banken bruger denne liste til at betale kreditorerne på organisationens vegne. Banken bogfører summen af betalinger som et enkelt træk på bankkontoen.

>   Opsummering af kreditorbetalinger understøttes kun via ét bilag. Hver kreditor angives som en separat linje for at bevare detaljer i kreditorreskontroen, men det opsummerede beløb for alle betalingerne modposteres på en enkelt linje for bankkontoen. Derfor vises trækket som et enkelt opsummeret beløb i bankreskontroen.

-   En organisation indbetaler debitorbetalinger, eller banken indbetaler debitorbetalinger på organisationens vegne, og indbetalingen vises som et engangsbeløb på bankkontoen.

>   Opsummering af debitorbetalinger understøttes typisk via indbetalingsfunktionen. Men hvis du bruger "mellemkonto" på betalingsmåden, understøttes denne situation kun via ét bilag. Debitorbetalinger angives på samme måde, der er beskrevet for opsummering af kreditorbetaling.

-   **Mekanisme til at gruppere transaktioner fra en forretningshændelse**

    -   En organisation har en enkelt forretningshændelse, der udløser flere transaktioner. Men regnskabsafdelingen ønsker at få vist regnskabsposterne sammen for at opnå en bedre revisionsegnethed.

>   Hvis en organisation skal have vist regnskabsposterne fra en forretningshændelse sammen, skal den bruge ét bilag. 

- **Landespecifikke funktioner**

  -   Funktionen et enkelt administrativt dokument (SAD) for Polen kræver i øjeblikket, at der bruges et enkelt bilag. Indtil en indstilling for gruppering er tilgængelig for denne funktion, skal du fortsætte med at bruge funktionen ét bilag. Der kan være flere landespecifikke funktioner, der kræver funktionen ét bilag.

- **Betalingskladde for debitorforudbetaling med moms på flere "linjer"**

  -   En debitor foretager en forudbetaling for en ordre, og linjerne i ordren har forskellige momsbeløb, der skal registreres for forudbetalingen. Den forudbetalte debitorbetaling er én postering, der simulerer linjerne i ordren, så den relevante moms kan registreres for beløbet på hver linje.

I dette scenario er debitorerne i det enkelte bilag den samme debitor, fordi transaktionen simulerer linjerne i en debitorordre. Forudbetalingen skal angives i et enkelt bilag, da beregningen af moms skal foretages på "linjerne" i den individuelle betaling, som debitoren har foretaget.

-   **Vedligeholdelse af anlægsaktiver: Catch-up-afskrivning, opdelt aktiv, beregne afskrivning ved salg**

De følgende anlægsaktivposteringer kan også oprette flere transaktioner inden for et enkelt bilag:
-   Der foretages en yderligere anskaffelse til et aktiv, og 'catch-up'-afskrivning beregnes.
-   Et aktiv opdeles.
-   En parameter til at beregne afskrivning på kassation er aktiveret, og derefter er anlægsaktivet kasseret.

<a name="scenarios-that-dont-require-one-voucher"></a>Scenarier, der ikke kræver ét bilag
----------------------------------------

Følgende scenarier kan opnås på andre måde og bør ikke bruge ét bilag.

-   **Bogføre debitorbetalinger i oversigtsform til bankkontoen**

En organisation indbetaler debitorbetalinger, eller banken indbetaler debitorbetalinger på organisationens vegne, og indbetalingen vises som et engangsbeløb på bankkontoen.

Opsummering af debitorbetalinger understøttes via funktionen indbetaling, når mellemkontoen ikke bruges på betalingsmåden.

-   **Modregning**

I modregning modregnes saldi for kreditor og debitor mod hinanden, fordi kreditoren og kunden er den samme part. Denne fremgangsmåde minimerer udveksling af penge mellem en organisation og parten debitor/kreditor.

Modregning kan foretages ved at angive stigningen og faldet i separate bilag og bogføre forskydningen på en clearingsfinanskonto.

-   **Bogføre oversigt i Finans**

Organisationer ønsker ofte at bogføre i finansmodulet i oversigtsform for at minimere mængden af data. Dog kræver organisationerne stadig typisk, at transaktionsoplysningerne opretholdes. Når bogføringen foretages i oversigtsform via et enkelt bilag, er transaktionsdetaljerne ikke kendt, og de kan ikke vedligeholdes.

   -   Da posteringsdetaljerne i øjeblikket ikke kan vedligeholdes, anbefales det, at ét bilag ikke bruges til bogføring af oversigt.
   -   Når support for ét bilag er fjernet, kan vi implementere strukturerne Kildedokument og Regnskab i kladderne. Disse strukturer vil derefter bevare transaktionsdetaljen og understøtte opsummering i Finans.

-   **Udligne flere ikke-bogførte betalinger til den samme faktura**

Dette scenario findes som regel i detailorganisationer, hvor kunderne kan bruge flere betalingsmåder til at betale for indkøb. I dette scenario skal organisationen kunne registrere flere ikke-bogførte betalinger og udligne dem mod debitorfakturaen.

En ny funktion, der blev tilføjet i Microsoft Dynamics 365 for Operations version 1611 (november 2016) giver mulighed for, at flere ikke-bogførte betalinger kan udlignes mod en enkelt faktura. Flere kundebetalinger behøver ikke længere at blive anført i et enkelt bilag.

-   **Importere bankkontoudtogstransaktioner**

Banker betaler og modtager ofte betalinger på vegne af en organisation, og disse transaktioner registreres i Finance and Operations via en fil, der modtages fra banken. Organisationer vil ofte gruppere disse transaktioner ved hjælp af bankkontonummeret i filen. Da hver transaktion vises med detaljer på bankens kontoudtog, kræves der ingen opsummering i bankreskontroen.

Transaktioner kan grupperes ved hjælp af andre felter i kladden, f.eks. selve kladdens batchnummer eller dokumentnummeret.

-   **Overfør saldi**

En organisation er måske nødt til at overføre en balance fra en kreditor til en anden, enten på grund af en fejl, eller fordi en anden kreditor har overtaget passivet. Overførsler af denne type kan også opstå til kontotyper som f.eks. debitorer og bankkonti.

Saldooverførsler fra én konto (kreditor, debitor, bankkonto osv.) til en anden konto kan foretages via separate bilag, og forskydningen kan bogføres på en clearingsfinanskonto.

-   **Angive primosaldi.**

Organisationer angiver ofte primosaldi for reskontrokonti (kreditorer, debitorer, anlægsaktiver og så videre) som en transaktion med ét bilag. Primosaldi for hver reskontrokonto kan angives som separate bilag, og forskydningen kan bogføres på en clearingsfinanskonto.

-   **Rette regnskabsposten for et bogført debitor- eller kreditordokument**

En organisation har muligvis brug for at rette debitor- eller kreditorkontoen i Finans for en regnskabspostering af en bogført faktura, men fakturaen kan ikke tilbageføres eller korrigeres gennem en anden mekanisme.

Hvis der skal foretages en korrektion af debitor- eller kreditorkontoen i Finans, skal der foretages en regulering direkte på finanskontoen. Reguleringen kan ikke foretages ved at bogføre via kreditoren eller debitoren. Denne metode kræver, at justeringen foretages under en "nedetid", så finanskontoen midlertidigt tillader manuel indtastning.

-   **"Systemet tillader det"**

Organisationer bruger ofte udelukkende funktionen ét bilag, fordi systemet lader dem bruge den, uden at de forstår konsekvenserne.

