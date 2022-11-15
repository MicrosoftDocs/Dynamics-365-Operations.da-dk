---
title: Annullere et job, der blev oprettet ved hjælp af det udfasede varedisponeringsprogram
description: Denne artikel beskriver, hvordan du kan annullere et aktivt planlægningsjob, der bruger det udfasede varedisponeringsprogram.
author: t-benebo
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace, ReqProcessList
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-12-16
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7b71a43f407050dccb7550db7c4b6a98a596d589
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740871"
---
# <a name="cancel-a-job-that-was-created-using-the-deprecated-master-planning-engine"></a>Annullere et job, der blev oprettet ved hjælp af det udfasede varedisponeringsprogram

[!include [banner](../includes/banner.md)]

Der er flere muligheder for annullering af et job, der er oprettet ved hjælp af det udfasede varedisponeringsprogram. Du kan for eksempel annullere et varedisponeringsjob, hvis det er startet ved en fejltagelse eller kører længere tid end forventet, og du vil afslutte det.

Den bedste måde at annullere et varedisponeringsjob på er ved hjælp af siden **Uafsluttede planlægningsprocesser**. Alternative indstillinger fra siderne **Batchjobs** og **Forbedrede batchjobs** bør kun bruges, hvis annullering af varedisponeringsjobbet fra siden **Uafsluttede planlægningsprocesser** ikke blev fuldført inden for få minutter.

## <a name="preferred-cancel-option"></a>Foretrukket annulleringsindstilling

### <a name="cancel-master-planning-job-from-the-unfinished-planning-processes-page"></a>Annullere varedisponeringsjob fra siden Uafsluttede planlægningsprocesser

1. Gå til **Varedisponering > Forespørgsler og rapporter > Varedisponering > Uafsluttede planlægningsprocesser**.
2. Vælg linjen med den planlægningsproces, du vil annullere.
3. Vælg **Annuller**.

## <a name="additional-cancel-options"></a>Flere annulleringsindstillinger

Disse bør kun anvendes hvis annulleringen af varedisponeringsjobbet fra siden **Uafsluttede planlægningsprocesser** ikke blev fuldført inden for få minutter.

### <a name="delete-master-planning-job-from-the-batch-jobs-page"></a>Slet varedisponeringsjobbet fra siden **Batchjobs**

1. Gå til **Systemadministration > Forespørgsler > Batchjob**.
2. Vælg linjen med det planlægningsjob, du vil slette.
3. Vælg **Slet**.

### <a name="abort-master-planning-job-task-from-the-batch-jobs-enhanced-page"></a>Afbryd opgaven varedisponeringsjob fra siden **Forbedrede batchjobs**

1. Gå til **Systemadministration > Forespørgsler > Batchjob**.
2. Hvis job-ID'et ikke fremgår af listen, skal du klikke på **Skift til udvidet formular**, ellers skal du fortsætte med næste trin.
3. Åbn batchjobbet. Vælg **Job-id** for batchjobbet med de opgaver, du vil afslutte.
4. Vælg hvilke opgaver, der skal afsluttes, i **Batchopgaver**.
5. Vælg **Skift status**, vælg **Annullerer**, og klik på **OK**.
6. I oversigtspanelet **Batchopgaver** skal du klikke på **Afbryd**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]