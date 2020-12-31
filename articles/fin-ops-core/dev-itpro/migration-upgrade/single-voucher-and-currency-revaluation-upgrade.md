---
title: Opgradere enkeltbilagskladder og værdireguleringer af valuta
description: Nogle organisationer angiver kladder, der indeholder et enkelt bilag, der har mere end én debitor eller kreditor, og de kører også processen til værdiregulering af udenlandsk valuta for debitorer eller kreditorer. I dette emne beskrives den fremgangsmåde, som disse organisationer skal følge, når de opgraderer til Microsoft Dynamics 365 for Operations version 1611.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7c06e54c5be8d0a410b9f15f2a89def3076b4638
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681018"
---
# <a name="upgrade-single-voucher-journals-and-currency-revaluations"></a>Opgradere enkeltbilagskladder og værdireguleringer af valuta

[!include [banner](../includes/banner.md)]

Nogle organisationer angiver kladder, der indeholder et enkelt bilag, der har mere end én debitor eller kreditor, og de kører også processen til værdiregulering af udenlandsk valuta for debitorer eller kreditorer. I dette emne beskrives den fremgangsmåde, som disse organisationer skal følge, når de opgraderer til Microsoft Dynamics 365 for Operations version 1611.

Følg disse trin, når du opgraderer til Microsoft Dynamics 365 for Operations version 1611.

1.  Før du opgraderer til Finance and Operations, skal du køre processerne til værdiregulering af udenlandsk valuta for debitorer og kreditorer. Angiv feltet **Metode** til **Fakturadato**. Der oprettes en værdireguleringspostering, der tilbagefører den sidste værdiregulering af udenlandsk valuta. Derfor værdiansættes de åbne posteringer til deres oprindelige regnskabsvaluta.
2.  Opgrader til version 1611.
3.  Kør processerne til værdiregulering af udenlandsk valuta for debitorer og kreditorer igen. Denne gang skal feltet **Metode** angives til **Standard**. Der oprettes en ny værdireguleringspostering, der er baseret på de aktuelle valutakurser. Denne transaktion registrerer urealiseret gevinst eller tab og den korrekte samlefinanskonto.
