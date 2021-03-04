---
title: Fjerne et kanban-job fra planen
description: Denne fremgangsmåde fokuserer på at fjerne et planlagt kanban-procesjob fra tidsplanen ved at gendanne jobstatussen til Ikke planlagt.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, SysLookupMultiSelectGrid, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0236faa9b534678ed232ac3572c8172c62e5241f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424323"
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