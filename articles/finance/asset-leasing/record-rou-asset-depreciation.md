---
title: Registrere afskrivning af brugsretsaktiver (prøveversion)
description: I dette emne forklares det, hvordan du opretter kladdeposteringen til den amortisering, der kræves til rettigheder, som genkendes i en organisationsbalance.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseAssetSchedule
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 40af957582f9cdf4e1caf3ab03ead41f2823b42d59d427c7e7623cd8688e1827
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6778356"
---
# <a name="record-right-of-use-asset-depreciation-preview"></a>Registrere afskrivning af brugsretsaktiver (prøveversion)

[!include [banner](../includes/banner.md)]

For rettigheder, der anerkendes i en organisationsbalance, amortiseres ROU-aktivet på månedsbasis. Dette emne forklarer, hvordan du opretter kladdeposteringen til amortiseringen. Amortisering debiterer udgiftsfinanskontoen og krediterer finanskontoen for den akkumulerede afskrivning ud fra opsætningen af posteringsprofilen og leasingaftaletypen. Disse poster kan oprettes for hver leasingaftale, eller de kan oprettes til flere leasingaftaler ved hjælp af batchkladdefunktionen.

## <a name="asset-depreciation-schedule"></a>Afskrivningstidsplan for aktiv

1. Vælg en leasingaftale på siden **Leasingoversigt**. Vælg derefter **Kartotek \> planlægning af afskrivningsplan** for at åbne siden **Aktivafskrivningsplan**.

    Kladdeposten til ROU for aktivafskrivning er baseret på beløbet i kolonnen **Afskrivningsudgifter**. Du kan se et eksempel på retningslinjerne for kontering af standardoverholdelse under [Beregning af ROU for afskrivning af aktiver for finansieringsleasingaftaler](#calculation-of-rou-asset-amortization-expense-for-finance-leases) senere i dette emne.

2. Vælg afskrivningsperioden, og vælg derefter **Opret kladde**. Du får vist en meddelelse, hvor det angives, at den kladde, der skal bruges til registrering af afskrivningen, blev oprettet.
3. Vælg **Kladder \> Aktivleasingkladder** for at åbne siden **Aktivleasingkladde**, hvor du kan få vist den kladdepost for afskrivning, der er oprettet.
4. Vælg kladdeposteringen, og vælg derefter **Bogfør** for at registrere afskrivningsposten i Finans.

## <a name="calculation-of-rou-asset-amortization-expense-for-operating-leases"></a>Beregning af ROU-aktiver for driftsleasingaftaler

Afskrivningsudgifterne for en driftsleasingaftale beregnes som forskellen mellem den månedlige lineære leasingudgift og de månedlige renteudgifter i forbindelse med leasingpassiver i overensstemmelse med regnskabsstandarderne Codification Topic 842 (ASC 842), som er standarden i almindeligt anerkendte regnskabsprincipper i USA (US GAAP). Den lineære leasingomkostning beregnes som summen af alle leasingbetalinger divideret med leasingperioden i måneder. (Summen af leasingbetalinger omfatter eventuelle forudbetalinger, indledende direkte omkostninger, afmonteringsomkostninger og incitamenter.) I følgende tabel vises et eksempel på en driftsleasingaftale, der indeholder et eksempler på amortiseringsudgifterne.

### <a name="example-of-rou-asset-amortization-expense-for-operating-leases"></a>Eksempel på ROU-aktiver for driftsleasingaftaler

| Felt                                          | Værdi       |
|------------------------------------------------|-------------|
| Betalingsbeløb                                 | 1.000       |
| Betalingshyppighed                              | Månedligt     |
| Leasingperiode (måneder)                            | 24          |
| Samlede leasingbetalinger                           | 24,000      |
| Trinvis lånesats                     | 5 %          |
| Annuitetstype                                   | Forfalden annuitet |
| Sammensætningsinterval                           | Månedligt     |
| Nutidsværdi af fremtidige minimumsleasingbetalinger | 22,888.87   |

Som tidligere nævnt beregnes lineære leasingomkostninger som summen af alle leasingbetalinger divideret med leasingperioden. De månedlige renteudgifter beregnes automatisk på basis af planlægningen af passivafskrivning. Renteudgiften beregnes ved hjælp af metoden faktisk rentesats. Systemet vil bruge den lineære leasingomkostning til at trække renteudgiften fra for hver måned. Værdien bruges til at reducere ROU-aktivet.

| Måned | Lineær leasingomkostninger | Renteudgift                        | Beregning af udgifter til afskrivning af ROU-aktiver |
|-------|--------------------------|-----------------------------------------|-----------------------------------------------|
| 1     | (24.000 ÷ 24) = 1.000,00 | (22.888.87 – 1.000) × (5 % ÷ 12) = 91,20 | 1.000 – 91,20 = 908,80                        |
| 2     | (24.000 ÷ 24) = 1.000,00 | (21.980,08 – 1.000) × (5 % ÷ 12) = 87,42 | 1.000 – 87,42 = 912,58                        |
| 3     | (24.000 ÷ 24) = 1.000,00 | (21.067,49 – 1.000) × (5 % ÷ 12) = 83,62 | 1.000 – 83,62 = 916,39                        |

> [!NOTE]
> Ifølge ASC 842 klassificeres afskrivningen af ROU-aktivet for en driftsleasingaftale som en leasingomkostning på resultatopgørelsen. For synlighed beskriver aktivleasing posten som afskrivningen af ROU-aktivet. Debetposten skal dog tildeles en konto til driftsleasing, og kreditposten skal tildeles direkte til ROU-aktivet for driftsleasing. Men i leasingparametrene kan du angive, at kreditposter skal oprettes til en akkumuleret afskrivningskonto for drifts ROU-aktiver.

## <a name="calculation-of-rou-asset-amortization-expense-for-finance-leases"></a>Beregning af ROU-aktiver for finansiel leasing

For leasingaftaler, der har en finansieringsklassifikation, beregner systemet anlægsaktivets amortisering på et lineært grundlag. Derfor vil afskrivningsudgiften være ens for hver måned.

I overensstemmelse med International Financial Reporting Standard 16 (IFRS 16) og ASC 842 vil aktivet blive amortiseret i enten leasingperioden eller aktivets levetid, afhængigt af hvad der er mindre. Hvis parameteren **Overdragelsen af ejerskab** også er slået til for leasingaftalen, vil leasingaftalen automatisk blive afskrevet over aktivets levetid.

### <a name="example-of-rou-asset-amortization-expense-for-finance-leases"></a>Eksempel på ROU-aktiver for finansielle leasingaftaler

| Felt                                | Værdi                                   |
|--------------------------------------|-----------------------------------------|
| Startsaldo for brugsretsaktiver | 22,889.87                               |
| Leasingperiode (måneder)                  | 24                                      |
| Brugstid for aktiv (måneder)           | 36                                      |
| Måned                                | Afskrivning af brugsretsaktiver |
| 1                                    | 22.889,87 ÷ 24 = 953,74                 |
| 2                                    | 22.889,87 ÷ 24 = 953,74                 |
| 3                                    | 22.889,87 ÷ 24 = 953,74                 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
