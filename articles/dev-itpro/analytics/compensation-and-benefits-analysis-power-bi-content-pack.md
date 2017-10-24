---
title: Power BI-indhold til kompensation og frynsegoder
description: "I dette emne beskrives Finance and Operations – Power BI-indhold til kompensation og frynsegoder. Det beskrives, hvordan du får adgang til rapporter, der er inkluderet i indholdspakken, og indeholder oplysninger om den datamodel og de enheder, der blev brugt til at oprette indholdspakken."
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, UnifiedOperations
ms.custom: 263914
ms.assetid: 18634bb5-3341-42f2-9cc9-7b04708b506b
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: fbffad24350ae4650cd0d4142799c5e641dcdbe3
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="compensation-and-benefits-power-bi-content"></a>Power BI-indhold til kompensation og frynsegoder

[!include[banner](../includes/banner.md)]


I dette emne beskrives Finance and Operations – Power BI-indhold til kompensation og frynsegoder. Det beskrives, hvordan du får adgang til rapporter, der er inkluderet i indholdspakken, og indeholder oplysninger om den datamodel og de enheder, der blev brugt til at oprette indholdspakken.

<a name="accessing-the-content-pack"></a>Adgang til indholdspakken
--------------------------

Du kan finde indholdspakken til kompensation og frynsegoder i biblioteket Delte aktiver i Microsoft Dynamics Lifecycle Services (LCS). Du kan finde flere oplysninger om, hvordan du henter indholdspakken og forbinder den med dine Microsoft Dynamics-365 for Finance and Operations-data, under [Power BI indhold i LCS fra Microsoft og dine partnere](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Rapporter, der er inkluderet i indholdspakken
Når du har knyttet indholdspakken til dine data i Finance and Operations, viser rapporterne din organisations data. Hvis du aldrig har brugt Microsoft Power BI før, kan du finde oplysninger om det under [Guidet indføring i Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). De rapporter, der er inkluderet i indholdspakken, har både diagrammer og tabeller, der indeholder yderligere oplysninger. Rapporterne er beskrevet i følgende tabel.

| Rapport                     | Indhold                                                                                                                              |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Analyse af kompensation og frynsegoder | Timelønnede og fastansatte medarbejdere pr. virksomhed, gennemsnitlig timeløn, gennemsnitsløn for fastansatte, medarbejdere efter ansættelsestype og tilmelding til plan |
| Medarbejderfrynsegoder          | Medarbejdertilmeldning efter valgt frynsegode                                                                                               |

Du kan filtrere diagrammer og felter i alle disse rapporter og fastgøre dem til dashboardet. Du kan finde flere oplysninger om filtrering og fastgørelse i Power BI under [Oprette og konfigurere et dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Forståelse af datamodellen og enheder
Finance and Operations-data bruges til at udfylde rapporterne i indholdspakken til kompensation og frynsegoder. Følgende tabel viser de enheder, som indholdspakken er baseret på.

| Enhed                            | Indhold                                                                                                   | Relationer med andre enheder                                                                                                                                                                                                                                                                                                |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Workforce\_CalendarOffset         | Kalenderforskydninger for at opdele rapporter                                                                          | Workforce\_PastPositionAssignment Workforce\_PositionTrend Workorce\_WorkerTrend Workforce\_TerminatedWorker                                                                                                                                                                                                                     |
| Workforce\_Company                | Virksomheder, som rapporter kan filtreres efter                                                                             | Workforce\_CurrentCompensation Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                        |
| Workforce\_Compensation           | Lønsats og -frekvens over tid                                                                           | Workforce\_CurrentCompensation Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                        |
| Workforce\_CurrentCompensation    | Lønsats og -frekvens pr. dags dato                                                              | Workforce\_Company Workforce\_Compensation Workforce\_Demographics Workforce\_Job Workforce\_Position                                                                                                                                                                                                                            |
| Workforce\_CurrentPosition        | Stillinger pr. dags dato, tilsvarende fuldtidsstilling (fuldtidsansatte), ledige stillinger og ledige-til-bestatte stillinger | Workforce\_Job Workforce\_Position                                                                                                                                                                                                                                                                                               |
| Workforce\_CurrentWorker          | Arbejdere pr. den aktuelle dato, alder og antallet af beskæftigede                                                         | Workforce\_Company Workforce\_Compensation Workforce\_GeographicLocation Workforce\_Performance Workforce\_WorkerName Workforce\_ReportsToWorkerName Workforce\_WorkerTitle Workforce\_Demographics Workforce\_Job Workforce\_Employment Workforce\_Position Workforce\_WorkerBenefit                                            |
| Workforce\_Date                   | Dage, uger, måneder og år                                                                             | Workforce\_PastPositionAssignment Workforce\_PositionTrend Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                     |
| Workforce\_Demographics           | Fødselsdato, køn, etnisk oprindelse og civilstand                                                   | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workforce\_Employment             | Startdato, slutdato og overførselsdato                                                                  | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workforce\_GeographicLocation     | By, landsdel, postkode og stat eller provins                                                           | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workforce\_Job                    | Funktion, type og titel                                                                                  | Workforce\_CurrentPosition Workforce\_CurrentWorker                                                                                                                                                                                                                                                                              |
| Workforce\_PastPositionAssignment | Årsagen til tildelingen, startdato, slutdato og job                                                           | Workforce\_CalendarOffset Workforce\_Date Workforce\_Job Workforce\_Position                                                                                                                                                                                                                                                     |
| Workforce\_Performance            | Klassifikation, beskrivelse og klassifikationsmodel                                                                      | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workforce\_Position               | Afdeling, fuldtidsansat, stilling, stillingstype og titel                                                        | Workforce\_CurrentPosition Workforce\_CurrentWorker                                                                                                                                                                                                                                                                              |
| Workforce\_PositionTrend          | Stillinger over tid, fuldtidsansatte og job                                                                          | Workforce\_CalendarOffset Workforce\_Date Workforce\_Job Workforce\_Position                                                                                                                                                                                                                                                     |
| Workforce\_ReportsToWorkerName    | Fornavn, efternavn og fulde navn                                                                       | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workforce\_Skill                  | Færdighed, færdighedstype og klassifikation                                                                              |                                                                                                                                                                                                                                                                                                                                  |
| Workforce\_TerminatedWorker       | Fratrådte medarbejdere, fratrædelsesdato, titel, stilling og job                                             | Workforce\_Company Workforce\_Compensation Workforce\_GeographicLocation Workforce\_Performance Workforce\_WorkerName Workforce\_ReportsToWorkerName Workforce\_CalendarOffset Workforces\_Date Workforce\_WorkerTitle Workforce\_Demographics Workforce\_Employment Workforce\_Job Workforce\_Position Workforce\_WorkerBenefit |
| Workforce\_WorkerBenefit          | Ikrafttrædelsesdato, frynsegodeindstilling, frynsegodeplan og frynsegodetype                                             | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workforce\_WorkerName             | Fornavn, efternavn og fulde navn                                                                       | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workforce\_WorkerTitle            | Titel og anciennitetsdato                                                                                   | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workorce\_WorkerTrend             | Arbejdere over tid, beskæftigede, virksomhed og stilling                                                        | Workforce\_Company Workforce\_Compensation Workforce\_GeographicLocation Workforce\_Performance Workforce\_WorkerName Workforce\_ReportsToWorkerName Workforce\_CalendarOffset Workforces\_Date Workforce\_WorkerTitle Workforce\_Demographics Workforce\_Employment Workforce\_Job Workforce\_WorkerBenefit                     |

Disse enheder blev brugt til at oprette beregnede målinger i datamodellen. Disse beregnede mål bruges derefter til at beregne nøgletal (KPI'er) og rapporter, der bruges i indholdspakken. Hvis du vil medtage yderligere beregninger i rapporter og dashboard, kan du hente og redigere filen CompensationandBenefits.pbix fra LCS. Denne fil er den standarddatamodel, der blev brugt til at oprette indholdspakken. Når du har foretaget ændringerne, kan du oprette en indholdspakke og et dashboard for organisationen, som indeholder de oplysninger, du har tilføjet.

## <a name="additional-resources"></a>Yderligere ressourcer
Her er nogle nyttige links, der er knyttet til enheder og oprettelse af Power BI-indhold:

-   [Dataenheder](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Oprettelse af organisatoriske indholdspakker](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datamodellering i Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Tilføjelse af Power BI-felter til arbejdsområder](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





