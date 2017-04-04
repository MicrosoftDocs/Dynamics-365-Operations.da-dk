---
title: "Medarbejderens kompetencer og udvikling strøm BI indhold"
description: "Dette emne beskriver de Dynamics 365 for operationer - medarbejderens kompetencer og udvikling strøm BI-indhold. Det forklarer, hvordan du kan få adgang til rapporter, der er inkluderet i pakken med indhold og indeholder oplysninger om datamodel og enheder, der blev brugt til at opbygge indhold pack."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263894
ms.assetid: 7d375d8a-b2de-4bec-b575-93d1d4521b79
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 1fd6f978b6a871f9f7d3d5e91ab3e0aac789ae88
ms.lasthandoff: 03/31/2017


---

# <a name="employee-competencies-and-development-power-bi-content"></a>Medarbejderens kompetencer og udvikling strøm BI indhold

Dette emne beskriver de Dynamics 365 for operationer - medarbejderens kompetencer og udvikling strøm BI-indhold. Det forklarer, hvordan du kan få adgang til rapporter, der er inkluderet i pakken med indhold og indeholder oplysninger om datamodel og enheder, der blev brugt til at opbygge indhold pack.

<a name="accessing-the-content-pack"></a>Adgang til indhold pack
--------------------------

Du kan finde på medarbejderens kompetencer og udvikling indhold pack i biblioteket delte aktiver i Microsoft Dynamics livscyklus Services (LCS). Finde flere oplysninger om, hvordan du henter indhold pack og forbinde den til din Microsoft Dynamics-365 for operationer data [Power BI indhold i LCS fra Microsoft og dine partnere](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Rapporter, der er inkluderet i pakken med indhold
Når du har forbundet indhold pack til din Dynamics 365 til data af handlinger, Vis rapporter af virksomhedens data. Hvis du aldrig har brugt Microsoft Power BI før, kan du lære mere om det på den [automatiseret Learning side for strøm BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). De rapporter, der er inkluderet i pakken med indhold har både diagrammer og tabeller, der indeholder yderligere oplysninger. Rapporterne er beskrevet i følgende tabel.

| Rapport                            | Indhold                                               |
|-----------------------------------|--------------------------------------------------------|
| Kompetencer og udvikling analyse | Team medlem færdighedstyper og færdigheder til medlem af team efter type |
| Kompetenceprofil                     | Kompetenceprofil og profilen for den valgte medarbejder                |
| Analyse af færdighed                    | Færdigheder efter type og vurdering                              |

Du kan filtrere de diagrammer og fliser på disse rapporter og pin diagrammer og fliser til dashboardet. Finde flere oplysninger om filter og pinkode i Power BI [oprette og konfigurere en Dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Forståelse af datamodellen og enheder
Dynamics 365 for operationer data bruges til at udfylde rapporter i medarbejderens kompetencer og udvikling indhold pack. Følgende tabel viser enheder, indhold pack er baseret på.

| Enhed                            | Indhold                                                                                                   | Relationer til andre objekter                                                                                                                                                                                                                                                                       |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Arbejdsstyrken\_CalendarOffset         | Kalender forskydninger på udsnittet rapporter                                                                          |                                                                                                                                                                                                                                                                                                         |
| Arbejdsstyrken\_virksomhed                | Virksomheder til at filtrere rapporter                                                                             |                                                                                                                                                                                                                                                                                                         |
| Arbejdsstyrken\_løn           | Lønsats og ofte over tid                                                                           |                                                                                                                                                                                                                                                                                                         |
| Arbejdsstyrken\_CurrentCompensation    | Lønsats og frekvens til dags dato                                                              | Arbejdsstyrken\_medarbejdere i firmaet\_CurrentCompensation arbejdsstyrke\_demografi arbejdsstyrke\_Job arbejdsstyrke\_Position                                                                                                                                                                                            |
| Arbejdsstyrken\_CurrentPosition        | Stillinger pr. dags dato, tilsvarende fuld tid (Fuldtidsansatte), åbne stillinger, og stillinger, der er åben til fyldt | Arbejdsstyrken\_Job arbejdsstyrke\_Position                                                                                                                                                                                                                                                                      |
| Arbejdsstyrken\_CurrentWorker          | Arbejdere på den aktuelle dato, alder og antallet af ansatte                                                         | Arbejdsstyrken\_medarbejdere i firmaet\_løn arbejdsstyrke\_GeographicLocation arbejdsstyrke\_ydeevne arbejdsstyrke\_PersonSkill arbejdsstyrke\_WorkerName arbejdsstyrke\_ReportsToWorkerName arbejdsstyrke\_WorkerTitle arbejdsstyrke\_demografi arbejdsstyrke\_Job arbejdsstyrke\_beskæftigelse af arbejdsstyrken\_Position                     |
| Arbejdsstyrken\_dato                   | Dage, uger, måneder og år                                                                             |                                                                                                                                                                                                                                                                                                         |
| Arbejdsstyrken\_demografi           | Fødselsdato, køn, etnisk oprindelse og civilstand                                                   |                                                                                                                                                                                                                                                                                                         |
| Arbejdsstyrken\_beskæftigelse             | Startdato, slutdato og datoen for overgang                                                                  |                                                                                                                                                                                                                                                                                                         |
| Arbejdsstyrken\_GeographicLocation     | By, landsdel, postal code, og stat eller provins                                                           |                                                                                                                                                                                                                                                                                                         |
| Arbejdsstyrken\_sag                    | Funktion, type og titel                                                                                  |                                                                                                                                                                                                                                                                                                         |
| Arbejdsstyrken\_JobPreferredSkill      | Prioritet, klassifikation, kompetence og færdigheder                                                                 | Arbejdsstyrken\_færdighed arbejdsstyrke\_sag                                                                                                                                                                                                                                                                         |
| Arbejdsstyrken\_PastPositionAssignment | Årsagen til tildelingen, startdato, slutdato og job                                                           | Arbejdsstyrken\_ClaendarOffset arbejdsstyrke\_dato arbejdsstyrke\_Job arbejdsstyrke\_Position                                                                                                                                                                                                                            |
| Arbejdsstyrken\_ydeevne            | Klassifikation, beskrivelse og rangeringsmodel                                                                      |                                                                                                                                                                                                                                                                                                         |
| Arbejdsstyrken\_PersonSkill            | Niveau, niveau dato og færdigheder                                                                               | Arbejdsstyrken\_færdighed                                                                                                                                                                                                                                                                                        |
| Arbejdsstyrken\_PersonSkillAnalysis    | Certificeret, niveauer, niveau dato og færdigheder                                                                    | Arbejdsstyrken\_WorkerName arbejdsstyrke\_færdighed                                                                                                                                                                                                                                                                  |
| Arbejdsstyrken\_Position               | Afdeling, Fuldtidsansatte, stilling, stillingstype og titel                                                        |                                                                                                                                                                                                                                                                                                         |
| Arbejdsstyrken\_PositionTrend          | Positioner i forhold til tid, Fuldtidsansatte og job                                                                          | Arbejdsstyrken\_CalendarOffset arbejdsstyrke\_dato arbejdsstyrke\_Job arbejdsstyrke\_Position                                                                                                                                                                                                                            |
| Arbejdsstyrken\_ReportsToWorkerName    | Fornavn, Efternavn og fulde navn                                                                       |                                                                                                                                                                                                                                                                                                         |
| Arbejdsstyrken\_færdighed                  | Færdighed, færdighedstype og vurdering                                                                              |                                                                                                                                                                                                                                                                                                         |
| Arbejdsstyrken\_TerminatedWorker       | Fratrådte medarbejdere, Fratrædelsesdato, titel, position og job                                             | Arbejdsstyrken\_medarbejdere i firmaet\_løn arbejdsstyrke\_GeographicLocation arbejdsstyrke\_ydeevne arbejdsstyrke\_WorkerName arbejdsstyrke\_ReportsToWorkerName arbejdsstyrke\_CalendarOffset arbejdsstyrker\_dato arbejdsstyrke\_WorkerTitle arbejdsstyrke\_demografi arbejdsstyrke\_beskæftigelse af arbejdsstyrken\_Job arbejdsstyrke\_Position |
| Arbejdsstyrken\_WorkerName             | Fornavn, Efternavn og fulde navn                                                                       |                                                                                                                                                                                                                                                                                                         |
| Arbejdsstyrken\_WorkerTitle            | Titel og anciennitet                                                                                   |                                                                                                                                                                                                                                                                                                         |
| Workorce\_WorkerTrend             | Arbejdere over tid, beskæftigede, virksomhed og placering                                                        | Arbejdsstyrken\_medarbejdere i firmaet\_kompensation arbejdsstyrke\_GeographicLocation arbejdsstyrke\_ydeevne arbejdsstyrke\_WorkerName arbejdsstyrke\_ReportsToWorkerName arbejdsstyrke\_CalendarOffset arbejdsstyrker\_dato arbejdsstyrke\_WorkerTitle arbejdsstyrke\_demografi arbejdsstyrke\_beskæftigelse af arbejdsstyrken\_sag                     |

Disse enheder blev brugt til at oprette beregnede målpunkter i datamodellen. Disse beregnes foranstaltninger bruges derefter til at beregne nøgletal (KPI'er) og rapporter, der bruges i indhold pack. Hvis du vil medtage yderligere beregninger på rapporter og dashboard, kan du hente og redigere filen CompetenciesandDevelopment.pbix fra Remburser. Denne fil er den standard datamodel, der blev brugt til at oprette indhold pack. Når du har foretaget ændringer, kan du oprette en organisatorisk indhold pack og dashboard, der indeholder de oplysninger, du har tilføjet.

## <a name="additional-resources"></a>Yderligere ressourcer
Her er nogle nyttige links, der er knyttet til enheder og oprettelse af Power BI-indhold:

-   [Dataenheder](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Oprettelse af organisatoriske indholdspakker](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datamodellering i Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Tilføjelse af Power BI-felter til arbejdsområder](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)



