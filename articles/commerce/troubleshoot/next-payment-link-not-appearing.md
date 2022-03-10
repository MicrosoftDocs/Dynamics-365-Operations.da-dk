---
title: Gem til min næste betalingsindstilling vises ikke
description: Dette emne indeholder vejledning i fejlfinding, der kan hjælpe, når afkrydsningsfeltet Gem til min næste betaling ikke vises under Betalingsmetode på e-handelswebstedet ved kassen.
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
ms.openlocfilehash: 4887cde3e4243ae7a4da6402782e69e780ae20331ed80df63ba1239ef5187e41
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6769265"
---
# <a name="save-for-my-next-payment-option-doesnt-appear"></a>Indstillingen "Gem til min næste betaling" vises ikke

[!include [banner](../../includes/banner.md)]

Dette emne indeholder vejledning i fejlfinding, der kan hjælpe, når afkrydsningsfeltet **Gem til min næste betaling** ikke vises under **Betalingsmetode** på e-handelswebstedet ved kassen.

## <a name="description"></a>Betegnelse

Afkrydsningsfeltet **Gem til min næste betaling** vises ikke i afsnittet **Betalingsmåde** på e-handelswebstedet ved kassen.

I følgende illustration vises et eksempel på en side til betaling ved kassen, hvor afkrydsningsfeltet **Gem til min næste betaling** vises.

![Afkrydsningsfeltet Gem til min næste betaling i betalingsmodulet.](media/payment-module-save-payment.jpg)

## <a name="resolution"></a>Løsning

### <a name="verify-that-the-dynamics-365-payment-connector-for-adyen-is-correctly-configured-in-commerce-headquarters"></a>Kontroller, at Dynamics 365 Payment Connector til Adyen er konfigureret korrekt i Commerce Headquarters

Følg disse trin for at kontrollere, at Dynamics 365 Payment Connector til Anøgle er konfigureret korrekt i Commerce Headquarters

1. Gå til **Retail og Commerce \> Kanaler \> Onlinebutikker**.
1. Vælg onlinebutikken.
1. I oversigtspanelet **Betalingskonti** skal du sørge for, at betalingsoplysningerne i feltet **Tillad lagring af betalingsoplysninger under e-handel** er angivet til **Sand**.

![Tillad lagring af betalingsoplysninger i feltet for e-handel i Commerce Headquarters.](media/payment-connector-save-payment.jpg)

## <a name="additional-resources"></a>Yderligere ressourcer

[Betalingsmodul](../payment-module.md)

[Gemme onlinebetalingsmidler med Adyen-connector](../dev-itpro/adyen-connector-listPI.md)
