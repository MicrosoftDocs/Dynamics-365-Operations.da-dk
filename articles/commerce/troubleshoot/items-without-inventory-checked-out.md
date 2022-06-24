---
title: Varer uden lager kan tjekkes ud
description: Denne artikel indeholder en vejledning i fejlfinding, der kan hjælpe, når kunder kan føje varer, der ikke er på lager, til deres indkøbsvogn og gå videre til kassen.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
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
ms.openlocfilehash: 24400953d2a17384be8ab3000aa829bf2bcb7192
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877179"
---
# <a name="items-without-inventory-can-be-checked-out"></a>Varer uden lager kan tjekkes ud

[!include [banner](../../includes/banner.md)]

Denne artikel indeholder en vejledning i fejlfinding, der kan hjælpe, når kunder kan føje varer, der ikke er på lager, til deres indkøbsvogn og gå videre til kassen.

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
