---
title: "Omkostningsregnskab analyse strøm BI-indhold"
description: "Dette emne beskriver, hvad der skal medtages i omkostningsregnskabet analysen strøm BI-indhold. Det forklares, hvordan du få adgang til strøm BI-rapporter og indeholder oplysninger om datamodel og enheder, der blev brugt til at oprette indholdet."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 270274
ms.assetid: b74549df-35d5-4f2f-b3c7-405b0d38ea78
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 50e7bd92ee693f59fd013226aee22bd1a54c81e2
ms.lasthandoff: 03/31/2017


---

# <a name="cost-accounting-analysis-power-bi-content"></a>Omkostningsregnskab analyse strøm BI-indhold

Dette emne beskriver, hvad der skal medtages i omkostningsregnskabet analysen strøm BI-indhold. Det forklares, hvordan du få adgang til strøm BI-rapporter og indeholder oplysninger om datamodel og enheder, der blev brugt til at oprette indholdet.

<a name="overview"></a>Overblik
--------

Den **omkostningsregnskab analyse** Microsoft Power BI-indhold er beregnet til omkostninger domænecontrollere eller andre, der er ansvarlig for udførelse af omkostningsstyringen for en organisation. Den indeholder vigtige mål, som omkostningen, omfanget og omkostningssats ved faktiske omkostninger budgetomkostninger og fleksible budgetomkostninger. Det bruger transaktionsdata fra omkostningsregnskab i Microsoft Dynamics 365 for operationer og giver en samlet oversigt over omkostninger for hele organisationen i en rapporteringsvaluta. Ledere kan filtrere dataene ved omkostningsobjekter til at udføre omkostningsstyring af deres organisatoriske enheder, selv om organisationen kan have flere juridiske enheder. Da den **omkostningsregnskab analyse** Power BI indhold fremhæver afvigelser mellem de faktiske omkostninger og budgetterede omkostninger ledere kan blive informeret om positive og negative tendenser for deres operationelle enheder. Ledere kan finde frem til den omkostninger element hierarkier eller individuelle omkostningselementer få detaljeret indsigt i hvordan omkostningsafvigelser er opstået, og derefter handle effektivt. Den **omkostningsregnskab analyse** Power BI indhold Lad revisorer omkostninger analysere, hvordan kostprisen flyder gennem omkostningsobjekter i hele organisationen. Yderligere oplysninger om omkostningsregnskabet finder du [omkostningsregnskab hjemmeside](/dynamics365/operations/financials/cost-accounting/cost-accounting-home-page.md). Ved at definere sikkerhed på brugerniveau i omkostningsregnskabet, og at kombinere den med på strøm BI rækkeniveau sikkerhed, kan du tildele alle omkostninger objektejere adgang til den **omkostningsregnskab analyse** Power BI-indhold. Alle data i de visuelle effekter, derefter filtreres baseret på det adgangsniveau, der styres i omkostningsregnskab. Hvis du vil vide mere om sikkerhed på brugerniveau og rækkeniveau sikkerhed, se [angive sikkerhed for omkostningsregnskab indhold for strøm BI](setup-security-cost-accounting-content-pack.md).

## <a name="accessing-the-power-bi-content"></a>Adgang til strøm BI-indhold
Du kan finde det **omkostningsregnskab analyse** Power BI indhold i biblioteket delte aktiver i Microsoft Dynamics livscyklus Services (LCS). Finde flere oplysninger om, hvordan du henter indholdet og forbinde den til din Dynamics 365 for operationer data [Power BI indhold i LCS fra Microsoft og dine partnere](power-bi-content-microsoft-partners.md). **Bemærk:** KB4011327 ** ** er en forudsætning for den **omkostningsregnskab analyse** Power BI-indhold.  Når du logger på levetidsservices, kan du få adgang til KB her: <https://fix.lcs.dynamics.com/issue/results/?q=kb4011327>.

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Mål, som er inkluderet i indholdet strøm BI
Indholdet omfatter et sæt rapportsider. Hver side består af en række mål, som er visualized som diagrammer, fliser og tabeller. Følgende tabel indeholder en oversigt over de visuelle effekter i den **omkostningsregnskab analyse** Power BI-indhold.

| Rapportside                      | Diagram                                                                                                                         | Felt                                          |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| Omkostningsstyring efter regnskabsperiode    | Faktiske omkostninger og budgetomkostninger ved omkostninger element hierarkiniveau                                                                   | Faktiske omkostninger vs budgetomkostninger                    |
|                                  | Budget afvigelse af omkostninger element hierarkiniveau                                                                               | Faktiske omkostninger sats vs budgetomkostninger hastighed          |
|                                  | Top 10 Budget afvigelse i procent af omkostningselement                                                                          | Omfanget af faktiske størrelse i forhold til Budget          |
| Omkostningsstyring pr. år til dato     | Faktiske omkostninger og budgetomkostninger pr. kalenderår periode                                                                           | Faktiske omkostninger vs budgetomkostninger                    |
|                                  | Budget afvigelse pr. kalenderår periode                                                                                       | Faktiske omkostninger sats vs budgetomkostninger hastighed          |
|                                  | Top 10 Budget afvigelse i procent af omkostningselement                                                                          | Omfanget af faktiske størrelse i forhold til Budget          |
| Omkostningssats af regnskabsår         | Faktiske omkostningssats af omkostninger-funktionalitet                                                                                             | Faktiske omkostninger sats vs budgetomkostninger hastighed          |
|                                  | Faktiske omkostningssats Budget omkostningsafvigelse sats, budgetomkostninger procentsats og Budget omkostningssats efter omkostninger element hierarkiniveau | Omfanget af faktiske størrelse i forhold til Budget          |
|                                  | Budget afvigelse af omkostninger element hierarkiniveau                                                                               |                                               |
|                                  | Top 10 Budget afvigelse i procent af omkostningselement                                                                          |                                               |
| Fleksibelt budget efter regnskabsperiode | Faktiske omkostninger og budgetomkostninger fleksible budgetomkostninger ved omkostninger element hierarkiniveau                                             | Omfanget af faktiske størrelse i forhold til Budget          |
|                                  | Varians for budget og fleksibelt budget afvigelse af omkostninger element hierarkiniveau                                                  | Faktiske omkostninger i forhold til fleksible budgetomkostninger           |
|                                  | Faktiske omkostninger og budgetomkostninger fleksible omkostninger ved kostet funktionsmåde og kostet element hierarkiniveau                                  | Faktiske omkostninger sats vs fleksibelt budget omkostningssats |
| Omkostninger erklæring fra regnskabsperioden  | Faktiske omkostninger ved omkostninger element hierarkiniveau og omkostninger objekt medlem dimensionsnavn                                             |                                               |
|                                  | Faktiske omkostninger ved omkostninger objekt dimension-medlemsnavn og omkostninger element medlem dimensionsnavn                                       |                                               |

## <a name="understanding-the-data-model-and-entities"></a>Forståelse af datamodellen og enheder
Dynamics 365 for operationer data bruges til at udfylde siderne af rapporten den **omkostningsregnskab analyse** Power BI-indhold. Disse data er repræsenteret som samlede målinger, der er nødvendige i butikken enhed, som er en Microsoft SQL-database, der er optimeret til analytics. Yderligere oplysninger finder du [oversigt over strøm BI integration med store enhed](power-bi-integration-entity-store.md). Følgende nøgle samlede målinger bruges som grundlag for indholdet.

| Enhed                  | Samlede Kontrolmålepunkt | Datakilden til Dynamics 365 til operationer | Felt     | Betegnelse                                   |
|-------------------------|---------------------------|---------------------------------------------|-----------|-----------------------------------------------|
| Omkostningsregnskab poster | SUM(Amount)               | CAMDATAAggregatedCostEntry                  | Beløb    | Beløbet i omkostningsregnskabet Finans |
| Statistiske poster     | SUM(Magnitude)            | CAMDATAAggregatedStatisctialEntry           | Størrelsesorden |                                               |

Følgende tabel viser, hvor vigtige målinger af samlede bruges til at oprette flere beregnede målpunkter i det indhold dataset.

| Målepunkt                                       | Beregning af foranstaltningen                                                                                          |
|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Faktisk omkostning                                   | BEREGN ('omkostningsregnskab poster'\[foranstaltning\], 'Transaktion versioner'\[ISSOURCEVERSIONBUDGET\_værdi\] = 0)            |
| Budgetterede omkostninger                                   | BEREGN ('omkostningsregnskab poster'\[foranstaltning\], 'Transaktion versioner'\[ISSOURCEVERSIONBUDGET\_værdi\] = 1)            |
| Budgetomkostninger afvigelse                          | \[Budgettere omkostninger\] - \[faktiske omkostninger\]                                                                                      |
| Budget afvigelse i procent                    | Hvis (\[budgetomkostninger\] = 0, blank(), \[Budget afvigelse\] / \[budgetomkostning\])                                                |
| Faktiske omfang                              | BEREGN ('Statistiske poster'\[FullMagnitude\], 'Transaktion versioner'\[ISSOURCEVERSIONBUDGET\_værdi\] = 0)          |
| Omfanget af budget                              | BEREGN (\[FullMagnitude\], 'Transaktion versioner'\[ISSOURCEVERSIONBUDGET\_værdi\] = 1)                               |
| Statistiske budget afvigelse                   | \[Omfanget af budget\] - \[faktiske størrelse\]                                                                            |
| Statistiske budget afvigelse i procent        | IF (\[Budget omfanget\] = 0, blank(), \[statistiske budget afvigelse\] / \[Budget omfanget\])                          |
| Faktisk omkostningssats                              | IF (\[faktiske omfang\] = 0, BLANK(), \[faktiske omkostninger\] / \[faktiske omfang\])                                          |
| Budgetomkostningssats                              | IF (\[Budget omfanget\] = 0, BLANK(), \[budgetomkostninger\] / \[Budget omfanget\])                                          |
| Budgetomkostninger sats afvigelse                     | \[Budget omkostningssats\] - \[faktiske omkostningssats\]                                                                            |
| Budgetomkostninger sats afvigelsesprocenten          | IF (\[budgetomkostninger\] = 0, blank(), \[Budget sats omkostningsafvigelse\] / \[Budget omkostningssats\])                                 |
| Fast budgetomkostninger                             | BEREGN (\[budgetomkostning\], 'Omkostninger accounting poster'\[COSTBEHAVIOR\] = 1)                                              |
| Variable budgetomkostninger                          | BEREGN (\[budgetomkostning\], 'Omkostninger accounting poster'\[COSTBEHAVIOR\] = 2)                                              |
| Fast fleksible budgetomkostninger                    | \[Fast budgetomkostninger\]                                                                                                  |
| Variable fleksible budgetomkostninger                 | IF (\[Budget omfanget\] = 0, BLANK(), (\[Variable budgetomkostninger\] / \[Budget omfanget\]) \*\[faktiske omfang\])       |
| Fleksible budgetomkostninger.                          | \[Faste omkostninger for fleksibelt budget\] + \[Variable fleksible budgetomkostninger\]                                                     |
| Fleksibelt budget afvigelse                      | \[Fleksible budgetomkostninger\] - \[faktiske omkostninger\]                                                                             |
| Fleksibelt budget afvigelse i procent           | IF (\[fleksible budgetomkostninger\] = 0, BLANK(), \[fleksibelt budget afvigelse\] / \[fleksible budgetomkostninger\])                     |
| Fleksible budgetomkostninger hastighed                     | IF (\[faktiske omfang\] = 0, BLANK(), \[fleksible budgetomkostninger\] / \[faktiske omfang\])                                 |
| Fleksible budgetomkostninger sats afvigelse            | \[Fleksibelt budget omkostningssats\] - \[faktiske omkostningssats\]                                                                   |
| Fleksibelt budget sats procentvise omkostningsafvigelse | IF (\[fleksibelt budget omkostningssats\] = 0, BLANK(), \[fleksibelt budget sats omkostningsafvigelse\] / \[fleksibelt budget omkostningssats\]) |

Følgende vigtige dimensioner bruges som filtre i udsnit af de samlede mål for at opnå større granularitet og giver større analytiske indsigt.

| Enhed                             | Eksempler på attributter                                                                                               |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Finansposter for omkostningsregnskab            | Finanspost for omkostningsregnskab                                                                                               |
| Omkostningskontrolenheder                 | Navn på omkostningskontrolenhed                                                                                               |
| Dimensioner for omkostningselement            | Omkostninger elementer dimension navn, omkostninger element dimension medlemsnavn, omkostninger dimension medlem elementbeskrivelse          |
| Dimensioner for omkostningsobjekt             | Omkostningsobjekt dimensionsnavnet, omkostninger objekt dimension medlemsnavn, omkostninger objekt dimension medlem beskrivelse              |
| Statistiske dimensioner             | Statistiske dimensionsnavnet, statistiske dimension medlemsnavn, statistiske dimensionsbeskrivelsen medlem              |
| Dimensionshierarkier omkostningsobjekt  | Cost objektet dimensionsnavnet hierarki, Cost objektet dimension hierarkiniveau, omkostninger objekt hierarki dimensionstræ    |
| Dimensionshierarkier omkostninger element | Omkostninger dimension hierarki elementnavn, omkostningskladde element dimension hierarkiniveau, omkostninger element dimension hierarkitræ |
| Statistiske dimensionshierarkier  | Statistiske dimensionsnavnet for hierarkiet, statistiske dimension hierarkiniveau, statistiske dimension hierarkitræ    |
| Versioner af transaktion               | Versionsnavn                                                                                                         |
| Regnskabskalendere                   | Kalenderen er kalender-beskrivelse                                                                                       |
| Regnskabsår                       | Kalenderår                                                                                                        |
| Regnskabsperioder                     | Periode af kalenderåret                                                                                                 |

## <a name="additional-resources"></a>Yderligere ressourcer
Her er nogle nyttige links, der er knyttet til enheder og oprettelse af Power BI-indhold:

-   [Dataenheder](..\data-entities\data-entities.md)
-   [Oprettelse af organisatoriske indholdspakker](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datamodellering i Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Tilføjelse af Power BI-felter til arbejdsområder](configure-power-bi-integration.md)
-   [Opsætning af sikkerhed for omkostningsregnskab indhold for strøm BI](setup-security-cost-accounting-content-pack.md)


