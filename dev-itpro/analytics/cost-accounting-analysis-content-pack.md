---
title: Power BI-indhold til omkostningsregnskabsanalyse
description: "I dette emne beskrives, hvad der skal medtages i Power BI-indhold til omkostningsregnskabet. Det beskrives, hvordan du får adgang til Power BI-rapporter, og der er oplysninger om den datamodel og de enheder, der blev brugt til at oprette indholdspakken."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 270274
ms.assetid: b74549df-35d5-4f2f-b3c7-405b0d38ea78
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 5ce75a6145bde4a8c33ed785c7d2a60a52416676
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="cost-accounting-analysis-power-bi-content"></a>Power BI-indhold til omkostningsregnskabsanalyse

[!include[banner](../includes/banner.md)]


I dette emne beskrives, hvad der skal medtages i Power BI-indhold til omkostningsregnskabet. Det beskrives, hvordan du får adgang til Power BI-rapporter, og der er oplysninger om den datamodel og de enheder, der blev brugt til at oprette indholdspakken.

<a name="overview"></a>Overblik
--------

Microsoft Power BI-indholdet til **Omkostningsregnskabsanalyse** er beregnet til omkostningscontrollere eller andre, der er ansvarlig for udførelse af en organisations omkostningsstyring. Det indeholder oversigt over målepunkter som omkostning, størrelsesorden og omkostningssats ved faktisk omkostning, budgetomkostninger og fleksible budgetomkostninger. Det bruger transaktionsdata fra omkostningsregnskab i Microsoft Dynamics 365 for Operations og giver en samlet oversigt over omkostninger for hele organisationen i én rapporteringsvaluta. Ledere kan filtrere dataene efter omkostningsobjekter for at udføre omkostningsstyring af deres organisatoriske enheder, selv om organisationen kan have flere juridiske enheder. Da Power BI indhold til **Omkostningsregnskabsanalyse** fremhæver afvigelser mellem de faktiske omkostninger og budgetterede omkostninger, kan ledere blive informeret om positive og negative tendenser for deres driftsenheder. Lederne kan foretage detailudledning i omkostningselementhierarkierne eller individuelle omkostningselementer for at få detaljeret indsigt i, hvordan omkostningsafvigelser er opstået, og derefter handle effektivt på det. Med Power BI-indholdet til **Omkostningsregnskabsanalyse** kan bogholdere analysere, hvordan omkostninger flyder gennem omkostningsobjekter i hele organisationen. Du kan finde flere oplysninger om omkostningsregnskabet i [Startside for omkostningsregnskab](/dynamics365/operations/financials/cost-accounting/cost-accounting-home-page). Ved at definere sikkerhed på brugerniveau i omkostningsregnskabet og kombinere det med sikkerhed på rækkeniveau i Power BI kan du tildele alle omkostningsobjektejere adgang til Power BI-indholdet til **Omkostningsregnskabsanalyse**. Alle data i visualiseringerne filtreres derefter baseret på det adgangsniveau, der styres i omkostningsregnskabet. Hvis du vil vide mere om sikkerhed på henholdsvis adgangsniveau og rækkeniveau, kan du se under [Konfigurere sikkerhed for indhold i omkostningsregnskab til Power BI](setup-security-cost-accounting-content-pack.md).

## <a name="accessing-the-power-bi-content"></a>Adgang til Power BI-indhold
Du kan finde Power Bi-indholdet til **Omkostningsregnskabsanalyse** i biblioteket Delte aktiver i Microsoft Dynamics Lifecycle Services (LCS). Du kan finde flere oplysninger om, hvordan du henter indholdet og forbinder det med dine Microsoft Dynamics-365 for Operations-data, under [Power BI indhold i LCS fra Microsoft og dine partnere](power-bi-content-microsoft-partners.md). 

> BEMÆRK - **KB4011327** er en forudsætning for dette Power BI-indhold. Når du logger på Lifecycle Services, kan du få adgang til KB her: <https://fix.lcs.dynamics.com/issue/results/?q=kb4011327>.

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Metrikker, der er inkluderet i Power BI-indhold
Indholdet omfatter et sæt rapportsider. Hver side består af en række mål, som er visualiseret som diagrammer, felter og tabeller. I nedenstående tabel vises en oversigt over visualiseringerne i Power BI-indholdet til **Omkostningsregnskabsanalyse**.

| Rapportside                      | Diagram                                                                                                                         | Felt                                          |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| Omkostningsstyring efter regnskabsperiode    | Faktisk omkostning og budgetomkostning efter niveau i omkostningselementhierarki                                                                   | Faktisk omkostning vs. budget                    |
|                                  | Budgetafvigelse af niveau i omkostningselementhierarki                                                                               | Faktisk omkostningssats vs. budgetomkostningssats          |
|                                  | 10 bedste budgetafvigelser i procent efter omkostningselement                                                                          | Faktisk størrelsesorden vs. størrelsesorden af budget          |
| Omkostningsstyring pr. år til dato     | Faktisk omkostning og budgetomkostning pr. kalenderårperiode                                                                           | Faktisk omkostning vs. budget                    |
|                                  | Budgetafvigelse pr. kalenderårperiode                                                                                       | Faktisk omkostningssats vs. budgetomkostningssats          |
|                                  | 10 bedste budgetafvigelser i procent efter omkostningselement                                                                          | Faktisk størrelsesorden vs. størrelsesorden af budget          |
| Omkostningssats pr. regnskabsår         | Faktisk omkostningssats efter omkostningsfunktionalitet                                                                                             | Faktisk omkostningssats vs. budgetomkostningssats          |
|                                  | Faktisk omkostningssats, budgetomkostningssatsafvigelse, budgetomkostningssatsprocent og budgetomkostningssats efter niveau i omkostningselementhierarki | Faktisk størrelsesorden vs. størrelsesorden af budget          |
|                                  | Budgetafvigelse af niveau i omkostningselementhierarki                                                                               |                                               |
|                                  | 10 bedste budgetafvigelser i procent efter omkostningselement                                                                          |                                               |
| Fleksibelt budget efter regnskabsperiode | Faktisk omkostning, budgetomkostning og fleksibel budgetomkostning efter niveau i omkostningselementhierarki                                             | Faktisk størrelsesorden vs. størrelsesorden af budget          |
|                                  | Budgetafvigelse og fleksibel budgetafvigelse efter niveau i omkostningselementhierarki                                                  | Faktisk omkostning vs. fleksibel budgetomkostning           |
|                                  | Faktisk omkostning, budgetomkostning og fleksibel omkostning efter funktionalitet af omkostning og niveau i omkostningselementhierarki                                  | Faktisk omkostningssats vs. fleksibel budgetomkostningssats |
| Omkostningsfordeling efter regnskabsperiode  | Faktisk omkostning efter niveau i omkostningselementhierarki og navn på dimensionsmedlem for omkostningsobjekt                                             |                                               |
|                                  | Faktisk omkostning efter navn på dimensionsmedlem for omkostningsobjekt                                       |                                               |

## <a name="understanding-the-data-model-and-entities"></a>Forståelse af datamodellen og enheder
Dynamics 365 for Operations-data bruges til at udfylde rapportsiderne i Power BI-indhold til **Omkostningsregnskabsanalyse**. Disse data repræsenteres som samlede målinger, der gemmes midlertidigt i enhedslageret, som er en Microsoft SQL-database, der er optimeret til analyse. Du kan finde flere oplysninger under [Oversigt over Power BI-integration med enhedslager](power-bi-integration-entity-store.md). Følgende samlede nøglemålinger bruges som grundlag for indholdet.

| Enhed                  | Samlede nøglemålinger | Datakilde til Dynamics 365 for Operations | Felt     | Betegnelse                                   |
|-------------------------|---------------------------|---------------------------------------------|-----------|-----------------------------------------------|
| Posteringer i omkostningsregnskab | SUM(Beløb)               | CAMDATAAggregatedCostEntry                  | Beløb    | Beløb i omkostningsregnskabets finanspostvaluta |
| Statistiske poster     | SUM(Størrelsesorden)            | CAMDATAAggregatedStatisctialEntry           | Størrelsesorden |                                               |

Følgende tabel viser, hvor de samlede nøglemålinger bruges til at oprette flere beregnede målepunkter i indholdets datasæt.

| Målepunkt                                       | Sådan beregnes målepunktet                                                                                          |
|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Faktisk omkostning                                   | CALCULATE('Posteringer i omkostningsregnskab'\[Målepunkt\], 'Versioner af transaktion'\[ISSOURCEVERSIONBUDGET\_VALUE\] = 0)            |
| Budgetterede omkostninger                                   | CALCULATE('Posteringer i omkostningsregnskab'\[Målepunkt\], 'Versioner af transaktion'\[ISSOURCEVERSIONBUDGET\_VALUE\] = 1)            |
| Budgetomkostningsafvigelse                          | \[Budgetterede omkostninger\] - \[Faktisk omkostning\]                                                                                      |
| Bugetafvigelsesprocent                    | IF(\[Budgetterede omkostninger\] = 0, blank(), \[Budgetafvigelse\] / \[Budgetterede omkostninger\])                                                |
| Faktisk størrelsesorden                              | CALCULATE('Statistiske poster'\[FullMagnitude\], 'Versioner af transaktion'\[ISSOURCEVERSIONBUDGET\_VALUE\] = 0)          |
| Størrelsesorden af budget                              | CALCULATE(\[FullMagnitude\], 'Versioner af transaktion'\[ISSOURCEVERSIONBUDGET\_VALUE\] = 1)                               |
| Statistisk budgetafvigelse                   | \[Størrelsesorden af budget\] - \[Faktisk størrelsesorden\]                                                                            |
| Statistisk bugetafvigelsesprocent        | IF(\[Størrelsesorden af budget\] = 0, blank(), \[Statistisk budgetafvigelse\] / \[Størrelsesorden af budget\])                          |
| Faktisk omkostningssats                              | IF(\[Faktisk størrelsesorden\] = 0, BLANK(), \[Faktisk omkostning\] / \[Faktisk størrelsesorden\])                                          |
| Budgetomkostningssats                              | IF(\[Størrelsesorden af budget\] = 0, BLANK(), \[Budgetterede omkostninger\] / \[Størrelsesorden af budget\])                                          |
| Afvigelse i budgetomkostningssats                     | \[Budgetomkostningssats\] - \[Faktisk omkostningssats\]                                                                            |
| Budgetomkostningssats i procent          | IF(\[Budgetterede omkostninger\] = 0, blank(), \[Afvigelse i budgetomkostningssats\] / \[Budgetomkostningssats\])                                 |
| Anlægsaktivomkostning                             | CALCULATE(\[Budgetterede omkostninger\], 'Posteringer i omkostningsregnskab'\[COSTBEHAVIOR\] = 1)                                              |
| Variabel budgetomkostning                          | CALCULATE(\[Budgetterede omkostninger\], 'Posteringer i omkostningsregnskab'\[COSTBEHAVIOR\] = 2)                                              |
| Fast fleksibel budgetomkostning                    | \[Anlægsaktivomkostning\]                                                                                                  |
| Variabel fleksibel budgetomkostning                 | IF(\[Størrelsesorden af budget\] = 0, BLANK(), (\[Variable budgetomkostninger\] / \[Størrelsesorden af budget\]) \* \[Faktisk størrelsesorden\])       |
| Fleksibel budgetomkostning                          | \[Fast fleksibel budgetomkostning\] + \[Variabel fleksibel budgetomkostning\]                                                     |
| Fleksibel budgetafvigelse                      | \[Fleksibel budgetomkostning\] - \[Faktisk omkostning\]                                                                             |
| Fleksibel bugetafvigelsesprocent           | IF(\[Fleksibel budgetomkostning\] = 0, BLANK(), \[Fleksibel budgetafvigelse\] / \[Fleksibel budgetomkostning\])                     |
| Fleksibel budgetomkostningssats                     | IF(\[Faktisk størrelsesorden\] = 0, BLANK(), \[Fleksibel budgetomkostning\] / \[Faktisk størrelsesorden\])                                 |
| Fleksibel afvigelse i budgetomkostningssats            | \[Fleksibel budgetomkostningssats\] - \[Faktisk omkostningssats\]                                                                   |
| Fleksibel budgetomkostningssats i procent | IF(\[Fleksibel budgetomkostningssats\] = 0, BLANK(), \[Fleksibel afvigelse i budgetomkostningssats\] / \[Fleksibel budgetomkostningssats\]) |

Følgende nøgledimensioner bruges som filtre til at skabe udsnit af de samlede målinger for at opnå større granularitet og give dybere analytisk indsigt.

| Enhed                             | Eksempler på attributter                                                                                               |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Finansposter for omkostningsregnskab            | Finanspost for omkostningsregnskab                                                                                               |
| Omkostningskontrolenheder                 | Navn på omkostningskontrolenhed                                                                                               |
| Dimensioner for omkostningselement            | Navn på dimension for omkostningselementer, navn på dimensionsmedlem af omkostningselement, beskrivelse af dimensionsmedlem af omkostningselement          |
| Dimensioner for omkostningsobjekt             | Navn på dimension for omkostningsobjekt, navn på dimensionsmedlem af omkostningsobjekt, beskrivelse af dimensionsmedlem af omkostningsobjekt              |
| Statistiske dimensioner             | Navn på statistisk dimension, navn på statistisk dimensionsmedlem, beskrivelse af statistisk dimensionsmedlem              |
| Dimensionshierarkier for omkostningsobjekt  | Navn på dimensionshierarki for omkostningsobjekt, niveau i dimensionshierarki for omkostningsobjekt, dimensionshierarkitræ for omkostningsobjekt    |
| Dimensionshierarkier for omkostningselement | Navn på dimensionshierarki for omkostningselement, niveau i dimensionshierarki for omkostningselement, dimensionshierarkitræ for omkostningselement |
| Statistiske dimensionshierarkier  | Navn på statistisk dimensionshierarki, niveau i statistisk dimensionshierarki, statistisk dimensionshierarkitræ    |
| Versioner af transaktion               | Versionsnavn                                                                                                         |
| Regnskabskalendere                   | Kalender, beskrivelse af kalender                                                                                       |
| Regnskabsår                       | Kalenderår                                                                                                        |
| Regnskabsperioder                     | Kalenderårperiode                                                                                                 |

## <a name="additional-resources"></a>Yderligere ressourcer
Her er nogle nyttige links, der er knyttet til enheder og oprettelse af Power BI-indhold:

-   [Dataenheder](..\data-entities\data-entities.md)
-   [Oprettelse af organisatoriske indholdspakker](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datamodellering i Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Tilføjelse af Power BI-felter til arbejdsområder](configure-power-bi-integration.md)
-   [Konfigurere sikkerhed for omkostningsregnskabsindhold til Power BI](setup-security-cost-accounting-content-pack.md)




