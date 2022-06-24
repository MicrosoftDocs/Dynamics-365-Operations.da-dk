---
title: Vise arbejdsproces historik
description: Denne artikel beskriver fremgangsmåden for at få vist statussen for et dokument, der er sendt til arbejdsgangssystemet til behandling og godkendelse.
author: jasongre
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowStatus
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8a5810eaed5d2ff6cb5c98e1b21c098c70f24485
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868573"
---
# <a name="view-workflow-history"></a>Vise arbejdsproces historik

[!include [banner](../../includes/banner.md)]


[!INCLUDE [PEAP](../../../../includes/peap-1.md)]

Denne artikel beskriver fremgangsmåden for at få vist statussen for et dokument, der er sendt til arbejdsgangssystemet til behandling og godkendelse. Det demodatafirma, der bruges til at oprette denne procedure, er USMF.

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



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]