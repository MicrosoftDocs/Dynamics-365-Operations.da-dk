---
title: Power BI-indhold til Nøgletal for arbejdsstyrke
description: Dette emne beskriver Power BI-indhold til Nøgletal for arbejdsstyrke.
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorkforceWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 264084
ms.assetid: 8e700583-3a7d-4f5f-9ac8-58c4feed1a02
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 9393b4dcc6cb5f65d38c6904bf38def9d50af281671e0e09314148824f3e6891
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6757267"
---
# <a name="workforce-metrics-power-bi-content"></a>Power BI-indhold til Nøgletal for arbejdsstyrke

[!include [banner](../includes/banner.md)]

Dette emne beskriver **Nøgletal for arbejdsstyrke** Microsoft Power BI-indhold. Det beskrives, hvordan du får adgang til Power BI-rapporter, og der er oplysninger om den datamodel og de enheder, der blev brugt til at oprette indholdspakken.

## <a name="accessing-the-power-bi-content"></a>Adgang til Power BI-indholdet
Power BI-indholdet til **Nøgletal for arbejdsstyrke** vises i arbejdsområdet **Personalestyring**, hvis du bruger et af disse produkter:

- Microsoft Dynamics 365 Finance
- Microsoft Dynamics 365 Human Resources

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Metrikker, der er inkluderet i Power BI-indholdet
I følgende tabel vises de metrikker, som vises på hver enkelt rapport.

| Rapport                                           | Metrik |
|--------------------------------------------------|---------|
| Personmetrikker                                   | Oversigt over andre rapporter |
| Analyse af antal beskæftigede virksomhed, afdeling, lokalitet | Antal beskæftigede pr. virksomhed, antal beskæftigede pr. afdeling, antal beskæftigede pr. lokalitet og samlede antal beskæftigede |
| Analyse af antallet af beskæftigede efter job, trin, chef            | Antal beskæftigede pr. job, antal beskæftigede pr. trin, antal beskæftigede pr. chef og samlede antal beskæftigede |
| Tendensanalyse af antal beskæftigede                         | Antal beskæftigede i år sammenlignet med sidste år pr. firma og rullende antal beskæftigede for de seneste 12 måneder |
| FTE-analyse                                     | Det samlede antal fuldtidsansatte (FTE), samlet antal tildelte FTE, FTE efter afdeling, FTE for de seneste 12 måneder og FTE efter job |
| Arbejdsstyrkens demografi                           | Antallet af beskæftigede efter alder og køn, antal beskæftigede efter etnisk oprindelse, antal beskæftigede efter veteranstatus, antallet beskæftigede efter civilstand, antal fuldtidsstuderende, gennemsnitlig ansættelsestid, gennemsnitlig alder, forholdet mellem kvindelige og mandlige medarbejdere og sprog, der tales af medarbejderne |
| Stillingsanalyse                                | Ledige stillinger efter afdeling, ledige i forhold til besatte stillinger, aktive i forhold til inaktive stillinger og stillinger pr. afdeling |
| Analyse af naturlig afgang                               | Naturlig afgang i år i forhold til sidste år, naturlig afgang, afgang af medarbejdere efter alder og køn, gennemsnitlig ansættelsestid for medarbejdere, der rejser, afgang af medarbejdere denne måned og afgang af medarbejdere efter årsag |
| Personer pr. afdeling                             | Medarbejdere med et personalenummer efter afdeling, placering og tildeling af start- og slutdatoer |
| Anciennitetsanalyse                               | Gennemsnitlig ansættelsestid, gennemsnitligt antal års tjeneste pr. firma og anciennitetsliste |
| Medarbejdernes jubilæer                           | Jubilæer denne måned, jubilæer næste måned, medarbejdere efter antal år i tjenesten og jubilæer efter antal års tjeneste pr. afdeling |
| Medarbejdernes fødselsdage                               | Fødselsdage denne måned, fødselsdage næste måned, medarbejderfødselsdage og fødselsdage efter måned og afdeling |
| Masseansættelsesprojekter                               | Samlede masseansættelsesprojekter, masseansættelsesprojekter efter status, masseansættelsesprojekter efter afdeling og ejer, masseansættelsesprojekter efter job og masseansættelsesprojekter |

Du kan filtrere diagrammer og felter i alle disse rapporter og fastgøre dem til dashboardet. Du kan finde flere oplysninger om filtrering og fastgørelse i Power BI under [Oprette og konfigurere et dashboard](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

Sørg for at downloade Power BI-indhold til **Nøgletal for arbejdsstyrke**, der gælder for den version af Microsoft Dynamics 365, du bruger.

> [!NOTE]
> De .pbix-filer, der er tilgængelige i Lifecycle Services, gælder kun for Finance and Operations-apps.

## <a name="understanding-the-data-model-and-entities"></a>Forståelse af datamodellen og enheder
Følgende tabel viser de enheder, som indholdet er baseret på.

| Enhed                   | Indhold                                                                            | Relationer med andre enheder |
|--------------------------|-------------------------------------------------------------------------------------|-----------------------------------|
| Kalenderforskydning          | Kalenderforskydninger for at opdele rapporter                                                   | Tidligere stillingstildeling, stillingstendens, medarbejdertendens, fratrådt medarbejder |
| Regnskab                  | Virksomheder, som rapporter kan filtreres efter                                                      | Aktuel medarbejder, fratrådt medarbejder, medarbejdertendens |
| Nuværende stilling         | Stillinger pr. dags dato, fuldtidsansatte, ledige stillinger og ledige-til-besatte stillinger | Job, stilling |
| Aktuel medarbejder         | Arbejdere pr. den aktuelle dato, alder og antallet af beskæftigede                                  | Firma, geografisk placering, medarbejdernavn, rapporterer til, medarbejdertitel, demografi, job, ansættelse, stilling |
| Dato                     | Dage, uger, måneder og år                                                      | Tidligere stillingstildeling, stillingstendens, fratrådt medarbejder, medarbejdertendens |
| Demografi             | Fødselsdato, køn, etnisk oprindelse og civilstand                            | Aktuel medarbejder, fratrådt medarbejder, medarbejdertendens |
| Ansættelse               | Startdato, slutdato og overførselsdato                                           | Aktuel medarbejder, fratrådt medarbejder, medarbejdertendens |
| Geografisk placering      | By, landsdel, postkode og stat eller provins                                    | Aktuel medarbejder, fratrådt medarbejder, medarbejdertendens |
| Stilling                      | Funktion, type og titel                                                           | Aktuel stilling, aktuel medarbejder |
| Tidligere stillingstildeling | Årsagen til tildelingen, startdato, slutdato og job                                    | Kalenderforskydning, dato, job, stilling |
| Stilling                 | Afdeling, fuldtidsansat, stilling, stillingstype og titel                                 | Aktuel stilling, aktuel medarbejder |
| Stillingstendens           | Stillinger over tid, fuldtidsansatte og job                                                   | Kalenderforskydning, dato, job, stilling |
| Rapporterer til               | Fornavn, efternavn og fulde navn                                                | Aktuel medarbejder, fratrådt medarbejder, medarbejdertendens |
| Fratrådt medarbejder      | Fratrådte medarbejdere, fratrædelsesdato, titel, stilling og job                      | Firma, geografisk placering, medarbejdernavn, rapporterer til, kalenderforskydning, dato, medarbejdertitel, demografi, job, ansættelse, job |
| Medarbejdernavn            | Fornavn, efternavn og fulde navn                                                | Aktuel arbejder, fratrådt medarbejder, medarbejdertendens |
| Medarbejdertitel           | Titel og anciennitetsdato                                                            | Aktuel medarbejder, fratrådt medarbejder, medarbejdertendens |
| Medarbejdertendens           | Arbejdere over tid, beskæftigede, virksomhed og stilling                                 | Firma, geografisk placering, medarbejdernavn, rapporterer til, kalenderforskydning, dato, medarbejdertitel, demografi, ansættelse, job |
| Masseansættelsesprojekt        | Antallet af masseansættelsesprojekter, projektejer og projektstatus                     | Firma, masseansættelseslinje. |
| Masseansættelseslinje           | Afdeling, medarbejdertype og stilling                                           | Dato, job, masseansættelsesprojekt |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]