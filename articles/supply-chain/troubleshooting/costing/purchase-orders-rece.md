---
title: Fysisk modtagne indkøbsordrer vises ikke i lagerlukningsrapporten
description: Fysisk modtagne indkøbsordrer vises ikke i lagerlukningsrapporten Kontroller åbne antal.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventOpenQtyCritical
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 9508d6d75d8ebee7ca10140ed4c4215d7ad1dda7
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026371"
---
# <a name="physically-received-purchase-orders-dont-appear-on-the-inventory-closing-report"></a>Fysisk modtagne indkøbsordrer vises ikke i lagerlukningsrapporten

KB-nummer: 4612595

## <a name="symptoms"></a>Symptomer

Fysisk modtagne indkøbsordrer vises ikke i lagerlukningsrapporten **Kontroller åbne antal**.

## <a name="resolution"></a>Løsning

Rapporten **Kontroller åbne antal** viser afgangsposteringer, der ikke kan udlignes mod økonomisk opdaterede lagertilgange pr. den valgte slutdato. Du kan vælge at medtage fysiske tilgange i rapporten. Hvis du gør det, vises fysiske tilgange, hvis de kan dække afgangsposteringer, der ikke kan udlignes. Du finder flere oplysninger under [Forberede kørsel af lagerlukning](/dynamicsax-2012/appuser-itpro/preparing-to-run-inventory-close).
