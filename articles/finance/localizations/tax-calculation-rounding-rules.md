---
title: Regler for afrunding af momsberegning
description: Dette emne indeholder oplysninger om afrundingsreglerne i parametrene for momsberegning for tjenesten Momsberegning.
author: kailiang
ms.date: 07/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 38760879d84d8262cc1e8395c59bcbc0429bc753
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/13/2021
ms.locfileid: "7347679"
---
# <a name="tax-calculation-rounding-rules"></a>Regler for afrunding af momsberegning

[!include [banner](../includes/banner.md)]

Dette emne indeholder oplysninger om, hvordan afrundingsreglerne fungerer i parametrene for momsberegning for tjenesten Momsberegning.

> [!NOTE] 
> Når tjenesten Momsberegning er aktiveret, er afrundingsreglerne på siderne **Momskode** og **Momsgruppe** ikke aktiveret.

Du kan få vist konfigurationen af afrundingsregler for tjenesten Momsberegning i sektionen **Afrundingsregel for moms** i oversigtspanelet **Beregning** under fanen **Generelt** på siden **Parametre for momsberegning** (**Moms** \> **Opsætning** \> **Momskonfiguration** \> **Parametre for momsberegning**).

[![Konfiguration af afrundingsregler på siden Parametre for momsberegning](./media/tax-calculation-parameters-calculation-1.png)](./media/tax-calculation-parameters-calculation-1.png)

Felterne **Afrundingpræcision** og **Afrundingsmetode** bestemmer, hvordan beregnede beløb i nyttedataene fra tjenesten Momsberegning afrundes.

## <a name="rounding-precision"></a>Afrundingspræcision

Felterne for **Afrundingpræcision** understøtter en værdi med op til seks decimaler. Hvis du f.eks. angiver feltet **Afrundingpræcision** til **0,000000**, afrundes beregnede beløb til seks decimaler og sendes derefter til Microsoft Dynamics 365 Finance. Hvis der f.eks. anvendes afrundingsmetoden **Normal**, afrundes beløbet **987,1234567** til **987,123457**.

> [!NOTE]
> Finance-afrunder beløb ifølge valutaens afrundingsregler. De momsbeløb, der vises og registreres i transaktioner, påvirkes derfor både af afrundingsregler for momsberegning og valutaafrundingsregler.

## <a name="rounding-method"></a>Afrundingsmetode

Afrundingsmetoden for momsberegning kan konfigureres for hver juridisk enhed. I feltet **Afrundingsmetode** kan du vælge mellem tre indstillinger: **Normal**, **Nedad** og **Oprunding**.

### <a name="rounding-example"></a>Eksempel på afrunding

Følgende tabel indeholder et eksempel på, hvordan beløbet **987,345** afrundes til forskellige kombinationer af afrundingpræcisioner og afrundingsmetoder.

<table>
<thead>
<tr>
<th rowspan="2">Afrundingsmetode</th>
<th colspan="8">Afrundingspræcision</th>
</tr>
<tr>
<th>0,00</th>
<th>0.01</th>
<th>0.10</th>
<th>1.00</th>
<th>10.00</th>
<th>0.02</th>
<th>0.05</th>
<th>0.25</th>
</tr>
</thead>
<tbody>
<tr>
<td>Almindelig</td>
<td>987.35</td>
<td>987.35</td>
<td>987.30</td>
<td>987.00</td>
<td>990.00</td>
<td>987.34</td>
<td>987.35</td>
<td>987.25</td>
</tr>
<tr>
<td>Nedad</td>
<td>987.00</td>
<td>987.34</td>
<td>987.30</td>
<td>987.00</td>
<td>980.00</td>
<td>987.34</td>
<td>987.30</td>
<td>987.25</td>
</tr>
<tr>
<td>Oprunding</td>
<td>988.00</td>
<td>987.35</td>
<td>987.40</td>
<td>988.00</td>
<td>990.00</td>
<td>987.36</td>
<td>987.35</td>
<td>987.50</td>
</tr>
</tbody>
</table>

Beregnings- og afrundingslogikken for momsbeløb kan konfigureres i overensstemmelse med momsreglerne.

## <a name="rounding-by"></a>Afrunding efter 

Vælg det afrundingsprincip, som gælder for moms, i feltet **Afrunding efter**. Der findes følgende indstillinger:

- **Momskoder** – Afrund momsbeløbet inden for hver momskode.
- **Momskodekombinationer** – Afrund momsbeløbet inden for momskodekombinationen på linjen.

## <a name="calculation-method"></a>Beregningsmåde

Vælg, om der skal beregnes moms for hver linje eller alle linjer, i feltet **Beregningsmetode**. Der findes følgende indstillinger:

- **Linje** – Beregn momsbeløbet linje for linje. Momsbeløbet på hver linje er ikke påvirket af momsbeløbet på andre linjer.
- **Total** – Beregn momsbeløbet på tværs af alle linjer i et dokument.

### <a name="rounding-calculation-example"></a>Eksempel på afrunding af momsberegning

Dette eksempel viser de forskellige beregninger, der kan udføres for en faktura, for forskellige kombinationer af værdier for **Afrunding efter** og **Beregningsmetode**. I dette eksempel er følgende opsætning på plads:

- Fakturaen indeholder fire linjer.
- Der findes to momskoder: **VAT1** (10 procent) og **VAT2** (10 procent).
- Afrundingpræcisionen er angivet til **0,01**.
- Afrundingsmetoden er angivet til **Oprunding**.

#### <a name="rounding-by--tax-codes-and-calculation-method--line"></a>Afrunding efter = Momskoder og beregningsmetode = Linje

| Linjenummer | Linjenettobeløb | Bestemte momskoder | Momsbeløb før afrunding | Afrundet momsbeløb |
|-------------|-----------------|----------------------|----------------------------|--------------------|
| 1           | 11.11           | VAT1                 | 1.111                      | 1.12               |
| 2           | 22.22           | VAT1; VAT2           | 2,222; 2,222               | 2,23; 2,23         |
| 3           | 33.33           | VAT1                 | 3.333                      | 3.34               |
| 4           | 44.44           | VAT1; VAT2           | 4,444; 4;444               | 4,45; 4,45         |

#### <a name="rounding-by--tax-code-combinations-and-calculation-method--line"></a>Afrunding efter = Momskoder og beregningsmetode = Linje

| Linjenummer | Linjenettobeløb | Bestemte momskoder | Momsbeløb før afrunding | Afrundet momsbeløb |
|-------------|-----------------|----------------------|----------------------------|--------------------|
| 1           | 11.11           | VAT1                 | 1.111                      | 1.12               |
| 2\*         | 22.22           | VAT1; VAT2           | 2,222; 2,222               | 2,23; 2,22         |
| 3           | 33.33           | VAT1                 | 3.333                      | 3.34               |
| 4\*\*       | 44.44           | VAT1; VAT2           | 4,444; 4;444               | 4,45; 4,44         |

\* Linje 2 = Afrund\[22,22 × (10 % + 10 %)\] = 2,23 + 2,22

\*\* Linje 4 = Afrund\[44,44 × (10 % + 10 %)\] = 4,45 + 4,44

#### <a name="rounding-by--tax-codes-and-calculation-method--total"></a>Afrunding efter = Momskoder og beregningsmetode = Total

| Linjenummer | Linjenettobeløb | Bestemte momskoder | Momsbeløb før afrunding | Afrundet momsbeløb |
|-------------|-----------------|----------------------|----------------------------|--------------------|
| 1           | 11.11           | VAT1\*               | 1.111                      | 1.12               |
| 2           | 22.22           | VAT1\*; VAT2\*\*     | 2,222; 2,222               | 2,22; 2,23         |
| 3           | 33.33           | VAT1\*               | 3.333                      | 3.33               |
| 4           | 44.44           | VAT1\*; VAT2\*\*     | 4,444; 4;444               | 4,44; 4,44         |

\* VAT1 (Linje 1, Linje 2, Linje 3, Linje 4) = Afrund\[(11,11 + 22,22 + 33,33 + 44,44) × 10 %\] = 1,12 + 2,22 + 3,33 + 4,44

\*\* VAT2 (Linje 2, Linje 4) = Afrund\[(22,22 + 44,44) × 10 %\] = 2,23 + 4,44

#### <a name="rounding-by--tax-code-combinations-and-calculation-method--total"></a>Afrunding efter = Momskoder og beregningsmetode = Total

| Linjenummer | Linjenettobeløb | Bestemte momskoder | Momsbeløb før afrunding | Afrundet momsbeløb |
|-------------|-----------------|----------------------|----------------------------|--------------------|
| 1\*         | 11.11           | VAT1                 | 1.111                      | 1.12               |
| 2\*\*       | 22.22           | VAT1; VAT2           | 2,222; 2,222               | 2,23; 2,22         |
| 3\*         | 33.33           | VAT1                 | 3.333                      | 3.33               |
| 4\*\*       | 44.44           | VAT1; VAT2           | 4,444; 4;444               | 4,44; 4,45         |

\* Linje 1, Linje 3 = Afrund\[(11,11 + 33,33) × 10 %\] = 1,12 + 3,33

\*\* Linje 2, Linje 4 = Afrund\[(22,22 + 44,44) × (10 % + 10 %)\] = 2,23 + 2,22 + 4,44 + 4,45

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
