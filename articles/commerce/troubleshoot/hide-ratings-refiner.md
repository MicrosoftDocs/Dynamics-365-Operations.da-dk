---
title: Bedømmelsesjustering vises på søgeresultater og kategorisider, når bedømmelser og gennemsyn af løsninger ikke er aktiveret
description: Denne artikel indeholder vejledning i fejlfinding af, hvordan du kan skjule vurderingerne i søgeresultater og kategorisider, når Microsoft Dynamics 365 Commerce-vurderinger og gennemsynsløsningen ikke er aktiveret for et e-handelswebsted.
author: gvrmohanreddy
manager: annbe
ms.date: 09/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-09-03
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: c35e176fc5673de194a81a3a4694a83f7bc9aa00
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885052"
---
# <a name="ratings-refiner-appears-on-search-results-and-category-pages-when-the-ratings-and-reviews-solution-isnt-enabled"></a>Bedømmelsesjustering vises på søgeresultater og kategorisider, når bedømmelser og gennemsyn af løsninger ikke er aktiveret

[!include [banner](../includes/banner.md)]

Denne artikel indeholder vejledning i fejlfinding af, hvordan du kan skjule vurderingerne i søgeresultater og kategorisider, når Microsoft Dynamics 365 Commerce-vurderinger og gennemsynsløsningen ikke er aktiveret for et e-handelswebsted.

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
