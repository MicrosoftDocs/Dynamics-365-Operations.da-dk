---
title: Beregning og afrunding af salgsmoms
description: Denne artikel indeholder en oversigt over momsberegning og afrunding og forklarer parametrene for momsberegning og afrundingsopsætning.
author: wangchen
ms.date: 06/01/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom:
- "13111"
- intro-internal
ms.assetid: fe5fdc7f-9834-49fb-a611-1dd9c289619d
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2022-05-31
ms.dyn365.ops.version: AX 10.0.28
ms.openlocfilehash: aa3564f0fcf4a958637ba4a5cdcc497bffc50000
ms.sourcegitcommit: 8b716849707ec96d1cb4cac85b9e782dc25f5a70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/07/2022
ms.locfileid: "8939227"
---
# <a name="sales-tax-calculation-and-rounding"></a>Beregning og afrunding af salgsmoms

[!include [banner](../includes/banner.md)]

Denne artikel giver et overblik over momsberegning og afrunding i Microsoft Dynamics 365 Finance. Den forklarer også de parametre, der bruges i opsætningen af momsberegning og -afrunding, og hvordan disse parametre arbejder sammen.

## <a name="parameters"></a>Parametre

Flere parametre styrer momsberegning og afrunding:

- **Beregningsmetode** – Denne parameter angives på siden **Finansparametre** og definerer, om momsbasisbeløbet beregnes pr. dokument eller pr. linje. Hvis parameteren **Beregningsgrundlag** for momskoden er angivet til **Nettobeløbet for fakturasaldo**, beregnes momsbasisbeløbet altid pr. dokument, uanset indstillingen i denne parameter.
- **Afrunding efter** – Denne parameter angives for momsgruppen og definerer, om momsbeløbet afrundes pr. momskode eller pr. momskodekombination.
- **Grundlag** – Denne parameter angives for momskoden og definerer, hvordan momsbeløbet beregnes. Du kan finde flere oplysninger i [Momsberegningsmetoderne i feltet Grundlag](sales-tax-calculation-methods-origin-field.md).
- **Beregningsgrundlag** – Denne parameter angives for momskoden og bestemmer, hvilke beløb der bruges til at vælge passende momssatser på siden **Momskodeværdier**. Du kan finde flere oplysninger i [Momssatser baseret på beregningsgrundlaget og felter for beregningsmetoder](marginal-base-field.md).
- **Momsafrundingsregel** – Denne parameter angives for momskoden og definerer, hvordan det fastlagte momsbeløb afrundes, herunder afrundingspræcision og afrundingsmetoden.

Resten af denne artikel indeholder nogle typiske eksempler på momsberegning og afrunding, der bruger en kombination af de foregående parametre.

## <a name="scenario-for-the-examples"></a>Scenario for eksemplerne

- Der er to linjer i momsdokumentet, og momsgrundlagsbeløbet for hver linje er 42,42.
- Der defineres to momskoder for hver linje: momskode 1 og momskode 2.
- Momssatsen for både momskode 1 og momskode 2 er 10 procent.
- Prisen er uden moms.
- Afrundingspræcisionen er 0,01.
- Afrundingsmetoden er **Rund op**.

## <a name="example-1"></a>Eksempel 1

### <a name="parameter-values"></a>Parameterværdier

| Beregningsmetode | Afrunding efter    | Oprindelse                   | Beregningsgrundlag       |
| ------------------ | -------------- | ------------------------ | ------------------- |
| Linje               | Momskode | Procent af nettobeløb | Nettobeløb pr. linje |

### <a name="calculation-and-rounding-behavior"></a>Beregnings- og afrundingsfunktion

| Linjenummer | Momskode | Beløbsoprindelse | Momsbeløb |
| ------------| ---------------| --------------| -----------------|
| 1           | Kode 1         | 42,42         | 4,25             |
| 1           | Kode 2         | 42,42         | 4,25             |
| 2           | Kode 1         | 42,42         | 4,25             |
| 2           | Kode 2         | 42,42         | 4,25             |

Momsbasisbeløbet beregnes pr. linje:

- **Linje 1:** 42,42
- **Linje 2:** 42,42

Momsbeløbet beregnes pr. momskode:

- **Linje 1:**

    - Momsbeløb for momskode 1 = 42,42 &times; 10 procent = 4,242
    - Momsbeløb for momskode 2 = 42,42 &times; 10 procent = 4,242

- **Linje 2:**

    - Momsbeløb for momskode 1 = 42,42 &times; 10 procent = 4,242
    - Momsbeløb for momskode 2 = 42,42 &times; 10 procent = 4,242

Momsbeløbet afrundes pr. momskode:

- **Linje 1:**

    - Afrundet momsbeløb for momskode 1 = 4,25
    - Afrundet momsbeløb for momskode 2 = 4,25

- **Linje 2:**

    - Afrundet momsbeløb for momskode 1 = 4,25
    - Afrundet momsbeløb for momskode 2 = 4,25

## <a name="example-2"></a>Eksempel 2

### <a name="parameter-values"></a>Parameterværdier

| Beregningsmetode | Afrunding efter    | Oprindelse                   | Beregningsgrundlag                 |
| ------------------ | -------------- | ------------------------ | ----------------------------- |
| Linje/total         | Momskode | Procent af nettobeløb | Nettobeløb på fakturasaldo |

### <a name="calculation-and-rounding-behavior"></a>Beregnings- og afrundingsfunktion

| Linjenummer | Momskode | Beløbsoprindelse | Momsbeløb |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kode 1         | 42,42         | 4,25             |
| 1           | Kode 2         | 42,42         | 4,25             |
| 2           | Kode 1         | 42,42         | 4,24             |
| 2           | Kode 2         | 42,42         | 4,24             |

Momsbasisbeløbet beregnes pr. dokument:

- Momsgrundlagsbeløb = 42,42 + 42,42 = 84,84

Momsbeløbet beregnes pr. momskode:

- Momsbeløb for momskode 1 = 84,84 &times; 10 procent = 8,484
- Momsbeløb for momskode 2 = 84,84 &times; 10 procent = 8,484

Momsbeløbet afrundes pr. momskode:

- Afrundet momsbeløb for momskode 1 = 8,49
- Afrundet momsbeløb for momskode 2 = 8,49

Afrundet momsbeløb tildeles hver linje pr. momskode:

- Tildel det afrundede momsbeløb for momskode 1 (8,49) til linje 1 (4,25) og linje 2 (4,24).
- Tildel det afrundede momsbeløb for momskode 2 (8,49) til linje 1 (4,25) og linje 2 (4,24).

## <a name="example-3"></a>Eksempel 3

### <a name="parameter-values"></a>Parameterværdier

| Beregningsmetode | Afrunding efter    | Oprindelse                              | Beregningsgrundlag       |
| ------------------ | -------------- | ----------------------------------- | ------------------- |
| Linje               | Momskode | Beregnet procent af nettobeløb | Nettobeløb pr. linje |

### <a name="calculation-and-rounding-behavior"></a>Beregnings- og afrundingsfunktion

| Linjenummer | Momskode | Beløbsoprindelse | Momsbeløb |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kode 1         | 42,42         | 4,72             |
| 1           | Kode 2         | 42,42         | 4,72             |
| 2           | Kode 1         | 42,42         | 4,72             |
| 2           | Kode 2         | 42,42         | 4,72             |

Momsbasisbeløbet beregnes pr. linje:

- **Linje 1:** 42,42
- **Linje 2:** 42,42

Momsbeløbet beregnes pr. momskode:

- **Linje 1:**

    - Momsbeløb for momskode 1 = 42,42 &times; 10 procent &divide; (1 – 10 procent) = 4,7133
    - Momsbeløb for momskode 2 = 42,42 &times; 10 procent &divide; (1 – 10 procent) = 4,7133

- **Linje 2:**

    - Momsbeløb for momskode 1 = 42,42 &times; 10 procent &divide; (1 – 10 procent) = 4,7133
    - Momsbeløb for momskode 2 = 42,42 &times; 10 procent &divide; (1 – 10 procent) = 4,7133

Momsbeløbet afrundes pr. momskode:

- **Linje 1:**

    - Afrundet momsbeløb for momskode 1 = 4,72
    - Afrundet momsbeløb for momskode 2 = 4,72

- **Linje 2:**

    - Afrundet momsbeløb for momskode 1 = 4,72
    - Afrundet momsbeløb for momskode 2 = 4,72

## <a name="example-4"></a>Eksempel 4

### <a name="parameter-values"></a>Parameterværdier

| Beregningsmetode | Afrunding efter    | Oprindelse                              | Beregningsgrundlag                 |
| ------------------ | -------------- | ----------------------------------- | ----------------------------- |
| Linje/total         | Momskode | Beregnet procent af nettobeløb | Nettobeløb på fakturasaldo |

### <a name="calculation-and-rounding-behavior"></a>Beregnings- og afrundingsfunktion

| Linjenummer | Momskode | Beløbsoprindelse | Momsbeløb |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kode 1         | 42,42         | 4,72             |
| 1           | Kode 2         | 42,42         | 4,72             |
| 2           | Kode 1         | 42,42         | 4,71             |
| 2           | Kode 2         | 42,42         | 4,71             |

Momsbasisbeløbet beregnes pr. dokument:

- Momsgrundlagsbeløb = 42,42 + 42,42 = 84,84

Momsbeløbet beregnes pr. momskode:

- Momsbeløb for momskode 1 = 84,84 &times; 10 procent &divide; (1 – 10 procent) = 9,4267
- Momsbeløb for momskode 2 = 84,84 &times; 10 procent &divide; (1 – 10 procent) = 9,4267

Momsbeløbet afrundes pr. momskode:

- Afrundet momsbeløb for momskode 1 = 9,43
- Afrundet momsbeløb for momskode 2 = 9,43

Afrundet momsbeløb tildeles hver linje pr. momskode:

- Tildel momsbeløbet for momskode 1 (9,43) til linje 1 (4,72) og linje 2 (4,71).
- Tildel momsbeløbet for momskode 2 (9,43) til linje 1 (4,72) og linje 2 (4,71).

## <a name="example-5"></a>Eksempel 5

### <a name="parameter-values"></a>Parameterværdier

| Beregningsmetode | Afrunding efter                | Oprindelse                   | Beregningsgrundlag       |
| ------------------ | -------------------------- | ------------------------ | ------------------- |
| Linje               | Momskodekombination | Procent af nettobeløb | Nettobeløb pr. linje |

### <a name="calculation-and-rounding-behavior"></a>Beregnings- og afrundingsfunktion

| Linjenummer | Momskode | Beløbsoprindelse | Momsbeløb |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kode 1         | 42,42         | 4,25             |
| 1           | Kode 2         | 42,42         | 4,24             |
| 2           | Kode 1         | 42,42         | 4,24             |
| 2           | Kode 2         | 42,42         | 4,24             |

Momsbasisbeløbet beregnes pr. linje:

- **Linje 1:** 42,42
- **Linje 2:** 42,42

Momsbeløbet beregnes pr. momskode:

- **Linje 1:**

    - Momsbeløb for momskode 1 = 42,42 &times; 10 procent = 4,242
    - Momsbeløb for momskode 2 = 42,42 &times; 10 procent = 4,242

- **Linje 2:**

    - Momsbeløb for momskode 1 = 42,42 &times; 10 procent = 4,242
    - Momsbeløb for momskode 2 = 42,42 &times; 10 procent = 4,242

Momsbeløbet afrundes pr. momskodekombination:

- Samlet momsbeløb = 4,242 + 4,242 + 4,242 + 4,242 = 16,968, som rundes op til 16,97

Afrundet momsbeløb tildeles hver linje pr. momskode:

- Tildel momsbeløbet (16,97) til linje 1 og linje 2:

    - **Linje 1:**

        - Momsbeløb for momskode 1 = 4,25
        - Momsbeløb for momskode 2 = 4,24

    - **Linje 2:**

        - Momsbeløb for momskode 1 = 4,24
        - Momsbeløb for momskode 2 = 4,24

## <a name="example-6"></a>Eksempel 6

### <a name="parameter-values"></a>Parameterværdier

| Beregningsmetode | Afrunding efter                | Oprindelse                   | Beregningsgrundlag                 |
| ------------------ | -------------------------- | ------------------------ | ----------------------------- |
| Linje/total         | Momskodekombination | Procent af nettobeløb | Nettobeløb på fakturasaldo |

### <a name="calculation-and-rounding-behavior"></a>Beregnings- og afrundingsfunktion

| Linjenummer | Momskode | Beløbsoprindelse | Momsbeløb |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kode 1         | 42,42         | 4,25             |
| 1           | Kode 2         | 42,42         | 4,24             |
| 2           | Kode 1         | 42,42         | 4,24             |
| 2           | Kode 2         | 42,42         | 4,24             |

Momsbasisbeløbet beregnes pr. dokument:

- Momsgrundlagsbeløb = 42,42 + 42,42 = 84,84

Momsbeløbet beregnes pr. momskode:

- Momsbeløb for momskode 1 = 84,84 &times; 10 procent = 8,484
- Momsbeløb for momskode 2 = 84,84 &times; 10 procent = 8,484

Momsbeløbet afrundes pr. momskodekombination:

- Samlet momsbeløb = 8,484 + 8,484 = 16,968, som rundes op til 16,97

Afrundet momsbeløb tildeles hver linje pr. momskode:

- Tildel momsbeløbet (16,97) til linje 1 og linje 2:

    - **Linje 1:**

        - Momsbeløb for momskode 1 = 4,25
        - Momsbeløb for momskode 2 = 4,24

    - **Linje 2:**

        - Momsbeløb for momskode 1 = 4,24
        - Momsbeløb for momskode 2 = 4,24

## <a name="example-7"></a>Eksempel 7

### <a name="parameter-values"></a>Parameterværdier

| Beregningsmetode | Afrunding efter                | Oprindelse                              | Beregningsgrundlag       |
| ------------------ | -------------------------- | ----------------------------------- | ------------------- |
| Linje               | Momskodekombination | Beregnet procent af nettobeløb | Nettobeløb pr. linje |

### <a name="calculation-and-rounding-behavior"></a>Beregnings- og afrundingsfunktion

| Linjenummer | Momskode | Beløbsoprindelse | Momsbeløb |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kode 1         | 42,42         | 4,72             |
| 1           | Kode 2         | 42,42         | 4,71             |
| 2           | Kode 1         | 42,42         | 4,71             |
| 2           | Kode 2         | 42,42         | 4,72             |

Momsbasisbeløbet beregnes pr. linje:

- **Linje 1:** 42,42
- **Linje 2:** 42,42

Momsbeløbet beregnes pr. momskode:

- **Linje 1:**

    - Momsbeløb for momskode 1 = 42,42 &times; 10 procent &divide; (1 – 10 procent) = 4,7133
    - Momsbeløb for momskode 2 = 42,42 &times; 10 procent &divide; (1 – 10 procent) = 4,7133

- **Linje 2:**

    - Momsbeløb for momskode 1 = 42,42 &times; 10 procent &divide; (1 – 10 procent) = 4,7133
    - Momsbeløb for momskode 2 = 42,42 &times; 10 procent &divide; (1 – 10 procent) = 4,7133

Momsbeløbet afrundes pr. momskodekombination:

- Samlet momsbeløb = 4,7133 + 4,7133 + 4,7133 + 4,7133 = 18,8532, som rundes op til 18,86

Afrundet momsbeløb tildeles hver linje pr. momskode:

- Tildel momsbeløbet (18,86) til linje 1 og linje 2:

    - **Linje 1:**

        - Momsbeløb for momskode 1 = 4,72
        - Momsbeløb for momskode 2 = 4,71

    - **Linje 2:**

        - Momsbeløb for momskode 1 = 4,71
        - Momsbeløb for momskode 2 = 4,72

## <a name="example-8"></a>Eksempel 8

### <a name="parameter-values"></a>Parameterværdier

| Beregningsmetode | Afrunding efter                | Oprindelse                              | Beregningsgrundlag                 |
| ------------------ | -------------------------- | ----------------------------------- | ----------------------------- |
| Linje/total         | Momskodekombination | Beregnet procent af nettobeløb | Nettobeløb på fakturasaldo |

### <a name="calculation-and-rounding-behavior"></a>Beregnings- og afrundingsfunktion

| Linjenummer | Momskode | Beløbsoprindelse | Momsbeløb |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kode 1         | 42,42         | 4,72             |
| 1           | Kode 2         | 42,42         | 4,71             |
| 2           | Kode 1         | 42,42         | 4,71             |
| 2           | Kode 2         | 42,42         | 4,72             |

Momsbasisbeløbet beregnes pr. dokument:

- Momsgrundlagsbeløb = 42,42 + 42,42 = 84,84

Momsbeløbet beregnes pr. momskode:

- Momsbeløb for momskode 1 = 84,84 &times; 10 procent &divide; (1 – 10 procent) = 9,4267
- Momsbeløb for momskode 2 = 84,84 &times; 10 procent &divide; (1 – 10 procent) = 9,4267

Momsbeløbet afrundes pr. momskodekombination:

- Samlet momsbeløb = 9,4267 + 9,4267 = 18,8534, som rundes op til 18,86

Afrundet momsbeløb tildeles hver linje pr. momskode:

- Tildel momsbeløbet (18,86) til linje 1 og linje 2:

    - **Linje 1:**

        - Momsbeløb for momskode 1 = 4,72
        - Momsbeløb for momskode 2 = 4,71

    - **Linje 2:**

        - Momsbeløb for momskode 1 = 4,71
        - Momsbeløb for momskode 2 = 4,72

## <a name="additional-resources"></a>Yderligere ressourcer

- [Momsberegningsmetoder i feltet Grundlag](sales-tax-calculation-methods-origin-field.md)
- [Momssatser baseret på beregningsgrundlaget og beregningsmåderne](marginal-base-field.md)
- [Indstillinger for beregning af hele beløbet og intervaller for momskoder](whole-amount-interval-options-sales-tax-codes.md)
