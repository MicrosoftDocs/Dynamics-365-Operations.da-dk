--- 
title: Opdatere status for kanban
description: "Når en kanban bliver tømt ved en fejltagelse eller en modtaget kanban skal tømmes, skal du opdatere kanban-statussen."
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: Kanban, KanbanResetEmpty
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3c2b5a5fbfc5bd83cc68ffafaa243dac9244c003
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="update-kanban-status"></a>Opdatere status for kanban

[!include [task guide banner](../../includes/task-guide-banner.md)]

Når en kanban bliver tømt ved en fejltagelse eller en modtaget kanban skal tømmes, skal du opdatere kanban-statussen. Det demodatafirma, der bruges til at oprette denne procedure, er USMF. Denne procedure er beregnet til den tilsynsførende.


## <a name="find-the-kanban"></a>Find kanban.
1. Gå til Produktionsstyring > Kanban > Kanbans.
2. Åbn kolonnefilteret Status på håndteringsenhed.
3. Klik på Ryd.
    * Dette nulstiller filtrene.  
4. Brug Quick Filter til at finde poster. Filtrer f.eks. efter feltet Kortnummer med værdien '000149'.

## <a name="change-emptied-status-to-received-status"></a>Ændre statussen Tømt til Modtaget
1. Klik på Fortryd tømning af materialehåndteringsenhed.
2. Klik på OK.
    * Bemærk, at Status på håndteringsenhed er Modtaget.  

## <a name="change-received-status-to-emptied-status"></a>Ændre statussen Modtaget til Tømt
1. Klik på Tøm kanban.
2. Markér den valgte række på listen.
    * Bemærk, at Status på håndteringsenhed er Tømt.  


