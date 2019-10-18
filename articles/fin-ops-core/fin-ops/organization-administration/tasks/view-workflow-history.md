---
title: Vise arbejdsgangshistorik
description: Dette emne beskriver fremgangsmåden for at få vist statussen for et dokument, der er sendt til arbejdsgangssystemet til behandling og godkendelse.
author: jasongre
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowStatus
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 16c6594161f1fecd36183a6b8f2c798f52d70a9c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189792"
---
# <a name="view-workflow-history"></a>Vise arbejdsgangshistorik

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dette emne beskriver fremgangsmåden for at få vist statussen for et dokument, der er sendt til arbejdsgangssystemet til behandling og godkendelse. Det demodatafirma, der bruges til at oprette denne procedure, er USMF.

1. Gå til **Navigationsrude > Moduler > Almindelig > Forespørgsler > Arbejdsgang > Arbejdsgangshistorik**.
    - Brug denne formular til at få vist status for et dokument, der er sendt til arbejdsgangssystemet til behandling og godkendelse.  
    - **Forekomst-ID'et** er identifikationskoden for den arbejdsgangsforekomst, der behandler eller har behandlet dokumentet.  
    - **Status** for arbejdsgangen for det valgte dokument.  
    - **Arbejdsgang-ID'et** er identifikationskoden for den arbejdsgang, der behandler eller har behandlet dokumentet.  
    - **Dokumentet** er identifikationskoden for dokumentet.  
    - **Dokumenttypen** er typen af dokument, der er sendt til behandling.  
    - **Arbejdsgangen** er navnet på den arbejdsgang, der behandler eller har behandlet dokumentet.  
    - **Version** er versionsnummeret på den arbejdsgang, der behandler eller har behandlet dokumentet.  
    - **Oprettelsesdatoen og klokkeslættet** er datoen og klokkeslættet, hvor dokumentet blev sendt.  
    - Den **Medgået tid** er den tid, der er gået, siden dokumentet blev sendt.  
    - Knappen **Genoptag** giver dig mulighed at genoptage arbejdsgangsprocessen for det valgte dokument.  
    - Knappen **Tilbagekald** gør det muligt at tilbagekalde det valgte dokument, så det ikke bliver behandlet.   
2. Vælg linket i den ønskede række på listen.
    - Sørg for, at afsnittet **Arbejdselementer** er udvidet. I dette afsnit kan du få vist de arbejdselementer, der er knyttet til det valgte dokument. For eksempel skal en opgave måske fuldføres, eller dokumentet skal muligvis godkendes.  
    - Knappen **Tildel igen** åbner en dialogboks, hvor du igen kan tildele et arbejdselement til en anden bruger.  
    - Sørg for, at sektionen **Sporingsdetaljer** er udvidet. I denne sektion kan du få vist arbejdsgangshistorikken for det valgte dokument.  

