---
title: Foretage fejlfinding af omkostningsstyring
description: Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med omkostningsstyring.
author: riluan
manager: tfehr
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails, InventValueProcess, InventValueReportSetup, InventClosing
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: e84bb167395c06295b0e8ef8b9fd98aa4bc0cc14
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4425073"
---
# <a name="troubleshoot-cost-management"></a>Foretage fejlfinding af omkostningsstyring

Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med omkostningsstyring.

## <a name="functional-gaps-between-the-inventory-valueaging-reports-and-their-storage-versions"></a>Funktionskløfter mellem lagerværdi/aldersfordelte rapporter og deres lagerversioner

Funktionerne [Lagerrapport over aldersfordelt lager](inventory-aging-report-storage.md) og [Lagerrapport over lagerværdi](inventory-value-report-storage.md) giver Supply Chain Management mulighed for at vise store mængder lagertransaktioner. I hvert enkelt tilfælde gemmes rapportresultaterne til gennemsyn og eksport, i modsætning til ikke-lagerversioner af disse rapporter. Men visse funktioner, der findes i ikke-lagerversionerne af disse rapporter, findes ikke i lagerversionerne. I følgende underafsnit opsummeres forskellene, og der angives løsninger.

### <a name="storage-reports-dont-include-subtotals-even-if-they-are-enabled-in-the-report-layout"></a>Lagerrapporter omfatter ikke subtotaler, selvom de er aktiveret i rapportlayoutet

Subtotaler kan give problemer, når resultatet eksporteres, især hvis brugerne ændrer postsekvensen.

Hvis du vil kontrollere subtotalerne, kan du eksportere resultatet til Microsoft Excel. Hvis du vil kontrollere subtotaler i Supply Chain Management, kan du bruge [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at aktivere funktionerne *Nyt gitterkontrolelement* og *(Prøveversion) gruppering i gitre*, hvilket giver en meget mere fleksibel måde at se subtotalen for en hvilken som helst gruppe efter kolonne. Du kan finde flere oplysninger under [Gitteregenskaber](../../fin-ops-core/fin-ops/get-started/grid-capabilities.md).

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]