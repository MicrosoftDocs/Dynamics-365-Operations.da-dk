---
title: Dobbeltrapportering
description: I dette emne gennemgås et eksempel med, hvordan du kan opfylde kravene til både rapportering af International Financial Reporting Standard (IFRS) og lovpligtig rapportering i aktivleasing.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a7d9b3ea3d4f1d48b8a7326bd5a01d3119310c62
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003175"
---
# <a name="dual-reporting"></a>Dobbeltrapportering

[!include [banner](../includes/banner.md)]

I dette emne gennemgås et eksempel med, hvordan du kan opfylde kravene til både rapportering af International Financial Reporting Standard (IFRS) og lovpligtig rapportering i aktivleasing. Det er nødvendigt med kendskab til posteringslag i Microsoft Dynamics 365 Finance, og det vil gøre det nemmere at forstå i eksemplet.

## <a name="example"></a>Eksempel

Følgende eksempelkonti til en leaseaftale under italiensk lovpligtig rapportering ved hjælp af både likviditetsmetoden og IFRS-rapporteringsmetoder. Firmaet skal etablere tre kartoteker for at kunne redegøre for både de italienske lovpligtige krav og IFRS 16-krav. Der kræves et kartotek til IFRS 16, et kartotek til lovpligtige krav, og et kartotek til automatisk tilbageføring af lovpligtige bogføringer. Kartotekerne oprettes som vist i følgende tabeller.

**IFRS 16-kartotek**

IFRS 16-kartoteket er konfigureret, så det overholder IFRS 16-regnskabsstandarden. Alle poster, der er bogført i dette kartotek, bogføres i et brugerdefineret lag.

| Navn                                    | Betegnelse    |
|-----------------------------------------|----------------|
| Kartotekstype                               | IFRS 16        |
| Bogbeskrivelse                        | IFRS 16        |
| Posteringslag                           | Brugerdefineret lag 1 |
| Leasingaftaletype                              | Finance        |
| Regnskabsstruktur                    | IFRS 16        |
| Konfiguration af leasingperiode/brugstid         | 0,00           |
| Konfiguration af nutidsværdi/handelsværdi af aktiv | 0,00           |
| Kortsigtet grænse                    | 12             |
| Grænse for lav værdi                     | 5,000.00       |
| Betal til kreditor                           | Ingen             |

**Lovpligtigt kartotek**

Det lovpligtige kartotek er en kassekladde, hvor firmaet kan redegøre for leasingudgifter som det kontantbeløb, der betales hver måned for leje. Dette kartotek opretter ikke et ROU-aktiv eller en leasingforpligtelse.

| Navn                                    | Betegnelse |
|-----------------------------------------|-------------|
| Kartotekstype                               | Lovpligtig   |
| Bogbeskrivelse                        | Lokal GAAP  |
| Posteringslag                           | Løbende     |
| Leasingaftaletype                              | Automatisk   |
| Regnskabsstruktur                    | Kontantgrundlag  |
| Konfiguration af leasingperiode/brugstid         | 0,00        |
| Konfiguration af nutidsværdi/handelsværdi af aktiv | 0,00        |
| Kortsigtet grænse                    | 0           |
| Grænse for lav værdi                     | 0           |
| Betal til kreditor                           | Ingen          |

**Lovpligtigt tilbageført kartotek**

Det lovpligtige tilbageførte kartotek konfigureres på samme måde som det lovpligtige kartotek.

| Navn                                    | Betegnelse                    |
|-----------------------------------------|--------------------------------|
| Kartotekstype                               | Lovpligtig - tilbageført           |
| Bogbeskrivelse                        | Kartotek, der skal tilbageføre lovpligtigt kartotek |
| Posteringslag                           | Brugerdefineret lag 1                 |
| Leasingaftaletype                              | Automatisk                      |
| Regnskabsstruktur                    | Kontantgrundlag                     |
| Konfiguration af leasingperiode/brugstid         | 0,00                           |
| Konfiguration af nutidsværdi/handelsværdi af aktiv | 0,00                           |
| Kortsigtet grænse                    | 0                              |
| Grænse for lav værdi                     | 0                              |
| Betal til kreditor                           | Ingen                             |

I dette eksempel er der oprettet en leasingaftale, der indeholder følgende indstillinger under fanerne **Generelt** og **Betalingsplanlinje**.

Fanen **Generelt**

| Felt                      | Værdi            |
|----------------------------|------------------|
| Trinvis lånesats | 5 %               |
| Dato for påbegyndelse          | 1/1/2020         |
| Leasinggruppe                | Bygninger        |
| Leverandør                     | 1001             |
| Aktivets handelsværdi    | 245,000          |
| Brugstid for aktiv          | 120              |
| Annuitetstype               | Almindelig annuitet |
| Sammensætningsinterval       | Månedligt          |

**Betalingsplanlinjer-fane**

| Felt             | Værdi      |
|-------------------|------------|
| Igangsæt dato        | 1/1/2020   |
| Periodeinterval   | Måneder     |
| Perioder           | 24         |
| Slutdato          | 12/31/2020 |
| Betalingshyppighed | Månedligt    |
| Betalingsbeløb    | 1.000      |

Hvis du vil redegøre for denne leasingaftale i forbindelse med to strukturer, skal du bruge et aktuelt posteringslag og et brugerdefineret posteringslag. Følgende tabel viser et eksempel på hver kladdepost, der er nødvendig for at repræsentere finanserne i de enkelte rapporteringsstandarder. En detaljeret beskrivelse af de enkelte kladdeposter for den første måned af leasingaftalen tildeles bagefter.

<table>
<thead>
<tr>
<th rowspan='3'>Kontonummer</th>
<th rowspan='3'>Betegnelse</th>
<th colspan='3'>Lovpligtigt kartotek (aktuelt lag)</th>
<th rowspan='3'>Aktuelt samlet lag</th>
<th>Tilbageført kartotek (brugerdefineret lag)</th>
<th colspan='4'>IFRS 16-kartotek (brugerdefineret lag)</th>
<th rowspan='3'>Aktuelt lag + brugerdefineret lag i alt</th>
</tr>
<tr>
<th>JE-100</th>
<th>JE-110</th>
<th>JE-120</th>
<th>JE-130</th>
<th>JE-140</th>
<th>JE-150</th>
<th>JE-160</th>
<th>JE-170</th>
</tr>
<tr>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
</tr>
</thead>
<tbody>
<tr>
<td>1</td>
<td>Leasingudgift</td>
<td>1,000.00</td>
<td></td>
<td></td>
<td>1,000.00</td>
<td>-1.000,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>2</td>
<td>Bankgebyr</td>
<td></td>
<td>3.00</td>
<td></td>
<td>3.00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>3.00</td>
</tr>
<tr>
<td>3</td>
<td>Momsudgift</td>
<td></td>
<td>5.00</td>
<td></td>
<td>5.00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>5.00</td>
</tr>
<tr>
<td>4</td>
<td>Clearingkonto</td>
<td>-1.000,00</td>
<td>1,000.00</td>
<td></td>
<td>0,00</td>
<td>1,000.00</td>
<td></td>
<td>-1.000,00</td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>5</td>
<td>Kreditor</td>
<td></td>
<td>-1.008,00</td>
<td>1,008.00</td>
<td>0,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>6</td>
<td>ROU-aktiv</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td>22,794.00</td>
<td></td>
<td></td>
<td></td>
<td>22,793.90</td>
</tr>
<tr>
<td>7</td>
<td>Finansiel leasingforpligtelse</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td>-22.794,00</td>
<td>1,000.00</td>
<td>-94,97</td>
<td></td>
<td>-21.888,87</td>
</tr>
<tr>
<td>8</td>
<td>Renteudgift</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td></td>
<td></td>
<td>94.97</td>
<td></td>
<td>94.97</td>
</tr>
<tr>
<td>9</td>
<td>Indløsning</td>
<td></td>
<td></td>
<td>-1.008,00</td>
<td>-1.008,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>-1.008,00</td>
</tr>
<tr>
<td>10</td>
<td>Afskrivningsomkostning</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>949.75</td>
<td>949.75</td>
</tr>
<tr>
<td>11</td>
<td>Akkumuleret afskrivning</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>-949,75</td>
<td>-949,75</td>
</tr>
</tbody>
</table>

Som vist i den foregående tabel, skal der rapporteres tre kartoteker under både lovpligtig rapportering og IFRS-rapportering.

- I det lovpligtige kartotek registreres leasingbetalingen i henhold til reglerne for kontantregnskab under det aktuelle lag.
- Det lovpligtige tilbageførte kartotek tilbagefører de lovpligtige kladdeposteringer.
- IFRS 16-kartoteket opretter de kladdeposteringer, der er påkrævet i IFRS 16.

Du skal kun angive en leasingaftale én gang. Du kan derefter åbne siden **Kartoteker** for at se alle de kartoteker, der er tilknyttet leasingaftalen.

> [!NOTE]
> Når du opretter kartotekerne, skal de alle tre knyttes til samme leasingpost.

Den første kladdepostering registrerer leasingudgiften i henhold til det lovpligtige kartotek. Du kan oprette betalinger enten i en batch eller ved at vælge betalingsplanen i det lovpligtige kartotek.

I dette eksempel er der oprettet følgende kladdepost for det lovpligtige kartotek fra betalingsplanen.

### <a name="lease-payment--1312020--je-100"></a>Leasingbetaling - 1/31/2020 - JE 100

| Kontotype | Kontonummer | Lag   | Kontobeskrivelse | Debet    | Kredit   |
|--------------|----------------|---------|---------------------|----------|----------|
| Ledger       | 1              | Løbende | Leasingudgift       | 1,000.00 |          |
| Ledger       | 4              | Løbende | Clearingkonto    |          | 1,000.00 |

En kreditormedarbejder bruger standardfunktionen for Dynamics 365 til at oprette en faktura, der skal betale for leasingaftalen uden for aktivleasing. I stedet for at vælge **leasingudgift** som debetkonto vælger kreditormedarbejderen en clearingkonto til at generere følgende post.

### <a name="ap-process--1312020--je-110"></a>AP-proces – 31/1/2020 – JE 110

| Kontotype | Kontonummer | Lag   | Kontobeskrivelse | Debet    | Kredit   |
|--------------|----------------|---------|---------------------|----------|----------|
| Ledger       | 4              | Løbende | Clearingkonto    | 1,000.00 |          |
| Ledger       | 2              | Løbende | Bankgebyr            | 3.00     |          |
| Ledger       | 3              | Løbende | Momsudgift         | 5.00     |          |
| Leverandør       | 5              | Løbende | Kreditor    |          | 1,008.00 |

Når opgørelsen er udstedt til leverandøren, skal du følge den almindelige betalingsproces. Under denne proces genereres følgende kladdepost.

### <a name="cash-payment--1312020--je-120"></a>Kontant betaling – 31/1/2020 – JE 120

| Kontotype | Kontonummer | Lag   | Kontobeskrivelse | Debet    | Kredit   |
|--------------|----------------|---------|---------------------|----------|----------|
| Leverandør       | 5              | Løbende | Kreditorer    | 1,008.00 |          |
| Bank         | 9              | Løbende | Indløsning                |          | 1,008.00 |

På dette tidspunkt har du taget fuld højde for denne leasingaftale under lovpligtige rapporteringskrav og kan generere en råbalance ved hjælp af det aktuelle lag. Systemet returnerer en råbalance, der har følgende tal.

<table>
<thead>
<tr>
<th rowspan='3'>Kontonummer</th>
<th rowspan='3'>Betegnelse</th>
<th colspan='3'>Lovpligtigt kartotek (aktuelt lag)</th>
<th rowspan='3'>Aktuelt samlet lag</th>
</tr>
<tr>
<th>JE-100</th>
<th>JE-110</th>
<th>JE-120</th>
</tr>
<tr>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
</tr>
</thead>
<tbody>
<tr>
<td>1</td>
<td>Leasingudgift</td>
<td>1,000.00</td>
<td></td>
<td></td>
<td>1,000.00</td>
</tr>
<tr>
<td>2</td>
<td>Bankgebyr</td>
<td></td>
<td>3.00</td>
<td></td>
<td>3.00</td>
</tr>
<tr>
<td>3</td>
<td>Momsudgift</td>
<td></td>
<td>5.00</td>
<td></td>
<td>5.00</td>
</tr>
<tr>
<td>4</td>
<td>Clearingkonto</td>
<td>-1.000,00</td>
<td>1,000.00</td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>5</td>
<td>Kreditor</td>
<td></td>
<td>-1.008,00</td>
<td>1,008.00</td>
<td>0,00</td>
</tr>
<tr>
<td>6</td>
<td>ROU-aktiv</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>7</td>
<td>Finansiel leasingforpligtelse</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>8</td>
<td>Renteudgift</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>9</td>
<td>Indløsning</td>
<td></td>
<td></td>
<td>-1.008,00</td>
<td>-1.008,00</td>
</tr>
<tr>
<td>10</td>
<td>Afskrivningsomkostning</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>11</td>
<td>Akkumuleret afskrivning</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
</tbody>
</table>

Hvis du vil bruge IFRS 16-tal til at køre samme råbalance, skal de lovpligtige regnskabskladdeposteringer tilbageføres, og de IFRS 16-journaloptegnelser skal bogføres. Hvis du vil tilbageføre lovpligtige kladdeposteringer, skal dette eksempel indeholde en lovpligtig tilbageførsel, der har samme opsætning som det lovpligtige kartotek, men en modsat posteringsprofil. Det lovpligtige kartotek har *debiteret* en konto til leasingomkostninger, men det tilbagevendende kartotek vil *kreditere* denne konto. Disse relationer defineres nemt i bankkonti for aktivleasing på siden **Aktivleasingparametre** (**Aktivleasing \> Konfiguration \> Aktivleasingparametre**).

Når den samme proces, der blev anvendt til det lovpligtige kartotek, bruges i et tilbageført kartotek, oprettes følgende kladdepost. Forskellen er, at det tilbageførte kartotek registrerer posteringer fra det lovpligtige kartotek. De tilbageførte posteringer foretages også i det brugerdefinerede lag. Når der køres en råbalance på det aktuelle lag, medtages der ikke kladdeposteringer til tilbageførsel.

### <a name="lease-payment--1312020--je-130"></a>Leasingbetaling - 31/1/2020 - JE 130

| Kontotype | Kontonummer | Lag  | Kontobeskrivelse | Debet    | Kredit   |
|--------------|----------------|--------|---------------------|----------|----------|
| Ledger       | 4              | Brugerdefineret | Clearingkonto    | 1,000.00 |          |
| Ledger       | 1              | Brugerdefineret | Leasingudgift       |          | 1,000.00 |

Nu, hvor du har elimineret lovpligtige kladdeposteringer, skal du reservere alle de kladdeposter, IFRS 16 har brug for, i IFRS 16-kartoteket. Disse poster omfatter den første anerkendelse af ROU-aktiv og ansvarsforsikring samt posten med renter og afskrivning.

### <a name="initial-recognition--112020--je-140"></a>Første indregning – 1/1/2020 – JE 140

| Kontotype | Kontonummer | Lag  | Kontobeskrivelse      | Debet     | Kredit    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| Ledger       | 6              | Brugerdefineret | ROU-aktiv                | 22,793.90 |           |
| Ledger       | 7              | Brugerdefineret | Finansiel leasingforpligtelse |           | 22,793.90 |

Leasingbetalingen bogføres på samme måde som andre leasingbetalinger. Årsagen til brug af clearing kontoen er at sikre, at kontant kun krediteres én gang.

### <a name="lease-payment--1312020--je-150"></a>Leasingbetaling - 31/1/2020 - JE 150

| Kontotype | Kontonummer | Lag  | Kontobeskrivelse      | Debet    | Kredit   |
|--------------|----------------|--------|--------------------------|----------|----------|
| Ledger       | 7              | Brugerdefineret | Finansiel leasingforpligtelse | 1,000.00 |          |
| Ledger       | 4              | Brugerdefineret | Clearingkonto         |          | 1,000.00 |

Renteudgiftskladdeposten genereres fra planen for passiv afskrivning.

### <a name="interest-expense--1312020--je-160"></a>Renteudgift – 31/1/2020 – JE 160

| Kontotype | Kontonummer | Lag  | Kontobeskrivelse      | Debet | Kredit |
|--------------|----------------|--------|--------------------------|-------|--------|
| Ledger       | 8              | Brugerdefineret | Renteudgift         | 94.97 |        |
| Ledger       | 7              | Brugerdefineret | Finansiel leasingforpligtelse |       | 94.97  |

Afskrivningsudgiftskladdeposten genereres fra planen for aktivafskrivning.

### <a name="depreciation-expense--1312020--je-170"></a>Afskrivningsudgift – 31/1/2020 – JE 170

| Kontotype | Kontonummer | Lag  | Kontobeskrivelse      | Debet  | Kredit |
|--------------|----------------|--------|--------------------------|--------|--------|
| Ledger       | 10             | Brugerdefineret | Afskrivningsomkostning     | 949.75 |        |
| Ledger       | 11             | Brugerdefineret | Akkumuleret afskrivning |        | 949.75 |

Når alle disse kladdeposteringer er oprettet og bogført, vises følgende værdier for "brugerdefineret lag 1". Bemærk, at den sidste kolonne indeholder bankgebyret, momsudgiften og reduktionen af kontanter fra det foregående lag, men ikke de lovpligtige rapporteringskladdeposteringer. Derfor opnås ægte Dual Reporting-funktioner. På dette tidspunkt har firmaet kun brug for sin råbalance, og kombinerer det aktuelle lag og det brugerdefinerede lag for at oprette en IFRS-råbalance.

| Kontonummer | Betegnelse              | Lovpligtigt kartotek\-Aktuelt lag\-JE\-100\-Dr \(Cr\) | Lovpligtigt kartotek\-Aktuelt lag\-JE\-110\-Dr \(Cr\) | Lovpligtigt kartotek\-Aktuelt lag\-JE\-120\-Dr \(Cr\) | Aktuelt lag \- I alt | - | Tilbageført kartotek\-Brugerdefineret lag\-JE\-130\-Dr \(Cr\) | IFRS 16 kartotek\-Brugerdefineret lag\-JE\-140\-Dr \(Cr\) | IFRS 16 kartotek\-Brugerdefineret lag\-JE\-150\-Dr \(Cr\) | IFRS 16 kartotek\-Brugerdefineret lag\-JE\-160\-Dr \(Cr\) | IFRS 16 kartotek\-Brugerdefineret lag\-JE\-170\-Dr \(Cr\) | Brugerdefineret lag \+ Aktuelt lag \- I alt |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| 1          | Leasingudgift            | 1,000\.00                                         |                                                   |                                                   | 1,000\.00               |   | \-1.000                                         |                                                |                                                |                                                |                                                | 0\.00                                   |
| 2          | Bankgebyr                 |                                                   | 3\.00                                             |                                                   | 3\.00                   |   |                                                 |                                                |                                                |                                                |                                                | 3\.00                                   |
| 3          | Momsudgift              |                                                   | 5\.00                                             |                                                   | 5\.00                   |   |                                                 |                                                |                                                |                                                |                                                | 5\.00                                   |
| 4          | Clearingkonto         | \-1.000\.00                                       | 1,000\.00                                         |                                                   | 0\.00                   |   | 1.000                                           |                                                | \-1.000                                        |                                                |                                                | 0\.00                                   |
| 5          | Kreditor         |                                                   | \-1.008\.00                                       | 1,008\.00                                         | 0\.00                   |   |                                                 |                                                |                                                |                                                |                                                | 0\.00                                   |
| 6          | ROU-aktiv                |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 | 22,794                                         |                                                |                                                |                                                | 22,793\.90                              |
| 7          | Finansiel leasingforpligtelse |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 | \-22.794                                       | 1.000                                          | \-94\.97                                       |                                                | \-21,888\.87                            |
| 8          | Renteudgift         |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 |                                                |                                                | 94\.97                                         |                                                | 94\.97                                  |
| 9          | Indløsning                     |                                                   |                                                   | \-1.008\.00                                       | \-1.008\.00             |   |                                                 |                                                |                                                |                                                |                                                | \-1.008\.00                             |
| 10         | Afskrivningsomkostning     |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 |                                                |                                                |                                                | 949\.75                                        | 949\.75                                 |
| 11         | Akkumuleret afskrivning |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 |                                                |                                                |                                                | \-949\.75                                      | \-949\.75                               |




[!INCLUDE[footer-include](../../includes/footer-banner.md)]