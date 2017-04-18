---
title: Varedisponering for lokationsdisponering, lagersted er ikke obligatorisk
description: I dette emne beskrives det, hvordan en vare med lokationsdimensionen indstillet til disponering bliver planlagt.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2474
ms.assetid: 316da918-67ae-43c5-baea-00ae559e29b0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 28607f0fc8db99c9fc8e96b4514763b8cf589dd8
ms.lasthandoff: 03/31/2017


---

# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a>Varedisponering for lokationsdisponering, lagersted er ikke obligatorisk

I dette emne beskrives det, hvordan en vare med lokationsdimensionen indstillet til disponering bliver planlagt.

Dette behovsplanlægningsscenario omfatter følgende forhold:

-   Lokationsdimensionen er angivet til obligatorisk og skal angives på behovsposteringen.
-   Lagerstedsdimensionen er ikke angivet til obligatorisk. Lagerstedet er måske kendt, men bruges ikke i beregningen i varedisponeringen.
-   Dimensionen for lokationen er angivet til disponering.
-   Dimensionen for lagerstedet er ikke angivet til disponering. Udbud og efterspørgsel aggregeres derfor efter lokation og måske også andre disponerede dimensioner.

I følgende grafik vises, hvordan varedisponering forløber. De parametre, der henvises til i grafikken, og deres placering er følgende:
-   Der er defineret varedisponering for varen. Klik på **administration af produktoplysninger &gt;produkter&gt; frigivne produkter**. Vælg varen, og klik derefter på **Plan &gt;Varedisponering**.
-   Der er angivet påfyldningsrelationer for lagerstedet. Klik på **Lagerstyring &gt;Setup &gt;Lageropdeling &gt;lagre**. Se feltgruppen **Hovedlagersted** under fanen **Overordnet planlægning**.
-   Standardordretypen er indstillet til Produktion, Indkøbsordre eller Kanban. Klik på **administration af produktoplysninger &gt;produkter&gt; frigivne produkter**. Vælg varen, og klik derefter på **Plan &gt;standardindstillinger for ordre**. I formen **Standardindstillinger for ordre** kan du se feltet **Standardordretype**.

![Efterspørgsel efter lokalitetsdisponering, lagersted er ikke obligatorisk](./media/multisitedemandexplosionscenarioforsitecoveragewarehousenotmandatory.jpg)



<a name="see-also"></a>Se også
--------

[Master planning and multisite functionality](master-plan-multisite-functionality.md)

[Overordnet planlægning – lokalitetsdisponering, lagersted er obligatorisk](master-plan-site-coverage-warehouse-mandatory.md)

[Overordnet planlægning – lokations- og lagerdisponering, lagersted er ikke obligatorisk](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Overordnet planlægning – lokations- og lagerdisponering, lagersted er obligatorisk](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Varedisponering - hvordan bestemmes styklisteversionen](master-plan-bom-version-determined.md)

