---
title: Glidende gennemsnit
description: Glidende gennemsnit er en permanent kalkulationsmetode baseret på gennemsnitsprincippet, hvor omkostninger på lagerafgange ikke ændres, når indkøbsprisen ændres. Differencen er aktiveret og baseret på en proportional beregning. Det beløb, der er tilbage, udgiftsføres.
author: AndersGirke
manager: tfehr
ms.date: 08/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 65531
ms.assetid: dfd10099-8f7f-44b1-917e-df37c2fe8773
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0957fee111ec1fd5bb66951126869cf46d88b36e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967477"
---
# <a name="moving-average"></a>Glidende gennemsnit

[!include [banner](../includes/banner.md)]

Glidende gennemsnit er en permanent kalkulationsmetode baseret på gennemsnitsprincippet, hvor omkostninger på lagerafgange ikke ændres, når indkøbsprisen ændres. Differencen er aktiveret og baseret på en proportional beregning. Det beløb, der er tilbage, udgiftsføres.

Når du bruger et glidende gennemsnit, understøttes lagerudligninger og lagermarkering ikke. Lukning af lageret påvirker ikke produkter, der har et glidende gennemsnit som lagermodelgruppe, og det genererer ikke nogen udligninger mellem transaktionerne.

Følgende er forudsætningerne for at bruge glidende gennemsnitskostpriser som en kalkulationsmetode.

1. På siden **Varemodelgrupper** skal du konfigurere en varemodelgruppe, hvor **Glidende gennemsnit** er valgt i feltet **Lagermodel**.

    > [!NOTE]
    > Når **Glidende gennemsnit** er valgt, er felterne **Bogfør fysisk varelager** og **Bogfør økonomisk varelager** som standard også markeret.

1. På siden **Bogføring** skal du tildele konti til **Prisdifference for glidende gennemsnit**. Du kan bruge kontoen **Prisdifference for glidende gennemsnit**, når omkostningen skal være forholdsmæssigt udgiftsført. Dette sker i følgende to situationer:
    - Der er en difference i omkostningen mellem en købskvittering og købsfakturaen, fordi der er en difference mellem det oprindelige lagerantal og den aktuelle disponible beholdning.
    - Posteringerne bringer lageret fra negativt til nul, og der er en difference mellem transaktionsomkostningerne og den aktuelle glidende gennemsnitlige omkostning.

1. På siden **Bogføring** skal du tildele konti til **Omkostningsværdiregulering for glidende gennemsnit** under fanen **Lager**. Du kan bruge kontoen **Omkostningsværdiregulering for glidende gennemsnit**, når du vil justere den glidende gennemsnitskostpris for et produkt til en ny enhedspris.

1. På siden **Frigivne produkter** skal du tildele varemodelgruppen med glidende gennemsnit til produktet.

    > [!NOTE]
    > Lukning af lageret lukker kun regnskabsperioden. Den påvirker ikke produkter, som har et glidende gennemsnit, der er tildelt som en varemodelgruppe.

## <a name="convert-to-the-moving-average-costing-method"></a>Konvertér til kalkulationsmetoden med glidende gennemsnit

Produkter kan konverteres til at bruge lagervurderingsmetoden med glidende gennemsnit. Denne type konvertering sker normalt i slutningen af året, når den sidste måned i det indeværende år er lukket. Det gøres ved hjælp af produktets aktuelle model for efterkalkulation. Du kan ændre din kalkulationsmetode for lageret fra en kalkulationsmetode, der er baseret på en gennemsnitlig kostpris eller standardomkostning til en metode, der er baseret på et glidende gennemsnit.

Hvis du ændrer din kalkulationsmetode fra en standard kalkulationsmetode til en metode med glidende gennemsnit, skal du udføre følgende opgaver:

1. Foretag justeringer for at få lagerantal og -værdier til 0 (nul).
1. Når lagerværdien og antallet er 0 (nul), skal du ændre varemodelgruppen til glidende gennemsnit.
1. Foretag justeringer for at få lagerantallet og -værdierne tilbage til lageret.

Du kan ikke ændre din kalkuleringsmetode for lageret fra en metode med glidende gennemsnit til en først ind-først ud-metode (FIFO), sidst ind-først ud-metode (LIFO) eller en metode med vægtet gennemsnit.

> [!NOTE]
> Konvertering fra standardomkostning til glidende vægtet gennemsnit er en manuel proces.

Følgende eksempler illustrerer effekten af at bruge kalkulationsmetoden med glidende gennemsnit. Der findes fire konfigurationer:

- Indkøbsordre og forholdsmæssigt udgiftsført omkostningsdifference.
- Glidende gennemsnit for produkt og lagerregulering
- Glidende gennemsnit med produktion
- Glidende gennemsnit med en tilbagedateret transaktion

## <a name="purchase-order-and-proportionally-expensed-cost-difference"></a>Indkøbsordre og forholdsmæssigt udgiftsført omkostningsdifference.

Med glidende gennemsnit bestemmes produktets kostpris af købskvitteringen. Hvis der er en difference i omkostningen mellem købskvitteringen og købsfakturaen, når købsfakturaen bogføres, reguleres differencen i forhold til de aktuelle produkter, der er på lager og eventuelle resterende beløb udgiftsføres.

I dette eksempel oprettes og modtages en indkøbsordre ved en omkostning, og købsfakturaen bogføres med en anden omkostning.

1. Opret en købsordre for en mængde på 2 og en salgspris på 10,00.
1. Opret en købskvittering for produktet.
1. Opret en salgsordre for en mængde på 1 og en enhedspris på 10,00.
1. Opret en købsfaktura for en mængde på 2 og en enhedspris på 12,00.

Differencen i enhedsprisen, 2,00, bogføres på kontoen Prisdifference for glidende gennemsnit, når købsfakturaen bogføres. Årsagen er, at to produkter blev købt til en pris på 20,00. Et af produkterne, der blev solgt til en enhedspris på 10,00. Købsfakturaen blev bogført med en enhedspris på 12,00 med et antal på 2. Enhedsprisen for produktet kan ikke bogføres ved 14,00.

## <a name="moving-average-product-and-inventory-adjustment"></a>Glidende gennemsnit for produkt og lagerregulering

Hvis du vil justere den glidende gennemsnitlige kostpris for et produkt, tillades lagerreguleringer for dags dato. Du kan ikke tilbagedatere en lagerregulering for at rette den glidende gennemsnitlige kostpris for et produkt. Du kan ikke have omkostningsforløb gennem efterfølgende transaktioner.

I dette eksempel er den glidende gennemsnitlige kostpris reguleret for et produkt.

1. Vælg det produkt, du vil justere den glidende gennemsnitlige omkostning for. 

 > [!NOTE]
 > På siden **Værdiregulering for glidende gennemsnit** undersøges det lager, der er tilgængeligt for et produkt. Det valgte produkt havde et bogført antal på 1, en bogført værdi på 12,00, en bogført enhedskostpris på 12,00 og en enhedskostpris på 12,00.
    
1. Opdater feltet **Enhedskostpris** til 16,00. Systemet beregner de resterende felter.
1. Reguleringen er bogført.

> [!NOTE]
> Du kan kun justere den glidende gennemsnitlige omkostning for dags dato.

På siden **Udligninger på bilag** kan du se en regulering på 4,00, der er bogført på kontoen Omkostningsværdiregulering for glidende gennemsnit.

## <a name="moving-average-with-production"></a>Glidende gennemsnit med produktion

Glidende gennemsnit understøtter producerede varer. Hvis du planlægger at bruge glidende gennemsnit i et produktionsmiljø, skal du vælge **Brug forkalkuleret kostpris** på siden **Produktionsstyringsparametre**. Dette betyder, at den kostpris, der er beregnet ved forkalkulationen bruges i stedet for den faktiske kostpris for styklistekalkulation.

## <a name="moving-average-with-a-backdated-transaction"></a>Glidende gennemsnit med en tilbagedateret transaktion

Tilbagedaterede transaktioner tildeles den aktuelle kostpris med glidende gennemsnit, og produktets fysiske antal opdateres, men den glidende gennemsnitlige kostpris påvirkes ikke. I dette eksempel på glidende gennemsnit bogføres en tilbagedateret transaktion for et produkt med glidende gennemsnit.

1. Opret en lagerregulering for et produkt med glidende gennemsnit til et antal på 1 og en omkostning på 20,00.
1. Lagertransaktionsoversigten for produktet ligner følgende:
    - En lagertransaktion på 1, en omkostning på 16,00, bogføringsdatoen 15. januar og transaktionsdatoen 15. januar.
    - En lagerjustering på 1, en omkostning på 20,00, bogføringsdatoen 1. januar og transaktionsdatoen 15. januar.
1. Bogfør reguleringen.

På siden **Lagertransaktioner** kan du se, at 4,00 udgiftsføres som det aktuelle glidende gennemsnit for produktet, er 16,00. Du kan tilbagedatere en bogføring, men differencen i omkostningen udgiftsføres, så den glidende gennemsnitlige kostpris påvirkes ikke.

## <a name="negative-inventory-balances"></a>Negative lagersaldi

Transaktioner håndteres forskelligt, afhængigt af det nye disponible lagerantal, efter at transaktionen er negativ, nul eller positiv.

### <a name="new-balance-is-negative-or-zero"></a>Den nye saldo er negativ eller nul

Hvis det nye disponible lagerantal er negativt eller nul, efterkalkuleres posteringen med de aktuelle gennemsnitlige omkostninger. Hvis der er forskel på købsprisen og de aktuelle gennemsnitlige omkostninger, bogføres den til **Prisdifference for glidende gennemsnit**.

### <a name="new-balance-is-positive"></a>Ny saldo er positiv

Hvis det nye disponible lagerantal er positivt efter transaktionen, deles transaktionen i to dele og efterkalkuleres på en anden måde, som det er opsummeret i følgende tabel.

| Del | Beskrivelse |
|---|---|
| Antal fra negativ til nul | Lager bruger den aktuelle glidende gennemsnitlige omkostning for varen i stedet for transaktionsomkostningerne for den del af tilgangsantallet, der øger den disponible saldo fra negativ til nul. Differencen mellem transaktionsomkostningen og den aktuelle glidende gennemsnitlige omkostning bogføres til **Prisdifference for glidende gennemsnit**. |
| Antal fra nul til positiv | Lager bruger posteringsomkostningen for den del af tilgangsantallet, der øger lagerbeholdningssaldoen fra nul til positiv.                                                  |

## <a name="inventory-value-report"></a>Rapporten Lagerværdi

I dette eksempel på et glidende gennemsnit udskrives lagerværdirapporten for at understøtte den aktuelle glidende gennemsnitlige beregning for et produkt. Rapporten Lagerværdi kan udskrive posteringerne i kronologisk rækkefølge sammen med omkostningerne for at understøtte den glidende gennemsnitlige beregning af et produkt. Rapporten viser den glidende gennemsnitlige kostpris for produktet. I dialogboksen **Lagerværdirapporter** giver et datointerval dig mulighed at vælge den **Transaktionsklokkeslæt** eller **Bogføringsdato** til at sortere rapporten efter. Indstillingen **Bogføringsdato** viser, hvordan rapporten traditionelt udskrives. Indstillingen **Transaktionsklokkeslæt** er den faktiske dato, hvor transaktionen er rapporteret, og den glidende gennemsnitlige omkostning for produktet opdateres. Du kan udskrive rapporten Lagerværdi ved hjælp af indstillingen **Sortering af transaktionsklokkeslæt**, hvis du vil se den glidende gennemsnitlige omkostningsberegning over tid. Følgende tabel viser transaktionerne for det produkt, som rapporten udskrives for, når indstillingen **Sortering af transaktionsklokkeslæt** bruges.

| Transaktionsklokkeslæt | Dato         | Transaktionstype           | Antal | Beløb | Gennemsnitlig enhedskostpris |
|------------------|--------------|----------------------------|----------|--------|-------------------|
|                  | 1. oktober    | Primosaldo          | 0        | 0,00   | 0,00              |
| 8. oktober        | 28. september | Tilbagedateret kvittering          | 1        | 16,00  | 16,00             |
| 3. oktober        | 3. oktober    | Købskvittering           | 2        | 20,00  | 12,00             |
| 5. oktober        | 5. oktober    | Salgsordre                | -1       | -10,00 | 13,00             |
| 7. oktober        | 7. oktober    | Indkøbsfaktura           |          | 2,00   | 14,00             |
| 8. oktober        | 8. oktober    | Værdiregulering med glidende gennemsnit |          | 4.00   | 16.00             |
|                  | 31. oktober   | Sum                      | 2        | 32.00  | 16.00             |

> [!NOTE]
> Du kan ikke afstemme finansmodulet med lager ved hjælp af indstillingen **Sortering af transaktionsklokkeslæt**. Rapporten skal udskrives ved hjælp af indstillingen **Bogføringsdato**.
