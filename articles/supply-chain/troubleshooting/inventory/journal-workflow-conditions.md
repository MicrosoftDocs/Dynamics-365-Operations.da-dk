---
title: Der gælder arbejdsgangsbetingelser for lagerkladder på kladdeniveau, ikke på linjeniveau
description: Betingelserne for arbejdsgange for lagerkladder gælder kun på kladdeniveau, ikke på linjeniveau.
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 46bdde7f09c639fbefd46162431762b056d521ae
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475903"
---
# <a name="inventory-journal-workflow-conditions-apply-at-the-journal-level-not-line-level"></a>Der gælder arbejdsgangsbetingelser for lagerkladder på kladdeniveau, ikke på linjeniveau

## <a name="symptoms"></a>Symptomer

Du kan opleve denne fejl, hvis du f.eks. prøver at konfigurere en betingelse for arbejdsgange for lagerkladder for kostbeløbet. Du konfigurerer betingelsen, så trin 1 kun køres, når kostbeløbet er mindre end 100. Du konfigurerer derefter en anden betingelse, så trin 2 kun køres, når kostbeløbet er mere end eller lig med 100. Når arbejdsgangen derefter køres, vises der kun én linje i arbejdsgangshistorikken, og den første betingelse evalueres altid som *sand*, uanset hvilken værdi der sendes.

## <a name="workaround"></a>Løsning

I den aktuelle version gælder betingelserne for arbejdsgange for lagerkladder kun på kladdeniveau, ikke på linjeniveau. Denne funktionsmåde er tilsigtet. Det anbefales, at du kun angiver betingelseskriterierne for attributter på kladdeniveau.
