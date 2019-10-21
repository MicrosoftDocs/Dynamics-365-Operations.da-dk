---
title: Behandle finansfordelingskladde
description: I dette emne beskrives, hvordan du behandler en fordelingsanmodning i Dynamics 365 Finance.
author: aprilolson
manager: AnnBe
ms.date: 07/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 882362a03e4fc4e249b092caea374640813eef88
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186066"
---
# <a name="process-ledger-allocation-journal"></a>Behandle finansfordelingskladde

[!include [task guide banner](../../includes/task-guide-banner.md)]

I dette emne beskrives, hvordan du behandler en fordelingsanmodning. Brug siden Udfør fordelingsanmodning til at oprette en fordelingskladde, der kan gennemses og godkendes før postering i Finans, eller bogføres direkte i Finans. Før du kan oprette en fordelingskladde, skal der være mindst én aktiv finansfordelingsregel. Denne opgave bruger demofirmaet USMF.

1. Gå til **Moduler > Finans > Fordelinger > Udfør fordelingsanmodning** i navigationsruden.
2. I feltet **Regel** skal du vælge den ønskede post i rullemenuen.
3. Angiv en dato i feltet **Pr. dato**.

    - **Pr. dato** er meget vigtig, når Finans er datakilden for reglen. Denne dato bestemmer, hvilke finanssaldi der skal medtages til fordeling.  
    - Vælg **Stop** i **Nul-kilde**-feltet. Derved standses fordelingsprocessen, og der vises en meddelelse, der angiver, at der er valgt et nul-kildebeløb.  

4. Vælg **Kun forslag** i feltet **Forslagsmuligheder**. Vælg **Kun forslag** for at gennemgå og eventuelt godkende resultatet i Fordelingskladder før bogføring af fordelingen til Finans.  
5. Angiv en dato i feltet Finansposteringsdato.
6. Vælg **OK**.
7. Gå til **Moduler > Finans > Fordelinger > Fordelingskladder** i navigationsruden.
8. Vælg **Linjer**.
9. Vælg **Bogfør**.
10. Vælg **Bogfør**.

