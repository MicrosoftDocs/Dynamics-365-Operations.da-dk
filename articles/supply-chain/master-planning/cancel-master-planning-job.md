---
title: Annuller et varedisponeringsjob
description: I dette emne beskrives det, hvordan du kan annullere et aktivt planlægningsjob, der bruger den indbyggede planlægningsfunktion.
author: ChristianRytt
manager: AnnBe
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-12-16
ms.dyn365.ops.version: ''
ms.openlocfilehash: 66d5b10e1471b98274d4049df18a2e53873f789a
ms.sourcegitcommit: 92cd55028be556a0bd41b6972c9c6d14b695dfa0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/10/2020
ms.locfileid: "2947474"
---
# <a name="cancel-a-master-planning-job"></a>Annuller et varedisponeringsjob

I Microsoft Dynamics 365 Supply Chain Management er der flere muligheder for at annullere et varedisponeringsjob. Du kan for eksempel annullere et varedisponeringsjob, hvis det er startet ved en fejltagelse eller kører længere tid end forventet, og du vil afslutte det. Den bedste måde at annullere et varedisponeringsjob på er ved hjælp af siden **Uafsluttede planlægningsprocesser**. Alternative indstillinger fra siderne **Batchjobs** og **Forbedrede batchjobs** bør kun bruges, hvis annullering af varedisponeringsjobbet fra siden **Uafsluttede planlægningsprocesser** ikke blev fuldført inden for få minutter.

## <a name="preferred-cancel-option"></a>Foretrukket annulleringsindstilling
### <a name="cancel-master-planning-job-from-unfinished-planning-processes-page"></a>Annuller varedisponeringsjob fra siden **Uafsluttede planlægningsprocesser**
1. Gå til **Varedisponering > Forespørgsler og rapporter > Varedisponering > Uafsluttede planlægningsprocesser**.
2. Vælg linjen med den planlægningsproces, du vil annullere.
3. Klik på **Annuller**.

## <a name="additional-cancel-options"></a>Flere annulleringsindstillinger
Disse bør kun anvendes hvis annulleringen af varedisponeringsjobbet fra siden **Uafsluttede planlægningsprocesser** ikke blev fuldført inden for få minutter.

### <a name="delete-master-planning-job-from-the-batch-jobs-page"></a>Slet varedisponeringsjobbet fra siden **Batchjobs**
1. Gå til **Systemadministration > Forespørgsler > Batchjob**.
2. Vælg linjen med det planlægningsjob, du vil slette.
3. Klik på **Slet**.

### <a name="abort-master-planning-job-task-from-the-batch-jobs-enhanced-page"></a>Afbryd opgaven varedisponeringsjob fra siden **Forbedrede batchjobs**
1. Gå til **Systemadministration > Forespørgsler > Batchjob**.
2. Hvis job-ID'et ikke fremgår af listen, skal du klikke på **Skift til udvidet formular**, ellers skal du fortsætte med næste trin.
3. Åbn batchjobbet. Klik på **Opgave-ID'et** for batchjobbet med de opgaver, du vil afslutte.
4. Vælg hvilke opgaver, der skal afsluttes, i **Batchopgaver**.
5. I oversigtspanelet **Batchopgaver** skal du klikke på **Afbryd**.
