---
title: Systemet kan ikke finde et ordreforslag under operationer på flere ordrer
description: Fejlen "Ordreforslag findes ikke" opstår, når du udfører operationer på flere ordreforslag, og mindst to ordrer tilhører samme vare-id.
author: t-benebo
ms.date: 12/07/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo_ReqTransPoMarkChangeType
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-12-07
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 0ece4a331b63b86e896c5b337a58185ed3ea1049
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920795"
---
# <a name="the-system-cant-find-a-planned-order-during-operations-on-multiple-orders"></a>Systemet kan ikke finde et ordreforslag under operationer på flere ordrer

Fejlkode: SYS24774

## <a name="symptoms"></a>Symptomer

Du får vist følgende fejlmeddelelse, når du forsøger at udføre en operation på flere ordreforslag samtidig, og mindst to af ordrerne tilhører samme vare-id. Fejlen kan f.eks. opstå, når ordrerne er autoriserede, eller deres ordretype er ændret.

> Ordreforslag %1 findes ikke.

## <a name="cause"></a>Årsag

Når systemet autoriserer eller ændrer en ordretype, skal det tage højde for eksisterende ordreforslag for varen for at sikre, at den planlagte forsyning opfylder efterspørgslen og den eksisterende forsyning. Som en del af denne proces genopretter systemet ordreforslag til varen. Det andet ordreforslag, som systemet forventer at behandle, findes derfor ikke længere.

## <a name="workaround"></a>Løsning

Godkend ordrerne, før du behandler dem. På denne måde slettes ordrerne ikke, når systemet behandler den første ordre på varen.
