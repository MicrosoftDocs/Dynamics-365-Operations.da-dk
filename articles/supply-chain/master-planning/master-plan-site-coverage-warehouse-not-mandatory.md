---
title: Varedisponering for lokalitetsdisponering, lagersted er ikke obligatorisk
description: Denne artikel beskriver, hvordan en vare med lokationsdimensionen indstillet til disponering bliver planlagt.
author: t-benebo
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
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6b03bd1970aa7a2f3276186a0a9f8c2cd2880956
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/03/2022
ms.locfileid: "9741143"
---
# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a>Varedisponering for lokalitetsdisponering, lagersted er ikke obligatorisk

[!include [banner](../includes/banner.md)]

Denne artikel beskriver, hvordan en vare med lokationsdimensionen indstillet til disponering bliver planlagt.

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

- [Oversigt over varedisponering og funktionen til flere lokationer](master-plan-multisite-functionality.md)
- [Varedisponering for lokalitets- og lagerdisponering, obligatorisk lagersted](master-plan-site-coverage-warehouse-mandatory.md)
- [Varedisponering for lokalitetsdisponering, obligatorisk lagersted](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)
- [Varedisponering for lokalitetsdisponering, lagersted ikke obligatorisk](master-plan-site-warehouse-coverage-warehouse-mandatory.md)
- [Bestemme styklisteversionen](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]