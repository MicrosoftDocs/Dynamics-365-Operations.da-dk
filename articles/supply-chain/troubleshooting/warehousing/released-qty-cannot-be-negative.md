---
title: En lastlinje kan ikke opdateres, fordi det frigivne antal vil være negativt
description: Dette problem opstår, når du opdaterer eller sletter en lastlinje, og det vil medføre et negativt frigivet antal.
author: GalynaFedorova
ms.date: 6/30/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningListPage_WHSLoadLineUnShipQty,WHSLoadTable_WHSLoadLineUnShipQty,WHSLoadPlanningWorkbench_WHSLoadLineUnShipQty,WHSShipmentDetails_WHSLoadLineUnShipQty,WHSLoadPlanningListPage_DeleteButtonLoadLine,WHSLoadTable_DeleteButtonLoadLine,WHSLoadPlanningWorkbench_DeleteButtonLoadLine,WHSShipmentDetails_DeleteButtonShipment
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a6325a632e1f68a0a3a9cb6b6091c48da014a405e8ce9ad69ea841f5cceb216f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6728453"
---
# <a name="cant-update-a-load-line-because-the-released-quantity-would-be-negative"></a>En lastlinje kan ikke opdateres, fordi det frigivne antal vil være negativt

Fejlkode: @WAX:ReleasedQtyCannotBeNegative

## <a name="symptoms"></a>Symptomer

Dette problem opstår, når du opdaterer eller sletter en lastlinje, og det vil medføre et negativt frigivet antal. Hvis det er tilfældet, vises følgende fejlmeddelelse, når du prøver at opdatere eller slette lastlinjen:

> Udleveret antal må ikke være negativt for varen %1, partiet %2.

Du kan derfor ikke opdatere eller slette lastlinjen.

## <a name="cause"></a>Årsag

Når du har opdateret eller slettet en lastlinje, opdaterer systemet det frigivne antal for den relaterede salgslinje (*whsSalesLine.ReleaseQty*). Systemet evaluerer det frigivne antal, og hvis det finder ud af, at det frigivne antal på linjen vil være negativt efter opdateringen, vil det ikke lade dig opdatere eller slette linjen. Denne validering sker, når du forsøger at opdatere enten antallet på lastlinjen eller måleenheden via forskellige handlinger, f.eks. sletning af en lastlinje, sletning af en forsendelse, ændring af antallet i en lastlinje, reduktion af plukket antal og kort plukning.

Den mest almindelige rodårsag til dette problem er en ændring i enhedsomregningen, der bruges til åbne lastlinjer. Enhedsomregningen, da en salgsordre blev frigivet, var f.eks. *50 hver = 1 PL*. Men før den relaterede lastforsendelse blev afsluttet, blev enhedsomregningen ændret til *100 hver = 1 PL*.

## <a name="resolution"></a>Løsning

Løsningen er at tilbageføre enhedsomregningsændringerne, opdatere eller slette lastlinjen og derefter implementere omregningen igen. Du skal forhindre andre laster, der indeholder den vare, der forårsagede problemet, i at blive behandlet, indtil problemet er løst. Ellers kan de nye omregninger blive brugt til andre laster, der allerede er åbne.

Du kan løse dette problem ved at udføre følgende opgaver:

1. Gennemse den enhedsomregning, der blev brugt til lastlinjen.
2. Gennemse den aktuelle enhedsomregning for varen, og foretag reguleringer, der gør det muligt at opdatere eller slette lastlinjen.
3. Opdater eller slet lastlinjen, og tilbagefør reguleringerne af enhedsomregninger.

### <a name="review-the-unit-conversion-that-was-used-for-the-load-line"></a>Gennemse den enhedsomregning, der blev brugt til lastlinjen

Benyt følgende fremgangsmåde til at gennemse lastlinjerne og notere dig den enhedsomregning, der blev brugt til lastlinjen.

1. Gå til **Lokationsstyring \> Laster \> Alle laster**.
1. Vælg den last, der omfatter den lastlinje, der ikke kan slettes eller opdateres.
1. under fanen **Laster** i gruppen **Relaterede oplysninger** i handlingsruden skal du vælge **Arbejde**.
1. Vælg det relevante arbejds-id i det øverste gitter.
1. Beregn omregningssatsen mellem værdien af **Arbejdsantal for lager** og værdien af **Arbejdsantal** under fanen **Generelt** nederst på siden. Notér dig satsen.
1. Gentag denne procedure for alle relevante arbejds-id'er for at sikre, at samme omregning blev anvendt.

### <a name="review-the-current-unit-conversion-for-the-item-and-make-adjustments"></a>Gennemgå den aktuelle enhedsomregning for varen, og foretag reguleringer

Brug følgende procedure til at gennemse produktets enhedsomregning og foretage justeringer for at sikre, at enhedsomregningen er tilpasset lastlinjen.

1. Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.
1. Åbn det relevante produkt for at gå til dets side med **Frigivne produktdetaljer**.
1. Gå til handlingsruden, og vælg **Enhedsomregninger** i gruppen **Opsætning** under fanen **Produkt**.
1. Vælg omregningen mellem enhederne, og foretag reguleringer ved hjælp af den omregning, du fandt i forrige afsnit.

### <a name="update-or-delete-the-load-line-and-revert-the-unit-conversion-adjustments"></a>Opdatere eller slette lastlinjen og tilbageføre reguleringerne af enhedsomregninger

Benyt følgende fremgangsmåde for at behandle lastlinjen efter behov og tilbageføre enhedsomregningerne.

1. Gå til **Lokationsstyring \> Laster \> Alle laster**.
1. Åbn den last, der omfatter den lastlinje, der ikke kan slettes eller opdateres.
1. Vælg linjen for lasten i oversigtspanelet **Lastlinjer**.
1. Fortsæt med de nødvendige handlinger efter behov. (Du kan f.eks. slette lastlinjen eller ændre dens antal).
1. Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.
1. Åbn det relevante produkt for at gå til dets side med **Frigivne produktdetaljer**.
1. Gå til handlingsruden, og vælg **Enhedsomregninger** i gruppen **Opsætning** under fanen **Produkt**.
1. Vælg omregningen mellem enhederne, og tilbagefør de reguleringer, du foretog i forrige afsnit.
