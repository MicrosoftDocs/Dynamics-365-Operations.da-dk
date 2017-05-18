---
title: "Kanban-området for overførsel understøtter stregkodescannere"
description: "Kanban-områdetet understøtter scannerinput fra en widget stregkodescanner til at vælge, starte, udfylde og tømme et kanban-job."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19391
ms.assetid: a426f645-d59b-4c98-8d78-eba8d64a562e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 96eae9e3c09e895d5d81c080da18fefaca5c1d78
ms.contentlocale: da-dk
ms.lasthandoff: 04/25/2017


---

# <a name="kanban-transfer-board-support-for-barcode-scanners"></a>Kanban-området for overførsel understøtter stregkodescannere

[!include[banner](../includes/banner.md)]


Kanban-områdetet understøtter scannerinput fra en widget stregkodescanner til at vælge, starte, udfylde og tømme et kanban-job.

<a name="registration-modes"></a>Registreringstilstande
------------------

På oversigtspanelet **Scanner registrering** kan du vælge den registreringstilstand, der styrer handlingen, når du scanner et kanban-kortnummer eller manuelt skriver tallet i feltet med kanban-kortet.
| Angiv registreringstilstand | Beskrivelse                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------|
| Igangsætning                 | Registrerer et kanban-overførselsjob som igangværende.                                                 |
| Fuldført              | Registrerer et kanban-overførselsjob som fuldført.                                                   |
| Tom                 | Registrerer den materialehåndteringsenhed, der refereres til på kanban-kortet, som tom.              |
| Vælg                | Registrerer et kanban-kortnummer og vælger automatisk det job, der refereres til på kanban-listen. |

 
<a name="registration-mode-select"></a>Valg af registreringstilstand
------------------------

Når du bruger en stregkodelæser til at vælge et job, ændres visningstilstanden for kanban-området. I denne tilstand gælder følgende betingelser:

-   Der vises kun det scannede kanban-job.
-   Detaljerne om det valgte job vises i oversigtspanelet **Detaljer**.
-   I oversigtspanelet **Meddelelser** vises der kun meddelelser for det valgte job.
-   Du kan ændre status for jobbet ved hjælp af funktioner, der er tilgængelige i handlingsruden. I kanban-overførselsområdet vises der fortsat kun et enkelt job i denne periode.
-   Du kan opdatere oplysningerne på listen over job manuelt ved at klikke på **Opdater** (Skift+F5) i handlingsruden. Når du har opdateret oplysningerne, vises de komplette resultater for jobfilteret igen.

## <a name="job-status-and-possible-actions"></a>Jobstatus og mulige handlinger
Status for det valgte job og status for udlignede job for hændelseskanbans bestemmer, om du kan behandle jobbet yderligere. I følgende tabel vises oplysninger om disse statusser og opgaver:
-   De statusser, der er tilgængelige for job eller for materialehåndteringsenheder, der henvises til af jobbene.
-   Hver opgave, du kan udføre for jobbet.

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th>Jobtype</th>
<th>Status for job eller status for materialehåndteringsenhed</th>
<th>Opdater plukliste</th>
<th>Igangsætning</th>
<th>Opdater registrering</th>
<th>Fuldført</th>
<th>Tom</th>
<th>Opret hændelseskanbans</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Flytning</td>
<td><ul>
<li>Ikke planlagt</li>
<li>Der er ingen udlignede job, eller udlignede job er fuldførte</li>
</ul></td>
<td>Ja</td>
<td>Ja</td>
<td>Ja</td>
<td>Ja</td>
<td>Nej</td>
<td>Ja</td>
</tr>
<tr class="even">
<td>Flytning</td>
<td><ul>
<li>Ikke planlagt</li>
<li>Det udlignede job er ikke fuldført</li>
</ul></td>
<td>Ja</td>
<td>Nej</td>
<td>Ja</td>
<td>Nej</td>
<td>Nej</td>
<td>Nej</td>
</tr>
<tr class="odd">
<td>Flytning</td>
<td>I gang</td>
<td>Ja</td>
<td>Nej</td>
<td>Ja</td>
<td>Ja</td>
<td>Nej</td>
<td>Nej</td>
</tr>
<tr class="even">
<td>Flytning</td>
<td>Gennemført</td>
<td>Nej</td>
<td>Nej</td>
<td>Nej</td>
<td>Nej</td>
<td>Ja</td>
<td>Nej</td>
</tr>
<tr class="odd">
<td>Overførsel eller proces</td>
<td>Tom</td>
<td>Nej</td>
<td>Nej</td>
<td>Nej</td>
<td>Nej</td>
<td>Nej</td>
<td>Nej</td>
</tr>
<tr class="even">
<td>Overførsel eller proces</td>
<td>Der blev ikke fundet et kanban-kort</td>
<td>Nej</td>
<td>Nej</td>
<td>Nej</td>
<td>Nej</td>
<td>Nej</td>
<td>Nej</td>
</tr>
<tr class="odd">
<td>Overførsel eller proces</td>
<td>Der blev fundet et kanban-kort, men det er ikke tildelt til en kanban</td>
<td>Nej</td>
<td>Nej</td>
<td>Nej</td>
<td>Nej</td>
<td>Nej</td>
<td>Nej</td>
</tr>
<tr class="even">
<td>Behandl</td>
<td><ul>
<li>Ikke planlagt</li>
<li>Forberedt</li>
<li>I gang</li>
</ul></td>
<td>Nej</td>
<td>Nej</td>
<td>Nej</td>
<td>Nej</td>
<td>Nej</td>
<td>Nej</td>
</tr>
<tr class="odd">
<td>Behandl</td>
<td>Gennemført</td>
<td>Nej</td>
<td>Nej</td>
<td>Nej</td>
<td>Nej</td>
<td>Nej</td>
<td>Nej</td>
</tr>
</tbody>
</table>






