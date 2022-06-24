---
title: Opmærksomhed mellem finansudligning og årsafslutning
description: Denne artikel indeholder oplysninger om forbedringer, der påvirker finansudligninger og finansårsafslutninger.
author: kweekley
ms.date: 04/06/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 30d3cc0bbd97cd006f12d06cda64ee63cb42252e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902510"
---
# <a name="awareness-between-ledger-settlement-and-year-end-close"></a>Opmærksomhed mellem finansudligning og årsafslutning

[!include [banner](../includes/banner.md)]


I Microsoft Dynamics 365 Finance version 10.0.25 er funktionen **Opmærksomhed mellem finansudligning og årsafslutning** tilgængelig i arbejdsområdet **Funktionsstyring**. Denne funktion tilføjer to primære forbedringer, der påvirker finansudligninger og finansårsafslutninger.

Ved finansårsafslutning medtages finansposteringer, der er udlignet, ikke længere i startsaldoen for det næste regnskabsår. Denne forbedring sikrer, at der kun inkluderes finansposteringer, der ikke er afstemt, i startsaldoen. Det er vigtigt, når der køres værdiregulering af udenlandsk valuta i finansmodulet. Værdiregulering af udenlandsk valuta køres kun for finansposteringer med statussen **Ikke udlignet**. Men før frigivelsen af funktionen **Opmærksomhed mellem finansudligning og årsafslutning**, opsummerede startsaldoen både posteringer, der har status af **Udlignet**, og dem, der har statussen **Ikke udlignet**, og statussen for det opsummerede beløb blev angivet til **Ikke udlignet**.

Den anden forbedring giver dig mulighed for at bogføre detaljerede startsaldoposteringer under finansårsafslutning. Hvis indstillingen **Behold detaljer ved årsslutning** er angivet til **Ja**, oprettes der en separat startsaldo for hver finanspostering, der ikke er udlignet. Denne indstilling defineres for hver hovedkonto i opsætningen af finansudligningen. Hvis du opbevarer detaljerede posteringer for startsaldoen, er det meget nemmere at kunne udligne de ikke-udlignede finansposteringer i det næste regnskabsår.

For at understøtte de nye forbedringer blev der foretaget ændringer i finansudligninger og årsafslutninger.

### <a name="changes-to-ledger-settlement"></a>Ændringer af finansudligning

- Finansudlign skal foretages inden for et regnskabsår.
- Finansudligning skal foretages for posteringer på en enkelt hovedkonto. Hovedkontoen er nu et påkrævet filter på siden **Finansudligning**.
- Finansudligning og tilbageførsel af finansudligning kan ikke udføres for posteringer, der bogføres inden for et afsluttet regnskabsår (det vil sige, at årsafslutningen er kørt).

### <a name="changes-to-year-end-close"></a>Ændringer i årsafslutning

- En årsafslutning kan ikke tilbageføres, hvis der er udlignet nogen startsaldoposteringer i det næste regnskabsår. Denne ændring gælder, når en årsafslutning tilbageføres, eller når en årsafslutning køres igen, og når indstillingen **Slet eksisterende ultimoposter ved fornyet lukning af året** angives til **Ja** i finansparametrene.
- Hvis indstillingen **Behold detaljer under årsafslutning** er angivet til **Ja** for en statuskonto i finansudligning, oprettes der mere detaljerede startsaldoposteringer for den pågældende hovedkonto.

## <a name="before-you-enable-the-feature"></a>Før du aktiverer funktionen

På grund af de ændrede funktioner og datamodellen er det vigtigt at overveje følgende, før du aktiverer funktionen:

- Da det kun er udlignede transaktioner, der er hentet frem i startsaldoen, skal du fjerne udligningen af transaktioner fra det indeværende regnskabsår, som er udlignet med transaktioner i det forrige regnskabsår. Transaktionerne skal udlignes igen i forhold til transaktioner i indeværende regnskabsår. Dette kan gøres ved hjælp af en reguleringspost i indeværende regnskabsår. Reguleringen tilbagefører de opsummerede startsaldi og modposterer med den detaljerede transaktion, der er nødvendig for at udligne finansposterne i indeværende år. 

  > [!IMPORTANT]
  > Hvis dette ikke er gjort, vil du modtage en **balancerer ikke**-fejl, når du kører årsslutslutning for det indeværende regnskabsår. Hvis det ikke er muligt at fjerne udligning og gentage udligning af finanstransaktionerne med samme regnskabsår, skal du først aktivere denne funktion, når årsafslutningen er gennemført. Aktivér funktionen umiddelbart efter, at årsafslutningen er fuldført, og før nye finanstransaktioner udlignes i det næste regnskabsår. 
  
- Alle posteringer, der er markeret til udligning, men som ikke er udlignet, får fjernet markeringen automatisk, når funktionen aktiveres. Du kan forhindre arbejdstab ved at udligne alle markerede posteringer, før du aktiverer funktionen.
- Nogle organisationer kører årsafslutningsprocessen flere gange for det samme regnskabsår. Du skal ikke aktivere funktionen, hvis årsafslutningen allerede er kørt en gang, og den vil blive kørt igen for samme regnskabsår. Funktionen skal være aktiveret, før du behandler den første årsafslutning, eller når du har behandlet den sidste årsafslutning for regnskabsåret.

  Hvis du vil aktivere funktionen, men årsafslutningen allerede er kørt en gang, skal du tilbageføre årsafslutningen, før du aktiverer funktionen.

- Da udligning på tværs af hovedkonti ikke længere er tilladt, skal du justere kontoplanen eller processerne efter behov for at sikre, at finansudligning kan foretages på den samme hovedkonto.
- Funktionen kan ikke aktiveres, hvis årsafslutningsprocessen for den offentlige sektor bruges.

## <a name="set-up-ledger-settlement"></a>Konfigurere finansudligning

Når du har aktiveret funktionen, og før du kører den næste årsafslutning, skal hver organisation bestemme, om den vil beholde posteringsoplysningerne i forbindelse med årsafslutningen. Valget har ingen indflydelse på startsaldoposteringer fra tidligere processer til årsafslutning.

Indstillingen **Behold detaljer under årsafslutning** angives for hver hovedkonto på siden **Opsætning af finansudligning**.

1.  Gå til **Finans** > **Opsætning Finans** > **Finansparametre**.
2.  Vælg **Finansudligningskonti** under fanen **Finansudligninger**.

-eller-

1.  Gå til **Finans** > **Periodiske opgaver** > **Finansudligninger**.
2.  Vælg **Finansudligningskonti**.

Der er føjet to kolonner til siden **Finansudligninger**:
    
- **Hovedkontotype** – Denne kolonne er udelukkende til orientering. Den viser den type, der er tildelt hovedkontoen.
- **Behold detaljer under årsafslutning** – Som standard er indstillingen angivet til **Nej**. Det kan kun angives til **Ja**, hvis værdien i kolonnen **Hovedkontotype** er **Balance**, **Aktiv** eller **Passiv**. Når indstillingen er angivet til **Nej**, bogføres startsaldi i oversigten, som det normalt er ved årsafslutning. Hvis den er angivet til **Ja**, oprettes startsaldi i detaljer for hver finanspostering, der ikke er udlignet for hovedkontoen.

## <a name="year-end-close"></a>Årsafslutning

Når du kører årsafslutningen ved at gå til **Finans** > **Periodeafslutning** > **Årsafslutning**, oprettes der startsaldi for de hovedkonti, der er defineret til finansudligning. Startsaldi oprettes i enten oversigt eller detaljer, afhængigt af opsætningen af finansudligning. Processen udelukker finansposteringer, der er udlignet, uanset om du bogfører startsaldoen for hver hovedkonto i oversigten eller i detaljer.

Der bogføres f.eks. flere posteringer på hovedkonto 130100 i regnskabsåret 2021.

| Kladdenummer | Bilag  | Date       | Type      | Finanskonto | Kontonavn        | Beskrivelse       | Valuta | Beløb i transaktionsvaluta | Antal  | Beløb i rapporteringsvaluta |
|----------------|----------|------------|-----------|----------------|---------------------|-------------------|----------|--------------------------------|---------|------------------------------|
| 20853          | FTV-3000 | 3-12-2021  | Igangværende | 130100-001-    | Debitor | Servicegebyr       | USD      | 100                            | 100     | 100                          |
| 20855          | FTV-3004 | 5-12-2021  | Igangværende | 130100-002-    | Debitor | Forbrugsomkostninger         | USD      | 175                            | 175     | 175                          |
| 20854          | CMV-4000 | 16-12-2021 | Igangværende | 130100-001-    | Debitor | Refusion            | USD      | -100                           | -100    | -100                         |
| 20851          | ARP-8000 | 20-12-2021 | Igangværende | 130100-002-    | Debitor |                   | USD      | -0,88                          | -0,88   | -0,88                        |
| 20853          | ARPM0004 | 20-12-2021 | Igangværende | 130100-002-    | Debitor |                   | EUR      | -127,11                        | -174,12 | -174,12                      |
| 20856          | CMV-4010 | 21-12-2021 | Igangværende | 130100-002-    | Debitor | Kredit på konto | USD      | -175                           | -175    | -175                         |
| 20857          | FTV-3011 | 28-12-2021 | Igangværende | 130100-001-    | Debitor | Forbrugsomkostninger         | USD      | 400                            | 400     | 400                          |
| 20910          | FTV-3020 | 29-12-2021 | Igangværende | 130100-002-    | Debitor | Service           | USD      | 300                            | 300     | 300                          |

Ud af disse posteringer udlignes tre ved finansudligning.

Der er en faktura på 175 USA dollars (USD 175). Denne faktura blev betalt i euro (EUR), og der blev foretaget en kasserabat.

| Kladdenummer | Bilag  | Date       | Type      | Finanskonto | Kontonavn        | Beskrivelse | Valuta | Beløb i transaktionsvaluta | Antal  | Beløb i rapporteringsvaluta |
|----------------|----------|------------|-----------|----------------|---------------------|-------------|----------|--------------------------------|---------|------------------------------|
| 20855          | FTV-3004 | 5-12-2021  | Igangværende | 130100-002-    | Debitor | Forbrugsomkostninger   | USD      | 175                            | 175     | 175                          |
| 20851          | ARP-8000 | 20-12-2021 | Igangværende | 130100-002-    | Debitor |             | USD      | -0,88                          | -0,88   | -0,88                        |
| 20853          | ARPM0004 | 20-12-2021 | Igangværende | 130100-002-    | Debitor |             | EUR      | -127,11                        | -174,12 | -174,12                      |

Resultaterne for hovedkonto 130100 afhænger af, om funktionen er aktiveret, før årsafslutningen køres. Hvis funktionen er aktiveret, afhænger resultatet også af indstillingen af Behold detaljer under årsafslutning.

### <a name="the-feature-isnt-enabled"></a>Funktionen er ikke aktiveret
Ved årsafslutningen oprettes der tre startsaldoposteringer for hovedkonto 130100 i 2022. Summen af posteringerne i regnskabsvalutaen er USD 525.

| Kladdenummer | Bilag  | Date     | Type    | Finanskonto | Kontonavn        | Beskrivelse | Valuta | Beløb i transaktionsvaluta | Antal  | Beløb i rapporteringsvaluta |
|----------------|----------|----------|---------|----------------|---------------------|-------------|----------|--------------------------------|---------|------------------------------|
| 20910          | YEC_2021 | 1/1/2022 | Åbner | 130100-002-    | Debitor |             | USD      | 299.12                         | 299.12  | 299.12                       |
| 20910          | YEC_2021 | 1/1/2022 | Åbner | 130100-001-    | Debitor |             | USD      | 400                            | 400     | 400                          |
| 20910          | YEC_2021 | 1/1/2022 | Åbner | 130100-002-    | Debitor |             | EUR      | -127,11                        | -174,12 | -174,12                      |

Selvom betalingsposteringen for EUR -127,11 blev udlignet i finansmodulet, kommer posteringen stadig frem som en startsaldo.

### <a name="feature-is-enabled-and-keep-detail-during-year-end-close--no"></a>Funktionen er aktiveret, og Behold detaljer under årsafslutning = Nej

Ved årsafslutningen oprettes der to startsaldoposteringer for hovedkonto 130100 i 2022. Summen af posteringerne i regnskabsvalutaen er stadig USD 525, men finansudlignede posteringer udelukkes fra startsaldoen. Totalbeløbet for konto 130100-002- er USD 125 i stedet for USD 299,12, og posteringen på EUR 127,11/USD 174,12 er helt udeladt.

| Kladdenummer | Bilag  | Date     | Type    | Finanskonto | Kontonavn        | Beskrivelse | Valuta | Beløb i transaktionsvaluta | Antal | Beløb i rapporteringsvaluta |
|----------------|----------|----------|---------|----------------|---------------------|-------------|----------|--------------------------------|--------|------------------------------|
| 20910          | YEC_2021 | 1/1/2022 | Åbner | 130100-002-    | Debitor |             | USD      | 125                            | 125    | 125                          |
| 20910          | YEC_2021 | 1/1/2022 | Åbner | 130100-001-    | Debitor |             | USD      | 400                            | 400    | 400                          |

### <a name="feature-is-enabled-and-keep-detail-during-year-end-close--yes"></a>Funktionen er aktiveret, og Behold detaljer under årsafslutning = Ja

Ved årsafslutningen oprettes der fem startsaldoposteringer for hovedkonto 130100 i 2022. Der oprettes en separat startsaldopostering for hver af de fem posteringer, som ikke er udlignet. Summen af posteringerne i regnskabsvalutaen er stadig USD 525.

| Kladdenummer | Bilag  | Date     | Type    | Finanskonto | Kontonavn        | Beskrivelse       | Valuta | Beløb i transaktionsvaluta | Antal | Beløb i rapporteringsvaluta |
|----------------|----------|----------|---------|----------------|---------------------|-------------------|----------|--------------------------------|--------|------------------------------|
| 20910          | YEC_2021 | 1/1/2022 | Åbner | 130100-001-    | Debitor | Servicegebyr       | USD      | 100                            | 100    | 100                          |
| 20910          | YEC_2021 | 1/1/2022 | Åbner | 130100-001-    | Debitor | Refusion            | USD      | -100                           | -100   | -100                         |
| 20910          | YEC_2021 | 1/1/2022 | Åbner | 130100-002-    | Debitor | Kredit på konto | USD      | -175                           | -175   | -175                         |
| 20910          | YEC_2021 | 1/1/2022 | Åbner | 130100-001-    | Debitor | Forbrugsomkostninger         | USD      | 400                            | 400    | 400                          |
| 20910          | YEC_2021 | 1/1/2022 | Åbner | 130100-002-    | Debitor | Service           | USD      | 300                            | 300    | 300                          |

Når posteringsoplysninger bevares, påvirkes de oprindelige detaljerede posteringer ikke. De er stadig bogført og ikke udlignet i det regnskabsår, der er ved at blive afsluttet. Der oprettes en kopi af disse posteringer til startsaldoen. Følgende værdier fra de oprindelige transaktioner kopieres til startsaldotransaktioner.

- Finanskonto (hovedkontoen og alle økonomiske dimensioner)
- Beløb i transaktions-, regnskabs- og rapporteringsvalutaer
- Beskrivelse
- Posteringslag
- Bogføringstype

   > [!NOTE]
   > Ingen andre startsaldoposteringer tildeles en bogføringstype. Derfor kan bogføringstypen bruges til at skelne mellem startposteringer, der er blevet videreført i detaljer.

Nogle felter fra de oprindelige posteringer skal ændres i startsaldoen med detaljerede posteringer. Datoen for startsaldoposteringer er altid den første dag i det næste regnskabsår. Kladdenummeret skal ændres, og bilagsnummeret ændres til den værdi, der blev angivet i dialogboksen til årsafslutningen.

Oplysninger fra de oprindelige posteringer kan findes på siden **Finansudligning**. Hver detaljerede startsaldopostering viser kolonnen **Oprindelig transaktionsdato** i gitteret. Denne kolonne kan hjælpe dig med at af matche posteringerne i det nye regnskabsår. Du kan vælge **Vis oprindeligt bilag** for at gå tilbage til hele det oprindelige bilag.

## <a name="settle-transactions"></a><a name="settle-transactions"></a>Udlign transaktioner
Du kan udligne finanstransaktionerne ved at følge disse trin.

1. Gå til **Finans** > **Periodiske opgaver** > **Finansudligninger**.
2.  Angiv filtrene øverst på siden.

    1. Vælg et datointerval. Eller vælg en datointervalkode for automatisk at udfylde datointervallet.

       - Datointervallet kan ikke gå på tværs af regnskabsår. Hvis datointervallet krydser regnskabsår, vises der ingen posteringer, når du vælger **Vis posteringer**.
       - Hvis datointervallet ligger i et åbent regnskabsår, kan posteringerne udlignes, og udligningen kan tilbageføres. Hvis datointervallet ligger inden for et lukket regnskabsår, eller hvis årsafslutningen er fuldført, vises posteringerne, men de kan ikke udlignes eller få ophævet udligning. Du kan kun fjerne markeringer af posteringer i et lukket regnskabsår. Hvis datointervallet ligger inden for et lukket regnskabsår, er knapperne **Markér valgte**, **Udlign markerede posteringer** og **Tilbagefør markerede posteringer** ikke tilgængelige.

    2. Vælg den hovedkonto, der skal vises posteringer for. Dette felt skal udfyldes. Opslaget viser kun de hovedkonti, der er valgt på siden **Finansudligning** for firmaets kontoplan.
    3. Vælg posteringslaget. Du kan ikke udligne posteringer, der findes i forskellige posteringslag.
    4. For at få vist hovedkontoen og dimensionerne i separate kolonner, skal du vælge et økonomisk dimensionssæt.

3.  Vælg **Vis posteringer** for at vise alle de posteringer, der matcher de filtre, du har angivet. Hvis du ændrer nogen af filtrene eller dimensionssættene, skal du vælge **Vis posteringer** igen.
4.  Vælg linjer til udligning. Værdien i feltet **Valgt beløb** øverst på siden forøges eller formindskes for at afspejle det samlede beløb på de linjer, du har valgt.
5.  Når du er færdig med at vælge posteringer, skal du vælge **Markér valgte**. Der vises en markering i kolonnen **Markeret** for hver postering, du har valgt. Værdien i feltet **Markeret beløb** over gitteret forøges eller formindskes for at afspejle det samlede beløb på de linjer, du har markeret.
6.  Når værdien i feltet **Markeret beløb** er **0** (nul), skal du vælge **Udlign markerede posteringer**.

    - Delvis udligning er ikke tilladt. Du kan f.eks. ikke udligne en $100 debiteringstransaktion mod en $90 kredittransaktion. Den resterende $10 kredittransaktion skal også markeres, så den kan medtages i udligningen.
    - Angiv en udligningsdato. Datoen skal være på eller efter den seneste dato for de posteringer, der er markeret til udligning.

Status for de markerede posteringer opdateres til **Udlignet**.

> [!IMPORTANT]
> Alle de posteringer, du har markeret til udligning for den aktive juridiske enhed og den valgte hovedkonto, udlignes. Transaktionerne behøver ikke at blive vist på siden. De udlignes, selvom de er skjult på grund af et filter.

Nogle processer, f.eks. tilbageførsel af en postering, udligner automatisk finansposteringer. En betaling og en faktura udlignes f.eks. i Debitor, og udligningen genererer realiseret gevinst/tab. Udligningen af betalingen og fakturaen udligner ikke finansposteringer som f.eks. posteringer på debitorfinanskontoen. Hvis betalingen og fakturaen ikke er udlignet i Debitor, vil den regnskabspost for tilbageførsel, der blev bogført under tilbageførslen af debitorudligningen, medføre, at de oprindelige og tilbageførte regnskabsposter udlignes i Finans. Når funktionen **Opmærksomhed mellem finansudligning og årsafslutning** er aktiveret, vil finansudligning af en tilbageførsel ikke automatisk finde sted, hvis tilbageførselsdatoen ligger i et andet regnskabsår.

## <a name="use-excel-for-ledger-settlement"></a>Bruge Excel til finansudligning

Posteringer, der vises på siden **Finansudligning**, kan eksporteres til Excel. I Excel kan du yderligere filtrere posteringer for at finde ud af, hvilke posteringer der skal markeres til udligning.
Begge finansudligningsenheder eksporterer kun finansposteringer for den hovedkonto, der er valgt på siden **Finansudligning**. Selvom posteringer for lukkede regnskabsår stadig kan markeres eller få fjernet markering ved hjælp af Excel, kan de ikke udlignes. Udlignede posteringer kan heller ikke tilbageføres for det pågældende regnskabsår.

## <a name="make-transactions-easier-to-find"></a>Gøre posteringer nemmere at finde

Siden **Finansudligninger** indeholder funktioner, der gør det nemmere at få vist de posteringer, du skal bruge til udligning.

•   Brug filteret **Markeret** til at filtrere posteringer afhængigt af, om afkrydsningsfeltet **Markeret** er valgt for dem.
•   Brug filteret **Status** til at filtrere posteringer på baggrund af deres status.
•   Vælg **Sortér efter absolut beløb** for at sortere beløbene efter absolut værdi. På denne måde kan du gruppere debet- og kreditbeløb med samme beløb.

## <a name="reverse-a-settlement"></a>Tilbageføre en udligning

Du kan tilbageføre en udligning, der er foretaget ved en fejl.

1.  Følg trin 1 til og med 3 i sektionen [Udligne posteringer](#settle-transactions) for at få vist de posteringer, du er interesseret i.
2.  Vælg **Udlignet** i filteret **Status**.
3.  Vælg linjer til tilbageførsel.
4.  Vælg **Tilbagefør markerede posteringer**. Statussen for alle posteringer, der har samme udlignings-id, opdateres til **Ikke udlignet**.

> [!IMPORTANT]
> Alle posteringer, der har samme udlignings-id, tilbageføres, selvom de ikke er markeret. Der er f.eks. markeret og udlignet fire linjer. Alle fire linjer har samme udlignings-id. Hvis du markerer en af de fire linjer og derefter vælger **Tilbagefør markerede posteringer**, tilbageføres alle fire linjer.






