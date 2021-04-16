---
title: Om udligning fra salgsordrer
description: Denne procedure fokuserer på validering af udligningstræet fra en salgslinje, hvor varen produceres med kanbans.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ff57169ea58a90d1113bb7ef0a581f900e62a9b2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828556"
---
# <a name="lean-pegging-from-sales-orders"></a>Om udligning fra salgsordrer

[!include [banner](../../includes/banner.md)]

Denne procedure fokuserer på validering af udligningstræet fra en salgslinje, hvor varen produceres med kanbans. Efter validering af udligningstræet, er alle kanban-job planlagt. Dette er nyttigt for ordrescenarier, hvor ordretageren skal sikre, at produktionen kan påbegyndes straks. Det demodatafirma, der bruges til at oprette denne procedure, er USMF. Denne procedure er beregnet til den avancerede ordretager, der arbejder i en lean virksomhed.


## <a name="create-a-sales-order-for-a-kanban-controlled-item"></a>Oprette en salgsordre for en kanban-kontrolleret vare
1. Gå til Alle salgsordrer.
2. Klik på Ny.
3. Indtast eller vælg en værdi i feltet Kundekonto.
    * Brug US-001.  
4. Klik på OK.
5. Skriv 'L0001' i feltet Varenummer.
6. Angiv antallet til '30'.
    * Det er vigtigt, at mængden er større end 24 for at udløse hændelsens kanban-regel.  

## <a name="open-a-pegging-tree"></a>Åbne et udligningstræ 
1. Klik på Produkt og forsyning.
2. Klik på Vis udligningstræ.
    * Bemærk, at udligningstræet viser alle niveauer af udligning, der er nødvendige for salgsordrelinjen. I dette tilfælde er der to niveauer af kanbans og alle de nødvendige komponenter.  

## <a name="plan-the-pegging-tree"></a>Planlæg udligningstræet
1. I træet vælg "Salgslinje 000832\Kanban 000558".
2. Udvid sektionen Kanban-job.
    * Bemærk, at jobstatus for kanban-jobbet er Ikke planlagt.  
3. Klik på Planlæg hele udligningstræet.
    * Dette vil planlægge alle kanban-job i udligningstræet, ændre jobstatus fra ikke-planlagt til planlagt.  
4. Opdater siden.
    * Bemærk, at den pågældende kanban jobstatus blev ændret fra Ikke planlagt til Planlagt.  
5. Vælg "Salgslinje 000832\Kanban 000558\Afgang for L0001\Kanban 000559" i træet.
    * Jobbet for den anden kanban er også planlagt, fordi hele udligningstræet er planlagt. Bemærk, at den pågældende kanbanjobstatus blev ændret fra Ikke planlagt til Planlagt.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]