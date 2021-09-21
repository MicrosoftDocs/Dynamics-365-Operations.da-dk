---
title: Direkte levering, der ikke kan behandles på lagerstedet, der er aktiveret til WMS
description: Hvis lagerstedet har WMS aktiveret, understøtter det ikke direkte levering. Hvis du derfor vil bruge direkte levering, skal du vælge en ikke-WMS-vare og et lagersted.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 090e17091e9fb92c2065679bb9b04637214e2eea
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475956"
---
# <a name="direct-delivery-not-able-to-process-for-wms-enabled-warehouse"></a>Direkte levering, der ikke kan behandles på lagerstedet, der er aktiveret til WMS

## <a name="symptoms"></a>Symptomer

Hvis en vare føjes til en salgslinje for direkte levering fra et lagersted, der er aktiveret til Warehouse Management (WMS), modtager du følgende fejlmeddelelse, når salgslinjen opdateres:

> Direkte levering kan ikke behandles for lagersted 1%, da Warehouse Management er aktiveret. Angiv et andet lagersted, der ikke er aktiveret til warehouse management.

## <a name="resolution"></a>Løsning

Microsoft har evalueret dette problem og har fastslået, at det er en funktionsbegrænsning. I øjeblikket understøtter WMS ikke direkte levering. Hvis du derfor vil bruge direkte levering, skal du vælge en ikke-WMS-vare og et lagersted.
