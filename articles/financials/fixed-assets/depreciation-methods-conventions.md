---
title: Afskrivningsmetoder og -principper
description: Denne artikel indeholder en oversigt over afskrivningsprincipper og afskrivningsmetoder, der understøttes af Microsoft Dynamics 365 for Finance and Operations.
author: ShylaThompson
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile, AssetGroupBookSetup, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3441
ms.assetid: 1d8267b1-86a8-44bf-8814-f56b5d45a0ae
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: be8e05a386178b9172a906109e015269dc72b32e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569649"
---
# <a name="depreciation-methods-and-conventions"></a>Afskrivningsmetoder og -principper

[!include [banner](../includes/banner.md)]

Denne artikel indeholder en oversigt over afskrivningsprincipper og afskrivningsmetoder, der understøttes af Microsoft Dynamics 365 for Finance and Operations.

Du kan vælge mellem forskellige afskrivningsmetoder og -principper. Formålet med metoderne er at fordele den værdi af et anlægsaktiv, der kan afskrives, på flere regnskabsperioder. Den værdi af et anlægsaktiv, der kan afskrives, er anskaffelsesprisen minus en eventuel scrapværdi. 

Hvis du bruger afskrivningsprincipper, og du ændrer den seneste startdato for afskrivning på et aktiv, så der springes nogle afskrivninger over, kan afskrivningen for det sidste år blive større eller mindre end forventet. Afskrivningen reguleres med det antal afskrivningsperioder, der påvirkes af ændringen af den seneste startdato for afskrivning.

Hvis du f.eks. bruger afskrivningsprincippet Halvår over tre år, afskrives der normalt over 3½ år. Hvis du ændrer den seneste startdato for afskrivning i løbet af de 3½ år, flytter det sidste afskrivningsår uden for det antal perioder, der påvirkes. Hvis du flytter datoen tre måneder, er der ni måneder, hvor der kan afskrives i det sidste år, hvor det normalt ellers ville være seks måneder.

Du kan vælge mellem følgende afskrivningsprincipper.


-   Halvår
-   Hel måned
-   Midt i kvartal
-   Midt i måned (d. 1. i måneden)
-   Midt i måned (d. 15. i måneden)
-   Halvår (årsstart)
-   Halvår (næste år)

Du kan vælge mellem følgende afskrivningsmetoder.
-   Lineær afskrivning over servicelevetiden
-   Saldoværdi
-   Manuelt
-   Faktor
-   Forbrug
-   Lineær afskrivning for den resterende levetid
-   200 % saldoværdi
-   175 % saldoværdi
-   150 % saldoværdi
-   125 % saldoværdi





<a name="additional-resources"></a>Yderligere ressourcer
--------

[Afskrivning af anlægsaktiv](fixed-asset-depreciation.md)

[Lineær afskrivning for levetiden](Straight-line-service-life-depreciation.md)

[Saldoafskrivning](reduce-balance-depreciation.md)

[Manuel afskrivning](manual-depreciation.md)

[Faktorafskrivning](factor-depreciation.md)

[Forbrugsafskrivning](consumption-depreciation.md)

[Lineær afskrivning for den resterende levetid](straight-line-life-remaining-depreciation.md)

[125 % saldoafskrivning](125-percent-reducing-balance-depreciation.md)

[150 % saldoafskrivning](150-percent-reducing-balance-depreciation.md)

[175 % saldoafskrivning](175-percent-reducing-balance-depreciation.md)

[200 % saldoafskrivning](200-percent-reducing-balance-depreciation.md)



