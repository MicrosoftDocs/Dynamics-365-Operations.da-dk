---
title: "Indkøbs- og forsyningsarbejdsgange"
description: "I visse organisationer kræves det, at indkøbsrekvisitioner og indkøbsordrer skal godkendes af en anden bruger end den person, som har indtastet transaktionen. Du kan oprette en arbejdsgang for at oprette en godkendelsesproces."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 67bdb8436ff379b0e55cfe1660597e8f93235eeb
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017

---

# <a name="procurement-and-sourcing-workflows"></a>Indkøbs- og forsyningsarbejdsgange

[!include[banner](../includes/banner.md)]


I visse organisationer kræves det, at indkøbsrekvisitioner og indkøbsordrer skal godkendes af en anden bruger end den person, som har indtastet transaktionen. Du kan oprette en arbejdsgang for at oprette en godkendelsesproces.

En arbejdsgang repræsenterer en forretningsproces. Den definerer, hvordan et dokument "flyder" gennem systemet, og viser, hvem der skal udføre en opgave eller godkende et dokument. Der er flere fordele ved at bruge arbejdsgangssystemet i organisationen:
-   **Ensartede processer** – Du kan bruge arbejdsgangssystemet til at definere godkendelsesprocessen for bestemte dokumenter, f.eks. indkøbsrekvisitioner og udgiftsrapporter. Du kan bruge arbejdsgangssystemet som en hjælp til at sikre, at dokumenter behandles og godkendes på en ensartet og effektiv måde.
-   **Synliggørelse af processer** – Du kan spore status, historik og performanceværdier for en bestemt arbejdsgangsforekomst. Dette hjælper dig med at bestemme, om der skal foretages ændringer i arbejdsgangen for at forbedre effektiviteten.
-   **Centraliseret arbejdsliste**– Brugerne kan få vist en centraliseret arbejdsliste for at få vist opgaverne i arbejdsgangen og godkendelser, der er tildelt til dem på tværs af alle arbejdsprocesser, som de deltager i. Dette er tilgængeligt på siden Workflowopgaver.

## <a name="the-types-of-workflows-that-you-can-create"></a> De typer arbejdsgange, du kan oprette
Der er følgende tilgængelige arbejdsgangstyper for Indkøb og forsyning.

|                                  |                                                               |
|----------------------------------|---------------------------------------------------------------|
| **Skriv**                         | **Brug denne type til at**                                          |
| Gennemgang af indkøbsrekvisition      | Oprette evalueringsarbejdsgange for indkøbsrekvisitioner.            |
| Evaluering af indkøbsrekvisitionslinjer | Oprette evalueringsarbejdsgange for indkøbsrekvisitionslinjer.       |
| Arbejdsgang for indkøbsordre          | Opret evaluerings- og godkendelsesarbejdsgange for indkøbsordrelinjer.     |
| Arbejdsgang for indkøbsordrelinje     | Oprette evaluerings- og godkendelsesarbejdsgange for indkøbsordrelinjer. |

## <a name="creating-a-workflow"></a>Oprettelse af en arbejdsgang
Hvis du vil oprette en arbejdsgang, skal du gå til Indkøb og forsyning &gt; Opsætning &gt; Indkøbs- og forsyningsarbejdsgange og oprette en ny arbejdsgang ved at vælge den type arbejdsgang, du vil oprette.  

På lærredet for arbejdsgangen kan du trække arbejdsgangselementer til designeren og sammenkæde elementerne til en arbejdsgang. Arbejdsgangselementerne bør være konfigureret. Du kan konfigurere, hvilken deltager der bør træffe foranstaltninger, i forbindelse med arbejdsgangselementer af typerne godkendelse og opgave.
Deltagertyper
----------------------

Du kan knytte et godkendelsestrin til følgende deltagergrupper.

| Brugergruppe    | Beskrivelse                                                               |
|---------------|---------------------------------------------------------------------------|
| Deltager   | Tildel godkendelsestrinnet til medlemmer af en gruppe eller en rolle.                   |
| Hierarki     | Tildel godkendelsestrinnet til brugere i et bestemt organisationshierarki. |
| Arbejdsgangsbruger | Tildel godkendelsestrinnet til brugere i denne arbejdsgang.                       |
| Kø         | Tildel godkendelsestrinnet til en workflowopgavekø.                            |
| Bruger          | Tildel godkendelsestrinnet til bestemte brugere.                               |



<a name="see-also"></a>Se også
--------

[Definition af forretningsprocesarbejdsgange for indkøbsrekvisitioner](https://mbs.microsoft.com/customersource/Global/AX/learning/documentation/white-papers/Defining_business_process_workflows_for_purchase_requisitions)

[Arbejdsgang for indkøbsrekvisitioner](purchase-requisitions-workflow.md)



