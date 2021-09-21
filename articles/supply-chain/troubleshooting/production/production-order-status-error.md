---
title: Fejl ved ændring af status for Færdigmeldt til Afsluttet
description: der kan vises en fejl ved ændring af status for produktionsordren fra Færdigmeldt til Afsluttet. Denne side forklarer, hvordan du afhjælper problemet.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 744637f5cccffe44b85f77c1a9df2034012fac40
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475910"
---
# <a name="error-when-changing-status-of-production-order-from-reported-as-finished-to-end"></a>Fejl ved ændring af status for produktionsordren fra Færdigmeldt til Afsluttet

## <a name="symptoms"></a>Symptomer

Når en produktionsordres status ændres fra Færdigmeldt til Afslut, vises en af følgende fejlmeddelelser:

> Opdateringskonflikt. Standardomkostningen stemmer ikke overens med den økonomiske lagerværdi efter opdateringen.

> Der er opstået en alvorlig fejl i funktionen InventCostMovement.checkVariance.

## <a name="cause"></a>Årsag

Dette problem opstår, fordi de underliggende data blev ændret af en anden proces. Processen vil forsøge at opdatere dataene op til fem gange. Hvis konflikten stadig findes efter fem forsøg, får du vist en af ovenfor angivne fejlmeddelelser:

## <a name="resolution"></a>Løsning

Denne funktionsmåde er tilsigtet. Du kan afhjælpe problemet ved at fortsætte batchjobbet. Det skal fuldføre kørslen.

Hvis batchjobbet konstant mislykkes, efter at du har genoptaget det, skal du kontrollere, at afrundingspræcisionen for finansens standardvaluta er kompatibel med den afrunding, der anvendes på værdierne i tabellen InventSum. Hvis afrundingspræcisionen er ændret til en ikke-kompatibel værdi, skal du sandsynligvis ændre den tilbage til en kompatibel værdi. Søg efter **ModifiedDateTime**. I dette tilfælde vil værdien typisk vise, at afrundingspræcisionen er ændret for nylig.
