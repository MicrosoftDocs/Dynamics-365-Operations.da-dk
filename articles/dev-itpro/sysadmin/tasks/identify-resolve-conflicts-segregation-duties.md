--- 
title: "Identificere og løse konflikter i opdeling af opgaver"
description: "Du kan oprette regler for at adskille opgaver, der skal udføres af forskellige brugere."
author: maertenm
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c3a366ea4b558ba4e4af7336992dbb091b0b1414
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="identify-and-resolve-conflicts-in-segregation-of-duties"></a>Identificere og løse konflikter i opdeling af opgaver

[!include [task guide banner](../../includes/task-guide-banner.md)]

Du kan oprette regler for at adskille opgaver, der skal udføres af forskellige brugere. Dette begreb kaldes opdeling af opgaver. Hvis definitionen af en sikkerhedsrolle eller rolletildelinger for en bruger overtræder reglerne, logføres konflikten. Alle konflikter skal løses af administratoren. Fuldfør følgende procedure for at identificere og løse konflikter. Det demodatafirma, der bruges til at oprette denne procedure, er USMF.


## <a name="verify-whether-user-role-assignments-comply-with-new-rules-for-segregation-of-duties"></a>Kontrollér, om brugerrolletildelinger overholder de nye regler for opdeling af opgaver.
1. Gå til Systemadministration > Sikkerhed > Opdeling af opgaver > Bekræft overholdelse af brugerrolletildelinger.
2. Klik på OK.
    * En besked viser resultaterne af valideringen.     Hvis der opstår en konflikt, kan du åbne siden Brugere og ændre brugerens rolletildelinger. Konflikter logføres også på siden Konflikter i opdeling af opgaver.     Hvis du vil køre bekræftelsesprocessen som et batchjob, skal du vælge Batchbehandling og derefter angive de andre batchparametre. Når kørslen er afsluttet, kan du gennemse konflikterne på siden Konflikter i opdeling af opgaver.  

## <a name="view-and-resolve-conflicting-user-role-assignments"></a>Få vist og løse modstridende brugerrolletildelinger
1. Gå til Systemadministration > Sikkerhed > Opdeling af opgaver > Konflikter i opdeling af opgaver.
    * Vælg en konflikt, og klik derefter på en af følgende knapper: Afvis tildeling – afvis tildelingen af brugeren til den ekstra sikkerhedsrolle. Hvis du afviser en automatisk rolletildeling, markeres brugeren som udelukket fra rollen. Den udelukkede bruger har ikke den adgang, der er tilknyttet rollen, og brugeren kan ikke tildeles rollen, før administratoren fjerner udelukkelsen.     Tillad tildeling – tilsidesæt konflikten, og tillad, at brugeren tildeles til begge sikkerhedsroller. Hvis du tilsidesætter en konflikt, skal du angive en årsag i feltet Årsag til tilsidesættelse.  
2. Luk siden.
3. Gå til Systemadministration > Sikkerhed > Opdeling af opgaver > Uløste konflikter i opdeling af opgaver.
    * Vælg en konflikt, og klik derefter på en af følgende knapper: Afvis tildeling – afvis tildelingen af brugeren til den ekstra sikkerhedsrolle. Hvis du afviser en automatisk rolletildeling, markeres brugeren som udelukket fra rollen. Den udelukkede bruger har ikke den adgang, der er tilknyttet rollen, og brugeren kan ikke tildeles rollen, før administratoren fjerner udelukkelsen.     Tillad tildeling – tilsidesæt konflikten, og tillad, at brugeren tildeles til begge sikkerhedsroller. Hvis du tilsidesætter en konflikt, skal du angive en årsag i feltet Årsag til tilsidesættelse.    
4. Luk siden.

## <a name="verify-whether-existing-roles-comply-with-new-rules-for-segregation-of-duties"></a>Kontrollér, om ekisterende roller overholder nye regler for opdeling af opgaver.
1. Gå til Systemadministration > Sikkerhed > Opdeling af opgaver > Regler for opdeling af opgaver.
    * Vælg en regel.  
2. Klik på Bekræft opgaver og roller.
    * Hvis nogen eksisterende roller overtræder den valgte regel, vises en meddelelse, som indeholder navnet på rollen og navnene på de opgaver, der er i konflikt. Administratoren skal enten angive afhjælpningen af sikkerhedsrisikoen eller ændre rollen, så den ikke overtræder reglerne for opdeling af opgaver.     Hvis ingen roller overtræder den valgte regel, angiver en meddelelse, at alle roller er i overensstemmelse.  


