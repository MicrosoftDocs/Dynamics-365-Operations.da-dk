---
title: Opdatere status for kanban
description: Når en kanban bliver tømt ved en fejltagelse eller en modtaget kanban skal tømmes, skal du opdatere kanban-statussen.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Kanban, KanbanResetEmpty
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 741a2a29e6b222c722e94db4e07dee6c8f4014030364753e3352fa30594dac0d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6715668"
---
# <a name="update-kanban-status"></a>Opdatere status for kanban

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]