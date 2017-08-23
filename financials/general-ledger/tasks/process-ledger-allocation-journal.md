--- 
title: Behandle finansfordelingskladde
description: "Brug siden Udfør fordelingsanmodning til at oprette en fordelingskladde, der kan gennemses og godkendes før postering i Finans, eller bogføres direkte i Finans."
author: aprilolson
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 1189ffeae052c72542b3b403a6b7a6e415b005c4
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="process-ledger-allocation-journal"></a>Behandle finansfordelingskladde

[!include[task guide banner](../../includes/task-guide-banner.md)]

Brug siden Udfør fordelingsanmodning til at oprette en fordelingskladde, der kan gennemses og godkendes før postering i Finans, eller bogføres direkte i Finans. Før du kan oprette en fordelingskladde, skal der være mindst én aktiv finansfordelingsregel. Denne opgave bruger demofirmaet USMF.

1. Gå til Finans > Fordelinger > Udfør fordelingsanmodning.
2. Klik på rullelisten i feltet Regel for at åbne opslaget.
3. Find og vælg den ønskede post på listen.
4. Klik op linket i den valgte række på listen.
5. Angiv en dato i feltet Pr. dato.
    * Fra-datoen er meget vigtig, hvis Finans er datakilden for reglen. Denne dato bestemmer, hvilke finanssaldi der skal medtages til fordeling.     Vælg Stop i Nul-kildefeltet. Derved standses fordelingsprocessen, og der vises en meddelelse, der angiver, at der er valgt et nul-kildebeløb.  
6. Vælg "Kun forslag" i feltet Forslagsmuligheder.
    * Vælg Kun forslag for at gennemgå og eventuelt godkende resultatet i Fordelingskladder før bogføring af fordelingen til Finans.  
7. Angiv en dato i feltet Finansposteringsdato.
8. Klik på OK.
9. Gå til Finans > Fordelinger > Fordelingskladder.
10. Klik på Linjer.
11. Klik på Bogfør.
12. Klik på Bogfør.


