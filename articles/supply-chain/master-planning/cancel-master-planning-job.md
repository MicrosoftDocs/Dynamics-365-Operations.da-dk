---
title: Annuller et varedisponeringsjob
description: I dette emne beskrives det, hvordan du kan annullere et aktivt planlægningsjob, der bruger den indbyggede planlægningsfunktion.
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
ms.openlocfilehash: d96f946c0c87db44ac5fe1adda68e47838dcc0d7
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/23/2022
ms.locfileid: "8469220"
---
# <a name="cancel-a-master-planning-job"></a>Annuller et varedisponeringsjob

[!include [banner](../includes/banner.md)]

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
5. Klik på **Skift status**, vælg **Annuller**, og klik på **OK**.
6. I oversigtspanelet **Batchopgaver** skal du klikke på **Afbryd**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]