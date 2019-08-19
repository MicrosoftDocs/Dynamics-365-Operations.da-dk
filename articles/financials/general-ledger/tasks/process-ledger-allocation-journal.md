---
title: Behandle finansfordelingskladde
description: Brug siden Udfør fordelingsanmodning til at oprette en fordelingskladde, der kan gennemses og godkendes før postering i Finans, eller bogføres direkte i Finans.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: 087bd4f203e8762447e823b19076b79296a390d6
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846361"
---
# <a name="process-ledger-allocation-journal"></a>Behandle finansfordelingskladde

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

