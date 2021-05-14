---
title: Arbejde forbliver blokeret
description: Arbejde forbliver blokeret
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTableListPage_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f85364d1ecfadc36b26c3395ab4402d3cb3b1603
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924124"
---
# <a name="work-remains-blocked"></a>Arbejde forbliver blokeret

Fejlkode: WHSWorkBlockingExecutingWaveReason_ErrorMessage

## <a name="symptoms"></a>Symptomer

Systemet viser følgende fejlmeddelelse:

> Arbejde %1 forbliver spærret, fordi den relaterede bølge %2 har status %3.

## <a name="cause"></a>Årsag

Arbejdet behandles i øjeblikket på en bølge og kan ikke låses op, som angivet med en af følgende forhold:

- Under fanen **Blokeringsårsager** er feltet **Årsag til blokering af arbejde** angivet for en eller flere linjer til *Behandler bølge*.
- Når du vælger **Bølge** i gruppen **Relaterede oplysninger** under fanen **Relaterede oplysninger** i handlingsruden, angives feltet **Bølgestatus** til *Behandler*.

## <a name="resolution"></a>Løsning

Vælg **Bølge** i gruppen **Relaterede oplysninger** under fanen **Relaterede oplysninger** i handlingsruden. Vælg **Ryd op i bølgedata** i gruppen **Bølge** under fanen **Bølge** på siden **Bølger** i handlingsruden.

## <a name="workaround"></a>Løsning

Hvis de foregående trin ikke løser problemet, kan du annullere arbejdet med følgende fremgangsmåde.

1. Gå til **Lagerstedsstyring \> Periodiske opgaver \> Oprydning \> Annuller arbejde**.
1. I feltet **Arbejds-id** skal du angive id'et for det arbejde, du vil annullere, og som i øjeblikket har en værdien for **Arbejdsstatus** *Åben*, *I gang*, *Annulleret*, *Kombineret* eller *Lukket*.
1. Vælg **OK**.
1. Vælg **Ja** for at bekræfte, at du vil annullere arbejdet.

Du kan finde flere oplysninger i [Annullere lagerstedsarbejde for undtagelseshåndtering](../../warehousing/cancel-warehouse-work.md).
