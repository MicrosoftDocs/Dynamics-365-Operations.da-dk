---
title: Varedisponering for lokalitetsdisponering, obligatorisk lagersted
description: Denne artikel beskriver, hvordan en vare med lokationen som disponeringsdimension bliver planlagt. Lagerstedet er en obligatorisk dimension.
author: t-benebo
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2454
ms.assetid: aa135030-f98c-48bf-902c-e52f680dc247
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df58017c25737cc946d09bf86ff7ad8bd33f4176
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/03/2022
ms.locfileid: "9741034"
---
# <a name="master-planning-for-site-coverage-mandatory-warehouse"></a>Varedisponering for lokalitetsdisponering, obligatorisk lagersted

[!include [banner](../includes/banner.md)]

Denne artikel beskriver, hvordan en vare med lokationen som disponeringsdimension bliver planlagt. Lagerstedet er en obligatorisk dimension.

Dette behovsplanlægningsscenario omfatter følgende forhold:

-   Lokationsdimensionen er angivet til obligatorisk og skal angives på behovsposteringen. Denne indstilling kan ikke redigeres.
-   Dimensionen for lagerstedet er angivet til tvungen og skal angives på behovsposteringen.
-   Dimensionen for lokationen er angivet til disponering. Der kan også angives andre dimensioner for disponering. De påvirkes dog ikke af funktionen til brug af flere lokationer.
-   Dimensionen for lagerstedet er ikke angivet til disponering. Udbud og efterspørgsel aggregeres derfor efter lokation og måske også andre disponerede dimensioner.

I følgende grafik vises, hvordan varedisponering forløber. De parametre, der henvises til i grafikken, og deres placering er følgende:
-   Der er defineret varedisponering for varen. Klik på **Administration af produktoplysninger &gt; Produkter &gt; Frigivne produkter**. Vælg varen, og klik derefter på **Plan &gt; Varedisponering**.
-   Der er angivet påfyldningsrelationer for lagerstedet. Klik på **Lagerstyring &gt; Opsætning &gt; Lageropdeling &gt; Lagersteder**. Se feltgruppen **Hovedlagersted** under fanen **Overordnet planlægning**.
-   Standardordretypen er indstillet til Produktion, Indkøbsordre eller Kanban. Klik på **Administration af produktoplysninger &gt; Produkter &gt; Frigivne produkter**. Vælg varen, og klik derefter på **Plan &gt; Standardindstillinger for ordre**. I formen **Standardindstillinger for ordre** kan du se **Standardordretype**.

![Efterspørgsel efter lokalitetsdisponering, lagersted obligatorisk.](./media/multisitedemandexplosionscenarioforsitecoveragewarehousemandatory.jpg)



## <a name="additional-resources"></a>Yderligere ressourcer

- [Oversigt over varedisponering og funktionen til flere lokationer](master-plan-multisite-functionality.md)
- [Varedisponering for lokalitets- og lagerdisponering, obligatorisk lagersted](master-plan-site-warehouse-coverage-warehouse-mandatory.md)
- [Varedisponering for lokalitetsdisponering, obligatorisk lagersted](master-plan-site-coverage-warehouse-mandatory.md)
- [Varedisponering for lokalitets- og lagerdisponering, lagersted ikke obligatorisk](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)
- [Bestemme styklisteversionen](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]