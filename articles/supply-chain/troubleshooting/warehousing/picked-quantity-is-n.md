---
title: Plukket antal er ikke tilstrækkeligt under generering af følgeseddel
description: Når du genererer en følgeseddel, indeholder den udgående last et plukket antal, der ikke svarer til det oprettede arbejdsantal på lastlinjen.
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
ms.openlocfilehash: 6febc340f140d0b3a3f08ea32a59d9eb4e6e5204
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920442"
---
# <a name="picked-quantity-isnt-sufficient-during-packing-slip-generation"></a>Plukket antal er ikke tilstrækkeligt under generering af følgeseddel

Fejlkode: SYS54073

## <a name="symptoms"></a>Symptomer

Når du genererer en følgeseddel, indeholder den udgående last et plukket antal, der ikke svarer til det oprettede arbejdsantal på lastlinjen.

Når du forsøger at oprette en følgeseddel, vises følgende fejlmeddelelse:

> Da der er plukket %1, kan der ikke kun opdateres %2, når resten efterfølgende skal være %3.

Du kan derfor ikke oprette følgesedlen for lasten.

## <a name="cause"></a>Årsag

Følgesedlen kan ikke oprettes i dens aktuelle tilstand, da en af følgende betingelser kan være til stede:

- Det relaterede arbejde er endnu ikke plukket og flyttet til det endelige afsendelsessted.
- Det plukkede arbejdsantal svarer ikke til det oprettede arbejdsantal på linjen for lasten.
- Antallet på lastlinjen, det oprettede arbejdsantal og det plukkede arbejdsantal stemmer ikke overens.

## <a name="resolution"></a>Løsning

Lasten eller forsendelsen er i øjeblikket i en tilstand, hvor der ikke kan oprettes en følgeseddel. Du kan håndtere dette problem ved at udføre en eller flere af følgende opgaver:

- Gennemse dine lastlinjer, og kontrollér, at alt det relaterede arbejde er fuldført på den endelige forsendelseslokation, og at mængderne stemmer overens.
- Justere antallet for lastlinjen.
- Tilbageføre alle plukregistreringer og gentage pluk.

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Gennemse dine lastlinjer, og kontrollér, at alt det relaterede arbejde er fuldført på den endelige forsendelseslokation, og at mængderne stemmer overens

Brug følgende procedure til at gennemse dine lastlinjer og kontrollere, at alt det relaterede arbejde er fuldført på den endelige forsendelseslokation, og at mængderne stemmer overens.

1. Gå til **Lokationsstyring \> Laster \> Alle laster**.
1. Vælg den last, som følgesedlen ikke kan genereres for.
1. Vælg linjen for lasten i oversigtspanelet **Lastlinjer**.
1. Notér værdien for feltet **Antal oprettet under arbejde**.
1. under fanen **Laster** i gruppen **Relaterede oplysninger** i handlingsruden skal du vælge **Arbejde**.
1. Kontrollér, at arbejdet er udført på den endelige forsendelseslokation, og at det plukkede arbejdsantal svarer til det oprettede arbejdsantal på lastlinjen.
1. Gentag denne procedure for alle lastlinjer for at sikre, at alle kriterier er opfyldt.

### <a name="adjust-the-load-line-quantity"></a>Justere antallet for lastlinjen

Du kan bruge følgende procedure til at justere antallet for lastlinjen.

1. Gå til **Lokationsstyring \> Laster \> Alle laster**.
1. Vælg den last, som følgesedlen ikke kan genereres for.
1. Vælg **Tilbagefør forsendelsesbekræftelse** i gruppen **Tilbagefør** under fanen **Levér og modtag** i handlingsruden.
1. Vælg lastlinjen for den vare, der forårsager et problem, under fanen **Lastlinjer**.
1. Vælg **Reducer plukket antal** for at justere det plukkede antal.
1. Angiv feltet **Reducer lastlinje**, så det afspejler justeringer på lastlinjen.

### <a name="reverse-all-pick-registrations-and-redo-picking"></a>Tilbageføre alle plukregistreringer og gentage pluk

Problemet kan forekomme, fordi en anden har brugt plukregistrering til at lukke en lastlinje uden arbejde. I dette tilfælde skal manuel plukregistrering tilbageføres, og plukningen skal derefter udføres ved hjælp af mobilappen Warehouse Management.

Du kan bruge følgende procedure til at tilbageføre plukregistreringen.

1. Gå til **Debitor \> Ordrer \> Alle ordrer**.
1. Vælg den salgsordre, som du ikke kan bogføre en følgeseddel for lasten for.
1. Vælg den salgsordrelinje, som plukregistrering er udført for, under fanen **Salgsordrelinjer**.
1. Vælg **Opdater linje \> Pluk** for at fortryde pluk af varerne.
