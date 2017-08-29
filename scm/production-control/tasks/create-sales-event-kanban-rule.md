--- 
title: "Oprette en kanban-regel for salgshændelse"
description: "Denne procedure fokuserer på den opsætning, der er nødvendig for at oprette en kanban-regel, som udløses under oprettelse af en salgsordre."
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
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 2d446b63041e00ae12ecbed501925afc46a90ca7
ms.contentlocale: da-dk
ms.lasthandoff: 07/28/2017

---
# <a name="create-a-sales-event-kanban-rule"></a>Oprette en kanban-regel for salgshændelse

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne procedure fokuserer på den opsætning, der er nødvendig for at oprette en kanban-regel, som udløses under oprettelse af en salgsordre. Hændelses-kanban-reglen genbestiller krav, der stammer fra salgsordrelinjer. Det demodatafirma, der bruges til at oprette denne procedure, er USMF. Den er beregnet til procesingeniøren eller værdistrømlederen, når de forbereder produktionen af et nyt eller ændret produkt.




## <a name="create-a-new-kanban-rule"></a>Opret en ny kanban-regel
1. Gå til kanban-regler.
2. Klik på Ny.
3. Vælg "Hændelse" i feltet Genopfyldningsstrategi.
    * Hvis Hændelse vælges, betyder det, at kanban-reglen udløses af en hændelse, for eksempel oprettelse af en salgsordrelinje.   Dette gælder for områder, hvor hver kanban skal dække et specifikt behov.  
4. Angiv eller vælg en værdi i feltet Første planaktivitet.
    * Vælg Endelig samling.  
5. Udvid afsnittet Detaljer.
6. Indtast eller vælg en værdi i feltet Produkt.
    * Vælg L0050.  

## <a name="define-an-event"></a>Definere en hændelse
1. Udvid afsnittet Hændelse.
2. Vælg "Automatisk" i feltet Salgshændelse.
    * Hvis salgshændelsen Automatisk vælges, udløses denne kanban-reglen automatisk, når en salgslinje svarer til produktet og modtagelseslokaliteten. I denne procedure er det produkt L0050 på lager 13.  
3. Angiv Mindste antal hændelser "50".
    * Med et minimumantal af hændelser på 50 udløses kanban-reglen kun af hændelser med et antal på 50 eller derover.  
4. Udvid sektionen Produktionsflow.
    * Bemærk, at Modtagelseslokalitet er lager 13. Det betyder, at denne kanban-regel udløses for denne lokalitet.  
    * I dette eksempel udløses kanban-reglen af en salgslinje for produktet L0050 med et antal på 50 eller derover på lager 13.  

## <a name="create-sales-line-to-trigger-event-kanban-rule"></a>Oprette salgslinje for at udløse hændelses-kanban-regel
1. Gå til Alle salgsordrer.
    * Der vises en advarsel, når kanban-reglen gemmes, hvilket betyder, at der oprettes kanbans i realtid under oprettelse af salgsordrer.  
2. Klik på Ny.
3. Indtast eller vælg en værdi i feltet Kundekonto.
    * Vælg f.eks. US-003.  
4. Klik på OK.
5. Skriv 'L0050' i feltet Varenummer.
6. Skriv "1" i feltet Sted.
    * Vælg Sted 1, fordi lageret 13 er på Sted 1.  
7. Indtast eller vælg en værdi i feltet Lagersted.
    * Angiv Lagersted til 13.  
8. Angiv antallet til '75'.
    * Angiv et mængde på 50 eller derover for at udløse den oprettede kanban-regel.  

## <a name="verify-that-kanban-is-created"></a>Kontroller, at kanban er oprettet
1. Klik på Produkt og forsyning.
2. Klik på Vis udligningstræ.
    * Bemærk, at der oprettes en kanban med den samme mængde som salgslinjen. Du kan også se de materialeproblemer, der er nødvendige for at producere L0050. Dette er det sidste trin i denne procedure.  


