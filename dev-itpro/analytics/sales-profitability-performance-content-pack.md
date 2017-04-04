---
title: "Salg og rentabilitet ydeevne strøm BI-indhold"
description: "Dette emne beskriver, hvad der skal medtages i Dynamics-365 for operationer – salg og rentabilitet ydeevne indhold pack til Microsoft Power BI. Det forklarer, hvordan du kan få adgang til rapporter, der er inkluderet i pakken med indhold og indeholder oplysninger om datamodel og enheder, der bruges til at oprette indhold pack."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 260674
ms.assetid: ab457f02-929e-4d34-b813-335be3092287
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 3e6b48768bb8e69d46f1555d9300f3b878b01ff1
ms.lasthandoff: 03/31/2017


---

# <a name="sales-and-profitability-performance-power-bi-content"></a>Salg og rentabilitet ydeevne strøm BI-indhold

Dette emne beskriver, hvad der skal medtages i Dynamics-365 for operationer – salg og rentabilitet ydeevne indhold pack til Microsoft Power BI. Det forklarer, hvordan du kan få adgang til rapporter, der er inkluderet i pakken med indhold og indeholder oplysninger om datamodel og enheder, der bruges til at oprette indhold pack.

<a name="overview"></a>Overblik
--------

Dette indhold pack blev oprettet til salgschefer overvåge nøglemål for omsætning, bruttoavance og overskudsgrader salg. Det bruger salg transaktionsdata fra Dynamics 365 for operationer og indeholder både en samlet oversigt over hele firmaet salgstal og en opdeling af salg til kunder og produkter. Ved at fremhæve ændringer i væksten i omsætning og overskud over tid, kan rapporter bruges til beskeder ledere om positive og negative tendenser for individuelle kunder og produkter. Kategori og regionale ledere kan finde det nyttigt at have diagrammer, der sammenligner indtjeningen af forskellige produktkategorier og debitorgrupper til hinanden til at udpege laggards og førende virksomheder. En omfattende rapport, der afbilder individuel kundes omsætning i forhold til fortjeneste tilbyder kontoadministratorer data sikkerhedskopieres grundlag for at attune deres salg og marketing indsats til hver enkelt kundes respektive profil. Salg og rentabilitet ydeevne indhold pack kan salgschefer til at analysere salgsresultater ved:

-   Omsætning, år til dato (efter debitorgruppe og individuelle kunder, salg kategorier og individuelle produkter og lande)
-   Ændring af omsætning, år-over-år (efter kunde regioner og salg kategorier)

Rentabiliteten kan analyseres ved:

-   Bruttoavance og fortjenstmargen (efter debitorgrupper og produktkategorier til salg)
-   Bruttoavance ændring år-over-år
-   Kunden rentabilitet (efter omsætning i forhold til dækningsbidraget)

## <a name="accessing-the-content-pack"></a>Adgang til indhold pack
Salg og rentabilitet ydeevne strøm BI indhold pack er udgivet på aktivsiden gennemførelse i livscyklus Services (LCS) og kan åbnes fra Dynamics 365 for operationer. Finde flere oplysninger om, hvordan du får adgang til og start strøm BI rapporter [Power BI indhold i LCS fra Microsoft og dine partnere](power-bi-content-microsoft-partners.md).

## <a name="metrics-included-in-the-content-pack"></a>Målestok, der er inkluderet i pakken med indhold
Indhold pack indeholder en rapport, der består af et sæt af metrisk visualized som diagrammer, fliser og tabeller. Følgende tabel indeholder en oversigt over visualisations i indhold pack.

|                        |                                            |                                                         |
|------------------------|--------------------------------------------|---------------------------------------------------------|
| **Rapportside**        | **Charts**                                 | **Fliser**                                               |
| Omsætning pr. kunde    | Bedste 10 kunder efter omsætning                | Samlet omsætning                                           |
|                        | Samlede indtægt efter kundegruppe            | YOY stigning i omsætningen                                      |
|                        | Gennemsnitlig kunde indtægt efter kundegruppe | Bruttoavance                                            |
|                        | Omsætning og bruttoavance efter kundegruppe   |                                                         |
| Omsætning efter produkt     | Omsætning og bruttoavance efter salgskategori   | Samlede \#af produkter                                    |
|                        | Top 10 produkter efter omsætning                 | Det samlede antal aktive produkter og procent af total |
|                        | Samlet omsætning efter salgskategori            | Antallet af produkter, der redegør for 80 % omsætning           |
| Omsætning pr. periode\*    | Omsætning pr. måned                           | YOY stigning i omsætningen                                      |
|                        | Efterfølgende omsætning afvigelse, YOY             | YOY omsætning vækst %                                    |
|                        | Afvigelse salg efter kunde, område    |                                                         |
| Omsætning pr. lokation    | Omsætning efter by                      |                                                         |
|                        | YOY omsætning vækst %                       |                                                         |
|                        | Omsætning efter område                    |                                                         |
| Kunden rentabilitet | Bruttoavance kontra omsætning pr. kunde   | Bruttofortjeneste, dækningsbidrag, YOY stigning i omsætningen          |
| Rentabilitetsanalyse | Omsætning og bruttoavance pr. måned          |                                                         |
|                        | Top 15 kunder efter dækningsbidrag           |                                                         |
|                        | Bruttoavance pr. måned, YOY                 |                                                         |

\*Omsætning dette og sidste år og vækst efter salgskategori.

## <a name="understanding-the-data-model-and-entities"></a>Forståelse af datamodellen og enheder
Dynamics 365 for operationer data bruges til at udfylde rapporten i salg og rentabilitet ydeevne indhold pack. Dette er repræsenteret som samlede målinger, der er nødvendige i butikken enhed, som er en Microsoft SQL-database, der er optimeret til analytics. Læs mere om det i bloggen [Power BI integration med enhed butik i Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). De samlede mål i dette indhold pack er et undersæt af de samlede mål, der var tilgængelige i kuben salg i Dynamics AX 2012 og AX 2012 R3. For at forberede kubens samlede mål i butikken enhed skal du foretage dem installerbare. Se proceduren kan finde flere oplysninger om, hvordan du forbereder samlede mål til enhed, der er gemt i bloggen [Power BI integration med enhed butik i Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Følgende nøgle samlede målinger af objektet faktura linjer bruges som grundlag for indhold pack.

|               |                                              |                                                 |                                              |                                          |
|---------------|----------------------------------------------|-------------------------------------------------|----------------------------------------------|------------------------------------------|
| **Entity**    | **Samlede nøgletal**               | **Datakilden til Dynamics 365 til operationer** | **Field**                                    | **Description**                          |
| Fakturalinjer | Indtægter                                      | CustInvoiceTrans                                | SUM(LineAmountMST)                           | Beløb i regnskabsvaluta            |
|               | Vareforbrug                           | InventTrans                                     | SUM (CostAmountPosted + CostAmountAdjustment) | Kostbeløb + justering                 |
|               | Kommissionen Linjebeløb – regnskabsvaluta | CustInvoiceTrans                                | SUM(CommissAmountMST)                        | Provisionsbeløbet i regnskabsvaluta |

Følgende tabel viser de vigtigste samlede målinger af objektet faktura linjer, der bruges til at oprette flere beregnede målpunkter i indhold pack dataset.

|                   |                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------|
| **Measure**       | **Beregnet som**                                                                                |
| Bruttoavance      | SUM (omsætning) – VAREFORBRUG – Kommissionen – moms (inkluderet i debitorfakturalinjebeløb)          |
| Bruttoavance      | SUM (bruttofortjeneste / (omsætning - moms (inkluderet i debitorfakturalinjebeløb)))             |
| Omsætning sidste år | Omsætning sidste år = BEREGN (SUM ('Fakturalinjer'\[indtægter\]), SAMEPERIODLASTYEAR (datoer\[dato\]) |

Følgende vigtige dimensioner i den **salg kube** er brugt som filtre til at vise de samlede mål for at opnå større granularitet og større analytiske indsigt.

|                  |                                                      |
|------------------|------------------------------------------------------|
| **Entity**       | **Eksempler på attributter**                           |
| Kunder        | Debitorgrupper, kunde regioner, adresse, branche |
| Produkter         | Produktnummer, produktnavn, grupper for elementnavn       |
| Salgskategorier | Salgskategorien navne                                 |
| Juridiske enheder   | Navn på juridisk enhed                                   |
| Datoer            | Datoer                                                |

Indhold pack viser data for det indeværende kalenderår som standard, men du kan åbne filtre rapportsektion og ændre Datofilter. Du kan også ændre filteret virksomhed.

## <a name="additional-resources"></a>Yderligere ressourcer
Her er nogle nyttige links, der er knyttet til enheder og oprettelse af Power BI-indhold:

-   [Dataenheder](..\data-entities\data-entities.md)
-   [Oprettelse af organisatoriske indholdspakker](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datamodellering i Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Tilføjelse af Power BI-felter til arbejdsområder](configure-power-bi-integration.md)



