---
title: Behandle finansfordelingskladde
description: I dette emne beskrives, hvordan du behandler en fordelingsanmodning i Dynamics 365 Finance.
author: aprilolson
ms.date: 07/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7d37b1a9869cc130786d0e8fde68184e04c881bad1f64c86943174213025db82
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765662"
---
# <a name="process-ledger-allocation-journal"></a>Behandle finansfordelingskladde

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]