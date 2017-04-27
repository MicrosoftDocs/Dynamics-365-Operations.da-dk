---
title: Salgs- og rentabilitetsperformance, Power BI-indhold
description: "Dette emne beskriver, hvad der er indeholdt i Dynamics-365 for Operations – indholdspakke til salgs- og rentabilitetsperformance til Microsoft Power BI. Det beskrives, hvordan du får adgang til rapporter, der er inkluderet i indholdspakken, og der er oplysninger om den datamodel og de enheder, der er brugt til at oprette indholdspakken."
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

# <a name="sales-and-profitability-performance-power-bi-content"></a>Salgs- og rentabilitetsperformance, Power BI-indhold

Dette emne beskriver, hvad der er indeholdt i Dynamics-365 for Operations – indholdspakke til salgs- og rentabilitetsperformance til Microsoft Power BI. Det beskrives, hvordan du får adgang til rapporter, der er inkluderet i indholdspakken, og der er oplysninger om den datamodel og de enheder, der er brugt til at oprette indholdspakken.

<a name="overview"></a>Overblik
--------

Denne indholdspakke blev oprettet til salgschefer overvågning af salgsmetrikker for omsætning, bruttoavance og overskudsgrader. Programmet bruger salgstransaktionsdata fra Microsoft Dynamics 365 for Operations og indeholder både en samlet oversigt over alle firmaets salgstal og en opdeling af salgsperformance for kunder og produkter. Ved at fremhæve ændringer i væksten i omsætning og overskud over tid, kan rapporter bruges til at gøre ledere opmærksom på positive og negative tendenser for individuelle kunder og produkter. Kategori- og områdeledere kan finde det nyttigt at have diagrammer, der sammenligner omsætning og rentabilitet for forskellige produktkategorier og kundegrupper med hinanden til at udpege tabere og vindere. En omfattende rapport, der afbilder de enkelte kunders omsætning i forhold til overskudsgraden giver account managers et databaseret grundlag for at tilpasse deres salgs- og marketingindsats til hver enkelt kundes respektive profil. Indholdspakken til salgs- og rentabilitetsperformance giver salgschefer mulighed for at analysere salgsperformance efter:

-   Omsætning, år til dato (efter kundegruppe og individuelle kunder, salgskategorier og individuelle produkter og geografiske områder)
-   Omsætningsændring, år for år (efter kunderegioner og salgskategorier)

Rentabiliteten kan analyseres efter:

-   Bruttoavance og overskudsgrad (efter kundegrupper og produktsalgskategorier)
-   Bruttoavanceændring, år for år
-   Kunderentabilitet (efter omsætning i forhold til bruttoavance)

## <a name="accessing-the-content-pack"></a>Adgang til indholdspakken
Indholdspakken til salgs- og rentabilitetsperformance til Power BI er udgivet som et implementeringsaktiv i Lifecycle Services (LCS) og kan åbnes fra Microsoft Dynamics 365 for Operations. Du kan finde yderligere oplysninger om adgang til og start af Power BI-rapporter i [Power BI-indhold i LCS fra Microsoft og dine partnere](power-bi-content-microsoft-partners.md).

## <a name="metrics-included-in-the-content-pack"></a>Metrikker, der er inkluderet i indholdspakken
Indholdspakken indeholder en rapport, der består af et sæt metrikker, der er visualiseret som diagrammer, felter og tabeller. I nedenstående tabel vises en oversigt over visualiseringerne i indholdspakken.

|                        |                                            |                                                         |
|------------------------|--------------------------------------------|---------------------------------------------------------|
| **Rapportside**        | **Diagrammer**                                 | **Felter**                                               |
| Omsætning efter kunde    | Top 10-kunder efter omsætning                | Samlet omsætning                                           |
|                        | Samlet omsætning efter kundegruppe            | Stigning år for år i omsætning                                      |
|                        | Gennemsnitlig kundeomsætning efter kundegruppe | Bruttoavance                                            |
|                        | Omsætning og bruttoavance efter kundegruppe   |                                                         |
| Omsætning efter produkt     | Omsætning og bruttoavance efter salgskategori   | Antal produkter i alt                                    |
|                        | Top 10-produkter efter omsætning                 | Antal aktive produkter i alt og procentdel af antal produkter i alt |
|                        | Omsætning i alt efter salgskategori            | Antal produkter, der udgør for 80 % af omsætningen           |
| Omsætning pr. periode\*    | Omsætning pr. måned                           | Stigning år for år i omsætning                                      |
|                        | Efterfølgende omsætningsafvigelse år for år             | Stigning i % år for år i omsætning                                    |
|                        | Afvigelse i salg i alt efter kundeområde    |                                                         |
| Omsætning efter lokalitet    | Omsætning efter by                      |                                                         |
|                        | Stigning i % år for år i omsætning                       |                                                         |
|                        | Omsætning pr. område                    |                                                         |
| Kunderentabilitet | Bruttoavance i forhold til omsætning, efter kunde   | Bruttofortjeneste, dækningsbidrag, stigning i omsætningen år for år          |
| Rentabilitetsanalyse | Omsætning og bruttoavance pr. måned          |                                                         |
|                        | Top 15-kunder efter bruttoavance           |                                                         |
|                        | Bruttoavance pr. måned, år for år                 |                                                         |

\* Omsætning dette og sidste år, og vækst efter salgskategori.

## <a name="understanding-the-data-model-and-entities"></a>Forståelse af datamodellen og enheder
Dynamics 365 for Operations-data bruges til at udfylde rapporterne i indholdspakken til salgs- og rentabilitetsperformance. Disse repræsenteres som samlede målinger, der gemmes midlertidigt i enhedslageret, som er en Microsoft SQL-database, der er optimeret til analyse. Læs mere om det i bloggen [Power BI-integration med enhedslager i Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). De samlede målinger i denne indholdspakke er et undersæt af de samlede målinger, der var tilgængelige i salgskuben i Dynamics AX 2012 og AX 2012 R3. For at forberede kubens samlede målinger i enhedslageret skal du gøre dem installerbare. Du kan finde flere oplysninger i fremgangsmåden for forberedelse af samlede målinger i enhedslager i blogindlægget [Power BI-integration med enhedslager i Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Følgende samlede nøglemålinger for enheden Fakturalinjer bruges som grundlag for indholdspakken.

|               |                                              |                                                 |                                              |                                          |
|---------------|----------------------------------------------|-------------------------------------------------|----------------------------------------------|------------------------------------------|
| **Enhed**    | **Samlede nøglemålinger**               | **Datakilde til Dynamics 365 for Operations** | **Felt**                                    | **Beskrivelse**                          |
| Fakturalinjer | Indtægter                                      | CustInvoiceTrans                                | SUM(LineAmountMST)                           | Beløb i regnskabsvaluta            |
|               | Vareforbrug                           | InventTrans                                     | SUM (CostAmountPosted + CostAmountAdjustment) | Omkostningsbeløb + regulering                 |
|               | Provisionslinjebeløb – regnskabsvaluta | CustInvoiceTrans                                | SUM(CommissAmountMST)                        | Provisionsbeløb i regnskabsvaluta |

Nedenstående tabel viser de samlede nøglemålinger af enheden Fakturalinjer, der bruges til at oprette flere beregnede målepunkter i indholdspakkens datasæt.

|                   |                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------|
| **Målepunkt**       | **Beregnet som**                                                                                |
| Bruttoavance      | SUM(Omsætning – vareforbrug – provision – moms (inkluderet i debitorfakturalinjebeløb))          |
| Bruttoavance      | SUM(Bruttoavance/(Omsætning - moms (inkluderet i debitorfakturalinjebeløb)))             |
| Omsætning sidste år | Omsætning sidste år = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\])) |

Følgende nøgledimensioner i **Salgskuben** bruges som filtre til at skabe udsnit af de samlede målinger for at opnå større granularitet og give dybere analytisk indsigt.

|                  |                                                      |
|------------------|------------------------------------------------------|
| **Enhed**       | **Eksempler på attributter**                           |
| Kunder        | Debitorgrupper, kundeområder, adresse, branche |
| Produkter         | Produktnummer, produktnavn, varegruppenavn       |
| Salgskategorier | Navne på salgskategorier                                 |
| Juridiske enheder   | Navne på juridisk enhed                                   |
| Datoer            | Datoer                                                |

Indholdspakken viser som standard data for det indeværende kalenderår, men du kan åbne afsnittet Rapportfiltre og ændre datofilteret. Du kan også ændre firmafilteret.

## <a name="additional-resources"></a>Yderligere ressourcer
Her er nogle nyttige links, der er knyttet til enheder og oprettelse af Power BI-indhold:

-   [Dataenheder](..\data-entities\data-entities.md)
-   [Oprettelse af organisatoriske indholdspakker](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datamodellering i Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Tilføjelse af Power BI-felter til arbejdsområder](configure-power-bi-integration.md)



