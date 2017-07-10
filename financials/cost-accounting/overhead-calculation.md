---
title: Beregning af fast omkostning
description: I dette emne beskrives de typiske processer til beregning og tildeling af faste omkostninger.
author: YuyuScheller
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: c040a50d9962d7a900fbef285ea1f1baea124033
ms.contentlocale: da-dk
ms.lasthandoff: 06/13/2017


---

# <a name="overhead-calculation"></a>Beregning af fast omkostning

[!include[banner](../includes/banner.md)]


I dette emne beskrives de typiske processer til beregning og tildeling af faste omkostninger.

<a name="term-definition"></a>Definition af begrebet
---------------

Faste omkostninger er de omkostninger, der er forbundet med at drive et firma, men som ikke direkte kan henføres til nogen specifikke aktiviteter, produkter eller tjenester. Faste omkostninger giver vigtig understøttelse til generering af aktiviteter, der kan skabe fortjeneste. Følgende er eksempler på faste omkostninger:

-   Leje
-   Elektricitet
-   Administrative lønninger

## <a name="overhead-calculation-overview"></a>Oversigt over beregning af fast omkostning
Beregning af faste omkostninger kører politikker for omkostningsregnskab i den rigtige rækkefølge. Hvis politikker for omkostningsregnskab er blevet ændret, eller der er fundet specifikke fejl, kan du køre beregning af faste omkostninger flere gange for den samme regnskabsperiode. De enkelte kørsler af beregningen af faste omkostninger gemmes og modtager et entydigt versions-ID, som du kan bruge til at sammenligne beregningerne i forskellige versioner. De omkostningsposter, der genereres af beregningen af faste omkostninger, modtager en regnskabsdatoen. Denne regnskabsdato svarer til slutdatoen for den regnskabsperiode, der bruges i beregningen. Det entydige versions-id består af følgende elementer:

-   Versionstype
-   Dato og klokkeslæt
-   Finanspost for omkostningsregnskab
-   Regnskabsår
-   Regnskabsperiode

Beregning af faste omkostninger køres uafhængigt af versionen. Derfor kan du beregne Budget-versionen før den faktiske version. Beregning af faste omkostninger består af fire trin, som vist i følgende illustration. I hvert trin oprettes der et kladdehoved med poster. Dette kladdehoved indeholder inddataene for hvert trin i beregningen. Politikker og regler anvendes på hver kladdelinje, og der oprettes omkostningsposter som output. Derfor kan dataene altid spores. 
[![Beregning af fast omkostning](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a>Beregne og fordele den faste omkostning for elektricitet
I et finansregnskab registreres nogle omkostninger, f.eks. elektricitet, som et engangsbeløb. Derfor er der ikke angivet detaljeret ledelsesmæssig indsigt for omkostningsregnskab. I omkostningsregnskabet skal omkostningerne gennemløbe de organisatoriske enheder for at give korrekte ledelsesmæssig viden på tværs af alle afdelinger og niveauer. Denne proces skal være baseret på enten en præcis registrering af forbruget eller en rimelig vurdering. En omkostning for elektricitet kan bogføres i finans som vist i følgende tabel.

<table>
<thead>
<tr>
<th>Regnskabsdato</th>
<th colspan="2">Bærer</th>
<th colspan="2">Hovedkonto</th>
<th>Beløb i regnskabsvalutaen</th>
</tr>
</thead>
<tbody>
<tr>
<td>3. januar 2017</td>
<td>CC099</td>
<td>Standardbærer</td>
<td>10001</td>
<td>Elektricitet</td>
<td>10.000,00</td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a>Trin 1: Behandle beregningen af omkostningsfunktionaliteten

Som standard, når omkostningsposter er importeret fra kildedataene, modtager de klassifikationen **Ikke-klassificerede** for funktionalitet af omkostning i omkostningsregnskabet. Ved at anvende politikregler for omkostningsfunktionalitet kan du genklassificeres omkostningsposter som enten **Fast omkostning** eller **Variabel omkostning**.

#### <a name="define-the-cost-behavior-rule"></a>Definere reglen for omkostningsfunktionalitet

I nogle tilfælde er en del af omkostningen et fast gebyr, og de resterende omkostninger er baseret på forbrug. Dette ses ofte på elektricitetsregninger. Når du betaler et bestemt fast gebyr, betaler du for forbrug pr. kilowatttime (kWh). Eksempelvis hvis det faste gebyr er 1.000,00, defineres reglen for omkostningsfunktionalitet sådan:

-   Fast beløb 1.000,00
    -   0 &lt;= 1.000,00 = Fast
    -   1000.01 &lt; N = Variabel

##### <a name="journal"></a>Kladden

<table>
<thead>
<tr>
<th>Kladden</th>
<th>Kladdetype</th>
<th colspan="3">Regnskabskalenderperiode</th>
<th>Version</th>
</tr>
</thead>
<tbody>
<tr>
<td>00001</td>
<td>Beregningskladde for funktionalitet af omkostning</td>
<td>Regnskabsår</td>
<td>2017</td>
<td>1. Periode</td>
<td>Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a>Kladdeposteringer (kladdeposteringer for omkostningsobjektsaldo)

<table>
<thead>
<tr>
<th>Regnskabsdato</th>
<th colspan="2">Omkostningsobjekt</th>
<th colspan="2">Omkostningselement</th>
<th>Funktionalitet af omkostning</th>
<th>Beløb</th>
</tr>
</thead>
<tbody>
<tr>
<td>3. januar 2017</td>
<td>CC099</td>
<td>Standardbærer</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Ikke-klassificerede</td>
<td>10.000,00</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>Omkostningsposter

<table>
<thead>
<tr>
<th colspan="2">Omkostningsobjekt</th>
<th colspan="2">Omkostningselement</th>
<th>Funktionalitet af omkostning</th>
<th>Beløb</th>
<th>Regnskabsdato</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC099</td>
<td>Standardbærer</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Ikke-klassificerede</td>
<td>10.000,00</td>
<td>3. januar 2017</td>
</tr>
<tr>
<td>CC099</td>
<td>Standardbærer</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Ikke-klassificerede</td>
<td>-10.000,00</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC099</td>
<td>Standardbærer</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Fast omkostning</td>
<td>1.000,00</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC099</td>
<td>Standardbærer</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Variabel omkostning</td>
<td>9.000,00</td>
<td>31. januar 2017</td>
</tr>
</tbody>
</table>

Du kan finde detaljerede oplysninger om funktionalitet af omkostninger under Politik for funktionalitet af omkostning. (Bemærk, at dette emne endnu ikke er færdigt, men det kommer snart).

### <a name="step-2-process-the-cost-distribution-calculation"></a>Trin 2: Behandle beregningen af omkostningsfordelingen

Omkostningsfordeling bruges til at omfordele omkostninger fra ét omkostningsobjekt til et eller flere andre omkostningsobjekter ved at anvende en relevant fordelingsgrundlag. Omkostningsfordeling og omkostningstildeling adskiller sig fra hinanden ved, at omkostningsfordeling altid sker på niveauet for det primære omkostningselement i den oprindelige omkostning.

#### <a name="define-the-cost-distribution-rule"></a>Definere reglen for omkostningsdistribution

I et finansregnskab registreres elektricitetsomkostninger ofte som et engangsbeløb. Denne metode ikke er tilstrækkeligt detaljeret i omkostningsregnskab. Den variable omkostning skal fordeles til de enkelte omkostningsobjekter på et rimeligt grundlag. Den mest logiske fordelingsgrundlag er forbruget af elektricitet (kWh). Der oprettes et statistisk dimensionsmedlem, Elektricitet, og forbruget af elektricitet registreres. Som standard bliver alle statistiske dimensionsmedlemmer tilgængelige som fordelingsgrundlag.

<table>
<thead>
<tr>
<th colspan="2">Omkostningsobjekt</th>
<th>KWh</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>Personale</td>
<td>1.000</td>
</tr>
<tr>
<td>CC002</td>
<td>Finans</td>
<td>6.000</td>
</tr>
<tr>
<td>CC003</td>
<td>Samling</td>
<td>0</td>
</tr>
</tbody>
</table>

Tabellen nedenfor viser resultatet, når elforbrug anvendes som en fordelingsgrundlag for variable omkostninger.

<table>
<thead>
<tr>
<th colspan="2">Omkostningsobjekt</th>
<th>Størrelsesorden</th>
<th>Fordelingsfaktor</th>
<th>Beløb</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>Personale</td>
<td>1.000</td>
<td>(1.000 ÷ 7.000) × 9.000,00</td>
<td>1,285.71</td>
</tr>
<tr>
<td>CC002</td>
<td>Finans</td>
<td>6.000</td>
<td>(6.000 ÷ 7.000) × 9.000,00</td>
<td>7,714.29</td>
</tr>
<tr>
<td>CC003</td>
<td>Samling</td>
<td>0</td>
<td>(0 ÷ 7.000) × 9.000,00</td>
<td>0,00</td>
</tr>
</tbody>
</table>

De faste omkostninger skal fordeles jævnt til de enkelte omkostningsobjekter, der har forbrugt elektricitet. Du kan opnå dette resultat ved hjælp af det statistiske dimensionsmedlem for Elektricitet på en formelfordelingsgrundlag: (Elektricitet &gt; 0,00). I følgende tabel vises resultatet, når elforbruget anvendes som fordelingsgrundlag for variable omkostninger.

<table>
<thead>
<tr>
<th colspan="2">Omkostningsobjekt</th>
<th>Formel</th>
<th>Størrelsesorden</th>
<th>Fordelingsfaktor</th>
<th>Beløb</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>Personale</td>
<td>(1,000 &gt; 0,00)</td>
<td>1</td>
<td>(1 ÷ 2) × 1.000,00</td>
<td>500,00</td>
</tr>
<tr>
<td>CC002</td>
<td>Finans</td>
<td>(6.000 &gt; 0,00)</td>
<td>1</td>
<td>(1 ÷ 2) × 1.000,00</td>
<td>500,00</td>
</tr>
<tr>
<td>CC003</td>
<td>Samling</td>
<td>(0 &gt; 0,00)</td>
<td>0</td>
<td>(0 ÷ 2) × 1.000,00</td>
<td>0,00</td>
</tr>
</tbody>
</table>

##### <a name="journal"></a>Kladden

<table>
<thead>
<tr>
<th>Kladden</th>
<th>Kladdetype</th>
<th colspan="3">Regnskabskalenderperiode</th>
<th>Version</th>
</tr>
</thead>
<tbody>
<tr>
<td>00002</td>
<td>Beregningskladde for omkostningsfordeling</td>
<td>Regnskabsår</td>
<td>2017</td>
<td>1. Periode</td>
<td>Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a>Kladdeposteringer (kladdeposteringer for omkostningsobjektsaldo)

<table>
<thead>
<tr>
<th>Regnskabsdato</th>
<th colspan="2">Omkostningsobjekt</th>
<th colspan="2">Omkostningselement</th>
<th>Funktionalitet af omkostning</th>
<th>Beløb</th>
</tr>
</thead>
<tbody>
<tr>
<td>31. januar 2017</td>
<td>CC099</td>
<td>Standardbærer</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Fast omkostning</td>
<td>1.000,00</td>
</tr>
<tr>
<td>31. januar 2017</td>
<td>CC099</td>
<td>Standardbærer</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Variabel omkostning</td>
<td>9.000,00</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>Omkostningsposter

<table>
<thead>
<tr>
<th colspan="2">Omkostningsobjekt</th>
<th colspan="2">Omkostningselement</th>
<th>Funktionalitet af omkostning</th>
<th>Beløb</th>
<th>Regnskabsdato</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC099</td>
<td>Standardbærer</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Fast omkostning</td>
<td>-1.000,00</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC001</td>
<td>Personale</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Fast omkostning</td>
<td>500,00</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Finans</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Fast omkostning</td>
<td>500,00</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC099</td>
<td>Standardbærer</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Variabel omkostning</td>
<td>-9.000,00</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC001</td>
<td>Personale</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Variabel omkostning</td>
<td>1,285.71</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Finans</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Variabel omkostning</td>
<td>7,714.29</td>
<td>31. januar 2017</td>
</tr>
</tbody>
</table>

Du kan finde detaljerede oplysninger om omkostningsfordeling og fordelingsgrundlag under Politik for omkostningsfordeling og Fordelingsgrundlag. (Bemærk, at dette emne endnu ikke er færdigt, men det kommer snart).

### <a name="step-3-process-the-overhead-rate-calculation"></a>Trin 3: Behandle beregning af faste omkostninger

Satsen for faste omkostninger bruges til at lægge gebyr på et eller flere specifikke omkostningsobjekter. Gebyret er baseret på en foruddefineret omkostningssats og størrelsesordenen fra det tildelte fordelingsgrundlag. 

#### <a name="define-the-overhead-rate"></a>Definere satsen for faste omkostninger

Omkostningsobjektet CC001 Personale bidrager til en række interne projekter. Et statistisk dimensionsmedlem med navnet Personaleprojekter oprettes for at måle den anvendte mængde.

<table>
<thead>
<tr>
<th colspan="2">Omkostningsobjekt</th>
<th>Timer</th>
</tr>
</thead>
<tbody>
<tr>
<td>Proj 1</td>
<td>Projekt 1</td>
<td>3</td>
</tr>
<tr>
<td>Proj 2</td>
<td>Projekt 2</td>
<td>1</td>
</tr>
</tbody>
</table>

En foruddefineret omkostningssats for de omkostningsprojektbidrag, der er defineret.

<table>
<thead>
<tr>
<th colspan="2">Omkostningsobjekt</th>
<th>Omkostningselement</th>
<th>Funktionalitet af omkostning</th>
<th>Enheder</th>
<th>Kurs</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>Personale</td>
<td>10001</td>
<td>Variabel omkostning</td>
<td>1</td>
<td>10</td>
</tr>
</tbody>
</table>

Tabellen nedenfor viser resultatet, når personaleprojekterne anvendes som fordelingsgrundlag.

<table>
<thead>
<tr>
<th colspan="2">Omkostningsobjekt</th>
<th>Størrelsesorden</th>
<th>Omkostningselement</th>
<th>Fordelingsfaktor</th>
<th>Beløb</th>
</tr>
</thead>
<tbody>
<tr>
<td>Proj 1</td>
<td>Projekt 1</td>
<td>3</td>
<td>10001</td>
<td>(3 ÷ 1) × 10,00</td>
<td>30,00</td>
</tr>
<tr>
<td>Proj 2</td>
<td>Projekt 2</td>
<td>1</td>
<td>10001</td>
<td>(1 ÷ 1) × 10,00</td>
<td>10,00</td>
</tr>
</tbody>
</table>

##### <a name="journal"></a>Kladden

<table>
<thead>
<tr>
<th>Kladden</th>
<th>Kladdetype</th>
<th colspan="3">Regnskabskalenderperiode</th>
<th>Version</th>
</tr>
</thead>
<tbody>
<tr>
<td>00003</td>
<td>Beregningskladde for satser for faste omkostninger</td>
<td>Regnskabsår</td>
<td>2017</td>
<td>1. Periode</td>
<td>Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a>Kladdeposteringer (kladdeposteringer for beregning af faste omkostninger)

<table>
<thead>
<tr>
<th>Regnskabsdato</th>
<th colspan="2">Omkostningsobjekt</th>
<th>Størrelsesorden</th>
</tr>
</thead>
<tbody>
<tr>
<td>31. januar 2017</td>
<td>Proj 1</td>
<td>Internt proj 1</td>
<td>3,00</td>
</tr>
<tr>
<td>31. januar 2017</td>
<td>Proj 2</td>
<td>Internt proj 2</td>
<td>1,00</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>Omkostningsposter

<table>
<thead>
<tr>
<th colspan="2">Omkostningsobjekt</th>
<th colspan="2">Omkostningselement</th>
<th>Funktionalitet af omkostning</th>
<th>Beløb</th>
<th>Regnskabsdato</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC0001</td>
<td>Personale</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Variabel omkostning</td>
<td>-30,00</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>Proj 1</td>
<td>Internt proj 1</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Variabel omkostning</td>
<td>30,00</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC001</td>
<td>Personale</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Variabel omkostning</td>
<td>-10,00</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>Proj 2</td>
<td>Internt proj 2</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Variabel omkostning</td>
<td>10,00</td>
<td>31. januar 2017</td>
</tr>
</tbody>
</table>

Detaljerede oplysninger om politik for satser for faste omkostninger finder du i Politik for sats for faste omkostninger og Fordelingsgrundlag. (Bemærk, at dette emne endnu ikke er færdigt, men det kommer snart).

### <a name="step-4-process-the-cost-allocation-calculation"></a>Trin 4: Behandle beregningen af omkostningstildelingen

Fordeling bruges til at fordele saldoen for et omkostningsobjekt til andre omkostningsobjekter ved at anvende et fordelingsgrundlag. Finance and Operations understøtter den gensidige fordelingsmetode. I den gensidig fordelingsmetode anerkendes de gensidige tjenester, som ekstra omkostningsobjekter udveksler, fuldt ud. Systemet bestemmer automatisk den rigtige rækkefølge, som tildelingerne skal udføre i. Saldoen for et omkostningsobjekt tildeles af et enkelt fordelingsgrundlag. Tildelinger på tværs af omkostningsobjektdimensioner og deres respektive medlemmer understøttes. Fordelingsrækkefølgen styres af omkostningskontrolenheden. [![Reciprok metode](./media/reciprocal-method.png)]

#### <a name="define-the-cost-allocation"></a>Definere omkostningstildelingen

Her er et enkelt eksempel, der forklarer, hvordan du kan spore strømmen af omkostninger. Omkostningsobjektet CC001 personale bidrager til flere omkostningsobjekter. Et statistisk dimensionsmedlem med navnet Personale-tjenester oprettes for at måle den anvendte mængde.

<table>
<thead>
<tr>
<th colspan="2">Omkostningsobjekt</th>
<th>Personale-tjenester</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC002</td>
<td>Finans</td>
<td>35</td>
</tr>
<tr>
<td>CC003</td>
<td>Samling</td>
<td>55</td>
</tr>
<tr>
<td>CC004</td>
<td>Emballage</td>
<td>10</td>
</tr>
</tbody>
</table>

Omkostningsobjektet CC002 Finans bidrager til flere omkostningsobjekter. Et statistisk dimensionsmedlem med navnet Finans-tjenester oprettes for at måle den anvendte mængde.

<table>
<thead>
<tr>
<th colspan="2">Omkostningsobjekt</th>
<th>Finans-tjenester</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC003</td>
<td>Samling</td>
<td>65</td>
</tr>
<tr>
<td>CC004</td>
<td>Emballage</td>
<td>35</td>
</tr>
</tbody>
</table>

Omkostningsobjektet CC003 Assembly bidrager til flere omkostningsobjekter. Et statistisk dimensionsmedlem med navnet Assembly oprettes for at måle den anvendte mængde.

<table>
<thead>
<tr>
<th colspan="2">Omkostningsobjekt</th>
<th>Assembly-tjenester (timer)</th>
</tr>
</thead>
<tbody>
<tr>
<td>Prod 1</td>
<td>Produkt 1</td>
<td>60</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Produkt 2</td>
<td>20</td>
</tr>
</tbody>
</table>

Omkostningsobjektet CC004 Emballage bidrager til flere omkostningsobjekter. Et statistisk dimensionsmedlem med navnet Emballage oprettes for at måle den anvendte mængde.

<table>
<thead>
<tr>
<th colspan="2">Omkostningsobjekt</th>
<th>Emballage-tjenester (timer)</th>
</tr>
</thead>
<tbody>
<tr>
<td>Prod 1</td>
<td>Produkt 1</td>
<td>80</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Produkt 2</td>
<td>15</td>
</tr>
</tbody>
</table>

**Bemærk!** I Finance and Operations kan statistiske foranstaltninger som f.eks. de produktionstimer, som et produkt forbruger, udledes af kildedataene. Du kan finde mere detaljerede oplysninger om providere af statistiske målinger under Skabeloner til providere af statistiske målinger. (Bemærk, at dette emne ikke er færdigt endnu, men kommer snart). Tabellen nedenfor viser resultatet, når HR tjenester anvendes som tildelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).

<table>
<thead>
<tr>
<th colspan="2">Omkostningsobjekt</th>
<th>Størrelsesorden</th>
<th>Fordelingsfaktor</th>
<th>Beløb</th>
<th>Funktionalitet af omkostning</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC002</td>
<td>Finans</td>
<td>35</td>
<td>(35 ÷ 100) × 500,00</td>
<td>175.00</td>
<td>Fast omkostning</td>
</tr>
<tr>
<td>CC003</td>
<td>Samling</td>
<td>55</td>
<td>(55 ÷ 100) × 500,00</td>
<td>275.00</td>
<td>Fast omkostning</td>
</tr>
<tr>
<td>CC004</td>
<td>Emballage</td>
<td>10</td>
<td>(10 ÷ 100) × 500,00</td>
<td>50,00</td>
<td>Fast omkostning</td>
</tr>
<tr>
<td>CC002</td>
<td>Finans</td>
<td>35</td>
<td>(35 ÷ 100) × 1.245,71</td>
<td>436.00</td>
<td>Variabel omkostning</td>
</tr>
<tr>
<td>CC003</td>
<td>Samling</td>
<td>55</td>
<td>(55 ÷ 100) × 1.245,71</td>
<td>685.14</td>
<td>Variabel omkostning</td>
</tr>
<tr>
<td>CC004</td>
<td>Emballage</td>
<td>10</td>
<td>(10 ÷ 100) × 1.245,71</td>
<td>124.57</td>
<td>Variabel omkostning</td>
</tr>
</tbody>
</table>

Tabellen nedenfor viser resultatet, når Finans-tjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).

<table>
<thead>
<tr>
<th colspan="2">Omkostningsobjekt</th>
<th>Størrelsesorden</th>
<th>Fordelingsfaktor</th>
<th>Beløb</th>
<th>Funktionalitet af omkostning</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC003</td>
<td>Samling</td>
<td>65</td>
<td>(65 ÷ 100) × (500,00 + 175,00)</td>
<td>438.75</td>
<td>Fast omkostning</td>
</tr>
<tr>
<td>CC004</td>
<td>Emballage</td>
<td>35</td>
<td>(35 ÷ 100) × (500,00 + 175,00)</td>
<td>236.25</td>
<td>Fast omkostning</td>
</tr>
<tr>
<td>CC003</td>
<td>Samling</td>
<td>65</td>
<td>(65 ÷ 100) × (7.714,29 + 436,00)</td>
<td>5,297.69</td>
<td>Variabel omkostning</td>
</tr>
<tr>
<td>CC004</td>
<td>Emballage</td>
<td>35</td>
<td>(35 ÷ 100) × (7.714,29 + 436,00)</td>
<td>2,852.60</td>
<td>Variabel omkostning</td>
</tr>
</tbody>
</table>

Tabellen nedenfor viser resultatet, når Assembly-tjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).

<table>
<thead>
<tr>
<th colspan="2">Omkostningsobjekt</th>
<th>Størrelsesorden</th>
<th>Fordelingsfaktor</th>
<th>Beløb</th>
<th>Funktionalitet af omkostning</th>
</tr>
</thead>
<tbody>
<tr>
<td>Prod 1</td>
<td>Produkt 1</td>
<td>60</td>
<td>(60 ÷ 80) × (275,00 + 438,75)</td>
<td>535.31</td>
<td>Fast omkostning</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Produkt 2</td>
<td>20</td>
<td>(20 ÷ 80) × (275,00 + 438,75)</td>
<td>178.44</td>
<td>Fast omkostning</td>
</tr>
<tr>
<td>Prod 1</td>
<td>Produkt 1</td>
<td>60</td>
<td>(60 ÷ 80) × (5.297,69 + 685,14)</td>
<td>4,487.12</td>
<td>Variabel omkostning</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Produkt 2</td>
<td>20</td>
<td>(20 ÷ 80) × (5.297,69 + 685,14)</td>
<td>1,495.71</td>
<td>Variabel omkostning</td>
</tr>
</tbody>
</table>

Tabellen nedenfor viser resultatet, når Emballage-tjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).

<table>
<thead>
<tr>
<th colspan="2">Omkostningsobjekt</th>
<th>Størrelsesorden</th>
<th>Fordelingsfaktor</th>
<th>Beløb</th>
<th>Funktionalitet af omkostning</th>
</tr>
</thead>
<tbody>
<tr>
<td>Prod 1</td>
<td>Produkt 1</td>
<td>80</td>
<td>(80 ÷ 95) × (50,00 + 236,25)</td>
<td>241.05</td>
<td>Fast omkostning</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Produkt 2</td>
<td>15</td>
<td>(15 ÷ 95) × (50,00 + 236,25)</td>
<td>45.20</td>
<td>Fast omkostning</td>
</tr>
<tr>
<td>Prod 1</td>
<td>Produkt 1</td>
<td>80</td>
<td>(80 ÷ 95) × (2.852,60 + 124,57)</td>
<td>2,507.09</td>
<td>Variabel omkostning</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Produkt 2</td>
<td>15</td>
<td>(15 ÷ 95) × (2.852,60 + 124,57)</td>
<td>470.08</td>
<td>Variabel omkostning</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a>Kladdeposteringer (kladdeposteringer for omkostningsobjektsaldo)

<table>
<thead>
<tr>
<th>Kladden</th>
<th>Kladdetype</th>
<th colspan="3">Regnskabskalenderperiode</th>
<th>Version</th>
</tr>
</thead>
<tbody>
<tr>
<td>00004</td>
<td>Kladde for omkostningsfordeling</td>
<td>Regnskabsår</td>
<td>2017</td>
<td>1. Periode</td>
<td>Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a>kladdelinjer

<table>
<thead>
<tr>
<th>Regnskabsdato</th>
<th colspan="2">Omkostningsobjekt</th>
<th colspan="2">Omkostningselement</th>
<th>Funktionalitet af omkostning</th>
<th>Beløb</th>
</tr>
</thead>
<tbody>
<tr>
<td>31. januar 2017</td>
<td>CC001</td>
<td>Personale</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Fast omkostning</td>
<td>500,00</td>
</tr>
<tr>
<td>31. januar 2017</td>
<td>CC001</td>
<td>Personale</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Variabel omkostning</td>
<td>1,245.71</td>
</tr>
<tr>
<td>31. januar 2017</td>
<td>CC002</td>
<td>Finans</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Fast omkostning</td>
<td>675.00</td>
</tr>
<tr>
<td>31. januar 2017</td>
<td>CC002</td>
<td>Finans</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Variabel omkostning</td>
<td>8,150.29</td>
</tr>
<tr>
<td>31. januar 2017</td>
<td>CC003</td>
<td>Samling</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Fast omkostning</td>
<td>713.75</td>
</tr>
<tr>
<td>31. januar 2017</td>
<td>CC003</td>
<td>Samling</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Variabel omkostning</td>
<td>5,982.83</td>
</tr>
<tr>
<td>31. januar 2017</td>
<td>CC003</td>
<td>Emballage</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Fast omkostning</td>
<td>286.25</td>
</tr>
<tr>
<td>31. januar 2017</td>
<td>CC003</td>
<td>Emballage</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Variabel omkostning</td>
<td>2,977.17</td>
</tr>
<tr>
<td>31. januar 2017</td>
<td>Prod 1</td>
<td>Produkt 1</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Fast omkostning</td>
<td>776.36</td>
</tr>
<tr>
<td>31. januar 2017</td>
<td>Prod 1</td>
<td>Produkt 1</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Variabel omkostning</td>
<td>6,994.21</td>
</tr>
<tr>
<td>31. januar 2017</td>
<td>Prod 2</td>
<td>Produkt 1</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Fast omkostning</td>
<td>223.64</td>
</tr>
<tr>
<td>31. januar 2017</td>
<td>Prod 2</td>
<td>Produkt 1</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Variabel omkostning</td>
<td>1,965.79</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>Omkostningsposter

<table>
<thead>
<tr>
<th colspan="2">Omkostningsobjekt</th>
<th colspan="2">Omkostningselement</th>
<th>Funktionalitet af omkostning</th>
<th>Beløb</th>
<th>Regnskabsdato</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>Personale</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Fast omkostning</td>
<td>-500,00</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Finans</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Fast omkostning</td>
<td>175.00</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Samling</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Fast omkostning</td>
<td>275.00</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC004</td>
<td>Emballage</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Fast omkostning</td>
<td>50,00</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC001</td>
<td>Personale</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Variabel omkostning</td>
<td>-1.245,71</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Finans</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Variabel omkostning</td>
<td>436.00</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Samling</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Variabel omkostning</td>
<td>685.14</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC004</td>
<td>Emballage</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Variabel omkostning</td>
<td>124.57</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Finans</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Fast omkostning</td>
<td>-675,00</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Samling</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Fast omkostning</td>
<td>438.75</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC004</td>
<td>Emballage</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Fast omkostning</td>
<td>236.25</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Finans</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Variabel omkostning</td>
<td>-8.150,29</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Samling</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Variabel omkostning</td>
<td>5,297.69</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC004</td>
<td>Emballage</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Variabel omkostning</td>
<td>2,852.60</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Samling</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Fast omkostning</td>
<td>-713,75</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>Prod 1</td>
<td>Produkt 1</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Fast omkostning</td>
<td>535.31</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Produkt 2</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Fast omkostning</td>
<td>178.44</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Samling</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Variabel omkostning</td>
<td>-5.982,83</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>Prod 1</td>
<td>Produkt 1</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Variabel omkostning</td>
<td>4,487.12</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Produkt 2</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Variabel omkostning</td>
<td>1,495.71</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Samling</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Fast omkostning</td>
<td>-286,25</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>Prod 1</td>
<td>Produkt 1</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Fast omkostning</td>
<td>241.05</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Produkt 2</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Fast omkostning</td>
<td>45.20</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Samling</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Variabel omkostning</td>
<td>-2.977,17</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>Prod 1</td>
<td>Produkt 1</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Variabel omkostning</td>
<td>2,507.09</td>
<td>31. januar 2017</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Produkt 2</td>
<td>10001</td>
<td>Elektricitet</td>
<td>Variabel omkostning</td>
<td>470.08</td>
<td>31. januar 2017</td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a>Konklusion
I Finansregnskab bogføres en omkostning på 10.000,00 for elektricitet til et dummy-bærer-id. Derfor kan bogholdere se, at disse omkostninger skal fordeles. I Omkostningsregnskab passerer omkostningerne på tværs af afdelinger og niveauer, baseret på de politikker og regler, der anvendes. Hver omkostning er knyttet et fordelingsgrundlag, der giver den bedste vurdering af fordelingen af omkostninger.

<table>
<thead>
<tr>
<th colspan="2" rowspan="2">Omkostningselement</th>
<th colspan="9">Omkostningsobjekt</th>
<th rowspan="2">Samlet</th>
</tr>
<tr>
<th>CC099</th>
<th>CC001</th>
<th>CC002</th>
<th>CC003</th>
<th>CC004</th>
<th>Proj 1</th>
<th>Proj 2</th>
<th>Prod 1</th>
<th>Prod 2</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2">10001 Elektricitet</td>
<td style="text-align: right;"><strong>0.00</strong></td>
<td style="text-align: right;"><strong>0.00</strong></td>
<td style="text-align: right;"><strong>0.00</strong></td>
<td style="text-align: right;"><strong>0.00</strong></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><strong>30.00</strong></td>
<td style="text-align: right;"><strong>10.00</strong></td>
<td style="text-align: right;"><strong>7,770.57</strong></td>
<td style="text-align: right;"><strong>2,189.43</strong></td>
<td style="text-align: right;"><strong>10,000.00</strong></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;">Ikke-klassificerede</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;">Fast omkostning</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;">776.36</td>
<td style="text-align: right;">223.64</td>
<td style="text-align: right;"><strong>1,000.00</strong></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;">Variabel omkostning</td>
<td style="text-align: right;">000</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">30,00</td>
<td style="text-align: right;">10,00</td>
<td style="text-align: right;">6,994.21</td>
<td style="text-align: right;">1,965.79</td>
<td style="text-align: right;"><strong>9,000.00</strong></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Dette emne viser, hvordan et primært omkostningselement, 10001 Elektricitet, flyder gennem omkostningsobjekter. Derfor tildeles disse faste omkostninger til det laveste niveau i organisationen. Det vil sige, at omkostningsobjekter på laveste niveau bærer omkostningen. Hvis du har brug for en visuel tilførsel af omkostningen mellem omkostningsobjekter, kan du bruge politikreglerne for omkostningsakkumuleringen til at visualisere strømmen af omkostningerne. Du kan finde flere oplysninger under Politik for omkostningstotaler. (Bemærk, at dette emne endnu ikke er færdigt, men det kommer snart).




