---
title: Oversigt over arbejdsgangssystem
description: I dette emne beskrives arbejdsgangssystemet.
author: sericks007
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
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6e5e795ca6f7831ecd3fa28be9782f0b287eea6e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189999"
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
+ [Konfigurere en arbejdsgang for linjeelementer](configure-line-item-workflow.md)
+ [Ofte stillede spørgsmål om arbejdsgang](workflow-FAQ.md)
