---
title: "Rekruttering strøm BI-indhold"
description: "Dette emne beskriver de Dynamics 365 for operationer - rekruttering strøm BI-indhold. Det forklarer, hvordan du kan få adgang til rapporter, der er inkluderet i pakken med indhold og indeholder oplysninger om datamodel og enheder, der blev brugt til at opbygge indhold pack."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263934
ms.assetid: 38e6827b-0819-473c-bc47-821a1ec482b8
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: d307733193b388149f83dd420cc7003edcf7749a
ms.lasthandoff: 03/31/2017


---

# <a name="recruiting-power-bi-content"></a>Rekruttering strøm BI-indhold

Dette emne beskriver de Dynamics 365 for operationer - rekruttering strøm BI-indhold. Det forklarer, hvordan du kan få adgang til rapporter, der er inkluderet i pakken med indhold og indeholder oplysninger om datamodel og enheder, der blev brugt til at opbygge indhold pack.

<a name="accessing-the-content-pack"></a>Adgang til indhold pack
--------------------------

Du kan finde det indhold pack rekruttering i biblioteket delte aktiver i Microsoft Dynamics livscyklus Services (LCS). Finde flere oplysninger om, hvordan du henter indhold pack og forbinde den til din Microsoft Dynamics-365 for operationer data [Power BI indhold i LCS fra Microsoft og dine partnere](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Rapporter, der er inkluderet i pakken med indhold
Når du har forbundet indhold pack til din Dynamics 365 til data af handlinger, Vis rapporter af virksomhedens data. Hvis du aldrig har brugt Microsoft Power BI før, kan du lære mere om det på den [automatiseret Learning side for strøm BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). De rapporter, der er inkluderet i pakken med indhold har både diagrammer og tabeller, der indeholder yderligere oplysninger. Rapporterne er beskrevet i følgende tabel.

| Rapport                       | Indhold                                                                                               |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| Analyse af ansøgeren           | Ansøgere efter job, ansøgeren kilder, ansøgere ved placering og det samlede antal ansøgere           |
| Ansøgeren Status             | Ansøgere efter type og status og status for ansøger                                                    |
| Ansøgeren demografi       | Ansøgere efter alder og køn og ansøgere efter uddannelsesniveau og status                             |
| Rekruttering analyse          | Netto leje forholdet, gennemsnitlig dage til at ansætte procentdel af dårlige ansættelser og rekruttering omkostninger                    |
| Ansættelse projektanalyse | Antallet af rekrutteringsprojekter, åbninger af rekrutteringsprojektet, og ansøgere efter rekrutteringsprojekt |

Du kan filtrere de diagrammer og fliser på disse rapporter og pin diagrammer og fliser til dashboardet. Finde flere oplysninger om filter og pinkode i Power BI [oprette og konfigurere en Dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Forståelse af datamodellen og enheder
Dynamics 365 for operationer data bruges til at udfylde rapporter i rekruttering indhold pack. Følgende tabel viser enheder, indhold pack er baseret på.

| Enhed                          | Indhold                                                         | Relationer til andre objekter                                                                                                                                                                                                                 |
|---------------------------------|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Rekruttering\_ansøger           | Ansøgere, ansatte ansøgere, forholdet mellem net leje og omkostninger          | Rekruttering\_ApplicantName rekruttering\_virksomhed rekrutterer\_CalendarOffset Recuriting\_dato rekruttering\_GeographicLocation rekruttering\_demografi rekruttering\_Job rekruttering\_Media rekruttering\_RecruitmentProject                                |
| Rekruttering\_ApplicantName       | Ansøgerens fornavn, Efternavn og fulde navn                   | Rekruttering\_ansøgeren rekruttering\_rekruttering EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Rekruttering\_CalendarOffset      | Kalender forskydninger på udsnittet rapporter                                | Rekruttering\_ansøgeren rekruttering\_rekruttering EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Rekruttering\_virksomhed             | Virksomheder til at filtrere rapporter                                   | Rekruttering\_ansøgeren rekruttering\_rekruttering EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Rekruttering\_dato                | Dage, uger, måneder og år                                   | Rekruttering\_ansøgeren rekruttering\_rekruttering EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Rekruttering\_demografi        | Fødselsdato, køn, etnisk oprindelse og civilstand         | Rekruttering\_ansøgeren rekruttering\_rekruttering EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Rekruttering\_EmployedApplicant   | Ansøgeren, ydeevne, startdato og ansøgeren type           | Rekruttering\_virksomhed rekrutterer\_CalendarOffset rekruttering\_dato rekruttering\_rekruttering GeographicLocation\_ApplicantName rekruttering\_beskæftigelse rekruttering\_ydeevne rekruttering\_Job rekruttering\_Media rekruttering\_RecruitmentProject          |
| Rekruttering\_beskæftigelse          | Startdato, slutdato og datoen for overgang                        | Rekruttering\_ansøgeren rekruttering\_rekruttering EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Rekruttering\_GeographicLocation  | By, landsdel, postal code, og stat eller provins                 | Rekruttering\_ansøgeren rekruttering\_rekruttering EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Rekruttering\_sag                 | Funktion, type og titel                                        | Rekruttering\_ansøgeren rekruttering\_rekruttering EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Rekruttering\_medier               | Kilden til ansøgere                                             | Rekruttering\_ansøgeren rekruttering\_rekruttering EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Rekruttering\_ydeevne         | Klassifikation, beskrivelse og rangeringsmodel                            | Rekruttering\_ansøgeren rekruttering\_rekruttering EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Rekruttering\_RecruitmentProject  | Beskrivelse af projektet, projektstatus og åbninger                | Rekruttering\_ansøgeren rekruttering\_rekruttering EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Rekruttering\_TerminatedApplicant | Afsluttet ansøgere, årsag, ydeevne og Fratrædelsesdato | Rekruttering\_firma rekruttering\_CalendarOffset rekruttering\_dato rekruttering\_GeographicLocation rekruttering\_ydeevne rekruttering\_demografi rekruttering\_beskæftigelse rekruttering\_Media rekruttering\_rekruttering RecruitmentProject\_ApplicantName |

Disse enheder blev brugt til at oprette beregnede målpunkter. Disse beregnes foranstaltninger bruges derefter til at beregne nøgletal (KPI'er) og rapporter, der bruges i indhold pack. Hvis du vil medtage yderligere beregninger på rapporter og dashboard, kan du hente og redigere filen Recruiting.pbix fra Remburser. Denne fil er den standard datamodel, der blev brugt til at oprette indhold pack. Når du har foretaget ændringer, kan du oprette en organisatorisk indhold pack og dashboard, der indeholder de oplysninger, du har tilføjet.

## <a name="additional-resources"></a>Yderligere ressourcer
Her er nogle nyttige links, der er knyttet til enheder og oprettelse af Power BI-indhold:

-   [Dataenheder](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Oprettelse af organisatoriske indholdspakker](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datamodellering i Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Tilføjelse af Power BI-felter til arbejdsområder](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)



