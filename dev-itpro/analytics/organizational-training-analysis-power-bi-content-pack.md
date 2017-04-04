---
title: "Organisatorisk oplæring strøm BI-indhold"
description: "Dette emne beskriver de Dynamics 365 for operationer - organisatorisk oplæring strøm BI-indhold. Det forklares, hvordan du få adgang til indhold pack og beskriver datamodel og enheder, der blev brugt til at opbygge indhold pack."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263874
ms.assetid: 45dbba14-aba6-4571-be0d-5d1aba3515d9
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 104164f8ffd0d2bc3a64bf15d2fb5213234046ce
ms.lasthandoff: 03/31/2017


---

# <a name="organizational-training-power-bi-content"></a>Organisatorisk oplæring strøm BI-indhold

Dette emne beskriver de Dynamics 365 for operationer - organisatorisk oplæring strøm BI-indhold. Det forklares, hvordan du få adgang til indhold pack og beskriver datamodel og enheder, der blev brugt til at opbygge indhold pack.

<a name="accessing-the-content-pack"></a>Adgang til indhold pack
--------------------------

Du kan finde den organisatoriske uddannelse indhold pack i biblioteket delte aktiver i Microsoft Dynamics livscyklus Services (LCS). Finde flere oplysninger om, hvordan du henter indhold pack og forbinde den til din Microsoft Dynamics-365 for operationer data [Power BI indhold i LCS fra Microsoft og dine partnere](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Rapporter, der er inkluderet i pakken med indhold
Når du har forbundet indhold pack til din Dynamics 365 til data af handlinger, Vis rapporter af virksomhedens data. Hvis du aldrig har brugt Microsoft Power BI før, kan du lære mere om det på den [automatiseret Learning side for strøm BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). De rapporter, der er inkluderet i pakken med indhold har både diagrammer og tabeller, der indeholder yderligere oplysninger. Rapporterne er beskrevet i følgende tabel.

| Rapport          | Indhold                                                                    |
|-----------------|-----------------------------------------------------------------------------|
| Analyse af kursus | Registrering af placering, kursus-deltagere ved status og registrering liste |
| Kursustyper.    | Kursustyper efter færdighed                                                       |

Du kan filtrere de diagrammer og fliser på disse rapporter og pin diagrammer og fliser til dashboardet. Finde flere oplysninger om filter og pinkode i Power BI [oprette og konfigurere en Dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Forståelse af datamodellen og enheder
Dynamics 365 for operationer data bruges til at udfylde rapporter i organisatorisk oplæring indhold pack. Følgende tabel viser enheder, indhold pack er baseret på.

| Enhed                    | Indhold                                                         | Relationer til andre objekter                                                                                                                                                                  |
|---------------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Uddannelse\_CalendarOffset  | Kalender forskydninger på udsnittet rapporter                                | Uddannelse\_CourseAgenda kursus\_CourseAttendees                                                                                                                                                   |
| Uddannelse\_virksomhed         | Virksomheder til at filtrere rapporter                                   | Uddannelse\_CourseAgenda kursus\_CourseAttendees                                                                                                                                                   |
| Uddannelse\_kursus          | Kursus, beskrivelse, instruktør navn, plads og status | Uddannelse\_CourseAgenda kursus\_CourseAttendees uddannelse\_CourseSkill                                                                                                                             |
| Uddannelse\_CourseAgenda    | Dagsordenen, kursus og start- og sluttidspunkter                          | Uddannelse\_uddannelse i firmaet\_CalendarOffset kursus\_dato uddannelse\_kursus                                                                                                                         |
| Uddannelse\_CourseAttendees | Dato for navn, status, job og registrering                         | Uddannelse\_uddannelse i firmaet\_CalendarOffset uddannelse\_dato uddannelse\_demografi uddannelse\_beskæftigelse uddannelse\_kursus uddannelse\_WorkerName uddannelse\_WorkerTitle uddannelse\_Job uddannelse\_Position |
| Uddannelse\_CourseSkill     | Færdighed, færdighedstype og niveau                                     | Uddannelse\_kursus                                                                                                                                                                                   |
| Uddannelse\_dato            | Dage, uger, måneder og år                                   | Uddannelse\_CourseAgenda kursus\_CourseAttendees                                                                                                                                                   |
| Uddannelse\_demografi    | Fødselsdato, køn, etnisk oprindelse og civilstand         | Uddannelse\_CourseAgenda kursus\_CourseAttendees                                                                                                                                                   |
| Uddannelse\_beskæftigelse      | Startdato, slutdato og datoen for overgang                        | Uddannelse\_CourseAgenda kursus\_CourseAttendees                                                                                                                                                   |
| Uddannelse\_sag             | Funktion, type og titel                                        | Uddannelse\_CourseAgenda kursus\_CourseAttendees                                                                                                                                                   |
| Uddannelse\_Position        | Placering, titel og tilsvarende fuld tid (Fuldtidsansatte)                  | Uddannelse\_CourseAgenda kursus\_CourseAttendees                                                                                                                                                   |
| Uddannelse\_WorkerName      | Fornavn, Efternavn og fulde navn                             | Uddannelse\_CourseAttendees                                                                                                                                                                          |
| Uddannelse\_WorkerTitle     | Titel og anciennitet                                         | Uddannelse\_CourseAttendees                                                                                                                                                                          |

Disse enheder blev brugt til at oprette beregnede målpunkter i datamodellen. Disse beregnes foranstaltninger bruges derefter til at beregne nøgletal (KPI'er) og rapporter, der bruges i indhold pack. Hvis du vil medtage yderligere beregninger på rapporter og dashboard, kan du hente og redigere filen Training.pbix fra Remburser. Denne fil er den standard datamodel, der blev brugt til at oprette indhold pack. Når du har foretaget ændringer, kan du oprette en organisatorisk indhold pack og dashboard, der indeholder de oplysninger, du har tilføjet.

## <a name="additional-resources"></a>Yderligere ressourcer
Her er nogle nyttige links, der er knyttet til enheder og oprettelse af Power BI-indhold:

-   [Dataenheder](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Oprettelse af organisatoriske indholdspakker](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datamodellering i Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Tilføjelse af Power BI-felter til arbejdsområder](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)



