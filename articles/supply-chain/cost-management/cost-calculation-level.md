---
title: Omkostningsberegningsniveau
description: Dette emne beskriver det styklisteniveau, der er navngivet Omkostningsberegningsniveau. Dette styklisteniveau omfatter ikke produktion og batchordrer fra beregningerne.
author: AndersGirke
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: e08d11c8e9d98e56c5ef076cbab7bb68bedea62a
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7581026"
---
# <a name="cost-calculation-level"></a>Omkostningsberegningsniveau

[!include [banner](../includes/banner.md)]

Styklisteniveauet, der er navngivet **Omkostningsberegningsniveau** udelukker produktionsordrer og batchordrer fra beregningerne. Systemet bruger dette niveau, når det kører omkostningsberegninger i efterkalkulationsversioner. I processer som genberegning og lagerlukning bruger systemet styklisteniveauet **Efterkalkulationsniveauet** i stedet.

I følgende simple scenarie vises forskellene mellem styklisteniveauet **Omkostningsberegningsniveau** og styklisteniveauet **Efterkalkulationsniveau**.

Du har tre produkter: A, B og C. Produkt C er komponent i produkt B, og produkt B er komponent i produkt A.

- **Efterkalkulationsniveau** tildeler følgende styklisteniveauer:

    - **Produkt A:** 0
    - **Produkt B:** 1
    - **Produkt C:** 2

- **Omkostningsberegningsniveau** tildeler følgende styklisteniveauer:

    - **Produkt A:** 0
    - **Produkt B:** 1
    - **Produkt C:** 2

Derefter oprettes der en produktionsordre til produkt C, og produkt A føjes til produktionsordrens stykliste. Når ordren er forkalkuleret, opdateres styklisteniveauerne på følgende måde:

- **Efterkalkulationsniveau** tildeler følgende styklisteniveauer:

    - **Produkt B:** 1
    - **Produkt C:** 2
    - **Produkt A:** 3

- **Omkostningsberegningsniveau** tildeler følgende styklisteniveauer:

    - **Produkt A:** 0
    - **Produkt B:** 1
    - **Produkt C:** 2

Denne funktionsmåde sikrer, at ændringer i produktionsordrestyklister ikke påvirker de efterfølgende omkostningsberegninger.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]