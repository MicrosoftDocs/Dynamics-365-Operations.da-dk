---
title: "Power BI-indhold til købsforbrugsanalyse"
description: "Dette emne beskriver, hvad der er inkluderet i købet af indholdspakken til købsforbrugsanalyse til Microsoft Power BI. Det beskrives, hvordan du får adgang til rapporter, der er inkluderet i indholdspakken, og der er oplysninger om den datamodel og de enheder, der er brugt til at oprette indholdspakken."
author: YuyuScheller
manager: AnnBe
ms.date: 2016-12-30 09 - 40 - 51
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 8cb928cbf1316e63a8c7de833587168cd36a455c
ms.lasthandoff: 03/29/2017


---

# <a name="purchase-spend-analysis-power-bi-content"></a>Power BI-indhold til købsforbrugsanalyse

Dette emne beskriver, hvad der er inkluderet i købet af indholdspakken til købsforbrugsanalyse til Microsoft Power BI. Det beskrives, hvordan du får adgang til rapporter, der er inkluderet i indholdspakken, og der er oplysninger om den datamodel og de enheder, der er brugt til at oprette indholdspakken.

<a name="overview"></a>Overblik
--------

Indholdspakken til købsforbrugsanalyse til Microsoft Power BI blev oprettet til indkøbschefer og chefer, der er ansvarlige for budgetter. Den er udviklet til at hjælpe dem med at holde øje med købsforbruget. Programmet bruger købstransaktionsdata fra Microsoft Dynamics 365 for Operations og indeholder både en samlet oversigt over alle firmaets købstal og en opdeling af købsforbrug pr. leverandør og vare. Rapporter fremhæve ændringer i købsforbruget over tid. Derfor kan de bruges til at give ledere besked om positive og negative forbrugstendenser for individuelle leverandører og produkter. Diagrammer viser købsforbruget til forskellige indkøbskategorier og kreditorgrupper. Kategori- og områdeledere kan have nytte af at bruge disse diagrammer til at identificere ændringer i forbrugsmønsteret. Indholdspakken giver indkøbschefer og ledere, der er ansvarlige for budgetter, mulighed for at analysere købsforbrug på følgende måder:

-   Køb år til dato (efter kreditorgruppe og individuelle kreditorer, indkøbskategori og individuelle produkter og leverandørlokalitet)
-   Ændring af køb år for-år (efter leverandørgruppe og indkøbskategori)

## <a name="accessing-the-content-pack"></a>Adgang til indholdspakken
Indholdspakken til analyse af købsforbrug er udgivet som et implementeringsaktiv i Microsoft Dynamics Lifecycle Services (LCS) og kan åbnes fra Microsoft Dynamics 365 for Operations. Du kan finde yderligere oplysninger om adgang til og åbning af Power BI-rapporter i [Power BI-indhold i LCS fra Microsoft og dine partnere](power-bi-content-microsoft-partners.md).

## <a name="metrics-that-are-included-in-the-content-pack"></a>Metrikker, der er inkluderet i indholdspakken
Indholdspakken til købsforbrugsanalyse indeholder en rapport, der består af et sæt metrikker. Disse metrikker visualiseres som diagrammer, felter og tabeller. I nedenstående tabel vises en oversigt over visualiseringerne i indholdspakken.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Rapportside</th>
<th>Diagrammer</th>
<th>Felter</th>
</tr>
</thead>
<tbody>
<tr class="odd">
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
<tr class="even">
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
<tr class="odd">
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
<tr class="even">
<td>Indkøb efter leverandørlokalitet</td>
<td><ul>
<li>Indkøb efter by</li>
<li>Indkøbsvækst år for år i %</li>
<li>Indkøb efter land</li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td>Købsforbrugsanalyse efter tidspunkt</td>
<td><ul>
<li>Indkøb indeværende år efter måned/dag (kurvediagram)</li>
<li>Køb indeværende og sidste år (linje- og søjlediagram)</li>
</ul></td>
<td></td>
</tr>
<tr class="even">
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
Dynamics 365 for Operations-data bruges til rapporten i indholdspakken til købsforbrugsanalyse. Disse data repræsenteres som samlede målinger, der gemmes midlertidigt i enhedslageret, som er en Microsoft SQL-database, der er optimeret til analyse. Du kan finde flere oplysninger om enhedslager i blogindlægget [Power BI-integration med enhedslager i Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). De samlede målinger i denne indholdspakke er et undersæt af samlede målinger, der var tilgængelige i indkøbskuben i Microsoft Dynamics AX 2012 og Microsoft Dynamics 365 for Operations 2012 R3. For at forberede kubens samlede målinger i enhedslageret skal du gøre dem installerbare. Du kan finde flere oplysninger i fremgangsmåden for forberedelse af samlede målinger i enhedslager i blogindlægget [Power BI-integration med enhedslager i Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Følgende samlede nøglemålinger er tilgængelige direkte fra enheden Fakturalinjer og bruges som grundlag for indholdspakken.

| Enhed        | Samlede nøglemålinger | Datakilde til Dynamics 365 for Operations | Felt              | Betegnelse                           |
|---------------|----------------------------|---------------------------------------------|--------------------|---------------------------------------|
| Fakturalinjer | Køb                   | VendInvoiceTrans                            | SUM(LineAmountMST) | Beløb i regnskabsvaluta |

Følgende tabel viser de vigtigste målinger, der beregnes i indholdspakken fra enheden Fakturalinjer.

| Målepunkt               | Kalkulation                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Køb indeværende år | Køb indeværende år = SUM('Invoice lines'\[Purchase\])                                            |
| Køb sidste år    | Køb sidste år = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\])) |
| Indkøbsvækst år for år   | Indkøbsvækst år for år = \[Purchase current year\] – \[Purchase last year\]                            |

Følgende nøgledimensioner i indholdspakken bruges som filtre til at skabe udsnit af de samlede målinger, så du kan få større granularitet og dybere analytisk indsigt.

| Enhed                 | Eksempler på attributter                                |
|------------------------|-------------------------------------------------------|
| Leverandører                | Kreditorgrupper, kreditorlande eller -områder, kreditornavn |
| Produkter               | Produktnummer, produktnavn, varegruppenavn        |
| Indkøbskategorier | Indkøbskategori, indkøbskategorinavne      |
| Juridiske enheder         | Navn på juridisk enhed                                     |
| Datoer                  | Datoer, årsforskydning                                    |

Som standard viser indholdspakken data for det indeværende kalenderår. Du kan dog ændre datofilteret i rapportens filterafsnit. Du kan også ændre firmafilteret.

## <a name="additional-resources"></a>Yderligere ressourcer
Her er nogle nyttige links, der er knyttet til enheder og oprettelse af Power BI-indhold:

-   [Dataenheder](..\data-entities\data-entities.md)
-   [Oprettelse af organisatoriske indholdspakker](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datamodellering i Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Tilføjelse af Power BI-felter til arbejdsområder](configure-power-bi-integration.md)



