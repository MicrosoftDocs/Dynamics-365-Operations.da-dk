---
title: "Indkøbs- og forsyningsarbejdsgange"
description: "I visse organisationer kræves det, at indkøbsrekvisitioner og indkøbsordrer skal godkendes af en anden bruger end den person, som har indtastet transaktionen. Du kan oprette en arbejdsgang for at oprette en godkendelsesproces."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 27c211e6ded17e085559add916c28a48c40e5b8e
ms.lasthandoff: 03/31/2017


---

# <a name="procurement-and-sourcing-workflows"></a>Indkøbs- og forsyningsarbejdsgange

I visse organisationer kræves det, at indkøbsrekvisitioner og indkøbsordrer skal godkendes af en anden bruger end den person, som har indtastet transaktionen. Du kan oprette en arbejdsgang for at oprette en godkendelsesproces.

En arbejdsgang repræsenterer en forretningsproces. Den definerer, hvordan et dokument "flyder" gennem systemet, og viser, hvem der skal udføre en opgave eller godkende et dokument. Der er flere fordele ved at bruge arbejdsgangssystemet i organisationen:
-   **Ensartede processer** – Du kan bruge arbejdsgangssystemet til at definere godkendelsesprocessen for bestemte dokumenter, f.eks. indkøbsrekvisitioner og udgiftsrapporter. Du kan bruge arbejdsgangssystemet som en hjælp til at sikre, at dokumenter behandles og godkendes på en ensartet og effektiv måde.
-   **Synliggørelse af processer** – Du kan spore status, historik og performanceværdier for en bestemt arbejdsgangsforekomst. Dette hjælper dig med at bestemme, om der skal foretages ændringer i arbejdsgangen for at forbedre effektiviteten.
-   **Centraliseret arbejdsliste**– brugerne kan få vist en centraliseret arbejdsliste for at få vist de arbejdsgangsopgaver og godkendelser, der er tilknyttet på tværs af alle arbejdsprocesser, som de deltager i. Dette er tilgængeligt på siden arbejdet varer.

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
Hvis du vil oprette en arbejdsproces, skal du gå til indkøb og forsyning &gt;Setup &gt;indkøb og forsyning af arbejdsprocesser og oprette en ny arbejdsproces ved at vælge typen arbejdsgang, du vil oprette.  

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

[Purchase requisition workflow](purchase-requisitions-workflow.md)


