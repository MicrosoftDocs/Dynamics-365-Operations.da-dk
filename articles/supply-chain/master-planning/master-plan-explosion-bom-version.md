---
title: Udfoldning af styklisteversion
description: I denne artikel beskrives en varedisponeringssituation, der involverer udfoldning af en styklisteversion.
author: t-benebo
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
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1ef8a04ce4ab2180f39a6d2bcdab976eb146d610
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/03/2022
ms.locfileid: "9741224"
---
# <a name="explosion-of-a-bom-version"></a>Udfoldning af styklisteversion

[!include [banner](../includes/banner.md)]

I denne artikel beskrives en varedisponeringssituation, der involverer udfoldning af en styklisteversion.

En efterspørgselsudfoldning af en styklisteversion opretter en efterspørgsel efter de enkelte varer på styklistelinjen på en bestemt lokation og muligvis på et bestemt lagersted. På en lokationsspecifik stykliste kan der defineres et bestemt lagersted defineret for de enkelte styklistelinjer. Og for de enkelte styklistelinjer bestemmer varens dimensionsindstillinger, om lagerstedet er påkrævet. Den resulterende efterspørgsel for de enkelte styklistelinjer bliver derefter startpunktet for en ekstra efterspørgselsudfoldning. Dette behovsplanlægningsscenario omfatter følgende forhold:

-   Lokationsdimensionen er obligatorisk og skal angives ved posteringen.
-   Lokationsdimensionen er konsistent. Lokationen for efterspørgsel på lavere niveau er derfor den samme som lokationen for posteringen af den indledende efterspørgsel.

I følgende grafik vises, hvordan efterspørgselsudfoldningen for behovsplanlægning forløber. ![Efterspørgselsudfoldning med styklisteversion.](./media/multisitedemandexplosionscenariousingbomversion.gif)

## <a name="additional-resources"></a>Yderligere ressourcer

- [Bestemme styklisteversionen](master-plan-bom-version-determined.md)
- [Oversigt over varedisponering og funktionen til flere lokationer](master-plan-multisite-functionality.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]