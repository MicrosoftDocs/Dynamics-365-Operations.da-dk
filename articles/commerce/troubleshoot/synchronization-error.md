---
title: Fejl ved ordresynkronisering i forbindelse med standardbetalingstjeneste
description: Denne artikel indeholder en vejledning i fejlfinding, der kan hjælpe med at rette en fejl, der kan opstå, når en onlineordre synkroniseres.
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
ms.openlocfilehash: aa57366fb8f351a8275c947220de78fe809b7b5a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276683"
---
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a>Fejl ved ordresynkronisering i forbindelse med standardbetalingstjeneste

[!include [banner](../../includes/banner.md)]

Denne artikel indeholder en vejledning i fejlfinding, der kan hjælpe med at rette en fejl, der kan opstå, når en onlineordre synkroniseres.

## <a name="description"></a>Betegnelse

Når du synkroniserer en onlineordre, modtager du følgende fejlmeddelelse: "Der skal være en standardbetalingstjeneste til behandling af kreditkorttransaktioner".

![Manglende fejl i standardbetalingstjenesten.](media/default-payment-method-error.jpg)

## <a name="resolution"></a>Løsning

### <a name="confirm-or-set-the-default-payment-service-in-commerce-headquarters"></a>Bekræft eller angiv standardbetalingstjenesten i Commerce Headquarters

Følg disse trin for at bekræfte eller angive standardbetalingstjenesten i Commerce Headquarters.

1. Gå til **Debitor \> Betalingsopsætning \> Betalingstjenester**.
1. Sørg for, at indstillingen **Standardprocessoren for den nye kreditkort** er angivet til **Ja** for én betalingstjeneste.

## <a name="additional-resources"></a>Yderligere ressourcer

[Opsætning, godkendelse og verifikation af kreditkort](../../finance/accounts-receivable/credit-card-authorizations.md)
