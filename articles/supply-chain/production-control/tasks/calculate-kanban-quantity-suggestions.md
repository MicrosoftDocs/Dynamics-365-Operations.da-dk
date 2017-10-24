--- 
title: "Beregne forslag til kanban-mængder"
description: "Denne fremgangsmåde fokuserer på optimering af kanban-størrelse og -mængder for en specifik kanban-regel ved at bruge beregningen af kanban-mængden."
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
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: a817dbc02890d863f68c5bf2a6cc11b9a5328060
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="calculate-kanban-quantity-suggestions"></a>Beregne forslag til kanban-mængder

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåde fokuserer på optimering af kanban-størrelse og -mængder for en specifik kanban-regel ved at bruge beregningen af kanban-mængden. Det demodatafirma, der bruges til at oprette denne procedure, er USMF. Denne procedure er beregnet til værdistrømlederen. Det er en forudsætning, at du har gennemført proceduren Føj en ny politik til beregning af kanban-mængde til en kanban-regel.


## <a name="create-a-kanban-quantity-calculation"></a>Opret en beregning af kanban-mængde
1. Gå til Produktionsstyring > Periodiske opgaver > Beregning af kanban-mængde > Beregn kanban-mængde.
2. Klik på Ny.
3. Skriv "Speaker2016" i feltet Navn.
4. Klik på rullelisten i feltet Navn for at åbne opslaget.
    * Vælg den politik, du har oprettet i proceduren Føj en politik til beregning af kanban-mængde til en kanban-regel. F.eks. Speaker2016.  
5. Klik op linket i den valgte række på listen.
6. I feltet Regel aktiv fra og med dato skal du angive dato og klokkeslæt til "2012-12-17T08:00:00".
    * Den dato bruges som basis for bestemmelse af, hvilke faste kanban-regler der medtages i beregning af kanban-mængden.  
7. I feltet Opfyldt efterspørgselsperiodes startdato skal du angive dato og klokkeslæt til "2012-11-17T09:00:00".
    * Datoen, fra hvilken tidligere efterspørgselstransaktioner medtages til beregning af kanban-mængden.  
8. I feltet Opfyldt efterspørgselsperiodes slutdato skal du angive dato og klokkeslæt til "2012-12-17T07:59:59".
    * Datoen, indtil hvilken tidligere efterspørgselstransaktioner medtages til beregning af kanban-mængden.  
9. I feltet Efterspørgselsperiodens startdato skal du angive dato og klokkeslæt til "2012-12-17T08:00:00".
    * Datoen, fra hvilken aktuelle efterspørgselstransaktioner medtages til beregning af kanban-mængden.  
10. I feltet Efterspørgselsperiodens slutdato skal du angive dato og klokkeslæt til "2013-01-16T07:59:59".
    * Datoen, indtil hvilken aktuelle efterspørgselstransaktioner medtages til beregning af kanban-mængden.  

## <a name="generate-kanban-quantity-proposal"></a>Generer forslag til kanban-mængde
1. Klik på Gem.
2. Klik på Generer.
    * Dette genererer en forslagslinje til kanban-mængde i kanban-reglen 000020.  

## <a name="run-kanban-quantity-calculation"></a>Kør beregning af kanban-mængde
1. Klik på Beregn.
    * Derved beregnes forslaget til kanban-mængde.  
2. Klik på OK.
3. Markér den valgte række på listen.
    * Bemærk, at den foreslåede kanban-mængden er 2.  

## <a name="change-product-quantity-and-calculate-again"></a>Ændr produktmængde, og beregn igen
1. Angiv Produktmængde til "5".
2. Klik på Beregn.
3. Klik på OK.
    * Bemærk, at med en kanban-mængde på 5 ændres forslaget til en kanban-mængde på 4.  
    * Dette skyldes, at med en lavere produktmængde har vi brug for flere kanbans for at opfylde behovet.  

## <a name="update-kanban-rule"></a>Opdater kanban-regel
1. Angiv en dato og et klokkeslæt i feltet Reglens ikrafttrædelsesdato.
    * Angiv "Regel aktiv fra og med dato" til en dato i fremtiden. F.eks. dags dato + et år.  
2. Klik på Opdater.
3. Klik på OK.
4. Luk siden.

## <a name="validate-change-on-kanban-rule"></a>Valider ændring af kanban-regel
1. Gå til Administration af produktoplysninger > Lean manufacturing > Kanban-regler.
2. Klik op linket i den valgte række på listen.
    * Vælg den kanban-regel, der er oprettet i den tidligere underopgave. Dette bør være den første kanban-regel på listen sorteret efter nummer.  
3. Slå udvidelsen af sektionen afsnittet Detaljer til/fra.
    * Bemærk ikrafttrædelsesdatoen, hvilket betyder at denne regel ikke aktiveres før denne dato.  
4. Slå udvidelsen af sektionen Antal til/fra.
    * Bemærk, at dette er den standardmængde, som du angav i beregningen af kanban-mængden.  
    * Bemærk, at dette er den faste kanban-mængde på 4 fra beregningen af kanban-mængden.  
5. Klik på fanen ListPanel.


