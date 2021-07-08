---
title: Fysisk restantal i enheden må ikke være nul
description: Når du opretter en følgeseddel, har de data, der leveres til den, et lagerantal, der ikke er nul, men et salgsantal på nul.
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
ms.openlocfilehash: bfd381160bcfd1e6e5489e16cc22178b8a5142ee
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/14/2021
ms.locfileid: "6248772"
---
# <a name="physical-remaining-quantity-in-the-unit-must-not-be-zero"></a>Fysisk restantal i enheden må ikke være nul

Fejlkode: SYS19591

## <a name="symptoms"></a>Symptomer

Når du opretter en følgeseddel, har de data, der leveres til den, et lagerantal, der ikke er nul, men et salgsantal på nul.

Når du forsøger at oprette følgesedlen, vises følgende fejlmeddelelse:

> Fysisk rest i enheden %1 skal være forskellig fra nul.

Du kan derfor ikke oprette følgesedlen for lasten.

## <a name="cause"></a>Årsag

Systemet evaluerer det fysiske restantal i lagerenheden og det fysisk restantal i forsendelsesenheden. Hvis det fysiske restantal i forsendelsesenheden er 0 (nul), men det fysiske restantal i lagerenheden ikke er 0, kan du ikke oprette følgesedlen. Dette problem kan for eksempel forekomme, hvis salgsenheden og lagerenheden for varen er forskellig, og omregningen mellem enheder ikke er nøjagtig.

## <a name="resolution"></a>Løsning

Lasten eller forsendelsen er i øjeblikket i en tilstand, hvor der ikke kan oprettes en følgeseddel. Du kan håndtere dette problem ved at udføre en eller flere af følgende opgaver:

- Gennemse dine lastlinjer, og kontrollér, at alt det relaterede arbejde er fuldført på den endelige forsendelseslokation, og at mængderne stemmer overens.
- Gennemse lastlinjerne, og foretag justeringer for at sikre, at antallet kan konverteres rent uden afrundingsproblemer.
- Gennemse lastlinjerne, og foretag justeringer for at sikre, at enheden og antallet er tilpasset enhedens decimalpræcision.
- Kontrollér, at måleenheden for lageret er mindre end måleenheden for salg.

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Gennemse dine lastlinjer, og kontrollér, at alt det relaterede arbejde er fuldført på den endelige forsendelseslokation, og at mængderne stemmer overens

Brug følgende procedure til at gennemse dine lastlinjer og kontrollere, at alt det relaterede arbejde er fuldført på den endelige forsendelseslokation, og at mængderne stemmer overens.

1. Gå til **Lokationsstyring \> Laster \> Alle laster**.
1. Vælg den last, som forsendelsen ikke kan bekræftes for.
1. Vælg linjen for lasten i oversigtspanelet **Lastlinjer**.
1. Notér værdien for feltet **Antal oprettet under arbejde**.
1. under fanen **Laster** i gruppen **Relaterede oplysninger** i handlingsruden skal du vælge **Arbejde**.
1. Kontrollér, at arbejdet er udført på den endelige forsendelseslokation, og at det plukkede arbejdsantal svarer til det oprettede arbejdsantal på lastlinjen.
1. Gentag denne procedure for alle lastlinjer for at sikre, at alle kriterier er opfyldt.

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-rounding-issues"></a>Gennemse lastlinjerne, og foretag justeringer for at sikre, at antallet kan konverteres rent uden afrundingsproblemer

Brug følgende procedure til at gennemse lastlinjerne og foretage justeringer for at sikre, at antallet kan konverteres rent uden afrundingsproblemer.

1. Gå til **Lokationsstyring \> Laster \> Alle laster**.
1. Vælg den last, som følgesedlen ikke kan genereres for.
1. Vælg  **Tilbagefør forsendelsesbekræftelse** i gruppen  **Tilbagefør** under fanen  **Levér og modtag** i handlingsruden.
1. Vælg lastlinjen for den vare, der overstiger overleveringen, under fanen  **Lastlinjer**.
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

### <a name="make-sure-that-the-inventory-unit-of-measure-is-smaller-than-the-sales-unit-of-measure"></a>Kontrollér, at måleenheden for lageret er mindre end måleenheden for salg

Kontrollér, at måleenheden for lageret er mindre end måleenheden for salg. Overvej at omkonfigurere måleenheden for varen efter behov.
