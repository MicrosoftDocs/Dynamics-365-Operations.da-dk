---
title: Oversigt over arbejdsgang
description: I dette emne beskrives arbejdsgangsystemet i Microsoft Dynamics 365 for Finance and Operations.
author: sericks007
manager: AnnBe
ms.date: 08/17/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6622f0e5ed6c38bb8131d13aa02061968862678b
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="workflow-overview"></a>Oversigt over arbejdsgang

[!include[banner](../includes/banner.md)]


I dette emne beskrives arbejdsgangsystemet i Microsoft Dynamics 365 for Finance and Operations.

<a name="what-is-workflow"></a>Hvad er en arbejdsgang?
-----------------

Udtrykket *arbejdsgang* kan defineres på to måder: som et system og som en forretningsproces.
### <a name="workflow-is-a-system"></a>Arbejdsgang er et system

Arbejdsgang er et system, som installeres med Finance and Operations, og som kører i AOS (applikationsobjektserveren). Arbejdsgangssystemet indeholder funktioner, som du kan bruge til oprette individuelle arbejdsgange eller forretningsprocesser.

### <a name="workflow-is-a-business-process"></a>Arbejdsgang er en forretningsproces

En arbejdsgang repræsenterer en forretningsproces. Den definerer, hvordan et dokument "flyder" eller bevæger sig gennem systemet, ved at vise, hvem der skal udføre en opgave, træffe en beslutning eller godkende et dokument. I nedenstående illustration vises f.eks. en arbejdsgang for udgiftsrapporter. 

![Arbejdsgang med elementer, der er tilknyttet brugere](./media/workflow_user.gif) 

Hvis du bedre vil kunne forstå denne arbejdsgang, kan du antage, at Søren sender en udgiftsrapport for kr. 7.000. I dette scenario skal Ivan gennemse de kvitteringer, som Søren har sendt til ham. Henrik og Mette skal derefter godkende udgiftsrapporten. Antag nu, at Søren sender en udgiftsrapport for kr. 11.000. I dette scenario skal Ivan gennemse kvitteringerne, og Henrik, Mette og Dorthe skal godkende udgiftsrapporten.

## <a name="benefits-of-using-the-workflow-system"></a>Fordele ved at bruge arbejdsgangssystemet

Der er flere fordele ved at bruge arbejdsgangssystemet i organisationen:
-   **Ensartede processer** – Du kan definere, hvordan bestemte dokumenter, f.eks. indkøbsrekvisitioner og udgiftsrapporter, behandles. Ved at bruge arbejdsgangssystemet kan du sikre, at dokumenter behandles og godkendes på en ensartet og effektiv måde.
-   **Synliggørelse af processer** – Du kan spore status, historik og performanceværdier for arbejdsgangsforekomster. Dette hjælper dig med at bestemme, om der skal foretages ændringer i arbejdsgangen for at forbedre effektiviteten.
-   **Centraliseret arbejdsliste** – Brugerne kan få vist en centraliseret arbejdsliste, der viser opgaverne i arbejdsgangen og de godkendelser, der er knyttet til dem.


## <a name="workflow-content"></a>Indhold af arbejdsgang

+ [Arkitektur for arbejdsgang](workflow-system-architecture.md)
+ [Arbejdsgangselementer](workflow-elements.md)
+ [Arbejdsgangshandlinger](workflow-actions.md)
+ [Oprette en arbejdsgang](create-workflow.md)
+ [Konfigurere egenskaberne for arbejdsgang](configure-workflow-properties.md)
+ [Konfigurere en manuel opgave i en arbejdsgang](configure-manual-task-workflow.md)
+ [Konfigurere en automatiseret opgave i en arbejdsgang](configure-automated-task-workflow.md)
+ [Konfigurere en godkendelsesproces i en arbejdsgang](configure-approval-process-workflow.md)
+ [Konfigurere et godkendelsestrin i en arbejdsgang](configure-approval-step-workflow.md)
+ [Konfigurere en manuel beslutning i en arbejdsgang](configure-manual-decision-workflow.md)
+ [Konfigurere en betinget beslutning i en arbejdsgang](configure-conditional-decision-workflow.md)
+ [Konfigurere en parallel aktivitet i en arbejdsgang](configure-parallel-activity-workflow.md)
+ [Konfigurere en parallel gren i en arbejdsgang](configure-parallel-branch-workflow.md)
+ [Konfigurere en arbejdsgang for linjeelement](configure-line-item-workflow.md)
