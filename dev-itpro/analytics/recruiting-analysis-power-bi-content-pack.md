---
title: Power BI-indhold til rekruttering
description: "Dette emne beskriver Dynamics 365 for Operations – Power BI-indhold til rekruttering. Det beskrives, hvordan du får adgang til rapporter, der er inkluderet i indholdspakken, og indeholder oplysninger om den datamodel og de enheder, der blev brugt til at oprette indholdspakken."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263934
ms.assetid: 38e6827b-0819-473c-bc47-821a1ec482b8
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 4b12a2c8983cf7bef770417f76df324293f06fb2
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="recruiting-power-bi-content"></a>Power BI-indhold til rekruttering

[!include[banner](../includes/banner.md)]


Dette emne beskriver Dynamics 365 for Operations – Power BI-indhold til rekruttering. Det beskrives, hvordan du får adgang til rapporter, der er inkluderet i indholdspakken, og indeholder oplysninger om den datamodel og de enheder, der blev brugt til at oprette indholdspakken.

<a name="accessing-the-content-pack"></a>Adgang til indholdspakken
--------------------------

Du kan finde indholdspakken til rekruttering i biblioteket Delte aktiver i Microsoft Dynamics Lifecycle Services (LCS). Du kan finde flere oplysninger om, hvordan du henter indholdspakken og forbinder den med dine Microsoft Dynamics-365 for Operations-data, under [Power BI indhold i LCS fra Microsoft og dine partnere](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Rapporter, der er inkluderet i indholdspakken
Når du har knyttet indholdspakken til dine data i Dynamics 365 for Operations, viser rapporterne din organisations data. Hvis du aldrig har brugt Microsoft Power BI før, kan du finde oplysninger om det under [Guidet indføring i Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). De rapporter, der er inkluderet i indholdspakken, har både diagrammer og tabeller, der indeholder yderligere oplysninger. Rapporterne er beskrevet i følgende tabel.

| Rapport                       | Indhold                                                                                               |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| Ansøgeranalyse           | Ansøgere efter job, ansøgningskilder, ansøgere efter lokalitet og det samlede antal ansøgere           |
| Ansøgerstatus             | Ansøgere efter type og status og ansøgerstatus                                                    |
| Ansøgerdemografi       | Ansøgere efter alder og køn og ansøgere efter uddannelsesniveau og status                             |
| Rekrutteringsanalyse          | Nettoansættelsesforhold, gennemsnitlig antal dage til ansættelse, procentdel af dårlige ansættelser og rekrutteringsomkostninger                    |
| Analyse af rekrutteringsprojekt | Antallet af rekrutteringsprojekter, åbninger efter rekrutteringsprojekt og ansøgere efter rekrutteringsprojekt |

Du kan filtrere diagrammer og felter i alle disse rapporter og fastgøre dem til dashboardet. Du kan finde flere oplysninger om filtrering og fastgørelse i Power BI under [Oprette og konfigurere et dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Forståelse af datamodellen og enheder
Dynamics 365 for Operations-data bruges til at udfylde rapporterne i indholdspakken til rekruttering. Følgende tabel viser de enheder, som indholdspakken er baseret på.

| Enhed                          | Indhold                                                         | Relationer med andre enheder                                                                                                                                                                                                                 |
|---------------------------------|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Recruiting\_Applicant           | Ansøgere, ansatte ansøgere, nettoansættelsesforhold og omkostninger          | Recruiting\_ApplicantName Recruiting\_Company Recruiting\_CalendarOffset Recuriting\_Date Recruiting\_GeographicLocation Recruiting\_Demographics Recruiting\_Job Recruiting\_Media Recruiting\_RecruitmentProject                                |
| Recruiting\_ApplicantName       | Ansøgers fornavn, efternavn og fulde navn                   | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_CalendarOffset      | Kalenderforskydninger for at opdele rapporter                                | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Company             | Virksomheder, som rapporter kan filtreres efter                                   | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Date                | Dage, uger, måneder og år                                   | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Demographics        | Fødselsdato, køn, etnisk oprindelse og civilstand         | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_EmployedApplicant   | Ansøger, performance, startdato og ansøgertype           | Recruiting\_Company Recruiting\_CalendarOffset Recruiting\_Date Recruiting\_GeographicLocation Recruiting\_ApplicantName Recruiting\_Employment Recruiting\_Performance Recruiting\_Job Recruiting\_Media Recruiting\_RecruitmentProject          |
| Recruiting\_Employment          | Startdato, slutdato og overførselsdato                        | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_GeographicLocation  | By, landsdel, postkode og stat eller provins                 | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Job                 | Funktion, type og titel                                        | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Media               | Kilde for ansøgere                                             | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Performance         | Klassifikation, beskrivelse og klassifikationsmodel                            | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_RecruitmentProject  | Projektbeskrivelse, projektstatus og åbninger                | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_TerminatedApplicant | Afsluttede ansøgere, årsag, performance og fratrædelsesdato | Recruiting\_Company Recruiting\_CalendarOffset Recruiting\_Date Recruiting\_GeographicLocation Recruiting\_Performance Recruiting\_Demographics Recruiting\_Employment Recruiting\_Media Recruiting\_RecruitmentProject Recruiting\_ApplicantName |

Disse enheder blev brugt til at oprette beregnede målinger. Disse beregnede mål bruges derefter til at beregne nøgletal (KPI'er) og rapporter, der bruges i indholdspakken. Hvis du vil medtage yderligere beregninger på rapporter og dashboard, kan du hente og redigere filen Recruiting.pbix fra LCS. Denne fil er den standarddatamodel, der blev brugt til at oprette indholdspakken. Når du har foretaget ændringerne, kan du oprette en indholdspakke og et dashboard for organisationen, som indeholder de oplysninger, du har tilføjet.

## <a name="additional-resources"></a>Yderligere ressourcer
Her er nogle nyttige links, der er knyttet til enheder og oprettelse af Power BI-indhold:

-   [Dataenheder](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Oprettelse af organisatoriske indholdspakker](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datamodellering i Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Tilføjelse af Power BI-felter til arbejdsområder](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





