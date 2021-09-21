---
title: Ikke nok arbejde til klyngen efter konfiguration af profilen
description: Hvis du konfigurerer en klyngeprofil, får du måske vist en fejlmeddelelse om, at der ikke kan findes tilstrækkelig arbejde. Rediger profilen, og angiv positionerne Aktivér til Nej.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 139fd72e571c8ef83af2fd0e497cf334b6ef0ea4
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475870"
---
# <a name="not-enough-work-found-for-cluster-when-using-system-directed-cluster-picking"></a>Der findes ikke nok arbejde til klynger, når der bruges systembaseret klyngepluk

## <a name="symptoms"></a>Symptomer

Når du bruger *Systemstyret klyngepluk* som proces, hvis du konfigurerer en klyngeprofil, hvor der f.eks. kan plukkes 10 placeringer, fungerer processen som planlagt, når der er nok arbejde til at plukke til 10 placeringer. Hvis der kun er otte stillinger, der skal plukkes, vises følgende fejlmeddelelse:

> Der findes ikke arbejde nok til klynge.

## <a name="resolution"></a>Løsning

Du kan løse dette problem ved at redigere klyngeprofilen og angive indstillingen **Aktivér placeringer** til *Nej*.
