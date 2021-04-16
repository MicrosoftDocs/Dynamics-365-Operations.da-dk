---
title: Foretage fejlfinding af omkostningsstyring
description: Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med omkostningsstyring.
author: AndersGirke
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails, InventValueProcess, InventValueReportSetup, InventClosing
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: fc6a48a44a529c82c2a9ee818af95569d9bcb249
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834283"
---
# <a name="troubleshoot-cost-management"></a>Foretage fejlfinding af omkostningsstyring

Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med omkostningsstyring.

## <a name="functional-gaps-between-the-inventory-valueaging-reports-and-their-storage-versions"></a>Funktionskløfter mellem lagerværdi/aldersfordelte rapporter og deres lagerversioner

Funktionerne [Lagerrapport over aldersfordelt lager](inventory-aging-report-storage.md) og [Lagerrapport over lagerværdi](inventory-value-report-storage.md) giver Supply Chain Management mulighed for at vise store mængder lagertransaktioner. I hvert enkelt tilfælde gemmes rapportresultaterne til gennemsyn og eksport, i modsætning til ikke-lagerversioner af disse rapporter. Men visse funktioner, der findes i ikke-lagerversionerne af disse rapporter, findes ikke i lagerversionerne. I følgende underafsnit opsummeres forskellene, og der angives løsninger.

### <a name="storage-reports-dont-include-subtotals-even-if-they-are-enabled-in-the-report-layout"></a>Lagerrapporter omfatter ikke subtotaler, selvom de er aktiveret i rapportlayoutet

Subtotaler kan give problemer, når resultatet eksporteres, især hvis brugerne ændrer postsekvensen.

Hvis du vil kontrollere subtotalerne, kan du eksportere resultatet til Microsoft Excel. Hvis du vil kontrollere subtotaler i Supply Chain Management, kan du bruge [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at aktivere funktionerne *Nyt gitterkontrolelement* og *Gruppering i gitre*, hvilket giver en meget mere fleksibel måde at se subtotalen for en hvilken som helst gruppe efter kolonne. Du kan finde flere oplysninger under [Gitteregenskaber](../../fin-ops-core/fin-ops/get-started/grid-capabilities.md).

### <a name="inventory-value-storage-report-doesnt-support-ledger-account-information"></a>Lagerrapport over lagerværdi understøtter ikke finanskontooplysninger

Du kan køre råbalanceet for at få lagerkontobalancen og sammenligne den med rapporten **Lagerværdi af lager**.

## <a name="warnings-or-errors-are-shown-when-changing-a-ledger-period-status-without-closing-inventory"></a>Der vises advarsler eller fejl, når status for en finansperiode ændres, uden at lageret lukkes

Microsoft har indført følgende valideringer for at forhindre problemer, der skyldes en forkert periodeafslutning omkring efterkalkulation. Hvis du støder på en af følgende fejlmeddelelser, kan du se [KB 4561987](https://fix.lcs.dynamics.com/Issue/Details?kb=4561987&bugId=445351&dbType=3&qc=f514f2adcddcddceec43af58c26ae8a9020effdc7cdfe085d9d0deeb8cc7b6a3) for at få flere oplysninger om, hvordan du kan løse problemerne.

- Du er ved at udføre en genberegning med en dato %1 (10-02-2019). Den sidst registrerede genberegning blev udført i en tidligere periode med en dato %2 (20-01-2019). Der er ikke registreret nogen udførelse af lagerlukning med en dato %3 (31-01-2019), der matcher periodeafslutning. Husk at udføre en lagerlukning pr. %3 (31-01-2019), der svarer til periodeafslutningen. Værdiansættelsen af lagerbeholdning, vareforbrug og afvigelser er måske ikke korrekte i reskontro eller finans, før dette er udført.

- Du er ved at ændre statussen for finansperioden %1 til %2. Der er ikke registreret nogen udførelse af lagerlukning med en dato %3, der matcher periodeafslutning. Udfør en lagerlukning pr. %3, der svarer til periodens afslutning, før du ændrer status. Værdiansættelsen af lagerbeholdning, vareforbrug og afvigelser er måske ikke korrekte i reskontro eller finans, før dette er udført. Rapporteret ud fra juridisk enhed %4. I øjeblikket er det kun til oplysning, men i fremtiden du skal udføre sådanne handlinger.

- Kontostrukturen %1 er ændret. En eller flere hovedkonti %2 findes ikke længere. Disse hovedkonti kræves af %3 med en dato %4. Føj disse hovedkonti til kontostrukturen %1, før du kan genoptage %3-jobbet. I øjeblikket er det kun til oplysning, men i fremtiden du skal udføre sådanne handlinger.

- Du er ved at udføre en lagerlukning med datoen %1 (31-01-2019). Der er ikke registreret nogen udførelse af beregning af efterkalkuleret varetræk med datoen %2 (31-01-2019), der matcher periodeafslutning. Husk at udføre beregning af efterkalkuleret varetræk med datoen %3 (31-01-2019), der matcher periodeafslutning. Værdiansættelsen af lagerbeholdning, vareforbrug og afvigelser er måske ikke korrekte i reskontro eller finans, før dette er udført.

- Du er ved at udføre en beregning af efterkalkuleret varetræk med en dato %1 (28-02-2019). Den sidst registrerede beregning af efterkalkuleret varetræk blev udført i en tidligere periode med en dato %2 (31-01-2019). Der er ikke registreret nogen udførelse af lagerlukning med en dato %3 (31-01-2019), der matcher en periodeafslutning.
Husk at udføre en lagerlukning pr. %3 (31-01-2019), der matcher en periodeafslutning. Værdiansættelsen af lagerbeholdning, vareforbrug og afvigelser er måske ikke korrekte i reskontro eller finans, før lagerlukningen er udført.

## <a name="inventory-aging-report-discrepancies"></a>Afvigelser i rapport over aldersfordelt lager

I **Rapporten Aldersfordelt lager** vises forskellige værdier, når du ser dem på forskellige lagerdimensioner (f.eks. lokation eller lagersted). Du kan finde flere oplysninger om rapporteringslogikken i [Eksempler og logik til rapport over aldersfordelt lager](inventory-aging-report.md).

## <a name="an-update-conflict-occurs-when-the-inventory-valuation-method-is-either-standard-cost-or-moving-average"></a>Der opstår en opdateringskonflikt, når lagervurderingsmetoden er Standardomkostning eller Glidende gennemsnit

Når du bogfører dokumenter som lagerkladder, indkøbsordrefakturaer eller salgsordrefakturaer parallelt med hensyn til skalerbarhed og ydeevne, modtager du måske en fejlmeddelelse om en opdateringskonflikt, og nogle af dokumenterne vil muligvis ikke blive bogført. Dette problem kan opstå, når lagervurderingsmetoden er *Standardomkostning* eller *Glidende gennemsnit*. Begge disse metoder er permanente kalkulationsmetoder. Det vil sige, at den endelige omkostning fastsættes på bogføringstidspunktet.

Hvis du bruger metoden *Glidende gennemsnit*, ligner fejlmeddelelsen dette eksempel:

> Lagerværdien xx.xx forventes ikke efter beregningen af den proportionale udgift

Hvis du bruger metoden *Standardomkostning*, ligner fejlmeddelelsen dette eksempel:

> Standardomkostningen stemmer ikke overens med den økonomiske lagerværdi efter opdateringen. Værdi = xx.xx, Antal = yy.yy, Standardomkostning = zz.zz

Indtil Microsoft frigiver en løsning for at løse problemet, kan du overveje at bruge følgende løsningsforslag som en hjælp til at undgå eller reducere disse fejl:

- Bogfør de mislykkede dokumenter igen.
- Opret dokumenter med færre linjer.
- Undgå decimalværdier i standardomkostningen. Prøv at definere standardomkostningen, så feltet **Prisantal** angives til *1*. Hvis du skal angive en værdi for **Prisantal** på mere end *1*, kan du forsøge at minimere antallet af decimaler i standardomkostningen for enheden. (Ideelt set skal der være mindre end to decimaler). Undgå f.eks. at definere standardomkostningsindstillinger som **Pris** = *10* og **Prisantal** = *3*, da de giver en standardomkostning pr. enhed på 3,333333 (hvor decimalværdien gentages).
- I de fleste dokumenter skal du undgå at have flere linjer med samme kombination af produkt- og økonomiske lagerdimensioner.
- Reducer graden af parallelisering. (I dette tilfælde kan systemet blive hurtigere, fordi der opstår færre opdateringskonflikter og forsøg).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]