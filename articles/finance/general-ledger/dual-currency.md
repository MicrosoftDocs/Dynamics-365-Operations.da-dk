---
title: Dobbelt valuta
description: Dette emne indeholder oplysninger om såkaldt dobbelt valuta, hvor rapporteringsvalutaen bruges som en ekstra regnskabsvaluta i Microsoft Dynamics 365 Finance.
author: kweekley
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, Ledger, AssetTransReportingCurrencyAmountsWizard,BankAccountTransReportingCurrencyAmountsWizard, LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-10
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 04738d2fe88fef5c0e96a39febfec86fab3bee7d
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/05/2022
ms.locfileid: "8713564"
---
# <a name="dual-currency"></a>Dobbelt valuta

[!include [banner](../includes/banner.md)]

Funktioner, der blev introduceret i Microsoft Dynamics 365 for Finance and Operations version 8.1 (oktober 2018) giver mulighed for at bruge rapporteringsvalutaen til andre formål og som endnu en regnskabsvaluta. Denne funktion kaldes *dobbelt valuta*. Ændringerne i forbindelse med den dobbelte valuta kan ikke deaktiveres via en konfigurationsnøgle eller parameter. Da rapporteringsvalutaen bruges som en ekstra regnskabsvaluta, er den måde, som rapporteringsvalutaen beregnes i bogføringslogikken, blevet ændret.

En række moduler til registrering, rapportering og brug af rapporteringsvalutaen i de forskellige processer er desuden blevet forbedret. De påvirkede moduler omfatter:

- Finans 
- Økonomirapportering 
- Kreditor
- Debitor 
- Kontant- og bankstyring 
- Anlægsaktiver 
- Konsolideringer

Efter en opgradering skal du fuldføre bestemte trin for Kontant- og bankstyring og Anlægsaktiver. Derfor skal du læse og forstå de relevante afsnit i dette emne omhyggeligt.

## <a name="posting-process"></a>Bogføringsproces

Bogføringslogikken er blevet ændret for alle transaktioner, der genererer en regnskabspost i Finans. Her kan du se, hvordan rapporteringsvalutaen tidligere blev beregnet:

Transaktionsvalutabeløb \> Regnskabsvalutabeløb \> Beløb i rapporteringsvaluta

En transaktion angives for eksempel i canadiske dollar (valutaen CAD). CAD-beløbet omregnes til regnskabsvalutaen, som er i amerikanske dollar (USD). USD-beløbet omregnes derefter til rapporteringsvalutaen, som er i euro (EUR). Derfor skal valutakurserne findes mellem CAD og USD og mellem USD og EUR.

Her er den nye beregning:

Transaktionsvalutabeløb \> Regnskabsvalutabeløb

Transaktionsvalutabeløb \> Rapporteringsvalutabeløb

På grund af denne ændring skal valutakurserne nu findes mellem CAD og USD og mellem CAD og EUR.

## <a name="reports-and-inquiries"></a>Rapporter og forespørgsler

Forskellige rapporter og forespørgsler viser nu både rapporteringsvalutabeløb og regnskabsvalutabeløb. Ikke alle rapporter og forespørgsler er blevet opdateret. For eksempel er rapporter, der kun viser beløb i transaktionsvalutaen, ikke blevet ændret.

Ændringerne følger et af to mønstre:

- Hvis der er plads i rapporten eller forespørgslen til at vise beløb i både regnskabsvalutaen og rapporteringsvalutaen, er rapporteringsvalutabeløbene blevet tilføjet.
- Hvis der ikke var tilstrækkelig plads i rapporten eller forespørgslen til at vise beløb i begge valutaer, er der tilføjet en indstilling, så brugere kan vælge, hvilken valuta der skal vises.

Der er også tilføjet logik til forskellige rapporter og forespørgsler for at forhindre, at rapporteringsvalutabeløbene vises, hvis rapporteringsvalutaen er den samme som regnskabsvalutaen, eller hvis rapporteringsvalutaen ikke er defineret i Finans for den juridiske enhed.

## <a name="financial-journals"></a>Økonomikladder

Økonomikladder, f.eks. finanskladden og kreditorfakturakladden, er blevet opdateret, så de indeholder yderligere oplysninger om rapporteringsvalutaen. Totaler for bilag og kladde vises nu i rapporteringsvalutaen. Derudover vises oplysninger om rapporteringsvalutaens valutakurs nu under fanen **Generelt** i kladdelinjerne. Derfor kan du tilsidesætte rapporteringsvalutaens valutakurs, når du angiver posteringer.

## <a name="vendor-invoices-sales-orders-and-sales-agreements"></a>Kreditorfakturaer, salgsordrer og salgsaftaler
Kreditorfakturaer, salgsordrer og salgsaftaler er blevet opdateret, så de indeholder en fast valutakurs for rapporteringsvalutaen. Der kan defineres en fast valutakurs for både regnskabsvalutaen og rapporteringsvalutaen, når transaktionsvalutaen er forskellig fra dem. Når regnskabsvalutaen og rapporteringsvalutaen er den samme, synkroniseres den faste valutakurs ved at bruge regnskabsvalutaens faste kurs som rapporteringsvalutaens faste kurs. Den faste valutakurs for rapporteringsvalutaen kan ikke ændres for denne konfiguration. Når regnskabsvalutaen og rapporteringsvalutaen er forskellige, kan der defineres en fast valutakurs for både regnskabsvalutaen og rapporteringsvalutaen under transaktionen. Hvis rapporteringsvalutaen ikke er defineret i finansmodulet, er feltet **Fast valutakurs for rapporteringsvaluta** ikke aktiveret, og der beregnes ikke et beløb for rapporteringsvalutaen.

## <a name="module-changes"></a>Ændringer af moduler

Følgende moduler bruger rapporteringsvalutaen som en ekstra regnskabsvaluta:

- [Finans](#general-ledger)
- [Økonomirapportering](#financial-reporting)
- [Kreditorer](#accounts-payable-and-accounts-receivable)
- [Debitor](#accounts-payable-and-accounts-receivable)
- [Kontant- og bankstyring](#cash-and-bank-management)
- [Anlægsaktiver](#fixed-assets)
- [Konsolideringer](#consolidations)

### <a name="general-ledger"></a>Finans

Hvis en rapporteringsvaluta er defineret i finans, har finansmodulet allerede registreret rapporteringsvalutabeløb i alle regnskabsposter. Disse beløb oversættes imidlertid nu fra transaktionsvalutabeløbene.

Følgende yderligere ændringer er foretaget i **Finans**-modulet:

- En separat valutakurstype for rapporteringsvalutaen kan defineres i finans. Hvis en organisation ikke vil bruge en anden valutakurstype, kan du lade feltet for valutakurstypen for rapporteringsvalutaen være tomt. Du kan også vælge den samme valutakurstype som den, der bruges til regnskabsvalutaen. Hvis du lader feltet stå tomt, bruger systemet valutakurstypen for regnskabsvalutaen.
- I en ny kladde, Reguleringskladde for rapporteringsvaluta, kan reguleringer kun bogføres på finanskonti i rapporteringsvalutaen. I kladden kan der kun bogføres til finanskonti. Kladden understøtter ikke interne bogføringer, og valutaen skal være rapporteringsvalutaen for den juridiske enhed, hvor kladden bogføres. Når kladden er bogført, er posteringsvaluta- og regnskabsvalutabeløbene 0 (nul), og rapporteringsvalutabeløbet bogføres med det beløb, der er angivet i posteringen. Da den måde rapporteringsvalutaen bruges i modulerne **Kreditor**, **Debitor** og **Anlægsaktiver** er ændret, kan du bruge denne kladde for reguleringer efter en opgradering. Eksempler på, hvordan du kan bruge denne kladde, finder du i afsnittene for disse moduler.
- Processen for periodefordeling er blevet opdateret, så der kan allokeres beløb i transaktions-, regnskabs- og rapporteringsvalutaerne. Tidligere blev beløb tildelt i transaktions- og regnskabsvalutaerne, og derefter blev regnskabsvalutabeløbet oversat til rapporteringsvalutaen. Denne funktionsmåde kunne forårsage, at en saldo forblev i rapporteringsvalutaen på finanskontoen. Nu, når beløbene beregnes og anvendes i regnskabsposten, foregår der ingen oversættelse.
- Processen til værdiregulering af udenlandsk valuta har allerede reguleret beløb i rapporteringsvalutaen. Dog beregnes rapporteringsvalutabeløbet nu via transaktionsvalutabeløbet som beskrevet i afsnittet [Bogføringsproces](#posting-process) tidligere i dette emne.
- Mange rapporter og forespørgsler i Finans havde allerede rapporteringsvalutaen, men nogle få havde den ikke. Et eksempel er listesiden **Råbalance**. Denne listeside omfatter nu kolonner til både regnskabsvalutaen og rapporteringsvalutaen. Bemærk, at kolonnerne til rapporteringsvalutaen er skjult, hvis regnskabsvalutaen og rapporteringsvalutaen er den samme, eller hvis der ikke blev defineret en rapporteringsvaluta i finans.

### <a name="financial-reporting"></a>Økonomirapportering

Med en udvidelse til modulet **Regnskabsaflæggelse** kan du medtage rapporteringsvalutabeløbet i et regnskab på to måder. I kolonnedefinitionen kan du rapporterer direkte om de rapporteringsvalutabeløb, der er bogført i finans (nye funktioner). Alternativt kan du fortsætte med at oversætte beløb fra regnskabsvalutaen til rapporteringsvalutaen (eksisterende funktionalitet).

Denne ændring er tilgængelig via indstillingen **Valutavisning** i kolonnedefinitionen. Hvis du vælger **Rapporteringsvaluta fra Finans**, oversættes beløbene i kolonnen ikke. I stedet rapporteres de direkte fra finans. Hvis kolonnen skal vise oversatte beløb, skal du vælge indstillingen **Oversæt til XXXX**, hvor *XXXX* er den rapporteringsvaluta, som kolonnen skal vise. I dette tilfælde oversættes regnskabsvalutabeløb til den valgte valuta ved hjælp af den eksisterende oversættelsesfunktionalitet.

### <a name="accounts-payable-and-accounts-receivable"></a>Debitor og kreditor

Modulerne **Kreditor** og **Debitor** kunne i forvejen registrere rapporteringsvalutabeløb. Beløbene bliver dog ikke vist eller brugt til forskellige processer. Der er foretaget følgende ændringer:

- Rapporteringsvalutabeløb vises nu i posteringer for både debitorer og kreditorer. Rapporteringsvalutabeløb vises også i den åbne saldo for hver transaktion.
- Aldersfordelingsprocessen er blevet opdateret, så en organisation kan få vist aldersfordelte filsæt i enten regnskabsvalutaen eller rapporteringsvalutaen.
- Forskellige forespørgsler og rapporter er opdateret, så de viser rapporteringsvalutabeløb. Eksempler er rapporterne **Debitor finans-afstemning** og **Kreditor til finansafstemning**.
- Processen til værdiregulering af udenlandsk valuta har allerede reguleret beløb i rapporteringsvalutaen. Dog beregnes rapporteringsvalutabeløbet nu via transaktionsvalutabeløbet som beskrevet i afsnittet [Bogføringsproces](#posting-process).
- **Opgraderingsovervejelse:** Før en opgradering beregnes rapporteringsvalutabeløb for dokumenter (fakturaer, betalinger osv.) ved hjælp af regnskabsvalutaen. F.eks. bogføres en faktura, før en organisation opgraderer, og fakturaen betales ikke. Under opgraderingen ændres fakturaens regnskabspost ikke. Men efter opgraderingen er ændringerne for dobbelt valuta trådt i kraft. Derfor, når der foretages en betaling for fakturaen, beregnes betalingens rapporteringsvalutabeløb nu via transaktionsvalutabeløbet. Når betalingen og fakturaen udlignes, kan der blive beregnet en lille difference i beløbet for realiseret gevinst/tab, fordi rapporteringsvalutabeløb nu beregnes forskelligt. Hvis den difference, der beregnes, anses for at være betydelig, kan den nye Reguleringskladde for rapporteringsvaluta kun bruges til at justere saldoen for realiseret gevinst/tab og kreditor/debitorfinanskonti i rapporteringsvalutaen.

### <a name="cash-and-bank-management"></a>Kontant- og bankstyring

Tidligere sporede **Kontant- og bankstyring**-modulet ikke nogen rapporteringsvalutabeløb for posteringer, der blev bogført i forhold til hver enkelt bankkonto. Efter en opgradering spores rapporteringsvalutabeløb automatisk for enhver ny transaktion, der bogføres. Dog skal rapporteringsvalutabeløb føjes til tidligere bogførte posteringer i reskontrokladden.

- **Opgraderingsovervejelser:** Fordi bankkontotransaktioner ikke tidligere registrerede rapporteringsvalutabeløb i reskontrokladden, er en guide blevet tilføjet, så du kan føje rapporteringsvalutabeløb til bankkontotransaktioner. Denne guide bogfører **ikke** i finans igen. I stedet tager den rapporteringsvalutabeløb fra finans og opdaterer dem i reskontrotabellerne.

    - Du starter guiden ved at vælge **Kontant- og bankstyring** \> **Konfiguration** \> **Føj rapporteringsvalutabeløb til bankkontotransaktioner**.
    - Guiden viser transaktioner for alle bankkonti i det aktuelle regnskab, der har et rapporteringsvalutabeløb på 0 (nul). Kun posteringer, der er bogført inden opgraderingen, medtages.
    - For hver bankkontotransaktion finder guiden de tilsvarende regnskabsposter i finansmodulet og angiver et standardrapporteringsvalutabeløb. Selvom beløbene kan redigeres, anbefales det **ikke** at redigerer dem. Ellers kan du muligvis ikke afstemme bankkontosaldi i finans. Det eneste tidspunkt, du skal redigere et beløb, er, hvis rapporteringsvalutabeløbet ikke bliver fundet i finans. Guiden viser i så fald et beløb på 0 (nul) for rapporteringsvalutaen.
    - Hvis du vælger **Annuller** i guiden, gemmes bankkontotransaktionerne, og eventuelle ændringer af rapporteringsvalutabeløbene gemmes, indtil næste gang du kører guiden. Rapporteringsvalutabeløbene opdateres dog ikke for bankkontotransaktionerne. Denne opdatering sker kun, når du vælger **Udfør** i guiden. Du kan bruge guiden flere gange. Derfor kan du rette eventuelle forkerte rapporteringsvalutabeløb, hvis du laver en fejl.

- Ingen processer i Kontant- og bankstyring er blevet ændret, men forskellige rapporter og forespørgsler er blevet opdateret, så de viser rapporteringsvalutabeløb. Likviditetsbudgetteringsrapporterne er en undtagelse. De er ikke blevet opdateret til at indeholde rapporteringsvalutabeløbene.

### <a name="fixed-assets"></a>Anlægsaktiver

Tidligere sporede **Anlægsaktiver**-modulet ikke nogen rapporteringsvalutabeløb for posteringer, der blev bogført i forhold til hvert anlægskartotek. Efter en opgradering spores rapporteringsvalutabeløb automatisk for enhver ny transaktion, der bogføres. Dog skal rapporteringsvalutabeløb føjes til tidligere bogførte posteringer i reskontrokladden.

Desuden er der foretaget større ændringer i forbindelse med afskrivningsprocessen. Disse ændringer kræver brugerhandling efter en opgradering. Det er vigtigt, at du læser og forstår følgende ændringer, selvom du endnu ikke bruger Anlægsaktiver.

- Den måde, afskrivningsprocessen bestemmer rapporteringsvalutabeløbet, er blevet ændret. I følgende scenario sammenlignes, hvordan afskrivning tidligere fastsatte rapporteringsvalutabeløbet, og hvordan rapporteringsvalutabeløbet bestemmes nu.



    **Afskrivningscenario**

    Et aktiv anskaffes og bogføres med følgende beløb. Bemærk, at rapporteringsvalutabeløbet bogføres i finans, men at det er ikke gemmes i tabellerne for reskontro for anlægsaktiver.

    | Posteringstype | Transaktionsbeløb | Valutakurs | Regnskabsvalutabeløb | Valutakurs | Rapporteringsvalutabeløb |
    |------------------|--------------------|---------------|----------------------------|---------------|---------------------------|
    | Anskaffelse      | 1.000.000 DKK      | 2,0           | 500.000 USD                | 2,5           | 200.000 EUR               |

    **Tidligere afskrivning for rapporteringsvalutaen**

    Ved årets udgang køres afskrivningsforslaget og beregner følgende beløb.

    | Posteringstype | Transaktionsbeløb | Valutakurs | Regnskabsvalutabeløb | Valutakurs | Rapporteringsvalutabeløb |
    |------------------|--------------------|---------------|----------------------------|---------------|---------------------------|
    | Afskrivning     | 50.000 USD         | 1.0           | 50.000 USD                 | 2,6           | 19.230,77 EUR             |

    Når afskrivningsforslaget køres, beregner det regnskabsvalutabeløbet ved hjælp af afskrivningsmetoden. Derefter oversætter dette beløb til rapporteringsvalutaen ved hjælp af den aktuelle valutakurs mellem USD og EUR. Denne oversættelse giver problemer, fordi aktivet ikke kan afskrives fuldt ud i rapporteringsvalutaen, når spotkursen bruges.

    **Ny afskrivning for rapporteringsvalutaen**

    Afskrivningsprocessen er blevet ændret, så rapporteringsvalutabeløbet også beregnes ved hjælp af afskrivningsmetoden. Her er resultaterne, når der køres afskrivning på aktivet.

    | Posteringstype | Transaktionsbeløb | Valutakurs | Regnskabsvalutabeløb | Valutakurs                                                       | Rapporteringsvalutabeløb |
    |------------------|--------------------|---------------|----------------------------|---------------------------------------------------------------------|---------------------------|
    | Afskrivning     | 50.000 USD         | 1.0           | 50.000 USD                 | 2,5<blockquote>[!NOTE] Selvom denne valutakurs vises, bruges den ikke til at oversætte til rapporteringsvalutaen.</blockquote> | 20.000 EUR                |

    Når afskrivningsforslaget køres, beregnes både regnskabsvalutabeløbet og rapporteringsvalutabeløbet ved hjælp af afskrivningsmetoden. Beløbene bruges derefter af regnskabsposten i Finans. Der foretages ingen oversættelse for at bestemme rapporteringsvalutabeløbet.

- **Opgraderingsovervejelser:** Fordi anlægskartotektransaktioner ikke tidligere registrerede rapporteringsvalutabeløbet, er en guide blevet tilføjet, så du kan føje rapporteringsvalutabeløb til anlægskartotektransaktioner. Denne guide bogfører **ikke** i finans igen. Da den måde, som afskrivningsforslaget beregner rapporteringsvalutabeløb, er ændret, **skal** guiden køres og skal fuldføres for hvert regnskab, før en organisation kan angive nogen afskrivningstransaktioner.

    - Start guiden ved at vælge **Anlægsaktiver** \> **Konfiguration** \> **Føj rapporteringsvalutabeløb til anlægskartoteker**.
    - Guiden viser transaktioner for alle anlægskartoteker i det aktuelle regnskab, der har et rapporteringsvalutabeløb på 0 (nul). Kun posteringer, der er bogført inden opgraderingen, medtages.
    - Guiden trækker **ikke** rapporteringsvalutabeløbene fra finansregnskabet. Som beskrevet i det forrige scenario bruger de rapporteringsvalutabeløb, der oprindeligt blev bogført i Finans, spotkursen forkert. Disse beløb bør ikke figurere i reskontro for anlægsaktivet, fordi næste afskrivningsberegning bruger de forkerte beløb. I stedet finder guiden valutakursen på datoen for den første anskaffelse. Derefter bruges den pågældende valutakurs til at anbefale det rapporteringsvalutabeløb, der skal bogføres i reskontrokladden. Her er f.eks., hvad guiden kan vise for det forrige scenario.

        | Anlægsaktiv | Kartotek      | Posteringstype | Posteringsdato | Valuta | Beløb i transaktionsvaluta | Beløb  | Valutakurs | Rapporteringsvalutabeløb |
        |-------------|-----------|------------------|------------------|----------|--------------------------------|---------|-----------|---------------------------|
        | BUIL-00001  | 200\_SLLT | Anskaffelse      | 6/3/2016         | DKK      | 1.000.000                      | 500,000 | 2.5       | 250,000                   |
        | BUIL-00001  | 200\_SLLT | Afskrivning     | 6/3/2016         | USD      | 50,000                         | 50,000  | 2.5       |  25,000                   |
        | BUIL-00001  | 200\_SLLT | Afskrivning     | 6/3/2016         | USD      | 50,000                         | 50,000  | 2.5       |  25,000                   |
        | BUIL-00001  | 200\_SLLT | Afskrivning     | 6/3/2016         | USD      | 50,000                         | 50,000  | 2.5       |  25,000                   |

    - Mange kunder sporer deres aktivtransaktionsoplysninger i projektmapper. Disse oplysninger omfatter valutakurser og beløb. Hvis du har disse data i en projektmappe, kan du oprette en brugerdefineret valutakurstype og opdatere den med valutakurserne fra projektmappen. Denne valutakurstype bruges derefter til at angive en standardvalutakurs på anskaffelsesdatoen og beregne rapporteringsvalutabeløbet. Hvis der ikke er valgt en valutakurstype, bruger guiden den valutakurstype, der blev defineret i Finans.
    - Valutakursen og rapporteringsvalutabeløbene kan ændres. Hvis valutakursen ændres, genberegnes rapporteringsvalutabeløbet ved hjælp af den nye kurs.
    - Hvis du vælger **Annuller** i guiden, gemmes anlægskartotekstransaktionerne, og eventuelle ændringer af valutakursen eller rapporteringsvalutabeløbene gemmes, indtil næste gang du kører guiden. Rapporteringsvalutabeløbene opdateres dog ikke for anlægskartotekstransaktionerne. Denne opdatering sker kun, når du vælger **Udfør** i guiden. Du kan bruge guiden flere gange. Derfor kan du rette eventuelle forkerte rapporteringsvalutabeløb, hvis du laver en fejl.
    - Når rapporteringsvalutabeløb er opdateret helt i reskontro, **skal** du indstille **Har du opdateret alle de rapporteringsvalutabeløbene på anlægskartotekstransaktionerne?** til **Ja** og derefter vælge **Udfør**. Afskrivningsberegninger kan ikke fuldføres, før du har indstillet **Har du opdateret alle de rapporteringsvalutabeløbene på anlægskartotekstransaktionerne?** til **Ja**. Når denne indstilling er sat til **Ja**, er guiden ikke længere tilgængelig.
    - Når anlægsaktivposteringerne i reskontro opdateres med rapporteringsvalutabeløb, svarer disse beløb ikke til de beløb, der oprindeligt blev bogført i Finans. Reguleringskladden for rapporteringsvaluta kan dog bruges til at opdatere saldiene for afskrivningsfinanskontiene i finans, så de stemmer overens med de beløb, der oprindeligt blev bogført.
    - En ny enhed for **Beløb i rapporteringsvaluta for aktivtransaktion**, som er tilføjet i **Datastyring**-arbejdsområdet, gør det muligt at eksportere dataene fra guiden. Du kan derefter bruge dataene til at bestemme saldoen i reskontro for anlægsaktiver for afskrivningsposteringerne. Denne saldo kan derefter bruges til at bestemme beløbet for rapporteringsvalutareguleringen i finansmodulet.

- **Opgraderingsovervejelse:** Nye opsætningsfelter er føjet til anlægsaktiver, og de bruges ved afskrivningsberegningen. Du skal muligvis opdatere disse felter inden næste afskrivningsberegning.

    - I anlægskartoteket (**Anlægsaktiver** \> **Bøger**) indeholder oversigtspanelet **Generelt** et nyt **Anskaffelsespris i rapporteringsvaluta**-felt.
    - I anlægskartoteket (**Anlægsaktiver** \> **Bøger**) indeholder oversigtspanelet **Afskrivning** et nyt **Forventet scrapværdi i rapporteringsvaluta**-felt.
    - I parametrene for anlægsaktivet (**Anlægsaktiver** \> **Konfiguration** \> **Anlægsaktivernes parametre**) har oversigtspanelet **Generelt** et nyt **Mindste afskrivningsbeløb i rapporteringsvaluta**.
    - I Bøger (**Anlægsaktiver** \> **Konfiguration** \> **Bøger**) har oversigtspanelet **Generelt** to nye felter: **Afrund afskrivning i rapporteringsvaluta** og **Behold bogført nettoværdi i rapporteringsvaluta**.

- Da afskrivningsforslaget nu beregner beløb i både regnskabsvalutaen og rapporteringsvalutaen, er anlægsaktivkladden opdateret, så den viser afskrivningsbeløbene i rapporteringsvalutaen. Transaktionsvalutaen er altid regnskabsvalutaen ved afskrivningsposteringer. Derfor vil disse beløb fortsat blive vist i kolonnerne **Debet** og **Kredit**. To nye kolonner, **Debet i rapporteringsvaluta** og **Kredit i rapporteringsvaluta**, er føjet til gitteret.

    - De nye felter er tilgængelige, når posteringstypen er en af de fire afskrivningstyper: **Afskrivning**, **Afskrivningsregulering**, **Ekstraordinær afskrivning** eller **Særlig afskrivning**.
    - Hvis der angives en afskrivningsposteringstype i anlægsaktivkladden, vises rapporteringsvalutabeløbene i de nye kolonner. Disse beløb kan ændres.
    - Hvis regnskabsvalutaen og rapporteringsvalutaerne i Finans er ens, vil beløbene blive holdt synkroniserede. Hvis du ændrer beløbet i **Kredit**, bliver beløbet i **Kredit i rapporteringsvaluta** automatisk ændret, så det passer til det.
    - Hvis der er angivet en anden posteringstype i anlægsaktivkladden, vises beløbene i **Debet i rapporteringsvaluta** og **Kredit i rapporteringsvaluta** aldrig, hverken før eller efter bogføringen. Regnskabsvaluta- og rapporteringsvalutabeløbene er stadig tilgængelige i det bilag, der bogføres i Finans.
    
### <a name="consolidations"></a>Konsolideringer
    
Funktionalitet, der blev introduceret i Dynamics 365 Finance version 10.0.5 (oktober 2019), giver mulighed for funktionsstyring med forbedret fleksibilitet til konsolidering og dobbelt valuta. Hvis du vil aktivere denne funktion, skal du gå til arbejdsområdet **Administration af funktioner** og vælge **Aktivér dobbelt valuta-funktionalitet i finanskonsolidering**.

I finanskonsolidering er der tilføjet en ny indstilling til konsolidering af enten regnskabs- eller rapporteringsvalutabeløb fra kildefirmaerne. Hvis regnskabs- eller rapporteringsvalutaen er den samme som regnskabs- eller rapporteringsvalutaen i det konsoliderede regnskab, vil beløbene blive kopieret direkte i stedet for omregnet.

-  Du kan nu vælge, om du vil bruge regnskabsvalutaen eller rapporteringsvalutaen fra kilderegnskabet som transaktionsvaluta i det konsoliderede regnskab.

- Regnskabs- eller rapporteringsvalutabeløbene fra kildefirmaet bliver kopieret direkte til regnskabs- eller rapporteringsvalutabeløbene i det konsoliderede regnskab, hvis én af valutaerne er den samme. Regnskabs- og rapporteringsvalutabeløbene i det konsoliderede regnskab beregnes ved hjælp af valutakursen, hvis ingen af valutaerne er den samme.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
