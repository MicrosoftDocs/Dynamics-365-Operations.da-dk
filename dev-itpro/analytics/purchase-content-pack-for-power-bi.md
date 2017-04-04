---
title: "Køb analyse strøm BI indhold af forbrug"
description: "Dette emne beskriver, hvad der er inkluderet i købet bruge analyse indhold pack til Microsoft Power BI. Det forklarer, hvordan du kan få adgang til rapporter, der er inkluderet i pakken med indhold og indeholder oplysninger om datamodel og enheder, der bruges til at oprette indhold pack."
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

# <a name="purchase-spend-analysis-power-bi-content"></a>Køb analyse strøm BI indhold af forbrug

Dette emne beskriver, hvad der er inkluderet i købet bruge analyse indhold pack til Microsoft Power BI. Det forklarer, hvordan du kan få adgang til rapporter, der er inkluderet i pakken med indhold og indeholder oplysninger om datamodel og enheder, der bruges til at oprette indhold pack.

<a name="overview"></a>Overblik
--------

Køb bruger analyse indhold pack til Microsoft Power BI blev oprettet for at købe ledere og ledere, der er ansvarlig for budgetter. Den er udviklet til at hjælpe dem med at holde øje med udgifterne til køb. Det bruger køb transaktionsdata fra Microsoft Dynamics 365 for operationer og indeholder både en samlet oversigt over hele firmaet køb tallene og en opdeling af køb forbrug af leverandør og vare. Rapporter fremhæve ændringer i purchase forbrug over tid. De kan derfor bruges til beskeder ledere om positive og negative udgifter tendenser for individuelle leverandører og produkter. Søjlediagrammer viser køb udgifter til forskellige indkøbskategorier og kreditorgrupper. Kategori og regionale ledere kan være nyttigt at bruge disse diagrammer til at identificere ændringer i forbrugs funktionsmåde. Indhold pack Lad indkøbschefer og ledere, der er ansvarlige for budgetter analysere køb forbrug på følgende måder:

-   Køb for år-til-dato (efter kreditorgruppe og individuelle kreditorer, indkøbskategori og individuelle produkter og leverandør)
-   Ændring af køb for år-over-år (efter leverandør gruppe og indkøb kategori)

## <a name="accessing-the-content-pack"></a>Adgang til indhold pack
Køb bruger analyse indhold pack er udgivet på aktivsiden gennemførelse i Microsoft Dynamics livscyklus Services (LCS) og kan åbnes fra Microsoft Dynamics 365 for operationer. Yderligere oplysninger om adgang til og åbne strøm BI-rapporter, du [Power BI indhold i LCS fra Microsoft og dine partnere](power-bi-content-microsoft-partners.md).

## <a name="metrics-that-are-included-in-the-content-pack"></a>Mål, som er inkluderet i pakken med indhold
Køb ofre indhold pack indeholder en rapport, der består af et sæt af metrisk analyse. Denne statistik er visualized som diagrammer, fliser og tabeller. Følgende tabel indeholder en oversigt over de visuelle effekter i indhold pack.

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
<th>Fliser</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Indkøb efter leverandør</td>
<td><ul>
<li>Top 10 leverandører ved køb (stablet liggende søjlediagram)</li>
<li>Samlet indkøb pr. leverandør gruppe / land / navn (cirkeldiagram)</li>
<li>Indkøb pr. leverandør gruppe / land / navn (søjlediagram)</li>
<li>Gennemsnitligt indkøb pr. leverandør gruppe / land / navn (søjlediagram)</li>
</ul></td>
<td><ul>
<li>Indkøb i alt</li>
<li>YOY køb vækst</li>
<li>Samlet antal kreditorer</li>
<li>Samlet antal aktive leverandører</li>
</ul></td>
</tr>
<tr class="even">
<td>Køb af produktet</td>
<td><ul>
<li>Køb efter indkøbskategori / produkt navn (søjlediagram)</li>
<li>Samlet køb efter indkøbskategori / produkt navn (cirkeldiagram)</li>
<li>Top 10 produkter efter køb (stablet liggende søjlediagram)</li>
</ul></td>
<td><ul>
<li>Samlet antal produkter</li>
<li>Aktive produkter for samlede procentdel af Samlet antal produkter</li>
<li>Antallet af produkter, der redegør for 80 % køb</li>
</ul></td>
</tr>
<tr class="odd">
<td>Køb af periode *</td>
<td><ul>
<li>Køb pr. måned / dag (søjlediagram)</li>
<li>Kumulative YOY Købsafvigelse (vandfald diagram)</li>
<li>Samlet køb YOY vækst (søjlediagram)</li>
<li>Indkøb-sætning (matrix)</li>
</ul></td>
<td><ul>
<li>YOY køb vækst</li>
<li>YOY køb vækst %</li>
</ul></td>
</tr>
<tr class="even">
<td>Indkøb efter leverandør</td>
<td><ul>
<li>Køb efter by</li>
<li>Køb YOY vækst %</li>
<li>Køb efter land</li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td>Køb analyse af forbrug af tid</td>
<td><ul>
<li>Køb indeværende år efter måned / dag (kurvediagram)</li>
<li>Købe aktuelle og sidste år (linje- og diagram)</li>
</ul></td>
<td></td>
</tr>
<tr class="even">
<td>Køb analyse af leverandør af forbrug</td>
<td><ul>
<li>Top 10 kreditor købs % af indkøb (tragtformet)</li>
<li>Top 10 leverandører med øget forbrug YOY</li>
<li>Top 10 leverandører med reduceret forbrug YOY</li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

\*Køb denne og sidste år og vækst efter indkøbskategori

## <a name="data-model-and-entities"></a>Datamodel og enheder
Dynamics 365 for operationer, der anvendes data for rapporten i købet ofre analyse indhold pack. Disse data er repræsenteret som samlede målinger, der er nødvendige i butikken enhed, som er en Microsoft SQL-database, der er optimeret til analytics. Finde flere oplysninger om butikken enhed, den [Power BI integration med enhed butik i Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/) blogindlæg. De samlede mål i dette indhold pack er undersæt af samlede målinger, der er tilgængelige i kuben i Microsoft Dynamics AX 2012 og Microsoft Dynamics 365 for operationer 2012 R3 køb. For at forberede kubens samlede mål i butikken enhed, skal du foretage dem installerbare. Yderligere oplysninger finder du i proceduren for midlertidig samlede mål i enhed, der er gemt i den [Power BI integration med enhed butik i Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/) blogindlæg. Følgende nøgle samlede målinger er tilgængelige direkte fra objektet faktura linjer og bruges som grundlag for indhold pack.

| Enhed        | Samlede nøgletal | Datakilden til Dynamics 365 til operationer | Felt              | Betegnelse                           |
|---------------|----------------------------|---------------------------------------------|--------------------|---------------------------------------|
| Fakturalinjer | Køb                   | VendInvoiceTrans                            | SUM(LineAmountMST) | Beløb i regnskabsvaluta |

Følgende tabel viser de vigtigste målinger, der beregnes i pakken med indhold fra objektet faktura linjer.

| Målepunkt               | Kalkulation                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Køb indeværende år | Køb indeværende år = SUM ('Fakturalinjer'\[køb\])                                            |
| Køb sidste år    | Køb sidste år = BEREGN (SUM ('Fakturalinjer'\[køb\]), SAMEPERIODLASTYEAR (datoer\[dato\])) |
| YOY køb vækst   | YOY købe vækst = \[køb af indeværende år\] – \[købe sidste år\]                            |

Følgende vigtige dimensioner i indhold pack bruges som filtre i udsnit af de samlede mål, så du kan opnå mere granularitet og større analytiske indsigt.

| Enhed                 | Eksempler på attributter                                |
|------------------------|-------------------------------------------------------|
| Leverandører                | Kreditorgrupper, kreditor lande eller regioner, kreditornavnet |
| Produkter               | Produktnummer, produktnavn, grupper for elementnavn        |
| Indkøbskategorier | Indkøbskategorien, indkøb kategorinavne      |
| Juridiske enheder         | Navn på juridisk enhed                                     |
| Datoer                  | Datoer, forskydning af år                                    |

Som standard viser indhold pack data for det indeværende kalenderår. Du kan dog ændre Datofilter i rapportafsnittet-filtre. Du kan også ændre filteret virksomhed.

## <a name="additional-resources"></a>Yderligere ressourcer
Her er nogle nyttige links, der er knyttet til enheder og oprettelse af Power BI-indhold:

-   [Dataenheder](..\data-entities\data-entities.md)
-   [Oprettelse af organisatoriske indholdspakker](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datamodellering i Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Tilføjelse af Power BI-felter til arbejdsområder](configure-power-bi-integration.md)



