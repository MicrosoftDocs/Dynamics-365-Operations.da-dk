---
title: Power BI-indhold til organisationsuddannelse
description: Dette emne beskriver Power BI-indhold til Finance and Operations – Oversigt over kontanter.
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 263874
ms.assetid: 45dbba14-aba6-4571-be0d-5d1aba3515d9
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: cd48c12ea3ea31904c437f678888a51e5381cfcfbeef0e1c709858b0c6cb857d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6763542"
---
# <a name="organizational-training-power-bi-content"></a>Power BI-indhold til organisationsuddannelse

[!include [banner](../includes/banner.md)]

Dette emne beskriver Power BI-indhold til Finance and Operations – Oversigt over kontanter.

## <a name="reports-that-are-included-in-the-content-pack"></a>Rapporter, der er inkluderet i indholdspakken
Når du har knyttet indholdspakken til dine data, viser rapporterne din organisations data. Hvis du aldrig har brugt Microsoft Power BI før, kan du finde oplysninger om det under [Guidet indføring i Power BI](https://powerbi.microsoft.com/guided-learning/?WT.mc_id=PBIService_GetData). De rapporter, der er inkluderet i indholdspakken, har både diagrammer og tabeller, der indeholder yderligere oplysninger. Rapporterne er beskrevet i følgende tabel.

| Rapport          | Indhold                                                                    |
|-----------------|-----------------------------------------------------------------------------|
| Analyse af kursus | Registrering efter lokalitet, kursusdeltagere efter status og registreringsliste |
| Kursustyper    | Kursustyper efter færdighed                                                       |

Du kan filtrere diagrammer og felter i alle disse rapporter og fastgøre dem til dashboardet. Du kan finde flere oplysninger om filtrering og fastgørelse i Power BI under [Oprette og konfigurere et dashboard](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Forståelse af datamodellen og enheder
Programdata bruges til at udfylde rapporterne i indholdspakken til organisatorisk uddannelse. Følgende tabel viser de enheder, som indholdspakken er baseret på.

| Enhed                    | Indhold                                                         | Relationer med andre enheder |
|---------------------------|------------------------------------------------------------------|-----------------------------------|
| Training\_CalendarOffset  | Kalenderforskydninger for at opdele rapporter                                | Training\_CourseAgenda, Training\_CourseAttendees |
| Training\_Company         | Virksomheder, som rapporter kan filtreres efter                                   | Training\_CourseAgenda, Training\_CourseAttendees |
| Training\_Course          | Kursus, beskrivelse, instruktørnavn, lokalitet, værelse og status | Training\_CourseAgenda, Training\_CourseAttendees, Training\_CourseSkill |
| Training\_CourseAgenda    | Agenda, kursus og start- og sluttidspunkter                          | Training\_Company, Training\_CalendarOffset, Training\_Date, Training\_Course |
| Training\_CourseAttendees | Navn, status, job og registreringsdato                         | Training\_Company, Training\_CalendarOffset, Training\_Date, Training\_Demographics, Training\_Employment, Training\_Course, Training\_WorkerName, Training\_WorkerTitle, Training\_Job, Training\_Position |
| Training\_CourseSkill     | Færdighed, færdighedstype og niveau                                     | Training\_Course |
| Training\_Date            | Dage, uger, måneder og år                                   | Training\_CourseAgenda, Training\_CourseAttendees |
| Training\_Demographics    | Fødselsdato, køn, etnisk oprindelse og civilstand         | Training\_CourseAgenda, Training\_CourseAttendees |
| Training\_Employment      | Startdato, slutdato og overførselsdato                        | Training\_CourseAgenda, Training\_CourseAttendees |
| Training\_Job             | Funktion, type og titel                                        | Training\_CourseAgenda, Training\_CourseAttendees |
| Training\_Position        | Stilling, titel og tilsvarende fuld tid (fuldtidsansat)                  | Training\_CourseAgenda, Training\_CourseAttendees |
| Training\_WorkerName      | Fornavn, efternavn og fulde navn                             | Training\_CourseAttendees |
| Training\_WorkerTitle     | Titel og anciennitetsdato                                         | Training\_CourseAttendees |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]