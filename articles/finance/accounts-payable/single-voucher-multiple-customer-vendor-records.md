---
title: Enkelt bilag med flere debitor- eller kreditorposter
description: Dette emne indeholder en oversigt over, hvad der sker, når du bogfører et enkelt bilag med flere debitor- eller kreditorposter. Denne funktion understøttes ikke i fremtidige versioner af Microsoft Dynamics 365 Finance, så derfor fraråder vi denne metode til bogføring grundet den regnskabsmæssige virkning af udligningsbehandling.
author: abruer
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 222534
ms.assetid: d4df11ce-4d36-4c66-8230-f5fc58e021bc
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8677eba2c38c6273555e1189c0153272a8ff9e005655f3846c0d7605b872ff94
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6737035"
---
# <a name="single-voucher-with-multiple-customer-or-vendor-records"></a>Enkelt bilag med flere debitor- eller kreditorposter

[!include [banner](../includes/banner.md)]

Dette emne indeholder en oversigt over, hvad der sker, når du bogfører et enkelt bilag med flere debitor- eller kreditorposter. Denne funktion understøttes ikke i fremtidige versioner, så derfor fraråder vi denne metode til bogføring grundet den regnskabsmæssige virkning af udligningsbehandling. 

Nogle almindelige eksempler på, hvor ét bilag bruges til flere debitorer eller kreditorer, omfatter saldooverførsler mellem debitorer og modregning mellem debitorer og kreditorer i samme organisation. 

Et bilag, der indeholder mere end én debitor eller kreditor, kan indtastes ved at benytte en af følgende fremgangsmåder:

-   Med en kladde, hvor indstillingen **Kun ét bilagsnummer** er valgt, så hver linje, der føjes til kladden, medtages på samme bilag.
-   Med et bilag, der indeholder flere linjer, hvor der ikke er nogen finansmodkonto, med mere end én debitor eller kreditor.
-   Angivelse af et bilag med kontoen og modkontoen værende kreditor/kreditor, debitor/debitor, kreditor/debitor eller debitor/kreditor.

Dette emne viser, hvordan udligning skal behandles, når der bogføres et bilag med flere poster for debitoren eller kreditoren. Dette emne indeholder desuden løsninger for at hjælpe dig med at forstå, hvordan du undgår at bruge ét bilag med flere debitorer eller kreditorer. Der findes eksempler, der illustrerer to almindelige scenarier med udligning, der er berørt af anvendelsen af et bilag med flere debitorer eller kreditorer:

-   Kasserabatregnskab
-   Værdireguleringsregnskab

## <a name="how-does-settlement-impact-single-voucher-usage"></a>Hvordan påvirker udligning forbrug af enkelt bilag
Ved bogføring af et bilag, der indeholder flere poster for debitor eller kreditor, oprettes der et enkelt regnskabsbilag, der indeholder flere debitor- eller kreditorsaldi. Under udligningsprocessen bruges de oprindelige regnskabsposter til at oprette regnskabsposter for kasserabatten, ikke-realiserede gevinster og tab, realiseret gevinst og tab og eftergivelse af samlekonto for det oprindelige dokument. For eksempel hvis en kasserabat tages, når du udligner en kreditorbetaling til en faktura, skal kasserabatregnskabet bogføre til kreditorfinanskontoen fra den oprindelige faktura. Hvis den oprindelige faktura er bogført i et bilag, der indeholder flere kreditorposter, opsummeres det oprindelige regnskab. I dette tilfælde, fordi det ikke er muligt at få adgang til den detaljerede regnskabspost for hver kreditorpostering i det enkelte bilag, er det umuligt at finde ud af, hvordan brugeren ville redegøre for kasserabatten.

### <a name="one-voucher-with-multiple-vendors-and-the-impact-on-cash-discount-accounting"></a>Et bilag med flere kreditorer og indvirkningen på kasserabatregnskabet

I følgende eksempel bliver flere kreditorfakturaer registreret i Finans i et enkelt bilag på siden **Finanskladde**. Disse fakturaer er fordelt på tværs af flere kontodimensioner.

| Bilag | Kontotype | Konto  | Betegnelse | Debet | Kredit |
|-------------|------------------|--------------|-----------------|-----------|------------|
| GNJL001     | Leverandør           | 1001         | INV1            |           | 100,00     |
| GNJL001     | Leverandør           | 1001         | INV2            |           | 200,00     |
| GNJL001     | Leverandør           | 1001         | INV3            |           | 300,00     |
| GNJL001     | Finans           | 606300-001-- | INV1            |   50,00   |            |
| GNJL001     | Finans           | 606300-002-- | INV1            |   50,00   |            |
| GNJL001     | Finans           | 606300-003-- | INV2            | 200,00    |            |
| GNJL001     | Finans           | 606300-004-- | INV3            | 300,00    |            |

Efter bogføring oprettes ét bilag.

| Bilag | Konto  | Bogføringstype | Beløb i transaktionsvaluta |
|-------------|--------------|------------------|------------------------------------|
| GNJL001     | 606300-001-- | Finanskladde   | 50,00                              |
| GNJL001     | 606300-002-- | Finanskladde   | 50,00                              |
| GNJL001     | 606300-003-- | Finanskladde   | 200,00                             |
| GNJL001     | 606300-004-- | Finanskladde   | 300,00                             |
| GNJL001     | 200110-001-  | Kreditorsaldo   | -100,00                            |
| GNJL001     | 200110-001-  | Kreditorsaldo   | -200,00                            |
| GNJL001     | 200110-001-  | Kreditorsaldo   | -300,00                            |

Bemærk, at bilaget indeholder tre poster for bogføringstypen for kreditorsaldoen i enkelt bilag. Det er ikke muligt at angive, at 50,00 debet til 606300-001 og 50,00 debet til 606300-002 skal modregnes i saldoen for kreditorposten 200110-001. Dette skyldes, at brugeren har angivet flere kreditorposter i et enkelt bilag.

I dette eksempel analyseres virkningen ved brug af ét bilag på efterfølgende udligning af regnskab. Antag, at du betaler 197,00 af 200,00 fakturaen med en kasserabat på 3,00. Bemærk, at kasserabattens kontoværdi fordeles på tværs af alle dimensioner fra fakturabilagets udgiftskonti. Dette skyldes, at ét bilag blev brugt til at bogføre ovenstående faktura med ingen angivelse af, hvordan brugeren ville have udgiftsfordelingerne korreleret til kreditorsaldoen i enkelt bilag.

| Bilag | Konto  | Bogføringstype     | Debet | Kredit |
|-------------|--------------|----------------------|-----------|------------|
| APPAYM001   | 200110-001-  | Kreditorsaldo       | 197.00    |            |
| APPAYM001   | 110110-001-  | Pengeinstitut                 |           | 197.00     |
| 14000056    | 520200-001-- | Kreditor kasserabat |           | 0.25       |
| 14000056    | 520200-002-- | Kreditor kasserabat |           | 0.25       |
| 14000056    | 520200-003-- | Kreditor kasserabat |           | 1,00       |
| 14000056    | 520200-004-- | Kreditor kasserabat |           | 1.50       |
| 14000056    | 200110-001-  | Kreditorsaldo       | 3,00      |            |

Hvis brugeren er utilfreds med den kasserabat, der fordeles på tværs af alle udgiftsfordelingerne fra den oprindelige faktura, bør flere bilag bruges i stedet for ét bilag til at bogføre fakturaerne. Her er et eksempel på, hvordan flere bilag angives i Finans, i stedet for ved hjælp af ét bilag, som vist i begyndelsen af dette eksempel.

| Bilag | Kontotype | Konto  | Betegnelse | Debet | Kredit | Modtype | Modkonto |
|-------------|------------------|--------------|-----------------|-----------|------------|-----------------|--------------------|
| GNJL001     | Leverandør           | 1001         | INV1            |           | 100,00     | Finans          | &lt;tom&gt;      |
| GNJL001     | Finans           | 606300-001-- | INV1            |   50,00   |            | Finans          | &lt;tom&gt;      |
| GNJL001     | Finans           | 606300-002-- | INV1            |   50,00   |            | Finans          | &lt;tom&gt;      |
| GNJL002     | Leverandør           | 1001         | INV2            |           | 200,00     | Finans          | 606300-003--       |
| GNJL003     | Leverandør           | 1001         | INV3            |           | 300,00     | Finans          | 606300-004--       |

Nu, når INV2 er betalt, bliver følgende post oprettet. Bemærk, at kasserabattens økonomiske dimensioner følger de tilknyttede udgifters økonomiske dimensioner.

| Bilag | Konto  | Bogføringstype     | Debet | Kredit |
|-------------|--------------|----------------------|-----------|------------|
| APPAYM001   | 200110-001-  | Kreditorsaldo       | 197.00    |            |
| APPAYM001   | 110110-001-  | Pengeinstitut                 |           | 197.00     |
| 14000056    | 520200-003-- | Kreditor kasserabat |           | 3,00       |
| 14000056    | 200110-001-  | Kreditorsaldo       | 3,00      |            |

### <a name="one-voucher-with-multiple-vendors-and-the-impact-on-realized-gainloss-accounting"></a>Et bilag med flere kreditorer og indvirkningen på regnskabet for realiseret gevinst/tab

| Bilag | Kontotype | Konto | Betegnelse | Debet | Kredit | Kontotype | Konto  |
|-------------|------------------|-------------|-----------------|-----------|------------|------------------|--------------|
| GNJL001     | Leverandør           | 1001        | INV1            |           | 100,00     | Finans           | 606300-001-- |
| GNJL001     | Leverandør           | 1001        | INV2            |           | 200,00     | Finans           | 606300-002-- |

I følgende eksempel bliver flere kreditorfakturaer registreret i Finans i et enkelt bilag på siden **Finanskladde**. Disse fakturaer er fordelt på tværs af flere kontodimensioner. Efter bogføring oprettes ét bilag.

| Bilag | Konto  | Bogføringstype | Beløb i transaktionsvaluta (EUR) | Beløb i regnskabsvaluta (USD) |
|-------------|--------------|------------------|------------------------------------------|-----------------------------------------|
| GNJL001     | 606300-001-- | Finanskladde   | 100,00                                   | 114.00                                  |
| GNJL001     | 606300-002-- | Finanskladde   | 200,00                                   | 228.00                                  |
| GNJL001     | 200110-001-  | Kreditorsaldo   | -100,00                                  | -114,00                                 |
| GNJL001     | 200110-001-  | Kreditorsaldo   | -200,00                                  | -228,00                                 |

Bemærk, at bilaget indeholder to poster for bogføringstypen for kreditorsaldoen i enkelt bilag. Det er ikke muligt at angive, at debet til 606300-001 skal modregne kreditorsaldoposten på 100,00 til 200110-001. Dette skyldes, at brugeren har angivet flere kreditorposter i et enkelt bilag. 

I dette eksempel analyseres virkningen ved brug af ét bilag på efterfølgende udligning af regnskab. Antag, at din regnskabsvaluta er USD, og de ovennævnte transaktioner blev bogført i transaktionsvalutaen EUR. Antag, at du betaler den fulde 200,00 EUR-faktura, men du støder på et realiseret tab på grund af en forskel i valutakursen mellem den tid, du har bogført fakturaen, og betalingen. Bemærk, at kontoværdien af realiseret tab fordeles på tværs af alle dimensioner fra fakturabilagets udgiftskonti. I dette tilfælde er både dimension 001 og 002 blevet tildelt, selvom brugerens opfattelse kan være, at kun 002 hører til udgiftskontoen fra den faktura, der udlignes. Dette skyldes, at ét bilag blev brugt til at bogføre ovenstående faktura uden mulighed for angivelse af, hvordan brugeren ville have udgiftsfordelingerne korreleret til kreditorsaldoen i enkelt bilag.

| Bilag | Konto | Bogføringstype   | Beløb i transaktionsvaluta (EUR) | Beløb i regnskabsvaluta (USD) |
|-------------|-------------|--------------------|------------------------------------------|-----------------------------------------|
| APPAYM001   | 200110-001- | Kreditorsaldo     | 200,00                                   | 230.00                                  |
| APPAYM001   | 110110-001- | Pengeinstitut               | -200,00                                  | -230,00                                 |
| 14000056    | 801300-001- | Valutakurstab | 0,00                                     | 0.67                                    |
| 14000056    | 801300-002- | Valutakurstab | 0,00                                     | 1.33                                    |
| 14000056    | 200110-001- | Kreditorsaldo     |                                          | -2,00                                   |

Hvis brugeren er utilfreds med det valutakurstab, der fordeles på tværs af alle udgiftsfordelingerne fra den oprindelige faktura, bør flere bilag bruges i stedet for ét bilag til at bogføre fakturaerne. Her er et eksempel på, hvordan flere bilag angives i Finans, i stedet for ved hjælp af ét bilag, som vist i begyndelsen af dette eksempel.

| Bilag | Kontotype | Konto | Betegnelse | Debet | Kredit | Modtype | Modkonto |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| GNJL002     | Leverandør           | 1001        | INV1            |           | 100,00     | Finans          | 606300-001--       |
| GNJL003     | Leverandør           | 1001        | INV2            |           | 200,00     | Finans          | 606300-002--       |

Nu, når INV2 er betalt, bliver følgende post oprettet. Bemærk, at valutakurstabets økonomiske dimensioner følger de tilknyttede udgifters økonomiske dimensioner.

| Bilag | Konto | Bogføringstype   | Beløb i transaktionsvaluta (EUR) | Beløb i regnskabsvaluta (USD) |
|-------------|-------------|--------------------|------------------------------------------|-----------------------------------------|
| APPAYM001   | 200110-001- | Kreditorsaldo     | 200,00                                   | 230.00                                  |
| APPAYM001   | 110110-001- | Pengeinstitut               | -200,00                                  | -230,00                                 |
| 14000056    | 801300-002- | Valutakurstab | 0,00                                     | 2.00                                    |
| 14000056    | 200110-001- | Kreditorsaldo     |                                          | -2,00                                   |

## <a name="one-voucher-for-balance-transfers-and-netting-scenarios"></a>Ét bilag for saldooverførsler og modregningsscenarier
To almindelige scenarier, der anvender et bilag, der indeholder flere debitorer eller kreditorer, omfatter saldooverførsler fra en debitor/kreditor til en anden debitor/kreditor og modregnings af en debitor og kreditor, der er den samme organisation. Følgende to eksempler illustrerer den foretrukne metode til at angive disse scenarier som et alternativ til at angive dem i ét bilag. 

A *saldooverførsel* er et bilag med flere debitorer, der er angivet med henblik på overførsel af saldoen fra en debitor til en anden debitor (samme for kreditorer). Denne situation kan opstå, når ansvaret for betaling af fakturaen skifter til en anden part, f.eks. et underordnet firma, der flytter ansvaret for et moderselskab. 

I dette eksempel antages et salg, hvor kunden er berettiget til en kasserabat, hvis betalingen finder sted inden for 10 dage. I dette eksempel anvender kunden et forsikringsselskab, der skal være ansvarlig for at betale regningen. Forsikringsselskabet er angivet som en anden debitor i systemet. Den oprindelige debitors saldo overføres til forsikringsselskabet, der betaler regningen med en kasserabat på 2 % for betaling inden for rabatperioden. 

For at illustrere dette forudsættes følgende salg til kunden ACME. Følgende regnskabsposter repræsenterer salg.

| Finanskonto | Bogføringstype | Debet | Kredit |
|--------------------|------------------|-----------|------------|
| 401100-002-023-    | Indtægter          |           | 100        |
| 130100-002-        | Debitorsaldo | 100       |            |

Derefter skal brugeren overføre den forfaldne saldo fra ACME til forsikringsselskabet i ét bilag i debitorbetalingskladden. Forsikringsselskabet oprettes som kundeforsikring.

| Bilag | Kontotype | Konto | Betegnelse | Debet | Kredit | Modtype | Modkonto |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| ARPAYM001   | Debitor          | ACME        | Ompostering        |           | 100,00     | Debitor         | Forsikring          |

Bemærk, at ovenstående post er indeholdt i ét bilag. Dette bilag indeholder to debitorposter. Følgende bilag oprettes, når ovenstående finanspost bogføres.

| Bilag | Konto | Bogføringstype | Beløb i transaktionsvaluta |
|-------------|-------------|------------------|------------------------------------|
| ARPAYM001   | 130100-002- | Debitorsaldo | 100,00                             |
| ARPAYM001   | 130100-002- | Debitorsaldo | -100,00                            |

Dernæst skal du antage, at du modtager en betaling fra forsikringskunden på 98,00, og du vil udligne betalingen med fakturaen, der er oprettet af saldooverførsel. Dette vil resultere i, at følgende bilag bogføres. Der kan være en forventning om, at udligningen bruger de økonomiske dimensioner fra den oprindelige faktura, men det er ikke muligt, fordi der ikke er et fakturadokument for forsikringskunden. Bemærk, at fordelingsdimensionerne på kasserabatten som standard kommer fra debitorpostering, der oprettes fra overførsel, ikke fra den oprindelige fakturas omsætningskonto. Standardværdien er et resultat af at bruge ét bilag til at overføre saldi.

| Bilag | Konto | Bogføringstype | Debet | Kredit |
|-------------|-------------|------------------|-----------|------------|
| ARPAYM002   | 110110-002- | Pengeinstitut             | 98.00     |            |
| ARPAYM002   | 130100-002- | Debitorsaldo |           | 98.00      |

På det relaterede bilag for kasserabatten kommer standarden for den økonomiske dimension fra debitorpostering, der oprettes ud fra overførslen, fordi overførslen har mere end én debitor.

| Bilag | Konto | Bogføringstype       | Debet | Kredit |
|-------------|-------------|------------------------|-----------|------------|
| ARP-00001   | 403300-002- | Debitor, kasserabat | 2.00      |            |
| ARP-00001   | 130100-002- | Debitorsaldo       |           | 2.00       |

Hvis brugeren er utilfreds med standarden for de økonomiske dimensioner for kasserabatten, bør flere bilag bruges i stedet for ét bilag til at registrere saldooverførsel. Denne situation kan ordnes ved at oprette en kreditnota for den debitor, som saldoen er flyttet FRA, og debetnota eller faktura, der er oprettet for den debitor, som saldoen er flyttet TIL. Følgende eksempel viser, hvordan flere bilag angives i debitorbetalingskladden til at overføre saldoen i stedet for ved hjælp af ét bilag, som vist tidligere i dette eksempel.

| Bilag | Kontotype | Konto | Betegnelse | Debet | Kredit | Modtype | Modkonto |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| ARPAYM001   | Debitor          | ACME        |                 |           | 100,00     | Finans          | 401100-002-023-    |
| ARPAYM002   | Debitor          | Forsikring   |                 | 100,00    |            | Finans          | 401100-002-023-    |

Det betyder, at når forsikringskunden betaler 98,00 med bilag ARPAYM02, bruges de rigtige økonomiske dimensioner fra bilag ARPAYM002's finanskontopost.

| Bilag | Konto | Bogføringstype | Debet | Kredit |
|-------------|-------------|------------------|-----------|------------|
| ARPAYM003   | 110110-002- | Pengeinstitut             | 98.00     |            |
| ARPAYM003   | 130100-002  | Debitorsaldo |           | 98.00      |

På det relaterede bilag for kasserabat bruges økonomiske dimensioner fra den modsvarende omsætningskonto, der vises på ARPAYM002's bilag.

| Bilag | Konto     | Bogføringstype       | Debet | Kredit |
|-------------|-----------------|------------------------|-----------|------------|
| ARP-00001   | 403300-002-023- | Debitor, kasserabat | 2.00      |            |
| ARP-00001   | 130100-002-     | Debitorsaldo       |           | 2.00       |

## <a name="one-voucher-with-a-netting-for-multiple-customers-and-vendors"></a>Et bilag med en modregning for flere debitorer og kreditorer
Modregning kan være nyttigt, når en organisation køber og sælger til samme virksomhed. I stedet for betaling af kreditorfakturaer og venten på at modtage betaling for debitorfakturaerne, modregnes kreditor- og debitorfakturaerne. Modregningsposteringen udlignes mod de udestående saldi. 

For at illustrere dette, forudsættes, at kreditor 1001 og debitor US-008 er den samme enhed, så din organisation vil modregne kreditor- og debitorsaldi før betaling/modtagelse af den resterende saldo. Antag, at debitorposten skylder 75,00 EUR, og kreditorposten skylder 100,00 EUR, hvilket betyder, at du foretrækker at modregne saldi og kun betale kreditor 25,00 EUR. Yderligere forudsætter er, at regnskabsvalutaen er USD. I så fald angives en modregningstransaktion i ét bilag i kreditorbetalingskladden.

| Bilag | Kontotype | Konto | Betegnelse | Debet | Kredit | Modtype | Modkonto |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| APPAYM001   | Leverandør           | 1001        | Modregning         |  75,00    |            | Debitor         | US-008             |

For at undgå uønskede problemer med fremtidige udligninger for denne transaktion, skal ét bilag erstattes af flere bilag i kladden til bogføring af modregningstransaktionen. Bemærk, at debitor- og kreditorsaldi modposteres med en enkelt clearingkonto for at undgå brugen af ét bilag, der indeholder flere debitor- og kreditorsaldi.

| Bilag | Kontotype | Konto | Betegnelse | Debet | Kredit | Modtype | Modkonto |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| 001         | Debitor          | US-008      |                 |           |  75,00     | Finans          | 999999---          |
| 002         | Leverandør           | 1001        |                 |  75,00    |            | Finans          | 999999---          |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]