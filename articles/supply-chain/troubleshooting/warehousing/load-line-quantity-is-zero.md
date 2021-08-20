---
title: Du kan ikke bekræfte en forsendelse, fordi lastlinjer har antallet nul
description: Du kan ikke bekræfte en forsendelse, fordi lastlinjer har antallet nul.
author: GalynaFedorova
ms.date: 07/30/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 5dc5f8962ba37d21d7ef505fea940dc8767a9d9295588cb0e12e9eebe379a35c
ms.sourcegitcommit: fa5ff2a0822aac16b518a2aea0d3389f79793390
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/07/2021
ms.locfileid: "7012151"
---
# <a name="you-cant-confirm-a-shipment-because-load-lines-have-zero-quantity"></a>Du kan ikke bekræfte en forsendelse, fordi lastlinjer har antallet nul

Fejlkode: WAX:LoadTableWarningAllLinesZero, WAX2543

## <a name="symptoms"></a>Symptomer

Når du forsøger at bekræfte en forsendelse, vises følgende fejlmeddelelse:

> Alle linjer i lasten %1 har antallet nul.  
> Forsendelsen af lasten %1 kunne ikke bekræftes.

Du kan derfor ikke bekræfte forsendelsen for lasten.

## <a name="cause"></a>Årsag

Systemet evaluerer, om lastlinjen kan få bekræftet forsendelse på basis af de oprettede arbejds-id'er, lastlinjeantal og underleveringsprocenten. Hvis systemet finder ud af, at der ikke er nogen arbejds-id'er, og hvis underleveringsprocenten er angivet til 100 procent, kan du ikke bekræfte forsendelsen.

Dette problem kan f.eks. forekomme, hvis arbejdet er blevet annulleret, og underleveringsprocenten på lastlinjen er 100 procent.

## <a name="resolution"></a>Løsning

Lasten eller forsendelsen er i øjeblikket i en tilstand, hvor forsendelsesbekræftelsen mislykkes. Du kan håndtere dette problem ved at udføre en eller flere af følgende opgaver:

- Gennemse dine lastlinjer for at sikre, at alt det relaterede arbejde er fuldført på den endelige forsendelseslokation, og at mængderne stemmer overens.
- Gennemgå lastlinjerne for at sikre, at underleveringsprocenten og -mængderne er tilpasset det plukkede arbejde.

### <a name="review-your-load-lines-to-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Gennemgå dine lastlinjer for at sikre, at alt det relaterede arbejde er fuldført på den endelige forsendelseslokation, og at mængderne stemmer overens

Brug følgende procedure til at gennemgå dine lastlinjer for at sikre, at alt det relaterede arbejde er fuldført på den endelige forsendelseslokation, og at mængderne stemmer overens.

1. Gå til **Lokationsstyring \> Laster \> Alle laster**.
1. Åbn den last, som forsendelsen ikke kan bekræftes for.
1. Vælg linjen for lasten i oversigtspanelet **Lastlinjer**.
1. Notér værdien for feltet **Antal oprettet under arbejde**.
1. under fanen **Laster** i gruppen **Relaterede oplysninger** i handlingsruden skal du vælge **Arbejde**.
1. Kontrollér, at arbejdet er udført på den endelige forsendelseslokation, og at det plukkede arbejdsantal svarer til det oprettede arbejdsantal på lastlinjen.
1. Hvis du finder uoverensstemmelser, skal du annullere det relevante arbejde, genkonfigurere lokationsvejledningen og frigive lasten igen. Du finder instruktioner under [Du kan ikke bekræfte en forsendelse, fordi der ikke er plukket varer](picked-quantity-is-not-on-final.md).
1. Gentag denne procedure for alle lastlinjer for at sikre, at alle kriterier er opfyldt.

### <a name="review-your-load-lines-to-make-sure-that-the-underdelivery-percentage-and-quantities-are-aligned-with-the-picked-work"></a>Gennemgå lastlinjerne for at sikre, at underleveringsprocenten og -mængderne er tilpasset det plukkede arbejde

Brug følgende procedure til at gennemgå lastlinjerne for at sikre, at underleveringsprocenten og -mængderne er tilpasset det plukkede arbejde.

1. Gå til **Lokationsstyring \> Laster \> Alle laster**.
1. Åbn den last, som forsendelsen ikke kan bekræftes for.
1. Vælg lastlinjen for den vare, der overstiger underleveringsprocenten, i oversigtspanelet **Lastlinjer**.
1. Juster værdien i feltet **Underlevering** eller feltet **Antal** efter behov.

> [!TIP]
> Hvis problemet stadig ikke er løst, skal du muligvis udføre mere plukarbejde for de relaterede salgsordrer eller flytteordrer, indtil det tilgængelige antal stemmer med lasten eller forsendelsen.
