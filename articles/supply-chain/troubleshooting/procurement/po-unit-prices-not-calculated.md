---
title: Enhedspriser på indkøbsordrer beregnes ikke ud fra enhedsomregningen
description: Enhedspriser på indkøbsordrer beregnes ikke ud fra enhedsomregningen
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 4695f4661c3abb8ab38e3ca74b513e8529e37d20
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475899"
---
# <a name="unit-prices-on-purchase-orders-arent-calculated-based-on-the-unit-conversion"></a>Enhedspriser på indkøbsordrer beregnes ikke ud fra enhedsomregningen

## <a name="symptoms"></a>Symptomer

Når en enhed ændres i en indkøbsordre, genberegnes priserne for samhandelsaftaler ikke ifølge definitionerne for enhedsomregning.

## <a name="cause"></a>Årsag

Priser hentes altid fra samhandelsaftaler (eller andre prisindstillinger i systemet, f.eks. salgsaftaler eller varepriser), og de angives for en enhed.

Hvis enheden ændres på en ordrelinje, søger systemet efter en pris for den nye enhed og anvender denne pris. Hvis der ikke findes en pris for enheden, vil systemet ikke anvende en pris. Enhedsomregningen kan ikke bruges til at genberegne prisen til en anden enhed. Teoretisk er prisen for en kasse på ti måske ikke lig med ti gange prisen på en enkelt kasse.

## <a name="workaround"></a>Løsning

En måde at løse dette problem på er at sikre, at der bruges samhandelsaftaler for de enheder, du forventer skal bruges på ordrelinjerne for varen.
