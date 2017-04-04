---
title: "Værdiregulering af udenlandsk valuta for Finans"
description: "Dette emne indeholder en oversigt over følgende til finansmodulet udenlandsk valuta værdiregulering proces - installation, kører processen beregning for processen, og hvordan du kan tilbageføre værdireguleringsposteringerne, hvis det er nødvendigt."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CurrencyLedgerGainLossAccount
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62153
ms.assetid: 842e8561-560f-4cc6-8668-70cca60b1ba3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: 5d6d13fe44eef7766b4dcaf274c3522bce3da816
ms.lasthandoff: 03/31/2017


---

# <a name="foreign-currency-revaluation-for-general-ledger"></a>Værdiregulering af udenlandsk valuta for Finans

Dette emne indeholder en oversigt over følgende til finansmodulet udenlandsk valuta værdiregulering proces - installation, kører processen beregning for processen, og hvordan du kan tilbageføre værdireguleringsposteringerne, hvis det er nødvendigt. 

I en periodeafslutning kræver regnskabsmæssige konventioner finanskontosaldi i fremmede valutaer, der reguleres ved hjælp af forskellige valutakurstyper (aktuelle, historiske, gennemsnit, osv.). For eksempel kræver en regnskabskonvention, at aktiver og passiver værdiansættes på ny ved den aktuelle valutakurs, anlægsaktiver ved den historiske valutakurs og driftskonti på det månedlige gennemsnit. Værdiregulering af udenlandsk valuta i Finans kan bruges til at regulere balancen og resultatopgørelseskonti. 

> [!NOTE]
> Værdiregulering af udenlandsk valuta er også tilgængelige i modulet Debitor (AR) og kreditor (AP). Hvis du bruger disse moduler, bør de udestående transaktioner, der reguleres ved hjælp af værdireguleringen af udenlandsk valuta i disse moduler. Værdiregulering af udenlandsk valuta i Debitor og Kreditor opretter en regnskabspost i Finans for at afspejle urealiseret gevinst eller tab og sikre, at reskontroer og Finans kan afstemmes. Da værdireguleringen af udenlandsk valuta i Debitor og Kreditor opretter regnskabsposter i Finans, skal debitor- og kreditorhovedkonti udelukkes fra finansmodulets værdiregulering af udenlandsk valuta. 

Når du kører processen til værdiregulering, reguleres saldoen i hver hovedkonto, der er bogført i udenlandsk valuta. De transaktioner for ikke-realiseret gevinst eller tab, der oprettes under værdireguleringsprocessen, er genereret af systemet. To posteringer kan oprettes, én for regnskabsvalutaen og en anden for rapporteringsvaluta, hvis det er relevant. Hver regnskabsposten bogføres Urealiseret gevinst eller tab, og den hovedkonto, der værdireguleres.

## <a name="prepare-to-run-foreign-currency-revaluation"></a>Klargøre kørsel af værdiregulering af udenlandsk valuta
Før du kan køre processen til værdiregulering, kræves følgende konfiguration.

-   På siden **Hovedkonto**:
-   Vælg **Værdiregulering af udenlandsk valuta** i finans, hvis hovedkontoen skal værdireguleres. Hvis den primære konto ikke bør reguleres (f.eks. for Debitor og Kreditor, hvis den reguleres i reskontroer), skal du fjerne markeringen i afkrydsningsfeltet.
-   Hvis hovedkontoen er markeret til værdiregulering, skal du angive den **valutakurstypen**. Denne valutakurstype bruges til regulering af hovedkontoen. Et særskilt felt **Valutakurstype for økonomirapportering** er tilgængeligt for økonomirapportering. De to felter holdes ikke synkroniseret, så der er mulighed for forskellige valutakurstyper til værdiregulering og økonomirapportering.

-   På siden **Finans**:
-   Angiv **valutakurstypen**. Hvis valutakurstypen ikke er defineret på hovedkontoen, bruges denne valutakurstype under værdiregulering af udenlandsk valuta.
-   Angiv den realiserede gevinst, det realiserede tab og kontiene for ikke-realiseret tab for værdiregulering af valuta. Konti for realiseret gevinst og realiseret tab bruges til udligning af debitor- og kreditortransaktioner, og konti for ikke-realiseret gevinst og ikke-realiseret tab bruges til åbne transaktioner og finanshovedkonti.

-   På siden **Værdireguleringskonti for valuta**:
-   Vælg forskellige konti til valutaværdiregulering for hver valuta og virksomhed. Hvis der ikke er defineret nogen konti, bruges kontiene på siden **Finans**.

## <a name="process-foreign-currency-revaluation"></a>Behandle værdiregulering af udenlandsk valuta
Når konfigurationen er fuldført, kan du bruge siden **Værdiregulering af udenlandsk valuta** til at værdiregulere saldi for hovedkontiene. Du kan køre processen i realtid eller planlægge, at den skal køre ved hjælp af en batch. 

Siden **Værdiregulering af udenlandsk valuta** viser en oversigt over hver værdireguleringsproces, herunder hvornår processen blev kørt, hvilke kriterier der blev defineret, et link til det oprettede bilag for reguleringen og en post, hvis en tidligere værdiregulering er tilbageført. Hvis du vil køre processen til værdiregulering, skal du vælge knappen **Værdiregulering af udenlandsk valuta**. 

Værdierne af **Fra dato** og **Til dato** definerer datointervallet for beregningen af saldoen for udenlandsk valuta, der reguleres. Når du værdiregulerer driftskonti, værdireguleres summen af alle de transaktioner, der forekommer i datointervallet. Når du værdiregulerer statuskonti, ignoreres Fra dato. I stedet bestemmes den saldo, der skal reguleres, ved at gå fra begyndelsen af regnskabsåret til Til dato. 

Den **dato rate** kan bruges til at angive den dato, som valutakursen som standard skal angives. For eksempel kan du regulere saldi mellem dato interval i januar 1 til 31, men du kan bruge den valutakurs, der er defineret for den 1. 

Vælg, hvilke hovedkonti der skal reguleres: Alle, Balance eller Drift. Kun hovedkonti markeret til værdiregulering (på konto-hovedside) reguleres. Hvis du yderligere vil begrænse de hovedkonti, bruge posterne **med** at definere en række hovedkonti eller enkelte hovedkonti. 

Af værdireguleringsprocessen kan køres for en eller flere juridiske enheder. Opslaget viser kun de juridiske enheder, som du har adgang til. Vælg de juridiske enheder, som du vil køre processen til værdiregulering. 

Reguleringen kan køres i en eller flere udenlandske valutaer. Opslaget omfatter alle de valutaer, der er bogført inden for datointervallet relevante for typen hovedkonto (balancen eller resultatopgørelsen) for de juridiske enheder, der er valgt til at regulere. Regnskabsvalutaen medtages på listen, men reguleres intet, hvis der vælges regnskabsvalutaen. 

Angiv **eksempel før bogføring** til **Ja** Hvis du vil have vist resultatet af værdireguleringen af Finans. Eksemplet i almindelighed Finans er forskellig fra simuleringen i P.A. og AP værdireguleringen af udenlandsk valuta. Simuleringen i AR og AP er en rapport, men Finans er et eksempel, der kan bogføres, uden at skulle køre værdireguleringsprocessen igen. Resultaterne af forhåndsvisningen kan eksporteres til Microsoft Excel for at bevare en oversigt over, hvordan beløbene er beregnet. Du kan ikke bruge batchbehandling, hvis du vil have en forhåndsvisning af resultaterne af reguleringen. I forhåndsvisningen har brugeren mulighed for at bogføre resultaterne af alle de juridiske enheder med knappen **Bogfør**. Hvis der er et problem med resultaterne for en juridisk enhed, har brugeren også mulighed for at bogføre et undersæt af de juridiske enheder ved hjælp af knappen **Vælg juridiske enheder, som skal bogføres**. 

Når processen til værdiregulering af udenlandsk valuta er fuldført, oprettes der en post for at registrere historikken for hver kørsel.  Der oprettes en separat post for hver juridisk enhed og posteringslag.

## <a name="calculate-unrealized-gainloss"></a>Beregne ikke-realiseret gevinst/tab
Ikke-realiseret gevinst/tab-posteringer oprettes forskelligt mellem Finans-værdiregulering og værdireguleringsprocessen for Debitor og Kreditor. I Debitor og Kreditor er den tidligere regulering tilbageført helt (forudsat, at transaktionen ikke er udlignet endnu), og der oprettes en ny postering af værdiregulering for ikke-realiseret gevinst eller tab baseret på den nye valutakurs. Dette skyldes, at vi regulerer hver enkelt transaktion i Debitor og Kreditor. I Finans tilbageføres tidligere værdireguleringen ikke. I stedet oprettes en postering for deltaet mellem saldoen på hovedkontoen, herunder eventuelle tidligere værdiregulering af beløb og den nye værdi, der er baseret på valutakursen for den dato sats. 

**Eksempel** findes følgende saldi for hovedkonto 110110.

|            |                    |                        |                       |
|------------|--------------------|------------------------|-----------------------|
| **Dato**   | **Finanskonto** | **Transaktionsbeløb** | **Regnskabsbeløb** |
| 20. januar | 110110 (Kontant)      | 500 EUR (Debet)        | 1000 USD (Debet)      |

Hovedkontoen værdireguleres på den 31.  Urealiseret gevinst eller tab beregnes på følgende måde.

|                                             |                                            |                                  |                                    |                             |
|---------------------------------------------|--------------------------------------------|----------------------------------|------------------------------------|-----------------------------|
| **Aktuel saldo i transaktionsvaluta** | **Aktuel saldo i regnskabsvaluta** | **Valutakurs på værdiregulering** | **Nyt beløb i regnskabsvaluta** | **Ikke-realiseret gevinst/tab**    |
| 500 EUR                                     | 1000 USD                                   | 166.6667                         | 833,33 EUR (500 x 1,666667)        | 166,67 tab (833,33 – 1000) |

Der oprettes følgende regnskabspost.

|            |                          |           |            |
|------------|--------------------------|-----------|------------|
| **Dato**   | **Finanskonto**       | **Debet** | **Kredit** |
| 31. januar | 110110 (Kontant)            |           | 166.67     |
| 31. januar | 801400 (Ikke-realiseret tab) | 166.67    |            |

Ingen nye posteringer, der bogføres for februar måned.  Hovedkontoen værdireguleres på den 28.

|                                             |                                            |                                  |                                    |                             |
|---------------------------------------------|--------------------------------------------|----------------------------------|------------------------------------|-----------------------------|
| **Aktuel saldo i transaktionsvaluta** | **Aktuel saldo i regnskabsvaluta** | **Valutakurs på værdiregulering** | **Nyt beløb i regnskabsvaluta** | **Ikke-realiseret gevinst/tab**    |
| 500 EUR                                     | 833,33 USD (1000 - 166,67)                 | 250.0000                         | 1250 USD (500 x 2,5)               | 416,67 gevinst (1250 – 833,33) |

Der oprettes følgende regnskabspost.

|             |                          |           |            |
|-------------|--------------------------|-----------|------------|
| **Dato**    | **Finanskonto**       | **Debet** | **Kredit** |
| 28. februar | 110110 (Kontant)            | 416.67    |            |
| 28. februar | 801600 (Ikke-realiseret gevinst) |           | 416.67     |

## <a name="reverse-foreign-currency-revaluation"></a>Tilbageføre værdiregulering af udenlandsk valuta
Hvis du vil tilbageføre værdireguleringstransaktionen, skal du vælge knappen **Tilbagefør postering** på siden **Værdiregulering af udenlandsk valuta**. Der oprettes en ny historisk post for værdiregulering af udenlandsk valuta for at bevare det historiske revisionsspor for, hvornår reguleringen opstod eller blev tilbageført. 

Du kan fortryde resultaterne af værdiregulering af datorækkefølgen, men du skal muligvis også tilbageføre en mere aktuel værdiregulering for at sikre, at de korrekte saldi for hver hovedkonto, der er regulerede. Tilbageførsler kan opstå forældet rækkefølge, fordi der er ingen måde at styre, hvilke hovedkonti revalueres og hyppigheden af hvor de er reguleret. For eksempel kan en organisation vælge at regulere deres kontanter hovedkonti på kvartalsvist grundlag, men alle andre hovedkonti hver måned.


