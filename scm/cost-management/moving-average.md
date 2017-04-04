---
title: Glidende gennemsnit
description: 
author: YuyuScheller
manager: AnnBe
ms.date: 2016-03-17 15 - 16 - 47
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 65531
ms.assetid: dfd10099-8f7f-44b1-917e-df37c2fe8773
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: e75016694e63dbc26f8d4c4ae73204966ca28dcf
ms.lasthandoff: 03/29/2017


---

# <a name="moving-average"></a>Glidende gennemsnit



Følgende er forudsætningerne for at bruge glidende gennemsnitskostpriser som en kalkulationsmetode.
1.  På siden **Varemodelgrupper** skal du konfigurere en varemodelgruppe, hvor Glidende gennemsnit er valgt i feltet **Lagermodel**.
    | **Bemærk! **                                                                                                                                |
    |-----------------------------------------------------------------------------------------------------------------------------------------|
    | Når Glidende gennemsnit er valgt, er felterne **Bogfør fysisk varelager** og **Bogfør økonomisk varelager** som standard også markeret. |

2.  På siden **Bogføring** skal du tildele konti til kontiene **Prisdifference for glidende gennemsnit** og **Omkostningsværdiregulering for glidende gennemsnit** under fanen **Lager**. Du kan bruge kontoen **Prisdifference for glidende gennemsnit**, når omkostningen skal være forholdsmæssigt udgiftsført. Dette sker på grund af en difference i omkostningen mellem en købskvittering og købsfakturaen og på grund af en difference mellem det oprindelige lagerantal og den aktuelle beholdning. Brug kontoen **Omkostningsværdiregulering for glidende gennemsnit**, når du vil justere den glidende gennemsnitskostpris for et produkt til en ny enhedspris.
3.  På siden **Frigivne produkter** skal du tildele varemodelgruppen med glidende gennemsnit til produktet.

| **Bemærk! **                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Lukning af lageret lukker kun regnskabsperioden. Den påvirker ikke produkter, som har et glidende gennemsnit, der er tildelt som en varemodelgruppe. |

## <a name="convert-to-the-moving-average-costing-method"></a>Konvertér til kalkulationsmetoden med glidende gennemsnit
Produkter kan konverteres til at bruge lagervurderingsmetoden med glidende gennemsnit. Denne type konvertering sker normalt i slutningen af året, når den sidste måned i det indeværende år er lukket. Det gøres ved hjælp af produktets aktuelle model for efterkalkulation. Du kan ændre din kalkulationsmetode for lageret fra en kalkulationsmetode, der er baseret på en gennemsnitlig kostpris eller standardomkostning til en metode, der er baseret på et glidende gennemsnit. Hvis du ændrer din kalkulationsmetode fra en standard kalkulationsmetode til en metode med glidende gennemsnit, skal du udføre følgende opgaver:
1.  Foretag justeringer for at få lagerantal og -værdier til 0 (nul).
2.  Når lagerværdien og antallet er 0 (nul), skal du ændre varemodelgruppen til glidende gennemsnit.
3.  Foretag justeringer for at få lagerantallet og -værdierne tilbage til lageret.

Du kan ikke ændre din kalkuleringsmetode for lageret fra en metode med glidende gennemsnit til en først ind-først ud-metode (FIFO), sidst ind-først ud-metode (LIFO) eller en metode med vægtet gennemsnit.
| **Bemærk! **                                                                      |
|-------------------------------------------------------------------------------|
| Konvertering fra standardomkostning til glidende vægtet gennemsnit er en manuel proces. |

Følgende eksempler illustrerer effekten af at bruge kalkulationsmetoden med glidende gennemsnit. Der findes fire konfigurationer:
-   Indkøbsordre og forholdsmæssigt udgiftsført omkostningsdifference.
-   Glidende gennemsnit for produkt og lagerregulering
-   Glidende gennemsnit med produktion
-   Glidende gennemsnit med en tilbagedateret transaktion

## <a name="purchase-order-and-proportionally-expensed-cost-difference"></a>Indkøbsordre og forholdsmæssigt udgiftsført omkostningsdifference.
Med glidende gennemsnit bestemmes produktets kostpris af købskvitteringen. Hvis der er en difference i omkostningen mellem købskvitteringen og købsfakturaen, når købsfakturaen bogføres, reguleres differencen i forhold til de aktuelle produkter, der er på lager og eventuelle resterende beløb udgiftsføres. I dette eksempel oprettes og modtages en indkøbsordre ved en omkostning, og købsfakturaen bogføres med en anden omkostning.
1.  Opret en købsordre for en mængde på 2 og en salgspris på 10,00.
2.  Opret en købskvittering for produktet.
3.  Opret en salgsordre for en mængde på 1 og en enhedspris på 10,00.
4.  Opret en købsfaktura for en mængde på 2 og en enhedspris på 12,00.

Differencen i enhedsprisen, 2,00, bogføres på kontoen Prisdifference for glidende gennemsnit, når købsfakturaen bogføres. Årsagen er, at to produkter blev købt til en pris på 20,00. Et af produkterne, der blev solgt til en enhedspris på 10,00. Købsfakturaen blev bogført til en enhedspris på 12,00 med et antal på 2. Enhedsprisen for produktet kan ikke bogføres ved 14,00.

## <a name="moving-average-product-and-inventory-adjustment"></a>Glidende gennemsnit for produkt og lagerregulering
Hvis du vil justere den glidende gennemsnitlige kostpris for et produkt, tillades lagerreguleringer for dags dato. Du kan ikke tilbagedatere en lagerregulering for at rette den glidende gennemsnitlige kostpris for et produkt. Du kan ikke have omkostningsforløb gennem efterfølgende transaktioner. I dette eksempel er den glidende gennemsnitlige kostpris reguleret for et produkt.
1.  Vælg det produkt, du vil justere den glidende gennemsnitlige omkostning for.
    | **Note**                                                                                    |
    |---------------------------------------------------------------------------------------------|
    | Den ** værdiregulering for glidende gennemsnit ** side undersøger det lager, der er tilgængelige for et produkt. |

    Det valgte produkt havde et bogført antal på 1, en bogført værdi på 12,00, en bogført enhedskostpris på 12,00 og en enhedskostpris på 12,00.
2.  Opdater feltet **Enhedskostpris** til 16,00. Systemet beregner de resterende felter.
3.  Reguleringen er bogført.

| **Bemærk! **                                                        |
|-----------------------------------------------------------------|
| Du kan kun justere den glidende gennemsnitlige kostpris for dags dato. |

På siden **Udligninger på bilag** kan du se en regulering på 4,00, der er bogført på kontoen Omkostningsværdiregulering for glidende gennemsnit.

## <a name="moving-average-with-production"></a>Glidende gennemsnit med produktion
Glidende gennemsnit understøtter producerede varer. Hvis du planlægger at bruge glidende gennemsnit i et produktionsmiljø, den **Brug anslået kostpris** skyderen i det ** produktionsparametre ** side skal være markerede. Dette betyder, at den kostpris, der er beregnet ved forkalkulationen bruges i stedet for den faktiske kostpris for styklistekalkulation.

## <a name="moving-average-with-a-backdated-transaction"></a>Glidende gennemsnit med en tilbagedateret transaktion
Tilbagedaterede transaktioner tildeles den aktuelle kostpris med glidende gennemsnit, og produktets fysiske antal opdateres, men den glidende gennemsnitlige kostpris påvirkes ikke. I dette eksempel på glidende gennemsnit bogføres en tilbagedateret transaktion for et produkt med glidende gennemsnit.
1.  Opret en lagerregulering for et produkt med glidende gennemsnit til et antal på 1 og en omkostning på 20,00.
2.  Lagertransaktionsoversigten for produktet ligner følgende:
    -   En lagertransaktion på 1, en omkostning på 16,00, bogføringsdatoen 15. januar og transaktionsdatoen 15. januar.
    -   En lagerjustering på 1, en omkostning på 20,00, bogføringsdatoen 1. januar og transaktionsdatoen 15. januar.

3.  Bogfør reguleringen.

På siden **Lagertransaktioner** kan du se, at 4,00 udgiftsføres som det aktuelle glidende gennemsnit for produktet, er 16,00. Du kan tilbagedatere en bogføring, men differencen i omkostningen udgiftsføres, så den glidende gennemsnitlige kostpris påvirkes ikke.

## <a name="inventory-value-report"></a>Rapporten Lagerværdi
I dette eksempel på et glidende gennemsnit udskrives lagerværdirapporten for at understøtte den aktuelle glidende gennemsnitlige beregning for et produkt. Rapporten Lagerværdi kan udskrive posteringerne i kronologisk rækkefølge sammen med omkostningerne for at understøtte den glidende gennemsnitlige beregning af et produkt. Rapporten viser den glidende gennemsnitlige kostpris for produktet. I dialogboksen **Lagerværdirapporter** giver et datointerval dig mulighed at vælge den **Transaktionsklokkeslæt** eller **Bogføringsdato** til at sortere rapporten efter. Indstillingen **Bogføringsdato** viser, hvordan rapporten traditionelt udskrives. Indstillingen **Transaktionsklokkeslæt** er den faktiske dato, hvor transaktionen er rapporteret, og den glidende gennemsnitlige omkostning for produktet opdateres. Du kan udskrive rapporten Lagerværdi ved hjælp af indstillingen **Sortering af transaktionsklokkeslæt**, hvis du vil se den glidende gennemsnitlige omkostningsberegning over tid. Følgende tabel viser transaktionerne for det produkt, som rapporten udskrives for, når indstillingen **Sortering af transaktionsklokkeslæt** bruges.

| Transaktionsklokkeslæt | Dato         | Transaktionstype           | Antal | Beløb | Gennemsnitlig enhedskostpris |
|------------------|--------------|----------------------------|----------|--------|-------------------|
|                  | 1. oktober    | Primosaldo          | 0        | 0,00   | 0,00              |
| 8. oktober        | 28. september | Tilbagedateret kvittering          | 1        | 16,00  | 16,00             |
| 3. oktober        | 3. oktober    | Købskvittering           | 2        | 20,00  | 12,00             |
| 5. oktober        | 5. oktober    | Salgsordre                | -1       | -10,00 | 13,00             |
| 7. oktober        | 7. oktober    | Indkøbsfaktura           |          | 2,00   | 14,00             |
| 8. oktober        | 8. oktober    | Værdiregulering med glidende gennemsnit |          | 4,00   | 16,00             |
|                  | 31. oktober   | I alt                      | 2        | 32,00  | 16,00             |

 

| **Bemærk! **                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Du kan ikke afstemme finansmodulet med lager ved hjælp af indstillingen **Sortering af transaktionsklokkeslæt**. Rapporten skal udskrives ved hjælp af indstillingen **Bogføringsdato**. |




