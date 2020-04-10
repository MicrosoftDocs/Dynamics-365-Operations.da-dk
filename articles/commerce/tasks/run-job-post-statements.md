---
title: Konfigurer og kør jobbet for at bogføre opgørelser
description: Denne procedure hjælper med at konfigurere og køre et tilbagevendende batchjob for at bogføre opgørelser for en valgt butik eller butiksgruppe.
author: josaw1
manager: AnnBe
ms.date: 07/29/2019
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
ms.openlocfilehash: f89203850b302b769b22920fa5c42d2b0b877684
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141171"
---
# <a name="configure-and-run-job-to-post-statements"></a>Konfigurer og kør jobbet for at bogføre opgørelser

[!include [banner](../includes/banner.md)]

Denne procedure hjælper med at konfigurere og køre et tilbagevendende batchjob for at bogføre opgørelser for en valgt butik eller butiksgruppe. Denne procedure bruger USRT-firmaets demodata.

1. Gå til Alle arbejdsområder > .. > Butiksregnskab.
2. Klik på Bogfør opgørelse i batch.
    * Vælg et organisationshierarki, og vælg derefter enten en enkelt butik eller en node i organisationens nodetræ. Vælg en node, hvis du vil oprette batchjobbet for en gruppe butikker.  
    * Klik på pilen for at føje dit valg.  
3. Klik på fanen Kør i baggrunden. ![Kør i baggrunden](../dev-itpro/media/runbackground.png "Kør i baggrunden") 
4. Markér eller fjern markeringen af afkrydsningsfeltet Batchbehandling.
![Batchbehandling](../dev-itpro/media/batchprocessing.png "Batchbehandling og gentagelse") 
5. Klik på Gentagelse.
6. Angiv en dato i feltet Startdato.
7. Angiv et tidspunkt i feltet Starttidspunkt.
    * Vælg, om du vil afslutte gentagelsen efter et bestemt antal kørsler, på en bestemt dato eller aldrig. Derefter skal du vælge forskellige indstillinger for at definere, hvor ofte jobbet skal køre.  
8. Klik på OK.
9. Klik på OK.

