---
title: Prognosereduktionsnøgler
description: Dette emne indeholder eksempler på, hvordan du konfigurerer en reduktionsnøgle. Den indeholder oplysninger om de forskellige indstillinger for reduktionsnøglen og resultaterne af hver. Du kan bruge en reduktionsnøgle til at definere, hvordan du kan reducere budgetbehov.
author: roxanadiaconu
manager: tfehr
ms.date: 04/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqPlanSched, ReqReduceKeyDefaultDataWizard, ReqReduceKey
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19251
ms.assetid: aa9e0dfb-6052-4a2e-9378-89507c02fdf2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1fc2b63bfdec1c663027cb4e551589a705c2164e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424500"
---
# <a name="forecast-reduction-keys"></a>Prognosereduktionsnøgler

[!include [banner](../includes/banner.md)]

Dette emne indeholder oplysninger om de forskellige metoder, der anvendes til at reducere prognosekrav. Det omfatter eksempler på de enkelte metoders resultater. Det beskriver endvidere, hvor du opretter, konfigurerer og anvender en prognosereduktionsnøgle. Visse metoder anvender en prognosereduktionsnøgle til at reducere prognosekrav.

## <a name="methods-that-are-used-to-reduce-forecast-requirements"></a>Metoder, der anvendes til at reducere prognosekrav.

Når du inkluderer en prognose i en masterplan, kan du vælge, hvordan prognosekravene skal reduceres, når den faktiske efterspørgsel inddrages. Bemærk, at varedisponering udelukker prognosebehovet fra fortiden, hvilket betyder alle prognosebehov før dags dato.

For at inkludere en prognose i en masterplan og vælge den metode, der skal anvendes til at reducere prognosekravene, skal du gå til **Varedisponering \> Opsætning \> Planer \> Masterplaner**. Vælg en prognosemodel i feltet **Prognosemodel**. I feltet **Metode, der anvendes til at reducere prognosekrav** skal du vælge en metode. Følgende indstillinger er tilgængelige:

- Ingen
- Procent – reduktionsnøgle
- Transaktioner – reduktionsnøgle
- Transaktioner – dynamisk periode

I de følgende afsnit finder du flere oplysninger om hver indstilling.

### <a name="none"></a>Ingen

Hvis du vælger **Ingen**, reduceres prognosekravene ikke i forbindelse med behovsplanlægningen. I dette tilfælde opretter varedisponeringen de planlagte ordrer for at opfylde det forventede behov (prognosekrav). Disse planlagte ordrer indeholder det foreslåede antal uafhængigt af andre behovstyper. Hvis der eksempelvis indløber salgsordrer, opretter varedisponeringen yderligere planlagte ordrer for at opfylde salgsordrene. Antallet af prognosekrav reduceres ikke.

### <a name="percent--reduction-key"></a>Procent – reduktionsnøgle

Hvis du vælger **Procent - reduktionsnøgle** reduceres prognosekravene i henhold til de procentandele og perioder, som er defineret af reduktionsnøglen. I dette fælde opretter varedisponeringen de planlagte ordrer, såfremt antallet beregnes i henhold til forventet antal × reduktionsnøgle for hver periode. Hvis der er andre behovstyper, opretter varedisponeringen ligeledes planlagte ordrer for at opfylde disse.

#### <a name="example-percent--reduction-key"></a>Eksempel: procent – reduktionsnøgle

Dette eksempel viser, hvordan en reduktionsnøgle reducerer efterspørgselsprognosebehovet i henhold til de procenter og tidsperioder, der er defineret i reduktionsnøglen.

I dette eksempel skal du medtage følgende behovsprognose i en masterplan.

| Måned    | Behovsprognose |
|----------|-----------------|
| Januar  | 1.000           |
| Februar | 1.000           |
| Marts    | 1.000           |
| April    | 1.000           |

På siden **Reduktionsnøgler** skal du konfigurere følgende linjer.

| Forskydning | Enhed  | Procent |
|--------|-------|---------|
| 1      | Måned | 100     |
| 2      | Måned | 75      |
| 3      | Måned | 50      |
| 4      | Måned | 25      |

Du tildeler reduktionsnøglen til varens dækningsgruppe. Dernæst vælger du **Procent - reduktionsnøgle** på siden **Masterplaner** i feltet **Metode, der anvendes til at reducere prognosekrav**.

Hvis du i dette tilfælde kører prognoseplanlægningen den 1. januar, forbruges kravene til behovsprognosen i overensstemmelse med den procentdel, du har konfigureret på siden **Reduktionsnøgler**. Følgende behovsantal overføres til behovsplanen.

| Måned                | Planlagt ordreantal | Udregning    |
|----------------------|------------------------|----------------|
| Januar              | 0                      | = 0 % × 1.000   |
| Februar             | 250                    | = 25 % × 1.000  |
| Marts                | 500                    | = 50 % × 1.000  |
| April                | 750                    | = 75 % × 1.000  |
| Maj-december | 1.000                  | = 100 % × 1.000 |

### <a name="transactions--reduction-key"></a>Transaktioner – reduktionsnøgle

Hvis du vælger **Transaktioner - reduktionsnøgle** reduceres prognosekravene af de transaktioner, som finder sted i løbet af de perioder, der er defineret af reduktionsnøglen.

#### <a name="example-transactions--reduction-key"></a>Eksempel: transaktioner – reduktionsnøgle

Dette eksempel viser, hvordan de faktiske ordrer, der forekommer i de perioder, der er defineret i reduktionsnøglen, reducerer efterspørgselsprognosebehovet.

I dette eksempels skal du vælge **Transaktioner - reduktionsnøgle** i feltet **Metode, der anvendes til at reducere prognosekrav** på siden **Masterplaner**.

Der findes følgende salgsordrer pr. 1. januar.

| Måned    | Antal bestilte enheder |
|----------|--------------------------|
| Januar  | 956                      |
| Februar | 1.176                    |
| Marts    | 451                      |
| April    | 119                      |

Såfremt du anvender den samme behovsprognose på 1.000 enheder pr. måned, som blev benyttet i det forrige eksempel, overføres følgende krævede antal til masterplanen.

| Måned                | Antal krævede enheder |
|----------------------|---------------------------|
| Januar              | 44                        |
| Februar             | 0                         |
| Marts                | 549                       |
| April                | 881                       |
| Maj-december | 1.000                     |

### <a name="transactions--dynamic-period"></a>Transaktioner – dynamisk periode

Hvis du vælger **Transaktioner - dynamisk periode**, reduceres prognosekravene med de faktiske ordretransaktioner, der finder sted i løbet af den dynamiske periode. Den dynamiske periode dækker de aktuelle budgetdatoer og slutter ved starten af det næste budget. I dette tilfælde opretter varedisponeringen de planlagte ordrer for at opfylde det forventede behov (prognosekrav). Når de faktiske ordretransaktioner indløber, reduceres prognosekravene dog. De faktiske transaktioner forbruger dele af prognosekravene.

Når denne indstilling bruges, forekommer følgende funktionsmåde:

- Der stilles ikke krav om reduktionsnøgler, og de finder ej heller anvendelse. 
- Hvis prognosen reduceres helt, bliver prognosekravene for den aktuelle prognose 0 (nul).
- Hvis der ikke er noget fremtidigt budget, bliver budgetbehovet fra det sidst angivne budget reduceret.
- Tidshorisonter medtages i beregningen af budgetreduktionen.
- Positive dage medtages i beregningen af budgetreduktionen.
- Hvis de faktiske ordreposteringer overstiger budgetbehovet, overføres de resterende posteringer ikke til den næste budgetperiode.

#### <a name="example-1-transactions--dynamic-period"></a>Eksempel 1: transaktioner – dynamisk periode

Her er et enkelt eksempel, som viser, hvordan metoden **Transaktioner - dynamisk periode** fungerer.

I dette eksempel skal du medtage følgende behovsprognose i en masterplan.

| Dato       | Behovsprognose |
|------------|-----------------|
| 1. januar  | 1.000           |
| 1. februar | 1.000             |

Du kan ligeledes oprette følgende salgsordrer.

| Dato        | Salgsordremængde |
|-------------|----------------------|
| 15. januar  | 200                  |
| 15. februar | 400                  |

I så fald oprettes følgende planlagte ordrer.

| Dato for behovsprognose | Mængde | Forklaring                           |
|--------------------- |----------|---------------------------------------|
| 1. januar            | 800      | Prognosekrav (=1.000 – 200) |
| 15. januar           | 200      | Krav til salgsordrer             |
| 1. februar           | 600      | Prognosekrav (=1.000 – 400) |
| 15. februar          | 400      | Krav til salgsordrer             |

#### <a name="example-2-transactions--dynamic-period"></a>Eksempel 2: transaktioner – dynamisk periode

I de fleste tilfælde konfigureres systemerne, således at transaktionerne reducerer behovsprognosen i specifikke prognoseperioder: uger, måneder osv. Disse perioder er defineret i reduktionsnøglen. Men tiden mellem to linjer i behovsprognosen kan også *omfatte* en periode.

I dette eksempel skal du oprette en behovsprognose for følgende datoer og antal.

| Dato       | Behovsprognose |
|------------|-----------------|
| 1. januar  | 1.000           |
| 5. januar  | 500             |
| 12. januar | 1.000           |

Bemærk, at der i denne prognose ikke er en tydelig periode mellem prognosedatoerne. Mellem første og anden dato er der et interval på fire dage, og mellem den anden og tredje dato er der et interval på syv dage. Disse intervaller er dynamiske perioder.

Du kan ligeledes oprette følgende salgsordrelinjer.

| Dato                             | Salgsordremængde |
|----------------------------------|----------------------|
| 15. december forrige år | 500                  |
| 3. januar                        | 100                  |
| 10. januar                       | 200                  |

I så fald reduceres prognosen på følgende måde:

- Da den første salgsordre ikke indgår i nogen periode, reducerer den ikke prognoserne.
- Da den anden salgsordre ligger mellem den 1. og 5. januar, vil den reducere prognosen for den 1. januar med 100.
- Da den tredje salgsordre ligger mellem den 5. og 12. januar, vil den reducere prognosen for den 5. januar med 200.

Derfor oprettes følgende planlagte ordrer.

| Dato for behovsprognose             | Mængde | Forklaring                                                         |
|----------------------------------|----------|---------------------------------------------------------------------|
| 15. december forrige år | 500      | Krav til salgsordrer                                            |
| 1. januar                        | 900      | Prognosekrav for perioden 1. til 5. januar (= 1.000 – 100) |
| 3. januar                        | 100      | Krav til salgsordrer                                            |
| 5. januar                        | 300      | Prognosekrav for perioden 5. til 10. januar (= 500 – 200)  |
| 12. januar                       | 1.000    | Prognosekrav for perioden 12. januar til slut                      |

## <a name="create-and-set-up-a-forecast-reduction-key"></a>Opret og konfigurer en prognosereduktionsnøgle

En prognosereduktionsnøgle anvendes af metoderne **Transaktioner - reduktionsnøgle** og **Procent - reduktionsnøgle** til at reducere prognosekrav. Følg følgende fremgangsmåde for at oprette og konfigurere en reduktionsnøgle:

1. Gå til **Varedisponering \> Opsætning \> Dækning \> Reduktionsnøgler**.
2. Vælg **Ny** eller tryk på **Ctrl+N** for at oprette en reduktionsnøgle.
3. I feltet **Reduktionsnøgle** indtastes en unik identifikator for prognosereduktionsnøglen. Dernæst indtastes et navn i feltet **Navn**. 
4. Fastsæt perioderne og reduktionsnøgleprocenterne for hver periode:

    - Feltet **Ikrafttrædelsesdato** angiver datoen for, hvornår periodens start blev oprettet. Når indstillingen **Anvend ikrafttrædelsesdatoen** er angivet til **Ja**, starter perioderne på den pågældende dato. Når indstillingen er angivet til **Nej**, starter perioderne, når varedisponeringen køres.
    - Angiv de perioder, hvor prognosereduktionen skal finde sted.
    - Angiv for en bestemt periode de procentandel, som prognosekravene bør reduceres med. Du kan angive positive værdier for at reducere behovet eller negative værdier for at øge behovet.

## <a name="use-a-reduction-key"></a>Anvend en reduktionsnøgle

Der skal tildeles en prognosereduktionsnøgle til elementets dækningsgruppe. Følg disse trin for at tildele en reduktionsnøgle til et elements dækningsgruppe.

1. Gå til **Varedisponering \> Opsætning \> Dækning \> Dækningsgrupper**.
2. I feltet **Reduktionsnøgle** i oversigtspanelet **Andre** vælges den reduktionsnøgle, der skal tildeles dækningsgruppen. Reduktionsnøglen gælder derefter for alle elementer, der tilhører den pågældende dækningsgruppe.
3. Hvis du vil bruge en reduktionsnøgle til at beregne prognosereduktionen i løbet af behovsplanlægningen, skal du definere denne indstilling under opsætningen af prognoseplanen eller masterplanen. Gå til en af følgende placeringer:

    - Varedisponering \> Opsætning \> Planer \> Prognoseplaner
    - Varedisponering \> Opsætning \> Planer \> Masterplaner

4. I feltet **Metode, der anvendes til at reducere prognosekrav** i oversigtspanelet **Generelt** på siden **Prognoseplaner** eller **Varedisponering** vælges enten **Procent - reduktionsnøgle** eller **Transaktioner - reduktionsnøgle**.

## <a name="reduce-a-forecast-by-transactions"></a>Reducer en prognose med transaktioner

Når du vælger **Transaktioner - reduktionsnøgle** eller **Transaktioner - dynamisk periode** som en metode til at reducere prognosekrav, kan du præcisere de transaktioner, der skal reducere prognosen. I feltet **Reducer prognose med** i oversigtspanelet **Andre** på siden **Disponeringsgrupper** skal du vælge **Alle transaktioner**, hvis alle transaktioner skal reducere prognosen, eller **Ordrer**, hvis alene salgsordrer skal reducere prognosen.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over behovsplaner](master-plans.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]