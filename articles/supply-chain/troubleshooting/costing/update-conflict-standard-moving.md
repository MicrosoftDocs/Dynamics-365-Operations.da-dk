---
title: Opdatere konflikt, når lagervurderingsmetoden er Standardomkostning eller Glidende gennemsnit
description: Der opstår en opdateringskonflikt, når lagervurderingsmetoden er Standardomkostning eller Glidende gennemsnit
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
ms.openlocfilehash: 920d20d19843ce0cac678c5426c00ec99aa61c61
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475934"
---
# <a name="an-update-conflict-occurs-when-the-inventory-valuation-method-is-either-standard-cost-or-moving-average"></a>Der opstår en opdateringskonflikt, når lagervurderingsmetoden er Standardomkostning eller Glidende gennemsnit

## <a name="symptoms"></a>Symptomer

Når du bogfører dokumenter som lagerkladder, indkøbsordrefakturaer eller salgsordrefakturaer parallelt med hensyn til skalerbarhed og ydeevne, modtager du måske en fejlmeddelelse om en opdateringskonflikt, og nogle af dokumenterne vil muligvis ikke blive bogført. Dette problem kan opstå, når lagervurderingsmetoden er *Standardomkostning* eller *Glidende gennemsnit*. Begge disse metoder er permanente kalkulationsmetoder. Det vil sige, at den endelige omkostning fastsættes på bogføringstidspunktet.

Hvis du bruger metoden *Glidende gennemsnit*, ligner fejlmeddelelsen dette eksempel:

> Lagerværdien xx.xx forventes ikke efter beregningen af den proportionale udgift

Hvis du bruger metoden *Standardomkostning*, ligner fejlmeddelelsen dette eksempel:

> Standardomkostningen stemmer ikke overens med den økonomiske lagerværdi efter opdateringen. Værdi = xx.xx, Antal = yy.yy, Standardomkostning = zz.zz

## <a name="workaround"></a>Løsning

Indtil Microsoft frigiver en løsning for at løse problemet, kan du overveje at bruge følgende løsningsforslag som en hjælp til at undgå eller reducere disse fejl:

- Bogfør de mislykkede dokumenter igen.
- Opret dokumenter med færre linjer.
- Undgå decimalværdier i standardomkostningen. Prøv at definere standardomkostningen, så feltet **Prisantal** angives til *1*. Hvis du skal angive en værdi for **Prisantal** på mere end *1*, kan du forsøge at minimere antallet af decimaler i standardomkostningen for enheden. (Ideelt set skal der være mindre end to decimaler). Undgå f.eks. at definere standardomkostningsindstillinger som **Pris** = *10* og **Prisantal** = *3*, da de giver en standardomkostning pr. enhed på 3,333333 (hvor decimalværdien gentages).
- I de fleste dokumenter skal du undgå at have flere linjer med samme kombination af produkt- og økonomiske lagerdimensioner.
- Reducer graden af parallelisering. (I dette tilfælde kan systemet blive hurtigere, fordi der opstår færre opdateringskonflikter og forsøg).
