---
title: Varer uden lager kan tjekkes ud
description: Denne artikel indeholder en vejledning i fejlfinding, der kan hjælpe, når kunder kan føje varer, der ikke er på lager, til deres indkøbsvogn og gå videre til kassen.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: 3bc924e44077886b942e19b25a84f0f1d4298c13
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282728"
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
