---
title: Power BI-indhold for kompensation
description: "Dette emne beskriver Power BI-indhold for kompensation. Det beskrives, hvordan du får adgang til rapporter, og der er oplysninger om den datamodel og de enheder, der blev brugt til at oprette indholdspakken."
author: jcart1106
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations, UnifiedOperations, Talent, Core
ms.search.region: Global
ms.author: JCart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 86229c27b75e2640a0fb88dd73aa50b47585b29d
ms.contentlocale: da-dk
ms.lasthandoff: 06/13/2017

---

# <a name="compensation-power-bi-content"></a>Power BI-indhold for kompensation

[!include[banner](../includes/banner.md)]

I dette emne beskrives **Kompensation** i Microsoft Power BI-indhold. Det beskrives, hvordan du får adgang til rapporter, og der er oplysninger om den datamodel og de enheder, der blev brugt til at oprette indholdspakken.

## <a name="accessing-the-power-bi-content"></a>Adgang til Power BI-indhold
Power BI-indholdet for **Kompensation** vises i arbejdsområdet **Kompensationsstyring**, hvis du bruger et af følgende produkter:

- Opdatering til Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, fra juli 2017
- Microsoft Dynamics 365 for Talent

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Rapporter, der er inkluderet i Power BI-indholdet
De rapporter, der er inkluderet i Power BI-indholdet for **Kompensation**, har både diagrammer og tabeller, der indeholder yderligere oplysninger. Rapporterne er beskrevet i følgende tabel.

| Rapport                     | Indhold |
|----------------------------|----------|
| Kompensationsoversigt      | Oversigt over andre rapporter |
| Kompensationsanalyse      | Timelønnede og fastansatte medarbejdere i firmaet, samlet antal medarbejdere efter kompensationsplan, mandlige og kvindelige medarbejdere efter kompensationsplan og medarbejderkompensation efter afdeling |
| Stillingsrelateret betalingsanalyse      | Højeste og laveste timeløn og fast løn, stillinger med højeste og laveste løn og fuldtids- og deltidsstillinger |
| Kompensationsplananalyse | Medarbejdertilmeldning efter valgt frynsegode |

Du kan filtrere diagrammer og felter i alle disse rapporter og fastgøre dem til dashboardet. Du kan finde flere oplysninger om filtrering og fastgørelse i Power BI under [Oprette og konfigurere et dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="extending-the-power-bi-content"></a>Udvidelse af Power BI-indhold
Hvis du bruger opdateringen til Microsoft Dynamics 365 for Operations version 1611 eller Finance and Operations, Enterprise edition fra juli 2017 kan du finde Power BI-indholdet til **Kompensation** i biblioteket Delte aktiver i LCS. Du kan finde flere oplysninger om, hvordan du downloader indhold og implementerer det i din organisation, under [Power BI-indhold i LCS fra Microsoft og dine partnere](power-bi-content-microsoft-partners.md). Hvis du vil se en demo, der viser, hvordan du implementerer Power BI-indholdet, kan du se dette Office Mix [Power BI-indhold fra Microsoft og dine partnere i Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w).

Sørg for at downloade det **Kompensation** Power BI-indhold, der gælder for den version af Microsoft Dynamics 365, du bruger.

>[!NOTE]
>De .pbix-filer, der er tilgængelige i Lifecycle Services gælder kun for Finance and Operations .

## <a name="understanding-the-data-model-and-entities"></a>Forståelse af datamodellen og enheder
Følgende data bruges til at udfylde rapporterne i Power BI-indhold for **Kompensation**. Denne tabel viser de enheder, som indholdet er baseret på.

| Enhed                   | Indhold                                                                                                   | Relationer med andre enheder |
|--------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Kalenderforskydning          | Kalenderforskydninger for at opdele rapporter                                                                          | Tidligere stillingstildeling, stillingstendens, medarbejdertendens, fratrådt medarbejder |
| Regnskab                  | Virksomheder, som rapporter kan filtreres efter                                                                             | Aktuel kompensation, aktuel medarbejder, fratrådt medarbejder, medarbejdertendens |
| Kompensation             | Lønsats og -frekvens over tid                                                                           | Aktuel kompensation, aktuel medarbejder, fratrådt medarbejder, medarbejdertendens |
| Aktuel kompensation     | Lønsats og -frekvens pr. dags dato                                                              | Firma, kompensation, demografi, job, stilling |
| Nuværende stilling         | Stillinger pr. dags dato, tilsvarende fuldtidsstilling (fuldtidsansatte), ledige stillinger og ledige-til-bestatte stillinger | Job, stilling |
| Aktuel medarbejder         | Arbejdere pr. den aktuelle dato, alder og antallet af beskæftigede                                                         | Firma, kompensation, geografisk placering, medarbejdernavn, rapporterer til, medarbejdertitel, demografi, job, ansættelse, stilling, frynsegoder |
| Dato                     | Dage, uger, måneder og år                                                                             | Tidligere stillingstildeling, stillingstendens, fratrådt medarbejder, medarbejdertendens |
| Demografi             | Fødselsdato, køn, etnisk oprindelse og civilstand                                                   | Aktuel medarbejder, fratrådt medarbejder, medarbejdertendens |
| Ansættelse               | Startdato, slutdato og overførselsdato                                                                  | Aktuel medarbejder, fratrådt medarbejder, medarbejdertendens |
| Geografisk placering      | By, landsdel, postkode og stat eller provins                                                           | Aktuel medarbejder, fratrådt medarbejder, medarbejdertendens |
| Stilling                      | Funktion, type og titel                                                                                  | Aktuel stilling, aktuel medarbejder |
| Tidligere stillingstildeling | Årsagen til tildelingen, startdato, slutdato og job                                                           | Kalenderforskydning, dato, job, stilling |
| Stilling                 | Afdeling, fuldtidsansat, stilling, stillingstype og titel                                                        | Aktuel stilling, aktuel medarbejder |
| Stillingstendens           | Stillinger over tid, fuldtidsansatte og job                                                                          | Kalenderforskydning, dato, job, stilling |
| Rapporterer til               | Fornavn, efternavn og fulde navn                                                                       | Aktuel arbejder, fratrådt medarbejder, medarbejdertendens |
| Fratrådt medarbejder      | Fratrådte medarbejdere, fratrædelsesdato, titel, stilling og job                                             | Firma, kompensation, geografisk placering, medarbejdernavn, rapporterer til, kalenderforskydning, dato, medarbejdertitel, demografi, job, ansættelse, job, stilling, frynsegoder |
| Frynsegoder                 | Ikrafttrædelsesdato, frynsegodeindstilling, frynsegodeplan og frynsegodetype                                             | Aktuel navn, fratrådt medarbejder, medarbejdertendens |
| Medarbejdernavn            | Fornavn, efternavn og fulde navn                                                                       | Aktuel medarbejder, fratrådt medarbejder, medarbejdertendens |
| Medarbejdertitel           | Titel og anciennitetsdato                                                                                   | Aktuel medarbejder, fratrådt medarbejder, medarbejdertendens |
| Medarbejdertendens           | Arbejdere over tid, beskæftigede, virksomhed og stilling                                                        | Firma, kompensation, geografisk placering, medarbejdernavn, rapporterer til, kalenderforskydning, dato, medarbejdertitel, demografi, job, ansættelse, job, frynsegoder |

Disse enheder blev brugt til at oprette beregnede målinger i datamodellen. Disse beregnede mål bruges derefter til at beregne nøgletal (KPI'er) og rapporter, der bruges i indholdet. Hvis du vil medtage yderligere beregninger på rapporter og dashboard, kan du hente og redigere .pbix-filen fra LCS. Denne fil er den standarddatamodel, der blev brugt til at oprette indholdet. Når du har foretaget ændringerne, kan du oprette en indholdspakke og et dashboard for organisationen, som indeholder de oplysninger, du har tilføjet.

