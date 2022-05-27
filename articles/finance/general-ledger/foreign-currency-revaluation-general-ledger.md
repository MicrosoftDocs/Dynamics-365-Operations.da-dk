---
title: Værdiregulering af udenlandsk valuta for Finans
description: 'Dette emne indeholder en oversigt over følgende proces til værdiregulering af udenlandsk valuta i finans: konfiguration, kørsel af processen beregning for processen, og hvordan du kan tilbageføre posteringerne, hvis det er nødvendigt.'
author: kweekley
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CurrencyLedgerGainLossAccount
audience: Application User
ms.reviewer: kfend
ms.custom: 62153
ms.assetid: 842e8561-560f-4cc6-8668-70cca60b1ba3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e4a138a26a23c804f5fd358d335b04aee3897dce
ms.sourcegitcommit: e09f5c6d78d7942af950ae3f6407df2fedceeba4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/06/2022
ms.locfileid: "8720332"
---
# <a name="foreign-currency-revaluation-for-general-ledger"></a>Værdiregulering af udenlandsk valuta for Finans

[!include [banner](../includes/banner.md)]

Dette emne indeholder en oversigt over følgende proces til værdiregulering af udenlandsk valuta i finans: konfiguration, kørsel af processen beregning for processen, og hvordan du kan tilbageføre posteringerne, hvis det er nødvendigt. 

I en periodeafslutning kræver regnskabsmæssige konventioner finanskontosaldi i fremmedvalutaer, der reguleres ved hjælp af forskellige valutakurstyper (aktuelle, historiske, gennemsnit, osv.). For eksempel kræver en regnskabskonvention, at aktiver og passiver værdiansættes på ny ved den aktuelle valutakurs, anlægsaktiver ved den historiske valutakurs og driftskonti på det månedlige gennemsnit. Værdiregulering af udenlandsk valuta i Finans kan bruges til at regulere balancen og resultatopgørelseskonti. 

> [!NOTE]
> Værdiregulering af udenlandsk valuta er også tilgængelig i Debitor- og Kreditor-modulerne. Hvis du bruger disse moduler, bør de udestående transaktioner reguleres ved hjælp af værdireguleringen af udenlandsk valuta i disse moduler. Værdiregulering af udenlandsk valuta i Debitor og Kreditor opretter en regnskabspost i Finans for at afspejle urealiseret gevinst eller tab og sikre, at reskontroer og Finans kan afstemmes. Da værdireguleringen af udenlandsk valuta i Debitor og Kreditor opretter regnskabsposter i Finans, skal debitor- og kreditorhovedkonti udelukkes fra finansmodulets værdiregulering af udenlandsk valuta. 

Når du kører processen til værdiregulering, reguleres saldoen i hver hovedkonto, der er bogført i udenlandsk valuta. De transaktioner for ikke-realiseret gevinst eller tab, der oprettes under værdireguleringsprocessen, er genereret af systemet. To posteringer kan oprettes, én for regnskabsvalutaen og en anden for rapporteringsvalutaen, hvis det er relevant. Hver regnskabspost bogføres i ikke-realiseret gevinst eller tab og den hovedkonto, der værdireguleres.

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

**Kursdato** kan bruges til at angive den dato, som valutakursen som standard skal angives for. For eksempel kan du regulere saldi mellem datointervallet 1. til 31. januar, men bruge den valutakurs, der er defineret for den 1. februar. 

Vælg, hvilke hovedkonti der skal reguleres: Alle, Balance eller Drift. Kun hovedkonti markeret til værdiregulering (på siden Hovedkonto) reguleres. Hvis du yderligere vil begrænse hovedkonti, skal du bruge fanen **Poster, der skal indgå** til at definere en række hovedkonti eller enkelte hovedkonti. 

Værdireguleringsprocessen kan køres for en eller flere juridiske enheder. Opslaget viser kun de juridiske enheder, som du har adgang til. Vælg de juridiske enheder, hvor du vil køre processen til værdiregulering. 

Reguleringen kan køres i en eller flere udenlandske valutaer. Opslaget omfatter alle de valutaer, der er bogført inden for datointervallet, der er relevant for typen af hovedkonto (Balancen eller Drift), for de juridiske enheder, der er valgt til værdiregulering. Regnskabsvalutaen medtages på listen, men intet reguleres, hvis regnskabsvalutaen er valgt. 

Indstil **Forhåndsvisning før bogføring** til **Ja**, hvis du vil have vist resultatet af værdireguleringen af Finans. Forhåndsvisningen i Finans er forskellig fra simuleringen i værdireguleringen af udenlandsk valuta i Debitor og Kreditor, hvor simuleringen er en rapport, men Finans har en forhåndsvisning, der kan bogføres uden at køre værdireguleringsprocessen igen.. Resultaterne af forhåndsvisningen kan eksporteres til Microsoft Excel for at bevare en oversigt over, hvordan beløbene er beregnet. Du kan ikke bruge batchbehandling, hvis du vil have en forhåndsvisning af resultaterne af reguleringen. I forhåndsvisningen har brugeren mulighed for at bogføre resultaterne af alle de juridiske enheder med knappen **Bogfør**. Hvis der er et problem med resultaterne for en juridisk enhed, har brugeren også mulighed for at bogføre et undersæt af de juridiske enheder ved hjælp af knappen **Vælg juridiske enheder, som skal bogføres**. 

Når processen til værdiregulering af udenlandsk valuta er fuldført, oprettes der en post for at registrere historikken for hver kørsel.  Der oprettes en separat post for hver juridiske enhed og posteringslag.

## <a name="calculate-unrealized-gainloss"></a>Beregne ikke-realiseret gevinst/tab
Ikke-realiseret gevinst/tab-posteringer oprettes forskelligt mellem Finans-værdiregulering og værdireguleringsprocessen for Debitor og Kreditor. I Debitor og Kreditor er den tidligere regulering tilbageført helt (forudsat, at transaktionen ikke er udlignet endnu), og der oprettes en ny postering af værdiregulering for ikke-realiseret gevinst eller tab baseret på den nye valutakurs. Dette skyldes, at vi regulerer hver enkelt transaktion i Debitor og Kreditor. I Finans tilbageføres den tidligere værdiregulering ikke. I stedet oprettes en postering for deltaet mellem saldoen på hovedkontoen, herunder eventuelle tidligere værdireguleringsbeløb, og den nye værdi, der er baseret på valutakursen for Kursdato. 

**Eksempel** Der findes følgende saldi for hovedkontoen 110110.

| Dato   | Finanskonto| Transaktionsbeløb | Regnskabsbeløb |
|------------|--------------------|------------------------|-----------------------|
| 20. januar | 110110 (Kontant)      | 500 EUR (Debet)        | 1000 USD (Debet)      |

Hovedkontoen værdireguleres den 31 januar.  Ikke-realiseret gevinst eller tab beregnes på følgende måde.

| Aktuel saldo i transaktionsvaluta | Aktuel saldo i regnskabsvaluta | Valutakurs på værdiregulering | Nyt beløb i regnskabsvaluta | Ikke-realiseret gevinst/tab    |
|---------------------------------------------|--------------------------------------------|----------------------------------|------------------------------------|-----------------------------|
| 500 EUR                                     | 1000 USD                                   | 166.6667                         | 833,33 USD (500 x 1,666667)        | 166,67 tab (833,33 – 1000) |

Der oprettes følgende regnskabspost.

| Dato   | Finanskonto       | Debet | Kredit |
|------------|--------------------------|-----------|------------|
| 31. januar | 110110 (Kontant)            |           | 166.67     |
| 31. januar | 801400 (Ikke-realiseret tab) | 166.67    |            |

Ingen nye posteringer, der bogføres for februar måned.  Hovedkontoen værdireguleres den 28. februar.

| Aktuel saldo i transaktionsvaluta | Aktuel saldo i regnskabsvaluta | Valutakurs på værdiregulering | Nyt beløb i regnskabsvaluta | Ikke-realiseret gevinst/tab    |
|---------------------------------------------|--------------------------------------------|----------------------------------|------------------------------------|-----------------------------|
| 500 EUR                                     | 833,33 USD (1000 - 166,67)                 | 250.0000                         | 1250 USD (500 x 2,5)               | 416,67 gevinst (1250 – 833,33) |

Der oprettes følgende regnskabspost.

| Dato    | Finanskonto       | Debet | Kredit |
|-------------|--------------------------|-----------|------------|
| 28. februar | 110110 (Kontant)            | 416.67    |            |
| 28. februar | 801600 (Ikke-realiseret gevinst) |           | 416.67     |

## <a name="reverse-foreign-currency-revaluation"></a>Tilbageføre værdiregulering af udenlandsk valuta
Hvis du vil tilbageføre værdireguleringstransaktionen, skal du vælge knappen **Tilbagefør postering** på siden **Værdiregulering af udenlandsk valuta**. Der oprettes en ny historisk post for værdiregulering af udenlandsk valuta for at bevare det historiske revisionsspor for, hvornår reguleringen opstod eller blev tilbageført. 

Du kan tilbageføre resultaterne af forældet værdiregulering, men du skal muligvis også tilbageføre en mere aktuel værdiregulering for at sikre korrekte saldi for hver hovedkonto, der er reguleret. Tilbageførsler kan opstå forældet, fordi der er ingen måde at styre, hvilke hovedkonti der revalueres og hvor ofte. For eksempel kan en organisation vælge at regulere deres kontanthovedkonti på kvartalsvist grundlag, men alle andre hovedkonti hver måned.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
