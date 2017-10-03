--- 
title: Vis arbejdsgangshistorik
description: "Brug disse trin for at få vist statussen for et dokument, der er sendt til arbejdsgangssystemet til behandling og godkendelse."
author: jasongre
manager: AnnBe
ms.date: 02/21/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: a0e16467972596ad6d8b0d9785e68b487150781c
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="view-workflow-history"></a>Vis arbejdsgangshistorik

[!include[task guide banner](../../includes/task-guide-banner.md)]

Brug disse trin for at få vist statussen for et dokument, der er sendt til arbejdsgangssystemet til behandling og godkendelse. Det demodatafirma, der bruges til at oprette denne procedure, er USMF.

1. Gå til Generelt > Forespørgsler > Arbejdsgang > Arbejdsgangshistorik.
    * Brug denne formular til at få vist status for et dokument, der er sendt til arbejdsgangssystemet til behandling og godkendelse.  
    * Forekomst-id'et er identifikationskoden for den arbejdsgangsforekomst, der behandler eller har behandlet dokumentet.  
    * Status for arbejdsgangen for det valgte dokument.  
    * Arbejdsgang-id'et er identifikationskoden for den arbejdsgang, der behandler eller har behandlet dokumentet.  
    * Dokumentet er identifikationskoden for dokumentet.  
    * Dokumenttypen er typen af dokument, der er sendt til behandling.  
    * Arbejdsgangen er navnet på den arbejdsgang, der behandler eller har behandlet dokumentet.  
    * Versionsnummeret er versionsnummeret på den arbejdsgang, der behandler eller har behandlet dokumentet.  
    * Oprettelsesdatoen og klokkeslættet er datoen og klokkeslættet, hvor dokumentet blev sendt.  
    * Den medgåede tid er den tid, der er gået, siden dokumentet blev sendt.  
    * Knappen Genoptag giver dig mulighed at genoptage arbejdsgangsprocessen for det valgte dokument.  
    * Knappen Tilbagekald gør det muligt at tilbagekalde det valgte dokument, så det ikke bliver behandlet.   
2. Klik op linket i den valgte række på listen.
    * Sørg for, at afsnittet Arbejdselementer er udvidet.    I dette afsnit kan du få vist de arbejdselementer, der er knyttet til det valgte dokument. For eksempel skal en opgave måske fuldføres, eller dokumentet skal muligvis godkendes.  
    * Knappen Tildel igen åbner en dialogboks, hvor du igen kan tildele et arbejdselement til en anden bruger.  
    * Sørg for, at sektionen Sporingsdetaljer er udvidet.    I denne sektion kan du få vist arbejdsgangshistorikken for det valgte dokument.  


