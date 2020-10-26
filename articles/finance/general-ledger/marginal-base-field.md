---
title: Momssatser baseret på beregningsgrundlaget og beregningsmåderne
description: Dette emne beskriver, hvordan værdierne i felterne Beregningsgrundlag og Beregningsmetode bestemmer momssatserne for salgs- og købstransaktioner.
author: ShylaThompson
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 7171
ms.assetid: 381fc309-b32a-4927-b5b8-fa1c31b0bd72
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8617785ea969f9f4facaccdf81cfaf5344c30839
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2020
ms.locfileid: "3974997"
---
# <a name="sales-tax-rates-based-on-the-marginal-base-and-calculation-methods"></a>Momssatser baseret på beregningsgrundlaget og beregningsmåderne

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan værdierne i felterne Beregningsgrundlag og Beregningsmetode bestemmer momssatserne for salgs- og købstransaktioner.

Beregningsgrundlaget for oversigtspanelet Beregning på siden Momskoder bestemmer, hvilke beløb der bruges til at plukke passende momssatser fra satserne på siden Momskodeværdier. Beløbstype i feltet Beregningsgrundlag i kombination med metoden i feltet Beregning bestemmer logikken, der skal bruges til at finde de korrekte momssatser for en transaktion. 

Forskellige kombinationer af værdier i disse felter resulterer i meget forskellige momsberegninger, som det fremgår af følgende eksempler. I eksemplerne bruges de værdier for momsinterval, der er defineret for hver momskode på siden Momskodeværdier. Du kan åbne denne side ved at klikke på Momskode &gt; Værdier på siden Momskoder.

> [!Important]                                                                                                                  
> Hvis beregningsgrundlaget for en eller flere af dine momskoder er baseret på linjebeløb eller -enheder, skal værdien i feltet Beregningsmåde på siden Finansparametre indstilles til Linje. |

## <a name="net-amount-per-line"></a> Nettobeløb pr. linje
Vælg denne indstilling for at bestemme momssatser baseret på nettobeløbet for fakturalinjerne, ekskl. andre afgifter.

### <a name="example"></a>Eksempel

Momssatserne er defineret i følgende intervaller.

| Beløbsinterval    | Momssats |
|--------------------|----------|
| 0-50             | 30 %      |
| 50-100           | 20 %      |
| 100 - 0 (&gt; 100) | 10 %      |

> [!NOTE]                                                                                                             
> Den øvre grænse på nul (0) i det sidste interval betyder, at alle beløb, der er højere end 100, er medtaget i intervallet.

Beregningsgrundlag: **Nettobeløb pr. linje** 

Beregningsmåde: **Interval** 

Du køber 8 lamper, der hver koster 25,00. 

Nettobeløbet for fakturalinjen er 200,00. 

Momsen beregnes på følgende måde: 

Samlet moms = 50 x 30 % + 50 x 20 % + 100 x 10 % = 15 + 10 + 10 = 35,00 

Samlet fakturabeløb = 200,00 + 35,00 = 235,00 

**Variation** 

Hvis fakturaen har to linjer og fire varer på hver linje, er nettobeløbet på hver linje 100,00, og momsen beregnes på følgende måde: 

Momslinje 1 = 50 x 30 % + 50 x 20 % = 15 + 10 = 25,00 

Momslinje 2 = 50 x 30 % + 50 x 20 % = 15 + 10 = 25,00 

Moms i alt= 25,00 + 25,00 = 50,00 

Samlet fakturabeløb = 200,00 + 50,00 = 250,00

## <a name="net-amount-per-unit"></a> Nettobeløb pr. enhed
Vælg denne indstilling for at bestemme momssatser baseret på værdien af hver enhed, ekskl. andre afgifter. Når et enhedsbaseret beregningsgrundlag vælges, skal også en enhed angives for momskoden.

### <a name="example"></a>Eksempel

Momssatserne er defineret i følgende intervaller.

| Beløb             | Momssats |
|--------------------|----------|
| 0-50             | 30 %      |
| 50-100           | 20 %      |
| 100 - 0 (&gt; 100) | 10 %      |

Beregningsgrundlag: **Nettobeløb pr. enhed** 

Beregningsmåde: **Hele beløbet** 

Du køber 8 lamper, der hver koster 25,00. 

Nettobeløbet for fakturalinjen er 200,00. 

Momsen beregnes på følgende måde: Moms pr. enhed = 25,00 x 30 % = 7,50 Samlet moms = 7,50 x 8 enheder = 60,00 Samlet fakturabeløb = 200,00 + 60,00 = 260,00

## <a name="net-amount-of-invoice-balance"></a> Nettobeløb på fakturasaldo

Vælg denne indstilling for at bestemme momssatser ud fra den samlede værdi af fakturaen, ekskl. andre afgifter.

### <a name="example"></a>Eksempel

Momssatserne er defineret i følgende intervaller.

| Beløb            | Momssats |
|-------------------|----------|
| 0-50            | 30 %      |
| 50-100          | 20 %      |
| 100 -0 (&gt; 100) | 10 %      |

Beregningsgrundlag: **Nettobeløb på fakturasaldo** 

Beregningsmåde: **Interval** En salgsfaktura har 2 linjer med 4 lamper på hver linje til 25,00 pr. stk. Fakturasaldoens nettobeløb er 4 x 25,00 + 4 x 25,00 = 200,00. Momsen beregnes på følgende måde: Samlet moms = 50 x 0,30 + 50 x 0,20 + 100 x 0,10 = 15 + 10 + 10 = 35,00 Samlet fakturabeløb = 200,00 + 35,00 = 235,00

## <a name="gross-amount-per-line"></a> Bruttobeløb pr. linje

Vælg denne indstilling for at bestemme momssatser ud fra værdien af linjen, inkl. alle andre afgifter for linjen.

> [!NOTE]
> I en momsgruppe kan du kun have én momskode med dette valg i feltet Beregningsgrundlag.

### <a name="example"></a>Eksempel

Momssatserne er defineret i følgende intervaller.

| Beløb             | Momssats |
|--------------------|----------|
| 0-50             | 30 %      |
| 50-100           | 20 %      |
| 100 - 0 (&gt; 100) | 10 %      |

Beregningsgrundlag: **Bruttobeløb pr. linje** Beregningsmåde: **Interval** Der er desuden en anden momskode, der beregnes for en særlig afgift på 5,00 på hver lampe. Afgiften lægges til nettobeløbet før momsberegningen. Du køber 8 lamper, der hver koster 25,00. Nettobeløbet for fakturalinjen er 200,00. Bruttobeløbet for fakturalinjen er 8 x 25,00 + 8 x 5,00 = 240,00. Momsen beregnes på følgende måde: Samlet moms = 50 x 0,30 + 50 x 0,20 + 140 x 0,10 = 15 + 20 + 14 = 39,00 Samlet afgift = 5,00 x 8 = 40,00 Samlet fakturabeløb = 200,00 + 39,00 + 40,00 = 279,00

**Variation** 

Hvis fakturaen oprettes ved hjælp af 2 fakturalinjer med 4 varer på hver linje, er nettobeløbet pr. fakturalinje 100. Bruttobeløb (inklusive afgift på 4 x 5,00) pr. fakturalinje er 120,00, og momsen beregnes på følgende måde: Moms for fakturalinje 1 = 50 x 0,30 + 50 x 0,20 + 20 x 0,10 = 15 + 10 + 2 = 27,00 Moms for fakturalinje 2 = 50 x 0,30 + 50 x 0,20 + 20 x 0,10 = 15 + 10 + 2 = 27,00 Samlet moms = 27,00 + 27,00 = 54,00 Samlet afgift = 5,00 x 8 = 40,00 Samlet fakturabeløb = 200,00 + 54,00 + 40,00 = 294,00

## <a name="gross-amount-per-unit"></a> Bruttobeløb pr. enhed

Vælg denne indstilling for at bestemme momssatser baseret på værdien af enheden, inkl. andre afgifter.

> [!NOTE]
> I en momsgruppe kan du kun have én momskode med dette valg i feltet Beregningsgrundlag.

### <a name="example"></a>Eksempel

Momssatserne er defineret i følgende intervaller.

| Beløb             | Momssats |
|--------------------|----------|
| 0-50             | 30 %      |
| 50-100           | 20 %      |
| 100 - 0 (&gt; 100) | 10 %      |

Beregningsgrundlag: **Bruttobeløb pr. enhed** Der er en særlig afgift på 5,00 på hver lampe. Afgiften lægges til nettobeløbet før momsberegningen. Du køber 8 lamper, der hver koster 25,00. Bruttobeløb pr. enhed er 30,00. Momsen beregnes på følgende måde: Moms pr. enhed = 30 x 30 % = 9,00 Samlet moms = 9,00 x 8 = 72,00 Samlet afgift = 5,00 x 8 = 40,00 Samlet fakturabeløb = 200,00 + 72,00 + 40,00 = 312,00

## <a name="invoice-total-incl-other-sales-tax-amounts"></a> Fakturatotal inkl. andre momsbeløb

Vælg denne indstilling for at bestemme momssatser ud fra den samlede værdi af fakturaen, inkl. andre afgifter.
> [!NOTE]
> I en momsgruppe kan du kun have én momskode med dette valg i feltet Beregningsgrundlag

### <a name="example"></a>Eksempel

Momssatserne er defineret i følgende intervaller.

| Beløb             | Momssats |
|--------------------|----------|
| 0-50             | 30 %      |
| 50-100           | 20 %      |
| 100 - 0 (&gt; 100) | 10 %      |

Beregningsgrundlag: **Fakturatotal inkl. andre momsbeløb** Beregningsmåde: **Interval**   
Der er en særlig afgift på hver lampe på 5,00. Afgiften lægges til nettobeløbet før momsberegningen. Du køber 8 lamper, der hver koster 25,00. Nettobeløbet for fakturaen er 200,00. Bruttobeløbet for fakturaen er 200,00 + (8 x 5,00) = 240,00. Momsen beregnes på følgende måde: Samlet moms = 50 x 0,30 + 50 x 0,20 + 140 x 0,10 = 15 + 10 + 14 = 39,00 Samlet afgift = 5,00 x 8 = 40,00 Samlet fakturabeløb = 200,00 + 39,00 + 40,00 = 279,00

Du kan finde flere oplysninger under [Indstillinger for beregning af hele beløbet og intervaller for momskoder](whole-amount-interval-options-sales-tax-codes.md) og [Momsberegningsmetoderne i feltet Grundlag](sales-tax-calculation-methods-origin-field.md)



