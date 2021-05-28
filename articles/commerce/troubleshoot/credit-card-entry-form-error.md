---
title: Siden kreditkortindtastning viser en fejl ved kassen
description: Dette emne indeholder en vejledning i fejlfinding, der kan hjælpe dig med, når afsnittet Betalingsmetode ikke indlæses, og viser en fejlmeddelelse.
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
ms.openlocfilehash: ea9105481e6c5812565f0d3604906c905bcb5443
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018500"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a>Siden kreditkortindtastning viser en fejl ved kassen

[!include [banner](../../includes/banner.md)]

Dette emne indeholder en vejledning i fejlfinding, der kan hjælpe dig med, når afsnittet **Betalingsmetode** ikke indlæses, og viser en fejlmeddelelse.

## <a name="description"></a>Betegnelse

Når du åbner siden til betaling ved kassen i en onlinebutik, er sektionen **Betalingsmetode** ikke indlæst, og følgende fejlmeddelelse vises: "Noget gik galt. Prøv igen senere."

![Betalingsmodulfejl](media/payment-module-error.jpg)

## <a name="resolution"></a>Løsning

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a>Vent, indtil commerce Scale Unit-cachen udløber

Betalingstjenestens indstillinger på betalingstjenestesiden ved kassen i onlinebutikken cachelagres på Commerce Scale Unit og kan tage op til 15 minutter, før de vises på e-handelswebstedet. Disse indstillinger for betalingstjeneste omfatter ændringer af forhandlerkonto-id, API-nøgle i skyen og forskellige konfigurationsindstillinger, der er relateret til betalingsmåden.

## <a name="additional-resources"></a>Yderligere ressourcer

[Konfigurere en onlinekanal](../channel-setup-online.md)
