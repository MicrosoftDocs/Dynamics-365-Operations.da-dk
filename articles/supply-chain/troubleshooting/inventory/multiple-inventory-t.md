---
title: Flere lagertransaktioner for batchnumre, når Ved fysisk opdatering er deaktiveret
description: Flere lagertransaktioner oprettes, når du har reguleret en indkøbsordrelinje for varer, hvor indstillingen Ved fysisk opdatering for batchnummergruppen er indstillet til Nej.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventNumGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: b8aef8835e90b7437bb7833c13c3d287d4ca836bf1fefc01bfeafef1c93329bc
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768588"
---
# <a name="multiple-inventory-transactions-for-batch-numbers-when-on-physical-update-is-disabled"></a>Flere lagertransaktioner for batchnumre, når Ved fysisk opdatering er deaktiveret

KB-nummer: 4613390

## <a name="symptoms"></a>Symptomer

Flere lagertransaktioner oprettes, når du har reguleret en indkøbsordrelinje for varer, hvor indstillingen **Ved fysisk opdatering** for batchnummergruppen er indstillet til *Nej*.

Når du opretter en vare, hvor indstillingen **Ved fysisk opdatering** for batchnummergruppen er indstillet til *Nej*, opretter systemet automatisk et nyt batchnummer, hvis du redigerer et antal på indkøbslinjen, og gemmer indkøbsordresiden.

## <a name="resolution"></a>Løsning

Indstillingen **Ved fysisk opdatering** for batchnummergrupper fungerer på følgende måde:

- Når indstillingen er *Ja*, oprettes der først nye batchnumre, efter at der er sket en fysisk opdatering (f.eks. når der afsendes eller modtages varer).
- Når indstillingen er *Nej*, oprettes der et nyt batchnummer, hver gang der finder en relevant opdatering sted (f.eks. når der føjes et nyt antal til en indkøbsordre).
