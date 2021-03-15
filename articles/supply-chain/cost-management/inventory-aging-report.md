---
title: Eksempler og logik til rapport over aldersfordelt lager
description: I dette emne vises nogle eksempler på, hvordan resultaterne af en rapport over aldersfordelt lager fortolkes.
author: RichardLuan
manager: tfehr
ms.date: 5/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-5-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: b3822cf4c26d7ef9cd0d062d57fa909140d7e258
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983919"
---
# <a name="inventory-aging-report-examples-and-logic"></a>Eksempler og logik til rapport over aldersfordelt lager

[!include [banner](../includes/banner.md)]

I dette emne vises nogle eksempler på, hvordan resultaterne af rapporten **Aldersfordelt lager** fortolkes. Denne rapport kategoriserer det disponible antal og lagerværdier for en valgt vare eller varegruppe i flere perioder. I dette emne vises også rapportens interne logik.

Eksemplerne i dette emne viser resultater, der præsenteres i en rapport over standard **Aldersfordelt lager**. Generelt anbefales det dog, at du bruger [Lagerrapport over aldersfordelt lager](inventory-aging-report-storage.md)-versionen af denne rapport, specielt hvis du har mange varer og lagersteder, der skal behandles. Lagerrapport over aldersfordelt lager gemmer alle de rapporter, du genererer, viser resultaterne som en interaktiv side og et diagram og giver dig mulighed for at eksportere gemte rapporter.

## <a name="sample-data-that-is-used-in-these-examples"></a>Eksempeldata, der bruges i disse eksempler

Eksemplerne i dette emne er baseret på de eksempeldata fra lagertransaktioner, der er beskrevet i dette afsnit.

### <a name="storage-dimension-setup"></a>Konfiguration af lagringsdimension

Systemeksemplet indeholder følgende opsætning af lagringsdimensioner.

| Navn      | Aktivt | Fysisk lager | Økonomisk lager |
|-----------|--------|--------------------|---------------------|
| Lokation      | Ja    | Ja                | Ja                 |
| Lagersted | Ja    | Ja                | Ingen                  |

### <a name="inventory-model"></a>Lagermodel

I forbindelse med eksempelsystemet er lagermodellen for de frigivne produkter *FIFO* og **Kostpris**-indstillingen for lagermodellen er *Medtag fysisk værdi*.

### <a name="inventory-transactions"></a>Lagerbevægelser

Eksempelsystemet indeholder følgende lagertransaktioner for et frigivet produkt, der har varenummeret *1000*.

| Reference      | Lokation | Lagersted | Tilgang   | Udsted | Fysisk dato | Økonomisk dato | Kvantitet | Kostbeløb | Fysisk kostbeløb |
|----------------|------|-----------|-----------|-------|---------------|----------------|----------|-------------|----------------------|
| Indkøbsordre | 1    | 11        | Købt |       | 15. marts      | 15. marts       | 10       | 1.000       | 1.000                |
| Indkøbsordre | 2    | 21        | Købt |       | 15. marts      | 15. marts       | 10       | 2,000       | 2,000                |
| Indkøbsordre | 1    | 11        | Modtaget  |       | 15. april      |                | 5        |             | 375                  |
| Overførselsordre | 1    | 11        |           | Solgt  | Maj 2         | Maj 2          | -5       | -458,33     | -458,33              |
| Overførselsordre | 1    | 12        | Købt |       | Maj 2         | Maj 2          | 5        | 458.33      | 458.33               |
| Salgsordre    | 1    | 12        |           | Solgt  | Maj 3         | Maj 3          | -1       | -91,67      | -91,67               |

## <a name="how-quantities-and-amounts-in-each-period-bucket-are-calculated"></a>Hvordan antal og beløb i hver periodes filsæt beregnes

Ved hjælp af de eksempeldata, der er beskrevet i de forrige afsnit, kan du køre en **Aldersfordelt lager**-rapport, der har følgende indstillinger:

- **Pr. dato:** *9. maj 2020*
- **Lokation:** *Vis*
- **Lagersted:** *Nr.*
- **Varenummer:** *Total*
- **Forældelsesperiode:** Angiv dette felt, hvis du vil generere månedlige filsæt.

I dette tilfælde ligner indholdet af den rapport, der genereres, følgende eksempel.

<table>
<thead>
<tr>
    <th rowspan="2">varenummer</th>
    <th rowspan="2">Lokation</th>
    <th rowspan="2">Beholdningsantal</th>
    <th rowspan="2">Beholdningsværdi</th>
    <th rowspan="2">Lagerværdimængde</th>
    <th rowspan="2">Lagerværdi</th>
    <th rowspan="2">Gennemsnitlig enhedskostpris</th>
    <th colspan="2">5/8/2020 - 5/1/2020</th>
    <th colspan="2">4/30/2020 - 4/1/2020</th>
    <th colspan="2">3/31/2020 - 3/1/2020</th>
</tr>
<tr>
    <th>P1:antal</th>
    <th>P1:beløb</th>
    <th>P2:antal</th>
    <th>P2:beløb</th>
    <th>P3:antal</th>
    <th>P3:beløb</th>
</tr>
</thead>
<tbody>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>14</td>
    <td>1,283.33</td>
    <td>14</td>
    <td>1,283.33</td>
    <td>91.67</td>
    <td></td>
    <td></td>
    <td>5.00</td>
    <td>458.33</td>
    <td>9.00</td>
    <td>825.00</td>
</tr>
<tr>
    <td>1000</td>
    <td>2</td>
    <td>10</td>
    <td>2,000.00</td>
    <td>10</td>
    <td>2,000.00</td>
    <td>200.00</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td>10.00</td>
    <td>2,000.00</td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><strong>1000 totaler</strong></td>
    <td></td>
    <td><strong>24.00</strong></td>
    <td><strong>3,283.33</strong></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><strong>5.00</strong></td>
    <td><strong>458.33</strong></td>
    <td><strong>19</strong></td>
    <td><strong>2,825.00</strong></td>
</tr>
</tfoot>
</table>

Bemærk følgende oplysninger i følgende eksempelrapport:

- De værdier af **Lagerværdiantal**, **Lagerværdi** og **Gennemsnitlig enhedskostpris**, der vises i rapporten, er værdier for den økonomiske lagerdimension (**Lokation** i dette tilfælde).

    I rapporten for lokation 1 vises f.eks. følgende oplysninger:

    - Værdien af **Lagerværdiantal** er *14* (= 10 + 5 – 5 + 5 – 1).
    - Værdien af **Lagerværdi** er *1.283,33* (= 1.000 + 375 – 458,33 + 458,33 – 91,67).
    - Værdien af **Gennemsnitlig enhedskostpris** er *91,67*.
    - Værdien af **Disponibel værdi** og **Beløb**-værdien i hver periodes filsæt beregnes ved hjælp af **Gennemsnitlig enhedskostpris**-værdien.

- Rapporten bestemmer det disponible antal for hvert periodefilsæt ved at opsummere det samlede modtagne lagerantal for hvert periodefilsæt. Derefter anvendes FIFO-princippet (First In – First Out) til at fratrække det samlede afgåede antal, uanset hvilken lagermodel varerne bruges til.

Hvis du kører den samme rapport igen, men denne gang angiver både feltet **Lokation** og **Lagersted** til *Vis*, minder den nye rapport om følgende eksempel.

<table>
<thead>
<tr>
    <th rowspan="2">varenummer</th>
    <th rowspan="2">Lokation</th>
    <th rowspan="2">Lagersted</th>
    <th rowspan="2">Beholdningsantal</th>
    <th rowspan="2">Beholdningsværdi</th>
    <th rowspan="2">Lagerværdimængde</th>
    <th rowspan="2">Lagerværdi</th>
    <th rowspan="2">Gennemsnitlig enhedskostpris</th>
    <th colspan="2">5/8/2020 - 5/1/2020</th>
    <th colspan="2">4/30/2020 - 4/1/2020</th>
    <th colspan="2">3/31/2020 - 3/1/2020</th>
</tr>
<tr>
    <th>P1:antal</th>
    <th>P1:beløb</th>
    <th>P2:antal</th>
    <th>P2:beløb</th>
    <th>P3:antal</th>
    <th>P3:beløb</th>
</tr>
</thead>
<tbody>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>11</td>
    <td>10</td>
    <td>916.67</td>
    <td>14</td>
    <td>1,283.33</td>
    <td>91.67</td>
    <td></td>
    <td></td>
    <td>5.00</td>
    <td>458.33</td>
    <td>5.00</td>
    <td>458.33</td>
</tr>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>12</td>
    <td>4</td>
    <td>366.67</td>
    <td>14</td>
    <td>1,283.33</td>
    <td>91.67</td>
    <td>4.00</td>
    <td>366.67</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td>1000</td>
    <td>2</td>
    <td></td>
    <td>10</td>
    <td>2,000.00</td>
    <td>10</td>
    <td>2,000.00</td>
    <td>200.00</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td>10.00</td>
    <td>2,000.00</td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><strong>1000 totaler</strong></td>
    <td></td>
    <td></td>
    <td><strong>24.00</strong></td>
    <td><strong>3,283.33</strong></td>
    <td></td>
    <td></td>
    <td></td>
    <td><strong>4.00</strong></td>
    <td><strong>366.67</strong></td>
    <td><strong>5.00</strong></td>
    <td><strong>458.33</strong></td>
    <td><strong>15</strong></td>
    <td><strong>2,458.33</strong></td>
</tr>
</tfoot>
</table>

Denne gang er lokation 1 opdelt i to rækker, én for lagersted 11 og én til lagersted 12. Men værdierne af **Lagerværdiantal**, **Lagerværdi** og **Gennemsnitlig enhedskostpris** er de samme, fordi **Lagersted** ikke er en økonomisk lagerdimension.

Bemærk desuden, at antalsfordelingen på lokation 1 er anderledes. I den første rapport, du har kørt, ignorerede systemet den flytteordre, der fandt sted på samme lokation, og trak antallet i salgsfakturaen fra perioden **3/31/2020-3/1/2020** på lokation 1. Men i den nye rapport trækker systemet antallet i salgsfakturaen fra perioden **5/8/2020 - 5/1/2020** på lagersted 12.

## <a name="effects-of-inventory-closing"></a>Virkning af lagerlukning

Hvis du kører lagerlukning for maj og derefter kører den forrige rapport igen, men angiver feltet **Pr. dato** til *31. maj 2020*, vil du bemærke følgende resultater:

- Værdierne af **Lagerværdi** og **Gennemsnitlig enhedskostpris** opdateres.
- Værdien af **Disponibel værdi** og alle **Beløb**-værdier i alle perioder opdateres tilsvarende.

Rapporten ser nu ud som i følgende eksempel:

<table>
<thead>
<tr>
    <th rowspan="2">varenummer</th>
    <th rowspan="2">Lokation</th>
    <th rowspan="2">Lagersted</th>
    <th rowspan="2">Beholdningsantal</th>
    <th rowspan="2">Beholdningsværdi</th>
    <th rowspan="2">Lagerværdimængde</th>
    <th rowspan="2">Lagerværdi</th>
    <th rowspan="2">Gennemsnitlig enhedskostpris</th>
    <th colspan="2">5/31/2020 - 5/1/2020</th>
    <th colspan="2">4/30/2020 - 4/1/2020</th>
    <th colspan="2">3/31/2020 - 3/1/2020</th>
</tr>
<tr>
    <th>P1:antal</th>
    <th>P1:beløb</th>
    <th>P2:antal</th>
    <th>P2:beløb</th>
    <th>P3:antal</th>
    <th>P3:beløb</th>
</tr>
</thead>
<tbody>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>11</td>
    <td>10</td>
    <td>910.70</td>
    <td>14</td>
    <td>1,275.00</td>
    <td>91.07</td>
    <td>0,00</td>
    <td></td>
    <td>5.00</td>
    <td>455.36</td>
    <td>5.00</td>
    <td>455.36</td>
</tr>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>12</td>
    <td>4</td>
    <td>364.29</td>
    <td>14</td>
    <td>1,275.00</td>
    <td>91.07</td>
    <td>4.00</td>
    <td>364.29</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td>1000</td>
    <td>2</td>
    <td></td>
    <td>10</td>
    <td>2,000.00</td>
    <td>10</td>
    <td>2,000.00</td>
    <td>200.00</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td>10.00</td>
    <td>2,000.00</td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><strong>1000 totaler</strong></td>
    <td></td>
    <td></td>
    <td><strong>24.00</strong></td>
    <td><strong>3,275.00</strong></td>
    <td></td>
    <td></td>
    <td></td>
    <td><strong>4.00</strong></td>
    <td><strong>364.29</strong></td>
    <td><strong>5.00</strong></td>
    <td><strong>455.36</strong></td>
    <td><strong>15</strong></td>
    <td><strong>2,455.36</strong></td>
</tr>
</tfoot>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]