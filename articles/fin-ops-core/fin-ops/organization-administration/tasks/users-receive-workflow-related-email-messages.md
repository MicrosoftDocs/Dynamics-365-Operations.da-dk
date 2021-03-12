---
title: Aktivér brugerne til at modtage e-mails, der er relateret til arbejdsgangen
description: Du kan konfigurere systemet til at sende e-mails til brugerne, når der opstår hændelser med relation til arbejdsgangen.
author: jasongre
manager: AnnBe
ms.date: 06/01/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysUserSetup
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 221e38cbe31e2ad24a56cb2e71206a1ebcdd619e
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798998"
---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a>Aktivér brugerne til at modtage e-mails, der er relateret til arbejdsgangen

[!include [banner](../../includes/banner.md)]

Du kan konfigurere systemet til at sende e-mails til brugerne, når der opstår hændelser med relation til arbejdsgangen. For eksempel kan e-mails sendes til brugerne, når dokumenter tildeles til dem til godkendelse. Det demodatafirma, der bruges til at oprette denne procedure, er USMF.

1. Gå til **Navigationsrude > Moduler > Systemadministration > Brugere > Brugere**.
2. Find og vælg den ønskede post på listen.
3. Klik på **Brugerindstillinger** i **Handlingsrude**.
4. Klik på fanen **Arbejdsgang**. Kontrollér, at sektionen **Beskeder** er udvidet. I sektionen **Beskeder** kan du angive, hvordan du ønsker, brugeren skal have besked om hændelser, der er relateret til arbejdsgangen.  
5. Vælg en indstilling i feltet **Beskedtype for arbejdsgang for linjeelement**.
    - Grupperet – beskeder om linjeelementer grupperes i en enkelt e-mail.
    - Individuelt – der sendes en e-mail for hvert linjeelement.  
    - Hvis du ønsker, at brugeren skal modtage beskeder i klienten, skal du markere afkrydsningsfeltet **Send beskeder i e-mail**.  
6. Klik på **Gem**.
7. Luk siden.

> [!NOTE]
> E-mailskabelonerne til arbejdsgangen leveres fra enten systemmailskabeloner eller virksomhedsmailskabeloner, afhængigt af om arbejdsgangen er på systemniveau (ikke firmaspecifik) eller på virksomhedsniveau (firmaspecifik).
