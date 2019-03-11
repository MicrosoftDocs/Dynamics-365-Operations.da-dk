---
title: Konfigurer og kør jobbet for at beregne opgørelser
description: Denne procedure hjælper med at konfigurere og køre tilbagevendende batchjob for at oprette og beregne opgørelser for en valgt butik eller butiksgruppe.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f52603672e95d0ae4973844851c4ed260484e5f0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "365172"
---
# <a name="configure-and-run-job-to-calculate-statements"></a>Konfigurer og kør jobbet for at beregne opgørelser

[!include[task guide banner](../includes/task-guide-banner.md)]

Denne procedure hjælper med at konfigurere og køre tilbagevendende batchjob for at oprette og beregne opgørelser for en valgt butik eller butiksgruppe. Denne procedure bruger USRT-firmaets demodata.

1. Gå til Alle arbejdsområder > Detailbutiksregnskab.
2. Klik på Beregn opgørelser.
    * Vælg enten en bestemt butik eller en node, hvis du vil oprette batchjobbet for en gruppe butikker.  
    * Klik på pilen for at føje dit valg.  
3. Klik på fanen Kør i baggrunden.
4. Vælg "Ja" under batchbehandling.
5. Klik på Gentagelse.
6. Angiv en dato i feltet Startdato.
7. Angiv et tidspunkt i feltet Starttidspunkt.
8. Vælg indstillingen Slutdato mangler.
9. Angiv "Dage" i feltet PatternUnit.
10. Angiv et tal i feltet Pr.
11. Klik på OK.
12. Klik på OK.

