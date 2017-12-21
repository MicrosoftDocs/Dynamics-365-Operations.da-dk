---
title: Power BI-indhold til medarbejderudvikling
description: "I dette emne beskrives Power BI-indhold til medarbejderudvikling. Det beskrives, hvordan du får adgang til rapporter, og der er oplysninger om den datamodel og de enheder, der blev brugt til at oprette indholdspakken."
author: jcart1106
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Talent, Core
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 6e64337f19600b18320550d91c134949c33af7b0
ms.openlocfilehash: f8ba7a968a1a5b376bac52106671607247f061d9
ms.contentlocale: da-dk
ms.lasthandoff: 12/01/2017

---

# <a name="employee-development-power-bi-content"></a>Power BI-indhold til medarbejderudvikling

[!include[banner](../includes/banner.md)]

I dette emne beskrives Microsoft Power BI-indhold til **Medarbejderudvikling**. Det beskrives, hvordan du får adgang til rapporter, og der er oplysninger om den datamodel og de enheder, der blev brugt til at oprette indholdspakken.

## <a name="accessing-the-power-bi-content"></a>Adgang til Power BI-indhold

Du kan finde indholdspakken **Medarbejderudvikling** i biblioteket Delte aktiver i Microsoft Dynamics Lifecycle Services (LCS). Du kan finde flere oplysninger om, hvordan du downloader indholdspakken og forbinder den med dine data, under [Power BI-indhold i LCS fra Microsoft og dine partnere](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Rapporter, der er inkluderet i Power BI-indholdet
De rapporter, der er inkluderet i Power BI-indholdet for **Medarbejderudvikling**, har både diagrammer og tabeller, der indeholder yderligere oplysninger. Rapporterne er beskrevet i følgende tabel.

| Rapport                        | Indhold |
|-------------------------------|----------|
| Oversigt over medarbejderudvikling | Oversigt over andre rapporter |
| Analyse af medarbejderkompetencer       | Medarbejderkompetencetyper og medarbejderkompetencer efter type |
| Analyse af medarbejderkompetenceniveauer | Medarbejderkompetenceniveauer efter afdeling, medarbejdere efter færdighedsniveau og færdighedstype og laveste og højeste niveauer pr. færdighed |
| Færdighedsprofil                 | Færdighedsprofil for den valgte medarbejder |
| Kompetenceanalyse                | Færdigheder efter type og klassifikation |
| Analyse af performanceanalyse   | Medarbejdere efter laveste og højeste klassifikation pr. job, medarbejderklassifikation efter afdeling, medarbejdere efter klassifikation og stillingstype og højeste og laveste klassifikationer efter stilling  |
| Analyse af medarbejderperformance | Medarbejderklassifikationer for den valgte klassifikation pr. leder |

Du kan filtrere diagrammer og felter i alle disse rapporter og fastgøre dem til dashboardet. Du kan finde flere oplysninger om filtrering og fastgørelse i Power BI under [Oprette og konfigurere et dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Forståelse af datamodellen og enheder
| Enhed                   | Indhold                                                                                                   | Relationer med andre enheder |
|--------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Kalenderforskydning          | Kalenderforskydninger for at opdele rapporter                                                                          | Tidligere stillingstildeling, stillingstendens, medarbejdertendens, fratrådt medarbejder 
| Regnskab                  | Virksomheder, som rapporter kan filtreres efter                                                                             | Aktuel medarbejder, fratrådt medarbejder, medarbejdertendens |
| Nuværende stilling         | Stillinger pr. dags dato, tilsvarende fuldtidsstilling (fuldtidsansatte), ledige stillinger og ledige-til-bestatte stillinger | Job, stilling |
| Aktuel medarbejder         | Arbejdere pr. den aktuelle dato, alder og antallet af beskæftigede                                                         | Firma, geografisk placering, medarbejdernavn, rapporterer til, medarbejdertitel, demografi, job, ansættelse, stilling |
| Dato                     | Dage, uger, måneder og år                                                                             | Tidligere stillingstildeling, stillingstendens, fratrådt medarbejder, medarbejdertendens |
| Demografi             | Fødselsdato, køn, etnisk oprindelse og civilstand                                                   | Aktuel medarbejder, fratrådt, medarbejder, medarbejdertendens |
| Ansættelse               | Startdato, slutdato og overførselsdato                                                                  | Aktuel medarbejder, fratrådt medarbejder, medarbejdertendens |
| Geografisk placering      | By, landsdel, postkode og stat eller provins                                                           | Aktuel medarbejder, fratrådt medarbejder, medarbejdertendens |
| Stilling                      | Funktion, type og titel                                                                                  | Aktuel stilling, aktuel medarbejder |
| Tidligere stillingstildeling | Årsagen til tildelingen, startdato, slutdato og job                                                           | Kalenderforskydning, dato, job, stilling |
| Stilling                 | Afdeling, fuldtidsansat, stilling, stillingstype og titel                                                        | Aktuel stilling, aktuel medarbejder |
| Stillingstendens           | Stillinger over tid, fuldtidsansatte og job                                                                          | Kalenderforskydning, dato, job, stilling |
| Rapporterer til               | Fornavn, efternavn og fulde navn                                                                       | Aktuel medarbejder, fratrådt medarbejder, medarbejdertendens |
| Fratrådt medarbejder      | Fratrådte medarbejdere, fratrædelsesdato, titel, stilling og job                                             | Firma, geografisk placering, medarbejdernavn, rapporterer til, kalenderforskydning, dato, medarbejdertitel, demografi, job, ansættelse, job |
| Medarbejdernavn            | Fornavn, efternavn og fulde navn                                                                       | Aktuel arbejder, fratrådt medarbejder, medarbejdertendens |
| Medarbejdertitel           | Titel og anciennitetsdato                                                                                   | Aktuel medarbejder, fratrådt medarbejder, medarbejdertendens |
| Medarbejdertendens           | Arbejdere over tid, beskæftigede, virksomhed og stilling                                                        | Firma, geografisk placering, medarbejdernavn, rapporterer til, kalenderforskydning, dato, medarbejdertitel, demografi, ansættelse, job |
| Stilling                      | Funktion, type og titel                                                                                      | Aktuel medarbejder, aktuel stilling, medarbejdertendens, job foretrukne færdighed, tidligere stillingstildeling, stillingstendens, fratrådt medarbejder |
| Jobbet foretrukne færdighed      | Prioritet, klassifikation, kompetence og færdighedsniveau                                                                 | Stilling |
| Analyse af medarbejderkompetencer  | Certificeret, niveau, niveaudato og færdighed                                                                    | Medarbejdernavn, færdighed |  
| Ydeevne              | Klassifikation, beskrivelse og klassifikationsmodel                                                                      | Aktuel medarbejder, aktuel stilling, medarbejdertendens, job foretrukne færdighed, tidligere stillingstildeling, stillingstendens, fratrådt medarbejder |
|  Færdighed                   | Færdighed, færdighedstype og klassifikation                                                                              | Analyse af medarbejderkompetencer, Job foretrukne færdighed |                                                                                                                        

Disse enheder blev brugt til at oprette beregnede målinger i datamodellen. Disse beregnede mål bruges derefter til at beregne nøgletal (KPI'er) og rapporter, der bruges i Power BI-indholdet. Hvis du vil medtage yderligere beregninger på rapporter og dashboard, kan du hente og redigere .pbix-filen fra LCS. Denne fil er den standarddatamodel, der blev brugt til at oprette Power BI-indholdet. Når du har foretaget ændringerne, kan du oprette en indholdspakke og et dashboard for organisationen, som indeholder de oplysninger, du har tilføjet.

