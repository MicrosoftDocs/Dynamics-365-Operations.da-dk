---
title: Delegere workflowopgaver i en arbejdsgang
description: Hvis du planlægger at være væk fra kontoret eller af anden årsag ikke kan udføre workflowopgaver, kan du delegere eller tildele dine workflowopgaver til andre brugere.
author: ChrisGarty
manager: AnnBe
ms.date: 07/07/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 96777b66645453bc909bd4053e2724a37771d5d6
ms.sourcegitcommit: 561d06c2a74602dfaa40334d8afac5053aebc055
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/07/2020
ms.locfileid: "3541079"
---
# <a name="delegate-work-items-in-a-workflow"></a>Delegere arbejdselementer i en arbejdsgang

[!include [banner](../../includes/banner.md)]

## <a name="manually-delegate-a-work-item"></a>Manuel delegering af et arbejdselement

For at delegere et individuelt arbejdselement skal du vælge indstillingen **Deleger** i menuen **Arbejdsgang** og derefter indtaste den bruger, som elementet skal delegeres til, samt en bemærkning hertil. Dette vil omfordele arbejdselementet til den pågældende bruger, således at denne kan udføre opgaven.

## <a name="manually-delegate-multiple-work-items"></a>Manuelt delegere flere arbejdselementer

Flere arbejdselementer kan delegeres sammen på siden **Arbejdselementer, der er tildelt mig**. Følgende arbejdsgangstyper er berettiget til massedelegering: arbejdsgang til godkendelse af købsaftaler, arbejdsgang til indkøbsordrer, gennemgang af indkøbsrekvisitioner og arbejdsgang til kreditorfakturaer. Funktionen **Deleger flere arbejdselementer** er som standard deaktiveret og kan aktiveres under **Arbejdsområder > Funktionsstyring**. Kontakt systemadministratoren for at få hjælp til at aktivere denne funktion.
1.  Gå til **Almindeligt > Almindeligt > Arbejdselementer > Arbejdselementer, der er tildelt til mig**.
2.  Vælg de arbejdselementer, der skal delegeres.
3.  Klik på menuen **Deler arbejdselementer**.
4.  Vælg den bruger, der skal delegeres arbejdselementer til, i feltet **Bruger**.
5.  Skriv en kommentar i feltet **Kommentar** for at forklare, hvorfor du delegerer arbejdselementer.
6.  Klik på knappen **Deleger arbejdselementer** for at fuldføre delegeringen af arbejdselementet.

## <a name="automatically-delegate-work-items"></a>Automatisk delegering af arbejdselementer

Hvis du har planer om at være væk fra kontoret eller på anden vis ikke er til rådighed i en periode, kan du automatisk delegere nye arbejdselementer til andre brugere ved hjælp af siden **Brugerindstillinger**.

### <a name="set-up-automatic-delegation"></a>Konfigurere automatisk delegering
1. Gå til **Generelt > Opsætning > Brugerindstillinger**.
2. Klik på fanen **Arbejdsgang**. Kontrollér, at afsnittet Delegering er udvidet. Hvis du vil konfigurere systemet til automatisk at delegere dine workflowopgaver til andre brugere, skal du oprette delegeringsregler, som angiver, hvornår bestemte workflowopgaver skal uddelegeres. Udfør følgende trin for at oprette en delegeringsregel:  
3. Klik på **Tilføj**.
4. Vælg en indstilling i feltet **Omfang**:
    - Alle – Deleger alle workflowopgaver, der er tildelt dig.
    - Modul – Deleger kun de arbejdselementer, der er relateret til en bestemt type arbejdsgang. Hvis du vælger denne indstilling, skal du også vælge arbejdsgangens type i feltet **Navn**.
    - Arbejdsgang – Deleger kun de arbejdselementer, der er relateret til en bestemt arbejdsgang. Hvis du vælger denne indstilling, skal du vælge arbejdsgangen i feltet **Navn**.  
5. I feltet **Navn**:
    - Vælg destinationsmodulet for området **Modul**.
    - For området **Arbejdsgang** skal du vælge destinationsarbejdsgangen.
6. Vælg den bruger, der skal delegeres arbejdselementer til, i feltet **Deleger**. Brug felterne **Startdato/-tidspunkt** og **Slutdato/-tidspunkt** til at angive, hvornår du ønsker, at arbejdselementerne skal delegeres automatisk.  
7. Angiv en dato og et klokkeslæt i feltet **Startdato/-klokkeslæt**.
8. Angiv en dato og et klokkeslæt i feltet **Slutdato/-klokkeslæt**.
9. Markér afkrydsningsfeltet **Aktiveret** for at aktivere delegeringsreglen. 
10. Skriv en kommentar i feltet **Kommentar** for at forklare, hvorfor du delegerer arbejdselementer.
