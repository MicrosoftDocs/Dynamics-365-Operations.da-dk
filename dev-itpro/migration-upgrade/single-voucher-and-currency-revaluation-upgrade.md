---
title: "Opgradering for enkelt bilag og værdiregulering af valuta"
description: "Nogle organisationer angiver kladder, der indeholder et enkelt bilag, der har mere end én debitor eller kreditor, og de kører også processen til værdiregulering af udenlandsk valuta for debitorer eller kreditorer. I dette emne beskrives den fremgangsmåde, som disse organisationer skal følge, når de opgraderer til Microsoft Dynamics 365 Operations version 1611."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: d3c6d817424be79b09ccdd89deb7f31599fe9bf5
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017

---

# <a name="single-voucher-and-currency-revaluation-upgrade"></a>Opgradering for enkelt bilag og værdiregulering af valuta

[!include[banner](../includes/banner.md)]


Nogle organisationer angiver kladder, der indeholder et enkelt bilag, der har mere end én debitor eller kreditor, og de kører også processen til værdiregulering af udenlandsk valuta for debitorer eller kreditorer. I dette emne beskrives den fremgangsmåde, som disse organisationer skal følge, når de opgraderer til Microsoft Dynamics 365 Operations version 1611.

Følg disse trin, når du opgraderer til Microsoft Dynamics 365 for Operations version 1611.

1.  Før du opgraderer til Dynamics 365 for Operations, skal du køre processerne til værdiregulering af udenlandsk valuta for debitorer og kreditorer. Angiv feltet **Metode** til **Fakturadato**. Der oprettes en værdireguleringspostering, der tilbagefører den sidste værdiregulering af udenlandsk valuta. Derfor værdiansættes de åbne posteringer til deres oprindelige regnskabsvaluta.
2.  Opgrader til Dynamics 365 for Operations version 1611.
3.  Kør processerne til værdiregulering af udenlandsk valuta for debitorer og kreditorer igen. Denne gang skal feltet **Metode** angives til **Standard**. Der oprettes en ny værdireguleringspostering, der er baseret på de aktuelle valutakurser. Denne transaktion registrerer urealiseret gevinst eller tab og den korrekte samlefinanskonto.





