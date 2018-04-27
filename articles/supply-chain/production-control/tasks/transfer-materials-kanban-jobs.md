--- 
title: "Overføre materialer med kanban-job (kun februar 2016)"
description: "Denne fremgangsmåde fokuserer på at udtrække et kanban-job for at overføre materialer."
author: ChristianRytt
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c79480d844627a7eed8129515924f1f70ad04f95
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="transfer-materials-with-kanban-jobs-february-2016-only"></a>Overføre materialer med kanban-job (kun februar 2016)

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåde fokuserer på at udtrække et kanban-job for at overføre materialer. Det demodatafirma, der bruges til at oprette denne procedure, er USMF. Denne procedure er beregnet til lagerarbejderen.


## <a name="display-transfer-jobs"></a>Vis Overførselsjob
1. Gå til Produktionsstyring > Kanban > Kanban-område til overførselsjob.
2. Udvis eller skjul sektionen Filtre.
    * I sektionen Filtre kan du angive, hvilke job du vil se ved at filtrere på Produktionsflow, Navn på aktivitet, Fra lagersted og lokalitet og Til lagersted og lokalitet.  
3. Skriv "11" i feltet Fra lagersted.
4. Skriv "12" i feltet en Til lokalitet.

## <a name="start-a-transfer-job"></a>Start et overførselsjob
1. Fjern markeringen af den valgte række, hvis der er en, på listen.
2. Markér række 4 på listen.
    * Vælg det første job med status som ikke-planlagt. Kontrollér, at dette er det eneste job, der er valgt.  
3. Klik på Start.
    * Bemærk, at et ikon angiver, at jobbet er startet.  

## <a name="select-a-second-transfer-job-and-change-quantity"></a>Vælg et andet overførselsjob, og ret mængde
1. Find og vælg den ønskede post på listen.
    * Du kan vælge flere job, men vælg række 5 for nu.  
2. Find og vælg den ønskede post på listen.
    * Kontrollér, at jobbet i det forrige trin er det eneste, der er valgt. Fravælg alle andre job.  
3. Notér værdien i feltet Jobantal til fremtidig reference
4. Indstil Jobantal til "30".
    * Bemærk advarslen! Du har ikke tilladelse til at overføre 30. Du kan kun overføre den oprindelige mængde i overensstemmelse med opsætningen af kanban-reglen.  
5. Brug den værdi, der tidligere er noteret i feltet Jobantal
    * Angiv Jobantallet til den forrige værdi.  

## <a name="start-the-second-transfer-job"></a>Start det andet overførselsjob
1. Klik på Start.
    * Dette starter overførslen af jobbet i række 5.  

## <a name="complete-both-transfer-jobs"></a>Udfør begge overførselsjob
1. Markér række 4 på listen.
    * Nu vælges to overførselsjob på række 4 og række 5.  
2. Klik på Fuldført.
    * Dette fuldfører overførsel af begge job.  


