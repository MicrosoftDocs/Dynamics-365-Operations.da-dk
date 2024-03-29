---
title: Forberede et kanban-procesjob, når materialer ikke er tilgængelige for arbejdscellen
description: Denne procedure drejer sig om at forberede et kanban-procesjob, når visse materialer ikke er tilgængelige for arbejdscellen, og det derfor er nødvendigt at plukke materialer fra lageret.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2f75cdbc6ce6f7e427bf266c90428d73c065eac3
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7576730"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-not-available-for-the-work-cell"></a>Forberede et kanban-procesjob, når materialer ikke er tilgængelige for arbejdscellen

[!include [banner](../../includes/banner.md)]

Denne procedure drejer sig om at forberede et kanban-procesjob, når visse materialer ikke er tilgængelige for arbejdscellen, og det derfor er nødvendigt at plukke materialer fra lageret. Proceduren "Klargør et kanban-procesjob, når materialerne er tilgængelige" er en forudsætning for oprettelsen af denne procedure. Denne procedure er beregnet til maskinoperatøren. Det demodatafirma, der bruges til at oprette denne procedure, er USMF.

1. Gå til Produktionsstyring > Kanban > Kanban-område til procesjob.
2. Klik på rullelisten i feltet Arbejdscelle for at åbne opslaget.
3. Klik op linket i den valgte række på listen.
    * Vælg arbejdscelle 1250.  
4. Find og vælg den ønskede post på listen.
    * Vælg kanban 000356.  
5. Find og vælg den ønskede post på listen.
    * Fjern markeringen af række 4 på listen. eller vælg række 4, hvis du ikke har fuldført opgaven "Forberede et kanban-procesjob, når materialer er tilgængelige for arbejdscellen".  
6. Slå udvidelsen af sektionen Plukliste til/fra.
    * Ikonet Ingen post under forsyningsstatus angiver, at 48 ea for vare P0002 mangler for arbejdscellen.  

## <a name="transfer-materials-to-work-cell"></a>Overfør materialer til arbejdscelle
1. Slå udvidelsen af sektionen Overførselsjob til/fra.
2. Brug Quick Filter til at filtrere på feltet Varenummer med værdien 'P0002'.
3. Find og vælg den ønskede post på listen.
4. Klik på Start.
    * Overførsel er i gang.  
5. Klik på Fuldført.
    * Vare P0002 er nu tilgængelig på pluklisten for kanban-jobbet. Det betyder, at vi kan klargøre kanban med alle de nødvendige materialer.  
6. Klik på Klargør.
    * Bemærk, at et ikon i Jobstatus angiver, at jobbet nu er klart.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]