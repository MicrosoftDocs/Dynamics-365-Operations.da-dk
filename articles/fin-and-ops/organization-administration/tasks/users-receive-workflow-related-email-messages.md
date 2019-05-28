---
title: Aktivér brugerne til at modtage e-mails, der er relateret til arbejdsgangen
description: Du kan konfigurere systemet til at sende e-mails til brugerne, når der opstår hændelser med relation til arbejdsgangen.
author: jasongre
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysUserSetup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6800d02878123388611d35760123d0215e9d539f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560492"
---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a>Aktivér brugerne til at modtage e-mails, der er relateret til arbejdsgangen

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

