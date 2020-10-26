---
title: Identificere og løse konflikter i opdeling af opgaver
description: Dette emne forklarer, hvordan du identificerer og løser konflikter i opdelingen af opgaver.
author: maertenm
manager: AnnBe
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesConflict, SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 69dabb44ef08bf798b86cd031536146880c8fd40
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982472"
---
# <a name="identify-and-resolve-conflicts-in-segregation-of-duties"></a>Identificere og løse konflikter i opdeling af opgaver

[!include [banner](../../includes/banner.md)]

Dette emne forklarer, hvordan du identificerer og løser konflikter i opdelingen af opgaver. Du kan oprette regler for at adskille opgaver, der skal udføres af forskellige brugere. Dette begreb kaldes opdeling af opgaver. Hvis definitionen af en sikkerhedsrolle eller rolletildelinger for en bruger overtræder reglerne, logføres konflikten. Alle konflikter skal løses af administratoren. Fuldfør følgende procedure for at identificere og løse konflikter. Det demodatafirma, der bruges til at oprette denne procedure, er USMF.


## <a name="verify-whether-user-role-assignments-comply-with-new-rules-for-segregation-of-duties"></a>Kontrollér, om brugerrolletildelinger overholder de nye regler for opdeling af opgaver.
1. Gå til **Navigationsrude > Moduler > Systemadministration > Sikkerhed > Opdeling af opgaver > Bekræft overholdelse af brugerrolletildelinger**.
2. Vælg **OK**. En besked viser resultaterne af valideringen. Såfremt der er en konflikt, kan du åbne siden **Brugere** og ændre brugerens tildelte roller. Konflikter registreres endvidere på siden **Konflikter relateret til opdeling af opgaver**. For at køre verifikationsprocessen som et batchjob skal du vælge **Batchbehandling** og dernæst angive de andre batchparametre. Når du har kørt batchjobbet, kan du gennemse konflikterne på siden **Konflikter relateret til opdeling af opgaver**.  

## <a name="view-and-resolve-conflicting-user-role-assignments"></a>Få vist og løse modstridende brugerrolletildelinger
1. Gå til **Navigationsrude > Moduler > Systemadministration > Sikkerhed > Opdeling af opgaver > Konflikter relateret til opdeling af opgaver.** Vælg en konflikt, og vælg dernæst en af følgende knapper: **Afvis tildeling – Afvis brugerens tildeling af den ekstra sikkerhedsrolle**. Hvis du afviser en automatisk rolletildeling, markeres brugeren som udelukket fra rollen. Den udelukkede bruger har ikke den adgang, der er tilknyttet rollen, og brugeren kan ikke tildeles rollen, før administratoren fjerner udelukkelsen. Tillad tildeling – **Tilsidesæt** konflikten, og giv brugeren tilladelse til at få tildelt begge sikkerhedsroller. Hvis du tilsidesætter en konflikt, skal du angive en begrundelse i feltet **Årsag til tilsidesættelse**.  
2. Luk siden.
3. Gå til **Navigationsrude > Moduler > Systemadministration > Sikkerhed > Opdeling af opgaver > Uløste konflikter relateret til opdeling af opgaver.** Vælg en konflikt, og vælg dernæst en af følgende knapper: **Afvis tildeling – Afvis brugerens tildeling af den ekstra sikkerhedsrolle**. Hvis du afviser en automatisk rolletildeling, markeres brugeren som udelukket fra rollen. Den udelukkede bruger har ikke den adgang, der er tilknyttet rollen, og brugeren kan ikke tildeles rollen, før administratoren fjerner udelukkelsen. Tillad tildeling – **Tilsidesæt** konflikten, og giv brugeren tilladelse til at få tildelt begge sikkerhedsroller. Hvis du tilsidesætter en konflikt, skal du angive en begrundelse i feltet **Årsag til tilsidesættelse**.    
4. Luk siden.

## <a name="verify-whether-existing-roles-comply-with-new-rules-for-segregation-of-duties"></a>Kontrollér, om ekisterende roller overholder nye regler for opdeling af opgaver.
1. Gå til **Navigationsrude > Moduler > Systemadministration > Sikkerhed > Opdeling af opgaver > Regler for opdeling af opgaver.** Vælg en regel.  
2. Vælg **Bekræft opgaver og roller**. Hvis nogen eksisterende roller overtræder den valgte regel, vises en meddelelse, som indeholder navnet på rollen og navnene på de opgaver, der er i konflikt. Administratoren skal enten angive afhjælpningen af sikkerhedsrisikoen eller ændre rollen, så den ikke overtræder reglerne for opdeling af opgaver. Hvis ingen roller overtræder den valgte regel, angiver en meddelelse, at alle roller er i overensstemmelse.  

