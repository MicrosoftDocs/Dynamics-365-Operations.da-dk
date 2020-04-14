---
title: Forberede et kanban-procesjob, når materialer er tilgængelige for arbejdscellen
description: Denne opgave fokuserer på at klargøre et kanban-procesjob, når alle materialerne ikke er tilgængelige for arbejdscellen.
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cf163968474e91da7e3d47fd638a857a76179645
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148957"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-available-for-the-work-cell"></a>Forberede et kanban-procesjob, når materialer er tilgængelige for arbejdscellen

[!include [banner](../../includes/banner.md)]

Denne opgave fokuserer på at klargøre et kanban-procesjob, når alle materialerne ikke er tilgængelige for arbejdscellen. Det demodatafirma, der bruges til at oprette denne opgave, er USMF. Denne opgave er beregnet til maskinoperatøren.

1. Gå til Kanban-område til procesjob.
2. Klik på rullelisten i feltet Arbejdscelle for at åbne opslaget.
3. Klik op linket i den valgte række på listen.
    * Vælg arbejdscelle 1250, og klik på OK.  
4. Markér række 4 på listen.
    * I det rene demofirma er Kanban 000329 i række 4 det første job, der ikke er fuldført endnu.  
5. Slå udvidelsen af sektionen Plukliste til/fra.
    * Kontrollér, at forsyningsstatus er tilgængelig for alle varer på pluklisten.  
    * Hvis flere job er markeret, viser pluklisten summen af alle varer, der er nødvendige for de valgte job.  
6. Klik på Klargør.
    * Klargøringsprocessen er nu fuldført. Det markerede afkrydsningsfelt for alle rækker på pluklisten angiver, at forsyningsstatus er plukket.  

