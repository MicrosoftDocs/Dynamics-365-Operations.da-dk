--- 
title: "Føje en beregningspolitik for kanban-mængder til en kanban-regel"
description: "Denne fremgangsmåde drejer sig om oprettelse af en politik for beregning af kanban-mængde og føje den til en kanban-regel til optimering af kanban-størrelse og mængde."
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
ms.openlocfilehash: f9e0ccf25a346d54e48f51b0866f0c11e98bf0a0
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="add-a-kanban-quantity-calculation-policy-to-a-kanban-rule"></a>Føje en beregningspolitik for kanban-mængder til en kanban-regel

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåde drejer sig om oprettelse af en politik for beregning af kanban-mængde og føje den til en kanban-regel til optimering af kanban-størrelse og mængde. Det demodatafirma, der bruges til at oprette denne procedure, er USMF. Denne procedure er beregnet til værdistrømlederen. Denne procedure er en forudsætning for oprettelse af proceduren Beregn kanban-mængdeforslag. 


## <a name="create-a-kanban-quantity-calculation-policy"></a>Opret en politik til beregning af kanban-mængde
1. Gå til Produktionsstyring > Periodiske opgaver > Beregning af kanban-mængde > Politikker for beregning af kanban-mængder.
2. Klik på Ny.
3. Skriv en værdi i feltet Navn.
    * Skriv f.eks. Speaker2016.  
4. Klik på rullelisten i feltet Behovsplan for at åbne opslaget.
5. Find og vælg den ønskede post på listen.
    * Vælg StaticPlan for at beregne behov.  
6. Klik op linket i den valgte række på listen.
7. Klik på Gem.
8. Indtast "1" i feltet Mindste kanban-mængde.
    * Dette er det ekstra antal kanbans, der er medtaget i beregningen af kanban-mængder.  
9. Indstil Sikkerhedsfaktor til "1".
    * Dette er den faktor, der bruges til at beregne den ekstra mængde sikkerhedslager.  
10. Angiv "30" i feltet Dage forud.
    * Dette er det antal dage før beregningsdatoen af kanban-mængde, der er medtager i behovsberegningen.  
11. Angiv "30" i feltet Dage bagud.
    * Dette er antallet af dage regnet fra den kanban-mængdeberegningsdato, der er medtaget i efterspørgselsberegningen.  Formlen bruges til beregningen vises med de faktiske værdier. For eksempel, Kanban-mængde = ((gennemsnitlig daglig efterspørgsel x 2.00) + sikkerhedslager)/produktmængde pr. håndteringsenhed + 1  
12. Luk siden.

## <a name="add-the-kanban-quantity-calculation-policy-to-a-kanban-rule"></a>Føj politikken til beregning af kanban-mængde til en kanban-regel
1. Gå til Administration af produktoplysninger > Lean manufacturing > Kanban-regler.
2. Find og vælg den ønskede post på listen.
    * Vælg kanban-regel 000020 for denne procedure.  
3. Klik op linket i den valgte række på listen.
4. Slå udvidelse af sektionen Politikker for beregning af kanban-mængder til/fra.
5. Klik på Tilføj.
    * Tilføj politik for beregning af den kanban-mængde, du lige har oprettet i forrige underopgave.  
6. Markér den valgte række på listen.
7. Klik på rullelisten i feltet Navn for at åbne opslaget.
8. Klik op linket i den valgte række på listen.
    * Vælg politikken, Speaker2016, du lige har oprettet i forrige underopgave.  


