---
title: Varedisponering for lokations- og lagerdisponering, lagersted er obligatorisk
description: I dette emne beskrives det, hvordan en vare med lokation og lagersted som disponeringsdimensioner bliver planlagt. Lagerstedsdimensionen er obligatorisk.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2554
ms.assetid: 3211e95f-b91a-4d27-8d92-f328ae2bcf12
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: bc4b54b25edf0f1a47839e8a8253db5a8c595a8f
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-mandatory"></a>Varedisponering for lokations- og lagerdisponering, lagersted er obligatorisk

[!include[banner](../includes/banner.md)]


I dette emne beskrives det, hvordan en vare med lokation og lagersted som disponeringsdimensioner bliver planlagt. Lagerstedsdimensionen er obligatorisk.

Dette behovsplanlægningsscenario omfatter følgende forhold:

-   Lokationsdimensionen er angivet til obligatorisk og skal angives på behovsposteringen.
-   Dimensionen for lagerstedet er angivet til tvungen og skal angives på behovsposteringen.
-   Dimensionerne for lokation og lagersted er angivet til disponering. Andre dimensioner angives måske også ved behovsplanlægning. Men de påvirkes ikke af funktionen til flere lokationer.

I følgende grafik vises, hvordan varedisponering forløber. De parametre, der henvises til i grafikken, og deres placering er følgende:
-   Lagerstedet er angivet til **Manuel**. Klik på **Lagerstyring &gt; Opsætning &gt; Lageropdeling &gt; Lagersteder**. I **Overordnet planlægning** oversigtspanelet finder du feltet **Manuel**.
-   Der er defineret varedisponering for varen. Klik på **Administration af produktoplysninger &gt; Produkter &gt; Frigivne produkter**. Vælg varen, og derefter skal du i Handlingsrude under fanen **Plan** klikke på **Varedisponering**.
-   Der er angivet påfyldningsrelationer for lagerstedet. Klik på **Lagerstyring &gt; Opsætning &gt; Lageropdeling &gt; Lagersteder**. Se feltgruppen **Hovedlagersted** i oversigtspanelet **Overordnet planlægning**.
-   Standardordretypen er indstillet til Produktion, Indkøbsordre eller Kanban. Klik på **Administration af produktoplysninger &gt; Produkter &gt; Frigivne produkter**. Vælg varen, og derefter skal du i Handlingsrude under fanen **Plan** klikke på **Standardindstillinger for ordre**. I formen **Standardindstillinger for ordre** kan du se **Standardordretype**.

![Efterspørgselslokalitet og lagerdisponering, lagersted er obligatorisk](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousemandatory.jpg)



<a name="see-also"></a>Se også
--------

[Varedisponering og funktionen til flere lokationer](master-plan-multisite-functionality.md)

[Overordnet planlægning – lokalitetsdisponering, lagersted er obligatorisk](master-plan-site-coverage-warehouse-mandatory.md)

[Overordnet planlægning – lokalitetsdisponering, lagersted er ikke obligatorisk](master-plan-site-coverage-warehouse-not-mandatory.md)

[Overordnet planlægning – lokations- og lagerdisponering, lagersted er ikke obligatorisk](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Overordnet planlægning – sådan bestemmes styklisteversionen](master-plan-bom-version-determined.md)




