---
title: Udfoldning af styklisteversion
description: I denne artikel beskrives en varedisponeringssituation, der involverer udfoldning af en styklisteversion.
author: ChristianRytt
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: be4dfc85ad7ab01df9a95a394896873e2d649e12
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7575093"
---
# <a name="explosion-of-a-bom-version"></a>Udfoldning af styklisteversion

[!include [banner](../includes/banner.md)]

I denne artikel beskrives en varedisponeringssituation, der involverer udfoldning af en styklisteversion.

En efterspørgselsudfoldning af en styklisteversion opretter en efterspørgsel efter de enkelte varer på styklistelinjen på en bestemt lokation og muligvis på et bestemt lagersted. På en lokationsspecifik stykliste kan der defineres et bestemt lagersted defineret for de enkelte styklistelinjer. Og for de enkelte styklistelinjer bestemmer varens dimensionsindstillinger, om lagerstedet er påkrævet. Den resulterende efterspørgsel for de enkelte styklistelinjer bliver derefter startpunktet for en ekstra efterspørgselsudfoldning. Dette behovsplanlægningsscenario omfatter følgende forhold:

-   Lokationsdimensionen er obligatorisk og skal angives ved posteringen.
-   Lokationsdimensionen er konsistent. Lokationen for efterspørgsel på lavere niveau er derfor den samme som lokationen for posteringen af den indledende efterspørgsel.

I følgende grafik vises, hvordan efterspørgselsudfoldningen for behovsplanlægning forløber. ![Efterspørgselsudfoldning med styklisteversion.](./media/multisitedemandexplosionscenariousingbomversion.gif)

## <a name="additional-resources"></a>Yderligere ressourcer

[Bestemme styklisteversionen](master-plan-bom-version-determined.md)

[Oversigt over varedisponering og funktionen til flere lokationer](master-plan-multisite-functionality.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]