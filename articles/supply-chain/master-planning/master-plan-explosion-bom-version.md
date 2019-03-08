---
title: Udfoldning af styklisteversion
description: I denne artikel beskrives en varedisponeringssituation, der involverer udfoldning af en styklisteversion.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4f3c800d96805df38a2e31018f2d6c305e3ed7da
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "353902"
---
# <a name="explosion-of-a-bom-version"></a>Udfoldning af styklisteversion

[!include [banner](../includes/banner.md)]

I denne artikel beskrives en varedisponeringssituation, der involverer udfoldning af en styklisteversion.

En efterspørgselsudfoldning af en styklisteversion opretter en efterspørgsel efter de enkelte varer på styklistelinjen på en bestemt lokation og muligvis på et bestemt lagersted. På en lokationsspecifik stykliste kan der defineres et bestemt lagersted defineret for de enkelte styklistelinjer. Og for de enkelte styklistelinjer bestemmer varens dimensionsindstillinger, om lagerstedet er påkrævet. Den resulterende efterspørgsel for de enkelte styklistelinjer bliver derefter startpunktet for en ekstra efterspørgselsudfoldning. Dette behovsplanlægningsscenario omfatter følgende forhold:

-   Lokationsdimensionen er obligatorisk og skal angives ved posteringen.
-   Lokationsdimensionen er konsistent. Lokationen for efterspørgsel på lavere niveau er derfor den samme som lokationen for posteringen af den indledende efterspørgsel.

I følgende grafik vises, hvordan efterspørgselsudfoldningen for behovsplanlægning forløber. ![Efterspørgselsudfoldning med styklisteversion](./media/multisitedemandexplosionscenariousingbomversion.gif)

<a name="additional-resources"></a>Yderligere ressourcer
--------

[Varedisponering – Sådan bestemmes styklisteversionen](master-plan-bom-version-determined.md)

[Varedisponering og funktionen til flere lokationer](master-plan-multisite-functionality.md)



