---
title: Optimere ydeevnen med automatiske oprydningsopgaver
description: Dette emne forklarer, hvordan du kan løse problemer med ydeevnen af Microsoft Dynamics 365 Talent ved at rydde historikken for batchjob.
author: andreabichsel
manager: AnnBe
ms.date: 09/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-09-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: a053c9094151f4e12e4aadc533dd272258779540
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832576"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a>Optimere ydeevnen med automatiske oprydningsopgaver

[!include [banner](includes/banner.md)]

**Udsted**

Microsoft Dynamics 365 Talent kan give problemer med ydeevnen, hvis historikken for batchjob bliver for stor.

**Årsag**

Batchjob, der kører ofte, kan føre til en ikke-bæredygtig forøgelse af historikken for batchjob. Dette kan forårsage problemer med ydeevnen. 

**Løsning**

Planlæg en automatisk opgave for at rydde op i historikken for batchjob. Vi anbefaler, at du konfigurerer opgaven til at køre ugentligt, men du kan blive nødt til at køre oprydningen mere eller mindre hyppigt, afhængigt af miljøet. Følgende procedure indeholder vores anbefalede indstillinger, men du kan ændre dem efter behov.

1. I Talent skal du vælge **Systemadministration**.

2. På linjen **Søg** skal du indtaste **Oprydning i batchjobhistorik**.

   ![Søg efter oprydning af historik for batchjob](media/talent-batch-history-cleanup-search-bar.png)

3. I **Historikgrænse (dage)** skal du skrive **30**.

   ![Angiv historikgrænse til 30](media/talent-batch-history-cleanup-history-limit.png)

4. Vælg **Kør i baggrunden**, og vælg derefter **Gentagelse**.

   ![Angiv gentagelse](media/talent-batch-history-cleanup-recurrence.png)

5. Under **Definer gentagelse** skal du angive **Startdato** og **Starttidspunkt**, der skal være uden for arbejdstiden eller i weekenden, og vælg derefter **Ingen slutdato**. 

   ![Definer startdato og -tidspunkt for gentagelse](media/talent-batch-history-cleanup-define-recurrence.png)

6. Vælg **Dage** under **Gentagelsesmønster**, og angiv **Gentag efter angivet interval** til **7**.

   ![Indstil oprydning til ugentlig gentagelse](media/talent-batch-history-cleanup-recurrence-pattern.png)

7. Vælg **OK**.

8. Rediger andre parametre under **Kør i baggrunden** efter behov, og vælg derefter **OK**.

