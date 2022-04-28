---
title: Indkøbskort
description: Dette emne forklarer, hvordan du opretter og sporer transaktioner med indkøbskort.
author: velofog
ms.date: 09/03/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.search.industry: public sector
ms.author: kfend
ms.search.validFrom: 2019-9-03
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: a5619b90193819a64bb88e883fd8e4460e1b0f64
ms.sourcegitcommit: 23588e66e25c05e989f3212ac519d7016820430a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/13/2022
ms.locfileid: "8565518"
---
# <a name="purchasing-cards"></a>Indkøbskort

[!include [banner](../includes/banner.md)]


Agenturerne bruger indkøbskort, så medarbejderne kan skaffe varer og tjenester uden at bruge standardprocessen for indkøbsrekvisitioner. De sider og felter, der er relateret til indkøbskort, indeholder en metode til sporing af indkøb. Hvert indkøb, som en medarbejder foretager via et indkøbskort, registreres på en kreditorfaktura. Fakturaen betales dog ikke med en check eller elektronisk betaling til den kreditor, der leverede varerne eller tjenesterne. Hver faktura af denne type er i stedet knyttet til en anden kreditorfaktura, der oprettes for at betale den leverandør, der udbyder tjenesterne for indkøbskort (dvs. finansinstitut). Kortkøbene betales, når den saldo, der skal betales til tjenesteudbyderen af indkøbskort, betales hver måned.

## <a name="enable-purchasing-card-pages-and-fields"></a>Aktivere sider og felter til indkøbskort

1. Gå til **Kreditor** \> **Opsætning** \> **Kreditorparametre**.
2. Under fanen **Faktura** skal du angive indstillingen **Aktivér indkøbskort** til **Ja**.

## <a name="enter-purchasing-card-records-for-employees"></a>Angive poster til indkøbskort for medarbejdere

Du skal angive oplysninger om de indkøbskort, der er udstedt til medarbejdere, så de kan købe varer eller tjenester. Disse oplysninger vil blive vist på kreditorfakturaer. Når et indkøbskort føjes til en bankkonto, kan kreditorfakturaer genkende kreditkortet som gyldigt under fakturabehandlingen.

1. Gå til **Kontant- og bankstyring** \> **Generelt** \> **Bankkonti**.
2. Vælg bankkontoen til leverandøren af købskorttjenester på listesiden.
3. I handlingsruden skal du under fanen **Opsætning** vælge **Indkøbskort**.
4. Vælg **Nyt** på siden **Bankindkøbskort** for at oprette en post med indkøbskort.
5. Angiv følgende oplysninger om indkøbskortet.

    - Angiv reference nummeret for kreditkortet i feltet **Referencenummer til indkøbskort**. Du kan f.eks. skrive de sidste fire cifre.

        > [!NOTE]
        > Når du har gemt referencenummeret til indkøbskortet, kan du ikke ændre det.

    - Indtast navnet på kortholderen, som det står på indkøbskortet, i feltet **Navn på kortholderen**.
    - Vælg den medarbejder, som kortet er udstedt til, i feltet **Medarbejder**.
    - Valgfrit: Angiv den dato, hvor kortet blev udstedt til medarbejderen, i feltet **Gyldigt fra**.
    - Valgfrit: Angiv den dato, hvor kortet udløber, i feltet **Udløbsdato**.
    - Valgfrit: Angiv det maksimale beløb, der kan opkræves på kortet, i feltet **Kreditgrænse**.

## <a name="set-up-a-posting-definition-for-vendor-invoices-that-track-employee-purchases"></a>Oprette en bogføringsdefinition for kreditorfakturaer, der sporer medarbejderindkøb

Du skal oprette en bogføringsdefinition for de kreditorfakturaer, du angiver for at registrere indkøb, der er foretaget ved hjælp af et indkøbskort. Når disse fakturaer bogføres, oprettes der modposter for udgiften i Finans. Når en kreditorfaktura udlignes, flyttes den til historikken, men der genereres ikke en betaling til kreditoren. Du bruger denne bogføringsdefinition, når du importerer fakturaer fra en ekstern fil, og når du manuelt angiver kreditorfakturaer for medarbejderindkøb.

Valgfrit: Du kan angive bogføringsdefinitionen, så den bruges som standard, når du opretter kreditorfakturaer for at registrere transaktioner med indkøbskort.

1. Gå til **Kreditor** \> **Opsætning** \> **Kreditorparametre**.
2. Vælg den bogføringsdefinition, du vil bruge som standardbogføringsdefinition, i feltet **Standardbogføringsdefinition for indkøbspost** under fanen **Faktura**.

## <a name="overview-processing-invoices-for-purchasing-card-transactions"></a>Oversigt: Behandling af fakturaer til transaktioner med indkøbskort

Når du har konfigureret dit system til indkøbskort, kan du oprette en faktura for en kreditor, eller et finansieringsinstitut, der leverer tjenester for indkøbskort. Du kan også oprette andre fakturaer for at spore de indkøb, der er foretaget af kortindehavere. Når du har modtaget den månedlige opgørelse for indkøbskort fra pengeinstituttet, kan du distribuere den til medarbejdere, der har købt noget i faktureringsperioden. Disse medarbejdere vil typisk kontrollere transaktionerne og levere kvitteringer eller fakturaer, der understøtter deres indkøb.

1. Opret en kreditorfaktura for at betale indkøbskortets tjenesteudbyder. Du skal oprette en check for denne kreditorfaktura for at betale saldoen på indkøbskortets opgørelse.
2. Opret andre kreditorfakturaer for at registrere indkøb, der er foretaget af kortindehavere.

> [!NOTE]
> Du skal typisk bruge dataenhederne for kreditorfakturaer til at udgive kreditorfakturadata i systemet.

## <a name="create-a-vendor-invoice-for-a-purchasing-card-statement"></a>Oprette en kreditorfaktura for et indkøbskorts opgørelse

Du kan bruge denne procedure til at oprette en kreditorfaktura for at registrere den periodiske kontoudtogssaldo for et købskorts opgørelse, der er modtaget fra en tjenesteudbyder af indkøbskort.

1. Gå til **Kreditor** \> **Generelt** \> **Kreditorfakturaer** \> **Åbne kreditorfakturaer**.
2. Vælg **Faktura** \> **Kreditorfaktura** i handlingsruden.
3. Angiv konto nummeret for den leverandør, der har sendt indkøbskortopgørelsen, i feltet **Fakturakonto** på siden **Kreditorfaktura**.
4. Angiv fakturanummeret i feltet **Nummer**.
5. Vælg **Tilføj linje** i gitterområdet **Linjer**, og angiv derefter oplysninger om linjen.
6. Hvis du vil angive flere oplysninger om linjen, skal du vælge oversigtspanelet **Linjedetaljer** og angive oplysningerne.
7. Vælg **Finans** for at tilføje eller ændre oplysninger om den økonomiske distribution for fakturalinjen.
8. Vælg **Overskrift** i handlingsruden for at angive yderligere oplysninger om fakturahovedet.
9. Vælg **Udbetaling af saldo** i feltet **Indkøbskortfaktura** under fanen **Generelt** i handlingsruden for at angive, at du udbetaler dit agenturs indkøbskortsaldo.
10. Valgfrit: Send fakturaen til arbejdsgangssystemet til gennemsyn og godkendelse, og bogfør derefter fakturaen.

    > [!NOTE]
    > Før du opretter en indkøbskortfaktura, skal du bogføre fakturaen for saldoudbetaling til indkøbskortets tjenesteudbyder. Alle indkøbskortfakturaer vil blive bogført mod denne faktura.

11. Hvis du vil gemme fakturaen uden at bogføre den, skal du lukke siden. Du kan se fakturaen på listesiden **Ventende kreditorfakturaer**.

## <a name="create-a-vendor-invoice-to-record-a-purchasing-card-transaction"></a>Oprette en kreditorfaktura for et registrere en indkøbskorttransaktion

Du kan bruge følgende procedure til at oprette en kreditorfaktura for at registrere et indkøb, der er foretaget ved hjælp af et indkøbskort. Denne faktura vil blive udlignet, men ikke betalt, til den leverandør, der leverede de indkøbte varer eller tjenester.

> [!NOTE]
> Fakturaen for den opgørelse, der er angivet som fakturaen for saldoudbetaling, skal bogføres på kreditorkontoen, før du opretter en indkøbskortfaktura.

1. Gå til **Kreditor** \> **Generelt** \> **Kreditorfakturaer** \> **Åbne kreditorfakturaer**.
2. Vælg **Faktura** \> **Kreditorfaktura** i handlingsruden.
3. Angiv kontonummeret for den leverandør, der har sendt fakturaen for varerne eller tjenesterne, i feltet **Fakturakonto** på siden **Kreditorfaktura**.
4. Angiv fakturanummeret i feltet **Nummer**.
5. Vælg **Overskrift** i handlingsruden for at angive yderligere oplysninger om fakturahovedet.
6. I feltet **Købskortfaktura** skal du vælge **Registrer indkøb** som den type af indkøbskorttransaktion, du indtaster fakturaen for.

    > [!NOTE]
    > En værdi af **Saldoudbetaling** angiver, at fakturaen betaler en saldo, der skal betales til tjenesteudbyderen af indkøbskort. Værdien **I/T** angiver, at fakturaen ikke involverer et indkøbskort.

7. I oversigtspanelet **Opsætning** i feltet **Bogføringsdefinition** skal du vælge bogføringsdefinitionen for indkøbskortet, hvis der ikke blev valgt en standardværdi på siden **Kreditorparametre**.

    > [!NOTE]
    > Den bogføringsdefinition, du vælger, skal være konfigureret til registrering af indkøbet, men ikke til bogføring i Kreditor. Ellers vil der blive foretaget en betaling til den leverandør, der leverede de varer eller tjenester, der er blevet indkøbt ved hjælp af indkøbskortet.

8. I oversigtspanelet **Betaling** kan du se eller angive oplysninger om det indkøbskort, der blev brugt til at foretage købet:

    - Angiv referencenummeret for kortet i feltet **Referencenummer til indkøbskort**.
    - Se navnet på den bank, der har udstedt kortet. Denne værdi vises, når du har angivet referencenummeret.
    - Se navnet på kortholderen. Denne værdi er baseret på det referencenummer, du har angivet.
    - Angiv kontonummeret for den leverandør, der udbyder indkøbskorttjenester, i feltet **Konto**.
    - Se navnet på indkøbskortets tjenesteudbyder. Denne værdi er baseret på det kontonummer, du har angivet.
    - I feltet **Købskortfaktura** skal du angive kreditorfakturanummeret på den relaterede saldoudbetalingsfaktura, der blev oprettet for at betale for den indkøbskortopgørelse, der omfatter dette indkøb. Dette felt skal være angivet til fakturanummeret på den bogførte faktura, der er angivet som saldoudbetalingsfaktura. Dette fakturanummer vises på listen, hvis fakturaen var markeret på den korrekte måde.

9. Vælg **Linjevisning** i handlingsruden for at angive oplysninger om indkøbsbeløbet.
10. Vælg **Tilføj linje** i gitterområdet **Linjer**, og angiv oplysninger om linjen.
11. Hvis du vil angive flere oplysninger om linjen, skal du vælge oversigtspanelet **Linjedetaljer** og angive oplysningerne.
12. Valgfrit: Send fakturaen til arbejdsgangssystemet til gennemsyn og godkendelse, og bogfør derefter fakturaen.
13. Hvis du vil gemme fakturaen uden at bogføre den, skal du lukke siden. Du kan se fakturaen på listesiden **Ventende kreditorfakturaer**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]