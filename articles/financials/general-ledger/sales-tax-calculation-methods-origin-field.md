---
title: Momsberegningsmetoderne i feltet Grundlag
description: I denne artikel beskrives indstillingerne i feltet Grundlag på siden Momskoder, og hvordan momsen beregnes ud fra den valgte indstilling for en momskode.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1473eeb2950296f5ae6250d7a53794af3d9cba81
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "330672"
---
# <a name="sales-tax-calculation-methods-in-the-origin-field"></a>Momsberegningsmetoderne i feltet Grundlag

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

I denne artikel beskrives indstillingerne i feltet Grundlag på siden Momskoder, og hvordan momsen beregnes ud fra den valgte indstilling for en momskode.

For hver momskode, du opretter på siden Momskoder, skal du vælge den beregningsmåde, der skal anvendes for momsgrundlagsbeløbet i feltet Grundlag.

## <a name="percentage-of-net-amount"></a>Procent af nettobeløb
Procentdelen af metoden til beregning af nettobeløb er standardværdien i feltet Grundlag. Momsen beregnes som en procentdel af købs- eller salgsbeløbet eksklusive evt. andre omsætningsafgifter.
### <a name="example"></a>Eksempel

Momssatsen er 25 %. Fakturalinjen viser et antal på 10 varer til en stykpris på 1,00, og kunden får en linjerabat på 10 %. Nettobeløbet: (10 x 1,00) -10 % = 9,00 moms: 9,00 x 25 % = 2,25 samlet beløb: 9,00 + 2,25 = 11,25

## <a name="percentage-of-gross-amount"></a> Procent af bruttobeløb
Hvis du vælger beregningsmetoden Procent af bruttobeløb, beregnes momsen som en procent af bruttosalgsbeløbet. Bruttobeløbet er nettobeløbet for linjen plus alle afgifter og gebyrer for linjen, bortset fra skatten, hvor Grundlag = Procent af bruttobeløb.
### <a name="example"></a>Eksempel

Momsmyndighederne har pålagt en vare specielle afgifter. Afgiftsbeløbene føjes til nettobeløbet, før der beregnes moms. Anvend følgende momskoder:
-   AFGIFT 1 = 10 % ved hjælp af beregningsmetoden Procent af nettobeløb
-   AFGIFT 2 = 20 % ved hjælp af beregningsmetoden Procent af nettobeløb
-   MOMS = 25 % ved hjælp af beregningsmetoden Procent af bruttobeløb

Hvis nettobeløbet er 10,00, er AFGIFT 1 1,00 (10,00 x 10 %) og AFGIFT 2 = 2,00 (10,00 x 20 %). Beløbene vil være som følger: Bruttobeløb: Nettobeløb + AFGIFT 1-beløb + AFGIFT 2-beløb (10,00 + 1,00 + 2,00) = 13,00 MOMS = 13,00 x 25 % = 3,25 samlede AFGIFTER og MOMS: 1,00 + 2,00 + 3,25 = 6,25 samlet beløb: 10,00 + 6,25 = 16,25

| **Bemærk!**                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kun én skattekode til Grundlag = Procentdel af bruttobeløb kan bruges til en transaktion. Hvis der bestemmes mere end én momskode for en transaktion, vises der en fejl om, at der ikke kan beregnes moms. |


<a name="percentage-of-sales-tax"></a>Procent af moms
-----------------------

Når du vælger Procent af moms i feltet Grundlag, beregnes momsen som en procent af den moms, der er valgt i feltet Moms på moms. Den moms, der er valgt i feltet Moms på moms, beregnes først. Den næste moms beregnes derefter på grundlag af det første momsbeløb.
### <a name="example"></a>Eksempel

Anvend følgende momskoder:
-   AFGIFT 1 = 10 % ved hjælp af metoden Procent af nettobeløb
-   AFGIFT 2 = 20 % ved hjælp af metoden Procent af moms med Afgift 1 i feltet Moms på moms
-   MOMS = 25 % ved hjælp af metoden Procent af bruttobeløb

Nettobeløb: 10,00 AFGIFT 1: 10,00 x 10 % = 1,00 AFGIFT 2: 1,00 x 20 % = 0,20 Bruttobeløb: 10,00 + 1,00 + 0,20 = 11,20 MOMS: 11,20 x 25 % = 2,80 Samlet AFGIFT og MOMS: 1,00 + 0,20 + 2,80 = 4,00 Samlet beløb: 10,00 + 4,00 = 14,00

| **Bemærk!**                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Moms på moms-beregninger på flere niveauer er ikke mulig. En moms kan ikke beregnes ud fra en moms, der allerede er beregnet ud fra en anden moms. Flere moms på moms-koder på et enkelt niveau kan beregnes for en transaktion. |

## <a name="amount-per-unit"></a> Beløb pr. enhed
Når du vælger Beløb pr. enhed i feltet Grundlag, beregnes momsen som et fast beløb pr. enhed, multipliceret med det antal, der er angivet på dokumentlinjen. Der skal vælges en enhed i feltet Enhed. Beløb pr. enhed angives på siden Momskodeværdier.
### <a name="example"></a>Eksempel

Momskode er sat op som: kr. 1,20 pr. enhed = kasse på salgsfakturalinje 25 kasser med en vare solgt Moms beregnes som 25 x 1,20 = 30,00

| **Bemærk!**                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Hvis transaktionen angives i en anden enhed end den enhed, der er angivet for momskoden, omregnes den automatisk på grundlag af de enhedsomregninger, der er angivet på siden Enhedsomregninger. |

###  <a name="amount-per-unit-additional-option"></a> Beløb pr. enhed, ekstra indstilling

Under fanen Beregning kan du vælge, om moms for et beløb pr. enhed skal beregnes før andre momskoder og føjes til nettobeløbet før andre momskoder, hvis Grundlag = Procent af nettobeløb beregnes.

### <a name="examples"></a>Eksempler

Antag, at vi beregner 2 momskoder for en transaktion.

-   AFGIFT: Grundlag = beløb pr. enhed og en moms, værdien er angivet til 5,00 pr. enhed = styk
-   MOMS: Grundlag = som vist i eksemplerne nedenfor, er værdien angivet til 25 %

Vi sælger 1 styk af en vare til en enhedspris på 10,00
#### <a name="example-1"></a>Eksempel 1

MOMS: Grundlag = metoden Procent af bruttobeløb. Indstillingen Beregn før moms har ingen virkning, fordi MOMS beregnes som en procentdel af bruttobeløbet. AFGIFT: 1 x 5,00 = 5,00 Bruttobeløb: 10,00 + 5,00 = 15,00 MOMS: 15,00 x 25 % = 3,75 Samlet moms: 5,00 + 3,75 = 8,75 Samlet beløb: 10,00 + 8,75 = 18,75

#### <a name="example-2"></a>Eksempel 2

MOMS: Grundlag = Procent af nettobeløb. Indstillingen Beregn før moms er ikke valgt til beregning af AFGIFT. Nettobeløb: 10,00 AFGIFT: 1 x 5,00 = 5,00 MOMS: 10,00 x 25 % = 2,50 Samlet moms: 5,00 + 2,50 = 7,50 Samlet beløb: 10,00 + 7,50 = 17,50

#### <a name="example-3"></a>Eksempel 3

MOMS: Grundlag = Procent af nettobeløb. Indstillingen Beregn før moms er valgt til beregning af AFGIFT. Nettobeløb: 10,00 AFGIFT: 1 x 5,00 = 5,00 MOMS: (10,00 + 5,00) x 25 % = 3,75 Samlet moms: 5,00 + 3,75 = 8,75 Samlet beløb: 10,00 + 8,75 = 18,75

#### <a name="example-4"></a>Eksempel 4

Resultatet af Eksempel 3 og Eksempel 1 er det samme, da der kun er én afgift. Antag, at du har to AFGIFTER, og kun én af dem er inkluderet i nettobeløbet for beregning af moms: AFGIFT 1: 5,00, ved hjælp af metoden Beløb pr. enhed og indstillingen Beregn før moms valgt AFGIFT 2: 2,50, ved hjælp af metoden Beløb pr. enhed, og indstillingen Beregn før moms er ikke valgt Moms: 25 %, ved hjælp af metoden Procent af nettobeløb Nettobeløb: 10,00 AFGIFT 1: 1 x 5,00 = 5,00 AFGIFT 2: 1 x 2,50 = 2,50 Nettebeløb, der skal beregnes moms af: 10,00 + 5,00 = 15,00 MOMS: 15,00 x 25 % = 3,75 Samlet moms herunder afgifter: 5,00 + 2,50 + 3,75 = 11,25 Samlet beløb: 10,00 + 11,25 = 21,25 MOMSEN på 25 % beregnes for summen af nettobeløb (10,00) + AFGIFT 1 (5,00) = 15,00. AFGIFT 2 føjes til afgiftsbeløbet, når momsen er beregnet.

## <a name="calculated-percentage-of-net-amount"></a> Beregnet procent af nettobeløb
Beregnet procent af nettobeløb håndterer momsberegning forskelligt, afhængigt af indstillingen af parameteren for Beløb inkl. moms for dokumentet eller kladden.
### <a name="example-1"></a>Eksempel 1

Dokument/kladde er angivet til Beløb inkl. moms = Ja Beløb på transaktionslinje: 10,00 Momssats: 25 % Moms: transaktionslinjebeløbet x momssats (10,00 x 25 %) = 2,50 Momsgrundlagsbeløb (oprindelsesbeløb): transaktionslinjebeløbet - moms (10,00 2,50) = 7,50

### <a name="example-2"></a>Eksempel 2

Dokument/kladde er angivet til Beløb inkl. moms = Nej Beløb på transaktionslinje: 10,00 Momssats: 25 % Moms: transaktionslinjebeløbet x momssats / (100 - momssats) (10,00 x 25 %) / (100 % - 25 %) = 3,33 Momsgrundlagsbeløb (oprindelsesbeløb): transaktionslinjebeløbet = 10,00



<a name="additional-resources"></a>Yderligere ressourcer
--------

[Bestemmelse af momssatser baseret på beregningsgrundlaget og felter for beregningsmåde](marginal-base-field.md)

[Indstillinger for beregning af hele beløbet og intervaller for momskoder](whole-amount-interval-options-sales-tax-codes.md)



