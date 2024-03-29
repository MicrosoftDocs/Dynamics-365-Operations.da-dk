---
title: Udføre kanban-procesjob
description: Denne procedure drejer sig om at udføre kanban-procesjob.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7ac6f0f6139fe17532f6fbd996b314e0b14f3d90
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566573"
---
# <a name="execute-kanban-process-jobs"></a>Udføre kanban-procesjob

[!include [banner](../../includes/banner.md)]

Denne procedure drejer sig om at udføre kanban-procesjob. Det første job er fuldført med det forventede antal og har ingen fejl. Det andet job er fuldført med fejl. Det demodatafirma, der bruges til at oprette denne procedure, er USMF. Denne procedure er beregnet til maskinoperatøren.


## <a name="select-a-kanban-job"></a>Vælge et kanban-job
1. Gå til Produktionsstyring > Kanban > Kanban-område til procesjob.
2. Klik på rullelisten i feltet Arbejdscelle for at åbne opslaget.
3. Klik på rækken med ressourcegruppen 1250. Dette filtrerer joblisten, så du kun får vist job for arbejdscelle 1250.
    * Markér den række, der har statussen Planlagt job.  

## <a name="complete-a-job-with-expected-quantity"></a>Fuldføre et job med forventet antal
1. Vis eller skjul sektionen Detaljer.
    * Denne sektion viser vigtige oplysninger om kortnummer, varenummer, bestilt antal og aktivitetsnavn.  
2. Udvid eller skjul sektionen Produktionsinstruktioner.
    * Denne sektion viser produktionsinstruktioner for aktiviteten. Instruktionerne kan bestå af tekst, billeder, tegninger og andre dokumenter.  
3. Klik på Start.
    * Vælg et job, der ikke er fuldført. Brug statusikoner i feltet Jobstatus til at få vist jobstatus.      
4. Klik på Fuldført.
    * Jobbet er fuldført med den forventede kvalitet.  

## <a name="complete-a-job-with-errors"></a>Fuldføre et job med fejl
1. Klik på Start.
    * Når et job er fuldført, vælges det næste job på listen automatisk. Dette er grunden til, at du ikke behøver at vælge et job, før du klikker på Start.  
2. Klik på Produktion i handlingsruden.
3. Klik på Udført (detaljer).
4. Markér den valgte række på listen.
5. Indtast et tal i feltet Antal fejl.
6. Indtast et tal i feltet Antal gode.
7. Klik på OK.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]