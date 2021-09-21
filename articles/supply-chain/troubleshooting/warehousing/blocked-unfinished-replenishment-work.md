---
title: Plukarbejde er spærret på grund af ikke-færdigmeldt genopfyldningsarbejde
description: Pluk af arbejde kan være blokeret på grund af afhængigt genopfyldningsarbejde. Fuldfør genopfyldningsarbejdet, og kør derefter plukarbejdet.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 53b50d1e3e2d7bb64e78514affe80076ddcb9052
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475950"
---
# <a name="picking-work-cant-be-unblocked-because-of-unfinished-replenishment-work"></a>Plukarbejde kan ikke spærres på grund af ikke-færdigmeldt genopfyldningsarbejde

## <a name="symptoms"></a>Symptomer

Når der bruges genopfyldning af efterspørgsel efter efterspørgsel, kan plukarbejde blokeres på grund af afhængigt genopfyldningsarbejde. Systemet opretter både genopfyldningsarbejdet og plukarbejdet, hvis en plukplads skal genopfyldes for at opfylde kildeordrebehovet. Plukarbejdet spærres dog, indtil genopfyldningsarbejdet er fuldført, og du får vist følgende fejlmeddelelse:

> Arbejdet %1 kan ikke få fjernet blokering, fordi det har ikke-afsluttet genopfyldningsarbejde.

## <a name="resolution"></a>Løsning

Denne funktionsmåde er bevidst, fordi plukpladsen ikke har nok lager, medmindre genopfyldningsarbejdet er fuldført. Fuldfør genopfyldningsarbejdet, og kør derefter plukarbejdet.
