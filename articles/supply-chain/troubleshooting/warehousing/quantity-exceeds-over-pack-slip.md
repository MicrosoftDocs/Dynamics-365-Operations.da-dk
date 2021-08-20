---
title: Antallet overskrider procenten for overlevering under oprettelse af en følgeseddel
description: Når du opretter en følgeseddel, indeholder den udgående last et antal, der overstiger procenten for overlevering.
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
ms.openlocfilehash: 00e3da7767b80e16f9351f59b109765bffc0128fe149cefafc1edda3a6cbcb96
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781339"
---
# <a name="quantity-exceeds-over-delivery-percentage-during-packing-slip-generation"></a>Antallet overskrider procenten for overlevering under oprettelse af en følgeseddel

Fejlkode: SYS24920

## <a name="symptoms"></a>Symptomer

Når du opretter en følgeseddel, indeholder den udgående last et antal, der overstiger procenten for overlevering.

Når du forsøger at oprette en følgeseddel, vises følgende fejlmeddelelse:

> Linjen overleveres med %1 procent, men den tilladte overlevering er kun %2 procent.

Du kan derfor ikke oprette følgesedlen for lasten.

## <a name="cause"></a>Årsag

Det plukkede antal for lasten eller forsendelsen er mere end det bestilte antal og ligger ikke inden for intervallet for procenten for overlevering.

## <a name="resolution"></a>Løsning

Lasten eller forsendelsen er i øjeblikket i en tilstand, hvor der ikke kan oprettes en følgeseddel. Du kan håndtere dette problem ved at udføre en eller flere af følgende opgaver:

- Justere antallet for lastlinjen.
- Justere procenten for overlevering.
- Tilbagefør og foretag reguleringer.

### <a name="adjust-the-load-line-quantity"></a>Justere antallet for lastlinjen

Du kan bruge følgende procedure til at justere antallet for lastlinjen.

1. Gå til **Lokationsstyring \> Laster \> Alle laster**.
1. Vælg den last, som følgesedlen ikke kan genereres for.
1. Vælg  **Tilbagefør forsendelsesbekræftelse** i gruppen  **Tilbagefør** under fanen  **Levér og modtag** i handlingsruden.
1. Vælg lastlinjen for den vare, der overstiger procenten for overlevering, under fanen  **Lastlinjer**.
1. Vælg **Reducer plukket antal** for at justere det plukkede antal.
1. Vælg **Ordre** under fanen  **Linjedetaljer**.
1. Angiv feltet **Antal** til det plukkede antal (dvs. værdien for feltet **Antal oprettet under arbejde**), så du kan fortsætte med at generere følgesedlen.

### <a name="adjust-the-over-delivery-percentage"></a>Justere procenten for overlevering

Du kan bruge følgende procedure til at justere procenten for overlevering.

1. Gå til **Debitor \> Ordrer \> Alle ordrer**.
1. Vælg den salgsordre, som du ikke kan bogføre en følgeseddel for lasten for.
1. Vælg salgsordrelinjen for den vare, der overstiger procenten for overlevering, i oversigtspanelet  **Salgsordrelinjer**.
1. Vælg **Levering** under fanen  **Linjedetaljer**.
1. Angiv feltet **Overlevering** til en større procentdel, der tager højde for det antal, der er plukket i forhold til lastantallet, så du kan fortsætte med at oprette følgesedlen.

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
