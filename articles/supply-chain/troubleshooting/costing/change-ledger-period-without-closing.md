---
title: Advarsler eller fejl ved ændring af finansperiodestatus uden lukning af lageret
description: Advarsler eller fejl ved ændring af finansperiodestatus uden lukning af lageret
author: AndersGirke
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails, InventValueProcess, InventValueReportSetup, InventClosing
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 05851753e29da75f014d2cc77e2b8df259620eee
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475890"
---
# <a name="warnings-or-errors-on-changing-ledger-period-status-without-closing-inventory"></a>Advarsler eller fejl ved ændring af finansperiodestatus uden lukning af lageret

Microsoft har indført følgende valideringer for at forhindre problemer, der skyldes en forkert periodeafslutning omkring efterkalkulation. Hvis du støder på en af følgende fejlmeddelelser, kan du se [KB 4561987](https://fix.lcs.dynamics.com/Issue/Details?kb=4561987&bugId=445351&dbType=3&qc=f514f2adcddcddceec43af58c26ae8a9020effdc7cdfe085d9d0deeb8cc7b6a3) for at få flere oplysninger om, hvordan du kan løse problemerne.

- Du er ved at udføre en genberegning med en dato %1 (10-02-2019). Den sidst registrerede genberegning blev udført i en tidligere periode med en dato %2 (20-01-2019). Der er ikke registreret nogen udførelse af lagerlukning med en dato %3 (31-01-2019), der matcher periodeafslutning. Husk at udføre en lagerlukning pr. %3 (31-01-2019), der svarer til periodeafslutningen. Værdiansættelsen af lagerbeholdning, vareforbrug og afvigelser er måske ikke korrekte i reskontro eller finans, før dette er udført.

- Du er ved at ændre statussen for finansperioden %1 til %2. Der er ikke registreret nogen udførelse af lagerlukning med en dato %3, der matcher periodeafslutning. Udfør en lagerlukning pr. %3, der svarer til periodens afslutning, før du ændrer status. Værdiansættelsen af lagerbeholdning, vareforbrug og afvigelser er måske ikke korrekte i reskontro eller finans, før dette er udført. Rapporteret ud fra juridisk enhed %4. I øjeblikket er det kun til oplysning, men i fremtiden du skal udføre sådanne handlinger.

- Kontostrukturen %1 er ændret. En eller flere hovedkonti %2 findes ikke længere. Disse hovedkonti kræves af %3 med en dato %4. Føj disse hovedkonti til kontostrukturen %1, før du kan genoptage %3-jobbet. I øjeblikket er det kun til oplysning, men i fremtiden du skal udføre sådanne handlinger.

- Du er ved at udføre en lagerlukning med datoen %1 (31-01-2019). Der er ikke registreret nogen udførelse af beregning af efterkalkuleret varetræk med datoen %2 (31-01-2019), der matcher periodeafslutning. Husk at udføre beregning af efterkalkuleret varetræk med datoen %3 (31-01-2019), der matcher periodeafslutning. Værdiansættelsen af lagerbeholdning, vareforbrug og afvigelser er måske ikke korrekte i reskontro eller finans, før dette er udført.

- Du er ved at udføre en beregning af efterkalkuleret varetræk med en dato %1 (28-02-2019). Den sidst registrerede beregning af efterkalkuleret varetræk blev udført i en tidligere periode med en dato %2 (31-01-2019). Der er ikke registreret nogen udførelse af lagerlukning med en dato %3 (31-01-2019), der matcher en periodeafslutning.

Husk at udføre en lagerlukning pr. %3 (31-01-2019), der matcher en periodeafslutning. Værdiansættelsen af lagerbeholdning, vareforbrug og afvigelser er måske ikke korrekte i reskontro eller finans, før lagerlukningen er udført.