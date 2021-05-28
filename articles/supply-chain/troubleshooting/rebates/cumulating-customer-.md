---
title: Akkumulering af debitorrabatter mislykkes, når der bruges varerabatgrupper
description: Når du bruger debitorrabataftaler sammen med varerabatgrupper, beregnes rabatter, men akkumuleringen mislykkes.
author: sherry-zheng
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PdsRebateTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 5222d5a52a34ecfa4a1eac96a2cb561f257f17ea
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026361"
---
# <a name="cumulation-of-customer-rebates-fails-when-item-rebate-groups-are-used"></a>Akkumulering af debitorrabatter mislykkes, når der bruges varerabatgrupper

KB-nummer: 4611372

## <a name="symptoms"></a>Symptomer

Når du bruger debitorrabataftaler (af typen *beløb*) sammen med varerabatgrupper, beregnes rabatter, men akkumuleringen mislykkes.

## <a name="resolution"></a>Løsning

Systemet fungerer som designet. Varegrupper grupperer kun varer, der har samme grænsebetingelse. Rabatbetingelsen (grænseværdien) angives i forhold til beløbet for hver vare og ikke i forhold til det akkumulerede beløb for en vare i varegruppen.
