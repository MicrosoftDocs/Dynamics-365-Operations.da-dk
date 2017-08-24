--- 
title: "Ændre kanban-regler for et procesjob"
description: "Denne procedure drejer sig om ændring af den brugte kanban-regel for en bestemt kanban."
author: ChristianRytt
manager: AnnBe
ms.date: 03/02/2016
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: e8355a94322e6489fe64f22a049a34b7ecfe65b9
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="change-kanban-rules-for-a-process-job"></a>Ændre kanban-regler for et procesjob

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne procedure drejer sig om ændring af den brugte kanban-regel for en bestemt kanban. Dette er nyttigt til belastningsudjævning af ressourcer eller i tilfælde af nedbrud. Det demodatafirma, der bruges til at oprette denne procedure, er USMF. Denne procedure er beregnet til planlæggeren, der arbejder på en lean manufacturing-virksomhed og er ansvarlig for værdistrømmen.


## <a name="copy-kanban-rule"></a>Kopiere kanban-regel
1. Gå til kanban-regler.
2. Find og vælg den ønskede post på listen.
    * Vælg hændelses-kanban-regel 000022 for L0001.  
3. Klik på Dupliker kanban-regel.
4. Klik på OK.

## <a name="change-kanban-rule"></a>Redigere kanban-regel
1. Luk siden.
2. Gå til Tidsplanlægning af kanban-job.
3. Markér den valgte række på listen.
    * Vælg linjen med Kanban 000177.  
4. Klik på Brug en anden kanban-regel.
5. Klik på Næste.
6. Indtast eller vælg en værdi i feltet Kanban-regel.
    * Vælg den kanban-regel, der blev oprettet tidligere. Dette er kanban-reglen med det højeste nummer.  
7. Klik på Finish.
    * Kanban-jobbet bruger nu en anden kanban-regel. Dette kan være nyttigt ved belastningsudjævning af arbejdsceller.  


