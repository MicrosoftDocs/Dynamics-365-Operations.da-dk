--- 
title: Flytte planlagte kanban-job
description: "Denne fremgangsmåde fokuserer på flytning af planlagte kanban-procesjob til en anden periode."
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 5f101a097643fa027a667b9d6577fbe5d24ecd27
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="move-scheduled-kanban-jobs"></a>Flytte planlagte kanban-job

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåde fokuserer på flytning af planlagte kanban-procesjob til en anden periode. Det demodatafirma, der bruges til at oprette denne procedure, er USMF. Denne procedure er beregnet til tilsynsførende eller produktionsplanlæggere, der arbejder med kanbans.


## <a name="select-scheduled-kanban-jobs"></a>Vælg planlagte kanban-job
1. Gå til Produktionsstyring > Kanban > Tidsplanlægning af kanban-job.
2. !MtCMR!Klik på rullelisten i feltet Arbejdscelle for at åbne opslaget. áçêìõý !
3. Markér den valgte række på listen.
    * Vælg arbejdscelle 1250.  
4. Klik på Vælg.
5. Vælg 'Planlagt' i feltet Vis jobstatus.
    * Dette filtrerer joblisten, så du får vist de planlagte kanban-job.  

## <a name="move-kanban-jobs-to-a-different-period"></a>Flyt kanban-job til en anden periode.
1. Find og vælg den ønskede post på listen.
    * Vælg et job, der har statussen Planlagt job, f.eks et job, der er planlagt til 20. december 2012 i feltet Planlagt periode. Flyt derefter jobbet til forrige periode.  
2. Klik på Forrige periode.
3. Klik på Afslut.
    * Dette vil flytte jobbet til slutningen af joblisten som det sidste job i den foregående periode.  
4. Find og vælg den ønskede post på listen.
    * Vælg et job, der har statussen Planlagt job, f.eks et job, der er planlagt til 18. december 2012 i feltet Planlagt periode. Flyt derefter jobbet til næste periode.  
5. Klik på Næste periode.
6. Klik på Start.
    * Dette vil flytte jobbet til starten af joblisten som det første job i den foregående periode.  

## <a name="task-move-a-job-within-a-period"></a>Opgave: Flyt et job inden for en periode
1. Find og vælg den ønskede post på listen.
    * Vælg et job, der har statussen Planlagt job, f.eks det andet job, der er planlagt til 19. december 2012, i feltet Planlagt periode. Flyt derefter jobbet inden for den planlagte periode.  
2. Klik på Videresend.
    * Bemærk, at jobbet er flyttet én linje ned på listen.  
3. Klik på Bagud.
    * Bemærk, at jobbet er flyttet én linje op på listen.  


