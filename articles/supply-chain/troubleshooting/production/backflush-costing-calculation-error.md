---
title: Fejl i beregning af varebeholdning ved lagerlukning
description: I tidligere versioner kan du have modtaget fejl i efterkalkulering af varelager under lagerlukning. Dette er blevet løst.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ae92b7121998d6b1ba2f08ea5736c55637867fbf
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475889"
---
# <a name="backflush-costing-calculation-error-during-inventory-closing"></a>Fejl i beregning af varebeholdning ved lagerlukning

## <a name="symptoms"></a>Symptomer

Hvis du i versioner før 10.0.13 ikke bruger omkostningsforløbet for lean produktionsflow, får du vist følgende fejlmeddelelse under lagerlukningen:

> Du er ved at udføre en lagerlukning med datoen %1. Der er ikke registreret nogen udførelse af beregning af efterkalkuleret varetræk med datoen %1 der matcher periodeafslutning. Husk at udføre beregning af efterkalkuleret varetræk med datoen %1 der matcher periodeafslutning. Værdiansættelsen af lagerbeholdning, vareforbrug og afvigelser er måske ikke korrekte i Reskontro eller Finans, før dette er udført.

## <a name="resolution"></a>Løsning

Dette problem er løst i version 10.0.13 og senere. Du kan finde flere oplysninger i [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).
