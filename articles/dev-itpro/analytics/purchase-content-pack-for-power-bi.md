---
title: "Power BI-indhold til købsforbrugsanalyse"
description: "I dette emne beskrives, hvad der skal medtages i Power BI-indhold til Købsforbrugsanalyse. Det beskrives, hvordan du får adgang til rapporter, der er inkluderet i indholdet, og indeholder oplysninger om den datamodel og de enheder, der bliver brugt til at oprette indholdet."
author: FrankDahl
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 821d8927211d7ac3e479848c7e7bef9f650d4340
ms.openlocfilehash: 069c4dc21959ab603ba6ca3da0ac68ef20325265
ms.contentlocale: da-dk
ms.lasthandoff: 08/13/2018

---

# <a name="purchase-spend-analysis-power-bi-content"></a>Power BI-indhold til købsforbrugsanalyse

[!include [banner](../includes/banner.md)]

I dette emne beskrives, hvad der skal medtages i Microsoft Power BI-indholdet til **Købsforbrugsanalyse**. Det beskrives, hvordan du får adgang til Power BI-rapporter, og der er oplysninger om den datamodel og de enheder, der er brugt til at oprette indholdspakken.

## <a name="overview"></a>Overblik

Power BI-indholdet til **Købsforbrugsanalyse** er udviklet til at hjælpe indkøbschefer og ledere, der er ansvarlige for budgetter, med at holde øje med udgifter til køb. Chefer kan analysere indkøbsudgifter på følgende måder:

- Køb år til dato (efter kreditorgruppe og individuelle kreditorer, indkøbskategori og individuelle produkter og leverandørlokalitet)
- Ændring af køb år for-år (efter leverandørgruppe og indkøbskategori)

Indholdet bruger købstransaktionsdata og indeholder både en samlet oversigt over alle firmaets købstal og en opdeling af købsforbrug pr. leverandør og vare. Rapporter fremhæve ændringer i købsforbruget over tid. Derfor kan rapporterne bruges til at give ledere besked om positive og negative forbrugstendenser for individuelle leverandører og produkter. Desuden viser diagrammer købsforbruget til forskellige indkøbskategorier og kreditorgrupper. Derfor kan kategori- og områdeledere bruge diagrammerne til at identificere ændringer i forbrugsmønsteret.

## <a name="accessing-the-power-bi-content"></a>Adgang til Power BI-indhold
Power BI-indholdet **Købsforbrugsanalyse** vises på siden **Købs- og forbrugsanalyse** (**Indkøb og forsyning** \> **Forespørgsler og rapporter** \> **Performanceanalyse for indkøb** \> **Købs- og forbrugsanalyse**).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Metrikker, der er inkluderet i Power BI-indhold
Power BI-indholdspakken til **Købsforbrugsanalyse** indeholder en rapport, der består af et sæt metrikker. Disse metrikker visualiseres som diagrammer, felter og tabeller. I nedenstående tabel vises en oversigt over visualiseringerne.

<table>
<thead>
<tr>
<th>Rapportside</th>
<th>Diagrammer</th>
<th>Felter</th>
</tr>
</thead>
<tbody>
<tr>
<td>Indkøb efter leverandør</td>
<td><ul>
<li>Top 10 leverandører efter indkøb (stablet liggende søjlediagram)</li>
<li>Samlet indkøb pr. leverandørgruppe/land/navn (cirkeldiagram)</li>
<li>Indkøb pr. leverandørgruppe/land/navn (søjlediagram)</li>
<li>Gennemsnitsindkøb pr. leverandørgruppe/land/navn (søjlediagram)</li>
</ul></td>
<td><ul>
<li>Indkøb i alt</li>
<li>Indkøbsvækst år for år</li>
<li>Antal leverandører i alt</li>
<li>Antal aktive leverandører i alt</li>
</ul></td>
</tr>
<tr>
<td>Køb pr. produkt</td>
<td><ul>
<li>Køb efter indkøbskategori/produktnavn (søjlediagram)</li>
<li>Indkøb i alt efter indkøbskategori/produktnavn (cirkeldiagram)</li>
<li>Top 10 produkter efter indkøb (stablet liggende søjlediagram)</li>
</ul></td>
<td><ul>
<li>Antal produkter i alt</li>
<li>Antal aktive produkter i alt i procentdel af antal produkter i alt</li>
<li>Antal produkter, der udgør for 80 % af indkøbet</li>
</ul></td>
</tr>
<tr>
<td>Indkøb efter periode*</td>
<td><ul>
<li>Indkøb pr. måned/dag (søjlediagram)</li>
<li>Afvigelse i akkumuleret indkøb år for år (vandfaldsdiagram)</li>
<li>Vækst i indkøb i alt år for år (søjlediagram)</li>
<li>Indkøbsopgørelse (matrix)</li>
</ul></td>
<td><ul>
<li>Indkøbsvækst år for år</li>
<li>Indkøbsvækst år for år i %</li>
</ul></td>
</tr>
<tr>
<td>Indkøb efter leverandørlokalitet</td>
<td><ul>
<li>Indkøb efter by</li>
<li>Indkøbsvækst år for år i %</li>
<li>Indkøb efter land</li>
</ul></td>
<td></td>
</tr>
<tr>
<td>Købsforbrugsanalyse efter tidspunkt</td>
<td><ul>
<li>Indkøb indeværende år efter måned/dag (kurvediagram)</li>
<li>Køb indeværende og sidste år (linje- og søjlediagram)</li>
</ul></td>
<td></td>
</tr>
<tr>
<td>Købsforbrugsanalyse efter leverandør</td>
<td><ul>
<li>Indkøb hos top 10 kreditorer i % af indkøb (tragtformet)</li>
<li>Top 10 leverandører med forøget forbrug år for år</li>
<li>Top 10 leverandører med faldende forbrug år for år</li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

\* Køb dette og sidste år, og vækst efter indkøbskategori

## <a name="data-model-and-entities"></a>Datamodel og enheder
Følgende data bruges til at udfylde rapportsiderne i Power BI-indholdet til **Købsforbrugsanalyse**. Disse data repræsenteres som samlede målinger, der er klargjort i enhedslageret. Enhedslageret er en Microsoft SQL Server-database, der er optimeret til analyser. Du kan finde flere oplysninger under [Oversigt over Power BI-integration med enhedslager](power-bi-integration-entity-store.md).

De samlede målinger i dette indhold er et undersæt af de samlede målinger, der var tilgængelige i indkøbskuben i Microsoft Dynamics AX 2012 og Microsoft Dynamics AX 2012 R3. For at forberede kubens samlede målinger i enhedslageret skal du gøre dem installerbare. Du kan finde flere oplysninger i fremgangsmåden for forberedelse af samlede målinger i enhedslager under [Oversigt over Power BI-integration med enhedslager](power-bi-integration-entity-store.md). Følgende samlede nøglemålinger er tilgængelige direkte fra enheden Fakturalinjer og bruges som grundlag for indholdet.

| Enhed        | Samlede nøglemålinger | Datakilde                                 | Felt              | Betegnelse                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| Fakturalinjer | Køb                   | VendInvoiceTrans                            | SUM(LineAmountMST) | Beløbet i regnskabsvalutaen. |

Følgende tabel viser de vigtigste målinger i indholdet, der beregnes fra enheden Fakturalinjer.

| Målepunkt               | Kalkulation                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Køb indeværende år | Køb indeværende år = SUM('Invoice lines'\[Purchase\])                                            |
| Køb sidste år    | Køb sidste år = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\])) |
| Indkøbsvækst år for år   | Indkøbsvækst år for år = \[Purchase current year\] – \[Purchase last year\]                            |

Følgende nøgledimensioner i indholdet bruges som filtre til at skabe udsnit af de samlede målinger, så du kan få større granularitet og dybere analytisk indsigt.

| Enhed                 | Eksempler på attributter                                |
|------------------------|-------------------------------------------------------|
| Leverandører                | Kreditorgrupper, kreditorlande eller -områder, kreditornavn |
| Produkter               | Produktnummer, produktnavn, varegruppenavn        |
| Indkøbskategorier | Indkøbskategori, indkøbskategorinavne      |
| Juridiske enheder         | Navn på juridisk enhed                                     |
| Datoer                  | Datoer, årsforskydning                                    |

Som standard viser indholdet data for det indeværende kalenderår. Du kan dog ændre datofilteret i rapportens filterafsnit. Du kan også ændre firmafilteret.

