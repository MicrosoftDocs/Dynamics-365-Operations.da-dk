---
title: Oversigt over arbejdsgangssystem
description: I dette emne beskrives arbejdsgangssystemet.
author: ChrisGarty
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 068f464fe5385486827b2f904114eb663e08b2e8
ms.sourcegitcommit: e55efd2f62bf60f678108c09ad4701a76b20cc68
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/17/2020
ms.locfileid: "3697963"
---
# <a name="workflow-system-overview"></a>Oversigt over arbejdsgangssystem

[!include [banner](../includes/banner.md)]

I dette emne beskrives arbejdsgangssystemet.

## <a name="what-is-workflow"></a>Hvad er en arbejdsgang?

Udtrykket *arbejdsgang* kan defineres på to måder: som et system og som en forretningsproces.

### <a name="workflow-is-a-system"></a>Arbejdsgang er et system

Arbejdsgang er et system, der kører på applikationsobjektserveren (AOS). Arbejdsgangssystemet indeholder funktioner, som du kan bruge til oprette individuelle arbejdsgange eller forretningsprocesser.

### <a name="workflow-is-a-business-process"></a>Arbejdsgang er en forretningsproces

En arbejdsgang repræsenterer en forretningsproces. Den definerer, hvordan et dokument "flyder" eller bevæger sig gennem systemet, ved at vise, hvem der skal udføre en opgave, træffe en beslutning eller godkende et dokument. I nedenstående illustration vises f.eks. en arbejdsgang for udgiftsrapporter.

![Arbejdsgang med elementer, der er tilknyttet brugere](./media/workflow_user.gif)

Hvis du bedre vil kunne forstå denne arbejdsgang, kan du antage, at Søren sender en udgiftsrapport for kr. 7.000. I dette scenario skal Ivan gennemse de kvitteringer, som Søren har sendt til ham. Henrik og Mette skal derefter godkende udgiftsrapporten. Antag nu, at Søren sender en udgiftsrapport for kr. 11.000. I dette scenario skal Ivan gennemse kvitteringerne, og Henrik, Mette og Dorthe skal godkende udgiftsrapporten.

## <a name="benefits-of-using-the-workflow-system"></a>Fordele ved at bruge arbejdsgangssystemet

Der er flere fordele ved at bruge arbejdsgangssystemet i organisationen:

- **Ensartede processer** – Du kan definere, hvordan bestemte dokumenter, f.eks. indkøbsrekvisitioner og udgiftsrapporter, behandles. Ved at bruge arbejdsgangssystemet kan du sikre, at dokumenter behandles og godkendes på en ensartet og effektiv måde.
- **Synliggørelse af processer** – Du kan spore status, historik og performanceværdier for arbejdsgangsforekomster. Dette hjælper dig med at bestemme, om der skal foretages ændringer i arbejdsgangen for at forbedre effektiviteten.
- **Centraliseret arbejdsliste** – Brugerne kan få vist en centraliseret arbejdsliste, der viser opgaverne i arbejdsgangen og de godkendelser, der er knyttet til dem.


## <a name="workflow-content"></a>Indhold af arbejdsgang

+ [Arkitektur for arbejdsgangssystem](workflow-system-architecture.md)
+ [Arbejdsgangselementer](workflow-elements.md)
+ [Handlinger i godkendelsesprocesser i arbejdsgang](workflow-actions.md)
+ [Oversigt over oprettelse af arbejdsgange](create-workflow.md)
+ [Konfigurere egenskaber for arbejdsgange](configure-workflow-properties.md)
+ [Konfigurere manuelle opgave i en arbejdsgang](configure-manual-task-workflow.md)
+ [Konfigurere automatiserede opgaver i en arbejdsgang](configure-automated-task-workflow.md)
+ [Konfigurere godkendelsesprocesser i en arbejdsgang](configure-approval-process-workflow.md)
+ [Konfigurere godkendelsestrin i en arbejdsgang](configure-approval-step-workflow.md)
+ [Konfigurere manuelle beslutninger i en arbejdsgang](configure-manual-decision-workflow.md)
+ [Konfigurere betingede beslutninger i en arbejdsgang](configure-conditional-decision-workflow.md)
+ [Konfigurere parallelle aktiviteter i en arbejdsgang](configure-parallel-activity-workflow.md)
+ [Konfigurere parallelle grene i en arbejdsgang](configure-parallel-branch-workflow.md)
+ [Konfigurere arbejdsgange for linjeelementer](configure-line-item-workflow.md)
+ [Ofte stillede spørgsmål om arbejdsgang](workflow-FAQ.md)
