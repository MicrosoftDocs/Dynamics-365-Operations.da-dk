---
title: Varedisponering med behovsprognoser
description: Dette emne forklarer, hvordan du kan inkludere behovsprognoser under varedisponering med Planlægningsoptimering.
author: ChristianRytt
manager: tfehr
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: cb696c365e02ab3e3b28da19b8b33f1975c142f8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983538"
---
# <a name="master-planning-with-demand-forecasts"></a>Varedisponering med behovsprognoser

[!include [banner](../../includes/banner.md)]

Du kan bruge en behovsprognose sammen med Planlægningsoptimering til at tage højde for forventet efterspørgsel i varedisponeringen. Du kan oprette en behovsprognose manuelt, importere den eller generere den ved hjælp af behovsprognosefunktionen i Microsoft Dynamics 365 Supply Chain Management. Yderligere oplysninger om behovsprognose finder du i [Oversigt over behovsprognose](../introduction-demand-forecasting.md).

> [!NOTE]
> Separat prognoseplanlægning understøttes ikke med Planlægningsoptimering. Den har indstillingen **Aktuel prognoseplan** på siden **Varedisponeringsparametre** ingen effekt, når du bruger Planlægningsoptimering.

## <a name="set-up-a-master-plan-to-include-a-demand-forecast"></a>Oprette en behovsplan, der omfatter en behovsprognose

Hvis du vil konfigurere en behovsplan, så den omfatter en behovsprognose, skal du følge disse trin.

1. Gå til **Varedisponering \> Opsætning \> Planer \> Behovsplaner**.
1. Vælg en eksisterende plan, eller opret en ny plan.
1. I oversigtspanelet **Generelt** skal du indstille følgende felter:

    - **Prognosemodel** – Vælg den prognosemodel, der skal anvendes. Denne model tages i betragtning, når der genereres et forsyningsforslag for den aktuelle behovsplan.
    - **Medtag behovsprognose** – Angiv denne indstilling til *Ja* for at medtage behovsprognosen i den aktuelle behovsplan. Hvis du angiver den til *Nej*, medtages der ikke behovsprognosetransaktioner i behovsplanen.
    - **Metode, der bruges til at reducere prognosekrav** – Vælg den metode, der skal bruges til at reducere prognosekravet. Du kan finde flere oplysninger i afsnittet [Prognosereduktionsnøgler](#reduction-keys) senere i dette emne.

1. I oversigtspanelet **Tidshorisont i dage** kan du angive følgende felter for at angive den periode, som behovsprognosen er inkluderet under:

    - **Hovedplan** – Angiv denne indstilling til *Ja* for at tilsidesætte den hovedplanstidshorisont, der stammer fra de enkelte disponeringsgrupper. Angiv værdien til *Nej* for at bruge værdierne fra de enkelte disponeringsgrupper for den aktuelle behovsplan.
    - **Prognoseperiode** – Hvis du angiver indstillingen **Hovedplan** til *Ja*, skal du angive det antal dage (fra dags dato), som behovsprognosen skal gælde for.

    > [!IMPORTANT]
    > Indstillingen **Hovedplan** understøttes ikke med Planlægningsoptimering.

## <a name="set-up-a-coverage-group-to-include-a-demand-forecast"></a>Oprette en disponeringsgruppe, der omfatter en behovsprognose

Hvis du vil konfigurere en disponeringsgruppe, så den omfatter en behovsprognose, skal du følge disse trin.

1. Gå til **Varedisponering \> Opsætning \> Planer \> Disponeringsgrupper**.
1. Vælg en eksisterende disponeringsgruppe, eller opret en ny gruppe.
1. I oversigtspanelet **Andet** skal du indstille følgende felter:

    - **Hovedplanstidshorisont** – Angiv det antal dage (fra dags dato), som behovsprognosen skal gælde for. Denne værdi kan tilsidesættes ved at bruge indstillingen **Hovedplan** på behovsplanen som beskrevet i det forrige afsnit.
    - **Reduktionsnøgle** – Vælg den reduktionsnøgle, der skal anvendes. Du kan finde flere oplysninger i sektionen [Oprette og konfigurere en prognosereduktionsnøgle](#create-reduction-key) og [Bruge en reduktionsnøgle](#use-reduction-key) senere i dette emne.
    - **Reducer prognose med** – For behovsplaner, hvor feltet **Metode, der er brugt til at reducere prognosebehovet** er angivet til *Transaktioner – reduktionsnøgle* eller *Transaktioner – dynamisk periode*, skal du angive, hvilke transaktioner der skal reducere prognoses. Vælg en af følgende værdier:

        - **Alle transaktioner** – Alle transaktioner skal reducere prognosen.
        - **Ordrer** – Det er kun salgsordrer, der skal reducere prognosen.

        > [!NOTE]
        > Hvis du vælger *Alle transaktioner*, betragtes de transaktioner, der har både udbud og efterspørgsel i samme lagerdimensioner, som neutrale, og de ignoreres under prognosereduktionen. Hvis planlægningsdimensionen f.eks. kun er angivet til lokation, ikke lagersted, vil en overflytningsordre mellem lokation 1, lagersted 11 og lokation 1, lagersted 13 blive ignoreret og vil ikke reducere den resterende behovsprognose.

    - **Medtag interne ordrer** – Angiv denne indstilling til *Ja*, hvis der skal inkluderes interne ordrer, når prognosen reduceres. Ellers skal du angive den til *Nej*.
    - **Medtag debitorprognose i behovsprognosen** – Angiv, om en debitorprognose skal medtages i den overordnede prognose. Denne indstilling bestemmer, hvordan faktisk efterspørgsel reducerer den estimerede efterspørgsel. Du kan bruge denne indstilling til at sikre, at varedisponering dækker levering af varer, der købes af specifikke kunder.

        - Angiv denne indstilling til *Ja* for at medtage en kundeprognose i den overordnede prognose. I dette tilfælde reducerer det faktiske kundebehov både debitorprognosen og den overordnede prognose. Varedisponering genererer kun ordreforslag til dækning af den overordnede prognosemængde.
        - Angiv denne indstilling til *Nej* for ikke at medtage en kundeprognose i den overordnede prognose. I dette tilfælde reducerer det faktiske kundebehov kun debitorprognosen. Behovsplanlægning genererer ordreforslag til dækning af både den samlede budgetmængde og prognosen for hver debitormængde.

## <a name="forecast-reduction-keys"></a><a name="reduction-keys"></a>Prognosereduktionsnøgler

Denne sektion indeholder oplysninger om de forskellige metoder, der anvendes til at reducere prognosekrav. Det omfatter eksempler på de enkelte metoders resultater. Det beskriver endvidere, hvor du opretter, konfigurerer og anvender en prognosereduktionsnøgle. Visse metoder anvender en prognosereduktionsnøgle til at reducere prognosekrav.

### <a name="methods-that-are-used-to-reduce-forecast-requirements"></a>Metoder, der anvendes til at reducere prognosekrav.

Når du inkluderer en prognose i en masterplan, kan du vælge, hvordan prognosekravene skal reduceres, når den faktiske efterspørgsel inddrages. Bemærk, at varedisponering udelukker prognosebehovet fra fortiden, hvilket betyder alle prognosebehov før dags dato.

For at inkludere en prognose i en masterplan og vælge den metode, der skal anvendes til at reducere prognosekravene, skal du gå til **Varedisponering \> Opsætning \> Planer \> Masterplaner**. Vælg en prognosemodel i feltet **Prognosemodel**. I feltet **Metode, der anvendes til at reducere prognosekrav** skal du vælge en metode. Der findes følgende indstillinger:

- None
- Procent – reduktionsnøgle
- Transaktioner – reduktionsnøgle (endnu ikke understøttet med Planlægningsoptimering)
- Transaktioner – dynamisk periode

I de følgende afsnit finder du flere oplysninger om hver indstilling.

#### <a name="none"></a>Ingen

Hvis du vælger **Ingen**, reduceres prognosekravene ikke i forbindelse med behovsplanlægningen. I dette tilfælde opretter varedisponeringen de planlagte ordrer for at opfylde det forventede behov (prognosekrav). Disse planlagte ordrer indeholder det foreslåede antal uafhængigt af andre behovstyper. Hvis der eksempelvis indløber salgsordrer, opretter varedisponeringen yderligere planlagte ordrer for at opfylde salgsordrene. Antallet af prognosekrav reduceres ikke.

#### <a name="percent--reduction-key"></a>Procent – reduktionsnøgle

Hvis du vælger **Procent - reduktionsnøgle** reduceres prognosekravene i henhold til de procentandele og perioder, som er defineret af reduktionsnøglen. I dette fælde opretter varedisponeringen de planlagte ordrer, såfremt antallet beregnes i henhold til forventet antal × reduktionsnøgle for hver periode. Hvis der er andre behovstyper, opretter varedisponeringen ligeledes planlagte ordrer for at opfylde disse.

##### <a name="example-percent--reduction-key"></a>Eksempel: procent – reduktionsnøgle

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

#### <a name="transactions--reduction-key"></a>Transaktioner – reduktionsnøgle

Hvis du vælger **Transaktioner - reduktionsnøgle** reduceres prognosekravene af de transaktioner, som finder sted i løbet af de perioder, der er defineret af reduktionsnøglen.

##### <a name="example-transactions--reduction-key"></a>Eksempel: transaktioner – reduktionsnøgle

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

#### <a name="transactions--dynamic-period"></a>Transaktioner – dynamisk periode

Hvis du vælger **Transaktioner - dynamisk periode**, reduceres prognosekravene med de faktiske ordretransaktioner, der finder sted i løbet af den dynamiske periode. Den dynamiske periode dækker de aktuelle budgetdatoer og slutter ved starten af det næste budget. I dette tilfælde opretter varedisponeringen de planlagte ordrer for at opfylde det forventede behov (prognosekrav). Når de faktiske ordretransaktioner indløber, reduceres prognosekravene dog. De faktiske transaktioner forbruger dele af prognosekravene.

Når denne indstilling bruges, forekommer følgende funktionsmåde:

- Der stilles ikke krav om reduktionsnøgler, og de finder ej heller anvendelse. 
- Hvis prognosen reduceres helt, bliver prognosekravene for den aktuelle prognose 0 (nul).
- Hvis der ikke er noget fremtidigt budget, bliver budgetbehovet fra det sidst angivne budget reduceret.
- Tidshorisonter medtages i beregningen af budgetreduktionen.
- Positive dage medtages i beregningen af budgetreduktionen.
- Hvis de faktiske ordreposteringer overstiger budgetbehovet, overføres de resterende posteringer ikke til den næste budgetperiode.

##### <a name="example-1-transactions--dynamic-period"></a>Eksempel 1: transaktioner – dynamisk periode

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

##### <a name="example-2-transactions--dynamic-period"></a>Eksempel 2: transaktioner – dynamisk periode

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

### <a name="create-and-set-up-a-forecast-reduction-key"></a><a name="create-reduction-key"></a>Opret og konfigurer en prognosereduktionsnøgle

En prognosereduktionsnøgle anvendes af metoderne **Transaktioner - reduktionsnøgle** og **Procent - reduktionsnøgle** til at reducere prognosekrav. Følg følgende fremgangsmåde for at oprette og konfigurere en reduktionsnøgle:

1. Gå til **Varedisponering \> Opsætning \> Dækning \> Reduktionsnøgler**.
2. Vælg **Ny** eller tryk på **Ctrl+N** for at oprette en reduktionsnøgle.
3. I feltet **Reduktionsnøgle** indtastes en unik identifikator for prognosereduktionsnøglen. Dernæst indtastes et navn i feltet **Navn**. 
4. Fastsæt perioderne og reduktionsnøgleprocenterne for hver periode:

    - Feltet **Ikrafttrædelsesdato** angiver datoen for, hvornår periodens start blev oprettet. Når indstillingen **Anvend ikrafttrædelsesdatoen** er angivet til **Ja**, starter perioderne på den pågældende dato. Når indstillingen er angivet til **Nej**, starter perioderne, når varedisponeringen køres.
    - Angiv de perioder, hvor prognosereduktionen skal finde sted.
    - Angiv for en bestemt periode de procentandel, som prognosekravene bør reduceres med. Du kan angive positive værdier for at reducere behovet eller negative værdier for at øge behovet.

### <a name="use-a-reduction-key"></a><a name="use-reduction-key"></a>Anvend en reduktionsnøgle

Der skal tildeles en prognosereduktionsnøgle til elementets dækningsgruppe. Følg disse trin for at tildele en reduktionsnøgle til et elements dækningsgruppe.

1. Gå til **Varedisponering \> Opsætning \> Dækning \> Dækningsgrupper**.
2. I feltet **Reduktionsnøgle** i oversigtspanelet **Andre** vælges den reduktionsnøgle, der skal tildeles dækningsgruppen. Reduktionsnøglen gælder derefter for alle elementer, der tilhører den pågældende dækningsgruppe.
3. Hvis du vil bruge en reduktionsnøgle til at beregne prognosereduktionen i løbet af behovsplanlægningen, skal du definere denne indstilling under opsætningen af prognoseplanen eller masterplanen. Gå til en af følgende placeringer:

    - Varedisponering \> Opsætning \> Planer \> Prognoseplaner
    - Varedisponering \> Opsætning \> Planer \> Masterplaner

4. I feltet **Metode, der anvendes til at reducere prognosekrav** i oversigtspanelet **Generelt** på siden **Prognoseplaner** eller **Varedisponering** vælges enten **Procent - reduktionsnøgle** eller **Transaktioner - reduktionsnøgle**.

### <a name="reduce-a-forecast-by-transactions"></a>Reducer en prognose med transaktioner

Når du vælger **Transaktioner - reduktionsnøgle** eller **Transaktioner - dynamisk periode** som en metode til at reducere prognosekrav, kan du præcisere de transaktioner, der skal reducere prognosen. I feltet **Reducer prognose med** i oversigtspanelet **Andre** på siden **Disponeringsgrupper** skal du vælge **Alle transaktioner**, hvis alle transaktioner skal reducere prognosen, eller **Ordrer**, hvis alene salgsordrer skal reducere prognosen.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]