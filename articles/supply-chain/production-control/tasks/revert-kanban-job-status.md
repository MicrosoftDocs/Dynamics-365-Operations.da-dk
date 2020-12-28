---
title: Gendan status for kanban-job
description: Denne procedure fokuserer på at vende tilbage til en forkert kanban-jobstatus.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9cca5ea3a4c33c7f36acd18a8af7034466b3b580
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424590"
---
# <a name="revert-kanban-job-status"></a>Gendan status for kanban-job

[!include [banner](../../includes/banner.md)]

Denne procedure fokuserer på at vende tilbage til en forkert kanban-jobstatus. Dette er nyttigt i tilfælde af, at maskinoperatøren opdaterer det forkerte job eller angiver forkert status ved en fejltagelse. I denne procedure er et kanban-job registreret som fremstillet ved en fejltagelse, og status er tilbageført. Det demodatafirma, der bruges til at oprette denne procedure, er USMF. Denne procedure er beregnet til den tilsynsførende eller maskinoperatøren, der arbejder i en virksomhed med lean manufacturing.


## <a name="open-process-board-for-the-work-cell"></a>Åbn procesområdet for arbejdscellen.
1. Gå til Kanban-område til procesjob.
2. Indtast eller vælg en værdi i feltet Arbejdscelle.
    * Vælg arbejdscelle 1260.  

## <a name="prepare-kanban-job"></a>Klargøre kanban-job
1. Klik på Klargør.
    * Hvis du ikke kan klikke på Forbered, fordi det er nedtonet, skal du sørge for, at det valgte kanban-job har statussen Planlagt, som angives af det tomme kanban-ikon. Hvis Forbered mislykkes, skal du kontrollere, at alle materialer på pluklisten, er tilgængelige.  
2. Vælg det klargjorte job på listen.
    * Vælg det første job, du lige har klargjort.  
    * Bemærk, at jobstatus er forberedt, hvilket er angivet med en trekant i kanban-ikonet.  

## <a name="revert-the-status-of-the-prepared-kanban-job"></a>Tilbageføre status for det forberedte kanban-job
1. Markér den valgte række på listen.
    * Vælg det første job, der blev klargjort.  
2. Klik på Produktion i handlingsruden.
3. Klik på Genindlæs status.
    * Du kan bruge en alternativ kanban-regel, når følgende betingelser er opfyldt: - Genopfyldningsstrategien er den samme for begge regler.  - Versionen af produktionsflowet er den samme for begge regler.  - Det produkt, der leveres, er det samme for begge regler.  - Enhver downstream-aktivitet, der er konfigureret for den sidste aktivitet i kanban-reglerne, skal være den samme for begge regler.  - De samme angivne lagerdimensioner skal være konfigureret til begge regler.  - Status for materialehåndteringsenheden skal være Ikke-tildelt.  - Konfigurationen for hændelses-kanbans skal være den samme.  
    * Sørg for, at den nye status er Planlagt.  
4. Klik på OK.
5. Fjern markeringen af den valgte række på listen.
    * Vælg det samme job.  
    * Bemærk, at jobstatus for kanban-jobbet er ført tilbage til Planlagt, hvilket angives med et tomt kanban-ikon.  

