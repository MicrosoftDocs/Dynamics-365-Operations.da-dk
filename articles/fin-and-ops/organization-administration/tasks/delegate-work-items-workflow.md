---
title: Delegere workflowopgaver i en arbejdsgang
description: Hvis du planlægger at være væk fra kontoret eller af anden årsag ikke kan udføre workflowopgaver, kan du delegere eller tildele dine workflowopgaver til andre brugere.
author: jasongre
manager: AnnBe
ms.date: 07/01/2019
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
ms.openlocfilehash: 44dc747543e32b54729d12c89a401b0187e25a61
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916409"
---
# <a name="delegate-work-items-in-a-workflow"></a>Delegere arbejdselementer i en arbejdsgang

[!include [task guide banner](../../includes/task-guide-banner.md)]

## <a name="manually-delegate-a-work-item"></a>Manuel delegering af et arbejdselement

For at delegere et individuelt arbejdselement skal du vælge indstillingen **Deleger** i menuen **Arbejdsgang** og derefter indtaste den bruger, som elementet skal delegeres til, samt en bemærkning hertil. Dette vil omfordele arbejdselementet til den pågældende bruger, således at denne kan udføre opgaven.

## <a name="automatically-delegate-work-items"></a>Automatisk delegering af arbejdselementer

Hvis du har planer om at være væk fra kontoret eller på anden vis ikke er til rådighed i en periode, kan du automatisk delegere nye arbejdselementer til andre brugere ved hjælp af siden **Brugerindstillinger**.

### <a name="set-up-automatic-delegation"></a>Konfigurere automatisk delegering
1. Gå til **Generelt > Opsætning > Brugerindstillinger**.
2. Klik på fanen **Arbejdsgang**. Kontrollér, at afsnittet Delegering er udvidet. Hvis du vil konfigurere systemet til automatisk at delegere dine workflowopgaver til andre brugere, skal du oprette delegeringsregler, som angiver, hvornår bestemte workflowopgaver skal uddelegeres. Udfør følgende trin for at oprette en delegeringsregel:  
3. Klik på **Tilføj**.
4. Vælg en indstilling i feltet **Omfang**.
    - Alle – Deleger alle workflowopgaver, der er tildelt dig.
    - Modul – Deleger kun de arbejdselementer, der er relateret til en bestemt type arbejdsgang. Hvis du vælger denne indstilling, skal du også vælge arbejdsgangens type i feltet Navn.
    - Arbejdsgang – Deleger kun de arbejdselementer, der er relateret til en bestemt arbejdsgang. Hvis du vælger denne indstilling, skal du vælge arbejdsgangen i feltet Navn.  
5. Vælg den bruger, der skal delegeres arbejdselementer til, i feltet **Deleger**. Brug felterne Startdato/-tidspunkt og Slutdato/-tidspunkt til at angive, hvornår du ønsker, at arbejdselementerne skal delegeres automatisk.  
6. Angiv en dato og et klokkeslæt i feltet **Startdato/-klokkeslæt**.
7. Angiv en dato og et klokkeslæt i feltet **Slutdato/-klokkeslæt**.
8. Markér afkrydsningsfeltet **Aktiveret** for at aktivere delegeringsreglen. Hvis du valgte **Modul** som Omfang, skal du vælge modulet i feltet Navn. Hvis du har valgt **Arbejdsgang** som Omfang, skal du vælge den specifikke arbejdsgang, der skal delegeres, i feltet Navn.  
9. Skriv en kommentar i feltet **Kommentar** for at forklare, hvorfor du delegerer arbejdselementer.

