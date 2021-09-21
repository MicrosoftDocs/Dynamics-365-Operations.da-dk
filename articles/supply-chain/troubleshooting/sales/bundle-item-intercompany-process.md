---
title: Bundtvare understøttes ikke i en intern proces
description: Bundtelementet er ikke tilgængeligt for køb. Salgsordren køber kun komponenterne i bundtelementet, ikke selve bundtelementet.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 21adc7d071837b762157364f6f8ed370c69c7fd3
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475906"
---
# <a name="a-bundle-item-isnt-supported-in-an-intercompany-process"></a>En bundtvare understøttes ikke i en intern proces

## <a name="symptoms"></a>Symptomer

Bundtvaren er ikke tilgængelig for indkøbsordren, fordi antallet er *0* (nul) på salgsordrelinjerne for bundtvaren, og status er *Annulleret*.

## <a name="resolution"></a>Løsning

Denne funktionsmåde er tilsigtet. Salgsordren køber kun komponenterne i bundtvaren. Den køber ikke selve bundtvaren. Hvis du skal købe et bundt, skal du overveje, om du vil markere det som en bundtvare, da denne funktionalitet er udviklet til scenarier for indtægtsføring. Yderligere oplysninger om bundtvarer finder du under [Bundter](/dynamics365/finance/accounts-receivable/revenue-recognition-setup).
