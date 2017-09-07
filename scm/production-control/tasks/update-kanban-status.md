--- 
title: Opdatere status for kanban
description: "Når en kanban bliver tømt ved en fejltagelse eller en modtaget kanban skal tømmes, skal du opdatere kanban-statussen."
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2016
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
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: caf7dead2da14e1ff76e205e7477b1eb11a2ca52
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="update-kanban-status"></a>Opdatere status for kanban

[!include[task guide banner](../../includes/task-guide-banner.md)]

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

