---
title: Regnskabsprincippet for bogføring på omkostningskonto
description: Dette emne indeholder en oversigt over regnskabsprincippet for bogføring til omkostningskonto.
author: rachel-profitt
ms.date: 05/02/2022
ms.topic: article
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2022-05-02
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 45dc1775c0db83faa89a7a1fa799bdd070d1b09a
ms.sourcegitcommit: 283e237d7bd2a76dd3a8ff64685b0a5f146edd25
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/06/2022
ms.locfileid: "8721392"
---
# <a name="post-to-charge-account-accounting-principle"></a>Regnskabsprincippet for bogføring på omkostningskonto

Regnskabsprincippet *bogføring på omkostningskontoen* giver dig mulighed for at tage højde for og nemmere afstemme eventuelle forskelle i enhedsprisen mellem fysisk bogføring og økonomisk bogføring, indirekte omkostninger på købte varer eller gebyrer på en indkøbsordre. 

To konfigurationer for kreditorgebyrkoder på siden **Gebyrkode** (**Kreditor \> Konfiguration af gebyrer \> Gebyrkode**) kan medføre, at en indkøbsordre påvirker værdiansættelsen af lageraktiver:

- For gebyrkoder, hvor feltet **Debettype** er angivet til *Vare*, og feltet **Kredittype** er angivet til *Finanskonto*, fungerer den finanskonto, der er valgt som overtagelseskonto, som en lagervariationskonto.
- For gebyrkoder , hvor feltet **Debettype** er angivet til *Vare*, og feltet **Kredittype** er angivet til *Debitor/Kreditor*, vil til gebyret blive taget i betragtning som materialeomkostninger, og lagervariationskontoen for varen anvendes.

## <a name="european-special-accounting-rule"></a>Særlig europæisk regnskabsregel

I Europa bruges bogføringsprincippet *bogfør på omkostningskonto* ofte til at medtage en særlig regnskabsregel. En af følgende metoder bruges f.eks. typisk til at tage højde for lagerændringer:

- **Salgsomkostningsmetode**– Standardkonfigurationen af lagerlagerposteringsprofilen understøtter denne metode. Regnskabsprincippet *bogføring på omkostningskontoen* er ikke obligatorisk.
- **Udgiftsmetodens art** – Mindre organisationer bruger ofte denne metode. Den omfatter typisk følgende trin:

    1. Varer eller tjenester udgiftsføres fuldt ud på tidspunktet for modtagelse.
    2. Ved periodens afslutning udføres en cyklusoptælling.
    3. En manuel regulering af antallet og værdien bogføres til lageret. (Modkontoen er en lagervariantkonto, der modregner den udgift, der blev bogført i trin 1. Du kan derfor kun se variationen i lagerværdien på denne konto).

Princippet *bogføring på omkostningskontoen* giver dig mulighed for at automatisere de to posteringer fuldstændigt. På den måde kan du eliminere en manuel bogføring af regulering ved afslutning af perioden.

## <a name="enable-the-post-to-charge-account-accounting-principle"></a>Aktivere regnskabsprincippet for bogføring på omkostningskonto

Benyt følgende fremgangsmåde for at aktivere bogføringsprincippet *bogføring på omkostningskonto*.

1. Gå til **Kreditor \> Opsætning \> Kreditorparametre**.
2. Under fanen **Faktura** skal du i oversigtspanelet **Faktura** angive **Vil du bogføre på omkostningskontoen i finans?** til *Ja*.
3. Luk siden.

## <a name="prerequisites-and-recommended-parameters-for-the-post-to-charge-account-accounting-principle"></a>Forudsætninger og anbefalede parametre for regnskabsprincippet for bogføring på omkostningskontoen

Hvis du planlægger at tage højde for indkøbsgebyrer og lagervariationer, skal følgende forudsætninger være tilstede:

- Under fanen **Faktura** på siden **Kreditorparametre** (**Kreditor \> Konfiguration \> Kreditorparametre**) skal indstillingen **Vil du bogføre på omkostningskontoen i finans?** være angivet til *Ja*.
- På siden **Varemodelgrupper** (**Omkostningsstyring \> Konfiguration af regnskabspolitik for lager \> Varemodelgrupper**) skal alle følgende indstillinger angives til *Ja* for hver relevant modelgruppe, der indeholder varer, der er inkluderet i en indkøbsordre:

    - Bogfør fysisk varelager
    - Bogfør økonomisk varelager
    - Periodiser passiver ved produktmodtagelse

- Under fanen **Levering** på siden **Indkøbs- og forsyningsparametre** (**Indkøb og forsyning \> Konfiguration \> Indkøbs- og forsyningsparametre**) skal indstillingen **Generér gebyrer på produktkvittering** angives til *Ja*.
- Under fanen **Lagerregnskab** på siden **Parametre til lager- og lokationsstyring** (**Lagerstyring \> Konfiguration \> Parametre til lager- og lokationsstyring**) skal indstillingen **Bogfør følgeseddel i finans** være angivet til *Ja*.
- Under fanen **Indkøbsordre** på siden **Bogføring** (**Lagerstyring \> Konfiguration \> Bogføring \> Bogføring**) skal der angives hovedkonti, der gælder for alle relevante varer, for hver af følgende bogføringstyper:

    - Udgifter til indkøb, ikke-faktureret
    - Udgifter til indkøb for produkt
    - Lagerafvigelse

## <a name="example-scenario-1-change-in-unit-cost-price"></a>Eksempel 1: Ændring i enhedskostpris

Dette eksempelscenarie har følgende forudsætninger:

- FIFO-efterkalkulationsmodel (First in, First out)

Følgende procedure viser et eksempel på, hvad der sker, når du ændrer enhedskostprisen på en indkøbsordre.

1. Opret en indkøbsordre for en mængde på 1 af en vare med en enhedspris på 100,00.
2. Bekræft indkøbsordren.
3. Bogfør produktkvitteringen for indkøbsordren.
4. Valider bilaget på produktkvitteringen. Følgende tabel viser et eksempelbilag.

    | Bogføringstype | Hovedkonto | Hovedkontonavn | Kontotype | Debet/Kredit? | Clearingkonto | Fysisk/Økonomisk? | Beløb |
    |---|---|---|---|---|---|---|---|
    | Køb, lagerafvigelse | 600170 | Lagerafvigelsesmaterialer | Udgift | Kredit | Nej | Fysisk | -100,00 |
    | Omkostning til købte materialer, der er modtaget | 140100 | Materialelager | Aktiv | Debet | Ja | Fysisk | 100.00 |
    | Udgifter til indkøb, ikke-faktureret | 600180 | Materialekvitteringer | Udgift | Debet | Ja | Fysisk | 100.00 |
    | Indkøb, periodisering | 200140 | Periodiserede køb | Passiv | Kredit | Ja | Fysisk | -100,00 |

5. Bogfør fakturaen for den indkøbsordre, der har en opdateret enhedspris på 110,00.
6. Valider bilaget på fakturaen. Følgende tabel viser et eksempelbilag.

    | Bogføringstype | Hovedkonto | Hovedkontonavn | Kontotype | Debet/Kredit? | Clearingkonto | Fysisk/Økonomisk? | Beløb |
    |---|---|---|---|---|---|---|---|
    | Køb, lagerafvigelse | 600170 | Lagerafvigelsesmaterialer | Udgift | Kredit | Nej | Finansielt | -10,00 |
    | Omkostning til købte materialer, der er modtaget | 140100 | Materialelager | Aktiv | Debet | Ja | Finansielt | -100,00 |
    | Udgifter til indkøb, ikke-faktureret | 600180 | Materialekvitteringer | Udgift | Debet | Ja | Finansielt | -100,00 |
    | Indkøb, periodisering | 200140 | Periodiserede køb | Passiv | Kredit | Ja | Finansielt | 100.00 |
    | Omkostning til købte materialer, der er faktureret | 140100 | Materialelager | Aktiv | Debet | Nej | Finansielt | 110.00 |
    | Udgifter til indkøb for produkt | 600180 | Materialekvittering | Udgift | Kredit | Nej | Finansielt | 110.00 |
    | Kreditorsaldo | 211000 | Kreditorhandel | Passiv | Kredit | Nej | Finansielt | -110,00 |

## <a name="example-2-charges-and-indirect-costs-on-the-purchase-order"></a>Eksempel 2: Gebyrer og indirekte omkostninger på indkøbsordren

Dette eksempelscenarie har følgende forudsætninger:

- FIFO-efterkalkulationsmodel
- **Gebyrkode 1:** Debetvare og kreditfinanskonto for 10 %
- **Gebyrkode 2:** Debetvare og kreditkunde/leverandør for 10,00 proportionalt
- **Indirekte omkostning:** 2,00 % føjet til købsprisen

Følgende procedure viser et eksempel på, hvad der sker, når du ændrer inkluderer gebyrer og indirekte omkostning på en indkøbsordre.

1. Opret en indkøbsordre for en mængde på 1 af en vare med en enhedspris på 100,00.
2. Tilføj en gebyrkode for 10 procent, der debiteres varen og krediteres finansmodulet.
3. Tilføj en gebyrkode for 10,00, der debiteres varen og krediteres kunden/leverandøren.
4. Fordel gebyrerne på indkøbsordrelinjerne.
5. Bekræft indkøbsordren.
6. Bogfør produktkvitteringen for indkøbsordren.
7. Valider bilaget på produktkvitteringen. Følgende tabel viser et eksempelbilag.

    | Bogføringstype | Hovedkonto | Hovedkontonavn | Kontotype | Debet/Kredit? | Clearingkonto | Fysisk eller økonomisk | Beløb |
    |---|---|---|---|---|---|---|---|
    | Køb, lagerafvigelse | 600170 | Lagerafvigelsesmaterialer | Udgift | Kredit | Nej | Fysisk | -110,00 |
    | Anslåede indirekte omkostninger, der er overtaget | 600520 | Indirekte omkostninger, der er overtaget | Udgift | Kredit | Ja | Fysisk | -2,40 |
    | Indkøbsfragt | 600120 | Fragt-/transportomkostninger | Udgift | Kredit | Nej | Fysisk | -10,00 |
    | Omkostning til købte materialer, der er modtaget | 140100 | Materialelager | Aktiv | Debet | Ja | Fysisk | 122.40 |
    | Udgifter til indkøb, ikke-faktureret | 600180 | Materialekvitteringer | Udgift | Debet | Ja | Fysisk | 110.00 |
    | Indkøb, periodisering | 200140 | Periodiserede køb | Passiv | Kredit | Ja | Fysisk | -110,00 |

8. Bogfør fakturaen for indkøbsordren.
9. Valider bilaget på fakturaen. Følgende tabel viser et eksempelbilag.

    | Bogføringstype | Hovedkonto | Hovedkontonavn | Kontotype | Debet/Kredit? | Clearingkonto | Fysisk/Økonomisk? | Beløb |
    |---|---|---|---|---|---|---|---|
    | Køb, lagerafvigelse | 600170 | Lagerafvigelsesmaterialer | Udgift | Kredit | Nej | Finansielt | 0,00 |
    | Anslåede indirekte omkostninger, der er overtaget | 600520 | Indirekte omkostninger, der er overtaget | Udgift | Debet | Ja | Finansielt | 2.40 |
    | Indirekte omkostninger, der er overtaget | 600520 | Indirekte omkostninger, der er overtaget | Udgift | Debet | Nej | Finansielt | -2,40 |
    | Omkostning til købte materialer, der er modtaget | 140100 | Materialelager | Aktiv | Kredit | Ja | Finansielt | -110,00 |
    | Udgifter til indkøb, ikke-faktureret | 600180 | Materialekvitteringer | Udgift | Kredit | Ja | Finansielt | -110,00 |
    | Indkøb, periodisering | 200140 | Periodiserede køb | Passiv | Debet | Ja | Finansielt | 110.00 |
    | Omkostning til købte materialer, der er faktureret | 140100 | Materialelager | Aktiv | Debet | Nej | Finansielt | 110.00 |
    | Udgifter til indkøb for produkt | 600180 | Materialekvittering | Udgift | Kredit | Nej | Finansielt | 110.00 |
    | Kreditorsaldo | 211000 | Kreditorhandel | Passiv | Kredit | Nej | Finansielt | -110,00 |
