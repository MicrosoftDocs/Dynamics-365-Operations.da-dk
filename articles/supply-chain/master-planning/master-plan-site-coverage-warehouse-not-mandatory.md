---
title: Varedisponering for lokalitetsdisponering, lagersted er ikke obligatorisk
description: I dette emne beskrives det, hvordan en vare med lokationsdimensionen indstillet til disponering bliver planlagt.
author: ChristianRytt
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2474
ms.assetid: 316da918-67ae-43c5-baea-00ae559e29b0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 484b178f3ac43f727fd6acb5deb40b7907c931ec
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579610"
---
# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a>Varedisponering for lokalitetsdisponering, lagersted er ikke obligatorisk

[!include [banner](../includes/banner.md)]

I dette emne beskrives det, hvordan en vare med lokationsdimensionen indstillet til disponering bliver planlagt.

Dette behovsplanlægningsscenario omfatter følgende forhold:

-   Lokationsdimensionen er angivet til obligatorisk og skal angives på behovsposteringen.
-   Lagerstedsdimensionen er ikke angivet til obligatorisk. Lagerstedet er måske kendt, men bruges ikke i beregningen i varedisponeringen.
-   Dimensionen for lokationen er angivet til disponering.
-   Dimensionen for lagerstedet er ikke angivet til disponering. Udbud og efterspørgsel aggregeres derfor efter lokation og måske også andre disponerede dimensioner.

I følgende grafik vises, hvordan varedisponering forløber. De parametre, der henvises til i grafikken, og deres placering er følgende:
-   Der er defineret varedisponering for varen. Klik på **Administration af produktoplysninger &gt; Produkter &gt; Frigivne produkter**. Vælg varen, og klik derefter på **Plan &gt; Varedisponering**.
-   Der er angivet påfyldningsrelationer for lagerstedet. Klik på **Lagerstyring &gt; Opsætning &gt; Lageropdeling &gt; Lagersteder**. Se feltgruppen **Hovedlagersted** under fanen **Overordnet planlægning**.
-   Standardordretypen er indstillet til Produktion, Indkøbsordre eller Kanban. Klik på **Administration af produktoplysninger &gt; Produkter &gt; Frigivne produkter**. Vælg varen, og klik derefter på **Plan &gt; Standardindstillinger for ordre**. I formen **Standardindstillinger for ordre** kan du se feltet **Standardordretype**.

![Efterspørgsel efter lokalitetsdisponering, lagersted er ikke obligatorisk.](./media/multisitedemandexplosionscenarioforsitecoveragewarehousenotmandatory.jpg)



## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over varedisponering og funktionen til flere lokationer](master-plan-multisite-functionality.md)

[Varedisponering for lokalitets- og lagerdisponering, obligatorisk lagersted](master-plan-site-coverage-warehouse-mandatory.md)

[Varedisponering for lokalitetsdisponering, obligatorisk lagersted](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Varedisponering for lokalitetsdisponering, lagersted ikke obligatorisk](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Bestemme styklisteversionen](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]