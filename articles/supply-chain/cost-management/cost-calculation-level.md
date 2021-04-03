---
title: Omkostningsberegningsniveau
description: Dette emne beskriver det styklisteniveau, der er navngivet Omkostningsberegningsniveau. Dette styklisteniveau omfatter ikke produktion og batchordrer fra beregningerne.
author: AndersGirke
manager: tfehr
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 1cfbbb6aadbd24a0352776285f6c60ff10f59549
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251020"
---
# <a name="cost-calculation-level"></a>Omkostningsberegningsniveau

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