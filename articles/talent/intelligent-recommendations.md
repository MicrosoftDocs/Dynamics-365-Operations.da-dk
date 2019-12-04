---
title: Intelligente anbefalinger i Attract
description: I denne artikel beskrives, hvordan maskinel indlæring kan bruges til at give anbefalinger om job og jobkandidater i Microsoft Dynamics 365 Talent - Attract.
author: andreabichsel
manager: AnnBe
ms.date: 05/16/2019
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
ms.openlocfilehash: fa06821c98e42dcd8590a764db9beb4a5c33fca2
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832785"
---
# <a name="intelligent-recommendations-in-attract"></a>Intelligente anbefalinger i Attract

[!include [banner](includes/banner.md)]

Maskinel indlæring kan hjælpe rekrutteringsmedarbejdere og ansættelsesansvarlige med at identificere de bedste kandidater til en stilling. Det kan også hjælpe jobkandidater med finde den stilling, der passer bedst til deres profil og interesser. Når disse funktioner bruges, og der gives tilbagemeldinger, forbedres anbefalingerne.

> [!NOTE] 
> - Funktionerne til intelligente anbefalinger er kun tilgængelige med [Tilføjelsesprogrammet Omfattende ansættelser](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).
> - De funktioner, der er angivet under dette emne, er tilgængelige som en del af en gennemgang af en eksempelversion. Indholdet og funktionaliteten kan blive ændret. For at anvende denne funktion skal du anmode en administrator om at aktivere den ved hjælp af **Administration** i Attract. Angiv indstillingerne for **Kandidatanbefaling**, **Jobanbefaling** og **Kandidatemneanbefaling** til **Til**. Du kan finde yderligere oplysninger under [Få adgang til funktioner i prøveversioner af Microsoft Dynamics 365 Talent](./access-preview-feature.md). 


## <a name="candidate-recommendations"></a>Kandidatanbefalinger

Da jobopslag kan tiltrække hundredvis af ansøgere, kan det være vanskeligt for rekrutteringsmedarbejdere og ansættelsesansvarlige at finde de kandidater, hvis færdigheder og baggrund bedst svarer til stillingen. Ved at analysere korrelation mellem stillingsbeskrivelsen og -kravene og data fra kandidaternes cv'er og profiler kan maskinel indlæring bruges til at producere kandidatanbefalinger. Kandidatanbefalinger kan hjælpe rekrutteringsmedarbejdere og ansættelsesansvarlige med at identificere de største talenter og hurtigere flytte dem til samtalestadiet. Hvis der til et job er mere end ti ansøgere eller jobkandidater, der har CV'er eller fuldstændige profiler, vises de ansøgere eller jobkandidater, der bedst opfylder kravene til jobbet, i sektionen **Ansøgere, der skal tages i betragtning** på **Job**-siden.

For enhver anbefalet kandidat kan du vælge **Vis kandidat** på kandidatkortet for at gennemgå kandidatens profil og handle på vedkommendes ansøgning. Du kan bruge ellipseknappen (**...**) til at åbne kandidatens profil under en ny fane. Du kan også bruge ellipseknappen til at give tilbagemeldinger om anbefalingen. På denne måde hjælper du med at finjustere anbefalingsprogrammet og forbedre fremtidige anbefalinger. Eventuelle anbefalinger, du ikke bryder dig om, fjernes fra sektionen **Ansøgere, der skal tages i betragtning**, når du opdaterer **Job**-siden. Du kan bruge tilbagemeldingskortet til at angive, hvorfor du ikke fandt anbefalingen nyttig.

## <a name="job-recommendations"></a>Stillingsanbefalinger 

Når en potentiel medarbejder anvender karrierewebstedet til at ansøge om et job, anbefaler Attract andre ledige stillinger i organisationen. Disse anbefalinger er baseret på tidligere ansøgninger og på kandidatemnets CV eller kandidatprofil. Derfor hjælper stillingsanbefalinger jobkandidater med hurtigt at identificere de job, der passer til dem. Stillingsanbefalinger vises for jobkandidater, hvis der er opslået mere end ti job på karrierewebstedet. Jobkandidater kan åbne detaljerne i et jobopslag fra anbefalingskortet. De kan også give tilbagemeldinger om en anbefaling for at forbedre fremtidige anbefalinger.

## <a name="prospect-recommendations"></a>Kandidatemneanbefalinger 

Det kan tage lang tid at gennemgå tidligere ansøgere og hele dit talentnetværk, når en ny stilling skal besættes. Attract kan hjælpe dig med dette ved at anvende intelligente algoritmer til maskinel indlæring. Det betyder, at Attract gennemgår alle kandidaterne og udarbejder forslag til, hvem der er et godt match, så snart du har oprettet jobbet. For at se disse anbefalinger skal du aktivere stadiet **Kandidatemne** for det pågældende job. Det kan tage op til et minut for Attract at scanne hele din kandidatdatabase igennem og udarbejde anbefalinger.

Anbefalingerne vises som kort i fanen **Kandidatemner** for alle jobs, der har stadiet **Kandidatemne** aktiveret. Disse kort oplister de færdigheder, der er lokaliseret i kandidatemnets profil, samt oplysninger om alle uddannelsesmæssige kvalifikationer. Hvis du finder en anbefaling, som du kan lide, kan du tilføje kandidaten til det pågældende job som et kandidatemne.

> [!NOTE]
> Hvis du først for nyligt er begyndt at anvende Attract, er du nødt til at vente, indtil du har 10 eller flere ansøgere med komplette profiler eller CV'er, før du kan benytte denne funktion.

For at undgå potentielle partiskhed i anbefalingerne scanner Attract alene kandidatprofilerne i relation til færdigheder, kvalifikationer og andre nøgleord, som matcher stillingsbeskrivelsen. Derudover fjerner Attract personlige oplysninger fra kandidatens profil forud for vurderingen.
