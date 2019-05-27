---
title: Power BI-indhold til medarbejderkompetencer og -udvikling
description: I dette emne beskrives Finance and Operations – Power BI-indhold til medarbejderkompetencer og -udvikling.
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 263894
ms.assetid: 7d375d8a-b2de-4bec-b575-93d1d4521b79
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 0442e795eadf28a07132c160d69ad44e9fb05eed
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1553271"
---
# <a name="employee-competencies-and-development-power-bi-content"></a>Power BI-indhold til medarbejderkompetencer og -udvikling

[!include [banner](../includes/banner.md)]

I dette emne beskrives Finance and Operations – Power BI-indhold til medarbejderkompetencer og -udvikling. 

## <a name="reports-that-are-included-in-the-content-pack"></a>Rapporter, der er inkluderet i indholdspakken
Når du har knyttet indholdspakken til dine data i Finance and Operations, viser rapporterne din organisations data. Hvis du aldrig har brugt Microsoft Power BI før, kan du finde oplysninger om det under [Guidet indføring i Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). De rapporter, der er inkluderet i indholdspakken, har både diagrammer og tabeller, der indeholder yderligere oplysninger. Rapporterne er beskrevet i følgende tabel.

| Rapport                            | Indhold                                               |
|-----------------------------------|--------------------------------------------------------|
| Kompetence- og udviklingsanalyse | Teammedlem-færdighedstyper og teammedlem-færdigheder efter type |
| Færdighedsprofil                     | Færdighedsprofil for den valgte medarbejder                |
| Kompetenceanalyse                    | Færdigheder efter type og klassifikation                              |

Du kan filtrere diagrammer og felter i alle disse rapporter og fastgøre dem til dashboardet. Du kan finde flere oplysninger om filtrering og fastgørelse i Power BI under [Oprette og konfigurere et dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Forståelse af datamodellen og enheder
Finance and Operations-data bruges til at udfylde rapporterne i indholdspakken til medarbejderkompensation og -udvikling. Følgende tabel viser de enheder, som indholdspakken er baseret på.

| Enhed                            | Indhold                                                                                                   | Relationer med andre enheder |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Workforce\_CalendarOffset         | Kalenderforskydninger for at opdele rapporter                                                                          | |
| Workforce\_Company                | Virksomheder, som rapporter kan filtreres efter                                                                             | |
| Workforce\_Compensation           | Lønsats og -frekvens over tid                                                                           | |
| Workforce\_CurrentCompensation    | Lønsats og -frekvens pr. dags dato                                                              | Workforce\_Company, Workforce\_CurrentCompensation, Workforce\_Demographics, Workforce\_Job, Workforce\_Position |
| Workforce\_CurrentPosition        | Stillinger pr. dags dato, tilsvarende fuldtidsstilling (fuldtidsansatte), ledige stillinger og ledige-til-bestatte stillinger | Workforce\_Job Workforce\_Position |
| Workforce\_CurrentWorker          | Arbejdere pr. den aktuelle dato, alder og antallet af beskæftigede                                                         | Workforce\_Company Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_PersonSkill, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Job, Workforce\_Employment, Workforce\_Position |
| Workforce\_Date                   | Dage, uger, måneder og år                                                                             | |
| Workforce\_Demographics           | Fødselsdato, køn, etnisk oprindelse og civilstand                                                   | |
| Workforce\_Employment             | Startdato, slutdato og overførselsdato                                                                  | |
| Workforce\_GeographicLocation     | By, landsdel, postkode og stat eller provins                                                           | |
| Workforce\_Job                    | Funktion, type og titel                                                                                  | |
| Workforce\_JobPreferredSkill      | Prioritet, klassifikation, kompetence og færdighedsniveau                                                                 | Workforce\_Skill, Workforce\_Job |
| Workforce\_PastPositionAssignment | Årsagen til tildelingen, startdato, slutdato og job                                                           | Workforce\_CalendarOffset, Workforce\_Date, Workforce\_Job, Workforce\_Position |
| Workforce\_Performance            | Klassifikation, beskrivelse og klassifikationsmodel                                                                      | |
| Workforce\_PersonSkill            | Niveau, niveau dato og færdighed                                                                               | Workforce\_Skill |
| Workforce\_PersonSkillAnalysis    | Certificeret, niveau, niveaudato og færdighed                                                                    | Workforce\_WorkerName, Workforce\_Skill |
| Workforce\_Position               | Afdeling, fuldtidsansat, stilling, stillingstype og titel                                                        | |
| Workforce\_PositionTrend          | Stillinger over tid, fuldtidsansatte og job                                                                          | Workforce\_CalendarOffset, Workforce\_Date, Workforce\_Job, Workforce\_Position |
| Workforce\_ReportsToWorkerName    | Fornavn, efternavn og fulde navn                                                                       | |
| Workforce\_Skill                  | Færdighed, færdighedstype og klassifikation                                                                              | |
| Workforce\_TerminatedWorker       | Fratrådte medarbejdere, fratrædelsesdato, titel, stilling og job                                             | Workforce\_Company, Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_CalendarOffset, Workforces\_Date, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Employment, Workforce\_Job, Workforce\_Position |
| Workforce\_WorkerName             | Fornavn, efternavn og fulde navn                                                                       | |
| Workforce\_WorkerTitle            | Titel og anciennitetsdato                                                                                   | |
| Workorce\_WorkerTrend             | Arbejdere over tid, beskæftigede, virksomhed og stilling                                                        | Workforce\_Company, Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_CalendarOffset, Workforces\_Date, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Employment, Workforce\_Job |
