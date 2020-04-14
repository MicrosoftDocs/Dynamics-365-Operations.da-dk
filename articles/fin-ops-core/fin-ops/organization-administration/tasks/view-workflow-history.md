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
ms.openlocfilehash: dd5b8d9f3fd2edab50b52a8345f254ebc6b31d0a
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140392"
---
# <a name="view-workflow-history"></a>Vise arbejdsgangshistorik

[!include [banner](../../includes/banner.md)]

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

