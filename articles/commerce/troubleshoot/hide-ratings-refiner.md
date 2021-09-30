---
title: Vurderingsjustering vises på søgeresultater og artssider, når vurderinger og gennemsyn af løsninger ikke er aktiveret
description: Dette emne indeholder vejledning i fejlfinding af, hvordan du kan skjule vurderingerne i søgeresultater og kategorisider, når Microsoft Dynamics 365 Commerce-vurderinger og gennemsynsløsningen ikke er aktiveret for et e-handelswebsted.
author: gvrmohanreddy
manager: annbe
ms.date: 09/02/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-09-03
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: f3438d12f4ffd06b07cbef724cda8fa490a5f4eb
ms.sourcegitcommit: d420b96d37093c26f0e99c548f036eb49a15ec30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/03/2021
ms.locfileid: "7472587"
---
# <a name="ratings-refiner-appears-on-search-results-and-category-pages-when-the-ratings-and-reviews-solution-isnt-enabled"></a>Vurderingsjustering vises på søgeresultater og artssider, når vurderinger og gennemsyn af løsninger ikke er aktiveret

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

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