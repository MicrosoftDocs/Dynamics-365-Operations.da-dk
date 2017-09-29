--- 
title: "Planlægge kanban-job"
description: "Denne fremgangsmåde fokuserer på planlægning af kanban-procesjob for en bestemt arbejdscelle."
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
ms.openlocfilehash: 88399f70a3c286d536637e166e8428eae50a561d
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="schedule-kanban-jobs"></a>Planlægge kanban-job

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåde fokuserer på planlægning af kanban-procesjob for en bestemt arbejdscelle. Proceduren "Klargør et kanban-procesjob, når materialerne ikke er tilgængelige" er en forudsætning for oprettelsen af denne procedure. Det demodatafirma, der bruges til at oprette denne procedure, er USMF. Denne opgave er beregnet til tilsynsførende og produktionsplanlæggere, der arbejder med kanbans.


## <a name="select-kanban-jobs-for-a-work-cell"></a>Vælg kanban-job til en arbejdscelle
1. Gå til Produktionsstyring > Kanban > Tidsplanlægning af kanban-job.
2. Udvid faktaboksen Periodekapacitet
    * Udvid faktaboksen Kanban.  
3. Klik på rullelisten i feltet Arbejdscelle for at åbne opslaget.
4. Markér den valgte række på listen.
    * Vælg arbejdscelle 1250. Dette vil filtrere visningen, så du kun får vist job for arbejdscelle 1250.  
5. Klik op linket i den valgte række på listen.
6. Klik på Vælg.

## <a name="schedule-a-kanban-job-in-the-first-available-period"></a>Planlæg et kanban-jobbet i den første tilgængelige periode.
1. Markér den valgte række på listen.
    * Markér den første række på listen, der har statussen Ikke planlagt. Ikonet med prikker i feltet Jobstatus angiver ikke-planlagte.  
2. Klik på Planlæg.
    * Dette vil planlægge kanban-jobbet i den første tilgængelige periode.  
    * Bemærk, at kanban-jobbet flyttes til slutningen af listen, fordi den er blevet føjet til den periode, der starter fra dags dato.  
    * Hvis den periode, der starter fra i dag er fuldt booket, flyttes jobbet til den første tilgængelige periode.  

## <a name="schedule-two-kanban-jobs-for-a-specific-day"></a>Planlæg to kanban-job for en bestemt dag
1. Markér række 1 på listen.
    * Du bør se, at den første række har statussen Ikke planlagt i feltet Jobstatus.  
2. Markér række 2 på listen.
    * Du bør se, at den anden række har statussen Ikke planlagt i feltet Jobstatus. Du har nu de to første job, der er valgt.  
3. Klik på Planlæg fra dato for at åbne dialogboksen.
4. Markér eller fjern markeringen i boksen Tilsidesæt reaktion på manglende kapacitet.
    * Denne indstilling giver dig mulighed for at tilsidesætte standardreaktionen på manglende kapacitet.  
5. Vælg "Føj til den angivne periode" i feltet Reaktion på manglende kapacitet.
    * Denne indstilling sikrer, at jobbet føjes til den angivne periode, uanset om arbejdscellen muligvis er overbelastet.  
6. Klik på Planlæg.
    * Bemærk, at begge job er føjet til den ønskede periode.  
    * Du kan se belastningen for hver periode i sektionen Periodekapacitet. Feltet Forbrug viser det planlagte forbrug i denne periode. Hvis det planlagte forbrug er højere end den tilgængelige kapacitet i denne periode, vælges det overbelastede forbrug.  

