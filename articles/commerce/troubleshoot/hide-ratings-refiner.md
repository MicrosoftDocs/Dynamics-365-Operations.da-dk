---
title: Vurderingsjustering vises på søgeresultater og artssider, når vurderinger og gennemsyn af løsninger ikke er aktiveret
description: Dette emne indeholder vejledning i fejlfinding af, hvordan du kan skjule vurderingerne i søgeresultater og kategorisider, når Microsoft Dynamics 365 Commerce-vurderinger og gennemsynsløsningen ikke er aktiveret for et e-handelswebsted.
author: gvrmohanreddy
manager: annbe
ms.date: 09/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-09-03
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: ff413e04d7e60da76cd83ecd720c3589b65e93d5
ms.sourcegitcommit: 6dc2b877cf8ea9185a07964ec05c5ddb7a78471b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/12/2022
ms.locfileid: "8407630"
---
# <a name="ratings-refiner-appears-on-search-results-and-category-pages-when-the-ratings-and-reviews-solution-isnt-enabled"></a>Vurderingsjustering vises på søgeresultater og artssider, når vurderinger og gennemsyn af løsninger ikke er aktiveret

[!include [banner](../includes/banner.md)]

Dette emne indeholder vejledning i fejlfinding af, hvordan du kan skjule vurderingerne i søgeresultater og kategorisider, når Microsoft Dynamics 365 Commerce-vurderinger og gennemsynsløsningen ikke er aktiveret for et e-handelswebsted.

## <a name="description"></a>Betegnelse

Vurderingsjustering vises på søgeresultater og kategorisider i en e-handelskanal, der ikke anvender vurderinger og gennemsyn af løsninger.

## <a name="resolution"></a>Løsning

### <a name="enable-the-hide-rating-setting-in-commerce-site-builder"></a>Aktivere indstillingen Skjul rangering i Commerce site builder

Hvis du vil aktivere indstillingen **Skjul rangering** i Commerce Site Builder, så rangeringsjusteringen er skjult på søgeresultater og kategorisider, skal du følge disse trin.

1. Gå til **Webstedsindstillinger \> Udvidelser**.
1. Marker afkrydsningsfeltet **Skjul rangering** under **Rangeringer og vurderinger**.
1. Vælg **Gem og udgiv**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over vurderinger og anmeldelser](../ratings-reviews-overview.md)

[Tilvælge brug af vurderinger og anmeldelser](../opt-in-ratings-reviews.md)
