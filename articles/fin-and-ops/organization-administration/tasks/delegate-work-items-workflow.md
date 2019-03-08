---
title: Delegere workflowopgaver i en arbejdsgang
description: Hvis du planlægger at være væk fra kontoret eller af anden årsag ikke kan udføre workflowopgaver, kan du delegere eller tildele dine workflowopgaver til andre brugere.
author: jasongre
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f85a1318822ceaf829134bf2eb3581e350d5bea4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "346243"
---
# <a name="delegate-work-items-in-a-workflow"></a>Delegere workflowopgaver i en arbejdsgang

[!include [task guide banner](../../includes/task-guide-banner.md)]

Hvis du planlægger at være væk fra kontoret eller af anden årsag ikke kan udføre workflowopgaver, kan du delegere eller tildele dine workflowopgaver til andre brugere. Denne procedure hjælper dig med at konfigurere systemet til automatisk at delegere dine arbejdselementer til en anden bruger.



Det demodatafirma, der bruges til at oprette denne procedure, er USMF.


## <a name="set-up-automatic-delegation"></a>Konfigurere automatisk delegering
1. Gå til Generelt > Opsætning > Brugerindstillinger.
2. Klik på fanen Arbejdsgang.
    * Sørg for, at sektionen Delegering er udvidet.    Hvis du vil konfigurere systemet til automatisk at delegere dine workflowopgaver til andre brugere, skal du oprette delegeringsregler, som angiver, hvornår bestemte workflowopgaver skal uddelegeres. Udfør følgende trin for at oprette en delegeringsregel:  
3. Klik på Tilføj.
4. Vælg en indstilling i feltet Område.
    * Alle – Deleger alle workflowopgaver, der er tildelt dig.    Modul – Deleger kun de arbejdselementer, der er relateret til en bestemt type arbejdsgang. Hvis du vælger denne indstilling, skal du også vælge arbejdsgangens type i feltet Navn.    Arbejdsgang – Deleger kun de arbejdselementer, der er relateret til en bestemt arbejdsgang. Hvis du vælger denne indstilling, skal du vælge arbejdsgangen i feltet Navn.  
5. Vælg den bruger, der skal delegeres arbejdselementer til, i feltet Deleger.
    * Brug felterne Startdato/-tidspunkt og Slutdato/-tidspunkt til at angive, hvornår du ønsker, at arbejdselementerne skal delegeres automatisk.  
6. Angiv en dato og et klokkeslæt i feltet Startdato/-tidspunkt.
7. Angiv en dato og et klokkeslæt i feltet Slutdato/-tidspunkt.
8. Marker afkrydsningsfeltet Aktiveret for at aktivere delegeringsreglen.
    * Hvis du valgte Modul som Område, skal du vælge modulet i feltet Navn.    Hvis du har valgt Arbejdsgang som Område, skal du vælge den specifikke arbejdsgang, der skal delegeres, i feltet Navn.  
9. Skriv en kommentar i feltet Kommentar for at forklare, hvorfor du delegerer arbejdselementer.

