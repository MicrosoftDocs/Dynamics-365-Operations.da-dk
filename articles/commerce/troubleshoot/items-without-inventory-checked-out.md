---
title: Varer uden lager kan checkes ud
description: Dette emne indeholder en vejledning i fejlfinding, der kan hjælpe, når kunder kan føje varer, der ikke er på lager, til deres indkøbsvogn og gå videre til kassen.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 6df9c77248c7f4e16765b98327fe5838f0fce7e4
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585247"
---
# <a name="items-without-inventory-can-be-checked-out"></a>Varer uden lager kan checkes ud

[!include [banner](../../includes/banner.md)]

Dette emne indeholder en vejledning i fejlfinding, der kan hjælpe, når kunder kan føje varer, der ikke er på lager, til deres indkøbsvogn og gå videre til kassen.

## <a name="description"></a>Betegnelse

Brugerne kan føje en vare til deres indkøbsvogn, selvom der ikke er nogen lagerbeholdning i butikken, og derefter gå videre til kassen.

## <a name="resolution"></a>Løsning

### <a name="enable-the-show-out-of-stock-errors-property-in-commerce-site-builder"></a>Aktiver egenskaben Vis fejl for lagerfejl i Commerce site builder

Aktiver egenskaben **Vis fejl for lagerfejl** i Commerce site builder ved at følge disse trin.

1. Vælg det sted, du arbejder på.
1. Vælg **Sider** i navigationsruden til venstre.
1. Vælg **CartPage** for at åbne den.
1. Marker afkrydsningsfeltet **Indkøbsvogn 1**, vælg **Rediger**, og marker derefter afkrydsningsfeltet **Vis lagerfejl** i egenskabsruden.
1. Gem og publicer siden.

## <a name="additional-resources"></a>Yderligere ressourcer

[Anvend lagerindstillinger](../inventory-settings.md)

[Beregne lagertilgængelighed for detailkanaler](../calculated-inventory-retail-channels.md)

[Konfigurere lagerbuffere og lagerniveauer](../inventory-buffers-levels.md)
