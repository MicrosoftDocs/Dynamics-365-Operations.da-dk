--- 
title: "Oprette en underleverandørarbejdscelle for lean manufacturing"
description: "Hvis du vil tilpasse underleverandørarbejde for lean manufacturing, skal du oprette en arbejdscelle, der er tilknyttet den kreditor, der leverer arbejdet."
author: cvocph
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 41cf47bb0578d9c854bd0dfc078b5b6fb559abca
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-subcontracted-work-cell-for-lean-manufacturing"></a>Oprette en underleverandørarbejdscelle for lean manufacturing

[!include[task guide banner](../../includes/task-guide-banner.md)]

Hvis du vil tilpasse underleverandørarbejde for lean manufacturing, skal du oprette en arbejdscelle, der er tilknyttet den kreditor, der leverer arbejdet. En underleverandørarbejdscelle er knyttet til kreditoren gennem tilknytningen af en ressource af typen Kreditor. Hvis du afspiller denne optagelse i USMF-demofirmaet, kan du vælge kreditorkonto-ID'et 1002 og lokation 1.


## <a name="create-a-vendor-resource"></a>Oprette en leverandørressource
1. Gå til ressourcer.
2. Klik på Ny.
3. Skriv en værdi i feltet Ressource.
4. Skriv en værdi i feltet Beskrivelse.
5. Vælg Kreditor i feltet Type.
6. Klik på rullelisten i feltet Kreditor for at åbne opslaget.

## <a name="create-the-resource-group"></a>Oprette ressourcegruppen
1. Gå til Ressourcegrupper.
2. Klik på Ny.
3. Indtast en værdi i feltet Ressourcegruppe.
4. Skriv en værdi i feltet Beskrivelse.
5. Klik på rullelisten i feltet Sted for at åbne opslaget.
    * Vælg det sted, som arbejdscellen skal tildeles til. I teorien kan et sted repræsentere et enkelt sted, der styres af en leverandør. I de fleste tilfælde tildeles underleverandørressourcer kun til det sted, der bestiller underleverandørarbejdet. Bemærk, at ind- og udlageringsstederne for arbejde udført af underleverandørens arbejdsceller skal være samme sted.  
6. Skriv en værdi i feltet Sted.
7. @SysTaskRecorder:_RequestClose
8. Markér eller fjern markeringen i afkrydsningsfeltet Arbejdscelle.
9. Klik på rullelisten i feltet Indlagringssted for at åbne opslaget.
    * Vælg det lagersted og lokalitet, der bruges til at forberede materialer til den kreditoradministrerede arbejdscelle. I mange tilfælde tilpasses lagerstedet og lokaliteten ved hjælp af et separat lagersted pr. leverandør og én lokalitet pr. arbejdscelle.  
10. Klik på rullelisten i feltet Indlagringslokation for at åbne opslaget.
11. Klik på rullelisten i feltet Udlagringssteder for at åbne opslaget.
    * Angiv det lagersted og lokalitet, hvor materialet bogføres, når underleverandørens aktiviteter for arbejdscellen bogføres. Lagerstedet og lokaliteten kan være på leverandørens lokalitet, hvis leverandøren rapporterer kanban-job. Lagerstedet og lokaliteten kan også være den modtagende lokalitet, der er knyttet til det næste trin i produktionsflowet.  
12. Klik på rullelisten i feltet Udlagringslokation for at åbne opslaget.
13. Udvid eller skjul sektionen Kalendere.
14. Klik på Tilføj.
15. Klik på rullelisten i feltet Kalender for at åbne opslaget.
    * Knyt arbejdstidskalenderen for arbejdscellen til ressourcegruppen. Det anbefales, at du for vigtige ressourcer definerer bestemte kalendere, der repræsenterer de nøjagtige arbejdstider og relateret kapacitet for arbejdscellen eller leverandørlokaliteten.  
16. Udvid eller skjul sektionen Ressourcer.
17. Klik på Tilføj.
    * En underleverandørressourcegruppe skal have en tilknyttet ressource af typen Leverandør, der knytter ressourcegruppen til kreditorkontoen.  
18. Klik på rullelisten i feltet Ressource for at åbne opslaget.
    * Vælg eller angiv den leverandørressource, du oprettede i forrige underopgave.  
19. Udvid eller skjul afsnittet Arbejdscelles kapacitet.
20. Klik på Tilføj.
    * En arbejdscelle skal have en defineret kapacitet. I dette eksempel skal vi oprette en gennemløbskapacitet på 100 styk pr. standardarbejdsdag.  
21. Klik på rullelisten i feltet Produktionsflowmodel for at åbne opslaget.
22. Vælg en indstilling i feltet Kapacitetsperiode.
23. Indtast et tal i feltet Gennemsnitligt antal gennemløb.
24. Klik på rullelisten i feltet Enhed for at åbne opslaget.
25. ResolveChanges enheden.


