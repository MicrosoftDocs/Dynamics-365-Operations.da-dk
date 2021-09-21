---
title: Du kan ikke konsolidere flere produktkvitteringer i en enkelt indkøbsordre
description: Du kan ikke konsolidere flere produktkvitteringer i en enkelt indkøbsordre, hvis de forskellige produktkvitteringslinjer har forskellige regnskabsdatoer.
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 485306279281ceb55a140526f4216af35574af42
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475873"
---
# <a name="you-cant-consolidate-multiple-product-receipts-into-a-single-purchase-order"></a>Du kan ikke konsolidere flere produktkvitteringer i en enkelt indkøbsordre

## <a name="symptoms"></a>Symptomer

Du kan ikke konsolidere flere produktkvitteringer i en enkelt indkøbsordre, hvis de forskellige produktkvitteringslinjer har forskellige regnskabsdatoer.

## <a name="resolution"></a>Løsning

I tidligere versioner af Dynamics 365 Supply Chain Management var konsolidering tilladt i denne situation. Det er dog fejlrisiko ved denne praksis. Regnskabsdatoen på de indkøbsordrelinjer, der oprettes, bør ikke være forskellige fra regnskabsdatoen på de produktkvitteringslinjer, som disse indkøbsordrelinjer er oprettet ud fra. (Regnskabsdatoen på indkøbsordrelinjerne svarer til regnskabsdatoen på indkøbsordrehovedet). Det er derfor ikke længere tilladt at konsolidere flere produktkvitteringer i en enkelt indkøbsordre.

Regnskabsdatoen bruges f.eks. ved budgetreservationer og behæftelser. Derfor skal den beholdes under overgangen fra produktkvittering til indkøbsordre.
