---
title: Funktionskløfter mellem lagerværdi/aldersfordelte rapporter og deres lagerversioner
description: Funktionskløfter mellem lagerværdi/aldersfordelte rapporter og deres lagerversioner
author: AndersGirke
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a72e2d32e755e137cebbc0bf7afb0bed08fb93f2
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475928"
---
# <a name="functional-gaps-between-inventory-valueaging-reports-and-their-storage-versions"></a>Funktionskløfter mellem lagerværdi/aldersfordelte rapporter og deres lagerversioner

Funktionerne [Lagerrapport over aldersfordelt lager](/dynamics365/supply-chain/cost-management/inventory-aging-report-storage.md) og [Lagerrapport over lagerværdi](/dynamics365/supply-chain/cost-management/inventory-value-report-storage.md) giver Supply Chain Management mulighed for at vise store mængder lagertransaktioner. I hvert enkelt tilfælde gemmes rapportresultaterne til gennemsyn og eksport, i modsætning til ikke-lagerversioner af disse rapporter. Men visse funktioner, der findes i ikke-lagerversionerne af disse rapporter, findes ikke i lagerversionerne. I følgende underafsnit opsummeres forskellene, og der angives løsninger.

## <a name="storage-reports-dont-include-subtotals-even-if-they-are-enabled-in-the-report-layout"></a>Lagerrapporter omfatter ikke subtotaler, selvom de er aktiveret i rapportlayoutet

Subtotaler kan give problemer, når resultatet eksporteres, især hvis brugerne ændrer postsekvensen.

Hvis du vil kontrollere subtotalerne, kan du eksportere resultatet til Microsoft Excel. Hvis du vil kontrollere subtotaler i Supply Chain Management, kan du bruge [Funktionsstyring](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at aktivere funktionerne *Nyt gitterkontrolelement* og *Gruppering i gitre*, hvilket giver en meget mere fleksibel måde at se subtotalen for en hvilken som helst gruppe efter kolonne. Du kan finde flere oplysninger under [Gitteregenskaber](/dynamics365/fin-ops-core/fin-ops/get-started/grid-capabilities.md).

## <a name="inventory-value-storage-report-doesnt-support-ledger-account-information"></a>Lagerrapport over lagerværdi understøtter ikke finanskontooplysninger

Du kan køre råbalanceet for at få lagerkontobalancen og sammenligne den med rapporten **Lagerværdi af lager**.
