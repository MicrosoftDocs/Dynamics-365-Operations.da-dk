---
title: Varedisponering for lokations- og lagerdisponering, lagersted er obligatorisk
description: Denne artikel beskriver, hvordan en vare med lokation og lagersted som disponeringsdimensioner bliver planlagt. Lagerstedsdimensionen er obligatorisk.
author: t-benebo
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2554
ms.assetid: 3211e95f-b91a-4d27-8d92-f328ae2bcf12
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: adcb2d41ff70714b6bc9c28f3e23ce95f5292f2e
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740053"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-mandatory"></a>Varedisponering for lokations- og lagerdisponering, lagersted er obligatorisk

[!include [banner](../includes/banner.md)]

Denne artikel beskriver, hvordan en vare med lokation og lagersted som disponeringsdimensioner bliver planlagt. Lagerstedsdimensionen er obligatorisk.

Dette behovsplanlægningsscenario omfatter følgende forhold:

-   Lokationsdimensionen er angivet til obligatorisk og skal angives på behovsposteringen.
-   Dimensionen for lagerstedet er angivet til tvungen og skal angives på behovsposteringen.
-   Dimensionerne for lokation og lagersted er angivet til disponering. Andre dimensioner angives måske også ved behovsplanlægning. Men de påvirkes ikke af funktionen til flere lokationer.

I følgende grafik vises, hvordan varedisponering forløber. De parametre, der henvises til i grafikken, og deres placering er følgende:
-   Lagerstedet er angivet til **Manuel**. Klik på **Lagerstyring &gt; Opsætning &gt; Lageropdeling &gt; Lagersteder**. I **Overordnet planlægning** oversigtspanelet finder du feltet **Manuel**.
-   Der er defineret varedisponering for varen. Klik på **Administration af produktoplysninger &gt; Produkter &gt; Frigivne produkter**. Vælg varen, og derefter skal du i Handlingsrude under fanen **Plan** klikke på **Varedisponering**.
-   Der er angivet påfyldningsrelationer for lagerstedet. Klik på **Lagerstyring &gt; Opsætning &gt; Lageropdeling &gt; Lagersteder**. Se feltgruppen **Hovedlagersted** i oversigtspanelet **Overordnet planlægning**.
-   Standardordretypen er indstillet til Produktion, Indkøbsordre eller Kanban. Klik på **Administration af produktoplysninger &gt; Produkter &gt; Frigivne produkter**. Vælg varen, og derefter skal du i Handlingsrude under fanen **Plan** klikke på **Standardindstillinger for ordre**. I formen **Standardindstillinger for ordre** kan du se **Standardordretype**.

![Efterspørgselslokalitet og lagerdisponering, lagersted er obligatorisk.](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousemandatory.jpg)



## <a name="additional-resources"></a>Yderligere ressourcer

- [Oversigt over varedisponering og funktionen til flere lokationer](master-plan-multisite-functionality.md)
- [Varedisponering for lokalitetsdisponering, obligatorisk lagersted](master-plan-site-coverage-warehouse-mandatory.md)
- [Varedisponering for lokalitetsdisponering, lagersted ikke obligatorisk](master-plan-site-coverage-warehouse-not-mandatory.md)
- [Varedisponering for lokalitets- og lagerdisponering, lagersted ikke obligatorisk](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)
- [Bestemme styklisteversionen](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]