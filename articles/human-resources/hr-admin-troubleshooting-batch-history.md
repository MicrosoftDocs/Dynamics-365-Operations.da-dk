---
title: Optimere ydeevnen med automatiske oprydningsopgaver
description: Denne artikel forklarer, hvordan du kan forbedre ydeevnen i Microsoft Dynamics 365 Human Resources ved at rydde historikken for batchjob.
author: twheeloc
ms.date: 08/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 10d535e54f71e7bb90c7385e09926270a446df7d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902192"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a>Optimere ydeevnen med automatiske oprydningsopgaver


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Udsted**

Microsoft Dynamics 365 Human Resources kan give problemer med ydeevnen, hvis historikken for batchjob bliver for stor.

**Årsag**

Batchjob, der kører ofte, kan føre til en ikke-bæredygtig forøgelse af historikken for batchjob. Dette kan forårsage problemer med ydeevnen. 

**Løsning**

Planlæg en automatisk opgave for at rydde op i historikken for batchjob. Vi anbefaler, at du konfigurerer opgaven til at køre ugentligt, men du kan blive nødt til at køre oprydningen mere eller mindre hyppigt, afhængigt af miljøet. Følgende procedure indeholder vores anbefalede indstillinger, men du kan ændre dem efter behov.

1. I Human Resources skal du vælge **Systemadministration**.

2. På linjen **Søg** skal du indtaste **Oprydning i batchjobhistorik**.

   ![Søg efter oprydning af historik for batchjob.](media/talent-batch-history-cleanup-search-bar.png)

3. I **Historikgrænse (dage)** skal du skrive **30**.

   ![Angiv historikgrænse til 30.](media/talent-batch-history-cleanup-history-limit.png)

4. Vælg **Kør i baggrunden**, og vælg derefter **Gentagelse**.

   ![Angiv gentagelse.](media/talent-batch-history-cleanup-recurrence.png)

5. Under **Definer gentagelse** skal du angive **Startdato** og **Starttidspunkt**, der skal være uden for arbejdstiden eller i weekenden, og vælg derefter **Ingen slutdato**. 

   ![Definer startdato og -tidspunkt for gentagelse.](media/talent-batch-history-cleanup-define-recurrence.png)

6. Vælg **Dage** under **Gentagelsesmønster**, og angiv **Gentag efter angivet interval** til **7**.

   ![Indstil oprydning til ugentlig gentagelse.](media/talent-batch-history-cleanup-recurrence-pattern.png)

7. Vælg **OK**.

8. Rediger andre parametre under **Kør i baggrunden** efter behov, og vælg derefter **OK**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
