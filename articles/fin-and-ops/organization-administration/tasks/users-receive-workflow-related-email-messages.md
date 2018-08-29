--- 
title: Konfigurere systemet til at sende arbejdsgangsrelateret mail til brugere
description: "Du kan konfigurere systemet til at sende e-mails til brugerne, når der opstår hændelser med relation til arbejdsgangen."
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
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 04d90c9ded1ba7fb1ceac4ff1d54f54f6c43f9e9
ms.contentlocale: da-dk
ms.lasthandoff: 08/08/2018

---
# <a name="configure-the-system-to-send-workflow-related-email-to-users"></a>Konfigurere systemet til at sende arbejdsgangsrelateret mail til brugere

[!include [task guide banner](../../includes/task-guide-banner.md)]

Du kan konfigurere systemet til at sende e-mails til brugerne, når der opstår hændelser med relation til arbejdsgangen. For eksempel kan e-mails sendes til brugerne, når dokumenter tildeles til dem til godkendelse. Det demodatafirma, der bruges til at oprette denne procedure, er USMF.

1. Gå til Systemadministration > Brugere > Brugere.
2. Find og vælg den ønskede post på listen.
3. Klik på Brugerindstillinger.
4. Klik på fanen Arbejdsgang.
    * Sørg for, at sektionen Beskeder er udvidet.     I sektionen Beskeder kan du angive, hvordan du ønsker, brugeren skal have besked om hændelser, der er relateret til arbejdsgangen.  
5. Vælg en indstilling i feltet Beskedtype for arbejdsgang for linjeelement.
    * Grupperet – beskeder om linjeelementer grupperes i en enkelt e-mail.    Individuelt – der sendes en e-mail for hvert linjeelement.  
    * Hvis du ønsker, at brugeren skal modtage beskeder i klienten, skal du markere afkrydsningsfeltet Send beskeder i e-mail.  
6. Klik på Gem.
7. Luk siden.


