---
title: Generere plukarbejde med det samme, når belastning frigives
description: Hvis arbejdet skal genereres med det samme, når lasten frigives, skal du konfigurere bølgeskabelonen i overensstemmelse hermed. Denne side viser dig gennem trinnene.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: fdeb0b27f4d2c1a2cc9f8e0c4ba537cdce604bd2
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475922"
---
# <a name="picking-work-isnt-generated-immediately-when-outbound-load-is-released"></a>Plukarbejde genereres ikke med det samme, når udgående belastning frigives

## <a name="symptoms"></a>Symptomer

Du kan oprette en udgående belastning ved at bruge en salgs- eller flytteordre og frigive belastningen til lagerstedet. Bemærk, at der endnu ikke er genereret noget plukarbejde.

## <a name="resolution"></a>Løsning

Hvis arbejdet skal genereres med det samme, når lasten frigives, skal du konfigurere bølgeskabelonen i overensstemmelse hermed. Angiv følgende indstillinger til *Ja* på bølgeskabelonen:

- Automatiser bølgeoprettelse
- Udfør behandling af bølgen ved frigivelse til lagerstedet
- Automatiser frigivelse af bølge
