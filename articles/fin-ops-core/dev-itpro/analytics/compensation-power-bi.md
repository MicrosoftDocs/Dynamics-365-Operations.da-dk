---
title: Power BI-indhold til kompensation
description: I dette emne beskrives Power BI-indhold til kompensation. Det forklarer, hvordan du får adgang til rapporterne, og giver oplysninger om datamodellen.
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmCompensationWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 1a961e71f0fdb34416a2720a5d5012c895e8a68c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754445"
---
# <a name="compensation-power-bi-content"></a>Power BI-indhold til kompensation

[!include [banner](../includes/banner.md)]

I dette emne beskrives **kompensation** i Microsoft Power BI-indhold til. Det beskrives, hvordan du får adgang til rapporter, og der er oplysninger om den datamodel og de enheder, der blev brugt til at oprette indholdspakken.

## <a name="accessing-the-power-bi-content"></a>Adgang til Power BI-indholdet
Power BI-indholdet til **Kompensation** vises i arbejdsområdet **Kompensationsstyring**, hvis du bruger et af følgende produkter:

- Finance and Operations-apps
- Microsoft Dynamics 365 Human Resources

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Rapporter, der er inkluderet i Power BI-indholdet
De rapporter, der er inkluderet i Power BI-indholdet til **Kompensation**, har både diagrammer og tabeller, der indeholder yderligere oplysninger. Rapporterne er beskrevet i følgende tabel.

| Rapport                     | Indhold |
|----------------------------|----------|
| Kompensationsoversigt      | Oversigt over andre rapporter |
| Kompensationsanalyse      | Timelønnede og fastansatte medarbejdere i firmaet, samlet antal medarbejdere efter kompensationsplan, mandlige og kvindelige medarbejdere efter kompensationsplan og medarbejderkompensation efter afdeling |
| Stillingsrelateret betalingsanalyse      | Højeste og laveste timeløn og fast løn, stillinger med højeste og laveste løn og fuldtids- og deltidsstillinger |
| Kompensationsplananalyse | Medarbejdertilmeldning efter valgt frynsegode |

Du kan filtrere diagrammer og felter i alle disse rapporter og fastgøre dem til dashboardet. Du kan finde flere oplysninger om filtrering og fastgørelse i Power BI under [Oprette og konfigurere et dashboard](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Forståelse af datamodellen og enheder
Følgende data bruges til at udfylde rapporterne i Power BI-indhold til **Kompensation**. Denne tabel viser de enheder, som indholdet er baseret på.

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
| Fratrådt medarbejder      | Fratrådte medarbejdere, fratrædelsesdato, titel, stilling og job                                           | Firma, kompensation, geografisk placering, medarbejdernavn, rapporterer til, kalenderforskydning, dato, medarbejdertitel, demografi, job, ansættelse, job, stilling, frynsegoder |
| Frynsegoder                 | Ikrafttrædelsesdato, frynsegodeindstilling, frynsegodeplan og frynsegodetype                                             | Aktuel navn, fratrådt medarbejder, medarbejdertendens |
| Medarbejdernavn            | Fornavn, efternavn og fulde navn                                                                       | Aktuel medarbejder, fratrådt medarbejder, medarbejdertendens |
| Medarbejdertitel           | Titel og anciennitetsdato                                                                                   | Aktuel medarbejder, fratrådt medarbejder, medarbejdertendens |
| Medarbejdertendens           | Arbejdere over tid, beskæftigede, virksomhed og stilling                                                        | Firma, kompensation, geografisk placering, medarbejdernavn, rapporterer til, kalenderforskydning, dato, medarbejdertitel, demografi, job, ansættelse, job, frynsegoder |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]