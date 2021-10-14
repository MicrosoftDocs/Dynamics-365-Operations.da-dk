---
title: Fjerne et kanban-job fra planen
description: Denne fremgangsmåde fokuserer på at fjerne et planlagt kanban-procesjob fra tidsplanen ved at gendanne jobstatussen til Ikke planlagt.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, SysLookupMultiSelectGrid, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 838270189e08065f791c9e58888351025e0a6df8
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573627"
---
# <a name="remove-a-kanban-job-from-the-schedule"></a>Fjerne et kanban-job fra planen

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåde fokuserer på at fjerne et planlagt kanban-procesjob fra tidsplanen ved at gendanne jobstatussen til Ikke planlagt. Det demodatafirma, der bruges til at oprette denne procedure, er USMF. Denne procedure er beregnet til tilsynsførende eller produktionsplanlæggere.


## <a name="find-a-planned-kanban-job"></a>Find et planlagt kanban-job
1. Gå til Produktionsstyring > Kanban > Tidsplanlægning af kanban-job.
2. Klik på rullelisten i feltet Arbejdscelle for at åbne opslaget.
3. Klik op linket i den valgte række på listen.
    * Vælg arbejdscelle 1250.  
4. Klik på Vælg.
5. Vælg "Planlagt" i feltet Vis jobstatus.

## <a name="remove-the-planned-kanban-job-from-the-schedule"></a>Fjern det planlagte kanban-job fra tidsplanen
1. Find og vælg den ønskede post på listen.
    * Vælg et job, der har statussen Planlagt, for eksempel et job fra 19. december 2012.  
2. Klik på Plan i handlingsruden.
3. Klik på Gendan jobstatus.
4. Klik på OK.
    * Dette vil gendanne jobbets aktuelle status fra "Planlagt" til "Ikke planlagt" og fjerne det fra procesområdet.   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]