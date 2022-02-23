---
title: Understøttelse af to momsvalutaer
description: I dette emne forklares det, hvordan du udvider funktionen vedrørende regnskab for to valutaer på momsområdet og indvirkningen på momsberegning og bogføring
author: EricWang
manager: Ann Beebe
ms.date: 12/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 9e5db8e4bbd14aa30196e3be617cdfcb72c091fd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441517"
---
# <a name="dual-currency-support-for-sales-tax"></a>Understøttelse af to momsvalutaer
[!include [banner](../includes/banner.md)]

I dette emne forklares det, hvordan du udvider regnskabet for to momsvalutaer og indvirkningen på momsberegning, bogføring og udligninger.

Funktionen vedrørende to valutaer for Dynamics 365 Finance blev introduceret i version 8.1 (oktober 2018). Den ændrer den måde, som regnskabsposter i rapporteringsvalutaen beregnes på.

I tidligere versioner blev transaktioner omregnet til rapporteringsvalutaen i følgende rækkefølge: 

- Det samlede transaktionsbeløb blev beregnet i transaktionsvalutaen > transaktionsbeløbet blev omregnet til regnskabsvalutaen > regnskabsvalutabeløbet blev omregnet til rapporteringsvalutaen

Når funktionen vedrørende to valutaer er aktiveret, blev transaktionerne omregnet til rapporteringsvalutaen i følgende rækkefølge:

- Transaktionsvalutabeløb > Rapporteringsvalutabeløb

Yderligere oplysninger om to valutaer finder du under [To valutaer](dual-currency.md).

Som følge af support i forbindelse med dobbelte valutaer er der stillet to nye funktioner i funktionsstyring til rådighed: 

- Momskonvertering (udgivet i version 10.0.9)
- Automatisk saldo for momsafregning i rapporteringsvaluta (udgivet i version 10.0.11)

Understøttelse af to momsvalutaer sikrer, at momsen beregnes nøjagtigt i momsvalutaen, og at momsafregningssaldoen beregnes nøjagtigt i både regnskabsvalutaen og rapporteringsvalutaen. 

## <a name="sales-tax-conversion"></a>Omregning af moms

Parameteren **Momskonvertering** giver to muligheder for at omregne momsbeløb fra transaktionsvaluta til momsvaluta. 

- Regnskabsvaluta: Fremgangsmåden er "Beløb i transaktionsvaluta > beløb i regnskabsvaluta > beløb i momsvaluta". Regnskabsvalutaens valutakurstype (konfigureret i finansopsætning) vil blive brugt til valutaomregningen.
- Rapporteringsvaluta: Fremgangsmåden er "Beløb i transaktionsvaluta > beløb i rapporteringsvaluta > beløb i momsvaluta". Rapporteringsvalutaens valutakurstype (konfigureret i finansopsætning) vil blive brugt til valutaomregningen.

### <a name="example"></a>Eksempel

Følgende er et eksempel på en enkelt måde, hvorpå denne funktionalitet kan demonstreres:

Valutaopsætning for finans og moms

| Transaktionsvaluta | Regnskabsvaluta | Rapporteringsvaluta | Momsvaluta |
| -------------------- | ------------------- | ------------------ | ------------ |
| EUR                  | USD                 | GBP                | GBP          |

Valutakurs

| Fra valuta | Til valuta | Faktor | Valutakurs |
| ------------- | ----------- | ------ | ------------- |
| EUR           | USD         | 1      | 1.11          |
| EUR           | GBP         | 1      | 0.83          |
| USD           | GBP         | 1      | 0.75          |

Beregning af momsbeløb ved forskellige parameterindstillinger

Momsbeløb = 100 EUR

| Omregningsparametre for moms | Transaktionsvaluta (EUR) | Regnskabsvaluta (USD) | Rapporteringsvaluta (GBP) | Momsvaluta (GBP) |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| Regnskabsvaluta             | 100                        | 111                       | 83                       | **83.25**          |
| Rapporteringsvaluta              | 100                        | 111                       | 83                       | **83**             |

Dette parameter kan konfigureres på grundlag af overholdelsesbehovet fra skattemyndighederne.


### <a name="upgrade-consideration"></a>Overvejelser omkring opgradering

Denne funktion gælder kun for nye transaktioner. For så vidt angår momstransaktioner, der allerede er blevet gemt i tabellen TAXTRANS, men som endnu ikke er blevet udlignet, vil systemet ikke genberegne momsbeløbet i momsvalutaen, fordi valutakursen på tidspunktet, hvor momsen skal bogføres, allerede mangler.

Hvis du vil undgå ovenstående, anbefales det, at du ændrer denne parameterværdi i en ny (ren) momsafregningsperiode, der ikke indeholder nogen ikke-udlignede momstransaktioner. Hvis du vil ændre denne værdi midt i en momsafregningsperiode, skal du køre programmet "Udligning og bogføring af moms" for den aktuelle momsafregningsperiode, før du ændrer denne parameterværdi.


## <a name="track-reporting-currency-tax-amount"></a>Spor momsbeløbet i rapporteringsvaluta

Der blev føjet tre nye felter til de momsrelaterede tabeller for at spore beløb i rapporteringsvalutaen. Disse felter findes i TAXUNCOMMITTED- og TAXTRANS-tabellerne:

- TaxAmountRep: momsbeløb i rapporteringsvaluta
- TaxBaseAmountRep: grundbeløbet i rapporteringsvaluta
- TaxInCostPriceRep: ikke-fradragsberettiget beløb i rapporteringsvaluta

Hvis momsen kun er gemt i tabellen TAXUNCOMMITTED, men ikke bogført endnu, vil systemet beregne momsbeløbet i rapporteringsvalutaen på bogføringstidspunktet og gemme det i TAXTRANS-tabellen.

Denne version omfatter ikke ændringer i rapporter og formularer, der viser momsbeløbet i rapporteringsvalutaen. Ændringer i rapporter og formularer vil blive leveret i den kommende udgivelse.



## <a name="tax-settlement-auto-balance-in-reporting-currency"></a>Automatisk saldo for momsafregning i rapporteringsvaluta

Hvis momsafregningen ikke er afstemt i rapporteringsvalutaen af en bestemt grund, f.eks. fordi fremgangsmåden for omregning af moms er "Regnskabsvaluta" eller valutakursen ændres i en enkelt momsafregningsperiode, vil systemet automatisk oprette regnskabsposter, der skal regulere afvigelse i momsbeløbet og modposteres i henhold til den realiserede vekselgevinst/tabskonto, der konfigureres i finansopsætningen.

Hvis du bruger eksemplet ovenfor til at demonstrere denne funktion, skal du gå ud fra, at dataene i tabellen TAXTRANS på bogføringstidspunktet er som følger.

| Omregningsparametre for moms | Transaktionsvaluta (EUR) | Regnskabsvaluta (USD) | Rapporteringsvaluta (GBP) | Momsvaluta (GBP) |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| Regnskabsvaluta             | 100                        | 111                       | 83                       | **83.25**          |
| Rapporteringsvaluta              | 100                        | 111                       | 83                       | **83**             |

Når du kører momsafregningsprogrammet ved månedsafslutning, vil regnskabsbogføringen være følgende:.
#### <a name="scenario-sales-tax-conversion--accounting-currency"></a>Scenarie: omberegning af momsbeløb = "Regnskabsvaluta"

| Hovedkonto           | Transaktionsvaluta (GBP) | Regnskabsvaluta (USD) | Rapporteringsvaluta (GBP) |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| Udgående/indgående moms | -83,25                     | -111                      | -83,25                   |
| Momsafregning         | 83.25                      | 111                       | 83.25                    |
| Realiseret gevinst/tab     | 0                          | 0                         | -0,25                    |
| Udgående/indgående moms | 0                          | 0                         | 0.25                     |

#### <a name="scenario-sales-tax-conversion--reporting-currency"></a>Scenarie: omberegning af momsbeløb = "Rapporteringsvaluta"


| Hovedkonto           | Transaktionsvaluta (GBP) | Regnskabsvaluta (USD) | Rapporteringsvaluta (GBP) |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| Udgående/indgående moms | -83                        | -110,67                   | -83                      |
| Momsafregning         | 83                         | 110.67                    | 83                       |
| Realiseret gevinst/tab     | 0                          | 0.33                      | 0                        |
| Udgående/indgående moms | 0                          | -0,33                     | 0                        |



Du kan finde flere oplysninger under følgende emner:

- [Dobbelt valuta](dual-currency.md)
- [Momsoversigt](indirect-taxes-overview.md)

