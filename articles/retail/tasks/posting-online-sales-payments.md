--- 
title: "Bogføring af onlinesalg og betalinger"
description: "Denne procedure hjælper med at konfigurere og køre et tilbagevendende batchjob for at oprette salgsordrer og betalinger for transaktioner i onlinebutik."
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 13839bbe6ca03f3cfc7036fce87477bf7d5af2a7
ms.contentlocale: da-dk
ms.lasthandoff: 09/14/2018

---
# <a name="posting-of-online-sales-and-payments"></a>Bogføring af onlinesalg og betalinger

[!include[task guide banner](../includes/task-guide-banner.md)]

Denne procedure hjælper med at konfigurere og køre et tilbagevendende batchjob for at oprette salgsordrer og betalinger for transaktioner i onlinebutik. Denne procedure bruger USRT-firmaets demodata.

1. Gå til Alle arbejdsområder > Detailbutiksregnskab.
2. Kik på Synkroniser ordrer.
3. Vælg "Detailbutikker efter område" i feltet Organisationshierarki.
    * Vælg enten en bestemt onlinebutik, eller vælg en node, hvis du vil oprette batchjobbet for en gruppe butikker.  
    * Klik på pilen for at føje dit valg.  
4. Klik på fanen Kør i baggrunden.
5. Markér eller fjern markeringen af afkrydsningsfeltet Batchbehandling.
6. Klik på Gentagelse.
7. Vælg indstillingen Slutdato mangler.
8. Angiv et tal i feltet Antal.
9. Klik på OK.
10. Klik på OK.


