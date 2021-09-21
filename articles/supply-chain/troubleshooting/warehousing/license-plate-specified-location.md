---
title: Der skal være specificeret id for denne lokation
description: Hvis du modtager denne fejl, når du bekræfter en forsendelse til et WMS-aktiveret lagersted, er feltet Standardmodtagelokation tomt for varer i transit.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 2e562ad2b41dd149f215adc83bd2d54e55dccc05
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475871"
---
# <a name="license-plate-specification-error-when-confirming-shipment-for-a-transfer-order"></a>Fejl i specifikation af id ved bekræftelse af forsendelse for en flytteordre

## <a name="symptoms"></a>Symptomer

Hvis du opretter en flytteordre med et lagersted, der ikke er aktiveret til en avanceret warehouse management (WMS), og du derefter forsøger at bekræfte forsendelsen, efter at arbejdet er fuldført, modtager du evt. følgende fejlmeddelelse.

> Der skal være specificeret id for denne lokation.

## <a name="cause"></a>Årsag

Det sker, fordi feltet **Standardmodtagelokation** er tomt for et transitlagersted i "fra"-lagerstedet.

## <a name="resolution"></a>Løsning

Du kan løse dette problem ved at angive en standardtilgangslokation på transitlagerstedet. Kontrollér, at denne lokation er id-styret.
