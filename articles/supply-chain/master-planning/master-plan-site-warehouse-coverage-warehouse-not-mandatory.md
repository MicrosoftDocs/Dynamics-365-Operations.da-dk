---
title: Varedisponering for lokations- og lagerdisponering, lagersted er ikke obligatorisk
description: Denne artikel beskriver, hvordan en vare med lokation og lagersted som disponeringsdimensioner bliver planlagt. Lagerstedsdimensionen er ikke obligatorisk.
author: t-benebo
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2514
ms.assetid: 92d47bdd-df68-4f60-ac9a-96aa08236c26
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b4989a05f4647ac836b78692da7f63396dbef788
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/03/2022
ms.locfileid: "9741006"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-not-mandatory"></a>Varedisponering for lokations- og lagerdisponering, lagersted er ikke obligatorisk

[!include [banner](../includes/banner.md)]

Denne artikel beskriver, hvordan en vare med lokation og lagersted som disponeringsdimensioner bliver planlagt. Lagerstedsdimensionen er ikke obligatorisk.

Dette behovsplanlægningsscenario omfatter følgende forhold:

-   Lokationsdimensionen er angivet til obligatorisk og skal angives på behovsposteringen. Denne indstilling kan ikke redigeres.
-   Lagerstedsdimensionen er ikke angivet til obligatorisk. Lagerstedet er måske kendt, men bruges ikke i beregningen i varedisponeringen.
-   Lokations- og lagerstedsdimensioner angives ved behovsplanlægning. Andre dimensioner angives måske også ved behovsplanlægning. Men de påvirkes ikke af funktionen til flere lokationer.

I følgende grafik vises, hvordan varedisponering forløber. De parametre, der henvises til i grafikken, og deres placering er følgende:
-   Lagerstedet er angivet til Manuel. Klik på **Lagerstyring &gt; Opsætning &gt; Lageropdeling &gt; Lagersteder**. I **Overordnet planlægning** oversigtspanelet finder du feltet **Manuel**.
-   Der er defineret varedisponering for varen. Klik på **Administration af produktoplysninger &gt; Produkter &gt; Frigivne produkter**. Vælg varen, og derefter skal du i Handlingsrude under fanen **Plan** klikke på **Varedisponering**.
-   Der er angivet påfyldningsrelationer for lagerstedet. Klik på **Lagerstyring &gt; Opsætning &gt; Lageropdeling &gt; Lagersteder**. Se feltgruppen **Hovedlagersted** i oversigtspanelet **Overordnet planlægning**.
-   Standardordretypen er indstillet til Produktion, Indkøbsordre eller Kanban. Klik på **Administration af produktoplysninger &gt; Produkter &gt; Frigivne produkter**. Vælg varen, og derefter skal du i Handlingsrude under fanen **Plan** klikke på **Standardindstillinger for ordre**. I formen **Standardindstillinger for ordre** kan du se **Standardordretype**.

![Efterspørgsel efter lokalitet og lagersted, lagersted er ikke obligatorisk.](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousenotmandatory.jpg)



## <a name="additional-resources"></a>Yderligere ressourcer

- [Oversigt over varedisponering og funktionen til flere lokationer](master-plan-multisite-functionality.md)
- [Varedisponering for lokalitetsdisponering, obligatorisk lagersted](master-plan-site-warehouse-coverage-warehouse-mandatory.md)
- [Varedisponering for lokalitets- og lagerdisponering, obligatorisk lagersted](master-plan-site-coverage-warehouse-mandatory.md)
- [Varedisponering for lokalitets- og lagerdisponering, lagersted ikke obligatorisk](master-plan-site-coverage-warehouse-not-mandatory.md)
- [Bestemme styklisteversionen](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]