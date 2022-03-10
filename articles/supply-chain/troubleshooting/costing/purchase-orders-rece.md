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
ms.openlocfilehash: 49faa2c68d496c5c0d8c7e4abfd93d9a917857220dd23c09a050fa3436e1d49a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746861"
---
# <a name="physically-received-purchase-orders-dont-appear-on-the-inventory-closing-report"></a>Fysisk modtagne indkøbsordrer vises ikke i lagerlukningsrapporten

KB-nummer: 4612595

## <a name="symptoms"></a>Symptomer

Fysisk modtagne indkøbsordrer vises ikke i lagerlukningsrapporten **Kontroller åbne antal**.

## <a name="resolution"></a>Løsning

Rapporten **Kontroller åbne antal** viser afgangsposteringer, der ikke kan udlignes mod økonomisk opdaterede lagertilgange pr. den valgte slutdato. Du kan vælge at medtage fysiske tilgange i rapporten. Hvis du gør det, vises fysiske tilgange, hvis de kan dække afgangsposteringer, der ikke kan udlignes. Du finder flere oplysninger under [Forberede kørsel af lagerlukning](/dynamicsax-2012/appuser-itpro/preparing-to-run-inventory-close).
