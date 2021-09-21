---
title: Dimensionsplaceringen kan ikke være tom, hvis serienummeret er angivet
description: Hvis du modtager denne fejl, når du bekræfter en forsendelse efter oprettelsen af en flytteordre for en serievare, er feltet Standardtilgangslokation tomt.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6f58c72438d5d1d93e59e46525debd65d44d9a76
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475940"
---
# <a name="error-when-confirming-shipment-after-creating-a-transfer-order-for-a-serial-item"></a>Fejl ved bekræftelse af forsendelse efter oprettelse af en flytteordre for en serievare

## <a name="symptoms"></a>Symptomer

Hvis du opretter en flytteordre for en serievare ved hjælp af et lagersted, der er aktiveret til avanceret Warehouse Management (WMS), og du derefter forsøger at bekræfte forsendelsen, efter at arbejdet er fuldført, modtager du følgende fejlmeddelelse.

> Dimensionsplaceringen kan ikke være tom, hvis dimensionens serienummer er angivet.

## <a name="cause"></a>Årsag

Det sker, fordi feltet **Standardmodtagelokation** er tomt for et transitlagersted i "fra"-lagerstedet.

## <a name="resolution"></a>Løsning

Du kan løse dette problem ved at angive en standardtilgangslokation på transitlagerstedet. Kontrollér, at denne lokation er id-styret.
