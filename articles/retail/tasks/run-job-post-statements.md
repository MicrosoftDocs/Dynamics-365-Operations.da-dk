---
title: Konfigurer og kør jobbet for at bogføre opgørelser
description: Denne procedure hjælper med at konfigurere og køre et tilbagevendende batchjob for at bogføre opgørelser for en valgt butik eller butiksgruppe.
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
ms.openlocfilehash: 676216d90c50c0d3fa1a839cab7a734e624708ba
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "346289"
---
# <a name="configure-and-run-job-to-post-statements"></a>Konfigurer og kør jobbet for at bogføre opgørelser

[!include[task guide banner](../includes/task-guide-banner.md)]

Denne procedure hjælper med at konfigurere og køre et tilbagevendende batchjob for at bogføre opgørelser for en valgt butik eller butiksgruppe. Denne procedure bruger USRT-firmaets demodata.

1. Gå til Alle arbejdsområder > .. > Detailbutiksregnskab.
2. Klik på Bogfør opgørelser.
    * Vælg et organisationshierarki, og vælg derefter enten en enkelt butik eller en node i organisationens nodetræ. Vælg en node, hvis du vil oprette batchjobbet for en gruppe butikker.  
    * Klik på pilen for at føje dit valg.  
3. Klik på fanen Kør i baggrunden.
4. Markér eller fjern markeringen af afkrydsningsfeltet Batchbehandling.
5. Klik på Gentagelse.
6. Angiv en dato i feltet Startdato.
7. Angiv et tidspunkt i feltet Starttidspunkt.
    * Vælg, om du vil afslutte gentagelsen efter et bestemt antal kørsler, på en bestemt dato eller aldrig. Derefter skal du vælge forskellige indstillinger for at definere, hvor ofte jobbet skal køre.  
8. Klik på OK.
9. Klik på OK.

