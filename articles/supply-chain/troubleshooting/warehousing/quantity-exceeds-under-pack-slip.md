---
title: Antallet overskrider procenten for underlevering under oprettelse af en følgeseddel
description: Når du opretter en følgeseddel, indeholder den udgående last et antal, der overstiger procenten for underlevering.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSSalesPackingSlipPost,WHSLoadPlanningListPage_WHSSalesPackingSlipPost,WHSLoadPlanningWorkbench_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: ecdd377d12faf40f64736e93671dcf42ff132403
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249074"
---
# <a name="quantity-exceeds-under-delivery-percentage-during-packing-slip-generation"></a>Antallet overskrider procenten for underlevering under oprettelse af en følgeseddel

Fejlkode: SYS24921

## <a name="symptoms"></a>Symptomer

Når du opretter en følgeseddel, indeholder den udgående last et antal, der overstiger procenten for underlevering.

Når du forsøger at oprette en følgeseddel, vises følgende fejlmeddelelse:

> Linjen underleveres med %1 procent, men den tilladte underlevering er kun %2 procent.

Du kan derfor ikke oprette følgesedlen for lasten.

## <a name="cause"></a>Årsag

Det plukkede antal for lasten eller forsendelsen er mindre end det bestilte antal og ligger ikke inden for intervallet for procenten for underlevering.

## <a name="resolution"></a>Løsning

Lasten eller forsendelsen er i øjeblikket i en tilstand, hvor der ikke kan oprettes en følgeseddel. Du kan håndtere dette problem ved at udføre en eller flere af følgende opgaver:

- Juster procenten for underlevering.
- Tilbagefør og foretag reguleringer.

### <a name="adjust-the-under-delivery-percentage"></a>Justere procenten for underlevering

Du kan bruge følgende procedure til at justere procenten for underlevering.

1. Gå til **Debitor \> Ordrer \> Alle ordrer**.
1. Vælg den salgsordre, som du ikke kan bogføre en følgeseddel for lasten for.
1. Vælg salgsordrelinjen for den vare, der overstiger procenten for underlevering, i oversigtspanelet  **Salgsordrelinjer**.
1. Vælg **Levering** under fanen  **Linjedetaljer**.
1. Angiv feltet **Underlevering** til en større procentdel, der tager højde for det antal, der er plukket i forhold til lastantallet, så du kan fortsætte med at oprette følgesedlen.

### <a name="reverse-and-make-adjustments"></a>Tilbageføre og foretage reguleringer

Tilbagefør alt det, der er bogført for lasten (f.eks. følgesedlen, forsendelsesbekræftelsen og arbejdet), foretag salgsordrereguleringer, frigiv ordren til lagerstedet igen, og fuldfør forsendelsesproceduren.

Brug følgende procedure til at annullere en følgeseddel.

1. Gå til **Lokationsstyring \> Laster \> Alle laster**.
1. Vælg  **Annuller følgesedler** i gruppen  **Tilbagefør** under fanen  **Levér og modtag** i handlingsruden.

Brug følgende procedure til at tilbageføre en forsendelsesbekræftelse.

1. Gå til **Lokationsstyring \> Laster \> Alle laster**.
1. Vælg  **Tilbagefør forsendelsesbekræftelse** i gruppen  **Tilbagefør** under fanen  **Levér og modtag** i handlingsruden.

Benyt følgende fremgangsmåde for at tilbageføre arbejde.

1. Gå til **Lokationsstyring \> Laster \> Alle laster**.
1. Gå til handlingsruden, og vælg  **Tilbagefør arbejde** i gruppen  **Arbejde** under fanen  **Laster**.
