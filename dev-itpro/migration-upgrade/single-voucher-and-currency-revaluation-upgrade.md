---
title: "Enkelt bilag og værdiregulering af valuta opgraderes til Microsoft Dynamics 365 for operationer version 1611 opdager"
description: "Nogle organisationer Angiv kladder, der indeholder et enkelt bilag, der har mere end én debitor eller kreditor, og de kører også debitor eller konti processen til værdiregulering af udenlandsk valuta, der skal betales. I dette emne beskrives de fremgangsmåde, som disse organisationer skal følge, når de opgraderer til Microsoft Dynamics 365 for operationer version 1611 opdager."
author: twheeloc
manager: AnnBe
ms.date: 2016-12-28 16 - 04 - 17
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: d42c753d0dc8b8efc2a0d2a26da32a4951d85503
ms.lasthandoff: 03/31/2017


---

# <a name="single-voucher-and-currency-revaluation-upgrade-for-microsoft-dynamics-365-for-operations-version-1611"></a>Enkelt bilag og værdiregulering af valuta opgraderes til Microsoft Dynamics 365 for operationer version 1611 opdager

Nogle organisationer Angiv kladder, der indeholder et enkelt bilag, der har mere end én debitor eller kreditor, og de kører også debitor eller konti processen til værdiregulering af udenlandsk valuta, der skal betales. I dette emne beskrives de fremgangsmåde, som disse organisationer skal følge, når de opgraderer til Microsoft Dynamics 365 for operationer version 1611 opdager.

Følg disse trin, når du opgraderer til Microsoft Dynamics 365 for operationer version 1611 opdager.

1.  Før du opgraderer til Dynamics 365 for operationer, køre processerne, der værdiregulering af udenlandsk valuta for debitorer og kreditorer. Angiv den **metode** til **fakturadato**. Der oprettes en værdiregulering postering, der vender den sidste værdiregulering af udenlandsk valuta. Derfor er de åbne posteringer værdiansættes til deres oprindelige regnskabsvaluta.
2.  Opgradere til Dynamics 365 for operationer version 1611 opdager.
3.  Kør debitor og konti skal betales udenlandsk valuta værdiregulering processer igen. Denne gang, den **metode** til **Standard**. Der oprettes en ny værdiregulering postering, der er baseret på de aktuelle valutakurser. Denne transaktion registreres Urealiseret gevinst eller tab og den korrekte samlefinanskonto.



