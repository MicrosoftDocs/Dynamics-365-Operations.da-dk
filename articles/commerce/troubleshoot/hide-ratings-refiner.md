---
title: Bedømmelsesjustering vises på søgeresultater og kategorisider, når bedømmelser og gennemsyn af løsninger ikke er aktiveret
description: Denne artikel indeholder vejledning i fejlfinding af, hvordan du kan skjule vurderingerne i søgeresultater og kategorisider, når Microsoft Dynamics 365 Commerce-vurderinger og gennemsynsløsningen ikke er aktiveret for et e-handelswebsted.
author: gvrmohanreddy
ms.date: 09/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-09-03
ms.dyn365.ops.version: 10.0.22
manager: annbe
ms.openlocfilehash: 28a3cefd6aab81f5e7907bda457763f2306e5a1d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267371"
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
