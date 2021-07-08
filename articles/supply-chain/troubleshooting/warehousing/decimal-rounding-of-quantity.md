---
title: Decimalafrunding af det fysiske opdateringsantal er ikke korrekt
description: Når du genererer en følgeseddel, indeholder den udgående last et antal, der ikke svarer til den decimalpræcision, der er defineret i enheden.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningListPage_WHSSalesPackingSlipPost, WHSLoadTable_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1e63440834f516879aa8ad711bd789e62b0ee993
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/14/2021
ms.locfileid: "6248773"
---
# <a name="decimal-rounding-of-the-physical-updating-quantity-is-incorrect"></a>Decimalafrunding af det fysiske opdateringsantal er ikke korrekt

Fejlkode: SYS19589

## <a name="symptoms"></a>Symptomer

Når du genererer en følgeseddel, indeholder den udgående last et antal, der ikke svarer til den decimalpræcision, der er defineret i enheden.

Når du forsøger at oprette en følgeseddel, vises følgende fejlmeddelelse:

> Fysisk opdateringsantal i enheden %1 er ikke korrekt decimalafrundet.

Du kan derfor ikke oprette følgesedlen for lasten.

## <a name="cause"></a>Årsag

Systemet evaluerer, om decimalafrunding af afsendelsesantallet svarer til den decimalpræcision, der er defineret for forsendelsesenheden. Når systemet afrunder afsendelsesantallet til det angivne antal decimaler, kan du ikke generere følgesedlen, hvis det afrundede afsendelsesantal ikke svarer til det faktiske afsendelsesantal. Dette problem kan f.eks. forekomme, hvis salgsantallet er 1,75 kg, men decimalpræcisionen er angivet til *1*.

## <a name="resolution"></a>Løsning

Lasten eller forsendelsen er i øjeblikket i en tilstand, hvor der ikke kan oprettes en følgeseddel. Du kan håndtere dette problem ved at udføre en eller flere af følgende opgaver:

- Gennemse lastlinjerne, og foretag justeringer for at sikre, at antallet kan konverteres rent uden decimaltal og andre afrundingsproblemer.
- Gennemse lastlinjerne, og foretag justeringer for at sikre, at enheden og antallet er tilpasset enhedens decimalpræcision.

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-decimal-numbers-and-any-other-rounding-issues"></a>Gennemse lastlinjerne, og foretag justeringer for at sikre, at antallet kan konverteres rent uden decimaltal og andre afrundingsproblemer

Brug følgende procedure til at gennemse lastlinjerne og foretage justeringer for at sikre, at antallet kan konverteres rent uden decimaltal og andre afrundingsproblemer.

1. Gå til **Lokationsstyring \> Laster \> Alle laster**.
1. Vælg den last, som følgesedlen ikke kan genereres for.
1. Vælg  **Tilbagefør forsendelsesbekræftelse** i gruppen  **Tilbagefør** under fanen  **Levér og modtag** i handlingsruden.
1. Vælg lastlinjen for den vare, der forårsager et problem, under fanen  **Lastlinjer**.
1. Vælg **Reducer plukket antal** for at justere det plukkede antal.
1. Vælg **Ordre** under fanen  **Linjedetaljer**.
1. Angiv feltet **Antal** til det plukkede antal (dvs. værdien for feltet **Antal oprettet under arbejde**), så du kan fortsætte med at generere følgesedlen.

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-unit-and-quantity-are-aligned-with-the-decimal-precision-of-the-unit"></a>Gennemse lastlinjerne, og foretag justeringer for at sikre, at enheden og antallet er tilpasset enhedens decimalpræcision

Brug følgende procedure til at gennemse lastlinjerne og foretage justeringer for at sikre, at enheden og antallet er tilpasset enhedens decimalpræcision.

1. Gå til **Lokationsstyring \> Laster \> Alle laster**.
1. Vælg den last, som følgesedlen ikke kan genereres for.
1. Vælg lastlinjen for den vare, der forårsager et problem, i oversigtspanelet **Lastlinjer**. Notér værdien for felterne **Antal** og **Enhed**.
1. Gå til **Virksomhedsadministration \> Enheder \> Enheder**.
1. Vælg den enhed, som følgesedlen ikke kan genereres for.
1. Juster værdien i feltet **Decimalpræcision** efter behov.
