---
title: Spore kilder til kandidatprofiler og -ansøgninger
description: Dette emne indeholder oplysninger om at spore kilden til kandidatprofiler og ansøgninger.
author: hachandr
manager: AnnBe
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: ebc82ada31d2803800358cd9aecfe389ada8f0dc
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517646"
---
# <a name="track-sources-for-candidate-profiles-and-applications"></a>Spore kilder til kandidatprofiler og -ansøgninger 

[!include[banner](../includes/banner.md)]

> [!NOTE] 
> De funktioner, der er angivet under dette emne, er tilgængelige som en del af en gennemgang af en eksempelversion. Indholdet og funktionaliteten kan blive ændret. For at anvende denne funktion skal du anmode en administrator om at aktivere den ved hjælp af **Administratorindstillinger** i Attract. I en kommende udgivelse stilles kildesporingsrapporter til rådighed. Du kan finde yderligere oplysninger under [Få adgang til funktioner i prøveversioner af Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/access-preview-feature).

Når en kandidat søger et job, sporer Attract automatisk kilden til dennes ansøgninger og giver dig værdifulde oplysninger, der kan hjælpe dig med at målrette din rekrutteringsindsats. Rekrutteringsmedarbejdere og ansættelsesansvarlige kan endvidere vælge en ansøgningskilde, når de manuelt tilføjer en kandidat til et job eller en talentpulje.

Du kan se ansøgningskilden i detaljerne om ansøgningsaktivitet under fanen **Aktivitet** samt i ansøgningshistorikken, der er tilgængelig under **Profil** i talentpuljer. Du kan finde en kandidats profilkilde i kandidatens detaljer under fanen **Profil** i både ansøgninger og talentpuljer.

> [!NOTE] 
> Du kan finde processkabeloner i [Tilføjelsesprogrammet Omfattende ansættelser](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/attract-comprehensive-hiring).

## <a name="pre-configured-sources"></a>Forudkonfigurerede kilder

Standardkildelisten omfatter fælles ansøgningskilder. Visse kildetyper såsom **Jobportal** og **Socialt netværk** har yderligere kildedetaljer. Eksempelvis omfatter **Socialt netværk** Facebook og Twitter. Kildetypen **Henvisning** gør det muligt for dig at angive en intern medarbejder som reference. Standardkildelisten omfatter følgende forudkonfigurerede kilder:

-   Attract's karrierewebsted

-   Forvaltning

-   Karrieremesse

-   Virksomhedens markedsføring

-   Konferencer og messer

-   Professionel tilknytning

-   Jobportal

    -   Indeed

    -   Seek

    -   CareerBuilder

    -   Google Jobs

    -   Xing

    -   Glassdoor

    -   Monster Jobs

-   Magasiner og publikationer

-   Socialt netværk

    -   Facebook

    -   Twitter

-   Universitetsrekruttering

-   LinkedIn

-   Annoncer

-   Henvisning

-   Tilføjet af rekrutteringsmedarbejder

-   Diverse

## <a name="customize-the-source-list"></a>Tilpas kildelisten 

Du kan udvide kildelisten til at omfatte yderligere ansøgningskilder. For at tilpasse denne liste skal du følge vejledningen i [Udvidede indstillingssæt i Attract](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/extensibility-attract#extending-option-sets-in-attract). Rediger enheden **TalentKilde** for at omfatte yderligere kilder. 

For at undgå at brugergrænsefladen (UI) påvirkes negativt, må du ikke redigere eller slette **TalentKategori**-enum-værdierne (undtagen navne) for følgende:

- **Henvisning**
- **LinkedIn**
- **Diverse**

Du kan i stedet udvide **TalentKilde**-enum for at tilføje andre kildetyper.
