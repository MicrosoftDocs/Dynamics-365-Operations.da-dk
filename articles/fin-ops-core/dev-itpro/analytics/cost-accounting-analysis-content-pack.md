---
title: Power BI-indhold til omkostningsregnskabsanalyse
description: Denne artikel beskriver, hvad der skal medtages i Power BI-indhold til omkostningsregnskabsanalyse.
author: AndersGirke
ms.date: 10/02/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 270274
ms.assetid: b74549df-35d5-4f2f-b3c7-405b0d38ea78
ms.openlocfilehash: 7339d0abf8d087ca8fcc8f46dc91a5e78ec0f325
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269719"
---
# <a name="cost-accounting-analysis-power-bi-content"></a>Power BI-indhold til omkostningsregnskabsanalyse

[!include [banner](../includes/banner.md)]

Denne artikel beskriver, hvad der skal medtages i Microsoft Power BI-indhold til **Omkostningsregnskabsanalyse**. Det beskrives, hvordan du får adgang til Power BI-rapporter, og der er oplysninger om den datamodel og de enheder, der blev brugt til at oprette indholdspakken.

## <a name="overview"></a>Overblik

Power BI-indholdet til **Omkostningsregnskabsanalyse** er beregnet til omkostningscontrollere eller andre, der er ansvarlige for udførelse af en organisations omkostningsstyring. Det indeholder oversigt over målepunkter som omkostning, størrelsesorden og omkostningssats ved faktisk omkostning, budgetomkostninger og fleksible budgetomkostninger. Det bruger transaktionsdata fra modulet **Omkostningsregnskab** og giver en samlet oversigt over omkostninger for hele organisationen i én rapporteringsvaluta. Ledere kan filtrere dataene efter omkostningsobjekter for at udføre omkostningsstyring af deres organisatoriske enheder, selv om organisationen kan have flere juridiske enheder.

Da indholdet til **Omkostningsregnskabsanalyse** fremhæver afvigelser mellem de faktiske omkostninger og budgetterede omkostninger, kan ledere blive informeret om positive og negative tendenser for deres driftsenheder. Ledere kan dykke ned i omkostningselementhierarkierne eller individuelle omkostningselementer. På denne måde kan ledere få detaljeret indsigt i, hvordan omkostningsafvigelser er opstået, og kan derefter handle effektivt.

Med indholdet til **Omkostningsregnskabsanalyse** kan bogholdere analysere, hvordan omkostninger flyder gennem omkostningsobjekter i hele organisationen.

Du kan finde flere oplysninger om omkostningsregnskabet i [Startside for omkostningsregnskab](../../../finance/cost-accounting/cost-accounting-home-page.md).

Ved at definere sikkerhed på brugerniveau i omkostningsregnskabet og kombinere det med sikkerhed på rækkeniveau i Power BI kan du tildele alle omkostningsobjektejere adgang til Power BI-indholdet til **Omkostningsregnskabsanalyse**. Alle data i visualiseringerne filtreres derefter baseret på det adgangsniveau, der styres i omkostningsregnskabet. Hvis du vil vide mere om sikkerhed på henholdsvis adgangsniveau og rækkeniveau, kan du finde flere oplysninger under [Konfigurer sikkerhed for Power BI-indholdet i analysen af Omkostningsregnskab](setup-security-cost-accounting-content-pack.md).

## <a name="accessing-the-power-bi-content"></a>Adgang til Power BI-indholdet
Du kan finde Power BI-indholdet til **Omkostningsregnskabsanalyse** i biblioteket Delte aktiver i Microsoft Dynamics Lifecycle Services (LCS). Du kan finde flere oplysninger om, hvordan du downloader indhold og implementerer det i din organisation, under [Power BI-indhold i LCS fra Microsoft og dine partnere](/archive/blogs/dynamicsaxbi/power-bi-content-from-microsoft-and-your-partners).

Sørg for at downloade det **Omkostningsregnskabsanalyse**-indhold, der gælder for den version af Microsoft Dynamics 365, du bruger.

> [!NOTE]
> KB 4011327 er en forudsætning for dette Power BI-indhold. Når du logger på LCS, du har adgang til KB her på <https://fix.lcs.dynamics.com/issue/results/?q=kb4011327>.

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Metrikker, der er inkluderet i Power BI-indholdet
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
Følgende data bruges til at udfylde rapportsiderne i Power BI-indholdet til **Omkostningsregnskabsanalyse**. Disse data repræsenteres som samlede målinger, der er klargjort i enhedslageret. Enhedslageret er en Microsoft SQL Server-database, der er optimeret til analyser. Du kan finde flere oplysninger under [Power BI-integration med Enhedslager](power-bi-integration-entity-store.md).

Følgende samlede nøglemålinger bruges som grundlag for indholdet.

| Enhed                  | Samlede nøglemålinger | Datakilden til Dynamics 365      | Felt     | Betegnelse                                        |
|-------------------------|---------------------------|-----------------------------------|-----------|----------------------------------------------------|
| Posteringer i omkostningsregnskab | SUM(Beløb)               | CAMDATAAggregatedCostEntry        | Beløb    | Beløbet i omkostningsregnskabets finanspostvaluta. |
| Statistiske poster     | SUM(Størrelsesorden)            | CAMDATAAggregatedStatisctialEntry | Størrelsesorden |                                                    |

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
