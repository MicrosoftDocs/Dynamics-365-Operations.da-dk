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
ms.openlocfilehash: fc3381dab77cf80c0fd65f3bc27c11b814e72368631bd0e2145aac0be4f4fba4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760364"
---
# <a name="cumulation-of-customer-rebates-fails-when-item-rebate-groups-are-used"></a>Akkumulering af debitorrabatter mislykkes, når der bruges varerabatgrupper

KB-nummer: 4611372

## <a name="symptoms"></a>Symptomer

Når du bruger debitorrabataftaler (af typen *beløb*) sammen med varerabatgrupper, beregnes rabatter, men akkumuleringen mislykkes.

## <a name="resolution"></a>Løsning

Systemet fungerer som designet. Varegrupper grupperer kun varer, der har samme grænsebetingelse. Rabatbetingelsen (grænseværdien) angives i forhold til beløbet for hver vare og ikke i forhold til det akkumulerede beløb for en vare i varegruppen.
