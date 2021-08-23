---
title: Leasingbogføringstyper
description: I dette emne beskrives de bogføringstyper, der bruges til aktivleasingtransaktioner.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 721463000c05eb1774335ccce1af39468c2aed9f179e5e88d8725f4d265d6870
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6718241"
---
# <a name="lease-posting-types"></a>Leasingbogføringstyper

[!include [banner](../includes/banner.md)]

I dette emne beskrives de bogføringstyper, der bruges til aktivleasingtransaktioner.

## <a name="lease-asset"></a>Leasingaktiv

Kontoen er knyttet til ROU-forbrugsretaktivet. Denne konto debiteres, når en leasingaftale oprindeligt genkendes i henhold til de nye regnskabsstandarder for leasingaftaler, Codification Emne 842 (ASC 842) og International Financial Reporting standard 16 (IFRS 16). I forbindelse med en ændret leasingaftale kan denne konto enten blive debiteret eller krediteret, afhængigt af om ændringen øger eller reducerer leasingforpligtelsen.

**Eksempler på kladdeposter:** Oprindelig genkendelse<br>
**Debet:** Leasingaktiv xxx<br>
**Kredit:** Leasingforpligtelse xxx

## <a name="lease-liability"></a>Leasingforpligtelse

Kontoen er knyttet til den leasginforpligtelse, der forekommer, når betalinger diskonteres i henhold til de nye IFRS 16- og ASC 842-standarder. Denne konto krediteres, når en leasingaftale i begyndelsen anerkendes under de nye standarder. Den debiteres for leasingbetalinger og krediteres for renteperiodiseringer.

**Eksempler på kladdeposter:** Oprindelig genkendelse<br>
**Debet:** Leasingaktiv xxx<br>
**Kredit:** Leasingforpligtelse xxx

**Eksempel kladdeposter:** Renteperiodisering<br>
**Debet:** Renteudgift xxx<br>
**Kredit:** Leasingforpligtelse xxx

**Eksempel på kladdeposter:** Leasingbetaling<br>
**Debet:** Leasingforpligtelse xxx<br>
**Kredit:** Kreditor-/leasingbetaling xxx

## <a name="short-term-lease-liability"></a>Kortfristet leasingforpligtelse

Kontoen er tilknyttet den kortfristede leasingforpligtelse, når den kortfristede leasingforpligtelse bogføres som kladdepostering. Denne konto krediteres på kortsigtede passiver fra amortiseringsplanen på den sidste dag i måneden. Det samme beløb debiteres dog den første dag i den næste måned.

**Eksempler på kladdeposter:** Kortfristet leasingforpligtelse<br>
**Debet:** Leasingforpligtelse xxx<br>
**Kredit:** Kortfristet leasingforpligtelse xxx<br>
**Debet:** Kortfristet leasingforpligtelse xxx<br>
**Kredit:** Leasingforpligtelse xxx

## <a name="depreciation-expense"></a>Afskrivningsomkostning

Kontoen er tilknyttet den udgift, der er relateret til afskrivningen af ROU-aktivet under IFRS 16, ASC 842, og finansielle leasingaftaler under IAS 17 og ASC 840. Denne konto debiteres, når et ROU-aktiv afskrives hver måned.

**Eksempel på kladdeposter:** Afskrivningsperiodisering<br>
**Debet:** Afskrivningsudgift xxx<br>
**Kredit:** Akkumuleret afskrivning xxx

## <a name="gainloss-on-lease-modification"></a>Gevinst/tab ved leasingændring

Kontoen er tilknyttet eventuelle gevinster eller tab, der opstår i forbindelse med leasingændringer. Der kan opstå en indtægt under en ændring af leasingaftalen, hvis ændringen reducerer leasingforpligtelsen med et beløb, der overstiger ROU-aktivets bærende værdi.

En leasingaftale har f. eks. en aktuel værdi på $150.000 og en bærende værdi af det ROU-aktiv i $100.000. Leasingaftalen ændres, og denne ændring giver en ny nutidsværdi af de fremtidige minimums leasingbetaling (PVFMLP) på $40.000. Leasingforpligtelsen debiteres med $110.000 ($150.000 – $40.000). Da ROU-aktivet kun er $100.000, vil reduktionen på $110.000 reducere aktivet med 0 (nul). Derfor angiver regnskabsvejledningen, at resten skal konteres til en gevinstkonto. I dette tilfælde vil den endelige journaloptegnelse være en debitering af leasingforpligtelsen på $110.000, en kreditering til leasingaktivet på $100.000 og en kreditering på gevinstkontoen på $10.000.

**Eksempel på kladdeposter:** Leasingændringer<br>
**Debet:** Leasingforpligtelse xxx<br>
**Kredit:** Leasingaktiv xxx<br>
**Kredit:** Gevinst xxx

## <a name="accumulated-depreciation"></a>Akkumuleret afskrivning

Kontoen er tilknyttet ROU-anlægsaktivets konto. Denne konto krediteres, når der afskrives udgifter.

**Eksempel på kladdeposter:** Afskrivningsperiodisering<br>
**Debet:** Afskrivningsudgift xxx<br>
**Kredit:** Akkumuleret afskrivning xxx

## <a name="variable-payment"></a>Variabel betaling

Kontoen er knyttet til variable leasingbetalinger, der er produceret af en indeksværdiregulering under ASC 842, ASC 840 og IAS 17-leasingaftaler. I betalingsplanen for leasingaftalen medtages variable betalinger i kolonnen **Variabel betaling**. Denne konto debiteres, når der oprettes en faktura i forhold til en betalingsplanlinje, der indeholder en variabel betaling.

**Eksempel på kladdeposter:** Leasingbetaling<br>
**Debet:** Leasingforpligtelse xxx<br>
**Debet:** Variabel betaling xxx<br>
**Kredit:** Kreditor-/leasingbetaling xxx

## <a name="deferred-rent-asset-liability"></a>Aktiv med udskudt leje (passiv)

Kontoen er knyttet til det udskudte aktiv- eller passivbeløb, der er fremstillet af en leasingaftale til at blive forskudt til lejebehandling. Denne konto debiteres, når en faktura bogføres i forhold til en udskudt lejebehandling af leasingaftale, hvis betalingsbeløbet er mere end periodens lejeudgifter. Den krediteres, hvis leasingbetalingen er mindre end den lineære lejeudgifter for perioden.

**Eksempler på kladdeposter:** Leasingbetaling (udskudt rettighed til lejebehandling af leasingaftale)<br>
**Debet:** Leasingudgift xxx<br>
**Kredit:** Leasingaftale med udskudt leje XXX<br>
**Kredit:** Kreditor-/leasingbetaling xxx

## <a name="lease-expense"></a>Leasingudgift

Kontoen er tilknyttet leasingudgift, hvis leasingen klassificeres som en rettighed til at opnå en udskudt lejebehandling af leasingaftalen. Denne konto debiteres, når en faktura bogføres i forhold til en leasingaftale til udskudt lejebehandling.

**Eksempler på kladdeposter:** Leasingbetaling (udskudt rettighed til lejebehandling af leasingaftale)<br>
**Debet:** Leasingudgift xxx<br>
**Kredit:** Leasingaftale med udskudt leje XXX<br>
**Kredit:** Kreditor-/leasingbetaling xxx

## <a name="impairment-expense"></a>Udgift til værdiforringelse

Kontoen bogføres i forhold til, når en leasingaftale er forringet. Denne konto debiteres, mens ROU-aktivkonto krediteres direkte.

**Eksempel på kladdeposter:** Leasingbetaling<br>
**Debet:** Udgift til værdiforringelse xxx<br>
**Kredit:** ROU-aktiv xxx

## <a name="lease-payment"></a>Leasingbetaling

Kontoen bogføres i forhold til parameteren **Betal til kreditor** er deaktiveret. Denne konto krediteres i stedet for kreditoren, hvis parameteren er deaktiveret.

**Eksempel på kladdeposter:** Leasingbetaling<br>
**Debet:** Leasingforpligtelse xxx<br>
**Kredit:** Leasingaftalebetaling xxx

## <a name="expense-type-postings"></a>Udgiftstypeposteringer

Den konto, der er valgt for hver udgiftstype, debiteres, når der genereres en betaling for den pågældende udgiftstype. Den konto, der er angivet for udgiftstypen **Forsikring**, debiteres f. eks., når en faktura- eller betalingskladdepost oprettes ud fra planlægningen af det udførende omkostningsskema for forsikringsudgifter.

**Eksempel på kladdeposter:** Forsikringsbetaling<br>
**Debet:** Forsikringsudgiftstypekonto xxx<br>
**Kredit:** Modkonto xxx

> [!NOTE]
> Modkontoen vælges på leasingniveau på linjerne for betalingsplanen for driftsomkostninger. Denne modkonto kan knyttes til kreditoren eller en finanskonto.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
