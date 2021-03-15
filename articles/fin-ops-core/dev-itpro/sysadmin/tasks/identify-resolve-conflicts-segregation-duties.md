---
title: Identificere og løse konflikter i opdeling af opgaver
description: Dette emne forklarer, hvordan du identificerer og løser konflikter i opdelingen af opgaver.
author: peakerbl
manager: AnnBe
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesConflict, SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: deff97c7728db91089d3ea834d15de738da500fa
ms.sourcegitcommit: 316200579dd5b04ad76f276a2ed6b0f55fa8c812
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/05/2021
ms.locfileid: "4826362"
---
# <a name="identify-and-resolve-conflicts-in-segregation-of-duties"></a>Identificere og løse konflikter i opdeling af opgaver

[!include [banner](../../includes/banner.md)]

Dette emne forklarer, hvordan du identificerer og løser konflikter i opdelingen af opgaver. Du kan oprette regler for at adskille opgaver, der skal udføres af forskellige brugere. Dette begreb kaldes opdeling af opgaver. Hvis definitionen af en sikkerhedsrolle eller rolletildelinger for en bruger overtræder reglerne, logføres konflikten. Alle konflikter skal løses af administratoren. Fuldfør følgende procedure for at identificere og løse konflikter.

Når der er tilføjet en regel, skal du kontrollere, at alle eksisterende roller overholder angivne standarder. 

## <a name="verify-that-existing-roles-and-duties-comply-with-new-rules-for-segregation-of-duties"></a>Kontrollér, at ekisterende roller og opgaver overholder nye regler for opdeling af opgaver.
1. Gå til **Systemadministration** > **Sikkerhed** > **Opdeling af opgaver** > **Regler for opdeling af opgaver**.
3. Vælg **Bekræft opgaver og roller**. Hvis nogen regler overtræder reglerne, vises en meddelelse, som indeholder navnet på reglen, rollen og navnene på de opgaver, der er i konflikt. Roller, der er i konflikt, skal ændres ved hjælp af **Sikkerhedskonfiguration** og kan ikke indeholde opgaver, der er i konflikt. Hvis ingen roller overtræder den valgte regel, angiver en meddelelse, at alle roller overholder angivne standarder.   

> [!NOTE]
> Valideringen udføres kun for den valgte regel. Det er vigtigt at validere overholdelse af angivne standarder for hver regel.   

Når du opretter eller redigerer en rolle, gennemtvinges reglerne for opdeling af opgaver automatisk. Du kan ikke tildele opgaver, der er i konflikt, til en rolle.

Kontrollér derefter, at alle eksisterende rolletildelinger overholder angivne standarder.

## <a name="verify-that-user-role-assignments-comply-with-new-rules-for-segregation-of-duties"></a>Kontrollér, at brugerrolletildelinger overholder de nye regler for opdeling af opgaver.
1. Gå til **Systemadministration > Sikkerhed > Opdeling af opgaver > Bekræft overholdelse af brugerrolletildelinger**.
2. Vælg **OK**. En besked viser resultaterne af valideringen. Konflikter logføres på siden **Uløste konflikter i opdeling af opgaver**.   

Når du tildeler brugere til roller, gennemtvinges reglerne for opdeling af opgaver automatisk. Hvis du forsøger at tildele en bruger til roller, der indeholder opgaver, som er i konflikt, modtager du en fejlmeddelelse. Derefter skal du løse problemet ved at afvise eller tillade yderligere rolletildeling. Den ekstra rolle tildeles, når tildelingen er tilladt. 

> [!NOTE]
> Konflikter kontrolleres i øjeblikket ikke for brugere, der er tildelt roller baseret på Active Directory-domænegrupperne.

## <a name="view-and-resolve-conflicting-user-role-assignments"></a>Få vist og løse modstridende brugerrolletildelinger
1. Gå til **Systemadministration** > **Sikkerhed** > **Opdeling af opgaver** > **Uløste konflikter i opdeling af opgaver**. 
2. Vælg en konflikt, og klik derefter på en af følgende handlinger: 

  - **Afvis tildeling**: Dette vil afvise tildelingen af brugeren til den ekstra sikkerhedsrolle. Hvis du afviser en automatisk rolletildeling, markeres brugeren som udelukket fra rollen. Den udelukkede bruger har ikke den adgang, der er tilknyttet rollen, og kan ikke tildeles rollen, før administratoren fjerner udelukkelsen. 
-  **Tillad tildeling**: Dette tilsidesætter konflikten og giver brugeren tilladelse til at få tildelt den ekstra sikkerhedsrolle. Hvis du tilsidesætter en konflikt, skal du angive en begrundelse i feltet **Årsag til tilsidesættelse**. Alle tilsidesatte rolletildelinger kan ses på siden **Konflikter i opdeling af opgaver**.  

> [!NOTE]
> Hvis der er angivet flere konflikter for samme bruger, skal du vælge brugerposten og evaluere tildelte roller på siden **Brugere**. Du kan undgå denne konflikt ved at validere hver regel, efter at den er tilføjet eller redigeret.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]