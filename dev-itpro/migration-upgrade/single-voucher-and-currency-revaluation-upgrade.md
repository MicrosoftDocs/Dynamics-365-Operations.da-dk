---
title: "Opgradering for enkelt bilag og værdiregulering af valuta til Microsoft Dynamics 365 for Operations version 1611"
description: "Nogle organisationer angiver kladder, der indeholder et enkelt bilag, der har mere end én debitor eller kreditor, og de kører også processen til værdiregulering af udenlandsk valuta for debitorer eller kreditorer. I dette emne beskrives den fremgangsmåde, som disse organisationer skal følge, når de opgraderer til Microsoft Dynamics 365 Operations version 1611."
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

# <a name="single-voucher-and-currency-revaluation-upgrade-for-microsoft-dynamics-365-for-operations-version-1611"></a>Opgradering for enkelt bilag og værdiregulering af valuta til Microsoft Dynamics 365 for Operations version 1611

Nogle organisationer angiver kladder, der indeholder et enkelt bilag, der har mere end én debitor eller kreditor, og de kører også processen til værdiregulering af udenlandsk valuta for debitorer eller kreditorer. I dette emne beskrives den fremgangsmåde, som disse organisationer skal følge, når de opgraderer til Microsoft Dynamics 365 Operations version 1611.

Følg disse trin, når du opgraderer til Microsoft Dynamics 365 for Operations version 1611.

1.  Før du opgraderer til Dynamics 365 for Operations, skal du køre processerne til værdiregulering af udenlandsk valuta for debitorer og kreditorer. Angiv feltet **Metode** til **Fakturadato**. Der oprettes en værdireguleringspostering, der tilbagefører den sidste værdiregulering af udenlandsk valuta. Derfor værdiansættes de åbne posteringer til deres oprindelige regnskabsvaluta.
2.  Opgrader til Dynamics 365 for Operations version 1611.
3.  Kør processerne til værdiregulering af udenlandsk valuta for debitorer og kreditorer igen. Denne gang skal feltet **Metode** angives til **Standard**. Der oprettes en ny værdireguleringspostering, der er baseret på de aktuelle valutakurser. Denne transaktion registrerer urealiseret gevinst eller tab og den korrekte samlefinanskonto.



