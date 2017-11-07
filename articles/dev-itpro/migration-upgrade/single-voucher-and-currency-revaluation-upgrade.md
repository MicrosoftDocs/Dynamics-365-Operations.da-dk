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
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 13ad43cc77731727525aae1edc4d405c166acbc1
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="single-voucher-and-currency-revaluation-upgrade"></a>Opgradering for enkelt bilag og værdiregulering af valuta

[!include[banner](../includes/banner.md)]


Nogle organisationer angiver kladder, der indeholder et enkelt bilag, der har mere end én debitor eller kreditor, og de kører også processen til værdiregulering af udenlandsk valuta for debitorer eller kreditorer. I dette emne beskrives den fremgangsmåde, som disse organisationer skal følge, når de opgraderer til Microsoft Dynamics 365 Operations version 1611.

Følg disse trin, når du opgraderer til Microsoft Dynamics 365 for Operations version 1611.

1.  Før du opgraderer til Dynamics 365 for Operations, skal du køre processerne til værdiregulering af udenlandsk valuta for debitorer og kreditorer. Angiv feltet **Metode** til **Fakturadato**. Der oprettes en værdireguleringspostering, der tilbagefører den sidste værdiregulering af udenlandsk valuta. Derfor værdiansættes de åbne posteringer til deres oprindelige regnskabsvaluta.
2.  Opgrader til Dynamics 365 for Operations version 1611.
3.  Kør processerne til værdiregulering af udenlandsk valuta for debitorer og kreditorer igen. Denne gang skal feltet **Metode** angives til **Standard**. Der oprettes en ny værdireguleringspostering, der er baseret på de aktuelle valutakurser. Denne transaktion registrerer urealiseret gevinst eller tab og den korrekte samlefinanskonto.





